# Proposta de Arquitetura

O sistema será um aplicativo móvel para Android e iOS, desenvolvido em Flutter. Dessa forma, será possível utilizar uma única base de código para as duas plataformas.

A aplicação seguirá a Clean Architecture, separando a interface, as regras do sistema e o acesso aos dados. Essa organização facilita a manutenção e a evolução do projeto.

O backend será desenvolvido em NestJS e será responsável pelo cadastro de usuários, autenticação, reuniões, mensagens e armazenamento das informações.

A comunicação utilizará:

* API REST para cadastro, login e consulta de dados;
* WebSocket para mensagens e atualizações em tempo real;
* WebRTC para chamadas de áudio e vídeo;
* LiveKit para gerenciamento das reuniões;
* Coturn para conexões em redes restritas.

O PostgreSQL será utilizado como banco de dados principal. O Redis poderá armazenar sessões, cache e dados temporários.

A infraestrutura será executada em Docker, permitindo instalar e executar os componentes de maneira organizada.

## Tecnologias

| Componente                | Tecnologia |
| ------------------------- | ---------- |
| Aplicativo móvel          | Flutter    |
| Linguagem do aplicativo   | Dart       |
| Backend                   | NestJS     |
| Linguagem do backend      | TypeScript |
| Banco de dados            | PostgreSQL |
| Cache e sessões           | Redis      |
| Áudio e vídeo             | WebRTC     |
| Servidor de reuniões      | LiveKit    |
| Servidor STUN/TURN        | Coturn     |
| Comunicação em tempo real | WebSocket  |
| Infraestrutura            | Docker     |

Essa arquitetura utiliza tecnologias modernas, gratuitas e de código aberto, além de permitir a criação de um sistema multiplataforma e escalável.

