---
title: Plānot pārdošanas vēstures datu tīrīšanu
description: Šajā rakstā ir aprakstīts, kā var palīdzēt uzlabot sistēmas veiktspēju, plānojot pārdošanas atjaunināšanas vēstures tīrīšanas periodisko uzdevumu, lai palaistu regulārā intervālā.
author: myvakalo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e9a4dd5372afa8a0452449d1cb9121107e6e1610
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335509"
---
# <a name="schedule-sales-history-data-cleanup"></a>Plānot pārdošanas vēstures datu tīrīšanu

[!include [banner](../includes/banner.md)]

Kā daļu no savas standarta operācijas Microsoft Dynamics 365 Supply Chain Management ģenerē un saglabā pārdošanas vēstures atjauninātos datus, balstoties uz notiekošu darbību. Laika gaitā jūsu sistēmā var uzkrāties lieli novecojuši pārdošanas vēstures dati. Šie uzkrātie dati var radīt veiktspējas un funkcionālos jautājumus, kad tiek grāmatoti ar pārdošanas pasūtījumiem saistītie dokumenti. (Šie dokumenti ietver pārdošanas pasūtījuma apstiprinājumus, pārdošanas pavadzīmes, pārdošanas izdošanas sarakstus un rēķinus). Tāpēc jums ir jāiestata un jāplāno Pārdošanas *atjaunināšanas vēstures tīrīšanas* periodiskais uzdevums, lai palaistu regulārā intervālā. Šis uzdevums noņems visus pārdošanas vēstures atjaunināšanas datus, kas vairs nav vajadzīgi.

Ja tiek izmantots pārdošanas *atjaunināšanas* vēstures tīrīšanas periodiskais uzdevums, *ir* ieteicams iespējot pārdošanas vēstures tīrīšanas veiktspējas uzlabojumu funkciju, kas padara uzdevumu efektīvāku. (Tomēr uzdevumu var palaist arī bez šīs funkcijas iespējošanas.)

## <a name="turn-on-the-sales-history-cleanup-features"></a>Ieslēgt pārdošanas vēstures tīrīšanas funkcijas

*Lai* iestatītu un lietotu pārdošanas atjaunināšanas vēstures tīrīšanas periodisko uzdevumu un visus šajā rakstā aprakstītos līdzekļus, *·* *ir* jāiespējo pārdošanas vēstures veiktspējas uzlabojumi un notīriet pārdošanas atjaunināšanas vēsturi, pamatojoties uz līdzekļu pārvaldības vecuma funkcijām, kā aprakstīts tālāk aprakstītajās apakšsadaļās.

### <a name="sales-history-cleanup-performance-improvements"></a>Pārdošanas vēstures tīrīšanas veiktspējas uzlabojumi

Periodiskā pakešuzdevuma **Pārdošanas atjauninājumu vēstures tīrīšana** var aizņemt ilgu laiku, ja tā netiek palaista regulāri vidēs ar lielu pārdošanas atjauninājumu daudzumu. Šādās situācijās *Pārdošanas vēstures tīrīšanas veiktspējas uzlabojumu* līdzeklis var palīdzēt samazināt izpildes ilgumu un uzlabot uzticamību.

Līdzeklis uzlabo esošo tīrīšanas darbu šādos veidos:

- Tīrīšanas darbs tiek sadalīts partijās (partijas lielumu var mainīt, izmantojot pielāgojumus).
- Tas tiks izpildīts 2 stundu laikā (ilgumu var mainīt, izmantojot pielāgojumus).
- Ja iespējams, tiks līdzsvarotas datu bāzes iespējas, lai samazinātu bloķēšanas konkurenci un izvairītos no darbību tabulu pievienošanas tīrīšanas laikā.

Pēc līdzekļa iespējošanas **Pārdošanas atjauninājumu vēstures tīrīšanas** pakešuzdevums (**Pārdošana un mārketings \> Periodu uzdevumi \> Tīrīšana \> Pārdošanas atjauninājumu vēstures tīrīšana**) tiks palaists kā iepriekš, bet ar labāku veiktspēju un maksimums uz divām stundām. Tas nozīmē, ka līdzekli var būt nepieciešams palaist vairākas reizes, lai notīrītu visus datus noteiktā glabāšanas laika posmā.

Pirms varat lietot šo funkciju, tai jābūt ieslēgtai jūsu sistēmai. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Pārdošana un mārketings*
- **Līdzekļa nosaukums:** *Pārdošanas vēstures tīrīšanas veiktspējas uzlabojumi*

### <a name="clean-up-sales-update-history-based-on-age"></a>Pārdošanas atjauninājumu vēstures tīrīšana, pamatojoties uz vecumu

Pārdošanas *atjaunināšanas tīrīšanas vēsture* *, pamatojoties uz vecuma funkciju, ļauj norādīt maksimālo ierakstu vecumu, kas jāsaglabā, kad tiek palaists pārdošanas atjaunināšanas vēstures tīrīšanas* periodiskais uzdevums. Vecāki ieraksti tiks dzēsti. Šī funkcija ir noderīga, iestatot uzdevumu periodiskai izpildei, jo vecums vienmēr tiek aprēķināts attiecībā pret datumu, kad uzdevums tiek palaists. Ja neizmantojat šo līdzekli, var iestatīt tikai specifisku datumu vecākajiem ierakstiem, kurus saglabāt.

Lai izmantotu šo funkciju, tai jābūt ieslēgtai jūsu sistēmai. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 funkcija ir obligāta, un to nevar izslēgt. Ja lietojat versiju, kas vecāka par 10.0.29 versiju, administratori var ieslēgt vai izslēgt šo funkcionalitāti, meklējot pārdošanas atjauninājumu vēstures notīrīšana, pamatojoties uz līdzekļu pārvaldības *darbvietas*[vecuma](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) līdzekli.

## <a name="set-up-and-schedule-the-sales-history-cleanup-periodic-task"></a>Iestatīt un plānot pārdošanas vēstures tīrīšanas periodisko uzdevumu

Lai iestatītu un plānotu pārdošanas vēstures *tīrīšanas periodisko* uzdevumu, sekojiet šiem soļiem.

1. Analizējiet savas biznesa vajadzības, lai noteiktu, cik dienas vēsturiskos pārdošanas pasūtījuma grāmatošanas datus jāsaglabā. Parasti ieteicams veikt tīrīšanas uzdevumu ik pēc trim mēnešiem un maksimāli ik pēc sešiem mēnešiem.
1. Pārejiet uz **tirdzniecības un mārketinga \> perioda uzdevumu \> tīrīšanas \> pārdošanas atjaunināšanas vēstures tīrīšanu**.
1. Kopsavilkuma cilnes **Parametri dialoglodziņā Pārdošanas** atjaunināšanas tīrīšana **iestatiet** šādus laukus:

    - **Tīrīšana —** atlasiet vienu no šīm vērtībām, lai norādītu tīrāmo ierakstu tipu:

        - **Izpildīts** - dzēsiet tikai tos ierakstus, kas ir pilnībā apstrādāti. Sakarā ar to, ka šiem ierakstiem maz ticams, ka šī opcija ir seifā.
        - **Izpildīts un kļūdains – dzēsiet** gan pilnībā apstrādātos, gan ierakstus, kuros radusies kļūda. Šī opcija ir visbiežāk izmantotā opcija. Varat vēlēties pārbaudīt un pat izlabot kļūdainus ierakstus tā vietā, lai tie tiktu automātiski iztīrīti. Tomēr daudzi uzņēmumi izvēlas iztīrīt šos ierakstus pārāk pēc mēneša, jo tie, iespējams, līdz tam laikam vairs nav saistīti.
        - **visi** – dzēsiet izpildītos, kļūdainos un gaidošos ierakstus; Gaidīšanas ieraksti ir derīgi, bet vēl nav pilnībā apstrādāti. Vairumā gadījumu, iespējams, nevēlaties tos dzēst automātiski. Tomēr dažās situācijās var izvēlēties, lai tie tiktu automātiski dzēsti pēc noteikta laika pagājis.

    - **Saglabājiet ierakstus,** pamatojoties uz vecumu – norādiet, vai vēlaties iztīrīt ierakstus, pamatojoties uz viņu vecumu dienā, kad uzdevums tiek palaists, vai dzēst ierakstus, kas tika izveidoti pirms fiksētā datuma. Plānojot tīrīšanu kā periodisku uzdevumu, *šī* opcija ir jāiestata uz Jā, jo vecums vienmēr tiek aprēķināts attiecībā pret datumu, kad uzdevums tiek izpildīts.

        - Iestatiet šo opciju jā *,* lai aktivizētu **maksimālo vecuma** lauku. Šo lauku izmanto, lai norādītu ierakstu maksimālo vecumu, kas jāsaglabā katru reizi, kad uzdevums tiek palaists. Lauks **Izveidots līdz** tiek ignorēts.
        - Iestatiet šo opciju, lai *iespējotu* lauku **Izveidots līdz**. šis lauks tiek lietots, lai norādītu vecāko uzdevuma izpildes laikā saglabāto ierakstu izveides datumu. Maksimālais **vecuma lauks** tiek ignorēts.

    - **Izveidots līdz** – šis iestatījums attiecas tikai uz tad, ja **opcija Saglabāt ierakstus, pamatojoties uz** vecumu ir iestatīta uz *Nē*. Norādiet vecāko uzdevuma izpildes laikā jāsaglabā ierakstu izveides datumu. Ieraksti, kas izveidoti pirms šī datuma, tiks dzēsti.
    - **Maksimālais vecums** – šis iestatījums attiecas tikai uz tad, ja **opcija Saglabāt ierakstus, pamatojoties uz** vecumu ir iestatīta uz *Jā*. Norādiet ierakstu maksimālo vecumu (dienās), kas jāsaglabā katru reizi, kad uzdevums tiek palaists. Vecāki ieraksti tiks dzēsti.

1. Kopsavilkuma cilnē **Izpildīt fonā** norādiet, kā, kad un cik bieži uzdevums tiek izpildīts. Izmantojiet šos iestatījumus, lai ieviestu grafiku, ko noteicis 1. solī. Lauki darbojas tāpat, kā tie citiem pakešuzdevumu [tipiem](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Piegādes ķēžu pārvaldībā.
1. Atlasiet **Labi**, lai iestatījumus piemērotu un aizvērtu dialoglodziņu.
