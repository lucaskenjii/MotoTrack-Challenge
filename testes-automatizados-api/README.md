# Testes Automatizados - MotoTrack API

Este diretório contém os casos de testes automatizados desenvolvidos para validação da API do sistema MotoTrack.

## Ferramenta utilizada
- Postman (Collection Runner)
- Variável de ambiente: `userId` (preenchida automaticamente após o cadastro)

## Endpoints testados
| Caso | Método | Endpoint | Descrição |
|------|--------|----------|-----------|
| 1 | GET | `/db/valida-senha` | Validação de senha (simula login) |
| 2 | POST | `/usuarios` | Cadastra novo usuário e salva o `id` |
| 3 | PUT | `/usuarios/{id}` | Atualiza usuário usando o `id` salvo automaticamente |
| 4 | GET | `/usuarios` ou `/motos` | Lista registros para verificação |

## Como executar os testes
1. Importe `MotoTrack_API_Tests.json` no Postman
2. Selecione o ambiente `MotoTrack-Local`
3. Clique em **Runner**
4. Execute a coleção **MotoTrack API Tests**
5. Todos os testes devem aparecer como **Passed ✅**

## Resultado esperado
- Cadastro: `201 Created`
- Atualização: `200 OK`
- Listagem: retorna dados em formato JSON
- Login: retorna confirmação válida
