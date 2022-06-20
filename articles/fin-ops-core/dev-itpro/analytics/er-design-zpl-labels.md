---
title: Jauna elektronisko pārskatu risinājuma izveide ZPL etiķešu izdrukāšanas nolūkā
description: Šajā rakstā skaidrots, kā projektēt jaunu elektronisko pārskatu (ER) risinājumu Etiķešu programmēšanas valodas (ZPL) etiķešu drukāšanai.
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: f861fe63c6d7d00d0a9f84d33c0d1b1b23735b61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845720"
---
# <a name="design-a-new-er-solution-to-print-zpl-labels"></a>Jauna elektronisko pārskatu risinājuma izveide ZPL etiķešu izdrukāšanas nolūkā

[!include [banner](../includes/banner.md)]


Šajā rakstā skaidrots, kā lietotājs Sistēmas administratora, [elektronisko pārskatu izstrādātāja vai elektronisko pārskatu funkcionālā konsultanta loma var konfigurēt elektronisko pārskatu (ER)](general-electronic-reporting.md) struktūras parametrus, projektēt nepieciešamās ER konfigurācijas jauna ER [risinājumam, lai piekļūtu noliktavas pārvaldības sistēmas datiem un ģenerētu pielāgotas noliktavas vietas etiķetes Vaibras programmēšanas](general-electronic-reporting.md#Configuration) valodā (ZPL) II formātā. Šīs darbības var veikt uzņēmumā **USRT**.

## <a name="business-scenario"></a>Biznesa scenārijs

Jūs pārstāvat uzņēmumu, kas ieviesis noliktavas pārvaldību Microsoft Dynamics 365 Finanšu gadā. Katrai noliktavas vietai ir jābūt iezīmētai ar pašpiegādības etiķeti, kurā ir svītrkods. Noliktavas darbinieki izmantos rokas svītrkoda lasītājus, lai skenētu svītrkodus.

Visas noliktavu vietas ir iezīmētas pirmstvēruma aktivitāšu jomā. Tomēr jums ir jābūt iespējai pēc pieprasījuma drukāt arī noliktavas vietas etiķetes, ja esošās etiķetes tiek bojātas vai notiek noliktavas novietojuma konfigurēšana. Izmantojot nesen izlaisto ER funkcionalitāti, varat konfigurēt jaunu ER risinājumu, kas noliktavas supervizoram ļauj izdrukāt etiķetes tieši uz etiķešu printeri.

## <a name="configure-the-er-framework"></a>ER struktūras konfigurēšana

Izpildiet sadaļā [ER struktūras konfigurēšana](er-quick-start2-customize-report.md#ConfigureFramework) norādītās darbības, lai iestatītu ER parametru minimālo kopu. Šis iestatījums ir jāpabeidz, pirms sākat lietot ER struktūru jauna ER risinājuma izstrādei.

## <a name="design-a-domain-specific-data-model"></a>Domēnam specifiska datu modeļa izveide

Izveidojiet jaunu ER konfigurāciju, kas ietver [datu modeļa](er-overview-components.md#data-model-component) komponentu noliktavas pārvaldības domēnam. Šis datu modelis tiks izmantots kā datu avots vēlāk, kad izveidosiet ER formātu, lai ģenerētu noliktavas vietas etiķetes.

### <a name="import-a-data-model-configuration"></a>Datu modeļa konfigurācijas importēšana

Izpildiet šīs darbības, lai importētu nepieciešamo datu modeli no Microsoft nodrošinātā XML faila. Alternatīvi var izveidot savu datu modeli, kā aprakstīts nākamajā sadaļā.

1. Lejupielādējiet [failu Noliktavas modelis.version.1.xml](https://download.microsoft.com/download/9/f/1/9f136e9b-bf5f-403a-b089-a2b2ed1da2ba/Warehouse-model.version.1.xml) un saglabājiet lokālajā datorā.
2. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
3. Darbvietā **Elektroniskie pārskati** atlasiet **Pārskatu veidošanas konfigurācijas**.
4. **Konfigurācijas lapā Darbību** rūtī atlasiet Maiņas **noslodze** \> **no XML faila.**
5. Atlasiet **Pārlūkot**, pēc tam atrodiet un atlasiet failu **Noliktavas modelis.version.1.xml**.
6. Atlasiet **Labi**, lai importētu konfigurāciju.

![Importētā ER datu modeļa konfigurācija konfigurāciju lapā.](./media/er-design-zpl-labels-imported-model.png)

### <a name="create-a-data-model-configuration"></a>Datu modeļa konfigurācijas izveide

Tā vietā, lai importētu Microsoft nodrošināto datu modeļa failu, jūs varat izveidot datu modeli no fragmenta. Piemēram, ja tiek parādīts, kā pabeigt šo uzdevumu, skatiet lauku [Jauna datu modeļa konfigurācijas izveide](er-quick-start1-new-solution.md#DesignDataModel).

### <a name="review-the-data-model"></a>Pārskatīt datu modeli

Konfigurētā datu modeļa rediģējamu versiju var skatīt datu modeļu veidotāja **lapā**.

![ER datu modeļa struktūra datu modeļu veidotāja lapā.](./media/er-design-zpl-labels-model.png)

## <a name="design-a-model-mapping-for-the-configured-data-model"></a>Konfigurētā datu modeļa kartēšanas izveidošana

Kā lietotājam elektronisko pārskatu izstrādātāja lomā jāizveido jauna ER [konfigurācija, kas ietver modeļa kartēšanas](er-overview-components.md#model-mapping-component) komponentu noliktavas datu modelim. Šis komponents ievieš konfigurēto datu modeli dynamics 365 finansēm un ir specifisks šai programmai. Tas jākonfigurē, lai norādītu programmas objektus, kas tiks izmantoti, lai izpildlaikā aizpildītu konfigurēto datu modeli ar programmas datiem. Lai pabeigtu šo uzdevumu, jums ir jāsaprot, kā noliktavas pārvaldības biznesa domēna datu struktūra tiek īstenota finansēs.

### <a name="import-a-model-mapping-configuration"></a>Modeļa kartēšanas konfigurācijas importēšana

Izpildiet šīs darbības, lai importētu nepieciešamo modeļa kartēšanu no Microsoft nodrošinātā XML faila. Alternatīvi var izveidot savu modeļa kartēšanu, kā aprakstīts nākamajā sadaļā.

1. Lejupielādējiet [noliktavas modeļa kartējumu.version.1.1.xml](https://download.microsoft.com/download/1/c/c/1cc94d28-3d90-4ffd-a118-77d6c322904f/Warehouse-model-mapping.version.1.1.xml) failu un saglabājiet to lokālajā datorā.
2. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
3. Darbvietā **Elektroniskie pārskati** atlasiet **Pārskatu veidošanas konfigurācijas**.
4. **Konfigurācijas lapā Darbību** rūtī atlasiet Maiņas **noslodze** \> **no XML faila.**
5. Atlasiet **Pārlūkot**, pēc tam atrodiet un atlasiet noliktavas modeļa **kartēšanas.version.1.1.xml** failu.
6. Atlasiet **Labi**, lai importētu konfigurāciju.

![Importētā ER modeļa kartēšanas konfigurācija konfigurāciju lapā.](./media/er-design-zpl-labels-imported-mapping.png)

### <a name="create-a-model-mapping-configuration"></a>Modeļa kartēšanas konfigurācijas izveide

Tā vietā, lai importētu Microsoft nodrošināto modeļa kartēšanas failu, modeļa kartēšanu varat izveidot no fragmenta. Piemēram, ja tiek parādīts, kā pabeigt šo uzdevumu, skatiet sadaļu [Jauna modeļa kartēšanas konfigurācijas izveide](er-quick-start1-new-solution.md#CreateModelMapping).

### <a name="review-the-model-mapping"></a>Pārskatīt modeļa kartēšanu

Konfigurētā modeļa kartēšanas rediģējamu versiju var skatīt modeļu kartēšanas **veidotāja** lapā.

![ER modeļa kartēšanas struktūra modeļu kartēšanas veidotāja lapā.](./media/er-design-zpl-labels-mapping.png)

## <a name="design-a-format"></a>Formāta veidošana

Kā lietotājs Elektroniskās ziņošanas funkcionālā konsultanta lomā jums ir jāizveido jauna ER konfigurācija, kas ietver [formāta](er-overview-components.md#format-component) komponentu. Lai konfigurētu šo komponentu, izmantosiet ZPL II kodu, lai norādītu noliktavas vietas etiķetes izkārtojumu.

### <a name="import-a-format-configuration"></a>Importēt formāta konfigurāciju

Izpildiet šīs darbības, lai importētu nepieciešamo formātu no Microsoft nodrošinātā XML faila. Alternatīvi var izveidot savu formātu, kā aprakstīts nākamajā sadaļā.

1. Lejupielādējiet [failu Noliktavas vietas iezīmes.version.1.1.xml](https://download.microsoft.com/download/5/7/5/5758b551-69a5-45bd-a2b2-21c3db73a6fc/Warehouse-location-labels.version.1.1.xml) un saglabājiet to lokālajā datorā.
2. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
3. Darbvietā **Elektroniskie pārskati** atlasiet **Pārskatu veidošanas konfigurācijas**.
4. **Konfigurācijas lapā Darbību** rūtī atlasiet Maiņas **noslodze** \> **no XML faila.**
5. Atlasiet **Pārlūkot**, pēc tam atrodiet un atlasiet failu **Noliktavas vietas iezīmes.version.1.1.xml**.
6. Atlasiet **Labi**, lai importētu konfigurāciju.

![Importēt ER formāta konfigurāciju lapā Konfigurācijas.](./media/er-design-zpl-labels-imported-format.png)

### <a name="create-a-format-configuration"></a>Formāta konfigurācijas izveide

Tā vietā, lai importētu Microsoft nodrošināto formāta failu, varat izveidot formātu no jauna. Piemēram, ja tiek parādīts, kā pabeigt šo uzdevumu, skatiet sadaļu [Jauna formāta konfigurācijas izveide](er-quick-start1-new-solution.md#FormatCreate).

### <a name="review-the-format"></a>Pārskatīt formātu

Konfigurētā formāta rediģējamu versiju varat skatīt formāta veidotāja **lapā**.

![ER formāta struktūra formāta veidotāja lapā.](./media/er-design-zpl-labels-format.png)

Šī `model.Location.Label` formāta datu avots ir konfigurēts, lai ģenerētu iezīmes, kas satur šādu informāciju:

- Noliktavas nosaukums kā teksts
- Noliktavas nosaukums kā svītrkods
- Atrašanās vietas nosaukums
- Kontrolcipari

**Formulas veidotāja** lapā datu avotam ER formula`CONCATENATE`, kas tiek izmantota iezīmju ģenerēšanai, ietver funkciju, kas apvieno informāciju vēlamajā izkārtojumā.

![Formula datu avotam formulas veidotāja lapā.](./media/er-design-zpl-labels-review-formula.png)

> [!TIP]
> Etiķešu izkārtojums ir veidots tā, lai vietas nosaukums un kontrolcipari būtu saskaņoti iezīmes centrā. Tomēr ZPL II neatbalsta centra līdzinājumu svītrkodiem. Tāpēc datu avota formula `model.Location.Warehouse.Alignment` tiek izmantota, lai saskaņotu svītrkodu iezīmes centrā. Šī formula aprēķina svītrkoda kreiso nobīdi, pamatojoties uz rakstzīmju skaitu noliktavas nosaukumā.

## <a name="prepare-your-environment-for-previewing-generated-labels"></a>Sagatavojiet vidi ģenerēto iezīmju priekšskatīšanasm

Tālāk sniegtajā piemērā ZPL etiķetēm tiek izmantota printera paradītā programma, lai ekrānā parādītu ģenerēto iezīmju priekšskatījumu. Izpildiet šīs darbības, lai aktivizētu šo opciju.

1. Pievienojiet printera [ER](er-destination-type-print.md) mērķi **noliktavas** vietas etiķetes ER formātam un konfigurējiet to [, lai nosūtītu ģenerētās iezīmes no finansēm uz dokumentu maršrutēšanas aģentu (DRA).](install-document-routing-agent.md)
2. Instalējiet un konfigurējiet DRA, lai maršrutēt ģenerētās etiķetes no Finansēm uz lokālo printeri, kas ir pieejams no pašreizējās darbstacijas.
3. Pievienojiet pašreizējai darbstacijai lokālo printeri un konfigurējiet to, lai ģenerētās etiķetes no DIK būtu printera programma.
4. Instalējiet printera programma kā hroma pārlūkprogrammas paplašinājumu un konfigurējiet to, lai ģenerētās etiķetes no lokālā printera ieturēs tīmekļa pakalpojumā, kas renderēs ģenerētās etiķetes un atgriezīs tās printera paralēlā priekšskatījumā.

<table>
<tbody>
<tr align="center">
<td>
<p>Finance</p>
<p>ER pārskats</p>
<p>Printera mērķis</p>
</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from Finance to the DRA."></td>
<td>Dokumentu maršrutēšanas aģents</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from the DRA to a local printer."></td>
<td>Lokālais printeris</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from a local printer to a printer emulator."></td>
<td>Printera modulis</td>
<td><img src="./media/er-design-zpl-labels-flow2.png" alt="Data flow direction: from a printer emulator to a rendering web service and then back to the printer emulator."></td>
<td>Renderēt tīmekļa pakalpojumu</td>
</td>
</tr>
</tbody>
</table>

### <a name="install-and-configure-a-printer-emulator-application"></a>Instalēt un konfigurēt printera iepriekšējs pieteikums

Pievienojiet printera programma ZPL renderēšanas programmai jūsu Chrome tīmekļa pārlūkam. Šajā piemērā tiek izmantots [Zpl printera](https://chrome.google.com/webstore/detail/zpl-printer/phoidlklenidapnijkabnfdgmadlcmjo) modulis, kas ir balstīts uz [ZPL etiķešu tīmekļa pakalpojumu](http://labelary.com/service.html). Printera programma izies ģenerētās etiķetes ZPL formātā no lokālā printera uz tīmekļa pakalpojumu un pēc tam atgriezīs etiķetes kā PDF vai PNG failus priekšskatījumā.

1. Pārlūka interneta veikalā atrodiet un atlasiet printera moduli, kuru vēlaties izmantot. Pēc tam atlasiet **Pievienot Pārlūkam Chrome**, lai pievienotu to Pārlūkam Chrome.

    ![Printera programmas pievienošana Hroma interneta pārlūkprogrammai no Hroma tīmekļa veikala.](./media/er-design-zpl-labels-add-app.png)

2. Atlasiet **palaist programmu,** lai darbinātu printera programma no Hroma tīmekļa pārlūkprogrammas.

    ![Printera programma tiek darbināta no pārlūkprogrammas Chrome.](./media/er-design-zpl-labels-run-app.png)

3. Konfigurēt palaisto programmu:

    1. Izslēdziet programmu.
    2. Printera iestatījumos iestatiet resursdatoru uz **127.0.0.1**.
    3. Iestatiet portu uz **9100**.

        ![Printera iepriekšējs lietojumprogrammas konfigurēšana.](./media/er-design-zpl-labels-configure-app.png)

    4. Ieslēpiet pieteikumu atpakaļ. Ir jāsaņem ziņojums, ka printeris tika startēts norādītajā resursdatorā un portā.

        ![Printera modulis ir ieslēgts atpakaļ.](./media/er-design-zpl-labels-turn-on-app.png)

> [!NOTE]
> Tā kā šajā piemērā izmantotā printera programma balstās uz tīmekļa pakalpojumu, lai atveidotu etiķetes, pārliecinieties, vai drošības iestatījumi ļauj jums komunicēt ar pakalpojumu. Pretējā gadījumā programma nesaņems atveidotās iezīmes, un šo iezīmju priekšskatījums nebūs pieejams.

### <a name="add-and-configure-a-local-printer"></a>Lokālā printera pievienošana un konfigurēšana

[Pievienojiet jaunu lokālo printeri, ko](https://support.microsoft.com/windows/install-a-printer-in-windows-10-cc0724cf-793e-3542-d1ff-727e4978638b) var izmantot pašreizējai ierīcei, lai no DĀR izietu ģenerētās iezīmes uz printera iepriekš izveidoto programmu.

1. Operētājsistēmā Windows atlasiet Sākt iestatījumu **ierīču** \> **·** \> **printeru** \> **skenerus.\&**
2. Atlasiet printeru **skeneru \& iestatījumus**.
3. Lai **pievienotu printeri vai skeneri**, atlasiet **Pievienot ierīci**.
4. Nav **uzskaitīts nevēlaties printerim**, un atlasiet **Pievienot manuāli**.
5. Laukā **Atrast printeri pēc citām opcijām** atlasiet Pievienot lokālo printeri **vai tīkla printeri ar manuāliem iestatījumiem**.
6. Laukā **Izvēlēties printera portu** atlasiet Izveidot **jaunu portu un pēc** tam veiciet tālāk aprakstītās darbības.

    1. **Porta tipa laukā** atlasiet standarta **TCP/IP portu**.
    2. Hostdatora **nosaukuma vai IP adreses** laukā ievadiet **127.0.0.1**.
    3. Laukā **Porta nosaukums** ievadiet **ZPL**.
    4. Uzgaidiet, līdz **tiek pabeigta tcp/IP porta** noteikšanas operācija.
    5. Laukā **Ierīces veids** atlasiet Pielāgots **un** pēc tam atlasiet **Iestatījumi**.
    6. Pārliecinieties, vai ir norādīti šādi porta iestatījumi:

        - **Porta nosaukums:** ZPL
        - **Printera nosaukums vai IP adrese:** 127.0.0.1
        - **Protokols: neapstrādāts**
        - **Porta numurs:** 9100

7. Laukā **Instalēt printera draiveri** atlasiet Tikai **vispārīgs/teksts**.
8. Laukā **Printera nosaukums** ievadiet **SiabraPrinter**.

![Lokālā printera pievienošana pašreizējai ierīcei.](./media/er-design-zpl-labels-configure-printer.png)

### <a name="install-and-configure-the-dra"></a>Instalēt un konfigurēt DIK

Sagatavojiet DRA, lai padotu ģenerētās etiķetes no finansēm uz konfigurēto lokālo printeri.

1. [Instalējiet DĀR](install-document-routing-agent.md#install-the-document-routing-agent).
2. [Konfigurējiet DĀR](install-document-routing-agent.md#configure-the-document-routing-agent).
3. [Reģistrējiet lokālo printeri](install-document-routing-agent.md#register-network-printers) DIK.
4. [Aktivizējiet lokālo printeri](install-document-routing-agent.md#administer-network-printers) finanšu vidē.

![TIEK sagatavots DDR, lai drukātu ģenerētās etiķetes.](./media/er-design-zpl-labels-configure-dra.png)

### <a name="configure-the-er-destination"></a>Konfigurēt ER adresātu

Sagatavojiet ER mērķi, lai padotu ģenerētās etiķetes no Finansēm uz DRA.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektroniskie pārskati** \> **Elektroniskās pārskatu veidošanas adresāts**.
2. **Elektronisko pārskatu adresāta** lapas Darbību rūtī atlasiet **Jauns**.
3. **Atsauces laukā** atlasiet Noliktavas vietas **etiķetes**.
4. Kopsavilkuma cilnē **Faila adresāts** atlasiet **Jauns**.
5. Laukā **Nosaukums** ievadiet **Iezīmes**.
6. Laukā **Faila komponenta nosaukums** atlasiet **Pārskats**.
7. Atlasiet **Iestatījumi**.
8. **Dialoglodziņa Mērķa iestatījumi** cilnē Printeris **iestatiet** opciju Iespējots **uz** **Jā**.
9. Laukā **Printera nosaukums** atlasiet **SiabraPrinter**.
10. Laukā **Dokumentu maršrutēšanas** veids izvēlieties **ZPL**.
11. Atlasiet **Labi**.

![ER adresāta konfigurēšana noliktavas vietas iezīmju formātam elektronisko pārskatu adresāta lapā.](./media/er-design-zpl-labels-configure-destination.png)

## <a name="review-warehouse-locations"></a>Pārskatīt noliktavas novietojumus

1. Pārejiet uz **noliktavas pārvaldības iestatīšanas** \> **noliktavas** \> **novietojumiem.** \> **·**
2. Vietu lapā **filtrējiet**, lai skatītu tikai vietas, kurām ir vērtība **laukā Kontrolcipari**.

![Pārskatiet noliktavas atrašanās vietas lapā Atrašanās vietas.](./media/er-design-zpl-labels-review-locations.png)

## <a name="print-warehouse-location-labels"></a>Drukāt noliktavas vietu etiķetes

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Konfigurācijas lapas **konfigurācijas** kokā izvērsiet Noliktavas modelis **un atlasiet Noliktavas** vietas **etiķetes**.
3. Darbību rūtī atlasiet **Palaist**.
4. Dialoglodziņā Elektroniskā **pārskata parametri** cilnē Iekļauja **ietvertie ieraksti** atlasiet **Filtrēt**.
5. Cilnē Diapazons **atrodiet** rindu, kur tabulas lauks **ir** iestatīts uz Vietas **, un** lauks **Lauks** ir iestatīts uz Atrašanās **vietu**. Laukā **Kritēriji ievadiet** LPEnabled **·**.
6. Atlasiet **Labi**.
7. Atlasiet **Labi**. Etiķete tiek ģenerēta un parādīta priekšskatījuma lapā printera iepriekšējs pieteikumā.

![Pārskatot ģenerēto iezīmi Zpl printera lietotā priekšskatījuma lapā.](./media/er-design-zpl-labels-preview-label.png)

## <a name="modify-the-layout-of-a-label"></a>Iezīmes izkārtojuma modificēšana

Noliktavas vietas iezīmju pašreizējo izkārtojumu var mainīt. Šajā piemērā ir parādīts, kā mainīt izkārtojumu, lai ģenerētās etiķetes iekļautu atrašanās vietas profila ID.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Iestatiet lauku **Izmantot adresātus melnraksta statusa**[ER lietotāja parametram kā](electronic-reporting-destinations.md#applicability)**Jā**.
3. Konfigurācijas lapas **konfigurācijas** kokā izvērsiet Noliktavas modelis **un atlasiet Noliktavas** vietas **etiķetes**.
4. Atlasiet **Noformētājs**.
5. **Cilnes Kartēšana** lapā Formāta veidotājs **atlasiet** datu `model.Location.Label` avotu.
6. **Datu avota rekvizītu dialoglodziņā** atlasiet Rediģēt formulu.**·** \> **·**
7. Formulas **veidotāja** lapā formulas **laukā pārskatiet** ER formulu, kas tiek lietota iezīmju ģenerēšanas laikā.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^XZ")
    ```

8. Atjauniniet formulu, lai ģenerētām etiķetēm pievienotu atrašanās vietas profila ID.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^CF0,40,40^FO0,240^FB800,1,0,C,0^FD",@.ProfileID,"\&^FS",CrLf,
    "^XZ")
    ```

9. Atlasiet **Saglabāt**.
10. Atlasiet **Labi**.
11. Darbību rūtī atlasiet **Palaist**.
12. Dialoglodziņā Elektroniskā **pārskata parametri** cilnē Iekļauja **ietvertie ieraksti** atlasiet **Filtrēt**.
13. Cilnē Diapazons **atrodiet** rindu, kur tabulas lauks **ir** iestatīts uz Vietas **, un** lauks **Lauks** ir iestatīts uz Atrašanās **vietu**. Laukā **Kritēriji** ievadiet **Sia**.
14. Atlasiet **Labi**.
15. Atlasiet **Labi**. Etiķete tiek ģenerēta un parādīta priekšskatījuma lapā printera iepriekšējs pieteikumā.

![Pārskatiet ģenerēto iezīmi, kas ietver atrašanās vietas profila ID Zpl printera programma priekšskatījuma lapā.](./media/er-design-zpl-labels-preview-label2.png)

## <a name="encoding"></a>Kodēšana

> [!NOTE]
> Jums ir jāsinhronizē **Common\\File** komponenta kodēšanas iestatījums rediģējamā ER formātā un atbilstošās iezīmes atbilstošais iestatījums. **Common\\File** komponenta lauka Kodēšana **[...](er-suppress-bom-characters.md)** vērtībai nav jābūt pretrunā ar ZPL komandu, kas tiek izmantota iezīmes kodēšanas kontrolei (piemēram, komandai).`^CI` ER nepārbauda, vai šie iestatījumi ir sinhronizēti.

## <a name="additional-resources"></a>Papildu resursi

[Printera mērķis](er-destination-type-print.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
