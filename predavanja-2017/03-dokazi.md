# Kaj je dokaz?

* Dokaz je utemeljitev izjave.

* Dokaz je zgrajen po točno določenih *pravilih sklepanja*.

* Pravila sklepanja in dokaze lahko podamo povsem formalno in jih tudi implementiramo na
  računalniku. Tako dobimo zelo natančen in zanesljiv sistem za preverjanje dokazov.

* V praksi ljudje ne pišejo posameznih korakov v dokazu, ampak izpuščajo lažje kose dokaza.
  Pogosto podajo samo glavno idejo, iz katere lahko izkušeni matematik sam rekonstruira dokaz.

* Mi bomo vadili podrobno pisanje dokazov. Pri ostalih predmetih boste videli "žive dokaze",
  ki imajo manj podrobnosti in so zapisani manj formalno. A vsi matematični dokazi, če so
  pravilni, se dajo zapisati na način, kot ga bomo predstavili mi.

* Pravila sklepanja so kot pravila igre. Ne povedo, kako dobro igrati, samo kaj je
  dovoljeno. Povedali bomo tudi nekaj navodil, kako izjavo dokažemo. A kot pri vsaki
  igri velja, da vaja dela mojstra.

# Kako pišemo dokaze

Dokaz ima vgnezdeno strukturo: sestoji iz pod-dokazov, ki sestojijo iz nadaljnih
pod-dokazov itn., ki se zaključijo z osnovnimi dejstvi. Vsi ti kosi so s pomočjo pravil
sklepanja zloženi v dokazno "drevo".

Ko pišemo dokaz, moramo v vsakem trenutku vedeti:

1. Kaj trenutno dokazujemo.
2. Katere spremenljivke in predpostavke imamo trenutno na voljo. Temu pravimo *kontekst*.

Ko napravimo korak v dokazu, mora biti utemeljen z enim od pravil sklepanja. Dokaz je
popoln, ko smo utemeljili vse pod-dokaze, ki ga sestavljajo.

#### Primer

Izjava: (p ∨ q) ∧ r ⇒ (p ∧ r) ∨ (p ∧ r).

Dokaz:

Dokazujemo (p ∨ q) ∧ r ⇒ (p ∧ r) ∨ (p ∧ r).
  Predpostavimo (p ∨ q) ∧ r.                   (1)
  Dokazujemo (p ∧ r) ∨ (p ∧ r).
     Velja p ∨ q zaradi (1).                   (2)
     Velja r zaradi (1).                       (3)
     Obravnavamo primera p, q zaradi (2):
         1. Predpostavimo p:                        (4)
             Dokazujemo (p ∧ r) ∨ (p ∧ r)
                Dokažimo p ∧ r:
                     1.1. Dokažimo p: velja p zaradi (4)
                     1.2. Dokažimo r: velja q zaradi (3)
         2. Predpostavimo q:                        (5)
             Dokazujemo (p ∧ r) ∨ (q ∧ r)
                Dokažimo q ∧ r:
                     1.1. Dokažimo q: velja q zaradi (5)
                     1.2. Dokažimo r: velja r zaradi (3)
Konec dokaza.

## Pravila sklepanja

Pravila sklepanja delimo na dve vrsti:

* **pravila vpeljave** izjavo, ki jo želimo dokazati, predelajo na druge, bolj preproste izjave
* **pravila uporabe** iz že znanih dejstev in predpostavk, ki jih imamo na voljo, izpeljemo nova dejstva

Poleg tega poznamo še pravila o zamenjavi:

* **zamenjava enakih izrazov**: izraz lahko vedno zamenjamo z njim enakim
* **zamenjava ekvivalentnih izjav**: izjavo vedno lahko zamenjamo z njej ekvivalentno

Danes bomo govorili o pravilih vpeljave in uporabe.

### Pravila vpeljave

Vsak veznik in kvantifikator ima svoja pravila.

### Pravila uporabe
