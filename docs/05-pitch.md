# Pitch — Clara, Assistente de Crédito Consciente

## 1. Problema

Muitas pessoas comparam empréstimos olhando apenas para a taxa de juros ou para o valor das parcelas. Essa análise pode esconder tarifas, impostos, seguros e outros custos da operação.

Também existe dificuldade para interpretar o Custo Efetivo Total, conhecido como CET, e identificar quais informações são necessárias antes de comparar propostas.

## 2. Solução

A Clara é um assistente virtual educacional que explica conceitos de crédito em linguagem simples e ajuda a comparar propostas fictícias.

Ela utiliza uma base de conhecimento organizada, responde com apoio de um modelo local e possui regras para evitar respostas inseguras ou inventadas.

## 3. Como funciona

A aplicação possui três componentes principais:

1. Base de conhecimento em Markdown;
2. Assistente conversacional com Ollama e Gemma 3 4B;
3. Comparador determinístico desenvolvido em Python.

O modelo responde dúvidas conceituais, enquanto os cálculos das propostas são realizados diretamente pelo código Python.

## 4. Demonstração

Durante a demonstração, apresento:

1. A tela inicial da Clara;
2. A base de conhecimento carregada;
3. Uma pergunta sobre o CET;
4. Uma pergunta sobre taxa individual de banco;
5. Uma tentativa de obter aprovação de empréstimo;
6. O comparador de duas propostas fictícias;
7. O alerta quando os valores liberados são diferentes.

## 5. Exemplo de comparação

A Proposta A possui:

- 24 parcelas de R$ 350,00;
- total de R$ 8.400,00.

A Proposta B possui:

- 36 parcelas de R$ 260,00;
- total de R$ 9.360,00.

A aplicação calcula a diferença de R$ 960,00, mas também informa que a soma das parcelas não substitui o CET.

## 6. Segurança

A Clara não acessa bancos, não consulta contas, não analisa CPF, não prevê aprovação e não recomenda contratação de crédito.

O projeto utiliza apenas dados fictícios e possui proteção contra:

- tentativa de revelar instruções internas;
- promessa de aprovação;
- solicitação de senha ou CPF;
- afirmações de acesso a dados bancários;
- respostas que não estejam fundamentadas na base.

## 7. Tecnologias

- Python;
- Streamlit;
- Requests;
- Ollama;
- Gemma 3 4B;
- Markdown;
- Base de conhecimento com referências do Banco Central do Brasil.

## 8. Resultados

Os testes demonstraram que:

- a Clara explica o CET corretamente;
- recusa previsões de aprovação;
- não processa dados sensíveis;
- resiste a tentativas de ignorar suas regras;
- calcula corretamente a soma das parcelas;
- alerta sobre limitações quando os valores liberados são diferentes.

## 9. Limitações

Este é um protótipo educacional. Ele não representa uma instituição financeira e não realiza análise real de crédito.

O comparador calcula somente a soma das parcelas. Uma análise completa precisa considerar o CET, o contrato, tarifas, impostos, seguros, entradas e outros pagamentos.

## 10. Encerramento

A Clara demonstra como inteligência artificial, programação e uma base de conhecimento podem ser combinadas para criar uma experiência educativa e segura.

O principal objetivo não é indicar qual empréstimo contratar, mas ajudar a pessoa usuária a fazer perguntas melhores e entender quais informações devem ser analisadas antes de tomar uma decisão financeira.
