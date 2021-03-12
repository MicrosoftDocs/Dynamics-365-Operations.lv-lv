---
title: Debitoru portāla Dynamics 365 Supply Chain Management pārskats
description: Šī tēma iepazīstina ar Debitoru portālu un izskaidro, kam tas ir jāizmanto un kā tas darbojas.
author: dasani-madipalli
manager: tfehr
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 25b1962af182fc2749fcd6ec0035613d8365deb1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980810"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>Debitoru portāla Dynamics 365 Supply Chain Management pārskats

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="what-is-the-customer-portal"></a>Kas ir Debitoru portāls?

Mūsdienīgas piegādes ķēžu sistēmas balstās uz integrāciju. Tās prasa, lai krājumi, debitoru pieprasījums un pārdošanas nodaļas tiktu integrēti, nevis atrastos atsevišķos silosos. Debitoru portāls palīdz uzņēmumiem, kas lieto Microsoft Dynamics 365 Supply Chain Management, uzlabot šo integrāciju un efektīvāk uzturēt klientu informētību.

Debitoru portāls ir [Power Apps portāls](https://docs.microsoft.com/powerapps/maker/portals/overview), kas ļauj uzņēmumiem izveidot ārēju no uzņēmuma uzņēmumam (B2B) tīmekļa vietni scenārijiem, kas saistīti ar pārdošanas pasūtījumu apstrādi. Veidne izmanto [duālais ieraksts](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), Supply Chain Management un Power Apps portālus, lai ļautu ārējiem uzņēmuma klientiem skatīt un izveidot datus no uzņēmuma Dynamics 365 vides.

Debitoru portāla veidnei ir visas pielāgošanas iespējas, ko piedāvā portāla Power Apps līdzekļi. Veidni var viegli mainīt, lai attēlotu uzņēmuma zīmolu, pievienotu palielinātu funkcionalitāti un mainītu lietotāja pieredzi. Visu funkcionalitāti, ko veidnes piedāvā standartā, var modificēt pēc vajadzības.

> [!IMPORTANT]
> Nevar gaidīt, lai pati veidne būtu pilnībā funkcionāla. Tas darbojas tikai kā veicinātājs debitoriem, kuri vēlas izveidot ārēji vērstu tīmekļa vietni, lai uzņēmuma klienti varētu sadarboties ar Supply Chain Management datiem.

> [!NOTE]
> Debitora portāla dokumentācija ir vērsta uz administratoriem, pielāgotājiem un sistēmu integrētājiem, kas iestatīt Debitoru portālu Supply Chain Management instalēšanai. Tā izmanto terminus _debitors_ un _lietotājs_, lai aprakstītu cilvēkus, kuri ir organizācijas klienti, kas lieto Supply Chain Management un kas izmantos galīgo portālu.

## <a name="video"></a>Video

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

[Klienta portāla veidnes apskats Dynamics 365 Supply Chain Management](https://youtu.be/nPrqoLuHfV8) video (parādīts iepriekš) ir iekļauts [Finance and Operations atskaņošanas sarakstā](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), kas pieejams YouTube.

## <a name="who-should-use-it"></a>Kam tas ir jāizmanto?

Debitoru portāls ir paredzēts uzņēmumiem, kas lieto Supply Chain Management un kas ir tālāk minētās īpašības.

- Tie vēlas izveidot ārēji vērstu tīmekļa vietni, kas komunicē pasūtījumu apstrādes informāciju (piemēram, pasūtījuma statusu vai konta informāciju) tieši no sistēmas Supply Chain Management saviem uzņēmuma klientiem.
- Tie pāriet no Dynamics AX 2012 uz Supply Chain Management, un iepriekš izmantoja [AX 2012 Klientu pašapkalpošanās portālu](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).

Tālāk minētie organizāciju veidi **nav** labi kandidāti Debitoru portāla ieviešanai.

- Uzņēmumi, kas vēlas izveidot tīmekļa vietni klientiem, kas nav uzņēmuma klienti. Šiem uzņēmumiem būtu jāapsver [Dynamics 365 Commerce e-komercijas vietnes izveide](https://docs.microsoft.com/dynamics365/commerce/create-ecommerce-site).
- Uzņēmumi, kas jau izmanto esošu Power Apps portālu tīmekļa vietni līdzīgam mērķim. Šie uzņēmumi nesaņems nekādu papildu labumu no Debitoru portāla. Debitoru portāls tiek piegādāts kā veidne, kas darbojas kā ceļvedis un sākumpunkts debitoriem, kuri vēlas "savienot punktus" starp dubulto ierakstu, Supply Chain Management un Power Apps portāliem. Ja esat jau iestatījis tīmekļa vietni, kas kalpo šim mērķim, jūs nevarēsit iegūt lielu vērtību no Debitoru portāla veidnes izmantošanas šīs tīmekļa vietnes atkārtotai nodrošināšanai.

## <a name="how-does-it-work"></a>Kā tas notiek?

Debitoru portāls tiek nodrošināts kā Power Apps portālu veidne. Tas ir atkarīgs no Power Apps portāliem un duālā ieraksta.

[Power Apps portāli](https://docs.microsoft.com/powerapps/maker/portals/overview) ir līdzeklis, kas ļauj lietotājiem izveidot ārēji vērstu tīmekļa vietni, kurā var pierakstīties cilvēki, kas nav organizācijas locekļi. Lai izveidotu portālus, ir nepieciešama neliela kodēšana vai tā nav vajadzīga vispār. Debitoru portāls ir viena no daudzām [Dynamics 365 portāla veidnēm](https://docs.microsoft.com/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365), kas pieejamas no Microsoft.

[Duālais ieraksts](https://docs.microsoft.com/powerapps/maker/portals/overview) ir standarta infrastruktūras produkts, kas nodrošina gandrīz reāllaika mijiedarbību starp Customer Engagement programmām un Finance and Operations programmām. Duālais ieraksts nodrošina divvirzienu integrāciju starp Finance and Operations programmām un Microsoft Dataverse. Tāpēc tas nodrošina integrētu lietotāja pieredzi programmās. Debitora portāls ir atkarīgs no tabulām, kas tiek sinhronizētas ar duālo ierakstu. Pirms Supply Chain Management datus var sakārtoti Debitoru portālā, ir jāiespējo duālais ieraksts visām atbilstošajām tabulām.

![Debitoru portāla atkarības](media/customer-portal-elements.png "Debitoru portāla atkarības")

Debitoru portāls darbojas kā sākumpunkts organizācijām, kas vēlas izmantot Power Apps portālus, lai izveidotu ārēji vērstu tīmekļa vietni, kura izmanto datus no to Supply Chain Management instalācijas. Tas palīdz organizācijām savienot duālo ierakstu, Supply Chain Management un Power Apps portālus.
