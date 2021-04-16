---
title: Krājuma bloķēšanas izveide un uzturēšana
description: Šajā procedūrā parādīts, kā citos izejošos pirmdokumentos neļaut rezervēt fiziski rīcībā esošus krājumus, izmantojot krājumu aizturēšanu.
author: perlynne
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 319ae6da1e0e504316b2d96001d582e835cef20c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834005"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Krājuma bloķēšanas izveide un uzturēšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā citos izejošos pirmdokumentos neļaut rezervēt fiziski rīcībā esošus krājumus, izmantojot krājumu aizturēšanu. Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF, izmantojot piemēra vērtības. Pirms šīs procedūras uzsākšanas, jums ir jābūt pieejamiem fiziski rīcībā esošiem krājumiem.


## <a name="create-an-inventory-blocking"></a>Krājumu bloķēšanas izveide
1. **Navigācijas rūtī** ejiet uz **Moduļi > Krājumu pārvaldība > Periodiskie uzdevumi > Krājumu bloķēšana**.
2. Klikšķiniet **Jauns**.
3. Laukā **Krājuma kods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā atlasiet krājumu, kuru vēlaties izmantot. Atlasiet krājuma numuru no fiziski rīcībā esošiem krājumiem, kuru vēlaties bloķēt. Ja izmantojat USMF, varat atlasīt krājumu M9201.  
5. Laukā **Daudzums** ierakstiet kādu skaitli. Ja lietojat krājumu M9201, ir jāatlasa mazāk par 200 vienībām.
6. Izvērsiet kopsavilkuma cilni **Krājumu izmēri**.
7. Laukā **Noliktava** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.
8. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Ja izmantojat krājumu M9201, varat atlasīt 51. noliktavu.  
9. Noklikšķiniet uz **Saglabāt**.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Krājumu bloķēšanas nosacījumu atjaunināšana
1. Kopsavilkuma cilnē **Vispārīgi** laukā **Daudzums** ievadiet skaitli. Atjauniniet krājumu daudzuma lauku, lai atspoguļotu bloķējamo daudzumu.  
2. Laukā **Paredzamais datums** ievadiet datumu. Varat norādīt, kad bloķētie krājumi varētu kļūt pieejami rezervācijai, norādot paredzamo datumu. Ja krājumu bloķēšanai ir atlasīta opcija Paredzamā saņemšana, kā tas ir pēc noklusējuma, manuāli izveidojot bloķēšanas pavēli, šis datums tiks attēlots paredzamajā transakcijā.  
3. Noklikšķiniet uz **Saglabāt**.

## <a name="remove-the-inventory-blocking"></a>Krājuma bloķēšanas noņemšana
1. **Darbību rūtī** noklikšķiniet uz **Dzēst**.
2. Noklikšķiniet uz pogas **Jā**.
3. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]