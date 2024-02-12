# Morse

Schrijf een programma `morse.c` dat een Morse-code vertaald naar tekst en deze uitprint. Morse-code is een systeem dat door middel van korte en lange signalen informatie overbrengt. Korte signalen worden met een punt (.) aangegeven en lange signalen met een streep (-). Een combinatie van strepen en punten kunnen vervolgens staan voor letters of cijfers. Zo is `...---...` het wel bekende SOS.

Voor deze opdracht definiëren we vier combinaties die staan voor de volgende letters:

- ... = S
- --- = O
- -.. = D
- .-. = R

Het programma moet als volgt werken:

    $ ./morse
    Usage: ./morse <code>

    $ ./morse ...---...
    SOS

    $ ./morse -..------.-.
    DOOR

Let op, je mag aannemen dat er altijd een morse-code door de gebruiker wordt ingevoerd die deelbaar is door 3. Ook mag je aannemen dat de gebruiker enkel streepjes en punten invoert.

Als beginpunt kan je deze code gebruiken:

    #include <cs50.h>
    #include <stdio.h>
    #include <string.h>

    int main(int argc, string argv[])
    {
        // TODO
    }

> `argc` & `argv`? Zie de [command-line arguments short](/shorts/argv)