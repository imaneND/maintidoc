# Journal des prompts – corpus MaintiDoc

## P01
- **Outil :** Claude (Anthropic)
- **Date :** 04/11/2026
- **Auteur :**BIKIKRE RANIA
- **Objectif :** choisir deux familles d'équipements dont la documentation est disponible en ligne avec des licences claires
- **Prompt :** Aidez-nous à trouver un équipement à partir duquel nous allons générer un dataset. Il faut que les fichiers ragde cet équipement soient disponibles, ainsi que sa documentation sur Internet et les licences associées aux fichiers. Guidez-nous pour choisir un domaine afin que nous puissions faire notre choix. 
- **Résultat :** options comparées ; pompes centrifuges et groupes électrogènes diesel retenus ; limites de licence signalées
- **Vérification et corrections :** choix validé par l'équipe
- **Documents concernés :** choix des familles

## P02
- **Outil :** Claude (Anthropic)
- **Date :**  05/11/2026
- **Auteur :** BIKIRE RANIA
- **Objectif :** obtenir les liens des documents publics (manuels DOE) et savoir quoi télécharger
- **Prompt :** Oui, je choisis l’option Pompes centrifuges + groupes électrogènes diesel. Je veux maintenant qu’on prépare une explication claire et structurée de notre choix, afin de pouvoir le présenter et le justifier devant notre professeur.

Tout d’abord, vérifie si les exigences suivantes concernant le corpus sont bien respectées et fournis les liens des documents et de leurs sources.

**Exigences sur le corpus :**
- 30 à 50 documents couvrant deux familles d’équipements (ex. pompes centrifuges et compresseurs, groupes électrogènes et onduleurs, convoyeurs et automates).
- Des types de documents variés : manuels, procédures, fiches de sécurité, schémas, tableaux de codes d’alarme, photographies de panneaux ou de voyants.
- Au moins 10 documents contenant des éléments visuels exploitables (schémas, figures, photos, tableaux) et au moins 2 documents scannés pour tester l’OCR.
- Des documents en français de préférence. Quelques documents en anglais sont acceptés, à condition de les signaler.
- Uniquement des documents publics et réutilisables, avec leurs licences ou conditions d’utilisation vérifiées, ou des documents synthétiques générés par l’équipe. Aucune donnée personnelle réelle.

**Concernant les deux approches proposées dans les consignes :**

1. **Recherche de documents publics :** rechercher des documents sur les sites des fabricants, dans les guides publics et les documentations accessibles en ligne. Chaque lien, son contenu et ses conditions de réutilisation doivent être vérifiés. Un lien proposé par une IA ne doit jamais être considéré comme fiable sans vérification.
2. **Génération de documents synthétiques :** créer des manuels, procédures ou historiques d'interventions fictifs, mais techniquement cohérents, avec des références d'équipements, des codes d'alarme et une pagination. Les schémas peuvent également être dessinés par l'équipe ou générés.

Nous souhaitons privilégier la première approche, c'est-à-dire la recherche de documents publics. Confirme que ce choix est cohérent avec les exigences du projet.

**Important :** respecte strictement toutes les consignes du Livrable 1. Ne suppose rien, n'invente aucune information et n'ajoute pas de parties qui ne sont pas demandées.

Nous voulons avancer étape par étape et comprendre réellement le travail réalisé. Pour chaque choix, explique-nous pourquoi nous l'avons fait, comment nous l'avons fait et sur quels éléments nous nous sommes appuyés. Nous devons être capables de justifier nos décisions et de répondre aux questions du professeur lors de la présentation.

Ne te contente donc pas de produire un livrable prêt à remettre : accompagne-nous dans sa réalisation et assure-toi que nous maîtrisons chaque partie du travail.
- **Résultat :** liste des volumes DOE ; un lien standards.doe.gov invalide ; adresse energy.gov trouvée par l'équipe
- **Vérification et corrections :** lien invalide détecté par l'équipe ; PDF téléchargés manuellement
- **Documents concernés :** ref_doe_meca_vol1, ref_doe_meca_vol2, ref_doe_elec_vol1, ref_doe_elec_vol3, ref_doe_elec_vol4

## P03
- **Outil :** Claude (Anthropic)
- **Date :**   05/11/2026
- **Auteur :** IMANE NADIF
- **Objectif :** analyser les 5 PDF fournis (modules, pages, figures) et produire le plan du corpus et l'inventaire des documents réels
- **Prompt :** Analyse les 5 PDF pour savoir s'ils contiennent bien les deux familles d'équipements choisies.
- **Résultat :** classeur Excel de plan et `inventaire.csv` des 5 documents DOE
- **Vérification et corrections :** contenu des volumes vérifié dans les PDF ; erreurs de l'assistant corrigées (volume des pompes, module Batteries mal attribué)
- **Documents concernés :** ref_doe_*

## P04
- **Outil :** Claude (Anthropic)
- **Date :**  05/11/2026
- **Auteur :** IMANE NADIF
- **Objectif :** rédiger le rapport du livrable 1 et un guide de réalisation
- **Prompt :** Est-ce que tu peux me donner le document docx du rapport prêt à télécharger, qui respecte les consignes du projet et nos choix, avec un contenu de 10 à 15 pages hors annexes, et qui répond à toutes les exigences du Livrable 1 ?
- **Résultat :** brouillons de rapport et de guide
- **Vérification et corrections :** rapport relu et adapté par l'équipe 
- **Documents concernés :** rapport (hors corpus)

## P05
- **Outil :** Claude (Anthropic)
- **Date :**  06/11/2026
- **Auteur :** BIKIKRE RANIA
- **Objectif :** générer les 35 documents synthétiques du corpus (17 famille pompes, 18 famille groupes électrogènes) : manuels, codes d'alarme, procédures, fiches de sécurité, schémas, historiques, images de panneaux, document piégé
- **Prompt :** Est-ce que tu te rappelles encore du contexte? Tu peux commencer à me générer les 35 documents synthétiques comme convenu  Revois le contexte du projet
- **Résultat :** 35 fichiers (31 PDF dont 2 scans simulés, 4 images JPG) ; contradictions voulues : couple du bouchon de vidange pompe A (25 N·m en v1, 35 N·m en v2) et quantité d'huile du groupe C (28 L en v1, 32 L en v2) ; voyants TEMP orange similaires sur la pompe B, les groupes C et D ; note de service contenant une instruction d'injection en page 2
- **Vérification et corrections :** contrôles automatiques de forme et de cohérence passés (voir `scripts/`) 
- **Documents concernés :** tous les documents dont `provenance = synthetique`
