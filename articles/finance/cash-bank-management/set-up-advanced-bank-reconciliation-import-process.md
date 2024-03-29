---
title: Iestatīt detalizētās bankas darbību saskaņošanas importa procesu
description: Detalizētās bankas darbību saskaņošanas funkcija ļauj jums importēt elektroniskos bankas izrakstus un automātiski saskaņot tos ar bankas Microsoft Dynamics darbībām 365 Finansēs. Šajā rakstā ir paskaidrots, kā iestatīt importēšanas funkcionalitāti saviem bankas izrakstiem.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60195962e50817b4d85840a2464848db6e666f46
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716023"
---
# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Iestatīt detalizētās bankas darbību saskaņošanas importa procesu

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Šī funkcionalitāte tiks nolietota 2022. gada septembrī, jaunajiem lietotājiem būs jāizmanto elektroniskie pārskati. Papildinformāciju skatiet sadaļā Detalizētas [bankas darbību saskaņošanas importēšanas iestatīšana, izmantojot elektroniskos pārskatus](../accounts-payable/import-bai2-er.md).


Detalizētās bankas darbību saskaņošanas līdzeklis ļauj jums importēt elektroniskos bankas izrakstus un automātiski saskaņot tos ar bankas darbībām programmā Dynamics 365 Finance. Šajā rakstā ir paskaidrots, kā iestatīt importēšanas funkcionalitāti saviem bankas izrakstiem. 

Bankas izraksta importēšanas iestatījumi ir dažādi, un tie ir atkarīgi no jūsu elektroniskā bankas izraksta formāta. Finance atbalsta trīs bankas izraksta formātus: ISO20022, MT940 un BAI2.

## <a name="set-time-zone-preference"></a>Iestatīt laika joslas preferenci
Konfigurējot bankas izrakstu importēšanas iestatījumus, var būt svarīgi ņemt vērā datuma un laika datu laika joslu importējamos bankas izraksta failos. Pēc noklusējuma tiek pieņemts, ka datuma un laika vērtības jau ir universālajā coordinētajā laikā (UTC) un tāpēc, importējot datus, netiks lietota laika zonas konvertēšana. 

Ir pieejama opcija norādīt laika joslu, ko izmantot datu importēšanai. Šī opcija ir pieejama laukā **Laika joslas preference** katrā **Avota datu formāta detalizēta informācija** lapā (**Datu pārvaldības darbvieta > Konfigurēt datu avotus > Atlasīt datu formātu > Reģionālie iestatījumi** Kopsavilkuma cilnē). Šī jūsu ievadītā laika joslas preference tiks piemērota visiem importējumiem, kas izmanto šo avota datu formātu. Lai importētu datus no vairākām laika zonām, var izveidot tik daudz datu avota formātu, cik nepieciešams.  

Šī laika josla var nebūt tāda pati kā lietotāja vai uzņēmuma laika josla, tāpēc noteikti precizējiet, kādu laika joslu izmanto datuma un laika dati. Iestatot laika joslas preferenci, ieteicams apsvērt šādus punktus. 

 - Jūsu ievadītā laika joslas preference tiks piemērota visiem importējumiem, kas izmanto šo avota datu formātu. Lai apstrādātu datu importēšanu no vairākām laika zonām, var izveidot tik daudz datu avota formātu, cik nepieciešams. 
 
 - Laika joslas preferencei vajadzētu būt datuma un laika datu vietējai laika joslai importēšanas failā. 
 
 - Datuma un laika datu laika josla var nebūt tāda pati kā lietotāja vai uzņēmuma laika josla.
 
 - Lietotāji var pielāgot savu laika joslu, izmantojot **Lietotāja opcijas**.

Ievērojiet, ka, importējot bankas izrakstus, tālāk norādītās darbības var palīdzēt samazināt iespējamos datumu un laiku konfliktus. 

 - Nemainiet laika joslas preferences visiem bankas kontiem, kuriem paziņojumi jau ir importēti. Laika joslas preferences maiņa var ietekmēt jaunu izrakstu pasūtīšanu, saistībā ar esošiem izrakstiem, laika joslas korekcijas dēļ. 
 
 - Pārskatiet visas importēšanas, kuri izmanto atlasīto datu avota formātu. Formātam norādītā laika joslas preference tiks piemērota visiem importēšanas projektiem, kas izmanto šo formātu. Verificējiet, ka laika joslas preference ir piemērota visiem importēšanas projektiem, kas izmanto šo formātu.

## <a name="sample-files"></a>Parauga faili
Visiem trim formātiem jums ir nepieciešami faili, kas elektronisko bankas izrakstu no sākotnējā formātā pārveido formātā, kuru var izmantot Finance. Nepieciešamie resursu faili ir pieejami Microsoft Visual Studio lietojumprogrammu pārlūka mezglā **Resursi**. Kad faili ir atrasti, kopējiet tos uz vienu zināmu vietu, lai iestatīšanas procesa laikā tos varētu ērti augšupielādēt.

| Resursa nosaukums                                           | Faila nosaukums                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt              | BAI2CSV-to-BAI2XML.xslt              |
| BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| BankStmtImport\_BankReconciliation\_to\_Composite\_xslt | BankReconciliation-to-Composite.xslt |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport\_SampleBankCompositeEntity\_xml          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Bankas izrakstu formātu un tehnisko izkārtojumu paraugi
Tālāk ir sniegti detalizētās bankas darbību saskaņošanas importētā faila tehnisko izkārtojumu definīciju paraugi un trīs saistītie bankas izrakstu parauga faili: [Failu piemēru importēšana](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Tehniskā izkārtojuma definīcija                             | Bankas izraksta parauga fails          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |



## <a name="set-up-the-import-of-iso20022-bank-statements"></a>Iestatīt ISO20022 bankas izrakstu importu
Vispirms ir jādefinē bankas izraksta formāta apstrādes grupa ISO20022 bankas izrakstiem, izmantojot datu elementa struktūru.

1.  Dodieties uz **Darbvietas** &gt; **Datu pārvaldība**.
2.  Noklikšķiniet uz **Importēt**.
3.  Ievadiet formāta nosaukumu, piemēram, **ISO20022**.
4.  Laukam **Avota datu formāts** iestatiet vērtību **XML elements**.
5.  Laukam **Elementa nosaukums** iestatiet vērtību **Bankas izraksti**.
6.  Lai augšupielādētu importa failus, noklikšķiniet uz **Augšupielādēt** un pēc tam pārlūkojiet, lai atlasītu iepriekš saglabāto failu **SampleBankCompositeEntity.xml**.
7.  Kad bankas izrakstu elements ir augšupielādēts un kartēšana ir pabeigta, noklikšķiniet uz darbības **Skatīt karti** šim elementam.
8.  Bankas izrakstu elements ir saliktais elements, kas sastāv no četriem atsevišķiem elementiem. Sarakstā atlasiet vienumu **BankStatementDocumentEntity** un pēc tam noklikšķiniet uz darbības **Skatīt karti**.
9.  Cilnē **Transformācijas** noklikšķiniet uz **Jauns**.
10. Kārtas numuram 1 noklikšķiniet uz **Augšupielādēt failu** un atlasiet iepriekš saglabāto failu **ISO20022XML-to-Reconciliation.xslt**. **Piezīme.** Transformāciju faili ir veidoti standarta formātam. Tā kā bankas bieži vien novirzās no šī formāta, jums var būt jāatjaunina transformācijas fails, lai kartētu uz savu bankas izraksta formātu. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. Noklikšķiniet uz **Jauns**.
12. Kārtas numuram 2 noklikšķiniet uz **Augšupielādēt failu** un atlasiet iepriekš saglabāto failu **BankReconciliation-to-Composite.xslt**.
13. Noklikšķiniet uz **Lietot transformācijas**.

Kad formāta apstrādes grupa ir iestatīta, ir jādefinē bankas izraksta formāta kārtulas ISO20022 bankas izrakstiem.

1.  Dodieties uz **Skaidras naudas un bankas vadība** &gt; **Iestatīšana** &gt; **Detalizētas bankas darbību saskaņošanas iestatīšana** &gt; **Bankas izraksta formāts**.
2.  Noklikšķiniet uz **Jauns**.
3.  Norādiet pārskata formātu, piemēram, **ISO20022**.
4.  Ievadiet formāta nosaukumu.
5.  Lauku **Apstrādes grupa** iestatiet uz iepriekš definēto grupu, piemēram, **ISO20022**.
6.  Atzīmējiet izvēles rūtiņu **XML fails**.

Visbeidzot ir jāiespējo detalizētā bankas darbību saskaņošana un jāiestata izraksta formāts bankas kontā.

1.  Dodieties uz **Skaidras naudas un bankas vadība** &gt; **Banku konti**.
2.  Atlasiet bankas kontu un atveriet to, lai skatītu detalizētu informāciju.
3.  Cilnē **Saskaņošana** opciju **Detalizētā bankas darbību saskaņošana** iestatiet uz **Jā**.
4.  Lauku **Izraksta formāts** iestatiet uz iepriekš izveidoto formātu, piemēram, **ISO20022**.

## <a name="set-up-the-import-of-mt940-bank-statements"></a>Iestatīt MT940 bankas izrakstu importu
Vispirms ir jādefinē bankas izraksta formāta apstrādes grupa MT940 bankas izrakstiem, izmantojot datu elementa struktūru.

1.  Dodieties uz **Darbvietas** &gt; **Datu pārvaldība**.
2.  Noklikšķiniet uz **Importēt**.
3.  Ievadiet formāta nosaukumu, piemēram, **MT940**.
4.  Laukam **Avota datu formāts** iestatiet vērtību **XML elements**.
5.  Laukam **Elementa nosaukums** iestatiet vērtību **Bankas izraksti**.
6.  Lai augšupielādētu importa failus, noklikšķiniet uz **Augšupielādēt** un pēc tam pārlūkojiet, lai atlasītu iepriekš saglabāto failu **SampleBankCompositeEntity.xml**.
7.  Kad bankas izrakstu elements ir augšupielādēts un kartēšana ir pabeigta, noklikšķiniet uz darbības **Skatīt karti** šim elementam.
8.  Bankas izrakstu elements ir saliktais elements, kas sastāv no četriem atsevišķiem elementiem. Sarakstā atlasiet vienumu **BankStatementDocumentEntity** un pēc tam noklikšķiniet uz darbības **Skatīt karti**.
9.  Cilnē **Transformācijas** noklikšķiniet uz **Jauns**.
10. Kārtas numuram 1 noklikšķiniet uz **Augšupielādēt failu** un atlasiet iepriekš saglabāto failu **MT940TXT-to-MT940XML.xslt**.
11. Noklikšķiniet uz **Jauns**.
12. Kārtas numuram 2 noklikšķiniet uz **Augšupielādēt failu** un atlasiet iepriekš saglabāto failu **MT940XML-to-Reconciliation.xslt**. **Piezīme.** Transformāciju faili ir veidoti standarta formātam. Tā kā bankas bieži vien novirzās no šī formāta, jums var būt jāatjaunina transformācijas fails, lai kartētu uz savu bankas izraksta formātu. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. Noklikšķiniet uz **Jauns**.
14. Kārtas numuram 3 noklikšķiniet uz **Augšupielādēt failu** un atlasiet iepriekš saglabāto failu **BankReconciliation-to-Composite.xslt**.
15. Noklikšķiniet uz **Lietot transformācijas**.

Kad formāta apstrādes grupa ir iestatīta, ir jādefinē bankas izraksta formāta kārtulas MT940 bankas izrakstiem.

1.  Dodieties uz **Skaidras naudas un bankas vadība** &gt; **Iestatīšana** &gt; **Detalizētas bankas darbību saskaņošanas iestatīšana** &gt; **Bankas izraksta formāts**.
2.  Noklikšķiniet uz **Jauns**.
3.  Norādiet pārskata formātu, piemēram, **MT940**.
4.  Ievadiet formāta nosaukumu.
5.  Lauku **Apstrādes grupa** iestatiet uz iepriekš definēto grupu, piemēram, **MT940**.
6.  Laukam **Faila tips** iestatiet vērtību **txt**.

Visbeidzot ir jāiespējo detalizētā bankas darbību saskaņošana un jāiestata izraksta formāts bankas kontā.

1.  Dodieties uz **Skaidras naudas un bankas vadība** &gt; **Banku konti**.
2.  Atlasiet bankas kontu un atveriet to, lai skatītu detalizētu informāciju.
3.  Cilnē **Saskaņošana** opciju **Detalizētā bankas darbību saskaņošana** iestatiet uz **Jā**.
4.  Kad tiek piedāvāts apstiprināt jūsu izvēli un iespējot detalizēto bankas darbību saskaņošanu, noklikšķiniet uz **Labi**.
5.  Lauku **Izraksta formāts** iestatiet uz iepriekš izveidoto formātu, piemēram, **MT940**.

## <a name="set-up-the-import-of-bai2-bank-statements"></a>Iestatīt BAI2 bankas izrakstu importu
Vispirms ir jādefinē bankas izraksta formāta apstrādes grupa BAI2 bankas izrakstiem, izmantojot datu elementa struktūru.

1.  Dodieties uz **Darbvietas** &gt; **Datu pārvaldība**.
2.  Noklikšķiniet uz **Importēt**.
3.  Ievadiet formāta nosaukumu, piemēram, **BAI2**.
4.  Laukam **Avota datu formāts** iestatiet vērtību **XML elements**.
5.  Laukam **Elementa nosaukums** iestatiet vērtību **Bankas izraksti**.
6.  Lai augšupielādētu importa failus, noklikšķiniet uz **Augšupielādēt** un pēc tam pārlūkojiet, lai atlasītu iepriekš saglabāto failu **SampleBankCompositeEntity.xml**.
7.  Kad bankas izrakstu elements ir augšupielādēts un kartēšana ir pabeigta, noklikšķiniet uz darbības **Skatīt karti** šim elementam.
8.  Bankas izrakstu elements ir saliktais elements, kas sastāv no četriem atsevišķiem elementiem. Sarakstā atlasiet vienumu **BankStatementDocumentEntity** un pēc tam noklikšķiniet uz darbības **Skatīt karti**.
9.  Cilnē **Transformācijas** noklikšķiniet uz **Jauns**.
10. Kārtas numuram 1 noklikšķiniet uz **Augšupielādēt failu** un atlasiet iepriekš saglabāto failu **BAI2CSV-to-BAI2XML.xslt**.
11. Noklikšķiniet uz **Jauns**.
12. Kārtas numuram 2 noklikšķiniet uz **Augšupielādēt failu** un atlasiet iepriekš saglabāto failu **BAI2XML-to-Reconciliation.xslt**. **Piezīme.** Transformāciju faili ir veidoti standarta formātam. Tā kā bankas bieži vien novirzās no šī formāta, jums var būt jāatjaunina transformācijas fails, lai kartētu uz savu bankas izraksta formātu. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. Noklikšķiniet uz **Jauns**.
14. Kārtas numuram 3 noklikšķiniet uz **Augšupielādēt failu** un atlasiet iepriekš saglabāto failu **BankReconciliation-to-Composite.xslt**.
15. Noklikšķiniet uz **Lietot transformācijas**.

Kad formāta apstrādes grupa ir iestatīta, ir jādefinē bankas izraksta formāta kārtulas BAI2 bankas izrakstiem.

1.  Dodieties uz **Skaidras naudas un bankas vadība** &gt; **Iestatīšana** &gt; **Detalizētas bankas darbību saskaņošanas iestatīšana** &gt; **Bankas izraksta formāts**.
2.  Noklikšķiniet uz **Jauns**.
3.  Norādiet pārskata formātu, piemēram, **BAI2**.
4.  Ievadiet formāta nosaukumu.
5.  Lauku **Apstrādes grupa** iestatiet uz iepriekš definēto grupu, piemēram, **BAI2**.
6.  Laukam **Faila tips** iestatiet vērtību **txt**.

Visbeidzot ir jāiespējo detalizētā bankas darbību saskaņošana un jāiestata izraksta formāts bankas kontā.

1.  Dodieties uz **Skaidras naudas un bankas vadība** &gt; **Banku konti**.
2.  Atlasiet bankas kontu un atveriet to, lai skatītu detalizētu informāciju.
3.  Cilnē **Saskaņošana** opciju **Detalizētā bankas darbību saskaņošana** iestatiet uz **Jā**.
4.  Kad tiek piedāvāts apstiprināt jūsu izvēli un iespējot detalizēto bankas darbību saskaņošanu, noklikšķiniet uz **Labi**.
5.  Lauku **Izraksta formāts** iestatiet uz iepriekš izveidoto formātu, piemēram, **BAI2**.

## <a name="test-the-bank-statement-import"></a>Testēt bankas izraksta importēšanu
Visbeidzot ir jāpārbauda, vai varat importēt savu bankas izrakstu.

1.  Dodieties uz **Skaidras naudas un bankas vadība** &gt; **Banku konti**.
2.  Atlasiet bankas kontu, kam ir iespējota detalizētās bankas darbību saskaņošanas funkcionalitāte.
3.  Cilnē **Saskaņot** noklikšķiniet uz **Bankas izraksti**.
4.  Lapā **Bankas izraksts** noklikšķiniet uz **Importēt izrakstu**.
5.  Laukam **Bankas konts** iestatiet atlasīto bankas kontu. Lauks **Pārskata formāts** tiks iestatīts automātiski, pamatojoties uz bankas konta iestatījumiem.
6.  Noklikšķiniet uz **Pārlūkot** un atlasiet savu elektroniskā bankas izraksta failu.
7.  Noklikšķiniet uz **Augšupielādēt**.
8.  Noklikšķiniet uz **Labi**.

Ja importēšana notika sekmīgi, jūs saņemat ziņojumu, ka jūsu izraksts tika importēts. Ja importēšana nebija sekmīga, darbvietas **Datu pārvaldība** sadaļā **Darbu vēsture** atrodiet šo darbu. Noklikšķiniet uz **Detalizēta informācija par izpildi** šim darbam, lai atvērtu lapu **Izpildes kopsavilkums**, un pēc tam noklikšķiniet uz **Skatīt izpildes žurnālu**, lai skatītu importēšanas kļūdas.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
