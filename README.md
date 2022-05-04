# OBSAT-MCTI

## Servidor de testes lançado



O servidor de testes da OBSAT foi lançado, agora você pode fazer requisições usando seu satélite!

**Informações gerais:**

- Link para fazer a requisição pelo BIPES: https://obsat.org.br/teste_post/envio_bipes.php 
- Link para refazer a requisição de outra maneira (Curl): https://obsat.org.br/teste_post/envio.php 
- Link para visualizar as requisições: https://obsat.org.br/teste_post/index.php
- Exemplo de Implementação: https://bipes.net.br/ide/?lang=pt-br#w2v6ep
- Obs: A implementação é apenas um exemplo, o seu payload não precisa necessariamente ter os mesmos campos que o do exemplo.


## Deu erro, e agora?


Primeiro, preste atenção no campo "Status". O Status geralmente irá dizer o erro para você. 	


### Lista de Erros:


**Tamanho limite do Payload excedido:**<br>
Causa: O valor do payload está extremamente grande (Maior do que o banco pode suportar).<br>
Solução: Diminua o número de informações do payload, e verifique se você está enviando corretamente.<br>

**A requisicao recebida não é um JSON**<br>
Causa: A sua requisição possui um JSON mal formatado<br>
Solução: Falta de aspas e chaves são os motivos mais comuns, preste atenção em como seu JSON está formatado, mais abaixo, um link será disponibilizado de uma plataforma que verifica se um JSON é válido.<br>

**O JSON recebido nao segue a formatacao correta**<br>
Causa: Seu JSON não possui todos o(s) campo(s) que deveria ter.<br>
Solução: Verifique se eles estão escritos de maneira IDÊNTICA aos campos corretos. Uma lista com todos os campos estará logo abaixo.<br>


**Truncado**<br>
Causa: O campo payload possui mais de 90 bytes e menos que 500 bytes, logo, ele foi truncado com o último campo válido<br>
Solução: Verifique o tamanho do seu payload, muito possivelmente ele está enviando dados extremamente grandes<br>


**N/A**<br>
Causa: Algum erro aconteceu, e os campos associados a sua requisição não foram enviados.<br>
Solução: Verifique o status, e por que isso ocorreu<br>


**Nada aconteceu**<br>
Causa: Isso pode ter mais de uma causa, mas geralmente, ou você enviou um JSON muito grande, que está acima do limite máximo do banco de dados, ou você não programou o BIPES corretamente<br>
Solução: Preste atenção no tamanho do seu JSON, e confira o link de exemplo, muito provavelmente, você não deve ter feito o procedimento de envio corretamente.<br>


### **Informações adicionais**

Site para verificar se um JSON é válido 
https://jsonformatter.org/json-viewer 

Link para o edital (Cheque o apêndince 1, no final do arquivo)
https://github.com/OBSAT-MCTI/OBSAT-MCTI/blob/main/editais/1a_OBSAT%20MCTI_Fases_2_11_04_2022.pdf

Todos os campos necessários:
```json
equipe
bateria
temperatura
pressao
giroscopio
acelerometro
payload
```

## F.A.Q

**O site não apresenta todas as colunas**<br>
Isso acontece porque alguma requisição deve ter sido extremamente larga, tire o zoom da página (CRTL -).

**Meu payload não está por inteiro**<br>
Isso acontece porque ele superou o limite máximo de 90 bytes, diminua o tamanho.

**Encontrei uma requisição maliciosa, o que devo fazer?**<br>
Contate algum administrador que ele irá remove-la. **Requisições maliciosas serão rastreadas, e os responsáveis serão punidos, podendo ser desclassificados da OBSAT, e banidos das próximas edições**

**Minhas requisições serão armazenadas para sempre?**<br>
Não, elas serão removidas automaticamente após 24 horas.















