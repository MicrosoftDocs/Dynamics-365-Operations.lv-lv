---
title: Elektronisko pārskatu veidotāja atbalstītie saliktie datu tipi
description: Šajā rakstā ir sniegta informācija par saliktajiem datu tipiem, kas tiek atbalstīti elektronisko pārskatu (ER) formulās.
author: NickSelin
ms.date: 06/02/2021
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc3fbe695d79eb0ec9796d471c4d2bb0bb7ab99d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869320"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a>Elektronisko pārskatu veidotāja atbalstītie saliktie datu tipi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par saliktajiem datu tipiem, kas tiek atbalstīti [elektronisko pārskatu (ER)](general-electronic-reporting.md) izteiksmēs. Saliktu datu tipi ir [class](#class), [container](#container), [record](#record), [record list](#record-list) un [object](#object).

## <a name="class"></a><a name="class"></a>Klase

Datu tips *class* attiecas uz publisku pieteikuma klasi. Rīkā ER to apzīmē kā [*record*](#record), kas ietver atsevišķu lauku katrai atsauču klases publiskai metodei. Ja metodes izsaukums ir parametrs, jums jānorāda arī nepieciešamie argumenti atbilstošiem tipiem ER izteiksmē, kas ir konfigurēta metodes izsaukšanai.

ER kartēšanas un formāta komponentos varat pievienot klases datu avotu, **kas** tiek rādīts kā datu avots un kas atgriež klases tipa *vērtību*. Šis datu avots atklāj klases publiskās metodes, ko var izsaukt izpildlaikā.

> [!NOTE]
> No ER izteiksmēm var izsaukt tikai metodes, kas atgriež vērtību.
>
> No ER izteiksmēm var izsaukt tikai metodes, kuru diapazons ir no nulles līdz astoņiem argumentiem.

Noklusējuma vērtība datu tipam *class* ir **null**.

Attēlā parādīts, kā **klases** datu tipa datu avots **System information(xInfo)** tiek pievienots, lai izveidotu instanci pieteikuma klasei **xInfo** un izsauktu tās **productName()** metodi, lai saņemtu pašreizējā pieteikuma nosaukumu. Pašreizējā pieteikuma nosaukums tiek ienests izpildlaikā, izpildot `xInfo.productName` saistījumu, kas tika konfigurēts ER datu modeļa laukam **Software name(SoftwareName)**. Šī saistīšana izsauc **xInfo** pieteikuma klases metodi `productName()`, kas attēlota pašreizējā modeļa kartēšanā kā **Sistēmas informācijas (xInfo)** datu avots.

[![Klases datu avota konfigurēšana ER modeļa kartēšanas noformētājā.](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)

Šajā attēlā parādīts, kā ER formāts tiek konfigurēts, lai ievietotu norādīto pieteikuma nosaukumu ģenerētajos dokumentos. Izmantotā datu modeļa lauks **Software name(SoftwareName)** tika saistīts ar komponentu **Virkne**, kas ligzdots zem **softwareUsed** XML elementa ER formātā. Tātad pašreizējā pieteikuma nosaukums izpildlaikā tiek novietots ģenerētā dokumenta XML formāta **softwareUsed** XML elementā.

[![Elektronisko izejošo dokumentu struktūras konfigurēšana ER formāta noformētājā.](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)

## <a name="container"></a><a name="container"></a>Konteiners

Datu tips *container* ietver bināro saturu. Datu tipa *container* vērtību var izmantot, lai ģenerētam dokumentam no krātuves nodotu specifisku informāciju. ER struktūrā šis datu tips bieži tiek izmantots, lai ģenerētos dokumentos ievietotu multivides saturu, piemēram, uzņēmuma logotipu.

> [!NOTE]
> Lai arī katru multivides krājumu var attēlot kā *container* vērtību, ne katra *container* vērtība pārstāv multivides krājumu. Tāpēc, ja ER formāts tiek konfigurēts tā, ka tas izmanto *container*, lai ievietotu attēlu ģenerētā dokumentā, bet atsauces *container* neatgriež multivides saturu, varētu tikt parādīts izņēmums, kas ir līdzīgs šim piemēram: “Kļūda, izpildot kodu: binārais (objekts), metode constructFromContainer metodes constructFromContainer izsaukts ar nederīgiem parametriem.”

Noklusējuma vērtība *container* ir **null**.

Šajā attēlā parādīts, kā datu tipa *Konteiners* lauks **Bitmap(Image)** ir saistīts ar datu modeļa datu tipa **Konteiners** lauku **Logotips** modeļa **Pārdošanas rēķins** kartēšanā. Šis saistījums uzņēmuma logotipu padara pieejamu jebkuram ER formātam, kas ir izstrādāts **SalesInvoice** saknes definīcijai un kas izpildlaikā izmanto šo modeļa kartējumu.

[![Konteinera tipa lauka saistīšana ER modeļa kartējuma noformētājā.](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)

## <a name="record"></a><a name="record"></a>Ieraksts

Datu tips *record* ir nosauktu lauku kopums, no kuriem katrs lauks ir saistīts ar [primitīva](er-formula-supported-data-types-primitive.md) datu tipa vai saliktu datu tipa vērtību. Parasti *record* izmanto, lai atspoguļotu vienu ierakstu no ierakstu saraksta. Šajā gadījumā katrs krājums ataino atsevišķus laukus, metodes un relācijas.

Noklusējuma vērtība datu tipam *record* ir **empty**.

> [!NOTE]
> Iegūstot tukša datu tipa *record* lauka vērtību, tiek atgriezta atbilstošā datu tipa noklusējuma vērtība.

Datu tipu *record* var ietvert, izmantojot šādas funkcijas:

- [FIRST](er-functions-list-first.md)
- [FIRSTORNULL](er-functions-list-firstornull.md)
- [EMPTYRECORD](er-functions-record-emptyrecord.md)
- [NULLCONTAINER](er-functions-record-nullcontainer.md)

Papildinformāciju par *record* vērtību pārvēršanu skatiet sadaļā [ER funkciju saraksts kategoriju sarakstā](er-functions-category-list.md).

## <a name="record-list"></a><a name="record-list"></a>Ierakstu saraksts

Datu tips *record list* ir saraksts ar krājumiem datu tipā *record*. Parasti *record list* izmanto, lai attēlotu sarakstu ar ierakstiem, kas ir ienesti no datu bāzes tabulas.

Pēc noklusējuma ierakstiem no *record list* var piekļūt secīgi. Lai piekļūtu konkrētam ierakstam, varat izmantot funkciju [INDEX](er-functions-list-index.md) un norādīt datu tipa *integer* indeksu.

Noklusējuma vērtība datu tipam *record list* ir **empty**. Varat izmantot [ISEMPTY](er-functions-list-isempty.md) funkciju, lai novērtētu, vai *record list* ir tukšs.

> [!NOTE]
> Ja *record list* ir tukšs, visi mēģinājumi iegūt lauka vērtību no datu tipa *record* izraisa izņēmumu izpildlaikā. Lai uzzinātu, kā palīdzēt novērst šī tipa izpildlaika izņēmumus, skatiet sadaļu [Tukšu sarakstu gadījumu apsvēršana](er-components-inspections.md#i9).

Datu tipu *record list* var aktivizēt, izmantojot šādas funkcijas:

- [ALLITEMS](er-functions-list-allitems.md)
- [ALLITEMSQUERY](er-functions-list-allitemsquery.md)
- [EMPTYLIST](er-functions-list-emptylist.md)
- [LIST](er-functions-list-list.md)
- [LISTDISTINCT](er-functions-list-listdistinct.md)

Papildinformāciju par *record list* vērtību pārvēršanu skatiet sadaļā [ER funkciju saraksts kategoriju sarakstā](er-functions-category-list.md). Lai uzzinātu, kā ieviest *record list* krājumus, aizpildiet tos ar pieteikuma datiem un pēc tam izmantojiet datus, lai ģenerētu biznesa dokumentus, skatiet sadaļu [Noformēt jaunu ER risinājumu, lai drukātu pielāgotu pārskatu](er-quick-start1-new-solution.md).

## <a name="object"></a><a name="object"></a>Objekts

Datu tips *object* attiecas uz *class* stāvokļa instanci. Parasti *object* tiek aktivizēts pirmkodā. Pēc tam tas tiek nodots ER modeļa kartēšanai un sniedz detalizētu informāciju par izpildes kontekstu.

Noklusējuma vērtība datu tipam *object* ir **null**.

Attēlā parādīts, kā *Objekta* tipa datu avots **ReportDataContract** tiek pievienots, lai informāciju par ģenerēto rēķinu no avota koda nodotu **Projekta rēķina** modeļa kartējumam. Piemēram, rēķina instances teksts tiek nodots kā daļa no izpildes konteksta. Šis teksts tiek ņemts no avota koda izpildlaikā, izpildot `ReportDataContract.parmInvoiceInstanceText` saistījumu, kas tika konfigurēts ER datu modeļa **Piezīmes** laukam. Šī saistīšana izsauc **PSAProjInvoiceContract** pieteikuma klases metodi `parmInvoiceInstanceText()`, kas attēlota pašreizējā modeļa kartēšanā kā **ReportDataContract** datu avots.

[![Objekta datu avota konfigurēšana ER modeļa kartēšanas noformētājā.](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)

Lai uzzinātu, kā nodot izpildes konteksta informāciju no avota koda uz palaisto ER risinājumu, skatiet sadaļu [Pieteikumu artefaktu izstrādāšana, lai izsauktu paredzēto pārskatu](er-quick-start1-new-solution.md#DevelopCustomCode).

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)
- [Elektronisko pārskatu veidošanas formulu valoda](er-formula-language.md)
- [Atbalstītie primitīvie datu tipi](er-formula-supported-data-types-primitive.md)
