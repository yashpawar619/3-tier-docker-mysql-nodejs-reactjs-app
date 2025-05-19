FROM node:20

WORKDIR /app

COPY package*.json ./

RUN npm install --force

COPY . .

RUN ls -l node_modules/.bin && npm ls react-scripts  # Debug line (optional)
RUN npm run build

EXPOSE 3001

CMD ["npx", "serve", "-s", "build"]