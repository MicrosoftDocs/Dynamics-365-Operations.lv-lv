---
title: Elektronisko pārskatu konfigurāciju izstrāde, lai aizpildītu PDF veidnes
description: Šajā tēmā ir sniegta informācija par elektronisko pārskatu (Electronic reporting — ER)formāta izstrādi, lai aizpildītu PDF veidni.
author: NickSelin
manager: AnnBe
ms.date: 04/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 96426ce54ec1b37c6751d990503d95960c2913df
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771310"
---
# <a name="design-er-configurations-to-fill-in-pdf-templates"></a>Elektronisko pārskatu konfigurāciju izstrāde, lai aizpildītu PDF veidnes

[!include[banner](../includes/banner.md)]

Šajā tēmā minētās procedūras ir piemēri, kas parāda, kā lietotājs, kura loma i r**Sistēmas administrators** vai **Elektroniskā pārskata izstrādātājs**, lomā var konfigurēt elektronisko pārskatu (ER) formātu, kas ģenerē pārskatus kā PDF failus, izmantojot aizpildāmus PDF dokumentus kā pārskatu veidnes. Šīs darbības var veikt jebkurā uzņēmumā, kas izmanto Dynamics 365 Finance vai Regulatory Configuration Service (RCS).

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat, jums ir nepieciešams kāds no tālāk minētajiem piekļuves veidiem atkarībā no pakalpojuma, ko izmantojat šajā tēmā aprakstīto procedūru pabeigšanai.

- Piekļuve Finance vienai no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

- Piekļuve pakalpojumam RCS vienai no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

Ir jāizpilda arī procedūra [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).

Visbeidzot jums ir jālejupielādē tālāk norādītie faili lapā [CustomerSource](https://go.microsoft.com/fwlink/?linkid=874111).

| Satura apraksts                       | Faila nosaukums                                     |
|-------------------------------------------|-----------------------------------------------|
| Pārskata pirmās lapas veidne | [IntrastatReportTemplate1.pdf](https://mbs.microsoft.com/Files/public/CS)                  |
| Pārskata pārējo lapu veidne    | [IntrastatReportTemplate2.pdf](https://mbs.microsoft.com/Files/public/CS/AX/IntrastatReportTemplate2.pdf)                  |
| Parauga ER formāts — PDF                          | [Intrastat report (PDF).version.1.1.xml](https://mbs.microsoft.com/Files/public/CS/AX/IntrastatreportPDFversion11.xml)        |
| Parauga ER formāts — Excel                          | [Intrastat (import from Excel).version.1.1.xml](https://mbs.microsoft.com/Files/public/CS/AX/IntrastatimportfromExcelversion11.xml) |
| Parauga datu kopa                            | [Intrastat sample data.xlsx](https://mbs.microsoft.com/Files/public/CS/AX/Intrastatsampledata.xlsx)                    |

## <a name="design-the-format-configuration"></a>Formāta konfigurācijas noformēšana

### <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Iegūt piekļuvi korporācijas Microsoft nodrošināto konfigurāciju sarakstam

1. Dodieties uz **Organizācijas administrēšana \> Darbvietas \> Elektronisko atskaišu veidošana**.
2. Pārbaudiet, vai pakalpojuma sniedzējs **Litware, Inc** ir pieejams un atzīmēts kā aktīvs.
3. **Microsoft** nodrošinātāja elementā atlasiet **Repozitoriji**.

    > [!NOTE]
    > Ja ir jau izveidots **LCS** tipa repozitorijs, izlaidiet atlikušās šīs procedūras darbības.

4. Atlasiet **Pievienot**.
5. Nolaižamajā dialoglodziņā lauku grupā **Konfigurācijas repozitorija tips** atlasiet opciju **LCS**.
6. Atlasiet **Izveidot repozitoriju**.
7. Atlasiet **Labi**.

### <a name="get-the-model-configurations-provided-by-microsoft"></a>Piekļuve korporācijas Microsoft nodrošinātajām modeļu konfigurācijām

1. Lapas **Konfigurācijas repozitoriji** kreisajā pusē atlasiet pogu **Rādīt filtrus** (piltuves simbols).
2. Pievienojiet filtru **LCS** vērtībai laukā **Tips** un lietojiet operatoru **sākas ar**.
3. Atlasiet **Lietot**.
4. Atlasiet **Atvērt**.
5. Kokā atlasiet **Intrastat modelis**.
6. Kopsavilkuma cilnē **Versijas** atlasiet versiju **1**.

    > [!NOTE]
    > Ja poga **Importēt** kopsavilkuma cilnē **Versijas** nav pieejama, izlaidiet atlikušās šīs procedūras darbības.

7. Atlasiet **Importēt**.
8. Atlasiet **Jā**, lai apstiprinātu atlasītās **Intrastat modelis** modeļa konfigurācijas versijas importēšanu.

### <a name="create-a-new-format-configuration"></a>Jaunas formāta konfigurācijas izveide

1. Darbvietā **Elektroniskie pārskati** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
2. Kokā atlasiet **Intrastat modelis**.
3. Atlasiet **Izveidot konfigurāciju**.

    > [!NOTE]
    > Ja poga **Izveidot konfigurāciju** nav pieejama, ir jāieslēdz noformējuma režīms lapā **Elektronisko pārskatu veidošanas parametri**, ko var atvērt no darbvietas **Elektroniskie pārskati**.

4. Nolaižamajā dialoglodziņā lauku grupā **Jauns** atlasiet opciju **Formāts pamatojoties uz datu modeli Intrastat**.
5. Laukā **Nosaukums** ievadiet **Intrastat pārskats (PDF)**.
6. Laukā **Apraksts** ievadiet **Intrastat pārskats PDF formātā**.

    > [!NOTE]
    > Tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs. Šis nodrošinātājs varēs uzturēt šo konfigurāciju. Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.

7. Pēc izvēles: laukā **Formāta tips** varat atlasīt noteiktu elektroniskā dokumenta formātu. Ja atlasāt **PDF**, noformēšanas laikā ER operāciju veidotājs piedāvās tikai tādus formāta elementus, kas ir piemēroti tikai dokumentiem, kas tiek ģenerēti PDF formātā **(PDF\Fails**, **PDF\PDF apvienotājs** utt.). Ja atstājat šo lauku tukšu, ER operāciju veidotājā noformēšanas laikā tiek norādīts elektroniskā dokumenta formāts, kad tiks pievienots pirmais formāta elements. Piemēram, ja kā pirmo formāta elementu pievienosit **Excel\File**, ER operāciju veidotājs piedāvās tikai tādus formāta elementus, kas ir piemēroti tikai dokumentiem, kas tiek ģenerēti Excel formātā (**Excel\Cell**, **Excel\Range** utt.). formāts.
8. Atlasiet **Izveidot konfigurāciju**.

Tiek izveidota jauna ER formāta konfigurācija. Varat izmantot šīs konfigurācijas melnraksta versiju, lai saglabātu ER formāta komponentu, kas izstrādāts elektronisko dokumentu ģenerēšanai PDF formātā.

### <a name="design-the-format-of-an-electronic-document"></a>Elektroniskā dokumenta formāta noformēšana

Pēc tam jūsu izveidotajā ER formāta konfigurācijā jūs izstrādāsit ER formātu, kas ģenerē pārskatu **Intrastat kontrole** PDF formātā. Šī pārskata pirmajā lapā ir jābūt pārskata kopsavilkumam un detalizētai informācijai par ārējās tirdzniecības transakcijām, kas iekļautas pārskatā. Pārējās lapās ir jāuzrāda tikai detalizēta informācija par ārējās tirdzniecības transakcijām, kas iekļautas pārskatā. Tā kā ģenerētajām pārskata lapām ir jābūt ar dažādiem izkārtojumiem, ER formātā tiks izmantotas divas dažādas veidnes PDF formātā.

Jebkurā PDF skatītājā atveriet lejupielādētās PDF veidnes. Ņemiet vērā, ka katrā veidnē ir vairāki lauki, kas jāaizpilda. Katrā veidnē detalizēta informācija par ārējās tirdzniecības transakcijām ir norādīta kā 42 rindas, un katrai no tām ir deviņi lauki. Rindas numurs tiek norādīts katra lauka nosaukuma beigās (piemēram, **Datums 1**...**Datums 42** un **Prece 1**...**Prece 42**).

Tālāk redzamajā attēla ir pārskata pirmās lapas PDF veidne.

![1. veidne](media/rcs-ger-filloutpdf-template1.png)

Tālāk redzamajā attēla ir pārskata pārējo lapu PDF veidne.

![2. veidne](media/rcs-ger-filloutpdf-template2.png)

1. Lapā **Konfigurācijas** atlasiet **Veidotājs**.
2. Atlasiet **Pievienot sakni**.
3. Nolaižamajā dialoglodziņā, kas atrodas kokā, atlasiet **PDF \> PDF apvienotājs**.

    Kad tiek atlasīts elements **PDF apvienošana** kā formāta saknes elements, visi izpildes laikā ģenerētie PDF dokumenti tiks sapludināti vienā gala PDF dokumentā. Ja ir nepieciešama tikai viena PDF veidne, lai ģenerētu visus vajadzīgos dokumentus, lietojot jūsu noformēto ER formātu, varat atlasīt opciju **PDF fails** kā saknes elementu.

4. Laikā **Nosaukums** ievadiet **Izvade**.
5. Laukā **Valodas preferences** atlasiet **Lietotāja preference**. Pārskats tiks ģenerēts tā lietotāja vēlamajā valodā, kurš to izpilda.
6. Laukā **Kultūras preferences** atlasiet **Lietotāja preference**. Pārskata lapās parādītās vērtības un datumi tiks formatēti, pamatojoties uz vēlamo tā lietotāja lokalizāciju, kurš izpilda pārskatu.
7. Atlasiet **Labi**.
8. Darbību rūts cilnē **Importēšana** atlasiet **Importēt no PDF**.

    Kad aizpildāms PDF dokuments tiek importēts kā veidne šim ER formātam, visi pieprasītie ER formāta elementi (**PDF fails**, **Lauku grupa**un **Lauks**) tiek automātiski izveidoti formātā, kas ir izstrādāts, pamatojoties uz importējamā PDF dokumenta struktūru.

9. Atlasiet **Pārlūkot**. Dodieties uz failu **IntrastatReportTemplate1. PDF**, ko lejupielādējāt agrāk kā priekšnosacījumu, un atlasiet to.
10. Atlasiet **Labi**.

    Atlasītais fails tiek ielādēts, un tiek aizpildīts lauks **Veidne** dialoglodziņā **Importēt no PDF**.

11. Atlasiet opcijai **Grupas lauki** iestatījumu **Jā**. Ja atlasītajā PDF dokumentā ir jebkādas lauku grupas, tās tiks izmantotas, lai grupētu izveidotos ER formāta elementus. Šim nolūkam tiks izveidots formāta elements **Lauku grupa**.

    Ja šī opcija ir iestatīta kā **Nē**, nepieciešamie ER formāta elementi tiks izveidoti kā plakans elementu saraksts, kas tiek ligzdots zem izveidotā formāta elementa **PDF fails**.

12. Atlasiet **Labi**.

    ![Dialoglodziņš Importēt no PDF](media/rcs-ger-filloutpdf-importtemplate.png)

13. Kokā izvērsiet opciju **Izvade**.

    Ņemiet vērā, ka komponents **PDF fails** ir izveidots automātiski, lai pārvaldītu tās pārskata pirmās lapas izveidi, kas tiek ģenerēta izpildes laikā.

14. Kokā izvērsiet opciju **Izvade \> PDF fails**.

    Ņemiet vērā, ka šajā ER formātā ir automātiski izveidots strukturēts formāta elementu saraksts, pamatojoties uz aizpildāmā PDF dokumenta struktūru, ko importējāt iepriekš.

15. Kokā atlasiet opciju **Izvade \> PDF fails**.
16. Laikā **Nosaukums** ievadiet **1. lapa**.

    Šis formāta elements tiks izmantots, lai ģenerētu pārskata **Intrastat kontrole** pirmo lapu. Šajā lapā tiks parādīts pārskata kopsavilkums un detalizēta informācija par ārējās tirdzniecības transakcijām.

    Ja lauks **Valodas preferences** tiks atstāts tukšs, iestatījums **Valodas preferences** (galvenais elements **PDF apvienotājs**) noteiks tā pārskata valodu, kas tiek ģenerēts, izmantojot šo formāta elementu. Varat atlasīt citu vērtību, lai ignorētu galvenā elementa iestatījumu.

    Ja lauks **Kultūras preferences** tiks atstāts tukšs, iestatījums **Kultūras preferences** (galvenais elements **PDF apvienotājs**) noteikts tā pārskata lokalizāciju, kas tiek ģenerēts, izmantojot šo formāta elementu. Lokalizācija nosaka vērtību un datumu formātu pārskata lapās. Varat atlasīt citu vērtību, lai ignorētu galvenā elementa iestatījumu.

17. Darbības rūtī atlasiet cilni **Importēt**. Ņemiet vērā, ka atlasītajam formāta elementam **PDF fails** ir kļuvusi pieejama poga **Atjaunināt no PDF faila**.

    Varat izmantot šo pogu, lai importētu atjaunināto PDF veidni rediģētajā formātā. Kad tiek importēta atjauninātā PDF veidne, atbilstoši tiek mainīts formātu elementu saraksts:

    - Visiem jaunajiem laukiem atjauninātajā PDF veidnē tiek veidoti jauni formāta elementi rediģētā ER formātā.
    - Ja atjauninātajā PDF veidnē vairs nav iekļauti lauki, kas atbilst visiem esošajiem formāta elementiem rediģētajā ER formātā, šie formāta elementi tiek dzēsti no ER formāta.

18. Cilnē **Formāts** atlasiet **Pielikumi**.

    Ņemiet vērā, ka importētais PDF dokuments ir pievienots rediģētajam ER formātam.

    ![PDF pielikuma priekšskatīšana](media/rcs-ger-filloutpdf-attachedtemplate.png)

19. Turpiniet noformēt šo formātu, importējot otro PDF veidni, pievienojot nepieciešamos saistījumus datu avotiem un tā tālāk.
20. Atlasiet **Saglabāt**.
21. Aizvērt lapu.
22. Atlasiet **Dzēst**.
23. Atlasiet **Jā**.

Lai uzzinātu, kā izmantot jaunus formāta elementus **PDF apvienotājs**, **PDF fails**, **Lauka grupa** un **Lauks** dokumentu ģenerēšanai PDF formāta, varat importēt un analizēt parauga ER formātu.

### <a name="import-the-format-configuration"></a>Formāta konfigurācijas importēšana

Pēc tam importējiet parauga ER formātu, ko iepriekš lejupielādējāt, lai ģenerētu pārskatu **Intrastat kontrole** PDF formātā. pārskata pirmajā lapā ir jābūt pārskata kopsavilkumam un detalizētai informācijai par ārējās tirdzniecības transakcijām, kas iekļautas pārskatā. Pārējās lapās ir jāuzrāda tikai detalizēta informācija par ārējās tirdzniecības transakcijām, kas iekļautas pārskatā.

1. Lapā **Konfigurācijas** atlasiet **Mainīt \> Ielādēt no XML faila**.
2. Atlasiet **Pārlūkot**. Dodieties uz failu **Intrastat report (PDF).version.1.1.xml**, ko lejupielādējāt agrāk kā priekšnosacījumu, un atlasiet to.
3. Atlasiet **Labi**.

## <a name="analyze-the-format-configuration"></a>Formāta konfigurācijas analīze

### <a name="format-layout"></a>Formāta izkārtojums

1. Koka lapā **Konfigurācijas** atlasiet **Intrastat modelis \> Intrastat pārskats (PDF)**.
2. Atlasiet **Noformētājs**.
3. Atlasiet **Rādīt detalizētu informāciju**.
4. Kokā izvērsiet opciju **Izvade: PDF apvienotājs**.

    Ņemiet vērā, ka šis ER formāts satur divus elementus **PDF fails**, un katrs izmanto citu PDF veidni. Viena veidne tiek izmantota, lai ģenerētu pārskata pirmo lapu PDF formātā, un otru veidni izmanto, lai ģenerētu citas lapas.

5. Kokā izvērsiet opciju **Izvade: PDF apvienotājs \> 1. lapa: PDF fails (IntrastatReportTemplate1)**.
6. Kokā izvērsiet opciju **Izvade: PDF apvienotājs \> N. lapa: PDF fails (IntrastatReportTemplate2)**.

    Ņemiet vērā, ka, tā kā abu PDF veidņu saturs atšķiras, abu elementu **PDF fails** ligzdoto formāta elementu struktūra atšķiras.

### <a name="format-mapping"></a>Formāta kartēšana

1. Lapā **Formāta veidotājs** atlasiet cilni **Kartēšana**.
2. Kokā izvērsiet sadaļu **Lapošana \> Lapas**.

    ![Formulas veidotāja lapa, kurā ir izvērsts modeļa koks](media/rcs-ger-filloutpdf-reviewformat.png)

    Ņemiet vērā tālāk norādīto informāciju.

    - Formāta elements **Izvade \> 1. lapa** (tips **PDF fails**) nav piesaistīts nevienam datu avotam, un šī formāta elementa izteiksme **Iespējots** ir tukša. Tāpēc izpildes laikā PDF veidne **IntrastatReportTemplate1** tiks aizpildīta tikai vienu reizi, kad tiek ģenerēts atsevišķs PDF dokuments.
    - Formāta elements **Izvade \> N. lapa** (tips **PDF fails**) ir piesaistīts tipa **Ierakstu saraksts** datu avotam **Paging.PageN**, un šī formāta elementa izteiksme **Iespējots** ir tukša. Tāpēc izpildes laikā PDF veidne **IntrastatReportTemplate2** tiks aizpildīta katram ierakstam no piesaistīto ierakstu saraksta, kad tiek ģenerēts atsevišķs PDF dokuments.
    - Tā kā formāta elementi **1. lapa: PDF fails** un **N. lapa:: PDF fails** ir formāta elementa **Izvade: PDF apvienotājs** atvasinātie elementi, visi aizpildītie PDF dokumenti tiks sapludināti vienā gala PDF dokumentā.
    - Datu avoti **Paging.Page1** un **Paging.PageN** tiek konfigurēti kā datu avota **Paging.Pages** ierakstu filtri. Šis datu avots ir konfigurēts, lai sadalītu visu ārējās tirdzniecības transakciju kopumu partijās. Katrā no partijām ietverts līdz 42 ierakstiem. Transakciju sadalīšanai partijās tiek izmantota šāda ER izteikmse:

        SPLITLIST(Totals.CommodityRecord,42)

    - Datu avotā **Paging.Pages** ir elements **Paging.Pages.Enumerated**, kas atgriež detalizēto informāciju par katru partijā iekļauto ierakstu. Šajā detalizētajā informācijā ir iekļauta ieraksta secība pašreizēja partijā (lauks **Paging.Pages.Enumerated.Number**). Lauks **Paging.Pages.Enumerated.Number** tiek izmantots formāta elementu **PDF lauks** izteiksmē **Nosaukums**, lai dinamiski ģenerētu lauka nosaukumu, kas ir balstīts uz transakcijas numuru partijā. Pēc tam ģenerētais lauka nosaukums tiek izmantots, lai aizpildītu atbilstošo PDF lauku izmantotajā PDF veidnē.
    - Formāta elements **Izvade \> N. lapa \> 2. detalizēta informācija** (tips **PDF grupa**) ir piesaistīts datu avotam **Paging.PageN.Enumerated** (vai **\@.Enumerated**, ja tiek izmantots skatīšanas režīms **Relatīvais ceļš**), kura tips ir **Ierakstu saraksts**. Tāpēc izpildes laikā šīs PDF grupas ligzdotie elementi tiks aizpildīti katram ierakstam no piessaistīto ierakstu saraksta. Tādējādi tiek virtuāli ģenerētas atsevišķas PDF rindas, kad katram N. no 42. ierakstiem sarakstā **Paging.PageN.Enumerated** tiek aizpildīti šādi PDF lauki: Datums N, Virziens N, Prece N utt. Tātad šajā ziņā formāta elementa **Lauka grupa** uzvedība līdzinās formāta elementu **XML \> Secība** un **Teksts \> Secība** uzvedībai.

3. Kokā izvērsiet sadaļu **Izvade \> N. lapa \> Details2**.
4. Kokā atlasiet **Izvade \> N. lapa \> Details2 \> PageFooter**.

    Ņemiet vērā, ka šī formāta elementa atribūts **Nosaukums** ir definēts kā **PageFooter.** Ņemier vērā arī, ka formāta elementa izteiksme **Nosaukums** ir tukša.

5. Kokā atlasiet **Izvade \> N. lapa \> Details2 \> 1. labojums**.

    Ņemiet vērā, ka šī formāta elementa atribūts **Nosaukums** ir definēts kā **1. labojums.** Ņemiet arī vērā, ka formāta elementa izteiksme **Nosaukums** ir definēta kā **Paging.FldName("Correction",\@.Number)**.

![Formāta veidotājs, kurā ir atlasīta kartēšana](media/rcs-ger-filloutpdf-reviewformat2.png)

Ņemiet vērā, ka formāta elements **Lauks** tiek izmantots, lai aizpildītu aizpildāma PDF dokumenta atsevišķu lauku, un šis dokuments ir definēts kā galvenais formāta elements **PDF fails**. Formāta elementa **PDF fails** vai tā ligzdotu elementu saistījums, ja tam ir ligzdoti elementi, norāda vērtību, kas ievadīta atbilstošajos PDF laukos. Dažādus formāta elementa **Lauks** rekvizītus var izmantot, lai norādītu, kurš PDF lauks tiek aizpildīts ar atsevišķu formāta elementu.

- Cilnē **Formāts**: formāta elementa atribūts **Nosaukums**
- Cilnē **Kartēšana**: formāta elementa izteiksme **Nosaukums**

Tā kā abi rekvizīti ir neobligāti formāta elementam **Lauks**, tiek lietotas tālāk minētās kārtulas, lai norādītu mērķa PDF lauku.

- Ja atribūts **Nosaukums** ir tukšs un izteiksme **Nosaukums** izpildes laikā atgriež tukšu virkni, izpildes laikā tiek parādīts izņēmums, lai paziņotu lietotājam, ka nevar atrast PDF lauku PDF veidnē , kas tiek izmantota, lai aizpildītu PDF dokumentu.
- Ja atribūts **Nosaukums** ir definēts un izteiksme **Nosaukums** ir tukša, tiek aizpildīts PDF lauks, kam ir tāds pats nosaukums kā formāta elementa atribūtam **Nosaukums**.
- Ja atribūts **Nosaukums** ir definēts un izteiksme **Nosaukums** ir konfigurēta, tiek aizpildīts PDF lauks, kam ir tāds pats nosaukums kā vērtībai, ko atgriež formāta elementa izteiksme **Nosaukums**.

> [!NOTE]
> PDF izvēles rūtiņu PDF var aizpildīt atlasot tālāk norādītajos veidos.
>
> - Ja atbilstošais formāta elements **Lauks** ir saistīts ar **Būla** datu tipa datu avota lauku, kam ir vērtība **True**
> - Ja atbilstošais formāta elements **Lauks** satur ligzdotu formāta elementu **Virkne**, kas ir saistīts ar datu avota lauku, kura teksta vērtība ir **1**, **True** vai **Jā**

## <a name="run-the-format-configuration"></a>Formāta konfigurācijas izpilde

### <a name="import-the-format-configuration"></a>Formāta konfigurācijas importēšana

Pēc tam ielādējiet parauga ER formātu **Intrastat (importēt no Excel)**. Šis formāts ir izveidots, lai parsētu lietotāja atlasīto Microsoft Excel darbgrāmatu, kas simulē ārējās tirdzniecības transakcijas.

1. Lapā **Konfigurācijas** atlasiet **Mainīt \> Ielādēt no XML faila**.
2. Atlasiet **Pārlūkot**. Dodieties uz failu **Intrastat (import from Excel).version.1.1.xml**, ko lejupielādējāt agrāk kā priekšnosacījumu, un atlasiet to.
3. Atlasiet **Labi**.
4. Kokā atlasiet **Intrastat modelis \> Intrastat (importēt no Excel)**.
5. Atlasiet **Rediģēt**.
6. Iestatiet opciju **Noklusējums modeļu kartēšanai** kā **Jā**.

    > [!NOTE]
    > Ja iepriekš iestatījāt opciju **Noklusējums modeļu kartēšanai** kā **Jā** konfigurācijai **Intrastat modelis** vai citai konfigurācijai, kas ligzdota zem konfigurācijas **Intrastat modelis**, iestatiet šo opciju kā **Nē**.

    Kad opcija **Noklusējums modeļu kartēšanai** ir iestatīta kā **Jā**, importētais ER formāts **Intrastat (importēt no Excel)** tiek piešķirts kā noklusējuma datu avots formāta konfigurācijai **Intrastat pārskats (PDF)**. Kad tiek palaista formāta **Intrastat pārskats (PDF)** konfigurācija, tās Excel darbgrāmatas saturs, ko parsē ER formāts **Intrastat (importēt no Excel)**, simulēs pārskatā iekļaujamās ārējās tirdzniecības transakcijas. Šajā attēlā parādīts Excel darbgrāmatas piemērs.

    ![Excel darbgrāmata ar parauga datiem](media/rcs-ger-filloutpdf-excelworkbook.png)

### <a name="run-the-format-configuration"></a>Formāta konfigurācijas izpilde

1. Koka lapā **Konfigurācijas** atlasiet **Intrastat modelis \> Intrastat pārskats (PDF)**.
2. Atlasiet **Izpildīt**.
3. Atlasiet **Pārlūkot**. Dodieties uz failu **Intrastat sample data.xlsx**, ko lejupielādējāt agrāk kā priekšnosacījumu, un atlasiet to.
4. Atlasiet **Labi**.
5. Laukā **Pārskata virziens** atlasiet **Abi**, lai aizpildītu visas transakcijas no importētās Excel darbgrāmatas ģenerētajā PDF pārskatā.
6. Atlasiet **Labi**.
7. Pārskatiet ģenerēto PDF dokumentu.

Tālāk redzamajā attēlā ir parādīts ģenerēta pārskata pirmās lapas piemērs.

![Ģenerētā pārskata pirmā lapa](media/rcs-ger-filloutpdf-generatedreport.png)

Tālāk redzamajā attēlā ir parādīts ģenerēta pārskata citas lapas piemērs.

![Ģenerētā pārskata cita lapa](media/rcs-ger-filloutpdf-generatedreport2.png)

## <a name="additional-resources"></a>Papildu resursi

- [ER Izveidot konfigurāciju pārskatu ģenerēšanai formātā OPENXML (2016. gada maijs)](tasks/er-design-reports-openxml-2016-11.md)
- [ER konfigurāciju noformēšana pārskatu ģenerēšanai Word formātā](tasks/er-design-configuration-word-2016-11.md)
