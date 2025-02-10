FROM node:20.18-alpine3.20 AS builder
RUN apk add git
WORKDIR /web
RUN git clone https://github.com/alvarocastilla05/AngularPokemon.git .
RUN npm install -g @angular/cli
RUN cd ./Pokemon-APP && npm install
RUN cd ./Pokemon-APP && ng build --configuration production --aot

FROM nginx:alpine
WORKDIR /web
COPY --from=builder /web/Pokemon-APP/dist/pokemon-app/* .
RUN mv ./* /usr/share/nginx/html/
