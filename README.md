# Giovlab Note

App Android nativa in Kotlin + Jetpack Compose, con interfaccia AMOLED nera e accento verde lime.

## Funzioni incluse
- Creazione, modifica ed eliminazione delle note
- Salvataggio locale persistente con Room/SQLite
- Ricerca per titolo, testo e categoria
- Categorie predefinite: Personale, Lavoro, Idee, Studio
- Campo checklist con una voce per riga (usa `[x]` per indicare una voce completata)
- Allegati immagine tramite selettore di sistema
- Registrazione audio in formato M4A, salvata nella memoria privata dell'app

## Requisiti
- Android Studio recente
- JDK 17
- Android SDK 35
- Connessione internet al primo build per scaricare le dipendenze Gradle

## Avvio
1. Estrai lo ZIP.
2. Apri la cartella `GiovlabNote` in Android Studio.
3. Attendi il completamento della sincronizzazione Gradle.
4. Avvia su un dispositivo o emulatore Android.

## Note
- Le immagini sono memorizzate come URI del selettore Android. Per una versione di produzione è consigliabile copiare gli allegati in uno storage privato dell'app e implementare una strategia di backup.
- La registrazione audio richiede il permesso del microfono.
- Il player audio, le checklist con caselle interattive, cartelle personalizzabili, backup e test automatici sono miglioramenti previsti per una versione successiva.


## Compilazione APK automatica con GitHub Actions
Il repository include `.github/workflows/build-apk.yml`.

1. Crea un repository GitHub vuoto e carica il contenuto di questa cartella sul branch `main`.
2. Apri la scheda **Actions** del repository e abilita i workflow se GitHub lo richiede.
3. Avvia **Build Giovlab Note APK** con **Run workflow** (oppure attendi il build dopo il push).
4. Apri l'esecuzione completata e scarica l'artifact `GiovlabNote-debug-apk`.
5. Estrai l'artifact: contiene `app-debug.apk`.

L'APK debug è adatto a test personali. Per pubblicare sul Play Store serve una build release firmata.
