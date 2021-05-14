---
title: Bieži uzdotie jautājumi par finanšu pārskatu veidošanu
description: Šajā tēmā uzskaitīti jautājumi saistībā ar finanšu pārskatu veidošanu, kurus uzdevuši citi lietotāji.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923029"
---
# <a name="financial-reporting-faq"></a>Bieži uzdotie jautājumi par finanšu pārskatu veidošanu 

Šī tēma sniedz atbildes uz bieži uzdotiem jautājumiem par finanšu pārskatu veidošanu. 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Kā var ierobežot piekļuvi pārskatam, izmantojot koka drošību?

Šajā piemērā parādīts, kā ierobežot piekļuvi pārskatam, izmantojot koka drošību.

USMF demonstrācijas uzņēmumam ir bilances pārskats, kuram nedrīkstētu piekļūt visi finanšu pārskatu lietotāji. Lai ierobežotu piekļuvi, varat izmantot koka drošību, lai ierobežotu piekļuvi atsevišķam pārskatam, lai tikai noteikti lietotāji varētu piekļūt pārskatam. Lai ierobežotu piekļuvi, rīkojieties šādi: 

1. Pierakstieties rīkā Financial Reporter Report Designer.
2. Izveidojiet jaunu koka definīciju. Go to **Fails > Jauns > Koka definīcija**.
3. Veiciet dubultklikšķi kolonnas **Vienības drošība** rindā **Kopsavilkums**.
4. Atlasiet **Lietotāji un grupas**.  
5. Atlasiet lietotājus vai grupu, kam vajadzīga piekļuve šim pārskatam. 
6. Atlasiet **Saglabāt**.
7. Pārskata definīcijā pievienojiet jaunu koka definīciju.
8. Koka definīcijā atlasiet **Iestatījums**. Sadaļā **Pārskata vienību atlase** atlasiet **Iekļaut visas vienības**.

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a>Kā var noteikt, kuri konti neatbilst manām bilancēm?

Ja jums ir pārskats, kurā nav saskaņotu bilanču, tālāk norādītas dažas darbības, ko varat veikt, lai identificētu šos kontus un novirzes. 

**Financial Reporter Report Designer**
1. Rīkā Financial Reporter Report Designer izveidojiet jaunu rindas definīciju. 
2. Atlasiet **Rediģēt > Ievietot rindas no dimensijām**.
3. Atlasiet **MainAccount**.  
4. Atlasiet **Labi**.
5. Saglabājiet rindas definīciju.
6. Jaunas kolonnas definīcijas izveide
7. Izveidojiet jaunu pārskata definīciju.
8. Atlasiet **Iestatījumi** un noņemiet atzīmi šai opcijai.  
9. Ģenerējiet pārskatu. 
10. Eksportējiet pārskatu uz Microsoft Excel.

**Dynamics 365 Finance** 
1. Programmā Dynamics 365 Finance dodieties uz **Virsgrāmata > Pieprasījumi un pārskati > Apgrozījuma bilance**.
2. Iestatiet šādus parametrus:
   - **Sākuma datums** — ievadiet finanšu gada sākumu.
   - **Beigu datums** — ievadiet datumu, kuram ģenerējat pārskatu.
   - **Finanšu dimensija** — iestatiet šo lauku kā **Galvenā konta kopa**.
 3. Atlasiet **Aprēķināt**.
 4. Eksportējiet pārskatu uz Microsoft Excel.

Tagad vajadzētu būt iespējai no Finanšu pārskatu Excel pārskata kopēt datus uz apgrozījuma bilances pārskatu, lai varat salīdzināt kolonnas **Beigu bilance**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]