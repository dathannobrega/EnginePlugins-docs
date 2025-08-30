# Banco de dados e backups

## Opções de banco de dados
- **SQLite**: padrão; armazena os dados localmente em `plugins/RaidEngine/raidengine.db`. Simples de configurar e ideal para servidores pequenos.
- **MySQL**: requer um servidor externo. Configure `host`, `porta`, `banco`, `usuário` e `senha` em `config.yml`. Indicado para redes ou ambientes com múltiplas instâncias.

## Migrações
- O plugin executa migrações SQL para criar/atualizar o schema.
- As migrações se adaptam ao banco escolhido quando necessário (ex.: SQLite vs MySQL).
- Antes de atualizar o plugin, faça um backup por segurança.

## Procedimentos de backup
### Backup
1. Pare o servidor ou bloqueie novas conexões.
2. Para **SQLite**, copie `raidengine.db`. Para **MySQL**, utilize `mysqldump`.
3. Armazene os arquivos em local seguro e versionado.

### Restauração
1. Pare o servidor.
2. Substitua `raidengine.db` pelo backup ou importe o `.sql` no MySQL.
3. Inicie o servidor e verifique se os dados foram carregados corretamente.

## Rotinas de manutenção e boas práticas
- Agende backups automáticos (diários ou semanais) e mantenha múltiplas versões.
- Teste periodicamente a restauração em um ambiente de staging.
- Monitore o espaço em disco e a integridade dos arquivos de banco.
- Mantenha o servidor MySQL atualizado e restrinja o acesso a credenciais.
- Utilize proteção contra quedas de energia para evitar corrupção de dados.
- Realize um backup completo antes de atualizar o plugin ou executar migrações manuais.
