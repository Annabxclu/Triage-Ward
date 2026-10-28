# Triage Ward

A browser hospital-management game. Name your hospital, open with a free Emergency Room, and grow into 21 departments.

**Play:** https://annabxclu.github.io/Triage-Ward/ (once GitHub Pages is enabled)

## How a case flows
1. A new patient arrives every 5 minutes, straight into the open ward for their condition (or another ward that treats it, or the ER). Name color is triage: red (1 hour), yellow, green.
2. In every ward, assign a **triage room** and a named **nurse** for the first tests (vitals, ECG, swabs, urine and glucose checks), then move them to the **waiting room** or a **diagnostic room** where you assign a **doctor** to examine, diagnose and treat.
3. Run real tests to uncover hidden findings. A doctor can place **Doctor orders** for tests in other departments (e.g. *Complete blood count — Laboratory*, *CT head — Radiology*). Send the patient there, assign a named lab tech or rad tech, and they run the orders before you return the patient.
4. Pick the diagnosis from 524 real conditions. The chart shows a likelihood percentage for the top candidates, updated as each finding comes in. A wrong guess sends the patient home without paying.
5. Treat in a department that handles the condition, or transfer to another hospital. Bigger cases (surgery, heart attacks, strokes, sepsis, labor…) then recover in that department's recovery beds; discharge them when the stay ends to collect room charges.
6. With a Pharmacy open, choose the right OTC and prescription meds.

Every confirmed case goes into the **Casebook** with its findings, tests, treatment and standard prescription.

Insurance plans and patient names are fictional. Medical content is simplified for gameplay and is not medical advice.

## Running locally
It's a single file. Open `index.html` in any modern browser. Progress saves in the browser's local storage. The game runs on real time (a 20-minute CT takes 20 real minutes) and pauses while the page is closed.

## Test mode
Click **Test mode** in the top bar to open test tools in the sidebar: add money, unlock and staff every department, skip time, finish all running timers, clear reception, or add a patient with a specific condition. Click it again to hide the tools.

## ICU and collapses
Urgent patients left waiting can **collapse**: a red alert bar names the patient and where they are, the department gets a ⚠ badge, and they have 15 minutes. The **ICU** has no queue or rooms, just beds (10 to start, more for $5,000 each). A patient in an ICU bed is stable, so their clock stops (the only place it does) while ICU nurses and doctors work them up, and ICU-treated conditions recover in the same bed.

## Saving and pausing
The game saves itself to your browser every few seconds. Switching tabs, minimizing, locking your screen or closing the page pauses the hospital; it resumes when you come back. Saves live in each browser separately, so the Claude version and the GitHub version keep separate hospitals.

## Random events
One event happens each day you play, at a random moment 20 minutes to 2 hours into that day's session: a **bus fire**, **highway pile-up**, **ice storm**, **heat wave**, **flu season surge**, **food poisoning outbreak**, **pollen storm**, **music festival** or **chemical plant leak** sends extra patients with matching conditions; **ambulance diversion** brings 60% more of everyone; a **VIP patient** pays triple but waits only half as long; **medical students** make doctors 25% faster for a shift; or a **quiet holiday** slows arrivals. An amber banner shows what's happening and how long it lasts.

## Outpatient Clinic
Unlock the **Outpatient Clinic** ($8,000) for scheduled appointments: a random 1–4 booked patients per hour arrive on time, on top of the every-5-minutes walk-ins. Nurses do intake (interview, blood pressure, pulse oximetry, weight/BMI, immunization review); doctors do the annual physical, ear exam and skin check and can order labs. Visits include annual physicals, blood pressure and diabetes follow-ups, cholesterol, earwax, mole checks, warts, vitamin D, weight management, well-child visits and flu shots.
