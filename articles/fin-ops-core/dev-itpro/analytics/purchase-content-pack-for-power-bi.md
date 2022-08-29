---
title: Power BI satura pakotne Pirkšanas tēriņu analīze
description: Šajā rakstā ir aprakstīts, kas ir iekļauts pirkšanas tēriņu analīzes saturā Power BI.
author: FrankDahl
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.form: PurchaseSpendAnalysisPowerBI
ms.openlocfilehash: 757b782131617104422e15f3ceec747b92d96666
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276666"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>Power BI satura pakotne Pirkšanas tēriņu analīze

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kas ir iekļauts pirkšanas **tēriņu analīzes saturā** Microsoft Power BI. Tajā ir paskaidrots, kā piekļūt Power BI pārskatiem, kā arī ir sniegta informācija par satura izstrādei izmantoto datu modeli un elementiem.

## <a name="overview"></a>Pārskats

Power BI satura pakotne **Pirkšanas tēriņu analīze** ir izveidota, lai palīdzētu iepirkumu nodaļas vadītājiem un par budžetu atbildīgajiem sekot pirkšanas tēriņiem. Vadītāji var analizēt pirkumu tēriņus šādos veidos:

- Līdzšinējā gada pirkumi (pēc kreditoru grupas, atsevišķa kreditora, sagādes kategorijas, atsevišķas preces un kreditora atrašanās vietas)
- Pirkumu izmaiņas pa gadiem (pēc kreditoru grupas un sagādes kategorijas)

Saturam tiek izmantoti pirkumu transakciju dati, un tas nodrošina gan uzņēmuma līmeņa pirkumu rādītāju apkopošanas skatu, gan pirkumu tēriņu sadalījumu pēc kreditora vai preces. Pārskatos ir izceltas pirkumu tēriņu izmaiņas laika gaitā. Tāpēc pārskatus var izmantot, lai brīdinātu vadītājus par pozitīvām un negatīvām tēriņu tendencēm saistībā ar atsevišķiem kreditoriem un precēm. Turklāt diagrammas ataino pirkumu tēriņus dažādām sagādes kategorijām un kreditoru grupām. Tādēļ kategoriju un reģionālie vadītāji var izmantot šīs diagrammas, lai palīdzētu noteikt tēriņu darbību izmaiņas.

## <a name="accessing-the-power-bi-content"></a>Piekļuve Power BI satura pakotnei
Power BI satura pakotne **Pirkšanas tēriņu analīze** tiek rādīta lapā **Pirkšanas un tēriņu rādītāju analīze** (**Sagāde un avoti** \> **Pieprasījumi un pārskati** \> **Pirkšanas rādītāju analīze** \> **Pirkšanas un tēriņu rādītāju analīze**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI satura pakotnē iekļautie rādītāji
Power BI satura pakotnē **Pirkšanas tēriņu analīze** ir iekļauts pārskats, kas sastāv no rādītāju kopas. Šie rādītāji tiek vizualizēti kā diagrammas, elementi un tabulas. 

Zemāk norādītajās sadaļās ir sniegts pārskats par vizualizācijām.

### <a name="purchase-by-vendor-report-page"></a>Pārskata lapa pirkumiem pēc kreditora
**Diagrammas**
- Pirmie 10 kreditori pēc pirkšanas (joslu grēdu diagramma)
- Pirkumu kopsumma pēc kreditoru grupas/valsts/nosaukuma (sektoru diagramma)
- Pirkumi pēc kreditoru grupas/valsts/nosaukuma (stabiņu diagramma)
- Vidējie pirkumi pēc kreditoru grupas/valsts/nosaukuma (stabiņu diagramma)

**Elementi**
- Kopējā pirkšana
- Pirkumu palielinājums pa gadiem
- Kreditoru kopskaits
- Aktīvo kreditoru kopskaits

**Piemērs**
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a>Pārskata lapa pirkumiem pēc preces

**Diagrammas**
- Pirkumi pēc sagādes kategorijas/preces nosaukuma (stabiņu diagramma)
- Pirkumu kopsumma pēc sagādes kategorijas/preces nosaukuma (sektoru diagramma)
- Pirmās 10 preces pēc pirkšanas (joslu grēdu diagramma)

**Elementi**
- Preču kopskaits</li>
- Aktīvo preču kopskaits procentos no preču kopskaita
- To preču skaits, kas veido 80% pirkumu

**Piemērs**


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a>Pārskata lapa pirkumiem pēc perioda
Šajā lapā parādīti šī gada un pagājušā gada pirkumi un palielinājums pēc sagādes kategorijas.

**Diagrammas** 
- Pirkumi pēc mēneša/dienas (stabiņu diagramma)
- Apkopotā pirkumu novirze pa gadiem (ūdenskrituma diagramma)
- Pirkumu kopsummas palielinājums pa gadiem (stabiņu diagramma)
- Sagādes izraksts (matrica)

**Elementi**
- Pirkumu palielinājums pa gadiem
- Pirkumu palielinājums (%)

**Piemērs**
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a>Pārskata lapa pirkumiem pēc vietas

**Diagrammas**
- Pirkumi pēc pilsētas
- Pirkumu palielinājums pa gadiem (%)
- Pirkumi pēc valsts

**Piemērs**
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a>Pārskata lapa pirkumu tēriņu analīzei pēc laika

**Diagrammas** 
- Pašreizējā gada pirkumi pēc mēneša/dienas (līniju diagramma)
- Pašreizējā un pagājušā gada pirkumi (līniju un stabiņu diagramma)

**Piemērs**
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a>Pārskata lapa pirkumu tēriņu analīzei pēc kreditora

**Diagrammas** 
- Pirmo 10 kreditoru pirkumi procentos (%) no pirkumiem (piltuves diagramma)
- Pirmie 10 kreditori ar palielinātiem tēriņiem pa gadiem
- Pirmie 10 kreditori ar samazinātiem tēriņiem pa gadiem

**Piemērs** 
<img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a>Datu modelis un elementi
Power BI satura pakotnes **Pirkšanas tēriņu analīze** pārskatu lapu aizpildīšanai tiek izmantoti tālāk norādītie dati. Šie dati tiek attēloti kā apkopoti mērījumi, kas tiek sagatavoti elementu krātuvē. Elementu krātuve ir analīzei optimizēta Microsoft SQL Server datu bāze. Papildinformāciju skatiet rakstā [Power BI integrācija elementu krātuvē](power-bi-integration-entity-store.md).

Šajā satura pakotnē ietvertie apkopošanas mērījumi ir to apkopošanas mērījumu apakškopa, kas ir pieejami pirkšanas kubā programmās Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3. Lai padarītu kuba apkopošanas mērījumus pieejamus elementu krātuvē, tie ir jāpadara izvietojami. Papildinformāciju skatiet emuāra ieraksta [Power BI integrāciju elementu krātuve](power-bi-integration-entity-store.md) sadaļā par procedūru apkopošanas mērījumu sagatavošanai elementu krātuvē. Tālāk norādītie galvenie apkopošanas mērījumi ir tieši pieejami no elementa Rēķina rindas, un tie tiek izmantoti kā satura pamatdati.

| Elements        | Galvenie apkopošanas mērījumi | Datu avots                                 | Lauks              | Apraksts                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Rēķina rindas | Pirkšana                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Summa uzskaites valūtā. |

Tālāk esošajā tabulā ir norādīti galvenie satura mērījumi, kas tiek aprēķināti no elementa Rēķina rindas.

| Mērs               | Aprēķins                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Pašreizējā gada pirkumi | Pašreizējā gada pirkumi = SUM('Rēģina rindas'\[Pirkšana\])                                            |
| Pagājušā gada pirkumi    | Pagājušā gada pirkumi = CALCULATE(SUM('Rēķina rindas'\[Pirkšana\]), SAMEPERIODLASTYEAR(Datumi\[Datums\])) |
| Pirkumu palielinājums pa gadiem   | Pirkumu palielinājums pa gadiem = \[Pašreizējā gada pirkumi\] – \[Pagājušā gada pirkumi\]                            |

Tālāk norādītās galvenās dimensijas saturam tiek izmantotas kā filtri, lai sadalītu apkopošanas mērījumus, iegūstot lielāku granularitāti un sniedzot dziļākus analītiskos ieskatus.

| Elements                 | Atribūtu piemēri                                |
|------------------------|-------------------------------------------------------|
| Kreditori                | Kreditoru grupas, Kreditora valsts vai reģions, Kreditora nosaukums |
| Preces               | Preces numurs, Preces nosaukums, Krājumu grupas nosaukums        |
| Sagādes kategorijas | Sagādes kategorija, Sagādes kategoriju nosaukumi      |
| Juridiskas personas         | Juridiskās personas nosaukums                                     |
| Datumi                  | Datumi, Gada nobīde                                    |

Pēc noklusējuma saturs nodrošina pašreizējā kalendārā gada datu rādīšanu. Taču varat mainīt datumu filtru pārskata filtru sadaļā. Varat mainīt arī uzņēmuma filtru.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
