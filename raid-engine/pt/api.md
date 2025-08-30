# API

## Obter clã de um jogador

```java
import java.util.UUID;
import com.datan.raidengine.RaidEngine;
import com.datan.raidengine.api.model.Clan;

UUID playerId = player.getUniqueId();
RaidEngine.api().getClanByPlayer(playerId).ifPresent(clan -> {
    String nome = clan.name();
    // faça algo com o clã
});
```

## Registrar dano ao núcleo

```java
import org.bukkit.Location;
import com.datan.raidengine.RaidEngine;

Location loc = player.getLocation();
RaidEngine.api().getClaimAt(loc).ifPresent(claim -> {
    boolean destruido = RaidEngine.api().damageCore(claim.id(), 25);
    if (destruido) {
        // núcleo destruído
    }
});
```

## Para desenvolvedores

### Dependências

```xml
<dependency>
    <groupId>com.datan</groupId>
    <artifactId>raidengine</artifactId>
    <version>0.1.0-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

### Uso do `RaidEngine.api()`

```java
import com.datan.raidengine.api.RaidEngineAPI;
import com.datan.raidengine.RaidEngine;

RaidEngineAPI api = RaidEngine.api();
```
