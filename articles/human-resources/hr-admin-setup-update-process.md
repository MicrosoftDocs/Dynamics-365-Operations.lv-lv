---
title: Procesa atjaunināšana
description: Microsoft Dynamics 365 Human Resources ir īsts programmatūras pakalpojums (software as a service — SaaS), kas nodrošina nepārtrauktus, bezkontakta pakalpojumu atjauninājumus lietojumprogrammu un platformu izmaiņām.
author: andreabichsel
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2af1f710ca010041bd684bca8ecfa6f20ac30d46
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063114"
---
# <a name="update-process"></a>Procesa atjaunināšana

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Microsoft Dynamics 365 Human Resources ir īsts programmatūras pakalpojums (software as a service — SaaS), kas nodrošina nepārtrauktus, bezkontakta pakalpojumu atjauninājumus. Šie atjauninājumi ietver gan programmas, gan platformas izmaiņas, kas bieži sniedz būtiskus pakalpojuma uzlabojumus, ieskaitot regulējošos atjauninājumus.

## <a name="update-policy"></a>Atjaunināšanas politika

Atjauninājumi tiek izlaisti ar regulāru kadenci visām vidēm. Human Resources atbalsts tiek nodrošināts saskaņā ar [Microsoft Lifecycle politiku](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), kas nodrošina pastāvīgas un prognozējamas vadlīnijas atbalsta pieejamībai.

## <a name="release-cadence"></a>Laidienu kadence 

Human Resources atjauninājumi tiek automātiski piemēroti visām vidēm. Human Resources nodrošina divu veidu laidienus.

- **Pakalpojuma atjauninājumi**: Atjauninājumi tiek veikti reizi divās nedēļās un ietver kļūdu labojumus un jaunus līdzekļus. Pakalpojuma atjauninājumi iekļauj arī noderīgus platformas atjauninājumus, kad tie tiek izlaisti. Lai iegūtu priekšstatu par to, kad tiek izlaisti platformas atjauninājumi, skatiet [3. tabula: platformas laidieni](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases). Atjauninājumiem, kas tiek veikti reizi divās nedēļās, ir pakāpeniska globāla izlaišana reģionos. Papildinformāciju par atjauninājumiem reizi divās nedēļās skatiet [Jaunumi un izmaiņas Dynamics 365 Human Resources](hr-admin-whats-new.md).

    Visi atbalstītie datu centri tiek atjaunināti ik pēc divām nedēļām, ja vien nav norādīts citādi. Atjauninājumos, kas notiek reizi divās nedēļās, ir ietverti ASV, Austrālijas, Eiropas, Apvienotās Karalistes, Āzijas un Kanādas reģioni. 

- **Dataverse risinājuma atjauninājumi**: šie atjauninājumi pēc nepieciešamības parādās aptuveni ik pēc sešām nedēļām. Tie ietver jaunus elementus un izmaiņas esošajos elementos Dataverse. Šie atjauninājumi tiek izlaisti tiem pašiem reģioniem kā atjauninājumi reizi divās nedēļās, un paiet aptuveni sešas nedēļas līdz tie tiek kopēti visos datu centros. Risinājumu atjauninājumi var būt vai var nebūt saskaņoti ar pakalpojumu atjauninājumiem reizi divās nedēļās.

> [!NOTE]
> Kad tie tiek izlaisti, risinājuma atjauninājumi ir pieejami visiem datu centriem. Ja nevēlaties gaidīt, kamēr atjauninājumi tiek kopēti automātiski, varat lietot šos atjauninājumus manuāli jebkurā vidē jebkurā datu centrā.

Ja nepieciešams, Human Resources nodrošina arī tālāk minētos labojumu veidus.

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

Visi jaunie līdzekļi paliek priekšskatījumā vismaz 30 dienas, un parasti 30-60 dienas. Galvenās funkcijas parasti ir pieejamas katra gada oktobrī un aprīlī pēc priekšskatījuma perioda. Tiklīdz jūs redzat jaunas iespējas Līdzekļu pārvaldības darbvietā, varat tās ieslēgt. Daži līdzekļi var būt ieslēgti pēc noklusējuma.

Reizēm šis līdzeklis būs ieslēgts pēc noklusējuma, un to nevar izslēgt (piemēram, Līdzekļu pārvaldības darbvieta).

Kolīdz līdzeklis ir vispārīgi pieejams, to var ieslēgt vai izslēgt ražošanas vidēs. Līdzekļu pārvaldības darbvieta norāda, kad priekšskatījuma līdzeklis kļūs obligāts. Šis datums parasti ir 1. oktobris vai 1. aprīlis, lai to saskaņotu ar pusgada laidiena plāniem. Jūs nevarat izslēgt obligātos līdzekļus. Kamēr tas kļūst obligāts, varat ieslēgt vai izslēgt līdzekli visās vidēs.

Mēs noteikti iesakām priekšskatīt līdzekļus smilškastes vai izmēģinājuma vidē. Ir ieteicams izveidot pašreizējās ražošanas vides vai datu bāzes kopiju smilškastes vidē, lai varētu iegūt pilnīgu pieredzi ar jaunajiem līdzekļiem, izmantojot savus datus.

Papildinformāciju par smilškastes vides nodrošināšanu skatiet [Human Resources projekta nodrošināšana](hr-admin-setup-provision.md). Lai noņemtu testa vidi, skatiet [Instances noņemšana](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Pārskata sniegšana par kļūdām

Testējot priekšskatījuma līdzekļus vai izmēģinot jaunas iespējas, iespējams, atradīsiet vienumus, kas nedarbojas kā paredzēts. Lūdzu, sniedziet pārskatu par jebkurām kļūdām, izmantojot [Microsoft Dynamics 365 atbalstu](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Skatiet arī

[Dynamics 365 un Power Platform laidiena plāni](/dynamics365/release-plans)</br>
[Jaunumi un izmaiņas Dynamics 365 Human Resources](hr-admin-whats-new.md)</br>
[Programmatūras dzīves cikla politika](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]