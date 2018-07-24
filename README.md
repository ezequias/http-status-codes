# Códigos de Status Http 

> Informações úteis sobre cada tipo do código http

*Inspirado por*

[![Mentioned in Awesome](https://awesome.re/mentioned-badge-flat.svg)](https://awesome.re)

## Lista de Códigos

A lista é separada por tipo.

### Informativo 1xx
- [100](http://httpstatus.es/100) - **Continue** - O cliente deve continuar com a requisição.
- [101](http://httpstatus.es/101) - **Switching Protocols** - O servidor está trocando protocolos.
- [102](http://httpstatus.es/102) - **Processing** - O servidor recebeu e está processando a requisição.
- [103](http://httpstatus.es/102) - **Processing** - O servidor recebeu e está processando a requisição.
- [122](http://httpstatus.es/102) - **Request-uri too long** - A URI é maior do que o limite máximo de 2083 caracteres.

### Sucesso 2xx
Estes códigos indicam sucesso. O corpo desta seção, caso exista, é o objeto retornado pela requisição. É um objeto no formato MIME. Ele está no formato MIME e e pode apenas estar nos formatos texto/plano, texto/html ou alguns dos formatos especificados como aceitáveis pela requisição.

- [200](http://httpstatus.es/200) - **Ok** - A requisição foi cumprida.
- [201](http://httpstatus.es/201) - **Created** - Após um comando POST, isto indica um sucesso mas a parte textual da linha da resposta indica a URI pelo qual o documento novo criado deve ser conhecido.
- [202](http://httpstatus.es/202) - **Accepted** - A requisição foi aceita para processameto mas o processamento não foi completado. A requisição pode, ou não, eventualmente ser aceita a medida que pode ser desabilitada quando o processo tiver sido iniciado. Não há instalação para retornos de status a partir de operações assíncronas como essa.
- [203](http://httpstatus.es/203) - **Partial Information** - Quando recebido a partir de um response de um comando GET, isto indica que a meta-informação não é um conjunto definitivo de objetos de um servidor com uma cópia do objeto mas de  this indicates that the returned metainformation is not a definitive set of the object from a server with a copy of the object, mas a sobreposição de uma web privada. Ele pode estar incluso em uma informação de anotação sobre o objeto por exemplo.
- [204](http://httpstatus.es/204) - **No Response** - O servidor recebeu a requisição mas não há informação para ser enviada de volta e o cliente deve permanecer na mesma visão de documento. Isto é basicamente para permitir a entrada de scripts sem a mudança do documento simultaneamente.
- [205](http://httpstatus.es/205) - **Reset Content** - A requisição foi processada, nenhum conteúdo retornado, resete a visão do documento.
- [206](http://httpstatus.es/206) - **Partial Content** - retorno parcial do resource devido ao cabeçalho da solicitação.
- [207](http://httpstatus.es/207) - **Multi-Status** - O XML, pode conter múltiplas e separadas respostas.
- [208](http://httpstatus.es/208) - **Already Reported** - resultados anteriormente retornados.
- [226](http://httpstatus.es/226) - **Im Used** - pedido cumprido, a resposta é manipulação de instâncias.

### Redirecionamento 3xx
The codes in this section indicate action to be taken (normally automatically) by the client in order to fulfill the request.

- [301](http://httpstatus.es/301) - **Moved** - The data requested has been assigned a new URI, the change is permanent. (N.B. this is an optimisation, which must, pragmatically, be included in this definition. Browsers with link editing capabiliy should automatically relink to the new reference, where possible)
- [302](http://httpstatus.es/302) - **Found** - The data requested actually resides under a different URL, however, the redirection may be altered on occasion (when making links to these kinds of document, the browser should default to using the Udi of the redirection document, but have the option of linking to the final document) as for "Forward".
- [303](http://httpstatus.es/303) - **Method** - Like the found response, this suggests that the client go try another network address. In this case, a different method may be used too, rather than GET.
- [304](http://httpstatus.es/304) - **Not Modified** - If the client has done a conditional GET and access is allowed, but the document has not been modified since the date and time specified in If-Modified-Since field, the server responds with a 304 status code and does not send the document body to the client.
- [305](http://httpstatus.es/305) - **Use Proxy** - Content located elsewhere, retrieve from there.
- [306](http://httpstatus.es/306) - **Switch Proxy** - Subsequent requests should use the specified proxy.
- [307](http://httpstatus.es/307) - **Temporary Redirect** - Connect again to different URI as provided.
- [308](http://httpstatus.es/308) - **Permanent Redirect** - Connect again to a different URI using the same method.

### Erros do lado do cliente 4xx
The 4xx codes are intended for cases in which the client seems to have erred, and the 5xx codes for the cases in which the server is aware that the server has erred. It is impossible to distinguish these cases in general, so the difference is only informational.

The body section may contain a document describing the error in human readable form. The document is in MIME format, and may only be in text/plain, text/html or one for the formats specified as acceptable in the request.

- [400](http://httpstatus.es/400) - **Bad Request** - The request had bad syntax or was inherently impossible to be satisfied.
- [401](http://httpstatus.es/401) - **Unauthorized** - The parameter to this message gives a specification of authorization schemes which are acceptable. The client should retry the request with a suitable [Authorization](http://www.w3.org/Protocols/HTTP/HTRQ_Headers.html#z9) header.
- [402](http://httpstatus.es/402) - **Payment Required** - The parameter to this message gives a specification of charging schemes acceptable. The client may retry the request with a suitable ChargeTo header.
- [403](http://httpstatus.es/403) - **Forbidden** - The request is for something forbidden. Authorization will not help.
- [404](http://httpstatus.es/404) - **Not Found** - The server has not found anything matching the URI given.
- [405](http://httpstatus.es/405) - **Method Not Allowed** - Request method not supported by that resource.
- [406](http://httpstatus.es/406) - **Not Acceptable** - Content not acceptable according to the Accept headers.
- [407](http://httpstatus.es/407) - **Proxy Authentication Required** - Client must first authenticate itself with the proxy.
- [408](http://httpstatus.es/408) - **Request Timeout** - Server timed out waiting for the request.
- [409](http://httpstatus.es/409) - **Conflict** - Request could not be processed because of conflict.
- [410](http://httpstatus.es/410) - **Gone** - Resource is no longer available and will not be available again.
- [411](http://httpstatus.es/411) - **Length Required** - Request did not specify the length of its content.
- [412](http://httpstatus.es/412) - **Precondition Failed** - Server does not meet request preconditions.
- [413](http://httpstatus.es/413) - **Request Entity Too Large** - Request is larger than the server is willing or able to process.
- [414](http://httpstatus.es/414) - **Request URI Too Large** - URI provided was too long for the server to process.
- [415](http://httpstatus.es/415) - **Unsupported Media Type** - Server does not support media type.
- [416](http://httpstatus.es/416) - **Requested Rage Not Satisfiable** - Client has asked for unprovidable portion of the file.
- [417](http://httpstatus.es/417) - **Expectation Failed** - Server cannot meet requirements of Expect request-header field.
- [418](http://httpstatus.es/418) - **I'm a teapot** - I'm a teapot.
- [420](http://httpstatus.es/420) - **Enhance Your Calm** - Twitter rate limiting.
- [421](https://tools.ietf.org/html/rfc7540#page-66) - **Misdirected Request** - Server is not able to produce a response.
- [422](http://httpstatus.es/422) - **Unprocessable Entity** - Request unable to be followed due to semantic errors.
- [423](http://httpstatus.es/423) - **Locked** - Resource that is being accessed is locked.
- [424](http://httpstatus.es/424) - **Failed Dependency** - Request failed due to failure of a previous request.
- [426](http://httpstatus.es/426) - **Upgrade Required** - Client should switch to a different protocol.
- [428](http://httpstatus.es/428) - **Precondition Required** - Origin server requires the request to be conditional.
- [429](http://httpstatus.es/429) - **Too Many Requests** - User has sent too many requests in a given amount of time.
- [431](http://httpstatus.es/429) - **Request Header Fields Too Large** - Server is unwilling to process the request.
- [444](http://httpstatus.es/444) - **No Response** - Server returns no information and closes the connection.
- [449](http://httpstatus.es/449) - **Retry With** - Request should be retried after performing action.
- [450](http://httpstatus.es/450) - **Blocked By Windows Parental Controls** - Windows Parental Controls blocking access to webpage.
- [451](http://httpstatus.es/451) - **Wrong Exchange Server** - The server cannot reach the client's mailbox.
- [499](http://httpstatus.es/499) - **Client Closed Request** - Connection closed by client while HTTP server is processing.

### Erros do lado do servidor 5xx
This means that even though the request appeared to be valid something went wrong at the server level and it wasn’t able to return anything.

- [500](http://httpstatus.es/500) - **Internal Error** - The server encountered an unexpected condition which prevented it from fulfilling the request.
- [501](http://httpstatus.es/501) - **Not Implemented** - The server does not support the facility required.
- [502](http://httpstatus.es/502) - **Service temporarily overloaded** - The server cannot process the request due to a high load (whether HTTP servicing or other requests). The implication is that this is a temporary condition which maybe alleviated at other times.
- [503](http://httpstatus.es/503) - **Gateway timeout** - This is equivalent to Internal Error 500, but in the case of a server which is in turn accessing some other service, this indicates that the respose from the other service did not return within a time that the gateway was prepared to wait. As from the point of view of the clientand the HTTP transaction the other service is hidden within the server, this maybe treated identically to Internal error 500, but has more diagnostic value.
- [504](http://httpstatus.es/504) - **Gateway Timeout** - Gateway did not receive response from upstream server.
- [505](http://httpstatus.es/505) - **Http Version Not Supported** - Server does not support the HTTP protocol version.
- [506](http://httpstatus.es/506) - **Variant Also Negotiates** - Content negotiation for the request results in a circular reference.
- [507](http://httpstatus.es/507) - **Insufficient Storage** - Server is unable to store the representation.
- [508](http://httpstatus.es/508) - **Loop Detected** - Server detected an infinite loop while processing the request.
- [509](http://httpstatus.es/509) - **Bandwidth Limit Exceeded** - Bandwidth limit exceeded.
- [510](http://httpstatus.es/510) - **Not Extended** - Further extensions to the request are required.
- [511](http://httpstatus.es/511) - **Network Authentication Required** - Client needs to authenticate to gain network access.
- [598](http://httpstatus.es/598) - **Network Read Timeout Error** - Network read timeout behind the proxy.
- [599](http://httpstatus.es/599) - **Network Connect Timeout Error** - Network connect timeout behind the proxy.


## Contribua

Contribuições são bem vindas! Leia [orientações de contribuições](contributing.md) first.


## Licensa

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)](http://creativecommons.org/publicdomain/zero/1.0/)
