FROM node:16

WORKDIR /usr/src/app

COPY . .

EXPOSE 3000

RUN npm ci

RUN CI=true npm test

RUN npm run build

CMD ["npm", "start"]