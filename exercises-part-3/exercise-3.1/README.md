# Implementation of exercise 3.1
- The repository/project used for this exercise can be found at [pacoder](https://github.com/PacoZG/pacoder)

# Development environment
## docker-compose.dev file configuration heroku-app deployment and docker-hub image deployment


## github pipeline file configuration
```yaml
name: pacoderzavala

on:
  push:
    branches:
      - master
  pull_request:
    branches: [ master ]
    types: [ opened, synchronize ]
  release:
    types: [published]

jobs:
  Pacoder_Zavala_app:
    runs-on: ubuntu-20.04
    steps:
      - uses: actions/checkout@v2
      - uses: actions/setup-node@v2
        with:
          node-version: '14.x'

      - name: Installing dependencies
        run: npm install
      - name: Prettify code
        run: npm run check-code-style
      - name: Building for production
        run: npm run build
      - name: Running Unit tests
        run: npm run test

      - name: Bump version and push tag
        uses: anothrNick/github-tag-action@1.33.0
        if: ${{ github.event_name == 'push' && !contains(join(github.event.commits.*.message, ', '), '#skip') }}
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          WITH_V: true
          DEFAULT_BUMP: '#patch'

      - name: Deployment to Heroku
        uses: akhileshns/heroku-deploy@v3.12.12 # This is the action
        if: ${{ github.event_name == 'push' && !contains(join(github.event.commits.*.message, ', '), '#skip') }}
        with:
          heroku_api_key: ${{secrets.HEROKU_API_KEY}}
          heroku_app_name: 'pacoderzavala' # Must be unique in Heroku
          heroku_email: 'sirpaquillo1@yahoo.com.mx'
          dontuseforce: false
          procfile: 'web: npm run production'
          healthcheck: 'https://pacoderzavala.herokuapp.com/health'
          checkstring: 'ok'
          delay: 5
          rollbackonhealthcheckfailed: true
  
  push_to_docker_hub:
    name: Push Docker image to Docker Hub
    runs-on: ubuntu-latest
    steps:
      - name: Check out the repo
        uses: actions/checkout@v3
      
      - name: Log in to Docker Hub
        uses: docker/login-action@v1
        with:
          username: ${{ secrets.DOCKERHUB_USERNAME }}
          password: ${{ secrets.DOCKERHUB_TOKEN }}
      
      - name: Build and push Docker image
        uses: docker/build-push-action@v2
        with:
          push: true
          tags: sirpacoder/pacoder_zavala_app:latest
        

```
## Dockerfile
```docker
FROM node:16

WORKDIR /usr/src/app

COPY . .

EXPOSE 3000

RUN npm install && CI=true npm test && npm run build

CMD ["npm", "start"]
```
___