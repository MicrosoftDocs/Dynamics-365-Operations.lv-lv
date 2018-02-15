---
title: "Microsoft Dynamics 365 for Talent nodrošināšana"
description: "Šajā tēmā ir izklāstīta jaunas vides nodrošināšana pakalpojumam Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a53c1997f74ebe572b17cc3090d2e236b6fe78f6
ms.openlocfilehash: 8a84cfe9b73f0c72f3cb0c3843749754c6b3d538
ms.contentlocale: lv-lv
ms.lasthandoff: 01/31/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talent nodrošināšana
Šajā tēmā ir izklāstīta jaunas vides nodrošināšana pakalpojumam Microsoft Dynamics 365 for Talent. Šajā tēmā tiek pieņemts, ka pakalpojumu Talent iegādājāties, izmantojot mākoņrisinājumu nodrošinātāja (Cloud Solution Provider — CSP) vai uzņēmuma arhitektūras (Enterprise Architecture — AE) līgumu. Ja jums ir Microsoft Dynamics 365 licence, kur jau ir ietverts Talent pakalpojumu plāns, bet nevarat izpildīt šajā tēmā aprakstītās darbības, sazinieties ar atbalsta dienestu.

Lai sāktu, globālajam administratoram ir jāpierakstās pakalpojumā [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) un jāizveido jauns Talent projekts. Nav nepieciešama palīdzība no atbalsta dienesta vai Dynamics Service tehniskajiem (Dynamics Service Engineering — DSE) pārstāvjiem, izņemot gadījumus, kad Talent nodrošināšanu jums neļauj veikt kāda licencēšanas problēma.

## <a name="create-an-lcs-project"></a>LCS projekta izveidošana
Lai lietotu LCS un pārvaldītu savas Talent vides, vispirms ir jāizveido LCS projekts.

1. Pierakstieties pakalpojumā [LCS](https://lcs.dynamics.com/Logon/Index), izmantojot to pašu kontu, ko lietojat Talent abonēšanai.
2. Atlasiet pluszīmi (**+**), lai izveidotu projektu.
3. Kā produkta nosaukumu un produkta versiju atlasiet **Microsoft Dynamics 365 for Talent**.
4. Atlasiet **Dynamics 365 for Talent** metodoloģiju.
5. Atlasiet **Izveidot**.

Informāciju par to, kā sākt darbu ar pakalpojumu Talent, skatiet **Talent** metodoloģijā, ko izveidojāt savā jaunajā projektā. Kad projekta izveidošana ir pabeigta, izpildiet tālāk norādīto procedūru, lai nodrošinātu savu Talent vidi.

## <a name="provision-a-talent-project"></a>Talent projekta nodrošināšana
Kad esat izveidojis LCS projektu, pakalpojumu Talent varat nodrošināt kādā vidē.

1. LCS projektā atlasiet elementu **Talent programmas pārvaldība**.
2. Pakalpojums Talent vienmēr tiek nodrošināts Microsoft PowerApps vidē, lai iespējotu PowerApps integrāciju un paplašināmību. Ja jums vēl nav PowerApps vides, pirms turpināšanas izpildiet šīs tēmas sadaļā “Jaunas PowerApps vides izveidošana (ja nepieciešams)” sniegtos norādījumus.

    > [!NOTE]
    > Lai skatītu esošās vides vai izveidotu jaunas vides, tā nomnieka administratoram, kurš nodrošina pakalpojumu Talent, ir jābūt piešķirtai PowerApps P2 licencei. Ja jūsu organizācijai nav PowerApps P2 licences, tādu varat saņemt no sava CSP vai no [PowerApps izcenojuma lapas](https://powerapps.microsoft.com/en-us/pricing/).

3. Atlasiet **Pievienot** un pēc tam atlasiet vidi, kurā nodrošināt pakalpojumu Talent.
4. Atlasiet **Jā**, lai piekristu nosacījumiem un sāktu izvietošanu.

    Jūsu jaunā vide tiek rādīta navigācijas rūts kreisajā pusē, sarakstā ar vidēm. Taču vidi nevar sākt izmantot, kamēr izvietošanas statuss tiek atjaunināts uz **Izvietots**. Šis process parasti aizņem tikai dažas minūtes. Ja nodrošināšana ir nesekmīga, ir jāsazinās ar atbalsta dienestu.

6. Atlasiet **Pieteikties pakalpojumā Talent**, lai izmantotu jauno vidi.

> [!NOTE]
> Ja vēl neesat izpildījis gala prasības, projektā varat izvietot Talent testa instanci. Pēc tam šo instanci varat lietot sava risinājuma testēšanai līdz brīdim, kad izrakstāties. Ja testēšanai lietojat savu jauno vidi, šī procedūra ir jāatkārto, lai izveidotu ražošanas vidi.

## <a name="create-a-new-powerapps-environment-if-required"></a>Jaunas PowerApps vides izveidošana (ja nepieciešams)

Talent integrācija ar PowerApps vidēm izstrādāta, lai nodrošinātu datu integrācijas un paplašinājumu plūsmas, papildus Talent datiem izmantojot PowerApps rīkus. Tādēļ, izvēloties produktam Talent izmantojamo vidi, ir svarīgi izprast PowerApps vides mērķi. Papildinformāciju par PowerApps vidēm, tostarp vides tvērumu, piekļuvi videi, kā arī vides izveidi un izvēli skatiet tēmā [Paziņojums par PowerApps vidēm](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/).  Lai gan katrs nomnieks ir automātiski nodrošināts noklusējuma PowerApps vidē, tā var nebūt labākā vide, ko izmantot Talent izvietojumam. Šīs darbības laikā ir jāapsver datu integrācijas un testēšanas stratēģijas, tādēļ ieteicams apsvērt dažādās implikācijas jūsu videi, jo vēlāk to nevarēs viegli mainīt.

1. Pakalpojumā LCS atlasiet **Pārvaldīt vides**. Tiek atvērts [PowerApps administrēšanas centrs](https://preview.admin.powerapps.com/environments), kur varat skatīt esošās vides un izveidot jaunas vides.
2. Atlasiet pogu (**+**) **Jauna vide**.
3. Ievadiet unikālu vides nosaukumu un atlasiet vietu, kur to izvietot.

    > [!NOTE]
    > Pakalpojums Talent nav pieejams visos reģionos. Tādēļ pirms savas vides atrašanās vietas atlasīšanas noteikti pārbaudiet pieejamību.

4. Kad tiek vaicāts, vai vēlaties izveidot datu bāzi, atlasiet **Izveidot datu bāzi**, lai izveidotu Common Data Service (CDS) datu bāzi, kur ir jāvieso daļa no jūsu Talent datiem. Izveidojot datu bāzi, pakalpojumā Talent varat arī integrēt PowerApps programmas.
5. Jums tiek jautāts par piekļuves līmeni, ko vēlaties izmantot datu bāzei. Ieteicams atlasīt **Ierobežot piekļuvi**, jo šī opcija Talent lietotājiem neļauj tieši piekļūt jutīgiem datiem, izmantojot PowerApps programmu.
6. Izveidotajā CD datu bāzē ir demonstrācijas dati. Šie demonstrācijas dati ir noderīgi, jo demonstrācijas datu uzņēmumu varat izmantot testēšanai vai uzdevumu ierakstu vai uzdevumu ceļvežu izveidošanai. Taču demonstrācijas dati jūsu ražošanas videi pievieno neaktīvus darbiniekus, fiktīvas adreses un citu informāciju. Lai noņemtu demonstrācijas datus, pēc CDS datu bāzes izveidošanas izpildiet tālāk norādītās darbības.

    > [!IMPORTANT]
    > Ja iepriekš esat izveidojis CD datu bāzi un ievadījis tajā kādus jūsu uzņēmuma ražošanas datus, ņemiet vērā, ka ar šīm darbībām tiek noņemti **visi** atlasītajā datu bāzē esošie dati, pat jūsu uzņēmuma ražošanas dati.

    1. Pierakstieties pakalpojumā [PowerApps](https://preview.web.powerapps.com/home) un lapas labajā pusē esošajā nolaižamajā sarakstā atlasiet 2. darbībā izveidoto vidi.
    2. Kreisajā navigācijas rūtī izvērsiet vienumu **Common Data Service** un izvēlieties vienumu **Elementi**.
    3. Lapas labajā pusē atlasiet daudzpunktes (**...**) pogu un pēc tam atlasiet **Notīrīt visus datus**.
    4. Atlasiet **Dzēst datus**, lai apstiprinātu, ka vēlaties šos datus noņemt. Ar šo darbību tiek noņemti visi demonstrācijas dati, kas CDS ir ietverti pēc noklusējuma. Tiek noņemti arī visi citi dati, kas ir ievadīti atlasītajā datu bāzē.
    
Tagad varat lietot savu jauno vidi.

## <a name="granting-access-to-the-environment"></a>Piekļuves piešķiršana videi
Globālajam administratoram, kurš izveidoja vidi, piekļuve būs pēc noklusējuma, taču citiem programmas lietotājiem piekļuve ir jāpiešķir. To var izdarīt, [pievienojot lietotājus](../dev-itpro/sysadmin/tasks/create-new-users.md) un [piešķirot viņiem atbilstošās lomas](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) pamata personāla vadības vidē. Papildus tam šie lietotāji ir arī jāpievieno PowerApps videi, lai viņi varētu piekļūt Attract un Onboard programmām.  Emuāra ieraksts [Iepazīstināšana ar PowerApps administrēšanas centru](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/) var jums palīdzēt veikt tālāk aprakstītās darbības.

> 1.    Globālajam administratoram, kas izvietoja Talent vidi, ir jāpāriet uz [PowerApps administrēšanas centru](https://preview.admin.powerapps.com/environments).   
> 2.    Atlasiet attiecīgo(-ās) vidi(-es).
> 3.    Cilnē Drošība pievienojiet vajadzīgos lietotājus lomai Vides veidotājs.

Ņemiet vērā, ka šī pēdējā darbība, kurā lietotāji tiek pievienoti PowerApps videi, ir īslaicīga. Mēs vēlāk pievienosim funkcionalitāti, kas to izpildīs automātiski, kad lietotājs tiks pievienots pamata personāla vadības vidē.


