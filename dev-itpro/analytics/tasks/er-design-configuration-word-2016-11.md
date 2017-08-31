--- 
title: "Noformēt konfigurāciju pārskatu ģenerēšanai Microsoft Word formātā elektronisko pārskatu veidošanai (ER)"
description: "Nākamajās darbībās ir paskaidrots, kā lietotājs, kam piešķirta loma Sistēmas administrators vai Elektronisko pārskatu izstrādātājs, var konfigurēt elektronisko pārskatu veidošanas (Electronic reporting — ER) formātus, lai pārskatus ģenerētu kā Microsoft Word failus."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5adf1d6e6314ac7ea4084cfb3fcde8b83168c7ae
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="design-a-configuration-for-generating-reports-in-microsoft-word-format-for-electronic-reporting-er"></a>Noformēt konfigurāciju pārskatu ģenerēšanai Microsoft Word formātā elektronisko pārskatu veidošanai (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Nākamajās darbībās ir paskaidrots, kā lietotājs, kam piešķirta loma Sistēmas administrators vai Elektronisko pārskatu izstrādātājs, var konfigurēt elektronisko pārskatu veidošanas (Electronic reporting — ER) formātus, lai pārskatus ģenerētu kā Microsoft Word failus. Šīs darbības var veikt uzņēmumā GBSI.

Lai veiktu šīs darbības, jums vispirms ir jāizpilda uzdevuma ceļvedī “Izveidot ER konfigurāciju pārskatu ģenerēšanai formātā OPENXML” norādītās darbības. Turklāt jums ir nepieciešams šim pašam pārskatam jau iepriekš lejupielādēt un lokāli saglabāt šādas veidnes:

http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReport.docx

http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReportBounded.docx

Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Microsoft Dynamics 365 for Operations versijā 1611.


## <a name="select-the-existing-er-report-configuration"></a>Atlasiet esošo ER pārskatu konfigurāciju
1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
    * Pārliecinieties, vai konfigurācijas nodrošinātājs “Litware, Inc.“ ir atlasīts kā aktīvs.  
2. Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.
    * Mēs atkārtoti izmantosim esošo ER konfigurācija, kas sākotnēji tika veidota tā, lai pārskata izvadi ģenerētu formātā OPENXML.  
3. Kokā struktūra izvērsiet sadaļu “Maksājuma modelis”.
4. Koka struktūrā atlasiet “Maksājuma modelis\Parauga darblapas atskaite”.
5. Noklikšķiniet uz Veidotājs.

## <a name="replace-the-excel-template-with-the-word-template"></a>Excel veidni nomainīt pret Word veidni
    * Pašlaik Excel dokuments tiek izmantots kā veidne, lai ģenerētu izvadi formātā OPENXML. Mēs šo pārskata veidni importēsim formātā Word.  
1. Noklikšķiniet uz Pielikumi.
    * Esošo Excel veidni aizstājiet ar iepriekš lejupielādēto Word veidni SampleVendPaymDocReport.docx. Ņemiet vērā, ka šī veidne satur tikai dokumenta izkārtojumu, kuru vēlamies ģenerēt kā ER izvadi.  
2. Noklikšķiniet uz Dzēst.
3. Noklikšķiniet uz Jā.
4. Noklikšķiniet uz Jauns.
5. Noklikšķiniet uz Fails.
6. Noklikšķiniet uz Pārlūkot. Pārejiet uz iepriekš lejupielādēto veidni SampleVendPaymDocReport.docx un atlasiet to. Noklikšķiniet uz OK.
    * Atlasiet veidni, kuru lejupielādējāt iepriekšējā darbībā.  
7. Ievadiet vai atlasiet kādu vērtību laukā Veidne.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Paplašināt Word veidni, pievienojot pielāgotu XML daļu
1. Noklikšķiniet uz Saglabāt.
    * Papildus konfigurācijas izmaiņu uzglabāšanai darbība Saglabāt arī atjaunina pievienoto Word veidni. Izstrādātā formāta struktūra tiek pārnesta uz pievienoto Word dokumentu kā jauna pielāgota XML daļa ar nosaukumu “Pārskats”. Ņemiet vērā, ka pievienotajā Word veidnē ir ne tikai dokumenta izkārtojums, kādā vēlamies ģenerēt ER izvadi, bet tajā ir arī datu struktūra, ar ko ER izpildlaikā aizpildīs šo veidni.  
2. Noklikšķiniet uz Pielikumi.
    * Tagad pielāgotās XML daļas “Pārskats” elementi ir jāsaista ar Word dokumenta daļām.  
    * Ja pārzināt Word dokumentus, ko var noformēt kā veidlapas, kurās atrodas ar pielāgotām XML daļām saistītas satura vadīklas — atskaņojiet visas nākamā apakšuzdevuma darbības, lai izveidotu šādu dokumentu. Papildinformāciju skatiet šajā saitē: https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US. Pretējā gadījumā izlaidiet visas nākamā apakšuzdevuma darbības.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Panākt, ka Word un pielāgotai XML daļai tiek veikti datu saistījumi
    * Atveriet šo dokumentu programmā Word un izpildiet tālāk aprakstītos norādījumus. - Atveriet cilni Word izstrādātājs (pielāgojiet lenti, ja tā vēl nav iespējota).  - Atlasiet XML kartēšanas rūti.  - Uzmeklēšanā atlasiet pielāgoto XML daļu “Pārskats”.  - Veiciet atlasītās pielāgotās XML daļas elementu un Word dokumenta satura vadīklu kartēšanu.  - Atjaunināto Word dokumentu saglabājiet lokālajā diskā.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>Augšupielādēt Word veidni, kur ar satura vadīklām ir saistīta pielāgota XML daļa
1. Noklikšķiniet uz Dzēst.
2. Noklikšķiniet uz Jā.
    * Pievienojiet jaunu veidni. Ja esat izpildījis iepriekšējā apakšuzdevumā aprakstītās darbības, atlasiet Word dokumentu, kuru sagatavojāt un lokāli saglabājāt. Pretējā gadījumā atlasiet iepriekš lejupielādēto SampleVendPaymDocReportBounded.docx MS Word veidni.  
3. Noklikšķiniet uz Jauns.
4. Noklikšķiniet uz Fails.
5. Noklikšķiniet uz Pārlūkot. Pārejiet uz iepriekš lejupielādēto veidni SampleVendPaymDocReportBounded.docx un atlasiet to. Noklikšķiniet uz Labi.
6. Laukā Veidne atlasiet dokumentu, kuru lejupielādējāt iepriekšējā darbībā.
7. Noklikšķiniet uz Saglabāt.
8. Aizvērt lapu.

## <a name="execute-the-format-to-create-word-output"></a>Izpildīt formātu, lai izveidotu Word izvadi
1. Darbību rūtī noklikšķiniet uz Konfigurācijas.
2. Noklikšķiniet uz Lietotāja parametri.
3. Laukā Palaist iestatījumus atlasiet Jā.
4. Noklikšķiniet uz OK.
5. Noklikšķiniet uz Rediģēt.
6. Laukā Palaist melnrakstu atlasiet Jā.
7. Noklikšķiniet uz Saglabāt.
8. Aizvērt lapu.
9. Aizvērt lapu.
10. Pārejiet uz sadaļu Kreditori > Maksājumi > Maksājumu žurnāls.
11. Noklikšķiniet uz Rindas.
12. Sarakstā atzīmējiet visas rindas vai noņemiet tām atzīmi.
13. Noklikšķiniet uz Maksājuma statuss.
14. Noklikšķiniet uz Nav.
15. Noklikšķiniet uz Ģenerēt maksājumus.
16. Noklikšķiniet uz OK.
17. Noklikšķiniet uz OK.
    * Analizējiet ģenerēto izvadi. Ņemiet vērā, ka izveidotā izvade tiek rādīta formātā Word, un tā ietver detalizētu informāciju par apstrādātajiem maksājumiem.  


