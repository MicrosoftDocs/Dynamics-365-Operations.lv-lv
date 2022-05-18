---
title: Izveidot saites no personāla vadības uz citu vidi
description: Šajā tēmā skaidrots, kā izveidot saiti no Microsoft Dynamics 365 Human Resources uz citu Dynamics 365 vidi.
author: twheeloc
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d20eef4b4861d85ead1d47ca493c3a5c2d2d85e8
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712787"
---
# <a name="create-links-from-human-resources-to-another-finance-environment"></a>Izveidot saites no cilvēkresursu grupas uz citu finanšu vidi

Debitoram, iespējams, ir divas Dynamics 365 vides, kurās viņi strādā. Piemēram, klientam, iespējams Dynamics 365 Human Resources, ir Finanšu infrastruktūras vide un ir jāizveido savienojums ar citu Dynamics 365 finanšu vidi. 

Šis līdzeklis ļaus saites no cilvēkresursu lapas uz noteiktu lapu citā finanšu vidē. Konfigurējot saites, varat norādīt, kur saite būs pieejama Personāla vadības sadaļā, un mērķa lapu, kas tiks atvērta citā vidē.

> [!Note] 
> Lai iegūtu šo funkciju **, līdzekļa pārvaldībā ir jāieslēdz** personāla **vadības** lietotāju pieredzes uzlabojumi.

## <a name="configure-target-systems"></a>Mērķa sistēmu konfigurēšana

Personāla vadības sistēmas administratori var definēt saites, kas tiks attēlotas cilvēkresursu **lapās**. Konfigurācijas daļas ir finanšu vides, uz kurām vēlaties pārvietoties kā uz saites mērķi. 

Lai konfigurētu mērķa sistēmu:
1. Lapā Konfigurēt **saites** atlasiet Konfigurēt **mērķa sistēmu**.  
2. Ievadiet mērķa sistēmas nosaukumu un norādiet Finanšu vides URL. Kad mērķa sistēmas ir konfigurētas, varat definēt savas saites.

## <a name="configure-links"></a>Konfigurēt saites

Katrai saitei, ko izveidojat, būs definēta šāda informācija:
 - **Saite**: saites nosaukums. Tiek lietots tikai identifikācijai.
 - **Aktivizēt šo saiti**: Iestatīt uz **Jā**, ja vēlaties parādīt saiti ar Cilvēkresursu lietotājiem.
 - **Parādāmais** nosaukums: ievadiet nosaukumu, kas parādīsies kā saite ar sekundāro vidi. 
 - **Saite uz formu**: izvēlieties, uz kuras lapas vēlaties rādīt saiti. Saites var tikt attēlotas tikai uz darbinieku **pašapkalpošanās darbalauku** **un lapām Darbs** **,** Amats, **Darbinieks** un **Racionalizēts Darbinieks.**
 - **Grupa**: varat organizēt savas saites, izmantojot grupas. Atlasiet esošu grupu vai veidojiet jaunu, izmantojot kolonnu **Grupa**.
 - **Mērķa sistēma**: atlasiet mērķa sistēmu, kas tika izveidota, izmantojot opciju **Konfigurēt mērķa** sistēmu. Tā būs sekundārā vide, kas tiks izmantota, izmantojot saiti.
 - **Izmantot lietotāja pašreizējo uzņēmumu: Atlasiet** **Jā**, lai, pārvietojoties uz Finansēm, izmantotu lietotāja pašreizējo uzņēmumu. Atlasiet **Nē,** lai atlasītu uzņēmumu, kas jāizmanto.
 - **Mērķa** izvēlnes elements: ievadiet izvēlnes vienumu no Finanšu vides, kuru saitei vajadzētu izmantot, pārvietojoties. Ir pieejami izvēlnes vienumi, uz kuriem varat pāriet tieši. 

   Lai atrastu vajadzīgo izvēlnes elementu:
   1. Dodieties uz finanšu vidi un atveriet lapu, kas ir navigācijas mērķis. 
   2. Kopējiet izvēlnes vienumu no vietrāža URL. Piemēram, ja vēlaties, lai saite jūs pārceltu uz darbinieku sarakstu programmā Finance and Operations, ievadiet vērtību, kas vietrādī URL ir redzama aiz “&mi”. 
   3. Izvēlnes vienums pāriešanai uz darbinieku saraksta lapu šajā piemērā ir: HcmWorkerListPage_Employees.

 - **Saite uz datu avotu**: atlasiet datu avotu, uz kuru ir atsauce saite. Ir pieejami visbiežāk izmantotie avoti, piemēram, **Nodarbinātais** un **Amats**.

### <a name="access-to-links"></a>Piekļuve saitēm

Sistēmas administratori redzēs jaunizveidotās saites uz definētām lapām pat tad, ja opcija **Iespējot šo saiti** būs ir iestatīta uz **Nē**. Šo funkcionalitāti var izmantot saišu testēšanai pirms to rādīšanas citiem darbiniekiem. Visas pārējās lomas redzēs tikai konfigurētās saites pēc **opcijas Iespējot šo saiti** iestatīšanas uz **Jā**. Darbinieki, kam ir piekļuve lapām, kurās saites tiek rādītas, varēs piekļūt šīm saitēm.

Lietotājiem arī jābūt drošības tiesībām sekundārajā vidē, kas definētas, lai piekļūtu šīs vides lapām. Ja viņiem tādu nav, saites lietošanas laikā tiek parādīts drošības dialoglodziņš.

