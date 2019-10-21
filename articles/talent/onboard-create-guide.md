---
title: Pievienošanās ceļveža izveide un nosūtīšana, izmantojot Dynamics 365 Talent - Onboard
description: Šajā tēmā ir paskaidrots, kā izmantot programmu Microsoft Dynamics 365 Talent - Onboard, lai izveidotu pievienošanas ceļvedi nesen nolīgtajiem darbiniekiem. Šis uzdevums ir būtisks pirmais solis cilvēkkapitāla pārvaldības (HCM) no pieņemšanas darbā līdz aiziešanai pensijā stratēģijā.
author: andreabichsel
manager: ''
ms.date: 05/02/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e4dbfcc3b3fd611eea36109a516a7b9361a9f654
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009858"
---
# <a name="create-and-send-an-onboarding-guide"></a>Pievienošanās ceļveža izveide un nosūtīšana

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Onboard ļauj izveidot pievienošanas ceļvežus no veidnēm, kuras pats esat izveidojis, no veidnēm, kas ir pieejamas galerijā, vai no nulles.

Kad esat izveidojis pievienošanas ceļvedi, varat to nosūtīt nesen nolīgtam darbiniekam. Vai arī varat to nosūtīt vairākiem nesen nolīgtiem darbiniekiem Microsoft Excel failā, kuru lejupielādējat no programmas Onboard.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a>Izveidot pievienošanas ceļvedi no veidnes un nosūtīt to vienam nesen nolīgtam darbiniekam

1. Kreisās puses izvēlnē atlasiet **Veidnes**.
2. Sadaļā **Manas veidnes**atlasiet veidni, kuru vēlaties iestatīt kā pievienošanas ceļvedi nesen nolīgtam darbiniekam.
3. Rediģējiet veidni pēc vēlēšanās. Neaizmirstiet saglabāt darbu.
4. Kad esat pabeidzis veidnes rediģēšanu, atlasiet **Izveidot ceļvedi**.

    [![Pievienošanās ceļveža izveide no veidnes](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)

5. Logā **Izveidot ceļvedi** sadaļā **Kuru jūs pievienojat** ievadiet nesen nolīgtā darbinieka vārdu vai e-pasta adresi. Ja nesen nolīgtais darbinieks vēl nav sistēmā, atlasiet **Pievienot tūlīt** un ievadiet darbinieka informāciju.

    ![[Informācijas ievadīšana pievienošanas ceļvedim](./Media/Onboard-Create-a-Guide-Window.png)](./media/onboard-create-a-guide-window.png)

6. Sadaļā **Kad viņi sāks**atlasiet sākuma datumu.
7. Ja pievienošanas ceļvedis ir automātiski jānosūta nesen nolīgtam darbiniekam konkrētā datumā, pārliecinieties, vai ir ieslēgta opcija **Ieplānot automātiskas nosūtīšanas datumu** un pēc tam atlasiet automātiskās nosūtīšanas datumu. Lai ceļvedi nosūtītu nekavējoties, izslēdziet opciju **Ieplānot automātiskās nosūtīšanas datumu**.
8. Atlasiet **Gatavs**.
9. Kad esat pabeidzis rediģēt pievienošanas ceļvedi, augšējā labajā stūrī atlasiet **Sūtīt**. Pēc tam izpildiet kādu no norādītajām darbībām.

    - Lai nosūtītu nesen nolīgtam darbiniekam saiti uz pievienošanas ceļvedi, atlasiet **Kopēt saiti** un pēc tam atlasiet **Kopēt**.
    - Lai pielāgotu pievienošanas ceļveža e-pastu pirms nosūtīšanas, atlasiet **Pielāgot e-pastu pirms nosūtīšanas**, atlasiet **Tālāk**, pielāgojiet e-pasta ziņojumu, kā vēlaties, un pēc tam atlasiet **Sūtīt**.
    - Lai nosūtītu e-pasta ziņojumu, to nepielāgojot, atlasiet **Tālāk** un pēc tam atlasiet  **Sūtīt**.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a>Izveidot pievienošanas ceļvedi no veidnes un nosūtīt to vairākiem nesen nolīgtiem darbiniekiem

Onboard ļauj nosūtīt pievienošanas ceļvedi vienlaikus vairākiemm nesen nolīgtiem darbiniekiem.

1. Kreisās puses izvēlnē atlasiet **Veidnes**.
2. Sadaļā **Manas veidnes**atlasiet veidni, kuru vēlaties iestatīt kā pievienošanas ceļvedi nesen nolīgtiem darbiniekiem.
3. Rediģējiet veidni pēc vēlēšanās. Neaizmirstiet saglabāt darbu.
4. Kad esat pabeidzis veidnes rediģēšanu, atlasiet **Izveidot ceļvedi**.
5. Logā **Izveidot ceļvedi** atlasiet **Nepieciešams pievienot vairākus cilvēkus uzreiz**.

    [![Pievienošanas ceļveža izveide vairākiem nesen nolīgtiem darbiniekiem](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)

6. Atlasiet **Nesen nolīgtā darbinieka veidne**.
7. Pēc tam, kad .xlsx fails ir lejupielādēts, atlasiet **Atvērt**, ievadiet darbinieka informāciju Excel darbgrāmatā un saglabājiet darbgrāmatu.

    [![Excel veidnes lejupielāde, lai nosūtītu pievienošanas ceļvedi vairākiem nesen nolīgtiem darbiniekiem](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)

    > [!NOTE]
    > Lai varētu rediģēt darbgrāmatu, programmā Excel jāatlasa **Iespējot rediģēšanu**.
    > 
    > [![Rediģēšanas iespējošana](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)

8. Velciet Excel darbgrāmatu uz norādīto apgabalu logā **Izveidot vairākus ceļvežus** vai noklikšķiniet jebkurā vietā šajā apgabalā, lai pārlūkotu failu datorā.

    [![Rediģētās darbgrāmatas vilkšana](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)

9. Kad esat pabeidzis rediģēt pievienošanas ceļvedi, augšējā labajā stūrī atlasiet **Sūtīt**. Pēc tam izpildiet kādu no norādītajām darbībām.

    - Lai nosūtītu nesen nolīgtiem darbiniekiem saiti uz pievienošanas ceļvedi, atlasiet **Kopēt saiti** un pēc tam atlasiet **Kopēt**.
    - Lai pielāgotu pievienošanas ceļveža e-pastu pirms nosūtīšanas, atlasiet **Pielāgot e-pastu pirms nosūtīšanas**, atlasiet **Tālāk**, pielāgojiet e-pasta ziņojumu, kā vēlaties, un pēc tam atlasiet **Sūtīt**.
    - Lai nosūtītu e-pasta ziņojumu, to nepielāgojot, atlasiet **Tālāk** un pēc tam atlasiet  **Sūtīt**.

## <a name="create-a-guide-without-using-a-template"></a>Ceļveža izveide bez veidnes izmantošanas

Ne vienmēr ir jāveido ceļvedis no veidnes. Ja vēlaties, varat izveidot ceļvedi no nulles.

1. Kreisās puses izvēlnē atlasiet **Ceļveži** un pēc tam atlasiet pogu **Pievienot** (pluszīme \[**+**\]).
2. Logā **Izveidot ceļvedi** sadaļā **Kuru jūs pievienojat** ievadiet nesen nolīgtā darbinieka vārdu vai e-pasta adresi. Ja nesen nolīgtais darbinieks vēl nav sistēmā, atlasiet **Pievienot tūlīt** un ievadiet darbinieka informāciju.

    ![[Informācijas ievadīšana pievienošanas ceļvedim](./Media/Onboard-Create-a-Guide-Window.png)](./media/onboard-create-a-guide-window.png)

3. Sadaļā **Kad viņi sāks**atlasiet sākuma datumu.
4. Ja pievienošanas ceļvedis ir automātiski jānosūta nesen nolīgtam darbiniekam konkrētā datumā, pārliecinieties, vai ir ieslēgta opcija **Ieplānot automātiskas nosūtīšanas datumu** un pēc tam atlasiet automātiskās nosūtīšanas datumu. Lai ceļvedi nosūtītu nekavējoties, izslēdziet opciju **Ieplānot automātiskās nosūtīšanas datumu**.
5. Atlasiet **Gatavs**.

## <a name="save-a-guide-as-a-template"></a>Saglabāt ceļvedi kā veidni

Pievienošanas ceļvedi var saglabāt kā veidni. Tādējādi varat ietaupīt laiku, kad vēlāk ir jāizveido vairāk pievienošanas ceļvežu.

1. Kreisās puses izvēlnē atlasiet **Ceļveži**.
2. Atlasiet pogu **Vairāk** (daudzpunkte \[**...**\]) ceļvedim, no kura vēlaties izveidot veidni, un pēc tam atlasiet **Saglabāt kā veidni**.

    ![[Saglabāt pievienošanas ceļvdi kā veidni](./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. Logā **Saglabāt kā jaunu veidni** ievadiet jaunās veidnes nosaukumu un pēc tam atlasiet **Saglabāt**.

## <a name="next-steps"></a>Nākamās darbības

- [Pievienošanas ceļvežu un veidņu rediģēšana](./onboard-edit-guides-templates.md)
- [Satura kopīgošana ar citiem ieguldītājiem](./onboard-share-template.md)
- [Uzdevumu un pievienoto darbinieku statusa skatīšana](./onboard-view-status.md)
- [Par pieņemšanu darbā atbildīgo grupu izveide Onboard](./onboard-create-team.md)

### <a name="see-also"></a>Skatiet arī

- [Programmas Onboard izmēģināšana vai iegāde](https://dynamics.microsoft.com/talent/onboard/)
- [Jaunumi](./whats-new.md)
- [Piezīmes par laidienu](https://docs.microsoft.com/business-applications-release-notes/index)
- [Atbalsta saņemšana](./talent-support.md)
