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

(repita a mesma estrutura acima)

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

### 4. [COMPLETAR com o que acontecer nos testes de prompts]
- **Problema:**
- **Causa:**
- **Solução:**
- **Aprendizado:**

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
