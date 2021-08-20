---
title: Transakcijas aizturēšana vai atsākšana pārdošanas punktā (POS)
description: Šajā tēmā ir paskaidrots, kā lietotāji var aizturēt notiekošas transakcijas un tās atsākt vēlāk vai citā kases sistēmā, izmantojot Dynamics 365 Commerce.
author: jblucher
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2efc88cfa7a8cede50969484d275c6fdbb2204dd2f29b3f8c7340d02cb61a79c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737558"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a>Transakcijas aizturēšana vai atsākšana pārdošanas punktā (POS)

[!include [banner](includes/banner.md)]


Pārdošanas punkta (POS) lietotāji var aizturēt notiekošas transakcijas un pēc tam atsākt tās vēlāk vai citā reģistrā. Transakcijas bieži tiek aizturētas, lai ātri atbrīvotu reģistru citam uzdevumam, nezaudējot pašreizējās transakcijas progresu. Piemēram, veikala speciālists sāk apstrādāt debitora transakciju mobilajā ierīcē, taču apstrāde ir jāpabeidz reģistrā, kam ir naudas kaste. Šajā gadījumā veikala speciālists var aizturēt transakciju mobilajā ierīcē un pēc tam atsaukt to un atsākt reģistrā.

## <a name="configure-suspend-and-resume-functionality"></a>Aizturēšanas un atsākšanas funkcijas konfigurēšana

### <a name="pos-operations"></a>POS operācijas

Divas [POS operācijas](pos-operations.md) ļauj POS atbalstīt aizturēšanas un atsākšanas scenārijus. Varat piešķirt šīs operācijas [pogu režģiem](pos-screen-layouts.md) transakciju lapā vai sveiciena lapā.

- 503: Aizturēt transakciju
- 504: Atsaukt transakciju

### <a name="receipt-template"></a>Kvīts veidne

POS var konfigurēt, lai ģenerētu drukātās pavadzīmes, kad transakcija ir aizturēta. Šo pavadzīmi var izmantot, lai vēlāk ātri noteiktu un atsauktu transakciju.

Lai iespējotu kvīts drukāšanau POS, veikala kvīts profilam ir jāpievieno kvīts formāts **Aizturēta transakcija**. Kvīts formātu var izveidot tā, lai tajā tiktu vai netiktu iekļauti noteikti transakcijas dati. Piemēram, formāts var iekļaut svītrkodu skenēšanas nodrošināšanai.

### <a name="receipt-numbering"></a>Kvīšu numerācija

Tāpat kā citiem POS transakciju tipiem, kuri ģenerē drukātas kvītis, veikala funkcionalitātes profila sadaļā **Kvīšu numerācija** varat definēt numerāciju aizturētajām transakcijām.

### <a name="void-when-closing-shift"></a>Anulēt, noslēdzot maiņu

Varat izmantot opciju **Anulēt, noslēdzot maiņu**, lai pieprasītu, ka lietotāji pabeidz vai anulē jebkuru aizturētu transakciju pirms savas maiņas slēgšanas. Operācijas **Maiņas slēgšana** laikā, POS piedāvās lietotājiem skatīt vai anulēt visas nenokārtotās aizturētās transakcijas.

## <a name="suspend-and-resume-a-transaction"></a>Transakcijas aizturēšana un atsākšana

### <a name="suspend-a-transaction"></a>Transakcijas aizturēšana

Lietotāji, kuriem ir atbilstošas privilēģijas un kuru ekrāna izkārtojumā ir ietverta operācija **Transkacijas aizturēšana**, var aizturēt transakciju, lai to atsaukttu vēlāk vai citā reģistrā.

Transakcijas var aizturēt tikai tad, ja tajās **nav** tālāk norādīto tipu rindu:

- Aktīvā maksājuma rindas
- Dāvanu kartes rindas (dāvanu kartes izsniegšana vai dāvanu kartes bilances papildināšana)

Aizturēta transakcija neietekmē pārdošanas informāciju vai krājumu pieejamības informāciju veikalā.

### <a name="resume-a-suspended-transaction"></a>Aizturētas transakcijas atsākšana

Aizturētās transakcijas var atsaukt un atsākt vienā veikalā jebkurš lietotājs, kuram ir atbilstošas privilēģijas un kuram ir arī izkārtojums, kas ietver operāciju **Transakcijas atsākšana**.

Lai ātri un viegli atsauktu aizturētu transakciju, noskenējiet drukātās pavadzīmes svītrkodu, kamēr skatāt operācijas **Transakcijas atsākšana** transakciju sarakstu.

### <a name="considerations-for-offline-mode"></a>Apsvērumi bezsaistes režīmā

- Transakcijas, kas ir aizturētas, kamēr POS ir tiešsaistes režīmā, nevar atsākt bezsaistes režīmā, jo dati nav sinhronizēti ar bezsaistes datu bāzi.
- Ja aizturat transakciju, kamēr POS ir bezsaistes režīmā, varat atsaukt to bezsaistes režīmā, ja ir zināms, ka POS nevienā brīdī pēc transakcijas aizturēšanas nav bijis pārslēgts atpakaļ tiešsaistes režīmā. Pārslēdzot POS atpakaļ tiešsaistes režīmā, dati par aizturētajām transakcijām tiek pārvietoti uz tiešsaistes datu bāzi un noņemti no bezsaistes datu bāzes. Tāpēc transakcijas var atsākt tikai tiešsaistes režīmā. Ja pārslēgsiet POS atpakaļ bezsaistes režīmā, aizturētās transakcijas nevarēsiet atsākt, jo tās jau būs noņemtas no bezsaistes datu bāzes.

### <a name="void-a-suspended-transaction"></a>Aizturētas transakcijas anulēšana

Aizturētās transakcijas varat anulēt, vai nu atsaucot transakciju un pēc tam veicot operāciju **Transakcijas anulēšana**, vai atlasot transakciju sarakstā **Transakcijas atsaukšana** un programmas joslā atlasot **Anulēt**. Var arī konfigurēt veikalu tā, lai lietotājiem piedāvātu anulēt aizturētās transakcijas, kad lietotāji slēdz maiņu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]