
# HeadSteal (Paper/Spigot 1.21.x)

**What it does**
- On player-vs-player death: drops the victim's player head and bans the victim.
- When that exact head is placed: unbans (revives) the victim and consumes the head (configurable).

## Build (Locally)
1. Install Java 21 (required for MC 1.21.x).
2. Run:
   ```bash
   ./gradlew build
   ```
   The JAR will be at `build/libs/HeadSteal-1.0.0.jar`.

3. Copy the JAR to your server's `plugins/` directory and restart.

## Notes
- Only **player kills** trigger ban/drop if `killerMustBePlayer: true` (default).
- Players with `headsteal.exempt` (ops by default) are not banned on death.
- Set `restrictPlacement: true` if you want only players with `headsteal.place` to be able to revive.
