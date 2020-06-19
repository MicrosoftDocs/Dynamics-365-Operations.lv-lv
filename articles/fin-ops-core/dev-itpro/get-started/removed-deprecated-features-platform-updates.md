---
title: Noņemtie vai novecojušie platformas līdzekļi
description: Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Finance and Operations programmu platformu atjauninājumiem.
author: sericks007
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 6fc699907d30fff2d05e752ea055cae8d1134d9b
ms.sourcegitcommit: 3eaa71c889545318737b3bc88b05eae1a47ad2c0
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/05/2020
ms.locfileid: "3433926"
---
# <a name="removed-or-deprecated-platform-features"></a>Noņemtie vai novecojušie platformas līdzekļi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti līdzekļi, kuri ir noņemti vai kurus ir paredzēts noņemt no Finance and Operations programmu platformu atjauninājumiem.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši. 

> [!NOTE]
> Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.

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

### <a name="explicit-whitelisting-for-self-service-environments"></a>Skaidra iekļaušana baltajā sarakstā pašapkalpošanās vidēm

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | IP iekļaušanas baltajā sarakstā process ir mainījies. Pašapkalpošanās vairs neatbalsta IP iekļaušanu baltajā sarakstā. |
| **Vai ir aizstāts ar citu līdzekli?**   | Plašāku informāciju skatiet [Azure Active Directory nosacījuma piekļuves konfigurēšana](https://docs.microsoft.com/appcenter/general/configuring-aad-conditional-access).|
| **Ietekmētie produkta apgabali**         | Drošība |
| **Izvietošanas iespēja**              | Mākonis |
| **Statuss**                         | **Novecojis:** šis līdzeklis ir pilnībā novecojis pašapkalpošanās izvietošanai. |

### <a name="visual-studio-2015"></a>Visual Studio2015

|   |  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Lai atbalstītu jaunākās Visual Studio versijas, ir jāveic dažas izmaiņas X++ paplašinājumos programmai Visual Studio. Šīs izmaiņas nav saderīgas ar Visual Studio 2015. |
| **Vai ir aizstāts ar citu līdzekli?**   | Visual Studio 2017 aizstās Visual Studio 2015 kā izvietotā un nepieciešamā versija. |
| **Ietekmētie produkta apgabali**         | Visual Studio izstrādes rīki |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Kad tiks paziņota jaunu virtuālo mašīnu (VM) ar Visual Studio 2017 pieejamība, esošās VM, kurās ir tikai Visual Studio 2015, būs atkārtoti jāizvieto ar 2021. gada 1. laidiena vilni. |

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

