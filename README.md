# Island Platoon Marathon — live loop feed

Streams the finished Island Platoon episodes 1–3 loop to the
"Island Platoon Marathon — Episodes 1-3 on Loop" YouTube stream, on repeat.

## How to start
Actions tab → "Island Platoon Marathon loop" → Run workflow.
The runner downloads the loop file from this repo's `loop-v1` release and
pushes it to YouTube until the run ends.

## How to stop
Actions tab → the running workflow run → Cancel run. The stream ends when
the feed stops.

## Limits (GitHub's, not ours)
- One run lasts at most 6 hours (GitHub's job cap). Restart it with
  Run workflow when it ends if the marathon should continue.
- Actions minutes are metered on the account's plan, so a marathon
  running many hours consumes plan minutes.

## Setup (already done)
- `YT_STREAM_KEY` repo secret: the stream key for the Marathon stream.
  It lives only as a repo secret, never in this repo's files.
- Loop file: `island_platoon_loop_ep1-3.mp4` (episodes 1, 2, 3 in order,
  ~304s) attached to the `loop-v1` release.
