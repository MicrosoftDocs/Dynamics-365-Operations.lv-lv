---
title: Izprotiet datuma un laika laukus
description: Saprast, ko sagaidīt, izmantojot laukus Datums un Laiks programmā Microsoft Dynamics 365 Human Resources. Iegūstiet skaidrību par to, ko sagaidīt, mijiedarbojoties ar datuma un laika datiem personāla vadības veidlapā, ārējā avotā vai Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 027e46d53fd9704f5483e90409be53c1510e8cd4
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529856"
---
# <a name="understand-date-and-time-fields"></a>Izprotiet datuma un laika laukus

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Datuma un laika** lauki ir pamatjēdzieni programmā Dynamics 365 Human Resources. Ir svarīgi saprast, kā strādāt ar **Datuma un laika** datiem Dynamics 365 Human Resources veidlapās, Common Data Service un ārējos avotos.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Izprast atšķirību starp datuma un datuma un laika lauku datu veidiem

**Datuma un laika** lauki ietver informāciju par laika joslu, bet **Datuma** lauki to neietver. **Datuma** lauki rāda vienu un to pašu informāciju jebkurā atrašanās vietā. Kad ievadāt datumu datumu laukā **Datums** programma Human Resources ieraksta šo pašu datumu datu bāzē.

Parādot datus laukā **Datums un laiks**, programma Human Resources pielāgo datumu un laiku, pamatojoties uz lietotāja laika zonu, kas iestatīta veidlapā **Lietotāja opcijas** (**Kopīgi > Iestatīšana > Lietotāja opcijas**). Datuma un laika informācija, ko ievadāt laukā, var nebūt vienāda ar datu bāzē ierakstīto informāciju.

[![Lietotāja opciju veidlapa](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Izpratne par Datuma un laika laukiem veidlapās 

Ievadot datus **Datuma un laika** laukā, ekrānā parādītie dati nav tādi paši kā dati, kas tiek glabāti datu bāzē, ja lietotāja laika josla nav iestatīta uz koordinēto pasaules laiku (UTC). Dati **Datuma un laika** laukos vienmēr tiek glabāti kā UTC.

[![Darbinieka veidlapa](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Izpratne par Datuma un laika laukiem datu bāzē 

Kad programma Human Resources ieraksta **Datuma un laika** vērtību datu bāzē, tā saglabā datus UTC. Tas ļauj lietotājiem skatīt visus **Datuma un laika** datus attiecībā pret laika joslu, kas definēta to lietotāja opcijās.
 
Iepriekšminētajā piemērā sākuma laiks ir laika punkts, nevis konkrēts datums. Mainot lietotājā reģistrēto laika joslu no GMT + 12:00 uz GMT UTC, tas pats tikko izveidotais ieraksts rāda 04/30/2019 12:00:00, nevis 05/01/2019 12:00:00.
  
Zemāk minētajā piemērā darbinieku 000724 nodarbinātība kļūst aktīva tajā pašā laikā neatkarīgi no laika zonas. Darbinieks būs aktīvs 04/30/2019 GMT laika joslā, kas ir tad pat kad 05/01/2019 GMT + 12:00 laika zonā. Abi attiecas uz vienu un to pašu punktu laikā, nevis konkrētu datumu. 

[![Darbinieka veidlapa](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a>Datuma un laika dati Datu pārvaldības struktūrā, Excel, Common Data Service un Power BI 

Datu pārvaldības struktūra, Excel pievienojumprogramma, Common Data Service un Power BI ziņošana ir paredzēta, lai mijiedarbotos ar datiem tieši datu bāzes līmenī. Tā kā nav klienta, lai koriģētu **Datuma un laika** datus uz lietotāja laika joslu, visas **Datuma un laika** vērtības ir UTC, kas var izraisīt dažus kļūdainus pieņēmumus, ievadot vai skatot datus.  
 
**Datuma un laika** dati, kas tiek iesniegti, izmantojot DMF, Excel vai Common Data Service, datu bāze pieņem, ka tie ir UTC. Tas var izraisīt pārpratumus, ja iesniegtā **Datuma un laika** vērtība netiek rādīta kā paredzēts, jo lietotājam, kurš skata datus, nav iestatīta lietotāja laika josla uz UTC. 
 
Tas pats var notikt pretēji, kad dati tiek eksportēti. **Datuma un laika** dati eksportētajā DMF elementā var atšķirties no tiem, kas tiek parādīti Dynamics klientā. 
 
Lietojot ārējos avotus, piemēram, DMF, lai skatītu vai autorizētu datus, ir svarīgi paturēt prātā, ka pēc noklusējuma tiek uzskatīts, ka **Datuma un laika** vērtības ir UTC neatkarīgi no lietotāja datora laika joslas vai to pašreizējā lietotāja laika joslas iestatījumiem. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Viena un tā paša ieraksta piemēri, kas tiek rādīti dažādos preču apgabalos 

**Programma Human Resources ar lietotāja laika joslu iestatītu uz UTC**

[![Darbinieka veidlapa](./media/worker-form3.png)](./media/worker-form3.png)

**Programma Human Resources ar lietotāja laika joslu iestatītu uz GMT +12:00** 

[![Darbinieka veidlapa](./media/worker-form4.png)](./media/worker-form4.png)

**Excel, izmantojot OData**

[![Excel, izmantojot OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF sagatavošana**

[![DMF sagatavošana](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF eksportēšana**

[![DMF sagatavošana](./media/DMFexport.png)](./media/DMFexport.png)

**Excel, izmantojot Common Data Service**

[![Excel, izmantojot Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Skatiet arī

[IDatuma un laika dati](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Lietotāja izvēlētās laika joslas](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]