# 1. Imagen base oficial de Node (versión ligera)
FROM node:20-alpine

# 2. Directorio de trabajo dentro del contenedor
WORKDIR /app

# 3. Copiar archivos de dependencias e instalarlas
COPY package*.json ./
RUN npm ci --only=production

# 4. Copiar el resto del código fuente
COPY . .

# 5. Documentar el puerto que usa la aplicación
EXPOSE 3000

# 6. Comando para iniciar el servidor
CMD ["npm", "start"]