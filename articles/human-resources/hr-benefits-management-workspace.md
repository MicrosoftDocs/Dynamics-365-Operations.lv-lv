---
title: Atvieglojumu pārvaldības darbvieta
description: 'Šajā rakstā ir aprakstīta atvieglojumu pārvaldības darbvieta šeit: Dynamics 365 Human Resources.'
author: twheeloc
ms.date: 01/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7975d1723e07ae390961d4f44e0f34f2ff2df44d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902923"
---
# <a name="benefits-management-workspace"></a>Atvieglojumu pārvaldības darbvieta


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [applies to](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

Šajā rakstā ir aprakstīta atvieglojumu **pārvaldības darbvieta** šeit: Dynamics 365 Human Resources.

> [!NOTE]
> Lai skatītu **Atvieglojumu pārvaldības** darbvietu, Līdzekļa pārvaldībā vispirms ir jāiespējo līdzeklis **(Priekšskatījums) Atvieglojumu pārvaldības** darbvieta. Lai iegūtu papildinformāciju par priekšskatījuma līdzekļu iespējošanu, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).<br><br>![Atvieglojumu pārvaldības darbvietas iespējošana.](./media/hr-benefits-management-workspace-enable.png)

**Atvieglojumu pārvaldības** darbvieta ļauj jums ātri skatīt atvieglojumu krājumus, kam ir nepieciešama jūsu uzmanība. Šajā lapa var redzēt:

- Kopsummas krājumiem, kas gaida darbību
- Darbinieki ar neapstiprināto atlasi
- Darbinieki, kas nesen reģistrējās atvieglojumiem
- Darbinieki ar nākotnes dzīves notikumiem
- Jaunas nolīgšanas, kas nav reģistrētas
- Darbinieki ar aktīviem notikumiem dzīvē
- Darbinieki ar atvērtām reģistrācijām, kuri nav izvēlējies nevienu plānu

![Atvieglojumu pārvaldības darbvieta.](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a>Skatīt darbības elementus

Darbību elementus varat skatīt, atlasot elementu vai cilni. Atlasot cilni, var skatīt un atlasīt darbiniekus tieši no darbvietas lapas.

![Darbības elementi.](./media/hr-benefits-management-workspace-action-items.png)

Ja atlasāt elementu, dodieties uz šī apgabala lapu. Piemēram, atlasot jebkuru no šiem informācija, tiek parādīta lapa **Darbinieka atvieglojumu plāni**, kas filtrēti darbiniekiem, par kuriem jāpieņem lēmums:

- **Neapstiprinātā atlase**
- **Atvērt reģistrācijas bez neapstiprināšanas plāniem**
- **Reģistrēts atvieglojumiem**
- **Jauna darbā pieņemšana nav reģistrēta**

![Nodarbināto atvieglojumu plāni.](./media/hr-benefits-management-workspace-plans.png)

Atlasot **Aktīvos dzīves notikumus** vai **Turpmākos dzīves notikumus**, jums tiek parādīts aktīvo vai nākotnes dzīves notikumu saraksts.

![Dzīves notikumi.](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a>Notiek apstrāde

Lai apstrādātu reģistrēšanas piemērotību, dzīves notikumus vai likmes maiņas atjauninājumus, atlasiet attiecīgo krājumu navigācijas joslā.

![Notiek apstrāde.](./media/hr-benefits-management-workspace-processing.png)

Lai skatītu apstrādes rezultātus, atlasiet lapā **Procesa rezultāti**.

![Procesa rezultāti.](./media/hr-benefits-management-workspace-process-results.png)

Plašāku informāciju par atvieglojumu apstrādi skatiet:

- [Procesa reģistrācijas piemērojamība](hr-benefits-process-enrollment-eligibility.md)
- [Apstrādāt dzīves notikumu izmaiņas](hr-benefits-process-life-event-changes.md)
- [Apstrādāt dzīves notikumu piemērotību](hr-benefits-process-life-event-eligibility.md)
- [Apstrādāt dzīves notikumus](hr-benefits-process-life-events.md)
- [Apstrādāt likmju izmaiņas](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a>Mainīt periodu

Lai skatītu citu atvieglojumu periodu, atlasiet to no nolaižamā saraksta **Periods**.

![Mainīt periodu.](./media/hr-benefits-management-workspace-period.png)


## <a name="open-enrollment-tab"></a>Atvērt reģistrācijas cilni

Darbību elementus varat skatīt, atlasot elementu vai cilni. Atlasot cilni, var skatīt un atlasīt darbiniekus tieši darbvietas lapā.
Cilne **Atvērt reģistrēšanu** nodrošina galvenos rādītājus atvērtam reģistrācijas procesam. 

Informācija par atvērto reģistrāciju tiks parādīta 30 dienas pirms **Reģistrācijas sākuma datuma**. Tas ir definēts **Periodu** iestatījumu **Atvieglojumu pārvaldība** > **Saites** > **Periodi** laukā **Reģistrācijas sākuma datums**.  Lai mainītu šo iestatījumu, pārejiet uz sadaļu **Cilvēkresursu kopīgie parametri** > **Atvieglojumu** > **pārvaldība Atveriet reģistrācijas opcijas** un atjauniniet **lauku** Skaits.  

Cilnē **Atvērt reģistrāciju** ir pieejama šāda informācija:
 - Darbinieki, kas nav sākuši atvērtās reģistrācijas procesu
 - Darbinieki, kas atrodas procesā
 - Darbinieki, kas ir pabeiguši procesu
 - Neapstiprinātā atlase

**Kopsavilkuma elementi**

- **Nav sākts** – elements **Nav sākts** parāda to darbinieku skaitu, kuri nav sākuši reģistrēšanās procesu. Elements **Nav sākts** ir filtrēts saraksts, kurā ir redzami tikai tie darbinieki, kuriem nav neviena plāna, kas nav atlasīti, atcelti vai paņemti atvērtam reģistrācijas plāna periodam. Obligātie plāni tiek ignorēti un nav iekļauti, jo tie pēc noklusējuma ir atlasīti darbiniekam.  Varat rakties šajā elementā, lai skatītu to darbinieku sarakstu, kuri nav sākuši atvērto reģistrācijas procesu **Darbinieka atvieglojumu plāna** lapā.

  > [!NOTE]
  > Ja nevēlaties izsekot **Plāna veidam** atvērto reģistrācijas norisi, varat to izslēgt, atverot **Atvieglojumu pārvaldība** > **Saites** > **Darbinieku pašapkalpošanās parametri** > **Atvieglojumu plānu iestatījumi** un atjauninot lauku **Izsekot atvērtās reģistrācijas progresu**.  Piemēram, var izveidot plānus, kur **Plāna tips** = **Cits**. Šie plāni var būt izvēles plāni, kuriem nevēlaties izsekot reģistrācijas progresu. Ja neatlasot šo plāna tipu, šo tipu plāni tiks ignorēti, izsekojot reģistrācijas norisi vai pabeidzot to cilnē **Atvērt reģistrāciju**. Šis iestatījums attiecas uz plāna tipu, kas atlasīts visiem periodiem un juridiskajām personām.

- **Notiek** – elements **Notiek** sniedz darbinieku skaitu, kuri ir procesā. Elements **Notiek** ir filtrēts saraksts, kurā ir redzami tikai darbinieki, kuriem ir vismaz viens plāns, kas ir atcelts vai atlasīts. Obligātie plāni tiek ignorēti un nav iekļauti, jo tie pēc noklusējuma ir atlasīti darbiniekam. Varat veikt detalizētu informāciju no šī elementa, lai skatītu atlasītos un atceltos plānus darbinieku **atvieglojumu plānu lielapjoma atjaunināšanas** lapā.

- **Reģistrēts atvieglojumos** – elements **Reģistrēts atvieglojumos** sniedz to darbinieku skaitu, kas ir pilnībā reģistrēti atvieglojumiem. Elements **Reģistrēts atvieglojumos** ir filtrēts saraksts, kurā ir redzami darbinieki, kuri ir atlasījuši vai atcēluši visus plānus. Vaicājums izslēdz plānus, kas netiek izsekoti atvērtajai reģistrācijai **Darbinieku pašapkalpošanās parametru** lapā. Varat rakties no šī elementa, lai skatītu darbinieku sarakstu lapā **Darbinieku atvieglojumu plāni**.

- **Neapstiprinātas atlases** — elements **Neapstiprinātas atlases** parāda to darbinieku skaitu, kuriem ir atlasīti vai atcelti plāni, kas ir jāapstiprina. Varat rakties no šī elementa, lai rādītu darbinieka atvieglojumu **plānu lielapjoma atjaunināšanas** lapu.

**Aktivitāte**

- **Nav sākts** – elements **Nav sākts** parāda to darbinieku skaitu, kuri nav sākuši reģistrēšanās procesu. Elements **Nav sākts** ir filtrēts saraksts, kurā ir redzami tikai tie darbinieki, kuriem nav neviena plāna, kas nav atlasīti, atcelti vai paņemti atvērtam reģistrācijas plāna periodam. Obligātie plāni tiek ignorēti un nav iekļauti, jo tie pēc noklusējuma ir atlasīti darbiniekam. Detalizētu informāciju par darbinieku var skatīt, lai rādītu lapu **Detalizēta informācija par darbinieka atvieglojumu plāniem**.

- **Notiek** – elements **Notiek** sniedz darbinieku skaitu, kuri ir procesā. Elements **Notiek** ir filtrēts saraksts, kurā ir redzami tikai darbinieki, kuriem ir vismaz viens plāns, kas ir atcelts vai atlasīts. Obligātie plāni tiek ignorēti un nav iekļauti, jo tie pēc noklusējuma ir atlasīti darbiniekam. Detalizētu informāciju par darbinieku var skatīt, lai rādītu lapu **Detalizēta informācija par darbinieka atvieglojumu plāniem**.

## <a name="view-more-options"></a>Skatīt vairāk opciju

Lai apskatītu vairāk informācijas un darbību, ko varat veikt, atlasiet **Saites**.

![Saites.](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a>Skatiet arī

[Atvieglojumu pārvaldības pārskats](hr-benefits-management-overview.md)
