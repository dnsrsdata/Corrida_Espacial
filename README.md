# Corrida espacial (1957 - 2020)
Durante essa semana, entre os estudos e afazeres domésticos, resolvi tirar um tempinho para relaxar e assistir Interestelar, que é um daqueles filmes que são excelentes, mas que são pouco comentados.

![](https://c.tenor.com/CoLT0XrDN_cAAAAC/interstellar-gargantua.gif)

Coincidentemente, um dos projetos de um curso que adquiri era para explorar um conjunto de dados sobre a corrida espacial, que continha elementos desde o inicio da mesma, em 1957. E aqui compartilharei o que eu consegui extrair desse conjunto.

## Apresentação dos dados 
Todos os dados incluídos no Dataset foram retirados do site Next Spaceflight, que contem dados como status da missão (sucesso/falha), o custo da missão, o número de lançamentos por país, etc. O conjunto que usei não contém todo o conteúdo contido no site, apenas parte dele. A coleta não foi realizada por mim, aproveitei os dados de um curso que realizei. Aqui está uma visão geral:

![](https://i.postimg.cc/WbyKgRZ1/vis-ogeral.png)

## Resultados
Para o nosso primeiro gráfico, precisei converter a coluna price, que estava em formato de str em um float, além também de excluir as colunas "_c0" e "Unnamed: 0". Após esse pequeno tratamento, plotei um gráfico sobre o total já investido por cada organização usando o Seaborn, tentando deixar os gráficos o mais autoexplicativo possível.

![](https://i.postimg.cc/hPG6TcPH/Captura-de-tela-de-2022-09-05-07-44-18.png)

A primeira vista, o gráfico já nos mostra que a NASA foi a organização que mais investiu no lançamento de foguetes, algo que pode se dar até pela data de sua fundação, em 1958.
Ainda em relação a data de fundação, podemos ver algo interessante:

![](https://i.postimg.cc/Rqrgk5KT/Captura-de-tela-de-2022-09-05-07-50-52.png)

A SpaceX e a ULA, empresas que surgiram respectivamente em 2002 e 2006, em questão de investimento, estão a frente de várias outras que são do século passado, com algumas surgindo ainda durante o período da Guerra Fria.

![](https://i.postimg.cc/HkNrdYVH/Captura-de-tela-de-2022-09-05-07-47-33.png)

Além disso, as agências russas e soviéticas, as principais rivais dos EUA durante o período da Guerra Fria sequer aparecem entre as 10 que mais investiram. Mas diante desses números, vem uma questão: **alto investimento impacta no número de lançamentos?**

Para responder isso, criei um dataset a partir do original, agrupando as organização com o número total de lançamentos de cada uma. Colocando em outro gráfico de barras, podemos ver:

![](https://i.postimg.cc/G2fRstnh/Captura-de-tela-de-2022-09-05-07-54-01.png)

E ai veio algo que eu não esperava, por ser uma empresa ativa desde 1958, e por ser a principal agência americana durante a Corrida Espacial durante a Guerra Fria, acreditava que a NASA estaria bem melhor colocada, mas a agência soviética RVSN USSR ficou no topo, de forma disparada, então da a entender que **alto investimento não impacta diretamente no número de foguetes lançados por organização**. Mas então vem outra questão, **o baixo investimento combinado com um alto número de lançamento de foguetes pode resultar em uma % maior de falha ou sucesso nos lançamentos?**

Para responder essa outra questão eu criei outro dataset, contendo cada organização com o respectivo número de falhas e sucessos, e ao concatenar com o conjunto que continha o número total de lançamentos de cada organização, pude gerar duas colunas com o percentual de falha e sucesso de cada uma. Colocando em um gráfico de barras mais uma vez, obtemos as seguintes visualizações:

![](https://i.postimg.cc/kGjT560f/Captura-de-tela-de-2022-09-05-07-56-46.png)

![](https://i.postimg.cc/9MsGgPj3/Captura-de-tela-de-2022-09-05-07-57-54.png)

Então, podemos ver que no caso observado, **investimento x quantidade de foguetes lançados não interfere na taxa de sucesso ou de fracasso dos lançamentos**.

Outra visualização que obtive com os dados foi um gráfico de linhas mostrando a quantidade de lançamentos em cada ano desde o início da corrida espacial até o ano de 2020. Vejamos a seguir:

![](https://i.postimg.cc/50XrFmmD/Captura-de-tela-de-2022-09-05-07-59-42.png)

A primeira vista, podemos ver que o gráfico possui dois picos, um por volta de 1970 e outro próximo a 2018. Pesquisando um pouco sobre essas datas, podemos perceber algumas coisas.

![](https://i.postimg.cc/PJm2mVvV/Captura-de-tela-de-2022-09-05-08-00-35.png)

O primeiro pico pode ser explicado facilmente pelo contexto histórico da época, já que a corrida para levar o primeiro homem a lua estava acontecendo, se dando em 1969, próximo de onde ocorreu nosso primeiro pico. Já o segundo ápice pode ser explicado pelo aumento de lançamentos comerciais, levando satélites até a órbita, assim como a corrida entre algumas empresas para realizarem voos de turismo espacial, que ficaram mais conhecidos em 2021 com o voo suborbital levando Jeff Bezos. Embora por motivos diferentes, os picos são comparáveis, nos mostrando que **o número de lançamentos realizados durante a corrida espacial na guerra fria, onde duas potências buscavam mostrar superioridade uma a outra se compara com o ápice que temos nos tempos atuais, onde o empreendimento de alguns nos levam as alturas, literalmente.**

E com isso chegamos ao final, acredito que consegui por em prática parte dos conhecimentos que possuo, espero que tenham gostado do conteúdo. Qualquer dica, assim como feedback são bem vindos, caso queiram entrar em contato, aqui está o meu [Linkedin](https://www.linkedin.com/in/daniel-soares-ti/).
