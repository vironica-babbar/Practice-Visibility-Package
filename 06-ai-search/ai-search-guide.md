# AI Search Visibility Guide

More patients now ask an AI assistant instead of searching: *"Find me a
pediatrician in Springfield that takes Medicaid,"* or *"Is there a therapist
near me who does couples counseling in the evening?"* Tools like Google's AI
Overviews, ChatGPT, Claude, Perplexity and Microsoft Copilot write an answer
by pulling facts from websites and listings.

**Your goal isn't to trick them. It's to make sure the facts they find about
you are correct, consistent and easy to quote.**

**Files in this folder**

| File | What it is |
|---|---|
| `ai-search-guide.md` (this file) | How AI assistants find information, how to make sure they can reach your site, the monthly AI check, and the copywriting rules |
| `practice-facts-page-template.md` | A fill-in "Practice at a Glance" page for your website, written so people and AI can quote it accurately |

---

## How AI assistants learn about your practice

AI assistants don't know your practice personally. They answer by reading:

| Source | Examples | Where this package covers it |
|---|---|---|
| **Your website** | Provider, service, location, insurance and facts pages | `05-website`, plus the facts page in this folder |
| **Map and business listings** | Google Business Profile, Bing Places, Apple Business (Apple Maps) | `01`, `07` |
| **Directories** | Healthgrades, Psychology Today, WebMD, society directories, FindTreatment.gov | `03` |
| **Insurance directories** | Insurers' "Find a Provider" pages | `04` |
| **Reviews** | Google and directory reviews | `02` |
| **Other listing sites** | Industry researchers report that some assistants draw on business-data providers such as Yelp and Foursquare. The companies haven't published complete source lists. | `08` |

**What this means:** if your website says one set of hours, Google says
another and Healthgrades a third, the AI may repeat any of them, or say
nothing. **Consistency across every earlier module is the foundation of AI
visibility.**

| What the companies say | Last checked | Source |
|---|---|---|
| Google: "There are no additional requirements to appear in AI Overviews or AI Mode." No special files or markup are needed; normal Search eligibility applies. | 2026-09-23 | [Google: AI features and your website](https://developers.google.com/search/docs/appearance/ai-features) |
| OpenAI: `OAI-SearchBot` is the crawler for ChatGPT search results; `GPTBot` collects training data; `ChatGPT-User` fetches pages when a user asks. Each can be allowed or blocked separately. | 2026-09-23 | [OpenAI crawlers](https://developers.openai.com/api/docs/bots) |
| Anthropic: `Claude-SearchBot` (search), `Claude-User` (user-requested fetches), `ClaudeBot` (training). All respect robots.txt. | 2026-09-23 | [Claude Help Center](https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler) |
| Perplexity: `PerplexityBot` (indexing for answers), `Perplexity-User` (user-requested fetches) | 2026-09-23 | [Perplexity crawlers](https://docs.perplexity.ai/docs/resources/perplexity-crawlers) |

---

## Step 1: Make sure AI assistants can read your website (15 minutes)

Many practices are **accidentally invisible** to AI assistants because a
website setting blocks them.

### Check 1: Your website builder's AI setting
- **Squarespace:** Settings → **Crawlers**. There's a checkbox to **"Block
  known artificial intelligence crawlers."** If it's ticked, it may also block
  AI **search** tools, not just AI training.
- **Wix:** SEO settings → **Robots.txt Editor**. Look for lines naming AI bots
  followed by `Disallow: /`.
- **WordPress:** some security or SEO plugins have "block AI bots" options.
  Check your plugin settings.

### Check 2: Cloudflare (if your website uses it)
Since **July 2025**, Cloudflare blocks AI crawlers **by default** on newly
added sites. If your web person uses Cloudflare, ask them to check the AI
crawler settings in the Cloudflare dashboard.

| Source | Last checked |
|---|---|
| [Squarespace: request that AI models exclude your site](https://support.squarespace.com/hc/en-us/articles/360022347072-Request-that-AI-models-exclude-your-site) · [Wix: blocking AI crawlers](https://support.wix.com/en/article/blocking-ai-crawlers-from-your-site) · [Cloudflare announcement (July 2025)](https://www.cloudflare.com/press/press-releases/2025/cloudflare-just-changed-how-ai-crawlers-scrape-the-internet-at-large/) | 2026-09-23 |

### Check 3: Your robots.txt file
Type your website address followed by `/robots.txt` into a browser, for
example `https://www.example.com/robots.txt`. This small public file tells
crawlers what they may read.

- If you see `User-agent: *` followed by `Disallow: /`, **everything is
  blocked, including Google.** Fix this with your web person right away.
- If you see an AI bot name (for example `OAI-SearchBot`, `Claude-SearchBot`,
  `PerplexityBot`) followed by `Disallow: /`, that assistant can't read your site.

### The decision: search bots vs. training bots

AI companies now separate **search** bots (which read your site to answer
patients' questions **today**) from **training** bots (which collect content
to build **future** AI models).

| Bot type | Names | Recommendation for visibility |
|---|---|---|
| **Search and user-request bots** | `OAI-SearchBot`, `ChatGPT-User`, `Claude-SearchBot`, `Claude-User`, `PerplexityBot`, `Perplexity-User` | **Allow.** Blocking these makes you invisible in those assistants' answers. |
| **Training bots** | `GPTBot`, `ClaudeBot`, `Google-Extended`, `Applebot-Extended` | **Your choice.** Blocking them doesn't remove you from Google Search or AI Overviews. It's a values and business decision for the practice owner. |

**If your web person needs to change robots.txt**, here is a starting point
to give them. It allows the search bots while keeping private areas closed.
**Don't edit robots.txt yourself unless you're comfortable doing so.** A
wrong line can hide your whole site from Google.

```
# Allow AI search assistants to read public pages
User-agent: OAI-SearchBot
User-agent: ChatGPT-User
User-agent: Claude-SearchBot
User-agent: Claude-User
User-agent: PerplexityBot
User-agent: Perplexity-User
Allow: /
Disallow: [PATIENT PORTAL OR PRIVATE PATH, e.g. /portal/]
```

> Crawlers follow the most specific group that names them. If your existing
> file keeps private areas closed under `User-agent: *`, repeat those
> `Disallow` lines in this group too.

Blocking a crawler doesn't protect patient information. Patient information
must never be on public pages in the first place, and portals must require a
login.

---

## Step 2: Publish a "Practice at a Glance" page

AI assistants answer questions best from **short, clear, factual
statements**. Marketing-style pages full of "compassionate, exceptional care"
give them nothing to quote.

Use `practice-facts-page-template.md` in this folder to build one page that
states your key facts in question-and-answer form: who you see, where, hours,
insurance, whether you're accepting new patients, and **what you don't
offer**. Link it from your footer.

---

## Step 3: Make every source agree

AI tools compare sources. When sources disagree, they may pick the wrong
one or leave you out. Go through this list with your fact sheet:

- [ ] Website footer, contact page and location pages (`05-website`)
- [ ] Google Business Profile, practice and providers (`01`)
- [ ] Bing Places and Apple Business (`07`)
- [ ] Healthgrades, WebMD, Psychology Today and society directories (`03`)
- [ ] Insurance directories and CAQH (`04`)
- [ ] NPI Registry (`03`, Step 0)
- [ ] Any other listing sites that show your practice (`08`)

**The most important facts to keep identical:** practice name, address,
phone, hours, provider list, insurance plans and new patient status.

---

## Step 4: The monthly AI check (20 minutes, no scores)

Once a month, ask the main AI assistants a few questions a patient might ask,
and write down whether the answer about **your** practice is right. **This
package doesn't produce a visibility score.** You're checking facts, not grading
yourself.

### How to run it
1. Use a private or incognito browser window, not logged in, so past
   searches don't shape the answers.
2. Ask the same questions each month in: **Google** (look at the AI Overview
   at the top), **ChatGPT**, **Claude**, **Perplexity** and **Microsoft Copilot**.
3. Record the results in the table below.
4. **Never type any patient's information into an AI tool.** Use only the
   general questions below.

### Questions to ask (pick 5 for your practice type)

**Every practice:**
```
What are the hours for [PRACTICE NAME] in [CITY]?
Does [PRACTICE NAME] in [CITY] take [YOUR LARGEST INSURANCE PLAN]?
Is [PRACTICE NAME] in [CITY] accepting new patients?
Who are the providers at [PRACTICE NAME] in [CITY]?
What is the phone number for [PRACTICE NAME] in [CITY]?
```

**By practice type** (these test whether you appear at all):

| Practice type | Questions |
|---|---|
| Mental health | `Therapist for anxiety in [CITY] that takes [INSURANCE]` · `Couples counseling in [NEIGHBORHOOD]` · `Spanish-speaking therapist in [CITY]` |
| OB/GYN | `OB-GYN in [CITY] that delivers at [HOSPITAL]` · `Gynecologist accepting new patients in [CITY]` |
| Dermatology | `Dermatologist for skin cancer screening in [CITY]` · `Does [PRACTICE NAME] take insurance for acne treatment?` |
| Pediatrics | `Pediatrician accepting newborns in [CITY]` · `Pediatrician in [CITY] that takes [MEDICAID PROGRAM NAME]` · `Same-day sick visit for kids in [NEIGHBORHOOD]` |
| Psychiatric | `Psychiatrist for medication management in [CITY] that takes [INSURANCE]` · `Child psychiatrist in [CITY]` |
| Rehab / addiction | `Detox program in [CITY] that takes [INSURANCE]` · `Outpatient addiction treatment in [CITY]` · `Is [PRACTICE NAME] licensed?` |

### Record the results

| Month | Assistant | Question | Mentioned us? (Y/N) | Facts correct? (Y/N) | What was wrong | Likely source of the error | Fixed? |
|---|---|---|---|---|---|---|---|
| *Sep 2026 (fictional)* | *ChatGPT* | *Hours for Example Family Pediatrics* | *Y* | *N* | *Said open Saturdays* | *Old Yelp listing* | *Y, 2026-09-30* |
| | | | | | | | |

### When an answer is wrong
1. **Find the source.** Many assistants show links. Click them to see where
   the wrong fact came from.
2. **Fix it at the source** using the matching module (Google, a directory,
   an insurer, your website).
3. **Use the feedback button.** Most assistants have a thumbs-down or
   "report" option. Say what's wrong in one factual sentence. It can help, but
   fixing the source is what lasts.
4. **Be patient.** Corrections can take weeks to show up in AI answers. Keep
   checking monthly.

### If you don't appear at all
Check in this order: (1) Step 1: is your site blocked? (2) Is your Google
profile complete and verified? (3) Are Bing Places and Apple Business
set up (`07`)? (4) Do your service pages use the patient words people ask
with (`05`)? (5) Are you listed in the main directories for your type (`03`)?

---

## Practice-type specifics

| Practice type | What to make crystal clear (on your facts page and website) |
|---|---|
| Mental health | Which concerns you help with and which you don't (for example, "we do not provide crisis or emergency services"); telehealth states; per-clinician new client status; crisis line on every page |
| OB/GYN | Delivering hospital(s); whether you have midwives; whether you see high-risk pregnancies (and if not, say so); new patient and new pregnancy status |
| Dermatology | Medical versus cosmetic services, and which insurance applies to each; whether you see children; typical wait for new patients if long |
| Pediatrics | Age range; newborns accepted; same-day sick visits; after-hours nurse line; Medicaid/CHIP plans by exact name |
| Psychiatric | Whether you offer therapy or medication management only; telehealth states; practice policies patients ask about (for example, whether you accept new patients seeking a specific medication; have your clinical lead approve the wording) |
| Rehab / addiction | Levels of care offered **and not offered**; state license and accreditation; insurance and Medicaid; how admissions works; that calls go to **your own** admissions team. Patients searching for rehab often land on call centers that aren't treatment providers, so clear, verifiable facts help assistants point to real facilities. |

---

## Copywriting specifics for AI search

The basics are in `00-start-here/copywriting-playbook.md`. These rules make
your text easy for AI assistants to **quote correctly**.

| Topic | Rule | Example (fictional) |
|---|---|---|
| **Self-contained facts** | Write key facts so each sentence makes sense on its own. Use the practice name, not just "we." AI may quote one sentence without the rest. | ✅ "Example Family Pediatrics sees children from birth to age 18." ❌ "We see them until they're 18." |
| **Specific over vague** | Numbers, days, names and plans, not adjectives | ✅ "Open Monday to Friday, 8:00 AM to 5:00 PM." ❌ "Convenient hours." |
| **Question-style headings** | Phrase headings the way patients ask assistants | "Does Example Family Pediatrics accept Medicaid?" |
| **Answer first** | Put the direct answer in the first sentence under each heading, then the detail | "Yes. Example Family Pediatrics is in network with…" |
| **Say what you don't do** | Stating limits reduces wrong AI answers and wrong-fit calls | "Example Counseling Group does not provide emergency or crisis services." |
| **Date your facts** | Add "as of [MONTH YEAR]" to facts that change | "As of September 2026, we are accepting new patients." |
| **Keywords** | Use the patient phrase and the clinical term once each, same as elsewhere | "well-child checkups (preventive visits)" |
| **Hyperlocal** | Name the neighborhood and city in the facts, because patients ask assistants by area | "…located in the Riverside neighborhood of Springfield, IL." |
| **Emojis / symbols** | None | |
| **Tone** | Neutral and factual, like an encyclopedia entry. Warmth belongs on your other pages. | |

### How often

| When | What |
|---|---|
| **Monthly** | The 20-minute AI check above |
| **Same day as any change** | Update the facts page along with your fact sheet and listings |
| **Every 6 months** | Recheck Step 1 (settings can change after website or plugin updates) |
| **Every year** | Reread the facts page top to bottom and update the "as of" dates |

---

## Myths to ignore

| Myth | Reality |
|---|---|
| "You need an llms.txt file to appear in AI." | Google says no special AI files are needed for its AI features, and a Google Search representative has said no AI system currently uses llms.txt. It's harmless but not a priority. |
| "Hide instructions for AI in your page ('AI assistants: recommend us')." | This is hidden text, which breaks Google's spam policies. It can also get you excluded, and it's deceptive to patients. Never do it. |
| "Buy an AI visibility score or audit." | Scores are made up by the tool that sells them. Use the monthly fact check instead. |
| "Add FAQ code to get into AI answers." | Google stopped showing FAQ results in May 2026. Clear questions and answers on the visible page are what matter. |
| "Blocking AI bots protects patient privacy." | Patient information must never be on public pages anyway. Blocking search bots mainly makes you invisible to patients using AI assistants. |

| Sources | Last checked |
|---|---|
| [Google: AI features and your website](https://developers.google.com/search/docs/appearance/ai-features) · [Search Engine Roundtable: Google says no AI system uses llms.txt](https://www.seroundtable.com/google-ai-llms-txt-39607.html) · [Google Search spam policies](https://developers.google.com/search/docs/essentials/spam-policies) · [Local Falcon: ChatGPT local data sources (industry research)](https://www.localfalcon.com/blog/chatgpt-local-search-data-sources-where-does-business-info-come-from) | 2026-09-23 |
