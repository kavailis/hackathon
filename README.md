# Hackathon - Eventkväll

Ni ska nu ger er på att försöka lösa fem olika programmeringsuppgifter. Outputen av varje löst problem ger en siffra, där de samlade lösningarna tillsammans ger en sifferkombination som motsvarar alfabetiska positioner. Givet dessa motsvarande bokstäver ska ni nu komma fram till korrekt ord som sökes. Exempelvis: Siffran 1 motsvarar bokstaven A, siffran 24 motsvarar bokstaven X. Bonus ges till de grupper som skriver både effektiv och läsbar kod!

Ni får lösa det i vilket programmeringsspråk ni vill, men vi uppmuntrar er till att använda Python då det är det vi kodar i!

Ord som sökes: 

## Problem 1
Ibland kan posten ha svårt att hitta till Violets adress, Linnégatan 87A, när de ska leverera paket. Mer specifikt har de ofta svårt att hitta vilken våning vi är på. posten har därför börjat med ett internt system för att lista ut vilken våning de ska leverera till, men brevbärarna tycker att instruktionerna är lite oklara. När de levererar ett paket börjar de på våning 0 och sedan följer instruktionerna en karaktär i taget. Ett plustecken, +, betyder att de ska upp en våning, ett minustecken, -, betyder att de ska ned en våning.

Exempelvis: 
++-- och +-+- båda resulterar i våning 0
+-- och --+ båda resulterar i våning -1 (källaren)
++++--+ resulterar i våning 3

Vilken våning ska posten leverera till?

Er input är finns här: https://gist.githubusercontent.com/kavailis/4710b5a3b42eddf20de753e47ba61394/raw/bf57b2981634a21866aad6146974167215d1a8b4/problem_1
