---
title: Konfigurēto ER komponentu pārbaude, lai novērstu izpildlaika problēmas
description: Šajā tēmā paskaidrots, kā pārbaudīt konfigurētos Elektronisko pārskatu (ER) komponentus, lai novērstu izpildlaika problēmas, kas varētu rasties.
author: NickSelin
manager: AnnBe
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86db6dc27a8a76e90494e3dc7a7cc9c828f9ec37
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574129"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a>Konfigurēto ER komponentu pārbaude, lai novērstu izpildlaika problēmas

[!include[banner](../includes/banner.md)]

Katru konfigurēto [Elektroniskā pārskata (ER)](general-electronic-reporting.md) [formāta](general-electronic-reporting.md#FormatComponentOutbound) un [modeļa kartēšanas](general-electronic-reporting.md#data-model-and-model-mapping-components) komponentu var [validēt](er-fillable-excel.md#validate-an-er-format) izstrādes laikā. Šīs validācijas laikā tiek veikta konsekvences pārbaude, lai palīdzētu novērst izpildlaika problēmas, kas var rasties, piemēram, izpildes kļūdas un veiktspējas kritums. Katrai atrastajai problēmai ir norādīts problemātiskā elementa ceļš. Dažām problēmām ir pieejams automātisks labojums.

Pēc noklusējuma validācija tiek automātiski pielietota tālāk norādītajos ER konfigurācijas gadījumos, kas satur iepriekš minētos ER komponentus.

- Tiek [importēta](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) jauna ER konfigurācijas [versija](general-electronic-reporting.md#component-versioning) jūsu Microsoft Dynamics 365 Finance instancē.
- Tiek mainīts rediģējamās ER konfigurācijas [statuss](general-electronic-reporting.md#component-versioning) no **Melnraksts** uz **Pabeigts**.
- Tiek [pārbāzēta](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) rediģējama ER konfigurācija, pielietojot jaunu bāzes versiju.

Noteikti varat palaist šo validāciju. Atlasiet vienu no tālāk norādītajām trim opcijām un sekojiet piedāvātajām darbībām.

- 1. opcija.

    1. Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.
    2. Kreisās puses rūtī esošajā konfigurāciju kokā atlasiet vēlamo ER konfigurāciju, kas satur ER formāta vai ER modeļa kartēšanas komponentu.
    3. Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER konfigurācijas vēlamo versiju.
    4. Darbību rūtī atlasiet **Pārbaudīt**.

- 2. variants ER formātam.

    1. Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.
    2. Kreisās puses rūtī esošajā konfigurāciju kokā atlasiet vēlamo ER konfigurāciju, kas satur ER formāta komponentu.
    3. Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER konfigurācijas vēlamo versiju.
    4. Darbību rūtī atlasiet **Noformētājs**.
    5. Lapā **Formāta noformētājs**, darbību rūtī atlasiet **Validēt**.

- 3. opcija ER modeļa kartēšanai.

    1. Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.
    2. Kreisās puses rūtī esošajā konfigurāciju kokā atlasiet vēlamo ER konfigurāciju, kas satur ER modeļa kartēšanas komponentu.
    3. Kopsavilkuma cilnē **Versijas** izvēlieties atlasītās ER konfigurācijas vēlamo versiju.
    4. Darbību rūtī atlasiet **Noformētājs**.
    5. Lapā **Datu avota kartējuma modelis** darbību rūtī atlasiet **Noformētājs**.
    6. Lapā **Modeļa kartēšanas veidotājs** darbību rūtī atlasiet **Validēt**.

Lai izlaistu validāciju, importējot konfigurāciju, veiciet tālāk norādītās darbības.

1. Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.
2. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
3. Iestatiet opciju **Validēt konfigurāciju pēc importēšanas** uz **Nē**.

Lai izlaistu validāciju, mainot vai pārbāzējot versijas statusu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.
2. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
3. Iestatiet opciju **Izlaist validāciju, mainot vai pārbāzējot konfigurācijas statusu** uz **Jā**.

ER lieto tālāk norādītās kategorijas, lai grupētu konsekvences pārbaudes.

- **Izpildāmība** — pārbaudes, kas atklāj kritiskas problēmas, kas var notikt izpildlaikā. Šīs problēmas lielākoties ir līmenī **Kļūda**. 
- **Veiktspēja** — pārbaudes, kas atklāj problēmas, kas var izraisīt neefektīvu konfigurēto ER komponentu izpildi. Šīs problēmas lielākoties ir līmenī **Brīdinājums**.
- **Datu integritāte** — pārbaudes, kas atklāj problēmas, kas var izraisīt datu zudumu vai izpildlaika problēmas. Šīs problēmas lielākoties ir līmenī **Brīdinājums**.

## <a name="list-of-inspections"></a>Pārbaužu saraksts

Tālāk redzamajā tabulā ir sniegts pārskats par ER sniegtajām pārbaudēm. Lai iegūtu vairāk informācijas par šīm pārbaudēm, izmantojiet saites pirmajā kolonnā, lai dotos uz attiecīgajām šīs tēmas sadaļām. Šajās sadaļās ir paskaidroti to komponentu veidus, kam ER nodrošina pārbaudes, un to, kā varat atkārtoti konfigurēt ER komponentus, lai palīdzētu novērst problēmas.

<table>
<thead>
<tr>
<th>Vārds, uzvārds</th>
<th>Kategorija</th>
<th>Līmenis</th>
<th>Ziņojums</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href='#i1'>Tipa pārveidošana</a></td>
<td>Izpildāmība</td>
<td>Kļūda</td>
<td>
<p>Nevar konvertēt &lt;veids&gt; veida izteiksmi uz &lt;veids&gt; veida lauku.</p>
<p><b>Izpildlaika kļūda:</b> veida izņēmums</p>
</td>
</tr>
<tr>
<td><a href='#i2'>Veida saderība</a></td>
<td>Izpildāmība</td>
<td>Kļūda</td>
<td>
<p>Konfigurēto izteiksmi nevar izmantot kā pašreizējā formāta elementa piesaisti datu avotam, jo šī izteiksme atpakaļsūta datu veida &lt;veids&gt; vērtību, kas ir ārpus datu veida apjoma, ko atbalsta pašreizējais formāta elements veids &lt;veids&gt;.</p>
<p><b>Izpildlaika kļūda:</b> izņēmums no veida</p>
</td>
</tr>
<tr>
<td><a href='#i3'>Trūkst konfigurācijas elementa</a></td>
<td>Izpildāmība</td>
<td>Kļūda</td>
<td>
<p>Nav atrasts ceļš &lt;ceļš&gt;.</p>
<p><b>Izpildlaika kļūda:</b> konfigurācijas elementa &lt;ceļš&gt; nav atrasts.</p>
</td>
</tr>
<tr>
<td><a href='#i4'>Izteiksmes ar FILTER funkciju izpildāmība</a></td>
<td>Izpildāmība</td>
<td>Kļūda</td>
<td>
<p>Funkcijas FILTER saraksta izteiksmei nevar izpildīt vaicājumu.</p>
<p><b>Izpildlaika kļūda:</b> filtrēšana netiek atbalstīta. Validējiet konfigurāciju, lai iegūtu plašāku informāciju par šo.</p>
</td>
</tr>
<tr>
<td rowspan='2'><a href='#i5'>GROUPBY datu avota izpildāmība</a></td>
<td>Izpildāmība</td>
<td>Kļūda</td>
<td>Ceļa &lt;ceļš&gt; neatbalsta vaicājumus.</td>
</tr>
<tr>
<td>Izpildāmība</td>
<td>Kļūda</td>
<td>
<p>Grupēšanu pēc funkcijas nevar izpildīt ar vaicājumu.</p>
<p><b>Izpildlaika kļūda:</b> grupēšanu pēc funkcijas nevar izpildīt ar vaicājumu.</p>
</td>
</tr>
<tr>
<td><a href='#i6'>JOIN datu avota izpildāmība</a></td>
<td>Izpildāmība</td>
<td>Kļūda</td>
<td>
<p>Nevar pievienot sarakstu &lt;ceļš&gt;, kas nav filtra vaicājums.</p>
<p><b>Izpildlaika kļūda:</b> apvienotā datu avota funkcijai jābūt filtra izteiksmei, nepareizi izsaukts aprēķinātais lauks.</p>
</td>
</tr>
<tr>
<td><a href='#i7'>Priekšroka funkcijai FILTER pret WHERE</a></td>
<td>Veiktspēja</td>
<td>Brīdinājums</td>
<td>FILTER funkcijas izmantošanai izteiksmei ir dodama priekšroka vairāk, nekā WHERE no veiktspējas perspektīvas. Atlasiet Labot, lai aizstātu to automātiski.</td>
</tr>
<tr>
<td><a href='#i8'>Priekšroka funkcijai ALLITEMSQUERY pret ALLITEMS</a></td>
<td>Veiktspēja</td>
<td>Brīdinājums</td>
<td>ALLITEMSQUERY funkcijas izmantošanai izteiksmei ir dodama priekšroka vairāk, nekā ALLITEMS no veiktspējas perspektīvas. Atlasiet Labot, lai aizstātu to automātiski.</td>
</tr>
<tr>
<td><a href='#i9'>Tukšu sarakstu gadījumu apsvēršana</a></td>
<td>Izpildāmība</td>
<td>Brīdinājums</td>
<td>
<p>Saraksts &lt;ceļš&gt; netiek pārbaudīts tukša saraksta gadījumam, tas var radīt kļūdu izpildlaikā. Pievienojiet pārbaudi tukša saraksta gadījumam.</p>
<p><b>Izpildlaika kļūda:</b> saraksts ir tukšs pie &lt;ceļš&gt;</p>
<p><b><a href='#i9a'>Potenciāla problēma</a> :</b> rinda tiek aizpildīta vienreiz, bet datu avots, no kā tā tiek aizpildīta, satur vairākus ierakstus</p>
</td>
</tr>
<tr>
<td><a href='#i10'>Izteiksmes ar FILTER funkciju izpildāmība (kešdarbe)</a></td>
<td>Izpildāmība</td>
<td>Kļūda</td>
<td>
<p>FILTER funkciju nevar pielietot atlasītajam datu avota veidam. Tabulas ierakstu veida datu avots ir pielietojams tikai tad, ja tas nav saglabāts kešatmiņā un tam nav manuāli pievienoti ligzdoti datu avoti.</p>
<p><b>Izpildlaika kļūda:</b> filtrēšana netiek atbalstīta. Validējiet konfigurāciju, lai iegūtu plašāku informāciju par šo.</p>
</td>
</tr>
<tr>
<td><a href='#i11'>Trūkst saistījuma</a></td>
<td>Izpildāmība</td>
<td>Brīdinājums</td>
<td>
<p>Ceļam &lt;ceļš&gt; nav saistījuma ar jebkādu datu avotu, izmantojot modeļa kartēšanu.</p>
<p><b>Izpildlaika kļūda:</b> Ceļš &lt;ceļš&gt; nav saistīts</p>
</td>
</tr>
<tr>
<td><a href='#i12'>Nav saistīta veidne</a></td>
<td>Datu integritāte</td>
<td>Brīdinājums</td>
<td>Fails &lt;nosaukums&gt; nav saistīts ar nevienu faila komponentu, un tas tiks noņemts pēc konfigurācijas versijas statusa maiņas.</td>
</tr>
<tr>
<td><a href='#i13'>Nav sinhronizēts formāts</a></td>
<td>Datu integritāte</td>
<td>Brīdinājums</td>
<td>Definētais nosaukums &lt;komponenta nosaukums&gt; nepastāv Excel lapā &lt;lapas nosaukumā&gt;</td>
</tr>
<tr>
<td><a href='#i14'>Nav sinhronizēts formāts</a></td>
<td>Datu integritāte</td>
<td>Brīdinājums</td>
<td>
<p>&lt;Atzīmētā Word satura kontrole&gt; tags nepastāv Word veidnes failā</p>
<p><b>Izpildlaika kļūda:</b> &lt;Atzīmētā Word satura kontrole&gt; tags nepastāv Word veidnes failā.</p>
</td>
</tr>
<tr>
<td><a href='#i15'>Nav noklusējuma kartējuma</a></td>
<td>Datu integritāte</td>
<td>Kļūda</td>
<td>
<p>Ir vairāk nekā viens modeļa kartējums &lt;modeļa nosaukumam (saknes aprakstītājam)&gt; datu modelim konfigurācijās &lt;konfigurāciju nosaukumi ir atdalīti ar komatu&gt;. Iestatiet vienu no konfigurācijām kā noklusējumu</p>
<p><b>Izpildlaika kļūda:</b> Ir vairāk nekā viens modeļa kartējums &lt;modeļa nosaukumam (saknes aprakstītājam)&gt; datu modelim konfigurācijās &lt;konfigurāciju nosaukumi ir atdalīti ar komatu&gt;. Iestatiet vienu no konfigurācijām kā noklusējumu.</p>
</td>
</tr>
<tr>
<td><a href='#i16'>Nesaskaņoti galvenes vai kājenes komponentu iestatījumi</a></td>
<td>Datu integritāte</td>
<td>Kļūda</td>
<td>
<p>Galvenes/kājenes (&lt;komponenta veids: galvene vai kājene&gt;) nesakrīt</p>
<p><b>Izpildlaiks:</b> pēdējais konfigurētais komponents tiek izmantots izpildlaikā, ja ir izpildīta konfigurētā ER formāta melnraksta versija.</p>
</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a>Tipa pārveidošana

ER pārbauda, vai datu modeļa lauka datu veids ir saderīgs ar izteiksmes datu veidu, kas ir konfigurēts kā šī lauka saistījums. Ja datu veidi nav saderīgi, ER modeļa kartēšanas veidotājā rodas validācijas kļūda. Ziņojumā, ko saņemat, norādīts, ka ER nevar pārveidot A veida izteiksmi B veida laukā.

Tālāk norādītajās darbībās parādīts, kā šī problēma varētu rasties.

1. Sāciet vienlaicīgi konfigurēt ER datu modeli un ER modeļa kartēšanas komponentus.
2. Datu modeļa kokā pievienojiet lauku ar nosaukumu **X** un kā datu veidu atlasiet **Vesels skaitlis**.

    ![X lauks un vesela skaitļa datu veids tiek pievienots datu režīma kokam Datu modeļa lapā](./media/er-components-inspections-01.png)

3. Modeļa kartēšanas veidotāja rūtī **Datu avoti** pievienojiet veida **Aprēķinātais lauks** datu avotu.
4. Piešķiriet jaunajam datu avotam nosaukumu **Y** un konfigurējiet to, lai tas ietvertu izteiksmi `INTVALUE(100)`.
5. Saistiet **X** ar **Y**.
6. Datu modeļa veidotājā mainiet datu veidu laukam **X** no **Vesels skaitlis** uz **Int64**.
7. Atlasiet **Validēt**, lai pārbaudītu rediģējamā modeļa kartēšanas komponentu lapā **Modeļa kartēšanas veidotājs**.

    ![Rediģējamā modeļa kartēšanas komponenta validēšana lapā Modeļa kartēšanas veidotājs](./media/er-components-inspections-01.gif)

8. Atlasiet **Validēt**, lai pārbaudītu atlasītās ER konfigurācijas modeļa kartēšanas komponentu lapā **Konfigurācijas**.

    ![Pārbaudiet modeļa kartēšanas komponentu lapā Konfigurācijas](./media/er-components-inspections-01a.png)

9. Ņemiet vērā, ka rodas validācijas kļūda. Ziņojumā norādīts, ka **Vesels skaitlis** veida vērtība, ko atpakaļsūta `INTVALUE(100)` izteiksme no **Y** datu avota nevar tikt saglabāta **X** datu modeļa laukā ar **Int64** veidu.

Tālāk redzamajā attēlā parādīta izpildlaika kļūda, kas rodas, ja ignorējat brīdinājumu un atlasāt **Palaist**, lai palaistu formātu, kas ir konfigurēts modeļa kartēšanas izmantošanai.

![Izpildlaika kļūdas Formāta veidotāja lapā](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a>Automātisks risinājums

Nav pieejama opcija automātiski novērst šo problēmu.

### <a name="manual-resolution"></a>Manuāls risinājums

#### <a name="option-1"></a>1. opcija

Atjauniniet datu modeļa struktūru, mainot datu modeļa lauka datu veidu tā, lai tas atbilstu tās izteiksmes datu veidam, kas ir konfigurēta šī lauka saistījumam. Iepriekšējā piemērā lauka **X** datu veids ir jānomaina atpakaļ uz **Vesels skaitlis**.

#### <a name="option-2"></a>2. opcija

Atjauniniet modeļa kartēšanu, mainot datu avota izteiksmi, kas ir saistīta ar datu modeļa lauku. Iepriekšējā piemērā datu avota **Y** izteiksme ir jāmaina uz `INT64VALUE(100)`.

## <a name="type-compatibility"></a><a id="i2"></a>Veida saderība

ER pārbauda, vai formāta elementa datu veids ir saderīgs ar izteiksmes datu veidu, kas ir konfigurēts kā šī formāta elementa saistījums. Ja datu veidi nav saderīgi, ER Darbību veidotājā rodas validācijas kļūda. Ziņojumā, ko saņemat, norādīts, ka konfigurēto izteiksmi nevar izmantot kā pašreizējā formāta elementa piesaisti datu avotam, jo šī izteiksme atpakaļsūta datu veida A vērtību, kas ir ārpus datu veida apjoma, ko atbalsta pašreizējais formāta elements veids B.

Tālāk norādītajās darbībās parādīts, kā šī problēma varētu rasties.

1. Sāciet vienlaicīgi konfigurēt ER datu modeli un ER formāta komponentus.
2. Datu modeļa kokā pievienojiet lauku ar nosaukumu **X** un kā datu veidu atlasiet **Vesels skaitlis**.
3. Formāta struktūras kokā pievienojiet **Skaitlisks** veida formāta elementu.
4. Piešķiriet nosaukumu jaunajam formāta elementam **Y**. Laukā **Skaitliskais veids** kā datu veidu atlasiet **Vesels skaitlis**.
5. Saistiet **X** ar **Y**.
6. Formāta struktūras kokā mainiet **Y** formāta elementa datu veidu no **Vesels skaitlis** uz **Int64**.
7. Atlasiet **Validēt**, lai pārbaudītu rediģējamā formāta komponentu lapā **Formāta veidotājs**.

    ![Vaida saderības validēšana lapā Formāta veidotājs](./media/er-components-inspections-02.gif)

8. Ņemiet vērā, ka rodas validācijas kļūda. Ziņojumā norādīts, ka konfigurētā izteiksme var akceptēt tikai **Int64** vērtības. Tāpēc datu modeļa lauka **X** vērtību ar veidu **Vesels skaitlis** nevar ievadīt **Y** formāta elementā.

### <a name="automatic-resolution"></a>Automātisks risinājums

Nav pieejama opcija automātiski novērst šo problēmu.

### <a name="manual-resolution"></a>Manuāls risinājums

#### <a name="option-1"></a>1. opcija

Atjauniniet formāta struktūru, mainot formāta elementa **Skaitlisks** datu veidu tā, lai tas atbilstu tās izteiksmes datu veidam, kas ir konfigurēta šī elementa saistījumam. Iepriekšējā piemērā vērtība **Skaitlisks veids** formāta elementam **X** ir jānomaina atpakaļ uz **Vesels skaitlis**.

#### <a name="option-2"></a>2. opcija

Atjauniniet formāta elementa **X** formāta kartēšanu, mainot izteiksmi no `model.X` uz `INT64VALUE(model.X)`.

## <a name="missing-configuration-element"></a><a id="i3"></a>Trūkst konfigurācijas elementa

ER pārbauda, vai saistījuma izteiksmes satur tikai tos datu avotus, kas ir konfigurēti rediģējamā ER komponentā. Katram saistījumam, kas satur datu avotu, kas trūkst rediģējamā ER komponentā, ER Darbību veidotājā vai ER modeļa kartēšanas veidotājā rodas validācijas kļūda.

Tālāk norādītajās darbībās parādīts, kā šī problēma varētu rasties.

1. Sāciet vienlaicīgi konfigurēt ER datu modeli un ER modeļa kartēšanas komponentus.
2. Datu modeļa kokā pievienojiet lauku ar nosaukumu **X** un kā datu veidu atlasiet **Vesels skaitlis**.

    ![Datu modeļa koks ar X lauku un vesela skaitļa datu veidu Datu modeļa lapā](./media/er-components-inspections-01.png)

3. Modeļa kartēšanas veidotāja rūtī **Datu avoti** pievienojiet veida **Aprēķinātais lauks** datu avotu.
4. Piešķiriet jaunajam datu avotam nosaukumu **Y** un konfigurējiet to, lai tas ietvertu izteiksmi `INTVALUE(100)`.
5. Saistiet **X** ar **Y**.
6. Modeļa kartēšanas veidotāja rūtī **Datu avoti** izdzēsiet datu avotu **Y**.
7. Atlasiet **Validēt**, lai pārbaudītu rediģējamā modeļa kartēšanas komponentu lapā **Modeļa kartēšanas veidotājs**.

    ![Pārbaudiet rediģējamā ER modeļa kartēšanas komponentu lapā Modeļa kartēšanas veidotājs](./media/er-components-inspections-03.gif)

8. Ņemiet vērā, ka rodas validācijas kļūda. Ziņojumā norādīts, ka datu modeļa lauka **X** saistījums satur ceļu, kas atsaucas uz datu avotu **Y**, bet šis datu avots nav atrasts.

### <a name="automatic-resolution"></a>Automātisks risinājums

Atlasiet **Atsaistīt**, lai automātiski novērstu šo problēmu, noņemot trūkstošo datu avota saistījumu.

### <a name="manual-resolution"></a>Manuāls risinājums

#### <a name="option-1"></a>1. opcija

Atsaistiet datu modeļa lauku **X**, lai pārtrauktu atsaukšanos uz neesošu datu avotu **Y**.

#### <a name="option-2"></a>2. opcija

Modeļa kartēšanas veidotāja rūtī **Datu avoti** no jauna pievienojiet datu avotu **Y**.

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a>Izteiksmes ar FILTER funkciju izpildāmība

Iebūvētā ER funkcija [FILTER](er-functions-list-filter.md) tiek izmantota, lai piekļūtu pieteikumu tabulām, skatiem vai datu entītijām, veicot vienu SQL izsaukumu, lai iegūtu vajadzīgos datus kā ierakstu sarakstu. **Ierakstu saraksts** veida datu avots tiek izmantots kā šīs funkcijas arguments un norāda izsaukuma pieteikuma avotu. ER pārbauda, vai var tikt izveidots tiešais SQL vaicājums uz datu avotu, kas ir norādīts funkcijā `FILTER`. Ja tiešo vaicājumu nevar izveidot, ER modeļa kartēšanas veidotājā rodas validācijas kļūda. Ziņojumā, ko saņemat, norādīts, ka ER izteiksmi, kas ietver funkciju `FILTER`, nevar palaist izpildlaikā.

Tālāk norādītajās darbībās parādīts, kā šī problēma varētu rasties.

1. Sāciet konfigurēt ER modeļa kartēšanas komponentu.
2. Pievienojiet **Dynamics 365 for Operations \\ Tabulas ieraksti** veida datu avotu.
3. Piešķiriet jaunajam datu avotam nosaukumu **Kreditors**. Laukā **Tabula** atlasiet **VendTable**, lai norādītu, ka šis datu avots pieprasīs VendTable tabulu.
4. Pievienojiet **Aprēķinātais lauks** veida datu avotu.
5. Piešķiriet jaunajam datu avotam nosaukumu **FilteredVendor** un konfigurējiet to, lai tas ietvertu izteiksmi `FILTER(Vendor, Vendor.AccountNum="US-101")`.
6. Atlasiet **Validēt**, lai pārbaudītu rediģējamo modeļa kartēšanas komponentu lapā **Modeļa kartēšanas veidotājs**, un pārbaudiet, vai var iesniegt vaicājumu izteiksmei `FILTER(Vendor, Vendor.AccountNum="US-101")` datu avotā **Kreditors**.
7. Modificējiet datu avotu **Kreditors**, pievienojot **Aprēķinātais lauks** veida ligzdoto lauku, lai iegūtu apgrieztu kreditora konta numuru.
8. Piešķiriet jaunajam ligzdotajam laukam nosaukumu **$AccNumber** un konfigurējiet to, lai tas ietvertu izteiksmi `TRIM(Vendor.AccountNum)`.
9. Atlasiet **Validēt**, lai pārbaudītu rediģējamo modeļa kartēšanas komponentu lapā **Modeļa kartēšanas veidotājs**, un pārbaudiet, vai var iesniegt vaicājumu izteiksmei `FILTER(Vendor, Vendor.AccountNum="US-101")` datu avotā **Kreditors**.

    ![Pārbaude, vai izteiksmei var iesniegt vaicājumu lapā Modeļa kartēšanas veidotājs](./media/er-components-inspections-04.gif)

10. Ņemiet vērā, ka validācijas kļūda rodas, jo datu avots **Kreditors** satur **Aprēķinātais lauks** veida ligzdoto lauku, kas neļauj **FilteredVendor** datu avota izteiksmi pārveidot par tiešu SQL norādīšanu.

Tālāk redzamajā attēlā parādīta izpildlaika kļūda, kas rodas, ja ignorējat brīdinājumu un atlasāt **Palaist**, lai palaistu formātu, kas ir konfigurēts modeļa kartēšanas izmantošanai.

![Izpildlaika kļūdas, kas rodas, palaižot rediģējamo formātu lapā Formāta veidotājs](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a>Automātisks risinājums

Nav pieejama opcija automātiski novērst šo problēmu.

### <a name="manual-resolution"></a>Manuāls risinājums

#### <a name="option-1"></a>1. opcija

Tā vietā, lai **Aprēķinātais lauks** veida ligzdoto lauku pievienotu datu avotam **Kreditors**, pievienojiet ligzdoto lauku **$AccNumber** datu avotam **FilteredVendor** un konfigurējiet to, lai tas saturētu izteiksmi `TRIM(FilteredVendor.AccountNum)`. Šādā veidā izteiksmi `FILTER(Vendor, Vendor.AccountNum="US-101")` var palaist SQL līmenī un pēc tam aprēķināt **$AccNumber** ligzdoto lauku.

#### <a name="option-2"></a>2. opcija

Mainiet datu avota **FilteredVendor** izteiksmi no `FILTER(Vendor, Vendor.AccountNum="US-101")` uz `WHERE(Vendor, Vendor.AccountNum="US-101")`. Nav ieteicams mainīt izteiksmi tabulai, kurā ir liels datu apjoms (darījumu tabula), jo tiks paņemti visi ieraksti, un vajadzīgo ierakstu atlase tiks veikta atmiņā. Tāpēc šī pieeja var izraisīt sliktu veiktspēju. Plašāku informāciju skatiet [ER funkcija WHERE](er-functions-list-where.md).

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a>GROUPBY datu avota izpildāmība

Datu avots **GROUPBY** sadala vaicājuma rezultātus ierakstu grupās, parasti, lai veiktu vienu vai vairākus apkopojumus katrā grupā. Katru datu avotu **GROUPBY** var konfigurēt tā, lai tas tiktu palaists vai nu datu bāzes līmenī, vai atmiņā. Kad datu avots **GROUPBY** ir konfigurēts tā, ka tas tiktu palaists datu bāzes līmenī, ER pārbauda, vai var tikt izveidots tiešais SQL vaicājums uz datu avotu, uz kuru ir atsauce šajā datu avotā. Ja tiešo vaicājumu nevar izveidot, ER modeļa kartēšanas veidotājā rodas validācijas kļūda. Ziņojumā, ko saņemat, norādīts, ka konfigurēto datu avotu **GROUPBY** nevar palaist izpildlaikā.

Tālāk norādītajās darbībās parādīts, kā šī problēma varētu rasties.

1. Sāciet konfigurēt ER modeļa kartēšanas komponentu.
2. Pievienojiet **Dynamics 365 for Operations \\ Tabulas ieraksti** veida datu avotu.
3. Piešķiriet jaunajam datu avotam nosaukumu **Trans**. Laukā **Tabula** atlasiet **VendTrans**, lai norādītu, ka šis datu avots pieprasīs VendTrans tabulu.
4. Pievienojiet **Grupēt pēc** veida datu avotu.
5. Piešķiriet jaunajam datu avotam nosaukumu **GroupedTrans** un konfigurējiet to, kā norādīts tālāk.

    - Atlasiet datu avotu **Trans** kā ierakstu avotu, kas jāgrupē.
    - Laukā **Izpildes vieta** atlasiet **Vaicājums**, lai norādītu, ka vēlaties palaist šo datu avotu datu bāzes līmenī.

    ![Datu avotu konfigurēšana lapā Rediģēt parametrus "Grupēt pēc"](./media/er-components-inspections-05a.gif)

6. Atlasiet **Validēt**, lai pārbaudītu rediģējamo modeļa kartēšanas komponentu lapā **Modeļa kartēšanas veidotājs** un pārbaudiet, vai var iesniegt vaicājumu konfigurētajam datu avotam **GroupedTrans**.
7. Modificējiet datu avotu **Trans**, pievienojot **Aprēķinātais lauks** veida ligzdoto lauku, lai iegūtu apgrieztu kreditora konta numuru.
8. Piešķiriet jaunajam datu avotam nosaukumu **$AccNumber** un konfigurējiet to, lai tas ietvertu izteiksmi `TRIM(Trans.AccountNum)`.

    ![Datu avota konfigurēšana lapā Modeļa kartēšanas veidotājs](./media/er-components-inspections-05a.png)

9. Atlasiet **Validēt**, lai pārbaudītu rediģējamo modeļa kartēšanas komponentu lapā **Modeļa kartēšanas veidotājs** un pārbaudiet, vai var iesniegt vaicājumu konfigurētajam datu avotam **GroupedTrans**.

    ![Validējiet ER modeļa kartēšanas komponentu un pārbaudiet, vai lapā Modeļa kartēšanas veidotājs var iesniegt vaicājumu datu avotam GroupedTrans](./media/er-components-inspections-05b.png)

10. Ņemiet vērā, ka validācijas kļūda rodas, jo datu avots **Trans** satur **Aprēķinātais lauks** veida ligzdoto lauku, kas neļauj **GroupedTrans** datu avota izteiksmes izsaukumu pārveidot par tiešu SQL norādīšanu.

Tālāk redzamajā attēlā parādīta izpildlaika kļūda, kas rodas, ja ignorējat brīdinājumu un atlasāt **Palaist**, lai palaistu formātu, kas ir konfigurēts modeļa kartēšanas izmantošanai.

![Izpildlaika kļūdas, kas rodas, ja tiek ignorēts brīdinājums lapā Formāta veidotājs](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a>Automātisks risinājums

Nav pieejama opcija automātiski novērst šo problēmu.

### <a name="manual-resolution"></a>Manuāls risinājums

#### <a name="option-1"></a>1. opcija

Tā vietā, lai **Aprēķinātais lauks** veida ligzdoto lauku pievienotu datu avotam **Trans**, pievienojiet ligzdoto lauku **$AccNumber** krājumam **GroupedTrans.lines** datu avotā **GroupedTrans** un konfigurējiet to, lai tas saturētu izteiksmi `TRIM(GroupedTrans.lines.AccountNum)`. Šādā veidā datu avotu **GroupedTrans** var palaist SQL līmenī un pēc tam aprēķināt **$AccNumber** ligzdoto lauku.

#### <a name="option-2"></a>2. opcija

Mainiet lauka **Izpildes vieta** vērtību datu avotam **GroupedTrans** no **Vaicājums** uz **Atmiņā**. Nav ieteicams mainīt vērtību tabulai, kurā ir liels datu apjoms (darījumu tabula), jo tiks paņemti visi ieraksti, un grupēšana un apkopošana tiks veikta atmiņā. Tāpēc šī pieeja var izraisīt sliktu veiktspēju.

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a>JOIN datu avota izpildāmība

Datu avots [JOIN](er-join-data-sources.md) apvieno ierakstus no divām vai vairākām datu bāzes tabulām, pamatojoties uz saistītiem laukiem. Katru datu avotu **JOIN** var konfigurēt tā, lai tas tiktu palaists vai nu datu bāzes līmenī, vai atmiņā. Kad datu avots **JOIN** ir konfigurēts tā, ka tas tiktu palaists datu bāzes līmenī, ER pārbauda, vai var tikt izveidots tiešais SQL vaicājums uz datu avotiem, uz kuriem ir atsauce šajā datu avotā. Ja nevar izveidot tiešo SQL vaicājumu ar vismaz vienu datu avotu, uz kuru ir atsauce, ER modeļa kartēšanas veidotājā rodas validācijas kļūda. Ziņojumā, ko saņemat, norādīts, ka konfigurēto datu avotu **JOIN** nevar palaist izpildlaikā.

Tālāk norādītajās darbībās parādīts, kā šī problēma varētu rasties.

1. Sāciet konfigurēt ER modeļa kartēšanas komponentu.
2. Pievienojiet **Dynamics 365 for Operations \\ Tabulas ieraksti** veida datu avotu.
3. Piešķiriet jaunajam datu avotam nosaukumu **Kreditors**. Laukā **Tabula** atlasiet **VendTable**, lai norādītu, ka šis datu avots pieprasīs VendTable tabulu.
4. Pievienojiet **Dynamics 365 for Operations \\ Tabulas ieraksti** veida datu avotu.
5. Piešķiriet jaunajam datu avotam nosaukumu **Trans**. Laukā **Tabula** atlasiet **VendTrans**, lai norādītu, ka šis datu avots pieprasīs VendTrans tabulu.
6. Pievienojiet **Aprēķinātais lauks** veida datu avotu kā datu avota **Kreditors** ligzdoto lauku.
7. Piešķiriet jaunajam datu avotam nosaukumu **FilteredTrans** un konfigurējiet to, lai tas ietvertu izteiksmi `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.
8. Pievienojiet **Savienot** veida datu avotu.
9. Piešķiriet jaunajam datu avotam nosaukumu **JoinedList** un konfigurējiet to, kā norādīts tālāk.

    1. Pievienojiet datu avotu **Kreditors** kā pirmo savienojamo ierakstu kopu.
    2. Pievienojiet datu avotu **Vendor.FilteredTrans** kā otro savienojamo ierakstu kopu. Atlasiet **INNER** kā veidu.
    3. Laukā **Izpildīt** atlasiet **Vaicājums**, lai norādītu, ka vēlaties palaist šo datu avotu datu bāzes līmenī.

    ![Datu avota konfigurēšana Savienošanas veidotāja lapā](./media/er-components-inspections-06a.gif)

10. Atlasiet **Validēt**, lai pārbaudītu rediģējamo modeļa kartēšanas komponentu lapā **Modeļa kartēšanas veidotājs** un pārbaudiet, vai var iesniegt vaicājumu konfigurētajam datu avotam **JoinedList**.
11. Mainiet datu avota **Vendor.FilteredTrans** izteiksmi no `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` uz `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.
12. Atlasiet **Validēt**, lai pārbaudītu rediģējamo modeļa kartēšanas komponentu lapā **Modeļa kartēšanas veidotājs** un pārbaudiet, vai var iesniegt vaicājumu konfigurētajam datu avotam **JoinedList**.

    ![Rediģējamā modeļa kartēšanas komponenta validācija un pārbaude, vai lapā Modeļa kartēšanas veidotājs var iesniegt vaicājumu datu avotam JoinedList](./media/er-components-inspections-06b.png)

13. Ņemiet vērā, ka validācijas kļūda rodas, jo datu avota **Vendor.FilteredTrans** izteiksmi nevar pārveidot par tiešu SQL izsaukumu. Turklāt tiešais SQL izsaukums neļauj datu avota **JoinedList** izsaukumu pārveidot par tiešu SQL norādīšanu.

    ![Izpildlaika kļūdas no neizdevušās JoinedList datu avota validācijas lapā Modeļa kartēšanas veidotājs](./media/er-components-inspections-06c.png)

Tālāk redzamajā attēlā parādīta izpildlaika kļūda, kas rodas, ja ignorējat brīdinājumu un atlasāt **Palaist**, lai palaistu formātu, kas ir konfigurēts modeļa kartēšanas izmantošanai.

![Rediģējamā formāta palaišana lapā Formāta veidotājs](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a>Automātisks risinājums

Nav pieejama opcija automātiski novērst šo problēmu.

### <a name="manual-resolution"></a>Manuāls risinājums

#### <a name="option-1"></a>1. opcija

Mainiet datu avota **Vendor.FilteredTrans** izteiksmi no `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` atpakaļ uz `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, kā ieteikts brīdinājumā.

![Atjaunināta datu avota izteiksme lapā Modeļa kartēšanas veidotājs](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a>2. opcija

Mainiet lauka **Izpildīt** vērtību datu avotam **JoinedList** no **Vaicājums** uz **Atmiņā**. Nav ieteicams mainīt vērtību tabulai, kurā ir liels datu apjoms (darījumu tabula), jo tiks paņemti visi ieraksti, un grupēšana un savienošana tiks veikta atmiņā. Tāpēc šī pieeja var izraisīt sliktu veiktspēju. Tiek parādīts brīdinājums par validāciju, lai informētu par šo risku.

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a>Priekšroka funkcijai FILTER pret WHERE

Iebūvētā ER funkcija [FILTER](er-functions-list-filter.md) tiek izmantota, lai piekļūtu pieteikumu tabulām, skatiem vai datu entītijām, veicot vienu SQL izsaukumu, lai iegūtu vajadzīgos datus kā ierakstu sarakstu. Funkcija [WHERE](er-functions-list-where.md) ielādē visus ierakstus no dotā avota un ieraksta atlasi atmiņā. **Ierakstu saraksts** veida datu avots tiek izmantots abu funkciju arguments un norāda ierakstu iegūšanas avotu. ER pārbauda, vai var tikt izveidots tiešais SQL izsaukums uz datu avotu, kas ir norādīts funkcijā **WHERE**. Ja tiešo izsaukumu nevar izveidot, ER modeļa kartēšanas veidotājā notiek brīdinājums par validāciju. Saņemtais ziņojums iesaka izmantot funkciju **FILTER**, nevis funkciju **WHERE**, lai palīdzētu uzlabot efektivitāti.

Tālāk norādītajās darbībās parādīts, kā šī problēma varētu rasties.

1. Sāciet konfigurēt ER modeļa kartēšanas komponentu.
2. Pievienojiet **Dynamics 365 for Operations \\ Tabulas ieraksti** veida datu avotu.
3. Piešķiriet jaunajam datu avotam nosaukumu **Trans**. Laukā **Tabula** atlasiet **VendTrans**, lai norādītu, ka šis datu avots pieprasīs VendTrans tabulu.
4. Pievienojiet **Aprēķinātais lauks** veida datu avotu kā datu avota **Kreditors** ligzdoto lauku.
5. Piešķiriet jaunajam datu avotam nosaukumu **FilteredTrans** un konfigurējiet to, lai tas ietvertu izteiksmi `WHERE(Trans, Trans.AccountNum="US-101")`.
6. Pievienojiet **Dynamics 365 for Operations \\ Tabulas ieraksti** veida datu avotu.
7. Piešķiriet jaunajam datu avotam nosaukumu **Kreditors**. Laukā **Tabula** atlasiet **VendTable**, lai norādītu, ka šis datu avots pieprasīs VendTable tabulu.
8. Pievienojiet **Aprēķinātais lauks** veida datu avotu.
9. Piešķiriet jaunajam datu avotam nosaukumu **FilteredVendor** un konfigurējiet to, lai tas ietvertu izteiksmi `WHERE(Vendor, Vendor.AccountNum="US-101")`.
10. Atlasiet **Validēt**, lai pārbaudītu rediģējamā modeļa kartēšanas komponentu lapā **Modeļa kartēšanas veidotājs**.

    ![Pārbaudiet rediģējamā modeļa kartēšanas komponentu lapā Modeļa kartēšanas veidotājs](./media/er-components-inspections-07a.png)

11. Ņemiet vērā, ka brīdinājumi par validāciju iesaka izmantot funkciju **FILTER**, nevis funkciju **WHERE** datu avotiem **FilteredVendor** un **FilteredTrans**.

    ![Ieteikums izmantot FILTRA funkciju, nevis funkciju "KUR" lapā Modeļa kartēšanas veidotājs](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a>Automātisks risinājums

Atlasiet **Labot**, lai automātiski aizstātu funkciju **WHERE** ar funkciju **FILTER** visu datu avotu izteiksmē, kas parādās režģī šī pārbaudes veida cilnē **Brīdinājumi**.

Varat arī atlasīt rindu vienam brīdinājumam režģī un pēc tam atlasīt **Labot atlasīto**. Šādā gadījumā izteiksme automātiski tiek mainīta tikai datu avotā, kas ir minēts atlasītajā brīdinājumā.

!["Labot" atlasīšana, lai automātiski aizstātu funkciju "KUR" ar FILTRA funkciju lapā Modeļa kartēšanas veidotājs](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a>Manuāls risinājums

Varat manuāli koriģēt visu validācijas režģī minēto datu avotu izteiksmes, aizstājot funkciju **KUR** ar funkciju **FILTRS**.

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a>Priekšroka funkcijai ALLITEMSQUERY pret ALLITEMS

Iebūvētās ER funkcijas [ALLITEMS](er-functions-list-allitems.md) un [ALLITEMSQUERY](er-functions-list-allitemsquery.md) tiek izmantotas, lai iegūtu saplacinātu **Ierakstu saraksts** vērtību, kas sastāv no ierakstu saraksta, kas pārstāv visus krājumus, kuri atbilst norādītajam ceļam. ER pārbauda, vai var tikt izveidots tiešais SQL izsaukums uz datu avotu, kas ir norādīts funkcijā **ALLITEMS**. Ja tiešo izsaukumu nevar izveidot, ER modeļa kartēšanas veidotājā notiek brīdinājums par validāciju. Saņemtais ziņojums iesaka izmantot funkciju **ALLITEMSQUERY**, nevis funkciju **ALLITEMS**, lai palīdzētu uzlabot efektivitāti.

Tālāk norādītajās darbībās parādīts, kā šī problēma varētu rasties.

1. Sāciet konfigurēt ER modeļa kartēšanas komponentu.
2. Pievienojiet **Dynamics 365 for Operations \\ Tabulas ieraksti** veida datu avotu.
3. Piešķiriet jaunajam datu avotam nosaukumu **Kreditors**. Laukā **Tabula** atlasiet **VendTable**, lai norādītu, ka šis datu avots pieprasīs VendTable tabulu.
4. Pievienojiet **Aprēķinātais lauks** veida datu avotu, lai iegūtu vairāku kreditoru ierakstus.
5. Piešķiriet jaunajam datu avotam nosaukumu **FilteredVendor** un konfigurējiet to, lai tas ietvertu izteiksmi `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.
6. Pievienojiet **Aprēķinātais lauks** veida datu avotu, lai visu filtrēto kreditoru darījumus.
7. Piešķiriet jaunajam datu avotam nosaukumu **FilteredVendorTans** un konfigurējiet to, lai tas ietvertu izteiksmi `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.
8. Atlasiet **Validēt**, lai pārbaudītu rediģējamā modeļa kartēšanas komponentu lapā **Modeļa kartēšanas veidotājs**.

    ![Pārbaudiet rediģējamā modeļa kartēšanas komponentu lapā Modeļa kartēšanas veidotājs](./media/er-components-inspections-08a.png)

9. Ņemiet vērā, ka notiek brīdinājums par validāciju. Ziņojumā ieteikts izmantot funkciju **ALLITEMSQUERY**, nevis funkciju **ALLITEMS** datu avotam **FilteredVendorTrans**.

    ![Ieteikums izmantot ALLITEMSQUERY funkciju, nevis funkciju ALLITEMS lapā Modeļa kartēšanas veidotājs](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a>Automātisks risinājums

Atlasiet **Labot**, lai automātiski aizstātu funkciju **ALLITEMS** ar funkciju **ALLITEMSQUERY** visu datu avotu izteiksmē, kas parādās režģī šī pārbaudes veida cilnē **Brīdinājumi**.

Varat arī atlasīt rindu vienam brīdinājumam režģī un pēc tam atlasīt **Labot atlasīto**. Šādā gadījumā izteiksme automātiski tiek mainīta tikai datu avotā, kas ir minēts atlasītajā brīdinājumā.

!["Labot atlasītos" atlasīšana lapā Modeļa kartēšanas veidotājs](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a>Manuāls risinājums

Varat manuāli koriģēt visu validācijas režģī minēto datu avotu izteiksmes, aizstājot funkciju **ALLITEMS** ar funkciju **ALLITEMSQUERY**.

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a>Tukšu sarakstu gadījumu apsvēršana

Varat konfigurēt savu ER formāta vai modeļa kartēšanas komponentu, lai iegūtu **Ierakstu saraksts** veida datu avota lauka vērtību. ER pārbauda, vai izveidotais apskata gadījumu, kad izsauktais datu avots nesatur ierakstus (tas ir tukšs), lai novērstu izpildlaika kļūdas, kad vērtība tiek iegūta no neeksistējoša ieraksta lauka.

Tālāk norādītajās darbībās parādīts, kā šī problēma varētu rasties.

1. Sāciet vienlaicīgi konfigurēt ER datu modeli, ER modeļa kartēšanu un ER formāta komponentus.
2. Datu modeļa kokā pievienojiet saknes krājumu, kura nosaukums ir **Root3**.
3. Modificējiet krājumu **Root3**, pievienojot **Ierakstu saraksts** veida ligzdoto krājumu.
4. Piešķiriet jaunajam ligzdotajam krājumam nosaukumu **Kreditors**.
5. Modificējiet krājumu **Kreditors** tālāk norādītajā veidā.

    - Pievienojiet **Virkne** veida ligzdoto lauku un piešķiriet tam nosaukumu **Nosaukums**.
    - Pievienojiet **Virkne** veida ligzdoto lauku un piešķiriet tam nosaukumu **AccountNumber**.

    ![Ligzdoto lauku pievienošana lapā Datu modelis](./media/er-components-inspections-09a.png)

6. Modeļa kartēšanas veidotāja rūtī rūtī **Datu avoti** pievienojiet veida **Dynamics 365 for Operations \\ Tabulas ieraksti** datu avotu.
7. Piešķiriet jaunajam datu avotam nosaukumu **Kreditors**. Laukā **Tabula** atlasiet **VendTable**, lai norādītu, ka šis datu avots pieprasīs VendTable tabulu.
8. Pievienojiet **Vispārīgi \\ Lietotāja ievades parametrs** veida datu avotu, lai uzmeklētu kreditora kontu izpildlaika dialoglodziņā.
9. Piešķiriet jaunajam datu avotam nosaukumu **RequestedAccountNum**. Laukā **Etiķete** ievadiet **Kreditora konta numurs**. Laukā **Operāciju datu veida nosaukums** atstājiet noklusējuma vērtību **Apraksts**.
10. Pievienojiet **Aprēķinātais lauks** veida datu avotu, lai filtrētu kreditoru, par kuru veikts vaicājums.
11. Piešķiriet jaunajam datu avotam nosaukumu **FilteredVendor** un konfigurējiet to, lai tas ietvertu izteiksmi `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Saistiet datu modeļa krājumus ar konfigurētajiem datu avotiem tālāk norādītajā veidā.

    - Saistiet **FilteredVendor** ar **Kreditors**.
    - Saistiet **FilteredVendor.AccountNum** ar **Vendor. AccountNumber**.
    - Saistiet **FilteredVendor.'name()'** ar **Vendor.Name**.

    ![Datu modeļa krājumu saistīšana lapā Modeļa kartēšanas veidotājs](./media/er-components-inspections-09b.png)

13. Formāta struktūras kokā pievienojiet tālāk norādītos krājumus, lai ģenerētu izejošo dokumentu XML formātā, kas satur informāciju par kreditoru.

    1. Pievienojiet saknes **Norādīšana** XML elementu.
    2. XML elementam **Norādīšana** pievienojiet ligzdoto XML elementu **Puse**.
    3. XML elementam **Puse** pievienojiet tālāk norādītos XML atribūtus.

        - Vārds, uzvārds
        - AccountNum

14. Saistiet formāta elementus ar nodrošinātajiem datu avotiem tālāk norādītajā veidā:

    - Saistiet formāta elementu **Norādīšana\\Puse\\Nosaukums** ar datu avota lauku **model.Vendor.Name**.
    - Saistiet formāta elementu **Norādīšana\\Puse\\AccountNum** ar datu avota lauku **model.Vendor.AccountNumber**.

15. Atlasiet **Validēt**, lai pārbaudītu rediģējamā formāta komponentu lapā **Formāta veidotājs**.

    ![Tādu formāta elementu validēšana, kas ir saistīti ar datu avotiem lapā Formāta veidotājs](./media/er-components-inspections-09c.png)

16. Ņemiet vērā, ka rodas validācijas kļūda. Ziņojumā norādīts, ka iespējams izpildlaikā tiek parādītas kļūdas konfigurētajos formāta komponentos **Statement\\Party\\Name** un **Statement\\Party\\AccountNum**, ja saraksts `model.Vendor` ir tukšs.

    ![Validācijas kļūdapar potenciālu kļūdu konfigurētajos formāta komponentos](./media/er-components-inspections-09d.png)

Tālāk redzamajā attēlā parādīta izpildlaika kļūda, kas rodas, ja ignorējat brīdinājumu, atlasāt **Palaist**, lai palaistu formātu, un atlasāt neeksistējoša kreditora konta numuru. Tā kā pieprasītais kreditors nepastāv, saraksts `model.Vendor` būs tukšs (tajā nebūs ierakstu).

![Izpildlaika kļūdas, kas radās formāta kartēšanas izpildes laikā](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a>Automātisks risinājums

Atlasītajai rindai cilnes **Brīdinājumi** režģī varat atlasīt **Atsaistīt**. Saistījums, kas norādīts kolonnā **Ceļš**, tiek automātiski noņemts no formāta elementiem.

### <a name="manual-resolution"></a>Manuāls risinājums

#### <a name="option-1"></a>1. opcija

Varat saistīt formāta elementu **Statement\\Party\\Name** ar datu avota krājumu `model.Vendor`. Izpildlaikā šis saistījums vispirms izsauc datu avotu `model.Vendor`. Kad `model.Vendor` atpakaļsūta tukšu ierakstu sarakstu, ligzdotie formāta elementi netiek palaisti. Tāpēc šai formāta konfigurācijai nav neviena validācijas brīdinājuma.

![Formāta element saistīšana ar datu avota krājumu lapā Formāta veidotājs](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a>2. opcija

Mainiet saistījumu formāta elementā **Statement\\Party\\Name** no `model.Vendor.Name` uz `FIRSTORNULL(model.Vendor).Name`. Atjauninātais saistījums nosacīti konvertē datu avota `model.Vendor` pirmo ierakstu, kam ir **Ierakstu saraksts** veids, uz jaunu **Ieraksts** veida datu avotu. Šis jaunais datu avots satur tādu pašu lauku kopu.

- Ja datu avotā `model.Vendor` ir pieejams vismaz viens ieraksts, šī ieraksta lauki tiek aizpildīti ar pirmā ieraksta lauku vērtībām datu avotā `model.Vendor`. Šādā gadījumā atjauninātais saistījums atpakaļsūta kreditora nosaukumu.
- Pretējā gadījumā katrs izveidotā ieraksta lauks tiek aizpildīts ar noklusējuma vērtību šī lauka datu veidam. Šādā gadījumā tiek atpakaļsūtīta tukša virkne kā datu veida **Virkne** noklusējuma vērtība.

Tādējādi nav validācijas brīdinājumu par formāta elementu **Statement\\Party\\Name**, ja tas ir saistīts ar izteiksmi `FIRSTORNULL(model.Vendor).Name`.

![Mainīts saistījums atrisina validācijas brīdinājumus lapā Formāta veidotājs](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a>3. opcija

Ja vēlaties skaidri norādīt datus, kas tiek ievadīti ģenerētajā dokumentā, ja datu avots `model.Vendor` ar veidu **Ierakstu saraksts** nenosūta atpakaļ nevienu ierakstu (šajā piemērā teksts **Nav pieejams**), mainiet saistījumu formāta elementam **Statement\\Party\\Name** no `model.Vendor.Name` uz `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`. Var izmantot arī izteiksmi `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.

### <a name="additional-consideration"></a><a id="i9a"></a>Papildu apsvērums

Pārbaude arī brīdina par citu iespējamu problēmu. Pēc noklusējuma, saistot formāta elementus **Statement\\Party\\Name** un **Statement\\Party\\AccountNum** ar atbilstošiem laukiem datu avotā `model.Vendor` ar veidu **Ierakstu saraksts**, šie saistījumi tiks palaisti un tie paņems atbilstošo lauku vērtības no pirmā ieraksta datu avotā `model.Vendor`, ja šis saraksts nav tukšs.

Tā kā formāta elements **Statement\\Party** nav saistīts ar datu avotu `model.Vendor`, elements **Statement\\Party** formāta izpildes laikā netiks atkārtots katram datu avota `model.Vendor` ierakstam. Tā vietā ģenerētais dokuments tiks aizpildīts ar informāciju tikai no pirmā ieraksta ierakstu sarakstā, ja šajā sarakstā ir vairāki ieraksti. Tādējādi var rasties problēma, ja formāts ir paredzēts, lai ģenerēto dokumentu aizpildītu ar informāciju par visiem kreditoriem no datu avota `model.Vendor`. Lai labotu šo problēmu, saistiet elementu **Statement\\Party** ar datu avotu `model.Vendor`.

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a>Izteiksmes ar FILTER funkciju izpildāmība (kešdarbe)

Vairākas iebūvētās ER funkcijas, ietverot [FILTER](er-functions-list-filter.md) un [ALLITEMSQUERY](er-functions-list-allitemsquery.md), tiek izmantots, lai piekļūtu pieteikumu tabulām, skatiem vai datu entītijām, veicot vienu SQL izsaukumu, lai iegūtu vajadzīgos datus kā ierakstu sarakstu. **Ierakstu saraksts** veida datu avots tiek izmantots kā katras no šo funkciju argumentiem un norāda izsaukuma pieteikuma avotu. ER pārbauda, vai var tikt izveidots tiešais SQL izsaukums uz datu avotu, kas ir norādīts vienā no šīm funkcijām. Ja nevar tikt izveidots tiešs izsaukums, jo datu avots ir apzīmēts kā [saglabāts kešatmiņā](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), ER modeļa kartēšanas veidotājā rodas validācijas kļūda. Ziņojumā, ko saņemat, norādīts, ka ER izteiksmi, kas satur vienu no šīm funkcijām , nevar palaist izpildlaikā.

Tālāk norādītajās darbībās parādīts, kā šī problēma varētu rasties.

1. Sāciet konfigurēt ER modeļa kartēšanas komponentu.
2. Pievienojiet **Dynamics 365 for Operations \\ Tabulas ieraksti** veida datu avotu.
3. Piešķiriet jaunajam datu avotam nosaukumu **Kreditors**. Laukā **Tabula** atlasiet **VendTable**, lai norādītu, ka šis datu avots pieprasīs VendTable tabulu.
4. Pievienojiet **Vispārīgi \\ Lietotāja ievades parametrs** veida datu avotu, lai uzmeklētu kreditora kontu izpildlaika dialoglodziņā.
5. Piešķiriet jaunajam datu avotam nosaukumu **RequestedAccountNum**. Laukā **Etiķete** ievadiet **Kreditora konta numurs**. Laukā **Operāciju datu veida nosaukums** atstājiet noklusējuma vērtību **Apraksts**.
6. Pievienojiet **Aprēķinātais lauks** veida datu avotu, lai filtrētu kreditoru, par kuru veikts vaicājums.
7. Piešķiriet jaunajam datu avotam nosaukumu **FilteredVendor** un konfigurējiet to, lai tas ietvertu izteiksmi `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
8. Atzīmējiet konfigurēto datu avotu **Kreditors** kā saglabātu kešatmiņā.

    ![Modeļa kartēšanas komponenta konfigurēšana lapā Modeļa kartēšanas veidotājs](./media/er-components-inspections-10a.gif)

9. Atlasiet **Validēt**, lai pārbaudītu rediģējamā modeļa kartēšanas komponentu lapā **Modeļa kartēšanas veidotājs**.

    ![FILTRA funkcijas validēšana, kas tiek lietota kešatmiņā saglabātā kreditora datu avotam lapā modeļa kartēšanas veidotājs](./media/er-components-inspections-10a.png)

10. Ņemiet vērā, ka rodas validācijas kļūda. Ziņojumā norādīts, ka funkciju **FILTER** nevar lietot kešatmiņā saglabātajam datu avotam **Kreditors**.

Tālāk redzamajā attēlā parādīta izpildlaika kļūda, kas rodas, ja ignorējat brīdinājumu un atlasāt **Palaist**, lai palaistu formātu.

![Izpildlaika kļūda, kas rodas, palaižot formāta kartēšanu lapā Formāta veidotājs](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a>Automātisks risinājums

Nav pieejama opcija automātiski novērst šo problēmu.

### <a name="manual-resolution"></a>Manuāls risinājums

#### <a name="option-1"></a>1. opcija

Noņemiet karodziņu **Kešatmiņa** no datu avota **Kreditors**. Tad datu avots **FilteredVendor** kļūs izpildāms, bet datu avotam **Kreditors**, uz kuru dota atsauce tabulā VendTable, tiks veikta piekļuve katru reizi, kad tiek izsaukts datu avots **FilteredVendor**.

#### <a name="option-2"></a>2. opcija

Mainiet datu avota **FilteredVendor** izteiksmi no `FILTER(Vendor, Vendor.AccountNum="US-101")` uz `WHERE(Vendor, Vendor.AccountNum="US-101")`. Šādā gadījumā datu avotam **Kreditors**, uz kuru dota atsauce tabulā VendTable, tiks veikta piekļuve tikai, pirmo reizi izsaucot datu avotu **Kreditors**. Tomēr ierakstu atlase tiks veikta atmiņā. Tāpēc šī pieeja var izraisīt sliktu veiktspēju.

## <a name="missing-binding"></a><a id="i11"></a>Trūkst saistījuma

Konfigurējot ER formāta komponentu, bāzes ER datu modelis tiek piedāvāts kā noklusējuma datu avots ER formātam. Kad tiek palaists konfigurētais ER formāts, bāzes modeļa [noklusējuma modeļa kartēšana](er-country-dependent-model-mapping.md) tiek izmantota, lai aizpildītu datu modeli ar pieteikuma datiem. ER formāta veidotājs parāda brīdinājumu, ja formāta elements tiek saistīts ar datu modeļa krājumu, kas nav saistīts ar nevienu datu avotu modeļa kartēšanā, kas ir pašlaik atlasīta kā noklusējuma modeļa kartēšana rediģējamajam formātam. Šo saistījuma veidu nevar palaist izpildlaikā, jo palaistais formāts nevar aizpildīt saistīto elementu ar pieteikuma datiem. Tādējādi izpildlaikā rodas kļūda.

Tālāk norādītajās darbībās parādīts, kā šī problēma varētu rasties.

1. Sāciet vienlaicīgi konfigurēt ER datu modeli, ER modeļa kartēšanu un ER formāta komponentus.
2. Datu modeļa kokā pievienojiet saknes krājumu, kura nosaukums ir **Root3**.
3. Modificējiet krājumu **Root3**, pievienojot jaunu **Ierakstu saraksts** veida ligzdoto krājumu.
4. Piešķiriet jaunajam ligzdotajam krājumam nosaukumu **Kreditors**.
5. Modificējiet krājumu **Kreditors** tālāk norādītajā veidā.

    - Pievienojiet **Virkne** veida ligzdoto lauku un piešķiriet tam nosaukumu **Nosaukums**.
    - Pievienojiet **Virkne** veida ligzdoto lauku un piešķiriet tam nosaukumu **AccountNumber**.

    ![Ligzdoto lauku pievienošana kreditora krājumam lapā Datu modelis](./media/er-components-inspections-11a.png)

6. Modeļa kartēšanas veidotāja rūtī rūtī **Datu avoti** pievienojiet veida **Dynamics 365 for Operations \\ Tabulas ieraksti** datu avotu.
7. Piešķiriet jaunajam datu avotam nosaukumu **Kreditors**. Laukā **Tabula** atlasiet **VendTable**, lai norādītu, ka šis datu avots pieprasīs VendTable tabulu.
8. Pievienojiet **Vispārīgi \\ Lietotāja ievades parametrs** veida datu avotu, lai vaicātu par kreditora kontu izpildlaika dialoglodziņā.
9. Piešķiriet jaunajam datu avotam nosaukumu **RequestedAccountNum**. Laukā **Etiķete** ievadiet **Kreditora konta numurs**. Laukā **Operāciju datu veida nosaukums** atstājiet noklusējuma vērtību **Apraksts**.
10. Pievienojiet **Aprēķinātais lauks** veida datu avotu, lai filtrētu kreditoru, par kuru veikts vaicājums.
11. Piešķiriet jaunajam datu avotam nosaukumu **FilteredVendor** un konfigurējiet to, lai tas ietvertu izteiksmi `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Saistiet datu modeļa krājumus ar konfigurētajiem datu avotiem tālāk norādītajā veidā.

    - Saistiet **FilteredVendor** ar **Kreditors**.
    - Saistiet **FilteredVendor.AccountNum** ar **Vendor. AccountNumber**.

    > [!NOTE]
    > Datu modeļa lauks **Vendor.Name** paliek nesaistīts.

    ![Datu modeļa krājumi, kas saistīti ar konfigurētajiem datu avotiem un datu režīma krājumu, kas paliek nesaistīti lapā Modeļa kartēšanas veidotājs](./media/er-components-inspections-11b.png)

13. Formāta struktūras kokā pievienojiet tālāk norādītos krājumus, lai ģenerētu izejošo dokumentu XML formātā, kas satur informāciju par kreditoriem, par kuriem veikts vaicājums.

    1. Pievienojiet saknes **Norādīšana** XML elementu.
    2. XML elementam **Norādīšana** pievienojiet ligzdoto XML elementu **Puse**.
    3. XML elementam **Puse** pievienojiet tālāk norādītos XML atribūtus:

        - Vārds, uzvārds
        - AccountNum

14. Saistiet formāta elementus ar nodrošinātajiem datu avotiem tālāk norādītajā veidā.

    - Saistiet formāta elementu **Statement\\Party** ar datu avota krājumu `model.Vendor`.
    - Saistiet formāta elementu **Norādīšana\\Puse\\Nosaukums** ar datu avota lauku **model.Vendor.Name**.
    - Saistiet formāta elementu **Norādīšana\\Puse\\AccountNum** ar datu avota lauku **model.Vendor.AccountNumber**.

15. Atlasiet **Validēt**, lai pārbaudītu rediģējamā formāta komponentu lapā **Formāta veidotājs**.

    ![ER formāta komponenta validācija lapā Formāta veidotājs](./media/er-components-inspections-11c.png)

16. Ņemiet vērā, ka notiek brīdinājums par validāciju. Ziņojumā norādīts, ka datu avota lauks **model.Vendor.Name** nav saistīts ar nevienu datu avotu modeļa kartēšanā, kas konfigurēta izmantošanai formātā. Tādējādi formāta elements **Statement\\Party\\Name** var nebūt aizpildīts izpildlaikā, un var rasties izņēmums izpildlaikā.

    ![ER formāta komponenta validācija lapā Formāta veidotājs](./media/er-components-inspections-11d.png)

Tālāk redzamajā attēlā parādīta izpildlaika kļūda, kas rodas, ja ignorējat brīdinājumu un atlasāt **Palaist**, lai palaistu formātu.

![Rediģējamā formāta palaišana lapā Formāta veidotājs](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a>Automātisks risinājums

Nav pieejama opcija automātiski novērst šo problēmu.

### <a name="manual-resolution"></a>Manuāls risinājums

#### <a name="option-1"></a>1. opcija

Modificējiet konfigurēto modeļa kartēšanu, pievienojot saistījumu datu avota laukam **model.Vendor.Name**.

#### <a name="option-2"></a>2. opcija

Modificējiet konfigurēto formātu, noņemot saistījumu formāta elementam **Norādīšana\\Puse\\Nosaukums**.

## <a name="not-linked-template"></a><a id="i12"></a>Nav saistīta veidne

Ja [manuāli](er-fillable-excel.md#manual-entry) konfigurējat ER formāta komponentu, lai izmantotu veidni izejošā dokumenta ģenerēšanai, ir manuāli jāpievieno elements **Excel\\Fails**, jāpievieno vajadzīgā veidne kā rediģējamā komponenta pielikums un jāatlasa šis pielikums pievienotajā elementā **Excel\\Fails**. Šādā veidā norādīsiet, ka pievienotais elements aizpildīs atlasīto veidni izpildlaikā. Konfigurējot formāta komponenta versiju **Melnraksts** [statusā](general-electronic-reporting.md#component-versioning), varat pievienot vairākas veidnes rediģējamam komponentam un pēc tam atlasīt katru veidni elementā **Excel\\Fails**, lai palaistu ER formātu. Šādā veidā varat redzēt, kā dažādas veidnes tiek aizpildītas izpildlaikā. Ja jums ir veidnes, kas nav atlasītas nevienā elementā **Excel\\Fails**, ER formāta veidotājs brīdina, ka šīs veidnes tiks dzēstas no rediģējamās ER formāta komponentu versijas, kad tās statuss tiek mainīts no **Melnraksts** uz **Pabeigts**.

Tālāk norādītajās darbībās parādīts, kā šī problēma varētu rasties.

1. Sāciet konfigurēt ER formāta komponentu.
2. Formāta struktūras kokā pievienojiet elementu **Excel\\Fails**.
3. Tikko pievienotajam elementam **Excel\\Fails** pievienojiet kā pielikumu Excel darbgrāmatas failu **A.xlsx**. Izmantojiet dokumenta veidu, kas konfigurēts [ER parametros](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents), lai norādītu ER formāta veidņu krātuvi.
4. Tikko pievienotajam elementam **Excel\\Fails** pievienojiet kā pielikumu citu Excel darbgrāmatas failu **B.xlsx**. Izmantojiet to pašu dokumenta veidu, kas izmantots darbgrāmatas failā A.
5. Elementā **Excel\\Fails** atlasiet darbgrāmatas failu A.
6. Atlasiet **Validēt**, lai pārbaudītu rediģējamā formāta komponentu lapā **Formāta veidotājs**.

    ![Darbgrāmatas faila rediģējamā formāta komponenta validācija lapā Formāta veidotājs](./media/er-components-inspections-12a.gif)

7. Ņemiet vērā, ka notiek brīdinājums par validāciju. Ziņojumā norādīts, ka darbgrāmatas fails B. xlsx nav saistīts ar nevienu komponentu un ka tas tiks noņemts pēc konfigurācijas versijas statusa maiņas.

### <a name="automatic-resolution"></a>Automātisks risinājums

Nav pieejama opcija automātiski novērst šo problēmu.

### <a name="manual-resolution"></a>Manuāls risinājums

Modificējiet konfigurēto formātu, noņemot visas veidnes, kas nav saistītas ar nevienu elementu **Excel\\Fails**.

## <a name="not-synced-format"></a><a id="i13"></a>Nav sinhronizēts formāts

Ja [konfigurējat](er-fillable-excel.md) ER formāta komponentu, lai izmantotu Excel veidni izejošā dokumenta ģenerēšanai, varat manuāli pievienot elementu **Excel\\Fails**, pievienot vajadzīgo veidni kā rediģējamā komponenta pielikumu un atlasīt šo pielikumu pievienotajā elementā **Excel\\Fails**. Šādā veidā norādīsiet, ka pievienotais elements aizpildīs atlasīto veidni izpildlaikā. Tā kā pievienotā Excel veidne ir ārēji izstrādāta, rediģējamais ER formāts var saturēt Excel nosaukumus, kas nav iekļauti pievienotajā veidnē. ER formāta veidotājs brīdina par jebkādām neatbilstībām starp ER formāta elementu rekvizītiem, kas atsaucas uz nosaukumiem, kas nav iekļauti pievienotajā Excel veidnē.

Tālāk norādītajās darbībās parādīts, kā šī problēma varētu rasties.

1. Sāciet konfigurēt ER formāta komponentu.
2. Formāta struktūras kokā pievienojiet **Excel\\Fails** elementu **Pārskats**.
3. Tikko pievienotajam elementam **Excel\\Fails** pievienojiet kā pielikumu Excel darbgrāmatas failu **A.xlsx**. Izmantojiet dokumenta veidu, kas konfigurēts [ER parametros](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents), lai norādītu ER formāta veidņu krātuvi.

    > [!IMPORTANT]
    > Pārliecinieties, vai pievienotajā Excel darbgrāmatā nav ietverts nosaukums **ReportTitle**.

4. Pievienojiet **Excel\\Šūna** elementu **Virsraksts** kā elementa **Pārskats** ligzdoto elementu. Laukā **Excel diapazons** ievadiet **ReportTitle**.
5. Atlasiet **Validēt**, lai pārbaudītu rediģējamā formāta komponentu lapā **Formāta veidotājs**.

    ![Ligzdoto elementu un lauku validācija lapā Formāta veidotājs](./media/er-components-inspections-13a.png)

6. Ņemiet vērā, ka notiek brīdinājums par validāciju. Ziņojumā norādīts, ka nosaukums **ReportTitle** nepastāv izmantotajā Excel veidnes lapā **Lapa1**.

    ![Brīdinājums par validāciju, ka nosaukums ReportTitle nepastāv Excel veidnes Lapa1](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a>Automātisks risinājums

Nav pieejama opcija automātiski novērst šo problēmu.

### <a name="manual-resolution"></a>Manuāls risinājums

#### <a name="option-1"></a>1. opcija

Modificējiet konfigurēto formātu, noņemot visus elementus, kas atsaucas uz Excel nosaukumiem, kuru nav veidnē.

#### <a name="option-2"></a>2. opcija

[Atjauniniet](er-fillable-excel.md#template-import) rediģējamo ER formātu, importējot Excel veidni. Rediģējamā ER formāta struktūra tiks [sinhronizēta](modify-electronic-reporting-format-reapply-excel-template.md) ar importētās Excel veidnes struktūru.

### <a name="additional-consideration"></a>Papildu apsvērums

Lai uzzinātu, kā formāta struktūru var sinhronizēt ar ER veidni [Biznesa dokumentu pārvaldnieka](er-business-document-management.md) veidņu redaktorā, skatiet [Biznesa dokumenta veidnes struktūras atjaunināšana](er-bdm-update-structure.md).

## <a name="not-synced-with-a-word-template-format"></a><a id="i14"></a>Nav sinhronizēts ar Word veidnes formātu

Ja [konfigurējat](er-fillable-excel.md) ER formāta komponentu, lai izmantotu Word veidni izejošā dokumenta ģenerēšanai, varat manuāli pievienot elementu **Excel\\Fails**, pievienot vajadzīgo Word veidni kā rediģējamā komponenta pielikumu un atlasīt šo pielikumu pievienotajā elementā **Excel\\Fails**.

> [!NOTE]
> Kad Word dokuments ir pievienots, ER formāta veidotājs piedāvā rediģējamu elementu kā **Word\\failu**.

Šādā veidā norādīsiet, ka pievienotais elements aizpildīs atlasīto veidni izpildlaikā. Tā kā pievienotā Word veidne ir ārēji izstrādāta, rediģējamais ER formāts var saturēt atsauces uz Word satura vadīklām, kas nav iekļautas pievienotajā veidnē. ER formāta veidotājs brīdina par jebkādām neatbilstībām starp ER formāta elementu rekvizītiem, kas atsaucas uz satura vadīklām, kas nav iekļautas pievienotajā Word veidnē.

Piemēru, kas parāda, kā šī problēma var notikt, skatiet sadaļā [Rediģējamā formāta konfigurēšana, lai likvidētu kopsavilkuma sadaļu](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control).

### <a name="automatic-resolution"></a>Automātisks risinājums

Nav pieejama opcija automātiski novērst šo problēmu.

### <a name="manual-resolution"></a>Manuāls risinājums

#### <a name="option-1"></a>1. opcija

Modificējiet konfigurēto formātu, dzēšot formulu **Noņemts** formāta elementā, kas ir minēts pārbaudes brīdinājumā.

#### <a name="option-2"></a>2. opcija

Modificējiet Word veidnes izmantošanu, [pievienojot](er-design-configuration-word-suppress-controls.md#tag-control) nepieciešamo tagu atbilstošajai Word satura vadīklai.

## <a name="no-default-mapping"></a><a id="i15"></a>Nav noklusējuma kartējuma

Kad ir veikta [trūkstošās saistīšanas](#i11) pārbaude, pārbaudītie formātu saistījumi tiek novērtēti attiecībā uz atbilstošo modeļa kartēšanas komponentu saistījumiem. Tā kā varat importēt [vairākas](./tasks/er-manage-model-mapping-configurations-july-2017.md) ER modeļa kartēšanas konfigurācijas uz jūsu Finance instanci, un katra konfigurācija var ietvert piemērojamo modeļa kartēšanas komponentu, viena konfigurācija ir jāatlasa kā noklusējuma konfigurācija. Pretējā gadījumā, mēģinot palaist, rediģēt vai validēt pārbaudīto ER formātu, rodas izņēmums, un saņemsit šādu ziņojumu: "Vairāk nekā viens modeļa kartējums pastāv \<model name (root descriptor)\> datu modelim konfigurācijās \<configuration names separated by comma\>. Iestatiet vienu no konfigurācijām kā noklusējumu."

Piemēru, kas parāda, kā šī problēma var notikt un kā to var labot, skatiet sadaļā [Vairāku atvasināto kartējumu pārvaldība viena modeļa saknei](er-multiple-model-mappings.md).

## <a name="inconsistent-setting-of-header-or-footer-components"></a><a id="i16"></a>Nesaskaņoti galvenes vai kājenes komponentu iestatījumi

Kad [konfigurējat](er-fillable-excel.md) ER formāta komponentu, lai izmantotu Excel veidni izejošā dokumenta ģenerēšanai, varat pievienot komponentu **Excel\\Galvene**, lai darblapas augšā aizpildītu Excel darbgrāmatas virsrakstus. Varat arī pievienot komponentu **Excel\\Kājene**, lai aizpildītu kājenes darblapas apakšdaļā. Katram pievienotajam **Excel\\Galvene** vai **Excel\\Kājene** ir jāiestata rekvizīts **Galvenes/kājenes izskats**, lai precizētu lapas, kurām komponents tiek palaists. Tā kā varat konfigurēt vairākus komponentus **Excel\\Galvene** vai **Excel\\Kājene** vienam komponentam **Lapa** un varat ģenerēt dažādas galvenes vai kājenes dažādiem lapu veidiem Excel darblapā, ir jākonfigurē viens **Excel\\Galvene** vai **Excel\\Kājene** komponents rekvizīta **Galvene/kājenes izskats** specifiskai vērtībai. Ja vairāk nekā viens komponents **Excel\\Galvene** vai **Excel\\Kājene** ir konfigurēts noteiktai rekvizīta **Galvenes/kājenes izskats**, rodas validācijas kļūda un tiek parādīts šāds kļūdas ziņojums: "Galvenes/kājenes (&lt;komponenta veids: galvene vai kājene&gt;) nesakrīt."

### <a name="automatic-resolution"></a>Automātisks risinājums

Nav pieejama opcija automātiski novērst šo problēmu.

### <a name="manual-resolution"></a>Manuāls risinājums

#### <a name="option-1"></a>1. opcija

Modificējiet konfigurēto formātu, dzēšot vienu no neatbilstošajiem komponentiem **Excel\\Galvene** vai **Excel\\Kājene**.

#### <a name="option-2"></a>2. opcija

Modificējiet rekvizīta **Galvenes/kājenes izskats** vērtību vienam no neatbilstošajiem komponentiem **Excel\\Galvene** vai **Excel\\Kājene**.

## <a name="additional-resources"></a>Papildu resursi

[ALLITEMS ER funkcija](er-functions-list-allitems.md)

[ALLITEMSQUERY ER funkcija](er-functions-list-allitemsquery.md)

[INT64VALUE ER funkcija](er-functions-conversion-int64value.md)

[INTVALUE ER funkcija](er-functions-conversion-intvalue.md)

[FILTER ER funkcija](er-functions-list-filter.md)

[WHERE ER funkcija](er-functions-list-where.md)

[Datu avotu JOIN izmantošana , lai iegūtu datus no vairākām pieteikumu tabulām ER modeļa kartēšanā](er-join-data-sources.md)

[Elektronisko atskaišu veidošanas (ER) formāta failu izpildes uzraudzīšana, lai novērstu veiktspējas problēmas](trace-execution-er-troubleshoot-perf.md)

[Biznesa dokumentu pārvaldības pārskats](er-business-document-management.md)

[Word satura vadīklu likvidēšana ģenerētajos pārskatos](er-design-configuration-word-suppress-controls.md)

[Vairāku atvasināto kartējumu pārvaldība viena modeļa saknei](er-multiple-model-mappings.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
