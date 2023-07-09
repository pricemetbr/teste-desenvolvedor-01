# TESTE PARA VAGA DESENVOLVEDOR PL/SR

## Descrição

Desenvolva uma API que tenha as seguintes rotas:

| Método | Path        | Descrição                                                  |
| :----- | :---------- | :--------------------------------------------------------- |
| `GET`  | `/`         | Essa rota vai devolver um `"Hello World"` e o status `200` |
| `GET`  | `/produtos` | Essa rota vai devolver uma lista de objetos do banco       |
| `POST` | `/produtos` | Essa rota vai receber um array de objetos                  |

## Requisitos dos endpoints de Produtos

- [x] POST:
  - Irá receber acima de 100k de linhas então insira no banco em chunks de 10k.
- [x] GET:
  - Vai receber como parâmetro dois dados para paginação:
      - **row_count**: quantidade de linhas a ser exibida.
      - **row_skip**: quantidade de linhas a ser ignorada.
- [ ] Validação dos campos antes da inserção no banco.
- [ ] Em caso de erro de validação:
  - Não inserir nenhum dado.
  - Informar ao usuário qual campo está errado e qual tipo de dado esperado.

## Requisitos do Projeto

- [x] Construção em NodeJS.
- [ ] Frameworks: Fastify/NestJS.
- [ ] Banco de dados (POSTGRES/MYSQL/SQLITE).
- [ ] Gerar logs contendo:
  - Data e hora de acionamento
  - Quantidade de itens a serem inseridos (em rotas POST)
  - Solicitação do Usuário (em rotas GET)

#### Legenda

- [ ] Opcional/Desejável
- [x] Obrigatório

## Conteúdo do repositório

| Arquivo                       | Descrição                                                                       |
| :---------------------------- | :------------------------------------------------------------------------------ |
| `modelo_do_objeto.json`       | modelo do objeto recebido e devolvido nas rotas de produto                      |
| `dados_a_serem_inseridos.zip` | Arquivo contendo um json com 190k de linhas com o objeto modelo (para inserção) |
