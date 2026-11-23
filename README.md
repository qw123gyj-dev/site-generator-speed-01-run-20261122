[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/qw123gyj-dev/site-generator-speed-01-run-20261122/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/qw123gyj-dev/site-generator-speed-01-run-20261122/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

# site-generator-speed-01-run-20261122

A faster drop-in for makefun-site 1.0.0: `solve.js` reimplements the reference
static site generator from scratch and returns byte-for-byte identical output
for every input, faster. `main.ts` is the driver the harness runs: it reads
every case from `/input/cases.json`, answers each with `run()`, and writes
`/output/answers.json`.

Speed comes from a fused single-pass Markdown renderer (no token objects,
plain runs escaped in bulk), memoised slugs, front matter parsed by scanning
line boundaries, and a template engine that renders into an array, reuses
loop scopes, and memoises includes whose result depends only on stable
values (site, tags, recent, or one post's card).
