# Interlinear audio study — עֲקֵדַת יִצְחָק in Yemenite Hebrew

An experiment in learning Hebrew **from Arabic**: Genesis 22:7–10 (the Akedah ·
قصّة الذَّبيح) read aloud in **Yemenite (Teimani) Hebrew**, the most conservative
surviving pronunciation — where **ח = ح**, **ע = ع**, **צ = ص**, **ק** is a hard
*g*, and **ו** is *w*.

**→ [Open the study page](https://diraneyya.github.io/hebrew-interlinear-study/)**

Click any word to hear that word alone, slowed, cut from the real recording.
Every word carries three lines — **Hebrew · pronunciation in Arabic letters ·
meaning in Arabic** — plus toggleable layers for the **root** (graded
solid / probable / speculative), the **pattern (وزن)**, and the **morpheme
breakdown**. A second button per verse plays the same text in **Modern Israeli
Hebrew** for comparison.

## Why this text

It is the Abrahamic story shared with Sūrat aṣ-Ṣāffāt, and the wording converges:

| Hebrew | القرآن (الصافّات ١٠٢) |
|---|---|
| **בְּנִי** | **يا بُنَيَّ** |
| אֱלֹהִים **יִרְאֶה**־לּוֹ | إنّي **أَرى** في المَنامِ |

Same roots, same scene. And the verse that follows carries **أَذْبَحُكَ** itself:

> **הַמִּזְבֵּחַ** ← ז־ב־ח = **ذ ب ح** → **مَذْبَح** — *the altar is the place-of-slaughter.*

Three **مَفعَل**-pattern nouns appear in two verses — **הַמָּקוֹם = مَقام**,
**הַמִּזְבֵּחַ = مَذْبَح**, **הַמַּאֲכֶלֶת = مَأكَلة** (the knife, *the instrument
of أكل*) — and the verb that names the whole story, **וַיַּעֲקֹד ← ع ق د**,
*and he bound him*. עֲקֵדָה = العَقْد.

Other cognates here: **יִצְחָק ← ضحك** (Isaac's name is a verb — *he laughs*),
**הַשֶּׂה = شاة**, **לְעֹלָה ← علا** (the offering is *what ascends*),
**יַחְדָּו ← واحد**, **שְׁנֵיהֶם ← اثنان**, **וְאַיֵּה = أين**,
**שָׁם = ثَمَّ**, **עַל = عَلى**, **וַיִּבֶן ← بَنى**.

## Credits

**Audio excerpt** (~21 s) from *“The Sound of the Yemenite Hebrew
language/dialect”* by the **[ILoveLanguages!](https://www.youtube.com/watch?v=ZUx9cUyHRZE)**
YouTube channel — please watch and support the original. Excerpted here for
non-commercial language study and cut into individual words. If the rights holder
objects, open an issue and it will be removed.

⚠️ ILoveLanguages sources volunteer speakers, so “Yemenite” is the channel's
attribution, not a documented tradition. The diagnostic is your own ear: a hard
**g** in *yiṣḥag* and a clean **ص** in *hāʿēṣīm* indicate a genuine Yemenite
reading.

Modern-Hebrew comparison audio synthesized with Microsoft `he-IL-AvriNeural`.

## How it was made

Whisper **fails completely** on this pronunciation — it garbled 87 seconds and
then hallucinated *תודה רבה* for a clean excerpt, because its acoustic model is
Modern Israeli and has never heard a pharyngeal ע. So the words were segmented on
**silence** instead, and the known text mapped onto the gaps. The alignment was
verified two ways: every segment's duration matches its word's length, and the
two largest gaps (0.42 s, 0.65 s) fall exactly at the ends of verses 7 and 8.

Built with `build_study.py` — whisper.cpp + ffmpeg, entirely local. The published
page is self-contained: all audio is embedded, nothing is fetched at runtime, and
it works offline.
