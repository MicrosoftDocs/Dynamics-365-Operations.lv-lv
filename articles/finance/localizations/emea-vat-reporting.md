---
title: PVN pārskati Eiropai
description: Šajā rakstā sniegta vispārīga informācija par pievienotās vērtības nodokļa (PVN) pārskata iestatīšanu un ģenerēšanu dažām Eiropas valstīm.
author: mrolecki
ms.date: 03/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: mrolecki
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 266844
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
ms.openlocfilehash: 54be8844fadf744cc5527001737ab470fcec46d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283417"
---
# <a name="vat-reporting-for-europe"></a>PVN pārskati Eiropai

[!include [banner](../includes/banner.md)]

Šajā rakstā sniegta vispārīga informācija par pievienotās vērtības nodokļa (PVN) pārskata iestatīšanu un ģenerēšanu dažām Eiropas valstīm.

Šis raksts sniedz vispārēju pieeju PVN deklarācijas iestatīšanai un ģenerēšanu. Šo metodi izmanto lietotāji juridiskajās personās tālāk norādītajās valstīs/reģionos.

-   Austrija
-   Beļģija
-   Čehija
-   Igaunija
-   Somija
-   Vācija
-   Latvija
-   Lietuva
-   Nīderlande
-   Zviedrija

> [!IMPORTANT]
> Šajā rakstā aprakstītie līdzekļi Austrijai, Čehijai, Vācijai, Nīderlandei un Zviedrijai ir novecojuši. Papildinformāciju skatiet sadaļā Noņemtie [un novecojušie līdzekļi](../get-started/removed-deprecated-features-finance.md).
> Izmantojiet šajā tabulā norādītās saites, lai uzzinātu vairāk par jauno PVN deklarāciju dizainu attiecīgajās valstīs.
> 
>
> | Valsts/reģions        | Papildinformācija                                                          |
> |----------------|---------------------------------------------------------------------------------|
> | Austrija        | [PVN deklarācija (Austrija)](emea-aut-vat-declaration-austria.md)       |                                                                           
> | Čehijas Republika | [PVN deklarācija (Čehijas Republika)](emea-cze-vat-declaration-tax-declaration-model.md) |
> | Dānija        | [PVN deklarācija (Dānija)](emea-dnk-vat-declaration-denmark.md)         |
> | Francija         | [PVN deklarācija (Francija)](emea-fra-vat-declaration-preview-france.md)       |
> | Vācija        | [PVN deklarācija (Vācija)](emea-deu-vat-declaration-germany.md)           |
> | Nīderlande    | [PVN deklarācija (Nīderlande)](emea-nl-vat-declaration-netherlands.md)    |
> | Norvēģija         | [PVN atgriešana ar tiešo iesniegšanu Altinn](emea-nor-vat-return.md) |
> | Spānija          | [PVN deklarācija (Spānija)](emea-esp-vat-declaration-spain.md)              |
> | Zviedrija         | [PVN deklarācija (Zviedrija)](emea-swe-vat-declaration-sweden.md)          |
> | Šveice    | [PVN deklarācija (Šveice)](emea-che-vat-declaration-switzerland.md) |
> | Uk             | [Sagatavošanās integrēšanai MRD iekļaušanai PVN](emea-gbr-mtd-vat-integration.md) |

## <a name="vat-statement-overview"></a>PVN deklarācijas apskats
PVN deklarācija ir balstīta uz nodokļu transakciju summām. PVN deklarācijas ģenerēšanas process ietilpst PVN maksājuma procesā, kurš ir ieviests ar funkciju Nosegt un grāmatot PVN. Šī funkcija aprēķina PVN, kurš ir jāmaksā par attiecīgo periodu. Nosegšanas aprēķinā ir iekļauts atlasītajam nosegšanas periodam nodokļu transakcijām grāmatotais PVN. Process PVN deklarācijas datu aprēķināšanai ir balstīts uz attiecībām starp PVN kodiem un PVN pārskatu kodiem, kur PVN pārskatu kodi atbilst PVN deklarācijas lodziņiem (vai etiķetēm XML failā). Attiecībā uz katru PVN kodu ir jāiestata PVN pārskatu kodi katram transakcijas tipam, piemēram, ar nodokli apliekamajai pārdošanai, ar nodokli apliekamajiem pirkumiem, ar nodokli apliekamajam importam. Šī veida darbības ir aprakstītas PVN kodus PVN pārskatu sadaļai tālāk šajā rakstā.

Katram PVN pārskatu kodam ir jānorāda noteikts pārskata izkārtojums. Tajā pašā laikā PVN kodi ir saistīti ar noteiktu PVN iestādi, izmantojot PVN nosegšanas periodus. Katrai PVN iestādei ir jānorāda noteikts pārskata izkārtojums. Tādējādi PVN koda pārskatu iestatīšanā var atlasīt tikai PVN pārskatu kodus ar vienādu pārskata izkārtojumu, kas attiecībā uz šo PVN kodu ir iestatīti PVN iestādei PVN nosegšanas periodos. Ar pasūtījuma vai žurnāla grāmatošanu ģenerēta PVN transakcija ietver PVN kodu, PVN avotu, PVN virzienu un transakciju summas (nodokļu bāzes summu un nodokļu summu uzskaites valūtā, PVN valūtā un transakcijas valūtā). Pamatojoties uz nodokļu transakciju atribūtu kombināciju, transakciju summas veido kopējās summas PVN pārskatu kodiem, kas norādīti PVN kodiem. Nākamajā attēlā ir redzamas datu attiecības.

![diagramma.](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a>PVN pārskata iestatīšana
Lai ģenerētu PVN pārskatu, ir jāiestata tālāk aprakstītie priekšnoteikumi.

### <a name="sales-tax-authorities-for-vat-reporting"></a>PVN iestādes PVN pārskatiem

Lai varētu iestatīt PVN pārskatu kodus, ir jāatlasa attiecīgajai PVN iestādei atbilstošais pārskata izkārtojums. Lapā **PVN iestādes**, sadaļā **Vispārīgi** atlasiet vienumu **Pārskata izkārtojums**. Šis izkārtojums tiek izmantots, kad iestatāt PVN pārskatu kodus.

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a>PVN pārskatu kodi

PVN pārskatu kodi ir lodziņu kodi PVN deklarācijā vai etiķešu nosaukumi XML formātā. Šie kodi tiek izmantoti, lai pārskatam apkopotu un sagatavotu summas. Kad konfigurējat PVN deklarācijas elektroniskā pārskata formātu, tiek izmantoti rezultātu summu nosaukumi. PVN pārskatu kodus varat izveidot un uzturēt lapā **PVN pārskatu kodi**. Katram kodam ir jāpiešķir kāds pārskata izkārtojums. Pēc PVN pārskatu kodu izveidošanas šos kodus varat izvēlēties lapas **PVN kodi** sadaļā **Pārskata iestatīšana**. <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a>PVN kodi PVN pārskatiem

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> PVN transakciju bāzes summas un nodokļu summas PVN deklarācijā var apkopot pārskatu kodos (XML etiķetēs vai deklarācijas lodziņos). Šo iespēju varat iestatīt, saistot PVN pārskatu kodus dažādiem transakciju tipiem PVN kodos lapā <strong>PVN kodi</strong>. Nākamajā tabulā ir aprakstīti transakciju tipi pārskatu iestatīšanai PVN kodiem. Šajā aprēķinā ir iekļautas transakcijas no visu tipu avotiem, izņemot PVN.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Transakcijas tips</strong></td>
<td><strong>Transakciju apraksts un summas, ko aprēķināt šim transakciju tipam</strong></td>
</tr>
<tr class="even">
<td><strong>Ar nodokli apliekamā pārdošana</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā/</li>
<li>Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Pārdošana bez nodokļiem</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li>Pārdošana ir eksports (<strong>Nodokļu virziens</strong> ir <strong>Pārdošana bez nodokļiem</strong>).</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Maksājamais PVN</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li>Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Ar nodokli apliekama pārdošanas kredīta nota</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li>Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Ar nodokli neapliekama pārdošanas kredīta nota</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li>Pārdošana ir eksports (<strong>Nodokļu virziens</strong> ir <strong>Pārdošana bez nodokļiem</strong>).</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>PVN pārdošanas kredīta notā</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li>Pārdošana ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Maksājamais PVN</strong>).</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Ar nodokļiem apliekamie pirkumi</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li>Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Pirkšana bez nodokļiem</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li>Pirkums ir imports (<strong>Nodokļu virziens</strong> ir <strong>Pirkšana bez nodokļiem</strong>).</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Saņemtais PVN</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li>Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Ar nodokli apliekama pirkšanas kredīta nota</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li>Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Ar nodokli neapliekama pirkšanas kredīta nota</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li>Pirkums ir imports (<strong>Nodokļu virziens</strong> ir <strong>Pirkšana bez nodokļiem</strong>).</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>PVN pirkšanas kredīta notā</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li>Pirkums ir iekšzemes (<strong>Nodokļu virziens</strong> ir <strong>Saņemtais PVN</strong>).</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Ar nodokli apliekams imports</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong></li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Apliekamais imports</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju apgrieztā summa <strong>Nodokļu bāzes summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Ar nodokli apliekama importa kredīta nota</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu bāzes summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
e<li><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Apliekamā importa kredīta nota</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju apgrieztā summa <strong>Nodokļu bāzes summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li>Nodokļu virziens ir <strong>Importa nodoklis</strong>.</li>
d<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Importa nodoklis</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju summa <strong>Nodokļu summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Kompensēt importa nodokli</strong></td>
<td>Tālāk aprakstītajiem nosacījumiem atbilstošu nodokļu transakciju apgrieztā summa <strong>Nodokļu summas</strong>.
<ul>
<li>Transakcijas datums ietilpst atlasītajā periodā.</li>
<li><strong>Nodokļu virziens</strong> ir <strong>Importa nodoklis</strong>.</li>
<li>Transakcijas <strong>Nodokļu bāzes summa</strong> vai <strong>Nodokļu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Iepriekšējā tabulā tiek pieņems, ka tiek ievēroti tālāk aprakstītie kritēriji. 
> -   Nodokļu bāzes summa ir transakcijas summa no lauka **Izcelsme uzskaites valūtā**.
> -   Nodokļu summa ir transakcijas summa no lauka **Reālā PVN summa uzskaites valūtā**.

### <a name="configure-the-er-model-and-format-for-the-report"></a>Pārskatam konfigurēt ER modeli un formātu

Varat izmantot elektronisko pārskatu veidošanu (Electronic Reporting — ER), lai datus eksportētu dažādos elektroniskajos formātos, nemainot X++ kodu. Papildinformāciju skatiet tālāk norādītajos resursos.

-   [Elektronisko pārskatu veidošanas apskats](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)
-   [Lejupielādēt elektronisko pārskatu veidošanas konfigurāciju no Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [Lokalizācijas prasības — izveidot GER konfigurāciju](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a>Valstij specifiskie resursi PVN deklarācijām
Katras valsts PVN deklarācijai ir jāatbilst attiecīgās valsts likumdošanas prasībām. Nākamajā tabulā uzskaitītajām valstīm pastāv sākotnēji definēti PVN deklarāciju vispārīgie modeļi un formāti.


| Valsts/reģions        | Papildinformācija                                                          |
|----------------|---------------------------------------------------------------------------------|
| Austrija        | [PVN deklarācijas informācija Austrijai](emea-aut-vat-statement-details.md)         |
| Beļģija        |                                                                                 |
| Čehijas Republika | [PVN deklarācija Čehijai](emea-cze-vat-statement-details.md)   |
| Igaunija        | [PVN deklarācijas informācija Igaunijai](emea-est-vat-statement-details.md) |
| Somija        | [Somijas PVN pārskats](emea-fin-sales-tax-payment-report-finland.md)          |
| Vācija        | [PVN deklarācija Vācijai](emea-de-vat-declaration.md)                       |
| Itālija          | [PVN deklarāciju informācija Itālijai](emea-ita-vat-statements-details.md)            |
| Latvija         | [PVN deklarācijas informācija Latvijai](emea-lva-vat-statement-details.md)           |
| Lietuva      | [PVN deklarācijas informācija Lietuvai](emea-ltu-vat-statement-details.md)         |
| Nīderlande    | [PVN deklarācija Nīderlandei](emea-nl-vat-declaration.md)           |
| Zviedrija         | [Zviedrijas PVN pārskats](emea-swe-sales-tax-payment-report-sweden.md)          |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
