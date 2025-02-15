FROM node:19-slim

COPY ./DeBoleia_FE_GIT/package*.json /app/deboleia-fe/

WORKDIR /app/deboleia-fe

RUN npm install -y && \
    npm install -g @angular/cli

COPY ./DeBoleia_FE_GIT /app/deboleia-fe

EXPOSE 4200

ENTRYPOINT [ "ng", "serve", "--host", "0.0.0.0" ]
