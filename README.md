# Controle de Rotas — Aço Norte Brasil

Aplicação estática para GitHub Pages, com autenticação e dados no Supabase.

Envie os arquivos desta pasta para a raiz do repositório anb-controle-rotas. Configure Pages: main, /(root). A instalação inicial e o complemento SQL devem ser executados no Supabase antes do uso.

O usuário administrador já configurado acessa com seu e-mail e senha do Supabase. Nenhuma senha está nos arquivos. A chave usada pelo navegador é exclusivamente publishable. Não coloque chaves secret ou service_role neste repositório.

O cadastro começa vazio. Cadastre os veículos e motoristas reais. Para liberar um motorista: crie seu usuário em Authentication > Users no Supabase e vincule o user_id ao driver_id correspondente na tabela anb_members, com role driver e enabled true. Não libere login de motorista como admin.

Teste com duas contas em navegadores distintos: administrador acompanha todos os lançamentos, motorista acompanha os seus. Rotas diárias abertas precisam ser finalizadas antes de fechar um ciclo. O ciclo inclui 3 abastecimentos e rotas fechadas ainda não incluídas em relatório até a data do último abastecimento.

KM/L é estimado, pois não há informação do nível do tanque. Registros vinculados a relatório ficam bloqueados para edição/exclusão até remover o relatório. Se já houver novos abastecimentos pendentes, a remoção de um relatório antigo pode ser bloqueada pelo limite de três; resolva os lançamentos pendentes primeiro.

Confirmação da senha do administrador gera uma sessão temporária usada apenas para a alteração. O servidor valida o papel e uma autenticação por senha nos últimos 120 segundos. Dados são atualizados a cada 20 segundos, quando a aba está visível e nenhum formulário de edição está aberto. Salvar depende de conexão à internet.

Esta versão não importa automaticamente dados de versões locais ou do protótipo hospedado anteriormente. Preserve esses dados até definir a importação.

Domínio personalizado será configurado depois do teste, mantendo o site principal separado.
