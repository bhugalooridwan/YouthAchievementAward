# Youth Achievement Award

A clickable, single-file prototype of a youth achievement award programme: participants set goals
across four core pillars, mentors assign and assess tasks, and badges are struck automatically as
objectives are met.

Everything lives in [index.html](index.html) — markup, styles and logic. There is no build step, no
server and no dependencies. Open the file in a browser and it runs.

## Programme model

**Four levels**, taken in order. Each has its own level badge and identity statement.

| Level | Level badge | Identity |
| --- | --- | --- |
| Foundation | Pathfinder Badge | "I started my journey" |
| Growth | Builder Badge | "I am consistent and growing" |
| Leadership | Navigator Badge | "I lead and take responsibility" |
| Purpose | Legacy Badge | "I create impact and purpose" |

**Four core pillars**, repeated in every level, each awarding one pillar badge:

- Personal Development → Personal Badge
- Skills Development → Skill Badge
- Service & Community Engagement → Service Badge
- Physical / Experiential Learning → Physical Badge

That gives 16 pillar badges in total, built from objectives drawn from the programme tracks.

## How progression works

1. A **pillar badge** is struck when every objective in that pillar has been met.
2. A **level badge** needs all four pillar badges, plus a written reflection, plus the final
   challenge. Badges alone do not close a level.
3. Closing a level unlocks the next one. Locked levels cannot award badges and cannot take goals.

Objectives are met through goals and tasks: a goal is linked to one or more objectives, and once
every task under that goal is recorded as met, the goal completes and its objectives are credited.

## Participant journey

Each participant is tracked through six stages, derived from their live data and shown as a stepper
on the participant home page, the staff drill-down and the guidelines page:

Enrollment → Goal Setting → Activity Participation → Mentorship / Supervision → Assessment →
Certification / Award

## Goal workflow

Goals move through a fixed sequence so that nothing is imposed on a participant:

1. Created by a mentor, coach or the participant, in one of the four pillars
2. **Proposed**
3. Mentor or coach **approves** it
4. Participant **acknowledges** it
5. **Active** — tasks can now be assigned
6. All tasks met → **Completed**, and the pillar badge is re-checked

## Roles

Sign-in is a role picker; no passwords. Each role sees a different application.

| Role | Can do |
| --- | --- |
| Participant | View their pathway and badge case, propose goals, acknowledge goals, start tasks, write level reflections, edit their own details |
| Mentor or coach | Everything for their group: set goals, approve proposals, assign tasks, record results, record final challenges, register participants |
| Helper | View and support only the participants assigned to them |
| Programme head (admin) | Full access, plus programme structure editing, achievement overrides, people management, reports and the activity log |

## What is in the prototype

- **Pathway** — the full four-level trail with medals, objective counts, and the reflection and
  final-challenge panels that close each level
- **Badge case** — every pillar badge by level, with progress bars
- **Goals and tasks** — proposal, approval, acknowledgement, task assignment, evidence records
  (supervisor, location, dates, skills) and comment threads
- **Approvals queue** — proposed goals waiting on a mentor
- **Programme structure editor** — rename pillars and badges, add, edit and remove objectives;
  changes re-run the progression engine for every participant
- **Reports** — badge completion by participant, badges awarded per pillar, skills logged on met
  tasks, and the goal pipeline
- **Activity log** — an audit trail of goal, task, badge and account changes
- **Guidelines** — the rules the system enforces, the journey, the pillars and the levels

## Notes

- All data is seeded in memory and resets on reload. Nothing is persisted.
- Safeguarding rules are modelled: participants under 13 need a guardian email on file, and tasks
  away from the institution need a named supervisor.
- The interface is responsive, keyboard-navigable and respects `prefers-reduced-motion`.