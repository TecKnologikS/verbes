# verbes

Site de l'app iOS **Verbes Irréguliers** (« Irregular Verbs », App Store ID 1579375000) : page de présentation, URL de confidentialité et de support demandées par l'App Store, conditions d'utilisation et mentions légales. Ticket Plane `VIA-34`.

Site statique publié avec GitHub Pages sur `verbes.tecknologiks.com` (workflow `.github/workflows/pages.yml`, à chaque push sur `main`). Seuls les fichiers `*.html`, `assets/`, les dossiers de langue (`fr`, `de`, `es`, `it`, `pt`) et `CNAME` sont publiés. Ce dépôt est la source du site.

Langues : anglais à la racine, puis `fr/`, `de/`, `es/`, `it/`, `pt/`. Chaque page a un sélecteur de langue vers la même page dans les 5 autres langues, et les balises `hreflang` correspondantes. Tutoiement dans toutes les langues, comme dans l'app ; portugais européen (« tu », « telemóvel »), comme les catalogues de l'app. Les libellés cités (« Restaurer l'achat », « Confidentialité des pubs »…) sont ceux des `.xcstrings` de l'app.

| Page | EN (racine) | FR | DE | ES | IT | PT | URL à déclarer |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Présentation : lien App Store, « gratuit avec achat unique sans pub », prix | `index.html` | `fr/index.html` | `de/index.html` | `es/index.html` | `it/index.html` | `pt/index.html` | App Store Connect → *Marketing URL* (optionnel) |
| Politique de confidentialité | `privacy.html` | `fr/confidentialite.html` | `de/datenschutz.html` | `es/privacidad.html` | `it/privacy.html` | `pt/privacidade.html` | App Store Connect → *Privacy Policy URL* (une par langue de la fiche) ; AdMob → paramètres de l'app si demandé |
| Support : contact + FAQ (restaurer l'achat, rappels, prononciation, langue) | `support.html` | `fr/support.html` | `de/support.html` | `es/soporte.html` | `it/supporto.html` | `pt/suporte.html` | App Store Connect → *Support URL* |
| Conditions : EULA standard d'Apple + règles de l'achat unique | `terms.html` | `fr/conditions.html` | `de/nutzungsbedingungen.html` | `es/condiciones.html` | `it/termini.html` | `pt/termos.html` | Optionnel (pas d'abonnement) |
| Mentions légales (LCEN, site édité en France) | `legal.html` | `fr/mentions-legales.html` | `de/impressum.html` | `es/aviso-legal.html` | `it/note-legali.html` | `pt/aviso-legal.html` | — |

Identité visuelle reprise de l'app (thème « Cahier », `iosApp/iosApp/Design/` du dépôt de l'app) : papier, lignes bleues, trait rouge de marge, Caveat pour les titres, police système pour le texte, code couleur des trois formes ; mode clair et sombre avec les valeurs de `Palette.swift`. La police Caveat est auto-hébergée (`assets/fonts`, licence OFL incluse) : le site ne charge aucune ressource externe, n'exécute aucun script et ne dépose aucun cookie, ce que dit la politique de confidentialité.

## À compléter avant publication

Chaque champ est marqué `[À compléter : …]` (fond orange) dans les pages, dans les 6 langues.

- [x] Éditeur et contact : TecKnologikS, support@tecknologiks.com, comme le site de Trente30 (sans adresse, téléphone ni SIREN).
- [ ] Dates de mise à jour (confidentialité, conditions).
- [ ] Prix de « Supprimer les pubs » (présentation).
- [ ] Base légale des pubs non personnalisées (confidentialité section 4) : décision à valider.
- [ ] Section « Enfants » de la confidentialité : public visé, âge minimum, classement d'âge App Store, traitement des pubs pour les mineurs (réglages AdMob) : décision à valider.
- [ ] Nom de l'app dans chaque langue : le site dit « Irregular Verbs » en anglais, allemand, espagnol, italien et portugais, et « Verbes Irréguliers » en français. Vérifier les noms des fiches App Store localisées.
- [ ] Badge officiel « Download on the App Store » d'Apple (règles marketing d'Apple, fichier à héberger dans `assets/`) à la place du bouton texte.
- [ ] Portugais : le chemin des réglages de suivi d'iOS est donné de façon générale (« Definições do iOS, em Privacidade e segurança ») faute de libellé exact vérifié.

## À garder à jour

La politique de confidentialité décrit le fonctionnement réel de l'app 3.0 (vérifié dans le code le 19/11/2026) : pubs Google AdMob avec consentement UMP puis ATT, aucune pub pour l'acheteur « sans pub », achat StoreKit 2, notifications locales, synthèse vocale de l'appareil, données d'apprentissage sur l'appareil (Core Data, UserDefaults), sans compte, sans serveur, sans iCloud, sans analytics ni crash reporting. Toute évolution qui touche aux données (nouveau SDK, analytics, crash reporting, synchronisation iCloud, compte, nouvel emplacement de pub, app Android…) doit être reportée ici **dans les 6 langues avant** sa mise en ligne, ainsi que dans la fiche « Confidentialité » d'App Store Connect.

La FAQ du support cite des libellés et des réglages de l'app (heure du rappel par défaut 18 h, langues proposées, emplacements des pubs) : à mettre à jour s'ils changent.

Ces textes sont une base rédigée à partir du code ; ils ne remplacent pas un avis juridique.
