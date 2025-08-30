# GUI

## Guidelines de cores e ícones

- Ícones comuns são centralizados no `MenuTheme`.
- **Voltar:** seta (`Material.ARROW`) com texto `gui.back`.
- **Confirmar:** lã verde (`Material.GREEN_WOOL`) com texto `gui.confirm`.
- **Próximo:** seta (`Material.ARROW`) com texto `gui.next` para avançar páginas ou níveis.
- Use verde para ações positivas e vermelho para cancelar.

## Para jogadores

### ClaimConfirmMenu
- **Como abrir:** execute `/claim` após pré-visualizar a área a ser reivindicada.
- **Principais ações:** confirmar ou cancelar a criação do claim.

### ClanBankConfirmMenu
- **Como abrir:** `/clan bank deposit <valor>` ou `/clan bank withdraw <valor>`.
- **Principais ações:** confirmar depósitos ou saques do banco do clã.

### ClanBankMenu
- **Como abrir:** botão "Banco" dentro do `ClanInfoMenu`.
- **Principais ações:** exibir saldo, depositar, sacar e visualizar últimas transações.

### ClanInfoMenu
- **Como abrir:** `/clan info`.
- **Principais ações:** visualizar saldo do clã e acessar menus de membros ou permissões.

### ClanMembersMenu
- **Como abrir:** botão "Membros" dentro do `ClanInfoMenu`.
- **Principais ações:** ver integrantes e promover/rebaixar funções.

### ClanPermissionsMenu
- **Como abrir:** botão "Permissões" dentro do `ClanInfoMenu` (somente líder dentro do claim).
- **Principais ações:** alternar flags de construção, uso, baús, PVP e outros acessos de visitantes.

 

## Para administradores
- Textos de botões, títulos e mensagens são personalizáveis em `plugins/RaidEngine/lang/<locale>.yml`.
- Ajuste o idioma padrão e opções gerais em `config.yml` (`raidengine.locale`).
- Custos e disponibilidade de upgrades ficam em `config.yml` na seção `upgrades`.
 

## Dicas de uso
- Utilize o item de seta "Voltar" para retornar rapidamente ao menu anterior.
- Defina permissões de claim com cuidado para evitar acesso indesejado ao território.
