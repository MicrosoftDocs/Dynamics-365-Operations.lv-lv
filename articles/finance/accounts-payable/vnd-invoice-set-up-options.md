---
title: Iestatījumu opcijas kreditoru rēķinu automatizācijai (priekšskatījums)
description: Šajā tēmā aprakstītas opcijas, kas pieejamas kreditoru rēķinu automatizācijas iestatīšanai un konfigurēšanai.
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
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 40de7c378bff602fa3629bb190a7a89fe584d2a6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993211"
---
# <a name="setup-options-for-vendor-invoice-automation"></a>Kreditoru rēķinu automatizācijas iestatīšanas opcijas

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstītas opcijas, kas pieejamas kreditoru rēķinu automatizācijas iestatīšanai un konfigurēšanai. Rēķinu automatizācijas līdzekļi izmanto šādus iestatījumu parametru tipus:

- Parametri importēto kreditoru rēķinu iesniegšanai darbplūsmas sistēmā un grāmatoto preču ieejas plūsmas rindu saskaņošana ar gaidošām kreditora rēķina rindām.
- Parametri automatizācijas fona uzdevumu apstrādei. Procesu automatizācijas struktūra tiek izmantota importēto kreditoru rēķinu iesniegšanai darbplūsmas sistēmā. Tas tiek izmantots arī, lai automātiski salīdzinātu iegrāmatotās produktu ieejas plūsmu rindas ar gaidošām kreditoru rēķinu rindām un lai veiktu rēķinu salīdzināšanas validēšanu manuāliem rēķiniem, kas automātiski tika saskaņoti ar produktu ieejas plūsmas rindām. Dažādi biznesa procesi izmanto šo struktūru, lai definētu, cik bieži atlasītais process tiek palaists. Pieejamais biežums fona procesiem **Preču ieejas plūsmu saskaņošana rēķina rindām** un **Kreditoru rēķinu iesniegšana darbplūsmā** ir **Stunda** vai **Katru dienu**.

Lai iestatītu vai skatītu informāciju par fona uzdevumu, dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Procesa automatizācijas**, un atlasiet cilni **Fona uzdevums**.

Lai iegūtu bezkontakta automatizāciju no importēšanas procesa, izmantojot kreditoru rēķinu grāmatošanu, ir jāiestata kreditoru rēķinu darbplūsma. Lai iestatītu darbplūsmu, dodieties uz **Kreditori > Iestatījumi > Kreditoru darbplūsmas**. Lai nodrošinātu, ka rēķinu var pilnībā apstrādāt bez manuālas iejaukšanās, jūsu darbplūsmas konfigurācijā ir jāiekļauj automatizēts grāmatošanas uzdevums.

## <a name="parameters-for-submitting-imported-vendor-invoices-to-the-workflow-system"></a>Parametri importēto kreditoru rēķinu iesniegšanai darbplūsmas sistēmā

Importēto kreditoru rēķinu iesniegšanai darbplūsmas sistēmā tiek izmantoti noteikti parametri. Turklāt daži parametri tiek izmantoti, lai saskaņotu grāmatoto preču ieejas plūsmu rindas ar gaidošām kreditora rēķina rindām. Cilnē **Kreditoru rēķinu izrakstīšanas automatizācija**, kas atrodas lapā **Kreditoru parametri**, parametri, kas jums jāiestata ir sadalīti tālāk minētajās sadaļās:

- Kreditoru rēķinu darbplūsma
- Automātiski saskaņot produktu ieejas plūsmas

Ir pieejami šādi parametri:

- **Automātiski iesniegt importētos rēķinus darbplūsmai** — Ja iestatāt šo opciju uz **Jā**, importētie rēķini automātiski tiek iesniegti darbplūsmas sistēmā. Ja šī opcija ir iestatīta uz **Nē**, rēķini ir jāiesniedz manuāli. Iestatot šo opciju uz **Jā**, jūs iespējojat bezkontakta procesu no importēšanas rezultātiem, izmantojot grāmatošanu.

    Varat iestatīt šo opciju uz **Jā** tikai tad, ja jūsu juridiskajai personai ir iestatīta aktīva kreditoru rēķinu darbplūsma. Lai iestatītu darbplūsmu, dodieties uz **Kreditori \> Iestatījumi \> Kreditoru darbplūsma**.

- **Preču ieejas plūsmu saskaņošana ar rēķina rindām pirms automātiskās iesniegšanas** — ja iestatāt šo opciju uz **Jā**, importēto rēķinu nevar automātiski iesniegt darbplūsmas sistēmā, kamēr saskaņotais preču ieejas plūsmas daudzums nav vienāds ar rēķina daudzumu. Iestatot šo opciju uz **Jā**, tiek iespējota automātiska grāmatoto preču ieejas plūsmu saskaņošana ar rēķina rindām, kam ir definēti trīsvirzienu atbilstības ierobežojumi. Šis process tiks izpildīts, līdz saskaņotais preču ieejas plūsmas daudzums būs vienāds ar rēķina daudzumu. Šajā brīdī rēķins tiek automātiski iesniegts darbplūsmas sistēmā.

    Opcija „Preču ieejas plūsmu saskaņošana ar rēķina rindām pirms automātiskās iesniegšanas” ir pieejama tikai tad, ja atlasīta opcija **Iespējot rēķinu salīdzināšanas pārbaudi**. Kad ir atlasīta šī opcija, opcija **Automātiska preču ieejas plūsmu saskaņošana ar rēķina rindām** tiek atlasīta automātiski.

- **Pieprasīt, lai aprēķinātās kopsummas ir vienādas ar importētajām kopsummām automātiskai iesniegšanai darbplūsmā** — Ja iestatāt šo opciju uz **Jā**, rēķinu nevar automātiski iesniegt darbplūsmas sistēmā, kamēr rēķinam aprēķinātās kopsummas nav vienādas ar importētajām kopsummām. Ja šī opcija ir iestatīta uz **Nē**, rēķinu var automātiski iesniegt darbplūsmas sistēmā, bet to nevar grāmatot, kamēr aprēķinātās kopsummas nav izlabotas, lai tās atbilstu importētajām kopsummām. Ja neimportējat rēķina summu vai PVN summu, šai opcijai ir jābūt iestatītai uz **Nē**.
- **Automātiska preču ieejas plūsmu saskaņošana ar rēķina rindām** — ja iestatāt šo opciju uz **Jā**, lai veiktu automātisku grāmatoto preču ieejas plūsmu saskaņošanu ar rēķina rindām, kam ir definēti trīsvirzienu atbilstības ierobežojumi, var tikt izmantota fona apstrāde. Šis process tiks veikts, līdz saskaņotais preču ieejas plūsmas daudzums būs vienāds ar rēķina daudzumu vai līdz lauka **Automātiskās saskaņošanas mēģinājumu skaits** vērtība būs sasniegta. Procesu var palaist, līdz rēķins tiek iesniegts darbplūsmas sistēmā.

    Šī opcija ir pieejama tikai tad, ja ir atlasīta opcija **Iespējot rēķinu salīdzināšanas pārbaudi**.

    Ja iestatāt opciju **Preču ieejas plūsmu saskaņošana ar rēķina rindām pirms automātiskās saskaņošanas** uz **Jā**, šo opciju nevar iestatīt uz **Nē**. Ja iestatāt šo opciju uz **Nē**, vispirms jāiestata opcija **Preču ieejas plūsmu saskaņošana ar rēķina rindām pirms automātiskās saskaņošanas** uz **Nē**.

- **Automātiskās saskaņošanas mēģinājumu skaits** — atlasiet skaitu, cik reizes sistēmai jāmēģina saskaņot preču ieejas plūsmu ar rēķina rindu, pirms tā secina, ka process neizdevās. Kad tiek sasniegts norādītais mēģinājumu skaits, rēķins tiek noņemts no automatizētās apstrādes.

