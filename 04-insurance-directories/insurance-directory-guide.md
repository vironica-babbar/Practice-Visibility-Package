# Insurance Directories Guide

Most insured patients start by searching their insurer's **"Find a
Provider"** directory. If you're missing, listed at the wrong address or
wrongly shown as "not accepting new patients," you're invisible to exactly
the patients most likely to book.

Insurance directories are also where **wrong listings cost you money**:

- **Patients can't find you**, or they call a number that no longer works.
- **Refunds:** under the No Surprises Act, if a patient relies on a
  directory that wrongly shows you as in-network, their cost is capped at
  in-network cost-sharing. A provider who collected more **must refund the
  difference, plus interest.**
- **Regulators are watching.** A 2023 U.S. Senate Finance Committee
  "secret shopper" study found that **more than 80%** of listed mental health
  providers it tried to reach in Medicare Advantage directories couldn't be
  reached, weren't in network or weren't taking new patients. These are
  called "ghost networks," and insurers are under pressure to clean them up,
  sometimes by removing providers who don't respond.

The copy-paste emails and data sheets are in `insurance-templates.md` in this
folder.

| Rules this guide relies on | Last checked | Source |
|---|---|---|
| No Surprises Act (2021): providers must send directory info to plans when a contract starts or ends, when info changes, and on request. Plans must verify at least every 90 days and update within 2 business days of receiving changes. | 2026-09-23 | [BCBS Kansas explainer](https://www.bcbsks.com/latest-news/understanding-provider-directory-requirements-no-surprises-act) · [MD Clarity](https://www.mdclarity.com/blog/no-surprises-act-provider-directory) · [AMA guide](https://www.ama-assn.org/system/files/2021-02/surprise-billing-provisions-guide.pdf) |
| Refund when a patient relied on a wrong directory | 2026-09-23 | [AOA No Surprises Act FAQ](https://www.aoa.org/practice/askaoa-webinar-series/no-surprises-act-good-faith-estimate-requirements-webinar/no-surprise-act-frequently-asked-questions) |
| Medicare Advantage: plans must update directories within 30 days of a change. Directory data now also feeds Medicare Plan Finder. | 2026-09-23 | [Federal Register, CY2026 rule](https://www.federalregister.gov/documents/2025/09/19/2025-18236/medicare-and-medicaid-programs-contract-year-2026-policy-and-technical-changes-to-the-medicare) |
| CAQH ProView re-attestation every 120 days (some states differ) | 2026-09-23 | [Grow Therapy CAQH guide](https://growtherapy.com/blog/caqh-setup-maintenance/) (third-party; check your CAQH account) |
| Senate "ghost network" study (May 2023) | 2026-09-23 | [Senate Finance Committee report](https://www.finance.senate.gov/imo/media/doc/050323%20Ghost%20Network%20Hearing%20-%20Secret%20Shopper%20Study%20Report.pdf) |

> State laws often add stricter directory rules on top of these. Ask your
> billing or credentialing lead which ones apply in your state.

---

## Where insurance directory data comes from

Insurers don't make up your listing. They build it from these sources, so
this is where fixes need to go:

| Source | What it is | Who usually manages it |
|---|---|---|
| **Your contract and credentialing file** with each insurer | The master record the plan keeps on you | Credentialing / billing lead |
| **CAQH ProView** | A shared online profile most insurers pull from | Each provider, or a delegate |
| **The insurer's provider portal or roster form** | Where you submit changes directly | Office manager / credentialing lead |
| **Behavioral health administrators** | Many health plans hand their mental health and substance use networks to a separate company. For therapists, psychiatrists and rehab programs, **the listing may live there, not with the health plan.** | Credentialing lead |
| **NPI Registry** | Some plans cross-check against it | Each provider (see `03-specialty-directories`, Step 0) |

**Key insight:** fixing a listing on an insurer's website alone often doesn't
stick. If CAQH still shows the old address, the next data pull puts it back.
**Always update CAQH and the insurer at the same time.**

---

## Step-by-step

### Step 1: List your insurers (15 minutes)
Ask your billing lead for every plan and network you're contracted with,
including Medicaid managed care plans, Medicare Advantage plans and
behavioral health administrators. Put them in the tracker in
`insurance-templates.md`.

### Step 2: Fill in one Provider Directory Data Sheet per provider
Template in `insurance-templates.md`. This is your "source of truth" for
insurers, in the same way the fact sheet is for everything else.

### Step 3: Search yourself like a patient
For each insurer, open its public "Find a Provider" page **without logging
in**. Search for each provider by name, and search by specialty and your ZIP
code. Check every field against the data sheet:

- [ ] Listed at all?
- [ ] Name and credentials correct
- [ ] Specialty correct
- [ ] **Only** at locations where the provider actually sees patients. Old
      or extra locations are a top cause of "ghost" listings.
- [ ] Phone reaches your scheduling line
- [ ] "Accepting new patients" status correct **for this plan and location**
- [ ] Telehealth shown correctly
- [ ] Languages, age range, hospital affiliations, accessibility
- [ ] Office hours

### Step 4: Submit corrections
Use the insurer's provider portal or roster update form if it has one
(preferred, because it leaves a record). Otherwise use the correction email in
`insurance-templates.md`. **Save a copy of everything you submit, with the
date.**

### Step 5: Update CAQH the same day
Log in to CAQH ProView, make the same changes, and **re-attest**.

### Step 6: Answer every verification request
Insurers must verify your data at least every 90 days, so they'll email,
call or send portal tasks. **Respond every time.** Providers who don't
respond can be removed from the directory.

### Step 7: Recheck in 30 days
Search again as a patient. If a correction hasn't appeared after 30 days,
follow up using the escalation template.

---

## Practice-type specifics

### Mental health clinics
- **Check two places:** the health plan's directory **and** the behavioral
  health administrator's directory. They are often different.
- Mental health listings get the most scrutiny for ghost listings. Keep
  "accepting new clients" status accurate **per clinician**, and update it
  the day a caseload fills.
- **Telehealth-only clinicians:** ask each insurer how they should be listed.
  Some plans have a telehealth-only designation, while others require a
  physical address.
- List each clinician's license type (LCSW, LPC, LMFT, PsyD, PhD) exactly as
  credentialed.

### OB/GYN clinics
- **Hospital affiliation is a key field.** Patients need both you **and** the
  delivering hospital in network. Check it on every plan.
- List certified nurse-midwives and nurse practitioners as individual
  providers, if the plan credentials them, so patients can find them.
- Medicaid managed care plans cover many pregnancies. Make sure you're listed
  correctly in each Medicaid plan you participate in.

### Dermatology clinics
- Directories cover **medical** dermatology only. Cosmetic services don't
  belong in insurance listings.
- "Accepting new patients" is often wrong at dermatology practices with long
  waits. If you're accepting patients but the wait is months, some plans let
  you add a note or appointment-availability field. Use it.
- List subspecialties, such as Mohs surgery or pediatric dermatology, if the
  plan has a field for them.

### Pediatric clinics
- **Age range** is a key field (for example, 0–18 or 0–21). A wrong age range
  hides you from searches.
- Medicaid and CHIP plans cover many children. Check your listing in each
  plan you participate in.
- Confirm that each pediatrician shows as a primary care provider (PCP) for
  plans that require patients to choose one. If not, families can't select
  you.

### Psychiatric clinics
- Like mental health, listings may sit with a **behavioral health
  administrator.** Check both.
- Psychiatric nurse practitioners should be listed under the plan's
  psychiatric or behavioral health specialty, not general nurse practitioner,
  where the plan allows.
- If the practice offers **medication management only** (no therapy), make
  sure listings don't imply therapy services.

### Rehab / addiction treatment facilities
- The **facility** usually needs its own listing (under the group NPI),
  separate from individual clinicians.
- List **levels of care** accurately (detox, residential, partial
  hospitalization, intensive outpatient, outpatient). Plans often have a
  specific field, sometimes using ASAM level names.
- Substance use benefits are often run by a behavioral health administrator.
  Check there too.
- Medication for opioid use disorder: if you provide it, make sure it appears
  in the plan's services field so patients can filter for it.

---

## Copywriting specifics for insurance directories

The basics are in `00-start-here/copywriting-playbook.md`. Insurance
directories are **mostly checkboxes and drop-downs**, so "copywriting" here
means choosing the right options and writing consistent, exact data.

| Topic | What to do |
|---|---|
| **Keywords** | Your **specialty choice** is your keyword. Pick the plan's exact specialty term for what you do (for example, "Psychiatry – Child & Adolescent," not just "Psychiatry"). Pick every *secondary* specialty or "area of focus" that's true, because each one is a search filter. |
| **Plan's words, not yours** | Insurance directories don't take creative wording. Use the plan's own terms for specialties and services, even if they sound clinical. Patient-friendly wording goes on Google and specialty directories. |
| **Free-text fields** | A few plans allow a short provider statement. Use the **short bio** from `03-specialty-directories/directory-bio-templates.md`, in third person, and leave out insurance lists (it's already their directory). |
| **Hyperlocal** | One listing per **real** location, with the suite number written exactly as in your fact sheet. For multiple offices, list the days each provider is at each one, if the plan allows. |
| **Phone number** | The number that reaches **scheduling**, not billing, a fax or a provider's cell phone |
| **Consistency** | Name, credentials, address and phone must match CAQH, the NPI Registry and your Google profile **character for character**. "Suite 200" versus "Ste. 200" can create a duplicate listing. |
| **Emojis / symbols** | Never. These are structured data fields. |
| **Tone in emails to insurers** | Short, factual, one request per email, with NPI numbers, the plan name and the exact correction. See the templates. |

### How often to work on insurance directories

| Frequency | Task |
|---|---|
| **When something changes** | Tell every insurer and update CAQH. The law requires providers to send updates on material changes, so do it within days, not months. |
| **Every 90 days** | Search yourself as a patient on each insurer's directory (a spot check). Respond to every verification request. |
| **Every 120 days** | CAQH re-attestation for each provider (check your account for your state's interval) |
| **Every year** | Reconfirm your plan list with billing; remove plans you've left |

---

## If you only have one hour

1. Search each provider on your **three largest** insurers' public directories.
2. Fix any wrong phone number, address or "accepting new patients" status.
3. Log in to CAQH for each provider and re-attest.
4. Put the next 90-day check on the calendar.

*This guide supports, but does not replace, advice from your credentialing
lead, billing team or attorney. Contract terms and state laws vary.*
