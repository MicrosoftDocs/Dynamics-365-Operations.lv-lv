---
title: Personāla vadības programma programmā Teams
description: Šī tēma iepazīstina jūs ar programmu Microsoft Dynamics 365 Human Resources sadaļā Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4822cc6560926df878a8b4e9f821b331ede27a8c
ms.sourcegitcommit: 15c68822f4d412bfc609be31b3702f18c81ea0bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2020
ms.locfileid: "3666364"
---
# <a name="human-resources-app-in-teams"></a>Personāla vadības programma programmā Teams

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources programma sadaļā Microsoft Teams ļauj darbiniekiem ātri pieprasīt prombūtni un skatīt savu laiku ārpusbilances informāciju Microsoft Teams. Darbinieki var sazināties ar botu, lai pieprasītu informāciju. Cilne **Laiks izslēgts** sniedz detalizētu informāciju.

![Personāla vadība Teams atstāj programmu botu](./media/hr-admin-teams-leave-app-bot.png)

![Personāla vadība Teams atstāj programmas cilni Laiks izslēgts](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>Instalēt un iestatīt

Personāla vadības programmu varat atrast Teams veikalā. Informāciju par programmu grupu instalēšanu skatiet sadaļā [Pārvaldīt atvaļinājumu pieprasījumus komandās ](hr-teams-leave-app.md).

Lai iegūtu informāciju par programmu atļauju pārvaldību grupās, skatiet sadaļu [programmu atļauju ierobežojumu pārvaldība sistēmā Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="known-issues"></a>Zināmās problēmas

| Izsniegt | Statuss |
| --- | --- |
| Horizontālā ritināšana nedarbojas Android tālruņos | Horizontālā ritināšana nav problēma iOS vai galddatora ierīcēs. Mēs strādājam pie risinājuma Android. |
| Kļūda: radās problēma, meklējot vidi, ar kuru jāizveido savienojums. | Šo kļūdu varat saņemt pat tad, ja esat pārliecinājies, ka lietotājs var piekļūt vienai vai vairākām Human Resources vidēm. Turklāt iespējams, ka neredzēsit visas paredzētās vides. Kamēr mēs novērsīsim šo problēmu, dzēsiet lietotāju un pēc tam importējiet to vēlreiz, lai atrisinātu problēmu. |
| Bilance nav pareiza, iesniedzot prombūtni nākotnes datumam. | Videoklips vēl nav pieejams. Parādās pašreizējā datuma bilance. |
| Samazinot esošā pieprasījumā uzņemto stundu skaitu, **Atlikusī bilance** tiek samazināta, nevis paaugstināta. | Nākotnē šī zināmā problēma tiks risināta. Displejs nav pareizs, bet pareizās summas tiek koriģētas pēc iesniegšanas. |
| Nevar atcelt **Pārskatā** pieprasījumu. | Šī funkcionalitāte pašlaik netiek atbalstīta, un tā tiks pievienota nākošajā laidienā. |
| Bilances informācija tiek aprēķināta no šodienas. | Sistēma pašlaik neparāda uzkrājumu perioda bilances, pat ja tās ir konfigurētas atvaļinājumu un prombūtnes parametros. |

## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti

Ar Dynamics 365 Human Resources botu programmā Microsoft Teams lietotāja teksta ievades tiek analizētas, lai saprastu pamatā esošo vaicājumu/nolūku. Lietotāja ievade, piemēram, "Meklēt kontu Contoso", ir maršrutēta uz vienu no Microsoft izziņas pakalpojumiem, kas saucas Valodas izpratnes inteliģences serviss (LUIS). Lasīt vairāk par LUIS  [šeit](https://www.luis.ai/). LUIS pakalpojums izprot lietotāja ievades nolūku (šajā gadījumā nolūks ir meklēt informāciju) un mērķa elementu (šajā gadījumā paredzētā vienība ir konts ar nosaukumu Contoso). Pēc tam šī informācija tiek nodota Microsoft  [Azure bota struktūrai](https://azure.microsoft.com/services/bot-service/) , kas mijiedarbojas ar datiem no Dynamics 365 Human Resources un izgūst vēlamo informāciju lietotāja vaicājumam. 

Instalējot un ļaujot izmantot botu, jūs piekrītat, ka ļautat LUIS pakalpojumam un Azure bota struktūrai apstrādāt ievades nodomu, kas rada lielāku sarunvalodas lietotāja pieredzi. LUIS pakalpojums un Azure bota struktūrai var būt dažādi atbilstības līmeņi, salīdzinot ar Dynamics 365 Human Resources. Lai gan LUIS pakalpojums var piekļūt tikai lietotāju vaicājumiem un nav paredzēts pievienot lietotāja Dynamics 365 Human Resources datiem vai kontam, Dynamics 365 Human Resources bota lietotājs var brīvprātīgi ievadīt vaicājumu, kurā ir ietverti klienta dati, personas dati vai citi dati, un šāds vaicājuma saturs varētu tikt nosūtīts uz LUIS pakalpojumu un Azure bota struktūru. 

Lietotāja vaicājumu un ziņojumu saturs tiek saglabāts LUIS sistēmā ne ilgāk kā 30 dienas, tiek šifrēts, un tas netiek izmantots apmācībās vai pakalpojumu uzlabošanā. Lasiet vairāk par Kognitīvajiem pakalpojumiem  [šeit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Lai pārvaldītu programmas administrēšanas iestatījumus programmā Microsoft Teams, dodieties uz [Microsoft Teams administrēšanas centru](https://admin.teams.microsoft.com/). 

## <a name="see-also"></a>Skatiet arī 

[Lejupielāde un instalēšana Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams palīdzības centrs](https://support.office.com/teams)</br>
[Atvaļinājumu pieprasījumu pārvaldība programmā Teams](hr-teams-leave-app.md)

