# Contributing

Thanks for your interest in contributing!

## Development workflow
- Edit the Pine Script in `src/MagicTrend_V1_1.pine`.
- Keep changes small and focused.
- Update the indicator title/version string when releasing (`Magic Trend_V1.2`, etc.).
- Update `CHANGELOG.md` for user-facing changes.

## Pull requests
1. Fork the repo and create a branch: `feature/short-name`.
2. Commit with clear messages:
   - `feat: add MTF toggle`
   - `fix: prevent line repaint on ...`
3. Open a PR against `main` and fill out the PR template.
4. Be ready to iterate based on review comments.

## Code style / guidelines
- Prefer descriptive variable names.
- Avoid repainting logic unless intentional and documented.
- Keep inputs well-labeled with `title`.
- Use comments to explain non-obvious logic.

## Testing
- Add the script to a chart with multiple symbols/timeframes.
- Verify alerts compile and trigger as expected.
- Check the MTF dashboard and S/R zones render without flicker on live bars.
