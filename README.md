# carbr <img src="site/logo.svg" align="right" height="120" alt="Logo do carbr" />

Os dados públicos do Cadastro Ambiental Rural (CAR), dos 27 estados, sem baixar a base inteira.

O carbr republica a camada pública de imóveis do Sicar em arquivos GeoParquet, organizados de modo
que cada consulta transfira só o trecho de que precisa. Este repositório é a porta de entrada do
projeto; a apresentação completa está em **<https://castlaboratory.github.io/carbr/>**.

## Como usar

| Para | Onde |
|---|---|
| Consultar no mapa, sem instalar nada | <https://car.castlab.org> |
| Entender os termos e a legislação | <https://car.castlab.org/ajuda.html> |
| Analisar em R | [carbr-r](https://github.com/castlaboratory/carbr-r) · [documentação](https://castlaboratory.github.io/carbr-r/) |
| Analisar em Python | [carbr-py](https://github.com/castlaboratory/carbr-py) · [documentação](https://castlaboratory.github.io/carbr-py/) · `pip install "carbr[geo]"` |
| Perguntar a um assistente de IA | servidor MCP em `https://mcp.castlab.org/mcp` · [carbr-mcp](https://github.com/castlaboratory/carbr-mcp) |
| Ler os arquivos diretamente | `https://car.castlab.org/current/catalog.json` |
| Reproduzir a carga | [carbr-etl](https://github.com/castlaboratory/carbr-etl) |

## O que está publicado

O perímetro declarado e dez atributos de cada um dos 8,6 milhões de imóveis, com atualização
semanal, resumos pré-calculados, indicadores de qualidade (sobreposição entre imóveis e área fora
do município declarado) e um histórico das mudanças de etapa da análise. Não há dado que
identifique proprietários, nem APP, reserva legal ou vegetação nativa, que o serviço público do
Sicar não oferece.

Fonte: Sicar, Serviço Florestal Brasileiro. Esta é uma republicação independente, sem caráter
oficial; em caso de divergência, vale o Sicar.

## Equipe

André Leite, Marcos Wasiliew, Hugo Vasconcelos, Carlos Amorim, Diogo Bezerra, Júlia Nascimento
Barreto e Hortênsia Nunes Braz de Oliveira, colaboradores do CastLab.

## Licença

MIT. O site fica em `site/` e é publicado pelo GitHub Pages a cada alteração.
