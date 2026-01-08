# World Pack Enabling

## World Configuration Files

Addon activation is controlled per world via:

* `world_behavior_packs.json`
* `world_resource_packs.json`

Each file contains a JSON array of enabled pack entries.

## Entry Format

```json
{
  "pack_id": "uuid-string",
  "version": [major, minor, patch]
}
```

## Enabling Packs

When enabling a pack for a world, the AI must:

1. Read the existing configuration file
2. Verify whether the pack UUID already exists
3. Add the pack only if it is not already present
4. Preserve valid JSON formatting

## Disabling Packs

Disabling a pack means:

* Removing the UUID entry from the world configuration file
* Leaving the pack installed on disk

This allows safe re-enabling later.

## Removing Packs

Removing a pack may involve:

* Disabling it for all worlds
* Optionally deleting its directory (only if allowed by AGENTS.md)

The AI must clearly distinguish between:

* **Enable** (world-level)
* **Disable** (world-level)
* **Remove** (server-level)
* **Delete** (filesystem-level)

## Duplicate Prevention

The AI must ensure:

* No duplicate UUID entries exist
* Vanilla pack entries are preserved
