FROM node:19-slim

# Copie apenas o package.json e package-lock.json para o diretório de trabalho
COPY ./Cars_BE_GIT/package*.json /app/cars-be/

# Defina o diretório de trabalho
WORKDIR /app/cars-be

# Instale as dependências
RUN npm install

# Copie o restante dos arquivos, exceto node_modules
COPY ./Cars_BE_GIT /app/cars-be

EXPOSE 8081

# Comando de entrada para iniciar o servidor
CMD ["npm", "start"]
