# Img di partenza
FROM nginx:alpine

# Directory di lavoro
WORKDIR /usr/share/nginx/html

# Copiamo i file nel container
COPY index.html .

#porta esposta
EXPOSE 80

#Avvio 
CMD ["nginx", "-g", "daemon off;"]