FROM node:8

RUN apt-get update && apt-get install -y --no-install-recommends \
    graphicsmagick \
  && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY package*.json ./

RUN npm install && npm cache clean --force

COPY . .

ENV CHARCOAL_FACTOR=0.1

CMD [ "node", "index.js" ]
