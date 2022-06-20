---
title: Norēķināšanās modulis
description: Šajā rakstā ir aprakstīts, kā pievienot lapu pārbaudes moduli un iestatīt nepieciešamos rekvizītus.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a30d56d7edf967a3afab7442338dd9f480ef7fd0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869032"
---
# <a name="checkout-module"></a>Norēķināšanās modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā pievienot lapu pārbaudes moduli un iestatīt nepieciešamos rekvizītus.

Norēķināšanās modulis ir īpašs konteiners, kas vieso visus moduļus, kuri nepieciešami pasūtījuma izveidei. Tas sniedz pakāpenisku plūsmu, ko klients izmanto, lai ievadītu visu atbilstošo informāciju pirkuma veikšanai. Tiek fiksēta piegādes adrese, nosūtīšanas metode un norēķinu informācija. Tas sniedz arī pasūtījuma kopsavilkumu un citu informāciju, kas saistīta ar klienta pasūtījumu.

Izrakstīšanās modulis atveido datus, pamatojoties uz groza ID. Šis groza ID tiek saglabāts kā pārlūkprogrammas sīkfails. Groza ID ir nepieciešams, lai atveidotu informāciju norēķināšanās modulī, piemēram, pasūtījumā norādītās preces, kopējo summu un atlaides. 

Attēlā zemāk redzams Fabrikam norēķināšanās moduļa piemērs norēķināšanās lapā.

![Norēķināšanās moduļa piemērs.](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>Norēķināšanās moduļa rekvizīti

Norēķinu modulī tiek rādīts pasūtījuma kopsavilkums, un tā nodrošina funkcionalitāti pasūtījuma ievietošanai. Lai apkopotu visu debitora informāciju, kas ir nepieciešama, lai varētu veikt pasūtījumu, papildu moduļi ir jāpievieno norēķinu modulim. Tāpēc mazumtirgotājiem ir elastīga iespēja pievienot pielāgotus moduļus izrakstīšanās plūsmai vai izslēgt moduļus, pamatojoties uz to prasībām.

| Rekvizīta nosaukums | Vērtības | apraksts |
|----------------|--------|-------------|
| Norēķināšanās virsraksts | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Virsraksts norēķināšanās modulim. |
| Pasūtījuma kopsavilkuma virsraksts | Virsraksta teksts | Moduļa pasūtījuma kopsavilkuma sadaļas virsraksts. |
| Groza rindas krājumu virsraksts | Virsraksta teksts | Virsraksts groza rindas krājumiem, kas tiek parādīti izrakstīšanās modulī. |
| Rādīt piegādes maksu tiešsaistes krājumu | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts kā **Patiess**, piegādes izmaksas, kas ir piemērojamas rindas krājumiem, tiks parādītas groza rindās. Ja līdzeklis **Virsraksta izmaksas bez proporcijas** ir ieslēgta Commerce Headquarters, nosūtīšanas maksa tiks piemērota virsraksta līmenī, nevis rindas līmenī. Šis līdzeklis tika pievienots Commerce versijā 10.0.13. |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduļi, ko var izmantot norēķināšanās modulī

- **Piegādes adrese** — šis modulis ļauj klientam pievienot vai atlasīt pasūtījuma piegādes adresi. Plašāku informāciju par šo moduli skatiet [Nosūtīšanas adreses modulis](ship-address-module.md).

    Attēlā zemāk redzams Fabrikam piegādes adreses moduļa piemērs norēķināšanās lapā.

    ![Piegādes adreses moduļa piemērs.](./media/ecommerce-shippingaddress.PNG)

- **Piegādes opcijas** — šis modulis ļauj klientam izvēlēties pasūtījuma piegādes veidu. Plašāku informāciju par šo moduli skatiet [Piegādes opciju modulis](delivery-options-module.md).

    Attēlā zemāk redzams piegādes opciju moduļa piemērs norēķināšanās lapā.
 
    ![Piegādes opciju moduļa piemērs.](./media/ecommerce-deliveryoptions.PNG)

- **Norēķināšanās sadaļas konteiners** — šis modulis ir konteiners, kurā varat ievietot vairākus moduļus, lai izveidotu sadaļu norēķināšanās plūsmā. Piemēram, visus ar maksājumiem saistītos moduļus var ievietot šajā konteinerā, lai tos varētu parādīt kā vienu sadaļu. Šis modulis ietekmē tikai plūsmas izkārtojumu.

- **Dāvanu karte** — šis modulis ļauj klientam apmaksāt pasūtījumu, izmantojot dāvanu karti. Plašāku informāciju par šo moduli skatiet [Dāvanu kartes modulis](add-giftcard.md).

- **Lojalitātes programmas punkti** – šis modulis ļauj klientam apmaksāt pasūtījumu, izmantojot lojalitātes programmas punktus. Tas sniedz kopsavilkumu par pieejamiem punktiem un punktiem, kam beidzas termiņš, un ļauj klientam atlasīt punktu skaitu izpirkšanai. Ja klients nav pierakstījies vai nav lojalitātes programmas dalībnieks, vai arī kopējā summa grozā ir 0 (nulle), šis modulis tiek automātiski slēpts.

- **Maksājums** — šis modulis ļauj klientam apmaksāt pasūtījumu, izmantojot kredītkarti vai debitkarti. Klienti var arī sniegt norēķinu adresi atlasītajai maksāšanas opcijai. Plašāku informāciju par šo moduli skatiet [Maksājuma modulis](payment-module.md).

    Attēlā zemāk ir parādīts dāvanu karšu, lojalitātes programmas punktu, maksājumu moduļu piemērs norēķināšanās lapā.

    ![Dāvanu karšu, lojalitātes programmas punktu, maksājumu moduļu piemērs norēķināšanās lapā.](./media/ecommerce-payments.PNG)

- **Kontaktinformācija** — šis modulis ļauj klientam pievienot vai mainīt kontaktpersonas informāciju (e-pasta adresi) pasūtījumam.

- **Teksta bloks** — šis modulis ietver jebkuru ziņojumapmaiņu, ko vada satura pārvaldības sistēma (CMS). Piemēram, tas var ietvert ziņojumu, kurā teikts: “Ja rodas problēmas ar jūsu pasūtījumu, lūdzu, sazinieties ar 1-800-Fabrikam”. 

- **Izrakstīšanās noteikumi un nosacījumi** — šis modulis rāda bagātinātu tekstu, kas ietver noteikumus un nosacījumus un izvēles rūtiņu debitora ievadei. Izvēles rūtiņa nav obligāta un ir konfigurējama. Ievadi nosaka modulis, un to var izmantot kā pārbaudi pirms pasūtījuma izvietošanas aktivizēšanas, bet tā nav iekļauta pasūtījuma kopsavilkuma informācijā. Šo moduli var pievienot izrakstīšanās konteineram, izrakstīšanās sadaļas konteineram vai noteikumu un nosacījumu slotam atbilstoši biznesa vajadzībām. Ja tas ir pievienots izrakstīšanās konteineram vai izrakstīšanās sadaļas konteinera slotam, tas parādīsies kā solis norēķinu procesā. Ja tas ir pievienots noteikumu un nosacījumu slotam, tas parādīsies blakus pasūtījuma izvietošanas pogai.

    Attēlā zemāk redzams noteikumu un nosacījumu piemērs norēķināšanās lapā.

    ![Norēķinu lapas noteikumu un nosacījumu piemērs.](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit mijiedarbība

Lielākā daļa norēķināšanās informācijas, piemēram, piegādes adrese un piegādes metode, tiek glabāta grozā un apstrādāta kā pasūtījuma daļa. Vienīgais izņēmums ir kredītkartes informācija. Šī informācija tiek apstrādāta tieši, izmantojot Adyen maksājuma savienotāju. Maksājums ir autorizēts, bet to neiekasē, kamēr pasūtījums nav izpildīts.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Norēķināšanās moduļa pievienošana lapā un nepieciešamo rekvizītu iestatīšana

Lai pievienotu norēķināšanās moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Dodieties uz **Fragmenti** un atlasiet **Jauns**, lai izveidotu jaunu fragmentu.
1. Dialoglodziņā Atlasīt **fragmentu** atlasiet moduli **Paņemt**.
1. Sadaļā **Fragmenta nosaukums** ievadiet nosaukumu **Norēķināšanās fragments** un pēc tam atlasiet **Labi**.
1. Atlasiet slotu **Norēķināšanās modulis**.
1. Rekvizītu rūts labajā pusē atlasiet zīmuļa simbolu, ievadiet virsraksta tekstu laukā un pēc tam atlasiet atzīmes simbolu.
1. **Izvēlnes informācijas slotā** atlasiet elipsi (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** atlasiet piegādes **adresi**, piegādes opcijas, **·** **·** **sadaļas** Paņemt konteineru un kontaktinformācijas moduļus, pēc tam atlasiet **Labi.**
1. Modulī **Izņemiet sadaļu** Konteiners atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Moduļu **atlase** atlasiet dāvanu karti **, lojalitātes** **programmas un maksājumu** moduļus **un** pēc tam atlasiet **Labi**. Šādā veidā ir jāpārliecinās, ka visas maksājumu metodes tiek rādītas kopā vienā sadaļā.
1. Sadaļā **Noteikumi un nosacījumi** pievienojiet **Norēķināšanās noteikumi un nosacījumi** moduli, ja tas ir nepieciešams. Moduļa rekvizītu rūtī atbilstoši konfigurējiet noteikumu un nosacījumu tekstu.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu fragmentu. Daži moduļi var netikt atveidoti priekšskatījumā, jo tiem nav groza konteksta.
1. Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu fragmentā, un pēc tam atlasiet **Publicēt**, lai publicētu to.
1. Izveidojiet veidni, kas izmanto jauno norēķināšanās fragmentu.
1. Izveidojiet norēķināšanās lapu, kas izmanto jauno veidni.

## <a name="additional-resources"></a>Papildu resursi

[Groza modulis](add-cart-module.md)

[Groza ikonas modulis](cart-icon-module.md)

[Maksājumu modulis](payment-module.md)

[Piegādes adreses modulis](ship-address-module.md)

[Piegādes opciju modulis](delivery-options-module.md)

[Saņemšanas informācijas modulis](pickup-info-module.md)

[Pasūtījumu informācijas modulis](order-confirmation-module.md)

[Dāvanu kartes modulis](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
