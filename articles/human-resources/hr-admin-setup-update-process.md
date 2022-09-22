---
title: Procesa atjaunināšana
description: Microsoft Dynamics 365 Human Resources ir īsts programmatūras pakalpojums (software as a service — SaaS), kas nodrošina nepārtrauktus, bezkontakta pakalpojumu atjauninājumus lietojumprogrammu un platformu izmaiņām.
author: twheeloc
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 71815866ef9674f317b7f08ecf2a65b465ddfff3
ms.sourcegitcommit: d2046cad5de570e6302a4390b41881a7ecb12e26
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/15/2022
ms.locfileid: "9520815"
---
# <a name="update-process"></a>Procesa atjaunināšana

_**Attiecas uz:** savrupas infrastruktūras personāla vadība_ 

> [!NOTE]
> Sākot no 2022. gada, jaunus cilvēkresursu vides nevar nodrošināt savrupos cilvēkresursu infrastruktūras un jaunos Microsoft Dynamics Lifecycle Services (LCS) projektos nevar izveidot tajā. Klienti var izvietot cilvēkresursu vides finanšu un operāciju infrastruktūrai. Papildinformāciju skatiet finanšu [un operāciju infrastruktūras sadaļu Personāla vadības nodrošināšana](hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Finanšu un operāciju programmas infrastruktūras atjaunināšanas un labojumfaila process atšķiras no cilvēkresursu savrupā atjaunināšanas un labojumfaila procesa. Papildinformāciju par atjaunināšanas procesu skatiet sadaļā ["Apstrādāt, lai pārietu uz pēdējo finanšu un operāciju atjauninājumu"](../fin-ops-core/dev-itpro/migration-upgrade/upgrade-latest-update.md). Papildinformāciju par labojumfailiem skatiet sadaļā [Atjauninājumu lejupielāde no lifecycle Services (LCS).](/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs.md) 

Microsoft Dynamics 365 Human Resources ir īsts programmatūras pakalpojums (software as a service — SaaS), kas nodrošina nepārtrauktus, bezkontakta pakalpojumu atjauninājumus. Šie atjauninājumi ietver gan programmas, gan platformas izmaiņas, kas bieži sniedz būtiskus pakalpojuma uzlabojumus, ieskaitot regulējošos atjauninājumus.

## <a name="update-policy"></a>Atjaunināšanas politika

Atjauninājumi tiek izlaisti ar regulāru kadenci visām vidēm. Human Resources atbalsts tiek nodrošināts saskaņā ar [Microsoft Lifecycle politiku](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), kas nodrošina pastāvīgas un prognozējamas vadlīnijas atbalsta pieejamībai.

## <a name="release-cadence"></a>Laidienu kadence 

Human Resources atjauninājumi tiek automātiski piemēroti visām vidēm. Human Resources nodrošina divu veidu laidienus.

- **Pakalpojuma atjauninājumi**: Atjauninājumi tiek veikti reizi divās nedēļās un ietver kļūdu labojumus un jaunus līdzekļus. Pakalpojumu atjauninājumi ietver arī piemērojamos platformas atjauninājumus, kad tie tiek izlaisti. Papildinformāciju par platformu laidieniem skatiet [sadaļā Kas jauns vai mainīts platformu atjauninājumos](../fin-ops-core/dev-itpro/get-started/whats-new-home-page.md). Atjauninājumiem ir stadijas globāla atrite reģionos. Papildinformāciju par atjauninājumiem skatiet [sadaļā Kas jauns vai mainīts Dynamics 365 Human Resources](hr-admin-whats-new.md).

- **Dataverse risinājuma atjauninājumi**: šie atjauninājumi pēc nepieciešamības parādās aptuveni ik pēc sešām nedēļām. Tie ietver jaunus elementus un izmaiņas esošajos elementos Dataverse. Šie atjauninājumi tiek izlaisti tiem pašiem reģioniem kā divu nedēļu atjauninājumi, un to replicēt pa visiem datu centriem ir aptuveni sešas nedēļas. Risinājumu atjauninājumi var būt vai var nebūt saskaņoti ar pakalpojumu atjauninājumiem reizi divās nedēļās.

> [!NOTE]
> Kad tie tiek izlaisti, risinājuma atjauninājumi ir pieejami visiem datu centriem. Ja nevēlaties gaidīt, kamēr atjauninājumi tiek kopēti automātiski, varat lietot šos atjauninājumus manuāli jebkurā vidē jebkurā datu centrā.

Nepieciešamības gadījumā cilvēkresursi nodrošina šādus labojumus tipus:

- **Pārstrādātais izdevums (labojumfails**): Kļūdu labojumi, kas var būt vai nu kopā ar pakalpojuma atjaunināšanas, kas notiek reizi divās nedēļās, laidienu, vai atsevišķi no tā

- **Ārkārtas labojums**: Proaktīvi un reaktīvi labojumfaili, kas ir pēc būtības ir paši par sevi, var ietvert tikai konfigurācijas vai koda izmaiņas, lai atrisinātu tiešsaistes vietnes problēmas, un tie var būt atsevišķi no iknedēļas pakalpojuma atjaunināšanas, kas notiek reizi divās nedēļās, laidiena

Laidieni tiek pārbaudīti, testēti un apstiprināti iekšējā vidē. Pēc izveidotā ir izrakstīšanas, tas tiek izvietots ražošanā.

## <a name="release-cadence-exceptions-in-2021"></a>Laidienu ritma izņēmumi 2021. gadā

Lai uzskaitītu brīvdienas, 2021. gada novembra un decembra izlaišanas grafiks ir šāds:

- Novembra izlaidums: 1. novembris - 14. novembris
- Decembra izlaidums: 29. novembris - 12. decembris
 
Divu nedēļu izlaidumu kadence tiks atsākta kā parasti 2022. gada 10. janvārī.

## <a name="communications"></a>Komunikācija

Tālāk minētajās vietās varat uzzināt, kas ietverts Human Resources darbībā un kādi bijuši laidieni.

- [Dynamics 365 Human Resources rīcības plāns](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Dynamics 365 laidiena plāni](/dynamics365/release-plans/)

- [Jaunumi un izmaiņas Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [Problēmu meklēšana Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (tikai ar platformu saistītām kļūdām)

- [Human Resources emuārs](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Human Resources Yammer kopiena](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Priekšskatījuma līdzekļi smilškastes vidē

Varat validēt priekšskatījuma līdzekļus smilškastes vidē pirms iespējot tos savā ražošanas vidē. Papildinformāciju par jaunu līdzekļu iespējošanu skatiet [Pārskats par līdzekļu pārvaldību](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Visi jaunie līdzekļi paliek priekšskatījumā vismaz 30 dienas, un parasti 30-60 dienas. Galvenās funkcijas parasti ir pieejamas katra gada oktobrī un aprīlī pēc priekšskatījuma perioda. Tiklīdz jūs redzat jaunas iespējas **Līdzekļu pārvaldības** darbvietā, varat tās ieslēgt. Daži līdzekļi var būt ieslēgti pēc noklusējuma.

Reizēm šis līdzeklis būs ieslēgts pēc noklusējuma, un to nevar izslēgt (piemēram, Līdzekļu pārvaldības darbvieta).

Kolīdz līdzeklis ir vispārīgi pieejams, to var ieslēgt vai izslēgt ražošanas vidēs. **Līdzekļu pārvaldības** darbvieta norāda, kad priekšskatījuma līdzeklis kļūs obligāts. Šis datums parasti ir 1. oktobris vai 1. aprīlis, lai to saskaņotu ar pusgada laidiena plāniem. Jūs nevarat izslēgt obligātos līdzekļus. Kamēr tas kļūst obligāts, varat ieslēgt vai izslēgt līdzekli visās vidēs.

Mēs noteikti iesakām priekšskatīt līdzekļus smilškastes vai izmēģinājuma vidē. Ir ieteicams izveidot pašreizējās ražošanas vides vai datu bāzes kopiju smilškastes vidē, lai varētu iegūt pilnīgu pieredzi ar jaunajiem līdzekļiem, izmantojot savus datus.

Papildinformāciju par smilškastes vides nodrošināšanu skatiet [Human Resources projekta nodrošināšana](hr-admin-setup-provision.md). Lai noņemtu testa vidi, skatiet [Instances noņemšana](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Pārskata sniegšana par kļūdām

Testējot priekšskatījuma līdzekļus vai izmēģinot jaunas iespējas, iespējams, atradīsiet vienumus, kas nedarbojas kā paredzēts. Lūdzu, sniedziet pārskatu par jebkurām kļūdām, izmantojot [Microsoft Dynamics 365 atbalstu](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Skatiet arī

[Dynamics 365 un Power Platform laidiena plāni](/dynamics365/release-plans)</br>
[Jaunumi un izmaiņas Dynamics 365 Human Resources](hr-admin-whats-new.md)</br>
[Programmatūras dzīves cikla politika](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
