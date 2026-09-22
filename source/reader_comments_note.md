# Source — the reader comment layer (not reproduced here)

The comic has had a Disqus comment thread running since 2012. Pages 905–923 carry roughly **393 live comments from around 14 regular commenters** — the largest-n human sample in the experiment, and the layer that surfaced the control-by-semiotics reading and the cross-language mastery observation.

**Those comments are not in this repository.** This file explains where they are, what was done with them, and what the omission costs.

---

## Where they are

In the comment threads on the pages themselves: `https://giftscomic.com/index.php?comic_id=N` (N = page + 1), below each comic. Reading them requires JavaScript — they do not appear in the page source, so a plain fetch does not retrieve them.

## How they were obtained

The author supplied a full Disqus XML export (a ~122,000-line file, ~4.9 MB). It was parsed with `xml.etree.ElementTree` — **not** regex, which is unreliable at that scale and silently drops malformed entries. 393 comments extracted and read.

## What was done with them

One question was asked of every comment: **what did this person notice that the author and I did not?** Not sentiment, not topic, not agreement. Vantage points. The findings are in `../analysis/synthesis.md` (vantage point 4), `../analysis/cross_language_note.md`, and `../FINDINGS.md`.

## Why they are not reproduced

The commenters commented on a comic. They did not agree to be part of a study. **Republishing their words inside an analytic frame they never consented to is a different act from reading them, and it is one this repository does not do.** Individual comments and usernames are excluded; their observations are summarised and generalised, with no identifying detail. See `../NOTICE.md`.

## What this costs

**The largest evidence base in the experiment is the one a reader cannot check.**

Everything downstream of the reader layer — the control-by-semiotics finding, the mastery observation, the claim that readers read faces for inner state — **is not independently verifiable from anything in this repository.** A reader who doubts those findings has no way to test them except by reading the thread themselves, which is possible but laborious, and by then their own reading is a *different* vantage point, not a check on mine.

**Stated plainly: if you are going to be sceptical of any part of this repo, be sceptical of the reader-layer findings.** They are the findings with the strongest sample and the weakest verifiability, and those two properties together are exactly the conditions under which a researcher's own frame is most likely to have done the work.

## If you are one of those commenters

The observation that English *mastery* carries a craft/command distinction Russian мастерство does not is **yours, not mine.** So is the reading that the arc is largely about steering people through information. Those two points reshaped how this experiment reads the whole comic, and they came from someone reading it for pleasure.

If you see your observation generalised here in a way you object to, that is a legitimate objection and it should be raised.

## How to check the layer yourself

The threads are public and the comic is free. Read the pages, then read the comments underneath, and ask the same single question: **what did this person notice that I did not?** That question is the whole method. It does not need my dataset.


**Update 2026-09-23:** the author confirms the reader layer is not merely reactive — reader input flows upstream into canon (a reader suggested the warlord Nero's name; reader-suggested situations became extra sketches; reader questions produced clarification pages in the comic proper). Details and structural reading: `analysis/the_inlet.md`. This strengthens the case for eventually verifying the comment layer despite the cost: it is the inlet, not just a vantage point.
