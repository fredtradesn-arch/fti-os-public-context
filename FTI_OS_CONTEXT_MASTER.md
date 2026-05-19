# FTI OS — CONTEXT MASTER

Version : 3.0
Date : 2026-05-18
Statut : ACTIF

---

# MOT DE REPRISE

N8_suite_11

---

# DOCTRINE FTI OS

"La gouvernance survivra aux outils."
Les règles > les outils. Le protocole > l'action. La validation humaine > l'automatisation.

---

# ARCHITECTURE 3 COUCHES

## COUCHE 1 — DROPBOX
Dropbox = vérité documentaire maître.

## COUCHE 2 — ODOO
Odoo = gouvernance opérationnelle.

## COUCHE 3 — IA + AUTOMATISATION
Claude + n8n + ChatGPT. Validation humaine obligatoire.

---

# RÈGLES IMMUTABLES

- AUCUN archivage sans validation Frédéric
- AUCUN renommage sans validation Frédéric
- Scripts : lecture seule / try/except / aucune clé API en clair

---

# PHASES FTI OS

Phase 1 — Naming : TERMINÉE
Phase 2 — Audits simples : TERMINÉE
Phase 3 — Dossiers lourds : EN COURS
  - 2026_KEBO_GROUP_GLOBAL
  - 2026_CAMNEDIS_GUINEA_GOLD_FTI
  - 2026_GOLD_NETWORK_CONGO ← TEMPLATE v2.1 VALIDÉ ✅

---

# MILESTONES 2026-05-18

## AMARYACO ✅
- Commit 636773a | Doc ID 2868 | CRM ID 2973
- Dossier 07_CHAÎNE_BANCAIRE | WAITING_CLIENT_SIGNATURE

## TEMPLATE v2 ✅
- Commit 4b9d413 | Tag FTI_OS_TEMPLATE_v2

## TEMPLATE v2.1 ✅ ACTUEL
- Commit 5997aba | Tag FTI_OS_TEMPLATE_v2.1
- N06 alwaysOutputData / N12 mail.message/create / limit:1 CRM

## GOLD NETWORK CONGO ✅ FULLY VALIDATED
- Lead ID 2966 | Folder ID 1013 (04_COMMUNICATION)
- N09 CreateDoc : SUCCESS
- N10 SearchCRM : Lead 2966 trouvé
- N12 PostChatter : mail.message/create SUCCESS
- Phrase : FTI OS — GOLD TEMPLATE v2.1 — ODOO JSON/2 + CHATTER MAIL.MESSAGE CREATE — VALIDATED

---

# RÉFÉRENCE TECHNIQUE JSON/2 — DÉFINITIVE

## Endpoints validés
- POST /json/2/documents.document/search_read
- POST /json/2/documents.document/create
- POST /json/2/crm.lead/search_read
- POST /json/2/mail.message/create

## Endpoints abandonnés
- /web/dataset/call_kw → 404
- /json/2/documents.folder → 404
- crm.lead/message_post → erreur singleton

## Body create document
{ "vals_list": { "name": "...", "type": "url", "url": "...", "folder_id": X } }
Retour {} = SUCCESS ✅

## Body chatter
{ "vals_list": [{ "model": "crm.lead", "res_id": X, "body": "...", "message_type": "comment" }] }
Retour {} = SUCCESS ✅

## Pièges n8n
- Using JSON + ={{ }} → erreur → utiliser RAW
- 0 items → stoppe → Always Output Data = true sur N06
- limit:1 obligatoire sur CRM search
- N07 context-loss → fix temporaire → refactor v2.2

---

# REPO GITHUB

fredtradesn-arch/fredtrade-ai-infrastructure
  workflows/FTI_OS_DROPBOX_TO_ODOO_CRM_v1.json           (636773a)
  workflows/FTI_OS_DROPBOX_TO_ODOO_CRM_TEMPLATE_v2.json   (4b9d413)
  workflows/FTI_OS_DROPBOX_TO_ODOO_CRM_TEMPLATE_v2.1.json (5997aba) ← ACTUEL
  docs/FTI_OS_CONTEXT_MASTER.md                           (e5e1ab7)

fredtradesn-arch/fti-os-public-context
  FTI_OS_CONTEXT_MASTER.md ← CE FICHIER (démarrage Claude)

---

# BACKLOG v2.2

- N07 refactor context propre sans hardcoded token
- authHeader dynamique partout
- Clean payload builders dans N02
- Test end-to-end production
- Commit + tag FTI_OS_TEMPLATE_v2.2

---

# BACKLOG STRATÉGIQUE

- Liaison Dropbox REF ↔ Odoo project_id
- Liaison Contact partner_id ↔ projets
- Audit factures orphelines
- Politique documentaire Odoo
- Protocole doublon CAMNEDIS

---

# PHRASES CLÉS VERROUILLÉES

FTI OS — Dropbox Master Control
FTI OS — KEBO UAE MASTER INDEX VALIDATED
FTI OS — GOLD v2.1 — MAIL.MESSAGE CREATE — OK
FTI OS — GOLD TEMPLATE v2.1 — ODOO JSON/2 + CHATTER MAIL.MESSAGE CREATE — VALIDATED

---

# RÔLES

Dropbox : vérité documentaire maître
Odoo : gouvernance opérationnelle
Claude : FTI OS — ODOO OPERATOR
ChatGPT : FTI OS — Dropbox Master Control
Frédéric : validation finale systématique

---

# REPRISE

Mot : N8_suite_11
Prochaine : N8_suite_11 — GOLD v2.2 refactor
