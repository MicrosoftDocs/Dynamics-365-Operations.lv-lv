---
title: Iestatīt un izmantot paplašinātās pieteikšanās iespēju
description: Šajā rakstā ir aprakstīts, kā iestatīt un izmantot pārdošanas punkta Microsoft Dynamics 365 Commerce (POS) programmas paplašinātās pieteikšanās iespējas.
author: boycez
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e27e8d94adccc46559089928b0481442306567ef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884315"
---
# <a name="set-up-and-use-the-extended-logon-capability"></a>Iestatīt un izmantot paplašinātās pieteikšanās iespēju

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā iestatīt un izmantot pārdošanas punkta Microsoft Dynamics 365 Commerce (POS) programmas paplašinātās pieteikšanās iespējas.

Cloud POS (CPOS) un Modern POS (MPOS) nodrošina paplašinātas pieteikšanās iespējas, kas ļauj mazumtirdzniecības veikala darbiniekiem pieteikties POS programmā, skenējot svītrkodu vai nokopējot karti, izmantojot magnētiskās joslas lasītāju (MSR).

## <a name="set-up-extended-logon"></a>Iestatiet paplašināto pieteikšanos

Lai iestatītu POS kases sistēmas paplašināto pieteikšanos mazumtirdzniecības veikalā, veiciet šīs darbības.

1. Programmā Commerce Headquarters iet uz **Retail un Commerce Channel \> Setup POS iestatīšanas \>\> POS profilu funkcionalitātes \> profiliem**. 
2. Kreisajā navigācijas rūtī atlasiet ar mazumtirdzniecības veikalu saistīto funkcionalitātes profilu.
3. Kopsavilkuma cilnē **Funkcijas** zem Papildu pieteikšanās autentifikācijas **opcijas** iestatiet šādas opcijas kā Jā **vai** **Nē**, ja nepieciešams:

    - **Personāla pieteikšanās ar svītrkodu** — iestatiet šo opciju kā **Jā**, ja vēlaties, lai darbinieki pieteiktos sistēmā POS, skenējot svītrkodu. 
    - **Darbinieku pieteikumam ar svītrkodu** nepieciešama parole — **iestatiet** šo opciju kā Jā, lai, piesakoties POS, darbinieki ievadītu paroli, skenējot svītrkodu.
    - **Personāla pieteikšanās ar** karti — iestatiet šo opciju kā **Jā**, ja vēlaties, lai darbinieki varētu pieteikties SISTĒMĀ POS, nokopot karti.
    - **Darbinieku pieteikumam ar karti** nepieciešama parole — **iestatiet** šo opciju kā Jā, ja vēlaties, lai jūsu darbinieki, piesakoties sistēmā POS, ievadītu paroli, no ievadot karti.

Svītrkods vai karte ir saistīta ar akreditācijas datiem, ko var piešķirt darbiniekam. Akreditācijas datiem jābūt vismaz sešām rakstzīmēm. Virknei, kas satur pirmās piecas rakstzīmes *, jābūt unikālai un tiek uzskatīta par akreditācijas datu ID*, ko izmanto, lai meklē darbinieku. Atlikušās rakstzīmes tiek lietotas drošības pārbaudei. Piemēram, jums ir divas kartes, vienai no tām ir akreditācijas dati 12345DABADEYTDW, un vienai no tām ir akreditācijas dati 12345RIFUTDAJH. Šo divu karšu akreditācijas datu ID ir 12345, tāpēc tās abas nevar tikt veiksmīgi piešķirtas darbiniekiem.

## <a name="assign-extended-logon"></a>Piešķirt paplašināto pieteikšanos

Pēc noklusējuma paplašinātās pieteikšanās tiesības strādniekiem var piešķirt tikai vadītāji. Lai piešķirtu paplašināto pieteikšanos, pārdošanas punktā (POS) dodieties uz **Paplašinātā pieteikšanās**. Pēc tam meklējiet nodarbināto, meklēšanas laukā ievadot nodarbinātā operatora ID. Atlasiet strādnieka vārdu un pēc tam noklikšķiniet uz **Piešķirt**. Nākamajā lapā nolasiet vai skenējiet paplašinātās pieteikšanās karti, lai piešķirtu to strādniekam. Ja kartes nolasīšana vai skenēšana ir sekmīga, aktivizēta tiek poga **Labi**. Noklikšķiniet uz **Labi**, lai saglabātu darbinieka paplašinātās pieteikšanās tiesības.

## <a name="delete-extended-logon"></a>Dzēst paplašināto pieteikšanos

Lai dzēstu darbiniekam piešķirtās paplašinātās pieteikšanās tiesības, izmantojiet darbību **Paplašinātā pieteikšanās** un meklējiet darbinieku. Atlasiet darbinieka vārdu un pēc tam noklikšķiniet uz **Noņemt piešķirtās tiesības**. Visi ar šo lietotāju saistītie paplašinātās pieteikšanās akreditācijas dati tiek noņemti.

## <a name="use-extended-logon"></a>Lietot paplašināto pieteikšanos

Kad ir konfigurēta paplašinātā pieteikšanās un darbiniekam ir piešķirts svītrkods vai magnētiskā josla, darbiniekam ir tikai jāseko kartei un jāskenē sava karte, kamēr tiek parādīta POS pieteikšanās lapa. Ja pirms pieteikšanās ir nepieciešama arī parole, darbiniekam tiek parādīta uzvedne par paroles ievadi.

## <a name="extend-extended-logon"></a>Paplašinātā pieteikšanās

Lai ieviestu paplašinātās pieteikšanās iespēju, nepieciešams, lai akreditācijas datiem minimālais garums būtu sešas rakstzīmes un ka pirmās piecas rakstzīmes (akreditācijas datu ID) ir unikālas. Sākotnēji tas bija paredzēts kā paraugs, kuru izstrādātāji var pielāgot, lai atbilstu specifiskas ieviešanas prasībām. (Piemēram, tas var tikt pielāgots, lai atbalstītu vairāk rakstzīmju vai izmantotu dažādus drošības pārbaudes noteikumus.) Plašāku informāciju par to, kā veidot paplašinājumus paplašinātai pieteikšanās pieteikšanās, [skatiet Paplašinātās pieteikšanās funkcionalitātes paplašināšana MPOS un Cloud POS](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/).

Pieteikšanās pakalpojumu var paplašināt arī, lai atbalstītu papildu paplašinātās pieteikšanās ierīces, piemēram, palmu skenerus. Papildinformāciju skatiet [POS paplašināmības dokumentācijā](dev-itpro/pos-extension/pos-extension-overview.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
