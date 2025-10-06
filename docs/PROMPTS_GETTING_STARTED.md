# Werken met prompts in Samenspraak

## 1. Doel van deze gids

Deze gids helpt bij het testen en ontwikkelen van prompts binnen Samenspraak.  
Het project bevindt zich nog in de verkenningsfase: er is geen backend of applicatie.  
Alle experimenten gebeuren handmatig, met bestaande taalmodellen zoals ChatGPT.

---

## 2. Wat is een prompt

Een prompt is de tekst waarmee een taalmodel wordt aangestuurd.  
Ze bepaalt toon, houding en richting van wat het model teruggeeft.

In Samenspraak worden prompts gebruikt om gesprekken te **vertragen en verdiepen**.  
Het doel is niet overtuigen of corrigeren, maar helpen reflecteren en luisteren.

---

## 3. Opbouw van een Samenspraak-prompt

Een gesprek bestaat uit drie lagen:

```
[Pre-prompt]
[Input]
[Post-prompt]
```

| Onderdeel | Functie |
|------------|----------|
| **Pre-prompt** | Legt rol, toon en grenzen vast. |
| **Input** | De tekst van de gebruiker. |
| **Post-prompt** | Bepaalt de vorm van de reactie. |

---

## 4. Prompts testen

1. Open een nieuwe chat.  
2. Plak de pre-prompt.  
3. Voeg de gebruikersinvoer toe.  
4. Sluit af met de post-prompt.  
5. Observeer de toon en diepgang van de reactie.

### Eenvoudig voorbeeld

| Stap | Tekst |
|------|-------|
| Pre | “Je bent een neutrale gespreksbegeleider. Stel reflectieve vragen zonder oordeel.” |
| Input | “Ik voel me niet gehoord.” |
| Post | “Geef één reflectieve vraag terug, zonder advies of conclusie.” |
| Resultaat | “Wat zou het voor jou betekenen als je je wel gehoord voelt?” |

---

### Uitgebreider voorbeeld

| Stap | Tekst |
|------|-------|
| **Pre-prompt** | “Je begeleidt een gesprek waarin spanning voelbaar is. Stel vragen die helpen onderliggende waarden te verkennen, zonder richting of oordeel.” |
| **Input** | “Ik heb vaak discussies met mijn collega over duurzaamheid. Hij noemt mij idealistisch en ik word daar boos van.” |
| **Post-prompt** | “Formuleer één reflectieve vraag die helpt onderzoeken wat er onder die boosheid ligt. Vermijd advies of interpretatie.” |
| **Mogelijke reactie** | “Wat raakt jou het meest als hij zegt dat je te idealistisch bent?” |
| **Observatie** | De vraag nodigt uit tot zelfonderzoek zonder oordeel. |

---

## 5. Waarop te letten bij het testen

### Neutraliteit en toon
- Vermijd sturende of moraliserende formuleringen.  
- Gebruik open vragen zoals “Wat maakt dat…” of “Hoe ervaar jij…”.  
- Houd de toon uitnodigend, niet adviserend.

### Bias
Bias kan op verschillende niveaus optreden:
- **Taalbias:** woorden met emotionele lading.  
- **Rolbias:** impliciet partij kiezen.  
- **Ideologische bias:** voorkeur voor een bepaald wereldbeeld.  

### Veiligheid
- Vermijd advies of diagnose.  
- Ga niet te diep in op persoonlijke thema’s.  
- Behoud een reflectieve afstand.

### Belangen
- Wees transparant over context en mogelijke belangen.  
- Noteer wanneer taal een bepaald perspectief bevoordeelt.

---

## 6. Bevindingen noteren en delen

Na het testen kunnen bevindingen worden vastgelegd.  
Gebruik daarvoor een korte tekst of JSON-structuur, zoals:

```json
{
  "user_input": "Ik raak gefrustreerd als mensen mijn zorgen over klimaat bagatelliseren.",
  "pre_prompt": "Je bent een neutrale gespreksbegeleider.",
  "post_prompt": "Geef één reflectieve vraag terug die helpt onderzoeken wat er onder de frustratie ligt.",
  "model_output": "Wat betekent het voor jou om serieus genomen te worden in dit onderwerp?",
  "bias_detected": false,
  "notes": "Goede toon, uitnodigend. Eventueel meer nadruk op waardeverkenning."
}
```

### Delen van resultaten

Er zijn twee mogelijkheden:

**A. Via GitHub Issues (aanbevolen)**  
- Ga naar *Issues → New issue → Prompttest*.  
- Vul het formulier in en verstuur het.  
- Er is geen technische handeling nodig.

**B. Via code (voor gevorderden)**  
- Fork de repository.  
- Voeg het JSON-bestand toe in `/experiments`.  
- Maak een pull request.

Kies de methode die het best bij je ervaring past.

---

## 7. Hoe resultaten later worden verwerkt

Volgens de [ROADMAP](../ROADMAP.md) worden de bevindingen in een volgende fase gebruikt om:

| Fase | Doel |
|------|------|
| **2** | Automatisering van pre-, input- en post-prompts. |
| **3** | Toetsing van bias en neutraliteit. |
| **4** | Ontwikkeling van reflectie-logica en logging. |

De huidige fase richt zich uitsluitend op observatie en inzicht.

---

## 8. Ethische uitgangspunten

Gebaseerd op het [Manifest](../MANIFESTO.md) en [Governance](../GOVERNANCE.md):

- Transparantie over keuzes.  
- Ruimte voor verschil.  
- Geen oordeel of advies.  
- Menselijkheid boven techniek.  
- Gedeelde verantwoordelijkheid.

---

## 9. Samenvatting

| Onderwerp | Richtlijn |
|------------|-----------|
| Neutraliteit | Open, reflectief, niet sturend. |
| Bias | Signaleren en documenteren. |
| Veiligheid | Vermijd advies of therapie. |
| Belangen | Transparant benoemen. |
| Injectie | Herkennen van manipulerende invoer. |
| Privacy | Geen herleidbare gegevens. |

---

Samenspraak gebruikt taal niet om te winnen, maar om te verhelderen.  
Iedere test draagt bij aan een beter begrip van hoe taalmodellen reflectie kunnen ondersteunen.
