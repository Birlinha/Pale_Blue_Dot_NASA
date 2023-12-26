# NASA | DrivenData.org
## O Ponto Azul Pálido - *Pale Blue Dot*

Este desafio proposto pela driven data, em conjunto com a NASA e NASA Tournament Labs - *NTL*
É um desafio cujo objetivo visa atingir os Objetivos de Desenvolvimento Sustentável - *ODS*
Os objetivos em palta são: Fome Zero, Limpeza e Sanitariedade das Águas e Mudanças Climáticas

Como analista de dados, cientista ou cidadão cientista, você deve criar visuais intrigantes que ajudem os legisladores - *policymakers* a tomarem decisões. 

Atenção: Necessário utilizar dados públicos e sobre os EUA em seu estudo. Confira os datasets disponíveis na íntegra em: [Pale Blue Dot](https://www.drivendata.org/competitions/256/pale-blue-dot/)

## Como fazer um projeto igual (*mas diferente*)

Para construir seu projeto, você deve se atentar aos 3 seguintes pontos (não necessariamente em ordem, e pode ser cíclico):

- Brainstorming
  - Compreensão do problema
  - Construção de possíveis soluções
  - Ligação entre dados disponíveis e problemas a solucionar
- Dados
  - Baixar dados
  - Compreender os dados
  - Transformar os dados
- Visualização / Resolução do Problema
  - Construção dos gráficos
  - Validação dos dados e do gráfico construído
  - Questão: Este gráfico resolve o problema proposto na fase de Brainstorming/Dados? Senão, voltar para onde achar necessário

Nesse caso, vamos pular a fase de brainstorming para treinarmos em um caso específico:
  A precipitação sobre gelo no Alaska

Ao perguntar o ChatGPT quais seriam os casos de uso para um dataset cujo objetivo é compreender o índice de precipitação sobre gelo no Alaska - este respondeu:

> Esse conjunto de dados sobre a frequência e distribuição de chuva sobre a neve durante as estações frias no Alasca entre 2003 e 2016 tem várias aplicações interessantes. Aqui estão alguns casos de uso potenciais:
> 
> Previsão de Risco de Inundação: Utilize os padrões de chuva sobre a neve para prever o risco de inundações durante o derretimento da neve na primavera. Isso pode ser crucial para comunidades e autoridades locais que desejam se preparar para eventos de inundação.
> 
> Impacto na Vida Selvagem: Analise como a chuva sobre a neve afeta a ecologia e o comportamento da vida selvagem no Alasca. Isso pode ajudar os biólogos e conservacionistas a entender melhor como as mudanças climáticas estão influenciando as populações animais na região.
> 
> Agricultura e Recursos Hídricos: Estude como a chuva sobre a neve afeta os níveis de água disponíveis para a agricultura e outras atividades humanas. Isso pode ser crucial para o planejamento de recursos hídricos e a gestão agrícola na região.
> 
> Modelagem de Mudanças Climáticas: Use esses dados para validar e melhorar modelos climáticos que tentam prever mudanças futuras no padrão de chuva sobre a neve. Isso pode ajudar a entender melhor as mudanças climáticas globais e seus impactos regionais.
> 
> Planejamento de Infraestrutura: Compreenda como a chuva sobre a neve afeta a infraestrutura, como estradas, edifícios e redes de energia, para planejar melhor a construção e manutenção em regiões afetadas.
> 
> A razão pela qual esses casos de uso são relevantes é que a chuva sobre a neve pode ter efeitos significativos em vários aspectos da vida e das operações humanas no Alasca. Compreender esses padrões pode ser fundamental para a adaptação às mudanças climáticas e para a mitigação de riscos associados.

Portanto, vamos utilizar o brainstorming realizado pelo nosso companheiro e estudar pelo menos um desses tópicos.

Na fase de dados, precisamos baixar os dados relevantes para nossa análise

Nesse caso, clicando aqui podemos ver os [dados sobre a precipitação no alaska de 2003-2016](https://search.earthdata.nasa.gov/search/granules?portal=idn&p=C2162145449-ORNL_CLOUD&pg%5B0%5D%5Bv%5D=f&pg%5B0%5D%5Bgsk%5D=-start_date&fi=MODIS&as%5Bscience_keywords%5D%5B0%5D=Atmosphere%3APrecipitation&tl=1703557365.73%213%21%21&fst0=Atmosphere&fsm0=Precipitation)

Vale lembrar que é necessário cadastrar-se no sistema desse site antes de ter disponibilidade para ver as informações e baixá-las.
Assim que tiver sua conta cadastrada, realizar o download de um arquivo é tão simples quanto encontrá-lo e clicar em um botão "download", ou "download all" -> e você receberá uma lista de URL's para clicar e baixar, um por vez

Considerando que você baixou o arquivo, então o último passo necessário seria abrir o arquivo ["ALASKA_rain_on_snow.ipynb"](https://github.com/Birlinha/Pale_Blue_Dot_NASA/blob/main/ALASKA_rain_on_snow.ipynb) e clicar no botão no topo "Open in Colab"

Dentro do Notebook, que é o nome dado a esse interpretador de código, você precisará abrir a aba logo a esquerda, onde tem o ícone de uma pastinha

Dentro dessa pastinha clique em upload e suba o arquivo de imagem .tif baixado do dataset de precipitação do alaska

Depois disso é só copiar o nome do arquivo e entregá-lo ao código, alterando o nome ABoVE.Rain-On-Snow.2003_Water_Year_Ah000-001v000-001.001.10212018 (1).tif pelo nome do seu arquivo

Ao executar todo o notebook, o mesmo pedirá sua permissão para acessar o google drive e armazenar o arquivo lá, dentro de uma pasta chamada rain_on_snow_NASA. Se a pasta não existir, o arquivo não será movido e não será possível realizar o print da imagem

Qualquer dificuldade, crie uma ISSUE nesse repositório, para nos comunicarmos

## Exemplos

Alguns dos projetos utilizados como exemplo no artigo principal do site [Pale Blue Dot](https://www.drivendata.org/competitions/256/pale-blue-dot/) são:

- Monitorizar as emissões de gases com efeito de estufa: Utilize os dados do [AIRS](https://airs.jpl.nasa.gov/) para criar um gráfico linear das emissões de um país específico ao longo do tempo e ajude os decisores políticos a monitorizar o progresso no ODS 13 (ação climática).
  - Para um exemplo mais avançado, consulte o [mapa global de emissões de metano](https://www.earthdata.nasa.gov/learn/articles/methane-fossil-fuel-exploitation) provenientes da exploração de petróleo, carvão e gás criado para o Sistema de Monitoramento de Carbono da NASA.

- Aumentar o rendimento das colheitas para agricultores de subsistência: Combine dados climáticos [HRRR](https://rapidrefresh.noaa.gov/hrrr/#:~:text=The%20HRRR%20is%20a%20NOAA,grids%20with%203km%20radar%20assimilation) com dados de humidade do solo [SMAP](https://www.earthdata.nasa.gov/learn/find-data/near-real-time/smap) para criar parcelas de condições de cultivo mensais para uma região agrícola e ajudar os agricultores a decidir o que e quando plantar.
  - Leia como [Catherine Nakalembe, com a missão Harvest da NASA, está a apoiar agricultores](https://www.devex.com/news/how-a-nasa-backed-scientist-uses-satellites-to-help-african-farmers-105010) em toda a África Oriental e Austral.
  - Outros projetos do mundo real estudaram a [agricultura de subsistência no Butão (*Buhtan*)](https://storymaps.arcgis.com/stories/e36505aa74ea474d9de8db3271ece80a) e o [arroz no oeste dos Estados Unidos](https://earthobservatory.nasa.gov/images/150412/a-rough-year-for-rice-in-california).

- Visualize a proliferação de algas nocivas em fontes de água potável: Utilize imagens de satélite Landsat para mapear a proliferação de algas perto de uma grande cidade e ajude os gestores de saúde pública a garantir o acesso a água potável.
  - Esse foi o objetivo da competição [Tick Tick Bloom da DrivenData](https://www.drivendata.org/competitions/143/tick-tick-bloom/)!
  - Aprenda sobre outro exemplo do mundo real no [Chile](https://earthobservatory.nasa.gov/images/151363/algae-in-the-andes).
