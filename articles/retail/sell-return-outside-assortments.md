---
title: Veikala preču klāstā neietvertu preču pārdošana un atgriešana
description: Izmantojot programmu Dynamics 365 for Retail, varat pārdot un atgriezt preces, kas nav ietvertas preču klāstos.
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 653a388de1a972fae488abd81f349d1b138fc716
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "352302"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a>Veikala preču klāstā neietvertu preču pārdošana un atgriešana

[!include [banner](includes/banner.md)]

Bieži izmantots scenārijs visiem mazumtirgotājiem ir preču pārdošana saviem klientiem vai atgriezto preču pieņemšana no tiem, pat ja konkrētās preces nav pieejamas veikalā (citiem vārdiem sakot, preces nav veikala sortimentā).

Tālāk uzskaitīti daži tipiski scenāriji.

+ Mazumtirgotājam nav jānodrošina visu savu preču pieejamība konkrētā veikalā. Pārējās preces tiek glabātas noliktavā. Veikala darbinieks var palīdzēt klientam meklēt vai pārlūkot preces noliktavā, pievienot tās grozam un veikt norēķināšanos, izvēloties piegādes metodi, piemēram, piegādi uz adresi no noliktavas, vai arī klients preci var saņemt pašreizējā vai citā veikalā.
+ Mazumtirgotājam nav jānodrošina konkrētu preču pieejamība veikalā, kuru klients apmeklē, ja preces ir pieejamas citos veikalos. Veikala darbinieks var palīdzēt klientam meklēt vai pārlūkot preces citā veikalā, pievienot tās grozam un veikt norēķināšanos, izvēloties piegādes metodi.
+ Mazumtirgotājam ir vairāki veikali noteiktā pilsētā un tās tuvumā vai pasta indeksa teritorijā, un mazumtirgotājs nevēlas likt klientiem atgriezt preces tajā pašā veikalā, kurā tās iegādājās. Tā vietā klienti var atgriezt preces jebkurā veikalā.

Šie izplatītie scenāriji ir pieejami mazumtirgotājiem, kuri izmanto programmu Dynamics 365 for Retail. Izmantojot Retail, var veikt šādas darbības:

+ meklēt vai pārlūkot preces citos veikalos;
+ meklēt vai pārlūkot visas izlaistās preces;
+ izveidot “pārdošana skaidrā naudā bez piegādes” transakcijas vai klientu pasūtījumus;
+ atlasīt piegādes opcijas klientu pasūtījumiem;
+ izsniegt preces pašreizējā vai citā veikalā;
+ atcelt pasūtījumu pašreizējā vai citā veikalā;
+ atgriezt pasūtījumu ar vai bez čeka (kvīts) pašreizējā vai citā veikalā.
