---
title: Maksājuma modulis
description: Šajā tēmā ir apskatīti maksājuma modulis un tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 4267391edaf70ec645933b2c5c08a72735f52894
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818330"
---
# <a name="payment-module"></a>Maksājuma modulis

[!include [banner](includes/banner.md)]

Šajā tēmā ir apskatīti maksājuma modulis un tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Maksājuma modulis ļauj klientiem apmaksāt pasūtījumus, izmantojot kredītkartes vai debitkartes. Maksājumu integrāciju šim modulim nodrošina Dynamics 365 Payment Connector for Adyen. Papildu informāciju par to, ka iestatīt un konfigurēt maksājuma savienotāju, skatiet [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).

Maksājumu modulī tiek viesota maksājuma informācija, kas tiek piegādāta, izmantojot Adyen HTML vienrindas kadrā (iframe). Maksājumu modulis mijiedarbojas ar Commerce Scale Unit, lai izgūtu informāciju par Adyen maksājumu. Kā daļu no Commerce Scale Unit mijiedarbības maksājuma modulis var ļaut izsniegt rēķina adreses informāciju vai nu iframe, vai kā atsevišķs modulis. Fabrikam tēmā rēķina adrese tiek rādīta atsevišķā modulī. Šī pieeja atļauj vairāk formatēšanas elastību, jo adreses rindas var atveidot tā, ka tās atgādina piegādes adreses rindas.

Maksājuma modulis arī ir pierakstījies, lai saglabātu informāciju par maksājumu. Maksājuma informācija un rēķina adrese tiek saglabātas un pārvaldītas, izmantojot Adyen maksājuma savienotāju.

Maksājuma modulis sedz visas pasūtījuma izmaksas, kas nav iekļautas lojalitātes programmas punktos vai dāvanu kartē. Ja pasūtījuma kopsummu pilnībā sedz lojalitātes programmas punkti vai dāvanu karšu kredīti, maksājuma modulis tiks slēpts, un klients varēs veikt pasūtījumu bez tā.

Adyen maksājuma savienotājs atbalsta arī drošu klientu autentifikāciju (SCA). Eiropas Savienības (ES) maksājumu pakalpojumu direktīvas 2.0 (PSD 2.0) daļa prasa, lai tiešsaistes pircēji tiktu autentificēti ārpus to tiešsaistes iepirkšanās pieredzes, kad tie izmanto elektronisko maksājumu metodi. Norēķinu plūsmas laikā klienti tiek novirzīti uz savu banku vietni. Pēc autentifikācijas tie tiek novirzīti uz Commerce norēķinu plūsmu. Šīs novirzīšanas laikā informācija, ko klients ievadījis norēķinu plūsmā (piemēram, piegādes adrese, piegādes opcijas, dāvanu kartes informācija un lojalitātes informācija) saglabāsies. Pirms jūs varat ieslēgt šo līdzekli, maksājuma savienotājam ir jābūt konfigurētam, lai varētu veikt programmas Commerce Headquarters SCA. Plašāku informāciju skatiet [Droša klientu autentifikācija, izmantojot Adyen](adyen_redirect.md).

Ilustrācijā zemāk ir parādīts dāvanu karšu, lojalitātes programmas, maksājumu moduļu piemērs norēķināšanās lapā.

![Dāvanu karšu, lojalitātes programmas, maksājumu moduļu piemērs norēķināšanās lapā](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a>Maksājuma moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | apraksts |
|---------------|--------|-------------|
| Virsraksts | Virsraksta teksts | Izvēles virsraksts maksājuma modulim. |
| Iframe augstums | Pikseļi | Iframe augstums pikseļos. Augstumu var pielāgot pēc nepieciešamības. |
| Radīt rēķina adresi | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts kā **Patiess**, norēķinu adrese tiks apkalpota ar Adyen, kas atrodas maksājumu moduļa iframe iekšpusē. Ja tas ir iestatīts kā **Aplams**, rēķina adrese netiks apkalpota ar Adyen, un Commerce lietotājam būs jākonfigurē modulis, lai parādītu norēķinu adresi norēķinu lapā. |
| Maksājuma stils tiek ignorēts | Kaskadētu stilu lapu (CSS) kods | Tā kā maksājuma modulis tiek viesots iframe, ir ierobežota stila iespēja. Varat iegūt kādu stilu, izmantojot šo rekvizītu. Lai ignorētu vietnes stilus, šis CSS kods ir jāielīmē kā šī rekvizīta vērtība. Vietnes veidotāja CSS atsauces un stili netiek piemēroti šim modulim. |

## <a name="billing-address"></a>Norēķinu adrese

Maksājuma moduļa klienti sniedz norēķinu adresi maksājuma informācijai. Tas arī ļauj izmantot piegādes adresi kā rēķina adresi, lai atvieglotu un paātrinātu izrakstīšanās plūsmu. Ja rekvizīts **Rādīt norēķinu adresi** ir iestatīts kā **Aplams**, maksājuma modulis ir jākonfigurē norēķinu lapā.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Maksājuma moduļa pievienošana norēķinu lapā un nepieciešamo rekvizītu iestatīšana

Maksājuma moduli var pievienot tikai norēķināšanās modulim. Lai iegūtu vairāk informācijas par to, kā konfigurēt maksājuma moduli norēķinu lapai, skatiet [Norēķinu modulis](add-checkout-module.md).

## <a name="additional-resources"></a>Papildu resursi

[Groza modulis](add-cart-module.md)

[Groza ikonas modulis](cart-icon-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Piegādes adreses modulis](ship-address-module.md)

[Piegādes opciju modulis](delivery-options-module.md)

[Pasūtījumu informācijas modulis](order-confirmation-module.md)

[Dāvanu kartes modulis](add-giftcard.md)

[Dynamics 365 maksājumu savienotājs pakalpojumam Adyen](dev-itpro/adyen-connector.md)

[Droša klientu autentifikācija, izmantojot Adyen](adyen_redirect.md)
