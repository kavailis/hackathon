# Hackathon hos Violet

Ni ska nu ger er på att försöka lösa fem olika programmeringsuppgifter. Outputen av varje löst problem ger en siffra, där de samlade lösningarna tillsammans ger en sifferkombination som motsvarar alfabetiska positioner. Givet dessa motsvarande bokstäver ska ni nu komma fram till korrekt ord som sökes. Exempelvis: Siffran 1 motsvarar bokstaven A, siffran 24 motsvarar bokstaven X. Bonus ges till de grupper som skriver både effektiv och läsbar kod!

Ni får lösa det i vilket programmeringsspråk ni vill, men vi uppmuntrar er till att använda Python då det är det vi kodar i!

Ord som sökes: 

## Problem 1
Ibland kan posten ha svårt att hitta till Violets adress, Linnégatan 87A, när de ska leverera paket. Mer specifikt har de ofta svårt att hitta vilken våning vi är på. posten har därför börjat med ett internt system för att lista ut vilken våning de ska leverera till, men brevbärarna tycker att instruktionerna är lite oklara. När de levererar ett paket börjar de på våning 0 och sedan följer instruktionerna en karaktär i taget. Ett plustecken, +, betyder att de ska upp en våning, ett minustecken, -, betyder att de ska ned en våning.

#### Exempelvis: 
* ++-- och +-+- resulterar båda i våning 0
* +-- och --+ resulterar båda i våning -1 (källaren)
* ++++--+ resulterar i våning 3

Vilken våning ska posten leverera till?

Er input är finns [här](https://gist.githubusercontent.com/kavailis/4710b5a3b42eddf20de753e47ba61394/raw/bf57b2981634a21866aad6146974167215d1a8b4/problem_1).


## Problem 2
Posten lyckades hitta till Violet men nu kvarstår nästa utmaning: Att hitta till rätt rum! Det öppna kontorslandskapet till trots kan det vara svårt att hitta till de mindre, inglasade, rummen. PostNord har dock listat ut ett sätt att ta sig till rätt rum, via ett dokument innehållandes en lista på möjliga rektanglar, där ett gömt svar ger siffran till vilket rum som brevbäraren ska ta sig till. 

För att en rektangel ska vara möjlig måste summan av alla vinklar av rektangeln vara lika med 360. Exempelvis ger vinklarna 180, 180, 60, 60 inte en rektangel, eftersom att 180+180+60+60 = 480 =/= 360. Däremot ger vinklarna 100, 80, 150, 30 en rektangel, då 100+80+150+30 = 360.

Givet [denna](https://gist.githubusercontent.com/kavailis/4710b5a3b42eddf20de753e47ba61394/raw/bf57b2981634a21866aad6146974167215d1a8b4/problem_2) lista, räkna ut hur många av de listade vinklarna som ger en rektangel.

## Problem 3
Äntligen har posten lyckats leverera till rätt rum hos Violet! Kan ni gissa vad paketet innehåller? That’s right, en mining-rig. Nu är det dags för Violet att bryta sina egna Violetcoins! Violetcoin mineras på ett annorlunda sätt jämfört med andra typer av kryptovalutor, nämligen genom att räkna ut medelvärdet av checksummor. Ni har fått ett tabulerat dokument med rader beståendes av till synes slumpmässiga tal, detta dokument ska ni nu använda till att lösa ut medelvärdet av checksumman. Hur får man då ut en checksumma? Jo, för varje rad i dokumentet ska ni ta reda på skillnaden mellan den största och lägsta siffran - checksumman fås av summan av alla dessa skillnader.

#### Exempelvis: 
Givet följande tabell:

3 8 11 9

2 1 0 6

4 7 1 12

* Den första radens största och lägsta siffra är 11 respektive 3, skillnaden mellan dessa är 8
* Den andra radens största och lägsta siffra är 6 respektive 0, skillnaden mellan dessa är 6
* Den tredje radens största och lägsta siffra är 12 respektive 1, skillnaden mellan dessa är 11

Checksumman för exempeltabellen blir 8+6+11 = 25, medelvärdet blir då avrundat till 8.

Vad blir medelvärdet av checksumman för [dessa](https://gist.githubusercontent.com/kavailis/4710b5a3b42eddf20de753e47ba61394/raw/bf57b2981634a21866aad6146974167215d1a8b4/gistfile1.txt?) rader? Avrunda till närmaste heltal om det behövs.

## Problem 4
Efter att ni nu satt upp mining-riggen bestämmer ni er för att ta en pingisrast. Ni går för att hämta racketen men inser snabbt att de förflyttats från sin vanliga plats till ett kassaskåp. Ingen på kontoret verkar veta vad lösenordet kan vara, men ni hittar en lapp på pingisbordet som innehåller några intressanta instruktioner för hur man kan få fram lösenordet:

1. Hitta ett sexsiffrigt värde mellan 248345 och 746315 som uppfyller följande kriterier:
* Går man från vänster till höger minskar aldrig siffrorna, de enbart ökar eller är samma som föregående siffra
* Två närliggande siffror i lösenordet är likadana (ex. 123345)
2. Värdet är den sexsiffriga kombination som är den tredje sexsiffriga kombination närmast siffran 248345 och som uppfyller kriterierna från 1.
3. Lösenordet fås genom att ta medelvärdet av den sexsiffriga kombinationen och avrunda till närmaste heltal.

#### Exempelvis:
Om vi i detta exempel letar efter ett tresiffrigt värde och har intervallet 100-300 ser vi att ett värde som som uppfyller Instruktion 1. kan vara 111, 122, 133, 144 osv, men av dessa är det enbart 133 som uppfyller Instruktion 2 (eftersom att 133 är tredje närmast 100, efter 111 och 122). Det avrundade medelvärdet blir nu (1+3+3) / 3 ≈ 2, enligt Instruktion 3, och svaret på frågan är således 2.

## Problem 5
Efter pingis-rasten kallar plikten och det är dags att gå tillbaka till det dagliga arbetet. Efter ett litet tag har du fått upp ett bra flow, något du gärna inte avbryter allt för mycket, men chefen har nu gett dig i uppgift att gå till varje enskild medarbetare för att få deras underskrift på ett födelsedagsgratulationskort som ska ges till en av kontorets många hundar. Du vill inte spilla alltför mycket tid på detta, så du tänker att det snabbaste är att planera ut den mest effektiva rutten för att samla in dessa underskrifter, baserat på avstånden mellan skrivborden. Du kan börja och sluta hos vilken person du vill, men du måste besöka varje skrivbord exakt en gång. Vad är det kortaste avståndet (i meter) du kan röra dig på och ändå besöka alla kollegor?

#### Exempelvis:
* Avståndet från A till B är 6
* Avståndet från A till C är 5
* Avståndet från B till C 2

De möjliga rutterna blir nu
* A -> B -> C = 6 + 2 = 8
* A -> C -> B  = 5 + 2 = 7
* B -> C -> A = 2 + 5 = 7
* B -> A -> C = 6 + 5 = 11
* C -> B -> A = 2 + 6 = 8
* C -> A -> B = 5 + 6 = 11

Den kortaste rutten är således 7 m.

Dina avstånd hittar du [här](https://gist.githubusercontent.com/kavailis/4710b5a3b42eddf20de753e47ba61394/raw/bf57b2981634a21866aad6146974167215d1a8b4/gistfile2.txt)
