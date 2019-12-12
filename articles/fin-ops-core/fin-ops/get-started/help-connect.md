---
title: Savienojuma izveide ar palīdzības sistēmu
description: Šajā tēmā ir aprakstīti Finance and Operations programmu palīdzības sistēmas komponenti, kā arī ir sniegts apskats par savienojumu izveidi ar tiem un kopsavilkums par pielāgota palīdzības satura izveidi.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2955464aa8a220563db1b9ebbb348be52f520659
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812584"
---
# <a name="connect-the-help-system"></a>Savienojuma izveide ar palīdzības sistēmu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti palīdzības sistēmas komponenti Finance and Operations programmām, piemēram Dynamics 365 Finance, Supply Chain Management, Retail un Talent. Tajā ir sniegts pārskats par to, kā izveidot savienojumu ar šiem komponentiem, kā arī kopsavilkums par to, kā izveidot pielāgotus palīdzības materiālus.

## <a name="help-architecture"></a>Palīdzības arhitektūra

Nākamajā attēlā ir parādītas daļas no palīdzības sistēmas. Produktā iebūvētā palīdzības sistēma izgūst rakstus no https://docs.microsoft.com, kā arī uzdevumu ceļvežus no Biznesa procesu modelētāja pakalpojumos Lifecycle Services (LCS).

> [!NOTE]
> Līdzekļi, kas diagrammā ir atzīmēti ar zvaigznīti (\*), ir plānoti, taču vēl nav pieejami.

[![Palīdzības sistēmas arhitektūra](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Savienojuma izveide ar palīdzības sistēmu

> [!NOTE]
> Cilne **Uzdevumu ceļveži** pašlaik nav pieejama Dynamics 365 Talent vai Retail. Mēs pašlaik strādājam pie tā, šo funkcionalitāti iespējotu nākamajos laidienos. Uzdevumu ceļveži versijas Talent funkcionalitātē Darba sākšana joprojām ir pieejami pamata funkcionalitātes segšanai. Procesuālā palīdzība ir pieejama arī vietnē docs.microsoft.com gan Retail, gan Talent.

Izmantojot lapu **Sistēmas parametri**, sistēmas administratori izveido savienojumu ar palīdzības sistēmas daļām implementācijas nolūkā.

[![Veidlapa Sistēmas parametri, kurā ir atvērti palīdzības iestatījumi](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Lapā **Sistēmas parametri** izpildiet šādas darbības:

> [!IMPORTANT]
> Kad cilni **Palīdzība** atverat pirmo reizi, ir jāizveido savienojums ar Lifecycle Services. Noteikti noklikšķiniet uz saites formas vidū, uzgaidiet, līdz tiek izveidots savienojums, aizveriet dialoglodziņu un pēc tam noklikšķiniet uz **Labi**, lai piekļūtu lapai **Sistēmas parametri**.
>
> [![Izveidot savienojumu ar LCS](./media/connect-to-lcs-crop-1024x365.png "Izveidot savienojumu ar LCS")](./media/connect-to-lcs-crop.png)

1. Atlasiet Lifecycle Services projektu, ar kuru izveidot savienojumu.
2. Atlasiet BPM bibliotēkas (atlasītajā projektā), no kurām izgūt uzdevumu ierakstus.
3. Iestatiet BPM bibliotēku attēlošanas secību. Tā nosaka secību, kādā uzdevumu ieraksti no bibliotēkām tiks rādīti rūtī **Palīdzība**.

Kad esat izpildījis šīs darbības, varat atvērt rūti **Palīdzība** un noklikšķināt uz cilnes **Uzdevumu ceļveži**. Tagad tiek rādīti uzdevumu ceļveži, kas attiecas uz Finance and Operations programmās pašlaik atvērto lapu. Ja netiek atrasts neviens uzdevuma ceļvedis, varat ievadīt atslēgvārdus, lai precizētu meklēšanu.

### <a name="showing-translated-task-guides"></a>Tulkotu uzdevumu ceļvežu parādīšana

Tulkotie uzdevumu ceļveži pirmo reizi tika nodrošināti 2016. gada maijā izlaistajā APQC vienotajā bibliotēkā un darba sākšanas bibliotēkā. Lai redzētu lokalizēto uzdevumu ceļvežu palīdzību Finance and Operations programmās, pārliecinieties, ka ir izveidots savienojums ar maija bibliotēku. Uzdevuma ceļveža rādīšanas valodu katram lietotājam var norādīt, izmantojot valodas iestatījumus sadaļā **Opcijas** &gt; **Preferences**.

> [!NOTE]
> Lai gan daudzi uzdevumu ceļveži ir iztulkoti, pašlaik klients nerāda tulkoto uzdevumu ceļvežu nosaukumus. Turklāt maijā izlaistajā bibliotēkā tulkotā veidā ir pieejami tikai tie uzdevumu ceļveži, kas tika izlaisti 2016. gada februārī. Mēs izdosim atjauninātu bibliotēku ar papildu tulkojumiem.
>
> - Ja kāds uzdevumu ceļvedis ir iztulkots, kad atverat šo uzdevumu ceļvedi, viss uzdevuma ceļveža teksts jums tiek rādīts jūsu izvēlētajā valodā.
> - Ja kāds uzdevumu ceļvedis vēl nav iztulkots, kad to atverat, jūsu izvēlētajā valodā jums tiek rādīta tikai daļa teksta (vadīklu teksts).

## <a name="creating-custom-help"></a>Pielāgotas palīdzības veidošana

Var lietot uzd. ceļv., lai izveidotu piel. palīdz. vai savienotu vietni ar rūti Pal.

### <a name="create-custom-help-with-task-guides"></a>Pielāg. pal. izveide ar uzd. ceļv.

Savai programmatūrai Finance, Supply Chain Management un Retail varat izveidot pielāgotu palīdzību, izveidojot uzdevumu ierakstus, kas atspoguļo jūsu implementāciju, un tos saglabājot LCS biznesa procesu bibliotēkā. Pielāgotus uzdevumu ceļvežus nevar izveidot programmatūrai Talent.

Partneriem — ja bibliotēku paaugstināt uz korporatīvu bibliotēku, un iekļaut to kādā risinājumā, tā būs pieejama jūsu klientiem. Varat arī izveidot APQC vienotās globālās bibliotēkas kopiju, pēc tam atvērt savu kopiju, no tās atvērt uzdevumu ierakstus, modificēt tos un saglabāt ierakstus ar savām veiktajām izmaiņām. Papildinformāciju skatiet tēmā [Uzdevuma reģistrētāja resursi](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-site"></a>Sav. ar piel. vietni

Microsoft ir sniedzis tehn. dokum. un parauga kodu, kas apraksta, kā veidot un savienot pielāg. palīdz. vietni ar rūti Palīdzība. Plašāku informāciju skatiet:

- [Pielāg. palīdz. izveide Finance and Operations programmām (tehn. dok.)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Pielāg. palīdz. GitHub repoz.](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>Papildu resursi

[Palīdzības sistēma](help-overview.md)

[Uzdevuma reģistrētāja resursi](../../dev-itpro/user-interface/task-recorder.md)

[Dokumentācijas vai apmācības izveide, izmantojot uzdevuma reģistrētāju](../../dev-itpro/user-interface/task-recorder-training-docs.md)