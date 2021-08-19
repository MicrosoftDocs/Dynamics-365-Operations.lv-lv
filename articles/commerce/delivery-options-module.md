---
title: Piegādes opciju modulis
description: Šajā tēmā aplūkoti piegādes opciju moduļi un paskaidrots, kā tos konfigurēt risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 69d3da5cbee5d7b921b0b0b422d838b9821e9c877d6f1951e85aeb49474bd4bc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760904"
---
# <a name="delivery-options-module"></a>Piegādes opciju modulis

[!include [banner](includes/banner.md)]

Šajā tēmā aplūkoti piegādes opciju moduļi un paskaidrots, kā tos konfigurēt risinājumā Microsoft Dynamics 365 Commerce.

Piegādes opciju moduļi ļauj klientiem izvēlēties piegādes veidu, piemēram, nosūtīšanas vai saņemšanas to tiešsaistes pasūtījumam. Piegādes adrese ir nepieciešama, lai noteiktu piegādes veidu. Ja piegādes adrese mainās, piegādes opcijas ir jāizgūst no jauna. Ja pasūtījumā ir iekļautas tikai tās preces, kas tiks saņemtas veikalā, šis modulis tiek automātiski slēpts.

Informāciju par to, kā konfigurēt piegādes veidus, skatiet sadaļās [Tiešsaistes kanāla iestatīšana](channel-setup-online.md) un [Iestatīt piegādes veidus](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Katram piegādes veidam var būt atbilstoša maksa. Papildinformāciju par to, kā konfigurēt izmaksas tiešsaistes veikalam, skatiet [Omni-Channel Advanced automātiskās izmaksas](omni-auto-charges.md).

Commerce versijā 10.0.13 piegādes opciju modulis ir atjaunināts, lai atbalstītu līdzekļus **Galvenes izmaksas bez proporcijas** un **Nosūtīšana kā rindas maksa**. Ja proporcija ir izslēgta, ir sagaidāms, ka e-komercijas darbplūsma neļaus jauktu piegādes veidu grozā esošajām precēm (tas ir, dažas preces ir atlasītas nosūtīšanai, bet citas tiek atlasītas saņemšanai). Līdzeklim **Galvenes izmaksas bez proporcijas** ir nepieciešams, lai programmā Commerce Headquarters tiktu ieslēgta opcija **Iespējot konsekventu piegādes režīma apstrādi kanāla** karodziņā. Kad līdzekļa karodziņš ir ieslēgts, nosūtīšanas izmaksas tiks piemērotas vai nu virsraksta līmenī, vai rindas līmenī atkarībā no Commerce headquarters konfigurācijas.

Fabrikam tēma atbalsta jauktu piegādes veidu, kur daži krājumi tiek atlasīti nosūtīšanai, bet citi tiek atlasīti saņemšanai. Šajā režīmā piegādes izmaksas tiks proporcionāli novērtētas visiem krājumiem, kas tiek atlasīti piegādes veidam. Lai strādātu ar jauktu piegādes veidu, vispirms ir jākonfigurē līdzeklis **Galvenes izmaksas bez proporcijas** programmā Commerce Headquarters. Plašāku informāciju par šo konfigurāciju skatiet [Samērot galvenes izmaksas, lai tās atbilstu pārdošanas rindām](pro-rate-charges-matching-lines.md).

Ja nosūtīšanas izmaksas attiecas uz rindas krājumiem, tās var tikt rādītas katra krājuma groza rindā. Lai izmantotu šo funkcionalitāti, ir jābūt ieslēgtam rekvizītam **Parādīt sūtīšanas izmaksas rindas krājumā**, kas paredzēts gan groza modulim, gan norēķināšanās modulim. Plašāku informāciju skatiet [Groza modulis](add-cart-module.md) un [Norēķināšanās modulis](add-checkout-module.md).

Ilustrācijā zemāk redzams piegādes opciju moduļa piemērs norēķināšanās lapā.

![Piegādes opciju moduļa piemērs norēķināšanās lapā.](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a>Piegādes opciju moduļa rekvizīti

| Rekvizīts | Vērtības | Apraksts |
|----------|--------|-------------|
| Virsraksts | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Izvēles virsraksts piegādes opciju modulim. |
| Pielāgotās CSS klases nosaukums | Teksts | Pielāgota Cascading Style Sheets (CSS) klases nosaukums, kas tiks izmantots šī moduļa atveidei, ja piemērojams. |
| Piegādes režīma filtra opcija | **Nefiltrēt** vai **Ar sūtīšanu nesaistīti veidi** | Vērtība, kas norāda, vai piegādes opciju modulim jāfiltrē visi piegādes veidi, kas nav saistīti ar nosūtīšanu. |
| Automātiski atlasīt piegādes opciju | **Nefiltrēt**, **Automātiski atlasīt piegādes opciju un rādīt kopsavilkumu** vai **Automātiski atlasīt piegādes opciju un nerādīt kopsavilkumu** | Šis rekvizīts automātiski piemēro pirmo pieejamo piegādes opciju, lai paņemtu, neprasot lietotājam to atlasīt. To vajadzētu izmantot tikai tad, ja ir viena pieejama piegādes opcija. Šis rekvizīts ir atbalstīts, kā Commerce versijas 10.0.19 laidienā. |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a>Piegādes opciju moduļa pievienošana norēķināšanās lapā un nepieciešamo rekvizītu iestatīšana

Piegādes opciju moduli var pievienot tikai norēķināšanās modulim. Lai iegūtu papildu informāciju par to, kā konfigurēt piegādes opciju moduli un pievienot to norēķinu lapai, skatiet sadaļu [Norēķināšanās modulis](add-checkout-module.md).

## <a name="additional-resources"></a>Papildu resursi

[Groza modulis](add-cart-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Maksājumu modulis](payment-module.md)

[Piegādes adreses modulis](ship-address-module.md)

[Saņemšanas informācijas modulis](pickup-info-module.md)

[Pasūtījumu informācijas modulis](order-confirmation-module.md)

[Dāvanu kartes modulis](add-giftcard.md)

[Tiešsaistes kanāla iestatīšana](channel-setup-online.md)

[Omni kanāla papildu automātiskās maksas](omni-auto-charges.md)

[Proporcionāla virsraksta maksu sadalīšana atbilstošajās pārdošanas rindās](pro-rate-charges-matching-lines.md)

[Iestatiet piegādes veidus](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
