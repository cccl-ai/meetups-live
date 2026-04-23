# Panel Questions Page — Prompts Used

**Session date:** 2026-04-21  
**Project:** `meetups-live` (github.com/cccl-ai/meetups-live)  
**Output:** `bangalore/blr-1/panel-questions.md`

---

## Phase 1 — Discovery & Structure

**Prompt 1**
> See we have CCCL meeting notes for recap etc for London. Look at the repos and see the structure and I want to create one for Bangalore. So just should I have a separate repo or can it go in the existing repos?

*Outcome: Explored `meetups-live`, `meetups-daily`, `meetups-deep-dives`. Decided on subfolder `bangalore/blr-1/` inside existing `meetups-live` repo.*

**Prompt 2**
> Okay, I need one for Bangalore and for Bangalore we might have panel. So I want to create a file that will have the questions. So just a structure.

*Outcome: Created stub files — `agenda.md`, `panel-questions.md`, `recap.md` inside `bangalore/blr-1/`.*

---

## Phase 2 — Main Creation

**Prompt 3 (key prompt)**
> see /Users/vikram/gitper/cccl-blr-questions.md use that to create panel-questions.md And then you know the drill, it needs to be a beautiful file like other files so that I can see it as a website. And I've forgotten how I do it but tell me once you've done it.

*Outcome: Read the WhatsApp-extracted questions file. Read `_layouts/default.html` and `assets/style.css` to understand the Jekyll/CSS design system. Created the full `panel-questions.md` using Jekyll frontmatter + `speaker-card` HTML components. Questions grouped into 6 themes. Ran Jekyll locally with homebrew Ruby (system Ruby 2.6 was too old; installed Ruby 4 via brew). Told user the local preview URL and the single command to run Jekyll in future.*

---

## Phase 3 — Iterative Refinements

**Prompt 4**
> need to have the ids

*Outcome: Added the question IDs (e.g. `pihe01`, `ANUM03`) as `<code>` tags in each card's speaker-links line.*

**Prompt 5**
> need to have the ids, the original file is updated now

*Outcome: Re-read source file. IDs were already there from the start — no change to source, confirmed IDs already mapped correctly.*

**Prompt 6**
> I want the questions to be verbatim.

*Outcome: Replaced all paraphrased question text with the original verbatim wording from the WhatsApp source, including typos, informal phrasing, and sentence fragments.*

**Prompt 7**
> only the footer for now WhatsApp · Slack · Events · cccl.ai

*Outcome: Investigated how to make the footer city-specific. Added `footer_links` frontmatter key to the page. Updated `_layouts/default.html` to check for `page.footer_links` and use it if present, falling back to London defaults.*

**Prompt 8**
> see cce to know what the Social links needs to be liked. Some of them point to Bangalore ones.

*Outcome: Searched `claude-code-events` repo for Bangalore URLs. Found `cccl.ai/blr/whatsapp`. Set WhatsApp footer link to that.*

**Prompt 9**
> events needs to go to bangalore events

*Outcome: Searched `claude-code-events` for Bangalore events URL. Found `cccl.ai/blr/luma`. Updated Events footer link.*

---

## Phase 4 — Publish & Share

**Prompt 10**
> looks good publish

*Outcome: Committed 4 files (`agenda.md`, `panel-questions.md`, `recap.md`, `_layouts/default.html`) and pushed to `cccl-ai/meetups-live` on GitHub. GitHub Pages deployed automatically.*

**Prompt 11**
> put the link to it in slack in private bangalore channel

*Outcome: Used Slack MCP to search for `#bangalore` channel (private, ID `C0AUP3JLWPJ`). Created a draft message with the live URL. User sent it.*

**Prompt 12**
> update the date to be the event date 25th april

*Outcome: Changed `event_date` in frontmatter from `21 April 2026` to `25 April 2026`. Committed and pushed.*

---

## Summary

| Phase | Prompts | Key output |
|-------|---------|------------|
| Discovery & structure | 2 | Folder + stub files created |
| Main creation | 1 | Full panel-questions page, Jekyll running locally |
| Refinements | 6 | IDs, verbatim text, city-specific footer |
| Publish & share | 3 | Live on GitHub Pages, shared in Slack |
| **Total** | **12** | |

**Total elapsed time:** ~60 minutes (including Ruby install and Jekyll setup)
