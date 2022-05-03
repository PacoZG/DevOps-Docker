FROM node:16

WORKDIR /usr/src/app

COPY . .

EXPOSE 5000

RUN npm install

RUN npm run build

RUN npm install -g serve

ENV REACT_APP_BACKEND_URL=http://localhost:8080

CMD ["serve", "-s", "-l", "5000", "build"]