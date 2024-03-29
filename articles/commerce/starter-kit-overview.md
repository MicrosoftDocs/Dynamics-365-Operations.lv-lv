---
title: Moduļu bibliotēkas pārskats
description: Šajā rakstā ir sniegts moduļu bibliotēkas Microsoft Dynamics 365 Commerce apskats.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d9dc07b3f6417c7e284c6555c2818c2a782d7683
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268951"
---
# <a name="module-library-overview"></a>Moduļu bibliotēkas pārskats

[!include [banner](includes/banner.md)]

Šajā rakstā ir sniegts moduļu bibliotēkas Microsoft Dynamics 365 Commerce apskats.

Dynamics 365 Commerce moduļu bibliotēka ir moduļu kopums, ko var izmantot, lai izveidotu e-komercijas vietni. Moduļos ir gan lietotāja interfeisa (UI) aspekti, gan funkcionālās uzvedības aspekti.

Tēmas var lietot moduļu bibliotēkas moduļiem, lai mainītu to izskatu un iespaidu. Tēmas izmanto stila lapas kaskadēšanu (CSS). Fiktīvas e-komercijas vietnes, kuras nosaukums ir “Fabrikam”, dizains tiek sniegts kā moduļu bibliotēkas daļa, un to var izmantot kā atsauci.

## <a name="module-library-modules"></a>Moduļu bibliotēkas moduļi

Moduļu bibliotēkā ir iekļauti tālāk norādītie moduļu tipi:

- **Konteinera modulis** — konteinera modulis ir vienkāršs modulis, kas darbojas kā resursdators citiem moduļiem. Tas kontrolē moduļu izkārtojumu, kas atrodas tajā.
- **Mārketinga moduļi** — mārketinga moduļi ietver satura bloka, teksta bloka, video atskaņotāja un karuseļa moduļus. Visus šos moduļus var izmantot, lai parādītu saturu. Tos var ievietot jebkurā lapā un tos vada dati no Satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā.
- **Galveņu un kājeņu moduļi** — galveņu un kājeņu moduļi ir redzami visu vietnes lapu galvenē un kājenē. Šos moduļus var konfigurēt pēc nepieciešamības, izmantojot rekvizītus.
- **Meklēšanas moduļi** — preces var skatīt, izmantojot meklēšanas moduli galvenē. Meklēšanas rezultāti parādās meklēšanas rezultātu lapā. Preces var skatīt arī kategorijas lapās, kas ir paredzētas katrai kategorijai, kas tiek atbalstīta kanāla navigācijas hierarhijā. Turklāt precizētos moduļus var izmantot, lai turpmāk filtrētu rezultātus meklēšanas rezultātos un kategoriju lapās.
- **Preces detalizētas informācijas lapas moduļi** — preces detalizētas informācijas lapas izmanto vairākus moduļus, lai parādītu preces informāciju. Pirkšanas kastes modulis ļauj klientiem skatīt preces un pievienot tās grozam. Citi moduļi, piemēram, tehniskās specifikācijas modulis parāda informāciju par preci. Vērtējumu un pārskatu moduli var izmantot, lai apskatītu un sniegtu pārskatus.
- **Modulis Pirkt tiešsaistē un paņemt veikalā** — šis modulis ir integrēts ar Bing kartēm. To var izmantot, lai atrastu tuvumā esošos veikalus, kuros klienti var saņemt preces, ko tie iegādājušies.
- **Pirkšanas moduļi** — pirkšanas moduļi ietver iepirkumu grozu moduli, ko var izmantot, lai pievienotu vienumus grozam. Norēķināšanās modulī tiek ietverta piegādes adrese, piegādes opcijas, dāvanu karte, lojalitātes programma un kredītkartes informācija, lai varētu apstrādāt pasūtījumu. Pēc tam, kad pasūtījums ir veikts, var izmantot pasūtījuma apstiprināšanas moduli, lai parādītu detalizētu informāciju par apstiprinājumu.
- **Konta pārvaldības moduļi** — pierakstīšanās modulis ļaut klientiem pieteikties esošā kontā, un reģistrēšanās modulis ļauj izveidot jaunu kontu. Kad konts ir izveidots, pasūtījumu vēstures modulis var tikt izmantots neseno pasūtījumu apskatīšanai, un pasūtījuma informācijas modulis var tikt izmantots pasūtījuma informācijas skatīšanai.
- **Ieteikumu modulis** — ieteikumi tiek parādīti, izmantojot preču izvietošanas moduli. Šis modulis atbalsta algoritmiskos un redakcijas sarakstus, kas var tikt izrādīti jebkurā lapā.

## <a name="additional-resources"></a>Papildu resursi

[Container modulis](add-container-module.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modelis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
