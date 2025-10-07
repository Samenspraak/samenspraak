# Bijdragen aan Samenspraak – Routes en richtlijnen

Samenspraak verwelkomt bijdragen van zowel technische als niet-technische deelnemers.  
De bijdragen zijn georganiseerd in vier routes, die samen de verschillende fasen van het project ondersteunen.

---

## 1. Route A – Prompttesten

Prompts vormen de kern van Samenspraak.  
Er zijn twee manieren om ze te testen: via een formulier (voor iedereen)  
of via code (voor ontwikkelaars).

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

## 2. Route B – Documentatie & onderzoek

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

## 3. Route C – Backend (Python)

Voor ontwikkelaars die willen bijdragen aan de technische basis van Samenspraak.

De backend wordt gebouwd in **Python**, met:
- **FastAPI** voor de API-laag  
- **LangChain** voor gesprekslogica  
- **Typer** voor de CLI  
- **uv/pyproject.toml** voor pakketbeheer

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

## 4. Route D – Frontend & UX

Deze route richt zich op toekomstige fases (3–4),  
wanneer een interface of prototype wordt ontwikkeld.

### Mogelijke bijdragen
- Ideeën of schetsen voor een eenvoudige, toegankelijke webinterface.  
- Concepten voor visualisatie van gesprekslogica of reflectie.  
- Feedback op toegankelijkheid en interactieontwerp.

### Hoe in te dienen
- Via een Issue met label `frontend` of `design`.  
- Of via een pull request in `/frontend` zodra die map actief is.

---

## 5. Samenvatting

| Route | Voor wie | Werkwijze |
|--------|-----------|-----------|
| **A. Prompttesten (non-tech / tech)** | Iedereen / ontwikkelaars | Formulier of JSON in `/experiments/`. |
| **B. Documentatie & onderzoek** | Inhoudelijk | Issue of PR met label `docs` of `ethics`. |
| **C. Backend (Python)** | Ontwikkelaars | Code in `backend/`, met review via `backend`-issue. |
| **D. Frontend & UX** | Ontwerpers / tech | Ideeën of concepten delen via `frontend`-issue. |

---

## 6. Overwegingen

- Alle routes zijn gelijkwaardig in waarde.  
- Technische bijdragen blijven ondersteunend aan de reflectieve bedoeling.  
- Documentatie en gesprekken over waarden zijn net zo belangrijk als code.  
- De AGPLv3-licentie geldt voor alle bijdragen.

---

## 7. Slot

Samenspraak groeit door samenwerking tussen verschillende werelden:  
taal, technologie, ontwerp, ethiek en onderzoek.  
Iedere bijdrage helpt om gesprekken menselijker te maken — stap voor stap.
