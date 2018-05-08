---
title: "Krājumu aizturēšanas izveide un uzturēšana"
description: "Šajā procedūrā parādīts, kā citos izejošos pirmdokumentos neļaut rezervēt fiziski rīcībā esošus krājumus, izmantojot krājumu aizturēšanu."
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7272349cf16b9459823a752b8d3df915f42606ef
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-maintain-inventory-blocking"></a>Krājumu aizturēšanas izveide un uzturēšana

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

