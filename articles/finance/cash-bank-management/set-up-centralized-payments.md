---
title: Iestatīt centralizētos maksājumus
description: Veiciet šīs darbības, lai sagatavos maksājumu apstrādei vienai juridiskajai personai citu jūsu organizācijas juridisko personu vārdā.
author: kweekley
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70b47f819730ae221568e625a1b218e046927e41
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445587"
---
# <a name="set-up-centralized-payments"></a>Iestatīt centralizētos maksājumus

[!include [banner](../includes/banner.md)]

Veiciet šīs darbības, lai sagatavos maksājumu apstrādei vienai juridiskajai personai citu jūsu organizācijas juridisko personu vārdā. Pirms sākat, jāveic tālāk aprakstītā iestatīšana.

-   Izveidojiet juridiskās personas.
-   Iestatiet Virsgrāmatas parametrus un kontu plānus.
-   Iestatiet kreditoru parametrus un debitoru parādu parametrus (atkarībā no moduļiem, kas izmanto centralizētos maksājumus).
-   Iestatiet starpuzņēmumu grāmatvedību.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Organizācijas hierarhijas iestatīšana centralizētiem maksājumiem
Jums ir jāiestata organizācijas hierarhija centralizētiem maksājumiem. Viena un tā pati organizācijas hierarhija tiek izmantota, lai apstrādātu centralizētos kreditoru maksājumus un centralizētos debitoru maksājumus. **Piezīme:** centralizētajiem maksājumiem hierarhijas struktūrai nav nozīmes. Jebkura juridiskā persona šajā hierarhijā varēs apstrādāt maksājumus citas šīs hierarhijas juridiskās personas vārdā. Lapā **Organizācijas hierarhijas** varat izveidot jaunu organizācijas hierarhiju. Laukā **Nolūks** ir jāatlasa **Centralizēti maksājumi**. 

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Starpuzņēmumu konta iestatīšana centralizētajiem norēķiniem
Kad pašreizējās juridiskās personas maksājumu transakcijas tiek nosegtas ar rēķiniem citās juridiskajās personās, katrai juridiskajai personai tiek izveidotas atbilstošas sākuma un beigu transakcijas. Jums jānorāda juridiskā persona, kurai tiek grāmatotas jebkuras termiņatlaižu vai realizētās peļņas vai zaudējumu summas. Pirms sākat, izlemiet, kuru juridisko personu izmantosiet kreditoru un debitoru maksājumu apstrādei. Ja viena juridiskā persona apstrādā kreditoru maksājumus, bet cita juridiskā persona apstrādā debitoru maksājumus, jums būs nepieciešams pārslēgties uz katru juridisko personu. Lapā **Starpuzņēmumu grāmatvedība** varat atlasīt starpuzņēmumu attiecību ierakstu juridiskajai personai, kuras vārdā apstrādāsit maksājumus. 

Cilnē **Centralizēti maksājumi** varat atlasīt, vai tiks grāmatotas termiņatlaides maksājuma (vai cita darījuma, kas samazina kreditora konta bilanci) juridiskajai personai vai rēķina (vai citas transakcijas, kas palielina kreditora konta bilanci) juridiskajai personai. Šī izvēle darbojas kopā ar lauku **Termiņatlaižu administrēšana** lapās **Kreditoru moduļa parametri** un **Debitoru moduļa parametri**. Pārmaksām un sīknaudas starpības tolerancēm tiek izmantots maksājuma juridiskās personas iestatījums. Nepilnas samaksas un sīknaudas starpības tolerancēm tiek izmantots rēķina juridiskās personas iestatījums.

## <a name="map-vendor-accounts-across-legal-entities"></a>Kreditoru kontu kartēšana dažādām juridiskajām personām
Ja maksājat kreditoram no vienas juridiskās personas un šim kreditoram vēlaties atlasīt rēķinus citās juridiskajās personās, ir jāpārliecinās, ka visi atbilstošie kreditoru konti katrai juridiskajai personai izmanto vienu un to pašu adrešu grāmatas ID. Ja saņemat maksājumu no debitora, kas maksā rēķinus vairāk nekā vienā juridiskajā personā, jums ir jāpārliecinās, ka katras juridiskās personas visos atbilstošajos debitoru kontos tiek izmantots vienāds adrešu grāmatas ID.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Grāmatošanas metožu iestatīšana centralizētajiem norēķiniem
Izveidojot maksājumu juridiskajā personā, kas rēķinus kārto citās juridiskajās personās, abās juridiskajās jābūt vienādam grāmatošanas metodes ID. Lai pārliecinātos, ka maksājumi tiek izveidoti pareizi, katrai rēķinā norādītajai juridiskajai personai iestatiet grāmatošanas metodi, kas atbilst maksājuma dokumentā norādītās juridiskās personas grāmatošanas metodēm. Pārejiet uz pirmo rēķinā minēto juridisko personu un tad lapā **Kreditoru grāmatošanas metodes** varat izveidot jaunu grāmatošanas metodi vai rediģēt esošu grāmatošanas metodi. Rēķinā norādītās juridiskās personas grāmatošanas metodei izvēlētajām opcijām nav jāatbilst maksājuma dokumentā norādītās juridiskās personas grāmatošanas metodes iestatījumiem.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Maksāšanas metožu iestatīšana centralizētajiem maksājumiem
Izveidojot maksājumu juridiskajā personā, kas rēķinus kārto citās juridiskajās personās, abās juridiskajās jābūt vienādam maksāšanas metodes ID. Lai pārliecinātos, ka maksājumi tiek izveidoti pareizi, katrai rēķinā norādītajai juridiskajai personai iestatiet maksāšanas metodi, kas atbilst maksājuma dokumentā norādītās juridiskās personas maksāšanas metodēm. Pārejiet uz pirmo rēķinā minēto juridisko personu un tad lapā **Maksāšanas metodes** varat izveidot jaunu maksāšanas metodi vai rediģēt esošu maksāšanas metodi. Rēķinā norādītās juridiskās personas maksāšanas metodei izvēlētajām opcijām nav jāatbilst maksājuma dokumentā norādītās juridiskās personas maksāšanas metodes iestatījumiem.

## <a name="set-up-default-descriptions"></a>Noklusējuma aprakstu iestatīšana
Starpuzņēmumu segšanas dokumentiem varat definēt noklusējuma aprakstus. Noklusējuma apraksts starpuzņēmumu apmaksas apstrādes laikā tiek ietverts apmaksas sākuma un beigu darījumos. Lapā **Noklusējuma apraksti** varat izveidot jaunus aprakstus gan **Starpuzņēmumu debitoru nosegšana**, gan **Starpuzņēmumu kreditora nosegšana**, atlasot valodu un pēc tam ievadot tekstu.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]