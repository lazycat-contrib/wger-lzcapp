# wger (LazyCat LPK)

Self-hosted workout and fitness manager.

- Upstream: https://github.com/wger-project/wger
- Image: `wger/server:2.7.0` (mirror mode, digest-matched)
- License: AGPL-3.0 (full text in `content/licenses/LICENSE`)
- Containers: single (SQLite)

## Notes

- Single container via `PS_DATABASE_URI=sqlite:////home/wger/src/database.sqlite`
  (upstream ships `config/dev-sqlite.env` proving SQLite is supported).
- `DJANGO_SECRET_KEY` comes from a platform stable secret.
- No seeded account: registration is open (`ALLOW_REGISTRATION=true`) and the first user
  signs up through the UI.
- Data on `/lzcapp/var/{src,media,static}`.
- No mail service configured (password reset by email unavailable).
- Not yet verified on a real device.
