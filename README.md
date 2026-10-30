# GiovLab Note

App Android per note, in Kotlin con Jetpack Compose, Material 3 e Room.

## Funzioni
- Note di testo e checklist (convertibili in entrambe le direzioni)
- Stile minimale monocromatico; colore della nota come piccolo punto
- Etichette: assegnazione dall'editor, filtro nella home, rinomina ed eliminazione
- Ricerca su titolo, testo, elementi checklist ed etichette
- Fissa in alto, condividi come testo, elimina con "Annulla"
- Salvataggio automatico (anche quando l'app va in background)
- Backup: esporta e importa un file JSON dal menu ⋮ della home.
  L'importazione non crea duplicati: una nota già presente viene aggiornata.

## Struttura
```
app/src/main/java/com/giovlab/note/
├── MainActivity.kt          navigazione
├── data/                    Room, modello, conversioni JSON, backup
└── ui/                      schermate, ViewModel, tema e colori
```

## Avvio
Apri la cartella in Android Studio, attendi la sincronizzazione Gradle e premi Run.
Requisiti: JDK 17, Android 8.0+ (minSdk 26).
