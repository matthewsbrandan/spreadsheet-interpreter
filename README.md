# DESAFIO INTERPRETADOR DE PLANILHAS

## Objetivo
  O objetivo é criar uma página utilizando ReactJS(iniciado com Vite) e TailwindCSS(diferêncial), onde o usuário carregue uma planilha qualquer, defina regras de validação e formatação (pode ser em JSON), e usando essas regras definidas no frontend, o backend(API Rest) deve ser capaz de interpretar o excel retornando os dados tratados no formato JSON.

  Com o retorno das informações, você deve renderizar uma tabela, que seja capaz de realizar filtragem por coluna.

## Tecnologias a serem utilizadas
  - ReactJS
  - TailwindCSS (opcional)
  - Axios
  - Express
  - NodeJS
  - Typescript

## Exemplo de campos do formulário de upload

  - input file

  - textarea para parametrização em json das colunas relevantes

    Este campo deve ser capaz de descrever o nome da coluna a ser localizada no excel, se ela é obrigatória ou não, e qual o nome que ela receberá no objeto final(pode ser diferente do nome da coluna de excel)

  - textarea para parametrização em json de formatações adicionais

    Quando lêmos um excel algumas informações podem vir mal formatadas, exemplo: data, moeda, telefone, etc. A ideia é que você seja capaz de descrever quais campos vão receber um tratamento especifico de formatação.

    Caso queira incluir essa parametrização no input anterior pode incluir.

## Tratamento de Erros

  Nas parametrizações definiremos quais campos são obrigatórios, e caso um campo obrigatório não sejam preenchido ele deve disparar um erro, que deve ser bem tratado no frontend, sendo mostrado em português para o usuário.

  Você pode escolher um dos 3 tipos de tratativas:

  **1- Simples:** Quando um erro for encontrado interrompe a execução e retorna a mensagem para o usuário.

  **2- Informativo:** Quando encontrar um erro você irá ignorar a linha do excel com problema e continuará o código. No final você deverá gerar uma lista dos erros encontrados e mostrar de forma adequada ao usuário.

  *Diferencial:* caso pelo menos uma linha for bem sucedida, você deverá retornar status de sucesso, renderizar a tabela com os dados que deu certo, e mostrar a lista de erros caso exista. Somente se todas falharem você retornara status de erro, e mostra da mesma forma a lista, apenas não renderizando a tabela de sucesso(que obviamente não existe)

  **3- Avançado:** Igual a tratativa 2, porém gerando um modal com as linhas que deram erro, permitindo que o usuário edite em tela, e ao finalizar a correção, adicionar os dados tratados a tabela de sucesso no frontend.

  Obs. não é necessário retornar ao backend depois disso, todo o tratamento pode ser realizado no front.