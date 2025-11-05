# Bijdragen aan Samenspraak

Samenspraak groeit door samenwerking tussen mensen met verschillende ervaring.  
Iedereen kan bijdragen.  
Door te schrijven, te onderzoeken, te ontwerpen of te bouwen.  

Het project draait om taal en aandacht.  
Techniek ondersteunt dat, maar bepaalt het niet.  
De waarde ligt in gezamenlijke oefening in spreken en luisteren met aandacht.

---

## 1. Overzicht van routes

Iedere route heeft een eigen vorm van bijdrage.  
Ze zijn gelijkwaardig in waarde en doel.  

| Route | Doel | Werkwijze |
|--------|------|-----------|
| **A. Prompttesten** | Onderzoeken hoe het model reageert op vaste prompts | Via formulier of JSON-bestand |
| **B. Documentatie en onderzoek** | Verbeteren van toon, helderheid en neutraliteit | Via issue of pull request |
| **C. Backend (Python)** | Bouwen aan de technische basis | Via code en backend-issues |
| **D. Frontend en ontwerp** | Werken aan toegankelijkheid en ervaring | Via ontwerpvoorstellen of schetsen |
| **E. Gesprek en reflectie** | Observeren hoe taal, toon en verschil zich tonen in echte gesprekken | Via observaties of reflecties |

Elke route kan afzonderlijk of samen met anderen worden gevolgd.  


---

## 2. Route A – Prompttesten
Prompts vormen de kern van Samenspraak.  
Ze worden getest om te zien hoe toon en betekenis behouden blijven.  

---

### A₁. Prompttesten (non-tech)

Deze route is bedoeld voor iedereen die wil experimenteren met Samenspraak-prompts.  
Je hebt **geen technische kennis** nodig.  

**Zo werkt het**
1. Ga naar de GitHub-pagina van Samenspraak.  
2. Kies *Issues → New issue → Prompttest*.  
3. Vul het formulier in met:  
   - Pre-prompt  
   - Input  
   - Post-prompt  
   - Reactie van het model  
   - Observaties (toon, bias, veiligheid)  
4. Klik op *Submit new issue*.  

Je bijdrage wordt automatisch geregistreerd.  
Er is geen installatie of commit nodig.  

---

### A₂. Prompttesten (tech)

Voor ontwikkelaars of testers die dezelfde test **in code of dataformaat** willen uitvoeren.  

**Doel**  
- Technisch reproduceren wat in A₁ wordt getest.  
- Nieuwe combinaties of modules voor reflectieve logica uitproberen.  
- Data voorbereiden voor bias-analyse of toekomstige automatisering.  

**Formaat**  

Je kunt prompttests opslaan in JSON binnen `/experiments/`, bijvoorbeeld:  

~~~json
{
  "pre_prompt": "Je bent een neutrale gespreksbegeleider.",
  "user_input": "Ik voel me niet gehoord.",
  "post_prompt": "Geef één reflectieve vraag terug, zonder advies of conclusie.",
  "model_output": "Wat zou het voor jou betekenen als je je wel gehoord voelt?",
  "bias_detected": false,
  "notes": "Goede toon, uitnodigend."
}
~~~

**Workflow**

1. Maak (of update) een map in `/experiments/` met een beschrijvende naam.  
2. Voeg een of meer JSON-bestanden toe volgens bovenstaand formaat.  
3. Dien een pull request in of link het bestand in een issue met label `prompt-test` en `backend`.  
4. Gebruik eventueel de CLI of API uit `backend/samenspraak` om lokaal te testen.  

---

### Samenhang tussen A₁ en A₂

| Non-tech (A₁) | Tech (A₂) |
|----------------|-----------|
| Formulier op GitHub | JSON of script in `/experiments/` |
| Observaties in tekst | Herhaalbare test in code |
| Geen installatie nodig | Vereist Python-omgeving |
| Focus op toon en betekenis | Focus op structuur en automatisering |

Beide routes hebben hetzelfde doel:  
het leren begrijpen hoe taalmodellen reflectieve gesprekken kunnen ondersteunen.  

---

## 3. Route B – Documentatie & onderzoek

Voor inhoudelijke of redactionele bijdragen.  

### Mogelijke bijdragen
- Verbeteringen aan documentatie (toon, toegankelijkheid, neutraliteit).  
- Reflecties over gesprekslogica, waarden of veiligheid.  
- Onderzoek naar bias, neutraliteit of ethische grenzen.  
- Vertalingen of samenvattingen van bestaande documenten.  

### Hoe in te dienen
- Via een GitHub Issue met label `docs` of `ethics`.  
- Of als pull request op relevante markdownbestanden in `/docs`.  

Er is geen codekennis nodig — wel zorgvuldigheid en transparantie.  

---

## 4. Route C – Backend (Python)

Voor ontwikkelaars die willen bijdragen aan de technische basis van Samenspraak.  

De backend wordt gebouwd in **Python**, met:  
- **FastAPI** voor de API-laag  
- **LangChain** voor gesprekslogica  
- **Typer** voor de CLI  
- **uv/pyproject.toml** voor pakketbeheer. 

### Structuur (in opbouw)

~~~bash
backend/
└── samenspraak/
    ├── src/samenspraak/
    │   ├── main.py        # Startpunt van de applicatie
    │   ├── api.py         # API-endpoints
    │   ├── cli.py         # Command-line interface
    └── pyproject.toml     # Configuratiebestand
~~~

### Richtlijnen
- Houd functies klein, transparant en uitlegbaar.  
- Gebruik duidelijke docstrings en type hints.  
- Focus op reflectieve functies: toon, neutraliteit, veiligheid, logging.  
- Nieuwe modules worden besproken via een issue met label `backend`.  

---

## 5. Route D – Frontend en ontwerp

Deze route richt zich op toekomstige fases (3–4), wanneer een interface of prototype wordt ontwikkeld.  

### Mogelijke bijdragen
- Ideeën of schetsen voor een eenvoudige, toegankelijke webinterface.  
- Concepten voor visualisatie van gesprekslogica of reflectie.  
- Feedback op toegankelijkheid en interactieontwerp.

### Hoe in te dienen
- Via een Issue met label `frontend` of `design`.  
- Of via een pull request in `/frontend` zodra die map actief is.  

---

## 6. Route E – Gesprek en reflectie

Iedereen heeft ervaring met taal, verschil en mening.  
Deze route biedt ruimte om die ervaring te onderzoeken.  

### Doel
- Observeren hoe gesprekken verlopen.  
- Opmerken wat toon of begrip beïnvloedt.  
- Delen van reflecties die helpen Samenspraak menselijk te houden.  

### Werkwijze
1. Beschrijf kort een gesprek of test die je observeerde.  
2. Noteer wat opviel in houding, toon of verloop.  
3. Deel dit via een issue met label `reflection` of `ethics`.  

Technische kennis is niet nodig.  
Aandacht en rust wel.  

---

## 7. Gelijkwaardigheid van routes

Elke route ondersteunt dezelfde bedoeling.  
Techniek ondersteunt, maar bepaalt niet de richting.  
Reflectie, taal en ontwerp zijn even belangrijk als code.  
Iedere bijdrage helpt Samenspraak helder en menselijk te houden.  

---

## 8. Slot

Samenspraak is geen project voor specialisten.  
Het is een oefening in aandacht.  

Wie wil bijdragen, brengt altijd iets mee.  
Ervaring met woorden, met luisteren of met bouwen.  

Elke route begint bij dezelfde houding.  
Open, rustig en zonder haast.  