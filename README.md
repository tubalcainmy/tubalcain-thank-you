[README.md](https://github.com/user-attachments/files/32593133/README.md)
# tubalcain-thank-you

The page installers land on after the onboarding form. One `index.html` and
an `assets/` folder of tab icons. No build step.

## Setting the plan

The page reads the installer's plan from the address. Set your onboarding
form's redirect to one of:

```
https://tubalcainmy.github.io/tubalcain-thank-you/?tier=1
https://tubalcainmy.github.io/tubalcain-thank-you/?tier=2
```

`?tier=1` is Verified Buyer and shows the upgrade section. `?tier=2` is
Package-Matched Buyer and shows a confirmation of what they get instead.
With no tier in the address the page treats them as Verified Buyer, so a
missing parameter never hides the upgrade.

Add `&name=Caleb` to greet them by name, if your form can pass the first
name into the redirect.

## Everything you edit

Only the `PAGE_CONFIG` block near the top of `index.html`:

| Field | What it does |
| --- | --- |
| `mysteryWhatsapp` | Your number, used by the upgrade and question buttons |
| `vslUrl` | The walkthrough video. Paste a YouTube, Loom or Vimeo link exactly as copied and it becomes an embedded player. Any other link becomes a "Watch" button. Empty shows the coming-soon card |
| `kitVol1Url`, `kitVol2Url` | The two Close Kit downloads |
| `loadCalculatorUrl` | The Solar Load Calculator |
| `tier1Price`, `tier2Price` | Used everywhere a price appears, including the upgrade difference |

## Updating the two Close Kit downloads

Open each existing Google Doc in Drive, choose **Manage versions** (or File,
then upload a new version), and upload the 8-Gate Edition over it. The file
ID stays the same, so the links in `PAGE_CONFIG` keep working and nothing on
this page needs changing.

## Tab icons

`assets/` holds the Tubalcain T mark as `favicon.svg`, `favicon-32.png`,
`favicon-16.png` and `apple-touch-icon.png`. Upload the whole folder
alongside `index.html`.
