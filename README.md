# ulfo.it

Personal site for Federico Ulfo. Plain static HTML/CSS/JS (Start Bootstrap
"Grayscale" theme), served by **GitHub Pages**.

## Structure

```
index.html          # homepage
consulting/         # /consulting landing page
404.html            # custom not-found page
css/ js/ assets/    # theme + images
CNAME               # custom domain (ulfo.it)
.nojekyll           # serve files as-is, skip Jekyll processing
```

## Deploy

GitHub Pages serves the **root of the `gh-pages` branch**. To deploy, just push:

```
git push origin gh-pages
```

Pages rebuilds automatically within ~1 minute. No build step, no CLI, no auth.

## Custom domain

`CNAME` pins the site to `ulfo.it`. DNS must point the apex domain at GitHub
Pages:

```
A     185.199.108.153
A     185.199.109.153
A     185.199.110.153
A     185.199.111.153
AAAA  2606:50c0:8000::153
AAAA  2606:50c0:8001::153
AAAA  2606:50c0:8002::153
AAAA  2606:50c0:8003::153
```

(Or a `CNAME`/ALIAS record to `feulf.github.io` if the DNS provider supports
apex flattening.) Enable "Enforce HTTPS" in the repo's Pages settings once the
certificate is issued.

## Local preview

```
python3 -m http.server 8000
# open http://localhost:8000
```
