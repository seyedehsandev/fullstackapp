FROM node:18

WORKDIR /opt/app

COPY ./package.json ./
COPY ./package-lock.json ./

RUN npm install

COPY . .

RUN npm run build

ENV NODE_ENV=production
ENV HOST=0.0.0.0
ENV PORT=1337

EXPOSE 1337

CMD ["npm", "run", "start"]