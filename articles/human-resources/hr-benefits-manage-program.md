---
title: Atvieglojumu programmas definēšana un pārvaldība
description: Personāla vadība sniedz rīkus, ko var izmantot, lai iestatītu un uzturētu atvieglojumus, atvilkumus un darbinieku kompensāciju plānus, kurus uzņēmums piedāvā vai apstrādā saviem darbiniekiem. Šis raksts sniedz informāciju par to, kā iestatīt un pārvaldīt atvieglojumus.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 08b80f4f90ce6b4a286120cd6329a45a4ebd3f71
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877806"
---
# <a name="define-and-manage-a-benefits-program"></a>Atvieglojumu programmas definēšana un pārvaldība


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Personāla vadība sniedz rīkus, ko var izmantot, lai iestatītu un uzturētu atvieglojumus, atvilkumus un darbinieku kompensāciju plānus, kurus uzņēmums piedāvā vai apstrādā saviem darbiniekiem. Šis raksts sniedz informāciju par to, kā iestatīt un pārvaldīt atvieglojumus.

## <a name="benefit-setup"></a>Atvieglojumu iestatīšana

Pirms darbiniekiem var reģistrēt atvieglojumus, jāizveido katra atvieglojuma elementi. Šie elementi apvienot līdzīgus atvieglojumu plānus un nosaka noklusējuma iestatījumus, piemēram, ieturējumu likmes un informāciju par uzskaiti. Daudzus no šiem iestatījumiem var pielāgot, kad darbinieki tiek vēlāk reģistrēti atvieglojumiem. Katram atvieglojumu plānam organizācija var piedāvāt vairākas reģistrācijas opcijas, vai darbinieks var atteikties no reģistrācijas plānā. 

[![Atvieglojumu procesa plūsma.](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Atvieglojumu elementi

Pirms sākat veidot atvieglojumus un reģistrēt tajos darbiniekus, ir jādefinē elementi, kas veido atvieglojumu: veids, plāns un opcijas.

-   **Tips** — plānu kopums konkrētiem atvieglojumiem, piemēram, ārstēšanai vai auto novietošanai.
-   **Plāns** — konkrēti atvieglojumi, kas saskaņā ar līgumu saņemti no nodrošinātāja.
-   **Opcija** — seguma līmenis, piemēram, atvieglojumi tikai darbiniekam vai darbiniekam un tā dzīvesbiedram/partnerim.

Katram atvieglojumu tipam, piemēram, redzes vai zobu, organizācija saviem darbiniekiem var piedāvāt vienu vai vairākus plānus. Katram plānam organizācija var piedāvāt dažādas opcijas. Piemēram, darbinieki var iegādāties papildu termiņa dzīvības apdrošināšanas segumu, kas vienu, divas vai trīs reizes pārsniedz gada algu. Katra plānu un opciju kombinācija kļūst par atvieglojumu, kuram darbinieki var reģistrēties. 

[![Atvieglojumu attēls.](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Piemērojamība
Daudzi faktori ietekmē darbinieka atbilstību dažādiem atvieglojumu tipiem, kurus piedāvā darba devējs. Kad veidojat atvieglojumu Dynamics 365 Human Resources, varat iestatīt piemērojamības tipu, kas attiecas uz šo atvieglojumu. 

Varat padarīt atvieglojumu pieejamu visiem nodarbinātajiem. Piemēram, daži uzņēmumi kā papildienākumu piedāvā visiem darbiniekiem stāvvietas caurlaides. Veidojot šo atvieglojumu, iestatiet piemērojamību **Visi darbinieki ir piemēroti**. 

Piemērotība neattiecas uz citiem atvieglojumiem, piemēram, ieturējumiem un nodokļu maksājumiem. Izveidojot šo veidu atvieglojumus, ir jāiestata piemērotības opcija **Apiet piemērojamības procesu**. 

Turklāt atvieglojumu piemērotība var būt atkarīga no kārtulām. Piemēram, uzņēmums piedāvā darbiniekiem divu veidu dzīvības apdrošināšanas atvieglojumus. Vadošie darbinieki var saņemt vienu dzīvības apdrošināšanas plānu, bet visi citi pilna laika darbinieki var saņemt citu dzīvības apdrošināšanas plānu. Human Resources varat izveidot atvieglojumu piemērotības kārtulu, lai atrastu visus vadošos darbiniekus, un citu kārtulu, lai atrastu visus citus pilna laika darbiniekus, un pēc tam varat lietot šīs kārtulas atbilstošajiem atvieglojumiem.

## <a name="enrollment"></a>Reģistrācija
Pēc tam, kad esat izveidojis uzņēmuma piedāvātos atvieglojumus un noteicis piemērojamību, varat reģistrēt jūsu darbiniekus atvieglojumiem. Varat reģistrēt atvieglojumam vienu darbinieku vai varat reģistrēt daudzus darbiniekus vienam vai vairākiem atvieglojumiem vienā procesā. 

Dažreiz organizācija pārtrauc piedāvāt noteiktus atvieglojumus. Šādā gadījumā ir jāatjaunina atvieglojumi un nodarbinātie, kuri ir reģistrēti to saņemšanai. Opcija Masveida atvieglojuma piemērošanas beigas sniedz iespēju vienlaikus mainīt gan atvieglojumu nodrošināšanas, gan nodarbināto reģistrācijas šo atvieglojumu saņemšanai beigu datumu. Varat arī izvēlēties vairākus darbiniekus, kuri ir reģistrējušies atvieglojumiem, un mainīt seguma beigu datumu. 

Līdzīgi, masveida atvieglojumu pagarināšana ļauj pagarināt atvieglojumu un darbinieku reģistrēšanās beigu datumu šim atvieglojumam, ja nolemjat piedāvāt atvieglojumu ilgāk nekā sākotnēji plānots.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
