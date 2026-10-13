# Requested Payout for Scam With Your Friends

Setup installs the required shared Core 1.0.4 when missing. Skipping setup requires Core 1.0.4 or newer already installed in BepInEx/core. Credit-card payouts add your stated price to the original reward; gift-card payouts use your stated price after correct fictional-code verification. Install on the multiplayer host.

Download **Requested-Payout-1.2.1.zip** from [Releases](https://github.com/h7sd/Requested-Payout/releases/latest). The ZIP has exactly two root files:

- `ScamWYF.RequestedPayout.dll`
- `post-install-requested-payout.ps1`

Package 1.2.1 changes distribution only; the DLL version remains 1.2.0. There is no launcher, dependency DLL or runtime inside this mod ZIP. Required dependencies are downloaded separately by setup using fixed HTTPS URLs and SHA-256 checks. Licence notices are included in the script.

The stock launcher offers setup only for catalogue installations. If using a direct ZIP URL, extract it and run `post-install-requested-payout.ps1 -GameDir "C:\Path\To\Game"` with the game closed.

[Source](https://github.com/h7sd/scam-with-your-friends-mods/tree/b1732624d24d933de3af0a4a09ef74af90a9f461/payout-mod) · [Package and dependency instructions](https://github.com/h7sd/scam-with-your-friends-mods/blob/b1732624d24d933de3af0a4a09ef74af90a9f461/catalogue/README.md)

Catalogue entry:

```json
{
  "owner": "h7sd",
  "repo": "Requested-Payout",
  "displayName": "Requested Payout",
  "summary": "Remembers the price stated during a call. Successful credit-card scams add it to the original reward; gift-card scams pay that price after the correct fictional code is verified. In multiplayer, install on the host.",
  "files": [
    {
      "fileName": "ScamWYF.RequestedPayout.dll",
      "folder": "plugins",
      "expectsPluginAttribute": true
    }
  ],
  "postInstall": [
    {
      "script": "post-install-requested-payout.ps1",
      "description": "Installs the required shared Core DLL from a pinned separate package and displays payout rules. If skipped, Core 1.0.4 or newer must already be installed in BepInEx/core for the mod to work."
    }
  ]
}
```
