---
title: "Pārskats par palīdzības sistēmu"
description: "Šajā rakstā ir sniegts apskats par Microsoft Dynamics 365 for Operations palīdzības sistēmas komponentiem. Tajā ir arī paskaidrots, kā savai organizācijai varat sniegt pielāgotu dokumentāciju un apmācību."
author: margoc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16381
ms.assetid: 018c148c-9cbd-41e0-8186-d75dbf66288f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6f785ac8b9a8be503bf9122f21716f745b17115b
ms.openlocfilehash: f08434b4c818460009644e77da1b37ba86cc1d54
ms.contentlocale: lv-lv
ms.lasthandoff: 04/27/2017


---

# <a name="help-overview"></a>Pārskats par palīdzības sistēmu

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegts apskats par Microsoft Dynamics 365 for Operations palīdzības sistēmas komponentiem. Tajā ir arī paskaidrots, kā savai organizācijai varat sniegt pielāgotu dokumentāciju un apmācību. 

Dynamics 365 for Operations ietver palīdzības sistēmu, kuras pamatā ir divi galvenie komponenti:

-   Dokumentācijas vietne
-   Uzdevumu ceļveži

Gan rakstiem, gan uzdevumu ceļvežiem varat piekļūt Dynamics 365 for Operations rūtī Palīdzība, kā tas ir redzams tālāk esošajā ekrānuzņēmumā. [![Rūts Palīdzība](./media/help-pane-ops-task-guides-1024x741.png)](./media/help-pane-ops-task-guides.png) Šajā rakstā ir aprakstīta palīdzības sistēma un paskaidrots, kā varat savai organizācijai izveidot pielāgotu dokumentāciju un apmācības resursus.

## <a name="help-on-docsmicrosoftcom"></a>Palīdzība vietnē docs.microsoft.com
Vietne docs.microsoft.com ([docs.microsoft.com/dynamics365/operations](/dynamics365/#pivot=solutions&panel=solutions_operations) ir galvenais Dynamics 365 for Operations produkta dokumentācijas avots. Vietnē ir pieejami tālāk norādītie līdzekļi.

-   **Piekļuve visjaunākajam saturam** — vietne nodrošina ātrāku un pielāgojamāku veidu, kā piegādāt un atjaunināt produkta dokumentāciju. Tāpēc tā palīdz garantēt, ka jums ir pieeja visjaunākajai tehniskajai informācijai.
-   **Saturs, ko ir rakstījuši speciālisti** — vietne nodrošina plašāku produkta dokumentācijas klāstu, ko var paplašināt kopienas dalībnieki gan korporācijā Microsoft, gan ārpus tās.
-   **Piekļuve dažāda veida saturam** — vietne sniedz iespēju ātri piekļūt dažāda veida saturam par programmatūru Dynamics 365 for Operations, piemēram, Microsoft Office Mix prezentācijām, uzdevumu ceļvežiem, videoklipiem un tēmām.
-   **Saturs, kas veicina jūsu biznesa procesus** — vietnē ir ietverts ar biznesa procesiem saistīts saturs, kas tiek nodrošināts, izmantojot biznesa procesu modelētāju (BPM) pakalpojumos Microsoft Dynamics Lifecycle Services (LCS).

Viss mūsu saturs ir migrēts no mūsu iepriekšējās palīdzības vikivietnes uz vietni docs. Mēs esam sajūsmā par savu jauno vietni un ceram, ka arī jums tā patiks.

### <a name="when-can-we-use-it"></a>Kad mēs varam to izmantot?

Vietnes docs saturu varat lasīt jau tagad — šī vietne ir pilnībā publiska, un tajā var veikt meklēšanu nepierakstoties. Lai atrastu saturu, varat izmantot jebkuru no iecienītākajām meklēšanas programmām. Ja vēlaties, varat pierakstīties un pievienot komentārus vietnē esošajiem rakstiem.


## <a name="task-guides"></a>Uzdevumu ceļveži
Uzdevuma ceļvedis ir kontrolēts, strukturēts, interaktīvs līdzeklis, kas palīdz veikt uzdevuma vai biznesa procesa darbības. Uzdevumu ceļvežus varat atvērt (atskaņot) rūtī Palīdzība. Kad pirmo reizi noklikšķināta uz kāda uzdevuma ceļveža, rūtī Palīdzība tiek parādīti detalizēti šī uzdevuma veikšanas norādījumi. Tagad ir pieejami lokalizēti uzdevumu ceļveži. [![Uzdevuma ceļveža lasīšanas skats](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png) Lai sāktu lietot strukturēto, interaktīvo līdzekli, noklikšķiet uz **Sākt uzdevuma ceļvedi** rūts Palīdzība apakšdaļā. Tiek atvērts melns rādītājs, un tas norāda uz darbību, kas jums ir jāveic. Izpildiet norādījumus, kas tiek parādīti UI, un ievadiet datus saskaņā ar norādījumiem. [![Uzdevuma ceļveža darbības veikšanas norādījums](./media/task-guide-step-1-ops.png)](./media/task-guide-step-1-ops.png) **Svarīgi!** Dati, ko ievadāt uzdevuma ceļveža atskaņošanas laikā, ir īsti. Ja esat ražošanas vidē, šie dati tiks ievadīti uzņēmumā, kuru pašlaik izmantojat.

### <a name="it-all-begins-with-task-recorder"></a>Viss sākas ar uzdevumu ierakstītāju

Uzdevumu ceļveži tiek veidoti, izmantojot uzdevumu ierakstītāju. Kad lietojat uzdevumu ierakstītāju, tiek ierakstītas visas darbības, ko izpildāt programmatūras Dynamics 365 for Operations lietotāja interfeisā (UI) (piemēram, klikšķināšana uz izvēlnēm, iestatījumu mainīšana un datu ievadīšana). Ierakstītās darbības kopā tiek sauktas par uzdevuma ierakstu. Kā paskaidrots iepriekšējā sadaļā, uzdevumu ierakstus var parādīt rūtī Palīdzība un atskaņot kā uzdevumu ceļvežus. Taču uzdevumu ierakstus varat izmantot arī citos veidos:

-   **Uzdevumu ierakstus saglabāt BPM**  — uzdevumu ierakstus varat saglabāt kādā hierarhijas rindā BPM bibliotēkā, kas atrodas LCS. Kad uzdevuma ierakstu saglabājat BPM, kopā ar ieraksta darbībām tiek ģenerēta un paradīta plūsmkartes diagramma. **Piezīme.** Lai uzdevumu ierakstu parādītu Dynamics 365 for Operations rūtī Palīdzība un to atskaņotu kā uzdevuma ceļvedi, šis ieraksts jums ir jāsaglabā BPM bibliotēkā.
-   **Uzdevumu ierakstus saglabāt kā Word dokumentus** — uzdevuma ierakstu saglabājot kā Microsoft Word dokumentu, savai organizācijai varat ērti sagatavot drukājamus apmācību ceļvežus.

Papildinformāciju par uzdevumu reģistrētāju skatiet tēmā [Uzdevumu reģistrētājs programmatūrā Dynamics 365 for Operations](../user-interface/task-recorder.md).

### <a name="creating-customized-task-recordings"></a>Pielāgotu uzdevumu ierakstu izveidošana

Varat izveidot pats savus uzdevumu ierakstus, vai varat lejupielādēt un pielāgot uzdevuma ierakstu, kas nodrošina Microsoft. Līdz ar to varat izveidot savai organizācijai pielāgotu palīdzību, kas atspoguļo jūsu konkrēto Dynamics 365 for Operations implementāciju. Lai Dynamics 365 for Operations rūtī Palīdzība parādītu uzdevuma ierakstu un to atskaņotu kā uzdevuma ceļvedi, šis ieraksts ir jāsaglabā LCS bibliotēkā. Ja esat partneris un pārveidojat bibliotēku par korporatīvo bibliotēku, un iekļaujat to kādā risinājumā, tā ir pieejama jūsu klientiem. Pilnīgus norādījumus skatiet tēmā [Uzdevumu ierakstu izmantošana, lai izveidotu dokumentāciju vai apmācību](../user-interface/task-recorder.md).

## <a name="in-product-help"></a>Produktā iebūvētā palīdzība
Lai piekļūtu palīdzības saturam programmatūrā Dynamics 365 for Operations, noklikšķiniet uz ikonas **Palīdzība** (**?**) un pēc tam izvēlieties Palīdzība vai nospiediet taustiņu kombināciju Ctrl+Shift+?. Abos gadījumos tiek atvērta rūts Palīdzība. Rūtī Palīdzība varat piekļūt rakstiem vai uzdevumu ceļvežiem. [![Palīdzības rūts](./media/help-pane-wiki-1024x684.png)](./media/help-pane-wiki.png)

### <a name="accessing-articles-from-the-help-pane"></a>Piekļuve rakstiem rūtī Palīdzība

Rūtī Palīdzība varat piekļūt rakstiem, kas attiecas uz Dynamics 365 for Operations klientu. Kad pirmo reizi atverat rūti Palīdzība un noklikšķināt uz cilnes **Vikivietne**, tiek parādīti raksti, kas attiecas uz programmatūrā Dynamics 365 for Operations pašlaik atvērto lapu. Ja nav atrasts neviens raksts, varat ievadīt atslēgvārdus, lai precizētu meklēšanu. Kad rūtī Palīdzība noklikšķināt uz kāda raksta, pārlūkprogrammā tiek atvērta jauna cilne un tiek parādīts šis raksts. 

### <a name="accessing-task-guides-from-the-help-pane"></a>Piekļuve uzdevumu ceļvežiem rūtī Palīdzība

Lai rūtī Palīdzība varētu piekļūt uzdevumu ceļvežiem, sistēmas administratoram programmatūrā Dynamics 365 for Operations ir jāatver lapa **Sistēmas parametri** un jākonfigurē daži iestatījumi. **Piezīmes.**

-   Lai konfigurētu palīdzību, jums ir jāpierakstās ar kontu tajā pašā nomniekā, kurā ir izvietota programmatūra Dynamics 365 for Operations.
-   Savienojumu ar LCS bibliotēku nav iespējams izveidot no Dynamics 365 for Operations instances, kas darbojas lokālā virtuālajā cietajā diskā (VHD).

[![Veidlapa Sistēmas parametri ar palīdzības sistēmas iestatījumiem](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Lapā **Sistēmas parametri** veiciet tālāk norādītās darbības.

1.  **Svarīgi!**Kad cilni Palīdzība atverat pirmo reizi, ir jāizveido savienojums ar Lifecycle Services. Noteikti noklikšķiniet uz saites veidlapas vidū, uzgaidiet, līdz tiek izveidots savienojums, aizveriet dialoglodziņu un pēc tam noklikšķiniet uz Labi, piekļūtu parametru veidlapai.[![Savienojuma izveide ar LCS](./media/connect-to-lcs-crop-1024x365.png)](./media/connect-to-lcs-crop.png)
2.  Atlasiet Lifecycle Services projektu, ar kuru izveidot savienojumu.
3.  Atlasiet BPM bibliotēkas (atlasītajā projektā), no kurām izgūt uzdevumu ierakstus.
4.  Iestatiet BPM bibliotēku attēlošanas secību. Tā nosaka secību, kādā uzdevumu ieraksti no bibliotēkām tiks rādīti rūtī Palīdzība.

Kad sistēmas administrators ir izpildījis šīs darbības, varat atvērt rūti Palīdzība un noklikšķināt uz cilnes **Uzdevumu ceļveži**. Tagad tiek parādīti uzdevumu ceļveži, kas attiecas uz programmatūrā Dynamics 365 for Operations pašlaik atvērto lapu. Ja nav atrasts neviens uzdevuma ceļvedis, varat ievadīt atslēgvārdus, lai precizētu meklēšanu. Kad rūtī Palīdzība noklikšķināt uz kāda uzdevuma ceļveža, rūtī Palīdzība tiek parādīti detalizēti norādījumi un varat atskaņot uzdevuma ceļvedi. [![Uzdevuma ceļveža lasīšanas skats](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides"></a>Kur ir pieejami tulkotie uzdevumu ceļveži?

Tulkotie uzdevumu ceļveži tiek izlaisti bibliotēkās, kuru nosaukumā ir vārdi “visas valodas”. Lai programmatūrā Dynamics 365 for Operations skatītu lokalizētus uzdevumu ceļvežu palīdzības materiālus, pārliecinieties, ka ir izveidots savienojums ar atbilstošo bibliotēku. Uzdevuma ceļveža rādīšanas valodu katram lietotājam var norādīt, izmantojot valodas iestatījumus sadaļā **Opcijas** &gt; **Preferences**. 
-   Ja kāds uzdevumu ceļvedis ir iztulkots, kad atverat šo uzdevumu ceļvedi, viss šī uzdevuma ceļveža teksts tiek rādīts jūsu izvēlētajā valodā.
-   Ja kāds uzdevumu ceļvedis vēl nav iztulkots, kad to atverat, jūsu izvēlētajā valodā tiek rādīta tikai daļa teksta (vadīklu teksts).

## <a name="additional-resources"></a>Papildu resursi
Nākamajā tabulā ir uzskaitītas vietnes, kuras nodrošina Dynamics 365 for Operations saturu. Mūsu satura vietnes ir sakārtotas tā, lai atbalstītu debitoru lietošanas ciklu. Katru fāzi atbalsta cita vietņu kopa. Vietnēs, pie kuru nosaukuma ir zvaigznīte (\*), ir jāpierakstās, izmantojot ar pakalpojumu plānu saistīto kontu.

| Atrašanās vieta                                                                     | apraksts                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Docs.microsoft.com](/dynamics365/#pivot=solutions&panel=solutions_operations) | Vieso vai sniedz saites uz visu produktu dokumentāciju programmatūrai Dynamics 365 for Operations.                                                                                                                                                               |
| [Lifecycle Services](http://lcs.dynamics.com/en/)\*                      | Sniedz mākonī pieejamu sadarbības darbvietu, ko debitori un partneri var izmantot, lai pārvaldītu Dynamics 365 for Operations projektus no pirmspārdošanas līdz ieviešanai un operācijām. Šī vietne ir noderīga visām ieviešanas fāzēm. |
| [CustomerSource](http://www.customersource.com/)\*                       | Vieso plašu apmācības resursu klāstu un ir primārā atbalsta vietne programmatūrai Dynamics 365 for Operations. Iespējams, ir nepieciešams pierakstīties, lai piekļūtu specifiskiem vietnes resursiem.                                                                      |
| [Atbalsta emuārs](http://aka.ms/AXSupportBlog)                              | Sniedz padomus un metodes, ko publicē Dynamics 365 for Operations atbalsta darba grupa.                                                                                                                                                  |
| [MSDN](http://aka.ms/AXMSDN)                                             | Vieso saturu no iepriekšējiem laidieniem, kas ir rakstīts izstrādātājiem.                                                                                                                                                                       |
| [TechNet](http://aka.ms/TechNet)                                         | Vieso saturu no iepriekšējiem laidieniem, kas ir rakstīts IT profesionāļiem un programmas lietotājiem.                                                                                                                                           |
| [Dynamics kopiena](http://community.dynamics.com/)                  | Vieso emuārus, forumus un video.                                                                                                                                                                                                           |
| [Microsoft.com/Dynamics/](http://www.microsoft.com/dynamics/)                 | Sniedz novērtējumu un pārdošanas informāciju.                                                                                                                                                                                                 |



<a name="see-also"></a>Skatiet arī
--------

[Dynamics 365 for Operations palīdzības sistēma (lejupielādējama informācijas lapa)](https://mbs.microsoft.com/files/public/CS/AX2012R3/DynamicsAXHelpSystemFactSheet.pdf)

[Uzdevumu reģistrētājs programmatūrā Microsoft Dynamics 365 for Operations](../user-interface/task-recorder.md)

[Dokumentācijas vai apmācības veidošana, izmantojot uzdevumu ierakstus](../user-interface/task-recorder.md)

[Jauni vai atjaunināti uzdevumu ceļveži (2016. gada novembris)](new-task-guides-november-2016.md)
[Jauni vai atjaunināti uzdevumu ceļveži (2016. gada augusts)](new-updated-task-guides-available-august-2016.md)
[Jauni vai atjaunināti uzdevumu ceļveži (2016. gada maijs)](new-updated-task-guides-available-may-2016.md)
[Jauni uzdevumu ceļveži (2016. gada februāris)](new-task-guides-available-february-2016.md)








