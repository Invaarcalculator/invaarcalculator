# HANDOFF v3.0.134 — GitHub-repository en GitHub Pages-hosting

**Datum**: 14 mei 2026
**Vorige versie**: v3.0.133 (taal-puristische overhaul Verantwoording-tekst)
**Deze versie**: v3.0.134 (broncode publiek via GitHub + hosting-melding in Privacy-modal)

---

## 1. Wijzigingen

### 1.1 Privacy-modal: nieuwe sectie "Hosting via GitHub Pages"
Tussen de bestaande secties "Geen cookies, geen tracking" en "Voor de inhoudelijke verantwoording" is een nieuwe sectie toegevoegd:

> **HOSTING VIA GITHUB PAGES**
> Deze tool wordt gehost via GitHub Pages (een dienst van GitHub, Inc., onderdeel van Microsoft). Bij het ophalen van de pagina door uw browser legt GitHub standaard HTTP-server-gegevens vast — IP-adres, gebruikte browser, tijdstip van bezoek, opgevraagde bestanden — voor beveiligings- en infrastructuurdoeleinden. Dit gebeurt buiten invloed van de auteur. Voor het privacy-beleid van GitHub: https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement.

Dit completeert de Privacy-toelichting: de eerste sectie zegt eerlijk dat geen invoer de browser verlaat (correct voor de calculator-logica), de tweede dat de tool zelf geen cookies of tracking gebruikt (correct), en de derde nieuwe sectie maakt expliciet dat de HTTP-server-laag (GitHub) wel standaard server-logging doet — buiten controle van de auteur. Daarmee is de privacy-statement volledig en eerlijk.

### 1.2 Verantwoording §2 "Hoe de tool tot stand is gekomen": GitHub-URL en hosting-melding
De zin over open-source-publicatie van broncode en modelspecificatie is uitgebreid:

> De tool is bewust open-source en transparant; de modelspecificatie en broncode zijn meegeleverd zodat onafhankelijke verificatie mogelijk is. **De broncode is publiek beschikbaar via https://github.com/Invaarcalculator/invaarcalculator.git; de tool zelf wordt gehost via GitHub Pages (zie de Privacy-link in de footer voor de implicaties daarvan).**

Cross-link naar Privacy zorgt dat een lezer die de Verantwoording leest en op de hosting-keuze stuit, direct doorgewezen wordt naar de relevante privacy-toelichting.

## 2. Technische wijzigingen

- `src/ui.app.ts` HELP_CONTENT.privacy: nieuwe HelpSection-object tussen index 1 en 2.
- `src/ui.app.ts` HELP_CONTENT.verantwoording §2 HOE: één zin uitgebreid.
- RELEASE_VERSION bumped: 3.0.133 → 3.0.134.
- Bundle: 190.6 KB (was 189.9 KB) — +0.7 KB voor de nieuwe Privacy-sectie + Verantwoording-uitbreiding.
- Build verifiëerd: 6 unieke kerntreffers ("HOSTING VIA GITHUB PAGES", "github.com/Invaarcalculator", "GitHub Pages" 2×, "GitHub, Inc.", "github-general-privacy-statement", "3.0.134") allemaal aanwezig in HTML-output.

## 3. Wat NIET in deze versie zit

- **PDF-hercompilatie (W17)**: blijft open. Geen wijzigingen in modelspecificatie zelf.
- **Engine-wijzigingen**: geen.
- **Andere helpteksten**: ongewijzigd.

## 4. Operationeel — wat dit betekent voor publicatie

Met v3.0.134 is de tool klaar voor publieke deployment via GitHub Pages:
- De Verantwoording-modal verwijst lezers naar de publieke GitHub-repository voor verificatie.
- De Privacy-modal is eerlijk over wat GitHub als hosting-partij standaard logt.
- De broncode-repository moet uiteraard daadwerkelijk publiek staan onder de gegeven URL (https://github.com/Invaarcalculator/invaarcalculator.git) op het moment dat de tool gedeployed wordt; controleer dit voor publicatie.

## 5. Open items (uit eerdere handoffs)

- W17 PDF-hercompilatie
- Tekortscenario tekst-tweak bij jaarequivalent-regel
- Cleanup onbereikbare files + CSS
- Visuele tests grafieken op echte devices
- Transitiebijdrage als DG-functie (bewust "laten zitten")
