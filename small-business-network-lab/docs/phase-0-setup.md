# Phase 0 — Setup & Repo Skeleton

## Goal
Verify my Packet Tracer installation and the exact device models this lab uses,
then create the GitHub repo and its file skeleton so every later phase has a home.

## Diagram
Not applicable yet — no topology exists. The first diagram arrives with Phase 1.

## Addressing
Not applicable yet — nothing is configured. The full plan already lives in
[ip-addressing-plan.md](ip-addressing-plan.md), all rows marked planned.

## Verification I ran (my actual results)
 Check  How  My result 
---------
 Packet Tracer version  Help → About  9.0.0 
 Router model 1941 available  bottom-left palette → Routers  found 
 Switch model 2960 available  bottom-left palette → Switches  found 
 PC + Server available  bottom-left palette → End Devices  found 
 GitHub repo created  github.com → New repository  small-business-network-lab 

Screenshot proof `verificationphase0-pt-version.png` (About dialog from my install).

## Commands learned
None this phase — Phase 0 is verification and setup, no device CLI.
The first Cisco CLI arrives in Phase 1.

## Problems & fixes
- Caught a wrong date in my own docs before the first commit the text said
  2026-11-20 while my file timestamps showed 2026-11-26. Fixed before committing.
  Lesson check generated text against reality, not the other way round.
- Nothing else — this section starts earning its keep in Phase 1.

## What I learned
- Exact versions matter device models and behavior differ between Packet Tracer
  releases, so documenting mine (9.0.0) makes the lab reproducible for anyone reading.
- Structure before content writing PROGRESS.md and the addressing plan before
  configuring anything means every later step has a fixed reference to check against.
- File names on GitHub are unforgiving (no spaces, exact extensions) — copy-paste
  and Notepad's All Files (.) beat typing from memory.

## Interview Q&A (Phase 0 edition)
Q Why document the Packet Tracer version and verify device model names before building anything
A Labs should be reproducible. Available models and behavior vary between PT versions,
so I verified that the 1941, 2960, PC, and Server exist in my 9.0.0 installation
before designing the topology around them.

Q Why is this repo public
A It's a portfolio. The value is showing how I work — plans, verification screenshots,
mistakes, and fixes. A private repo proves nothing to a reviewer.

Q What is PROGRESS.md for
A It's the live state of the build last completed step, exact next step, open issues.
My sessions are short and sometimes interrupted, so it lets me resume without leaving
the network half-configured.