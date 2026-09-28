# 📚 Miniguia de Estudos: Gestão Financeira para Pequenas Indústrias

Projeto desenvolvido para o desafio da DIO, usando o **NotebookLM** como ferramenta de aprendizagem ativa.

---

## 🎯 Contexto e Objetivos

Trabalho como gestor financeiro em uma pequena indústria e escolhi estudar os fundamentos da gestão financeira aplicados a esse tipo de empresa: **fluxo de caixa, margem de contribuição e ponto de equilíbrio**.

**Objetivos de estudo:**
- Entender a diferença entre fluxo de caixa realizado e projetado
- Aprender a calcular e interpretar a margem de contribuição
- Saber calcular o ponto de equilíbrio de uma empresa com mais de uma fonte de receita

---

## 📂 Curadoria de Fontes

Fontes abertas que selecionei e carreguei no NotebookLM:

1. [E-book Fluxo de Caixa – SEBRAE-SP (2016)](https://bibliotecas.sebrae.com.br/chronus/ARQUIVOS_CHRONUS/bds/bds.nsf/a54c29c120d08789e9369c2da15aa9e1/$File/9880.pdf)
2. [Margem de Contribuição: quanto sobra para sua empresa? – SEBRAE](https://bibliotecas.sebrae.com.br/chronus/ARQUIVOS_CHRONUS/bds/bds.nsf/E809A7FF3D9553E90325714700620C06/$File/NT00031FEA.pdf)
3. [Análise da margem de contribuição e ponto de equilíbrio e sua importância para a tomada de decisões – TCC UNIFACVEST (2019)](https://www.unifacvest.edu.br/assets/uploads/files/arquivos/10dc1-trabalho-de-conclusao-de-curso---analise-da-margem-de-contribuicao-e-ponto-de-equilibrio,-e-sua-importancia-para-a-tomada-de-decisoes.pdf)
4. [O cálculo do ponto de equilíbrio e margem de contribuição como ferramenta de gestão – ABEPRO/ENEGEP 2017](https://abepro.org.br/biblioteca/TN_STO_240_391_32939.pdf)

**Critério de escolha:** priorizei fontes gratuitas e confiáveis, combinando material didático do SEBRAE (linguagem acessível, voltada a pequenos negócios) com trabalhos acadêmicos que aplicam os conceitos em casos reais. Testei cada link antes de carregar no NotebookLM.
---

## 🧠 Engenharia de Prompts

### Pergunta 1: O que é fluxo de caixa?

**Prompt inicial:**
> O que é fluxo de caixa?

**Resultado:** resposta correta e bem organizada (entradas, saídas, saldo e benefícios do controle diário), mas genérica: serviria para qualquer tipo de empresa e não deixava claro de qual fonte vinha cada informação.

**Prompt refinado:**
> Com base apenas nas fontes, explique fluxo de caixa para um gestor de pequena indústria, diferenciando o controle do que já aconteceu da projeção de caixa. Indique qual fonte sustenta cada ponto.

**Resultado:** resposta muito mais estruturada, separando o controle do realizado (movimento de caixa) da projeção de caixa, com uma tabela comparativa ao final. Porém, ao conferir, encontrei três problemas:
- atribuiu informações ao "TCC da Uniplac", quando a fonte é da UNIFACVEST (erro de citação);
- adaptou exemplos ao contexto industrial (matéria-prima, sazonalidade fabril) que não estão nas fontes, cujos casos são de restaurante e clínica;
- misturou conceitos de ponto de equilíbrio na explicação de fluxo de caixa.

**Conclusão:** pedir contexto e fontes melhorou muito a organização, mas aumentou o risco de a IA "preencher lacunas" para atender ao pedido. Citar fontes não garante que a citação esteja correta.

### Pergunta 2: O que é margem de contribuição?

**Prompt inicial:**
> O que é margem de contribuição?

**Resultado:** explicação completa e fiel à cartilha do SEBRAE: fórmula (Margem de Contribuição = Vendas − (Custos Variáveis + Despesas Variáveis)), diferença entre margem unitária, total e percentual, e o alerta sobre o erro de confundir margem com o percentual aplicado sobre o custo (markup). Não indicou claramente as fontes.

**Prompt refinado:**
> Compare como as fontes definem margem de contribuição. Mostre onde concordam, onde divergem e dê um exemplo numérico simples.

**Resultado:** organizou a resposta por fonte e citou os nomes corretamente. Destaques:
- reconheceu que o e-book de fluxo de caixa não trata do tema, em vez de forçar uma citação;
- mostrou o que cada fonte acrescenta: o alerta sobre markup (SEBRAE), os três tipos de ponto de equilíbrio (ABEPRO) e a diferença entre margem unitária e total (UNIFACVEST).

Pontos de atenção:
- as fontes não divergem de fato, apenas têm ênfases diferentes; a IA tentou atender ao pedido de "mostrar divergências" mesmo sem haver;
- o exemplo numérico (preço R$ 100, custo R$ 40) foi inventado, embora as fontes tenham exemplos próprios.

**Conclusão:** renomear as fontes no NotebookLM com nomes curtos parece ter ajudado a IA a citá-las corretamente. E a forma de pedir importa: pedir "divergências" induz a IA a encontrá-las, e pedir "um exemplo" sem dizer "das fontes" abre espaço para números inventados.

**Variação extra (teste de correção):**
> Refaça o exemplo numérico usando apenas os números que aparecem nas fontes, indicando de qual fonte veio cada valor.

**Resultado:** a IA trouxe três exemplos reais, um de cada fonte, com as contas corretas:
- MC SEBRAE: preço R$ 22,50, custo R$ 15,00 e despesas variáveis de 10,5% → margem de R$ 5,14 (22,8% do preço);
- UNIFACVEST: sabão em pó a R$ 11,00 com custo de R$ 8,35 → margem unitária de R$ 2,65 e total de R$ 159,00 (60 unidades);
- ABEPRO: produto industrial a R$ 124,20 com custo variável de R$ 59,60 → margem de R$ 64,60 (52,01% do preço).

**Conclusão:** exigir explicitamente "apenas números das fontes" eliminou os valores inventados.

### Pergunta 3: Como calcular o ponto de equilíbrio?

**Prompt inicial:**
> Como calcular o ponto de equilíbrio?

**Resultado:** explicação completa das fórmulas em quantidade (Custos Fixos ÷ Margem Unitária) e em valor (Custos Fixos ÷ Margem Percentual), incluindo os três tipos de ponto de equilíbrio (contábil, financeiro e econômico) do artigo da ABEPRO. Curiosidade: ao final, ofereceu aplicar os cálculos "à sua fábrica", deduzindo esse contexto de perguntas anteriores.

**Prompt refinado** (já incorporando o aprendizado da Pergunta 2 de exigir números das fontes):
> Usando apenas as fontes, monte um passo a passo para calcular o ponto de equilíbrio em quantidade e em valor, com um exemplo que use somente números das fontes. Explique também as limitações do cálculo quando a empresa vende produtos diferentes.

**Resultado:** usou corretamente os dados do TCC da UNIFACVEST (sabão em pó) e explicou bem que calcular o ponto de equilíbrio de um único produto gera uma meta irreal (928 unidades contra 60 vendidas). Porém, ao conferir as contas, encontrei dois problemas:
- **Arredondamento:** o ponto de equilíbrio em valor (R$ 10.248,75) não bate com quantidade × preço (928,18 × R$ 11,00 = R$ 10.209,98), porque a margem foi arredondada de 24,09% para 24%. O erro já estava no TCC e a IA o repetiu.
- **Contradição:** a IA explicou que o ponto de equilíbrio de vários produtos depende do mix de vendas, mas citou como exemplo "ponderado" o cálculo do TCC, que na verdade soma os preços dos produtos sem considerar as quantidades vendidas. Refazendo a conta ponderada pelas vendas reais, a margem média é de 24,26% e o ponto de equilíbrio fica em cerca de R$ 10.139.

**Conclusão:** a IA reproduz os erros das fontes sem questioná-los e pode até apresentá-los como exemplos corretos. Conferir as contas manualmente foi indispensável.

---

## 🩹 Cicatrizes (Dificuldades e Aprendizados)

### 1. Links de fontes que pararam de funcionar
- **Problema:** os primeiros links do portal SEBRAE que selecionei abriam uma página genérica de "Conteúdos", e não o material específico.
- **Causa:** o SEBRAE reorganizou o site e os endereços antigos passaram a redirecionar para a página inicial.
- **Solução:** busquei os materiais equivalentes na Biblioteca Digital do SEBRAE e testei cada link no navegador antes de carregar no NotebookLM.
- **Aprendizado:** curadoria não termina ao encontrar a fonte; é preciso verificar se ela está acessível e estável.

### 2. Erro enganoso ao adicionar uma fonte
- **Problema:** ao colar o link do TCC da UNIFACVEST, o NotebookLM respondeu que "o URL precisa começar com http:// ou https://", mesmo o link já começando com https.
- **Causa:** o endereço continha vírgulas, que o NotebookLM não aceita bem em links.
- **Solução:** baixei o PDF e enviei como arquivo.
- **Aprendizado:** a mensagem de erro nem sempre aponta a causa real; vale investigar antes de descartar uma boa fonte.

### 3. Resumo automático que ignorou parte das fontes
- **Problema:** com 4 fontes carregadas, o resumo inicial do caderno descreveu apenas o artigo da ABEPRO (indústria metalmecânica), ignorando as cartilhas do SEBRAE e o TCC. As perguntas sugeridas pela ferramenta também focaram só nesse artigo.
- **Causa:** o NotebookLM parece dar mais peso a uma fonte na visão geral automática.
- **Solução:** não usei o resumo automático como base; fiz perguntas direcionadas e conferi nas respostas quais fontes estavam sendo citadas.
- **Aprendizado:** a primeira impressão gerada pela IA pode ser parcial; é preciso verificar se ela representa todo o material.

### 4. A IA citou uma fonte com o nome errado
- **Problema:** no prompt refinado sobre fluxo de caixa, o NotebookLM atribuiu informações a um "TCC da Uniplac", mas a fonte carregada é um TCC da UNIFACVEST.
- **Causa:** provável confusão da IA entre duas instituições da mesma cidade (Lages/SC). É uma alucinação: a resposta parece confiável justamente por citar fontes.
- **Solução:** conferi as citações clicando nos números da resposta dentro do NotebookLM, e não no texto copiado (ao copiar, os números de citação se perdem).
- **Aprendizado:** pedir que a IA cite as fontes melhora a rastreabilidade, mas não substitui a conferência humana.

  ### 5. Exemplo numérico inventado e fórmulas ilegíveis
- **Problema:** ao pedir um exemplo numérico, o NotebookLM criou valores fictícios, embora as fontes tivessem exemplos reais. Além disso, ao copiar as respostas, as fórmulas vinham com códigos de formatação (como \text{} e \[) que ficam ilegíveis no GitHub.
- **Causa:** o prompt pedia "um exemplo simples", sem exigir que viesse das fontes. Já as fórmulas usam uma linguagem de formatação matemática (LaTeX) que o NotebookLM exibe bem, mas que não aparece corretamente no README.
- **Solução:** reformulei o pedido exigindo "apenas números que aparecem nas fontes". Para o README, reescrevi as fórmulas em texto simples.
- **Aprendizado:** a IA faz exatamente o que o prompt permite; se a instrução deixa brecha, ela preenche com conteúdo próprio.

  ### 6. A IA repetiu e validou erros de cálculo da fonte
- **Problema:** no cálculo do ponto de equilíbrio, o NotebookLM reproduziu um arredondamento do TCC que distorcia o resultado em cerca de R$ 39, e apresentou como "margem ponderada" um cálculo que não considera as quantidades vendidas de cada produto.
- **Causa:** o NotebookLM trata o conteúdo das fontes como verdadeiro. Ele resume e reorganiza bem, mas não audita os cálculos.
- **Solução:** fiz a "prova real" (quantidade × preço deve igual ao valor) e refiz o cálculo ponderado pelas vendas de cada produto.
- **Aprendizado:** fonte acadêmica não é garantia de acerto, e a IA não substitui a conferência dos números. Em finanças, uma diferença de arredondamento na margem pode mudar a meta de faturamento.

---

## ✅ Miniguia de Estudo (Entrega Final)

### Resumos

**Fluxo de caixa:** [COMPLETAR]

**Margem de contribuição:** [COMPLETAR]

**Ponto de equilíbrio:** [COMPLETAR]

### Glossário

| Termo | Significado |
|---|---|
| [COMPLETAR] | [COMPLETAR] |
| [COMPLETAR] | [COMPLETAR] |

### Prompts reutilizáveis para revisão

1. [COMPLETAR]
2. [COMPLETAR]
3. [COMPLETAR]

---

## 🛠️ Ferramentas utilizadas

- NotebookLM (Google)
- GitHub
- Claude (apoio na organização do material)
