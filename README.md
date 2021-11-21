# Aprendendo as funcionalidade dos Insomnia
Aqui temos todas funcionalidades que o `Insomnia` possui como variáveis e funções

## Ambiente de trabalho
Para criar uma API falsa usamos a dependência `JSON Server` onde para executar ele podemos usar o seguinte atalho configurado no `package.json`
```bash
yarn server
```
```json
"server": "json-server db.json -w -d 750 -p 3333"
// -w faz o server reiniciar ao detectar alterações
// -d cria um atraso nas respostas das requisições
// -p define a porta de execução
```

## Métodos
Ele possui todos os métodos de requisição `HTML`, eles podem ser agrupado pastas e possui diversas configurações adicionais como `auth`, `query`, `header` e `docs`

## Variáveis
Podemos utilizar as variáveis para armazenar valores padrão para assim ele ser trocado em todos locais com somente uma alteração, ela pode ser criada em três grupos como global, sub e pasta

## Funções de geração de valores
Existe algumas funções que cria valores como um `ID` do tipo `UUID`; valores aleatório como o `MD5`, `SHA1`, `SHA256` e `SHA512`; e recuperação da data e hora do momento que a requisição foi realizada com o `Timestamp`, todas estas funções pode ser editadas

## Função response
Com ela conseguimos coletar informações de forma dinâmica como um `ID` ou um `token`, ela é vinculada a um outro método que será executado conforme decidimos, existe 4 maneiras, e para selecionar o valor desejado devemos usar o simbolo `$` e depois informar o nome do campo
  * Nunca - Nunca reenvie o pedido
  * Sem histórico - Reenviar quando não houver respostas
  * Quando expirado - Reenviar quando a resposta existente expirar
  * Sempre - Reenviar solicitação quando necessário

## Função request
Podemos utilizar para enviar algumas informações na requisição como um `cookie`

## Exporta estrutura do projeto
Podemos exportar os métodos criado para um projeto para assim conseguimos configurar ele sem a necessidade de ler a documentação do projeto, para isso basta selecionar a opção Import/Export no titulo do projeto e realizar oque deseja

Para realizar a importação com facilidade podemos criar um [Insomnia Run Button](https://insomnia.rest/create-run-button) onde com ele basta clicar no botão para importa as informações
  1. Exportamos as configurações
  2. Agora enviamos para um repositório do `Github`
  3. Depois abrimos ele e copiamos o link gerado pelo `raw`
  4. Agora acessamos este [site](https://insomnia.rest/create-run-button) para criar
  5. Informamos um nome da aplicação e o link copiado
  6. Por último usamos o código `markdown snippet` para criar o botão no `Github`
