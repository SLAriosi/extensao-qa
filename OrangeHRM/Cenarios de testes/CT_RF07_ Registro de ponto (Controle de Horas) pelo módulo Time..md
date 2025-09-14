## Cenário 07: Registro de ponto (Controle de Horas) pelo módulo Time.

### Caso de Teste 01: Marcar ponto (Check In) com horário válido.

| ID       | Descrição                                                                  |
| :------- | :------------------------------------------------------------------------- |
| C07-CT01 | O sistema deve permitir que o usuário registre sua entrada com sucesso.    |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao módulo "Time".    |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu \"Time > Attendance > Punch In\" |
| **E** verifica que o horário atual é válido                     |
| **QUANDO** clicar em \"Punch In\"                               |
| **ENTÃO** o registro de entrada deve ser salvo com sucesso      |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve confirmar o registro com uma mensagem e salvar o horário. |

| **Teste realizado Evidência**                                   |
| :-------------------------------------------------------------- |
| https://jam.dev/c/cf5cbde2-90cc-4b03-8fef-c42cb92bbd86 |

---

### Caso de Teste 02: Tentar marcar ponto sem horário permitido ou fora do expediente.

| ID       | Descrição                                                                 |
| :------- | :------------------------------------------------------------------------ |
| C07-CT02 | O sistema deve impedir o registro de entrada fora do horário permitido.   |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar fora do horário permitido para entrada.  |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu \"Punch In\" fora do horário permitido |
| **QUANDO** tentar registrar o ponto                             |
| **ENTÃO** o sistema deve exibir uma mensagem de erro ou restrição |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve impedir o registro e apresentar mensagem adequada. |

| **Teste realizado Evidência**                                   |
| :-------------------------------------------------------------- |
| https://jam.dev/c/cf5cbde2-90cc-4b03-8fef-c42cb92bbd86 |

Prineiro mostra permitindo e depois não permitindo, aparentemente o não permitido é só quando ele valida que o horário marcado no relógio do site é o horário de agora e agora não é mais permitido bater o ponto.

---

### Caso de Teste 03: Consultar registro de ponto anterior.

| ID       | Descrição                                                              |
| :------- | :---------------------------------------------------------------------- |
| C07-CT03 | O sistema deve permitir que o usuário consulte registros de ponto anteriores. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve ter ao menos um registro de ponto anterior.    |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu \"Time > Attendance > My Records\" |
| **QUANDO** selecionar uma data anterior                         |
| **ENTÃO** o sistema deve exibir os registros de entrada e saída da data selecionada |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve exibir corretamente os registros existentes da data informada. |

| **Teste realizado Evidência**                                   |
| :-------------------------------------------------------------- |
| https://jam.dev/c/dc071d7e-cc2b-40a0-b8a9-77ae45ed227f |
