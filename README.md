# Lumen Harbor Insurance (Fictional Demo)

A one-page website for a **fictional** insurance company, built as a portfolio project to show an AI risk assessment agent made with Microsoft Copilot Studio.

> **Lumen Harbor Insurance is not a real company.** It is not an insurer, agency, or broker, it is not licensed anywhere, and it sells no policies. Nothing on the site or from the agent is insurance, legal, financial, or risk advice. Any resemblance to a real company is a coincidence.

## What is in this repo

| File | Purpose |
|---|---|
| `index.html` | The whole site: HTML, CSS, and a small amount of JavaScript |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |
| `README.md` | This file |

No build step and no dependencies. Fonts load from Google Fonts.

## Connect your Copilot Studio agent

1. In Copilot Studio, open your agent and go to **Channels**.
2. Open the **Demo website** or **Custom website** channel and copy the link, or the `src` address from the iframe snippet.
3. In `index.html`, find this line near the bottom and paste the address between the quotes:
   ```js
   const AGENT_EMBED_URL = "";
   ```
4. Commit the change and reload the page. Click **Talk to the risk agent** to open the chat.

Until you add the address, the chat panel shows setup instructions instead of the agent.

### If the chat shows blank or "refused to connect"
- Publish the agent again after any change.
- For a public site, the agent needs authentication set to **No authentication** (Settings, then Security). Otherwise visitors will be asked to sign in.
- If the Demo website link will not load inside an iframe, use the Custom website channel's embed snippet, or link to the demo page from the button instead of embedding it.

## Publish on GitHub Pages

1. Create a new repository on GitHub, for example `lumen-harbor-demo`.
2. Upload all files from this folder (drag them into the repo page, or use `git push`).
3. Go to **Settings, then Pages**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose `main` and `/ (root)`, and save.
5. After a minute, your site is live at `https://<your-username>.github.io/lumen-harbor-demo/`.

## Customizing
- **Welcome audio:** edit `WELCOME_TEXT` in the script. It uses the browser's built-in speech, so there are no audio files.
- **Colors:** change the variables at the top of the stylesheet (`--ink`, `--teal`, `--beacon`, and so on).
- **Copy:** every word is in `index.html`. Keep the fictional-company notices in the top banner, the FAQ, and the footer.

## Notes
- Each conversation with the agent uses Copilot Credits. For a public link, set a spending limit in your billing settings.
- Keep the knowledge file and agent free of anything confidential, since visitors can surface its content.
- Do not add a real company's name, logo, or trademarks.
