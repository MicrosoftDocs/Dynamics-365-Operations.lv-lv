---
title: "Savienojuma izveide ar palīdzības sistēmu"
description: "Šajā tēmā ir aprakstīti programmatūrai Microsoft Dynamics 365 for Finance and Operations paredzētās palīdzības sistēmas komponenti, sniegts apskats par to, kā tos savienot, un kopsavilkums par to, kā izveidot pielāgotu palīdzību."
author: margoc
manager: AnnBe
ms.date: 09/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: a27b21ffcde9bfbb7e6276ef35b2e48bd23af70d
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="connect-the-help-system"></a>Savienojuma izveide ar palīdzības sistēmu

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīti Microsoft Dynamics 365 for Finance and Operations palīdzības sistēmas komponenti. Tajā ir sniegts pārskats par to, kā izveidot savienojumu ar šiem komponentiem, kā arī kopsavilkums par to, kā izveidot pielāgotus palīdzības materiālus. 

## <a name="help-architecture"></a>Palīdzības arhitektūra
Nākamajā attēlā ir redzamas Finance and Operations palīdzības sistēmas daļas. Produktā iebūvētā palīdzības sistēma izgūst rakstus no Finance and Operations vietnes (https://docs.microsoft.com), kā arī uzdevumu ceļvežus no biznesa procesu modelētāja pakalpojumos Lifecycle Services (LCS). 
> [!NOTE]
> Līdzekļi, kas diagrammā ir atzīmēti ar zvaigznīti (\*), ir plānoti, taču vēl nav pieejami. [![Palīdzības sistēmas arhitektūra](./media/help-architecture.png)](./media/help-architecture.png)


## <a name="connecting-the-help-system"></a>Savienojuma izveide ar palīdzības sistēmu
> [!NOTE]
> Cilne **Uzdevumu ceļveži** pašlaik nav pieejama versijā Microsoft Dynamics 365 for Talent un Microsoft Dynamics 365 for Retail. Mēs pašlaik strādājam pie tā, šo funkcionalitāti iespējotu nākamajos laidienos. Uzdevumu ceļveži versijas Talent funkcionalitātē Darba sākšana joprojām ir pieejami pamata funkcionalitātes segšanai. Palīdzība saistībā ar procedūrām ir pieejama arī vietnē docs.microsoft.com ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) gan versijai Retail, gan versijai Talent.
 

Izmantojot lapu **Sistēmas parametri**, sistēmas administratori izveido savienojumu ar palīdzības sistēmas daļām implementācijas nolūkā. [![Veidlapa Sistēmas parametri ar palīdzības sistēmas iestatījumiem](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Lapā **Sistēmas parametri** veiciet tālāk norādītās darbības.

> [!IMPORTANT]
> Kad cilni **Palīdzība** atverat pirmo reizi, ir jāizveido savienojums ar Lifecycle Services. Noteikti noklikšķiniet uz saites veidlapas vidū, uzgaidiet, līdz tiek izveidots savienojums, aizveriet dialoglodziņu un pēc tam noklikšķiniet uz **Labi**, lai piekļūtu lapai **Sistēmas parametri**.[![Savienojuma izveide ar LCS](./media/connect-to-lcs-crop-1024x365.png "Savienojuma izveide ar LCS")](./media/connect-to-lcs-crop.png)

1.  Atlasiet Lifecycle Services projektu, ar kuru izveidot savienojumu.
2.  Atlasiet BPM bibliotēkas (atlasītajā projektā), no kurām izgūt uzdevumu ierakstus.
    - Saistībā ar programmatūru Finance and Operations un Microsoft saturu atlasiet visjaunāko APQC vienoto bibliotēku programmatūrai Finance and Operations. 
    - Versijai Retail mēs bibliotēku izlaidīsim tuvākajā laikā. 
    - Nav nepieciešams atlasīt bibliotēku versijai Talent — savienojums ar pareizo bibliotēku jums ir izveidots. 

3.  Iestatiet BPM bibliotēku attēlošanas secību. Tā nosaka secību, kādā uzdevumu ieraksti no bibliotēkām tiks rādīti rūtī **Palīdzība**.

Kad esat izpildījis šīs darbības, varat atvērt rūti **Palīdzība** un noklikšķināt uz cilnes **Uzdevumu ceļveži**. Tagad tiek rādīti uzdevumu ceļveži, kas attiecas uz programmatūrā Finance and Operations pašlaik atvērto lapu. Ja netiek atrasts neviens uzdevuma ceļvedis, varat ievadīt atslēgvārdus, lai precizētu meklēšanu.

### <a name="showing-translated-task-guides"></a>Tulkotu uzdevumu ceļvežu parādīšana

Tulkotie uzdevumu ceļveži pirmo reizi tika nodrošināti 2016. gada maijā izlaistajā APQC vienotajā bibliotēkā un darba sākšanas bibliotēkā. Lai redzētu lokalizēto uzdevumu ceļvežu palīdzību programmatūrā Finance and Operations, pārliecinieties, ka ir izveidots savienojums ar maija bibliotēku. Uzdevuma ceļveža rādīšanas valodu katram lietotājam var norādīt, izmantojot valodas iestatījumus sadaļā **Opcijas** &gt; **Preferences**. 

> [!NOTE]
> Lai gan daudzi uzdevumu ceļveži ir iztulkoti, pašlaik Finance and Operations klients nerāda tulkoto uzdevumu ceļvežu nosaukumus. Turklāt maijā izlaistajā bibliotēkā tulkotā veidā ir pieejami tikai tie uzdevumu ceļveži, kas tika izlaisti 2016. gada februārī. Mēs izdosim atjauninātu bibliotēku ar papildu tulkojumiem.
> -   Ja kāds uzdevumu ceļvedis ir iztulkots, kad atverat šo uzdevumu ceļvedi, viss uzdevuma ceļveža teksts jums tiek rādīts jūsu izvēlētajā valodā.
> -   Ja kāds uzdevumu ceļvedis vēl nav iztulkots, kad to atverat, jūsu izvēlētajā valodā jums tiek rādīta tikai daļa teksta (vadīklu teksts).

## <a name="creating-custom-help"></a>Pielāgotas palīdzības veidošana
Savai programmatūrai Finance and Operations un Retail varat izveidot pielāgotu palīdzību, izveidojot uzdevumu ierakstus, kas atspoguļo jūsu implementāciju, un tos saglabājot LCS biznesa procesu bibliotēkā. Pielāgotus uzdevumu ceļvežus nevar izveidot programmatūrai Talent. 

Partneriem — ja bibliotēku paaugstināt uz korporatīvu bibliotēku, un iekļaut to kādā risinājumā, tā būs pieejama jūsu klientiem. Varat arī izveidot APQC vienotās globālās bibliotēkas kopiju, pēc tam atvērt savu kopiju, no tās atvērt uzdevumu ierakstus, modificēt tos un saglabāt ierakstus ar savām veiktajām izmaiņām. Papildinformāciju skatiet tēmā [Kā izveidot uzdevuma ierakstu izmantošanai dokumentācijas vai apmācības nolūkā](../../dev-itpro/user-interface/task-recorder.md).

<a name="see-also"></a>Skatiet arī
--------

[Pārskats par palīdzības sistēmu](help-overview.md)

[Pārskats par uzdevuma reģistrētāju](../../dev-itpro/user-interface/task-recorder.md)

[Kā izveidot uzdevuma ierakstu, ko lietot kā dokumentāciju vai apmācību](../../dev-itpro/user-interface/task-recorder-training-docs.md)




