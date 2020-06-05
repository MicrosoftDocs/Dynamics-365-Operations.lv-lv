---
title: Atvaļinājuma pieprasījumu pārvaldība programmā Teams
description: Šajā tēmā parādīts, kā pieprasīt prombūtni Dynamics 365 Human Resources programmā Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 67501a1fa65493a1a23eb6176ece5be98d6e4659
ms.sourcegitcommit: 7fc0726c0a93ce6f4dafaad3232b4687f61cdc88
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/21/2020
ms.locfileid: "3393012"
---
# <a name="manage-leave-requests-in-teams"></a>Atvaļinājuma pieprasījumu pārvaldība programmā Teams

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources programma sadaļā Microsoft Teams ļauj ātri pieprasīt prombūtni un skatīt savas prombūtnes bilances informāciju Microsoft Teams. Varat sazināties ar botu, lai pieprasītu informāciju. Cilne **Laiks izslēgts** sniedz detalizētu informāciju.

## <a name="install-the-app"></a>Programmas instalēšana

Personāla vadības programmu varat atrast Teams veikalā.

1. Sadaļā Microsoft Teams atlasiet daudzpunkti.

   ![Human Resources Teams atstāj programmas daudzpunkti](./media/hr-teams-leave-app-ellipses.png)
 
2. Meklējiet Dynamics 365 Human Resources un pēc tam atlasiet elementu **Personāla vadība**.

   ![Human Resources Teams atstāj programmas elementu personāla vadība](./media/hr-teams-leave-app-human-resources-tile.png)

3. Atlasiet pogu **Pievienot**, lai instalētu programmu.

   ![Human Resources Teams atstāj programmas instalēšanu](./media/hr-teams-leave-app-in-store.png)

Ja programma jūs automātiski nepieraksta, atlasiet cilni **Iestatījumi**, lai pierakstītos.

![Human Resources Teams atstāj programmas cilni Iestatījumi](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> Ja nav redzams pierakstīšanās dialoglodziņš, pārbaudiet pārlūkprogrammas iestatījumus, lai atļautu uznirstošos elementus. 

Ja jums ir piekļuve vairāk nekā vienai Human Resources instancei, varat atlasīt, ar kuru vidi vēlaties veidot savienojumu, cilnē **Iestatījumi**.

> [!WARNING]
> Programma pašlaik neatbalsta sistēmas administratora drošības lomu un tiks parādīts kļūdas ziņojumu, ja pierakstīsities ar sistēmas administratora kontu. Lai pierakstītos ar citu kontu, cilnē **Iestatījumi** atlasiet pogu **Kontu pārslēgšana** un pēc tam pierakstieties ar lietotāja kontu, kam nav sistēmas administratora privilēģiju.
 
## <a name="use-the-bot"></a>Bota izmantošana

Pēc programmas instalēšanas, tiek parādīts sveiciena ziņojums, informējot jūs par darbību veidiem, ko bots var veikt jūsu vārdā.

![Human Resources Teams atstāj programmas bota sveiciena ziņojumu](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> Pirmo reizi izmantojot botu, var būt nepieciešams pierakstīties. Ja nav redzams pierakstīšanās dialoglodziņš, pārbaudiet pārlūkprogrammas iestatījumus, lai atļautu uznirstošos elementus.

Varat lūgt botam:

- Rādīt prombūtnes bilances informāciju katram atvaļinājuma veidam, kurā esat reģistrēts.

   ![Human Resources Teams atstāj programmas bilances rādīšanu](./media/hr-teams-leave-app-bot-balances.png)
 
- Rādīt papildu informāciju par konkrētu atvaļinājuma veidu.

   ![Human Resources Teams atstāj programmas informācijas rādīšanu](./media/hr-teams-leave-app-bot-details.png)

- Izveidot atvaļinājuma pieprasījumu.

   ![Human Resources Teams atstāj programmas atvaļinājuma pieprasījumu](./media/hr-teams-leave-app-bot-request.png)
 
Sākot atvaļinājuma pieprasījumu, varat pielāgot dienas tieši kartītē, vai atlasīt **Rediģēt informāciju**, lai pievienotu papildinformāciju savam pieprasījumam.

![Human Resources Teams atstāj programmas rediģēšanas pieprasījumu](./media/hr-teams-leave-app-bot-edit.png)
 
Kad esat pabeidzis ievadīt informāciju, ierakstiet **Iesniegt**, lai to iesniegtu apstiprināšanai. Varat arī ierakstīt **Saglabāt kā melnrakstu**, lai atgrieztos pie tā vēlāk.

![Human Resources Teams atstāj programmas pieprasījuma iesniegšanu](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>Atvaļinājuma pārvaldība programmā Teams

Cilne **Prombūtne** ļauj skatīt:

- Bilances informāciju katram atvaļinājuma veidam, kurā esat reģistrēts

- Gaidāmos atvaļinājuma pieprasījumus

- Prombūtnes pieprasījumus

- Melnraksta atvaļinājuma pieprasījumus

![Personāla vadība Teams atstāj programmas cilni Laiks izslēgts](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>Jauna pieprasījuma izveidošana

1. Lai izveidotu jaunu atvaļinājuma pieprasījumu, atlasiet **Jauns pieprasījums**.

   ![Human Resources Teams atstāj programmas Jauns pieprasījums](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. Ievadiet dienu vai dienas, kurās vēlaties ņemt pārtraukumu, un pēc tam atlasiet **Pievienot**.

   ![Human Resources Teams atstāj programmas pievienot prombūtni](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. Ja piemērojams, ievadiet iemesla kodu. Ievadiet arī komentārus un pievienojiet pielikumus.

4. Kad esat pabeidzis ievadīt informāciju, ierakstiet **Iesniegt**, lai to iesniegtu apstiprināšanai. Varat arī ierakstīt **Saglabāt kā melnrakstu**, lai atgrieztos pie tā vēlāk.

### <a name="manage-draft-requests"></a>Melnraksta pieprasījumu pārvaldība

1. Atlasiet cilni **Melnraksti**.

   ![Human Resources Teams atstāj programmas cilni Melnraksti](./media/hr-teams-leave-app-drafts-tab.png)

2. Atlasiet zīmuli, lai rediģētu pieprasījumu, vai atlasiet atkritni, lai dzēstu pieprasījumu.

3. Veiciet nepieciešamās izmaiņas. Kad esat pabeidzis ievadīt informāciju, ierakstiet **Iesniegt**, lai to iesniegtu apstiprināšanai. Varat arī atlasīt **Saglabāt kā melnrakstu**, lai atgrieztos pie tā vēlāk.

   ![Human Resources Teams atstāj programmas rediģēšanas melnraksts](./media/hr-teams-leave-app-drafts-edit.png)
   
## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti

Ar Dynamics 365 Human Resources botu programmā Microsoft Teams lietotāja teksta ievades tiek analizētas, lai saprastu pamatā esošo vaicājumu/nolūku. Lietotāja ievade, piemēram, "Meklēt kontu Contoso", ir maršrutēta uz vienu no Microsoft izziņas pakalpojumiem, kas saucas Valodas izpratnes inteliģences serviss (LUIS). Lasīt vairāk par LUIS  [šeit](https://www.luis.ai/). LUIS pakalpojums izprot lietotāja ievades nolūku (šajā gadījumā nolūks ir meklēt informāciju) un mērķa elementu (šajā gadījumā paredzētā vienība ir konts ar nosaukumu Contoso). Pēc tam šī informācija tiek nodota Microsoft  [Azure bota struktūrai](https://azure.microsoft.com/services/bot-service/) , kas mijiedarbojas ar datiem no Dynamics 365 Human Resources un izgūst vēlamo informāciju lietotāja vaicājumam. 

Instalējot un ļaujot izmantot botu, jūs piekrītat, ka ļautat LUIS pakalpojumam un Azure bota struktūrai apstrādāt ievades nodomu, kas rada lielāku sarunvalodas lietotāja pieredzi. LUIS pakalpojums un Azure bota struktūrai var būt dažādi atbilstības līmeņi, salīdzinot ar Dynamics 365 Human Resources. Lai gan LUIS pakalpojums var piekļūt tikai lietotāju vaicājumiem un nav paredzēts pievienot lietotāja Dynamics 365 Human Resources datiem vai kontam, Dynamics 365 Human Resources bota lietotājs var brīvprātīgi ievadīt vaicājumu, kurā ir ietverti klienta dati, personas dati vai citi dati, un šāds vaicājuma saturs varētu tikt nosūtīts uz LUIS pakalpojumu un Azure bota struktūru. 

Lietotāja vaicājumu un ziņojumu saturs tiek saglabāts LUIS sistēmā ne ilgāk kā 30 dienas, tiek šifrēts, un tas netiek izmantots apmācībās vai pakalpojumu uzlabošanā. Lasiet vairāk par Kognitīvajiem pakalpojumiem  [šeit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Lai pārvaldītu programmas administrēšanas iestatījumus programmā Microsoft Teams, dodieties uz [Microsoft Teams administrēšanas centru](https://admin.teams.microsoft.com/). 

## <a name="see-also"></a>Skatiet arī

[Lejupielāde un instalēšana Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams palīdzības centrs](https://support.office.com/teams)</br>
[Programma Human Resources programmā Teams](hr-admin-teams-leave-app.md)
