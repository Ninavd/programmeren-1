# Oefententamen

Hieronder vind je vier opdrachten van verschillende niveaus (bij het tentamen zijn dit er vijf). Om het tentamen te halen moet je één werkend programma van het eerste niveau inleveren en twee werkende programma's van het tweede niveau.

Het doel is te demonstreren dat je zelfstandig een oplossing voor een probleem kunt ontwikkelen, en daarbij gebruik kunt maken van de basistechnieken van programmeren in C, zoals bijvoorbeeld de verschillende soorten loops, if-else-constructies, enzovoort.

Vanwege dit doel heeft het geen zin om alleen het juiste antwoord uit te printen zodat `check50` tevreden is (het zogenaamde "hardcoden"). Het is daarom ook aan te raden om zoveel mogelijk van de opdrachten te doen, mits de tijd dit toelaat. Dat geeft ruimte als je onbedoeld een antwoord hebt ge-hardcode.

## Kaartje in de trein kopen (niveau 1)

Wanneer je vroeger in de trein stapte zonder kaartje betaalde je bij controle door de conducteur een toeslag van 3,50 op de normale ritprijs. Het normale tarief voor de trein bedroeg 20 cent per kilometer. Een creatieve treinreiziger wil een programma hebben waarbij de kans dat hij gecontroleerd wordt (in procenten) en het aantal kilometers dat zijn treinreis lang is opgegeven kunnen worden, waarna de computer berekent hoeveel deze reiziger betaalt en hoeveel dit procentueel is van het bedrag dat een reiziger met kaartje moet betalen. Schrijf dit programma voor deze treinreiziger.

    $ ./trein
    Hoeveel kilometers ga je rijden? 100
    Wat is de kans dat je wordt gecontroleerd in procenten? 50
    Je betaalt 11.75 euro
    Dit is 59 procent van het normale bedrag

    $ ./trein
    Hoeveel kilometers ga je rijden? 20
    Wat is de kans dat je wordt gecontroleerd in procenten? 75
    Je betaalt 5.63 euro
    Dit is 141 procent van het normale bedrag

> Let op, alle resultaten moeten goed worden afgerond en euro's mogen niet meer dan twee decimalen na de komma worden geprint.



## Babysitten (niveau 1)

Babysitten is tegenwoordig een lucratief bijbaantje. Wanneer babies zich koest houden kun je lekker studeren zonder te worden afgeleid en je krijgt er nog voor betaald ook. Marieke krijgt vóór 12 uur ‘s nachts een vergoeding van 6 euro per uur en ná middernacht wordt dat 10. De mensen waar ze op de kleine kinderen past zijn soepel en ronden de tijd dat ze heeft opgepast op een vriendelijke manier af. Voor de tijd van aankomst nemen ze het laatste hele uur voorafgaand aan de werkelijke tijd van aankomst en de tijd van vertrek ronden ze af op het hele uur naar boven toe. Schrijf een programma waarmee Marieke kan uitrekenen wat ze verdienen zal, gegeven een door de gebruiker ingevoerd begintijdstip (na 7 uur ‘s avonds) en een door de gebruiker ingevoerd eindtijdstip (vóór 3 uur ‘s nachts).

    $ ./babysitten
    Wanneer begon je met babysitten? 1930
    Wanneer was je klaar met babysitten? 0047
    Je verdiende 40 euro

    $ ./babysitten
    Wanneer begon je met babysitten? 2045
    Wanneer was je klaar met babysitten? 0200
    Je verdiende 44 euro

    $ ./babysitten
    Wanneer begon je met babysitten? 2040
    Wanneer was je klaar met babysitten? 2320
    Je verdiende 24 euro

    $ ./babysitten
    Wanneer begon je met babysitten? 0033
    Wanneer was je klaar met babysitten? 0133
    Je verdiende 20 euro


## Holle driehoek (niveau 2)

Schrijf een programma dat een holle driehoek uitprint. De gebruiker mag een hoogte opgeven. Deze hoogte mag niet kleiner dan 5 zijn en niet hoger dan 20.

    $ ./driehoek
    Hoe hoog moet de driehoek zijn? 5
        ##
       #  #
      #    #
     #      #
    ##########

    $ ./driehoek
    Hoe hoog moet de driehoek zijn? 15
                  ##
                 #  #
                #    #
               #      #
              #        #
             #          #
            #            #
           #              #
          #                #
         #                  #
        #                    #
       #                      #
      #                        #
     #                          #
    ##############################


## Temperaturen (niveau 2)

Graden Celsius C en graden Fahrenheit F staan met elkaar in verband via `F = (18C + 320) / 10` en andersom `C = (10F - 320) / 18`. Schrijf een programma dat de gebruiker vraagt om de eenheid van temperatuur, of C van Celsius of F van Fahrenheit. Vervolgens vraagt het programma om de begintemperatuur, de eindtemperatuur en de stapsgrootte. Waarna een nette tabel wordt uitgeprint met op iedere rij de gekozen temperatuur en de temperatuur in de andere eenheid.

Vraag de gebruiker opnieuw om input als er iets anders dan C of F wordt gekozen voor de eenheid van temperatuur. Vraag de gebruiker ook opnieuw om input als er een stapgrootte kleiner dan 1 wordt ingevuld. 

    $ ./temperaturen
    Welke eenheid van temperatuur (C of F)? C
    Wat is de begintemperatuur? 0
    Wat is de eindtemperatuur? 20
    Wat is de stapgrootte? 5
      C |   F
      0 |  32
      5 |  41
     10 |  50
     15 |  59
     20 |  68

    $ ./temperaturen
    Welke eenheid van temperatuur (C of F)? F
    Wat is de begintemperatuur? 0
    Wat is de eindtemperatuur? 10
    Wat is de stapgrootte? 2
      F |   C
      0 | -17
      2 | -16
      4 | -15
      6 | -14
      8 | -13
     10 | -12

    $ ./temperaturen 
    Welke eenheid van temperatuur (C of F)? F
    Wat is de begintemperatuur? 100
    Wat is de eindtemperatuur? 0
    Wat is de stapgrootte? 3
      F |   C

     $ ./temperaturen 
    Welke eenheid van temperatuur (C of F)? c
    Welke eenheid van temperatuur (C of F)? v
    Welke eenheid van temperatuur (C of F)? F
    Wat is de begintemperatuur? 0
    Wat is de eindtemperatuur? 9
    Wat is de stapgrootte? -3
    Wat is de stapgrootte? 0
    Wat is de stapgrootte? 3
      F |   C
      0 | -17
      3 | -16
      6 | -14
      9 | -12

> Tip: zo print je een waarde uit met een vaste lengte `printf("%3d", getal)`. Is `getal` hier bijvoorbeeld `9`, dan worden er twee spaties uitgeprint voor de `9` om zo toch de opgegeven lengte 3 te krijgen.