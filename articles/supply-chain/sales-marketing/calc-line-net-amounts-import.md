---
title: Pārrēķināt rindu neto summas, importējot pārdošanas pasūtījumus un piedāvājumus
description: Šajā rakstā ir aprakstīts, vai un kā sistēma pārrēķina rindu neto summas, kad tiek importēti pārdošanas pasūtījumi un piedāvājumi. Šeit aprakstīts arī, kā varat kontrolēt uzvedību dažādās Microsoft versijās Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 08/05/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2022-06-08
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: edda0c016130e2a273adf8f3d3e00e2d3ae9d5c6
ms.sourcegitcommit: ce58bb883cd1b54026cbb9928f86cb2fee89f43d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719339"
---
# <a name="recalculate-line-net-amounts-when-importing-sales-orders-and-quotations"></a>Pārrēķināt rindu neto summas, importējot pārdošanas pasūtījumus un piedāvājumus

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, vai un kā sistēma pārrēķina rindu neto summas, kad tiek importēti pārdošanas pasūtījumi un piedāvājumi. Šeit aprakstīts arī, kā varat kontrolēt uzvedību dažādās Microsoft versijās Dynamics 365 Supply Chain Management.

## <a name="how-updates-to-net-line-amounts-are-calculated-on-import"></a>Kā importēšanas laikā tiek aprēķināti neto rindu summu atjauninājumi

Piegādes ķēdes pārvaldības versija 10.0.23 [604418](https://fix.lcs.dynamics.com/issue/results/?q=604418). Šis kļūdas labojums izmainīja **nosacījumus**, saskaņā ar kuriem neto summas lauku rindā var atjaunināt vai pārrēķināt, kad tiek importēti esošo pārdošanas pasūtījumu un piedāvājumu atjauninājumi. Versijā 10.0.29 varat aizstāt šo kļūdu *, ieslēdzot importēšanas līdzekļa rindas Neto summas aprēķins*. Šai funkcijai ir līdzīga ietekme, bet tā nodrošina globālu iestatījumu, kas ļauj atgriezties pie vecās uzvedības, ja nepieciešams. Lai gan jaunā uzvedība padara sistēmu darbojas daudz jaunā veidā, tā var radīt neparedzētus rezultātus noteiktos scenārijos, kuros ir spēkā visi šie nosacījumi:

- *Dati, kas atjaunina esošos ierakstus, tiek importēti, izmantojot pārdošanas pasūtījuma rindas V2*, *pārdošanas piedāvājuma rindas V2* vai Atgriešanas pasūtījuma rindu elementu, *izmantojot* Atvērto datu protokolu (OData), tostarp situācijas, kad izmantojat duālās rakstīšanas, importēšanas/eksportēšanas, izmantojot Excel, un dažas trešās puses integrācijas.
- [Tirdzniecības līgumu vērtēšanas politikas](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper), kas atrodas vietā, izveido izmaiņu politiku, kas ierobežo neto summas lauka atjauninājumus pārdošanas pasūtījuma rindās, pārdošanas piedāvājuma rindās un/vai atgriešanas **pasūtījuma** rindās. Ievērojiet, ka atgriešanas pasūtījuma rindām **neto** summas lauks vienmēr tiek aprēķināts un to nevar iestatīt manuāli.
- Importētie **dati** ietver izmaiņas neto summas laukā rindās vai izmaiņas (piemēram, vienības cenu, daudzumu vai atlaidi), **kas** izraisīs neto summas lauka vērtību rindās, kas jāpārrēķina vienam vai vairākiem esošiem rindas ierakstiem.

Šajos noteiktos scenārijos tirdzniecības līgumu novērtēšanas politikas ietekme uz neto **summas** lauka atjaunināšanu rindā rada ierobežojumu. Šis ierobežojums pazīstams kā *izmaiņu politika*. Šīs politikas dēļ, kad izmantojat lietotāja interfeisu lauka labošanai vai pārrēķinam, sistēma prasa, lai jūs apstiprināsit, vai vēlaties veikt izmaiņas. Tomēr, importējot ierakstu, sistēmai ir jāveic jūsu izvēle. Pirms versijas 10.0.23 sistēma vienmēr atstāja rindas neto summu nemainīgu, ja ienākošās rindas neto summa nav 0 (nulle). Tomēr jaunākās versijās sistēma vienmēr atjaunina vai pārrēķina neto summu, kā nepieciešams, ja vien nav skaidri norādīts, ka tā nav skaidra. Lai gan jaunā uzvedība ir loģiskāka, tas var radīt problēmas jums, ja jūs jau darbojaties procesus vai integrācijas, kas pieņem vecāko uzvedību. Šajā rakstā ir aprakstīts, kā atgriezties pie vecās uzvedības, ja nepieciešams.

## <a name="control-calculations-of-line-net-amounts-in-versions-10029-and-later"></a>Kontrolēt rindu neto summu aprēķinus versijās 10.0.29 vai jaunākās versijās

Piegādes ķēdes pārvaldības versija 10.0.29 tika ieviesta funkcija ar nosaukumu *Aprēķināt rindas neto summu importam*. Šī funkcija pievieno opciju ar nosaukumu Aprēķināt rindas **neto summu** debitoru **parādu parametru lapai**. Šī opcija ļauj atlasīt starp jauno un mantojuma uzvedību rindas importa neto summu aprēķināšanai.

### <a name="turn-the-calculate-line-net-amount-on-import-feature-on-or-off"></a>Ieslēgt vai izslēgt importēšanas līdzekli Aprēķināt rindas neto summu

Kad atjaunināt uz versiju 10.0.29, *opcija Aprēķināt rindas neto summu importēšanai pēc noklusējuma ir ieslēgta,* **un opcija Aprēķināt rindas neto summu sākotnēji tiek iestatīta uz** Jā *.* Iestatījums *Jā* atbilst jaunajai standarta funkcionalitātei. Tā atbilst sistēmas funkcionalitātei, ja funkcija ir izslēgta, [izņemot parametru CalculateLineAmount funkcionalitātes](#CalculateLineAmount) gadījumā, kā aprakstīts tālāk šajā rakstā. Neviens *iestatījums* neatbilst sistēmas funkcionalitātei pirms versijas 10.0.23 un tas galvenokārt paredzēts mantojuma integrācijas scenāriju atbalstam.

Administratori var ieslēgt vai izslēgt *importēšanas līdzekli Aprēķināt* rindas neto summu, izmantojot līdzekļu pārvaldības [darbvietu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="set-the-calculate-line-net-amount-option"></a>Opcijas Aprēķināt rindas neto summu iestatīšana

Ja ir *ieslēgta opcija Aprēķināt rindas* neto summu importa funkcijai, opciju **Aprēķināt rindas neto summu** varat iestatīt, veidojot šādus soļus.

1. Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru parādu parametri**.
1. Cilnē **Cenas**, kas atrodas **kopsavilkuma cilnē Rindas neto** summas aprēķināšana, izmantojot integrāciju, **iestatiet** opciju Aprēķināt rindas neto summu uz vienu no šīm vērtībām:

    - *Jā* – sistēma vienmēr pārrēķinās un vajadzības gadījumā atjauninās rindu summas. (Tādēļ tā ignorēs tirdzniecības līgumu novērtēšanas politiku.)
    - *Nē* – ja esošā vai ienākošā neto summa jebkurai rindai ir 0 (nulle), šīs rindas vērtība tiek pārrēķināta, pamatojoties uz citām vērtībām (piemēram, vienības cenu, daudzumu un atlaidi). Ja esošā vai ienākošā neto summa atšķiras no 0 (nulle) **un** izmaiņu politika ir iestatīta neto summas laukā rindā, lauks netiek pārrēķināts un atjaunināts, pat ja ienākošās izmaiņas rindas cenā, daudzumā un/vai atlaidē nozīmē, ka rindas kopsumma ir jāpārrēķina. Šī darbība atbilst versijai 10.0.22.

### <a name="how-the-calculate-line-net-amount-on-import-feature-affects-the-calculatelineamount-parameter"></a><a name="CalculateLineAmount"></a> Kā aprēķināt rindas neto summu importa funkcijai ietekmē parametru CalculateLineAmount

Ja ir *ieslēgta funkcija Aprēķināt rindas* neto summu importa funkcijai, šīs tabulas `CalculateLineAmount` parametra `SalesLine` vērtībai `SalesQuotationLine` nav ietekmes. Tā vietā darbību globāli kontrolē opcija **Aprēķināt rindas neto summu**, kas aprakstīta iepriekšējā sadaļā. Tādēļ, ja funkcija ir ieslēgta, jūs nevarat ņemt nekādu atkarību no `CalculateLineAmount` vērtības.

*Kad* ir izslēgta importēšanas funkcijas rindas neto summa, `CalculateLineAmount``SalesLine``SalesQuotationLine` parametrs un tabulas darbojas tāpat kā piegādes ķēdes pārvaldības versijās 10.0.23 līdz 10.0.28 atbilstoši aprakstam nākamajā sadaļā.

## <a name="control-line-net-amount-calculations-in-versions-10028-and-earlier"></a>Kontroles rindas neto summas aprēķini versijās 10.0.28 un vecākās versijās

Kad [10.0.23. versijā tika ieviests kļūdu labojums 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418), bija iespējams atlasīt, kā katram atbilstošajam datu elementam ir jābūt uzrādāmam, kad rindas neto summa tika rediģēta vai bija jāpārrēķina citu izmaiņu dēļ (piemēram, atjaunināta krājuma cena). Jūs variet kontrolēt šo darbību, iestatot `CalculateLineAmount` jaunu parametru katrai rindai uz vienu no šīm vērtībām importētā failā:

- **`CalculateLineAmount` = *1*** – **Neto summas lauks** rindā vienmēr tiek pārrēķināts un atjaunināts, neatkarīgi no tā, vai izmaiņu politika ir iestatīta laukam un neatkarīgi no ienākošās vai esošās rindas neto summas vērtības.
- **`CalculateLineAmount` = *0*** – ja esošā vai ienākošā neto summa jebkurai rindai ir 0 (nulle), šīs rindas vērtība tiek pārrēķināta, pamatojoties uz citām vērtībām (piemēram, vienības cenu, daudzumu un atlaidi). Ja esošā vai ienākošā neto summa atšķiras no 0 (nulle), **un** izmaiņu politika ir iestatīta rindas laukā Neto summa, lauks netiek pārrēķināts vai atjaunināts.  

Sistēmas uzvedība ir atkarīga no jūsu Piegādes ķēdes pārvaldības versijas:

- Versijā 10.0.22 un vecākā versijā sistēma vienmēr izveidojās tā, `CalculateLineAmount`*it kā būtu iestatīta uz 0*, `CalculateLineAmount`*un nav iespējams to padarīt parādību, it kā tā būtu iestatīta uz 1*.
- Versijās `CalculateLineAmount`*10.0.23 līdz 10.0.28 sistēma ir iestatīta kā 1* visām *rindām, kur importa failā tā nav skaidri iestatīta uz 0*.
