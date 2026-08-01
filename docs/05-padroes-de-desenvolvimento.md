# Padrões de Nomenclatura e Desenvolvimento

## 1. Objetivo

Este documento define os padrões de nomenclatura, organização do código, práticas de programação e documentação que deverão ser seguidos durante o desenvolvimento do MeetPoint.

O objetivo é manter o projeto organizado, legível, padronizado e fácil de manter.

---

## 2. Padrões de nomenclatura

### 2.1 Telas

As telas do aplicativo deverão possuir nomes claros e relacionados à sua função.

As classes deverão utilizar o padrão `PascalCase` e terminar com `Page`.

Exemplos:

```dart
LoginPage
RegisterPage
HomePage
MeetingPage
ScheduleMeetingPage
ParticipantsPage
SettingsPage
ProfilePage
```

Os nomes dos arquivos deverão utilizar `snake_case`.

Exemplos:

```text
login_page.dart
register_page.dart
home_page.dart
meeting_page.dart
schedule_meeting_page.dart
participants_page.dart
settings_page.dart
profile_page.dart
```

---

### 2.2 Componentes

Os componentes reutilizáveis deverão possuir nomes que indiquem claramente sua função.

Exemplos de classes:

```dart
PrimaryButton
SecondaryButton
MeetingCard
ParticipantTile
CustomTextField
LoadingIndicator
ConfirmationDialog
```

Exemplos de arquivos:

```text
primary_button.dart
secondary_button.dart
meeting_card.dart
participant_tile.dart
custom_text_field.dart
loading_indicator.dart
confirmation_dialog.dart
```

---

### 2.3 Variáveis

As variáveis deverão utilizar o padrão `camelCase`.

Exemplos:

```dart
String userName;
String meetingCode;
bool isMicrophoneEnabled;
bool isCameraEnabled;
int participantCount;
```

Os nomes deverão ser claros e descritivos.

Evitar:

```dart
String n;
bool mic;
int qtd;
```

Preferir:

```dart
String userName;
bool isMicrophoneEnabled;
int participantCount;
```

---

### 2.4 Constantes

As constantes deverão utilizar `camelCase` e a palavra-chave `const`.

Exemplos:

```dart
const int minimumPasswordLength = 8;
const int maximumParticipants = 50;
const Duration connectionTimeout = Duration(seconds: 30);
```

Constantes globais poderão ser agrupadas em uma classe.

```dart
class AppConstants {
  static const String appName = 'MeetPoint';
  static const int minimumPasswordLength = 8;
  static const int maximumParticipants = 50;
}
```

---

### 2.5 Métodos e funções

Os métodos deverão começar com um verbo e indicar claramente a ação realizada.

Exemplos:

```dart
createMeeting()
joinMeeting()
scheduleMeeting()
loadParticipants()
validateEmail()
toggleMicrophone()
sendMessage()
```

Métodos que retornam valores booleanos deverão utilizar prefixos como:

```text
is
has
can
should
```

Exemplos:

```dart
isUserAuthenticated()
hasCameraPermission()
canRemoveParticipant()
shouldShowNotification()
```

---

### 2.6 Classes e modelos

As classes deverão utilizar o padrão `PascalCase`.

Exemplos:

```dart
User
Meeting
Participant
Message
MeetingRepository
AuthenticationService
```

Os modelos de dados deverão possuir nomes no singular.

Correto:

```dart
Meeting
Participant
Message
```

Evitar:

```dart
Meetings
Participants
Messages
```

---

### 2.7 Pastas

Os nomes das pastas deverão utilizar letras minúsculas e `snake_case`.

Exemplo:

```text
lib/
├── core/
├── features/
├── shared/
├── services/
└── repositories/
```

Cada funcionalidade poderá possuir sua própria estrutura:

```text
features/
└── meeting/
    ├── data/
    ├── domain/
    └── presentation/
```

---

### 2.8 Rotas do aplicativo

As rotas deverão utilizar letras minúsculas e palavras separadas por hífen.

Exemplos:

```text
/login
/register
/home
/meetings
/meeting-details
/schedule-meeting
/settings
```

---

### 2.9 Endpoints da API

Os endpoints da API deverão utilizar substantivos no plural e letras minúsculas.

Exemplos:

```text
GET /users
GET /meetings
POST /meetings
GET /meetings/{id}
POST /meetings/{id}/participants
DELETE /meetings/{id}/participants/{participantId}
```

Ações específicas poderão ser representadas por sub-recursos.

Exemplos:

```text
POST /meetings/{id}/join
POST /meetings/{id}/leave
POST /meetings/{id}/start
POST /meetings/{id}/end
```

---

### 2.10 Banco de dados

As tabelas e colunas deverão utilizar `snake_case`.

Exemplos de tabelas:

```text
users
meetings
participants
messages
meeting_participants
```

Exemplos de colunas:

```text
user_id
meeting_id
created_at
updated_at
is_active
```

As chaves primárias deverão utilizar:

```text
id
```

As chaves estrangeiras deverão indicar a entidade relacionada.

Exemplos:

```text
user_id
meeting_id
participant_id
```

---

## 3. Práticas de programação

### 3.1 Código legível

O código deverá ser simples, organizado e fácil de compreender.

Deverão ser evitados:

- métodos muito grandes;
- classes com muitas responsabilidades;
- nomes genéricos;
- código duplicado;
- comentários desnecessários;
- valores fixos espalhados pelo código.

---

### 3.2 Responsabilidade única

Cada classe, serviço ou método deverá possuir uma responsabilidade principal.

Por exemplo, uma classe responsável pela autenticação não deverá também gerenciar reuniões ou mensagens.

---

### 3.3 Reutilização de componentes

Elementos utilizados em várias telas deverão ser transformados em componentes reutilizáveis.

Exemplos:

- botões;
- campos de texto;
- cartões de reunião;
- caixas de diálogo;
- indicadores de carregamento;
- mensagens de erro.

---

### 3.4 Evitar código duplicado

Trechos repetidos deverão ser transformados em funções, componentes ou serviços reutilizáveis.

Essa prática facilita a manutenção e reduz a possibilidade de erros.

---

### 3.5 Tratamento de erros

Todas as operações que podem falhar deverão possuir tratamento adequado.

Exemplos:

- falha de conexão;
- código de reunião inválido;
- usuário não autorizado;
- erro ao carregar participantes;
- falha ao ativar câmera ou microfone.

As mensagens exibidas ao usuário deverão ser claras e simples.

---

### 3.6 Validação de dados

Os dados deverão ser validados tanto no aplicativo quanto no backend.

Exemplos:

- e-mail válido;
- senha com tamanho mínimo;
- código de reunião válido;
- campos obrigatórios preenchidos;
- data e horário corretos.

---

### 3.7 Segurança

Informações sensíveis não deverão ser armazenadas diretamente no código.

Não deverão ser enviadas ao repositório:

- senhas;
- tokens;
- chaves de API;
- credenciais do banco de dados;
- certificados privados.

Essas informações deverão ser armazenadas em variáveis de ambiente.

Exemplo:

```text
.env
```

O arquivo `.env` deverá ser adicionado ao `.gitignore`.

---

### 3.8 Programação assíncrona

Operações de rede, banco de dados e arquivos deverão utilizar programação assíncrona.

No Flutter, deverão ser utilizados `Future`, `async` e `await`.

Exemplo:

```dart
Future<void> loadMeetings() async {
  final meetings = await meetingRepository.getMeetings();
}
```

---

### 3.9 Gerenciamento de estado

O gerenciamento de estado deverá seguir um único padrão durante todo o projeto.

Para o MeetPoint, será utilizado o Riverpod.

Não deverão ser misturadas várias soluções de gerenciamento de estado sem necessidade.

---

### 3.10 Formatação do código

O código deverá seguir os formatadores oficiais das tecnologias utilizadas.

No Flutter:

```text
dart format
```

No NestJS e TypeScript:

```text
Prettier
ESLint
```

Antes de enviar alterações ao repositório, o código deverá estar formatado e sem erros de análise.

---

## 4. Organização do projeto Flutter

Estrutura sugerida:

```text
lib/
├── core/
│   ├── constants/
│   ├── errors/
│   ├── routes/
│   ├── theme/
│   └── utils/
├── features/
│   ├── authentication/
│   ├── home/
│   ├── meeting/
│   ├── messages/
│   ├── profile/
│   └── settings/
├── shared/
│   └── widgets/
└── main.dart
```

Cada funcionalidade poderá seguir a Clean Architecture.

Exemplo:

```text
meeting/
├── data/
│   ├── datasources/
│   ├── models/
│   └── repositories/
├── domain/
│   ├── entities/
│   ├── repositories/
│   └── usecases/
└── presentation/
    ├── pages/
    ├── providers/
    └── widgets/
```

---

## 5. Organização do backend

Estrutura sugerida:

```text
src/
├── auth/
├── users/
├── meetings/
├── participants/
├── messages/
├── notifications/
├── common/
└── main.ts
```

Cada módulo deverá conter seus próprios arquivos.

Exemplo:

```text
meetings/
├── dto/
├── entities/
├── meetings.controller.ts
├── meetings.service.ts
└── meetings.module.ts
```

---

## 6. Práticas de documentação

### 6.1 Comentários

Os comentários deverão ser utilizados apenas quando forem necessários para explicar uma regra ou decisão que não seja evidente.

Evitar comentários que apenas repetem o código.

Evitar:

```dart
// Ativa o microfone
isMicrophoneEnabled = true;
```

Preferir comentários que expliquem uma regra:

```dart
// O áudio deve ser priorizado quando a conexão estiver instável.
```

---

### 6.2 Documentação de classes e métodos

Métodos públicos ou que possuam regras importantes deverão ter uma breve descrição.

Exemplo em Dart:

```dart
/// Cria uma nova reunião e retorna o código de acesso gerado.
Future<String> createMeeting(Meeting meeting) async {
  // implementação
}
```

Exemplo em TypeScript:

```typescript
/**
 * Cria uma nova reunião e retorna os dados cadastrados.
 */
async createMeeting(data: CreateMeetingDto) {
  // implementação
}
```

---

### 6.3 Documentação da API

A API deverá ser documentada com Swagger ou OpenAPI.

A documentação deverá apresentar:

- endpoint;
- método HTTP;
- parâmetros;
- corpo da requisição;
- resposta esperada;
- possíveis erros;
- necessidade de autenticação.

---

### 6.4 README

O arquivo `README.md` deverá conter:

- nome do projeto;
- descrição;
- objetivo;
- tecnologias;
- instruções de instalação;
- estrutura do projeto;
- links para a documentação;
- status do desenvolvimento.

---

## 7. Padrão de commits

As mensagens de commit deverão ser curtas e descrever claramente a alteração realizada.

Exemplos:

```text
Adiciona tela de login
Cria endpoint de reuniões
Corrige validação de e-mail
Atualiza documentação da arquitetura
Adiciona logo do MeetPoint
```

Também poderá ser utilizado o padrão Conventional Commits.

Exemplos:

```text
feat: adiciona tela de login
fix: corrige entrada por código
docs: atualiza documentação
style: formata componentes
test: adiciona testes de autenticação
refactor: reorganiza serviço de reuniões
```

---

## 8. Padrão de branches

A branch principal será:

```text
main
```

Novas funcionalidades deverão ser desenvolvidas em branches separadas.

Exemplos:

```text
feature/login
feature/create-meeting
feature/meeting-chat
fix/camera-permission
docs/interface-standards
```

Depois de concluídas, as alterações deverão ser revisadas antes de serem integradas à branch principal.

---

## 9. Testes

Sempre que possível, deverão ser criados testes para:

- regras de negócio;
- validações;
- autenticação;
- criação de reuniões;
- entrada por código;
- permissões dos participantes;
- tratamento de erros.

Os testes deverão possuir nomes que descrevam claramente o comportamento esperado.

Exemplo:

```dart
test('deve retornar erro quando o código da reunião for inválido', () {
  // teste
});
```

---

## 10. Revisão de código

Antes de concluir uma funcionalidade, deverá ser verificado se:

- os nomes estão claros;
- não existe código duplicado;
- os erros foram tratados;
- os dados foram validados;
- o código está formatado;
- os testes estão funcionando;
- a documentação foi atualizada;
- nenhuma informação sensível foi enviada ao repositório.

---

## 11. Conclusão

Os padrões definidos neste documento deverão ser seguidos durante todo o desenvolvimento do MeetPoint.

A padronização dos nomes, da estrutura do código, dos commits e da documentação ajuda a manter o projeto organizado, facilita o trabalho em equipe e reduz erros durante a manutenção e evolução do sistema.
