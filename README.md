# Sunday Heroes OnDisplay — Releases

Ce dépôt est le **miroir public des versions** de Sunday Heroes OnDisplay, une application de bureau (macOS / Windows) qui génère des vidéos de présentation d'équipe pour les clubs de basket amateur.

Le code source de l'application est privé. Ce dépôt ne sert qu'à distribuer les binaires et leurs sommes de contrôle.

## Télécharger

→ Page officielle : <https://sundayheroes.app/logiciels/ondisplay>

Les binaires sont publiés dans la section [Releases](../../releases/latest).

## Convention de nommage des assets

```
ondisplay-<version>-<os>-<arch>.<ext>
```

Exemples :

- `ondisplay-1.0.0-macos-arm64.dmg`
- `ondisplay-1.0.0-macos-x64.dmg`
- `ondisplay-1.0.0-windows-x64.exe`

Chaque release inclut également un fichier `SHA256SUMS`.

## Statut de signature

| Version | macOS | Windows |
| ------- | ----- | ------- |
| `0.1.x` | Signature **ad-hoc** (build développeur, non notarisé) | — |
| À venir | Notarisée par Apple (Developer ID) | Authenticode |

À partir d'une release ultérieure, les binaires macOS seront notarisés par Apple et les binaires Windows signés avec un certificat Authenticode. Pour les versions `0.1.x`, suivez les instructions ci-dessous à la première ouverture.

## À la première ouverture sur macOS (versions `0.1.x`)

Comme l'application n'est pas encore notarisée, macOS Gatekeeper bloquera son lancement par défaut. Deux options :

**Option 1 — clic droit "Ouvrir"**

1. Glissez `Sunday Heroes OnDisplay.app` dans `/Applications`.
2. Faites un clic droit sur l'icône → **Ouvrir**.
3. macOS affiche un avertissement avec un bouton **Ouvrir** ; cliquez dessus.
4. L'application est désormais autorisée pour les lancements suivants.

**Option 2 — Réglages système**

1. Tentez de lancer l'application normalement (le lancement sera bloqué).
2. Ouvrez **Réglages système → Confidentialité et sécurité**.
3. Tout en bas, cliquez sur **Ouvrir quand même** à côté du message concernant Sunday Heroes OnDisplay.

## Vérifier l'intégrité d'un téléchargement

Chaque release inclut un fichier `SHA256SUMS`.

**macOS**

```sh
shasum -a 256 -c SHA256SUMS --ignore-missing
```

**Windows (PowerShell)**

```powershell
Get-FileHash .\ondisplay-<version>-windows-x64.exe -Algorithm SHA256
```

Comparez la valeur renvoyée à celle attendue dans `SHA256SUMS`.

## Support

Pour signaler un bug ou poser une question, passez par le site : <https://sundayheroes.app>.

Les *Issues* et *Discussions* sont désactivées sur ce dépôt — il n'est utilisé que pour la distribution.
