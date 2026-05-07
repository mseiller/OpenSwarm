# BJJ Swarm — Curriculum Production Pipeline

![BJJ Swarm](assets/new-framework.jpg)

**The open-source multi-agent system for building BJJ curriculum at scale.**

One prompt generates a complete lesson package: slide deck, instructor guide, grading rubric, technique diagrams, and video reference clips — all coordinated by specialist agents, all calibrated to belt level and curriculum scope.

Built on [Agency Swarm](https://github.com/VRSEN/agency-swarm).

---

## What It Produces Per Module

| Deliverable | Agent | Format |
|-------------|-------|--------|
| Lesson slide deck | Slides Agent | HTML + PPTX export |
| Instructor guide | Docs Agent | DOCX + PDF |
| Grading rubric | Docs Agent | DOCX |
| Position diagrams | Image Gen Agent | PNG |
| Technique sequence art | Image Gen Agent | PNG |
| Reference video clips | Video Agent | MP4 |
| Research brief | Deep Research | Markdown |

---

## The Pipeline in Action

**"Build a closed guard module for blue belts"**

1. Deep Research → IBJJF closed guard requirements for blue belt, modern pedagogical approach, common mistakes
2. Slides Agent → Position overview, sweep hierarchy, submission setups, drilling sequence
3. Docs Agent → Class flow, instructor notes, safety callouts, grading criteria
4. Image Gen Agent → Top/side position diagrams, grip fighting sequence, common mistake illustrations
5. Video Agent → Technique reference roll, drilling demo, mistake correction footage

All five run in parallel after Deep Research completes the brief.

---

## Get Started

```bash
git clone https://github.com/YOUR_GITHUB/bjj-swarm.git
cd bjj-swarm
npm install -g @vrsen/openswarm
openswarm
```

Or run locally:

```bash
python swarm.py
```

See [AGENTS.md](AGENTS.md) for customization instructions.

---

## Forked from OpenSwarm

BJJ Swarm is a domain-specific fork of [VRSEN/OpenSwarm](https://github.com/VRSEN/OpenSwarm) — the general-purpose content production swarm. Customizations are in the agent `instructions.md` files and `shared_instructions.md`.
