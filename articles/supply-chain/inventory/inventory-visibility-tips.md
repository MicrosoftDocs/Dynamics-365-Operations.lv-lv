---
title: Krājumu redzamības padomi
description: Šajā rakstā ir sniegti daži padomi, kas jums jāapsver, kad iestatāt un izmantojat krājumu redzamības pievienojumprogrammu.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3bdd161815a15d5c39b3c0afc176a288c8d9055a
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306091"
---
# <a name="inventory-visibility-tips"></a>Krājumu redzamības padomi

[!include [banner](../includes/banner.md)]

Šeit sniegti daži padomi, kas jāievēro, iestatot un lietojot pievienojumprogrammu Krājumu redzamība:

- Pašlaik krājumu redzamības pievienojumprogramma atbalsta tikai Microsoft Dataverse vides, kas izveidotas, izmantojot Microsoft Dynamics lifecycle Services (LCS). Dataverse Ja vide tika izveidota citādi (piemēram, Power Apps izmantojot administrēšanas centru) un ja tā ir saistīta ar vidi, vispirms jālūdz krājumu redzamības Dynamics 365 Supply Chain Management produktu komandai labot kartēšanas problēmu. Varat sazināties ar darba grupu inventvisibilitysupp@microsoft.com [...](mailto:inventvisibilitysupp@microsoft.com). Komanda ļaus jums zināt, kad jūsu vide ir gatava instalēt Krājumu redzamību.
- Ja ir vairāk nekā viena LCS vide, izveidojiet atšķirīgu Azure Active Directory (Azure AD) programmu katrai videi. Ja lietojat vienu lietojumprogrammas ID un nomnieka ID, lai instalētu Inventory Visibility lietojumprogrammu atšķirīgām vidēm, vecākām vidēm tiks rādīta marķiera problēma. Ir derīga tikai pēdējā instalētā krājumu redzamības pievienojumprogrammas instance.
- Mākonī viesotajām vidēm krājumu redzamība pašlaik netiek atbalstīta. Tas tiek atbalstīts tikai pakāpju-2+ vidēm.
- Programmas programmēšanas interfeiss (API) pašlaik atbalsta vaicājumus līdz 100 atsevišķiem krājumiem pēc `ProductID` vērtības. Katrs `SiteID` vaicājumā `LocationID` var norādīt vairākas vērtības. Maksimālais ierobežojums ir definēts kā `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- Lielapjoma API var atgriezt maksimāli 512 ierakstus katram pieprasījumam.
- Datu `fno` avots ir rezervēts Piegādes ķēžu pārvaldībai. Ja krājumu redzamības pievienojumprogramma ir integrēta Piegādes ķēdes pārvaldības vidē, mēs iesakām nedzēšam konfigurācijas, kas saistītas `fno` ar [datu avotu](inventory-visibility-configuration.md#data-source-configuration).
- Krājumu redzamību nevar mainīt datu avota `fno` datus. Datu plūsma ir vienvirziena, kas nozīmē, ka `fno` visām daudzuma izmaiņām datu avotam ir jābūt no jūsu Piegādes ķēžu pārvaldības vides. Tādēļ jūs nevarat izmantot API, lai nosūtītu rīcībā esošos izmaiņu vai rezervēšanas pieprasījumus datu `fno` avotam.
- Ja pievienosiet vienu vai vairākus jaunus pasākumus jūsu Piegādes ķēdes pārvaldības videi, jums tie jāpievieno arī krājumu redzamībai. Tomēr visām daudzuma izmaiņām jaunam daudzumam ir jābūt no Jūsu Piegādes ķēdes pārvaldības vides.
- Nodalījuma [konfigurācija pašlaik](inventory-visibility-configuration.md#partition-configuration) sastāv no divām pamatdimensijām (`SiteId` un `LocationId`), kas norāda, kā dati tiek sadalīti. Operācijas vienā un tajā pašā nodalījumā var piegādāt lielāku veiktspēju par zemākām izmaksām. Risinājums ietver šo nodalījuma konfigurāciju pēc noklusējuma. *Tādēļ jums tas nav jādefinē pats*. Ne pielāgojiet noklusējuma nodalījuma konfigurāciju. Ja to dzēšat vai maināt, iespējams, radusies negaidīta kļūda.
- Pamatdimensijas, kas ir definētas nodalījuma konfigurācijā, nav jādefinē preču [indeksa hierarhijas konfigurācijā](inventory-visibility-configuration.md#index-configuration).
- Preces [indeksa hierarhijas](inventory-visibility-configuration.md#index-configuration) konfigurācijā jābūt iekļautai vismaz vienai indeksu hierarhijai (piemēram, `Empty` satur pamatdimensiju), pretējā gadījumā vaicājumiem neizdosies kļūda "Nav iestatīta indeksu hierarhija."
- Datu avots `@iv` ir iepriekš definēts datu avots un ar prefiksu definētie fiziskie `@iv` pasākumi ir `@` iepriekš definētie pasākumi. Šie pasākumi ir iepriekš definēta sadalījuma funkcijas konfigurācija, tāpēc tie nav jāmaina vai jādzēš, vai, lietojot sadalījuma līdzekli, rodas neparedzētas kļūdas.
- Iepriekš definētajam aprēķinātajam mēram var pievienot jaunus fiziskos `@iv.@available_to_allocate` mērus, bet nosaukumu nedrīkst mainīt.
- Ja atjaunojat Piegādes ķēdes pārvaldības datu bāzi, tad atjaunotā datu bāze var saturēt datus, kas vairs neatbilst datiem, kas iepriekš nav sinhronizēti, izmantojot krājumu redzamību.Dataverse Šī datu neatbilstība var izraisīt sistēmas kļūdas un citas problēmas. Tādēļ ir svarīgi vienmēr iztīrīt visus saistītos krājumu redzamības datus no Dataverse pirms Piegādes ķēžu pārvaldības datu bāzes atjaunošanas. Papildinformāciju skatiet [tīrīšanas krājumu redzamības datos Dataverse pirms piegādes ķēdes pārvaldības datu bāzes atjaunošanas](inventory-visibility-setup.md#restore-environment-database).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
