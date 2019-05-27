---
title: Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana
description: Šajā ierakstā parādīts, kā izveidot atvieglojumu piemērojamības noteikumus un ierobežojumus un pēc tam piešķirt noteikumus atvieglojumiem.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d35266c95cfbf3473a14fec47a1c748229dd25
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510588"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā ierakstā parādīts, kā izveidot atvieglojumu piemērojamības noteikumus un ierobežojumus un pēc tam piešķirt noteikumus atvieglojumiem.  

Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo ierakstu, ir USMF.


## <a name="create-benefit-eligibility-policy-rule-type"></a>Atvieglojumu piemērojamības ierobežojuma nosacījumu tipa izveide
1. Dodieties uz Personāla vadība > Atvieglojumi > Piemērojamība > Atvieglojumu piemērojamības ierobežojumu nosacījumu tipi.
2. Noklikšķiniet uz Jauns.
3. Laukā Kārtulas nosaukums ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Vaicājuma nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Noklikšķiniet uz Saglabāt.
8. Aizvērt lapu.

## <a name="benefit-eligibility-policy"></a>Atvieglojumu piemērojamības ierobežojumi
1. Dodieties uz Personāla vadība > Atvieglojumi > Piemērojamība > Atvieglojumu piemērojamības ierobežojumi.
2. Atlasiet esošu atvieglojumu ierobežojumu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Pārslēdziet sadaļas Politikas organizācijas paplašinājumu.  Šeit varat pievienot vai noņemt jebkuras organizācijas, kuras vēlaties iekļaut politikā.
5. Izvērsiet vai sakļaujiet sadaļu Ierobežojuma nosacījumi.
6. Sarakstā atrodiet iepriekš izveidoto ierobežojuma nosacījumu.
7. Noklikšķiniet uz Izveidot ierobežojuma nosacījumu.
8. Laukā Spēkā stāšanās datums ievadiet datumu, kurā politikai vajadzētu stāties spēkā.
    * Iestatot spēkā stāšanās un beigu datumus, ir iespējams veikt turpmākas ierobežojuma nosacījumu izmaiņas un novērst vajadzību atgriezties pie politikas, lai šīs izmaiņas aktivizētu.  
9. 
    * Piemēram, ja jūs vēlaties, lai kārtula attiecas tikai uz pārdošanas daļu vadītājiem, izveidojiet WHERE klauzulu ar loģiku: kur amata apraksts ir vienāds ar pārdošanas daļas vadītājs.  Vienā kārtulā varat savienot vairākus WHERE nosacījumus, izmantojot AND vai OR.  
10. Noklikšķiniet uz OK.
11. Aizvērt lapu.
12. Aizvērt lapu.

## <a name="assign-rule-to-benefit"></a>Nosacījuma piešķiršana atvieglojumam
1. Pārejiet uz sadaļu Personāla vadība > Atvieglojumi > Atvieglojumi.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Izvērsiet vai sakļaujiet sadaļu Piemērotības noteikumi.
5. Noklikšķiniet uz Rediģēt.
6. Laukā Piemērojamība atlasiet no saraksta Atbilstoši nosacījumiem.
7. Laukā Nosacījuma tips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
8. Sarakstā atrodiet un atlasiet iepriekš izveidoto nosacījumu.
9. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
10. Noklikšķiniet uz Saglabāt.
11. Aizveriet formu.

