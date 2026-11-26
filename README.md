# carbr <img src="site/logo.svg" align="right" height="120" alt="Logo do carbr" />

Os dados públicos do Cadastro Ambiental Rural (CAR), dos 27 estados, prontos para análise.

O carbr republica a camada pública de imóveis do Sicar em arquivos GeoParquet, organizados de modo
que um programa leia só o trecho de que precisa, sem baixar a base inteira. Sobre esses arquivos há
pacotes em R e em Python, indicadores de qualidade por imóvel, uma tipologia dos municípios, um
servidor para assistentes de IA e uma página de consulta. Este repositório é a porta de entrada do
projeto; a apresentação completa está em **<https://castlaboratory.github.io/carbr/>**.

## Como usar

| Para | Onde |
|---|---|
| Analisar em R | [carbr-r](https://github.com/castlaboratory/carbr-r) · [documentação](https://castlaboratory.github.io/carbr-r/) |
| Analisar em Python | [carbr-py](https://github.com/castlaboratory/carbr-py) · [documentação](https://castlaboratory.github.io/carbr-py/) · `pip install "carbr[geo]"` |
| Ver análises prontas, com o código | [a fila da análise](https://castlaboratory.github.io/carbr-r/articles/analise.html) · [inconsistências do cadastro](https://castlaboratory.github.io/carbr-r/articles/inconsistencias.html) |
| Perguntar a um assistente de IA | servidor MCP em `https://mcp.castlab.org/mcp` · [carbr-mcp](https://github.com/castlaboratory/carbr-mcp) |
| Ler os arquivos diretamente | `https://car.castlab.org/current/catalog.json` |
| Consultar no mapa, sem instalar nada | <https://car.castlab.org> · [ajuda](https://car.castlab.org/ajuda.html) |
| Reproduzir a carga | [carbr-etl](https://github.com/castlaboratory/carbr-etl) |

```r
library(carbr)
car_summary("size_class")                              # o país inteiro, em segundos
car_properties("PE", municipality = "Petrolina")       # um município, lendo 4 de 107 blocos
car_check(codigos)                                     # triagem em lote, com terras indígenas e UCs
car_typology()                                         # o perfil de cada município
```

## E o portal oficial?

O Sicar tem o [Consulta Pública](https://consulta.car.gov.br), que busca um imóvel pelo número de
registro e oferece downloads por município. Ele é a fonte oficial e o lugar certo para conferir um
cadastro. O carbr não o substitui: serve a quem precisa dos dados dentro de um programa, sem login
nem captcha, e acrescenta o que o portal não traz, como os totais do país numa linha de código, os
indicadores de sobreposição, o cruzamento com terras indígenas e unidades de conservação, a
tipologia dos municípios e o histórico semanal.

## O que está publicado

O perímetro declarado e dez atributos de cada um dos 8,6 milhões de imóveis, com atualização
semanal, resumos pré-calculados, indicadores de qualidade (sobreposição entre imóveis, área fora do
município declarado, terras indígenas e unidades de conservação), uma tipologia dos municípios e
um histórico das mudanças de etapa da análise. Não há dado que
identifique proprietários, nem APP, reserva legal ou vegetação nativa, que o serviço público do
Sicar não oferece.

Fonte: Sicar, Serviço Florestal Brasileiro. Esta é uma republicação independente, sem caráter
oficial; em caso de divergência, vale o Sicar.

## Equipe

André Leite, Marcos Wasiliew, Hugo Vasconcelos, Carlos Amorim, Diogo Bezerra, Júlia Nascimento
Barreto e Hortênsia Nunes Braz de Oliveira, colaboradores do CastLab.

## Licença

MIT. O site fica em `site/` e é publicado pelo GitHub Pages a cada alteração.
