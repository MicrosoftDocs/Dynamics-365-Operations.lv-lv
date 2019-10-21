---
title: ER Izveidot konfigurāciju pārskatu ģenerēšanai formātā OPENXML (2016. gada maijs)
description: Šajā tēmā ir paskaidrots, kā lietotājs Sistēmas administratora vai Elektronisko pārskatu izstrādātāja lomā var izveidot Elektronisko pārskatu (EK) konfigurāciju, kas ietver veidni elektronisko dokumentu ģenerēšanai OPENXML formātā.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1229c89f43f9ded955dadf2f4d87825c9ab4e71
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182581"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>ER Izveidot konfigurāciju pārskatu ģenerēšanai formātā OPENXML (2016. gada maijs)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā tēmā ir paskaidrots, kā lietotājs Sistēmas administratora vai Elektronisko pārskatu izstrādātāja lomā var izveidot Elektronisko pārskatu (EK) konfigurāciju, kas ietver veidni elektronisko dokumentu ģenerēšanai OPENXML formātā. Šī konfigurācija tiks izmantota kreditoru maksājumu apstrādei.

Šajā piemērā tiek izveidota parauga uzņēmuma Litware, Inc. konfigurācija. Šīs darbības var veikt jebkurā GBSI uzņēmumā.

Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības. Jums ir nepieciešams arī Excel fails, kas tiks importēts, veidojot veidni. Lai piekļūtu šim failam, izmantojiet opciju [Maksājumu pārskata veidne](https://go.microsoft.com/fwlink/?linkid=862266).


## <a name="upload-the-payments-data-model-configuration"></a>Augšupielādēt maksājumu datu modeļa konfigurāciju
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Organizācijas administrēšana > Darbvietas > Elektroniskie pārskati**.
2. Sarakstā atzīmējiet konfigurācijas sniedzēju parauguzņēmumam “Litware, Inc.” Ja neredzat šo konfigurācijas sniedzēju, vispirms veiciet šajā rakstā minētās darbības [Izveidojiet konfigurācijas sniedzēju un atzīmējiet to kā aktīvu](er-configuration-provider-mark-it-active-2016-11.md).
3. Atlasiet **Iestatīt kā aktīvu**.
4. Atlasiet **Repozitoriji**. Atlasiet repozitoriju tipam Operācijas resursi, ja tāds ir pieejams. Ja tas ir pieejams, izlaidiet nākamās darbības par jauna repozitorija izveidošanu.  
5. Atlasiet **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.
6. Laukā **Konfigurācijas repozitorija tips** ievadiet `Operations resourcesdd`.
7. Atlasiet **Izveidot repozitoriju**.
8. Atlasiet **Labi**.
9. Atlasiet **Atvērt**.
10. Koka struktūrā atlasiet **Maksājuma modelis**.
11. Atlasiet **Importēt**. Importējiet šo datu modeli. Tas tiks izmantots kā datu avots jaunā formāta konfigurācijā. Izlaidiet šo darbību, ja šī konfigurācija jau ir importēta.  
12. Atlasiet **Jā**.
13. Aizveriet lapas, līdz atgriezīsieties uz Elektronisko pārskatu lapu.

## <a name="create-a-new-format-configuration"></a>Jaunas formāta konfigurācijas izveide
1. Atlasiet **Pārskatu konfigurācijas**.
2. Koka struktūrā atlasiet **Maksājuma modelis**.
3. Atlasiet **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.
4. Laukā **Jauns** ievadiet `Format based on data model PaymentModel`. Izveidojiet formātu, kas ir balstīts uz datu modeli PaymentModel.
5. Laukā **Nosaukums** ievadiet `Sample worksheet report`. Parauga darblapas atskaite  
6. Laukā **Apraksts** ievadiet `Sample worksheet report for vendors’ payments`. Parauga darblapas atskaite kreditoru maksājumiem.  
7. Ievadiet vai atlasiet kādu vērtību laukā **Datu modeļa definīcija**. Atlasiet definīciju **CustomerCreditTransferInitiation**.  
8. Atlasiet **Izveidot konfigurāciju**.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Noformēt jaunu dokumentu OPENXML darblapas formātā
1. Koka struktūrā atlasiet **Maksājuma modelis\Parauga darblapas atskaite**.
2. Atlasiet **Noformētājs**.
3. Darbību rūtī atlasiet **Importēt**.
4. Atlasiet **Importēt no Excel**.
5. Atlasiet **Pielikumi**. Pievienojiet esošo Excel dokumentu kā veidni.  
6. Atlasiet **Jauns**.
7. Atlasiet **Fails**. Norādiet uz esošo Excel failu.  
8. Aizvērt lapu.
9. Laukā **Veidne** ievadiet vai atlasiet vērtību. Atlasiet pievienoto Excel failu, ko izmantot kā veidni.  
10. Atlasiet **Labi**. Ņemiet vērā, ka ER formātā komponenti tika izveidoti, izstrādājot formātu un pamatojoties uz atsauces MS Excel dokumenta (nosauktie diapazoni) struktūru.  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Izveidot jaunu datu avotu, lai aprēķinātu kopsummas pēc valūtu kodiem
1. Atlasiet cilni **Kartēšana**.
2. Atlasiet **Pievienot sakni**, lai atvērtu nolaižamo dialoglodziņu.
3. Koka struktūrā atlasiet **Funkcijas\Grupēt pēc**.
4. Laukā **Nosaukums** ievadiet `PaymentByCurrency`.
5. Atlasīt **Rediģēt grupu pēc**.
6. Kokā izvērtiet **modelis**, pēc tam atlasiet **modelis\Maksājumi**.
7. Atlasiet **Pievienot lauku**.
8. Atlasiet **Ko grupēt**.
9. Kokā izvērtiet **modelis\Maksājumi**, pēc tam atlasiet **modelis\Maksājumi\Valūta**.
10. Atlasiet **Pievienot lauku**.
11. Atlasiet **Grupētie lauki**.
12. Koka struktūrā atlasiet **modelis\Maksājumi\Instruētā summa(InstructedAmount)**.
13. Atlasiet **Pievienot lauku**, pēc tam atlasiet **Apkopojuma lauks**.
14. Atlasiet opciju laukā **Metode**. Atlasiet funkciju **SUM apkopojums**.  
15. Laukā **Nosaukums** ievadiet `TotalInstructuredAmount`.
16. Atlasiet **Saglabāt**.
17. Aizvērt lapu.
18. Atlasiet **Labi**.

## <a name="map-format-components-to-data-sources"></a>Kartēt formāta komponentus uz datu avotiem
1. Koka struktūrā atlasiet **modelis\Maksājumi\Iniciējošā puse(InitiatingParty)\Nosaukums** un **Excel\ReportHeader\CompanyName**.
2. Atlasiet **Saistīt**.
3. Koka struktūrā atlasiet **modelis\Maksājumi\Kreditors\Identifikācija\Avota ID(SourceID)** un **Excel\PaymLines\VendAccountName**.
4. Atlasiet **Saistīt**.
5. Koka struktūrā atlasiet **modelis\Maksājumi\Kreditors\Nosaukums** un **Excel\PaymLines\VendName**.
6. Atlasiet **Saistīt**.
7. Koka struktūrā atlasiet **modelis\Maksājumi\Kreditora aģents(CreditorAgent)\Nosaukums** un **Excel\PaymLines\Banka**.
8. Atlasiet **Saistīt**.
9. Koka struktūrā atlasiet **modelis\Maksājumi\Kreditora aģents(CreditorAgent)\Maršrutēšanas numurs(RoutingNumber)** un **Excel\PaymLines\RoutingNumber**.
10. Atlasiet **Saistīt**.
11. Koka struktūrā atlasiet **modelis\Maksājumi\Kreditora konts(CreditorAccount)\Identifikācija\Numurs** un **Excel\PaymLines\AccountNumber**.
12. Atlasiet **Saistīt**.
13. Koka struktūrā atlasiet **modelis\Maksājumi\Instruētā summa(InstructedAmount)** un **Excel\PaymLines\Debets**.
14. Atlasiet **Saistīt**.
15. Koka struktūrā atlasiet **modelis\Maksājumi\Valūta** un **Excel\PaymLines\Valūta**.
16. Atlasiet **Saistīt**.
17. Koka struktūrā atlasiet **PaymentByCurrency\grupēts\Valūta** un **Excel\SummaryLines\SummaryCurrency**.
18. Atlasiet **Saistīt**.
19. Koka struktūrā atlasiet **PaymentByCurrency\apkopotais\TotalInstructuredAmount** un **Excel\SummaryLines\SummaryAmount**.
20. Atlasiet **Saistīt**.
21. Koka struktūrā atlasiet **PaymentByCurrency** un **Excel\SummaryLines**.
22. Atlasiet **Saistīt**.
23. Koka struktūrā atlasiet **modelis\Maksājumi** un **Excel\PaymLines**.
24. Atlasiet **Saistīt**.
25. Atlasiet **Saglabāt**, pēc tam aizveriet lapu.

## <a name="use-the-created-configuration-for-payments-processing"></a>Izmantojiet izveidoto konfigurāciju maksājumu apstrādei
1. Atlasiet **Mainīt statusu**.
2. Atlasiet **Pabeigt**.
3. Atlasiet **Labi**.
4. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Kreditori > Maksājuma iestatīšana > Maksāšanas veidi**.
5. Lietojiet Ātro filtru, lai laukā **Maksāšanas veids** filtrētu, izmantojot vērtību **Elektronisks**.
6. Atlasiet **Rediģēt**.
7. Izvērtiet sadaļu **Faila formāti**.
8. Atlasiet **Jā** laukā **Vispārīgie elektroniskie pārskati**.
9. Laukā **Eksporta formāta konfigurācija** ievadiet vai atlasiet vērtību. Atlasiet konfigurāciju **Parauga darblapas pārskats**.  
10. Atlasiet **Saglabāt**.
11. Aizvērt lapu.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Izmantot izveidoto konfigurāciju maksājumu žurnālu apstrādes testēšanai
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Kreditori > Maksājumi > Maksājumu žurnāls**.
2. Atlasiet **Jauns**, lai izveidotu jaunu maksājuma žurnālu.
3. Laukā **Nosaukums** ievadiet **VendPay**.
4. Atlasiet **Rindas**.
5. Laukā **Konts** norādiet vērtības `GB_SI_000001`.
6. Iestatiet **Debets** uz `1000`.
7. Atlasiet **Jauns**.
8. Laukā **Konts** norādiet vērtības `GB_SI_000005`.
9. Iestatiet **Debets** uz `2000`.
10. Laukā **Valūta** ievadiet `EUR`.
11. Laukā **Korespondējošais konts** norādiet vērtības `GBSI OPER`.
12. Laukā **Maksāšanas veids** ievadiet `Electronic`.
13. Atlasiet **Saglabāt**.
14. Atlasiet **Ģenerēt maksājumus**.
15. Laukā **Maksāšanas veids** ievadiet `Electronic`.
16. Laukā **Faila nosaukums** ievadiet `Payments`.
17. Laukā **Bankas konts** ievadiet `GBSI OPER`.
18. Atlasiet **Labi**, pēc tam vēlreiz atlasiet **Labi**. Pārskatiet izveidoto darblapu, tostarp informāciju par maksājuma rindām, kā arī kopsummas katram valūtas kodam, kas ir izmantots šajā maksājuma ziņojumā.  

