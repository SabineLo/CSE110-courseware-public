# Lemon Clicker Bug Report

**Name:**
**Tickets solved: 1** <!-- e.g. 1, 2, 3, 5, 6 (at least five) -->

Copy the template below once for each ticket you solved. 

---

## Ticket 1: Stats always say "Stats unavailable"

### Actual cause

<!-- Which file and function was the bug in, and what was wrong with the code?
     Explain why that code produced the behavior described in the ticket. -->

**File / function:**
file: MenuScreenController function: loadStatsFromServer()

**What was wrong:**
It was trying to fetch api/stat but it was not working because it could not find it and was unable to load it. Since it could not fetch the stats it was not displaying the data in the front page.
### Fix

<!-- What did you change, and why does that change fix the problem? -->
I saw how the server defined the app.get in index.ts and it was api/stats. So in loadStatsFromServer() function I changed it to stats in order for it to get the right request. And the output met the expected output.

### How did you find it?

#### Hypothesis testing

**What hypothesis ultimately led you to identify the buggy code, and why?**
The hypothesis that led me to ultimately identify the buggy code was that all the other functions were calling stats and were called stats while the api was the only one calling stat.
#### Backward tracing

<!-- Start from the symptom you saw and work backwards, one step at a time,
     until you reach the buggy line. For each step, note where you looked
     and what you saw there. Add steps as needed. -->

1. **Symptom:** <!-- what you saw, e.g. text on screen, console error -->
I saw the console error where it was failing and it was giving me a 404 error saying not found.
2. **Traced back to:** <!-- where that came from, e.g. a function, a request in the Network tab, a server log -->
I clicked on the console log where it said it was missing up in and it led me to MenuScreenController line 47 
4. **Buggy code:** <!-- the file, function and line where the trace ended -->
Which is where the buggy code was at await fetch("/api/stat");

<!-- It is okay to use your judgement here in limiting the number of traceback steps. We want to understand your 
    reasoning for how you discovered where the bug was -->

### Confirming the fix
I confirmed the problem was gone by refreshing and making sure that the desired output was being displayed on the screen and it matched the expected result.
<!-- How did you confirm the problem is gone? -->
