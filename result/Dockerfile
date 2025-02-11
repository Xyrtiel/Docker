# Utiliser une image officielle Node.js Alpine
FROM node:18-alpine

# Définir le répertoire de travail
WORKDIR /app

# Copier package.json et package-lock.json
COPY package.json .

# Installer les dépendances
RUN npm install --omit=dev

# Copier le code source (exclure node_modules avec .dockerignore)
COPY . .

# Exposer le port 80
EXPOSE 80

# Lancer l'application
CMD ["node", "app.js"]
