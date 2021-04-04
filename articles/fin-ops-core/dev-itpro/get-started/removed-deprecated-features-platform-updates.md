---
title: Noņemtie vai novecojušie platformas līdzekļi
description: Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Finance and Operations programmu platformu atjauninājumiem.
author: sericks007
manager: AnnBe
ms.date: 02/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: f363b122e30990f5b36e69fd8fe271bdc15e2e79
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563998"
---
# <a name="removed-or-deprecated-platform-features"></a>Noņemtie vai novecojušie platformas līdzekļi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Finance and Operations programmu platformu atjauninājumiem.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši. 

Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](https://docs.microsoft.com/dynamics/s-e/global/axtechrefrep_61). Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.

## <a name="feature-removed-effective-january-28-2021"></a>Līdzeklis noņemts 2021. gada 28. janvārī

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>Pakešuzdevums SQL indeksa defragmentēšanai

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Lai samazinātu operāciju, uzraudzības un klientu indeksa pārvaldības uzturēšanu papildu atbalstu, šī funkcija ir noņemta. |
| **Vai ir aizstāts ar citu līdzekli?**   | Notiekot uz priekšu, indeksa uzturēšanu veiks Microsoft pakalpojumi. Tas tiks veikts nepārtraukti, neietekmējot lietotāja darba noslodzes. |
| **Ietekmētie produkta apgabali**         | Finance and Operations programmas|
| **Izvietošanas iespēja**              | Mākoņa izvietošana — ietekmē Microsoft pārvaldītas ražošanas vides un 2. pakāpes, izmantojot 5. pakāpes tekstlodziņa vides. |
| **Statuss**                         | Šī funkcija ir noņemta. |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmu 10.0.17 versijai

> [!IMPORTANT]
> Versija 10.0.17 ir pieejama kā daļa no priekšskatījuma laidiena. Saturs un funkcionalitāte var tikt mainīti. Papildinformāciju par priekšskatījuma laidieniem skatiet sadaļā [Bieži uzdotie jautājumi par vienas versijas pakalpojuma atjauninājumiem](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).

### <a name="visual-studio-2015"></a>Visual Studio2015

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Lai atbalstītu jaunākās Visual Studio versijas, ir jāveic dažas izmaiņas X++ paplašinājumos programmai Visual Studio. Šīs izmaiņas nav saderīgas ar Visual Studio 2015. |
| **Vai ir aizstāts ar citu līdzekli?**   | Visual Studio 2017 aizstās Visual Studio 2015 kā izvietotā un nepieciešamā versija. |
| **Ietekmētie produkta apgabali**         | Visual Studio izstrādes rīki |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis. Pēc atjaunināšanas iepriekšējie X++ rīki tiks noņemti no Visual Studio 2015. gada versijas un netiks atjaunināti Visual Studio 2015. gada versijā. Viesotie būvējumi netiek neietekmēti. Lai mainītu atkarību no MSBuild 14.0 Visual Studio (2015) uz MSBuild 15.0 (Visual Studio2017), būvējuma konveijers ir manuāli jāatjaunina, kā aprakstīts [Azure konveijera atjauninājumu konveijerā](../dev-tools/pipeline-msbuild-update.md). |

### <a name="user-avatar"></a>Lietotāja bilde 

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Lietotāja displejs, kas tiek rādīts navigācijas joslas labajā pusē, tika izgūts, izmantojot API no Dynamics 365 virsraksta kontroles, kas ir novecojusi. |
| **Vai ir aizstāts ar citu līdzekli?**   | Tā vietā lietotāji redzēs viņu iniciāļus navigācijas joslā apļa pusē. Tas ir tas pats vizuālais, kas pašreiz tiek izmantots izstrādes mašīnām. |
| **Ietekmētie produkta apgabali**         | Tīmekļa klients |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Noņemts, sākot ar versiju 10.0.17 |

### <a name="enterprise-portal-ep-deprecation"></a>Uzņēmuma portāla (EP) nolietojuma aprēķins  

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Ar Dynamics AX 2012 uzņēmuma portālu (EP) saistītie metadatu artefakti ir novecojuši, jo EP nekad netiek atbalstīts programmās Finance and Operations. |
| **Vai ir aizstāts ar citu līdzekli?**   | Nr. |
| **Ietekmētie produkta apgabali**         | Tīmekļa klients |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis. Visi EP kodi ir ieplānoti izņemšanai no 2021. gada oktobra. |

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmu 10.0.15 versijai

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 atbalsts Dynamics 365 ir novecojis

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Sākot ar 2020. gada decembri, Microsoft Internet Explorer 11 atbalsts visām Dynamics 365 precēm ir novecojis, un Internet Explorer 11 netiks atbalstīts pēc 2021. gada augusta.<br><br>Tas ietekmēs klientus, kas izmanto Dynamics 365 preces, kas paredzētas izmantošanai ar Internet Explorer 11 interfeisu. No 2021. gada augusta Internet Explorer 11 šīs Dynamics 365 preces netiks atbalstītas. |
| **Vai ir aizstāts ar citu līdzekli?**   | Mēs rekomendējam, lai klienti pāriet uz Microsoft Edge.|
| **Ietekmētie produkta apgabali**         | Visas Dynamics 365 preces |
| **Izvietošanas iespēja**              | Visu|
| **Statuss**                         | Novecojis. Internet Explorer 11 netiks atbalstīts pēc 2021. gada augusta.|


### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Visual Studio pievienojumprogramma, lai lietotu metadatu labojumfailus

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Metadatu labojumfaili vairs netiek atbalstīti ar [One Version](../../fin-ops/get-started/one-version.md) pakalpojuma atjauninājumiem, kas tika ieviesti 2018. jūlijā ar versiju 8.1. |
| **Vai ir aizstāts ar citu līdzekli?**   | Atsevišķi metadatu labojumfaili nav pieejami atbalstītajām versijām. Tā vietā tiek piemēroti kumulatīvi kvalitātes atjauninājumi. |
| **Ietekmētie produkta apgabali**         | Visual Studio pievienojumprogrammas |
| **Izvietošanas iespēja**              | Izstrādes virtuālās mašīnas |
| **Statuss**                         | Izmantojot versiju 10.0.15, pievienojumprogramma vairs nav iekļauta Visual Studio rīkos. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmu 10.0.14 versijai

### <a name="online-users-page"></a>Tiešsaistes lietotāju lapa 

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šī ir mantota lapa, kas tika izveidota iepriekšējā klienta/servera arhitektūrai. Informācija šajā lapā ne vienmēr ir precīza, kas var būt mulsinoši un maldinoši. |
| **Vai ir aizstāts ar citu līdzekli?**   | Turpmākajā atjauninājumā tiks nodrošināta jauna lapa.|
| **Ietekmētie produkta apgabali**         | Sistēmas administrēšana |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Līdz 2021. gada oktobrim šī veidlapa tiks noņemta.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmu 10.0.13 versijai


### <a name="custom-code-defined-in-ssrs-report-properties"></a>Pielāgots kods, kas definēts SSRS pārskata rekvizītos 

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Parasti pielāgots kods piedāvā ierobežotas priekšrocības, tajā pašā laikā nodrošina būtisku resursu piešķiršanu un aprēķina atbalstu. Pielāgotu kodu galvenokārt izmanto pārskatu autori, lai izsauktu publiskās metodes no pielāgotas koda komplektācijas. Tomēr mākoņa viesots pakalpojums neatbalsta atsauces uz sistēmas SSRS pārskatus pielāgotajām komplektācijām. |
| **Vai ir aizstāts ar citu līdzekli?**   | Pārskata autori var izvēlēties turpināt atsauces uz publiskajiem .NET API matemātikai, pārveidošanai un formāta operācijām no jebkuras tekstlodziņa izteiksmes. Papildinformāciju skatiet sadaļā [Koda pievienošana pārskatam (SSRS)](https://docs.microsoft.comsql/reporting-services/report-design/add-code-to-a-report-ssrs?view=sql-server-ver15).  |
| **Ietekmētie produkta apgabali**         | To programmas pārskata noformējumu apakškopa, kas definētas RDL, kas satur pielāgotu kodu. |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Izmantojot versiju 10.0.13, kompilators sāks brīdinājuma izdošanu gadījumiem, kad pielāgots kods tiek noteikts SSRS pārskata definīcijā. Lai labotu problēmu, atveriet pārskata noformējuma definīciju un noņemiet visus pielāgotos kodu artefaktus. Šis brīdinājums tiks aizstāts ar kompilatora kļūdu turpmākajā atjauninājumā.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Triju jQuery komponentu bibliotēku jaunināšana 

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Trīs jQuery komponentu bibliotēkas tiek atjauninātas drošības labojumiem un valūtas uzturēšanai.   
| **Vai ir aizstāts ar citu līdzekli?**   | Tiek ietekmētas šādas bibliotēkas: jQuery (uz versiju 3.5.0 no versijas 2.1.4), jQuery UI (uz versiju 1.12.1 no versijas 1.11.4), jQuery qTip (uz versiju 3.0.3 no 2.2.1). Migrācijas vadlīnijas ir nodrošinātas tiešsaistē ar jQuery.  |
| **Ietekmētie produkta apgabali**         | Paplašināmās vadīklas, īpaši pielāgots JavaScript kods, izmantojot novecojušus vai noņemtus API |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Ar versiju 10.0.13/Platformas atjauninājums 37 klienti pēc izvēles var pārvietoties uz jaunākajām bibliotēkām, iespējojot līdzekli "Jaunināt trīs jQuery komponentu bibliotēkas". Pāreja uz jaunajām bibliotēkām būs obligāta ar 2021. gada aprīļa izlaidumu, lai atļautu laiku ietekmēto API migrācijai.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Esošā režģa vadīkla/forceLegacyGrid() API

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Esošā režģa vadīkla tiek aizstāta ar jauno režģa vadīklu. |
| **Vai ir aizstāts ar citu līdzekli?**   | [Jaunā režģa vadīkla](../..//fin-ops/get-started/grid-capabilities.md) |
| **Ietekmētie produkta apgabali**         | Tīmekļa klients |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Versijā 10.0.13 jaunā režģa vadīkla ir vispārēji pieejama, un klienti pēc izvēles var ieslēgt šo līdzekli. Jaunā režģa vadīkla kļūs obligāta 2021. gada oktobra laidienā. Kad jaunā režģa kontrole kļūs obligāta, **forceLegacyGrid()** API vairs netiks uzturēta. |

### <a name="personalization-without-saved-views"></a>Personalizācija bez saglabātajiem skatiem 

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Personalizācijas apakšsistēma ir pārstrādāta ar saglabāto skatījumu līdzekli, lai tā varētu uzlabot veiktspēju un piedāvāt papildu iespējas. |
| **Vai ir aizstāts ar citu līdzekli?**   | Saglabātie skati |
| **Ietekmētie produkta apgabali**         | Tīmekļa klients |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Versijā 10.0.13/Platform atjauninājums 37, ir vispārēji pieejami saglabāto skatījumu līdzekļi, un klienti pēc izvēles var ieslēgt šo līdzekli. Saglabātā skatījuma līdzeklis kļūs obligāts 2021. gada oktobra laidienā. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmu 10.0.12 versijai

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Režģa vai grupas vadīklu veidlapas paplašinājumi, kas satur nederīgas lauku atsauces

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Datu grupas rekvizīts režģī vai grupas vadīklās tiek izmantots, lai automātiski parādītu visus lauku grupas laukus. Režģa vai grupas vadīkla, kas pievienota ar paplašinājumu, var saturēt laukus, kas vairs nav definēti lauku grupā, vai varbūt trūkst lauku grupā definēto lauku. Tas var izraisīt nekonsekventu darbību izpildlaikā. Platformas atjauninājumi Finance and Operations programmu 10.0.12 versija tagad iedala šo problēmu kā kompilatora *brīdinājumu*. Lai labotu šo problēmu, atveriet veidlapas paplašinājumu un saglabājiet to.
| **Vai ir aizstāts ar citu līdzekli?**   | Šis kompilatora brīdinājums tiks aizstāts ar kompilatora kļūdu turpmākajā atjauninājumā. |
| **Ietekmētie produkta apgabali**         | Visual Studio izstrādes rīki |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Kompilatora brīdinājums ir ieviests platformas atjauninājumos Finance and Operations programmu 10.0.12 versijā. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Platformas atjauninājumi Finance and Operations programmu 10.0.11 versijai

### <a name="explicit-safe-lists-for-self-service-environments"></a>Precīzi drošie saraksti pašapkalpošanās videi

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Ir mainījies process, kurā IP tiek pārvietoti uz drošajiem sarakstiem. Pašapkalpošanās vairs neatbalsta IP iekļaušanu drošajā sarakstā. |
| **Vai ir aizstāts ar citu līdzekli?**   | Plašāku informāciju skatiet [Konfigurēt Azure Active Directory nosacījuma piekļuvi](https://docs.microsoft.com/appcenter/general/configuring-aad-conditional-access).|
| **Ietekmētie produkta apgabali**         | Drošība |
| **Izvietošanas iespēja**              | Mākonis |
| **Statuss**                         | **Novecojis:** šis līdzeklis ir pilnībā novecojis pašapkalpošanās izvietošanai. |

### <a name="visual-studio-2015"></a>Visual Studio 2015

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Lai atbalstītu jaunākās Visual Studio versijas, ir jāveic dažas izmaiņas X++ paplašinājumos programmai Visual Studio. Šīs izmaiņas nav saderīgas ar Visual Studio 2015. |
| **Vai ir aizstāts ar citu līdzekli?**   | Visual Studio 2017 aizstās Visual Studio 2015 kā izvietotā un nepieciešamā versija. |
| **Ietekmētie produkta apgabali**         | Visual Studio izstrādes rīki |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Virtuālās mašīnas, kas izvietotas versijā 10.0.13 (platformas atjauninājums 37) vai jaunākā versijā, ietver Visual Studio 2017. Versija 10.0.16 (platformas atjauninājums 40) ir galīgais laidiens ar Visual Studio 2015 atbalstu. Virtuālās mašīnas, kurām ir tikai Visual Studio 2015, nevarēs veikt jaunināšanu uz versiju 10.0.17 (platformas atjauninājums 41). |

### <a name="field-groups-containing-invalid-field-references"></a>Lauku grupas, kas ietver nederīgas lauku atsauces

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Tabulas metadatu definīcijās lauku grupas var ietvert lauku atsauces, kas nav derīgas. Ja šīs lauku grupas ir izvietotas, tās var izraisīt izpildlaika kļūmes modulī Financial Reporting un Microsoft SQL Server pārskatu izveides pakalpojumos (SSRS). Platformas atjauninājums 23 ieviesa kompilatora *brīdinājumu*, kas ļāva risināt šo metadatu problēmu. Platformas atjauninājumi Finance and Operations programmu 10.0.11 versija iedala šo problēmu kā kompilatora *kļūdu*.<p>Lai novērstu šo problēmu, izpildiet sekojošās darbības.</p><ol><li>Noņemiet nederīgo lauka atsauci no tabulas lauku grupas definīcijas.</li><li>Pārkompilēt.</li><li>Pārliecinieties, vai kļūdas ir novērstas.</li></ol> |
| **Vai ir aizstāts ar citu līdzekli?**   | Šī kompilatora kļūda neatgriezeniski aizstāj kompilatora brīdinājumu.  |
| **Ietekmētie produkta apgabali**         | Visual Studio izstrādes rīki |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | **Novecojis:** kompilatora brīdinājums ir kompilatora kļūda platformas atjauninājumiem Finance and Operations programmu 10.0.11 versijā. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>ISV licences, kas izveidotas, izmantojot SHA1 hashing algoritmu

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Neatkarīgu programmatūras piegādātāju (ISV) licenču izveides process ir mainījies. Lai iegūtu papildinformāciju, skatiet [Neatkarīga programmatūras izstrādātāja (ISV) licencēšana](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā. Izmantojiet programmu Windows PowerShell, lai izveidotu licences. |
| **Ietekmētie produkta apgabali**         | Visual Studio izstrādes rīki |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | <strong>Novecojis:</strong> ISV licences, kas izveidotas, izmantojot SHA1 jaukšanas algoritmu. Šis algoritms ir atkarīgs no sertifikātiem, kas tika izveidoti, izmantojot utilītu MakeCert, un šī utilīta ir novecojusi.<p><strong>Novecojusi:</strong> SHA1 izmantošana drošības vai jaukšanas nolūkiem. SHA1 vairs nedarbosies 2021. gada sākumā. Tāpēc tas vairs nav jālieto.<p><strong>Noņemts:</strong> atbalsts transporta slāņa drošībai (TLS) 1.0 un TLS 1.1 ienākošajiem vai izejošajiem pieprasījumiem. |

## <a name="platform-update-32"></a>Platformas update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Darbplūsmas pieprasījuma maiņas dialoglodziņā vairs nav lietotāja atlases nolaižamā saraksta
|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Tas bija drošības jautājums, jo izmaiņu pieprasījums var tikt nosūtīts neparedzētam lietotājam. Tas bija arī lietojamības jautājums, jo tas lika lietotājam noteikt, kas bijis darbplūsmas iniciators un viņu manuāli atlasīt.  |
| **Vai ir aizstāts ar citu līdzekli?**   | Nē |
| **Ietekmētie produkta apgabali**         | Darbplūsma |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Lietotāja atlases nolaižamais saraksts tika noņemts no izmaiņu pieprasīšanas dialoglodziņa Platform atjauninājumā 32. Pieprasījuma izmaiņu pieprasījumi automātiski tiks nosūtīti iniciatoram, kā paredzēts. Plašāku informāciju par šo funkcionalitāti skatiet [Darbības darbplūsmas apstiprināšanas procesos](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Iegultās detalizētās saites vairs netiek atbalstītas numurētos dokumentos, ko sniedz mākoņa balstītais pakalpojums 
|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Pakalpojuma sniegto dokumentu iegultās navigācijas URL var saturēt sensitīvus biznesa datus. Mēs noņemam atbalstu iegultām urbšanas saitēm dokumentos kā drošības piesardzības līdzekli, lai turpmāk aizsargātu klienta datus. Lietotāji arī gūs labumu no uzlabotas veiktspējas, vienlaikus interaktīvi veidojot dokumentus šo izmaiņu dēļ.  |
| **Vai ir aizstāts ar citu līdzekli?**   | Nr. |
| **Ietekmētie produkta apgabali**         | Pārskatu veidošana |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Šis līdzeklis tiek noņemts no pakalpojuma.<br><br>Mūsdienu klients piedāvā daudzas opcijas tādu skatu izveidei, kas ietver automātiski ģenerētās saites, lai palīdzētu programmas pārskatīšanai. Ar pakalpojumu sniegtie, numurētie dokumenti ir ieteicami ārējiem sakariem, kas tiek sūtīti pa e-pastu, arhivēti un izdrukāti adresātiem. Mēs esam uzlabojuši pieredzi dokumentu priekšskatīšanai tieši pārlūkprogrammā, kas piedāvā tiešu piekļuvi lokālajiem printeriem. Papildinformāciju skatiet šeit [PDF dokumentu priekšskatījums ar iegultu skatītāju](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Iepriekšēji paziņojumi par noņemtiem vai novecojušiem līdzekļiem
Lai uzzinātu vairāk par līdzekļiem, kas iepriekšējos laidienos ir noņemti vai novecojuši, skatiet [Noņemti vai novecojuši līdzekļi iepriekšējos laidienos](../migration-upgrade/deprecated-features.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
