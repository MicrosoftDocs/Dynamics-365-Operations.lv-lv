--- 
title: "Modificēt formātu, atkārtoti pielietojot Microsoft Excel veidni elektronisko pārskatu veidošanai (ER)"
description: "Lai veiktu šīs procedūras darbības, jums vispirms ir jāizpilda procedūra “ER Noformēt konfigurāciju pārskatu ģenerēšanai formātā OPENXML”."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: b49cfe39732a450e4723419c50d8bcc3d64b7ec9
ms.openlocfilehash: 2f35727376812b0de428ce929ebe0d33bc497984
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="modify-a-format-by-reapplying-a-microsoft-excel-template-for-electronic-reporting-er"></a>Modificēt formātu, atkārtoti pielietojot Microsoft Excel veidni elektronisko pārskatu veidošanai (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Lai veiktu šīs procedūras darbības, jums vispirms ir jāizpilda procedūra “ER Noformēt konfigurāciju pārskatu ģenerēšanai formātā OPENXML”.

Šajā procedūrā paskaidrots, kā modificēt elektroniskā pārskata (ER) formāta konfigurāciju, atkārtoti lietojot Microsoft Excel veidni, kura ir modificēta. Šajā procedūrā importēsiet modificētu Excel veidni ER formāta konfigurācijās, kuras ir izveidotas parauga uzņēmumam “Litware, Inc.”, un pēc tam ģenerēsit elektroniskos dokumentus. Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. Šīs darbības var veikt, izmantojot GBSI datu kopu. Pirms darba sākšanas lejupielādējiet un saglabājiet failu SampleVendPaymWsReport2.xlsx, kurš ir norādīts palīdzības tēmā “Elektronisko pārskatu veidošanas formāta mainīšana, atkārtoti pielietojot Microsoft Excel veidni” (modify-electronic-reporting-format-reapply-excel-template/).

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
    * Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un ir atzīmēts kā aktīvs. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.  

## <a name="select-the-er-format"></a>Atlasīt ER formātu
1. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
2. Kokā struktūra izvērsiet sadaļu “Maksājuma modelis”.
3. Koka struktūrā atlasiet “Maksājuma modelis\Parauga darblapas atskaite”.
4. Noklikšķiniet uz Pielikumi.
    * Ņemiet vērā, ka Excel fails SampleVendPaymWsReport.xlsx pašlaik tiek izmantots kā veidne maksājumu žurnālu apstrādei.   
5. Noklikšķiniet uz Atvērt.
    * Noklikšķiniet uz Atvērt, lai izpētītu Excel veidnes izkārtojumu.  
    * Pārskatiet veidni. Ņemiet vērā, ka tajā pašlaik ietverta šāda informācija par katru maksājuma rindu: kreditora konta numurs, kreditora nosaukums, banka, reģistrācijas numurs, konta numurs, debets, kredīts un valūta. Šajā piemērā mēs vēlamies paplašināt šo sarakstu, pievienojot detalizētu informāciju par maksājuma datumu.   
6. Aizvērt lapu.

## <a name="reapply-a-new-excel-template-to-er-format"></a>Atkārtoti lietot jaunu Excel veidni ER formātam
1. Noklikšķiniet uz Veidotājs.
    * Atveriet atlasītā ER formāta melnraksta versiju rediģēšanai.  
2. Darbību rūtī noklikšķiniet uz Importēt.
3. Noklikšķiniet uz Atjaunināt no Excel.
    * Noklikšķiniet uz Atjaunināt veidni un pēc tam atlasiet failu SampleVendPaymWsReport2.xlsx.  
    * Noklikšķiniet uz Atjaunināt veidni un pārlūkojiet līdz iepriekš lejupielādētajam failam SampleVendPaymWsReport2.xlsx.  
4. Noklikšķiniet uz OK.
    * Tiek lietota veidne SampleVendPaymWsReport2.xlsx. ER formāta struktūra ir sinhronizēta ar tās veidnes saturu, kuras elementi tiek pievienoti ER formātam. Visi esošie ER formāta elementi, kas nav iekļauti veidnē, tiek noņemti no formāta definīcijas.  
5. Kokā atlasiet “Excel”.
    * Ņemiet vērā, ka lauks Veidne tagad satur atsauci uz jauno veidni.   
6. Noklikšķiniet uz Pielikumi.
7. Noklikšķiniet uz Atvērt.
    * Noklikšķiniet uz Atvērt, lai izpētītu modificētās Excel veidnes izkārtojumu.  
    * Pārskatiet veidni. Ņemiet vērā, ka tas tagad satur maksājuma datuma rindu.   
8. Aizvērt lapu.
9. Kokā izvērsiet “Excel”.
10. Koka struktūrā izvērsiet zaru “Excel\PaymLines”.
11. Kokā atlasiet 'Excel\PaymLines\PaymDate'.
    * Ņemiet vērā, ka ER formāts tagad satur vienu papildu vienumu. Excel veidnei ir pievienota šūna PaymDate.  
12. Noklikšķiniet uz cilnes Kartēšana.
13. Koka struktūrā izvērsiet elementu “modelis”.
14. Kokā izvērsiet sadaļu “modelis\Maksājumi”.
15. Kokā atlasiet "modelis\Maksājumi\Transakcijas datums(TransactionDate)".
16. Noklikšķiniet uz Saistīt.
    * Norādiet, kādi dati jāpievieno jaunajai šūnai izpildlaikā.  
17. Noklikšķiniet uz Saglabāt.
18. Aizvērt lapu.

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a>Iespējot ER formāta modificēto melnraksta versiju lietošanai maksājumu žurnāla apstrādei
1. Darbību rūtī noklikšķiniet uz Konfigurācijas.
2. Noklikšķiniet uz Lietotāja parametri.
3. Laukā Palaist iestatījumus atlasiet Jā.
4. Noklikšķiniet uz OK.
5. Noklikšķiniet uz Rediģēt.
6. Laukā Palaist melnrakstu atlasiet Jā.

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a>Izmantot ER formāta modificēto melnraksta versiju lietošanai maksājumu žurnāla apstrādei
    * Pārskatiet izveidoto darblapu, ieskaitot jauno maksājuma informācijas rindu — maksājuma datumu.  

