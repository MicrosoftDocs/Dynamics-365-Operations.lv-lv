---
title: Bieži uzdotie jautājumi par personāla darbībām
description: Šajā tēmā ir atbildes uz jautājumiem, kas varētu rasties, ja jūsu organizācija izmanto personāla darbības.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: c952bdc95b49c92fea34aef63b57c7e193b2f09a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065155"
---
# <a name="personnel-actions-faq"></a>Bieži uzdotie jautājumi par personāla darbībām


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā ir atbildes uz jautājumiem, kas varētu rasties, ja jūsu organizācija izmanto personāla darbības. Personāla darbības ir papildu darbības, kas jāizpilda, kad veicat noteiktus uzdevumus saistībā ar personālu. 

Uzdevumu piemēri, kuriem var būt nepieciešamas personāla darbības, ir šādi:
 - Kad veidojat jaunas pozīcijas. 
 - Mainiet esošās pozīcijas vērtības. 
 - Pieņemt darbā jaunus darbiniekus. 
 - Pārcelt darbiniekus. 
 - Mainīt strādnieka kompensāciju. 
 - Mainiet pozīciju uzdevumus. 
 - Atlaist darbiniekus.

> [!NOTE]
> Personāla darbības ir pieejamas tikai tad, ja **Iespējot darbinieku darbības** un **Iespējot pozīcijas darbības** lauki ir iestatīti uz **Jā**, iekš **Personāla darbības** cilne uz **Cilvēkresursu kopīgie parametri** lappuse. 

## <a name="how-can-i-tell-if-my-organization-requires-personnel-actions"></a>Kā noteikt, vai mana organizācija pieprasa personāla darbības?
Jūsu organizācija pieprasa personāla darbības, ja jums ir jāatlasa personāla darbība, kad veidojat jaunus amatus, maināt pastāvošos amatus, pieņemat darbā jaunus darbiniekus, pārsūtāt darbiniekus, maināt darbinieka atlīdzību, maināt amatu piešķires, pārtraucat darba attiecības ar darbiniekiem vai ievadāt darbiniekiem atvaļinājumus. 

## <a name="what-is-the-difference-between-a-position-action-and-a-worker-action"></a>Kāda ir atšķirība starp amata darbību un darbinieka darbību?
Ir divu veidu personāla darbības.

- **Pozīcija** darbība – pozīcijas darbība tiek veikta esošajām pozīcijām vai jaunām pozīcijām. Amata darbība var būt nepieciešama, piemēram, ja maināt pastāvošā amata vērtību vai ja veidojat jaunu sezonālu amatu. 

- **Strādnieks** darbība – darbinieka darbība tiek veikta esošajiem darbiniekiem vai jauniem darbiniekiem. Darbinieka darbība var būt nepieciešama, piemēram, kad tiek pieņemts darbā jauns darbinieks vai tiek paaugstināts amatā jau esošais darbinieks. 

## <a name="what-do-the-statuses-of-the-personnel-actions-mean"></a>Ko nozīmē personāla darbību statusi?
Personāla darbībām var būt tālāk norādītie statusi.

- **Melnraksts** – ja tiek izmantota darbplūsma, darbība nav iesniegta. Ja darbplūsma netiek izmantota, darbība nav pabeigta.
- **Notiek pārskatīšana** – personāla darbība ir iesniegta darbplūsmai, bet darbplūsma nav pabeigta.
- **Apstiprināts gaida** – darbplūsma ir pabeigta, bet izmaiņas joprojām tiek veiktas. **Atcelts** – Darbplūsma tika atcelta vai personāla darbība tika atsaukta. **Noraidīts** – Darbības pieprasījumu apstiprinātājs noraidīja.
- **Darbības apstrāde** – darbības pieprasījums ir apstiprināts, un izmaiņas tiek apstrādātas.
- **Darbplūsma izpildīta**  – darbplūsma ir pabeigta un izmaiņas ir apstrādātas. **Neizdevās** – Darbplūsma neizdevās, jo informācija ir novecojusi. Klikšķis **Atkārtoti aktivizējiet** lai parādītu jaunāko informāciju un turpinātu.
- **Pabeigts** – amats tika sekmīgi izveidots vai modificēts, vai darbinieks tika sekmīgi pieņemts darbā vai pārsūtīts, vai darba attiecības ar šo darbinieku ir sekmīgi izbeigtas, vai ir veiksmīgi mainīta darbinieka atlīdzība. **Kļūda** – Radās problēma, kas nav novecojusi informācija. Atveriet **Personāla darbību ziņojumu žurnāls** lai noteiktu kļūdas cēloni.
- **Liegts** – apstiprinātājs darbības pieprasījumu liedza.

## <a name="can-i-delete-a-personnel-action"></a>Vai personāla darbību var izdzēst?
Jā, varat dzēst personāla darbības, kuru statuss ir **Melnraksts**, **Kļūda**, **Nesekmīgi** vai **Atcelts**. Personāla darbības ar statusu **Pabeigts** var dzēst tikai tad, ja lapā **Cilvēkresursu kopīgie parametri** opcija **Atļaut pabeigto darbinieka darbību dzēšanu** ir iestatīta uz **Jā**.

## <a name="what-is-the-fastest-way-to-check-the-status-of-a-personnel-action-request"></a>Kā var visātrāk pārbaudīt personāla darbības pieprasījuma statusu?
Atveriet jebkuru no **Personāla darbība** saraksta lapas un atlasiet personāla darbību.

## <a name="what-should-i-do-if-a-personnel-action-request-fails"></a>Ko darīt, ja personāla darbības pieprasījumu neizdodas izpildīt?
Ja personāla darbības pieprasījumu neizdodas izpildīt, veiciet tālāk aprakstītās darbības, lai atrisinātu šo kļūdu un iesniegtu pieprasījumu vēlreiz.

> 1. Sadaļā **Darbību rūts** noklikšķiniet uz pogas **Kļūdas teksts**, lai apskatītu ziņojuma tekstu, kur šī problēma ir aprakstīta.
> 
> 2. Sadaļā **Darbību rūts** noklikšķiniet uz **Aktivizēt no jauna**, lai ielādētu visjaunāko informāciju un personāla darbības statusu atkal iestatītu kā **Melnraksts**.
> 
> 3. Novērsiet kļūdu un pēc tam noklikšķiniet uz **Pabeigt** vai **Iesniegt**.

## <a name="what-happens-to-a-personnel-action-that-uses-workflow-when-the-final-approval-is-completed"></a>Kas notiek ar personāla darbību, kas izmanto darbplūsmu, kad galīgais apstiprinājums tiek pabeigts?
Ja nav kļūdu, šī personāla darbība kļūst tikai lasāma. (Vēsturi varat skatīt vietnē **Visas darbinieku darbības** saraksta lapa, bet jūs nevarat mainīt personāla darbību.) Kad personāla darbības statuss ir **Pabeigts**, amata vai darbinieka ieraksts jau ir atjaunināts. Lai skatītu veiktās izmaiņas, atveriet saraksta lapu **Amati** vai **Nodarbinātie**.

## <a name="why-do-i-receive-the-following-error-when-i-enter-a-non-zero-value-in-the-pay-rate-field-the-value-is-out-of-its-valid-range--it-much-be-between-000-and-000"></a>Kāpēc tiek rādīta šāda kļūda, ja apmaksas likmes laukā ievadu vērtību, kas nav nulle? "Vērtība atrodas ārpus tās derīguma diapazona – tai ir jābūt no 0,00 līdz 0,00"
Jūs saņemat šo ziņojumu, jo **Līmenis** lauks uz **Darbs** lapa ir tukša darbam, kas ir saistīts ar atlasīto amatu.

Lai novērstu šo kļūdu, izpildiet tālāk aprakstītās darbības.

> 1. Uz **Strādnieka amatu uzdevumi** lapu, noklikšķiniet uz **Pozīcija** lauks.  
> 2. Noklikšķiniet uz **Darbs** lauka vērtību, lai atvērtu **Darbs** lappuse.
> 3. Darbību rūtī noklikšķiniet uz **Rediģēt**.
> 4. Noklikšķiniet uz **Kompensācija** cilne.
> 5. Iekš **Līmenis** laukā atlasiet līmeni.
> 6. Aizveriet **Darbs** lappuse.
> 7. Aizveriet **Pozīcija** lappuse.
> 8. Atgriezties uz **Kompensācija** cilne uz **Strādnieks** lapu, atlasiet **Fiksēta kompensācija**.  Izvēlieties **Jauns** un ievadiet darbinieka amatu **Pozīcija** lauks.  Ievadiet vērtību laukā **Plānot** laukā un pēc tam ievadiet darbinieka atlīdzību laukā **Maksas likme** lauks.

## <a name="why-cant-i-change-the-effective-date-on-the-header-of-the-worker-action-page"></a>Kāpēc es nevaru mainīt spēkā stāšanās datumu Darbinieka darbību lapas galvenē?
Spēkā stāšanās datumu nevarat mainīt, jo šis lauks tiek aizpildīts ar attiecīgajam darbības tipam vispiemērotāko datumu.

Piemērs.

- Spēkā stāšanās datums darbības **Pārtraukt darba attiecības ar nodarbināto** galvenē ir datums, ko ievadījāt laukā **Darba attiecību izbeigšanas datums**.
- Spēkā stāšanās datums darbības **Nolīgt nodarbināto** galvenē ir datums, ko ievadījāt laukā **Darba attiecību uzsākšanas datums**.
- Spēkā stāšanās datums darbības **Pārcelt nodarbināto** galvenē ir datums, ko šim nodarbinātajam ievadījāt laukā **Norīkojuma sākuma datums**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
