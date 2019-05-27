---
title: Darbinieka reģistrēšana fiksētās atlīdzības plānā
description: Lai pārvaldītu darbinieku pamata algas, atlīdzību un atvieglojumu vadītājs var piešķirt darbiniekus fiksētu atlīdzību plāniem.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee0ba197ee47d2a2da2372b12291e5625ddc9ba1
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510498"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>Darbinieka reģistrēšana fiksētās atlīdzības plānā

[!include [task guide banner](../../includes/task-guide-banner.md)]

Lai pārvaldītu darbinieku pamata algas, atlīdzību un atvieglojumu vadītājs var piešķirt darbiniekus fiksētu atlīdzību plāniem. Šajā procedūrā pieņemts, ka fiksētais plāns ir izveidots un ir aktīvs, un ka plānam ir iestatīti piemērotības nosacījumi. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Lai sāktu procedūru, dodieties uz Personāla vadība > Darbinieki > Darbinieki > Atlīdzība > Fiksēts plāns

1. Noklikšķiniet uz Jauns.
2. Lai aprakstītu darbinieka atlīdzības izmaiņas, laukā Darbība atlasiet Fiksētās kompensācijas darbība ar tipu Pieņemt darbā/atkārtoti pieņemt darbā.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Laukā Amats noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Līmenis, kas tiek parādīts, ir nolasīts no mainīgā Atlīdzības līmenis, kas atbilst pozīcijas darbam. Pirms darbiniekam būs iespējams piešķirt atlīdzību, ir jāiestata uz darbu attiecināmais līmenis.  
6. Laukā Plāns atlasiet darbinieka fiksēto atlīdzības plānu. Plāna meklēšana tiek filtrēta, lai parādītu tikai tos plānus, uz kuriem darbinieks ir tiesīgs, pamatojoties uz iestatījumiem sadaļā Piemērotības noteikumi.
7. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlīdzības efektīvais un termiņa beigu datumi pēc noklusējuma tiek ņemti no darbinieka amata piešķiršanas sākuma un beigu datumiem. Šos datumus varat mainīt pēc vajadzības.  
    * Ja mainīgā Fiksētās atlīdzības plāns vērtība ir soļu plāns, atlasiet soli, kas satur darbiniekam atbilstošu algas likmi. Ja mainīgā Fiksētās atlīdzības plāns vērtība ir pakāpenisks vai indeksēts plāns, atlasiet darbiniekam atbilstošu algas likmi. Algas likme tiks validēta pēc plāna tolerances iestatījumiem, kā arī darba atlīdzības līmeņa minimālo un maksimālo atsauces punktu.  
8. Noklikšķiniet uz OK.

