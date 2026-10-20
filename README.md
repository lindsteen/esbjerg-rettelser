# Rettelser til Esbjerg-sitet

Oversigt over designafvigelser på https://esbjerg.rodekors.dk/ i forhold til Figma-designet for lokalafdelingssites, med status (To do, Doing, Done) for hvert punkt.

- Siden: `index.html` (statisk, serveres af GitHub Pages)
- Skærmbilleder fra Figma: `img/`
- Status gemmes i Firebase Firestore (projekt `rettelserlokalsites`, samlingen `status`, ét dokument pr. punkt)
- Sikkerhedsregler: `firestore.rules`

## Opdatér sikkerhedsreglerne

Reglerne skal ligge i Firebase, før siden kan læse og gemme status:

1. Åbn https://console.firebase.google.com/project/rettelserlokalsites/firestore/rules
2. Erstat indholdet med teksten fra `firestore.rules`
3. Klik **Publish**

Tilføjes der nye punkter i `index.html`, skal deres id også tilføjes i listen i `firestore.rules`.
