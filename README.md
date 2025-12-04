📄 README – Teste de Carga e Pico com JMeter
📌 Visão Geral

Este documento apresenta o resultado da execução de um teste de carga utilizando o Apache JMeter, com o objetivo de validar o seguinte critério de aceitação:

250 requisições por segundo com tempo de resposta (90th percentile) inferior a 2 segundos.

Foram simuladas requisições para um cenário composto por 1 chamada GET e 3 chamadas POST, totalizando 1000 requisições durante a execução.

⚙️ Estrutura do Teste

Ferramenta: Apache JMeter 5.6.3

Cenário executado:

1 requisição GET

3 requisições POST

Execuções configuradas: 250 loops

Total de requisições: 1000

Listeners utilizados:

View Results in Table

Aggregate Report

📊 Relatório da Execução (Aggregate Report)
Totais consolidados:
Métrica	Valor
Samples	1000
Média	1120 ms
Mediana	1032 ms
90th percentile	2134 ms
Throughput	134,4 req/s
Máximo	3099 ms
Erros	0%
❌ Avaliação do Critério de Aceitação

O critério definido exigia:

250 requisições por segundo, e

90th percentile < 2000 ms

Resultado obtido:

Throughput: 134,4 req/s
→ abaixo dos 250 req/s esperados

90th percentile: 2134 ms
→ acima do limite de 2000 ms

Conclusão:

O critério de aceitação não foi atendido.

📝 Justificativa (Explicação Simples)

A aplicação respondeu corretamente a todas as requisições (0% de erro), porém:

A vazão (throughput) foi insuficiente, atingindo apenas cerca de 134 req/s — aproximadamente metade do exigido.

O tempo de resposta apresentou variações, elevando o 90th percentile para acima de 2 segundos.

Isso indica que o sistema não conseguiu manter performance estável sob carga mais elevada.
