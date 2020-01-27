---
title: Pievienošanas ceļvežu un veidņu rediģēšana programmā Dynamics 365 Talent - Onboard
description: Šajā tēmā ir paskaidrots, kā pievienot darbības un citu informāciju pievienošanas ceļvežiem un veidnēm programmā Microsoft Dynamics 365 Talent - Onboard.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 291f7aefac61c26dfab81cfff28c1c6580d46de5
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897124"
---
# <a name="edit-onboarding-guides-and-templates"></a>Pievienošanas ceļvežu un veidņu rediģēšana

[!include [banner](includes/banner.md)]

Kad esat izveidojis pievienošanas ceļvedi vai veidni programmā Microsoft Dynamics 365 Talent: Onboard, jums jāpievieno ievads, darbības, kontaktpersonas un resursi. Onboard ļauj iekļaut bagātīgu saturu jūsu pārvietošanas ceļvežiem, tostarp:

- YouTube videoklipus
- Microsoft Sway prezentācijas
- Microsoft PowerApps programmas
- Microsoft Stream videoklipus
- Microsoft Forms veidlapas
- Iframe, kurā iekļauts tīmekļa saturs

## <a name="edit-introductions-or-activities-imported-from-a-template"></a>No veidnes importēto ievadu vai darbību rediģēšana

Ja izveidojat pievienošanas ceļvedi no veidnes vai importējat darbības no vienas veidnes uz citu, uz importētajām darbībām pamanīsit pogu **Slēdzene**. Tās sauc par *pārvaldītām darbībām*.

[![Pārvaldītās darbības](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)

Atlasot pārvaldīto darbību, darbības augšdaļā var redzēt avota veidni.

[![Pārvaldītās darbības avots](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)

Ja rediģējat darbību veidnē, Onboard pārbīdīs izmaiņas uz visām veidnēm un nenosūtītiem ceļvežiem, kuru pamatā ir šī veidne. Ja atlasīsit nenosūtītu ceļvedi, kura pamatā ir rediģētā veidne, un pēc tam ceļvedī atlasīsit cilni **Darbības**, tiks parādīts paziņojums, ka jūsu ceļvedis ir mainījies. Lai noraidītu paziņojumu, atlasiet **Labi**. 

[![Paziņojuma maiņa](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)

Blakus atjauninātajām darbībām redzēsit melnu punktu.

[![Mainīta darbība](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)

Pārvaldītās darbības nevar rediģēt ārpus oriģinālās veidnes, izņemot to, ka darbības labās puses sadaļā ir jāpievieno piešķīrējs, izpildes datums vai cita informācija.

Ja vēlaties rediģēt pārvaldīto darbību vai nevēlaties, lai darbība saņem atjauninājumus no veidnes, no kuras tie nākuši, atlasiet šīs darbības pogu **Slēdzene**. Poga **Slēdzene** izzudīs. Šo darbību vairs nepārvaldīs oriģinālā veidne, un tā vairs nesaņems atjauninājumus no minētās veidnes. Atjauninājumi, ko veicat darbībai, neietekmē oriģinālo veidni.

Ja izdzēšat darbību no ceļveža un izbīdāt izmaiņas no šā ceļveža veidnes, aktivitāte ceļvedī paliks izdzēsta.

> [!NOTE]
> Veidnes nepārvalda kontaktpersonas un resursus. Turklāt sadaļas netiek pārvaldītas, tādēļ, ja pievienojat vai rediģējat sadaļu veidnē, izmaiņas netiks izstumtas uz visiem ceļvežiem vai veidnēm, kas izmanto šo veidni.
> 
> Ja veidnei pievienojat jaunas darbības, jaunās darbības tiek virzītas uz ceļvežiem un veidnēm, kuru pamatā ir šī veidne, un jaunās darbības tiek parādītas augšpusē.

## <a name="import-activities-from-another-template"></a>Darbību importēšana no citas veidnes

Ceļvedī vai veidnē varat importēt darbības no vienas vai vairākām veidnēm.

1. Atlasiet ceļvedi vai veidni, kuru vēlaties rediģēt.

2. Atlasiet cilni **Darbības**.

3. Atlasiet cilni **Importēt** sadaļā pa labi.

   [![Darbību importēšana](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)

4. Lai priekšskatītu uzdevumus jaunā cilnē jūsu pārlūkā, jebkurā veidnē atlasiet pogu **Atvērt jaunā cilnē**.

   [![Darbību importēšana](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)

5. Velciet un nometiet vajadzīgo veidni tajā vietā jūsu ceļveža veidnē, kur vēlaties, lai darbības tiktu rādītas. Turpiniet rediģēt savu ceļvedi vai veidni.

Importētās darbības saturēs pogu **Slēdzene**, kas norāda, ka šīs darbības pārvalda veidne, no kuras jūs importējāt. Veicot izmaiņas importētajā veidnē, šīs darbības atjauninās veidnē, uz kuru tās importējāt. Tomēr izmaiņas netiks automātiski izstumtas uz visiem ceļvežiem, kas izveidoti no veidnes, uz kuru importējāt.

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a>Izmaiņu no veidnes uz citām veidnēm vai ceļvežiem izstumšana

Rediģējot veidni, kas satur darbības, kuras tiek izmantotas citās veidnēs vai ceļvežos, jums ir jāstumj izmaiņas, ja vēlaties, lai tās parādītos citās veidnēs vai ceļvežos.

Ja neesat pārliecināts, vai veidnes darbības tiek izmantotas citās veidnēs vai ceļvežos, atlasiet cilni **Izmantots**, lai skatītu, kur šīs aktivitātes ir redzamas.

   [![Skatīt ceļvežus un veidnes, kuros darbības tiek izmantotas](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)

Lai izstumtu jūsu izmaiņas, veiciet tālāk norādītās darbības.

1. Saglabājiet izmaiņas, atlasot pogu **Saglabāt**. Ja to nedarīsit, jums tiks lūgts saglabāt izmaiņas nākamajā darbībā.

2. Atlasiet **Izstumt šīs izmaiņas**.

   
## <a name="add-or-edit-an-introduction"></a>Ievada pievienošana vai rediģēšana

1. Cilnē **Ievads** ievadiet ceļveža nosaukumu un sākuma ziņojumu. Lai izmantotu parauga tekstu, atlasiet **Lietot šo ziņojumu**.

    [![Ievada cilne Onboard veidnē](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)

2. Izmantojiet formatēšanas pogas, lai izsauktu nepieciešamo tekstu vai pievienotu attēlus vai saites.
3. Atlasiet **Saglabāt**, lai saglabātu veikto darbu.

## <a name="add-or-edit-activities"></a>Darbību pievienošana vai rediģēšana

1. Cilnē **Darbības** velciet vienumus no labās puses uz rediģēšanas apgabalu.
2. Lai organizētu ceļvedi sadaļās, velciet vienumu **Jauna sadaļa** uz rediģēšanas apgabalu un ievadiet sadaļas nosaukumu un neobligātu aprakstu.

    ![[Jaunas sadaļas pievienošana pievienošanas ceļvedim vai veidnei](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. Lai pabeigtu darbību pievienošanu nesen nolīgtajam darbiniekam, velciet vienumu **Jauna darbība** uz rediģēšanas apgabalu un ievadiet darbības nosaukumu un aprakstu.

    ![[Jaunas aktivitātes pievienošana pievienošanas ceļvedim vai veidnei](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. Bagātināta satura pievienošana savam pievienošanas cveļvedim

    - Lai pievienotu YouTube videoklipu, velciet **YouTube** vienumu uz rediģēšanas apgabalu, ievadiet darbības nosaukumu un aprakstu un ievadiet YouTube videoklipa vietrādi URL.
    - Lai pievienotu Sway prezentāciju vai biļetenu, velciet vienumu **Sway** uz rediģēšanas apgabalu, ievadiet darbības nosaukumu un aprakstu un ievadiet Sway prezentācijas vai biļetena iegulto vietrādi URL.
    - Lai pievienotu programmu Microsoft Power Apps, velciet vienumu **Power Apps** uz rediģēšanas apgabalu, ievadiet darbības nosaukumu un aprakstu un vai nu atlasiet programmu Power Apps vai arī ievadiet programmas Power Apps ID.
    - Lai pievienotu Microsoft Stream videoklipu, velciet **Microsoft Stream** vienumu uz rediģēšanas apgabalu, ievadiet darbības nosaukumu un aprakstu un ievadiet Microsoft Stream videoklipa vietrādi URL.
    - Lai pievienotu Microsoft Forms veidlapu, velciet vienumu **Microsoft Forms** uz rediģēšanas apgabalu, ievadiet darbības nosaukumu un aprakstu, ievadiet Microsoft Forms veidlapas vietrādi URL un norādiet ekrāna laukuma lielumu.
    - Lai pievienotu iframe, kas ietver tīmekļa saturu, velciet vienumu **Tīmekļa saturs (iframe)** uz rediģēšanas apgabalu, ievadiet darbības nosaukumu un aprakstu, ievadiet tīmekļa satura vietrādi URL un norādiet ekrāna laukuma lielumu.

    ![[Bagātināta satura pievienošana pievienošanas ceļvedim vai veidnei](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. Neobligāti: katras darbības labās puses apgabalā piešķiriet darbību konkrētai personai vai lomai, pievienojiet izpildes datumu un kontaktpersonu, un piešķiriet kategorijas krāsu. Piešķirot darbību personai vai lomai, katrai personai tiek izveidots uzdevums. Šis uzdevums tiek parādīts Onboard izvēlnē **Uzdevumi**.

    [![Darbības piešķiršana pievienošanas ceļvedī vai veidnē](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)

3. Atlasiet **Saglabāt**, lai saglabātu veikto darbu.

Lai izdzēstu darbību vai sadaļu, atlasiet pogu **Dzēst** (atkritnes simbols) darbības vai sadaļas augšējā labajā stūrī.

Lai pārkārtotu darbības un sadaļas, velciet tās uz jaunu atrašanās vietu.

## <a name="add-or-edit-contacts"></a>Kontaktpersonu pievienošana vai rediģēšana

Varat pievienot kontaktpersonas, kas var palīdzēt jūsu nesen nolīgtajam darbiniekam gūt panākumus no pirmās dienas. Šīs kontaktpersonas var būt darba devēji, grupas biedri, nolīgšanas palīgi, padomdevēji, administratori un IT atbalsta personāls.

1. Cilnē **Kontaktpersonas** atlasiet **Jauna kontaktpersona**.
2. Dialoglodziņā **Pievienot grupas dalībnieku** ievadiet kontaktpersonas vārdu vai e-pasta adresi, ievadiet īsu aprakstu, kurā paskaidrots, kā kontaktpersona var palīdzēt nesen nolīgtajam darbiniekam un pēc tam atlasiet **Pievienot**. 

    ![[Kontaktu pievienošana pievienošanas ceļvedim vai veidnei](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    Vai arī varat atlasīt vienu vai vairākas kontaktpersonas sadaļā **Ieteikumi.**

3. Atlasiet **Saglabāt**, lai saglabātu veikto darbu.

Lai izdzēstu kontaktpersonu, atlasiet pogu **Dzēst** (atkritnes simbols) pa labi no kontaktpersonas.

Lai rediģētu kontaktpersonu, atlasiet pogu **Rediģēt** (zīmuļa simbols) pa labi no kontaktpersonas.

## <a name="add-or-edit-resources"></a>Resursu pievienošana vai rediģēana

Varat pievienot noderīgus failus, kartes un saites jūsu pievienošanas ceļveža sadaļai **Resursi**.

1. Cilnē **Resursi** atlasiet **Jauns resurss**.
2. Izpildiet kādu no norādītajām transakcijām.

    - Lai pievienotu failu, atlasiet cilni **Fails** un velciet failu uz norādīto apgabalu. (Vai arī noklikšķiniet jebkurā vietā šajā apgabalā, lai pārlūkotu failu savā datorā, vai atlasiet **Pārlūkot OneDrive**.) Ievadiet faila nosaukumu un pēc tam atlasiet **Pievienot**.
    - Lai pievienotu saiti, atlasiet cilni **Saite**, ievadiet saites nosaukumu un adresi un pēc tam atlasiet **Pievienot**.
    - Lai pievienotu karti, atlasiet cilni **Karte**, ievadiet kartes nosaukumu un adresi un pēc tam atlasiet **Pievienot**. Onboard ietvers jūsu norādītās adreses karti.

    ![[Resursa pievienošana pievienošanas ceļvedim vai veidnei](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. Atlasiet **Saglabāt**, lai saglabātu veikto darbu.

Lai izdzēstu resursu, atlasiet pogu **Dzēst** (atkritnes simbols) pa labi no resursa.

Lai rediģētu kontaktpersonu, atlasiet pogu **Rediģēt** (zīmuļa simbols) pa labi no resursa.

## <a name="next-steps"></a>Nākamās darbības

- [Satura kopīgošana ar citiem ieguldītājiem](./onboard-share-template.md)
- [Uzdevumu un pievienoto darbinieku statusa skatīšana](./onboard-view-status.md)
- [Par pieņemšanu darbā atbildīgo grupu izveide Onboard](./onboard-create-team.md)

### <a name="see-also"></a>Skatiet arī

- [Programmas Onboard izmēģināšana vai iegāde](https://dynamics.microsoft.com/talent/onboard/)
- [Jaunumi un izmaiņas Dynamics 365 Talent](./whats-new.md)
- [Nodošanas izpildei plāni](https://docs.microsoft.com/business-applications-release-notes/index)
- [Atbalsta saņemšana saistībā ar Microsoft Dynamics 365 Talent](./talent-support.md)
