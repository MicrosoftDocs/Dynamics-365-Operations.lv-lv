---
title: Atbalstīt ER datu modeļu parametru izsaukumus
description: Šajā tēmā skaidrots, kā ieviest elektronisko pārskatu (ER) datu modeļu parametru izsaukumus.
author: NickSelin
ms.date: 03/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula, ERDataModelDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 968b0769607e9fdbed57c25b727ed44988a92913
ms.sourcegitcommit: 399d0d3f8e2ebb81b6b9d640365ebe182690bab2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/15/2022
ms.locfileid: "8419515"
---
# <a name="support-parameterized-calls-of-er-data-models"></a>Atbalstīt ER datu modeļu parametru izsaukumus

[!include [banner](../includes/banner.md)]

Lai ģenerētu biznesa dokumentus, jūs konfigurējat Elektronisko [pārskatu (ER) risinājumu](general-electronic-reporting.md), kas satur šādus ER komponentus:

- **[Formāts](er-overview-components.md#format-component)** – šis komponents nosaka biznesa dokumenta struktūru.
- **Formāta kartēšana** – šis komponents kontrolē, kā izpildlaikā tiek aizpildīts biznesa dokuments.
- **[Modeļa kartēšana](er-overview-components.md#model-mapping-component)** - šis komponents norāda, ko dati no programmas izvelk no formāta kartēšanas.
- **[Datu modelis](er-overview-components.md#data-model-component)** – šis komponents atbilst informācijai starp atsevišķiem komponentiem.

Palaižot ER formātu, tiek palaists katrs formāta elements, sākot no saknes formāta elementa. Ja formāta elements, kas tiek izpildīts, ietver saistījumu ar datu avotu, datu avots tiek palaists, lai piegādātu paredzamos datus un izmantotu tos [formāta](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents) elementa aizpildīšanai. Izsaucot modeļa tipa datu *avotu*, tiek izsaukta atbilstoša modeļa kartēšana, lai vilktu datus no programmas, balstoties uz modeļu kartēšanas iestatījumiem.

Iepriekš šos modeļa kartēšanas izsaukumus nevarēja iestatīt parametrā, lai padarītu tos atkarīgus no palaistā formāta loģikas. Tika atbalstīta tikai šāda datu plūsma.

<table>
<tbody>
<tr align="center">
<td>
<b>Formāts</b><br>
Formatelement (Formatelement&nbsp;)<br>
&nbsp;
</td>
<td>
<i>Saistīšana</i><br>
&gt;&nbsp; Pieprasījumu&nbsp;&gt;<br>
&lt;&nbsp;vērtība&nbsp;&lt;
</td>
<td><b>Formāta&nbsp; maiņa</b><br>
Datu avots<br>
&nbsp;
</td>
<td>
<i>Datamodel&nbsp;</i><br>
&gt;&nbsp; Pieprasījumu&nbsp;&gt;<br>
&lt;&nbsp;vērtība&nbsp;&lt;
</td>
<td>
<b>Modeļa&nbsp; izlaišana</b><br>
Datu&nbsp; avots<br>
&nbsp;
</td>
<td>
<i>Saistīšana</i><br>
&gt;&nbsp; Pieprasījumu&nbsp;&gt;<br>
&lt;&nbsp;vērtība&nbsp;&lt;
</td>
<td>
<b>Tabula</b><br>
Reģistrēt<br>
Lauks
</td>
</tr>
</tbody>
</table>

Taču versijā 10.0.15 un jaunākā versijā jūs varat konfigurēt datu modeļa laukus, kurus var izsaukt tikai tad, ja ir nodrošinātas konfigurēto parametru vērtības. Ja šāds lauks ir konfigurēts un izsaukts no formāta komponenta, ir jānodrošina nepieciešamie parametri formātā, kas ir saistoši kā izsaukuma argumenti. Šādos gadījumos argumentu vērtības var norādīt, pamatojoties uz formātam raksturīgām vērtībām. Tāpēc jūs varat izmantot dinamiskā izpildlaika **parametrizāciju** datu modeļa izsaukumi, lai atbalstītu sekojošo datu plūsmu.

<table>
<tbody>
<tr align="center">
<td>
<b>Formāts</b><br>
Formatelement1 (formatelement1&nbsp;&nbsp;)<br>
<br>
Formatelement2&nbsp;&nbsp;<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Saistīšana</i><br>
&gt;&nbsp; pieprasījums Nr.&nbsp; 1&nbsp;&gt;<br>
&lt;&nbsp; vērtība&nbsp; 1&nbsp;&lt;<br>
&gt;&nbsp; pieprasījums Nr.&nbsp; 2&nbsp;&gt;<br>
&lt;&nbsp; vērtība&nbsp; 3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Formatmapping&nbsp;</b><br>
Datu&nbsp; avots1&nbsp;<br>
&nbsp;<br>
<b>value2=Kolonnu(value1)</b><br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Datamodel&nbsp;</i><br>
&gt;&nbsp; Lauka Nr. 1&nbsp;&gt;<br>
&lt;&nbsp; vērtība&nbsp; 1&nbsp;&lt;<br>
<b>&gt;&nbsp; field2(value2)&nbsp;&gt;</b><br>
&lt;&nbsp; vērtība&nbsp; 3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Modeļa&nbsp; izlaišana</b><br>
Datu&nbsp; avots1&nbsp;<br>
<br>
Datu&nbsp; avots2&nbsp;<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Saistīšana</i><br>
&gt;&nbsp; pieprasījums Nr.&nbsp; 1&nbsp;&gt;<br>
&lt;&nbsp; vērtība&nbsp; 1&nbsp;&lt;<br>
&gt;&nbsp; pieprasījums Nr.&nbsp; 2&nbsp;&gt;<br>
&lt;&nbsp; vērtība&nbsp; 3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Table1&nbsp;</b><br>
Ieraksts Nr.&nbsp; 1<br>
Lauks Nr.&nbsp; 1<br>
<b>Table2&nbsp;</b><br>
Ieraksts Nr.&nbsp; 2<br>
Lauks Nr.&nbsp; 2
</td>
</tr>
</tbody>
</table>

Jaunā funkcionalitāte ļauj parametrizēt izsaukumu uz jebkuru datu modeļa lauku, kas [*ir ieraksta*](er-formula-supported-data-types-composite.md#record) vai [*ieraksta saraksta*](er-formula-supported-data-types-composite.md#record-list) tipa. Datu modeļa lauka parametriem tiek atbalstīti šādi datu tipi:

- [Būla](er-formula-supported-data-types-primitive.md#boolean)
- [Konteiners](er-formula-supported-data-types-composite.md#container)
- [Datums](er-formula-supported-data-types-primitive.md#date)
- [Datums un laiks](er-formula-supported-data-types-primitive.md#datetime)
- [GUID](er-formula-supported-data-types-primitive.md#guid)
- [Int64](er-formula-supported-data-types-primitive.md#int64)
- [Vesels skaitlis](er-formula-supported-data-types-primitive.md#integer)
- [Reāls](er-formula-supported-data-types-primitive.md#real)
- [Virkne](er-formula-supported-data-types-primitive.md#string)

Varat norādīt katru parametru datu modeļa laukam, kuram argumentu [*var norādīt kā noteiktu datu tipa vienu vērtību un šādu*](er-formula-supported-data-types-composite.md#record-list) vērtību sarakstu.

> [!NOTE]
> Datu modeļa lauka parametra noklusējuma vērtība netiek atbalstīta. Ja datu modelī laukā pievienojat parametru un šī datu modeļa versija jau ir nodota un publicēta, [ir](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) atkārtoti jāveic visu atbilstošo modeļa kartējumu un formātu bāze jaunajai šī modeļa versijai, jo šī datu modeļa izmaiņa nav atpakaļ saderīga.

Parametru datu modeļa laukus var konfigurēt, lai veiktu modeļa kartēšanas izsaukumus formātam raksturīgus. Šī pieeja var palīdzēt samazināt modeļa kartēšanas skaitu, kas jākonfigurē daudziem viena datu modeļa formātiem. Šo pieeju iespējams arī izmantot, lai uzlabotu savu formātu izpildes veiktspēju un samazinātu laiku, kas nepieciešams biznesa dokumentu ģenerēšanai. Lai iegūtu papildinformāciju par šo līdzekli, aizpildiet šajā tēmā sniegto piemēru.

## <a name="example-use-parameterized-calls-of-er-data-models"></a>Piemērs: izmantojiet ER datu modeļu parametru izsaukumus

Turpmākie soļi skaidro veidu, kā lietotājs sistēmas administratora vai elektronisko pārskatu izstrādātāja lomā var projektēt ER risinājumu, kas satur datu modeli, modeļu kartēšanu un formāta ER komponentu, kas ir konfigurēts, lai izsauktu modeļa kartēšanu no formāta, sniedzot argumentu izsaukumam, kura vērtība ir aprēķināta izpildlaikā, izmantojot izpildlaika formulu. 

Šīs darbības var veikt uzņēmumā **DEMF**. Koda modifikācijas nav nepieciešamas. 

Šajā piemērā izveidojat nepieciešamās ER konfigurācijas [uzņēmumam](general-electronic-reporting.md#Configuration)**Litware, Inc.** sample. Pārliecinieties, vai **Litware, Inc.** (`http://www.litware.com`) parauga uzņēmuma konfigurācijas nodrošinātājs ir norādīts ER struktūrā un vai tas ir atzīmēts kā **aktīvs**. Ja šī konfigurācijas nodrošinātāja nav **uzskaitīts** vai arī tas nav atzīmēts kā aktīvs, [izpildiet darbības, kas norādītas Sadaļā Konfigurācijas nodrošinātāja izveide un atzīmējiet to kā aktīvu](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="business-scenario"></a>Biznesa scenārijs

Jums ir ER risinājums, kas ietver formātu, ko varat palaist, lai audita nolūkos ģenerētu elektronisku dokumentu. Šis formāts satur nodokļu darbības, kas saistītas ar pārdošanas pasūtījumiem un pirkšanas pasūtījumiem, un kam ir nepieciešama informācija, piemēram, darbības datums un nodokļa vērtība. Jaunajā finanšu gadā šī dokumenta struktūra ir mainījusies. Tagad jums jāiesniedz paplašināts dokuments, kas ietver papildu detaļas (nosaukumus) visām pusēm (debitoriem un kreditoriem), kuru darbības tiek uzrādītas ģenerētos pārskatos. Tādēļ ir jāmodificē ER risinājums tā, lai tas ģenerētu dokumentus, kas atbilst šai jaunajai prasībai.

### <a name="configure-the-er-framework"></a>ER struktūras konfigurēšana

Izpildiet sadaļā [ER struktūras konfigurēšana](er-quick-start2-customize-report.md#ConfigureFramework) norādītās darbības, lai iestatītu ER parametru minimālo kopu. Šis iestatījums ir jāpabeidz, pirms sākat lietot ER struktūru jauna ER risinājuma izstrādei.

### <a name="design-a-domain-specific-data-model"></a>Domēnam specifiska datu modeļa izveide

Ir jāizveido jauna ER konfigurācija, kas satur nepieciešamo datu modeļa komponentu. Šis datu modelis tiks izmantots kā datu avots vēlāk, kad izveidosiet ER formātu, lai ģenerētu audita pārskatu.

Izpildiet šīs darbības, lai importētu nepieciešamo datu modeli no Microsoft nodrošinātā XML faila.

1. Lejupielādējiet [parauga audit model.version.1.xml](https://download.microsoft.com/download/7/1/9/719b0132-fed7-4c73-8afa-90cac29c2fee/Sample-audit-model.version.1.xml) failu un saglabājiet to lokālajā datorā.
2. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
3. Darbvietā **Elektroniskie pārskati** atlasiet **Pārskatu veidošanas konfigurācijas**.
4. **Konfigurācijas lapā Darbību** rūtī atlasiet Maiņas **noslodze** \> **no XML faila.**
5. Atlasiet **Pārlūkot**, pēc tam atrodiet un atlasiet failu **Parauga audita model.version.1.xml**.
6. Atlasiet **Labi**, lai importētu konfigurāciju.

    ![Importētā ER datu modeļa konfigurācija konfigurāciju lapā.](./media/er-data-model-parameterized-calls-imported-model.png)

Šajā attēlā parādīta konfigurētā datu modeļa rediģējamā versija datu modeļu **veidotāja** lapā.

![ER datu modeļa struktūra datu modeļu veidotāja lapā.](./media/er-data-model-parameterized-calls-model1.png)

Pašreiz modelis paredzēts tikai nodokļu darbībām, kurām ir nepieciešamā informācija.

### <a name="design-a-model-mapping-for-the-configured-data-model"></a>Konfigurētā datu modeļa kartēšanas izveidošana

Kā lietotājam elektronisko pārskatu izstrādātāja lomā jāizveido jauna ER konfigurācija, kas ietver modeļa kartēšanas komponentu audita datu modeļa paraugs. Šis komponents ievieš konfigurēto datu modeli korporācijai Microsoft un Dynamics 365 Finance ir specifisks šai programmai. Ir jākonfigurē modeļa kartēšanas komponents, lai norādītu programmas objektus, kas jāizmanto, lai aizpildītu konfigurēto datu modeli ar programmas datiem izpildlaikā. Lai pabeigtu šo uzdevumu, jums ir jāsaprot, kā nodokļu biznesa domēna datu struktūra tiek īstenota Finansēs.

Izpildiet šīs darbības, lai importētu nepieciešamo modeļa kartēšanu no Microsoft nodrošinātā XML faila.

1. Lejupielādējiet [parauga audita modeļa kartējumu.version.1.1.xml](https://download.microsoft.com/download/c/0/3/c03a4673-b1b1-4ef8-96d0-bf96518be6e0/Sample-audit-model-mapping.version.1.1.xml) failu un saglabājiet to lokālajā datorā.
2. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
3. Darbvietā **Elektroniskie pārskati** atlasiet **Pārskatu veidošanas konfigurācijas**.
4. **Konfigurācijas lapā Darbību** rūtī atlasiet Maiņas **noslodze** \> **no XML faila.**
5. Atlasiet **Pārlūkot**, pēc tam atrodiet un atlasiet failu **Parauga audita modeļa kartēšana.version.1.1.xml**.
6. Atlasiet **Labi**, lai importētu konfigurāciju.

    ![Importētā ER modeļa kartēšanas konfigurācija konfigurāciju lapā.](./media/er-data-model-parameterized-calls-imported-mapping.png)

Šajā ilustrācijā parādīta konfigurētā modeļa kartēšanas rediģējamā versija modeļu kartēšanas **veidotāja** lapā.

![ER modeļa kartēšanas struktūra modeļu kartēšanas veidotāja lapā.](./media/er-data-model-parameterized-calls-mapping1.png)

Pašlaik modeļa kartēšana ir veidota, lai atklātu nodokļu darbības, kam ir nepieciešamā informācija. Tā iāk šo informāciju no programmas `TaxTrans` tabulas, izmantojot konfigurētos un `TaxTrans``TaxTransFiltered` ER datu avotus.

### <a name="design-a-new-format"></a>Veidot jaunu formātu

Kā lietotājs Elektroniskās ziņošanas funkcionālā konsultanta lomā jums ir jāizveido jauna ER konfigurācija, kas ietver formāta komponentu. Ir jākonfigurē formāta komponents, lai aizpildītu ģenerētos pārskatus ar nodokļu darbībām, kam ir visas nepieciešamās detaļas.

Izpildiet šīs darbības, lai importētu nepieciešamo formātu no Microsoft nodrošinātā XML faila.

1. Lejupielādējiet [parauga audita format.version.1.1.xml](https://download.microsoft.com/download/e/b/7/eb7e126e-2bb3-4bbb-a735-ffd4c48920b1/Sample-audit-format.version.1.1.xml) failu un saglabājiet to lokālajā datorā.
2. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
3. Darbvietā **Elektroniskie pārskati** atlasiet **Pārskatu veidošanas konfigurācijas**.
4. **Konfigurācijas lapā Darbību** rūtī atlasiet Maiņas **noslodze** \> **no XML faila.**
5. Atlasiet **Pārlūkot**, pēc tam atrodiet un atlasiet failu **Parauga audita formāts.version.1.1.xml**.
6. Atlasiet **Labi**, lai importētu konfigurāciju.

    ![Importēt ER formāta konfigurāciju lapā Konfigurācijas.](./media/er-data-model-parameterized-calls-imported-format.png)

Šajā ilustrācijā parādīta konfigurētā formāta rediģējamā versija formāta veidotāja **lapā**.

![ER formāta struktūra formāta veidotāja lapā.](./media/er-data-model-parameterized-calls-format1.png)

ER formāts ir konfigurēts, lai izveidotu pārskatu kā teksta failu komatatdalīto vērtību (CSV) formātā.

### <a name="run-the-imported-format"></a>Importētā formāta palaišana

1. **Lapā Konfigurācijas atlasiet** parauga **audita formāta** konfigurāciju un pēc tam darbību rūtī atlasiet **Palaist**.
2. Dialoglodziņā Elektroniskā **pārskata parametri** cilnē Iekļauja **ietvertie ieraksti** atlasiet **Filtrēt**.
3. Norādiet nosacījumus, lai atlasītu **PIV-110000004** **un INV-10000001** nodokļu darbības.
4. Atlasiet **Labi**.
5. Atlasiet **Labi**.
6. Pārskatiet ģenerēto dokumentu, kas ietver atlasīto dokumentu nodokļu darbības.

    ![Ģenerētā dokumenta ar nodokļu darbībām priekšskatījums.](./media/er-data-model-parameterized-calls-output1.png)

### <a name="adjust-the-imported-er-solution"></a>Pielāgot importēto ER risinājumu

Atbilstoši jaunajai prasībai dokumentam, kas jāiesniedz, jāsatur debitoru un kreditoru nosaukumi, kuru darbības ir iekļautas. Tādējādi jums ir jāpārveidojiet importētais ER risinājums tā, lai tas ģenerētu dokumentu, kas atbilst šai jaunajai prasībai.

Izlemiet, kā vēlaties ieviest importēto ER komponentu nepieciešamās modifikācijas.

Šāda pieeja ir šādu modifikāciju implementēšanu implementēšanu:

- Datu modelī pievienojiet Virknes `Transaction.Party.Name` tipa jaunā datu *modeļa* lauku.
- Modeļa kartēšanā konfigurējiet `DirPartyTable` saistīšanu jaunajam datu modeļa laukam, izmantojot pieejamās tabulu relācijas, `Name` lai piekļūtu programmas tabulas atbilstošajam ierakstam un iegūtu no tās lauka vērtību.

Kaut arī šī pieeja darbosies, tā var radīt veiktspējas problēmas SQL datu bāzē, `TaxTrans` jo tā ir darījumu tabula un tādējādi var saturēt lielu ierakstu apjomu. Šajā gadījumā zvanu skaitam jābūt vienādam `DirPartyTable` ar ierakstu skaitu tabulā, kas var `TaxTrans` izraisīt veiktspējas problēmas.

Alternatīvi jūs varat ieviest šādas modifikācijas:

- Datu modelī pievienojiet jauno sakni `Party` un jauno `Party.Name` lauku.
- Modeļa kartēšanā pievienojiet jaunu datu avotu, kas savienos visus tabulas ierakstus, kas tiek lietoti tabulu relācijās, `DirPartyTable` lai piekļūtu programmas tabulas atbilstošajam ierakstam, sākot no tabulas`TaxTrans`.

Kaut arī šī pieeja darbosies, tā var izraisīt atmiņas patēriņa problēmas. Pat ja jauns [JOIN](er-join-data-sources.md) datu avots darbojas kā viens SQL pieprasījums programmas datu bāzei, lai novērstu datu bāzes veiktspējas problēmas, rezultāts ir jāņem uz programmas servera atmiņas vietu. Ierakstu skaits un lauku skaits šajos ierakstos būs ļoti liela, šī pieeja var radīt ļoti lielu atmiņas patēriņu. Iespējams, ir pat atmiņas kļūdanības izpildlaika izņēmums.

Modifikācijas var ieviest, izpildot formātu, atmiņā apkopojot unikālos debitoru un kreditoru identifikācijas kodus visām nodokļu darbībām, kas tiks iesniegtas ģenerētajā pārskatā. Tā kā ir jāsaglabā tikai unikāli kodi, beidzamā kodu kopa nebūs pietiekami liela, lai ietekmētu atmiņas patēriņu. Pēc tam kodu kopa tiks nodota modeļa kartēšanai kā arguments citam datu avota izsaukšanai no modeļa *tipa*. Pamatojoties uz šo izsaukumu, modeļa kartēšana izpildīs jaunu ER datu avotu, kas veido vienu SQL pieprasījumu programmas datu bāzei, `DirPartyTable` lai no tabulas ienestu ierakstus tikai tām pusēm, kuru kodi ir norādīti izveidotajā kodu kopā.

### <a name="adjust-the-imported-data-model"></a>Pielāgot importēto datu modeli

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. **Konfigurācijas lapas konfigurāciju** kokā kreisās puses rūtī atlasiet Parauga **audita modelis**.
3. Kopsavilkuma cilnē **Versijas** atlasiet versiju **2**, kuras statuss ir Melnraksts **[...](general-electronic-reporting.md#component-versioning)**.
4. Atlasiet kopsavilkuma cilni **Konfigurācijas komponenti**.
5. Atlasiet **Veidotājs**, lai atvērtu datu modeli labošanai.
6. Datu modeļa **lapā pārliecinieties**, ka lauks ir `Root` atlasīts, un pēc tam atlasiet **Jauns**.
7. Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības.

    1. **Lauka grupā Jauns zars** kā atlasiet aktīvā **zara atvasināto** opciju.
    2. Laukā **Nosaukums** ievadiet **Puse**.
    3. Laukā **Vienuma veids** atlasiet **Ierakstu saraksts**.
    4. Atlasiet **Pievienot,** lai pabeigtu jauna lauka pievienošanu.

8. Pārliecinieties, ka `Root.Party` lauks ir atlasīts, un pēc tam cilnē **Mezgls** atlasiet **Parametri**.
9. **Dialoglodziņā Parametri** izpildiet šādas darbības:

    1. **Cilnē Parametri** atlasiet **Jauns**.
    2. Laukā **Nosaukums ievadiet** PartyRefRecId **·**.
    3. Laukā **Tips** atlasiet **Int64**.
    4. Atzīmējiet **izvēles** rūtiņu Saraksts.
    5. Atlasiet **Labi,** lai pabeigtu parametru ievadi.

    > [!NOTE]
    > Jūs tikko konfigurējat datu `Root.Party` modeļa lauku kā lauku, **kas tiek izsaukts, kad parametrā PartyRefRecId ir sniegta** vērtība. Šai vērtībai ir jābūt to ierakstu sarakstā, kas ietver datu `Value` tipa *Int64* lauku.

    ![Parametru dialoglodziņš.](./media/er-data-model-parameterized-calls-model2a.png)

10. Pārliecinieties, ka lauks `Root.Party` joprojām ir atlasīts, un pēc tam atlasiet **Jauns**.
11. Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības.

    1. **Lauka grupā Jauns zars** kā atlasiet aktīvā **zara atvasināto** opciju.
    2. Laukā **Nosaukums** ievadiet **nosaukumu**.
    3. Laukā **Vienuma veids** atlasiet **Virkne**.
    4. Atlasiet **Pievienot,** lai pabeigtu jauna lauka pievienošanu.

12. Atlasiet **Saglabāt** un aizveriet datu **modeļa** lapu.

    ![Pielāgotā ER datu modeļa struktūra datu modeļu veidotāja lapā.](./media/er-data-model-parameterized-calls-model2b.png)

13. Kopsavilkuma cilnē **Versijas** 2 **atlasiet** Mainīt **statusu** \> **Pabeigts.** Pēc tam atlasiet **Labi**.

    > [!NOTE]
    > Datu modeļa izmaiņas tiek saglabātas **parauga audita modeļa datu modeļa komponenta otrajā pārskatījumā, kas atrodas parauga audita** **modeļa** ER konfigurācijas otrajā versijā.

![Atjaunināta ER datu modeļa konfigurācija konfigurāciju lapā.](./media/er-data-model-parameterized-calls-updated-model.png)

### <a name="adjust-the-imported-model-mapping"></a>Pielāgot importēto modeļa kartējumu

1. **Lapā Konfigurācijas konfigurāciju** koka kreisajā rūtī izvērsiet **parauga audita modeli**.
2. Atlasiet **audita modeļa** **kartējuma** paraugs un pēc tam kopsavilkuma cilnē Versijas atlasiet otro kartēšanas versiju, kas ir balstīta uz pirmo datu modeļa versiju (**versija 1.2**) un kuras statuss ir Melnraksts.**·**
3. Atlasiet **Pārskatīt**.
4. Laukā **Mērķa versija** atstājiet parauga audita **modeļa bāzes modeļa** versiju **2**.
5. Atlasiet **Labi,** lai pārkārtotu un līdzinātu modeļa kartēšanu ar pēdējām datu modeļa izmaiņām.

    Ievērojiet, **ka rediģējamā modeļa kartēšanas versijas numurs ir mainījies no 1.2** **uz 2.2**, lai norādītu, ka otrā modeļa versija pašlaik tiek izmantota kā bāze.

6. Atlasiet **Noformētājs**.
7. Lapā Modelis **uz datu avota kartēšanu** atlasiet Veidotājs **pašreizējā** modeļa kartēšanai.
8. Lai piekļūtu programmas tabulai, rīkojieties šādi, lai pievienotu jaunu `DirPartyTable` datu avotu:

    1. **Datu avota tipa rūtī** atlasiet Tabulas **Dynamics 365 for Operations\> ieraksti**.
    2. Atlasiet **Pievienot sakni** rūtī **Datu avoti**.
    3. Laukā **Nosaukums ievadiet** PartyTable **·**.
    4. Laukā **Tabula ievadiet** DirPartyTable **·**.
    5. Atlasiet **Labi,** lai pabeigtu jauna datu avota pievienošanu.

9. Veiciet šīs darbības, lai pievienotu jaunu datu avotu ierakstu pieprasījumu `DirPartyTable`, balstoties uz sniegto ierakstu identifikācijas kodu sarakstu:

    1. Datu avota **tipa rūtī atlasiet** Vispārējs tukšs **konteiners \>**.
    2. Atlasiet **Pievienot sakni** rūtī **Datu avoti**.
    3. Laukā **Nosaukums** ievadiet **Datus**.
    4. Atlasiet **Labi,** lai pabeigtu jauna datu avota pievienošanu.
    5. **Datu avotu** rūtī atlasiet datu **datu** avotu.
    6. Datu avota **tipa rūtī** atlasiet funkcijas aprēķināto **\> lauku**.
    7. **Datu avotu rūtī** atlasiet **Pievienot**.
    8. Laukā **Nosaukums ievadiet** DirParty **·**.
    9. Atlasiet **Rediģēt formulu**.
    10. Formulas **veidotāja** lapā atlasiet **Parametri**.
    11. **Dialoglodziņā Parametri** izpildiet šādas darbības:

        1. **Cilnē Parametri** atlasiet **Jauns**.
        2. Laukā **Nosaukums ievadiet** DirPartyId **·**.
        3. Laukā **Tips** atlasiet **Int64**.
        4. Atzīmējiet **izvēles** rūtiņu Saraksts.
        5. Atlasiet **Labi**.

        > [!NOTE]
        > Jūs tikko konfigurējat šo aprēķināto lauku, lai izpildlaikā tas akceptētu viena parametra, kas ir konfigurēts kā ierakstu saraksts, kuram ir viens Int64`Value` tipa lauks, *arguments*.

    12. Laukā **Formula** ievadiet šādu izteiksmi:

        `FILTER(PartyTable, VALUEINLARGE(PartyTable.RecId, DirPartyId, DirPartyId.Value))`

        > [!NOTE]
        > Aprēķinātais lauks ir tikko `DirParty``DirPartyTable``DirPartyId` konfigurēts, lai ienestu tikai tos ierakstus, kuru ierakstu identifikācijas kodi ir iekļauti sarakstā, kas tiek sniegts kā arguments `DirParty` lauka piesaukšanās laikā.

        ![Formula, lai ienestu pušu nosaukumus no programmas tabulas formulas veidotāja lapā.](./media/er-data-model-parameterized-calls-formula1.png)

    13. Atlasiet **Saglabāt** un aizvēriet lapu **Formulas veidotājs** .
    14. Atlasiet **Saglabāt** un pēc tam atlasiet Labi, **lai** pabeigtu jauna datu avota pievienošanu.

10. Sekojiet šiem soļiem, lai saistītu jauno datu avotu ar jaunu datu modeļa lauku tā, lai datu modelis tiek izmantots pušu nosaukumu piekļuvei:

    1. **Datu modeļa rūtī** atlasiet datu `Root.Party` modeļa lauku.
    2. Atlasiet **Rediģēt** rūtī **Datu modelis**.
    3. Formulas **veidotāja** lapas formulas **laukā** ievadiet izteiksmi `Data.DirParty(PartyRefRecId)`.
    4. Atlasiet **Saglabāt** un aizvēriet lapu **Formulas veidotājs** .

        > [!NOTE]
        > Jūs tikko konfigurējāt saistīšanu `Data.DirParty``Root.Party`, lai izsauktu konfigurēto datu avotu un sniegtu ierakstu identifikācijas kodu sarakstu, kas tiks norādīts formātā, kad datu modeļa lauks tiek izsaukts.

    5. **Datu modeļa rūtī** atlasiet datu `Root.Party.Name` modeļa lauku.
    6. Atlasiet **Rediģēt** rūtī **Datu modelis**.
    7. Formulas **veidotāja** lapas datu avota **rūtī** izvērsiet Data **\> DirParty** un atlasiet **Nosaukums**.
    8. Atlasiet **Pievienot datu avotu**.
    9. Atlasiet **Saglabāt** un aizvēriet lapu **Formulas veidotājs** .

    ![Pielāgotās ER modeļa kartēšanas struktūra modeļu kartēšanas veidotāja lapā.](./media/er-data-model-parameterized-calls-mapping2.png)

11. Atlasiet **Saglabāt un** aizvērt modeļu kartēšanas **veidotāja** lapu.
12. Aizveriet lapu **Datu avota kartējuma modelis**.
13. Kopsavilkuma cilnē **Versijas** 2.2 **atlasiet** Mainīt **statusu \> Pabeigts**. Pēc tam atlasiet **Labi**.

### <a name="adjust-the-imported-format"></a>Pielāgot importēto formātu

1. **Lapā Konfigurācijas atlasiet** audita **parauga formātu**.
2. Kopsavilkuma cilnē **Versijas** atlasiet versiju **1.2**, kuras statuss ir **Melnraksts**.
3. Atlasiet **Pārskatīt**.
4. Laukā **Mērķa versija** atstājiet parauga audita **modeļa bāzes modeļa** versiju **2**.
5. Atlasiet **Ok,** lai pārkārtotu un līdzinātu savu formātu ar pēdējām datu modeļa izmaiņām.
6. Atlasiet **Noformētājs**.
7. Formāta veidotāja **lapas** formāta struktūras kokā kreisajā rūtī atlasiet Izvērst **/sakļaut**.
8. Sekojiet šiem soļiem, lai pievienotu jaunu formāta elementu, lai apkopotu ierakstu identifikācijas kodus pusēm, kuru darbības tiek iesniegtas ģenerētos pārskatos.

    1. Formāta struktūras kokā atlasiet Report.Row.Trans **secības** elementu.
    2. Atlasiet **Pievienot**.
    3. **Dialoglodziņā Pievienot** atlasiet Datu **avota \> krājums**.
    4. **Dialoglodziņa Komponenta rekvizīti** laukā Nosaukums **ievadiet** **ID**.
    5. Laukā **Datu tips atlasiet** Int64 **·**.
    6. Atlasiet **Labi**.

    > [!NOTE]
    > Datu **avota krājuma \>** elementu var izmantot, lai veiktu iekšējos aprēķinus un datu pārvēršanu tikai darbojošās formāta darbības jomā. Tādēļ, pievienojot šo formāta elementu, jūs nemaināt ģenerētā dokumenta saturu.

9. Izpildiet šos soļus, lai pievienotu jaunus formāta elementus, lai ievadītu pušu nosaukumus ģenerētos pārskatos:

    1. Atlasiet Report.Row **secības** elementu.
    2. Atlasiet **Pievienot**.
    3. **Dialoglodziņā Pievienot** atlasiet Teksta **\> secība**.
    4. **Dialoglodziņa Komponenta rekvizīti** laukā Nosaukums **ievadiet** **Puse**.
    5. Atlasiet **Labi**.
    6. Atlasiet Report.Row.Party **secības** elementu.
    7. Atlasiet **Pievienot**.
    8. **Dialoglodziņā Pievienot** atlasiet Teksta **\> virkne**.
    9. Dialoglodziņa Komponenta **rekvizīti laukā Nosaukums** ievadiet **Nosaukums** **.**
    10. Atlasiet **Labi**.

10. Sekojiet šiem soļiem, lai pievienotu jaunu datu avotu, lai apkopotu ierakstu identifikācijas kodus pusēm, kuru darbības tiek iesniegtas ģenerētos pārskatos:

    1. Cilnē Kartēšana **atlasiet** Pievienot **sakni**.
    2. Dialoglodziņā Pievienot **datu avotu** atlasiet Funkciju datu **\> apkopojums**.
    3. Datu apkopošanas **datu avota rekvizītu** dialoglodziņa laukā Nosaukums **ievadiet** **PartyIds**.
    4. Laukā **Krājuma tips atlasiet** Int64 **·**.
    5. Atlasiet **Labi**.

11. Sekojiet šiem soļiem, lai pievienotu jaunu saistīšanu un apkopotu to pušu ierakstu identifikācijas kodus, kuru darbības ir iesniegtas ģenerētos pārskatos:

    1. Formāta struktūras kokā atlasiet datu **Report.Row.Trans.Id** elementu.
    2. Atlasiet **Rediģēt formulu**.
    3. Formulas **veidotāja** lapā ievadiet izteiksmi `PartyIds.Collect(model.Transaction.Party.RecId)`.
    4. Atlasiet **Saglabāt** un aizvēriet lapu **Formulas veidotājs** .

12. Izpildiet šos soļus, lai pievienotu jaunus saistījumus, lai ievadītu pušu nosaukumus ģenerētos pārskatos:

    1. Formāta struktūras kokā atlasiet Report.Party **secības** elementu.
    2. Atlasiet **Rediģēt formulu**.
    3. Formulas **veidotāja** lapā ievadiet izteiksmi `model.Party(PartyIds.Result)`.
    4. Atlasiet **Saglabāt** un aizvēriet lapu **Formulas veidotājs** .
    5. Formāta struktūras kokā atlasiet elementu **Report.Party.Name** kārtas elementu.
    6. **Cilnē Kartēšana** atlasiet datu `model.Party.Name` modeļa lauku.
    7. Atlasiet **Saistīt**.

    ![Pielāgotā ER formāta struktūra formāta veidotāja lapā.](./media/er-data-model-parameterized-calls-format2.png)

13. Atlasiet **Saglabāt** un aizvērt formāta veidotāja **lapu**.
14. Aizveriet lapu **Datu avota kartējuma modelis**.
15. Kopsavilkuma cilnē **Versijas** 2.2 **atlasiet** Mainīt **statusu** \> **Pabeigts.** Pēc tam atlasiet **Labi**.

### <a name="run-the-adjusted-format"></a>Palaist pielāgoto formātu

1. **Lapā Konfigurācijas atlasiet** parauga **audita formātu** un pēc tam darbību rūtī atlasiet **Palaist**.
2. Dialoglodziņā Elektroniskā **pārskata parametri** cilnē Iekļauja **ietvertie ieraksti** atlasiet **Filtrēt**.
3. Norādiet nosacījumus, lai atlasītu **PIV-110000004** un **INV-10000001** dokumentus.
4. Atlasiet **Labi**.
5. Atlasiet **Labi**.
6. Pārskatiet ģenerēto dokumentu, kas ietver atlasīto dokumentu nodokļu darbības, un atbilstošā debitora un kreditora nosaukumus.

    ![Ģenerētā dokumenta priekšskatījums ar nodokļu darbībām un pušu nosaukumiem.](./media/er-data-model-parameterized-calls-output2.png)

7. Dodieties **uz Kreditoru** \> **kreditoriem** \> **visiem kreditoriem** un **pārskatiet atlasītā PIV-110000004** detalizētu informāciju, ieskaitot kreditora nosaukumu.

    ![Pārskatiet pirkšanas dokumenta informāciju par visiem kreditoriem un Rēķinu žurnāla lapām.](./media/er-data-model-parameterized-calls-review1.gif)

8. Dodieties **uz Debitoru** \> **parādiem** \> **Debitori** visi debitori **un pārskatiet atlasītā INV-10000001** dokumenta detaļas, ieskaitot debitora vārdu.

    ![Pārskata pārdošanas dokumenta informāciju par visiem debitoriem un grāmatotā PVN lapām.](./media/er-data-model-parameterized-calls-review2.gif)

Lai iegūtu sīkāku informāciju par šo ER risinājuma izpildi, izmantojiet ER iebūvēto veiktspējas [izsekošanas](trace-execution-er-troubleshoot-perf.md) parsētāju.

## <a name="additional-resources"></a>Papildu resursi

- [Atbalsta Aprēķināto lauka tipa ER datu avotu parametru izsaukumus.](er-calculated-field-type.md)
- [Elektronisko atskaišu veidošanas (ER) formāta failu izpildes uzraudzīšana, lai novērstu veiktspējas problēmas](trace-execution-er-troubleshoot-perf.md)
- [DATU APKOPOŠANAS datu avotu izmantošana Elektronisko pārskatu formātos](er-data-collection-data-sources.md)
- [ValueInLarge ER funkcija](er-functions-logical-valueinlarge.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
