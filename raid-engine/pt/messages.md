# Mensagens

Todos os textos são carregados de `plugins/RaidEngine/lang/*.yml`. Por padrão o plugin cria `en_US.yml` e `pt_BR.yml` na primeira execução. Você pode adicionar novos idiomas colocando mais arquivos `.yml` nessa pasta.

## Estrutura

Cada arquivo se chama `<locale>.yml`, onde `<locale>` é o código de idioma como `en_US` ou `pt_BR`. As chaves são organizadas em seções aninhadas:

```yml
clan:
  command:
    create:
      success: '<green>Clã criado.'
```
Use sempre recuo com **dois espaços**. Os textos podem conter:
- **Cores**: utilize tags do [MiniMessage](https://docs.adventure.kyori.net/minimessage/format.html) como `<red>` e `<green>`.
- **Placeholders**: mantenha intactos marcadores como `%amount%`, `%player%` ou `{clan}`; eles são substituídos automaticamente.

Strings com dois pontos, símbolos especiais ou cores devem ser envolvidas em aspas simples (`'texto'`).

## Idioma padrão (`raidengine.locale`)

No arquivo `config.yml`, escolha o idioma carregado por padrão:

```yml
raidengine:
  locale: pt_BR
```

Após salvar, reinicie o servidor ou use `/raidadmin reload`.

## Adicionando novos idiomas

1. Copie um arquivo existente na pasta `lang`, por exemplo:
   ```bash
   cp plugins/RaidEngine/lang/en_US.yml plugins/RaidEngine/lang/es_ES.yml
   ```
2. Traduza cada entrada, preservando chaves, cores e placeholders.
3. Defina `raidengine.locale` para o novo código (`es_ES`).
4. Reinicie o servidor ou use `/raidadmin reload`.

## Exemplo de edição

Para alterar a mensagem de depósito no banco do clã:

```yml
clan:
  bank:
    deposit_success: '<green>Depósito realizado com sucesso!'
```

## Cuidados e formatação

- Não utilize tabulações; apenas espaços.
- Cores e formatação devem seguir o padrão MiniMessage.
- Verifique sempre placeholders e chaves antes de salvar.

## Dicas de backup

Antes de modificar qualquer arquivo:

```bash
cp plugins/RaidEngine/lang/pt_BR.yml plugins/RaidEngine/lang/pt_BR.yml.bak
```

Manter uma cópia ou versionar os arquivos facilita a restauração em caso de erro.

## Exemplo de uso de placeholders

Os placeholders do RaidEngine podem ser utilizados diretamente nas mensagens. Exemplo:

```yml
placeholders:
  example: "<yellow>Clã %raidengine_f_name% [%raidengine_f_tag%]: DTR %raidengine_f_dtr% - %raidengine_f_state% - Online %raidengine_f_online% - Escudo %raidengine_f_shield_timeleft%"
```
