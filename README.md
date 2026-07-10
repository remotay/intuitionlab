# The Intuition Lab

Machines for seeing what numbers hide — a small collection of interactive,
animated visualizations. Every figure is live: drag the gauges and watch the
physics respond.

## Visualizations

| # | Page | What it shows |
|---|------|---------------|
| 01 | [`light-clock.html`](light-clock.html) | **The Light Clock** — special-relativity time dilation. Two photon clocks tick side by side; a velocity fader slows the moving clock's ticks by the Lorentz factor, live, with a γ-vs-velocity dilation curve. |
| 02 | [`memory-ladder.html`](memory-ladder.html) | **The Memory Ladder** — memory-hierarchy latency, L1 cache to hard disk. Each runner crosses its track in exactly one access time; a logarithmic time-zoom gauge spans the 8,000,000× gap. |

`index.html` is the site shell: a sidebar that loads each visualization
(standalone HTML files) into a frame, with hash routing (`#light-clock`,
`#memory-ladder`).

## Run locally

It's a fully static site — any file server works:

```
python -m http.server 8741
```

Then open <http://localhost:8741/>.

## Deploy (Render)

Create a **Static Site** on [Render](https://render.com), point it at this
repo, leave the build command empty, and set the publish directory to `.` —
there is no build step.

## Adding a visualization

1. Drop a new standalone `your-viz.html` in the repo root.
2. In `index.html`, add a nav entry and one line to the `VIZ` map.
