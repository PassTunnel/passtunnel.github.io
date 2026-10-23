# passtunnel.github.io

Deploys <https://passtunnel.github.io/>, the PassTunnel website. GitHub serves the root of the host
only from this repository; the website itself lives in
[`site/`](https://github.com/PassTunnel/passtunnel/tree/main/site) of
[PassTunnel/passtunnel](https://github.com/PassTunnel/passtunnel) and is described in its
[docs/WEBSITE.md](https://github.com/PassTunnel/passtunnel/blob/main/docs/WEBSITE.md).

- `site.ref` holds the commit of PassTunnel/passtunnel whose `site/` is live (one full SHA). That
  repository's `site.yml` workflow updates it after every push to its `main` that touches `site/`.
- The Pages workflow (on every push to `main`, and by hand) checks out `site/` at that commit, runs
  its `scripts/check-site.sh` and deploys `site/` together with the extras here.
- To publish another commit by hand, change `site.ref` and push to `main`.

Extras kept here: `googlea85b3b6d8ba5a01d.html` (Search Console verification) and `passtunnel/`, a
redirect from the old address `/passtunnel/` to `/` that keeps the `#section`. An extra never
replaces a file of `site/`; the build fails instead.
