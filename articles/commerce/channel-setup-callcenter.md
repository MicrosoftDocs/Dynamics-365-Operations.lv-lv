---
title: Zvanu centra kanāla iestatīšana
description: Šajā tēmā aprakstīts, kā izveidot jaunu zvanu centra kanālu programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002454"
---
# <a name="set-up-a-call-center-channel"></a>Zvanu centra kanāla iestatīšana


[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot jaunu zvanu centra kanālu programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Programmā Dynamics 365 Commerce zvanu centrs ir mazumtirdzniecības kanāla veids, ko var definēt lietojumprogrammā. Lai noteiktu kanālu jūsu zvanu centra entītijām, sistēma ļauj saistīt specifiskus datus un pasūtījumu apstrādes noklusējumus pārdošanas pasūtījumos. Uzņēmums var definēt vairākus zvanu centra kanālus programmā Commerce. 

Pirms jauna zvanu centra kanāla izveidošanas pārliecinieties, ka esat pabeiguši [Kanāla iestatīšanas priekšnosacījumus](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Jauna zvanu centra kanāla izveide un konfigurācija

Lai izveidotu un konfigurētu jaunu zvanu centra kanālu, veiciet tālāk norādītās darbības.

1. Navigācijas rūtī atveriet **Moduļi \> Kanāli \> Zvanu centri \> Visi zvanu centri**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Nosaukums** ievadiet jaunā kanāla nosaukumu.
1. Atlasiet atbilstošo **Juridisko personu** no nolaižamā saraksta.
1. Atlasiet atbilstošo atrašanās vietu **Noliktava** no nolaižamā saraksta.
1. Laukā **Noklusējuma debitors** norādiet derīgu noklusējuma debitoru.
1. Laukā **e-pasta paziņojuma profils** norādiet derīgu e-pasta paziņojumu profilu.
1. Nodrošiniet informācijas kodu **Cenas ignorēšana**. Ņemiet vērā, ka jums, iespējams, vispirms būs jāizveido informācijas kods.
1. Norādiet informācijas kodu **Aizturēšanas kods**. Ņemiet vērā, ka jums, iespējams, vispirms būs jāizveido informācijas kods.
1. Norādiet informācijas kodu **Kredīts**. Ņemiet vērā, ka jums, iespējams, vispirms būs jāizveido informācijas kods.
1. Atlasiet **Saglabāt**.

Tālāk redzamajā attēlā parādīta jauna zvanu centra kanāla izveide.

![Jauns zvanu centra kanāls](media/channel-setup-callcenter-1.png)

Tālāk redzamajā attēlā ir parādīts zvanu centra kanāla piemērs.

![Zvanu centra kanāla piemērs](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Papildu kanāla iestatīšana

Papildu uzdevumi, kas nepieciešami zvanu centra kanāla iestatīšanai, ietver maksājuma metožu un piegādes režīmu iestatīšanu.

Tālāk esošajā attēlā ir parādītas cilnes **Iestatīšana** iestatīšanas opcijas **Piegādes veidi** un **Maksāšanas metodes**.

![Papildu zvanu centra kanāla iestatīšanas darbības](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Iestatīt maksājuma metodes

Lai iestatītu maksājuma metodes, katram šajā kanālā atbalstītajam maksājuma tipam veiciet tālāk norādītās darbības.

1. Darbības rūtī atlasiet cilni **Iestatīšana** un pēc tam atlasiet **Maksājumu metodes**.
1. Darbību rūtī atlasiet **Jauns**.
1. Navigācijas rūtī atlasiet vēlamo maksājuma metodi.
1. Sadaļā **Vispārīgi** norādiet **Operācijas nosaukumu** un konfigurējiet citus vēlamos iestatījumus.
1. Konfigurējiet jebkādus papildu iestatījumus, kas nepieciešami maksājuma veidam.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk esošajā attēlā ir parādīts skaidras naudas maksājuma piemērs.

![Maksājumu metožu piemērs](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Iestatiet piegādes veidus

Varat skatīt konfigurētos piegādes režīmus, atlasot **Piegādes veidi** no cilnes **Iestatījumi**, kas atrodas **Darbību rūtī**.  

Lai mainītu vai pievienotu piegādes veidu, rīkojieties, kā norādīts tālāk.

1. Navigācijas rūtī atveriet **Moduļi \> krājumu pārvaldība \> Piegādes režīmi**.
1. Darbības rūtī atlasiet **Jauns**, lai izveidotu jaunu piegādes režīmu, vai atlasiet esošu režīmu.
1. Sadaļā **Mazumtirdzniecības kanāli** atlasiet **Pievienot rindu**, lai pievienotu kanālu. Kanālu pievienošana, izmantojot organizācijas mezglus, nevis pievienojot katru kanālu atsevišķi, var racionalizēt kanālu pievienošanu.

Tālāk redzamajā attēlā parādīts piegādes režīma piemērs.

![Iestatiet piegādes veidus](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a>Papildu resursi

[Kanālu iestatīšanas priekšnosacījumi](channels-prerequisites.md)

[Zvanu centra pārdošanas funkcionalitāte](call-center-functionality.md)

[Iestatīt zvanu centra pasūtījumu apstrādes opcijas](set-up-order-processing-options.md)

[Zvanu centra katalogi](call-center-catalogs.md)

[Pārkāpumu brīdinājumu iestatīšana un darbs ar tiem](set-up-fraud-alerts.md)

[Nepārtrauktības programmu iestatīšana zvanu centriem](set-up-continuity-program.md)
