---
title: "Definēt un pārvaldīt programmas priekšrocības"
description: "Personāla vadība sniedz rīkus, ko var izmantot, lai iestatītu un uzturētu atvieglojumus, atvilkumus un darbinieku kompensāciju plānus, kurus uzņēmums piedāvā vai apstrādā saviem darbiniekiem. Šis raksts sniedz informāciju par to, kā iestatīt pārvaldīt atvieglojumus."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 81b5c9056001b26c33b2b42a95711ff5b50243e6
ms.openlocfilehash: 9d00d8f6dfa075f53473af31c257deb57c9efa86
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-manage-a-benefits-program"></a>Definēt un pārvaldīt programmas priekšrocības

Personāla vadība sniedz rīkus, ko var izmantot, lai iestatītu un uzturētu atvieglojumus, atvilkumus un darbinieku kompensāciju plānus, kurus uzņēmums piedāvā vai apstrādā saviem darbiniekiem. Šajā tēmā ir sniegta informācija par to, kā iestatīt pārvaldīt priekšrocības.

<a name="benefit-setup"></a>Labumu iestatīšana
-------------

Pirms darbiniekiem var reģistrēt atvieglojumus, jāizveido katra atvieglojuma elementi. Šie elementi apvienot līdzīgus atvieglojumu plānus un nosaka noklusējuma iestatījumus, piemēram, ieturējumu likmes un informāciju par uzskaiti. Daudzus no šiem iestatījumiem var pielāgot, kad darbinieki tiek vēlāk reģistrēti atvieglojumiem. Katram atvieglojumu plānam organizācija var piedāvāt vairākas reģistrācijas opcijas, vai darbinieks var atteikties no reģistrācijas plānā. 

[![Labumu procesa gaitu](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Atvieglojumu elementi
Pirms sākat veidot atvieglojumus un reģistrēt tajos darbiniekus, ir jādefinē elementi, kas veido atvieglojumu: tips, plāns un opcijas.

-   **Tips** — plānu kopums konkrētiem atvieglojumiem, piemēram, ārstēšanai vai auto novietošanai.
-   **Plāns** — konkrēti atvieglojumi, kas saskaņā ar līgumu saņemti no nodrošinātāja.
-   **Opcija** — seguma līmenis, piemēram, atvieglojumi tikai darbiniekam vai darbiniekam un tā dzīvesbiedram/partnerim.

Katram atvieglojumu tipam, piemēram, redzes vai zobu, organizācija saviem darbiniekiem var piedāvāt vienu vai vairākus plānus. Katram plānam organizācija var piedāvāt dažādas opcijas. Piemēram, darbinieki var iegādāties papildu termiņa dzīvības apdrošināšanas segumu, kas vienu, divas vai trīs reizes pārsniedz gada algu. Katra plānu un opciju kombinācija kļūst par atvieglojumu, kuram darbinieki var reģistrēties. 

[![labumu pic](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Piemērojamība
Daudzi faktori ietekmē darbinieka atbilstību dažādiem atvieglojumu tipiem, kurus piedāvā darba devējs. Veidojot Microsoft Dynamics 365 operācijām labumu, varat iestatīt atbilstība, kas attiecas uz šā pabalsta veidu. 

Labumu var padarīt pieejamu visiem darba ņēmējiem. Piemēram, daži uzņēmumi piedāvā autostāvvietu iet visiem darbiniekiem kā papildienākumu. Veidojot šo atvieglojumu, iestatiet piemērojamību **Visi darbinieki ir piemēroti**. 

Attiecībā uz citiem pabalstiem, piemēram, izmaksu un nodokļu maksājumu atbilstību neattiecas. Sūkalu izveidot šāda veida pabalstus, jāiestata tiesības pretendēt uz **apiet atbilstības procesu**. 

Visbeidzot, ieguvumu atbilstību var būt kārtulas pamatā. Piemēram, uzņēmums piedāvā divu veidu dzīvības apdrošināšanas priekšrocības darbiniekiem. Izpildvaras darbinieki ir tiesīgi viena dzīvības apdrošināšanas plānu, tā kā citi pilna laika darbinieki ir tiesīgas saņemt citu dzīvības apdrošināšanas plānu. Programmā Dynamics 365 operācijām, var radīt labumu atbilstības kārtulu noskaidrot visiem izpildvaras darbiniekiem un cita kārtula jāatrod citi pilna laika darbinieki un pēc tam lietot šajos noteikumos attiecīgu labumu.

## <a name="enrollment"></a>Reģistrācija
Pēc tam, kad esat izveidojis uzņēmuma piedāvātos atvieglojumus un noteicis piemērojamību, varat reģistrēt jūsu darbiniekus atvieglojumiem. Varat reģistrēt atvieglojumam vienu darbinieku vai varat reģistrēt daudzus darbiniekus vienam vai vairākiem atvieglojumiem vienā procesā. 

Dažreiz organizācija pārtrauc piedāvāt noteiktus atvieglojumus. Šādā gadījumā jums ir jāatjaunina pabalsta un darba ņēmējiem, kuri ir uzņemti. Masveida pabalsta termiņa beigām ļauj mainīt beigu datums gan pabalstu, gan darbinieku iesaistīšanās šī pabalsta, tajā pašā laikā. Varat arī izvēlēties vairākus darbiniekus, kuri ir reģistrējušies atvieglojumiem, un mainīt seguma beigu datumu. 

Līdzīgi, masveida atvieglojumu pagarināšana ļauj pagarināt atvieglojumu un darbinieku reģistrēšanās beigu datumu šim atvieglojumam, ja nolemjat piedāvāt atvieglojumu ilgāk nekā sākotnēji plānots.

<a name="see-also"></a>Skatiet arī
--------

[Benefit eligibility policies](benefit-eligibility-policies.md)


