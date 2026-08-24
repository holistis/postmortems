## 2026-08-24: Je AI-app is in een week gebouwd. Is hij ook in een week gecheckt?

In januari 2026 bouwde iemand een complete app zonder zelf een regel code te schrijven. Binnen drie dagen na lancering lag zijn hele klantendatabase open voor iedereen op internet, zonder in te loggen. Dit is geen uitzondering. Het is wat er gebeurt als snelheid wint van een controle die niemand met opzet overslaat, maar die bijna iedereen overslaat door haast.

### Het probleem, in cijfers

Uit onderzoek bij grote bedrijven blijkt dat ontwikkelaars die met AI werken drie tot vier keer zoveel code leveren, maar tien keer zoveel beveiligingsfouten introduceren. Veracode testte meer dan honderd AI-modellen op beveiligingsgevoelige programmeertaken en vond dat 45 procent van de gegenereerde code een bekende, veelvoorkomende kwetsbaarheid bevat. Dit is geen incident. Dit is bezig de nieuwe standaard te worden.

### Wat er precies misging

De sleutel naar de database stond gewoon zichtbaar in de website-code. Dat hoeft op zichzelf geen probleem te zijn, want die sleutel is vaak bedoeld om door elke bezoeker gebruikt te worden. Het wordt pas een probleem als het slot erachter ontbreekt, de regel die zegt: iedereen mag alleen zijn eigen data zien. Dat slot stond uit. Het resultaat: elke bezoeker kon zonder in te loggen bij alle klantgegevens.

### Zelf checken in vijf minuten

1. Open je site, druk F12, en ga naar het tabblad Netwerk.
2. Vernieuw de pagina en zoek tussen de aanvragen naar iets met "supabase" of "key" erin.
3. Vind je zo'n sleutel, noteer dan de projectnaam die erbij hoort.
4. De volgende vraag is of er ook echt data achter die sleutel zit zonder in te loggen. Dat zelf narekenen vraagt iets meer technische kennis dan de eerste drie stappen. Een ontwikkelaar kan dit meestal in twee minuten voor je bevestigen.
5. Twijfel je, vraag het gewoon na bij wie de app gebouwd heeft, of laat het checken.

### Tot slot

Dit kost vijf minuten om te checken en kan je maanden aan opruimwerk schelen. Wil je het liever door iemand anders laten doen, ik help daar graag bij.

Bronnen: onderzoek naar AI-code-kwaliteit bij grote bedrijven (Fortune 50), Veracode's test van meer dan 100 AI-modellen op beveiligingsgevoelige code, en de publiek gedocumenteerde Moltbook-casus van januari 2026.
