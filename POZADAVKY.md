# Katalog požadavků softwarového projektu (IS DobaKeřová)

Tento dokument obsahuje seznam funkčních a nefunkčních požadavků pro informační systém komunitních zahrad **DobaKeřová**. Požadavky detailně definují, co systém dělá a jaké jsou jeho technické a provozní vlastnosti.

---

## 1. Funkční požadavky
Funkční požadavky popisují konkrétní funkce systému a akce, které mohou jednotliví uživatelé (podle svých rolí) provádět.

### 1.1 Správa uživatelů a rolí
* **F-01: Registrace a přihlášení:** Systém umožní uživatelům vytvořit si účet (jméno, e-mail, heslo) a bezpečně se přihlásit.
* **F-02: Správa rolí:** Systém bude rozlišovat 3 typy uživatelů: *Zahrádkář* (běžný člen), *Správce* (organizátor zahrady) a *Pokladník* (finance).
* **F-03: Schvalování členů:** Nově registrovaný uživatel se stane aktivním členem až poté, co jeho žádost v systému schválí *Správce*.

### 1.2 Evidence a pronájem záhonů
* **F-04: Katalog záhonů:** Systém zobrazí přehled (seznam/mapu) všech záhonů s informacemi o jejich velikosti, typu půdy, ceně a aktuálním stavu (volný/obsazený).
* **F-05: Rezervace a platba:** *Zahrádkář* si může zažádat o pronájem volného záhonu na sezónu. *Pokladník* v systému zaznamená přijetí platby, čímž se záhon oficiálně označí jako pronajatý.
* **F-06: Historie pěstování:** Systém ukládá data o tom, co se na kterém záhonu v uplynulých letech pěstovalo.

### 1.3 Brigády a bodový systém (Kredity)
* **F-07: Vypsání brigády:** *Správce* může vytvořit novou komunitní akci (název, datum, čas, popis práce a maximální počet lidí).
* **F-08: Přihlašování na akce:** *Zahrádkář* se může na brigádu přihlásit nebo se z ní odhlásit.
* **F-09: Připsání kreditů:** Po skončení brigády *Správce* v systému potvrdí reálnou docházku a systém automaticky připíše účastníkům body (kredity) na jejich účet.

### 1.4 Rezervace nářadí a chytré funkce
* **F-10: Půjčovna nářadí:** Systém obsahuje kalendář pro rezervaci sdíleného komunitního vybavení (např. sekačka, drtič větví).
* **F-11: Hlídání konfliktů:** Systém nedovolí rezervovat stejný kus nářadí dvěma uživatelům ve stejný čas.
* **F-12: Agronomické doporučení:** Na základě historie záhonu (F-06) systém zobrazí uživateli jednoduché textové varování, pokud se chystá zasadit stejnou plodinu více let po sobě (upozornění na vyčerpání půdy).

### 1.5 Komunitní bazar
* **F-13: Vytvoření inzerátu:** *Zahrádkář* může do vnitro-komunitního bazaru vložit nabídku nebo poptávku (např. přebytky sazenic rajčat, semínka) včetně popisu a množství.
* **F-14: Správa inzerátu:** Autor může inzerát označit za vyřízený nebo ho smazat.

---

## 2. Nefunkční požadavky
Nefunkční požadavky určují kvalitu, bezpečnost, technologické omezení a uživatelskou přívětivost systému.

### 2.1 Bezpečnost a data
* **N-01: Šifrování hesel:** Uživatelská hesla musí být v databázi bezpečně zašifrována pomocí moderních algoritmů.
* **N-02: Ochrana soukromí:** Kontaktní údaje uživatelů (telefon, e-mail) uvidí pouze *Správce* a *Pokladník*, běžným uživatelům zůstanou skryté.

### 2.2 Dostupnost a výkon
* **N-03: Responzivita (Mobilní zobrazení):** Webové rozhraní systému musí být plně responzivní, aby ho zahrádkáři mohli pohodlně ovládat na mobilech přímo na zahradě.
* **N-04: Rychlost odezvy:** Běžné operace (načtení seznamu záhonů, odeslání formuláře) nesmí trvat déle než 2 sekundy při standardním internetovém připojení.

### 2.3 Provozní a technologické požadavky
* **N-05: Webová platforma:** Systém bude navržen jako webová aplikace běžící v běžných internetových prohlížečích (Chrome, Firefox, Safari) bez nutnosti instalace.
* **N-06: Jazyk rozhraní:** Celé uživatelské prostředí systému bude v českém jazyce.