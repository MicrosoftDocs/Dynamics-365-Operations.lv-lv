---
title: "Talent nodrošināšana"
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
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: 2fc4119f3b33aa583274f4d823e296752cdde41d
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="provision-talent"></a>Talent nodrošināšana

[!include [banner](includes/banner.md)]

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
5. Atlasiet opciju “Iekļaut demonstrācijas datus”, ja vēlaties jūsu vidē iekļaut to pašu demonstrācijas datu kopu, kas izmantota Talent izmēģinājuma vides ietvaros.  Tas ir izdevīgi ilgtermiņa demonstrācijas vai apmācības vidē, un to nekādā gadījumā nedrīkst lietot ražošanas vidē.  Ņemiet vērā, ka šī opcija ir jāizvēlas pēc sākotnējās izvietošanas un ka esošo izvietojumu nevar atjaunināt vēlāk.
6. Atlasiet **Jā**, lai piekristu nosacījumiem un sāktu izvietošanu.

    Jūsu jaunā vide tiek rādīta navigācijas rūts kreisajā pusē, sarakstā ar vidēm. Taču vidi nevar sākt izmantot, kamēr izvietošanas statuss tiek atjaunināts uz **Izvietots**. Šis process parasti aizņem tikai dažas minūtes. Ja nodrošinājuma process ir nesekmīgs, sazinieties ar atbalsta dienestu.

7. Atlasiet **Pieteikties pakalpojumā Talent**, lai izmantotu jauno vidi.

> [!NOTE]
> Ja vēl neesat izpildījis gala prasības, projektā varat izvietot Talent testa instanci. Pēc tam šo instanci varat lietot sava risinājuma testēšanai līdz brīdim, kad izrakstāties. Ja testēšanai lietojat savu jauno vidi, šī procedūra ir jāatkārto, lai izveidotu ražošanas vidi.

> [!NOTE]
> Tā kā Talent abonementa ietvaros ir atļautas tikai divas LCS vides, varat apsvērt iespēju izmantot bezmaksas 60 dienu [Talent izmēģinājuma vidi](https://dynamics.microsoft.com/en-us/talent/overview/). Kaut arī izmēģinājuma vide pieder lietotājam, kurš to pieprasīja, citus lietotājus var uzaicināt, izmantojot pamata personāla vadības sistēmas administrēšanu. Izmēģinājuma vides satur fiktīvsu datus, ko var izmantot, lai izpētītu programmu drošā veidā. Šīs vides nav paredzētas izmantošanai kā ražošanas vides. Ņemiet vērā, ka, beidzoties izmēģinājuma vides termiņam pēc 60 dienām, visi tajā esošie dati tiek dzēsti un nevar tikt atgūti. Pēc esošās vides termiņa beigām jūs varat pieteikties jaunai izmēģinājuma videi.

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

2. Lejupielādes mapē ar peles labo pogu noklikšķiniet uz tikko lejupielādētā faila ProvisionCDSEnvironment.zip un atlasiet **Rekvizīti**.  Ja dialoglodziņa apakšdaļā ir drošības piezīme, kurā norādīts “Šis fails ir no cita datora un var tikt bloķēts, lai palīdzētu aizsargāt šo datoru", atzīmējiet izvēles rūtiņu **Atbloķēt** un pēc tam noklikšķiniet uz **Lietot** un pēc tam uz **Labi**.

3. Kādā mapē, kas nav saknes mape, izgūstiet visu saturu no ZIP arhīva faila ProvisionCDSEnviroinment.zip.

4. Palaidiet programmu Windows PowerShell vai Windows PowerShell ISE kā administrators.

   Lai uzzinātu vairāk par izpildes politikas iestatīšanu skriptu palaišanai skatiet tēmā [Izpildes politikas iestatīšana](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6). Ieteicams izmantot “Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope Process”, taču ievērojiet uzņēmuma drošības politiku un aizveriet PowerShell logu, kad process ir pabeigts. 
  
5. Programmā PowerShell pārejiet uz mapi, kur izguvāt saturu no ZIP arhīva faila, un palaidiet tālāk norādīto komandu, aizstājot vērtības, kā ir norādīts tālāk.
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   **MyNewEnvironment** ir jāaizstāj ar jūsu vides nosaukumu. Šis nosaukums tiek rādīts LCS, un lietotāji to redz, kad izvēlas izmantojamo Talent vidi. 

   **YourLocation** ir jāaizstāj ar vienu no reģioniem, kur tiek atbalstīta programmatūra Talent: unitedstates, europe, australia. 

   **-Verbose** ir izvēles parametrs, kurā tiek norādīta detalizēta informācija, ko nosūtīt atbalsta dienestam problēmu gadījumā.

6. Turpiniet nodrošināšanas procesu.
 

## <a name="grant-access-to-the-environment"></a>Piekļuves piešķiršana videi
Pēc noklusējuma videi var piekļūt globālais administrators, kas to izveidoja. Taču citiem programmas lietotājiem piekļuve ir jāpiešķir. Piekļuvi var piesķirt, [pievienojot lietotājus](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) un [piešķirot viņiem atbilstošās lomas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles) pamata personāla vadības vidē. Globālajam administratoram, kas izvietoja Talent, ir jāpalaiž arī programmas Attract un Onboard, lai pabeigtu inicializēšanu un iespējotu piekļuvi citiem nomnieku lietotājiem.  Kamēr tas nav izdarīts, citi lietotāji nevarēs piekļūt programmām Attract un Onboard un tiem tiks rādītas piekļuves pārkāpumu kļūdas.


