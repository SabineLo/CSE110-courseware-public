# Lemon Clicker Bug Report

**Name:**
**Tickets solved: 3** <!-- e.g. 1, 2, 3, 5, 6 (at least five) -->

Copy the template below once for each ticket you solved. 

---

## Ticket 3 : The Lemon Only Lands in Four Spots

### Actual cause

<!-- Which file and function was the bug in, and what was wrong with the code?
     Explain why that code produced the behavior described in the ticket. -->

**File / function:**
file: GameScreenView.ts function: randomizeLemonPosition(): void  
**What was wrong:**
The lemon kept appearing on the four corners of the screen so I had to view the code in randomizeLemonPosition and I found the error being that it was being rounded.
### Fix
Fixed it by getting rid of the rounded method and it fixes it because it no longer takes it to the nearest whole number so it isnt in the same spots majority of the times. 
<!-- What did you change, and why does that change fix the problem? -->

### How did you find it?

#### Hypothesis testing

**What hypothesis ultimately led you to identify the buggy code, and why?**
I had an idea of where the bug could be located since it had to do with the lemon position and last lab we worked on implementing that so I checked the functionality for that and noticed that the x and y positions were being rounded which would lead them to the corners.

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

<!-- How did you confirm the problem is gone? -->
Confirmed it by playing a couple games and making sure that the positions varied and werent always being directed to the corners.
