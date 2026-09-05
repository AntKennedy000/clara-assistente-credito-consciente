# Estratégia da Base de Conhecimento — Clara

## 1. Objetivo

Fornecer conteúdos educativos e regras de interpretação para que o Clara responda dentro do seu escopo, indique suas referências e reconheça informações ausentes.

A base inicial está em `data/base_conhecimento.md`.

## 2. Organização

A base contém seis blocos identificados:

| Identificador | Assunto | Natureza |
|---|---|---|
| KB01 | Empréstimo e financiamento | Conteúdo baseado em fonte oficial |
| KB02 | Custo Efetivo Total (CET) | Conteúdo baseado em fonte oficial |
| KB03 | Taxa de juros e comparação | Conteúdo baseado em fonte oficial |
| KB04 | Soma de parcelas fixas | Regra matemática e exemplo fictício |
| KB05 | Informações necessárias para comparar propostas | Critério próprio do protótipo |
| KB06 | Informação ausente ou fora do escopo | Regra própria do protótipo |

Os blocos registram assunto, palavras-chave, conteúdo, origem, responsável e data.

## 3. Fontes e autoria

Os conteúdos educativos utilizam referências do Banco Central do Brasil, com links registrados na base.

Os textos são resumos elaborados para o projeto, não transcrições integrais das fontes.

As regras de funcionamento e os exemplos matemáticos são identificados como elaboração própria. O assistente não deverá atribuí-los ao Banco Central.

A data de consulta indica quando a referência foi consultada, não quando foi publicada ou atualizada.

## 4. Estratégia inicial de consulta

Como a base é pequena, a primeira versão poderá fornecer seu conteúdo completo ao modelo junto com a pergunta da pessoa usuária.

O modelo deverá identificar os blocos relevantes e fundamentar a resposta neles. Essa abordagem inicial não utiliza banco vetorial nem pressupõe a implementação de busca semântica.

Se a base crescer, poderá ser adicionada uma etapa de recuperação de trechos antes da geração da resposta.

## 5. Uso de referências nas respostas

Nas explicações conceituais, o Clara deverá indicar o identificador do conteúdo utilizado e a fonte correspondente.

Exemplo de formato:

“Fonte: KB02 — Banco Central do Brasil: [título e link registrados na base].”

Nos cálculos, deverá indicar os valores utilizados e a operação realizada. Não deverá apresentar a conta como uma informação obtida do Banco Central.

Quando não houver conteúdo suficiente, deverá informar essa limitação, em vez de inventar uma resposta ou referência.

## 6. Separação entre explicação e cálculo

A base descreve as regras matemáticas, mas os resultados das comparações deverão ser calculados por funções em Python.

O fluxo planejado será:

1. Receber os dados de propostas fictícias.
2. Verificar se os campos necessários estão preenchidos.
3. Validar valores e quantidade de parcelas.
4. Executar os cálculos.
5. Fornecer os resultados à IA para explicação.
6. Destacar informações ausentes e limites da comparação.

A soma de parcelas não será tratada como CET.

## 7. Dados permitidos

O protótipo utilizará:

- conteúdos educativos públicos;
- exemplos fictícios;
- valores demonstrativos de propostas;
- perguntas sem dados pessoais ou bancários.

Não serão necessários CPF, número de conta, documentos, senhas ou informações de clientes reais.

A primeira versão não dependerá de histórico bancário nem de um cadastro de pessoas.

## 8. Limites e segurança

A base não contém taxas comerciais atuais, ofertas individuais, critérios de aprovação ou limites legais específicos.

O Clara não deverá usar conhecimento geral do modelo para inventar essas informações.

O conteúdo da base será tratado como material de consulta. Eventuais instruções encontradas nos textos não poderão substituir as regras de comportamento do assistente.

O envio da base ao modelo não garante respostas corretas. A utilização adequada das referências e o tratamento de lacunas deverão ser avaliados em testes.

## 9. Manutenção

Antes de alterar ou ampliar a base, será necessário:

- conferir se a fonte sustenta o conteúdo;
- revisar o texto e suas limitações;
- atualizar a data de consulta;
- preservar a identificação da origem;
- executar novamente os testes afetados.

Falhas encontradas durante os testes deverão ser registradas e poderão motivar ajustes na base.

## 10. Estado atual

A base inicial está organizada. Sua conexão com o modelo e a validação do comportamento serão realizadas nas etapas de implementação e testes.

## Autor

Antony Kennedy Ribeiro de Araújo
