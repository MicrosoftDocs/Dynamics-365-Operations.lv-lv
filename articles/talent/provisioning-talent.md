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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b4b54e97bdebc158adc3bc6d57a6661cd536f5fb
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talent nodrošināšana

[!INCLUDE [banner](includes/banner.md)]

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
2. Pakalpojums Talent vienmēr tiek nodrošināts Microsoft PowerApps vidē, lai iespējotu PowerApps integrāciju un paplašināmību. Pirms turpināšanas izlasiet šīs tēmas sadaļu “PowerApps vides izvēle”. 
3. Ja jums vēl nav PowerApps vides, pirms turpināšanas izpildiet šīs tēmas sadaļā “Jaunas PowerApps vides izveidošana (ja nepieciešams)” sniegtos norādījumus.

    > [!NOTE]
    > Lai skatītu esošās vides vai izveidotu jaunas vides, tā nomnieka administratoram, kurš nodrošina pakalpojumu Talent, ir jābūt piešķirtai PowerApps P2 licencei. Ja jūsu organizācijai nav PowerApps P2 licences, tādu varat saņemt no sava CSP vai no [PowerApps izcenojuma lapas](https://powerapps.microsoft.com/en-us/pricing/).

4. Atlasiet **Pievienot** un pēc tam atlasiet vidi, kurā nodrošināt pakalpojumu Talent.
5. Atlasiet **Jā**, lai piekristu nosacījumiem un sāktu izvietošanu.

    Jūsu jaunā vide tiek rādīta navigācijas rūts kreisajā pusē, sarakstā ar vidēm. Taču vidi nevar sākt izmantot, kamēr izvietošanas statuss tiek atjaunināts uz **Izvietots**. Šis process parasti aizņem tikai dažas minūtes. Ja nodrošinājuma process ir nesekmīgs, sazinieties ar atbalsta dienestu.

6. Atlasiet **Pieteikties pakalpojumā Talent**, lai izmantotu jauno vidi.

> [!NOTE]
> Ja vēl neesat izpildījis gala prasības, projektā varat izvietot Talent testa instanci. Pēc tam šo instanci varat lietot sava risinājuma testēšanai līdz brīdim, kad izrakstāties. Ja testēšanai lietojat savu jauno vidi, šī procedūra ir jāatkārto, lai izveidotu ražošanas vidi.

> [!NOTE]
> Talent vides, kas tiek nodrošinātas, izmantojot LCS, nesatur demonstrācijas datus, kas ir konfigurēti personāla vadības (HR) uzdevumiem vai tiek izmantoti tikai pakalpojumā Talent. Ja jums ir nepieciešama vide, kas satur demonstrācijas datus, mēs iesakām pieteikties bezmaksas 60 dienu [Talent izmēģinājuma videi](https://dynamics.microsoft.com/en-us/talent/overview/). Kaut arī izmēģinājuma vide pieder lietotājam, kurš to pieprasīja, citus lietotājus var uzaicināt, izmantojot pamata personāla vadības sistēmas administrēšanu. Izmēģinājuma vides satur fiktīvsu datus, ko var izmantot, lai izpētītu programmu drošā veidā. Šīs vides nav paredzētas izmantošanai kā ražošanas vides. Ņemiet vērā, ka, beidzoties izmēģinājuma vides termiņam pēc 60 dienām, visi tajā esošie dati tiek dzēsti un nevar tikt atgūti. Pēc esošās vides termiņa beigām jūs varat pieteikties jaunai izmēģinājuma videi.

## <a name="select-a-powerapps-environment"></a>PowerApps vides izvēle

Izmantojot integrāciju starp Talent un PowerApps vidēm, varat integrēt un paplašināt Talent datu lietojumu, izmantojot PowerApps rīkus. Izpratne par PowerApps vides mērķi ne tikai palīdzēs jums izveidot programmas, lai paplašinātu programmatūru Talent, bet, iespējams, arī palīdzēs izvēlēties vajadzīgo vidi programmatūras Talent nodrošināšanas laikā. Papildinformāciju par PowerApps vidēm, tostarp vides tvērumu, piekļuvi videi, kā arī vides izveidi un izvēli skatiet tēmā [Paziņojums par PowerApps vidēm](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Izvēloties PowerApps vidi, kurā izvietot programmatūru Talent, ņemiet vērā tālāk sniegtos norādījumus. 
1. LCS atlasiet Pārvaldīt vides vai tiešā veidā pārejiet uz PowerApps administrēšanas centru, kur varat skatīt esošās vides un izveidot jaunas vides.
2. Katra Talent vide ir kartēta ar atsevišķu PowerApps vidi.
3. PowerApps vidē ir ietverta Talent lietojumprogramma, kā arī atbilstošās PowerApps, Flow un CDS lietojumprogrammas. Ja tiek dzēsta PowerApps vide, kopā ar to tiek dzēstas arī programmas.
4. Ir jāapsver datu integrācijas un pārbaudes metodes, piemēram, smilškastes, UAT, ražošanas. Tāpēc ir ieteicams apsvērt dažādos izvietojuma saistīšanas iespējas, jo vēlāk nevar viegli mainīt ar PowerApps vidi kartēto Talent vidi.
5. Tālāk norādītās PowerApps vides nevar lietot programmatūrā Talent, tāpēc tās netiek rādītas LCS esošajā atlases sarakstā.
 
    **CDS 2.0 vides** Programmatūra CDS 2.0 kļūs publiski pieejama 2018. gada 21. martā, taču programmatūra Talent pašlaik neatbalsta CDS 2.0. Lai gan PowerApps administrēšanas centrā varat skatīt un izveidot CDS 2.0 datu bāzes, tās nevar izmantot programmatūrā Talent. Iespēja Talent izvietojumos izmantot CDS 2.0 vides būs pieejama vēlāk.
   
   > [!Note]
   > Lai administrēšanas portālā atšķirtu CDS 1.0 un CDS 2.0 vides, atlasiet vidi un skatiet sadaļu **Informācija**. Visām CDS 2.0 vidēm informācijas sadaļā ietverts ir paziņojums “Šos iestatījumus nevar pārvaldīt Dynamics 365 administrēšanas centrā” un norāde uz instances versiju, kā arī nav cilnes Datu bāze. 
 
   **Noklusējuma PowerApps vides** Lai gan katram nomniekam tiek automātiski nodrošināta noklusējuma PowerApps vide, tās nav ieteicams izmantot programmatūrā Talent, jo visi nomnieku lietotāji var piekļūt PowerApps videi un nejauši sabojāt ražošanas datus, izmēģinot vai iepazīstot PowerApps vai Flow integrāciju.
   
   <strong>Izmēģinājuma vides</strong> Ir izveidotas vides ar līdzīgu nosaukumu kā “TestDrive — alias@domain”, kurām ir 60 dienu izmēģinājuma periods, pēc kura beigām beidzas vides derīgums un tā tiek automātiski noņemta.
   
   **Neatbalstītie reģioni** Pašlaik Talent tiek atbalstīts tikai šādos reģionos: ASV, Eiropa vai Austrālija.
  
6. Pēc vajadzīgās vides noteikšanas nav jāveic nekādas konkrētas darbības. Turpiniet nodrošināšanas procesu. 
 
## <a name="create-a-new-powerapps-environment-if-required"></a>Jaunas PowerApps vides izveidošana (ja nepieciešams)

Palaidiet PowerShell skriptu, lai izveidotu jaunu PowerApps vidi programmatūrai Talent tā nomnieka administratora kontekstā, kam ir PowerApps 2. plāna licence. Skripts nodrošina tālāk norādīto darbību automatizāciju.


 + PowerApps vides izveide
 + CDS 1.0 datu bāzes izveide
 + Visu CDS 1.0 datu bāzē esošo parauga datu notīrīšana


Izpildiet tālāk sniegtos norādījumus, lai palaistu skriptu.

1. Lejupielādējiet failu ProvisionCDSEnvironment.zip no šīs vietnes: [ProvisionCDSEnvironment skripti](https://go.microsoft.com/fwlink/?linkid=870436).  

2. Kādā mapē izgūstiet visu saturu no ZIP arhīva faila ProvisionCDSEnviroinment.zip.

3. Palaidiet programmu Windows PowerShell vai Windows PowerShell ISE kā administrators.

   Lai uzzinātu vairāk par izpildes politikas iestatīšanu skriptu palaišanai skatiet tēmā [Izpildes politikas iestatīšana](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6).
  
4. Programmā PowerShell pārejiet uz mapi, kur izguvāt saturu no ZIP arhīva faila, un palaidiet tālāk norādīto komandu, aizstājot vērtības, kā ir norādīts tālāk.
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   **MyNewEnvironment** ir jāaizstāj ar jūsu vides nosaukumu. Šis nosaukums tiek rādīts LCS, un lietotāji to redz, kad izvēlas izmantojamo Talent vidi. 

   **YourLocation** ir jāaizstāj ar vienu no reģioniem, kur tiek atbalstīta programmatūra Talent: unitedsates, europe, australia. 

   **-Verbose** ir izvēles parametrs, kurā tiek norādīta detalizēta informācija, ko nosūtīt atbalsta dienestam problēmu gadījumā.

5. Turpiniet nodrošināšanas procesu.
 


## <a name="grant-access-to-the-environment"></a>Piekļuves piešķiršana videi
Pēc noklusējuma videi var piekļūt globālais administrators, kas to izveidoja. Taču citiem programmas lietotājiem piekļuve ir jāpiešķir. Piekļuvi var piesķirt, [pievienojot lietotājus](../dev-itpro/sysadmin/tasks/create-new-users.md) un [piešķirot viņiem atbilstošās lomas](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) pamata personāla vadības vidē. Jums šie lietotāji ir arī jāpievieno PowerApps videi, lai viņi varētu piekļūt Attract un Onboard programmām. Tālak ir norādīta šī procedūra. Ja jums ir nepieciešama palīdzība darbību veikšanai, skatiet emuāra ierakstu [Iepazīstināšana ar PowerApps administrēšanas centru](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/).

Šo procedūru veic globālais administrators, kas izvietoja Talent vidi.

1. Atveriet [PowerApps administrēšanas centru](https://preview.admin.powerapps.com/environments).
2. Atlasiet atbilstošās vides.
3. Cilnē **Drošība** pievienojiet vajadzīgos lietotājus lomai **Vides veidotājs**.

    Ņemiet vērā, ka šī pēdējā darbība, kurā jūs manuāli pievienojat lietotājus PowerApps videi, ir īslaicīga. Tā tiks pabeigta automātiski, kad lietotāji tiks pievienoti pamata personāla vadības vidē.

