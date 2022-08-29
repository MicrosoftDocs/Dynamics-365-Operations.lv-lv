---
title: Datu importēšanas no SharePoint konfigurēšana
description: Šajā rakstā skaidrots, kā importēt datus no Microsoft SharePoint.
author: kfend
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 11208267de0cc35db55c64ccf2de224df854404d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277792"
---
# <a name="configure-data-import-from-sharepoint"></a>Datu importēšanas no SharePoint konfigurēšana

[!include[banner](../includes/banner.md)]

Lai importētu datus no ienākoša faila, izmantojot elektronisko pārskatu (Electronic reporting — ER) struktūru, ir nepieciešams konfigurēt ER formātu, kas atbalsta importēšanu, un pēc tam palaist modeļa kartēšanu ar tipu **Uz galamērķi**, kas šo formātu izmanto kā datu avotu. Lai importētu datus, ir jāpāriet uz failu, kuru vēlaties importēt. Ienākošo failu lietotājs var atlasīt manuāli. Jaunā ER iespēja atbalstīt datu importēšanu no Microsoft SharePoint sniedz iespēju konfigurēt šo procesu kā neuzraudzītu. Varat izmantot ER konfigurācijas, lai importētu datus no failiem, kas tiek glabāti Microsoft SharePoint mapēs. Šajā rakstā skaidrots, kā pabeigt importēšanu no SharePoint. Piemēros kā biznesa dati tiek izmantotas kreditoru transakcijas.

## <a name="prerequisites"></a>Priekšnosacījumi
Lai pabeigtu piemērus šajā rakstā, jums ir jābūt šādai piekļuvei:

- Piekļuve vienai no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

- Piekļūstiet Microsoft SharePoint Server instancei, kas ir konfigurēta lietošanai kopā ar programmu.
- ER formātu un modeļu konfigurācijas 1099 maksājumiem.

### <a name="create-required-er-configurations"></a>Nepieciešamo ER konfigurāciju izveidošana
Noskatieties uzdevumu ceļvežus **ER: datu importēšana no Microsoft Excel faila**, kas ir ietverti biznesa procesā **7.5.4.3. IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)**. Šajos uzdevumu ceļvežos ir detalizēti aprakstīta ER konfigurāciju izstrāde un izmantošana, lai interaktīvā veidā importētu kreditoru transakcijas no Microsoft Excel failiem. Plašāku informāciju skatiet tēmā [Ienākošo dokumentu parsēšana programmā Excel formātā](parse-incoming-documents-excel.md). Pēc tam, kad būsiet noskatījies uzdevumu ceļvežus, jums būs tālāk norādītie iestatījumi.

#### <a name="er-configurations"></a>ER konfigurācijas

- ER modeļa konfigurācija **1099 maksājumu modelis**
- ER formāta konfigurācija **Formāts kreditoru transakciju importēšanai no Excel**

![ER konfigurācijas datu importēšanai no SharePoint.](./media/GERImportFromSharePoint-01-Configurations.PNG)

#### <a name="sample-of-the-incoming-file-for-data-import"></a>Ienākošā faila paraugs datu importēšanai

- Excel fails **1099import-data.xlsx** ar kreditoru transakcijām, kas ir jāimportē programmā.

![Excel faila paraugs importēšanai no SharePoint.](./media/GERImportFromSharePoint-02-Excel.PNG)
    
> [!NOTE]
> Formāts kreditoru transakciju importēšanai ir atlasīts kā noklusējuma modeļa kartēšana. Tādēļ, ja palaižat modeļa kartēšanu **1099 maksājumu modelis** un šī modeļa kartēšana ir ar tipu **Uz galamērķi**, modeļa kartēšana palaiž šo formātu, lai importēt datus no ārējiem failiem. Pēc tam tā izmanto šos datus, lai atjauninātu programmas tabulas.

## <a name="configure-access-to-sharepoint-for-file-storage"></a>SharePoint piekļuves konfigurēšana failu glabāšanai
Lai glabātu elektronisko pārskatu failus SharePoint vietā, ir jākonfigurē piekļuve SharePoint Server instancei, ko izmantos pašreizējais uzņēmums. Šajā piemērā šis uzņēmums ir USMF. Norādījumus skatiet rakstā [Krātuves SharePoint konfigurēšana](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage).

1. Veiciet rakstā [Krātuves SharePoint konfigurēšana](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage) norādītās darbības.
2. Atveriet konfigurēto SharePoint vietni.
3. Izveidojiet šādas mapes ienākošo elektronisko pārskatu failu glabāšanai:

     - Failu importēšanas avots (Galvenais) (Piemērs parādīts ekrānuzņēmumā tālāk)
     - Failu importēšanas avots (alternatīvais)

    ![Failu importēšanas avots (galvenais).](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

4. (Neobligāti) Failu glabāšanai pēc importēšanas izveidojiet tālāk norādītās mapes. 

    - Failu arhīva mape — mape veiksmīgi importētajiem failiem.
    - Failu ar brīdinājumiem mape — mape failiem, kas ir importēti ar brīdinājumu.
    - Kļūdaino failu mape — mape failiem, kuru importēšana neizdevās.

4. Dodieties uz **Organizācijas administrēšana > Dokumentu pārvaldība > Dokumentu veidi**.
5. Izveidojiet tālāk norādīto tipu dokumentus, kas tiks izmantoti, lai piekļūtu izveidotajām SharePoint mapēm. Norādījumus skatiet sadaļā [Dokumentu tipu konfigurēšana](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types).

|Dokumenta tips       | Grupa              | Vieta      | SharePoint mape      |
|--------------------|--------------------|---------------|------------------------|
|SP galvenais             |Fails                |SharePoint     |Failu importēšanas avots (galvenais)|
|SP alternatīvais             |Fails                |SharePoint     |Failu importēšanas avots (alternatīvais)|
|SP arhīvs             |Fails                |SharePoint     |Failu arhīva mape|
|SP brīdinājums             |Fails                |SharePoint     |Failu ar brīdinājumiem mape|
|SP kļūda             |Fails                |SharePoint     |Kļūdaino failu mape|

![SharePoint iestatījums — jauns dokumentu tips.](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>ER avotu konfigurēšana ER formātam
1. Noklikšķiniet uz **Organizācijas administrēšana** \> **Elektroniskie pārskati** \> **Elektronisko pārskatu avots**.
2. Lapā **Elektronisko pārskatu avots** konfigurējiet avota failus datu importēšanai, izmantojot konfigurēto ER formātu.
3. Definējiet faila nosaukuma masku, lai tiktu importēti tikai faili ar paplašinājumu .xlsx. Faila nosaukuma maska nav obligāta, un tā tiek izmantota tikai tad, ja tāda ir definēta. Katram ER formātam var definēt tikai vienu masku.
4. Mainiet iestatījumu **Kārtot failus pirms importēšanas** uz **Nekārtot**, ja ir vairāki faili importēšanai un importēšanas secība nav svarīga.
5. Atlasiet visas iepriekš izveidotās SharePoint mapes.

    [![ER failu avota iestatījums.](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
> - ER *avots* tiek definēts katram programmas uzņēmumam atsevišķi. Savukārt ER *konfigurācijas* tiek koplietotas dažādos uzņēmumos.
> - Kad dzēšat ER avota iestatījumu kādam ER formātam, pēc apstiprināšanas tiek dzēsti arī visi pievienotie failu stāvokļi (skatiet tālāk).

## <a name="review-the-files-states-for-the-er-format"></a>Failu stāvokļu pārskatīšana ER formātam
1. Lapā **Elektronisko pārskatu avots** atlasiet **Failu stāvokļi avotiem**, lai pārskatītu konfigurēto failu avotu saturu pašreizējam ER formātam.
2. Sadaļā **Faili** pārskatiet failu sarakstu. Šajā sarakstā ir tālāk noradītā informācija.

    - Avota faili, kas ir piemērojami, pamatojoties uz faila nosaukuma masku (ja ir definēta faila nosaukuma maska), un kas ir gatavi datu importēšanai. Šiem failiem sadaļa **Avotu žurnāls importa formātam** ir tukša.
    - Iepriekš importētie faili. Katram no šiem failiem sadaļā **Avotu žurnāls importa formātam** varat pārskatīt attiecīgā faila importēšanas vēsturi.

Varat arī atvērt lapu **Failu stāvokļi avotiem**, atlasot **Organizācijas administrēšana** \> **Elektroniskie pārskati** \> **Failu stāvokļi avotiem**. Tādā gadījumā lapā ir sniegta informācija par failu avotiem visiem ER formātiem, kuriem ir konfigurēti failu avoti tajā uzņēmumā, kurā pašlaik esat pieteicies.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Datu importēšana no Excel failiem, kas atrodas SharePoint mapē
1. Pakalpojumā SharePoint augšupielādējiet Microsoft Excel failu **1099import-data.xlsx**, kurā ir ietvertas kreditoru transakcijas, iepriekš izveidotajā SharePoint mapē **Failu importēšanas avots (galvenais)**.

    [![SharePoint saturs — importējamais Microsoft Excel fails.](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. Lapā **Failu stāvokļi avotiem** atlasiet **Atsvaidzināt**, lai šo lapu atsvaidzinātu. Pakalpojumā SharePoint augšupielādētajam Excel failam šajā lapā tiek rādīts statuss **Gatavs**. Pašlaik tiek atbalstīti tālāk norādītie statusi.

    - **Gatavs** — tiek automātiski piešķirts katram jaunajam failam SharePoint mapē. Šis statuss nozīmē, ka fails ir gatavs importēšanai.
    - **Importēšana** — ER pārskats to piešķir automātiski, kad importēšanas process šo failu bloķē, lai novērstu iespēju to izmantot ar citiem procesiem (ja daudzi no tiem darbojas vienlaikus).
    - **Importēts** — ER pārskats to piešķir automātiski, kad faila importēšana ir sekmīgi pabeigta. Šis statuss nozīmē, ka importētais fails ir izdzēsts no konfigurētā failu avota (SharePoint mapes).
    - **Nesekmīgi** — ER pārskats to piešķir automātiski, kad faila importēšana ir pabeigta ar kļūdām vai izņēmumiem.
    - **Aizturēts** — to manuāli piešķir šīs lapas lietotājs. Šis statuss nozīmē, ka fails pagaidām netiks importēts. Šo statusu var izmantot, lai atliktu dažu failu importēšanu.

    [![Atjaunināta ER failu stāvokļu lapa atlasītajiem avotiem.](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Datu importēšana no SharePoint failiem
1. Atveriet ER konfigurāciju koku, atlasiet **1099 maksājumu modelis** un izvēstiet ER modeļa komponentu sarakstu.
2. Atlasiet modeļa kartēšanas nosaukumu, lai atvērtu sarakstu ar atlasītās ER modeļa konfigurācijas modeļa kartējumiem.

    [![Lapa Konfigurācija.](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Atlasiet **Palaist**, lai palaistu atlasīto modeļa kartēšanu. Tā kā jūs konfigurējāt failu avotus šim ER formātam, pēc nepieciešamības varat mainīt opcijas **Faila avots** iestatījumu. Ja saglabājat šīs opcijas iestatījumu, no konfigurētajiem avotiem (šajā piemērā no SharePoint mapēm) tiek importēti .xslx formāta faili.

    Šajā piemērā jūs importējat tikai vienu failu. Taču, ja ir pieejami vairāki faili, tie tiek atlasīti importēšanai tādā secībā, kādā tie tika pievienoti SharePoint mapei. Katra ER formāta palaišana importē vienu atlasīto failu.

    [![Importēšana no SharePoint un ER modeļa kartēšanas palaišana.](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Modeļa kartēšanu var palaist [neuzraudzītu](#limitations) partijas režīmā. Tādā gadījumā katru reizi, kad partija palaiž šo ER formātu, tiek importēts viens fails no konfigurētajiem failu avotiem.

    Kad fails ir veiksmīgi importēts no SharePoint mapes, tas tiek izdzēsts no attiecīgās mapes un pārvietots uz veiksmīgi importēto failu mapi vai mapi, kurā tiek saglabāti ar brīdinājumiem importētie faili. Pretējā gadījumā fails tiek pārvietots uz mapi, kurā faili neizdevās, vai arī tiek glabāts mapē, ja nav iestatīta failu kļūme. 

5. Ievadiet dokumenta ID, piemēram, **V-00001**, un pēc tam atlasiet **Labi**.

    [![ER modeļa kartēšanas palaišana.](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. Lapā **Failu stāvokļi avotiem** atlasiet **Atsvaidzināt**, lai šo lapu atsvaidzinātu.

    [![ER failu stāvokļi avotu lapai.](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. Sadaļā **Faili** pārskatiet failu sarakstu. Sadaļā **Avotu žurnāls importa formātam** ir sniegta Excel faila importēšanas vēsture. Tā kā šis fails ir sekmīgi importēts, SharePoint mapē tas ir atzīmēts ar statusu **Dzēsts**.
8. Pārskatiet SharePoint mapi **Failu importēšanas avots (galvenais)**. Excel faili, kas tika sekmīgi importēti, no šīs mapes ir dzēsti.
9. Dodieties uz **Kreditori** \> **Periodiskie uzdevumi** \> **Nodokļi 1099** \> **Kreditora nodokļa 1099 nosegšana**.
10. Laukā **No datuma** un laukā **Līdz datumam** ievadiet atbilstošās vērtības. Pēc tam atlasiet **Manuālas 1099 transakcijas**.

    Lapā tiek parādītas kreditoru transakcijas, kas tika importētas no Excel failiem pakalpojumā SharePoint dokumentam **V-00001**.

    [![1099 kreditoru transakciju lapa.](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Excel faila sagatavošana importēšanai
1. Atveriet Excel failu, ko izmantojāt iepriekš. 3. rindas 1. kolonnā pievienojiet kreditora kodu, kas nepastāv programmā. Pievienojiet šai rindai papildu aplamu kreditora informāciju.

    [![Pakalpojuma Microsoft Excel faila paraugs importēšanai no SharePoint.](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Augšupielādējiet atjaunināto Excel failu, kurā ir ietvertas kreditoru transakcijas, SharePoint mapē **Failu importēšanas avots (galvenais)**.
3. Atveriet ER konfigurāciju koku, atlasiet **1099 maksājumu modelis** un izvēstiet ER modeļa komponentu sarakstu.
4. Atlasiet modeļa kartēšanas nosaukumu, lai atjauninātu modeļa kartēšanu tā, ka datu importēšanas procesa laikā nepareizais kreditora kods tiek uzskatīts par kļūdu.
5. Atlasiet **Noformētājs**.
6. Cilnē **Validācijas** jums ir jāmaina pēcvalidācijas darbība attiecībā uz validācijas kārtulu, kas bija konfigurēta, lai novērtētu, vai programmā pastāv importētais kreditora konts. Lauka **Pēcvalidācijas darbība** vērtību atjauniniet uz **Apturēt izpildi**, saglabājiet veiktās izmaiņas un aizveriet lapu.

    [![ER modeļa kartēšanas noformētāja lapa.](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Saglabājiet veiktās izmaiņas un aizveriet ER modeļa kartēšanas noformētāju.
8. Atlasiet **Palaist**, lai palaistu modificēto ER modeļa kartēšanu.
9. Ievadiet dokumenta ID, piemēram, **V-00002**, un pēc tam atlasiet **Labi**.

    Informācijas žurnālā ir ietverts paziņojums par to, ka SharePoint mapē ir fails, kurā ir ietverts nepareizs kreditora konts un kuru nevar importēt.

    [![Pabeigta ER modeļa kartēšana.](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. Lapā **Failu stāvokļi avotiem** atlasiet **Atsvaidzināt** un pēc tam sadaļā **Faili** pārskatiet failu sarakstu.

    [![ER failu stāvokļu lapa atlasītajiem avotiem.](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

   Sadaļā **Avotu žurnāls importēšanas formātam** ir norādīts, ka importēšanas process bija nesekmīgs un fails atrodas SharePoint mapē Kļūdainie faili (nav atzīmēta izvēles rūtiņa **Ir dzēsts** ). Ja labojat šo failu pakalpojumā SharePoint, pievienojot pareizo kreditora kodu, un pēc tam pārvietojat to uz SharePoint mapi Failu importēšanas avots (galvenais), varat vēlreiz importēt failu.

11. Atlasiet **Kreditori** \> **Periodiskie uzdevumi** \> **Nodoklis 1099** \> **Kreditora nodokļa 1099 nosegšana**, ievadiet atbilstošās vērtības laukā **No datuma** un **Līdz datumam** un pēc tam atlasiet **Manuālas 1099 transakcijas**.

    Ir pieejamas tikai transakcijas dokumentam V-00001. Nav pieejama neviena transakcija dokumentam V-00002, lai gan Excel failā tika atrasta kļūda pēdējai importētajai transakcijai.

## <a name=""></a><a name="limitations">Ierobežojumi</a>

Dynamics 365 finanšu versijās pirms versijas 10.0.25 ER struktūras lietotāja interfeiss (UI) nepiedāvā iespēju iniciēt jaunu pakešuzdevumu, kas izpildīs modeļa kartēšanu datu importēšanai ne apmeklētajā režīmā. Tā vietā ir jāizveido jauna loģika, lai konfigurēto ER modeļa kartēšanu varētu izsaukt no programmas UI, lai importētu datus no ienākošajiem failiem. Lai izstrādātu šo loģiku, ir nepieciešams tehniskais darbs. 

Papildinformāciju par atbilstošo ER API skatiet sadaļā Kods [datu](er-apis-app73.md#code-to-run-a-format-mapping-for-data-import)[importēšanas sadaļas datu importēšanai ER struktūras API izmaiņu palaišanai programmu atjaunināšanai 7.3](er-apis-app73.md). Pārskatiet kodu modeļa `Application Suite` klasē `BankImport_RU`, lai skatītu, kā var īstenot pielāgoto loģiku. Klase `BankImport_RU` paplašina klasi `RunBaseBatch`. It īpaši pārskatiet `runER()` metodi, kurā `ERIModelMappingDestinationRun` objekts ir izveidots kā ER modeļa kartēšanas pasūtījums.

Finanšu versijā 10.0.25 vai jaunākā versijā ER struktūras UI piedāvā iespēju iniciēt jaunu pakešuzdevumu, kas izpildīs datu importēšanas modeļa kartēšanu neraudzītā režīmā. Papildinformāciju par šo procesu skatiet sadaļā [Datu importēšana pakešveida režīmā no manuāli atlasītiem failiem](er-configure-data-import-batch.md).

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[ER struktūras API izmaiņas programmas atjauninājumam 7.3](er-apis-app73.md)

[ER struktūras API izmaiņas programmas atjauninājumam 10.0.23](er-apis-app10-0-23.md)

[ER struktūras API izmaiņas programmas atjauninājumam 10.0.25](er-apis-app10-0-25.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
