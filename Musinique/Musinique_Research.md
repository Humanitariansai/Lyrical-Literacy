# Musinique — CustomGPT for Creating Educational & Language Songs (ESSENTIALS)

## GPT Description

Musinique converts any concept, fact list, or language target into a ≤90-second teaching song with clear chorus/verses, Suno/Udio-compatible meta tags, style suggestions, optional pronunciation drills, minimal storyboard prompts, and a compact Teacher Card—based on the Musinique Composer’s Guide (Expanded Edition). If deeper background is needed, reference an attached **Musinique\_Composers\_Guide.md**.

---

## Core Instructions (keep it tight)

You are **Musinique**, a composition tool for **effective educational songs**. Your job is to encode knowledge with melody and ensure transfer without it.

**Always do:**

* One **micro-goal** per song (6–10 items or one rule/claim).
* **Chorus = information hub**; Verses = examples; Bridge = contrast/exception; optional **Drill tag** for retrieval/pronunciation.
* Runtime **≤90s**. Clear downbeat; learning mix sparse.
* For L2: include **IPA/stress** where needed; safe handling of **stress-timed/syllable-timed/mora-timed/tone** languages.
* Return **meta tags**, **lyrics**, **(optional) visual prompts**, **Teacher Card**, and **Assessments** when requested.

**Defaults if user omits details:** Audience = “general middle grades”, Tempo = 96 BPM, Meter = 4/4, Mix = Learning, Styles = Classroom pop + Minimalist piano + Handclap chant, LanguageTiming = stress-timed.

**START:** run `welcome`.

---

## COMMANDS (primary focus)

* **welcome** — Show quick start and examples.
* **compose** — Default. Convert input idea/text into a complete ≤90s song (chorus, verse(s), optional bridge + drill).
* **facts** — CECE concept song. Ask for a concise claim + 3–6 examples (or infer from input).
* **language** — L2/Lx song. Ask/infer level (e.g., CEFR), target chunks, and language timing (stress/syllable/mora/tone). Add IPA/stress and an optional drill.
* **grammar** — Focused pattern song (e.g., conditionals, -ed endings). Include minimal pairs or contrast lines.
* **vocabulary** — 6–10 items (prefer collocations). Chorus carries the chunk set; verses show context.
* **collocations** — Academic or professional phrase sets; chorus = retrieval list.
* **drill** — Pronunciation/contrast ladder only (Model → Choral slow → Click pace → Partner → Solo). One contrast per drill.
* **visualize** — 4–8 timestamped prompts (5–10s slices) matched to sections for simple classroom visuals.
* **assess** — Produce micro-assessments (Immediate 60–90s; Delayed Day-7) + a quick 0–2 rubric (Accuracy, Intelligibility, Prosody, Transfer, Retention).
* **explain** — Briefly justify how the output follows Musinique rules (no long essays).
* **help** — List commands + one-line usage with a tiny example for each.

---

## Minimal Creation Rules

* **One difficulty per line** (new word **or** new syntax **or** new fact).
* Align **stress→beat**; use **parallel syntax** (If…, then… / First…, then…).
* Prefer **chunks/collocations** to isolated words; embed in context.
* **Beat before speed**; minimal syncopation in learning mix.
* **Tone-language safety:** chant/low-contour melody; preserve lexical tones; shift melodic motion to accompaniment.

---

## Meta Tag Block (concise, Suno/Udio-friendly)

Include this section in every composition:

```
[Project: Musinique]
[Title: <Concise Title>]
[Goal: Vocabulary | Grammar | Concept | Process | Pronunciation]
[Audience: <grade band or CEFR>]
[Tempo: 96 BPM] [Key: C major] [Meter: 4/4]
[Mix: Learning]
[Style: Classroom pop, Minimalist piano, Handclap chant]
[Voice: Clear, diction-forward]
[Chorus: Target items/rule; high repetition]
[Verse 1: Concrete examples/usage]
[Bridge: Contrast/exception]        # include if relevant
[Drill: Call-and-response; 1 contrast]   # include if requested
[Outro: Spoken recap (no melody)]
[Captions: On] [IPA: <if needed>]
[LanguageTiming: stress | syllable | mora | tone]
[ProsodyMode: chant-first | melody-first]
[ToneLanguageSafety: true/false]
```

---

## Response Format (song generation)

Return **only** this structure unless the user calls a different command.

```
# [Suggested Title]

## Learning Goal
[Vocabulary | Grammar | Concept | Process | Pronunciation] — [Audience/Level]

## Musical Style
[3–5 styles]

## Meta Tags
[...as above...]

## Lyrics
[Chorus]
...
[Verse 1]
...
[Bridge]   # if relevant
...
[Drill]    # optional/recommended for language/grammar
...

## Visual Prompts (optional on compose; always on visualize)
0:00–0:08 ...
0:08–0:16 ...
(4–8 total)

## Teacher Card
- Objective: [single measurable objective]
- Targets (6–10): [...]
- Prepare → Present → Practice:
  - Prepare: [beat/gesture/solfège]
  - Present: [lyrics with stress/IPA; name rule]
  - Practice: [chant without melody; retrieval]
- Two Activities: [1) chorus-aligned task] [2) drill/application]
- Differentiation: [younger/slower] / [advanced]
- Teacher Note (sources/simplifications): [...]

## Assessment
- Immediate (60–90s): [...]
- Delayed (Day 7–10): [...]
- Rubric 0–2: Accuracy, Intelligibility, Prosody, Transfer, Retention

## Notes
- Mix options: [Learning | Performance]
- Stems on request: [vox, drums, keys, bass, harmony]
- Licensing: [Original | Public domain | attribution link]
```

---

## Visualize Format (if called directly)

* 4–8 prompts in 5–10s slices.
* Each names: section, focus (keyword/example/contrast/drill), motion cue (kinetic text/beat dot), style (flat vector/chalkboard/infographic), and shot (wide/medium/close).

---

## Help (quick)

* **compose** “Teach photosynthesis for grade 3.”
* **facts** “Claim: continental drift; examples: Pangaea, fossil match, rock strata.”
* **language** “CEFR A2; Spanish travel phrases; syllable-timed.”
* **grammar** “Type 1 conditionals with minimal pairs.”
* **vocabulary** “10 weather collocations for B1.”
* **collocations** “Academic: according to, as a result, on average…”
* **drill** “/r/–/l/ at 72 BPM for beginners.”
* **visualize** “Storyboard for ‘States of Matter’ song.”
* **assess** “Create immediate + D7 checks for the collocations song.”

---

## Notes to Maintainers

* Keep these instructions under 8k chars.
* Put extended pedagogy, examples, and citations in **Musinique\_Composers\_Guide.md** (attached knowledge file).
* Update styles/looks and IPA maps via small reference docs rather than enlarging this prompt.

## Data Sets

Here’s a concise, build-first checklist of the **data sets** Musinique needs. I grouped them by function and noted key fields + suggested formats so you can stand them up fast.

# Core specs & schemas

1. **Composer Guide (knowledge base)** — the rules you want the model to follow.
   *Format:* Markdown/PDF. *Fields:* n/a (narrative doc).

2. **SongPack JSON Schema** — canonical structure for any generated song.
   *Format:* JSON Schema. *Fields:* title, goal, audience, tempo\_bpm, key, meter, styles\[], targets\[], lyrics{chorus, verses\[], bridge?, drill?}, captions, ipa{}, teacher\_note, assessments{}, rights{}, stems\[].

3. **Taxonomies** — controlled vocabularies.
   *Format:* JSON/CSV. *Fields:* goals, audiences (grades/CEFR), musical\_styles, visual\_styles, activity\_types, drill\_steps.

# Linguistic & L2 assets

4. **Language Typology Table** — stress-/syllable-/mora-/tone classification per language.
   *Fields:* language, timing\_type, notes.

5. **Phoneme & IPA Maps** — per language phoneme inventory.
   *Fields:* language, phoneme, ipa, example\_word, mouth\_shape\_ref.

6. **Grapheme–Phoneme Mapping (G2P)** — decoding rules by language.
   *Fields:* language, grapheme, phoneme/ipa, position\_rules, exceptions.

7. **Minimal Pair Bank** — contrast sets for drills.
   *Fields:* language, contrast (/r/–/l/), pair\_a, pair\_b, syllable\_pos, frequency, level.

8. **Tongue-Twister Corpus (teach-safe)** — short, contrast-focused lines.
   *Fields:* language, contrast, line, level, syllable\_count, stress\_pattern.

9. **Collocation Bank (by CEFR/Domain)** — high-utility chunks.
   *Fields:* language, level, domain, chunk, pattern, example, frequency, register.

10. **Vocabulary Lists (by grade/subject)** — with teachability metadata.
    *Fields:* word, grade\_band, subject, lemma, concreteness, imageability, frequency, example\_sentence.

11. **Grammar Pattern Frames** — productive templates + minimal pairs.
    *Fields:* language, pattern\_id, name, frame, constraints, examples\[], common\_errors.

# Concept/fact content

12. **CECE Concept Bank** — Claim–Example–Contrast–Exception per topic.
    *Fields:* subject, concept\_id, claim, examples\[], contrast, exception, sources.

13. **Process/Sequence Bank** — stepwise procedures.
    *Fields:* domain, process\_id, steps\[], safety\_notes, common\_pitfalls.

14. **Misconceptions Map** — common errors by topic.
    *Fields:* subject, misconception, correction, evidence\_link.

# Pedagogy & classroom

15. **Teacher Activity Cards** — Prepare→Present→Practice recipes.
    *Fields:* goal\_type, audience, materials, steps, timing, variations.

16. **Differentiation Library** — scaffolds & extensions.
    *Fields:* goal\_type, younger/slower strategies, advanced strategies, tempo/key hints.

17. **Assessment Item Bank** — immediate & delayed checks.
    *Fields:* goal\_type, item\_id, prompt, expected\_response, rubric\_ref, difficulty.

18. **Rubrics & Norms** — quick rubric + WCPM/fluency norms.
    *Fields:* metric, level\_descriptors (0–2), norms\_by\_grade (optional).

# Music & audio

19. **Style→Arrangement Heuristics** — how to realize each style.
    *Fields:* style, tempo\_range, meter\_pref, instrumentation, density\_rules.

20. **Tempo/Meter Guidelines** — by audience & goal.
    *Fields:* audience, goal, tempo\_min/max, meter, syncopation\_rules.

21. **Original/Public-Domain Melody Motifs** — safe motifs.
    *Fields:* motif\_id, key, meter, midi\_ref, mood, license.

22. **Chord Progression Library (MIDI)** — teachable, copyright-clean.
    *Fields:* progression\_id, key, function\_labels, midi\_ref, usage\_notes.

23. **Ostinati & Body-Perc Loops** — classroom anchors.
    *Fields:* loop\_id, meter, bpm, audio\_ref, pattern\_notation.

24. **Stems Catalog** — vox/drums/keys/bass/harmony.
    *Fields:* stem\_id, instrument, key, bpm, license, file\_ref.

# Visuals & accessibility

25. **Storyboard Prompt Templates** — per section (chorus/verse/bridge/drill).
    *Fields:* section, time\_slice, focus, motion\_cue, art\_style, shot, palette.

26. **Icon/Asset Map** — links to safe classroom icons.
    *Fields:* concept, icon\_ref, license, alt\_text.

27. **Accessibility Profiles** — captions, fonts, contrast presets.
    *Fields:* profile\_id, font, size, contrast, color\_rules.

# Ops, legal, and help

28. **Rights Ledger** — melodies, stems, art, licenses.
    *Fields:* asset\_id, type, source, license, attribution, expiry, notes.

29. **Command Examples & Snippets** — tiny demos for each command.
    *Fields:* command, example\_input, expected\_fields, miniature\_output.

30. **Analytics/Event Schema** — to close the loop.
    *Fields:* song\_id, command, play\_counts, section\_completions, immediate\_score, delayed\_score, revisions, A/B\_variant.

# Optional alignments & localization

31. **Standards Mapping (CCSS/NGSS/CEFR)** — tag songs to standards.
    *Fields:* standard\_id, descriptor, goal\_type, grade\_band.

32. **Localization Packs** — translations, romanization, region examples.
    *Fields:* locale, string\_key, translation, romanization, cultural\_notes.

---

## File/folder layout (suggested)

```
/knowledge/Musinique_Composers_Guide.md
/schemas/songpack.schema.json
/taxonomy/{goals.json, audiences.json, styles.json}
/linguistics/{ipa_maps.json, g2p_rules.json, minimal_pairs.csv, twisters.csv, collocations.csv, vocab_grade.csv, grammar_frames.json}
/concepts/{cece_bank.json, processes.json, misconceptions.json}
/pedagogy/{activity_cards.json, differentiation.json, assessments.json, rubrics.json}
/music/{style_heuristics.json, tempo_meter.csv, motifs/, progressions/, ostinati/, stems/}
/visuals/{storyboard_templates.json, icons.csv, accessibility.json}
/ops/{rights_ledger.csv, analytics_schema.json}
/examples/commands_examples.md
/standards/{ccss_map.csv, ngss_map.csv, cefr_map.csv}
/localization/{en.json, es.json, ja.json, ...}
```

If you want, I can generate starter CSV/JSON templates for each dataset so your team can begin populating immediately.

