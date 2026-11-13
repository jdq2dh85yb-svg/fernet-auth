# Auth relay (Discord login)

Discord only accepts normal HTTPS redirect addresses for this app. This page receives the Discord login
result and hands it to the launcher via `projectfernet://auth`.

1. Create a public GitHub repo (e.g. `fernet-auth`), upload `index.html`.
2. Settings > Pages > deploy from branch `main`, folder `/ (root)`.
3. Your address is `https://<your-github-name>.github.io/fernet-auth/`.
4. Discord Developer Portal > OAuth2 > Redirects: add exactly that address and Save Changes.
5. In `FernetAuth.swift` set `defaultRelayURL` to that address so your community does not have to type anything.
