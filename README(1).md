# Roskilde Data Runner

## [▶ Play the game in your browser](https://johnshorter.github.io/roskilde-data-runner/)

No install and no login. The link opens the game directly. Works in Chrome, Edge, Safari, and Firefox.

**Want to play offline?** [Download the game as a zip](https://github.com/johnshorter/roskilde-data-runner/archive/refs/heads/main.zip), unzip it, and double-click `Roskilde_Data_Runner.html`.

---

A browser game companion to **Basic Course 1: Empirical Data** (Roskilde University, autumn 2026). Ten quick levels, one per lecture: sorting data types, fixing a messy Danish CSV, choosing the right graph, center and spread, fitting a line, sampling, probability, the binomial, the normal curve, and a final "mini-project" boss round.

## How scoring works

- **Campaign** plays all ten levels in order (about 45 min) for a 1.5× full-run bonus.
- **Free play** jumps to any level; replays keep the best score.
- **Hard mode** runs 2× faster for 2× points.

At the end the student gets a card with name, score, medals, and a verification code of the form `RDR-[flag]-[score]-[hash]`. To win the high-score prize, screenshot that card and send it to your teacher.

Scores never persist between sessions, on purpose. The screenshot is the record, so nothing is stored on the student's machine.

## Files

- **`Roskilde_Data_Runner.html`**: the game. One self-contained file (HTML, CSS, and vanilla JS).
- **`index.html`**: a tiny redirect so the short Play link above opens the game.
- **`TEACHER_verify_code.html`**: [teacher tool](https://johnshorter.github.io/roskilde-data-runner/TEACHER_verify_code.html) for checking a student's score code. Nothing in it is secret, since the same algorithm ships inside the game file, so treat scores as a fun leaderboard, not an exam. The check catches casual screenshot editing only.
- **`docs/moodle_post.md`**: a ready-to-paste Moodle announcement.

## Contributing

Yes please. See [CONTRIBUTING.md](CONTRIBUTING.md). Bug reports and gameplay or teaching suggestions are welcome as issues.

## License

MIT. See [LICENSE](LICENSE).
