# Générateur Alerte Info

Outil web pour créer des visuels d’actualité aux formats Facebook, Instagram et statut WhatsApp : douze modèles (Alerte, Bandeau, Une, Citation, Chiffre, Surligné, Duo, Dossier, Post, Carte, Flash, Cadre), identité du média, légende prête à copier, export JPG en 1080 px et vidéos MP4.

## Assistant de rédaction

Colle un texte brut (article, communiqué, post, message) : l’assistant le résume, choisit le modèle, propose trois titres, remplit le visuel, rédige la légende (en arabe aussi, sur demande) et liste les points à vérifier avant de publier. Il lit aussi les captures jointes : un document part dans le modèle Dossier, une photo va sur le visuel.

- Sans clé : mode simple, qui découpe le texte avec des règles, sans IA. Tout reste dans le navigateur.
- Avec une clé API Claude (Réglages de l’assistant) : Claude rédige. La clé est gardée dans le navigateur de l’appareil et n’est envoyée qu’à l’API d’Anthropic, avec le texte et les captures à analyser.

## Post

Le modèle Post met une déclaration en forme de publication de réseau social : photo de profil ronde, nom, badge certifié en option, identifiant et texte avec ses paragraphes, sur fond clair ou sombre. La photo de profil reste sur l’appareil pour les posts suivants.

## Carrousel

Un sujet long devient une série d’images : la couverture, puis des pages texte, citation ou chiffre, et une page d’abonnement. L’assistant écrit ces pages en même temps que le visuel. Sur téléphone, on les fait défiler du doigt dans l’aperçu, et Partager les envoie toutes d’un coup à Facebook, Instagram ou WhatsApp.

## Vidéo

- Habiller une vidéo : la vidéo importée prend la place de la photo, le titre, l’étiquette, le logo et la signature restent posés dessus. On choisit le début, la fin (jusqu’à 20 minutes), l’image de couverture et le son. Le son des longues vidéos MP4 et MOV est lu par tranches, sans charger la vidéo en mémoire.
- Animer un visuel : sans vidéo, la photo zoome doucement et les éléments entrent l’un après l’autre (6, 10 ou 15 secondes).
- Carrousel en vidéo : toutes les pages à la suite dans une seule vidéo, avec un glissement entre elles.
- En option : titre animé, carton de fin d’abonnement, barre de progression.

La vidéo se fabrique dans le navigateur, image par image (WebCodecs) : les images de la vidéo source sont décodées, habillées puis encodées en MP4 H.264, plus vite que la durée de la vidéo, et le son d’origine est recopié tel quel. Sur un navigateur ancien, l’outil repasse à l’enregistrement en temps réel (MediaRecorder). Rien n’est envoyé sur un serveur.

Site : https://togoimy-hassane.github.io/alerte-info/
