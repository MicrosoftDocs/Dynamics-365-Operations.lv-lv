---
title: "Savienojuma izveide ar palīdzības sistēmu"
description: "Šajā tēmā ir aprakstīti programmatūrai Microsoft Dynamics 365 for Operations paredzētās palīdzības sistēmas komponenti, sniegts apskats par to, kā tos savienot, un kopsavilkums par to, kā izveidot pielāgotu palīdzību."
author: margoc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 86c7cb3961ba5170c32979e77aaa5f506ffac8a1
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="connect-the-help-system"></a>Savienojuma izveide ar palīdzības sistēmu

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīti Microsoft Dynamics 365 for Operations palīdzības sistēmas komponenti. Tajā ir sniegts pārskats par to, kā izveidot savienojumu ar šiem komponentiem, kā arī kopsavilkums par to, kā izveidot pielāgotus palīdzības materiālus. 

<a name="help-architecture"></a>Palīdzības arhitektūra
-----------------

Tālāk esošajā attēlā ir redzamas Dynamics 365 for Operations palīdzības sistēmas daļas. Produktā iebūvētā palīdzības sistēma nodrošina rakstu izguvi no Dynamics 365 for Operations vietnes (https://docs.microsoft.com), kā arī uzdevumu ceļvežus no biznesa procesu modelētāja pakalpojumos Lifecycle Services (LCS). 
**Piezīme.** Līdzekļi, kas shēmā ir atzīmēti ar zvaigznīti (\*), ir plānoti, taču vēl nav pieejami. [![Palīdzības sistēmas arhitektūra](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Savienojuma izveide ar palīdzības sistēmu
Izmantojot lapu **Sistēmas parametri**, sistēmas administratori izveido savienojumu ar palīdzības sistēmas daļām implementācijas nolūkā. [![Veidlapa Sistēmas parametri ar palīdzības sistēmas iestatījumiem](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Lapā **Sistēmas parametri** veiciet tālāk norādītās darbības.

> [!IMPORTANT]
> Kad cilni **Palīdzība** atverat pirmo reizi, ir jāizveido savienojums ar Lifecycle Services. Noteikti noklikšķiniet uz saites veidlapas vidū, uzgaidiet, līdz tiek izveidots savienojums, aizveriet dialoglodziņu un pēc tam noklikšķiniet uz **Labi**, lai piekļūtu lapai **Sistēmas parametri**.[![Savienojuma izveide ar LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)

1.  Atlasiet Lifecycle Services projektu, ar kuru izveidot savienojumu.
2.  Atlasiet BPM bibliotēkas (atlasītajā projektā), no kurām izgūt uzdevumu ierakstus.
3.  Iestatiet BPM bibliotēku attēlošanas secību. Tā nosaka secību, kādā uzdevumu ieraksti no bibliotēkām tiks rādīti rūtī **Palīdzība**.

Kad esat pabeidzis šīs darbības, varat atvērt rūti **Palīdzība** un noklikšķināt uz cilnes **Uzdevumu ceļveži**. Tagad tiek rādīti uzdevumu ceļveži, kas attiecas uz programmatūrā Dynamics 365 for Operations pašlaik atvērto lapu. Ja netiek atrasts neviens uzdevuma ceļvedis, varat ievadīt atslēgvārdus, lai precizētu meklēšanu.

### <a name="showing-translated-task-guides"></a>Tulkotu uzdevumu ceļvežu parādīšana

Tulkotie uzdevumu ceļveži pirmo reizi tika nodrošināti 2016. gada maijā izlaistajā APQC vienotajā bibliotēkā un darba sākšanas bibliotēkā. Lai programmatūrā Dynamics 365 for Operations redzētu lokalizēto uzdevumu ceļvežu palīdzību, pārliecinieties, ka ir izveidots savienojums ar maija bibliotēku. Uzdevuma ceļveža rādīšanas valodu katram lietotājam var norādīt, izmantojot valodas iestatījumus sadaļā **Opcijas** &gt; **Preferences**. 

> [!NOTE]
> Lai gan daudzi uzdevumu ceļveži ir iztulkoti, pašlaik Dynamics 365 for Operations klients nerāda tulkoto uzdevumu ceļvežu nosaukumus. Turklāt maijā izlaistajā bibliotēkā tulkotā veidā ir pieejami tikai tie uzdevumu ceļveži, kas tika izlaisti 2016. gada februārī. Mēs izdosim atjauninātu bibliotēku ar papildu tulkojumiem.
> -   Ja kāds uzdevumu ceļvedis ir iztulkots, kad atverat šo uzdevumu ceļvedi, viss uzdevuma ceļveža teksts jums tiek rādīts jūsu izvēlētajā valodā.
> -   Ja kāds uzdevumu ceļvedis vēl nav iztulkots, kad to atverat, jūsu izvēlētajā valodā jums tiek rādīta tikai daļa teksta (vadīklu teksts).

## <a name="creating-custom-help"></a>Pielāgotas palīdzības veidošana
Savai Dynamics 365 for Operations implementācijai varat izveidot pielāgotu palīdzību, izveidojot uzdevumu ierakstus, kas atspoguļo jūsu implementāciju, un tos saglabājot LCS biznesa procesu bibliotēkā. Partneriem — ja bibliotēku paaugstināt uz korporatīvu bibliotēku, un iekļaut to kādā risinājumā, tā būs pieejama jūsu klientiem. Varat arī izveidot APQC vienotās globālās bibliotēkas kopiju, pēc tam atvērt savu kopiju, no tās atvērt uzdevumu ierakstus, modificēt tos un saglabāt ierakstus ar savām veiktajām izmaiņām. Papildinformāciju skatiet tēmā [Kā izveidot uzdevuma ierakstu izmantošanai dokumentācijas vai apmācības nolūkā](../user-interface/task-recorder.md).

<a name="see-also"></a>Skatiet arī
--------

[Pārskats par palīdzības sistēmu](help-overview.md)

[Pārskats par uzdevuma reģistrētāju](../user-interface/task-recorder.md)

[Kā izveidot uzdevuma ierakstu, ko lietot kā dokumentāciju vai apmācību](../user-interface/task-recorder-training-docs.md)





