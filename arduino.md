[Intro 1](https://www.youtube.com/watch?v=d8_xXNcGYgo)

### Links
- [TinkerCad Circuits](https://www.tinkercad.com/circuits)

### Downloads

- [Arduino IDE](https://www.arduino.cc/en/main/software#download)


# Opgaver

## 5. september

Start med at åbne TinkerCad Circuits fra linket ovenfor (opret konto eller log ind). I TinkerCad kan man både skrive kode og lave elektriske kredsløb.

Start med at tilføje en Arduino Uno. Klik derefter på `Code Editor`, for at se standardkoden de har tilføjet:
```c
// Pin 13 has an LED connected on most Arduino boards.
// give it a name:
int led = 13;

// the setup routine runs once when you press reset:
void setup() {
  // initialize the digital pin as an output.
  pinMode(led, OUTPUT);
}

// the loop routine runs over and over again forever:
void loop() {
  digitalWrite(led, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);               // wait for a second
  digitalWrite(led, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);               // wait for a second
}
```

### Opgave 1

Som forklaret i videoen vi så sidste gang, består et simpelt Arduino-program af tre sektioner:

#### Globale variable

Her opretter vi de variable vi skal bruge i programmet.
```c
// Pin 13 has an LED connected on most Arduino boards.
// give it a name:
int led = 13;
```

#### Opsætning

Her sætter vi Arduinoen op som vi skal bruge den.  Den øverste række (0-13) af forbindelser (pins) kan bruges enten til at sende strøm ud, eller se om der kommer strøm ind.  Det skal sættes rigtigt op, inden vi bruger dem.

Vi har i de globale variable bestemt at led er pin 13.
```c
// the setup routine runs once when you press reset:
void setup() {
  // initialize the digital pin as an output.
  pinMode(led, OUTPUT);
}
```

#### Programmet

Selve programmet kører i en løkke (loop) og bliver gentaget igen og igen og igen...

Her skriver vi værdien `HIGH` til `led` (som er 13).  `HIGH` betyder også *tændt*.  Dernæst venter vi 1000 milisekunder (1000 milisekunder = 1 sekund).  Så sætter skriver vi værdien `LOW` til `led`, hvilket slukker den igen.  Til sidst venter vi et sekund mere - og så starter løkken forfra.
```c
// the loop routine runs over and over again forever:
void loop() {
  digitalWrite(led, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);               // wait for a second
  digitalWrite(led, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);               // wait for a second
}
```

### Kør programmet

I Code Editor vinduet: Klik på Upload & Run og se at dioden `L` blinker gult på Arduinoen.  Først er den tændt i et sekund, derefter slukket i et sekund.

### Byg elektrisk kredsløb

Klik på `Stop Simulation` og dernæst på `+ Components` og tilføj:

- 1 Breadboard Small
- 1 Resistor (modstand)
- 1 LED (lysdiode)

Sæt dem:

- Modstanden i hullerne `b1` og `-1`
- Lysdioden i hullerne `c1` og `c2`

Træk ledninger ved at klikke på først den ene ende og derefter på den anden ende af:

- `GND` -> `-30`
- `PIN13` -> `a2`

Tænk på at strømmen løber fra `PIN13` til `a2`.  Her løber den ind i lysdioden i `c2`, igennem den, videre til modstanden (for at beskytte lysdioden) og ned til `-1`.  Til sidst løber den fra `-30` tilbage til `GND` (som er minus) på Arduinoen.

Når `PIN13` er tændt kan strømmen løbe og når den er slukket kan strømmen ikke løbe.


### Opgave 2

Tilføj en eller flere lysdioder mere på samme måde og prøv at få dem til at blinke én af gangen på stribe.

### Opgave 3

Følg eksemplet her for at få tilslutte en knap.

[Arduino Tutorial: Button](https://www.arduino.cc/en/Tutorial/Button)
