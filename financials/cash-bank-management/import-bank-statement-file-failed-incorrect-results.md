---
title: "Bankas izraksta faila importēšanas problēmu novēršana"
description: "Ir svarīgi, lai no bankas saņemtais bankas izraksta fails atbilstu programmatūrā Microsoft Dynamics 365 for Operations atbalstītajam izkārtojumam. Stingro bankas izrakstu standartu dēļ lielākā daļa integrāciju darbosies pareizi. Tomēr dažreiz izraksta failu nevar importēt vai ir nepareizi rezultāti. Parasti šīs problēmas izraisa nelielas atšķirības bankas izraksta failā. Šajā rakstā ir paskaidrots, kā novērst šīs atšķirības un atrisināt problēmas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 97d48e978a82805fd9050668c6ddc51a1d3759be
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="bank-statement-file-import-troubleshooting"></a>Bankas izraksta faila importēšanas problēmu novēršana

[!include[banner](../includes/banner.md)]


Ir svarīgi, lai no bankas saņemtais bankas izraksta fails atbilstu programmatūrā Microsoft Dynamics 365 for Operations atbalstītajam izkārtojumam. Stingro bankas izrakstu standartu dēļ lielākā daļa integrāciju darbosies pareizi. Tomēr dažreiz izraksta failu nevar importēt vai ir nepareizi rezultāti. Parasti šīs problēmas izraisa nelielas atšķirības bankas izraksta failā. Šajā rakstā ir paskaidrots, kā novērst šīs atšķirības un atrisināt problēmas.

<a name="what-is-the-error"></a>Kāda kļūda radusies?
------------------

Pēc bankas pārskata faila importēšanas mēģinājuma atveriet sadaļu Datu pārvaldības uzdevumu vēsture un tās detalizēto izpildes informāciju, lai atrastu kļūdu. Kļūda var palīdzēt, norādot uz izrakstu, bilanci vai izraksta rindu. Tomēr ir maz ticams, ka tā nodrošinās pietiekami daudz informācijas, lai palīdzētu noteikt lauku vai elementu, kas radīja problēmu.

## <a name="what-are-the-differences"></a>Kādas ir galvenās atšķirības?
Salīdziniet bankas faila izkārtojuma definīciju ar Microsoft Dynamics 365 for Operations importēšanas definīciju un pievērsiet uzmanību lauku un elementu atšķirībām. Salīdziniet bankas izraksta failu ar saistīto Dynamics 365 for Operations faila paraugu. ISO20022 failos var viegli pamanīt jebkādas atšķirības.

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

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  Kopējiet bankas izraksta faila saturu un ielīmējiet to XML failā tā, lai tas aizstātu **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>XSLT atkļūdošana

Sīkāku informāciju skatiet šeit: <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.

1.  Startējiet Microsoft Visual Studio.
2.  Izveidojiet konsoles pieteikumu.
3.  Atveriet atbilstošo XSLT.
4.  Noklikšķiniet uz XLST un tās rekvizītu lapas.
5.  Iestatiet ievadi bankas izraksta faila atrašanās vietā.
6.  Norādiet izvades atrašanās vietu un faila nosaukumu.
7.  Iestatiet nepieciešamos pārtraukumpunktus.
8.  Izvēlnē noklikšķiniet uz **XML** &gt; **Sākt XSLT atkļūdošanu**.

### <a name="format-the-xslt-output"></a>XSLT izvades formatēšana

Transformācijas darbības laikā tiek izveidots izvades fails, kuru var skatīt programmā Visual Studio. Izmantojiet Ctrl+A, Ctrl+K un Ctrl+D, lai ātri formatētu izvades failu.

### <a name="adjust-the-transformation"></a>Transformācijas korekcija

Koriģējiet transformāciju, lai iegūtu atbilstošo lauku vai elementu bankas pārskata failā. Pēc tam kartējiet attiecīgo lauku vai elementu ar atbilstošo Dynamics 365 for Operations elementu.

### <a name="debitcredit-indicator"></a>Debeta/kredīta indikators

Dažreiz debets var tikt importēts kā kredīts un kredīts var tikt importēts kā debets. Lai atrisinātu šo problēmu, ir jāmaina atbilstošā XSLT. Ja bankas izraksti ir no vairākām bankām, pārliecinieties, ka tajos visos ir izmantota tā pati debeta/kredīta pieeja, vai izveidojiet atsevišķas transformācijas.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator veidne
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit veidne
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator veidne

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Bankas izrakstu formātu un tehnisko izkārtojumu paraugi
Šajā tabulā ir minēti detalizētās bankas darbību saskaņošanas importa failu tehnisko izkārtojumu definīciju paraugi un trīs saistītie bankas izrakstu parauga faili. Failu un tehnisko izkārtojumu paraugus varat lejupielādēt šeit: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| Tehniskā izkārtojuma definīcija                             | Bankas izraksta parauga fails          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |





