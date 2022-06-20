---
title: Elektronisko pārskatu izveides (ER) konfigurēšana, lai pārsūtītu datus uz pakalpojumu Power BI
description: Šajā rakstā skaidrots, kā var lietot elektronisko pārskatu (ER) konfigurāciju, lai noteiktu datu pārsūtīšanu no instances uz Power BI pakalpojumiem.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e6903513dec4da20dbc4463fbae6a406fc06e1a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896739"
---
# <a name="configure-electronic-reporting-er-to-pull-data-into-power-bi"></a>Elektronisko pārskatu izveides (ER) konfigurēšana, lai pārsūtītu datus uz pakalpojumu Power BI

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā var lietot elektronisko pārskatu (ER) konfigurāciju, lai noteiktu datu pārsūtīšanu no instances uz Power BI pakalpojumiem. Piemēram, šis raksts lieto Intrastat darbības kā biznesa datus, kas jāpārsūta. Power BI kartes vizualizācijas funkcija izmanto šos Intrastat darbību datus, lai Power BI pārskatā parādītu uzņēmuma importēšanas/eksportēšanas aktivitāšu analīzi.

## <a name="overview"></a>Pārskats

Microsoft Power BI ir programmatūras pakalpojumu, programmu un savienotāju kopa, kuras komponenti savstarpēji sadarbojas, lai no ārējiem datu avotiem iegūtu saprotamus, vizuāli visaptverošus un interaktīvus ieskatus. Modulis Elektronisko pārskatu izveide (ER) sniedz lietotājiem iespēju viegli konfigurēt datu avotus un konfigurēt datu pārsūtīšanu no programmas uz pakalpojumu Power BI. Dati tiek pārsūtīti kā OpenXML darblapas (Microsoft Excel darbgrāmatas) formāta faili. Pārsūtītie faili tiek glabāti Microsoft SharePoint Server serverī, kas ir konfigurēts šim nolūkam. Glabātie faili tiek izmantoti pakalpojumā Power BI, lai izveidotu pārskatus, kuros ir ietvertas vizualizācijas (tabulas, diagrammas, kartes utt.). Power BI pārskati tiek kopīgoti ar Power BI lietotājiem, un tiem var piekļūt Power BI informācijas paneļos un programmas lapās. Šajā rakstā skaidroti šādi uzdevumi:

- Konfigurējiet Microsoft Dynamics 365 Finanses.
- Sagatavojiet savu ER formāta konfigurāciju, lai saņemtu datus no programmas Finance.
- Konfigurējiet ER vidi datu pārsūtīšanai uz pakalpojumu Power BI.
- Izmantojiet pārsūtītos datus, lai izveidotu Power BI pārskatu.
- Padariet Power BI pārskatu pieejamu programmā Finance.

## <a name="prerequisites"></a>Priekšnosacījumi
Lai pabeigtu piemēru šajā rakstā, jums ir jābūt šādai piekļuvei:

- Piekļuve vienai no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

- Piekļuve SharePoint Server, kas ir konfigurēts lietošanai kopā ar programmu
- Piekļuve Power BI struktūrai

## <a name="configure-document-management-parameters"></a>Konfigurēt dokumentu pārvaldības parametrus
1. Lapā **Dokumentu pārvaldības parametri** konfigurējiet piekļuvi SharePoint Server serverim, kas tiks izmantots uzņēmumā, kurā esat pierakstījies (šajā piemērā tas ir uzņēmums DEMF).
2. Pārbaudiet savienojumu ar SharePoint Server serveri, lai pārliecinātos, vai jums ir piešķirtas piekļuves tiesības.

    [![Lapa Dokumentu pārvaldības parametri.](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)

3. Atveriet konfigurēto SharePoint vietni. Izveidojiet jaunu mapi, kurā modulim ER ir jāsaglabā Excel faili, kuros ir ietverti biznesa dati, kas ir nepieciešami Power BI pārskatiem izmantošanai kā Power BI datu kopu avots.
4. Lapā **Dokumentu veidi** izveidojiet jaunu dokumenta tipu, kas tiks izmantots, lai piekļūtu jaunizveidotajai SharePoint mapei. Ievadiet vērtību **Fails** laukā **Grupa** un vērtību **SharePoint** laukā **Vieta** un pēc tam ievadiet SharePoint mapes adresi.

    [![Lapa Dokumentu tipi.](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>Konfigurējiet ER parametrus
1. Darbvietā **Elektronisko pārskatu veidošana** noklikšķiniet uz saites **Elektronisko pārskatu veidošanas parametri**.
2. Cilnē **Pielikumi** atlasiet dokumenta tipu **Fails** visiem laukiem.
3. Darbvietā **Elektronisko pārskatu veidošana** nepieciešamo pakalpojumu sniedzēju padariet aktīvu, noklikšķinot uz **Iestatīt kā aktīvu**. Lai iegūtu papildinformāciju, noskatieties uzdevuma ceļvedi **ER Atlasīt pakalpojumu sniedzēju**.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>Izmantot ER datu modeli kā datu avotu
Kā Power BI pārskatos izmantojamais biznesa datu avots ir jāizmanto ER datu modelis. Šis datu modelis tiek augšupielādēts no ER konfigurācijas krātuves. Papildinformāciju skatiet tēmā [Lejupielādēt elektronisko pārskatu veidošanas konfigurācijas no Lifecycle Services](download-electronic-reporting-configuration-lcs.md) vai noskatieties uzdevuma ceļvedi **ER Importēt konfigurāciju no Lifecycle Services**. Atlasiet **Intrastat** kā datu modeli, kurš tiks augšupielādēts no atlasītā ER konfigurāciju repozitorija. (Šajā piemērā tiek lietota modeļa 1. versija.) Pēc tam varat piekļūt ER modeļa konfigurācijai **Intrastat** lapā **Konfigurācijas**.

[![Intrastat ER modeļa kofigurācija konfigurāciju lapā.](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Noformēt ER formāta konfigurāciju
Jums ir jāizveido jauna ER formāta konfigurācija, kas kā biznesa datu avotu lieto **Intrastat** datu modeli. Šai formāta konfigurācijai izvades rezultāti ir jāģenerē kā elektroniskie dokumenti OpenXML (Excel faila) formātā. Lai iegūtu papildinformāciju, noskatieties uzdevuma ceļvedi **ER Izveidot konfigurāciju pārskatiem OPENXML formātā**. Jaunajai konfigurācijai piešķiriet nosaukumu **Importēšanas/eksportēšanas aktivitātes**, kā parādīts nākamajā attēlā. kad noformējat ER formātu, kā veidni izmantojiet Excel failu [ER dati — importēšanas un eksportēšanas informācija](https://download.microsoft.com/download/f/7/5/f755c0fd-025c-4aa9-920b-909abb8302ad/ER-data-import-and-export-details.xlsx). (Lai uzzinātu, kā importēt formāta veidni, noskatieties uzdevuma ceļvedi.)

[![Konfigurācija Importēšanas/eksportēšanas aktivitātes.](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png)

Lai modificētu formāta konfigurāciju **Importēšanas/eksportēšanas aktivitātes**, izpildiet tālāk aprakstītās darbības.

1. Noklikšķiniet uz **Veidotājs**.
2. Cilnē **Formāts** šī formāta faila elementam piešķiriet nosaukumu **Excel izvades fails**.

    [![Elements Excel izvades fails.](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)

3. Cilnē **Kartēšana** norādiet nosaukumu tam Excel failam, kurš tiks ģenerēts ikreiz, kad tiks palaists šis formāts. Konfigurējiet saistīto izteiksmi, lai atgrieztu vērtību **Importēšanas un eksportēšanas informācija** (faila nosaukuma paplašinājums .xlsx tiks pievienots automātiski).

    [![Veidotāja formāts.](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)

4. Pievienotu jaunu datu avota vienumu šim formātam. (Šis uzskaitījums būs nepieciešams turpmākai datu saistīšanai.)

    1. Piešķiriet datu avotam nosaukumu **direction\_enum**.
    2. Kā datu avota tipu atlasiet **Datu modeļu uzskaitījums**.
    3. Skatiet datu modeļu uzskaitījumu **Virziens**.

    [![direction_enum.](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)

5. Pabeidziet datu modeļa **Intrastat** un norādītā formāta elementu saistīšanu, kā parādīts nākamajā attēlā.

    [![Saistīšanas pabeigšana.](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Pēc tā palaišanas ER formāts ģenerē izvades rezultātu Excel formātā. Informāciju par Intrastat transakcijām tas nosūta uz izvades rezultātu, un tās atdala kā transakcijas, kuras apraksta importēšanas aktivitātes vai eksportēšanas aktivitātes. Noklikšķiniet uz **Palaist**, lai testētu jauno ER formātu ar Intrastat transakciju sarakstu, kas ir norādīts lapā **Intrastat** (**Nodokļi** &gt; **Deklarācijas** &gt; **Ārējā tirdzniecība** &gt; **Intrastat**).

[![Lapa Intrastat.](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png)

Tiek ģenerēts tālāk norādītais izvades rezultāts. Faila nosaukums ir **Importēšanas un eksportēšanas informācija.xlsx**, kā norādījāt formāta iestatījumos.

[![Importēšanas un eksportēšanas informācija.xlsx.](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>Konfigurēt ER adresātu
Ir nepieciešams konfigurēt ER struktūru, lai jaunā ER formāta konfigurācijas izvades rezultātu sūtītu īpašā veidā.

- Izvades rezultāts ir jānosūta uz atlasītā SharePoint Server servera mapi.
- Katrai formātā konfigurācijas izpildei ir jāizveido tā paša Excel faila jauna versija.

Lapā **Elektroniskie pārskati** (**Organizācijas administrēšana** &gt; **Elektroniskie pārskati**) noklikšķiniet uz vienuma **Elektroniskās pārskatu veidošanas adresāts** un pievienojiet jaunu adresātu. Laukā **Atsauce** atlasiet iepriekš izveidoto formāta konfigurāciju **Importēšanas/eksportēšanas aktivitātes**. Izpildiet tālāk aprakstītās darbības, lai atsaucei pievienotu jaunu faila adresāta ierakstu.

1. Laukā **Nosaukums** ievadiet faila adresāta nosaukumu.
2. Laukā **Faila nosaukums** atlasiet nosaukumu **Excel izvades fails** Excel faila formāta komponentam.

Noklikšķiniet uz pogas **Iestatījumi** jaunajam adresāta ierakstam. Pēc tam dialoglodziņā **Adresāta iestatījumi** izpildiet tālāk aprakstītās darbības.

1. Cilnē **Power BI** iestatiet opcijas **Iespējots** vērtību **Jā**.
2. Laukā **SharePoint** atlasiet iepriekš izveidoto dokumenta tipu **Kopīgots**.

## <a name="schedule-execution-of-the-configured-er-format"></a>Plānot konfigurētā ER formāta izpildi
1. Lapā **Konfigurācijas** (**Organizācijas administrēšana** &gt; **Elektroniskie pārskati** &gt; **Konfigurācijas**) esošajā konfigurācijas kokā atlasiet iepriekš izveidoto konfigurāciju **Importēšanas/eksportēšanas aktivitātes**.
2. Lai šo formātu padarītu pieejamu lietošanai, versijas 1.1 statusu no **Melnraksts** mainiet uz **Pabeigts**.

    [![Importēt/eksportēt aktivitāšu konfigurāciju lapā Konfigurācijas.](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png)

3. Atlasiet konfigurācijas **Importēšanas/eksportēšanas aktivitātes** pabeigto versiju un pēc tam noklikšķiniet uz **Palaist**. Ievērojiet, ka konfigurētais adresāts tiek lietots izvades rezultātam, kurš tiek ģenerēts Excel formātā.
4. Opcijai **Pakešapstrāde** iestatiet vērtību **Jā**, lai šo pārskatu palaistu neuzraudzītā režīmā.
5. Noklikšķiniet uz **Periodiskums**, lai šī pakešuzdevuma izpildei plānotu nepieciešamo periodiskumu. no periodiskuma ir atkarīgs tas, cik bieži atjauninātie dati tiek pārsūtīti uz pakalpojumu Power BI.

    [![Dialoglodziņš Elektronisko pārskatu parametri.](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png)

6. Kad tas ir konfigurēts, ER pārskata izpildes darbs ir atrodams lapā **Pakešuzdevumi** (**Sistēmas administrēšana &gt; Pieprasījumi &gt; Pakešuzdevumi**).

    [![Lapa Pakešuzdevumi.](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png)

7. Pirmo reizi izpildot šo darbu, galamērķa sistēma izveido jaunu Excel failu ar konfigurēto nosaukumu atlasītajā SharePoint mapē. Katrā turpmākajā šī darba palaišanas reizē adresāts izveido jaunu šī Excel faila versiju.

    [![Jauna Excel faila versija.](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Power BI datu kopas izveide, izmantojot ER formāta izvades rezultātu
1. Pierakstieties pakalpojumā Power BI un atveriet esošu Power BI grupu (darbvietu) vai izveidojiet jaunu grupu. Noklikšķiniet uz **Pievienot** izvēlnē **Faili** sadaļā **Importējiet datus vai izveidojiet savienojumu ar tiem** vai noklikšķiniet uz pluszīmes (**+**), kas atrodas blakus vienumam **Datu kopas** kreisajā rūtī.

    [![Datu kopas izveidošana.](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png)

2. Atlasiet **SharePoint — darba grupas vietnes** un pēc tam ievadiet izmantotā SharePoint Server servera ceļu (mūsu piemērā tas ir`https://ax7partner.litware.com` ).
3. Pārlūkojiet līdz mapei **/Koplietotie dokumenti/GER dati/PowerBI** un atlasiet izveidoto Excel failu kā jaunās Power BI datu kopas datu avotu.

    [![Excel faila atlasīšana.](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png)

4. Noklikšķiniet uz **Savienot** un pēc tam — uz **Importēt**. Tiek izveidota jauna datu kopa, kas ir balstīta uz atlasīto Excel failu. Šo datu kopu jaunizveidotajam informācijas panelim var pievienot arī automātiski.

    [![Datu kopa informācijas panelī.](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png)

5. Konfigurējiet šīs datu kopas atsvaidzināšanas grafiku, lai piespiestu veikt periodisku atjaunināšanu. Periodiskie atjauninājumi sniedz iespēju lietot jaunos biznesa datus, kas tiek saņemti, periodiski izpildot ER pārskatu ar jaunām SharePoint serverī izveidotā Excel faila versijām.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Power BI pārskata izveide, izmantojot jauno datu kopu
1. Noklikšķiniet uz iepriekš izveidotās Power BI datu kopas **Importēšanas un eksportēšanas informācija**.
2. Konfigurējiet vizualizāciju. Piemēram, atlasiet vizualizāciju **Kartogramma** un konfigurējiet to tālāk aprakstītajā veidā.

    - Datu kopas lauku **CountryOrigin** piešķiriet kartes vizualizācijas laukam **Atrašanās vieta**.
    - Datu kopas lauku **Summa** piešķiriet kartes vizualizācijas laukam **Krāsu piesātinājums**.
    - Datu kopas laukus **Aktivitāte** un **Gads** pievienojiet kartes vizualizācijas lauku kolekcijai **Filtri**.

3. Saglabājiet šo Power BI pārskatu ar nosaukumu **Importēšanas un eksportēšanas informācijas pārskats**.

    [![Importēšanas un eksportēšanas informācijas pārskats.](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png)

    Ievērojiet, ka kartē tiek rādītas valstis/reģioni, kas ir minēti Excel failā (šajā piemērā tās ir Austrija un Šveice). Šīs valstis/reģioni ir iekrāsoti, lai katram rādītu rēķinos iekļauto summu proporcionālo daudzumu.

4. Atjauniniet Intrastat transakciju sarakstu. Tiek pievienotas Itālijas izcelsmes eksporta transakcijas.

    [![Intrastat transakciju saraksts.](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png)

5. Gaidiet nākamo plānoto ER pārskata izpildi un nākamo plānoto Power BI datu kopas atjaunināšanu. Pēc tam skatiet Power BI pārskatu (atlasiet tikai importēšanas transakciju rādīšanas režīmu). Tagad atjauninātajā kartē tiek rādīta Itālija.

    [![Atjaunināta karte.](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-finance"></a>Piekļuve Power BI pārskatam programmā Finance
Iestatiet integrāciju ar Power BI. Papildinformāciju skatiet rakstā [Pakalpojuma Power BI integrācijas konfigurēšana darbvietām](configure-power-bi-integration.md).

1. Darbvietas **Elektronisko pārskatu izveide** lapā, kas atbalsta Power BI integrāciju (**Organizācijas administrēšana** &gt; **Darbvietas** &gt; **Elektronisko pārskatu izveides darbvieta**), noklikšķiniet uz **Opcijas** &gt; **Atvērt pārskatu katalogu**.
2. Atlasiet jūsu izveidoto Power BI pārskatu **Importēšanas un eksportēšanas informācija**, lai šis pārskats tiktu parādīts kā darbības vienums atlasītajā lapā.
3. Noklikšķiniet uz darbības vienuma, lai atvērtu lapu, kurā ir redzams pārskats, ko noformējāt pakalpojumā Power BI.

    [![Importēšanas un eksportēšanas informācijas pārskats, izveidots Power BI.](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

## <a name="additional-resources"></a>Papildu resursi

[Elektroniskās pārskatu veidošanas (ER) adresāti](electronic-reporting-destinations.md)

[Elektronisko ziņojumu (ER) pārskats](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
