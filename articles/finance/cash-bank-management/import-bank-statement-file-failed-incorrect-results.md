---
title: Bankas izraksta faila importēšanas problēmu novēršana
description: Ir svarīgi, lai no bankas saņemtais bankas izrakstu fails atbilstu programmā Microsoft Dynamics 365 Finance atbalstītajam izkārtojumam. Stingro bankas izrakstu standartu dēļ lielākā daļa integrāciju darbosies pareizi. Tomēr dažreiz izraksta failu nevar importēt vai ir nepareizi rezultāti. Parasti šīs problēmas izraisa nelielas atšķirības bankas izraksta failā. Šajā rakstā ir paskaidrots, kā novērst šīs atšķirības un atrisināt problēmas.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc5b9cf3449b48767a27891a019f8fe8df2a900559898e3cb1849d25bec7c987
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757125"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Bankas izraksta faila importēšanas problēmu novēršana

[!include [banner](../includes/banner.md)]

Ir svarīgi, lai no bankas saņemtais bankas izrakstu fails atbilstu programmā Microsoft Dynamics 365 Finance atbalstītajam izkārtojumam. Stingro bankas izrakstu standartu dēļ lielākā daļa integrāciju darbosies pareizi. Tomēr dažreiz izraksta failu nevar importēt vai ir nepareizi rezultāti. Parasti šīs problēmas izraisa nelielas atšķirības bankas izraksta failā. Šajā rakstā ir paskaidrots, kā novērst šīs atšķirības un atrisināt problēmas.

## <a name="what-is-the-error"></a>Kāda kļūda radusies?

Pēc bankas pārskata faila importēšanas mēģinājuma atveriet sadaļu Datu pārvaldības uzdevumu vēsture un tās detalizēto izpildes informāciju, lai atrastu kļūdu. Kļūda var palīdzēt, norādot uz izrakstu, bilanci vai izraksta rindu. Tomēr ir maz ticams, ka tā nodrošinās pietiekami daudz informācijas, lai palīdzētu noteikt lauku vai elementu, kas radīja problēmu.

> [!NOTE]
> Importētie bankas izraksti var pārklāties tikai vienu reizi.  Piemēram, ja pārskats beidzas 2021. gada 1. janvārī plkst. 12:00, tad nākamā pārskata sākuma datums var būt 2021. gada 1. janvāris plkst. 12:00, 12:00:00.

## <a name="what-are-the-differences"></a>Kādas ir galvenās atšķirības?
Bankas faila izkārtojuma definīciju salīdziniet ar Finance importa definīciju un pievērsiet uzmanību atšķirībām laukos un elementos. Bankas izraksta failu salīdziniet ar saistīto Finance faila paraugu. ISO20022 failos var viegli pamanīt jebkādas atšķirības.

## <a name="time-zone-differences-on-imported-bank-statements"></a>Laika joslu atšķirības importētajos bankas izrakstos
Datuma-laika vērtības importa failā var atšķirties no datuma/laika vērtībām, kas tiek rādītas Finance and Operations. Lai novērstu šo neatbilstību, ievadiet laika joslas preferences lapā **Datu avotu konfigurēšana**. Papildinformāciju par to, kā ievadīt laika zonas preferenci, skatiet tēmā [Papildu bankas darbību saskaņošanas importēšanas procesa iestatīšana](set-up-advanced-bank-reconciliation-import-process.md).

## <a name="transformations"></a>Transformācijas
Parasti izmaiņas ir jāveic, izmantojot vienu no trīs transformācijām. Katra transformācija ir rakstīta konkrētam standartam.

| Resursa nosaukums                                         | Faila nosaukums                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Atkļūdošanas transformācijas
### <a name="adjust-the-bai2-and-mt940-files"></a>BAI2 un MT940 failu korekcija

BAI2 un MT940 faili ir teksta faili, un tiem nepieciešama korekcija, lai iespējotu paplašināmo stila lapas valodas transformāciju (XSLT) atkļūdošanu. Programma veic šo korekciju, importējot failu.

1.  Izveidojiet XML failu un iekopējiet tajā šo tekstu.

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  Kopējiet bankas izraksta faila saturu un ielīmējiet to XML failā tā, lai tas aizstātu **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>XSLT atkļūdošana

Lai iegūtu papildus informāciju, skatiet <https://msdn.microsoft.com/library/ms255605.aspx>.

1.  Palaidiet Microsoft Visual Studio.
2.  Izveidojiet konsoles pieteikumu.
3.  Atveriet atbilstošo XSLT.
4.  Noklikšķiniet uz XLST un tās rekvizītu lapas.
5.  Iestatiet ievadi bankas izraksta faila atrašanās vietā.
6.  Norādiet izvades atrašanās vietu un faila nosaukumu.
7.  Iestatiet nepieciešamos pārtraukumpunktus.
8.  Izvēlnē noklikšķiniet uz **XML** &gt; **Sākt XSLT atkļūdošanu**.

### <a name="format-the-xslt-output"></a>XSLT izvades formatēšana

Transformācijas izpildes laikā tiek izveidots izvades fails, ko varat skatīt programmā Visual Studio. Izmantojiet Ctrl+A, Ctrl+K un Ctrl+D, lai ātri formatētu izvades failu.

### <a name="adjust-the-transformation"></a>Transformācijas korekcija

Koriģējiet transformāciju, lai iegūtu atbilstošo lauku vai elementu bankas pārskata failā. Pēc tam attiecīgo lauku vai elementu kartējiet uz atbilstošo Finance elementu.

### <a name="debitcredit-indicator"></a>Debeta/kredīta indikators

Dažreiz debets var tikt importēts kā kredīts un kredīts var tikt importēts kā debets. Lai atrisinātu šo problēmu, ir jāmaina atbilstošā XSLT. Ja bankas izraksti ir no vairākām bankām, pārliecinieties, ka tajos visos ir izmantota tā pati debeta/kredīta pieeja, vai izveidojiet atsevišķas transformācijas.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator veidne
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit veidne
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator veidne

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Bankas izrakstu formātu un tehnisko izkārtojumu paraugi
Šajā tabulā ir minēti detalizētās bankas darbību saskaņošanas importa failu tehnisko izkārtojumu definīciju paraugi un trīs saistītie bankas izrakstu parauga faili. Piemēra failus un tehniskos izkārtojumus var lejupielādēt šeit: [Importēt faila piemērus](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Tehniskā izkārtojuma definīcija                             | Bankas izraksta parauga fails          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
