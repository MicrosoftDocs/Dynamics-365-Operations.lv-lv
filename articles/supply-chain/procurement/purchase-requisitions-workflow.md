---
title: "Pirkšanas pieprasījuma darbplūsma"
description: "Šajā darbplūsmas procesā pārskatīšanas procesa gaitā tiek pārvietoti pirkšanas pieprasījumi no sākotnēja statusa Melnraksts līdz galīgajam statusam Apstiprināts. Kad pirkšanas pieprasījums ir iesniegts pārskatīšanai, tiek uzsākts darbplūsmas process. Kad pirkšanas pieprasījums ir apstiprināts, pirkšanas pasūtījumu var ģenerēt pirkšanas pieprasījuma rindām un iesniegt kreditoram pasūtījuma izpildīšanai."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqAuthorization, WorkflowParticipantExpenToken
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2234
ms.assetid: dad3ba5a-2892-45d2-874a-300896f59b34
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 0b1ec4f11672c5c2f9a6f4d072637dfd22246f77
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="purchase-requisition-workflow"></a>Pirkšanas pieprasījuma darbplūsma

[!include[banner](../includes/banner.md)]


Šajā darbplūsmas procesā pārskatīšanas procesa gaitā tiek pārvietoti pirkšanas pieprasījumi no sākotnēja statusa Melnraksts līdz galīgajam statusam Apstiprināts. Kad pirkšanas pieprasījums ir iesniegts pārskatīšanai, tiek uzsākts darbplūsmas process. Kad pirkšanas pieprasījums ir apstiprināts, pirkšanas pasūtījumu var ģenerēt pirkšanas pieprasījuma rindām un iesniegt kreditoram pasūtījuma izpildīšanai.

Lai pirkšanas pieprasījumu iesniegtu pārskatīšanai, jānokonfigurē darbplūsma. Darbplūsmas process var ietvert vienu vai vairākas pārskatīšanas darbības jebkādā secībā. Darbplūsmas procesu var arī konfigurēt, lai izlaistu pārskatīšanas uzdevumus un automātiski apstiprinātu pirkšanas pieprasījumu. Varat konfigurēt, lai darbplūsma maršrutētu pirkšanas pieprasījumu kā vienotu dokumentu, vai arī varat maršrutēt atsevišķas pirkšanas pieprasījuma rindas atbilstošajiem pārskatītājiem. Varat arī izveidot scenāriju, kur pirkšanas pieprasījums kā viens dokuments tiek maršrutēts noteiktiem pārskatītājiem, un atlasītās pirkšanas pieprasījuma rindas tiek maršrutētas citiem pārskatītājiem.  

Ja pirkšanas pieprasījuma rindas tiek pārskatītas atsevišķi, pārskatīšanas process ir jāaizpilda visām pirkšanas pieprasījuma rindām, pirms darbplūsmas process var pāriet uz nākamo darbību un pirms iespējams pabeigt visa pirkšanas pieprasījuma pārskatīšanas procesu. Kad pirkšanas pieprasījumam, tostarp visām rindām, ir pabeigts pārskatīšanas process, vispārējais pirkšanas pieprasījuma statuss mainās uz **Apstiprināts**.  

Varat konfigurēt savu darbplūsmu, lai atspoguļotu biznesa procesu pirkšanas pieprasījumiem savā organizācijā. Konfigurējot pirkšanas pieprasījuma darbplūsmas procesu, ņemiet vērā turpmāk norādīto.

-   Kādi izdevumi ir jāpārskata?
-   Kādus izdevumus var apstiprināt automātiski?
-   Kam ir nepieciešams pārskatīt un apstiprināt izdevumu pieprasījumus? Kāda loma šiem lietotājiem ir piešķirta?
-   Kādas darbības jāizpilda, ja recenzents nav pieejams?

Nākamajos piemēros ir parādīti divi darbplūsmu pirkšanas pieprasījumu konfigurēšanas veidi.

## <a name="example-1-route-a-purchase-requisition-as-a-single-document-for-review"></a>1. piemērs. Maršrutēt pirkšanas pieprasījumu pārskatīšanai kā vienu dokumentu
Nākamajā attēlā ir parādīts, kā pirkšanas pieprasījums var pārvietoties cauri darbplūsmas pārskatīšanas procesam kā vienots dokuments. Pirkšanas pieprasījuma rindas nav maršrutētas atsevišķi. Šī piemēra darbplūsmas procesā ir iekļautas šādas lomas:

-   **Pieprasītājs** — lietotājs, kas pieprasa preces vai pakalpojumus. Prasītājs var sagatavot pirkšanas pieprasījumu, vai cits darbinieks var sagatavot pirkšanas pieprasījumu pieprasītāja vārdā. Šis darbinieks ir sagatavotājs. Sagatavotājs ir atbildīgs par pirkšanas pieprasījuma pārvaldīšanu visā pārskatīšanas procesa laikā. Tikai pirkšanas pieprasījuma sagatavotājs var to modificēt.

**Piezīme.** Darbiniekam ir jābūt piešķirtām atbilstošām atļaujām izveidot pirkšanas pieprasījumu kāda cita vārdā. Izmantojiet lapu **Pirkšanas pieprasījuma atļauja**, lai iestatītu šīs atļaujas.

-   **Pirkšanas aģents** — lietotājs, kurš veic sagādes pārskatīšanu un var apstiprināt šo dokumentu.
-   **Pieprasītāja vadītājs** — lietotājs, kurš veic vadības pārskatu un var apstiprināt šo dokumentu.

![Pirkšanas pieprasījuma darbplūsmas pārskatīšanas process](./media/purchreqworkflowoverview_submission.gif)  
Šajā piemērā pirkšanas pieprasījuma darbplūsmas process ietver šādas darbības:

1.  Sagatavotājs iesniedz pirkšanas pieprasījumu pārskatīšanai.
2.  Pirkšanas aģents saņem paziņojumu. Paziņojumā pieprasīts, lai pirkšanas aģents verificē pirkšanas pieprasījumā ietverto informāciju. Ja nepieciešamās informācijas trūkst, pirkšanas aģents var pievienot to vai nosūtīt pirkšanas pieprasījumu atpakaļ sagatavotājam, lai to pievienotu. Kad visa nepieciešama informācija ievadīta, pirkšanas pieprasījuma rindu var pārvietot uz nākamo pārskatīšanas procesa darbību.
3.  Pieprasītāja vadītājs pārskata pirkšanas pieprasījumu. Pirkšanas pieprasījumu var maršrutēt uz pieprasītāja vadītāju, ja, piemēram, pirkšanas pieprasījuma summa pārsniedz pieprasītāja izdevumu ierobežojumu pirkšanas pieprasījumiem. Pieprasītāja vadītājs var apstiprināt vai noraidīt pirkšanas pieprasījumu, vai atgriezt to sagatavotājam izmaiņu veikšanai.

## <a name="example-2-route-the-individual-purchase-requisition-lines-for-review"></a>2. piemērs. Maršrutēt pārskatīšanai atsevišķas pirkšanas pieprasījuma rindas
Nākamajā attēlā ir parādīts, kā cauri darbplūsmai var maršrutēt atsevišķas pirkšanas pieprasījuma rindas. Process katrai rindai parasti ir tāds pats kā process pirkšanas pieprasījumam, kas tiek pārskatīts kā viens dokuments. Taču katrai rindai ir atsevišķi jāpabeidz darbplūsmas process, pirms darbplūsmu var pabeigt visam pirkšanas pieprasījumam.  

Šajā piemērā darbinieks ievada pieprasījumu pēc plakātiem un T-krekliem mārketinga kampaņai. Plakātu izmaksas tiek sadalītas starp mārketinga nodaļu un pārdošanas nodaļu. Ja plakātu vai T-kreklu izmaksas pārsniedz nodaļu vadītāju pilnvarojuma parakstīšanas ierobežojumu, pirkšanas pieprasījums ir jāpārskata grupas vadītājam.  

Šī piemēra darbplūsmas procesā ir iekļautas šādas lomas:

-   **Pieprasītājs** — lietotājs, kas pieprasa preces vai pakalpojumus. Prasītājs var sagatavot pirkšanas pieprasījumu, vai cits darbinieks var sagatavot pirkšanas pieprasījumu pieprasītāja vārdā. Šis darbinieks ir sagatavotājs. Sagatavotājs ir atbildīgs par pirkšanas pieprasījuma pārvaldīšanu visā pārskatīšanas procesa laikā. Tikai pirkšanas pieprasījuma sagatavotājs var to modificēt.

**Piezīme.** Darbiniekam ir jābūt piešķirtām atbilstošām atļaujām izveidot pirkšanas pieprasījumu kāda cita vārdā. Izmantojiet lapu **Pirkšanas pieprasījuma atļauja**, lai iestatītu šīs atļaujas.

-   **Pirkšanas aģents** — lietotājs, kurš veic sagādes pārskatīšanu un var apstiprināt šo dokumentu.
-   **Pieprasītāja vadītājs** — lietotājs, kurš veic vadības pārskatu un var apstiprināt šo dokumentu.
-   **Nodaļas vadītājs** — lietotājs, kurš veic izdevumu pārskatu un var apstiprināt šo dokumentu.
-   **Grupas vadītājs** — lietotājs, kurš veic parakstīšanas pilnvarojuma pārskatu un var apstiprināt šo dokumentu.

![Pirkšanas pieprasījuma rindas darbplūsmas pārskatīšanas process](./media/purchreqlineworkflowoverview.gif)  
Šajā piemērā pirkšanas pieprasījuma rindu darbplūsmas process ietver šādas darbības:

1.  Sagatavotājs iesniedz pirkšanas pieprasījumu pārskatīšanai. Katra rinda tiek maršrutēta uz pārskatītāju, kas ir konfigurēts tās saņemšanai darbplūsmas procesā.
2.  Pirkšanas aģents saņem paziņojumu. Pirkšanas aģentam, kas saņem paziņojuma pieprasījumus, jāverificē pirkšanas pieprasījumā un pirkšanas pieprasījuma rindās ietverto informāciju. Kad pirkšanas aģents atver pirkšanas pieprasījumu, ir redzamas visas rindas, bet vizuālais indikators norāda, kuras rindas pirkšanas aģentam ir nosūtītas pārskatīšanai. Ja nepieciešamās informācijas trūkst, pirkšanas aģents var pievienot to vai nosūtīt pirkšanas pieprasījuma rindu atpakaļ sagatavotājam, lai to pievienotu. Kad visa nepieciešama informācija ievadīta, pirkšanas pieprasījuma rindu var pārvietot uz nākamo pārskatīšanas procesa darbību. Pirkšanas pieprasījuma rindas pārskatīšanas procesu var veikt savstarpēji neatkarīgi.
3.  Pieprasītāja rindas vadītājs pārskata un apstiprina pirkšanas pieprasījuma rindas. Apstiprinājumu var maršrutēt pieprasītāja vadītājam, ja, piemēram, pirkšanas pieprasījuma rindas summa pārsniedz pieprasītāja izdevumu ierobežojumu pirkšanas pieprasījumu rindām. Vadītājs var apstiprināt vai noraidīt vienu vai abas no pirkšanas pieprasījuma rindām.
4.  Mārketinga nodaļas vadītājs pārskata pirkšanas pieprasījuma rindas gan plakātiem, gan T-krekliem. Pārdošanas nodaļas vadītājs pārskata pirkšanas pieprasījuma rindu tikai plakātiem, jo pārdošanas nodaļai ir jāsedz tikai tās izmaksas.
5.  Grupas vadītājs pārskata un apstiprina pirkšanas pieprasījuma rindu T-krekliem tikai tad, ja ir nepieciešams grupas vadītāja apstiprinājums, ja, piemēram, summa pirkšanas pieprasījuma rindā pārsniedz nodaļas vadītāja apstiprināto ierobežojumu. Grupas vadītājam nav jāapstiprina pirkšanas pieprasījuma rinda plakātiem.

## <a name="configuring-a-workflow-for-purchase-requisitions"></a>Darbplūsmas konfigurēšana pirkšanas pieprasījumiem
Lai pirkšanas pieprasījumu maršrutētu pārskatīšanai, jums ir jākonfigurē pirkšanas pieprasījuma darbplūsmas procesi. Jūsu definētais darbplūsmas process kontrolē mijiedarbību starp lietotāju, kas pieprasīja krājumus (pieprasītāju), un darbplūsmas pārskatītāju un apstiprinātāju. Pirkšanas pieprasījuma maršrutēšana ir atkarīga no nosacījumiem, kas norādīti darbplūsmas konfigurācijā. Piemēram: šie nosacījumi nosaka, kad pirkšanas pieprasījums jāmaršrutē, kuram lietotājam vai lomai pirkšanas pieprasījums jāmaršrutē, un darbības, kādas lietotāji var veikt.  

Šīs tēmas piemēros ir aprakstīts, kā pirkšanas pieprasījumu var maršrutēt cauri darbplūsmai kā vienu dokumentu vai kā atsevišķas pirkšanas pieprasījuma rindas. Varat arī pirkšanas pieprasījumiem konfigurēt darbplūsmu tā, lai parādītu pirkšanas pieprasījumu iekšējās kontroles pārskatīšanu, kas definēta jūsu organizācijai.  

Dalībnieki vai pārskatītāji, kuriem šis uzdevums ir piešķirts darbplūsmā, var būt konkrētas lietotāju grupas dalībnieki, kuriem ir īpaša drošības loma, lietotāji, kuri ir saistīti ar vadības hierarhijas iesniedzēju vai nosaukti lietotāji vai lietotāji ar īpašu izdevumu atbildību.

### <a name="purchase-requisition-expenditure-reviewers"></a>Pirkšanas pieprasījumu izdevumu pārskatītāji

Izdevumu pārskatītāju konfigurācijas ļauj dinamiskai maršrutēt izdevumus pārskatīšanai, pamatojoties uz lietotāju, kas piešķirts projekta lomai vai finanšu dimensijai, kurā šie izdevumi tiek iekasēti. Darbplūsmas process izmanto norādīto projekta lomu vai finanšu dimensijas īpašnieku, lai noteiktu, kam maršrutēt izdevumus.  

Varat definēt vienu vai vairākas izdevumu pārskatītāju konfigurācijas un tad atlasīt konfigurāciju, veidojat darbplūsmu. Izdevumu pārskatītāju vērtības katrai juridiskajai personai jūsu organizācijā var konfigurēt. Pēc izdevumu pārskatītāju konfigurāciju definēšanas šī konfigurācija jāpiešķir darbplūsmas uzdevumam.  

Izdevumu pārskatītāju konfigurācijas nav jādefinē. Tā vietā, definējot savu darbplūsmu, varat piešķirt konkrētus lietotājus vai lietotāju grupas kā pārskatītājus. Tomēr sarežģītas struktūras organizācijas gadījumā izdevumu pārskatītāji var palielināt apstiprināšanas procesa efektivitāti. Turklāt, iestatot izdevumu pārskatītājus, nav jāatjaunina darbplūsmas recenzenta piešķires katru reizi, kad pārskatītājs maina darba lomas.  

Izdevumu pārskatītājus var iestatīt lapā **Pirkšanas pieprasījumu izdevumu pārskatītāji**. Izveidojiet izdevumu pārskatītāju konfigurāciju un ievadiet vērtības katrai jūsu organizācijas juridiskajai personai. Projektam piešķirtajos pieprasījumos var norādīt to, kurš būs atbildīgs par pieprasījumu pārskatīšanu: projekta vadītājs, projekta kontrolieris vai projekta pārdošanas vadītājs. Izdevumi tiks maršrutēti lietotājam, kuram ir piešķirta konkrēta loma. Izdevumus ir iespējams maršrutēt arī finanšu dimensijas īpašniekam, atzīmējot atbilstošās finanšu dimensijas opciju cilnē **Organizācijas sadales**.  

Lai izmantotu kādu no darbplūsmā iestatītajiem izdevumu pārskatītājiem, opcija **Dalībnieka tips** ir jāiestata uz **Izdevumu dalībnieki** sadaļas **Piešķire**  attiecīgās darbplūsmas elementa rekvizītos.

<a name="see-also"></a>Skatiet arī
--------

[Patēriņa pieprasījuma izveide (uzdevuma ceļvedis)](tasks/create-requisition-consumption.md)

[Biznesa procesu darbplūsmu definēšana pirkšanas pieprasījumiem](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Sagādes un avotu darbplūsmas](procurement-sourcing-workflows.md)

[Pirkšanas pieprasījuma pārskats](purchase-requisitions-overview.md)




