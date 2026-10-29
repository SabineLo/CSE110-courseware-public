# Lemon Clicker Bug Report

**Name:**
**Tickets solved: 4** <!-- e.g. 1, 2, 3, 5, 6 (at least five) -->

Copy the template below once for each ticket you solved. 

---

## Ticket 4 : Stuck on the Game Over screen

### Actual cause

<!-- Which file and function was the bug in, and what was wrong with the code?
     Explain why that code produced the behavior described in the ticket. -->

**File / function:**
file: GameScreenController function: endGame()
**What was wrong:**
It was calling this.StopTimer() incorrectly so the timer just kept going/ it kept calling the showResultsFromServer repeatedly.

### Fix

<!-- What did you change, and why does that change fix the problem? -->
Fixed it by calling this.StopTimer() correctly so I added the parenthesis.

### How did you find it?

#### Hypothesis testing

**What hypothesis ultimately led you to identify the buggy code, and why?**
Knew that the showResultsFromServer kept being called caused I added a consoleLog so I knew somewhere it was being called I checked main and I checked what else was using the switch screens and it was endGame and the error was i want truly ending screen.

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
Confirmed it was gone because I played it again and it was no longer making the noises repeatedly or calling that function multiple times.
<!-- How did you confirm the problem is gone? -->
