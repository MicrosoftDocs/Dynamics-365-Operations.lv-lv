---
title: Akordeona modulis
description: Šajā tēmā aplūkoti Accordion moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e17476d745da6f498b4f3ed90d55b0d13a0264b6
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780693"
---
# <a name="accordion-module"></a>Akordeona modulis

[!include [banner](includes/banner.md)]

Šajā tēmā aplūkoti Accordion moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.

Akordeona moduļi ir konteineram līdzīgi moduļi, ko izmanto informācijas vai moduļu organizēšanai lapā, nodrošinot saliekamu atvilktnei līdzīgu iespēju. Akordeona moduli var izmantot jebkurā lapā.

Katrā akordeona modulī var pievienot vienu vai vairākus akordeona krājumu moduļus. Katrs akordeona krājumu modulis attēlo saliekamu atvilktni. Katrā akordeona krājuma modulī var pievienot vienu vai vairākus moduļus. Moduļu veidiem, kurus var pievienot akordeona krājuma modulim, nav ierobežojumu.

Attēlā zemāk redzams akordeona moduļa piemērs, kas tiek izmantots informācijas organizēšanai veikala bieži uzdoto jautājumu (FAQ) lapā.

![Akordeona moduļa piemērs.](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a>Akordeona moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | Apraksts |
|---------------|--------|-------------|
| Virsraksts | Teksts | Šis rekvizīts norāda neobligātu teksta virsrakstu akordeona modulim. |
| Izvērst visus | **Patiess** vai **Nepatiess** | Ja vērtība ir iestatīta uz **Patiess**, izvēršanas/sakļaušanas funkcionalitāte ir ieslēgta, lai visus akordeona moduļa krājumus varētu izvērst un sakļaut. |
| Mijiedarbības stils | **Neatkarīgs** vai **Izvērst tikai vienu krājumu** | Šis rekvizīts definē mijiedarbības stilu akordeona krājumiem. Ja vērtība ir iestatīta uz **Neatkarīgs**, katru akordeona krājumu var izvērst vai sakļaut neatkarīgi no citiem. Ja vērtība ir iestatīta uz **Izvērst tikai vienu krājumu**, vienlaicīgi var izvērst tikai vienu krājumu. Krājumus izvēršot, iepriekš izvērstie krājumi tiek sakļauti. |

## <a name="accordion-item-module-properties"></a>Akordeona krājuma moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | apraksts |
|----------------|--------|-------------|
| Nosaukums | Teksts | Šis rekvizīts norāda virsraksta tekstu akordeona krājuma modulim. Atlasot virsraksta reģionu, lietotāji var izvērst vai sakļaut sadaļu. |
| Izvērst pēc noklusējuma | **Patiess** vai **Nepatiess** | Ja vērtība ir iestatīta uz **Patiess**, akordeona krājums tiek izvērsts pēc noklusējuma, ielādējot lapu. |

## <a name="add-an-accordion-module-to-a-faq-page"></a>Akordeona moduļa pievienošana FAQ lapā

Lai pievienotu akordeona moduli FAQ lapai un iestatītu tās rekvizītus vietņu veidotājā, veiciet tālāk minētās darbības.

1. Dodieties uz **Lapas** un izmantojiet Fabrikam mārketinga veidni (vai jebkuru veidni, kurai nav ierobežojumu), lai izveidotu jaunu lapu, kuras nosaukums ir **Veikala FAQ**.
1. Noklusējuma lapas **galvenajam** slotam **atlasiet** daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet moduli Konteiners **un** pēc tam atlasiet **Labi**.
1. Konteinera slotā **atlasiet** daudzpunkti (**...) un** pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet moduli Summu **moduli un** pēc tam atlasiet **Labi**.
1. Akordeona moduļa rekvizītu rūtī atlasiet blakus zīmuļa simbolam **Virsraksts**.
1. Dialoglodziņa **Virsraksts** sadaļā **Virsraksta teksts** ievadiet **Bieži uzdotie jautājumi**. Tad atl. **Labi**.
1. Akordeona moduļa rekvizītu rūtī atzīmējiet izvēles rūtiņu **Rādīt izvērstu visu** un pēc tam laukā **Saziņas stils** atlasiet **Neatkarīgs**.
1. Izpildot **drošības slotu**, atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet moduli Summu **modulis Un** pēc tam atlasiet **Labi**.
1. Akordeona krājuma moduļa rekvizītu rūtī sadaļā **Nosaukums** ievadiet virsraksta tekstu (piemēram, **Kā darbojas atgriešana?**).
1. **Laika krājuma slotā** atlasiet elipsi (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet moduli Teksta bloķēšana **un** pēc tam atlasiet **Labi**.
1. Teksta bloka moduļa rekvizītu rūtī ievadiet teksta rindkopu (piemēram, **Atgriešana ir jāapstrādā, izmantojot zvanu centru. Sazinieties ar 1-800-FABRIKAM atgriešanai. Precēm ir 30 dienu atgriešanas politika. Atgriešanas ir jāuzsāk šajā laika posmā**).
1. Slotā **Akordeons** pievienojiet vēl dažus akordeona krājumu moduļus. Katrā akordeona krājuma modulī pievienojiet teksta bloka moduli, kam ir saturs.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu. Lapā tiks parādīts akordeona modulis ar pievienoto saturu.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Konteinera modulis](add-container-module.md)

[Cilnes modulis](add-tab.md)

[Teksta bloka modulis](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
