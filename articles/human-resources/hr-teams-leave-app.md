---
title: Atvaļinājuma pieprasījumu pārvaldība programmā Teams
description: Šajā tēmā parādīts, kā pieprasīt prombūtni Dynamics 365 Human Resources programmā Microsoft Teams.
author: andreabichsel
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aec6d784fd6bd54297ac4204c834c7f77ed75362
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356516"
---
# <a name="manage-leave-requests-in-teams"></a>Atvaļinājumu pieprasījumu pārvaldība programmā Teams

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources programma sadaļā Microsoft Teams ļauj ātri pieprasīt prombūtni un skatīt savas prombūtnes bilances informāciju Microsoft Teams. Varat mijiedarboties ar botu, lai pieprasītu informāciju un sāktu atvaļinājuma pieprasījumu. Cilne **Brīvais laiks** sniedz detalizētu informāciju. Varat arī nosūtīt personām informāciju par gaidāmo prombūtni programmā Teams un tērzēšanā ārpus Human Resources programmas.

## <a name="install-the-app"></a>Programmas instalēšana

Dynamics 365 Human Resources programmu varat atrast Teams veikalā.

1. Programmā Microsoft Teams pārejiet uz programmu sarakstu.
 
2. Meklējiet Dynamics 365 Human Resources un pēc tam atlasiet elementu **Personāla vadība**.

3. Atlasiet pogu **Pievienot**, lai instalētu programmu.

Ja programma jūs automātiski nepieraksta, atlasiet cilni **Iestatījumi**, lai pierakstītos.

> [!NOTE]
> Ja nav redzams pierakstīšanās dialoglodziņš, pārbaudiet pārlūkprogrammas iestatījumus, lai atļautu uznirstošos elementus. 

Ja jums ir piekļuve vairāk nekā vienai Human Resources instancei, varat atlasīt, ar kuru vidi vēlaties veidot savienojumu, cilnē **Iestatījumi**.

> [!NOTE]
> Programma tagad atbalsta Sistēmas administratora drošības lomu.
 
## <a name="use-the-bot"></a>Bota izmantošana

Pēc programmas instalēšanas, tiek parādīts sveiciena ziņojums, informējot jūs par darbību veidiem, ko bots var veikt jūsu vārdā.

> [!NOTE]
> Pirmo reizi izmantojot botu, var būt nepieciešams pierakstīties. Ja nav redzams pierakstīšanās dialoglodziņš, pārbaudiet pārlūkprogrammas iestatījumus, lai atļautu uznirstošos elementus.

Varat lūgt botam:

- Skatīt jūsu pašreizējo atvaļinājumu bilances. Piemēram, nosūtiet ziņojumu, kas paziņo "Skatīt atvaļinājumu bilances."

- Izveidot atvaļinājuma pieprasījumu. Piemēram, nosūtiet ziņojumu, kas paziņo "Paņemt atvaļinājumu" vai "Es vēlos paņemt atvaļinājuma laiku nākamajā ceturtdienā un piektdienā", lai konkrētāk veiktu pieprasījumu atvaļinājuma pieprasīšanas veidam. 

  ![Sākt atvaļinājuma pieprasījumu Teams tērzētavā.](./media/hr-teams-leave-app-initiate.png)

- Tērzēšanas bots aizpildīs jūsu atvaļinājuma pieprasījumu. Atlasiet **Izslēgt pieprasījuma laiku** un rediģējiet detalizētu informāciju par jūsu pieprasījumu.

   Ja vēlaties iesniegt atvaļinājumu pieprasījumus vairākiem atvaļinājumu tipiem vienā datumā, atlasiet opciju **Sadalīt dienu ar** izvēlnē **Papildu opcijas**. 

   Ja izvēlaties pusdienas atvaļinājumu, kad atvaļinājuma pieprasījuma vienība ir dienās, varat norādīt, vai vēlaties pieprasīt brīvo laiku pirmajā dienas pusē vai otrajā, izvēloties opciju **Pusdienas definīcija** izvēlnē **Papildu opcijas**.
   
   ![Pusdienas definēšana.](./media/HalfDayDefinitions.png)

- Kad esat beidzis rediģēt atvaļinājuma pieprasījuma detaļas, atlasiet **Iesniegt**, lai to iesniegtu apstiprināšanai.

  ![Iesniegt atvaļinājuma pieprasījumu.](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a>Atvaļinājuma pārvaldība programmā Teams

Cilne **Brīvais laiks** ļauj skatīt: 

- Bilances informāciju katram atvaļinājuma veidam, kurā esat reģistrēts

- Gaidāmos atvaļinājuma pieprasījumus

- Prombūtnes pieprasījumus

- Melnraksta atvaļinājuma pieprasījumus
 
### <a name="create-a-new-request"></a>Jauna pieprasījuma izveidošana

1. Lai izveidotu jaunu atvaļinājuma pieprasījumu, atlasiet **Jauns pieprasījums**.

2. Ievadiet dienu vai dienas, kurās vēlaties ņemt pārtraukumu, un pēc tam atlasiet **Pievienot**.

   ![Human Resources Teams atstāj programmas pievienot prombūtni.](./media/TimeOffHours.png)

3. Ja piemērojams, ievadiet iemesla kodu. Ievadiet arī komentārus un pievienojiet pielikumus.

4. Ja vēlaties iesniegt atvaļinājumu pieprasījumus vairākiem atvaļinājumu tipiem vienā datumā, atlasiet opciju **Sadalīt dienu ar** izvēlnē **Papildu opcijas**.

5. Atlasiet opciju **Pusdienas definīcija**, lai norādītu, vai vēlaties pieprasīt brīvu pirmo dienas pusi vai otro dienas pusi. Šī opcija ir pieejama, ja atvaļinājuma pieprasījuma vienība ir dienās un pieprasītā summa ir 0,5 dienas.

6. Kad esat pabeidzis ievadīt informāciju, ievadiet **Iesniegt**, lai to iesniegtu apstiprināšanai. Varat arī ievadīt **Saglabāt kā melnrakstu**, lai atgrieztos pie tā vēlāk.

### <a name="manage-draft-requests"></a>Melnraksta pieprasījumu pārvaldība

1. Atlasiet cilni **Melnraksti**.

2. Atlasiet zīmuli, lai rediģētu pieprasījumu, vai atlasiet atkritni, lai dzēstu pieprasījumu.

3. Veiciet nepieciešamās izmaiņas. Kad esat pabeidzis ievadīt informāciju, ierakstiet **Iesniegt**, lai to iesniegtu apstiprināšanai. Varat arī atlasīt **Saglabāt kā melnrakstu**, lai atgrieztos pie tā vēlāk.
   
### <a name="respond-to-teams-notifications"></a>Atbildēt uz programmas Teams paziņojumiem

Kad jūs vai darbinieks, kuram jūs esat apstiprinātājs, iesniedz atvaļinājuma pieprasījumu, jums tiek nosūtīts paziņojums Teams risinājuma Human Resources programmā. Varat atlasīt paziņojumu, lai to skatītu. Paziņojumi tiek rādīti arī **Tērzēšanas** zonā.

Ja esat apstiprinātājs, varat izvēlēties **Apstiprināt** vai **Atteikt** paziņojumā. Var arī norādīt neobligātu ziņojumu.

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>Sūtīt gaidāmās prombūtnes informāciju saviem kolēģiem

Pēc tam, kad esat instalējis Human Resources programmu Teams, varat vienkārši nosūtīt informāciju par jūsu gaidāmo prombūtni saviem kolēģiem grupās vai tērzēšanā.

1. Programmas Teams grupā vai tērzēšanā atlasiet Human Resources pogu zem tērzēšanas loga.

   ![Human Resources poga zem tērzēšanas loga.](./media/hr-teams-leave-app-chat-button.png)

2. Atlasiet atvaļinājuma pieprasījumu, kuru vēlaties kopīgot. Ja vēlaties kopīgot melnraksta atvaļinājuma pieprasījumu, vispirms atlasiet **Melnraksti**.

Jūsu atvaļinājuma pieprasījums tiks parādīts tērzēšanā.

Ja esat kopīgojis melnraksta pieprasījumu, tas tiks parādīts kā melnraksts.

## <a name="view-your-teams-leave-calendar"></a>Skatiet savas grupas atvaļinājuma kalendāru

Ja esat vādītājs ar tiešajiem pārskatiem, varat apskatīt savas grupas apstiprināto un gaidošo brīvo laiku.

1. Programmā Human Resources risinājumā Teams atlasiet **Brīvais laiks**.

2. Atlasiet **Grupas kalendārs**. Kalendārā tiek rādīti jūsu tiešo pārskatu apstiprinātais un gaidošais brīvais laiks.

   > [!NOTE]
   > Ja neredzat grupas kalendāru, palūdziet savam administratoram to iespējot. Papildinformāciju skatiet sadaļā [Instalēšana un iestatīšana](hr-admin-teams-leave-app.md#install-and-setup).

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

## <a name="troubleshooting"></a>Problēmu novēršana

Ja jums rodas problēmas, pierakstoties vai izmantojot Dynamics 365 Human Resources Teams programmu, izmēģiniet šīs problēmu novēršanas instrukcijas. Ja pēc problēmu novēršanas problēmas joprojām pastāv, sazinieties ar atbalsta dienestu. Lai iegūtu papildinformāciju, skatiet [Iegūt atbalstu](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Nevar pierakstīties personāla vadības lietojumprogrammā Teams

Ja nevarat pierakstīties lietojumprogrammā, iespējams, ka konts, kuru izmantojat, lai pierakstītos Microsoft Teams nav saistīts ar darbinieka ierakstu Dynamics 365 Human Resources. Sazinieties ar sistēmas administratoru, lai pārliecinātos, ka darbinieka ieraksts ir pareizi saistīts.

### <a name="translations-dont-display-correctly"></a>Tulkojumi netiek rādīti pareizi

Ja tulkojumi netiek rādīti kā gaidīti, pārliecinieties, ka programmā Teams atlasītā valoda atbilst Human Resources atlasītajai valodai sadaļā **Lietotāja opcijas**.

Teams sadaļā skatiet **Programmas valoda** **Iestatījumos**.

![Teams iestatījumi.](./media/hr-teams-leave-app-settings.png)

Sadaļā Cilvēkresursi atlasiet **Iestatījumi** un pēc tam atlasiet **Lietotāja opcijas**. Pārbaudiet, vai lauks **Valoda** atbilst **Lietojumprogrammas valodas** laukam programmā Teams.

![Cilvēkresursu Lietotāja opcijas.](./media/hr-teams-leave-app-user-options.png)

Ja joprojām pastāv tulkošanas problēmas, ļauj mums zināt. Papildinformāciju skatiet sadaļā [Iegūt atbalstu Finance and Operations programmām vai Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Kļūda, apstiprinot atvaļinājumu pieprasījumus personāla vadības lietojumprogrammā Teams

Ja jūs saņemat kļūdu, mēģinot apstiprināt atvaļinājumu pieprasījumus lietojumprogrammā Teams, mēģiniet veikt tālāk norādītos problēmu novēršanas pasākumus:

1. Pārbaudiet, vai konts, kuru izmantojat, lai pierakstītos Microsoft Teams ir tas pats, ko izmantojat, lai piekļūtu Dynamics 365 Human Resources.

2. Pārbaudiet, vai esat derīgs pieprasījuma apstiprinātājs, pārbaudot darbplūsmas iestatījumus atvaļinājumu apstiprināšanai. Papildinformāciju par atvaļinājumu pieprasījumu darbplūsmām skatiet šeit: [Atvaļinājuma pieprasījuma darbplūsmas izveide](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Atvainājuma apstiprinātāji nesaņem Teams tērzēšanas ziņojumus, lai apstiprinātu atvaļinājuma pieprasījumus

1. Pārliecinieties, vai videi un lietotājam ir iespējoti paziņojumi. Papildinformāciju skatiet sadaļā [Iespējot paziņojumus programmai Human Resources pakalpojumā Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) un [Ieslēgt vai izslēgt paziņojumus atsevišķiem lietotājiem](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Pārliecinieties, vai lietotāji ir pierakstījušies cilnē **Tērzēšana** ar tiem pašiem akreditācijas datiem, ko tie izmanto atvaļinājumu pieprasījumu apstiprināšanai. Lietojiet ziņojumus "izrakstīties" un pēc tam "pieteikties", lai pieteiktos, izmantojot pareizos akreditācijas datus.

3. Ja problēma joprojām pastāv, pārbaudiet biznesa notikumu sistēmas pakešuzdevuma statusu kā sistēmas administrators. Ja tas ir gaidīšanas vai izpildes posmā, pārbaudiet atpakaļ pēc dažām minūtēm. Ja statuss paliek nemainīgs, reģistrējiet atbalsta biļeti, lai mūsu komanda varētu palīdzēt atrisināt šo problēmu.

## <a name="known-accessibility-issues"></a>Zināmās pieejamības problēmas

Personāla vadības programmā risinājumā Teams ir šādas pieejamības problēmas, pie kurām mēs strādājam turpmākajos laidienos.

| Izsniegt | Profilakse vai skaidrojums |
| --- | --- |
| Tālummaiņa līdz 400% darbvirsmā slēpj dažas darbības pogas no skata. | Mēs iesakām izmantot lupu, kamēr mēs varam atbalstīt šo tālummaiņas līmeni. |
| Cilnē **Pārtraukums** aizkadra balss paziņo par pogas darbību, kamēr tiek lasīts pārtraukuma režģa virsraksts. | Galvene un elementi režģī tiek grupēti pēc gada, un tie ir saliekami. Aizkadra balss to interpretē kā rīcībā esošu krājumu, bet tā nav. |
| Cilnē **Pārtraukums** ir papildu vilkšanas žests, navigējot uz **Iemesla kodu** jaunā pieprasījumā. | Nav nevienas slēptas kontroles, ko vilkšanas navigācija mēģina iegūt. |
| Ja cilnē **Pārtraukums** veicat vilkšanas žestu, kamēr ir atvērts kalendārs, jūs nokļūsiet ārpus vadīklas, nevis jauna pieprasījuma sākumā vai pieprasījuma rediģēšanā. | Kad sasniedzat **Doties uz šodienu**, ņemiet vērā, ka tās ir vadīklas beigas, pavelciet uz pretējo pusi, lai atgrieztos augšā. |
| Kad cilnē **Tērzēšana** ievadāt datumu, kamēr izmantojat atbalsta rīku vai tastatūras navigāciju, fokuss pārlec uz augšu. | Nospiediet cilni, līdz atkal tiek sasniegts ievades apgabals. |

## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft valodu izpratnes intelektiskais pakalpojums (Microsoft Language Understanding Intelligent Service - LUIS)

Ar Dynamics 365 Human Resources botu programmā Microsoft Teams lietotāja teksta ievades tiek analizētas, lai saprastu pamatā esošo vaicājumu/nolūku. Lietotāja ievade, piemēram, "Meklēt kontu Contoso", ir maršrutēta uz vienu no Microsoft Cognitive Service, kas saucas Language Understanding Intelligent Service (LUIS). Lasīt vairāk par LUIS [šeit](https://www.luis.ai/). LUIS pakalpojums izprot lietotāja ievades nolūku (šajā gadījumā nolūks ir meklēt informāciju) un mērķa elementu (šajā gadījumā paredzētā vienība ir konts ar nosaukumu Contoso). Pēc tam šī informācija tiek nodota Microsoft [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), kas mijiedarbojas ar datiem no Dynamics 365 Human Resources un izgūst vēlamo informāciju lietotāja vaicājumam. 

Instalējot un ļaujot izmantot botu, jūs piekrītat, ka ļautat LUIS pakalpojumam un Azure bota struktūrai apstrādāt ievades nodomu, kas rada lielāku sarunvalodas lietotāja pieredzi. LUIS pakalpojums un Azure bota struktūrai var būt dažādi atbilstības līmeņi, salīdzinot ar Dynamics 365 Human Resources. Lai gan LUIS pakalpojums var piekļūt tikai lietotāju vaicājumiem un nav paredzēts pievienot lietotāja Dynamics 365 Human Resources datiem vai kontam, Dynamics 365 Human Resources bota lietotājs var brīvprātīgi ievadīt vaicājumu, kurā ir ietverti klienta dati, personas dati vai citi dati, un šāds vaicājuma saturs varētu tikt nosūtīts uz LUIS pakalpojumu un Azure bota struktūru. 

Lietotāja vaicājumu un ziņojumu saturs tiek saglabāts LUIS sistēmā ne ilgāk kā 30 dienas, tiek šifrēts, un tas netiek izmantots apmācībās vai pakalpojumu uzlabošanā. Lasiet vairāk par Kognitīvajiem pakalpojumiem [šeit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Lai pārvaldītu programmas administrēšanas iestatījumus programmā Microsoft Teams, dodieties uz [Microsoft Teams administrēšanas centru](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid un Azure Cosmos DB

Izmantojot programmu Dynamics 365 Human Resources risinājumā Microsoft Teams, noteikti klienta dati var ieplūst ārpus ģeogrāfiskā reģiona, kurā atrodas jūsu nomnieka Human Resources pakalpojums.

Dynamics 365 Human Resources nosūta darbinieka atvaļinājuma pieprasījumu un darbplūsmas uzdevuma informāciju Microsoft Azure Event Grid un Microsoft Teams. Šos datus var uzglabāt Microsoft Azure Event Grid līdz 24 stundām un tie tiks apstrādāti Amerikas Savienotajās Valstīs, tie ir šifrēti tranzītā un bez tā, un Microsoft vai tās apakšprocesori tos neizmanto apmācības vai pakalpojumu uzlabošanai. Lai saprastu, kur dati tiek glabāti programmā Teams, lūdzu, skatiet sadaļu: [Datu atrašanās vieta Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Sarunājoties ar botu Human Resources programmā, sarunas saturs var tikt saglabāts Azure Cosmos DB un pārsūtīts uz Microsoft Teams. Šie dati var tikt glabāti Azure Cosmos DB līdz 24 stundām un tos var apstrādāt ārpus ģeogrāfiskā reģiona, kurā atrodas jūsu nomnieka Human Resources pakalpojums, tie ir šifrēti tranzītā un bez tā, un Microsoft vai tās apakšprocesori tos neizmanto apmācības vai pakalpojumu uzlabošanai. Lai saprastu, kur dati tiek glabāti programmā Teams, lūdzu, skatiet sadaļu: [Datu atrašanās vieta Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Lai ierobežotu piekļuvi Human Resources programmai Microsoft Teams jūsu organizācijā vai lietotājiem jūsu organizācijā, skatiet sadaļu [Programmu atļauju ierobežojumu pārvaldība sistēmā Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Skatiet arī

[Lejupielāde un instalēšana Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams palīdzības centrs](https://support.office.com/teams)</br>
[Programma Human Resources programmā Teams](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
