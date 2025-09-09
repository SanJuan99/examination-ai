# examination-ai
Examination-ai, Fe24, Johan Berg Ekvall.

## AI och datalogiskt tänkande 
## 01 
# ChatGPT: 
"Hej! Ja, jag kan hjälpa dig med det.
De fyra datalogiska delprocesserna är:

Indata

Bearbetning

Utdata

Lagring (ibland även kallad minneshantering)

Vi applicerar dessa på ditt tärningsspel – där målet är att slå tärningen tills du får en stege: 1, 2, 3, 4, 5, 6 i rätt ordning.

🎲 Spelets beskrivning:

Man kastar en 6-sidig tärning.

Första målet är att slå 1.

Därefter 2, sedan 3, upp till 6 i följd.

Man fortsätter kasta tills rätt tal kommer upp. När fel tal kastas, kastar man om samma steg igen.

Man räknar antalet kast totalt tills hela stegen (1 till 6) är klar.

🔄 Tillämpning av de 4 delprocesserna:
1. Indata

Det som spelet tar in eller behöver som startvärden:

Tärningskast (slumpmässigt genererat tal mellan 1–6)

Inga användarinmatningar krävs, men man kan välja att t.ex. låta användaren starta spelet eller trycka för att kasta.

2. Bearbetning

Det som händer i själva programflödet:

Slumpa ett tärningskast

Jämför kastet med det aktuella målet i stegen (börjar med 1)

Om kastet är rätt → gå vidare till nästa steg i stegen (ex. från 1 till 2)

Om kastet är fel → fortsätt försöka på samma steg

Räkna hur många kast som görs totalt

Loopa tills hela stegen (1 till 6) är klar

3. Utdata

Det som spelet visar eller returnerar:

Totalt antal kast som krävdes för att få hela stegen

(Eventuellt: en logg av vad varje kast blev, men det är bonus)

Exempel på utdata:

"Du klarade stegen på 19 kast!"

4. Lagring

Det som behöver sparas under spelets gång:

Nuvarande mål i stegen (vilket tal du försöker få)

Antal kast som har gjorts

(Eventuellt en lista med alla kast, om du vill spara hela historiken)

🧠 Kort kodskiss (frivillig bonus)

Vill du ha ett exempel i Python? Här är ett enkelt:

import random

kast = 0
mål = 1

while mål <= 6:
    kast += 1
    tärning = random.randint(1, 6)
    print(f"Kast {kast}: Du slog {tärning}")
    if tärning == mål:
        mål += 1

print(f"Du klarade hela stegen på {kast} kast!")


Vill du att jag hjälper dig skriva det här i pseudokod eller i ett annat programmeringsspråk?"

# Aizo: 
Absolut! 🎲 Det låter som ett roligt projekt! Vi kan bryta ner det i de fyra datalogiska delprocesserna: dekomposition, mönsterigenkänning, abstraktion och algoritmdesign. Låt oss ta en titt på varje delprocess:

Dekomposition: 
Bryt ner problemet i mindre delar. Vi har flera steg här:
Kasta en tärning och kontrollera om resultatet är 1.
Om 1 inte fås, kasta igen.
När 1 är uppnått, kasta för 2, sedan 3, och så vidare upp till 6.
Räkna antal kast.

Mönsterigenkänning:
Vi letar efter mönster i problemet. Här är mönstret att vi kastar tärningen och kontrollerar om vi får önskat nummer i en sekvens (1 till 6).
Varje kast är oberoende, men vi följer en sekvens för att bestämma nästa mål.

Abstraktion:
Fokusera på vad som är relevant. Här är det relevanta att hantera tärningskast och räkna hur många kast som behövs för att nå en stege från 1 till 6.
Ignorera detaljer som tärningsfärg eller kaststil som inte påverkar målet.

Algoritmdesign:
Nu är det dags att designa en algoritm. Här är ett enkelt flöde:
Initiera en räknare för kast.
Starta en loop för att kasta tärningen.
Kontrollera om tärningen visar det aktuella målnumret.
Om ja, gå vidare till nästa mål.
Om nej, kasta om.
Fortsätt tills hela sekvensen 1-6 är uppnådd.
Returnera eller skriv ut antalet kast.

Nu när du har en översikt, vad tror du är nästa steg? Kan du börja skriva koden för att kasta tärningen och kontrollera resultatet?

# MITT SVAR
Det ser ut som att båda ai:s svar är ganska lika. De applicera de fyra datalogiska delprocesserna före eller senare i varsina svar. Båda två fokuserar på vad som är relevant och förklarar vad som kan vara oviktig information som man inte behöver tänka på.

# 02
# ChatGPT:
START

Sätt kast = 0
Sätt mål = 1  // Det första talet vi vill slå

SÅ LÄNGE mål <= 6 GÖR:
    Slå en tärning (slumpa tal mellan 1 och 6) → resultat
    Öka kast med 1

    OM resultat = mål SÅ:
        Öka mål med 1   // Gå vidare till nästa steg i stegen
    ANNARS:
        // Fortsätt försöka på samma mål (gör ingenting)

SLUTSATS:
Skriv ut: "Du klarade stegen på [kast] kast."

STOPP

## MITT SVAR
Både ChatGPT och Aizo skrev samma svar. Kort och logiskt som pseudokod brukar vara?

# 03
## Aizo och ChatGPT skrev liknande svar:
"// Tärningsspelet – Stege 1 till 6
function spelaTarningsStege() {
    let kast = 0;
    let mål = 1;

    console.log("🎲 Spelet startar! Målet är att slå en stege: 1, 2, 3, 4, 5, 6");

    while (mål <= 6) {
        // Slå tärning: slumpa ett heltal mellan 1 och 6
        let resultat = Math.floor(Math.random() * 6) + 1;
        kast++;

        console.log(`Kast ${kast}: Du slog ${resultat} (Försöker få ${mål})`);

        if (resultat === mål) {
            console.log(`✔️ Rätt! Du går vidare till ${mål + 1}`);
            mål++;
        } else {
            console.log(`❌ Fel. Försök igen på ${mål}`);
        }
    }

    console.log(`🎉 Du klarade hela stegen på ${kast} kast!`);
}

// Kör spelet
spelaTarningsStege();"
# RESULTAT:
// Kör spelet
spelaTarningsStege();
VM268:6 🎲 Spelet startar! Målet är att slå en stege: 1, 2, 3, 4, 5, 6

VM268:13 Kast 1: Du slog 3 (Försöker få 1)

VM268:19 ❌ Fel. Försök igen på 1

VM268:13 Kast 2: Du slog 5 (Försöker få 1)

VM268:19 ❌ Fel. Försök igen på 1

VM268:13 Kast 3: Du slog 2 (Försöker få 1)

VM268:19 ❌ Fel. Försök igen på 1

VM268:13 Kast 4: Du slog 2 (Försöker få 1)

VM268:19 ❌ Fel. Försök igen på 1

VM268:13 Kast 5: Du slog 2 (Försöker få 1)

VM268:19 ❌ Fel. Försök igen på 1

VM268:13 Kast 6: Du slog 6 (Försöker få 1)

VM268:19 ❌ Fel. Försök igen på 1

VM268:13 Kast 7: Du slog 2 (Försöker få 1)

VM268:19 ❌ Fel. Försök igen på 1

VM268:13 Kast 8: Du slog 4 (Försöker få 1)

VM268:19 ❌ Fel. Försök igen på 1

VM268:13 Kast 9: Du slog 5 (Försöker få 1)

VM268:19 ❌ Fel. Försök igen på 1

VM268:13 Kast 10: Du slog 4 (Försöker få 1)

VM268:19 ❌ Fel. Försök igen på 1

VM268:13 Kast 11: Du slog 1 (Försöker få 1)

VM268:16 ✔️ Rätt! Du går vidare till 2

VM268:13 Kast 12: Du slog 3 (Försöker få 2)

VM268:19 ❌ Fel. Försök igen på 2

VM268:13 Kast 13: Du slog 1 (Försöker få 2)

VM268:19 ❌ Fel. Försök igen på 2

VM268:13 Kast 14: Du slog 5 (Försöker få 2)

VM268:19 ❌ Fel. Försök igen på 2

VM268:13 Kast 15: Du slog 4 (Försöker få 2)

VM268:19 ❌ Fel. Försök igen på 2

VM268:13 Kast 16: Du slog 5 (Försöker få 2)

VM268:19 ❌ Fel. Försök igen på 2

VM268:13 Kast 17: Du slog 4 (Försöker få 2)

VM268:19 ❌ Fel. Försök igen på 2

VM268:13 Kast 18: Du slog 3 (Försöker få 2)

VM268:19 ❌ Fel. Försök igen på 2

VM268:13 Kast 19: Du slog 6 (Försöker få 2)

VM268:19 ❌ Fel. Försök igen på 2

VM268:13 Kast 20: Du slog 5 (Försöker få 2)

VM268:19 ❌ Fel. Försök igen på 2

VM268:13 Kast 21: Du slog 2 (Försöker få 2)

VM268:16 ✔️ Rätt! Du går vidare till 3

VM268:13 Kast 22: Du slog 3 (Försöker få 3)

VM268:16 ✔️ Rätt! Du går vidare till 4

VM268:13 Kast 23: Du slog 4 (Försöker få 4)

VM268:16 ✔️ Rätt! Du går vidare till 5

VM268:13 Kast 24: Du slog 1 (Försöker få 5)

VM268:19 ❌ Fel. Försök igen på 5

VM268:13 Kast 25: Du slog 1 (Försöker få 5)

VM268:19 ❌ Fel. Försök igen på 5

VM268:13 Kast 26: Du slog 5 (Försöker få 5)

VM268:16 ✔️ Rätt! Du går vidare till 6

VM268:13 Kast 27: Du slog 2 (Försöker få 6)

VM268:19 ❌ Fel. Försök igen på 6

VM268:13 Kast 28: Du slog 1 (Försöker få 6)

VM268:19 ❌ Fel. Försök igen på 6

VM268:13 Kast 29: Du slog 3 (Försöker få 6)

VM268:19 ❌ Fel. Försök igen på 6

VM268:13 Kast 30: Du slog 1 (Försöker få 6)

VM268:19 ❌ Fel. Försök igen på 6

VM268:13 Kast 31: Du slog 4 (Försöker få 6)

VM268:19 ❌ Fel. Försök igen på 6

VM268:13 Kast 32: Du slog 6 (Försöker få 6)

VM268:16 ✔️ Rätt! Du går vidare till 7

VM268:23 🎉 Du klarade hela stegen på 32 kast!

undefined

## Ai som studiekamrat
# 04
Jag tror där det skulle börja uppstå problem är i större projekt. När det är många rader kod och olika saker som påverkas och det blir svårt för Ai att få allt att hänga ihop. Mindre projekt eller delar som är fokuserat på att bara göra en sak är ai bättre på tror jag.

# 05
# Aizo:
"Självklart! Här används CSS-egenskapen box-shadow för att lägga till en skugga till ett element. Låt oss bryta ner värdena:

12px: Detta är den horisontella offseten för skuggan. Ett positivt värde flyttar skuggan till höger, medan ett negativt värde skulle flytta den till vänster.

12px: Detta är den vertikala offseten för skuggan. Ett positivt värde flyttar skuggan nedåt, medan ett negativt värde skulle flytta den uppåt.

2px: Detta är suddighetsradien. Ju större värde, desto mer suddig blir skuggan. Ett värde på 0 skulle betyda att skuggan har skarpa kanter.

1px: Detta är spridningsradien. Ett positivt värde gör skuggan större, medan ett negativt värde gör den mindre.

rgba(0, 0, 255, .2): Detta anger färgen på skuggan. rgba står för röd, grön, blå och alfa (genomskinlighet). Här är skuggan blå (0, 0, 255) med en genomskinlighet på 20% (.2).

Så, denna box-shadow skapar en blå skugga som ligger 12 pixlar till höger och 12 pixlar nedanför elementet, med en lätt suddighet och en liten spridning."
# ChatGPT:
"Absolut! Låt oss bryta ner den här CSS-regeln:

box-shadow: 12px 12px 2px 1px rgba(0, 0, 255, 0.2);


Detta skapar en skugga runt ett HTML-element.
Här är vad varje del betyder:

📦 box-shadow: Skapar en skugga bakom ett element

Syntaxen är:

box-shadow: offset-x offset-y blur-radius spread-radius color;

📘 Din specifika regel:
box-shadow: 12px 12px 2px 1px rgba(0, 0, 255, 0.2);


Förklaring:

Värde	Vad det gör
12px	Horisontellt avstånd – skuggan förskjuts 12px till höger
12px	Vertikalt avstånd – skuggan förskjuts 12px nedåt
2px	Blur-radius (oskärpa) – gör skuggan mjukare, diffus med 2px
1px	Spread-radius – skuggan expanderar 1px utåt från kanten
rgba(0, 0, 255, 0.2)	Färg – en genomskinlig blå färg (20% opacitet)
🎨 Visuellt:

Det ser ut som att elementet har en svagt blå skugga.

Skuggan ligger lite snett neråt till höger.

Den är lite suddig (2px blur).

Den är även lite större än själva elementet (1px spread).
# MITT SVAR:
Jag kan inte direkt se några språkliga skillnader. Den enda skillnaden jag kan se är att Aizo kanske förklarar lite smått mer vad ett värde gör. Båda förklarar vad alla värden betyder.

# 06
Jag såg inte att jag fick tillbaka exakt samma svar. chatGPT rekommenderade först en utdaterad lösning med promise(). Den kanske rekommenderar utdaterade svar när den märker att den måste skriva om fungerande kod?

# 07 - Anpassa ChatGPT
