# API

## Get a player's clan

```java
import java.util.UUID;
import com.datan.raidengine.RaidEngine;
import com.datan.raidengine.api.model.Clan;

UUID playerId = player.getUniqueId();
RaidEngine.api().getClanByPlayer(playerId).ifPresent(clan -> {
    String name = clan.name();
    // do something with the clan
});
```

## Register core damage

```java
import org.bukkit.Location;
import com.datan.raidengine.RaidEngine;

Location loc = player.getLocation();
RaidEngine.api().getClaimAt(loc).ifPresent(claim -> {
    boolean destroyed = RaidEngine.api().damageCore(claim.id(), 25);
    if (destroyed) {
        // core destroyed
    }
});
```

## For developers

### Dependencies

```xml
<dependency>
    <groupId>com.datan</groupId>
    <artifactId>raidengine</artifactId>
    <version>0.1.0-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

### Using `RaidEngine.api()`

```java
import com.datan.raidengine.api.RaidEngineAPI;
import com.datan.raidengine.RaidEngine;

RaidEngineAPI api = RaidEngine.api();
```
