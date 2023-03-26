# Base image
FROM node:14-alpine

# Set the working directory
WORKDIR /app

COPY package*.json ./

RUN npm install --silent

COPY . .

RUN npm run build

# Set environment variable
ENV NODE_ENV=production

EXPOSE 3000

CMD ["npm", "start"]