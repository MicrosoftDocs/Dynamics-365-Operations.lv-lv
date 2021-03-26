---
title: Bieži uzdotie jautājumi par finanšu pārskatu veidošanu
description: Šajā tēmā uzskaitīti jautājumi saistībā ar finanšu pārskatu veidošanu, kurus uzdevuši citi lietotāji.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2d49213ea18e09f04b026559bdca49fee1de0ef7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249310"
---
# <a name="financial-reporting-faq"></a>Bieži uzdotie jautājumi par finanšu pārskatu veidošanu 

Šajā tēmā uzskaitīti jautājumi saistībā ar finanšu pārskatu veidošanu, kurus uzdevuši citi lietotāji. 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Kā var ierobežot piekļuvi pārskatam, izmantojot drošības koku?

Scenārijs: USMF demonstrācijas uzņēmumam ir bilances pārskats, un uzņēmums nevēlas, lai visi finanšu pārskatu lietotāji to varētu skatīt pakalpojumā D365. Risinājums: jūs varat izmantot drošības koku, lai ierobežotu piekļuvi atsevišķam pārskatam, lai tikai noteikti lietotāji varētu piekļūt pārskatam. 

1.  Piesakieties finanšu pārskatu veidotājā

2.  Izveidojiet jaunu koka definīciju (Fails | Jauns | Koka definīcija) a.    Veiciet dubultklikšķi kolonnas **Vienības drošība** rindā **Kopsavilkums**.
  i.    Noklikšķiniet uz Lietotāji un grupas.  
          1. Atlasiet lietotājus vai grupu, kas vēlas piekļūt šim pārskatam. 
          
[![lietotāja ekrāns](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)

[![drošības ekrāns](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)

  b.    Noklikšķiniet uz **Saglabāt**.
  
[![poga Saglabāt](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)

3.  Pārskata definīcijā pievienojiet jaunu koka definīciju

[![koka definīcijas forma](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)

A.  Koka definīcijas sadaļā noklikšķiniet uz Iestatījums un sadaļā “Pārskata vienību atlase” atzīmējiet “Iekļaut visas vienības”

[![pārskata vienības atlases forma](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)

**Pirms:** [![pirms ekrānuzņēmuma](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)

**Pēc:** [![pēc ekrānuzņēmuma](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)

Piezīme. Iepriekš minētā ziņojuma iemesls ir: lietotājam nav piekļuves šim pārskatam pēc vienības drošības lietošanas



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a>Kā var noteikt, kuri konti neatbilst manām bilancēm pakalpojumā D365?

Ja jums ir pārskats, kas neatbilst tam, ko varētu sagaidīt pakalpojumā D365, tālāk norādītas dažas darbības, ko varat veikt, lai identificētu šos kontus un novirzes. 

### <a name="in-financial-reporter-report-designer"></a>Finanšu pārskatu veidotājā

1.  Izveidojiet jaunu rindas definīciju a.    Noklikšķiniet uz Rediģēt | Ievietot rindas no dimensijām i.  Atlasiet MainAccount [![Atlasiet galveno ekrānu](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)
    
    ii. Noklikšķiniet uz Labi b.    Saglabājiet rindas definīciju

2.  Izveidojiet jaunu kolonnas definīciju     [![Izveidojiet jaunu kolonnas definīciju](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)

3.  Izveidojiet jaunu pārskata definīciju a.    Noklikšķiniet uz iestatījumiem un noņemiet atzīmi no [![Iestatījumu formas](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)
   
4.  Ģenerējiet pārskatu. 

5.  Eksportējiet pārskatu uz programmu Excel.

### <a name="in-d365"></a>Pakalpojumā D365: 
1.  Noklikšķiniet uz Virsgrāmata | Pieprasījumi un pārskati | Apgrozījuma bilance a.    Parametri i.  Sākuma datums: finanšu gada sākums ii. Beigu datums: datums, kam ģenerēts pārskats iii.    Finanšu dimensijas kopa “Galvenā konta kopa” [![Galvenā konta forma](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)
      
  b.    Noklikšķiniet uz Aprēķināt

2.  Eksportējiet pārskatu uz programmu Excel

Tagad vajadzētu būt iespējai no FR Excel pārskata kopēt datus uz D365 apgrozījuma bilances pārskatu un salīdzināt kolonnas “Beigu bilance”.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]