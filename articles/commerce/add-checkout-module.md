---
title: Norēķināšanās modulis
description: Šajā tēmā ir aprakstīts, kā pievienot norēķināšanas moduli lapā un iestatīt nepieciešamos rekvizītus.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4b810441fd25d41ee0893b119b4f7d91e7435d21
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697087"
---
# <a name="checkout-module"></a>Norēķināšanās modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā pievienot norēķināšanas moduli lapā un iestatīt nepieciešamos rekvizītus.

## <a name="overview"></a>Pārskats

Norēķināšanās modulis ir īpašs konteiners, kas vieso visus moduļus, kuri nepieciešami pasūtījuma izveidei. Norēķināšanās modulī var iekļaut moduļus, kas apstrādā piegādes adresi, piegādes metodes, norēķinu informāciju, pasūtījumu kopsavilkumu un citu informāciju, kas saistīta ar klienta pasūtījumu. Tas sniedz pakāpenisku plūsmu, ko klients izmanto, lai ievadītu visu atbilstošo informāciju pirkuma veikšanai.

Izrakstīšanās modulis atveido datus, pamatojoties uz groza ID. Šis groza ID tiek saglabāts kā pārlūkprogrammas sīkfails. Groza ID ir nepieciešams, lai atveidotu informāciju norēķināšanās modulī, piemēram, pasūtījumā norādītās preces, kopējo summu un atlaides.

## <a name="checkout-module-properties"></a>Norēķināšanās moduļa rekvizīti

Norēķināšanās modulī tiek viesots moduļu kopums. Platuma rekvizīts ļauj norādīt, vai elementiem izrakstīšanās modulī ir jāatbilst tā platumam vai jāaizpilda ekrāns.

Norēķināšanās modulim ir vairāki sloti, piemēram, **Norēķināšanās informācijas** slots, **Pasūtījuma kopsavilkuma**  slots un slots **Veikt pasūtījumu**. Katrs slots atbalsta moduļu kopu, kas tiks parādīta lapā noteiktā izkārtojumā. Piemēram, **Norēķināšanās informācijas** slots ietver visus moduļus, kas nepieciešami, lai aktivizētu norēķināšanos, piemēram, piegādes adreses un maksājuma metodes moduļus. Slota **Pasūtījuma kopsavilkums** rāda pasūtījuma kopsavilkumu un atbalsta darbību pasūtījuma veikšanai. Slots **Veikt pasūtījumu** atbalsta arī darbību pasūtījuma veikšanai. Pasūtījumu veikšanas moduļus var definēt divos slotos, lai optimizētu pasūtījumu veikšanas procesu no dažādām platformām.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduļi, ko var izmantot norēķināšanās modulī

- **Piegādes adrese** — šis modulis ļauj klientam pievienot vai atlasīt pasūtījuma piegādes adresi. Ja klients ir pierakstījies, tiek rādītas visas adreses, kas iepriekš tika saglabātas šim klientam. Klients pēc tam veikt atlasi no šīm adresēm. Klients var arī pievienot jaunu adresi. Piegādes adrese tiek izmantota visām precēm pasūtījumā, kuras nepieciešams piegādāt. To nevar pielāgot atsevišķiem rindas krājumiem. Piegādes adreses formāti ir definēti katrai valstij vai reģionam, un šis modulis lieto valsts/reģiona specifiskos noteikumus. Kaut arī šis modulis nenodrošina adrešu validāciju, adreses validāciju var īstenot ar pielāgošanu. Ja pasūtījumā ir iekļautas tikai tās preces, kas tiks saņemtas veikalā, šis modulis tiek automātiski slēpts.
- **Piegādes opcijas** — šis modulis ļauj klientam izvēlēties pasūtījuma piegādes opciju. Piegādes opcijas ir balstītas uz piegādes adresi. Ja piegādes adrese ir mainīta, piegādes opcijas ir jāizgūst no jauna. Ja pasūtījumā ir iekļautas tikai tās preces, kas tiks saņemtas veikalā, šis modulis tiek automātiski slēpts.
- **Norēķināšanās sadaļas konteiners** — šis modulis ir konteiners, kurā varat ievietot vairākus moduļus, lai izveidotu sadaļu norēķināšanās plūsmā. Piemēram, visus ar maksājumiem saistītos moduļus var ievietot šajā konteinerā, lai tos varētu parādīt kā vienu sadaļu. Šis modulis ietekmē tikai plūsmas izkārtojumu.
- **Dāvanu karte** — šis modulis ļauj klientam apmaksāt pasūtījumu, izmantojot dāvanu karti. Tas atbalsta tikai Microsoft Dynamics 365 Commerce dāvanu kartes. Pasūtījumam var lietot vienu vai vairākas dāvanu kartes. Ja dāvanu kartes bilance nesedz summu grozā, dāvanu karti var apvienot ar citu maksājuma metodi. Dāvanu kartes var izpirkt tikai tad, ja klients ir pierakstījies.
- **Lojalitātes programmas punkti** – šis modulis ļauj klientam apmaksāt pasūtījumu, izmantojot lojalitātes programmas punktus. Tas sniedz kopsavilkumu par pieejamiem punktiem un punktiem, kam beidzas termiņš, un ļauj klientam atlasīt punktu skaitu izpirkšanai. Ja klients nav pierakstījies vai nav lojalitātes programmas dalībnieks, vai arī kopējā summa grozā ir 0 (nulle), šis modulis tiek automātiski slēpts.
- **Kredītkarte** — šis modulis ļauj klientam apmaksāt pasūtījumu, izmantojot kredītkarti. Ja kopējā summa grozā tiek segta ar lojalitātes programmas punktiem vai dāvanu karti, vai ja tā ir 0 (nulle), šis modulis tiek automātiski slēpts. Kredītkaršu integrāciju nodrošina Adyen maksājumu savienotājs. Lai iegūtu vairāk informācijas par to, kā izmantot šo savienotāju, skatiet tēmu [Adyen maksājumu savienotājs](https://).
- **Norēķinu adrese** — šis modulis ļauj klientam sniegt norēķinu informāciju. Izmantojot Adyen, šī informācija tiek apstrādāta kopā ar kredītkartes informāciju. Šajā modulī ir ietverta opcija, kas ļauj klientiem izmantot savu norēķinu adresi kā piegādes adresi.
- **Kontaktinformācija** — šis modulis ļauj klientam pievienot vai mainīt kontaktpersonas informāciju (e-pasta adresi) pasūtījumam.
- **Veikt pasūtījumu** — šis modulis ļauj klientam veikt pasūtījumu.
- **Bagātinātā satura bloks** — šis modulis ietver jebkuru ziņojumapmaiņu, ko vada satura pārvaldības sistēma (CMS). Piemēram, tas var ietvert ziņojumu, kurā teikts: “Ja rodas problēmas ar jūsu pasūtījumu, lūdzu, sazinieties ar 1-800-FABRIKAM”. 
- **Pasūtījuma kopsavilkums** — šis modulis parāda pasūtījuma izmaksu sadalījumu.
- **Pasūtījuma rindas elementi** — šis modulis rāda elementu kopsavilkumu, kas tiks iekļauti pasūtījumā.

## <a name="retail-server-interaction"></a>Mijiedarbība ar mazumtirdzniecības serveri

Lielākā daļa norēķināšanās informācijas, piemēram, piegādes adrese un piegādes metode, tiek glabāta grozā un apstrādāta kā pasūtījuma daļa. Vienīgais izņēmums ir kredītkartes informācija. Šī informācija tiek apstrādāta tieši, izmantojot Adyen maksājuma savienotāju. Maksājums ir autorizēts, bet nav iekasēts.

## <a name="add-a-checkout-module-to-a-new-page-and-set-the-required-properties"></a>Norēķināšanās moduļa pievienošana jaunā lapā un nepieciešamo rekvizītu iestatīšana

Lai pievienotu norēķināšanās moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Fragments \>Jauns fragments** un nosauciet jauno fragmentu par **Norēķināšanās fragmentu**.
1. Pievienojiet norēķināšanās moduli fragmentam.
1. Pievienojiet virsrakstu norēķināšanās modulim.
1. Slotā **Norēķināšanās informācija** pievienojiet piegādes adresi, piegādes opcijas, norēķināšanās sadaļas konteineru un kontaktpersonu informācijas moduļus. Slotā **Norēķināšanās informācija** ir jābūt četrām sadaļām.
1. Norēķināšanās sadaļas konteinera modulī pievienojiet dāvanu karti, lojalitātes programmas punktus un kredītkaršu moduļus. Šādā veidā ir jāpārliecinās, ka visas maksājumu metodes tiek rādītas kopā vienā sadaļā.
1. Slotā **Pasūtījuma kopsavilkums** pievienojiet pasūtījuma kopsavilkumu, ievietojiet pasūtījumu un bagātinātā satura bloka moduļus.
1. Bagātinātā satura bloka modulī pievienojiet šādu tekstu: **Jautājumiem saistībā ar jūsu pasūtījumu, sazinieties ar 1-800-FABRIKAM.**
1. Slotā **Veikt pasūtījumu** pievienojiet moduli Veikt pasūtījumu.
1. Atlasiet **Saglabāt**. Daži moduļi var netikt atveidoti priekšskatījumā, jo tiem nav groza konteksta.
1. Pārbaudiet fragmentu un publicējiet to.
1. Izveidojiet veidni, kas izmanto jauno norēķināšanās fragmentu.
1. Izveidojiet norēķināšanās lapu, kas izmanto jauno veidni.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Container modulis](add-container-module.md)

[Iegādes lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Pasūtījuma apstiprinājuma modelis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)
