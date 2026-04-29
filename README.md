# Sunday Heroes OnDisplay — Releases

Ce dépôt est le **miroir public des versions** de Sunday Heroes OnDisplay, une application de bureau (macOS / Windows) qui génère des vidéos de présentation d'équipe pour les clubs de basket amateur.

Le code source de l'application est privé. Ce dépôt ne sert qu'à distribuer les binaires signés et leurs sommes de contrôle.

## Télécharger

→ Page officielle : <https://sundayheroes.app/logiciels/ondisplay>

Les binaires sont publiés dans la section [Releases](../../releases/latest) de ce dépôt.

## Convention de nommage des assets

```
ondisplay-<version>-<os>-<arch>.<ext>
```

Exemples :

- `ondisplay-1.0.0-macos-arm64.dmg`
- `ondisplay-1.0.0-macos-x64.dmg`
- `ondisplay-1.0.0-windows-x64.exe`

Chaque release inclut également un fichier `SHA256SUMS`.

## Vérifier l'intégrité d'un téléchargement

**macOS / Linux**

```sh
shasum -a 256 -c SHA256SUMS --ignore-missing
```

**Windows (PowerShell)**

```powershell
Get-FileHash .\ondisplay-<version>-windows-x64.exe -Algorithm SHA256
```

Comparez la valeur renvoyée à celle attendue dans `SHA256SUMS`.

Sur macOS, l'application est **notarisée par Apple**. Sur Windows, elle est **signée avec un certificat Authenticode**. Si votre système d'exploitation signale un éditeur inconnu ou un binaire non signé, ne l'exécutez pas : il n'est pas authentique.

## Support

Pour signaler un bug ou poser une question, passez par le site : <https://sundayheroes.app>.

Les *Issues* et *Discussions* sont désactivées sur ce dépôt — il n'est utilisé que pour la distribution.
