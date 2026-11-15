# ilo Lighthouse — suli pi toki sona: lipu lawa pi pini ala (toki pona)

> **toki lili pi lipu ni:** lipu ni li lipu pi kulupu, li tan nasin NTARI "P2-002". lipu suli li lipu Inli "lighthouse-weight-tiers.md" (tenpo pi 2026-10-05). ilo sona li pali e lipu ni; kulupu li wile lukin e ona kepeken nasin "P2-002" kipisi "3.1".
>
> **Note:** This is a community rendering under NTARI policy P2-002. The complete document is the English original lighthouse-weight-tiers.md (snapshot 2026-10-05). Machine-assisted draft pending community review per P2-002 section 3.1.
>
> sina lukin e pakala lon toki ni la o pona e ona: o pali e "fork" lon
> https://github.com/NTARI-RAND/lighthouse, o pana e "pull request". pana sina
> li pona tawa mi mute.
>
> **lipu Inli li lawa.** lipu ni li tawa lukin, li tawa ala sona pi nasin lawa: lipu ni li ante tan `lighthouse-weight-tiers.md` la lipu Inli li lawa. nimi lawa (MUST, MUST NOT, SHOULD, SHOULD NOT, MAY), nimi pi poki sona, nimi sitelen en nimi ilo li awen lon toki Inli, tan ni: ona li lipu lawa pi nasin sama.

---

lipu ni li lon anpa pi nasin JFA (Janus-Facing Architecture). suli wan li **ijo lon pi nasin insa, li toki e toki sama tan jan ante**, li toki ala e ni: ijo li lon anu lon ala. jan li nanpa e suli kepeken **wan pi tomo pi lawa ante**: tomo ("hub") li wan pi nanpa, poki jan ("account") li wan ala; jan li lukin e lawa ante lon nasin insa, li weka e tomo pi lawa sama. nasin pi suli li **nasin lawa, li ilo ala** — ona li lon sama sona pi nasin lawa (jan li ken lukin e ante ona), li tawa lipu awen pi jan lukin, li jo e toki pi ante ona kepeken nimi pi jan ale, la wile sona ni li jo e toki tan jan lukin lon tenpo ale: "tenpo pi sitelen ni la nasin seme pi suli li lawa?" sitelen ale pi suli li jo e lipu pi pana sona: pali sin seme, tomo seme, kipisi seme pi toki sama, nanpa seme pi nasin lawa pi suli. toki sona en pali sin ona li **linja pi nimi kulupu**, li ante tan sitelen pi esun en sitelen pi lawa utala; jan lukin ala li ken nasa e ona.

---

## T0 — Anchored (toki li lon lipu awen)

toki sona li lon lipu awen pi jan lukin sama ijo tu wan pi wan — **toki pi ijo lon, nasin pali, ijo pini** — tan jan toki pi nimi pona, lon tomo, lon nasin pi lipu awen: jan li ken taso pana e ijo sin lon pini ona, jan lukin pi lawa ante li lukin e ona, ona li tawa monsi ala. pana awen li pana e **ijo lon pi nasin insa en nimi tawa ijo taso**: nanpa ("hash") pi insa pi ijo tu wan, nimi pi kulupu toki, nimi pi nanpa pi nasin pali, sitelen tenpo, nimi len pi jan toki, nimi pi tomo. ijo ni sama — lipu pi nasin pali, sona nanpa — li tawa poki pana pi jan ale (nasin "AGPL"); jan li alasa e ona kepeken nanpa pi insa ona, tomo li pana e ona; lipu nanpa awen li jo e nanpa ("hash") taso.

- kipisi pi toki awen (Covenant) li lawa e ken pi pana awen: nimi pona pi jan li toki e ni: poki jan li **ken ala ken** pana awen; ona li toki ala e mute, li toki ala e ni: jan mute li ken lukin e ona anu seme.
- lon li supa anpa taso, li ijo ala pi pana lon. jan lukin li ken sona e ni: toki ni, kepeken nasin pali ni, li lon lon tenpo ni, tan poki jan pi nimi pona lon tenpo ni. jan lukin li ken ALA sona e ni: jan li lukin pona e ona, ona li ken lon, ona li lon.
- jan li ken toki tawa pana awen ale. jan ale li ken pana awen e utala tawa ona; jan toki li toki ala la tenpo awen ("dwell") li kama suli — ni li ijo lon ken lukin, ilo li lawa ala e ona.
- jan li ken ala kama jo e ijo la pana awen li weka ala; toki sona li sitelen kepeken nimi "artifact-dark" — ni kin li ijo lon ken lukin.
- tenpo kama la jan toki li pakala e kipisi pi toki awen la, ni li **pana e toki lili lon poka pi pana awen ona, li weka ala e ona**. jan pi toki lon ala li ken toki e ijo lon; pali sin pi toki ona li awen lon lipu awen pi pali sin ni.

nasin pi musi ike: pali mute mute pi pana awen. awen: T0 li pana ala e suli; pana awen ale li open tawa utala lon anpa pi kipisi pi toki awen; tomo li ken lili e mute pi pana awen lon tenpo, sama nasin lawa pi tomo ni, lon lipu tawa jan ale.

## T1 — Cited (jan ante li toki e ona)

pana awen ante li toki e toki sona. toki tan ("citation") li **linja pi nimi kulupu** — extends, uses-procedure, disputes, mentions — en nimi kulupu pi linja li sona pi nasin lawa. toki tan li sitelen e **sitelen linja pi alasa sona**: kepeken ona la jan li alasa e toki sona, li lukin e ona, li utala e ona lon tomo mute.

- nanpa pi toki tan li MUST NOT tawa insa pi suli, pi nasin nanpa tawa pana pona, anu pi ken kama — **lon tenpo ale**, li awen ala e ijo kama. tenpo ni en tenpo kama la, pali pi toki tan li wile e mani lili lili taso; sitelen li wile ala e mani la ona li ken ala pana e suli.
- linja *disputes* li suli sama linja ale, li lon poka pi linja *extends* lon sitelen. sitelen linja li weka ala e ona tu kepeken nanpa.
- lupa pi alasa sona li MUST sitelen e ma open — jan seme li toki tan, tan tomo seme — la sike pi toki tan li ken lukin sama selo. ilo pi lukin e ijo pi pona nasa mute (too-clean scan) li lukin e kipisi linja pini sama ijo pi sitelen ike ("flag"); sitelen ike li pana tawa utala, li weka ala e ijo.

jan lukin li ken sona e ni: jan li lukin e ona, ona li jo e linja tawa ijo ante. jan lukin li ken ALA sona e toki sama tan jan ante. toki tan li alasa e toki sona; ona li toki ala e ni: toki sona li lon.

## T2 — Replicated in-hub (jan li pali sin lon tomo sama)

poki jan ante (ona li jan toki ala) li lon lipu nimi pi **tomo pi jan toki sama**, li pali e nanpa pi nasin pali, e nanpa ni taso, li pana awen e **pali sin**: nimi pi nanpa pi nasin pali, nanpa ("hash") pi ijo pini ona sama, en **toki ona pi sama** — consistent (sama), inconsistent (sama ala), anu inconclusive (sona ala) — ni li toki ona sama: jan li ken toki tawa ona, li ken utala e ona sama pana awen ale.

- pali sin ale lon tomo sama li **kama wan pi tomo wan**; poki jan li mute ala mute la ni li sama. kama wan ni li awen tan nasin ike "Sybil": poki jan len li kama jo e ala, nanpa li awen pona, ilo li wile ala alasa e jan lawa.
- poki jan pi jan toki sama li weka; lawa sama pi poki jan li ken lukin lon nasin insa la, ona kin li weka — taso nasin pi kama wan li awen e pona, alasa li awen ala e ona.
- T2 li pana e nasin insa e sitelen, li pana ala e ken kama. pali ona li nasin open: ona li pana e sona ni: **luka ante li ken pali e nasin pali, luka pi jan pali ona taso ala**; ona li suno e pakala pi nasin pali kepeken mani lili, lon tenpo pi pali ala lon tomo ante.

jan lukin li ken sona e ni: jan li ken pali e ona, jan lon tomo ni li wile sona e ona. jan lukin li ken ALA sona e toki lon tan lawa ante — tomo sama li jo e ilo sama, e wawa sama pi kulupu jan, e ma sama pi lukin ala.

## T3 — Replicated cross-hub (tomo ante li pali sin)

pali sin pi pana awen li lon tan tomo pi **lawa ante lon nasin insa** tan tomo pi jan toki. suli ni li jo e nanpa pi wan tomo — nanpa pi tomo ante pi lawa ante, tomo ale ni li jo e pali sin pi pana awen wan anu mute — li awen **lon kulupu wan wan pi toki sama**: "consistent lon tomo 4, inconsistent lon tomo 1" li tawa jan sama ni, lon tenpo ale. ni li nasin pi nanpa meso ala, lon sona.

- jan li lukin e lawa ante lon nasin insa, lon mute pi tomo: tomo tu ale li jo e lawa ante. jan pali sama, jan lawa sama, kulupu lawa mama sama — ona li weka. **tomo lipu lili luka luka pi kulupu tomo lipu wan pi ma lili li wan taso.**
- linja pi jan lukin li linja lawa ala. tomo li sitelen e nimi ona lon lipu pini lili ("checkpoint") pi tomo ante la, ona li awen jan pi toki sama pi lawa ante; ni li lon ala la, tomo poka pi kulupu tomo li ken ala toki sama tawa ona, kulupu linja lili li moli lon tenpo open ona.
- tomo li ken wan lon nanpa lon tenpo ni taso: jan lukin li lukin lon e lipu awen ona — jan lukin tu anu mute pi lawa ante; ilo open ona sama li jan lukin ala. pali sin pi tomo sin li lon anpa pi **nimi "stand-in"** lon tenpo pi lukin lon ala: kama sona li kama lon tenpo mute, sama sama kipisi lawa (Governance).
- pali sin lon li pana e ijo pi sama ala. toki sama pi pona nasa mute lon tomo pi lawa ante (jan li toki e ni) li ijo pi sitelen ike tan ilo lukin — ni li sitelen pi esun len, lon sona.
- jan li toki ala tawa sama ala la, tenpo awen ("dwell") li kama suli lon toki sona open — ona li ken lukin, ilo li anpa ala e suli ona.

nasin pi musi ike: tomo sin len, tan ni: nasin "AGPL" la jan ale li ken open e tomo. awen: tomo li kama wan lon nasin insa taso — lipu awen pi jan lukin, weka pi lawa sama, "stand-in" lon tenpo pi kulupu tomo ala — la tomo len li wile e mani sama tomo lon.

## T4 — Attested (tomo li toki e kama)

tomo li pana awen e **toki pi kama** kepeken ilo open pi kulupu ona: nanpa ni pi nasin pali li kama lon tomo ni, lon tenpo suno ni, lon tenpo pali ni, tan nimi ni pi poki jan. **kama taso, lon ala** — tomo li toki e kama ni: ona sama li jo e kama ni lon tomo ona; ona li toki ala e sona pi kama. ijo pini en toki pi sama pi jan pi pali sin li awen pana awen ante ona sama, li jo e linja tawa ona.

- toki pi kama pi lon ala li pakala pi tomo sama lon kipisi pi toki awen — jan li ken lawa e ona, li lukin e ona sama nasin insa; ona li pana tawa lukin pi pali pi jan lawa tomo, lukin ni li lawa e nimi pona tomo. toki pi kama li jo e wawa, tan ni: nimi pona pi kulupu li lon monsi ona.
- jan li nanpa e ona kepeken wan tomo sama T3: pali mute pi toki kama lon tomo wan li wan taso. nanpa pi pali li sitelen sama ijo lili, li pana ala e suli.
- **toki pi kama li pali pona tawa jan; ona li pana ala e ken.** tomo li ken wile ala jo e nasin pali, li ken wile ala toki e kama ona — nasin tenpo, lukin lawa, en wile pi awen pona pi jan li nasin lawa pi tomo, li lon lipu tawa jan ale — en toki sona pi wile ala li weka ala e ijo lon ma ante: ona li pana awen lon T0, li tawa lon sitelen linja lon T1, li kama toki sama lon tomo ante lon T3. awen pona pi tomo li pali e pona pi pakala ala, la insa ala li kama lawa pi lon anu lawa pi ijo insa.
- tomo li MUST NOT toki e kama pi pali tan poki jan lon anpa pi lawa ona — jan lawa ona, jan pali ona lon pali tomo. lon suli ni la pali mani li linja lawa; wan pi toki kama tan ona sama li sama ni: soweli li nanpa e waso ona: ona li nanpa ala (0), li jo e nimi.
- mani pi pali e suli ni li **sijelo jan en tenpo suno** — tomo sin li wile e mani sama, mute li lili ala e mani. nasin ni pi mani sama, lukin pi nimi jan ala, li nasin mani pi "Sybil".

jan lukin li ken sona e ni: kulupu pi lawa ante li pana e nimi pona ona tawa ni: kama li kama lon. jan lukin li ken ALA sona e ni: ijo pini li pona — ona li ken sona e ni taso: pali len li wile e tenpo suno lon tan kulupu lon, mute mute.

---

## nasin awen pi suli ale

- **linja pi nanpa nasin.** pali sin li linja tawa nanpa pi nasin pali: ona li pali e nanpa ni. nasin pali pona sin li pana awen sin, li toki tan nasin pini; suli pi nanpa ale li kama lon nanpa ni taso, jan li ken lukin e linja ale. ni li lon ala la suli li kama lon v1, taso v2 li tawa jan lon anpa ona, jan li sona ala.
- **toki sama li sona; pakala li pali jan.** pali sin pi sama ala li ijo lon pi toki sama, li toki ike ala tawa jan, li tawa ala nasin pi toki pi pakala. pali jan taso — pali pi ijo len, toki lon ala pi pali, toki pi kama pi lon ala — li tawa linja toki pi kipisi pi toki awen. **pilin ante li pakala ala.** linja tu li awen tu la, toki pi pakala li kama ala ilo utala lon utala sona.
- **ken kama taso, suli mani ala.** suli li lawa e ni: toki sona li ken ala ken kama jo e mani tan kipisi esun; selo — T3 en sewi, anu T4 taso lon tenpo pi ante — li nasin lawa pi kulupu, li nasin pi suli ala. suli pi mani pana li tan esun lon (ona li pana e mani tawa esun ni); esun ni li jo e wawa ike pi esun, suli li ken ala jo e ni.
- **sitelen wan ala.** nanpa wan ala, mun ala, sitelen "verified" ala. suli li sitelen lon poka pi lipu pana sona ona: pali sin, tomo, kipisi pi toki sama, nanpa pi nasin lawa lon tenpo ni.

## wile ni la o pana ala, anu o pana e sitelen ike

- *"o pana e nanpa wan pi toki sona."* → ni li pali sin e nanpa meso; kipisi pi toki awen li weka e ni. o pana e kipisi ale.
- *"o suli e toki sona kepeken nanpa pi toki tan."* → T1 li pana ala e suli, lon tenpo ale.
- *"o ken e ni: tomo li toki e kama pi pali pi jan pali ona."* → toki kama tan ona sama, lon len pi ilo open pi kulupu.
- *"o ken e ni: tomo li kama jo e mani tan lon pi tenpo lili anu tan suli sewi."* → nimi pona li esun. nasin tenpo pi toki kama li nasin lawa pi tomo; jan li ken ala esun e suli.
- *"o anpa e suli lon pali sin pi sama ala."* → toki sama li sona. o sitelen e ona; o lawa ala e ona kepeken tenpo anu nanpa.
- *"o pana e nimi "verified" tawa toki sona lon T4."* → lawa pi lon lon len pona. kama taso, lon ala.
- *"o pana e nimi pona esun tawa suli sona."* → ni li nasa e linja pi nimi kulupu. jan esun pona li jan pona pi toki sona ala tan ni.

## ike awen (nimi ona)

weka tan ma: kulupu li jo ala e tomo lon pali la ona li ken ala kama T4, li ken kama T3 taso kepeken lipu nimi lon tomo weka — ni li lupa; o pali e nasin lon poka ona (tenpo suno pi toki kama pi tawa, nasin pi tomo poka), o kama ala ken e ona lon kalama ala. open lete: lon open la tomo li lili, la toki sama tan jan ante li lili; nimi "stand-in" li awen e lon lon tenpo ale, kulupu tomo li kama suli ala la. sike pi pali ike sama pi jan lon lon tomo mute li ken lon kepeken mani sama; ona li pali len — ma pi kipisi pi toki awen — en pakala ale ni (jan li lawa e ona) li pakala, li weka ala tan nanpa meso.
