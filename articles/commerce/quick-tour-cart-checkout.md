---
title: Pārskats par grozu un norēķināšanās lapām
description: Šajā tēmā sniegts pārskats par grozu un izrakstīšanas lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f7c708aa7f1a858e78cdbda809b90b944606022
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244795"
---
# <a name="cart-and-checkout-pages-overview"></a>Groza un norēķināšanās lapu pārskats

[!include [banner](includes/banner.md)]

Šajā tēmā sniegts pārskats par grozu un izrakstīšanas lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Elektroniskās tirdzniecības tīmekļa vietnes groza lapā ir redzamas visas preces, ko klients pievienojis grozam. Groza lapa tiek izveidota, izmantojot groza moduli. Groza modulis ir konteiners, kas vieso visus moduļus, kas ir nepieciešami, lai parādītu grozā esošās preces. Groza modulis var izmantot arī citus moduļus, lai parādītu pasūtījumu kopsavilkumu un visus veicināšanas kodus, kas ir piemēroti klienta pasūtījumam.

E-tirdzniecības tīmekļa vietnes izrakstīšanas lapa parāda darbību secību, kam klients seko, lai ievadītu visu informāciju, kas nepieciešama pasūtījuma izvietošanai. Izrakstīšanas modulī var iekļaut moduļus, kas apstrādā piegādes adresi, piegādes metodes, norēķinu informāciju, pasūtījumu kopsavilkumu un citu informāciju, kas saistīta ar klienta pasūtījumiem.

## <a name="cart-page"></a>Groza lapa

Groza lapa kalpo kā iepirkumu soma un ietver visas preces, kas ir pievienotas grozam.

Tālāk redzamajā attēlā ir parādīts groza lapas piemērs, kura izveidota, izmantojot moduļu bibliotēku un “Fabrikam” tēmu.

![Groza lapas piemērs](./media/cart2.PNG)

Groza lapas galvenā daļa parāda visas preces, ko klients pievienojis grozam. Tiek rādītas visas piemērojamās atlaides. Šīs atlaides ietver sarežģītas atlaides. Piemēram, ir "pērciet 3 preces un saņemiet 10% atlaidi" vai "pērciet pudeli un mugursomu, lai iegūtu 10% atlaidi". Pasūtījuma kopsavilkuma modulis parāda summu, kas jāmaksā pēc atlaižu, piegādes maksas, nodokļu utt. piemērošanas. Tur ir arī veicināšanas koda modulis, kas ļauj klientam piemērot vai noņemt veicināšanas kodus.

Klients var iepirkties anonīmi vai kā pierakstījies lietotājs. Ja klients ir pierakstījies, preces grozā tiek saglabātas starp sesijām. Šādā veidā klients var turpināt iepirkšanos no vairākām ierīcēm.

No groza klients var turpināt uz izrakstīšanos. Klients var uzsākt izrakstīšanos kā vieslietotājs vai kā pierakstījies lietotājs.

Lai iegūtu informāciju par to, kā autorēt lapa grozu, skatiet [Groza moduļa pievienošana lapai](add-cart-module.md).

## <a name="checkout-page"></a>Izrakstīšanas lapa

Izrakstīšanas lapa ir vieta, kur klienti ievada informāciju, kas nepieciešama pasūtījuma veikšanai.

Tālāk redzamajā attēlā ir parādīts norēķināšanās lapas piemērs, kura izveidota, izmantojot moduļu bibliotēku.

![Izrakstīšanas lapas piemērs](./media/Checkout.PNG)

Izrakstīšanas lapas galvenā daļā ir vieta, kur tiek apkopota visa pasūtījuma informācija. Šī informācija ietver piegādes adresi, piegādes opcijas un maksājuma informāciju. Izrakstīšana ir darbību secība, jo apstrādāšanai paredzētā informācija ir jāievada noteiktā secībā. Piemēram, piegādes adrese jāievada pirms piegādes izmaksu aprēķināšanas un maksājuma autorizēšanas.

### <a name="shipping-address"></a>Piegādes adrese

Piegādes adrese ir nepieciešama, ja preces ir jāpiegādā. Adreses formātu Dynamics 365 Commerce var konfigurēt katrai piegādes lokalizācijai. Piemēram, ja preces tiks piegādātas Amerikas Savienotajās Valstīs, piegādes adresē ir jāiekļauj mājas adrese, štats un pasta indekss. Piegādes adreses laukiem tiek veikta zināma pamata ievades validācija, piemēram, lai apstiprinātu burtciparu rakstzīmes, maksimālo garumu un numurus. Lai gan pašas adreses derīgums netiek verificēts, šo verifikāciju var veikt, izmantojot pielāgotus trešās puses pakalpojumus.

Piegādes adrese tiek lietota visām grozā esošajām precēm, kurām ir atlasīta opcija "piegāde". Ja izmantojat norēķināšanās plūsmu, ko nodrošina moduļu bibliotēka, atsevišķas groza preces nevar piegādāt uz dažādām adresēm. Ja šī iespēja ir nepieciešama, to var īstenot, izmantojot izrakstīšanas moduļu pielāgošanu.

Kad tiek norādīta piegādes adrese, tiek parādītas Dynamics 365 Commerce tiešsaistes veikalā pieejamās piegādes metodes. Piegādes metodes un adreses, kuras tās atbalsta, var konfigurēt Commerce.

### <a name="payment"></a>Maksājums

Nākamā darbība izrakstīšanas plūsmā ir maksājums. E-tirdzniecībā, lai veiktu pasūtījumus, var izmantot vairākas maksājumu metodes, piemēram, kredītkartes, dāvanu kartes un lojalitātes punktus. Var tikt izmantots arī šo maksājuma metožu apvienojums. Atkarībā no izmantotajām maksājuma metodēm, var būt nepieciešama papildu informācija. Piemēram, kredītkartes maksājumam ir nepieciešama rēķina nosūtīšanas adrese. Kredītkaršu maksājumi tiek apstrādāti, izmantojot Adyen Payment Connector.

#### <a name="loyalty-points"></a>Lojalitātes programmas punkti

Izrakstīšanas plūsmas laikā klients, kurš ir lojalitātes programmas dalībnieks un kam ir uzkrāti lojalitātes punkti, var pasūtījumā izpirkt šos lojalitātes punktus. Lojalitātes punktu modulis tiek parādīts tikai tad, ja klients ir lojalitātes programmas dalībnieks. Nereģistrētiem lietotājiem un vieslietotājiem šis modulis ir slēpts.

#### <a name="gift-cards"></a>Dāvanu kartes

Moduļu bibliotēka ļauj pasūtījumā izpirkt iekšējās dāvanu kartes. Lai izmantotu iekšējo dāvanu karti, klientam ir jāpierakstās. Papildu drošībai mēs iesakām pielāgot plūsmu, izmantojot iekšējo dāvanu karšu personīgo identifikācijas numuru (PIN).

### <a name="signed-in-and-guest-users"></a>Pierakstījušies lietotāji un vieslietotāji

Klients var pabeigt izrakstīšanas procesu kā vieslietotājs vai kā pierakstījies lietotājs. Ja klients pierakstās, tiek automātiski izgūta konta informācija, piemēram, saglabātās piegādes adreses un saglabātā kredītkartes informācija.

### <a name="order-summary"></a>Pasūtījuma kopsavilkums

Izrakstīšana parāda rindas preču kopsavilkumu grozā, lai klients varētu pārbaudīt pasūtījumu pirms tā veikšanas. Rindas preces nevar labot izrakstīšanas plūsmas laikā. Tomēr tiek sniegta saite uz grozu gadījumam, ja lietotājs vēlas atgriezties un rediģēt rindas preces.

Pēc tam, kad klients sniedz piegādes un rēķina informāciju, pasūtījuma kopsavilkums atspoguļo summu, kas jāmaksā pēc lojalitātes punktu, dāvanu karšu un citiem maksājumu piemērošanas.

### <a name="order-confirmation-and-email"></a>Pasūtījuma apstiprinājums un e-pasts

Kad klients veic pasūtījumu, tiek noradīts apstiprinājuma numurs. Šajā brīdī maksājums ir autorizēts, bet nav ieskaitīts. Maksājums tiks ieskaitīts tikai tad, kad pasūtījums būs izpildīts (tas ir, kad tas būs nosūtīts vai saņemts).

Kad pasūtījums ir izveidots, klientam tiek nosūtīts pasūtījuma apstiprinājuma e-pasts.

Lai iegūtu vairāk informācijas par to, kā autorēt izrakstīšanas lapu, skatiet [Izrakstīšanas moduļa pievienošana lapai](add-checkout-module.md).

## <a name="additional-resources"></a>Papildu resursi

[Mājas lapas pārskats](quick-tour-home-page.md)

[Preču papildinformācijas lapu apskats](quick-tour-pdp.md)

[Konta pārvaldības lapu pārskats](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]