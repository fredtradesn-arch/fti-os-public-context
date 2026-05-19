# FTI OS — CONTEXT MASTER

Version : 2.0
Date : 2026-05-18
Statut : ACTIF

---

# DOCTRINE FTI OS

"La gouvernance survivra aux outils."

Les règles > les outils.
Le protocole > l'action.
La validation humaine > l'automatisation.

---

# ARCHITECTURE 3 COUCHES

## COUCHE 1 — DROPBOX

Dropbox = vérité documentaire maître.

Rôle :
- source documentaire officielle
- structure REF FTI
- aucun doublon massif
- organisation stable

---

## COUCHE 2 — ODOO

Odoo = gouvernance opérationnelle.

Rôle :
- workflow
- métadonnées
- CRM
- tâches
- traçabilité
- indexation

---

## COUCHE 3 — IA + AUTOMATISATION

Claude + n8n + ChatGPT.

Rôle :
- audit
- proposition
- automatisation contrôlée
- validation humaine obligatoire

---

# RÈGLES IMMUTABLES

## Archivage

AUCUN archivage sans :
- audit chatter
- audit tâches
- audit documents
- audit dates
- validation Frédéric

## Renommage

AUCUN renommage sans :
- vérification Dropbox
- REF contact
- tâches liées
- CRM lié
- automatisations n8n
- validation Frédéric

## Scripts

Tous les scripts :
- lecture seule par défaut
- défensifs try/except
- continuité même si erreur
- aucune clé API en clair

---

# FRAMEWORK AUDIT V3 [FIGÉ]

Sections :
1. Projet
2. Tâches
3. Chatter
4. Followers
5. Documents
6. Facturation élargie
7. Rapport risques

Statut :
FIGÉ — ne plus modifier sans validation.

---

# PHASES FTI OS

## Phase 1 — Naming Governance

STATUT : TERMINÉE

## Phase 2 — Audits simples

STATUT : TERMINÉE

Projets validés :
- 2026_GOLD_SAIKOU_BARRY_FTI
- 2026_SUCRE_AVELAN_DAKAR_FTI
- 2026_OIL_ISRAEL_INTERTABBACO_FTI
- 2026_SBLC_MORMAND_500M_FTI
- 2026_SETUP_DUBAI_MORMAND_FTI
- 2026_PRESTATION_MORMAND_185K_FTI
- 2026_PRESTATION_MORMAND_195K_FTI

---

# PHASE 3 — DOSSIERS LOURDS

À traiter :
- 2026_KEBO_GROUP_GLOBAL
- 2026_CAMNEDIS_GUINEA_GOLD_FTI
- 2026_GOLD_NETWORK_CONGO ← TEST TEMPLATE v2.1 EN COURS

---

# MILESTONE SESSION 2026-05-18

## Workflow AMARYACO — VALIDÉ
- Commit : 636773a
- Deal   : 2026_AMARYACO_DLC_2.249M_USD_FTI
- Doc ID Odoo : 2868
- CRM ID : 2973
- Dossier : 07_CHAÎNE_BANCAIRE
- Statut  : WAITING_CLIENT_SIGNATURE

## Template ENGINE v2 — COMMITTÉ
- Commit : 4b9d413
- Tag    : FTI_OS_TEMPLATE_v2
- Fichier : workflows/FTI_OS_DROPBOX_TO_ODOO_CRM_TEMPLATE_v2.json

## Template ENGINE v2.1 — FIXES CRITIQUES — ACTUEL
- Commit : 5997aba
- Tag    : FTI_OS_TEMPLATE_v2.1
- Fichier : workflows/FTI_OS_DROPBOX_TO_ODOO_CRM_TEMPLATE_v2.1.json
- Fixes  :
  - N06 : alwaysOutputData = true
  - N12 : mail.message/create (plus crm.lead/message_post)
  - N12 : vals_list sans subtype_xmlid
  - N10 : limit:1 forcé
  - n8n : RAW pour expressions

---

# RÉFÉRENCE TECHNIQUE ODOO JSON/2

## Endpoints validés
- POST /json/2/documents.document/search_read
- POST /json/2/documents.document/create
- POST /json/2/crm.lead/search_read
- POST /json/2/mail.message/create

## Endpoints abandonnés
- /web/dataset/call_kw → 404
- /json/2/documents.folder → 404
- crm.lead/message_post → erreur singleton

## Auth
- Authorization: Bearer TOKEN
- Content-Type: application/json

## Body chatter validé
POST /json/2/mail.message/create
{
  "vals_list": [{
    "model": "crm.lead",
    "res_id": <leadId>,
    "body": "<HTML>",
    "message_type": "comment"
  }]
}

## Body create document validé
POST /json/2/documents.document/create
{
  "vals_list": [{
    "name": "<docName>",
    "type": "url",
    "url": "<dropboxUrl>",
    "folder_id": <folderId>
  }]
}

## Pièges n8n
- Using JSON + ={{ }} → erreur → utiliser RAW
- 0 items → n8n stoppe → Always Output Data = true sur N06
- Merge node bloque si branche vide → éviter
- Noms variables : token/docName/dealName (pas jeton/Nom du document)

---

# REPO GITHUB

fredtradesn-arch/fredtrade-ai-infrastructure

workflows/
  FTI_OS_DROPBOX_TO_ODOO_CRM_v1.json          (636773a)
  FTI_OS_DROPBOX_TO_ODOO_CRM_TEMPLATE_v2.json  (4b9d413)
  FTI_OS_DROPBOX_TO_ODOO_CRM_TEMPLATE_v2.1.json (5997aba) ← ACTUEL

---

# TEST EN ATTENTE

DEAL  : 2026_GOLD_NETWORK_CONGO_FTI
DOC   : 2026-05-18_FTI_TEMPLATE_V2_TEST_GOLD_NETWORK.pdf
URL   : https://www.dropbox.com/
DOSSIER : 04_COMMUNICATION
STATUS  : TEST_TEMPLATE_V2

EN ATTENTE :
- Rotation token Odoo (révocation e42dbe1f...)
- 5 outputs n8n : N02/N06/N09/N10/N12
- GO/NO-GO template v2.1

---

# BACKLOG STRATÉGIQUE

- Liaison Dropbox REF ↔ Odoo project_id
- Liaison Contact partner_id ↔ projets
- Audit factures orphelines
- Politique documentaire Odoo
- Protocole doublon CAMNEDIS
- Rotation token Odoo ← PRIORITAIRE

---

# MOT DE REPRISE

N8_suite_10

---

# FICHIERS STRATÉGIQUES

- FTI_OS_DOCTRINE.md
- FTI_OS_AUDIT_LOG.md
- fti_audit_v3.py
- fti_rename_controlled.py
- workflows/FTI_OS_DROPBOX_TO_ODOO_CRM_TEMPLATE_v2.1.json ← MOTEUR ACTUEL

---

# RÔLES

Dropbox :
vérité documentaire maître

Odoo :
gouvernance opérationnelle

Claude :
audit + exécution contrôlée

ChatGPT :
mémoire stratégique + architecture

Frédéric :
validation finale systématique

---

# PHRASES CLÉS

ChatGPT :
FTI OS — Dropbox Master Control

Claude :
FTI OS — ODOO OPERATOR

Reprise :
N8_suite_10
