# Lemon Clicker Bug Report

**Name:**
**Tickets solved: 5** <!-- e.g. 1, 2, 3, 5, 6 (at least five) -->

Copy the template below once for each ticket you solved. 

---

## Ticket 5: Leaderboard dates show "undefined"

### Actual cause

<!-- Which file and function was the bug in, and what was wrong with the code?
     Explain why that code produced the behavior described in the ticket. -->

**File / function:**
file: ResultsScreenModel, ResultsScreenView function: updateLeaderboard(entries: LeaderboardEntry[]), type LeaderboardEntry

**What was wrong:**
The type names were not matching one was timestamp the other was time, with the server so it wasnt getting anything which is why it kept showing up as undefined.
### Fix

<!-- What did you change, and why does that change fix the problem? -->
Made sure that all the names matched for time since it was timestamp and time so I changed it all to time.

### How did you find it?

#### Hypothesis testing

**What hypothesis ultimately led you to identify the buggy code, and why?**
I knew it had something to do with the ResultsScreenView since that is where it was being displayed I checked it to make sure it worked and it seemed right so I checked server to see if it was being loaded correctly and I noticed the discrepancies with the naming which is when I changed it and I checked where else it was being named and I went to the Model to change the type there.

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
Confirmed it by playing the game multiple times and refreshing it.
<!-- How did you confirm the problem is gone? -->
