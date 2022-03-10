---
title: Automatizēts kreditoru rēķinu izrakstīšanas procesa pārskats
description: Šajā tēmā ir aprakstīta iespēja automatizēt kreditora rēķina apstrādi un automatizēta procesa izmantošanas priekšrocības.
author: abruer
ms.date: 02/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f21b76bb0d30370e4ea4fdd718999d537e9ce925
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358435"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Automatizēts kreditoru rēķinu izrakstīšanas procesa pārskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta iespēja automatizēt kreditora rēķina apstrādi un automatizēta procesa izmantošanas priekšrocības. Šo iespēju veido līdzekļi, kas ir ieslēgti līdzekļu pārvaldībā. Šie līdzekļi attiecas tikai uz pārdevēju rēķiniem, nevis rēķiniem, kuri tiek apstrādāti, izmantojot lapu **Rēķinu žurnāls** vai **Rēķinu reģistra žurnāls**.

Daudzos gadījumos organizācijas sadarbojas ar trešajām pusēm, lai apstrādātu papīra formāta rēķinus, izmantojot optisko rakstzīmju pazīšanas (OCR) pakalpojumu sniedzēju. Pakalpojumu sniedzējs atgriež mašīnlasāmus rēķina metadatus. Lai palīdzētu ar automatizāciju, kreditoru automatizācijas līdzekļi ļauj patērēt šos artefaktus no kreditoriem.

Varat automatizēt dažus kreditoru rēķinu izrakstīšanas procesus. Šajos procesos ir iekļauta importēto kreditoru rēķinu iesniegšana darbplūsmas sistēmā un grāmatoto preču ieejas plūsmas rindu saskaņošana ar gaidošām kreditora rēķina rindām. Automatizētajā procesā tiek parādīta informācija par kreditora rēķina apstrādi, kad tas tiek pārvietots caur katru procesu. Šī iespēja var palīdzēt kreditoru darbiniekiem un vadītājiem efektīvāk apstrādāt kreditoru rēķinus. Kā arī palīdzēt samazināt kļūdas un neprasmi, kas var rasties, manuāli ievadot un apstrādājot informāciju.

Automatizācijas procesus var izmantot, lai veiktu šos uzdevumus:

- Automātiski lietot priekšapmaksu kreditoru rēķiniem
- Automātiski iesniegt importētos rēķinus darbplūsmas sistēmai.
- Preču ieejas plūsmu saskaņošana ar gaidošām kreditora rēķina rindām.
- Simulēt grāmatošanu pirms kreditora rēķina iegrāmatošanas.
- Ātri un efektīvi skatīt darbplūsmas un automatizācijas vēsturi.
- Skatīt un analizēt kreditora rēķinu automatizētas apstrādes rezultātus.
- Atsākt vairāku rēķinu automatizētu apstrādi.

## <a name="submit-imported-vendor-invoices-to-the-workflow-system"></a>Importēto kreditoru rēķinu iesniegšana darbplūsmas sistēmā

Kā daļa no bezskaipa parādu kreditoriem rēķinu izrakstīšanas procesa, importēto rēķinu var automātiski iesniegt darbplūsmas sistēmā. Process darbosies fonā, izmantojot jūsu norādīto biežumu (katru stundu vai dienu). Iespējai automātiski iesniegt importētos rēķinus darbplūsmas sistēmā ir nepieciešams, lai process sāktos ar importētu rēķinu. Lai nodrošinātu, ka rēķinu var pilnībā apstrādāt bez manuālas iejaukšanās, darbplūsmas konfigurācijā ir jāiekļauj automatizēts grāmatošanas uzdevums.


Rēķinus, kas saistīti ar pirkšanas pasūtījumiem (PP), un rēķinus, kas ietver ar PP nesaistītu sagādes kategoriju, un neuzkrātas rindas var automātiski iesniegt darbplūsmas sistēmā. Rēķinus, kurus ievada manuāli, un rēķinus, kurus izveido, izmantojot darbvietu **Kreditoru sadarbības rēķinu izrakstīšana** ir manuāli jāiesniedz darbplūsmas sistēmā. Iepriekšēja maksājuma lietošanas apstrāde importētiem rēķiniem ir jāveic manuāli. Varat manuāli piemērot iepriekšējus maksājums pirms vai pēc importētā rēķina izvietošanas. Iepriekšējos maksājumus varat manuāli piemērot neizvietotiem standarta rēķiniem, izmantojot lapu **Kreditoru rēķini**. Pēc izvietošanas sagatavotais iepriekšējais maksājums būs pieejams manuālai piemērošanai citiem rēķiniem no šī kreditora lapā **Kreditori** (**Kreditori \> Vispārīgi \> Kreditori \> Visi kreditori \> Rēķinu cilne \> Piemērot**).

Automatizācijas līdzeklis nodrošina elastīgu struktūru, kas ļauj definēt uzņēmuma specifiskos noteikumus importēto kreditoru rēķinu iesniegšanai darbplūsmas sistēmā un grāmatoto preču ieejas plūsmas rindu saskaņošana ar gaidošām kreditora rēķina rindām.

## <a name="match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Saskaņojiet produktu kvītis ar rēķinu rindām, kurām ir trīsvirzienu atbilstības ierobežojumi

Grāmatotās produktu ieejas plūsmas var automātiski saskaņot ar rēķina rindām, kurām ir definēti trīsvirziena atbilstības ierobežojumi. Process tiks veikts, līdz saskaņotais preču ieejas plūsmas daudzums būs vienāds ar rēķina daudzumu. Kā daļu no šī procesa var norādīt maksimālo reižu skaitu, kuru laikā sistēmai jāmēģina saskaņot preču ieejas plūsmu ar rēķina rindu, pirms tiek secināts, ka process nav izdevies. Process darbosies fonā vai nu katru stundu, vai katru dienu. Automatizēto saskaņošanas procesu var palaist kā daļu no rēķinu iesniegšanas procesa darbplūsmas sistēmā. Vai arī varat to palaist kā savrupu procesu.

## <a name="pre-validate-vendor-invoice-posting"></a>Iepriekš validējiet kreditora rēķina izvietošanu

Grāmatošanas simulācija izpilda validācijas darbības, kas tiek veiktas kreditora rēķinu iegrāmatošanas procesā, bet neviens konts netiek atjaunināts. Lai palaistu procesu, atlasiet vienu vai vairākus rēķinus lapā **Gaidošie kreditoru rēķini**.

## <a name="enhanced-experience-for-viewing-workflow-and-automation-historical-information-for-vendor-invoices"></a>Uzlabota darbplūsmas skatīšanās un kreditoru rēķinu vēsturiskās informācijas automatizācija

Tiek nodrošināts vienkārši lasāms kreditora rēķinu darbplūsmas vēstures skats. Kreditora rēķina darbplūsmas vēsturei var piekļūt tieši no kreditora rēķina. Tādējādi, lai atrastu informāciju, ir jāveic mazāks darbību skaits. Ja jūsu organizācija ir iespējojusi automātisku importēto kreditoru rēķinu iesniegšanu darbplūsmai, importētajiem rēķiniem ir nodrošināta automatizācijas vēsture. Automatizācijas vēsture palīdz identificēt pašreizējo procesa darbību, kā arī darbības, kas jau ir pabeigtas. Ja solis nav izdevusies, tiks sniegta detalizēta informācija, lai palīdzētu izprast kļūmes iemeslu.

## <a name="analytics-and-metrics"></a>Analīze un metrika

Darbvieta **Kreditora rēķina ieraksts** ļauj koncentrēties uz kreditoru rēķiniem, kas netika apstrādāti, izmantojot automatizēto procesu. Elementi darbvietas saraksta informācijā par kreditoru rēķiniem, kas netika veiksmīgi iesniegti darbplūsmas sistēmā, importēti vai saskaņoti ar preču ieejas plūsmām. Microsoft Power BI metrika tiek nodrošināta, lai kreditoru pārvaldniekiem sniegtu ieskatu kreditoru rēķinu automatizācijas efektivitātē.


## <a name="resume-automation-processing-for-multiple-invoices"></a>Automatizācijas procesa atsākšana vairākiem rēķiniem

Ja importēts rēķins netiek sekmīgi iesniegts darbplūsmā, izmantojot automatizēto procesu, sistēma to noņems no turpmākas automatizētās apstrādes. Kreditoru darbinieks var pārskatīt un rediģēt rēķinu, pirms automatizētais process to atkārtoti iesniedz darbplūsmai. Ja ar vienu un to pašu labojumu var atrisināt kļūmes iemeslu vairākos rēķinos, varat atsākt automātisko procesu lapā **Atsākt automātisko rēķinu apstrādi**. 

## <a name="tracking-the-invoice-received-date-value"></a>Datuma vērtība Rēķins saņemts izsekošana

Vērtība **Rēķina saņemšanas datums** ir datums, kurā uzņēmums no kreditora ir saņēmis rēķinu. Tajā sniegts sākumpunkts rēķina virzības izsekošanai, izmantojot automatizētos procesus. Šo vērtību var iekļaut kreditora rēķina importētajos datos. Manuāli izveidotiem rēķiniem varat norādīt datumu. Ja vērtība netiek ievadīta, pēc noklusējuma izmanto pašreizējo datumu.


## <a name="tracking-the-imported-invoice-amount-and-imported-sales-tax-amount-values"></a>Vērtību Importētā rēķina summa un Importētais pārdošanas nodoklis izsekošana

Kreditoru rēķinu vērtības **Importētā rēķina summa** un **Importētā pārdošanas nodokļa summa** var nodrošināt kreditora rēķinu importētajā failā. Parasti šīs vērtības ir no rēķina, kuru ieskenēja ārpakalpojumu sniedzējs un iekļāvis importētajā failā. Kad rēķins tiek apstrādāts Parādi kreditoriem, vērtības tiks aprēķinātas, pamatojoties uz rēķina datiem. Rēķinu var izvietot vienīgi tad, ja importētās vērtības atbilst aprēķinātajām vērtībām. Vērtību atbilstība nodrošina, ka rēķinā precīzi atspoguļota kreditoram izmaksājamā summa. Ja jūsu organizācija ļauj darbplūsmas sistēmā automātiski iesniegt importētus rēķinus, jūs varat pēc izvēles pieprasīt, ka importētajām kopsummām ir jāatbilst aprēķinātajām kopsummām, pirms rēķinu var iesniegt darbplūsmas sistēmā.

## <a name="vendor-invoice-automation---resume-automation-processing-for-multiple-invoices"></a>Kreditora rēķina automatizācija — vairāku rēķinu automatizētas apstrādes atsākšana
Kad importētais rēķins, izmantojot automatizēto procesu, nav sekmīgi iesniegts darbplūsmai, tas tiks noņemts tālākai automatizētai apstrādei. Kreditoru darbinieks var pārskatīt un rediģēt rēķinu, pirms automatizētais process to atkārtoti iesniedz darbplūsmai. Ja ar vienu un to pašu labojumu var atrisināt kļūmes iemeslu vairākos rēķinos, varat atsākt automātisko procesu lapā **Atsākt automātisko rēķinu apstrādi**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
