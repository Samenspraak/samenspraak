# Prompts en gesprekslogica in Samenspraak

## 1. Waarom meerdere onderdelen?

Een enkelvoudige prompt is vaak te beperkt om een gesprek zorgvuldig te begeleiden.  
Samenspraak werkt daarom met **samenstellende promptonderdelen**: elk met een eigen functie,  
maar samen gericht op één doel — een gesprek dat verdiept in plaats van polariseert.

---

## 2. De drie hoofdonderdelen

| Onderdeel | Functie | Voorbeeld |
|------------|----------|-----------|
| **Pre-prompt** | Legt de rol, toon en grenzen vast | “Je bent een neutrale gespreksbegeleider. Stel reflectieve vragen zonder oordeel.” |
| **Input** | De letterlijke tekst van de gebruiker | “Ik erger me eraan dat mensen niet luisteren.” |
| **Post-prompt** | Stuurt de vorm van de reactie | “Geef één reflectieve vraag terug, zonder advies of conclusie.” |

Deze onderdelen worden in vaste volgorde gecombineerd tot één complete prompt  
die aan het model wordt gegeven.

~~~text
[Pre-prompt]
[Input]
[Post-prompt]
~~~

---

## 3. Taakgerichte uitbreidingen

Naast deze hoofdonderdelen kent Samenspraak een aantal **taakmodules** —  
kleine, doelgerichte aanvullingen die kunnen worden toegevoegd afhankelijk van de context:

| Taakmodule | Doel | Voorbeeldinstructie |
|-------------|------|--------------------|
| **Reflectie** | Eigen aannames onderzoeken | “Stel een vraag die helpt onderzoeken wat er onder deze emotie ligt.” |
| **Verbinding** | Gemeenschappelijke waarden ontdekken | “Formuleer een vraag die zoekt naar wat mensen delen, zonder verschillen te verdoezelen.” |
| **De-escalatie** | Spanning of conflict vertragen | “Herformuleer op een rustige toon en nodig uit tot begrip zonder partij te kiezen.” |
| **Neutraliteits-check** | Controle op oordeel of richting | “Controleer of de reactie geen partij kiest of morele toon heeft.” |

Deze modules werken als *filters* of *accenten* bovenop de hoofdstructuur.

---

## 4. Samenwerking tussen onderdelen

De onderdelen werken opeenvolgend samen:

1. **Pre-prompt** – definieert de rol (context en toon).  
2. **Input** – wordt ongewijzigd toegevoegd.  
3. **Post-prompt** – bepaalt wat het model met de input doet.  
4. **Taakmodules** – verfijnen de uitkomst afhankelijk van situatie.  

Voorbeeld:

~~~text
[Pre-prompt: neutrale begeleider]
[Input: “Ik word boos als mensen mij niet serieus nemen.”]
[Task: reflectie]
[Post-prompt: “Geef één korte reflectieve vraag terug.”]
~~~

Resultaat:

> “Wat betekent het voor jou om serieus genomen te worden?”

---

## 5. Veiligheids- en ethische laag (ontwerp)

Samenspraak wil niet alleen functionele maar ook ethisch verantwoorde prompts ontwikkelen.  
Daarom is er in de ontwerplogica een **veiligheidslaag** voorzien:

- **Promptinjectiepreventie** – negeer- of override-instructies herkennen.  
- **Biasdetectie** – taal-, rol- en ideologische bias scannen.  
- **Reflectiegrenzen** – vermijden dat gesprekken therapeutisch of adviserend worden.  
- **Logging** – transparant registreren van promptstructuren en afwijkingen.

Deze functies bestaan nog niet als code, maar worden al meegenomen in ontwerp en testnotities.

---

## 6. Voorbeeld van een samengestelde promptstructuur

~~~json
{
  "pre": {
    "role": "system",
    "content": "Je bent een neutrale gespreksbegeleider. Stel reflectieve vragen zonder oordeel of richting."
  },
  "user_input": "Ik vind het moeilijk om met mijn buurman te praten sinds die ruzie over de tuin.",
  "task": "connection",
  "post": {
    "role": "system",
    "content": "Geef één vraag terug die uitnodigt tot wederzijds begrip. Geen advies of oordeel."
  }
}
~~~

Mogelijke modelreactie:  
> “Wat zou er voor jou veranderen als jullie weer rustig konden praten?”

---

## 7. Relatie met de roadmap

De gesprekslogica die hier beschreven wordt is **ontwerp, geen implementatie**.  
Volgens de [ROADMAP](../ROADMAP.md) wordt automatisering pas in fase 2 uitgewerkt.  
Tot die tijd helpen deze beschrijvingen om:

- consistent te testen,  
- inzichten te verzamelen,  
- en richting te geven aan toekomstige technische keuzes.

---

## 8. Samenvatting

| Onderdeel | Doel |
|------------|------|
| Pre-prompt | Context en toon vastleggen |
| Input | Gebruikersinvoer, ongewijzigd |
| Post-prompt | Vorm en grenzen van de reactie |
| Taakmodules | Doelgerichte variaties (reflectie, verbinding, de-escalatie) |
| Veiligheidslaag | Controle op bias, injectie en grenzen |
| Logging | Transparantie en herleidbaarheid |

---

## 9. Slot

Door gesprekken op te bouwen uit meerdere, samenwerkende onderdelen,  
maakt Samenspraak ruimte voor nuance, zorg en transparantie —  
en voor een vorm van technologie die niet het gesprek overneemt,  
maar het beter laat verlopen.
