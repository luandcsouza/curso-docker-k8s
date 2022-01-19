## Referenciando para uma imagem no docker hub que possua as dependências do node e npm já instaladas https://hub.docker.com/_/node?tab=description&page=1&ordering=last_updated
FROM node:16

## Aqui eu defini o diretório de trabalho onde o conteúdo será armazenado e onde o build será executado
WORKDIR /src/app

## Aqui estou copiando os arquivs de packages do node para poder buildar a aplicação com as dependências especificadas nos arquivos
COPY package*.json ./

## Aqui estou baixando as dependências da aplicação
RUN npm install

## Aqui estou copiando todo o fonte para dentro do contêiner
COPY . .

## Liberando a porta 8080 para execução da aplicação
EXPOSE 8080

## Executando a aplicação
CMD [ "node", "server.js" ]
