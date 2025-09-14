## Cenário 09: Consulta de colaboradores no módulo Diretório.

### Caso de Teste 01: Buscar colaborador por nome com sucesso.

| ID       | Descrição                                                               |
| :------- | :---------------------------------------------------------------------- |
| C09-CT01 | O sistema deve retornar corretamente o colaborador pesquisado pelo nome. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu \"Directory\"              |
| **E** insere o nome de um colaborador existente no campo de busca |
| **QUANDO** clicar em \"Search\"                                 |
| **ENTÃO** o sistema deve exibir o colaborador correspondente à busca |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O nome, cargo e localização do colaborador devem ser exibidos corretamente. |

| **Teste realizado Evidência**                                   |
| :-------------------------------------------------------------- |
| https://jam.dev/c/668bdde9-d4e4-4949-99be-85ac54fc276a |

---

### Caso de Teste 02: Buscar colaborador inexistente.

| ID       | Descrição                                                                   |
| :------- | :-------------------------------------------------------------------------- |
| C09-CT02 | O sistema deve exibir uma mensagem apropriada quando nenhum colaborador for encontrado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu \"Directory\"              |
| **E** digita um nome que não corresponde a nenhum colaborador    |
| **QUANDO** clicar em \"Search\"                                 |
| **ENTÃO** uma mensagem como \"No Records Found\" deve ser exibida |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve exibir claramente que não há registros encontrados. |

| **Teste realizado Evidência**                                   |
| :-------------------------------------------------------------- |
| https://jam.dev/c/bc265aef-ca1a-43ab-bb44-17ce7fffcafb |

Aparentemente não funciona, no jeito que está hoje, nem permitindo clicar no OK está dando mais.

---

### Caso de Teste 03: Aplicar filtro por cargo (Job Title).

| ID       | Descrição                                                                |
| :------- | :------------------------------------------------------------------------ |
| C09-CT03 | O sistema deve permitir a filtragem de colaboradores por cargo.           |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e o sistema deve conter dados de funcionários. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu \"Directory\"              |
| **E** seleciona um cargo no campo \"Job Title\"                 |
| **QUANDO** clicar em \"Search\"                                 |
| **ENTÃO** apenas os colaboradores com o cargo selecionado devem ser listados |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve funcionar corretamente e retornar apenas resultados válidos. |

| **Teste realizado Evidência**                                   |
| :-------------------------------------------------------------- |
| https://jam.dev/c/274116f0-4606-4b74-aae4-9d42d6bd784b |
