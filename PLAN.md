TASK: Build a self-contained HTML quiz portal from course subtitles (Week 1, 2, and 3).

STEP 1 — FIND & READ:
Look in the current folder (and subfolders for each week) for:
- Subtitle/CC files (.srt, .vtt, or .txt) for Week 1, Week 2, and Week 3
- description.html files for each video (Week 1 and Week 2 have these — read and 
  use them as additional context to understand what each video actually teaches, 
  since descriptions often clarify concepts better than raw subtitles)

Read and parse all of this fully. Cross-reference subtitles with their matching 
description.html where available, to build a clear understanding of each topic 
before writing questions.

STEP 2 — GENERATE QUIZ QUESTIONS:
Create 25-30 quiz questions based STRICTLY on the concepts actually taught in 
these files. Do not invent content or pull from general AI knowledge outside 
what's covered.

FORMAT RULE:
- ALL questions must be multiple choice (MCQ) only. No short-answer, no 
  "explain why" open text questions. Every single question needs exactly 4 options.

DIFFICULTY / DISTRACTOR RULE (important):
- Wrong options must be genuinely plausible, not guessable by elimination.
- Do NOT write options where the correct answer is obviously longer, more 
  detailed, or more "technical-sounding" than the wrong ones — that's a giveaway.
- Do NOT write wrong options that are vague, silly, or clearly off-topic just to 
  fill the 4-option slot.
- All 4 options should be similar in length, tone, and specificity.
- Best practice: wrong options should be common misconceptions, half-truths, or 
  answers that would be correct in a DIFFERENT but related context — so someone 
  who skimmed the material could actually be tricked into picking them.
- Test yourself mentally: if a question could be answered correctly without 
  knowing the material, just by "sounds right" pattern matching — rewrite it.

CONTENT RULES:
- No trivial or "gotcha" questions — every question must test real understanding
- Cover the FULL breadth of material across all 3 weeks, not just one topic
- Order from easier/foundational to harder/applied
- No ambiguous wording
- If the material only genuinely supports fewer good questions, give fewer 
  instead of padding with weak ones

LABELING RULE (important):
- The QUESTION TEXT itself must NEVER mention which day, video, or week the 
  content is from (e.g. do not write "In Day 1 – Sub-Agents & Context Management, 
  what does X mean?"). Just ask the concept directly, e.g. "What does X mean?"
- The week/day/video reference is allowed ONLY inside the "topic" field, the 
  hint, or the explanation — as a citation, not as part of the question itself.

FOR EACH QUESTION PROVIDE:
- question text (concept only, no day/video/week labels in it)
- 4 options
- correct answer
- a one-line hint (doesn't give away the answer, doesn't reveal it by making 
  the correct option stand out)
- a full explanation (why correct answer is right, why each wrong option is 
  wrong or where it would apply instead)
- a "source" field noting week/day/video — for reference only, never shown 
  during the question itself

Save this as quiz-data.json in the current folder.

STEP 3 — BUILD THE QUIZ PORTAL:
Create index.html (single file, inline CSS/JS, no external dependencies except 
loading quiz-data.json) with:

- Start screen: quiz title, number of questions, "Start Exam" button
- One question shown at a time, with a progress bar (e.g. "Question 4 of 27")
- Question text shown WITHOUT any day/week/video label
- 4 clickable MCQ options, randomized order each time the quiz loads
- A "Hint" button per question that reveals the hint without penalty
- On submitting an answer: immediately show if correct/incorrect, then reveal 
  the full explanation (including the source/week reference here) before 
  moving to "Next Question"
- Track score as user goes
- Final results screen: score, percentage, and a review list showing every 
  question, the user's answer, correct answer, explanation, and source — so 
  it works as a study tool afterward
- Clean, minimal, readable design, good spacing and typography, no clutter. 
  Should work fully offline in a browser, just by opening index.html.

STEP 4 — VERIFY:
Open/check the generated files to confirm quiz-data.json is valid JSON, that 
no question text contains day/week/video labels, that every question has 
exactly 4 balanced-quality options, and that index.html correctly loads and 
renders everything end to end.

Do all of this now without asking me to paste content — read directly from 
the folder and subfolders.