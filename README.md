# Mod Installer Database

A community-built database for [**Blade & Sorcery**](https://www.nexusmods.com/bladeandsorcery) and [**Blade & Sorcery: Nomad**](https://www.nexusmods.com/bladeandsorcerynomad), **automatically populated by Mod Installer** with mod names and their corresponding Nexus Mods pages.

## Database Files

| File | Contents |
| --- | --- |
| `pcvrMods.json` | PCVR mod folder names mapped to Nexus Mods URLs |
| `nomadMods.json` | Nomad mod folder names mapped to Nexus Mods URLs |
| `lastSynced.json` | Tracks last synced mods to retrieve only newly submitted records from Firestore |

Each platform file is a JSON object where the key is a mod folder name and the value is its Nexus Mods page:

```json
{
  "!QolMenu!": "https://www.nexusmods.com/bladeandsorcery/mods/11243"
}
```

## How It Works

When mods are installed through **Mod Installer**, the installer automatically submits mod folder names and their corresponding Nexus Mods links to a Firebase Firestore database. New entries are then periodically exported to the JSON files in this repository.

## License & Attribution

This database is made available under the [Open Data Commons Attribution License (ODC-By 1.0)](https://opendatacommons.org/licenses/by/1-0/).

Any public use or redistribution of this database, or works produced from it, must provide attribution to **Bread-Hockey** in accordance with the license.

Suggested attribution:

> Mod data provided by [Bread-Hockey's Mod Installer Database](https://github.com/Bread-Hockey/ModInstallerDatabase).

Please include attribution in your project's documentation, credits, or another reasonably accessible location.

## Privacy

**The published JSON files are not user download histories.** They contain only mod identifiers and Nexus Mods URLs, not usernames, device identifiers, IP addresses, or records of which individual installed a mod.

## Notes

- **PCVR and Nomad are maintained separately** because the same mod name can refer to different Nexus Mods pages.
- Entries are community-sourced and may occasionally be missing or incorrect.
- This repository is an independent community project and is not affiliated with Nexus Mods or the developers of Blade & Sorcery.
