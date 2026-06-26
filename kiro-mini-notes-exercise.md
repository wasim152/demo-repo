# Kiro Learning Exercise: Mini Notes App

This file is a step-by-step exercise you can use on another laptop to learn Kiro features slowly and clearly.

The goal is not to build everything at once. The goal is to learn how Kiro works by using:

- Feature Spec
- Requirements
- Design
- Task List
- Steering
- Manual Hook
- Bug Spec
- Refactor

---

## Project: Mini Notes App

You will build a simple website using only:

```text
index.html
style.css
script.js
README.md
```

The app will let you:

1. Add a note
2. Show notes on the page
3. Delete a note
4. Save notes in browser localStorage
5. Load notes again after refresh
6. Use a Kiro Feature Spec
7. Use Steering
8. Use Tasks one by one
9. Use a Bug Spec
10. Use a Manual Hook

---

# Step 0: Create a new project folder

Do not reuse the counter project.

Create a new folder called:

```text
kiro-notes-demo
```

Open that folder in Kiro.

Your folder should be empty at first.

---

# Step 1: Ask Kiro to create a Feature Spec only

Paste this into Kiro chat:

```text
Create a new Feature Spec for a very simple website called Mini Notes App.

Use requirements-first workflow.

Use only:
- HTML
- CSS
- vanilla JavaScript

Do not use:
- React
- Vue
- Angular
- TypeScript
- Vite
- Node
- any backend
- any database

The app should:
- show a page title
- have a text input or textarea for writing a note
- have an Add Note button
- display added notes in a list
- allow the user to delete a note
- save notes in browser localStorage
- load saved notes when the page refreshes
- show a message when there are no notes
- include a README with run instructions and manual test checklist

Do not write code yet.
Only create the spec.
```

## What you should check

After this step, you should see something like:

```text
.kiro/specs/mini-notes-app/
  requirements.md
  design.md
  tasks.md
  config.kiro
```

At this point, do not ask Kiro to implement yet.

---

# Step 2: Review the requirements

Open:

```text
.kiro/specs/mini-notes-app/requirements.md
```

Check that it includes these requirements:

```text
The app shall allow the user to type a note.
The app shall allow the user to add the note.
The app shall display added notes.
The app shall allow the user to delete a note.
The app shall save notes to localStorage.
The app shall load saved notes after page refresh.
The app shall show an empty-state message when no notes exist.
The app shall not require a backend server.
```

If any are missing, paste this into Kiro:

```text
Update the requirements.

Make sure the requirements include:
- user can type a note
- user can add a note
- user can see notes in a list
- user can delete a note
- notes are saved in localStorage
- saved notes load again after page refresh
- empty message appears when no notes exist
- app works without backend server

Do not write code yet.
```

Only continue when the requirements look correct.

---

# Step 3: Create steering before coding

This time, create steering early.

In the file tree, create:

```text
.kiro/steering/project.md
```

Your project should look like this:

```text
.kiro/
  specs/
    mini-notes-app/
      requirements.md
      design.md
      tasks.md
      config.kiro
  steering/
    project.md
```

Paste this into `.kiro/steering/project.md`:

```md
# Project Steering

## Project Goal

Build a very small beginner-friendly Mini Notes App using only HTML, CSS, and vanilla JavaScript.

## Technology Rules

- Use only index.html, style.css, script.js, and README.md.
- Do not use React, Vue, Angular, TypeScript, Vite, Node, npm, backend servers, or databases.
- Use browser localStorage for saving notes.
- Keep the app simple enough for a beginner to understand.

## Work Style Rules

- Implement only one task at a time.
- After each task, stop and explain what changed.
- Do not skip ahead to later tasks.
- Do not rewrite the whole project unless asked.
- Update README.md only when the behavior changes or when tests are added.

## Code Style Rules

- Use semantic HTML where possible.
- Use clear CSS class names.
- Use beginner-friendly JavaScript.
- Prefer simple functions.
- Avoid clever or advanced patterns.
- Add comments only where they help learning.

## Testing Rules

After each behavior change, manually test the app.

The final checklist must include:
- page opens correctly
- empty-state message appears when no notes exist
- user can type a note
- Add Note button adds the note
- empty notes are not added
- user can delete a note
- notes remain after page refresh
- deleted notes stay deleted after refresh
```

---

# Step 4: Tell Kiro to read steering

Paste this into Kiro chat:

```text
I created .kiro/steering/project.md.

Read and follow the steering rules before continuing.

Do not implement anything yet.

First, confirm the project rules you will follow in 5 short bullet points.
```

## What you should expect

Kiro should summarize rules like:

```text
- Use only HTML, CSS, and vanilla JavaScript.
- Build one task at a time.
- Use localStorage for saving notes.
- Keep code beginner-friendly.
- Update README when behavior changes.
```

If Kiro says it will use React, npm, Vite, or TypeScript, stop it and say:

```text
Do not use frameworks or build tools. Follow .kiro/steering/project.md.
```

---

# Step 5: Ask for the design

Paste this:

```text
Create the design for the Mini Notes App.

Follow .kiro/steering/project.md.

Use this exact file structure:
- index.html
- style.css
- script.js
- README.md

The design should explain:
- what each file does
- what HTML elements are needed
- what CSS sections are needed
- what JavaScript functions are needed
- how localStorage will be used

Do not write code yet.
```

## What to check

The design should mention simple functions like:

```text
loadNotes()
saveNotes()
renderNotes()
addNote()
deleteNote()
```

It should also mention localStorage key, for example:

```text
miniNotes
```

If it does not mention localStorage, ask:

```text
Update the design to explain exactly how localStorage will save and load notes.
Do not write code yet.
```

---

# Step 6: Ask for tasks, but no code

Paste this:

```text
Create the implementation task list.

Follow .kiro/steering/project.md.

Make each task small and testable.

Do not write code yet.
```

Your tasks should look something like this:

```text
Task 1: Create basic HTML structure.
Task 2: Add CSS layout and styling.
Task 3: Add JavaScript to add notes to the page.
Task 4: Prevent empty notes.
Task 5: Add delete note feature.
Task 6: Save notes to localStorage.
Task 7: Load saved notes on page refresh.
Task 8: Add README instructions and manual test checklist.
Task 9: Final review and cleanup.
```

---

# Step 7: Implement Task 1 only

Paste this:

```text
Implement Task 1 only.

Task 1: Create the basic HTML structure.

Follow .kiro/steering/project.md.

Requirements for this task:
- create index.html
- add a page title
- add a textarea for writing a note
- add an Add Note button
- add an area where notes will appear
- add an empty-state message
- link style.css
- link script.js

Do not add JavaScript logic yet.
Do not add full styling yet.
After finishing, stop and explain what changed.
```

## Test after Task 1

Open `index.html` in your browser.

You should see:

```text
Mini Notes App
textarea
Add Note button
empty message
```

Do not expect the button to work yet.

---

# Step 8: Implement Task 2 only

Paste this:

```text
Implement Task 2 only.

Task 2: Add simple CSS layout and styling.

Follow .kiro/steering/project.md.

Requirements for this task:
- create style.css if it does not exist
- center the main app container
- make the textarea easy to see
- style the Add Note button
- style the notes list area
- style the empty-state message
- keep the design simple

Do not add JavaScript logic yet.
After finishing, stop and explain what changed.
```

## Test after Task 2

Refresh your browser.

Check:

```text
The page looks cleaner.
The textarea is visible.
The Add Note button is styled.
The empty message is visible.
```

Still, the button may not work yet. That is okay.

---

# Step 9: Implement Task 3 only

Paste this:

```text
Implement Task 3 only.

Task 3: Add JavaScript to add notes to the page.

Follow .kiro/steering/project.md.

Requirements for this task:
- create script.js if it does not exist
- when the user types a note and clicks Add Note, the note appears in the notes list
- clear the textarea after adding a note
- hide the empty-state message when at least one note exists
- keep JavaScript beginner-friendly

Do not add delete yet.
Do not add localStorage yet.
After finishing, stop and explain how the JavaScript works.
```

## Test after Task 3

In the browser:

1. Type:

```text
Buy milk
```

2. Click Add Note.

Expected:

```text
Buy milk
```

appears on the page.

3. Add another note:

```text
Study Kiro
```

Expected:

```text
Buy milk
Study Kiro
```

4. Refresh the page.

Expected for now:

```text
Notes disappear
```

That is okay because localStorage is not added yet.

---

# Step 10: Implement Task 4 only

Paste this:

```text
Implement Task 4 only.

Task 4: Prevent empty notes.

Follow .kiro/steering/project.md.

Requirements for this task:
- if the textarea is empty, do not add a note
- if the textarea contains only spaces, do not add a note
- show a short message such as "Please write a note first."
- clear the message after a valid note is added
- keep the code simple

Do not add delete yet.
Do not add localStorage yet.
After finishing, stop and explain what changed.
```

## Test after Task 4

Test these:

| Action | Expected result |
|---|---|
| Click Add Note with empty textarea | No note is added |
| Type spaces only and click Add Note | No note is added |
| Type real note and click Add Note | Note is added |
| After real note is added | Warning message disappears |

---

# Step 11: Implement Task 5 only

Paste this:

```text
Implement Task 5 only.

Task 5: Add delete note feature.

Follow .kiro/steering/project.md.

Requirements for this task:
- each note should have a Delete button
- clicking Delete removes only that note
- if all notes are deleted, show the empty-state message again
- keep the code beginner-friendly

Do not add localStorage yet.
After finishing, stop and explain what changed.
```

## Test after Task 5

Add three notes:

```text
Note one
Note two
Note three
```

Delete the second note.

Expected:

```text
Note one
Note three
```

Then delete all notes.

Expected:

```text
No notes yet
```

or your empty-state message appears again.

---

# Step 12: Implement Task 6 only

Paste this:

```text
Implement Task 6 only.

Task 6: Save notes to localStorage.

Follow .kiro/steering/project.md.

Requirements for this task:
- save the notes array to localStorage whenever a note is added
- save the notes array to localStorage whenever a note is deleted
- use a clear localStorage key, such as "miniNotes"
- keep the code simple

Do not add loading from localStorage yet.
After finishing, stop and explain what changed.
```

## Test after Task 6

Add a note.

Open browser DevTools:

```text
Application tab -> Local Storage
```

Look for a key like:

```text
miniNotes
```

You should see your notes stored there.

Refresh the page.

Expected for now:

```text
Notes may still disappear from the page
```

That is okay because loading is Task 7.

---

# Step 13: Implement Task 7 only

Paste this:

```text
Implement Task 7 only.

Task 7: Load saved notes from localStorage when the page opens.

Follow .kiro/steering/project.md.

Requirements for this task:
- when the page loads, read saved notes from localStorage
- convert saved JSON back into an array
- display saved notes on the page
- if there are no saved notes, show the empty-state message
- keep the code beginner-friendly

After finishing, stop and explain how localStorage loading works.
```

## Test after Task 7

Do this carefully:

1. Add this note:

```text
This note should stay after refresh
```

2. Refresh the browser.

Expected:

```text
This note should stay after refresh
```

3. Delete the note.

4. Refresh again.

Expected:

```text
The note should not come back
```

This confirms both save and load work.

---

# Step 14: Implement Task 8 only

Paste this:

```text
Implement Task 8 only.

Task 8: Add README instructions and manual test checklist.

Follow .kiro/steering/project.md.

README.md should include:
- project name
- what the app does
- files used
- how to run by opening index.html
- manual test checklist
- note that data is saved in browser localStorage

After finishing, stop and explain what changed.
```

## Check README

Open:

```text
README.md
```

Make sure it has a checklist similar to:

```text
- Page opens correctly
- Empty-state message appears when no notes exist
- User can add a note
- Empty notes are blocked
- User can delete a note
- Notes stay after refresh
- Deleted notes do not return after refresh
```

---

# Step 15: Use a Manual Hook

Now test a different Kiro feature: Manual Hook.

Ask Kiro:

```text
Create a manual hook called README Review.

When I run this hook, it should:
- review index.html, style.css, script.js, and README.md
- check whether README.md matches the current app behavior
- update README.md if the app behavior changed
- keep the README beginner-friendly

Do not run automatically.
Only run when I manually trigger it.
```

## After creating the hook

Run the hook manually from Kiro.

Then check whether `README.md` was reviewed or updated.

This is useful because hooks help you automate repeatable project maintenance.

---

# Step 16: Create a Bug Spec

Now intentionally test the bug workflow.

Paste this:

```text
Create a Bug Spec.

Bug:
If I type a note with spaces before or after the words, the app saves the spaces too.

Expected behavior:
The app should trim spaces before saving the note.

Example:
If I type "   Learn Kiro   ", the saved note should display as "Learn Kiro".

Use requirements-first bug workflow.
Do not fix the bug until the bug requirements and tasks are created.
```

## What to check

Kiro should create a bug spec with:

```text
Bug requirement
Expected behavior
Tasks to fix
```

Then ask:

```text
Implement the bug fix task only.

Follow .kiro/steering/project.md.

After fixing:
- notes should be trimmed before saving
- empty notes with only spaces should still be blocked
- README test checklist should be updated
- stop and explain what changed
```

---

# Step 17: Test the bug fix

In the app, type:

```text
   Learn Kiro   
```

Click Add Note.

Expected:

```text
Learn Kiro
```

not:

```text
   Learn Kiro   
```

Then type only spaces:

```text
     
```

Expected:

```text
No note is added
```

---

# Step 18: Ask Kiro to refactor only

Now test refactoring.

Paste this:

```text
Refactor script.js only.

Follow .kiro/steering/project.md.

Goals:
- keep the same behavior
- make the code easier to read
- use simple function names
- do not change the UI
- do not add new features
- do not change CSS
- do not change HTML unless absolutely necessary

After refactoring, explain what changed and list what I should retest.
```

## Retest after refactor

Retest:

```text
Add note
Block empty note
Delete note
Refresh page
Deleted note stays deleted
```

---

# Step 19: Final learning review

Paste this into Kiro:

```text
Review this project as a learning exercise.

Explain:
- what the Feature Spec did
- what Steering did
- what Tasks did
- what the Manual Hook did
- what the Bug Spec did
- how localStorage works in this project
- what I should build next
```

This step helps you connect the project to Kiro’s features instead of only looking at the final code.

---

# Important rule for this exercise

Do not ask Kiro to “build the whole app.”

Use this pattern every time:

```text
Implement Task X only.
After finishing, stop and explain what changed.
```

That is the best way to learn.

Your learning path for this project is:

```text
Spec -> Requirements -> Steering -> Design -> Tasks -> Task 1 -> Test
Task 2 -> Test
Task 3 -> Test
Task 4 -> Test
Task 5 -> Test
Task 6 -> Test
Task 7 -> Test
README -> Hook -> Bug Spec -> Refactor
```
