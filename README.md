# Triage Ward

A browser hospital-management game. Name your hospital, open with a free Emergency Room, Pharmacy, Laboratory and Radiology, and grow into 24 departments.

**Play:** https://annabxclu.github.io/Triage-Ward/ (once GitHub Pages is enabled)

## How a case flows
1. Walk-ins arrive at random, about 100 per game day to start (more as you accept insurance plans), straight into the open ward for their condition (or another ward that treats it, or the ER). Name color is triage: red (1 real hour), yellow (2 hours), green (3 hours).
2. In every ward, assign a **triage room** and a named **nurse** for the first tests (vitals, ECG, swabs, urine and glucose checks), then move them to the **waiting room** or a **diagnostic room** where you assign a **doctor** to examine, diagnose and treat.
3. Run tests to uncover hidden findings. The chart's **Examinations** section lists the basic work-up plus only the tests that could help with the current likely diagnoses, grouped as bedside, Laboratory and Radiology. Tap the ones you want: the doctor runs the bedside exams, then the patient goes to the Lab and/or Radiology automatically, a tech runs the ordered tests, and the patient comes back to a diagnostic room with the results. Lab and Radiology only run what a doctor ordered.
4. Pick the diagnosis from 600 real conditions. You need evidence first: at least half the patient's findings, at least one from an exam or test, and a lab or imaging result if the case has one. The chart shows a likelihood percentage for the top candidates, updated as each finding comes in. A wrong guess sends the patient home without paying.
5. Treat in a department that handles the condition, or transfer to another hospital. Bigger cases (surgery, heart attacks, strokes, sepsis, labor…) then recover in that department's recovery beds; discharge them when the stay ends to collect room charges.
6. With a Pharmacy open, choose the right OTC and prescription meds.

Every confirmed case goes into the **Casebook** with its findings, tests, treatment and standard prescription. Starting a new game clears it.

Insurance plans and patient names are fictional. Medical content is simplified for gameplay and is not medical advice.

## Running locally
It's a single file. Open `index.html` in any modern browser. Progress saves in the browser's local storage. The game runs on game time: 1 game minute is 15 real seconds at 1× (a 10-minute CT head takes 2½ real minutes). It pauses while the page is closed.

## Settings and Sandbox mode
Open **Settings** in the top bar to change the top bar color, turn the arrival sound on or off, start a **New game**, or switch on **Sandbox mode**, which adds tools to the sidebar: add money, unlock and staff every department, skip time, finish all running timers, clear reception, or add a patient with a specific condition. Click it again to hide the tools.

## Insurance

Patients arrive at random through the day. How many come is set by the insurance plans you accept: you start with five (Uninsured, Unity Health, Harbor Mutual, Cygnet Care, Bluepoint Shield) for about 100 patients per game day. The **Insurance** page lists all 19 plans. Each locked plan has a challenge, such as treating 30 patients in the ER for StateCare; finish it and the plan unlocks for free, adding its patients per day. A new patient's insurance is drawn from your accepted plans in proportion to the patients each one sends.

## Surgery

About 100 diagnoses are real operating-room surgeries (appendectomy, C-section, craniotomy, fracture fixation and so on). Once a doctor confirms one, the chart shows **Admit for surgery** instead of Start treatment. Admitting moves the patient to a recovery bed in that department. When an **operating room** ($10,000, up to 4 per department; the Emergency Room does not do surgery), a **surgeon** ($2,500 to hire), an **anesthesiologist** ($2,000 to hire) and a nurse are all free, the team operates automatically, then the patient recovers in the bed and is discharged as usual. Red patients stay critical until surgery starts.

## ICU and collapses
Urgent patients left waiting can **collapse**: a red alert bar names the patient and where they are, the department gets a ⚠ badge, and they have 15 minutes. The **ICU** has no queue or rooms, just beds (10 to start, more for $5,000 each). A patient in an ICU bed is stable, so their clock stops (the only place it does) while ICU nurses and doctors work them up, and ICU-treated conditions recover in the same bed.

## Account and cloud save

Open **Settings → Sign in with Google** on the GitHub site to save your hospital and Casebook to your account (Firebase Auth + Firestore, project `triage-ward`). The game saves to your account every 30 seconds while you play and when you leave the page. Signing in on another device loads whichever save is newest. Each person can only read and write their own save.

## Sound

A soft chime plays whenever a new patient arrives; red patients get a quicker three-note alert. The speaker button next to the hospital name turns it off or on, and the choice is remembered.

## Saving and pausing
The game saves itself to your browser every few seconds. Switching tabs, minimizing, locking your screen or closing the page pauses the hospital; it resumes when you come back. Saves live in each browser separately, so the Claude version and the GitHub version keep separate hospitals.

## Random events
One event happens each day you play, at a random moment 20 minutes to 2 hours into that day's session: a **bus fire**, **highway pile-up**, **ice storm**, **heat wave**, **flu season surge**, **food poisoning outbreak**, **pollen storm**, **music festival** or **chemical plant leak** sends extra patients with matching conditions; **ambulance diversion** brings 60% more of everyone; a **VIP patient** pays triple but waits only half as long; **medical students** make doctors 25% faster for a shift; or a **quiet holiday** slows arrivals. An amber banner shows what's happening and how long it lasts.

## Outpatient Clinic
Unlock the **Outpatient Clinic** ($8,000) for scheduled appointments: a random 1–4 booked patients per real hour (every 4 game hours) arrive on time, on top of the every-8-real-minutes walk-ins. Nurses do intake (interview, blood pressure, pulse oximetry, weight/BMI, immunization review); doctors do the annual physical, ear exam and skin check and can order labs. Visits include annual physicals, blood pressure and diabetes follow-ups, cholesterol, earwax, mole checks, warts, vitamin D, weight management, well-child visits and flu shots.
