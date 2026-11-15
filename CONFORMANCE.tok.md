# ilo Lighthouse — lipu pi nasin sama: toki tan ona sama (toki pona)

> **toki lili pi lipu ni:** lipu ni li lipu pi kulupu, li tan nasin NTARI "P2-002". lipu suli li lipu Inli "CONFORMANCE.md" (tenpo pi 2026-10-05). ilo sona li pali e lipu ni; kulupu li wile lukin e ona kepeken nasin "P2-002" kipisi "3.1".
>
> **Note:** This is a community rendering under NTARI policy P2-002. The complete document is the English original CONFORMANCE.md (snapshot 2026-10-05). Machine-assisted draft pending community review per P2-002 section 3.1.
>
> sina lukin e pakala lon toki ni la o pona e ona: o pali e "fork" lon
> https://github.com/NTARI-RAND/lighthouse, o pana e "pull request". pana sina
> li pona tawa mi mute.
>
> **lipu Inli li lawa.** lipu ni li tawa lukin, li tawa ala sona pi nasin lawa: lipu ni li ante tan `CONFORMANCE.md` la lipu Inli li lawa. nimi lawa (MUST, MUST NOT, SHOULD, SHOULD NOT, MAY), nimi pi poki sona, nimi sitelen en nimi ilo li awen lon toki Inli, tan ni: ona li lipu lawa pi nasin sama.

---

*ilo Lighthouse li toki e ni tan ona sama taso; ona li lon tenpo open (lipu open). nimi nanpa lon lipu nimi: `JFA/jfa-conformance-suite.py`. ilo Lighthouse li toki e nasin pona ona sama pi ijo luka tu lon lipu `lighthouse-seed.md` ("The standard"); lipu ni li pana e nasin pona ni lon lipu nimi pi nasin JFA, li toki lon e ni: seme li lon lipu nasin taso, seme li pali pini lon (jan li pali pini ala e ijo lon tenpo ni).*

**selo:** poki sona pi jan ale lon kipisi pi kama sona (kipisi VI); jan lukin li lukin e ona. tomo ("hub") pi kulupu ma li jo e ona. tomo ale li jo e pali tu: ilo lawa en jan lukin — ona li lukin tawa tomo ante; tenpo ala la ona li lukin e lipu awen ona sama.

| nimi nanpa (ID) / nasin awen | lon seme |
|---|---|
| lawa ala pi toki lon (kipisi VI) | **pona tan nasin (Met by design)** — ona li sitelen e ken ike, li toki ala e ike lon; ona li awen e toki lon lipu awen, li toki ala e ni: toki ni li lon; lon T4 la toki li toki e kama, li toki ala e lon; tomo ala, tomo suli ala, lukin ilo ala, ilo sona ala li pana e toki lawa pini |
| nasin pi toki tan lipu ante (citation) li ken lukin pona, li ken pali sin (forkable) (kipisi VI) | **pona tan nasin (Met by design)** — sitelen linja pi alasa sona (typed discovery graph) — linja ale li jo e nimi pi kulupu ona; ilo li pana lukin e ma tan pi ijo (provenance); ijo pali li lon poki pi jan ale (AGPL) — nimi ona li nanpa tan insa ona (content-addressed) |
| nimi pona li kama tan pali, li esun ala lon tenpo ale (kipisi VI) | **pona tan nasin (Met by design)** — jan li ken ala pana e mani tawa sewi lon lipu (paid placement); toki pi kama lon (attestation) li pali pona tawa jan, li nanpa sewi ala pi ken esun lon tenpo ale |
| toki li awen lon lipu awen sama toki taso (kipisi VI) | **pona tan nasin (Met by design)** — kulupu wan pi ijo tu wan (toki pi ijo lon/nasin pali/ijo pini) li awen e ijo pi kama insa en ijo pi kama weka lon lipu awen, li awen ala e toki lawa pini lon tenpo ale |
| COV-1 nanpa meso ala | **pona tan nasin (Met by design)** — nanpa ale li lon (full distribution), li kama ala nanpa wan; kulupu ijo ale li jo e sama ona ("sama lon tomo tu tu, ante lon tomo wan"); nanpa pi toki tan lipu ante li pana ala e suli awen tawa ijo |
| COV-3 sama tawa poka tu | **pona tan nasin (Met by design)** — jan li ken toki sin tawa toki ale lon lipu awen; utala li linja nanpa wan lon sitelen linja (first-class edges); weka pi utala li pana e toki poka; pakala li pana e toki poka, li weka ala e ijo lon tenpo ale |
| REC-1/3 lipu li kama suli taso, sona pi jan ("PII") li lon ala | **pona tan nasin (Met by design)** — sona pi selo en nanpa "hash" taso; ijo pali li kama pimeja (artifact-dark), li weka ala; sona pi jan ("PII") li lon ala poki pi jan ale |
| REC-6/7/8 lukin pi jan lukin, toki tawa sewi (filing upstream) | **lon lipu nasin (Designed)** — kulupu ala li lukin e lipu awen ona sama; jan li toki e ike lon tomo poka; nanpa lili pi kulupu tomo (federation) li tomo tu; anpa ona la nimi "stand-in" li lon |
| COV-6 awen tan nasin ike "Sybil" li kama lon tenpo open; suli tan toki (citation-weight) li kama lon tenpo kama | **pona tan nasin (tan nasin pi tenpo) (Met by design (by ordering))** — suli li pana ala e mute tawa ijo. ni li ante taso lon tenpo ni: kulupu lawa li open e ante (switch), jan lukin li lukin e ni; nanpa pi toki sama li nanpa tomo, li nanpa ala pi poki jan ("account"); jan li wile lon kepeken sijelo — ni li mani tawa wan ale |
| ECO-2/4/5 mani li kama insa esun | **lon lipu nasin (Designed)** — ona li pana e ken taso, li pana ala e mute lon tenpo ale; jan li kama jo tan pali, li esun ala e ona, li ken ala ante e ona tawa mani pi ma suli; sona pi lawa ma (regulatory read) li lawa e open pi ilo ni |
| GOV-9 lipu pi wile sona pi pini ala li lon, li ante lon tenpo ale | **pona (Met)** — `OPEN-QUESTIONS.md` li kama jo e kipisi IX; kipisi IX pi lipu open li ma tan pi toki ni |
| GOV-10 poki pi jan ale (copyleft) | **pona (Met)** — AGPL-3.0 (sitelen ilo), pana insa = pana weka (inbound = outbound), lipu CLA ala |
| pakala nanpa 2 / tenpo nanpa 0 | **jo e nimi (Named)** — lipu awen pi tomo tu lon kulupu tomo li kama lon ala la ijo ale sewi T1 li ken ala toki lon; lipu ni li lon ala la, nimi ale li tan toki pi ona sama taso |

**toki lon:** ilo Lighthouse li lipu open taso — linja ale lon sewi li lipu nasin, li sitelen ilo pi pali lon ala. nasin ona pi "tomo li jan lukin" li ilo *pi toki wile* tawa pakala nanpa 8 pi nasin JFA; jan o lukin e lon ona lon pali lon, o pilin ala e lon ona. nanpa lili pi open li tomo tu pi lawa ante; ijo li lili tan ni la ona li kama kepeken nimi "stand-in".
