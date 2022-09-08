---
title: Pakalpojuma Dynamics 365 Commerce priekšskatījums 10.0.30 (2022. gada novembris)
description: Šajā rakstā ir aprakstītas funkcijas, kas ir jaunas vai mainītas Microsoft Dynamics 365 Commerce programmā 10.0.30.
author: josaw1
ms.date: 08/31/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-09-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 0149c9671e8baeb26965b4f136ed91d09e2d039b
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405522"
---
# <a name="preview-of-dynamics-365-commerce-10030-november-2022"></a>Pakalpojuma Dynamics 365 Commerce priekšskatījums 10.0.30 (2022. gada novembris)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā rakstā ir uzskaitīti līdzekļi, kas ir jauni vai mainīti priekšskatījuma Microsoft Dynamics 365 Commerce versijā 10.0.30. Šai versijai ir ražošanas numuru 10.0.1362 un tā ir pieejama šajā grafikā:

- **Laidiena priekšskatījums:** 2022. gada septembris
- **Vispārēja laidiena (pašatjaunināšana) pieejamība:** 2022. gada oktobris
- **Vispārēja laidiena (automātiskā atjaunināšana) pieejamība:** 2022. gada novembris

## <a name="features-included-in-this-release"></a>Šajā laidienā iekļautie līdzekļi

Šajā tabulā ir uzskaitīti šajā laidienā iekļautie līdzekļi. Mēs varētu atjaunināt šo rakstu, lai ietvertu līdzekļus, kas tika pievienoti būvējumam pēc šī raksta sākotnējās publicēšanas.

| Līdzekļu apgabals | Līdzeklis | Papildinformācija | Iespējoja: |
|---------|------------------|----------------|--------------| 
| Klientu atbalsts   | Tērzēšanu e-komercijas vietnē, izmantojot botu Power Virtual Agents. | Šī funkcija dos e-commerce vietnes lietotājiem iespēju izmantot tērzētavas Power Virtual Agents botu atbalsta pieprasījumiem. | Aktivizē administratori/veidotāji gala lietotājiem |
| Ieskati  |  Plūsmas pārdošanas punkta (POS) operāciju ieskatu notikumi jūsu kontā Application Insights. | [Piekļuve žurnāliem Application Insights](../dev-itpro/retail-component-events-diagnostics-troubleshooting.md#enable-diagnostic-events-in-application-insights)   |  IT pro/izstrādātāja pieteikšanās   |
|  Maksājumi  | PayPal pasūtījuma atbalsts pēc 29 dienu autorizācijas perioda. | Maksimālais PayPal autorizācijas periods ir 29 dienas, pēc kurām jāģenerē jauns autorizācijas un pasūtījuma ID. Kā alternatīvu PayPal piedāvā opciju, kur pasūtījumam PayPal pasūtījumu var norādīt kā vispārēju pasūtījumu, kas atļauj vairākas autorizācijas un notvertas attiecībā pret vienu un to pašu pasūtījuma ID, tā vietā, lai ģenerētu jaunu autorizāciju un pasūtījuma ID 29 dienu laikā). | Konfigurējot PayPal maksājumu savienotāju programmā Commerce Headquarters, lauks **OrderIntent ir** pievienots, un tam var būt divas vērtības:<p><p>- **Autorizēt** - šī konfigurācija ir noklusējuma (ja lauks ir atstāts tukšs, **Autorizēt** darbosies kā noklusējums). **OrderIntent konfigurēšana** autorizējot **korelātus** ar PayPal **processing_instruction** vērtību **NO_INSTRUCTION**. Pasūtījums tiks autorizēts ar PayPal, un autorizāciju nevar modificēt, ja tiks izmantota šī vērtība.<p>- **Saglabāt** - kad **OrderIntent vērtība** ir iestatīta uz **Saglabāt**, šī korelācija ir ar PayPal **processing_instruction** vērtību **ORDER_SAVED_EXPLICITLY**. Pasūtījuma atsauces tiks saglabātas PayPal pakalpojumā, kad šī vērtība tiks izmantota.  |
| POS pierakstīšanās  | [Iespējot pašapkalpošanās diagnozes iespējas POS pierakstīšanās laikā](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-self-serve-diagnosis-capabilities-pos-sign-in)  |  Šī funkcija pārdošanas punktā (POS) un programmā Commerce headquarters nodrošina pašapkalpošanās diagnozes iespējas, lai palīdzētu veikala darbiniekiem un pārvaldniekiem ātri identificēt un labot POS pierakstīšanās problēmu cēloņus.<p><p>- POS pierakstīšanās ekrānā parādītie kļūmes ziņojumi tika uzlaboti, lai sniegtu noteiktu saknes iemeslu informāciju, kas var palīdzēt saglabāt darbiniekus, kuri izmanto POS, saprast, kas radās nepareizi, lai varētu veikt nepieciešamās darbības problēmas atrisināšanai.<p>— Testa **pieteikšanās funkcija** ir pieejama **Commerce** Headquarters lapā Darbinieki, lai veikala vadītāji, kas iestata POS ierīces, varētu simulēt POS pieteikšanos. Pierakstīšanās kļūmes gadījumā šī funkcija sniedz darbību traucējummeklēšanas ceļvežus, lai vadītāji varētu pārbaudīt atbilstošas konfigurācijas, labot problēmas un validēt labojumus.  | Ieslēgts pēc noklusējuma |


## <a name="additional-resources"></a>Papildu resursi

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformas atjauninājumi finanšu un operāciju programmām

Dynamics 365 Finanses 10.0.30 ietver platformu atjauninājumus. Lai uzzinātu vairāk, skatiet [Informāciju par Platformas atjauninājumiem finanšu un operāciju programmu versijā 10.0.30](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>Kļūdu labojumi

Lai iegūtu informāciju par kļūdu labojumiem, kas ietverti katrā atjauninājumā, kas ir daļa no versijas 10.0.30, piesakieties lifecycle Services (LCS) [un skatiet zināšanu bāzes rakstu](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 un rūpniecības mākoņi: 2022. gada 2. laidiena plāns

Vai interesējaties par gaidāmajām un nesen izlaistajām biznesa programmu un platformu iespējām?

Apskatiet [Dynamics 365 un rūpniecības mākoņi: 2022. gada 2. laidiena plāns](/dynamics365-release-plan/2022wave2/). Visa informācija no “a” līdz “z” ir apkopota vienā dokumentā, kuru varat izmantot plānošanai.

### <a name="removed-and-deprecated-features"></a>Noņemtie un novecojušie līdzekļi

Noņemtie [vai novecojušie līdzekļi rakstu Dynamics 365 Commerce](removed-deprecated-features-commerce.md) ir aprakstīti līdzekļi, kas ir noņemti vai novecojuši attiecībā uz Commerce.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Pirms kāda līdzekļa noņemšanas no preces paziņojums [Dynamics 365 Commerce](removed-deprecated-features-commerce.md) par nolietojumu tiks papildu pievienots 12. rakstu funkcionalitātes Noņemtie vai novecojušie 12 mēnešu skaits pirms noņemšanas.

Lai pārveidotu izmaiņas, kas ietekmē tikai apkopošanas laiks, bet ir bināri saderīgas ar smilškastes un ražošanas vidēm, izslēgšanas laiks būs īsāks par 12 mēnešiem. Parasti tie ir funkcionāli atjauninājumi, kas jāveic apkopotājam.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
