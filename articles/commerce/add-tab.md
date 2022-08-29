---
title: Cilnes modulis
description: Šajā rakstā ir apskatīti ciļņu moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 91c79ca1b70a776352ef99d854397ada34c548e3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276978"
---
# <a name="tab-module"></a>Cilnes modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir apskatīti ciļņu moduļi un aprakstīts, kā pievienot tos vietņu lapām Microsoft Dynamics 365 Commerce.

Cilnes moduļi ir konteineram līdzīgi moduļi, kas tiek izmantoti, lai organizētu informāciju vietnes lapā cilnēs. Tos var izmantot visās lapās, kurās informācija ir jāsniedz cilnēs.

Katrā cilnes modulī var pievienot vienu vai vairākus cilnes krājumu moduļus. Katrs cilnes krājuma modulis pārstāv vienu cilni. Katrā cilnes krājuma modulī var pievienot vienu vai vairākus moduļus. Moduļu veidiem, kurus var pievienot cilnes krājuma modulim, nav ierobežojumu.

Attēlā zemāk redzams cilnes moduļa piemērs vietas lapā. Šajā piemērā ir atlasīta cilne **Piegāde**.

![Cilnes moduļa piemērs.](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a>Cilnes moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | Apraksts |
|---------------|--------|-------------|
| Virsraksts | Teksts | Šis rekvizīts norāda neobligātu teksta virsrakstu cilnes modulim. |
| Aktīvās cilnes indekss | Skaits | Šis rekvizīts norāda cilni, kas pēc noklusējuma ir jāaktivizē, kad tiek ielādēta lapa. Ja nav norādīta vērtība, pēc noklusējuma ir aktīvs ir pirmais cilnes elements. |

## <a name="tab-item-module-properties"></a>Cilnes krājuma moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | apraksts |
|---------------|--------|-------------|
| Nosaukums | Teksts | Šis rekvizīts norāda virsraksta tekstu krājuma modulim. |

## <a name="add-a-tab-module-to-a-page"></a>Cilnes moduļa pievienošana lapā

Lai pievienotu cilnes moduli lapai un iestatītu rekvizītus, veiciet šādas darbības.

1. Izmantojiet Fabrikam mārketinga veidni (vai jebkuru veidni, kurai nav ierobežojumu), lai izveidotu jaunu lapu, kuras nosaukums ir **Veikala politiku lapa**.
1. Noklusējuma lapas **galvenajam** slotam **atlasiet** daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet moduli Konteiners **un** pēc tam atlasiet **Labi**.
1. Konteinera slotā **atlasiet** daudzpunkti (**...) un** pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet moduli Cilne **un** pēc tam atlasiet **Labi**.
1. Cilnes moduļa rekvizītu rūtī atlasiet blakus zīmuļa simbolam **Virsraksts**.
1. Dialoglodziņa **Virsraksts** sadaļā **Virsraksta teksts** ievadiet virsraksta tekstu (piemēram, **Politikas**). Tad atl. **Labi**.
1. Cilnes slotā **atlasiet** daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet cilnes elementa **moduli un** pēc tam atlasiet **Labi**.
1. Cilnes krājuma moduļa rekvizītu rūtī sadaļā **Nosaukums** ievadiet virsraksta tekstu (piemēram, **Piegāde**).
1. Cilnes krājuma **slotā** atlasiet elipsi (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet moduli Teksta bloķēšana **un** pēc tam atlasiet **Labi**.
1. Teksta bloka moduļa rekvizītu rūtī pievienojiet tekstu sadaļā **Bagātinātais teksts** un ievadiet teksta rindkopu.
1. Slotā **Cilne** pievienojiet vēl dažus cilnes krājumu moduļus, kuriem ir virsraksti. Katrā cilnes krājuma modulī pievienojiet teksta bloka moduli, kam ir saturs.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu. Lapā tiks parādīts cilnes modulis, kas satur cilnes krājumu moduļus, kuriem ir jūsu pievienotais saturs.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Konteinera modulis](add-container-module.md)

[Akordeona modulis](add-accordion.md)

[Teksta bloka modulis](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
