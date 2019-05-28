---
title: Starpuzņēmumu rēķinu izrakstīšana
description: Šajā rakstā ir sniegta informācija un piemēri par starpuzņēmumu rēķinu izrakstīšanu projektiem programmā Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 857aee796db2a4743cdbd91da3eb1cf6f996f9d1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557264"
---
# <a name="intercompany-invoicing"></a>Starpuzņēmumu rēķinu izrakstīšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija un piemēri par starpuzņēmumu rēķinu izrakstīšanu projektiem programmā Microsoft Dynamics 365 for Finance and Operations.

Jūsu organizācijai var būt vairākas nodaļās, meitasuzņēmumi un citas juridiskās personas, kas projektos savstarpēji pārsūta preces un pakalpojumus. Juridiskā persona, kas nodrošina pakalpojumu vai preci, tiek dēvēta par *patapināšanas juridisko personu*, un juridiskā persona, kas saņem pakalpojumu vai preci, tiek dēvēta par *piesaistīšanas juridisko personu*. 

Nākamajā attēlā ir redzams tipisks scenārijs, kur divas juridiskās personas — SI FR (piesaistīšanas juridiskā persona) un SI USA (patapināšanas juridiskā persona) — koplieto resursus, lai nodrošinātu projektu klientam A. Šī scenārija nolūkos juridiskā persona SI FR ir nolīgta, lai piegādātu darbu debitoram A. 

[![Starpuzņēmumu rēķina izrakstīšanas piemērs](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Mērķis ir padarīt starpuzņēmumu projektu transakciju izmaksu kontroles, ieņēmumu atzīšanas, nodokļu un transfertcenas procesus vieglāk pielāgojamus un efektīvākus. Turklāt tiek sniegtas šādas iespējas:

-   Izveidot debitora rēķinus atbilstoši projektam piesaistīšanas juridiskajā personā, izmantojot starpuzņēmumu darba laika uzskaites tabulas, izdevumus un kreditoru rēķinus patapināšanas juridiskajā personā.
-   Atbalstīt nodokļu aprēķinus un netiešās izmaksas.
-   Atlikt ieņēmumu atzīšanu patapināšanas juridiskajā personā un gadījumos, kad piesaistīšanas juridiskajai personai ir jāatzīst izmaksas.
-   Uzkrāt nepabeigtās ražošanas (NP) ienākumus patapināšanas juridiskajā personā.
-   Iestatīt transfertcenas, kuru pamatā var būt dažādi cenu noteikšanas modeļi. Daži piemēri:
    -   **Daudzums** — summa, ko ievadāt laukā **Cenu noteikšana**, ir faktiskās izmaksas uz daudzumu vai vienību.
    -   **Izmaksu summa** — cena/izmaksas uz transakciju plus izmaksu summa, ko ievadāt laukā **Cenu noteikšana**.
    -   **Izmaksas procentos** — transfertcena ir cena/izmaksas uz transakciju, reizinātas ar izmaksu procentuālo daudzumu, ko ievadāt laukā **Cenu noteikšana**.
    -   **Pārdošanas cenas procentu likme** —-pārdošanas cenas procenti, kas tiek nodoti patapināšanas juridiskajai personai.
    -   **Summa zem pārdošanas cenas** — summa, kuru piesaistīšanas juridiskā persona aiztur no pārdošanas cenām pirms nodošanas patapināšanas juridiskajai personai.
    -   **Seguma summas norma** — skaitlis, ko ievadāt laukā **Cenu noteikšana**, ir seguma summas likme, kas ir izteikta kā procenti no pārdošanas cenas.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>1. piemērs. Iestatīt parametrus starpuzņēmumu rēķinu izrakstīšanai
Šajā piemērā USSI ir patapināšanas juridiskā persona, un tās resursiem tiek ziņots laiks attiecībā uz piesaistīšanas juridisko personu, FRSI, kurai ir noslēgts līgums ar gala klientu. USSI darbinieku ziņotās stundas un izdevumus var iekļaut projekta rēķinā, ko ģenerē FRSI. Turklāt pastāv transakciju trešais avots tādām transakcijām, kuras var rasties no patapināšanas juridiskās personas (šajā piemērā tā ir USSI), kad šī juridiskā persona sniedz kopīgus kreditoru pakalpojumus meitasuzņēmumiem (piemēram, FRSI) un pēc tam šīs izmaksas nodod tālāk projektiem šajos meitasuzņēmumos. Visu rēķinu dokumentu saskaņošanu un nodokļu aprēķināšanu veic programmatūra Finance and Operations. 

Šajā piemērā juridiskajai personai FRSI ir jābūt debitoram juridiskajā personā USSI un juridiskajai personai USSI ir jābūt kreditoram juridiskajā personā FRSI. Pēc tam varat iestatīt starpuzņēmumu attiecības starp abām juridiskajām personām. Nākamajā procedūrā ir parādīts, kā iestatīt parametrus tā, lai abas juridiskās personas varētu piedalīties starpuzņēmumu rēķinu izrakstīšanā.

1. Iestatiet FRSI kā debitoru juridiskajā personā USSI un iestatiet USSI kā kreditoru juridiskajā personā FRSI. Šī uzdevuma izpildīšanai pastāv trīs ievades punkti.

   | Solis |                                                       Ieejas punkts                                                        |                                                                                                                                                                                               Apraksts                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | Juridiskās personas USSI sadaļā noklikšķiniet uz <strong>Debitoru parādi</strong> &gt; <strong>Debitori</strong> &gt; <strong>Visi debitori</strong>. |                                                                                                                                                                  Izveidojiet jaunu debitora ierakstu juridiskajai personai FRSI un atlasiet debitoru grupu.                                                                                                                                                                  |
   |  B   |    Juridiskās personas FRSI sadaļā noklikšķiniet uz <strong>Parādi kreditoriem</strong> &gt; <strong>Kreditori</strong> &gt; <strong>Visi kreditori</strong>.     |                                                                                                                                                                    Izveidot jaunu kreditora ierakstu juridiskajai personai USSI un atlasiet kreditoru grupu.                                                                                                                                                                    |
   |  C   |                                  Juridiskajā personā FRSI atveriet tikko izveidoto kreditora ierakstu.                                  | Sadaļas Darbību rūts cilnē <strong>Vispārīgi</strong>, grupā <strong>Iestatīt</strong> noklikšķiniet uz <strong>Starpuzņēmumu</strong>. Lapas <strong>Starpuzņēmumu</strong> cilnē <strong>Darījumu attiecības</strong> slīdni <strong>Aktīvs</strong> iestatiet uz <strong>Jā</strong>. Laukā <strong>Debitora uzņēmums</strong> atlasiet darbībā A izveidoto debitora ierakstu. |


2. Noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Iestatījumi** &gt; **Projektu vadības un uzskaites parametri** un pēc tam noklikšķiniet uz cilnes **Starpuzņēmumu**. Veids, kādā iestatāt parametrus, ir atkarīgs no tā, vai jūs esat piesaistīšanas juridiskā persona vai patapināšanas juridiskā persona.
   -   Ja esat piesaistīšanas juridiskā persona, atlasiet iepirkuma kategoriju, kas ir jāizmanto, lai salīdzinātu ar automātiski ģenerētajiem kreditoru rēķiniem.
   -   Ja esat patapināšanas juridiskā persona, tad katrai piesaistīšanas juridiskajai personai atlasiet noklusējuma projektu kategoriju attiecībā uz katru transakcijas tipu. Projektu kategorijas tiek lietotas nodokļu konfigurēšanai, kad rēķinos iekļautā kategorija starpuzņēmumu transakcijās pastāv tikai piesaistīšanas juridiskajā personā. Varat izvēlēties, vai uzkrāt ieņēmumus starpuzņēmumu transakcijām. Šis uzkrājums tiek veikts, kad transakcijas tiek grāmatotas, un pēc tam tas tiek anulēts, kad starpuzņēmumu rēķins tiek grāmatots.

3. Noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Iestatījumi** &gt; **Cenas** &gt; **Transfērcena**.
4. Atlasiet valūtu, transakcijas tipu un transfertcenas modeli. Rēķinos izmantotā valūta ir valūta, kas ir konfigurēta debitora ierakstā piesaistīšanas juridiskajai personai šajā patapināšanas juridiskajā personā. Šī valūta tiek izmantota, lai noteiktu ierakstu atbilstību transfertcenu tabulā.
5. Noklikšķiniet uz **Virsgrāmata** &gt; **Grāmatošanas iestatīšana** &gt; **Starpuzņēmumu uzskaite** un iestatiet juridisko personu USSI un FRSI attiecības.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>2. piemērs. Veidot un grāmatot starpuzņēmumu darba laika uzskaites tabulu
Patapināšanas juridiskajai personai USSI ir jāizveido un jāgrāmato darba laika uzskaites tabula kādam projektam no FRSI, piesaistīšanas juridiskās personas. Šī uzdevuma izpildīšanai pastāv divi ievades punkti.

| Solis | Ieejas punkts                                                                       | Apraksts                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektu vadība un uzskaite** &gt; **Darba laika uzskaites tabulas** &gt; **Visas darba laika uzskaites tabulas** | Izveidot jaunu darba laika uzskaites tabulu. Darba laika uzskaites tabulas rindā, laukā **Juridiskā persona** atlasiet **FRSI**. Laukā **Projekta ID** atlasiet attiecīgo projektu juridiskajā personā FRSI. Ievadiet stundas katrai nedēļas dienai. |
| B    | Lapa **Darba laika uzskaites tabula**                                                                | Pēc darbplūsmas izpildes grāmatojiet šo darba laika uzskaites tabulu un pierakstiet dokumenta numuru.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>3. piemērs. Veidot un grāmatot starpuzņēmumu kreditoru rēķinu
Patapināšanas juridiskajai personai USSI ir jāizveido un jāgrāmato starpuzņēmumu kreditoru rēķins kādam projektam no FRSI, piesaistīšanas juridiskās personas. Šis kreditora rēķins tiek izrakstīts par ārpakalpojumu darbu un izdevumiem, ko izpildīja USSI apmaksāti kreditori. Šī uzdevuma izpildīšanai pastāv divi ievades punkti.

| Solis | Ieejas punkts                                                                                      | Apraksts                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Parādi kreditoriem** &gt; **Rēķini** &gt; **Atvērt kreditoru rēķinus** &gt; **Jauns kreditora rēķins** | Izveidojiet jaunu kreditora rēķinu un ievadiet pakalpojumus, kas tika sniegti FRSI projekta vārdā.                                                                                                                                                                                  |
| B    | Lapa **Kreditora rēķins**                                                                      | Ievadiet rindas, kas norāda FRSI vārdā sniegtos ārpakalpojumus. Kopsavilkuma cilnē **Detalizēta informācija par rindu**, rēķina rindas cilnē **Projekts**, laukā **Projekta uzņēmums** ievadiet **FRSI**. Ievadiet projektu un atbilstošo informāciju. Pēc tam grāmatojiet šo kreditora rēķinu. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>4. piemērs. Veidot un grāmatot starpuzņēmumu rēķinu
Patapināšanas juridiskajai personai USSI ir jāizveido un jāgrāmato starpuzņēmumu rēķins. Šī uzdevuma izpildīšanai pastāv divi ievades punkti.

| Solis | Ieejas punkts                                                                                             | Apraksts                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektu vadība un uzskaite** &gt; **Projekta rēķini** &gt; **Starpuzņēmumu debitora rēķins**  | Noklikšķiniet uz **Jauns**, lai atvērtu lapu **Izveidot starpuzņēmumu rēķinu**.                                                                                  |
| B    | **Projektu vadība un uzskaite** &gt; **Projekta rēķini** &gt; **Starpuzņēmumu debitoru rēķini** | Lapā **Izveidot starpuzņēmumu rēķinu** ievadiet juridisko personu, norādiet transakciju, ko vēlaties iekļaut, un pēc tam noklikšķiniet uz **Meklēt**. |
| C    | **Projektu vadība un uzskaite** &gt; **Projekta rēķini** &gt; **Starpuzņēmumu debitoru rēķini** | Atlasiet transakcijas, kuras iekļaut rēķinā, vai noklikšķiniet uz **Atlasīt visus**, lai rēķinā iekļautu visas sarakstā esošās transakcijas, un pēc tam noklikšķiniet uz **Labi**.                  |
| D    | Lapa **Starpuzņēmumu rēķins**                                                                       | Tiek rādīts starpuzņēmumu debitora rēķina priekšlikums.                                                                                             |
| E    | Lapa **Starpuzņēmumu rēķins**                                                                       | Noklikšķiniet uz **Grāmatot**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>5. piemērs. Grāmatot kreditora rēķinu un izrakstīt rēķinu debitoram
Kad patapināšanas juridiskā persona USSI grāmato starpuzņēmumu debitora rēķinu, patapināšanas juridiskajā personā FRSI tiek izveidots atbilstošs kreditora rēķins. Pēc šī kreditora rēķina grāmatošanas FRSI arī izraksta rēķinu projekta debitoram par stundām, ko ievadīja USSI. Šī uzdevuma izpildīšanai pastāv trīs ievades punkti.

| Solis | Ieejas punkts                                                                                        | Apraksts                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Parādi kreditoriem** &gt; **Rēķini** &gt; **Neizlemtie kreditora rēķini**                            | Pārskatiet rēķinu, lai pārbaudītu, vai darba laika uzskaites vērtības ir iekļautas, un pēc tam grāmatojiet kreditora rēķinu.                  |
| B    | **Projektu vadība un uzskaite** &gt; **Projekta rēķini** &gt; **Projekta rēķinu priekšlikumi** | Izveidojiet jaunu projektu rēķinu attiecīgajam projektam un pārbaudiet, vai tajā tiek rādītas grāmatotās stundu transakcijas.            |
| C    | Lapa **Projekta rēķins**                                                                       | Atlasiet projekta rēķinu un pēc tam noklikšķiniet uz **Skatīt detalizētu informāciju**, lai pārskatītu izmaksas un pārdošanas summu. Pēc tam grāmatojiet šo rēķinu. |


Plašāku informāciju skatiet šeit: [Konfigurēt starpuzņēmumu projekta rēķinu izrakstīšanu](tasks/configure-intercompany-project-invoicing.md).


