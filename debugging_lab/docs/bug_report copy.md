# Lemon Clicker Bug Report

**Name:**
**Tickets solved: 2** <!-- e.g. 1, 2, 3, 5, 6 (at least five) -->

Copy the template below once for each ticket you solved. 

---

## Ticket 2 : Best Score Always Shows 0

### Actual cause

<!-- Which file and function was the bug in, and what was wrong with the code?
     Explain why that code produced the behavior described in the ticket. -->

**File / function:**
file: index.ts function: "app.get("/api/stats", (_req, res) =>) "
**What was wrong:**
The highest socre is always 0 even though there the input in json had the score being 19 so it should have been a new best score.
### Fix

The issue was that since it best was 0 we had it so that if the newest entry for the game was < 0 then it would update best but no number was ever less than 0 and we were trying to find highest score so it should have been reversed if entry > best then best gets replaced.
<!-- What did you change, and why does that change fix the problem? -->

### How did you find it?

#### Hypothesis testing

**What hypothesis ultimately led you to identify the buggy code, and why?**
Looked at the logic of how the scrores were being set up because I knew it had something wrong with how best was being set. Checked the code for that and looked through the logic found that it was because of the < sign which meant it had to be reversed because it was not doing the desired outcome.

#### Backward tracing

<!-- Start from the symptom you saw and work backwards, one step at a time,
     until you reach the buggy line. For each step, note where you looked
     and what you saw there. Add steps as needed. -->

1. **Symptom:** <!-- what you saw, e.g. text on screen, console error -->
2. **Traced back to:** <!-- where that came from, e.g. a function, a request in the Network tab, a server log -->
3. **Traced back to:**
4. **Buggy code:** <!-- the file, function and line where the trace ended -->

<!-- It is okay to use your judgement here in limiting the number of traceback steps. We want to understand your 
    reasoning for how you discovered where the bug was -->

### Confirming the fix
Added different scores in leaderboard.json to make sure the best was always accurate and I refreshed it in order to make sure it would persist. The scores would stay and highest would always show as best score.
<!-- How did you confirm the problem is gone? -->
