---
title: Automatizēts kreditoru rēķinu izrakstīšanas procesa pārskats
description: Šajā tēmā ir aprakstīta iespēja automatizēt kreditora rēķina apstrādi un automatizēta procesa izmantošanas priekšrocības.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ec3598ebd158cc23ac7c02d7e33557141d5901bc
ms.sourcegitcommit: 9e7ceb5604472f3088f611aa0360bd6a716db32b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022500"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Automatizēts kreditoru rēķinu izrakstīšanas procesa pārskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta iespēja automatizēt kreditora rēķina apstrādi un automatizēta procesa izmantošanas priekšrocības. Šo iespēju veido līdzekļi, kas ir ieslēgti līdzekļu pārvaldībā. Šie līdzekļi attiecas tikai uz kreditoru rēķiniem, nevis uz rēķiniem, kas tiek apstrādāti, izmantojot **Rēķinu žurnāls** vai **Rēķinu reģistrācijas žurnāls** lapu.

Daudzos gadījumos organizācijas sadarbojas ar trešajām pusēm, lai apstrādātu papīra formāta rēķinus, izmantojot optisko rakstzīmju pazīšanas (OCR) pakalpojumu sniedzēju. Pakalpojumu sniedzējs atgriež mašīnlasāmus rēķina metadatus. Lai palīdzētu ar automatizāciju, kreditoru automatizācijas līdzekļi ļauj patērēt šos artefaktus no kreditoriem.

Varat automatizēt dažus kreditoru rēķinu izrakstīšanas procesus. Šajos procesos ir iekļauta importēto kreditoru rēķinu iesniegšana darbplūsmas sistēmā un grāmatoto preču ieejas plūsmas rindu saskaņošana ar gaidošām kreditora rēķina rindām. Automatizētajā procesā tiek parādīta informācija par kreditora rēķina apstrādi, kad tas tiek pārvietots caur katru procesu. Šī iespēja var palīdzēt kreditoru darbiniekiem un vadītājiem efektīvāk apstrādāt kreditoru rēķinus. Kā arī palīdzēt samazināt kļūdas un neprasmi, kas var rasties, manuāli ievadot un apstrādājot informāciju.

Automatizācijas procesus var izmantot, lai veiktu šos uzdevumus:

- Automātiski iesniegt importētos rēķinus darbplūsmas sistēmai.
- Preču ieejas plūsmu saskaņošana ar gaidošām kreditora rēķina rindām.
- Simulēt grāmatošanu pirms kreditora rēķina iegrāmatošanas.
- Ātri un efektīvi skatīt darbplūsmas vēsturi.
- Skatīt un analizēt kreditora rēķinu automatizētas apstrādes rezultātus.

## <a name="vendor-invoice-automation--submit-imported-vendor-invoices-to-the-workflow-system"></a>Kreditoru rēķinu automatizācija — importēto kreditoru rēķinu iesniegšana darbplūsmas sistēmā

Kā daļu no bezkontakta kreditoru rēķinu izrakstīšanas procesa, varat likt sistēmai automātiski iesniegt importētu rēķinu darbplūsmas sistēmā. Process darbosies fonā, izmantojot jūsu norādīto biežumu (katru stundu vai dienu). Iespējai automātiski iesniegt importētos rēķinus darbplūsmas sistēmā ir nepieciešams, lai process sāktos ar importētu rēķinu. Lai nodrošinātu, ka rēķinu var pilnībā apstrādāt bez manuālas iejaukšanās, darbplūsmas konfigurācijā ir jāiekļauj automatizēts grāmatošanas uzdevums.

Rēķinus, kas saistīti ar pirkšanas pasūtījumiem (PP), un rēķinus, kas ietver sagādes kategoriju, kas nepieder PP, un neuzkrātas rindas var automātiski iesniegt darbplūsmas sistēmā. Rēķini, kas tiek ievadīti manuāli un rēķini, kas izveidoti, izmantojot **Kreditora sadarbības rēķinu izveides** darbvietu, ir manuāli jāiesniedz darbplūsmas sistēmā.

Automatizācijas līdzeklis nodrošina elastīgu struktūru, kas ļauj definēt uzņēmuma specifiskos noteikumus importēto kreditoru rēķinu iesniegšanai darbplūsmas sistēmā un grāmatoto preču ieejas plūsmas rindu saskaņošana ar gaidošām kreditora rēķina rindām.

## <a name="vendor-invoice-automation--match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Kreditoru rēķinu automatizācija — preču ieejas plūsmu saskaņošana ar rēķina rindām, kurām ir trīsvirzienu atbilstības ierobežojumi

Sistēma var automātiski saskaņot grāmatotās preču ieejas plūsmas ar rēķina rindām, kurām ir definēti trīsvirzienu atbilstības ierobežojumi. Process tiks veikts, līdz saskaņotais preču ieejas plūsmas daudzums būs vienāds ar rēķina daudzumu. Kā daļu no šī procesa var norādīt maksimālo reižu skaitu, kuru laikā sistēmai jāmēģina saskaņot preču ieejas plūsmu ar rēķina rindu, pirms tiek secināts, ka process nav izdevies. Process darbosies fonā vai nu katru stundu, vai katru dienu. Automatizēto saskaņošanas procesu var palaist kā daļu no rēķinu iesniegšanas procesa darbplūsmas sistēmā. Vai arī varat to palaist kā savrupu procesu.

## <a name="vendor-invoice-automation--pre-validate-vendor-invoice-posting"></a>Kreditoru rēķinu automatizācija — kreditora rēķina iegrāmatošanas iepriekšēja validēšana

Grāmatošanas simulācija izpilda validācijas darbības, kas tiek veiktas kreditora rēķinu iegrāmatošanas procesā, bet neviens konts netiek atjaunināts. Lai palaistu procesu, atlasiet vienu vai vairākus rēķinus lapā **Gaidošie kreditoru rēķini**.

## <a name="vendor-invoice-automation--enhanced-experience-for-viewing-workflow-historical-information-for-vendor-invoices"></a>Kreditoru rēķinu automatizācija — uzlabota pieredze darbplūsmas vēsturiskās informācijas skatīšanai piegādātāja rēķinos

Tiek nodrošināts vienkārši lasāms kreditora rēķinu darbplūsmas vēstures skats. Kreditora rēķina darbplūsmas vēsturei var piekļūt tieši no kreditora rēķina. Tādējādi, lai atrastu informāciju, ir jāveic mazāks darbību skaits.

## <a name="vendor-invoice-automation--analytics-and-metrics"></a>Kreditoru rēķinu automatizācija — analīze un metrika

Darbvieta **Kreditora rēķina ieraksts** ļauj koncentrēties uz kreditoru rēķiniem, kas netika apstrādāti, izmantojot automatizēto procesu. Elementi darbvietas saraksta informācijā par kreditoru rēķiniem, kas netika veiksmīgi iesniegti darbplūsmas sistēmā, importēti vai saskaņoti ar preču ieejas plūsmām. Tiek nodrošināta arī Microsoft Power BI metrika, lai kreditoru vadītājiem sniegtu ieskatu par kreditoru rēķinu automatizācijas efektivitāti.
