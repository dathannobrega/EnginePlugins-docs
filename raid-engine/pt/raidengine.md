# RaidEngine
![Engine Plugins - Banner](../assets/images/banners/banner-home.png)
## Instalação
1. Baixe o arquivo `.jar` do RaidEngine.
2. Coloque-o na pasta `plugins` do seu servidor Spigot ou Paper.
3. Reinicie o servidor e verifique se o plugin foi carregado corretamente.

## Visão Geral
O RaidEngine introduz mecânicas de clãs, territórios e guerras. O objetivo é competir por áreas do mapa e fortalecer seu clã para dominar o servidor.

## Progressão de Clãs
- Obtenha recursos para ganhar experiência e subir de nível.
- Desbloqueie upgrades e bônus para os membros ao evoluir.

## Dicas
- Coopere com os membros do clã para evoluir mais rápido.
- Use o mapa para planejar ataques e defesas.

## Fluxos de Jogo
### Criar Clã
1. Use `/clan create <nome>` para fundar um novo clã.
2. Convide amigos com `/clan invite <jogador>`.
3. Defina a base e organize as funções dos membros.

### Reivindicar Território
1. Vá até a área desejada.
2. Execute `/claim` para confirmar a área selecionada para o seu clã.
3. Proteja a região contra invasores.

### Janelas de Guerra
- Raids ocorrem apenas nos horários configurados.
- Líderes declaram ou aceitam guerras; verifique as regras locais com a staff.

## Administradores

### Dependências
- Servidor Spigot ou Paper recente.
- Plugin de economia compatível (ex.: Vault).
- Banco de dados configurado, se necessário, para persistência.

### Permissões Globais
- `raidengine.admin` para acesso completo (grupo definido no `plugin.yml`).
- `raidadmin.admin` para usar o comando de administração.

### Comandos Principais
- `/raidadmin reload` para recarregar configurações e mensagens.
- `/raidadmin give <jogador> claim_core <qtd>` para conceder Núcleos de Claim.
- `/raidadmin world <enable|disable|list>` para gerenciar mundos onde os claims valem.

### Guias gerais
- [Banco de dados e backups](data.md)
- [Scoreboard](scoreboard.md)
- [Mensagens e idiomas](messages.md)

