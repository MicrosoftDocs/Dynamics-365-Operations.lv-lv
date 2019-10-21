---
title: Veikala preču klāstā neietvertu preču pārdošana un atgriešana
description: Izmantojot programmu Dynamics 365 Retail, varat pārdot un atgriezt preces, kas nav ietvertas preču klāstos.
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
ms.openlocfilehash: ae6bac983ddb4d4a217fe83c8f68c5a87ccd6a47
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024941"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a>Veikala preču klāstā neietvertu preču pārdošana un atgriešana

[!include [banner](includes/banner.md)]

Bieži izmantots scenārijs visiem mazumtirgotājiem ir preču pārdošana saviem klientiem vai atgriezto preču pieņemšana no tiem, pat ja konkrētās preces nav pieejamas veikalā (citiem vārdiem sakot, preces nav veikala sortimentā).

Tālāk uzskaitīti daži tipiski scenāriji.

+ Mazumtirgotājam nav jānodrošina visu savu preču pieejamība konkrētā veikalā. Pārējās preces tiek glabātas noliktavā. Veikala darbinieks var palīdzēt klientam meklēt vai pārlūkot preces noliktavā, pievienot tās grozam un veikt norēķināšanos, izvēloties piegādes metodi, piemēram, piegādi uz adresi no noliktavas, vai arī klients preci var saņemt pašreizējā vai citā veikalā.
+ Mazumtirgotājam nav jānodrošina konkrētu preču pieejamība veikalā, kuru klients apmeklē, ja preces ir pieejamas citos veikalos. Veikala darbinieks var palīdzēt klientam meklēt vai pārlūkot preces citā veikalā, pievienot tās grozam un veikt norēķināšanos, izvēloties piegādes metodi.
+ Mazumtirgotājam ir vairāki veikali noteiktā pilsētā un tās tuvumā vai pasta indeksa teritorijā, un mazumtirgotājs nevēlas likt klientiem atgriezt preces tajā pašā veikalā, kurā tās iegādājās. Tā vietā klienti var atgriezt preces jebkurā veikalā.

Šie izplatītie scenāriji ir pieejami mazumtirgotājiem, kuri izmanto programmu Retail. Izmantojot Retail, var veikt šādas darbības:

+ meklēt vai pārlūkot preces citos veikalos;
+ meklēt vai pārlūkot visas izlaistās preces;
+ izveidot “pārdošana skaidrā naudā bez piegādes” transakcijas vai klientu pasūtījumus;
+ atlasīt piegādes opcijas klientu pasūtījumiem;
+ izsniegt preces pašreizējā vai citā veikalā;
+ atcelt pasūtījumu pašreizējā vai citā veikalā;
+ atgriezt pasūtījumu ar vai bez čeka (kvīts) pašreizējā vai citā veikalā.
