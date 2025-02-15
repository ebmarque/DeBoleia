FROM node:19-slim

# Copie apenas o package.json e package-lock.json para o diretório de trabalho
COPY ./DeBoleia_BE_GIT/DeBoleia/package*.json /app/deboleia-be/

# Defina o diretório de trabalho
WORKDIR /app/deboleia-be

# Instale as dependências
RUN npm install

# Copie o restante dos arquivos, exceto node_modules
COPY ./DeBoleia_BE_GIT/DeBoleia /app/deboleia-be

EXPOSE 8082

# Comando de entrada
ENTRYPOINT [ "npm", "run", "start" ]
