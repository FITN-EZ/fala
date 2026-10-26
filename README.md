# Fala: put it on your phone

It's a web app (PWA). Host the folder anywhere with HTTPS, open it on your phone, and add it to your home screen. It then runs full-screen with its own icon and works offline.

## 1. Host it (GitHub Pages, ~3 min)
1. github.com > New repository > name it `fala` > Public > Create.
2. "uploading an existing file" > drag in everything in this folder > Commit.
3. Settings > Pages > Source: Deploy from a branch > Branch: main, / (root) > Save.
4. After about a minute your app is at https://YOUR-USERNAME.github.io/fala/

## 2. Install it
- iPhone (Safari only): open the link > Share > Add to Home Screen.
- Android (Chrome): open the link > menu (three dots) > Add to Home screen / Install app.

## 3. Turn on AI features
Progresso > Settings > paste an Anthropic API key (console.anthropic.com). It is stored only on your phone.
Use a separate key with a low monthly spend limit.

## Updating
Replace index.html in the repo. The app picks up the new version next time it opens online.
