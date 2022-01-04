---
title: Noņemtie vai novecojušie platformas līdzekļi
description: Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Finance and Operations programmu platformu atjauninājumiem.
author: sericks007
ms.date: 12/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 4ac68cfdd8f8b2c65993fbd91587e52cce56a437
ms.sourcegitcommit: a5861c2fef4071e130208ad20e26cb3a42a45cf1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/17/2021
ms.locfileid: "7927483"
---
# <a name="removed-or-deprecated-platform-features"></a>Noņemtie vai novecojušie platformas līdzekļi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Finance and Operations programmu platformu atjauninājumiem.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši. 

Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](/dynamics/s-e/global/axtechrefrep_61). Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.

## <a name="feature-removal-effective-october-2021"></a>Līdzekļu noņemšana, kas ir spēkā no 2021. gada oktobra

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Microsoft Azure SQL pārskati Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Visas darbības un pārraudzību veic platforma, iekšēji un izmantojot automatizāciju. Nebūs nepieciešama manuāla iejaukšanās.|
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, tagad ir automatizēta sistēma, kas atveido šīs iespējas novecojušas. |
| **Ietekmētie produkta apgabali**         | SQL pārskati: Pašreizējais DTU, Pašreizējās DTU detaļas, Iegūt detalizētu informāciju par bloķēšanu, Pašreizējā plāna palīglīniju saraksts, Iegūt vaicājuma ID sarakstu, Iegūt SQL vaicājumu plānu pašreizējam plāna ID, Iegūt vaicājuma plānus un izpildes statusu, Iegūt droseles configurāciju, Iegūt gaidīšanas statistiku, Uzskaitīt dārgākus vaicājumus |
| **Izvietošanas iespēja**              | Mākoņa izvietošana: ietekmē Microsoft pārvaldītas ražošanas vides un 2. pakāpes, izmantojot 5. pakāpes tekstlodziņa vides. |
| **Statuss**                         | Noņemts |

### <a name="azure-sql-actions-in-lcs"></a>Azure SQL darbības LCS

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Mēs nolietojam dažus SQL darbības LCS. Visas darbības un pārraudzību veic platforma, iekšēji un izmantojot automatizāciju. Nebūs nepieciešama manuāla iejaukšanās. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, tagad ir automatizēta sistēma, kas atveido šīs iespējas novecojušas. |
| **Ietekmētie produkta apgabali**         | SQL darbības: Izveidot plāna palīglīniju, lai spēkā būtu plāna ID, Izveidot plāna palīglīniju, lai pievienotu tabulas norādes, Noņemt plāna palīglīniju, Atspējot/iespējot lapas bloķēšanu un bloķēšanas eskalāciju, Atjaunināt statistiku tabulā, Atjaunot indeksu, Izveidot indeksu |
| **Izvietošanas iespēja**              | Mākoņa izvietošana: ietekmē Microsoft pārvaldītas ražošanas vides un 2. pakāpes, izmantojot 5. pakāpes tekstlodziņa vides. |
| **Statuss**                         | Noņemts |


## <a name="feature-deprecation-effective-october-2021"></a>Līdzekļu nolietošana, kas ir spēkā no 2021. gada oktobra

### <a name="show-related-document-attachments-feature"></a>Līdzeklis "Rādīt saistīto dokumentu pielikumus"

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Funkcija atgrieza neparedzētus rezultātus. |
| **Vai ir aizstāts ar citu līdzekli?**   | Nē. Visi turpmākie plāni saistībā ar šo funkcionalitāti tiks sasniegti, izmantojot mūsu standarta izlaišanas kopuma izpaušanas procesu. |
| **Ietekmētie produkta apgabali**         | Tīmekļa klients - dokumenta pielikumu pieredze |
| **Izvietošanas iespēja**              | Visi |
| **Statuss**                         | Novecojis  |

## <a name="platform-updates-for-version-10023-of-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmu 10.0.23 versijai

### <a name="ondbsynchronize-event"></a>OnDBSynchronize notikums

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Nav vadīklas, ko izmantot šī notikuma izpildei. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, pārvietojiet esošās metodes, **abonētais OnDBSynchronize** notikums uz SysSetup paplašināto klasi. |
| **Ietekmētie produkta apgabali**         | Datu bāzes sinhronizēšana |
| **Izvietošanas iespēja**              | Visi |
| **Statuss**                         | Novecojis. Plānotais noņemšanas datums ir 2022. gada oktobris. |


### <a name="systemnotificationsmanageraddnotification-api"></a>SystemNotificationsManager.AddNotification API

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Pievienojot paziņojumus, Microsoft pieprasa papildu parametrus. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, **SystemNotificationsManager.AddSystemNotification()** API. Šim API ir nepieciešams, lai ģenerētajiem paziņojumiem skaidri iestatītu ExpirationDateTime un RuleID. |
| **Ietekmētie produkta apgabali**         | Tīmekļa klients |
| **Izvietošanas iespēja**              | Visi |
| **Statuss**                         | Novecojis. Plānotais noņemšanas datums ir 2023. gada aprīlis. |

## <a name="platform-updates-for-version-10021-of-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmu 10.0.21 versijai

### <a name="skype-for-business-online-support"></a>Skype uzņēmumiem tiešsaistes atbalsts

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Skype uzņēmumiem tiešsaistē ir noņemts. Lai iegūtu papildu informāciju, skatieties [Skype uzņēmumiem tiešsaistes pakalpojums ir noņemts](https://techcommunity.microsoft.com/t5/microsoft-teams-blog/the-skype-for-business-online-service-has-retired/ba-p/2596601). |
| **Vai ir aizstāts ar citu līdzekli?**   | Šobrīd tā nav, lai gan mēs varam apsvērt klātbūtnes pievienošanu nākotnē no Teams.|
| **Ietekmētie produkta apgabali**         | Tīmekļa klients |
| **Izvietošanas iespēja**              | Visi |
| **Statuss**                         | Novecojis. Iestatījums **Skype ir ieslēgts** ir atslēgts no laidiena 10.0.21. Šī iestatījuma noņemšana ir plānota 2022.gada aprīlī; tomēr funkcija vairs nedarbosies, kad Skype komanda izbeigs pakalpojumu. |
 
## <a name="feature-deprecation-effective-august-2021"></a>Līdzekļu nolietošana, kas ir spēkā no 2021. gada augusta

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Microsoft Azure SQL pārskati Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Visas darbības un pārraudzību veic platforma, iekšēji un izmantojot automatizāciju. Nebūs nepieciešama manuāla iejaukšanās.|
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, tagad ir automatizēta sistēma, kas atveido šīs iespējas novecojušas. |
| **Ietekmētie produkta apgabali**         | SQL pārskati: Pašreizējais DTU, Pašreizējās DTU detaļas, Iegūt detalizētu informāciju par bloķēšanu, Pašreizējā plāna palīglīniju saraksts, Iegūt vaicājuma ID sarakstu, Iegūt SQL vaicājumu plānu pašreizējam plāna ID, Iegūt vaicājuma plānus un izpildes statusu, Iegūt droseles configurāciju, Iegūt gaidīšanas statistiku, Uzskaitīt dārgākus vaicājumus |
| **Izvietošanas iespēja**              | Mākoņa izvietošana: ietekmē Microsoft pārvaldītas ražošanas vides un 2. pakāpes, izmantojot 5. pakāpes tekstlodziņa vides. |
| **Statuss**                         | Novecojis: plānotais noņemšanas datums ir 2021. gada oktobris. |

### <a name="azure-sql-actions-in-lcs"></a>Azure SQL darbības LCS

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Mēs nolietojam dažus SQL darbības LCS. Visas darbības un pārraudzību veic platforma, iekšēji un izmantojot automatizāciju. Nebūs nepieciešama manuāla iejaukšanās. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, tagad ir automatizēta sistēma, kas atveido šīs iespējas novecojušas. |
| **Ietekmētie produkta apgabali**         | SQL darbības: Izveidot plāna palīglīniju, lai spēkā būtu plāna ID, Izveidot plāna palīglīniju, lai pievienotu tabulas norādes, Noņemt plāna palīglīniju, Atspējot/iespējot lapas bloķēšanu un bloķēšanas eskalāciju, Atjaunināt statistiku tabulā, Atjaunot indeksu, Izveidot indeksu |
| **Izvietošanas iespēja**              | Mākoņa izvietošana: ietekmē Microsoft pārvaldītas ražošanas vides un 2. pakāpes, izmantojot 5. pakāpes tekstlodziņa vides. |
| **Statuss**                         | Novecojis: plānotais noņemšanas datums ir 2021. gada oktobris. |

## <a name="feature-deprecation-effective-may-2021"></a>Līdzekļu nolietošana, kas ir spēkā no 2021. gada maijs

### <a name="globalization-portal-in-lifecycle-services-lcs"></a>Globalizācijas portāls programmā Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Mēs nolietojam globalizācijas portālu LCS, jo šo funkciju aizstāj citi LCS balstītie pakalpojumi. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, šis līdzeklis tiek aizstāts ar LCS [izsniegšanas meklēšanu](../lifecycle-services/issue-search-lcs.md) un [Dynamics uzraudzības brīdinājuma iesniegšanas pakalpojumu](../lcs-solutions/submit-localization-alerts.md). |
| **Ietekmētie produkta apgabali**         | Globalizācijas portāls programmā LCS|
| **Izvietošanas iespēja**              | Mākoņa izvietošana |
| **Statuss**                         | Novecojis: plānotais noņemšanas datums ir 2022. gada maijs. |


## <a name="feature-removed-effective-january-28-2021"></a>Līdzeklis noņemts 2021. gada 28. janvārī

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>Pakešuzdevums SQL indeksa defragmentēšanai

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Lai samazinātu operāciju, uzraudzības un klientu indeksa pārvaldības uzturēšanu papildu atbalstu, šī funkcija ir noņemta. |
| **Vai ir aizstāts ar citu līdzekli?**   | Notiekot uz priekšu, indeksa uzturēšanu veiks Microsoft pakalpojumi. Tas tiks veikts nepārtraukti, neietekmējot lietotāja darba noslodzes. |
| **Ietekmētie produkta apgabali**         | Finance and Operations programmas|
| **Izvietošanas iespēja**              | Mākoņa izvietošana — ietekmē Microsoft pārvaldītas ražošanas vides un 2. pakāpes, izmantojot 5. pakāpes tekstlodziņa vides. |
| **Statuss**                         | Šī funkcija ir noņemta. |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmu 10.0.17 versijai


### <a name="visual-studio-2015"></a>Visual Studio 2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Lai atbalstītu jaunākās Visual Studio versijas, ir jāveic dažas izmaiņas X++ paplašinājumos programmai Visual Studio. Šīs izmaiņas nav saderīgas ar Visual Studio 2015. |
| **Vai ir aizstāts ar citu līdzekli?**   | Visual Studio 2017 aizstās Visual Studio 2015 kā izvietotā un nepieciešamā versija. |
| **Ietekmētie produkta apgabali**         | Visual Studio izstrādes rīki |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: pēc atjaunināšanas iepriekšējie X++ rīki tiks noņemti no Visual Studio 2015. gada versijas un netiks atjaunināti Visual Studio 2015. gada versijā. Viesotie būvējumi netiek neietekmēti. Lai mainītu atkarību no MSBuild 14.0 (Visual Studio 2015) uz MSBuild 15.0 (Visual Studio 2017), būvējuma konveijers ir manuāli jāatjaunina, kā aprakstīts [Azure konveijera atjauninājumu konveijerā](../dev-tools/pipeline-msbuild-update.md). |

### <a name="user-avatar"></a>Lietotāja bilde 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Lietotāja displejs, kas tiek rādīts navigācijas joslas labajā pusē, tika izgūts, izmantojot API no Dynamics 365 virsraksta kontroles, kas ir novecojusi. |
| **Vai ir aizstāts ar citu līdzekli?**   | Tā vietā lietotāji redzēs viņu iniciāļus navigācijas joslā apļa pusē. Tas ir tas pats vizuālais, kas pašreiz tiek izmantots izstrādes mašīnām. |
| **Ietekmētie produkta apgabali**         | Tīmekļa klients |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Noņemts, sākot ar versiju 10.0.17 |

### <a name="enterprise-portal-ep-deprecation"></a>Uzņēmuma portāla (EP) nolietojuma aprēķins  

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Ar Dynamics AX 2012 uzņēmuma portālu (EP) saistītie metadatu artefakti ir novecojuši, jo EP nekad netiek atbalstīts programmās Finance and Operations. |
| **Vai ir aizstāts ar citu līdzekli?**   | Nē |
| **Ietekmētie produkta apgabali**         | Tīmekļa klients |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: visi EP kodi ir ieplānoti izņemšanai no 2021. gada oktobra. |

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmu 10.0.15 versijai

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 atbalsts Dynamics 365 ir novecojis

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Sākot ar 2020. gada decembri, Microsoft Internet Explorer 11 atbalsts visām Dynamics 365 precēm ir novecojis, un Internet Explorer 11 netiks atbalstīts pēc 2021. gada augusta.<br><br>Tas ietekmēs klientus, kas izmanto Dynamics 365 preces, kas paredzētas izmantošanai ar Internet Explorer 11 interfeisu. No 2021. gada augusta Internet Explorer 11 šīs Dynamics 365 preces netiks atbalstītas. |
| **Vai ir aizstāts ar citu līdzekli?**   | Mēs rekomendējam, lai klienti pāriet uz Microsoft Edge.|
| **Ietekmētie produkta apgabali**         | Visas Dynamics 365 preces |
| **Izvietošanas iespēja**              | Visu|
| **Statuss**                         | Novecojis: Internet Explorer 11 netiks atbalstīts pēc 2021. gada augusta.|


### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Visual Studio pievienojumprogramma, lai lietotu metadatu labojumfailus

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Metadatu labojumfaili vairs netiek atbalstīti ar [One Version](../../fin-ops/get-started/one-version.md) pakalpojuma atjauninājumiem, kas tika ieviesti 2018. jūlijā ar versiju 8.1. |
| **Vai ir aizstāts ar citu līdzekli?**   | Atsevišķi metadatu labojumfaili nav pieejami atbalstītajām versijām. Tā vietā tiek piemēroti kumulatīvi kvalitātes atjauninājumi. |
| **Ietekmētie produkta apgabali**         | Visual Studio pievienojumprogrammas |
| **Izvietošanas iespēja**              | Izstrādes virtuālās mašīnas |
| **Statuss**                         | Izmantojot versiju 10.0.15, pievienojumprogramma vairs nav iekļauta Visual Studio rīkos. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmu 10.0.14 versijai

### <a name="online-users-page"></a>Tiešsaistes lietotāju lapa 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šī ir mantota lapa, kas tika izveidota iepriekšējā klienta/servera arhitektūrai. Informācija šajā lapā ne vienmēr ir precīza, kas var būt mulsinoši un maldinoši. |
| **Vai ir aizstāts ar citu līdzekli?**   | Turpmākajā atjauninājumā tiks nodrošināta jauna lapa.|
| **Ietekmētie produkta apgabali**         | Sistēmas administrēšana |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Līdz 2021. gada oktobrim šī veidlapa tiks noņemta.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmu 10.0.13 versijai


### <a name="custom-code-defined-in-ssrs-report-properties"></a>Pielāgots kods, kas definēts SSRS pārskata rekvizītos 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Parasti pielāgots kods piedāvā ierobežotas priekšrocības, tajā pašā laikā nodrošina būtisku resursu piešķiršanu un aprēķina atbalstu. Pielāgotu kodu galvenokārt izmanto pārskatu autori, lai izsauktu publiskās metodes no pielāgotas koda komplektācijas. Tomēr mākoņa viesots pakalpojums neatbalsta atsauces uz sistēmas SSRS pārskatus pielāgotajām komplektācijām. |
| **Vai ir aizstāts ar citu līdzekli?**   | Pārskata autori var izvēlēties turpināt atsauces uz publiskajiem .NET API matemātikai, pārveidošanai un formāta operācijām no jebkuras tekstlodziņa izteiksmes. Papildinformāciju skatiet sadaļā [Koda pievienošana pārskatam (SSRS)](/sql/reporting-services/report-design/add-code-to-a-report-ssrs).  |
| **Ietekmētie produkta apgabali**         | To programmas pārskata noformējumu apakškopa, kas definētas RDL, kas satur pielāgotu kodu. |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Izmantojot versiju 10.0.13, kompilators sāks brīdinājuma izdošanu gadījumiem, kad pielāgots kods tiek noteikts SSRS pārskata definīcijā. Lai labotu problēmu, atveriet pārskata noformējuma definīciju un noņemiet visus pielāgotos kodu artefaktus. Šis brīdinājums tiks aizstāts ar kompilatora kļūdu turpmākajā atjauninājumā.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Triju jQuery komponentu bibliotēku jaunināšana 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Trīs jQuery komponentu bibliotēkas tiek atjauninātas drošības labojumiem un valūtas uzturēšanai.   
| **Vai ir aizstāts ar citu līdzekli?**   | Tiek ietekmētas šādas bibliotēkas: jQuery (uz versiju 3.5.0 no versijas 2.1.4), jQuery UI (uz versiju 1.12.1 no versijas 1.11.4), jQuery qTip (uz versiju 3.0.3 no 2.2.1). Migrācijas vadlīnijas ir nodrošinātas tiešsaistē ar jQuery.  |
| **Ietekmētie produkta apgabali**         | Paplašināmās vadīklas, īpaši pielāgots JavaScript kods, izmantojot novecojušus vai noņemtus API |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Ar versiju 10.0.13/Platformas atjauninājums 37 klienti pēc izvēles var pārvietoties uz jaunākajām bibliotēkām, iespējojot līdzekli "Jaunināt trīs jQuery komponentu bibliotēkas". Pāreja uz jaunajām bibliotēkām būs obligāta ar 2021. gada aprīļa izlaidumu, lai atļautu laiku ietekmēto API migrācijai.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Esošā režģa vadīkla/forceLegacyGrid() API

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Esošā režģa vadīkla tiek aizstāta ar jauno režģa vadīklu. |
| **Vai ir aizstāts ar citu līdzekli?**   | [Jaunā režģa vadīkla](../..//fin-ops/get-started/grid-capabilities.md) |
| **Ietekmētie produkta apgabali**         | Tīmekļa klients |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Versijā 10.0.13 jaunā režģa vadīkla ir vispārēji pieejama, un klienti pēc izvēles var ieslēgt šo līdzekli. Jaunā režģu vadība kļūs par noklusējuma vadību ar 2021. gada laidienu, un tiek plānots, ka tā kļūs obligāta 2022. gada aprīlī. Kad jaunā režģa kontrole kļūs obligāta, **forceLegacyGrid()** API vairs netiks uzturēta. |

### <a name="personalization-without-saved-views"></a>Personalizācija bez saglabātajiem skatiem 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Personalizācijas apakšsistēma ir pārstrādāta ar saglabāto skatījumu līdzekli, lai tā varētu uzlabot veiktspēju un piedāvāt papildu iespējas. |
| **Vai ir aizstāts ar citu līdzekli?**   | Saglabātie skati |
| **Ietekmētie produkta apgabali**         | Tīmekļa klients |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Versijā 10.0.13/Platform atjauninājums 37, ir vispārēji pieejami saglabāto skatījumu līdzekļi, un klienti pēc izvēles var ieslēgt šo līdzekli. Saglabātā skatījuma līdzeklis kļūs obligāts 2021. gada oktobra laidienā. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmu 10.0.12 versijai

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Režģa vai grupas vadīklu veidlapas paplašinājumi, kas satur nederīgas lauku atsauces

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Datu grupas rekvizīts režģī vai grupas vadīklās tiek izmantots, lai automātiski parādītu visus lauku grupas laukus. Režģa vai grupas vadīkla, kas pievienota ar paplašinājumu, var saturēt laukus, kas vairs nav definēti lauku grupā, vai varbūt trūkst lauku grupā definēto lauku. Tas var izraisīt nekonsekventu darbību izpildlaikā. Platformas atjauninājumi Finance and Operations programmu 10.0.12 versija tagad iedala šo problēmu kā kompilatora *brīdinājumu*. Lai labotu šo problēmu, atveriet veidlapas paplašinājumu un saglabājiet to.
| **Vai ir aizstāts ar citu līdzekli?**   | Šis kompilatora brīdinājums tiks aizstāts ar kompilatora kļūdu turpmākajā atjauninājumā. |
| **Ietekmētie produkta apgabali**         | Visual Studio izstrādes rīki |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Kompilatora brīdinājums ir ieviests platformas atjauninājumos Finance and Operations programmu 10.0.12 versijā. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmu 10.0.11 versijai

### <a name="explicit-safe-lists-for-self-service-environments"></a>Precīzi drošie saraksti pašapkalpošanās videi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Ir mainījies process, kurā IP tiek pārvietoti uz drošajiem sarakstiem. Pašapkalpošanās vairs neatbalsta IP iekļaušanu drošajā sarakstā. |
| **Vai ir aizstāts ar citu līdzekli?**   | Plašāku informāciju skatiet [Konfigurēt Azure Active Directory nosacījuma piekļuvi](/appcenter/general/configuring-aad-conditional-access).|
| **Ietekmētie produkta apgabali**         | Drošība |
| **Izvietošanas iespēja**              | Mākonis |
| **Statuss**                         | Novecojis: šis līdzeklis ir pilnībā novecojis pašapkalpošanās izvietošanai. |

### <a name="visual-studio-2015"></a>Visual Studio 2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Lai atbalstītu jaunākās Visual Studio versijas, ir jāveic dažas izmaiņas X++ paplašinājumos programmai Visual Studio. Šīs izmaiņas nav saderīgas ar Visual Studio 2015. |
| **Vai ir aizstāts ar citu līdzekli?**   | Visual Studio 2017 aizstās Visual Studio 2015 kā izvietotā un nepieciešamā versija. |
| **Ietekmētie produkta apgabali**         | Visual Studio izstrādes rīki |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Virtuālās mašīnas, kas izvietotas versijā 10.0.13 (platformas atjauninājums 37) vai jaunākā versijā, ietver Visual Studio 2017. Versija 10.0.16 (platformas atjauninājums 40) ir galīgais laidiens ar Visual Studio 2015 atbalstu. Virtuālās mašīnas, kurām ir tikai Visual Studio 2015, nevarēs veikt jaunināšanu uz versiju 10.0.17 (platformas atjauninājums 41). |

### <a name="field-groups-containing-invalid-field-references"></a>Lauku grupas, kas ietver nederīgas lauku atsauces

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Tabulas metadatu definīcijās lauku grupas var ietvert lauku atsauces, kas nav derīgas. Ja šīs lauku grupas ir izvietotas, tās var izraisīt izpildlaika kļūmes modulī Financial Reporting un Microsoft SQL Server pārskatu izveides pakalpojumos (SSRS). Platformas atjauninājums 23 ieviesa kompilatora *brīdinājumu*, kas ļāva risināt šo metadatu problēmu. Platformas atjauninājumi Finance and Operations programmu 10.0.11 versija iedala šo problēmu kā kompilatora *kļūdu*.<p>Lai novērstu šo problēmu, izpildiet sekojošās darbības.</p><ol><li>Noņemiet nederīgo lauka atsauci no tabulas lauku grupas definīcijas.</li><li>Pārkompilēt.</li><li>Pārliecinieties, vai kļūdas ir novērstas.</li></ol> |
| **Vai ir aizstāts ar citu līdzekli?**   | Šī kompilatora kļūda neatgriezeniski aizstāj kompilatora brīdinājumu.  |
| **Ietekmētie produkta apgabali**         | Visual Studio izstrādes rīki |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: kompilatora brīdinājums ir kompilatora kļūda platformas atjauninājumiem Finance and Operations programmu 10.0.11 versijā. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>ISV licences, kas izveidotas, izmantojot SHA1 hashing algoritmu

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Neatkarīgu programmatūras piegādātāju (ISV) licenču izveides process ir mainījies. Lai iegūtu papildinformāciju, skatiet [Neatkarīga programmatūras izstrādātāja (ISV) licencēšana](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā. Izmantojiet programmu Windows PowerShell, lai izveidotu licences. |
| **Ietekmētie produkta apgabali**         | Visual Studio izstrādes rīki |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: ISV licences, kas izveidotas, izmantojot SHA1 jaukšanas algoritmu. Šis algoritms ir atkarīgs no sertifikātiem, kas tika izveidoti, izmantojot utilītu MakeCert, un šī utilīta ir novecojusi.<br><br>Novecojusi: SHA1 izmantošana drošības vai jaukšanas nolūkiem. SHA1 vairs nedarbosies 2021. gada sākumā. Tāpēc tas vairs nav jālieto.<br><br>Noņemts: atbalsts transporta slāņa drošībai (TLS) 1.0 un TLS 1.1 ienākošajiem vai izejošajiem pieprasījumiem. |

## <a name="platform-update-32"></a>Platformas update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Darbplūsmas pieprasījuma maiņas dialoglodziņā vairs nav lietotāja atlases nolaižamā saraksta

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Tas bija drošības jautājums, jo izmaiņu pieprasījums var tikt nosūtīts neparedzētam lietotājam. Tas bija arī lietojamības jautājums, jo tas lika lietotājam noteikt, kas bijis darbplūsmas iniciators un viņu manuāli atlasīt.  |
| **Vai ir aizstāts ar citu līdzekli?**   | Nē |
| **Ietekmētie produkta apgabali**         | Darbplūsma |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Lietotāja atlases nolaižamais saraksts tika noņemts no izmaiņu pieprasīšanas dialoglodziņa Platform atjauninājumā 32. Pieprasījuma izmaiņu pieprasījumi automātiski tiks nosūtīti iniciatoram, kā paredzēts. Plašāku informāciju par šo funkcionalitāti skatiet [Darbības darbplūsmas apstiprināšanas procesos](../../fin-ops/organization-administration/workflow-actions.md?toc=%2fdynamics365%2fcommerce%2ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Iegultās detalizētās saites vairs netiek atbalstītas numurētos dokumentos, ko sniedz mākoņa balstītais pakalpojums 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Pakalpojuma sniegto dokumentu iegultās navigācijas URL var saturēt sensitīvus biznesa datus. Mēs noņemam atbalstu iegultām urbšanas saitēm dokumentos kā drošības piesardzības līdzekli, lai turpmāk aizsargātu klienta datus. Lietotāji arī gūs labumu no uzlabotas veiktspējas, vienlaikus interaktīvi veidojot dokumentus šo izmaiņu dēļ.  |
| **Vai ir aizstāts ar citu līdzekli?**   | Nē |
| **Ietekmētie produkta apgabali**         | Pārskatu veidošana |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Šis līdzeklis tiek noņemts no pakalpojuma.<br><br>Mūsdienu klients piedāvā daudzas opcijas tādu skatu izveidei, kas ietver automātiski ģenerētās saites, lai palīdzētu programmas pārskatīšanai. Ar pakalpojumu sniegtie, numurētie dokumenti ir ieteicami ārējiem sakariem, kas tiek sūtīti pa e-pastu, arhivēti un izdrukāti adresātiem. Mēs esam uzlabojuši pieredzi dokumentu priekšskatīšanai tieši pārlūkprogrammā, kas piedāvā tiešu piekļuvi lokālajiem printeriem. Papildinformāciju skatiet šeit [PDF dokumentu priekšskatījums ar iegultu skatītāju](../analytics/preview-pdf-documents.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Iepriekšēji paziņojumi par noņemtiem vai novecojušiem līdzekļiem
Lai uzzinātu vairāk par līdzekļiem, kas iepriekšējos laidienos ir noņemti vai novecojuši, skatiet [Noņemti vai novecojuši līdzekļi iepriekšējos laidienos](../migration-upgrade/deprecated-features.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
