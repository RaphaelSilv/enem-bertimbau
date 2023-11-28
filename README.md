# ENEM-BERTimbau

O presente repositório contém os experimentos realizados para a conclusão do Trabalho de Curso (TCC) em Sistemas de Informação pela Universidade de Santa Catarina.

## Referencias

```
@inproceedings{raphael-et-al-23,
  author = {Raphael Ramos da Silva},
  title = {Análise da aderência semântica de redações do ENEM aos textos motivadores: uma abordagem baseada no BERTimbau},
  year = {2023},
  publisher = {Universidade Federal de Santa Catarina},
  address = {Online},
  doi = {TODO:},
  url = {TODO:}
}
```

## Descrição

Todos os anos, milhares de estudantes brasileiros se submetem à maior avaliação de ensino do país, o Exame Nacional do Ensino Médio (ENEM). 
O exame avalia não só a qualidade da educação básica nacional, mas também é utilizado para o ingresso em instituições de ensino superior. 
Além de questões de múltipla-escolha abrangendo as grandes áreas do conhecimento, a prova também é composta por uma redação que deve ser redigida obedecendo o estilo dissertativo-argumentativo. A redação é avaliada em cinco competências, sendo o objetivo da segunda, grosso modo, avaliar a compatibilidade semântica do texto produzido com o tema proposto.  

O processo manual de avaliação das redações é dispendioso. O custo  estimado em 2015 para cada correção de redação era de R$15,88. 
Nesse mesmo ano, 6,4 milhões de redações foram corrigidas.

Levando isso em consideração, o presente trabalho propõe o uso de técnicas Aprendizado Profundo e de Processamento de Linguagem Natural para determinar a pontuação de uma dada redação na segunda competência avaliativa. O uso do modelo de linguagem *BERT* será central para nossa investigação, especificamente a variação do modelo pré-treinado para a língua portuguesa do Brasil, o *BERTimbau*. 
Tal proposta não apenas se alinha ao que há de mais recente nas práticas de *PLN* voltadas ao âmbito educacional, como também busca preencher a lacuna de aplicações correlatas especificamente adaptadas para a língua portuguesa.  Para atingir os objetivos, um modelo de regressão e outro de classificação foi criado. Os experimentos utilizaram o modelo *BERTimbau* para extrair *embeddings* contextualizados do textos processados e realizou o fine-tuning dos hiper-parâmetros do *BERT*. Ambos modelos foram treinados por três diferentes taxas de aprendizado, e a técnica de validação cruzada *kfold* foi utilizada para validação dos resultados. O modelo adaptado para a tarefa de classificação apresenta boa capacidade de generalização a novos dados, atingindo a acurácia 90,45 e *F1score* de 0,90, para uma das taxas de aprendizado. Já os resultados do modelo de regressão sugere baixa adaptabilidade para resolver o problema proposto tendo seu *MAE* superior a 120 para treinamento e validação. 
