---
title: Vērtējumu un atsauksmju pārvaldība
description: Šajā tēmā ir paskaidrots, kā pārvaldīt vērtējumus un atsauksmes Microsoft Dynamics 365 Commerce vietņu veidotājā.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fc88bc5a5868dce7c0539bf3f0ddc5b751e7b75
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414072"
---
# <a name="manage-ratings-and-reviews"></a>Vērtējumu un atsauksmju pārvaldība

[!include [banner](includes/banner.md)]

Šajā tēmā ir paskaidrots, kā pārvaldīt vērtējumus un atsauksmes Microsoft Dynamics 365 Commerce vietņu veidotājā.

## <a name="overview"></a>Pārskats

Dynamics 365 Commerce izmanto Microsoft Azure Cognitive Service, lai automātiski moderētu apskata tekstu, rediģējot nepiedienīgos vārdus. Turklāt moderatori var izmantot Dynamics 365 Commerce vietņu veidotāju, lai ieviestu šādus manuālus uzdevumus:

- Moderēt apskatus, atbildot uz tiem vai noņemot tos.
- Dzēst klienta apskatu pēc klienta pieprasījuma.
- Importēt visu preču vērtējumu un apskatu datus lielā apjomā Microsoft Power BI veidnē, lai varētu analizēt vērtējumu un apskatu tendences.

## <a name="read-a-review"></a>Apskata lasīšana 

Lai lasītu atsauksmi Commerce vietņu veidotājā, veiciet tālāk norādītās darbības.

1. Dodieties uz **Sākums \> Apskati \> Moderēšana**.
1. Lai filtrētu apskatus, kas tiek parādīti pēc preces ID, preces nosaukuma vai apskata teksta, izmantojiet meklēšanas lauku lapas augšējā labajā stūrī.

Papildu filtri ļauj ierobežot apskatus pēc perioda, vērtējuma, kanāla vai svarīguma statusa (noņemts, atbildēts vai ziņots).

![Moderēšanas sākumlapa](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a>Atbildēšana uz apskatu 

Dažkārt klienti, kuri iegādājušies preci, izsaka savu apmierinātību vai neapmierinātību vai nesaprot, kā izmantot preci. Kā moderators varat ievietot atbildi uz apskatu. Šī atbilde parādīsies vietnē kopā ar apskatu. 

Lai atbildētu uz atsauksmi Commerce vietņu veidotājā, veiciet tālāk norādītās darbības.

1. Dodieties uz **Sākums \> Apskati \> Moderēšana**.
1. Atrodiet un atlasiet apskatu, kam nepieciešama atbilde.
1. Rekvizītu rūts labajā pusē atlasiet **Pievienot atbildi**.
1. Ievadiet atbildes tekstu un parādāmo atbildētāja vārdu. Noklusējuma atbildētāja vārds ir **Moderators**.
1. Pēc pabeigšanas atlasiet **Ievietot atbildi**.

![Atbildēšana uz apskatu](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a>Apskata noņemšana 

Dažreiz moderatoriem ir biznesa pamatojums, lai noņemtu klienta apskatus. 

Lai noņemtu atsauksmi Commerce vietņu veidotājā, veiciet tālāk norādītās darbības.

1. Dodieties uz **Sākums \> Apskati \> Moderēšana**.
1. Atrodiet un atlasiet apskatu, kas jānoņem.
1. Labajā pusē rekvizītu rūtī atlasiet noņemšanas iemeslu sadaļā **Noņemt atsauksmi** un tad atlasiet **Noņemt**.
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a>Klienta apskata dzēšana pēc klienta pieprasījuma 

Dažkārt klienti vēlas, lai viņu vērtējumu un apskatu dati tiktu neatgriezeniski dzēsti no e-tirdzniecības vietnes. Moderators, kas saņem noņemšanas pieprasījumu no klienta, var noņemt klienta datus, izmantojot apstatu dzēšanas līdzekli. Lai atrastu un dzēstu klienta datus, moderatoram ir nepieciešama e-pasta adrese, ko klients izmantojis, lai pierakstītos un sniegtu apskatus. 

Lai atrastu un dzēstu klienta datus Commerce vietņu veidotājā, rīkojieties šādi.

1. Dodieties uz **Sākums \> Apskati \> Dzēst**.
1. Lodziņā **Meklēt lietotājus pēc e-pasta adreses** ievadiet klienta e-pasta adresi un pēc tam atlasiet **Meklēt**.
1. Ja klients veicis kādas apskatīšanas aktivitātes (piemēram, iesniedzis apskatus, balsojis par cita klienta apskatu noderīgumu vai komentējis cita klienta apskatu), tiek parādīti rezultāti. Katram elementam ir poga **Dzēst**.
1. Katram elementam, kas jāizdzēš, atlasiet **Dzēst**. Kad tiek pieprasīts apstiprinājums, atlasiet **Jā**. 
    
![Klienta datu dzēšana](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - Var paiet līdz septiņām dienām, lai dati tiktu pilnībā noņemti no sistēmas. Moderatoriem jāpaziņo klientiem par šo kavēšanos.
> - Ja klienti ir mainījuši savu vārdu konta iestatījumos, meklēšanas rezultātos var parādīties vairāki elementi. Šādā gadījumā, lai pilnībā dzēstu klienta datus, moderatoram katram elementam jāatlasa **Dzēst**. 

## <a name="download-ratings-and-reviews-data"></a>Vērtējumu un apskatu datu lejupielāde

Commerce vietņu veidotājs ļauj moderatoriem importēt vērtējumu un atsauksmju datus lielapjomā, lai varētu analizēt tendences. Ir pieejama Power BI veidne, kas ietver pamata rādītājus. Moderatori var izmantot šo veidni, lai savienotu lielā apjomā importētos datus un skatītu informācijas paneli. Viņiem nav jāizveido pielāgots informācijas panelis. Moderatori var arī pielāgot Power BI veidni, lai tā atbilstu viņu īpašajām vajadzībām. 

Lai lejupielādētu vērtējumu un atsauksmju datus Commerce vietņu veidotājā, rīkojieties šādi.

1. Dodieties uz **Sākums \> Apskati \> Ziņošana**.
1. Atlasiet **Lejupielādēt atsauksmju datus**, lai lejupielādētu vērtējumu un atsauksmju datus lielapjomā ar komatiem atdalītu vērtību (CSV) formātā.

## <a name="view-ratings-and-reviews-trends"></a>Vērtējumu un apskatu tendenču skatīšana

Moderatori var lejupielādēt Power BI veidni, lai varētu skatīt tendences informācijas panelī.

Lai skatītu vērtējumu un atsauksmju tendences Commerce vietņu veidotājā, rīkojieties šādi.

1. Dodieties uz **Sākums \> Apskati \> Ziņošana**.
1. Atlasiet **PowerBI veidne**, lai lejupielādētu veidni.

    ![Lejupielādējiet Power BI veidni](media/rnr-moderation-reports.png) 

1. Atveriet lejupielādēto veidni, izmantojot Power BI programmu. Aizveriet parādījušos dialoglodziņu **Piekļuve tīmekļa saturam** un pēc tam aizveriet parādījušos "Atsvaidzināt" kļūdas ziņojumu.
1. Dodieties uz **Sākums**, atlasiet **Rediģēt vaicājumus** un pēc tam atlasiet **Datu avota iestatījumi**.
1. Dialoglodziņā **Datu avota iestatījumi** atlasiet **Mainīt avotu**.
1. Laukā **URL** ievadiet ceļu uz apskatu datiem, ko lejupielādējāt iepriekšējā procedūrā (piemēram, **c:\\reviews\\ReviewsData.csv**).

    ![URL lauks ar komatu atdalīto vērtību dialoglodziņā](media/rnr-powerbi-datasource-settings.png) 

1. Atlasiet **Labi** un pēc tam atlasiet **Piemērot izmaiņas**. Lai datu avotam tiktu piemērotas izmaiņas, būs nepieciešamas vienas līdz divas minūtes.
1. Atlasiet **Tendenču loksne**, lai skatītu vērtējumu un apskatu tendences.

    ![Vērtējumu un apskatu tendences](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a>Papildu resursi

[Vērtējumu un atsauksmju apskats](ratings-reviews-overview.md)

[Piekrišana izmantot vērtējumus un atsauksmes](opt-in-ratings-reviews.md)

[Vērtējumu un atsauksmju konfigurēšana](configure-ratings-reviews.md)

[Preču vērtējumu sinhronizācija Dynamics 365 Retail](sync-product-ratings.md)
