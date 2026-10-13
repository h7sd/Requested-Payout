# Requested Payout for Scam With Your Friends

Successful credit-card scams pay the original reward plus your stated price. Gift-card scams pay the stated price after correct fictional-code verification. Install on the multiplayer host. No runtime download is needed.

Download **Requested-Payout-1.2.0.zip** from [Releases](https://github.com/h7sd/Requested-Payout/releases/latest). Its ZIP contains only root-level DLLs and one optional post-install script. The shared library is installed to BepInEx/core; plugin DLLs go to BepInEx/plugins.

The stock launcher offers setup steps only for catalogue entries. For a direct-URL installation, extract the ZIP and run its root script yourself with `-GameDir "C:\Path\To\Game"` while the game is closed.

[Source and build scripts](https://github.com/h7sd/scam-with-your-friends-mods/tree/edacd91f088f9601b278bdd4cff7e172e09c1ae3/payout-mod), [package instructions](https://github.com/h7sd/scam-with-your-friends-mods/blob/edacd91f088f9601b278bdd4cff7e172e09c1ae3/catalogue/README.md). Source revision: `edacd91f088f9601b278bdd4cff7e172e09c1ae3`. Licence notices are included in the post-install script.

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
    },
    {
      "fileName": "ScamWYF.Modding.Core.dll",
      "folder": "core",
      "expectsPluginAttribute": false
    }
  ],
  "postInstall": [
    {
      "script": "post-install-requested-payout.ps1",
      "description": "Checks the installed mod and displays its payout rules and multiplayer host instructions. Skipping does not affect the mod; no additional setup or downloads are required."
    }
  ]
}
```

Unofficial community mod, unaffiliated with the game developer or the external service.
