---
title: Elektr. ziņojumapm.
description: Šajā rakstā ir sniegta pārskata un iestatīšanas informācija elektroniskajai ziņojumapmaiņai Microsoft Dynamics 365 Finanses.
author: liza-golub
ms.date: 01/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: cf9ee77b2588283f0b34f2099d6f8d78e15a5af5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934719"
---
# <a name="electronic-messaging"></a>Elektr. ziņojumapm.

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta pārskata un iestatīšanas informācija elektronisko **ziņojumu** (EM) funkcionalitātei.

Nesen valdības un likumdošanas iestādes dažādās valstīs un reģionos visā pasaulē ieviesa pārskatu veidošanas prasības uzņēmumiem, kas reģistrēti attiecīgajās valstīs vai reģionos. Prasību mērķis ir nodrošināt iespēju iegūt datus no minētajiem uzņēmumiem elektroniskā formātā tieši no sistēmām, kurās tika veikta to uzskaite, uzglabāšana un apstrāde.

EM funkcionalitāte Microsoft Dynamics 365 finansēs atbalsta dažādus procesus elektroniskai interoperaācijai starp Finansēm un sistēmām, kas sniedz iespēju veidot atskaites, iesniegt un saņemt oficiālo informāciju.

EM funkcionalitāte ir integrēta modulī **Elektronisko pārskatu veidošana** (ER). Varat iestatīt ER formātus elektroniskajiem ziņojumiem. Papildinf. sk. tēmā [Elektr. pārskatu veidošana (ER)](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

## <a name="basic-concepts-for-em-functionality"></a>EM funkcionalitātes pamatjēdzieni

EM funkcionalitāte ir balstīta uz šādiem elementiem:

- **Elektroniskais ziņojums** – pārskats vai deklarācija, kas pārskatāma vai jāpārsūta iekšēji, piemēram, pārskats, kas tiek nosūtīts nodokļu birojā.
- **Elektroniskā ziņojuma vienumi** — ieraksti, kas jāiekļauj ziņojumā, par kuru tiek ziņots.
- **Elektroniskā ziņojumu apstrāde** — darbību ķēde, kas ir jāizpilda, lai savāktu nepieciešamos datus, ģenerētu pārskatus, uzglabātu datus Azure Blob krātuvē, pārsūtītu pārskatus ārpus sistēmas, saņemtu atbildes no sistēmas ārpuses un atjauninātu datu bāzi, pamatojoties uz saņemto informāciju. Darbības ķēdē var saistīt vai atsaistīt.

Nākamajā attēlā ir parādīta EM datu plūsma.

![Elektroniskā ziņojuma datu plūsma.](media/electronic-messaging-data-flow.png)

## <a name="scenarios-supported-by-the-em-functionality"></a>EM funkcionalitātes atbalstītie scenāriji

EM funkcionalitāte atbalsta šādus scenārijus:

- Manuāli izveidojiet ziņojumus un ģenerējiet pārskatus, pamatojoties uz dažādu veidu saistītajiem eksportēšanas ER formātiem. Šie tipi ietver Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, tekstu un Microsoft Word.
- Automātiski izveidojiet un apstrādājiet ziņojumus, kas balstīti uz informāciju, kas tika pieprasīta un saņemta no iestādes, izmantojot saistīto importēšanas ER formātu.
- Apkopojiet un apstrādājiet informāciju no datu avota kā ziņojumu vienumus. Datu avots ir Finance tabula.
- Glabājiet papildu inform. un novērtējiet dažādas vērtības, izsaucot īpaši definētas izpildāmās klases saistībā ar ziņojumiem vai ziņojumu krājumiem.
- Apkopojiet inform., kas apkopota ziņojumu vienumos, sadaliet šo inform. atbilstoši ziņoj. un ģenerējiet pārskatus, kas ir saistītajos eksport. ER formātos.
- Pārsūtiet ģenerētos pārskatus uz tīmekļa pakalpojumu, izmantojot drošības informāciju, kas glabājas Azure Key Vault.
- Saņemiet atbildi no tīmekļa pakalpojuma, interpretējiet atbildi un atjauniniet datus Finance pēc vajadzības.
- Saglabājiet un pārskatiet visus ģenerētos pārskatus.
- Saglab. un pārsk. žurnāla inf., kas saistīta ar darb., kuras tiek izpildītas ziņojumam vai ziņojuma vienumam.
- Kontrolējiet apstrādi, izmantojot ziņoj. statusus un ziņoj. vienumu statusus.

## <a name="security-privileges"></a>Drošības privilēģijas

Elektroniskajiem ziņojumiem ir pieejamas šādas drošības privilēģijas.

| Drošības privilēģija           | Piekļuves līmenis | Asociācija |
|------------------------------|--------------|-------------|
| Uzturēt elektroniskos ziņojumus | Šī privilēģija sniedz pilnu piekļuvi EM funkcijai. Ja jums ir šī privilēģija, jūs varat iestatīt elektronisko ziņojumapmaiņu un palaist visus procesus. | Šī privilēģija ir iekļauta drošības pienākumā **Uzturēt pārdošanas nodokļu transakcijas**. Šis pienākums ir iekļauts drošības lomā **Grāmatvedis**. |
| Skatīt elektroniskos ziņojumus     | Šī privilēģija sniedz tikai lasīšanas piekļuvi EM funkcijai. Ja jums ir šī privilēģija, jūs varat skatīt elektroniskās ziņojumapmaiņas iestatījumus un ziņojumus. Taču jūs neko nevarat iestatīt vai palaist. | Šī privilēģija ir iekļauta drošības pienākumā **Vaicāt par pārdošanas nodokļu transakcijas statusu**. Šis pienākums ir iekļauts šādās drošības lomās:<ul><li>Iekasēšanas pārvaldnieks</li><li>Debitoru parādu darbinieks</li><li>Debitoru parādu vadītājs</li><li>Nodokļu grāmatvedis</li><li>Grāmatvedis</li><li>Uzskaites vadītājs</li><li>Uzskaites supervizors</li><li>Pārdošanas daļas vadītājs</li><li>Kreditoriem maksājamo parādu darbinieks</li></ul> |
| Apstrādāt elektroniskos ziņojumus  | Šī privilēģija sniedz piekluvi tikai lapām **Elektroniskie ziņojumi** un **Elektronisko ziņojumu elementi**. Ja jums ir šī privilēģija, jūs varat palaist visu apstrādi, kas tiek izsaukta no šīm lapām. | Šī privilēģija ir iekļauta drošības pienākumā **Darbināt elektroniskos ziņojumus**. Šis pienākums ir iekļauts drošības lomā **Elektronisko ziņojumu operators**. |

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>Valstij specifiskās regulēšanas funkcijas, ko atbalsta EM funkcionalitāte

Tabulā ir sniegta informācija par dažām valstij specifiskām regulēšanas funkcijām, ko atbalsta EM funkcionalitāte.

| Valsts/reģions     | Līdzekļa nosaukums | Līdzekļu demonstrācijas ierakstīšana |
|-------------|--------------|------------------------|
| Spānija       | [Tūlītēja informācijas piegāde par PVN (Suminilla Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Ungārija     | [Tiešsaistes rēķinu izrakstīšanas sistēma](../localizations/emea-hun-online-invoicing.md) | |
| Apvienotā Karaliste | [Nodokļu digitalizācija (Making Tax Digital - MTD) – PVN deklarācijas iesniegšana](../localizations/emea-gbr-mtd-vat-integration.md) | [Finanses un operācijas: Lielbritānijas digitālais nodoklis - PVN deklarācija sistēmā Dynamics 365](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Lietuva   | [i.SAF pārskatu veidošana](../localizations/emea-ltu-isaf.md) | |
| Polija      | [PVN deklarācija ar reģistriem (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 finanses: MAKS./DARBA PVN audita reģistri](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Nīderlande | [PVN deklarācija Nīderlandēm](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Čehijas Republika | [PVN deklarācija](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brazīlija      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| Krievija      | [PVN deklarācija](../localizations/rus-vat-declaration.md) | |
| Krievija      | [Uzskaites pārskati elektroniskā formātā](../localizations/rus-accounting-reporting.md) | |
| Krievija      | [Peļņas nodokļu deklarācija](../localizations/rus-profit-tax-declaration.md) | |
| Krievija      | [Likmēto nodokļu deklarācija](../localizations/rus-assessed-tax-declaration.md) | |
| Krievija      | [Transporta nodokļu deklarācija](../localizations/rus-transport-tax-declaration.md) | |
| Krievija      | [Zemes nodokļu deklarācija](../localizations/rus-land-tax-declaration.md) | |
| Norvēģija      | [PVN atgriešana ar tiešo iesniegšanu Altinn](../localizations/emea-nor-vat-return.md) | [Jauna PVN atgriešana ar tiešo iesniegšanu Altinn dynamics 365 finansēs](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/new-vat-return-with-direct-submission-to-altinn-in-dynamics-365-finance-december-1-2021) |
| Francija      | [PVN deklarācija (Francija)](../localizations/emea-fra-VAT-declaration-preview-France.md) | |
| Austrija     | [PVN deklarācija (Austrija)](../localizations/emea-aut-vat-declaration-austria.md) | |
| Vācija     | [PVN deklarācija (Vācija)](../localizations/emea-deu-vat-declaration-germany.md) | |
| Nīderlande | [PVN deklarācija Nīderlandēm](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Zviedrija      | [PVN deklarācija (Zviedrija)](../localizations/emea-swe-VAT-declaration-Sweden.md) | |
| Šveice | [PVN deklarācija (Šveice)](../localizations/emea-che-vat-declaration-switzerland.md) | |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

