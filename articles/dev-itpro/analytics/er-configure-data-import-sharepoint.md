---
title: "Datu importa konfigurēšana importēšanai no SharePoint"
description: "Šajā tēmā ir paskaidrots, kā importēt datus no Microsoft SharePoint."
author: NickSelin
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 4285db9c71208bce45d64933e692a25ef3f46b26
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2018

---
# <a name="configure-data-import-from-sharepoint"></a>Datu importa konfigurēšana importēšanai no SharePoint

[!include[banner](../includes/banner.md)]

Lai importētu datus no ienākoša faila, izmantojot elektronisko pārskatu (Electronic reporting — ER) struktūru, ir nepieciešams konfigurēt ER formātu, kas atbalsta importēšanu, un pēc tam palaist modeļa kartēšanu ar tipu **Uz galamērķi**, kas šo formātu izmanto kā datu avotu. Lai importētu datus, ir jāpāriet uz failu, kuru vēlaties importēt. Ienākošo failu lietotājs var atlasīt manuāli. Tā kā ir ieviesta jaunā ER iespēja atbalstīt datu importēšanu no Microsoft SharePoint, šo procesu var konfigurēt kā neuzraudzītu. Varat izmantot ER konfigurācijas, lai veiktu datu importēšanu no failiem, kas tiek glabāti Microsoft SharePoint mapēs. Šajā tēmā ir paskaidrots, kā izpildīt importēšanu no SharePoint uz Microsoft Dynamics 365 for Finance and Operations. Piemēros kā biznesa dati tiek izmantotas kreditoru transakcijas.

## <a name="prerequisites"></a>Priekšnosacījumi
Lai izpildītu šajā tēmā aprakstītos piemērus, jums ir nepieciešama tālāk norādītā piekļuve.

- Piekļuve programmai Finance and Operations vienai no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

- Piekļuve Microsoft SharePoint Server instancei, kas ir konfigurēta lietošanai ar Finance and Operations
- ER formātu un modeļu konfigurācijas 1099 maksājumiem

### <a name="create-required-er-configurations"></a>Nepieciešamo ER konfigurāciju izveidošana
Noskatieties uzdevumu ceļvežus **ER Datu importēšana no Microsoft Excel faila**, kas veido daļu no biznesa procesa **7.5.4.3 IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)**. Šajos uzdevumu ceļvežos jums ir detalizēti aprakstīta ER konfigurāciju izstrādāšana un lietošana interaktīvai kreditoru transakciju importēšanai no ārējiem Microsoft Excel failiem. Plašāku informāciju skatiet tēmā [Ienākošo dokumentu parsēšana programmā Microsoft Excel](parse-incoming-documents-excel.md). Visbeidzot, jums ir tālāk uzskaitītie elementi.

- ER konfigurācijas:

    - ER modeļa konfigurācija **1099 maksājumu modelis**
    - ER formāta konfigurācija **Formāts kreditoru transakciju importēšanai no Excel**

[![ER konfigurācijas datu importēšanai no SharePoint](./media/GERImportFromSharePoint-01-Configurations.PNG)](./media/GERImportFromSharePoint-01-Configurations.PNG)

- Ienākošā faila paraugs datu importēšanai:

    - Excel fails **1099import-data.xlsx** ar kreditoru transakcijām, kas ir jāimportē programmā Finance and Operations

[![Microsoft Excel faila paraugs importēšanai no SharePoint](./media/GERImportFromSharePoint-02-Excel.PNG)](./media/GERImportFromSharePoint-02-Excel.PNG)

> [!NOTE]
> Formāts kreditoru transakciju importēšanai ir atlasīts kā noklusējuma modeļa kartēšana. Tādēļ, ja palaižat modeļa kartēšanu **1099 maksājumu modelis** un šī modeļa kartēšana ir ar tipu **Uz galamērķi**, modeļa kartēšana palaiž šo formātu, lai importēt datus no ārējiem failiem. Pēc tam tā izmanto šos datus, lai atjauninātu programmas tabulas.

## <a name="configure-document-management-parameters"></a>Dokumentu pārvaldības parametru konfigurēšana
1. Lapā **Dokumentu pārvaldības parametri** konfigurējiet piekļuvi SharePoint Server instancei, kuru izmantos tas uzņēmums, kurā pašlaik esat pierakstījies. Šajā piemērā šis uzņēmums ir USMF.
2. Pārbaudiet savienojumu ar SharePoint Server instanci, lai pārliecinātos, ka jums ir piešķirta piekļuve.

[![Dokumentu pārvaldības iestatījums — SharePoint server](./media/GERImportFromSharePoint-03-SharePointSetup.png)](./media/GERImportFromSharePoint-03-SharePointSetup.png)

3. Atveriet konfigurēto SharePoint vietni un izveidojiet tālāk norādītās mapes, kur var uzglabāt ienākošos failus.

    - Failu importēšanas avots (galvenais)
    - Failu importēšanas avots (alternatīvais)

[![Dokumentu pārvaldības iestatījums — SharePoint server](./media/GERImportFromSharePoint-04-SharePointFolder1.png)](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

[![Dokumentu pārvaldības iestatījums — SharePoint server](./media/GERImportFromSharePoint-05-SharePointFolder2.png)](./media/GERImportFromSharePoint-05-SharePointFolder2.png)

4. Programmas Finance and Operations lapā **Dokumentu tipi** izveidojiet tālāk norādītos dokumentu tipus, kas tiks izmantoti, lai piekļūtu jūsu tikko izveidotajām SharePoint mapēm.

    - SP galvenais
    - SP alternatīvais

5. Izveidotajiem dokumentu tipiem laukā **Grupa** ievadiet **Fails** un laukā **Atrašanās vieta** ievadiet **SharePoint**. Pēc tam ievadiet SharePoint mapes adresi tālāk norādītajā veidā.

    - Dokumentu tipam **SP galvenais**: Failu importa avots (galvenais)
    - Dokumentu tipam **SP alternatīvais**: Failu importa avots (alternatīvais)

[![SharePoint iestatījums — jauns dokumentu tips](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>ER avotu konfigurēšana ER formātam
1. Noklikšķiniet uz **Organizācijas administrēšana** > **Elektroniskie pārskati** > **Elektronisko pārskatu avots**.
2. Lapā **Elektronisko pārskatu avots** konfigurējiet avota failus datu importēšanai, izmantojot konfigurēto ER formātu.
3. Definējiet faila nosaukuma masku, lai tiktu importēti tikai faili ar paplašinājumu .xlsx. Faila nosaukuma maska nav obligāta, un tā tiek izmantota tikai tad, ja tāda ir definēta. Katram ER formātam var definēt tikai vienu masku.
4. Atlasiet abas iepriekš izveidotās SharePoint mapes.

[![ER failu avota iestatījums](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
>ER *avots* tiek definēts katram programmas uzņēmumam atsevišķi. Savukārt ER *konfigurācijas* tiek koplietotas dažādos uzņēmumos.

> [!NOTE]
> Kad dzēšat ER avota iestatījumu kādam ER formātam, tiek izdzēsti arī visi pievienotie failu stāvokļi (skatiet tālāk).

## <a name="review-the-files-states-for-the-er-format"></a>Failu stāvokļu pārskatīšana ER formātam
1. Lapā **Elektronisko pārskatu avots** atlasiet **Failu stāvokļi avotiem**, lai pārskatītu konfigurēto failu avotu saturu pašreizējam ER formātam.
2. Sadaļā **Faili** pārskatiet failu sarakstu. Šajā sarakstā ir tālāk noradītā informācija.

    - Avota faili, kas ir piemērojami, pamatojoties uz faila nosaukuma masku (ja ir definēta faila nosaukuma maska), un kas ir gatavi datu importēšanai. Šiem failiem sadaļa **Avotu žurnāls importa formātam** ir tukša.
    - Iepriekš importētie faili. Katram no šiem failiem sadaļā **Avotu žurnāls importa formātam** varat pārskatīt attiecīgā faila importēšanas vēsturi.

Varat arī atvērt lapu **Failu stāvokļi avotiem**, atlasot **Organizācijas administrēšana** \> **Elektroniskie pārskati** \> **Failu stāvokļi avotiem**. Tādā gadījumā lapā ir sniegta informācija par failu avotiem visiem ER formātiem, kuriem ir konfigurēti failu avoti tajā uzņēmumā, kurā pašlaik esat pieteicies.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Datu importēšana no Excel failiem, kas atrodas SharePoint mapē
1. Pakalpojumā SharePoint Microsoft Excel failu **1099import-data.xlsx**, kurā atrodas kreditoru transakcijas, augšupielādējiet uz iepriekš izveidoto SharePoint mapi **Failu importēšanas avots (galvenais)**.

[![SharePoint saturs — Microsoft Excel fails importēšanai](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. Programmas Finance and Operations lapā **Failu stāvokļi avotiem** atlasiet **Atsvaidzināt**, lai šo lapu atsvaidzinātu. Ņemiet vērā, ka Excel fails, kuru augšupielādējāt pakalpojumā SharePoint, šajā formā bija redzams ar statusu **Gatavs**. Pašlaik tiek atbalstīti tālāk norādītie statusi.

    - **Gatavs** — automātiski piešķirts katram jaunajam failam SharePoint mapē. Šis statuss nozīmē, ka fails ir gatavs importēšanai.
    - **Importēšana** — ER pārskats to piešķir automātiski, kad importēšanas process šo failu bloķē, lai novērstu iespēju to izmantot ar citiem procesiem (ja daudzi no tiem darbojas vienlaikus).
    - **Importēts** — ER pārskats to piešķir automātiski, kad faila importēšana ir sekmīgi pabeigta. Šis statuss nozīmē, ka importētais fails ir izdzēsts no konfigurētā failu avota (SharePoint mapes).
    - **Nesekmīgi** — ER pārskats to piešķir automātiski, kad faila importēšana ir pabeigta ar kļūdām vai izņēmumiem.
    - **Aizturēts** — to manuāli piešķir šīs formas lietotājs. Šis statuss nozīmē, ka fails pagaidām netiks importēts. Šo statusu var izmantot, lai atliktu dažu failu importēšanu.

[![ER failu stāvokļu lapa atlasītajiem avotiem](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Datu importēšana no SharePoint failiem
1. Atveriet ER konfigurāciju koku, atlasiet **1099 maksājumu modelis** un izvēstiet ER modeļa komponentu sarakstu.
2. Atlasiet modeļa kartēšanas nosaukumu, lai atvērtu sarakstu ar atlasītās ER modeļa konfigurācijas modeļa kartējumiem.

[![ER failu stāvokļu lapa atlasītajiem avotiem](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Atlasiet **Palaist**, lai palaistu atlasīto modeļa kartēšanu. Tā kā jūs konfigurējāt failu avotus šim ER formātam, pēc nepieciešamības varat mainīt opcijas **Faila avots** iestatījumu. Ja paturat šīs opcijas iestatījumu, tiek importēti .xslx faili no konfigurētajiem avotiem (šajā piemērā tās ir SharePoint mapes).

    Šajā piemērā jūs importējat tikai vienu failu. Taču, ja ir vairāki faili, tie tiek atlasīti importēšanai tādā secībā, kādā tie tika pievienoti SharePoint mapei. Katra ER formāta palaišana importē vienu atlasīto failu.

[![ER modeļa kartēšanas palaišana](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Modeļa kartēšanu var palaist neuzraudzītu partijas režīmā. Tādā gadījumā katru reizi, kad partija palaiž šo ER formātu, tiek importēts viens fails no konfigurētajiem failu avotiem. Lai ieviestu šo partijas palaišanu, izmantojiet tālāk norādīto kodu.

    ```
    ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId().run()
    ```

    Kad fails ir sekmīgi importēts no SharePoint mapes, tas tiek izdzēsts no šīs mapes.

5. Ievadiet dokumenta ID, piemēram, **V-00001**, un pēc tam atlasiet **Labi**.

[![ER modeļa kartēšanas palaišana](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. Lapā **Failu stāvokļi avotiem** atlasiet **Atsvaidzināt**, lai šo lapu atsvaidzinātu.

[![ER failu stāvokļu lapa atlasītajiem avotiem](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. Sadaļā **Faili** pārskatiet failu sarakstu. Sadaļā **Avotu žurnāls importa formātam** ir sniegta Excel faila importēšanas vēsture. Tā kā šis fails tika sekmīgi importēts, SharePoint mapē tas ir atzīmēts kā **Dzēsts**.
8. Pārskatiet SharePoint mapi **Failu importa avots (galvenais)**. Excel faili, kas tika sekmīgi importēti, no šīs mapes ir dzēsti.
9. Programmā Finance and Operations atlasiet **Parādi kreditoriem** \> **Periodiskie uzdevumi** \> **Nodoklis 1099** \> **Kreditora nodokļa 1099 nosegšana**.
10. Laukā **No datuma** un laukā **Līdz datumam** ievadiet atbilstošās vērtības. Pēc tam atlasiet **Manuālas 1099 transakcijas**.

    Lapā tiek parādītas kreditoru transakcijas, kas tika importētas no Excel failiem pakalpojumā SharePoint dokumentam **V-00001**.

[![1099 kreditoru transakciju lapa](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Excel faila sagatavošana importēšanai
1. Atveriet Excel failu, ko izmantojāt iepriekš. 3. rindas 1. kolonnā pievienojiet kreditora kodu, kas nepastāv programmā. Pievienojiet šai rindai papildu aplamu kreditora informāciju.

[![Microsoft Excel faila paraugs importēšanai no SharePoint](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Atjaunināto Excel failu, kurā ir kreditoru transakcijas, augšupielādējiet uz SharePoint mapi **Failu importa avots (galvenais)**.
3. Programmā Finance and Operations atveriet ER konfigurāciju koku, atlasiet **1099 maksājumu modelis** un izvēstiet ER modeļa komponentu sarakstu.
4. Atlasiet modeļa kartēšanas nosaukumu, lai atjauninātu modeļa kartēšanu tā, ka datu importēšanas procesa laikā nepareizais kreditora kods tiek uzskatīts par kļūdu.
5. Atlasiet **Noformētājs**.
6. Cilnē **Validācijas** jums ir jāmaina pēcvalidācijas darbība attiecībā uz validācijas kārtulu, kas bija konfigurēta, lai novērtētu, vai programmā pastāv importētais kreditora konts. Lauka **Pēcvalidācijas darbība** vērtību atjauniniet uz **Apturēt izpildi**, saglabājiet veiktās izmaiņas un aizveriet lapu.

[![ER modeļa kartēšanas noformētāja lapa](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Saglabājiet veiktās izmaiņas un aizveriet ER modeļa kartēšanas noformētāju.
8. Atlasiet **Palaist**, lai palaistu modificēto ER modeļa kartēšanu.
9. Ievadiet dokumenta ID, piemēram, **V-00002**, un pēc tam atlasiet **Labi**.

    Ņemiet vērā, ka informācijas žurnālā ir paziņojums par to, ka SharePoint mapē esošā failā ir nepareizs kreditora konts un to nevar importēt.

[![ER modeļa kartēšanas palaišana](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. Lapā **Failu stāvokļi avotiem** atlasiet **Atsvaidzināt** un pēc tam sadaļā **Faili** pārskatiet failu sarakstu.

[![ER failu stāvokļu lapa atlasītajiem avotiem](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

Sadaļā **Avotu žurnāls importa formātam** ir norādīts, ka importēšanas process bija nesekmīgs un ka fails joprojām atrodas SharePoint mapē (nav atzīmēta izvēles rūtiņa **Ir dzēsts**). Ja izlabojat šo failu pakalpojumā SharePoint, pievienojot atbilstošu kreditora kodu, un pēc tam faila statusu no **Nesekmīgi** maināt uz **Gatavs** sadaļā **Avotu žurnāls importa formātam**, varat šo failu importēt vēlreiz.

11. Pārskatiet SharePoint mapi **Failu importa avots (galvenais)**. Ievērojiet, ka Excel fails, kas netika importēts, joprojām atrodas šajā mapē.
12. Programmā Finance and Operations atlasiet **Parādi kreditoriem** \> **Periodiskie uzdevumi** \> **Nodoklis 1099** \> **Kreditora nodokļa 1099 nosegšana** ievadiet atbilstošās vērtības laukā **No datuma** un **Līdz datumam**, un pēc tam atlasiet **Manuālas 1099 transakcijas**.

    Ir pieejamas tikai transakcijas dokumentam V-00001. Nav pieejama neviena transakcija dokumentam V-00002, lai gan Excel failā tika atrasta kļūda pēdējai importētajai transakcijai.

