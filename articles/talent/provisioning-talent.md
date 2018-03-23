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
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: e4459e8be4bfab8e0789744eacd533286b6c05e0
ms.contentlocale: lv-lv
ms.lasthandoff: 03/08/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talent nodrošināšana

[!include[banner](includes/banner.md)]

Šajā tēmā ir izklāstīta jaunas ražošanas vides nodrošināšana pakalpojumam Microsoft Dynamics 365 for Talent. Šajā tēmā tiek pieņemts, ka pakalpojumu Talent iegādājāties, izmantojot mākoņrisinājumu nodrošinātāja (Cloud Solution Provider — CSP) vai uzņēmuma arhitektūras (Enterprise Architecture — AE) līgumu. Ja jums ir Microsoft Dynamics 365 licence, kur jau ir ietverts Talent pakalpojumu plāns, bet nevarat izpildīt šajā tēmā aprakstītās darbības, sazinieties ar atbalsta dienestu.

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

    Jūsu jaunā vide tiek rādīta navigācijas rūts kreisajā pusē, sarakstā ar vidēm. Taču vidi nevar sākt izmantot, kamēr izvietošanas statuss tiek atjaunināts uz **Izvietots**. Šis process parasti aizņem tikai dažas minūtes. Ja nodrošinājuma process ir nesekmīgs, sazinieties ar atbalsta dienestu.

6. Atlasiet **Pieteikties pakalpojumā Talent**, lai izmantotu jauno vidi.

> [!NOTE]
> Ja vēl neesat izpildījis gala prasības, projektā varat izvietot Talent testa instanci. Pēc tam šo instanci varat lietot sava risinājuma testēšanai līdz brīdim, kad izrakstāties. Ja testēšanai lietojat savu jauno vidi, šī procedūra ir jāatkārto, lai izveidotu ražošanas vidi.

> [!NOTE]
> Talent vides, kas tiek nodrošinātas, izmantojot LCS, nesatur demonstrācijas datus, kas ir konfigurēti personāla vadības (HR) uzdevumiem vai tiek izmantoti tikai pakalpojumā Talent. Ja jums ir nepieciešama vide, kas satur demonstrācijas datus, mēs iesakām pieteikties bezmaksas 60 dienu [Talent izmēģinājuma videi](https://dynamics.microsoft.com/en-us/talent/overview/). Kaut arī izmēģinājuma vide pieder lietotājam, kurš to pieprasīja, citus lietotājus var uzaicināt, izmantojot pamata personāla vadības sistēmas administrēšanu. Izmēģinājuma vides satur fiktīvsu datus, ko var izmantot, lai izpētītu programmu drošā veidā. Šīs vides nav paredzētas izmantošanai kā ražošanas vides. Ņemiet vērā, ka, beidzoties izmēģinājuma vides termiņam pēc 60 dienām, visi tajā esošie dati tiek dzēsti un nevar tikt atgūti. Pēc esošās vides termiņa beigām jūs varat pieteikties jaunai izmēģinājuma videi.

## <a name="create-a-new-powerapps-environment-if-required"></a>Jaunas PowerApps vides izveidošana (ja nepieciešams)
Izmantojot integrāciju starp Talent un PowerApps vidēm, varat integrēt un paplašināt Talent datu lietojumu, izmantojot PowerApps rīkus. Izprotot, kāpēc tiek izmantotas PowerApps vides, varēsiet veidot lietotnes, kas atbildīs jūsu nepieciešamībai pēc Talent paplašinašanas. Papildinformāciju par PowerApps vidēm, tostarp vides tvērumu, piekļuvi videi, kā arī vides izveidi un izvēli skatiet tēmā [Paziņojums par PowerApps vidēm](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). Lai gan katrs nomnieks ir automātiski nodrošināts noklusējuma PowerApps vidē, tā var nebūt labākā vide, ko izmantot Talent izvietojumam. Šīs darbības laikā ir jāapsver datu integrācijas un testēšanas stratēģijas, tādēļ ieteicams apsvērt implikācijas, kas var ietekmēt jūsu izvietojumus, jo vēlāk dažas izmaiņas nevarēs viegli mainīt. 

Lai gan katrs nomnieks ir automātiski nodrošināts noklusējuma PowerApps vidē, tā var nebūt labākā vide, ko izmantot Talent izvietojumam. Šīs darbības laikā ir jāapsver datu integrācijas un testēšanas stratēģijas. Tādēļ ieteicams apsvērt dažādās implikācijas jūsu izvietojumam, jo vēlāk PowerApps vidi nevarēs viegli mainīt.

1. Pakalpojumā LCS atlasiet **Pārvaldīt vides**. Tiek atvērts [PowerApps administrēšanas centrs](https://preview.admin.powerapps.com/environments), kur varat skatīt esošās vides un izveidot jaunas vides.
2. Atlasiet **Jauna vide**.
3. Ievadiet unikālu vides nosaukumu un atlasiet vietu, kur to izvietot.

    > [!NOTE]
    > Pakalpojums Talent nav pieejams visos reģionos. Tādēļ pirms savas vides atrašanās vietas atlasīšanas noteikti pārbaudiet pieejamību.

4. Kad tiek vaicāts, vai vēlaties izveidot datu bāzi, atlasiet **Izveidot datu bāzi**, lai izveidotu Common Data Service (CDS) datu bāzi, kur ir jāvieso daļa no jūsu Talent datiem. Izveidojot datu bāzi, pakalpojumā Talent varat arī integrēt PowerApps programmas.
5. Jums tiek jautāts par datu bāzē izmantojamo piekļuves līmeni. Ieteicams atlasīt **Ierobežot piekļuvi**, jo šī opcija Talent lietotājiem neļauj tieši piekļūt jutīgiem datiem, izmantojot PowerApps programmu.
6. Izveidotajā CD datu bāzē ir demonstrācijas dati, kas jūsu ražošanas videi pievieno neaktīvus darbiniekus, fiktīvas adreses un citu informāciju. Lai noņemtu demonstrācijas datus, pēc CDS datu bāzes izveidošanas izpildiet tālāk norādītās darbības.

    > [!IMPORTANT]
    > Ja iepriekš esat izveidojis CD datu bāzi un ievadījis tajā kādus jūsu uzņēmuma ražošanas datus, ar šīm darbībām tiek noņemti **visi** atlasītajā datu bāzē esošie dati, pat jūsu uzņēmuma ražošanas dati.

    1. Pierakstieties vietnē [PowerApps](https://preview.web.powerapps.com/home).
    2. Nolaižamajā sarakstā augšējā labajā stūrī atlasiet vidi, ko izveidojāt 2. darbībā.
    3. Kreisajā pusē esošajā navigācijas rūtī izvērsiet vienumu **Common Data Service** un pēc tam atlasiet **Elementi**.
    4. Lapas labajā pusē atlasiet daudzpunktes (**...**) pogu un pēc tam atlasiet **Notīrīt visus datus**.
    5. Atlasiet **Dzēst datus**, lai apstiprinātu, ka vēlaties šos datus noņemt. Ar šo darbību tiek noņemti visi demonstrācijas dati, kas CDS ir ietverti pēc noklusējuma. Tiek noņemti arī visi citi dati, kas ir ievadīti atlasītajā datu bāzē.

Tagad varat lietot savu jauno vidi.

## <a name="grant-access-to-the-environment"></a>Piekļuves piešķiršana videi
Pēc noklusējuma videi var piekļūt globālais administrators, kas to izveidoja. Taču citiem programmas lietotājiem piekļuve ir jāpiešķir. Piekļuvi var piesķirt, [pievienojot lietotājus](../dev-itpro/sysadmin/tasks/create-new-users.md) un [piešķirot viņiem atbilstošās lomas](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) pamata personāla vadības vidē. Jums šie lietotāji ir arī jāpievieno PowerApps videi, lai viņi varētu piekļūt Attract un Onboard programmām. Tālak ir norādīta šī procedūra. Ja jums ir nepieciešama palīdzība darbību veikšanai, skatiet emuāra ierakstu [Iepazīstināšana ar PowerApps administrēšanas centru](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/).

Šo procedūru veic globālais administrators, kas izvietoja Talent vidi.

1. Atveriet [PowerApps administrēšanas centru](https://preview.admin.powerapps.com/environments).
2. Atlasiet atbilstošās vides.
3. Cilnē **Drošība** pievienojiet vajadzīgos lietotājus lomai **Vides veidotājs**.

Ņemiet vērā, ka šī pēdējā darbība, kurā jūs manuāli pievienojat lietotājus PowerApps videi, ir īslaicīga. Tā tiks pabeigta automātiski, kad lietotāji tiks pievienoti pamata personāla vadības vidē.

