---
title: Rēķinu iesniegšana darbplūsmu sistēmā un produktu ieejas plūsmu atbilstības nodrošināšana
description: Šajā tēmā ir paskaidrota kreditoru rēķinu iesniegšana darbplūsmas sistēmā un automātiska grāmatoto preču ieejas plūsmas rindu saskaņošana ar kreditora rēķiniem.
author: abruer
ms.date: 09/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 84699746349024854a4eeb9cee62960ec38bc338
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827822"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines"></a>Rēķinu iesniegšana darbplūsmu sistēmā un produktu ieejas plūsmu atbilstības nodrošināšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrota kreditoru rēķinu iesniegšana darbplūsmas sistēmā un automātiska grāmatoto preču ieejas plūsmas rindu saskaņošana ar kreditora rēķiniem.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>Importēto kreditoru rēķinu iesniegšana darbplūsmas sistēmā un grāmatoto preču ieejas plūsmas rindu saskaņošana ar gaidošām kreditora rēķina rindām

Kā daļu no bezkontakta kreditoru rēķinu izrakstīšanas procesa, varat likt sistēmai automātiski iesniegt importētu rēķinu darbplūsmas sistēmā. Varat konfigurēt importēto rēķinu iesniegšanas procesu darbplūsmas sistēmā cilnē **Kreditoru rēķinu izrakstīšanas automatizācija** lapā **Parādu kreditoriem parametri** (**Kreditori \> Iestatījumi \> Parādu kreditoriem parametri**). Darbplūsmā iesniegšanas process darbosies fonā, izmantojot jūsu norādīto biežumu (katru stundu vai dienu).

Automātiski iesniedzot rēķinus darbplūsmas sistēmā, jāsāk ar importētu rēķinu. Lai nodrošinātu, ka rēķinu var pilnībā apstrādāt bez manuālas iejaukšanās, jums darbplūsmas konfigurācijā ir jāiekļauj automatizēts grāmatošanas uzdevums. Rēķinus, kas saistīti ar pirkšanas pasūtījumiem (PP), un rēķinus, kas ietver ar PP nesaistītu sagādes kategoriju, un neuzkrātas rindas var automātiski iesniegt darbplūsmas sistēmā. Manuāli ievadītie rēķini ir manuāli jāiesniedz darbplūsmas sistēmā.

Darbplūsmas vērtība **Iesniedza** ir fona uzdevumā **Kreditoru rēķinu iesniegšana darbplūsmā** ievadītais lietotāja ID lapā **Procesu automatizācija**. Lietotājs, kam ir šis lietotāja ID, pēc nepieciešamības varēs atsaukt rēķinu no darbplūsmas sistēmas.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Grāmatoto preču ieejas plūsmu saskaņošana ar rēķina rindām, kurām ir trīsvirzienu atbilstības ierobežojumi

Kā daļu no bezkontakta kreditoru rēķinu izrakstīšanas procesa, sistēma var automātiski saskaņot grāmatotās produktu ieejas plūsmas ar rēķina rindām. Šim uzdevumam ir jādefinē trīsvirzienu atbilstības ierobežojumi. Šis līdzeklis ir pieejams, ja līdzeklis **Kreditoru rēķinu izrakstīšanas automatizācija** ir iespējots lapā **Līdzekļu pārvaldība**.

Atbilstības process tiks veikts, līdz saskaņotais preču ieejas plūsmas daudzums būs vienāds ar rēķina daudzumu. Tomēr, ja vienai rēķina rindai ir vairākas produktu ieejas plūsmas, process ir jāpalaiž vairākas reizes, lai sasniegtu pilnu daudzuma atbilstību. Var norādīt maksimālo reižu skaitu, kuru laikā sistēmai jāmēģina saskaņot preču ieejas plūsmu ar rēķina rindu, pirms tiek secināts, ka process nav izdevies. Process darbosies fonā vai nu katru stundu, vai katru dienu. 

Automatizēto saskaņošanas procesu var palaist kā daļu no rēķinu iesniegšanas procesa darbplūsmas sistēmā. Vai arī varat to palaist kā savrupu procesu. Iestatījumi preču ieejas plūsmu un rēķina rindu saskaņošanas procesam tiek konfigurēti cilnē **Kreditoru rēķinu izrakstīšanas automatizācija** lapā **Parādu kreditoriem parametri** (**Kreditori \> Iestatījumi \> Parādu kreditoriem parametri**).

Rēķina rindas, kurām ir trīsvirzienu atbilstības ierobežojumi, kur saskaņotais ieejas plūsmas daudzums ir mazāks par daudzumu rēķinā, tiks iekļauts automatizētajā saskaņošanas procesā ar preču ieejas plūsmu.

Lai skatītu statusu **Pēdējā atbilstība** rēķiniem, kas nav iekļauti automatizētajā darbplūsmā iesniegšanas procesā, atveriet rēķinu no lapas **Kreditoru rēķini**. Skatot rēķinu, atbilstošā validācijas informācija tiek atjaunināta. Statusu **Pēdējā atbilstība** var atjaunināt automātiski, izmantojot fona uzdevumu **Pārbaudīt rēķina atbilstību**. Varat konfigurēt statusa **Pēdējā atbilstība** sautomātiskās atjaunināšanas procesu lapas **Procesu automatizācija** cilnē **Fona procesi** (**Sistēmas adminstrēšana\> Iestatīšana\> Procesa automatizācija**).

Rēķina rinda tiks izslēgta no automātiskās apstrādes, ja izpildīts kāds no šiem nosacījumiem:

- Rēķina rindas vērtība **Automatizētās preču ieejas plūsmas atbilstības statuss** ir **Nesekmīgs**.
- Rēķins tiek izmantots.
- Rēķins ir darbplūsmas sistēmā.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
