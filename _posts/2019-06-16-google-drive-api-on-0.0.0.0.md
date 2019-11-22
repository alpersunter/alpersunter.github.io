---
layout: post
title: Google Drive API on 0.0.0.0
subtitle: Run python http.server at localhost, not at 0.0.0.0
---

[Browser Quickstart](https://developers.google.com/drive/api/v3/quickstart/js) tutorial by Google is good, but not perfect.

## Problem?

- `python3 -m http.server 8000` by default, starts the local server at `http://0.0.0.0:8000`.

- The tutorial tells you to set **OAuth 2.0 client > Authorised JavaScript origins** to `http://localhost:8000`, which doesn't work.

- You, as a rational person, decide to set **Authorised JavaScript origins** to `http://0.0.0.0:8000` because that is the return value of `window.location.origin` in the developer console of your local server.

- And that raises the error

![Yeah Google, thanks.](https://lh3.googleusercontent.com/wsGZNpNJtrBrnnndeKlqrsr1do28aag7lSbe4TcpQnCMR5f0yN8EwjZTO70nSKRYH2ezgRk0s6oR "error message")

## Solution

- Play the game with their rules.

- Set **Authorised JavaScript origins** to `http://localhost:8000`.

- Run localserver not on `0.0.0.0` but on `localserver` by

`python3 -m http.server 8000 --bind 127.0.0.1`

## That's it!
