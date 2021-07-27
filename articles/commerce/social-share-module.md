---
title: Sociālās koplietošanas modulis
description: Šajā tēmā tiek stāstīts par sociālās koplietošanas moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0cd19f218e9fa05cd23c52fdf9bbdac6ad82a23b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357718"
---
# <a name="social-share-module"></a>Sociālo tīklu dalīšanās modulis

[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par sociālās koplietošanas moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

Sociālās koplietošanas moduļi ļauj lietotājiem koplietot e-komercijas vietnes lapas vietrāžus URL tādos sociālos plašsaziņas līdzekļos kā Facebook, Twitter, Pinterest un LinkedIn. Vietnes lapas vietrāžus URL var koplietot arī pa e-pastu. Sociālās koplietošanas moduļi bieži tiek izmantoti preču informācijas lapās (PDPs), lai palīdzētu lietotājiem koplietot produktu informāciju.

Katrs sociālās koplietošanas modulis ir konteiners sociālās koplietošanas krājumu moduļiem. Katru sociālās koplietošanas krājuma moduli var konfigurēt, lai norādītu uz noteiktu sociālo plašsaziņas līdzekļu vietni. Integrācija ar Facebook, Twitter, Pinterest, LinkedIn un e-pastu tiek atbalstīta ārpus lodziņa. Kad vietnes lietotājs atlasa sociālā plašsaziņas līdzekļa simbolu, attiecīgajai sociālo mediju vietnei tiek palaists HTML iFrame. Programmā iFrame lietotājs var pierakstīties un publicēt apskatīto lapas saturu.

Katra sociālo mediju platforma var izsekot sīkfailus, tāpēc šim modulim ir nepieciešams, lai vietnes lietotāji pieņemtu sīkfailu piekrišanas paziņojuma ziņojumu. Ja sīkfailu piekrišana nav pieņemta, modulis lapā tiks paslēpts. Lai iegūtu papildinformāciju, skatiet [Sīkfailu piekrišana](cookie-compliance.md).

Sekojošajā attēlā ir parādīts sociālās koplietošanas moduļa piemērs, kas tiek izmantots preces informācijas lapā.

![Sociālās koplietošanas moduļa piemērs.](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a>Sociālās koplietošanas moduļa rekvizīti

| Rekvizīta nosaukums             | Vērtība                 | Apraksts |
|---------------------------|-----------------------|-------------|
| Paraksts                  | Teksts | Šis rekvizīts norāda moduļa parakstu. |
| Orientācija | **Horizontāli** vai **Vertikāli**  | Šis rekvizīts nosaka sociālo mediju vienumu izkārtojuma orientāciju. |

## <a name="social-share-item-module-properties"></a>Sociālās koplietošanas vienuma moduļa rekvizīti
| Rekvizīta nosaukums             | Vērtība                 | Apraksts |
|---------------------------|-----------------------|-------------|
| Sociālie mediji              | **Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail** | Nolaižamā izvēlne ar sociālo mediju platformu sarakstu. |
| Icon |Attēls    | Tas būs attēls, kas tiks rādīta attiecīgajiem sociālajiem medijiem. Lai iegūtu ieteicamo attēlu, ko izmantot katrai platformai, skatiet sociālo mediju platformas SDK. |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a>Sociālās koplietošanas moduļa pievienošana pirkšanas lodziņa modulim

Lai pirkšanas lodziņa modulim pievienotu sociālās koplietošanas moduli, veiciet tālāk norādītās darbības.

1. Vietnē Fabrikam atlasiet **Lapas** un pēc tam atlasiet lapu **DefaultPDP**, lai atvērtu informāciju par preču lapu. 
1. Slotā **Buybox (obligāti)** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **Sociālā koplietošana** un pēc tam atlasiet **Labi**.
1. Slotā **Sociālā koplietošana** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **SocialShare** un pēc tam atlasiet **Labi**.
1. Moduļa **SocialShare** rekvizītu rūtī, sadaļā **Orientācija** atlasiet **Horizontāli**. Pēc nepieciešamības, pievienojiet parakstu.
1. Slotā **SocialShare** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.
1. Dialoglodziņā **Pievienot moduli** atlasiet moduli **SocialShareItem** un pēc tam atlasiet **Labi**.
1. Moduļa **SocialShareItem** rekvizītu rūtī, sadaļā **Sociālie mediji** atlasiet **Facebook**.
1. Moduļa **SocialShareItem** rekvizītu rūtī, sadaļā **Ikona** atlasiet **+ Pievienot attēlu**.
1. Dialoglodziņā **Multivides atlasītājs** atlasiet logotipa attēlu Facebook un pēc tam atlasiet **Labi**. Ja nav Facebook logotipa attēla, atlasiet **Augšupielādēt jaunu multivides vienumu**, lai augšupielādētu šo vienumu.
1. Pēc nepieciešamības pievienojiet un konfigurējiet papildu **SocialShareItem** moduļus.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu. Lapā tiks parādīts sociālās koplietošanas modulis.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Sīkfailu atbilstība](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]