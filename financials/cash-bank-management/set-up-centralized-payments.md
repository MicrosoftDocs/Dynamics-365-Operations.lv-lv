---
title: "Centralizēto maksājumu iestatīšana"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 44d51807cd6bb64ae2c4bef58d8a445417ffa3a9
ms.openlocfilehash: 815282422a6d7b8eef7d0628cf10b715449e1d1d
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-centralized-payments"></a>Centralizēto maksājumu iestatīšana



Izpildiet šīs darbības, lai sagatavotu apstrādāt maksājumu vienu juridisku personu uzdevumā citas juridiskās personas, kas organizācijā. Pirms darba sākšanas jāaizpilda šādi iestatījumi:

-   Izveidojiet juridiskās personas.
-   Iestatiet Virsgrāmatas parametrus un kontu plānus.
-   Iestatiet kreditoru parametrus un debitoru parādu parametrus (atkarībā no moduļiem, kas izmanto centralizētos maksājumus).
-   Iestatiet starpuzņēmumu grāmatvedību.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Organizācijas hierarhijas iestatīšana centralizētiem maksājumiem
Jums ir jāiestata organizācijas hierarhija centralizētiem maksājumiem. Viena un tā pati organizācijas hierarhija tiek izmantota, lai apstrādātu centralizētos kreditoru maksājumus un centralizētos debitoru maksājumus. **Piezīme:** centralizētajiem maksājumiem hierarhijas struktūrai nav nozīmes. Jebkura juridiskā persona šajā hierarhijā varēs apstrādāt maksājumus citas šīs hierarhijas juridiskās personas vārdā. Lapā **Organizācijas hierarhijas** varat izveidot jaunu organizācijas hierarhiju.

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Starpuzņēmumu konta iestatīšana centralizētajiem norēķiniem
Kad pašreizējās juridiskās personas maksājumu transakcijas tiek nosegtas ar rēķiniem citās juridiskajās personās, katrai juridiskajai personai tiek izveidotas atbilstošas sākuma un beigu transakcijas. Jums jānorāda juridiskā persona, kurai tiek grāmatotas jebkuras termiņatlaižu vai realizētās peļņas vai zaudējumu summas. Pirms sākat, izlemiet, kuru juridisko personu izmantosiet kreditoru un debitoru maksājumu apstrādei. Ja viena juridiskā persona apstrādā kreditoru maksājumus, bet cita juridiskā persona apstrādā debitoru maksājumus, jums būs nepieciešams pārslēgties uz katru juridisko personu. Par **starpuzņēmumu kontiem** lapu, atlasiet starpuzņēmumu attiecības ierakstu par juridisku personu, kas tiek izpildīta maksājumu vārdā. Par **centralizētu maksājumu** tab, var izvēlēties, vai grāmatot naudas atlaides maksājumu (vai citu darbību, kas samazina kreditora konta atlikumu) tiesību subjekta vai tiesību subjekta rēķina (vai citu darbību, kas palielina kreditora konta atlikums). Šī izvēle darbojas kopā ar lauku **Termiņatlaižu administrēšana** lapās **Kreditoru moduļa parametri** un **Debitoru moduļa parametri**. Pārmaksām un sīknaudas starpības tolerancēm tiek izmantots maksājuma juridiskās personas iestatījums. Nepilnas samaksas un sīknaudas starpības tolerancēm tiek izmantots rēķina juridiskās personas iestatījums.

## <a name="map-vendor-accounts-across-legal-entities"></a>Kreditoru kontu kartēšana dažādām juridiskajām personām
Ja maksājat kreditoram no vienas juridiskās personas un šim kreditoram vēlaties atlasīt rēķinus citās juridiskajās personās, ir jāpārliecinās, ka visi atbilstošie kreditoru konti katrai juridiskajai personai izmanto vienu un to pašu adrešu grāmatas ID. Ja saņemat maksājumu no debitora, kas maksā rēķinus vairāk nekā vienā juridiskajā personā, jums ir jāpārliecinās, ka katras juridiskās personas visos atbilstošajos debitoru kontos tiek izmantots vienāds adrešu grāmatas ID.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Grāmatošanas metožu iestatīšana centralizētajiem norēķiniem
Izveidojot maksājumu juridiskajā personā, kas rēķinus kārto citās juridiskajās personās, abās juridiskajās jābūt vienādam grāmatošanas metodes ID. Lai pārliecinātos, ka maksājumi tiek izveidoti pareizi, katrai rēķinā norādītajai juridiskajai personai iestatiet grāmatošanas metodi, kas atbilst maksājuma dokumentā norādītās juridiskās personas grāmatošanas metodēm. Pārslēgties uz pirmo juridiskās personas rēķina, un pēc tam uz **formu Vendor posting profiles** lapu, varat izveidot jaunu grāmatošanas metodi vai rediģējiet esošo grāmatošanas metodi. Atlases, ko veicat programmā juridiskās personas rēķina grāmatošanas metodei nav atbilstoši juridiskās vienības maksājumu grāmatošanas metodes iestatījumiem.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Maksāšanas metožu iestatīšana centralizētajiem maksājumiem
Izveidojot maksājumu juridiskajā personā, kas rēķinus kārto citās juridiskajās personās, abās juridiskajās jābūt vienādam maksāšanas metodes ID. Lai pārliecinātos, ka maksājumi tiek izveidoti pareizi, katrai rēķinā norādītajai juridiskajai personai iestatiet maksāšanas metodi, kas atbilst maksājuma dokumentā norādītās juridiskās personas maksāšanas metodēm. Pārejiet uz pirmo rēķinā minēto juridisko personu un tad lapā **Maksāšanas metodes **varat izveidot jaunu maksāšanas metodi vai rediģēt esošu maksāšanas metodi. Rēķinā norādītās juridiskās personas maksāšanas metodei izvēlētajām opcijām nav jāatbilst maksājuma dokumentā norādītās juridiskās personas maksāšanas metodes iestatījumiem.

## <a name="set-up-default-descriptions"></a>Noklusējuma aprakstu iestatīšana
Starpuzņēmumu segšanas dokumentiem varat definēt noklusējuma aprakstus. Noklusējuma apraksts starpuzņēmumu apmaksas apstrādes laikā tiek ietverts apmaksas sākuma un beigu darījumos. Lapā **Noklusējuma apraksti** varat izveidot jaunus aprakstus gan **Starpuzņēmumu debitoru nosegšana**, gan **Starpuzņēmumu kreditora nosegšana**, atlasot valodu un pēc tam ievadot tekstu.


