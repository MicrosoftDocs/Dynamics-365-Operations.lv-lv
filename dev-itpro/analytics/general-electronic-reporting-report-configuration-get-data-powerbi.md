---
title: "Konfigurēt elektroniskos pārskatus, lai ievilktu datus pakalpojumā Power BI"
description: "Šajā tēmā ir paskaidrots, kā varat lietot savu elektronisko pārskatu (Electronic Reporting — ER) konfigurāciju, lai organizētu datu pārsūtīšanu no jūsu Dynamics 365 for Operations instances uz Power BI pakalpojumiem. Kā piemērs šajā tēmā ir izmantotas Intrastat transakcijas, kas veido pārsūtāmos biznesa datus. Power BI kartes vizualizācija šos Intrastat transakciju datus izmanto, lai sniegtu skatu uzņēmuma importēšanas/eksportēšanas aktivitāšu analīzei Power BI pārskatā."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 4bbc77eb1edfe0c109434ce4d26228ed031f48bc
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="configure-electronic-reporting-to-pull-data-into-power-bi"></a>Konfigurēt elektroniskos pārskatus, lai ievilktu datus pakalpojumā Power BI

[!include[banner](../includes/banner.md)]


Šajā tēmā ir paskaidrots, kā varat lietot savu elektronisko pārskatu (Electronic Reporting — ER) konfigurāciju, lai organizētu datu pārsūtīšanu no jūsu Dynamics 365 for Operations instances uz Power BI pakalpojumiem. Kā piemērs šajā tēmā ir izmantotas Intrastat transakcijas, kas veido pārsūtāmos biznesa datus. Power BI kartes vizualizācija šos Intrastat transakciju datus izmanto, lai sniegtu skatu uzņēmuma importēšanas/eksportēšanas aktivitāšu analīzei Power BI pārskatā.

<a name="overview"></a>Pārskats
--------

Microsoft Power BI ir kolekcija ar programmatūras pakalpojumiem, programmām un savienotājiem, kas savstarpēji sadarbojas, ārējos datu avotus padarot par saprotamiem, vizuāli visaptverošiem un interaktīviem ieskatiem. Elektroniskā pārskatu veidošana (Electronic reporting — ER) programmā Microsoft Dynamics 365 for Operations lietotājiem ļauj vienkārši konfigurēt datu avotus un sakārtot datu pārsūtīšanu no Dynamics 365 for Operations uz Power BI. Dati tiek pārsūtīti kā faili OpenXML darblapas (Microsoft Excel darbgrāmatas faila) formātā. Pārsūtītie faili tiek glabāti pakalpojumā Microsoft SharePoint Server, kas ir konfigurēts šim nolūkam. Glabātie faili tiek izmantoti pakalpojumā Power BI, vai veidotu pārskatus, kuri ietver vizualizācijas (tabulas, diagrammas, kartes un citus elementus). Power BI pārskati tiek koplietoti ar Power BI lietotājiem, un tiem tiek piekļūts Power BI informācijas paneļos un Dynamics 365 for Operations lapās. Šajā tēmā ir paskaidroti tālāk uzskaitītie uzdevumi.

-   Konfigurējiet programmu Dynamics 365 for Operations.
-   Sagatavojiet savu ER formāta konfigurāciju, lai saņemtu datus no Dynamics 365 for Operations.
-   Konfigurējiet ER vidi datu pārsūtīšanai uz Power BI.
-   Lietojiet pārsūtītos datus Power BI pārskata veidošanai.
-   Padariet Power BI pārskatu pieejamu programmā Dynamics 365 for Operations.

## <a name="prerequisites"></a>Priekšnosacījumi
Lai izpildītu šajā tēmā aprakstīto piemēru, jums ir nepieciešama tālāk norādītā piekļuve.

-   Piekļuve programmai Dynamics 365 for Operations vienai no šīm lomām:
    -   Elektroniskā pārskata izstrādātājs
    -   Elektronisko pārskatu veidošanas funkcionālais konsultants
    -   Sistēmas administrators
-   Piekļuve pakalpojumam SharePoint Server, kas ir konfigurēts lietošanai ar Dynamics 365 for Operations
-   Piekļuve Power BI struktūrai

## <a name="configure-document-management-parameters"></a>Konfigurēt dokumentu pārvaldības parametrus
1.  Lapā **Dokumentu pārvaldības parametri** konfigurējiet piekļuvi pakalpojumam SharePoint Server, kas tiks izmantots tajā uzņēmumā, kurā esat pierakstījies (šajā piemērā tas ir DEMF uzņēmums).
2.  Pārbaudiet savienojumu ar SharePoint Server, lai pārliecinātos, ka jums ir piešķirta piekļuve. [![Lapa Dokumentu pārvaldības parametri](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)
3.  Atveriet konfigurēto SharePoint vietni. Izveidojiet jaunu mapi, kur ER saglabās Excel failus, kuros ir biznesa dati, kas Power BI pārskatiem ir nepieciešami kā Power BI datu kopu avots.
4.  Programmā Dynamics 365 for Operations, lapā **Dokumentu tipi** izveidojiet jaunu dokumenta tipu, kas tiks izmantots, lai piekļūtu jūsu tikko izveidotajai SharePoint mapei. Ievadiet vērtību **Fails** laukā **Grupa** un vērtību **SharePoint** laukā **Atrašanās vieta**, un pēc tam ievadiet SharePoint mapes adresi. [![Lapa Dokumentu tipi](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>Konfigurēt ER parametrus
1.  Darbvietā **Elektronisko pārskatu veidošana** noklikšķiniet uz saites **Elektronisko pārskatu veidošanas parametri**.
2.  Cilnē **Pielikumi** atlasiet dokumenta tipu **Fails** visiem laukiem.
3.  Darbvietā **Elektronisko pārskatu veidošana** nepieciešamo pakalpojumu sniedzēju padariet aktīvu, noklikšķinot uz **Iestatīt kā aktīvu**. Lai iegūtu papildinformāciju, noskatieties uzdevuma ceļvedi **ER Atlasīt pakalpojumu sniedzēju**.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>Izmantot ER datu modeli kā datu avotu
Jums ir nepieciešams ER datu modelis kā biznesa datu avots, kurš tiks izmantots Power BI pārskatos. Šis datu modelis tiek augšupielādēts no ER konfigurācijas krātuves. Papildinformāciju skatiet tēmā [Lejupielādēt elektronisko pārskatu veidošanas konfigurācijas no Lifecycle Services](download-electronic-reporting-configuration-lcs.md) vai noskatieties uzdevuma ceļvedi **ER Importēt konfigurāciju no Lifecycle Services**. Atlasiet **Intrastat**kā datu modeli, kurš tiks augšupielādēts no atlasītā ER konfigurāciju repozitorija. (Šajā piemērā tiek lietota modeļa 1. versija.) Pēc tam varat piekļūt ER modeļa konfigurācijai **Intrastat** lapā **Konfigurācijas**. [![Lapa Konfigurācijas](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Noformēt ER formāta konfigurāciju
Jums ir jāizveido jauna ER formāta konfigurācija, kas kā biznesa datu avotu lieto **Intrastat** datu modeli. Šai formāta konfigurācijai izvades rezultāti ir jāģenerē kā elektroniskie dokumenti OpenXML (Excel faila) formātā. Lai iegūtu papildinformāciju, noskatieties uzdevuma ceļvedi **ER Izveidot konfigurāciju pārskatiem OPENXML formātā**. Jaunajai konfigurācijai piešķiriet nosaukumu **Importēšanas/eksportēšanas aktivitātes**, kā parādīts nākamajā attēlā. kad noformējat ER formātu, kā veidni izmantojiet Excel failu [ER dati — importēšanas un eksportēšanas informācija](https://go.microsoft.com/fwlink/?linkid=845208). (Lai uzzinātu, kā importēt formāta veidni, atskaņojiet uzdevuma ceļvedi.) [![Konfigurācija Importēšanas/eksportēšanas aktivitātes](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png) Lai modificētu formāta konfigurāciju **Importēšanas/eksportēšanas aktivitātes**, veiciet tālāk norādītās darbības.

1.  Noklikšķiniet uz **Veidotājs**.
2.  Cilnē **Formāts** šī formāta faila elementam piešķiriet nosaukumu **Excel izvades fails**. [![Elements Excel izvades fails](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)
3.  Cilnē **Kartēšana** norādiet nosaukumu tam Excel failam, kurš tiks ģenerēts ikreiz, kad tiks palaists šis formāts. Konfigurējiet saistīto izteiksmi, lai atgrieztu vērtību **Importēšanas un eksportēšanas informācija** (faila nosaukuma paplašinājums .xlsx tiks pievienots automātiski). [![Formāta veidotājs](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)
4.  Pievienotu jaunu datu avota vienumu šim formātam. (Šis uzskaitījums būs nepieciešams turpmākai datu saistīšanai.)
    1.  Piešķiriet datu avotam nosaukumu **direction\_enum**.
    2.  Kā datu avota tipu atlasiet **Datu modeļu uzskaitījums**.
    3.  Skatiet datu modeļu uzskaitījumu **Virziens**.

    [![direction\_enum](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)
5.  Pabeidziet datu modeļa **Intrastat** un norādītā formāta elementu saistīšanu, kā parādīts nākamajā attēlā. [![Saistīšanas pabeigšana](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Pēc tā palaišanas ER formāts ģenerē izvades rezultātu Excel formātā. Informāciju par Intrastat transakcijām tas nosūta uz izvades rezultātu, un tās atdala kā transakcijas, kuras apraksta importēšanas aktivitātes vai eksportēšanas aktivitātes. Noklikšķiniet uz **Palaist**, lai testētu jauno ER formātu ar Intrastat transakciju sarakstu, kas ir norādīts lapā **Intrastat** (**Nodokļi** &gt; **Deklarācijas** &gt; **Ārējā tirdzniecība** &gt; **Intrastat**). [![Lapa Intrastat](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png) Tiek ģenerēts tālāk norādītais izvades rezultāts. Faila nosaukums ir **Importēšanas un eksportēšanas informācija.xlsx**, kā norādījāt formāta iestatījumos. [![Importēšanas un eksportēšanas informācija.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>Konfigurēt ER adresātu
Ir nepieciešams konfigurēt ER struktūru, lai jaunā ER formāta konfigurācijas izvades rezultātu sūtītu īpašā veidā.

-   Šis izvades rezultāts ir jānosūta uz atlasītā SharePoint Server mapi.
-   Katrai formātā konfigurācijas izpildei ir jāizveido tā paša Excel faila jauna versija.

Lapā **Elektroniskie pārskati** (**Organizācijas administrēšana** &gt; **Elektroniskie pārskati**) noklikšķiniet uz vienuma **Elektroniskās pārskatu veidošanas adresāts** un pievienojiet jaunu adresātu. Laukā **Atsauce** atlasiet iepriekš izveidoto formāta konfigurāciju **Importēšanas/eksportēšanas aktivitātes**. Izpildiet tālāk aprakstītās darbības, lai atsaucei pievienotu jaunu faila adresāta ierakstu.

1.  Laukā **Nosaukums** ievadiet faila adresāta nosaukumu.
2.  Laukā **Faila nosaukums** atlasiet nosaukumu **Excel izvades fails** Excel faila formāta komponentam.

Noklikšķiniet uz pogas **Iestatījumi** jaunajam adresāta ierakstam. Pēc tam dialoglodziņā **Adresāta iestatījumi** izpildiet tālāk aprakstītās darbības.

1.  Cilnē **Power BI** opcijai **Iespējots** iestatiet vērtību **Jā**.
2.  Laukā **SharePoint** atlasiet iepriekš izveidoto dokumenta tipu **Kopīgots**.

## <a name="schedule-execution-of-the-configured-er-format"></a>Plānot konfigurētā ER formāta izpildi
Lapā **Konfigurācijas** (**Organizācijas administrēšana** &gt; **Elektroniskie pārskati** &gt; **Konfigurācijas**) esošajā konfigurācijas kokā atlasiet iepriekš izveidoto konfigurāciju **Importēšanas/eksportēšanas aktivitātes**. Lai šo formātu padarītu pieejamu lietošanai, versijas 1.1 statusu no **Melnraksts** mainiet uz **Pabeigts**. [![Lapa Konfigurācijas](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png) Atlasiet pabeigto konfigurācijas **Importēšanas/eksportēšanas aktivitātes** versiju un noklikšķiniet uz **Palaist**. Ievērojiet, ka konfigurētais adresāts tiek lietots izvades rezultātam, kurš tiek ģenerēts Excel formātā. Opcijai **Pakešapstrāde** iestatiet vērtību **Jā**, lai šo pārskatu palaistu neuzraudzītā režīmā. Noklikšķiniet uz **Periodiskums**, lai šī pakešuzdevuma izpildei plānotu nepieciešamo periodiskumu. Periodiskums nosaka, cik bieži atjauninātie dati no Dynamics 365 for Operations tiks pārsūtīti uz Power BI. [![Dialoglodziņš Elektroniskā pārskata parametri](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png) Kad tas ir konfigurēts, ER pārskata izpildes darbs ir pieejams lapā **Pakešuzdevumi** (**Sistēmas administrēšana &gt; Pieprasījumi &gt; Pakešuzdevumi**). [![Lapa Pakešuzdevumi](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png) Kad šis darbs tiek palaists pirmo reizi, adresāts izveido jaunu Excel failu ar konfigurēto nosaukumu atlasītajā SharePoint mapē. Katrā turpmākajā šī darba palaišanas reizē adresāts izveido jaunu šī Excel faila versiju. [![Jauna Excel faila versija](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Izveidot Power BI datu kopu, izmantojot ER formāta izvades rezultātu
Pierakstieties pakalpojumā Power BI un atveriet esošu Power BI grupu (darbvieta) vai izveidojiet jaunu grupu. Noklikšķiniet uz **Pievienot** izvēlnē **Faili** sadaļā **Importējiet datus vai izveidojiet savienojumu ar tiem** vai noklikšķiniet uz pluszīmes (**+**), kas atrodas blakus vienumam **Datu kopas** kreisajā rūtī. [![Datu kopas izveide](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png) Atlasiet opciju **SharePoint — darba grupas vietnes** un pēc tam ievadiet izmantotā SharePoint servera ceļu (šajā piemērā tas ir **https://ax7partner.spoppe.com**). Pēc tam pārlūkojiet uz mapi **/Koplietotie dokumenti/GER dati/PowerBI** un atlasiet Excel failu, kuru izveidojāt kā jaunās Power BI datu kopas datu avotu. [![Excel faila atlase](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png) Noklikšķiniet uz **Izveidot savienojumu** un pēc tam noklikšķiniet uz **Importēt**. Tiek izveidota jauna datu kopa, kas ir balstīta uz atlasīto Excel failu. Šo datu kopu jaunizveidotajam informācijas panelim var pievienot arī automātiski. [![Datu kopa informācijas panelī](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png) Konfigurējiet šīs datu kopas atsvaidzināšanas grafiku, lai piespiedu kārtā veiktu periodisku atjaunināšanu. Periodiskie atjauninājumi ļauj patērēt jaunus biznesa datus, kas tiek saņemti no Dynamics 365 for Operations, izmantojot periodisku ER pārskata izpildi ar jaunām pakalpojumā SharePoint Server esošā Excel faila versijām.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Izveidot Power BI pārskatu, izmantojot jauno datu kopu
Lai izveidotu jaunu Power BI pārskatu, noklikšķiniet uz jūsu izveidoto **Importēšanas un eksportēšanas informācija** Power BI datu kopu. Pēc tam konfigurējiet vizualizācijas. Piemēram, atlasiet vizualizāciju **Kartogramma** un konfigurējiet to tālāk aprakstītajā veidā.

-   Datu kopas lauku **CountryOrigin** piešķiriet kartes vizualizācijas laukam **Atrašanās vieta**.
-   Datu kopas lauku **Summa** piešķiriet kartes vizualizācijas laukam **Krāsu piesātinājums**.
-   Datu kopas laukus **Aktivitāte** un **Gads** pievienojiet kartes vizualizācijas lauku kolekcijai **Filtri**.

Saglabājiet šo Power BI pārskatu kā **Importēšanas un eksportēšanas informācijas pārskats**. [![Importēšanas un eksportēšanas informācijas pārskats](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png) Ņemiet vērā, ka kartē tiek rādītas valstis/reģioni, kas ir norādīti Excel failā (šajā piemērā tās ir Austrija un Šveice) Šīs valstis/reģioni ir iekrāsoti, lai katram rādītu rēķinos iekļauto summu proporcionālo daudzumu. Atjauniniet Intrastat transakciju sarakstu. Tiek pievienotas Itālijas izcelsmes eksporta transakcijas. [![Intrastat transakciju saraksts](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png) Gaidiet nākamo plānoto ER pārskata izpildi un nākamo plānoto Power BI datu kopas atjaunināšanu. Pēc tam pārskatiet Power BI pārskatu (atlasiet, lai rādītu tikai importa transakcijas). Tagad atjauninātajā kartē tiek rādīta Itālija. [![Atjaunināta karte](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-dynamics-365-for-operations"></a>Piekļūt Power BI pārskatam programmā Dynamics 365 for Operations
Iestatiet integrāciju starp programmu Dynamics 365 for Operations un pakalpojumu Power BI. Papildinformāciju skatiet tēmā [Power BI integrācijas konfigurēšana darbvietām](configure-power-bi-integration.md). Lapā **Elektronisko pārskatu darbvieta**, kas atbalsta Power BI integrāciju (**Organizācijas administrēšana** &gt; **Darbvietas** &gt; **Elektronisko pārskatu darbvieta**), noklikšķiniet uz **Opcijas** &gt; **Atvērt katalogu pārskatu**. Atlasiet jūsu izveidoto Power BI pārskatu **Importēšanas un eksportēšanas informācija**, lai šis pārskats atlasītajā lapā tiktu rādīts kā darbības vienums. Noklikšķiniet uz darbības vienuma, lai atvērtu Dynamics 365 for Operations lapu, kurā ir redzams pārskats, ko noformējāt pakalpojumā Power BI. [![Importēšanas un eksportēšanas informācijas pārskats](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

<a name="see-also"></a>Skatiet arī
--------

[Elektronisko atskaišu galamērķi](electronic-reporting-destinations.md)

[Elektronisko atskaišu veidošanas pārskats](general-electronic-reporting.md)



