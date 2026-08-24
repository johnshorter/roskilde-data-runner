# Contributing

Thanks for helping make the game better. A few ground rules keep it simple to maintain and distribute.

## The one hard constraint

The game must stay a **single self-contained HTML file** with **no external dependencies** (no CDN scripts, no fonts fetched from the network, no build step). Students download one file and double-click it, sometimes offline. If a change needs a library, it probably needs rethinking.

## How to work on it

1. Fork, branch, edit `Roskilde_Data_Runner.html` directly.
2. Test by opening the file in a browser. Play the level you touched in both normal and hard mode; also run it once inside a full Campaign to make sure level transitions still work.
3. Optional syntax check without a browser:
   ```bash
   python3 - << 'EOF'
   import re, subprocess, pathlib
   html = pathlib.Path("Roskilde_Data_Runner.html").read_text()
   for i, s in enumerate(re.findall(r'<script[^>]*>(.*?)</script>', html, re.S)):
       p = pathlib.Path(f"/tmp/s{i}.js"); p.write_text(s)
       r = subprocess.run(["node","--check",str(p)], capture_output=True, text=True)
       print(f"script {i}:", "OK" if r.returncode==0 else r.stderr[:400])
   EOF
   ```
4. Open a PR describing what changed and how you tested it.

## Code conventions

- Vanilla ES5-ish JavaScript, matching the existing style (each level is an IIFE module `L1`…`L10` with a `start()` entry point).
- All user-facing English strings live in `I18N.en`; keep the parallel Danish strings in `I18N.da` updated when you change or add text, even though the language toggle is currently disabled.
- Use the existing CSS variables (`--mint`, `--coral`, `--amber`, etc.) rather than new hex colors.
- Keep the timer pattern consistent: levels call `setTimerbar(frac)` inside `startLoop`.

## Scope notes

- The verification code is intentionally not cryptographically secure. Making it "unfakeable" is out of scope; making it *less* casual-fakeable is fine.
- Content changes (question pools, level tuning) should match what's actually taught in BC1 — when in doubt, cite the lecture or compendium chapter in the PR.
