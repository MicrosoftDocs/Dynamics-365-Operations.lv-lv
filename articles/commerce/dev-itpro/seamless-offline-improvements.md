---
title: Ērta bezsaistes pārslēgšanās dāvanu karšu un kredītrēķinu darbībām
description: Šajā tēmā sniegts to uzlabojumu apskats, kas nodrošina ērtu bezsaistes pārslēgšanos noteiktiem maksājuma veidiem.
author: BrianShook
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 59f1a0b213bd22906ba8b2c3e7da38a9818f6d4f
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779496"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a>Ērta bezsaistes pārslēgšanās dāvanu karšu un kredītrēķinu darbībām

[!include [banner](../includes/banner.md)]

Ja pārdošanas punkta (POS) ierīce zaudē savu savienojumu ar kanāla datu bāzi, lielākā daļa POS darbību un transakciju, kas bija uzsāktas, var tikt turpinātas pēc tam, kad kasieris saņems brīdinājuma ziņojumu par savienojamības zudumu. Tomēr dažos gadījumos transakcijām ir elementi, kas paļaujas uz reāllaika pakalpojumu, un šie elementi netiek atbalstīti, ja POS ir bezsaistē. Šajā tēmā ir aprakstīta daļa funkcionalitātes, kas palīdz samazināt zaudētās savienojamības ietekmi šādos gadījumos.

## <a name="completing-gift-card-transactions-in-offline-mode"></a>Dāvanu karšu transakciju izpilde bezsaistes režīmā

Iekšējās dāvanu kartes ir atkarīgas no reāllaika pakalpojuma, jo dāvanu karšu bilancei jābūt centralizēti uzturētai programmā Microsoft Dynamics 365 Commerce Headquarters. Lai novērstu krāpšanu vai citas sinhronizēšanas problēmas, dāvanu kartes tiek bloķētas, tiklīdz tās tiek pievienotas transakcijai. Bloķēšanas funkcija nodrošina to, ka dāvanu karti nevar izmantot vairākos termināļos vienlaicīgi. Pēc darbības pabeigšanas dāvanu karte tiek automātiski atjaunināta un atbloķēta.

Tomēr, ja POS pazaudē savienojumu pēc tam, kad dāvanu karte ir pievienota transakcijai, dāvanu karte var kļūt nelietojama. Lai nepieļautu šo situāciju, Dynamics 365 Commerce ir parametrs, kas aktivizē transakcijas, kas ietver dāvanu kartes rindu, kas jāizpilda, kamēr POS ir bezsaistē. Kad šis parametrs ir ieslēgts, dāvanu kartes transakcijas, kas nonāk bezsaistē, tiks saglabātas kopā ar bezsaistes transakcijām, un tās tiks sinhronizētas ar Commerce Headquarters, kad tiks sinhronizētas bezsaistes transakcijas. Sinhronizācija arī atbloķē dāvanu karti, lai to varētu izmantot citā terminālī.

Lai iespējotu funkcionalitāti, kas ļauj noslēgt dāvanu kartes transakcijas pēc pārslēgšanās uz bezsaistes režīmu, dodieties uz cilni **Grāmatošana**, kas atrodas lapā **Commerce parametri**. Šajā cilnē atrodiet kopsavilkuma cilni **Dāvanu karte** un iestatiet opciju **Noslēgt dāvanu karšu darbības bezsaistes režīmā** uz **Jā**.

![Bezsaistes dāvanu kartes iestatīšana.](../media/gift.png)

Commerce parametri parasti tiek kešoti. Tāpēc, lai sinhronizētu izmaiņas kanālā pēc šī parametra iestatījuma atjaunināšanas un sadales grafika sākšanas, izmaiņas var ilgt līdz pat 24 stundām. Lai izmaiņas stātos spēkā nekavējoties, atiestatiet Microsoft Internet Information Services (IIS).

## <a name="completing-credit-memo-transactions-in-offline-mode"></a>Kredītrēķina transakciju izpilde bezsaistes režīmā

Līdzīgi kā iekšējās dāvanu kartes, kredītrēķini tiek centralizēti uzturēti pakalpojumā Commerce Headquarters. Commerce ir parametrs, kas iespējo kredītrēķinu transakciju izpildi, kamēr POS ir bezsaistē. Šis parametrs darbojas tāpat kā dāvanu kartes parametrs, kas minēts iepriekšējā sadaļā. Kad parametrs ir ieslēgts, kredītrēķina transakcijas, kas nonākušas bezsaistē, tiks sinhronizētas ar kanāla datu bāzi kopā ar citām transakcijām, kas tika veiktas, kamēr POS bija bezsaistē.

Lai iespējotu funkcionalitāti, kas ļauj noslēgt kredītrēķina transakcijas pēc pārslēgšanās uz bezsaistes režīmu, dodieties uz cilni **Grāmatošana**, kas atrodas lapā **Commerce parametri**. Šajā cilnē atrodiet kopsavilkuma cilni **Kredītrēķins** un iestatiet opciju **Noslēgt kredītrēķinu transakcijas bezsaistes režīmā** uz **Jā**.

![Bezsaistes kredītrēķina iestatīšana.](../media/creditmemo.png)

Commerce parametri parasti tiek kešoti. Tāpēc, lai sinhronizētu izmaiņas kanālā pēc šī parametra iestatījuma atjaunināšanas un sadales grafika sākšanas, izmaiņas var ilgt līdz pat 24 stundām. Lai izmaiņas stātos spēkā nekavējoties, atiestatiet IIS.

## <a name="related-topics"></a>Saistītās tēmas

- [Pārdošanas punktu (POS) funkcionalitāte bezsaistē](../pos-offline-functionality.md)
- [Tiešsaistes un bezsaistes pārdošanas punkta (POS) operācijas](../pos-operations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]