---
title: Atjaunināšanas process
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1817e072805bafbf0d5a9eb2698ef75abc75ad68
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031094"
---
# <a name="update-process"></a>Atjaunināšanas process

Microsoft Dynamics 365 Human Resources ir īsts programmatūras pakalpojums (software as a service — SaaS), kas nodrošina nepārtrauktus, bezkontakta pakalpojumu atjauninājumus. Šie atjauninājumi ietver gan programmas, gan platformas izmaiņas, kas bieži sniedz būtiskus pakalpojuma uzlabojumus, ieskaitot regulējošos atjauninājumus.

## <a name="update-policy"></a>Atjaunināšanas politika

Atjauninājumi tiek izlaisti ar regulāru kadenci visām vidēm. Human Resources atbalsts tiek nodrošināts saskaņā ar [Microsoft Lifecycle politiku](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), kas nodrošina pastāvīgas un prognozējamas vadlīnijas atbalsta pieejamībai.

## <a name="release-cadence"></a>Laidienu kadence

Human Resources atjauninājumi tiek automātiski piemēroti visām vidēm. Human Resources nodrošina divu veidu laidienus.

- **Pakalpojuma atjauninājumi**: iknedēļas atjauninājumi, kas ietver kļūdu labojumus un jaunus līdzekļus. Pakalpojuma atjauninājumi iekļauj arī noderīgus platformas atjauninājumus, kad tie tiek izlaisti. Lai iegūtu priekšstatu par to, kad tiek izlaisti platformas atjauninājumi, skatiet [3. tabula: platformas laidieni](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases). Iknedēļas atjauninājumi parasti tiek izlaisti trešdienās. Papildinformāciju par iknedēļas atjauninājumiem skatiet [Jaunumi un izmaiņas Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).

    Visi atbalstītie datu centri tiek atjaunināti katru nedēļu, ja vien nav norādīts citādi. Iknedēļas atjauninājumi parasti sākas trešdien un tiek pabeigti līdz svētdienai. Iknedēļas atjauninājumos ir ietverti ASV, Austrālijas, Eiropas, Apvienotās Karalistes, Āzijas un Kanādas reģioni. 

- **Common Data Service risinājuma atjauninājumi**: šie atjauninājumi pēc nepieciešamības parādās aptuveni ik pēc sešām nedēļām. Tie ietver jaunus elementus un izmaiņas esošajos elementos Common Data Service. Šie atjauninājumi tiek izlaisti tiem pašiem reģioniem kā iknedēļas atjauninājumi, un paiet aptuveni sešas nedēļas līdz tie tiek kopēti visos datu centros. Risinājumu atjauninājumi var būt vai var nebūt saskaņoti ar iknedēļas pakalpojumu atjauninājumiem.

Tālāk redzamajā tabulā ir parādīts grafika paraugs.

| Nedēļa | Labošanas tips |
| --- | --- |
| 1. | Pakalpojuma atjauninājums (visi reģioni) |
| 2. | Pakalpojuma atjauninājums (visi reģioni) + risinājuma atjauninājums (1. nedēļas reģioni) |
| 3 | Pakalpojuma atjauninājums (visi reģioni) + risinājuma atjauninājums (2. nedēļas reģioni) |
| 4. | Pakalpojuma atjauninājums (visi reģioni) + risinājuma atjauninājums (3. nedēļas reģioni) |
| 5 | Pakalpojuma atjauninājums (visi reģioni) + risinājuma atjauninājums (4. nedēļas reģioni) |
| 6 | Pakalpojuma atjauninājums (visi reģioni) + risinājuma atjauninājums (5. nedēļas reģioni) |
| 7 | Pakalpojuma atjauninājums (visi reģioni) + risinājuma atjauninājums (6. nedēļas reģioni) |
| 8 | Pakalpojuma atjauninājums (visi reģioni) |

> [!NOTE]
> Kad tie tiek izlaisti, risinājuma atjauninājumi ir pieejami visiem datu centriem. Ja nevēlaties gaidīt, kamēr atjauninājumi tiek kopēti automātiski, varat lietot šos atjauninājumus manuāli jebkurā vidē jebkurā datu centrā.

Ja nepieciešams, Human Resources nodrošina arī tālāk minētos labojumu veidus.

- **Pārstrādātais izdevums (labojumfails**): kļūdu labojumi, kas var būt vai nu kopā ar iknedēļas pakalpojuma atjaunināšanas laidienu, vai atsevišķi no tā

- **Ārkārtas labojums**: proaktīvi un reaktīvi labojumfaili, kas ir pēc būtības ir paši par sevi, var ietvert tikai konfigurācijas vai koda izmaiņas, lai atrisinātu tiešsaistes vietnes problēmas, un tie var būt atsevišķi no iknedēļas pakalpojuma atjaunināšanas laidiena

Laidieni tiek pārbaudīti, testēti un apstiprināti iekšējā vidē. Pēc izveidotā ir izrakstīšanas, tas tiek izvietots ražošanā.

## <a name="exceptions-in-2019"></a>Izņēmumi 2019. gadā

Tālāk minētie datumi ir izņēmumi no regulāro laidienu grafika.

| Datums | Apraksts |
| --- | --- |
| 25. novembra nedēļa | Nav atjauninājumu |
| 16. decembra nedēļa | Tikai mazsvarīgi atjauninājumi |
| 23. decembra nedēļa | Nav atjauninājumu |
| 30. decembra nedēļa | Nav atjauninājumu |

## <a name="communications"></a>Komunikācija

Tālāk minētajās vietās varat uzzināt, kas ietverts Human Resources darbībā un kādi bijuši laidieni.

- [Dynamics 365 Human Resources rīcības plāns](https://dynamics.microsoft.com/roadmap/talent/)

- [Dynamics 365 laidiena plāni](https://docs.microsoft.com/dynamics365/release-plans/)

- [Jaunumi un izmaiņas Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [Problēmu meklēšana Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (tikai ar platformu saistītām kļūdām)

- [Human Resources emuārs](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Human Resources Yammer kopiena](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Priekšskatījuma līdzekļi smilškastes vidē

Varat validēt priekšskatījuma līdzekļus smilškastes vidē pirms iespējot tos savā ražošanas vidē. Papildinformāciju par jaunu līdzekļu iespējošanu skatiet [Pārskats par līdzekļu pārvaldību](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Visi jaunie līdzekļi paliek priekšskatījumā vismaz 30 dienas, un parasti 30-60 dienas. Galvenās funkcijas parasti ir pieejamas katra gada oktobrī un aprīlī pēc priekšskatījuma perioda. Tiklīdz jūs redzat jaunas iespējas Līdzekļu pārvaldības darbvietā, varat tās ieslēgt. Daži līdzekļi var būt ieslēgti pēc noklusējuma.

Reizēm šis līdzeklis būs ieslēgts pēc noklusējuma, un to nevar izslēgt (piemēram, Līdzekļu pārvaldības darbvieta).

Kolīdz līdzeklis ir vispārīgi pieejams, to var ieslēgt vai izslēgt ražošanas vidēs. Līdzekļu pārvaldības darbvieta norāda, kad priekšskatījuma līdzeklis kļūs obligāts. Šis datums parasti ir 1. oktobris vai 1. aprīlis, lai to saskaņotu ar pusgada laidiena plāniem. Jūs nevarat izslēgt obligātos līdzekļus. Kamēr tas kļūst obligāts, varat ieslēgt vai izslēgt līdzekli visās vidēs.

Mēs noteikti iesakām priekšskatīt līdzekļus smilškastes vai izmēģinājuma vidē. Ir ieteicams izveidot pašreizējās ražošanas vides vai datu bāzes kopiju smilškastes vidē, lai varētu iegūt pilnīgu pieredzi ar jaunajiem līdzekļiem, izmantojot savus datus.

Papildinformāciju par smilškastes vides nodrošināšanu skatiet [Human Resources projekta nodrošināšana](hr-admin-setup-provision.md). Lai noņemtu testa vidi, skatiet [Instances noņemšana](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Pārskata sniegšana par kļūdām

Testējot priekšskatījuma līdzekļus vai izmēģinot jaunas iespējas, iespējams, atradīsiet vienumus, kas nedarbojas kā paredzēts. Lūdzu, sniedziet pārskatu par jebkurām kļūdām, izmantojot [Microsoft Dynamics 365 atbalstu](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Skatiet arī

- [Dynamics 365 un Power Platform laidiena plāni](https://docs.microsoft.com/dynamics365/release-plans)
- [Jaunumi un izmaiņas Dynamics 365 Human Resources](hr-admin-whats-new.md)
- [Programmatūras dzīves cikla politika](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

