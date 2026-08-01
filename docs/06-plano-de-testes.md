# Plano de Testes

## Objetivo

Este documento define os testes que serão realizados durante o desenvolvimento do MeetPoint e como seus resultados serão registrados. O objetivo é garantir o funcionamento correto do sistema, sua segurança, desempenho e facilidade de uso.

---

## Testes propostos

Durante o desenvolvimento serão realizados os seguintes testes:

- **Testes unitários:** validar funções e regras de negócio, como login, cadastro, criação de reuniões e validação de dados.
- **Testes de integração:** verificar a comunicação entre o aplicativo, a API, o banco de dados e os serviços de videoconferência.
- **Testes de interface:** conferir o funcionamento das telas, botões, formulários e navegação.
- **Testes de usabilidade:** avaliar se o aplicativo é simples e intuitivo para o usuário.
- **Testes de desempenho:** verificar tempo de resposta, consumo de memória e estabilidade em reuniões com vários participantes.
- **Testes de segurança:** validar autenticação, permissões de acesso e proteção dos dados dos usuários.
- **Testes de compatibilidade:** garantir o funcionamento em dispositivos Android e iOS com diferentes tamanhos de tela.

---

## Documentação dos resultados

Cada teste executado deverá ser registrado contendo:

- código do teste;
- funcionalidade testada;
- data da execução;
- resultado esperado;
- resultado obtido;
- situação (Aprovado ou Reprovado);
- observações, quando necessário.

Exemplo:

| Código | Funcionalidade | Resultado esperado | Situação |
|---------|----------------|-------------------|----------|
| CT-001 | Login | Usuário acessa o sistema | Aprovado |
| CT-002 | Entrar em reunião | Participante entra com código válido | Aprovado |
| CT-003 | Código inválido | Exibir mensagem de erro | Reprovado |

As evidências dos testes, como capturas de tela ou vídeos, poderão ser armazenadas na pasta:

```text
docs/testes/evidencias/
```

---

## Conclusão

Os testes serão realizados durante todo o desenvolvimento do MeetPoint, permitindo identificar falhas, validar funcionalidades e garantir a qualidade do sistema antes da entrega final.
