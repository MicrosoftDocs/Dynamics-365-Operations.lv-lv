---
title: Pirkšanas ierobežojumu izveide
description: Šajā tēmā ir parādīts, kā izveidot pirkšanas politikas, lai tās atbilstu jūsu biznesa pirkšanas procesiem.
author: Henrikan
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dde2df0f04ea8ed1b200ae731df7143cc8de3aae
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579500"
---
# <a name="create-purchasing-policies"></a>Pirkšanas ierobežojumu izveide

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir parādīts, kā izveidot pirkšanas politikas, lai tās atbilstu jūsu biznesa pirkšanas procesiem. Lai varētu izveidot pirkšanas politikas, ir jāiestata pirkšanas politikas parametri. Pirkšanas politiku var izveidot, modificēt un noņemt, bet pirkšanas politiku nevar dzēst. Šo procedūru parasti veic pirkšanas vadītājs. Šo procedūru varat lietot, izmantojot paraugdatu uzņēmumu USMF vai izmantojot savus datus.


## <a name="set-up-policy-parameters"></a>Iestatīt politikas parametrus
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Sagāde un avoti > Iestatīšana > Politikas > Pirkšanas politikas**.
2. Darbību rūtī atlasiet **Parametri**.
- Politikas prioritātes kārtulas attiecas uz dažādiem līmeņiem jūsu organizācijā. Rādītās organizācijas vienības ir atkarīgas no jūsu organizācijas hierarhijas, kā arī no tā, kuros hierarhijas līmeņos ir piešķirts sagādes iekšējās kontroles mērķis. Piemēram, jūsu organizācijā var būt juridiskās personas, izmaksu centri, reģioni un departamenti, bet ir iespējams, ka tikai dažiem no tiem ir sagādes iekšējās kontroles hierarhijas mērķis. Pēc noklusējuma ir pieejama organizācija ar tipu Uzņēmums.  
3. Atlasiet cilni **Politikas kārtulas tipu parametri**.
4. Koka struktūrā dodieties uz **Pirkšanas politika > Pirkšanas pieprasījuma kontroles kārtula**.
- Jūs definējat ierobežojumu piemērošanas prioritāšu secību ierobežojumu līmenī. Tomēr dažiem ierobežojumu veidiem var ignorēt atsevišķu ierobežojumu kārtulu tipu prioritāšu secību. Piemēram, pirkšanas politikām varat definēt šādu prioritāšu secību: izmaksu centrs, departaments, uzņēmums. Kataloga politikas kārtulai, iespējams, vēlaties šādu prioritāšu secību: departaments, izmaksu centrs, uzņēmums. Kataloga politikas kārtulai varat mainīt prioritāšu secību. Kad kāds nodarbinātais izveido pieprasījumu, tad rādītais katalogs ir atkarīgs no politikām, kas ir saistītas ar šī nodarbinātā departamentu, pēc tam — viņa izmaksu centru, un pēc tam — viņa uzņēmumu.  
- Ja ir uzskaitīti vairāki organizācijas līmeņi, varat lietot augšupvērsto/lejupvērsto bultiņu, lai iestatītu pirkšanas pieprasījuma kontroles kārtulas prioritāšu secību.  
5. Aizvērt lapu.

## <a name="create-a-new-policy"></a>Izveidot jaunu politiku
1. Atlasiet **Jauns**.
2. Laukā **Nosaukums** ierakstiet kādu vērtību.
3. Laukā **Apraksts** ierakstiet kādu vērtību.
- Viena pirkšanas politika var attiekties tikai uz vienu organizācijas hierarhiju. Piemēram, jums varētu būt viena hierarhija ar nosaukumu “Ģeogrāfisks” un viena ar nosaukumu “Departaments”, un katrai no tām var būt citāda pirkšanas politika.  
- Atlasiet organizāciju, kam ir jālieto šī politika.  
4. Atlasiet bultiņu, lai pievienotu atlasīto organizāciju.
- Varat atkārtot šo procesu, lai pievienotu vairāk organizāciju.  

## <a name="add-a-policy-rule"></a>Pievienot politikas kārtulu
1. Sarakstā **Politikas kārtulu tips** atlasiet **Pieprasījuma mērķa kārtula**.
- Jūs izveidosiet kārtulu, kas noklusējuma pieprasījuma mērķi iestata uz tipu Patēriņš, bet ļauj tā vietā atlasīt tipu Papildināšana.  
2. Atlasiet **Izveidot ierobežojuma nosacījumu**.
3. Atlasiet **Jā** laukā **Atļaut manuālo ignorēšanu**.
4. Atlasiet **Aizvērt**.
- Tagad pirkšanas politikai varat iestatīt citas politikas kārtulas. Ņemiet vērā, ka tipā Politikas kārtula nevar būt kārtulu, kuras pārklājas un kuras vienlaicīgi ir aktīvas vienā un tajā pašā sagādes politikā.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]