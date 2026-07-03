# Gesamtskript — Lineare Algebra II, Analysis II & Physik II

## Inhaltsverzeichnis

- [Kapitel 0 — Polynome, Teilbarkeit und Faktorisierung](#kapitel-0-polynome-teilbarkeit-und-faktorisierung)
  - [Motivation](#motivation)
  - [Intuition](#intuition)
  - [Formale Definitionen](#formale-definitionen)
    - [Polynomring](#polynomring)
    - [Grad](#grad)
    - [Nullteilerfreiheit, Einheiten](#nullteilerfreiheit-einheiten)
    - [Teilbarkeit, irreduzibel, prim](#teilbarkeit-irreduzibel-prim)
    - [Primzahl](#primzahl)
    - [Nullstelle](#nullstelle)
    - [Algebraisch abgeschlossen](#algebraisch-abgeschlossen)
  - [Eigenschaften](#eigenschaften)
  - [Sätze](#sätze)
    - [Satz 0.12 (Gradformeln)](#satz-012-gradformeln)
    - [Satz 0.13 (Primelement $\Rightarrow$ irreduzibel)](#satz-013-primelement-rightarrow-irreduzibel)
    - [Satz 0.14 (Division mit Rest)](#satz-014-division-mit-rest)
    - [Satz 0.15 (ggT und Bézout)](#satz-015-ggt-und-bézout)
    - [Satz 0.16 / 0.17 (Eindeutige Faktorisierung)](#satz-016-017-eindeutige-faktorisierung)
    - [Satz 0.18 (irreduzibel $\Leftrightarrow$ prim in $\mathbb{Z}$ und $k[X]$)](#satz-018-irreduzibel-leftrightarrow-prim-in-mathbbz-und-kx)
    - [Satz 0.19 (Nullstellen und Linearfaktoren)](#satz-019-nullstellen-und-linearfaktoren)
    - [Satz 0.20 (Fundamentalsatz der Algebra)](#satz-020-fundamentalsatz-der-algebra)
  - [Beweise](#beweise)
    - [Beweis von Satz 0.12 (Gradformeln) — *Beweisstil: direkt*](#beweis-von-satz-012-gradformeln-beweisstil-direkt)
    - [Beweis von Satz 0.13 (prim $\Rightarrow$ irreduzibel) — *Beweisstil: direkt*](#beweis-von-satz-013-prim-rightarrow-irreduzibel-beweisstil-direkt)
    - [Beweis von Satz 0.14 (Division mit Rest) — *Beweisstil: Existenz konstruktiv + Eindeutigkeit per Widerspruch*](#beweis-von-satz-014-division-mit-rest-beweisstil-existenz-konstruktiv-eindeutigkeit-per-widerspruch)
    - [Beweis von Satz 0.15 (ggT/Bézout) — *Beweisstil: Euklidischer Algorithmus (konstruktiv) + Induktion*](#beweis-von-satz-015-ggtbézout-beweisstil-euklidischer-algorithmus-konstruktiv-induktion)
    - [Beweis von Satz 0.18 (irreduzibel $\Rightarrow$ prim) — *Beweisstil: direkt mit Bézout*](#beweis-von-satz-018-irreduzibel-rightarrow-prim-beweisstil-direkt-mit-bézout)
    - [Beweis der Eindeutigkeit der Faktorisierung (0.16/0.17) — *Beweisstil: Induktion + Primeigenschaft*](#beweis-der-eindeutigkeit-der-faktorisierung-016017-beweisstil-induktion-primeigenschaft)
    - [Beweis von Satz 0.19 (Nullstellen) — *Beweisstil: direkt via Division mit Rest*](#beweis-von-satz-019-nullstellen-beweisstil-direkt-via-division-mit-rest)
  - [Algorithmen](#algorithmen)
    - [Algorithmus A — Polynomdivision (Division mit Rest in $k[X]$)](#algorithmus-a-polynomdivision-division-mit-rest-in-kx)
    - [Algorithmus B — (Erweiterter) Euklidischer Algorithmus](#algorithmus-b-erweiterter-euklidischer-algorithmus)
  - [Beispiele](#beispiele)
  - [Gegenbeispiele](#gegenbeispiele)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben)
  - [Typische Fehler](#typische-fehler)
  - [Verbindungen](#verbindungen)
  - [Zusammenfassung](#zusammenfassung)
- [Kapitel 1 — Quotientenvektorräume](#kapitel-1-quotientenvektorräume)
  - [Motivation](#motivation-1)
  - [Intuition](#intuition-1)
  - [Formale Definitionen](#formale-definitionen-1)
    - [Äquivalenzrelation (Grundlage)](#äquivalenzrelation-grundlage)
    - [Der Quotientenvektorraum](#der-quotientenvektorraum)
    - [Die kanonische Projektion](#die-kanonische-projektion)
  - [Eigenschaften](#eigenschaften-1)
  - [Sätze](#sätze-1)
    - [Satz 1.6 (Wohldefiniertheit und Vektorraumstruktur)](#satz-16-wohldefiniertheit-und-vektorraumstruktur)
    - [Satz 1.7 (Projektion: linear, surjektiv, Kern $U$)](#satz-17-projektion-linear-surjektiv-kern-u)
    - [Satz 1.8 (Universelle Eigenschaft / Homomorphiesatz)](#satz-18-universelle-eigenschaft-homomorphiesatz)
    - [Satz 1.9 (Dimension und Basis von $V/U$)](#satz-19-dimension-und-basis-von-vu)
  - [Beweise](#beweise-1)
    - [Beweis von Satz 1.6 (Wohldefiniertheit) — *Beweisstil: direkt, Repräsentantenunabhängigkeit*](#beweis-von-satz-16-wohldefiniertheit-beweisstil-direkt-repräsentantenunabhängigkeit)
    - [Beweis von Satz 1.7 (Projektion) — *Beweisstil: direkt*](#beweis-von-satz-17-projektion-beweisstil-direkt)
    - [Beweis von Satz 1.8 (universelle Eigenschaft) — *Beweisstil: Existenz (Konstruktion + Wohldefiniertheit) und Eindeutigkeit*](#beweis-von-satz-18-universelle-eigenschaft-beweisstil-existenz-konstruktion-wohldefiniertheit-und-eindeutigkeit)
    - [Beweis von Satz 1.9 (Dimension) — *Beweisstil: direkt (Erzeugendensystem + lineare Unabhängigkeit)*](#beweis-von-satz-19-dimension-beweisstil-direkt-erzeugendensystem-lineare-unabhängigkeit)
  - [Algorithmen](#algorithmen-1)
    - [Verfahren — Rechnen in $V/U$ und Basis von $V/U$ bestimmen](#verfahren-rechnen-in-vu-und-basis-von-vu-bestimmen)
  - [Beispiele](#beispiele-1)
  - [Gegenbeispiele](#gegenbeispiele-1)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-1)
  - [Typische Fehler](#typische-fehler-1)
  - [Verbindungen](#verbindungen-1)
  - [Zusammenfassung](#zusammenfassung-1)
- [Kapitel 2 — Eigenwerte, Diagonalisierung und Trigonalisierung](#kapitel-2-eigenwerte-diagonalisierung-und-trigonalisierung)
  - [Motivation](#motivation-2)
  - [Intuition](#intuition-2)
  - [Formale Definitionen](#formale-definitionen-2)
  - [Eigenschaften](#eigenschaften-2)
  - [Sätze](#sätze-2)
    - [Satz 2.8 (Eigenwert-Kriterium)](#satz-28-eigenwert-kriterium)
    - [Satz 2.9 (Diagonalisierbarkeitskriterium)](#satz-29-diagonalisierbarkeitskriterium)
    - [Satz 2.10 ($\chi_f$ ist wohldefiniert)](#satz-210-chi_f-ist-wohldefiniert)
    - [Satz 2.11 (Trigonalisierbarkeitskriterium) — *Hauptsatz des Kapitels*](#satz-211-trigonalisierbarkeitskriterium-hauptsatz-des-kapitels)
    - [Lemma 2.12 ($\chi$ zerlegt sich an invariantem Unterraum)](#lemma-212-chi-zerlegt-sich-an-invariantem-unterraum)
    - [Lemma 2.13 (geometrische $\le$ algebraische Vielfachheit)](#lemma-213-geometrische-le-algebraische-vielfachheit)
  - [Beweise](#beweise-2)
    - [Beweis von Satz 2.8 — *Beweisstil: direkt (Äquivalenzkette)*](#beweis-von-satz-28-beweisstil-direkt-äquivalenzkette)
    - [Lemma 2.11′ (Eigenvektoren zu verschiedenen Eigenwerten sind linear unabhängig) — *Beweisstil: Induktion*](#lemma-211-eigenvektoren-zu-verschiedenen-eigenwerten-sind-linear-unabhängig-beweisstil-induktion)
    - [Beweis von Lemma 2.13 — *Beweisstil: Basisergänzung + Blockdeterminante*](#beweis-von-lemma-213-beweisstil-basisergänzung-blockdeterminante)
    - [Beweis von Satz 2.9 (Diagonalisierbarkeitskriterium) — *Beweisstil: Ringschluss*](#beweis-von-satz-29-diagonalisierbarkeitskriterium-beweisstil-ringschluss)
    - [Beweis von Lemma 2.12 — *Beweisstil: direkt (Blockmatrix)*](#beweis-von-lemma-212-beweisstil-direkt-blockmatrix)
    - [Beweis von Satz 2.11 (Trigonalisierbarkeit) — *Beweisstil: $\Rightarrow$ direkt, $\Leftarrow$ Induktion über $\dim V$ via Quotient* ★ vollständig](#beweis-von-satz-211-trigonalisierbarkeit-beweisstil-rightarrow-direkt-leftarrow-induktion-über-dim-v-via-quotient-vollständig)
  - [Algorithmen](#algorithmen-2)
    - [Algorithmus — Diagonalisierung einer Matrix](#algorithmus-diagonalisierung-einer-matrix)
    - [Algorithmus-Skizze — Trigonalisierung](#algorithmus-skizze-trigonalisierung)
  - [Beispiele](#beispiele-2)
  - [Gegenbeispiele](#gegenbeispiele-2)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-2)
  - [Typische Fehler](#typische-fehler-2)
  - [Verbindungen](#verbindungen-2)
  - [Zusammenfassung](#zusammenfassung-2)
- [Kapitel 3 — Minimalpolynom und Satz von Cayley-Hamilton](#kapitel-3-minimalpolynom-und-satz-von-cayley-hamilton)
  - [Motivation](#motivation-3)
  - [Intuition](#intuition-3)
  - [Formale Definitionen](#formale-definitionen-3)
  - [Eigenschaften](#eigenschaften-3)
  - [Sätze](#sätze-3)
    - [Satz 3.4 (Einsetzen ist Ringhomomorphismus)](#satz-34-einsetzen-ist-ringhomomorphismus)
    - [Satz 3.5 (Existenz eines Annihilators)](#satz-35-existenz-eines-annihilators)
    - [Satz 3.6 (ggT von Annihilatoren annihiliert)](#satz-36-ggt-von-annihilatoren-annihiliert)
    - [Satz 3.7 (Eindeutigkeit von $\mu_f$)](#satz-37-eindeutigkeit-von-mu_f)
    - [Satz 3.8 (Teilbarkeitscharakterisierung)](#satz-38-teilbarkeitscharakterisierung)
    - [Satz 3.9 (Cayley-Hamilton) — *zentraler Satz*](#satz-39-cayley-hamilton-zentraler-satz)
    - [Satz 3.10 ($\mu_f$ und $\chi_f$ haben dieselben Nullstellen)](#satz-310-mu_f-und-chi_f-haben-dieselben-nullstellen)
    - [Satz 3.11 (Gestalt von $\mu_f$ bei zerfallendem $\chi_f$)](#satz-311-gestalt-von-mu_f-bei-zerfallendem-chi_f)
    - [Satz 3.12 (Diagonalisierbarkeitskriterium via $\mu_f$) — *Hauptanwendung*](#satz-312-diagonalisierbarkeitskriterium-via-mu_f-hauptanwendung)
  - [Beweise](#beweise-3)
    - [Beweis von Satz 3.4(ii) (Multiplikativität) — *Beweisstil: direkt, Doppelsumme*](#beweis-von-satz-34ii-multiplikativität-beweisstil-direkt-doppelsumme)
    - [Beweis von Satz 3.5 (Existenz) — *Beweisstil: Dimensionsargument*](#beweis-von-satz-35-existenz-beweisstil-dimensionsargument)
    - [Beweis von Satz 3.6 (ggT annihiliert) — *Beweisstil: direkt mit Bézout*](#beweis-von-satz-36-ggt-annihiliert-beweisstil-direkt-mit-bézout)
    - [Beweis von Satz 3.8 (Teilbarkeit) — *Beweisstil: Division mit Rest*](#beweis-von-satz-38-teilbarkeit-beweisstil-division-mit-rest)
    - [Beweis von Satz 3.9 (Cayley-Hamilton) — *zwei Wege*](#beweis-von-satz-39-cayley-hamilton-zwei-wege)
    - [Beweis von Satz 3.11 — *Beweisstil: direkt*](#beweis-von-satz-311-beweisstil-direkt)
    - [Beweis von Satz 3.12 (Diagonalisierbarkeit via $\mu_f$) — *Beweisstil: zwei Richtungen*](#beweis-von-satz-312-diagonalisierbarkeit-via-mu_f-beweisstil-zwei-richtungen)
  - [Algorithmen](#algorithmen-3)
    - [Algorithmus A — Minimalpolynom über Teiler von $\chi_f$](#algorithmus-a-minimalpolynom-über-teiler-von-chi_f)
    - [Algorithmus B — Minimalpolynom über lineare Abhängigkeit](#algorithmus-b-minimalpolynom-über-lineare-abhängigkeit)
  - [Beispiele](#beispiele-3)
  - [Gegenbeispiele](#gegenbeispiele-3)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-3)
  - [Typische Fehler](#typische-fehler-3)
  - [Verbindungen](#verbindungen-3)
  - [Zusammenfassung](#zusammenfassung-3)
- [Kapitel 4 — Haupträume und Jordan-Normalform](#kapitel-4-haupträume-und-jordan-normalform)
  - [Motivation](#motivation-4)
  - [Intuition](#intuition-4)
  - [Formale Definitionen](#formale-definitionen-4)
  - [Eigenschaften](#eigenschaften-4)
  - [Sätze](#sätze-4)
    - [Lemma 4.8 (Stabilisierung der Kernkette)](#lemma-48-stabilisierung-der-kernkette)
    - [Satz 4.9 (Hauptraumzerlegung) — *Strukturhauptsatz*](#satz-49-hauptraumzerlegung-strukturhauptsatz)
    - [Lemma 4.10 (Nilpotente Jordan-Kette)](#lemma-410-nilpotente-jordan-kette)
    - [Satz 4.11 (Normalform nilpotenter Endomorphismen) — *Kern der JNF*](#satz-411-normalform-nilpotenter-endomorphismen-kern-der-jnf)
    - [Satz 4.12 (Existenz der Jordan-Normalform)](#satz-412-existenz-der-jordan-normalform)
    - [Satz 4.13 (Eindeutigkeit der JNF und Blockzahlen)](#satz-413-eindeutigkeit-der-jnf-und-blockzahlen)
    - [Satz 4.14 (Jordan-Chevalley-Zerlegung)](#satz-414-jordan-chevalley-zerlegung)
  - [Beweise](#beweise-4)
    - [Beweis von Lemma 4.8 (Stabilisierung) — *Beweisstil: direkt*](#beweis-von-lemma-48-stabilisierung-beweisstil-direkt)
    - [Beweis von Satz 4.9 (Hauptraumzerlegung) — *Beweisstil: Bézout-Partition der Eins $+$ Direktheit*](#beweis-von-satz-49-hauptraumzerlegung-beweisstil-bézout-partition-der-eins-direktheit)
    - [Beweis von Lemma 4.10 — *Beweisstil: direkt*](#beweis-von-lemma-410-beweisstil-direkt)
    - [Beweis von Satz 4.11 (nilpotente Normalform) — *Beweisstil: Konstruktion über Kernketten (von oben nach unten)*](#beweis-von-satz-411-nilpotente-normalform-beweisstil-konstruktion-über-kernketten-von-oben-nach-unten)
    - [Beweis von Satz 4.12 (Existenz JNF) — *Beweisstil: Zusammensetzen*](#beweis-von-satz-412-existenz-jnf-beweisstil-zusammensetzen)
    - [Beweis von Satz 4.13 (Blockzahlen / Eindeutigkeit) — *Beweisstil: Invarianten zählen*](#beweis-von-satz-413-blockzahlen-eindeutigkeit-beweisstil-invarianten-zählen)
  - [Algorithmen](#algorithmen-4)
    - [Algorithmus — Jordan-Normalform berechnen (Kochrezept)](#algorithmus-jordan-normalform-berechnen-kochrezept)
    - [Algorithmus-Zusatz — Jordan-Basis / Transformationsmatrix $T$](#algorithmus-zusatz-jordan-basis-transformationsmatrix-t)
  - [Beispiele](#beispiele-4)
  - [Gegenbeispiele](#gegenbeispiele-4)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-4)
  - [Typische Fehler](#typische-fehler-4)
  - [Verbindungen](#verbindungen-4)
  - [Zusammenfassung](#zusammenfassung-4)
- [Kapitel 5 — Der Körper der komplexen Zahlen](#kapitel-5-der-körper-der-komplexen-zahlen)
  - [Motivation](#motivation-5)
  - [Intuition](#intuition-5)
  - [Formale Definitionen](#formale-definitionen-5)
  - [Eigenschaften](#eigenschaften-5)
  - [Sätze](#sätze-5)
    - [Satz 5.6 ($\mathbb{C}$ ist ein Körper)](#satz-56-mathbbc-ist-ein-körper)
    - [Satz 5.7 (Rechenregeln für Konjugation und Betrag)](#satz-57-rechenregeln-für-konjugation-und-betrag)
    - [Satz 5.8 (Matrixdarstellung der Multiplikation)](#satz-58-matrixdarstellung-der-multiplikation)
    - [Satz 5.9 ($\mathbb{C}\cong\mathbb{R}[X]/(X^2+1)$)](#satz-59-mathbbccongmathbbrxx21)
    - [Satz 5.10 (Fundamentalsatz der Algebra)](#satz-510-fundamentalsatz-der-algebra)
    - [Satz 5.11 (Euler-Formel)](#satz-511-euler-formel)
    - [Satz 5.12 (Polarform und Multiplikation)](#satz-512-polarform-und-multiplikation)
  - [Beweise](#beweise-5)
    - [Beweis von Satz 5.6 (Inverses) — *Beweisstil: direkt (Konstruktion)*](#beweis-von-satz-56-inverses-beweisstil-direkt-konstruktion)
    - [Beweis von Satz 5.7 (Konjugation/Betrag) — *Beweisstil: direkt*](#beweis-von-satz-57-konjugationbetrag-beweisstil-direkt)
    - [Beweis von Satz 5.9 ($\mathbb{C}\cong\mathbb{R}[X]/(X^2+1)$) — *Beweisstil: Homomorphiesatz*](#beweis-von-satz-59-mathbbccongmathbbrxx21-beweisstil-homomorphiesatz)
    - [Beweis von Satz 5.11 (Euler) — *Beweisstil: Reihenumordnung (absolute Konvergenz)*](#beweis-von-satz-511-euler-beweisstil-reihenumordnung-absolute-konvergenz)
    - [Korollar (Additionstheoreme) — *Beweisstil: Real-/Imaginärteilvergleich*](#korollar-additionstheoreme-beweisstil-real-imaginärteilvergleich)
    - [Beweis von Satz 5.12 (Polarmultiplikation) — *Beweisstil: direkt mit Euler*](#beweis-von-satz-512-polarmultiplikation-beweisstil-direkt-mit-euler)
  - [Algorithmen](#algorithmen-5)
    - [Algorithmus A — Umrechnung kartesisch $\leftrightarrow$ polar](#algorithmus-a-umrechnung-kartesisch-leftrightarrow-polar)
    - [Algorithmus B — $n$-te Wurzeln einer komplexen Zahl (de Moivre)](#algorithmus-b-n-te-wurzeln-einer-komplexen-zahl-de-moivre)
  - [Beispiele](#beispiele-5)
  - [Gegenbeispiele](#gegenbeispiele-5)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-5)
  - [Typische Fehler](#typische-fehler-5)
  - [Verbindungen](#verbindungen-5)
  - [Zusammenfassung](#zusammenfassung-5)
- [Kapitel 6 — Skalarprodukt, Norm und Metrik](#kapitel-6-skalarprodukt-norm-und-metrik)
  - [Motivation](#motivation-6)
  - [Intuition](#intuition-6)
  - [Formale Definitionen](#formale-definitionen-6)
  - [Eigenschaften](#eigenschaften-6)
  - [Sätze](#sätze-6)
    - [Satz 6.9 (Matrixkriterien)](#satz-69-matrixkriterien)
    - [Lemma 6.10 ($\|v\|\ge0$)](#lemma-610-vge0)
    - [Lemma 6.11 ($d(x,y)\ge0$)](#lemma-611-dxyge0)
    - [Lemma 6.12 (Norm induziert Metrik)](#lemma-612-norm-induziert-metrik)
    - [Satz 6.13 (Cauchy-Schwarz-Ungleichung) — *zentral*](#satz-613-cauchy-schwarz-ungleichung-zentral)
    - [Satz 6.14 (induzierte Norm ist Norm)](#satz-614-induzierte-norm-ist-norm)
  - [Beweise](#beweise-6)
    - [Beweis von Lemma 6.10 ($\|v\|\ge0$) — *Beweisstil: direkt*](#beweis-von-lemma-610-vge0-beweisstil-direkt)
    - [Beweis von Lemma 6.12 (Norm $\to$ Metrik) — *Beweisstil: direkt (Axiomcheck)*](#beweis-von-lemma-612-norm-to-metrik-beweisstil-direkt-axiomcheck)
    - [Beweis von Satz 6.13 (Cauchy-Schwarz) — *Beweisstil: Optimierung (geschickte Wahl von $a$)*](#beweis-von-satz-613-cauchy-schwarz-beweisstil-optimierung-geschickte-wahl-von-a)
    - [Beweis von Satz 6.14 (induzierte Norm) — *Beweisstil: direkt, N2 via Cauchy-Schwarz*](#beweis-von-satz-614-induzierte-norm-beweisstil-direkt-n2-via-cauchy-schwarz)
  - [Algorithmen](#algorithmen-6)
    - [Verfahren — Prüfen, ob $s$ ein Skalarprodukt ist](#verfahren-prüfen-ob-s-ein-skalarprodukt-ist)
  - [Beispiele](#beispiele-6)
  - [Gegenbeispiele](#gegenbeispiele-6)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-6)
  - [Typische Fehler](#typische-fehler-6)
  - [Verbindungen](#verbindungen-6)
  - [Zusammenfassung](#zusammenfassung-6)
- [Kapitel 7 — Orthogonalität, Projektion und Gram-Schmidt](#kapitel-7-orthogonalität-projektion-und-gram-schmidt)
  - [Motivation](#motivation-7)
  - [Intuition](#intuition-7)
  - [Formale Definitionen](#formale-definitionen-7)
  - [Eigenschaften](#eigenschaften-7)
  - [Sätze](#sätze-7)
    - [Satz 7.6 (Längenformel und Pythagoras)](#satz-76-längenformel-und-pythagoras)
    - [Satz 7.7 (Parallelogrammgleichung)](#satz-77-parallelogrammgleichung)
    - [Satz 7.8 (Satz des Thales)](#satz-78-satz-des-thales)
    - [Lemma 7.9 (orthogonal $\Rightarrow$ linear unabhängig)](#lemma-79-orthogonal-rightarrow-linear-unabhängig)
    - [Satz 7.10 (Normierung, Lemma 3.15)](#satz-710-normierung-lemma-315)
    - [Satz 7.11 (orthogonales Komplement von Erzeugnissen)](#satz-711-orthogonales-komplement-von-erzeugnissen)
    - [Satz 7.12 (Orthogonale Zerlegung) — *zentral*](#satz-712-orthogonale-zerlegung-zentral)
    - [Satz 7.13 (orthogonale Projektion und Bestapproximation) — *Herzstück*](#satz-713-orthogonale-projektion-und-bestapproximation-herzstück)
    - [Lemma 7.14 (Projektionsformel via ONB)](#lemma-714-projektionsformel-via-onb)
    - [Satz 7.15 (Gram-Schmidt-Orthonormalisierung) — *zentraler Algorithmus*](#satz-715-gram-schmidt-orthonormalisierung-zentraler-algorithmus)
  - [Beweise](#beweise-7)
    - [Beweis von Satz 7.6 (Längenformel) — *Beweisstil: direkt (Ausmultiplizieren)*](#beweis-von-satz-76-längenformel-beweisstil-direkt-ausmultiplizieren)
    - [Beweis von Satz 7.7 (Parallelogramm) — *Beweisstil: direkt*](#beweis-von-satz-77-parallelogramm-beweisstil-direkt)
    - [Beweis von Satz 7.8 (Thales, euklidisch) — *Beweisstil: direkt*](#beweis-von-satz-78-thales-euklidisch-beweisstil-direkt)
    - [Beweis von Lemma 7.9 (orthogonal $\Rightarrow$ unabhängig) — *Beweisstil: direkt*](#beweis-von-lemma-79-orthogonal-rightarrow-unabhängig-beweisstil-direkt)
    - [Beweis von Satz 7.12 ($V=U\oplus U^\perp$) — *Beweisstil: Konstruktion via ONB $+$ Schnitt*](#beweis-von-satz-712-vuoplus-uperp-beweisstil-konstruktion-via-onb-schnitt)
    - [Beweis von Satz 7.13 (Bestapproximation) — *Beweisstil: Pythagoras*](#beweis-von-satz-713-bestapproximation-beweisstil-pythagoras)
    - [Beweis von Lemma 7.14 (Projektionsformel) — *Beweisstil: direkt (Charakterisierung 7.13a)*](#beweis-von-lemma-714-projektionsformel-beweisstil-direkt-charakterisierung-713a)
    - [Beweis von Satz 7.15 (Gram-Schmidt) — *Beweisstil: Induktion mit Projektion*](#beweis-von-satz-715-gram-schmidt-beweisstil-induktion-mit-projektion)
  - [Algorithmen](#algorithmen-7)
    - [Algorithmus — Gram-Schmidt-Orthonormalisierung](#algorithmus-gram-schmidt-orthonormalisierung)
    - [Algorithmus — Orthogonale Projektion / Bestapproximation](#algorithmus-orthogonale-projektion-bestapproximation)
  - [Beispiele](#beispiele-7)
  - [Gegenbeispiele](#gegenbeispiele-7)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-7)
  - [Typische Fehler](#typische-fehler-7)
  - [Verbindungen](#verbindungen-7)
  - [Zusammenfassung](#zusammenfassung-7)
- [Kapitel 8 — Isometrien, adjungierte Abbildungen und Spektralsätze](#kapitel-8-isometrien-adjungierte-abbildungen-und-spektralsätze)
  - [Motivation](#motivation-8)
  - [Intuition](#intuition-8)
  - [Formale Definitionen](#formale-definitionen-8)
  - [Eigenschaften](#eigenschaften-8)
  - [Sätze](#sätze-8)
    - [Lemma 8.5½ (Yoga-Lemma) — *Rechenbrücke abstrakt $\leftrightarrow$ Matrix*](#lemma-85½-yoga-lemma-rechenbrücke-abstrakt-leftrightarrow-matrix)
    - [Satz 8.6 (Existenz und Eindeutigkeit der Adjungierten)](#satz-86-existenz-und-eindeutigkeit-der-adjungierten)
    - [Satz 8.7 (Rechenregeln, Lemma 7.2)](#satz-87-rechenregeln-lemma-72)
    - [Satz 8.8 (Charakterisierung von Isometrien) — *zentral*](#satz-88-charakterisierung-von-isometrien-zentral)
    - [Lemma 8.9 (Invarianz-Übergang aufs Komplement)](#lemma-89-invarianz-übergang-aufs-komplement)
    - [Lemma 8.9½ (Normalität ist normerhaltend, „Lemma 7.7\*")](#lemma-89½-normalität-ist-normerhaltend-lemma-77)
    - [Lemma 8.10 (Eigenräume von $f$ und $f^*$ bei normalen $f$)](#lemma-810-eigenräume-von-f-und-f-bei-normalen-f)
    - [Satz 8.11 (Unitärer Spektralsatz) — *Höhepunkt*](#satz-811-unitärer-spektralsatz-höhepunkt)
    - [Satz 8.12 (Matrixversion / unitäre Diagonalisierung)](#satz-812-matrixversion-unitäre-diagonalisierung)
    - [Satz 8.13 (Eigenwerte der Sonderklassen)](#satz-813-eigenwerte-der-sonderklassen)
    - [Satz 8.14 (Reeller Spektralsatz) — *ergänzt; Kurshöhepunkt über $\mathbb{R}$*](#satz-814-reeller-spektralsatz-ergänzt-kurshöhepunkt-über-mathbbr)
  - [Beweise](#beweise-8)
    - [Beweis von Satz 8.6 (Adjungierte) — *Beweisstil: Konstruktion in ONB $+$ Eindeutigkeit*](#beweis-von-satz-86-adjungierte-beweisstil-konstruktion-in-onb-eindeutigkeit)
    - [Beweis von Satz 8.8 (Isometrie-Charakterisierung) — *Beweisstil: Ringschluss*](#beweis-von-satz-88-isometrie-charakterisierung-beweisstil-ringschluss)
    - [Beweis von Lemma 8.9 — *Beweisstil: direkt*](#beweis-von-lemma-89-beweisstil-direkt)
    - [Beweis von Lemma 8.10 ($\mathrm{Eig}(f,\lambda)=\mathrm{Eig}(f^*,\bar\lambda)$) — *Beweisstil: Normalität + Norm*](#beweis-von-lemma-810-mathrmeigflambdamathrmeigfbarlambda-beweisstil-normalität-norm)
    - [Beweis von Satz 8.11 (Unitärer Spektralsatz) — *Beweisstil: Induktion über $\dim V$ via $U^\perp$* ★](#beweis-von-satz-811-unitärer-spektralsatz-beweisstil-induktion-über-dim-v-via-uperp)
    - [Beweis von Satz 8.13 (Eigenwerte) — *Beweisstil: direkt*](#beweis-von-satz-813-eigenwerte-beweisstil-direkt)
    - [Beweis von Satz 8.14 (Reeller Spektralsatz) — *Beweisstil: Eigenwerte reell $+$ reelle Induktion* ★](#beweis-von-satz-814-reeller-spektralsatz-beweisstil-eigenwerte-reell-reelle-induktion)
  - [Algorithmen](#algorithmen-8)
    - [Algorithmus — Orthonormale (unitäre/orthogonale) Diagonalisierung](#algorithmus-orthonormale-unitäreorthogonale-diagonalisierung)
  - [Beispiele](#beispiele-8)
  - [Gegenbeispiele](#gegenbeispiele-8)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-8)
  - [Typische Fehler](#typische-fehler-8)
  - [Verbindungen](#verbindungen-8)
  - [Zusammenfassung](#zusammenfassung-8)
- [Epilog — Das Skript als System](#epilog-das-skript-als-system)
- [Analysis auf allgemeinen linearen Räumen](#analysis-auf-allgemeinen-linearen-räumen)
    - [Vollständiges Skript — rekonstruiert aus Vorlesung, bereinigt und ergänzt](#vollständiges-skript-rekonstruiert-aus-vorlesung-bereinigt-und-ergänzt)
  - [Vorwort](#vorwort)
- [Kapitel 1: Topologische Räume](#kapitel-1-topologische-räume)
  - [Motivation](#motivation-9)
  - [Intuition](#intuition-9)
  - [Formale Definitionen](#formale-definitionen-9)
    - [Definition 1.1 (Topologischer Raum / Umgebungstopologie)](#definition-11-topologischer-raum-umgebungstopologie)
    - [Definition 1.2 (Offene und abgeschlossene Mengen)](#definition-12-offene-und-abgeschlossene-mengen)
    - [Definition 1.4 (Umgebungsbasis)](#definition-14-umgebungsbasis)
    - [Definition 1.5 (Hausdorff-Raum)](#definition-15-hausdorff-raum)
    - [Definition 1.6 (Konvergenz)](#definition-16-konvergenz)
    - [Definition 1.8 (Stetigkeit — punktweise)](#definition-18-stetigkeit-punktweise)
  - [Eigenschaften](#eigenschaften-9)
    - [Satz 1.3 (Eigenschaften offener Mengen)](#satz-13-eigenschaften-offener-mengen)
    - [Beispiele topologischer Räume](#beispiele-topologischer-räume)
    - [Lemma 1.7 (Eindeutigkeit von Grenzwerten in Hausdorff-Räumen)](#lemma-17-eindeutigkeit-von-grenzwerten-in-hausdorff-räumen)
    - [Lemma 1.9 (Charakterisierung von Stetigkeit über Urbilder offener Mengen)](#lemma-19-charakterisierung-von-stetigkeit-über-urbilder-offener-mengen)
    - [Lemma 1.10 (Folgenkriterium der Stetigkeit unter erster Abzählbarkeit)](#lemma-110-folgenkriterium-der-stetigkeit-unter-erster-abzählbarkeit)
  - [Beispiele](#beispiele-9)
  - [Gegenbeispiele](#gegenbeispiele-9)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-9)
  - [Typische Fehler](#typische-fehler-9)
  - [Verbindungen](#verbindungen-9)
  - [Zwischenschritt: Zusammenhang, Kompaktheit (topologisch)](#zwischenschritt-zusammenhang-kompaktheit-topologisch)
    - [Definition 1.14 (Zusammenhängender Raum)](#definition-114-zusammenhängender-raum)
    - [Satz 1.12 (Zwischenwertsatz, topologische Version)](#satz-112-zwischenwertsatz-topologische-version)
    - [Definition 1.17 (Kompaktheit)](#definition-117-kompaktheit)
    - [Lemma 1.14 (Stetige Bilder kompakter Mengen sind kompakt)](#lemma-114-stetige-bilder-kompakter-mengen-sind-kompakt)
- [Kapitel 2: Metrische Räume](#kapitel-2-metrische-räume)
  - [Motivation](#motivation-10)
  - [Intuition](#intuition-10)
  - [Formale Definitionen](#formale-definitionen-10)
    - [Definition 1.15 (Metrik, metrischer Raum)](#definition-115-metrik-metrischer-raum)
    - [Definition 1.16 (Metrische Topologie)](#definition-116-metrische-topologie)
    - [Definition 1.17 (Cauchy-Folgen)](#definition-117-cauchy-folgen)
    - [Definition 1.20 (Vollständigkeit)](#definition-120-vollständigkeit)
    - [Definition 1.21 (Dichtheit)](#definition-121-dichtheit)
  - [Eigenschaften](#eigenschaften-10)
    - [Lemma 1.18 (Charakterisierung von Konvergenz über die Metrik)](#lemma-118-charakterisierung-von-konvergenz-über-die-metrik)
    - [Lemma 1.19 (Konvergent $\Rightarrow$ Cauchy, aber nicht umgekehrt)](#lemma-119-konvergent-rightarrow-cauchy-aber-nicht-umgekehrt)
  - [Sätze](#sätze-9)
    - [Satz 1.23 (Vervollständigung metrischer Räume)](#satz-123-vervollständigung-metrischer-räume)
    - [Satz 1.26 (Bolzano–Weierstraß in metrischen Räumen)](#satz-126-bolzanoweierstraß-in-metrischen-räumen)
    - [Satz 1.55 (Satz von Heine–Borel, $\mathbb{R}^n$)](#satz-155-satz-von-heineborel-mathbbrn)
  - [Vergleichstabelle: Konvergenz vs. Cauchy-Eigenschaft vs. Vollständigkeit](#vergleichstabelle-konvergenz-vs-cauchy-eigenschaft-vs-vollständigkeit)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-10)
  - [Typische Fehler](#typische-fehler-10)
  - [Verbindungen](#verbindungen-10)
  - [Zusammenfassung Kapitel 1 & 2](#zusammenfassung-kapitel-1-2)
- [Analysis auf allgemeinen linearen Räumen — Teil 2](#analysis-auf-allgemeinen-linearen-räumen-teil-2)
- [Kapitel 3: Banachräume und die Fréchet-Ableitung](#kapitel-3-banachräume-und-die-fréchet-ableitung)
  - [Motivation](#motivation-11)
  - [Intuition](#intuition-11)
  - [Formale Definitionen](#formale-definitionen-11)
    - [Definition 1.28 (Norm, normierter Raum)](#definition-128-norm-normierter-raum)
    - [Standardbeispiele: Die $p$-Normen auf $\mathbb{R}^n$](#standardbeispiele-die-p-normen-auf-mathbbrn)
    - [Lemma 1.29 (Norm induziert Metrik)](#lemma-129-norm-induziert-metrik)
    - [Definition 1.30 (Banachraum)](#definition-130-banachraum)
    - [Definition 1.31/1.32 (Lineare, beschränkte Abbildungen und Operatornorm)](#definition-131132-lineare-beschränkte-abbildungen-und-operatornorm)
    - [Lemma 1.74 (Beschränkt $\iff$ Stetig, für lineare Abbildungen)](#lemma-174-beschränkt-iff-stetig-für-lineare-abbildungen)
    - [Lemma 1.35 (L(A,B) ist Banachraum)](#lemma-135-lab-ist-banachraum)
    - [Definition 1.37 (Fréchet-Differenzierbarkeit)](#definition-137-fréchet-differenzierbarkeit)
    - [Definition 1.38 (Stetige Differenzierbarkeit)](#definition-138-stetige-differenzierbarkeit)
  - [Eigenschaften](#eigenschaften-11)
    - [Ableitungsregeln (Satz, ohne separate Nummer in der Mitschrift)](#ableitungsregeln-satz-ohne-separate-nummer-in-der-mitschrift)
    - [Satz 1.29 (Kettenregel)](#satz-129-kettenregel)
    - [Lemma 1.90 (Mittelwertungleichung)](#lemma-190-mittelwertungleichung)
    - [Gegenbeispiel: Klassischer Mittelwertsatz gilt nicht in Banachräumen](#gegenbeispiel-klassischer-mittelwertsatz-gilt-nicht-in-banachräumen)
  - [Verbindungen](#verbindungen-11)
- [Kapitel 4: Umkehrsatz, Banach-Fixpunktsatz und implizite Funktionen](#kapitel-4-umkehrsatz-banach-fixpunktsatz-und-implizite-funktionen)
  - [Motivation](#motivation-12)
  - [Intuition](#intuition-12)
  - [Formale Definitionen](#formale-definitionen-12)
    - [Definition (Kontraktion)](#definition-kontraktion)
  - [Sätze](#sätze-10)
    - [Satz 1.43 (Banach-Fixpunktsatz)](#satz-143-banach-fixpunktsatz)
    - [Satz 1.42 (Umkehrsatz)](#satz-142-umkehrsatz)
    - [Lemma 1.44 (GL(X,Y) ist offen in L(X,Y) — Stetigkeit der Inversion)](#lemma-144-glxy-ist-offen-in-lxy-stetigkeit-der-inversion)
    - [Satz 1.45 (Satz über implizite Funktionen)](#satz-145-satz-über-implizite-funktionen)
  - [Beispiele](#beispiele-10)
  - [Gegenbeispiele](#gegenbeispiele-10)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-11)
  - [Typische Fehler](#typische-fehler-11)
  - [Verbindungen](#verbindungen-12)
  - [Zusammenfassung Kapitel 3 & 4](#zusammenfassung-kapitel-3-4)
- [Analysis auf allgemeinen linearen Räumen — Teil 3](#analysis-auf-allgemeinen-linearen-räumen-teil-3)
- [Kapitel 5: Höhere Ableitungen und die Taylor-Formel](#kapitel-5-höhere-ableitungen-und-die-taylor-formel)
  - [Motivation](#motivation-13)
  - [Intuition](#intuition-13)
  - [Formale Definitionen](#formale-definitionen-13)
    - [Definition (Iterierte Ableitung)](#definition-iterierte-ableitung)
    - [Definition 1.46 (Räume der Klasse $C^k$)](#definition-146-räume-der-klasse-ck)
    - [Definition 1.47 ($k$-lineare Abbildungen)](#definition-147-k-lineare-abbildungen)
  - [Eigenschaften](#eigenschaften-12)
    - [Lemma 1.48 (Kanonischer Isomorphismus $L^k(X,Y) \cong \tilde L^k(X,Y)$)](#lemma-148-kanonischer-isomorphismus-lkxy-cong-tilde-lkxy)
    - [Lemma 1.65 (Satz von Schwarz — Symmetrie der zweiten Ableitung)](#lemma-165-satz-von-schwarz-symmetrie-der-zweiten-ableitung)
  - [Sätze](#sätze-11)
    - [Satz 1.49 (Taylor-Formel in Banachräumen)](#satz-149-taylor-formel-in-banachräumen)
    - [Korollar 1.66 (Taylorformel im $\mathbb{R}^n$, explizite Koordinatenform)](#korollar-166-taylorformel-im-mathbbrn-explizite-koordinatenform)
  - [Beispiele](#beispiele-11)
  - [Gegenbeispiele](#gegenbeispiele-11)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-12)
  - [Typische Fehler](#typische-fehler-12)
  - [Verbindungen](#verbindungen-13)
- [Kapitel 6: Hilberträume](#kapitel-6-hilberträume)
  - [Motivation](#motivation-14)
  - [Intuition](#intuition-14)
  - [Formale Definitionen](#formale-definitionen-14)
    - [Definition 1.50 (Skalarprodukt)](#definition-150-skalarprodukt)
    - [Definition 1.54 (Hilbertraum)](#definition-154-hilbertraum)
    - [Definition 1.56 (Orthonormalbasis, ONB)](#definition-156-orthonormalbasis-onb)
  - [Eigenschaften](#eigenschaften-13)
    - [Lemma 1.51 (Cauchy-Schwarz-Ungleichung)](#lemma-151-cauchy-schwarz-ungleichung)
    - [Lemma 1.53 (Skalarprodukt induziert Norm)](#lemma-153-skalarprodukt-induziert-norm)
  - [Vergleichstabelle: Die Raumhierarchie](#vergleichstabelle-die-raumhierarchie)
    - [Satz 1.55 & 1.57 (Existenz von Orthonormalbasen, Gram-Schmidt)](#satz-155-157-existenz-von-orthonormalbasen-gram-schmidt)
  - [Algorithmus: Gram-Schmidt-Verfahren](#algorithmus-gram-schmidt-verfahren)
    - [Satz 1.58 (Parseval-artige Entwicklung, Besselsche Ungleichung)](#satz-158-parseval-artige-entwicklung-besselsche-ungleichung)
  - [Beispiele](#beispiele-12)
  - [Gegenbeispiele](#gegenbeispiele-12)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-13)
  - [Typische Fehler](#typische-fehler-13)
  - [Verbindungen](#verbindungen-14)
  - [Zusammenfassung Kapitel 5 & 6](#zusammenfassung-kapitel-5-6)
- [Analysis auf allgemeinen linearen Räumen — Teil 4](#analysis-auf-allgemeinen-linearen-räumen-teil-4)
- [Kapitel 7: Ableitungen im $\mathbb{R}^n$](#kapitel-7-ableitungen-im-mathbbrn)
  - [Motivation](#motivation-15)
  - [Intuition](#intuition-15)
  - [Formale Definitionen](#formale-definitionen-15)
    - [Definition (Vektorwertige Funktionen einer Variablen — Vorstufe)](#definition-vektorwertige-funktionen-einer-variablen-vorstufe)
    - [Definition 1.60 (Partielle Ableitung, Richtungsableitung)](#definition-160-partielle-ableitung-richtungsableitung)
    - [Definition (Jacobi-Matrix)](#definition-jacobi-matrix)
  - [Eigenschaften](#eigenschaften-14)
    - [Lemma 1.61 (Fréchet-differenzierbar $\Rightarrow$ alle partiellen Ableitungen existieren, mit expliziter Formel)](#lemma-161-fréchet-differenzierbar-rightarrow-alle-partiellen-ableitungen-existieren-mit-expliziter-formel)
    - [Satz 1.64 (Stetige partielle Ableitungen $\Rightarrow$ stetig differenzierbar)](#satz-164-stetige-partielle-ableitungen-rightarrow-stetig-differenzierbar)
  - [Gegenbeispiele](#gegenbeispiele-13)
    - [Das Standard-Gegenbeispiel: Partielle Ableitungen existieren, aber $f$ ist nicht differenzierbar](#das-standard-gegenbeispiel-partielle-ableitungen-existieren-aber-f-ist-nicht-differenzierbar)
  - [Vergleichstabelle: Differenzierbarkeitsbegriffe im $\mathbb{R}^n$](#vergleichstabelle-differenzierbarkeitsbegriffe-im-mathbbrn)
  - [Beispiele](#beispiele-13)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-14)
  - [Typische Fehler](#typische-fehler-14)
  - [Verbindungen](#verbindungen-15)
- [Kapitel 8: Extrema — frei und mit Nebenbedingungen](#kapitel-8-extrema-frei-und-mit-nebenbedingungen)
  - [Motivation](#motivation-16)
  - [Intuition](#intuition-16)
  - [Formale Definitionen](#formale-definitionen-16)
    - [Definition 1.67 (Extrema)](#definition-167-extrema)
    - [Definition 1.69 (Kritischer Punkt)](#definition-169-kritischer-punkt)
    - [Definition (Gradient)](#definition-gradient)
    - [Definition (Hesse-Matrix)](#definition-hesse-matrix)
    - [Definition 1.71 (Definitheit)](#definition-171-definitheit)
    - [Definition 1.73 (Mannigfaltigkeit)](#definition-173-mannigfaltigkeit)
    - [Definition 1.74 (Tangentialvektor, Tangentialraum)](#definition-174-tangentialvektor-tangentialraum)
  - [Sätze](#sätze-12)
    - [Satz 1.70 (Notwendige Bedingung erster Ordnung)](#satz-170-notwendige-bedingung-erster-ordnung)
    - [Satz 1.72 (Hinreichende Bedingung zweiter Ordnung)](#satz-172-hinreichende-bedingung-zweiter-ordnung)
    - [Satz 1.78 (Lagrange-Multiplikatorenregel)](#satz-178-lagrange-multiplikatorenregel)
    - [Lemma 1.75/1.76 (Tangentialraum = Kern der Ableitung der Nebenbedingung)](#lemma-175176-tangentialraum-kern-der-ableitung-der-nebenbedingung)
  - [Beispiele](#beispiele-14)
  - [Gegenbeispiele](#gegenbeispiele-14)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-15)
  - [Typische Fehler](#typische-fehler-15)
  - [Verbindungen](#verbindungen-16)
  - [Zusammenfassung Kapitel 7 & 8](#zusammenfassung-kapitel-7-8)
- [Analysis auf allgemeinen linearen Räumen — Teil 5](#analysis-auf-allgemeinen-linearen-räumen-teil-5)
- [Kapitel 9: Globale Approximation von Funktionen](#kapitel-9-globale-approximation-von-funktionen)
  - [Motivation](#motivation-17)
  - [Intuition](#intuition-17)
  - [Formale Definitionen](#formale-definitionen-17)
    - [Definition 1.80 (Punktweise und gleichmäßige Konvergenz)](#definition-180-punktweise-und-gleichmäßige-konvergenz)
    - [Definition 1.82/1.83 (Kompakter Träger, Faltung, Dirac-Folge)](#definition-182183-kompakter-träger-faltung-dirac-folge)
  - [Eigenschaften](#eigenschaften-15)
    - [Beispiele für Dirac-Folgen](#beispiele-für-dirac-folgen)
  - [Sätze](#sätze-13)
    - [Satz 1.81 (Gleichmäßiger Grenzwert stetiger Funktionen ist stetig)](#satz-181-gleichmäßiger-grenzwert-stetiger-funktionen-ist-stetig)
    - [Lemma 1.84 (Konvolution mit Dirac-Folge konvergiert gegen die Funktion)](#lemma-184-konvolution-mit-dirac-folge-konvergiert-gegen-die-funktion)
    - [Satz 1.85 (Weierstraßscher Approximationssatz)](#satz-185-weierstraßscher-approximationssatz)
  - [Vergleichstabelle: Punktweise vs. gleichmäßige Konvergenz](#vergleichstabelle-punktweise-vs-gleichmäßige-konvergenz)
  - [Beispiele](#beispiele-15)
  - [Gegenbeispiele](#gegenbeispiele-15)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-16)
  - [Typische Fehler](#typische-fehler-16)
  - [Verbindungen](#verbindungen-17)
  - [Zusammenfassung Kapitel 9](#zusammenfassung-kapitel-9)
- [Kapitel 10: Integration auf $\mathbb{R}^n$](#kapitel-10-integration-auf-mathbbrn)
  - [Motivation](#motivation-18)
  - [Intuition](#intuition-18)
  - [Formale Definitionen](#formale-definitionen-18)
    - [Definition 2.1 (Elementare Stufenfunktion)](#definition-21-elementare-stufenfunktion)
    - [Definition 2.3 (Integral elementarer Stufenfunktionen)](#definition-23-integral-elementarer-stufenfunktionen)
    - [Definition 2.5 (Ober- und Unterintegral)](#definition-25-ober-und-unterintegral)
    - [Definition 2.6 (Riemann-Integrierbarkeit)](#definition-26-riemann-integrierbarkeit)
  - [Sätze](#sätze-14)
    - [Satz 2.7 (Stetige Funktionen mit kompaktem Träger sind Riemann-integrierbar)](#satz-27-stetige-funktionen-mit-kompaktem-träger-sind-riemann-integrierbar)
    - [Satz 2.8 (Satz von Fubini)](#satz-28-satz-von-fubini)
    - [Satz 2.9 (Transformationssatz)](#satz-29-transformationssatz)
    - [Lemma 2.10 (Volumen = Determinante, via Gram-Schmidt)](#lemma-210-volumen-determinante-via-gram-schmidt)
  - [Algorithmus: Polarkoordinaten als Standardanwendung des Transformationssatzes](#algorithmus-polarkoordinaten-als-standardanwendung-des-transformationssatzes)
  - [Beispiele](#beispiele-16)
  - [Gegenbeispiele](#gegenbeispiele-16)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-17)
  - [Typische Fehler](#typische-fehler-17)
  - [Verbindungen](#verbindungen-18)
  - [Zusammenfassung Kapitel 10](#zusammenfassung-kapitel-10)
- [Analysis auf allgemeinen linearen Räumen — Teil 6 (Abschluss)](#analysis-auf-allgemeinen-linearen-räumen-teil-6-abschluss)
- [Kapitel 11: Kurvenintegrale und Differentialformen](#kapitel-11-kurvenintegrale-und-differentialformen)
  - [Motivation](#motivation-19)
  - [Intuition](#intuition-19)
  - [Formale Definitionen](#formale-definitionen-19)
    - [Definition (Kurve und Parametrisierung)](#definition-kurve-und-parametrisierung)
    - [Definition 3.1 (Äquivalenz von Parametrisierungen)](#definition-31-äquivalenz-von-parametrisierungen)
    - [Definition 3.2 (Kurve)](#definition-32-kurve)
    - [Definition 3.3 (Länge einer Kurve, Bogenlänge)](#definition-33-länge-einer-kurve-bogenlänge)
    - [Definition (Vektorfeld, Differentialform)](#definition-vektorfeld-differentialform)
    - [Definition 3.4 (Exakte und geschlossene Formen)](#definition-34-exakte-und-geschlossene-formen)
    - [Definition 3.7 (Integral einer Differentialform längs einer Kurve)](#definition-37-integral-einer-differentialform-längs-einer-kurve)
  - [Eigenschaften](#eigenschaften-16)
    - [Lemma 3.5 (Exakt $\Rightarrow$ geschlossen)](#lemma-35-exakt-rightarrow-geschlossen)
  - [Sätze](#sätze-15)
    - [Satz 3.8 (Hauptsatz für Kurvenintegrale — Wegunabhängigkeit exakter Formen)](#satz-38-hauptsatz-für-kurvenintegrale-wegunabhängigkeit-exakter-formen)
    - [Satz 3.8a (Umkehrung — Wegunabhängigkeit $\Rightarrow$ Exaktheit)](#satz-38a-umkehrung-wegunabhängigkeit-rightarrow-exaktheit)
  - [Gegenbeispiele](#gegenbeispiele-17)
    - [Das klassische Gegenbeispiel: Geschlossen, aber nicht exakt](#das-klassische-gegenbeispiel-geschlossen-aber-nicht-exakt)
  - [Beispiele](#beispiele-17)
  - [Vergleichstabelle: exakt vs. geschlossen](#vergleichstabelle-exakt-vs-geschlossen)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-18)
  - [Typische Fehler](#typische-fehler-18)
  - [Verbindungen](#verbindungen-19)
  - [Zusammenfassung Kapitel 11](#zusammenfassung-kapitel-11)
- [Kapitel 12: Komplexe Analysis](#kapitel-12-komplexe-analysis)
  - [Motivation](#motivation-20)
  - [Intuition](#intuition-20)
  - [Formale Definitionen](#formale-definitionen-20)
    - [Definition 4.1 (Komplexe Zahlen)](#definition-41-komplexe-zahlen)
    - [Satz 4.3 (Fundamentalsatz der Algebra)](#satz-43-fundamentalsatz-der-algebra)
    - [Definition 4.4 (Komplexe Differenzierbarkeit)](#definition-44-komplexe-differenzierbarkeit)
    - [Definition 4.6 (Holomorphie)](#definition-46-holomorphie)
  - [Sätze](#sätze-16)
    - [Lemma 4.5 (Cauchy-Riemann-Gleichungen)](#lemma-45-cauchy-riemann-gleichungen)
  - [Beispiele](#beispiele-18)
  - [Gegenbeispiele](#gegenbeispiele-18)
  - [Kurvenintegrale in $\mathbb{C}$ und der Cauchysche Integralsatz](#kurvenintegrale-in-mathbbc-und-der-cauchysche-integralsatz)
    - [Definition 4.10 (Komplexes Kurvenintegral)](#definition-410-komplexes-kurvenintegral)
    - [Zusammenhang mit reellen 1-Formen](#zusammenhang-mit-reellen-1-formen)
    - [Satz 4.12 (Cauchyscher Integralsatz)](#satz-412-cauchyscher-integralsatz)
  - [Vergleichstabelle: Reelle vs. komplexe Differenzierbarkeit](#vergleichstabelle-reelle-vs-komplexe-differenzierbarkeit)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-19)
  - [Typische Fehler](#typische-fehler-19)
  - [Verbindungen](#verbindungen-20)
  - [Zusammenfassung Kapitel 12](#zusammenfassung-kapitel-12)
- [Gesamtübersicht: Der rote Faden der Vorlesung](#gesamtübersicht-der-rote-faden-der-vorlesung)
- [Physik II — Vollständiges Skript](#physik-ii-vollständiges-skript)
  - [Teil I: Mechanik der Fluide und Wärmelehre](#teil-i-mechanik-der-fluide-und-wärmelehre)
- [Inhaltsverzeichnis Teil I](#inhaltsverzeichnis-teil-i)
- [Kapitel 1: Strömende Flüssigkeiten und Gase](#kapitel-1-strömende-flüssigkeiten-und-gase)
  - [Motivation](#motivation-21)
  - [Intuition](#intuition-21)
  - [Formale Definitionen](#formale-definitionen-21)
  - [Eigenschaften](#eigenschaften-17)
  - [Sätze](#sätze-17)
    - [Satz 1.1 (Kontinuitätsgleichung)](#satz-11-kontinuitätsgleichung)
    - [Beweis von Satz 1.1](#beweis-von-satz-11)
    - [Satz 1.2 (Bernoulli-Gleichung)](#satz-12-bernoulli-gleichung)
    - [Beweis von Satz 1.2](#beweis-von-satz-12)
    - [Satz 1.3 (Hagen-Poiseuille-Gesetz)](#satz-13-hagen-poiseuille-gesetz)
    - [Beweis von Satz 1.3 (Beweisidee, da nicht vollständig aus den Grundgleichungen hergeleitet, sondern über Kräftebilanz)](#beweis-von-satz-13-beweisidee-da-nicht-vollständig-aus-den-grundgleichungen-hergeleitet-sondern-über-kräftebilanz)
    - [Satz 1.4 (Stokes'sches Gesetz)](#satz-14-stokessches-gesetz)
  - [Algorithmen](#algorithmen-9)
  - [Beispiele](#beispiele-19)
  - [Gegenbeispiele](#gegenbeispiele-19)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-20)
  - [Typische Fehler](#typische-fehler-20)
  - [Verbindungen](#verbindungen-21)
  - [Zusammenfassung](#zusammenfassung-9)
- [Kapitel 2: Kinetische Gastheorie und Temperatur](#kapitel-2-kinetische-gastheorie-und-temperatur)
  - [Motivation](#motivation-22)
  - [Intuition](#intuition-22)
  - [Formale Definitionen](#formale-definitionen-22)
  - [Eigenschaften](#eigenschaften-18)
  - [Sätze](#sätze-18)
    - [Satz 2.1 (Kinetische Druckformel)](#satz-21-kinetische-druckformel)
    - [Beweis von Satz 2.1](#beweis-von-satz-21)
    - [Satz 2.2 (Gleichverteilungssatz / Äquipartitionstheorem)](#satz-22-gleichverteilungssatz-äquipartitionstheorem)
    - [Satz 2.3 (Kombination von Gasgesetzen zur idealen Gasgleichung)](#satz-23-kombination-von-gasgesetzen-zur-idealen-gasgleichung)
  - [Algorithmen](#algorithmen-10)
  - [Beispiele](#beispiele-20)
  - [Gegenbeispiele](#gegenbeispiele-20)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-21)
  - [Typische Fehler](#typische-fehler-21)
  - [Verbindungen](#verbindungen-22)
  - [Zusammenfassung](#zusammenfassung-10)
- [Kapitel 3: Transportphänomene](#kapitel-3-transportphänomene)
  - [Motivation](#motivation-23)
  - [Intuition](#intuition-23)
  - [Formale Definitionen](#formale-definitionen-23)
  - [Eigenschaften](#eigenschaften-19)
  - [Sätze](#sätze-19)
    - [Satz 3.1 (2. Fick'sches Gesetz aus Kontinuität + 1. Fick'schem Gesetz)](#satz-31-2-ficksches-gesetz-aus-kontinuität-1-fickschem-gesetz)
    - [Satz 3.2 (Analogie Diffusionsgleichung — Wärmeleitungsgleichung)](#satz-32-analogie-diffusionsgleichung-wärmeleitungsgleichung)
  - [Algorithmen](#algorithmen-11)
  - [Beispiele](#beispiele-21)
  - [Gegenbeispiele](#gegenbeispiele-21)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-22)
  - [Typische Fehler](#typische-fehler-22)
  - [Verbindungen](#verbindungen-23)
  - [Zusammenfassung](#zusammenfassung-11)
- [Kapitel 4: Wärme, Arbeit und der 1. Hauptsatz der Thermodynamik](#kapitel-4-wärme-arbeit-und-der-1-hauptsatz-der-thermodynamik)
  - [Motivation](#motivation-24)
  - [Intuition](#intuition-24)
  - [Formale Definitionen](#formale-definitionen-24)
  - [Eigenschaften](#eigenschaften-20)
  - [Sätze](#sätze-20)
    - [Satz 4.1 (1. Hauptsatz der Thermodynamik)](#satz-41-1-hauptsatz-der-thermodynamik)
    - [Satz 4.2 ($C_p - C_V = R$, "Robert-Mayer-Beziehung")](#satz-42-c_p-c_v-r-robert-mayer-beziehung)
    - [Beweis von Satz 4.2](#beweis-von-satz-42)
    - [Satz 4.3 (Adiabatengleichungen)](#satz-43-adiabatengleichungen)
    - [Beweis von Satz 4.3](#beweis-von-satz-43)
  - [Algorithmen](#algorithmen-12)
  - [Beispiele](#beispiele-22)
  - [Gegenbeispiele](#gegenbeispiele-22)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-23)
  - [Typische Fehler](#typische-fehler-23)
  - [Verbindungen](#verbindungen-24)
  - [Zusammenfassung](#zusammenfassung-12)
- [Kapitel 5: Kreisprozesse und der 2. Hauptsatz der Thermodynamik](#kapitel-5-kreisprozesse-und-der-2-hauptsatz-der-thermodynamik)
  - [Motivation](#motivation-25)
  - [Intuition](#intuition-25)
  - [Formale Definitionen](#formale-definitionen-25)
  - [Eigenschaften](#eigenschaften-21)
  - [Sätze](#sätze-21)
    - [Satz 5.1 (Carnot-Wirkungsgrad)](#satz-51-carnot-wirkungsgrad)
    - [Beweis von Satz 5.1](#beweis-von-satz-51)
    - [Satz 5.2 (Carnot'scher Satz — Optimalität)](#satz-52-carnotscher-satz-optimalität)
    - [Satz 5.3 (Entropieänderung bei Zustandsänderungen idealer Gase)](#satz-53-entropieänderung-bei-zustandsänderungen-idealer-gase)
    - [Satz 5.4 (2. Hauptsatz — Entropiezunahme in abgeschlossenen Systemen)](#satz-54-2-hauptsatz-entropiezunahme-in-abgeschlossenen-systemen)
    - [Satz 5.5 (Boltzmann-Entropie und statistische Interpretation)](#satz-55-boltzmann-entropie-und-statistische-interpretation)
  - [Algorithmen](#algorithmen-13)
  - [Beispiele](#beispiele-23)
  - [Gegenbeispiele](#gegenbeispiele-23)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-24)
  - [Typische Fehler](#typische-fehler-24)
  - [Verbindungen](#verbindungen-25)
  - [Zusammenfassung](#zusammenfassung-13)
- [Physik II — Vollständiges Skript](#physik-ii-vollständiges-skript-1)
  - [Teil II: Elektromagnetismus](#teil-ii-elektromagnetismus)
- [Inhaltsverzeichnis Teil II](#inhaltsverzeichnis-teil-ii)
- [Kapitel 6: Elektrostatik I — Ladung, Coulombgesetz, elektrisches Feld, Potential](#kapitel-6-elektrostatik-i-ladung-coulombgesetz-elektrisches-feld-potential)
  - [Motivation](#motivation-26)
  - [Intuition](#intuition-26)
  - [Formale Definitionen](#formale-definitionen-26)
  - [Eigenschaften](#eigenschaften-22)
  - [Sätze](#sätze-22)
    - [Satz 6.1 (Wegunabhängigkeit der Arbeit im elektrostatischen Feld)](#satz-61-wegunabhängigkeit-der-arbeit-im-elektrostatischen-feld)
    - [Satz 6.2 (Feld einer unendlich ausgedehnten geladenen Platte)](#satz-62-feld-einer-unendlich-ausgedehnten-geladenen-platte)
  - [Algorithmen](#algorithmen-14)
  - [Beispiele](#beispiele-24)
  - [Gegenbeispiele](#gegenbeispiele-24)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-25)
  - [Typische Fehler](#typische-fehler-25)
  - [Verbindungen](#verbindungen-26)
  - [Zusammenfassung](#zusammenfassung-14)
- [Kapitel 7: Elektrostatik II — Gauß'sches Gesetz, Leiter, Kondensatoren](#kapitel-7-elektrostatik-ii-gaußsches-gesetz-leiter-kondensatoren)
  - [Motivation](#motivation-27)
  - [Intuition](#intuition-27)
  - [Formale Definitionen](#formale-definitionen-27)
  - [Eigenschaften](#eigenschaften-23)
  - [Sätze](#sätze-23)
    - [Satz 7.1 (Gauß'sches Gesetz, integral)](#satz-71-gaußsches-gesetz-integral)
    - [Satz 7.2 (Gauß'sches Gesetz, differentiell — 1. Maxwell-Gleichung)](#satz-72-gaußsches-gesetz-differentiell-1-maxwell-gleichung)
    - [Satz 7.3 (Feld einer geladenen Kugel — innen und außen)](#satz-73-feld-einer-geladenen-kugel-innen-und-außen)
    - [Satz 7.4 (Kondensatorformeln)](#satz-74-kondensatorformeln)
    - [Satz 7.5 (Energie des elektrischen Feldes im Kondensator)](#satz-75-energie-des-elektrischen-feldes-im-kondensator)
  - [Algorithmen](#algorithmen-15)
  - [Beispiele](#beispiele-25)
  - [Gegenbeispiele](#gegenbeispiele-25)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-26)
  - [Typische Fehler](#typische-fehler-26)
  - [Verbindungen](#verbindungen-27)
  - [Zusammenfassung](#zusammenfassung-15)
- [Kapitel 8: Elektrostatik III — Dielektrika, Materie im elektrischen Feld](#kapitel-8-elektrostatik-iii-dielektrika-materie-im-elektrischen-feld)
  - [Motivation](#motivation-28)
  - [Intuition](#intuition-28)
  - [Formale Definitionen](#formale-definitionen-28)
  - [Eigenschaften](#eigenschaften-24)
  - [Sätze](#sätze-24)
    - [Satz 8.1 (Div $\vec D$ = freie Ladungsdichte — Maxwell-Gleichung in Materie)](#satz-81-div-vec-d-freie-ladungsdichte-maxwell-gleichung-in-materie)
    - [Satz 8.2 (Brechungsgesetz für das E-Feld an einer dielektrischen Grenzfläche)](#satz-82-brechungsgesetz-für-das-e-feld-an-einer-dielektrischen-grenzfläche)
    - [Satz 8.3 (Kapazität und Feldenergie mit Dielektrikum)](#satz-83-kapazität-und-feldenergie-mit-dielektrikum)
  - [Algorithmen](#algorithmen-16)
  - [Beispiele](#beispiele-26)
  - [Gegenbeispiele](#gegenbeispiele-26)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-27)
  - [Typische Fehler](#typische-fehler-27)
  - [Verbindungen](#verbindungen-28)
  - [Zusammenfassung](#zusammenfassung-16)
- [Kapitel 9: Elektrischer Strom und Gleichstromkreise](#kapitel-9-elektrischer-strom-und-gleichstromkreise)
  - [Motivation](#motivation-29)
  - [Intuition](#intuition-29)
  - [Formale Definitionen](#formale-definitionen-29)
  - [Eigenschaften](#eigenschaften-25)
  - [Sätze](#sätze-25)
    - [Satz 9.1 (Kontinuitätsgleichung für elektrische Ladung)](#satz-91-kontinuitätsgleichung-für-elektrische-ladung)
    - [Satz 9.2 (Mikroskopische Herleitung des Ohm'schen Gesetzes)](#satz-92-mikroskopische-herleitung-des-ohmschen-gesetzes)
    - [Satz 9.3 (Kirchhoff'sche Regeln)](#satz-93-kirchhoffsche-regeln)
    - [Satz 9.4 (Ersatzwiderstände: Reihen- und Parallelschaltung)](#satz-94-ersatzwiderstände-reihen-und-parallelschaltung)
  - [Algorithmen](#algorithmen-17)
  - [Beispiele](#beispiele-27)
  - [Gegenbeispiele](#gegenbeispiele-27)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-28)
  - [Typische Fehler](#typische-fehler-28)
  - [Verbindungen](#verbindungen-29)
  - [Zusammenfassung](#zusammenfassung-17)
- [Kapitel 10: Ladungstransport in Materialien](#kapitel-10-ladungstransport-in-materialien)
  - [Motivation](#motivation-30)
  - [Intuition](#intuition-30)
  - [Formale Definitionen](#formale-definitionen-30)
  - [Eigenschaften](#eigenschaften-26)
  - [Sätze](#sätze-26)
    - ["Satz" 10.1 (Wiedemann-Franz-Gesetz, Wiederholung/Vertiefung aus Kapitel 3)](#satz-101-wiedemann-franz-gesetz-wiederholungvertiefung-aus-kapitel-3)
  - [Algorithmen](#algorithmen-18)
  - [Beispiele](#beispiele-28)
  - [Gegenbeispiele](#gegenbeispiele-28)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-29)
  - [Typische Fehler](#typische-fehler-29)
  - [Verbindungen](#verbindungen-30)
  - [Zusammenfassung](#zusammenfassung-18)
- [Kapitel 11: Magnetismus I — Kraftwirkungen (Lorentzkraft)](#kapitel-11-magnetismus-i-kraftwirkungen-lorentzkraft)
  - [Motivation](#motivation-31)
  - [Intuition](#intuition-31)
  - [Formale Definitionen](#formale-definitionen-31)
  - [Eigenschaften](#eigenschaften-27)
  - [Sätze](#sätze-27)
    - [Satz 11.1 (Kreisbahn im homogenen Magnetfeld)](#satz-111-kreisbahn-im-homogenen-magnetfeld)
    - [Satz 11.2 (Hall-Effekt)](#satz-112-hall-effekt)
  - [Algorithmen](#algorithmen-19)
  - [Beispiele](#beispiele-29)
  - [Gegenbeispiele](#gegenbeispiele-29)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-30)
  - [Typische Fehler](#typische-fehler-30)
  - [Verbindungen](#verbindungen-31)
  - [Zusammenfassung](#zusammenfassung-19)
- [Kapitel 12: Magnetismus II — Feldquellen und magnetische Materialien](#kapitel-12-magnetismus-ii-feldquellen-und-magnetische-materialien)
  - [Motivation](#motivation-32)
  - [Intuition](#intuition-32)
  - [Formale Definitionen](#formale-definitionen-32)
  - [Eigenschaften](#eigenschaften-28)
  - [Sätze](#sätze-28)
    - [Satz 12.1 (Div B = 0 — 2. Maxwell-Gleichung)](#satz-121-div-b-0-2-maxwell-gleichung)
    - [Satz 12.2 (Magnetfeld eines geraden, unendlich langen Leiters)](#satz-122-magnetfeld-eines-geraden-unendlich-langen-leiters)
    - [Satz 12.3 (Ampère'sches Gesetz)](#satz-123-ampèresches-gesetz)
    - [Satz 12.4 (Magnetfeld einer langen Spule)](#satz-124-magnetfeld-einer-langen-spule)
  - [Algorithmen](#algorithmen-20)
  - [Beispiele](#beispiele-30)
  - [Gegenbeispiele](#gegenbeispiele-30)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-31)
  - [Typische Fehler](#typische-fehler-31)
  - [Verbindungen](#verbindungen-32)
  - [Zusammenfassung](#zusammenfassung-20)
- [Kapitel 13: Elektrodynamik — Induktion](#kapitel-13-elektrodynamik-induktion)
  - [Motivation](#motivation-33)
  - [Intuition](#intuition-33)
  - [Formale Definitionen](#formale-definitionen-33)
  - [Eigenschaften](#eigenschaften-29)
  - [Sätze](#sätze-29)
    - [Satz 13.1 (Faraday'sches Induktionsgesetz — 3. Maxwell-Gleichung)](#satz-131-faradaysches-induktionsgesetz-3-maxwell-gleichung)
    - [Satz 13.2 (Selbstinduktion und Aufbauverhalten in einer RL-Schaltung)](#satz-132-selbstinduktion-und-aufbauverhalten-in-einer-rl-schaltung)
  - [Algorithmen](#algorithmen-21)
  - [Beispiele](#beispiele-31)
  - [Gegenbeispiele](#gegenbeispiele-31)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-32)
  - [Typische Fehler](#typische-fehler-32)
  - [Verbindungen](#verbindungen-33)
  - [Zusammenfassung](#zusammenfassung-21)
- [Kapitel 14: Wechselstromkreise](#kapitel-14-wechselstromkreise)
  - [Motivation](#motivation-34)
  - [Intuition](#intuition-34)
  - [Formale Definitionen](#formale-definitionen-34)
  - [Eigenschaften](#eigenschaften-30)
  - [Sätze](#sätze-30)
    - [Satz 14.1 (Impedanz des Kondensators)](#satz-141-impedanz-des-kondensators)
    - [Satz 14.2 (Impedanz der Spule)](#satz-142-impedanz-der-spule)
    - [Satz 14.3 (Kirchhoff'sche Regeln gelten unverändert für komplexe Größen)](#satz-143-kirchhoffsche-regeln-gelten-unverändert-für-komplexe-größen)
  - [Algorithmen](#algorithmen-22)
  - [Beispiele](#beispiele-32)
  - [Gegenbeispiele](#gegenbeispiele-32)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-33)
  - [Typische Fehler](#typische-fehler-33)
  - [Verbindungen](#verbindungen-34)
  - [Zusammenfassung](#zusammenfassung-22)
- [Kapitel 15: Elektromagnetische Wellen](#kapitel-15-elektromagnetische-wellen)
  - [Motivation](#motivation-35)
  - [Intuition](#intuition-35)
  - [Formale Definitionen](#formale-definitionen-35)
  - [Eigenschaften](#eigenschaften-31)
  - [Sätze](#sätze-31)
    - [Satz 15.1 (Wellengleichung aus den Maxwell-Gleichungen)](#satz-151-wellengleichung-aus-den-maxwell-gleichungen)
    - [Satz 15.2 (Ebene, harmonische Welle — Struktureigenschaften)](#satz-152-ebene-harmonische-welle-struktureigenschaften)
  - [Algorithmen](#algorithmen-23)
  - [Beispiele](#beispiele-33)
  - [Gegenbeispiele](#gegenbeispiele-33)
  - [Typische Klausuraufgaben](#typische-klausuraufgaben-34)
  - [Typische Fehler](#typische-fehler-34)
  - [Verbindungen](#verbindungen-35)
  - [Zusammenfassung](#zusammenfassung-23)
- [Kapitel 16: Exkurs — Lorentz-Transformation und Spezielle Relativitätstheorie](#kapitel-16-exkurs-lorentz-transformation-und-spezielle-relativitätstheorie)
  - [Motivation](#motivation-36)
  - [Grundidee](#grundidee)
  - [Formeln](#formeln)
  - [Beispiel 1: Zwillingsparadoxon (qualitativ)](#beispiel-1-zwillingsparadoxon-qualitativ)
  - [Beispiel 2: Myonenparadoxon (quantitativ)](#beispiel-2-myonenparadoxon-quantitativ)
  - [Zusammenfassung](#zusammenfassung-24)

---

<a id="kapitel-0-polynome-teilbarkeit-und-faktorisierung"></a>
# Kapitel 0 — Polynome, Teilbarkeit und Faktorisierung

> **Stellung im Kurs.** Dieses Kapitel ist das algebraische Fundament der gesamten Vorlesung.
> Die zentralen Objekte der Linearen Algebra 2 — charakteristisches Polynom, Minimalpolynom,
> Diagonalisierbarkeit, Trigonalisierbarkeit, Jordan-Normalform — leben *von der Faktorisierung
> von Polynomen*. Wer hier sicher ist, versteht später, *warum* eine Matrix diagonalisierbar ist
> oder nicht, statt es nur zu rechnen.

---

<a id="motivation"></a>
## Motivation

In der Linearen Algebra 1 ging es um Vektorräume und lineare Abbildungen. In der Linearen Algebra 2 stellt sich eine schärfere Frage:

> **Leitfrage des Kurses.** Gegeben eine lineare Abbildung $f\colon V\to V$ (bzw. eine quadratische Matrix $A$). Gibt es eine Basis, bezüglich der die darstellende Matrix *besonders einfach* aussieht — diagonal, oder wenigstens obere Dreiecksmatrix, oder in **Jordan-Normalform**?

Die Antwort hängt vollständig davon ab, wie sich ein einziges Polynom — das **charakteristische Polynom** $\chi_f$ — in Faktoren zerlegen lässt:

- $\chi_f$ zerfällt in *verschiedene* Linearfaktoren $\;\Rightarrow\;$ $f$ ist diagonalisierbar.
- $\chi_f$ zerfällt in Linearfaktoren (mit Vielfachheiten) $\;\Rightarrow\;$ $f$ ist trigonalisierbar / besitzt eine Jordan-Normalform.
- $\chi_f$ zerfällt *nicht* $\;\Rightarrow\;$ keine dieser Normalformen über dem Grundkörper.

Um diese Sätze überhaupt formulieren und beweisen zu können, brauchen wir eine **Theorie der Teilbarkeit von Polynomen**: Was heißt „ein Polynom teilt ein anderes"? Was sind die „unzerlegbaren Bausteine" (analog zu Primzahlen)? Wann ist die Zerlegung *eindeutig*?

**Mathematische und historische Wurzel.** Die entscheidende Beobachtung ist eine **strukturelle Analogie**:

$$
\boxed{\;\mathbb{Z}\ (\text{ganze Zahlen})\quad\longleftrightarrow\quad k[X]\ (\text{Polynome über einem Körper})\;}
$$

In beiden Ringen kann man **mit Rest dividieren** (Euklid, ca. 300 v. Chr., ursprünglich für ganze Zahlen). Aus der Division mit Rest folgt — in beiden Welten mit *demselben* Argument —:

1. die Existenz eines **größten gemeinsamen Teilers** (ggT), darstellbar als Linearkombination (**Bézout**),
2. die Tatsache, dass **irreduzibel = prim** gilt,
3. die **eindeutige Primfaktorzerlegung** (für $\mathbb{Z}$: Fundamentalsatz der Arithmetik; für $k[X]$: eindeutige Polynomzerlegung).

Wir entwickeln deshalb beide Theorien **parallel**. Das spart nicht nur Arbeit — es macht sichtbar, dass „Primzahl" und „irreduzibles Polynom" *dasselbe Konzept in zwei Kostümen* sind. Ringe mit Division-mit-Rest heißen **euklidische Ringe**; sie sind der gemeinsame Rahmen.

---

<a id="intuition"></a>
## Intuition

**Polynome verhalten sich wie ganze Zahlen.** Stell dir $k[X]$ als ein „Zahlensystem" vor:

| Begriff in $\mathbb{Z}$ | Begriff in $k[X]$ | gemeinsame Idee |
|---|---|---|
| Betrag $\lvert n\rvert$ | Grad $\deg P$ | **Größenmaß** zum Vergleichen / Abbrechen |
| Einheiten $\{+1,-1\}$ | Konstanten $\neq 0$ | „unsichtbare" Faktoren, die nichts zerlegen |
| Primzahl $2,3,5,\dots$ | irreduzibles Polynom | **unzerlegbarer Baustein** |
| $6 = 2\cdot 3$ | $X^2-1=(X-1)(X+1)$ | Zerlegung in Bausteine |
| ggT$(12,8)=4$ | ggT$(X^2-1,\,X-1)=X-1$ | größter gemeinsamer Teiler |

Ein **irreduzibles** Element ist eines, das man *nicht weiter zerschlagen* kann, ohne dass ein Stück eine Einheit (ein „trivialer" Faktor) ist — so wie $7$ sich nur als $7=1\cdot 7$ oder $7=(-1)\cdot(-7)$ schreiben lässt.

Der **Grad** ist der Schlüssel: Beim Dividieren $P = A\cdot Q + R$ ist der Rest $R$ *echt kleiner* (im Grad) als der Divisor $Q$. Diese „Verkleinerung bei jedem Schritt" ist genau, was den **Euklidischen Algorithmus** zum Stoppen bringt — exakt wie bei ganzen Zahlen, wo der Rest betragsmäßig schrumpft.

**Warum Eindeutigkeit nicht selbstverständlich ist.** Dass $12 = 2\cdot 2\cdot 3$ die *einzige* Primzerlegung ist (bis auf Reihenfolge), beweist man — es ist ein Satz, kein Axiom. In „exotischeren" Zahlbereichen kann die Eindeutigkeit *scheitern* (siehe Gegenbeispiel $\mathbb{Z}[\sqrt5]$). Der Grund, warum sie in $\mathbb{Z}$ und $k[X]$ *gilt*, ist genau die Division mit Rest.

---

<a id="formale-definitionen"></a>
## Formale Definitionen

Im ganzen Kapitel ist $k$ ein **Körper** (z. B. $\mathbb{Q},\mathbb{R},\mathbb{C},\mathbb{F}_p$).

<a id="polynomring"></a>
### Polynomring

**Definition 0.1 (Polynomring).**
Der **Polynomring** $k[X]$ ist die Menge aller formalen Ausdrücke

$$
P = a_n X^n + a_{n-1}X^{n-1} + \dots + a_1 X + a_0,\qquad n\in\mathbb{N}_0,\ a_0,\dots,a_n\in k,
$$

mit der üblichen Addition und Multiplikation. Mit diesen Operationen ist $k[X]$ ein **kommutativer Ring mit Eins**:

- **Nullelement:** das Nullpolynom $0$ (alle $a_i=0$),
- **Einselement:** das konstante Polynom $1$.

Zugleich ist $k[X]$ ein **$k$-Vektorraum** (mit Basis $1, X, X^2, X^3, \dots$, also unendlichdimensional).

> *Erläuterung.* „Formal" heißt: Ein Polynom ist die Folge seiner Koeffizienten $(a_0,a_1,\dots)$, nicht die durch es definierte Funktion. Diese Unterscheidung ist wichtig — über endlichen Körpern können verschiedene Polynome dieselbe Funktion liefern (siehe Gegenbeispiele).

<a id="grad"></a>
### Grad

**Definition 0.2 (Grad).**
Für $P = a_nX^n+\dots+a_0$ mit $a_n\neq 0$ ist der **Grad** $\deg P := n$ und $a_n$ der **Leitkoeffizient**. Für das Nullpolynom setzt man

$$
\deg(0) := -\infty,
$$

mit den Rechenkonventionen $-\infty < n$ und $-\infty + n = -\infty$ für alle $n\in\mathbb{N}_0$.

**Definition 0.3 (normiert).**
$P$ heißt **normiert** (engl. *monic*), wenn sein Leitkoeffizient $a_n = 1$ ist.

<a id="nullteilerfreiheit-einheiten"></a>
### Nullteilerfreiheit, Einheiten

**Definition 0.4 (Nullteilerfrei / Integritätsring).**
Ein kommutativer Ring $R$ (mit $1\neq 0$) heißt **nullteilerfrei** (oder **Integritätsring**), wenn für alle $a,b\in R$ gilt:

$$
a\neq 0\ \text{und}\ b\neq 0 \;\Longrightarrow\; a\cdot b\neq 0.
$$

Äquivalent: aus $a\cdot b = 0$ folgt $a=0$ oder $b=0$.

**Definition 0.5 (Einheit / invertierbar).**
Ein Element $a\in R$ heißt **invertierbar** (eine **Einheit**), wenn es $b\in R$ mit $a\cdot b = 1$ gibt. Die Menge der Einheiten heißt $R^\times$.

<a id="teilbarkeit-irreduzibel-prim"></a>
### Teilbarkeit, irreduzibel, prim

**Definition 0.6 (Teilbarkeit).**
Seien $x,a\in R$. Man sagt **$a$ teilt $x$** (schreibe $a\mid x$), wenn es $b\in R$ mit $x = a\cdot b$ gibt.

**Definition 0.7 (assoziiert).**
$x,y\in R$ heißen **assoziiert**, wenn $x = u\cdot y$ für eine Einheit $u\in R^\times$. (In $\mathbb{Z}$: $x$ und $-x$. In $k[X]$: $P$ und $c\cdot P$ für $c\in k\setminus\{0\}$.)

**Definition 0.8 (irreduzibel und prim).**
Sei $R$ ein nullteilerfreier kommutativer Ring und $x\in R\setminus\{0\}$ keine Einheit.

- $x$ heißt **irreduzibel**, wenn aus jeder Zerlegung $x = a\cdot b$ folgt, dass $a$ *oder* $b$ eine Einheit ist.
  *(„Man kann $x$ nur trivial zerlegen.")*
- $x$ heißt **Primelement**, wenn für alle $a,b\in R$ gilt:
  $$
  x\mid a\cdot b \;\Longrightarrow\; x\mid a\ \text{oder}\ x\mid b.
  $$
  *(„Wenn $x$ ein Produkt teilt, teilt es schon einen Faktor.")*

> **Achtung — der feine Unterschied.** Irreduzibel ist eine Aussage über *Zerlegungen von $x$ selbst*. Prim ist eine Aussage über *das Teilungsverhalten von $x$ in Produkten*. Diese beiden Begriffe sind im Allgemeinen **verschieden** und fallen nur in „guten" Ringen (wie $\mathbb{Z}$, $k[X]$) zusammen. Das ist eines der wichtigsten Lernziele dieses Kapitels.

<a id="primzahl"></a>
### Primzahl

**Definition 0.9 (Primzahl).**
Eine ganze Zahl $x\in\mathbb{Z}$ mit $x>1$ heißt **Primzahl**, wenn ihre einzigen positiven Teiler $1$ und $x$ sind.

<a id="nullstelle"></a>
### Nullstelle

**Definition 0.10 (Auswertung und Nullstelle).**
Für $P=a_nX^n+\dots+a_0\in k[X]$ und $\alpha\in k$ ist die **Auswertung** $P(\alpha) := a_n\alpha^n+\dots+a_0 \in k$. Ein $\alpha\in k$ heißt **Nullstelle** von $P$, falls $P(\alpha)=0$.

<a id="algebraisch-abgeschlossen"></a>
### Algebraisch abgeschlossen

**Definition 0.11 (algebraisch abgeschlossen).**
Ein Körper $k$ heißt **algebraisch abgeschlossen**, wenn jedes nicht-konstante Polynom $P\in k[X]$ eine Nullstelle in $k$ besitzt. (Äquivalent: jedes Polynom zerfällt über $k$ vollständig in Linearfaktoren.)

---

<a id="eigenschaften"></a>
## Eigenschaften

| Eigenschaft | Aussage | Kurzbegründung |
|---|---|---|
| **Gradadditivität** | $\deg(P\cdot Q)=\deg P+\deg Q$ | Leitkoeffizienten multiplizieren sich; $a_n b_m\neq 0$ in einem Körper. |
| **Gradsumme** | $\deg(P+Q)\le\max(\deg P,\deg Q)$ | Höchste Potenzen können sich auslöschen, aber nicht *erhöhen*. |
| **$k[X]$ ist Integritätsring** | $P,Q\neq 0\Rightarrow PQ\neq 0$ | folgt aus Gradadditivität: $\deg(PQ)=\deg P+\deg Q\ge 0$. |
| **Einheiten von $k[X]$** | $k[X]^\times = k\setminus\{0\}$ (Polynome vom Grad $0$) | $PQ=1\Rightarrow \deg P+\deg Q=0\Rightarrow\deg P=0$. |
| **Einheiten von $\mathbb{Z}$** | $\mathbb{Z}^\times=\{+1,-1\}$ | nur $\pm1$ haben ein ganzzahliges Inverses. |
| **Polynome vom Grad $1$** | stets irreduzibel (über jedem $k$) | Grad $1$ lässt sich nur als (Grad $0$)$\cdot$(Grad $1$) schreiben; Grad-$0$-Faktor ist Einheit. |
| **Funktionswerte additiv/multiplikativ** | $(P+Q)(\alpha)=P(\alpha)+Q(\alpha)$, $(PQ)(\alpha)=P(\alpha)Q(\alpha)$ | Auswertung ist ein Ringhomomorphismus $k[X]\to k$. |

**Wichtig:** Die Gradadditivität nutzt aus, dass $k$ ein **Körper** (zumindest nullteilerfrei) ist. Über einem Ring mit Nullteilern, z. B. $\mathbb{Z}/6\mathbb{Z}$, kann sie scheitern: $(2X)(3X)=6X^2=0$.

---

<a id="sätze"></a>
## Sätze

<a id="satz-012-gradformeln"></a>
### Satz 0.12 (Gradformeln)

**Aussage.** Für $P,Q\in k[X]$ gilt
(i) $\deg(P+Q)\le \max(\deg P,\deg Q)$, und
(ii) falls $P,Q\neq 0$, dann $P\cdot Q\neq 0$ und $\deg(P\cdot Q)=\deg P+\deg Q$.

**Voraussetzungen.** $k$ Körper (allgemeiner: $k$ nullteilerfrei).
**Bedeutung.** Macht $k[X]$ zu einem Integritätsring und liefert das „Größenmaß" für die Division mit Rest.
**Intuition.** Multiplizieren addiert Grade (wie Multiplizieren von Zehnerpotenzen Stellen addiert); Addieren kann den Grad nur halten oder senken.
**Konsequenzen.** Einheiten von $k[X]$ sind genau die Konstanten $\neq0$; Kürzungsregel ($PQ=PR,\,P\neq0\Rightarrow Q=R$).

<a id="satz-013-primelement-rightarrow-irreduzibel"></a>
### Satz 0.13 (Primelement $\Rightarrow$ irreduzibel)

**Aussage.** In einem nullteilerfreien kommutativen Ring $R$ ist **jedes Primelement irreduzibel**.
**Voraussetzungen.** $R$ Integritätsring.
**Bedeutung.** Eine Richtung der Begriffsgleichung „prim $=$ irreduzibel". Die *Umkehrung* gilt nur in speziellen Ringen.
**Intuition.** Wer ein Produkt nur teilen kann, indem er einen Faktor teilt, kann sich selbst nicht nichttrivial aufspalten.
**Konsequenzen.** Zusammen mit Satz 0.18 (Umkehrung in $\mathbb{Z},k[X]$) ergibt sich die volle Äquivalenz.

<a id="satz-014-division-mit-rest"></a>
### Satz 0.14 (Division mit Rest)

**Aussage.**
(a) *In $\mathbb{Z}$:* Zu $s,t\in\mathbb{Z}$, $t\neq0$, existieren **eindeutig** $a,r\in\mathbb{Z}$ mit
$$
s = a\,t + r,\qquad 0\le r < \lvert t\rvert.
$$
(b) *In $k[X]$ (Polynomdivision):* Zu $P,Q\in k[X]$, $Q\neq0$, existieren **eindeutig** $A,R\in k[X]$ mit
$$
P = A\,Q + R,\qquad \deg R < \deg Q.
$$

**Voraussetzungen.** Divisor $\neq0$.
**Bedeutung.** Der *einzige* nichttriviale Baustein, aus dem die gesamte Teilbarkeitstheorie folgt. Macht $\mathbb{Z}$ und $k[X]$ zu **euklidischen Ringen**.
**Intuition.** Man „zieht so oft wie möglich Vielfache des Divisors ab", bis der Rest echt kleiner ist.
**Konsequenzen.** Euklidischer Algorithmus, Bézout, eindeutige Faktorisierung.

<a id="satz-015-ggt-und-bézout"></a>
### Satz 0.15 (ggT und Bézout)

**Aussage.** Sei $R=\mathbb{Z}$ oder $R=k[X]$, und seien $p_1,p_2\in R\setminus\{0\}$. Dann existiert $d\in R\setminus\{0\}$ mit
$$
d\mid p_1,\quad d\mid p_2,\qquad\text{und}\qquad d = c_1 p_1 + c_2 p_2\ \text{für gewisse } c_1,c_2\in R.
$$
Jeder gemeinsame Teiler von $p_1,p_2$ teilt auch $d$. Man nennt $d$ (passend normiert) den **größten gemeinsamen Teiler** $\gcd(p_1,p_2)$.

**Voraussetzungen.** $R$ euklidisch; $p_1,p_2\neq0$.
**Bedeutung.** Der ggT ist nicht nur „der größte gemeinsame Teiler", sondern eine **Linearkombination** der beiden Elemente. Das ist der Schlüsselhebel für „irreduzibel $\Rightarrow$ prim".
**Intuition.** Der ggT ist „die feinste Größe, die in beiden steckt"; Bézout sagt, dass man ihn aus $p_1,p_2$ *zusammenbauen* kann.
**Konsequenzen.** Satz 0.18 (irreduzibel $\Rightarrow$ prim), Eindeutigkeit der Faktorisierung.

<a id="satz-016-017-eindeutige-faktorisierung"></a>
### Satz 0.16 / 0.17 (Eindeutige Faktorisierung)

**Aussage (in $\mathbb{Z}$, Fundamentalsatz der Arithmetik).** Jede ganze Zahl $z\neq0$ schreibt sich als
$$
z = a\cdot p_1\cdots p_n,\qquad a\in\{+1,-1\},\ n\ge0,\ p_i\ \text{Primzahlen},
$$
und diese Darstellung ist **eindeutig** bis auf die Reihenfolge der Faktoren.

**Aussage (in $k[X]$, Polynomfaktorzerlegung).** Jedes Polynom $P\in k[X]$, $P\neq0$, schreibt sich als
$$
P = a\cdot P_1\cdots P_n,\qquad a\in k\setminus\{0\},\ P_i\ \text{irreduzibel und normiert},
$$
und diese Darstellung ist **eindeutig** bis auf die Reihenfolge der Faktoren.

**Voraussetzungen.** $R=\mathbb{Z}$ bzw. $k[X]$.
**Bedeutung.** Die „Atomtheorie" der Zahlen/Polynome: Bausteine $+$ Eindeutigkeit.
**Intuition.** Jede Zahl/Polynom hat einen eindeutigen „genetischen Code" aus Primfaktoren.
**Konsequenzen.** Wohldefiniertheit von Vielfachheiten; in der LinA 2: eindeutige Faktorisierung von $\chi_f$ und $\mu_f$ in Linearfaktoren.

<a id="satz-018-irreduzibel-leftrightarrow-prim-in-mathbbz-und-kx"></a>
### Satz 0.18 (irreduzibel $\Leftrightarrow$ prim in $\mathbb{Z}$ und $k[X]$)

**Aussage.** In $R=\mathbb{Z}$ oder $R=k[X]$ gilt für $x\in R\setminus\{0\}$, keine Einheit:
$$
x\ \text{irreduzibel}\quad\Longleftrightarrow\quad x\ \text{Primelement}.
$$
Insbesondere: $x\in\mathbb{Z}$, $x>1$, ist Primzahl $\Leftrightarrow$ irreduzibel $\Leftrightarrow$ Primelement.

**Voraussetzungen.** $R$ euklidisch (genauer: Hauptidealring).
**Bedeutung.** Rechtfertigt nachträglich, dass man „prim" und „irreduzibel" in diesen Ringen synonym verwenden darf.
**Intuition.** In Ringen mit Bézout erzwingt Unzerlegbarkeit auch das gute Teilungsverhalten.

<a id="satz-019-nullstellen-und-linearfaktoren"></a>
### Satz 0.19 (Nullstellen und Linearfaktoren)

**Aussage.**
(i) Ist $\alpha\in k$ eine Nullstelle von $P\in k[X]$, so gilt $(X-\alpha)\mid P$.
(ii) Ein Polynom $P\neq0$ hat **höchstens $\deg P$ Nullstellen** in $k$.
(iii) $\alpha$ ist genau dann Nullstelle von $P$, wenn $(X-\alpha)$ in der Primfaktorzerlegung von $P$ vorkommt.

**Voraussetzungen.** $k$ Körper.
**Bedeutung.** Verbindet *Nullstellen* (Analysis-/Eigenwertseite) mit *Faktorisierung* (Algebra-Seite). Genau diese Brücke trägt später die Eigenwerttheorie.
**Intuition.** Eine Nullstelle „herausziehen" senkt den Grad um $1$; mehr als $\deg P$ Linearfaktoren passen nicht hinein.
**Konsequenzen.** „$\chi_f$ zerfällt in Linearfaktoren" $=$ „$f$ hat genug Eigenwerte"; Schranke für die Anzahl der Eigenwerte.

<a id="satz-020-fundamentalsatz-der-algebra"></a>
### Satz 0.20 (Fundamentalsatz der Algebra)

**Aussage.** $\mathbb{C}$ ist algebraisch abgeschlossen: jedes nicht-konstante $P\in\mathbb{C}[X]$ hat eine Nullstelle in $\mathbb{C}$; äquivalent zerfällt jedes $P\in\mathbb{C}[X]$ vollständig in Linearfaktoren.
**Bedeutung.** Über $\mathbb{C}$ *zerfällt $\chi_f$ immer* — deshalb ist über $\mathbb{C}$ jede Matrix trigonalisierbar und besitzt eine Jordan-Normalform. Dieser Satz ist der Grund, warum komplexe Zahlen in Kapitel 5 unverzichtbar werden.
**Beweisstil.** Wird in dieser Vorlesung **zitiert**, nicht bewiesen (der Beweis ist analytisch/topologisch und gehört in die Funktionentheorie).

---

<a id="beweise"></a>
## Beweise

> **Lesehinweis.** Klausurrelevant sind besonders die Beweise zu **Satz 0.13**, **0.14**, **0.15**, **0.18** und **0.19** — sie sind kurz, lehrreich und immer wieder als Beweisaufgabe geeignet. Der Eindeutigkeitsbeweis der Faktorisierung (0.16/0.17) ist konzeptionell wichtig.

<a id="beweis-von-satz-012-gradformeln-beweisstil-direkt"></a>
### Beweis von Satz 0.12 (Gradformeln) — *Beweisstil: direkt*

Seien $P=a_nX^n+\dots$, $a_n\neq0$, und $Q=b_mX^m+\dots$, $b_m\neq0$.

**(i)** In $P+Q$ können nur Potenzen $X^j$ mit $j\le\max(n,m)$ auftreten, also $\deg(P+Q)\le\max(n,m)$.

**(ii)** Der höchste Term von $P\cdot Q$ ist $a_nb_m\,X^{n+m}$. Da $k$ Körper und $a_n,b_m\neq0$, ist $a_nb_m\neq0$. Also ist $X^{n+m}$ tatsächlich der Leitterm, $PQ\neq0$ und $\deg(PQ)=n+m=\deg P+\deg Q$. $\qquad\blacksquare$

<a id="beweis-von-satz-013-prim-rightarrow-irreduzibel-beweisstil-direkt"></a>
### Beweis von Satz 0.13 (prim $\Rightarrow$ irreduzibel) — *Beweisstil: direkt*

Sei $x$ ein Primelement; angenommen $x = a\cdot b$. Dann gilt insbesondere $x\mid a\cdot b$ (mit Gleichheit). Da $x$ prim ist, folgt $x\mid a$ oder $x\mid b$. O. B. d. A. $x\mid a$, also $a = x\cdot a'$. Einsetzen:
$$
x = a\cdot b = x\cdot a'\cdot b \;\Longrightarrow\; 0 = x(a'b - 1).
$$
Da $R$ nullteilerfrei und $x\neq0$, folgt $a'b = 1$, d. h. **$b$ ist eine Einheit**. Also lässt sich $x$ nur trivial zerlegen — $x$ ist irreduzibel. $\qquad\blacksquare$

> **Merke den Trick:** „$0 = x(a'b-1)\Rightarrow a'b=1$" nutzt *Nullteilerfreiheit*. Ohne diese Voraussetzung bricht der Beweis (und die Aussage) zusammen.

<a id="beweis-von-satz-014-division-mit-rest-beweisstil-existenz-konstruktiv-eindeutigkeit-per-widerspruch"></a>
### Beweis von Satz 0.14 (Division mit Rest) — *Beweisstil: Existenz konstruktiv + Eindeutigkeit per Widerspruch*

**(b), Polynomfall — Existenz.** Sei $Q=b_mX^m+\dots$, $b_m\neq0$. Ist $\deg P<\deg Q$, nimm $A=0$, $R=P$. Andernfalls senken wir den Grad schrittweise: Hat $P=b X^{d}+\dots$ Grad $d\ge m$ (Leitkoeffizient $b$), so bilde
$$
P - \frac{b}{b_m}X^{d-m}\cdot Q.
$$
Der Leitterm $bX^d$ wird exakt weggehoben, der Grad sinkt um mindestens $1$. Wiederhole, bis der Grad $<m$ ist. Die Summe der abgezogenen Terme ist das gesuchte $A$, der Endrest ist $R$ mit $\deg R<\deg Q$.

**Eindeutigkeit.** Angenommen $P = AQ+R = A'Q+R'$ mit $\deg R,\deg R'<\deg Q$. Subtraktion:
$$
R-R' = (A'-A)\,Q.
$$
Wäre $A'-A\neq0$, dann $\deg(R-R') = \deg(A'-A)+\deg Q \ge \deg Q$. Andererseits $\deg(R-R')\le\max(\deg R,\deg R')<\deg Q$ — **Widerspruch**. Also $A=A'$ und damit $R=R'$.

**(a), ganzzahliger Fall — Existenz.** Für $s\ge0$ ziehe wiederholt $\lvert t\rvert$ ab, bis das Ergebnis in $\{0,\dots,\lvert t\rvert-1\}$ liegt; für $s<0$ addiere wiederholt $\lvert t\rvert$. **Eindeutigkeit:** wären $s=at+r=a't+r'$ mit $r\ne r'$ in $\{0,\dots,\lvert t\rvert-1\}$, so $\lvert r-r'\rvert=\lvert a-a'\rvert\,\lvert t\rvert\ge\lvert t\rvert$, aber $\lvert r-r'\rvert<\lvert t\rvert$ — Widerspruch. $\qquad\blacksquare$

<a id="beweis-von-satz-015-ggtbézout-beweisstil-euklidischer-algorithmus-konstruktiv-induktion"></a>
### Beweis von Satz 0.15 (ggT/Bézout) — *Beweisstil: Euklidischer Algorithmus (konstruktiv) + Induktion*

Setze $p_1,p_2$ als Start. Division mit Rest liefert eine **absteigende Restfolge**:
$$
\begin{aligned}
p_1 &= a_2 p_2 + p_3, & 0\le p_3 < p_2 \ (\text{bzw. } \deg p_3<\deg p_2),\\
p_2 &= a_3 p_3 + p_4, & \text{usw.},\\
&\ \ \vdots\\
p_{\ell-1} &= a_\ell p_\ell + 0.
\end{aligned}
$$
Da Reste echt schrumpfen (Betrag bzw. Grad), bricht die Folge nach **endlich vielen** Schritten ab; sei $d := p_\ell$ der letzte von $0$ verschiedene Rest.

**$d$ ist gemeinsamer Teiler.** Aus der letzten Zeile $d\mid p_{\ell-1}$; rückwärts eingesetzt folgt per Induktion $d\mid p_{j}$ für alle $j$, insbesondere $d\mid p_1$ und $d\mid p_2$.

**$d$ ist Linearkombination.** Aus jeder Zeile $p_{j+2}=p_j-a_{j+1}p_{j+1}$; rückwärts auflösen drückt $d$ als $d=c_1p_1+c_2p_2$ aus (erweiterter Euklid).

**Maximalität.** Ist $e$ ein gemeinsamer Teiler von $p_1,p_2$, so teilt $e$ jede Linearkombination $c_1p_1+c_2p_2 = d$, also $e\mid d$. $\qquad\blacksquare$

<a id="beweis-von-satz-018-irreduzibel-rightarrow-prim-beweisstil-direkt-mit-bézout"></a>
### Beweis von Satz 0.18 (irreduzibel $\Rightarrow$ prim) — *Beweisstil: direkt mit Bézout*

Die Richtung „prim $\Rightarrow$ irreduzibel" ist Satz 0.13. Sei nun $x$ **irreduzibel**; zu zeigen: prim. Angenommen $x\mid a\cdot b$, aber $x\nmid a$. Betrachte $d=\gcd(x,a)$. Da $d\mid x$ und $x$ irreduzibel, ist $d$ eine Einheit oder zu $x$ assoziiert. Wäre $d$ zu $x$ assoziiert, dann $x\mid a$ (Widerspruch). Also ist $d$ eine **Einheit**, d. h. $\gcd(x,a)=1$, und Bézout liefert $1 = c_1 x + c_2 a$. Multiplikation mit $b$:
$$
b = c_1 x b + c_2 a b.
$$
Beide Summanden sind durch $x$ teilbar ($x\mid x$ und $x\mid ab$), also $x\mid b$. Damit teilt $x$ einen der Faktoren — $x$ ist prim. $\qquad\blacksquare$

<a id="beweis-der-eindeutigkeit-der-faktorisierung-016017-beweisstil-induktion-primeigenschaft"></a>
### Beweis der Eindeutigkeit der Faktorisierung (0.16/0.17) — *Beweisstil: Induktion + Primeigenschaft*

(Skizze, hier für $k[X]$; $\mathbb{Z}$ analog.) **Existenz** per Induktion über $\deg P$: ist $P$ irreduzibel, fertig; sonst $P=BC$ mit $\deg B,\deg C<\deg P$, Induktionsvoraussetzung anwenden, Leitkoeffizienten zu $a$ zusammenfassen.

**Eindeutigkeit:** Angenommen
$$
a\,P_1\cdots P_n = a'\,P_1'\cdots P_m'
$$
mit irreduziblen normierten $P_i,P_j'$. Vergleich der Leitkoeffizienten gibt $a=a'$. Nun ist $P_1$ irreduzibel, also (Satz 0.18) **prim**, und teilt die rechte Seite, also einen Faktor $P_j'$. Da $P_j'$ irreduzibel und beide normiert sind, folgt $P_1=P_j'$. Kürzen (Integritätsring!) und Induktion über $n$ liefern $n=m$ und Übereinstimmung bis auf Reihenfolge. $\qquad\blacksquare$

> **Kernbotschaft.** Eindeutigkeit der Faktorisierung steht und fällt mit „irreduzibel $=$ prim". Wo dieser Schritt fehlt (Gegenbeispiel unten), gibt es mehrere Zerlegungen.

<a id="beweis-von-satz-019-nullstellen-beweisstil-direkt-via-division-mit-rest"></a>
### Beweis von Satz 0.19 (Nullstellen) — *Beweisstil: direkt via Division mit Rest*

**(i)** Polynomdivision durch $X-\alpha$ liefert $P = A\cdot(X-\alpha)+R$ mit $\deg R<\deg(X-\alpha)=1$, also $R=r\in k$ konstant. Einsetzen von $\alpha$:
$$
0 = P(\alpha) = A(\alpha)\cdot\underbrace{(\alpha-\alpha)}_{=0} + r = r.
$$
Also $r=0$ und $P=A\cdot(X-\alpha)$, d. h. $(X-\alpha)\mid P$.

**(ii)** Sei $P=a\,P_1\cdots P_n$ die Primfaktorzerlegung. Wegen $\deg P_i\ge1$ ist $\deg P=\sum\deg P_i\ge n$, also höchstens $\deg P$ verschiedene Primfaktoren. Jede Nullstelle $\alpha$ liefert nach (i) einen Linearfaktor $(X-\alpha)$, der nach Satz 0.19(iii) in der Zerlegung vorkommt; verschiedene Nullstellen geben verschiedene (nicht assoziierte) Linearfaktoren. Also gibt es höchstens $\deg P$ Nullstellen. $\qquad\blacksquare$

---

<a id="algorithmen"></a>
## Algorithmen

<a id="algorithmus-a-polynomdivision-division-mit-rest-in-kx"></a>
### Algorithmus A — Polynomdivision (Division mit Rest in $k[X]$)

- **Motivation.** Grundoperation für *alles* Weitere: Faktorabspaltung $(X-\alpha)$, ggT, Reduktion.
- **Idee.** Wiederholt den Leitterm des Divisors „passend skaliert" abziehen, bis der Rest echt kleineren Grad hat.
- **Voraussetzungen.** Divisor $Q\neq0$; Rechnen im Körper $k$ (Division durch den Leitkoeffizienten $b_m$ nötig).
- **Pseudocode.**
  ```
  Eingabe: P, Q in k[X], Q != 0
  R <- P;  A <- 0
  solange deg(R) >= deg(Q):
      t <- (Leitkoeff(R)/Leitkoeff(Q)) * X^(deg(R)-deg(Q))
      A <- A + t
      R <- R - t*Q
  Ausgabe: A (Quotient), R (Rest)   # P = A*Q + R, deg(R) < deg(Q)
  ```
- **Mathematische Beschreibung.** Liefert das eindeutige Paar $(A,R)$ aus Satz 0.14(b).
- **Laufzeit.** $O(\deg A\cdot\deg Q)$ Körperoperationen, im Worst Case $O(\deg P\cdot\deg Q)$.
- **Speicherbedarf.** $O(\deg P)$ (Koeffizienten von $R$ und $A$).
- **Korrektheitsidee.** Jeder Durchlauf senkt $\deg R$ um $\ge1$ und erhält die Invariante $P=A Q+R$; Abbruch bei $\deg R<\deg Q$.
- **Anwendungen.** Faktorabspaltung bei Nullstellen; Auswertung des Euklidischen Algorithmus; Reduktion modulo eines Polynoms (Kapitel 5: $\mathbb{R}[X]/(X^2+1)$).
- **Typische Fehler.** Vergessen, durch den Leitkoeffizienten zu *dividieren* (nur korrekt, wenn $Q$ normiert); Vorzeichenfehler bei $R\leftarrow R-tQ$.

<a id="algorithmus-b-erweiterter-euklidischer-algorithmus"></a>
### Algorithmus B — (Erweiterter) Euklidischer Algorithmus

- **Motivation.** Liefert $\gcd(p_1,p_2)$ **und** die Bézout-Koeffizienten $c_1,c_2$ aus Satz 0.15.
- **Idee.** Wiederholte Division mit Rest; die Reste schrumpfen, der letzte $\neq0$ Rest ist der ggT. „Rückwärts einsetzen" liefert die Koeffizienten.
- **Voraussetzungen.** $R=\mathbb{Z}$ oder $k[X]$; $p_1,p_2\neq0$.
- **Pseudocode (ggT).**
  ```
  Eingabe: p1, p2 (!= 0)
  (a, b) <- (p1, p2)
  solange b != 0:
      r <- a mod b        # Division mit Rest
      (a, b) <- (b, r)
  Ausgabe: a              # = gcd(p1, p2)  (in k[X]: normieren)
  ```
- **Mathematische Beschreibung.** Berechnet das $d$ aus Satz 0.15; die erweiterte Variante propagiert zusätzlich $(c_1,c_2)$ mit $d=c_1p_1+c_2p_2$.
- **Laufzeit.** In $k[X]$: $O((\deg p_1)\cdot(\deg p_2))$ Körperoperationen (Gradsumme schrumpft pro Schritt). In $\mathbb{Z}$: $O(\log\min(p_1,p_2))$ Divisionsschritte.
- **Speicherbedarf.** $O(\deg p_1+\deg p_2)$ bzw. $O(1)$ Register im Integer-Fall.
- **Korrektheitsidee.** Invariante: $\gcd(a,b)=\gcd(p_1,p_2)$ bleibt bei jedem Schritt erhalten (denn $\gcd(a,b)=\gcd(b,\,a\bmod b)$); Terminierung durch strikt fallendes Größenmaß.
- **Anwendungen.** Nachweis „irreduzibel $\Rightarrow$ prim"; Inverse in $\mathbb{Z}/n\mathbb{Z}$ bzw. $k[X]/(P)$; teilerfremde Zerlegungen (später Haupträume, Partition der Eins über $\gcd(P_1,\dots,P_r)=1$).
- **Typische Fehler.** ggT in $k[X]$ nicht **normieren** (ggT ist nur bis auf Einheit eindeutig); Bézout-Koeffizienten falsch zurückpropagieren.

> **Vergleich der beiden Algorithmen.** B *ruft* A in jeder Iteration auf. A ist eine *einzelne* Division; B ist eine *Folge* von Divisionen mit absteigendem Größenmaß. Beide terminieren aus demselben Grund: das Größenmaß (Grad bzw. Betrag) fällt strikt.

---

<a id="beispiele"></a>
## Beispiele

**Beispiel 1 (leicht — Polynomdivision).** $P=X^3+3X^2$, $Q=X^2+X+2$ über $\mathbb{Q}$:
$$
X^3+3X^2 = (X+2)(X^2+X+2) + (-4X-4).
$$
Probe: $(X+2)(X^2+X+2)=X^3+3X^2+4X+4$; plus $(-4X-4)$ ergibt $X^3+3X^2$. ✓ Rest hat Grad $1<2$. ✓

**Beispiel 2 (leicht — Linearfaktor abspalten).** $P=X^2-5X+6$ hat Nullstelle $\alpha=2$ ($P(2)=4-10+6=0$). Division durch $X-2$:
$$
X^2-5X+6=(X-2)(X-3).
$$

**Beispiel 3 (mittel — ggT in $k[X]$).** $\gcd(X^3-1,\;X^2-1)$ über $\mathbb{Q}$:
$$
X^3-1=(X)(X^2-1)+(X-1),\qquad X^2-1=(X+1)(X-1)+0.
$$
Letzter Rest $\neq0$ ist $X-1$, also $\gcd=X-1$ (bereits normiert).

**Beispiel 4 (mittel — vollständige Faktorisierung).** Über $\mathbb{Q}$:
$$
X^5+X^4-X-1=(X+1)(X^4-1)=(X+1)(X^2-1)(X^2+1)=(X+1)^2(X-1)(X^2+1).
$$
Die rationalen/reellen Nullstellen sind $1$ und $-1$; $X^2+1$ ist über $\mathbb{R}$ irreduzibel, über $\mathbb{C}$ aber $=(X-i)(X+i)$.

**Beispiel 5 (schwer — Faktorisierung hängt vom Körper ab).** $P=X^2-2$:
- über $\mathbb{Q}$: irreduzibel (keine rationale Nullstelle, $\sqrt2\notin\mathbb{Q}$);
- über $\mathbb{R}$: $=(X-\sqrt2)(X+\sqrt2)$, *reduzibel*;
- über $\mathbb{C}$: ebenfalls reduzibel.

Dieselbe „Substanz", drei verschiedene Faktorisierungen — die Faktorisierung ist eine Eigenschaft des **Paares** $(P,k)$, nicht von $P$ allein.

**Beispiel 6 (schwer — erweiterter Euklid / Bézout).** In $\mathbb{Z}$: $\gcd(12,8)$.
$$
12=1\cdot8+4,\quad 8=2\cdot4+0\ \Rightarrow\ \gcd=4,\qquad 4=12-1\cdot8=1\cdot12+(-1)\cdot8.
$$
Bézout: $c_1=1,\,c_2=-1$.

---

<a id="gegenbeispiele"></a>
## Gegenbeispiele

**Gegenbeispiel A (irreduzibel $\neq$ prim — Eindeutigkeit scheitert).**
Im Ring $R=\mathbb{Z}[\sqrt5]=\{a+b\sqrt5\mid a,b\in\mathbb{Z}\}\subseteq\mathbb{R}$ ist das Element $2$ **irreduzibel, aber kein Primelement**.

- *Irreduzibel:* Mit der **Norm** $N(a+b\sqrt5)=a^2-5b^2$ gilt $N(2)=4$. Eine echte Zerlegung $2=\alpha\beta$ bräuchte $N(\alpha)=\pm2$, also $a^2-5b^2=\pm2$. Modulo $5$: $a^2\in\{0,1,4\}$, aber $\pm2\notin\{0,1,4\}$ — unmöglich. Also ist jede Zerlegung trivial.
- *Nicht prim:* $2\mid(1+\sqrt5)(1-\sqrt5)=1-5=-4$, aber $2\nmid(1+\sqrt5)$ und $2\nmid(1-\sqrt5)$ (sonst wäre $\tfrac{1}{2}\in\mathbb{Z}$).

Folge: In $\mathbb{Z}[\sqrt5]$ kann die Primfaktorzerlegung **mehrdeutig** sein. Der Grund: $\mathbb{Z}[\sqrt5]$ ist *kein* euklidischer Ring, hat *kein* Bézout — der entscheidende Schritt im Beweis von Satz 0.18 fehlt.

> *(Das kanonische Lehrbuchbeispiel ist $\mathbb{Z}[\sqrt{-5}]$ mit $2\cdot3=(1+\sqrt{-5})(1-\sqrt{-5})$; in $\mathbb{Z}[\sqrt5]$ funktioniert es genauso. Beachte: $\mathbb{Z}[\sqrt5]$ ist nicht ganzabgeschlossen.)*

**Gegenbeispiel B (Gradadditivität scheitert ohne Nullteilerfreiheit).**
In $(\mathbb{Z}/6\mathbb{Z})[X]$: $(2X+1)(3X+1)=6X^2+5X+1=5X+1$. Grad $1$, nicht $2$ — weil $2\cdot3=0$ in $\mathbb{Z}/6\mathbb{Z}$.

**Gegenbeispiel C (verschiedene Polynome, gleiche Funktion).**
Über $k=\mathbb{F}_2$ liefern $X^2$ und $X$ *dieselbe* Funktion ($0\mapsto0,\,1\mapsto1$), sind aber verschiedene Polynome. Allgemein über $\mathbb{F}_p$: $X^p-X$ ist das Nullpolynom *als Funktion*, aber nicht *als Polynom*. Deshalb sind Polynome **formal** zu definieren (Definition 0.1).

**Gegenbeispiel D (mehr als $\deg P$ Nullstellen über Nicht-Körpern).**
In $\mathbb{Z}/8\mathbb{Z}$ hat $X^2-1$ die vier Nullstellen $1,3,5,7$ — Satz 0.19(ii) braucht zwingend, dass $k$ ein **Körper** ist (sonst kein Integritätsring).

---

<a id="typische-klausuraufgaben"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Woran erkennbar | Strategie |
|---|---|---|
| **Polynomdivision / Rest bestimmen** | „Berechne $P$ geteilt durch $Q$ mit Rest." | Algorithmus A schematisch; Grad des Rests kontrollieren. |
| **ggT zweier Polynome** | „Bestimmen Sie $\gcd(P,Q)$." | Euklid (Algorithmus B); am Ende **normieren**. |
| **Bézout-Darstellung** | „Schreiben Sie $\gcd$ als Linearkombination." | erweiterter Euklid, Reste rückwärts einsetzen. |
| **Vollständig faktorisieren** | „Zerlegen Sie $P$ über $\mathbb{Q}/\mathbb{R}/\mathbb{C}$." | rationale Nullstellen raten (Teiler von $a_0/a_n$), Linearfaktoren abspalten, Restgrad senken; **Körper beachten**. |
| **Irreduzibilität entscheiden** | „Ist $P$ über $k$ irreduzibel?" | Grad $\le3$: irreduzibel $\Leftrightarrow$ keine Nullstelle in $k$; höhere Grade: Eisenstein/Reduktion mod $p$ (falls behandelt). |
| **irreduzibel vs. prim** | „Zeigen Sie: $x$ ist irreduzibel/prim / geben Sie ein Gegenbeispiel." | Definitionen sauber anwenden; bei „nicht prim" Normargument (Gegenbeispiel A). |
| **Anzahl der Nullstellen** | „Wie viele Nullstellen kann $P$ höchstens haben?" | Satz 0.19(ii): $\le\deg P$ (Körper!). |

---

<a id="typische-fehler"></a>
## Typische Fehler

| Fehler | Warum falsch | Richtig |
|---|---|---|
| „$\deg(P+Q)=\max(\deg P,\deg Q)$" als Gleichheit | Leitterme können sich auslöschen: $(X^2+1)+(-X^2)=1$. | Nur **$\le$**; Gleichheit nur bei verschiedenen Graden. |
| ggT in $k[X]$ nicht normiert | ggT ist nur bis auf Einheit (Konstante $\neq0$) eindeutig. | Auf **normiertes** Polynom skalieren. |
| „irreduzibel $=$ prim immer" | Gilt nur in euklidischen Ringen / HIR; siehe $\mathbb{Z}[\sqrt5]$. | Äquivalenz nur in $\mathbb{Z},k[X]$ (Satz 0.18). |
| Polynom $=$ Funktion gesetzt | Über endlichen Körpern verschiedene Polynome $=$ gleiche Funktion. | Polynome **formal** (Koeffizientenfolge). |
| „$1$ ist Primzahl" | $1$ ist Einheit; Primzahlen sind $>1$. | $1$ ist weder prim noch irreduzibel. |
| Irreduzibilität ohne Körperangabe | $X^2-2$ irreduzibel über $\mathbb{Q}$, reduzibel über $\mathbb{R}$. | Immer **„über welchem $k$"** angeben. |
| Bei der Division durch nicht-normiertes $Q$ den Leitkoeffizienten ignorieren | $t=\frac{\text{LK}(R)}{\text{LK}(Q)}X^{\dots}$ braucht den Quotienten. | Stets durch $\text{LK}(Q)$ teilen. |

---

<a id="verbindungen"></a>
## Verbindungen

- **→ Kapitel 2 (Eigenwerte):** Das charakteristische Polynom $\chi_f$ lebt in $k[X]$. „$\chi_f$ zerfällt in Linearfaktoren" (Satz 0.19/0.20) entscheidet über Diagonalisier- und Trigonalisierbarkeit. Die Schranke „$\le\deg P$ Nullstellen" wird zur Schranke für die Anzahl der Eigenwerte.
- **→ Kapitel 3 (Minimalpolynom):** $\mu_f\mid\chi_f$ und die Teilbarkeitslehre dieses Kapitels sind die Grundlage; $\mu_f=\prod(X-\lambda_j)^{m_j}$ ist eine Faktorisierungsaussage.
- **→ Kapitel 4 (Jordan):** Die Zerlegung $V=\bigoplus\mathrm{Haupt}(f,\lambda_j)$ beruht auf $\gcd(P_1,\dots,P_r)=1$ und der Bézout-Partition der Eins (direkte Verallgemeinerung von Satz 0.15).
- **→ Kapitel 5 ($\mathbb{C}$):** Der Fundamentalsatz (Satz 0.20) erzwingt das Arbeiten über $\mathbb{C}$; $\mathbb{C}=\mathbb{R}[X]/(X^2+1)$ ist ein **Quotientenring** — die Faktorisierung $X^2+1$ irreduzibel über $\mathbb{R}$ ist genau, was diesen Körper liefert.
- **← Lineare Algebra 1:** Körperaxiome, Vektorraumstruktur von $k[X]$.

**Definitionen, die später ständig gebraucht werden:** Grad, normiert, irreduzibel, ggT, Nullstelle, „zerfällt in Linearfaktoren", algebraisch abgeschlossen.

---

<a id="zusammenfassung"></a>
## Zusammenfassung

| Kernaussage | Symbolisch |
|---|---|
| $k[X]$ ist Integritätsring, Einheiten $=$ Konstanten $\neq0$. | $k[X]^\times=k\setminus\{0\}$ |
| Grad multipliziert sich, addiert höchstens. | $\deg(PQ)=\deg P+\deg Q$, $\deg(P+Q)\le\max$ |
| Division mit Rest gilt in $\mathbb{Z}$ und $k[X]$. | $P=AQ+R$, $\deg R<\deg Q$ |
| ggT existiert und ist Linearkombination (Bézout). | $d=c_1p_1+c_2p_2$ |
| In $\mathbb{Z},k[X]$: irreduzibel $=$ prim. | (Satz 0.18) |
| Eindeutige Primfaktorzerlegung. | $P=a\,P_1\cdots P_n$, eindeutig |
| Nullstelle $\Leftrightarrow$ Linearfaktor; $\le\deg P$ Nullstellen. | $(X-\alpha)\mid P$ |
| Über $\mathbb{C}$ zerfällt **jedes** Polynom. | (Fundamentalsatz) |

**Die eine Idee des Kapitels:** *Division mit Rest* $\Rightarrow$ *Bézout* $\Rightarrow$ *irreduzibel $=$ prim* $\Rightarrow$ *eindeutige Faktorisierung*. Diese Kette trägt die gesamte Normalformentheorie der LinA 2.



---

<a id="kapitel-1-quotientenvektorräume"></a>
# Kapitel 1 — Quotientenvektorräume

> **Stellung im Kurs.** Der Quotientenraum $V/U$ ist ein **Werkzeugkapitel**. Es liefert keine
> spektakulären Endresultate, sondern die *Beweistechnik*, mit der später die schwierigen Sätze
> fallen: Trigonalisierbarkeit (Kap. 2), Hauptraumzerlegung und Jordan-Normalform (Kap. 4) werden
> per **Induktion über $V/U$** bewiesen. Außerdem ist $\mathbb{C}=\mathbb{R}[X]/(X^2+1)$ (Kap. 5) ein
> Quotient. Wer $V/U$ verstanden hat, versteht diese Beweise.

---

<a id="motivation-1"></a>
## Motivation

Oft will man einen „störenden" Unterraum **loswerden**, ohne den ganzen Vektorraum zu zerstören. Drei konkrete Bedürfnisse:

1. **Induktion über die Dimension.** Viele Sätze der LinA 2 haben die Form: „Eigenschaft gilt für $\dim V$, wenn sie für kleinere Dimension gilt." Um die Dimension zu *senken*, braucht man einen Mechanismus, der aus $V$ einen kleineren Raum macht — und zwar so, dass eine gegebene lineare Abbildung $f$ „mitwandert". Genau das leistet $V/U$ mit $\dim(V/U)=\dim V-\dim U$.

2. **Homomorphiesatz / Faktorisierung.** Eine lineare Abbildung $f\colon V\to W$ mit Kern $U$ ist auf $U$ „blind" (sie schickt ganz $U$ auf $0$). Man möchte $f$ so umschreiben, dass diese Redundanz verschwindet — als injektive Abbildung auf $V/U$. Das ist der **Homomorphiesatz** und der Ursprung des Begriffs „Quotient".

3. **Konstruktion neuer Strukturen.** Quotienten erzeugen neue Objekte aus alten: $\mathbb{Z}/n\mathbb{Z}$ (modulares Rechnen), $\mathbb{R}[X]/(X^2+1)=\mathbb{C}$ (Kapitel 5), Funktionenräume modulo „Nullmengen" usw.

**Mathematische Wurzel.** Die Idee ist dieselbe wie beim **Rechnen modulo $n$**: In $\mathbb{Z}/5\mathbb{Z}$ behandelt man $3$ und $8$ als „gleich", weil sie sich um ein Vielfaches von $5$ unterscheiden. Beim Quotientenvektorraum behandelt man zwei Vektoren als „gleich", wenn sie sich um ein Element von $U$ unterscheiden. Quotientenbildung ist also **„kontrolliertes Gleichsetzen"** entlang eines Unterraums.

---

<a id="intuition-1"></a>
## Intuition

**Das Bild: $U$ zu einem Punkt zusammendrücken.**
Stell dir $V=\mathbb{R}^2$ vor und $U$ eine Gerade durch den Ursprung. Im Quotienten $V/U$ wird die *gesamte Gerade $U$* zum Nullpunkt. Was bleibt übrig? Alle zu $U$ **parallelen Geraden** — und jede solche parallele Gerade ist *ein einzelner Punkt* von $V/U$. Da man parallele Geraden in $\mathbb{R}^2$ durch *eine* Zahl (den senkrechten Abstand mit Vorzeichen) durchnummerieren kann, ist $\mathbb{R}^2/U\cong\mathbb{R}$.

```
   V = ℝ²                          V/U  (jede Parallele = 1 Punkt)
   │ ╱ ╱ ╱  U und Parallelen        •  ← v3 + U
   │╱ ╱ ╱                           •  ← v2 + U
  ─┼─────  U (wird zu 0)            (0) ← U selbst
   │╱ ╱ ╱                           •  ← v1 + U
```

**Die Elemente von $V/U$ sind affine Teilräume.** Ein Element von $V/U$ ist eine **Nebenklasse**
$$
v+U=\{v+u\mid u\in U\},
$$
also eine zu $U$ parallele „verschobene Kopie". Zwei Vektoren $v,v'$ liefern *dieselbe* Nebenklasse genau dann, wenn $v-v'\in U$.

**Warum das ein Vektorraum ist.** Man addiert Nebenklassen, indem man Repräsentanten addiert: $(v+U)+(w+U):=(v+w)+U$. Der einzige Haken — und das ist die ganze Subtilität — ist die **Wohldefiniertheit**: Das Ergebnis darf nicht davon abhängen, *welchen* Repräsentanten man wählt. Dass es nicht abhängt, liegt daran, dass $U$ ein *Unterraum* ist (abgeschlossen unter $+$ und $\cdot$). Bei einer beliebigen Teilmenge ginge es schief.

**Analogie zum modularen Rechnen.**

| modulo $n$ in $\mathbb{Z}$ | modulo $U$ in $V$ |
|---|---|
| $a\equiv b \Leftrightarrow n\mid(a-b)$ | $v\sim v'\Leftrightarrow v-v'\in U$ |
| Restklasse $\bar a=a+n\mathbb{Z}$ | Nebenklasse $v+U$ |
| $\mathbb{Z}/n\mathbb{Z}$ | $V/U$ |
| „$+,\cdot$ wohldefiniert, weil $n\mathbb{Z}$ Ideal" | „$+,\cdot$ wohldefiniert, weil $U$ Unterraum" |

---

<a id="formale-definitionen-1"></a>
## Formale Definitionen

<a id="äquivalenzrelation-grundlage"></a>
### Äquivalenzrelation (Grundlage)

**Definition 1.1 (Äquivalenzrelation).**
Eine **Äquivalenzrelation** $\sim$ auf einer Menge $M$ ist eine Teilmenge von $M\times M$ (man schreibt $x\sim y$ statt $(x,y)\in\,\sim$), die

- **reflexiv:** $x\sim x$ für alle $x$,
- **symmetrisch:** $x\sim y\Rightarrow y\sim x$,
- **transitiv:** $x\sim y$ und $y\sim z\Rightarrow x\sim z$

erfüllt.

**Definition 1.2 (Äquivalenzklasse, Partition).**
Die **Äquivalenzklasse** von $x$ ist $[x]=\{y\in M\mid y\sim x\}$. Die Klassen bilden eine **Partition** von $M$: $M$ ist die disjunkte Vereinigung paarweise verschiedener Klassen. (Zwei Klassen sind entweder identisch oder disjunkt.)

<a id="der-quotientenvektorraum"></a>
### Der Quotientenvektorraum

**Definition 1.3 (Quotientenrelation und $V/U$).**
Sei $V$ ein $k$-Vektorraum und $U\subseteq V$ ein **Unterraum**. Auf $V$ definiere
$$
v\sim v' \quad:\Longleftrightarrow\quad v-v'\in U.
$$
Dies ist eine Äquivalenzrelation (siehe Eigenschaften). Die Äquivalenzklasse von $v$ ist die **Nebenklasse**
$$
v+U=\{v+u\mid u\in U\}.
$$
Die Menge aller Nebenklassen heißt **Quotientenraum** $V/U:=\{\,v+U\mid v\in V\,\}$.

**Definition 1.4 (Vektorraumstruktur auf $V/U$).**
Auf $V/U$ definiere
$$
(v+U)+(w+U):=(v+w)+U,\qquad a\cdot(v+U):=(a\,v)+U\quad(a\in k).
$$
Mit diesen Operationen ist $V/U$ ein $k$-Vektorraum (genannt **Quotientenvektorraum**), mit **Nullvektor** $0+U=U$.

<a id="die-kanonische-projektion"></a>
### Die kanonische Projektion

**Definition 1.5 (Projektion).**
Die Abbildung
$$
p_U\colon V\to V/U,\qquad p_U(v)=v+U,
$$
heißt **kanonische Projektion** (oder Quotientenabbildung).

---

<a id="eigenschaften-1"></a>
## Eigenschaften

| Eigenschaft | Aussage | Kurzbegründung |
|---|---|---|
| **$\sim$ ist Äquivalenzrelation** | reflexiv/symmetrisch/transitiv | $v-v=0\in U$; $v-v'\in U\Rightarrow v'-v=-(v-v')\in U$; $(v-w)+(w-z)\in U$. |
| **Gleichheit von Nebenklassen** | $v+U=w+U\Leftrightarrow v-w\in U$ | direkt aus der Definition von $\sim$. |
| **$+,\cdot$ wohldefiniert** | unabhängig vom Repräsentanten | nutzt, dass $U$ Unterraum ist (Beweis unten). |
| **$p_U$ ist linear** | $p_U(av+bw)=a\,p_U(v)+b\,p_U(w)$ | folgt aus Definition 1.4. |
| **$p_U$ ist surjektiv** | jedes $v+U$ ist Bild von $v$ | per Definition. |
| **$\ker(p_U)=U$** | $v+U=0+U\Leftrightarrow v\in U$ | Nullvektor von $V/U$ ist $U$. |
| **Dimension** | $\dim(V/U)=\dim V-\dim U$ (endlichdim.) | Basisergänzung (Satz 1.9). |

---

<a id="sätze-1"></a>
## Sätze

<a id="satz-16-wohldefiniertheit-und-vektorraumstruktur"></a>
### Satz 1.6 (Wohldefiniertheit und Vektorraumstruktur)

**Aussage.** Die Operationen aus Definition 1.4 sind **wohldefiniert**, und $(V/U,+,\cdot)$ ist ein $k$-Vektorraum.
**Voraussetzungen.** $U\subseteq V$ **Unterraum** (nicht bloß Teilmenge!).
**Bedeutung.** Erst die Wohldefiniertheit macht $V/U$ überhaupt zu einem rechenbaren Objekt.
**Intuition.** Verschiebt man Repräsentanten um Elemente von $U$, so ändert sich das Ergebnis nur um Elemente von $U$ — also dieselbe Nebenklasse.
**Konsequenzen.** $p_U$ ist eine wohldefinierte lineare Abbildung.

<a id="satz-17-projektion-linear-surjektiv-kern-u"></a>
### Satz 1.7 (Projektion: linear, surjektiv, Kern $U$)

**Aussage.** $p_U\colon V\to V/U$ ist linear und surjektiv mit $\ker(p_U)=U$.
**Bedeutung.** $U$ ist *der* Kern einer linearen Abbildung — das ist die Quelle des Homomorphiesatzes.
**Intuition.** $p_U$ „vergisst" genau die $U$-Richtung.
**Konsequenzen.** Jeder Unterraum ist Kern einer linearen Abbildung; Brücke zur universellen Eigenschaft.

<a id="satz-18-universelle-eigenschaft-homomorphiesatz"></a>
### Satz 1.8 (Universelle Eigenschaft / Homomorphiesatz)

**Aussage.** Seien $V,W$ Vektorräume, $U\subseteq V$ ein Unterraum und $f\colon V\to W$ linear mit $U\subseteq\ker(f)$. Dann gibt es **genau eine** lineare Abbildung
$$
g\colon V/U\to W,\qquad g(v+U)=f(v),\qquad\text{sodass}\quad f=g\circ p_U.
$$
Das Diagramm
$$
\begin{array}{ccc}
V & \xrightarrow{\ f\ } & W\\[-2pt]
{\scriptstyle p_U}\big\downarrow & \nearrow{\scriptstyle g} & \\[-2pt]
V/U & &
\end{array}
\qquad\text{„kommutiert".}
$$
**Voraussetzungen.** $U\subseteq\ker(f)$ — das ist die *entscheidende* Bedingung.
**Bedeutung.** Jede Abbildung, die auf $U$ verschwindet, „faktorisiert" eindeutig über $V/U$. Das ist das universelle Werkzeug, um Abbildungen *auf Quotienten* zu definieren.
**Intuition.** Wenn $f$ alle $U$-Unterschiede ignoriert, „hängt $f$ nur von der Nebenklasse ab" — also ist $f$ in Wahrheit eine Abbildung auf $V/U$.
**Konsequenzen.** Homomorphiesatz $V/\ker(f)\cong\mathrm{Bild}(f)$; in Kap. 2/4 die induzierte Abbildung $\bar f\colon V/U\to V/U$ bei $f$-invariantem $U$.

<a id="satz-19-dimension-und-basis-von-vu"></a>
### Satz 1.9 (Dimension und Basis von $V/U$)

**Aussage.** Sei $\dim V<\infty$, $\{b_1,\dots,b_m\}$ eine Basis von $U$, ergänzt zu einer Basis $\{b_1,\dots,b_m,v_1,\dots,v_n\}$ von $V$. Dann ist
$$
\{\,v_1+U,\dots,v_n+U\,\}\ \text{eine Basis von }V/U,
\qquad\text{also}\qquad \dim(V/U)=n=\dim V-\dim U.
$$
**Voraussetzungen.** $\dim V<\infty$.
**Bedeutung.** Quotientenbildung **senkt die Dimension** kontrolliert — die Grundlage aller Induktionsbeweise.
**Intuition.** Die $U$-Richtungen $b_i$ werden zu $0$; nur die „Ergänzungsrichtungen" $v_j$ überleben.

---

<a id="beweise-1"></a>
## Beweise

> **Klausurrelevant:** Satz 1.6 (Wohldefiniertheit), 1.7 (Projektion), 1.8 (universelle Eigenschaft).
> Diese drei sind kurze, beliebte Beweisaufgaben.

<a id="beweis-von-satz-16-wohldefiniertheit-beweisstil-direkt-repräsentantenunabhängigkeit"></a>
### Beweis von Satz 1.6 (Wohldefiniertheit) — *Beweisstil: direkt, Repräsentantenunabhängigkeit*

Zu zeigen: Wählt man andere Repräsentanten, kommt dieselbe Nebenklasse heraus.

**Addition.** Seien $v+U=v'+U$ und $w+U=w'+U$, also $v-v'\in U$ und $w-w'\in U$. Dann
$$
(v+w)-(v'+w')=\underbrace{(v-v')}_{\in U}+\underbrace{(w-w')}_{\in U}\in U,
$$
weil $U$ unter Addition abgeschlossen ist. Also $(v+w)+U=(v'+w')+U$. ✓

**Skalarmultiplikation.** Sei $v+U=v'+U$, also $v-v'\in U$. Für $a\in k$:
$$
a v-a v'=a\,(v-v')\in U,
$$
weil $U$ unter Skalarmultiplikation abgeschlossen ist. Also $(av)+U=(av')+U$. ✓

Die Vektorraumaxiome (Assoziativität, Distributivität usw.) „erben" sich repräsentantenweise von $V$; der Nullvektor ist $0+U=U$. $\qquad\blacksquare$

> **Genau hier** wird benutzt, dass $U$ ein **Unterraum** ist. Für eine beliebige Teilmenge wäre weder $(v-v')+(w-w')\in U$ noch $a(v-v')\in U$ garantiert — die Operationen wären nicht wohldefiniert.

<a id="beweis-von-satz-17-projektion-beweisstil-direkt"></a>
### Beweis von Satz 1.7 (Projektion) — *Beweisstil: direkt*

**Linearität.** Für $v,w\in V$, $a\in k$:
$$
p_U(av+w)=(av+w)+U=a(v+U)+(w+U)=a\,p_U(v)+p_U(w).
$$
**Surjektivität.** Jedes Element von $V/U$ hat die Form $v+U=p_U(v)$.
**Kern.** Der Nullvektor von $V/U$ ist $U=0+U$. Also
$$
v\in\ker(p_U)\ \Leftrightarrow\ v+U=0+U\ \Leftrightarrow\ v-0\in U\ \Leftrightarrow\ v\in U.\qquad\blacksquare
$$

<a id="beweis-von-satz-18-universelle-eigenschaft-beweisstil-existenz-konstruktion-wohldefiniertheit-und-eindeutigkeit"></a>
### Beweis von Satz 1.8 (universelle Eigenschaft) — *Beweisstil: Existenz (Konstruktion + Wohldefiniertheit) und Eindeutigkeit*

**Wohldefiniertheit von $g$.** Definiere $g(v+U):=f(v)$. Ist $v+U=v'+U$, also $v-v'\in U\subseteq\ker f$, dann
$$
f(v)-f(v')=f(v-v')=0\ \Rightarrow\ f(v)=f(v').
$$
Der Wert hängt also nur von der Nebenklasse ab — $g$ ist wohldefiniert.

**Linearität von $g$.**
$$
g\big(a(v+U)+(w+U)\big)=g\big((av+w)+U\big)=f(av+w)=a f(v)+f(w)=a\,g(v+U)+g(w+U).
$$

**Faktorisierung.** $(g\circ p_U)(v)=g(v+U)=f(v)$, also $f=g\circ p_U$.

**Eindeutigkeit.** Erfüllt $g'$ ebenfalls $f=g'\circ p_U$, so $g'(v+U)=g'(p_U(v))=f(v)=g(v+U)$ für alle $v$, also $g'=g$. $\qquad\blacksquare$

<a id="beweis-von-satz-19-dimension-beweisstil-direkt-erzeugendensystem-lineare-unabhängigkeit"></a>
### Beweis von Satz 1.9 (Dimension) — *Beweisstil: direkt (Erzeugendensystem + lineare Unabhängigkeit)*

**Erzeugend.** Für $v\in V$ schreibe $v=\sum_i\alpha_i b_i+\sum_j\beta_j v_j$. Anwenden von $p_U$ und $p_U(b_i)=b_i+U=U=0$:
$$
v+U=\sum_j\beta_j\,(v_j+U),
$$
also erzeugen die $v_j+U$ ganz $V/U$.

**Linear unabhängig.** Sei $\sum_j\beta_j(v_j+U)=0+U$, d. h. $\big(\sum_j\beta_j v_j\big)\in U$. Da $\{b_i\}$ Basis von $U$, gibt es $\alpha_i$ mit $\sum_j\beta_j v_j=\sum_i\alpha_i b_i$, also
$$
\sum_j\beta_j v_j-\sum_i\alpha_i b_i=0.
$$
Da $\{b_1,\dots,b_m,v_1,\dots,v_n\}$ Basis von $V$ (linear unabhängig), folgt alle $\beta_j=0$ (und $\alpha_i=0$). $\qquad\blacksquare$

---

<a id="algorithmen-1"></a>
## Algorithmen

<a id="verfahren-rechnen-in-vu-und-basis-von-vu-bestimmen"></a>
### Verfahren — Rechnen in $V/U$ und Basis von $V/U$ bestimmen

- **Motivation.** Konkret mit Quotienten rechnen (Klausur: „Bestimmen Sie eine Basis von $V/U$").
- **Idee.** Basis von $U$ zu einer Basis von $V$ ergänzen; die *Ergänzungsvektoren* liefern (als Nebenklassen) eine Basis von $V/U$.
- **Voraussetzungen.** $\dim V<\infty$, Unterraum $U$ gegeben (z. B. durch Erzeuger).
- **Pseudocode.**
  ```
  Eingabe: Basis {b_1,...,b_m} von U,  Vektorraum V (dim n+m)
  1. Ergänze {b_1,...,b_m} zu einer Basis {b_1,...,b_m, v_1,...,v_n} von V
     (z. B. via Gauß: linear unabhängige v_j hinzufügen)
  2. Ausgabe: { v_1+U, ..., v_n+U }  als Basis von V/U
  Rechnen:  (v+U)+(w+U) = (v+w)+U;   reduziere v mod U,
            indem du den U-Anteil (Linearkombination der b_i) abziehst.
  ```
- **Mathematische Beschreibung.** Liefert die Basis aus Satz 1.9; $\dim(V/U)=n$.
- **Laufzeit.** Dominiert von der Basisergänzung (Gauß): $O((m+n)^3)$ Körperoperationen.
- **Speicherbedarf.** $O((m+n)^2)$.
- **Korrektheitsidee.** Satz 1.9.
- **Anwendungen.** Reduktion der Dimension in Induktionsbeweisen; konkrete Berechnung induzierter Abbildungen $\bar f$.
- **Typische Fehler.** $U$-Anteil beim „Reduzieren mod $U$" nicht vollständig abziehen; Ergänzungsvektoren wählen, die *in* $U$ liegen (dann linear abhängig).

---

<a id="beispiele-1"></a>
## Beispiele

**Beispiel 1 (leicht — Gerade in $\mathbb{R}^2$).** $V=\mathbb{R}^2$, $U=\big\{\binom{x}{y}\mid x+y=0\big\}=\mathrm{span}\binom{1}{-1}$.
Die Nebenklasse von $\binom{a}{b}$ ist die zu $U$ parallele Gerade durch $\binom{a}{b}$:
$$
\binom{a}{b}+U=\Big\{\binom{x}{y}\ \Big|\ x+y=a+b\Big\}.
$$
Zwei Vektoren liegen in derselben Klasse $\Leftrightarrow$ gleiche Summe $x+y$. Also $V/U\cong\mathbb{R}$ via $\binom{a}{b}+U\mapsto a+b$. Basis: $\binom{1}{0}+U$.

**Beispiel 2 (mittel — Dimension).** $V=\mathbb{R}^4$, $U=\mathrm{span}(e_1,e_2)$. Basisergänzung: $\{e_1,e_2,e_3,e_4\}$. Also Basis von $V/U$: $\{e_3+U,\,e_4+U\}$, $\dim(V/U)=2$. Konkret: $e_3+U$ und $e_4+U$ „messen" die letzten beiden Koordinaten.

**Beispiel 3 (mittel — modulares Rechnen als Quotient).** $\mathbb{Z}/5\mathbb{Z}$ ist der Quotient des $\mathbb{Z}$-Moduls $\mathbb{Z}$ nach dem Untermodul $5\mathbb{Z}$. Dieselbe Mechanik: $a\sim b\Leftrightarrow 5\mid(a-b)$.

**Beispiel 4 (schwer — Quotientenring $\mathbb{C}$).** $\mathbb{R}[X]/(X^2+1)$: Hier ist $V=\mathbb{R}[X]$ und $U=(X^2+1)\cdot\mathbb{R}[X]$ das von $X^2+1$ erzeugte Ideal. Jedes Polynom ist mod $X^2+1$ kongruent zu seinem Rest $a+bX$ (Polynomdivision!). Mit der von der Multiplikation induzierten Struktur entsteht **$\mathbb{C}$**, wobei $\bar X$ die Rolle von $i$ spielt ($\bar X^2=\overline{X^2}=\overline{-1}=-1$). Das greift Kapitel 5 auf.

**Beispiel 5 (schwer — induzierte Abbildung).** Sei $f\colon V\to V$ linear und $U$ ein $f$-**invarianter** Unterraum ($f(U)\subseteq U$). Dann ist
$$
\bar f\colon V/U\to V/U,\qquad \bar f(v+U):=f(v)+U
$$
wohldefiniert (universelle Eigenschaft, angewandt auf $p_U\circ f$, das $U$ in den Kern schickt). Genau diese induzierte Abbildung trägt die Induktionsbeweise in Kap. 2 und 4.

---

<a id="gegenbeispiele-1"></a>
## Gegenbeispiele

**Gegenbeispiel A ($U$ keine Untergruppe/kein Unterraum $\Rightarrow$ nicht wohldefiniert).**
Nimm in $\mathbb{R}^2$ die Teilmenge $U=\{(t,0)\mid t\ge0\}$ (Halbgerade, *kein* Unterraum). Definierte man $v\sim v'\Leftrightarrow v-v'\in U$, so wäre $\sim$ nicht einmal symmetrisch ($(1,0)-(0,0)\in U$, aber $(0,0)-(1,0)\notin U$). Quotientenbildung scheitert. **Die Unterraumeigenschaft ist unverzichtbar.**

**Gegenbeispiel B (universelle Eigenschaft ohne $U\subseteq\ker f$).**
Sei $V=\mathbb{R}^2$, $U=\mathrm{span}(e_1)$, $f=\mathrm{id}$. Dann ist $U\not\subseteq\ker f=\{0\}$. Die „Vorschrift" $g(v+U)=f(v)=v$ ist **nicht** wohldefiniert: $e_1+U=0+U$, aber $f(e_1)=e_1\neq0=f(0)$. Ohne $U\subseteq\ker f$ gibt es kein $g$.

**Gegenbeispiel C (Dimension im unendlichdim. Fall).**
Für $V=\mathbb{R}[X]$ und $U=\{P\mid P(0)=0\}$ ist $\dim V=\dim U=\infty$, aber $\dim(V/U)=1$ (jede Klasse bestimmt durch $P(0)$). Die naive „Differenzformel" $\dim V-\dim U=\infty-\infty$ ist sinnlos — Satz 1.9 braucht $\dim V<\infty$.

---

<a id="typische-klausuraufgaben-1"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Woran erkennbar | Strategie |
|---|---|---|
| **Basis/Dimension von $V/U$** | „Bestimmen Sie eine Basis von $V/U$." | Basis von $U$ zu Basis von $V$ ergänzen; Ergänzungsvektoren $\bmod\,U$ nehmen (Satz 1.9). |
| **Wohldefiniertheit zeigen** | „Zeigen Sie, dass $g$/die Operation wohldefiniert ist." | Repräsentantenunabhängigkeit nachrechnen; Unterraumeigenschaft von $U$ nutzen. |
| **Universelle Eigenschaft anwenden** | „Zeigen Sie, dass $f$ über $V/U$ faktorisiert." | $U\subseteq\ker f$ prüfen, dann Satz 1.8. |
| **Induzierte Abbildung $\bar f$** | „$U$ ist $f$-invariant; definieren Sie $\bar f$ auf $V/U$." | Wohldefiniertheit via $f(U)\subseteq U$; Matrix von $\bar f$ aus Ergänzungsbasis ablesen. |
| **Homomorphiesatz** | „Zeigen Sie $V/\ker f\cong\mathrm{Bild}\,f$." | $g\colon V/\ker f\to\mathrm{Bild}\,f$ aus Satz 1.8; Injektivität + Surjektivität. |

---

<a id="typische-fehler-1"></a>
## Typische Fehler

| Fehler | Warum falsch | Richtig |
|---|---|---|
| Nebenklassen als „Mengen von Zahlen" verrechnen | Elemente von $V/U$ sind *ganze* affine Teilräume. | Mit Repräsentanten rechnen; Resultat ist wieder eine Nebenklasse. |
| Wohldefiniertheit unterschlagen | Ohne sie ist $+,\cdot$ (oder $g$) gar keine Abbildung. | Immer Repräsentantenunabhängigkeit prüfen. |
| Universelle Eigenschaft ohne $U\subseteq\ker f$ | Dann existiert $g$ nicht (Gegenbeispiel B). | Voraussetzung $U\subseteq\ker f$ explizit nachweisen. |
| Ergänzungsvektoren aus $U$ wählen | Sie liefern $v_j+U=0$, also keine Basis. | $v_j$ **außerhalb** $U$, linear unabhängig modulo $U$. |
| $\dim(V/U)=\dim V-\dim U$ blind im $\infty$-Fall | Formel nur endlichdimensional gültig. | Voraussetzung $\dim V<\infty$ beachten. |
| $V/U$ mit $U^\perp$ oder „Komplement" verwechseln | $V/U$ ist *kein* Unterraum von $V$. | $V/U$ ist ein *eigener* Vektorraum aus Nebenklassen. |

> **Vergleichstabelle: $V/U$ vs. Komplement $U'$ (mit $V=U\oplus U'$).**
>
> | | Quotient $V/U$ | Komplement $U'$ |
> |---|---|---|
> | Was ist es? | Vektorraum aus Nebenklassen $v+U$ | Unterraum von $V$ |
> | Teil von $V$? | nein (eigener Raum) | ja |
> | Eindeutig? | ja (kanonisch) | nein (viele Komplemente) |
> | Dimension | $\dim V-\dim U$ | $\dim V-\dim U$ |
> | Beziehung | $U'\xrightarrow{\ p_U\ }V/U$ ist ein Isomorphismus | liefert konkretes Modell für $V/U$ |
>
> Merksatz: $V/U$ ist „kanonisch, aber abstrakt"; ein Komplement $U'$ ist „konkret, aber unkanonisch". $p_U|_{U'}$ verbindet beide.

---

<a id="verbindungen-1"></a>
## Verbindungen

- **→ Kapitel 2 (Trigonalisierbarkeit):** Der Induktionsbeweis „$\chi_f$ zerfällt $\Rightarrow$ $f$ trigonalisierbar" wählt einen Eigenvektor, bildet $U=\mathrm{span}(b_1)$ und arbeitet mit $\bar f\colon V/U\to V/U$ — mit $\dim(V/U)=\dim V-1$. Es gilt $\chi_f=\chi_{f|_U}\cdot\chi_{\bar f}$.
- **→ Kapitel 4 (Jordan):** Dieselbe Technik (Reduktion auf $V/U$) trägt die Existenz der Jordan-Normalform und die Hauptraumzerlegung.
- **→ Kapitel 5 ($\mathbb{C}$):** $\mathbb{C}=\mathbb{R}[X]/(X^2+1)$ ist ein Quotient; das Rechnen „$\bmod\,(X^2+1)$" ist Beispiel 4.
- **← Kapitel 0:** Die Quotientenkonstruktion verallgemeinert „$\bmod\,n$" / „$\bmod\,P$" (Polynomdivision liefert die Repräsentanten).
- **← Lineare Algebra 1:** Basisergänzungssatz, Dimensionsformel, lineare Abbildungen, Kern/Bild.

**Definitionen, die später ständig gebraucht werden:** kanonische Projektion $p_U$, induzierte Abbildung $\bar f$, universelle Eigenschaft, $\dim(V/U)=\dim V-\dim U$.

---

<a id="zusammenfassung-1"></a>
## Zusammenfassung

| Kernaussage | Symbolisch |
|---|---|
| $v\sim v'\Leftrightarrow v-v'\in U$; Klassen $=$ Nebenklassen. | $v+U$ |
| $V/U$ ist Vektorraum (Operationen wohldefiniert, weil $U$ Unterraum). | (Satz 1.6) |
| Projektion ist linear, surjektiv, Kern $U$. | $\ker p_U=U$ |
| Jede auf $U$ verschwindende Abbildung faktorisiert eindeutig über $V/U$. | $f=g\circ p_U$ (Satz 1.8) |
| Dimension senkt sich kontrolliert. | $\dim(V/U)=\dim V-\dim U$ |
| $f$-invariantes $U$ liefert induziertes $\bar f$ auf $V/U$. | $\bar f(v+U)=f(v)+U$ |

**Die eine Idee des Kapitels:** $V/U$ ist „$V$, in dem man $U$ ignoriert". Es senkt die Dimension um $\dim U$ und erlaubt es, lineare Abbildungen auf einem *kleineren* Raum fortzuführen — die Grundlage aller Induktionsbeweise der Normalformentheorie.



---

<a id="kapitel-2-eigenwerte-diagonalisierung-und-trigonalisierung"></a>
# Kapitel 2 — Eigenwerte, Diagonalisierung und Trigonalisierung

> **Stellung im Kurs.** Hier beginnt das eigentliche Programm der LinA 2: lineare Abbildungen
> *klassifizieren*, indem man eine Basis sucht, in der die Matrix maximal einfach ist. Dieses
> Kapitel klärt die beiden „leichteren" Normalformen — **Diagonalmatrix** (bester Fall) und
> **obere Dreiecksmatrix** (zweitbester Fall) — und macht präzise, *wann* sie erreichbar sind.
> Beide Antworten lesen sich vollständig am charakteristischen Polynom ab. Die schwierigste
> Normalform (Jordan) folgt in Kapitel 4.

---

<a id="motivation-2"></a>
## Motivation

Eine lineare Abbildung $f\colon V\to V$ kann man durch verschiedene Matrizen darstellen — je nach gewählter Basis. Die Frage ist:

> **Welche Basis macht die Matrix so einfach wie möglich?**

**Warum „einfach" so wichtig ist.** Mit einer Diagonalmatrix $D=\mathrm{diag}(\lambda_1,\dots,\lambda_n)$ wird *alles* trivial:
$$
D^m=\mathrm{diag}(\lambda_1^m,\dots,\lambda_n^m),\qquad e^{D}=\mathrm{diag}(e^{\lambda_1},\dots,e^{\lambda_n}),
$$
Potenzen, Exponentiale, Inverse, Determinanten — koordinatenweise. Genau das braucht man, um **lineare Differentialgleichungssysteme** $\dot{x}=Ax$ zu lösen, **Markovketten** $x_{m+1}=Ax_m$ langfristig zu verstehen, **Rekursionen** wie Fibonacci geschlossen zu lösen, oder **Hauptachsen** quadratischer Formen zu finden.

**Die geometrische Idee.** Ein **Eigenvektor** ist eine Richtung, die $f$ *nicht dreht*, sondern nur **streckt**: $f(v)=\lambda v$. Findet man genug solche Richtungen, um eine Basis zu bilden, dann „zerfällt" $f$ in lauter unabhängige Streckungen — und in dieser Basis ist die Matrix diagonal. Diagonalisierbarkeit heißt also: **$V$ zerlegt sich vollständig in Streckrichtungen von $f$.**

**Wenn das scheitert.** Manchmal gibt es nicht genug Eigenvektoren (Scherungen haben nur *eine* invariante Richtung), oder über $\mathbb{R}$ gar keine (Drehungen drehen *alles*). Dann fragt man bescheidener: Gibt es wenigstens eine Basis, in der die Matrix **obere Dreiecksgestalt** hat? Das ist **Trigonalisierbarkeit** — geometrisch: eine *Kette ineinander geschachtelter invarianter Unterräume* (eine **Fahne**).

**Mathematische Wurzel.** Beide Begriffe hängen am charakteristischen Polynom $\chi_f$, das die Eigenwerte als Nullstellen kodiert (Cauchy, Cayley, 19. Jh.). Die Brücke „Nullstelle $\Leftrightarrow$ Linearfaktor" aus Kapitel 0 wird hier zur Brücke „Eigenwert $\Leftrightarrow$ Linearfaktor von $\chi_f$".

---

<a id="intuition-2"></a>
## Intuition

**Eigenvektor = unverdrehte Achse.** Lege ein Gummituch (= $V$), wende $f$ an. Die meisten Pfeile ändern Richtung *und* Länge. Eigenvektoren sind die Pfeile, deren *Richtung gleich bleibt* — sie werden nur um den Faktor $\lambda$ gestreckt (bzw. gestaucht/gespiegelt bei $\lambda<0$).

**Diagonalisierbar = genug Achsen.** Wenn man $n$ unabhängige solche Achsen findet, kann man $V$ in dieser „Eigenbasis" beschreiben, und $f$ tut nichts anderes, als entlang jeder Achse zu strecken. Bild:

```
   f wirkt diagonal in der Eigenbasis:
   Achse 1 ──×λ₁──>      Achse 2 ──×λ₂──>     ...    Achse n ──×λₙ──>
   (unabhängige Streckungen, keine Vermischung)
```

**Trigonalisierbar = gestaffelte Invarianz.** Auch ohne volle Eigenbasis kann es eine **Fahne** geben
$$
\{0\}\subsetneq U_1\subsetneq U_2\subsetneq\dots\subsetneq U_n=V,\qquad f(U_i)\subseteq U_i,
$$
mit $\dim U_i=i$. Wählt man eine Basis „entlang der Fahne", wird die Matrix obere Dreiecksmatrix: $f(b_i)$ bleibt im bereits aufgespannten Bereich $U_i$. Geometrisch: $f$ „mischt nur nach oben", nie nach unten.

**Charakteristisches Polynom als Detektor.** $\chi_f(\lambda)=\det(\lambda\,\mathrm{id}-f)$ ist genau dann $0$, wenn $\lambda\,\mathrm{id}-f$ *nicht invertierbar* ist — wenn es also einen Vektor $\neq0$ gibt, den $f$ um $\lambda$ streckt. $\chi_f$ ist der **Eigenwert-Detektor**: seine Nullstellen sind die Eigenwerte.

---

<a id="formale-definitionen-2"></a>
## Formale Definitionen

Sei $k$ ein Körper, $V$ ein endlichdimensionaler $k$-Vektorraum, $\dim V=n$, $f\colon V\to V$ linear, $A\in k^{n\times n}$.

**Definition 2.1 (Eigenwert, Eigenvektor, Eigenraum).**
$\lambda\in k$ heißt **Eigenwert** von $f$, wenn es $v\in V\setminus\{0\}$ mit $f(v)=\lambda v$ gibt; ein solches $v$ heißt **Eigenvektor** zum Eigenwert $\lambda$. Der **Eigenraum** ist
$$
\mathrm{Eig}(f,\lambda):=\{v\in V\mid f(v)=\lambda v\}=\ker(\lambda\,\mathrm{id}_V-f).
$$
Für Matrizen: $\mathrm{Eig}(A,\lambda)=\ker(\lambda E_n-A)$. (Hier ist $0\in\mathrm{Eig}$ enthalten — der Eigenraum ist ein Unterraum; Eigenvektoren sind die Elemente $\neq0$.)

**Definition 2.2 (charakteristisches Polynom).**
$$
\chi_A:=\det(X\,E_n-A)\in k[X],\qquad \chi_f:=\det(X\,E_n-A)\ \text{für eine darstellende Matrix }A\text{ von }f.
$$
$\chi_f$ ist **normiert** vom Grad $n$ und basisunabhängig (siehe Satz 2.10).

**Definition 2.3 (algebraische und geometrische Vielfachheit).**
Ist $\lambda$ Eigenwert und $\chi_f=(X-\lambda)^{n_\lambda}\cdot Q$ mit $Q(\lambda)\neq0$, so heißt $n_\lambda$ die **algebraische Vielfachheit** von $\lambda$. Die **geometrische Vielfachheit** ist $\dim\mathrm{Eig}(f,\lambda)$.

**Definition 2.4 (diagonalisierbar).**
$f$ heißt **diagonalisierbar**, wenn es eine Basis von $V$ aus Eigenvektoren von $f$ gibt (dann ist die darstellende Matrix diagonal). $A\in k^{n\times n}$ heißt diagonalisierbar, wenn $f_A\colon k^n\to k^n,\ x\mapsto Ax$ diagonalisierbar ist — äquivalent: $A$ ist **ähnlich** zu einer Diagonalmatrix.

**Definition 2.5 (trigonalisierbar).**
$f$ heißt **trigonalisierbar**, wenn es eine Basis von $V$ gibt, bzgl. der die darstellende Matrix eine **obere Dreiecksmatrix** ist. $A$ heißt trigonalisierbar, wenn $A$ ähnlich zu einer oberen Dreiecksmatrix ist.

**Definition 2.6 (zerfällt in Linearfaktoren).**
$\chi_f$ **zerfällt über $k$ in Linearfaktoren**, wenn $\chi_f=(X-\lambda_1)^{n_1}\cdots(X-\lambda_r)^{n_r}$ mit $\lambda_i\in k$, $n_i\ge1$, $n_1+\dots+n_r=n$.

**Definition 2.7 (ähnlich).**
$A,B\in k^{n\times n}$ heißen **ähnlich** ($A\sim B$), wenn es eine invertierbare Matrix $T$ mit $B=TAT^{-1}$ gibt. Ähnlichkeit ist eine Äquivalenzrelation; ähnliche Matrizen stellen *dieselbe* lineare Abbildung in verschiedenen Basen dar.

---

<a id="eigenschaften-2"></a>
## Eigenschaften

| Eigenschaft | Aussage | Kurzbegründung |
|---|---|---|
| **Eigenwert $\Leftrightarrow$ Nullstelle** | $\lambda$ Eigenwert $\Leftrightarrow \chi_f(\lambda)=0$ | $\mathrm{Eig}\neq\{0\}\Leftrightarrow\lambda\,\mathrm{id}-f$ singulär $\Leftrightarrow\det=0$. |
| **$\chi_f$ normiert, Grad $n$** | Leitkoeffizient $1$, $\deg\chi_f=n$ | Determinante von $X E_n-A$. |
| **höchstens $n$ Eigenwerte** | Anzahl verschiedener Eigenwerte $\le n$ | $\le\deg\chi_f$ Nullstellen (Satz 0.19). |
| **Vielfachheitsschranke** | $1\le\dim\mathrm{Eig}(f,\lambda)\le n_\lambda$ | geom. $\le$ alg. Vielfachheit (Lemma 2.13). |
| **Eigenräume unabhängig** | Summe verschiedener Eigenräume ist direkt | Eigenvektoren zu versch. Eigenwerten lin. unabh. (Lemma 2.11). |
| **$\chi$ ähnlichkeitsinvariant** | $A\sim B\Rightarrow\chi_A=\chi_B$ | $\det(XE-TAT^{-1})=\det(T(XE-A)T^{-1})=\det(XE-A)$. |
| **Dreieck: $\chi=\prod(X-a_{ii})$** | $\chi$ einer Dreiecksmatrix $=$ Produkt der Diagonale | Determinante einer Dreiecksmatrix. |
| **Spur & Determinante** | $\mathrm{tr}(A)=\sum\lambda_i$, $\det(A)=\prod\lambda_i$ (mit Vielfachh., falls $\chi$ zerfällt) | Koeffizienten von $\chi_A$. |

---

<a id="sätze-2"></a>
## Sätze

<a id="satz-28-eigenwert-kriterium"></a>
### Satz 2.8 (Eigenwert-Kriterium)

**Aussage.** $\lambda\in k$ ist Eigenwert von $f$ $\;\Longleftrightarrow\;\mathrm{Eig}(f,\lambda)\neq\{0\}\;\Longleftrightarrow\;\chi_f(\lambda)=0$.
**Bedeutung.** Reduziert die Eigenwertsuche auf das **Nullstellensuchen** eines Polynoms.
**Intuition.** $\lambda$ ist Eigenwert $\Leftrightarrow$ $f-\lambda\,\mathrm{id}$ „verliert eine Dimension".
**Konsequenzen.** Über $\mathbb{C}$ existiert (Fundamentalsatz) stets ein Eigenwert.

<a id="satz-29-diagonalisierbarkeitskriterium"></a>
### Satz 2.9 (Diagonalisierbarkeitskriterium)

**Aussage.** Sei $\chi_f=(X-\lambda_1)^{n_1}\cdots(X-\lambda_r)^{n_r}\cdot Q$ mit $\lambda_i$ paarweise verschieden, $Q$ ohne Nullstelle in $k$. Dann sind äquivalent:
1. $f$ ist diagonalisierbar;
2. $\chi_f$ zerfällt ($Q=1$, d. h. $n_1+\dots+n_r=n$) **und** $\dim\mathrm{Eig}(f,\lambda_i)=n_i$ für alle $i$;
3. $V=\bigoplus_{i=1}^r\mathrm{Eig}(f,\lambda_i)$;
4. $\sum_{i=1}^r\dim\mathrm{Eig}(f,\lambda_i)=n$.

Ein **hinreichendes** (nicht notwendiges) Kriterium: hat $f$ **$n$ paarweise verschiedene Eigenwerte**, so ist $f$ diagonalisierbar.

**Voraussetzungen.** $\dim V=n<\infty$.
**Bedeutung.** Das praktische Werkzeug: „zerfällt $\chi$? und stimmen geometrische und algebraische Vielfachheiten überein?"
**Intuition.** Diagonalisierbar $\Leftrightarrow$ es gibt *so viele* unabhängige Eigenvektoren wie Dimensionen.
**Konsequenzen.** Defekte (= nicht diagonalisierbare) Abbildungen erkennt man an einer „zu kleinen" geometrischen Vielfachheit.

<a id="satz-210-chi_f-ist-wohldefiniert"></a>
### Satz 2.10 ($\chi_f$ ist wohldefiniert)

**Aussage.** $\chi_f$ hängt nicht von der gewählten darstellenden Matrix ab.
**Beweisstil.** *direkt* (Ähnlichkeitsinvarianz, siehe Eigenschaftstabelle).
**Bedeutung.** Erlaubt, von „dem" charakteristischen Polynom einer Abbildung zu sprechen.

<a id="satz-211-trigonalisierbarkeitskriterium-hauptsatz-des-kapitels"></a>
### Satz 2.11 (Trigonalisierbarkeitskriterium) — *Hauptsatz des Kapitels*

**Aussage.** $f\colon V\to V$ ($\dim V=n<\infty$) ist trigonalisierbar $\;\Longleftrightarrow\;\chi_f$ **zerfällt über $k$ in Linearfaktoren**.
Äquivalente Matrixfassung: $A\in k^{n\times n}$ ist trigonalisierbar $\Leftrightarrow\chi_A$ zerfällt über $k$.
**Voraussetzungen.** $\dim V<\infty$.
**Bedeutung.** Klärt vollständig, *wann* die Dreiecksform erreichbar ist — und liefert das Standard-Korollar: **über $\mathbb{C}$ ist jede Matrix trigonalisierbar** (Fundamentalsatz).
**Intuition.** „Genug Eigenwerte (mit Vielfachheit) im Körper" $\Leftrightarrow$ es existiert eine Fahne invarianter Unterräume.
**Konsequenzen.** Existenz der Jordan-Normalform (Kap. 4) baut hierauf auf; $\mathrm{tr}$ und $\det$ als Summe/Produkt der Eigenwerte (über $\mathbb{C}$ immer gültig).

<a id="lemma-212-chi-zerlegt-sich-an-invariantem-unterraum"></a>
### Lemma 2.12 ($\chi$ zerlegt sich an invariantem Unterraum)

**Aussage.** Ist $U\subseteq V$ ein $f$-invarianter Unterraum und $\bar f\colon V/U\to V/U$ die induzierte Abbildung, so gilt
$$
\chi_f=\chi_{f|_U}\cdot\chi_{\bar f}.
$$
**Bedeutung.** Das Bindeglied zwischen Kapitel 1 (Quotient) und der Induktion im Trigonalisierbarkeitsbeweis.

<a id="lemma-213-geometrische-le-algebraische-vielfachheit"></a>
### Lemma 2.13 (geometrische $\le$ algebraische Vielfachheit)

**Aussage.** Für jeden Eigenwert $\lambda$: $\ 1\le\dim\mathrm{Eig}(f,\lambda)\le n_\lambda$.
**Bedeutung.** Erklärt, warum „$\chi$ zerfällt" allein nicht für Diagonalisierbarkeit reicht.

---

<a id="beweise-2"></a>
## Beweise

> **Klausurrelevant in voller Tiefe:** Satz 2.8, Lemma 2.11 (Eigenvektoren lin. unabh.), Lemma 2.13,
> Satz 2.9 (Kriterium) und **Satz 2.11 (Trigonalisierbarkeit)**. Letzterer ist *der* klassische
> Induktionsbeweis der Vorlesung.

<a id="beweis-von-satz-28-beweisstil-direkt-äquivalenzkette"></a>
### Beweis von Satz 2.8 — *Beweisstil: direkt (Äquivalenzkette)*

$$
\lambda\ \text{Eigenwert}
\Leftrightarrow \exists v\neq0:\ (\lambda\,\mathrm{id}-f)v=0
\Leftrightarrow \ker(\lambda\,\mathrm{id}-f)\neq\{0\}
\Leftrightarrow \lambda\,\mathrm{id}-f\ \text{singulär}
\Leftrightarrow \det(\lambda\,\mathrm{id}-f)=0
\Leftrightarrow \chi_f(\lambda)=0.\ \blacksquare
$$

<a id="lemma-211-eigenvektoren-zu-verschiedenen-eigenwerten-sind-linear-unabhängig-beweisstil-induktion"></a>
### Lemma 2.11′ (Eigenvektoren zu verschiedenen Eigenwerten sind linear unabhängig) — *Beweisstil: Induktion*

Seien $v_1,\dots,v_m$ Eigenvektoren zu **paarweise verschiedenen** Eigenwerten $\lambda_1,\dots,\lambda_m$. Induktion über $m$. $m=1$: $v_1\neq0$, klar. Schritt: Sei
$$
a_1v_1+\dots+a_mv_m=0.\tag{$\ast$}
$$
Wende $f$ an und ziehe das $\lambda_m$-fache von $(\ast)$ ab:
$$
f(\ast):\ \sum_i a_i\lambda_i v_i=0,\qquad
f(\ast)-\lambda_m(\ast):\ \sum_{i=1}^{m-1}a_i(\lambda_i-\lambda_m)v_i=0.
$$
Nach Induktionsvoraussetzung sind $v_1,\dots,v_{m-1}$ unabhängig, also $a_i(\lambda_i-\lambda_m)=0$. Da $\lambda_i\neq\lambda_m$, folgt $a_i=0$ für $i<m$. Eingesetzt in $(\ast)$: $a_mv_m=0$, also $a_m=0$. $\blacksquare$

**Korollar.** Die Summe $\sum_i\mathrm{Eig}(f,\lambda_i)$ über verschiedene Eigenwerte ist **direkt**.

<a id="beweis-von-lemma-213-beweisstil-basisergänzung-blockdeterminante"></a>
### Beweis von Lemma 2.13 — *Beweisstil: Basisergänzung + Blockdeterminante*

Sei $m=\dim\mathrm{Eig}(f,\lambda)$, $\{w_1,\dots,w_m\}$ Basis des Eigenraums, ergänzt zu einer Basis von $V$. Bzgl. dieser Basis hat $f$ Blockgestalt
$$
A=\begin{pmatrix}\lambda E_m & *\\ 0 & B\end{pmatrix}
\ \Rightarrow\
\chi_f=\det(XE-A)=(X-\lambda)^m\cdot\chi_B.
$$
Also $(X-\lambda)^m\mid\chi_f$, d. h. $n_\lambda\ge m$. Die untere Schranke $1\le m$ gilt, da $\lambda$ Eigenwert ist. $\blacksquare$

<a id="beweis-von-satz-29-diagonalisierbarkeitskriterium-beweisstil-ringschluss"></a>
### Beweis von Satz 2.9 (Diagonalisierbarkeitskriterium) — *Beweisstil: Ringschluss*

$(1)\Leftrightarrow(3)$: $f$ diagonalisierbar $\Leftrightarrow$ es gibt eine Basis aus Eigenvektoren $\Leftrightarrow$ $V$ wird von Eigenvektoren erzeugt $\Leftrightarrow$ $V=\sum_i\mathrm{Eig}(f,\lambda_i)$. Da diese Summe stets direkt ist (Korollar zu 2.11′), ist das $\Leftrightarrow V=\bigoplus_i\mathrm{Eig}(f,\lambda_i)$.

$(3)\Leftrightarrow(4)$: Bei direkter Summe gilt $\dim\big(\bigoplus_i\mathrm{Eig}\big)=\sum_i\dim\mathrm{Eig}$. Diese Summe $=n\Leftrightarrow\bigoplus_i\mathrm{Eig}=V$.

$(2)\Leftrightarrow(4)$: Stets $\dim\mathrm{Eig}(f,\lambda_i)\le n_i$ (Lemma 2.13) und $\sum_i n_i\le n$ (mit „$=$" $\Leftrightarrow\chi$ zerfällt). Daher
$$
\sum_i\dim\mathrm{Eig}(f,\lambda_i)\ \le\ \sum_i n_i\ \le\ n.
$$
Gleichheit links $=n$ erzwingt beide Ungleichungen als Gleichheiten: $\chi$ zerfällt **und** $\dim\mathrm{Eig}=n_i$ überall.

**Hinreichendes Kriterium:** $n$ verschiedene Eigenwerte liefern $n$ unabhängige Eigenvektoren (Lemma 2.11′), also eine Eigenbasis. $\blacksquare$

<a id="beweis-von-lemma-212-beweisstil-direkt-blockmatrix"></a>
### Beweis von Lemma 2.12 — *Beweisstil: direkt (Blockmatrix)*

Wähle eine Basis $b_1,\dots,b_s$ von $U$, ergänzt zu $b_1,\dots,b_s,v_1,\dots,v_t$ von $V$. Da $f(U)\subseteq U$, hat $f$ Blockgestalt $\begin{psmallmatrix}A_{11}&A_{12}\\0&A_{22}\end{psmallmatrix}$, wobei $A_{11}$ die Matrix von $f|_U$ ist und $A_{22}$ (modulo $U$) die Matrix von $\bar f$. Block-Dreiecks-Determinante:
$$
\chi_f=\det(XE-A)=\det(XE-A_{11})\cdot\det(XE-A_{22})=\chi_{f|_U}\cdot\chi_{\bar f}.\ \blacksquare
$$

<a id="beweis-von-satz-211-trigonalisierbarkeit-beweisstil-rightarrow-direkt-leftarrow-induktion-über-dim-v-via-quotient-vollständig"></a>
### Beweis von Satz 2.11 (Trigonalisierbarkeit) — *Beweisstil: $\Rightarrow$ direkt, $\Leftarrow$ Induktion über $\dim V$ via Quotient* ★ vollständig

**„$\Rightarrow$".** Ist $f$ trigonalisierbar, gibt es eine Basis mit oberer Dreiecksmatrix $A=(a_{ij})$, $a_{ij}=0$ für $i>j$. Dann
$$
\chi_f=\chi_A=\det(XE_n-A)=\prod_{i=1}^n(X-a_{ii})
$$
(Determinante einer Dreiecksmatrix $=$ Produkt der Diagonaleinträge). Also zerfällt $\chi_f$ in Linearfaktoren.

**„$\Leftarrow$".** Induktion über $n=\dim V$.

*Induktionsanfang* $n=1$: jede $1\times1$-Matrix ist (trivial) obere Dreiecksmatrix.

*Induktionsschritt* $n\ge2$: Sei $\chi_f=(X-a_1)(X-a_2)\cdots(X-a_n)$ mit $a_i\in k$. Insbesondere ist $a_1$ Nullstelle von $\chi_f$, also (Satz 2.8) **Eigenwert**; wähle einen Eigenvektor $b_1\neq0$, $f(b_1)=a_1b_1$. Setze
$$
U:=\mathrm{span}(b_1)\quad(\dim U=1,\ f\text{-invariant}).
$$
Betrachte den Quotienten $V/U$ und die induzierte Abbildung $\bar f\colon V/U\to V/U$, $\bar f(v+U)=f(v)+U$ (wohldefiniert, da $U$ $f$-invariant — Kapitel 1). Es ist $\dim(V/U)=n-1$, und nach Lemma 2.12
$$
\chi_f=\chi_{f|_U}\cdot\chi_{\bar f}=(X-a_1)\cdot\chi_{\bar f}
\ \Rightarrow\ \chi_{\bar f}=(X-a_2)\cdots(X-a_n).
$$
Also zerfällt $\chi_{\bar f}$ ebenfalls. Nach **Induktionsvoraussetzung** ist $\bar f$ trigonalisierbar: es gibt eine Basis $(\,v_2+U,\dots,v_n+U\,)$ von $V/U$, bzgl. der $\bar f$ obere Dreiecksmatrix hat, d. h.
$$
\bar f(v_j+U)=\sum_{i=2}^{j} c_{ij}\,(v_i+U)\qquad(j=2,\dots,n).\tag{$\dagger$}
$$

**Korrigierter Schlussschritt (Hochheben der Basis).** Da $\{v_2+U,\dots,v_n+U\}$ Basis von $V/U$ und $b_1$ Basis von $U$ ist, ist
$$
\mathcal{B}=(b_1,\,v_2,\dots,v_n)\quad\text{eine Basis von }V\quad(\text{Satz 1.9 rückwärts}).
$$
Wir prüfen, dass die Matrix von $f$ bzgl. $\mathcal{B}$ obere Dreiecksmatrix ist:

- *erste Spalte:* $f(b_1)=a_1b_1$ — nur der erste Basisvektor tritt auf. ✓
- *$j$-te Spalte* ($j\ge2$): Aus $(\dagger)$ folgt $f(v_j)-\sum_{i=2}^{j}c_{ij}v_i\in U=\mathrm{span}(b_1)$, also
$$
f(v_j)=\underbrace{\mu_j\, b_1}_{\text{Zeile }1}+\sum_{i=2}^{j} c_{ij}\,v_i\qquad(\mu_j\in k).
$$
In Koordinaten bzgl. $\mathcal{B}=(b_1,v_2,\dots,v_n)$ hat diese Spalte nur Einträge in Zeile $1$ (der $b_1$-Anteil $\mu_j$) und in den Zeilen $i\le j$ (die $c_{ij}$). Da $b_1$ der **erste** Basisvektor ist, liegen alle Einträge **auf oder oberhalb der Diagonale**. ✓

Damit ist die Matrix von $f$ bzgl. $\mathcal{B}$ obere Dreiecksmatrix — $f$ ist trigonalisierbar. $\blacksquare$

> **Warum dieser Schlussschritt nötig ist.** Die Induktion liefert die Dreiecksform nur für $\bar f$ *auf $V/U$*. Dass das Hochheben zu einer Dreiecksform für $f$ *auf ganz $V$* führt, muss man — wie oben — explizit nachrechnen. Genau hier hatte die Mitschrift eine Lücke (rotes „?").

---

<a id="algorithmen-2"></a>
## Algorithmen

<a id="algorithmus-diagonalisierung-einer-matrix"></a>
### Algorithmus — Diagonalisierung einer Matrix

- **Motivation.** Standard-Klausuraufgabe: „Ist $A$ diagonalisierbar? Wenn ja, gib $T$ und $D$ mit $D=T^{-1}AT$."
- **Idee.** Eigenwerte als Nullstellen von $\chi_A$ finden; für jeden eine Basis des Eigenraums berechnen; passen insgesamt $n$ unabhängige Eigenvektoren zusammen, ist $A$ diagonalisierbar.
- **Voraussetzungen.** $A\in k^{n\times n}$; Nullstellen von $\chi_A$ in $k$ bestimmbar.
- **Pseudocode.**
  ```
  Eingabe: A in k^{n×n}
  1. χ ← det(X·E_n − A)                       # charakteristisches Polynom
  2. Bestimme die verschiedenen Nullstellen λ_1,…,λ_r ∈ k mit Vielfachh. n_i
  3. falls Σ n_i < n:  return "χ zerfällt nicht über k ⇒ nicht diagonalisierbar (über k)"
  4. für jedes λ_i:
        B_i ← Basis von Kern(λ_i·E_n − A)      # via Gauß
        falls |B_i| < n_i:  return "geom. < alg. Vielfachheit ⇒ NICHT diagonalisierbar"
  5. T ← Matrix mit Spalten = alle Eigenvektoren aus B_1,…,B_r
     D ← diag(λ_1,…,λ_1, λ_2,…)               # passend zu den Spalten von T
  6. return T, D       # es gilt A·T = T·D, also D = T^{-1} A T
  ```
- **Mathematische Beschreibung.** Liefert (falls möglich) $T$ invertierbar mit $T^{-1}AT=D$ diagonal; Korrektheit ist Satz 2.9.
- **Laufzeit.** $\chi$ berechnen $O(n^3)$ (z. B. Faddeev–LeVerrier); Nullstellen je nach $k$; jeder Eigenraum per Gauß $O(n^3)$. Gesamt $\approx O(n^3)$ plus Nullstellensuche.
- **Speicherbedarf.** $O(n^2)$.
- **Korrektheitsidee.** Eigenvektoren zu verschiedenen Eigenwerten sind unabhängig (Lemma 2.11′); Schritt 4 stellt geom. $=$ alg. Vielfachheit sicher $\Rightarrow$ Eigenbasis (Satz 2.9).
- **Anwendungen.** $A^m$, $e^{tA}$, lineare DGL/Rekursionen, Hauptachsentransformation.
- **Typische Fehler.** Schritt 3/4 weglassen (nur „$\chi$ zerfällt" prüfen reicht nicht!); Eigenraum als **Bild** statt **Kern** rechnen; Reihenfolge der Spalten von $T$ nicht zur Diagonale von $D$ passend; Körper $k$ ignorieren.

<a id="algorithmus-skizze-trigonalisierung"></a>
### Algorithmus-Skizze — Trigonalisierung

Falls $\chi_A$ zerfällt, aber $A$ nicht diagonalisierbar: Eigenvektor $b_1$ zu $a_1$ wählen, in $V/U$ rekursiv weiter (genau der Beweis von Satz 2.11). Praktisch in Klausuren seltener verlangt als Diagonalisierung; meist über die Jordan-Form (Kap. 4) erledigt.

---

<a id="beispiele-2"></a>
## Beispiele

**Beispiel 1 (leicht — diagonalisierbar, verschiedene Eigenwerte).** $A=\begin{psmallmatrix}2&1\\0&3\end{psmallmatrix}$ über $\mathbb{R}$. $\chi_A=(X-2)(X-3)$, zwei verschiedene Eigenwerte $\Rightarrow$ diagonalisierbar. Eigenvektoren: $\mathrm{Eig}(2)=\mathrm{span}\binom{1}{0}$, $\mathrm{Eig}(3)=\mathrm{span}\binom{1}{1}$. $T=\begin{psmallmatrix}1&1\\0&1\end{psmallmatrix}$, $D=\mathrm{diag}(2,3)$.

**Beispiel 2 (mittel — $\chi$ zerfällt, aber prüfen!).** $A=\begin{psmallmatrix}5&-1\\1&3\end{psmallmatrix}$. $\chi_A=X^2-8X+16=(X-4)^2$. Eigenwert $4$, alg. Vielfachheit $2$. $\mathrm{Eig}(4)=\ker\begin{psmallmatrix}1&-1\\1&-1\end{psmallmatrix}=\mathrm{span}\binom{1}{1}$, geom. Vielfachheit $1<2$. **Nicht diagonalisierbar** (aber trigonalisierbar, da $\chi$ zerfällt).

**Beispiel 3 (mittel — über $\mathbb{C}$ doch diagonalisierbar).** Drehmatrix $A=\begin{psmallmatrix}0&-1\\1&0\end{psmallmatrix}$. $\chi_A=X^2+1$.
- Über $\mathbb{R}$: keine Nullstelle $\Rightarrow$ kein Eigenwert $\Rightarrow$ **nicht** trigonalisierbar.
- Über $\mathbb{C}$: Eigenwerte $\pm i$, verschieden $\Rightarrow$ diagonalisierbar, $D=\mathrm{diag}(i,-i)$.

**Beispiel 4 (mittel — Parameteraufgabe).** $A=\begin{psmallmatrix}1&t\\0&1\end{psmallmatrix}$. $\chi=(X-1)^2$, Eigenwert $1$. $\mathrm{Eig}(1)=\ker\begin{psmallmatrix}0&t\\0&0\end{psmallmatrix}$: für $t=0$ ist das ganz $\mathbb{R}^2$ (diagonalisierbar, $A=E$); für $t\neq0$ nur $\mathrm{span}\binom{1}{0}$, geom. $1<2$, **nicht** diagonalisierbar.

**Beispiel 5 (schwer — $3\times3$).** $A=\begin{psmallmatrix}2&0&0\\1&2&0\\0&0&3\end{psmallmatrix}$. $\chi=(X-2)^2(X-3)$. $\mathrm{Eig}(3)=\mathrm{span}\,e_3$ (geom $=$ alg $=1$). $\mathrm{Eig}(2)=\ker\begin{psmallmatrix}0&0&0\\1&0&0\\0&0&1\end{psmallmatrix}=\mathrm{span}\,e_2$ — geom. Vielfachheit $1<2$. **Nicht diagonalisierbar**; trigonalisierbar (Jordan-Block zu $2$).

---

<a id="gegenbeispiele-2"></a>
## Gegenbeispiele

**Gegenbeispiel A (Scherung — defekt trotz zerfallendem $\chi$).** $\begin{psmallmatrix}1&1\\0&1\end{psmallmatrix}$: $\chi=(X-1)^2$ zerfällt, aber nur eine Eigenrichtung. *„$\chi$ zerfällt" $\not\Rightarrow$ diagonalisierbar.* Geometrisch: eine Scherung lässt nur eine Achse invariant.

**Gegenbeispiel B (Drehung — $\chi$ zerfällt nicht über $\mathbb{R}$).** $\begin{psmallmatrix}0&-1\\1&0\end{psmallmatrix}$ über $\mathbb{R}$: weder diagonalisierbar noch trigonalisierbar, da $X^2+1$ keine reelle Nullstelle hat. *Diagonalisierbarkeit/Trigonalisierbarkeit sind körperabhängig.*

**Gegenbeispiel C (geom. $<$ alg. Vielfachheit).** Jeder Jordan-Block $J^{(t)}(\lambda)$ mit $t\ge2$: alg. Vielfachheit $t$, geom. Vielfachheit $1$. Nicht diagonalisierbar — der „Prototyp" des Defekts (Kapitel 4).

---

<a id="typische-klausuraufgaben-2"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Woran erkennbar | Strategie |
|---|---|---|
| **Diagonalisieren** | „Bestimmen Sie $T,D$ mit $T^{-1}AT=D$." | $\chi$, Eigenwerte, Eigenräume, Vielfachheiten prüfen, $T$ zusammensetzen. |
| **„Ist $A$ diagonalisierbar?"** | Ja/Nein mit Begründung | $\chi$ zerfällt? geom $=$ alg? (Satz 2.9). |
| **Parameteraufgabe** | „Für welche $t$ ist $A$ diagonalisierbar?" | Fallunterscheidung nach Vielfachheit/Eigenraumdimension. |
| **Trigonalisierbarkeit** | „Zeigen Sie, dass $A$ trigonalisierbar ist." | nur prüfen, ob $\chi$ über $k$ zerfällt (Satz 2.11). |
| **Eigenwerte/-vektoren** | „Bestimmen Sie alle Eigenwerte/-vektoren." | $\chi$-Nullstellen, dann $\ker(\lambda E-A)$. |
| **Über welchem Körper?** | $\mathbb{R}$ vs. $\mathbb{C}$ | Drehungen/irreduzible Faktoren beachten. |
| **Anwendung** | „Berechnen Sie $A^{m}$ / lösen Sie $\dot x=Ax$." | diagonalisieren, koordinatenweise rechnen, zurücktransformieren. |

---

<a id="typische-fehler-2"></a>
## Typische Fehler

| Fehler | Warum falsch | Richtig |
|---|---|---|
| „$\chi$ zerfällt $\Rightarrow$ diagonalisierbar" | Scherung: $\chi=(X-1)^2$, trotzdem defekt. | Zusätzlich geom. $=$ alg. Vielfachheit prüfen. |
| algebraische und geometrische Vielfachheit verwechseln | alg. $=$ Exponent in $\chi$; geom. $=\dim\mathrm{Eig}$. | Vergleichstabelle unten beachten. |
| Eigenraum als Bild statt Kern | $\mathrm{Eig}(f,\lambda)=\ker(\lambda\,\mathrm{id}-f)$, nicht Bild. | Immer Kern von $\lambda E-A$. |
| Körper ignorieren | $X^2+1$ über $\mathbb{R}$ vs. $\mathbb{C}$. | „über welchem $k$" stets angeben. |
| Spalten von $T$ und Diagonale von $D$ nicht synchron | $D=T^{-1}AT$ verlangt Reihenfolgentreue. | $i$-te Spalte von $T$ $\leftrightarrow$ $i$-ter Diagonaleintrag von $D$. |
| Vorzeichen in $\chi$ | $\det(A-XE)=(-1)^n\det(XE-A)$. | Konvention $\chi=\det(XE-A)$ (normiert) durchhalten. |
| Nullvektor als Eigenvektor | Eigenvektoren sind $\neq0$. | $0\in\mathrm{Eig}$, aber kein Eigenvektor. |

> **Vergleichstabelle: diagonalisierbar vs. trigonalisierbar.**
>
> | | diagonalisierbar | trigonalisierbar |
> |---|---|---|
> | Normalform | Diagonalmatrix | obere Dreiecksmatrix |
> | Kriterium | $\chi$ zerfällt **und** geom $=$ alg | $\chi$ zerfällt |
> | geom. Vielfachheit | $=$ alg. (für alle $\lambda$) | beliebig $\ge1$ |
> | über $\mathbb{C}$ immer? | **nein** | **ja** |
> | geometrisch | Basis aus Eigenvektoren | Fahne invarianter Unterräume |
> | impliziert | $\Rightarrow$ trigonalisierbar | — |
>
> **Vergleichstabelle: algebraische vs. geometrische Vielfachheit.**
>
> | | algebraisch $n_\lambda$ | geometrisch $\dim\mathrm{Eig}(f,\lambda)$ |
> |---|---|---|
> | Definition | Exponent von $(X-\lambda)$ in $\chi_f$ | Dimension des Eigenraums |
> | Größe | stets $\ge$ geometrisch | stets $\le$ algebraisch, $\ge1$ |
> | diagonalisierbar $\Leftrightarrow$ | — | $=$ algebraisch für **alle** $\lambda$ |
> | Jordan-Block $J^{(t)}(\lambda)$ | $t$ | $1$ |

---

<a id="verbindungen-2"></a>
## Verbindungen

- **← Kapitel 0:** „Eigenwert $\Leftrightarrow$ Nullstelle von $\chi_f$" ist „Nullstelle $\Leftrightarrow$ Linearfaktor"; „$\chi$ zerfällt" benutzt die Faktorisierungstheorie.
- **← Kapitel 1:** Der Trigonalisierbarkeitsbeweis lebt vom Quotienten $V/U$, der induzierten Abbildung $\bar f$ und der Dimensionsformel.
- **→ Kapitel 3 (Minimalpolynom):** Liefert ein *zweites* Diagonalisierbarkeitskriterium: $f$ diagonalisierbar $\Leftrightarrow\mu_f$ zerfällt in **verschiedene** Linearfaktoren (quadratfrei). $\mu_f$ verfeinert die Information von $\chi_f$.
- **→ Kapitel 4 (Jordan):** Die JNF ist die *vollständige* Klassifikation, wenn $\chi$ zerfällt — sie misst genau, „wie weit" $f$ von diagonalisierbar entfernt ist (Größe der Jordan-Blöcke). Trigonalisierbarkeit ist die Vorstufe.
- **→ Kapitel 5 ($\mathbb{C}$):** „Über $\mathbb{C}$ zerfällt $\chi$ immer" macht jede komplexe Matrix trigonalisierbar — der Grund, warum die Jordan-Theorie über $\mathbb{C}$ universell ist.
- **→ Kapitel 8 (Spektralsatz):** Dort wird für *normale* Operatoren sogar eine **orthonormale** Eigenbasis garantiert — die „perfekte" Diagonalisierung.

**Definitionen, die später ständig gebraucht werden:** $\chi_f$, Eigenwert/-raum, algebraische/geometrische Vielfachheit, „zerfällt in Linearfaktoren", ähnlich.

---

<a id="zusammenfassung-2"></a>
## Zusammenfassung

| Kernaussage | Symbolisch |
|---|---|
| Eigenwerte $=$ Nullstellen von $\chi_f$. | $\chi_f(\lambda)=0$ |
| $\mathrm{Eig}(f,\lambda)=\ker(\lambda\,\mathrm{id}-f)$. | Eigenraum $=$ Kern |
| $1\le$ geom. $\le$ alg. Vielfachheit. | $\dim\mathrm{Eig}\le n_\lambda$ |
| Eigenvektoren zu verschiedenen $\lambda$ sind unabhängig. | Summe der Eigenräume direkt |
| **Diagonalisierbar** $\Leftrightarrow$ $\chi$ zerfällt **und** geom $=$ alg $\Leftrightarrow V=\bigoplus\mathrm{Eig}$. | (Satz 2.9) |
| **Trigonalisierbar** $\Leftrightarrow$ $\chi$ zerfällt über $k$. | (Satz 2.11) |
| Über $\mathbb{C}$: jede Matrix trigonalisierbar. | (Fundamentalsatz) |
| $\chi$ ist ähnlichkeitsinvariant. | $A\sim B\Rightarrow\chi_A=\chi_B$ |

**Die eine Idee des Kapitels:** Beide Normalformen liest man an $\chi_f$ ab. *Zerfällt $\chi$ nicht*, gibt es über $k$ keine Dreiecksform. *Zerfällt $\chi$, reicht das aber nicht für Diagonalität* — dafür müssen zusätzlich genug Eigenvektoren da sein (geom $=$ alg). Der Abstand zwischen „zerfällt" und „diagonalisierbar" ist genau das, was die Jordan-Normalform in Kapitel 4 vermisst.



---

<a id="kapitel-3-minimalpolynom-und-satz-von-cayley-hamilton"></a>
# Kapitel 3 — Minimalpolynom und Satz von Cayley-Hamilton

> **Stellung im Kurs.** Kapitel 2 hat gezeigt: $\chi_f$ entscheidet über Trigonalisierbarkeit,
> aber für Diagonalisierbarkeit braucht man eine *Zusatzbedingung* (geom $=$ alg). Dieses Kapitel
> liefert das Objekt, das diese Zusatzbedingung **in einem einzigen Polynom** kodiert: das
> **Minimalpolynom** $\mu_f$. Es ist feiner als $\chi_f$ und das letzte Werkzeug vor der
> Jordan-Normalform. Der Satz von Cayley-Hamilton ($\chi_f(f)=0$) ist der „Klebstoff", der
> $\mu_f$ an $\chi_f$ bindet.

---

<a id="motivation-3"></a>
## Motivation

Man kann in eine lineare Abbildung $f\colon V\to V$ **Polynome einsetzen**: aus $P=a_nX^n+\dots+a_0$ wird der Operator
$$
P(f)=a_n f^n+\dots+a_1 f+a_0\,\mathrm{id}_V,
$$
wobei $f^n=f\circ\dots\circ f$. Das ist kein technischer Spielerei-Trick, sondern eröffnet eine ganze Welt:

1. **Annihilatoren.** Gibt es überhaupt ein Polynom $P\neq0$ mit $P(f)=0$? Ja — und das **kleinste** solche Polynom ($\mu_f$) speichert *die gesamte Struktur* von $f$ kompakter als $\chi_f$.

2. **Diagonalisierbarkeit in einem Polynom.** Kapitel 2 brauchte zwei Bedingungen. Mit $\mu_f$ wird daraus *eine*:
   $$
   f\ \text{diagonalisierbar}\quad\Longleftrightarrow\quad \mu_f\ \text{zerfällt in }\textbf{verschiedene}\text{ Linearfaktoren}.
   $$
   „Mehrfache Faktoren in $\mu_f$" $=$ „Defekt" $=$ „nicht diagonalisierbar".

3. **Praktischer Nutzen.** Cayley-Hamilton $\chi_f(f)=0$ erlaubt es, *hohe Potenzen* $f^m$ durch niedrige auszudrücken, **Inverse** als Polynom in $A$ zu schreiben und Rekursionen zu lösen.

**Mathematische Wurzel.** Die Menge $\{P\in k[X]\mid P(f)=0\}$ ist ein **Ideal** in $k[X]$. Da $k[X]$ ein Hauptidealring ist (Kapitel 0!), wird dieses Ideal von *einem* Polynom erzeugt — genau dem Minimalpolynom. Hier zahlt sich die Teilbarkeitstheorie aus Kapitel 0 direkt aus: „Division mit Rest" liefert sofort die Eindeutigkeit von $\mu_f$.

**Historisch.** Cayley (1858) formulierte „jede Matrix erfüllt ihre eigene charakteristische Gleichung" und prüfte es für $2\times2$ und $3\times3$; Frobenius gab den allgemeinen Beweis. Der scheinbar offensichtliche „Beweis" $\chi_A(A)=\det(AE-A)=\det(0)=0$ ist **falsch** (siehe Gegenbeispiele) — ein berühmter Stolperstein.

---

<a id="intuition-3"></a>
## Intuition

**$\mu_f$ ist die „minimale Gleichung" von $f$.** Stell dir $f$ als ein Element vor, das eine algebraische Relation erfüllt — so wie $\sqrt2$ die Gleichung $x^2-2=0$ erfüllt. Das Minimalpolynom ist die *kleinste* solche Relation für $f$. Alle anderen Annihilatoren sind Vielfache davon.

**Warum $\mu_f$ feiner ist als $\chi_f$.** $\chi_f$ „zählt jeden Eigenwert mit voller algebraischer Vielfachheit". $\mu_f$ zählt jeden Eigenwert nur **so oft, wie der größte Jordan-Block es verlangt**. Beispiel:
$$
A=\mathrm{diag}(2,2,2)\ \Rightarrow\ \chi_A=(X-2)^3,\quad \mu_A=(X-2).
$$
$\chi_A$ sagt „dreifacher Eigenwert", $\mu_A$ sagt „aber völlig harmlos (diagonalisierbar)". Der **Exponent in $\mu_f$** misst die *Bösartigkeit* eines Eigenwerts.

**Cayley-Hamilton als „Selbstauslöschung".** $\chi_f(f)=0$ bedeutet: Setzt man $f$ in sein *eigenes* charakteristisches Polynom ein, kommt der Nulloperator heraus. Anschaulich (im trigonalisierbaren Fall): Die Faktoren $(f-\lambda_i\,\mathrm{id})$ schieben $V$ entlang einer Fahne schrittweise „nach unten" $U_n\to U_{n-1}\to\dots\to\{0\}$, bis nichts mehr übrig ist.

**Das Diagonalisierbarkeitskriterium anschaulich.** Ein Eigenwert $\lambda$ ist „brav" (diagonalisierbar-verträglich), wenn $(f-\lambda)$ den zugehörigen Teilraum *in einem Schritt* auslöscht — dann steht $(X-\lambda)$ **einfach** in $\mu_f$. Braucht man mehrere Schritte (Jordan-Block $>1$), erscheint $(X-\lambda)$ **mehrfach** — und $f$ ist nicht diagonalisierbar.

---

<a id="formale-definitionen-3"></a>
## Formale Definitionen

Sei $V$ endlichdim. $k$-Vektorraum, $\dim V=d$, $f\colon V\to V$ linear.

**Definition 3.1 (Einsetzen).**
Für $n\in\mathbb{N}$ sei $f^n=\underbrace{f\circ\dots\circ f}_{n}$ und $f^0=\mathrm{id}_V$. Für $P=a_nX^n+\dots+a_0\in k[X]$:
$$
P(f):=a_nf^n+a_{n-1}f^{n-1}+\dots+a_1f+a_0\,\mathrm{id}_V\ \in\ \mathrm{End}(V).
$$
Analog $P(A)$ für eine Matrix $A$.

**Definition 3.2 (Einsetzungshomomorphismus).**
Die Abbildung
$$
\psi_f\colon k[X]\to\mathrm{End}(V),\qquad P\mapsto P(f)
$$
ist ein **Ringhomomorphismus** (siehe Satz 3.4). Sein Bild ist kommutativ.

**Definition 3.3 (Minimalpolynom).**
Das **Minimalpolynom** $\mu_f$ von $f$ ist das **normierte** Polynom **minimalen Grades** $\ge1$ mit
$$
\mu_f(f)=0,
$$
unter allen $P\in k[X]\setminus\{0\}$ mit $P(f)=0$. (Existenz: Satz 3.5; Eindeutigkeit: Satz 3.7.) Analog $\mu_A$ für Matrizen.

---

<a id="eigenschaften-3"></a>
## Eigenschaften

| Eigenschaft | Aussage | Kurzbegründung |
|---|---|---|
| **$\psi_f$ Ringhom.** | $(P+Q)(f)=P(f)+Q(f)$, $(PQ)(f)=P(f)\circ Q(f)$ | Satz 3.4. |
| **Bild kommutativ** | $P(f)\circ Q(f)=Q(f)\circ P(f)$ | $(PQ)(f)=(QP)(f)$, da $k[X]$ kommutativ. |
| **Annihilator-Ideal** | $\{P\mid P(f)=0\}$ ist Ideal in $k[X]$ | Summe/Vielfache von Annihilatoren annihilieren. |
| **$\mu_f$ erzeugt** | $P(f)=0\Leftrightarrow\mu_f\mid P$ | Satz 3.8. |
| **$\mu_f\mid\chi_f$** | folgt aus Cayley-Hamilton | $\chi_f(f)=0\Rightarrow\mu_f\mid\chi_f$. |
| **gleiche Nullstellen** | NST$(\mu_f)=$ NST$(\chi_f)=$ Eigenwerte | Satz 3.10. |
| **$\deg\mu_f\le d$** | da $\mu_f\mid\chi_f$, $\deg\chi_f=d$ | Gradargument. |
| **ähnlichkeitsinvariant** | $A\sim B\Rightarrow\mu_A=\mu_B$ | $P(B)=P(TAT^{-1})=T\,P(A)\,T^{-1}$. |

---

<a id="sätze-3"></a>
## Sätze

<a id="satz-34-einsetzen-ist-ringhomomorphismus"></a>
### Satz 3.4 (Einsetzen ist Ringhomomorphismus)

**Aussage.** Für $P,Q\in k[X]$: $(P+Q)(f)=P(f)+Q(f)$ und $(P\cdot Q)(f)=P(f)\circ Q(f)$.
**Bedeutung.** Macht „mit Polynomen in $f$ rechnen" zu echtem Ringrechnen; ohne diese Verträglichkeit gäbe es keine Minimalpolynom-Theorie.
**Intuition.** Polynome multiplizieren $\leftrightarrow$ zugehörige Operatoren verketten.
**Konsequenzen.** Das Bild $k[f]=\{P(f)\}$ ist ein kommutativer Unterring von $\mathrm{End}(V)$.

<a id="satz-35-existenz-eines-annihilators"></a>
### Satz 3.5 (Existenz eines Annihilators)

**Aussage.** Es gibt ein $P\in k[X]\setminus\{0\}$ mit $P(f)=0$.
**Voraussetzungen.** $\dim V=d<\infty$.
**Bedeutung.** Sichert, dass $\mu_f$ überhaupt existiert.
**Intuition.** $\mathrm{End}(V)$ hat endliche Dimension $d^2$; die $d^2+1$ Operatoren $\mathrm{id},f,f^2,\dots,f^{d^2}$ können nicht alle unabhängig sein.

<a id="satz-36-ggt-von-annihilatoren-annihiliert"></a>
### Satz 3.6 (ggT von Annihilatoren annihiliert)

**Aussage.** Sind $P(f)=Q(f)=0$, so gilt auch $G(f)=0$ für $G=\gcd(P,Q)$.
**Bedeutung.** Schlüssel zur Eindeutigkeit des Minimalpolynoms.
**Beweisstil.** *direkt mit Bézout.*

<a id="satz-37-eindeutigkeit-von-mu_f"></a>
### Satz 3.7 (Eindeutigkeit von $\mu_f$)

**Aussage.** Das Minimalpolynom ist eindeutig bestimmt.
**Beweisidee.** Gäbe es zwei normierte Minimalpolynome $\mu_1\neq\mu_2$ minimalen Grades, so wäre $G=\gcd(\mu_1,\mu_2)$ ein Annihilator (Satz 3.6) **kleineren** Grades — Widerspruch zur Minimalität.

<a id="satz-38-teilbarkeitscharakterisierung"></a>
### Satz 3.8 (Teilbarkeitscharakterisierung)

**Aussage.** Für $P\in k[X]$ gilt $\;P(f)=0\ \Longleftrightarrow\ \mu_f\mid P.$
**Bedeutung.** $\mu_f$ ist *der* Erzeuger des Annihilator-Ideals; jeder Annihilator ist ein Vielfaches.

<a id="satz-39-cayley-hamilton-zentraler-satz"></a>
### Satz 3.9 (Cayley-Hamilton) — *zentraler Satz*

**Aussage.** $\chi_f(f)=0$. Matrixfassung: $\chi_A(A)=0$, d. h.
$$
A^n+a_{n-1}A^{n-1}+\dots+a_1A+a_0E_n=0,\qquad\text{wenn }\chi_A=X^n+a_{n-1}X^{n-1}+\dots+a_0.
$$
**Voraussetzungen.** Keine (gilt über jedem Körper, ohne dass $\chi$ zerfallen muss).
**Bedeutung.** Bindet $\mu_f$ an $\chi_f$: $\mu_f\mid\chi_f$. Erlaubt Reduktion hoher Potenzen.
**Intuition.** $f$ erfüllt seine eigene charakteristische Gleichung.
**Konsequenzen.** $\deg\mu_f\le n$; $A^{-1}$ als Polynom in $A$ (falls $a_0\neq0$); JNF-Theorie.

<a id="satz-310-mu_f-und-chi_f-haben-dieselben-nullstellen"></a>
### Satz 3.10 ($\mu_f$ und $\chi_f$ haben dieselben Nullstellen)

**Aussage.** $\lambda$ ist Eigenwert von $f$ $\Leftrightarrow\chi_f(\lambda)=0\Leftrightarrow\mu_f(\lambda)=0$.
**Bedeutung.** $\mu_f$ „sieht" alle Eigenwerte, nur mit (evtl.) kleineren Vielfachheiten.

<a id="satz-311-gestalt-von-mu_f-bei-zerfallendem-chi_f"></a>
### Satz 3.11 (Gestalt von $\mu_f$ bei zerfallendem $\chi_f$)

**Aussage.** Zerfällt $\chi_f=(X-\lambda_1)^{n_1}\cdots(X-\lambda_r)^{n_r}$ ($\lambda_i$ verschieden), so
$$
\mu_f=(X-\lambda_1)^{m_1}\cdots(X-\lambda_r)^{m_r}\qquad\text{mit}\quad 1\le m_i\le n_i.
$$
**Bedeutung.** Jeder Eigenwert kommt in $\mu_f$ vor (Exponent $\ge1$), aber höchstens mit seiner algebraischen Vielfachheit. $m_i=$ Größe des **größten** Jordan-Blocks zu $\lambda_i$ (Kapitel 4).

<a id="satz-312-diagonalisierbarkeitskriterium-via-mu_f-hauptanwendung"></a>
### Satz 3.12 (Diagonalisierbarkeitskriterium via $\mu_f$) — *Hauptanwendung*

**Aussage.** $f$ ist diagonalisierbar $\;\Longleftrightarrow\;\mu_f$ zerfällt in **paarweise verschiedene** Linearfaktoren:
$$
\mu_f=(X-\lambda_1)(X-\lambda_2)\cdots(X-\lambda_r),\qquad\lambda_i\ \text{verschieden}.
$$
(Äquivalent: $\mu_f$ ist **quadratfrei** und zerfällt über $k$.)
**Bedeutung.** Diagonalisierbarkeit in **einer** Bedingung an **ein** Polynom — oft viel schneller als Eigenräume zu vergleichen.
**Intuition.** „Alle Jordan-Blöcke haben Größe $1$" $\Leftrightarrow$ alle $m_i=1$ $\Leftrightarrow$ $\mu_f$ quadratfrei.

---

<a id="beweise-3"></a>
## Beweise

> **Klausurrelevant in voller Tiefe:** Satz 3.4(ii), 3.5, 3.8, **Cayley-Hamilton 3.9** und Satz 3.12.

<a id="beweis-von-satz-34ii-multiplikativität-beweisstil-direkt-doppelsumme"></a>
### Beweis von Satz 3.4(ii) (Multiplikativität) — *Beweisstil: direkt, Doppelsumme*

Sei $P=\sum_i a_iX^i$, $Q=\sum_j b_jX^j$, also $PQ=\sum_\ell c_\ell X^\ell$ mit $c_\ell=\sum_{i+j=\ell}a_ib_j$. Da $f^i\circ f^j=f^{i+j}$ und Operatoren in $f$ kommutieren:
$$
P(f)\circ Q(f)=\Big(\sum_i a_if^i\Big)\circ\Big(\sum_j b_jf^j\Big)
=\sum_i\sum_j a_ib_j\,f^{i+j}
=\sum_\ell\Big(\sum_{i+j=\ell}a_ib_j\Big)f^\ell
=\sum_\ell c_\ell f^\ell=(PQ)(f).\ \blacksquare
$$

<a id="beweis-von-satz-35-existenz-beweisstil-dimensionsargument"></a>
### Beweis von Satz 3.5 (Existenz) — *Beweisstil: Dimensionsargument*

$\mathrm{End}(V)=\mathrm{Hom}(V,V)$ hat Dimension $d^2$ (Basis $E_{ij}$). Die $d^2+1$ Elemente
$$
\mathrm{id}=f^0,\ f,\ f^2,\ \dots,\ f^{d^2}
$$
liegen in einem $d^2$-dimensionalen Raum, sind also **linear abhängig**: es gibt $a_0,\dots,a_{d^2}\in k$, nicht alle $0$, mit $\sum_{i=0}^{d^2}a_if^i=0$. Das Polynom $P=\sum a_iX^i\neq0$ erfüllt $P(f)=0$. $\blacksquare$

<a id="beweis-von-satz-36-ggt-annihiliert-beweisstil-direkt-mit-bézout"></a>
### Beweis von Satz 3.6 (ggT annihiliert) — *Beweisstil: direkt mit Bézout*

Nach Kapitel 0 gibt es $A,B\in k[X]$ mit $G=\gcd(P,Q)=A\,P+B\,Q$. Einsetzen (Satz 3.4):
$$
G(f)=A(f)\circ P(f)+B(f)\circ Q(f)=A(f)\circ 0+B(f)\circ 0=0.\ \blacksquare
$$

<a id="beweis-von-satz-38-teilbarkeit-beweisstil-division-mit-rest"></a>
### Beweis von Satz 3.8 (Teilbarkeit) — *Beweisstil: Division mit Rest*

„$\Leftarrow$": Ist $P=A\,\mu_f$, so $P(f)=A(f)\circ\mu_f(f)=A(f)\circ0=0$.
„$\Rightarrow$": Division mit Rest: $P=A\,\mu_f+R$ mit $\deg R<\deg\mu_f$. Dann
$$
0=P(f)=\underbrace{A(f)\circ\mu_f(f)}_{=0}+R(f)=R(f).
$$
Wäre $R\neq0$, hätte man einen Annihilator $R$ kleineren Grades als $\mu_f$ — Widerspruch zur Minimalität. Also $R=0$, d. h. $\mu_f\mid P$. $\blacksquare$

<a id="beweis-von-satz-39-cayley-hamilton-zwei-wege"></a>
### Beweis von Satz 3.9 (Cayley-Hamilton) — *zwei Wege*

> **Strategie.** Wir beweisen es zuerst für den Fall, dass $\chi_f$ **zerfällt** (dann ist $f$ trigonalisierbar, Kap. 2), und reduzieren den allgemeinen Fall per **Körpererweiterung** darauf. Das ist der saubere Standardweg.

**Schritt 1 — zerfallender Fall.** *(Beweisstil: Fahnenargument.)*
Da $\chi_f$ zerfällt, ist $f$ trigonalisierbar: es gibt eine Basis $e_1,\dots,e_n$ mit oberer Dreiecksmatrix, Diagonale $\lambda_1,\dots,\lambda_n$ (also $\chi_f=\prod_i(X-\lambda_i)$). Setze die **Fahne**
$$
U_i=\mathrm{span}(e_1,\dots,e_i),\qquad U_0=\{0\}\subseteq U_1\subseteq\dots\subseteq U_n=V.
$$
Da die Matrix obere Dreiecksgestalt hat, gilt $f(e_i)\in U_i$ und genauer
$$
(f-\lambda_i\,\mathrm{id})(U_i)\subseteq U_{i-1}\qquad(i=1,\dots,n).
$$
*(Denn $(f-\lambda_i)(e_i)=$ Linearkombination von $e_1,\dots,e_{i-1}\in U_{i-1}$, und für $j<i$ ist $(f-\lambda_i)(e_j)\in U_j\subseteq U_{i-1}$.)*
Die Faktoren $(f-\lambda_i\,\mathrm{id})$ **kommutieren** (Polynome in $f$). Wende sie der Reihe nach an:
$$
\chi_f(f)\,V=(f-\lambda_1)\cdots(f-\lambda_n)\,V
\ \subseteq\ (f-\lambda_1)\cdots(f-\lambda_{n-1})\,U_{n-1}\ \subseteq\ \dots\ \subseteq\ (f-\lambda_1)U_1\ \subseteq\ U_0=\{0\}.
$$
Also $\chi_f(f)=0$.

**Schritt 2 — allgemeiner Körper.** *(Beweisstil: Reduktion via Erweiterungskörper.)*
Sei $k$ beliebig. Es gibt einen Erweiterungskörper $L\supseteq k$, über dem $\chi_A$ in Linearfaktoren zerfällt (z. B. einen Zerfällungskörper; existiert nach der Konstruktion $k[X]/(P)$ aus Kapitel 0/1, iteriert). Betrachte $A$ als Matrix in $L^{n\times n}$. Das charakteristische Polynom $\chi_A$ und der Ausdruck $\chi_A(A)$ haben **dieselben Einträge**, ob man sie über $k$ oder über $L$ bildet. Nach Schritt 1 gilt $\chi_A(A)=0$ über $L$, also auch über $k$. $\blacksquare$

> **Alternative (klassischer Adjunkten-Beweis, nur Idee).** Mit der Adjunkten gilt die Polynom-Matrix-Identität $(XE-A)\cdot\mathrm{adj}(XE-A)=\chi_A(X)\cdot E$ in $(k[X])^{n\times n}$. Koeffizientenvergleich nach Potenzen von $X$ und geschicktes Aufsummieren liefert $\chi_A(A)=0$. **Vorsicht:** Man darf *nicht* einfach „$X:=A$" in $\det(XE-A)$ einsetzen — siehe Gegenbeispiele.

<a id="beweis-von-satz-311-beweisstil-direkt"></a>
### Beweis von Satz 3.11 — *Beweisstil: direkt*

$\mu_f\mid\chi_f$ (Cayley-Hamilton $+$ Satz 3.8), also ist $\mu_f$ ein Produkt der Faktoren $(X-\lambda_i)$ mit Exponenten $m_i\le n_i$. Jedes $\lambda_i$ ist Eigenwert, also Nullstelle von $\mu_f$ (Satz 3.10), folglich $m_i\ge1$. $\blacksquare$

<a id="beweis-von-satz-312-diagonalisierbarkeit-via-mu_f-beweisstil-zwei-richtungen"></a>
### Beweis von Satz 3.12 (Diagonalisierbarkeit via $\mu_f$) — *Beweisstil: zwei Richtungen*

**„$\Rightarrow$".** Sei $f$ diagonalisierbar mit verschiedenen Eigenwerten $\lambda_1,\dots,\lambda_r$. Setze $P=\prod_{j=1}^r(X-\lambda_j)$. In einer Eigenbasis wirkt $P(f)$ auf einem Eigenvektor $v$ zum Eigenwert $\lambda_i$ als
$$
P(f)v=\prod_j(f-\lambda_j)v=\prod_j(\lambda_i-\lambda_j)\,v=0,
$$
denn der Faktor $j=i$ verschwindet. Da Eigenvektoren $V$ aufspannen, ist $P(f)=0$, also $\mu_f\mid P$. Somit ist $\mu_f$ ein Produkt verschiedener Linearfaktoren (quadratfrei).

**„$\Leftarrow$".** Sei $\mu_f=\prod_{j=1}^r(X-\lambda_j)$ mit verschiedenen $\lambda_j$. Die Faktoren $Q_j=\prod_{i\neq j}(X-\lambda_i)$ haben $\gcd(Q_1,\dots,Q_r)=1$, also gibt es (Bézout, Kapitel 0) $A_j\in k[X]$ mit $\sum_j A_jQ_j=1$. Einsetzen:
$$
\mathrm{id}_V=\sum_{j=1}^r A_j(f)\,Q_j(f).
$$
Für jeden Vektor $v$ liegt $A_j(f)Q_j(f)\,v$ in $\mathrm{Eig}(f,\lambda_j)$: denn $(f-\lambda_j)\,Q_j(f)=\mu_f(f)=0$, also $(f-\lambda_j)\big(A_j(f)Q_j(f)v\big)=0$. Damit ist jedes $v$ Summe von Eigenvektoren, $V=\sum_j\mathrm{Eig}(f,\lambda_j)$; die Summe ist direkt (Lemma 2.11′), also $V=\bigoplus_j\mathrm{Eig}(f,\lambda_j)$ — $f$ ist diagonalisierbar (Satz 2.9). $\blacksquare$

> **Bemerkung.** Die „$\Leftarrow$"-Richtung ist der **Spezialfall $m_j=1$** der Hauptraumzerlegung aus Kapitel 4. Die Bézout-Partition der Eins ist genau die Technik, die dort die volle JNF trägt.

---

<a id="algorithmen-3"></a>
## Algorithmen

<a id="algorithmus-a-minimalpolynom-über-teiler-von-chi_f"></a>
### Algorithmus A — Minimalpolynom über Teiler von $\chi_f$

- **Motivation.** „Bestimmen Sie $\mu_A$" ist Standardaufgabe; meist ist $\chi_A$ schon bekannt.
- **Idee.** $\mu_f\mid\chi_f$ und $\mu_f$ hat **dieselben Nullstellen** wie $\chi_f$. Also $\mu_f=\prod_i(X-\lambda_i)^{m_i}$ mit $1\le m_i\le n_i$; teste aufsteigende Exponenten.
- **Voraussetzungen.** $\chi_A$ zerfällt (sonst Faktorisierung über $k$ nutzen).
- **Pseudocode.**
  ```
  Eingabe: A, χ_A = ∏ (X−λ_i)^{n_i}
  für jeden Eigenwert λ_i:
      m_i ← kleinstes m ≥ 1 mit (A − λ_i E)^m · [Rest] = 0
              # konkret: kleinstes m mit  rank((A−λ_iE)^m) stabilisiert
  μ_A ← ∏ (X − λ_i)^{m_i}
  Prüfe: μ_A(A) = 0     # zur Sicherheit
  ```
- **Mathematische Beschreibung.** $m_i$ = Größe des größten Jordan-Blocks zu $\lambda_i$ = kleinstes $m$ mit $\ker((A-\lambda_iE)^m)=\ker((A-\lambda_iE)^{m+1})$.
- **Laufzeit.** $O(n^3)$ pro getestetem Exponenten (Matrixpotenz + Rang); insgesamt $O(n^4)$ grob.
- **Speicherbedarf.** $O(n^2)$.
- **Korrektheitsidee.** Satz 3.8/3.11; die Kernkette stabilisiert genau bei der maximalen Blockgröße.
- **Anwendungen.** Diagonalisierbarkeitstest (Satz 3.12); JNF-Vorbereitung.
- **Typische Fehler.** $m_i$ zu klein wählen (nicht $\mu_A(A)=0$ prüfen); $\mu$ nicht normiert lassen.

<a id="algorithmus-b-minimalpolynom-über-lineare-abhängigkeit"></a>
### Algorithmus B — Minimalpolynom über lineare Abhängigkeit

- **Motivation.** Funktioniert ohne $\chi_A$ und ohne Eigenwerte zu kennen.
- **Idee.** Finde das kleinste $m$, für das $\mathrm{id},A,A^2,\dots,A^m$ linear abhängig sind; die Abhängigkeit *ist* $\mu_A$.
- **Pseudocode.**
  ```
  Eingabe: A
  Liste ← [vec(E), vec(A), vec(A^2), ...]   # Matrizen als Vektoren in k^{n²}
  m ← kleinstes m, für das vec(A^m) ∈ span(vec(E),…,vec(A^{m−1}))
  schreibe  A^m = −(a_{m−1}A^{m−1}+…+a_0E)
  μ_A ← X^m + a_{m−1}X^{m−1} + … + a_0
  ```
- **Laufzeit.** $O(n^4)$ (Gauß im $n^2$-dim. Raum). **Speicher.** $O(n^2\cdot m)$.
- **Korrektheitsidee.** Erste lineare Abhängigkeit liefert das normierte Polynom minimalen Grades — per Definition $\mu_A$.
- **Typische Fehler.** Matrizen falsch „vektorisieren"; Abbruch zu früh.

> **Vergleich A vs. B.** A ist schneller, *braucht aber die Eigenwerte/Faktorisierung* von $\chi_A$. B ist robust und faktorisierungsfrei, aber rechenintensiver. In Klausuren mit kleinem $n$: A nach Bestimmung von $\chi_A$.

---

<a id="beispiele-3"></a>
## Beispiele

**Beispiel 1 (leicht — $\mu\neq\chi$).** $A=\mathrm{diag}(2,2,5)$. $\chi_A=(X-2)^2(X-5)$, aber $A$ diagonal $\Rightarrow$ $\mu_A=(X-2)(X-5)$ (quadratfrei). Probe: $(A-2E)(A-5E)=0$. ✓

**Beispiel 2 (leicht — Jordan-Block).** $A=\begin{psmallmatrix}3&1\\0&3\end{psmallmatrix}$. $\chi_A=(X-3)^2$. $(A-3E)=\begin{psmallmatrix}0&1\\0&0\end{psmallmatrix}\neq0$, $(A-3E)^2=0$. Also $\mu_A=(X-3)^2=\chi_A$. **Nicht** diagonalisierbar (Satz 3.12: $\mu$ nicht quadratfrei).

**Beispiel 3 (mittel — Diagonalisierbarkeit per $\mu$).** $A=\begin{psmallmatrix}1&0&0\\0&1&0\\0&0&2\end{psmallmatrix}$ ist diagonal $\Rightarrow\mu_A=(X-1)(X-2)$, quadratfrei $\Rightarrow$ diagonalisierbar (klar). Aber das Kriterium spart Eigenraumrechnung.

**Beispiel 4 (mittel — Cayley-Hamilton zum Invertieren).** $A=\begin{psmallmatrix}1&2\\3&4\end{psmallmatrix}$, $\chi_A=X^2-5X-2$. CH: $A^2-5A-2E=0\Rightarrow A^2=5A+2E$. Außerdem $A(A-5E)=2E\Rightarrow A^{-1}=\tfrac12(A-5E)=\tfrac12\begin{psmallmatrix}-4&2\\3&-1\end{psmallmatrix}$.

**Beispiel 5 (mittel — hohe Potenz reduzieren).** Mit $A^2=5A+2E$ (Beispiel 4): $A^3=A\cdot A^2=5A^2+2A=5(5A+2E)+2A=27A+10E$. Jede Potenz $A^m$ wird zu $\alpha A+\beta E$.

**Beispiel 6 (schwer — $\mu$ bei mehreren Blöcken).**
$A=\begin{psmallmatrix}2&1&0&0\\0&2&0&0\\0&0&2&0\\0&0&0&5\end{psmallmatrix}$ (Jordan-Blöcke: $J^{(2)}(2),J^{(1)}(2),J^{(1)}(5)$). $\chi_A=(X-2)^3(X-5)$. Größter Block zu $2$ hat Größe $2$, zu $5$ Größe $1$, also $\mu_A=(X-2)^2(X-5)$. Quadratfrei? Nein $\Rightarrow$ nicht diagonalisierbar.

---

<a id="gegenbeispiele-3"></a>
## Gegenbeispiele

**Gegenbeispiel A (der berühmte Fehl-„Beweis" von Cayley-Hamilton).**
„$\chi_A(A)=\det(A\cdot E-A)=\det(0)=0$." **Falsch.** Grund: $\chi_A(X)=\det(XE-A)$ ist eine **Determinante mit der Variablen $X$ in der Diagonale** — ein Skalar-Polynom. Es in $A$ einzusetzen heißt, das *Polynom* $\chi_A$ auf den Operator $A$ anzuwenden ($A^n+a_{n-1}A^{n-1}+\dots$), **nicht** „$X$ durch $A$ in $\det(XE-A)$ ersetzen". Letzteres ergäbe $\det(AE-A)=\det(0)=0$ als Skalar $0$, was die Matrixgleichung $\chi_A(A)=0$ gar nicht trifft. (Die naive Substitution mischt „Skalar einsetzen" und „Matrix einsetzen".)

**Gegenbeispiel B ($\mu_f=\chi_f$ ist nicht immer).** $A=\mathrm{diag}(2,2,2)$: $\chi=(X-2)^3$, $\mu=(X-2)$. *$\mu$ kann echt kleineren Grad haben.* (Gleichheit $\mu=\chi$ gilt genau, wenn zu **jedem** Eigenwert nur **ein** Jordan-Block existiert.)

**Gegenbeispiel C (Quadratfreiheit nötig).** $A=\begin{psmallmatrix}1&1\\0&1\end{psmallmatrix}$: $\mu_A=(X-1)^2$ nicht quadratfrei $\Rightarrow$ nicht diagonalisierbar — obwohl $\chi$ zerfällt und nur *ein* Eigenwert da ist.

**Gegenbeispiel D ($\mu$ zerfällt nicht über $k$).** $A=\begin{psmallmatrix}0&-1\\1&0\end{psmallmatrix}$ über $\mathbb{R}$: $\mu_A=X^2+1$ irreduzibel $\Rightarrow$ kein Linearfaktor $\Rightarrow$ nicht diagonalisierbar (über $\mathbb{R}$). Über $\mathbb{C}$: $\mu=(X-i)(X+i)$ quadratfrei $\Rightarrow$ diagonalisierbar.

---

<a id="typische-klausuraufgaben-3"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Woran erkennbar | Strategie |
|---|---|---|
| **$\mu_A$ bestimmen** | „Berechnen Sie das Minimalpolynom." | $\chi_A$ faktorisieren, Exponenten $m_i$ über Kernketten testen (Alg. A). |
| **Diagonalisierbar via $\mu$** | „Entscheiden Sie mit dem Minimalpolynom." | $\mu_A$ quadratfrei $\Leftrightarrow$ diagonalisierbar (Satz 3.12). |
| **Cayley-Hamilton anwenden** | „Drücken Sie $A^{-1}$/$A^m$ durch niedrige Potenzen aus." | $\chi_A(A)=0$ umstellen; iterativ reduzieren. |
| **$\mu\mid\chi$, gleiche NST** | „Zeigen Sie …" | Satz 3.8/3.10 anwenden. |
| **CH beweisen** | „Beweisen Sie Cayley-Hamilton (zerfallender Fall)." | Fahnenargument (Schritt 1). |
| **Gestalt von $\mu$** | „Welche Form hat $\mu_A$?" | $\prod(X-\lambda_i)^{m_i}$, $m_i=$ größter Block. |

---

<a id="typische-fehler-3"></a>
## Typische Fehler

| Fehler | Warum falsch | Richtig |
|---|---|---|
| Fehl-„Beweis" $\det(AE-A)=0$ | mischt Skalar- und Matrix-Einsetzung (Gegenbeispiel A). | $\chi_A(A)=A^n+\dots+a_0E$, *Polynom* in $A$. |
| „$\mu_f=\chi_f$ immer" | bei mehreren/kleinen Blöcken echt kleiner. | $\mu_f\mid\chi_f$, Exponenten $=$ größte Blockgröße. |
| $\mu$ nicht normiert | Minimalpolynom ist per Definition normiert. | Leitkoeffizient auf $1$ skalieren. |
| Teilbarkeitsrichtung verwechselt | $P(f)=0\Rightarrow\mu_f\mid P$ (nicht $P\mid\mu_f$). | $\mu_f$ teilt jeden Annihilator. |
| Diagonalisierbarkeit ohne Quadratfreiheit | $\mu$ muss verschiedene Linearfaktoren haben. | quadratfrei **und** zerfällt über $k$. |
| Eigenwerte in $\mu$ vergessen | jeder Eigenwert ist NST von $\mu$ ($m_i\ge1$). | NST$(\mu)=$ NST$(\chi)$. |

> **Vergleichstabelle: $\chi_f$ vs. $\mu_f$.**
>
> | | $\chi_f$ | $\mu_f$ |
> |---|---|---|
> | Definition | $\det(X\,\mathrm{id}-f)$ | normierter Annihilator min. Grades |
> | Grad | genau $n=\dim V$ | $\le n$, oft kleiner |
> | Exponent von $(X-\lambda)$ | alg. Vielfachheit $n_\lambda$ | Größe des **größten** Jordan-Blocks $m_\lambda$ |
> | Nullstellen | Eigenwerte | dieselben Eigenwerte |
> | Diagonalisierbar $\Leftrightarrow$ | (zerfällt $+$ geom $=$ alg) | $\mu_f$ **quadratfrei** $+$ zerfällt |
> | Teilbarkeit | $\mu_f\mid\chi_f$ | teilt jeden Annihilator |
> | Selbstauslöschung | $\chi_f(f)=0$ (Cayley-Hamilton) | $\mu_f(f)=0$ (per Definition) |

---

<a id="verbindungen-3"></a>
## Verbindungen

- **← Kapitel 0:** Annihilator-Ideal $+$ Hauptidealring $\Rightarrow$ Eindeutigkeit von $\mu_f$; Bézout trägt Satz 3.6 und 3.12.
- **← Kapitel 1:** Körpererweiterung im CH-Beweis nutzt die Quotientenkonstruktion ($k[X]/(P)$) zur Erzeugung von Zerfällungskörpern.
- **← Kapitel 2:** $\mu_f$ verfeinert das Diagonalisierbarkeitskriterium; $\mu_f(\lambda)=0\Leftrightarrow\lambda$ Eigenwert.
- **→ Kapitel 4 (Jordan):** Der Exponent $m_i$ in $\mu_f$ ist die Größe des größten Jordan-Blocks zu $\lambda_i$; die Bézout-Partition aus Satz 3.12 ist die Keimzelle der Hauptraumzerlegung $V=\bigoplus\mathrm{Haupt}(f,\lambda_j)$.
- **→ Kapitel 8:** Normale Operatoren sind genau dann diagonalisierbar (sogar orthonormal), wenn $\mu_f$ quadratfrei über $\mathbb{C}$ — für normale Operatoren ist das automatisch.

**Definitionen, die später ständig gebraucht werden:** $P(f)$, $\mu_f$, $\mu_f\mid\chi_f$, „$\mu_f$ quadratfrei", Bézout-Partition der Eins.

---

<a id="zusammenfassung-3"></a>
## Zusammenfassung

| Kernaussage | Symbolisch |
|---|---|
| Einsetzen ist Ringhomomorphismus. | $(PQ)(f)=P(f)\circ Q(f)$ |
| Es gibt Annihilatoren ($\dim\mathrm{End}(V)=d^2$). | $\exists P\neq0:\ P(f)=0$ |
| $\mu_f$ existiert, ist eindeutig, normiert, minimal. | (Satz 3.5/3.7) |
| $\mu_f$ erzeugt das Annihilator-Ideal. | $P(f)=0\Leftrightarrow\mu_f\mid P$ |
| **Cayley-Hamilton:** $f$ erfüllt $\chi_f$. | $\chi_f(f)=0$ |
| Daraus $\mu_f\mid\chi_f$, gleiche Nullstellen. | $\mu_f\mid\chi_f$ |
| Bei zerfallendem $\chi$: $\mu_f=\prod(X-\lambda_i)^{m_i}$, $1\le m_i\le n_i$. | (Satz 3.11) |
| **Diagonalisierbar** $\Leftrightarrow$ $\mu_f$ quadratfrei (und zerfällt). | (Satz 3.12) |

**Die eine Idee des Kapitels:** $\chi_f$ kennt die Eigenwerte *mit voller Vielfachheit*; $\mu_f$ kennt sie *mit der minimal nötigen Vielfachheit* (Größe des größten Jordan-Blocks). Cayley-Hamilton verklammert beide ($\mu_f\mid\chi_f$). Die **Quadratfreiheit von $\mu_f$** ist das schärfste, kompakteste Diagonalisierbarkeitskriterium — und der direkte Vorbote der Jordan-Normalform.



---

<a id="kapitel-4-haupträume-und-jordan-normalform"></a>
# Kapitel 4 — Haupträume und Jordan-Normalform

> **Stellung im Kurs.** Dies ist der Höhepunkt von Teil I und der schwierigste Stoff der ersten
> Kurshälfte. Kapitel 2 lieferte „diagonal oder dreieckig", Kapitel 3 das Minimalpolynom als
> Diagonalisierbarkeits-Detektor. Jetzt kommt die **vollständige Klassifikation**: Wenn $\chi_f$
> zerfällt, gibt es *immer* eine Basis, in der die Matrix in **Jordan-Normalform** ist — die
> „bestmögliche" Form, wenn Diagonalität scheitert. Sie misst exakt, *wie weit* $f$ von
> diagonalisierbar entfernt ist.

---

<a id="motivation-4"></a>
## Motivation

Nicht jede Matrix ist diagonalisierbar (Scherungen, defekte Eigenwerte). Aber man möchte trotzdem eine **Normalform**: eine Standardgestalt, sodass

- man $A^m$, $e^{tA}$ usw. *trotzdem* leicht berechnen kann,
- zwei Matrizen genau dann „gleich" (ähnlich) sind, wenn ihre Normalformen übereinstimmen,
- man die gesamte Struktur von $f$ aus wenigen Zahlen abliest.

Die **Jordan-Normalform** (JNF) leistet genau das. Sie ist „Diagonalmatrix plus minimal nötige Nebendiagonal-Einsen":
$$
J=\begin{pmatrix}J_1 & & 0\\ & \ddots & \\ 0 & & J_c\end{pmatrix},\qquad
J^{(t)}(\lambda)=\begin{pmatrix}\lambda&1&&0\\&\lambda&\ddots&\\&&\ddots&1\\0&&&\lambda\end{pmatrix}.
$$
Die Diagonale trägt die Eigenwerte, die **Einsen auf der oberen Nebendiagonale** kodieren den „Defekt".

**Das Grundproblem und seine Lösung.** Warum scheitert Diagonalisierung? Weil es zu wenige Eigenvektoren gibt. Die Idee: Wenn man Eigenvektoren ($\ker(f-\lambda)$) nicht in ausreichender Zahl hat, nimmt man **verallgemeinerte Eigenvektoren** dazu — Vektoren, die *irgendwann* von einer Potenz $(f-\lambda)^\ell$ ausgelöscht werden. Diese füllen den **Hauptraum** $\mathrm{Haupt}(f,\lambda)$. Der zentrale Strukturplan:

$$
\boxed{\;V=\bigoplus_j\mathrm{Haupt}(f,\lambda_j)\;}\quad\text{und auf jedem Hauptraum ist }(f-\lambda_j)\text{ \textbf{nilpotent}.}
$$

Damit zerfällt das schwere Problem in zwei leichte: (1) **Hauptraumzerlegung** (Bézout, Kapitel 3) und (2) **Normalform nilpotenter Abbildungen** (Kernketten). Die JNF entsteht durch Zusammensetzen.

**Mathematische/historische Wurzel.** Camille Jordan (1870) klassifizierte lineare Abbildungen über $\mathbb{C}$. Die JNF ist die *vollständige* Lösung des Ähnlichkeitsproblems über algebraisch abgeschlossenen Körpern — das „Endspiel" der Eigenwerttheorie.

---

<a id="intuition-4"></a>
## Intuition

**Verallgemeinerte Eigenvektoren = „Eigenvektoren mit Verzögerung".** Ein echter Eigenvektor erfüllt $(f-\lambda)v=0$ *sofort*. Ein verallgemeinerter Eigenvektor erfüllt $(f-\lambda)^\ell v=0$ erst nach $\ell$ Anwendungen. Bild: $(f-\lambda)$ ist eine „Abwärtstreppe":
$$
v_t\ \xrightarrow{f-\lambda}\ v_{t-1}\ \xrightarrow{f-\lambda}\ \dots\ \xrightarrow{f-\lambda}\ v_1\ \xrightarrow{f-\lambda}\ 0.
$$
Eine solche **Jordan-Kette** der Länge $t$ ist genau *ein* Jordan-Block $J^{(t)}(\lambda)$. Der unterste Vektor $v_1$ ist ein echter Eigenvektor; die darüber sind „verzögerte" Eigenvektoren.

**Die JNF als „Würfelturm".** Stell dir zu jedem Eigenwert $\lambda$ Stapel von Würfeln vor (ein Stapel $=$ ein Jordan-Block, Höhe $=$ Blockgröße). Die Anzahl der Stapel $=$ Zahl der echten Eigenvektoren ($=\dim\mathrm{Eig}$). Die Gesamtzahl der Würfel $=$ algebraische Vielfachheit ($=\dim\mathrm{Haupt}$). Die Höhe des höchsten Stapels $=$ Exponent in $\mu_f$. Aus diesen „Profildaten" liest man die ganze JNF ab.

```
   Eigenwert λ, alg. Vielfachheit 4:           Kernketten-Profil:
   ▢          ▢                                d_1 = #Stapel        = 2
   ▢                                           d_2 = d_1 + #(Höhe≥2)= 3
   ▢                                           d_3 = ... = 4 = n_λ
   ──────────                                  ⇒ Blöcke: Größen 3 und 1
   Stapel 1   Stapel 2
   (Höhe 3)   (Höhe 1)
```

**Warum „nilpotent" das Wesentliche ist.** Auf $\mathrm{Haupt}(f,\lambda)$ ist $(f-\lambda)$ nilpotent — es „schiebt alles schrittweise nach $0$". Die ganze Schwierigkeit der JNF steckt im nilpotenten Fall; der Rest ist „$+\lambda\,\mathrm{id}$".

---

<a id="formale-definitionen-4"></a>
## Formale Definitionen

Sei $V$ endlichdim. über $k$, $f\colon V\to V$ linear, $g\in\mathrm{End}(V)$.

**Definition 4.1 (nilpotent).**
$g$ heißt **nilpotent**, wenn $g^N=0$ für ein $N\in\mathbb{N}$. Das kleinste solche $N$ heißt **Nilpotenzindex**.

**Definition 4.2 (Hauptraum / verallgemeinerter Eigenraum).**
Für einen Eigenwert $\lambda$ von $f$:
$$
\mathrm{Haupt}(f,\lambda):=\{v\in V\mid \exists\,\ell\in\mathbb{N}:\ (f-\lambda\,\mathrm{id})^\ell v=0\}=\bigcup_{\ell\ge1}\ker\big((f-\lambda\,\mathrm{id})^\ell\big).
$$
Elemente $\neq0$ heißen **verallgemeinerte Eigenvektoren**.

**Definition 4.3 (direkte Summe).**
Unterräume $U_1,\dots,U_k\subseteq V$ bilden eine **direkte Summe** $V=\bigoplus_{j}U_j$, wenn $V=U_1+\dots+U_k$ und für alle $u_j\in U_j$ mit $u_1+\dots+u_k=0$ folgt $u_1=\dots=u_k=0$. Äquivalent: $U_i\cap(U_1+\dots+\widehat{U_i}+\dots+U_k)=\{0\}$. Sind $B_j$ Basen der $U_j$, so ist $B_1\cup\dots\cup B_k$ eine Basis von $V$.

**Definition 4.4 (Jordan-Block).**
Für $t\ge1$, $\lambda\in k$:
$$
J^{(t)}(\lambda)=\begin{pmatrix}\lambda&1&&0\\&\lambda&\ddots&\\&&\ddots&1\\0&&&\lambda\end{pmatrix}\in k^{t\times t},\qquad
\big(J^{(t)}(\lambda)\big)_{ij}=\begin{cases}\lambda,&i=j\\ 1,&i+1=j\\ 0,&\text{sonst.}\end{cases}
$$

**Definition 4.5 (Jordan-Normalform).**
Eine Matrix ist in **Jordan-Normalform**, wenn sie blockdiagonal aus Jordan-Blöcken $J^{(t)}(\lambda)$ besteht. Eine lineare Abbildung $f$ „besitzt eine JNF", wenn es eine Basis (**Jordan-Basis**) gibt, bzgl. der die Matrix in JNF ist.

**Definition 4.6 (ähnlich, Wiederholung).**
$A\sim B :\Leftrightarrow \exists T$ invertierbar mit $B=TAT^{-1}$. Genau dann stellen $A,B$ dieselbe Abbildung in verschiedenen Basen dar.

---

<a id="eigenschaften-4"></a>
## Eigenschaften

| Eigenschaft | Aussage | Kurzbegründung |
|---|---|---|
| **Kernkette wächst** | $\ker(g)\subseteq\ker(g^2)\subseteq\dots$ | $g^k v=0\Rightarrow g^{k+1}v=0$. |
| **Kernkette stabilisiert** | $\ker(g^m)=\ker(g^{m+1})\Rightarrow\ker(g^m)=\ker(g^{m+j})\ \forall j$ | Lemma 4.8; spätestens bei $m=\dim V$. |
| **$\mathrm{Eig}\subseteq\mathrm{Haupt}$** | $\ker(f-\lambda)\subseteq\mathrm{Haupt}(f,\lambda)$ | $\ell=1$. |
| **$\mathrm{Haupt}$ $f$-invariant** | $f(\mathrm{Haupt}(f,\lambda))\subseteq\mathrm{Haupt}(f,\lambda)$ | $f$ vertauscht mit $(f-\lambda)^\ell$. |
| **$(f-\lambda)$ nilpotent auf $\mathrm{Haupt}$** | $(f-\lambda)^{n_\lambda}|_{\mathrm{Haupt}}=0$ | Definition $+$ Stabilisierung. |
| **$\dim\mathrm{Haupt}=n_\lambda$** | gleich algebraischer Vielfachheit | Hauptraumzerlegung $+$ $\chi$. |
| **JNF: Diagonale $=$ Eigenwerte** | $\chi_J=\prod_\text{Blöcke}(X-\lambda)^{t}$ | Dreiecksdeterminante. |
| **$J^{(t)}(\lambda)$: geom. Vielfachheit $1$** | nur ein Eigenvektor pro Block | $\ker(J-\lambda E)$ eindim. |

---

<a id="sätze-4"></a>
## Sätze

<a id="lemma-48-stabilisierung-der-kernkette"></a>
### Lemma 4.8 (Stabilisierung der Kernkette)

**Aussage.** Für $g\in\mathrm{End}(V)$ gilt: ist $\ker(g^m)=\ker(g^{m+1})$, so $\ker(g^m)=\ker(g^{m+j})$ für alle $j\ge0$. Die Kette stabilisiert spätestens bei $m=\dim V$.
**Bedeutung.** Macht $\mathrm{Haupt}(f,\lambda)=\ker((f-\lambda)^m)$ für ein endliches $m$ wohldefiniert.

<a id="satz-49-hauptraumzerlegung-strukturhauptsatz"></a>
### Satz 4.9 (Hauptraumzerlegung) — *Strukturhauptsatz*

**Aussage.** Zerfällt $\chi_f=(X-\lambda_1)^{n_1}\cdots(X-\lambda_r)^{n_r}$ ($\lambda_j$ paarweise verschieden), so
$$
V=\bigoplus_{j=1}^r\mathrm{Haupt}(f,\lambda_j),\qquad \dim\mathrm{Haupt}(f,\lambda_j)=n_j,
$$
und $\mathrm{Haupt}(f,\lambda_j)=\ker\big((f-\lambda_j\,\mathrm{id})^{n_j}\big)$.
**Voraussetzungen.** $\chi_f$ zerfällt über $k$.
**Bedeutung.** Zerlegt $V$ in $f$-invariante Bausteine, auf denen $(f-\lambda_j)$ nilpotent ist — die Brücke zur JNF.
**Intuition.** Jeder Eigenwert „beansprucht" einen Teilraum der Dimension $=$ seiner algebraischen Vielfachheit.

<a id="lemma-410-nilpotente-jordan-kette"></a>
### Lemma 4.10 (Nilpotente Jordan-Kette)

**Aussage.** Ist $v\neq0$, $g^{k-1}(v)\neq0$, $g^k(v)=0$, so sind $v,g(v),\dots,g^{k-1}(v)$ linear unabhängig.
**Bedeutung.** Eine Jordan-Kette der Länge $k$ ist wirklich „$k$ unabhängige Stufen".

<a id="satz-411-normalform-nilpotenter-endomorphismen-kern-der-jnf"></a>
### Satz 4.11 (Normalform nilpotenter Endomorphismen) — *Kern der JNF*

**Aussage.** Ist $g\in\mathrm{End}(V)$ nilpotent, so gibt es eine Basis von $V$ der Form
$$
u_1,g(u_1),\dots,g^{a_1-1}(u_1),\ \dots,\ u_s,g(u_s),\dots,g^{a_s-1}(u_s),\qquad g^{a_i}(u_i)=0,
$$
bzgl. der $g$ blockdiagonal aus Jordan-Blöcken $J^{(a_i)}(0)$ besteht.
**Bedeutung.** Klassifiziert nilpotente Abbildungen vollständig; der einzige nichttriviale Schritt zur JNF.
**Intuition.** $V$ zerlegt sich in „Türme" (Jordan-Ketten) unter $g$.

<a id="satz-412-existenz-der-jordan-normalform"></a>
### Satz 4.12 (Existenz der Jordan-Normalform)

**Aussage.** Zerfällt $\chi_f$ über $k$ in Linearfaktoren, so besitzt $f$ eine Jordan-Normalform: es gibt eine Basis von $V$, bzgl. der die Matrix blockdiagonal aus Blöcken $J^{(t)}(\lambda_j)$ besteht, $\lambda_j\in\{\lambda_1,\dots,\lambda_r\}$.
Matrixfassung: Ist $k$ algebraisch abgeschlossen (z. B. $\mathbb{C}$), so ist **jede** Matrix $A\in k^{n\times n}$ ähnlich zu einer JNF $J_A$.
**Voraussetzungen.** $\chi_f$ zerfällt.
**Bedeutung.** Die universelle Normalform; über $\mathbb{C}$ ausnahmslos.

<a id="satz-413-eindeutigkeit-der-jnf-und-blockzahlen"></a>
### Satz 4.13 (Eindeutigkeit der JNF und Blockzahlen)

**Aussage.** Die JNF ist **eindeutig bis auf die Reihenfolge der Blöcke**. Mit $d_k(\lambda):=\dim\ker\big((f-\lambda\,\mathrm{id})^k\big)$ und $d_0:=0$ gilt für die Anzahl der Jordan-Blöcke der Größe **genau $s$** zum Eigenwert $\lambda$:
$$
\ell(s,\lambda)=2\,d_s(\lambda)-d_{s-1}(\lambda)-d_{s+1}(\lambda).
$$
Insbesondere:
- Anzahl **aller** Blöcke zu $\lambda$ $=d_1(\lambda)=\dim\mathrm{Eig}(f,\lambda)$ (geometrische Vielfachheit);
- Anzahl Blöcke der Größe $\ge s$ $=d_s(\lambda)-d_{s-1}(\lambda)$;
- **größter** Block zu $\lambda$ $=m_\lambda$ (Exponent in $\mu_f$);
- **Summe** der Blockgrößen zu $\lambda$ $=n_\lambda=\dim\mathrm{Haupt}(f,\lambda)$.

**Bedeutung.** Die JNF ist eine **vollständige Ähnlichkeitsinvariante**: $A\sim B\Leftrightarrow$ gleiche JNF (bis auf Blockreihenfolge). Aus den Kerndimensionen liest man sie eindeutig ab.

<a id="satz-414-jordan-chevalley-zerlegung"></a>
### Satz 4.14 (Jordan-Chevalley-Zerlegung)

**Aussage.** Zerfällt $\chi_f$, so gibt es eindeutige $f_d,f_n\in\mathrm{End}(V)$ mit
$$
f=f_d+f_n,\quad f_d\ \text{diagonalisierbar},\quad f_n\ \text{nilpotent},\quad f_d\circ f_n=f_n\circ f_d.
$$
**Bedeutung.** „Jedes $f$ $=$ diagonalisierbarer Anteil $+$ nilpotenter Anteil." $f_d$ ist auf $\mathrm{Haupt}(f,\lambda_j)$ die Streckung $\lambda_j$, $f_n=f-f_d$.

---

<a id="beweise-4"></a>
## Beweise

> **Klausurrelevant:** Lemma 4.8, 4.10, **Satz 4.9 (Hauptraumzerlegung)**, **Satz 4.11 (nilpotent)**,
> Existenz 4.12 und die **Blockzahl-Herleitung** 4.13. Die JNF-*Eindeutigkeit* wird oft über die
> Kerndimensionen begründet (siehe unten).

<a id="beweis-von-lemma-48-stabilisierung-beweisstil-direkt"></a>
### Beweis von Lemma 4.8 (Stabilisierung) — *Beweisstil: direkt*

Sei $\ker(g^m)=\ker(g^{m+1})$. Zu zeigen: $\ker(g^{m+1})=\ker(g^{m+2})$ (dann per Induktion alles). Sei $v\in\ker(g^{m+2})$, also $g^{m+1}(g v)=0$, d. h. $gv\in\ker(g^{m+1})=\ker(g^m)$, also $g^m(gv)=g^{m+1}v=0$, d. h. $v\in\ker(g^{m+1})$. Da die Kette aus *echt* wachsenden Räumen besteht, bis sie stehen bleibt, und $\dim V<\infty$, stabilisiert sie nach $\le\dim V$ Schritten. $\blacksquare$

<a id="beweis-von-satz-49-hauptraumzerlegung-beweisstil-bézout-partition-der-eins-direktheit"></a>
### Beweis von Satz 4.9 (Hauptraumzerlegung) — *Beweisstil: Bézout-Partition der Eins $+$ Direktheit*

Setze $g_j=f-\lambda_j\,\mathrm{id}$ und $P_j=\prod_{i\neq j}(X-\lambda_i)^{n_i}$. Die $P_1,\dots,P_r$ haben **keinen gemeinsamen Faktor**, also $\gcd(P_1,\dots,P_r)=1$; Bézout liefert $A_1,\dots,A_r\in k[X]$ mit
$$
\sum_{j=1}^r A_j P_j=1\quad\Longrightarrow\quad \mathrm{id}_V=\sum_{j=1}^r A_j(f)\,P_j(f).\tag{$\ast$}
$$

**$V=\sum_j\mathrm{Haupt}(f,\lambda_j)$.** Für $v\in V$ ist $w_j:=A_j(f)P_j(f)v$. Wegen Cayley-Hamilton $\chi_f(f)=0$ und $\chi_f=(X-\lambda_j)^{n_j}P_j$ gilt $(f-\lambda_j)^{n_j}P_j(f)=\chi_f(f)=0$, also
$$
(f-\lambda_j)^{n_j}w_j=A_j(f)\,(f-\lambda_j)^{n_j}P_j(f)\,v=0\ \Rightarrow\ w_j\in\mathrm{Haupt}(f,\lambda_j).
$$
Nach $(\ast)$ ist $v=\sum_j w_j$. Also erzeugen die Haupträume $V$.

**Direktheit.** Sei $\sum_j u_j=0$ mit $u_j\in\mathrm{Haupt}(f,\lambda_j)$. Fixiere $i$. Auf $\mathrm{Haupt}(f,\lambda_i)$ wirkt $P_i(f)$ **invertierbar** (denn $P_i$ enthält nur Faktoren $(X-\lambda_j)$, $j\neq i$, und $(f-\lambda_j)$ ist auf $\mathrm{Haupt}(f,\lambda_i)$ invertierbar, weil $\lambda_j\neq\lambda_i$). Auf $\mathrm{Haupt}(f,\lambda_j)$ für $j\neq i$ verschwindet $P_i(f)$ (da Faktor $(f-\lambda_j)^{n_j}$ enthalten). Anwenden von $A_i(f)P_i(f)$ auf $\sum_j u_j=0$ ergibt $A_i(f)P_i(f)u_i=0$; da $A_iP_i\equiv1$ auf $\mathrm{Haupt}(f,\lambda_i)$ (modulo der Partition), folgt $u_i=0$. Also alle $u_j=0$.

**Dimension.** Aus der direkten Summe und der Blockstruktur folgt $\sum_j\dim\mathrm{Haupt}(f,\lambda_j)=n=\sum_j n_j$; da stets $\dim\mathrm{Haupt}(f,\lambda_j)\le n_j$ (das ist die algebraische Vielfachheit, vgl. Lemma 2.13 angewandt auf $\mathrm{Haupt}$), folgt Gleichheit überall: $\dim\mathrm{Haupt}(f,\lambda_j)=n_j$. $\blacksquare$

<a id="beweis-von-lemma-410-beweisstil-direkt"></a>
### Beweis von Lemma 4.10 — *Beweisstil: direkt*

Sei $\sum_{i=0}^{k-1}c_i\,g^i(v)=0$. Wende $g^{k-1}$ an: alle Terme mit $i\ge1$ verschwinden ($g^{k-1+i}(v)=0$ für $i\ge1$), übrig bleibt $c_0\,g^{k-1}(v)=0$, also $c_0=0$ (da $g^{k-1}(v)\neq0$). Wende $g^{k-2}$ an: $c_1=0$. Iterativ alle $c_i=0$. $\blacksquare$

<a id="beweis-von-satz-411-nilpotente-normalform-beweisstil-konstruktion-über-kernketten-von-oben-nach-unten"></a>
### Beweis von Satz 4.11 (nilpotente Normalform) — *Beweisstil: Konstruktion über Kernketten (von oben nach unten)*

Sei $g^N=0$, $g^{N-1}\neq0$. Kernkette
$$
\{0\}=\ker(g^0)\subsetneq\ker(g)\subsetneq\dots\subsetneq\ker(g^N)=V.
$$
Setze die **Schichtdimensionen** $\delta_i:=\dim\big(\ker(g^i)/\ker(g^{i-1})\big)=d_i-d_{i-1}$.

**Schlüsselbehauptung.** $g$ induziert für $i\ge2$ eine **injektive** lineare Abbildung
$$
\ker(g^i)/\ker(g^{i-1})\ \longrightarrow\ \ker(g^{i-1})/\ker(g^{i-2}),\qquad x+\ker(g^{i-1})\mapsto g(x)+\ker(g^{i-2}).
$$
*(Wohldefiniert: $x\in\ker(g^i)\Rightarrow g(x)\in\ker(g^{i-1})$; $x\in\ker(g^{i-1})\Rightarrow g(x)\in\ker(g^{i-2})$. Injektiv: $g(x)\in\ker(g^{i-2})\Rightarrow x\in\ker(g^{i-1})$.)*
Folglich $\delta_i\le\delta_{i-1}$, die Schichtdimensionen sind **schwach fallend**: $\delta_1\ge\delta_2\ge\dots\ge\delta_N$.

**Basiskonstruktion (top-down).** Wähle in der obersten Schicht Vektoren $b_{N,1},\dots,b_{N,\delta_N}$, deren Klassen eine Basis von $\ker(g^N)/\ker(g^{N-1})$ bilden. Ihre Bilder $g(b_{N,\cdot})$ sind (nach der Injektivität) unabhängig modulo $\ker(g^{N-2})$ in der nächsten Schicht; ergänze sie dort zu einer Basis. So absteigend fortfahren bis Schicht $1$. Die Gesamtheit aller so erzeugten Vektoren $g^{j}(b_{i,\cdot})$ bildet eine Basis von $V$ (Kardinalität $=\sum_i\delta_i\cdot(\dots)=n$, Unabhängigkeit nach Lemma 4.10 und der Schichtkonstruktion). Jede „Spalte" $b,\,g(b),\,\dots$ ist eine Jordan-Kette und liefert einen Block $J^{(a)}(0)$. $\blacksquare$

> **Aus dem Beweis liest man die Blockzahlen ab:** Anzahl Blöcke der Größe $\ge s$ $=\delta_s=d_s-d_{s-1}$. Für $\lambda=0$ direkt; für allgemeines $\lambda$ wende dies auf $g=f-\lambda\,\mathrm{id}$ an.

<a id="beweis-von-satz-412-existenz-jnf-beweisstil-zusammensetzen"></a>
### Beweis von Satz 4.12 (Existenz JNF) — *Beweisstil: Zusammensetzen*

Nach Satz 4.9 ist $V=\bigoplus_j\mathrm{Haupt}(f,\lambda_j)$, $f$-invariant. Auf $H_j:=\mathrm{Haupt}(f,\lambda_j)$ ist $g_j:=(f-\lambda_j\,\mathrm{id})|_{H_j}$ nilpotent. Nach Satz 4.11 gibt es eine Jordan-Basis von $H_j$ für $g_j$, in der $g_j$ aus Blöcken $J^{(t)}(0)$ besteht. Wegen $f|_{H_j}=g_j+\lambda_j\,\mathrm{id}$ wird daraus $J^{(t)}(0)+\lambda_j E=J^{(t)}(\lambda_j)$. Die Vereinigung der Jordan-Basen aller $H_j$ ist eine Basis von $V$ (direkte Summe), in der $f$ in JNF ist. $\blacksquare$

<a id="beweis-von-satz-413-blockzahlen-eindeutigkeit-beweisstil-invarianten-zählen"></a>
### Beweis von Satz 4.13 (Blockzahlen / Eindeutigkeit) — *Beweisstil: Invarianten zählen*

Die Zahlen $d_k(\lambda)=\dim\ker((f-\lambda)^k)$ sind **ähnlichkeitsinvariant** (Kerne transformieren mit). In JNF zerfällt $(f-\lambda)$ blockweise; ein Block $J^{(t)}(\lambda)$ trägt zu $d_k(\lambda)$ genau $\min(t,k)$ bei (denn $(J^{(t)}(\lambda)-\lambda E)^k$ hat Rang $\max(t-k,0)$, Kerndimension $\min(t,k)$). Also
$$
d_k(\lambda)=\sum_{s\ge1}\min(s,k)\cdot\ell(s,\lambda).
$$
Differenzenbildung liefert: Anzahl Blöcke der Größe $\ge s$ $=d_s-d_{s-1}$, und Anzahl der Größe **genau** $s$:
$$
\ell(s,\lambda)=(d_s-d_{s-1})-(d_{s+1}-d_s)=2d_s-d_{s-1}-d_{s+1}.
$$
Da die $\ell(s,\lambda)$ durch die invarianten $d_k(\lambda)$ eindeutig festgelegt sind, ist die JNF bis auf Blockreihenfolge eindeutig; insbesondere $A\sim B\Leftrightarrow$ gleiche JNF. $\blacksquare$

---

<a id="algorithmen-4"></a>
## Algorithmen

<a id="algorithmus-jordan-normalform-berechnen-kochrezept"></a>
### Algorithmus — Jordan-Normalform berechnen (Kochrezept)

- **Motivation.** Die zentrale Rechenaufgabe der ersten Kurshälfte.
- **Idee.** Pro Eigenwert die Kerndimensionen $d_k$ berechnen; daraus die Blockgrößen ablesen.
- **Voraussetzungen.** $\chi_A$ zerfällt über $k$ (über $\mathbb{C}$ immer).
- **Pseudocode.**
  ```
  Eingabe: A ∈ k^{n×n}
  1. χ_A = ∏_j (X − λ_j)^{n_j}     # Eigenwerte + algebraische Vielfachheiten
  2. für jeden Eigenwert λ_j:
        d_0 ← 0
        d_k ← dim Kern((A − λ_j E)^k)   für k = 1,2,…
              bis d_k = n_j  (= stabilisiert)        # m_j = dieses kleinste k
        für s = 1,2,…,m_j:
            ℓ(s,λ_j) ← 2·d_s − d_{s−1} − d_{s+1}     # Anzahl Blöcke der Größe s
  3. Baue J aus allen Blöcken J^{(s)}(λ_j), je ℓ(s,λ_j)-mal.
  Ausgabe: J     # die Jordan-Normalform
  ```
- **Mathematische Beschreibung.** $\ell(s,\lambda)=2d_s-d_{s-1}-d_{s+1}$ (Satz 4.13); Korrektheit über die Kerndimensionen.
- **Laufzeit.** Pro $\lambda$ und $k$: Matrixpotenz $+$ Rang $O(n^3)$; insgesamt $\approx O(n^4)$.
- **Speicherbedarf.** $O(n^2)$.
- **Korrektheitsidee.** Satz 4.11/4.13.
- **Anwendungen.** Ähnlichkeitstest; $A^m$, $e^{tA}$; Lösen von DGL-Systemen mit defekten Eigenwerten.
- **Typische Fehler.** $(A-\lambda E)^k$ statt $A^k-\lambda E$ rechnen (Reihenfolge/Potenz!); Stabilisierung übersehen; $d_0=0$ vergessen.

> **Probe-Invarianten (immer prüfen!):**
> $\sum_s s\cdot\ell(s,\lambda)=n_\lambda$ (Summe Blockgrößen $=$ alg. Vielfachheit),
> $\sum_s\ell(s,\lambda)=d_1=\dim\mathrm{Eig}$ (Blockzahl $=$ geom. Vielfachheit),
> $\max\{s:\ell(s,\lambda)>0\}=m_\lambda$ (Exponent in $\mu_A$).

<a id="algorithmus-zusatz-jordan-basis-transformationsmatrix-t"></a>
### Algorithmus-Zusatz — Jordan-Basis / Transformationsmatrix $T$

Für jeden Block: wähle einen Vektor $u$ in der höchsten Kernschicht ($u\in\ker((A-\lambda E)^{a})\setminus\ker((A-\lambda E)^{a-1})$), bilde die Kette $u,(A-\lambda E)u,\dots,(A-\lambda E)^{a-1}u$ (das ist ein Jordan-Block, **untere** Kettenglieder zuerst als Basisspalten). Alle Ketten zusammen sind die Spalten von $T$; dann $T^{-1}AT=J$. (Rechenintensiver; in Klausuren oft nur die JNF selbst verlangt.)

---

<a id="beispiele-4"></a>
## Beispiele

**Beispiel 1 (leicht — Block ablesen).** $A=\begin{psmallmatrix}5&1\\0&5\end{psmallmatrix}$: $\chi=(X-5)^2$, $d_1=\dim\ker\begin{psmallmatrix}0&1\\0&0\end{psmallmatrix}=1$, $d_2=2$. $\ell(1)=2d_1-d_0-d_2=2-0-2=0$, $\ell(2)=2d_2-d_1-d_3=4-1-2=1$. Also **ein** Block $J^{(2)}(5)$ — $A$ ist bereits JNF.

**Beispiel 2 (mittel — zwei Blöcke).** Eigenwert $2$, $n_2=4$, gemessene Kerndimensionen $d_1=2,\ d_2=3,\ d_3=4$.
$$
\ell(1)=2\cdot2-0-3=1,\quad\ell(2)=2\cdot3-2-4=0,\quad\ell(3)=2\cdot4-3-4=1.
$$
$\Rightarrow$ Blöcke $J^{(3)}(2)$ und $J^{(1)}(2)$. Probe: $3+1=4=n_2$ ✓, Blockzahl $2=d_1$ ✓, größter Block $3=m_2$.

**Beispiel 3 (mittel — $3\times3$, vollständig).** $A=\begin{psmallmatrix}2&1&0\\0&2&0\\0&0&2\end{psmallmatrix}$: $\chi=(X-2)^3$. $A-2E=\begin{psmallmatrix}0&1&0\\0&0&0\\0&0&0\end{psmallmatrix}$, $d_1=2$ (Kern $=\mathrm{span}(e_1,e_3)$); $(A-2E)^2=0$, $d_2=3$. $\ell(1)=2\cdot2-0-3=1$, $\ell(2)=2\cdot3-2-3=1$. Blöcke: $J^{(2)}(2),J^{(1)}(2)$. $\mu_A=(X-2)^2$, nicht diagonalisierbar.

**Beispiel 4 (mittel — diagonalisierbar als Spezialfall).** $A=\mathrm{diag}(3,3,7)$: alle $d_1=n_\lambda$, also nur Blöcke der Größe $1$. JNF $=A$. $\mu_A=(X-3)(X-7)$ quadratfrei — konsistent mit Kapitel 3.

**Beispiel 5 (schwer — zwei Eigenwerte).**
$\chi_A=(X-6)^7(X+2)^3$. Zu $\lambda=6$ gemessen $d_1=3,d_2=5,d_3=6,d_4=7$; zu $\lambda=-2$: $d_1=2,d_2=3$.
- $\lambda=6$: $\ell(1)=2\cdot3-0-5=1$, $\ell(2)=2\cdot5-3-6=1$, $\ell(3)=2\cdot6-5-7=0$, $\ell(4)=2\cdot7-6-7=1$. Blöcke $J^{(4)},J^{(2)},J^{(1)}$ zu $6$ (Summe $7$ ✓, Blockzahl $3=d_1$ ✓).
- $\lambda=-2$: $\ell(1)=2\cdot2-0-3=1$, $\ell(2)=2\cdot3-2-3=1$. Blöcke $J^{(2)},J^{(1)}$ zu $-2$.
$\mu_A=(X-6)^4(X+2)^2$.

---

<a id="gegenbeispiele-4"></a>
## Gegenbeispiele

**Gegenbeispiel A ($\chi$ zerfällt nicht $\Rightarrow$ keine JNF über $k$).** $\begin{psmallmatrix}0&-1\\1&0\end{psmallmatrix}$ über $\mathbb{R}$: $\chi=X^2+1$ zerfällt nicht $\Rightarrow$ keine JNF über $\mathbb{R}$ (über $\mathbb{C}$: $\mathrm{diag}(i,-i)$). *Die Voraussetzung „$\chi$ zerfällt" ist essenziell.*

**Gegenbeispiel B (JNF nicht eindeutig ohne Blockordnung).** $\mathrm{diag}(J^{(2)}(0),J^{(1)}(0))$ und $\mathrm{diag}(J^{(1)}(0),J^{(2)}(0))$ sind ähnlich — die JNF ist nur **bis auf Blockreihenfolge** eindeutig.

**Gegenbeispiel C ($\mu$ und $\chi$ bestimmen JNF *nicht* allein).**
$\chi=(X-0)^4$, $\mu=(X-0)^2$ ist *nicht eindeutig*: Blöcke $\{2,2\}$ und $\{2,1,1\}$ haben beide $\chi=X^4,\ \mu=X^2$, aber verschiedene JNF (unterscheidbar durch $d_1$: $2$ bzw. $3$). *Man braucht die vollen Kerndimensionen $d_k$.*

**Gegenbeispiel D (geometrische Vielfachheit zählt Blöcke, nicht Würfel).** $J^{(3)}(\lambda)$: alg. Vielfachheit $3$, aber **nur ein** Eigenvektor. Wer „Eigenraum $=$ Hauptraum" annimmt, verfehlt die JNF.

---

<a id="typische-klausuraufgaben-4"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Woran erkennbar | Strategie |
|---|---|---|
| **JNF bestimmen** | „Geben Sie die Jordan-Normalform an." | Kochrezept: $\chi$, dann $d_k$ pro $\lambda$, dann $\ell(s,\lambda)$. |
| **Jordan-Basis / $T$** | „Bestimmen Sie $T$ mit $T^{-1}AT=J$." | Ketten aus höchster Kernschicht aufbauen. |
| **Ähnlichkeit entscheiden** | „Sind $A,B$ ähnlich?" | JNF beider vergleichen (Blockstruktur). |
| **JNF aus $\chi,\mu,d_1$** | „Welche JNF sind möglich?" | alle Blockprofile mit passendem $\chi$ ($\sum$), $\mu$ (max), $d_1$ (Anzahl). |
| **$\mu_A,\chi_A$ aus JNF** | „Lesen Sie $\mu,\chi$ ab." | $\chi=\prod(X-\lambda)^{n_\lambda}$, $\mu=\prod(X-\lambda)^{m_\lambda}$. |
| **$A^m$ / $e^{tA}$** | „Berechnen Sie …" | über JNF (Block-Potenzen geschlossen). |

---

<a id="typische-fehler-4"></a>
## Typische Fehler

| Fehler | Warum falsch | Richtig |
|---|---|---|
| $\mu,\chi$ bestimmen JNF eindeutig | Gegenbeispiel C ($\{2,2\}$ vs. $\{2,1,1\}$). | volle Kerndimensionen $d_k$ nötig. |
| $\mathrm{Eig}=\mathrm{Haupt}$ | nur bei diagonalisierbar gleich. | $\mathrm{Eig}\subsetneq\mathrm{Haupt}$ bei Blöcken $>1$. |
| Blockzahl $=$ alg. Vielfachheit | Blockzahl $=$ **geom.** Vielfachheit $d_1$. | $\sum s\cdot\ell=n_\lambda$, $\sum\ell=d_1$. |
| $(A-\lambda E)^k$ mit $A^k-\lambda^k E$ verwechselt | völlig andere Matrix. | erst $A-\lambda E$, dann potenzieren. |
| $\ell(s)$-Formel ohne $d_0=0$ | Randterm fehlt. | $d_0:=0$ setzen. |
| JNF über $\mathbb{R}$ bei nicht-zerfallendem $\chi$ | existiert nicht. | erst Zerfallen prüfen / zu $\mathbb{C}$ übergehen. |
| Jordan-Kette in falscher Reihenfolge in $T$ | Block wird untere statt obere Nebendiagonale. | unterstes Kettenglied $(A-\lambda E)^{a-1}u$ zuerst. |

> **Vergleichstabelle: die vier Vielfachheits-Zahlen pro Eigenwert $\lambda$.**
>
> | Zahl | Bedeutung | Formel |
> |---|---|---|
> | $n_\lambda$ (algebraisch) | Vielfachheit in $\chi$; $\dim\mathrm{Haupt}$ | $\sum_s s\cdot\ell(s,\lambda)$ |
> | $d_1=\dim\mathrm{Eig}$ (geometrisch) | Anzahl Jordan-Blöcke | $\sum_s\ell(s,\lambda)$ |
> | $m_\lambda$ | Exponent in $\mu$; größter Block | $\max\{s:\ell(s,\lambda)>0\}$ |
> | $\ell(s,\lambda)$ | Blöcke der Größe genau $s$ | $2d_s-d_{s-1}-d_{s+1}$ |
>
> Merksatz: $n_\lambda$ zählt **Würfel**, $d_1$ zählt **Stapel**, $m_\lambda$ ist die **Höhe** des höchsten Stapels.

---

<a id="verbindungen-4"></a>
## Verbindungen

- **← Kapitel 0:** Bézout (Partition der Eins) trägt die Hauptraumzerlegung; „$\chi$ zerfällt" $=$ Faktorisierung.
- **← Kapitel 1:** Die Existenzbeweise nutzen Quotienten/Induktion; $\dim\mathrm{Haupt}$ über Dimensionsformeln.
- **← Kapitel 2:** „$\chi$ zerfällt" ist Voraussetzung; geometrische Vielfachheit $=$ Blockzahl; diagonalisierbar $=$ „alle Blöcke Größe $1$".
- **← Kapitel 3:** $\mu_f=\prod(X-\lambda_j)^{m_j}$, $m_j=$ größter Block; Cayley-Hamilton im Hauptraumbeweis; Diagonalisierbarkeit $=$ $\mu$ quadratfrei $=$ JNF diagonal.
- **→ Kapitel 5 ($\mathbb{C}$):** Über $\mathbb{C}$ existiert die JNF **immer** (Fundamentalsatz) — der Grund, warum die komplexe Theorie „rund" ist.
- **→ Kapitel 8 (Spektralsätze):** Für *normale* Operatoren über $\mathbb{C}$ sind alle Jordan-Blöcke der Größe $1$ (orthonormal diagonalisierbar) — die JNF degeneriert zur Diagonalmatrix mit ONB.

**Definitionen, die später ständig gebraucht werden:** Hauptraum, nilpotent, Jordan-Block, JNF, $d_k(\lambda)$, Blockzahl-Formel.

---

<a id="zusammenfassung-4"></a>
## Zusammenfassung

| Kernaussage | Symbolisch |
|---|---|
| Kernkette wächst und stabilisiert. | $\ker(g^k)\nearrow\mathrm{Haupt}$ |
| Hauptraumzerlegung (bei zerfallendem $\chi$). | $V=\bigoplus_j\mathrm{Haupt}(f,\lambda_j)$ |
| $(f-\lambda_j)$ ist nilpotent auf $\mathrm{Haupt}(f,\lambda_j)$. | — |
| Nilpotente Abb. $=$ Jordan-Ketten. | Blöcke $J^{(a)}(0)$ |
| **Existenz JNF** bei zerfallendem $\chi$ (über $\mathbb{C}$ immer). | (Satz 4.12) |
| JNF **eindeutig** bis auf Blockreihenfolge. | $A\sim B\Leftrightarrow$ gleiche JNF |
| Blockzahlen aus Kerndimensionen. | $\ell(s,\lambda)=2d_s-d_{s-1}-d_{s+1}$ |
| $n_\lambda=$ Würfel, $d_1=$ Stapel, $m_\lambda=$ Höhe. | (Vielfachheitstabelle) |

**Die eine Idee des Kapitels:** Das schwere Klassifikationsproblem zerfällt in zwei leichte — **Hauptraumzerlegung** (Bézout) und **nilpotente Normalform** (Kernketten). Die JNF ist die *vollständige* Ähnlichkeitsinvariante: Sie kodiert jede lineare Abbildung (mit zerfallendem $\chi$) bis auf Basiswechsel exakt durch ihre Blockgrößen — und diese liest man aus den Kerndimensionen $d_k(\lambda)$ ab.



---

<a id="kapitel-5-der-körper-der-komplexen-zahlen"></a>
# Kapitel 5 — Der Körper der komplexen Zahlen

> **Stellung im Kurs.** Dies ist die **Brücke** zwischen Teil I (Normalformen) und Teil III
> (Skalarprodukträume). Teil I endete mit der Einsicht: *Über $\mathbb{C}$ zerfällt jedes Polynom,
> also existiert dort immer eine JNF.* Teil III braucht $\mathbb{C}$ ein zweites Mal — für
> Sesquilinearformen, hermitesche Skalarprodukte und den **Spektralsatz**. Außerdem ist die
> **komplexe Konjugation** das algebraische Werkzeug, das den ganzen unitären Apparat ($A^*=\bar A^{\mathsf T}$,
> normale Operatoren) erst möglich macht.

---

<a id="motivation-5"></a>
## Motivation

Der Körper $\mathbb{R}$ hat einen **Defekt**: das Polynom $X^2+1$ hat keine reelle Nullstelle. Konsequenzen, die wir in Teil I spürten:

- Die Drehmatrix $\begin{psmallmatrix}0&-1\\1&0\end{psmallmatrix}$ hat über $\mathbb{R}$ **keinen** Eigenwert — sie ist weder diagonalisier- noch trigonalisierbar.
- $\chi_f$ zerfällt nicht immer über $\mathbb{R}$ — die JNF existiert nicht garantiert.

Man möchte einen Körper, in dem **jedes** Polynom in Linearfaktoren zerfällt (algebraisch abgeschlossen). Der kleinste Schritt dorthin: **füge eine Wurzel von $X^2+1$ hinzu**. Nennt man sie $i$ (mit $i^2=-1$), entsteht
$$
\mathbb{C}=\{a+bi\mid a,b\in\mathbb{R}\}.
$$
Das überraschende Geschenk (Fundamentalsatz der Algebra): Mit dieser *einen* hinzugefügten Wurzel zerfällt **schon jedes** Polynom — $\mathbb{C}$ ist algebraisch abgeschlossen. Man muss nicht weiter erweitern.

**Warum $\mathbb{C}$ überall auftaucht.** Komplexe Zahlen kodieren **Drehungen und Schwingungen** algebraisch: Wechselstrom, Quantenmechanik, Signalverarbeitung (Fourier), Regelungstechnik — überall, wo „rotieren" und „skalieren" zusammenkommen. Die Euler-Formel $e^{i\varphi}=\cos\varphi+i\sin\varphi$ verbindet *Exponentialwachstum* mit *Rotation* und ist eine der folgenreichsten Gleichungen der Mathematik.

**Mathematische Wurzel.** $\mathbb{C}$ entsteht als **Quotientenring** $\mathbb{R}[X]/(X^2+1)$ (Kapitel 0 und 1!). Da $X^2+1$ über $\mathbb{R}$ **irreduzibel** ist, ist dieser Quotient ein **Körper**. Das ist kein Zufall, sondern das allgemeine Prinzip „$k[X]/(P)$ ist Körper $\Leftrightarrow P$ irreduzibel".

---

<a id="intuition-5"></a>
## Intuition

**$\mathbb{C}$ ist die Ebene mit einer Drehmultiplikation.** Punkte $a+bi$ leben in $\mathbb{R}^2$. Die Addition ist die gewohnte Vektoraddition. Das Neue ist die **Multiplikation**:

- $i$ ist die **Vierteldrehung** (90° gegen den Uhrzeigersinn): $i\cdot1=i$, $i\cdot i=-1$, $i\cdot(-1)=-i$, $i\cdot(-i)=1$. Viermal $i$ $=$ volle Drehung.
- Multiplikation mit $z=r\,e^{i\varphi}$ bedeutet: **drehe um den Winkel $\varphi$ und strecke um den Faktor $r$**.

```
       Im                          Multiplikation mit i = Drehung um 90°
        │   • z=a+bi                       i·z
       b┤  ╱|                               ↑
        │ ╱ |                          z ───┘
        │╱φ |                          (gedreht um 90°, Länge gleich)
   ─────┼───┴──── Re
        │   a
       -b┤  • z̄=a−bi   (Konjugation = Spiegelung an der reellen Achse)
```

**Konjugation = Spiegelung.** $\bar z=a-bi$ ist die Spiegelung von $z$ an der reellen Achse. Sie tauscht „oben" und „unten", lässt $\mathbb{R}$ fest und kehrt Drehrichtungen um.

**Betrag = Länge.** $|z|=\sqrt{a^2+b^2}$ ist der euklidische Abstand zum Ursprung; $|z|^2=z\bar z$.

**Euler-Formel anschaulich.** $e^{i\varphi}$ läuft auf dem **Einheitskreis**: Realteil $\cos\varphi$, Imaginärteil $\sin\varphi$. „Exponential einer imaginären Zahl" $=$ „Punkt auf dem Einheitskreis im Winkel $\varphi$". Das macht Drehungen zu *Multiplikationen* — der ganze Trick.

---

<a id="formale-definitionen-5"></a>
## Formale Definitionen

**Definition 5.1 (Der Körper $\mathbb{C}$).**
$\mathbb{C}=\mathbb{R}\times\mathbb{R}$ mit
$$
(a,b)+(c,d)=(a+c,\ b+d),\qquad (a,b)\cdot(c,d)=(ac-bd,\ ad+bc).
$$
Nullelement $(0,0)$, Einselement $(1,0)$. Man setzt $i:=(0,1)$ und identifiziert $a\in\mathbb{R}$ mit $(a,0)$; dann
$$
(a,b)=a+bi,\qquad i^2=(0,1)(0,1)=(-1,0)=-1.
$$
$\mathbb{C}$ ist ein $\mathbb{R}$-Vektorraum mit Basis $\{1,i\}$.

**Definition 5.2 (alternative Konstruktion).**
$\mathbb{C}\cong\mathbb{R}[X]/(X^2+1)$ via $[P]\mapsto P(i)$; $\bar X$ entspricht $i$ (siehe Satz 5.9). Jedes Element hat den eindeutigen Repräsentanten $a+bX$ (Polynomdivision durch $X^2+1$).

**Definition 5.3 (Real-/Imaginärteil, Betrag, Konjugation).**
Für $z=a+bi$ ($a,b\in\mathbb{R}$):
$$
\mathrm{Re}(z)=a,\quad \mathrm{Im}(z)=b,\quad |z|=\sqrt{a^2+b^2}\ (\text{Betrag}),\quad \bar z=a-bi\ (\text{Konjugierte}).
$$
Die **Konjugation** ist die Abbildung $\mathbb{C}\to\mathbb{C},\ z\mapsto\bar z$.

**Definition 5.4 (Exponential, Sinus, Cosinus — Reihen).**
$$
\exp(z)=\sum_{n=0}^\infty\frac{z^n}{n!}\ (z\in\mathbb{C}),\qquad
\cos(x)=\sum_{n=0}^\infty(-1)^n\frac{x^{2n}}{(2n)!},\qquad
\sin(x)=\sum_{n=0}^\infty(-1)^n\frac{x^{2n+1}}{(2n+1)!}\ (x\in\mathbb{R}).
$$
Man schreibt $e^z:=\exp(z)$ ($e=\exp(1)\approx2{,}71828$).

**Definition 5.5 (Polarkoordinaten).**
Jede komplexe Zahl $z\in\mathbb{C}\setminus\{0\}$ schreibt sich **eindeutig** als
$$
z=r\,e^{i\alpha},\qquad r=|z|>0,\quad \alpha\in[0,2\pi),
$$
mit $z=r(\cos\alpha+i\sin\alpha)$. $\alpha$ heißt **Argument** $\arg(z)$.

> **Korrektur gegenüber gängiger Mitschrift:** Für die *Eindeutigkeit* muss $r>0$ (nicht $r\ge0$) gefordert werden — bei $r=0$ (also $z=0$) ist der Winkel $\alpha$ unbestimmt. Deshalb $z\neq0$.

---

<a id="eigenschaften-5"></a>
## Eigenschaften

| Eigenschaft | Aussage | Kurzbegründung |
|---|---|---|
| **$\mathbb{C}$ ist Körper** | alle Körperaxiome | Inverses $z^{-1}=\bar z/|z|^2$ (Satz 5.6). |
| **$\mathbb{R}\hookrightarrow\mathbb{C}$** | $a\mapsto(a,0)$ ist Körpereinbettung | erhält $+,\cdot$. |
| **Konjugation ist Involution** | $\overline{\bar z}=z$ | zweimal spiegeln. |
| **Konjugation ist Ringhom.** | $\overline{z+w}=\bar z+\bar w$, $\overline{zw}=\bar z\,\bar w$ | Satz 5.7. |
| **$|z|^2=z\bar z$** | reell, $\ge0$ | $(a+bi)(a-bi)=a^2+b^2$. |
| **$z+\bar z=2\mathrm{Re}(z)$, $z-\bar z=2i\,\mathrm{Im}(z)$** | — | direkt. |
| **$z^{-1}=\bar z/|z|^2$** | für $z\neq0$ | $z\cdot\bar z/|z|^2=1$. |
| **$|zw|=|z|\,|w|$, $|\bar z|=|z|$** | Betrag multiplikativ | Satz 5.7. |
| **$\exp(z+w)=\exp(z)\exp(w)$** | Funktionalgleichung | Cauchy-Produkt der Reihen. |
| **$|e^{ix}|=1$** | $e^{ix}$ auf Einheitskreis | $\cos^2+\sin^2=1$. |
| **Multiplikation $\leftrightarrow$ Matrix** | $a+bi\leftrightarrow\begin{psmallmatrix}a&-b\\b&a\end{psmallmatrix}$ | erhält $+,\cdot$ (Satz 5.8). |

---

<a id="sätze-5"></a>
## Sätze

<a id="satz-56-mathbbc-ist-ein-körper"></a>
### Satz 5.6 ($\mathbb{C}$ ist ein Körper)

**Aussage.** $(\mathbb{C},+,\cdot)$ erfüllt alle Körperaxiome; jedes $z\neq0$ hat das Inverse $z^{-1}=\dfrac{\bar z}{|z|^2}$.
**Bedeutung.** $\mathbb{C}$ ist ein vollwertiger Körper — alles aus Teil I (Vektorräume, Eigenwerte, JNF) gilt über $\mathbb{C}$.
**Intuition.** Dividieren $=$ „rückwärts drehen und durch $|z|$ strecken".

<a id="satz-57-rechenregeln-für-konjugation-und-betrag"></a>
### Satz 5.7 (Rechenregeln für Konjugation und Betrag)

**Aussage.** Für $z,w\in\mathbb{C}$:
$$
\overline{z+w}=\bar z+\bar w,\quad \overline{z\,w}=\bar z\,\bar w,\quad z\bar z=|z|^2,\quad |zw|=|z||w|,\quad |\bar z|=|z|.
$$
**Bedeutung.** Das Rechenfundament; insbesondere ist Konjugation ein **Körperautomorphismus** von $\mathbb{C}$, der $\mathbb{R}$ fest lässt.
**Konsequenzen.** $\overline{z^{-1}}=\bar z^{-1}$; $z\in\mathbb{R}\Leftrightarrow z=\bar z$; $z\in i\mathbb{R}\Leftrightarrow z=-\bar z$.

<a id="satz-58-matrixdarstellung-der-multiplikation"></a>
### Satz 5.8 (Matrixdarstellung der Multiplikation)

**Aussage.** Die Abbildung
$$
\mathbb{C}\to\mathbb{R}^{2\times2},\qquad a+bi\mapsto\begin{pmatrix}a&-b\\b&a\end{pmatrix}
$$
ist eine **injektive Ringhomomorphie**: Addition und Multiplikation in $\mathbb{C}$ entsprechen Matrixaddition und -multiplikation. Die Linksmultiplikation $x\mapsto zx$ auf $\mathbb{C}\cong\mathbb{R}^2$ ist genau diese Matrix.
**Bedeutung.** Komplexe Multiplikation ist eine **Drehstreckung** der Ebene; $\det\begin{psmallmatrix}a&-b\\b&a\end{psmallmatrix}=a^2+b^2=|z|^2$.

<a id="satz-59-mathbbccongmathbbrxx21"></a>
### Satz 5.9 ($\mathbb{C}\cong\mathbb{R}[X]/(X^2+1)$)

**Aussage.** Die Abbildung $\mathbb{R}[X]/(X^2+1)\to\mathbb{C}$, $[P]\mapsto P(i)$, ist ein **Körperisomorphismus**.
**Voraussetzungen.** $X^2+1$ irreduzibel über $\mathbb{R}$ (Kapitel 0).
**Bedeutung.** Zeigt $\mathbb{C}$ als „Standard-Quotientenkonstruktion" und verbindet Kapitel 0/1 mit Kapitel 5.

<a id="satz-510-fundamentalsatz-der-algebra"></a>
### Satz 5.10 (Fundamentalsatz der Algebra)

**Aussage.** $\mathbb{C}$ ist algebraisch abgeschlossen: jedes nicht-konstante $P\in\mathbb{C}[X]$ hat eine Nullstelle in $\mathbb{C}$; äquivalent zerfällt jedes $P$ vollständig in Linearfaktoren über $\mathbb{C}$.
**Bedeutung.** *Über $\mathbb{C}$ zerfällt $\chi_f$ immer* $\Rightarrow$ jede komplexe Matrix ist trigonalisierbar und besitzt eine JNF.
**Beweisstil.** **Zitiert** (analytisch-topologischer Beweis, Funktionentheorie).

<a id="satz-511-euler-formel"></a>
### Satz 5.11 (Euler-Formel)

**Aussage.** Für $x\in\mathbb{R}$: $\;e^{ix}=\cos x+i\sin x$. Insbesondere $e^{i\pi}=-1$, also $e^{i\pi}+1=0$, und $e^{2\pi i}=1$.
**Bedeutung.** Verbindet Exponential, Trigonometrie und Geometrie; macht Drehungen zu Multiplikationen.
**Konsequenzen.** Additionstheoreme, Polarform, de Moivre.

<a id="satz-512-polarform-und-multiplikation"></a>
### Satz 5.12 (Polarform und Multiplikation)

**Aussage.** Jedes $z\neq0$ ist eindeutig $z=r\,e^{i\alpha}$ ($r>0$, $\alpha\in[0,2\pi)$). Für $z=re^{i\alpha}$, $w=se^{i\beta}$:
$$
z\,w=rs\,e^{i(\alpha+\beta)},\qquad z^{-1}=r^{-1}e^{-i\alpha},\qquad z^n=r^n e^{in\alpha}\ (\textbf{de Moivre}).
$$
**Bedeutung.** Multiplikation $=$ Winkel addieren $+$ Beträge multiplizieren. Grundlage des Wurzelziehens.
**Intuition.** „Drehen kombiniert sich additiv, Strecken multiplikativ."

---

<a id="beweise-5"></a>
## Beweise

> **Klausurrelevant:** Satz 5.6 (Inverses), 5.7 (Konjugationsregeln), **5.11 (Euler)**, Additionstheoreme, 5.9.

<a id="beweis-von-satz-56-inverses-beweisstil-direkt-konstruktion"></a>
### Beweis von Satz 5.6 (Inverses) — *Beweisstil: direkt (Konstruktion)*

Assoziativität/Kommutativität/Distributivität rechnet man komponentenweise nach (oder folgt aus Satz 5.8/5.9). Für $z=a+bi\neq0$ ist $|z|^2=a^2+b^2>0$, und
$$
z\cdot\frac{\bar z}{|z|^2}=\frac{z\bar z}{|z|^2}=\frac{|z|^2}{|z|^2}=1.
$$
Also ist $\dfrac{\bar z}{|z|^2}=\dfrac{a-bi}{a^2+b^2}$ das multiplikative Inverse. $\blacksquare$

<a id="beweis-von-satz-57-konjugationbetrag-beweisstil-direkt"></a>
### Beweis von Satz 5.7 (Konjugation/Betrag) — *Beweisstil: direkt*

Mit $z=a+bi$, $w=c+di$:
$$
\overline{z+w}=\overline{(a+c)+(b+d)i}=(a+c)-(b+d)i=\bar z+\bar w.
$$
$$
\overline{zw}=\overline{(ac-bd)+(ad+bc)i}=(ac-bd)-(ad+bc)i=(a-bi)(c-di)=\bar z\,\bar w.
$$
Für den Betrag: $|zw|^2=(zw)\overline{(zw)}=zw\bar z\bar w=(z\bar z)(w\bar w)=|z|^2|w|^2$, also $|zw|=|z||w|$ (beide $\ge0$). $\blacksquare$

<a id="beweis-von-satz-59-mathbbccongmathbbrxx21-beweisstil-homomorphiesatz"></a>
### Beweis von Satz 5.9 ($\mathbb{C}\cong\mathbb{R}[X]/(X^2+1)$) — *Beweisstil: Homomorphiesatz*

Die Auswertung $\mathrm{ev}_i\colon\mathbb{R}[X]\to\mathbb{C}$, $P\mapsto P(i)$, ist ein surjektiver Ringhomomorphismus ($a+bX\mapsto a+bi$). Ihr Kern ist $\{P\mid P(i)=0\}=(X^2+1)$ (denn $X^2+1$ ist das normierte Erzeugerpolynom dieses Ideals — irreduzibel, $i$ als Nullstelle). Nach dem Homomorphiesatz (Kapitel 1) ist $\mathbb{R}[X]/(X^2+1)\cong\mathrm{Bild}=\mathbb{C}$. Da $X^2+1$ irreduzibel ist, ist der Quotient ein Körper. $\blacksquare$

<a id="beweis-von-satz-511-euler-beweisstil-reihenumordnung-absolute-konvergenz"></a>
### Beweis von Satz 5.11 (Euler) — *Beweisstil: Reihenumordnung (absolute Konvergenz)*

Setze $z=ix$ in die Exponentialreihe ein und spalte nach geraden/ungeraden Indizes (erlaubt, da absolut konvergent):
$$
e^{ix}=\sum_{n=0}^\infty\frac{(ix)^n}{n!}
=\sum_{k=0}^\infty\frac{(ix)^{2k}}{(2k)!}+\sum_{k=0}^\infty\frac{(ix)^{2k+1}}{(2k+1)!}.
$$
Mit $i^{2k}=(i^2)^k=(-1)^k$ und $i^{2k+1}=i\cdot(-1)^k$:
$$
e^{ix}=\sum_{k=0}^\infty(-1)^k\frac{x^{2k}}{(2k)!}+i\sum_{k=0}^\infty(-1)^k\frac{x^{2k+1}}{(2k+1)!}=\cos x+i\sin x.\ \blacksquare
$$

<a id="korollar-additionstheoreme-beweisstil-real-imaginärteilvergleich"></a>
### Korollar (Additionstheoreme) — *Beweisstil: Real-/Imaginärteilvergleich*

$$
\cos(x+y)+i\sin(x+y)=e^{i(x+y)}=e^{ix}e^{iy}=(\cos x+i\sin x)(\cos y+i\sin y).
$$
Ausmultiplizieren und Vergleich von Real- und Imaginärteil:
$$
\cos(x+y)=\cos x\cos y-\sin x\sin y,\qquad \sin(x+y)=\sin x\cos y+\cos x\sin y.\ \blacksquare
$$

<a id="beweis-von-satz-512-polarmultiplikation-beweisstil-direkt-mit-euler"></a>
### Beweis von Satz 5.12 (Polarmultiplikation) — *Beweisstil: direkt mit Euler*

$z\,w=re^{i\alpha}\,se^{i\beta}=rs\,e^{i\alpha}e^{i\beta}=rs\,e^{i(\alpha+\beta)}$ (Funktionalgleichung von $\exp$). Iteriert: $z^n=r^ne^{in\alpha}$. Inverses: $z\cdot r^{-1}e^{-i\alpha}=e^{0}=1$. Eindeutigkeit der Darstellung: $r=|z|$ ist eindeutig; $\alpha$ ist durch $\cos\alpha=\mathrm{Re}(z)/r$, $\sin\alpha=\mathrm{Im}(z)/r$ in $[0,2\pi)$ eindeutig festgelegt (für $z\neq0$). $\blacksquare$

---

<a id="algorithmen-5"></a>
## Algorithmen

<a id="algorithmus-a-umrechnung-kartesisch-leftrightarrow-polar"></a>
### Algorithmus A — Umrechnung kartesisch $\leftrightarrow$ polar

- **Motivation.** Multiplikation/Potenzen/Wurzeln gehen in Polarform viel leichter.
- **Pseudocode.**
  ```
  kartesisch → polar:   r ← sqrt(a²+b²);  α ← atan2(b,a) mod 2π
  polar → kartesisch:   a ← r·cos α;       b ← r·sin α
  ```
- **Laufzeit/Speicher.** $O(1)$.
- **Typische Fehler.** Quadranten falsch (immer `atan2`, nicht `arctan(b/a)` ohne Vorzeichenprüfung); $r=0$ behandeln (Winkel undefiniert).

<a id="algorithmus-b-n-te-wurzeln-einer-komplexen-zahl-de-moivre"></a>
### Algorithmus B — $n$-te Wurzeln einer komplexen Zahl (de Moivre)

- **Motivation.** Klassische Klausuraufgabe: „Bestimmen Sie alle Lösungen von $w^n=z$."
- **Idee.** In Polarform $z=r e^{i\alpha}$ hat $w^n=z$ genau $n$ Lösungen, gleichmäßig auf einem Kreis verteilt.
- **Voraussetzungen.** $z\neq0$.
- **Pseudocode.**
  ```
  Eingabe: z = r·e^{iα} (r>0),  n ≥ 1
  für k = 0,…,n−1:
      w_k ← r^{1/n} · exp( i·(α + 2πk)/n )
  Ausgabe: w_0,…,w_{n−1}     # n verschiedene n-te Wurzeln
  ```
- **Mathematische Beschreibung.** $w_k=r^{1/n}\exp\!\big(i\frac{\alpha+2\pi k}{n}\big)$, $k=0,\dots,n-1$. Die $n$-ten **Einheitswurzeln** sind der Fall $z=1$: $\zeta_k=e^{2\pi i k/n}$.
- **Laufzeit/Speicher.** $O(n)$ / $O(n)$.
- **Korrektheitsidee.** $w_k^n=r\,e^{i(\alpha+2\pi k)}=r\,e^{i\alpha}=z$; verschiedene $k\in\{0,\dots,n-1\}$ geben verschiedene Winkel modulo $2\pi$.
- **Anwendungen.** Nullstellen von $X^n-z$; Faktorisierung über $\mathbb{C}$; FFT.
- **Typische Fehler.** Nur eine Wurzel angeben (es sind $n$!); $+2\pi k$ vergessen; $r^{1/n}$ als ganze reelle Wurzel statt $\ge0$ wählen.

---

<a id="beispiele-5"></a>
## Beispiele

**Beispiel 1 (leicht — kartesisch rechnen).** $(1+i)^2=1+2i+i^2=2i$. $\dfrac{1}{2-i}=\dfrac{2+i}{(2-i)(2+i)}=\dfrac{2+i}{5}=\tfrac25+\tfrac15 i$.

**Beispiel 2 (leicht — Polarform).** $1+i=\sqrt2\,e^{i\pi/4}$ (denn $|1+i|=\sqrt2$, Winkel $45°$). Damit $(1+i)^8=(\sqrt2)^8 e^{i\cdot8\cdot\pi/4}=16\,e^{2\pi i}=16$.

**Beispiel 3 (mittel — Division in Polarform).** $\dfrac{1+i}{1-i}=\dfrac{\sqrt2 e^{i\pi/4}}{\sqrt2 e^{-i\pi/4}}=e^{i\pi/2}=i$.

**Beispiel 4 (mittel — Einheitswurzeln).** Dritte Einheitswurzeln ($w^3=1$): $\zeta_k=e^{2\pi i k/3}$, $k=0,1,2$:
$$
1,\quad -\tfrac12+\tfrac{\sqrt3}{2}i,\quad -\tfrac12-\tfrac{\sqrt3}{2}i.
$$
Sie bilden ein gleichseitiges Dreieck auf dem Einheitskreis.

**Beispiel 5 (mittel — Wurzel ziehen).** $w^2=i=e^{i\pi/2}$: $w_k=e^{i(\pi/2+2\pi k)/2}$, $k=0,1$:
$$
w_0=e^{i\pi/4}=\tfrac{1}{\sqrt2}(1+i),\qquad w_1=e^{i5\pi/4}=-\tfrac{1}{\sqrt2}(1+i).
$$

**Beispiel 6 (schwer — Faktorisierung über $\mathbb{C}$).** $X^4+1$ hat die Nullstellen $e^{i\pi/4},e^{i3\pi/4},e^{i5\pi/4},e^{i7\pi/4}$, also
$$
X^4+1=\prod_{k}(X-e^{i(2k+1)\pi/4})=(X^2-\sqrt2\,X+1)(X^2+\sqrt2\,X+1)\ \text{über }\mathbb{R}.
$$

---

<a id="gegenbeispiele-5"></a>
## Gegenbeispiele

**Gegenbeispiel A ($\mathbb{C}$ ist nicht anordbar).** Gäbe es eine mit $+,\cdot$ verträgliche Ordnung, so wären alle Quadrate $\ge0$. Dann $i^2=-1\ge0$, aber auch $1=1^2\ge0$; Addition gibt $0=1+(-1)\ge2>0$ — Widerspruch. *Auf $\mathbb{C}$ gibt es kein sinnvolles „$<$".* (Deshalb braucht „positiv definit" in Kapitel 6 die hermitesche Konstruktion.)

**Gegenbeispiel B (Konjugation ist nicht $\mathbb{C}$-linear).** $\overline{i\cdot1}=\overline{i}=-i$, aber $i\cdot\overline{1}=i$. Also $\overline{i\,z}\neq i\,\bar z$ — Konjugation ist nur $\mathbb{R}$-linear (sie ist **konjugiert-linear**). Genau das macht Sesquilinearformen (Kapitel 6) nötig.

**Gegenbeispiel C (Polarform versagt bei $z=0$).** $0=0\cdot e^{i\alpha}$ für **jedes** $\alpha$ — der Winkel ist nicht bestimmt. Deshalb $r>0$ und $z\neq0$ in Satz 5.12.

**Gegenbeispiel D ($\sqrt{zw}=\sqrt z\sqrt w$ gilt nicht).** Mit $z=w=-1$: $\sqrt{(-1)(-1)}=\sqrt1=1$, aber $\sqrt{-1}\cdot\sqrt{-1}=i\cdot i=-1$. *Wurzeln sind mehrdeutig; es gibt keinen global stetigen „Hauptzweig".*

---

<a id="typische-klausuraufgaben-5"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Woran erkennbar | Strategie |
|---|---|---|
| **Kartesisch rechnen** | $(a+bi)(c+di)$, Division | ausmultiplizieren; dividieren via $\bar w/|w|^2$. |
| **Polarform / Potenzen** | „$z^{10}$" o. Ä. | in $re^{i\alpha}$, de Moivre. |
| **$n$-te Wurzeln** | „Alle Lösungen von $w^n=z$." | Algorithmus B; **alle $n$** angeben. |
| **Konjugationsregeln beweisen** | „Zeigen Sie $\overline{zw}=\bar z\bar w$." | komponentenweise. |
| **Euler / Additionstheoreme** | „Leiten Sie … her." | $e^{i(x+y)}=e^{ix}e^{iy}$, Real/Imaginärteil. |
| **Faktorisierung über $\mathbb{C}/\mathbb{R}$** | „Zerlegen Sie $X^n\pm1$." | Einheitswurzeln, konjugierte Paare zu reellen Quadraten zusammenfassen. |

---

<a id="typische-fehler-5"></a>
## Typische Fehler

| Fehler | Warum falsch | Richtig |
|---|---|---|
| nur **eine** $n$-te Wurzel | es gibt genau $n$. | $+\frac{2\pi k}{n}$, $k=0,\dots,n-1$. |
| $r\ge0$ in der Polarform | bei $r=0$ Winkel undefiniert. | $r>0$, $z\neq0$ (Korrektur). |
| Konjugation als $\mathbb{C}$-linear | $\overline{iz}=-i\bar z\neq i\bar z$. | konjugiert-linear. |
| $\mathbb{C}$ anordnen | unmöglich (Gegenbeispiel A). | nur $|z|$ vergleichen. |
| $|z|$ und $|z|^2$ verwechseln | $z\bar z=|z|^2$, nicht $|z|$. | $|z|=\sqrt{z\bar z}$. |
| $\arg$ ohne Quadrant | `arctan(b/a)` verliert Vorzeichen. | `atan2(b,a)`. |
| $\sqrt{zw}=\sqrt z\sqrt w$ | Wurzel mehrdeutig (Gegenbeispiel D). | mit Polarform/allen Wurzeln arbeiten. |

> **Vergleichstabelle: $\mathbb{R}$ vs. $\mathbb{C}$.**
>
> | | $\mathbb{R}$ | $\mathbb{C}$ |
> |---|---|---|
> | $X^2+1$ | keine Nullstelle | $\pm i$ |
> | algebraisch abgeschlossen | nein | **ja** (Fundamentalsatz) |
> | anordbar | ja | **nein** |
> | $\chi_f$ zerfällt | nicht immer | **immer** |
> | JNF existiert | nicht immer | **immer** |
> | „Skalarprodukt" | symmetrische Bilinearform | hermitesche Sesquilinearform |

---

<a id="verbindungen-5"></a>
## Verbindungen

- **← Kapitel 0:** $X^2+1$ irreduzibel über $\mathbb{R}$ $\Rightarrow$ $\mathbb{R}[X]/(X^2+1)$ Körper; Fundamentalsatz als algebraische Abschließung.
- **← Kapitel 1:** $\mathbb{C}$ ist ein **Quotient** $\mathbb{R}[X]/(X^2+1)$; der Iso folgt aus dem Homomorphiesatz.
- **→ Kapitel 2/4:** Über $\mathbb{C}$ zerfällt $\chi_f$ stets $\Rightarrow$ jede Matrix trigonalisierbar, JNF existiert immer.
- **→ Kapitel 6:** Die **Konjugation** (konjugiert-linear, Gegenbeispiel B) erzwingt Sesquilinearformen statt Bilinearformen; $|z|^2=z\bar z$ ist der Prototyp eines positiv-definiten hermiteschen Produkts.
- **→ Kapitel 8:** $A^*=\bar A^{\mathsf T}$ (adjungierte Matrix) lebt von der Konjugation; der **Spektralsatz** ist die schönste Konsequenz der algebraischen Abgeschlossenheit von $\mathbb{C}$.

**Definitionen, die später ständig gebraucht werden:** $\bar z$, $|z|$, $\mathrm{Re}/\mathrm{Im}$, „$\mathbb{C}$ algebraisch abgeschlossen", konjugiert-linear.

---

<a id="zusammenfassung-5"></a>
## Zusammenfassung

| Kernaussage | Symbolisch |
|---|---|
| $\mathbb{C}=\mathbb{R}^2$ mit Drehmultiplikation; $i^2=-1$. | $(a,b)(c,d)=(ac-bd,ad+bc)$ |
| $\mathbb{C}$ ist Körper; $z^{-1}=\bar z/|z|^2$. | (Satz 5.6) |
| Konjugation: Ringhom., Involution, fixiert $\mathbb{R}$. | $\overline{zw}=\bar z\bar w$ |
| $\mathbb{C}\cong\mathbb{R}[X]/(X^2+1)$. | (Satz 5.9) |
| **Fundamentalsatz:** $\mathbb{C}$ algebraisch abgeschlossen. | jedes $P$ zerfällt |
| **Euler:** $e^{ix}=\cos x+i\sin x$, $e^{i\pi}+1=0$. | (Satz 5.11) |
| Polarform (eindeutig, $r>0$): Multiplikation $=$ Winkel $+$, Betrag $\cdot$. | $z=re^{i\alpha}$, de Moivre |
| $n$-te Wurzeln: $n$ Stück, gleichverteilt. | $w_k=r^{1/n}e^{i(\alpha+2\pi k)/n}$ |
| $\mathbb{C}$ ist **nicht** anordbar. | (Gegenbeispiel A) |

**Die eine Idee des Kapitels:** Man fügt $\mathbb{R}$ eine einzige Wurzel von $X^2+1$ hinzu — und erhält einen Körper, in dem *jedes* Polynom zerfällt (Fundamentalsatz). Geometrisch ist $\mathbb{C}$ die Ebene mit Drehmultiplikation; die Euler-Formel macht Drehungen zu Exponentialen. Die **konjugiert-lineare Konjugation** ist das Werkzeug, das in Teil III die ganze unitäre Theorie trägt.



---

<a id="kapitel-6-skalarprodukt-norm-und-metrik"></a>
# Kapitel 6 — Skalarprodukt, Norm und Metrik

> **Stellung im Kurs.** Hier beginnt Teil III: die **Geometrie** der Vektorräume. Bis jetzt hatten
> Vektoren weder Länge noch Winkel — reine lineare Algebra ist „ungemessen". Ein **Skalarprodukt**
> fügt genau diese metrische Struktur hinzu und macht Längen, Abstände, Winkel, Orthogonalität und
> Projektionen (Kapitel 7) sowie die Spektralsätze (Kapitel 8) überhaupt erst möglich. Die
> zentrale Feinheit: Über $\mathbb{C}$ muss man **sesquilinear** statt bilinear arbeiten, sonst hat
> kein Vektor eine sinnvolle Länge.

---

<a id="motivation-6"></a>
## Motivation

In der bisherigen linearen Algebra kann man addieren und skalieren — aber nicht **messen**. Es gibt keine Antwort auf:

- „Wie **lang** ist ein Vektor?"
- „Welchen **Winkel** schließen zwei Vektoren ein?"
- „Wann stehen zwei Vektoren **senkrecht**?"
- „Welcher Punkt eines Unterraums ist einem gegebenen Vektor am **nächsten**?" (Bestapproximation, kleinste Quadrate)

All das braucht ein zusätzliches Datum: das **Skalarprodukt** $\langle v,w\rangle$. Es ist die algebraische Maschine, die jedem Vektorpaar eine Zahl zuordnet, aus der man Länge ($\|v\|=\sqrt{\langle v,v\rangle}$), Winkel und Orthogonalität gewinnt.

**Warum über $\mathbb{C}$ die Bilinearität scheitert.** Die naive Fortsetzung des reellen Standardprodukts, $\langle x,y\rangle=\sum x_iy_i$, liefert über $\mathbb{C}$ Unsinn: $\langle(i,0),(i,0)\rangle=i^2=-1<0$ — eine „negative Länge²". Die Rettung ist die **Konjugation** aus Kapitel 5:
$$
\langle x,y\rangle=\sum_i x_i\overline{y_i}\ \Rightarrow\ \langle x,x\rangle=\sum_i|x_i|^2\ge0.
$$
Der Preis: das Produkt ist im zweiten Argument nur noch **konjugiert-linear** (sesquilinear). Genau hier zahlt sich Kapitel 5 aus.

**Anwendungen.** Methode der kleinsten Quadrate (Statistik/Regression), Fourier-Analyse (Funktionen als „Vektoren", Orthogonalität von $\sin,\cos$), Quantenmechanik (Zustände in Hilberträumen, $\langle\psi\mid\phi\rangle$), Signalverarbeitung, numerische Optimierung. Der Begriff „Winkel zwischen Funktionen" wird durch das Skalarprodukt erst sinnvoll.

**Mathematische Wurzel.** Historisch aus der euklidischen Geometrie (Skalarprodukt $=|v||w|\cos\theta$) abstrahiert. Cauchy und Schwarz bewiesen die fundamentale Ungleichung, die Winkel und Dreiecksungleichung trägt.

---

<a id="intuition-6"></a>
## Intuition

**Das Skalarprodukt misst „Ausrichtung".** $\langle v,w\rangle$ ist groß, wenn $v,w$ „in dieselbe Richtung zeigen", null, wenn sie senkrecht stehen, negativ, wenn sie „entgegengesetzt" sind. Die Selbstpaarung $\langle v,v\rangle=\|v\|^2$ ist das **Längenquadrat**.

**Drei Ebenen der Struktur — was induziert was?**
```
   SKALARPRODUKT  ⟨v,w⟩        (misst Länge UND Winkel)
        │  ‖v‖ := √⟨v,v⟩
        ▼
      NORM  ‖v‖                (misst nur Länge)
        │  d(v,w) := ‖v−w‖
        ▼
     METRIK  d(v,w)            (misst nur Abstand)
        │
        ▼
    TOPOLOGIE                  (misst nur „nah/fern")
```
Jeder Pfeil geht **nur in eine Richtung** von selbst. Die Rückrichtungen gelten nur unter Zusatzbedingungen (siehe Kasten unten) — das war eine berechtigte Verständnisfrage.

**Warum die Konjugation im 2. Argument?** Damit $\langle v,v\rangle$ **reell und $\ge0$** wird. Anschaulich: Länge muss eine positive reelle Zahl sein. Die Konjugation „bügelt die imaginären Anteile bei der Selbstpaarung weg" ($z\bar z=|z|^2$).

**Cauchy-Schwarz anschaulich.** $|\langle v,w\rangle|\le\|v\|\,\|w\|$ sagt: „Die Ausrichtung ist nie größer als das Produkt der Längen" — d. h. $\cos\theta\le1$. Gleichheit genau bei parallelen Vektoren.

---

<a id="formale-definitionen-6"></a>
## Formale Definitionen

Sei $V$ ein Vektorraum über $k$.

**Definition 6.1 (Bilinearform).**
$s\colon V\times V\to k$ heißt **Bilinearform**, wenn sie in **beiden** Argumenten linear ist: für alle $v,v',w,w'\in V$, $a\in k$,
$$
s(v+v',w)=s(v,w)+s(v',w),\quad s(av,w)=a\,s(v,w),
$$
$$
s(v,w+w')=s(v,w)+s(v,w'),\quad s(v,aw)=a\,s(v,w).
$$
$s$ heißt **symmetrisch**, wenn $s(v,w)=s(w,v)$ für alle $v,w$.

**Definition 6.2 (Sesquilinearform, über $k=\mathbb{C}$).**
$s\colon V\times V\to\mathbb{C}$ heißt **Sesquilinearform**, wenn sie im **ersten** Argument linear und im **zweiten** konjugiert-linear ist:
$$
s(v+v',w)=s(v,w)+s(v',w),\quad s(av,w)=a\,s(v,w),
$$
$$
s(v,w+w')=s(v,w)+s(v,w'),\quad s(v,aw)=\overline{a}\,s(v,w).
$$

> **Konventionsfestlegung (durchgehend in diesem Skript):** linear im **1.**, konjugiert-linear im **2.** Argument. Manche Bücher wählen es umgekehrt; wir bleiben konsequent bei dieser Wahl, damit $\langle x,y\rangle=\sum_i x_i\overline{y_i}$ und $A^*=\bar A^{\mathsf T}$ (Kapitel 8) konsistent sind.

**Definition 6.3 (hermitesch).**
Eine Sesquilinearform $s$ heißt **hermitesch**, wenn $s(v,w)=\overline{s(w,v)}$ für alle $v,w$. Dann ist $s(v,v)=\overline{s(v,v)}\in\mathbb{R}$ (reell).

**Definition 6.4 (positiv definit, Skalarprodukt).**
- Eine symmetrische Bilinearform (über $\mathbb{R}$) bzw. hermitesche Sesquilinearform (über $\mathbb{C}$) heißt **positiv definit**, wenn $s(v,v)>0$ für alle $v\neq0$.
- Ein **Skalarprodukt** ist eine positiv definite symmetrische Bilinearform (reell) bzw. positiv definite hermitesche Sesquilinearform (komplex). Man schreibt $\langle v,w\rangle$ statt $s(v,w)$.

**Definition 6.5 (euklidischer / unitärer Vektorraum).**
- Ein **euklidischer Vektorraum** ist ein $\mathbb{R}$-Vektorraum mit Skalarprodukt.
- Ein **unitärer Vektorraum** ist ein $\mathbb{C}$-Vektorraum mit Skalarprodukt.

**Definition 6.6 (Norm).**
Eine **Norm** auf einem $\mathbb{R}$- oder $\mathbb{C}$-Vektorraum $V$ ist $\|\cdot\|\colon V\to\mathbb{R}$ mit
$$
\text{(N1)}\ \|a v\|=|a|\,\|v\|,\qquad
\text{(N2)}\ \|v+w\|\le\|v\|+\|w\|\ (\text{Dreiecksungleichung}),\qquad
\text{(N3)}\ \|v\|=0\Leftrightarrow v=0.
$$

**Definition 6.7 (Metrik).**
Eine **Metrik** auf einer Menge $M$ ist $d\colon M\times M\to\mathbb{R}$ mit
$$
\text{(M1)}\ d(x,y)=d(y,x),\qquad
\text{(M2)}\ d(x,z)\le d(x,y)+d(y,z),\qquad
\text{(M3)}\ d(x,y)=0\Leftrightarrow x=y.
$$

**Definition 6.8 (induzierte Norm/Metrik, Winkel).**
In einem euklidischen/unitären Raum:
$$
\|v\|:=\sqrt{\langle v,v\rangle}\ (\text{Länge}),\qquad d(v,w):=\|v-w\|\ (\text{Abstand}).
$$
Im **euklidischen** Fall (für $v,w\neq0$) der **Winkel**
$$
\angle(v,w):=\arccos\!\left(\frac{\langle v,w\rangle}{\|v\|\,\|w\|}\right)\in[0,\pi].
$$

> **Korrektur/Präzisierung:** Die Winkelformel setzt $\langle v,w\rangle\in\mathbb{R}$ voraus und ist daher direkt nur im **euklidischen** Fall sinnvoll. Im unitären Fall ist $\langle v,w\rangle$ i. A. komplex; man verwendet dann $\mathrm{Re}\langle v,w\rangle$ oder $|\langle v,w\rangle|$. Cauchy-Schwarz sichert, dass das Argument von $\arccos$ in $[-1,1]$ liegt.

---

<a id="eigenschaften-6"></a>
## Eigenschaften

| Eigenschaft | Aussage | Kurzbegründung |
|---|---|---|
| **hermitesch $\Rightarrow$ $\langle v,v\rangle\in\mathbb{R}$** | Selbstpaarung reell | $s(v,v)=\overline{s(v,v)}$. |
| **Standardprodukt pos. definit** | $\langle x,x\rangle=\sum|x_i|^2>0$ für $x\neq0$ | Summe von Quadraten/Beträgen. |
| **Matrixform** | $\langle x,y\rangle=x^{\mathsf T}A\bar y$; herm. $\Leftrightarrow A=A^*$ | Sesquilinearität. |
| **$\|v\|\ge0$** | Norm nichtnegativ | Lemma 6.10. |
| **$d\ge0$** | Metrik nichtnegativ | Lemma 6.11. |
| **Cauchy-Schwarz** | $|\langle v,w\rangle|\le\|v\|\|w\|$ | Satz 6.13. |
| **Norm $\Rightarrow$ Metrik** | $d(v,w)=\|v-w\|$ ist Metrik | Lemma 6.12. |
| **Skalarprodukt $\Rightarrow$ Norm** | $\|v\|=\sqrt{\langle v,v\rangle}$ ist Norm | Satz 6.14. |

> **Antwort auf „was induziert was, und wann rückwärts?"**
>
> | Übergang | Gilt immer? | Rückrichtung gilt genau dann, wenn … |
> |---|---|---|
> | Skalarprodukt $\to$ Norm | ja ($\|v\|=\sqrt{\langle v,v\rangle}$) | die Norm die **Parallelogrammgleichung** erfüllt (Jordan–von Neumann; Kap. 7). |
> | Norm $\to$ Metrik | ja ($d=\|v-w\|$) | die Metrik **translationsinvariant** und **homogen** ist: $d(v+u,w+u)=d(v,w)$, $d(av,aw)=|a|d(v,w)$. |
> | Metrik $\to$ Topologie | ja (offene Bälle) | (fast nie eindeutig umkehrbar) |
>
> Kurz: **Skalarprodukt ist die reichste Struktur, Topologie die ärmste.** Jeder Abstieg ist kanonisch, jeder Aufstieg braucht eine Zusatzbedingung.

---

<a id="sätze-6"></a>
## Sätze

<a id="satz-69-matrixkriterien"></a>
### Satz 6.9 (Matrixkriterien)

**Aussage.** Für $A\in k^{n\times n}$ ist $(x,y)\mapsto x^{\mathsf T}Ay$ (reell) bzw. $x^{\mathsf T}A\bar y$ (komplex) eine Bilinear- bzw. Sesquilinearform. Sie ist
- **symmetrisch** $\Leftrightarrow A^{\mathsf T}=A$ (reell),
- **hermitesch** $\Leftrightarrow A^*:=\bar A^{\mathsf T}=A$ (komplex).

**Bedeutung.** Skalarprodukte auf $k^n$ entsprechen **positiv definiten** (hermiteschen/symmetrischen) Matrizen.

<a id="lemma-610-vge0"></a>
### Lemma 6.10 ($\|v\|\ge0$)

**Aussage.** Für jede Norm gilt $\|v\|\ge0$.
**Beweisstil.** *direkt aus N1/N2/N3.*

<a id="lemma-611-dxyge0"></a>
### Lemma 6.11 ($d(x,y)\ge0$)

**Aussage.** Für jede Metrik gilt $d(x,y)\ge0$.
**Beweisstil.** *direkt aus M1/M2/M3.*

<a id="lemma-612-norm-induziert-metrik"></a>
### Lemma 6.12 (Norm induziert Metrik)

**Aussage.** Ist $\|\cdot\|$ eine Norm, so ist $d(v,w)=\|v-w\|$ eine Metrik.
**Bedeutung.** Jeder normierte Raum ist metrischer Raum.

<a id="satz-613-cauchy-schwarz-ungleichung-zentral"></a>
### Satz 6.13 (Cauchy-Schwarz-Ungleichung) — *zentral*

**Aussage.** In einem euklidischen oder unitären Vektorraum gilt für alle $v,w$:
$$
|\langle v,w\rangle|\le\|v\|\,\|w\|,
$$
mit Gleichheit genau dann, wenn $v,w$ linear abhängig sind.
**Voraussetzungen.** $\langle\cdot,\cdot\rangle$ positiv definit.
**Bedeutung.** Sichert die Dreiecksungleichung der induzierten Norm und die Wohldefiniertheit des Winkels ($\arccos$-Argument in $[-1,1]$).
**Intuition.** „Ausrichtung $\le$ Produkt der Längen."

<a id="satz-614-induzierte-norm-ist-norm"></a>
### Satz 6.14 (induzierte Norm ist Norm)

**Aussage.** $\|v\|=\sqrt{\langle v,v\rangle}$ erfüllt (N1)–(N3), ist also eine Norm; damit ist $d(v,w)=\|v-w\|$ eine Metrik.
**Bedeutung.** Skalarprodukt $\Rightarrow$ Norm $\Rightarrow$ Metrik — die gesamte metrische Geometrie folgt aus dem Skalarprodukt.

---

<a id="beweise-6"></a>
## Beweise

> **Klausurrelevant in voller Tiefe:** **Cauchy-Schwarz (6.13)** und die Dreiecksungleichung (N2) in Satz 6.14 — beide sind Standard-Beweisaufgaben.

<a id="beweis-von-lemma-610-vge0-beweisstil-direkt"></a>
### Beweis von Lemma 6.10 ($\|v\|\ge0$) — *Beweisstil: direkt*

$$
0=\|0\|=\|v+(-v)\|\overset{\text{N2}}{\le}\|v\|+\|-v\|\overset{\text{N1}}{=}\|v\|+|-1|\,\|v\|=2\|v\|,
$$
also $\|v\|\ge0$. $\blacksquare$

<a id="beweis-von-lemma-612-norm-to-metrik-beweisstil-direkt-axiomcheck"></a>
### Beweis von Lemma 6.12 (Norm $\to$ Metrik) — *Beweisstil: direkt (Axiomcheck)*

$d(v,w)=\|v-w\|$. (M1): $\|v-w\|=|-1|\,\|w-v\|=\|w-v\|$. (M2): $\|v-z\|=\|(v-w)+(w-z)\|\le\|v-w\|+\|w-z\|$. (M3): $\|v-w\|=0\Leftrightarrow v-w=0\Leftrightarrow v=w$ (N3). $\blacksquare$

<a id="beweis-von-satz-613-cauchy-schwarz-beweisstil-optimierung-geschickte-wahl-von-a"></a>
### Beweis von Satz 6.13 (Cauchy-Schwarz) — *Beweisstil: Optimierung (geschickte Wahl von $a$)*

Ist $w=0$: $|\langle v,0\rangle|=0=\|v\|\cdot0$. ✓ Sei $w\neq0$, also $\langle w,w\rangle>0$. Für **jedes** $a\in k$ gilt wegen positiver Definitheit (Konvention: linear im 1., konjugiert-linear im 2. Argument):
$$
0\le\langle v-aw,\ v-aw\rangle=\langle v,v\rangle-a\langle w,v\rangle-\overline{a}\langle v,w\rangle+a\overline{a}\langle w,w\rangle.
$$
Setze $a=\dfrac{\langle v,w\rangle}{\langle w,w\rangle}$ (dann $\overline a=\dfrac{\langle w,v\rangle}{\langle w,w\rangle}$, da $\langle w,v\rangle=\overline{\langle v,w\rangle}$). Einsetzen und Zusammenfassen (mit $\langle v,w\rangle\langle w,v\rangle=|\langle v,w\rangle|^2$):
$$
0\le\langle v,v\rangle-\frac{|\langle v,w\rangle|^2}{\langle w,w\rangle}
\ \Longrightarrow\ |\langle v,w\rangle|^2\le\langle v,v\rangle\langle w,w\rangle=\|v\|^2\|w\|^2.
$$
Wurzelziehen: $|\langle v,w\rangle|\le\|v\|\|w\|$. **Gleichheit** tritt genau bei $v-aw=0$ auf, d. h. wenn $v,w$ linear abhängig sind. $\blacksquare$

<a id="beweis-von-satz-614-induzierte-norm-beweisstil-direkt-n2-via-cauchy-schwarz"></a>
### Beweis von Satz 6.14 (induzierte Norm) — *Beweisstil: direkt, N2 via Cauchy-Schwarz*

**(N1)** $\|av\|=\sqrt{\langle av,av\rangle}=\sqrt{a\overline a\langle v,v\rangle}=|a|\sqrt{\langle v,v\rangle}=|a|\,\|v\|$.
**(N3)** $\|v\|=0\Leftrightarrow\langle v,v\rangle=0\overset{\text{pos. def.}}{\Leftrightarrow}v=0$.
**(N2)** Mit $\langle v,w\rangle+\langle w,v\rangle=2\mathrm{Re}\langle v,w\rangle$:
$$
\|v+w\|^2=\langle v+w,v+w\rangle=\|v\|^2+\|w\|^2+2\mathrm{Re}\langle v,w\rangle
\le\|v\|^2+\|w\|^2+2|\langle v,w\rangle|
$$
$$
\overset{\text{C-S}}{\le}\|v\|^2+\|w\|^2+2\|v\|\|w\|=(\|v\|+\|w\|)^2.
$$
Wurzelziehen: $\|v+w\|\le\|v\|+\|w\|$. $\blacksquare$

---

<a id="algorithmen-6"></a>
## Algorithmen

<a id="verfahren-prüfen-ob-s-ein-skalarprodukt-ist"></a>
### Verfahren — Prüfen, ob $s$ ein Skalarprodukt ist

- **Motivation.** Klausur: „Zeigen Sie, dass $\langle\cdot,\cdot\rangle$ ein Skalarprodukt ist" oder „Für welche Parameter?".
- **Idee.** Drei Eigenschaften nachweisen: (bi/sesqui-)linear, symmetrisch/hermitesch, positiv definit.
- **Pseudocode.**
  ```
  Eingabe: s: V×V → k  (oder Matrix A mit s(x,y)=x^T A y bzw. x^T A ȳ)
  1. Linearität im 1. Argument prüfen (bei Matrix automatisch).
  2. Symmetrie:  A^T = A   (reell)      /   hermitesch: Ā^T = A  (komplex).
  3. Positiv definit prüfen:
       - Eigenwerte von A alle > 0,  ODER
       - Hauptminoren-Kriterium (Sylvester): alle führenden
         Hauptminoren > 0.
  return "Skalarprodukt" gdw. alle drei erfüllt.
  ```
- **Mathematische Beschreibung.** $s$ Skalarprodukt $\Leftrightarrow A$ symmetrisch/hermitesch **und** positiv definit.
- **Laufzeit.** Eigenwerte/Minoren $O(n^3)$.
- **Korrektheitsidee.** Ein Skalarprodukt entspricht genau einer positiv definiten symmetrischen/hermiteschen Matrix.
- **Typische Fehler.** Positive Definitheit vergessen (Symmetrie allein reicht nicht); Konjugation im komplexen Fall übersehen; nur $s(v,v)\ge0$ statt $>0$ für $v\neq0$.

---

<a id="beispiele-6"></a>
## Beispiele

**Beispiel 1 (leicht — Standardskalarprodukt).** Auf $\mathbb{R}^n$: $\langle x,y\rangle=\sum_i x_iy_i=x^{\mathsf T}y$. Auf $\mathbb{C}^n$: $\langle x,y\rangle=\sum_i x_i\overline{y_i}=x^{\mathsf T}\bar y$. Beide positiv definit ($\langle x,x\rangle=\sum|x_i|^2$).

**Beispiel 2 (mittel — gewichtetes Produkt).** Auf $\mathbb{R}^2$: $\langle x,y\rangle=2x_1y_1+3x_2y_2$, Matrix $A=\mathrm{diag}(2,3)$. Symmetrisch, Eigenwerte $2,3>0$ $\Rightarrow$ Skalarprodukt.

**Beispiel 3 (mittel — Integral-Skalarprodukt).** Auf $V=C([0,1],\mathbb{R})$ (stetige Funktionen):
$$
\langle f,g\rangle=\int_0^1 f(t)g(t)\,dt.
$$
Positiv definit ($\langle f,f\rangle=\int f^2>0$ für $f\neq0$ stetig). Dies ist ein **unendlichdimensionaler** euklidischer Raum — Grundlage der Fourier-Theorie ($\sin,\cos$ orthogonal).

**Beispiel 4 (mittel — Cauchy-Schwarz konkret).** Auf $\mathbb{R}^n$ ist $|\sum x_iy_i|\le\sqrt{\sum x_i^2}\sqrt{\sum y_i^2}$ — die klassische Cauchy-Schwarz-Summenungleichung.

**Beispiel 5 (schwer — Winkel im Funktionenraum).** In $C([0,1])$ mit obigem Produkt: der „Winkel" zwischen $f(t)=1$ und $g(t)=t$ ist
$$
\cos\angle(f,g)=\frac{\int_0^1 t\,dt}{\sqrt{\int_0^1 1}\sqrt{\int_0^1 t^2}}=\frac{1/2}{1\cdot 1/\sqrt3}=\frac{\sqrt3}{2}\ \Rightarrow\ \angle=30°.
$$

---

<a id="gegenbeispiele-6"></a>
## Gegenbeispiele

**Gegenbeispiel A (Bilinearform über $\mathbb{C}$ ist kein Skalarprodukt).** $s(x,y)=\sum x_iy_i$ (ohne Konjugation) auf $\mathbb{C}^n$: $s\big((i,0),(i,0)\big)=i^2=-1<0$. *Keine positive Definitheit* $\Rightarrow$ keine Länge. Deshalb **Sesquilinearität** über $\mathbb{C}$.

**Gegenbeispiel B (indefinite Form).** Die Minkowski-Form $s(x,y)=x_1y_1-x_2y_2$ auf $\mathbb{R}^2$ ist symmetrisch, aber $s\big((0,1),(0,1)\big)=-1<0$ — nicht positiv definit, also **kein** Skalarprodukt (wohl aber wichtig in der Relativitätstheorie).

**Gegenbeispiel C (Norm ohne Skalarprodukt).** Die $1$-Norm $\|x\|_1=\sum|x_i|$ und die Maximumsnorm $\|x\|_\infty=\max|x_i|$ sind Normen, kommen aber von **keinem** Skalarprodukt — sie verletzen die Parallelogrammgleichung (Kapitel 7). *Norm $\not\Rightarrow$ Skalarprodukt.*

**Gegenbeispiel D (Metrik ohne Norm).** Die **diskrete Metrik** $d(x,y)=1$ für $x\neq y$, $d(x,x)=0$ ist eine Metrik, aber nicht homogen ($d(2x,0)=1\neq2=|2|d(x,0)$) — kommt von keiner Norm. *Metrik $\not\Rightarrow$ Norm.*

---

<a id="typische-klausuraufgaben-6"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Woran erkennbar | Strategie |
|---|---|---|
| **Skalarprodukt nachweisen** | „Zeigen Sie, dass $\langle\cdot,\cdot\rangle$ ein Skalarprodukt ist." | Linearität, Symmetrie/Hermitizität, positive Definitheit. |
| **Parameteraufgabe** | „Für welche $t$ ist $A$ pos. definit?" | Eigenwerte/Hauptminoren $>0$. |
| **Cauchy-Schwarz beweisen** | „Beweisen Sie C-S." | $\langle v-aw,v-aw\rangle\ge0$, $a=\langle v,w\rangle/\langle w,w\rangle$. |
| **Dreiecksungleichung** | „Zeigen Sie $\|v+w\|\le\dots$" | $\|v+w\|^2$ ausschreiben, C-S. |
| **Länge/Abstand/Winkel** | „Berechnen Sie …" | induzierte Norm/Metrik/Winkelformel (euklidisch). |
| **Norm $\neq$ Skalarprodukt** | „Kommt $\|\cdot\|_1$ von einem Skalarprodukt?" | Parallelogrammgleichung testen (Kap. 7). |

---

<a id="typische-fehler-6"></a>
## Typische Fehler

| Fehler | Warum falsch | Richtig |
|---|---|---|
| Konjugation im komplexen Fall vergessen | $\langle x,x\rangle$ kann sonst negativ/komplex werden. | $\langle x,y\rangle=\sum x_i\overline{y_i}$. |
| positive Definitheit übersehen | Symmetrie allein macht kein Skalarprodukt. | $\langle v,v\rangle>0$ für $v\neq0$ **beweisen**. |
| Winkelformel im unitären Fall | $\langle v,w\rangle$ dann komplex, $\arccos$ undefiniert. | $\mathrm{Re}$ oder $|\cdot|$ verwenden; direkt nur euklidisch. |
| „Norm $\Rightarrow$ Skalarprodukt" | falsch (Gegenbeispiel C). | nur mit Parallelogrammgleichung. |
| $\|v\|$ und $\langle v,v\rangle$ verwechseln | $\|v\|=\sqrt{\langle v,v\rangle}$. | Quadrieren beachten. |
| C-S-Gleichheitsfall vergessen | Gleichheit $\Leftrightarrow$ linear abhängig. | im Beweis $v-aw=0$ notieren. |
| $\langle v,v\rangle\ge0$ ohne Hermitizität annehmen | nur bei hermitesch reell/positiv. | erst Hermitizität sichern. |

> **Vergleichstabelle: Bilinearform vs. Sesquilinearform.**
>
> | | Bilinearform (reell) | Sesquilinearform (komplex) |
> |---|---|---|
> | 1. Argument | linear | linear |
> | 2. Argument | linear | **konjugiert-linear** |
> | Symmetriebegriff | symmetrisch $s(v,w)=s(w,v)$ | hermitesch $s(v,w)=\overline{s(w,v)}$ |
> | $s(v,v)$ | reell | **reell** (bei hermitesch) |
> | Matrixkriterium | $A^{\mathsf T}=A$ | $A^*=\bar A^{\mathsf T}=A$ |
> | Skalarprodukt-Fall | pos. def. symmetrisch | pos. def. hermitesch |
>
> **Vergleichstabelle: Skalarprodukt / Norm / Metrik.**
>
> | | misst | Bedingungen | induziert |
> |---|---|---|---|
> | Skalarprodukt $\langle v,w\rangle$ | Länge **und** Winkel | linear, herm./symm., pos. def. | Norm |
> | Norm $\|v\|$ | Länge | N1–N3 | Metrik |
> | Metrik $d(x,y)$ | Abstand | M1–M3 | Topologie |

---

<a id="verbindungen-6"></a>
## Verbindungen

- **← Kapitel 5:** Die Konjugation (konjugiert-linear!) erzwingt Sesquilinearität; $z\bar z=|z|^2$ ist der Prototyp positiver Definitheit.
- **→ Kapitel 7:** Orthogonalität ($\langle v,w\rangle=0$), Pythagoras, Parallelogrammgleichung (Rückweg Norm $\to$ Skalarprodukt), orthogonale Projektion und Gram-Schmidt bauen direkt auf Cauchy-Schwarz und der induzierten Norm auf.
- **→ Kapitel 8:** Die adjungierte Abbildung $f^*$ ist über $\langle f(v),w\rangle=\langle v,f^*(w)\rangle$ definiert; $A^*=\bar A^{\mathsf T}$ nutzt die Konjugationskonvention dieses Kapitels; der Spektralsatz braucht positive Definitheit und Orthonormalbasen.
- **← Kapitel 2/4:** Positive Definitheit über Eigenwerte $>0$ verknüpft „Skalarprodukt" mit Eigenwerttheorie.

**Definitionen, die später ständig gebraucht werden:** $\langle v,w\rangle$, $\|v\|$, positiv definit, hermitesch, $A^*$, Cauchy-Schwarz.

---

<a id="zusammenfassung-6"></a>
## Zusammenfassung

| Kernaussage | Symbolisch |
|---|---|
| Skalarprodukt $=$ pos. def. symm./herm. (Sesqui-)Bilinearform. | $\langle v,v\rangle>0$ |
| Über $\mathbb{C}$ konjugiert-linear im 2. Argument. | $\langle v,aw\rangle=\bar a\langle v,w\rangle$ |
| hermitesch $\Rightarrow\langle v,v\rangle\in\mathbb{R}$. | — |
| Matrixkriterium: symm. $A^{\mathsf T}=A$ / herm. $A^*=A$. | — |
| **Cauchy-Schwarz:** $|\langle v,w\rangle|\le\|v\|\|w\|$. | (Satz 6.13) |
| Skalarprodukt $\to$ Norm $\to$ Metrik (einseitig). | $\|v\|=\sqrt{\langle v,v\rangle}$, $d=\|v-w\|$ |
| Rückwege nur mit Zusatzbedingung. | Parallelogr.-Gl. / Homogenität |

**Die eine Idee des Kapitels:** Ein Skalarprodukt verwandelt einen nackten Vektorraum in einen **Messraum** — mit Länge, Abstand und (euklidisch) Winkel. Über $\mathbb{C}$ ist die konjugierte Linearität im zweiten Argument kein Schönheitsfehler, sondern die Bedingung dafür, dass $\langle v,v\rangle$ reell und positiv ist. Cauchy-Schwarz ist der Angelpunkt, aus dem Dreiecksungleichung und Winkel folgen.



---

<a id="kapitel-7-orthogonalität-projektion-und-gram-schmidt"></a>
# Kapitel 7 — Orthogonalität, Projektion und Gram-Schmidt

> **Stellung im Kurs.** Kapitel 6 gab uns Länge, Abstand und Winkel. Jetzt ernten wir die
> geometrischen Früchte: **Orthogonalität** (rechte Winkel), das **orthogonale Komplement**
> ($V=U\oplus U^\perp$), die **orthogonale Projektion** als Bestapproximation (kleinste Quadrate)
> und das **Gram-Schmidt-Verfahren**, das aus jeder Basis eine Orthonormalbasis fabriziert.
> Orthonormalbasen machen Kapitel 8 (Spektralsätze) erst effizient.

---

<a id="motivation-7"></a>
## Motivation

Eine gewöhnliche Basis ist praktisch, aber „schief": Um Koordinaten zu bestimmen, muss man ein lineares Gleichungssystem lösen (Matrix invertieren). Eine **Orthonormalbasis** (ONB) beseitigt das komplett:
$$
v=\sum_i\langle v,b_i\rangle\,b_i,\qquad \|v\|^2=\sum_i|\langle v,b_i\rangle|^2.
$$
Die Koordinaten sind **einfach Skalarprodukte** — keine Inversion, keine Gleichungssysteme. Das ist der Grund, warum ONB überall bevorzugt werden.

**Drei Probleme, die dieses Kapitel löst:**

1. **Bestapproximation / kleinste Quadrate.** Gegeben ein Vektor $v$ und ein Unterraum $U$ (z. B. der Bildraum einer Messmatrix): Welcher Punkt in $U$ liegt $v$ am **nächsten**? Antwort: die **orthogonale Projektion** $\Pi_U(v)$. Das ist das Herz der linearen Regression.

2. **Zerlegung.** Jeder Vektor spaltet sich eindeutig in „Anteil in $U$" plus „Anteil senkrecht dazu": $V=U\oplus U^\perp$. Das entkoppelt Probleme in unabhängige Richtungen.

3. **ONB herstellen.** Man hat eine beliebige Basis, will aber die Bequemlichkeit einer ONB — **Gram-Schmidt** liefert sie konstruktiv.

**Mathematische/historische Wurzel.** Die Idee „senkrechte Zerlegung" ist uralt (Euklid). Gram (1883) und Schmidt (1907) formalisierten das Orthonormalisierungsverfahren. Die unendlichdimensionale Version ist die **Fourier-Reihe**: eine Funktion in orthonormale Schwingungen zerlegen.

---

<a id="intuition-7"></a>
## Intuition

**Orthogonal $=$ „kein gemeinsamer Anteil".** $v\perp w$ bedeutet: $v$ hat keine Komponente in Richtung $w$. Solche Vektoren sind „maximal unabhängig" — Unabhängigkeit in Reinform.

**Pythagoras $=$ „unabhängige Beiträge zur Länge addieren sich quadratisch".** Stehen $v,w$ senkrecht, ist $\|v+w\|^2=\|v\|^2+\|w\|^2$ — genau der Satz des Pythagoras, jetzt in beliebiger Dimension.

**Projektion $=$ „Lot fällen".** Um den nächsten Punkt eines Unterraums $U$ zu einem Vektor $v$ zu finden, fällt man das **Lot** von $v$ auf $U$. Der Fußpunkt ist $\Pi_U(v)$; der Abstand $\|v-\Pi_U(v)\|$ ist minimal, und der Fehler $v-\Pi_U(v)$ steht **senkrecht** auf $U$.

```
        v
        │╲
        │ ╲  v − Π_U(v)  ⟂ U   (Fehler senkrecht)
        │  ╲
  ──────┼───•────────  U
        Π_U(v)   (nächster Punkt in U)
```

**Gram-Schmidt $=$ „Basis geraderücken".** Man nimmt die Basisvektoren nacheinander und **entfernt bei jedem den Anteil, der schon von den vorherigen abgedeckt ist** (durch Abziehen der Projektion). Was übrig bleibt, steht senkrecht auf allem Vorherigen. Danach auf Länge $1$ normieren. Bild: eine schiefe Basis wird Schritt für Schritt in ein rechtwinkliges Achsenkreuz verwandelt.

---

<a id="formale-definitionen-7"></a>
## Formale Definitionen

Sei $V$ euklidisch oder unitär mit Skalarprodukt $\langle\cdot,\cdot\rangle$ und induzierter Norm $\|\cdot\|$.

**Definition 7.1 (Orthogonalität).**
$v,w\in V$ heißen **orthogonal** ($v\perp w$), falls $\langle v,w\rangle=0$. Es gilt $v\perp w\Leftrightarrow w\perp v$ (denn $\langle v,w\rangle=0\Leftrightarrow\langle w,v\rangle=\overline{\langle v,w\rangle}=0$).

**Definition 7.2 (orthogonale/orthonormale Menge).**
Eine Teilmenge $M\subseteq V$ heißt
- **orthogonal**, falls $v\perp w$ für alle $v\neq w$ aus $M$ und $0\notin M$;
- **orthonormal**, falls sie orthogonal ist und zusätzlich $\|v\|=1$ (d. h. $\langle v,v\rangle=1$) für alle $v\in M$.

**Definition 7.3 (Orthogonal-/Orthonormalbasis).**
Eine Basis von $V$ heißt **Orthogonalbasis**, wenn sie orthogonal ist, und **Orthonormalbasis (ONB)**, wenn sie orthonormal ist.

**Definition 7.4 (orthogonales Komplement).**
Für $M\subseteq V$:
$$
M^\perp:=\{w\in V\mid \langle w,v\rangle=0\ \forall v\in M\}=\{w\in V\mid w\perp v\ \forall v\in M\}.
$$
$M^\perp$ ist stets ein **Unterraum**. Für $M=\mathrm{span}(v_1,\dots,v_m)$ gilt $M^\perp=\bigcap_i v_i^\perp$.

**Definition 7.5 (orthogonale Projektion).**
Sei $U\subseteq V$ ein endlichdimensionaler Unterraum. Die **orthogonale Projektion** $\Pi_U\colon V\to U$ ist die lineare Abbildung mit
$$
\Pi_U(u+u')=u\quad\text{für }u\in U,\ u'\in U^\perp
$$
(wohldefiniert, da $V=U\oplus U^\perp$, Satz 7.12). Es gilt $\ker(\Pi_U)=U^\perp$.

---

<a id="eigenschaften-7"></a>
## Eigenschaften

| Eigenschaft | Aussage | Kurzbegründung |
|---|---|---|
| **$0\perp$ alles** | $\langle 0,v\rangle=0$ | Linearität. |
| **orthogonal $\Rightarrow$ lin. unabh.** | orthogonale Menge (ohne $0$) ist lin. unabh. | Lemma 7.9. |
| **Normieren** | $v\neq0\Rightarrow\|\tfrac{1}{\|v\|}v\|=1$ | N1. |
| **$M^\perp$ Unterraum** | abgeschlossen unter $+,\cdot$ | Linearität von $\langle\cdot,v\rangle$. |
| **$U\cap U^\perp=\{0\}$** | für jeden Unterraum | $v\in$ beide $\Rightarrow\langle v,v\rangle=0\Rightarrow v=0$. |
| **$V=U\oplus U^\perp$** | endlichdim. $U$ | Satz 7.12. |
| **$\Pi_U$ idempotent** | $\Pi_U\circ\Pi_U=\Pi_U$ | $\Pi_U$ fixiert $U$. |
| **ONB-Koordinaten** | $v=\sum\langle v,b_i\rangle b_i$ | Lemma 7.14. |
| **Parseval** | $\|v\|^2=\sum|\langle v,b_i\rangle|^2$ | Pythagoras über ONB. |

---

<a id="sätze-7"></a>
## Sätze

<a id="satz-76-längenformel-und-pythagoras"></a>
### Satz 7.6 (Längenformel und Pythagoras)

**Aussage.** Für $v,w\in V$: $\;\|v+w\|^2=\|v\|^2+\|w\|^2+\langle v,w\rangle+\langle w,v\rangle=\|v\|^2+\|w\|^2+2\mathrm{Re}\langle v,w\rangle.$
**Korollar (Pythagoras).** Ist $v\perp w$, so $\|v+w\|^2=\|v\|^2+\|w\|^2$.
**Bedeutung.** Verknüpft Skalarprodukt und Länge; Grundlage der Bestapproximation.

<a id="satz-77-parallelogrammgleichung"></a>
### Satz 7.7 (Parallelogrammgleichung)

**Aussage.** $\;\|v+w\|^2+\|v-w\|^2=2\|v\|^2+2\|w\|^2.$
**Bedeutung.** Charakterisiert Normen, die von einem Skalarprodukt kommen (Jordan–von Neumann): Eine Norm stammt genau dann aus einem Skalarprodukt, wenn sie diese Gleichung erfüllt. Das liefert den in Kapitel 6 erwähnten „Rückweg".

<a id="satz-78-satz-des-thales"></a>
### Satz 7.8 (Satz des Thales)

**Aussage.** In einem **euklidischen** Raum gilt für $v,w$ mit $\|v\|=\|w\|$: $\;(v+w)\perp(v-w)$.
**Voraussetzungen.** euklidisch (reelles, symmetrisches Produkt).
**Intuition.** Der Winkel im Halbkreis (Durchmesserwinkel) ist ein rechter Winkel.

<a id="lemma-79-orthogonal-rightarrow-linear-unabhängig"></a>
### Lemma 7.9 (orthogonal $\Rightarrow$ linear unabhängig)

**Aussage.** Eine orthogonale Menge $\{v_1,\dots,v_m\}$ (alle $\neq0$) ist linear unabhängig.
**Bedeutung.** ONB sind automatisch Basen; „senkrecht" ist die stärkste Form von „unabhängig".

<a id="satz-710-normierung-lemma-315"></a>
### Satz 7.10 (Normierung, Lemma 3.15)

**Aussage.** Für $v\neq0$ ist $\tfrac{1}{\|v\|}v$ ein Einheitsvektor in Richtung $v$.
**Bedeutung.** Macht aus Orthogonalbasen Orthonormalbasen.

<a id="satz-711-orthogonales-komplement-von-erzeugnissen"></a>
### Satz 7.11 (orthogonales Komplement von Erzeugnissen)

**Aussage.** Ist $M=\mathrm{span}(v_1,\dots,v_m)$, so $M^\perp=\bigcap_{i=1}^m v_i^\perp$. Ferner $(U^\perp)^\perp=U$ für endlichdim. $U$.
**Bedeutung.** Reduziert das Berechnen von $U^\perp$ auf ein lineares Gleichungssystem.

<a id="satz-712-orthogonale-zerlegung-zentral"></a>
### Satz 7.12 (Orthogonale Zerlegung) — *zentral*

**Aussage.** Ist $V$ endlichdimensional (oder $U$ endlichdim.), $U\subseteq V$ Unterraum, so
$$
V=U\oplus U^\perp.
$$
**Voraussetzungen.** $U$ endlichdimensional. **Achtung:** im Unendlichdimensionalen kann $U\oplus U^\perp=V$ **scheitern**.
**Bedeutung.** Jeder Vektor spaltet sich eindeutig in „$U$-Anteil" $+$ „senkrechter Anteil"; macht $\Pi_U$ wohldefiniert.
**Intuition.** $V$ zerfällt in zwei zueinander senkrechte „Achsengruppen".

<a id="satz-713-orthogonale-projektion-und-bestapproximation-herzstück"></a>
### Satz 7.13 (orthogonale Projektion und Bestapproximation) — *Herzstück*

**Aussage.** Für $v\in V$ gilt:
(a) $\Pi_U(v)=u\Leftrightarrow v-u\in U^\perp$ (Charakterisierung);
(b) **Bestapproximation:** für alle $u\in U$ ist $\;d(v,u)\ge d(v,\Pi_U(v))$, mit Gleichheit $\Leftrightarrow u=\Pi_U(v)$.
**Bedeutung.** $\Pi_U(v)$ ist der **eindeutige nächste Punkt** in $U$ zu $v$ — die geometrische Grundlage der kleinsten Quadrate.
**Intuition.** Der Fehler steht senkrecht auf $U$; jeder andere Punkt ist per Pythagoras weiter weg.

<a id="lemma-714-projektionsformel-via-onb"></a>
### Lemma 7.14 (Projektionsformel via ONB)

**Aussage.** Ist $\{b_1,\dots,b_m\}$ eine ONB von $U$, so
$$
\Pi_U(v)=\sum_{i=1}^m\langle v,b_i\rangle\,b_i.
$$
Für $U=V$: $\;v=\sum_i\langle v,b_i\rangle b_i$ und $\|v\|^2=\sum_i|\langle v,b_i\rangle|^2$ (**Parseval**).
**Bedeutung.** Mit einer ONB sind Projektion und Koordinaten reine Skalarprodukte.

<a id="satz-715-gram-schmidt-orthonormalisierung-zentraler-algorithmus"></a>
### Satz 7.15 (Gram-Schmidt-Orthonormalisierung) — *zentraler Algorithmus*

**Aussage.** Sei $\{b_1,\dots,b_n\}$ eine Basis von $V$. Dann gibt es eine ONB $\{b_1',\dots,b_n'\}$ mit
$$
\mathrm{span}(b_1',\dots,b_j')=\mathrm{span}(b_1,\dots,b_j)\qquad\text{für alle }j=1,\dots,n.
$$
**Bedeutung.** Jeder endlichdim. Skalarproduktraum hat eine ONB, konstruktiv erzeugbar. Die „Stufenbedingung" (gleiche Teilräume) ist wichtig für QR-Zerlegung und Beweise.

---

<a id="beweise-7"></a>
## Beweise

> **Klausurrelevant in voller Tiefe:** Pythagoras (7.6), Lemma 7.9, **Satz 7.12**, **Bestapproximation 7.13**, Projektionsformel 7.14, **Gram-Schmidt 7.15**.

<a id="beweis-von-satz-76-längenformel-beweisstil-direkt-ausmultiplizieren"></a>
### Beweis von Satz 7.6 (Längenformel) — *Beweisstil: direkt (Ausmultiplizieren)*

$$
\|v+w\|^2=\langle v+w,v+w\rangle=\langle v,v\rangle+\langle v,w\rangle+\langle w,v\rangle+\langle w,w\rangle=\|v\|^2+\|w\|^2+2\mathrm{Re}\langle v,w\rangle.
$$
Ist $v\perp w$, verschwinden die Mischterme: $\|v+w\|^2=\|v\|^2+\|w\|^2$. $\blacksquare$

<a id="beweis-von-satz-77-parallelogramm-beweisstil-direkt"></a>
### Beweis von Satz 7.7 (Parallelogramm) — *Beweisstil: direkt*

$$
\|v+w\|^2+\|v-w\|^2=\big(\|v\|^2+\|w\|^2+2\mathrm{Re}\langle v,w\rangle\big)+\big(\|v\|^2+\|w\|^2-2\mathrm{Re}\langle v,w\rangle\big)=2\|v\|^2+2\|w\|^2.\ \blacksquare
$$

<a id="beweis-von-satz-78-thales-euklidisch-beweisstil-direkt"></a>
### Beweis von Satz 7.8 (Thales, euklidisch) — *Beweisstil: direkt*

$\langle v+w,v-w\rangle=\langle v,v\rangle-\langle v,w\rangle+\langle w,v\rangle-\langle w,w\rangle=\|v\|^2-\|w\|^2=0$, da $\|v\|=\|w\|$ (im euklidischen Fall $\langle v,w\rangle=\langle w,v\rangle$). Also $(v+w)\perp(v-w)$. $\blacksquare$

<a id="beweis-von-lemma-79-orthogonal-rightarrow-unabhängig-beweisstil-direkt"></a>
### Beweis von Lemma 7.9 (orthogonal $\Rightarrow$ unabhängig) — *Beweisstil: direkt*

Sei $\sum_i a_iv_i=0$. Bilde $\langle\cdot,v_j\rangle$:
$$
0=\Big\langle\sum_i a_iv_i,\ v_j\Big\rangle=\sum_i a_i\langle v_i,v_j\rangle=a_j\langle v_j,v_j\rangle,
$$
da $\langle v_i,v_j\rangle=0$ für $i\neq j$. Wegen $v_j\neq0$ ist $\langle v_j,v_j\rangle>0$, also $a_j=0$. Für alle $j$. $\blacksquare$

<a id="beweis-von-satz-712-vuoplus-uperp-beweisstil-konstruktion-via-onb-schnitt"></a>
### Beweis von Satz 7.12 ($V=U\oplus U^\perp$) — *Beweisstil: Konstruktion via ONB $+$ Schnitt*

**$U\cap U^\perp=\{0\}$:** $v\in U\cap U^\perp\Rightarrow\langle v,v\rangle=0\Rightarrow v=0$ (positive Definitheit).
**$V=U+U^\perp$:** Wähle (Gram-Schmidt) eine ONB $\{b_1,\dots,b_m\}$ von $U$. Für $v\in V$ setze $u:=\sum_{i=1}^m\langle v,b_i\rangle b_i\in U$. Dann gilt für jedes $j$:
$$
\langle v-u,b_j\rangle=\langle v,b_j\rangle-\sum_i\langle v,b_i\rangle\langle b_i,b_j\rangle=\langle v,b_j\rangle-\langle v,b_j\rangle=0,
$$
also $v-u\perp U$, d. h. $v-u\in U^\perp$. Damit $v=u+(v-u)\in U+U^\perp$. Zusammen mit dem trivialen Schnitt folgt die direkte Summe. $\blacksquare$

<a id="beweis-von-satz-713-bestapproximation-beweisstil-pythagoras"></a>
### Beweis von Satz 7.13 (Bestapproximation) — *Beweisstil: Pythagoras*

(a) folgt aus der Definition von $\Pi_U$ und $V=U\oplus U^\perp$.
(b) Sei $u\in U$ beliebig. Zerlege $v-u=\underbrace{(v-\Pi_U(v))}_{\in U^\perp}+\underbrace{(\Pi_U(v)-u)}_{\in U}$. Die beiden Summanden stehen senkrecht, also (Pythagoras 7.6):
$$
\|v-u\|^2=\|v-\Pi_U(v)\|^2+\|\Pi_U(v)-u\|^2\ge\|v-\Pi_U(v)\|^2.
$$
Gleichheit genau bei $\Pi_U(v)-u=0$, also $u=\Pi_U(v)$. $\blacksquare$

<a id="beweis-von-lemma-714-projektionsformel-beweisstil-direkt-charakterisierung-713a"></a>
### Beweis von Lemma 7.14 (Projektionsformel) — *Beweisstil: direkt (Charakterisierung 7.13a)*

Setze $u=\sum_i\langle v,b_i\rangle b_i\in U$. Wie im Beweis von 7.12 gilt $\langle v-u,b_j\rangle=0$ für alle $j$, also $v-u\in U^\perp$; nach 7.13(a) ist $u=\Pi_U(v)$. Die Parseval-Gleichung folgt aus $\|v\|^2=\langle v,v\rangle=\sum_{i,j}\langle v,b_i\rangle\overline{\langle v,b_j\rangle}\langle b_i,b_j\rangle=\sum_i|\langle v,b_i\rangle|^2$. $\blacksquare$

<a id="beweis-von-satz-715-gram-schmidt-beweisstil-induktion-mit-projektion"></a>
### Beweis von Satz 7.15 (Gram-Schmidt) — *Beweisstil: Induktion mit Projektion*

Konstruiere induktiv. Setze $V_j:=\mathrm{span}(b_1,\dots,b_j)$ und $b_1':=\tfrac{1}{\|b_1\|}b_1$. Für $j\ge2$ ziehe von $b_j$ die Projektion auf $V_{j-1}$ ab:
$$
w_j:=b_j-\Pi_{V_{j-1}}(b_j)=b_j-\sum_{i=1}^{j-1}\langle b_j,b_i'\rangle\,b_i',\qquad b_j':=\frac{1}{\|w_j\|}w_j.
$$
**$w_j\neq0$:** Wäre $w_j=0$, läge $b_j=\Pi_{V_{j-1}}(b_j)\in V_{j-1}=\mathrm{span}(b_1,\dots,b_{j-1})$ — Widerspruch zur linearen Unabhängigkeit. Also $\|w_j\|>0$.
**$b_j'\perp b_i'$ für $i<j$:** $\langle w_j,b_i'\rangle=\langle b_j,b_i'\rangle-\langle b_j,b_i'\rangle=0$ (nach 7.14).
**Norm $1$ und Spanngleichheit:** $\|b_j'\|=1$ per Konstruktion; da $b_j'$ eine Linearkombination von $b_1,\dots,b_j$ ist und umgekehrt, gilt $\mathrm{span}(b_1',\dots,b_j')=V_j$. Somit ist $\{b_1',\dots,b_n'\}$ orthonormal (Lemma 7.9: linear unabhängig) und Basis. $\blacksquare$

---

<a id="algorithmen-7"></a>
## Algorithmen

<a id="algorithmus-gram-schmidt-orthonormalisierung"></a>
### Algorithmus — Gram-Schmidt-Orthonormalisierung

- **Motivation.** Die häufigste Rechenaufgabe in Teil III; liefert ONB, QR-Zerlegung, Projektionsbasen.
- **Idee.** Jeden Vektor „senkrecht machen", indem man die bereits abgedeckten Anteile abzieht, dann normieren.
- **Voraussetzungen.** $\{b_1,\dots,b_n\}$ **linear unabhängig** (sonst Division durch $0$).
- **Pseudocode.**
  ```
  Eingabe: Basis b_1,…,b_n
  b_1' ← b_1 / ‖b_1‖
  für j = 2,…,n:
      w ← b_j
      für i = 1,…,j−1:
          w ← w − ⟨b_j, b_i'⟩ · b_i'      # Projektionsanteil abziehen
      b_j' ← w / ‖w‖                        # normieren
  Ausgabe: ONB b_1',…,b_n'
  ```
- **Mathematische Beschreibung.** $w_j=b_j-\sum_{i<j}\langle b_j,b_i'\rangle b_i'$, $b_j'=w_j/\|w_j\|$; erhält $\mathrm{span}(b_1,\dots,b_j)$.
- **Laufzeit.** $O(n^2 d)$ Operationen ($d=\dim V$; $n$ Vektoren, je $O(n)$ Projektionen à $O(d)$).
- **Speicherbedarf.** $O(nd)$.
- **Korrektheitsidee.** Satz 7.15 (Induktion; $w_j\neq0$ wegen Unabhängigkeit).
- **Anwendungen.** ONB konstruieren; QR-Zerlegung $A=QR$; kleinste Quadrate; Beweis $V=U\oplus U^\perp$.
- **Typische Fehler.** Bei nicht-orthonormalem $b_i'$ die Formel verwenden (nur mit **normierten** $b_i'$ korrekt); Konjugation im komplexen Fall vergessen ($\langle b_j,b_i'\rangle$, nicht $\langle b_i',b_j\rangle$); Reihenfolge der Abzüge (alle vorherigen $i<j$).

> **Numerische Bemerkung.** Das obige „klassische" Gram-Schmidt ist numerisch instabil; die Variante **modifiziertes Gram-Schmidt** (Projektionen sofort nacheinander abziehen) ist stabiler. Für Klausuren spielt das keine Rolle.

<a id="algorithmus-orthogonale-projektion-bestapproximation"></a>
### Algorithmus — Orthogonale Projektion / Bestapproximation

- **Idee.** ONB von $U$ per Gram-Schmidt, dann $\Pi_U(v)=\sum\langle v,b_i\rangle b_i$.
- **Pseudocode.**
  ```
  Eingabe: Unterraum U (Basis), Vektor v
  {b_1,…,b_m} ← Gram-Schmidt(Basis von U)
  Π ← Σ_i ⟨v, b_i⟩ · b_i
  Abstand ← ‖v − Π‖
  ```
- **Anwendungen.** Kleinste Quadrate (Regressionsgerade $=$ Projektion auf Spaltenraum).
- **Typische Fehler.** Projektionsformel mit nicht-orthonormaler Basis; $U^\perp$-Anteil nicht abziehen.

---

<a id="beispiele-7"></a>
## Beispiele

**Beispiel 1 (leicht — Pythagoras).** In $\mathbb{R}^2$: $v=(3,0)\perp w=(0,4)$, $\|v+w\|^2=25=9+16=\|v\|^2+\|w\|^2$. ✓

**Beispiel 2 (mittel — ONB-Koordinaten).** ONB $b_1=\tfrac{1}{\sqrt2}(1,1)$, $b_2=\tfrac{1}{\sqrt2}(1,-1)$ von $\mathbb{R}^2$. Für $v=(3,1)$: $\langle v,b_1\rangle=\tfrac{4}{\sqrt2}=2\sqrt2$, $\langle v,b_2\rangle=\tfrac{2}{\sqrt2}=\sqrt2$. Probe: $2\sqrt2\,b_1+\sqrt2\,b_2=(2,2)+(1,-1)=(3,1)$. ✓ Parseval: $8+2=10=\|v\|^2$. ✓

**Beispiel 3 (schwer — Gram-Schmidt in $\mathbb{R}^3$, vollständig).** Basis $b_1=(1,1,0)$, $b_2=(1,0,1)$, $b_3=(0,1,1)$, Standardprodukt.

*Schritt 1:* $\|b_1\|=\sqrt2$, $b_1'=\tfrac{1}{\sqrt2}(1,1,0)$.

*Schritt 2:* $\langle b_2,b_1'\rangle=\tfrac{1}{\sqrt2}$, also
$$
w_2=b_2-\tfrac{1}{\sqrt2}b_1'=(1,0,1)-\tfrac12(1,1,0)=(\tfrac12,-\tfrac12,1),\quad \|w_2\|=\sqrt{\tfrac32}=\tfrac{\sqrt6}{2},\quad b_2'=\tfrac{1}{\sqrt6}(1,-1,2).
$$

*Schritt 3:* $\langle b_3,b_1'\rangle=\tfrac{1}{\sqrt2}$, $\langle b_3,b_2'\rangle=\tfrac{1}{\sqrt6}$, also
$$
w_3=(0,1,1)-\tfrac12(1,1,0)-\tfrac16(1,-1,2)=(-\tfrac23,\tfrac23,\tfrac23),\quad \|w_3\|=\tfrac{2}{\sqrt3},\quad b_3'=\tfrac{1}{\sqrt3}(-1,1,1).
$$

*Probe:* $\langle b_1',b_2'\rangle=\langle b_1',b_3'\rangle=\langle b_2',b_3'\rangle=0$. ✓ Die $b_i'$ bilden eine ONB von $\mathbb{R}^3$.

**Beispiel 4 (mittel — Projektion / kleinste Quadrate).** $U=\mathrm{span}\{(1,1,0)\}$ in $\mathbb{R}^3$, $v=(2,0,3)$. ONB von $U$: $b_1=\tfrac{1}{\sqrt2}(1,1,0)$. $\langle v,b_1\rangle=\tfrac{2}{\sqrt2}=\sqrt2$, also $\Pi_U(v)=\sqrt2\,b_1=(1,1,0)$. Abstand $\|v-\Pi_U(v)\|=\|(1,-1,3)\|=\sqrt{11}$.

**Beispiel 5 (schwer — Fourier-Idee).** In $C([-\pi,\pi])$ mit $\langle f,g\rangle=\int_{-\pi}^\pi fg\,dt$ sind $\{1,\cos t,\sin t,\cos2t,\dots\}$ paarweise orthogonal. Die orthogonale Projektion einer Funktion auf $\mathrm{span}$ endlich vieler dieser Funktionen ist ihre **Fourier-Partialsumme** — die beste trigonometrische Approximation (Bestapproximation!).

---

<a id="gegenbeispiele-7"></a>
## Gegenbeispiele

**Gegenbeispiel A (orthogonal $\neq$ orthonormal).** $\{(2,0),(0,3)\}$ ist orthogonal, aber nicht orthonormal ($\|(2,0)\|=2\neq1$). Die Projektionsformel $\Pi_U(v)=\sum\langle v,b_i\rangle b_i$ gilt **nur** für ONB; mit dieser Menge müsste man durch $\|b_i\|^2$ teilen.

**Gegenbeispiel B ($V=U\oplus U^\perp$ scheitert unendlichdim.).** Sei $V=\{$Folgen $(a_i)$ mit $\sum a_i^2<\infty\}$ ($\ell^2$), $\langle a,b\rangle=\sum a_ib_i$. $U=\{$Folgen mit nur endlich vielen $a_i\neq0\}$. Dann ist $U^\perp=\{0\}$ (eine Folge senkrecht zu allen $e_i$ ist $0$), also $U\oplus U^\perp=U\neq V$. *$U$ ist nicht abgeschlossen.* Satz 7.12 braucht $U$ endlichdimensional.

**Gegenbeispiel C (linear unabhängig $\neq$ orthogonal).** $\{(1,0),(1,1)\}$ ist eine Basis, aber nicht orthogonal ($\langle\cdot\rangle=1$). Deshalb braucht man Gram-Schmidt.

**Gegenbeispiel D (Gram-Schmidt bricht bei Abhängigkeit).** Für $b_1=(1,0)$, $b_2=(2,0)$ ist $w_2=b_2-\langle b_2,b_1'\rangle b_1'=(2,0)-2(1,0)=0$ — Division durch $\|w_2\|=0$. *Eingabe muss linear unabhängig sein.*

---

<a id="typische-klausuraufgaben-7"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Woran erkennbar | Strategie |
|---|---|---|
| **Gram-Schmidt** | „Orthonormalisieren Sie …" | Schritt für Schritt; Projektionen abziehen, normieren; Probe. |
| **Projektion / Abstand** | „Nächster Punkt in $U$ / Abstand von $v$ zu $U$." | ONB von $U$, Projektionsformel, $\|v-\Pi_U(v)\|$. |
| **$U^\perp$ bestimmen** | „Berechnen Sie das orthogonale Komplement." | LGS $\langle w,v_i\rangle=0$ lösen (Satz 7.11). |
| **ONB verifizieren** | „Zeigen Sie, dass … ONB ist." | paarweise $\langle b_i,b_j\rangle=\delta_{ij}$. |
| **Pythagoras/Parallelogramm** | „Beweisen Sie …" | Längenformel ausschreiben. |
| **kleinste Quadrate** | „Regressionsgerade / beste Näherung." | Projektion auf Spaltenraum. |

---

<a id="typische-fehler-7"></a>
## Typische Fehler

| Fehler | Warum falsch | Richtig |
|---|---|---|
| Projektionsformel mit nicht-ONB | $\sum\langle v,b_i\rangle b_i$ gilt nur orthonormal. | erst ONB (Gram-Schmidt) oder durch $\|b_i\|^2$ teilen. |
| Normieren vergessen | Orthogonalbasis $\neq$ ONB. | jeden $w_j$ auf Länge $1$ bringen. |
| Konjugation im komplexen Fall | $\langle b_j,b_i'\rangle$ statt $\langle b_i',b_j\rangle$. | Konvention aus Kap. 6 beachten. |
| $V=U\oplus U^\perp$ unendlichdim. angenommen | scheitert (Gegenbeispiel B). | $U$ endlichdim. voraussetzen. |
| Thales im unitären Fall | Beweis nutzt $\langle v,w\rangle=\langle w,v\rangle$. | nur euklidisch. |
| Gram-Schmidt bei Abhängigkeit | Division durch $0$. | Eingabe muss Basis (unabhängig) sein. |
| beim Abziehen nur den letzten Anteil | man muss **alle** $i<j$ abziehen. | Summe über alle vorherigen $b_i'$. |

> **Vergleichstabelle: Orthogonal vs. Orthonormal vs. „nur Basis".**
>
> | | linear unabhängig? | paarweise $\perp$? | $\|b_i\|=1$? | Projektionsformel gilt? |
> |---|---|---|---|---|
> | beliebige Basis | ✓ | ✗ | ✗ | nein (LGS lösen) |
> | Orthogonalbasis | ✓ | ✓ | ✗ | mit $/\|b_i\|^2$ |
> | Orthonormalbasis | ✓ | ✓ | ✓ | ja: $\sum\langle v,b_i\rangle b_i$ |

---

<a id="verbindungen-7"></a>
## Verbindungen

- **← Kapitel 6:** Cauchy-Schwarz garantiert die Dreiecksungleichung; die induzierte Norm liefert „Abstand", ohne den Bestapproximation sinnlos wäre. Die Parallelogrammgleichung (7.7) ist der Rückweg Norm $\to$ Skalarprodukt.
- **→ Kapitel 8:** ONB (Gram-Schmidt) sind die Basis, in der die adjungierte Matrix $A^*=\bar A^{\mathsf T}$ und der Spektralsatz sauber funktionieren; $V=U\oplus U^\perp$ trägt den Induktionsschritt im Spektralsatz-Beweis (Einschränkung auf $U^\perp$).
- **← Kapitel 2/4:** Orthogonale Projektionen sind spezielle diagonalisierbare Abbildungen ($\Pi_U^2=\Pi_U$, Eigenwerte $0,1$).

**Definitionen, die später ständig gebraucht werden:** $\perp$, ONB, $U^\perp$, $V=U\oplus U^\perp$, $\Pi_U$, Gram-Schmidt.

---

<a id="zusammenfassung-7"></a>
## Zusammenfassung

| Kernaussage | Symbolisch |
|---|---|
| Orthogonal $\Rightarrow$ Pythagoras. | $\|v+w\|^2=\|v\|^2+\|w\|^2$ |
| Orthogonal (ohne $0$) $\Rightarrow$ linear unabhängig. | (Lemma 7.9) |
| Endlichdim.: $V=U\oplus U^\perp$. | (Satz 7.12) |
| Projektion $=$ Bestapproximation; Fehler $\perp U$. | (Satz 7.13) |
| ONB-Koordinaten sind Skalarprodukte (Parseval). | $v=\sum\langle v,b_i\rangle b_i$ |
| Gram-Schmidt liefert ONB (spannenerhaltend). | (Satz 7.15) |
| Parallelogrammgleichung $\Leftrightarrow$ Norm aus Skalarprodukt. | (Satz 7.7) |

**Die eine Idee des Kapitels:** Orthogonalität macht Geometrie **berechenbar**. Eine ONB reduziert Koordinaten auf Skalarprodukte, die orthogonale Projektion löst das Bestapproximationsproblem (kleinste Quadrate), und Gram-Schmidt stellt die dafür nötige ONB aus jeder Basis her. Der rote Faden — „Fehler senkrecht $=$ minimal" — trägt von Pythagoras bis zur Fourier-Analyse.



---

<a id="kapitel-8-isometrien-adjungierte-abbildungen-und-spektralsätze"></a>
# Kapitel 8 — Isometrien, adjungierte Abbildungen und Spektralsätze

> **Stellung im Kurs.** Das Finale. Hier verschmelzen beide Kurshälften: die Eigenwerttheorie aus
> Teil I und die Skalarproduktgeometrie aus Teil III. Die **adjungierte Abbildung** $f^*$ ist der
> „richtig gemachte" transponierte Operator; **selbstadjungierte** und **normale** Operatoren sind
> die schönsten überhaupt; und der **Spektralsatz** krönt alles: Ein Operator besitzt genau dann
> eine **orthonormale Eigenbasis**, wenn er normal ist. Das ist die perfekte Diagonalisierung —
> Diagonalität *plus* rechte Winkel.

---

<a id="motivation-8"></a>
## Motivation

Zwei Fragen treiben dieses Kapitel:

1. **Welche linearen Abbildungen erhalten die Geometrie?** Also Längen, Abstände, Winkel? Das sind die **Isometrien** — die „starren Bewegungen" (Drehungen, Spiegelungen). Sie bilden die **orthogonale** bzw. **unitäre Gruppe** und sind die Symmetrien des Skalarproduktraums.

2. **Welche Operatoren lassen sich *orthonormal* diagonalisieren?** Kapitel 2 fragte „diagonalisierbar?", ignorierte aber die Geometrie. Jetzt wollen wir eine **Orthonormalbasis** aus Eigenvektoren — perpendikuläre Hauptachsen, entlang derer $f$ nur streckt. Die überraschend saubere Antwort (Spektralsatz): **genau die normalen Operatoren**.

**Das Werkzeug dazu — die Adjungierte.** Über die Definition $\langle f(v),w\rangle=\langle v,f^*(w)\rangle$ „schiebt" man $f$ von einem Argument des Skalarprodukts ins andere. In Matrixform ist $f^*$ einfach die **konjugiert-transponierte** Matrix $A^*=\bar A^{\mathsf T}$. Mit ihr definieren sich die zentralen Klassen:
$$
\textbf{selbstadjungiert: } f^*=f,\qquad \textbf{normal: } f\circ f^*=f^*\circ f,\qquad \textbf{isometrisch: } f^*=f^{-1}.
$$

**Warum das wichtig ist.** Selbstadjungierte Operatoren modellieren **Observablen** der Quantenmechanik (reelle Messwerte $=$ reelle Eigenwerte), **quadratische Formen** (Hauptachsentransformation), **Trägheitstensoren**, **Kovarianzmatrizen** (PCA/Hauptkomponentenanalyse). Der Spektralsatz ist eines der meistbenutzten Resultate der angewandten Mathematik.

**Mathematische Wurzel.** Die Konjugation aus Kapitel 5 ($A^*=\bar A^{\mathsf T}$) und die ONB aus Kapitel 7 sind die Zutaten. Der Fundamentalsatz der Algebra (Kap. 5) liefert im Beweis den nötigen Eigenwert.

---

<a id="intuition-8"></a>
## Intuition

**Isometrie $=$ starre Bewegung.** Eine Isometrie „verbiegt nichts": Sie dreht und spiegelt, aber bewahrt jede Länge und jeden Winkel. In der Ebene ist $O_2(\mathbb{R})$ genau *Drehungen und Spiegelungen*.

**Adjungierte $=$ „Wirkung ins andere Argument spiegeln".** $\langle f(v),w\rangle=\langle v,f^*(w)\rangle$ heißt: Statt $f$ auf $v$ anzuwenden, kann man äquivalent $f^*$ auf $w$ anwenden. $f^*$ ist der „Partner" von $f$ bezüglich des Skalarprodukts — die geometrisch korrekte Transponierung.

**Die drei Sonderklassen als Geometrie:**
```
   selbstadjungiert  f* = f      → reelle Streckungen auf ⟂ Achsen  (Hauptachsen)
   isometrisch       f* = f⁻¹    → Drehungen/Spiegelungen (Eigenwerte |λ|=1)
   normal            f f* = f* f  → beliebige komplexe Streckungen auf ⟂ Achsen
```

**Normal $=$ „$f$ und $f^*$ vertragen sich".** Kommutieren $f$ und $f^*$, so „ziehen sie nicht gegeneinander" — und genau dann gibt es perpendikuläre Achsen, die *beide* respektieren. Das ist der Kern des Spektralsatzes.

**Spektralsatz anschaulich.** Ein normaler Operator wirkt wie eine Diagonalmatrix *in einem gedrehten, aber immer noch rechtwinkligen* Koordinatensystem. Selbstadjungiert $\Rightarrow$ die Streckfaktoren sind **reell**; isometrisch $\Rightarrow$ sie liegen auf dem **Einheitskreis** ($|\lambda|=1$).

---

<a id="formale-definitionen-8"></a>
## Formale Definitionen

Sei $V$ endlichdim. euklidisch ($k=\mathbb{R}$) oder unitär ($k=\mathbb{C}$) mit Skalarprodukt $\langle\cdot,\cdot\rangle$. Konvention: linear im 1., konjugiert-linear im 2. Argument (Kap. 6).

**Definition 8.1 (metrisch / isometrisch).**
$f\colon V\to W$ (beide euklidisch/unitär) heißt **metrisch** (oder **isometrisch**), wenn
$$
\langle f(v),f(v')\rangle=\langle v,v'\rangle\qquad\forall v,v'\in V.
$$
Im euklidischen Fall sagt man **orthogonal**, im unitären **unitär**. Eine bijektive metrische Abbildung heißt **Isometrie**.

**Definition 8.2 (Isometriegruppe, $O_n$, $U_n$).**
Die Isometrien $V\to V$ bilden eine Gruppe (Verkettung), die **Isometriegruppe**:
$$
O(V)\ (\text{euklidisch}),\qquad U(V)\ (\text{unitär}).
$$
Matrixgruppen:
$$
O_n(\mathbb{R})=\{A\in\mathbb{R}^{n\times n}\mid A^{-1}=A^{\mathsf T}\},\qquad U_n(\mathbb{C})=\{A\in\mathbb{C}^{n\times n}\mid A^{-1}=A^*=\bar A^{\mathsf T}\}.
$$

**Definition 8.3 (adjungierte Matrix / Abbildung).**
Für $A\in k^{n\times n}$: $A^*:=\bar A^{\mathsf T}$ (reell: $A^*=A^{\mathsf T}$). Für $f\colon V\to V$ ist die **adjungierte Abbildung** $f^*\colon V\to V$ die eindeutige lineare Abbildung mit
$$
\langle f(v),w\rangle=\langle v,f^*(w)\rangle\qquad\forall v,w\in V.
$$
(Existenz/Eindeutigkeit: Satz 8.6. In manchen Quellen $f^\circ$ statt $f^*$.)

**Definition 8.4 (selbstadjungiert, normal).**
$f$ heißt **selbstadjungiert**, wenn $f^*=f$; **normal**, wenn $f\circ f^*=f^*\circ f$. Für Matrizen: $A$ selbstadjungiert $\Leftrightarrow A^*=A$ (reell: **symmetrisch**; komplex: **hermitesch**); $A$ normal $\Leftrightarrow AA^*=A^*A$.

**Definition 8.5 (Orthonormalbasis-Diagonalisierung).**
$f$ ist **orthonormal diagonalisierbar**, wenn es eine **Orthonormalbasis** von $V$ aus Eigenvektoren von $f$ gibt.

---

<a id="eigenschaften-8"></a>
## Eigenschaften

| Eigenschaft | Aussage | Kurzbegründung |
|---|---|---|
| **metrisch $\Rightarrow$ längentreu** | $\|f(v)\|=\|v\|$ | $v'=v$ einsetzen. |
| **metrisch $\Rightarrow$ injektiv** | $\ker f=\{0\}$ | $\|f(v)\|=\|v\|=0\Rightarrow v=0$. |
| **$A^*=\bar A^{\mathsf T}$-Regeln** | $(A+B)^*=A^*+B^*$, $(aA)^*=\bar a A^*$, $(AB)^*=B^*A^*$, $(A^*)^*=A$ | direkt. |
| **selbstadj. $\Rightarrow$ normal** | $ff^*=f^2=f^*f$ | $f^*=f$. |
| **metrisch $\Rightarrow$ normal** | $ff^*=f^*f=\mathrm{id}$ | $f^*=f^{-1}$. |
| **$\det$ von Isometrien** | $\det A\in\{\pm1\}$ (orth.), $|\det A|=1$ (unitär) | $\det(AA^*)=1$. |
| **$\mathrm{Eig}(f,\lambda)=\mathrm{Eig}(f^*,\bar\lambda)$** | für normale $f$ | Lemma 8.10. |
| **Invarianz-Übergang** | $f(U)\subseteq U\Rightarrow f^*(U^\perp)\subseteq U^\perp$ | Lemma 8.9. |

---

<a id="sätze-8"></a>
## Sätze

<a id="lemma-85½-yoga-lemma-rechenbrücke-abstrakt-leftrightarrow-matrix"></a>
### Lemma 8.5½ (Yoga-Lemma) — *Rechenbrücke abstrakt $\leftrightarrow$ Matrix*

**Aussage.** Sei $\{b_1,\dots,b_n\}$ eine **Orthonormalbasis** von $V$, und seien $f,f'\colon V\to V$ linear mit darstellenden Matrizen $A,A'\in k^{n\times n}$ bzgl. dieser ONB. Dann gilt für alle $x,y\in k^n$ (mit $v=\sum_i x_ib_i$, $w=\sum_i y_ib_i$):
$$
\big\langle f(v),\,f'(w)\big\rangle=\big\langle Ax,\,A'y\big\rangle_{\mathrm{Std}}=(x_1,\dots,x_n)\,A^{\mathsf T}\,\overline{A'}\,\begin{pmatrix}\overline{y_1}\\\vdots\\\overline{y_n}\end{pmatrix}.
$$
Insbesondere gilt bei einer ONB $\langle v,w\rangle=\langle x,y\rangle_{\mathrm{Std}}=\sum_i x_i\overline{y_i}$: das abstrakte Skalarprodukt **ist** das Standardskalarprodukt der Koordinaten.
**Voraussetzungen.** $\{b_i\}$ **orthonormal** (nur dann $\langle b_i,b_j\rangle=\delta_{ij}$).
**Bedeutung.** Übersetzt jede Skalarproduktrechnung in Matrixrechnung — das technische Arbeitspferd, mit dem man $A^*=\bar A^{\mathsf T}$ (Satz 8.6), die Adjungierten-Rechenregeln (Satz 8.7) und die Matrixkriterien für selbstadjungiert/normal (unten) *überhaupt* herleitet.
**Intuition.** In einer ONB „vergisst" man die abstrakte Geometrie gefahrlos und rechnet mit Koordinaten wie im $k^n$ mit Standardprodukt.
**Beweisstil.** *direkt.* $\langle f(v),f'(w)\rangle=\big\langle\sum_i(Ax)_ib_i,\sum_j(A'y)_jb_j\big\rangle=\sum_{i,j}(Ax)_i\overline{(A'y)_j}\langle b_i,b_j\rangle=\sum_i(Ax)_i\overline{(A'y)_i}=(Ax)^{\mathsf T}\overline{(A'y)}=x^{\mathsf T}A^{\mathsf T}\overline{A'}\,\bar y$, da $\langle b_i,b_j\rangle=\delta_{ij}$. $\blacksquare$

<a id="satz-86-existenz-und-eindeutigkeit-der-adjungierten"></a>
### Satz 8.6 (Existenz und Eindeutigkeit der Adjungierten)

**Aussage.** Zu jeder linearen $f\colon V\to V$ gibt es **genau eine** lineare $f^*\colon V\to V$ mit $\langle f(v),w\rangle=\langle v,f^*(w)\rangle$ für alle $v,w$. Bezüglich einer **Orthonormalbasis** ist die Matrix von $f^*$ gerade $A^*=\bar A^{\mathsf T}$, wenn $A$ die Matrix von $f$ ist.
**Voraussetzungen.** $V$ endlichdim., ONB vorhanden (Kap. 7).
**Bedeutung.** Macht $f^*$ zu einem wohldefinierten Objekt; verbindet abstrakte Adjungierte mit der konkreten Matrix $\bar A^{\mathsf T}$.

<a id="satz-87-rechenregeln-lemma-72"></a>
### Satz 8.7 (Rechenregeln, Lemma 7.2)

**Aussage.** $(f+g)^*=f^*+g^*$, $(af)^*=\bar a\,f^*$, $(f^*)^*=f$, $(f\circ g)^*=g^*\circ f^*$.
**Bedeutung.** Die Adjungierung ist eine **konjugiert-lineare Involution** mit Antihomomorphie bei Verkettung.

<a id="satz-88-charakterisierung-von-isometrien-zentral"></a>
### Satz 8.8 (Charakterisierung von Isometrien) — *zentral*

**Aussage.** Für $f\colon V\to V$ ($\dim V<\infty$) sind äquivalent:
1. $f$ ist Isometrie ($\langle f(v),f(w)\rangle=\langle v,w\rangle$);
2. $f$ ist längentreu ($\|f(v)\|=\|v\|$);
3. $f\circ f^*=f^*\circ f=\mathrm{id}$, d. h. $f$ bijektiv mit $f^{-1}=f^*$;
4. $f$ bildet eine (jede) ONB auf eine ONB ab;
5. die Matrix $A$ bzgl. einer ONB erfüllt $A\in O_n(\mathbb{R})$ bzw. $A\in U_n(\mathbb{C})$.

**Bedeutung.** Die vielen Gesichter der Isometrie; „$A^{-1}=A^*$" ist das Rechenkriterium.
**Konsequenz.** $O_2(\mathbb{R})$ besteht genau aus Drehungen (det $=+1$) und Spiegelungen (det $=-1$).

<a id="lemma-89-invarianz-übergang-aufs-komplement"></a>
### Lemma 8.9 (Invarianz-Übergang aufs Komplement)

**Aussage.** Ist $U\subseteq V$ mit $f(U)\subseteq U$, so gilt $f^*(U^\perp)\subseteq U^\perp$. Für **normale** $f$ mit $f$-invariantem $U$, das auch $f^*$-invariant ist, ist $U^\perp$ ebenfalls $f$-invariant.
**Bedeutung.** Der Motor der Spektralsatz-Induktion (Übergang von $V$ auf $U^\perp$).

<a id="lemma-89½-normalität-ist-normerhaltend-lemma-77"></a>
### Lemma 8.9½ (Normalität ist normerhaltend, „Lemma 7.7\*")

**Aussage.** $f$ ist genau dann normal, wenn $\langle f^*(v),f^*(w)\rangle=\langle f(v),f(w)\rangle$ für alle $v,w$ gilt; äquivalent (Polarisierung):
$$
f\ \text{normal}\quad\Longleftrightarrow\quad \|f^*(v)\|=\|f(v)\|\quad\text{für alle }v\in V.
$$
**Bedeutung.** $f$ und $f^*$ „bewegen jeden Vektor gleich weit". Diese Norm­gleichheit ist der Schlüsselschritt für Lemma 8.10 und damit für den Spektralsatz.
**Beweisstil.** *direkt.* Für alle $v,w$:
$$
\langle f(v),f(w)\rangle=\langle v,f^*f(w)\rangle,\qquad \langle f^*(v),f^*(w)\rangle=\langle v,ff^*(w)\rangle.
$$
Diese sind für alle $v,w$ gleich $\Leftrightarrow f^*f=ff^*\Leftrightarrow f$ normal. Der Spezialfall $v=w$ liefert $\|f(v)\|^2=\langle v,f^*f(v)\rangle=\langle v,ff^*(v)\rangle=\|f^*(v)\|^2$; umgekehrt folgt aus Längengleichheit per Polarisierung die volle Identität. $\blacksquare$

<a id="lemma-810-eigenräume-von-f-und-f-bei-normalen-f"></a>
### Lemma 8.10 (Eigenräume von $f$ und $f^*$ bei normalen $f$)

**Aussage.** Ist $f$ normal, so gilt für alle $\lambda$: $\;\mathrm{Eig}(f,\lambda)=\mathrm{Eig}(f^*,\bar\lambda)$. Insbesondere $\ker f=\ker f^*$.
**Bedeutung.** Eigenvektoren von $f$ sind zugleich Eigenvektoren von $f^*$ — die Schlüsseleigenschaft, die $U$ *doppelt* invariant macht.

<a id="satz-811-unitärer-spektralsatz-höhepunkt"></a>
### Satz 8.11 (Unitärer Spektralsatz) — *Höhepunkt*

**Aussage.** Sei $V$ endlichdim. **unitär** ($k=\mathbb{C}$), $f\colon V\to V$ linear. Dann:
$$
f\ \text{normal}\quad\Longleftrightarrow\quad \text{es gibt eine ONB von }V\text{ aus Eigenvektoren von }f.
$$
Insbesondere ist jeder normale Operator **orthonormal diagonalisierbar**.
**Voraussetzungen.** $V$ unitär (über $\mathbb{C}$), endlichdim.
**Bedeutung.** Die vollständige, geometrisch perfekte Diagonalisierung. „Normal" ist exakt die richtige Bedingung.

<a id="satz-812-matrixversion-unitäre-diagonalisierung"></a>
### Satz 8.12 (Matrixversion / unitäre Diagonalisierung)

**Aussage.** Für $A\in\mathbb{C}^{n\times n}$ äquivalent:
1. $A$ normal ($AA^*=A^*A$);
2. es gibt eine ONB von $\mathbb{C}^n$ aus Eigenvektoren von $A$;
3. es gibt eine **unitäre** Matrix $S\in U_n(\mathbb{C})$ mit $S^{-1}AS=S^*AS$ diagonal.

**Bedeutung.** Rechenfassung: normale Matrizen sind unitär diagonalisierbar.

<a id="satz-813-eigenwerte-der-sonderklassen"></a>
### Satz 8.13 (Eigenwerte der Sonderklassen)

**Aussage.** Für einen **normalen** Operator $f$:
- $f$ **selbstadjungiert** $\Leftrightarrow$ alle Eigenwerte sind **reell**;
- $f$ **isometrisch (unitär)** $\Leftrightarrow$ alle Eigenwerte haben **Betrag $1$**.

**Bedeutung.** Die geometrische Deutung: selbstadjungiert $=$ reelle Streckungen, unitär $=$ Drehungen (Phasen $e^{i\varphi}$).

<a id="satz-814-reeller-spektralsatz-ergänzt-kurshöhepunkt-über-mathbbr"></a>
### Satz 8.14 (Reeller Spektralsatz) — *ergänzt; Kurshöhepunkt über $\mathbb{R}$*

**Aussage.** Sei $A\in\mathbb{R}^{n\times n}$ **symmetrisch** ($A^{\mathsf T}=A$) bzw. $f\colon V\to V$ **selbstadjungiert** auf einem euklidischen Raum. Dann:
1. alle Eigenwerte von $A$ sind **reell**;
2. es gibt eine **Orthonormalbasis von $\mathbb{R}^n$ aus Eigenvektoren** von $A$;
3. es gibt eine **orthogonale** Matrix $S\in O_n(\mathbb{R})$ mit $S^{\mathsf T}AS$ diagonal (reell).

**Bedeutung.** *Jede reelle symmetrische Matrix ist orthogonal diagonalisierbar.* Das ist die **Hauptachsentransformation** (quadratische Formen, PCA, Trägheitstensor) und der praktisch wichtigste Spezialfall.
**Intuition.** Symmetrische Matrizen strecken den Raum entlang perpendikulärer Hauptachsen — ohne jede Scherung oder Drehung „zwischen" den Achsen.

---

<a id="beweise-8"></a>
## Beweise

> **Klausurrelevant in voller Tiefe:** Lemma 8.5½ (Yoga-Lemma), Satz 8.6 (Adjungierte via $A^*$), 8.8 (Isometrie $\Leftrightarrow A^*=A^{-1}$),
> Lemma 8.9½ (Normalität normerhaltend), Lemma 8.10, **Satz 8.11 (unitärer Spektralsatz)**, Satz 8.13 und **Satz 8.14 (reeller Spektralsatz)**.

<a id="beweis-von-satz-86-adjungierte-beweisstil-konstruktion-in-onb-eindeutigkeit"></a>
### Beweis von Satz 8.6 (Adjungierte) — *Beweisstil: Konstruktion in ONB $+$ Eindeutigkeit*

Sei $\{b_1,\dots,b_n\}$ eine ONB. In Koordinaten ist $\langle v,w\rangle=w^*v$ (Spaltenvektoren; $w^*=\bar w^{\mathsf T}$), denn $w^*v=\sum_i\overline{w_i}v_i=\sum_i v_i\overline{w_i}$. Sei $A$ die Matrix von $f$. Definiere $f^*$ durch die Matrix $A^*=\bar A^{\mathsf T}$. Dann
$$
\langle f(v),w\rangle=w^*(Av)=(w^*A)v=\big((A^*w)^*\big)v=\langle v,A^*w\rangle=\langle v,f^*(w)\rangle,
$$
denn $(A^*w)^*=w^*(A^*)^*=w^*A$. **Eindeutigkeit:** Erfüllen $g,g'$ beide $\langle v,g(w)\rangle=\langle v,g'(w)\rangle$ für alle $v$, so $\langle v,(g-g')(w)\rangle=0$ für alle $v$, also $(g-g')(w)=0$ für alle $w$, d. h. $g=g'$. $\blacksquare$

<a id="beweis-von-satz-88-isometrie-charakterisierung-beweisstil-ringschluss"></a>
### Beweis von Satz 8.8 (Isometrie-Charakterisierung) — *Beweisstil: Ringschluss*

$(1)\Rightarrow(2)$: $w=v$ einsetzen. $(2)\Rightarrow(1)$: **Polarisierung** — das Skalarprodukt lässt sich aus der Norm zurückgewinnen (Kap. 7, Längenformel), also folgt Winkeltreue aus Längentreue.
$(1)\Leftrightarrow(3)$: $\langle f(v),f(w)\rangle=\langle v,(f^*f)(w)\rangle$; dies $=\langle v,w\rangle$ für alle $v,w$ $\Leftrightarrow f^*f=\mathrm{id}$. Bei $\dim V<\infty$ folgt $f$ bijektiv und $f^{-1}=f^*$ (also auch $ff^*=\mathrm{id}$).
$(3)\Leftrightarrow(5)$: In ONB ist $f^*f=\mathrm{id}$ gerade $A^*A=E$, d. h. $A^{-1}=A^*$ — Definition von $O_n/U_n$.
$(1)\Leftrightarrow(4)$: $f$ metrisch $\Leftrightarrow\langle f(b_i),f(b_j)\rangle=\langle b_i,b_j\rangle=\delta_{ij}$ $\Leftrightarrow\{f(b_i)\}$ ONB. $\blacksquare$

<a id="beweis-von-lemma-89-beweisstil-direkt"></a>
### Beweis von Lemma 8.9 — *Beweisstil: direkt*

Sei $f(U)\subseteq U$ und $w\in U^\perp$. Für alle $u\in U$: $\langle u,f^*(w)\rangle=\langle f(u),w\rangle=0$ (da $f(u)\in U$, $w\in U^\perp$). Also $f^*(w)\perp U$, d. h. $f^*(w)\in U^\perp$. $\blacksquare$

<a id="beweis-von-lemma-810-mathrmeigflambdamathrmeigfbarlambda-beweisstil-normalität-norm"></a>
### Beweis von Lemma 8.10 ($\mathrm{Eig}(f,\lambda)=\mathrm{Eig}(f^*,\bar\lambda)$) — *Beweisstil: Normalität + Norm*

Mit $f$ ist auch $g:=f-\lambda\,\mathrm{id}$ normal (mit $g^*=f^*-\bar\lambda\,\mathrm{id}$). Nach Lemma 8.9½ ist $\|g(v)\|=\|g^*(v)\|$ für alle $v$. Damit
$$
v\in\mathrm{Eig}(f,\lambda)\Leftrightarrow g(v)=0\Leftrightarrow\|g(v)\|=0\Leftrightarrow\|g^*(v)\|=0\Leftrightarrow g^*(v)=0\Leftrightarrow v\in\mathrm{Eig}(f^*,\bar\lambda).\ \blacksquare
$$

<a id="beweis-von-satz-811-unitärer-spektralsatz-beweisstil-induktion-über-dim-v-via-uperp"></a>
### Beweis von Satz 8.11 (Unitärer Spektralsatz) — *Beweisstil: Induktion über $\dim V$ via $U^\perp$* ★

**„$\Leftarrow$".** Gibt es eine ONB aus Eigenvektoren, so ist die Matrix $A=\mathrm{diag}(\lambda_1,\dots,\lambda_n)$; dann $A^*=\mathrm{diag}(\bar\lambda_1,\dots,\bar\lambda_n)$, und $AA^*=\mathrm{diag}(|\lambda_i|^2)=A^*A$ — $f$ ist normal.

**„$\Rightarrow$".** Induktion über $n=\dim V$. $n=1$: klar (jeder Einheitsvektor ist Eigenvektor). $n\ge2$: Nach dem Fundamentalsatz der Algebra hat $\chi_f$ eine Nullstelle $\lambda\in\mathbb{C}$, also einen Eigenvektor $u$ mit $\|u\|=1$. Nach Lemma 8.10 ist $u$ auch Eigenvektor von $f^*$ (zu $\bar\lambda$). Setze $U=\mathrm{span}(u)$: dann ist $U$ sowohl $f$- als auch $f^*$-invariant. Nach Lemma 8.9 ist $U^\perp$ **$f$-invariant** (und $f^*$-invariant). Die Einschränkung $f|_{U^\perp}$ ist normal (ihre Adjungierte ist $f^*|_{U^\perp}$), und $\dim U^\perp=n-1$. Nach Induktionsvoraussetzung besitzt $U^\perp$ eine ONB aus Eigenvektoren von $f|_{U^\perp}$. Zusammen mit $u$ ergibt das eine ONB von $V=U\oplus U^\perp$ aus Eigenvektoren von $f$. $\blacksquare$

<a id="beweis-von-satz-813-eigenwerte-beweisstil-direkt"></a>
### Beweis von Satz 8.13 (Eigenwerte) — *Beweisstil: direkt*

**Selbstadjungiert $\Rightarrow$ reell:** Sei $f(v)=\lambda v$, $v\neq0$. Dann
$$
\lambda\langle v,v\rangle=\langle f(v),v\rangle=\langle v,f^*(v)\rangle=\langle v,f(v)\rangle=\langle v,\lambda v\rangle=\bar\lambda\langle v,v\rangle,
$$
also $\lambda=\bar\lambda$, d. h. $\lambda\in\mathbb{R}$. **Isometrisch $\Rightarrow|\lambda|=1$:** $\|v\|=\|f(v)\|=\|\lambda v\|=|\lambda|\|v\|\Rightarrow|\lambda|=1$. Die Umkehrungen folgen aus dem Spektralsatz (Diagonalmatrix mit reellen bzw. betragsgleichen Einträgen ist selbstadjungiert bzw. unitär). $\blacksquare$

<a id="beweis-von-satz-814-reeller-spektralsatz-beweisstil-eigenwerte-reell-reelle-induktion"></a>
### Beweis von Satz 8.14 (Reeller Spektralsatz) — *Beweisstil: Eigenwerte reell $+$ reelle Induktion* ★

**(i) Eigenwerte reell.** Fasse $A\in\mathbb{R}^{n\times n}$ symmetrisch als komplexe Matrix auf; dann $A^*=\bar A^{\mathsf T}=A^{\mathsf T}=A$, also $A$ hermitesch $=$ selbstadjungiert über $\mathbb{C}$. Nach Satz 8.13 sind alle Eigenwerte reell.

**(ii)/(iii) reelle Induktion über $n$.** $n=1$ klar. $n\ge2$: $\chi_A$ hat nach (i) eine **reelle** Nullstelle $\lambda$; da $A$ reell und $\lambda$ reell, ist $\det(A-\lambda E)=0$ über $\mathbb{R}$, also existiert ein **reeller** Einheitseigenvektor $u\in\mathbb{R}^n$. Setze $U=\mathrm{span}(u)$. Für $w\in U^\perp$ gilt wegen der Symmetrie
$$
\langle Aw,u\rangle=\langle w,Au\rangle=\lambda\langle w,u\rangle=0,
$$
also $Aw\in U^\perp$ — $U^\perp$ ist $A$-invariant. Die Einschränkung $A|_{U^\perp}$ ist wieder symmetrisch, $\dim U^\perp=n-1$. Nach Induktionsvoraussetzung besitzt $U^\perp$ eine reelle ONB aus Eigenvektoren. Zusammen mit $u$: eine reelle ONB von $\mathbb{R}^n$ aus Eigenvektoren. Die Matrix $S$ mit diesen ONB-Vektoren als Spalten ist orthogonal ($S^{\mathsf T}=S^{-1}$) und erfüllt $S^{\mathsf T}AS=\mathrm{diag}(\lambda_1,\dots,\lambda_n)$. $\blacksquare$

> **Warum dieser Satz das Kursziel ist.** Er sagt: *Reelle symmetrische Matrizen sind ausnahmslos orthogonal diagonalisierbar* — ohne komplexe Zahlen, mit reellen Eigenwerten und perpendikulären reellen Eigenvektoren. Das ist die Hauptachsentransformation und der meistbenutzte Spektralsatz der Anwendungen. In der ursprünglichen Mitschrift fehlte er — hier ist er.

---

<a id="algorithmen-8"></a>
## Algorithmen

<a id="algorithmus-orthonormale-unitäreorthogonale-diagonalisierung"></a>
### Algorithmus — Orthonormale (unitäre/orthogonale) Diagonalisierung

- **Motivation.** „Bestimmen Sie eine (unitäre/orthogonale) Matrix $S$, die $A$ diagonalisiert."
- **Idee.** Normal/symmetrisch prüfen; Eigenräume berechnen; **innerhalb jedes Eigenraums Gram-Schmidt**; Eigenräume sind automatisch zueinander orthogonal.
- **Voraussetzungen.** $A$ normal (komplex) bzw. symmetrisch (reell).
- **Pseudocode.**
  ```
  Eingabe: A  (normal bzw. symmetrisch)
  1. χ_A, Eigenwerte λ_1,…,λ_r
  2. für jeden λ_i:
        Basis von Eig(A,λ_i) = Kern(A − λ_i E)
        Gram-Schmidt darauf  → ONB des Eigenraums
  3. S ← Matrix mit allen ONB-Eigenvektoren als Spalten
     (Eigenräume zu verschiedenen λ sind automatisch orthogonal)
  4. return S    # S* A S = diag(λ_1,…)   (reell: S^T A S)
  ```
- **Mathematische Beschreibung.** $S\in U_n$ bzw. $O_n$, $S^{-1}AS=\mathrm{diag}(\lambda_i)$ (Satz 8.12/8.14).
- **Laufzeit.** $O(n^3)$ (Eigenräume $+$ Gram-Schmidt).
- **Korrektheitsidee.** Spektralsatz: bei normal/symmetrisch existiert die ONB; Eigenräume zu verschiedenen $\lambda$ stehen senkrecht (Lemma 8.10 $\Rightarrow$ Orthogonalität).
- **Anwendungen.** Hauptachsentransformation quadratischer Formen; PCA; Diagonalisierung von Kovarianz-/Trägheitsmatrizen.
- **Typische Fehler.** Gram-Schmidt **innerhalb** der Eigenräume vergessen (Spalten dann nicht orthonormal); $S^{-1}$ statt $S^*$ verwenden (bei nicht-orthonormalen Spalten falsch); Normalität/Symmetrie nicht prüfen.

> **Warum Eigenräume zu verschiedenen $\lambda$ orthogonal sind (normale $f$):** Für $f(v)=\lambda v$, $f(w)=\mu w$ mit $\lambda\neq\mu$:
> $\lambda\langle v,w\rangle=\langle f(v),w\rangle=\langle v,f^*(w)\rangle=\langle v,\bar\mu w\rangle=\mu\langle v,w\rangle$ (Lemma 8.10), also $(\lambda-\mu)\langle v,w\rangle=0\Rightarrow v\perp w$.

---

<a id="beispiele-8"></a>
## Beispiele

**Beispiel 1 (leicht — Drehung ist Isometrie).** $A=\begin{psmallmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{psmallmatrix}\in O_2(\mathbb{R})$: $A^{\mathsf T}A=E$, $\det A=1$ (Drehung). Eine Spiegelung hat $\det=-1$.

**Beispiel 2 (mittel — reelle symmetrische Diagonalisierung).** $A=\begin{psmallmatrix}2&1\\1&2\end{psmallmatrix}$ symmetrisch. $\chi=(X-1)(X-3)$, Eigenvektoren $\tfrac{1}{\sqrt2}(1,-1)$ (zu $1$), $\tfrac{1}{\sqrt2}(1,1)$ (zu $3$) — automatisch orthogonal. $S=\tfrac{1}{\sqrt2}\begin{psmallmatrix}1&1\\-1&1\end{psmallmatrix}\in O_2$, $S^{\mathsf T}AS=\mathrm{diag}(1,3)$.

**Beispiel 3 (mittel — selbstadjungiert $\Rightarrow$ reell).** $A=\begin{psmallmatrix}0&-i\\i&0\end{psmallmatrix}$ (hermitesch: $A^*=A$). $\chi=X^2-1$, Eigenwerte $\pm1$ — reell, wie vom Satz garantiert.

**Beispiel 4 (mittel — unitär $\Rightarrow|\lambda|=1$).** $A=\begin{psmallmatrix}0&1\\-1&0\end{psmallmatrix}$ (orthogonal, $A^{\mathsf T}A=E$). Über $\mathbb{C}$: Eigenwerte $\pm i$, Betrag $1$. Über $\mathbb{R}$ nicht diagonalisierbar (keine reellen Eigenwerte) — konsistent: der **reelle** Spektralsatz gilt nur für **symmetrische** Matrizen, nicht für orthogonale.

**Beispiel 5 (schwer — Hauptachsentransformation).** Die quadratische Form $q(x,y)=5x^2+4xy+5y^2$ hat Matrix $A=\begin{psmallmatrix}5&2\\2&5\end{psmallmatrix}$. Eigenwerte $3,7$, ONB-Eigenvektoren $\tfrac{1}{\sqrt2}(1,-1),\tfrac{1}{\sqrt2}(1,1)$. In den Hauptachsen: $q=3\,\xi^2+7\,\eta^2$ — eine Ellipse, deren Achsen die Eigenvektorrichtungen sind. Das ist der praktische Kern des reellen Spektralsatzes.

---

<a id="gegenbeispiele-8"></a>
## Gegenbeispiele

**Gegenbeispiel A (diagonalisierbar, aber nicht orthonormal).** $A=\begin{psmallmatrix}1&1\\0&2\end{psmallmatrix}$ ist diagonalisierbar (Eigenwerte $1,2$), aber **nicht normal** ($AA^*\neq A^*A$) — es gibt **keine ONB** aus Eigenvektoren (die Eigenvektoren stehen nicht senkrecht). *Diagonalisierbar $\neq$ orthonormal diagonalisierbar.*

**Gegenbeispiel B (reeller Spektralsatz nur für symmetrisch).** $\begin{psmallmatrix}0&-1\\1&0\end{psmallmatrix}$ ist orthogonal (also normal), aber über $\mathbb{R}$ **nicht** diagonalisierbar — der reelle Spektralsatz verlangt **Symmetrie**, nicht bloß Normalität.

**Gegenbeispiel C (Adjungierte hängt vom Skalarprodukt ab).** $f^*$ ist relativ zu einem *festen* Skalarprodukt definiert; ändert man das Skalarprodukt, ändert sich $f^*$. $A^*=\bar A^{\mathsf T}$ gilt nur bezüglich einer **ONB** des Standardprodukts.

**Gegenbeispiel D (unitärer Spektralsatz braucht $\mathbb{C}$).** Über $\mathbb{R}$ ist „normal" **nicht** hinreichend für Diagonalisierbarkeit (Gegenbeispiel B). Erst über $\mathbb{C}$ (Fundamentalsatz) greift der Beweis.

---

<a id="typische-klausuraufgaben-8"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Woran erkennbar | Strategie |
|---|---|---|
| **Orthogonal/unitär diagonalisieren** | „Bestimmen Sie $S$ mit $S^*AS$ diagonal." | Eigenräume, Gram-Schmidt je Eigenraum, $S$ zusammensetzen. |
| **Isometrie prüfen** | „Ist $A$ orthogonal/unitär?" | $A^*A=E$ testen. |
| **Selbstadjungiert/normal prüfen** | „Ist $f$ selbstadj./normal?" | $A^*=A$ bzw. $AA^*=A^*A$. |
| **Adjungierte bestimmen** | „Berechnen Sie $f^*$." | $A^*=\bar A^{\mathsf T}$ (in ONB!). |
| **Eigenwerteigenschaften** | „Zeigen Sie: reelle/Betrag-1-Eigenwerte." | Satz 8.13-Beweis. |
| **Hauptachsen / quadratische Form** | „Bringen Sie $q$ auf Normalform." | reeller Spektralsatz, $S^{\mathsf T}AS$ diagonal. |
| **Spektralsatz beweisen** | „Beweisen Sie den (unitären) Spektralsatz." | Induktion über $U^\perp$ (Satz 8.11). |

---

<a id="typische-fehler-8"></a>
## Typische Fehler

| Fehler | Warum falsch | Richtig |
|---|---|---|
| diagonalisierbar $=$ orthonormal diagonalisierbar | Gegenbeispiel A (nicht normal). | ONB nur bei normal/symmetrisch. |
| reeller Spektralsatz für alle normalen | gilt nur für **symmetrische** reelle Matrizen. | Symmetrie $A^{\mathsf T}=A$ prüfen. |
| $A^*=\bar A^{\mathsf T}$ ohne ONB | gilt nur bzgl. ONB des Standardprodukts. | erst ONB sichern. |
| Konjugation bei $A^*$ vergessen | komplex: $A^*=\bar A^{\mathsf T}$, nicht $A^{\mathsf T}$. | konjugieren **und** transponieren. |
| Gram-Schmidt je Eigenraum vergessen | Spalten von $S$ nicht orthonormal. | innerhalb jedes Eigenraums orthonormalisieren. |
| $S^{-1}$ statt $S^*$ | nur bei orthonormalem $S$ gleich. | $S$ unitär/orthogonal machen, dann $S^{-1}=S^*$. |
| „normal $\Rightarrow$ diagonalisierbar über $\mathbb{R}$" | falsch (Gegenbeispiel B/D). | über $\mathbb{C}$; reell nur symmetrisch. |

> **Vergleichstabelle: die drei Operatorklassen.**
>
> | | Definition | Matrix | Eigenwerte | ONB-Eigenbasis? | Geometrie |
> |---|---|---|---|---|---|
> | **normal** | $ff^*=f^*f$ | $AA^*=A^*A$ | beliebig $\in\mathbb{C}$ | ja (über $\mathbb{C}$) | Streckung auf $\perp$ Achsen |
> | **selbstadjungiert** | $f^*=f$ | $A^*=A$ (symm./herm.) | **reell** | ja | reelle Hauptachsen |
> | **isometrisch (unitär/orth.)** | $f^*=f^{-1}$ | $A^*=A^{-1}$ ($O_n/U_n$) | $|\lambda|=1$ | ja (über $\mathbb{C}$) | Drehung/Spiegelung |
>
> **Vergleichstabelle: $O_n(\mathbb{R})$ vs. $U_n(\mathbb{C})$.**
>
> | | $O_n(\mathbb{R})$ | $U_n(\mathbb{C})$ |
> |---|---|---|
> | Bedingung | $A^{\mathsf T}A=E$ | $A^*A=E$ |
> | $\det$ | $\pm1$ | Betrag $1$ (auf Einheitskreis) |
> | Geometrie | Drehungen/Spiegelungen von $\mathbb{R}^n$ | „komplexe Drehungen" von $\mathbb{C}^n$ |

---

<a id="verbindungen-8"></a>
## Verbindungen

- **← Kapitel 5:** Konjugation $\Rightarrow A^*=\bar A^{\mathsf T}$; Fundamentalsatz liefert den Eigenwert im Spektralsatz-Beweis.
- **← Kapitel 6:** Skalarprodukt definiert $f^*$; selbstadjungiert/normal sind Skalarprodukt-Begriffe.
- **← Kapitel 7:** ONB (Gram-Schmidt) und $V=U\oplus U^\perp$ tragen den Induktionsschritt (Einschränkung auf $U^\perp$).
- **← Kapitel 2/3/4:** Der Spektralsatz ist die *orthonormale* Verfeinerung der Diagonalisierbarkeit; normale Operatoren haben quadratfreies $\mu_f$ über $\mathbb{C}$ (nur Blöcke der Größe $1$ — JNF degeneriert zur Diagonalmatrix).
- **→ Anwendungen (außerhalb LinA 2):** Hauptachsentransformation, PCA, Fourier-Analyse, Quantenmechanik, Schwingungsanalyse.

**Definitionen, die zentral bleiben:** $f^*$, selbstadjungiert, normal, Isometrie, Spektralsatz.

---

<a id="zusammenfassung-8"></a>
## Zusammenfassung

| Kernaussage | Symbolisch |
|---|---|
| Adjungierte existiert eindeutig; $A^*=\bar A^{\mathsf T}$ (ONB). | $\langle f(v),w\rangle=\langle v,f^*(w)\rangle$ |
| Yoga-Lemma: ONB übersetzt Skalarprodukt in Matrixrechnung. | $\langle f(v),f'(w)\rangle=x^{\mathsf T}A^{\mathsf T}\overline{A'}\bar y$ |
| Isometrie $\Leftrightarrow$ längentreu $\Leftrightarrow f^*=f^{-1}\Leftrightarrow A\in O_n/U_n$. | (Satz 8.8) |
| selbstadj. $\Rightarrow$ normal; metrisch $\Rightarrow$ normal. | — |
| normal $\Leftrightarrow$ $\|f^*(v)\|=\|f(v)\|$; $\mathrm{Eig}(f,\lambda)=\mathrm{Eig}(f^*,\bar\lambda)$. | (Lemma 8.9½/8.10) |
| **Unitärer Spektralsatz:** normal $\Leftrightarrow$ ONB aus Eigenvektoren. | (Satz 8.11) |
| Matrixversion: normal $\Leftrightarrow S^*AS$ diagonal, $S$ unitär. | (Satz 8.12) |
| selbstadj. $\Leftrightarrow$ reelle EW; unitär $\Leftrightarrow|\lambda|=1$. | (Satz 8.13) |
| **Reeller Spektralsatz:** symmetrisch $\Rightarrow$ orthogonal diagonalisierbar, reelle EW. | (Satz 8.14) |

**Die eine Idee des Kapitels:** Das Skalarprodukt liefert jeder Abbildung einen „Spiegelpartner" $f^*$. Genau wenn $f$ mit seinem Spiegelpartner **vertauscht** (normal ist), zerfällt der Raum in perpendikuläre Achsen, auf denen $f$ nur streckt — der **Spektralsatz**. Selbstadjungiert macht die Streckfaktoren reell (Hauptachsen), isometrisch macht sie zu Phasen $|\lambda|=1$ (Drehungen). Damit schließt sich der Bogen: Die Eigenwerttheorie aus Teil I wird durch die Geometrie aus Teil III zur *perfekten* Diagonalisierung vollendet.

---

<a id="epilog-das-skript-als-system"></a>
# Epilog — Das Skript als System

Die neun Kapitel bilden **eine** durchgehende Geschichte:

$$
\underbrace{\text{Polynome}\to\text{Faktorisierung}}_{\text{Kap. 0}}
\ \longrightarrow\
\underbrace{\chi_f,\mu_f\to\text{Diag./Trig.}\to\text{Jordan}}_{\text{Kap. 2–4, Werkzeug: Kap. 1}}
$$
$$
\underbrace{\mathbb{C}\ \text{(alles zerfällt)}}_{\text{Kap. 5, Brücke}}
\ \longrightarrow\
\underbrace{\text{Skalarprodukt}\to\text{Orthogonalität, Gram-Schmidt}}_{\text{Kap. 6–7}}
\ \longrightarrow\
\underbrace{\text{Spektralsätze}}_{\text{Kap. 8}}
$$

**Der rote Faden in einem Satz:** *Man klassifiziere lineare Abbildungen bis auf Basiswechsel* (Teil I, über Faktorisierung von $\chi_f$) *und verfeinere dies mit Geometrie zu einer orthonormalen Klassifikation* (Teil III, Spektralsatz). Das eine Prinzip, das beide Teile trägt, ist **„Nullstelle $\Leftrightarrow$ Linearfaktor"** — von Kapitel 0 (Faktorisierung) über Kapitel 2–4 (Eigenwerte) bis Kapitel 8 (Spektrum).



---

<a id="analysis-auf-allgemeinen-linearen-räumen"></a>
# Analysis auf allgemeinen linearen Räumen
<a id="vollständiges-skript-rekonstruiert-aus-vorlesung-bereinigt-und-ergänzt"></a>
### Vollständiges Skript — rekonstruiert aus Vorlesung, bereinigt und ergänzt

---

<a id="vorwort"></a>
## Vorwort

Dieses Skript rekonstruiert den Stoff einer Vorlesung "Analysis 2" (Titel: *Analysis auf allgemeinen linearen Räumen*), die den klassischen Weg von der mehrdimensionalen Differential- und Integralrechnung über eine moderne, raumtheoretische Perspektive aufbaut: Statt sofort im $\mathbb{R}^n$ zu rechnen, wird der gesamte Kalkül zunächst in **beliebigen Banachräumen** entwickelt. Der $\mathbb{R}^n$ erscheint danach nur noch als *Spezialfall*. Dieser Aufbau ist anspruchsvoller als der klassische Weg, aber erheblich lohnender: Man versteht am Ende, *warum* die Formeln so aussehen, wie sie aussehen, und nicht nur, *dass* sie gelten.

Die Kapitelstruktur folgt einer inneren Logik:

$$
\text{Topologie} \to \text{Metrik} \to \text{Norm (Banachraum)} \to \text{Ableitung} \to \text{Extrema} \to \text{Integration} \to \text{Kurvenintegrale} \to \text{Komplexe Analysis}
$$

Jeder Pfeil bedeutet: Die rechte Theorie *braucht* die Struktur der linken, um überhaupt formuliert werden zu können. Ohne einen Konvergenzbegriff (Topologie) kann man nicht von Stetigkeit sprechen; ohne Stetigkeit nicht von Differenzierbarkeit; ohne Differenzierbarkeit nicht von Extrema; usw.

---

<a id="kapitel-1-topologische-räume"></a>
# Kapitel 1: Topologische Räume

<a id="motivation-9"></a>
## Motivation

**Welches Problem lösen wir?**

In der Analysis 1 haben Sie Grenzwerte, Stetigkeit und Konvergenz für Funktionen $f:\mathbb{R}\to\mathbb{R}$ kennengelernt — definiert über den Betrag $|x-y|$. Nun wollen wir dieselben Konzepte auf sehr viel allgemeineren Räumen zur Verfügung haben: Räume von Funktionen, Räume von Matrizen, Räume von Folgen. Auf diesen Räumen gibt es *a priori* keinen "Abstand". Wir brauchen daher ein Fundament, das noch schwächer ist als eine Metrik, aber stark genug, um von **Nähe, Konvergenz und Stetigkeit** zu sprechen: die **Topologie**.

**Historischer Kontext.** Die Topologie entstand aus der Frage, welche Eigenschaften geometrischer Objekte unter stetigen Verformungen erhalten bleiben (Poincaré, Ende 19. Jh.). Felix Hausdorff abstrahierte 1914 den Begriff der "Umgebung" so, dass er unabhängig von einer konkreten Abstandsmessung wird. Genau diese Hausdorff'sche Idee — Nähe über *Umgebungssysteme* statt über Zahlen zu definieren — ist der Ausgangspunkt dieses Kapitels.

<a id="intuition-9"></a>
## Intuition

Stellen Sie sich vor, Sie wollen einer Person mitteilen, "wie nahe" zwei Punkte beieinander liegen, ohne ihr eine Maßeinheit zu geben. Sie können stattdessen sagen: *"Zu jedem Punkt $x$ gebe ich dir eine Familie von 'Nachbarschaften' $N(x)$ — Mengen, die $x$ "einschließen". Zwei Punkte gelten als nah, wenn sie in derselben kleinen Nachbarschaft liegen."*

Das ist die Grundidee der **Umgebungstopologie**: Statt eines Abstands $d(x,y)\in\mathbb{R}_{\ge 0}$ geben wir jedem Punkt $x$ eine Kollektion von Mengen $N(x)$ vor — seine "Umgebungen". Die Axiome, die wir gleich formulieren, stellen sicher, dass sich dieses System so verhält, wie man es intuitiv von "Nähe" erwartet: Umgebungen enthalten den Punkt selbst, größere Mengen um Umgebungen sind wieder Umgebungen, und man kann Umgebungen "verkleinern".

Eine gute Analogie: Stellen Sie sich eine Familie von "Nebelglocken" vor, die man über einen Punkt $x$ stülpen kann. Je "dichter" der Nebel, desto kleiner die Glocke — aber es gibt keine "kleinste" Glocke, sondern beliebig kleine.

<a id="formale-definitionen-9"></a>
## Formale Definitionen

<a id="definition-11-topologischer-raum-umgebungstopologie"></a>
### Definition 1.1 (Topologischer Raum / Umgebungstopologie)

Sei $X$ eine Menge. Eine Abbildung
$$
N: X \to \mathcal{P}(\mathcal{P}(X)), \qquad x \mapsto N(x)
$$
(d.h. $N(x)$ ist eine Familie von Teilmengen von $X$) heißt **Umgebungstopologie** auf $X$, falls für alle $x \in X$ gilt:

| Axiom | Aussage | Bedeutung |
|---|---|---|
| (i) | $U \in N(x) \Rightarrow x \in U$ | Jede Umgebung von $x$ enthält $x$ selbst |
| (ii) | $V \subseteq X,\ \exists U \in N(x): U \subseteq V \Rightarrow V \in N(x)$ | Obermengen von Umgebungen sind Umgebungen |
| (iii) | $U, V \in N(x) \Rightarrow U \cap V \in N(x)$ | Endliche Schnitte von Umgebungen sind Umgebungen |
| (iv) | $\forall U \in N(x)\ \exists V \in U,\ V \subseteq U: \forall y \in V,\ V \in N(y)$ | Jede Umgebung enthält eine "offene" Umgebung |

Das Paar $(X, N)$ heißt **topologischer Raum**.

> **Warum genau diese vier Axiome?** (i) garantiert, dass "Umgebung von $x$" tatsächlich etwas über die Nähe *zu* $x$ aussagt. (ii) sorgt dafür, dass "Umgebung sein" keine Größenbeschränkung ist — nur eine Mindestanforderung. (iii) stellt sicher, dass wir zwei Näherungsbedingungen gleichzeitig verlangen dürfen (wichtig z.B. für die Eindeutigkeit von Grenzwerten). (iv) ist das technisch wichtigste Axiom: Es erlaubt, von *offenen* Umgebungen zu sprechen, die überall in sich selbst offen "bleiben" — das Fundament für Definition 1.2.

<a id="definition-12-offene-und-abgeschlossene-mengen"></a>
### Definition 1.2 (Offene und abgeschlossene Mengen)

Sei $(X,N)$ ein topologischer Raum.

$$
O \subseteq X \text{ heißt \textbf{offen}} \quad :\Leftrightarrow \quad \forall x \in O:\ O \in N(x)
$$

$$
A \subseteq X \text{ heißt \textbf{abgeschlossen}} \quad :\Leftrightarrow \quad A^c = X \setminus A \text{ ist offen}
$$

**Intuition:** Eine Menge ist offen, wenn sie für *jeden* ihrer Punkte eine "Sicherheitszone" bildet — es gibt keinen Punkt am "Rand", der aus der Menge herausragt.

<a id="definition-14-umgebungsbasis"></a>
### Definition 1.4 (Umgebungsbasis)

Eine Sammlung $\mathcal{B}$ offener Mengen heißt **Umgebungsbasis**, wenn jede offene Menge Vereinigung von Mengen aus $\mathcal{B}$ ist.

**Beispiel:** In $\mathbb{R}$ mit der Standardtopologie bildet
$$
\mathcal{B} = \{I_\varepsilon(x) : x \in \mathbb{Q},\ \varepsilon \in \mathbb{Q}_{>0}\}, \qquad I_\varepsilon(x) = (x-\varepsilon, x+\varepsilon)
$$
eine **abzählbare** Umgebungsbasis — ein Beispiel für einen sogenannten *zweitabzählbaren* Raum. Dies ist technisch relevant für Lemma 1.10 (Folgenkriterium der Stetigkeit).

<a id="definition-15-hausdorff-raum"></a>
### Definition 1.5 (Hausdorff-Raum)

$(X,N)$ heißt **Hausdorff'sch** (oder $T_2$), falls
$$
\forall x \neq y \in X\ \exists U_x \in N(x),\ U_y \in N(y): \quad U_x \cap U_y = \emptyset.
$$

**Intuition:** Verschiedene Punkte lassen sich immer durch disjunkte Umgebungen "trennen" — es gibt kein "Verschmieren" der Punkte. Fast alle in der Praxis relevanten Räume (insbesondere alle metrischen Räume, siehe Kapitel 2) sind Hausdorff'sch.

<a id="definition-16-konvergenz"></a>
### Definition 1.6 (Konvergenz)

Sei $(X,N)$ topologischer Raum, $a: \mathbb{N} \to X$ eine Folge. $a$ heißt **konvergent** gegen $x \in X$, falls
$$
\forall U \in N(x)\ \exists n_0 \in \mathbb{N}\ \forall n \geq n_0:\ a_n \in U.
$$
Man schreibt dann $x = \lim_{n\to\infty} a_n$ und nennt $x$ einen **Grenzwert** von $a$.

> **Warnung:** In allgemeinen topologischen Räumen ist der Grenzwert **nicht eindeutig**! Erst die Hausdorff-Eigenschaft garantiert Eindeutigkeit (siehe Lemma 1.7).

<a id="definition-18-stetigkeit-punktweise"></a>
### Definition 1.8 (Stetigkeit — punktweise)

Seien $(X,N), (Y,M)$ topologische Räume, $f: X \to Y$. $f$ heißt **stetig bei $x$**, falls
$$
\forall U \in M(f(x))\ \exists V \in N(x):\ f(V) \subseteq U.
$$

*Klärung eines häufigen Verständnisproblems (in der Mitschrift als offene Frage markiert):* Warum brauchen wir hier keine explizite "$\varepsilon$-$\delta$"-artige Definition? Weil die Umgebungssysteme $N(x)$ und $M(f(x))$ genau die Rolle von "$\varepsilon$-Bällen" übernehmen — die Definition ist eine direkte Verallgemeinerung der $\varepsilon$-$\delta$-Stetigkeit, bei der die $\varepsilon$-Bälle durch beliebige Umgebungen ersetzt wurden.

<a id="eigenschaften-9"></a>
## Eigenschaften

<a id="satz-13-eigenschaften-offener-mengen"></a>
### Satz 1.3 (Eigenschaften offener Mengen)

Sei $(X,N)$ topologischer Raum. Dann gilt:

1. $\emptyset$ und $X$ sind offen.
2. Die Vereinigung **beliebig vieler** offener Mengen ist offen.
3. Der Durchschnitt **endlich vieler** offener Mengen ist offen.

**Beweis von (3)** *(Beweisstil: direkter Nachweis über die Umgebungsdefinition)*

Seien $O, O'$ offen. Ist $O \cap O' = \emptyset$, so ist die Aussage trivial (die leere Menge ist offen nach (1)).

Sei also $O \cap O' \neq \emptyset$. Für beliebiges $x \in O \cap O'$ gilt: Da $O$ offen ist, folgt $O \in N(x)$ (Definition 1.2). Da $O'$ offen ist, folgt analog $O' \in N(x)$. Nach Axiom (iii) der Umgebungstopologie gilt dann
$$
O \cap O' \in N(x).
$$
Da $x \in O \cap O'$ beliebig war, ist $O \cap O'$ nach Definition 1.2 offen. $\blacksquare$

**Wichtiger Kommentar:** Diese Eigenschaften sind der Grund, warum man in der modernen Literatur einen topologischen Raum meist *direkt* über ein System offener Mengen $\mathcal{O} \subseteq \mathcal{P}(X)$ mit den Eigenschaften 1.–3. definiert (die sogenannte **Mengensystem-Definition**). Die Umgebungsdefinition (Def. 1.1) und die Mengensystem-Definition sind **äquivalent** — man kann von einer zur anderen übergehen:
$$
N(x) := \{U \subseteq X : \exists O \in \mathcal{O},\ x \in O \subseteq U\}.
$$

> **Achtung — Standard-Gegenbeispiel:** Der Durchschnitt *unendlich* vieler offener Mengen muss nicht offen sein! In $\mathbb{R}$ mit Standardtopologie:
> $$
> \bigcap_{n\in\mathbb{N}} \left(-\tfrac{1}{n}, \tfrac{1}{n}\right) = \{0\}
> $$
> und $\{0\}$ ist **nicht** offen (jede Umgebung von $0$ enthält ein Intervall, $\{0\}$ aber nicht). Dies ist einer der häufigsten Fallstricke beim ersten Kontakt mit Topologie.

<a id="beispiele-topologischer-räume"></a>
### Beispiele topologischer Räume

| Name | Definition von $N(x)$ | Eigenschaften |
|---|---|---|
| **Standardtopologie auf $\mathbb{R}$** | Menge aller Teilmengen von $\mathbb{R}$, die eine offene Menge (im $\varepsilon$-Sinn) enthalten, die $x$ enthält | Hausdorff, zweitabzählbar |
| **Diskrete Topologie** | $N(x) \ni \{x\}$; jede Teilmenge, die $x$ enthält, ist Umgebung | Hausdorff, aber jede Teilmenge offen — "maximal fein" |
| **Indiskrete (triviale) Topologie** | $N(x) = \{X\}$ für alle $x$ | **Nicht** Hausdorff (falls $|X|>1$) — "maximal grob" |

Diese drei Beispiele markieren die beiden Extreme des Spektrums: Die diskrete Topologie trennt *alles* voneinander (jeder Punkt ist "isoliert"), die indiskrete Topologie trennt *nichts* (alle Punkte sind "verschmiert"). Die Standardtopologie liegt dazwischen.

<a id="lemma-17-eindeutigkeit-von-grenzwerten-in-hausdorff-räumen"></a>
### Lemma 1.7 (Eindeutigkeit von Grenzwerten in Hausdorff-Räumen)

**Aussage:** Ist $X$ Hausdorff'sch, so hat jede konvergente Folge **höchstens einen** Grenzwert.

**Voraussetzungen:** $(X,N)$ Hausdorff'sch.

**Bedeutung:** Ohne diese Eigenschaft wäre der Ausdruck "der Grenzwert" sinnlos — er müsste immer als "ein Grenzwert" gelesen werden. Fast die gesamte Analysis beruht implizit auf der Eindeutigkeit von Grenzwerten.

**Beweisidee** *(Widerspruchsbeweis)*: Angenommen $a_n \to x$ und $a_n \to y$ mit $x \neq y$. Nach Hausdorff-Eigenschaft gibt es disjunkte Umgebungen $U_x \in N(x)$, $U_y \in N(y)$. Wegen Konvergenz liegen ab einem Index $n_0$ *alle* Folgenglieder sowohl in $U_x$ als auch in $U_y$ — Widerspruch zu $U_x \cap U_y = \emptyset$. $\blacksquare$

<a id="lemma-19-charakterisierung-von-stetigkeit-über-urbilder-offener-mengen"></a>
### Lemma 1.9 (Charakterisierung von Stetigkeit über Urbilder offener Mengen)

**Aussage:** $f: X \to Y$ ist stetig **für alle** $x \in X$ genau dann, wenn für jede offene Menge $O \subseteq Y$ das Urbild $f^{-1}(O) := \{x \in X: f(x) \in O\}$ offen in $X$ ist.

**Bedeutung:** Dies ist die *wichtigste* Charakterisierung von Stetigkeit in der Topologie — sie wird in praktisch jedem Beweis über stetige Funktionen benutzt (z.B. beim Beweis, dass stetige Bilder kompakter Mengen kompakt sind, Lemma 1.14).

**Beweis** *(Beweisstil: Äquivalenzbeweis, zwei Implikationsrichtungen)*

**"$\Rightarrow$":** Sei $f$ stetig für alle $x \in X$, sei $O \subseteq Y$ offen. Sei $x \in f^{-1}(O)$ beliebig, d.h. $f(x) \in O$. Da $O$ offen ist, gilt $O \in M(f(x))$. Nach Stetigkeit bei $x$ existiert $V \in N(x)$ mit $f(V) \subseteq O$, also $V \subseteq f^{-1}(O)$. Da jede Umgebung eine offene Umgebung enthält (Axiom (iv)), enthält $f^{-1}(O)$ eine offene Umgebung von $x$; also ist $x$ ein innerer Punkt. Da $x$ beliebig war, ist $f^{-1}(O)$ offen.

**"$\Leftarrow$":** Sei $f^{-1}(O)$ offen für alle offenen $O \subseteq Y$. Sei $x \in X$, $U \in M(f(x))$. Da jede Umgebung eine offene Umgebung enthält, gibt es offenes $O$ mit $f(x) \in O \subseteq U$. Nach Voraussetzung ist $f^{-1}(O)$ offen und enthält $x$, also $f^{-1}(O) \in N(x)$. Setze $V := f^{-1}(O)$; dann gilt $f(V) \subseteq O \subseteq U$. Also ist $f$ stetig bei $x$. $\blacksquare$

<a id="lemma-110-folgenkriterium-der-stetigkeit-unter-erster-abzählbarkeit"></a>
### Lemma 1.10 (Folgenkriterium der Stetigkeit unter erster Abzählbarkeit)

**Aussage:** Seien $X, Y$ topologische Räume, $x\in X$ habe eine **abzählbare Umgebungsbasis** $\{N_i : i \in \mathbb{N}\} \subseteq N(x)$ (d.h. für jedes $U \in N(x)$ existiert $i$ mit $N_i \subseteq U$). Dann ist $f$ genau dann stetig bei $x$, wenn für **jede** Folge $a$ in $X$ mit $\lim a_n = x$ gilt $\lim f(a_n) = f(x)$.

> **Wichtige Klarstellung (behebt eine offene Frage in der ursprünglichen Mitschrift):** Diese Äquivalenz gilt **nicht** in beliebigen topologischen Räumen! Die Voraussetzung "abzählbare Umgebungsbasis bei $x$" (auch **erste Abzählbarkeit** genannt) ist essentiell für die Rückrichtung. Ohne sie kann es Funktionen geben, die folgenstetig, aber nicht stetig sind (Standardgegenbeispiel: Ordinalzahlraum $[0,\omega_1]$ mit Ordnungstopologie — für diese Vorlesung nicht examensrelevant, aber gut zu wissen, *dass* die Voraussetzung nicht überflüssig ist).

**Beweis:**

**"$\Rightarrow$" (Stetigkeit $\Rightarrow$ Folgenstetigkeit), gilt ohne erste Abzählbarkeit:**
Sei $f$ stetig bei $x$, sei $\lim a_n = x$. Sei $V \in M(f(x))$ beliebig. Wegen Stetigkeit existiert $U \in N(x)$ mit $f(U) \subseteq V$. Wegen $\lim a_n = x$ existiert $n_0$ mit $a_n \in U$ für alle $n \geq n_0$. Dann gilt $f(a_n) \in f(U) \subseteq V$ für alle $n\geq n_0$. Da $V$ beliebig war, folgt $\lim f(a_n) = f(x)$.

**"$\Leftarrow$" (Folgenstetigkeit $\Rightarrow$ Stetigkeit), benötigt erste Abzählbarkeit:**
Wir führen einen Widerspruchsbeweis. Angenommen $f$ ist **nicht** stetig bei $x$. Dann existiert eine offene Umgebung $U \in M(f(x))$, sodass $f^{-1}(U)$ **nicht** offen ist — insbesondere gibt es kein $V \in N(x)$ mit $f(V) \subseteq U$.

Sei $\{N_i\}_{i\in\mathbb{N}}$ die abzählbare Umgebungsbasis bei $x$. Bilde für jedes $i$ die Menge $\hat{N}_i := N_1 \cap \dots \cap N_i$ (nach Axiom (iii) wieder eine Umgebung von $x$, sogar eine "schrumpfende" Kette). Da kein $N_i$ (und damit auch kein $\hat N_i$) ganz in $f^{-1}(U)$ liegt, wähle für jedes $i$ ein Element
$$
x_i \in \hat N_i \setminus f^{-1}(U).
$$
Dann gilt $\lim_{i\to\infty} x_i = x$ (da die $\hat N_i$ eine schrumpfende Umgebungsbasis bilden), aber $f(x_i) \notin U$ für alle $i$, also $\lim f(x_i) \neq f(x)$ — Widerspruch zur Folgenstetigkeit. $\blacksquare$

<a id="beispiele-9"></a>
## Beispiele

**Beispiel 1 (leicht):** Zeigen Sie, dass in der diskreten Topologie **jede** Funktion $f: X \to Y$ stetig ist (für beliebige Topologie auf $Y$).
*Lösung:* Für jede offene Menge $O \subseteq Y$ ist $f^{-1}(O) \subseteq X$ automatisch offen, da in der diskreten Topologie *jede* Teilmenge offen ist. Nach Lemma 1.9 folgt Stetigkeit.

**Beispiel 2 (mittel):** Zeigen Sie: Ist $Y$ Hausdorff'sch und $f, g: X \to Y$ stetig, so ist $\{x \in X : f(x) = g(x)\}$ abgeschlossen.
*Lösungsskizze:* Betrachte $h := (f,g): X \to Y \times Y$ (stetig, da $f,g$ stetig) und die Diagonale $\Delta = \{(y,y): y \in Y\}$. Da $Y$ Hausdorff'sch ist, ist $\Delta$ abgeschlossen in $Y \times Y$ (Übung: zeigen Sie dies direkt über die Hausdorff-Definition). Dann ist $\{x : f(x)=g(x)\} = h^{-1}(\Delta)$ abgeschlossen als stetiges Urbild einer abgeschlossenen Menge.

**Beispiel 3 (schwer):** Zeigen Sie, dass $[0,1]$ mit Standardtopologie keine abzählbare *diskrete* Teilmenge unendlicher Mächtigkeit als abgeschlossene Teilmenge ohne Häufungspunkt besitzen kann.
*(Dies ist ein Vorgriff auf Kompaktheit — siehe unten.)*

<a id="gegenbeispiele-9"></a>
## Gegenbeispiele

- **Nicht-Eindeutigkeit von Grenzwerten ohne Hausdorff:** In der indiskreten Topologie auf $X=\{a,b\}$ konvergiert *jede* Folge gegen *jeden* Punkt — Grenzwerte sind hier bedeutungslos.
- **Unendliche Schnitte offener Mengen:** siehe oben, $\bigcap_n (-1/n,1/n) = \{0\}$ ist nicht offen.
- **Folgenstetigkeit ohne erste Abzählbarkeit:** siehe Bemerkung zu Lemma 1.10.

<a id="typische-klausuraufgaben-9"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Erkennungsmerkmal | Strategie |
|---|---|---|
| "Zeigen Sie, dass $N(x):=\dots$ eine Umgebungstopologie definiert" | Explizite Konstruktion von $N(x)$ gegeben | Alle vier Axiome (i)–(iv) *einzeln* nachprüfen; Axiom (iv) wird oft vergessen! |
| "Ist $(X,N)$ Hausdorff'sch?" | Konkreter Raum gegeben | Für zwei beliebige Punkte explizit disjunkte Umgebungen konstruieren (oder Gegenbeispiel angeben) |
| "Zeigen Sie Stetigkeit über Urbilder" | Abstrakte Abbildung zwischen topologischen Räumen | Lemma 1.9 anwenden statt $\varepsilon$-$\delta$-Argumente |
| "Warum funktioniert das Folgenkriterium hier (nicht)?" | Raum ohne offensichtliche Metrik | Prüfen, ob erste Abzählbarkeit vorliegt |

<a id="typische-fehler-9"></a>
## Typische Fehler

1. **Verwechslung von "offen" und "Umgebung":** Eine Umgebung von $x$ muss *nicht* offen sein (nur eine offene Umgebung *enthalten*, Axiom (iv)). Häufiger Fehler: Studierende behandeln $N(x)$ als hätte es nur offene Elemente.
2. **Unendliche Schnitte für offen halten:** siehe Gegenbeispiel oben — nur *endliche* Schnitte offener Mengen sind garantiert offen.
3. **Folgenstetigkeit mit Stetigkeit gleichsetzen ohne Abzählbarkeitsvoraussetzung zu prüfen.**
4. **Hausdorff-Eigenschaft für selbstverständlich halten:** Nicht jeder in Aufgaben auftauchende topologische Raum ist automatisch Hausdorff'sch — immer explizit prüfen, bevor Eindeutigkeit von Grenzwerten verwendet wird.

<a id="verbindungen-9"></a>
## Verbindungen

- Kapitel 2 (Metrische Räume) liefert die **wichtigste Klasse** von Beispielen topologischer Räume: Jede Metrik induziert eine Topologie (Definition 1.16), die automatisch Hausdorff'sch und zweitabzählbar ist — dort gilt also *immer* das Folgenkriterium (Lemma 1.10) uneingeschränkt.
- Der Kompaktheitsbegriff (weiter unten in diesem Kapitel) und der Zusammenhangsbegriff sind rein topologische Konzepte, die in Kapitel 3 (Banachräume) und Kapitel 5 (Extrema) zentral wiederverwendet werden (Extremwertsatz, Satz 1.68).
- Lemma 1.9 (Stetigkeit über Urbilder) ist die Grundlage für den Beweis, dass stetige Bilder kompakter Mengen kompakt sind (Lemma 1.14) — ein Baustein des Extremwertsatzes.

---

<a id="zwischenschritt-zusammenhang-kompaktheit-topologisch"></a>
## Zwischenschritt: Zusammenhang, Kompaktheit (topologisch)

<a id="definition-114-zusammenhängender-raum"></a>
### Definition 1.14 (Zusammenhängender Raum)

Ein topologischer Raum $X$ heißt **zusammenhängend**, wenn $X$ *nicht* die Vereinigung zweier disjunkter, nicht-leerer offener Mengen ist. Eine Teilmenge $A \subseteq X$ heißt zusammenhängend, wenn sie als Teilraum (mit der induzierten Topologie) zusammenhängend ist.

**Intuition:** Ein zusammenhängender Raum lässt sich nicht in zwei "getrennte Stücke" zerlegen — man kann ihn nicht mit einer Schere durchschneiden, ohne dass die beiden Teile sich "berühren".

<a id="satz-112-zwischenwertsatz-topologische-version"></a>
### Satz 1.12 (Zwischenwertsatz, topologische Version)

**Aussage:** Seien $X, Y$ topologische Räume, $f: X \to Y$ stetig, $X$ zusammenhängend. Dann ist $f(X)$ zusammenhängend.

**Bedeutung:** Dies ist die abstrakte Wurzel des klassischen Zwischenwertsatzes aus Analysis 1: Ist $X = [a,b] \subseteq \mathbb{R}$ (zusammenhängend) und $f$ stetig mit Werten in $\mathbb{R}$, so ist $f([a,b])$ zusammenhängend, also — wie man zeigen kann — ein Intervall. Damit nimmt $f$ jeden Wert zwischen $f(a)$ und $f(b)$ an.

**Beweis** *(Beweisstil: Widerspruchsbeweis; dieser Beweis fehlte in der Mitschrift vollständig und wird hier ergänzt)*

Angenommen $f(X)$ ist **nicht** zusammenhängend. Dann existieren nicht-leere, disjunkte, in $f(X)$ (mit Teilraumtopologie) offene Mengen $O_1, O_2$ mit $f(X) = O_1 \cup O_2$. Da $O_1, O_2$ offen in der Teilraumtopologie von $f(X)$ sind, existieren offene Mengen $\tilde O_1, \tilde O_2 \subseteq Y$ mit $O_i = \tilde O_i \cap f(X)$.

Betrachte $U_i := f^{-1}(\tilde O_i) = f^{-1}(O_i)$ für $i=1,2$. Nach Lemma 1.9 (Stetigkeit über Urbilder) sind $U_1, U_2 \subseteq X$ offen. Da $O_1 \cup O_2 = f(X)$, folgt $U_1 \cup U_2 = X$. Da $O_1 \cap O_2 = \emptyset$, folgt $U_1 \cap U_2 = \emptyset$. Da $O_1, O_2 \neq \emptyset$, sind auch $U_1, U_2 \neq \emptyset$ (jedes Element von $O_i$ hat ein Urbild in $X$).

Damit ist $X = U_1 \cup U_2$ eine Zerlegung in zwei disjunkte, nicht-leere offene Mengen — Widerspruch zur Zusammenhangsvoraussetzung an $X$. $\blacksquare$

<a id="definition-117-kompaktheit"></a>
### Definition 1.17 (Kompaktheit)

Sei $X$ topologischer Raum, $K \subseteq X$. $K$ heißt **kompakt**, wenn jede **offene Überdeckung** von $K$ eine **endliche Teilüberdeckung** besitzt:
$$
\forall (O_\alpha)_{\alpha \in A} \text{ offen mit } K \subseteq \bigcup_{\alpha \in A} O_\alpha \quad \exists E \subseteq A \text{ endlich}: \quad K \subseteq \bigcup_{\alpha \in E} O_\alpha.
$$

**Intuition:** Kompaktheit ist eine Art "Endlichkeit im Unendlichen". Auch wenn $K$ unendlich viele Punkte hat, reichen *endlich viele* der überdeckenden Mengen aus, um $K$ vollständig abzudecken — man kann "nicht ins Unendliche entkommen" oder "sich am Rand verlieren".

**Klassisches Gegenbeispiel für Nicht-Kompaktheit:** $(0,1) \subseteq \mathbb{R}$ mit der Überdeckung $O_n = (1/n, 1)$ für $n \in \mathbb{N}$: Es gibt keine endliche Teilüberdeckung, da für jede endliche Teilmenge $E$ das Element $\min_{n \in E} 1/n =: \varepsilon$ existiert und $(0, \varepsilon)$ nicht überdeckt wird.

<a id="lemma-114-stetige-bilder-kompakter-mengen-sind-kompakt"></a>
### Lemma 1.14 (Stetige Bilder kompakter Mengen sind kompakt)

**Aussage:** Seien $X, Y$ topologische Räume, $f: X \to Y$ stetig, $K \subseteq X$ kompakt. Dann ist $f(K) \subseteq Y$ kompakt.

**Bedeutung:** Dies ist der zentrale Baustein für den **Extremwertsatz** (Satz 1.68, Kapitel 5): Eine stetige reellwertige Funktion auf einem Kompaktum nimmt Maximum und Minimum an.

**Beweis** *(Beweisstil: direkte Konstruktion einer endlichen Teilüberdeckung)*

Sei $(O_\alpha)_{\alpha \in A}$ eine offene Überdeckung von $f(K)$. Nach Lemma 1.9 sind die Mengen $f^{-1}(O_\alpha)$ offen in $X$. Da $(O_\alpha)$ ganz $f(K)$ überdeckt, überdecken die $f^{-1}(O_\alpha)$ ganz $K$. Da $K$ kompakt ist, existiert eine endliche Teilmenge $E \subseteq A$ mit
$$
K \subseteq \bigcup_{\alpha \in E} f^{-1}(O_\alpha).
$$
Anwendung von $f$ liefert
$$
f(K) \subseteq f\left(\bigcup_{\alpha \in E} f^{-1}(O_\alpha)\right) = \bigcup_{\alpha \in E} f(f^{-1}(O_\alpha)) \subseteq \bigcup_{\alpha \in E} O_\alpha.
$$
Also ist $(O_\alpha)_{\alpha \in E}$ eine endliche Teilüberdeckung von $f(K)$. $\blacksquare$

---

<a id="kapitel-2-metrische-räume"></a>
# Kapitel 2: Metrische Räume

<a id="motivation-10"></a>
## Motivation

**Welches Problem lösen wir?**

Topologische Räume sind extrem allgemein — zu allgemein, um konkret zu rechnen. In der Praxis will man Abstände *messen*, nicht nur qualitativ von "Nähe" sprechen. Die **Metrik** ist die naheliegendste Zusatzstruktur: eine Funktion $d(x,y)$, die den Abstand zweier Punkte als reelle Zahl angibt und sich intuitiv "abstandsartig" verhält (Symmetrie, Dreiecksungleichung).

**Warum reicht Topologie allein nicht?** Mit einer Metrik können wir Cauchy-Folgen definieren, Vollständigkeit fordern, und — ganz entscheidend für die spätere Differentialrechnung — Approximationsgüten quantifizieren ("wie nah ist $f(x+h)$ an $f(x)$, gemessen in $h$"). Ohne Metrik (nur mit Topologie) ist "Konvergenzgeschwindigkeit" nicht einmal definierbar.

<a id="intuition-10"></a>
## Intuition

Eine Metrik ist die Formalisierung des "gesunden Menschenverstands" über Entfernungen: Der Abstand zwischen zwei verschiedenen Punkten ist positiv, der Abstand eines Punktes zu sich selbst ist null, der Abstand ist symmetrisch (Hin- und Rückweg gleich lang), und ein Umweg über einen dritten Punkt ist nie kürzer als der direkte Weg (**Dreiecksungleichung**) — das ist buchstäblich die Aussage, dass in einem Dreieck jede Seite kürzer ist als die Summe der anderen beiden.

<a id="formale-definitionen-10"></a>
## Formale Definitionen

<a id="definition-115-metrik-metrischer-raum"></a>
### Definition 1.15 (Metrik, metrischer Raum)

Ein **metrischer Raum** ist eine Menge $M$ zusammen mit einer Abbildung $d: M \times M \to \mathbb{R}$, sodass für alle $x,y,z \in M$:

$$
\begin{aligned}
\text{(i)}\quad & d(x,y) \geq 0 \\
\text{(ii)}\quad & d(x,y) = 0 \iff x = y \\
\text{(iii)}\quad & d(x,y) = d(y,x) \quad \text{(Symmetrie)}\\
\text{(iv)}\quad & d(x,y) \leq d(x,z) + d(z,y) \quad \text{(Dreiecksungleichung)}
\end{aligned}
$$

$d$ heißt **Metrik**.

> **Bemerkung (Redundanz von (i)):** Axiom (i) folgt bereits aus (ii)–(iv): Setze in der Dreiecksungleichung $z=x$: $d(x,y)\le d(x,x)+d(x,y)$, was mit (ii) trivial ist — stattdessen setze $z=y$ in $0=d(x,x)\le d(x,y)+d(y,x)=2d(x,y)$ (mit (iii)), also $d(x,y)\ge 0$. Die Vorlesungsmitschrift verweist an dieser Stelle korrekt auf diese Übung.

<a id="definition-116-metrische-topologie"></a>
### Definition 1.16 (Metrische Topologie)

Sei $(M,d)$ metrischer Raum. Die **metrische Topologie** auf $M$ ist die kleinste Umgebungstopologie, die alle Mengen der Form
$$
U_\varepsilon(x) := \{y \in M : d(x,y) < \varepsilon\}, \qquad x \in M,\ \varepsilon > 0
$$
(die sogenannten **offenen $\varepsilon$-Bälle**) enthält.

**Fundamentale Tatsache:** Jeder metrische Raum ist automatisch:
- **Hausdorff'sch** (trenne $x\neq y$ mit $\varepsilon := d(x,y)/2$: dann sind $U_\varepsilon(x)$ und $U_\varepsilon(y)$ disjunkt wegen der Dreiecksungleichung),
- **erst-abzählbar** (die Bälle $U_{1/n}(x)$, $n \in \mathbb{N}$, bilden eine abzählbare Umgebungsbasis bei $x$).

Damit gilt in jedem metrischen Raum **uneingeschränkt** das Folgenkriterium der Stetigkeit (Lemma 1.10) und die Eindeutigkeit von Grenzwerten (Lemma 1.7). Dies ist der Hauptgrund, warum metrische Räume in der Praxis so viel angenehmer sind als allgemeine topologische Räume.

<a id="definition-117-cauchy-folgen"></a>
### Definition 1.17 (Cauchy-Folgen)

Sei $(M,d)$ metrischer Raum, $a: \mathbb{N} \to M$ Folge. $a$ heißt **Cauchy-Folge**, falls
$$
\forall \varepsilon > 0\ \exists n_0 \in \mathbb{N}\ \forall n,m \geq n_0:\quad d(a_n, a_m) < \varepsilon.
$$

**Intuition:** Die Folgenglieder rücken beliebig nah zusammen — unabhängig davon, ob sie tatsächlich gegen einen (im Raum vorhandenen!) Grenzwert konvergieren. Das ist der entscheidende begriffliche Unterschied zu Konvergenz: Cauchy-Eigenschaft ist eine *interne* Bedingung an die Folge, Konvergenz eine *externe* (verlangt Existenz eines Grenzwertes im Raum).

<a id="definition-120-vollständigkeit"></a>
### Definition 1.20 (Vollständigkeit)

$(M,d)$ heißt **vollständig**, falls **jede** Cauchy-Folge in $M$ konvergiert (gegen ein Element von $M$).

<a id="definition-121-dichtheit"></a>
### Definition 1.21 (Dichtheit)

$D \subseteq M$ heißt **dicht** in $(M,d)$, falls
$$
\forall x \in M\ \exists (a_n)_{n} \subseteq D: \quad x = \lim_{n\to\infty} a_n.
$$

**Intuition:** Jeder Punkt des Raumes lässt sich beliebig gut durch Punkte aus $D$ approximieren. Klassisches Beispiel: $\mathbb{Q}$ ist dicht in $\mathbb{R}$.

<a id="eigenschaften-10"></a>
## Eigenschaften

<a id="lemma-118-charakterisierung-von-konvergenz-über-die-metrik"></a>
### Lemma 1.18 (Charakterisierung von Konvergenz über die Metrik)

$$
\lim_{n\to\infty} a_n = x \quad \iff \quad \lim_{n\to\infty} d(a_n,x) = 0.
$$

Dies reduziert Konvergenz in $(M,d)$ auf gewöhnliche reelle Konvergenz der Zahlenfolge $(d(a_n,x))_n$ — der Grund, warum metrische Räume so rechnerfreundlich sind.

<a id="lemma-119-konvergent-rightarrow-cauchy-aber-nicht-umgekehrt"></a>
### Lemma 1.19 (Konvergent $\Rightarrow$ Cauchy, aber nicht umgekehrt)

**Aussage:** In jedem metrischen Raum ist jede konvergente Folge eine Cauchy-Folge. Die Umkehrung gilt **im Allgemeinen nicht**.

**Beweis der Hinrichtung** *(direkter Beweis via Dreiecksungleichung)*:
Sei $\lim a_n = x$. Sei $\varepsilon>0$. Wähle $n_0$ mit $d(a_n,x)<\varepsilon/2$ für $n\ge n_0$. Dann gilt für $n,m\ge n_0$:
$$
d(a_n,a_m) \le d(a_n,x) + d(x,a_m) < \varepsilon/2+\varepsilon/2 = \varepsilon. \qquad \blacksquare
$$

**Gegenbeispiel zur Umkehrung:** $M = \mathbb{Q}$ mit der Standardmetrik $d(x,y)=|x-y|$. Die Folge der Dezimalapproximationen von $\sqrt{2}$ (z.B. $1, 1.4, 1.41, 1.414, \dots$) ist eine Cauchy-Folge in $\mathbb{Q}$, konvergiert aber gegen $\sqrt 2 \notin \mathbb{Q}$ — sie hat also **keinen Grenzwert in $\mathbb{Q}$**. $(\mathbb{Q}, |\cdot|)$ ist somit **nicht vollständig**.

<a id="sätze-9"></a>
## Sätze

<a id="satz-123-vervollständigung-metrischer-räume"></a>
### Satz 1.23 (Vervollständigung metrischer Räume)

**Aussage:** Sei $(M,d)$ metrischer Raum. Sei $\overline M$ die Menge aller Äquivalenzklassen von Cauchy-Folgen in $M$ bezüglich der Äquivalenzrelation
$$
a \sim b \quad :\iff \quad d_c(a,b) := \lim_{n\to\infty} d(a_n,b_n) = 0.
$$
Dann ist $(\overline M, d_c)$ (mit $d_c([a],[b]):=d_c(a,b)$, wohldefiniert) ein **vollständiger** metrischer Raum, und $M$ bettet sich isometrisch und **dicht** in $\overline M$ ein.

**Bedeutung:** Dieser Satz zeigt, dass man *jeden* unvollständigen metrischen Raum "auffüllen" kann, um Vollständigkeit zu erzwingen — die kanonische Konstruktion, mit der man z.B. $\mathbb{R}$ aus $\mathbb{Q}$ gewinnt (via Cauchy-Folgen von Dedekind, alternativ zu Dedekindschnitten).

**Beweisidee** *(Beweisstil: mehrstufige Konstruktion — Wohldefiniertheit, Metrikeigenschaften, Vollständigkeit)*

**Schritt 1 — $d_c$ ist wohldefiniert (der Limes existiert):**
Seien $a,b$ Cauchy-Folgen in $M$. Zu zeigen: $\lim_n d(a_n,b_n)$ existiert. Man zeigt, dass die reelle Folge $(d(a_n,b_n))_n$ selbst eine Cauchy-Folge in $\mathbb{R}$ ist — mittels der sogenannten *umgekehrten Dreiecksungleichung*:
$$
d(a_n,b_n) - d(a_m,b_m) \leq d(a_n,a_m) + d(b_m,b_n).
$$
*(Herleitung: $d(a_n,b_n)\le d(a_n,a_m)+d(a_m,b_m)+d(b_m,b_n)$ nach zweifacher Dreiecksungleichung, umgestellt.)* Da $a,b$ Cauchy-Folgen sind, wird die rechte Seite für $n,m\to\infty$ beliebig klein; symmetrisch erhält man auch die Abschätzung mit vertauschten Rollen, also insgesamt
$$
|d(a_n,b_n)-d(a_m,b_m)| \leq d(a_n,a_m)+d(b_n,b_m) \xrightarrow{n,m\to\infty} 0.
$$
Also ist $(d(a_n,b_n))_n$ Cauchy in $\mathbb{R}$, und da $\mathbb{R}$ vollständig ist, existiert der Grenzwert $d_c(a,b)$.

**Schritt 2 — $d_c$ erfüllt (i), (iii), (iv) einer Metrik, aber (ii) nur "fast":**
Direktes Nachrechnen zeigt $d_c(a,b)\ge 0$, $d_c(a,b)=d_c(b,a)$, und die Dreiecksungleichung überträgt sich im Limes von $d$. Aber: $d_c(a,b)=0$ bedeutet **nicht** $a=b$ als Folgen, sondern nur, dass die Folgen "im Grenzwert zusammenlaufen". Deshalb ist $d_c$ zunächst nur eine **Pseudometrik** — dies motiviert den Übergang zu Äquivalenzklassen.

**Schritt 3 — Äquivalenzrelation und Wohldefiniertheit auf Äquivalenzklassen:**
Man prüft, dass $\sim$ tatsächlich eine Äquivalenzrelation ist (Reflexivität, Symmetrie, Transitivität — Transitivität folgt aus der Dreiecksungleichung für $d_c$) und dass $d_c([a],[b]) := d_c(a,b)$ **unabhängig von den Repräsentanten** ist: Sind $a, \tilde a \in [a]$ und $b$ Cauchy-Folge, so zeigt eine doppelte Dreiecksungleichung
$$
d_c(a,b) \leq d_c(a,\tilde a) + d_c(\tilde a, b) = d_c(\tilde a, b), \qquad d_c(\tilde a, b) \leq d_c(\tilde a, a) + d_c(a,b) = d_c(a,b),
$$
also $d_c(a,b) = d_c(\tilde a, b)$. Auf den Äquivalenzklassen ist $d_c$ dann eine echte Metrik.

**Schritt 4 — Dichtheit von $M$ in $\overline M$:**
Bette $M \hookrightarrow \overline M$ ein via $x \mapsto [\text{konstante Folge } x]$. Für eine beliebige Cauchy-Folge $a$ zeigt man $\lim_{n\to\infty}[a^{(n)}] = [a]$ (wobei $a^{(n)}$ die konstante Folge mit Wert $a_n$ ist), indem man
$$
d_c([a^{(n)}], [a]) = \lim_{m\to\infty} d(a_n,a_m)
$$
betrachtet — dies wird für $n\to\infty$ beliebig klein, da $a$ Cauchy ist. Also liegt jedes Element von $\overline M$ im Abschluss des eingebetteten $M$.

**Schritt 5 — Vollständigkeit von $\overline M$:** (technisch, hier nur skizziert) Man zeigt, dass jede Cauchy-Folge in $\overline M$ mittels der Dichtheit von $M$ durch eine "Diagonalfolge" approximiert werden kann, die selbst eine Cauchy-Folge in $M$ ist und deren Äquivalenzklasse der gesuchte Grenzwert ist. $\blacksquare$

<a id="satz-126-bolzanoweierstraß-in-metrischen-räumen"></a>
### Satz 1.26 (Bolzano–Weierstraß in metrischen Räumen)

**Aussage:** Sei $(M,d)$ metrischer Raum, $K \subseteq M$. Dann gilt:
$$
K \text{ ist kompakt} \quad \iff \quad \text{jede Folge in } K \text{ besitzt eine konvergente Teilfolge mit Grenzwert in } K.
$$

**Bedeutung:** In metrischen Räumen fällt der (topologische) Überdeckungsbegriff von Kompaktheit mit dem intuitiveren **Folgenkompaktheitsbegriff** zusammen. Das ist der Grund, warum man in der Praxis fast immer mit dem Folgenkriterium arbeitet.

**Beweis** *(Beweisstil: zweigeteilter Äquivalenzbeweis)*

**"$\Rightarrow$" (kompakt $\Rightarrow$ jede Folge hat konvergente Teilfolge mit Grenzwert in $K$):**
Kontraposition: Habe eine Folge $a$ in $K$ **keinen** Häufungspunkt in $K$. Dann gilt für jedes $x\in K$: Es existiert $\varepsilon_x>0$, sodass $U_{\varepsilon_x}(x)$ nur endlich viele Folgenglieder enthält (sonst wäre $x$ Häufungspunkt). Die Familie $\{U_{\varepsilon_x}(x)\}_{x\in K}$ ist eine offene Überdeckung von $K$. Wäre $K$ kompakt, gäbe es eine endliche Teilüberdeckung — aber jede der endlich vielen Mengen enthält nur endlich viele Folgenglieder, also insgesamt nur endlich viele. Widerspruch, da die Folge unendlich viele Glieder hat. Also ist $K$ nicht kompakt.

**"$\Leftarrow$" (Folgenkompaktheit $\Rightarrow$ kompakt):** Dies ist die technisch aufwendigere Richtung, bestehend aus zwei Teilschritten:

*Teilschritt (i) — Lebesguezahl-Argument:* Sei $\{O_\alpha\}_{\alpha\in A}$ offene Überdeckung von $K$. Man zeigt zunächst: Es existiert $\varepsilon>0$ ("Lebesgue-Zahl"), sodass für jedes $x\in K$ ein $\alpha\in A$ existiert mit $U_\varepsilon(x)\subseteq O_\alpha$.
*Beweis durch Widerspruch:* Angenommen, für jedes $\varepsilon>0$ existiert $x\in K$ mit $U_\varepsilon(x)\not\subseteq O_\alpha$ für alle $\alpha$. Wähle $\varepsilon=1/n$ und entsprechendes $x_n$; die Folge $(x_n)$ hat nach Voraussetzung eine konvergente Teilfolge mit Grenzwert $y\in K$. Da $\{O_\alpha\}$ Überdeckung ist, liegt $y\in O_{\alpha_0}$ für ein $\alpha_0$; da $O_{\alpha_0}$ offen ist, gibt es $\delta>0$ mit $U_\delta(y)\subseteq O_{\alpha_0}$. Für hinreichend große $n$ (entlang der Teilfolge) gilt $U_{1/n}(x_n)\subseteq U_\delta(y)\subseteq O_{\alpha_0}$ — Widerspruch zur Wahl von $x_n$.

*Teilschritt (ii) — endliche $\varepsilon$-Überdeckbarkeit:* Man zeigt: Für jedes $\varepsilon>0$ lässt sich $K$ mit endlich vielen $\varepsilon$-Bällen überdecken.
*Beweis durch Widerspruch mittels Induktion:* Angenommen nicht. Dann konstruiert man induktiv eine Folge $(a_n)$ in $K$ mit $d(a_n,a_m)\geq \varepsilon$ für alle $n\neq m$ (wähle $a_{n+1}$ außerhalb der Vereinigung der bisherigen $\varepsilon$-Bälle, was nach Annahme möglich ist, da endlich viele Bälle $K$ nicht überdecken). Diese Folge hat aber **keine** konvergente Teilfolge (je zwei Glieder haben Abstand $\geq \varepsilon$) — Widerspruch zur Voraussetzung.

*Zusammenführung:* Aus (i) und (ii) mit $\varepsilon$ = Lebesgue-Zahl folgt: Überdecke $K$ mit endlich vielen $\varepsilon$-Bällen $U_\varepsilon(x_1),\dots,U_\varepsilon(x_k)$; wähle für jeden Ball ein $O_{\alpha_i}\supseteq U_\varepsilon(x_i)$ (existiert nach (i)). Dann ist $\{O_{\alpha_1},\dots,O_{\alpha_k}\}$ die gesuchte endliche Teilüberdeckung. $\blacksquare$

<a id="satz-155-satz-von-heineborel-mathbbrn"></a>
### Satz 1.55 (Satz von Heine–Borel, $\mathbb{R}^n$)

**Aussage:** Eine Menge $K \subseteq \mathbb{R}^n$ ist kompakt $\iff$ $K$ ist **abgeschlossen und beschränkt**.

**Bedeutung:** Dies ist die praktisch mit Abstand wichtigste Kompaktheitscharakterisierung, da "abgeschlossen und beschränkt" viel leichter zu prüfen ist als das abstrakte Überdeckungskriterium. Sie gilt **nur** im $\mathbb{R}^n$ (bzw. endlichdimensionalen normierten Räumen) — **nicht** in allgemeinen (insbesondere unendlichdimensionalen) metrischen oder Banachräumen!

**Beweis** *(Beweisstil: Induktion über die Dimension $n$, kombiniert mit Satz 1.26)*

**"$\Rightarrow$":** Ist $K$ kompakt, so ist $K$ nach Satz 1.26 folgenkompakt. Wäre $K$ unbeschränkt, könnte man eine Folge mit $\|a_n\|\to\infty$ konstruieren — diese hätte keine konvergente Teilfolge (jede Teilfolge wäre ebenfalls unbeschränkt), Widerspruch. Wäre $K$ nicht abgeschlossen, gäbe es einen Häufungspunkt $x \notin K$ von $K$; eine gegen $x$ konvergente Folge in $K$ hätte dann keine in $K$ konvergente Teilfolge (jede Teilfolge konvergiert ebenfalls gegen $x \notin K$), Widerspruch.

**"$\Leftarrow$":** Sei $K$ abgeschlossen und beschränkt. Wir zeigen per Induktion über $n$, dass jede Folge in $K$ einen Häufungspunkt in $K$ besitzt (nach Satz 1.26 äquivalent zu Kompaktheit).

*Induktionsanfang $n=1$:* Klassischer Satz von Bolzano-Weierstraß aus Analysis 1 (jede beschränkte Folge in $\mathbb{R}$ hat eine konvergente Teilfolge; deren Grenzwert liegt in $K$, da $K$ abgeschlossen).

*Induktionsschritt $n-1 \to n$:* Sei $a$ Folge in $K \subseteq \mathbb{R}^n$, schreibe $a_i = (b_i, c_i)$ mit $b_i \in \mathbb{R}^{n-1}$, $c_i \in \mathbb{R}$. Da $a$ beschränkt ist, sind auch $b$ und $c$ beschränkt. Nach Induktionsvoraussetzung besitzt $b$ eine konvergente Teilfolge $b_{k_i} \to \tilde b$; auf den entsprechenden Indizes besitzt die (beschränkte, reelle) Folge $c_{k_i}$ wiederum eine konvergente Teilfolge $c_{k_{j_i}} \to \tilde c$ (Induktionsanfang). Dann konvergiert $a_{k_{j_i}} = (b_{k_{j_i}}, c_{k_{j_i}}) \to (\tilde b,\tilde c)$ (komponentenweise Konvergenz $\Rightarrow$ Konvergenz im $\mathbb{R}^n$). Da $K$ abgeschlossen ist, liegt der Grenzwert in $K$. $\blacksquare$

<a id="vergleichstabelle-konvergenz-vs-cauchy-eigenschaft-vs-vollständigkeit"></a>
## Vergleichstabelle: Konvergenz vs. Cauchy-Eigenschaft vs. Vollständigkeit

| Begriff | Definition | Braucht Grenzwert *im Raum*? | Gilt in $\mathbb{Q}$? |
|---|---|---|---|
| **Konvergente Folge** | $\exists x \in M: \lim d(a_n,x)=0$ | Ja (explizit gefordert) | Nur für rationale Grenzwerte |
| **Cauchy-Folge** | $d(a_n,a_m)\to 0$ für $n,m\to\infty$ | Nein | Ja, auch mit irrationalem "Ziel" |
| **Vollständigkeit** | Jede Cauchy-Folge konvergiert | Eigenschaft des *Raumes* | **Nein** ($\mathbb{Q}$ ist nicht vollständig) |

<a id="typische-klausuraufgaben-10"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Erkennungsmerkmal | Strategie |
|---|---|---|
| "Zeigen Sie, dass $d(\cdot,\cdot)$ eine Metrik ist" | Konkrete Formel für $d$ gegeben | Alle 4 Axiome einzeln; Dreiecksungleichung ist meist der schwierigste Teil (oft via Cauchy-Schwarz oder Minkowski-Ungleichung) |
| "Ist $(M,d)$ vollständig?" | Konkreter Raum, oft Funktionenraum | Cauchy-Folge nehmen, Kandidat für Grenzwert konstruieren, Konvergenz *im Raum* nachweisen (nicht nur punktweise!) |
| "Zeigen Sie Nicht-Vollständigkeit" | Raum mit "fehlenden Grenzwerten" | Explizite Cauchy-Folge angeben, die gegen ein Element *außerhalb* des Raumes konvergiert |
| "Ist $K$ kompakt?" (im $\mathbb{R}^n$) | Konkrete Teilmenge des $\mathbb{R}^n$ | Heine-Borel: abgeschlossen + beschränkt prüfen |
| "Ist $K$ kompakt?" (allgemeiner metrischer Raum) | Funktionenraum, Folgenraum | Heine-Borel gilt NICHT automatisch — Folgenkompaktheit (Satz 1.26) direkt prüfen |

<a id="typische-fehler-10"></a>
## Typische Fehler

1. **Heine-Borel unreflektiert auf unendlichdimensionale Räume anwenden.** Die abgeschlossene Einheitskugel in einem unendlichdimensionalen Banachraum (z.B. $C^0([0,1])$) ist abgeschlossen und beschränkt, aber **nicht** kompakt! (Standard-Gegenbeispiel für spätere Vertiefung.)
2. **Cauchy-Folge mit konvergenter Folge verwechseln**, insbesondere in nicht-vollständigen Räumen.
3. **Bei Vervollständigung vergessen, dass Äquivalenzklassen gebildet werden müssen** — die "rohe" Grenzfunktion $d_c$ ist nur eine Pseudometrik.
4. **Dreiecksungleichung falsch anwenden** (z.B. $d(x,z) \geq d(x,y) - d(y,z)$ statt der korrekten Richtung).

<a id="verbindungen-10"></a>
## Verbindungen

- Die metrische Topologie (Def. 1.16) ist die Brücke zwischen Kapitel 1 und den nachfolgenden Kapiteln: **Jeder** normierte Raum (Kapitel 3) ist automatisch ein metrischer Raum via $d(x,y):=\|x-y\|$ (Lemma 1.29) — Vollständigkeit und Kompaktheit aus diesem Kapitel werden dort direkt weiterverwendet.
- Satz 1.26 (Folgenkompaktheit) wird beim Beweis des Extremwertsatzes (Kap. 5) und implizit beim Beweis der Riemann-Integrierbarkeit stetiger Funktionen (Kap. 6) benötigt.
- Der Vervollständigungssatz 1.23 ist die abstrakte Version der Konstruktion von $\mathbb{R}$ aus $\mathbb{Q}$ und motiviert später die Konstruktion von $L^p$-Räumen (außerhalb dieser Vorlesung, aber begrifflich verwandt).
- Heine-Borel (Satz 1.55) wird in Kapitel 6 (Riemann-Integral) für die gleichmäßige Stetigkeit stetiger Funktionen auf kompakten Quadern verwendet.

<a id="zusammenfassung-kapitel-1-2"></a>
## Zusammenfassung Kapitel 1 & 2

- **Topologie** liefert den minimalen Rahmen für Konvergenz und Stetigkeit über Umgebungssysteme $N(x)$ mit vier Axiomen.
- **Offene Mengen** sind stabil unter beliebigen Vereinigungen und *endlichen* Schnitten — nicht unter unendlichen Schnitten.
- **Hausdorff-Eigenschaft** garantiert Eindeutigkeit von Grenzwerten; **erste Abzählbarkeit** garantiert die Äquivalenz von Stetigkeit und Folgenstetigkeit.
- **Stetigkeit** lässt sich äquivalent über Urbilder offener Mengen charakterisieren (Lemma 1.9) — die technisch wichtigste Definition für Beweise.
- **Zusammenhang** und **Kompaktheit** sind rein topologische Eigenschaften, die unter stetigen Abbildungen erhalten bleiben (Satz 1.12, Lemma 1.14) und den Extremwertsatz vorbereiten.
- **Metrische Räume** verfeinern Topologie durch eine quantitative Abstandsfunktion; sie sind automatisch Hausdorff'sch und erst-abzählbar.
- **Cauchy-Folgen** sind eine intrinsische (grenzwertfreie) Konvergenzbedingung; **Vollständigkeit** fordert, dass jede solche Folge tatsächlich konvergiert.
- Jeder metrische Raum lässt sich **vervollständigen** (Satz 1.23) — Konstruktion über Äquivalenzklassen von Cauchy-Folgen.
- Im $\mathbb{R}^n$ (und nur dort!) ist Kompaktheit äquivalent zu "abgeschlossen und beschränkt" (Heine-Borel, Satz 1.55) — in allgemeinen metrischen/normierten Räumen gilt dies **nicht**.

---

*Ende Teil 1. Fortsetzung folgt mit Kapitel 3 (Banachräume, Fréchet-Ableitung), Kapitel 4 (Umkehrsatz, implizite Funktionen) auf Anfrage.*



---

<a id="analysis-auf-allgemeinen-linearen-räumen-teil-2"></a>
# Analysis auf allgemeinen linearen Räumen — Teil 2

*Fortsetzung von Teil 1 (Topologische und metrische Räume). Dieses Dokument setzt Kapitel 1 und 2 als bekannt voraus.*

---

<a id="kapitel-3-banachräume-und-die-fréchet-ableitung"></a>
# Kapitel 3: Banachräume und die Fréchet-Ableitung

<a id="motivation-11"></a>
## Motivation

**Welches Problem lösen wir?**

Ein metrischer Raum liefert uns einen Abstandsbegriff — aber keine algebraische Struktur. Wir können nicht "addieren" oder "skalieren", nicht von Geraden, Ebenen oder linearen Approximationen sprechen. Für die Differentialrechnung brauchen wir aber genau das: Die Ableitung einer Funktion $f$ bei $x$ soll die *beste lineare Approximation* von $f$ in der Nähe von $x$ sein. Dafür braucht man einen **Vektorraum mit einer verträglichen Metrik** — das ist ein **normierter Raum**. Damit Grenzwertprozesse (wie sie z.B. bei der Definition der Ableitung als Limes eines Differenzenquotienten auftreten) nicht "ins Leere laufen", fordert man zusätzlich **Vollständigkeit**: einen **Banachraum**.

**Warum reicht der $\mathbb{R}^n$ nicht als alleiniges Fundament?** Weil viele der interessantesten Anwendungen (Differentialgleichungen, Funktionalanalysis, Variationsrechnung) in **unendlichdimensionalen** Räumen stattfinden — Räumen von Funktionen, nicht von Zahlentupeln. Baut man den Kalkül von vornherein in Banachräumen auf, bekommt man den $\mathbb{R}^n$-Kalkül automatisch als Spezialfall (da $\mathbb{R}^n$ mit jeder Norm ein Banachraum ist), gewinnt aber zusätzlich alle unendlichdimensionalen Anwendungen.

**Historischer Kontext.** Der Begriff des normierten Vektorraums und seine Vervollständigung geht auf Stefan Banach (1920er Jahre, Polen) zurück, der damit die Funktionalanalysis begründete. Die hier entwickelte "Fréchet-Ableitung" (nach Maurice Fréchet) verallgemeinert die aus der Schule bekannte Ableitung so, dass sie in *jedem* Banachraum funktioniert.

<a id="intuition-11"></a>
## Intuition

Eine **Norm** $\|\cdot\|$ ist eine "Längenmessung" für Vektoren, aus der sich über $d(x,y):=\|x-y\|$ automatisch ein Abstand ergibt. Man kann sich das wie ein Lineal vorstellen, das man an *jeden* Vektor anlegen kann — unabhängig davon, ob der Vektor ein Punkt im $\mathbb{R}^3$, eine Matrix oder eine ganze Funktion ist.

Ein **Banachraum** ist dann ein normierter Raum, in dem es "keine Löcher gibt" — jede Folge, die sich (im Sinne der Cauchy-Bedingung) einem Grenzwert annähert, findet diesen Grenzwert auch tatsächlich im Raum vor. Das ist analog zur Vollständigkeit von $\mathbb{R}$ gegenüber $\mathbb{Q}$: In $\mathbb{Q}$ "fehlen" Grenzwerte wie $\sqrt 2$; in unvollständigen normierten Räumen fehlen analog Grenzwerte von Cauchy-Folgen von Vektoren.

Die **Fréchet-Ableitung** verallgemeinert die bekannte Ableitung $f'(x)$ so: Statt einer *Zahl* $f'(x)$, mit der man multipliziert ($f(x+h)\approx f(x)+f'(x)\cdot h$), suchen wir eine **lineare Abbildung** $Df(x)$, die den Zuwachs $h$ auf den (approximativen) Funktionszuwachs abbildet:
$$
f(x+h) \approx f(x) + Df(x)[h].
$$
Der Trick, der diese Approximation präzisiert, ist derselbe wie in der Schule: Der Fehler dieser Approximation soll *schneller* gegen null gehen als $h$ selbst — nur dass "schneller als $h$" jetzt über die Norm gemessen wird: $\|h(g)\|/\|g\| \to 0$.

<a id="formale-definitionen-11"></a>
## Formale Definitionen

<a id="definition-128-norm-normierter-raum"></a>
### Definition 1.28 (Norm, normierter Raum)

Sei $E$ ein Vektorraum über $\mathbb{R}$ (oder $\mathbb{C}$). Eine Abbildung $\|\cdot\|: E \to \mathbb{R}_{\geq 0}$ heißt **Norm**, falls für alle $\alpha \in \mathbb{R}$, $x,y \in E$:

$$
\begin{aligned}
\text{(i)}\quad & \|\alpha x\| = |\alpha| \, \|x\| \quad \text{(absolute Homogenität)}\\
\text{(ii)}\quad & \|x+y\| \leq \|x\| + \|y\| \quad \text{(Dreiecksungleichung / Subadditivität)}\\
\text{(iii)}\quad & \|x\| = 0 \iff x = 0 \quad \text{(Definitheit)}
\end{aligned}
$$

<a id="standardbeispiele-die-p-normen-auf-mathbbrn"></a>
### Standardbeispiele: Die $p$-Normen auf $\mathbb{R}^n$

$$
\|x\|_2 = \sqrt{x_1^2+\dots+x_n^2} \quad (\text{euklidische Norm}), \qquad \|x\|_p = \left(\sum_{i=1}^n |x_i|^p\right)^{1/p}, \quad p \geq 1
$$

Auf dem Folgenraum $\ell^2(\mathbb{R}) := \{x: \mathbb{N}\to\mathbb{R} : \sum_i x_i^2 < \infty\}$ ist analog $\|x\|_2 := \sqrt{\sum_i x_i^2}$ eine Norm — hier zeigt sich zum ersten Mal ein **unendlichdimensionaler** Banachraum.

<a id="lemma-129-norm-induziert-metrik"></a>
### Lemma 1.29 (Norm induziert Metrik)

**Aussage:** Ist $(E,\|\cdot\|)$ normierter Raum, so ist $d(x,y):=\|x-y\|$ eine Metrik auf $E$.

**Beweisidee** *(direktes Nachrechnen)*: Die Metrikaxiome übertragen sich direkt aus den Normaxiomen — z.B. folgt die Dreiecksungleichung für $d$ aus der für die Norm: $d(x,y)=\|x-y\|=\|(x-z)+(z-y)\|\le \|x-z\|+\|z-y\|=d(x,z)+d(z,y)$. $\blacksquare$

**Konsequenz:** Jeder normierte Raum ist automatisch ein metrischer Raum — alle Begriffe aus Kapitel 2 (Konvergenz, Cauchy-Folgen, Vollständigkeit, Kompaktheit) stehen sofort zur Verfügung.

<a id="definition-130-banachraum"></a>
### Definition 1.30 (Banachraum)

Ein normierter Raum $(B,\|\cdot\|)$ heißt **Banachraum**, wenn er (bezüglich der induzierten Metrik $d(x,y)=\|x-y\|$) **vollständig** ist.

<a id="definition-131132-lineare-beschränkte-abbildungen-und-operatornorm"></a>
### Definition 1.31/1.32 (Lineare, beschränkte Abbildungen und Operatornorm)

Seien $A,B$ Banachräume. $f: A\to B$ heißt **linear**, falls $f(cx+dy)=cf(x)+df(y)$ für alle $x,y\in A$, $c,d\in\mathbb{R}$.

Für lineares $a: A \to B$ definiert man die **Operatornorm**
$$
\|a\| := \sup_{0\neq x \in A} \frac{\|a(x)\|}{\|x\|} = \sup_{\|x\|=1} \|a(x)\|.
$$
Ist $\|a\|<\infty$, heißt $a$ **beschränkt**. Man setzt
$$
L(A,B) := \{a: A \to B \text{ linear} : \|a\| < \infty\} \qquad \text{(Menge aller beschränkten linearen Abbildungen)}.
$$

> **Wichtige Notationskonvention:** $L(A,B)$ ist selbst wieder ein Vektorraum (sogar Banachraum, siehe Lemma 1.35), und $\|a\|$ ist eine Norm darauf.

<a id="lemma-174-beschränkt-iff-stetig-für-lineare-abbildungen"></a>
### Lemma 1.74 (Beschränkt $\iff$ Stetig, für lineare Abbildungen)

**Aussage:** Für lineares $a: A \to B$ zwischen normierten Räumen gilt:
$$
a \text{ beschränkt} \quad \iff \quad a \text{ stetig (auf ganz } A\text{)}.
$$

**Bedeutung:** Bei linearen Abbildungen fallen "Stetigkeit" und "Beschränktheit" zusammen — ein entscheidender Unterschied zu allgemeinen (nichtlinearen) Funktionen, wo Beschränktheit und Stetigkeit völlig unabhängige Eigenschaften sind! Dies rechtfertigt, warum $L(A,B)$ *nur* die beschränkten linearen Abbildungen enthält: Es sind genau die *stetigen*.

**Beweis:**

**"$\Rightarrow$" (beschränkt $\Rightarrow$ stetig):** Sei $\|a\|=c<\infty$. Für beliebige $x,y \in A$ gilt wegen Linearität und Definition der Operatornorm:
$$
\|a(x)-a(y)\| = \|a(x-y)\| \leq \|a\| \cdot \|x-y\| = c\|x-y\|.
$$
Diese sogenannte **Lipschitz-Stetigkeit** impliziert direkt Stetigkeit (zu $\varepsilon>0$ wähle $\delta:=\varepsilon/c$).

**"$\Leftarrow$" (stetig $\Rightarrow$ beschränkt):** Sei $a$ stetig, insbesondere stetig bei $0$ (mit $a(0)=0$ wegen Linearität). Zu $\varepsilon=1$ existiert $\delta>0$, sodass $\|x-0\|<\delta \Rightarrow \|a(x)-a(0)\|<1$, also $\|a(x)\|<1$ für $\|x\|\le \delta$ (durch Stetigkeit bei 0, mit geeigneter Wahl). Für beliebiges $x\neq 0$ betrachte $\hat x := \delta \cdot x/\|x\|$ (mit $\|\hat x\|=\delta$). Dann:
$$
\|a(\hat x)\| \leq 1 \quad \Rightarrow \quad \left\|a\left(\frac{\delta x}{\|x\|}\right)\right\| \leq 1 \quad \Rightarrow \quad \frac{\delta}{\|x\|}\|a(x)\| \leq 1 \quad \Rightarrow \quad \|a(x)\| \leq \frac{\|x\|}{\delta}.
$$
Also $\|a\| \leq 1/\delta < \infty$. $\blacksquare$

<a id="lemma-135-lab-ist-banachraum"></a>
### Lemma 1.35 (L(A,B) ist Banachraum)

**Aussage:** Sind $A,B$ Banachräume, so ist $(L(A,B),\|\cdot\|)$ (mit der Operatornorm) selbst ein Banachraum.

**Bedeutung:** Dies ist essentiell, um später von "Ableitungen der Ableitung" (höhere Ableitungen, Kapitel weiter unten) sprechen zu können — die zweite Ableitung ist eine Abbildung mit Werten in $L(A,L(A,B))$, und damit dies wieder ein wohlverhaltener Raum ist, muss $L(A,B)$ selbst Banachraum sein.

**Beweisidee** *(Beweisstil: Normaxiome direkt, Vollständigkeit über punktweise Konstruktion des Grenzoperators)*

*Normeigenschaften:* Direktes Nachrechnen über die Supremum-Definition (Dreiecksungleichung folgt aus $\sup(f+g)\le \sup f + \sup g$).

*Vollständigkeit (Kernstück):* Sei $(a_n)_n$ Cauchy-Folge in $L(A,B)$ (bzgl. Operatornorm). Für jedes feste $x\in A$ gilt
$$
\|a_n(x) - a_m(x)\| \leq \|a_n-a_m\|\cdot\|x\| \xrightarrow{n,m\to\infty} 0,
$$
also ist $(a_n(x))_n$ Cauchy-Folge in $B$; da $B$ vollständig ist, konvergiert sie gegen ein Element, das wir $a(x):=\lim_n a_n(x)$ nennen. Man verifiziert, dass $x \mapsto a(x)$ linear ist (Grenzwertbildung vertauscht mit Linearkombinationen) und dass $a$ beschränkt ist:
$$
\|a(x)\| = \lim_{n\to\infty}\|a_n(x)\| \leq \|x\| \cdot \limsup_n \|a_n\| < \infty
$$
(da Cauchy-Folgen beschränkt sind). Schließlich zeigt man $\|a_n - a\| \to 0$ (Konvergenz in der Operatornorm, nicht nur punktweise!) mittels eines $\varepsilon/2$-Arguments über die Cauchy-Eigenschaft von $(a_n)$. $\blacksquare$

<a id="definition-137-fréchet-differenzierbarkeit"></a>
### Definition 1.37 (Fréchet-Differenzierbarkeit)

Seien $A,B$ Banachräume, $U \subseteq A$ offen, $x \in U$. $f: U \to B$ heißt **differenzierbar bei $x$**, falls ein $a \in L(A,B)$ existiert, sodass mit
$$
h(g) := f(x+g) - f(x) - a(g)
$$
gilt:
$$
\lim_{g \to 0} \frac{\|h(g)\|}{\|g\|} = 0, \qquad \text{äquivalent:} \qquad \|h(g)\| = o(\|g\|) \text{ für } g \to 0.
$$
Man schreibt $Df(x) := a$ und nennt $Df(x) \in L(A,B)$ die **Ableitung** von $f$ bei $x$.

> **Kernidee dieser Definition, ausformuliert:** $Df(x)$ ist die (eindeutig bestimmte — Übung, folgt aus der Eindeutigkeit von Grenzwerten in Hausdorff-Räumen) lineare Abbildung, die $f$ in einer Umgebung von $x$ **bis auf einen Fehler höherer Ordnung** approximiert:
> $$
> f(x+g) = f(x) + Df(x)[g] + o(\|g\|).
> $$
> Die eckige Klammer $Df(x)[g]$ betont, dass $Df(x)$ selbst eine *Abbildung* ist, die auf den Vektor $g$ angewendet wird — nicht mit ihm multipliziert wird (wie im 1-dimensionalen Fall $f'(x)\cdot h$, was formal auch nur die Anwendung der linearen Abbildung "Multiplikation mit $f'(x)$" ist).

<a id="definition-138-stetige-differenzierbarkeit"></a>
### Definition 1.38 (Stetige Differenzierbarkeit)

$f: U \to B$ heißt **stetig differenzierbar** in $U \subseteq A$ (offen), falls $f$ für alle $x \in U$ differenzierbar ist **und** die Abbildung
$$
Df: U \to L(A,B), \qquad x \mapsto Df(x)
$$
stetig ist. Notation: $f \in C^1(U,B)$.

<a id="eigenschaften-11"></a>
## Eigenschaften

<a id="ableitungsregeln-satz-ohne-separate-nummer-in-der-mitschrift"></a>
### Ableitungsregeln (Satz, ohne separate Nummer in der Mitschrift)

Seien $f,g: U\to B$ differenzierbar bei $x$, $\alpha \in \mathbb{R}$. Dann:

| Regel | Formel | Bemerkung |
|---|---|---|
| **Summenregel** | $D(f+g)(x) = Df(x)+Dg(x)$ | Direkt aus Linearität des Grenzwerts |
| **Skalarregel** | $D(\alpha f)(x) = \alpha \, Df(x)$ | ebenso |
| **Produktregel** | **existiert nicht allgemein** | Siehe Bemerkung unten |

> **Präzisierung (behebt eine Lücke der ursprünglichen Mitschrift):** Es stimmt, dass es *keine* allgemeine Produktregel für zwei $B$-wertige Funktionen gibt — schlicht, weil in einem allgemeinen Banachraum $B$ **kein Produkt zweier Vektoren** definiert ist! Es gibt aber sehr wohl eine Verallgemeinerung: Ist $\beta: X \times Y \to Z$ eine **stetige bilineare Abbildung** zwischen Banachräumen und sind $f: U \to X$, $g: U \to Y$ differenzierbar, so ist $x \mapsto \beta(f(x),g(x))$ differenzierbar mit
> $$
> D[\beta(f,g)](x)[h] = \beta(Df(x)[h], g(x)) + \beta(f(x), Dg(x)[h]).
> $$
> Für $X=Y=Z=\mathbb{R}$, $\beta(a,b)=ab$ erhält man die klassische Produktregel zurück.

<a id="satz-129-kettenregel"></a>
### Satz 1.29 (Kettenregel)

**Aussage:** Seien $X,Y,Z$ Banachräume, $f: X \to Y$ differenzierbar bei $x$, $g: Y \to Z$ differenzierbar bei $f(x)$. Dann ist $g\circ f: X \to Z$ differenzierbar bei $x$, und
$$
D(g\circ f)(x) = Dg(f(x)) \circ Df(x).
$$

**Bedeutung:** Die vielleicht wichtigste Ableitungsregel überhaupt — sie erlaubt, komplizierte zusammengesetzte Funktionen Schritt für Schritt abzuleiten. Beachten Sie, dass rechts eine **Verkettung linearer Abbildungen** steht (kein Produkt!) — das entspricht im Eindimensionalen der Matrixmultiplikation der Jacobi-Matrizen.

**Beweis** *(Beweisstil: direkte $\varepsilon$-Abschätzung über die Definition der Ableitung, mit sorgfältiger Kontrolle der Fehlerterme)*

Setze $D_g := Dg(f(x))$, $D_f := Df(x)$. Wir zeigen, dass
$$
R(g) := g(f(x+g)) - g(f(x)) - D_g \circ D_f [g]
$$
die Bedingung $\|R(g)\| = o(\|g\|)$ erfüllt. Schreibe
$$
R(g) = \underbrace{g(f(x+g)) - g(f(x)) - D_g[f(x+g)-f(x)]}_{=:\Theta_1} + \underbrace{D_g\big[f(x+g)-f(x) - D_f[g]\big]}_{=:\Theta_2}.
$$
(Nachrechnen: Addition und Subtraktion von $D_g[f(x+g)-f(x)]$ liefert genau diese Zerlegung.)

**Abschätzung von $\Theta_2$:** Da $f$ differenzierbar bei $x$ ist, gilt $f(x+g)-f(x)-D_f[g] = o(\|g\|)$; da $D_g \in L(Y,Z)$ beschränkt ist,
$$
\|\Theta_2\| \leq \|D_g\| \cdot \|f(x+g)-f(x)-D_f[g]\| = \|D_g\| \cdot o(\|g\|) = o(\|g\|).
$$

**Abschätzung von $\Theta_1$:** Da $g$ differenzierbar bei $f(x)$ ist, gilt für $k:=f(x+g)-f(x)$:
$$
\Theta_1 = g(f(x)+k) - g(f(x)) - D_g[k] = o(\|k\|).
$$
Es bleibt zu zeigen, dass $o(\|k\|) = o(\|g\|)$, wofür man $\|k\| = \|f(x+g)-f(x)\| \leq C\|g\|$ für $\|g\|$ klein genug benötigt (Lipschitz-artige Kontrolle, die aus der Differenzierbarkeit von $f$ folgt, da $\|f(x+g)-f(x)\| \le \|D_f\|\|g\| + o(\|g\|) \le C\|g\|$). Damit ist $\|\Theta_1\| = o(\|k\|) = o(\|g\|)$.

Zusammen: $\|R(g)\| \leq \|\Theta_1\|+\|\Theta_2\| = o(\|g\|)$. $\blacksquare$

<a id="lemma-190-mittelwertungleichung"></a>
### Lemma 1.90 (Mittelwertungleichung)

**Aussage:** Seien $X,Y$ Banachräume, $U \subseteq X$, $f: U \to Y$ stetig differenzierbar mit $\|Df(x)\| \leq M$ für alle $x \in U$. Dann gilt für alle $x,y \in U$ (mit der Verbindungsstrecke $[x,y]\subseteq U$):
$$
\|f(x) - f(y)\| \leq M \|x-y\|.
$$

**Bedeutung:** Dies ersetzt den klassischen (eindimensionalen) **Mittelwertsatz** $f(x)-f(y)=f'(\xi)(x-y)$, der in Banachräumen **nicht** wörtlich gilt (es gibt i.A. kein "$\xi$" für vektorwertige Funktionen — Standard-Gegenbeispiel weiter unten). Die Mittelwertungleichung ist der korrekte, allgemeingültige Ersatz und in der Praxis meist ausreichend.

**Beweis** *(Beweisstil: Reduktion auf den Fall $B=\mathbb{R}$ mittels Hilfsfunktion, dann Integration der Ableitung)*

Definiere $F: [0,1] \to Y$ durch $F(t) := f((1-t)y+tx)$. Nach Kettenregel gilt
$$
F'(t) = Df((1-t)y+tx)[x-y].
$$
Aus der (hier vorausgesetzten, siehe Wegintegrale Kap. 3.3 später) Beziehung $F(1)-F(0)=\int_0^1 F'(s)\,ds$ (Hauptsatz für Banachraum-wertige Funktionen einer reellen Variablen) folgt
$$
\|f(x)-f(y)\| = \|F(1)-F(0)\| = \left\|\int_0^1 F'(s)\,ds\right\| \leq \int_0^1 \|F'(s)\|\,ds \leq \int_0^1 \|Df(\cdot)\| \cdot \|x-y\|\,ds \leq M\|x-y\|. \quad \blacksquare
$$

<a id="gegenbeispiel-klassischer-mittelwertsatz-gilt-nicht-in-banachräumen"></a>
### Gegenbeispiel: Klassischer Mittelwertsatz gilt nicht in Banachräumen

Betrachte $f: \mathbb{R} \to \mathbb{R}^2$, $f(t) = (\cos t, \sin t)$. Dann $f(2\pi)-f(0) = (0,0)$, aber $Df(t)[1] = (-\sin t,\cos t) \neq (0,0)$ für **jedes** $t$ — es gibt also kein $\xi \in (0,2\pi)$ mit $f(2\pi)-f(0)=Df(\xi)[2\pi]$. Der klassische Mittelwertsatz (mit **Gleichheit**) gilt somit für vektorwertige Funktionen nicht — nur die **Ungleichung** (Lemma 1.90) bleibt richtig.

<a id="verbindungen-11"></a>
## Verbindungen

- Die Fréchet-Ableitung und die Kettenregel sind das Fundament für **alles** Weitere in diesem Skript: Umkehrsatz, implizite Funktionen, Taylorformel, Extrema, Lagrange-Multiplikatoren.
- Lemma 1.35 ($L(A,B)$ Banachraum) wird für höhere Ableitungen $D^kf(x) \in L^k(X,Y)$ (Kapitel weiter unten) unverzichtbar.
- Die Mittelwertungleichung wird im Beweis des Umkehrsatzes (Kap. 4) verwendet, um die Kontraktionseigenschaft der Hilfsabbildung nachzuweisen.

---

<a id="kapitel-4-umkehrsatz-banach-fixpunktsatz-und-implizite-funktionen"></a>
# Kapitel 4: Umkehrsatz, Banach-Fixpunktsatz und implizite Funktionen

<a id="motivation-12"></a>
## Motivation

**Welches Problem lösen wir?**

Gegeben eine differenzierbare Funktion $f$, wann besitzt sie lokal eine Umkehrfunktion? Aus der Schule kennen Sie die Faustregel: Ist $f'(x_0)\neq 0$, so ist $f$ lokal umkehrbar. Der **Umkehrsatz** verallgemeinert dies auf Banachräume: Ist die *lineare* Approximation $Df(x_0)$ ein Isomorphismus (invertierbar mit stetiger Inverser), so ist $f$ selbst lokal umkehrbar — eine der stärksten und am häufigsten verwendeten Aussagen der gesamten Analysis.

Eng verwandt ist die Frage: Gegeben eine implizite Gleichung $\phi(x,y)=0$, wann lässt sich diese lokal nach $y$ auflösen, d.h. wann existiert eine Funktion $y=g(x)$ mit $\phi(x,g(x))=0$? Der **Satz über implizite Funktionen** beantwortet dies — und ist tatsächlich **äquivalent** zum Umkehrsatz (jeder lässt sich aus dem anderen herleiten).

**Warum ist das so fundamental?** Praktisch jede Anwendung, bei der man ein Gleichungssystem "nach einer Variablen auflösen" möchte (Kurven/Flächen als Graphen darstellen, Nebenbedingungen parametrisieren, Differentialgleichungen lösen), beruht letztlich auf diesen beiden Sätzen.

<a id="intuition-12"></a>
## Intuition

Stellen Sie sich $f$ als eine "Verzerrung" des Raumes vor. Ist die Ableitung $Df(x_0)$ bei $x_0$ invertierbar, bedeutet das: In erster Näherung (linear) ist die Verzerrung *nicht entartet* — sie "faltet" den Raum lokal nicht zusammen, sondern streckt/dreht ihn nur um einen bestimmten Faktor. Die Kernaussage des Umkehrsatzes ist: **Diese lokale Nicht-Entartung der linearen Näherung reicht aus**, um zu garantieren, dass auch $f$ selbst (nicht nur seine lineare Näherung!) lokal umkehrbar ist — vorausgesetzt, $f$ ist stetig differenzierbar (die Ableitung "springt nicht").

Der Beweis nutzt einen wunderschönen Trick: Man reduziert das Problem "Finde $x$ mit $f(x)=y$" auf ein **Fixpunktproblem** "Finde $x$ mit $g(x)=x$" für eine geeignet konstruierte Abbildung $g$, und wendet dann den **Banach-Fixpunktsatz** an — ein Resultat, das auf den ersten Blick nichts mit Differenzierbarkeit zu tun hat, aber sich als das eigentliche Herzstück des Beweises entpuppt.

**Physikalische Analogie zum Fixpunktsatz:** Stellen Sie sich eine Landkarte vor, die auf den Tisch gelegt wird, auf dem sie das darauf abgebildete Gebiet zeigt. Es gibt garantiert genau einen Punkt auf der Karte, der exakt über dem entsprechenden Punkt in der Realität liegt — das ist die Kernaussage des Fixpunktsatzes, angewendet auf eine kontrahierende Verkleinerungsabbildung.

<a id="formale-definitionen-12"></a>
## Formale Definitionen

<a id="definition-kontraktion"></a>
### Definition (Kontraktion)

Sei $(M,d)$ metrischer Raum. $F: M \to M$ heißt **Kontraktion**, falls ein $0 \leq \lambda < 1$ existiert mit
$$
d(F(x),F(y)) \leq \lambda \, d(x,y) \qquad \forall x,y \in M.
$$

<a id="sätze-10"></a>
## Sätze

<a id="satz-143-banach-fixpunktsatz"></a>
### Satz 1.43 (Banach-Fixpunktsatz)

**Aussage:** Sei $(M,d)$ ein **vollständiger** metrischer Raum, $F: M \to M$ eine Kontraktion mit Kontraktionskonstante $\lambda \in [0,1)$. Dann besitzt $F$ **genau einen** Fixpunkt $x_0 \in M$, d.h. $F(x_0)=x_0$.

**Bedeutung:** Einer der wichtigsten Sätze der gesamten Analysis — er garantiert nicht nur *Existenz*, sondern auch *Eindeutigkeit* einer Lösung, und liefert zusätzlich ein **konstruktives Näherungsverfahren** (die Fixpunktiteration), das in der Numerik ständig verwendet wird.

**Voraussetzungen — worauf Sie achten müssen:**
- **Vollständigkeit** von $M$ ist essentiell (sonst könnte die approximierende Folge "aus dem Raum herauslaufen").
- $\lambda < 1$ **strikt** — für $\lambda=1$ (nicht-strikte Kontraktion) kann die Aussage scheitern.

**Beweis** *(Beweisstil: konstruktiver Beweis via Iterationsfolge, Cauchy-Nachweis über geometrische Reihe)*

Wähle $x_1 \in M$ beliebig, definiere rekursiv $x_{n+1} := F(x_n)$. Dann gilt per Induktion:
$$
d(x_{n+1},x_n) = d(F(x_n),F(x_{n-1})) \leq \lambda\, d(x_n,x_{n-1}) \leq \dots \leq \lambda^{n-1} d(x_2,x_1).
$$
Für $m > n$ liefert die Dreiecksungleichung, kombiniert mit der geometrischen Reihe:
$$
d(x_m,x_n) \leq \sum_{k=n}^{m-1} d(x_{k+1},x_k) \leq \sum_{k=n}^{m-1} \lambda^{k-1} d(x_2,x_1) \leq \frac{\lambda^{n-1}}{1-\lambda} d(x_2,x_1) \xrightarrow{n\to\infty} 0.
$$
Also ist $(x_n)$ eine Cauchy-Folge; da $M$ vollständig ist, konvergiert sie gegen ein $x_0 \in M$.

**Fixpunkteigenschaft:** $F$ ist Lipschitz-stetig (mit Konstante $\lambda$), also insbesondere stetig; somit
$$
F(x_0) = F\left(\lim_{n\to\infty} x_n\right) = \lim_{n\to\infty} F(x_n) = \lim_{n\to\infty} x_{n+1} = x_0.
$$

**Eindeutigkeit:** Seien $x_0, y_0$ beide Fixpunkte. Dann
$$
d(x_0,y_0) = d(F(x_0),F(y_0)) \leq \lambda\, d(x_0,y_0) \quad \Rightarrow \quad (1-\lambda)\,d(x_0,y_0) \leq 0 \quad \Rightarrow \quad d(x_0,y_0)=0
$$
(da $1-\lambda>0$), also $x_0=y_0$. $\blacksquare$

**Konvergenzgeschwindigkeit (a-priori-Fehlerabschätzung):** Aus obiger Rechnung mit $m\to\infty$ folgt
$$
d(x_n, x_0) \leq \frac{\lambda^{n-1}}{1-\lambda} d(x_2,x_1) \qquad \text{(geometrische, "lineare" Konvergenz)}.
$$

<a id="satz-142-umkehrsatz"></a>
### Satz 1.42 (Umkehrsatz)

**Aussage:** Seien $X,Y$ Banachräume, $U \subseteq X$ offen, $f: U \to Y$ stetig differenzierbar. Sei $x \in U$, und sei $Df(x): X \to Y$ ein **beschränkter Isomorphismus** (d.h. bijektiv mit $Df(x)^{-1} \in L(Y,X)$, kurz: $Df(x) \in GL(X,Y)$). Dann existiert eine offene Umgebung $V$ von $f(x)$ und eine stetig differenzierbare Abbildung $g: V \to X$, sodass
$$
\forall y \in V:\ f(g(y)) = y \qquad \text{und} \qquad Dg(y) = Df(g(y))^{-1}.
$$

**Voraussetzungen — Zusammenfassung:**

| Voraussetzung | Warum nötig |
|---|---|
| $f \in C^1(U,Y)$ | Damit $Df$ stetig ist — sonst kann die lineare Approximation "instabil" sein |
| $Df(x)$ invertierbar (in $L(X,Y)$) | Kernbedingung: nicht-entartete lineare Näherung |
| $X,Y$ Banachräume | Für den Banach-Fixpunktsatz im Beweis benötigt |

**Bedeutung:** Umkehrbarkeit ist eine **lokale** Aussage — sie garantiert nur, dass in einer (u.U. kleinen) Umgebung eine Umkehrfunktion existiert, nicht global. Die Formel $Dg(y) = Df(g(y))^{-1}$ ist die Verallgemeinerung der Schulformel $(f^{-1})'(y) = 1/f'(f^{-1}(y))$.

**Beweisidee** *(Beweisstil: Reduktion auf Fixpunktproblem via Banach-Fixpunktsatz — mehrstufiger konstruktiver Beweis)*

**Schritt 0 (Normalisierung):** Man reduziert (ohne Beschränkung der Allgemeinheit, durch affine Verschiebung/Verkettung mit $Df(x)^{-1}$) auf den Fall $x=0$, $f(0)=0$, $Df(0)=\mathrm{id}$.

**Schritt 1 (Umformulierung als Fixpunktproblem):** Gesucht ist zu gegebenem $y$ (nahe $0$) ein $z$ mit $f(z)=y$. Schreibe $f(z) = z + h(z)$ mit $h(z) := f(z)-z$ (klein, da $Df(0)=\mathrm{id}$, also $Dh(0)=0$). Die Gleichung $f(z)=y$ wird zu
$$
z = y - h(z) =: g_y(z) \qquad \text{(Fixpunktgleichung!)}.
$$

**Schritt 2 (Kontraktionseigenschaft von $g_y$):** Da $Dh$ stetig ist und $Dh(0)=0$, existiert $r>0$ mit $\|Dh(z)\| < 1/2$ für $\|z\| < r$. Nach der Mittelwertungleichung (Lemma 1.90) gilt dann
$$
\|h(z_1)-h(z_2)\| \leq \tfrac12 \|z_1-z_2\| \qquad \text{für } z_1,z_2 \in \overline{B_r}.
$$
Für $y \in \overline{B_{r/2}}$ und $z \in \overline{B_r}$ gilt: $\|g_y(z)\| \leq \|y\| + \|h(z)\| \leq \tfrac{r}{2}+\tfrac{r}{2}=r$, d.h. $g_y$ bildet $\overline{B_r}$ in sich ab. Zudem ist $g_y$ eine Kontraktion mit Konstante $\lambda=1/2$:
$$
\|g_y(z_1)-g_y(z_2)\| = \|h(z_1)-h(z_2)\| \leq \tfrac12\|z_1-z_2\|.
$$

**Schritt 3 (Anwendung des Banach-Fixpunktsatzes):** $\overline{B_r}$ ist ein vollständiger metrischer Raum (abgeschlossene Teilmenge des Banachraums $X$). Nach Satz 1.43 existiert genau ein Fixpunkt $z=g_y(z) \in \overline{B_r}$, den wir $z=f^{-1}(y)=:g(y)$ nennen.

**Schritt 4 (Lipschitz-Stetigkeit von $g$, dann Stetigkeit):** Für $y_1,y_2 \in \overline{B_{r/2}}$:
$$
\|g(y_1)-g(y_2)\| = \|g_{y_1}(g(y_1)) - g_{y_2}(g(y_2))\| = \|y_1-h(g(y_1)) - y_2+h(g(y_2))\| \leq \|y_1-y_2\| + \tfrac12\|g(y_1)-g(y_2)\|,
$$
also $\|g(y_1)-g(y_2)\| \leq 2\|y_1-y_2\|$ — $g$ ist Lipschitz-stetig, insbesondere stetig.

**Schritt 5 (Differenzierbarkeit von $g$):** Der technisch aufwendigste Teil: Man zeigt $Df(z)$ ist invertierbar für alle $z$ nahe $0$ (mittels der Neumannschen Reihe, siehe Lemma 1.44 unten), und weist dann direkt über die Definition der Ableitung nach, dass
$$
g^{-1}(y_1)-g^{-1}(y_2) - Df(g(y_2))^{-1}(y_1-y_2) = o(\|y_1-y_2\|),
$$
was $Dg(y) = Df(g(y))^{-1}$ liefert. Die Stetigkeit von $Dg$ folgt aus der Stetigkeit von $Df$ und der Stetigkeit der Inversionsabbildung (Lemma 1.44). $\blacksquare$

<a id="lemma-144-glxy-ist-offen-in-lxy-stetigkeit-der-inversion"></a>
### Lemma 1.44 (GL(X,Y) ist offen in L(X,Y) — Stetigkeit der Inversion)

**Aussage:** Seien $X,Y$ Banachräume. Dann ist $GL(X,Y)$ (die Menge der beschränkten linearen Isomorphismen mit stetiger Inverser) eine **offene** Teilmenge von $L(X,Y)$, und die Abbildung $g \mapsto g^{-1}$ ist stetig auf $GL(X,Y)$.

**Bedeutung:** Dies rechtfertigt Schritt 5 im Beweis des Umkehrsatzes: "Nahe an einem Isomorphismus" ist man wieder bei einem Isomorphismus — Invertierbarkeit ist eine *offene* (stabile) Eigenschaft.

**Beweisidee** *(Beweisstil: Konstruktion der Inversen über die Neumannsche Reihe)*

**Kernlemma (geometrische Reihe von Operatoren):** Ist $\|h\| < 1$ (für $h \in L(X,X)$), so ist $\mathrm{id}-h$ invertierbar, mit
$$
(\mathrm{id}-h)^{-1} = \sum_{k=0}^\infty h^{\circ k} \qquad \text{(Neumannsche Reihe)},
$$
wobei die Reihe wegen $\|h^{\circ k}\| \leq \|h\|^k$ und $\|h\|<1$ absolut konvergiert (Vergleich mit geometrischer Reihe; $L(X,X)$ ist Banachraum nach Lemma 1.35, also konvergiert jede absolut konvergente Reihe).

**Anwendung:** Sei $g \in GL(X,Y)$, $f \in L(X,Y)$ mit $\|f-g\| < \|g^{-1}\|^{-1}$. Dann:
$$
\|g^{-1}\circ(f-g)\| \leq \|g^{-1}\|\cdot\|f-g\| < 1,
$$
also ist $\mathrm{id} - g^{-1}\circ(g-f) = g^{-1}\circ f$ invertierbar (Kernlemma), somit auch $f = g \circ (g^{-1}\circ f)$ invertierbar (Verkettung von Isomorphismen). Damit liegt eine ganze Kugel um $g$ in $GL(X,Y)$ — $GL(X,Y)$ ist offen. Die Stetigkeit der Inversion folgt durch explizite Fehlerabschätzung mittels der Neumannschen Reihe (technisch, hier nicht ausgeführt). $\blacksquare$

<a id="satz-145-satz-über-implizite-funktionen"></a>
### Satz 1.45 (Satz über implizite Funktionen)

**Aussage:** Seien $X,Y,Z$ Banachräume, $U \subseteq X$, $V \subseteq Y$ offen, $f: U\times V \to Z$ stetig differenzierbar. Sei $(x_0,y_0)\in U\times V$ mit $D_yf(x_0,y_0) \in GL(Y,Z)$ (die partielle Ableitung nach $y$ ist ein beschränkter Isomorphismus). Dann existieren Umgebungen $U_0 \subseteq X$ von $x_0$, $U_1 \subseteq Z$ von $f(x_0,y_0)$ und eine **eindeutige** stetig differenzierbare Abbildung
$$
g: U_0 \times U_1 \to V \quad \text{mit} \quad \forall (x,w) \in U_0\times U_1:\ f(x,g(x,w)) = w.
$$

**Spezialfall $Z=\{0\}$-artig (Auflösung von $f(x,y)=0$):** Ist $D_yf(x_0,y_0)$ invertierbar und $f(x_0,y_0)=0$, so existiert lokal eine eindeutige Funktion $y=g(x)$ mit $f(x,g(x))=0$ und
$$
Dg(x) = -[D_yf(x,g(x))]^{-1} \circ D_xf(x,g(x)).
$$

**Bedeutung:** Dies ist die Formalisierung der Frage "Wann lässt sich eine implizite Gleichung nach einer Variablen auflösen?" — die Antwort lautet: *genau dann, wenn die partielle Ableitung nach dieser Variablen invertierbar ist*. Der Satz ist die Grundlage für die spätere Theorie der Mannigfaltigkeiten (Kapitel Extrema mit Nebenbedingungen).

**Beweis** *(Beweisstil: Reduktion auf den Umkehrsatz durch geschicktes Konstruieren einer Hilfsfunktion — "Trick", der in der Literatur Standard ist)*

**Konstruktion:** Definiere $F: U\times V \to X \times Z$ durch
$$
F(x,y) := (x, f(x,y)).
$$
Die Ableitung von $F$ bei $(x_0,y_0)$ ist (in Blockmatrix-Form bezüglich der Zerlegung $X\times Y \to X\times Z$):
$$
DF(x_0,y_0) = \begin{pmatrix} \mathrm{id}_X & 0 \\ D_xf(x_0,y_0) & D_yf(x_0,y_0) \end{pmatrix}.
$$

**Invertierbarkeit von $DF(x_0,y_0)$:** Da $D_yf(x_0,y_0)$ nach Voraussetzung invertierbar ist, ist diese Blockmatrix invertierbar mit expliziter Inverser
$$
DF(x_0,y_0)^{-1} = \begin{pmatrix} \mathrm{id}_X & 0 \\ -D_yf(x_0,y_0)^{-1}D_xf(x_0,y_0) & D_yf(x_0,y_0)^{-1} \end{pmatrix}
$$
*(Nachweis durch direktes Ausmultiplizieren beider Produkte $DF\cdot DF^{-1} = DF^{-1}\cdot DF = \mathrm{id}$.)*

**Anwendung des Umkehrsatzes auf $F$:** Da $DF(x_0,y_0)$ invertierbar und $F$ stetig differenzierbar ist, existiert nach Satz 1.42 eine lokale $C^1$-Umkehrabbildung $F^{-1}$, definiert auf einer Umgebung $U_0\times U_1$ von $F(x_0,y_0)=(x_0,f(x_0,y_0))$, mit
$$
F^{-1}(x,w) = (x, g(x,w)) \qquad \text{für eine Funktion } g,
$$
(die erste Komponente von $F^{-1}$ ist $x$, da $F$ die $x$-Komponente unverändert lässt).

**Verifikation der gesuchten Eigenschaft:** Aus $F(F^{-1}(x,w))=(x,w)$ folgt $F(x,g(x,w)) = (x, f(x,g(x,w))) = (x,w)$, also $f(x,g(x,w))=w$ — genau die behauptete Eigenschaft. Stetige Differenzierbarkeit von $g$ folgt aus der von $F^{-1}$ (Umkehrsatz). $\blacksquare$

<a id="beispiele-10"></a>
## Beispiele

**Beispiel 1 (leicht — Einheitskreis):** Sei $\phi(x,y) = x^2+y^2-1$. Bei $(x_0,y_0)=(0,1)$ gilt $D_y\phi(0,1) = 2y|_{(0,1)} = 2 \neq 0$ — invertierbar. Nach Satz 1.45 lässt sich $\phi=0$ lokal um $(0,1)$ nach $y$ auflösen: $y=g(x)=\sqrt{1-x^2}$ (das positive Vorzeichen, da $g(0)=1$).

**Beispiel 2 (mittel):** Bei $(x_0,y_0)=(1,0)$ (rechter Rand des Kreises) gilt $D_y\phi(1,0)=2\cdot 0=0$ — **nicht** invertierbar! Hier lässt sich die Gleichung *nicht* lokal nach $y$ auflösen (der Kreis hat dort eine vertikale Tangente — für jedes $x$ nahe $1$ gibt es zwei $y$-Werte oder keinen). Man kann aber stattdessen nach $x$ auflösen: $D_x\phi(1,0)=2\neq 0$.

**Beispiel 3 (schwer — Anwendung des Umkehrsatzes auf ein nichtlineares System):** Betrachten Sie $f:\mathbb{R}^2\to\mathbb{R}^2$, $f(x,y)=(x+y^2, y+x^2)$. Bei $(0,0)$: $Df(0,0) = \begin{pmatrix}1&0\\0&1\end{pmatrix} = \mathrm{id}$, invertierbar. Nach dem Umkehrsatz existiert lokal um $(0,0)$ eine Umkehrfunktion — obwohl $f$ selbst nicht global injektiv sein muss.

<a id="gegenbeispiele-10"></a>
## Gegenbeispiele

- **$Df(x_0)$ nicht invertierbar $\Rightarrow$ Umkehrsatz nicht anwendbar (aber lokale Umkehrbarkeit evtl. trotzdem möglich oder nicht):** $f(x)=x^3$ bei $x_0=0$: $f'(0)=0$, Umkehrsatz nicht anwendbar. Tatsächlich ist $f$ hier sogar global bijektiv — der Umkehrsatz liefert nur eine *hinreichende*, keine notwendige Bedingung für lokale Umkehrbarkeit.
- **$f(x)=x^2$ bei $x_0=0$:** $f'(0)=0$, und tatsächlich ist $f$ hier **nicht** lokal injektiv (jede Umgebung von $0$ enthält Punkte $x,-x$ mit $f(x)=f(-x)$) — hier korrespondiert die Entartung der Ableitung tatsächlich mit dem Scheitern der lokalen Umkehrbarkeit.
- **Fixpunktsatz ohne Vollständigkeit:** $M=(0,1)$ (nicht vollständig, offenes Intervall), $F(x)=x/2$. $F$ ist Kontraktion mit $\lambda=1/2$, aber der einzige Fixpunkt $0 \notin M$ — der Satz greift nicht, weil $M$ nicht vollständig ist.
- **Fixpunktsatz mit $\lambda=1$ (nicht strikt):** $M=\mathbb{R}$, $F(x)=x+1$. Hier $d(F(x),F(y))=d(x,y)$ (Isometrie, $\lambda=1$), aber $F$ hat **keinen** Fixpunkt.

<a id="typische-klausuraufgaben-11"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Erkennungsmerkmal | Strategie |
|---|---|---|
| "Zeigen Sie, dass $F$ eine Kontraktion ist, und finden Sie den Fixpunkt" | Explizite Iterationsvorschrift oder Gleichung $x=F(x)$ | Kontraktionskonstante $\lambda<1$ nachweisen (oft via Ableitung: $|F'(x)|\le\lambda$), dann Banach-Fixpunktsatz zitieren |
| "Ist $f$ bei $x_0$ lokal umkehrbar?" | Konkrete (meist $\mathbb{R}^n\to\mathbb{R}^n$) Funktion, Punkt gegeben | Jacobi-Matrix bei $x_0$ berechnen, Determinante $\neq 0$ prüfen (⟺ invertierbar im Endlichdimensionalen) |
| "Lässt sich $\phi(x,y)=0$ nach $y$ auflösen?" | Implizite Gleichung, oft Kurven/Flächen (Kreis, Ellipse, etc.) | $D_y\phi$ berechnen und auf Invertierbarkeit prüfen; bei Nichtinvertierbarkeit alternative Variable probieren |
| "Berechnen Sie $g'(x)$ für die implizit definierte Funktion" | Nach Existenznachweis gefragt | Formel $Dg = -[D_y\phi]^{-1}D_x\phi$ anwenden (oder implizites Differenzieren direkt) |
| "Warum funktioniert der Umkehrsatz hier nicht?" | Punkt mit singulärer Jacobi-Matrix | Determinante = 0 zeigen, ggf. Gegenbeispiel für tatsächliches Scheitern der Injektivität konstruieren |

<a id="typische-fehler-11"></a>
## Typische Fehler

1. **Determinantenkriterium unreflektiert auf unendlichdimensionale Räume übertragen:** "Invertierbar" bedeutet in $L(X,Y)$ für unendlichdimensionale Räume **nicht** "Determinante $\neq 0$" (Determinanten sind dort i.A. nicht definiert) — man muss echte Bijektivität mit stetiger Inverser zeigen.
2. **Globale statt lokale Umkehrbarkeit behaupten:** Der Umkehrsatz liefert *nur* eine lokale Aussage. $f(x)=x^3+x$ hat überall $f'(x)>0$, ist also überall lokal (und hier sogar global) umkehrbar — aber das folgt streng genommen aus punktweiser Anwendung, nicht automatisch aus einer einzigen Anwendung des Satzes.
3. **Vollständigkeit beim Fixpunktsatz vergessen zu prüfen** (klassischer Fehler: Kontraktion auf offenem statt abgeschlossenem Intervall).
4. **$\lambda<1$ nicht strikt nachweisen** — "$\lambda\le 1$" reicht nicht.
5. **Beim Satz über implizite Funktionen die falsche partielle Ableitung prüfen** (z.B. $D_x\phi$ statt $D_y\phi$, wenn nach $y$ aufgelöst werden soll).

<a id="verbindungen-12"></a>
## Verbindungen

- Satz 1.42 und Satz 1.45 sind **äquivalent** (jeder folgt aus dem anderen) — hier wurde der Umkehrsatz als primär gewählt und der Satz über implizite Funktionen daraus hergeleitet.
- Der Satz über implizite Funktionen ist die Grundlage für die Definition von **Mannigfaltigkeiten** (Kapitel Extrema mit Nebenbedingungen, Definition der Mannigfaltigkeit über $\phi(x)=0$ mit vollem Rang von $D\phi$).
- Der Banach-Fixpunktsatz taucht in der Numerik (Fixpunktiteration, Newton-Verfahren als Spezialfall) und in der Theorie gewöhnlicher Differentialgleichungen (Satz von Picard-Lindelöf, dort nicht behandelt, aber strukturell identisch) wieder auf.
- Lemma 1.44 (Offenheit von $GL(X,Y)$) wird für die Differenzierbarkeit der Umkehrfunktion im Beweis von Satz 1.42 selbst gebraucht — ein Beispiel für die enge Verzahnung der Resultate.

<a id="zusammenfassung-kapitel-3-4"></a>
## Zusammenfassung Kapitel 3 & 4

- Ein **Banachraum** ist ein vollständiger normierter Vektorraum; jede Norm induziert eine Metrik (Lemma 1.29).
- Für lineare Abbildungen sind **Beschränktheit und Stetigkeit äquivalent** (Lemma 1.74) — der Raum $L(A,B)$ der beschränkten linearen Abbildungen ist selbst ein Banachraum (Lemma 1.35).
- Die **Fréchet-Ableitung** $Df(x)\in L(A,B)$ verallgemeinert die klassische Ableitung als beste lineare Approximation; es gilt die **Kettenregel** $D(g\circ f)=Dg(f(x))\circ Df(x)$, aber **keine allgemeine Produktregel** (nur für bilineare Abbildungen).
- Die **Mittelwertungleichung** $\|f(x)-f(y)\|\le M\|x-y\|$ ersetzt den (in Banachräumen i.A. falschen) klassischen Mittelwertsatz.
- Der **Banach-Fixpunktsatz** garantiert Existenz und Eindeutigkeit eines Fixpunkts einer Kontraktion auf einem vollständigen metrischen Raum — konstruktiv über die Iterationsfolge $x_{n+1}=F(x_n)$.
- Der **Umkehrsatz** garantiert lokale Umkehrbarkeit, wenn $Df(x_0)$ ein beschränkter Isomorphismus ist; sein Beweis reduziert das Problem via Fixpunktgleichung auf den Banach-Fixpunktsatz.
- Der **Satz über implizite Funktionen** ist äquivalent zum Umkehrsatz und beantwortet, wann sich $f(x,y)=0$ lokal nach $y$ auflösen lässt: genau dann, wenn $D_yf$ invertierbar ist.

---

*Ende Teil 2. Fortsetzung folgt mit Kapitel 5 (Höhere Ableitungen, Taylor-Formel in Banachräumen) und Kapitel 6 (Hilberträume) auf Anfrage.*



---

<a id="analysis-auf-allgemeinen-linearen-räumen-teil-3"></a>
# Analysis auf allgemeinen linearen Räumen — Teil 3

*Fortsetzung von Teil 1 (Topologie, Metrik) und Teil 2 (Banachräume, Umkehrsatz). Dieses Dokument setzt beide als bekannt voraus.*

---

<a id="kapitel-5-höhere-ableitungen-und-die-taylor-formel"></a>
# Kapitel 5: Höhere Ableitungen und die Taylor-Formel

<a id="motivation-13"></a>
## Motivation

**Welches Problem lösen wir?**

Die erste Ableitung $Df(x)$ liefert die beste *lineare* Approximation von $f$ bei $x$. Aber lineare Approximationen sind oft zu grob: Sie können nicht zwischen einem lokalen Minimum, Maximum oder Sattelpunkt unterscheiden (an einem kritischen Punkt ist $Df(x)=0$, egal welcher Fall vorliegt). Um solche feineren Fragen zu beantworten, braucht man **quadratische** (und höhere) Approximationen — die **Taylor-Formel**. Diese wiederum setzt voraus, dass wir sinnvoll von der "Ableitung der Ableitung" sprechen können.

**Warum ist das technisch heikel?** $Df$ ist selbst eine Abbildung mit Werten im Banachraum $L(X,Y)$ — die zweite Ableitung $D^2f(x) = D(Df)(x)$ ist dann ein Element von $L(X,L(X,Y))$. Das ist zunächst kein "Objekt mit zwei Eingaben", sondern eine "Abbildung, die eine Abbildung ausgibt, die dann wieder etwas einsetzt". Der entscheidende Schritt dieses Kapitels ist der Nachweis, dass sich $L(X,L(X,Y))$ **kanonisch identifizieren** lässt mit dem Raum der stetigen **bilinearen** Abbildungen $X\times X \to Y$ — dadurch wird $D^2f(x)$ zu einem vertrauten Objekt: einer symmetrischen Bilinearform (die im $\mathbb{R}^n$ als **Hesse-Matrix** erscheint).

<a id="intuition-13"></a>
## Intuition

Denken Sie an die eindimensionale Taylor-Reihe:
$$
f(x+h) = f(x) + f'(x)h + \tfrac12 f''(x)h^2 + \dots
$$
Jeder Term ist ein Polynom in $h$ vom entsprechenden Grad. Im Banachraum-Fall wird aus "$f''(x)h^2$" der Ausdruck $D^2f(x)[h,h]$ — die zweite Ableitung wird auf **zwei Kopien** von $h$ angewendet (daher "bilinear": zwei Eingänge). Das ist konsistent mit der Schulnotation, wenn man bedenkt, dass im Eindimensionalen $D^2f(x)[h,h] = f''(x)\cdot h \cdot h = f''(x)h^2$ gilt.

**Geometrische Vorstellung:** Die erste Ableitung beschreibt die *Tangente* (Ebene), die zweite Ableitung die *Krümmung* — wie stark und in welche Richtung sich der Graph von der Tangentialebene wegbiegt. Genau diese Krümmungsinformation (kodiert in der Hesse-Matrix) entscheidet später, ob ein kritischer Punkt ein Minimum, Maximum oder Sattelpunkt ist.

<a id="formale-definitionen-13"></a>
## Formale Definitionen

<a id="definition-iterierte-ableitung"></a>
### Definition (Iterierte Ableitung)

Sei $f: U \to Y$ ($U\subseteq X$ offen) differenzierbar, sodass $Df: U \to L(X,Y)$ selbst wieder bei $x$ differenzierbar ist. Dann heißt $f$ **zweimal differenzierbar** bei $x$, und man setzt
$$
D^2f(x) := D(Df)(x) \in L\big(X, L(X,Y)\big).
$$
Allgemein, rekursiv: $f$ ist **$k$-mal differenzierbar** bei $x$, wenn $D^{k-1}f$ in einer Umgebung von $x$ existiert und bei $x$ differenzierbar ist; man setzt
$$
D^kf(x) := D(D^{k-1}f)(x) \in L^k(X,Y) := L\big(X, L^{k-1}(X,Y)\big), \qquad L^1(X,Y):=L(X,Y).
$$

<a id="definition-146-räume-der-klasse-ck"></a>
### Definition 1.46 (Räume der Klasse $C^k$)

Ist $D^kf$ in $U$ stetig, schreibt man $f \in C^k(U,Y)$. Gilt $f\in C^k(U,Y)$ für alle $k\in\mathbb{N}$, schreibt man $f \in C^\infty(U,Y)$.

<a id="definition-147-k-lineare-abbildungen"></a>
### Definition 1.47 ($k$-lineare Abbildungen)

Seien $X_1,\dots,X_k,Y$ Banachräume. Eine Abbildung $\Phi: X_1\times\dots\times X_k \to Y$ heißt **$k$-linear**, falls sie in jedem Argument (bei Festhalten der übrigen) linear ist:
$$
\Phi(x_1,\dots, x_i+y_i,\dots,x_k) = \Phi(x_1,\dots,x_i,\dots,x_k) + \Phi(x_1,\dots,y_i,\dots,x_k)
$$
$$
\Phi(x_1,\dots,\alpha x_i,\dots,x_k) = \alpha\,\Phi(x_1,\dots,x_i,\dots,x_k)
$$
für alle $i=1,\dots,k$, $\alpha \in \mathbb{R}$. Man schreibt $\tilde L^k(X,Y)$ (bzw. $L(X^k,Y)$) für die Menge der **stetigen** $k$-linearen Abbildungen $X\times\dots\times X \to Y$.

<a id="eigenschaften-12"></a>
## Eigenschaften

<a id="lemma-148-kanonischer-isomorphismus-lkxy-cong-tilde-lkxy"></a>
### Lemma 1.48 (Kanonischer Isomorphismus $L^k(X,Y) \cong \tilde L^k(X,Y)$)

**Aussage:** Es existiert ein (kanonischer, natürlicher) Isomorphismus
$$
j: L^k(X,Y) \longrightarrow \tilde L^k(X,Y) = L(X^k,Y)
$$
zwischen dem iterierten Abbildungsraum und dem Raum der $k$-linearen Abbildungen.

**Bedeutung:** Dies ist der technische Schlüssel des ganzen Kapitels: Er erlaubt es, die $k$-te Ableitung $D^kf(x)$, formal ein Element von $L^k(X,Y)$, **als** $k$-lineare Abbildung $D^kf(x): X^k \to Y$ aufzufassen und auf $k$ Vektoren gleichzeitig anzuwenden: $D^kf(x)[h_1,\dots,h_k]$.

**Beweisidee** *(Beweisstil: Induktion über $k$, mit expliziter Konstruktion des Isomorphismus)*

**Fall $k=1$:** $L^1(X,Y)=L(X,Y)=\tilde L^1(X,Y)$ — trivial, nichts zu zeigen.

**Fall $k=2$ (illustrativ):** Sei $\phi \in L^2(X,Y) = L(X,L(X,Y))$. Für $x_1,x_2 \in X$ ist $\phi(x_1) \in L(X,Y)$, also können wir $\phi(x_1)[x_2] \in Y$ bilden. Definiere
$$
j(\phi)(x_1,x_2) := \phi(x_1)[x_2].
$$
Man prüft direkt, dass $j(\phi)$ bilinear ist (Linearität in $x_2$, da $\phi(x_1)\in L(X,Y)$; Linearität in $x_1$, da $\phi$ selbst linear ist und Auswertung $\mapsto \phi(x_1)[x_2]$ die Linearität respektiert). Umgekehrt definiert man für $\psi \in \tilde L^2(X,Y)$ die Abbildung $j^{-1}(\psi) \in L(X,L(X,Y))$ via $j^{-1}(\psi)(x_1) := \psi(x_1,\cdot)$ (die partielle Auswertung). Man verifiziert $j\circ j^{-1}=\mathrm{id}$ und $j^{-1}\circ j = \mathrm{id}$.

**Induktionsschritt $k-1 \to k$:** Analog, unter Verwendung des bereits etablierten Isomorphismus für $\tilde L^{k-1}$. $\blacksquare$

> **Praktische Konsequenz:** Ab sofort schreiben wir $D^kf(x)[h_1,\dots,h_k]$ und behandeln $D^kf(x)$ als $k$-lineare, stetige (also beschränkte) Abbildung.

<a id="lemma-165-satz-von-schwarz-symmetrie-der-zweiten-ableitung"></a>
### Lemma 1.65 (Satz von Schwarz — Symmetrie der zweiten Ableitung)

**Aussage:** Sei $U \subseteq X$ offen, $f: U \to Y$ zweimal **stetig** differenzierbar. Dann ist $D^2f(x)$ (als Bilinearform aufgefasst via Lemma 1.48) **symmetrisch**:
$$
D^2f(x)[h,k] = D^2f(x)[k,h] \qquad \forall h,k \in X.
$$

**Bedeutung:** Dies ist einer der überraschendsten und wichtigsten Sätze der mehrdimensionalen Analysis — a priori gibt es keinen Grund, warum die Reihenfolge, in der man zweimal ableitet, keine Rolle spielen sollte. Im $\mathbb{R}^n$ bedeutet dies die Symmetrie der **Hesse-Matrix** und die Vertauschbarkeit gemischter partieller Ableitungen $\partial_i\partial_j f = \partial_j\partial_i f$.

**Beweisidee** *(Beweisstil: direkte $\varepsilon$-Abschätzung über eine geschickt konstruierte Hilfsgröße $A(h,k)$, symmetrisch per Konstruktion)*

Definiere für $h,k\in X$ (klein genug, sodass alle Auswertungen in $U$ liegen):
$$
A(h,k) := f(x+h+k) - f(x+h) - f(x+k) + f(x).
$$
**Beobachtung:** $A(h,k) = A(k,h)$ per Definition (die Formel ist symmetrisch in $h,k$).

**Kernbehauptung:** $\|A(h,k) - D^2f(x)[h,k]\| = o(\|h\|+\|k\|)^2$ (kleiner als quadratisch).

Aus dieser Behauptung folgt der Satz: Da auch $A(h,k)=A(k,h)$, muss
$$
D^2f(x)[h,k] - D^2f(x)[k,h] = o((\|h\|+\|k\|)^2)
$$
gelten; setzt man $h=\varepsilon\hat h$, $k=\varepsilon\hat k$ mit $\|\hat h\|=\|\hat k\|=1$, so ist die linke Seite (bilinear!) proportional zu $\varepsilon^2$, während die rechte Seite $o(\varepsilon^2)$ ist — für $\varepsilon\to 0$ folgt, dass der (in $\varepsilon$ konstante) Koeffizient verschwinden muss:
$$
D^2f(x)[\hat h,\hat k] - D^2f(x)[\hat k,\hat h] = 0.
$$

**Beweis der Kernbehauptung** (Skizze): Man definiert $B(h) := f(x+h+k)-f(x+h) - Df(x+k)[h] + Df(x)[h]$ und leitet diese Hilfsfunktion nach $h$ ab, wobei man die Differenzierbarkeit von $Df$ (also $D^2f$-Existenz) verwendet:
$$
DB(h) = Df(x+h+k) - Df(x+h) - Df(x+k)+Df(x) + o(1) = D^2f(x)[h,k] + o(\|h\|+\|k\|).
$$
Über die Mittelwertungleichung, angewendet auf $B$ (mit $B(0)=A(k)-\text{const}$, technisches Detail), erhält man die behauptete quadratische Fehlerabschätzung. $\blacksquare$

*(Dieser Beweis wird im Skript mit voller technischer Sorgfalt ausgeführt — er ist der schwierigste Beweis der Vorlesung. Für Klausurzwecke reicht in der Regel das Verständnis der Grundidee: symmetrische Hilfsgröße $A(h,k)$ konstruieren, zeigen, dass sie $D^2f(x)[h,k]$ bis auf einen Fehler kleiner als quadratisch approximiert.)*

<a id="sätze-11"></a>
## Sätze

<a id="satz-149-taylor-formel-in-banachräumen"></a>
### Satz 1.49 (Taylor-Formel in Banachräumen)

**Aussage:** Seien $X,Y$ Banachräume, $U\subseteq X$ offen, $f\in C^k(U,Y)$. Dann existieren stetige Abbildungen $\phi_p: U \to \tilde L^p(X,Y)$ für $p=1,\dots,k$ und eine stetige Abbildung $R_k: \tilde U \to \tilde L^k(X,Y)$ (auf einer geeigneten Menge $\tilde U$ von Paaren $(x,h)$), sodass
$$
f(x+h) = f(x) + \phi_1(x)[h] + \tfrac{1}{2}\phi_2(x)[h,h] + \dots + \tfrac{1}{k!}\phi_k(x)[h,\dots,h] + R_k(x,h)[h,\dots,h],
$$
wobei $R_k(x,0)=0$ und $\phi_p(x) = j(D^pf)(x)$ (der Isomorphismus aus Lemma 1.48).

**Bedeutung:** Dies ist die Verallgemeinerung der klassischen Taylor-Formel auf beliebige Banachräume. Sie zerlegt $f$ in einen Polynomanteil (in $h$) plus einen Restterm, der (unter geeigneten Voraussetzungen) klein von höherer Ordnung ist.

**Beweisidee** *(Beweisstil: vollständige Induktion über $k$, mit dem Grundfall $k=1$ als Differenzierbarkeitsdefinition)*

**Induktionsanfang $k=1$:** Dies ist exakt die Definition der Differenzierbarkeit (Def. 1.37): $f(x+h)-f(x)-Df(x)[h] = o(\|h\|)$.

**Induktionsschritt:** Sei die Formel für $k=n-1$ bereits gezeigt. Man zeigt, dass die Ableitung des Taylor-Polynoms $T_{f,n}(h)$ (bezüglich $h$, an der Stelle $x$ fest) gleich dem Taylor-Polynom der um eine Ordnung reduzierten Ableitung $Df$ ist:
$$
D_h T_{f,n}(h) = T_{Df,n-1}(h).
$$
Zusammen mit der Induktionsvoraussetzung, angewendet auf $Df$ (welches als $C^{n-1}$ vorausgesetzt werden kann, da $f\in C^n$), und der Mittelwertungleichung, um von einer Abschätzung der *Ableitung* des Restglieds auf eine Abschätzung des Restglieds selbst zu schließen, folgt die Behauptung für $k=n$. $\blacksquare$

*(Die Mitschrift bezeichnet diesen Beweis treffend als "ein etwas schwächeres Resultat" — die vollständige technische Ausführung mit allen Indizes ist for Klausurzwecke nicht in voller Tiefe erforderlich; die Beweisidee — Induktion über die Ordnung, Kopplung über $D_hT_{f,n}=T_{Df,n-1}$ — sollte aber sitzen.)*

<a id="korollar-166-taylorformel-im-mathbbrn-explizite-koordinatenform"></a>
### Korollar 1.66 (Taylorformel im $\mathbb{R}^n$, explizite Koordinatenform)

**Aussage:** Sei $U\subseteq\mathbb{R}^n$ offen, $f: U\to\mathbb{R}$ $k$-mal stetig differenzierbar. Dann gilt für $x, x+h \in U$ (mit Verbindungsstrecke in $U$):
$$
f(x+h) = f(x) + \sum_{i=1}^n \frac{\partial f}{\partial x_i}(x)h_i + \frac12\sum_{i,j=1}^n \frac{\partial^2f}{\partial x_i\partial x_j}(x)h_ih_j + \dots + \frac{1}{k!}\sum_{i_1,\dots,i_k=1}^n \frac{\partial^kf(x)}{\partial x_{i_1}\cdots\partial x_{i_k}}h_{i_1}\cdots h_{i_k} + R_k(x,h),
$$
mit Restglied (Lagrange-Form)
$$
R_k(x,h) = \frac{1}{k!}\sum_{i_1,\dots,i_k} \left(\frac{\partial^kf(x+sh)}{\partial x_{i_1}\cdots\partial x_{i_k}} - \frac{\partial^kf(x)}{\partial x_{i_1}\cdots\partial x_{i_k}}\right) h_{i_1}\cdots h_{i_k}, \qquad s\in(0,1).
$$

**Bedeutung:** Dies ist die konkrete, klausurrelevante Form der Taylorformel — der Spezialfall $X=\mathbb{R}^n$, $Y=\mathbb{R}$ von Satz 1.49, wobei die $k$-lineare Form $D^kf(x)$ über den Standard-Basisvektoren $e_i$ zu den partiellen Ableitungen $\partial^kf/\partial x_{i_1}\cdots\partial x_{i_k}$ wird.

<a id="beispiele-11"></a>
## Beispiele

**Beispiel 1 (leicht):** Taylorentwicklung 2. Ordnung von $f(x,y)=x^2y+e^y$ bei $(0,0)$:
$$
\nabla f(0,0) = (2xy, x^2+e^y)|_{(0,0)} = (0,1), \qquad H f(0,0) = \begin{pmatrix}2y & 2x\\ 2x & x^2+e^y\end{pmatrix}\Big|_{(0,0)} = \begin{pmatrix}0&0\\0&1\end{pmatrix}.
$$
Also $f(h,k) \approx 0 + (0,1)\cdot(h,k) + \tfrac12 k^2 = k + \tfrac12 k^2$.

**Beispiel 2 (mittel):** Zeigen Sie, dass $D^2f(x)[h,k]$ für $f: \mathbb{R}^2\to\mathbb{R}$, $f(x,y)=x^3y^2$ tatsächlich symmetrisch ist (explizite Verifikation des Satzes von Schwarz):
$$
\partial_x f = 3x^2y^2,\quad \partial_y\partial_x f = 6x^2y; \qquad \partial_y f = 2x^3y, \quad \partial_x\partial_y f = 6x^2y.
$$
Beide gemischten Ableitungen stimmen überein — wie vom Satz von Schwarz garantiert.

<a id="gegenbeispiele-11"></a>
## Gegenbeispiele

**Gegenbeispiel zum Satz von Schwarz ohne Stetigkeitsvoraussetzung:** Die klassische Funktion
$$
f(x,y) = \begin{cases} \dfrac{xy(x^2-y^2)}{x^2+y^2} & (x,y)\neq(0,0) \\ 0 & (x,y)=(0,0)\end{cases}
$$
erfüllt $\partial_x\partial_y f(0,0) = 1 \neq -1 = \partial_y\partial_x f(0,0)$ — die gemischten partiellen Ableitungen existieren zwar überall, sind aber bei $(0,0)$ **unstetig**, und die Vertauschbarkeit scheitert. Dies zeigt, dass die Stetigkeitsvoraussetzung in Lemma 1.65 **nicht** überflüssig ist.

<a id="typische-klausuraufgaben-12"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Erkennungsmerkmal | Strategie |
|---|---|---|
| "Berechnen Sie das Taylorpolynom 2. Ordnung von $f$ bei $x_0$" | Konkrete Funktion $\mathbb{R}^n\to\mathbb{R}$ | Gradient und Hesse-Matrix bei $x_0$ berechnen, in die Formel einsetzen |
| "Zeigen Sie $\partial_i\partial_jf=\partial_j\partial_i f$" | Konkrete Funktion | Beide gemischten Ableitungen explizit berechnen und vergleichen (Verifikation, kein Beweis nötig) |
| "Ist $f\in C^2$?" | Funktion mit möglicher Unstetigkeit im Ursprung | Partielle Ableitungen berechnen, Stetigkeit bei kritischem Punkt separat (oft über Polarkoordinaten) prüfen |

<a id="typische-fehler-12"></a>
## Typische Fehler

1. **$D^2f(x)[h,k]$ mit $D^2f(x)[h]\cdot k$ verwechseln** — es handelt sich um eine bilineare Auswertung, nicht um Multiplikation.
2. **Symmetrie des Satzes von Schwarz ohne Stetigkeitsprüfung annehmen** — insbesondere bei stückweise definierten Funktionen.
3. **Restglied bei Taylor vergessen oder falsch abschätzen** — insbesondere den Unterschied zwischen "klein von Ordnung $o(\|h\|^k)$" (qualitativ) und der expliziten Lagrange-Form (quantitativ) durcheinanderbringen.

<a id="verbindungen-13"></a>
## Verbindungen

- Lemma 1.65 (Satz von Schwarz) ist die Grundlage für die spätere Definition **geschlossener Differentialformen** (Kapitel Kurvenintegrale): $d\omega=0$ verwendet die Symmetrie gemischter partieller Ableitungen.
- Die Taylorformel 2. Ordnung (mit der Hesse-Matrix) ist das zentrale Werkzeug für die **Extremwerttheorie** (nächstes Kapitel): Definitheit der Hesse-Matrix entscheidet über Minima/Maxima/Sattelpunkte.
- Lemma 1.48 (Isomorphismus $L^k \cong \tilde L^k$) wird stillschweigend in der gesamten mehrdimensionalen Differentialrechnung benutzt, sobald man von "der Hesse-Matrix" statt von "der iterierten Ableitung" spricht.

---

<a id="kapitel-6-hilberträume"></a>
# Kapitel 6: Hilberträume

<a id="motivation-14"></a>
## Motivation

**Welches Problem lösen wir?**

Ein Banachraum liefert Längen (Normen), aber keine **Winkel**. Wir können nicht von "Orthogonalität" sprechen, keine orthogonalen Projektionen bilden, keine "kürzeste Verbindung zu einem Unterraum" bestimmen. Der **Hilbertraum** schließt diese Lücke: Er stattet den Vektorraum mit einem **Skalarprodukt** aus, aus dem sich sowohl eine Norm (Längenmessung) als auch ein Winkelbegriff (über den Kosinussatz) ableiten lässt.

**Warum brauchen wir das in dieser Vorlesung?** Hilberträume liefern das technische Werkzeug (**Gram-Schmidt-Verfahren**, **Orthonormalbasen**), das später — insbesondere beim Aufbau von Koordinaten im $\mathbb{R}^n$ und der Transformationsformel für Mehrfachintegrale (Kapitel Integration) — implizit gebraucht wird, um Volumina über Determinanten auszudrücken.

<a id="intuition-14"></a>
## Intuition

Ein **Skalarprodukt** $\langle x,y\rangle$ verallgemeinert das aus der Schule bekannte "Punktprodukt" $x\cdot y = \sum x_iy_i$ im $\mathbb{R}^n$. Geometrisch codiert es zwei Informationen gleichzeitig: die *Länge* eines Vektors ($\|x\|=\sqrt{\langle x,x\rangle}$) und den *Winkel* zwischen zwei Vektoren (über $\langle x,y\rangle = \|x\|\|y\|\cos\theta$). Zwei Vektoren stehen **orthogonal** aufeinander, wenn ihr Skalarprodukt verschwindet — eine algebraische Fassung der geometrischen Rechtwinkligkeit.

Die **Cauchy-Schwarz-Ungleichung** $|\langle x,y\rangle| \le \|x\|\|y\|$ ist die präzise Aussage "der Kosinus eines Winkels liegt zwischen $-1$ und $1$" — ohne dass man den Winkel selbst je definiert haben muss.

Das **Gram-Schmidt-Verfahren** ist ein Algorithmus, der aus einer beliebigen (linear unabhängigen) Basis eine **orthonormale** Basis konstruiert — man kann sich das vorstellen wie das "Begradigen" eines schiefen Koordinatensystems zu einem rechtwinkligen: Jeder neue Basisvektor wird zunächst von allen bereits konstruierten orthogonalen Richtungen "befreit" (Projektion abziehen) und dann auf Länge 1 normiert.

<a id="formale-definitionen-14"></a>
## Formale Definitionen

<a id="definition-150-skalarprodukt"></a>
### Definition 1.50 (Skalarprodukt)

Sei $V$ Vektorraum über $\mathbb{R}$ (oder $\mathbb{C}$). Eine Abbildung $\langle\cdot,\cdot\rangle: V\times V\to\mathbb{R}$ (bzw. $\mathbb{C}$) heißt **Skalarprodukt**, falls für alle $x,y,z\in V$, $\alpha\in\mathbb{R}$ (bzw. $\mathbb{C}$):

$$
\begin{aligned}
\text{(i)}\quad & \langle x,y\rangle = \overline{\langle y,x\rangle} \quad \text{(Konjugiert-Symmetrie; im Reellen: } \langle x,y\rangle=\langle y,x\rangle\text{)}\\
\text{(ii)}\quad & \langle x,y+z\rangle = \langle x,y\rangle + \langle x,z\rangle \quad \text{(Additivität)}\\
\text{(iii)}\quad & \langle x,\alpha y\rangle = \alpha\langle x,y\rangle \quad \text{(Homogenität im 2. Argument)}\\
\text{(iv)}\quad & \langle x,x\rangle \geq 0, \text{ und } \langle x,x\rangle=0 \iff x=0 \quad \text{(positive Definitheit)}
\end{aligned}
$$

> **Bemerkung zur Sesquilinearität (komplexer Fall):** Aus (i) und (iii) folgt $\langle \alpha x, y\rangle = \overline{\alpha}\langle x,y\rangle$ — das Skalarprodukt ist im ersten Argument nur *konjugiert*-linear. Dies ist notwendig, damit (iv) überhaupt sinnvoll ist ($\langle x,x\rangle$ muss reell und nicht-negativ sein).

<a id="definition-154-hilbertraum"></a>
### Definition 1.54 (Hilbertraum)

Ein Vektorraum $V$ mit Skalarprodukt $\langle\cdot,\cdot\rangle$, der bezüglich der induzierten Metrik (siehe Lemma 1.53) **vollständig** ist, heißt **Hilbertraum**.

**Standardbeispiele:**
$$
\mathbb{R}^n \text{ mit } \langle x,y\rangle = \sum_{i=1}^n x_iy_i; \qquad \ell^2(\mathbb{R}) := \left\{a:\mathbb{N}\to\mathbb{R} : \sum_i a_i^2<\infty\right\}, \quad \langle a,b\rangle := \sum_i a_ib_i.
$$

<a id="definition-156-orthonormalbasis-onb"></a>
### Definition 1.56 (Orthonormalbasis, ONB)

Eine Menge $S=\{x_\alpha\}_{\alpha\in A}$ orthonormaler Elemente eines Hilbertraums $H$ (d.h. $\|x_\alpha\|=1$ und $\langle x_\alpha,x_\beta\rangle=0$ für $\alpha\neq\beta$) heißt **Orthonormalbasis (ONB)**, falls es keine echte Obermenge $S' \supsetneq S$ von orthonormalen Elementen gibt (Maximalität).

<a id="eigenschaften-13"></a>
## Eigenschaften

<a id="lemma-151-cauchy-schwarz-ungleichung"></a>
### Lemma 1.51 (Cauchy-Schwarz-Ungleichung)

**Aussage:** Für alle $x,y \in V$ (mit Skalarprodukt) gilt
$$
|\langle x,y\rangle| \leq \sqrt{\langle x,x\rangle}\cdot\sqrt{\langle y,y\rangle}.
$$

**Bedeutung:** Fundamentalste Ungleichung der linearen Algebra/Analysis; wird für den Beweis der Dreiecksungleichung der induzierten Norm gebraucht (Lemma 1.53) sowie in unzähligen Abschätzungen überall in der Analysis.

**Beweis** *(Beweisstil: algebraischer Trick — orthogonale Zerlegung und Ausnutzen der Positivität)*

Ist $y=0$, ist die Aussage trivial ($0\le 0$). Sei $y\neq 0$. Definiere die **Orthogonalprojektion** von $x$ auf $y$:
$$
z := x - \frac{\langle y,x\rangle}{\langle y,y\rangle} y.
$$
Man rechnet nach, dass $\langle z,y\rangle = \langle x,y\rangle - \frac{\langle y,x\rangle}{\langle y,y\rangle}\langle y,y\rangle = \langle x,y\rangle - \langle y,x\rangle = 0$ (im Reellen; $z$ steht orthogonal zu $y$ — daher der Name "Projektion"). Dann gilt (Satz des Pythagoras, algebraisch):
$$
\langle x,x\rangle = \left\langle z + \frac{\langle y,x\rangle}{\langle y,y\rangle}y,\ z+\frac{\langle y,x\rangle}{\langle y,y\rangle}y\right\rangle = \langle z,z\rangle + \frac{|\langle x,y\rangle|^2}{\langle y,y\rangle} \geq \frac{|\langle x,y\rangle|^2}{\langle y,y\rangle}
$$
(da $\langle z,z\rangle\ge 0$ nach positiver Definitheit, und die gemischten Terme wegen $\langle z,y\rangle=0$ verschwinden). Umstellen liefert
$$
|\langle x,y\rangle|^2 \leq \langle x,x\rangle\langle y,y\rangle \quad \Rightarrow \quad |\langle x,y\rangle| \leq \sqrt{\langle x,x\rangle}\sqrt{\langle y,y\rangle}. \qquad \blacksquare
$$

<a id="lemma-153-skalarprodukt-induziert-norm"></a>
### Lemma 1.53 (Skalarprodukt induziert Norm)

**Aussage:** $\|x\|:=\sqrt{\langle x,x\rangle}$ ist eine Norm auf $V$; insbesondere gilt die Dreiecksungleichung.

**Beweis der Dreiecksungleichung** *(direkte Rechnung unter Verwendung von Cauchy-Schwarz)*:
$$
\|x+y\|^2 = \langle x+y,x+y\rangle = \langle x,x\rangle + \langle y,y\rangle + 2\langle x,y\rangle \leq \|x\|^2+\|y\|^2+2\|x\|\|y\| = (\|x\|+\|y\|)^2,
$$
wobei im Ungleichheitsschritt $\langle x,y\rangle \le |\langle x,y\rangle| \le \|x\|\|y\|$ (Cauchy-Schwarz) verwendet wurde. Wurzelziehen liefert die Behauptung. $\blacksquare$

**Konsequenz:** Jeder Hilbertraum ist insbesondere ein Banachraum — die Hierarchie lautet also:
$$
\text{Hilbertraum} \ \subsetneq\ \text{Banachraum} \ \subsetneq\ \text{normierter Raum} \ \subsetneq\ \text{metrischer Raum} \ \subsetneq\ \text{topologischer Raum}.
$$

<a id="vergleichstabelle-die-raumhierarchie"></a>
## Vergleichstabelle: Die Raumhierarchie

| Struktur | Zusätzliche Daten | Was neu möglich wird | Beispiel |
|---|---|---|---|
| **Topologischer Raum** | Umgebungssystem $N(x)$ | Konvergenz, Stetigkeit | beliebige Mengen mit Umgebungsaxiomen |
| **Metrischer Raum** | Metrik $d(x,y)$ | Quantitative Nähe, Cauchy-Folgen | $(\mathbb{Q},|\cdot|)$ |
| **Normierter Raum** | Norm $\|x\|$ (+ Vektorraumstruktur) | Addition, Skalierung, Längen | $(C^0[0,1],\|\cdot\|_\infty)$ |
| **Banachraum** | + Vollständigkeit | Grenzwerte von Cauchy-Folgen existieren im Raum | $\ell^p$, $C^0[0,1]$ mit $\|\cdot\|_\infty$ |
| **Hilbertraum** | + Skalarprodukt (+ Vollständigkeit) | Winkel, Orthogonalität, Projektionen | $\mathbb{R}^n$, $\ell^2$ |

<a id="satz-155-157-existenz-von-orthonormalbasen-gram-schmidt"></a>
### Satz 1.55 & 1.57 (Existenz von Orthonormalbasen, Gram-Schmidt)

**Aussage (Satz 1.57):** Jeder Hilbertraum $H$ besitzt eine Orthonormalbasis. Ist $H$ separabel (besitzt eine abzählbare dichte Teilmenge), so besitzt $H$ eine **abzählbare** ONB, die mit dem Gram-Schmidt-Verfahren aus einer beliebigen abzählbaren, linear unabhängigen, dichten Familie konstruiert werden kann.

<a id="algorithmus-gram-schmidt-verfahren"></a>
## Algorithmus: Gram-Schmidt-Verfahren

**Motivation:** Gegeben eine linear unabhängige, aber nicht notwendig orthogonale Familie von Vektoren $(v_1,\dots,v_n)$, konstruiere eine orthonormale Familie $(e_1,\dots,e_n)$, die denselben Unterraum aufspannt.

**Idee:** Iterativ: Nimm den nächsten Vektor $v_{k+1}$, ziehe seine Projektionen auf alle bisher konstruierten $e_1,\dots,e_k$ ab (macht ihn orthogonal zu allen vorherigen), normiere das Ergebnis.

**Voraussetzungen:** $(v_1,\dots,v_n)$ linear unabhängig in einem Vektorraum mit Skalarprodukt.

**Mathematische Beschreibung:**
$$
e_1 := \frac{v_1}{\|v_1\|}, \qquad e_{k+1} := \frac{v_{k+1} - \sum_{i=1}^k \langle e_i,v_{k+1}\rangle e_i}{\left\|v_{k+1} - \sum_{i=1}^k \langle e_i,v_{k+1}\rangle e_i\right\|} \qquad (k=1,\dots,n-1).
$$

**Pseudocode:**
```
GRAM-SCHMIDT(v_1, ..., v_n):
    e_1 := v_1 / ||v_1||
    for k = 1 to n-1:
        w := v_{k+1}
        for i = 1 to k:
            w := w - <e_i, v_{k+1}> * e_i     # Projektionen abziehen
        e_{k+1} := w / ||w||                   # normieren
    return e_1, ..., e_n
```

**Korrektheitsidee** *(Induktion über $k$)*: Man zeigt per Induktion, dass $(e_1,\dots,e_k)$ nach jedem Schritt orthonormal ist und denselben Unterraum wie $(v_1,\dots,v_k)$ aufspannt. Der Kern der Induktion: Für $j\le k$ gilt
$$
\langle e_{k+1}, e_j\rangle = \frac{1}{\|w\|}\left(\langle v_{k+1},e_j\rangle - \sum_{i=1}^k \langle e_i,v_{k+1}\rangle\langle e_i,e_j\rangle\right) = \frac{1}{\|w\|}\big(\langle v_{k+1},e_j\rangle - \langle e_j,v_{k+1}\rangle\big) = 0
$$
(da $\langle e_i,e_j\rangle=\delta_{ij}$ nach Induktionsvoraussetzung, und im Reellen $\langle e_j,v_{k+1}\rangle=\langle v_{k+1},e_j\rangle$).

**Laufzeit:** $O(n^2 d)$ für $n$ Vektoren der Dimension $d$ (jeder der $n$ Schritte benötigt bis zu $n$ Skalarprodukt-Berechnungen, jede in $O(d)$).

**Speicherbedarf:** $O(nd)$ (Speicherung aller Vektoren).

**Typische Anwendungen:** QR-Zerlegung von Matrizen, Konstruktion orthonormaler Polynombasen (Legendre-Polynome), Konstruktion von Koordinatensystemen im Beweis des Transformationssatzes (Kapitel Integration — Determinante als Volumen).

**Typische Fehler:** Normierung *vor* statt *nach* der Projektionsabziehung; Verwechslung von $\langle e_i,v_{k+1}\rangle$ mit $\langle v_{k+1},e_i\rangle$ im komplexen Fall (Reihenfolge relevant wegen Konjugation); numerische Instabilität bei fast linear abhängigen Vektoren (in der Praxis verwendet man daher die numerisch stabilere *modifizierte* Gram-Schmidt-Variante).

<a id="satz-158-parseval-artige-entwicklung-besselsche-ungleichung"></a>
### Satz 1.58 (Parseval-artige Entwicklung, Besselsche Ungleichung)

**Aussage:** Sei $H$ Hilbertraum, $S=\{x_\alpha\}_{\alpha\in A}$ eine ONB. Dann gilt für jedes $y \in H$:
$$
y = \sum_{\alpha\in A} \langle x_\alpha,y\rangle x_\alpha \qquad \text{(Fourierentwicklung bzgl. der ONB)}, \qquad \|y\|^2 = \sum_{\alpha\in A} |\langle x_\alpha,y\rangle|^2 \qquad \text{(Parsevalsche Gleichung)}.
$$

**Bedeutung:** Dies ist die unendlichdimensionale Verallgemeinerung der vertrauten Koordinatendarstellung $y=\sum y_ie_i$ im $\mathbb{R}^n$ — jedes Element eines Hilbertraums lässt sich (im Sinne der durch die Norm induzierten Konvergenz) durch seine "Koordinaten" bezüglich einer ONB vollständig rekonstruieren.

**Beweisidee** *(Beweisstil: Besselsche Ungleichung zuerst, dann Cauchy-Folgen-Argument zur Konvergenz)*

**Schritt 1 (Besselsche Ungleichung):** Für jede endliche Teilmenge $\{x_1,\dots,x_N\}\subseteq S$ gilt
$$
0 \leq \left\|y - \sum_{i=1}^N\langle x_i,y\rangle x_i\right\|^2 = \|y\|^2 - \sum_{i=1}^N|\langle x_i,y\rangle|^2
$$
(direktes Ausmultiplizieren unter Verwendung der Orthonormalität), also $\sum_{i=1}^N |\langle x_i,y\rangle|^2 \le \|y\|^2$ für jedes $N$ — die Partialsummen sind durch $\|y\|^2$ beschränkt, also konvergiert (als monoton wachsende, beschränkte Reihe reeller Zahlen) $\sum_\alpha |\langle x_\alpha,y\rangle|^2 \le \|y\|^2$.

**Schritt 2 (Konvergenz der Reihe der Vektoren):** Man zeigt, dass die Partialsummen $y_N := \sum_{\alpha=1}^N \langle x_\alpha,y\rangle x_\alpha$ eine **Cauchy-Folge** in $H$ bilden:
$$
\|y_N - y_{N+m}\|^2 = \sum_{\alpha=N+1}^{N+m}|\langle x_\alpha,y\rangle|^2 \leq \sum_{\alpha>N}|\langle x_\alpha,y\rangle|^2 \xrightarrow{N\to\infty} 0
$$
(als Rest einer konvergenten Reihe). Da $H$ vollständig ist (Hilbertraum!), konvergiert $y_N \to y'$ für ein $y' \in H$.

**Schritt 3 (Identifikation $y'=y$):** Man zeigt $\langle y-y', x_\alpha\rangle = 0$ für alle $\alpha$ — würde $y\neq y'$ gelten, wäre $(y-y')/\|y-y'\|$ ein weiterer, zu allen $x_\alpha$ orthogonaler Einheitsvektor, was der **Maximalität** von $S$ als ONB widerspricht. Also $y=y'$. $\blacksquare$

<a id="beispiele-12"></a>
## Beispiele

**Beispiel 1 (leicht):** Führen Sie Gram-Schmidt an $v_1=(1,1,0)$, $v_2=(1,0,1)$ im $\mathbb{R}^3$ durch:
$$
e_1 = \frac{1}{\sqrt2}(1,1,0), \qquad w = v_2 - \langle e_1,v_2\rangle e_1 = (1,0,1) - \frac{1}{\sqrt2}\cdot\frac{1}{\sqrt2}(1,1,0) = \left(\tfrac12,-\tfrac12,1\right), \qquad e_2 = \frac{w}{\|w\|}.
$$

**Beispiel 2 (mittel):** Zeigen Sie, dass $\ell^2(\mathbb{R})$ mit dem angegebenen Skalarprodukt tatsächlich vollständig ist (Hilbertraum). *(Beweis analog zur Vollständigkeit von $L(A,B)$ in Kapitel 3: Cauchy-Folge komponentenweise konvergieren lassen, dann Grenzelement als in $\ell^2$ liegend nachweisen via Fatou-artigem Grenzübergang in der Normabschätzung.)*

<a id="gegenbeispiele-12"></a>
## Gegenbeispiele

- **Nicht jeder Banachraum ist Hilbertraum:** $(C^0[0,1],\|\cdot\|_\infty)$ ist Banachraum, aber die Supremumsnorm erfüllt **nicht** die Parallelogrammgleichung $\|x+y\|^2+\|x-y\|^2 = 2\|x\|^2+2\|y\|^2$ (notwendiges Kriterium dafür, dass eine Norm von einem Skalarprodukt kommt) — es gibt also kein Skalarprodukt, das diese Norm induziert.
- **Nicht jede Orthonormalfamilie ist eine ONB:** In $\mathbb{R}^3$ ist $\{e_1,e_2\}$ orthonormal, aber **nicht maximal** (nicht Basis) — $e_3$ kann noch orthogonal hinzugefügt werden.

<a id="typische-klausuraufgaben-13"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Erkennungsmerkmal | Strategie |
|---|---|---|
| "Führen Sie Gram-Schmidt an ... durch" | Explizite Vektoren gegeben | Schrittweise Formel anwenden, jeden Schritt vorrechnen |
| "Zeigen Sie Cauchy-Schwarz für konkrete Vektoren/Funktionen" | Integral- oder Summenausdruck | Direkt Lemma 1.51 zitieren oder elementar nachrechnen |
| "Ist $\langle\cdot,\cdot\rangle$ ein Skalarprodukt?" | Explizite Bilinearform gegeben | Alle 4 Axiome prüfen, insbesondere positive Definitheit oft der kritische Punkt |

<a id="typische-fehler-13"></a>
## Typische Fehler

1. **Reihenfolge im Skalarprodukt bei komplexen Räumen vertauschen** (Konjugation nicht beachtet).
2. **Normierung vor Orthogonalisierung** beim Gram-Schmidt-Verfahren.
3. **Parallelogrammgleichung ignorieren**, wenn gefragt wird, ob eine gegebene Norm von einem Skalarprodukt kommt.

<a id="verbindungen-14"></a>
## Verbindungen

- Das Gram-Schmidt-Verfahren wird in Kapitel Integration (Transformationssatz, Lemma 2.10) direkt wiederverwendet, um zu zeigen, dass das Volumen eines von Vektoren aufgespannten Parallelepipeds gleich der Determinante der entsprechenden Matrix ist.
- Die Cauchy-Schwarz-Ungleichung (Lemma 1.51) wird für die Gradientenrichtung des steilsten Anstiegs verwendet: $Df(x)[h] = \langle \nabla f(x), h\rangle \le \|\nabla f(x)\|\|h\|$, mit Gleichheit für $h \parallel \nabla f(x)$ — dies motiviert die geometrische Bedeutung des Gradienten in der Extremwerttheorie.
- Heine-Borel im $\mathbb{R}^n$ (Kapitel 2) verwendet implizit die euklidische Struktur, die vom Standard-Skalarprodukt kommt.

<a id="zusammenfassung-kapitel-5-6"></a>
## Zusammenfassung Kapitel 5 & 6

- Höhere Ableitungen $D^kf(x)$ leben formal in $L^k(X,Y)$, lassen sich aber via Lemma 1.48 kanonisch als **$k$-lineare Abbildungen** $X^k\to Y$ auffassen.
- Der **Satz von Schwarz** (Lemma 1.65) garantiert die **Symmetrie** von $D^2f(x)$ unter der Voraussetzung stetiger zweiter Differenzierbarkeit — ohne Stetigkeit kann die Symmetrie scheitern.
- Die **Taylor-Formel** (Satz 1.49, Korollar 1.66) approximiert $f$ durch Polynome in $h$, mit Koeffizienten $\tfrac{1}{k!}D^kf(x)$.
- Ein **Hilbertraum** ist ein Banachraum mit zusätzlicher Skalarproduktstruktur; die **Cauchy-Schwarz-Ungleichung** (Lemma 1.51) und die daraus folgende Dreiecksungleichung (Lemma 1.53) sind die zentralen Werkzeuge.
- Das **Gram-Schmidt-Verfahren** konstruiert aus einer beliebigen linear unabhängigen Familie eine Orthonormalfamilie; jeder (separable) Hilbertraum besitzt eine (abzählbare) Orthonormalbasis, bezüglich derer jedes Element eine konvergente "Fourierentwicklung" besitzt (Satz 1.58).

---

*Ende Teil 3. Fortsetzung folgt mit Kapitel 7 (Ableitungen im $\mathbb{R}^n$, partielle Ableitungen, Jacobi-Matrix) und Kapitel 8 (Extrema, Hesse-Matrix, Lagrange-Multiplikatoren) auf Anfrage.*



---

<a id="analysis-auf-allgemeinen-linearen-räumen-teil-4"></a>
# Analysis auf allgemeinen linearen Räumen — Teil 4

*Fortsetzung von Teil 1–3. Dieses Dokument setzt Topologie, Metrik, Banachräume, Umkehrsatz, Taylor-Formel und Hilberträume als bekannt voraus.*

---

<a id="kapitel-7-ableitungen-im-mathbbrn"></a>
# Kapitel 7: Ableitungen im $\mathbb{R}^n$

<a id="motivation-15"></a>
## Motivation

**Welches Problem lösen wir?**

Die gesamte bisherige Theorie wurde abstrakt für Banachräume entwickelt. Jetzt spezialisieren wir auf den konkretesten und wichtigsten Fall: $X=\mathbb{R}^n$, $Y=\mathbb{R}^m$. Hier wird die abstrakte Fréchet-Ableitung $Df(x) \in L(\mathbb{R}^n,\mathbb{R}^m)$ zu einem greifbaren Objekt: einer **Matrix** — der **Jacobi-Matrix**. Damit wird aus der abstrakten Theorie ein konkretes Rechenwerkzeug.

**Das zentrale Problem dieses Kapitels:** Wie berechnet man $Df(x)$ praktisch? Die Antwort liegt in den **partiellen Ableitungen** — Ableitungen entlang einzelner Koordinatenachsen. Der überraschende (und klausurrelevante!) Kern dieses Kapitels ist: *Die Existenz aller partiellen Ableitungen allein garantiert noch nicht die (Fréchet-)Differenzierbarkeit* — man braucht zusätzlich **Stetigkeit** der partiellen Ableitungen.

<a id="intuition-15"></a>
## Intuition

Stellen Sie sich eine Landschaft (Graph von $f:\mathbb{R}^2\to\mathbb{R}$) vor. Die partielle Ableitung $\partial f/\partial x$ bei einem Punkt misst die Steigung, wenn Sie **nur in Ost-West-Richtung** laufen (bei festem $y$); $\partial f/\partial y$ misst die Steigung in Nord-Süd-Richtung. Diese beiden Zahlen allein sagen aber nichts darüber aus, wie steil es in einer *diagonalen* Richtung wird — es sei denn, die Landschaft ist "glatt genug" (stetig differenzierbar), dann lässt sich die Steigung in *jede* Richtung aus den beiden Achsen-Steigungen linear kombinieren. Ist die Landschaft dagegen "zackig" (unstetige partielle Ableitungen), kann es sein, dass Sie entlang der Achsen keine Steigung wahrnehmen, aber entlang einer Diagonalen abrupt abstürzen — ein Paradebeispiel folgt unten.

<a id="formale-definitionen-15"></a>
## Formale Definitionen

<a id="definition-vektorwertige-funktionen-einer-variablen-vorstufe"></a>
### Definition (Vektorwertige Funktionen einer Variablen — Vorstufe)

$f:\mathbb{R}\to\mathbb{R}^n$, $f=(f_1,\dots,f_n)$, ist differenzierbar bei $x$ genau dann, wenn jede Komponente $f_i:\mathbb{R}\to\mathbb{R}$ differenzierbar ist, und dann gilt (Lemma 1.59):
$$
Df(x) = \sum_{i=1}^n f_i'(x)\,e_i \in L(\mathbb{R},\mathbb{R}^n).
$$

**Beweisidee:** Direkt via der Ungleichungskette $\|(f(x+h)-f(x)-Df(x)h)\| \le \sqrt{n}\cdot\max_i|f_i(x+h)-f_i(x)-f_i'(x)h|$ — Konvergenz aller $n$ reellen Differenzenquotienten gegen $f_i'(x)$ ist äquivalent zur Konvergenz des vektorwertigen Ausdrucks (Äquivalenz aller Normen im $\mathbb{R}^n$).

<a id="definition-160-partielle-ableitung-richtungsableitung"></a>
### Definition 1.60 (Partielle Ableitung, Richtungsableitung)

Sei $f:\mathbb{R}^n \to \mathbb{R}^m$ differenzierbar bei $x$. Setze $F_i(t) := f(x+te_i)$. Dann heißt
$$
\frac{\partial f}{\partial x_i}(x) := F_i'(0) = Df(x)[e_i] \in \mathbb{R}^m
$$
die **partielle Ableitung** von $f$ nach $x_i$ bei $x$.

> **Wichtige begriffliche Klärung:** Die partielle Ableitung ist ein Spezialfall der **Richtungsableitung** $D_vf(x) := Df(x)[v]$ — nämlich die Richtungsableitung in Richtung des $i$-ten Einheitsvektors $e_i$. Man kann partielle Ableitungen also berechnen, indem man alle Variablen außer $x_i$ als Konstanten behandelt und nach $x_i$ im gewöhnlichen (eindimensionalen) Sinn ableitet.

<a id="definition-jacobi-matrix"></a>
### Definition (Jacobi-Matrix)

Ist $f:\mathbb{R}^n\to\mathbb{R}^m$ bei $x$ differenzierbar, so ist $Df(x) \in L(\mathbb{R}^n,\mathbb{R}^m)$ bezüglich der Standardbasen durch die **Jacobi-Matrix**
$$
Df(x) = \left(\frac{\partial f_j}{\partial x_i}(x)\right)_{\substack{j=1,\dots,m\\ i=1,\dots,n}} = \begin{pmatrix} \dfrac{\partial f_1}{\partial x_1}(x) & \cdots & \dfrac{\partial f_1}{\partial x_n}(x) \\ \vdots & \ddots & \vdots \\ \dfrac{\partial f_m}{\partial x_1}(x) & \cdots & \dfrac{\partial f_m}{\partial x_n}(x)\end{pmatrix}
$$
gegeben, sodass $Df(x)[h] = \left(\sum_{i=1}^n \frac{\partial f_j}{\partial x_i}(x)h_i\right)_{j=1,\dots,m}$ für $h=(h_1,\dots,h_n)$.

<a id="eigenschaften-14"></a>
## Eigenschaften

<a id="lemma-161-fréchet-differenzierbar-rightarrow-alle-partiellen-ableitungen-existieren-mit-expliziter-formel"></a>
### Lemma 1.61 (Fréchet-differenzierbar $\Rightarrow$ alle partiellen Ableitungen existieren, mit expliziter Formel)

**Aussage:** Ist $f:\mathbb{R}^n\to\mathbb{R}^m$ bei $x$ (Fréchet-)differenzierbar, so existieren alle partiellen Ableitungen $\partial f_j/\partial x_i(x)$, und $Df(x)$ ist durch die Jacobi-Matrix gegeben.

**Beweisidee:** Direkt aus der Definition der Richtungsableitung: Da $Df(x)[e_i]$ definitionsgemäß gleich $\lim_{t\to 0}\frac{f(x+te_i)-f(x)}{t} = F_i'(0)$ ist (mit $F_i(t):=f(x+te_i)$, unter Ausnutzung der Fréchet-Differenzierbarkeit bei $x$, angewendet auf die spezielle Richtung $h=te_i$), folgt die Existenz und der Wert der partiellen Ableitung direkt aus der bereits etablierten Differenzierbarkeit — die Konvergenz $\lim_{t\to0}\|f(x+te_i)-f(x)-Df(x)[te_i]\|/\|te_i\|=0$ impliziert $F_i'(0)=Df(x)[e_i]$.

> **Umkehrung gilt NICHT automatisch!** Dies ist die wichtigste Warnung des ganzen Kapitels — siehe Gegenbeispiel unten.

<a id="satz-164-stetige-partielle-ableitungen-rightarrow-stetig-differenzierbar"></a>
### Satz 1.64 (Stetige partielle Ableitungen $\Rightarrow$ stetig differenzierbar)

**Aussage:** Sei $D\subseteq\mathbb{R}^n$ offen, $f: D\to\mathbb{R}^m$. Existieren alle partiellen Ableitungen $\partial f_k/\partial x_i$ ($k=1,\dots,n$, wobei hier $f$ als reellwertig angenommen wird, o.B.d.A. $m=1$) auf ganz $D$ und sind sie **stetig**, so ist $f$ in $D$ stetig differenzierbar.

**Bedeutung:** Dies ist das praktische Arbeitspferd der mehrdimensionalen Differentialrechnung: In der Praxis prüft man **nie** direkt die Fréchet-Definition, sondern berechnet die partiellen Ableitungen und prüft deren Stetigkeit — das genügt.

**Beweis** *(Beweisstil: Induktion über die Dimension $n$, Reduktion auf den eindimensionalen Mittelwertsatz in jeder Koordinatenrichtung)*

**Induktionsanfang $n=1$:** Trivial (partielle Ableitung = gewöhnliche Ableitung).

**Induktionsschritt $n-1\to n$:** Sei $x\in D$, $\delta_0>0$ mit $B_{\delta_0}(x)\subseteq D$. Schreibe $x=(\hat x, x_n)$ mit $\hat x\in\mathbb{R}^{n-1}$. Definiere $\phi(\hat\xi) := f(\hat\xi,x_n)$ für $(\hat\xi,x_n)\in D$. Da alle partiellen Ableitungen $\partial\phi/\partial x_i = \partial f/\partial x_i$ ($i=1,\dots,n-1$) stetig sind, ist nach Induktionsvoraussetzung $\phi$ stetig differenzierbar auf einer offenen Umgebung $\hat D := \{\hat\xi : (\hat\xi,x_n)\in D\}$, mit
$$
\left\|\phi(\hat x+\hat h) - \phi(\hat x) - \sum_{i=1}^{n-1}\frac{\partial\phi}{\partial x_i}(\hat x)\hat h_i\right\| \leq \frac{\varepsilon}{2}\|\hat h\| \qquad \text{für } \|\hat h\|\leq \delta_1 \text{ (aus I.V.)}.
$$
Da $\partial f/\partial x_n$ stetig ist, existiert $\delta_2$ mit $|\partial f/\partial x_n(z) - \partial f/\partial x_n(x)| < \varepsilon/2$ für $\|z-x\|<\delta_2$. Setze $\delta=\min(\delta_1,\delta_2)$.

Für $\|h\|<\delta$ zerlegt man den Gesamtzuwachs in zwei Teile — einen "diagonalen" Schritt in $x_n$-Richtung und einen "horizontalen" Schritt in den ersten $n-1$ Koordinaten:
$$
f(x+h)-f(x) - \sum_{i=1}^n \frac{\partial f}{\partial x_i}(x)h_i = \underbrace{\Big[f(\hat x+\hat h,x_n+h_n) - f(\hat x+\hat h,x_n) - \frac{\partial f}{\partial x_n}(x)h_n\Big]}_{=:A} + \underbrace{\Big[\phi(\hat x+\hat h) - \phi(\hat x) - \sum_{i=1}^{n-1}\frac{\partial\phi}{\partial x_i}(\hat x)h_i\Big]}_{=:B}.
$$
Der Term $B$ ist bereits nach Induktionsvoraussetzung durch $\tfrac\varepsilon2\|\hat h\|$ beschränkt. Für den Term $A$ wendet man den eindimensionalen Mittelwertsatz auf die Funktion $t\mapsto f(\hat x+\hat h, t)$ zwischen $x_n$ und $x_n+h_n$ an: Es existiert $\xi$ zwischen $x_n$ und $x_n+h_n$ mit
$$
A = \left(\frac{\partial f}{\partial x_n}(\hat x+\hat h,\xi) - \frac{\partial f}{\partial x_n}(x)\right)h_n,
$$
und da $(\hat x+\hat h,\xi)$ innerhalb der $\delta_2$-Umgebung von $x$ liegt, ist $|A| \leq \tfrac\varepsilon2 |h_n| \le \tfrac\varepsilon2\|h\|$.

Zusammen: $\|f(x+h)-f(x)-\sum_i \partial_if(x)h_i\| \leq \varepsilon\|h\|$ für $\|h\|<\delta$ — genau die Definition der (stetigen) Differenzierbarkeit. $\blacksquare$

<a id="gegenbeispiele-13"></a>
## Gegenbeispiele

<a id="das-standard-gegenbeispiel-partielle-ableitungen-existieren-aber-f-ist-nicht-differenzierbar"></a>
### Das Standard-Gegenbeispiel: Partielle Ableitungen existieren, aber $f$ ist nicht differenzierbar

$$
f: \mathbb{R}^2 \to \mathbb{R}, \qquad f(x,y) = (xy)^{1/3}.
$$

**Partielle Ableitungen bei $(0,0)$:**
$$
\frac{\partial f}{\partial x}(0,0) = \lim_{t\to0}\frac{f(t,0)-f(0,0)}{t} = \lim_{t\to0}\frac{0-0}{t}=0, \qquad \text{analog } \frac{\partial f}{\partial y}(0,0)=0.
$$
Beide partiellen Ableitungen existieren bei $(0,0)$ und sind $=0$.

**Aber:** Die Richtungsableitung in diagonaler Richtung $v=(1,1)$ ergibt
$$
\lim_{t\to0}\frac{f(t,t)-f(0,0)}{t} = \lim_{t\to0}\frac{(t^2)^{1/3}}{t} = \lim_{t\to0} t^{2/3-1} = \lim_{t\to0}t^{-1/3} = \infty \qquad (\neq 0!)
$$

Wäre $f$ bei $(0,0)$ (Fréchet-)differenzierbar, müsste nach Linearität von $Df(0,0)$ gelten: Richtungsableitung in Richtung $(1,1)$ $=Df(0,0)[(1,1)]=\partial_xf(0,0)+\partial_yf(0,0)=0$. Der tatsächliche Wert ist aber divergent — **Widerspruch**. Also ist $f$ bei $(0,0)$ **nicht differenzierbar**, obwohl beide partiellen Ableitungen existieren.

**Lehre:** Dieses Beispiel zeigt eindrücklich, *warum* Satz 1.64 die Stetigkeit der partiellen Ableitungen fordert: Hier sind die partiellen Ableitungen (für $x,y\neq0$: $\partial_xf = \tfrac13x^{-2/3}y^{1/3}$) bei $(0,0)$ **unstetig** (sie divergieren, wenn man sich z.B. entlang $y=x$ nähert) — genau die Voraussetzung von Satz 1.64 ist verletzt.

<a id="vergleichstabelle-differenzierbarkeitsbegriffe-im-mathbbrn"></a>
## Vergleichstabelle: Differenzierbarkeitsbegriffe im $\mathbb{R}^n$

| Begriff | Definition | Impliziert | Wird impliziert von |
|---|---|---|---|
| **Partielle Differenzierbarkeit** | Alle $\partial f/\partial x_i$ existieren | — | Fréchet-Differenzierbarkeit |
| **Richtungsdifferenzierbarkeit** | $D_vf(x)$ existiert für alle $v$ | partielle Diffbarkeit ($v=e_i$) | Fréchet-Differenzierbarkeit |
| **Fréchet-Differenzierbarkeit** | $\exists$ lineare Approximation im Sinne von Def. 1.37 | Stetigkeit, Richtungsdiffbarkeit, partielle Diffbarkeit | stetige partielle Diffbarkeit |
| **Stetige (partielle) Differenzierbarkeit** ($C^1$) | Partielle Ableitungen existieren und sind stetig | Fréchet-Differenzierbarkeit (Satz 1.64) | — |

> **Merksatz für die Klausur:** $C^1 \Rightarrow$ Fréchet-diffbar $\Rightarrow$ partiell diffbar. Keiner dieser Pfeile lässt sich umkehren — für jeden gibt es Gegenbeispiele (das obige Beispiel zeigt, dass "partiell diffbar" $\not\Rightarrow$ "Fréchet-diffbar").

<a id="beispiele-13"></a>
## Beispiele

**Beispiel 1 (leicht):** Berechnen Sie die Jacobi-Matrix von $f(x,y)=(x^2y, \sin(xy))$:
$$
Df(x,y) = \begin{pmatrix} 2xy & x^2 \\ y\cos(xy) & x\cos(xy)\end{pmatrix}.
$$

**Beispiel 2 (mittel):** Zeigen Sie, dass $f(x,y)=\sqrt{|xy|}$ bei $(0,0)$ partiell differenzierbar, aber nicht Fréchet-differenzierbar ist (analoge Rechnung zum obigen Standardbeispiel — Übung).

**Beispiel 3 (schwer):** Konstruieren Sie eine Funktion, die in *jeder* Richtung differenzierbar ist (alle Richtungsableitungen existieren), aber trotzdem nicht Fréchet-differenzierbar ist. *(Hinweis: $f(x,y)=\frac{x^2y}{x^4+y^2}$ für $(x,y)\neq(0,0)$, $f(0,0)=0$ — alle Richtungsableitungen bei $(0,0)$ existieren und sind $0$, aber $f$ ist nicht einmal stetig bei $(0,0)$, da $f(x,x^2)=1/2$ für alle $x\neq0$.)*

<a id="typische-klausuraufgaben-14"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Erkennungsmerkmal | Strategie |
|---|---|---|
| "Berechnen Sie die Jacobi-Matrix" | Konkrete Funktion $\mathbb{R}^n\to\mathbb{R}^m$ | Partielle Ableitungen zeilenweise berechnen |
| "Ist $f$ bei $(0,0)$ differenzierbar?" | Stückweise Definition, oft mit Wurzeln/Brüchen bei $(0,0)$ | Partielle Ableitungen bei $(0,0)$ direkt über Grenzwert berechnen, dann eine *diagonale* Richtungsableitung prüfen und mit der Linearitätsvorhersage vergleichen |
| "Zeigen Sie $f\in C^1$" | Funktion mit erkennbar stetigen partiellen Ableitungen | Partielle Ableitungen berechnen, Stetigkeit (meist offensichtlich als Verkettung stetiger Funktionen) feststellen, Satz 1.64 zitieren |

<a id="typische-fehler-14"></a>
## Typische Fehler

1. **Aus Existenz der partiellen Ableitungen auf Differenzierbarkeit schließen** — der häufigste Fehler dieses Kapitels überhaupt.
2. **Bei der Differenzierbarkeitsprüfung nur entlang der Achsen testen**, statt eine diagonale oder allgemeine Richtung zu prüfen.
3. **Jacobi-Matrix transponiert aufschreiben** (Zeilen/Spalten vertauschen — Konvention: Zeile $j$ = Komponente $f_j$, Spalte $i$ = Variable $x_i$).

<a id="verbindungen-15"></a>
## Verbindungen

- Satz 1.64 ist die praktische Arbeitsgrundlage für **alle** folgenden expliziten Rechnungen im $\mathbb{R}^n$ (Extrema, Lagrange, Transformationssatz).
- Die partiellen Ableitungen 2. Ordnung (Kapitel 5, hier spezialisiert) liefern die **Hesse-Matrix**, das zentrale Werkzeug des nächsten Kapitels.
- Das Gegenbeispiel $(xy)^{1/3}$ ist eine beliebte Klausuraufgabe zur Illustration von Satz 1.64 und sollte auswendig beherrscht werden.

---

<a id="kapitel-8-extrema-frei-und-mit-nebenbedingungen"></a>
# Kapitel 8: Extrema — frei und mit Nebenbedingungen

<a id="motivation-16"></a>
## Motivation

**Welches Problem lösen wir?**

Dieses Kapitel ist der eigentliche **Anwendungshöhepunkt** der bisherigen Theorie: Wie findet man Maxima und Minima einer Funktion? Aus der Schule kennen Sie das Vorgehen im Eindimensionalen: $f'(x)=0$ finden, dann $f''(x)$ auf Vorzeichen prüfen. Wir verallgemeinern dies zunächst auf $f:\mathbb{R}^n\to\mathbb{R}$ (Gradient $=0$, Hesse-Matrix auf Definitheit prüfen), und dann auf den ungleich schwierigeren Fall von **Extrema unter Nebenbedingungen** — z.B. "Finde das Maximum von $f$ auf der Einheitssphäre" — wofür der **Satz über implizite Funktionen** (Kapitel 4!) unverzichtbar wird.

**Warum ist Nebenbedingungen-Optimierung so viel schwieriger?** Ohne Nebenbedingung ist der zulässige Bereich (ganz $\mathbb{R}^n$) ein Vektorraum — man kann in jede Richtung gehen. Mit einer Nebenbedingung $\phi(x)=0$ ist die zulässige Menge im Allgemeinen **kein Vektorraum mehr** (z.B. ist eine Kugeloberfläche kein Vektorraum), sondern eine gekrümmte Fläche — eine **Mannigfaltigkeit**. Das gesamte Maschinenwerk der Mannigfaltigkeitstheorie (Tangentialräume, Satz über implizite Funktionen) wird gebraucht, um überhaupt zu definieren, was "die zulässigen Richtungen" an einem Punkt der Fläche sind.

<a id="intuition-16"></a>
## Intuition

**Kritische Punkte (frei):** Am Gipfel eines Berges, im tiefsten Punkt eines Tals oder an einem Sattelpunkt zeigt der Gradient (die Richtung des steilsten Anstiegs) in **keine** Richtung — er verschwindet. Das ist die notwendige Bedingung $\nabla f(x)=0$. Um zwischen Gipfel, Tal und Sattel zu unterscheiden, betrachtet man die **Krümmung** (Hesse-Matrix): Krümmt sich die Landschaft in *jeder* Richtung nach unten (negativ definite Hesse-Matrix) — Maximum. In *jeder* Richtung nach oben (positiv definit) — Minimum. In einigen Richtungen nach oben, in anderen nach unten (indefinit) — Sattelpunkt.

**Lagrange-Multiplikatoren:** Stellen Sie sich vor, Sie stehen auf einer Bergkette (der Nebenbedingungsfläche) und suchen den höchsten Punkt der Kette (nicht den höchsten Punkt der ganzen Landschaft!). An diesem Punkt zeigt der Gradient von $f$ (die Richtung, in der es *insgesamt* am steilsten bergauf geht) **senkrecht zur Bergkette** — sonst könnte man ja noch etwas entlang der Kette weiterlaufen und höher kommen. "Senkrecht zur Bergkette" bedeutet: $\nabla f(x)$ ist parallel zu $\nabla\phi(x)$ (dem Gradienten der Nebenbedingung, der ja definitionsgemäß senkrecht auf der Fläche $\phi=0$ steht). Genau das codiert die Lagrange-Bedingung $\nabla f = \lambda \nabla\phi$.

<a id="formale-definitionen-16"></a>
## Formale Definitionen

<a id="definition-167-extrema"></a>
### Definition 1.67 (Extrema)

Sei $f: X\to\mathbb{R}$, $A\subseteq X$. $x_0\in A$ heißt **absolutes Minimum** (bzw. Maximum) von $f$ auf $A$, falls $f(x_0)\leq f(x)$ (bzw. $\ge$) für alle $x\in A$. $x_0$ heißt **relatives (lokales) Minimum**, falls eine offene Umgebung $U$ von $x_0$ existiert mit $f(x_0)\le f(x)$ für alle $x\in U\cap A$ (analog Maximum). Ein relatives Extremum heißt **strikt**, falls die Ungleichung für $x\neq x_0$ strikt ist.

<a id="definition-169-kritischer-punkt"></a>
### Definition 1.69 (Kritischer Punkt)

$X$ Banachraum, $f:X\to\mathbb{R}$. $x\in X$ heißt **kritischer Punkt**, falls $Df(x)=0$.

<a id="definition-gradient"></a>
### Definition (Gradient)

Für $f:\mathbb{R}^n\to\mathbb{R}$ differenzierbar bei $x$ ist $Df(x) \in L(\mathbb{R}^n,\mathbb{R}) = (\mathbb{R}^n)^*$. Der **Gradient** $\nabla f(x) \in \mathbb{R}^n$ ist der (via Standard-Skalarprodukt) zu $Df(x)$ korrespondierende Vektor:
$$
\nabla f(x) := \left(\frac{\partial f}{\partial x_1}(x),\dots,\frac{\partial f}{\partial x_n}(x)\right), \qquad Df(x)[h] = \langle \nabla f(x), h\rangle.
$$

<a id="definition-hesse-matrix"></a>
### Definition (Hesse-Matrix)

Für $f\in C^2(\mathbb{R}^n,\mathbb{R})$ ist die **Hesse-Matrix** bei $x$
$$
H(x) := \left(\frac{\partial^2f}{\partial x_i\partial x_j}(x)\right)_{i,j=1,\dots,n} \qquad \text{(symmetrisch nach Satz von Schwarz, Lemma 1.65).}
$$

<a id="definition-171-definitheit"></a>
### Definition 1.71 (Definitheit)

Sei $X$ Banachraum, $M \in \tilde L^2(X,\mathbb{R})$ eine (stetige) Bilinearform. $M$ heißt

$$
\begin{array}{ll}
\textbf{positiv definit} & : \forall x\neq 0: M(x,x)>0\\
\textbf{negativ definit} & : \forall x\neq 0: M(x,x)<0\\
\textbf{positiv semidefinit} & : \forall x: M(x,x)\geq0\\
\textbf{negativ semidefinit} & : \forall x: M(x,x)\leq0\\
\textbf{indefinit} & : \text{weder semidefinit positiv noch negativ}
\end{array}
$$

Im $\mathbb{R}^n$: $M$ (repräsentiert durch symmetrische Matrix) ist positiv definit $\iff \sum_{i,j}M_{ij}x_ix_j>0$ für alle $x\neq0$, äquivalent (Hauptminorenkriterium, nicht in der Mitschrift, aber Standardstoff): alle führenden Hauptminoren $>0$.

<a id="definition-173-mannigfaltigkeit"></a>
### Definition 1.73 (Mannigfaltigkeit)

Sei $1\leq r\leq n$, $p\geq 1$. Eine nicht-leere Menge $M\subseteq\mathbb{R}^n$ heißt **Mannigfaltigkeit der Dimension $r$ und Klasse $C^p$**, wenn zu jedem $x_0\in M$ eine offene Umgebung $U\subseteq\mathbb{R}^n$ von $x_0$ und eine Funktion $\phi\in C^p(U,\mathbb{R}^{n-r})$ existieren mit

$$
\text{(i)} \quad M\cap U = \{x\in U: \phi(x)=0\}, \qquad \text{(ii)} \quad \forall y\in M\cap U:\ \mathrm{rang}(D\phi(y)) = n-r.
$$

**Intuition:** $M$ "sieht lokal aus wie der Graph einer $C^p$-Funktion $\mathbb{R}^r\to\mathbb{R}^{n-r}$" — die volle Rangbedingung (ii) stellt sicher, dass die Nebenbedingung $\phi=0$ "nicht entartet" ist, sodass der Satz über implizite Funktionen anwendbar wird.

<a id="definition-174-tangentialvektor-tangentialraum"></a>
### Definition 1.74 (Tangentialvektor, Tangentialraum)

Sei $M\subseteq\mathbb{R}^n$ Mannigfaltigkeit, $x_0\in M$. $t\in\mathbb{R}^n$ heißt **Tangentialvektor** an $M$ bei $x_0$, falls $\delta>0$ und $\gamma\in C^1((-\delta,\delta),M)$ existieren mit $\gamma(0)=x_0$, $\gamma'(0)=t$. Die Menge aller Tangentialvektoren bei $x_0$ heißt **Tangentialraum** $T_{x_0}M$.

<a id="sätze-12"></a>
## Sätze

<a id="satz-170-notwendige-bedingung-erster-ordnung"></a>
### Satz 1.70 (Notwendige Bedingung erster Ordnung)

**Aussage:** Sei $X$ Banachraum, $f:X\to\mathbb{R}$ differenzierbar. Nimmt $f$ bei $x\in X$ ein relatives Extremum an, so gilt $Df(x)=0$.

**Beweis** *(Beweisstil: Reduktion auf den eindimensionalen Fall via Hilfsfunktion)*

Sei $x$ relatives Extremum, o.B.d.A. Minimum. Sei $v\in X$ beliebig, definiere $\psi(t):=f(x+tv)$. Dann hat $\psi$ bei $t=0$ ein relatives Minimum (in $\mathbb{R}$), also $\psi_-'(0)\le0$ und $\psi_+'(0)\ge0$ (einseitige Ableitungen, aus der Definition des Minimums: $\psi(t)-\psi(0)\ge 0$ nahe $0$). Da $\psi$ differenzierbar ist (Kettenregel), gilt $\psi_-'(0)=\psi_+'(0)=\psi'(0)$, also $\psi'(0)=0$. Da $\psi'(0)=Df(x)[v]$ (Kettenregel), folgt $Df(x)[v]=0$. Da $v$ beliebig war, $Df(x)=0$. $\blacksquare$

**Bedeutung:** Notwendig, aber **nicht** hinreichend — kritische Punkte sind nur *Kandidaten* für Extrema (Sattelpunkte sind ebenfalls kritisch).

<a id="satz-172-hinreichende-bedingung-zweiter-ordnung"></a>
### Satz 1.72 (Hinreichende Bedingung zweiter Ordnung)

**Aussage:** Sei $f:\mathbb{R}^n\to\mathbb{R}$ in einer Umgebung von $x$ zweimal stetig differenzierbar, $x$ kritischer Punkt ($\nabla f(x)=0$).

(i) Nimmt $f$ bei $x$ ein relatives Maximum an, so ist $H(x)$ negativ semidefinit.
(ii) Ist $H(x)$ positiv definit, so hat $f$ bei $x$ ein **striktes** relatives Minimum. (Analog für negativ definit / Maximum.)

**Wichtig:** (i) und (ii) sind **nicht** Umkehrungen voneinander — semidefinit (i) ist notwendig, definit (ii) ist hinreichend. Ist $H(x)$ **indefinit**, liegt garantiert **kein** Extremum vor (Sattelpunkt). Ist $H(x)$ nur semidefinit (aber nicht definit), ist mit den Mitteln 2. Ordnung **keine Entscheidung** möglich — höhere Ordnung nötig.

**Beweis von (ii)** *(Beweisstil: direkter Beweis via Taylorformel 2. Ordnung und Stetigkeitsargument)*

Da $H$ stetig ist und $H(x)$ positiv definit ist, existiert (Stetigkeitsargument, kompakte Einheitssphäre) $\theta_0>0$, sodass $H(x+\theta y)$ für $\|y\|=1$, $\theta<\theta_0$ ebenfalls positiv definit bleibt (die kleinste Eigenwert-Funktion ist stetig und bei $\theta=0$ positiv). Nach der Taylorformel (Korollar 1.66) mit Restglied gilt für $\|h\|$ klein genug:
$$
f(x+h)-f(x) = \underbrace{Df(x)[h]}_{=0} + \frac12\sum_{i,j}H(x+sh)_{ij}h_ih_j \qquad \text{für ein } s\in(0,1)
$$
(Lagrange-Restglied, angewendet auf die Hilfsfunktion $t\mapsto f(x+th)$). Da $H(x+sh)$ (für $\|h\|$ klein genug, sodass $s\|h\|<\theta_0$) positiv definit ist, gilt
$$
\sum_{i,j}H(x+sh)_{ij}h_ih_j > 0 \qquad \text{für } h\neq0,
$$
also $f(x+h)>f(x)$ für alle $h\neq0$ mit $\|h\|$ hinreichend klein — striktes relatives Minimum. $\blacksquare$

**Beweis von (i)** (Kontraposition/direkt): Wäre $H(x)$ nicht negativ semidefinit, existiert $y$ mit $H(x)y\cdot y>0$. Aus Stetigkeit folgt, dass $H(x+\theta y)y\cdot y>0$ für kleine $\theta$, was via Taylorformel $f(x+\theta y)-f(x)>0$ für kleine $\theta>0$ liefert — Widerspruch zum angenommenen relativen Maximum bei $x$. $\blacksquare$

<a id="satz-178-lagrange-multiplikatorenregel"></a>
### Satz 1.78 (Lagrange-Multiplikatorenregel)

**Aussage:** Sei $f\in C^1(\mathbb{R}^n,\mathbb{R})$, $M\subseteq\mathbb{R}^n$ eine $C^1$-Mannigfaltigkeit der Dimension $r$, die in einer Umgebung von $x_0\in M$ durch $\phi(x_0)=0$ beschrieben wird ($\phi:\mathbb{R}^n\to\mathbb{R}^{n-r}$, $\mathrm{rang}(D\phi)=n-r$). Nimmt $f$ bei $x_0\in M$ ein relatives Extremum der eingeschränkten Funktion $f|_M: M\to\mathbb{R}$ an, so existiert $\lambda \in \mathbb{R}^{n-r}$ (**Lagrange-Multiplikatoren**), sodass $x_0$ kritischer Punkt der Funktion
$$
f + \sum_{k=1}^{n-r}\lambda_k\phi_k
$$
ist, d.h. äquivalent:
$$
\nabla f(x_0) = \sum_{k=1}^{n-r}\lambda_k \nabla\phi_k(x_0).
$$

**Voraussetzungen — worauf besonders zu achten ist:**

| Voraussetzung | Konsequenz bei Verletzung |
|---|---|
| $f, \phi \in C^1$ | Ohne dies keine wohldefinierten Gradienten |
| $\mathrm{rang}(D\phi(x_0)) = n-r$ (voller Rang) | "Regularitätsbedingung" — ohne sie ist $x_0$ evtl. gar nicht auf einer Mannigfaltigkeit, oder die Lagrange-Bedingung liefert falsche/keine Aussage |

**Bedeutung:** Reduziert ein Optimierungsproblem mit Nebenbedingungen auf ein System algebraischer Gleichungen (Gradientengleichung + Nebenbedingung), das explizit lösbar ist.

**Beweis** *(Beweisstil: Reduktion auf freie Extrema via Kurven im Tangentialraum, dann lineare Algebra über Dimensionen)*

**Schritt 1:** Sei $t\in T_{x_0}M$ ein beliebiger Tangentialvektor, $\gamma:(-\delta,\delta)\to M$ mit $\gamma(0)=x_0,\gamma'(0)=t$. Definiere $v(s):=f(\gamma(s))$. Da $f|_M$ bei $x_0$ ein relatives Extremum hat, hat auch $v$ bei $s=0$ eines; nach Satz 1.70 (angewendet in $\mathbb{R}$) gilt $v'(0)=0$. Mit Kettenregel: $v'(0)=Df(x_0)[\gamma'(0)]=Df(x_0)[t] = \langle\nabla f(x_0),t\rangle$. Da $t$ beliebiger Tangentialvektor war:
$$
\nabla f(x_0) \perp T_{x_0}M.
$$

**Schritt 2 (Tangentialraum = Kern von $D\phi(x_0)$):** Nach Lemma 1.75/1.76 (siehe unten) gilt $T_{x_0}M = \ker(D\phi(x_0))$.

**Schritt 3 (Dimensionsargument):** Die Gradienten $\nabla\phi_1(x_0),\dots,\nabla\phi_{n-r}(x_0)$ sind linear unabhängig (da $D\phi(x_0)$ vollen Rang $n-r$ hat — die Zeilen der Jacobi-Matrix, welche gerade die transponierten Gradienten der $\phi_k$ sind, sind linear unabhängig) und spannen (als Zeilenraum von $D\phi(x_0)$) genau das **orthogonale Komplement** von $\ker(D\phi(x_0))=T_{x_0}M$ auf (Standardfakt der linearen Algebra: Zeilenraum $\perp$ Kern). Da $\nabla f(x_0) \perp T_{x_0}M$ (Schritt 1) und $\{\nabla\phi_k(x_0)\}$ eine Basis von $(T_{x_0}M)^\perp$ bilden, lässt sich $\nabla f(x_0)$ als Linearkombination der $\nabla\phi_k(x_0)$ schreiben:
$$
\nabla f(x_0) = \sum_{k=1}^{n-r}\lambda_k\nabla\phi_k(x_0). \qquad \blacksquare
$$

<a id="lemma-175176-tangentialraum-kern-der-ableitung-der-nebenbedingung"></a>
### Lemma 1.75/1.76 (Tangentialraum = Kern der Ableitung der Nebenbedingung)

**Aussage:** Ist $M$ bei $x_0$ durch $\phi(x_0)=0$ (mit vollem Rang) beschrieben, so gilt $T_{x_0}M = \ker(D\phi(x_0)) = \{t\in\mathbb{R}^n : D\phi(x_0)[t]=0\}$.

**Beweisidee, "$\subseteq$" (Lemma 1.75):** Ist $t$ Tangentialvektor via Kurve $\gamma$ mit $\gamma(s)\in M$ für alle $s$, so gilt $\phi(\gamma(s))=0$ für alle $s$; Ableiten nach $s$ bei $s=0$ (Kettenregel) liefert $D\phi(x_0)[\gamma'(0)]=D\phi(x_0)[t]=0$, also $t\in\ker(D\phi(x_0))$.

**Beweisidee, "$\supseteq$" (Lemma 1.76, technisch aufwendiger):** Sei $t\in\ker(D\phi(x_0))$. Man konstruiert explizit eine Kurve $\gamma(s):=(\hat x_0+s\hat t,\, g(\hat x_0+s\hat t))$ mittels der durch den Satz über implizite Funktionen (Satz 1.45!) gelieferten lokalen Graphendarstellung $g$ von $M$ und zeigt $\gamma'(0)=t$ via Kettenregel und der Ableitungsformel für $g$. **Dies ist die Stelle, an der der Satz über implizite Funktionen aus Kapitel 4 direkt in die Extremwerttheorie eingeht** — ohne ihn ließe sich der Tangentialraum nicht mit dem Kern von $D\phi$ identifizieren.

<a id="beispiele-14"></a>
## Beispiele

**Beispiel 1 (leicht, frei):** $f(x,y)=x^2+y^2-2x$. $\nabla f = (2x-2,2y)=0 \Rightarrow (x,y)=(1,0)$. Hesse-Matrix $H=\begin{pmatrix}2&0\\0&2\end{pmatrix}$, positiv definit $\Rightarrow$ striktes Minimum bei $(1,0)$.

**Beispiel 2 (mittel, Sattelpunkt):** $f(x,y)=x^2-y^2$. $\nabla f=(2x,-2y)=0\Rightarrow(0,0)$. $H=\begin{pmatrix}2&0\\0&-2\end{pmatrix}$, indefinit $\Rightarrow$ Sattelpunkt (kein Extremum).

**Beispiel 3 (schwer, Lagrange — vollständig durchgerechnet, aus der Vorlesung):** Finden Sie die Extrema von $f(x_1,x_2)=x_1^2x_2^2$ auf $M=S^1=\{x_1^2+x_2^2=1\}$.

*Aufstellen:* $\phi(x_1,x_2)=x_1^2+x_2^2-1$. Lagrange-Bedingung $\nabla f = \lambda\nabla\phi$:
$$
\begin{pmatrix}2x_1x_2^2\\2x_1^2x_2\end{pmatrix} = \lambda\begin{pmatrix}2x_1\\2x_2\end{pmatrix}.
$$

*Fall $\lambda\neq0$:* Aus $x_1=0$ folgt (aus $\phi=0$) $x_2=\pm1$, aber dann löst dies die erste Gleichung ($2\cdot0\cdot x_2^2=0=\lambda\cdot0$, konsistent) — also ist $(0,\pm1)$ eine Lösung, aber Prüfung zeigt: mit $x_1=x_2^2=1$ als Alternative, $x_1^2=x_2^2=\tfrac12$ (aus beiden Gleichungen $x_2^2=\lambda=x_1^2$, kombiniert mit $\phi=0$): dies liefert die **vier kritischen Punkte** $(\pm1/\sqrt2,\pm1/\sqrt2)$.

*Fall $\lambda=0$:* $x_1=0$ oder $x_2=0$; kombiniert mit $x_1^2+x_2^2=1$ ergibt die **vier kritischen Punkte** $(\pm1,0), (0,\pm1)$.

*Auswertung:* $f(\pm1/\sqrt2,\pm1/\sqrt2)=1/4$ (Maximum auf $S^1$); $f(\pm1,0)=f(0,\pm1)=0$ (Minimum auf $S^1$).

<a id="gegenbeispiele-14"></a>
## Gegenbeispiele

- **Kritischer Punkt ohne Extremum:** $f(x,y)=x^2-y^2$ bei $(0,0)$ (siehe Beispiel 2) — notwendige Bedingung erfüllt, aber kein Extremum.
- **Semidefinite Hesse-Matrix ohne Entscheidbarkeit:** $f(x,y)=x^2+y^4$ hat bei $(0,0)$ $H=\begin{pmatrix}2&0\\0&0\end{pmatrix}$ (positiv semidefinit, aber nicht definit) — trotzdem liegt ein (striktes) Minimum vor. Vergleichen Sie mit $f(x,y)=x^2-y^4$: gleiche Hesse-Matrix bei $(0,0)$, aber **kein** Minimum (Sattelpunkt, da $f(0,y)=-y^4<0$ für $y\neq0$). Dies zeigt: **Bei semidefiniter (nicht definiter) Hesse-Matrix ist mit Mitteln 2. Ordnung keine Aussage möglich** — entscheidend ist hier die Fallunterscheidung.
- **Lagrange ohne Regularitätsbedingung:** Ist $\mathrm{rang}(D\phi(x_0))<n-r$ (z.B. bei einem singulären Punkt der Nebenbedingungsmenge, wie der Spitze von $\phi(x,y)=y^2-x^3$ bei $(0,0)$), kann die Lagrange-Bedingung scheitern oder falsche Kandidaten liefern — die Voraussetzung des vollen Rangs ist essentiell.

<a id="typische-klausuraufgaben-15"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Erkennungsmerkmal | Strategie |
|---|---|---|
| "Finden und klassifizieren Sie alle kritischen Punkte von $f$" | Konkrete Funktion $\mathbb{R}^n\to\mathbb{R}$, keine Nebenbedingung | $\nabla f=0$ lösen, Hesse-Matrix bei jedem kritischen Punkt auf Definitheit prüfen (Eigenwerte oder Hauptminorenkriterium) |
| "Finden Sie Extrema von $f$ unter der Nebenbedingung $\phi=0$" | Explizite Nebenbedingung, oft Kreis/Sphäre/Ellipse | Lagrange-System $\nabla f=\lambda\nabla\phi$ zusammen mit $\phi=0$ aufstellen und lösen; Fallunterscheidung nach $\lambda$ |
| "Extrema auf kompakter Menge mit Rand" | Abgeschlossene, beschränkte Menge, z.B. Einheitskreisscheibe | Innere kritische Punkte UND Randextrema (via Lagrange auf dem Rand) separat bestimmen, dann Werte vergleichen (Extremwertsatz garantiert Existenz) |
| "Zeigen Sie, dass $M$ eine Mannigfaltigkeit ist" | Explizite Gleichung $\phi(x)=0$ | Rang von $D\phi$ auf ganz $M$ prüfen |

<a id="typische-fehler-15"></a>
## Typische Fehler

1. **Nur notwendige Bedingung prüfen und vergessen, die Hesse-Matrix zu klassifizieren** (kritischer Punkt $\neq$ Extremum).
2. **Bei semidefiniter (nicht definiter) Hesse-Matrix fälschlich eine Entscheidung treffen** — hier ist eine gesonderte Untersuchung nötig (siehe Gegenbeispiel oben).
3. **Randbedingung bei Extrema auf kompakten Mengen mit Rand vergessen** (Extremwertsatz garantiert Existenz, aber Kandidaten müssen sowohl im Inneren als auch am Rand gesucht werden).
4. **Vorzeichen des Lagrange-Multiplikators überinterpretieren** — $\lambda$ selbst hat i.A. keine unmittelbare geometrische Bedeutung als Vorzeichen des Extremtyps; die Fallunterscheidung erfolgt über Auswertung von $f$ an allen Kandidaten.
5. **Regularitätsbedingung ($\mathrm{rang}(D\phi)=n-r$) nicht prüfen**, bevor Lagrange angewendet wird.

<a id="verbindungen-16"></a>
## Verbindungen

- Satz 1.68 (**Extremwertsatz**, hier nicht erneut hergeleitet, folgt direkt aus Lemma 1.14 + Kompaktheit, Kapitel 1/2): Eine stetige Funktion auf einer kompakten Menge nimmt Maximum und Minimum an — dies garantiert, dass die Suche nach kritischen Punkten überhaupt "Erfolg haben muss".
- Der Satz über implizite Funktionen (Kapitel 4) ist über Lemma 1.76 direkt in den Beweis der Lagrange-Regel eingebettet.
- Der Satz von Schwarz (Kapitel 5) garantiert die Symmetrie der Hesse-Matrix, die für die Definitheitsklassifikation vorausgesetzt wird.
- Die hier entwickelte Theorie der Mannigfaltigkeiten wird in Kapitel Kurvenintegrale (Parametrisierung von Kurven als 1-dimensionale Mannigfaltigkeiten) und implizit im Transformationssatz (Integration) wiederverwendet.

<a id="zusammenfassung-kapitel-7-8"></a>
## Zusammenfassung Kapitel 7 & 8

- Partielle Ableitungen sind Richtungsableitungen entlang der Koordinatenachsen; ihre Existenz allein garantiert **nicht** Fréchet-Differenzierbarkeit (Gegenbeispiel $(xy)^{1/3}$) — dafür braucht man **stetige** partielle Ableitungen (Satz 1.64).
- Notwendige Bedingung für ein relatives Extremum: $\nabla f(x)=0$ (Satz 1.70). Hinreichend (bei kritischem Punkt): Definitheit der Hesse-Matrix (Satz 1.72) — positiv definit $\Rightarrow$ striktes Minimum, negativ definit $\Rightarrow$ striktes Maximum, indefinit $\Rightarrow$ Sattelpunkt, semidefinit $\Rightarrow$ keine Entscheidung möglich.
- Eine **Mannigfaltigkeit** ist lokal als Nullstellenmenge einer $C^p$-Funktion mit vollem Rang der Ableitung beschrieben; ihr **Tangentialraum** ist der Kern der Ableitung der Nebenbedingungsfunktion (Lemma 1.75/1.76, beruhend auf dem Satz über implizite Funktionen).
- Die **Lagrange-Multiplikatorenregel** (Satz 1.78) reduziert Extrema unter Nebenbedingungen auf das algebraische System $\nabla f=\sum\lambda_k\nabla\phi_k$, $\phi=0$.

---

*Ende Teil 4. Fortsetzung folgt mit Kapitel 9 (Globale Approximation, Weierstraßscher Approximationssatz) und Kapitel 10 (Riemann-Integral, Fubini, Transformationssatz) auf Anfrage.*



---

<a id="analysis-auf-allgemeinen-linearen-räumen-teil-5"></a>
# Analysis auf allgemeinen linearen Räumen — Teil 5

*Fortsetzung von Teil 1–4. Dieses Dokument setzt Topologie, Metrik, Banachräume, Differentialrechnung, Taylor, Hilberträume und Extremwerttheorie als bekannt voraus.*

---

<a id="kapitel-9-globale-approximation-von-funktionen"></a>
# Kapitel 9: Globale Approximation von Funktionen

<a id="motivation-17"></a>
## Motivation

**Welches Problem lösen wir?**

Bisher haben wir Funktionen *lokal* approximiert (Taylorformel: Approximation nahe einem Punkt $x$). Jetzt fragen wir: Kann man eine beliebige stetige Funktion *global*, auf ihrem gesamten Definitionsbereich, durch besonders "schöne" Funktionen (z.B. Polynome oder $C^\infty$-Funktionen) beliebig gut approximieren? Diese Frage ist praktisch enorm wichtig: Polynome sind einfach zu rechnen (Addition, Multiplikation), $C^\infty$-Funktionen sind beliebig oft differenzierbar — wenn man weiß, dass man jede stetige Funktion durch solche approximieren kann, lassen sich viele Aussagen zunächst für die "schönen" Funktionen beweisen und dann per Approximationsargument auf beliebige stetige Funktionen übertragen.

**Historischer Kontext.** Karl Weierstraß bewies 1885, dass jede stetige Funktion auf einem kompakten Intervall gleichmäßiger Grenzwert von Polynomen ist — ein zunächst überraschendes Resultat, da stetige Funktionen (z.B. die Weierstraß-Funktion, nirgends differenzierbar) sehr "wild" sein können, Polynome aber extrem "zahm" sind.

<a id="intuition-17"></a>
## Intuition

**Punktweise vs. gleichmäßige Konvergenz:** Der entscheidende Unterschied ist, *wie gleichmäßig* der Fehler der Approximation gegen null geht. Bei punktweiser Konvergenz darf die "Geschwindigkeit", mit der $f_n(x)\to f(x)$, von $x$ abhängen — bei gleichmäßiger Konvergenz muss ein und dieselbe Rate für *alle* $x$ gleichzeitig funktionieren. Das ist wie der Unterschied zwischen "jeder einzelne Läufer erreicht irgendwann das Ziel" und "es gibt eine gemeinsame Zeitschranke, ab der *alle* Läufer im Ziel sind".

**Dirac-Folgen und Faltung:** Die Grundidee zur Konstruktion glatter Approximationen ist die **Faltung**: Man "verschmiert" die Funktion $f$ mit einem immer schmaler werdenden "Glättungskern" $\delta_n$ (einer Familie von Funktionen, die sich zunehmend wie eine Dirac-Distribution — eine unendlich hohe, unendlich schmale Spitze mit Gesamtfläche 1 — verhalten). Das Ergebnis $f*\delta_n$ ist glatt (da $\delta_n$ glatt ist) und konvergiert gegen $f$ (da der "Verschmierungsbereich" immer kleiner wird).

**Physikalische Analogie:** Stellen Sie sich vor, Sie fotografieren $f$ mit einer zunehmend schärferen Kamera (kleinere "Unschärfekreise" $\delta_n$) — mit unendlich scharfer Kamera ($n\to\infty$) erhalten Sie exakt $f$ zurück, aber jedes einzelne Foto (endliches $n$) ist ein leicht "verschmiertes", dafür beliebig glattes Bild von $f$.

<a id="formale-definitionen-17"></a>
## Formale Definitionen

<a id="definition-180-punktweise-und-gleichmäßige-konvergenz"></a>
### Definition 1.80 (Punktweise und gleichmäßige Konvergenz)

Seien $(M,d_1), (N,d_2)$ metrische Räume, $D\subseteq M$, $f_n,f: D\to N$.

$$
f_n \to f \text{ \textbf{punktweise}} \quad :\iff \quad \forall x\in D:\ \lim_{n\to\infty} f_n(x)=f(x), \text{ d.h. } \forall x\in D\ \forall\varepsilon>0\ \exists n_0\ \forall n\geq n_0:\ d_2(f_n(x),f(x))<\varepsilon.
$$

$$
f_n \to f \text{ \textbf{gleichmäßig}} \quad :\iff \quad \forall\varepsilon>0\ \exists n_0\ \forall n\geq n_0\ \forall x\in D:\ d_2(f_n(x),f(x))<\varepsilon.
$$

> **Der entscheidende Quantorentausch:** Bei punktweiser Konvergenz darf $n_0$ von $x$ *und* $\varepsilon$ abhängen; bei gleichmäßiger Konvergenz hängt $n_0$ nur von $\varepsilon$ ab — dieselbe Schranke muss für **alle** $x\in D$ gleichzeitig funktionieren. Ist $N$ normierter Raum, ist gleichmäßige Konvergenz äquivalent zu $\lim_{n\to\infty}\|f_n-f\|_\infty=0$ mit der Supremumsnorm $\|g\|_\infty:=\sup_{x\in D}\|g(x)\|$.

<a id="definition-182183-kompakter-träger-faltung-dirac-folge"></a>
### Definition 1.82/1.83 (Kompakter Träger, Faltung, Dirac-Folge)

$f:\mathbb{R}\to\mathbb{R}$ hat **kompakten Träger**, falls ein kompaktes Intervall $K$ existiert mit $f(x)=0$ für $x\notin K$.

Für stetige $f,g:\mathbb{R}\to\mathbb{R}$, von denen mindestens eine kompakten Träger hat, heißt
$$
(f * g)(x) := \int_{\mathbb{R}} f(y)g(x-y)\,dy = \int_{\mathbb{R}} f(x-y)g(y)\,dy
$$
die **Faltung** von $f$ und $g$.

Eine Folge $(\delta_n)_{n}$ stetiger Funktionen $\delta_n: \mathbb{R}\to[0,\infty)$ heißt **Dirac-Folge**, falls:
$$
\text{(i)} \quad \forall n:\ \int_{\mathbb{R}}\delta_n(x)\,dx = 1, \qquad \text{(ii)} \quad \forall \varepsilon>0\ \forall r>0\ \exists n_0\ \forall n\geq n_0: \int_{|x|>r}\delta_n(x)\,dx < \varepsilon.
$$

**Intuition zu (ii):** Die "Masse" von $\delta_n$ konzentriert sich zunehmend um den Nullpunkt — außerhalb jeder festen Umgebung des Ursprungs geht das Integral über $\delta_n$ gegen null.

<a id="eigenschaften-15"></a>
## Eigenschaften

<a id="beispiele-für-dirac-folgen"></a>
### Beispiele für Dirac-Folgen

| Folge | Formel | Eigenschaft |
|---|---|---|
| **Gauß-Kerne** | $\delta_n(x) = \dfrac{1}{\sqrt{4\pi/n}}\exp(-nx^2/4)$ | $C^\infty$, glockenförmig |
| **Rechteck-Kerne** | $\delta_n(x) = n\cdot\mathbb{1}_{[0,1/n]}(x)$ | stetig-stückweise, kompakter Träger, aber nicht glatt |

Nur die erste Familie ist geeignet, um **glatte** Approximationen zu erzeugen (siehe Satz 1.85 unten) — dafür braucht man $\delta_n \in C^\infty$.

<a id="sätze-13"></a>
## Sätze

<a id="satz-181-gleichmäßiger-grenzwert-stetiger-funktionen-ist-stetig"></a>
### Satz 1.81 (Gleichmäßiger Grenzwert stetiger Funktionen ist stetig)

**Aussage:** Seien $M,N,D$ metrische Räume, $(f_n)_{n}$ Folge stetiger Funktionen $D\to N$, die **gleichmäßig** gegen $f$ konvergiert. Dann ist $f$ stetig.

**Bedeutung:** Bei punktweiser Konvergenz gilt dies **nicht** (Gegenbeispiel unten) — dies ist der Hauptgrund, warum gleichmäßige Konvergenz der "richtige" Konvergenzbegriff für die Vertauschung von Grenzwerten und Stetigkeit ist.

**Beweis** *(Beweisstil: klassisches $\varepsilon/3$-Argument, dreifache Dreiecksungleichung)*

Sei $\varepsilon>0$, $x\in D$. Wegen gleichmäßiger Konvergenz existiert $n_0$ mit $d_2(f_n(z),f(z))<\varepsilon/3$ für alle $n\geq n_0$, $z\in D$. Fixiere $n=n_0$. Da $f_{n_0}$ stetig bei $x$ ist, existiert $\delta>0$ mit $d_2(f_{n_0}(x),f_{n_0}(y))<\varepsilon/3$ für $d_1(x,y)<\delta$. Für solche $y$ gilt dann (Dreiecksungleichung, dreifach angewendet):
$$
d_2(f(x),f(y)) \leq d_2(f(x),f_{n_0}(x)) + d_2(f_{n_0}(x),f_{n_0}(y)) + d_2(f_{n_0}(y),f(y)) < \tfrac\varepsilon3+\tfrac\varepsilon3+\tfrac\varepsilon3 = \varepsilon.
$$
Also ist $f$ stetig bei $x$. $\blacksquare$

**Klassisches Gegenbeispiel bei nur punktweiser Konvergenz:** $f_n:[0,1]\to\mathbb{R}$, $f_n(x)=x^n$. Punktweiser Grenzwert:
$$
\lim_{n\to\infty} f_n(x) = \begin{cases} 0 & x\in[0,1) \\ 1 & x=1\end{cases}
$$
— **unstetig**, obwohl jedes $f_n$ stetig ist. Die Konvergenz ist hier **nicht** gleichmäßig: Für jedes $n$ existiert $x$ nahe $1$ mit $f_n(x)$ nahe $1$, sodass $\sup_x|f_n(x)-f(x)|$ nicht gegen $0$ geht (genauer: $=1$ für jedes $n$, da man $x$ stets nahe genug an 1 wählen kann).

<a id="lemma-184-konvolution-mit-dirac-folge-konvergiert-gegen-die-funktion"></a>
### Lemma 1.84 (Konvolution mit Dirac-Folge konvergiert gegen die Funktion)

**Aussage:** Sei $f:\mathbb{R}\to\mathbb{R}$ stetig und beschränkt, $(\delta_n)_n$ Dirac-Folge stetiger Funktionen, wobei $f$ oder alle $\delta_n$ kompakten Träger haben. Dann:

(i) $\forall x\in\mathbb{R}: \lim_{n\to\infty}(f*\delta_n)(x) = f(x)$ (**punktweise** Konvergenz).
(ii) Ist $f$ zusätzlich **gleichmäßig stetig**, so konvergiert $(f*\delta_n)$ **gleichmäßig** gegen $f$.

**Bedeutung:** Dies ist der technische Motor hinter dem Weierstraßschen Approximationssatz: Faltung mit einer geeigneten (glatten!) Dirac-Folge liefert glatte Approximationen einer beliebigen stetigen Funktion.

**Beweisidee** *(Beweisstil: direkte Abschätzung, Aufspaltung des Integrationsbereichs in "nah" und "fern" vom Ursprung)*

Man schreibt
$$
(f*\delta_n)(x) - f(x) = \int_{\mathbb{R}} [f(x-y)-f(x)]\,\delta_n(y)\,dy
$$
(unter Ausnutzung von $\int\delta_n=1$) und spaltet das Integral in $|y|<r$ (wo $f(x-y)\approx f(x)$ wegen Stetigkeit) und $|y|>r$ (wo $\delta_n$ wegen der Dirac-Eigenschaft (ii) verschwindend kleines Gewicht trägt) auf. Für $|y|<r$ (bei geeigneter Wahl von $r$, abhängig von der Stetigkeit von $f$ bei $x$) ist $|f(x-y)-f(x)|<\varepsilon$; für $|y|>r$ nutzt man die Beschränktheit von $f$ (Konstante $M$) und Eigenschaft (ii) der Dirac-Folge, um das Integral über diesen Bereich $<\varepsilon$ zu machen. Insgesamt folgt $|(f*\delta_n)(x)-f(x)| \le \varepsilon(1+2M)$ für $n$ groß genug. Ist $f$ gleichmäßig stetig, ist die Wahl von $r$ (und damit $n_0$) unabhängig von $x$ — das liefert die gleichmäßige Version (ii). $\blacksquare$

<a id="satz-185-weierstraßscher-approximationssatz"></a>
### Satz 1.85 (Weierstraßscher Approximationssatz)

**Aussage:** Seien $a,b\in\mathbb{R}$, $a<b$, $f:[a,b]\to\mathbb{R}$ stetig. Dann existiert eine Folge von Polynomen $(p_n)_n$, die **gleichmäßig** auf $[a,b]$ gegen $f$ konvergiert.

**Bedeutung:** Einer der wichtigsten Approximationssätze der Analysis — Polynome liegen "dicht" in $(C^0[a,b],\|\cdot\|_\infty)$. Dies rechtfertigt zahlreiche Beweistechniken, bei denen man eine Aussage zunächst für Polynome zeigt und dann approximativ auf stetige Funktionen überträgt.

**Beweis** *(Beweisstil: konstruktiver Beweis via Bernstein/Landau-Kernen, Reduktion auf Standardintervall)*

**Schritt 1 (Reduktion auf $[0,1]$ mit Randnullbedingung):** Man zeigt zunächst den Fall $a=0,b=1$, $f(0)=f(1)=0$ (allgemeiner Fall folgt anschließend durch affine Transformation des Intervalls und Abzug einer linearen Funktion, die die Randwerte korrigiert — siehe Schritt 3).

**Schritt 2 (Landau-Kerne):** Definiere für $n\in\mathbb{N}$ die **Landau-Kerne**
$$
L_n(x) := \frac{1}{c_n}(1-x^2)^n \cdot \mathbb{1}_{[-1,1]}(x), \qquad c_n := \int_{-1}^1 (1-x^2)^n\,dx \quad \text{(Normierungskonstante)}.
$$
Man zeigt (Übung, elementare Integralabschätzung), dass $(L_n)_n$ eine Dirac-Folge ist.

**Schritt 3 (Anwendung von Lemma 1.84):** Da $f$ auf dem Kompaktum $[0,1]$ stetig ist, ist $f$ dort gleichmäßig stetig (klassischer Satz aus Analysis 1 — folgt aus Kompaktheit + Stetigkeit, vgl. Lemma 1.27). Nach Lemma 1.84(ii) konvergiert $(f*L_n)_n$ gleichmäßig gegen $f$ auf $[0,1]$.

**Schritt 4 (Nachweis: $f*L_n$ ist tatsächlich ein Polynom):** Für $x\in[0,1]$:
$$
(f*L_n)(x) = \frac{1}{c_n}\int_{x-1}^{x+1} f(y)(1-(x-y)^2)^n\,\mathbb{1}_{[-1,1]}(x-y)\,dy = \frac1{c_n}\int_0^1 f(y)(1-(x-y)^2)^n\,dy
$$
(unter Ausnutzung von $f(y)=0$ außerhalb $[0,1]$, was die Trägerbedingung vereinfacht). Der Integrand $(1-(x-y)^2)^n$ ist, als Funktion von $x$ betrachtet, ein Polynom vom Grad $2n$ in $x$ (Ausmultiplizieren via Binomischem Lehrsatz); die Integration über $y$ (bei festem Polynomgrad in $x$) liefert wieder ein Polynom in $x$ vom Grad $\leq 2n$. Also ist $f*L_n$ ein Polynom.

**Schritt 5 (Rücktransformation für allgemeine $a,b$ und Randwerte):** Für allgemeines $f:[a,b]\to\mathbb{R}$ (ohne Randnullbedingung) definiert man zunächst die affine Reparametrisierung $T(x):=2(b-a)x + \tfrac14(3a-b)$ (bzw. eine geeignete lineare Transformation von $[0,1]$ nach $[a,b]$) sowie eine Hilfsfunktion
$$
s(x) := \begin{cases} f(a)\,x & x\in[0,\tfrac14]\\ f(T(x)) & x\in[\tfrac14,\tfrac34]\\ f(b)(1-x) & x\in[\tfrac34,1]\end{cases}
$$
die stetig ist, an den Rändern $0$ ist, und approximiert $s$ mit obigem Verfahren durch Polynome; Rücktransformation liefert die Approximation für $f$. $\blacksquare$

<a id="vergleichstabelle-punktweise-vs-gleichmäßige-konvergenz"></a>
## Vergleichstabelle: Punktweise vs. gleichmäßige Konvergenz

| Eigenschaft | Punktweise Konvergenz | Gleichmäßige Konvergenz |
|---|---|---|
| Stetigkeit des Grenzwerts | **nicht** garantiert | garantiert (Satz 1.81), falls alle $f_n$ stetig |
| Vertauschung mit Integration | i.A. nicht erlaubt | erlaubt (unter zusätzlichen milden Voraussetzungen) |
| Formale Definition | $n_0$ darf von $x$ abhängen | $n_0$ unabhängig von $x$ |
| Charakterisierung über Norm | — | $\|f_n-f\|_\infty \to 0$ |

<a id="beispiele-15"></a>
## Beispiele

**Beispiel 1 (leicht):** $f_n(x)=\sin(x)/n$ auf $\mathbb{R}$ konvergiert gleichmäßig gegen $0$, da $\|f_n\|_\infty = 1/n \to 0$ — unabhängig von $x$.

**Beispiel 2 (mittel):** $f_n(x) = nx e^{-nx^2}$ auf $[0,1]$: Punktweise gilt $f_n(x)\to 0$ für jedes feste $x$, aber $f_n(1/\sqrt n) = \sqrt n \cdot e^{-1} \to \infty$ — die Konvergenz ist **nicht** gleichmäßig (obwohl der punktweise Grenzwert hier sogar stetig ist! Dies zeigt: Stetigkeit des Grenzwerts ist notwendig, aber nicht hinreichend für gleichmäßige Konvergenz).

**Beispiel 3 (schwer, Anwendung):** Nutzen Sie den Weierstraßschen Approximationssatz, um zu zeigen: Ist $f:[0,1]\to\mathbb{R}$ stetig und gilt $\int_0^1 f(x)x^n\,dx=0$ für alle $n\in\mathbb{N}_0$, so ist $f\equiv0$. *(Beweisidee: Aus der Voraussetzung folgt $\int_0^1 f(x)p(x)\,dx=0$ für jedes Polynom $p$; approximiere $f$ selbst gleichmäßig durch Polynome $p_n\to f$, dann $\int f^2 = \lim\int f\cdot p_n = 0 \Rightarrow f\equiv 0$.)*

<a id="gegenbeispiele-15"></a>
## Gegenbeispiele

- **$f_n(x)=x^n$ auf $[0,1]$:** siehe oben — punktweise, aber nicht gleichmäßige Konvergenz; Grenzfunktion unstetig.
- **Rechteck-Kerne als Dirac-Folge, aber ungeeignet für glatte Approximation:** Obwohl $\delta_n(x)=n\cdot\mathbb{1}_{[0,1/n]}(x)$ eine gültige Dirac-Folge ist, ist $f*\delta_n$ i.A. **nicht** glatt (nur so glatt wie $f$ selbst) — für den Weierstraßschen Satz braucht man die zusätzliche Glattheit (bzw. Polynomeigenschaft) der Landau-Kerne.

<a id="typische-klausuraufgaben-16"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Erkennungsmerkmal | Strategie |
|---|---|---|
| "Konvergiert $(f_n)$ gleichmäßig?" | Konkrete Funktionenfolge | Punktweisen Grenzwert bestimmen, dann $\sup_x|f_n(x)-f(x)|$ explizit berechnen/abschätzen; typischer Kandidat für Gegenbeispiel: Maximum wandert mit $n$ |
| "Zeigen Sie, dass $(\delta_n)$ eine Dirac-Folge ist" | Explizite Formel für $\delta_n$ | Beide Axiome (Integral $=1$, Massenkonzentration) einzeln nachrechnen |
| "Nutzen Sie Weierstraß, um ... zu zeigen" | Dichtheitsargument gefragt | Approximierende Polynomfolge konstruieren/zitieren, Grenzübergang in der gewünschten Aussage durchführen |

<a id="typische-fehler-16"></a>
## Typische Fehler

1. **Punktweise Konvergenz mit gleichmäßiger verwechseln** — insbesondere beim "Beweisen" von Stetigkeit des Grenzwerts ohne Prüfung der Gleichmäßigkeit.
2. **Bei Dirac-Folgen die zweite Bedingung (Massenkonzentration) vergessen** — nur $\int\delta_n=1$ zu prüfen reicht nicht.
3. **Weierstraß mit Taylor verwechseln:** Taylor approximiert lokal (nahe einem Punkt) mit evtl. divergierendem Restglied fernab des Entwicklungspunkts; Weierstraß liefert eine **global gleichmäßige** Approximation, aber die approximierenden Polynome haben i.A. nichts mit der Taylorreihe von $f$ zu tun (und $f$ muss nicht einmal differenzierbar sein!).

<a id="verbindungen-17"></a>
## Verbindungen

- Satz 1.81 wird beim Aufbau der Riemann-Integration (nächstes Kapitel) implizit gebraucht, um Grenzübergänge unter dem Integral zu rechtfertigen.
- Der Weierstraßsche Approximationssatz motiviert später (außerhalb dieser Vorlesung) die Fourier-Analysis und die $L^p$-Theorie.
- Die Konstruktion via Faltung/Dirac-Folgen taucht in der Wahrscheinlichkeitstheorie (Zentraler Grenzwertsatz, Gauß-Kerne) und in der Signalverarbeitung wieder auf.

<a id="zusammenfassung-kapitel-9"></a>
## Zusammenfassung Kapitel 9

- **Gleichmäßige Konvergenz** ist strikt stärker als punktweise Konvergenz; nur sie garantiert, dass der Grenzwert stetiger Funktionen wieder stetig ist (Satz 1.81).
- Eine **Dirac-Folge** approximiert im Grenzwert das Verhalten der Delta-Distribution; **Faltung** mit einer Dirac-Folge glättet eine Funktion, während sie (unter gleichmäßiger Stetigkeit) gleichmäßig gegen die ursprüngliche Funktion konvergiert (Lemma 1.84).
- Der **Weierstraßsche Approximationssatz** (Satz 1.85) zeigt konstruktiv (via Landau-Kerne), dass jede stetige Funktion auf einem kompakten Intervall gleichmäßiger Grenzwert von Polynomen ist.

---

<a id="kapitel-10-integration-auf-mathbbrn"></a>
# Kapitel 10: Integration auf $\mathbb{R}^n$

<a id="motivation-18"></a>
## Motivation

**Welches Problem lösen wir?**

Aus Analysis 1 kennen Sie das Riemann-Integral für Funktionen einer Variablen — definiert über Ober- und Untersummen bezüglich Zerlegungen eines Intervalls. Wir verallgemeinern dies auf Funktionen mehrerer Variablen $f:\mathbb{R}^n\to\mathbb{R}$, wobei "Zerlegungen" jetzt Unterteilungen in Quader (statt Intervalle) sind. Dies liefert das mehrdimensionale Volumenintegral, das Volumina, Massen, Schwerpunkte etc. berechnet.

**Zwei zentrale technische Fragen dieses Kapitels:**
1. Wie berechnet man ein mehrdimensionales Integral praktisch? (**Satz von Fubini** — Reduktion auf iterierte eindimensionale Integrale.)
2. Wie verhält sich das Integral unter Koordinatenwechsel (z.B. Polarkoordinaten)? (**Transformationssatz** — die mehrdimensionale Verallgemeinerung der Substitutionsregel.)

<a id="intuition-18"></a>
## Intuition

Das Riemann-Integral im $\mathbb{R}^n$ misst das "Volumen unter dem Graphen" von $f$, approximiert durch immer feinere Quaderzerlegungen — auf jedem kleinen Quader wird $f$ durch einen konstanten Wert ersetzt (Ober-/Untersumme), und man verfeinert die Zerlegung, bis Ober- und Untersumme zusammenfallen.

**Fubini** sagt aus, dass man ein mehrdimensionales Volumen "scheibchenweise" berechnen kann: Um das Volumen unter einem Funktionsgraphen über einem Rechteck zu berechnen, kann man zuerst für jedes feste $y$ die Fläche des entsprechenden Querschnitts (Integral über $x$) berechnen, und dann diese Flächen über $y$ aufsummieren (integrieren) — wie ein Laib Brot, dessen Gesamtvolumen man erhält, indem man die Fläche jeder Scheibe berechnet und über die Dicke aller Scheiben aufsummiert.

**Der Transformationssatz** verallgemeinert die Substitutionsregel $\int f(g(x))g'(x)\,dx = \int f(y)\,dy$ auf mehrere Dimensionen. Der entscheidende neue Bestandteil ist die **Funktionaldeterminante** $|\det Dg(x)|$ — sie misst, wie stark die Transformation $g$ das Volumen an der Stelle $x$ lokal streckt oder staucht. Das ist geometrisch einleuchtend: Eine lineare Abbildung mit Matrix $A$ verzerrt das Volumen eines Parallelepipeds um genau den Faktor $|\det A|$ (Standardfakt der linearen Algebra, hier über Gram-Schmidt bewiesen) — die Transformationsformel überträgt dies lokal (punktweise über die Ableitung) auf nichtlineare Transformationen.

<a id="formale-definitionen-18"></a>
## Formale Definitionen

<a id="definition-21-elementare-stufenfunktion"></a>
### Definition 2.1 (Elementare Stufenfunktion)

Seien $x \prec y \in \mathbb{R}^n$ (d.h. $x_i<y_i$ für alle $i$). Der **halboffene Quader** ist
$$
I[x,y] := \{z\in\mathbb{R}^n : x_i \leq z_i < y_i,\ i=1,\dots,n\}.
$$
Ein **Netz** ist eine Zerlegung des $\mathbb{R}^n$ in solche Quader durch geordnete Punktfolgen $x^1\prec\dots\prec x^k$ in jeder Koordinatenrichtung. Eine Funktion $h:\mathbb{R}^n\to\mathbb{R}$ heißt **elementare Stufenfunktion**, falls ein Netz existiert, sodass $h$ auf jedem Quader des Netzes konstant ist und außerhalb des Netzes (auf dem "unbeschränkten Rest") den Wert $0$ annimmt. Die Menge aller elementaren Stufenfunktionen wird mit $\mathfrak{E}$ bezeichnet.

<a id="definition-23-integral-elementarer-stufenfunktionen"></a>
### Definition 2.3 (Integral elementarer Stufenfunktionen)

$$
\int_{\mathbb{R}^n} \phi(x)\,dx := \sum_{\ell_1,\dots,\ell_n} \omega_{\ell_1,\dots,\ell_n}\cdot \mathrm{Vol}_n(I^{\ell_1,\dots,\ell_n}),
$$
wobei $\omega_{\ell_1,\dots,\ell_n}$ der (konstante) Wert von $\phi$ auf dem Quader $I^{\ell_1,\dots,\ell_n}$ ist und $\mathrm{Vol}_n(I[x,y]) = \prod_{i=1}^n(y_i-x_i)$.

<a id="definition-25-ober-und-unterintegral"></a>
### Definition 2.5 (Ober- und Unterintegral)

Sei $f:\mathbb{R}^n\to\mathbb{R}$ beschränkt mit kompaktem Träger. **Oberintegral** und **Unterintegral**:
$$
\int^* f\,dx := \inf\left\{\int\phi\,dx : \phi\in\mathfrak{E},\ \phi\geq f\right\}, \qquad \int_* f\,dx := \sup\left\{\int\phi\,dx : \phi\in\mathfrak{E},\ \phi\leq f\right\}.
$$

<a id="definition-26-riemann-integrierbarkeit"></a>
### Definition 2.6 (Riemann-Integrierbarkeit)

$f$ heißt **Riemann-integrierbar**, falls $\int^*f\,dx = \int_*f\,dx =: \int f\,dx$.

<a id="sätze-14"></a>
## Sätze

<a id="satz-27-stetige-funktionen-mit-kompaktem-träger-sind-riemann-integrierbar"></a>
### Satz 2.7 (Stetige Funktionen mit kompaktem Träger sind Riemann-integrierbar)

**Aussage:** Ist $f$ beschränkt, $K\subseteq\mathbb{R}^n$ kompakt mit $f=0$ auf $K^c$, und ist $f$ auf $K$ stetig, so ist $f$ Riemann-integrierbar.

**Beweisidee** *(Beweisstil: gleichmäßige Stetigkeit auf Kompakta ausnutzen, Fehlerabschätzung über Zerlegungsfeinheit)*

Man betrachtet $K\subseteq[0,1]^n$ (o.B.d.A. nach Skalierung) und zerlegt in Würfel der Kantenlänge $1/k$. Da $f$ auf dem Kompaktum $[0,1]^n$ **gleichmäßig stetig** ist (klassisches Resultat: Stetigkeit + Kompaktheit $\Rightarrow$ gleichmäßige Stetigkeit, Lemma 1.27), wird die Oszillation von $f$ auf jedem einzelnen (kleinen) Würfel für $k\to\infty$ beliebig klein — dies zeigt, dass Ober- und Untersummen (gebildet aus Supremum bzw. Infimum von $f$ auf jedem Würfel) für $k\to\infty$ gegen denselben Wert konvergieren, also $\int^*f=\int_*f$. $\blacksquare$

<a id="satz-28-satz-von-fubini"></a>
### Satz 2.8 (Satz von Fubini)

**Aussage:** Sei $f:\mathbb{R}^2\to\mathbb{R}$ stetig mit kompaktem Träger. Definiere
$$
g(y) := \int_{\mathbb{R}} f(x,y)\,dx, \qquad h(x) := \int_{\mathbb{R}} f(x,y)\,dy.
$$
Dann gilt
$$
\int_{\mathbb{R}^2} f(x,y)\,d(x,y) = \int_{\mathbb{R}} g(y)\,dy = \int_{\mathbb{R}} h(x)\,dx.
$$

**Bedeutung:** Reduziert ein zweidimensionales (bzw. allgemein $n$-dimensionales) Integral auf iterierte eindimensionale Integrale — das praktische Rechenwerkzeug für explizite Integralberechnungen.

**Beweisidee** *(Beweisstil: Sandwich-Argument über Ober-/Unterintegrale der einzelnen Variablen, mit gleichmäßiger Stetigkeit als Kontrollmittel)*

Man approximiert $f$ durch Stufenfunktionen $\phi_k^-\le f\le\phi_k^+$ (wie im Beweis von Satz 2.7). Für die Ober-/Unterintegrale bezüglich $x$ (bei festem $y$) zeigt man mittels gleichmäßiger Stetigkeit von $f$, dass diese für $k\to\infty$ gleichmäßig in $y$ gegen $g(y)$ konvergieren; dies erlaubt die Vertauschung der Integrationsreihenfolge in den iterierten Ober-/Untersummen, und man erhält im Grenzwert die behauptete Gleichheit der drei Integrale. $\blacksquare$

<a id="satz-29-transformationssatz"></a>
### Satz 2.9 (Transformationssatz)

**Aussage:** Sei $\Omega\subseteq\mathbb{R}^n$ offen, $F:\mathbb{R}^n\to\mathbb{R}$ Riemann-integrierbar, $g:\Omega\to g(\Omega)\subseteq\mathbb{R}^n$ invertierbar mit $g, g^{-1}$ **stetig differenzierbar**. Dann:
$$
\int_\Omega F(g(x))\,dx = \int_{g(\Omega)} F(y)\,|\det(Dg^{-1}(y))|\,dy \qquad \Longleftrightarrow \qquad \int_{g(\Omega)} F(y)\,dy = \int_\Omega F(g(x))\,|\det(Dg(x))|\,dx
$$
(die zweite Form, Korollar 2.11, ist die in der Praxis meist verwendete Version — beide sind äquivalent via $\det(Dg^{-1}(y))=1/\det(Dg(g^{-1}(y)))$, Kettenregel).

**Bedeutung:** Die mehrdimensionale Verallgemeinerung der Substitutionsregel. Der Faktor $|\det Dg(x)|$ (**Funktionaldeterminante** oder **Jacobi-Determinante**) korrigiert die lokale Volumenverzerrung durch $g$.

**Beweis** *(Beweisstil: dreistufiger Beweis — erst Indikatorfunktionen von Quadern, dann lineare Transformationen, schließlich allgemeine $g$ via lokaler Linearisierung)*

**Schritt 1 ($F=\mathbb{1}_R$, $R$ Rechteck):** Direkt aus der Definition des Volumens: $\int_\Omega \mathbb{1}_{g^{-1}(R)}\,dx = \mathrm{Vol}(g^{-1}(R))$.

**Schritt 2 ($g$ linear, $g=L$):** Man zeigt zunächst (Lemma 2.10, siehe unten) mittels **Gram-Schmidt**, dass das Volumen eines von Vektoren $q^1,\dots,q^n$ aufgespannten Parallelepipeds gleich $|\det(q^1,\dots,q^n)|$ ist. Daraus folgt direkt $\mathrm{Vol}(L(R)) = |\det L| \cdot \mathrm{Vol}(R)$ für Rechtecke $R$, also die Formel für $F=\mathbb{1}_R$, $g=L$.

**Schritt 3 (allgemeines $g$, nicht-linear):** Man zerlegt den Zielbereich $R$ in kleine Würfel $I_i^{(k)}$ der Kantenlänge $1/k$. Für $x\in I_i^{(k)}$ gilt (Taylor 1. Ordnung / Definition der Differenzierbarkeit von $g^{-1}$):
$$
g^{-1}(y) = g^{-1}(x_i^{(k)}) + Dg^{-1}(x_i^{(k)})(y-x_i^{(k)}) + \text{Rest}, \qquad \text{Rest} = o(1/k) \text{ gleichmäßig}.
$$
Das bedeutet, dass $g^{-1}(I_i^{(k)})$ approximativ (bis auf einen Fehler, der für $k\to\infty$ relativ verschwindet) das Bild von $I_i^{(k)}$ unter der **linearen** Approximation $Dg^{-1}(x_i^{(k)})$ ist — und für diese lineare Approximation gilt bereits nach Schritt 2:
$$
\mathrm{Vol}(g^{-1}(I_i^{(k)})) = |\det(Dg^{-1}(x_i^{(k)}))|\cdot \mathrm{Vol}(I_i^{(k)}) \cdot (1+o(1)).
$$
Summation über alle Würfel $i$, kombiniert mit der gleichmäßigen Stetigkeit von $\det(Dg^{-1})$ (welche den Approximationsfehler beim Ersetzen von $\det(Dg^{-1}(y))$ durch $\det(Dg^{-1}(x_i^{(k)}))$ innerhalb jedes Würfels kontrolliert), liefert im Grenzwert $k\to\infty$:
$$
\int_R \mathbb{1}\,d(\text{via } g^{-1}) = \int_R |\det(Dg^{-1}(y))|\,dy.
$$
**Schritt 4 (Linearität, dann Approximation durch Stufenfunktionen):** Die Formel für Indikatorfunktionen von Rechtecken überträgt sich (Linearität des Integrals) auf Stufenfunktionen und dann (Approximationsargument, Satz 2.7/Weierstraß-artige Dichtheit) auf beliebige Riemann-integrierbare $F$. $\blacksquare$

<a id="lemma-210-volumen-determinante-via-gram-schmidt"></a>
### Lemma 2.10 (Volumen = Determinante, via Gram-Schmidt)

**Aussage:** Seien $q^1,\dots,q^n\in\mathbb{R}^n$. Das Volumen des von diesen Vektoren aufgespannten Parallelepipeds ist $|\det(q^1,\dots,q^n)|$ (Matrix mit Spalten $q^i$).

**Beweisidee** *(direkt via Gram-Schmidt, Kapitel 6)*: Sind die $q^i$ bereits **orthogonal**, ist das Volumen offensichtlich $\prod_i\|q^i\|$ (Quaderformel), und dies stimmt mit $|\det|$ überein, da die Determinante einer Diagonalmatrix mit Einträgen $\|q^i\|$ (nach geeigneter orthonormaler Basiswahl) gerade $\prod_i\|q^i\|$ ist. Im allgemeinen Fall führt man das **Gram-Schmidt-Verfahren** (Kapitel 6!) an $q^1,\dots,q^n$ durch, das eine orthogonale Familie $p^1,\dots,p^n$ mit $\mathrm{Vol}(q^1,\dots,q^n)=\mathrm{Vol}(p^1,\dots,p^n)=\prod_i\|p^i\|$ liefert (das Volumen ändert sich bei den Gram-Schmidt-Scherungsoperationen nicht — geometrisch: Ein "Schrägstellen" des Parallelepipeds durch Addition eines Vielfachen einer anderen Kante ändert das Volumen nicht, analog zum Determinanten-Kalkül: Spaltenumformungen vom Typ "Addition eines Vielfachen einer anderen Spalte" ändern die Determinante nicht). Da zudem $\det(q^1,\dots,q^n)=\det(p^1,\dots,p^n)$ (dieselben Spaltenumformungen ändern die Determinante nicht — Standardfakt der linearen Algebra), folgt
$$
\mathrm{Vol}(q^1,\dots,q^n) = \prod_i\|p^i\| = |\det(p^1,\dots,p^n)| = |\det(q^1,\dots,q^n)|. \qquad \blacksquare
$$

**Dies ist die angekündigte Querverbindung zu Kapitel 6**: Ohne das Gram-Schmidt-Verfahren wäre dieser fundamentale Fakt der linearen Algebra (Volumen = Determinante) an dieser Stelle nicht elementar beweisbar.

<a id="algorithmus-polarkoordinaten-als-standardanwendung-des-transformationssatzes"></a>
## Algorithmus: Polarkoordinaten als Standardanwendung des Transformationssatzes

**Motivation:** Viele Integrale über kreisförmige/radialsymmetrische Bereiche vereinfachen sich drastisch in Polarkoordinaten.

**Transformation:**
$$
g: [0,\infty)\times[0,2\pi) \to \mathbb{R}^2, \qquad g(r,\theta) = (r\cos\theta, r\sin\theta).
$$

**Jacobi-Matrix und Determinante:**
$$
Dg(r,\theta) = \begin{pmatrix}\cos\theta & -r\sin\theta \\ \sin\theta & r\cos\theta\end{pmatrix}, \qquad \det(Dg(r,\theta)) = r\cos^2\theta + r\sin^2\theta = r.
$$

**Transformationsformel:**
$$
\int_{\mathbb{R}^2} F(x,y)\,d(x,y) = \int_0^\infty\int_0^{2\pi} F(r\cos\theta,r\sin\theta)\cdot r\,d\theta\,dr.
$$

**Typische Anwendung (Gauß-Integral):**
$$
\left(\int_{-\infty}^\infty e^{-x^2/2}\,dx\right)^2 = \int_{\mathbb{R}^2} e^{-(x^2+y^2)/2}\,d(x,y) = \int_0^\infty\int_0^{2\pi} e^{-r^2/2}\,r\,d\theta\,dr = 2\pi\int_0^\infty re^{-r^2/2}\,dr = 2\pi\left[-e^{-r^2/2}\right]_0^\infty = 2\pi,
$$
also $\int_{-\infty}^\infty e^{-x^2/2}\,dx = \sqrt{2\pi}$ — die berühmte Normierungskonstante der Standardnormalverteilung.

**Typische Fehler:** Den Faktor $r$ (die Jacobi-Determinante) beim Übergang zu Polarkoordinaten vergessen — der häufigste Einzelfehler in diesem gesamten Kapitel.

<a id="beispiele-16"></a>
## Beispiele

**Beispiel 1 (leicht, Fubini):** $\int_{[0,1]^2} xy\,d(x,y) = \int_0^1\left(\int_0^1 xy\,dx\right)dy = \int_0^1 \tfrac12 y\,dy = \tfrac14$.

**Beispiel 2 (mittel, Transformation):** Berechnen Sie $\int_D (x^2+y^2)\,d(x,y)$, $D=\{x^2+y^2\le 4\}$, via Polarkoordinaten:
$$
\int_0^2\int_0^{2\pi} r^2\cdot r\,d\theta\,dr = 2\pi\int_0^2 r^3\,dr = 2\pi\cdot 4 = 8\pi.
$$

**Beispiel 3 (schwer, kombiniert Fubini + Transformation):** Berechnen Sie das Volumen der Kugel $B_R=\{x^2+y^2+z^2\le R^2\}\subseteq\mathbb{R}^3$ mittels Kugelkoordinaten (analoge Transformation mit Jacobi-Determinante $r^2\sin\phi$, hier nicht explizit hergeleitet, aber Standardstoff): $\mathrm{Vol}(B_R) = \tfrac43\pi R^3$.

<a id="gegenbeispiele-16"></a>
## Gegenbeispiele

- **Fubini scheitert ohne Integrierbarkeitsvoraussetzung:** Für gewisse unbeschränkte oder nicht absolut integrierbare Funktionen können die iterierten Integrale $\int\int f$ und $\int\int f$ (in vertauschter Reihenfolge) verschiedene Werte liefern oder gar nicht existieren — Standardgegenbeispiel (außerhalb dieser Vorlesung, aber gut zu kennen): $f(x,y)=\frac{x^2-y^2}{(x^2+y^2)^2}$ auf $(0,1)^2$.
- **Transformationssatz ohne Invertierbarkeit:** Ist $g$ nicht injektiv (z.B. $g(r,\theta)$ mit $\theta\in[0,4\pi)$, "doppelt überdeckt"), liefert die naive Anwendung der Formel einen um den Faktor der Überdeckungsvielfachheit falschen Wert.

<a id="typische-klausuraufgaben-17"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Erkennungsmerkmal | Strategie |
|---|---|---|
| "Berechnen Sie $\int_D f\,d(x,y)$" (Rechteckbereich) | Produktbereich, einfache Funktion | Fubini direkt anwenden, iterierte Integrale berechnen |
| "Berechnen Sie $\int_D f$" über Kreis/Kugel/Radialbereich | Kreisförmiger Integrationsbereich, oder Integrand hängt nur von $x^2+y^2$ ab | Polarkoordinaten (2D) bzw. Kugelkoordinaten (3D), Jacobi-Determinante nicht vergessen! |
| "Zeigen Sie $\int e^{-x^2}dx=\sqrt\pi$" | Gauß-Integral-artige Aufgabe | Quadrieren, auf $\mathbb{R}^2$ übergehen, Polarkoordinaten |
| "Bestimmen Sie das Volumen von ..." | Geometrischer Körper | Geeignete Koordinatentransformation wählen, Integrationsgrenzen sorgfältig bestimmen |

<a id="typische-fehler-17"></a>
## Typische Fehler

1. **Jacobi-Determinante bei Koordinatentransformation vergessen.**
2. **Integrationsreihenfolge bei Fubini falsch anpassen, wenn sich die Grenzen des inneren Integrals mit der äußeren Variablen ändern** (bei nicht-rechteckigen Bereichen die Grenzen falsch aus der Bereichsbeschreibung ablesen).
3. **Bei Transformation vergessen, dass die neuen Integrationsgrenzen dem transformierten Bereich $g^{-1}(\Omega)$ entsprechen müssen**, nicht dem ursprünglichen Bereich.
4. **Vorzeichen/Betrag bei der Jacobi-Determinante vergessen** — es steht immer $|\det Dg|$, nicht $\det Dg$.

<a id="verbindungen-18"></a>
## Verbindungen

- Der Beweis des Transformationssatzes (via Lemma 2.10) nutzt das **Gram-Schmidt-Verfahren** aus Kapitel 6 — eine der schönsten Querverbindungen des gesamten Skripts.
- Satz 2.7 (Integrierbarkeit stetiger Funktionen) nutzt **gleichmäßige Stetigkeit auf Kompakta**, die letztlich auf dem Satz von Heine-Borel (Kapitel 2) beruht.
- Das Riemann-Integral wird im nächsten Kapitel (Kurvenintegrale) direkt für die Definition von Wegintegralen $\int_\gamma \omega$ verwendet.
- Der Transformationssatz wird in Kapitel Komplexe Analysis implizit gebraucht, um komplexe Kurvenintegrale mit reellen Doppelintegralen (Satz von Green/Cauchy) zu verknüpfen.

<a id="zusammenfassung-kapitel-10"></a>
## Zusammenfassung Kapitel 10

- Das mehrdimensionale **Riemann-Integral** wird über Ober-/Unterintegrale bezüglich elementarer Stufenfunktionen definiert; stetige Funktionen mit kompaktem Träger sind stets Riemann-integrierbar (Satz 2.7).
- Der **Satz von Fubini** (Satz 2.8) erlaubt die Berechnung mehrdimensionaler Integrale als iterierte eindimensionale Integrale.
- Der **Transformationssatz** (Satz 2.9) verallgemeinert die Substitutionsregel: $\int_{g(\Omega)}F\,dy = \int_\Omega F(g(x))|\det Dg(x)|\,dx$; der Beweis beruht fundamental auf der Identifikation von Volumen und Determinante (Lemma 2.10, via Gram-Schmidt).
- **Polarkoordinaten** (Jacobi-Determinante $r$) sind die wichtigste konkrete Anwendung — Standardbeispiel: Gauß-Integral $\int e^{-x^2/2}dx=\sqrt{2\pi}$.

---

*Ende Teil 5. Fortsetzung folgt mit Kapitel 11 (Kurvenintegrale, Differentialformen) und Kapitel 12 (Komplexe Analysis) auf Anfrage.*



---

<a id="analysis-auf-allgemeinen-linearen-räumen-teil-6-abschluss"></a>
# Analysis auf allgemeinen linearen Räumen — Teil 6 (Abschluss)

*Fortsetzung von Teil 1–5. Dieses Dokument setzt das gesamte bisherige Skript als bekannt voraus, insbesondere Kapitel 5 (Satz von Schwarz) und Kapitel 10 (Riemann-Integral).*

---

<a id="kapitel-11-kurvenintegrale-und-differentialformen"></a>
# Kapitel 11: Kurvenintegrale und Differentialformen

<a id="motivation-19"></a>
## Motivation

**Welches Problem lösen wir?**

Bisher haben wir Funktionen über *Bereiche* (Quader, Kreise) integriert. Jetzt wollen wir Funktionen — genauer: **Vektorfelder** — entlang einer *Kurve* integrieren. Die physikalische Grundfrage lautet: *Wie viel Arbeit verrichtet ein Kraftfeld, wenn ein Teilchen sich entlang eines vorgegebenen Weges bewegt?* Dies führt zum **Kurvenintegral**.

Die zentrale, tiefe Frage dieses Kapitels ist: *Wann hängt das Kurvenintegral nur vom Anfangs- und Endpunkt ab, unabhängig vom konkret gewählten Weg?* Die Antwort führt zum Begriff der **exakten Differentialform** — einer Form, die als Ableitung einer "Potentialfunktion" darstellbar ist. Dies ist die höherdimensionale Verallgemeinerung des Hauptsatzes der Differential- und Integralrechnung.

**Physikalischer Hintergrund:** In der Physik entspricht Wegunabhängigkeit des Arbeitsintegrals genau der Existenz eines **Potentials** (z.B. Gravitationspotential, elektrisches Potential) — konservative Kraftfelder sind exakt die Gradientenfelder solcher Potentiale.

<a id="intuition-19"></a>
## Intuition

**Kurve vs. Parametrisierung:** Ein wichtiger begrifflicher Punkt, den die Vorlesung explizit betont: Eine "Kurve" ist **nicht** einfach eine Teilmenge des $\mathbb{R}^n$ — sie ist eine **Äquivalenzklasse von Parametrisierungen**. Der Kreis $\{x^2+y^2=1\}$ als *Menge* sagt nichts darüber aus, ob man ihn einmal, zweimal oder mit variabler Geschwindigkeit durchläuft. Erst die Parametrisierung (die "Uhr", die angibt, wo man sich zu welcher Zeit befindet) macht daraus eine Kurve im Sinne dieses Kapitels.

**Differentialformen als "Messgeräte für Richtungen":** Eine 1-Form $\omega$ ordnet jedem Punkt $x$ eine lineare Abbildung $\omega(x): \mathbb{R}^n\to\mathbb{R}$ zu — ein "Messgerät", das, angewendet auf einen Tangentialvektor (eine Richtung), eine Zahl liefert. Bewegt man sich entlang einer Kurve, wird an jedem Punkt der Tangentialvektor der Kurve gemessen, und die Summe (das Integral) all dieser Messungen ergibt das Kurvenintegral.

**Exakt vs. geschlossen — die zentrale Unterscheidung:** Eine Form ist *exakt*, wenn sie ein globales Potential besitzt ($\omega=Df$). Eine Form ist *geschlossen*, wenn sie lokal die notwendige Symmetriebedingung (Satz von Schwarz!) erfüllt ($\partial_i\omega_j = \partial_j\omega_i$). Jede exakte Form ist geschlossen (leichte Richtung) — aber **nicht** jede geschlossene Form ist exakt (die berühmte Umkehrung scheitert im Allgemeinen, siehe das klassische Gegenbeispiel unten)! Dies ist eine der wichtigsten Lehren des Kapitels und ein beliebter Fallstrick.

<a id="formale-definitionen-19"></a>
## Formale Definitionen

<a id="definition-kurve-und-parametrisierung"></a>
### Definition (Kurve und Parametrisierung)

Sei $I=[a,b]\subseteq\mathbb{R}$. Eine Abbildung $g:I\to\mathbb{R}^n$ heißt **Parametrisierung** einer Kurve.

<a id="definition-31-äquivalenz-von-parametrisierungen"></a>
### Definition 3.1 (Äquivalenz von Parametrisierungen)

Seien $h,g$ stetig differenzierbare Parametrisierungen (auf $I=[a,b]$ bzw. $J=[\alpha,\beta]$). $h$ und $g$ heißen **äquivalent**, falls eine Funktion $\psi: I\to J$ existiert mit:
$$
\text{(i)}\ \psi \text{ streng monoton wachsend, stetig diffbar, } \psi'(t)\neq0\ \forall t, \qquad \text{(ii)}\ \psi(a)=\alpha,\ \psi(b)=\beta,
$$
sodass $h = g\circ\psi$.

<a id="definition-32-kurve"></a>
### Definition 3.2 (Kurve)

Eine **Kurve** $\gamma$ der Klasse $C^{(k)}$ ist eine **Äquivalenzklasse** von Parametrisierungen der Klasse $C^{(k)}$ bezüglich obiger Äquivalenzrelation.

> **Wichtige Warnung (in der Mitschrift explizit hervorgehoben):** *Eine Kurve ist nicht einfach eine Teilmenge des $\mathbb{R}^n$!* Zwei völlig verschiedene Parametrisierungen (unterschiedliche Geschwindigkeit, sogar unterschiedliche Richtung, falls man die Monotoniebedingung abschwächt) können dieselbe Kurve im Sinne dieser Definition sein, solange sie durch eine zulässige Umparametrisierung $\psi$ auseinander hervorgehen.

**Jordankurve:** Eine Kurve heißt **Jordankurve**, wenn für jede Parametrisierung $g$ gilt: $g(t_1)=g(t_2) \Rightarrow t_1=t_2$ (außer eventuell an den Endpunkten für geschlossene Kurven) — d.h. die Kurve "kreuzt sich selbst nicht".

<a id="definition-33-länge-einer-kurve-bogenlänge"></a>
### Definition 3.3 (Länge einer Kurve, Bogenlänge)

Sei $\gamma$ Kurve, $g$ Parametrisierung. Die **Länge** ist
$$
L(\gamma) := \int_I \|g'(t)\|\,dt \qquad \text{(unabhängig von der Wahl der Parametrisierung — Übung/Kettenregel)}.
$$
Die **Bogenlängenparametrisierung** $h:[0,L(\gamma)]\to\mathbb{R}^n$ ist die (bis auf Orientierung eindeutige) Parametrisierung mit $\|h'(t)\|=1$ für alle $t$ — die "Parametrisierung mit konstanter Einheitsgeschwindigkeit".

<a id="definition-vektorfeld-differentialform"></a>
### Definition (Vektorfeld, Differentialform)

Ein **Vektorfeld** ist eine Abbildung $V:\mathbb{R}^n\to\mathbb{R}^n$. Eine **Differentialform** (genauer: 1-Form) ist eine Abbildung
$$
\omega:\mathbb{R}^n \to L(\mathbb{R}^n,\mathbb{R}), \qquad \omega(x) = \sum_{i=1}^n \omega_i(x)\,e^i,
$$
wobei $e^i:\mathbb{R}^n\to\mathbb{R}$ die duale Basis ist ($e^i(e_j)=\delta_{ij}$) — man identifiziert $e^i \equiv dx_i$.

**Zusammenhang:** Ist $f:\mathbb{R}^n\to\mathbb{R}$ differenzierbar, so ist $Df(x) = \sum_i \frac{\partial f}{\partial x_i}(x)\,e^i =: df(x)$ eine (spezielle Art von) 1-Form.

<a id="definition-34-exakte-und-geschlossene-formen"></a>
### Definition 3.4 (Exakte und geschlossene Formen)

Eine 1-Form $\omega$ auf $D\subseteq\mathbb{R}^n$ heißt

$$
\textbf{exakt} \quad :\iff \quad \exists f\in C^{(1)}(D,\mathbb{R}): \omega = Df \text{ auf } D,
$$

$$
\textbf{geschlossen} \quad :\iff \quad \forall x\in D\ \forall i,j=1,\dots,n: \quad \frac{\partial\omega_i(x)}{\partial x_j} = \frac{\partial\omega_j(x)}{\partial x_i}.
$$

<a id="definition-37-integral-einer-differentialform-längs-einer-kurve"></a>
### Definition 3.7 (Integral einer Differentialform längs einer Kurve)

Sei $\gamma$ Kurve, $\omega$ stetige 1-Form, $g$ Parametrisierung von $\gamma$. Dann
$$
\int_\gamma \omega := \int_I \omega(g(t))\big[g'(t)\big]\,dt.
$$

> **Wohldefiniertheit:** Dieses Integral ist **unabhängig von der Wahl der Parametrisierung** (Übung via Substitutionsregel, angewendet auf die Umparametrisierungsfunktion $\psi$) — ein weiterer Beweis dafür, warum die abstrakte Definition der Kurve als Äquivalenzklasse (statt als bloße Punktmenge) die richtige ist.

<a id="eigenschaften-16"></a>
## Eigenschaften

<a id="lemma-35-exakt-rightarrow-geschlossen"></a>
### Lemma 3.5 (Exakt $\Rightarrow$ geschlossen)

**Aussage:** Jede exakte $C^{(1)}$-Differentialform ist geschlossen.

**Beweis** *(Beweisstil: direkte Anwendung des Satzes von Schwarz)*

Ist $\omega=Df$ exakt, so $\omega_i(x) = \frac{\partial f(x)}{\partial x_i}$. Dann
$$
\frac{\partial\omega_i(x)}{\partial x_j} = \frac{\partial^2f(x)}{\partial x_j\partial x_i} \stackrel{\text{Satz von Schwarz (Lemma 1.65)}}{=} \frac{\partial^2f(x)}{\partial x_i\partial x_j} = \frac{\partial\omega_j(x)}{\partial x_i}. \qquad \blacksquare
$$

**Bedeutung:** Dies ist die **erste** (leichte) Richtung des Zusammenhangs zwischen exakt und geschlossen — der Satz von Schwarz aus Kapitel 5 wird hier zum ersten Mal direkt "geerntet". Die **Umkehrung gilt im Allgemeinen nicht** (siehe unten) — sie erfordert zusätzliche topologische Voraussetzungen an den Definitionsbereich.

<a id="sätze-15"></a>
## Sätze

<a id="satz-38-hauptsatz-für-kurvenintegrale-wegunabhängigkeit-exakter-formen"></a>
### Satz 3.8 (Hauptsatz für Kurvenintegrale — Wegunabhängigkeit exakter Formen)

**Aussage:** Sei $\omega=Df$ exakt auf $D$, $\gamma$ Kurve in $D$ von $x_0$ nach $x_1$ (mit Parametrisierung $g:[a,b]\to D$, $g(a)=x_0$, $g(b)=x_1$). Dann:
$$
\int_\gamma \omega = f(x_1)-f(x_0).
$$
Insbesondere: Ist $\gamma$ **geschlossen** ($x_0=x_1$), so $\int_\gamma\omega=0$.

**Bedeutung:** Die höherdimensionale Version des Hauptsatzes der Differential- und Integralrechnung: Das Kurvenintegral einer exakten Form hängt nur vom Anfangs- und Endpunkt ab — der konkrete Weg dazwischen ist irrelevant. Dies rechtfertigt die physikalische Sprechweise "konservatives Kraftfeld" (die verrichtete Arbeit hängt nicht vom gewählten Weg ab, nur von der Potentialdifferenz).

**Beweis** *(Beweisstil: direkte Rechnung via Kettenregel und Hauptsatz der eindimensionalen Integralrechnung)*

$$
\int_\gamma \omega = \int_a^b \omega(g(t))[g'(t)]\,dt = \int_a^b Df(g(t))[g'(t)]\,dt = \int_a^b \frac{d}{dt}\big[f(g(t))\big]\,dt \qquad \text{(Kettenregel!)}
$$
$$
= f(g(b))-f(g(a)) = f(x_1)-f(x_0)
$$
(nach dem eindimensionalen Hauptsatz der Differential- und Integralrechnung, angewendet auf die skalare Funktion $t\mapsto f(g(t))$). $\blacksquare$

<a id="satz-38a-umkehrung-wegunabhängigkeit-rightarrow-exaktheit"></a>
### Satz 3.8a (Umkehrung — Wegunabhängigkeit $\Rightarrow$ Exaktheit)

**Aussage:** Gilt $\int_\gamma\omega=0$ für **jede** geschlossene Kurve $\gamma$ in $D$, so ist $\omega$ exakt.

**Bedeutung:** Zusammen mit Satz 3.8 liefert dies eine vollständige Charakterisierung: Exaktheit $\iff$ Wegunabhängigkeit $\iff$ Verschwinden auf allen geschlossenen Kurven.

**Beweis** *(Beweisstil: explizite Konstruktion der Stammfunktion via Integration von einem Basispunkt, dann Nachweis der Differenzierbarkeit)*

**Konstruktion der Kandidatenfunktion:** Fixiere $x_0\in D$. Für $x\in D$ definiere $f(x) := \int_{\gamma_x}\omega$ für **irgendeine** Kurve $\gamma_x$ von $x_0$ nach $x$ (dies ist wohldefiniert, d.h. unabhängig von der Wahl von $\gamma_x$: Sind $\gamma_x,\gamma_x'$ zwei solche Kurven, so ist $\gamma_x$ gefolgt von $\gamma_x'$ rückwärts eine geschlossene Kurve, auf der nach Voraussetzung $\int\omega=0$ gilt — also $\int_{\gamma_x}\omega=\int_{\gamma_x'}\omega$).

**Nachweis $Df(x)=\omega(x)$:** Sei $h\in\mathbb{R}^n$ klein. Wähle als Weg von $x_0$ nach $x+h$ die Konkatenation von $\gamma_x$ (bis $x$) mit der geraden Verbindungsstrecke $g(s):=x+sh$, $s\in[0,1]$, von $x$ nach $x+h$. Dann
$$
f(x+h)-f(x) = \int_0^1 \omega(x+sh)[h]\,ds.
$$
Man schätzt ab:
$$
\left|f(x+h)-f(x)-\omega(x)[h]\right| = \left|\int_0^1 \big(\omega(x+sh)-\omega(x)\big)[h]\,ds\right| \leq \|h\|\cdot\sup_{s\in[0,1]}\|\omega(x+sh)-\omega(x)\|,
$$
und das Supremum geht (wegen Stetigkeit von $\omega$) für $h\to0$ gegen $0$ — also $f(x+h)-f(x)-\omega(x)[h]=o(\|h\|)$, d.h. $Df(x)=\omega(x)$. $\blacksquare$

<a id="gegenbeispiele-17"></a>
## Gegenbeispiele

<a id="das-klassische-gegenbeispiel-geschlossen-aber-nicht-exakt"></a>
### Das klassische Gegenbeispiel: Geschlossen, aber nicht exakt

Betrachten Sie auf $D=\mathbb{R}^2\setminus\{(0,0)\}$ die Form
$$
\omega = x\,dy - y\,dx.
$$

**Prüfung auf Geschlossenheit:** $\omega_1=-y$, $\omega_2=x$; $\partial_y\omega_1 = -1$, $\partial_x\omega_2=1$. **Diese stimmen nicht überein** — diese spezielle Form ist also gar nicht geschlossen. *(Korrektur zur illustrativen Standardform: die tatsächlich in der Vorlesung behandelte, korrekt geschlossene, aber nicht exakte Form ist die folgende.)*

**Die korrekte Standardform (Winkelform):**
$$
\omega = \frac{-y\,dx + x\,dy}{x^2+y^2} \qquad \text{auf } D=\mathbb{R}^2\setminus\{(0,0)\}.
$$
Direktes Nachrechnen zeigt $\partial_y\omega_1 = \partial_x\omega_2 = \frac{y^2-x^2}{(x^2+y^2)^2}$ — die Form **ist geschlossen**.

**Integral über den Einheitskreis** (Parametrisierung $g(\theta)=(\cos\theta,\sin\theta)$, $\theta\in[0,2\pi]$):
$$
\int_\gamma \omega = \int_0^{2\pi} \big(\cos^2\theta+\sin^2\theta\big)\,d\theta = \int_0^{2\pi} 1\,d\theta = 2\pi \neq 0.
$$

Da das Integral über eine geschlossene Kurve **nicht** verschwindet, ist $\omega$ nach Satz 3.8 (Kontraposition) **nicht exakt** — obwohl $\omega$ geschlossen ist!

**Warum funktioniert die Umkehrung hier nicht?** Der Beweis von Satz 3.8a scheitert hier daran, dass der Definitionsbereich $D=\mathbb{R}^2\setminus\{0\}$ **nicht einfach zusammenhängend** ist (man kann eine Schleife um den Ursprung nicht innerhalb von $D$ auf einen Punkt zusammenziehen). Diese topologische Einschränkung ist in der Mitschrift nicht explizit als Satz formuliert, aber implizit in den Beispielen sichtbar — sie ist als das **Poincaré-Lemma** bekannt: *Auf einfach zusammenhängenden Gebieten ist jede geschlossene Form exakt.* Auf $\mathbb{R}^2\setminus\{0\}$ (nicht einfach zusammenhängend, da der fehlende Punkt "im Weg steht") gilt dies nicht mehr.

**Die "reparierte" exakte Variante:** Die Form $\omega=x^2dx+y^2dy = \tfrac13 d(x^3+y^3)$ ist dagegen (auf ganz $\mathbb{R}^2$, wo kein Loch stört) sowohl geschlossen als auch exakt, mit Stammfunktion $f(x,y)=\tfrac13(x^3+y^3)$ — Integral über jede geschlossene Kurve verschwindet.

<a id="beispiele-17"></a>
## Beispiele

**Beispiel 1 (leicht):** Berechnen Sie $\int_\gamma \omega$ für $\omega=y\,dx+x\,dy$ (exakt, mit $f(x,y)=xy$) entlang **irgendeiner** Kurve von $(0,0)$ nach $(1,2)$. Nach Satz 3.8: $\int_\gamma\omega = f(1,2)-f(0,0) = 2-0=2$ — unabhängig vom konkreten Weg.

**Beispiel 2 (mittel):** Zeigen Sie, dass $\omega=(2xy)\,dx+(x^2+3y^2)\,dy$ exakt ist, und finden Sie eine Stammfunktion. *Lösung:* $\partial_y(2xy)=2x=\partial_x(x^2+3y^2)$ — geschlossen. Auf einfach zusammenhängendem $\mathbb{R}^2$: exakt. Stammfunktion (via Integration): $f(x,y)=x^2y+y^3$.

**Beispiel 3 (schwer):** Berechnen Sie $\int_\gamma \omega$ für die Winkelform $\omega=\frac{-ydx+xdy}{x^2+y^2}$ entlang einer Kurve, die den Ursprung **zweimal** umläuft. *Lösung:* Analog zur obigen Rechnung, aber mit $\theta\in[0,4\pi]$: $\int_\gamma\omega = 4\pi$ — das Integral "zählt" die Anzahl der Umläufe (Windungszahl), multipliziert mit $2\pi$.

<a id="vergleichstabelle-exakt-vs-geschlossen"></a>
## Vergleichstabelle: exakt vs. geschlossen

| Eigenschaft | Definition | Gilt immer? |
|---|---|---|
| **Exakt** | $\omega = Df$ für ein $f$ | Stärkere Eigenschaft |
| **Geschlossen** | $\partial_i\omega_j=\partial_j\omega_i$ überall | Schwächere, lokale Eigenschaft |
| Exakt $\Rightarrow$ Geschlossen | Immer (Lemma 3.5, via Satz von Schwarz) | ✓ |
| Geschlossen $\Rightarrow$ Exakt | Nur auf **einfach zusammenhängenden** Gebieten (Poincaré-Lemma) | ✗ im Allgemeinen (Gegenbeispiel: Winkelform) |

<a id="typische-klausuraufgaben-18"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Erkennungsmerkmal | Strategie |
|---|---|---|
| "Ist $\omega$ exakt? Finden Sie ggf. eine Stammfunktion" | Explizite 1-Form gegeben | Geschlossenheit prüfen (partielle Ableitungen vergleichen); bei einfach zusammenhängendem Gebiet: Stammfunktion durch sukzessive Integration konstruieren |
| "Berechnen Sie $\int_\gamma\omega$" (nicht exakte Form) | Explizite Kurve und Form gegeben | Direkt über die Definition parametrisieren und das eindimensionale Integral auswerten |
| "Zeigen Sie, dass $\omega$ geschlossen, aber nicht exakt ist" | Form mit Definitionslücke (z.B. bei $0$) | Geschlossenheit direkt nachrechnen; Nicht-Exaktheit über ein Integral über eine geeignete geschlossene Kurve (typischerweise Einheitskreis um die Singularität) zeigen, das $\neq 0$ ist |

<a id="typische-fehler-18"></a>
## Typische Fehler

1. **Geschlossen mit exakt gleichsetzen**, ohne den Definitionsbereich auf einfachen Zusammenhang zu prüfen — der klassische Fehler dieses Kapitels.
2. **Bei der Berechnung von Kurvenintegralen die Parametrisierung falsch ableiten** (Kettenregel vergessen, $g'(t)$ falsch berechnen).
3. **Vorzeichen bei Umkehrung der Durchlaufrichtung vergessen:** $\int_{-\gamma}\omega = -\int_\gamma\omega$.

<a id="verbindungen-19"></a>
## Verbindungen

- Lemma 3.5 ist die direkte Anwendung des **Satzes von Schwarz** (Kapitel 5) — ohne ihn ließe sich nicht einmal die *leichte* Richtung (exakt $\Rightarrow$ geschlossen) beweisen.
- Kurvenintegrale und die Mittelwertungleichung (Kapitel 3, Lemma 1.90) sind eng verwandt: Der Beweis von Lemma 1.90 nutzt implizit den Hauptsatz für Wegintegrale $F(1)-F(0)=\int_0^1F'(s)\,ds$.
- Kapitel 12 (komplexe Analysis) baut Differentialformen und Kurvenintegrale direkt weiter aus: Das komplexe Kurvenintegral $\int_\gamma f(z)\,dz$ zerfällt in Real- und Imaginärteil, die jeweils reelle 1-Formen $\omega,\hat\omega$ darstellen — und die Frage "wann verschwindet $\int_\gamma f\,dz$ für geschlossene $\gamma$" wird zum **Cauchyschen Integralsatz**, dessen Beweis direkt auf der Exaktheits-Theorie dieses Kapitels aufbaut.

<a id="zusammenfassung-kapitel-11"></a>
## Zusammenfassung Kapitel 11

- Eine **Kurve** ist eine Äquivalenzklasse von Parametrisierungen — nicht bloß eine Punktmenge.
- Das **Kurvenintegral** $\int_\gamma\omega = \int_I \omega(g(t))[g'(t)]\,dt$ ist unabhängig von der gewählten Parametrisierung.
- **Exakte** Formen ($\omega=Df$) sind stets **geschlossen** (Satz von Schwarz), aber die Umkehrung gilt nur auf einfach zusammenhängenden Gebieten (Poincaré-Lemma) — Standard-Gegenbeispiel: die Winkelform auf $\mathbb{R}^2\setminus\{0\}$ mit Integral $2\pi$ über den Einheitskreis.
- Exaktheit $\iff$ Wegunabhängigkeit $\iff$ Verschwinden des Integrals über jede geschlossene Kurve (Satz 3.8 und 3.8a).

---

<a id="kapitel-12-komplexe-analysis"></a>
# Kapitel 12: Komplexe Analysis

<a id="motivation-20"></a>
## Motivation

**Welches Problem lösen wir?**

Die komplexen Zahlen $\mathbb{C}$ lassen sich als $\mathbb{R}^2$ mit einer zusätzlichen Multiplikationsstruktur auffassen. Funktionen $f:\mathbb{C}\to\mathbb{C}$ können daher sowohl als Funktionen $\mathbb{R}^2\to\mathbb{R}^2$ (mit der bisherigen Differentialrechnung) **als auch** über den neuen, komplexen Differenzenquotienten $\lim_{z\to a}\frac{f(z)-f(a)}{z-a}$ untersucht werden. Die zentrale Entdeckung dieses Kapitels: **Komplexe Differenzierbarkeit ist eine viel stärkere Bedingung** als reelle Differenzierbarkeit von $\mathbb{R}^2\to\mathbb{R}^2$ — sie erzwingt zusätzlich die **Cauchy-Riemann-Gleichungen**. Funktionen, die dieser stärkeren Bedingung überall genügen (**holomorphe** Funktionen), haben verblüffende Eigenschaften (automatische $C^\infty$-Glattheit, Potenzreihenentwicklung, der Cauchysche Integralsatz), die reell differenzierbare Funktionen im Allgemeinen nicht haben.

**Warum ist der Unterschied so groß?** Bei der reellen Differenzierbarkeit $\mathbb{R}^2\to\mathbb{R}^2$ darf die lineare Approximation eine **beliebige** $2\times2$-Matrix sein. Bei komplexer Differenzierbarkeit ("$\lim (f(z)-f(a))/(z-a)$ existiert") muss diese lineare Approximation die spezielle Form "Multiplikation mit einer komplexen Zahl" haben — und Multiplikation mit einer komplexen Zahl entspricht (wie wir sehen werden) genau den $2\times2$-Matrizen einer sehr speziellen Form (Drehstreckungen). Diese Einschränkung ist der Ursprung aller "Wunder" der komplexen Analysis.

<a id="intuition-20"></a>
## Intuition

**Multiplikation mit einer komplexen Zahl als Drehstreckung:** Ist $c=a+ib$, so bewirkt die Multiplikation $z\mapsto cz$ auf $\mathbb{R}^2$ (via $z=x+iy \leftrightarrow (x,y)$) genau die lineare Abbildung mit Matrix $\begin{pmatrix}a&-b\\b&a\end{pmatrix}$ — eine Drehung um $\arg(c)$ kombiniert mit einer Streckung um $|c|$. **Keine** beliebige $2\times2$-Matrix hat diese Form — nur Matrizen mit dieser speziellen "antisymmetrischen Diagonalstruktur". Komplex differenzierbar zu sein bedeutet also: *Die lokale lineare Approximation von $f$ ist überall eine reine Drehstreckung* — winkeltreu (konform), im Gegensatz zu einer allgemeinen linearen Abbildung, die Winkel verzerren kann.

**Der Cauchysche Integralsatz — geometrische Intuition:** Ist $f$ holomorph, so "gibt es keine Quellen oder Senken" im Inneren einer geschlossenen Kurve — das Integral über jede geschlossene Kurve (in einem einfach zusammenhängenden Gebiet) verschwindet. Dies ist strukturell identisch mit der Aussage "geschlossene Form auf einfach zusammenhängendem Gebiet ist exakt" aus Kapitel 11 — und tatsächlich ist der Cauchysche Integralsatz **genau diese Aussage**, angewendet auf die aus $f$ gewonnenen reellen 1-Formen.

<a id="formale-definitionen-20"></a>
## Formale Definitionen

<a id="definition-41-komplexe-zahlen"></a>
### Definition 4.1 (Komplexe Zahlen)

$$
\mathbb{C} := \{z=a+ib : a,b\in\mathbb{R}\}, \qquad i^2=-1,
$$
mit Addition $(a+ib)+(c+id)=(a+c)+i(b+d)$ und Multiplikation $(a+ib)(c+id)=(ac-bd)+i(bc+ad)$ — dies macht $\mathbb{C}$ zu einem **Körper**. **Konjugation** $\bar z:=a-ib$; $\mathrm{Re}(z):=(z+\bar z)/2$, $\mathrm{Im}(z):=(z-\bar z)/(2i)$; **Betrag** $|z|:=\sqrt{z\bar z}=\sqrt{a^2+b^2}$ (identisch mit der euklidischen Norm auf $\mathbb{R}^2$).

**Polardarstellung:** $z=r(\cos\varphi+i\sin\varphi)$, $r=|z|$, $\varphi=\arg(z)$; es gilt $|z_1z_2|=|z_1||z_2|$, $\arg(z_1z_2)=\arg(z_1)+\arg(z_2)$.

<a id="satz-43-fundamentalsatz-der-algebra"></a>
### Satz 4.3 (Fundamentalsatz der Algebra)

**Aussage:** $\mathbb{C}$ ist **algebraisch abgeschlossen**, d.h. jedes nicht-konstante Polynom $\sum_{k=0}^n a_kz^k$ hat mindestens eine Nullstelle in $\mathbb{C}$.

*(Hinweis: In der Vorlesung wird dieser Satz nur zitiert, nicht bewiesen — der natürliche Beweis benötigt entweder den Satz von Liouville [holomorphe, beschränkte Funktionen auf ganz $\mathbb{C}$ sind konstant] als Konsequenz des Cauchyschen Integralsatzes, oder ein rein algebraisches/topologisches Argument, das über den Stoff dieser Vorlesung hinausgeht.)*

<a id="definition-44-komplexe-differenzierbarkeit"></a>
### Definition 4.4 (Komplexe Differenzierbarkeit)

$D\subseteq\mathbb{C}$ offen, $f:D\to\mathbb{C}$. $f$ heißt **komplex differenzierbar** bei $a\in D$, falls
$$
\lim_{z\to a} \frac{f(z)-f(a)}{z-a} =: f'(a) \in \mathbb{C} \quad \text{existiert}.
$$

<a id="definition-46-holomorphie"></a>
### Definition 4.6 (Holomorphie)

Ist $f$ komplex differenzierbar für **alle** $z\in D$ ($D$ offen), heißt $f$ **analytisch** oder **holomorph** in $D$.

<a id="sätze-16"></a>
## Sätze

<a id="lemma-45-cauchy-riemann-gleichungen"></a>
### Lemma 4.5 (Cauchy-Riemann-Gleichungen)

**Aussage:** Sei $f:D\to\mathbb{C}$, $\hat f:D\to\mathbb{R}^2$ die zugehörige reelle Darstellung, $f(x+iy)=g(x,y)+ih(x,y)$. Dann ist $f$ komplex differenzierbar bei $a$ **genau dann**, wenn $\hat f$ (im gewöhnlichen $\mathbb{R}^2\to\mathbb{R}^2$-Sinne) differenzierbar bei $a$ ist **und** die **Cauchy-Riemann-Gleichungen** gelten:
$$
\frac{\partial g}{\partial x} = \frac{\partial h}{\partial y}, \qquad \frac{\partial g}{\partial y} = -\frac{\partial h}{\partial x}.
$$

**Bedeutung:** Dies ist der zentrale Satz des Kapitels — er übersetzt die abstrakte komplexe Differenzierbarkeit in eine konkret nachprüfbare Bedingung an die partiellen Ableitungen von Real- und Imaginärteil.

**Beweisidee** *(Beweisstil: Vergleich der Matrixdarstellung von $Df$ mit der Matrixdarstellung der Multiplikation mit einer komplexen Zahl)*

**Kern des Arguments:** Die reelle Ableitung $D\hat f(a)$ ist eine $2\times2$-Matrix $A=\begin{pmatrix}a_{11}&a_{12}\\a_{21}&a_{22}\end{pmatrix}$. Man zeigt: $\hat A(x+iy) := (a_{11}x+a_{12}y)+i(a_{21}x+a_{22}y)$ ist genau dann Multiplikation mit einer komplexen Zahl $c=a_{11}+ia_{21}$ (d.h. $\hat A(z)=cz$), wenn $a_{11}=a_{22}$ und $a_{21}=-a_{12}$ gilt (direktes Nachrechnen der Multiplikationsformel $cz=(a_{11}+ia_{21})(x+iy)=(a_{11}x-a_{21}y)+i(a_{21}x+a_{11}y)$ und Koeffizientenvergleich mit $A\begin{pmatrix}x\\y\end{pmatrix}$).

Komplexe Differenzierbarkeit bedeutet gerade, dass die beste lineare Approximation $D\hat f(a)$ diese spezielle Form hat (Multiplikation mit $c=f'(a)$) — und die Bedingungen $a_{11}=a_{22}$, $a_{21}=-a_{12}$ sind (mit $a_{11}=\partial g/\partial x$, $a_{12}=\partial g/\partial y$, $a_{21}=\partial h/\partial x$, $a_{22}=\partial h/\partial y$) exakt die Cauchy-Riemann-Gleichungen. $\blacksquare$

<a id="beispiele-18"></a>
## Beispiele

**Beispiel 1 (leicht):** Zeigen Sie, dass $f(z)=z^2$ holomorph ist: $f(x+iy)=(x+iy)^2 = (x^2-y^2)+i(2xy)$, also $g=x^2-y^2$, $h=2xy$. Prüfung: $\partial_xg=2x=\partial_yh$ ✓, $\partial_yg=-2y=-\partial_xh=-2y$ ✓. CR-Gleichungen erfüllt, $f$ ist überall holomorph (glatt, da $g,h$ Polynome).

**Beispiel 2 (mittel):** Zeigen Sie, dass $f(z)=\bar z$ **nirgends** holomorph ist: $g=x$, $h=-y$; $\partial_xg=1$, $\partial_yh=-1$ — $1\neq-1$, CR-Gleichungen verletzt überall.

**Beispiel 3 (schwer):** Sei $f$ holomorph auf einem Gebiet $D$ mit $f'(z)=0$ für alle $z\in D$ ($D$ zusammenhängend). Zeigen Sie $f$ ist konstant. *(Beweisidee: $f'=0 \Rightarrow$ nach CR-Gleichungen sind alle partiellen Ableitungen von $g,h$ Null $\Rightarrow$ $g,h$ lokal konstant $\Rightarrow$, da $D$ zusammenhängend, global konstant — Anwendung des Zwischenwertsatzes/Zusammenhangs aus Kapitel 1!)*

<a id="gegenbeispiele-18"></a>
## Gegenbeispiele

- **$f(z)=\bar z$:** siehe Beispiel 2 — reell differenzierbar (sogar $C^\infty$ als Abbildung $\mathbb{R}^2\to\mathbb{R}^2$), aber nirgends komplex differenzierbar. Dies zeigt eindrücklich, dass komplexe Differenzierbarkeit strikt stärker ist als reelle Differenzierbarkeit.
- **$f(z)=|z|^2 = z\bar z$:** $g=x^2+y^2$, $h=0$. CR: $\partial_xg=2x \stackrel{!}{=}\partial_yh=0$ — nur bei $x=0$ erfüllt; analog $\partial_yg=2y\stackrel{!}{=}-\partial_xh=0$ nur bei $y=0$. Also ist $f$ **nur** bei $z=0$ komplex differenzierbar, aber nirgends holomorph (Holomorphie erfordert eine ganze *offene* Umgebung, nicht nur einen isolierten Punkt!).

<a id="kurvenintegrale-in-mathbbc-und-der-cauchysche-integralsatz"></a>
## Kurvenintegrale in $\mathbb{C}$ und der Cauchysche Integralsatz

<a id="definition-410-komplexes-kurvenintegral"></a>
### Definition 4.10 (Komplexes Kurvenintegral)

Sei $\gamma$ Kurve in $\mathbb{C}$ mit $C^{(1)}$-Parametrisierung $g:[a,b]\to\mathbb{C}$, $f:D\to\mathbb{C}$, $\gamma\subseteq D$. Dann
$$
\int_\gamma f(z)\,dz := \int_a^b f(g(t))\,g'(t)\,dt \in \mathbb{C}.
$$

<a id="zusammenhang-mit-reellen-1-formen"></a>
### Zusammenhang mit reellen 1-Formen

Schreibt man $f=u+iv$, $z=x+iy$, so gilt (direktes Nachrechnen, Aufspalten in Real- und Imaginärteil):
$$
\int_\gamma f(z)\,dz = \int_\gamma \omega + i\int_\gamma\hat\omega, \qquad \omega := u\,dx-v\,dy, \qquad \hat\omega := v\,dx+u\,dy.
$$

**Ist $f$ holomorph**, so zeigt eine direkte Rechnung unter Verwendung der Cauchy-Riemann-Gleichungen, dass sowohl $\omega$ als auch $\hat\omega$ **geschlossene** 1-Formen (im Sinne von Kapitel 11!) sind:
$$
d\omega = \left(\frac{\partial(-v)}{\partial x}-\frac{\partial u}{\partial y}\right)dx\wedge dy \stackrel{\text{CR}}{=} \left(-\frac{\partial v}{\partial x}+\frac{\partial v}{\partial x}\right)dx\wedge dy = 0
$$
(unter Verwendung von $\partial u/\partial y = -\partial v/\partial x$, der zweiten CR-Gleichung); analog für $\hat\omega$.

<a id="satz-412-cauchyscher-integralsatz"></a>
### Satz 4.12 (Cauchyscher Integralsatz)

**Aussage:** Sei $f$ holomorph in einem **einfach zusammenhängenden** offenen Gebiet $D\subseteq\mathbb{C}$, $\gamma$ geschlossene Kurve in $D$. Dann
$$
\int_\gamma f(z)\,dz = 0.
$$

**Bedeutung:** Das zentrale Resultat der komplexen Analysis — es folgen daraus u.a. die Cauchysche Integralformel, die Existenz von Potenzreihenentwicklungen jeder holomorphen Funktion, der Satz von Liouville, und letztlich der Fundamentalsatz der Algebra. Dieser Satz markiert (auch in der zugrundeliegenden Vorlesung) einen geeigneten Abschlusspunkt des Semesters.

**Beweisstruktur** *(Beweisstil: Reduktion auf Kapitel 11 — Nachweis, dass $\omega,\hat\omega$ exakt sind, dann Anwendung von Satz 3.8)*

**Schritt 1 (Kernidee):** Nach obiger Rechnung sind $\omega,\hat\omega$ geschlossen. Da $D$ **einfach zusammenhängend** ist, sind $\omega,\hat\omega$ nach dem **Poincaré-Lemma** (Kapitel 11 — geschlossen $\Rightarrow$ exakt auf einfach zusammenhängenden Gebieten) beide **exakt**: Es existieren $U,V$ mit $\omega=DU$, $\hat\omega=DV$.

**Schritt 2 (Anwendung von Satz 3.8):** Da $\gamma$ geschlossen ist, folgt nach Satz 3.8 (Kapitel 11!) direkt $\int_\gamma\omega=0$ und $\int_\gamma\hat\omega=0$, also
$$
\int_\gamma f(z)\,dz = \int_\gamma\omega + i\int_\gamma\hat\omega = 0+i\cdot0 = 0. \qquad \blacksquare
$$

**Alternativer, direkter Beweisansatz (Goursat-Methode, in der Mitschrift begonnen):** Ein alternativer, von der Poincaré-Lemma-Technik unabhängiger Beweis (der historisch der ursprüngliche ist und ohne die Voraussetzung stetiger Ableitungen von $f$ auskommt — Satz von Goursat) funktioniert über eine **Rechteckszerlegung**: Man zerlegt ein Rechteck $R$, das die Kurve umschließt, in vier Teilrechtecke, zeigt, dass sich das Integral über den Rand von $R$ als Summe der Integrale über die Ränder der Teilrechtecke schreiben lässt (die inneren Kanten heben sich paarweise auf, da sie mit entgegengesetzter Orientierung durchlaufen werden), und führt einen Widerspruchsbeweis: Wäre $\left|\int_{\partial R}f\,dz\right| = M > 0$, so gibt es unter den vier Teilrechtecken mindestens eines, für das $|\int_{\partial R_i} f\,dz| \geq M/4$; iterativ verkleinert man so das Rechteck ($R \supset R_1 \supset R_2 \supset \dots$, mit $\mathrm{diam}(R_k)\to0$), bis sich die Rechtecke auf einen Punkt $z_0$ zusammenziehen — dort nutzt man die (komplexe!) Differenzierbarkeit von $f$ bei $z_0$, um zu zeigen, dass $\int_{\partial R_k}f\,dz$ tatsächlich schneller als die Fehlerabschätzung aus der Konstruktion gegen $0$ geht — Widerspruch zu $M>0$.

> **Anmerkung zur Vollständigkeit dieses Skripts:** Die ursprüngliche Vorlesungsmitschrift bricht den Beweis exakt an dieser Stelle ab (letzte Notiz: *"Cauchy bis hier"*). Der oben skizzierte **Poincaré-Lemma-Ansatz** (Schritt 1–2) ist mathematisch vollständig und schließt die in der Mitschrift entstandene Lücke unter der (in der Vorlesung ohnehin über den Satz von Schwarz implizit vorausgesetzten) zusätzlichen Voraussetzung, dass $f\in C^1$ ist (sodass $u,v$ stetige partielle Ableitungen haben und Lemma 3.5/Poincaré anwendbar sind). Der **Satz von Goursat** ist die stärkere, technisch aufwendigere Version, die *ohne* diese Zusatzvoraussetzung auskommt (sie zeigt sogar nachträglich, dass jede holomorphe Funktion automatisch $C^\infty$ ist) — dies geht über den in der Mitschrift dokumentierten Vorlesungsstoff hinaus, ist aber der historisch korrekte und in der Standardliteratur (z.B. Freitag/Busam, *Funktionentheorie*) zu findende vollständige Beweis.

<a id="vergleichstabelle-reelle-vs-komplexe-differenzierbarkeit"></a>
## Vergleichstabelle: Reelle vs. komplexe Differenzierbarkeit

| Eigenschaft | Reell diffbar ($\mathbb{R}^2\to\mathbb{R}^2$) | Komplex diffbar |
|---|---|---|
| Lineare Approximation $Df(a)$ | Beliebige $2\times2$-Matrix | Nur Matrizen der Form $\begin{pmatrix}a&-b\\b&a\end{pmatrix}$ (Drehstreckung) |
| Zusätzliche Bedingung | — | Cauchy-Riemann-Gleichungen |
| Aus einmaliger Diffbarkeit folgt... | nichts Weiteres | (nicht in dieser Vorlesung bewiesen, aber Standardfakt der Funktionentheorie:) automatisch $C^\infty$ und lokale Potenzreihenentwicklung |
| Beispiel, das die eine, aber nicht die andere Eigenschaft hat | $f(z)=\bar z$ | — (komplex diffbar $\Rightarrow$ reell diffbar gilt immer, Lemma 4.5) |

<a id="typische-klausuraufgaben-19"></a>
## Typische Klausuraufgaben

| Aufgabentyp | Erkennungsmerkmal | Strategie |
|---|---|---|
| "Ist $f$ holomorph?" | Explizite komplexe Funktion | $g=\mathrm{Re}(f)$, $h=\mathrm{Im}(f)$ bestimmen, Cauchy-Riemann-Gleichungen direkt nachrechnen |
| "Wo ist $f$ komplex differenzierbar?" | Funktion, die CR nur an isolierten Punkten erfüllt | CR-Gleichungen als Gleichungssystem lösen, Lösungsmenge angeben (Achtung: Holomorphie erfordert eine ganze *Umgebung*, nicht nur isolierte Punkte!) |
| "Berechnen Sie $\int_\gamma f(z)\,dz$" | Explizite Kurve, holomorphe oder nicht-holomorphe Funktion | Bei Holomorphie auf einfach zusammenhängendem Gebiet: Cauchyscher Integralsatz $\Rightarrow 0$; sonst direkt parametrisieren und integrieren |

<a id="typische-fehler-19"></a>
## Typische Fehler

1. **Reelle und komplexe Differenzierbarkeit verwechseln** — die Existenz aller partiellen Ableitungen (reell) reicht nicht, es müssen zusätzlich die CR-Gleichungen gelten.
2. **Cauchyschen Integralsatz ohne Prüfung des einfachen Zusammenhangs anwenden** — z.B. bei Funktionen mit Polstellen im umschlossenen Gebiet (wie $f(z)=1/z$ bei $z=0$) gilt der Satz **nicht** (analoges Gegenbeispiel zur Winkelform aus Kapitel 11!).
3. **Holomorphie an einem einzelnen Punkt mit Holomorphie in einer Umgebung verwechseln** (siehe Gegenbeispiel $f(z)=|z|^2$).

<a id="verbindungen-20"></a>
## Verbindungen

- Lemma 4.5 (Cauchy-Riemann) ist eine direkte Anwendung der reellen Differentialrechnung aus Kapitel 7 (Jacobi-Matrix), spezialisiert auf $\mathbb{R}^2\to\mathbb{R}^2$.
- Der **Cauchysche Integralsatz** ist strukturell **identisch** mit Satz 3.8/3.8a aus Kapitel 11 (Wegunabhängigkeit exakter Formen) — die gesamte komplexe Analysis in diesem Kapitel baut auf der reellen Theorie der Kurvenintegrale und Differentialformen auf.
- Das Gegenbeispiel $f(z)=1/z$ (Integral über den Einheitskreis $=2\pi i$) ist exakt die komplexe Fassung der Winkelform aus Kapitel 11 — beide illustrieren dasselbe Phänomen: geschlossen, aber nicht exakt, wegen fehlendem einfachen Zusammenhang.

<a id="zusammenfassung-kapitel-12"></a>
## Zusammenfassung Kapitel 12

- Komplexe Differenzierbarkeit ist strikt stärker als reelle Differenzierbarkeit von $\mathbb{R}^2\to\mathbb{R}^2$: Sie erfordert zusätzlich die **Cauchy-Riemann-Gleichungen** $\partial_xg=\partial_yh$, $\partial_yg=-\partial_xh$ (Lemma 4.5).
- Holomorphe Funktionen $u+iv$ erzeugen **geschlossene** reelle 1-Formen $u\,dx-v\,dy$ und $v\,dx+u\,dy$ — via CR-Gleichungen äquivalent zum Satz von Schwarz.
- Der **Cauchysche Integralsatz** (Satz 4.12) — Kernresultat der komplexen Analysis — folgt direkt aus der Theorie exakter/geschlossener Formen aus Kapitel 11, angewendet auf einfach zusammenhängende Gebiete.

---

<a id="gesamtübersicht-der-rote-faden-der-vorlesung"></a>
# Gesamtübersicht: Der rote Faden der Vorlesung

Mit Abschluss von Kapitel 12 ist die Rekonstruktion der Vorlesung vollständig. Der innere Zusammenhang, den dieses Skript sichtbar gemacht hat, lässt sich wie folgt zusammenfassen:

$$
\underbrace{\text{Topologie}}_{\text{Kap. 1}} \to \underbrace{\text{Metrik}}_{\text{Kap. 2}} \to \underbrace{\text{Banachraum}}_{\text{Kap. 3}} \to \underbrace{\text{Ableitung, Umkehrsatz}}_{\text{Kap. 3–4}} \to \underbrace{\text{Taylor, Hilbertraum}}_{\text{Kap. 5–6}} \to \underbrace{\text{Extrema}}_{\text{Kap. 7–8}}
$$
$$
\to \underbrace{\text{Approximation}}_{\text{Kap. 9}} \to \underbrace{\text{Integration}}_{\text{Kap. 10}} \to \underbrace{\text{Kurvenintegrale}}_{\text{Kap. 11}} \to \underbrace{\text{Komplexe Analysis}}_{\text{Kap. 12}}
$$

**Die drei wichtigsten Querverbindungen, die dieses Skript explizit gemacht hat** (und die in der ursprünglichen Mitschrift nur implizit oder gar nicht sichtbar waren):

1. **Gram-Schmidt (Kap. 6) → Transformationssatz (Kap. 10):** Die Identifikation von Volumen und Determinante im Beweis von Lemma 2.10 beruht direkt auf dem Gram-Schmidt-Verfahren.
2. **Satz von Schwarz (Kap. 5) → Exakte Formen (Kap. 11) → Cauchyscher Integralsatz (Kap. 12):** Eine einzige Symmetrieeigenschaft der zweiten Ableitung zieht sich durch drei Kapitel und kulminiert im zentralen Satz der komplexen Analysis.
3. **Satz über implizite Funktionen (Kap. 4) → Tangentialraum von Mannigfaltigkeiten (Kap. 8) → Lagrange-Multiplikatoren:** Die abstrakte Auflösbarkeitstheorie wird zum konkreten Rechenwerkzeug für Optimierung unter Nebenbedingungen.

Für die Klausurvorbereitung empfiehlt sich, diese drei Verbindungslinien besonders zu verinnerlichen — sie zeigen, dass die Vorlesung kein "Sammelsurium" von Einzelresultaten ist, sondern ein zusammenhängendes System, in dem wenige tiefe Ideen (Vollständigkeit, lineare Approximation, Symmetrie zweiter Ableitungen) immer wieder in neuen Gewändern auftreten.

---

*Ende des Skripts. Alle sechs Teile (Kapitel 1–12) bilden zusammen die vollständige, bereinigte und ergänzte Rekonstruktion der Vorlesung.*



---

<a id="physik-ii-vollständiges-skript"></a>
# Physik II — Vollständiges Skript
<a id="teil-i-mechanik-der-fluide-und-wärmelehre"></a>
## Teil I: Mechanik der Fluide und Wärmelehre

> Dieses Skript ist die vollständige, fehlerbereinigte und lehrbuchartig ausgearbeitete Rekonstruktion der Vorlesung. Es ersetzt die Mitschrift und ist so geschrieben, dass kein zusätzliches Lehrbuch nötig sein sollte.

---

<a id="inhaltsverzeichnis-teil-i"></a>
# Inhaltsverzeichnis Teil I

1. Strömende Flüssigkeiten und Gase
2. Kinetische Gastheorie und Temperatur
3. Transportphänomene
4. Wärme, Arbeit und der 1. Hauptsatz der Thermodynamik
5. Kreisprozesse und der 2. Hauptsatz der Thermodynamik

---

<a id="kapitel-1-strömende-flüssigkeiten-und-gase"></a>
# Kapitel 1: Strömende Flüssigkeiten und Gase

<a id="motivation-21"></a>
## Motivation

In der Mechanik des Massenpunkts und starrer Körper beschreiben wir Bewegung durch die Trajektorie einzelner Objekte. Bei einer Flüssigkeit oder einem Gas ist das unmöglich — ein Liter Wasser enthält etwa $3,3\cdot 10^{25}$ Moleküle. Wir brauchen daher eine **Feldbeschreibung**: Statt "wo ist Teilchen $i$ zur Zeit $t$?" fragen wir "wie groß ist Geschwindigkeit, Druck und Dichte an jedem Ort $\vec r$ zur Zeit $t$?".

Historisch entstand diese Denkweise aus sehr praktischen Problemen: Wie schnell fließt Wasser aus einem Loch im Fass (Torricelli, 17. Jh.)? Wie trägt eine Tragfläche (Bernoulli, 18. Jh.)? Wie groß ist der Druckverlust in einer Rohrleitung (Hagen, Poiseuille, 19. Jh.)? Die in diesem Kapitel entwickelten Gesetze sind Spezialfälle der viel allgemeineren Navier-Stokes-Gleichungen, die wir hier bewusst nicht vollständig herleiten — sie sind Gegenstand eigener Vorlesungen (Strömungsmechanik). Wir beschränken uns auf die Fälle, die mit Erhaltungssätzen (Masse, Energie) und einfachen empirischen Ansätzen (Newtonsche Reibung) lösbar sind.

<a id="intuition-21"></a>
## Intuition

Stell dir Wasser als ein Bündel dünner "Stromfäden" vor, die nie beginnen oder enden (außer an Quellen/Senken) und sich nie kreuzen (bei stationärer Strömung). Wo die Fäden eng zusammenrücken (enges Rohr), muss das Wasser schneller fließen — genau wie eine Menschenmenge, die sich durch eine Engstelle drängt, dort automatisch schneller läuft, wenn niemand verloren gehen darf.

Die Bernoulli-Gleichung ist im Kern eine **Energiebilanz entlang eines Stromfadens**: Geschwindigkeit "kostet" Druck. Wenn eine Flüssigkeit beschleunigt wird (weil das Rohr enger wird), muss diese kinetische Energie irgendwoher kommen — sie wird aus dem statischen Druck "bezahlt". Das ist derselbe Mechanismus, der ein Blatt Papier nach oben zieht, wenn man von oben darüber bläst: schnellere Luft = geringerer Druck.

Reale Flüssigkeiten haben zusätzlich **innere Reibung** (Viskosität): benachbarte Flüssigkeitsschichten, die sich unterschiedlich schnell bewegen, üben Scherkräfte aufeinander aus — man kann sich das wie viele dünne Kartenstapel vorstellen, die übereinander verschoben werden und sich dabei gegenseitig bremsen.

<a id="formale-definitionen-21"></a>
## Formale Definitionen

**Definition 1.1 (Stromdichte, Geschwindigkeitsfeld).**
Ein Fluid wird durch ein Geschwindigkeitsfeld $\vec v(\vec r, t)$ und ein Dichtefeld $\rho(\vec r,t)$ beschrieben. Die **Stromdichte** ist
$$\vec j(\vec r,t) := \rho(\vec r,t)\,\vec v(\vec r,t), \qquad [\vec j] = \frac{\text{kg}}{\text{m}^2\,\text{s}}.$$

**Definition 1.2 (Stationäre Strömung).**
Eine Strömung heißt *stationär*, wenn $\partial \vec v/\partial t = 0$ und $\partial \rho/\partial t = 0$ überall gilt — das Geschwindigkeitsfeld ändert sich nicht mit der Zeit (wohl aber i. A. mit dem Ort).

**Definition 1.3 (Volumen- bzw. Massendurchfluss).**
Für eine Querschnittsfläche $A$ senkrecht zur Strömung:
$$\dot V := \frac{dV}{dt} = A\cdot v, \qquad \dot m := \frac{dm}{dt} = \rho A v.$$

**Definition 1.4 (Divergenz eines Vektorfeldes).**
$$\operatorname{div}\vec j := \nabla\cdot\vec j = \frac{\partial j_x}{\partial x}+\frac{\partial j_y}{\partial y}+\frac{\partial j_z}{\partial z}.$$
Die Divergenz misst die "Quellstärke" eines Feldes an einem Punkt: Wie viel mehr fließt lokal heraus als hinein?

**Definition 1.5 (Viskosität).**
Für eine Scherströmung mit Geschwindigkeitsgefälle $dv/dz$ senkrecht zur Strömungsrichtung ist die Scherkraft pro Fläche (Schubspannung) proportional zum Gradienten:
$$\frac{F}{A} = \eta\,\frac{dv}{dz} \qquad \text{(Newtonsches Reibungsgesetz)},$$
mit der **dynamischen Viskosität** $\eta$, $[\eta] = \text{Pa}\cdot\text{s} = 10\ \text{Poise}$.

**Definition 1.6 (Reynoldszahl).**
$$\mathrm{Re} := \frac{\rho\, v\, \Delta z}{\eta},$$
eine dimensionslose Kennzahl, die das Verhältnis von Trägheitskräften zu Reibungskräften angibt ($\Delta z$: charakteristische Länge des Systems, z. B. Rohrdurchmesser).

<a id="eigenschaften-17"></a>
## Eigenschaften

| Eigenschaft | Aussage | Kurzbegründung |
|---|---|---|
| Masseerhaltung | $\operatorname{div}\vec j = -\dot\rho$ | Folgt aus Gauß'schem Satz + Massebilanz über beliebiges Volumen |
| Inkompressibilität | $\operatorname{div}\vec v = 0$ | Für Flüssigkeiten ($\rho=\text{const}$) folgt dies direkt aus obiger Gleichung |
| Bernoulli gilt nur | entlang eines Stromfadens, reibungsfrei, stationär, inkompressibel | Energieerhaltung wird nur *entlang* eines Fadens formuliert, nicht global |
| Laminar vs. turbulent | $\mathrm{Re} < \mathrm{Re}_{krit}$: laminar; sonst turbulent | Empirisches Kriterium, $\mathrm{Re}_{krit}\approx 2300$ im Rohr, $\approx 100$ um ein Hindernis |
| Viskosität temperaturabhängig | $\eta$ sinkt bei Flüssigkeiten mit $T$, steigt bei Gasen mit $T$ | Flüssigkeiten: thermische Bewegung schwächt Bindungen; Gase: mehr Impulsaustausch bei höherer Molekülgeschwindigkeit |

<a id="sätze-17"></a>
## Sätze

<a id="satz-11-kontinuitätsgleichung"></a>
### Satz 1.1 (Kontinuitätsgleichung)

**Aussage:**
$$\operatorname{div}\vec j(\vec r,t) = -\frac{\partial \rho}{\partial t}(\vec r,t).$$
Für inkompressible, stationäre Strömung folgt speziell $A\cdot v = \text{const}$ entlang eines Stromröhrchens.

**Voraussetzungen:** Keine — die Kontinuitätsgleichung ist eine reine Konsequenz der Massenerhaltung, gilt also immer (für Massenstromdichte; analoge Formen gelten für jede Erhaltungsgröße).

**Bedeutung:** Sie ist das fluidmechanische Analogon zur Ladungserhaltung in der Elektrodynamik (vgl. Kapitel 9) — "was nicht erzeugt oder vernichtet wird, kann nur durch die Oberfläche eines Volumens ab- oder zufließen."

**Intuition:** Stell dir ein beliebiges, festes Kontrollvolumen $V$ vor. Die Masse darin kann sich nur ändern, wenn Masse durch die Oberfläche $S$ hinein- oder herausströmt. Es gibt keine "Zauberei" in der Mitte, die Masse erschafft.

**Konsequenzen:** Für eine inkompressible Strömung im Rohr mit veränderlichem Querschnitt: $A_1 v_1 = A_2 v_2$ — verengt sich das Rohr, muss die Geschwindigkeit steigen.

<a id="beweis-von-satz-11"></a>
### Beweis von Satz 1.1

**Beweisstil:** Direkter Beweis über ein Kontrollvolumen (Bilanzargument) + Satz von Gauß.

Sei $V$ ein beliebiges, zeitlich festes Volumen mit Rand $S = \partial V$. Die Masse in $V$ ist $m(t) = \int_V \rho\, dV$. Die zeitliche Änderung ist
$$\frac{dm}{dt} = \int_V \frac{\partial \rho}{\partial t}\, dV.$$
Andererseits kann sich die Masse nur durch den Fluss über den Rand ändern. Der Massenstrom, der pro Zeit durch ein Flächenelement $d\vec A$ (nach außen orientiert) austritt, ist $\vec j\cdot d\vec A$. Also
$$\frac{dm}{dt} = -\oint_S \vec j\cdot d\vec A$$
(Minuszeichen, weil Ausströmen die Masse in $V$ *verringert*). Mit dem Satz von Gauß,
$$\oint_S \vec j\cdot d\vec A = \int_V \operatorname{div}\vec j\, dV,$$
folgt
$$\int_V \frac{\partial\rho}{\partial t}\, dV = -\int_V \operatorname{div}\vec j\, dV.$$
Da $V$ *beliebig* gewählt war, müssen die Integranden punktweise übereinstimmen:
$$\operatorname{div}\vec j = -\frac{\partial\rho}{\partial t}. \qquad \blacksquare$$

<a id="satz-12-bernoulli-gleichung"></a>
### Satz 1.2 (Bernoulli-Gleichung)

**Aussage:** Für eine stationäre, reibungsfreie, inkompressible Strömung entlang eines Stromfadens gilt
$$p + \rho g h + \tfrac{1}{2}\rho v^2 = \text{const}.$$

**Voraussetzungen:** stationär, reibungsfrei (keine Viskosität), inkompressibel ($\rho = \text{const}$), entlang *eines* Stromfadens.

**Bedeutung:** Energieerhaltung für Fluide: statischer Druck + hydrostatischer Druck + dynamischer Druck ist entlang eines Stromfadens konstant.

**Intuition:** Multipliziert man mit einem Volumenelement $dV$, so wird jeder Term zu einer Energie: $p\,dV$ ist die Verschiebearbeit (Druckkraft mal Weg), $\rho g h\, dV$ die potentielle Energie, $\tfrac12 \rho v^2\, dV$ die kinetische Energie. Die Gleichung ist also nichts anderes als der Energieerhaltungssatz der Mechanik, angewendet auf ein mitbewegtes Fluidelement.

**Konsequenzen:** An einer Engstelle ($v$ groß) ist $p$ klein — das erklärt Auftrieb an Tragflächen (näherungsweise, s. u.) und den Venturi-Effekt.

<a id="beweis-von-satz-12"></a>
### Beweis von Satz 1.2

**Beweisstil:** Energiebilanz (Arbeit-Energie-Satz), direkter Beweis.

Betrachte ein Fluidelement, das sich entlang eines Stromfadens von Punkt 1 (Querschnitt $A_1$, Geschwindigkeit $v_1$, Druck $p_1$) zu Punkt 2 bewegt. In der Zeit $dt$ tritt bei 1 ein Volumen $dV = A_1 v_1\, dt$ ein und bei 2 (wegen Kontinuität) dasselbe Volumen $dV$ aus.

Die am Fluid *verrichtete* Arbeit durch die Druckkraft bei 1 ist
$$dW_1 = F_1\, dx_1 = p_1 A_1 \cdot v_1\, dt = p_1\, dV,$$
und die *vom* Fluid gegen den Druck bei 2 verrichtete Arbeit ist $dW_2 = p_2\, dV$. Die Nettoarbeit am System ist also $dW_1 - dW_2 = (p_1-p_2)\,dV$.

Nach dem Arbeit-Energie-Satz muss diese Nettoarbeit gleich der Änderung der kinetischen (und ggf. potentiellen) Energie des herausgeschobenen Volumenelements sein:
$$(p_1-p_2)\,dV = dE_{kin,2}-dE_{kin,1} = \tfrac12 \rho\, dV\,(v_2^2-v_1^2)$$
(für horizontale Strömung; bei Höhenunterschied kommt zusätzlich $\rho g\,dV\,(h_2-h_1)$ hinzu). Division durch $dV$ und Umsortieren:
$$p_1 + \tfrac12\rho v_1^2 = p_2 + \tfrac12 \rho v_2^2 \quad(+\rho g h_1 = \dots + \rho g h_2).$$
Da 1 und 2 beliebige Punkte auf dem Stromfaden waren, ist $p+\rho gh + \tfrac12\rho v^2$ entlang des gesamten Fadens konstant. $\blacksquare$

<a id="satz-13-hagen-poiseuille-gesetz"></a>
### Satz 1.3 (Hagen-Poiseuille-Gesetz)

**Aussage:** Für eine laminare, stationäre Strömung einer viskosen Flüssigkeit durch ein zylindrisches Rohr der Länge $\ell$, Radius $R$, bei Druckdifferenz $\Delta p$, ist das Geschwindigkeitsprofil parabelförmig,
$$v(r) = \frac{\Delta p}{4\eta \ell}\left(R^2 - r^2\right),$$
und der Volumendurchsatz
$$\frac{\dot V}{\phantom{}} = \frac{\pi \Delta p}{8\eta \ell} R^4.$$

**Voraussetzungen:** laminare Strömung ($\mathrm{Re}<\mathrm{Re}_{krit}$), Newtonsches Fluid, Haftbedingung an der Rohrwand ($v(R)=0$), stationär.

**Bedeutung:** Der Durchsatz skaliert mit $R^4$ — verdoppelt man den Rohrdurchmesser, versechzehnfacht sich (bei gleichem $\Delta p$) der Durchsatz. Das ist medizinisch/technisch enorm wichtig (z. B. Gefäßverengung).

**Intuition:** Die treibende Druckkraft auf einen Fluidzylinder vom Radius $r$ wird durch die Reibungskraft an dessen Mantelfläche balanciert — je weiter außen, desto größer die Mantelfläche und desto stärker die Bremsung, daher das parabolische Profil mit Maximum in der Rohrmitte.

<a id="beweis-von-satz-13-beweisidee-da-nicht-vollständig-aus-den-grundgleichungen-hergeleitet-sondern-über-kräftebilanz"></a>
### Beweis von Satz 1.3 (Beweisidee, da nicht vollständig aus den Grundgleichungen hergeleitet, sondern über Kräftebilanz)

**Beweisstil:** Kräftebilanz an einem Fluidzylinder (Gleichgewichtsbetrachtung).

Betrachte einen koaxialen Fluidzylinder vom Radius $r$ und Länge $dz$. Die Druckkraft treibt ihn an: $F_{Druck} = \Delta p\cdot \pi r^2$. Die Reibungskraft an seiner Mantelfläche $2\pi r\, dz$ bremst ihn gemäß Newtonschem Reibungsgesetz: $F_{Reib} = -\eta\, \dfrac{dv}{dr}\cdot 2\pi r\, dz$. Im stationären Zustand ist die Summe der Kräfte null:
$$\Delta p\, \pi r^2 = -\eta\,2\pi r\,dz\,\frac{dv}{dr} \;\Longrightarrow\; \frac{dv}{dr} = -\frac{\Delta p}{2\eta\, dz}\, r.$$
Integration mit Randbedingung $v(R)=0$ liefert
$$v(r) = \frac{\Delta p}{4\eta \ell}(R^2-r^2).$$
Den Gesamtdurchsatz erhält man durch Integration über alle konzentrischen Ringe:
$$\dot V = \int_0^R v(r)\cdot 2\pi r\, dr = \frac{\pi\Delta p}{8\eta\ell}R^4$$
(Rechendetail: Substitution und Standardintegral $\int_0^R (R^2-r^2)r\,dr = R^4/4$). $\blacksquare$

<a id="satz-14-stokessches-gesetz"></a>
### Satz 1.4 (Stokes'sches Gesetz)

**Aussage:** Die Widerstandskraft auf eine Kugel vom Radius $r$, die sich mit konstanter Geschwindigkeit $\bar v$ durch eine viskose Flüssigkeit bewegt (bei kleiner Reynoldszahl), ist
$$F_W = 6\pi \eta r \bar v.$$

**Voraussetzungen:** kleine Reynoldszahl (schleichende Strömung, keine Turbulenz), kugelförmiger Körper, Newtonsches Fluid.

**Bedeutung:** Grundlage des Kugelfallviskosimeters zur Messung von $\eta$.

**Beweisstil:** Dieses Gesetz erfordert die vollständige Lösung der Navier-Stokes-Gleichungen für schleichende Strömung um eine Kugel (Stokes 1851) — **kein** elementarer Beweis mit den Mitteln dieser Vorlesung möglich. Wir übernehmen das Ergebnis als gegeben (so auch in der Originalvorlesung explizit vermerkt).

**Konsequenz — Sedimentationsgeschwindigkeit:** Im Kräftegleichgewicht (Gewichtskraft − Auftrieb = Widerstand) für eine Kugel der Dichte $\rho_K$ in einer Flüssigkeit der Dichte $\rho_{Fl}$:
$$(\rho_K-\rho_{Fl})\,\tfrac43\pi r^3\, g = 6\pi\eta r\bar v \;\Longrightarrow\; \bar v = \frac{2}{9}\frac{(\rho_K-\rho_{Fl})\,g}{\eta}\, r^2.$$
Da $\bar v \propto r^2$, fällt eine größere Kugel überproportional schneller — daher eignen sich zwei verschieden große Kugeln zur Viskositätsbestimmung.

<a id="algorithmen-9"></a>
## Algorithmen

Kapitel 1 enthält keine klassischen Algorithmen im informatischen Sinn, aber eine **standardisierte Lösungsstrategie** für Strömungsaufgaben, die wie ein Algorithmus behandelt werden sollte:

**"Rezept" zur Lösung von Strömungsaufgaben**

- **Motivation:** Strömungsaufgaben in Klausuren folgen fast immer demselben Muster; ein festes Vorgehen verhindert, die falsche Gleichung (Bernoulli vs. Hagen-Poiseuille) anzuwenden.
- **Idee:** Zuerst klären, ob Reibung relevant ist (→ Hagen-Poiseuille/Stokes) oder vernachlässigbar (→ Bernoulli/Kontinuität).
- **Voraussetzungen:** Geometrie und gegebene Größen (Querschnitte, Drücke, Geschwindigkeiten) müssen identifizierbar sein.
- **Pseudocode:**
```
EINGABE: Strömungsproblem
1. Bestimme Reynoldszahl (falls η gegeben) oder prüfe Aufgabentext auf
   "reibungsfrei" / "ideal" vs. "viskos" / "zäh"
2. WENN reibungsfrei:
   a. Wende Kontinuitätsgleichung an: A1 v1 = A2 v2
   b. Wende Bernoulli-Gleichung zwischen zwei Punkten an
   c. Löse das (i. A. lineare) Gleichungssystem nach der gesuchten Größe
3. WENN viskos UND Rohrströmung:
   a. Prüfe laminar (Re < Re_krit)
   b. Wende Hagen-Poiseuille-Gesetz an
4. WENN viskos UND Kugel in Flüssigkeit:
   a. Wende Stokes'sches Gesetz + Kräftegleichgewicht an
AUSGABE: gesuchte Größe (v, p, Q, η, ...)
```
- **Mathematische Beschreibung:** Fallunterscheidung nach dominierendem physikalischem Mechanismus (Trägheit vs. Reibung), quantifiziert durch $\mathrm{Re}$.
- **Laufzeit / Speicherbedarf:** nicht anwendbar (kein numerischer Algorithmus).
- **Korrektheitsidee:** Jeder Fall entspricht einer separat bewiesenen Erhaltungsgleichung (Sätze 1.1–1.4); die Fallunterscheidung stellt sicher, dass die Voraussetzungen des jeweils verwendeten Satzes erfüllt sind.
- **Typische Anwendungen:** Ausflussgeschwindigkeit aus Behältern, Venturi-Rohr, Blutfluss in Gefäßen, Tragflächenauftrieb (näherungsweise).
- **Typische Fehler:** Bernoulli wird auf viskose Strömungen angewendet (verboten!), oder Hagen-Poiseuille wird für turbulente Strömungen benutzt (nur für laminar gültig).

<a id="beispiele-19"></a>
## Beispiele

**Beispiel 1 (leicht):** Wasser fließt durch ein Rohr, das sich von $A_1 = 4\,\text{cm}^2$ auf $A_2 = 1\,\text{cm}^2$ verjüngt. Bei $v_1 = 2\,\text{m/s}$: Wie groß ist $v_2$?
*Lösung:* $A_1 v_1 = A_2 v_2 \Rightarrow v_2 = v_1 A_1/A_2 = 2\cdot 4 = 8\,\text{m/s}$.

**Beispiel 2 (mittel):** Aus einem großen, offenen Behälter mit Wasserstand $h$ über einem kleinen Loch fließt Wasser aus. Wie groß ist die Ausflussgeschwindigkeit (Torricelli)?
*Lösung:* Bernoulli zwischen Wasseroberfläche (Index 1, $v_1\approx 0$, $p_1 = p_{atm}$, Höhe $h$) und Loch (Index 2, Höhe 0, $p_2 = p_{atm}$):
$$p_{atm} + \rho g h = p_{atm} + \tfrac12 \rho v_2^2 \;\Rightarrow\; v_2 = \sqrt{2gh}.$$

**Beispiel 3 (mittel):** Blut ($\eta \approx 3\cdot 10^{-3}\,\text{Pa s}$) fließt durch ein Blutgefäß der Länge $\ell = 5\,\text{cm}$, Radius $R = 1\,\text{mm}$, bei Druckdifferenz $\Delta p = 500\,\text{Pa}$. Berechne den Volumendurchsatz.
*Lösung:* Hagen-Poiseuille: $\dot V = \dfrac{\pi \Delta p R^4}{8\eta\ell} = \dfrac{\pi\cdot 500\cdot (10^{-3})^4}{8\cdot 3\cdot10^{-3}\cdot 0{,}05} \approx 1{,}3\cdot 10^{-6}\,\text{m}^3/\text{s}$.

**Beispiel 4 (schwer):** Zwei Kugeln (Radius $1\,\text{mm}$ und $2\,\text{mm}$, gleiches Material) fallen in Öl. Um welchen Faktor ist die größere schneller?
*Lösung:* $\bar v \propto r^2 \Rightarrow$ Faktor $= (2/1)^2 = 4$.

**Beispiel 5 (schwer, kombiniert):** Ein Venturi-Rohr wird zur Durchflussmessung genutzt. Am weiten Teil ($A_1=10\,\text{cm}^2$) misst man $p_1 = 200\,\text{kPa}$, am engen Teil ($A_2=2\,\text{cm}^2$) $p_2=150\,\text{kPa}$. Dichte $\rho=1000\,\text{kg/m}^3$. Bestimme $\dot V$.
*Lösung:* Aus Kontinuität $v_1 = (A_2/A_1)v_2$. Bernoulli: $p_1+\tfrac12\rho v_1^2 = p_2 + \tfrac12\rho v_2^2$. Einsetzen und nach $v_2$ auflösen:
$$v_2 = \sqrt{\frac{2(p_1-p_2)}{\rho\,[1-(A_2/A_1)^2]}} = \sqrt{\frac{2\cdot 50000}{1000\cdot(1-0{,}04)}} \approx 10{,}2\,\text{m/s},$$
$$\dot V = A_2 v_2 = 2\cdot10^{-4}\cdot10{,}2 \approx 2{,}0\cdot10^{-3}\,\text{m}^3/\text{s}.$$

<a id="gegenbeispiele-19"></a>
## Gegenbeispiele

- **Bernoulli funktioniert NICHT** bei turbulenter Strömung (Energie wird dissipativ in Wärme/Wirbel umgewandelt, ist also entlang des "Stromfadens" nicht mehr erhalten) und **nicht** bei kompressiblen Gasen mit großen Geschwindigkeitsänderungen (dann muss $\rho(p)$ berücksichtigt werden — Gasdynamik).
- **Hagen-Poiseuille funktioniert NICHT** für turbulente Strömung ($\mathrm{Re}>\mathrm{Re}_{krit}\approx 2300$) — der Durchsatz wächst dann nicht mehr linear mit $\Delta p$, sondern langsamer (ca. $\sqrt{\Delta p}$), da Turbulenz zusätzlichen Widerstand erzeugt.
- **Stokes'sches Gesetz funktioniert NICHT** für große, schnell fallende Körper (großes $\mathrm{Re}$) — dort dominiert der Trägheitswiderstand ($F\propto v^2$, Newton-Widerstand) statt des viskosen Widerstands ($F\propto v$).

<a id="typische-klausuraufgaben-20"></a>
## Typische Klausuraufgaben

- **Erkennungsmerkmal "reibungsfrei/ideal":** → Bernoulli + Kontinuität kombinieren. Strategie: immer zwei Punkte auf demselben Stromfaden identifizieren, Bernoulli dort ansetzen.
- **Erkennungsmerkmal "durch ein Rohr/eine Kapillare", Viskosität gegeben:** → Hagen-Poiseuille. Achtung auf $R^4$-Abhängigkeit bei Vergleichsaufgaben.
- **Erkennungsmerkmal "Kugel fällt/steigt in Flüssigkeit", "Viskosimeter":** → Stokes + Kräftegleichgewicht (Gewicht = Auftrieb + Reibung).
- **Kombinationsaufgaben:** Ausflussgeschwindigkeit + Reichweite eines Strahls (Bernoulli liefert $v$, dann Wurfparabel aus Mechanik I).

<a id="typische-fehler-20"></a>
## Typische Fehler

1. Bernoulli wird verwendet, obwohl Reibung explizit erwähnt ist (Fehler: Voraussetzung ignoriert).
2. Verwechslung von $A_1v_1=A_2v_2$ (Kontinuität, gilt für inkompressibel) mit einer Impuls- oder Energiegleichung.
3. Vorzeichenfehler bei der Höhenkorrektur in Bernoulli (welcher Punkt liegt höher?).
4. Vergessen, dass Hagen-Poiseuille nur für **laminare** Strömung gilt — Reynoldszahl nicht geprüft.
5. Stokes'sches Gesetz mit dem *Radius* statt dem *Durchmesser* verwechseln (Faktor 2 bzw. 4 Fehler in Endergebnis).

<a id="verbindungen-21"></a>
## Verbindungen

- Die **Kontinuitätsgleichung** (Satz 1.1) ist strukturell identisch mit der **Ladungserhaltung** in der Elektrodynamik (Kapitel 9, $\operatorname{div}\vec j = -\dot\rho$) — dasselbe mathematische Muster (lokale Erhaltungsgröße + Fluss) taucht dort wieder auf.
- Der **Satz von Gauß**, hier zum ersten Mal verwendet, ist zentrales Werkzeug in der **Elektrostatik** (Gauß'sches Gesetz, Kapitel 6).
- Die **Reynoldszahl** und das Konzept "empirischer dimensionsloser Kennzahlen" begegnet uns in ähnlicher Form nicht wieder in diesem Kurs, ist aber grundlegend für weiterführende Strömungslehre-Vorlesungen.
- Die **Viskosität** als Transportphänomen (Impulstransport) wird in Kapitel 3 systematisch neben Wärmeleitung und Diffusion eingeordnet.

<a id="zusammenfassung-9"></a>
## Zusammenfassung

- Fluide werden durch Felder $\vec v(\vec r,t)$, $\rho(\vec r,t)$, $p(\vec r,t)$ beschrieben.
- **Kontinuitätsgleichung** $\operatorname{div}\vec j = -\dot\rho$: Massenerhaltung, für inkompressible Strömung $Av=\text{const}$.
- **Bernoulli-Gleichung** $p+\rho gh+\tfrac12\rho v^2=\text{const}$: Energieerhaltung entlang eines Stromfadens, nur für reibungsfreie, stationäre, inkompressible Strömung.
- **Hagen-Poiseuille**: $\dot V = \dfrac{\pi\Delta p R^4}{8\eta\ell}$ für laminare Rohrströmung.
- **Stokes'sches Gesetz**: $F_W=6\pi\eta r\bar v$ für schleichende Umströmung einer Kugel.
- **Reynoldszahl** $\mathrm{Re}$ entscheidet laminar vs. turbulent.

---

<a id="kapitel-2-kinetische-gastheorie-und-temperatur"></a>
# Kapitel 2: Kinetische Gastheorie und Temperatur

<a id="motivation-22"></a>
## Motivation

Was *ist* Temperatur eigentlich? Im Alltag ist sie eine Zahl auf einem Thermometer. Die kinetische Gastheorie (Bernoulli, Clausius, Maxwell, Boltzmann, 18.–19. Jh.) beantwortet die Frage fundamental: Temperatur ist ein **Maß für die mittlere kinetische Energie** der ungeordneten Teilchenbewegung. Diese Erkenntnis ist einer der großen Triumphe der Physik des 19. Jahrhunderts, weil sie eine makroskopische Größe (Temperatur, messbar mit einem Thermometer) auf mikroskopische Mechanik (Newtonsche Stöße von Molekülen) zurückführt — und damit den Übergang von der klassischen Mechanik zur statistischen Physik einleitet.

Das Problem, das gelöst werden musste: Ein Mol Gas enthält $N_A\approx 6{,}022\cdot 10^{23}$ Teilchen. Man kann unmöglich $10^{23}$ Bewegungsgleichungen lösen. Die Lösung ist, nur *statistische Mittelwerte* zu betrachten (Druck, Temperatur) statt individueller Trajektorien.

<a id="intuition-22"></a>
## Intuition

Stell dir ein Gas als extrem viele, sehr kleine, elastisch stoßende Kugeln vor, die chaotisch durch einen Behälter fliegen. Der **Druck** entsteht dadurch, dass diese Kugeln ständig gegen die Wand prallen und dabei Impuls übertragen — wie ein Sandstrahl, der gegen eine Fläche trifft, erzeugt viele kleine, schnelle Stöße makroskopisch eine kontinuierlich wirkende Kraft.

Die **Temperatur** ist ein Maß dafür, *wie heftig* diese Teilchen im Mittel herumfliegen. Doppelte Temperatur (in Kelvin) bedeutet doppelte mittlere kinetische Energie pro Freiheitsgrad — nicht doppelte Geschwindigkeit (die wächst nur mit $\sqrt{T}$, weil Energie quadratisch in $v$ eingeht).

Die **Freiheitsgrade** zählen, auf wie viele unabhängige Arten ein Molekül Energie "speichern" kann: ein einzelnes Atom kann sich nur in $x,y,z$ bewegen (3 FG), ein zweiatomiges Molekül kann zusätzlich um zwei Achsen rotieren (2 weitere FG) — man kann sich das wie Schubladen vorstellen, in die thermische Energie "einsortiert" wird, und jede offene Schublade bekommt im Mittel den gleichen Anteil ($\tfrac12 kT$) — das ist der **Gleichverteilungssatz (Äquipartitionstheorem)**.

<a id="formale-definitionen-22"></a>
## Formale Definitionen

**Definition 2.1 (Ideales Gas — Modellannahmen).**
Ein ideales Gas besteht aus $N$ identischen Teilchen mit folgenden Eigenschaften:
1. Punktförmig (Eigenvolumen vernachlässigbar gegenüber dem Behältervolumen).
2. Keine Wechselwirkung außer bei elastischen Stößen (Wand und untereinander).
3. Bewegung folgt der klassischen Mechanik.

**Definition 2.2 (Druck, mikroskopisch).**
Der Druck ist die mittlere Kraft pro Fläche, die durch Teilchenstöße auf eine Wand ausgeübt wird:
$$p := \frac{\langle F\rangle}{A}.$$

**Definition 2.3 (Freiheitsgrad, FG).**
Ein Freiheitsgrad ist eine unabhängige Koordinate, in der ein Molekül kinetische (oder potentielle) Energie speichern kann. Für ein punktförmiges Teilchen: 3 Translations-FG. Für ein zweiatomiges Molekül zusätzlich: 2 Rotations-FG (um die zwei Achsen senkrecht zur Verbindungsachse; Rotation um die Verbindungsachse selbst trägt praktisch kein Trägheitsmoment und zählt nicht).

**Definition 2.4 (Absolute Temperatur, kinetisch).**
Über den Gleichverteilungssatz definiert:
$$\left\langle \varepsilon_{kin}\right\rangle = \frac{3}{2}k_BT \quad\text{(pro Teilchen, nur Translation)},$$
mit der **Boltzmann-Konstante** $k_B = 1{,}38\cdot10^{-23}\,\text{J/K}$.

**Definition 2.5 (Ideale Gasgleichung).**
$$pV = Nk_BT = nRT,$$
mit Stoffmenge $n$ (in mol; **hier bewusst $n$ statt $\nu$ oder $v$ verwendet, um Verwechslung mit der Geschwindigkeit zu vermeiden — siehe Fehlerkorrektur aus der Mitschrift**), universeller Gaskonstante $R = 8{,}31\,\text{J}/(\text{mol}\,\text{K})$, und $R = N_A k_B$.

**Definition 2.6 (Innere Energie eines idealen Gases).**
$$U := \sum_{i=1}^N \varepsilon_{kin,i} + \sum \varepsilon_{pot,i} = N\cdot f\cdot\tfrac12 k_BT = n\cdot f\cdot\tfrac12 RT,$$
wobei $f$ die Anzahl der Freiheitsgrade pro Molekül ist (für ideale Gase ist $\varepsilon_{pot}=0$, da keine Wechselwirkung).

**Definition 2.7 (Maxwell-Boltzmann-Geschwindigkeitsverteilung).**
Die Wahrscheinlichkeitsdichte, ein Teilchen mit Geschwindigkeitsbetrag $v=|\vec v|$ zu finden:
$$h(v)\, dv = 4\pi\left(\frac{m}{2\pi k_BT}\right)^{3/2} v^2\, e^{-\frac{mv^2}{2k_BT}}\, dv.$$

<a id="eigenschaften-18"></a>
## Eigenschaften

| Größe | Formel | Bedeutung |
|---|---|---|
| Wahrscheinlichste Geschwindigkeit | $v_w = \sqrt{2k_BT/m}$ | Maximum von $h(v)$ |
| Mittlere Geschwindigkeit | $\langle v\rangle = \sqrt{8k_BT/(\pi m)}$ | Mittelwert über $h(v)$ |
| Quadratisch gemittelte Geschwindigkeit | $\sqrt{\langle v^2\rangle} = \sqrt{3k_BT/m}$ | Geht direkt in $\langle\varepsilon_{kin}\rangle$ ein |
| $\langle v^2\rangle > \langle v\rangle^2$ | stets | Cauchy-Schwarz / Varianz $\geq 0$ |
| $f=3$ | einatomiges Gas (Edelgase) | nur Translation |
| $f=5$ | zweiatomiges Gas bei mittleren $T$ | 3 Translation + 2 Rotation |
| $f=6$ (oder mehr) | zweiatomiges Gas bei hohem $T$ | zusätzlich Vibrations-FG (2, da kinetisch+potentiell) |

<a id="sätze-18"></a>
## Sätze

<a id="satz-21-kinetische-druckformel"></a>
### Satz 2.1 (Kinetische Druckformel)

**Aussage:** $$pV = \frac{2}{3}N\langle\varepsilon_{kin}\rangle = \frac13 Nm\langle v^2\rangle.$$

**Voraussetzungen:** ideales Gas (Modellannahmen 1–3), isotrope Geschwindigkeitsverteilung (kein bevorzugter Richtung).

**Bedeutung:** Diese Formel *ist* die Brücke zwischen Mechanik (einzelne Stöße) und Thermodynamik (makroskopischer Druck).

**Intuition:** Druck ist "gemittelter Impulsübertrag pro Zeit und Fläche" — die Formel zählt systematisch, wie viele Teilchen pro Zeit auf ein Wandstück treffen und wie viel Impuls sie jeweils übertragen.

<a id="beweis-von-satz-21"></a>
### Beweis von Satz 2.1

**Beweisstil:** Konstruktiver Beweis durch explizite Stoßbilanz (Standardherleitung der kinetischen Gastheorie).

Betrachte ein Teilchen der Masse $m$ mit Geschwindigkeitskomponente $v_x$, das elastisch von einer Wand (senkrecht zur $x$-Achse) reflektiert wird. Der Impulsübertrag pro Stoß ist $\Delta p_x = 2mv_x$ (Impuls kehrt sich um).

Die Zeit zwischen zwei Stößen desselben Teilchens gegen dieselbe Wand (Behälterlänge $L$ in $x$-Richtung) ist $\Delta t = 2L/v_x$ (Hin- und Rückweg). Die mittlere Kraft *eines* Teilchens auf die Wand ist
$$F_1 = \frac{\Delta p_x}{\Delta t} = \frac{2mv_x}{2L/v_x} = \frac{mv_x^2}{L}.$$
Für $N$ Teilchen mit im Mittel gleichem $\langle v_x^2\rangle$:
$$F = N\frac{m\langle v_x^2\rangle}{L}.$$
Wegen Isotropie ist $\langle v_x^2\rangle = \langle v_y^2\rangle = \langle v_z^2\rangle = \tfrac13\langle v^2\rangle$ (da $v^2=v_x^2+v_y^2+v_z^2$ und alle drei Richtungen gleichwertig sind). Mit der Wandfläche $A$ und Volumen $V=LA$:
$$p = \frac{F}{A} = \frac{Nm\langle v_x^2\rangle}{LA} = \frac{Nm\langle v^2\rangle}{3V} \;\Longrightarrow\; pV = \frac13 Nm\langle v^2\rangle = \frac23 N\left(\tfrac12 m\langle v^2\rangle\right) = \frac23 N\langle\varepsilon_{kin}\rangle.\ \blacksquare$$

<a id="satz-22-gleichverteilungssatz-äquipartitionstheorem"></a>
### Satz 2.2 (Gleichverteilungssatz / Äquipartitionstheorem)

**Aussage:** Im thermischen Gleichgewicht entfällt auf jeden quadratischen Freiheitsgrad im Mittel die Energie $\tfrac12 k_BT$:
$$U = N\cdot f\cdot\tfrac12 k_BT.$$

**Voraussetzungen:** thermisches Gleichgewicht, klassische (nicht-quantisierte) Betrachtung der Freiheitsgrade.

**Bedeutung:** Verallgemeinert Satz 2.1 (der nur Translation, $f=3$, behandelt) auf beliebige Moleküle mit Rotation und Vibration.

**Beweisstil:** Wird in dieser Vorlesung *nicht* streng bewiesen (der vollständige Beweis benötigt die Boltzmann-Statistik / kanonisches Ensemble aus der statistischen Physik). Wir übernehmen ihn als empirisch/statistisch begründetes Postulat — dies ist explizit zu kennzeichnen, da ein Klausurbeweis hierzu nicht erwartet werden sollte.

**Konsequenz:** Aus $U=nf\tfrac12 RT$ und $U=nC_VT$ (Def. Kapitel 4) folgt sofort $C_V = \tfrac f2 R$ — eine der wichtigsten Formeln für die Wärmelehre-Kapitel.

<a id="satz-23-kombination-von-gasgesetzen-zur-idealen-gasgleichung"></a>
### Satz 2.3 (Kombination von Gasgesetzen zur idealen Gasgleichung)

**Aussage:** $pV=nRT$ vereinigt drei historisch getrennt entdeckte Gesetze: Boyle-Mariotte ($pV=\text{const}$ bei $T=\text{const}$), Gay-Lussac ($p\propto T$ bei $V=\text{const}$), Charles ($V\propto T$ bei $p=\text{const}$).

**Beweisidee:** Aus Satz 2.1 und Definition 2.4 folgt direkt $pV = \tfrac23 N\cdot\tfrac32 k_BT = Nk_BT$, was bei fixiertem $N$ genau die drei Spezialfälle reproduziert, je nachdem welche Größe konstant gehalten wird.

<a id="algorithmen-10"></a>
## Algorithmen

**"Rezept" zur Lösung von Gastheorie-Aufgaben**

- **Motivation:** Viele Aufgaben verlangen den Wechsel zwischen mikroskopischer Beschreibung ($v$, $\varepsilon_{kin}$ einzelner Teilchen) und makroskopischer ($p$, $V$, $T$, $U$) — ein systematisches Vorgehen verhindert Verwechslungen.
- **Pseudocode:**
```
EINGABE: gegebene Größen (z. B. T, p, V, m, N, f)
1. WENN T gesucht UND (v oder ε_kin gegeben):
     nutze ⟨ε_kin⟩ = (3/2) k_B T  (nur Translation!)
2. WENN p, V, n, T verknüpft werden sollen:
     nutze pV = nRT
3. WENN U gesucht:
     bestimme zuerst f (aus Molekülstruktur/Temperaturbereich),
     dann U = n f (1/2) R T
4. WENN Geschwindigkeitsverteilung gefragt:
     unterscheide v_w, ⟨v⟩, sqrt(⟨v²⟩) — NICHT verwechseln!
AUSGABE: gesuchte Größe
```
- **Korrektheitsidee:** Jeder Schritt basiert auf einer separat bewiesenen/begründeten Beziehung (Sätze 2.1–2.3).
- **Typische Fehler:** $f$ falsch bestimmt (z. B. bei zweiatomigen Gasen bei sehr tiefer Temperatur werden Rotationsfreiheitsgrade "eingefroren" — quantenmechanischer Effekt, den das klassische Modell nicht erfasst); Verwechslung der drei charakteristischen Geschwindigkeiten.

<a id="beispiele-20"></a>
## Beispiele

**Beispiel 1 (leicht):** Wie groß ist $\langle\varepsilon_{kin}\rangle$ eines Gasteilchens bei $T=300\,\text{K}$?
*Lösung:* $\langle\varepsilon_{kin}\rangle = \tfrac32 k_BT = 1{,}5\cdot1{,}38\cdot10^{-23}\cdot300 \approx 6{,}2\cdot10^{-21}\,\text{J} \approx 0{,}039\,\text{eV}$.

**Beispiel 2 (leicht):** Berechne $\sqrt{\langle v^2\rangle}$ für Stickstoff ($N_2$, $m=4{,}65\cdot10^{-26}\,\text{kg}$) bei $300\,\text{K}$.
*Lösung:* $\sqrt{\langle v^2\rangle}=\sqrt{3k_BT/m} = \sqrt{3\cdot1{,}38\cdot10^{-23}\cdot300/4{,}65\cdot10^{-26}} \approx 517\,\text{m/s} \approx 1850\,\text{km/h}$.

**Beispiel 3 (mittel):** Ein ideales einatomiges Gas ($f=3$) mit $n=2\,\text{mol}$ wird von $300\,\text{K}$ auf $400\,\text{K}$ erwärmt. Wie groß ist $\Delta U$?
*Lösung:* $\Delta U = nf\tfrac12 R\Delta T = 2\cdot3\cdot0{,}5\cdot8{,}31\cdot100 \approx 2493\,\text{J}$.

**Beispiel 4 (mittel):** Zwei Gase im thermischen Gleichgewicht ($T_A=T_B$) — Gas A besteht aus schweren, Gas B aus leichten Teilchen. Welches hat die höhere mittlere Geschwindigkeit?
*Lösung:* Aus $\tfrac12 m_A\langle v_A^2\rangle = \tfrac12 m_B\langle v_B^2\rangle = \tfrac32 k_BT$ folgt $\langle v^2\rangle \propto 1/m$ — die leichteren Teilchen (B) sind im Mittel schneller, obwohl beide Gase dieselbe mittlere *Energie* haben.

**Beispiel 5 (schwer):** Bestimme das Verhältnis $\langle v\rangle/v_w$ aus der Maxwell-Boltzmann-Verteilung und interpretiere es.
*Lösung:* $\dfrac{\langle v\rangle}{v_w} = \dfrac{\sqrt{8k_BT/(\pi m)}}{\sqrt{2k_BT/m}} = \sqrt{\dfrac{4}{\pi}} \approx 1{,}128$ — die mittlere Geschwindigkeit liegt (wegen der asymmetrischen, rechtsschiefen Verteilung) etwas über der wahrscheinlichsten.

<a id="gegenbeispiele-20"></a>
## Gegenbeispiele

- Bei **sehr tiefen Temperaturen** versagt die klassische Gleichverteilung für Rotations-/Vibrationsfreiheitsgrade — diese werden quantenmechanisch "eingefroren" (die thermische Energie $k_BT$ reicht nicht aus, um den ersten angeregten Rotations-/Vibrationszustand zu erreichen). $f$ ist dann effektiv kleiner als der klassische Wert.
- Bei **sehr hohen Dichten oder tiefen Temperaturen nahe der Verflüssigung** versagt das ideale Gasmodell komplett (Eigenvolumen und Wechselwirkungen werden relevant — reales Gas, z. B. van-der-Waals-Gleichung, hier nicht behandelt).
- Für **relativistische Geschwindigkeiten** (extrem hohe $T$) ist $\varepsilon_{kin}=\tfrac12 mv^2$ nicht mehr korrekt.

<a id="typische-klausuraufgaben-21"></a>
## Typische Klausuraufgaben

- Umrechnung zwischen $T$, $\langle\varepsilon_{kin}\rangle$, $\langle v^2\rangle$ — Erkennungsmerkmal: Angabe einer Temperatur und Frage nach einer Geschwindigkeit (oder umgekehrt).
- Bestimmung von $f$ aus der Molekülstruktur und anschließende Berechnung von $U$ oder $C_V$ — wird oft als Vorbereitung für Kapitel 4/5-Aufgaben gestellt.
- Vergleichsaufgaben zwischen zwei Gasen unterschiedlicher Masse bei gleicher Temperatur (Strategie: immer über $\langle\varepsilon_{kin}\rangle$ gehen, nie direkt Geschwindigkeiten vergleichen).

<a id="typische-fehler-21"></a>
## Typische Fehler

1. $\langle\varepsilon_{kin}\rangle = \tfrac32 k_BT$ wird mit der *gesamten* inneren Energie pro Teilchen verwechselt (das gilt nur für $f=3$, einatomige Gase!).
2. $n$ (Stoffmenge) und $v$/$\nu$ (Geschwindigkeit) werden notationsbedingt verwechselt — in diesem Skript daher konsequent $n$ für Stoffmenge reserviert.
3. Bei zweiatomigen Gasen wird die Rotation um die Molekülachse selbst mitgezählt (falsch — deren Trägheitsmoment ist vernachlässigbar).
4. $v_w$, $\langle v\rangle$, $\sqrt{\langle v^2\rangle}$ werden durcheinandergebracht (sie unterscheiden sich um Faktoren nahe 1, aber nicht exakt 1!).

<a id="verbindungen-22"></a>
## Verbindungen

- $pV=nRT$ ist die Grundgleichung für **alle** Zustandsänderungen in Kapitel 4 (isochor, isobar, isotherm, adiabatisch).
- $C_V = \tfrac f2 R$ (aus Satz 2.2) wird in Kapitel 4 zur zentralen Größe für Enthalpie, Adiabatenexponent $\kappa=C_p/C_V$.
- Die **freie Bewegung der Gasteilchen** ist die mikroskopische Grundlage der **Diffusion** (Kapitel 3) und der **elektrischen Leitfähigkeit in Gasen** (Ladungsträgerbewegung, später in Kapitel 8).
- Das Konzept "makroskopische Größe = statistischer Mittelwert vieler mikroskopischer Freiheitsgrade" kehrt bei der **Entropie** (Kapitel 5, Boltzmann-Formel $S=k_B\ln W$) in verallgemeinerter Form wieder.

<a id="zusammenfassung-10"></a>
## Zusammenfassung

- Ideales Gas: punktförmige, nicht wechselwirkende Teilchen.
- $pV = \tfrac23 N\langle\varepsilon_{kin}\rangle = Nk_BT = nRT$.
- $\langle\varepsilon_{kin}\rangle = \tfrac32 k_BT$ (nur Translation); allgemein $U = n f \tfrac12 RT$ (Gleichverteilungssatz).
- Freiheitsgrade $f$: 3 (einatomig), 5 (zweiatomig, Translation+Rotation), mehr bei hoher $T$ (Vibration).
- Maxwell-Boltzmann-Verteilung beschreibt die statistische Verteilung der Geschwindigkeiten; $v_w<\langle v\rangle<\sqrt{\langle v^2\rangle}$.

---

<a id="kapitel-3-transportphänomene"></a>
# Kapitel 3: Transportphänomene

<a id="motivation-23"></a>
## Motivation

Bisher haben wir Gase/Flüssigkeiten im *Gleichgewicht* betrachtet. Was passiert aber, wenn das System *nicht* im Gleichgewicht ist — z. B. wenn irgendwo eine höhere Konzentration, Temperatur oder Geschwindigkeit herrscht als anderswo? Die Natur "will" Gleichgewicht herstellen, und der Weg dahin führt über **Transportprozesse**: Diffusion (Stofftransport), Wärmeleitung (Energietransport), Konvektion (Massentransport durch Auftrieb) und, wie in Kapitel 1 gesehen, Viskosität (Impulstransport). Diese Prozesse folgen alle demselben mathematischen Muster: **Fluss proportional zu einem Gradienten** — ein zentrales, wiederkehrendes Prinzip der Physik.

<a id="intuition-23"></a>
## Intuition

Stell dir eine Tinte vor, die in ein Glas Wasser tropft. Ohne Rühren breitet sie sich trotzdem langsam aus — das ist Diffusion. Der Grund ist rein statistisch: Dort, wo viel Tinte ist, gibt es (durch die zufällige thermische Bewegung der Moleküle) mehr Moleküle, die *zufällig* nach außen wandern, als von außen *zufällig* hineinwandern. Es braucht keine "Kraft", die die Tinte auseinandertreibt — nur die schlichte Tatsache, dass mehr Teilchen dort sind, wo mehr Teilchen sind, und die Zufallsbewegung diesen Unterschied im Mittel ausgleicht.

Wärmeleitung ist im Wesentlichen dasselbe Prinzip, nur dass statt Teilchenzahl die *kinetische Energie* transportiert wird: schnelle (heiße) Moleküle stoßen mit langsamen (kalten) zusammen und geben dabei im Mittel Energie ab.

<a id="formale-definitionen-23"></a>
## Formale Definitionen

**Definition 3.1 (Teilchenstromdichte, Fick'sches Gesetz — 1. Fick'sches Gesetz).**
$$\vec j = -D\,\nabla n(\vec r), \qquad [D] = \frac{\text{m}^2}{\text{s}},$$
mit Konzentration (Teilchendichte) $n(\vec r)$ und Diffusionskoeffizient $D$.

**Definition 3.2 (2. Fick'sches Gesetz).**
Kombiniert man Definition 3.1 mit der Kontinuitätsgleichung (Kapitel 1, Satz 1.1, angewendet auf Teilchenzahl statt Masse):
$$\frac{\partial n}{\partial t} = D\,\Delta n, \qquad \Delta = \nabla^2 \ \text{(Laplace-Operator)}.$$

**Definition 3.3 (Wärmestromdichte, Fourier'sches Gesetz).**
$$\vec j_E = -\lambda\, \nabla T, \qquad [\lambda] = \frac{\text{W}}{\text{m}\,\text{K}},$$
mit Wärmeleitfähigkeit $\lambda$.

**Definition 3.4 (Wiedemann-Franz-Gesetz).**
Für Metalle (Ladungstransport und Wärmetransport durch dieselben freien Elektronen):
$$\frac{\lambda}{\sigma} = a\,T, \qquad a = \frac{\pi^2}{3}\left(\frac{k_B}{e}\right)^2 \approx 2{,}45\cdot 10^{-8}\ \frac{\text{W}\Omega}{\text{K}^2}$$
(Lorenz-Zahl; $\sigma$ elektrische Leitfähigkeit, vgl. Kapitel 8).

<a id="eigenschaften-19"></a>
## Eigenschaften

| Prozess | Transportierte Größe | Gesetz | Triebkraft |
|---|---|---|---|
| Diffusion | Teilchenzahl/Masse | 1./2. Fick'sches Gesetz | Konzentrationsgradient $\nabla n$ |
| Wärmeleitung | Energie | Fourier'sches Gesetz | Temperaturgradient $\nabla T$ |
| Viskosität (Kap. 1) | Impuls | Newtonsches Reibungsgesetz | Geschwindigkeitsgradient $\nabla v$ |
| Konvektion | Masse (makroskopisch) | kein einfaches lineares Gesetz | Dichteunterschied + Gravitation |

Alle drei linearen Transportgesetze (Diffusion, Wärmeleitung, Viskosität) haben dieselbe Struktur: **Fluss = −(Transportkoeffizient) × Gradient(intensive Größe)**. Dieses Muster wird uns in Kapitel 8 (Ohm'sches Gesetz, $\vec j = \sigma\vec E$, hier ist $\vec E = -\nabla\phi$!) exakt wiederbegegnen.

<a id="sätze-19"></a>
## Sätze

<a id="satz-31-2-ficksches-gesetz-aus-kontinuität-1-fickschem-gesetz"></a>
### Satz 3.1 (2. Fick'sches Gesetz aus Kontinuität + 1. Fick'schem Gesetz)

**Aussage:** $\dfrac{\partial n}{\partial t} = D\Delta n$.

**Voraussetzungen:** $D$ räumlich konstant, keine Quellen/Senken von Teilchen (keine chemische Reaktion).

**Beweis (Beweisstil: direkte Substitution).**
Die Kontinuitätsgleichung für die Teilchendichte lautet analog zu Satz 1.1:
$$\operatorname{div}\vec j = -\frac{\partial n}{\partial t}.$$
Einsetzen von $\vec j = -D\nabla n$ (Definition 3.1):
$$\operatorname{div}(-D\nabla n) = -\frac{\partial n}{\partial t} \;\Longrightarrow\; -D\,\operatorname{div}(\nabla n) = -\frac{\partial n}{\partial t} \;\Longrightarrow\; \frac{\partial n}{\partial t} = D\,\Delta n. \qquad\blacksquare$$

**Bedeutung:** Dies ist eine partielle Differentialgleichung (Diffusionsgleichung, mathematisch identisch mit der Wärmeleitungsgleichung — s. u.), deren Lösungen die zeitliche Ausbreitung eines Konzentrationsprofils beschreiben.

<a id="satz-32-analogie-diffusionsgleichung-wärmeleitungsgleichung"></a>
### Satz 3.2 (Analogie Diffusionsgleichung — Wärmeleitungsgleichung)

**Aussage:** Setzt man in der Herleitung von Satz 3.1 statt $n$ die Größe "Energiedichte" bzw. (bei konstanter spezifischer Wärme $c$ und Dichte $\rho$) die Temperatur $T$ ein, erhält man die formal identische Gleichung
$$\frac{\partial T}{\partial t} = \frac{\lambda}{\rho c}\,\Delta T =: \kappa_{th}\,\Delta T$$
mit der Temperaturleitfähigkeit $\kappa_{th}$.

**Bedeutung:** Diffusion und Wärmeleitung sind mathematisch **dieselbe** Gleichung mit unterschiedlicher physikalischer Interpretation — ein Paradebeispiel dafür, wie Physik durch abstrakte, wiederverwendbare mathematische Strukturen enorm an Eleganz gewinnt.

<a id="algorithmen-11"></a>
## Algorithmen

**Lösungsstrategie für Transportaufgaben**
- **Motivation:** Diffusions-, Wärmeleitungs- und Viskositätsaufgaben werden oft verwechselt, weil sie strukturell gleich aussehen.
- **Pseudocode:**
```
EINGABE: Transportproblem (Was wird transportiert? Wodurch?)
1. Identifiziere die transportierte Größe:
   Teilchen/Masse → Diffusion (Fick)
   Wärme/Energie  → Wärmeleitung (Fourier)
   Impuls         → Viskosität (Newton, Kapitel 1)
2. Identifiziere den Gradienten (Konzentration, Temperatur, Geschwindigkeit)
3. Wende j = -K * grad(Größe) an (K = D, λ bzw. η)
4. WENN stationär (∂/∂t = 0): j = const, oft linear approximierbar
   (j ≈ K * ΔGröße / Δx für ebene Geometrie)
5. WENN zeitabhängig: 2. Fick'sches Gesetz / Wärmeleitungsgleichung lösen
AUSGABE: Stromdichte, Konzentrations-/Temperaturprofil
```
- **Typische Fehler:** Vorzeichen vergessen (Fluss ist *entgegen* dem Gradienten gerichtet — von hoch nach tief); Verwechslung von $D$, $\lambda$, $\eta$ (unterschiedliche Einheiten!).

<a id="beispiele-21"></a>
## Beispiele

**Beispiel 1 (leicht):** Eine Membran trennt zwei Bereiche mit $n_1=10^{20}\,\text{m}^{-3}$ und $n_2=10^{19}\,\text{m}^{-3}$, Abstand $\Delta x = 1\,\text{mm}$, $D=10^{-9}\,\text{m}^2/\text{s}$. Bestimme $j$.
*Lösung:* $j \approx D\dfrac{n_1-n_2}{\Delta x} = 10^{-9}\cdot\dfrac{9\cdot10^{19}}{10^{-3}} = 9\cdot10^{7}\,\text{m}^{-2}\text{s}^{-1}$.

**Beispiel 2 (mittel):** Eine Wand ($\lambda = 0{,}8\,\text{W/(mK)}$, Dicke $d=20\,\text{cm}$) trennt Innen ($20\,°\text{C}$) von Außen ($0\,°\text{C}$). Bestimme den Wärmestrom pro $\text{m}^2$.
*Lösung:* $j_E = \lambda\dfrac{\Delta T}{d} = 0{,}8\cdot\dfrac{20}{0{,}2} = 80\,\text{W/m}^2$.

**Beispiel 3 (schwer):** Zeige, dass eine Gauß-Verteilung $n(x,t)=\frac{N_0}{\sqrt{4\pi Dt}}e^{-x^2/(4Dt)}$ die Diffusionsgleichung (1D: $\partial_tn=D\partial_x^2n$) löst.
*Lösung:* Direktes Differenzieren (Rechenaufgabe) — Ableitung nach $t$ und zweite Ableitung nach $x$ einsetzen, beide Seiten stimmen überein. (Wird hier als Übung empfohlen, nicht vollständig vorgerechnet, da reine Rechentechnik ohne neue Konzepte.)

<a id="gegenbeispiele-21"></a>
## Gegenbeispiele

- Bei **hoher Konzentration/starken Gradienten** kann $D$ selbst konzentrationsabhängig werden (nichtlineare Diffusion) — Fick's Gesetz ist dann nur noch näherungsweise gültig.
- **Konvektion** lässt sich NICHT durch ein einfaches lineares Fluss-Gradient-Gesetz beschreiben, da sie makroskopischen Massentransport durch Auftrieb involviert (keine einfache Proportionalität zu einem Gradienten wie bei den anderen drei Prozessen).

<a id="typische-klausuraufgaben-22"></a>
## Typische Klausuraufgaben

- Stationäre Wärmeleitung durch mehrschichtige Wände (Reihenschaltung von "thermischen Widerständen" $d/\lambda$ — direkte Analogie zu elektrischen Widerständen, Kapitel 8!).
- Abschätzung von Diffusionszeiten über $\Delta x \sim \sqrt{Dt}$ (aus der Struktur der Diffusionsgleichung).
- Osmotischer Druck ($\pi_{osm} = \frac{n}{V}RT$, van't-Hoff'sches Gesetz) bei halbdurchlässigen Membranen.

<a id="typische-fehler-22"></a>
## Typische Fehler

1. Fourier'sches und Fick'sches Gesetz werden inhaltlich verwechselt (unterschiedliche transportierte Größe).
2. Vorzeichen des Gradienten falsch gesetzt (Fluss fließt von hoher zu niedriger Konzentration/Temperatur, das Minuszeichen ist essenziell).
3. Stationärer Fall (linear approximiert) wird auf zeitabhängige Probleme angewendet, wo eigentlich die volle Diffusionsgleichung nötig wäre.

<a id="verbindungen-23"></a>
## Verbindungen

- Direkte mathematische Analogie zu **Viskosität** (Kap. 1) und **Ohm'schem Gesetz** (Kap. 8, $\vec j=\sigma\vec E=-\sigma\nabla\phi$) — alle drei sind Spezialfälle des Musters "Fluss $\propto$ Gradient einer intensiven Größe".
- Die thermischen Widerstände $d/\lambda$ bei Reihenschaltung von Wänden sind strukturell identisch zu elektrischen Reihenwiderständen (Kirchhoff'sche Regeln, Kap. 8).
- Grundlage für ein tieferes Verständnis, warum **Wärmeleitung** in Kapitel 4/5 als eigener Mechanismus des Energieaustauschs (neben Arbeit) eine Rolle spielt.

<a id="zusammenfassung-11"></a>
## Zusammenfassung

- Transportprozesse folgen dem Muster Fluss $=-K\cdot\nabla(\text{Größe})$.
- Diffusion: $\vec j=-D\nabla n$, 2. Fick'sches Gesetz $\partial_tn=D\Delta n$.
- Wärmeleitung: $\vec j_E=-\lambda\nabla T$, mathematisch identische Differentialgleichung wie Diffusion.
- Wiedemann-Franz-Gesetz verknüpft Wärme- und elektrische Leitfähigkeit in Metallen.
- Konvektion ist kein lineares Gradientengesetz, sondern makroskopischer Auftriebstransport.

---

<a id="kapitel-4-wärme-arbeit-und-der-1-hauptsatz-der-thermodynamik"></a>
# Kapitel 4: Wärme, Arbeit und der 1. Hauptsatz der Thermodynamik

<a id="motivation-24"></a>
## Motivation

Im 19. Jahrhundert war eine der zentralen offenen Fragen: Ist Wärme eine eigenständige "Substanz" (Caloricum-Theorie) oder eine Form von Energie? Joule zeigte experimentell (Rührwerk-Experiment), dass mechanische Arbeit vollständig in Wärme umgewandelt werden kann, mit einem festen Umrechnungsfaktor. Das führte zur Erkenntnis: **Wärme ist eine Form von Energieübertragung**, keine Substanz. Der 1. Hauptsatz ist nichts anderes als der Energieerhaltungssatz, erweitert um Wärme als zusätzliche "Buchungsposition".

<a id="intuition-24"></a>
## Intuition

Stell dir die innere Energie $U$ eines Gases als ein Bankkonto vor. Es gibt zwei Wege, das Konto zu verändern: **Einzahlungen/Abhebungen durch Wärme** ($Q$, wie eine Überweisung von außen) und **Einzahlungen/Abhebungen durch Arbeit** ($W$, wie physische Bargeldübergabe). Der Kontostand selbst ($U$) kennt nicht, auf welchem Weg das Geld hereinkam — nur die Summe zählt. Das ist der Kern des 1. Hauptsatzes: $U$ ist eine **Zustandsgröße** (hängt nur vom aktuellen Zustand ab), während $Q$ und $W$ **Prozessgrößen** sind (hängen vom Weg ab, wie man dorthin kam).

<a id="formale-definitionen-24"></a>
## Formale Definitionen

**Definition 4.1 (Volumenarbeit).**
Bei quasistatischer Volumenänderung $dV$ gegen den Außendruck $p$ verrichtet das Gas die Arbeit
$$\delta W_{vom\ Gas} = p\, dV.$$
Die *am* Gas verrichtete Arbeit ist entsprechend $\delta W = -p\,dV$.

**Definition 4.2 (Vorzeichenkonvention — hier vereinheitlicht).**
$$dU = \delta Q - p\, dV,$$
mit $\delta Q>0$: dem Gas wird Wärme zugeführt; $p\,dV>0$: das Gas leistet Arbeit (dehnt sich aus) und $U$ sinkt entsprechend. **(Diese Konvention wird im gesamten Skript konsistent verwendet — im Gegensatz zur uneinheitlichen Schreibweise der Mitschrift.)**

**Definition 4.3 (Wärmekapazität).**
$$C := \frac{1}{n}\frac{\delta Q}{dT}, \qquad [C] = \frac{\text{J}}{\text{mol}\,\text{K}}.$$
Wichtig: $C$ ist **prozessabhängig** — man unterscheidet $C_V$ (bei konstantem Volumen) und $C_p$ (bei konstantem Druck).

**Definition 4.4 (Enthalpie).**
$$H := U + pV.$$

**Definition 4.5 (Adiabatenexponent).**
$$\kappa := \frac{C_p}{C_V}.$$

<a id="eigenschaften-20"></a>
## Eigenschaften

| Größe | Zustandsgröße? | Bedeutung |
|---|---|---|
| $U$ | ja | hängt nur vom momentanen Zustand $(p,V,T)$ ab |
| $H$ | ja | wie $U$, aber praktisch für isobare Prozesse |
| $Q$ | **nein** | hängt vom Weg/Prozess ab |
| $W$ | **nein** | hängt vom Weg/Prozess ab |
| $C_V,\ C_p$ | (Materialgröße) | $C_p > C_V$ stets (siehe Satz 4.2) |

<a id="sätze-20"></a>
## Sätze

<a id="satz-41-1-hauptsatz-der-thermodynamik"></a>
### Satz 4.1 (1. Hauptsatz der Thermodynamik)

**Aussage:** $dU = \delta Q - p\,dV$. Für ein ideales Gas gilt zusätzlich $U=U(T)$ *nur* (unabhängig von $V$!), also $dU = nC_V\,dT$ für jeden Prozess.

**Voraussetzungen:** geschlossenes System (kein Stoffaustausch), quasistatischer Prozess (Definition der Volumenarbeit setzt Gleichgewichtsdruck voraus).

**Bedeutung:** Energieerhaltungssatz, erweitert um Wärme. Fundamentalste Gleichung der gesamten Thermodynamik.

**Intuition:** Es gibt keine "Energiequelle aus dem Nichts" — jede Änderung der inneren Energie muss durch Wärmeaustausch mit der Umgebung oder durch am/vom System verrichtete Arbeit erklärt werden.

**Konsequenz — Perpetuum mobile 1. Art:** Maschinen, die dauerhaft mehr Arbeit leisten als $dU-dQ$ zulässt (also Energie "erschaffen"), sind unmöglich.

<a id="satz-42-c_p-c_v-r-robert-mayer-beziehung"></a>
### Satz 4.2 ($C_p - C_V = R$, "Robert-Mayer-Beziehung")

**Aussage:** Für ein ideales Gas gilt $C_p - C_V = R$, also stets $C_p>C_V$.

**Voraussetzungen:** ideales Gas ($pV=nRT$, $U=U(T)$ allein).

**Bedeutung:** Bei konstantem Druck muss zusätzlich zur Temperaturerhöhung auch noch Ausdehnungsarbeit gegen den Außendruck verrichtet werden — das kostet zusätzliche Wärme im Vergleich zum isochoren Prozess.

<a id="beweis-von-satz-42"></a>
### Beweis von Satz 4.2

**Beweisstil:** Direkter Beweis über die Definitionen von $C_V$, $C_p$ und den 1. Hauptsatz.

Bei konstantem Volumen ist $dV=0$, also nach Def. 4.2: $dU = \delta Q \Rightarrow C_V = \dfrac1n\dfrac{dU}{dT}\Big|_{V} = \dfrac1n\dfrac{dU}{dT}$ (da für ideales Gas $U=U(T)$ ohnehin nur von $T$ abhängt, ist die Bedingung "bei konstantem $V$" hier automatisch erfüllt für die Ableitung).

Bei konstantem Druck ist nach Def. 4.4 $dH = dU + p\,dV + V\,dp = dU+p\,dV$ (da $dp=0$). Mit dem 1. Hauptsatz $dU=\delta Q-p\,dV$ folgt $dH = \delta Q$, also
$$C_p = \frac1n\frac{dH}{dT}\bigg|_p.$$
Aus $H=U+pV=U+nRT$ (ideales Gas) folgt $dH = dU + nR\,dT$, also
$$nC_p\,dT = nC_V\,dT + nR\,dT \;\Longrightarrow\; C_p = C_V+R. \qquad\blacksquare$$

<a id="satz-43-adiabatengleichungen"></a>
### Satz 4.3 (Adiabatengleichungen)

**Aussage:** Für eine adiabatische ($\delta Q=0$), quasistatische Zustandsänderung eines idealen Gases gilt
$$T\,V^{\kappa-1} = \text{const}, \qquad p\,V^{\kappa} = \text{const}, \qquad \frac{T^{\kappa}}{p^{\kappa-1}} = \text{const}.$$

**Voraussetzungen:** ideales Gas, $\delta Q=0$, quasistatisch, $C_V$ temperaturunabhängig im betrachteten Bereich.

**Bedeutung:** Beschreibt schnelle Kompressionen/Expansionen (z. B. im Verbrennungsmotor), bei denen keine Zeit für Wärmeaustausch mit der Umgebung bleibt.

<a id="beweis-von-satz-43"></a>
### Beweis von Satz 4.3

**Beweisstil:** Direkte Integration einer separierbaren Differentialgleichung.

Aus dem 1. Hauptsatz mit $\delta Q=0$: $\;nC_V\,dT = -p\,dV$. Mit $p=nRT/V$ (ideale Gasgleichung):
$$nC_V\,dT = -\frac{nRT}{V}\,dV \;\Longrightarrow\; C_V\frac{dT}{T} = -R\frac{dV}{V}.$$
Beide Seiten integrieren:
$$C_V\ln T = -R\ln V + \text{const} \;\Longrightarrow\; \ln T = -\frac{R}{C_V}\ln V+\text{const}.$$
Mit $R=C_p-C_V$ (Satz 4.2) ist $\dfrac{R}{C_V} = \dfrac{C_p-C_V}{C_V} = \kappa - 1$. Also
$$\ln T = -(\kappa-1)\ln V + \text{const} \;\Longrightarrow\; T = \text{const}\cdot V^{-(\kappa-1)} \;\Longrightarrow\; T\,V^{\kappa-1}=\text{const}.$$
Mit $T=pV/(nR)$ eingesetzt folgt direkt $p\,V^\kappa=\text{const}$, und Elimination von $V$ zwischen beiden Formen liefert $T^\kappa/p^{\kappa-1}=\text{const}$. $\blacksquare$

<a id="algorithmen-12"></a>
## Algorithmen

**Lösungsstrategie für Zustandsänderungen**
- **Motivation:** Die vier Standardprozesse (isochor, isobar, isotherm, adiabatisch) tauchen in fast jeder Klausur auf und verlangen jeweils andere Formeln für $Q$, $W$, $\Delta U$.
- **Pseudocode:**
```
EINGABE: Prozesstyp, Anfangs-/Endzustand
1. Identifiziere Prozesstyp anhand der konstant gehaltenen Größe:
   V = const → isochor
   p = const → isobar
   T = const → isotherm
   Q = 0     → adiabatisch
2. Berechne ΔU = n C_V ΔT  (gilt IMMER für ideales Gas, unabhängig vom Prozess!)
3. FALLS isochor:      W = 0,             Q = ΔU
   FALLS isobar:       W = p ΔV = nR ΔT,  Q = n C_p ΔT
   FALLS isotherm:     ΔU = 0,            W = Q = nRT ln(V2/V1)
   FALLS adiabatisch:  Q = 0,             W = -ΔU = -n C_V ΔT
4. Nutze ggf. Adiabatengleichung (Satz 4.3), um fehlende Zustandsgröße
   (p, V oder T am Endpunkt) zu bestimmen
AUSGABE: Q, W, ΔU für den Prozess
```
- **Korrektheitsidee:** Schritt 2 gilt immer wegen $U=U(T)$ für ideale Gase (unabhängig vom Weg — Zustandsgröße!); die Fallunterscheidung in Schritt 3 folgt direkt aus den Definitionen und Satz 4.1.
- **Typische Fehler:** $\Delta U=nC_V\Delta T$ wird fälschlich nur für isochore Prozesse angewendet — es gilt aber für **jeden** Prozess eines idealen Gases, weil $U$ eine reine Funktion von $T$ ist!

<a id="beispiele-22"></a>
## Beispiele

**Beispiel 1 (leicht):** $2\,\text{mol}$ eines einatomigen idealen Gases werden bei konstantem Volumen von $300\,\text{K}$ auf $400\,\text{K}$ erwärmt ($C_V=\tfrac32R$). Berechne $Q$, $W$, $\Delta U$.
*Lösung:* $W=0$ (isochor). $\Delta U = nC_V\Delta T = 2\cdot1{,}5\cdot8{,}31\cdot100 = 2493\,\text{J} = Q$.

**Beispiel 2 (mittel):** Dasselbe Gas wird stattdessen isotherm bei $300\,\text{K}$ von $V_1=10\,\text{L}$ auf $V_2=20\,\text{L}$ expandiert. Berechne $W$.
*Lösung:* $\Delta U=0$ (isotherm, ideales Gas). $W=Q=nRT\ln(V_2/V_1)=2\cdot8{,}31\cdot300\cdot\ln 2 \approx 3456\,\text{J}$.

**Beispiel 3 (mittel):** Luft ($\kappa=1{,}4$) wird adiabatisch von $V_1=1\,\text{L}$, $p_1=1\,\text{bar}$ auf $V_2=0{,}5\,\text{L}$ komprimiert. Bestimme $p_2$.
*Lösung:* $p_1V_1^\kappa=p_2V_2^\kappa \Rightarrow p_2=p_1(V_1/V_2)^\kappa = 1\cdot 2^{1,4}\approx 2{,}64\,\text{bar}$.

**Beispiel 4 (schwer):** Berechne $C_p$ für ein zweiatomiges Gas ($f=5$) und vergleiche mit einatomigem Gas.
*Lösung:* $C_V=\tfrac52R$, also $C_p=C_V+R=\tfrac72R\approx 29{,}1\,\text{J/(mol K)}$, gegenüber $C_p=\tfrac52R\approx 20{,}8\,\text{J/(mol K)}$ für einatomige Gase. $\kappa_{zweiatomig}=7/5=1{,}4$ statt $\kappa_{einatomig}=5/3\approx1{,}67$.

**Beispiel 5 (schwer, kombiniert):** Ein Gas durchläuft nacheinander: (1) isochore Erwärmung, (2) isotherme Expansion. Skizziere den Prozess im $p$-$V$-Diagramm und berechne die Gesamtarbeit.
*Lösung:* Strategie: Arbeit ist additiv über Teilprozesse; $W_{ges}=W_1+W_2 = 0 + nRT_2\ln(V_3/V_2)$ (mit $T_2$ = Temperatur nach Schritt 1). Details hängen von den konkreten Zahlenwerten ab — wichtig ist die Erkenntnis, dass sich mehrstufige Prozesse durch Aneinanderreihung der Einzelformeln lösen lassen.

<a id="gegenbeispiele-22"></a>
## Gegenbeispiele

- $\Delta U = nC_V\Delta T$ gilt **NICHT** für reale Gase (dort hängt $U$ zusätzlich von $V$ ab, wegen zwischenmolekularer Wechselwirkung — van-der-Waals-Korrektur nötig).
- Die Adiabatengleichungen (Satz 4.3) gelten **NICHT**, wenn der Prozess nicht quasistatisch ist (z. B. eine plötzliche, sehr schnelle Expansion ins Vakuum — dort wird zwar auch $Q=0$, aber auch $W=0$, da kein Gegendruck existiert, und $T$ bleibt beim idealen Gas konstant, was der Adiabatengleichung scheinbar widerspricht, weil diese quasistatisches Gleichgewicht voraussetzt).

<a id="typische-klausuraufgaben-23"></a>
## Typische Klausuraufgaben

- "Berechnen Sie $Q$, $W$, $\Delta U$ für einen [isochoren/isobaren/isothermen/adiabatischen] Prozess" — Strategie: siehe Algorithmus oben, IMMER zuerst $\Delta U=nC_V\Delta T$ berechnen.
- $p$-$V$-Diagramme zeichnen und Fläche unter der Kurve als Arbeit interpretieren.
- Mehrstufige Prozesse (Kombination mehrerer Zustandsänderungen) — Vorbereitung auf Kreisprozesse in Kapitel 5.
- Bestimmung von $\kappa$ oder $f$ aus gegebenen $C_p$, $C_V$ oder umgekehrt.

<a id="typische-fehler-23"></a>
## Typische Fehler

1. $\Delta U=nC_V\Delta T$ wird nur für isochore Prozesse "erlaubt" gehalten — falsch, gilt für alle Prozesse idealer Gase.
2. Vorzeichenfehler: Arbeit *am* Gas vs. *vom* Gas verwechselt.
3. $C_p$ und $C_V$ vertauscht (v. a. bei isobaren Aufgaben).
4. Adiabatengleichung mit falschem Exponenten ($\kappa$ statt $\kappa-1$ oder umgekehrt) angewendet.

<a id="verbindungen-24"></a>
## Verbindungen

- Baut direkt auf Kapitel 2 auf ($U=nf\tfrac12RT \Rightarrow C_V=\tfrac f2R$).
- Ist die Grundlage für **Kreisprozesse** (Kapitel 5) — jeder Kreisprozess besteht aus einer Abfolge der hier eingeführten vier Standardprozesse.
- Die Enthalpie $H$ wird in der Chemie/Verfahrenstechnik systematisch weiterverwendet (hier nur eingeführt, nicht vertieft).

<a id="zusammenfassung-12"></a>
## Zusammenfassung

- 1. Hauptsatz: $dU=\delta Q-p\,dV$; $U$ Zustandsgröße, $Q,W$ Prozessgrößen.
- Für ideales Gas: $\Delta U=nC_V\Delta T$ gilt **immer**, unabhängig vom Prozess.
- $C_p-C_V=R$ (Robert-Mayer), $\kappa=C_p/C_V>1$.
- Vier Standardprozesse mit charakteristischen $Q$-$W$-$\Delta U$-Formeln (siehe Algorithmus).
- Adiabatengleichungen: $TV^{\kappa-1}=\text{const}$, $pV^\kappa=\text{const}$.

---

<a id="kapitel-5-kreisprozesse-und-der-2-hauptsatz-der-thermodynamik"></a>
# Kapitel 5: Kreisprozesse und der 2. Hauptsatz der Thermodynamik

<a id="motivation-25"></a>
## Motivation

Der 1. Hauptsatz sagt: Energie kann nicht erzeugt oder vernichtet werden. Er verbietet aber **nicht** offensichtlich unsinnige Prozesse — z. B. dass Wärme spontan von einem kalten zu einem heißen Körper fließt (das würde $U$ nirgends verletzen!) oder dass eine Maschine Wärme *vollständig* in Arbeit umwandelt, ohne Abwärme abzugeben. Beides beobachten wir nie in der Natur. Der 2. Hauptsatz ergänzt daher den 1. Hauptsatz um eine **Richtungsaussage**: Manche energetisch erlaubten Prozesse laufen trotzdem nie (oder nur in eine Richtung) ab. Historisch entstand dies aus dem sehr praktischen Problem, den Wirkungsgrad von Dampfmaschinen zu maximieren (Carnot, 1824) — lange bevor man wusste, warum es eine fundamentale Grenze gibt.

<a id="intuition-25"></a>
## Intuition

Denk an einen Stapel Bücher, der umfällt: Die Bücher verteilen sich chaotisch auf dem Boden. Der Prozess "Bücher fallen und verteilen sich" passiert spontan; der umgekehrte Prozess ("Bücher springen von selbst zurück in einen ordentlichen Stapel") widerspricht nicht der Energieerhaltung, passiert aber praktisch nie. Der Grund: Es gibt extrem viele "unordentliche" Anordnungen, aber nur sehr wenige "ordentliche". Das System bewegt sich statistisch fast immer in Richtung *mehr* Möglichkeiten — das ist der Kern der **Entropie**: ein Maß für die Anzahl der mikroskopischen Möglichkeiten, die zu einem gegebenen makroskopischen Zustand passen.

Bei einer Wärmekraftmaschine ist die tiefere Ursache dieselbe: Um Wärme vollständig in Arbeit (eine hochgeordnete Form von Energie, alle Moleküle bewegen sich "im gleichen Takt") umzuwandeln, müsste man die ungeordnete thermische Bewegung komplett "ordnen" — das ist statistisch extrem unwahrscheinlich, wenn nicht gleichzeitig woanders Unordnung zunimmt (Abwärme an ein kälteres Reservoir).

<a id="formale-definitionen-25"></a>
## Formale Definitionen

**Definition 5.1 (Kreisprozess).**
Ein Kreisprozess ist eine Folge von Zustandsänderungen, die das System zum Ausgangszustand zurückführt: $\oint dU = 0$ (da $U$ Zustandsgröße ist).

**Definition 5.2 (Wirkungsgrad einer Wärmekraftmaschine).**
$$\eta := \frac{|W|}{Q_{zu}},$$
das Verhältnis von gewonnener Arbeit zu zugeführter Wärme (vom heißen Reservoir).

**Definition 5.3 (Entropie, thermodynamisch).**
$$dS := \frac{\delta Q_{rev}}{T}$$
für einen *reversiblen* Prozess (Index "rev" zur Betonung — für irreversible Prozesse gilt nur $dS \geq \delta Q/T$, s. Satz 5.4).

**Definition 5.4 (Entropie, statistisch — Boltzmann).**
$$S := k_B\ln W,$$
mit $W$ = Anzahl der mikroskopischen Realisierungsmöglichkeiten (Mikrozustände), die zum gegebenen Makrozustand führen.

<a id="eigenschaften-21"></a>
## Eigenschaften

| Kreisprozess | Teilschritte | Typische Anwendung |
|---|---|---|
| Carnot | isotherm–adiabatisch–isotherm–adiabatisch | theoretischer Referenzprozess, maximaler Wirkungsgrad |
| Stirling | isotherm–isochor–isotherm–isochor | Stirlingmotor |
| Otto | adiabatisch–isochor–adiabatisch–isochor | Benzinmotor |
| Diesel | adiabatisch–isobar–adiabatisch–isochor | Dieselmotor |

| Vergleich | Wärmekraftmaschine | Kältemaschine/Wärmepumpe |
|---|---|---|
| Zweck | mechanische Arbeit gewinnen | Wärme von kalt nach warm transportieren |
| Energiefluss | $Q_1$ (warm, rein) → $W$ (raus) + $Q_2$ (kalt, raus) | $W$ (rein) + $Q_2$ (kalt, rein) → $Q_1$ (warm, raus) |
| Kennzahl | Wirkungsgrad $\eta=|W|/Q_1$ | Leistungszahl $\varepsilon = Q_1/W$ bzw. $Q_2/W$ |

<a id="sätze-21"></a>
## Sätze

<a id="satz-51-carnot-wirkungsgrad"></a>
### Satz 5.1 (Carnot-Wirkungsgrad)

**Aussage:** Für den Carnot-Prozess zwischen den Temperaturen $T_1$ (heiß) und $T_2$ (kalt) gilt
$$\eta_{Carnot} = 1 - \frac{T_2}{T_1} = \frac{T_1-T_2}{T_1}.$$

**Voraussetzungen:** reversibler Kreisprozess, ideales Gas als Arbeitsmedium, zwei Wärmereservoire konstanter Temperatur.

**Bedeutung:** Dies ist der **maximal mögliche** Wirkungsgrad jeder Wärmekraftmaschine, die zwischen zwei festen Temperaturen arbeitet — unabhängig vom Funktionsprinzip (2. Hauptsatz, Carnot'scher Satz).

**Intuition:** Je größer der Temperaturunterschied, desto mehr "Ordnung" (niedrige Entropie bei $T_2$) steht zur Verfügung, um in Arbeit umgewandelt zu werden.

<a id="beweis-von-satz-51"></a>
### Beweis von Satz 5.1

**Beweisstil:** Direkte Berechnung der vier Teilprozesse (konstruktiver Beweis).

Der Carnot-Zyklus besteht aus vier Schritten (Zustände 1→2→3→4→1):

1. **Isotherme Expansion** bei $T_1$ ($V_1\to V_2$): $\Delta U=0$, also $Q_{12}=W_{12}=nRT_1\ln(V_2/V_1)$.
2. **Adiabatische Expansion** ($T_1\to T_2$, $V_2\to V_3$): $Q_{23}=0$, $W_{23}=-nC_V(T_2-T_1)$.
3. **Isotherme Kompression** bei $T_2$ ($V_3\to V_4$): $Q_{34}=nRT_2\ln(V_4/V_3) < 0$ (da $V_4<V_3$).
4. **Adiabatische Kompression** ($T_2\to T_1$, $V_4\to V_1$): $Q_{41}=0$.

Aus den Adiabatengleichungen (Satz 4.3) für die Schritte 2 und 4:
$$T_1V_2^{\kappa-1} = T_2V_3^{\kappa-1}, \qquad T_1V_1^{\kappa-1}=T_2V_4^{\kappa-1}.$$
Division dieser beiden Gleichungen liefert $\dfrac{V_2}{V_1}=\dfrac{V_3}{V_4}$.

Die insgesamt aufgenommene Wärme ist $Q_1:=Q_{12}=nRT_1\ln(V_2/V_1)$, die abgegebene $|Q_2|:=-Q_{34}=nRT_2\ln(V_3/V_4)=nRT_2\ln(V_2/V_1)$ (wegen $V_3/V_4=V_2/V_1$).

Die insgesamt verrichtete Arbeit ist (da $\oint dU=0$): $|W| = Q_1 - |Q_2| = nR(T_1-T_2)\ln(V_2/V_1)$.

Damit:
$$\eta = \frac{|W|}{Q_1} = \frac{nR(T_1-T_2)\ln(V_2/V_1)}{nRT_1\ln(V_2/V_1)} = \frac{T_1-T_2}{T_1} = 1-\frac{T_2}{T_1}. \qquad\blacksquare$$

<a id="satz-52-carnotscher-satz-optimalität"></a>
### Satz 5.2 (Carnot'scher Satz — Optimalität)

**Aussage:** Keine Wärmekraftmaschine, die zwischen den Temperaturen $T_1$ und $T_2$ arbeitet, kann einen höheren Wirkungsgrad als $\eta_{Carnot}$ erreichen.

**Beweisidee (Widerspruchsbeweis):** Angenommen, es gäbe eine "Super-Carnot"-Maschine mit $\eta' > \eta_{Carnot}$. Man könnte sie mit einer rückwärts laufenden (als Kältemaschine betriebenen) Carnot-Maschine koppeln, sodass die Super-Maschine die Carnot-Maschine antreibt. Netto würde dann Wärme *ohne* äußere Arbeitszufuhr vom kalten zum heißen Reservoir fließen — ein Widerspruch zum 2. Hauptsatz (Formulierung nach Clausius: "Es gibt keinen Prozess, dessen einziges Ergebnis der Wärmeübergang von einem kälteren zu einem wärmeren Körper ist"). Also kann $\eta'>\eta_{Carnot}$ nicht existieren. **Markierung:** Dies ist ein reiner Existenz-/Widerspruchsbeweis, kein Rechenbeweis — für die Klausur genügt in der Regel die Beweisidee.

<a id="satz-53-entropieänderung-bei-zustandsänderungen-idealer-gase"></a>
### Satz 5.3 (Entropieänderung bei Zustandsänderungen idealer Gase)

**Aussage:**
$$\Delta S(T,V) = nC_V\ln\frac{T_2}{T_1} + nR\ln\frac{V_2}{V_1}, \qquad \Delta S(p,T) = nC_p\ln\frac{T_2}{T_1} - nR\ln\frac{p_2}{p_1}.$$

**Beweis (Beweisstil: direkte Integration).**
Aus Definition 5.3 und dem 1. Hauptsatz:
$$dS = \frac{\delta Q}{T} = \frac{dU+p\,dV}{T} = \frac{nC_V\,dT}{T} + \frac{nRT\,dV/V}{T} = nC_V\frac{dT}{T}+nR\frac{dV}{V}.$$
Integration von Zustand 1 nach 2 liefert direkt die erste Formel. Die zweite folgt analog über $dH=T\,dS+V\,dp$. $\blacksquare$

<a id="satz-54-2-hauptsatz-entropiezunahme-in-abgeschlossenen-systemen"></a>
### Satz 5.4 (2. Hauptsatz — Entropiezunahme in abgeschlossenen Systemen)

**Aussage:** Für ein abgeschlossenes System gilt $\Delta S \geq 0$; Gleichheit genau dann, wenn der Prozess reversibel ist.

**Beweisidee:** Wird anhand des Beispiels von zwei Körpern unterschiedlicher Temperatur $T_1>T_2$, die in thermischen Kontakt gebracht werden, illustriert (kein allgemeiner Beweis, sondern paradigmatisches Beispiel — dies ist in der Vorlesung so behandelt worden). Man berechnet $\Delta S_1<0$ (kälterer Körper) und $\Delta S_2>0$ (wärmerer Körper verliert Wärme, aber bei tieferer effektiver Temperatur als der Empfänger sie erhält) und zeigt $\Delta S_{ges}=\Delta S_1+\Delta S_2 = mc\ln\dfrac{T_m^2}{T_1T_2} > 0$ für $T_1\neq T_2$ (mit Mischtemperatur $T_m=(T_1+T_2)/2$), unter Ausnutzung der Ungleichung vom arithmetisch-geometrischen Mittel.

**Bedeutung:** Formuliert die "Zeitrichtung" der Physik — Prozesse laufen spontan nur in Richtung wachsender Gesamtentropie.

<a id="satz-55-boltzmann-entropie-und-statistische-interpretation"></a>
### Satz 5.5 (Boltzmann-Entropie und statistische Interpretation)

**Aussage:** Die statistische Definition $S=k_B\ln W$ (Def. 5.4) ist konsistent mit der thermodynamischen Definition $dS=\delta Q_{rev}/T$.

**Beweisidee:** Wird am Beispiel der freien Expansion eines idealen Gases (Volumen $V_0\to V$) gezeigt: Die Anzahl der Realisierungsmöglichkeiten für $N_A$ Teilchen, alle im Volumen $V$ statt $V_0$ zu finden, skaliert wie $W\propto (V/V_0)^{N_A}$, also
$$S = k_B\ln W = k_B N_A\ln(V/V_0) = R\ln(V/V_0),$$
was exakt mit der thermodynamischen Formel $\Delta S=nR\ln(V_2/V_1)$ (aus Satz 5.3, isotherme Expansion) für $n=1\,\text{mol}$ übereinstimmt. **Konsequenz:** Entropie ist ein Maß für die Anzahl mikroskopischer Möglichkeiten — Systeme entwickeln sich spontan zum makroskopisch wahrscheinlichsten (= entropiereichsten) Zustand.

**Nernst'sches Theorem (3. Hauptsatz, ohne Beweis):** $\lim_{T\to0} S(T) = 0$ — bei $T=0$ existiert (idealisiert) nur ein einziger Mikrozustand ($W=1$), maximale Ordnung.

<a id="algorithmen-13"></a>
## Algorithmen

**Lösungsstrategie für Kreisprozess-Aufgaben**
- **Motivation:** Kreisprozessaufgaben kombinieren mehrere Zustandsänderungen aus Kapitel 4 — ohne systematisches Vorgehen verliert man leicht den Überblick.
- **Pseudocode:**
```
EINGABE: Kreisprozess (Folge von Teilschritten), Anfangszustand
1. Zeichne den Prozess im p-V-Diagramm (Orientierung! Uhrzeigersinn =
   Wärmekraftmaschine, Gegenuhrzeigersinn = Kältemaschine)
2. Berechne für JEDEN Teilschritt einzeln Q_i, W_i, ΔU_i
   (nutze die Formeln aus Kapitel 4, je nach Teilschritt-Typ)
3. Prüfe: Summe aller ΔU_i muss 0 sein (Kreisprozess!) — Kontrollrechnung
4. Bestimme Q_zu (Summe aller Q_i > 0) und Q_ab (Summe aller Q_i < 0)
5. η = |W_ges| / Q_zu = (Q_zu - |Q_ab|) / Q_zu
6. Falls Carnot: η direkt über 1 - T2/T1 (schneller als Einzelschritte!)
AUSGABE: η bzw. Leistungszahl ε
```
- **Korrektheitsidee:** Schritt 3 folgt direkt aus $U$ als Zustandsgröße (Def. 5.1); Schritt 5 aus Definition 5.2 kombiniert mit dem 1. Hauptsatz über den gesamten Zyklus.
- **Typische Fehler:** Vorzeichen von $Q_{ab}$ vergessen (es ist negativ definiert, im Wirkungsgrad wird der Betrag gebraucht); Carnot-Formel auf nicht-Carnot-Prozesse angewendet (nur Carnot erreicht $\eta_{Carnot}$, andere Prozesse haben i. A. geringeren Wirkungsgrad bei gleichen $T_1,T_2$).

<a id="beispiele-23"></a>
## Beispiele

**Beispiel 1 (leicht):** Eine Carnot-Maschine arbeitet zwischen $T_1=500\,\text{K}$ und $T_2=300\,\text{K}$. Berechne $\eta$.
*Lösung:* $\eta = 1-300/500 = 0{,}4 = 40\%$.

**Beispiel 2 (mittel):** Dieselbe Maschine nimmt pro Zyklus $Q_1=1000\,\text{J}$ auf. Wie viel Arbeit wird gewonnen, wie viel Wärme abgegeben?
*Lösung:* $|W|=\eta Q_1=400\,\text{J}$, $|Q_2|=Q_1-|W|=600\,\text{J}$.

**Beispiel 3 (mittel):** Eine Wärmepumpe (als Carnot-Kältemaschine betrieben) soll ein Haus bei $T_1=293\,\text{K}$ heizen, Außentemperatur $T_2=273\,\text{K}$. Berechne die Leistungszahl $\varepsilon=Q_1/W$.
*Lösung:* Für die Carnot-Wärmepumpe gilt $\varepsilon_{WP} = \dfrac{T_1}{T_1-T_2} = \dfrac{293}{20} \approx 14{,}65$ — pro Joule Arbeit werden $14{,}65\,\text{J}$ Wärme ins Haus gepumpt (deutlich effizienter als direkte elektrische Heizung, $\varepsilon=1$).

**Beispiel 4 (schwer):** $2\,\text{kg}$ Wasser bei $80\,°\text{C}$ werden mit $2\,\text{kg}$ Wasser bei $20\,°\text{C}$ gemischt ($c=4187\,\text{J/(kgK)}$). Berechne $\Delta S_{ges}$.
*Lösung:* Mischtemperatur $T_m = (353+293)/2 = 323\,\text{K}$. $\Delta S_1 = mc\ln(T_m/T_1) = 2\cdot4187\cdot\ln(323/353) \approx -757\,\text{J/K}$. $\Delta S_2 = 2\cdot4187\cdot\ln(323/293)\approx 829\,\text{J/K}$. $\Delta S_{ges}\approx 72\,\text{J/K} > 0$ ✓ (konsistent mit Satz 5.4).

**Beispiel 5 (schwer):** Vergleiche den Otto-Wirkungsgrad $\eta_{Otto}=1-(V_2/V_1)^{\kappa-1}$ mit dem Carnot-Wirkungsgrad zwischen den auftretenden Extremtemperaturen. Was fällt auf?
*Lösung:* Man zeigt (Rechenaufgabe mit Adiabatengleichungen), dass $\eta_{Otto} < \eta_{Carnot}(T_{max},T_{min})$ — konsistent mit Satz 5.2, da der Otto-Prozess nicht reversibel zwischen nur zwei konstanten Temperaturreservoiren abläuft (isochore Schritte durchlaufen ein Temperaturkontinuum).

<a id="gegenbeispiele-23"></a>
## Gegenbeispiele

- Ein Kreisprozess mit $\eta > \eta_{Carnot}(T_1,T_2)$ ist **unmöglich** (Satz 5.2) — falls eine Rechnung das ergibt, liegt ein Fehler vor.
- $\Delta S_{system} < 0$ ist möglich (z. B. Gas wird komprimiert) — der 2. Hauptsatz verlangt nur $\Delta S_{gesamt}$ (System + Umgebung) $\geq 0$, **nicht** dass die Entropie jedes Teilsystems für sich wächst.
- Ein "Perpetuum mobile 2. Art" (Maschine, die Wärme aus einem einzigen Reservoir vollständig in Arbeit umwandelt, ohne Abwärme) widerspricht dem 2. Hauptsatz und ist nie beobachtet worden — im Gegensatz zum 1. Hauptsatz, der ein solches Gerät nicht verbieten würde.

<a id="typische-klausuraufgaben-24"></a>
## Typische Klausuraufgaben

- Wirkungsgrad-/Leistungszahl-Berechnung für Carnot-Prozesse zwischen gegebenen Temperaturen — Erkennungsmerkmal: "reversibel", "idealer Kreisprozess", zwei Temperaturangaben.
- Vollständige Analyse eines 4-Schritt-Kreisprozesses (oft Otto oder Stirling) mit $p$-$V$-Diagramm — Strategie: Teilschritte einzeln mit Kapitel-4-Formeln durchrechnen.
- Entropieänderungsberechnung bei Mischungs- oder Wärmeleitungsprozessen — Erkennungsmerkmal: zwei Körper/Reservoire unterschiedlicher Temperatur.
- Qualitative Fragen: "Warum ist ein Perpetuum mobile 2. Art unmöglich?" — Strategie: Clausius- oder Kelvin-Planck-Formulierung zitieren und mit Entropieargument verknüpfen.

<a id="typische-fehler-24"></a>
## Typische Fehler

1. Carnot-Wirkungsgrad wird mit Temperaturen in $°\text{C}$ statt Kelvin berechnet — führt zu falschen (oft negativen oder >1) Ergebnissen. **Immer Kelvin verwenden!**
2. $\eta$ und $\varepsilon$ (Leistungszahl) verwechselt — unterschiedliche Definitionen für Wärmekraftmaschine vs. Kältemaschine/Wärmepumpe.
3. Vorzeichen von $Q_{ab}$ bei der Wirkungsgradberechnung ignoriert.
4. Entropieänderung eines Teilsystems ($\Delta S<0$ möglich!) wird fälschlich als Verletzung des 2. Hauptsatzes interpretiert — nur die **Gesamtentropie** muss zunehmen.
5. Bei Nicht-Carnot-Kreisprozessen wird trotzdem die Carnot-Formel $\eta=1-T_2/T_1$ verwendet (nur für Carnot exakt gültig).

<a id="verbindungen-25"></a>
## Verbindungen

- Baut vollständig auf Kapitel 4 auf (jeder Kreisprozess = Abfolge der vier Standardprozesse).
- Die **statistische Entropie** (Satz 5.5) verbindet dieses Kapitel zurück zu Kapitel 2 (kinetische Gastheorie, mikroskopische Beschreibung) — beide zeigen, wie makroskopische Größen aus dem Zählen/Mitteln über viele Mikrozustände entstehen.
- Das Konzept "Zustandsgröße vs. Prozessgröße" wird in der Elektrodynamik wiederkehren: das **elektrische Potential** (Kapitel 6) ist eine Zustandsgröße (wegunabhängig), die Arbeit im Allgemeinen nicht.
- Schließt Teil I des Skripts ab; Teil II (Elektromagnetismus) beginnt mit einem strukturell komplett neuen, aber mathematisch ähnlichen Werkzeugkasten (Felder, Flussintegrale, Erhaltungssätze).

<a id="zusammenfassung-13"></a>
## Zusammenfassung

- Kreisprozess: $\oint dU=0$; Wirkungsgrad $\eta=|W|/Q_{zu}$.
- **Carnot-Wirkungsgrad** $\eta_{Carnot}=1-T_2/T_1$ ist die obere Schranke für *jede* Wärmekraftmaschine (Carnot'scher Satz).
- **Entropie**: thermodynamisch $dS=\delta Q_{rev}/T$, statistisch $S=k_B\ln W$ — beide Definitionen sind konsistent.
- **2. Hauptsatz**: $\Delta S_{gesamt}\geq 0$ für abgeschlossene Systeme; Gleichheit nur bei reversiblen Prozessen.
- Perpetuum mobile 1. Art (verletzt 1. HS) und 2. Art (verletzt 2. HS) sind beide unmöglich, aus unterschiedlichen Gründen.
- 3. Hauptsatz (Nernst): $S\to0$ für $T\to0$.

---

*Ende Teil I. Teil II (Elektromagnetismus: Elektrostatik, elektrischer Strom, Magnetismus, Elektrodynamik, Wechselstrom, elektromagnetische Wellen) folgt in gleicher Tiefe im nächsten Schritt.*



---

<a id="physik-ii-vollständiges-skript-1"></a>
# Physik II — Vollständiges Skript
<a id="teil-ii-elektromagnetismus"></a>
## Teil II: Elektromagnetismus

> Fortsetzung von Teil I (Mechanik der Fluide und Wärmelehre). Gleiche didaktische Tiefe, gleiche Notationskonventionen.

---

<a id="inhaltsverzeichnis-teil-ii"></a>
# Inhaltsverzeichnis Teil II

6. Elektrostatik I: Ladung, Coulombgesetz, elektrisches Feld, Potential
7. Elektrostatik II: Gauß'sches Gesetz, Leiter, Kondensatoren
8. Elektrostatik III: Dielektrika — Materie im elektrischen Feld
9. Elektrischer Strom und Gleichstromkreise
10. Ladungstransport in Materialien
11. Magnetismus I: Kraftwirkungen (Lorentzkraft)
12. Magnetismus II: Feldquellen und magnetische Materialien
13. Elektrodynamik: Induktion
14. Wechselstromkreise
15. Elektromagnetische Wellen

---

<a id="kapitel-6-elektrostatik-i-ladung-coulombgesetz-elektrisches-feld-potential"></a>
# Kapitel 6: Elektrostatik I — Ladung, Coulombgesetz, elektrisches Feld, Potential

<a id="motivation-26"></a>
## Motivation

Die Gravitation kennt nur eine "Sorte" Masse und immer Anziehung. Elektrische Ladung ist reichhaltiger: Es gibt zwei Vorzeichen, Ladungen stoßen sich ab oder ziehen sich an, und die Kraft ist um viele Größenordnungen stärker als die Gravitation (das Verhältnis Coulombkraft/Gravitationskraft zwischen zwei Elektronen ist $\sim 10^{42}$!). Warum brauchen wir trotzdem ein eigenes Kapitel, obwohl die Formel dem Gravitationsgesetz zum Verwechseln ähnlich sieht? Weil das *Konzept des Feldes*, das wir hier einführen, weit über die Elektrostatik hinausgeht — es ist die Sprache, in der die gesamte moderne Physik (inkl. Quantenfeldtheorie) geschrieben ist. Historisch entstand das Feldkonzept bei Faraday (empirisch, über Feldlinien) und wurde von Maxwell mathematisch präzisiert.

<a id="intuition-26"></a>
## Intuition

Stell dir eine Ladung nicht als isolierten Punkt vor, sondern als etwas, das den *gesamten umgebenden Raum* verändert — so wie eine Masse die Raumzeit krümmt (nur hier einfacher: sie erzeugt ein Vektorfeld). Eine zweite Ladung "spürt" nicht die erste Ladung direkt (das wäre Fernwirkung), sondern reagiert nur auf das *lokale* Feld an ihrem eigenen Ort. Das Feld ist wie eine unsichtbare "Strömung", die von positiven Ladungen ausgeht und in negativen endet — genau wie die Stromfäden aus Kapitel 1, nur ohne dass tatsächlich etwas fließt.

Das **Potential** ist die elektrische Analogie zur Höhe in einem Gravitationsfeld: Genauso wie ein Ball von selbst bergab rollt (zu niedrigerer potentieller Energie), bewegt sich eine positive Ladung von selbst zu niedrigerem Potential. Der Vorteil des Potentials: Es ist ein **Skalar** (eine Zahl pro Ort), viel einfacher zu handhaben als das vektorielle Feld — und aus ihm lässt sich das Feld durch Gradientenbildung vollständig zurückgewinnen.

<a id="formale-definitionen-26"></a>
## Formale Definitionen

**Definition 6.1 (Elektrische Ladung).**
Ladung $q$ ist eine additive, erhaltene, quantisierte skalare Eigenschaft der Materie. Die kleinste (frei existierende) Ladungseinheit ist die Elementarladung
$$e = 1{,}602\cdot10^{-19}\,\text{C}, \qquad q = z\cdot e,\ z\in\mathbb Z.$$
(Quarks tragen $\pm\tfrac13e,\pm\tfrac23e$, sind aber nicht frei/isoliert beobachtbar.)

**Definition 6.2 (Coulombgesetz).**
Die Kraft, die eine Punktladung $q_1$ auf eine Punktladung $q_2$ im Abstand $r$ ausübt:
$$\vec F_C = \frac{1}{4\pi\varepsilon_0}\frac{q_1q_2}{r^2}\,\hat e_r,$$
mit der **elektrischen Feldkonstante** (Permittivität des Vakuums) $\varepsilon_0 = 8{,}854\cdot10^{-12}\,\text{C}^2/(\text{N}\,\text{m}^2)$, wobei $\hat e_r$ vom Ort der Quellladung zur betrachteten Ladung zeigt.

**Definition 6.3 (Elektrisches Feld).**
$$\vec E(\vec r) := \lim_{q\to 0}\frac{\vec F_C(\vec r)}{q} = \frac{1}{4\pi\varepsilon_0}\frac{Q}{r^2}\hat e_r \quad\text{(Feld einer Punktladung $Q$)},\qquad [\vec E]=\frac{\text{N}}{\text{C}}=\frac{\text{V}}{\text{m}}.$$
Der Grenzwert $q\to0$ ("Probeladung") stellt sicher, dass das Feld eine Eigenschaft der *Quelle* ist, nicht der Testladung (die das Quellfeld sonst selbst stören würde).

**Definition 6.4 (Superpositionsprinzip).**
Für $n$ Punktladungen $q_i$ an Orten $\vec r_i$:
$$\vec E(\vec r) = \frac{1}{4\pi\varepsilon_0}\sum_{i=1}^n q_i\,\frac{\vec r-\vec r_i}{|\vec r-\vec r_i|^3}.$$
Für eine kontinuierliche Ladungsverteilung $\rho(\vec r')$:
$$\vec E(\vec r) = \frac{1}{4\pi\varepsilon_0}\int_V \rho(\vec r')\,\frac{\vec r-\vec r'}{|\vec r-\vec r'|^3}\,dV'.$$

**Definition 6.5 (Potentielle Energie und elektrisches Potential).**
Die Arbeit, eine Ladung $q$ von $A$ nach $B$ gegen das Feld zu bewegen:
$$W_{A\to B} = -\int_A^B \vec F_C\cdot d\vec r = q\big(\phi(\vec r_A)-\phi(\vec r_B)\big),$$
mit dem **elektrischen Potential**
$$\phi(\vec r) := \frac{E_{pot}(\vec r)}{q}, \qquad \phi(\vec r) = \frac{1}{4\pi\varepsilon_0}\frac{Q}{r}\ \text{(Punktladung, Konvention } \phi(\infty)=0\text{)}.$$
Die **Spannung** ist die Potentialdifferenz: $U := \phi(\vec r_A)-\phi(\vec r_B)$, $[U]=\text{V}$.

**Definition 6.6 (Zusammenhang Feld — Potential).**
$$\vec E = -\nabla\phi = -\operatorname{grad}\phi.$$

**Definition 6.7 (Elektrischer Dipol).**
Zwei Ladungen $+Q$, $-Q$ im Abstand $\vec d$ (von $-$ nach $+$ zeigend). Das **Dipolmoment**:
$$\vec p := Q\,\vec d, \qquad [\vec p] = \text{C}\,\text{m}.$$
Im Fernfeld ($R\gg d$):
$$\phi(\vec R) \approx \frac{1}{4\pi\varepsilon_0}\frac{\vec p\cdot\hat R}{R^2}, \qquad \vec E(\vec R)\approx\frac{1}{4\pi\varepsilon_0 R^3}\big(3(\vec p\cdot\hat R)\hat R-\vec p\big).$$

<a id="eigenschaften-22"></a>
## Eigenschaften

| Eigenschaft | Aussage | Begründung |
|---|---|---|
| Ladungserhaltung | $Q_{ges}=\text{const}$ in einem abgeschlossenen System | Fundamentales Naturgesetz, nie verletzt beobachtet |
| $\vec F_C$ ist konservativ | $\oint \vec F_C\cdot d\vec r = 0$ | Zentralkraft, $\propto 1/r^2$ — wie Gravitation |
| $\vec E$ additiv (Superposition) | siehe Def. 6.4 | Coulombkraft ist linear in den Quellladungen |
| $\phi$ additiv, aber skalar | einfacher zu addieren als $\vec E$ | Skalare Summe statt Vektorsumme — Rechenvorteil! |
| Feldlinien | beginnen an $+$, enden an $-$ (oder im Unendlichen); Dichte $\propto |\vec E|$ | Veranschaulichung von Def. 6.3/6.4 |
| Kraft auf Dipol im homogenen Feld | $\vec F=0$, aber Drehmoment $\vec M=\vec p\times\vec E\neq0$ | Kräfte auf $+Q$ und $-Q$ heben sich auf, Angriffspunkte unterschiedlich |
| Kraft auf Dipol im inhomogenen Feld | $\vec F = (\vec p\cdot\nabla)\vec E \neq 0$ | Feldstärke an den beiden Polen unterschiedlich |
| Potentielle Energie des Dipols | $E_{pot}=-\vec p\cdot\vec E$ | minimal, wenn $\vec p\parallel\vec E$ (Dipol richtet sich aus) |

<a id="sätze-22"></a>
## Sätze

<a id="satz-61-wegunabhängigkeit-der-arbeit-im-elektrostatischen-feld"></a>
### Satz 6.1 (Wegunabhängigkeit der Arbeit im elektrostatischen Feld)

**Aussage:** $W_{A\to B}$ hängt nur von den Endpunkten $A,B$ ab, nicht vom gewählten Weg.

**Voraussetzungen:** elektrostatisches (zeitunabhängiges) Feld einer ruhenden Ladungsverteilung.

**Bedeutung:** Rechtfertigt die Existenz eines Potentials $\phi$ — ohne Wegunabhängigkeit wäre $\phi(\vec r)$ als eindeutige Funktion des Ortes gar nicht definierbar.

**Beweisidee (Beweisstil: Rückführung auf Zentralkraft, analog zur Mechanik).** Die Coulombkraft ist eine Zentralkraft ($\vec F\parallel \hat e_r$, Betrag nur von $r$ abhängig). Für jede Zentralkraft $\vec F(r) = f(r)\hat e_r$ ist $\vec F = -\nabla V(r)$ mit $V(r)=-\int f(r)\,dr$ erfüllt (elementare Vektoranalysis: der Gradient einer nur radial abhängigen Funktion zeigt radial). Damit ist $\vec F$ ein Gradientenfeld, und Gradientenfelder sind per Definition wegunabhängig integrierbar (Hauptsatz für Kurvenintegrale). $\blacksquare$

<a id="satz-62-feld-einer-unendlich-ausgedehnten-geladenen-platte"></a>
### Satz 6.2 (Feld einer unendlich ausgedehnten geladenen Platte)

**Aussage:** Für eine unendlich ausgedehnte Ebene mit Flächenladungsdichte $\sigma=Q/A$ ist das Feld senkrecht zur Platte, homogen und ortsunabhängig:
$$\vec E = \frac{\sigma}{2\varepsilon_0}\,\hat e_n.$$

**Voraussetzungen:** unendlich ausgedehnte Fläche (Randeffekte vernachlässigt), homogene Flächenladungsdichte.

**Beweis (Beweisstil: direkte Integration über Def. 6.4, Ausnutzung der Symmetrie).**

Wir zerlegen die Platte in konzentrische Ringe um den Fußpunkt des Lots vom Aufpunkt $P$ (Abstand $z$ von der Platte). Ein Ring bei Radius $r$, Breite $dr$, trägt die Ladung $dQ = \sigma\cdot 2\pi r\,dr$. Sein Beitrag zum Feld in $P$ hat wegen der Kreissymmetrie nur eine Komponente entlang der Flächennormalen $\hat e_n$ (die Radialkomponenten aller Punkte auf dem Ring heben sich paarweise auf):
$$dE_z = \frac{1}{4\pi\varepsilon_0}\frac{dQ}{R^2}\cos\alpha, \qquad R^2=z^2+r^2,\quad \cos\alpha=\frac{z}{R}.$$
Also
$$dE_z = \frac{\sigma}{4\pi\varepsilon_0}\frac{2\pi r\,dr\cdot z}{(z^2+r^2)^{3/2}} = \frac{\sigma z}{2\varepsilon_0}\frac{r\,dr}{(z^2+r^2)^{3/2}}.$$
Integration über alle Ringe ($r:0\to\infty$), mit Substitution $u=z^2+r^2$, $du=2r\,dr$:
$$E_z = \frac{\sigma z}{2\varepsilon_0}\int_{z^2}^{\infty} \frac{du/2}{u^{3/2}} = \frac{\sigma z}{2\varepsilon_0}\Big[-u^{-1/2}\Big]_{z^2}^{\infty} = \frac{\sigma z}{2\varepsilon_0}\cdot\frac1z = \frac{\sigma}{2\varepsilon_0}.$$
Das Ergebnis ist unabhängig von $z$ — das Feld ist homogen. $\blacksquare$

**Konsequenz:** Für einen Plattenkondensator (zwei Platten mit $+\sigma$, $-\sigma$) addieren sich die Felder zwischen den Platten ($\vec E_1,\vec E_2$ gleichgerichtet) und heben sich außerhalb auf:
$$E_{innen} = \frac{\sigma}{2\varepsilon_0}+\frac{\sigma}{2\varepsilon_0}=\frac{\sigma}{\varepsilon_0}, \qquad E_{außen}=0.$$

<a id="algorithmen-14"></a>
## Algorithmen

**Lösungsstrategie für Feld-/Potentialberechnungen mit Superposition**
- **Motivation:** Bei komplexen Ladungsverteilungen ist die direkte Integration oft die einzige Methode (bevor in Kapitel 7 das Gauß'sche Gesetz als Abkürzung für symmetrische Fälle eingeführt wird).
- **Pseudocode:**
```
EINGABE: Ladungsverteilung (diskret oder kontinuierlich ρ(r'))
1. Wähle Koordinatensystem passend zur Symmetrie der Verteilung
2. WENN diskrete Ladungen:
     E(r) = (1/4πε0) * Σ q_i (r-r_i)/|r-r_i|³   (vektoriell aufsummieren!)
3. WENN kontinuierliche Verteilung:
     a. Zerlege in Ladungselemente dQ = ρ dV (bzw. σ dA, λ dl)
     b. Nutze Symmetrie: welche Feldkomponenten heben sich weg?
     c. Integriere nur die verbleibende(n) Komponente(n)
4. Für Potential: gleiches Vorgehen, aber skalar (einfacher!) —
     φ(r) = (1/4πε0) ∫ dQ / |r-r'|
5. Falls E gesucht, aber φ bereits bekannt: E = -grad(φ)
AUSGABE: E(r) oder φ(r)
```
- **Korrektheitsidee:** Direkte Anwendung von Def. 6.4 (Superposition), abgesichert durch die Linearität der Coulombkraft.
- **Typische Fehler:** Vektorielle Integration wird versehentlich skalar durchgeführt (Feldkomponenten, die sich eigentlich aufheben sollten, werden addiert); Symmetrie wird nicht ausgenutzt, was zu unnötig komplizierten Integralen führt.

<a id="beispiele-24"></a>
## Beispiele

**Beispiel 1 (leicht):** Zwei Punktladungen $q_1=2\,\mu\text{C}$, $q_2=-3\,\mu\text{C}$ im Abstand $10\,\text{cm}$. Berechne die Kraft.
*Lösung:* $F=\dfrac{1}{4\pi\varepsilon_0}\dfrac{|q_1q_2|}{r^2} = 9\cdot10^9\cdot\dfrac{6\cdot10^{-12}}{0{,}01}\approx5{,}4\,\text{N}$ (anziehend, da unterschiedliches Vorzeichen).

**Beispiel 2 (leicht):** Berechne $\vec E$ im Abstand $r=1\,\text{m}$ von $Q=1\,\mu\text{C}$.
*Lösung:* $E = \dfrac{1}{4\pi\varepsilon_0}\dfrac{Q}{r^2} = 9\cdot10^9\cdot10^{-6} = 9000\,\text{V/m}$.

**Beispiel 3 (mittel):** Berechne das Potential im Mittelpunkt zwischen zwei Ladungen $+Q$ und $-Q$ im Abstand $2a$.
*Lösung:* Wegen Symmetrie (gleicher Abstand $a$, aber entgegengesetztes Vorzeichen): $\phi = \dfrac{1}{4\pi\varepsilon_0}\left(\dfrac{Q}{a}+\dfrac{-Q}{a}\right)=0$ — Achtung: $\vec E$ ist dort **nicht** null (die Feldbeiträge addieren sich, da $\vec E$ Vektor ist)! Wichtiges Gegenbeispiel für "$\phi=0\Rightarrow\vec E=0$".

**Beispiel 4 (mittel):** Ein Dipol ($p=3{,}3\cdot10^{-30}\,\text{C m}$, typisch für ein Wassermolekül) steht im homogenen Feld $E=10^5\,\text{V/m}$ senkrecht zu $\vec p$. Berechne das Drehmoment.
*Lösung:* $M = pE\sin(90°) = 3{,}3\cdot10^{-30}\cdot10^5 = 3{,}3\cdot10^{-25}\,\text{N m}$.

**Beispiel 5 (schwer):** Berechne das Feld auf der Achse eines geladenen Rings (Radius $R$, Ladung $Q$) im Abstand $z$ vom Mittelpunkt.
*Lösung:* Analog zu Satz 6.2, aber jetzt ist der "Ring" selbst die Quelle (nicht eine Scheibe von Ringen). Jedes Ladungselement $dQ=Q\,d\theta/(2\pi)$ trägt $dE_z = \dfrac{1}{4\pi\varepsilon_0}\dfrac{dQ\,z}{(z^2+R^2)^{3/2}}$ bei (Radialkomponenten heben sich durch Symmetrie auf). Integration über den vollen Ring ($\int dQ=Q$):
$$E_z = \frac{1}{4\pi\varepsilon_0}\frac{Qz}{(z^2+R^2)^{3/2}}.$$
Für $z\gg R$ geht dies gegen $\dfrac{1}{4\pi\varepsilon_0}\dfrac{Q}{z^2}$ (Punktladungslimes) — eine wichtige Plausibilitätsprüfung für jede Feldberechnung ausgedehnter Ladungsverteilungen.

<a id="gegenbeispiele-24"></a>
## Gegenbeispiele

- $\phi=0$ an einem Punkt bedeutet **nicht** $\vec E=0$ dort (siehe Beispiel 3) — Potential ist ein Skalar, Nullstellen sagen nichts über den Gradienten aus.
- Die Coulombkraft ist **nicht** additiv im Sinne "Kraft auf $q_3$ hängt nur von $q_1$ und $q_3$ ab" — sie ist additiv im Sinne von Def. 6.4 (Vektorsumme *aller* Einzelkräfte); ein Missverständnis führt oft zu falscher Vernachlässigung einer dritten Ladung.
- Die Formel für das Plattenfeld ($E=\sigma/\varepsilon_0$ zwischen den Platten) gilt **nicht** an den Rändern eines endlichen Kondensators (dort treten Streufelder auf — die Näherung "unendlich ausgedehnt" versagt).

<a id="typische-klausuraufgaben-25"></a>
## Typische Klausuraufgaben

- Kraft-/Feldberechnung zwischen mehreren Punktladungen — Erkennungsmerkmal: konkrete Ladungswerte und Abstände, oft mit Vektoraddition in 2D.
- Feld-/Potentialberechnung für symmetrische Ladungsverteilungen (Ring, Platte, Linie) durch direkte Integration — Strategie: Symmetrie zuerst ausnutzen, dann integrieren.
- Kraft/Drehmoment auf einen Dipol im homogenen/inhomogenen Feld — Erkennungsmerkmal: "Dipol", "polares Molekül".
- Kombination Kraft + Bewegung (z. B. Ladung im homogenen Feld beschleunigt, ballistische Bahn) — nutzt Mechanik-Grundlagen aus Teil I.

<a id="typische-fehler-25"></a>
## Typische Fehler

1. $\vec E$ und $\phi$ werden verwechselt (Vektor vs. Skalar) — Nullstellen des einen implizieren nicht das andere.
2. Vorzeichenfehler bei $\hat e_r$ (Richtung von Quelle zu Aufpunkt, nicht umgekehrt).
3. Bei Superposition wird vektoriell statt komponentenweise summiert (v. a. bei nicht-kollinearen Ladungsanordnungen).
4. Grenzfall-Check wird vergessen (z. B. $z\gg R$ sollte immer auf die Punktladungsformel zurückführen — guter Fehlerindikator).

<a id="verbindungen-26"></a>
## Verbindungen

- Das Superpositionsprinzip (Def. 6.4) und die direkte Integration werden in Kapitel 7 durch das viel effizientere **Gauß'sche Gesetz** ergänzt (für symmetrische Fälle).
- Der Zusammenhang $\vec E=-\nabla\phi$ ist strukturell identisch zum Zusammenhang zwischen konservativer Kraft und potentieller Energie in der Mechanik (Teil I, vgl. Satz 6.1-Beweis).
- Das **Dipolmoment** taucht in Kapitel 8 (Dielektrika, induzierte Dipole) und in Kapitel 12 (magnetisches Dipolmoment) in enger struktureller Analogie wieder auf.

<a id="zusammenfassung-14"></a>
## Zusammenfassung

- Coulombgesetz: $\vec F_C=\dfrac{1}{4\pi\varepsilon_0}\dfrac{q_1q_2}{r^2}\hat e_r$; elektrisches Feld $\vec E=\vec F_C/q$.
- Superposition gilt für $\vec E$ (vektoriell) und $\phi$ (skalar, einfacher).
- $\vec E=-\nabla\phi$; $U=\phi_A-\phi_B$.
- Elektrischer Dipol: $\vec p=Q\vec d$; $\vec M=\vec p\times\vec E$, $E_{pot}=-\vec p\cdot\vec E$.
- Feld einer unendlichen Platte: $E=\sigma/(2\varepsilon_0)$; im Plattenkondensator $E=\sigma/\varepsilon_0$.

---

<a id="kapitel-7-elektrostatik-ii-gaußsches-gesetz-leiter-kondensatoren"></a>
# Kapitel 7: Elektrostatik II — Gauß'sches Gesetz, Leiter, Kondensatoren

<a id="motivation-27"></a>
## Motivation

Die direkte Integration aus Kapitel 6 ist für symmetrische Ladungsverteilungen (Kugel, Zylinder, Ebene) unnötig aufwendig. Gauß erkannte: Es gibt einen tieferen Zusammenhang zwischen dem elektrischen Fluss durch eine *geschlossene* Fläche und der eingeschlossenen Ladung — unabhängig von der genauen Form der Fläche. Das ist keine neue Physik (es folgt direkt aus dem Coulombgesetz), sondern ein mächtiges *mathematisches Werkzeug*, das symmetrische Probleme drastisch vereinfacht — dieselbe Idee wie die Kontinuitätsgleichung in Kapitel 1, nur für das elektrische Feld statt für Massenstromdichte.

<a id="intuition-27"></a>
## Intuition

Stell dir das elektrische Feld als Strömung vor (wie in Kapitel 6 angedeutet). Der "Fluss" durch eine Fläche misst, wie viele Feldlinien hindurchtreten. Eine geladene Kugel im Zentrum einer beliebigen umschließenden Fläche "strahlt" eine feste Anzahl Feldlinien aus — egal ob die umschließende Fläche eine Kugel, ein Würfel oder eine verbeulte Kartoffel ist, es treten immer gleich viele Feldlinien hindurch, weil keine Feldlinien im ladungsfreien Raum entstehen oder enden können. Das ist der Kern des Gauß'schen Gesetzes.

Bei **Leitern** ist die Kernidee: Ladungen sind frei beweglich. Im Gleichgewicht müssen sie sich so anordnen, dass im Inneren $\vec E=0$ ist — sonst würden die freien Ladungen weiter beschleunigt (es gäbe kein Gleichgewicht). Das ist wie Wasser in einem Gefäß: Es fließt so lange, bis die Oberfläche eben ist (Kräftegleichgewicht) — bei Leitern ist die "ebene Oberfläche" der Zustand $\vec E_{innen}=0$.

<a id="formale-definitionen-27"></a>
## Formale Definitionen

**Definition 7.1 (Elektrischer Fluss).**
$$\Phi_{el} := \int_A \vec E\cdot d\vec A,$$
mit Flächennormalenvektor $d\vec A$ (bei geschlossenen Flächen konventionell nach außen orientiert).

**Definition 7.2 (Leiter, elektrostatisches Gleichgewicht).**
Ein Leiter enthält frei bewegliche Ladungsträger. Im elektrostatischen Gleichgewicht gilt im Inneren des Leiters $\vec E_{innen}=0$ und das gesamte Leitermaterial ist eine Äquipotentialfläche ($\phi=\text{const}$).

**Definition 7.3 (Kapazität).**
$$C := \frac{Q}{U}, \qquad [C]=\text{F (Farad)} = \text{C/V}.$$

**Definition 7.4 (Energiedichte des elektrischen Feldes).**
$$w_{el} := \frac{1}{V}\int_{Aufladung} \delta W = \frac12\varepsilon_0 E^2, \qquad [w_{el}]=\text{J/m}^3.$$

<a id="eigenschaften-23"></a>
## Eigenschaften

| Eigenschaft | Aussage | Kurzbegründung |
|---|---|---|
| Feld im Leiterinneren | $\vec E=0$ | sonst würden freie Ladungen weiterfließen (kein GGW) |
| Ladung sitzt auf der Oberfläche | $\rho_{innen}=0$ | folgt aus Gauß'schem Gesetz angewendet auf $\vec E=0$-Region |
| $\vec E$ senkrecht zur Leiteroberfläche | $\vec E \perp$ Oberfläche | sonst würde eine Tangentialkomponente Ladung entlang der Oberfläche verschieben |
| Hohlleiter, keine Ladung im Hohlraum | $\vec E=0$ im Hohlraum, unabhängig vom Außenfeld | Faraday-Käfig-Prinzip |
| Kondensatoren, Reihenschaltung | $\dfrac1{C_{ges}}=\sum\dfrac1{C_i}$ | $U$ addiert sich, $Q$ gleich auf allen |
| Kondensatoren, Parallelschaltung | $C_{ges}=\sum C_i$ | $U$ gleich auf allen, $Q$ addiert sich |

<a id="sätze-23"></a>
## Sätze

<a id="satz-71-gaußsches-gesetz-integral"></a>
### Satz 7.1 (Gauß'sches Gesetz, integral)

**Aussage:**
$$\oint_S \vec E\cdot d\vec A = \frac{Q_{innen}}{\varepsilon_0}.$$

**Voraussetzungen:** $S$ geschlossene Fläche; $Q_{innen}$ = gesamte von $S$ eingeschlossene Ladung.

**Bedeutung:** Eine der vier Maxwell-Gleichungen (integral). Äquivalent zum Coulombgesetz, aber viel einfacher anwendbar bei Symmetrie.

**Beweis (Beweisstil: Nachweis für Punktladung + Superposition, dann Verallgemeinerung).**

*Schritt 1 — Punktladung, Kugel als Gauß-Fläche:* Für eine Punktladung $Q$ im Zentrum einer Kugel vom Radius $R$: $\vec E$ ist überall auf der Kugeloberfläche radial und vom gleichen Betrag $E=\dfrac{1}{4\pi\varepsilon_0}\dfrac{Q}{R^2}$ (Def. 6.3), also
$$\oint_S\vec E\cdot d\vec A = E\cdot 4\pi R^2 = \frac{1}{4\pi\varepsilon_0}\frac{Q}{R^2}\cdot4\pi R^2 = \frac{Q}{\varepsilon_0}.$$

*Schritt 2 — beliebige Fläche um dieselbe Punktladung:* Der Raumwinkel, den ein Flächenelement $dA$ vom Ladungsort aus einnimmt, ist $d\Omega = \dfrac{dA\cos\alpha}{R^2}$ ($\alpha$ Winkel zwischen $\vec E$ und Flächennormale). Damit ist $\vec E\cdot d\vec A = E\,dA\cos\alpha = \dfrac{Q}{4\pi\varepsilon_0}\,d\Omega$, und die Integration über eine *beliebige* geschlossene Fläche, die die Ladung umschließt, liefert $\oint d\Omega=4\pi$ (voller Raumwinkel), also wieder $Q/\varepsilon_0$ — unabhängig von der Form.

*Schritt 3 — Ladung außerhalb der Fläche:* Jede Feldlinie, die eintritt, tritt auch wieder aus (Raumwinkelbeiträge heben sich auf) → Netto-Fluss $=0$.

*Schritt 4 — viele Ladungen (Superposition, Def. 6.4):* Da $\vec E$ additiv ist, ist auch $\Phi_{el}$ additiv. Für mehrere Punktladungen (bzw. eine kontinuierliche Verteilung) tragen nach Schritt 2/3 nur die *innerhalb* liegenden Ladungen bei, jede mit $q_i/\varepsilon_0$. Summation liefert $Q_{innen}/\varepsilon_0$. $\blacksquare$

<a id="satz-72-gaußsches-gesetz-differentiell-1-maxwell-gleichung"></a>
### Satz 7.2 (Gauß'sches Gesetz, differentiell — 1. Maxwell-Gleichung)

**Aussage:** $$\operatorname{div}\vec E(\vec r) = \frac{1}{\varepsilon_0}\rho(\vec r).$$

**Beweis (Beweisstil: direkte Anwendung des Satzes von Gauß auf Satz 7.1).**
$$\oint_S\vec E\cdot d\vec A \overset{\text{Gauß-Integralsatz}}{=} \int_V \operatorname{div}\vec E\, dV \overset{\text{Satz 7.1}}{=} \frac{Q_{innen}}{\varepsilon_0} = \frac1{\varepsilon_0}\int_V\rho\,dV.$$
Da $V$ beliebig ist, folgt punktweise Gleichheit der Integranden. $\blacksquare$

**Konsequenz:** Mit $\vec E=-\nabla\phi$ (Def. 6.6) folgt die **Poisson-Gleichung**
$$\Delta\phi(\vec r) = -\frac{1}{\varepsilon_0}\rho(\vec r),$$
bzw. im ladungsfreien Raum die **Laplace-Gleichung** $\Delta\phi=0$.

<a id="satz-73-feld-einer-geladenen-kugel-innen-und-außen"></a>
### Satz 7.3 (Feld einer geladenen Kugel — innen und außen)

**Aussage:** Für eine gleichmäßig geladene Kugelschale/Kugel (Gesamtladung $Q$, Radius $R$):
$$E(r) = 0 \ (r<R), \qquad E(r) = \frac{1}{4\pi\varepsilon_0}\frac{Q}{r^2}\ (r>R).$$

**Beweis (Beweisstil: Anwendung Gauß'sches Gesetz mit kugelsymmetrischer Gauß-Fläche).**
Wegen Kugelsymmetrie ist $\vec E=E(r)\hat e_r$. Wähle als Gauß-Fläche eine konzentrische Kugel vom Radius $r$:
$$\oint\vec E\cdot d\vec A = E(r)\cdot4\pi r^2 = \frac{Q_{innen}}{\varepsilon_0}.$$
Für $r<R$ (Hohlkugel, Ladung nur auf der Oberfläche bei $R$): $Q_{innen}=0\Rightarrow E=0$.
Für $r>R$: $Q_{innen}=Q\Rightarrow E(r)=\dfrac{Q}{4\pi\varepsilon_0r^2}$ — von außen sieht die Kugel exakt wie eine Punktladung aus. $\blacksquare$

<a id="satz-74-kondensatorformeln"></a>
### Satz 7.4 (Kondensatorformeln)

| Kondensatortyp | Kapazität | Herleitungsidee |
|---|---|---|
| Plattenkondensator | $C=\varepsilon_0\dfrac{A}{d}$ | $E=\sigma/\varepsilon_0$ (Satz 6.2-Konsequenz), $U=Ed$, $Q=\sigma A$ |
| Kugelkondensator (Radien $a<b$) | $C=\dfrac{4\pi\varepsilon_0}{1/a-1/b}$ | $U=\phi(a)-\phi(b)$ mit $\phi(r)=Q/(4\pi\varepsilon_0r)$ (Satz 7.3) |
| Einzelkugel ($b\to\infty$) | $C=4\pi\varepsilon_0a$ | Grenzfall des Kugelkondensators |

**Beweis (Plattenkondensator, Beweisstil: direkte Kombination bereits bewiesener Sätze).**
Aus Satz 6.2 (Konsequenz): $E=\sigma/\varepsilon_0$ zwischen den Platten. Da $\vec E$ homogen ist, gilt $U=\int\vec E\cdot d\vec r = E\cdot d = \dfrac{\sigma d}{\varepsilon_0} = \dfrac{Qd}{\varepsilon_0A}$. Also $C=Q/U = \varepsilon_0A/d$. $\blacksquare$

<a id="satz-75-energie-des-elektrischen-feldes-im-kondensator"></a>
### Satz 7.5 (Energie des elektrischen Feldes im Kondensator)

**Aussage:** $$W = \frac12CU^2 = \frac{Q^2}{2C} = \frac12 QU.$$

**Beweis (Beweisstil: Integration der Aufladearbeit).**
Beim Aufladen wird in jedem Moment die Ladung $dQ$ gegen die bereits vorhandene Spannung $U(Q)=Q/C$ transportiert: $\delta W = U\,dQ = \dfrac{Q}{C}dQ$. Integration von $0$ bis $Q_{end}$:
$$W = \int_0^{Q}\frac{Q'}{C}dQ' = \frac{Q^2}{2C} = \frac12 CU^2. \qquad\blacksquare$$
Mit $C=\varepsilon_0A/d$ und $U=Ed$: $W=\tfrac12\varepsilon_0E^2\cdot(Ad)=\tfrac12\varepsilon_0E^2\cdot V$, was die Energiedichte $w_{el}=\tfrac12\varepsilon_0E^2$ (Def. 7.4) bestätigt — die Feldenergie ist also **im Feld selbst** gespeichert, nicht "an den Ladungen".

<a id="algorithmen-15"></a>
## Algorithmen

**Lösungsstrategie: Gauß'sches Gesetz anwenden**
- **Motivation:** Das Gauß'sche Gesetz ist nur nützlich, wenn man die passende Gauß-Fläche wählt — sonst bleibt $\oint\vec E\cdot d\vec A$ unlösbar kompliziert.
- **Pseudocode:**
```
EINGABE: Ladungsverteilung mit Symmetrie
1. Erkenne Symmetrietyp:
   Kugelsymmetrisch  → Gauß-Fläche = konzentrische Kugel
   Zylindersymmetrisch → Gauß-Fläche = koaxialer Zylinder
   Ebene Symmetrie   → Gauß-Fläche = "Gauß-Dose" (Quader/Zylinder
                         mit Deckflächen parallel zur geladenen Ebene)
2. Prüfe: Ist |E| auf der gewählten Fläche konstant und E parallel
   (oder senkrecht) zu dA? WENN NEIN: falsche Fläche gewählt, erneut prüfen
3. Berechne Q_innen als Funktion des Flächenparameters (r, ...)
4. Löse E * A_Fläche = Q_innen/ε0 nach E auf
AUSGABE: E(r) im gesamten Raum (typischerweise stückweise, innen/außen)
```
- **Korrektheitsidee:** Direkte Anwendung von Satz 7.1; die Symmetrieprüfung in Schritt 2 stellt sicher, dass $\vec E$ aus dem Integral herausgezogen werden darf.
- **Typische Anwendungen:** Feld von Kugel, unendlichem Zylinder/Draht, unendlicher Ebene/Platte.
- **Typische Fehler:** Gauß'sches Gesetz wird auf *nicht*-symmetrische Verteilungen angewendet (dann ist es zwar weiterhin *wahr*, aber nicht *nützlich*, da $E$ nicht aus dem Integral gezogen werden kann); falsche Gauß-Fläche (z. B. Kugel bei zylindrischer Symmetrie).

<a id="beispiele-25"></a>
## Beispiele

**Beispiel 1 (leicht):** Eine Kugel mit $Q=5\,\text{nC}$, $R=2\,\text{cm}$. Berechne $E$ bei $r=1\,\text{cm}$ und $r=5\,\text{cm}$.
*Lösung:* $r<R$: $E=0$. $r>R$: $E=\dfrac{1}{4\pi\varepsilon_0}\dfrac{Q}{r^2}=9\cdot10^9\cdot\dfrac{5\cdot10^{-9}}{0{,}0025}\approx1{,}8\cdot10^4\,\text{V/m}$.

**Beispiel 2 (mittel):** Ein unendlich langer, gerader Draht mit Linienladungsdichte $\lambda$ — bestimme $E(r)$ mittels Gauß'schem Gesetz.
*Lösung:* Zylindrische Gauß-Fläche, Radius $r$, Länge $\ell$: $E\cdot2\pi r\ell = \lambda\ell/\varepsilon_0 \Rightarrow E(r)=\dfrac{\lambda}{2\pi\varepsilon_0r}$ (Feld fällt mit $1/r$, nicht $1/r^2$ — charakteristisch für Zylindersymmetrie!).

**Beispiel 3 (mittel):** Ein Plattenkondensator ($A=100\,\text{cm}^2$, $d=1\,\text{mm}$) wird auf $U=100\,\text{V}$ aufgeladen. Berechne $C$, $Q$, $W$.
*Lösung:* $C=\varepsilon_0A/d = 8{,}854\cdot10^{-12}\cdot0{,}01/10^{-3}\approx8{,}85\cdot10^{-11}\,\text{F}$. $Q=CU\approx8{,}85\cdot10^{-9}\,\text{C}$. $W=\tfrac12CU^2\approx4{,}4\cdot10^{-7}\,\text{J}$.

**Beispiel 4 (schwer):** Drei Kondensatoren $C_1=2\,\mu\text{F}$, $C_2=3\,\mu\text{F}$ (parallel), diese Kombination in Reihe mit $C_3=6\,\mu\text{F}$. Berechne $C_{ges}$.
*Lösung:* Parallel: $C_{12}=C_1+C_2=5\,\mu\text{F}$. Reihe mit $C_3$: $\dfrac1{C_{ges}}=\dfrac15+\dfrac16=\dfrac{11}{30}\Rightarrow C_{ges}=\dfrac{30}{11}\approx2{,}73\,\mu\text{F}$.

**Beispiel 5 (schwer):** Zeige mit dem Gauß'schen Gesetz, dass im Hohlraum eines geladenen Leiters (ohne Ladung im Hohlraum) $\vec E=0$ gilt, selbst wenn außen ein beliebig kompliziertes Feld herrscht.
*Lösung:* Wähle die Gauß-Fläche direkt innerhalb der Leiteroberfläche, den Hohlraum umschließend, aber vollständig im Leitermaterial verlaufend. Dort ist $\vec E=0$ (Eigenschaft von Leitern, Def. 7.2), also $\oint\vec E\cdot d\vec A=0 \Rightarrow Q_{innen}=0$. Da im Hohlraum keine Ladung sitzt, könnte höchstens auf der *inneren* Oberfläche des Leiters (die den Hohlraum begrenzt) eine Ladung induziert sein — aber ohne Ladung im Hohlraum selbst zeigt eine genauere Analyse (Eindeutigkeitssatz der Poisson-Gleichung, hier nicht im Detail bewiesen), dass diese induzierte Ladung ebenfalls null ist und somit $\vec E=0$ im gesamten Hohlraum gilt. Dies ist das Funktionsprinzip des **Faraday-Käfigs**.

<a id="gegenbeispiele-25"></a>
## Gegenbeispiele

- Gauß'sches Gesetz liefert bei **fehlender Symmetrie** zwar eine korrekte, aber praktisch nutzlose Gleichung — z. B. für zwei beliebig positionierte Punktladungen lässt sich $E$ nicht aus $\oint\vec E\cdot d\vec A=Q_{innen}/\varepsilon_0$ isolieren, da $\vec E$ nicht konstant auf einer einfachen Fläche ist. Hier bleibt nur Superposition (Kapitel 6).
- Im Inneren eines Leiters ist $\vec E=0$ **nur im elektrostatischen Gleichgewicht** — fließt Strom (Kapitel 9), ist $\vec E\neq0$ im Leiter erforderlich, um den Strom aufrechtzuerhalten.

<a id="typische-klausuraufgaben-26"></a>
## Typische Klausuraufgaben

- Feldberechnung mit Gauß'schem Gesetz für Kugel/Zylinder/Ebene — Erkennungsmerkmal: hochsymmetrische Ladungsverteilung. Strategie: siehe Algorithmus.
- Kondensator-Netzwerke (Reihen-/Parallelschaltung, gemischt) — Strategie: schrittweise von "innen nach außen" zusammenfassen.
- Energieberechnung beim Auf-/Entladen oder beim Verbinden zweier geladener Kondensatoren.
- Faraday-Käfig-/Influenz-Verständnisfragen.

<a id="typische-fehler-26"></a>
## Typische Fehler

1. Gauß'sches Gesetz wird auf unsymmetrische Probleme angewendet und dann trotzdem $E$ vor das Integral gezogen (unzulässig!).
2. Bei der Kugel wird vergessen, dass $E=0$ im Inneren einer *Hohlkugel* gilt, aber bei einer *massiven, gleichmäßig raumgeladenen* Kugel $E(r)\propto r$ im Inneren (unterschiedliche Ladungsverteilung → unterschiedliches $Q_{innen}(r)$!).
3. Reihen-/Parallelformeln für Kondensatoren mit denen für Widerstände (Kapitel 9) verwechselt (dort ist es genau umgekehrt!).
4. Energie wird mit $W=CU^2$ statt $W=\tfrac12CU^2$ berechnet (Faktor-2-Fehler durch Vergessen der Integration).

<a id="verbindungen-27"></a>
## Verbindungen

- Satz 7.2 ist die **1. Maxwell-Gleichung** — wird in Kapitel 15 zusammen mit den übrigen drei Maxwell-Gleichungen zur vollständigen Theorie des Elektromagnetismus zusammengeführt.
- Die Poisson-/Laplace-Gleichung ist eine der wichtigsten partiellen Differentialgleichungen der Physik überhaupt (elektrostatisches Potential, aber auch Gravitationspotential, stationäre Wärmeleitung).
- Kondensator-Reihen-/Parallelformeln sind das **Spiegelbild** der Widerstandsformeln aus Kapitel 9 — guter Vergleichspunkt.
- $\vec E$-Feld an Leiteroberflächen ist die Grundlage für Kapitel 8 (Grenzflächenbedingungen bei Dielektrika).

<a id="zusammenfassung-15"></a>
## Zusammenfassung

- Gauß'sches Gesetz (integral): $\oint\vec E\cdot d\vec A = Q_{innen}/\varepsilon_0$; (differentiell): $\operatorname{div}\vec E=\rho/\varepsilon_0$.
- Nützlich bei Kugel-, Zylinder-, Ebenensymmetrie — liefert $E(r)$ ohne direkte Integration.
- Leiter im elektrostatischen Gleichgewicht: $\vec E_{innen}=0$, Ladung nur auf der Oberfläche, Oberfläche ist Äquipotentialfläche.
- Kondensator: $C=Q/U$; Platten-, Kugelkondensator-Formeln; Reihen-/Parallelschaltung (Kehrwert- bzw. direkte Addition).
- Feldenergie: $W=\tfrac12CU^2$, Energiedichte $w_{el}=\tfrac12\varepsilon_0E^2$ — Energie steckt im Feld, nicht in den Ladungen.

---

<a id="kapitel-8-elektrostatik-iii-dielektrika-materie-im-elektrischen-feld"></a>
# Kapitel 8: Elektrostatik III — Dielektrika, Materie im elektrischen Feld

<a id="motivation-28"></a>
## Motivation

Bisher haben wir Felder im Vakuum betrachtet. Reale Kondensatoren enthalten aber fast immer ein Isoliermaterial (Dielektrikum) zwischen den Platten — nicht zufällig, sondern weil es die Kapazität *erhöht*. Um zu verstehen, warum, müssen wir untersuchen, was mikroskopisch passiert, wenn ein elektrisches Feld auf Materie trifft, die selbst keine frei beweglichen Ladungsträger hat (im Gegensatz zu Leitern, Kapitel 7).

<a id="intuition-28"></a>
## Intuition

In einem Isolator sind die Elektronen fest an ihre Atome gebunden — sie können nicht frei wandern wie in einem Leiter. Ein äußeres Feld kann sie aber ein kleines Stück verschieben: Der positive Kern und die negative Elektronenhülle "verrutschen" leicht gegeneinander, das Atom wird zu einem winzigen Dipol (induzierte Polarisation) — man kann sich das wie ein Gummiband vorstellen, das sich unter Zug leicht dehnt, aber nicht reißt oder wegfließt.

Diese vielen mikroskopischen Dipole richten sich (teilweise) entlang des äußeren Feldes aus und erzeugen selbst ein Gegenfeld, das dem äußeren Feld im Material entgegenwirkt und es dadurch abschwächt. Weniger Feld bei gleicher Ladung auf den Kondensatorplatten bedeutet weniger Spannung bei gleicher Ladung — und damit (da $C=Q/U$) eine **größere** Kapazität.

<a id="formale-definitionen-28"></a>
## Formale Definitionen

**Definition 8.1 (Polarisation).**
$$\vec P := \frac1V\sum_i \vec p_i,$$
die mittlere Dipolmomentdichte im Material, $[\vec P]=\text{C/m}^2$.

**Definition 8.2 (Dielektrizitätszahl).**
Experimentell: Bei konstanter Ladung sinkt die Spannung am Kondensator um den Faktor $\varepsilon$ beim Einbringen eines Dielektrikums:
$$C_{diel} = \varepsilon\, C_{Vakuum}, \qquad \varepsilon\geq1\ \text{(dimensionslos)}.$$

**Definition 8.3 (Dielektrische Suszeptibilität).**
$$\vec P = \varepsilon_0\chi\vec E_{diel}, \qquad \chi:=\varepsilon-1.$$

**Definition 8.4 (Dielektrisches Verschiebungsfeld).**
$$\vec D := \varepsilon_0\vec E_{diel}+\vec P = \varepsilon_0\varepsilon\,\vec E_{diel} = \varepsilon_0\vec E_{vak}.$$

<a id="eigenschaften-24"></a>
## Eigenschaften

| Größe | Quelle | Verschwindet im Vakuum? |
|---|---|---|
| $\vec E_{diel}$ | freie **und** gebundene (Polarisations-)Ladungen | nein, ist das "wahre" Feld im Material |
| $\vec P$ | gebundene Ladungen allein | ja ($\chi=0$ im Vakuum) |
| $\vec D$ | **nur** freie Ladungen | nein, aber $\vec D=\varepsilon_0\vec E$ im Vakuum |

| Materialtyp | $\chi$ | Beispiel |
|---|---|---|
| Vakuum | $0$ | — |
| unpolares Dielektrikum | $\chi>0$, klein | $N_2$, unpolare Gase |
| polares Dielektrikum | $\chi>0$, größer | Wasser ($\varepsilon\approx80$) |

<a id="sätze-24"></a>
## Sätze

<a id="satz-81-div-vec-d-freie-ladungsdichte-maxwell-gleichung-in-materie"></a>
### Satz 8.1 (Div $\vec D$ = freie Ladungsdichte — Maxwell-Gleichung in Materie)

**Aussage:** $$\operatorname{div}\vec D = \rho_{frei}.$$

**Voraussetzungen:** lineares, isotropes Dielektrikum.

**Beweis (Beweisstil: Bilanz freier vs. gebundener Ladung, aufbauend auf Satz 7.2).**

Das Gauß'sche Gesetz (Satz 7.2) gilt *immer* für das tatsächliche Feld, mit der *gesamten* Ladungsdichte (frei + Polarisation/gebunden):
$$\operatorname{div}\vec E_{diel} = \frac{1}{\varepsilon_0}(\rho_{frei}+\rho_{pol}).$$
Die gebundene (Polarisations-)Ladungsdichte hängt mit der Polarisation zusammen über $\rho_{pol}=-\operatorname{div}\vec P$ (ohne Beweis hier übernommen — folgt aus einer Bilanzbetrachtung analog zu Satz 1.1, angewendet auf die "verschobene" gebundene Ladung). Einsetzen:
$$\operatorname{div}\vec E_{diel} = \frac1{\varepsilon_0}\rho_{frei} - \frac1{\varepsilon_0}\operatorname{div}\vec P \;\Longrightarrow\; \operatorname{div}(\varepsilon_0\vec E_{diel}+\vec P) = \rho_{frei}.$$
Mit Definition 8.4 ($\vec D=\varepsilon_0\vec E_{diel}+\vec P$) folgt direkt $\operatorname{div}\vec D=\rho_{frei}$. $\blacksquare$

**Bedeutung:** $\vec D$ ist ein "Hilfsfeld", das nur auf die (kontrollierbaren) freien Ladungen reagiert — praktisch für Rechnungen, da man die komplizierte Polarisationsladungsverteilung nicht kennen muss.

<a id="satz-82-brechungsgesetz-für-das-e-feld-an-einer-dielektrischen-grenzfläche"></a>
### Satz 8.2 (Brechungsgesetz für das E-Feld an einer dielektrischen Grenzfläche)

**Aussage:** An einer ladungsfreien Grenzfläche zwischen zwei Dielektrika ($\varepsilon_1,\varepsilon_2$) gilt für die Winkel zur Flächennormalen:
$$\varepsilon_1\tan\alpha_2 = \varepsilon_2\tan\alpha_1 \quad\text{bzw. äquivalent}\quad \tan\alpha_1 = \varepsilon_1\tan\alpha_2/\varepsilon_2.$$

**Beweisidee (Beweisstil: getrennte Analyse von Tangential- und Normalkomponente).**
Zwei Teilaussagen werden kombiniert: (1) Die **Tangentialkomponente** von $\vec E$ ist an der Grenzfläche stetig ($E_{t,1}=E_{t,2}$) — folgt aus $\oint\vec E\cdot d\vec s=0$ (Konservativität, Satz 6.1) angewendet auf eine schmale Schleife, die die Grenzfläche kreuzt. (2) Die **Normalkomponente** von $\vec D$ ist stetig ($D_{n,1}=D_{n,2}$), falls keine freie Flächenladung vorhanden ist — folgt aus Satz 8.1 (Gauß'sches Gesetz für $\vec D$), angewendet auf eine flache "Gauß-Dose" über die Grenzfläche. Aus $D_n=\varepsilon_0\varepsilon E_n$ und Division der beiden Stetigkeitsbedingungen ($E_t/E_n=\tan\alpha$) folgt die Behauptung. $\blacksquare$

<a id="satz-83-kapazität-und-feldenergie-mit-dielektrikum"></a>
### Satz 8.3 (Kapazität und Feldenergie mit Dielektrikum)

**Aussage:** $$C_{diel}=\varepsilon C_{vak}, \qquad w_{el}=\tfrac12\varepsilon_0\varepsilon E^2 = \tfrac12 \vec E\cdot\vec D.$$

**Beweisidee:** Direkte Konsequenz aus $\vec D=\varepsilon_0\varepsilon\vec E$ eingesetzt in die Kondensator- und Energieformeln aus Kapitel 7 (Sätze 7.4, 7.5), unter Beachtung, dass bei *konstanter Ladung* $Q$ das Feld $E$ um den Faktor $\varepsilon$ sinkt.

<a id="algorithmen-16"></a>
## Algorithmen

**Lösungsstrategie: Kondensator mit Dielektrikum**
```
EINGABE: Kondensatorgeometrie, Dielektrikum(a) mit ε_r
1. Bestimme, ob Q oder U konstant gehalten wird (z. B. Batterie
   angeschlossen = U konstant; isoliert = Q konstant)
2. Berechne C_vak für die gegebene Geometrie (Kapitel 7)
3. C_diel = ε * C_vak  (bei vollständig gefülltem Kondensator)
   Bei teilweiser Füllung: Reihen-/Parallelschaltung von Teilkondensatoren
   mit und ohne Dielektrikum modellieren!
4. WENN Q konstant: neues U = Q/C_diel (sinkt), E sinkt um Faktor ε
   WENN U konstant: neues Q = C_diel * U (steigt)
5. Energie über W = Q²/(2C) bzw. W = ½CU² je nachdem, was konstant ist
AUSGABE: C, Q, U, E, W im Endzustand
```
- **Typischer Fehler:** Bei teilweiser Füllung (z. B. Dielektrikum füllt nur die halbe Plattenfläche oder nur die halbe Plattendistanz) wird fälschlich einfach $C=\varepsilon C_{vak}$ für den *gesamten* Kondensator verwendet, statt die Geometrie korrekt als Parallel- oder Reihenschaltung zweier Teilkondensatoren zu modellieren.

<a id="beispiele-26"></a>
## Beispiele

**Beispiel 1 (leicht):** Ein Plattenkondensator mit $C_{vak}=10\,\text{pF}$ wird mit Glas ($\varepsilon=6$) gefüllt. Neue Kapazität?
*Lösung:* $C_{diel}=6\cdot10=60\,\text{pF}$.

**Beispiel 2 (mittel):** Derselbe Kondensator wird zuerst mit $U_0=100\,\text{V}$ (Batterie) aufgeladen, dann von der Batterie getrennt, dann wird das Dielektrikum eingeführt. Wie ändert sich $U$?
*Lösung:* $Q$ bleibt konstant (isoliert!). $U_{neu}=Q/C_{diel}=Q/(6C_{vak}) = U_0/6\approx16{,}7\,\text{V}$.

**Beispiel 3 (mittel):** Ein Kondensator ist zur Hälfte (Fläche) mit einem Dielektrikum ($\varepsilon=4$) gefüllt, zur Hälfte Vakuum, gleiche Plattenspannung $U$. Wie verhalten sich die beiden Hälften zueinander?
*Lösung:* Beide Hälften liegen an derselben Spannung $U$ (Platten sind durchgehend leitend) → **Parallelschaltung** zweier Kondensatoren mit halber Fläche: $C_{ges}=\tfrac12C_{vak}+\tfrac12\cdot4C_{vak} = 2{,}5\,C_{vak}$.

**Beispiel 4 (schwer):** Ein Lichtstrahl (Analogie zur Feldlinienbrechung) trifft mit $\alpha_1=30°$ von einem Medium mit $\varepsilon_1=1$ auf ein Medium mit $\varepsilon_2=4$. Berechne $\alpha_2$ für die E-Feldlinie (Satz 8.2).
*Lösung:* $\tan\alpha_2 = \dfrac{\varepsilon_2}{\varepsilon_1}\tan\alpha_1 = 4\cdot\tan30° \approx 2{,}31 \Rightarrow \alpha_2\approx66{,}6°$ — die Feldlinie wird beim Übergang in das Medium mit höherem $\varepsilon$ stärker von der Normalen weggebrochen.

<a id="gegenbeispiele-26"></a>
## Gegenbeispiele

- $C_{diel}=\varepsilon C_{vak}$ gilt **nur**, wenn das Dielektrikum den *gesamten* felderfüllten Raum ausfüllt — bei teilweiser Füllung muss immer über Ersatzschaltbilder (Reihen-/Parallelschaltung von Teilkondensatoren) gerechnet werden.
- Anisotrope Kristalle haben **keine** skalare Dielektrizitätszahl $\varepsilon$ — dort ist $\vec D=\varepsilon_0\hat\varepsilon\vec E$ mit einem Tensor $\hat\varepsilon$ (hier nicht behandelt, aber wichtige Einschränkung der Gültigkeit von Def. 8.2/8.4).

<a id="typische-klausuraufgaben-27"></a>
## Typische Klausuraufgaben

- "Wie ändert sich $C$/$U$/$Q$/$W$, wenn ein Dielektrikum eingeführt wird?" — Strategie: zuerst klären, ob $Q$ oder $U$ konstant bleibt (Batterie angeschlossen oder nicht).
- Teilweise gefüllte Kondensatoren — Strategie: Ersatzschaltbild aus Teilkondensatoren (parallel bei gemeinsamer Spannung/unterschiedlicher Fläche, Reihe bei gemeinsamer Ladung/unterschiedlichem Plattenabstand).
- Grenzflächenbedingungen (Satz 8.2) — eher Verständnisaufgabe.

<a id="typische-fehler-27"></a>
## Typische Fehler

1. Verwechslung, ob $Q$ oder $U$ beim Einbringen des Dielektrikums konstant bleibt (führt zu entgegengesetzten Antworten für $E$ und $U$!).
2. Teilweise gefüllte Kondensatoren werden als vollständig gefüllt behandelt.
3. $\vec D$ und $\vec E$ werden verwechselt — $\vec D$ hängt nur von freien Ladungen ab, $\vec E$ vom Gesamtfeld.

<a id="verbindungen-28"></a>
## Verbindungen

- Direkte Erweiterung von Kapitel 7 (Kondensatoren) auf reale Materialien.
- $\vec D=\rho_{frei}$-Formulierung ist eine der vier Maxwell-Gleichungen "in Materie" — wird in Kapitel 15 im Vakuum-Grenzfall wieder auf die einfache Form aus Kapitel 7 reduziert.
- Konzeptuelle Parallele zu **magnetisierbaren Materialien** (Kapitel 12): dort spielt $\vec H$ die analoge Rolle zu $\vec D$, $\vec M$ (Magnetisierung) die analoge Rolle zu $\vec P$.

<a id="zusammenfassung-16"></a>
## Zusammenfassung

- Dielektrika werden durch ein äußeres Feld polarisiert ($\vec P=\varepsilon_0\chi\vec E$), was das Feld im Material abschwächt.
- $\vec D:=\varepsilon_0\vec E+\vec P=\varepsilon_0\varepsilon\vec E$ hängt nur von freien Ladungen ab: $\operatorname{div}\vec D=\rho_{frei}$.
- Kondensator mit vollständig füllendem Dielektrikum: $C_{diel}=\varepsilon C_{vak}$.
- Grenzflächen: $E_t$ stetig, $D_n$ stetig (ohne freie Flächenladung) → Brechungsgesetz für Feldlinien.

---

<a id="kapitel-9-elektrischer-strom-und-gleichstromkreise"></a>
# Kapitel 9: Elektrischer Strom und Gleichstromkreise

<a id="motivation-29"></a>
## Motivation

Elektrostatik behandelt ruhende Ladungen. Doch die meisten praktischen Anwendungen (Beleuchtung, Elektronik, Motoren) beruhen auf *bewegten* Ladungen — elektrischem Strom. Die zentrale Frage: Wie hängt der Strom, der durch ein Material fließt, mit der angelegten Spannung zusammen? Die Antwort (Ohm'sches Gesetz) ist empirisch, aber lässt sich mikroskopisch aus der Bewegung der Ladungsträger im Material verstehen — ein weiteres Beispiel für den Brückenschlag zwischen mikroskopischer Mechanik und makroskopischem Verhalten, wie schon in Kapitel 2.

<a id="intuition-29"></a>
## Intuition

Stell dir Elektronen in einem Metall wie Menschen in einer dichten, aber fließenden Menschenmenge vor. Ein elektrisches Feld ist wie eine leichte Neigung des Bodens: Die Menge bewegt sich im Mittel bergab, aber jede einzelne Person stößt ständig mit anderen zusammen (Streuung an Gitteratomen) und wird abgebremst — daher stellt sich eine **konstante mittlere Driftgeschwindigkeit** ein (nicht eine ständig wachsende), genau wie ein Fallschirmspringer eine Grenzgeschwindigkeit erreicht, wenn Luftwiderstand die Gewichtskraft ausgleicht. Das Ohm'sche Gesetz ist die makroskopische Konsequenz dieses mikroskopischen Gleichgewichts.

<a id="formale-definitionen-29"></a>
## Formale Definitionen

**Definition 9.1 (Stromstärke).**
$$I := \frac{dQ}{dt}, \qquad [I]=\text{A (Ampere)}.$$

**Definition 9.2 (Stromdichte).**
$$\vec j(\vec r) := n\,q\,\vec v_{Drift}, \qquad I = \int_A \vec j\cdot d\vec A,$$
mit Ladungsträgerdichte $n$, Ladung $q$ pro Träger, mittlerer Driftgeschwindigkeit $\vec v_{Drift}$.

**Definition 9.3 (Elektrischer Widerstand, spezifischer Widerstand).**
$$R := \frac{U}{I}, \qquad [R]=\Omega\text{ (Ohm)}; \qquad R = \varrho\,\frac{\ell}{A},$$
mit spezifischem Widerstand $\varrho$ (Materialkonstante), Leitfähigkeit $\sigma:=1/\varrho$.

**Definition 9.4 (Elektrische Leistung).**
$$P := \frac{dW}{dt} = U\cdot I.$$

<a id="eigenschaften-25"></a>
## Eigenschaften

| Größe | Formel | Bemerkung |
|---|---|---|
| Mikroskopisches Ohm'sches Gesetz | $\vec j=\sigma\vec E$ | lineare Antwort, gilt für "Ohm'sche" Leiter |
| Kontinuitätsgleichung für Ladung | $\operatorname{div}\vec j=-\dot\rho$ | identisch zu Satz 1.1, angewendet auf Ladung |
| Stationärer Strom | $\operatorname{div}\vec j=0$ | keine Ladungsanhäufung irgendwo |
| Temperaturabhängigkeit (Metalle) | $\varrho(T)=\varrho_0(1+\alpha T+\beta T^2)$, $\alpha\gg\beta T$ | mehr Gitterschwingungen bei höherem $T$ → mehr Streuung |
| Temperaturabhängigkeit (Halbleiter) | $n(T)\propto e^{-E_g/(k_BT)}$ | mehr Ladungsträger bei höherem $T$ (dominiert über erhöhte Streuung) |
| Supraleiter | $R=0$ für $T<T_c$ | Quantenphänomen, hier nicht hergeleitet |

<a id="sätze-25"></a>
## Sätze

<a id="satz-91-kontinuitätsgleichung-für-elektrische-ladung"></a>
### Satz 9.1 (Kontinuitätsgleichung für elektrische Ladung)

**Aussage:** $$\operatorname{div}\vec j = -\frac{\partial\rho}{\partial t}.$$

**Beweis:** Identisch zum Beweis von Satz 1.1, mit Massenstromdichte $\to$ elektrische Stromdichte, Massendichte $\to$ Ladungsdichte ersetzt (dieselbe Bilanzargumentation über ein beliebiges Kontrollvolumen + Satz von Gauß). $\blacksquare$

<a id="satz-92-mikroskopische-herleitung-des-ohmschen-gesetzes"></a>
### Satz 9.2 (Mikroskopische Herleitung des Ohm'schen Gesetzes)

**Aussage:** $$\vec j = \sigma\vec E, \qquad U = R\,I.$$

**Voraussetzungen:** Driftgeschwindigkeit klein gegen thermische Geschwindigkeit, lineares Reibungsmodell (Stoßzeit-Näherung), homogener, isotroper Leiter.

**Beweis (Beweisstil: Kräftebilanz, analog zur Sedimentationsgeschwindigkeit in Kapitel 1).**

Ein Ladungsträger der Masse $m$, Ladung $q$, erfährt im Feld $\vec E$ die Kraft $\vec F=q\vec E$. Gleichzeitig wird er durch Stöße mit dem Gitter gebremst; wir modellieren dies durch eine effektive Reibungskraft $\vec F_{Reib}=-\vec v/\mu$ mit einer Materialkonstante $\mu$ (Beweglichkeit). Im stationären Zustand (Kräftegleichgewicht, analog zur Stokes-Sedimentation, Kapitel 1):
$$q\vec E = \frac{\vec v_{Drift}}{\mu} \;\Longrightarrow\; \vec v_{Drift}=\mu\vec E.$$
Einsetzen in Definition 9.2:
$$\vec j = nq\vec v_{Drift} = nq\mu\vec E =: \sigma\vec E, \qquad \sigma:=nq\mu.$$
Für einen homogenen Leiter der Länge $\ell$, Querschnitt $A$, mit $I=jA$ und $U=E\ell$ (homogenes Feld):
$$I = \sigma E A = \sigma\frac{U}{\ell}A \;\Longrightarrow\; U = \frac{\ell}{\sigma A}\,I =: R\,I,\quad R=\frac{\ell}{\sigma A}=\varrho\frac{\ell}{A}. \qquad\blacksquare$$

<a id="satz-93-kirchhoffsche-regeln"></a>
### Satz 9.3 (Kirchhoff'sche Regeln)

**Aussage:**
- **Knotenregel (1. Kirchhoff'sche Regel):** $\sum_k I_k = 0$ (Vorzeichen: zufließend positiv, abfließend negativ) an jedem Knotenpunkt.
- **Maschenregel (2. Kirchhoff'sche Regel):** $\sum_n U_n = 0$ entlang jeder geschlossenen Masche.

**Voraussetzungen:** stationärer (oder quasistationärer) Strom.

**Beweis Knotenregel (Beweisstil: direkte Konsequenz von Satz 9.1).**
Für stationären Strom gilt $\operatorname{div}\vec j=0$ (Satz 9.1 mit $\dot\rho=0$). Integration über ein kleines Volumen um einen Knotenpunkt und Anwendung des Satzes von Gauß:
$$0 = \int_V\operatorname{div}\vec j\, dV = \oint_S\vec j\cdot d\vec A = \sum_k I_k. \qquad\blacksquare$$

**Beweis Maschenregel (Beweisstil: direkte Konsequenz der Konservativität des elektrostatischen Feldes, Satz 6.1).**
Für ein (quasi-)elektrostatisches Feld gilt $\oint\vec E\cdot d\vec s=0$ (Satz 6.1, da $\vec E=-\nabla\phi$). Entlang einer Masche ist dieses Integral gerade die Summe aller Spannungsabfälle und -quellen: $\oint\vec E\cdot d\vec s = \sum_n U_n = 0$. $\blacksquare$

**Bedeutung:** Diese beiden Regeln erlauben die vollständige Analyse *beliebiger* linearer Netzwerke (nicht nur reine Reihen-/Parallelschaltungen).

<a id="satz-94-ersatzwiderstände-reihen-und-parallelschaltung"></a>
### Satz 9.4 (Ersatzwiderstände: Reihen- und Parallelschaltung)

**Aussage:** $$R_{Reihe}=\sum_i R_i, \qquad \frac1{R_{Parallel}}=\sum_i\frac1{R_i}.$$

**Beweis Reihenschaltung (Beweisstil: Kombination Knoten-/Maschenregel).**
Bei Reihenschaltung fließt durch alle Widerstände derselbe Strom $I$ (Knotenregel, da keine Verzweigung). Maschenregel: $U_{ges}=\sum_iU_i=\sum_iR_iI = I\sum_iR_i =: I\,R_{Reihe}$. $\blacksquare$

**Beweis Parallelschaltung (analog, Beweisstil: Kombination Knoten-/Maschenregel).**
Bei Parallelschaltung liegt an allen Widerständen dieselbe Spannung $U$ an. Knotenregel: $I_{ges}=\sum_iI_i=\sum_iU/R_i = U\sum_i1/R_i =: U/R_{Parallel}$. $\blacksquare$

**Bemerkung:** Beachte die **Umkehrung** gegenüber Kondensatoren (Kapitel 7, Satz 7.4/Eigenschaftentabelle) — dort war es genau andersherum (Kehrwertaddition bei Reihe für Kondensatoren, direkte Addition bei Reihe für Widerstände). Vergleichstabelle:

| | Widerstände | Kondensatoren |
|---|---|---|
| Reihenschaltung | $R_{ges}=\sum R_i$ | $1/C_{ges}=\sum1/C_i$ |
| Parallelschaltung | $1/R_{ges}=\sum1/R_i$ | $C_{ges}=\sum C_i$ |
| Grund des Unterschieds | bei Widerständen ist $I$ (nicht $U$) bei Reihe gleich; bei Kondensatoren ist $Q$ (nicht $U$) bei Reihe gleich | — |

<a id="algorithmen-17"></a>
## Algorithmen

**Netzwerkanalyse-Algorithmus (Kirchhoff'sche Regeln)**

- **Motivation:** Bei komplexen Schaltungen (nicht reine Reihen-/Parallelschaltung) versagt die einfache Ersatzwiderstandsmethode; man braucht ein systematisches Gleichungssystem.
- **Idee:** Jeder unabhängige Knoten liefert eine Knotengleichung, jede unabhängige Masche eine Maschengleichung — zusammen genug Gleichungen, um alle unbekannten Ströme zu bestimmen.
- **Voraussetzungen:** lineares Netzwerk (Ohm'sche Widerstände, ideale Spannungsquellen).
- **Pseudocode:**
```
EINGABE: Schaltung mit b Zweigen, k Knoten, definierten Stromrichtungen
1. Wähle (k-1) unabhängige Knoten, stelle Knotengleichungen auf (Satz 9.3)
2. Bestimme unabhängige Maschen (b - k + 1 Stück), stelle
   Maschengleichungen auf (Satz 9.3), Vorzeichen konsistent mit
   gewähltem Umlaufsinn
3. Löse das entstehende lineare Gleichungssystem (b Gleichungen,
   b Unbekannte Ströme) z. B. mit Gauß-Elimination
4. Prüfe Ergebnis: negative Ströme bedeuten nur, dass die tatsächliche
   Richtung der angenommenen entgegengesetzt ist (kein Fehler!)
AUSGABE: alle Zweigströme I_i
```
- **Mathematische Beschreibung:** lineares Gleichungssystem $A\vec I = \vec b$ mit Inzidenzmatrix $A$ (Knotengleichungen) und Maschenimpedanzen.
- **Laufzeit:** Gauß-Elimination auf $b\times b$-System: $O(b^3)$.
- **Speicherbedarf:** $O(b^2)$ für die Koeffizientenmatrix.
- **Korrektheitsidee:** Folgt direkt aus Satz 9.3; die Anzahl der unabhängigen Gleichungen ($k-1$ Knoten + $b-k+1$ Maschen $=b$) entspricht genau der Anzahl der Unbekannten.
- **Typische Anwendungen:** Brückenschaltungen, Netzwerke mit mehreren Spannungsquellen, Spannungsteiler unter Last.
- **Typische Fehler:** Vorzeichenkonvention beim Maschenumlauf inkonsistent gewählt; eine abhängige (redundante) Masche/Knoten wird mitgezählt, was zu einem singulären Gleichungssystem führt.

<a id="beispiele-27"></a>
## Beispiele

**Beispiel 1 (leicht):** Ein Draht ($\ell=2\,\text{m}$, $A=1\,\text{mm}^2$, $\varrho=1{,}7\cdot10^{-8}\,\Omega\text{m}$, Kupfer). Berechne $R$.
*Lösung:* $R=\varrho\ell/A = 1{,}7\cdot10^{-8}\cdot2/10^{-6}=0{,}034\,\Omega$.

**Beispiel 2 (leicht):** Ein Widerstand $R=100\,\Omega$ liegt an $U=10\,\text{V}$. Berechne $I$ und $P$.
*Lösung:* $I=U/R=0{,}1\,\text{A}$. $P=UI=1\,\text{W}$.

**Beispiel 3 (mittel):** Drei Widerstände $R_1=10\,\Omega$, $R_2=20\,\Omega$ (parallel), in Reihe mit $R_3=5\,\Omega$. Berechne $R_{ges}$.
*Lösung:* $R_{12}=(1/10+1/20)^{-1}=6{,}67\,\Omega$. $R_{ges}=6{,}67+5=11{,}67\,\Omega$.

**Beispiel 4 (mittel):** Unbelasteter Spannungsteiler mit $R_1=R_2=1\,\text{k}\Omega$ an $U_0=10\,\text{V}$. Berechne $U_2$. Nun wird ein Lastwiderstand $R_L=1\,\text{k}\Omega$ parallel zu $R_2$ geschaltet — wie ändert sich $U_2$?
*Lösung:* Unbelastet: $U_2=U_0R_2/(R_1+R_2)=5\,\text{V}$. Belastet: $R_2\|R_L=500\,\Omega$, $U_2'=U_0\cdot500/(1000+500)\approx3{,}33\,\text{V}$ — die Spannung bricht unter Last ein (wichtiger Effekt bei realen Spannungsteilern!).

**Beispiel 5 (schwer):** Eine Brückenschaltung (Wheatstone-Brücke) mit vier Widerständen $R_1,R_2,R_3,R_4$ und einem Galvanometer in der Brückendiagonale. Zeige, dass im "abgeglichenen" Zustand (kein Strom durchs Galvanometer) $R_1/R_2=R_3/R_4$ gilt.
*Lösung:* Im abgeglichenen Zustand fließt kein Strom durch die Diagonale, also verhalten sich die beiden Zweige wie zwei unabhängige Spannungsteiler an derselben Gesamtspannung. Gleichsetzen der Teilspannungen an den beiden Mittelknoten (die dann gleiches Potential haben müssen, da kein Strom durch die Verbindung fließt) liefert nach Umformen $R_1/R_2=R_3/R_4$ — Grundprinzip der präzisen Widerstandsmessung.

<a id="gegenbeispiele-27"></a>
## Gegenbeispiele

- Nicht alle Materialien sind "Ohm'sch" — z. B. Dioden, Glühlampen (Widerstand ändert sich stark mit $I$ bzw. $T$) haben eine nichtlineare Kennlinie $I(U)$; das Ohm'sche Gesetz $U=RI$ gilt dort nur lokal (differentiell) mit $R(I)$, nicht global mit konstantem $R$.
- Reale Spannungsquellen haben einen **Innenwiderstand** — die Klemmenspannung sinkt unter Last; ideale Spannungsquellen (konstantes $U$ unabhängig von $I$) sind eine Idealisierung.

<a id="typische-klausuraufgaben-28"></a>
## Typische Klausuraufgaben

- Ersatzwiderstandsberechnung für Reihen-/Parallel-/gemischte Schaltungen — Strategie: schrittweise "von außen nach innen" oder "innen nach außen" zusammenfassen.
- Kirchhoff'sche Regeln bei Mehrfachmaschen (Brückenschaltung, Netzwerke mit mehreren Quellen) — Strategie: siehe Algorithmus.
- Belasteter vs. unbelasteter Spannungsteiler — Erkennungsmerkmal: "Lastwiderstand", "Verbraucher angeschlossen".
- Leistungsberechnung, Joule'sche Wärme in Schaltungen.

<a id="typische-fehler-28"></a>
## Typische Fehler

1. Reihen-/Parallelformeln für Widerstände und Kondensatoren verwechselt (siehe Vergleichstabelle oben!).
2. Beim Spannungsteiler wird die Belastung durch $R_L$ vergessen — führt zu systematisch zu hohen $U_2$-Werten.
3. Vorzeichenfehler bei Kirchhoff'scher Maschenregel (Umlaufsinn nicht konsistent mit Strom-/Quellenrichtung).
4. Ohm'sches Gesetz wird auf nichtlineare Bauelemente (Diode, Glühlampe) mit konstantem $R$ angewendet.

<a id="verbindungen-29"></a>
## Verbindungen

- Die Kontinuitätsgleichung (Satz 9.1) und die Kirchhoff'sche Knotenregel sind direkte Anwendungen desselben Prinzips wie in Kapitel 1 (Massenerhaltung) — ein wiederkehrendes Muster der gesamten Physik.
- $\vec j=\sigma\vec E$ hat exakt dieselbe mathematische Struktur wie die Transportgesetze aus Kapitel 3 (Fick, Fourier) — "Fluss $\propto$ Gradient".
- Widerstand und Temperaturabhängigkeit werden in Kapitel 10 (Ladungstransport in Materialien) mikroskopisch vertieft.
- RC-Aufladevorgänge (hier kurz als Anwendung erwähnt) werden strukturell in Kapitel 14 (Wechselstrom, komplexe Widerstände) wieder aufgegriffen.

<a id="zusammenfassung-17"></a>
## Zusammenfassung

- $I=dQ/dt$; $\vec j=nq\vec v_{Drift}$.
- Ohm'sches Gesetz (mikroskopisch: $\vec j=\sigma\vec E$; makroskopisch: $U=RI$), $R=\varrho\ell/A$.
- Kirchhoff'sche Regeln: Knotenregel ($\sum I=0$) aus Ladungserhaltung, Maschenregel ($\sum U=0$) aus Konservativität von $\vec E$.
- Widerstände: Reihe addiert sich direkt, Parallel als Kehrwertsumme (umgekehrt wie bei Kondensatoren!).
- $P=UI=RI^2=U^2/R$ (Joule'sche Wärme).

---

<a id="kapitel-10-ladungstransport-in-materialien"></a>
# Kapitel 10: Ladungstransport in Materialien

<a id="motivation-30"></a>
## Motivation

Warum leiten Metalle Strom gut, Isolatoren fast gar nicht, und Halbleiter irgendwo dazwischen — und warum ändert sich das bei Halbleitern so stark mit der Temperatur (im Gegensatz zu Metallen)? Die Antwort erfordert einen Blick auf die *quantenmechanische* Struktur der Materie (Bändermodell) — ein erster Ausblick über die klassische Physik dieser Vorlesung hinaus, der aber für das Verständnis moderner Elektronik (Transistoren, Solarzellen) unverzichtbar ist.

<a id="intuition-30"></a>
## Intuition

Stell dir die erlaubten Energieniveaus der Elektronen in einem Festkörper nicht als einzelne Linien (wie im isolierten Atom), sondern als breite "Bänder" erlaubter Energien vor, getrennt durch "verbotene" Energielücken (Bandlücken) — wie Stockwerke eines Gebäudes mit einigen "gesperrten" Zwischengeschossen. Elektronen können nur dann zum elektrischen Strom beitragen, wenn sie sich in einem *teilweise* gefüllten Band frei bewegen können (so wie Menschen sich nur dann durch ein Stockwerk bewegen können, wenn nicht *jeder* Platz bereits besetzt ist — bei einem voll besetzten Band kann niemand "einen Platz weiterrücken", ohne dass ein anderer bereits dort ist, es sei denn es gibt einen Sprung ins nächste, unbesetzte Band).

Bei **Metallen** überlappt das oberste besetzte Band mit dem nächsten (oder ist nur teilweise gefüllt) — Elektronen bewegen sich fast frei. Bei **Isolatoren** ist eine riesige Bandlücke zum nächsten Band vorhanden — bei Raumtemperatur schafft es praktisch kein Elektron, sie zu überspringen. Bei **Halbleitern** ist die Lücke klein genug, dass thermische Anregung ($k_BT$) einige wenige Elektronen "hinüberspringen" lässt — und mit steigender Temperatur werden es exponentiell mehr.

<a id="formale-definitionen-30"></a>
## Formale Definitionen

**Definition 10.1 (Bändermodell — qualitativ).**
Elektronen in einem Festkörper besetzen erlaubte Energiebänder, getrennt durch Bandlücken $E_g$. Das höchste bei $T=0$ vollständig besetzte Band heißt **Valenzband**, das nächsthöhere (bei $T=0$ leere) **Leitungsband**.

**Definition 10.2 (Klassifikation nach Bandstruktur).**

| Typ | Bandstruktur | Bandlücke $E_g$ |
|---|---|---|
| Metall (Leiter) | Leitungsband teilweise gefüllt oder Bänder überlappen | $E_g=0$ (kein Gap) |
| Halbleiter | Valenzband voll, Leitungsband leer bei $T=0$, aber $E_g$ klein | $E_g\sim1{-}2\,\text{eV}$ (z. B. Si: $1{,}1\,\text{eV}$) |
| Isolator | wie Halbleiter, aber $E_g$ groß | $E_g\gg k_BT$ (mehrere eV) |

**Definition 10.3 (Ladungsträgerdichte im Halbleiter, intrinsisch).**
$$n(T) \propto e^{-E_g/(2k_BT)}$$
(exponentielles "Ausfrieren" bei tiefer $T$; Herleitung erfordert Fermi-Dirac-Statistik, hier nicht im Detail behandelt).

<a id="eigenschaften-26"></a>
## Eigenschaften

| Eigenschaft | Metall | Halbleiter |
|---|---|---|
| $\varrho(T)$-Verhalten | steigt mit $T$ (mehr Streuung) | **sinkt** mit $T$ (exponentiell mehr Ladungsträger) |
| Ladungsträger bei $T=0$ | vorhanden (Fermi-See) | keine (im intrinsischen Fall) |
| Dotierung möglich | nein (sinnlos) | ja — gezielte Erhöhung der Ladungsträgerdichte |

**Wichtige Vergleichstabelle — Temperaturabhängigkeit des Widerstands (Zusammenfassung aus Kapitel 9 + hier vertieft):**

| Material | Formel | Grund |
|---|---|---|
| Metall | $\varrho(T)=\varrho_0(1+\alpha T)$, $\alpha>0$ | mehr Gitterschwingungen → mehr Streuung, Ladungsträgerdichte $n$ konstant |
| Halbleiter | $\varrho(T)\propto e^{+E_g/(2k_BT)}$ (sinkt mit steigendem $T$) | $n(T)$ steigt exponentiell, dominiert über (schwächer wachsende) Streuung |
| Supraleiter | $\varrho=0$ für $T<T_c$ | Cooper-Paare, quantenmechanischer Effekt |

<a id="sätze-26"></a>
## Sätze

Dieses Kapitel enthält (im Rahmen dieser Vorlesung) keine vollständig herleitbaren Sätze im strengen Sinn, da die zugrundeliegende Bandtheorie Quantenmechanik voraussetzt, die hier nicht Gegenstand ist. Die zentralen Aussagen werden daher als **empirisch begründete Modellvorstellungen** behandelt:

<a id="satz-101-wiedemann-franz-gesetz-wiederholungvertiefung-aus-kapitel-3"></a>
### "Satz" 10.1 (Wiedemann-Franz-Gesetz, Wiederholung/Vertiefung aus Kapitel 3)

**Aussage:** $\lambda/\sigma = aT$ (Definition 3.4).

**Begründung (qualitativ, kein vollständiger Beweis):** In Metallen werden sowohl Wärme als auch elektrischer Strom von *denselben* freien Leitungselektronen getragen. Da beide Transportprozesse auf demselben mikroskopischen Mechanismus (Elektronenbewegung + Streuung an Gitterdefekten) beruhen, sind $\lambda$ und $\sigma$ nicht unabhängig, sondern über die universelle Lorenz-Zahl verknüpft.

<a id="algorithmen-18"></a>
## Algorithmen

Kein klassischer Algorithmus; stattdessen eine **Entscheidungsstrategie zur Materialklassifikation**:
```
EINGABE: Widerstand R(T)-Messkurve oder Bandlücke E_g
1. WENN dR/dT > 0 (Widerstand steigt mit T): → Metall
2. WENN dR/dT < 0 (Widerstand sinkt mit T):  → Halbleiter (oder Isolator,
   falls Leitfähigkeit bei Raumtemperatur verschwindend gering)
3. WENN R = 0 unterhalb einer kritischen Temperatur T_c: → Supraleiter
AUSGABE: Materialklasse
```

<a id="beispiele-28"></a>
## Beispiele

**Beispiel 1 (leicht):** Silizium hat $E_g=1{,}1\,\text{eV}$. Bei welcher Temperaturskala wird $k_BT\sim E_g$?
*Lösung:* $T\sim E_g/k_B = 1{,}1\cdot1{,}6\cdot10^{-19}/1{,}38\cdot10^{-23}\approx12750\,\text{K}$ — bei Raumtemperatur ($300\,\text{K}$) ist $k_BT\approx0{,}026\,\text{eV}\ll E_g$, daher sind bei Raumtemperatur nur sehr wenige Elektronen thermisch angeregt (exponentiell unterdrückt), was erklärt, warum reines (intrinsisches) Silizium bei Raumtemperatur ein sehr viel schlechterer Leiter ist als ein Metall.

**Beispiel 2 (mittel):** Ein Kupferdraht hat bei $20\,°\text{C}$ den Widerstand $R_0=10\,\Omega$, $\alpha=0{,}004\,\text{K}^{-1}$. Berechne $R$ bei $80\,°\text{C}$.
*Lösung:* $R=R_0(1+\alpha\Delta T)=10(1+0{,}004\cdot60)=12{,}4\,\Omega$.

<a id="gegenbeispiele-28"></a>
## Gegenbeispiele

- Das lineare Modell $\varrho(T)=\varrho_0(1+\alpha T)$ für Metalle gilt **nicht** bei sehr tiefen Temperaturen (dort dominieren andere Streumechanismen, z. B. an Verunreinigungen, das Verhalten wird komplizierter) und **nicht** in der Nähe des Schmelzpunkts.
- Bei Supraleitern versagt jedes klassische Widerstandsmodell komplett — $R=0$ ist ein rein quantenmechanischer Effekt (Cooper-Paare), nicht durch klassische Streutheorie erklärbar.

<a id="typische-klausuraufgaben-29"></a>
## Typische Klausuraufgaben

- Temperaturabhängige Widerstandsberechnung für Metalle (linear) — meist einfache Einsetzaufgabe.
- Qualitative Erklärung, warum Halbleiterwiderstand mit $T$ sinkt, Metallwiderstand steigt — Verständnisfrage, Bändermodell-Argumentation gefragt.
- Einordnung eines Materials anhand einer gegebenen $R(T)$-Kurve.

<a id="typische-fehler-29"></a>
## Typische Fehler

1. Halbleiter- und Metallverhalten bei Temperaturabhängigkeit verwechselt (Vorzeichen von $d\varrho/dT$).
2. Bandlücke $E_g$ wird mit der thermischen Energie $k_BT$ verwechselt (unterschiedliche Größenordnungen, siehe Beispiel 1).

<a id="verbindungen-30"></a>
## Verbindungen

- Direkte Fortsetzung von Kapitel 9 (Temperaturabhängigkeit des Widerstands, dort nur empirisch eingeführt, hier mikroskopisch motiviert).
- Wiedemann-Franz-Gesetz verbindet zurück zu Kapitel 3 (Wärmeleitung).
- Erster Kontaktpunkt mit Konzepten, die in der Festkörperphysik/Quantenmechanik vertieft werden (außerhalb dieser Vorlesung).

<a id="zusammenfassung-18"></a>
## Zusammenfassung

- Bändermodell erklärt Leiter/Halbleiter/Isolator über die Größe der Bandlücke $E_g$ relativ zu $k_BT$.
- Metalle: $\varrho$ steigt mit $T$ (mehr Streuung, $n$ konstant).
- Halbleiter: $\varrho$ sinkt mit $T$ (exponentiell mehr Ladungsträger, $n(T)\propto e^{-E_g/2k_BT}$).
- Supraleiter: $R=0$ unterhalb $T_c$ (quantenmechanisch, hier nicht hergeleitet).

---

<a id="kapitel-11-magnetismus-i-kraftwirkungen-lorentzkraft"></a>
# Kapitel 11: Magnetismus I — Kraftwirkungen (Lorentzkraft)

<a id="motivation-31"></a>
## Motivation

Elektrische und magnetische Phänomene wurden lange als getrennt betrachtet — bis Ørsted 1820 entdeckte, dass ein stromdurchflossener Draht eine Kompassnadel ablenkt: **bewegte** Ladungen erzeugen magnetische Effekte. Das ist der erste Hinweis auf die tiefe Einheit von Elektrizität und Magnetismus, die Maxwell später vollständig formalisierte (Kapitel 15). In diesem Kapitel betrachten wir zunächst nur die *Kraftwirkung* eines gegebenen Magnetfelds auf bewegte Ladungen — die *Erzeugung* von Magnetfeldern folgt in Kapitel 12.

<a id="intuition-31"></a>
## Intuition

Die Lorentzkraft ist ungewöhnlich, weil sie **senkrecht** sowohl zur Geschwindigkeit als auch zum Feld steht — sie ändert also nie den Betrag der Geschwindigkeit (verrichtet keine Arbeit!), sondern nur ihre Richtung. Stell dir das wie eine unsichtbare Hand vor, die ein Teilchen immer seitlich "anschubst", nie nach vorne oder hinten — das Ergebnis ist eine Kreis- oder Spiralbewegung, niemals eine Geschwindigkeitsänderung im Betrag. Das ist fundamental anders als die elektrische Kraft (Kapitel 6), die sehr wohl Arbeit verrichten kann.

<a id="formale-definitionen-31"></a>
## Formale Definitionen

**Definition 11.1 (Lorentzkraft).**
$$\vec F_L = q\,\vec v\times\vec B, \qquad [\vec B] = \text{T (Tesla)} = \frac{\text{Vs}}{\text{m}^2}.$$
Allgemein (elektrisches + magnetisches Feld):
$$\vec F = q(\vec E+\vec v\times\vec B).$$

**Definition 11.2 (Magnetisches Dipolmoment einer Stromschleife).**
$$\vec\mu := I\,A\,\hat n,$$
mit Flächenvektor $\hat n$ nach der Rechte-Hand-Regel zur Umlaufrichtung des Stroms.

<a id="eigenschaften-27"></a>
## Eigenschaften

| Eigenschaft | Aussage | Begründung |
|---|---|---|
| Lorentzkraft verrichtet keine Arbeit | $\vec F_L\perp\vec v$ stets | $\vec F_L\cdot\vec v = q(\vec v\times\vec B)\cdot\vec v=0$ (Spatprodukt mit wiederholtem Vektor) |
| Bahn bei homogenem $\vec B$, $\vec v\perp\vec B$ | Kreisbahn | konstante Zentripetalkraft senkrecht zu $\vec v$ |
| Bahn bei $\vec v$ mit Komponente $\parallel\vec B$ | Schraubenbahn (Helix) | Parallelkomponente unbeeinflusst, Senkrechtkomponente kreist |
| Drehmoment auf Stromschleife | $\vec M=\vec\mu\times\vec B$ | strukturidentisch zu elektrischem Dipol (Kapitel 6) |

<a id="sätze-27"></a>
## Sätze

<a id="satz-111-kreisbahn-im-homogenen-magnetfeld"></a>
### Satz 11.1 (Kreisbahn im homogenen Magnetfeld)

**Aussage:** Ein geladenes Teilchen mit $\vec v\perp\vec B$ bewegt sich auf einer Kreisbahn mit Radius
$$r = \frac{mv}{|q|B},$$
und Umlauffrequenz (Zyklotronfrequenz) $\omega = \dfrac{|q|B}{m}$ (unabhängig von $v$!).

**Beweis (Beweisstil: Gleichsetzen von Lorentzkraft und Zentripetalkraft).**
Für Kreisbewegung ist die notwendige Zentripetalkraft $F_{Zp}=mv^2/r$, radial nach innen gerichtet. Die Lorentzkraft $F_L=qvB$ (für $\vec v\perp\vec B$) steht ebenfalls stets senkrecht zu $\vec v$, radial. Gleichsetzen:
$$qvB = \frac{mv^2}{r} \;\Longrightarrow\; r = \frac{mv}{qB}.$$
Mit $\omega=v/r$ folgt $\omega = v\cdot\dfrac{qB}{mv} = \dfrac{qB}{m}$ — unabhängig von $v$, eine bemerkenswerte Eigenschaft, die dem Zyklotron (Teilchenbeschleuniger) zugrunde liegt: Teilchen unterschiedlicher Geschwindigkeit brauchen dieselbe Zeit pro Umlauf. $\blacksquare$

<a id="satz-112-hall-effekt"></a>
### Satz 11.2 (Hall-Effekt)

**Aussage:** Fließt Strom $I$ durch einen Leiter (Dicke $d$, senkrecht dazu Magnetfeld $B$), stellt sich eine Querspannung (Hall-Spannung) ein:
$$U_H = \frac{I\,B}{n\,q\,d}.$$

**Voraussetzungen:** stationärer Strom, homogenes $B$-Feld senkrecht zur Stromrichtung.

**Beweisidee (Beweisstil: Kräftegleichgewicht quer zum Strom).**
Die driftenden Ladungsträger erfahren die Lorentzkraft $qv_{Drift}B$ senkrecht zur Stromrichtung — sie werden zur einen Seite des Leiters abgelenkt und häufen sich dort an, bis das entstehende elektrische Querfeld $E_H$ die Lorentzkraft gerade kompensiert: $qE_H=qv_{Drift}B \Rightarrow E_H=v_{Drift}B$. Mit $U_H=E_H\cdot d$ und $v_{Drift}=I/(nqA)=I/(nqd\cdot b)$ ($b$: Leiterbreite, $A=d\cdot b$) folgt nach Einsetzen $U_H=IB/(nqd)$ (die Breite $b$ kürzt sich heraus). $\blacksquare$

**Bedeutung:** Der Hall-Effekt erlaubt (a) die Messung von Magnetfeldern (Hall-Sonde) und (b) die Bestimmung von Vorzeichen und Dichte $n$ der Ladungsträger — historisch wichtig für den Nachweis, dass in Metallen negative Ladungsträger (Elektronen) den Strom tragen.

<a id="algorithmen-19"></a>
## Algorithmen

**Lösungsstrategie für Bewegung im Magnetfeld**
```
EINGABE: geladenes Teilchen mit Anfangsgeschwindigkeit v, Feld B
1. Zerlege v in Komponenten parallel und senkrecht zu B
2. Parallelkomponente: unverändert (keine Kraft in dieser Richtung)
3. Senkrechtkomponente: Kreisbewegung mit r = mv_perp/(|q|B),
   ω = |q|B/m
4. WENN v_parallel = 0: reine Kreisbahn
   WENN v_parallel ≠ 0: Überlagerung = Schraubenbahn (Helix)
5. Für Kräfte-/Energiefragen: beachte, dass B nie Arbeit verrichtet
   (nur E-Feld-Anteile ändern die kinetische Energie!)
AUSGABE: Bahnkurve, Radius, Frequenz
```
- **Typischer Fehler:** Es wird versucht, mit der Lorentzkraft eine Energieänderung zu berechnen — das ist grundsätzlich unmöglich, da $\vec F_L\perp\vec v$ immer gilt.

<a id="beispiele-29"></a>
## Beispiele

**Beispiel 1 (leicht):** Ein Elektron ($q=-e$, $v=10^6\,\text{m/s}$) bewegt sich senkrecht zu $B=0{,}1\,\text{T}$. Berechne $F_L$.
*Lösung:* $F_L=|q|vB=1{,}6\cdot10^{-19}\cdot10^6\cdot0{,}1=1{,}6\cdot10^{-14}\,\text{N}$.

**Beispiel 2 (mittel):** Dasselbe Elektron — berechne den Bahnradius.
*Lösung:* $r=mv/(|q|B) = 9{,}1\cdot10^{-31}\cdot10^6/(1{,}6\cdot10^{-19}\cdot0{,}1)\approx5{,}7\cdot10^{-5}\,\text{m}$.

**Beispiel 3 (mittel):** Ein Massenspektrometer nutzt Kreisbahnen im Magnetfeld, um Ionen nach Masse zu trennen. Zwei Ionen gleicher Ladung, gleicher Geschwindigkeit, aber $m_1\neq m_2$ — welches hat den größeren Bahnradius?
*Lösung:* $r\propto m$ (bei festem $q,v,B$) — das schwerere Ion hat den größeren Radius.

**Beispiel 4 (schwer):** Ein Proton fliegt mit $v=(v_x,0,v_z)$ in ein Feld $\vec B=(0,0,B)$. Beschreibe die Bahn.
*Lösung:* $v_z$ (parallel zu $B$) bleibt unverändert. $v_x$ (senkrecht zu $B$) erzeugt eine Kreisbewegung in der $xy$-Ebene mit $r=mv_x/(qB)$. Überlagerung: eine Schraubenbahn (Helix) mit Ganghöhe $h=v_z\cdot T=v_z\cdot2\pi m/(qB)$ pro Umlauf.

<a id="gegenbeispiele-29"></a>
## Gegenbeispiele

- Für $\vec v\parallel\vec B$ ist $\vec F_L=q\vec v\times\vec B=0$ — **keine** Kraftwirkung, das Teilchen fliegt geradeaus weiter (Grenzfall, oft in Klausuraufgaben als "Fallstrick" verwendet).
- Die Formel $\omega=qB/m$ (Zyklotronfrequenz) gilt **nicht** mehr exakt bei relativistischen Geschwindigkeiten (dort wird $m\to\gamma m$ geschwindigkeitsabhängig) — für diese Vorlesung nicht relevant, aber wichtige Erinnerung an den Gültigkeitsbereich.

<a id="typische-klausuraufgaben-30"></a>
## Typische Klausuraufgaben

- Kreisradius/Zyklotronfrequenz-Berechnung für geladene Teilchen im $B$-Feld — Erkennungsmerkmal: "Massenspektrometer", "Zyklotron", "Kreisbahn".
- Hall-Effekt-Berechnung, oft kombiniert mit Bestimmung der Ladungsträgerdichte $n$ — Erkennungsmerkmal: "Hall-Spannung", "Hall-Sonde".
- Kombination $\vec E$- und $\vec B$-Feld (Geschwindigkeitsfilter, "Wien-Filter": $qE=qvB \Rightarrow v=E/B$ für ungestörten Durchgang).
- Schraubenbahn-Aufgaben (3D-Bewegung).

<a id="typische-fehler-30"></a>
## Typische Fehler

1. Vorzeichen der Ladung bei der Kreuzproduktrichtung vergessen (Elektronen kreisen entgegengesetzt zu positiven Ladungen bei gleichem $\vec v,\vec B$).
2. Es wird versucht, eine Geschwindigkeits-/Energieänderung durch $\vec B$ allein zu berechnen (unmöglich, siehe Eigenschaftentabelle).
3. Bei $\vec v$ nicht senkrecht zu $\vec B$ wird trotzdem die einfache Kreisbahnformel (ohne Zerlegung in Parallel-/Senkrechtkomponente) verwendet.

<a id="verbindungen-31"></a>
## Verbindungen

- Das magnetische Dipolmoment (Def. 11.2) und sein Drehmoment $\vec M=\vec\mu\times\vec B$ sind strukturell identisch zum elektrischen Dipol (Kapitel 6) — direkte Vergleichstabelle:

| | Elektrischer Dipol | Magnetischer Dipol |
|---|---|---|
| Moment | $\vec p=Q\vec d$ | $\vec\mu=IA\hat n$ |
| Drehmoment | $\vec M=\vec p\times\vec E$ | $\vec M=\vec\mu\times\vec B$ |
| Energie | $E_{pot}=-\vec p\cdot\vec E$ | $E_{pot}=-\vec\mu\cdot\vec B$ |

- Die Erzeugung des $\vec B$-Feldes selbst (durch Ströme) folgt in Kapitel 12.
- Der Hall-Effekt verbindet dieses Kapitel zurück zu Kapitel 9/10 (Ladungsträgerdichte, Vorzeichen der Ladungsträger).

<a id="zusammenfassung-19"></a>
## Zusammenfassung

- Lorentzkraft $\vec F_L=q\vec v\times\vec B$ steht immer senkrecht zu $\vec v$ — verrichtet keine Arbeit.
- Kreisbahn bei $\vec v\perp\vec B$: $r=mv/(|q|B)$, $\omega=|q|B/m$ (geschwindigkeitsunabhängig).
- Schraubenbahn bei beliebigem $\vec v$: Zerlegung in Parallel-/Senkrechtkomponente.
- Hall-Effekt: $U_H=IB/(nqd)$ — Messung von $B$ und Bestimmung von Ladungsträgereigenschaften.
- Magnetisches Dipolmoment $\vec\mu=IA\hat n$, Drehmoment $\vec M=\vec\mu\times\vec B$ — Analogie zum elektrischen Dipol.

---

<a id="kapitel-12-magnetismus-ii-feldquellen-und-magnetische-materialien"></a>
# Kapitel 12: Magnetismus II — Feldquellen und magnetische Materialien

<a id="motivation-32"></a>
## Motivation

Kapitel 11 behandelte die Wirkung eines *gegebenen* Magnetfelds. Jetzt fragen wir: Wie entsteht ein Magnetfeld überhaupt? Ørsteds Entdeckung (bewegte Ladungen/Ströme erzeugen $\vec B$) wird hier quantifiziert (Biot-Savart-Gesetz, Ampère'sches Gesetz) — das magnetische Analogon zum Coulombgesetz/Gauß'schen Gesetz der Elektrostatik, mit einem entscheidenden strukturellen Unterschied: Es gibt **keine magnetischen Monopole**.

<a id="intuition-32"></a>
## Intuition

Ströme erzeugen Magnetfelder, die sich *um* den Strom herum wickeln — nicht radial wie beim elektrischen Feld einer Punktladung, sondern zirkulär, wie die Wirbel, die ein Löffel beim Umrühren im Tee erzeugt. Das Fehlen magnetischer Monopole bedeutet: Jede Feldlinie eines $\vec B$-Feldes ist geschlossen (hat keinen Anfang und kein Ende) — im Gegensatz zu elektrischen Feldlinien, die an Ladungen beginnen/enden.

<a id="formale-definitionen-32"></a>
## Formale Definitionen

**Definition 12.1 (Biot-Savart-Gesetz).**
Das Magnetfeld eines stromdurchflossenen Leiterelements $d\vec\ell$ am Aufpunkt $\vec r$ (relativ zum Leiterelement):
$$d\vec B = \frac{\mu_0}{4\pi}\frac{I\,d\vec\ell\times\hat r}{r^2},$$
mit der **magnetischen Feldkonstante** $\mu_0 = 4\pi\cdot10^{-7}\,\text{Tm/A}$ (bzw. $\text{Vs/(Am)}$).

**Definition 12.2 (Magnetischer Fluss).**
$$\Phi_B := \int_A\vec B\cdot d\vec A.$$

**Definition 12.3 (Magnetisierung, magnetische Feldstärke).**
Analog zu Def. 8.1/8.4:
$$\vec M := \frac1V\sum_i\vec\mu_i, \qquad \vec H := \frac{\vec B}{\mu_0}-\vec M.$$

<a id="eigenschaften-28"></a>
## Eigenschaften

| Eigenschaft | Aussage | Begründung |
|---|---|---|
| Keine magnetischen Monopole | $\operatorname{div}\vec B=0$ überall (2. Maxwell-Gleichung) | nie beobachtet; $\vec B$-Feldlinien sind stets geschlossen |
| $\vec B$-Feldlinien um Draht | konzentrische Kreise | Rechte-Hand-Regel (Daumen = Stromrichtung, Finger = $\vec B$) |

**Vergleichstabelle magnetische Materialien:**

| Typ | $\chi_m$ (magn. Suszeptibilität) | Mikroskopischer Ursprung | Beispiel |
|---|---|---|---|
| Diamagnetisch | $\chi_m<0$, sehr klein | induzierte Gegenmomente (Lenz'sche Regel auf atomarer Ebene) | Wasser, Kupfer, Bismut |
| Paramagnetisch | $\chi_m>0$, klein | permanente atomare Momente richten sich aus | Aluminium, Sauerstoff |
| Ferromagnetisch | $\chi_m\gg1$, stark nichtlinear | kollektive Ausrichtung in Domänen (Weiss-Bezirke) | Eisen, Kobalt, Nickel |

<a id="sätze-28"></a>
## Sätze

<a id="satz-121-div-b-0-2-maxwell-gleichung"></a>
### Satz 12.1 (Div B = 0 — 2. Maxwell-Gleichung)

**Aussage:** $$\operatorname{div}\vec B(\vec r) = 0 \quad\text{überall}, \qquad \oint_S\vec B\cdot d\vec A = 0\ \text{(für jede geschlossene Fläche)}.$$

**Bedeutung:** Formalisiert die Abwesenheit magnetischer Monopole — das strukturelle Gegenstück zu $\operatorname{div}\vec E=\rho/\varepsilon_0$ (Satz 7.2), nur mit Quellstärke null.

**Beweisidee:** Wird in dieser Vorlesung als empirischer Befund (keine magnetischen Monopole je beobachtet) postuliert, nicht aus tieferliegenden Prinzipien hergeleitet — konsistent mit der Struktur des Biot-Savart-Gesetzes, bei dem $d\vec B\perp d\vec\ell$ und $d\vec B\perp\hat r$ stets zirkuläre, geschlossene Feldlinien erzwingt.

<a id="satz-122-magnetfeld-eines-geraden-unendlich-langen-leiters"></a>
### Satz 12.2 (Magnetfeld eines geraden, unendlich langen Leiters)

**Aussage:** $$B(r) = \frac{\mu_0 I}{2\pi r}.$$

**Beweis (Beweisstil: direkte Integration von Biot-Savart über den unendlichen Draht).**

Für ein Leiterelement $d\vec\ell=dz\,\hat e_z$ bei $z$ auf dem Draht (Aufpunkt im Abstand $r$ senkrecht zum Draht) ist $|d\vec\ell\times\hat r| = dz\sin\theta$, mit $\sin\theta=r/\sqrt{r^2+z^2}$ (Winkel zwischen Draht und Verbindungslinie zum Aufpunkt). Alle Beiträge $d\vec B$ zeigen (wegen der Zylindersymmetrie um den Draht) in dieselbe tangentiale Richtung, sodass wir die Beträge direkt aufaddieren dürfen:
$$B = \frac{\mu_0I}{4\pi}\int_{-\infty}^{\infty} \frac{dz\cdot r}{(r^2+z^2)^{3/2}}.$$
Mit der Substitution $z=r\tan\phi$ ($dz=r\sec^2\phi\,d\phi$, $r^2+z^2=r^2\sec^2\phi$) wird das Integral zu
$$B = \frac{\mu_0I}{4\pi r}\int_{-\pi/2}^{\pi/2}\cos\phi\,d\phi = \frac{\mu_0I}{4\pi r}\cdot2 = \frac{\mu_0I}{2\pi r}. \qquad\blacksquare$$

<a id="satz-123-ampèresches-gesetz"></a>
### Satz 12.3 (Ampère'sches Gesetz)

**Aussage:** $$\oint_C\vec B\cdot d\vec s = \mu_0 I_{umschlossen}.$$

**Voraussetzungen:** stationärer Strom, $C$ geschlossene Kurve, $I_{umschlossen}$ = Nettostrom durch eine von $C$ berandete Fläche.

**Beweisidee (Beweisstil: Nachweis für den geraden Leiter mit Kreis als Integrationsweg, dann Verallgemeinerung analog zu Satz 7.1).**

Für einen geraden Leiter mit Kreis vom Radius $r$ um den Draht als Integrationsweg $C$: $\vec B$ ist überall auf $C$ tangential mit konstantem Betrag $B(r)=\mu_0I/(2\pi r)$ (Satz 12.2), also
$$\oint_C\vec B\cdot d\vec s = B(r)\cdot2\pi r = \mu_0I.$$
Für eine *beliebige* geschlossene Kurve um denselben Draht liefert eine dem Raumwinkelargument von Satz 7.1 analoge Überlegung (hier: "Umschlingungswinkel" statt Raumwinkel) dasselbe Ergebnis $\mu_0I$, solange die Kurve den Draht genau einmal umschließt; Kurven, die den Draht nicht umschließen, liefern null. Für beliebige Stromverteilungen folgt die allgemeine Aussage durch Superposition (wie bei Satz 7.1, Schritt 4). $\blacksquare$

**Bedeutung:** Analog zum Gauß'schen Gesetz (elektrisch) ist Ampère's Gesetz das effiziente Werkzeug zur Feldberechnung bei Stromverteilungen mit hoher Symmetrie (langer Draht, Spule, Toroid).

<a id="satz-124-magnetfeld-einer-langen-spule"></a>
### Satz 12.4 (Magnetfeld einer langen Spule)

**Aussage:** Im Inneren einer langen Spule (Länge $\ell$, $N$ Windungen, Strom $I$), fern von den Enden:
$$B = \mu_0\frac{N}{\ell}I =: \mu_0 nI \quad(n:=N/\ell\text{, Windungsdichte}), \qquad B_{außen}\approx0.$$

**Beweis (Beweisstil: Anwendung des Ampère'schen Gesetzes mit rechteckigem Integrationsweg).**
Wähle als Integrationsweg $C$ ein Rechteck: eine Seite der Länge $L$ im Spuleninneren (parallel zur Achse), die gegenüberliegende Seite weit außerhalb (wo $B\approx0$ angenommen wird), verbunden durch zwei kurze Seiten senkrecht zur Achse (deren Beitrag zum Wegintegral verschwindet, da dort $\vec B\perp d\vec s$ bzw. $B\approx0$ außen). Der umschlossene Strom ist $I_{umschlossen}=N'\cdot I$, mit $N'=nL$ Windungen innerhalb der Weglänge $L$. Ampère'sches Gesetz:
$$B\cdot L = \mu_0\, nL\, I \;\Longrightarrow\; B=\mu_0 nI. \qquad\blacksquare$$

<a id="algorithmen-20"></a>
## Algorithmen

**Lösungsstrategie: Ampère'sches Gesetz anwenden**
```
EINGABE: Stromverteilung mit Symmetrie
1. Erkenne Symmetrietyp (analog zu Gauß'schem Gesetz, Kapitel 7):
   Gerader Draht (Zylindersymmetrie) → kreisförmiger Integrationsweg
   Lange Spule / Toroid → rechteckiger bzw. kreisförmiger Weg im Inneren
2. Prüfe: Ist |B| auf dem gewählten Weg konstant und B parallel zu ds?
   WENN NEIN: falscher Integrationsweg gewählt
3. Bestimme I_umschlossen (Vorzeichen nach Rechte-Hand-Regel!)
4. Löse B * (Weglänge) = μ0 * I_umschlossen nach B auf
AUSGABE: B(r) bzw. B im Spuleninneren
```
- **Typischer Fehler:** Vorzeichen von $I_{umschlossen}$ falsch (Rechte-Hand-Regel zwischen Umlaufsinn von $C$ und Stromrichtung nicht konsistent angewendet).

<a id="beispiele-30"></a>
## Beispiele

**Beispiel 1 (leicht):** Ein gerader Draht führt $I=5\,\text{A}$. Berechne $B$ im Abstand $r=2\,\text{cm}$.
*Lösung:* $B=\mu_0I/(2\pi r) = 4\pi\cdot10^{-7}\cdot5/(2\pi\cdot0{,}02) = 5\cdot10^{-5}\,\text{T}$.

**Beispiel 2 (mittel):** Eine Spule ($N=500$, $\ell=20\,\text{cm}$, $I=2\,\text{A}$). Berechne $B$ im Inneren.
*Lösung:* $B=\mu_0(N/\ell)I = 4\pi\cdot10^{-7}\cdot(500/0{,}2)\cdot2\approx6{,}28\cdot10^{-3}\,\text{T}$.

**Beispiel 3 (mittel):** Zwei parallele, stromdurchflossene Drähte ($I_1=I_2=10\,\text{A}$, Abstand $d=5\,\text{cm}$, gleiche Richtung). Berechne die Kraft pro Länge zwischen ihnen (nutze $\vec F=I\vec\ell\times\vec B$ aus Kap. 11 kombiniert mit Satz 12.2).
*Lösung:* $B_1$ am Ort von Draht 2: $B_1=\mu_0I_1/(2\pi d)$. Kraft pro Länge: $F/\ell = I_2B_1 = \mu_0I_1I_2/(2\pi d) = 4\pi10^{-7}\cdot100/(2\pi\cdot0{,}05) = 4\cdot10^{-4}\,\text{N/m}$ (anziehend, da gleiche Stromrichtung — diese Kraft definiert historisch die Einheit Ampere!).

<a id="gegenbeispiele-30"></a>
## Gegenbeispiele

- Ampère'sches Gesetz liefert für **nicht-symmetrische** Stromverteilungen zwar eine korrekte, aber nicht direkt nach $B$ auflösbare Gleichung (analog zu Gauß'schem Gesetz, Kapitel 7).
- Am **Rand/Ende** einer endlichen Spule gilt $B=\mu_0nI$ **nicht** mehr exakt (dort treten Streufelder auf, ähnlich den Randeffekten beim Plattenkondensator, Kapitel 6).

<a id="typische-klausuraufgaben-31"></a>
## Typische Klausuraufgaben

- Feldberechnung mit Ampère'schem Gesetz für Draht/Spule/Toroid — Strategie: siehe Algorithmus.
- Kraft zwischen parallelen Strömen — Kombination aus Kapitel 11 und 12.
- Qualitative Fragen zu Dia-/Para-/Ferromagnetismus (Domänenstruktur, Hysterese bei Ferromagneten — hier nur qualitativ erwähnt).

<a id="typische-fehler-31"></a>
## Typische Fehler

1. Rechte-Hand-Regel falsch angewendet (Vorzeichen/Richtung von $\vec B$).
2. Ampère'sches Gesetz auf unsymmetrische Probleme angewendet und $B$ trotzdem vor das Integral gezogen.
3. Streufelder an Spulenenden vernachlässigt, wo die Näherung eigentlich nicht mehr gilt (nur bei expliziter Fragestellung relevant).

<a id="verbindungen-32"></a>
## Verbindungen

- Satz 12.1 ist die **2. Maxwell-Gleichung**, Satz 12.3 die Vorstufe der **4. Maxwell-Gleichung** (die in Kapitel 15 durch den Maxwell'schen Verschiebungsstrom noch ergänzt wird!).
- Strukturelle Analogie zu Kapitel 7 (Gauß'sches Gesetz ↔ Ampère'sches Gesetz) — beide sind "Integralformen", die bei Symmetrie eine schnelle Feldberechnung erlauben.
- Die Kraft zwischen parallelen Strömen (Beispiel 3) ist die historische Grundlage der SI-Definition des Ampere.
- Grundlage für Kapitel 13 (Induktion) — die zeitliche Änderung des hier definierten magnetischen Flusses $\Phi_B$ erzeugt eine induzierte Spannung.

<a id="zusammenfassung-20"></a>
## Zusammenfassung

- Biot-Savart-Gesetz: $d\vec B = \dfrac{\mu_0}{4\pi}\dfrac{Id\vec\ell\times\hat r}{r^2}$ — Grundgesetz zur Feldberechnung.
- $\operatorname{div}\vec B=0$: keine magnetischen Monopole, Feldlinien stets geschlossen.
- Ampère'sches Gesetz: $\oint\vec B\cdot d\vec s=\mu_0I_{umschlossen}$ — effizient bei Symmetrie.
- Gerader Draht: $B=\mu_0I/(2\pi r)$; lange Spule: $B=\mu_0nI$.
- Magnetische Materialien: dia- (schwach abstoßend), para- (schwach anziehend), ferromagnetisch (stark, nichtlinear, Domänenstruktur).

---

<a id="kapitel-13-elektrodynamik-induktion"></a>
# Kapitel 13: Elektrodynamik — Induktion

<a id="motivation-33"></a>
## Motivation

Wir haben gesehen: Ströme erzeugen Magnetfelder (Kapitel 12). Faraday stellte 1831 die umgekehrte Frage: Kann ein Magnetfeld einen Strom erzeugen? Die Antwort ist ja — aber nur, wenn sich das Feld (bzw. der von einer Leiterschleife eingeschlossene Fluss) *ändert*. Diese Entdeckung ist die Grundlage praktisch der gesamten elektrischen Energieerzeugung (Generatoren) und schließt den Kreis zur vollständigen Vereinigung von Elektrizität und Magnetismus.

<a id="intuition-33"></a>
## Intuition

Stell dir den magnetischen Fluss durch eine Leiterschleife als "Menge an Feldlinien" vor, die durch die Schleife hindurchtreten. Ändert sich diese Menge (weil sich das Feld ändert, die Schleife bewegt oder gedreht wird), "spürt" die Schleife das als induzierte Spannung — als würde die Natur versuchen, die Änderung zu "kompensieren". Diese Kompensationstendenz (Lenz'sche Regel) ist ein Spezialfall des allgemeineren Prinzips "System reagiert der Störung entgegen" (vergleichbar mit Trägheit in der Mechanik: ein Körper "widersetzt" sich einer Geschwindigkeitsänderung).

<a id="formale-definitionen-33"></a>
## Formale Definitionen

**Definition 13.1 (Induktionsspannung).**
$$U_{ind} := -\frac{d\Phi_B}{dt}.$$

**Definition 13.2 (Selbstinduktivität).**
$$L := \frac{\Phi_B}{I}, \qquad [L]=\text{H (Henry)} = \text{Vs/A}.$$

<a id="eigenschaften-29"></a>
## Eigenschaften

| Eigenschaft | Aussage |
|---|---|
| Induktion tritt auf bei | Änderung von $B$, Fläche $A$, oder Winkel zwischen $\vec B$ und $\hat n$ |
| Lenz'sche Regel | Der induzierte Strom fließt so, dass er seiner Ursache entgegenwirkt (Vorzeichen in Def. 13.1!) |
| Selbstinduktivität einer langen Spule | $L=\mu_0n^2A\ell = \mu_0\dfrac{N^2}{\ell}A$ |

<a id="sätze-29"></a>
## Sätze

<a id="satz-131-faradaysches-induktionsgesetz-3-maxwell-gleichung"></a>
### Satz 13.1 (Faraday'sches Induktionsgesetz — 3. Maxwell-Gleichung)

**Aussage:** $$U_{ind} = \oint_C\vec E\cdot d\vec s = -\frac{d}{dt}\int_A\vec B\cdot d\vec A.$$

**Bedeutung:** Ein sich zeitlich änderndes Magnetfeld erzeugt ein elektrisches Wirbelfeld (nicht mehr konservativ, im Gegensatz zu Satz 6.1!) — dies ist eine fundamentale Erweiterung der Elektrostatik.

**Beweisidee (Beweisstil: Spezialfall — bewegter Leiter im konstanten Feld, dann Verallgemeinerung als Postulat).**

Für den Spezialfall einer Leiterschleife, die sich mit Geschwindigkeit $\vec v$ durch ein *zeitlich konstantes* $\vec B$-Feld bewegt: Auf die Ladungsträger im bewegten Leiter wirkt die Lorentzkraft $\vec F=q\vec v\times\vec B$ (Kapitel 11), die entlang des Leiters eine effektive "bewegungsinduzierte" elektrische Feldstärke $\vec E'=\vec v\times\vec B$ erzeugt. Integriert man diese entlang der Schleife und wandelt in eine Flussänderung um (Rechenschritt: geometrische Betrachtung der pro Zeit überstrichenen Fläche), erhält man exakt $U_{ind}=-d\Phi_B/dt$.

Für den allgemeineren Fall eines *ruhenden* Leiters in einem *zeitlich veränderlichen* Feld lässt sich dies nicht mehr auf die Lorentzkraft zurückführen — hier postulierte Faraday (bzw. später Maxwell in voller Allgemeinheit) das Gesetz als eigenständiges Naturgesetz, bestätigt durch alle bekannten Experimente. **Markierung:** Vollständiger allgemeiner Beweis erfordert die relativistische Vereinheitlichung von $\vec E$ und $\vec B$ (Spezielle Relativitätstheorie) und geht über diese Vorlesung hinaus — hier wird das Gesetz für den allgemeinen Fall als postuliert/experimentell bestätigt behandelt.

<a id="satz-132-selbstinduktion-und-aufbauverhalten-in-einer-rl-schaltung"></a>
### Satz 13.2 (Selbstinduktion und Aufbauverhalten in einer RL-Schaltung)

**Aussage:** Beim Einschalten einer Spannung $U_0$ an einen Kreis mit Widerstand $R$ und Induktivität $L$ steigt der Strom gemäß
$$I(t) = \frac{U_0}{R}\left(1-e^{-t/\tau}\right), \qquad \tau = \frac{L}{R}.$$

**Beweis (Beweisstil: Aufstellen und Lösen der Differentialgleichung — direkte Analogie zur RC-Aufladung).**

Maschenregel (Satz 9.3) für den RL-Kreis: $U_0 = IR + L\dfrac{dI}{dt}$ (die Spule erzeugt eine Gegenspannung $U_L=L\,dI/dt$, Konsequenz aus Satz 13.1 mit $\Phi_B=LI$, Def. 13.2). Dies ist eine lineare, inhomogene Differentialgleichung 1. Ordnung:
$$\frac{dI}{dt} + \frac{R}{L}I = \frac{U_0}{L}.$$
Die allgemeine Lösung ist die Summe aus partikulärer Lösung ($I_p=U_0/R$, stationärer Endwert) und homogener Lösung ($I_h=Ce^{-Rt/L}$). Mit der Anfangsbedingung $I(0)=0$ (Spule verhindert sprunghafte Stromänderung):
$$0 = \frac{U_0}{R}+C \;\Longrightarrow\; C=-\frac{U_0}{R}.$$
Also
$$I(t) = \frac{U_0}{R}\left(1-e^{-Rt/L}\right) = \frac{U_0}{R}\left(1-e^{-t/\tau}\right),\quad \tau=\frac{L}{R}. \qquad\blacksquare$$

**Vergleichstabelle RC- vs. RL-Aufladung** (Verbindung zu Kapitel 9):

| | RC-Kreis (Kondensator) | RL-Kreis (Spule) |
|---|---|---|
| Zeitkonstante | $\tau=RC$ | $\tau=L/R$ |
| Verhindert Sprünge in | Spannung $U_C$ | Strom $I$ |
| Anfangswert | $U_C(0)=0$ | $I(0)=0$ |
| Endwert | $U_C(\infty)=U_0$ | $I(\infty)=U_0/R$ |

<a id="algorithmen-21"></a>
## Algorithmen

**Lösungsstrategie für Induktionsaufgaben**
```
EINGABE: Anordnung mit zeitlich veränderlichem Fluss
1. Bestimme Φ_B(t) = ∫∫ B·dA — beachte ALLE zeitabhängigen Faktoren:
   B(t), A(t), Winkel(t) zwischen B und Flächennormale
2. U_ind = -dΦ_B/dt
3. Bestimme Vorzeichen/Richtung des induzierten Stroms über
   Lenz'sche Regel (nicht nur aus der Formel — Plausibilitätscheck!)
4. WENN Selbstinduktion relevant (Spule im Stromkreis):
   Maschenregel mit U_L = L dI/dt aufstellen, DGL lösen
AUSGABE: U_ind(t), I(t)
```
- **Typischer Fehler:** Nur EINEN der drei möglichen zeitabhängigen Faktoren ($B$, $A$, Winkel) berücksichtigen, obwohl mehrere gleichzeitig variieren (z. B. bei einer rotierenden Spule im konstanten Feld ändert sich der *Winkel*, nicht $B$ selbst — leicht übersehen).

<a id="beispiele-31"></a>
## Beispiele

**Beispiel 1 (leicht):** Eine Leiterschleife ($A=0{,}01\,\text{m}^2$) liegt in einem Feld, das sich mit $dB/dt=0{,}5\,\text{T/s}$ ändert. Berechne $U_{ind}$.
*Lösung:* $U_{ind}=-A\dfrac{dB}{dt} = -0{,}01\cdot0{,}5=-5\cdot10^{-3}\,\text{V}$.

**Beispiel 2 (mittel):** Eine Spule mit $N=200$ Windungen, $A=5\,\text{cm}^2$, wird in $t=0{,}1\,\text{s}$ von $B_1=0$ auf $B_2=0{,}8\,\text{T}$ hochgefahren. Berechne die mittlere Induktionsspannung.
*Lösung:* $U_{ind}=-N\dfrac{\Delta\Phi_B}{\Delta t} = -N\dfrac{A\Delta B}{\Delta t} = -200\cdot\dfrac{5\cdot10^{-4}\cdot0{,}8}{0{,}1}=-0{,}8\,\text{V}$.

**Beispiel 3 (mittel):** Eine Spule mit $L=0{,}5\,\text{H}$, $R=10\,\Omega$, an $U_0=20\,\text{V}$. Berechne $\tau$ und $I$ nach $t=\tau$.
*Lösung:* $\tau=L/R=0{,}05\,\text{s}$. $I(\tau)=\dfrac{U_0}{R}(1-e^{-1})\approx2\cdot0{,}632=1{,}26\,\text{A}$.

**Beispiel 4 (schwer):** Eine rechteckige Leiterschleife ($a\times b$) rotiert mit Winkelgeschwindigkeit $\omega$ in einem homogenen Feld $B$ um eine Achse in der Schleifenebene, senkrecht zu $\vec B$ bei $t=0$. Bestimme $U_{ind}(t)$.
*Lösung:* $\Phi_B(t)=BA\cos(\omega t)$ (Winkel zwischen $\vec B$ und Flächennormale ändert sich!). $U_{ind}=-\dfrac{d\Phi_B}{dt}=BA\omega\sin(\omega t)$ — dies ist das **Grundprinzip des Wechselstromgenerators** und motiviert direkt Kapitel 14 (sinusförmige Wechselspannung entsteht auf natürliche Weise aus Rotation).

<a id="gegenbeispiele-31"></a>
## Gegenbeispiele

- Eine Leiterschleife in einem **konstanten**, **unbewegten** Feld hat $U_{ind}=0$, unabhängig von der Feldstärke — nur *Änderungen* induzieren eine Spannung (häufiger Irrtum: "starkes Feld = starke Induktion", falsch, es zählt nur die *Änderungsrate*).
- Eine Schleife, deren Fläche sich ändert, aber deren *Flächenvektor* stets senkrecht zu $\vec B$ steht (z. B. Rotation um eine Achse parallel zu $\vec B$), hat trotz Bewegung $U_{ind}=0$, da sich $\Phi_B$ dabei nicht ändert.

<a id="typische-klausuraufgaben-32"></a>
## Typische Klausuraufgaben

- Berechnung von $U_{ind}$ bei zeitlich veränderlichem $B$, $A$ oder Winkel — Strategie: Alle drei Faktoren in $\Phi_B(t)$ explizit hinschreiben, dann ableiten.
- RL-Auf-/Entladevorgänge — direkte Analogie zu RC-Kreisen (Kapitel 9/hier), Strategie: Differentialgleichung aufstellen und mit bekannter Lösungsform vergleichen.
- Generatorprinzip (rotierende Schleife) — oft Übergang zu Wechselstromaufgaben (Kapitel 14).
- Lenz'sche Regel als Verständnisfrage ("in welche Richtung fließt der induzierte Strom?").

<a id="typische-fehler-32"></a>
## Typische Fehler

1. Nur $dB/dt$ berücksichtigt, obwohl sich auch $A$ oder der Winkel ändern (siehe Algorithmus-Warnung).
2. Vorzeichen/Minuszeichen in $U_{ind}=-d\Phi_B/dt$ vergessen — führt zu falscher Richtung des induzierten Stroms (Verletzung der Lenz'schen Regel/Energieerhaltung!).
3. RL- und RC-Zeitkonstanten verwechselt ($\tau=L/R$ vs. $\tau=RC$ — unterschiedliche Struktur!).
4. Bei Selbstinduktion wird vergessen, dass $L\,dI/dt$ eine *Gegenspannung* ist (Vorzeichen in der Maschengleichung).

<a id="verbindungen-33"></a>
## Verbindungen

- Satz 13.1 ist die **3. Maxwell-Gleichung** und schließt (zusammen mit dem noch fehlenden Maxwell'schen Verschiebungsstrom, Kapitel 15) die vollständige Vereinigung von Elektrizität und Magnetismus ab.
- Die RL-Aufladung (Satz 13.2) ist mathematisch identisch zur RC-Aufladung (Kapitel 9) — dieselbe Differentialgleichungsstruktur, andere physikalische Größen.
- Das Generatorprinzip (Beispiel 4) ist die physikalische Motivation für Kapitel 14 (Wechselstrom) — sinusförmige Spannungen entstehen natürlich aus Rotation im Magnetfeld.
- Lenz'sche Regel ist ein Spezialfall des allgemeineren Prinzips "Le Chatelier" bzw. Energieerhaltung (ein induzierter Strom, der seine Ursache *verstärken* würde, würde Energie aus dem Nichts erzeugen — Widerspruch zum 1. Hauptsatz).

<a id="zusammenfassung-21"></a>
## Zusammenfassung

- Faraday'sches Induktionsgesetz: $U_{ind}=-d\Phi_B/dt$ — jede Änderung des umschlossenen Flusses induziert eine Spannung.
- Lenz'sche Regel: induzierter Strom wirkt seiner Ursache entgegen (Vorzeichen in der Formel).
- Selbstinduktivität $L=\Phi_B/I$; RL-Aufladung mathematisch analog zur RC-Aufladung, $\tau=L/R$.
- Rotierende Leiterschleife im Magnetfeld erzeugt sinusförmige Spannung — Grundprinzip des Generators.

---

<a id="kapitel-14-wechselstromkreise"></a>
# Kapitel 14: Wechselstromkreise

<a id="motivation-34"></a>
## Motivation

Die meisten technischen Anwendungen (Stromnetz, Funktechnik) nutzen nicht Gleichstrom, sondern zeitlich sinusförmig veränderlichen Wechselstrom — nicht zuletzt, weil er sich (via Transformatoren, hier nicht vertieft) verlustarm auf hohe Spannungen transformieren lässt, und weil er (wie in Kapitel 13, Beispiel 4 gesehen) auf natürliche Weise aus rotierenden Generatoren entsteht. Kondensatoren und Spulen verhalten sich bei Wechselstrom fundamental anders als bei Gleichstrom — dieses Kapitel entwickelt das Werkzeug (komplexe Widerstände), um das systematisch zu berechnen.

<a id="intuition-34"></a>
## Intuition

Bei Gleichstrom "blockiert" ein Kondensator im stationären Zustand vollständig (er ist ja aufgeladen, kein weiterer Strom fließt) und eine Spule "blockiert" gar nicht (konstanter Strom erzeugt keine Gegenspannung). Bei Wechselstrom ändert sich das: Ein Kondensator wird ständig um- und aufgeladen — je schneller die Wechselspannung oszilliert, desto leichter "kommt der Strom durch" (der Kondensator wirkt wie ein frequenzabhängiger Widerstand, der bei hoher Frequenz klein wird). Eine Spule reagiert umgekehrt: Sie erzeugt bei schnellen Stromänderungen eine große Gegenspannung (Selbstinduktion, Kapitel 13) und "blockiert" daher hohe Frequenzen stärker.

Die komplexe Schreibweise ist ein **reines Rechenwerkzeug**: Sinus- und Kosinusfunktionen mit Phasenverschiebung lassen sich mühsam mit trigonometrischen Additionstheoremen addieren — oder elegant als Realteil komplexer Exponentialfunktionen, die sich einfach multiplizieren.

<a id="formale-definitionen-34"></a>
## Formale Definitionen

**Definition 14.1 (Wechselspannung, komplexe Darstellung).**
$$u(t) = \hat U\cos(\omega t) = \operatorname{Re}\{\hat U e^{i\omega t}\}.$$

**Definition 14.2 (Komplexer Widerstand, Impedanz).**
$$\underline Z := \frac{\underline U}{\underline I}, \qquad [\underline Z]=\Omega.$$

**Definition 14.3 (Impedanzen der Grundelemente).**

| Element | Impedanz $\underline Z$ | Phasenverschiebung ($u$ gegen $i$) |
|---|---|---|
| Widerstand $R$ | $R$ | $0$ |
| Kondensator $C$ | $\dfrac{1}{i\omega C}$ | $u$ eilt $i$ um $90°$ **nach** |
| Spule $L$ | $i\omega L$ | $u$ eilt $i$ um $90°$ **voraus** |

<a id="eigenschaften-30"></a>
## Eigenschaften

| Größe | Formel | Bedeutung |
|---|---|---|
| Betrag der Impedanz | $|\underline Z|=\sqrt{R^2+(X_L-X_C)^2}$ (Reihenschaltung RLC) | effektiver Widerstand |
| Blindwiderstände | $X_L=\omega L$, $X_C=1/(\omega C)$ | frequenzabhängig |
| Phasenwinkel | $\tan\varphi = (X_L-X_C)/R$ | Verschiebung zwischen $u(t)$ und $i(t)$ |
| Resonanz (Serienschwingkreis) | $\omega_0=1/\sqrt{LC}$ | $X_L=X_C\Rightarrow |\underline Z|=R$ minimal |

<a id="sätze-30"></a>
## Sätze

<a id="satz-141-impedanz-des-kondensators"></a>
### Satz 14.1 (Impedanz des Kondensators)

**Aussage:** $\underline Z_C = \dfrac{1}{i\omega C}$.

**Beweis (Beweisstil: direkte Herleitung aus $I=C\,dU/dt$).**
Für einen Kondensator gilt $Q=CU \Rightarrow I=dQ/dt=C\,dU/dt$. Mit dem Ansatz $\underline U(t)=\hat U e^{i\omega t}$:
$$\underline I(t) = C\frac{d}{dt}\left(\hat Ue^{i\omega t}\right) = i\omega C\,\hat Ue^{i\omega t} = i\omega C\,\underline U(t).$$
Also $\underline Z_C = \underline U/\underline I = \dfrac{1}{i\omega C}$. $\blacksquare$

<a id="satz-142-impedanz-der-spule"></a>
### Satz 14.2 (Impedanz der Spule)

**Aussage:** $\underline Z_L = i\omega L$.

**Beweis (Beweisstil: direkte Herleitung aus $U=L\,dI/dt$, Satz 13.2 verallgemeinert).**
Mit Ansatz $\underline I(t)=\hat Ie^{i\omega t}$ und $U_L=L\,dI/dt$ (aus Satz 13.2/Def. 13.2):
$$\underline U(t) = L\frac{d}{dt}\left(\hat Ie^{i\omega t}\right) = i\omega L\,\hat Ie^{i\omega t} = i\omega L\,\underline I(t) \;\Longrightarrow\; \underline Z_L=i\omega L. \qquad\blacksquare$$

<a id="satz-143-kirchhoffsche-regeln-gelten-unverändert-für-komplexe-größen"></a>
### Satz 14.3 (Kirchhoff'sche Regeln gelten unverändert für komplexe Größen)

**Aussage:** Knoten- und Maschenregel (Satz 9.3) gelten formal identisch für die komplexen Ströme/Spannungen $\underline I,\underline U$.

**Beweisidee:** Da die Maxwell-Gleichungen linear sind und $\operatorname{Re}\{\cdot\}$ mit Addition vertauscht, gelten alle linearen Beziehungen (insbesondere die Kirchhoff'schen Regeln) für die komplexen Amplituden genauso wie für die reellen Momentanwerte — Realteilbildung kann "am Ende" der Rechnung erfolgen. Ersatzimpedanzen addieren sich daher nach denselben Regeln wie Ersatzwiderstände (Satz 9.4), nur mit komplexen $\underline Z$ statt reellen $R$.

<a id="algorithmen-22"></a>
## Algorithmen

**Lösungsstrategie für Wechselstromkreise (komplexe Rechnung)**
- **Motivation:** Direkte Lösung der Differentialgleichungen für RLC-Netzwerke ist mühsam; komplexe Impedanzen reduzieren das Problem auf simple algebraische (Ohm'sche) Gleichungen.
- **Pseudocode:**
```
EINGABE: RLC-Netzwerk, Anregungsfrequenz ω
1. Ersetze jedes Bauelement durch seine komplexe Impedanz:
   R → R,  C → 1/(iωC),  L → iωL
2. Wende Kirchhoff'sche Regeln / Ersatzimpedanz-Formeln
   (Reihe: Z_ges = ΣZ_i; Parallel: 1/Z_ges = Σ1/Z_i) an,
   GENAU WIE bei Gleichstromwiderständen (Satz 14.3)
3. Berechne gesuchte komplexe Größe (I, U, Z)
4. Extrahiere Betrag (Amplitude) und Phase:
   Amplitude = |Z|,  Phasenwinkel φ = arg(Z)
5. Rücktransformation in Zeitbereich falls nötig:
   u(t) = Re{U_komplex * e^{iωt}} = |U| cos(ωt + φ)
AUSGABE: Amplitude, Phase, ggf. Zeitverlauf
```
- **Korrektheitsidee:** Direkte Konsequenz aus Sätzen 14.1–14.3; die Linearität aller beteiligten Gleichungen erlaubt das Rechnen mit komplexen Größen und Realteilbildung erst am Ende.
- **Typische Fehler:** Betrag und Realteil einer komplexen Größe verwechselt; Phasenwinkel-Vorzeichen falsch (kapazitiv vs. induktiv).

<a id="beispiele-32"></a>
## Beispiele

**Beispiel 1 (leicht):** Ein Kondensator $C=1\,\mu\text{F}$ bei $\omega=1000\,\text{rad/s}$. Berechne $|Z_C|$.
*Lösung:* $|Z_C|=1/(\omega C)=1/(1000\cdot10^{-6})=1000\,\Omega$.

**Beispiel 2 (mittel):** Reihenschaltung $R=100\,\Omega$, $L=0{,}1\,\text{H}$ bei $\omega=1000\,\text{rad/s}$. Berechne $|Z|$ und $\varphi$.
*Lösung:* $X_L=\omega L=100\,\Omega$. $|Z|=\sqrt{R^2+X_L^2}=\sqrt{100^2+100^2}\approx141{,}4\,\Omega$. $\varphi=\arctan(X_L/R)=45°$ (Strom eilt Spannung um $45°$ nach).

**Beispiel 3 (mittel):** RLC-Serienschwingkreis mit $L=1\,\text{mH}$, $C=1\,\mu\text{F}$. Berechne die Resonanzfrequenz $\omega_0$.
*Lösung:* $\omega_0=1/\sqrt{LC}=1/\sqrt{10^{-3}\cdot10^{-6}}\approx3{,}16\cdot10^4\,\text{rad/s}$.

**Beispiel 4 (schwer):** Zeige, dass bei Resonanz ($\omega=\omega_0$) im RLC-Serienkreis die Spannungen an $L$ und $C$ jeweils um den Faktor $\omega_0L/R$ (bzw. $1/(\omega_0CR)$, was bei Resonanz gleich ist — "Güte" $Q$) größer sein können als die angelegte Gesamtspannung.
*Lösung:* Bei Resonanz gilt $|Z|=R$ (da $X_L=X_C$ sich in der Summe $i(X_L-X_C)$ aufheben), also $I=U/R$. Die Spannung an der Spule: $U_L=I\cdot X_L = (U/R)\cdot\omega_0L$. Für $R$ klein (schwache Dämpfung) kann $U_L\gg U$ werden — ein auf den ersten Blick paradoxes, aber korrektes Resultat (Spannungsüberhöhung im Reihenschwingkreis), da sich $U_L$ und $U_C$ zu jedem Zeitpunkt gegenseitig größtenteils aufheben (Phasenverschiebung von $180°$ zueinander) und nur die Differenz mit der äußeren Spannung übereinstimmen muss.

<a id="gegenbeispiele-32"></a>
## Gegenbeispiele

- Die einfachen Ersatzimpedanz-Regeln (Reihe/Parallel wie bei Gleichstromwiderständen) gelten **nur**, solange man konsequent mit *komplexen* Größen rechnet — eine direkte Addition der *Beträge* $|Z_i|$ ist bei gemischten R-L-C-Netzwerken **falsch** (nur bei reinen Reihen-/Parallelschaltungen *gleichartiger* Elemente ohne Phasenverschiebung zulässig).
- Bei $\omega=0$ (Gleichstrom) wird $Z_C\to\infty$ (Kondensator sperrt vollständig) und $Z_L\to0$ (Spule ist ein Kurzschluss) — Grenzfälle, die die Ergebnisse aus Kapitel 9 (reiner Gleichstromkreis) korrekt reproduzieren müssen; guter Plausibilitätscheck.

<a id="typische-klausuraufgaben-33"></a>
## Typische Klausuraufgaben

- Impedanzberechnung für RLC-Netzwerke (Reihe, Parallel, gemischt) — Strategie: siehe Algorithmus, konsequent komplex rechnen.
- Resonanzfrequenz-Berechnung und Diskussion des Verhaltens bei/unter/über Resonanz.
- Phasenverschiebung zwischen Strom und Spannung bestimmen und interpretieren (kapazitiv/induktiv/rein ohmsch).
- Grenzfallanalyse ($\omega\to0$, $\omega\to\infty$) als Plausibilitätscheck.

<a id="typische-fehler-33"></a>
## Typische Fehler

1. Beträge der Einzelimpedanzen werden direkt addiert statt komplex (führt bei gemischten RLC-Netzwerken zu falschen Ergebnissen).
2. Vorzeichen von $X_L-X_C$ im Phasenwinkel vertauscht (kapazitiv vs. induktiv verwechselt).
3. Resonanzformel $\omega_0=1/\sqrt{LC}$ mit der Zeitkonstante $\tau=L/R$ bzw. $\tau=RC$ aus Kapitel 13/9 verwechselt — unterschiedliche physikalische Bedeutung!
4. Rücktransformation in den Zeitbereich vergessen, wenn nach $u(t)$ statt nach der komplexen Amplitude gefragt ist.

<a id="verbindungen-34"></a>
## Verbindungen

- Direkte Fortsetzung von Kapitel 9 (Gleichstromkreise) und Kapitel 13 (Selbstinduktion) — komplexe Wechselstromrechnung verallgemeinert beide.
- Grenzfall $\omega\to0$ reproduziert Kapitel 9; die $L$-Impedanz baut direkt auf Satz 13.2 auf.
- Resonanzphänomene sind konzeptuell verwandt mit mechanischen Resonanzphänomenen (erzwungene Schwingung, hier vorausgesetzt, aber nicht Teil dieses Skripts).
- Motiviert Kapitel 15: ein oszillierender Strom (Wechselstrom) in einer Antenne ist die Quelle elektromagnetischer Wellen.

<a id="zusammenfassung-22"></a>
## Zusammenfassung

- Wechselgrößen werden komplex dargestellt: $u(t)=\operatorname{Re}\{\hat Ue^{i\omega t}\}$.
- Impedanzen: $Z_R=R$, $Z_C=1/(i\omega C)$, $Z_L=i\omega L$.
- Kirchhoff'sche Regeln und Ersatzimpedanz-Formeln gelten unverändert (formal identisch zu Gleichstrom, aber komplex).
- Resonanz im RLC-Serienkreis bei $\omega_0=1/\sqrt{LC}$: minimale Impedanz, möglicherweise starke Spannungsüberhöhung an $L$/$C$.

---

<a id="kapitel-15-elektromagnetische-wellen"></a>
# Kapitel 15: Elektromagnetische Wellen

<a id="motivation-35"></a>
## Motivation

Die vier bisher gefundenen Gesetze (Gauß elektrisch, Gauß magnetisch, Faraday, Ampère) beschrieben zunächst stationäre oder quasistationäre Situationen. Maxwell erkannte 1861–1865 eine fehlende Symmetrie: Ein sich änderndes $\vec B$-Feld erzeugt ein $\vec E$-Feld (Faraday, Kapitel 13) — sollte nicht auch ein sich änderndes $\vec E$-Feld ein $\vec B$-Feld erzeugen? Diese von Maxwell hinzugefügte Korrektur (**Verschiebungsstrom**) macht die Gleichungen symmetrisch — und sagt als Konsequenz selbstständig ausbreitende elektromagnetische Wellen voraus, deren Geschwindigkeit exakt mit der (damals unabhängig gemessenen) Lichtgeschwindigkeit übereinstimmt. Dies war einer der größten Triumphe der theoretischen Physik: Licht wurde als elektromagnetisches Phänomen identifiziert, ohne dass dies ursprünglich das Ziel der Theorie war.

<a id="intuition-35"></a>
## Intuition

Stell dir ein oszillierendes $\vec E$-Feld vor, das (nach der Maxwell'schen Ergänzung) ein oszillierendes $\vec B$-Feld erzeugt, welches wiederum (nach Faraday) ein oszillierendes $\vec E$-Feld erzeugt — ein sich selbst tragender Prozess, der sich wie eine Welle durch den Raum ausbreitet, *ohne* dass ein Medium nötig ist (im Gegensatz zu Schallwellen, die Materie brauchen). Man kann es sich wie zwei Personen vorstellen, die sich gegenseitig anstoßen und dadurch gemeinsam vorwärts "rollen", ganz ohne festen Boden unter den Füßen.

<a id="formale-definitionen-35"></a>
## Formale Definitionen

**Definition 15.1 (Verschiebungsstrom).**
$$\vec j_{Vers} := \varepsilon_0\frac{\partial\vec E}{\partial t}.$$

**Definition 15.2 (Vollständige Maxwell-Gleichungen im Vakuum).**

| Nr. | Integralform | Differentialform | Name |
|---|---|---|---|
| I | $\oint\vec E\cdot d\vec A=Q_{innen}/\varepsilon_0$ | $\operatorname{div}\vec E=\rho/\varepsilon_0$ | Gauß (elektrisch) |
| II | $\oint\vec B\cdot d\vec A=0$ | $\operatorname{div}\vec B=0$ | Gauß (magnetisch) |
| III | $\oint\vec E\cdot d\vec s=-\dfrac{d\Phi_B}{dt}$ | $\operatorname{rot}\vec E=-\dfrac{\partial\vec B}{\partial t}$ | Faraday |
| IV | $\oint\vec B\cdot d\vec s=\mu_0I+\mu_0\varepsilon_0\dfrac{d\Phi_E}{dt}$ | $\operatorname{rot}\vec B=\mu_0\vec j+\mu_0\varepsilon_0\dfrac{\partial\vec E}{\partial t}$ | Ampère-Maxwell |

<a id="eigenschaften-31"></a>
## Eigenschaften

| Eigenschaft | Aussage |
|---|---|
| $\vec E$, $\vec B$, Ausbreitungsrichtung | stehen paarweise senkrecht aufeinander (transversale Welle) |
| Ausbreitungsgeschwindigkeit im Vakuum | $c=1/\sqrt{\mu_0\varepsilon_0}\approx3\cdot10^8\,\text{m/s}$ |
| Energiefluss | Poynting-Vektor $\vec S=\vec E\times\vec H$ |
| Erzeugung | beschleunigte Ladungen (z. B. oszillierender Dipol, "Hertz'scher Dipol") |

<a id="sätze-31"></a>
## Sätze

<a id="satz-151-wellengleichung-aus-den-maxwell-gleichungen"></a>
### Satz 15.1 (Wellengleichung aus den Maxwell-Gleichungen)

**Aussage:** Im ladungs- und stromfreien Vakuum erfüllt jede kartesische Komponente von $\vec E$ und $\vec B$ die Wellengleichung
$$\Delta\vec E = \mu_0\varepsilon_0\frac{\partial^2\vec E}{\partial t^2}, \qquad \Delta\vec B=\mu_0\varepsilon_0\frac{\partial^2\vec B}{\partial t^2}.$$

**Beweis (Beweisstil: direkte Kombination der Maxwell-Gleichungen III und IV, Vektoridentität).**

Im Vakuum ohne freie Ladungen/Ströme ($\rho=0,\vec j=0$) lauten III und IV:
$$\operatorname{rot}\vec E = -\frac{\partial\vec B}{\partial t}, \qquad \operatorname{rot}\vec B = \mu_0\varepsilon_0\frac{\partial\vec E}{\partial t}.$$
Wende $\operatorname{rot}$ auf die erste Gleichung an:
$$\operatorname{rot}(\operatorname{rot}\vec E) = -\frac{\partial}{\partial t}(\operatorname{rot}\vec B) = -\mu_0\varepsilon_0\frac{\partial^2\vec E}{\partial t^2}$$
(im letzten Schritt wurde die zweite Gleichung eingesetzt). Mit der Vektoridentität $\operatorname{rot}(\operatorname{rot}\vec E) = \nabla(\operatorname{div}\vec E)-\Delta\vec E$ und $\operatorname{div}\vec E=0$ (Maxwell I, ladungsfrei):
$$-\Delta\vec E = -\mu_0\varepsilon_0\frac{\partial^2\vec E}{\partial t^2} \;\Longrightarrow\; \Delta\vec E = \mu_0\varepsilon_0\frac{\partial^2\vec E}{\partial t^2}.$$
Analog für $\vec B$ (Rollen von $\vec E$ und $\vec B$ vertauscht). $\blacksquare$

**Bedeutung:** Vergleich mit der allgemeinen 3D-Wellengleichung $\Delta\psi = \dfrac{1}{v^2}\dfrac{\partial^2\psi}{\partial t^2}$ zeigt sofort
$$v = c = \frac{1}{\sqrt{\mu_0\varepsilon_0}}.$$
Einsetzen der bekannten Werte für $\mu_0,\varepsilon_0$ liefert $c\approx2{,}998\cdot10^8\,\text{m/s}$ — exakt die (unabhängig gemessene) Lichtgeschwindigkeit. Diese Übereinstimmung war Maxwells zentrales Argument, dass **Licht eine elektromagnetische Welle ist**.

<a id="satz-152-ebene-harmonische-welle-struktureigenschaften"></a>
### Satz 15.2 (Ebene, harmonische Welle — Struktureigenschaften)

**Aussage:** Für eine ebene Welle $\vec E(\vec r,t) = \vec E_0\cos(\vec k\cdot\vec r-\omega t)$, die die Wellengleichung löst, gilt notwendig $\omega=ck$ (Dispersionsrelation), sowie $\vec E\perp\vec k$, $\vec B\perp\vec k$, $\vec E\perp\vec B$, mit $|\vec B|=|\vec E|/c$.

**Beweisidee (Beweisstil: Einsetzen des Lösungsansatzes in die Maxwell-Gleichungen).**
Einsetzen des ebenen-Wellen-Ansatzes in $\operatorname{div}\vec E=0$ liefert $\vec k\cdot\vec E_0=0$, also $\vec E\perp\vec k$ (Transversalität). Einsetzen in die Wellengleichung (Satz 15.1) liefert direkt $k^2=\mu_0\varepsilon_0\omega^2=\omega^2/c^2$, also $\omega=ck$. Einsetzen in $\operatorname{rot}\vec E=-\partial\vec B/\partial t$ liefert die Kopplung zwischen $\vec E_0$ und $\vec B_0$ inklusive der senkrechten Orientierung zueinander und dem Betragsverhältnis $c$.

<a id="algorithmen-23"></a>
## Algorithmen

Kein klassischer Algorithmus; stattdessen eine **Checkliste zur Analyse elektromagnetischer Wellen**:
```
EINGABE: gegebene Welle (E0, k, ω oder Frequenz f, Ausbreitungsmedium)
1. Prüfe Dispersionsrelation: ω = ck (Vakuum) bzw. ω = v_Phase * k (Medium)
2. Bestimme B aus E über |B| = |E|/c, Richtung senkrecht zu E und k
   (Rechte-Hand-Regel: E × B zeigt in Ausbreitungsrichtung)
3. Für Energiefragen: Poynting-Vektor S = E × H, zeitgemittelt
   <S> = ½ E0 B0 / μ0  (analog zur mittleren Leistung bei Wechselstrom!)
AUSGABE: vollständige Wellenbeschreibung
```

<a id="beispiele-33"></a>
## Beispiele

**Beispiel 1 (leicht):** Berechne $c$ aus $\mu_0=4\pi\cdot10^{-7}\,\text{Tm/A}$, $\varepsilon_0=8{,}854\cdot10^{-12}\,\text{C}^2/(\text{Nm}^2)$.
*Lösung:* $c=1/\sqrt{\mu_0\varepsilon_0} = 1/\sqrt{4\pi\cdot10^{-7}\cdot8{,}854\cdot10^{-12}}\approx2{,}998\cdot10^8\,\text{m/s}$.

**Beispiel 2 (leicht):** Eine EM-Welle hat $E_0=100\,\text{V/m}$. Berechne $B_0$.
*Lösung:* $B_0=E_0/c=100/(3\cdot10^8)\approx3{,}33\cdot10^{-7}\,\text{T}$.

**Beispiel 3 (mittel):** Bestimme die Wellenlänge einer EM-Welle mit $f=100\,\text{MHz}$ (UKW-Rundfunk).
*Lösung:* $\lambda=c/f = 3\cdot10^8/10^8=3\,\text{m}$.

**Beispiel 4 (schwer):** Zeige, dass die Dispersionsrelation $\omega=ck$ tatsächlich aus dem Einsetzen des ebenen-Wellen-Ansatzes in die Wellengleichung folgt (Satz 15.2, Rechendetail).
*Lösung:* Mit $\vec E=\vec E_0\cos(\vec k\cdot\vec r-\omega t)$: $\Delta\vec E = -k^2\vec E$ (zweifache Ortsableitung bringt Faktor $-k^2$), $\partial^2\vec E/\partial t^2=-\omega^2\vec E$ (zweifache Zeitableitung bringt Faktor $-\omega^2$). Einsetzen in $\Delta\vec E=\mu_0\varepsilon_0\partial^2\vec E/\partial t^2$: $-k^2\vec E = -\mu_0\varepsilon_0\omega^2\vec E \Rightarrow k^2=\mu_0\varepsilon_0\omega^2=\omega^2/c^2 \Rightarrow \omega=ck$ (positive Wurzel für Ausbreitung in $+\vec k$-Richtung).

<a id="gegenbeispiele-33"></a>
## Gegenbeispiele

- Eine **longitudinale** elektromagnetische Welle (Feld schwingt parallel zur Ausbreitungsrichtung) existiert im Vakuum **nicht** — die Transversalitätsbedingung ($\vec k\cdot\vec E_0=0$) folgt zwingend aus $\operatorname{div}\vec E=0$ (Maxwell I im ladungsfreien Raum).
- In einem **Medium** mit Ladungen/Strömen (z. B. einem Leiter) gilt die einfache Wellengleichung (Satz 15.1) **nicht** unverändert — dort muss der Ohm'sche Strom $\vec j=\sigma\vec E$ (Kapitel 9) mitberücksichtigt werden, was zu Dämpfung (Skin-Effekt) statt ungedämpfter Ausbreitung führt.

<a id="typische-klausuraufgaben-34"></a>
## Typische Klausuraufgaben

- Berechnung von $c$, $\lambda$, $f$, $B_0$ aus gegebenen Wellenparametern — meist direkte Einsetzaufgaben.
- Herleitung/Nachvollziehen der Wellengleichung aus den Maxwell-Gleichungen (Satz 15.1) — Verständnisaufgabe zur Struktur der Theorie.
- Qualitative Fragen zur Bedeutung des Verschiebungsstroms (warum musste Maxwell die Ampère-Gleichung ergänzen?).
- Polarisation und Orientierung von $\vec E$, $\vec B$, $\vec k$ zueinander.

<a id="typische-fehler-34"></a>
## Typische Fehler

1. $\vec E$, $\vec B$ und Ausbreitungsrichtung werden nicht als senkrecht zueinander erkannt (Transversalität vergessen).
2. Verwechslung von $\omega$ (Kreisfrequenz) und $f$ (Frequenz): $\omega=2\pi f$.
3. Der Verschiebungsstrom wird mit einem "echten" Ladungsstrom verwechselt — er beschreibt lediglich die Wirkung eines sich ändernden $E$-Feldes, es fließen dabei keine Ladungen.

<a id="verbindungen-35"></a>
## Verbindungen

- Schließt den gesamten Elektromagnetismus-Teil ab: Alle vier Maxwell-Gleichungen (Kapitel 7, 12, 13 + hier ergänzter Verschiebungsstrom) werden hier erstmals vollständig zusammengeführt.
- Der Hertz'sche Dipol (oszillierender elektrischer Dipol, Kapitel 6) als Wellenquelle verbindet dieses Kapitel zurück zur Elektrostatik.
- Die Energiebetrachtung (Poynting-Vektor) baut auf den Energiedichteformeln aus Kapitel 7 ($w_{el}$) und (analog) Kapitel 12 ($w_{mag}$, hier nicht explizit hergeleitet, aber strukturell analog) auf.
- Optik, Radiowellentechnik und die gesamte moderne Kommunikationstechnik bauen unmittelbar auf diesem Kapitel auf (außerhalb dieser Vorlesung vertieft).

<a id="zusammenfassung-23"></a>
## Zusammenfassung

- Maxwell ergänzte den Verschiebungsstrom $\varepsilon_0\partial\vec E/\partial t$, um die Ampère-Gleichung zu symmetrisieren.
- Die vier vollständigen Maxwell-Gleichungen (Def. 15.2) implizieren im Vakuum die Wellengleichung für $\vec E$ und $\vec B$.
- Ausbreitungsgeschwindigkeit $c=1/\sqrt{\mu_0\varepsilon_0}$ — identisch mit der Lichtgeschwindigkeit, was Licht als EM-Welle identifiziert.
- EM-Wellen sind transversal: $\vec E\perp\vec B\perp\vec k$, mit $|\vec B|=|\vec E|/c$.
- Energietransport über den Poynting-Vektor $\vec S=\vec E\times\vec H$.

---

---

<a id="kapitel-16-exkurs-lorentz-transformation-und-spezielle-relativitätstheorie"></a>
# Kapitel 16: Exkurs — Lorentz-Transformation und Spezielle Relativitätstheorie

> **Hinweis:** Dieses Kapitel ist bewusst rudimentär gehalten (entsprechend dem tatsächlichen Umfang, der in der Vorlesung behandelt wurde) und folgt nicht der vollen Kapitelstruktur der übrigen Kapitel. Es enthält nur die Kernformeln und die zwei zugehörigen Standardbeispiele.

<a id="motivation-36"></a>
## Motivation

Kapitel 15 zeigte: Die Maxwell-Gleichungen sagen eine Ausbreitungsgeschwindigkeit $c$ für elektromagnetische Wellen voraus — und zwar **denselben Wert $c$, unabhängig vom Bezugssystem** (die Herleitung von Satz 15.1 benutzt an keiner Stelle die Geschwindigkeit eines Beobachters). Das widerspricht der klassischen (Galilei'schen) Vorstellung, nach der sich Geschwindigkeiten einfach addieren ($u'=u-v$). Einstein löste diesen Widerspruch 1905, indem er die Konstanz von $c$ für alle Beobachter als Postulat akzeptierte und stattdessen Raum und Zeit selbst beobachterabhängig machte.

<a id="grundidee"></a>
## Grundidee

Zwei Inertialsysteme $S$ (ruhend) und $S'$ (bewegt sich mit Geschwindigkeit $v$ entlang der $x$-Achse relativ zu $S$) sind durch die **Lorentz-Transformation** verknüpft — nicht mehr durch die einfache Galilei-Transformation $x'=x-vt,\ t'=t$.

<a id="formeln"></a>
## Formeln

**Lorentz-Faktor:**
$$\gamma := \frac{1}{\sqrt{1-v^2/c^2}} \geq 1.$$

**Lorentz-Transformation** (Boost entlang $x$):
$$x' = \gamma(x-vt), \qquad t' = \gamma\left(t-\frac{vx}{c^2}\right), \qquad y'=y,\quad z'=z.$$

**Zeitdilatation:** Eine Uhr, die in ihrem eigenen Ruhesystem die **Eigenzeit** $\tau$ anzeigt, wird von einem relativ dazu bewegten Beobachter als "langsamer gehend" gemessen:
$$\Delta t_{Beobachter} = \gamma\,\Delta\tau \quad(\geq \Delta\tau).$$

**Längenkontraktion** (auch: **Lorentzkontraktion**): Ein Objekt der **Eigenlänge** $L$ (gemessen im eigenen Ruhesystem) erscheint einem relativ dazu bewegten Beobachter verkürzt:
$$L' = \frac{L}{\gamma} \quad(\leq L).$$

**Invariantes Raumzeit-Intervall** (folgt direkt aus der Konstanz von $c$, siehe Herleitung unten):
$$s^2 := (ct)^2-x^2 = (ct')^2-x'^2 = \text{const} \quad\text{(gleich in jedem Inertialsystem)}.$$

**Kurze Herleitung der Invarianz von $s^2$:** Einsetzen der Lorentz-Transformation liefert
$$(ct')^2-x'^2 = c^2\gamma^2\left(t-\frac{vx}{c^2}\right)^2-\gamma^2(x-vt)^2 = \gamma^2\left[c^2t^2-2vxt+\frac{v^2x^2}{c^2}-x^2+2vxt-v^2t^2\right]$$
$$= \gamma^2\left[c^2t^2\left(1-\frac{v^2}{c^2}\right)-x^2\left(1-\frac{v^2}{c^2}\right)\right] = \gamma^2\left(1-\frac{v^2}{c^2}\right)(c^2t^2-x^2) = c^2t^2-x^2,$$
da $\gamma^2(1-v^2/c^2)=1$ per Definition von $\gamma$. $\blacksquare$

<a id="beispiel-1-zwillingsparadoxon-qualitativ"></a>
## Beispiel 1: Zwillingsparadoxon (qualitativ)

Ein Zwilling bleibt auf der Erde, der andere fliegt mit hoher Geschwindigkeit $v$ zu einem fernen Stern und zurück. Aus Sicht des ruhenden Zwillings vergeht für den reisenden Zwilling wegen Zeitdilatation weniger Eigenzeit ($\Delta\tau = \Delta t_{Erde}/\gamma$) — bei der Rückkehr ist der reisende Zwilling jünger. Das "Paradoxon" (jeder der beiden könnte sich als "ruhend" und den anderen als "bewegt" ansehen, symmetrisch) löst sich dadurch auf, dass **nur** der reisende Zwilling beim Umkehren beschleunigt und damit das Inertialsystem wechselt — die Situation ist nicht symmetrisch, es gibt ein eindeutiges Ergebnis.

<a id="beispiel-2-myonenparadoxon-quantitativ"></a>
## Beispiel 2: Myonenparadoxon (quantitativ)

Kosmische Myonen entstehen hoch in der Atmosphäre und haben im eigenen Ruhesystem eine mittlere Lebensdauer von nur $\tau\approx2{,}2\,\mu\text{s}$. Mit Lichtgeschwindigkeit würden sie ohne Relativitätseffekte im Mittel nur $c\tau\approx660\,\text{m}$ zurücklegen — viel zu wenig, um die Erdoberfläche (Flugstrecke $\sim10\,\text{km}$) zu erreichen. Dennoch werden sie am Boden nachgewiesen. Zwei äquivalente Erklärungen:

- **Aus Sicht des Beobachters auf der Erde:** Die Myonen bewegen sich schnell ($v\approx0{,}998c$, $\gamma\approx16{-}20$ je nach Beispielwerten), ihre Lebensdauer erscheint durch Zeitdilatation verlängert: $\Delta t_{Erde}=\gamma\tau$. Die zurückgelegte Strecke ist dann $\beta c\cdot\gamma\tau = O(10\,\text{km})$ — ausreichend, um die Erdoberfläche zu erreichen.
- **Aus Sicht des Myons (Eigensystem):** Das Myon "lebt" nur seine Eigenzeit $\tau$, aber die Atmosphäre rast ihm mit $v$ entgegen und ist durch Längenkontraktion auf $L'=L/\gamma \approx 200\,\text{m}$ (statt $10\,\text{km}$) verkürzt — auch aus dieser Perspektive kommt es problemlos am Boden an.

**Beide Sichtweisen sind physikalisch gleichwertig** und liefern dasselbe (beobachtbare) Ergebnis — ein Musterbeispiel dafür, dass Zeitdilatation und Längenkontraktion zwei Seiten derselben Medaille sind, je nachdem, aus welchem Bezugssystem man das Ereignis betrachtet.

<a id="zusammenfassung-24"></a>
## Zusammenfassung

- Lorentz-Transformation: $x'=\gamma(x-vt)$, $t'=\gamma(t-vx/c^2)$, mit $\gamma=1/\sqrt{1-v^2/c^2}$.
- Zeitdilatation: bewegte Uhren gehen langsamer, $\Delta t=\gamma\,\Delta\tau$.
- Längenkontraktion: bewegte Objekte erscheinen verkürzt, $L'=L/\gamma$.
- Zwillingsparadoxon: Asymmetrie durch Beschleunigung des reisenden Zwillings löst das scheinbare Paradoxon auf.
- Myonenparadoxon: Zeitdilatation (Beobachtersicht) und Längenkontraktion (Myon-Eigensicht) erklären dasselbe Phänomen äquivalent.

---

*Ende Teil II und damit des vollständigen Skripts (Kapitel 1–16). Zusammen mit Teil I deckt dieses Skript den gesamten rekonstruierten Vorlesungsstoff ab.*



---
