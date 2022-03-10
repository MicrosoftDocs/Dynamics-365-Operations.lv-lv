---
title: Informācija par datuma un laika laukiem
description: Šajā tēmā ir paskaidrots, kas sagaidāms, izmantojot Microsoft laukus Datums un laiks Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c81155f0c5150af44982f224c8eca2026a78ee7
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060893"
---
# <a name="understand-date-and-time-fields"></a>Informācija par datuma un laika laukiem

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



**Datums un laiks** lauki ir Microsoft pamatjēdziens Dynamics 365 Human Resources. Ir svarīgi, lai jūs saprastu, kā ar to strādāt **Datums un laiks** dati lapās, in Dataverse un ārējos avotos.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Izprast atšķirību starp datuma un datuma un laika lauku datu veidiem

**Datums un laiks** laukos ir informācija par laika joslu, savukārt **Datums** laukiem nav. **Datums** laukos tiek rādīta viena un tā pati informācija jebkurā vietā. Ievadot datumu laukā a **Datums** laukā tas pats datums tiek ierakstīts datu bāzē.

Kad dati tiek parādīti a **Datums un laiks** laukā datums un laiks tiek pielāgoti, pamatojoties uz lietotāja laika joslu, kas ir atlasīta **Lietotāja opcijas** lappuse (**Bieži \> Uzstādīt \> Lietotāja opcijas**). Laukā ievadītā datuma un laika informācija var nebūt tāda pati kā informācija, kas tiek ierakstīta datu bāzē.

[![Lietotāja opciju lapa.](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>Izpratne par datuma un laika laukiem lapās 

**Datuma un laika** ekrānā parādītie dati nav tādi paši kā dati, kas tiek glabāti datu bāzē, ja lietotāja laika josla nav iestatīta uz koordinēto pasaules laiku (UTC). Dati **Datuma un laika** laukos vienmēr tiek glabāti kā UTC.

[![Darba ņēmēja lapa UTC.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Izpratne par Datuma un laika laukiem datu bāzē 

Kad **Datums un laiks** vērtība tiek ierakstīta datu bāzē, dati tiek saglabāti kā UTC. Tāpēc lietotāji var redzēt jebkuru **Datums un laiks** datus saistībā ar laika joslu, kas definēta viņu lietotāja opcijās.
 
Iepriekšminētajā piemērā sākuma laiks ir laika punkts, nevis konkrēts datums. Mainot lietotājā reģistrēto laika joslu no GMT + 12:00 uz GMT UTC, tas pats ieraksts rāda 04/30/2019 12:00:00, nevis 05/01/2019 12:00:00.

Tālāk esošajā piemērā darbinieka 000724 nodarbinātība kļūst aktīva vienlaikus neatkarīgi no laika joslas. Darbinieks būs aktīvs 04/30/2019 GMT laika joslā, kas ir tad pat kad 05/01/2019 GMT + 12:00 laika zonā. Abi attiecas uz vienu un to pašu punktu laikā, nevis konkrētu datumu. 

[![Darbinieka lapa GMT.](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Datuma un laika dati Datu pārvaldības struktūrā, Excel, Dataverse un Power BI 

Datu pārvaldības sistēma (DMF), Excel pievienojumprogramma,Dataverse, un Power BI Visi ziņojumi ir paredzēti, lai mijiedarbotos ar datiem tieši datu bāzes līmenī. Tā kā nav klienta, lai koriģētu **Datuma un laika** datus uz lietotāja laika joslu, visas **Datuma un laika** vērtības ir UTC, kas var izraisīt dažus kļūdainus pieņēmumus, ievadot vai skatot datus.
 
Kad **Datums un laiks** dati tiek iesniegti, izmantojot DMF, Excel vai Dataverse, datu bāze pieņem, ka tas ir UTC. Tomēr, ja lietotājiem, kuri skatās datus, lietotāja laika joslai nav iestatīta UTC, tiek iesniegts **Datums un laiks** vērtība neparādīsies, kā paredzēts, un lietotāji var apjukt. 
 
Tas pats var notikt pretēji, kad dati tiek eksportēti. **Datuma un laika** dati eksportētajā DMF elementā var atšķirties no tiem, kas tiek parādīti Dynamics klientā. 
 
Lietojot ārējos avotus, piemēram, DMF, lai skatītu vai autorizētu datus, jāpatur prātā, ka pēc noklusējuma tiek uzskatīts, ka **Datuma un laika** vērtības ir UTC neatkarīgi no lietotāja datora laika joslas vai to pašreizējā lietotāja laika joslas iestatījumiem. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Viena un tā paša ieraksta piemēri, kas tiek rādīti dažādos preču apgabalos 

**Programma Human Resources ar lietotāja laika joslu iestatītu uz UTC**

[![Darbinieka lapa iestatīta uz UTC.](./media/worker-form3.png)](./media/worker-form3.png)

**Programma Human Resources ar lietotāja laika joslu iestatītu uz GMT +12:00** 

[![Darbinieka lapa iestatīta uz GMT.](./media/worker-form4.png)](./media/worker-form4.png)

**Excel, izmantojot OData**

[![Excel, izmantojot OData.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF sagatavošana**

[![DMF sagatavošana.](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF eksportēšana**

[![DMF eksports.](./media/DMFExport.png)](./media/DMFExport.png)

**Excel, izmantojot Dataverse**

[![Excel, izmantojot Dataverse.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Skatiet arī

[IDatuma un laika dati](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Lietotāja izvēlētās laika joslas](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
