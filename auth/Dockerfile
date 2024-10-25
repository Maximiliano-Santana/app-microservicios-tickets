FROM node:alpine

WORKDIR /app

# Copiamos solo package.json y package-lock.json primero para aprovechar la cache de Docker.
COPY package.json package-lock.json ./

# Ejecutamos npm install para instalar dependencias
RUN npm install --trace-warnings

# Copiamos el resto del código de la aplicación
COPY . .

# Comando para iniciar la aplicación
CMD ["npm", "start"]
