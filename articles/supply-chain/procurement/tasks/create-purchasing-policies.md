--- 
title: "Pirkšanas ierobežojumu izveide"
description: "Šajā procedūrā ir parādīts, kā izveidot pirkšanas politikas, lai tās atbilstu jūsu biznesa pirkšanas procesiem."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c2b3a66443394f5bfbe51b6685513281025d68fd
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-purchasing-policies"></a>Pirkšanas ierobežojumu izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā izveidot pirkšanas politikas, lai tās atbilstu jūsu biznesa pirkšanas procesiem. Lai varētu izveidot pirkšanas politikas, ir jāiestata pirkšanas politikas parametri. Pirkšanas politiku var izveidot, modificēt un noņemt, bet pirkšanas politiku nevar dzēst. Šo procedūru parasti veic pirkšanas vadītājs. Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.


## <a name="set-up-policy-parameters"></a>Iestatīt politikas parametrus
1. Dodieties uz Pirkšanas politikas.
2. Noklikšķiniet uz Parametri.
    * Politikas prioritātes kārtulas attiecas uz dažādiem līmeņiem jūsu organizācijā. Rādītās organizācijas vienības ir atkarīgas no jūsu organizācijas hierarhijas, kā arī no tā, kuros hierarhijas līmeņos ir piešķirts sagādes iekšējās kontroles mērķis. Piemēram, jūsu organizācijā var būt juridiskās personas, izmaksu centri, reģioni un departamenti, bet ir iespējams, ka tikai dažiem no tiem ir sagādes iekšējās kontroles hierarhijas mērķis. Pēc noklusējuma ir pieejama organizācija ar tipu Uzņēmums.  
3. Noklikšķiniet uz cilnes Politikas kārtulas tipu parametri.
4. Koka struktūrā atlasiet vienumu “Pirkšanas politika\Pirkšanas pieprasījuma kontroles kārtula”.
    * Jūs definējat ierobežojumu piemērošanas prioritāšu secību ierobežojumu līmenī. Tomēr dažiem ierobežojumu veidiem var ignorēt atsevišķu ierobežojumu kārtulu tipu prioritāšu secību. Piemēram, pirkšanas politikām varat definēt šādu prioritāšu secību: izmaksu centrs, departaments, uzņēmums. Kataloga politikas kārtulai, iespējams, vēlaties šādu prioritāšu secību: departaments, izmaksu centrs, uzņēmums. Kataloga politikas kārtulai varat mainīt prioritāšu secību. Kad kāds nodarbinātais izveido pieprasījumu, tad rādītais katalogs ir atkarīgs no politikām, kas ir saistītas ar šī nodarbinātā departamentu, pēc tam — viņa izmaksu centru, un pēc tam — viņa uzņēmumu.  
    * Ja ir uzskaitīti vairāki organizācijas līmeņi, varat lietot augšupvērsto/lejupvērsto bultiņu, lai iestatītu pirkšanas pieprasījuma kontroles kārtulas prioritāšu secību.  
5. Aizvērt lapu.

## <a name="create-a-new-policy"></a>Izveidot jaunu politiku
1. Noklikšķiniet uz Jauns.
2. Laukā Nosaukums ierakstiet kādu vērtību.
3. Apraksta laukā ierakstiet vērtību.
    * Viena pirkšanas politika var attiekties tikai uz vienu organizācijas hierarhiju. Piemēram, jums varētu būt viena hierarhija ar nosaukumu “Ģeogrāfisks” un viena ar nosaukumu “Departaments”, un katrai no tām var būt citāda pirkšanas politika.  
    * Atlasiet organizāciju, kam ir jālieto šī politika.  
4. Noklikšķiniet uz bultiņas, lai pievienotu atlasīto organizāciju.
    * Varat atkārtot šo procesu, lai pievienotu vairāk organizāciju.  

## <a name="add-a-policy-rule"></a>Pievienot politikas kārtulu
1. Politikas kārtulu tipu sarakstā atlasiet Pieprasījuma mērķa kārtula.
    * Jūs izveidosiet kārtulu, kas noklusējuma pieprasījuma mērķi iestata uz tipu Patēriņš, bet ļauj tā vietā atlasīt tipu Papildināšana.  
2. Noklikšķiniet uz Izveidot politikas kārtulu.
3. Laukā Atļaut manuālo ignorēšanu atlasiet Jā.
4. Noklikšķiniet uz Aizvērt.
    * Tagad pirkšanas politikai varat iestatīt citas politikas kārtulas.   Ņemiet vērā, ka tipā Politikas kārtula nevar būt kārtulu, kuras pārklājas un kuras vienlaicīgi ir aktīvas vienā un tajā pašā sagādes politikā.  
5. Aizvērt lapu.
6. Aizvērt lapu.


