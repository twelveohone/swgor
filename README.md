# Outer Rim 4K UI

Download [OuterRim-4K-UI.zip](https://github.com/twelveohone/swgor/releases/latest/download/OuterRim-4K-UI.zip).

This is the Outer Rim interface scaled for a 3840×2160 screen. It belongs in an Outer Rim install that uses `SwgClient_r.exe`. It is not for SWG Uprising or any other client.

Quit the game before you copy these in.

## Where the files go

Unzip the download. You will see two things:

- a folder named `ui`
- a file at `string\en\ui_charsheet.stf`

Put them in the Outer Rim game folder, the same folder that contains `SwgClient_r.exe`.

1. Copy the `ui` folder into the game folder. If that folder already has a `ui` folder, let these files overwrite the ones with the same names. Example: `D:\Games\SWG Outer Rim\ui`.
2. Copy `ui_charsheet.stf` into the game’s `string\en` folder. Example: `D:\Games\SWG Outer Rim\string\en\ui_charsheet.stf`. Create `string\en` if it is not there.

Leave both of them as loose files. Do not pack them into a `.tre` archive. The game reads these loose files in place of the copies stored in the archives.

## Resolution

In the game folder, open `options.cfg` and set:

```
screenWidth=3840
screenHeight=2160
```

Start the game after the files are in place. A restart is required any time these files change.

## Chat text

The chat window’s font size is saved by the game itself. It is not in this download. After you log in, set the chat font size to 22.
