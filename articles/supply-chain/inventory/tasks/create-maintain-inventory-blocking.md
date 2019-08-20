---
title: Krājuma bloķēšanas izveide un uzturēšana
description: Šajā procedūrā parādīts, kā citos izejošos pirmdokumentos neļaut rezervēt fiziski rīcībā esošus krājumus, izmantojot krājumu aizturēšanu.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 845d517ad10245df3b208874df61e235c199c7fe
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836409"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Krājuma bloķēšanas izveide un uzturēšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā citos izejošos pirmdokumentos neļaut rezervēt fiziski rīcībā esošus krājumus, izmantojot krājumu aizturēšanu. Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF, izmantojot piemēra vērtības. Pirms šīs procedūras uzsākšanas, jums ir jābūt pieejamiem fiziski rīcībā esošiem krājumiem.


## <a name="create-an-inventory-blocking"></a>Krājumu bloķēšanas izveide
1. Dodieties uz Krājumu vadība > Periodiskie uzdevumi > Krājumu bloķēšana.
2. Noklikšķiniet uz Jauns.
3. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atlasiet krājumu, kuru vēlaties izmantot. 
    * Atlasiet krājuma numuru no fiziski rīcībā esošiem krājumiem, kuru vēlaties bloķēt. Ja izmantojat USMF, varat atlasīt krājumu M9201.  
5. Laukā Daudzums ievadiet skaitli.
    * Ja lietojat krājumu M9201, ir jāatlasa mazāk par 200 vienībām.  
6. Pārslēdziet sadaļas Krājumu dimensijas paplašinājumu.
7. Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
8. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Ja izmantojat krājumu M9201, varat atlasīt 51. noliktavu.  
9. Noklikšķiniet uz Saglabāt.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Krājumu bloķēšanas nosacījumu atjaunināšana
1. Laukā Daudzums ievadiet skaitli.
    * Atjauniniet krājumu daudzuma lauku, lai atspoguļotu bloķējamo daudzumu.  
2. Ievadiet datumu laukā Prognozētais datums.
    * Varat norādīt, kad bloķētie krājumi varētu kļūt pieejami rezervācijai, norādot paredzamo datumu. Ja krājumu bloķēšanai ir atlasīta opcija Paredzamā saņemšana, kā tas ir pēc noklusējuma, manuāli izveidojot bloķēšanas pavēli, šis datums tiks attēlots paredzamajā transakcijā.  
3. Noklikšķiniet uz Saglabāt.

## <a name="remove-the-inventory-blocking"></a>Krājuma bloķēšanas noņemšana
1. Noklikšķiniet uz Dzēst.
2. Noklikšķiniet uz Jā.
3. Aizvērt lapu.

