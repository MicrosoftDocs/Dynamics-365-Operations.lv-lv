---
title: Paplašinātās pieteikšanās funkcionalitātes iestatīšana pārdošanas punktiem MPOS un Cloud POS
description: Šajā tēmā ir aprakstītas Cloud POS un Retail Modern POS (MPOS) paplašinātās pieteikšanās iestatīšanas iespējas.
author: rubencdelgado
ms.date: 06/20/2017
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
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f9d8889581e2e11fa5261805c866a6014df57611
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027580"
---
# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a>Paplašinātās pieteikšanās funkcionalitātes iestatīšana MPOS un Cloud POS

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstītas Cloud POS un Retail Modern POS (MPOS) paplašinātās pieteikšanās iestatīšanas iespējas.

## <a name="setting-up-extended-logon"></a>Paplašinātās pieteikšanās iestatīšana

Svītrkoda masku iestatījumi ir pieejami, izmantojot šādu ceļu: **Mazumtirdzniecība un komercija** &gt; **Kanāla iestatījumi** &gt; **POS iestatījumi** &gt; **POS profili** &gt; **Funkcionalitātes profili**. Kopsavilkuma cilnē **Funkcijas** ir iekļautas tālāk norādītās opcijas, kas ir saistītas ar paplašināto pieteikšanos.

### <a name="staff-bar-code-logon"></a>Personāla pieteikšanās ar svītrkodu

Ja ir iespējota opcija **Personāla pieteikšanās ar svītrkodu**, darbinieki, kuru pārdošanas punkta (POS) akreditācijas datiem ir piešķirtas paplašinātās pieteikšanās tiesības, var pieteikties, izmantojot svītrkodu.

### <a name="staff-bar-code-logon-requires-password"></a>Darbinieku pieteikumam ar svītrkodu nepieciešama parole

Ja ir iespējota opcija **Personāla pieteikšanās ar svītrkodu jāpapildina ar paroli**, personāla pieteikšanās ar svītrkodu laikā tiek atlasīts tikai tas darbinieks, kam ir piešķirtas paplašinātās pieteikšanās tiesības, kas tiek apliecinātas. Ja šī opcija ir iespējota, darbiniekiem tomēr jāievada parole.

### <a name="staff-card-logon"></a>Personāla pieteikšanās ar karti

Ja ir iespējota opcija **Personāla pieteikšanās ar karti**, darbinieki, kuru POS akreditācijas datos ir piešķirtas paplašinātās pieteikšanās tiesības, var pieteikties, izmantojot magnētisko karti.

### <a name="staff-card-logon-requires-password"></a>Darbinieku pieteikumam ar karti nepieciešama parole

Ja ir iespējota opcija **Personāla pieteikšanās ar karti jāpapildina ar paroli**, kad personāls piesakās, izmantojot karti, tiek atlasīts tikai tas darbinieks, kam ir piešķirtas paplašinātās pieteikšanās tiesības, kas tiek apliecinātas. Ja šī opcija ir iespējota, darbiniekiem tomēr jāievada parole.

## <a name="assigning-an-extended-logon"></a>Paplašinātās pieteikšanās tiesību piešķiršana

Pēc noklusējuma paplašinātās pieteikšanās tiesības strādniekiem var piešķirt tikai vadītāji. Lai piešķirtu paplašināto pieteikšanos, pārdošanas punktā (POS) dodieties uz **Paplašinātā pieteikšanās**. Pēc tam meklējiet nodarbināto, meklēšanas laukā ievadot nodarbinātā operatora ID. Atlasiet strādnieka vārdu un pēc tam noklikšķiniet uz **Piešķirt**. Nākamajā lapā nolasiet vai skenējiet paplašinātās pieteikšanās karti, lai piešķirtu to strādniekam. Ja kartes nolasīšana vai skenēšana ir sekmīga, aktivizēta tiek poga **Labi**. Noklikšķiniet uz **Labi**, lai saglabātu darbinieka paplašinātās pieteikšanās tiesības.

## <a name="deleting-an-extended-logon"></a>Paplašinātās pieteikšanās tiesību dzēšana

Lai dzēstu darbiniekam piešķirtās paplašinātās pieteikšanās tiesības, izmantojiet darbību **Paplašinātā pieteikšanās** un meklējiet darbinieku. Atlasiet darbinieka vārdu un pēc tam noklikšķiniet uz **Noņemt piešķirtās tiesības**. Visi ar šo lietotāju saistītie paplašinātās pieteikšanās akreditācijas dati tiek noņemti.

## <a name="extending-extended-logon"></a>Paplašinātās pieteikšanās tiesību paplašināšana

Pieteikšanās pakalpojumu var paplašināt, lai atbalstītu papildu paplašinātās pieteikšanās ierīces, piemēra, plaukstas skenerus. Lai iegūtu papildinformāciju, skatiet POS dokumentāciju par paplašināšanas iespējām.

## <a name="using-extended-logon"></a>Paplašinātās pieteikšanās tiesību izmantošana

Ja paplašinātā pieteikšanās opcija ir konfigurēta un darbiniekam ir piešķirts svītrkods un magnētiskā karte, darbiniekam ir tikai jānolasa vai jānoskenē karte, kamēr ir atvērta POS pieteikšanās lapa. Ja pirms pieteikšanās turpināšanas ir jāievada arī parole, darbiniekam tiek parādīta uzvedne ievadīt savu parole.


[!INCLUDE[footer-include](../includes/footer-banner.md)]