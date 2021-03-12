---
title: Unikālas noliktavas vienības saņemšana, izmantojot noliktavas programmu
description: Šajā tēmā ir izskaidrots, kā iestatīt noliktavas programmu, lai atbalstītu unikālas noliktavas vienības saņemšanas procesa izmantošanu, lai saņemtu fizisko krājumu.
author: perlynne
manager: tfehr
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters, WHSRFMenuItem, WHSLicensePlate, WHSPackingStructure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 0fe02a83d05e4b86694c1b210906128ac0cf6a84
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998432"
---
# <a name="license-plate-receiving-via-the-warehouse-app"></a>Unikālas noliktavas vienības saņemšana, izmantojot noliktavas programmu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir izskaidrots, kā iestatīt noliktavas programmu, lai tā atbalstītu unikālas noliktavas vienības saņemšanas procesa izmantošanu, lai saņemtu fizisko krājumu.

Jūs varat izmantot šo funkcionalitāti, lai ātri ierakstītu ienākošo krājumu saņemšanu, kas ir saistīts ar iepriekšējo paziņojums par nosūtīšanu (ASN). Sistēma automātiski izveido ASN, kad noliktavas pārvaldības procesi tiek izmantoti, lai nosūtītu pārsūtīšanas pasūtījumu. Pirkšanas pasūtījuma procesam ASN var tikt manuāli reģistrēts, vai to var automātiski importēt, izmantojot ienākošo ASN datu elementa procesu.

ASN dati ir saistīti ar noslodzēm un kravām, izmantojot *iepakošanas struktūras*, kur paletes (standarta numura zīmes) var ietvert gadījumus (ligzdotas numura zīmes).

> [!NOTE]
> Lai samazinātu krājumu transakciju skaitu, kad tiek izmantotas iepakojuma struktūras, kurām ir ligzdotas numura zīmes, sistēma reģistrē fiziskos rīcībā esošos krājumus uz pamatnumura zīmes. Lai izraisītu fizisko rīcībā esošo krājumu pārvietošanu no pamatnumura zīmes uz ligzdotajām numura zīmēm, kas balstītas uz iepakojuma struktūras datiem, mobilajai ierīcei ir jānorāda izvēlnes elements, kas ir atkarīgs no *Ligzdotu licenču plāksnīšu iepakošanas* darba izveides procesiem.

## <a name="warehousing-mobile-device-app-processing"></a>Noliktavu mobilās ierīces programmas apstrāde

Kad darbinieks skenē ienākošo noliktavas vienības ID, sistēma inicializē noliktavas vienības saņemšanas procesu. Pamatojoties uz šo informāciju, saņemšanas doka vietā tiek fiziski reģistrēts noliktavas vienības saturs (dati, ko nosūta ASN). Turpmākās plūsmas būs atkarīgas no biznesa procesa vajadzībām.

## <a name="work-policies"></a>Darba politikas

Tāpat kā (piemēram) kā mobilās ierīces izvēlnes elementu process *Reģistrēt pabeigšanu*, noliktavas vienības saņemšanas process atbalsta vairākas darbplūsmas, kas pamatotas uz definētajiem iestatījumiem.

### <a name="work-policies-with-work-creation"></a>Darba politikas ar darba izveidi

Kad reģistrējat ienākošos krājumus, izmantojot darba politiku, kas izveido darbu, sistēma ģenerē un saglabā izvietošanas darba ierakstu katrai reģistrācijai. Ja izmantojat darba procesu *Noliktavas vienības saņemšana un izvietošana*, tad reģistrācija un izvietošana tiek apstrādāta kā viena darbība, izmantojot vienas mobilās ierīces izvēlnes elementu. Ja izmantojat procesu *Noliktavas vienības saņemšana*, tad saņemšanas un izvietošanas procesi tiek apstrādāti kā divas dažādas noliktavas operācijas — katra ar savu mobilās ierīces izvēlnes elementu.

### <a name="work-policies-without-work-creation"></a>Darba politikas bez darba izveides

Varat izmantot noliktavas vienības saņemšanas procesu, neveidojot darbu. Ja nosakāt darba politikas, kurām darba pasūtījuma veids ir *Pārsūtīšanas saņemšana* un/vai *Pirkšanas pasūtījumi*, un jūs izmantojat procesu *Noliktavas vienības saņemšana (un izvietošana)*, tālāk minētie divi noliktavu mobilās programmas procesi neveidos darbu. Tā vietā tie tikai reģistrēs ienākošos fiziskos krājumus noliktavas vienībai saņemšanas dokā.

- *Noliktavas vienības saņemšana*
- *Numura zīmes saņemšana un izvietošana*

> [!NOTE]
> - Ir jādefinē vismaz viena atrašanās vieta darba politikai sadaļā **Krājumu atrašanās vietas**. Vairākām darba politikām nevar norādīt vienu un to pašu atrašanās vietu.
> - Noliktavu mobilās ierīces izvēlnes elementu opcija **Drukāt etiķeti** nedrukās noliktavas vienības etiķeti bez darba izveides.

Lai šo funkcionalitāti padarītu pieejamu jūsu sistēmā, ir jāieslēdz līdzeklis *Noliktavas vienības saņemšanas uzlabojumi* [funkciju pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="receive-inventory-on-a-location-that-doesnt-track-license-plates"></a>Krājumu saņemšana atrašanās vietā, kas neizseko noliktavas vienības

Ir iespējams izmantot noliktavas atrašanās vietu, kas piešķirta atrašanās vietas profilam, pat ja opcija **Izmantot noliktavas vienības izsekošanu** nav ieslēgta. Tāpēc, saņemot krājumus, varat tieši reģistrēt rīcībā esošos krājumus atrašanās vietā bez darba izveides.

## <a name="add-mobile-device-menu-items-for-each-receiving-location-in-a-warehouse"></a>Mobilās ierīces izvēlnes elementu pievienošana katrai saņemšanas vietai noliktavā

Līdzeklis *Noliktavas vienības saņemšanas uzlabojumi* ļauj saņemt jebkurā noliktavas vietā, pievienojot atrašanās vietai specifiskus noliktavas vienības saņemšanas (un izvietošanas) izvēlnes elementus noliktavu mobilajai programmai. Iepriekš sistēma atbalstīja saņemšanu tikai noklusētajā atrašanās vietā, kas definēta katrai noliktavai. Tomēr, ja šis līdzeklis ir ieslēgts, mobilās ierīces izvēlnes elementi noliktavas vienības saņemšanai (un izvietošanai) tagad nodrošina opciju **Izmantot noklusējuma datus**, kas ļauj atlasīt pielāgotu "uz" atrašanās vietu katram izvēlnes elementam. (Šī opcija jau bija pieejama dažiem citiem izvēlnes elementu veidiem.)

Lai šo funkcionalitāti padarītu pieejamu jūsu sistēmā, ir jāieslēdz līdzeklis *Noliktavas vienības saņemšanas uzlabojumi* [funkciju pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="show-or-skip-the-receiving-summary-page"></a>Rādīt vai izlaist saņemšanas kopsavilkuma lapu

Jūs varat izmantot līdzekli *Kontrolēt, vai mobilajās ierīcēs tiktu parādīta saņemšanas kopsavilkuma lapa*, lai izmantotu papildu detalizēto Noliktavu programmu plūsmu kā daļu no numura zīmes saņemšanas procesa.

Kad šis līdzeklis ir ieslēgts, mobilās ierīces izvēlnes vienumi numura zīmes saņemšanas vai numura zīmes saņemšanas un izvietošanas laikā nodrošinās iestatījumu **Parādīt saņemšanas kopsavilkuma lapu**. Šim iestatījumam ir šādas opcijas:

- **Rādīt detalizētu kopsavilkumu** — veicot numura zīmes saņemšanu, darbinieki redzēs papildu lapu, kas parāda pilnu ASN informāciju.
- **Izlaist kopsavilkumu** — darbinieki neredzēs pilnu ASN informāciju. Noliktavas darbinieki arī saņemšanas procesa laikā nevarēs iestatīt izvietojuma kodu vai pievienot izņēmumus.

Lai šo funkcionalitāti padarītu pieejamu jūsu sistēmā, ir jāaktivizē līdzeklis *Kontrolēt, vai ir jārāda saņemšanas kopsavilkuma lapa mobilajās ierīces* sadaļā [funkciju pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Nepieļaut nodošanas pasūtījuma nosūtīto numura zīmju izmantošanu noliktavās, kas nav galamērķa noliktava

Nevar izmantot noliktavas vienības saņemšanas procesu, ja ASN ietver noliktavas vienības ID, kas jau eksistē un kam ir fiziski rīcībā esošie dati noliktavas atrašanās vietā, kas atšķiras no noliktavas atrašanās vietas, kur notiek noliktavas vienības reģistrācija.

Pārsūtīšanas pasūtījumu scenārijiem, kuros tranzīta noliktava neseko numura zīmēm (un tāpēc arī neseko līdzi katras numura zīmes fiziskajam inventāram uz vietas), varat izmantot līdzekli *Nepieļaut nodošanas pasūtījuma nosūtīto numura zīmju izmantošanu noliktavās, kas nav galamērķa noliktava*, lai novērstu to, ka fiziskas rīcībā esošas numura zīmes ir pieejamas tranzītā.

Lai šo funkcionalitāti padarītu pieejamu jūsu sistēmā, ir jāieslēdz līdzeklis *Neatļaut pārsūtīšanas pasūtījuma nosūtītās noliktavas vienības izmantot citās noliktavās, kas nav mērķa noliktava* [līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Lai pārvaldītu funkcionalitāti, kad šī funkcija ir pieejama, veiciet šādas darbības.

1. Doties uz **Noliktavas vadība\> Iestatīšana \> Noliktavas vadības parametri**.
1. Cilnē **Vispārīgi** kopsavilkuma cilnē **Numura zīmes**  iestatiet **Tranzīta noliktavas numura zīmes politikas** lauku uz vienu no šīm vērtībām:

    - **Atļaut nereģistrētas numura zīmes atkārtotu izmantošanu** — sistēma darbojas tādā pašā veidā, kā tas darbojas, kad līdzeklis *Nepieļaut nodošanas pasūtījuma nosūtīto numura zīmju izmantošanu citās noliktavās, kas nav galamērķa noliktava* nav pieejams. Šī vērtība ir noklusētais iestatījums, pirmoreiz aktivizējot līdzekli.
    - **Novērst nereģistrētas numura zīmju atkārtotu izmantošanu** - līdz pārsūtīšanas pasūtījuma saņemšanai mērķa noliktavā tiks atļauti tikai rīcībā esošie atjauninājumi, kas saistīti ar nosūtītajām numura zīmēm.

## <a name="more-information"></a>Papildinformācija

Papildinformāciju par mobilās ierīces izvēlnes elementiem skatiet [Mobilo ierīču iestatīšana noliktavas darbam](configure-mobile-devices-warehouse.md).

Papildinformāciju par ražošanas scenāriju *Reģistrēt pabeigšanu* skatiet [Noliktavas darba politiku pārskats](warehouse-work-policies.md).

Papildinformāciju par saņemšanas noslodzes pārvaldību skatiet [Ienākošo noslodžu noliktavas apstrāde pirkšanas pasūtījumu veikšanai](inbound-load-handling.md).
