# Examples

This section shows real-world, plain-English examples of how an AI agent uses `AGENTS.md` to manage Minecraft Bedrock addons.

These are **not scripts** — they are *intent-driven commands* issued to an AI running in the Bedrock server directory.

---

## Install Everything

**User says:**

> Enable all addons in the folder `mods/`

**AI does:**

1. Scans `mods/` for `.mcaddon` and `.mcpack`
2. Determines pack types (behavior/resource)
3. Extracts them safely
4. Fixes unicode folder names
5. Installs into correct directories
6. Updates world pack JSON files
7. Reports what was enabled

---

## Install One Addon

**User says:**

> Install `Create Lite.mcaddon`

**AI does:**

* Locates the archive
* Extracts BP/RP correctly
* Installs only the detected packs
* Enables them for the selected world

---

## Disable an Addon

**User says:**

> Disable Create Lite addon

**AI does:**

* Finds matching packs by name
* Removes their UUIDs from world JSON files
* Leaves files installed but inactive
* Confirms what was disabled

---

## Remove an Addon Completely

**User says:**

> Remove broken weapon pack

**AI does:**

* Identifies matching pack folders
* Disables them in all worlds
* Deletes addon folders
* Verifies no UUIDs remain

---

## Diagnose a Problem

**User says:**

> Something is wrong with this addon

**AI does:**

* Validates manifests
* Checks missing files
* Detects wrong pack types
* Explains the issue clearly
* Suggests how to fix it

---

## Multi-World Control

**User says:**

> Enable all mods for CreativeWorld only

**AI does:**

* Leaves other worlds untouched
* Updates only the specified world configs

---

## Idempotent Execution

Running the same command twice produces the same result:

* No duplicate UUIDs
* No reinstallation
* No corruption
