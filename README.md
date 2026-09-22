# Tanzimul’s portfolio

A minimal HugoBlox Academic CV website with a profile, submitted research, two engineering projects, and background.

## Local development

Install Hugo Extended 0.162.0, Go 1.25+, Node.js 22+, and pnpm 10.14.0.

```sh
pnpm install --frozen-lockfile
pnpm dev
```

Build with `pnpm build`. Generated files are in `public/`.

## Content

- `content/_index.md`: homepage sections
- `data/authors/me.yaml`: name, bio, and contact links
- `content/research/fedtransferad/index.md`: submitted paper summary
- `assets/media/authors/me.jpg`: supplied portrait, unchanged
- `static/uploads/`: supplied CV and submitted manuscript
- `config/_default/params.yaml`: appearance

FedTransferAD is explicitly described as submitted, not accepted or published. The anonymized manuscript does not provide an author list, so none is invented. Results are reported from the supplied manuscript, not independently reproduced.

The site URL is `https://mdtanzimulislamrefat.github.io/`. Use the `mdtanzimulislamrefat.github.io` repository and select GitHub Actions under Settings → Pages → Source. The included workflow builds and deploys pushes to `main`; it can also be started manually from the Actions tab. Pull requests build without deploying.

Theme: [HugoBlox Academic CV](https://github.com/HugoBlox/hugo-theme-academic-cv), using its pinned HugoBlox module. Original theme license is retained in `LICENSE.md`.
