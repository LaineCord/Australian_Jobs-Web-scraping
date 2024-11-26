# Projeto em construção


### Web Scraping e Análise de padrões

Este projeto tem o intuito de realizar uma análise dos principais trabalhos encontrados na Australia para Algumas cidades. 
Os dados foram coletados no dia 6-11-2024, logo, o padrão a ser encontrado terá relação com  pelo menos os ultimos 30 dias que antecedem a extração.

## 1 Etapa: Realizar a extração dos dados:
A extração dos dados precisa ser realizada de forma que seja possivel retirar o máximo de dados relevantes da página para porterior análise. Nesta etapa foi utilizada a biblioteca Selenium para a extração dos dados do site indeed.au. Por ser uma biblioteca extremamente poderosa para automação WEB ela foi utilizada para facilitar o processo de extração dos dados atualizados que serão utilizados nesse projeto. Por meio dela foram extraidos do indeed:
- Titulos das vagas;
- Localização;
- Descrição da vaga.

  
## 2 Etapa: Tratamento dos dados extraídos: 
Após extraído os dados é necessário trata-los para que seja possivel fazer análises relevantes com as informações encontradas por meio de padrões mais comuns nos dados. No tratamento foram retirados vagas com o campo "Titulo" em branco. 

## 3 Etapa: Clusterização dos dados: 
Os Titulos das vagas não seguem um padrão. Muitas vagas, apesar de necessitarem de habilidades similares são descritas de formas diferentes dependendo da companhia. Visto isso, foi feito um teste sobre qual seria a forma ideial de retirar as palavras-chave das vagas para posterior clusterização.  O teste foi feito retirando palavras-chave do Titulo e da descrição.  Após retiradas as palavras-chave e adicionadas em colunas diferentes, criando novas features, foram feitas clusterização das colunas utilizando o DBSCAN. O DBSCAN é comunmente utilizado para identificar clusters que não possuem um padrão definido.

## 4 Etapa: Análise dos padrões.

 
