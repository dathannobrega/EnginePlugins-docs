# Sistema de Claims

## Para jogadores

### Craft
- Obtenha o **Núcleo de Claim** por meio da receita do servidor (lodestone + obsidiana + netherite) ou peça a um admin com `/raidadmin give`.

### Pré-visualização
- Tente posicionar o núcleo para pré-visualizar a área. Se estiver válido (sem colisões e respeitando a altura mínima relativa), você verá partículas e uma bossbar.
- Confirme com `/claim` para criar o território.

### Confirmação
- Use `/claim` para abrir o menu de confirmação. Ao confirmar, o banco do clã é debitado (`clan.bank.claim_place_cost`).

### Upgrades
- O raio e o HP do núcleo escalam conforme a configuração e a progressão do clã.

### Dicas de defesa
- Posicione o núcleo protegido e preferencialmente no centro da base para dificultar ataques.
- Mantenha espaço livre ao redor para evitar que inimigos usem o terreno como cobertura.
- Aproveite o recurso `claim.anti_cover` para impedir construções que protejam demais o núcleo.

### Erros comuns ao posicionar o núcleo
- Tentar colocar o núcleo muito baixo ou alto em relação ao terreno, violando `claim.min_relative_height`.
- Encostar o núcleo em outro claim existente.
- Não possuir dinheiro suficiente no banco do clã para o custo de colocação.
- Esquecer de confirmar com `/claim` após a pré-visualização.

## Para administradores

### Chaves de configuração (`config.yml`)
- `worlds_enabled`: mundos onde o sistema de claim é válido.
- `preview.particles` e `preview.bossbar`: controlam efeitos de pré-visualização.
- `claim.min_relative_height` e `claim.anti_cover`: regras de posicionamento do núcleo.
- `claim.levels`: define raio e HP por nível.
- `claim.core.base_hp`: vida inicial do núcleo.
- `clan.max_claims_by_level`: limite de claims por nível de clã.
- `clan.bank.claim_place_cost`: custo para colocar o núcleo.

### Mensagens
- Personalize títulos, textos de confirmação e demais avisos nos arquivos em `plugins/RaidEngine/lang/` (por exemplo, `pt_BR.yml`).

### Permissões
- O comando `/claim` é liberado para todos. Comandos administrativos, como `/raidadmin`, requerem nós específicos (`raidadmin.admin`, `raidadmin.give`, etc.) conforme definidos em `plugin.yml`.
