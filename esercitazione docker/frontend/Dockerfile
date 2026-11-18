FROM node AS build
WORKDIR /app
COPY . .
#install dependencies e costruiamo applicazione
RUN npm i 
#puntatore a binari già presenti in macchina
RUN ./node_modules/.bin/ng build

#Runtime stage, serviamo applicazione
FROM nginx
COPY --from=build /app/dist/SomeBankingFrontend/browser /usr/share/nginx/html

EXPOSE 4200