FROM node:18
WORKDIR /app

COPY package.json package.json
COPY package-lock.json package-lock.json

RUN npm install
# RUN NODE_ENV=development npm i
RUN npm install axios

RUN NODE_ENV=development npm install --save react-bootstrap bootstrap@3
RUN npx browserslist@latest --update-db


COPY . .
RUN npm run build

CMD ["npx", "-y", "http-server", "-p", "8000", "/app/build"]