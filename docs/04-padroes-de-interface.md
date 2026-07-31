# Padrões de Interface

## 1. Objetivo

A interface do aplicativo será simples, intuitiva e responsiva. O objetivo é permitir que o usuário crie, agende ou entre em uma reunião com poucos toques, tanto em dispositivos Android quanto iOS.

## 2. Padrão visual

Todas as telas deverão seguir o mesmo padrão de cores, fontes, ícones, botões e espaçamentos.

Serão utilizados:

* textos legíveis;
* botões grandes;
* ícones acompanhados de texto;
* cores com bom contraste;
* espaçamento adequado entre os elementos;
* suporte aos modos claro e escuro;
* mensagens de erro simples;
* indicadores de carregamento;
* confirmação para ações importantes.

Ações como excluir uma conta, remover participantes ou encerrar uma reunião deverão solicitar confirmação.

## 3. Menu principal

O aplicativo terá um menu localizado na parte inferior da tela, facilitando a navegação em dispositivos móveis.

| Opção     | Função                                     |
| --------- | ------------------------------------------ |
| Início    | Criar, agendar ou entrar em uma reunião    |
| Reuniões  | Visualizar reuniões agendadas e anteriores |
| Contatos  | Acessar usuários e grupos salvos           |
| Mensagens | Visualizar conversas e avisos              |
| Perfil    | Alterar dados pessoais e configurações     |

## 4. Tela inicial

A tela inicial apresentará as principais funções do aplicativo:

* criar uma reunião;
* entrar com código;
* agendar uma reunião;
* visualizar as próximas reuniões.

Os botões principais deverão ter maior destaque visual.

## 5. Tela de login

A tela de login terá:

* campo de e-mail;
* campo de senha;
* botão para entrar;
* opção para recuperar senha;
* opção para criar uma conta;
* opção de login com Google ou Apple.

## 6. Tela de cadastro

A tela de cadastro solicitará apenas as informações necessárias:

* nome;
* e-mail;
* senha;
* confirmação de senha;
* aceite dos termos de uso.

Os campos deverão exibir mensagens claras de validação, como:

* “Preencha este campo”;
* “E-mail inválido”;
* “As senhas não são iguais”;
* “A senha deve possuir pelo menos oito caracteres”.

Também haverá a opção de mostrar ou ocultar a senha.

## 7. Tela de reunião

Durante a reunião, os controles principais ficarão na parte inferior da tela.

Serão exibidos botões para:

* ativar ou desativar o microfone;
* ativar ou desativar a câmera;
* compartilhar a tela;
* abrir as mensagens;
* visualizar os participantes;
* sair ou encerrar a reunião.

Recursos menos utilizados, como gravação, legendas, reações e salas simultâneas, ficarão em um menu adicional.

## 8. Tela de participantes

A tela mostrará a lista de pessoas presentes na reunião, identificando:

* organizador;
* moderadores;
* participantes;
* convidados.

Usuários autorizados poderão:

* silenciar participantes;
* remover participantes;
* alterar permissões;
* aceitar usuários da sala de espera;
* bloquear novas entradas.

## 9. Tela de agendamento

A tela de agendamento terá os seguintes campos:

* título da reunião;
* descrição;
* data;
* horário;
* duração;
* participantes convidados;
* senha opcional;
* ativação da sala de espera.

Após o agendamento, o sistema deverá gerar um link e um código de acesso.

## 10. Tela de configurações

As configurações serão divididas nas seguintes categorias:

* conta;
* áudio e vídeo;
* notificações;
* privacidade e segurança;
* acessibilidade;
* economia de dados e bateria.

## 11. Mensagens e notificações

O aplicativo utilizará mensagens simples para informar o resultado das ações.

Exemplos:

* “Reunião criada com sucesso”;
* “Código de reunião inválido”;
* “Conexão instável”;
* “Microfone desativado”;
* “Participante removido”.

As notificações poderão informar convites, lembretes, mudanças de horário e cancelamentos.

## 12. Acessibilidade

A interface deverá oferecer:

* suporte a leitores de tela;
* ajuste do tamanho da fonte;
* legendas;
* contraste adequado;
* identificação textual dos ícones;
* botões com tamanho apropriado;
* navegação simples.

## 13. Responsividade

As telas deverão se adaptar a diferentes tamanhos e orientações de dispositivos.

A interface deverá funcionar corretamente em:

* celulares com telas pequenas;
* celulares com telas grandes;
* tablets;
* modo retrato;
* modo paisagem.

## 14. Conclusão

Os padrões de interface foram definidos para reduzir a complexidade encontrada em outros aplicativos de reunião. O foco será oferecer uma navegação simples, consistente e acessível, permitindo que as principais tarefas sejam realizadas com poucos toques.
