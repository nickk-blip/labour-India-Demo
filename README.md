# Labour India (demo)

A clickable demo of the Labour India worker app and employer app. It is a static website: plain HTML and JavaScript, with no build step and no server code.

All names, wages and ratings are sample data. Nothing typed into the demo is saved or sent anywhere.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The page that loads and runs both apps |
| `Main.dc.html` | Worker app screens and logic |
| `Factory.dc.html` | Employer app screens and logic |
| `manifest.json`, `icon.svg` | Name and icon for "Add to Home screen" |
| `render.yaml` | Optional Render Blueprint for a static site |

## Run it on your computer

Opening `index.html` by double-click will not work, because the page loads the other files over HTTP. Start a small local server instead:

```
python3 -m http.server 8000
```

Then open http://localhost:8000

## Deploy on Render

1. Push this folder to a GitHub repository.
2. In Render, choose **New** > **Static Site** and connect that repository.
3. Leave **Build Command** empty.
4. Set **Publish Directory** to `.`
5. Choose **Create Static Site**. Render gives you a link ending in `.onrender.com`.

Every push to the repository redeploys the site. To take the demo offline, suspend or delete the static site in Render.

## Use it on a phone

Open the Render link in Chrome on Android, then choose **Add to Home screen** from the menu. It opens full screen like an app.

- Worker app: the main link
- Employer app: add `#employer` to the end of the link, or tap **Employer login** on the first screen
