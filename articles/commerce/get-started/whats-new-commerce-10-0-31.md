---
title: Dynamics 365 Commerce 10.0.31 priekšskatījums (2023. gada februāris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni vai mainīti programmā Microsoft Dynamics 365 Commerce 10.0.31.
author: josaw1
ms.date: 10/18/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-10-01
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 05ccd9794ffeba6a09d6fec0a57ffad2b59707ad
ms.sourcegitcommit: 87e75aa6af2c3280316d7d73eafa14a52353a5e4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/21/2022
ms.locfileid: "9709873"
---
# <a name="preview-of-dynamics-365-commerce-10031-february-2023"></a>Dynamics 365 Commerce 10.0.31 priekšskatījums (2023. gada februāris)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā rakstā ir uzskaitīti līdzekļi, kas ir jauni vai mainīti priekšskatījuma Microsoft Dynamics 365 Commerce versijā 10.0.31. Šai versijai ir ražošanas numuru 10.0.1406 un tā ir pieejama šajā grafikā:

- **Laidiena priekšskatījums:** 2022. gada oktobris
- **Vispārēja laidiena (paša veikts atjauninājums) pieejamība:** 2023. gada janvāris
- **Vispārēja laidiena (automātisks atjauninājums) pieejamība:** 2023. gada februāris

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Mēs varētu atjaunināt šo rakstu, lai ietvertu līdzekļus, kas tika pievienoti būvējumam pēc šī raksta sākotnējās publicēšanas.

| Līdzekļu apgabals | Līdzeklis | Papildinformācija | Iespējoja: |
|---|---|---|---|
| Kļūdu kodi | Commerce ieviestas standartizētas kļūdu atsauces, kas jāietver tiešsaistes kanāla pārbaudes kļūdās, kas iesniegtas tiešsaistes veikalam.| [Pārbaudes moduļa kļūdu kodi](../checkout-module-error-codes.md)  | Ieslēgts pēc noklusējuma |
| Maksājumi | [Iespējojiet Saņemšanas apmaksu, izmantojot Dynamics 365 maksājumu savienotāju Aādēnei](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-apple-pay-dynamics-365-payment-connector-adyen)  | E-komercijas debitori var izmantot Algu par grozu un norēķināšanas lapas, izmantojot atbalstītās ierīces vai pārlūkprogrammas. | Izstrādātāja pieteikšanās |
| Maksājumi  |  Commerce pievienoja iespēju ierobežot lietotāju mijiedarbošanās ar periodiskām maksājumu žetoniem programmas Commerce Headquarters lietotāja interfeisā. Maksājumu formas, piemēram **, lapa Zvanu** centra pārdošanas pasūtījums, vairs nerāda debitora iepriekš izmantotā periodiskā maksājuma marķieri izmantošanai jaunā darbībā. Tikai noteikta karte failā, kas tiek ievadīta Commerce **Customer Payments** ekrānā vai vienošanās ar debitoru, veicot maksājumu ar pārdošanas pasūtījumu, tiks iesniegta zvanu centram vai Commerce Headquarters lietotājiem, apstrādājot maksājumu jaunai darbībai. | [Ierobežot maksājuma marķiera izmantošanu](../dev-itpro/limit-token-usage.md)  |  Līdzekļu pārvaldība<p>*Ierobežot maksājuma marķiera izmantošanu pasūtījuma kontekstā*  |
| POS | [Izveidot pirkšanas pasūtījumus no POS](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/create-purchase-orders-pos)  |  Uzlabota saņemšanas krājumu operācija pārdošanas punktā (POS), lai ļautu lietotājiem izveidot, rediģēt un apstiprināt pirkšanas pasūtījumu pieprasījumus. |  Līdzekļu pārvaldība<p>*Iespēja izveidot pirkšanas pasūtījuma pieprasījumu POS*   |



## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi finanšu un operāciju programmām

Microsoft Dynamics 365 Commerce 10.0.31 ietver platformas atjauninājumus. Lai uzzinātu vairāk, skatiet [Informāciju par Platformas atjauninājumiem finanšu un operāciju programmu versijā 10.0.31 (2023. gada februāris](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-31.md)). 
  

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas ietverti katrā atjauninājumā, kas ir daļa no versijas 10.0.31, Microsoft Dynamics piesakieties lifecycle Services un skatiet [zināšanu bāzes rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 un rūpniecības mākoņi: 2022. gada 2. laidiena plāns

Vai interesējaties par gaidāmajām un nesen izlaistajām biznesa programmu un platformu iespējām?

Apskatiet [Dynamics 365 un rūpniecības mākoņi: 2022. gada 2. laidiena plāns](/dynamics365-release-plan/2022wave2/). Visa informācija no “a” līdz “z” ir apkopota vienā dokumentā, kuru varat izmantot plānošanai.

### <a name="removed-and-deprecated-commerce-features"></a>Noņemtie un novecojušie Commerce līdzekļi

Noņemtie [vai novecojušie līdzekļi rakstu Dynamics 365 Commerce](removed-deprecated-features-commerce.md) ir aprakstīti līdzekļi, kas ir noņemti vai novecojuši attiecībā uz Commerce.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Pirms kāda līdzekļa noņemšanas no preces paziņojums [Dynamics 365 Commerce](removed-deprecated-features-commerce.md) par nolietojumu tiks papildu pievienots 12. rakstu funkcionalitātes Noņemtie vai novecojušie 12 mēnešu skaits pirms noņemšanas.


Lai pārveidotu izmaiņas, kas ietekmē tikai apkopošanas laiks, bet ir bināri saderīgas ar smilškastes un ražošanas vidēm, izslēgšanas laiks būs īsāks par 12 mēnešiem. Parasti tie ir funkcionāli atjauninājumi, kas jāveic apkopotājam.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
