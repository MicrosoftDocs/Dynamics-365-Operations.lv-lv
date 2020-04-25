---
title: Human Resources nodrošināšana
description: Šajā rakstā ir detalizēti aprakstīta jaunas ražošanas vides nodrošināšana Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/18/2020
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
ms.openlocfilehash: 4f2fd2b7bf9f09a61d07e1bc35ad48fe2c5d7383
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138363"
---
# <a name="provision-human-resources"></a>Human Resources nodrošināšana

Šajā rakstā ir detalizēti aprakstīta jaunas ražošanas vides nodrošināšana Microsoft Dynamics 365 Human Resources. Šajā rakstā tiek pieņemts, ka esat iegādājies Human Resources, noslēdzot mākoņpakalpojumu nodrošinātāja (Cloud Solution Provider — CSP) vai uzņēmuma arhitektūras (enterprise architecture — EA) līgumu. Ja jums ir Microsoft Dynamics 365 licence, kurā jau ir ietverts Human Resources pakalpojumu plāns, un nevarat izpildīt šajā rakstā aprakstītās darbības, sazinieties ar atbalsta dienestu.

Lai sāktu, globālajam administratoram ir jāpierakstās [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) un jāizveido jauns Human Resources projekts. Ja vien Human Resource nodrošināšanu neļauj veikt kāda licencēšanas problēma, nav nepieciešama palīdzība no atbalsta dienesta vai Dynamics Service tehniskajiem darbiniekiem (Dynamics Service Engineering — DSE).

## <a name="create-an-lcs-project"></a>LCS projekta izveidošana

Lai lietotu LCS un pārvaldītu savas Human Resources vides, vispirms ir jāizveido LCS projekts.

1. Pierakstieties pakalpojumā [LCS](https://lcs.dynamics.com/Logon/Index), izmantojot to pašu kontu, ko lietojat Human Resources abonēšanai.

2. Atlasiet pluszīmi (**+**), lai izveidotu projektu.

3. Kā produkta nosaukumu un produkta versiju atlasiet **Microsoft Dynamics 365 Human Resources**.

4. Atlasiet metodoloģiju **Dynamics 365 Human Resources**.

5. Atlasiet **Izveidot**.

Informāciju par to, kā sākt darbu ar Human Resources, skatiet **Human Resources** metodoloģijā, ko izveidojāt savā jaunajā projektā. Kad projekta izveidošana ir pabeigta, izpildiet tālāk minēto procedūru, lai nodrošinātu savu Human Resources vidi.

## <a name="provision-a-human-resources-project"></a>Human Resources projekta nodrošināšana

Kad esat izveidojis LCS projektu, varat nodrošināt Human Resources kādā vidē.

1. Savā LCS projektā atlasiet elementu **Human Resources programmas pārvaldība**.

2. Norāda, vai šī ir Human Resources ražošanas vai smilškastes instance. Smilškastes instancēs varētu būt pieejami agrīni priekšskatījuma līdzekļi, lai varētu agri veikt testēšanu un saņemt atsauksmes.
   
    > [!NOTE]
    > Human Resources instances tipu nevar mainīt pēc iestatīšanas. Pirms turpināt, pārbaudiet, vai ir atlasīts pareizais instances tips.</br></br>
    > Human Resources instances veids ir neatkarīgs no Microsoft Power Apps vides instances veida, kuru iestatāt Power Apps administrēšanas centrā.
    
3. Atlasiet opciju **Iekļaut demonstrācijas datus**, ja vēlaties konkrētajā vidē iekļaut to pašu demonstrācijas datu kopu, kas izmantota Human Resources izmēģinājuma vides ietvaros. Tas ir izdevīgi ilgtermiņa demonstrācijas vai apmācības vidē, un to nekādā gadījumā nedrīkst lietot ražošanas vidē.  Ņemiet vērā, ka šī opcija ir jāizvēlas pēc sākotnējās izvietošanas. Esošu izvietošanu vēlāk nevar atjaunināt.

4. Human Resources vienmēr tiek nodrošināta Microsoft Power Apps vidē, lai iespējotu Power Apps integrāciju un paplašināmību. Pirms turpināšanas izlasiet šī raksta sadaļu “Power Apps vides izvēle”. Ja jums vēl nav pieejama Power Apps vide, pakalpojumā LCS atlasiet Pārvaldīt vides vai pārejiet uz Power Apps administrēšanas centru. Pēc tam izpildiet norādījumus par procedūru [Izveidot Power Apps vidi](https://docs.microsoft.com/powerapps/administrator/create-environment).

5. Atlasiet vidi, kurā nodrošināt Human Resources.

6. Atlasiet **Jā**, lai piekristu nosacījumiem un sāktu izvietošanu.

   Jūsu jaunā vide tiek rādīta navigācijas rūts kreisajā pusē, sarakstā ar vidēm. Taču vidi nevar sākt izmantot, kamēr izvietošanas statuss tiek atjaunināts uz **Izvietots**. Šis process parasti aizņem dažas minūtes. Ja nodrošinājuma process ir nesekmīgs, sazinieties ar atbalsta dienestu.

7. Lai izmantotu jauno vidi, atlasiet **Pieteikties Human Resources**.

    > [!NOTE]
    > Ja vēl neesat izrakstījies no gala prasībām, projektā varat izvietot Human Resources testa instanci. Pēc tam šo instanci varat lietot sava risinājuma testēšanai līdz brīdim, kad izrakstāties. Ja testēšanai lietojat savu jauno vidi, šī procedūra ir jāatkārto, lai izveidotu ražošanas vidi.

    > Jūs varētu apsvērt iespēju izmantot bezmaksas 60 dienu [Human Resources izmēģinājuma vidi](https://dynamics.microsoft.com/talent/overview/). Kaut arī izmēģinājuma vide pieder lietotājam, kurš to pieprasīja, citus lietotājus var uzaicināt, izmantojot Human Resources sistēmas administrēšanu. Izmēģinājuma vides satur fiktīvsu datus, ko var izmantot, lai izpētītu programmu drošā veidā. Šīs vides nav paredzētas izmantošanai kā ražošanas vides. Ņemiet vērā, ka, beidzoties izmēģinājuma vides termiņam pēc 60 dienām, visi tajā esošie dati tiek dzēsti un nevar tikt atgūti. Pēc esošās vides termiņa beigām jūs varat pieteikties jaunai izmēģinājuma videi.

## <a name="select-a-power-apps-environment"></a>Atlasiet Power Apps vidi

Izmantojot integrāciju starp Human Resources un Power Apps vidēm, varat integrēt un paplašināt Human Resources datu lietojumu, izmantojot Power Apps rīkus. Izpratne par Power Apps vides mērķi ne tikai palīdzēs izveidot programmas, lai paplašinātu Human Resources, bet arī palīdzēs izvēlēties vajadzīgo vidi Human Resources nodrošināšanas laikā. Papildinformāciju par Power Apps vidēm, tostarp vides tvērumu, piekļuvi videi, kā arī vides izveidi un izvēli skatiet tēmā [Paziņojums par Power Apps vidēm](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Izvēloties Power Apps vidi, kurā izvietot Human Resources, ņemiet vērā tālāk sniegtos norādījumus. 

1. LCS atlasiet **Pārvaldīt vides** vai dodieties tieši uz Power Apps administrēšanas centru, kur varat skatīt esošās vides un izveidot jaunas vides.

2. Katra Human Resources vide ir kartēta atsevišķā Power Apps vidē.

3. Power Apps vide satur Human Resources, kā arī atbilstošās Power Apps, Power Automate un Common Data Service programmas. Ja tiek dzēsta Power Apps vide, kopā ar to tiek dzēstas arī programmas. Kad nodrošināt Human Resources vidi, varat nodrošināt vai nu vidi **Izmēģinājumversija**, vai **Ražošana**. Vides tips ir jāizvēlas atkarībā no veida, kādā šī vide tiks izmantota. 

4. Ir jāapsver datu integrācijas un pārbaudes metodes, piemēram, smilškastes, UAT vai ražošanas. Mēs iesakām apsvērt dažādas izvietojuma saistīšanas iespējas, jo vēlāk nevar viegli mainīt to, kura Human Resources vide ir kartēta uz Power Apps vidi.

5. Tālāk minētās Power Apps vides nevar lietot Human Resources, tāpēc tās netiek rādītas LCS esošajā atlases sarakstā.
 
    - **Noklusējuma Power Apps vides**— lai gan katram nomniekam tiek automātiski nodrošināta noklusējuma Power Apps vide, tās nav ieteicams izmantot programmatūrā Human Resources, jo visi nomnieka lietotāji var piekļūt Power Apps videi un nejauši sabojāt ražošanas datus, izmēģinot vai iepazīstot Power Apps vai Power Automate integrāciju.
   
    - **Izmēģinājuma vides** — šīs vides ir izveidotas ar beigu datumu, un beigsies pēc tā, kā rezultātā jūsu vide un tajā ietvertās jebkuras Human Resources instances tiks automātiski noņemtas.
   
    - **Neatbalstītie reģioni** – pašlaik Human Resources tiek atbalstīts tikai šādos reģionos: ASV, Eiropa, Apvienotā Karaliste, Austrālija, Kanāda un Āzija.

    > [!NOTE]
    > Human Resources vide ir nodrošināta tajā pašā reģionā, kurā ir nodrošināta Power Apps vide. Human Resources vides migrācija uz citu reģionu netiek atbalstīta.

6. Kad ir noteikta izmantošanai pareizā vide, var pāriet pie nodrošinājuma procesa. 
 
## <a name="grant-access-to-the-environment"></a>Piekļuves piešķiršana videi

Pēc noklusējuma videi var piekļūt globālais administrators, kas to izveidoja. Taču citiem programmas lietotājiem piekļuve ir jāpiešķir. Lai piešķirtu piekļuvi, ir jāpievieno lietotāji un jāpiešķir viņiem atbilstošās lomas Human Resources vidē. Globālajam administratoram, kas izvietoja Human Resources, ir jāpalaiž gan Attract, gan Onboard, lai pabeigtu inicializēšanu un iespējotu piekļuvi citiem nomnieka lietotājiem.  Kamēr tas nav izdarīts, citi lietotāji nevarēs piekļūt Attract un Onboard un tiem tiks rādītas piekļuves pārkāpumu kļūdas. Plašāku informāciju skatiet tēmā [Jaunu lietotāju izveide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) un [Drošības lomu piešķiršana lietotājiem](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
