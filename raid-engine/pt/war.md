# Sistema de Guerra e Raid

## Fluxo Completo
1. **Declarar guerra** – o líder usa `/f war declare <clã>` e paga o custo definido. A guerra só inicia se ambos os clãs estiverem sem escudo e dentro da janela configurada.
2. **Janela de raid** – ataques só são válidos entre `raid.start_time` e `raid.end_time`. Fora desse período, TNT não causa dano e novas guerras não começam.
3. **Dano ao núcleo** – durante a guerra, explodir TNT sobre o Núcleo inimigo remove `raid.tnt.damage` de HP. O `RaidStateService` gerencia o HP e o tempo do raid.
4. **Estado RAIDED** – ao chegar a 0 HP, o claim entra em estado **RAIDED** por `raid.raided_duration_minutes` minutos, relaxando proteções até o fim do timer.

## Jogadores
### Como atacar
- Declare guerra e aguarde a janela de raid.
- Use TNT no Núcleo inimigo para causar dano e reduzir o HP.
- Quando o HP chegar a zero, aproveite o estado RAIDED para saquear.

### Como defender
- Mantenha defensores online para impedir ativação do escudo offline.
- Reforce o Núcleo e repare danos antes que o HP zere.
- Utilize aliados: apenas inimigos declarados podem causar dano ao Núcleo.

### Avisos de raid
- Ao ter o Núcleo atacado, todos recebem bossbar com HP e tempo restante.
- Membros e aliados são alertados no chat e com sons de campainha.
- Opcionalmente, o servidor pode enviar alertas ao Discord quando a raid inicia e termina.

## Administradores
### Configuração de escudo offline
- `raidengine.war.offline_shield.enabled`: ativa o escudo automático.
- `min_online_defenders`: mínimo de membros online para permitir ataque.
- `cooldown_minutes`: tempo de recarga após o escudo ser usado.

### Custos
- A declaração de guerra desconta do banco do clã o valor configurado.
- Ajuste valores no bloco `clan.bank` do `config.yml` para equilibrar a economia.

### Duração
- `war.min_notice_minutes`: aviso mínimo antes do início.
- `war.duration_minutes`: tempo máximo de guerra.
- `raid.raided_duration_minutes`: quanto tempo o claim permanece RAIDED após zerar o HP.
