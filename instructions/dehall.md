# DEHALL Instruction Design

## Doel

Deze instructie beschrijft hoe de dehallucination layer werkt en welke onderdelen nodig zijn.

## Kerncomponenten

1. Retrieval (RAG)
   - Zoek relevante documenten of feiten op
   - Gebruik een search-engine, vector database of externe kennisbron

2. Grounding
   - Houd de modelprompt gebonden aan de gevonden bronnen
   - Geef expliciete context en citaten mee

3. Fact checking
   - Vergelijk het gegenereerde antwoord met de bronnen
   - Detecteer uitspraken die niet gedekt zijn of inconsistenties bevatten

4. Self verification
   - Laat de modeloutput opnieuw beoordelen
   - Vraag het model om zijn eigen antwoord te valideren en te corrigeren

## Hoe gebruik je dit in Copilot?

- `instructions/` is een plek om je prompt-architectuur en workflow vast te leggen.
- `skills/` is waar je de implementatie bouwt.

### Praktijk

1. Neemt een gebruikersvraag aan
2. Haalt relevante bronnen op via `skills/retrieval`
3. Bouwt een overzichtelijke prompt voor Copilot/LLM
4. Laat het model antwoorden op basis van de bronnen
5. Controleert het antwoord met `skills/fact_checking`
6. Laat het antwoord zelf verifiëren met `skills/self_verification`

## Opmerking

GitHub Copilot zelf biedt geen directe plugin-API om een interne reasoning layer in te voegen.
Je bouwt daarom een externe laag die de prompt en het antwoord beheert, en die je output controleert.
