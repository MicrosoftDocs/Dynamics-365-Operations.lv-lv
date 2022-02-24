---
title: Cilnes modulis
description: Šī tēma ietver cilnes moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c9d897113442f14b95539efb9fec9482be96447a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413994"
---
# <a name="tab-module"></a>Cilnes modulis

[!include [banner](includes/banner.md)]

Šī tēma ietver cilnes moduļus un apraksta, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Cilnes moduļi ir konteineram līdzīgi moduļi, kas tiek izmantoti, lai organizētu informāciju vietnes lapā cilnēs. Tos var izmantot visās lapās, kurās informācija ir jāsniedz cilnēs.

Katrā cilnes modulī var pievienot vienu vai vairākus cilnes krājumu moduļus. Katrs cilnes krājuma modulis pārstāv vienu cilni. Katrā cilnes krājuma modulī var pievienot vienu vai vairākus moduļus. Moduļu veidiem, kurus var pievienot cilnes krājuma modulim, nav ierobežojumu.

Attēlā zemāk redzams cilnes moduļa piemērs vietas lapā. Šajā piemērā ir atlasīta cilne **Piegāde**.

![Cilnes moduļa piemērs](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a>Cilnes moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | apraksts |
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
1. **Noklusējuma lapas** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Konteiners** un pēc tam atlasiet **Labi**.
1. Slotā **Konteiners** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Cilne** un pēc tam atlasiet **Labi**.
1. Cilnes moduļa rekvizītu rūtī atlasiet blakus zīmuļa simbolam **Virsraksts**.
1. Dialoglodziņa **Virsraksts** sadaļā **Virsraksta teksts** ievadiet virsraksta tekstu (piemēram, **Politikas**). Tad atl. **Labi**.
1. Slotā **Cilne** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Cilnes krājums** un pēc tam atlasiet **Labi**.
1. Cilnes krājuma moduļa rekvizītu rūtī sadaļā **Nosaukums** ievadiet virsraksta tekstu (piemēram, **Piegāde**).
1. Slotā **Cilnes krājums** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Teksta bloks** un pēc tam atlasiet **Labi**.
1. Teksta bloka moduļa rekvizītu rūtī pievienojiet tekstu sadaļā **Bagātinātais teksts** un ievadiet teksta rindkopu.
1. Slotā **Cilne** pievienojiet vēl dažus cilnes krājumu moduļus, kuriem ir virsraksti. Katrā cilnes krājuma modulī pievienojiet teksta bloka moduli, kam ir saturs.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu. Lapā tiks parādīts cilnes modulis, kas satur cilnes krājumu moduļus, kuriem ir jūsu pievienotais saturs.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Konteinera modulis](add-container-module.md)

[Akordeona modulis](add-accordion.md)

[Teksta bloka modulis](add-content-rich-block.md)
