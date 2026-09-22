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

The default URL is the root site at `https://tanzimul3islam.github.io/`. For GitHub Pages hosting at this address, use the `tanzimul3islam.github.io` repository. Set `baseURL` in `config/_default/hugo.yaml` for another address. A manual GitHub Pages workflow is included; enable Pages with GitHub Actions, then run it when ready. Nothing has been published automatically.

Theme: [HugoBlox Academic CV](https://github.com/HugoBlox/hugo-theme-academic-cv), using its pinned HugoBlox module. Original theme license is retained in `LICENSE.md`.
