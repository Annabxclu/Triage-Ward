# Triage Ward

A browser hospital-management game. Name your hospital, open with a free Emergency Room, and grow into 21 departments.

**Play:** https://annabxclu.github.io/Triage-Ward/ (once GitHub Pages is enabled)

## How a case flows
1. A patient reaches Reception every 5 game minutes (10 can wait). Name color is triage: red (30 min to live), yellow, green.
2. Read the complaint and send them to an open department. In the ER, assign a **triage room** and a named **nurse** for the first tests (vitals, ECG, swabs, urine and glucose checks), then move them to the **waiting room** or a **diagnostic room** where you assign a **doctor** to examine, diagnose and treat.
3. Run real tests to uncover hidden findings. A doctor can place **Doctor orders** for tests in other departments (e.g. *Complete blood count — Laboratory*, *CT head — Radiology*). Send the patient there, assign a named lab tech or rad tech, and they run the orders before you return the patient.
4. Pick the diagnosis from 73 real conditions. The chart shows a likelihood percentage for the top candidates, updated as each finding comes in. A wrong guess sends the patient home without paying.
5. Treat in a department that handles the condition, or transfer to another hospital. Bigger cases (surgery, heart attacks, strokes, sepsis, labor…) then recover in that department's recovery beds; discharge them when the stay ends to collect room charges.
6. With a Pharmacy open, choose the right OTC and prescription meds.

Every confirmed case goes into the **Casebook** with its findings, tests, treatment and standard prescription.

Insurance plans and patient names are fictional. Medical content is simplified for gameplay and is not medical advice.

## Running locally
It's a single file. Open `index.html` in any modern browser. Progress saves in the browser's local storage. One in-game day lasts 48 real minutes (a game minute is 2 seconds), and the game pauses while the page is closed.

## Test mode
Click **Test mode** in the top bar to open test tools in the sidebar: add money, unlock and staff every department, skip time, finish all running timers, clear reception, or add a patient with a specific condition. Click it again to hide the tools.
