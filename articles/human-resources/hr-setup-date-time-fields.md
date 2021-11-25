---
title: Informācija par datuma un laika laukiem
description: Šajā tēmā skaidrots, ko gaidīt, kad izmantojat Microsoft datuma un laika laukus Dynamics 365 Human Resources.
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
ms.openlocfilehash: 06c783c1e4a2961f1445909ea03d557c0985064e
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728593"
---
# <a name="understand-date-and-time-fields"></a>Informācija par datuma un laika laukiem

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Datuma un laika** lauki ir Microsoft fundamentāla koncepcija Dynamics 365 Human Resources. Ir svarīgi izprast, kā strādāt ar datuma un laika datiem lapās, in un ārējos **·** Dataverse avotos.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Izprast atšķirību starp datuma un datuma un laika lauku datu veidiem

**Datuma un** laika laukos ir ietverta informācija par laika joslu, **bet datuma lauki** nav. **Datuma** laukos vienāda informācija tiek rādīta jebkurā vietā. Ievadot datumu laukā **·** Datums, šis datums tiek rakstīts datu bāzē.

Kad dati tiek rādīti laukā Datums un laiks, datums un laiks tiek pielāgoti, pamatojoties uz lietotāja laika joslu, kas ir atlasīta lapā Lietotāja opcijas **·** **·** **(Kopējās \> iestatījuma \> lietotāja** opcijas). Datuma un laika informācija, ko ievadāt laukā, var nebūt tāda pati kā informācija, kas ierakstīta datu bāzē.

[![ Lietotāja opciju lapa.](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>Izzināšanas datuma un laika lauki lapās 

**Datuma un laika** ekrānā parādītie dati nav tādi paši kā dati, kas tiek glabāti datu bāzē, ja lietotāja laika josla nav iestatīta uz koordinēto pasaules laiku (UTC). Dati **Datuma un laika** laukos vienmēr tiek glabāti kā UTC.

[![ Darbinieka lapas UTC.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Izpratne par Datuma un laika laukiem datu bāzē 

Kad datu **bāzē tiek** ierakstīta datuma un laika vērtība, dati tiek saglabāti kā UTC. Tāpēc lietotāji var redzēt visus **datuma un laika datus attiecībā pret laika** joslu, kas ir noteikta viņu lietotāja opcijās.
 
Iepriekšminētajā piemērā sākuma laiks ir laika punkts, nevis konkrēts datums. Mainot lietotājā reģistrēto laika joslu no GMT + 12:00 uz GMT UTC, tas pats ieraksts rāda 04/30/2019 12:00:00, nevis 05/01/2019 12:00:00.

Tālāk piemērā darbinieka 000724 nodarbinātība kļūst aktīva vienlaicīgi neatkarīgi no laika zonas. Darbinieks būs aktīvs 04/30/2019 GMT laika joslā, kas ir tad pat kad 05/01/2019 GMT + 12:00 laika zonā. Abi attiecas uz vienu un to pašu punktu laikā, nevis konkrētu datumu. 

[![ Darbinieka lapas GMT.](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Datuma un laika dati Datu pārvaldības struktūrā, Excel, Dataverse un Power BI 

Datu pārvaldības struktūra (DMF), Excel pievienojumprogramma un pārskati tie visi ir veidoti, lai mijiedarbotos ar datiem Dataverse Power BI tieši datu bāzes līmenī. Tā kā nav klienta, lai koriģētu **Datuma un laika** datus uz lietotāja laika joslu, visas **Datuma un laika** vērtības ir UTC, kas var izraisīt dažus kļūdainus pieņēmumus, ievadot vai skatot datus.
 
Kad **datuma un laika dati tiek** iesniegti, izmantojot DMF, Excel vai, datu bāze pieņem, ka tā Dataverse ir UTC formātā. Tomēr, ja lietotāji, kuri skatā datus, nav iestatījuši savu lietotāja laika joslu uz UTC, iesniegtā datuma un laika vērtība neparādīsies kā paredzēts, un lietotāji var tikt **·** jaukti. 
 
Tas pats var notikt pretēji, kad dati tiek eksportēti. **Datuma un laika** dati eksportētajā DMF elementā var atšķirties no tiem, kas tiek parādīti Dynamics klientā. 
 
Lietojot ārējos avotus, piemēram, DMF, lai skatītu vai autorizētu datus, jāpatur prātā, ka pēc noklusējuma tiek uzskatīts, ka **Datuma un laika** vērtības ir UTC neatkarīgi no lietotāja datora laika joslas vai to pašreizējā lietotāja laika joslas iestatījumiem. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Viena un tā paša ieraksta piemēri, kas tiek rādīti dažādos preču apgabalos 

**Programma Human Resources ar lietotāja laika joslu iestatītu uz UTC**

[![ Darbinieka lapa iestatīta uz UTC.](./media/worker-form3.png)](./media/worker-form3.png)

**Programma Human Resources ar lietotāja laika joslu iestatītu uz GMT +12:00** 

[![ Darbinieka lapa iestatīta uz GMT.](./media/worker-form4.png)](./media/worker-form4.png)

**Excel, izmantojot OData**

[![ Excel, izmantojot OData.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF sagatavošana**

[![ DMF sagatavošana.](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF eksportēšana**

[![ DMF eksports.](./media/DMFExport.png)](./media/DMFExport.png)

**Excel, izmantojot Dataverse**

[![ Excel, izmantojot Dataverse.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Skatiet arī

[IDatuma un laika dati](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Lietotāja izvēlētās laika joslas](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
