---
title: ER konfigurāciju noformēšana pārskatu ģenerēšanai Word formātā
description: Tālāk sniegtajā darbību aprakstā ir paskaidrots, kā lietotājs, kam piešķirta loma Sistēmas administrators vai Elektronisko pārskatu izstrādātājs, var konfigurēt elektronisko pārskatu izveides formātus, lai ģenerētu pārskatus Microsoft Word failu formātā.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 327f03435ab55551953fd998dd89c831c76c4c26
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182604"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a>ER konfigurāciju noformēšana pārskatu ģenerēšanai Word formātā

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tālāk sniegtajā darbību aprakstā ir paskaidrots, kā lietotājs, kam piešķirta loma Sistēmas administrators vai Elektronisko pārskatu izstrādātājs, var konfigurēt elektronisko pārskatu izveides (Electronic reporting — ER) formātus, lai ģenerētu pārskatus Microsoft Word failu formātā. Šīs darbības var veikt uzņēmumā GBSI.

Lai veiktu šīs darbības, jums vispirms ir jāizpilda uzdevuma ceļvedī “Izveidot ER konfigurāciju pārskatu ģenerēšanai formātā OPENXML” norādītās darbības. Turklāt jums ir nepieciešams šim pašam pārskatam jau iepriekš lejupielādēt un lokāli saglabāt šādas veidnes:

- [Maksājumu pārskata veidne](https://go.microsoft.com/fwlink/?linkid=862266)
- [Maksājumu pārskata saistītā veidne](https://go.microsoft.com/fwlink/?linkid=862266)


Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Microsoft Dynamics 365 for Operations versijā 1611.


## <a name="select-the-existing-er-report-configuration"></a>Atlasiet esošo ER pārskatu konfigurāciju
1. **Navigācijas rūtī pārejiet uz sadaļu Moduļi > Organizācijas administrēšana > Darbvietas > Elektroniskie pārskati**. Pārliecinieties, vai konfigurācijas nodrošinātājs “Litware, Inc.“ ir atlasīts kā aktīvs.  
2. Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**. Mēs atkārtoti izmantosim esošo ER konfigurācija, kas sākotnēji tika veidota tā, lai pārskata izvadi ģenerētu formātā OPENXML.  
3. Koka struktūrā izvērsiet sadaļu “Maksājuma modelis”.
4. Koka struktūrā atlasiet “Maksājuma modelis\Parauga darblapas atskaite”.
5. Noklikšķiniet uz Veidotājs.

## <a name="replace-the-excel-template-with-the-word-template"></a>Excel veidni nomainīt pret Word veidni

Pašlaik Excel dokuments tiek izmantots kā veidne, lai ģenerētu izvadi formātā OPENXML. Mēs šo pārskata veidni importēsim formātā Word.

1. Noklikšķiniet uz **Pielikumi**. Esošo Excel veidni aizstājiet ar iepriekš lejupielādēto Word veidni SampleVendPaymDocReport.docx. Ņemiet vērā, ka šī veidne satur tikai dokumenta izkārtojumu, kuru vēlamies ģenerēt kā ER izvadi.  
2. Noklikšķiniet uz **Dzēst**.
3. Noklikšķiniet uz pogas **Jā**.
4. Klikšķiniet **Jauns**.
5. Noklikšķiniet uz **Fails**.
6. Noklikšķiniet uz **Pārlūkot**. Pārejiet uz iepriekš lejupielādēto veidni SampleVendPaymDocReport.docx un atlasiet to. Noklikšķiniet uz **Labi**. Atlasiet veidni, kuru lejupielādējāt iepriekšējā darbībā.  
7. Laukā **Veidne** ievadiet vai atlasiet vērtību.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Paplašināt Word veidni, pievienojot pielāgotu XML daļu
1. Noklikšķiniet uz **Saglabāt**. Papildus konfigurācijas izmaiņu uzglabāšanai darbība Saglabāt arī atjaunina pievienoto Word veidni. Izstrādātā formāta struktūra tiek pārnesta uz pievienoto Word dokumentu kā jauna pielāgota XML daļa ar nosaukumu “Pārskats”. Ņemiet vērā, ka pievienotajā Word veidnē ir ne tikai dokumenta izkārtojums, kādā vēlamies ģenerēt ER izvadi, bet tajā ir arī datu struktūra, ar ko ER izpildlaikā aizpildīs šo veidni.  
2. Noklikšķiniet uz **Pielikumi**.
    + Tagad pielāgotās XML daļas “Pārskats” elementi ir jāsaista ar Word dokumenta daļām.  
    + Ja pārzināt Word dokumentus, ko var noformēt kā veidlapas, kurās atrodas ar pielāgotām XML daļām saistītas satura vadīklas — atskaņojiet visas nākamā apakšuzdevuma darbības, lai izveidotu šādu dokumentu. Papildinformāciju skatiet rakstā [Veidlapu izveide, kuras lietotāji var aizpildīt un izdrukāt Word formātā](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US). Pretējā gadījumā izlaidiet visas nākamā apakšuzdevuma darbības.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Panākt, ka Word un pielāgotai XML daļai tiek veikti datu saistījumi

Atveriet šo dokumentu programmā Word un veiciet tālāk norādītās darbības:  
1. Atveriet Word cilni Izstrādātājs (pielāgojiet lenti, ja tā vēl nav iespējota).
2. Atlasiet XML kartēšanas rūti.
3. Uzmeklēšanā atlasiet pielāgotu XML daļu “Pārskats”.
4. Veiciet kartēšanu elementiem no atlasītās pielāgotās XML daļas un Word dokumenta satura vadīklām.  5. Saglabājiet atjaunināto Word dokumentu lokālajā diskā.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>Augšupielādēt Word veidni, kur ar satura vadīklām ir saistīta pielāgota XML daļa
1. Noklikšķiniet uz **Dzēst**.
2. Noklikšķiniet uz pogas **Jā**. Pievienojiet jaunu veidni. Ja esat izpildījis iepriekšējā apakšuzdevumā aprakstītās darbības, atlasiet Word dokumentu, kuru sagatavojāt un lokāli saglabājāt. Pretējā gadījumā atlasiet iepriekš lejupielādēto SampleVendPaymDocReportBounded.docx MS Word veidni.  
3. Klikšķiniet **Jauns**.
4. Noklikšķiniet uz **Fails**.
5. Noklikšķiniet uz **Pārlūkot**. Pārejiet uz iepriekš lejupielādēto veidni SampleVendPaymDocReportBounded.docx un atlasiet to. Noklikšķiniet uz **Labi**.
6. Laukā **Veidne** atlasiet dokumentu, ko lejupielādējāt, veicot iepriekšējo darbību.
7. Noklikšķiniet uz **Saglabāt**.
8. Aizvērt lapu.

## <a name="execute-the-format-to-create-word-output"></a>Izpildīt formātu, lai izveidotu Word izvadi
1. **Darbību rūtī** noklikšķiniet **Konfigurācijas**.
2. Noklikšķiniet uz **Lietotāja parametri**.
3. Atlasiet Jā laukā **Palaist iestatījumus**.
4. Noklikšķiniet uz **Labi**.
5. Noklikšķiniet uz **Rediģēt**.
6. Atlasiet Jā laukā **Palaist melnrakstu**.
7. Noklikšķiniet uz **Saglabāt**.
8. Aizvērt lapu.
9. Aizvērt lapu.
10. **Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Kreditori > Maksājumi > Maksājumu žurnāls**.
11. Noklikšķiniet uz **Rindas**.
12. Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.
13. Noklikšķiniet uz **Maksājuma statuss**.
14. Noklikšķiniet uz **Nav**.
15. Noklikšķiniet uz **Ģenerēt maksājumus**.
16. Noklikšķiniet uz **Labi**.
17. Noklikšķiniet uz **Labi**. Analizējiet ģenerēto izvadi. Ņemiet vērā, ka izveidotā izvade tiek rādīta formātā Word, un tā ietver detalizētu informāciju par apstrādātajiem maksājumiem.  

