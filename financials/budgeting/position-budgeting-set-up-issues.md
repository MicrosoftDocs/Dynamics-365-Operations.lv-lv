---
title: "Pozīciju budžeta izveides problēmu novēršana"
description: "Šajā raksta ir sniegtas atbildes uz jautājumiem, kas var rasties budžeta veidošanas pozīciju konfigurēšanas gaitā. Tēma atsaucas uz biežāk uzdotajiem jautājumiem par to, kā izveidot budžeta izmaksu elementus, atlīdzību grupas un atlīdzību režģus."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c3fe1e1842b1cd808d35105ec7ec494107127690
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017

---

# <a name="position-budgeting-troubleshooting"></a>Pozīciju budžeta izveides problēmu novēršana

[!include[banner](../includes/banner.md)]


Šajā raksta ir sniegtas atbildes uz jautājumiem, kas var rasties budžeta veidošanas pozīciju konfigurēšanas gaitā. Tēma atsaucas uz biežāk uzdotajiem jautājumiem par to, kā izveidot budžeta izmaksu elementus, atlīdzību grupas un atlīdzību režģus. 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a>Kāpēc nevar atrast prognozes pozīciju lapā Personāla vadība?
---------------------------------------------------------------

Prognožu pozīcijas ir pārvietotas uz lapu Budžeta veidošana.

## <a name="why-cant-i-delete-a-budget-cost-element"></a>Kāpēc es nevaru izdzēst budžeta izmaksu elementu?
Jūs nevarat dzēst budžeta izmaksu elementu, kas ir piešķirts prognožu pozīcijai. Lai varētu izdzēst budžeta izmaksu elementu, tas vispirms ir jānoņem visās prognožu pozīcijās. **Padoms.** Lai varētu atrast visas pozīcijas, kurām ir piešķirts budžeta izmaksu elements, atlasiet izmaksu elementu lapā **Budžeta izmaksu elementi** un pēc tam noklikšķiniet uz **Atjaunināt pozīcijas**. Pozīcijas, kuras izmantoto izmaksu elementu, ir uzskaitītas augšējā režģī.

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a>Kā var noņemt izmaksu elementu vairākās budžeta pozīcijās, neatverot tās katru atsevišķi?
Izmaksu elementu nevar noņemt. Tomēr, ja tiek mainīts sākuma un beigu datums tā, tie būtu ārpus budžeta plānošanas cikla, izmaksu elements vairs netiek piešķirts prognožu pozīcijām budžeta plānošanas ciklā. Lai varētu veikt šādas izmaiņas, atveriet budžeta izmaksu elementu un pēc tam kopsavilkuma cilnē **Izmaksu aprēķināšana** noklikšķiniet uz **Mainīt datumus** un mainiet spēkā stāšanās vai beigu datumu. Pēc tam noklikšķiniet uz **Labi**, lai automātiski atjaunina visas prognozes pozīcijas, kurām ir piešķirts izmaksu elements. **Padoms.** Ja tiek izmantota šī metode, ņemiet vērā, ka tādējādi budžeta izmaksu elements tiek noņemts **visās** prognožu pozīcijās, kuru sākuma un beigu datums vairs nav atbilstošajā diapazonā. Ja to nevēlaties, katra prognozes pozīcija, kurai vēlaties noņemt budžeta izmaksu elementu, ir jāatver atsevišķi un jāveic izmaiņas manuāli.

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a>Kāpēc nevar ievadīt budžeta izmaksu elementa gada summu kopsavilkuma cilnē Izmaksu aprēķināšana?
Gada summu nevar ievadīt, ja kopsavilkuma cilnē **Aprēķina bāze** ir budžeta izmaksu elementi, jo, lai varētu aprēķināt vērtību, sistēmā ir nepieciešama procentuālā vērtība. Lai mainītu vērtību, noņemiet visus budžeta izmaksu elementus kopsavilkuma cilnē **Aprēķina bāze**.

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a>Kāpēc nevar izmainīt budžeta izmaksu veidu Ienākums uz citu budžeta izmaksu veidu?
Daži budžeta izmaksu elementi izmanto izmaksu elementu Ienākums kā aprēķinu bāzi. Lai mainītu vērtību laukā **Budžeta izmaksu veids**, noņemiet ieņēmumu izmaksu elementu kopsavilkuma cilnē **Aprēķina bāze** visiem budžeta izmaksu elementiem.

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a>Kāpēc es nevaru mainīt datumu budžeta izmaksu elementu rindās budžeta izmaksu elementam?
Ja budžeta izmaksu elements ir izmantots prognozes pozīcijā, budžeta izmaksu elementa rindā nevar mainīt datumu. Šis ierobežojums nodrošina, ka prognožu pozīcijas vienmēr atbilst budžeta izmaksu elementa vadlīnijām. Lai mainītu datumu, kopsavilkuma cilnē **Izmaksu aprēķināšana** noklikšķiniet uz **Mainīt datumu** un ievadiet jaunu datumu. Pēc tam noklikšķiniet uz **Labi**, lai atjaunina pozīcijas, kurām ir piešķirts izmaksu elements.

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a>Kāpēc nevar mainīt budžeta izmaksu elementa izmaksas lapā Atlīdzības grupa?
Budžeta izmaksu elementus var izveidot un mainīt tikai lapā **Budžeta izmaksu elementi**.

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a>Kāpēc, mainot izmaksu elementa datumu prognozes pozīcijā, tiek parādīts kļūdas ziņojums?
Prognozes pozīcijas izmaksu elementa rindas datumiem jābūt tālāk norādītajās robežās.

-   Pozīcijas aktivizēšanas un norakstīšanas datums.
-   Budžeta izmaksu elementa aktivizēšanas un beigu datums.
-   Budžeta cikla sākuma un beigu datums, kas ir saistīts ar prognozes pozīcijas budžeta plānošanas procesu.





