FROM node:18-alpine

# Définir le répertoire de travail
WORKDIR /result

# Copier les fichiers de l'application
COPY . .

# Installer les dépendances
RUN npm install

# Exposer le port pour le serveur Express
EXPOSE 3000

# Démarrer l'application Node.js
CMD ["node", "server.js"]
