# Instalação do software

1. Colocar todos os ficheiros e pastas numa pasta principal
2. Para compilar usa-se o seguinte comando

LINUX:  
`javac -d bin -cp libs/jsoup-1.15.4.jar:libs/sqlite-jdbc-3.7.2.jar @sources.txt`

WINDOWS:  
`javac -d bin -cp libs/jsoup-1.15.4.jar;libs/sqlite-jdbc-3.7.2.jar @sources.txt`

## Correr

### Class files

Para correr cada um dos programas usa-se (na pasta "bin/"):  

- Fila de URLS:

`java searchEngine.URLs.UrlQueue 2003 fila-urls`

- Downloader(s)

`java -cp .:../libs/jsoup-1.15.4.jar searchEngine.crawler.Downloader 2003 fila-urls 224.3.2.1 4321 dl1`

- SearchModule(s)

`java -cp .:../libs/sqlite-jdbc-3.7.2.jar searchEngine.search.SearchModule ../config.cfg`

- Barrel(s)

`java -cp .:../libs/sqlite-jdbc-3.7.2.jar searchEngine.barrel.Barrel 2000 barrel1 224.3.2.1 4321`

- Cliente

`java searchEngine.client.Client ../configCliente.cfg`

## Jar files

Para correr cada um dos artefactos usa-se (na pasta "bin/"):  

- Fila de URLS:

`java -jar URLQueue.jar 2003 fila-urls`

- Downloader(s)

`java -jar Downloader.jar 2003 fila-urls 224.3.2.1 4321 dl1`

- SearchModule(s)

`java -jar SearchModule.jar ../config.cfg`

- Barrel(s)

`java -jar Barrel.jar 2000 barrel1 224.3.2.1 4321`

- Cliente

`java -jar Client.jar ../configCliente.cfg`

## Spring boot

Configurar os ips de forma correta no applications.propreties que se encontra nos resources.

`./mvnw spring-boot:run`