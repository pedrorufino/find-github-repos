#  [!TIP] Os tres passos para o AJAX (ASYNC JS AND XML)

<p>
Ele permite requisições assíncronas na mesma url,
a resposta pode ser em diversos tipos de arquivo
</p>



1. Instanciar o objeto ajax, não é necessário acessar o objeto window, pois já estamos em escopo global
**const ajax = new xmlhttprquest()**

1. Abriremos a requisição, passando como argumentos um protocolo http válido (get, post, delete, etc.), a url que queremos solicitar os dados, e se a operação será assíncrona, um valor boleano para decidir se o método send() não retornará nada até qua a requisição seja recebida.

**ajax.open(<\protocolo>,<\url>, <\async>)**

1. A resposta deve vir junto ao código 200 do http

lembrando que:
- 1xx => Informações
- 2xx => Confirmações e sucessos
- 3xx => Redirecionamentos
- 4xx => Erros do cliente
- 5xx => Erros do servidor

[https://http.cat/](todos os códigos http) 

**ajax.send(<\data>)**

Para vermos as mudanças, adicionaremos o evento, ***readystatechange***, que verifica se uma requisição mudou de estado, e os estados são:

- 0: nao enviado, quando o open nao é chamado
- 1: conexao aberta, o open ja foi chamado
- 2: header contedo pronto e recebido
- 3: conteúdo sendo carregado para sua manipulação
- 4: pronto



