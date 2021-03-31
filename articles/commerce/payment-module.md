---
title: Maksājuma modulis
description: Šajā tēmā ir apskatīti maksājuma modulis un tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d9c0956e30d413f5ae695cf75b06fb58711b2944
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222500"
---
# <a name="payment-module"></a>Maksājumu modulis

[!include [banner](includes/banner.md)]

Šajā tēmā ir apskatīti maksājuma modulis un tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.

Maksājuma modulis ļauj klientiem apmaksāt pasūtījumus, izmantojot kredītkartes vai debitkartes. Maksājumu integrāciju šim modulim nodrošina Dynamics 365 Payment Connector for Adyen. Papildu informāciju par to, ka iestatīt un konfigurēt maksājuma savienotāju, skatiet [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).  

Kopš Commerce versijas 10.0.14 izlaišanas maksājuma modulis arī ir integrēts ar Dynamics 365 PayPal maksājuma savienotāju, lai klienti varētu apmaksāt pasūtījumus, izmantojot PayPal. Papildu informāciju par to, ka iestatīt un konfigurēt Dynamics 365 PayPal maksājuma savienotāju, skatiet [Dynamics 365 Payment Connector for PayPal](paypal.md). 

## <a name="dynamics-365-payment-connector-for-adyen"></a>Dynamics 365 maksājumu savienotājs pakalpojumam Adyen 

Maksājumu modulī tiek viesota maksājuma informācija, kas tiek piegādāta, izmantojot Adyen HTML vienrindas kadrā (iframe). Maksājumu modulis mijiedarbojas ar Commerce Scale Unit, lai izgūtu informāciju par Adyen maksājumu. Kā daļu no Commerce Scale Unit mijiedarbības maksājuma modulis var ļaut izsniegt rēķina adreses informāciju vai nu iframe, izmantojot Adyen, vai kā atsevišķs modulis. Fabrikam tēmā rēķina adrese ir iespējota kā atsevišķs modulis. Šī pieeja atļauj vairāk formatēšanas elastību, jo adreses rindas var atveidot tā, ka tās atgādina piegādes adreses rindas.

Maksājuma modulis arī ir pierakstījies, lai saglabātu informāciju par maksājumu. Maksājuma informācija un rēķina adrese tiek saglabātas un pārvaldītas, izmantojot Adyen maksājuma savienotāju.

Maksājuma modulis sedz visas pasūtījuma izmaksas, kas nav iekļautas lojalitātes programmas punktos vai dāvanu kartē. Ja pasūtījuma kopsummu pilnībā sedz lojalitātes programmas punkti vai dāvanu karšu kredīti, maksājuma modulis tiks slēpts, un klients varēs veikt pasūtījumu bez tā.

Adyen maksājuma savienotājs atbalsta arī drošu klientu autentifikāciju (SCA). Eiropas Savienības (ES) pārskatītās maksājumu pakalpojumu direktīvas (PSD2) daļa prasa, lai tiešsaistes pircēji tiktu autentificēti ārpus to tiešsaistes iepirkšanās pieredzes, kad tie izmanto elektronisko maksājumu metodi. Norēķinu plūsmas laikā klienti tiek novirzīti uz viņu bankas vietni, un pēc autentifikācijas tie tiek novirzīti uz Commerce Checkout plūsmu. Šīs novirzīšanas laikā informācija, ko klients ievadījis norēķinu plūsmas laikā (piemēram, piegādes adrese, piegādes opcijas, dāvanu kartes informācija un lojalitātes informācija) saglabāsies. Pirms jūs varat ieslēgt Adyen maksājuma savienotāja līdzekli, maksājuma savienotājam ir jābūt konfigurētam, lai varētu veikt programmas Commerce Headquarters SCA. Plašāku informāciju skatiet [Droša klientu autentifikācija, izmantojot Adyen](adyen_redirect.md). Šis līdzeklis tika iespējots Commerce laidienā 10.0.12.

> [!NOTE]
> Adyen maksājuma savienotājam, iFrame modulis maksājuma modulī var tikt atveidots tikai tad, ja pievienojat Adyen vietrādi URL savam vietnes atļautajam sarakstam. Lai veiktu šo darbību, pievienojiet **\*.adyen.com** **child-src**, **connect-src**, **img-src**, **script-src** un **style-src** jūsu vietnes satura drošības politikas direktīvām. Papildinformāciju skatiet [Pārvaldīt satura drošības politiku](manage-csp.md). 

Ilustrācijā zemāk ir parādīts dāvanu karšu, lojalitātes programmas, Adyen maksājumu moduļu piemērs norēķināšanās lapā.

![Dāvanu karšu, lojalitātes programmas punktu, Adyen maksājumu moduļu piemērs norēķināšanās lapā](./media/ecommerce-payments.PNG)

## <a name="dynamics-365-payment-connector-for-paypal"></a>Dynamics 365 maksājumu savienotājs pakalpojumam PayPal

Kopš Commerce izlaišanas 10.0.14 maksājumu modulis ir integrēts ar Dynamics 365 maksājuma savienotāju PayPal. Papildu informāciju par to, ka iestatīt un konfigurēt šo maksājuma savienotāju, skatiet [Dynamics 365 Payment Connector for PayPal](paypal.md).
 
Norēķinu lapā varat izmantot gan Adyen, gan PayPal konfigurētos savienotājus. Maksājumu modulis ir uzlabots ar papildu rekvizītiem, lai palīdzētu noteikt, ar kuru savienotāju ir jādarbojas. Lai iegūtu sīkāku informāciju, skatiet **Atbalstītos norēķinu veidus** un **Primārais maksājums** moduļa rekvizītus sekojošajā tabulā.
  
Kad maksājumu modulis ir konfigurēts, lai izmantotu PayPal maksājuma savienotāju, izrakstīšanās lapā tiek parādīta PayPal poga. Kad klients to izsauc, maksājuma modulis izveido iframe, kas satur PayPal informāciju. Klients var pieteikties un sniegt savu PayPal informāciju šajā iframe, lai pabeigtu savu darbību. Kad debitors izvēlas maksāt ar PayPal, atlikusī bilance pasūtījumā tiks iekasēta caur PayPal.

PayPal maksājuma savienotājam nav nepieciešams norēķinu adreses modulis, jo visu ar rēķinu saistīto informāciju apstrādā PayPal tās iframe ietvaros. Tomēr ir jānorāda piegādes adreses un piegādes opciju moduļi.

Sekojošajā attēlā ir parādīts divu maksājumu moduļu piemērs norēķinu lapā, viens konfigurēts ar Adyen maksājuma savienotāju un otrs ar PayPal maksājuma savienotāju.
![Adyen un PayPal maksājumu moduļu piemērs norēķināšanās lapā](./media/ecommerce-paypal.png)

Sekojošajā attēlā redzams piemērs no PayPal iframe, kas tiek izsaukts, izmantojot PayPal pogu. 
![Paypal iframe piemērs izrakstīšanās lapā](./media/ecommerce-paypal-iframe.png)

## <a name="payment-module-properties"></a>Maksājuma moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | apraksts |
|---------------|--------|-------------|
| Virsraksts | Virsraksta teksts | Izvēles virsraksts maksājuma modulim. |
| Iframe augstums | Pikseļi | Iframe augstums pikseļos. Augstumu var pielāgot pēc nepieciešamības. |
| Radīt rēķina adresi | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts kā **Patiess**, norēķinu adrese tiks apkalpota ar Adyen, kas atrodas maksājumu moduļa iframe iekšpusē. Ja tas ir iestatīts kā **Aplams**, rēķina adrese netiks apkalpota ar Adyen, un Commerce lietotājam būs jākonfigurē modulis, lai parādītu norēķinu adresi norēķinu lapā. PayPal maksājuma savienotājam šim laukam nav ietekmes, jo rēķina adrese tiek pilnībā apstrādāta PayPal ietvaros. |
| Maksājuma stils tiek ignorēts | Kaskadētu stilu lapu (CSS) kods | Tā kā maksājuma modulis tiek viesots iframe, ir ierobežota stila iespēja. Varat iegūt kādu stilu, izmantojot šo rekvizītu. Lai ignorētu vietnes stilus, šis CSS kods ir jāielīmē kā šī rekvizīta vērtība. Vietnes veidotāja CSS atsauces un stili netiek piemēroti šim modulim. |
|Atbalstītie konkursu veidi| Virkne| Ja ir konfigurēti vairāki maksājumu savienotāji, jums jānodrošina atbalstītā norēķinu tipa virkne, kā definēts Commerce Headquarters maksājuma savienotāja konfigurācijā (skatiet attēlu šādiem jautājumiem). Ja lauks ir tukšs, tas pēc noklusējuma tiek iestatīts uz Adyen maksājuma savienotāju. Pievienots Commerce izlaidumā 10.0.14.|
|Ir primārais maksājums|  **Patiess** vai **Nepatiess** | Ja **Patiess**, visi kļūdu ziņojumi tiks ģenerēti no primārā maksājuma savienotāja norēķinu lapā. Ja abi Adyen un PayPal maksājuma savienotāji ir konfigurēti, iestatiet Adyen uz **Patiess**, kas tika pievienots Commerce 10.0.14 laidienā.|

Sekojošajā attēlā ir parādīts **Atbalstīto norēķinu veidu** vērtības piemērs, kas iestatīts uz "PayPal" maksājuma savienotāja konfigurāciju Commerce Headquarters.
![Commerce Headquarters atbalstīto norēķinu veidu piemērs](./media/ecommerce-paymenttendertypes.png)

## <a name="billing-address"></a>Norēķinu adrese

Rēķinu izrakstīšanas adreses modulis var tikt izmantots izrakstīšanās lapā, ja Adyen maksājuma savienotāja norēķinu adreses rindas neatbilst pārējās vietnes izskatam. 

Lai norēķinu lapā izmantotu norēķinu adreses moduli, kad maksājumu modulis ir integrēts ar Adyen maksājuma savienotāju, iestatiet rekvizītu **Rādīt norēķinu adresi** uz **Aplams**, lai noklusējuma Adyen rēķina adreses vietā varētu izmantot īpašu norēķinu adreses moduli. Šādā gadījumā vietnes autoram jānorāda norēķinu adreses modulis norēķinu lapā. Adyen maksājuma savienotājs ļauj arī izmantot piegādes adresi kā norēķina adresi, lai minimizētu darbību skaitu vietnes lietotājam.

Līdzīgi maksājumu moduļiem ir pievienots **Atbalstīto norēķinu tipu** rekvizīts, kas tiek pievienots Commerce 10.0.14 laidienā. Šī rekvizīta vērtībai jābūt vienādai ar maksājuma modulī norādīto vērtību, lai nodrošinātu, ka tie sadarbojas. Adyen maksājuma savienotājam gan maksājuma modulim, gan norēķinu adreses modulim šī vērtība ir jāatstāj tukša (noklusētais stāvoklis). PayPal savienotājam atvēlētais norēķinu adreses modulis nav nepieciešams. Cita veida maksājumu savienotājiem virkne ir jāsniedz konfigurēta Commerce Headquarters.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Maksājuma moduļa pievienošana norēķinu lapā un nepieciešamo rekvizītu iestatīšana

Maksājuma moduli var pievienot tikai norēķināšanās modulim. Lai iegūtu vairāk informācijas par to, kā konfigurēt maksājuma moduli norēķinu lapai, skatiet [Norēķinu modulis](add-checkout-module.md).

Ja ir nepieciešami abi Adyen un PayPal maksājumu savienotāji, pievienojiet abus moduļus maksājumu sadaļā. Pārliecinieties, ka **Atbalstīto norēķinu veidu** rekvizīta vērtība ir konfigurēta pakalpojumam PayPal, un atstājiet to tukšu pakalpojumam Adyen. Iestatiet arī rekvizītu **Primārais maksājums** uz **Patiess** pakalpojumam Adyen.

## <a name="additional-resources"></a>Papildu resursi

[Groza modulis](add-cart-module.md)

[Groza ikonas modulis](cart-icon-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Piegādes adreses modulis](ship-address-module.md)

[Piegādes opciju modulis](delivery-options-module.md)

[Saņemšanas informācijas modulis](pickup-info-module.md)

[Pasūtījumu informācijas modulis](order-confirmation-module.md)

[Dāvanu kartes modulis](add-giftcard.md)

[Dynamics 365 maksājumu savienotājs pakalpojumam Adyen](dev-itpro/adyen-connector.md)

[Dynamics 365 maksājumu savienotājs pakalpojumam PayPal](paypal.md)

[Droša klientu autentifikācija, izmantojot Adyen](adyen_redirect.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]