# passtunnel.github.io

The root of <https://passtunnel.github.io/>: a redirect to the PassTunnel website at
[/passtunnel/](https://passtunnel.github.io/passtunnel/), plus `robots.txt` and `llms.txt`.
The website itself lives in [`site/`](https://github.com/PassTunnel/passtunnel/tree/main/site) of
[PassTunnel/passtunnel](https://github.com/PassTunnel/passtunnel). `/llms.txt` is not kept here: the
Pages workflow fetches `site/llms.txt` from `main` of that repository on every deploy and once a day.
