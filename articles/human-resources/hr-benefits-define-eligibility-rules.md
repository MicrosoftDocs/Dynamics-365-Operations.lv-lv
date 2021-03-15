---
title: Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana
description: Šajā rakstā parādīts, kā izveidot atvieglojumu piemērotības kārtulas un ierobežojumus un pēc tam piešķirt kārtulas atvieglojumiem.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: cc80549eaffa72a22dec51829c86d04a763de96a
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113377"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana

Šajā tēmā parādīts, kā izveidot atvieglojumu piemērotības kārtulas un ierobežojumus un pēc tam piešķirt kārtulas atvieglojumiem.  

## <a name="create-benefit-eligibility-policy-rule-type"></a>Atvieglojumu piemērojamības ierobežojuma nosacījumu tipa izveide

1. Dodieties uz **Personāla vadība > Atvieglojumi > Piemērojamība > Atvieglojumu piemērojamības ierobežojumu nosacījumu tipi**.
2. Atlasiet **Jauns**.
3. Ievadiet vērtību laukā **Nosacījuma nosaukums**.
4. Laukā **Apraksts** ievadiet kādu vērtību.
5. Laukā **Vaicājuma nosaukums** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu.
6. Sarakstā atlasiet saiti atlasītajā rindā.
7. Atlasiet **Saglabāt**.
8. Aizvērt lapu.

## <a name="benefit-eligibility-policy"></a>Atvieglojumu piemērojamības ierobežojumi

1. Dodieties uz **Personāla vadība > Atvieglojumi > Piemērojamība > Atvieglojumu piemērojamības ierobežojumi**.
2. Atlasiet esošu atvieglojumu ierobežojumu.
3. Sarakstā atlasiet saiti atlasītajā rindā.
4. Pārslēdziet sadaļas **Politikas organizācijas** paplašinājumu. Varat pievienot vai noņemt jebkuras organizācijas, kuras vēlaties iekļaut politikā.
5. Izvērsiet vai sakļaujiet sadaļu **Ierobežojuma nosacījumi**.
6. Sarakstā atrodiet iepriekš izveidoto ierobežojuma nosacījumu.
7. Atlasiet **Izveidot ierobežojuma nosacījumu**.
8. Laukā **Spēkā stāšanās datums** ievadiet datumu, kurā politikai vajadzētu stāties spēkā.
    * Iestatot spēkā stāšanās beigu datumus, ir iespējams veikt turpmākas ierobežojuma nosacījumu izmaiņas, tādēļ nebūs jāatgriežas pie politikas, lai šīs izmaiņas aktivizētu.  
9. Ja nepieciešams, pievienojiet klauzulu laukā **Pievienot nosacījumu**.
    * Piemēram, ja jūs vēlaties, lai kārtula attiecas tikai uz pārdošanas daļu vadītājiem, izveidojiet ¨kur¨ klauzulu ar loģiku: kur amata apraksts ir vienāds ar pārdošanas daļas vadītājs. Vienā kārtulā varat pievienot vairākus ¨kur¨ nosacījumus.  
10. Atlasiet **Labi**.
11. Aizvērt lapu.

## <a name="assign-rule-to-benefit"></a>Nosacījuma piešķiršana atvieglojumam

1. Pārejiet uz sadaļu **Personāla vadība > Atvieglojumi > Atvieglojumi**.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā atlasiet saiti atlasītajā rindā.
4. Izvērsiet vai sakļaujiet sadaļu **Piemērotības noteikumi**.
5. Atlasiet **Rediģēt**.
6. Laukā **Piemērojamība** atlasiet kārtulu.
7. Laukā **Kārtulas veids** atlasiet iepriekš izveidoto nosacījumu.
9. Sarakstā atlasiet saiti atlasītajā rindā.
10. Atlasiet **Saglabāt**.
11. Aizveriet formu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]