---
title: Sertificēšanas ceļa kļūda, iestatos programmu savienojumu
description: Ja Warehouse Management programma rada kļūdu "Sertificēšanas ceļa drošības enkurs nav atrasts", izmantojiet šo lapu, lai atrisinātu vai novērstu problēmu.
author: ivanv-microsoft
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: WMA
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e4a36874ac4982c9c92a7dcc17c13c7c7c02bf8c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476987"
---
# <a name="trust-anchor-for-certification-path-not-found-when-setting-up-app-connection"></a>Sertificēšanas ceļa drošības enkurs nav atrasts, iestatot programmas savienojumu

## <a name="symptoms"></a>Simptomi

Mēģinot pieslēgties Supply Chain Management, Warehouse Management programma varētu rādīt šādu kļūdas ziņojumu:

> java.security.cert.certPathValidatorException: Sertificēšanas ceļa drošības enkurs nav atrasts.

Šī problēma var ietekmēt ierīces ar šādiem raksturlielumiem:

- **OS versija**: Android 4.4.x (piemēram, Zebra TC55). Šī problēma nepastāv jaunākajās Android versijās.
- **Supply Chain Management atrašanās vieta**: Mākonis
- **Savienojuma režīms**: Klienta slēptās vērtības vai sertifikāts

## <a name="possible-cause"></a>Iespējamais iemesls

Microsoft varētu būt atjaunojuši servera SSL sertifikātus, kurus izmanto Supply Chain Management. Tā rezultātā var tikt mainīts saknes sertifikāts un/vai viens no starpnieku sertifikātiem, tāpēc jaunā sertifikāta nav mobilās ierīces drošo sistēmas sertifikātu sarakstā. Jaunākā Android versija automātiski atjaunina drošo sertifikātu sarakstu, taču Android 4.4.x versija to nedara.

## <a name="resolution"></a>Novēršana

Lai novērstu šo problēmu, veiciet kādu no tālāk norādītajām darbībām:

- Lietojiet norādījumus, kas aprakstīti sadaļā tālāk, lai atjauninātu katru ierīci.
- *Varētu* būt iespējams sazināties ar Zebra vai Google, lai saņemtu sistēmas drošo sertificēšanas iestāžu (CA) sertifikātu atjauninājumu. Taču tas nav apstiprināts.
- Ja iespējams, apsveriet vecāko ierīču aizstāšanu ar ierīcēm, kurās darbojas jaunāka Android versija (kurā droši CA sertifikāti tiek atjaunināti automātiski).

### <a name="workaround"></a>Kļūdas apiešanas risinājums

#### <a name="step-1-export-the-new-root-certificate-from-supply-chain-management"></a>1. darbība: Eksportējiet jauno saknes sertifikātu no Supply Chain Management

Manuāli lejupielādējiet jauno saknes sertifikātu, izmantojot interneta pārlūku un veicot šādas darbības:

1. Piesakieties Dynamics Supply Chain Management un atveriet sākumlapu.

1. Pārlūka adrešu joslā atlasiet slēdzenes ikonu, lai atvērtu dialoglodziņu **Atrašanās vieta ir droša**.
1. Dialoglodziņā atlasiet **Sertifikāts (derīgs)**, lai atvērtu sertifikāta logu **Sertifikāts**.
1. Atveriet loga **Sertifikāts** cilni **Sertifikācijas ceļš**.
1. Atlasiet hierarhijas augšpusē parādīto sertifikātu. (tas ir saknes sertifikāts).
1. Atveriet loga **Sertikāts** cilni **Informācija**.
1. Cilnes **Informācija** apakšā atlasiet pogu **Kopēt failā**.
1. Tiek atvērts **Sertifikāta eksportēšanas vednis**. Lai turpinātu, atlasiet **Tālāk**.
1. Tiek atvērta lapa **Eksportēt faila formātu**. Atlasiet **DER kodēts binārais X.509 (.CER)**. Atlasiet **Tālāk**, lai turpinātu.
1. Tiek atvērta lapa **Eksportējamie faili**, norādiet faila nosaukumu un atrašanās vietu. Atlasiet **Tālāk**, lai turpinātu.
1. Tiek atvērta lapa **Sertifikāta eksportēšanas vedņa izpilde**, kurā tiek rādīts eksporta rezultāts. Atl. **Pabeigt**.

#### <a name="step-2-install-the-downloaded-certificate-onto-the-affected-devices"></a>2. darbība: Instalējiet lejupielādēto sertifikātu skartajās ierīcēs

Instalējiet lejupielādēto sertifikātu, izpildot šādas darbības:

1. Pārsūtiet iepriekšējā darbībā lejupielādēto sertifikātu uz ierīci, kuru vēlaties atjaunināt. Piemēram, iespējams, lietosit SD karti vai tīkla savienojumu, lai padarītu failu pieejamu ierīcei.
1. Atveriet ierīces drošības iestatījumus un atlasiet izvēlnes opciju, lai instalētu sertifikātu no faila. (Precīzas darbības ir atkarīgas no ierīces un OS versijas).
1. Jaunajam sertifikātam vajadzētu būt rādītam drošo sertifikātu cilnē **Lietotājs**.
1. Atkārtojiet šo procedūru katrai skartajai ierīcei.
