---
title: Programma Human Resources programmā Teams
description: Šī tēma iepazīstina jūs ar programmu Microsoft Dynamics 365 Human Resources sadaļā Microsoft Teams.
author: twheeloc
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8eebe154a19dd8476f6e9d75ebfd69fdc5b9e2b7
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913493"
---
# <a name="human-resources-app-in-teams"></a>Programma Human Resources programmā Teams

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Programmas Microsoft programma ļauj darbiniekiem ātri pieprasīt izslēgšanas laiku un Dynamics 365 Human Resources skatīt informāciju par to Microsoft Teams bilances nelīdzsvarošanu Microsoft Teams. Darbinieki var sazināties ar botu, lai pieprasītu informāciju. Cilne **Brīvais laiks** sniedz detalizētu informāciju. Turklāt darbinieki var nosūtīt personām informāciju par gaidāmo prombūtni grupās un tērzēšanas sarunās ārpus personāla vadības lietojumprogrammas.

![Human Resources Teams atstāj programmu botu.](./media/hr-teams-leave-app-bot.png)

![Personāla vadība Teams atstāj programmas cilni Brīvais laiks.](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources programmas atvaļinājuma pieprasījuma karte.](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Instalēt un iestatīt

Dynamics 365 Human Resources programmu varat atrast Teams veikalā. Informāciju par programmas Teams instalēšanu skatiet sadaļā [Pārvaldīt atvaļinājumu pieprasījumus programmā Teams](hr-teams-leave-app.md).

Lai iegūtu informāciju par programmu atļauju pārvaldību programmā Teams, skatiet sadaļu [Programmu atļauju ierobežojumu pārvaldība sistēmā Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

Ja vēlaties, lai lietotāji programmā skatītu atvaļinājumu un prombūtnes kalendāru, funkcionalitātes pārvaldībā aktivizējiet kalendāru **Atvaļinājums un kavējumi darba komandās**. Lai iegūtu papildinformāciju par priekšskatījuma līdzekļu iespējošanu, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Iespējot paziņojumus programmai Human Resources programmā Teams

Ja vēlaties, lai lietotāji saņemtu paziņojumus par atvaļinājumu pieprasījumiem programmā Teams, paziņojumi ir jāiespējo programmā Dynamics 365 Human Resources.

>[!NOTE]
>Paziņojumus saņems tikai tie lietotāji, kuri ir pieteikušies Teams un izmanto Dynamics 365 Human Resources Teams programmu.

1. Human Resources atlasiet **Sistēmas administrēšana**.

2. Atlasiet **Saites**.

3. Sadaļā **Iestatīšana** atlasiet **Sistēmas parametri**.

4. Cilnē **Vispārīgi** iestatiet **Iespējot paziņojumus Teams programmai** uz **Jā**.

   ![Aktivizējiet Teams programmas paziņojumus Sistēmas parametros.](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Lai ieslēgtu Teams paziņojumus visiem lietotājiem, uzvednē atlasiet **Jā** .

   ![Iespējojiet Teams paziņojumus visiem lietotājiem.](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Ieslēdziet vai izslēdziet Teams paziņojumus atsevišķiem lietotājiem

Pēc tam, kad esat iespējojis paziņojumus Dynamics 365 Human Resources Teams programmai, varat ieslēgt vai izslēgt paziņojumus atsevišķiem lietotājiem.

1. Human Resources atlasiet **Sistēmas administrēšana**.

2. Atlasiet **Saites**.

3. Sadaļā **Lietotāji** atlasiet **Lietotāja opcijas**.

4. Atlasiet cilni **Darbplūsma** .

5. Iestatiet opciju **Iespējot paziņojumus programmai Teams** uz **Jā** , lai lietotājam iespējotu paziņojumus, vai uz **Nē**, lai atspējotu paziņojumus lietotājam.

   ![Iespējojiet Teams programmas paziņojumus cilnē Lietotāju opciju darbplūsma.](./media/hr-admin-teams-leave-app-notifications.png)

6. Atlasiet **Saglabāt**.

## <a name="supported-languages"></a>Atbalstītās valodas

Programma Dynamics 365 Human Resources lietotnē Teams atbalsta šādas valodas:

| Atrašanās vietas ID | Valoda |
| --- | --- |
| de-DE | Vācu (Vācija) |
| es-ES | Spāņu (Spānija) |
| es-MX | Spāņu (Meksika) |
| fr-CA | Franču (Kanāda) |
| fr-FR | Franču (Francija) |
| it-IT | Itāļu (Itālija) |
| nl-NL | Holandiešu (Nīderlande) |
| pt-BR | Portugāļu (Brazīlija) |
| tr-TR | Turku (Turcija) |
| zh-(CN) | Ķīniešu (vienkāršotā) |

## <a name="notes"></a>Piezīmes

Turpmākajiem laidieniem ir noslīdētas šādas darba vienības:

| Darbplūsmas elements | Statuss |
| --- | --- |
| Bilance nav pareiza, iesniedzot prombūtni nākotnes datumam. | Videoklips vēl nav pieejams. Parādās pašreizējā datuma bilance. |
| Nevar atcelt **Pārskatā** pieprasījumu. | Šī funkcionalitāte pašlaik netiek atbalstīta, un tā tiks pievienota nākošajā laidienā. |
| Bilances informācija tiek aprēķināta no šodienas. | Sistēma pašlaik nerāda bilances uzkrājumu periodam, pat ja tā ir konfigurēta atvaļinājumu un **kavējumu parametru** lapā. |

## <a name="troubleshooting"></a>Problēmu novēršana

Ja lietotājam rodas problēmas, pierakstoties vai izmantojot personāla vadības lietojumprogrammu Teams, izmēģiniet šīs problēmu novēršanas instrukcijas. Ja pēc problēmu novēršanas problēmas joprojām pastāv, sazinieties ar atbalsta dienestu. Lai iegūtu papildinformāciju, skatiet [Iegūt atbalstu](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="ensure-the-teams-human-resources-application-is-up-to-date"></a>Nodrošināt, ka grupas Personāla vadības programma ir atjaunināta
Ja rodas problēmas ar darba grupu personāla vadības programmu, jāapstiprina, ka esat palaidis jaunāko versiju. Minimālā atbalstītā versija ir 1.1.5. Instrukcijas par to, kā atjaunināt Teams programmu, skatiet [Brigādes dokumentācijā](/MicrosoftTeams/apps-update-experience).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Nevar pierakstīties personāla vadības lietojumprogrammā Teams

Ja lietotājs sazinās ar jums, jo viņš nevar pierakstīties lietojumprogrammā, pārbaudiet, vai lietotājam ir saistītais darbinieka ieraksts personāla vadībā.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Kļūda, apstiprinot atvaļinājumu pieprasījumus personāla vadības lietojumprogrammā Teams

Ja lietotājs saņem kļūdu, mēģinot apstiprināt atvaļinājumu pieprasījumus darba grupu programmā, mēģiniet veikt šādas traucējummeklēšanas darbības:

1. Pārbaudiet, vai lietotāja Teams konts ir tas pats, ko lietotājs izmanto, lai piekļūtu personāla vadībai.

2. Pārbaudiet, vai lietotājs ir derīgs pieprasījuma apstiprinātājs, pārbaudot darbplūsmas iestatījumus atvaļinājumu apstiprināšanai. Papildinformāciju par atvaļinājumu pieprasījumu darbplūsmām skatiet šeit: [Atvaļinājuma pieprasījuma darbplūsmas izveide](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Atvainājuma apstiprinātāji nesaņem Teams tērzēšanas ziņojumus, lai apstiprinātu atvaļinājuma pieprasījumus

1. Pārliecinieties, vai videi un lietotājam ir iespējoti paziņojumi. Papildinformāciju skatiet sadaļā [Iespējot paziņojumus programmai Human Resources pakalpojumā Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) un [Ieslēgt vai izslēgt paziņojumus atsevišķiem lietotājiem](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Pārliecinieties, vai lietotāji ir pierakstījušies cilnē **Tērzēšana** ar tiem pašiem akreditācijas datiem, ko tie izmanto atvaļinājumu pieprasījumu apstiprināšanai. Lietojiet ziņojumus "izrakstīties" un pēc tam "pieteikties", lai pieteiktos, izmantojot pareizos akreditācijas datus.

3. Ja problēma joprojām pastāv, pārbaudiet biznesa notikumu **sistēmas pakešuzdevuma** statusu kā sistēmas administrators. Ja tas ir posmā Gaida **vai** Notiek **izpilde**, pārbaudiet vēlreiz pēc dažām minūtēm. Ja statuss paliek nemainīgs, reģistrē atbalsta biļeti, lai mūsu komanda varētu palīdzēt atrisināt šo problēmu.

## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft valodu izpratnes intelektiskais pakalpojums (Microsoft Language Understanding Intelligent Service - LUIS)

Ar Dynamics 365 Human Resources Microsoft Teams botu, lietotāja teksta ievades tiek analizētas, lai saprastu pamatā esošo vaicājumu/līdz ar to. Lietotāja ievade, piemēram, "Meklēšanas konta Contoso", tiek maršrutēta uz vienu no Microsoft ko pie ko pie kotācijas pakalpojumiem, ko sauc par valodas zināšanas intelligent service (GUID). Lasīt vairāk par LUIS [šeit](https://www.luis.ai/). LUIS pakalpojums izprot lietotāja ievades nolūku (šajā gadījumā nolūks ir meklēt informāciju) un mērķa elementu (šajā gadījumā paredzētā vienība ir konts ar nosaukumu Contoso). Pēc tam šī informācija tiek nodota Microsoft [Azure bota struktūrā](https://azure.microsoft.com/services/bot-service/), kura mijiedarbojas ar datiem un izgūst lietotāja Dynamics 365 Human Resources vaicājumam vēlamo informāciju.

Instalējot un ļaujot izmantot botu, jūs piekrītat, ka ļautat LUIS pakalpojumam un Azure bota struktūrai apstrādāt ievades nodomu, kas rada lielāku sarunvalodas lietotāja pieredzi. LUIS pakalpojums un Azure bota struktūrai var būt dažādi atbilstības līmeņi, salīdzinot ar Dynamics 365 Human Resources. Lai gan JUMS ir piekļuve tikai lietotāja vaicājumiem un nav izveidota, lai tas būtu paredzēts savienojumam ar lietotāja datiem vai kontu, bota lietotājs var ievadīt vaicājumu, kurā ir Klienta dati, Personas dati vai citi dati, kā arī šāda vaicājuma saturs var tikt nosūtīts uz BOT pakalpojumu un Dynamics 365 Human Resources Dynamics 365 Human Resources Azure bot struktūru. 

Lietotāja vaicājumu un ziņojumu saturs tiek saglabāts UZ NE vairāk kā 30 dienām, bet netiek lietots apmācības vai pakalpojumu uzlabošanas sistēmā. Lasiet vairāk par Kognitīvajiem pakalpojumiem [šeit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Lai pārvaldītu programmas administrēšanas iestatījumus programmā Microsoft Teams, dodieties uz [Microsoft Teams administrēšanas centru](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid un Azure Cosmos DB

Izmantojot programmu, noteikti debitora dati var plūst ārpus ģeogrāfiskā reģiona, kur Dynamics 365 Human Resources Microsoft Teams izvietots jūsu nomnieka Cilvēkresursu pakalpojums.

Dynamics 365 Human Resources pārsūta darbinieka atvaļinājuma pieprasījumu un darbplūsmas uzdevuma detaļas uz Notikuma Microsoft Azure režģi Microsoft Teams un. Šos datus var uzglabāt Microsoft Azure Event Grid līdz 24 stundām un tie tiks apstrādāti Amerikas Savienotajās Valstīs, tie ir šifrēti tranzītā un bez tā, un Microsoft vai tās apakšprocesori tos neizmanto apmācības vai pakalpojumu uzlabošanai. Lai saprastu, kur dati tiek glabāti programmā Teams, lūdzu, skatiet sadaļu: [Datu atrašanās vieta Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Sarunājoties ar botu Human Resources programmā, sarunas saturs var tikt saglabāts Azure Cosmos DB un pārsūtīts uz Microsoft Teams. Šie dati var tikt glabāti Azure Cosmos DB līdz 24 stundām un tos var apstrādāt ārpus ģeogrāfiskā reģiona, kurā atrodas jūsu nomnieka Human Resources pakalpojums, tie ir šifrēti tranzītā un bez tā, un Microsoft vai tās apakšprocesori tos neizmanto apmācības vai pakalpojumu uzlabošanai. Lai saprastu, kur dati tiek glabāti programmā Teams, lūdzu, skatiet sadaļu: [Datu atrašanās vieta Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Lai ierobežotu piekļuvi Human Resources programmai Microsoft Teams jūsu organizācijā vai lietotājiem jūsu organizācijā, skatiet sadaļu [Programmu atļauju ierobežojumu pārvaldība sistēmā Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Skatiet arī 

[Lejupielāde un instalēšana Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams palīdzības centrs](https://support.office.com/teams)</br>
[Atvaļinājumu pieprasījumu pārvaldība programmā Teams](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
