FROM node:18-alpine

# Définir le répertoire de travail
WORKDIR /app

# Copier les fichiers de l'application
COPY package.json package-lock.json ./

# Installer les dépendances
RUN npm install --omit=dev

COPY . .

# Exposer le port pour le serveur Express
EXPOSE 80

# Démarrer l'application Node.js
CMD ["node", "server.js"]
