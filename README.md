# Dev Team v5 — kit-ის წესებით

## რა სჭირდება
გლობალურად დაყენებული claude-agent-kit (`~/.claude`): `CLAUDE.md`, `project-standard` და `finish-check` skill-ები. Dev Team მათ პირდაპირ იყენებს — ერთი წყარო, ერთნაირი ხარისხი.

## დაყენება
`.claude` საქაღალდე ჩააკოპირე **ახალი ან არსებული პროექტის** root-ში (kit-ის `project-template`-ის **ნაცვლად**, არა ერთად — ორივეს აქვს `.claude/settings.json`). შემდეგ `git add .claude` და commit.

## ბრძანებები
- `/auto <აღწერა>` — ბოლომდე, კითხვების გარეშე, ბრენჩზე `team/...`
- `/auto plan: <აღწერა>` — მხოლოდ გეგმა, მერე ჩერდება
- `/auto continue` — გაგრძელება
- `/audit [სფერო | GitHub URL] [trusted]` — მხოლოდ შემოწმება → `AUDIT.md`
- `/fix [A-001 ...]` — გასწორება ტესტებით

## kit-თან რა არის ერთნაირი
- State: `PROJECT.md` (Appendix A + API Contract) და `PROGRESS.md` (Run State `Stage`-ით) — kit-ის `/next-task` და `/finish-check` აქაც მუშაობს
- დეველოპერები = kit-ის `task-executor`-ის წესები + როლის წესები + ფაილების საზღვარი
- `code-reviewer` = kit-ის `standard-reviewer` (Opus, high)
- ეტაპის შემოწმება = kit-ის `finish-check` (reviewer-ად code-reviewer + security-auditor)
- სიმძიმე, მტკიცებულების წესი, fix-ის ლიმიტი (2 რაუნდი), Accepted Risks, Backlog

## რით განსხვავდება kit-ისგან
- ავტონომიური: არ ჩერდება, ბლოკერებს `## Blockers`-ში წერს და აგრძელებს
- 2 დეველოპერი (frontend / backend) + ცალკე security-auditor + tester (Haiku)
- ცალკე ბრენჩი ყოველ გაშვებაზე
- `verify.sh` ბრძანებებს თავად პოულობს (ხელით შევსება არ სჭირდება)
