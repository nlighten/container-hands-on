FROM node:12 AS build-env
ADD app/. /app
WORKDIR /app
RUN npm install --production

FROM gcr.io/distroless/nodejs:12
COPY --from=build-env /app /app
WORKDIR /app
EXPOSE 3000
CMD ["hello.js"]
