---
title: "PVN atskaišu Eiropai"
description: "Šajā tēmā ir vispārīga informācija par iestatīšanu un radot dažās Eiropas valstīs pievienotās vērtības nodokļa (PVN) deklarāciju."
author: ShylaThompson
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266844
ms.assetid: 06798e29-6140-489e-9b4e-66b45b26be2b
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 84a639b25c64821e00ca4397f42f69298953e599
ms.lasthandoff: 03/31/2017


---

# <a name="vat-reporting-for-europe"></a>PVN atskaišu Eiropai

Šajā tēmā ir vispārīga informācija par iestatīšanu un radot dažās Eiropas valstīs pievienotās vērtības nodokļa (PVN) deklarāciju.

Šī tēma sniedz vispārēju pieeju iestatīšanu un radot PVN deklarācijas. Šī pieeja ir kopējā lietotājiem juridiskām personām šādas valstīs/reģionos:

-   Austrija
-   Beļģija
-   Čehijas Republika
-   Igaunija
-   Somija
-   Vācija
-   Latvija
-   Lietuva
-   Nīderlande
-   Zviedrija

## <a name="vat-statement-overview"></a>PVN deklarāciju pārskatu
PVN deklarācijas pamatā ir nodokļu darbības summām. PVN deklarācijas ģenerēšanas process ir daļa no PVN maksāšanas process, kas tiek īstenota ar PVN nokārtot un ziņu funkciju. Šī funkcija aprēķina PVN, kas maksājams par noteiktu periodu. Nosegšanas aprēķinā ir iekļauts grāmatošanas PVN atlasītajā maksājumu periodā nodokļu darbībām par. Procesu, aprēķinot PVN deklarācijas datu pamatā ir attiecības starp PVN kodiem un PVN pārskatu kodi, kur PVN pārskatu kodi atbilst PVN pārskatu lodziņi (vai XML tagus). Katram PVN kodam PVN pārskatu kodi ir jābūt iestatītu katra veida darbību, piemēram, pārdošanas nodokli, nodokli pirkumus, apliekamo importa. Šāda veida darbības, kas aprakstītas [PVN kodi, PVN pārskatiem](#Sales tax codes for VAT reporting) sadaļu šajā tēmā.

Katram PVN pārskatu kodam ir jānosaka īpašas atskaites izkārtojumu. Tajā pašā laikā PVN kodi ir saistīti ar noteiktu PVN iestāde, izmantojot PVN maksājumu periodi. Katrai nodokļu iestādei ir jānosaka pārskata izkārtojumu. Tādējādi tikai PVN pārskatu kodi ar vienu un to pašu atskaites izkārtojumu, ka nodokļu iestādei iestatīta formā PVN maksājumu periodi PVN koda var atlasīt pārskatu iestatīšana PVN kodu. PVN darbību, kas radīts pēc nosūtīšanas rīkojumu vai žurnālu, satur PVN kods, PVN avots, PVN virziens un darījumu summas (nodokļa pamatsummai un nodokļa summa norēķinu valūtu, PVN valūta un darījuma valūtā). Pamatojoties uz nodokļu darbības atribūtu kombinācija, darījumu summas sacerēt kopējās summas PVN pārskatu kodi norādīti PVN kodus. Sekojošajā attēlā redzama attiecība datus.

![diagram](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a>PVN pārskata iestatījumi
Radīt PVN deklarācijā ir jāiestata šādi.

### <a name="sales-tax-authorities-for-vat-reporting"></a>PVN iestādes PVN pārskatiem

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-authorities/). -->
Lai iestatītu PVN pārskatu kodi, jāatlasa nodokļu iestādei pareizi atskaites izkārtojumu. Par **PVN iestādēm** lapa, jo **vispārējā** sadaļu, atlasiet **atskaites izkārtojuma**. Šis izkārtojums tiks izmantots uzstādot PVN pārskatu kodi.

### <a name="sales-tax-reporting-codes"></a>PVN pārskatu kodi

PVN pārskatu kodi ir kaste kodus PVN deklarāciju vai tagu nosaukumi XML formātā. Šie kodi tiek izmantoti, apkopot un sagatavot atskaites summas. Konfigurējot elektronisko pārskatu formu PVN deklarācijas, rezultātu summas tiks izmantoti kontaktpersonu vārdi. Varat izveidot un uzturēt PVN pārskatu kodi par **PVN pārskatu kodi** lapā. Katram kodam ir jāpiešķir atskaites izkārtojumu. Pēc tam, kad esat izveidojis PVN pārskatu kodi, var izvēlēties kodus **pārskata iestatījumi** sadaļu par **PVN kodus** lapā. <!---For more information, see [Set up sales tax reporting codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-reporting-codes/) and [Sales tax reporting codes page (Field descriptions)](http://ax.help.dynamics.com/en/wiki/sales-tax-reporting-codes-page-field-descriptions/).-->

### <a name="sales-tax-codes-for-vat-reporting"></a>PVN kodus PVN pārskatiem

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-codes/).-->Bāzes summas un nodokļu summas PVN darījumiem var apkopot atskaišu kodi PVN deklarācijā (XML tagus vai deklarāciju kastes). Jūs varat iestatīt to saistot PVN pārskatu kodi dažādiem darījumu veidiem PVN kodi par **PVN kodus** lapā. Tabulā aprakstītas darbības tipus pārskatu iestatīšana PVN kodiem. Aprēķinos ir iekļauti visu veidu avotiem, izņemot PVN darbības.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Transaction type</strong></td>
<td><strong>Darbības un summas, rēķinot uz darbības tipu apraksts</strong></td>
</tr>
<tr class="even">
<td><strong>Pārdošanas nodokļa</strong></td>
<td>Summa <strong>nodokļa bāzes summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā /</li>
<li>Pārdošana ir iekšzemes (<strong>PVN virzienu</strong> ir <strong>maksājamais PVN</strong>).</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Beznodokļu tirdzniecības</strong></td>
<td>Summa <strong>nodokļa bāzes summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li>Pārdošana ir eksporta (<strong>PVN virzienu</strong> ir <strong>beznodokļu pārdošana</strong>).</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sales tax payable</strong></td>
<td>Summa <strong>nodokļa summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li>Pārdošana ir iekšzemes (<strong>PVN virzienu</strong> ir <strong>maksājamais PVN</strong>).</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Taxable sales credit note</strong></td>
<td>Summa <strong>nodokļa bāzes summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li>Pārdošana ir iekšzemes (<strong>PVN virzienu</strong> ir <strong>maksājamais PVN</strong>).</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Faksa Neapliekamās pārdošanas kredīta notas</strong></td>
<td>Summa <strong>nodokļa bāzes summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li>Pārdošana ir eksporta (<strong>PVN virzienu</strong> ir <strong>beznodokļu pārdošana</strong>).</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Sales tax on sales credit note</strong></td>
<td>Summa <strong>nodokļa summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li>Pārdošana ir iekšzemes (<strong>PVN virzienu</strong> ir <strong>maksājamais PVN</strong>).</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable purchases</strong></td>
<td>Summa <strong>nodokļa bāzes summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li>Pirkums ir iekšzemes (<strong>PVN virzienu</strong> ir <strong>PVN ieņēmumi</strong>).</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Tax-free purchase</strong></td>
<td>Summa <strong>nodokļa bāzes summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li>Iegāde ir importa (<strong>PVN virzienu</strong> ir <strong>beznodokļu pirkuma</strong>).</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sales tax receivable</strong></td>
<td>Summa <strong>nodokļa summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li>Pirkums ir iekšzemes (<strong>PVN virzienu</strong> ir <strong>PVN ieņēmumi</strong>).</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Taxable purchase credit note</strong></td>
<td>Summa <strong>nodokļa bāzes summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li>Pirkums ir iekšzemes (<strong>PVN virzienu</strong> ir <strong>PVN ieņēmumi</strong>).</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Tax exempt purchase credit note</strong></td>
<td>Summa <strong>nodokļa bāzes summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li>Iegāde ir importa (<strong>PVN virzienu</strong> ir <strong>beznodokļu pirkuma</strong>).</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Sales tax on purchase credit note</strong></td>
<td>Summa <strong>nodokļa summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li>Pirkums ir iekšzemes (<strong>PVN virzienu</strong> ir <strong>PVN ieņēmumi</strong>).</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable import</strong></td>
<td>Summa <strong>nodokļa bāzes summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li><strong>PVN virziens</strong> ir <strong>īpašuma nodoklis</strong></li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset taxable import</strong></td>
<td>Anulētā summa <strong>nodokļa bāzes summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li><strong>PVN virziens</strong> ir <strong>īpašuma nodoklis</strong>.</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable import credit note</strong></td>
<td>Summa <strong>nodokļa bāzes summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
e<li><strong>PVN virziens</strong> ir <strong>īpašuma nodoklis</strong>.</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset taxable import credit note</strong></td>
<td>Anulētā summa <strong>nodokļa bāzes summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li>PVN virziens ir <strong>īpašuma nodoklis</strong>.</li>
d<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Use tax</strong></td>
<td>Summa <strong>nodokļa summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li><strong>PVN virziens</strong> ir <strong>īpašuma nodoklis</strong>.</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset use tax</strong></td>
<td>Anulētā summa <strong>nodokļa summas</strong> nodokļu darbībām, kas atbilst šādiem nosacījumiem:
<ul>
<li>Darbības datums ir atlasītajā periodā.</li>
<li><strong>PVN virziens</strong> ir <strong>īpašuma nodoklis</strong>.</li>
<li>Darbības <strong>nodokļa pamatsummai</strong> vai <strong>nodokļa summa</strong>&gt; 0.</li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Iepriekš redzamās tabulas, tiek pieņemts, ka ir izpildīti šādi kritēriji: 
> -   PVN bāzes summa ir darījuma summa no **izcelsmes uzskaites valūtā** lauks.
> -   Nodokļu summa ir pārejas summu no **faktiskie PVN summa norēķinu valūtu** lauks.

### <a name="configure-the-er-model-and-format-for-the-report"></a>Konfigurēt ER modelis un pārskata formātu

Elektronisko pārskatu (ER) var izmantot, lai konfigurētu pārskatus un atskaites, kā eksportēt datus dažādos elektroniskos formātos, nemainot X + + kodā. Papildu informācija:

-   [Elektronisko atskaišu veidošanas pārskats](/dynamics365/operations/dev-itpro/dev-itpro/analytics/general-electronic-reporting)
-   [Elektronisko atskaišu veidošanas konfigurāciju lejupielāde no Lifecycle Services](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)
-   [Lokalizācijas prasībām-GER konfigurācijas izveide](/dynamics365/operations/dev-itpro/analytics/electronic-reporting-configuration)

## <a name="countryspecific-resources-for-vat-statements"></a>Countryspecific resursu PVN deklarācijas
Katrai valstij PVN deklarācijā jāatbilst valsts tiesību aktu prasībām. Ir iepriekš definētas vispārējas modeļus un formāti PVN deklarāciju attiecībā uz valstīm, kas uzskaitītas sekojošajā tabulā.


| Valsts/reģions        | Papildinformācija                                                          |
|----------------|---------------------------------------------------------------------------------|
| Austrija        |  [Austrijas PVN pārskata detaļas](emea-aut-vat-statement-details.md)         |
| Beļģija        |                                                                                 |
| Čehijas Republika |  [PVN pārskata detaļas Čehijā](emea-cze-vat-statement-details.md)   |
| Igaunija        |  [PVN pārskata detaļas par Igauniju](emea-est-vat-statement-details.md) |
| Somija        |                                                                                 |
| Vācija        |                                                                                 |
| Itālija          | [PVN pārskata detaļas, Itālija](emea-ita-vat-statements-details.md)            |
| Latvija         | [PVN pārskata detaļas Latvija](emea-lva-vat-statement-details.md)           |
| Lietuva      | [PVN pārskata detaļas Lietuvā](emea-ltu-vat-statement-details.md)         |
| Nīderlande    |                                                                                 |
| Zviedrija         |                                                                                 |




