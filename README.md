# Hyper India — single-folder project

All project files are in this one folder. There is no separate `public` folder.

## Render settings
- Runtime: Node
- Root Directory: leave blank when the files below are at the repository root
- Build Command: `npm install`
- Start Command: `npm start`

Upload the CONTENTS of this `Hyper-India` folder to the top level of your GitHub repository. Keep `server.js`, `package.json`, `index.html`, `style.css`, and `app.js` together.

Set these environment variables in Render (keep secrets private):
- `NODE_ENV=production`
- `SESSION_SECRET`: a long random secret
- `ADMIN_EMAIL`: your admin email
- `ADMIN_PASSWORD`: a strong unique password
- `BASE_URL=https://hyper-india.onrender.com`

Use a persistent disk for the SQLite database and session files before relying on real accounts or payouts. Demo product links use `example.com`; replace them with valid affiliate URLs from programs you are approved to use. This starter does not automatically verify partner sales or send payouts.
