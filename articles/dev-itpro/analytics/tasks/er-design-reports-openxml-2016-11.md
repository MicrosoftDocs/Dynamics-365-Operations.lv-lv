--- 
title: "Noformēt konfigurāciju pārskatu ģenerēšanai OpenXML formātā elektronisko pārskatu veidošanai (ER)"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var izveidot jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurāciju, kas satur veidni elektronisko dokumentu ģenerēšanai OPENXML formātā."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 04def14ddf9b079005bf11acbcaf64b21aa80fdb
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a>Noformēt konfigurāciju pārskatu ģenerēšanai OpenXML formātā elektronisko pārskatu veidošanai (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var izveidot jaunu elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurāciju, kas satur veidni elektronisko dokumentu ģenerēšanai OPENXML formātā. Šī konfigurācija tiks izmantota kreditoru maksājumu apstrādei.



Šajā piemērā tiek izveidota parauga uzņēmuma Litware, Inc. konfigurācija. Šīs darbības var veikt jebkurā GBSI uzņēmumā.



Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības. Jums ir nepieciešams arī Excel fails, kas tiks importēts, veidojot veidni. Šim failam var piekļūt no vietnes: https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx


## <a name="upload-the-payments-data-model-configuration"></a>Augšupielādēt maksājumu datu modeļa konfigurāciju
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
2. Sarakstā atzīmējiet atlasīto rindu.
    * Atlasiet konfigurācijas nodrošinātāju parauga uzņēmumam "Litware, Inc." Ja jūs neredzat šo konfigurācijas nodrošinātāju, vispirms jāveic darbības, kas aprakstītas procedūrā "Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu".  
3. Noklikšķiniet uz Iestatīt aktīvu.
4. Noklikšķiniet uz Repozitoriji.
    * Atlasiet repozitoriju tipam Operācijas resursi, ja tāds ir pieejams. Ja tas ir pieejams, izlaidiet nākamās darbības par jauna repozitorija izveidošanu.  
5. Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.
6. Laukā Konfigurācijas repozitorija tips ievadiet Operācijas resursi.
7. Noklikšķiniet uz Izveidot repozitoriju.
8. Noklikšķiniet uz OK.
9. Noklikšķiniet uz Atvērt.
10. Koka struktūrā atlasiet “Maksājuma modelis”.
11. Noklikšķiniet uz Importēt.
    * Importējiet šo datu modeli. Tas tiks izmantots kā datu avots jaunā formāta konfigurācijā. Izlaidiet šo darbību, ja šī konfigurācija jau ir importēta.  
12. Noklikšķiniet uz Jā.
13. Aizvērt lapu.
14. Aizvērt lapu.

## <a name="create-a-new-format-configuration"></a>Jaunas formāta konfigurācijas izveide
1. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
2. Koka struktūrā atlasiet “Maksājuma modelis”.
3. Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.
4. Laukā Jauns ievadiet "Formāts pamatojoties uz datu modeli PaymentModel".
    * Izveidojiet formātu, kas ir balstīts uz datu modeli PaymentModel.  
5. Laukā Nosaukums ierakstiet “Parauga darblapas atskaite”.
    * Parauga darblapas atskaite  
6. Laukā Apraksts ierakstiet “Parauga darblapas atskaite kreditoru maksājumiem”.
    * Parauga darblapas atskaite kreditoru maksājumiem.  
7. Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.
    * Atlasiet definīciju “CustomerCreditTransferInitiation”.  
8. Klikšķiniet Izveidot konfigurāciju.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Noformēt jaunu dokumentu OPENXML darblapas formātā
1. Koka struktūrā atlasiet “Maksājuma modelis\Parauga darblapas atskaite”.
2. Noklikšķiniet uz Veidotājs.
3. Darbību rūtī noklikšķiniet uz Importēt.
4. Noklikšķiniet uz Importēt no Excel.
5. Noklikšķiniet uz Pielikumi.
    * Pievienojiet esošo Excel dokumentu kā veidni.  
6. Noklikšķiniet uz Jauns.
7. Noklikšķiniet uz Fails.
    * Norādiet uz esošo Excel failu.  
8. Aizvērt lapu.
9. Ievadiet vai atlasiet kādu vērtību laukā Veidne.
    * Atlasiet pievienoto Excel failu, ko izmantot kā veidni.  
10. Noklikšķiniet uz OK.
    * Ņemiet vērā, ka ER formātā komponenti tika izveidoti, izstrādājot formātu un pamatojoties uz atsauces MS Excel dokumenta (nosauktie diapazoni) struktūru.  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Izveidot jaunu datu avotu, lai aprēķinātu kopsummas pēc valūtu kodiem
1. Noklikšķiniet uz cilnes Kartēšana.
2. Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.
3. Koka struktūrā atlasiet “Funkcijas\Grupēt pēc”.
4. Laukā Nosaukums ierakstiet “PaymentByCurrency”.
    * PaymentByCurrency  
5. Noklikšķiniet uz Rediģēt grupu pēc.
6. Koka struktūrā izvērsiet elementu “modelis”.
7. Kokā atlasiet “modelis\Maksājumi”.
8. Noklikšķiniet uz Pievienot lauku pie.
9. Noklikšķiniet uz Ko grupēt.
10. Kokā izvērsiet sadaļu “modelis\Maksājumi”.
11. Koka struktūrā atlasiet elementu “modelis\Maksājumi\Valūta”.
12. Noklikšķiniet uz Pievienot lauku pie.
13. Noklikšķiniet uz Grupētie lauki.
14. Koka struktūrā atlasiet elementu “modelis\Maksājumi\Instruētā summa(InstructedAmount)”.
15. Noklikšķiniet uz Pievienot lauku pie.
16. Noklikšķiniet uz Apkopojuma lauki.
17. Atlasiet opciju laukā Metode.
    * Atlasiet SUM apkopošanas funkciju.  
18. Laukā Nosaukums ierakstiet “TotalInstructuredAmount”.
    * TotalInstructuredAmount  
19. Noklikšķiniet uz Saglabāt.
20. Aizvērt lapu.
21. Noklikšķiniet uz OK.

## <a name="map-format-components-to-data-sources"></a>Kartēt formāta komponentus uz datu avotiem
1. Koka struktūrā izvērsiet elementu “modelis”.
2. Kokā izvērsiet sadaļu “modelis\Maksājumi”.
3. Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Iniciējošā puse(InitiatingParty)”.
4. Koka struktūrā atlasiet elementu “modelis\Maksājumi\Iniciējošā puse(InitiatingParty)\Nosaukums”.
5. Koka struktūrā izvērsiet zaru “Excel\ReportHeader”.
6. Koka struktūrā atlasiet zaru “Excel\ReportHeader\CompanyName”.
7. Noklikšķiniet uz Saistīt.
8. Kokā izvērsiet sadaļu “modelis\Maksājumi\Kreditors”.
9. Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditors\Identifikācija“.
10. Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditors\Identifikācija\Avota ID(SourceID)“.
11. Koka struktūrā izvērsiet zaru “Excel\PaymLines”.
12. Koka struktūrā atlasiet zaru “Excel\PaymLines\VendAccountName”.
13. Noklikšķiniet uz Saistīt.
14. Kokā atlasiet “modelis\Maksājumi\Kreditors\Nosaukums”.
15. Koka struktūrā atlasiet zaru “Excel\PaymLines\VendName”.
16. Noklikšķiniet uz Saistīt.
17. Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)“.
18. Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)\Nosaukums“.
19. Koka struktūrā atlasiet zaru “Excel\PaymLines\Banka”.
20. Noklikšķiniet uz Saistīt.
21. Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)\Maršrutēšanas numurs(RoutingNumber)”.
22. Koka struktūrā atlasiet zaru “Excel\PaymLines\RoutingNumber”.
23. Noklikšķiniet uz Saistīt.
24. Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)“.
25. Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)\Identifikācija“.
26. Koka struktūrā atlasiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)\Identifikācija\Numurs“.
27. Koka struktūrā atlasiet zaru “Excel\PaymLines\AccountNumber”.
28. Noklikšķiniet uz Saistīt.
29. Koka struktūrā atlasiet elementu “modelis\Maksājumi\Instruētā summa(InstructedAmount)”.
30. Koka struktūrā atlasiet zaru “Excel\PaymLines\Debit”.
31. Noklikšķiniet uz Saistīt.
32. Kokā izvērsiet sadaļu “modelis\Maksājumi\Kreditors”.
33. Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora konts(CreditorAccount)“.
34. Koka struktūrā izvērsiet elementu “modelis\Maksājumi\Kreditora aģents(CreditorAgent)“.
35. Koka struktūrā atlasiet elementu “modelis\Maksājumi\Valūta”.
36. Koka struktūrā atlasiet zaru “Excel\PaymLines\Valūta”.
37. Noklikšķiniet uz Saistīt.
38. Koka struktūrā izvērsiet elementu “PaymentByCurrency”.
39. Koka struktūrā izvērsiet elementu “PaymentByCurrency\grupēts”.
40. Koka struktūrā atlasiet elementu “PaymentByCurrency\grupēts\Valūta”.
41. Koka struktūrā izvērsiet zaru “Excel\SummaryLines”.
42. Koka struktūrā atlasiet zaru “Excel\SummaryLines\SummaryCurrency”.
43. Noklikšķiniet uz Saistīt.
44. Koka struktūrā izvērsiet elementu “PaymentByCurrency\apkopots”.
45. Koka struktūrā atlasiet elementu “PaymentByCurrency\apkopots\TotalInstructuredAmount”.
46. Koka struktūrā atlasiet zaru “Excel\SummaryLines\SummaryAmount”.
47. Noklikšķiniet uz Saistīt.
48. Koka struktūrā atlasiet elementu “PaymentByCurrency”.
49. Koka struktūrā atlasiet zaru “Excel\SummaryLines”.
50. Noklikšķiniet uz Saistīt.
51. Kokā atlasiet “modelis\Maksājumi”.
52. Koka struktūrā atlasiet zaru “Excel\PaymLines”.
53. Noklikšķiniet uz Saistīt.
54. Noklikšķiniet uz Saglabāt.
55. Aizvērt lapu.

## <a name="use-the-created-configuration-for-payments-processing"></a>Izmantojiet izveidoto konfigurāciju maksājumu apstrādei
1. Noklikšķiniet uz Mainīt statusu.
2. Noklikšķiniet uz Pabeigt.
3. Noklikšķiniet uz OK.
4. Aizvērt lapu.
5. Aizvērt lapu.
6. Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Maksāšanas metodes.
7. Izmantojiet līdzekli Ātrais filtrs, lai filtrētu pēc lauka Maksāšanas metode ar vērtību “Elektroniski”.
    * Elektroniski  
8. Noklikšķiniet uz Rediģēt.
9. Izvērsiet sadaļu Failu formāti.
10. Laukā Vispārīga elektronisko pārskatu veidošana atlasiet Jā.
11. Ievadiet vai atlasiet vērtību laukā Eksporta formāta konfigurācija.
    * Atlasiet konfigurāciju “Parauga darblapas atskaite”.  
12. Noklikšķiniet uz Saglabāt.
13. Aizvērt lapu.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Izmantot izveidoto konfigurāciju maksājumu žurnālu apstrādes testēšanai
1. Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.
2. Noklikšķiniet uz Jauns.
    * Izveidojiet jaunu maksājumu žurnālu.  
3. Laukā Nosaukums ierakstiet VendPay.
    * VendPay  
4. Noklikšķiniet uz Rindas.
5. Laukā Konts norādiet vērtības “GB_SI_000001”.
    * GB_SI_000001  
6. Vienumam Debets norādiet vērtību “1000”.
7. Noklikšķiniet uz Jauns.
8. Laukā Konts norādiet vērtības “GB_SI_000005”.
    * GB_SI_000005  
9. Vienumam Debets norādiet vērtību “2000”.
10. Laukā Valūta ierakstiet vērtību “EUR”.
    * EUR  
11. Laukā Korespondējošais konts norādiet vērtības “GBSI OPER”.
    * GBSI OPER  
12. Laukā Maksāšanas metode ierakstiet “Elektroniski”.
    * Elektroniski  
13. Noklikšķiniet uz Saglabāt.
14. Noklikšķiniet uz Ģenerēt maksājumus.
15. Laukā Maksāšanas metode ierakstiet “Elektroniski”.
    * Elektroniski  
16. Laukā Faila nosaukums ierakstiet “Maksājumi”.
    * Piemēram, tips Maksājumi.  
17. Laukā Bankas konts atlasiet “GBSI OPER”.
    * GBSI OPER  
18. Noklikšķiniet uz OK.
19. Noklikšķiniet uz OK.
    * Pārskatiet izveidoto darblapu, tostarp informāciju par maksājuma rindām, kā arī kopsummas katram valūtas kodam, kas ir izmantots šajā maksājuma ziņojumā.  


