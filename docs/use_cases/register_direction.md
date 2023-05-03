# PI-001

## Cadastrar Direcionamento

### História do Usuário

Eu como usuário quero poder criar um direcionamento de acordo com a minha escolha de termos chave, termos de exclusão e tipos de noticias para que o bot direcione-as para meu grupo de WhatsApp.

### Critério de aceitação

- Deve ser possível cadastrar palavras conforme a escolha do usuário
- Deve ser possível excluir palavras chaves conforme a escolha do usuário
- É necessário que o usuário seja o administrador do grupo
- O usuário não deve repetir termos nos campos de exclusão e inclusão concomitantemente

### Fluxo Principal

- Pré-condições: o usuário deve estar autenticado no sistema
- Usuário aperta no botão "criar direcionamento"
- O sistema mostra o modal com o formulário para o cadastro com os um campo para inserir um novo termo de inclusão e outro para termo de exclusão
- O usuário é direcionado ao novo modal para selecionar o grupo de WhatsApp para direcionamento, podendo [Cadastrar um Novo Grupo de WhatsApp](#cadastrar-novo-grupo-de-whatsapp)
- O usuário clica no botão confirmar para finalizar o cadastro

### Fluxo alternativo

- Titulo do Direcionamento não foi especificado: o usuário é impedido de prosseguir ao modal de seleção de Grupo
- Nenhum termo de inclusão foi inserido: o usuário é impedido de prosseguir ao modal de seleção de Grupo
- Há termo(s) de inclusão igual(is) a termos de exclusão: o usuário é impedido de prosseguir ao modal de seleção de Grupo
- O grupo selecionado não é administrado pelo usuário: sistema exibe um aviso de erro e impede o cadastro do Direcionamento

## Cadastrar Novo Grupo de WhatsApp

### História

Eu como usuário poderei cadastrar um grupo do WhatsApp para poder seleciona-lo ao criar novos direcionamentos. Para tal, o bot entrará no grupo a partir de um link de convite.

### Critérios de aceitação

- Deve ser possível personalizar o nome de exibição do grupo no sistema
- É necessário que o usuário seja administrador do grupo para cadastra-lo ao sistema

### Fluxo principal

- Pré condições: o usuário deve estar autenticado no sistema, ser administrador do grupo, estar na tela de criação de Direcionamento ou na tela de listagem de Grupos de WhatsApp
- O sistema mostra o modal de cadastro com um titulo editável e campo para o link de convite
- Usuário é confirmado como administrador e o grupo é adicionado a lista de Grupos do WhatsApp no sistema
- Se a origem do caso de uso for a tela de Cadastrar Novo Direcionamento, o grupo recém adicionado, é selecionado como grupo do Direcionamento

### Fluxo alternativos

- O usuário não descreveu o titulo alternativo do grupo: o nome do grupo original do grupo é usado
- O usuário não é administrador do grupo selecionado: o sistema sairá do grupo e impedirá o cadastro do grupo no Sistema
