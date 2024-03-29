---
title: Maksājumu modulis
description: Šajā rakstā ir apskatīts maksājumu modulis un skaidrots, kā to konfigurēt Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: fa1482cb73a40df5f9bc9d3037196def71accf18
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279480"
---
# <a name="payment-module"></a>Maksājumu modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir apskatīts maksājumu modulis un skaidrots, kā to konfigurēt Microsoft Dynamics 365 Commerce.

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

![Dāvanu karšu, lojalitātes programmas punktu, Adyen maksājumu moduļu piemērs norēķināšanās lapā.](./media/ecommerce-payments.PNG)

## <a name="dynamics-365-payment-connector-for-paypal"></a>Dynamics 365 Payment Connector pakalpojumam PayPal

Kopš Commerce izlaišanas 10.0.14 maksājumu modulis ir integrēts ar Dynamics 365 maksājuma savienotāju PayPal. Papildu informāciju par to, ka iestatīt un konfigurēt šo maksājuma savienotāju, skatiet [Dynamics 365 Payment Connector for PayPal](paypal.md).
 
Norēķinu lapā varat izmantot gan Adyen, gan PayPal konfigurētos savienotājus. Maksājumu modulis ir uzlabots ar papildu rekvizītiem, lai palīdzētu noteikt, ar kuru savienotāju ir jādarbojas. Detalizētu informāciju skatiet tālāk esošajā **tabulā sadaļā Atbalstītie** norēķinu **veidi un** ir primārie maksājumu moduļa rekvizīti.
  
Kad maksājumu modulis ir konfigurēts, lai izmantotu PayPal maksājuma savienotāju, izrakstīšanās lapā tiek parādīta PayPal poga. Kad klients to izsauc, maksājuma modulis izveido iframe, kas satur PayPal informāciju. Klients var pieteikties un sniegt savu PayPal informāciju šajā iframe, lai pabeigtu savu darbību. Kad debitors izvēlas maksāt ar PayPal, atlikusī bilance pasūtījumā tiks iekasēta caur PayPal.

PayPal maksājuma savienotājam nav nepieciešams norēķinu adreses modulis, jo visu ar rēķinu saistīto informāciju apstrādā PayPal tās iframe ietvaros. Tomēr ir jānorāda piegādes adreses un piegādes opciju moduļi.

Sekojošajā attēlā ir parādīts divu maksājumu moduļu piemērs norēķinu lapā, viens konfigurēts ar Adyen maksājuma savienotāju un otrs ar PayPal maksājuma savienotāju.
![Adyen un PayPal maksājumu moduļu piemērs norēķināšanās lapā.](./media/ecommerce-paypal.png)

Sekojošajā attēlā redzams piemērs no PayPal iframe, kas tiek izsaukts, izmantojot PayPal pogu. 
![, Paypal iframe piemērs izrakstīšanās lapā.](./media/ecommerce-paypal-iframe.png)

## <a name="payment-module-properties"></a>Maksājuma moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | Apraksts |
|---------------|--------|-------------|
| Virsraksts | Virsraksta teksts | Izvēles virsraksts maksājuma modulim. |
| Iframe augstums | Pikseļi | Iframe augstums pikseļos. Augstumu var pielāgot pēc nepieciešamības. |
| Radīt rēķina adresi | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts kā **Patiess**, norēķinu adrese tiks apkalpota ar Adyen, kas atrodas maksājumu moduļa iframe iekšpusē. Ja tas ir iestatīts kā **Aplams**, rēķina adrese netiks apkalpota ar Adyen, un Commerce lietotājam būs jākonfigurē modulis, lai parādītu norēķinu adresi norēķinu lapā. PayPal maksājuma savienotājam šim laukam nav ietekmes, jo rēķina adrese tiek pilnībā apstrādāta PayPal ietvaros. |
| Maksājuma stils tiek ignorēts | Kaskadētu stilu lapu (CSS) kods | Tā kā maksājuma modulis tiek viesots iframe, ir ierobežota stila iespēja. Varat iegūt kādu stilu, izmantojot šo rekvizītu. Lai ignorētu vietnes stilus, šis CSS kods ir jāielīmē kā šī rekvizīta vērtība. Vietnes veidotāja CSS atsauces un stili netiek piemēroti šim modulim. |
|Atbalstītie konkursu veidi| Virkne| Ja ir konfigurēti vairāki maksājumu savienotāji, ir jānorāda atbalstītā norēķinu veida virkne, kā norādīts Commerce Headquarters maksājumu savienotāja konfigurācijā (skatiet tālāk norādīto attēlu). Ja lauks ir tukšs, tas pēc noklusējuma tiek iestatīts uz Adyen maksājuma savienotāju. Pievienots Commerce izlaidumā 10.0.14.|
|Ir primārais maksājums|  **Patiess** vai **Nepatiess** | Ja **Patiess**, visi kļūdu ziņojumi tiks ģenerēti no primārā maksājuma savienotāja norēķinu lapā. Ja abi Adyen un PayPal maksājuma savienotāji ir konfigurēti, iestatiet Adyen uz **Patiess**, kas tika pievienots Commerce 10.0.14 laidienā.|
|Savienotāja ID lietošana| **Patiess** vai **Nepatiess** | Izmantojiet šo rekvizītu, ja vietnei ir konfigurēti vairāki maksājumu savienotāji. Ja **šis vienums** ir Patiess, savienotājiem maksājuma korelācijai jāizmanto savienotāja ID.|
|Lietot pārlūka iestatīšanas valodas kodu iFrame|  **Patiess** vai **Nepatiess** | (tikai Ahaen) Ja **patiess**, Akodēns iFrame atveidos valodu, balstoties uz vietas lietotāja pārlūka kontekstu, nevis izmantojot vietai konfigurētā Commerce kanāla valodas kodu. Pievienots Commerce izlaidumā 10.0.27.|

Sekojošajā attēlā ir parādīts **Atbalstīto norēķinu veidu** vērtības piemērs, kas iestatīts uz "PayPal" maksājuma savienotāja konfigurāciju Commerce Headquarters.
![Atbalstīto piedāvājumu veidu piemērs Commerce Headquarters.](./media/ecommerce-paymenttendertypes.png)

## <a name="billing-address"></a>Norēķinu adrese

Rēķinu izrakstīšanas adreses modulis var tikt izmantots izrakstīšanās lapā, ja Adyen maksājuma savienotāja norēķinu adreses rindas neatbilst pārējās vietnes izskatam. 

Lai norēķinu lapā izmantotu norēķinu adreses moduli, kad maksājumu modulis ir integrēts ar Adyen maksājuma savienotāju, iestatiet rekvizītu **Rādīt norēķinu adresi** uz **Aplams**, lai noklusējuma Adyen rēķina adreses vietā varētu izmantot īpašu norēķinu adreses moduli. Šādā gadījumā vietnes autoram jānorāda norēķinu adreses modulis norēķinu lapā. Adyen maksājuma savienotājs ļauj arī izmantot piegādes adresi kā norēķina adresi, lai minimizētu darbību skaitu vietnes lietotājam.

Līdzīgi maksājumu moduļiem ir pievienots **Atbalstīto norēķinu tipu** rekvizīts, kas tiek pievienots Commerce 10.0.14 laidienā. Šī rekvizīta vērtībai jābūt vienādai ar maksājuma modulī norādīto vērtību, lai nodrošinātu, ka tie sadarbojas. Adyen maksājuma savienotājam gan maksājuma modulim, gan norēķinu adreses modulim šī vērtība ir jāatstāj tukša (noklusētais stāvoklis). PayPal savienotājam atvēlētais norēķinu adreses modulis nav nepieciešams. Cita veida maksājumu savienotājiem virkne ir jāsniedz konfigurēta Commerce Headquarters.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Maksājuma moduļa pievienošana norēķinu lapā un nepieciešamo rekvizītu iestatīšana

Maksājuma moduli var pievienot tikai norēķināšanās modulim. Lai iegūtu vairāk informācijas par to, kā konfigurēt maksājuma moduli norēķinu lapai, skatiet [Norēķinu modulis](add-checkout-module.md).

## <a name="configure-the-adyen-and-paypal-payment-connectors-when-both-are-used"></a>Konfigurēt Andien un PayPal maksājumu savienotājus, ja tiek izmantoti abi

Ja gan Andien, gan PayPal maksājumu savienotāji tiks izmantoti jūsu vietnei, sekojiet šiem soļiem Commerce Site Builder, lai pievienotu maksājumu moduļus katram savienotājam pārbaudes modulim un pēc tam konfigurētu rekvizītus katram modulim.

1. PayPal maksājuma moduļa rekvizītu rūtī veiciet šādas darbības:

    1. Rekvizīta Atbalstītie norēķinu veidi **laukā** ievadiet **PayPal**.
    1. Notīriet izvēles rūtiņu rekvizītam **Ir primārais maksājuma rekvizīts**.
    1. Atzīmējiet izvēles rūtiņu Lietot savienotāja **ID rekvizītu**.

1. Rekvizītu rūtī Aībasen maksājumu modulim, sekojiet šiem soļiem:

    1. Atstājiet lauku rekvizītam Atbalstītie **norēķinu veidi** kā tukši.
    1. Atzīmējiet izvēles rūtiņu Rekvizītam **Ir primārais maksājuma rekvizīts**.
    1. Atzīmējiet izvēles rūtiņu Lietot savienotāja **ID rekvizītu**.

> [!NOTE]
> Konfigurējot Amazumtirdzniecības un PayPal savienotājus **izmantošanai** kopā, **Dynamics 365 Maksājumu savienotājam Amaksājoten** konfigurācijai jābūt pirmajā pozīcijā tiešsaistes kanāla maksājumu kontu savienotāja konfigurācijā Commerce Headquarters. Lai apstiprinātu vai mainītu savienotāja pasūtījumu, dodieties **uz tiešsaistes** veikaliem un atlasiet jūsu vietnes kanālu. Pēc **tam** **cilnē** Iestatījumi kopsavilkuma cilnē Maksājumu konti zem Savienotāja pārliecinieties, **·** **vai Dynamics 365 maksājumu savienotājs A pārtaisītajām** konfigurācijām ir pirmajā pozīcijā (tas ir, augšējā rindā) **un ka Dynamics 365 maksājumu savienotājs PayPal** konfigurācijai ir otrajā rindā. Pēc vajadzības pievienojiet vai noņemiet savienotājus, lai tos pārkārtotu.

## <a name="additional-resources"></a>Papildu resursi

[Groza modulis](add-cart-module.md)

[Groza ikonas modulis](cart-icon-module.md)

[Izrakstīšanas modulis](add-checkout-module.md)

[Piegādes adreses modulis](ship-address-module.md)

[Piegādes opciju modulis](delivery-options-module.md)

[Saņemšanas informācijas modulis](pickup-info-module.md)

[Pasūtījumu informācijas modulis](order-confirmation-module.md)

[Dāvanu kartes modulis](add-giftcard.md)

[Dynamics 365 maksājumu savienotājs pakalpojumam Adyen](dev-itpro/adyen-connector.md)

[Dynamics 365 maksājumu savienotājs pakalpojumam PayPal](paypal.md)

[Droša klientu autentifikācija, izmantojot Adyen](adyen_redirect.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
