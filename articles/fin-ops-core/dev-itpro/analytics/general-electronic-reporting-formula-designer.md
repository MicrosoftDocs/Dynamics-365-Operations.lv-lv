---
title: Formulas veidotājs elektronisko pārskatu veidošanā (ER)
description: Šajā rakstā ir sniegta informācija, kā izmantot formulas veidotāju elektroniskajā pārskatā (ER).
author: NickSelin
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b03613cb40c5ca718f45e69740d29059fcfb70b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894300"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Formulas veidotājs elektronisko pārskatu veidošanā (ER)

[!include [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrots, kā elektronisko atskaišu veidošanā (Electronic reporting — ER) lietot formulas veidotāju. Kad veidojat formātu noteiktam ER elektroniskajam dokumentam, datu pārveidošanai varat lietot formulas, lai nodrošinātu atbilstību dokumenta izpildes un formatējuma prasībām. Šīs formulas līdzinās formulām programmā Microsoft Excel. Formulās tiek atbalstīti dažādi funkciju tipi — teksta, datuma un laika, matemātiskās, loģiskās, informācijas un datu tipu pārveidošanas un arī citas, biznesa jomai specifiskas, funkcijas.

## <a name="formula-designer-overview"></a>Pārskats par formulas veidotāju

ER atbalsta formulas veidotāju. Tāpēc veidošanas laikā varat konfigurēt izteiksmes, kuras var izmantot tālāk norādīto uzdevumu izpildes laikā.

- To datu pārveidošana, kuri ir saņemti no programmas datu bāzes un ir jāievada ER datu modelī, kas ir paredzēts izmantošanai kā datu avots ER formātiem. (Šie pārveidojumi var iekļaut, piemēram, filtrēšanu, grupēšanu un datu tipa pārveidošanu.)
- Datu formatēšana tādiem datiem, kas ir jāsūta uz ģenerēto elektronisko dokumentu saskaņā ar noteikta ER formāta izkārtojumu un nosacījumiem. (Formatēšanu var veikt, piemēram, saskaņā ar pieprasīto valodu, kultūru vai kodējumu.)
- Elektronisko dokumentu izveides procesa kontrolēšana. (Piemēram, izteiksmes var iespējot vai atspējot noteiktu formāta elementu izvadi atkarībā no datu apstrādes. Tās var arī pārtraukt dokumenta izveides procesu vai sūtīt ziņojumus lietotājiem.)

Lapu **Formulas veidotājs** var atvērt, veicot kādu no tālāk norādītajām darbībām.

- Datu avota elementus saistīt ar datu modeļa komponentiem.
- Datu avota elementus saistīt ar formāta komponentiem.
- Pabeigt uzturēšanu aprēķinātajiem laukiem, kas ir daļa no datu avotiem.
- Nosakiet lietotāja ievades parametru redzamību un rediģēšanas nosacījumus.
- Nosakiet noklusējuma vērtības lietotāja ievades parametriem.
- Formatēt formāta transformācijas.
- Definēt formāta komponentu iespējošanas nosacījumus.
- Definēt failu nosaukumus formāta komponentiem FILE.
- Definēt nosacījumus procesa kontroles pārbaudēm.
- Definēt ziņojumu tekstu procesa kontroles pārbaudēm.

## <a name="data-binding"></a><a name="Binding"></a>Datu saistīšana

ER formulas veidotāju var izmantot, lai definētu izteiksmi, kas pārveido no datu avotiem saņemtos datus, lai izpildes laikā šos datus varētu ievadīt datu patērētājā šādos veidos:

- No programmas datu avotiem un izpildes laika parametriem uz ER datu modeli
- No ER datu modeļa uz ER formātu
- No programmas datu avotiem un izpildes laika parametriem uz ER formatu

Nākamajā attēlā ir parādīts šī tipa izteiksmes noformējums. Šajā piemērā izteiksme noapaļo tabulas Intrastat lauka **Intrastat.AmountMST** vērtību līdz diviem cipariem aiz komata un pēc tam atgriež noapaļoto vērtību.

[![Datu saistīšanas izteiksme.](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Tālāk esošajā attēlā ir parādīts, kā var lietot šī tipa izteiksmi. Šajā piemērā izveidotās izteiksmes rezultāts tiek ievadīts datu modeļa **Nodokļu pārskatu veidošanas modelis** komponentā **Transaction.InvoicedAmount**.

[![Tiek izmantota datu saistīšanas izteiksme.](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Izpildes laikā izveidotā formula `ROUND (Intrastat.AmountMST, 2)` katra tabulas Instrastat ieraksta lauka **AmountMST** vērtību noapaļo līdz diviem cipariem aiz komata. Pēc tam tā noapaļoto vērtību ievada datu modeļa **Nodokļu pārskatu veidošana** komponentā **Transaction.InvoicedAmount**.

## <a name="data-formatting"></a><a name="Transformation"></a>Datu formatēšana

ER formulas veidotāju var izmantot, lai definētu izteiksmi, kas formatē no datu avotiem saņemtos datus, lai šos datus varētu nosūtīt kā daļu no ģenerētā elektroniskā dokumenta. Iespējams, jums ir formatējums, kas jālieto kā tipiska kārtula, kuru nepieciešams atkārtoti izmantot kādam formātam. Šajā gadījumā formāta konfigurācijā šo formatēšanu varat vienu reizi ieviest kā nosauktu pārveidošanu, kurai ir formatēšanas izteiksme. Pēc tam šo nosaukto pārveidošanu var saistīt ar daudziem formāta komponentiem, kuriem ir nepieciešams formatēt izvadi atbilstoši jūsu izveidotajai formatēšanas izteiksmei.

Nākamajā attēlā ir parādīts šī tipa transformēšanas noformējums. Šajā piemērā pārveidošana **TrimmedString** apcērt ienākošos datus ar datu tipu *String*, noņemot sākuma un beigu atstarpes. Pēc tam tā atgriež apcirstu virknes vērtību.

[![Pārveidošana.](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Nākamajā attēlā ir parādīts, kā var lietot šī tipa transformēšanu. Šajā piemērā vairāki formāta komponenti izpildes laikā kā izvadi uz ģenerēto elektronisko dokumentu sūta tekstu. Visi šie formāta komponenti atsaucas uz pārveidošanu **TrimmedString** pēc nosaukuma.

[![Tiek izmantota pārveidošana.](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Kad formāta komponenti, piemēram, iepriekšējā attēlā norādītais komponents **partyName**, atsaucas uz pārveidošanu **TrimmedString**, pārveidošana uz ģenerēto elektronisko dokumentu kā izvadi sūta tekstu. Šis teksts neietver sākuma un beigu atstarpes.

Ja jums ir formatējums, kas ir jālieto atsevišķi, šo formatējumu varat ieviest kā noteikta formāta komponenta saistīšanas atsevišķu izteiksmi. Nākamajā attēlā ir parādīta šī tipa izteiksme. Šajā piemērā formāta komponents **partyType** tiek saistīts ar datu avotu, izmantojot izteiksmi, kas ienākošos datus no lauka **Model.Company.RegistrationType** datu avotā pārveido par tekstu, kurš rakstīts ar lielajiem burtiem. Pēc tam izteiksme šo tekstu kā izvadi sūta uz elektronisko dokumentu.

[![Formatējuma lietošana atsevišķam komponentam.](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>Apstrādes plūsmas kontrole

ER formulas veidotāju var izmantot, lai definētu izteiksmes, kas kontrolē elektronisko dokumentu ģenerēšanas procesa plūsmu. Jūs varat veikt tālāk norādītos uzdevumus.

- Definējiet nosacījumus, kas nosaka, kad ir jāaptur dokumenta veidošanas process.
- Norādiet izteiksmes, kas izveido ziņojumus lietotājam par apturētiem procesiem vai parāda izpildes žurnāla ziņojumus par pārskata ģenerēšanas procesa turpināšanu.
- Norādiet ģenerēto elektronisko dokumentu failu nosaukumus un kontrolējiet to izveidošanas nosacījumus.

Katrs apstrādes plūsmas kontroles noteikums ir paredzēts kā atsevišķa pārbaude. Nākamajā attēlā ir parādīta šī tipa pārbaude. Šeit ir šajā piemērā lietotās konfigurācijas skaidrojums:

- Pārbaude tiek novērtēta, kad XML faila ģenerēšanas laikā tiek izveidots mezgls **INSTAT**.
- Ja transakciju saraksts ir tukšs, pārbaude aptur izpildes procesu un atgriež uzrakstu **FALSE**.
- Pārbaude atgriež kļūdas ziņojumu, kas ietver etiķetes SYS70894 tekstu lietotāja vēlamajā valodā.

[![Validēšana.](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER formulas veidotāju var izmantot arī, lai ģenerētu faila nosaukumu ģenerētajam elektroniskajam dokumentam un kontrolētu faila izveides procesu. Nākamajā attēlā ir parādīts šī tipa procesa plūsmas kontroles noformējums. Šeit ir šajā piemērā lietotās konfigurācijas skaidrojums:

- Ierakstu saraksts no datu avota **model.Intrastat** tiek sadalīts partijās. Katrā no partijām ietverts līdz 1000 ierakstiem.
- Izvade izveido zip failu, kas katrai izveidotajai partijai satur vienu failu XML formātā.
- Izteiksme atgriež faila nosaukumu ģenerētajiem elektroniskajiem dokumentiem, savienojot faila nosaukumu un faila nosaukuma paplašinājumu. Otrajai partijai un visām turpmākajām partijām faila nosaukums kā sufiksu ietver partijas ID.
- Izteiksme iespējo (atgriežot vērtību **TRUE**) faila izveides procesu partijām, kas ietver vismaz vienu ierakstu.

[![Apstrādes plūsmas kontrole.](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a>Dokumenta satura kontrole

ER formulu noformētāju var izmantot, lai konfigurētu izteiksmes, kuras kontrolē to, kādi dati tiks ievietoti ģenerētajos elektroniskajos dokumentos izpildlaikā. Izteiksmes var iespējot vai atspējot konkrētu formāta elementu izvadi atkarībā no apstrādes datiem un konfigurētās loģikas. Šīs izteiksmes var ievadīt viena formāta elementam cilnes **Kartēšana** laukā **Iespējots** lapā **Operāciju noformētājs**. Izteiksmes var ievadīt kā loģisku nosacījumu, kas atgriež *Būla* vērtību:

- Ja nosacījums atgriež **True**, tiek palaists pašreizējais formāta elements.
- Ja nosacījums atgriež **False**, tiek izlaists pašreizējais formāta elements.

Nākamajā attēlā ir parādītas šī tipa izteiksmes. (Kā piemēru izmanto Microsoft nodrošināto **ISO20022 kredīta pārsūtīšanas (NO)** formāta konfigurācijas 11.12.11 versiju.) **XMLHeader** formāta komponents ir konfigurēts tā, lai aprakstītu kredīta pārsūtīšanas ziņojuma struktūru saskaņā ar ISO 20022 XML ziņojumu standartiem. Formāta komponents **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** ir konfigurēts, lai ģenerētajam ziņojumam pievienotu **Ustrd** XML elementu un ievietotu pārveduma formātu kā šādu XML elementu tekstu:

- Komponents **PaymentNotes** tiek izmantots, lai ģenerētu tekstu no maksājuma piezīmēm.
- Komponents **DelimitedSequence** ģenerē ar komatu atdalītus rēķina numurus, kuri tiek izmantoti, lai veiktu doto kredīta pārnesi.

[![PaymentNotes un DelimitedSequence komponenti.](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> Komponenti **PaymentNotes** un **DelimitedSequence** tiek marķēti, izmantojot jautājumzīmi. Jautājuma zīme norāda, ka komponenta lietošana ir nosacījumu. Šādā gadījumā komponentu lietošana ir pamatota uz šādiem kritērijiem:
>
> - Izteiksme `@.PaymentsNotes <> ""`, kas definēta komponentam **PaymentNotes**, iespējo (atgriežot **TRUE**) XML elementu **Ustrd**, kurā jāievieto maksājuma piezīmju teksts, ja šis teksts pašreizējai kredīta pārvirzei nav tukšs.
>
>    [![PaymentNotes komponenta izteiksme.](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - Izteiksme `@.PaymentsNotes = ""`, kas definēta komponentam **DelimitedSequence**, iespējo (atgriežot **TRUE**) XML elementu **Ustrd**, kas jāaizpilda ar ar komatu atdalītu rēķina numuru sarakstu, kuri tiek izmantoti, lai veiktu doto kredīta pārvadājumu, ja šī kredīta pārvadājuma maksājumu piezīmes nav tukšas.
>
>    [![DelimitedSequence komponenta izteiksme.](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> Pamatojoties uz šo iestatījumu, ģenerētais ziņojums par katru debitora maksājumu — XML elements **Ustrd**— saturēs vai nu maksājuma piezīmju tekstu, vai, ja šis teksts ir tukšs, sarakstu, kurā ar komatiem atdalīti rēķina numuri, kas izmantoti, lai veiktu šo maksājumu.

## <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a>Konfigurēto formulu validācija

Lapā **formulas veidotājs** atlasiet **Testēt**, lai pārbaudītu, kā darbojas konfigurētā formula.

[![Testēšanas atlasīšana, lai validētu varbūt.](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

Ja ir nepieciešamas formulas argumentu vērtības, jūs varat atvērt dialoglodziņu **Teksta izteiksme**, kas atrodas lapā **Formulas noformētājs**. Vairumā gadījumu šiem argumentiem jābūt manuāli definētiem, jo konfigurētie saistījumi netiek palaisti noformēšanas laikā. Lapas **Formulas noformētājs** cilnē **Testa rezultāts** tiek parādīts konfigurētās formulas izpildes rezultāts.

Šajā piemērā ir parādīts, kā var pārbaudīt ārējās tirdzniecības domēnam konfigurēto formulu, lai pārliecinātos, ka Intrastat preču kods satur tikai ciparus.

Testējot šo formulu, var izmantot dialoglodziņu **Testa izteiksme**, lai norādītu Intrastat preču koda vērtību testēšanai.

[![Intrastat preču kodu testēšanai norādīšana.](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

Kad ir norādīts Intrastat preču kods un atlasīts **Labi**, lapas **Formulu noformētājs** cilnē **Testa rezultāts** tiek parādīts konfigurētās formulas izpildes rezultāts. Pēc tam varat novērtēt, vai rezultāts ir pieņemams. Ja rezultāts nav pieņemams, varat atjaunināt formulu un vēlreiz to pārbaudīt.

[![Testa rezultāts.](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

Dažas formulas nevar testēt noformēšanas laikā. Piemēram, formula var atgriezt datu tipa rezultātu, ko nevar parādīt cilnē **Testa rezultāts.** Šādā gadījumā tiek parādīts kļūdas ziņojums, kurā teikts, ka formulu nevar testēt.

[![Kļūdas ziņojums.](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)
- [Elektronisko pārskatu veidošanas formulu valoda](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
