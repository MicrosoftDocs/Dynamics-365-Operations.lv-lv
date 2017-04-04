---
title: "Savienojuma izveide ar palīdzības sistēmu"
description: "Šajā tēmā ir aprakstīti programmatūrai Microsoft Dynamics 365 for Operations paredzētās palīdzības sistēmas komponenti, sniegts apskats par to, kā tos savienot, un kopsavilkums par to, kā izveidot pielāgotu palīdzību."
author: margoc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 5ac5e30cff2239f601778001368fa7aaba478f5c
ms.lasthandoff: 03/31/2017


---

# <a name="connect-the-help-system"></a>Savienojuma izveide ar palīdzības sistēmu

Šajā tēmā ir aprakstītas palīdzības sistēmas komponentiem par Microsoft Dynamics 365 operācijām. Tajā sniegts pārskats par to, kā savienot šos komponentus un kopsavilkumu par to, kā izveidot pielāgotu palīdzību. 

<a name="help-architecture"></a>Palīdzības arhitektūra
-----------------

Sekojošajā attēlā redzama dinamika 365 palīdzības operāciju sistēmas daļām. Produkta palīdzības sistēma atvelk rakstus no Dynamics 365 darbības vietu uz https://docs.microsoft.com, kā arī uzdevumu gidi, kas saglabāti Business Process modelētājs Lifecycle Services (LCS). 
**Piezīme:** shēmā ar zvaigznīti uzskaitītās pazīmes (\*) ir plānotas, bet vēl nav pieejami. [![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Savieno palīdzības sistēma
Izmantojot **sistēmas parametru** lapu, sistēmas administratoriem izveidot savienojumu gabali palīdzības sistēmas īstenošanai. [![Sistēmas parametru formā ar palīdzības iestatījumi](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) par **sistēmas parametru** lapu, rīkojieties šādi:

1.  **Svarīgi:** pirmo reizi atverat **palīdzēt** tab, ir jāizveido savienojums ar Lifecycle Services. Neaizmirstiet saite vidū formu, sagaidiet savienojumu, aizveriet dialoglodziņu un pēc tam noklikšķiniet uz **OK** nokļūt **sistēmas parametru** lapā. [![LCS pieslēgties](./media/connect-to-lcs-crop-1024x365.png "LCS pieslēgties")](./media/connect-to-lcs-crop.png)
2.  Atlasiet Lifecycle Services projektu, ar kuru izveidot savienojumu.
3.  Atlasiet BPM bibliotēkas (atlasītajā projektā), no kurām izgūt uzdevumu ierakstus.
4.  Iestatiet BPM bibliotēku attēlošanas secību. Tā nosaka secību, kādā uzdevumu ieraksti no bibliotēkām tiks rādīti rūtī **Palīdzība**.

Kad esat pabeidzis šīs darbības, varat atvērt rūti **Palīdzība** un noklikšķināt uz cilnes **Uzdevumu ceļveži**. Tagad tiek rādīti uzdevumu ceļveži, kas attiecas uz programmatūrā Dynamics 365 for Operations pašlaik atvērto lapu. Ja netiek atrasts neviens uzdevuma ceļvedis, varat ievadīt atslēgvārdus, lai precizētu meklēšanu.

### <a name="showing-translated-task-guides"></a>Tulkotu uzdevumu ceļvežu parādīšana

Rokasgrāmatas tulkotās uzdevumu vispirms tika nosūtītas maija 2016 APQC vienotās bibliotēku un bibliotēku darba sākšana. Lai programmatūrā Dynamics 365 for Operations redzētu lokalizēto uzdevumu ceļvežu palīdzību, pārliecinieties, ka ir izveidots savienojums ar maija bibliotēku. Valodu, kurā tiek parādīta uzdevumu rokasgrāmata katram lietotājam kontrolē valodu iestatījumos, kas atrodas **opcijas**&gt;**Preferences**. **Piezīme.** Lai gan daudzi uzdevumu ceļveži ir iztulkoti, pašlaik Dynamics 365 for Operations klients nerāda tulkoto uzdevumu ceļvežu nosaukumus. Arī, tikai uzdevumu gidi, kas tika izlaists februāra 2016 pieejami tulkošanas maijs bibliotēkā. Mēs izdosim atjauninātu bibliotēku ar papildu tulkojumiem.

-   Ja kāds uzdevumu ceļvedis ir iztulkots, kad atverat šo uzdevumu ceļvedi, viss uzdevuma ceļveža teksts jums tiek rādīts jūsu izvēlētajā valodā.
-   Ja kāds uzdevumu ceļvedis vēl nav iztulkots, kad to atverat, jūsu izvēlētajā valodā jums tiek rādīta tikai daļa teksta (vadīklu teksts).

## <a name="creating-custom-help"></a>Pielāgotas palīdzības veidošana
Savai Dynamics 365 for Operations implementācijai varat izveidot pielāgotu palīdzību, izveidojot uzdevumu ierakstus, kas atspoguļo jūsu implementāciju, un tos saglabājot LCS biznesa procesu bibliotēkā. Partneriem — ja bibliotēku paaugstināt uz korporatīvu bibliotēku, un iekļaut to kādā risinājumā, tā būs pieejama jūsu klientiem. Varat arī izveidot APQC vienotās globālās bibliotēkas kopiju, pēc tam atvērt savu kopiju, no tās atvērt uzdevumu ierakstus, modificēt tos un saglabāt ierakstus ar savām veiktajām izmaiņām. Lai iegūtu papildinformāciju, skatiet [kā izveidot uzdevuma ierakstu, kuru vēlaties izmantot kā dokumentāciju vai apmācību](../user-interface/task-recorder.md).

<a name="see-also"></a>Skatiet arī
--------

[Help overview](help-overview.md)

[Ierakstītājs uzdevumu apskats](../user-interface/task-recorder.md)

[Kā izveidot uzdevuma ierakstu, ko lietot kā dokumentāciju vai apmācību](../user-interface/task-recorder-training-docs.md)

[Izveidojot jaunu apmācību bibliotēkās Dynamics 365 operācijas ietvaros Lifecycle Services programmatūra, izmantojot uzdevuma Recorder (ārējā saite)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)


