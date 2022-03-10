---
title: Elektr. ziņojumapm.
description: Šajā tēmā ir sniegts apskats par elektronisko ziņojumapmaiņu un tās iestatīšanai nepieciešamo informāciju programmā Microsoft Dynamics 365 Finance.
author: liza-golub
ms.date: 06/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 191abc37b7c349aaf3c9e871fe2f1885eec9fc896271d6fac27e5caa0b0fe3b0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768343"
---
# <a name="electronic-messaging"></a>Elektroniskā ziņojumapmaiņa

[!include [banner](../includes/banner.md)]

Šajā tēmā sniegts pārskats un informācija par funkcionalitāti **Elektroniskie ziņojumi** (EM).

Nesen valdības un likumdošanas iestādes dažādās valstīs un reģionos visā pasaulē ieviesa pārskatu veidošanas prasības uzņēmumiem, kas reģistrēti attiecīgajās valstīs vai reģionos. Prasību mērķis ir nodrošināt iespēju iegūt datus no minētajiem uzņēmumiem elektroniskā formātā tieši no sistēmām, kurās tika veikta to uzskaite, uzglabāšana un apstrāde.

EM funkcionalitāte programmā Microsoft Dynamics 365 Finance atbalsta dažādus procesus elektroniskajai sadarbspējai starp Finance un sistēmām, kuras valdības un likumdošanas iestādes nodrošina oficiālās informācijas ziņošanai, iesniegšanai un saņemšanai.

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

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>Valstij specifiskās regulēšanas funkcijas, ko atbalsta EM funkcionalitāte

Tabulā ir sniegta informācija par dažām valstij specifiskām regulēšanas funkcijām, ko atbalsta EM funkcionalitāte.

| Valsts/reģions     | Līdzekļa nosaukums | Līdzekļu demonstrācijas ierakstīšana |
|-------------|--------------|------------------------|
| Spānija       | [Tūlītēja informācijas piegāde par PVN (Suminilla Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Ungārija     | [Tiešsaistes rēķinu izrakstīšanas sistēma](../localizations/emea-hun-online-invoicing.md) | |
| Apvienotā Karaliste | [Nodokļu digitalizācija (Making Tax Digital - MTD) – PVN deklarācijas iesniegšana](../localizations/emea-gbr-mtd-vat-integration.md) | [Finance and Operations: Lielbritānijas digitālais nodoklis - PVN deklarācija sistēmā Dynamics 365](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Lietuva   | [i.SAF pārskatu veidošana](../localizations/emea-ltu-isaf.md) | |
| Polija      | [PVN deklarācija ar reģistriem (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: SAF/JPK PVN audita reģistri](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Nīderlande | [PVN deklarācija Nīderlandēm](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Čehijas Republika | [PVN deklarācija](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brazīlija      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| Krievija      | [PVN deklarācija](../localizations/rus-vat-declaration.md) | |
| Krievija      | [Uzskaites pārskati elektroniskā formātā](../localizations/rus-accounting-reporting.md) | |
| Krievija      | [Peļņas nodokļu deklarācija](../localizations/rus-profit-tax-declaration.md) | |
| Krievija      | [Likmēto nodokļu deklarācija](../localizations/rus-assessed-tax-declaration.md) | |
| Krievija      | [Transporta nodokļu deklarācija](../localizations/rus-transport-tax-declaration.md) | |
| Krievija      | [Zemes nodokļu deklarācija](../localizations/rus-land-tax-declaration.md) | |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

