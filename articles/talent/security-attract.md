---
title: Iestatīt lietotāju atļaujas programmā Attract
description: Šajā tēmā ir sniegta informācija par lomu drošību programmā Microsoft Dynamics 365 Talent — Attract.
author: andreabichsel
manager: AnnBe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: efac512cfa07bb2183f06b8be45f74bef9af0767
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461864"
---
# <a name="set-user-permissions-in-attract"></a>Iestatīt lietotāju atļaujas programmā Attract

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract izmanto no lomas atkarīgu drošību. Citiem vārdiem sakot, piekļuve netiek piešķirta atsevišķiem lietotājiem, bet gan drošības lomām, un lietotāji tiek piešķirti šīm drošības lomām. Lietotājam, kas ir piešķirts kādai drošības lomai, ir piekļuve ar šo lomu saistītajai privilēģiju kopai.

Attract nodrošina piecas tālāk uzskaitītās lietotāju pamata lomas.

- Administrators
- Par pieņemšanu darbā atbildīgais vadītājs:
- Personāla atlases darbinieks
- Intervētājs
- Tikai lasāms

Loma “Administrators” ir vienīgā loma, kurai ir atļauja pievienot citus lietotājus un mainīt viņu tiesības.

- **Pievienot** — sadaļas Administrēšanas centrs cilnē **Lietotāju atļaujas** atlasiet **Piešķirt lomas**, meklējiet pievienojamo lietotāju un pēc tam piešķiriet atļaujas šim lietotājam.
- **Rediģēt** — meklējiet lietotāju vai atrodiet lietotāju sarakstā un pēc tam atlasiet **Rediģēt**, lai veiktu izmaiņas šī lietotāja atļaujās.
- **Dzēst** — ja dzēšat kāda lietotāja atļaujas, šis lietotājs netiek noņemts no sistēmas. Taču jūs ierobežojat šī lietotāja piekļuvi un privilēģijas programmā Attract. Piemēram, Hilda bija piešķirta lomai “Par pieņemšanu darbā atbildīgais vadītājs”, un viņa ir pievienota darbam kā par pieņemšanu darbā atbildīgais vadītājs. Ja vēlāk Hilda tiek noņemta no lomas “Par pieņemšanu darbā atbildīgais vadītājs”, darbā viņa joprojām ir par pieņemšanu darbā atbildīgais vadītājs un viņai joprojām ir piekļuve šim darbam. Taču viņa nevar izveidot citus darbus.

Nākamajās sadaļās ir sniegts augsta līmeņa apraksts par katru lomu. Tēmā tālāk esošajās tabulās ir sniegta detalizētāka informācija.

> [!NOTE]
> Noteikti līdzekļi ir pieejami tikai kopā ar visaptverošās darbā pieņemšanas pievienojumprogrammu programmai Attract.

## <a name="administrator"></a>Administrators

Lietotāji, kas ir piešķirti lomai “Administrators”, var piekļūt un mainīt visus datus programmā Attract. Administratori var izveidot, lasīt, atjaunināt un dzēst datus. Viņiem ir piekļuve administrēšanas centram, kur viņi var konfigurēt Attract un iestatīt lietotāju informāciju. Iesakām piešķir lomu “Administrators” vismaz vienai personai. Pēc noklusējuma Microsoft Power Apps vides administrators tiek iestatīts kā administrators programmā Attract. Ja reģistrējāties programmas Attract izmēģinājumversijai, jums tiek automātiski piešķirta loma “Administrators”. Lai izveidotu darbus, pašlaik lietotājiem ar lomu “Administrators” ir nepieciešama arī loma “Personāla atlases darbinieks” vai loma “Par pieņemšanu darbā atbildīgais vadītājs”.

## <a name="hiring-manager"></a>Par pieņemšanu darbā atbildīgais vadītājs:

Lietotāji, kas ir piešķirti lomai “Par pieņemšanu darbā atbildīgais vadītājs”, var izveidot darbus un atjaunināt iepriekš izveidotus darbus. Par pieņemšanu darbā atbildīgajiem vadītājiem ir pieejama tikai ierobežota kopa ar darbībām, ko viņi var veikt saistībā ar darbu un ar šo darbu saistītajiem pieteikumiem. Darbā pieņemšanas grupai kā par pieņemšanu darbā atbildīgos vadītājus var pievienot tikai lietotājus, kuri ir piešķirti lomai “Par pieņemšanu darbā atbildīgais vadītājs”.

## <a name="recruiter-role"></a>Loma “Personāla atlases darbinieks”

Lietotājiem, kas ir piešķirti lomai “Personāla atlases darbinieks”, ir pilnīgas lasīšanas, izveidošanas, atjaunināšanas un dzēšanas privilēģijas tiem darbiem, ko viņi ir izveidojuši. Šiem lietotājiem var būt arī pilnīgas izveidošanas, lasīšanas, atjaunināšanas un dzēšanas privilēģijas attiecībā uz pieteikumiem, kas ir saistīti ar viņiem piederošajiem darbiem. Darbā pieņemšanas grupai kā personāla atlases darbiniekus var pievienot tikai lietotājus, kuri ir piešķirti lomai “Personāla atlases darbinieks”.

## <a name="interviewer"></a>Intervētājs

Kā intervētāju darbā pieņemšanas grupai var pievienot jebkuru lietotāju, kuram ir Azure Active Directory (Azure AD) konts attiecīgajā organizācijā. Lietotāji, kas ir piešķirti lomai “Intervētājs”, var skatīt darba informāciju un kandidāta datus darbiem, kuriem šie lietotāji ir ietverti darbā pieņemšanas grupā. Šiem darbiem intervētāji var izteikt arī ieteikumus par pieņemšanu darbā un sniegt atsauksmes par kandidātiem. Taču viņi nevar atjaunināt darba informāciju vai kandidāta datus.

## <a name="read-only"></a>Tikai lasāms

Lietotājiem, kas ir piešķirti lomai “Tikai lasāms”, ir tikai lasīšanas piekļuve visiem datiem Attract vidē. Taču šie lietotāji nevar izveidot vai rediģēt nekādus datus.

## <a name="find-out-which-roles-you-have"></a>Savu lomu noskaidrošana

1.  Programmā Attract noklikšķiniet uz jautājuma zīmes (**?**) lapas augšējā labajā stūrī.

2.  Noklikšķiniet uz **Par**.

    Parādītajā logā tiek rādīts, kuras lomas jums ir programmā Attract.

    ![Attract licences tipa skatīšana](media/attract-license-types.png)
    
## <a name="delegated-roles"></a>Deleģētās lomas

Katram darbam, saistībā ar kuriem lietotāji ir ietverti darbā pieņemšanas grupā, personāla atlases darbinieki un par pieņemšanu darbā atbildīgie vadītāji var deleģēt vienu vai vairākus savus delegātus. Taču viņi nevar norādīt delegātus citām personām attiecīgajā darbā pieņemšanas grupā.

Delegātiem ir tādas pašas privilēģijas kā personai, kas šos delegātus norādīja. Piemēram, ja par pieņemšanu darbā atbildīgais vadītājs kādam darbam norāda savu delegātu, šim delegātam attiecībā uz šo darbu ir tādas pašas privilēģijas kā par pieņemšanu darbā atbildīgajam vadītājam. Delegāti nevar noņemt citus delegātus no darbā pieņemšanas grupas. Viņi nevar arī noņemt personas, kuras viņus deleģēja.

## <a name="job-details-and-actions"></a>Darba informācija un darbības

Lietotāji, kuriem ir loma “Personāla atlases darbinieks” vai “Par pieņemšanu darbā atbildīgais vadītājs”, var izveidot darbus. Tālāk norādītās privilēģijas attiecas uz darba informāciju un darbībām, kuras var veikt saistībā ar darbiem.

| Dati vai darbība    | Personāla atlases darbinieks | Par pieņemšanu darbā atbildīgais vadītājs: | Intervētājs |
|-------------------|-----------|----------------|-------------|
| Darba informācija       | Izveidot, lasīt, atjaunināt un dzēst darbiem, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Izveidot, lasīt, atjaunināt un dzēst darbiem, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Tikai lasāms |
| Darbā pieņemšanas grupa       | Izveidot, lasīt, atjaunināt un dzēst darbiem, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Izveidot, lasīt, atjaunināt un dzēst darbiem, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Tikai lasāms |
| Darba grāmatošana       | Izveidot, lasīt, atjaunināt un dzēst darbiem, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Tikai lasāms | Tikai lasāms |
| Apstrādāt           | Izveidot, lasīt, atjaunināt un dzēst darbiem, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Izveidot, lasīt, atjaunināt un dzēst darbiem, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Tikai lasāms |
| Pievienot kandidātus    | Pievienot kandidātus darbiem, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Pievienot kandidātus darbiem, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Nav atļauts |
| Pievienot potenciālos darba ņēmējus     | Pievienot potenciālos darba ņēmējus darbiem, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Konfigurācijas opcija sadaļā [potenciālo darba ņēmēju aktivitātes iestatīšana](./activities-attract.md#prospect-activity) kontrolē, vai intervētāji var pievienot un skatīt potenciālos darba ņēmējus. | Nav atļauts |
| Aktivizēt darbu      | Aktivizēt darbus, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Aktivizēt darbus, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Nav atļauts |
| Aizvērt darbu         | Aizvērt darbus, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Nav atļauts | Nav atļauts |
| Dzēst darbu        | Dzēst darbus, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Tikai tad, ja darbam nav pievienots neviens kandidāts | Nav atļauts |
| Dzēst kandidātus | Dzēst kandidātus, ja lietotājs ir darbā pieņemšanas grupā | Nav atļauts | Nav atļauts |

## <a name="application-details-and-actions"></a>Pieteikuma informācija un darbības

Tālāk norādītās privilēģijas attiecas uz darbam raksturīgo informāciju par kandidātiem un darbībām, kuras var veikt ar pieteikumiem.

| Dati vai darbība          | Personāla atlases darbinieks | Par pieņemšanu darbā atbildīgais vadītājs: | Intervētājs |
|-------------------------|-----------|----------------|-------------|
| Pieteikumu dokumenti   | Izveidot, lasīt, atjaunināt un dzēst darbiem, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Izveidot, lasīt, atjaunināt un dzēst darbiem, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Tikai lasāms |
| Pieteikumu piezīmes       | Izveidot, lasīt, atjaunināt un dzēst darbiem, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Izveidot, lasīt, atjaunināt un dzēst darbiem, kuriem lietotājs ir ietverts darbā pieņemšanas grupā | Tikai lasāms|
| Pieteikumu aktivitāte    | Skatīt, ja lietotājs ir darbā pieņemšanas grupā | Skatīt, ja lietotājs ir darbā pieņemšanas grupā | Tikai lasāms |
| Pieteikumu atsauksmes    | Pievienot un skatīt visas atsauksmes, ja lietotājs ir darbā pieņemšanas grupā | Pievienot un skatīt visas atsauksmes, ja lietotājs ir darbā pieņemšanas grupā | Var pievienot atsauksmes\*\* |
| Noraidīt pieteikumu      | Var noraidīt, ja lietotājs ir darbā pieņemšanas grupā | Nav atļauts | Nav atļauts |
| Pārcelt uz nākamo posmu           | Var noraidīt, ja lietotājs ir darbā pieņemšanas grupā | Var pārcelt, ja lietotājs ir darbā pieņemšanas grupā | Nav atļauts |
| Palaist piedāvājumu pārvaldību | Var sākt piedāvājumu pārvaldību | Pastāv konfigurācijas opcija piedāvājumu aktivitātei. | Nav atļauts |


\*\* Konfigurācijas opcija sadaļā [atsauksmju aktivitāšu iestatīšana](./activities-attract.md) kontrolē to, vai intervētāji var redzēt viens otra atsauksmes.


## <a name="process-templates"></a>Procesa veidnes

Tālāk norādītās privilēģijas attiecas uz darbā pieņemšanas procesa veidnēm. Grupas dalībnieku iespējas izveidot un rediģēt veidnes tiek konfigurētas administrēšanas centra sadaļā **Veidņu pārvaldība**. Ja veidņu pārvaldība ir ieslēgta, personāla atlases darbinieki un par pieņemšanu darbā atbildīgie vadītāji var izveidot un rediģēt paši savas procesa veidnes. Ja veidņu pārvaldība ir izslēgta, procesa veidnes var izveidot un rediģēt tikai administratori. Nākamajā tabulā tiek pieņemts, veidņu pārvaldība ir ieslēgta.

| Dati              | Personāla atlases darbinieks                                           | Par pieņemšanu darbā atbildīgais vadītājs:                                      | Intervētājs |
|-------------------|-----------------------------------------------------|-----------------------------------------------------|-------------|
| Apstrādes veidnes | Pilnīgas privilēģijas attiecībā uz veidnēm, ko lietotājs izveido | Pilnīgas privilēģijas attiecībā uz veidnēm, ko lietotājs izveido | Nav piekļuves   |

## <a name="email-and-email-templates"></a>E-pasts un e-pasta veidnes

Tālāk norādītās privilēģijas attiecas uz e-pasta veidnēm un darbībām, kuras var veikt saistībā ar e-pasta ziņojumiem. E-pasta veidnes var izveidot un rediģēt tikai administratori.

| Dati vai darbība     | Personāla atlases darbinieks          | Par pieņemšanu darbā atbildīgais vadītājs:     | Intervētājs |
|--------------------|--------------------|--------------------|-------------|
| E-pasta veidnes    | Tikai lasīšanas piekļuve   | Tikai lasīšanas piekļuve   | Nav piekļuves   |
| Nosūtīt e-pasta ziņojumu         | Sūtīt vienai aktivitātei  | Sūtīt vienai aktivitātei  | Nav piekļuves   |
| Rediģēt e-pasta saturu | Rediģēt e-pasta saturu | Rediģēt e-pasta saturu | Nav piekļuves   |

## <a name="talent-pools"></a>Potenciālo kandidātu kopas

Tālāk norādītās privilēģijas attiecas uz talantu kopām. Talantu kopas ir redzamas tikai personai, kas tās izveidoja, izņemot gadījumus, kas šī persona izlemj tās kopīgot. Var izmantot kandidātu meklēšanu, lai meklētu kandidātus, kas nav pievienoti nosauktai kopai.

| Dati vai darbība   | Personāla atlases darbinieks                                       | Par pieņemšanu darbā atbildīgais vadītājs:                                  | Intervētājs |
|------------------|-------------------------------------------------|-------------------------------------------------|-------------|
| Nosaukta kopa       | Pilnīgas privilēģijas attiecībā uz kopām, ko lietotājs izveido | Pilnīgas privilēģijas attiecībā uz kopām, ko lietotājs izveido | Nav piekļuves   |
| Kopīgot kopu       | Tikai kopas, ko lietotājs izveido                | Tikai kopas, ko lietotājs izveido                | Nav piekļuves   |
| Kandidātu meklēšana | Pilnīgas meklēšanas iespējas                        | Pilnīgas meklēšanas iespējas                        | Nav piekļuves   |

## <a name="candidates"></a>Kandidāti

Kandidāti ir personas, kas ir pievienotas talantu kopai, bet nav saistītas ar darbu.

| Dati                        | Personāla atlases darbinieks                        | Par pieņemšanu darbā atbildīgais vadītājs:                   | Intervētājs |
|-----------------------------|----------------------------------|----------------------------------|-------------|
| Profils — informāciju par kandidātu | Izveidot, lasīt, atjaunināt un dzēst | Izveidot, lasīt, atjaunināt un dzēst | Nav piekļuves   |
| Dokumenti                   | Izveidot, lasīt, atjaunināt un dzēst | Izveidot, lasīt, atjaunināt un dzēst | Nav piekļuves   |


[!INCLUDE[footer-include](../includes/footer-banner.md)]