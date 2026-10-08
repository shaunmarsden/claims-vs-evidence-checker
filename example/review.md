# Review: Renovation Tracker Output

I checked [output.md](output.md) against what [tracker.md](tracker.md) was built to test.

## What Worked

It caught the false "Done". The cabinets note contradicts its own status: it says a check is still outstanding. The output caught this rather than trusting the status field. That's the main job of this skill.

It caught the stale "In Progress" that looked active. At a glance nothing about the tiles item looked wrong, and the status field gives no hint of a problem. Only the age of the note showed that three months had passed with nothing recorded.

It called the blocked item healthy. The electrician item's status is "Blocked", which might look like a problem in itself. The output saw that a specific reason with a named day is what a healthy "blocked" status looks like. It didn't invent a concern where the record and the evidence agree.

It left the empty item alone. There are no notes for painting the hallway, and a job that hasn't started doesn't need any yet. The output didn't invent a concern just to seem thorough on every row.

## What Still Needs a Human Check

Only the person doing the work can confirm whether anyone has checked the corner unit since the cabinets note.

The electrician note has no date of its own, only "next Tuesday". The output calls it dated and current, but nothing in the tracker shows when the note was written. Someone should check the visit still stands.

No notes for painting the hallway can't show the job hasn't started. Only the person doing the work can say.

The three months used to call the tiles item stale is an example for this project. Another project might sensibly use a shorter or longer limit.

## Verdict

No automatic failure. It caught the two mismatched items. It left the two healthy items alone, including one whose label alone might look worrying.
