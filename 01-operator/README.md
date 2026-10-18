# Operator — an AI-orchestrated build I directed

**What it is:** A personal operating-system web app (habit/goal tracker with a daily boot/shutdown ritual, a self-paced study-pace instrument, and automated email reminders). Built as a Google Apps Script web app with a tested pace engine and a one-command deploy pipeline.

**My role:** I did not hand-write the app. I specified it, made the product decisions, and directed [Claude Code](https://claude.com/claude-code) to build, test, and deploy it — then reviewed every change. This is the AI-orchestration skill at the center of modern AI engineering: turning intent into a shipped, tested, deployed system by directing an agent and owning the judgment layer.

**What it demonstrates**
- **Spec → ship:** translated a fuzzy personal need into a working, deployed product.
- **Testing:** a server-side pace engine with a Node test suite and fixtures; releases are gated on green tests.
- **Deployment:** `clasp` push → version → redeploy pipeline, with a post-deploy check that the live version id actually moved.
- **Reviewing AI output:** every agent diff reviewed before release — the judgment layer is mine.

**Honest scope:** Solo project, single user (me). No live external traffic or customers. The value shown is the *orchestration + ship + verify* loop, not scale.

**Stack:** Google Apps Script, JavaScript, HTML, Node (tests), clasp (deploy).

> TODO before applying: public-safe screenshots, a 60-second architecture note, and a short "what I'd do differently" section.
