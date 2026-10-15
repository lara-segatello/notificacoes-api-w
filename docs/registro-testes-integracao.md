# Registro de Testes de Integração

Aluno: Lara segatello Marquez

Grupo: Grupo 7

Data: 15/10/2026

## Banco de teste

Nome do banco de teste: notificacoes_test;

Por que ele é separado do banco da API (uma frase): Para não gerar confusões 

## Testes escritos

| #   | Arquivo | O que o teste verifica | Verde ou vermelho? |

| --- | ------- | ---------------------- | ------------------ |

| 1   | tests/integration/evento.integration.test.js.         |  Verifica se o evento é gravado corretamente no banco de dados.                      | Verde                   |

| 2   | tests/integration/participante.integration.test.js         | Verifica se um participante com e-mail inválido é recusado e não é gravado no banco.                       |  Verde                  |

| 3   |tests/integration/participante.integration.test.js         | Verifica se a atualização do nome do participante é realmente salva no banco de dados.                        |  Vermelho                  |

## Resultado

Linha "Tests:" da saída do npm run test:integration: 
# TEST 1:
 PASS  tests/integration/evento.integration.test.js
 PASS  tests/integration/participante.integration.test.js

Test Suites: 2 passed, 2 total
Tests:       4 passed, 4 total
Snapshots:   0 total
Time:        0.74 s, estimated 1 s
Ran all test suites matching tests/integration.

# TEST 2:
 PASS  tests/integration/participante.integration.test.js
 PASS  tests/integration/evento.integration.test.js

Test Suites: 2 passed, 2 total
Tests:       5 passed, 5 total
Snapshots:   0 total
Time:        0.784 s, estimated 1 s
Ran all test suites matching tests/integration.

# TEST 3:
 PASS  tests/integration/evento.integration.test.js

Test Suites: 1 failed, 1 passed, 2 total
Tests:       1 failed, 5 passed, 6 total
Snapshots:   0 total
Time:        0.829 s, estimated 1 s
Ran all test suites matching tests/integration.
## Defeito encontrado

Teste: 3

Esperado: "Ana Maria"

Obtido: "Ana" (se o nome não foi atualizado no banco de dados).

O que o usuário da API veria (a rota responde 200, mas...): 
A rota responde 200, o nome do participante pode continuar como “Ana” em vez de ser atualizado para “Ana Maria” no banco de dados.

