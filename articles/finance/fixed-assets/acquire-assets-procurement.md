---
title: Iegūt līdzekļus, izmantojot sagādi
description: Šajā tēmā ir aprakstīts, kā iestatīt lauku Pamatlīdzekļi un Kreditori integrāciju, lai automātiski izveidotu pamatlīdzekļus no pirkšanas pasūtījumiem vai kreditora rēķiniem vai automātiski grāmatotu pamatlīdzekļu iegādes un iegādes korekcijas transakcijas.
author: ShylaThompson
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 3481
ms.assetid: d4e73a3f-633b-48b2-b8db-7a4a59a4d7ec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ccdcef6858c4b7badd48e8a90cef97c25824223
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257613"
---
# <a name="acquire-assets-through-procurement"></a>Iegūt līdzekļus, izmantojot sagādi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā iestatīt lauku Pamatlīdzekļi un Kreditori integrāciju, lai automātiski izveidotu pamatlīdzekļus no pirkšanas pasūtījumiem vai kreditora rēķiniem vai automātiski grāmatotu pamatlīdzekļu iegādes un iegādes korekcijas transakcijas. Viena pirkšanas rinda izveidos vienu pamatlīdzekli neatkarīgi no daudzuma pirkšanas rindā. Ja nepieciešams izveidot vairākus pamatlīdzekļus, ir jāizveido vairākas pirkšanas rindas.

 Pamatlīdzekļu un kreditoru saistīšanai ir pieejamas tālāk aprakstītās metodes, un visiem pamatlīdzekļiem ir jāizmanto vienāda metode.
-   Pirms pamatlīdzekļa numura pievienošanas pirkšanas pasūtījuma vai kreditora rēķina rindā ir manuāli jāizveido pamatlīdzekļa ieraksts. Iegrāmatojot kreditora rēķinu, automātiski tiek iegrāmatota pamatlīdzekļa iegādes transakcija. Šī metode ir pēc noklusējuma.
-   Pirms pamatlīdzekļa numura pievienošanas pirkšanas pasūtījuma vai kreditora rēķina rindā ir manuāli jāizveido pamatlīdzekļa ieraksts. Iegrāmatojot kreditora rēķinu, līdzekļa iegādes transakcija netiek iegrāmatota.
-   Iegrāmatojot produktu ieejas plūsmu vai kreditora rēķinu, kam ir atzīmēta izvēles rūtiņa Izveidot jaunu pamatlīdzekli, automātiski tiek izveidots pamatlīdzeklis. Iegrāmatojot kreditora rēķinu, automātiski tiek iegrāmatota pamatlīdzekļa iegādes transakcija.
-   Iegrāmatojot produktu ieejas plūsmu vai kreditora rēķinu, kam ir atzīmēta izvēles rūtiņa Izveidot jaunu pamatlīdzekli, automātiski tiek izveidots pamatlīdzeklis. Iegrāmatojot kreditora rēķinu, līdzekļa iegādes transakcija netiek iegrāmatota.

Atlasiet vienu no pirmajām divām metodēm, ja vēlaties manuāli izveidot pamatlīdzekļus, un pēc tam pirkšanas pasūtījumam vai kreditora rēķinam piešķiriet pamatlīdzekļa numuru. Atlasiet vienu no pēdējām divām metodēm, ja vēlaties izmantot elastīgāku mehānismu: atkarībā no krājumu detalizētajā informācijā pieejamajiem pamatlīdzekļu datiem dažreiz pamatlīdzekļus var izveidot manuāli, bet dažreiz — automātiski. 

Neatkarīgi no tā, vai pamatlīdzekļi ir izveidoti manuāli, vai arī tiek izmantots elastīgāks mehānisms, ir jānoskaidro, vai iegādes transakciju var iegrāmatot tikai parametru lapā Pamatlīdzekļi vai arī to var iegrāmatot, veicot kreditora rēķina iegrāmatošanu. Dažas organizācijas vēlas, lai lietotāji iegādes un iegādes transakciju ierakstus parametru lapā Pamatlīdzekļi izveido manuāli, izmantojot manuālos žurnāla ierakstus vai piedāvājumus. 

Šajā tēmā apskatīta detalizēta informācija par katru metodi.

## <a name="methods-for-manually-creating-fixed-assets"></a>Manuālai pamatlīdzekļu izveidošanai izmantojamās metodes
Ja parametru lapā Pamatlīdzekļi ir atzīmēta opcija Atļaut līdzekļu iegādi iepirkuma procesā, iegrāmatojot kreditora rēķinu, kura rindās ir ievadīts pamatlīdzekļa numurs, iegāde tiek iegrāmatota automātiski un līdzekļa statuss mainās uz Atvērts. 

Ja iegādi nevar iegrāmatot, iegādes transakciju var manuāli ievadīt parametru lapā Pamatlīdzekļi vai arī var izmantot iegādes piedāvājumu pamatlīdzekļu žurnālā, lai vienā reizē izveidotu vairākus iegādes transakciju ierakstus.

> [!NOTE]                                                                                                                              
> Ja parametru lapā Pamatlīdzekļi ir iestatīts ierobežojums, ka iegādes transakciju iegrāmatošanu var veikt kāda noteikta lietotāju grupa, jums ir jābūt šīs lietotāju grupas dalībniekam, lai varētu iegrāmatot rēķinos norādītās iegādes transakcijas.

## <a name="methods-for-automatically-creating-fixed-assets"></a>Automātiskai pamatlīdzekļu izveidošanai izmantojamās metodes
Iegrāmatojot produktu ieejas plūsmu, kuras rindai ir atzīmēta opcija Izveidot jaunu pamatlīdzekli, tiek izveidots jauns pamatlīdzeklis ar statusu Vēl nav iegādāts. Ja parametru lapā Pamatlīdzekļi ir iestatīta opcija, kas atļauj veikt līdzekļu iegādi no kreditoriem, un jūs esat lietotāju grupas, kas var iegrāmatot iegādes transakcijas, dalībnieks, iegrāmatojot kreditora rēķinu ar jaunu pamatlīdzekli, tiek iegrāmatota jauna pamatlīdzekļa iegādes transakcija un pamatlīdzekļa statuss mainās uz Atvērts. 

Ja, iegrāmatojot produktu ieejas plūsmu, iepirkuma rindā nav atzīmēta opcija Jauns pamatlīdzeklis?, bet tā ir atzīmēta, iegrāmatojot kreditora rēķinu, un ja parametru lapā Pamatlīdzekļi ir iestatīta opcija, kas atļauj veikt izveidošanu un iegādāšanos, tiek izveidots jauns pamatlīdzeklis ar iegādes ar statusu Atvērts. Iegrāmatojot kreditora rēķinu, papildu līdzeklis netiek izveidots, ja tas jau ir izveidots, iegrāmatojot produktu ieejas plūsmu.

### <a name="capitalization-threshold"></a>Kapitalizācijas slieksnis

Izmantojot metodi, kurā pamatlīdzeklis tiek izveidots un iegūts automātiski, jūs varat iestatīt sistēmu apstiprināt, vai pamatlīdzekļa pirkšanas summa atbilst noteiktajam pamatlīdzekļu nolietojuma kapitalizācijas slieksnim. Šādā gadījumā līdzekļa grāmatās tiek atlasīta opcija Nolietojums, ja tas tiek izveidots, veicot iegādi no kreditoriem. 

Kapitalizācijas slieksnis ir valūtas summa, kas nosaka, vai līdzekļi ir nolietojušies, ja tie sasniedz noteikto summu. Piemēram, ja iegādājaties pamatlīdzekli un pirkšanas summa ir mazāka nekā kapitalizācijas slieksnis, pamatlīdzeklis nav atzīmēts nolietojumam; ja pirkšanas summa sasniedz vai pārsniedz slieksni, pamatlīdzeklis tiek atzīmēts nolietojumam. 

Kapitalizācijas slieksni var iestatīt lapā Pamatlīdzekļu grupas.

## <a name="scenario"></a>Scenārijs
Šajā scenārijā aprakstīts pilns Pamatlīdzekļu un Parādu kreditoriem integrācijas cikls. Tālāk ir redzams iestatīšanas paraugs, kā arī aprakstīta iegādes piedāvājumu izmantošana. 

Šajā scenārijā sistēma ir iestatīta šādi:

-   Līdzekļi tiek izveidoti automātiski produktu ieejas plūsmas vai kreditora rēķina iegrāmatošanas laikā, bet parametru lapā Pamatlīdzekļi tiek iestatīts ierobežojums, kas neatļauj no kreditoriem veiktas iegādes transakciju iegrāmatošanu.
-   Ar pamatlīdzekļa saņemšanu saistītie konti tiek norādīti laukā Konta veids, bet ar pamatlīdzekļu izsniegšanu saistītie konta veidi — lapā Krājuma grupas.
-   Datoru grupas (COMP) kapitalizācijas slieksnis ir 1500.
-   Jūsu uzdevums ir ievadīt darbiniekam paredzēta jauna klēpjdatora pirkšanas pasūtījumu, iegrāmatot pirkšanas pasūtījumu, pārbaudīt, vai ekspeditors iegrāmato produktu ieejas plūsmu, iegrāmatot kreditora rēķinu un pēc tam pārbaudīt, vai grāmatvedis atjaunina klēpjdatora līdzekli ar statusu Atvērts.

Lai uzsāktu procesu, izmantojiet lapu Pirkšanas pasūtījums un ievadiet detalizētu informāciju par klēpjdatoru, kura cena ir 1600. Pirkšanas pasūtījuma rindu kopsavilkuma cilnē Pamatlīdzekļi atlasiet opciju Jauns pamatlīdzeklis?, atlasiet pamatlīdzekļu grupu COMP un saglabājiet pirkšanas pasūtījumu. 

Kad klēpjdators ir saņemts, ekspeditors ievada un iegrāmato produktu ieejas plūsmu, reģistrējot klēpjdatora saņemšanu. Ir izveidots klēpjdatora līdzekļa ieraksts ar statusu Vēl nav iegādāts. Summa pārsniedz kapitalizācijas slieksni. Tāpēc klēpjdatora līdzekļa grāmatās tiek atzīmēta opcija Nolietojums. Notika šādas darbības.

| Apraksts                               | Konts             | Debets    | Kredīts   |
|-------------------------------------------|---------------------|----------|----------|
| Pirkšana, produktu ieejas plūsma        | Saņemšanas bez rēķiniem | 1 600,00 |          |
| Pirkšana, produktu ieejas plūsmas pirkšanas korespondējošais konts | Uzkrātie pirkšanas pasūtījumi   |          | 1 600,00 |

Pēc tam iegrāmatojiet klēpjdatora kreditora rēķinu. Klēpjdatora statuss netiek mainīts, jo parametru lapā Pamatlīdzekļi ir iestatīta opcija, kas nepieļauj līdzekļu iegādes transakciju iegrāmatošanu kreditora rēķina iegrāmatošanas laikā. Iegrāmatojot kreditora rēķinu, tika atlasīta opcija Izveidot jaunu pamatlīdzekli. Tāpēc tiek izmantots pamatlīdzekļa saņemšanas konts. Pamatlīdzekļa saņemšanas konts netika izmantots, jo nav iegrāmatota iegāde; tas tiks izmantots vēlāk, kad jūsu organizācijas grāmatvedis parametru lapā Pamatlīdzekļi iegrāmatos iegādes transakciju, izmantojot iegādes piedāvājumus. 

Notika šādas darbības.

| Apraksts                               | Konts             | Debets    | Kredīts   |
|-------------------------------------------|---------------------|----------|----------|
| Pirkšana, produktu ieejas plūsmas pirkšanas korespondējošais konts | Uzkrātie pirkšanas pasūtījumi   | 1 600,00 |          |
| Kreditora bilance                            | Parādi kreditoriem    |          | 1 600,00 |
| Pirkšana, pamatlīdzekļa saņemšana             | Datoru izdevumi    | 1 600,00 |          |
| Pirkšana, produktu ieejas plūsma        | Saņemšanas bez rēķiniem |          | 1 600,00 |

Visbeidzot, grāmatvedis pārskata visus pamatlīdzekļus ar statusu Vēl nav iegādāts. Līdz ar to tiek pārskatīts arī jaunais klēpjdatora līdzeklis. Grāmatvedis tad, izmantojot pamatlīdzekļu žurnāla rindas, atver lapu Iegādes piedāvājums un izveido visu to līdzekļu iegādes transakcijas, kam ir pieejams rēķins, bet kuru statuss vēl ir Vēl nav iegādāts. Kad žurnāls ir iegrāmatots, klēpjdatora līdzekļa statuss tiek mainīts uz Atvērts. Pamatlīdzekļa izsniegšanas konts tiek kreditēts un līdzekļa iegādes konts tiek debetēts. 

Tālāk norādītie ir šī scenārija varianti:

-   Ja parametru lapā Pamatlīdzekļi ir iestatīta opcija, kas kreditora rēķinu iegrāmatošanas laikā atļauj veikt līdzekļu iegādes transakciju iegrāmatošanu, grāmatvedim nav jāizmanto iegādes piedāvājumi parametru lapā Pamatlīdzekļi, jo ir izveidota iegādes transakcija. Kreditora rēķina iegrāmatošanas laikā tiek atjaunināti arī dažādi konti. Tiek debitēts pamatlīdzekļa saņemšanas krājumu konts, nevis datoru izsniegšanas konts, un tiek veiktas divas papildu transakcijas: līdzekļa iegādes konts tiek debitēts un pamatlīdzekļa izsniegšanas krājumu konts tiek kreditēts.
-   Ja, iegrāmatojot produktu ieejas plūsmu, nav atzīmēta opcija Izveidot jaunu pamatlīdzekli, šajā brīdī pamatlīdzeklis netiek izveidots. Ja opcija Izveidot jaunu pamatlīdzekli tiek atlasīta pirms kreditora rēķina iegrāmatošanas, tiek izveidots līdzeklis ar statusu Vēl nav iegādāts vai ar statusu Atvērts, ja kreditora rēķinu iegrāmatošanas laikā tiek veikta arī iegādes transakciju iegrāmatošana.
-   Ja klēpjdatora cena ir 1400, nevis 1600, kapitalizācijas slieksnis nav sasniegts. Līdz ar to tiek izveidots līdzeklis un opcijas Nolietojums atlase tiek noņemta.
-   Ja tiek izmantots rēķinu reģistrs, lai izgūtu dokumentu, pēc rēķinu reģistra iegrāmatošanas izmantojiet lapu Rēķinu apstiprināšanas žurnāls, sasaistiet pirkšanas pasūtījumu ar kreditora rēķinu, atlasiet opciju Izveidot jaunu pamatlīdzekli un pēc tam iegrāmatojiet kreditora rēķinu. Ja esat lietotāju grupas, kas var izveidot iegādes transakcijas, dalībnieks, tiek izveidots iegādes ieraksts un pamatlīdzeklim tiek piešķirts statuss Atvērts.
-   Ja ir saņemts tikai daļējs daudzums, saskaņā ar lietotāju grupai noteiktajiem ierobežojumiem pēc pirmā kreditora rēķina netiek izveidots līdzekļa iegādes ieraksts. Iegādes, kas saistīta ar pasūtīto preču daudzumu noslēdzošo otro kreditora rēķinu, iegrāmatošanu var veikt tikai tad, ja iegādes transakcija ir jau ievadīta pēc pirmā kreditora rēķina un ja jūs esat lietotāju grupas, kam ir atļauta iegādes transakciju iegrāmatošana, dalībnieks.


Plašāku informāciju skatiet rakstā [Pamatlīdzekļu integrācija](fixed-asset-integration.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]