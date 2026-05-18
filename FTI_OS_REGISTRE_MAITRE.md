# FTI OS — REGISTRE MAÎTRE GOUVERNANCE DOCUMENTAIRE
Version : 1.0
Date : 2026-05-18
Source : Audit global pattern 250/253 — 16 dossiers scannés
Statut : RÉFÉRENCE CENTRALE FTI OS

## RÈGLE SYSTÉMIQUE CONFIRMÉE

250/253/XXX = Dossier UI métier maître (access=edit)
15/1278/XXX = Branche support FTI (access=view)
15/XXX      = Orphan auto Odoo (access=edit, vide)

## TABLEAU MAÎTRE

| Deal | Projet | Doc UI | Score | Doublons | Statut | Risque |
|---|---|---|---|---|---|---|
| KEBO_GROUP_GLOBAL_FTI | 9 | 315 | 20 | 3 | GELÉ | Élevé |
| GOLD_BUYERS_NETWORK_CONGO_FTI | — | 1100 | 16 | 2 | HYBRIDE | Moyen |
| CAMNEDIS_GUINEA_GOLD_FTI | 21/22 | 1074 | 15 | 4 | GELÉ | Élevé |
| AMARYACO_DLC_FTI | 2 | 90 | 9 | 3 | EXCEPTION | Élevé |
| SBLC_MORMAND_500M_FTI | 19 | 157 | 10 | 1 | STABLE | Faible |
| GOLD_SAIKOU_BARRY_FTI | 15 | 258 | 10 | 1 | STABLE | Faible |
| OIL_ISRAEL_INTERTABBACO_FTI | 14 | 305 | 10 | 3 | HYBRIDE | Moyen |
| PRESTATION_MORMAND_185K_FTI | 18 | 168 | 8 | 1 | STABLE | Faible |
| GOLD_NETWORK_CONGO_FTI | 11 | 847 | 8 | 1 | GELÉ | Faible |
| GOLD_NAIROBI_JEANMICHEL_FTI | 13 | 972 | 8 | 3 | HYBRIDE | Moyen |
| PRESTATION_MORMAND_195K_FTI | 17 | 169 | 7 | 1 | STABLE | Faible |
| EN590_TTO_LOME_WARDA_FTI | — | 1082 | 7 | 2 | HYBRIDE | Moyen |
| SOCETE_MINIERE_MANIEMA_FTI | — | 1090 | 7 | 2 | HYBRIDE | Moyen |
| RDC_CORRIDORS_RN7_FTI | 23 | 1222 | 7 | 8 | CRITIQUE | Élevé |
| SUCRE_AVELAN_DAKAR_FTI | 20 | 88 | 6 | 0 | STABLE | Faible |
| SETUP_DUBAI_MORMAND_FTI | 16 | 170 | 6 | 1 | STABLE | Faible |

## STATISTIQUES

Total deals audités : 16
STABLES : 6
GELÉS : 4
HYBRIDES : 5
CRITIQUES : 1 RDC_CORRIDORS 8 doublons

## PRIORITÉS MIGRATION

Phase A — Déjà gelés
KEBO CAMNEDIS GOLD_NETWORK

Phase B — À geler
Priorité 1 : GOLD_BUYERS_NETWORK 1100
Priorité 2 : OIL_ISRAEL 305
Priorité 3 : GOLD_NAIROBI 972
Priorité 4 : AMARYACO 90

Phase C — Audits projets manquants
GOLD_BUYERS WARDA MANIEMA

Phase D — Cas critique session dédiée
RDC_CORRIDORS 8 doublons imbrication KEBO

## EXCEPTIONS VALIDÉES

1 AMARYACO point dans le nom conservé
2026_AMARYACO_DLC_2.249M_USD_FTI
Decision 2026-05-18 Frederic

## RÈGLES FTI OS v4

1. Toujours utiliser 250/253 comme référence UI
2. Nouveaux deals créés sous 03_DEALS ID 253
3. Orphans 15/XXX archivés après validation Frédéric
4. Branches 15/1278/XXX ne reçoivent pas de nouveau contenu
5. RDC_CORRIDORS session dédiée obligatoire

La gouvernance survivra aux outils.
FTI OS Fredtrade Senegal v1.0 2026-05-18
