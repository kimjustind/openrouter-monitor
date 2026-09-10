# OpenRouter Monitor

A single HTML file that watches your OpenRouter credit balance draw down in real time.

Open `index.html` over `http://` (not `file://` — the browser blocks the cross-origin
request), paste an API key, and it polls `/credits` on an interval you pick with the slider.

- **Burn rate** — spend in the trailing window, extrapolated to an hourly rate, with runway.
- **Spend per check** — one bar per poll, newest on the right, tweened in place as the window scrolls.
- **Daily spend** — last 30 completed UTC days, and the top models by cost. Needs a
  management key (Settings → Provisioning keys); a normal key still drives the live meter.

The key lives in the page's memory only. Nothing is stored, and nothing is sent anywhere
but `openrouter.ai`. Closing the tab clears it.

Dark mode follows your OS. Motion respects `prefers-reduced-motion`.
