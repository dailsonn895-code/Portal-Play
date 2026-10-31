# Portal-Play
Para facilitar a vida dos porteiros

## Outras Chaves (atualização)

- Aba **Outras Chaves** independente de Jogos, com catálogo inicial de 20 chaves.
- Retiradas por morador consultam o mesmo cadastro de moradores do Portal Play; retiradas internas usam funcionário cadastrado ou nome digitado.
- Administrador edita lista de chaves e funcionários em **Sistema > Administração de Outras Chaves**.
- Retiradas/devoluções em tempo real usam a coleção Firestore `outrasChavesRetiradas`.
- Configuração compartilhada usa o documento `configuracoes/outrasChaves`.
- **Importante:** as regras do Firestore devem autorizar usuários legítimos a ler e registrar os novos dados e restringir edição de configuração a administradores. A interface sozinha NÃO é um mecanismo de controle de acesso. Confira as regras de segurança atuais antes de publicar. O fluxo de login legado do projeto utiliza autenticação própria e merece reforço em uma etapa de segurança.
- Não foram aplicadas regras nem escritos dados remotamente; o catálogo inicial aparece no app mesmo antes de salvar a configuração. Salve no admin após a publicação para persistir o catálogo.
