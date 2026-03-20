# ME712
## Descrição do projeto 
O objetivo da pesquisa é modelar quantitativamente o Índice de Bioturbação em uma planície de maré, avaliando como fatores abióticos influenciam a atividade biológica no sedimento. Pretende modelar a influência de preditores ambientais (físico-químico da água e do sedimento) sobre o índice de bioturbação, lidando com problemas como multicolinearidade e tamanho amostral. 
Para a consultoria a pesquisadora espera:
- Validar a especificação dos modelos de mensuração (outer model) e estrutural (inner model);
- Assegurar que os índices de ajustes (GoF, vif) atendam os critérios para confirmar a robustez das inferências
- Confirmar se o modelo PLS-PM é o mais recomendado para os dados trabalhados, ou se outros modelos como regressão e GLM são mais interpretáveis.

## Etapas do projeto 
### Análise Exploratória 
Para compreensão inicial do conjunto de dados, foram gerados gráficos e matrizes de correlação, das quais obtivemos as seguintes informações:

**Composição Granulométrica:**
A partir da análise de boxplots, observou-se que o sedimento é predominantemente composto por lama e areia muito fina. Em contraste, as frações de areia grossa e muito grossa apresentam baixa representatividade e pouca variação nas amostras.

**Correlação das variáveis:**
- Associação negativa: Notou-se que as frações de _"areia fina (%)"_ e _areia muito fina (%)"_ estão associadas negativamente a variável _"lama"_. Isso indica que, à medida que o teor de lama aumenta reduz as frações arenonas.
- Associação positiva: observou-se que uma alta correlação positiva entre os pares _"areia muito grossa (%)"_ / _"areia grossa (%)"_ assim como _"areia muito fina (%)"_ /_"areia fina (%)"_.

Esses valores altos sugerem a presença de multicolinearidade, para o modelo pode ser necessário estudar a redução de dimensionalidade, como PCA.


### Implementação e Validação do Modelo Multivariado 
### Hierarquizar os Fatores ambientais
