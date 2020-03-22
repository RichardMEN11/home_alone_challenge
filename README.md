# home_alone_challenge

> My hunky-dory Nuxt.js project

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).

## Design
> :warning: **Mobil**: das Design ist hier weitgehend noch nicht für mobil umgesetzt!

## Pages
Folgende Seiten sind noch nicht vollständig umgesetzt.
Daher folgt hier vorwiegend eine Beschreibung der Inhalte für die einzelnen Seiten.

### Index/Landingpage
pages/index.vue
- Login
- Beschreibung der Website/Zweck
- Anleitung für neue Nutzer für leichteren Einstieg

### Login
pages/login.vue

### Registrierung
pages/sign-up.vue

### Challenge Index -> Meine Challenges
pages/challenges/index.vue
- soll meine Challenges anzeigen (von mir erstellt und teilgenommene)
- neue Challenge erstellen

### Challenge Detail-Seite
pages/challenges/details.vue
- beschreibt eine einzelne Challenge
- Kommentare für die angezeigte Challenge
- Teilnahme an der Challenge starten
- Challenge liken

### Profil
pages/profile/index.vue
- Ranking? Punktzahl?
- Link zu Einstellungen

### Einstellungen
pages/profile/settings.vue
- Accounteinstellungen, wie man sie auch von anderen Websiten kennt
- z.B. Passwort ändern, Nutzernamen ändern, Benachrichtigungen einstellen


## Components
Die Vue Components liegen im Ordner components.

### allgemeine Seitenelemente
- Header (Nav.vue)
- Logo (Logo.vue)
- Footer (Footer.vue)

### Authentifizierung
- Formular zum Login (authentification/LoginForm.vue)
- Formular zum Registrieren (authentification/SignUpForm.vue)

### Challenge-Elemente
- Preview einer Challenge (ChallengeCard.vue)
- Ausführliche Beschreibung einer einzelnen Challenge (challenges/ChallengeDetails.vue)
- Liste einer von Teilnehmern (challenges/ParticipantsList.vue)

#### Kommentarfunktion
- Kommentar hinzufügen (comments/AddCommentItem.vue)
- Darstellung eines einzelnen Kommentars (comments/CommentItem.vue)

### Nutzer
- Darstellung eines Nutzerbilds (Avatar.vue)

## Anbindung ans Backend
Die Anbindung an das [Backend](https://github.com/ps100000/WirVsVirus) wurde bisher noch nicht implementiert.
