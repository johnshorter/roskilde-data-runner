# Roskilde Data Runner

A browser game companion to **Basic Course 1: Empirical Data** (Roskilde University, autumn 2026). Ten quick levels, one per lecture: sorting data types, fixing a messy Danish CSV, choosing the right graph, center and spread, fitting a line, sampling, probability, the binomial, the normal curve, and a final "mini-project" boss round.

No install, no internet, no build step. Download `Roskilde_Data_Runner.html` and open it in any browser.

## Files

- **`Roskilde_Data_Runner.html`** — the game. One self-contained file (HTML + CSS + vanilla JS).
- **`TEACHER_verify_code.html`** — teacher tool for checking a student's score code from their screenshot. Not for students, but nothing in it is secret: the verification algorithm also ships inside the game file, so treat scores as a fun leaderboard, not an exam.
- **`docs/moodle_post.md`** — a ready-to-paste Moodle announcement.

## How scoring works

- **Campaign** plays all ten levels in order (~45 min) for a 1.5× full-run bonus.
- **Free play** jumps to any level; replays keep the best score.
- **Hard mode** runs 2× faster for 2× points.

At the end the student gets a card with name, score, medals, and a verification code of the form `RDR-[flag]-[score]-[hash]`. The check catches casual screenshot editing only.

Scores never persist between sessions, on purpose — the screenshot is the record, so nothing is stored on the student's machine.

## Contributing

Yes please — see [CONTRIBUTING.md](CONTRIBUTING.md). Bug reports and gameplay/pedagogy suggestions are welcome as issues.

## License

MIT — see [LICENSE](LICENSE).
