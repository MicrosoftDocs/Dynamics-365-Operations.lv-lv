---
title: Piegādes opciju modulis
description: Šajā tēmā ir apskatīti piegādes opciju moduļi un tiek paskaidrots, kā tos konfigurēt programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 39e597b88afcca69623b1a23acc95e4da3873082
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818303"
---
# <a name="delivery-options-module"></a>Piegādes opciju modulis

[!include [banner](includes/banner.md)]

Šajā tēmā ir apskatīti piegādes opciju moduļi un tiek paskaidrots, kā tos konfigurēt programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Piegādes opciju moduļi ļauj klientiem izvēlēties piegādes veidu, piemēram, nosūtīšanas vai saņemšanas to tiešsaistes pasūtījumam. Piegādes adrese ir nepieciešama, lai noteiktu piegādes veidu. Ja piegādes adrese mainās, piegādes opcijas ir jāizgūst no jauna. Ja pasūtījumā ir iekļautas tikai tās preces, kas tiks saņemtas veikalā, šis modulis tiek automātiski slēpts.

Informāciju par to, kā konfigurēt piegādes veidus, skatiet sadaļās [Tiešsaistes kanāla iestatīšana](channel-setup-online.md) un [Iestatīt piegādes veidus](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Katram piegādes veidam var būt atbilstoša maksa. Papildinformāciju par to, kā konfigurēt izmaksas tiešsaistes veikalam, skatiet [Omni-Channel Advanced automātiskās izmaksas](omni-auto-charges.md).

Commerce versijā 10.0.13 piegādes opciju modulis ir atjaunināts, lai atbalstītu līdzekļus **Galvenes izmaksas bez proporcijas** un **Nosūtīšana kā rindas maksa**. Ja proporcija ir izslēgta, ir sagaidāms, ka e-komercijas darbplūsma neļaus jauktu piegādes veidu grozā esošajām precēm (tas ir, dažas preces ir atlasītas nosūtīšanai, bet citas tiek atlasītas saņemšanai). **Galvenes izmaksas bez proporcijas** līdzeklim ir nepieciešams, lai programmā Commerce Headquarters tiktu ieslēgta opcija **Iespējot konsekventu piegādes režīma apstrādi kanāla** karodziņā. Kad šis karodziņš ir ieslēgts, nosūtīšanas izmaksas tiks piemērotas vai nu virsraksta līmenī, vai rindas līmenī atkarībā no Commerce headquarters konfigurācijas.

Fabrikam tēma atbalsta jauktu piegādes veidu, kur daži krājumi tiek atlasīti nosūtīšanai, bet citi tiek atlasīti saņemšanai. Šajā režīmā piegādes izmaksas tiks proporcionāli novērtētas visiem krājumiem, kas tiek atlasīti piegādes veidam. Lai strādātu ar jauktu piegādes veidu, vispirms ir jākonfigurē līdzeklis **Galvenes izmaksas bez proporcijas** programmā Commerce Headquarters. Plašāku informāciju par šo konfigurāciju skatiet [Samērot galvenes izmaksas, lai tās atbilstu pārdošanas rindām](pro-rate-charges-matching-lines.md).

Ja nosūtīšanas izmaksas attiecas uz rindas krājumiem, tās var tikt rādītas katra krājuma groza rindā. Lai izmantotu šo funkcionalitāti, ir jābūt ieslēgtam rekvizītam **Parādīt sūtīšanas izmaksas rindas krājumā**, kas paredzēts gan groza modulim, gan norēķināšanās modulim. Plašāku informāciju skatiet [Groza modulis](add-cart-module.md) un [Norēķināšanās modulis](add-checkout-module.md).

Ilustrācijā zemāk redzams piegādes opciju moduļa piemērs norēķināšanās lapā.

![Piegādes opciju moduļa piemērs norēķināšanās lapā](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a>Piegādes opciju moduļa rekvizīti

| Rekvizīts | Vērtības | apraksts |
|----------|--------|-------------|
| Virsraksts | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Izvēles virsraksts piegādes opciju modulim. |
| Pielāgotās CSS klases nosaukums | Teksts | Pielāgota Cascading Style Sheets (CSS) klases nosaukums, kas tiks izmantots šī moduļa atveidei, ja piemērojams. |
| Piegādes režīma filtra opcija | **Nefiltrēt** vai **Ar sūtīšanu nesaistīti veidi** | Vērtība, kas norāda, vai piegādes opciju modulim jāfiltrē visi piegādes veidi, kas nav saistīti ar nosūtīšanu. |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a>Piegādes opciju moduļa pievienošana norēķināšanās lapā un nepieciešamo rekvizītu iestatīšana

Piegādes opciju moduli var pievienot tikai norēķināšanās modulim. Lai iegūtu papildu informāciju par to, kā konfigurēt piegādes opciju moduli un pievienot to norēķinu lapai, skatiet sadaļu [Norēķināšanās modulis](add-checkout-module.md).

## <a name="additional-resources"></a>Papildu resursi

[Groza modulis](add-cart-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Maksājuma modulis](payment-module.md)

[Piegādes adreses modulis](ship-address-module.md)

[Pasūtījumu informācijas modulis](order-confirmation-module.md)

[Dāvanu kartes modulis](add-giftcard.md)

[Tiešsaistes kanāla iestatīšana](channel-setup-online.md)

[Omni kanāla papildu automātiskās maksas](omni-auto-charges.md)

[Proporcionāla virsraksta maksu sadalīšana atbilstošajās pārdošanas rindās](pro-rate-charges-matching-lines.md)

[Iestatiet piegādes veidus](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
