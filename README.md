# Ali Arbabian Site

Quarto personal site with a Tufte-inspired academic style and GitHub Pages deployment.

## Local Development

Install Quarto, then run:

```sh
quarto preview
```

Render the static site with:

```sh
quarto render
```

## GitHub Pages

This repository is configured to publish from GitHub Actions. After pushing to GitHub:

1. Open the repository settings.
2. Go to Pages.
3. Set the source to GitHub Actions.
4. Push to `main` and check the Pages workflow.

## Custom Domain

This site is configured for `https://aliarbabian.com`.

In your domain registrar DNS settings, point the apex domain to GitHub Pages:

```txt
A     @     185.199.108.153
A     @     185.199.109.153
A     @     185.199.110.153
A     @     185.199.111.153
AAAA  @     2606:50c0:8000::153
AAAA  @     2606:50c0:8001::153
AAAA  @     2606:50c0:8002::153
AAAA  @     2606:50c0:8003::153
```

For `www.aliarbabian.com`, add:

```txt
CNAME  www  <your-github-username>.github.io
```

After the Pages deployment succeeds, open the repository Pages settings, set the custom domain to `aliarbabian.com`, and enable HTTPS once GitHub finishes DNS validation.
