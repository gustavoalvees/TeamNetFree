# Team NetFree 
Repositorio cujo objetivo de ajudar usuarios de internet gratuita ( via tunnel ssh ), com criação de arquivos e utilização, sem fins lucrativos.

"internet ilimitada", "netfree", "vpn", são termos que tem objetivo de trazer para seu utilizador um método de acesso para internet, sem que o utilizador precise ter credítos para poder realizar pesquisas e jogos em geral, por meio de "tunnel de ssh", usando "headers" modificado que faça "modificação", no recebimento/envio de dados atráves de um SNI/TLS em conjuto com um servidor (pirata) com trafégo ilimitado, usando um payload virculado no mesmo ssh com dominio;


### Estrutura de um Payload
```
 
 < --- CloudFlare x CloudFront--- >
 <       Dominio Apenas ( Direct )  >
 
GET / HTTP/1.1[crlf]Host: {dominio}[crlf]Connection: Upgrade[crlf]Upgrade: Websocket[crlf][crlf]

 < --- CloudFlare x CloudFront--- >
 <          Server+Dominio        >
 
GET wss://{servidorssh}/ HTTP/1.1[crlf]Host:{ dominio}[crlf]Connection: Upgrade[crlf]Upgrade: Websocket[crlf][crlf]

 < --- CloudFront--- >
 <  Server+Dominio   >
GET sni://{SNI} HTTP/1.1[crlf]Host: {Dominio}[crlf]Connection: Upgrade[crlf]Upgrade: Websocket[crlf][crlf]

```

#### Termos
    >Dominio
        - Dominío é responsavel pelo redirencionamento do pacote TLS/WS para o servidor SSH ({dominio});
            Exemplos de dominios>
                - br1.seconvpn.tk
                - d1k34qllbexpyg.cloudfront.net
                - nasa.tl
                  - Entre outros...
    
    >Host
        - 
    
### Criação de arquivos...
```
    Hosts
      > Claro
      > Oi
      > Tim
      > Vivo
```
    
