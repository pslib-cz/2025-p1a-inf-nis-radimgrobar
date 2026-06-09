# Informační systém DobaKeřová 


Vítejte v repozitáři pro komunitní zahrádkářský informační systém **DobaKeřová** který vám usnadní život. Tento projekt byl kompletně navržen a zdokumentován v rámci školního projektu analýzy a návrhu NIS (Nového Informačního Systému)
---
## Cíl projektu

Hlavním cílem tohoto projektu bylo vypracovat kompletní analytický a architekturní návrh systému před samotným zahájením vývoje. Záměrem bylo čistě analyticky definovat byznys logiku, datové toky, uživatelské role a technologické zázemí aplikace. Součástí zadání nebylo psaní samotného zdrojového kódu ani implementace systému, ale vytvoření jednoznačné, přehledné a technicky správné blueprint dokumentace, která by sloužila jako závazný podklad pro vývojový tým.
## Rozcestník dokumentace

Pro maximální přehlednost je projekt rozdělen do samostatných logických celků. Kliknutím na níže uvedené odkazy se dostanete k příslušné části specifikace:

*  **[Koncept projektu a téma](KONCEPT.md)** – Původní záměr, představení vize komunitní zahrady a rozdělení uživatelských rolí odevzdaný k termínu 27. 5.
*  **[Katalog požadavků](POZADAVKY.md)** – Kompletně zpracovaný katalog funkčních a nefunkčních požadavků (F-01 až F-14) odevzdaný k termínu 3. 6.

---

## Analytické a architekturní UML diagramy

Níže naleznete finální grafické návrhy struktury a chování systému, které plně pokrývají zadání projektu. Všechny diagramy jsou v repozitáři uloženy ve složce `diagramy/`.

### 1. Diagram případů užití (Use Case)
Definuje hranice systému a ukazuje, jaké akce mohou jednotliví aktéři (*Zahrádkář*, *Správce*, *Pokladník*) v systému provádět. Zachycuje také byznys vztah, kde zaznamenání platby rozšiřuje (`<<extend>>`) samotnou rezervaci záhonu.
--> **[Zobrazit zdrojový diagram](diagramy/UseCase.drawio.png)**

---

### 2. Diagram tříd (Class Diagram)
Představuje statickou datovou strukturu systému, definuje jednotlivé entity (`Uzivatel`, `Zahon`, `Naradi`, etc.), jejich atributy, datové typy, metody a vzájemné multiplicity. Slouží jako přímý podklad pro tvorbu databáze.
--> **[Zobrazit zdrojový diagram](diagramy/TřídovýDiagram.drawio.png)**

---

### 3. Sekvenční diagram (Sequence Diagram)
Zachycuje dynamické chování systému v čase při klíčovém procesu **Rezervace nářadí**. Detailně vizualizuje volání metod mezi uživatelským rozhraním a backendovými objekty včetně logického bloku `alt` pro řešení kolizí termínů.
--> **[Zobrazit zdrojový diagram](diagramy/SekvenčníDiagram.drawio.png)**

---

### 4. Diagram nasazení a technologií (Deployment)
Zobrazuje fyzickou a technologickou architekturu systému rozdělenou do tří vrstev podle standardů moderních webových aplikací: *Uživatel (Frontend v prohlížeči)* $\rightarrow$ *Backend Server (Cloudová aplikační logika)* $\rightarrow$ *Databázový Server (PostgreSQL/MySQL)*.
--> **[Zobrazit zdrojový diagram](diagramy/TechnologieANasazení.drawio.png)**

---

## Závěr

Projekt je úspěšně dokončen a odevzdán v plném rozsahu k finálnímu termínu **10. 6.** Všechny milníky (Koncept, Katalog požadavků i kompletní sada 4 diagramů) byly splněny a zvládnuty. Celkově jsem s prací spokojen, doufám že se bude líbit a budu rád za jakoukoliv zpětnou vazbu. **Toď vše**.