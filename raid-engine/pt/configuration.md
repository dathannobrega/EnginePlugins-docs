# Configuração

## Administradores

### `config.yml`
O arquivo define parâmetros globais do plugin e é gerado na pasta de dados
(`plugins/RaidEngine`). Ajuste nele:

- `raidengine.locale`: código do idioma padrão (igual ao arquivo em `plugins/RaidEngine/lang`, ex.: `pt_BR`).
- `raidengine.worlds_enabled`: mundos onde claims são permitidos.
- `raidengine.database`: tipo (`sqlite` ou `mysql`), host, usuário e senha.
- Demais seções como `claim`, `clan` e `upgrades` para regras específicas.
- Horários e regras de raid e guerra ficam em `raid.*` e `war.*`.

### Perfis (descontinuado)
Builds antigos suportavam perfis de configuração. A versão atual consolida as
configurações em um único `config.yml`. A chave `raidengine.profile` é ignorada.

### Arquivos de idioma (`plugins/RaidEngine/lang/*.yml`)
Personalize todos os textos editando arquivos como `pt_BR.yml` ou `en_US.yml` em `plugins/RaidEngine/lang`. Suporta cores Bukkit/MiniMessage e placeholders como `%amount%`.

Os textos aceitam cores do Bukkit/MiniMessage e placeholders como `%amount%`.
Consulte o [guia de mensagens](messages.md) para detalhes sobre estrutura,
cores e como adicionar novos idiomas.

### Conexão SQL (`HikariConfigFactory`)
A classe cria o `HikariConfig` com base em `config.yml`, permitindo usar
SQLite ou conectar a um servidor MySQL. Garanta que `raidengine.database`
possua os dados corretos para o tipo escolhido.

### Migrações (`SchemaMigrator`)
Durante a inicialização, o plugin converte o arquivo de esquema SQL para o
formato esperado pelo banco definido. O `SchemaMigrator` troca, por exemplo,
`AUTOINCREMENT` por `AUTO_INCREMENT` ao usar MySQL.

## Jogadores
As mensagens podem ser traduzidas conforme o seu idioma. Peça à staff para ajustar os arquivos em `plugins/RaidEngine/lang/` ou alterar `raidengine.locale` no `config.yml`.
