# Valentine

A single-page “Will you be my Valentine?” ask page. Mobile-friendly, with a dodge-the-No-button game and a “Yes” modal (optional redirect link).

## Customizing the page

Edit the **“Customize these”** block at the top of the `<script>` in `index.html`. Change these variables:

| Variable | What it does |
|----------|----------------|
| `herName` | If set, headline becomes *“{herName}, will you be my Valentine? 💘”*; if empty, *“Will you be my Valentine? 💘”* |
| `fromName` | Subtext ends with *“— {fromName}”* (e.g. *“— Chase”*) |
| `afterYesMessage` | The message shown in the modal after they click Yes (or after 6 dodges). |
| `redirectUrlAfterYes` | If set, the modal shows a **“Go to your surprise 💝”** link that opens this URL in a new tab. If empty, the modal shows a **Close** button. |

**Exact lines to edit** (around lines 187–190 in `index.html`):

```javascript
var herName = '';                    // e.g. 'Sarah' → "Sarah, will you be my Valentine? 💘"
var fromName = 'Chase';              // subtext ends with "— {fromName}"
var afterYesMessage = "Now you're stuck with me. Happy Valentine's Day 💘";
var redirectUrlAfterYes = '';        // if set, modal shows "Go to your surprise 💝" link (new tab); else "Close" button
```

Examples:

- `herName = 'Sarah';` → headline: *“Sarah, will you be my Valentine? 💘”*
- `fromName = 'Alex';` → subtext ends with *“— Alex”*
- `redirectUrlAfterYes = 'https://example.com/surprise';` → modal has *“Go to your surprise 💝”* opening that URL in a new tab.

---

## GitHub Pages setup

1. Open your repo on GitHub.
2. Go to **Settings** → **Pages** (left sidebar).
3. Under **Build and deployment**:
   - **Source:** *Deploy from a branch*
   - **Branch:** `main`
   - **Folder:** */(root)*
4. Click **Save**.

**Site URL:**  
`https://USERNAME.github.io/REPO/`  
(Replace `USERNAME` with your GitHub username and `REPO` with this repo’s name, e.g. `https://jane.github.io/Valentine/`.)

It can take **1–2 minutes** for the site to go live after saving. If you see a 404, wait a bit and refresh.
