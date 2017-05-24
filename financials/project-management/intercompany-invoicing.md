---
title: "Starpuzņēmumu rēķinu izrakstīšana"
description: "Šajā rakstā ir sniegta informācija un piemēri par projektu starpuzņēmumu rēķinu izrakstīšanu programmatūrā Microsoft Dynamics 365 for Operations."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 8af9f2c1f6720c5d0a7b98c250a2cc52a5641cef
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="intercompany-invoicing"></a>Starpuzņēmumu rēķinu izrakstīšana

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija un piemēri par projektu starpuzņēmumu rēķinu izrakstīšanu programmatūrā Microsoft Dynamics 365 for Operations.

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
Šajā piemērā USSI ir patapināšanas juridiskā persona, un tās resursiem tiek ziņots laiks attiecībā uz piesaistīšanas juridisko personu, FRSI, kurai ir noslēgts līgums ar gala klientu. USSI darbinieku ziņotās stundas un izdevumus var iekļaut projekta rēķinā, ko ģenerē FRSI. Turklāt pastāv transakciju trešais avots tādām transakcijām, kuras var rasties no patapināšanas juridiskās personas (šajā piemērā tā ir USSI), kad šī juridiskā persona sniedz kopīgus kreditoru pakalpojumus meitasuzņēmumiem (piemēram, FRSI) un pēc tam šīs izmaksas nodod tālāk projektiem šajos meitasuzņēmumos. Programmatūra Dynamics 365 for Operations nodrošina visu atbilstošo rēķinu dokumentu aizpildīšanu un nodokļu aprēķinu veikšanu. 

Šajā piemērā juridiskajai personai FRSI ir jābūt debitoram juridiskajā personā USSI un juridiskajai personai USSI ir jābūt kreditoram juridiskajā personā FRSI. Pēc tam varat iestatīt starpuzņēmumu attiecības starp abām juridiskajām personām. Nākamajā procedūrā ir parādīts, kā iestatīt parametrus tā, lai abas juridiskās personas varētu piedalīties starpuzņēmumu rēķinu izrakstīšanā.

1.  Iestatiet FRSI kā debitoru juridiskajā personā USSI un iestatiet USSI kā kreditoru juridiskajā personā FRSI. Šī uzdevuma izpildīšanai pastāv trīs ievades punkti.
    | Solis | Ieejas punkts                                                                       | apraksts   |
    |------|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | A    | Juridiskās personas USSI sadaļā noklikšķiniet uz **Debitoru parādi** &gt; **Debitori** &gt; **Visi debitori**. | Izveidojiet jaunu debitora ierakstu juridiskajai personai FRSI un atlasiet debitoru grupu.                                                                                                                                                                                                                           |
    | mljrd.    | Juridiskās personas FRSI sadaļā noklikšķiniet uz **Parādi kreditoriem** &gt; **Kreditori** &gt; **Visi kreditori**.        | Izveidot jaunu kreditora ierakstu juridiskajai personai USSI un atlasiet kreditoru grupu.                                                                                                                                                                                                                               |
    | K    | Juridiskajā personā FRSI atveriet tikko izveidoto kreditora ierakstu.                            | Sadaļas Darbību rūts cilnē **Vispārīgi**, grupā **Iestatīt** noklikšķiniet uz **Starpuzņēmumu**. Lapas **Starpuzņēmumu** cilnē **Darījumu attiecības** slīdni **Aktīvs** iestatiet uz **Jā**. Laukā **Debitora uzņēmums** atlasiet darbībā A izveidoto debitora ierakstu. |

2.  Noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Iestatījumi** &gt; **Projektu vadības un uzskaites parametri** un pēc tam noklikšķiniet uz cilnes **Starpuzņēmumu**. Veids, kādā iestatāt parametrus, ir atkarīgs no tā, vai jūs esat piesaistīšanas juridiskā persona vai patapināšanas juridiskā persona.
    -   Ja esat piesaistīšanas juridiskā persona, atlasiet iepirkuma kategoriju, kas ir jāizmanto, lai salīdzinātu ar automātiski ģenerētajiem kreditoru rēķiniem.
    -   Ja esat patapināšanas juridiskā persona, tad katrai piesaistīšanas juridiskajai personai atlasiet noklusējuma projektu kategoriju attiecībā uz katru transakcijas tipu. Projektu kategorijas tiek lietotas nodokļu konfigurēšanai, kad rēķinos iekļautā kategorija starpuzņēmumu transakcijās pastāv tikai piesaistīšanas juridiskajā personā. Varat izvēlēties, vai uzkrāt ieņēmumus starpuzņēmumu transakcijām. Šis uzkrājums tiek veikts, kad transakcijas tiek grāmatotas, un pēc tam tas tiek anulēts, kad starpuzņēmumu rēķins tiek grāmatots.

3.  Noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Iestatījumi** &gt; **Cenas** &gt; **Transfērcena**.
4.  Atlasiet valūtu, transakcijas tipu un transfertcenas modeli. Rēķinos izmantotā valūta ir valūta, kas ir konfigurēta debitora ierakstā piesaistīšanas juridiskajai personai šajā patapināšanas juridiskajā personā. Šī valūta tiek izmantota, lai noteiktu ierakstu atbilstību transfertcenu tabulā.
5.  Noklikšķiniet uz **Virsgrāmata** &gt; **Grāmatošanas iestatīšana** &gt; **Starpuzņēmumu uzskaite** un iestatiet juridisko personu USSI un FRSI attiecības.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>2. piemērs. Veidot un grāmatot starpuzņēmumu darba laika uzskaites tabulu
Patapināšanas juridiskajai personai USSI ir jāizveido un jāgrāmato darba laika uzskaites tabula kādam projektam no FRSI, piesaistīšanas juridiskās personas. Šī uzdevuma izpildīšanai pastāv divi ievades punkti.

| Solis | Ieejas punkts                                                                       | apraksts                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektu vadība un uzskaite** &gt; **Darba laika uzskaites tabulas** &gt; **Visas darba laika uzskaites tabulas** | Izveidot jaunu darba laika uzskaites tabulu. Darba laika uzskaites tabulas rindā, laukā **Juridiskā persona** atlasiet **FRSI**. Laukā **Projekta ID** atlasiet attiecīgo projektu juridiskajā personā FRSI. Ievadiet stundas katrai nedēļas dienai. |
| mljrd.    | Lapa **Darba laika uzskaites tabula**                                                                | Pēc darbplūsmas izpildes grāmatojiet šo darba laika uzskaites tabulu un pierakstiet dokumenta numuru.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>3. piemērs. Veidot un grāmatot starpuzņēmumu kreditoru rēķinu
Patapināšanas juridiskajai personai USSI ir jāizveido un jāgrāmato starpuzņēmumu kreditoru rēķins kādam projektam no FRSI, piesaistīšanas juridiskās personas. Šis kreditora rēķins tiek izrakstīts par ārpakalpojumu darbu un izdevumiem, ko izpildīja USSI apmaksāti kreditori. Šī uzdevuma izpildīšanai pastāv divi ievades punkti.

| Solis | Ieejas punkts                                                                                      | apraksts                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Parādi kreditoriem** &gt; **Rēķini** &gt; **Atvērt kreditoru rēķinus** &gt; **Jauns kreditora rēķins** | Izveidojiet jaunu kreditora rēķinu un ievadiet pakalpojumus, kas tika sniegti FRSI projekta vārdā.                                                                                                                                                                                  |
| mljrd.    | Lapa **Kreditora rēķins**                                                                      | Ievadiet rindas, kas norāda FRSI vārdā sniegtos ārpakalpojumus. Kopsavilkuma cilnē **Detalizēta informācija par rindu**, rēķina rindas cilnē **Projekts**, laukā **Projekta uzņēmums** ievadiet **FRSI**. Ievadiet projektu un atbilstošo informāciju. Pēc tam grāmatojiet šo kreditora rēķinu. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>4. piemērs. Veidot un grāmatot starpuzņēmumu rēķinu
Patapināšanas juridiskajai personai USSI ir jāizveido un jāgrāmato starpuzņēmumu rēķins. Šī uzdevuma izpildīšanai pastāv divi ievades punkti.

| Solis | Ieejas punkts                                                                                             | apraksts                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektu vadība un uzskaite** &gt; **Projekta rēķini** &gt; **Starpuzņēmumu debitora rēķins**  | Noklikšķiniet uz **Jauns**, lai atvērtu lapu **Izveidot starpuzņēmumu rēķinu**.                                                                                  |
| mljrd.    | **Projektu vadība un uzskaite** &gt; **Projekta rēķini** &gt; **Starpuzņēmumu debitoru rēķini** | Lapā **Izveidot starpuzņēmumu rēķinu** ievadiet juridisko personu, norādiet transakciju, ko vēlaties iekļaut, un pēc tam noklikšķiniet uz **Meklēt**. |
| K    | **Projektu vadība un uzskaite** &gt; **Projekta rēķini** &gt; **Starpuzņēmumu debitoru rēķini** | Atlasiet transakcijas, kuras iekļaut rēķinā, vai noklikšķiniet uz **Atlasīt visus**, lai rēķinā iekļautu visas sarakstā esošās transakcijas, un pēc tam noklikšķiniet uz **Labi**.                  |
| D    | Lapa **Starpuzņēmumu rēķins**                                                                       | Tiek rādīts starpuzņēmumu debitora rēķina priekšlikums.                                                                                             |
| E    | Lapa **Starpuzņēmumu rēķins**                                                                       | Noklikšķiniet uz **Grāmatot**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>5. piemērs. Grāmatot kreditora rēķinu un izrakstīt rēķinu debitoram
Kad patapināšanas juridiskā persona USSI grāmato starpuzņēmumu debitora rēķinu, patapināšanas juridiskajā personā FRSI tiek izveidots atbilstošs kreditora rēķins. Pēc šī kreditora rēķina grāmatošanas FRSI arī izraksta rēķinu projekta debitoram par stundām, ko ievadīja USSI. Šī uzdevuma izpildīšanai pastāv trīs ievades punkti.

| Solis | Ieejas punkts                                                                                        | apraksts                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Parādi kreditoriem** &gt; **Rēķini** &gt; **Neizlemtie kreditora rēķini**                            | Pārskatiet rēķinu, lai pārbaudītu, vai darba laika uzskaites vērtības ir iekļautas, un pēc tam grāmatojiet kreditora rēķinu.                  |
| mljrd.    | **Projektu vadība un uzskaite** &gt; **Projekta rēķini** &gt; **Projekta rēķinu priekšlikumi** | Izveidojiet jaunu projektu rēķinu attiecīgajam projektam un pārbaudiet, vai tajā tiek rādītas grāmatotās stundu transakcijas.            |
| K    | Lapa **Projekta rēķins**                                                                       | Atlasiet projekta rēķinu un pēc tam noklikšķiniet uz **Skatīt detalizētu informāciju**, lai pārskatītu izmaksas un pārdošanas summu. Pēc tam grāmatojiet šo rēķinu. |





