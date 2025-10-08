# Prompts en gesprekslogica in Samenspraak

Deze gids beschrijft hoe Samenspraak werkt met vaste prompts  
om gesprekken rustig, open en menselijk te begeleiden.  
Ze sluit aan op [PROMPTS_GETTING_STARTED.md](PROMPTS_GETTING_STARTED.md),  
waar wordt uitgelegd hoe prompttesten worden uitgevoerd.

---

## 1. Waarom gesprekslogica

Samenspraak gebruikt taalmodellen niet om te overtuigen of te adviseren,  
maar om gesprekken te ondersteunen die aandachtig en gelijkwaardig blijven.  
Daarvoor is een vaste gesprekslogica nodig:  
een structuur die rust brengt in toon, rol en volgorde.

Deze logica zorgt dat:
- gesprekken herkenbaar en herhaalbaar zijn;  
- deelnemers weten vanuit welk kader het model reageert;  
- observaties betekenisvol kunnen worden vergeleken.

Samenspraak is daarmee geen “slim” systeem,  
maar een zorgvuldig vormgegeven omgeving voor taal.

---

## 2. De basisstructuur van een prompt

Elke prompt in Samenspraak bestaat uit drie onderdelen.

~~~text
[Pre-prompt]
[Input]
[Post-prompt]
~~~

| Onderdeel | Doel | Beschrijving |
|------------|------|--------------|
| **Pre-prompt** | Legt de rol, toon en grenzen vast. | Vaste tekst die bepaalt hoe het model zich opstelt. |
| **Input** | Brengt de woorden van de gebruiker(s) in. | Wat mensen zelf schrijven of zeggen. |
| **Post-prompt** | Stuurt de vorm van de reactie. | Vaste tekst die bepaalt hoe het model reageert. |

De pre- en post-prompts komen uit een gemeenschappelijke bibliotheek  
en worden niet door een model gegenereerd of aangepast.  
Ze zijn zorgvuldig geformuleerd, getest en herbruikbaar in verschillende gesprekken.

---

## 3. Een gesprek als proces

Een gesprek binnen Samenspraak verloopt in vaste fasen.  
Elke fase heeft één of meer vaste pre- en post-prompts die passen bij de bedoeling van dat moment.  
Deze prompts bepalen de toon en houding, maar niet de inhoud van het gesprek.

De volgorde van fasen is logisch en wordt handmatig (of later systeemmatig) bepaald:  
het gesprek gaat pas verder als dat passend is.  
Samenspraak kiest of schrijft niets automatisch.

| Fase | Doel |
|------|------|
| **1. Oriëntatie** | Rust creëren en het gesprek openen. |
| **2. Verkenning** | Onderzoeken wat belangrijk is voor de deelnemers. |
| **3. Verbinding** | Aandacht richten op wat mensen delen of begrijpen. |
| **4. Afronding** | Reflecteren op wat het gesprek bracht. |

---

### Voorbeeld van een doorlopend gesprek

Onderstaand fictief voorbeeld laat zien hoe twee mensen samen één Samenspraak-interface gebruiken.  
De pre- en post-prompts komen uit de bibliotheek en blijven per fase gelijk.  
De **LLM genereert de reacties** binnen deze vaste kaders.  
De voorbeeldteksten zijn illustratief: ze tonen hoe toon en houding door de structuur worden vastgehouden.

---

**Fase 1 – Oriëntatie**

Oriëntatie is bedoeld om het gesprek op gang te brengen.  
Er zijn meerdere vaste post-prompts beschikbaar,  
afhankelijk van hoe open of concreet de eerste inbreng is.  
De juiste variant kan handmatig of systeemmatig worden gekozen.

~~~text
Pre-prompt:  Je bent een neutrale gespreksruimte. Je ondersteunt twee mensen die samen een gesprek beginnen. De toon is rustig en open.  
Input:       “Ik weet niet goed waar ik moet beginnen, maar er zit me iets dwars.”  
Post-prompt: Stel één open vraag die helpt verkennen wat iemand wil inbrengen.
~~~

**Reactie van de LLM:**  
> “Wat zou je op dit moment willen delen of onderzoeken?”

Wanneer iemand direct een concreet onderwerp noemt,  
kan een andere vaste post-prompt uit dezelfde fase worden gebruikt:

~~~text
Post-prompt (variant): Stel één korte vraag die helpt even stil te staan bij wat iemand zojuist deelde.
~~~

**Reactie van de LLM:**  
> “Wat maakte dit belangrijk om nu te benoemen?”

---

**Fase 2 – Verkenning**

Verkenning helpt mensen te onderzoeken wat voor hen van waarde is.  
Ook hier bestaan meerdere vaste promptvarianten,  
afhankelijk van hoe het gesprek zich ontwikkelt.

~~~text
Pre-prompt:  Je bent een neutrale gespreksruimte. Je ondersteunt twee mensen in een open gesprek. De toon is rustig en onderzoekend.  
Input:       “Ik merk dat we elkaar soms verkeerd begrijpen.”  
Post-prompt: Stel één vraag die helpt onderzoeken wat ieder belangrijk vindt om gehoord te worden.
~~~

**Reactie van de LLM:**  
> “Wat is voor ieder van jullie belangrijk om gehoord te worden?”

Andere vaste variant in dezelfde fase:

~~~text
Post-prompt (variant): Stel één vraag die helpt verkennen wat onder deze woorden ligt, zonder richting te geven.
~~~

**Reactie van de LLM:**  
> “Wat speelt er voor ieder van jullie onder dit gevoel van misverstand?”

---

**Fase 3 – Verbinding**

Verbinding richt zich op wat mensen delen, zonder dat verschillen verdwijnen.

~~~text
Pre-prompt:  Je bent een neutrale gespreksruimte. Je ondersteunt twee mensen in een gesprek waarin verschil mag bestaan. De toon is uitnodigend en reflectief.  
Input:       “Ik snap nu beter waar jij vandaan komt.”  
Post-prompt: Stel één vraag die uitnodigt om te benoemen wat jullie delen, zonder conclusie te trekken.
~~~

**Reactie van de LLM:**  
> “Wat willen jullie allebei behouden, ook als er verschillen blijven?”

---

**Fase 4 – Afronding**

De afronding nodigt uit tot rust en terugblik.

~~~text
Pre-prompt:  Je bent een neutrale gespreksruimte. Je ondersteunt twee mensen die samen terugkijken op hun gesprek. De toon is rustig en uitnodigend.  
Input:       “Het was goed om dit rustig te bespreken.”  
Post-prompt: Stel één korte vraag die uitnodigt om stil te staan bij wat dit gesprek bracht.
~~~

**Reactie van de LLM:**  
> “Wat nemen jullie mee uit dit gesprek?”

---

Deze vaste fasen vormen de kern van de gesprekslogica in Samenspraak.  
De inhoud verandert door wat mensen zelf inbrengen,  
maar de structuur en toon blijven gelijk.  
De LLM reageert alleen binnen de grenzen van de pre- en post-prompts.  
In een latere fase kan worden onderzocht of het systeem  
automatisch kan toetsen of een volgende fase passend is.

---

## 4. Werken met vaste prompts

Samenspraak werkt met een bibliotheek van **generieke pre- en post-prompts**,  
ontwikkeld en beheerd door de community.  
Iedere prompt is een bouwsteen die hergebruikt kan worden in verschillende gesprekken en fasen.

### 4.1 Rolverdeling tussen Samenspraak en LLM

| Rol | Verantwoordelijkheid |
|------|----------------------|
| **Samenspraak** | Bepaalt de structuur, kiest vaste pre- en post-prompts, bewaakt de volgorde en fase. |
| **LLM** | Genereert de tekstuele reactie binnen de grenzen van die prompts, zonder ze te wijzigen. |

Samenspraak bepaalt dus *het kader*,  
de LLM brengt er *taal in beweging* binnen dat kader.  
Zo ontstaat een gesprek dat voorspelbaar, veilig en herhaalbaar is,  
maar toch levend in toon.

### 4.2 Kenmerken van vaste prompts

- **Herkenbaar:** iedereen ziet welke tekst wordt gebruikt.  
- **Herhaalbaar:** dezelfde prompt kan in meerdere contexten worden toegepast.  
- **Menselijk eigendom:** teksten worden niet door modellen gegenereerd.  
- **Fasegericht:** prompts horen bij een bepaald gespreksmoment.  
- **Variabel binnen grenzen:** per fase kunnen meerdere vaste prompt-varianten bestaan.

### 4.3 Voorbeeld van bibliotheekprompts

| Fase | Pre-prompt (voorbeeld) | Post-prompt (voorbeeld) |
|------|-------------------------|--------------------------|
| Oriëntatie | “Je bent een neutrale gespreksruimte. Je helpt twee mensen een gesprek te beginnen.” | - “Stel één open vraag die helpt verkennen wat iemand wil inbrengen.”<br>- “Stel één korte vraag die helpt even stil te staan bij wat iemand zojuist deelde.” |
| Verkenning | “Je ondersteunt twee mensen die iets van elkaar willen begrijpen.” | - “Stel één vraag die helpt onderzoeken wat ieder belangrijk vindt om gehoord te worden.”<br>- “Stel één vraag die helpt verkennen wat onder deze woorden ligt.” |
| Verbinding | “Je ondersteunt twee mensen in een gesprek waarin verschil en overeenstemming mogen bestaan.” | “Stel één vraag die uitnodigt tot gedeeld begrip.” |
| Afronding | “Je bent een neutrale gespreksruimte die helpt afronden zonder oordeel.” | “Stel één vraag die uitnodigt om stil te staan bij wat dit gesprek bracht.” |

Samenspraak kan in de toekomst logische condities gebruiken  
om te bepalen welke variant binnen een fase het meest passend is.  
Die keuze gebeurt niet via een LLM, maar via eenvoudige controlelogica of handmatige selectie.

---

## 5. Afstemming op toon en context

De reacties van de LLM mogen zich aanpassen in **toon en taal**,  
maar niet in inhoud of richting.  
De prompts blijven vast; de reactie sluit taalkundig aan bij wat mensen schrijven of zeggen.

### Richtlijnen

- **Wel:** woorden uit de input hernemen om nabijheid te tonen.  
- **Wel:** toon afstemmen op emotie of spanning.  
- **Niet:** prompts wijzigen of inhoudelijk interpreteren.  
- **Niet:** advies geven, samenvatten of oordelen.

### Voorbeeld

~~~text
Vaste pre-prompt:  Je bent een neutrale gespreksruimte. De toon is rustig en uitnodigend.  
Input:             “Ik word er moedeloos van dat het telkens opnieuw misgaat.”  
Vaste post-prompt: Stel één reflectieve vraag die helpt verkennen wat iemand bezighoudt, zonder richting of conclusie.
~~~

**Reactie van de LLM:**  
> “Wat maakt dat het telkens opnieuw misgaan zoveel met je doet?”

De prompt blijft vast; de LLM neemt woorden uit de input over  
om aandachtig en betrokken te blijven in toon.

---

## 6. Zorgvuldigheid en veiligheid

Samenspraak is ontworpen met aandacht voor veiligheid, transparantie en begrenzing.  
De gesprekslogica helpt voorkomen dat het model adviseert, oordeelt of samenvat.  

Belangrijke aandachtspunten:

- **Rolbehoud:** Samenspraak is gespreksruimte, geen deelnemer.  
- **Biasobservatie:** letten op subtiele voorkeuren in toon of taal.  
- **Grenzen aan reflectie:** geen diagnose of persoonlijke richting.  
- **Transparantie:** altijd zichtbaar maken welke prompts zijn gebruikt.

---

## 7. Testen en terugkoppelen

Testresultaten worden vastgelegd volgens de structuur in  
[PROMPTS_GETTING_STARTED.md](PROMPTS_GETTING_STARTED.md#6-bevindingen-vastleggen).  

Voorbeeld:

~~~json
{
  "pre_prompt": "Je bent een neutrale gespreksruimte.",
  "user_input": "Ik vind het lastig om rustig te blijven als iemand me tegenspreekt.",
  "post_prompt": "Stel één korte vraag die helpt onderzoeken wat iemand bezighoudt, zonder oordeel.",
  "model_output": "Wat maakt het voor jou moeilijk als iemand je tegenspreekt?",
  "bias_detected": false,
  "notes": "Toon is rustig en reflectief. Geen oordeel of richting."
}
~~~

Zo blijft elk gesprek herleidbaar tot de gebruikte prompts en observaties.

---

## 8. Slot

De gesprekslogica van Samenspraak draait om aandacht, rust en menselijke maat.  
De prompts zijn niet bedoeld om taal te sturen, maar om ruimte te bieden aan verschil.  
Door te werken met vaste, gemeenschappelijk ontwikkelde teksten  
blijft Samenspraak transparant, uitlegbaar en zorgzaam.  
De LLM brengt taal in beweging binnen deze kaders,  
maar de betekenis ontstaat in het gesprek tussen mensen.
