# Utiliser l'image officielle Nginx très légère
FROM nginx:alpine

# Copier les fichiers statiques du frontend vers le dossier public de Nginx
COPY . /usr/share/nginx/html

# Exposer le port 80 (qui sera ensuite redirigé vers le 3000 par docker-compose)
EXPOSE 80
