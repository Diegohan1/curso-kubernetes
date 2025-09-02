FROM node:20-slim

# Directorio de trabajo
WORKDIR /app

# Copiar solo el código principal
COPY webui.js .

# Instalar dependencias necesarias
RUN npm install express redis@2.8.0

# Exponer puerto 80
EXPOSE 80

# Comando por defecto
CMD ["node", "webui.js"]
