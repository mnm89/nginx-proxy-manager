## Builder
FROM node:18-alpine3.16 AS builder

WORKDIR /usr/src/app

COPY . .

RUN npm ci
RUN npm run build

## Final image
FROM node:18-alpine3.16

ENV NODE_ENV=production

WORKDIR /usr/src/app

COPY --from=builder /usr/src/app/dist/second-app/browser ./public

RUN npm install -g serve

# By default will serve static files on port 3000 
CMD ["serve","-s","public"]