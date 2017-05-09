---
title: "Iestatīt detalizētās bankas darbību saskaņošanas importa procesu"
description: "Līdzeklis Detalizētā bankas darbību saskaņošana jums ļauj importēt elektroniskus bankas izrakstus un automātiski saskaņot tos ar bankas transakcijām programmatūrā Microsoft Dynamics 365 for Operations Šajā rakstā ir paskaidrots, kā iestatīt importēšanas funkcionalitāti saviem bankas izrakstiem."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eab840b2974f4e9e8cf542c146482ba8e4239079
ms.openlocfilehash: acf7bacf6e95725024ff0a542a059349593d01a0
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Iestatīt detalizētās bankas darbību saskaņošanas importa procesu

[!include[banner](../includes/banner.md)]


Līdzeklis Detalizētā bankas darbību saskaņošana jums ļauj importēt elektroniskus bankas izrakstus un automātiski saskaņot tos ar bankas transakcijām programmatūrā Microsoft Dynamics 365 for Operations Šajā rakstā ir paskaidrots, kā iestatīt importēšanas funkcionalitāti saviem bankas izrakstiem. 

Bankas izraksta importēšanas iestatījumi ir dažādi, un tie ir atkarīgi no jūsu elektroniskā bankas izraksta formāta. Microsoft Dynamics 365 for Operations standarta komplektācijā atbalsta trīs bankas izraksta formātus: ISO20022, MT940 un BAI2.

## <a name="sample-files"></a>Parauga faili
Visiem trim formātiem jums ir nepieciešami faili, kas elektronisko bankas izrakstu no sākotnējā formāta pārveido formātā, kuru var izmantot Dynamics 365 for Operations. Nepieciešamie resursu faili ir atrodami Microsoft Visual Studio programmu pārlūka zarā **Resursi**. Kad faili ir atrasti, kopējiet tos uz vienu zināmu vietu, lai iestatīšanas procesa laikā tos varētu ērti augšupielādēt.

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
Tālāk ir sniegti detalizētās bankas darbību saskaņošanas importa faila tehnisko izkārtojumu definīciju paraugi un trīs saistītie bankas izrakstu parauga faili: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  

| Tehniskā izkārtojuma definīcija                             | Bankas izraksta parauga fails          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |

 

## <a name="set-up-the-import-of-iso20022-bank-statements"></a>Iestatīt ISO20022 bankas izrakstu importu
Vispirms ir jādefinē bankas izraksta formāta apstrādes grupa ISO20022 bankas izrakstiem, izmantojot datu elementa struktūru.

1.  Dodieties uz **Darbvietas** &gt; **Datu pārvaldība**.
2.  Noklikšķiniet uz **Importēt**.
3.  Ievadiet formāta nosaukumu, piemēram, **ISO20022**.
4.  Laukam **Avota datu formāts **iestatiet vērtību **XML elements**.
5.  Laukam **Elementa nosaukums** iestatiet vērtību **Bankas izraksti**.
6.  Lai augšupielādētu importa failus, noklikšķiniet uz **Augšupielādēt** un pēc tam pārlūkojiet, lai atlasītu iepriekš saglabāto failu **SampleBankCompositeEntity.xml**.
7.  Kad bankas izrakstu elements ir augšupielādēts un kartēšana ir pabeigta, noklikšķiniet uz darbības **Skatīt karti** šim elementam.
8.  Bankas izrakstu elements ir saliktais elements, kas sastāv no četriem atsevišķiem elementiem. Sarakstā atlasiet vienumu **BankStatementDocumentEntity** un pēc tam noklikšķiniet uz darbības **Skatīt karti**.
9.  Cilnē **Transformācijas** noklikšķiniet uz **Jauns**.
10. Kārtas numuram 1 noklikšķiniet uz **Augšupielādēt failu** un atlasiet iepriekš saglabāto failu** ISO20022XML-to-Reconciliation.xslt**. **Piezīme.** Dynamics 365 for Operations transformāciju faili ir veidoti standarta formātam. Tā kā bankas bieži vien novirzās no šī formāta, jums var būt jāatjaunina transformācijas fails, lai kartētu uz savu bankas izraksta formātu. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
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
3.  Cilnē **Saskaņošana** opciju **Detalizētā bankas darbību saskaņošana **iestatiet uz **Jā**.
4.  Lauku **Izraksta formāts **iestatiet uz iepriekš izveidoto formātu, piemēram, **ISO20022**.

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
11. Klikšķiniet **Jauns**.
12. Kārtas numuram 2 noklikšķiniet uz **Augšupielādēt failu** un atlasiet iepriekš saglabāto failu **MT940XML-to-Reconciliation.xslt**. **Piezīme.** Dynamics 365 for Operations transformāciju faili ir veidoti standarta formātam. Tā kā bankas bieži vien novirzās no šī formāta, jums var būt jāatjaunina transformācijas fails, lai kartētu uz savu bankas izraksta formātu. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
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
11. Klikšķiniet **Jauns**.
12. Kārtas numuram 2 noklikšķiniet uz **Augšupielādēt failu** un atlasiet iepriekš saglabāto failu **BAI2XML-to-Reconciliation.xslt**. **Piezīme.** Dynamics 365 for Operations transformāciju faili ir veidoti standarta formātam. Tā kā bankas bieži vien novirzās no šī formāta, jums var būt jāatjaunina transformācijas fails, lai kartētu uz savu bankas izraksta formātu. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
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
7.  Klikšķiniet **Augšupielādēt**.
8.  Noklikšķiniet uz **OK**.

Ja importēšana notika sekmīgi, jūs saņemat ziņojumu, ka jūsu izraksts tika importēts. Ja importēšana nebija sekmīga, darbvietas **Datu pārvaldība** sadaļā **Darbu vēsture** atrodiet šo darbu. Noklikšķiniet uz **Detalizēta informācija par izpildi** šim darbam, lai atvērtu lapu **Izpildes kopsavilkums**, un pēc tam noklikšķiniet uz **Skatīt izpildes žurnālu**, lai skatītu importēšanas kļūdas.




