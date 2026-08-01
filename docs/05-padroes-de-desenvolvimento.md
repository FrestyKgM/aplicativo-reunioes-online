# Padrões de Nomenclatura, Programação e Documentação

## Objetivo

Este documento define os padrões de nomenclatura, organização do código e boas práticas que deverão ser seguidos durante o desenvolvimento do MeetPoint, garantindo um projeto organizado, padronizado e de fácil manutenção.

---

## Padrões de nomenclatura

### Telas

As telas deverão utilizar nomes em **PascalCase**, terminando com `Page`.

Exemplos:

```dart
LoginPage
HomePage
MeetingPage
SettingsPage
```

Os arquivos utilizarão **snake_case**.

```text
login_page.dart
home_page.dart
meeting_page.dart
settings_page.dart
```

### Componentes

Os componentes reutilizáveis deverão possuir nomes claros.

Exemplos:

```dart
PrimaryButton
MeetingCard
ParticipantTile
CustomTextField
```

### Variáveis e métodos

Variáveis e métodos deverão utilizar **camelCase**.

Exemplos:

```dart
String userName;
String meetingCode;
bool isCameraEnabled;

createMeeting();
joinMeeting();
sendMessage();
```

Os nomes deverão ser descritivos, evitando abreviações.

### Classes

As classes deverão utilizar **PascalCase**.

Exemplos:

```dart
User
Meeting
Participant
Message
MeetingRepository
```

### Banco de dados

As tabelas e colunas deverão utilizar **snake_case**.

Exemplos:

```text
users
meetings
participants

user_id
meeting_id
created_at
```

---

## Práticas de programação

Durante o desenvolvimento deverão ser seguidas as seguintes práticas:

- escrever código simples e organizado;
- utilizar componentes reutilizáveis;
- evitar código duplicado;
- utilizar nomes claros para classes, métodos e variáveis;
- validar dados no aplicativo e no backend;
- tratar erros de forma adequada;
- armazenar informações sensíveis em arquivos `.env`;
- manter o código formatado e organizado.

O projeto seguirá a **Clean Architecture**, separando a aplicação em camadas para facilitar a manutenção.

---

## Organização do projeto

O aplicativo Flutter será organizado por funcionalidades.

Exemplo:

```text
lib/
├── core/
├── features/
├── shared/
└── main.dart
```

O backend seguirá uma estrutura modular.

```text
src/
├── auth/
├── users/
├── meetings/
├── messages/
└── notifications/
```

---

## Documentação

Toda funcionalidade desenvolvida deverá ser documentada.

O projeto deverá possuir:

- README com informações gerais;
- documentação da arquitetura;
- documentação da interface;
- documentação da identidade visual;
- documentação das APIs.

Comentários deverão ser utilizados apenas quando necessários para explicar regras importantes do sistema.

---

## Commits

As mensagens de commit deverão ser objetivas.

Exemplos:

```text
feat: adiciona tela de login
fix: corrige criação de reunião
docs: atualiza documentação
refactor: reorganiza módulo de autenticação
```

---

## Conclusão

A utilização desses padrões garante maior organização, padronização e qualidade durante o desenvolvimento do MeetPoint, facilitando a manutenção do sistema e o trabalho em equipe.
