FROM node:18
WORKDIR /app

COPY package.json package.json
COPY package-lock.json package-lock.json

# RUN npm install
RUN NODE_ENV=development npm i

COPY . .
RUN npm run build

CMD ["npx", "-y", "http-server", "-p", "8000", "/app/build"]