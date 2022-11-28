# Violet Hackathon Pre-MTD 2022

Välkomna! Ni ska nu ger er på att försöka lösa *fem* olika programmeringsuppgifter. Svaret till de fyra första problem ger en eller flera siffor, beroende på antal inputs. Spara undan siffrorna, ni kommer att behöva samtliga till sista problemet. Ni har 1.5 h på er. Lycka till!

*Ni får lösa uppgifterna i vilket programmeringsspråk ni vill, men vi uppmuntrar er till att använda Python eller JavaScript då de är de vanligaste språken vi på Violet kodar i. Eloge ges till de grupper som skriver läsbar och samtidigt effektiv kod! Ni får dessutom givetvis ställa oss frågor och använda Google. :)*

## Problem 1
Ibland kan posten ha svårt att hitta till Violets adress när de ska leverera paket. Mer specifikt har de svårt att hitta vilken våning vi är på. Posten har därför börjat med ett internt system för att lista ut vilken våning de ska leverera till, men brevbärarna tycker att instruktionerna är lite oklara. Instruktionerna säger att när de levererar ett paket ska de börja på våning 0 och sedan följa instruktionerna en karaktär i taget. Instruktionerna innehåller enbart en massa plus- och minustecken. Ett plustecken, **+**, betyder att de ska upp en våning, ett minustecken, **-**, betyder att de ska ned en våning.

#### Exempelvis: 
* ++-- och +-+- resulterar båda i våning 0
* +-- och --+ resulterar båda i våning -1 (källaren)
* ++++--+ resulterar i våning 3

Vilken våning ska posten leverera till?

Era input är finns [här](https://gist.githubusercontent.com/kavailis/4710b5a3b42eddf20de753e47ba61394/raw/e660ed6153a3c4781bff29f9070b1db3d334bc6d/problem_1.txt).


## Problem 2
Posten lyckades hitta till Violet men nu kvarstår nästa utmaning: Att hitta till rätt rum! Det öppna kontorslandskapet till trots kan det vara svårt att hitta till de mindre, inglasade, rummen. Posten har dock listat ut ett sätt att ta sig till rätt rum, via ett dokument innehållandes en lista av möjliga fyrkanter, där ett gömt svar ger siffran till vilket rum som brevbäraren ska ta sig till. 

För att en fyrkant ska vara möjlig måste summan av alla vinklar av fyrkant vara lika med 360. Exempelvis ger vinklarna 180, 180, 60, 60 inte en fyrkant, eftersom att 180+180+60+60 = 480 =/= 360. Däremot ger vinklarna 100, 80, 150, 30 en fyrkant, då 100+80+150+30 = 360.

Givet [dessa listor](https://gist.githubusercontent.com/kavailis/4710b5a3b42eddf20de753e47ba61394/raw/776682304af2657382810f0fb23a66b8d221cf65/problem_2.txt) lista, räkna ut hur många av de listade vinklarna som ger en fyrkant.

## Problem 3
Äntligen har posten lyckats leverera till rätt rum hos Violet! Kan ni gissa vad paketet innehåller? That’s right, en mining-rig. Nu är det dags för Violet att bryta sina egna Violetcoins! Violetcoins bryts på ett annorlunda sätt jämfört med andra typer av kryptovalutor, nämligen genom att räkna ut medelvärdet av checksummor. Ni har fått ett tabulerat dokument med rader beståendes av till synes slumpmässiga tal, detta dokument ska ni nu använda till att lösa ut medelvärdet av checksumman. Hur får man då ut en checksumma? Jo, för varje rad i dokumentet ska ni ta reda på skillnaden mellan den största och lägsta siffran - checksumman fås av summan av alla dessa skillnader.

#### Exempelvis: 
Givet följande tabell:

3 8 11 9

2 1 0 6

4 7 1 12

* Den första radens största och lägsta siffra är 11 respektive 3, skillnaden mellan dessa är 8
* Den andra radens största och lägsta siffra är 6 respektive 0, skillnaden mellan dessa är 6
* Den tredje radens största och lägsta siffra är 12 respektive 1, skillnaden mellan dessa är 11

Checksumman för exempeltabellen blir 8+6+11 = 25, medelvärdet blir då avrundat till 8.

Vad blir medelvärdet av checksumman för [dessa](https://gist.githubusercontent.com/kavailis/4710b5a3b42eddf20de753e47ba61394/raw/2e6e22382a82e91b854d1a74534192a454b14ba4/problem_3.txt) rader? Avrunda till närmaste heltal om det behövs.

## Problem 4

Innan ni börjar här hos Violet så måste ni ju såklart bli klara med era studier, det innebär även alla era mattekurser. Sista frågan på Vektorn är skillnaden mellan ett U och en examen. Men! Som tur är så har svaret på sista frågan på Vektorn samma värde som svaret på detta problem!

Så, givet alla mattekurser och deras respektive kurskoder nedan, ska ni nu tillämpa ett par regler för att få ut korrekt svar:

#### Kurskoder
| Kursnamn | Kurskod |
| :--------- | :----------- |
| Matematisk Grundkurs | TNA001 |
| Linjär Algebra | TNA002 |
| Analys I | TNA003 |
| Analys II | TNA004 |
| Tillämpad matematik i teknik och naturvetenskap | TNA005 |
| Analys III | TNA006 |
| Vektoranalys | TNA007 |
| Tillämpad Transformteori | TNG032 |

#### Regler
- För varje kurs &rarr; k = kursnamn / kod 
- Kursnamn = summan av bokstavsvärdena (a = 0, b = 1..)
- Om bokstaven är en versal blir värdet fördubblat (A = 0, B = 2, C = 4..)
- Om bokstaven är på udda position relativt till en merge:ad sträng av alla kursnamn så blir "bokstav = -bokstav", 
dvs: "Matematisk GrundkursLinjär AlgebraAnalys IAnalys II..." där "M" = jämn, "a" = udda, osv 
- Vi räknar mellanslag som "bokstav/char" och mellanslag har värdet = -1

Vi har då att svaret till sista tentafrågan blir => (k0+k1+k2...) **-** 84
### Exempelvis: 
| Kursnamn | Kurskod |
| :--------- | :----------- |
| Philip | NGO003 |
| Kevin | MTD001 |


&rarr; 
Merged: "PhilipKevin"

k0 = (2\*15+7-8+11-8+15) / 3 = 15,6666666667

k1 = (-2\*10+4-21+8-13+21) / 1 = -21

&rarr; (k0 + k1) - 84 = (15,6666666667 + -21) - 84 = -89,3333333333

Svar: -89

Vad är svaret på sista tenta frågan?


## Slutuppgift
Om ni har löst alla problem har ni fått ut 7 st siffror. Varje siffra mostvarar ett ord i en lista, som ni finner nedan, där siffran är ordets index i listan. Givet dessa ord ska ni nu komma fram till korrekt frågeställning som sökes. När ni kommit fram till en frågeställning så meddela oss!

Listan hittar ni [här](https://gist.githubusercontent.com/kavailis/4710b5a3b42eddf20de753e47ba61394/raw/036e09d2ca756bd7c2af3c243bb8e25017e7ce72/slutuppgift.txt).


