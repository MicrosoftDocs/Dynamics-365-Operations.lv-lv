---
title: "Talent nodrošināšana"
description: "Šajā tēmā ir izklāstīta jaunas vides nodrošināšana pakalpojumam Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 09/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: d28ca1f9cf2bef73dc687a85592056cccc767da5
ms.contentlocale: lv-lv
ms.lasthandoff: 10/01/2018

---
# <a name="provision-talent"></a>Talent nodrošināšana

[!include [banner](includes/banner.md)]

Šajā tēmā ir izklāstīta jaunas ražošanas vides nodrošināšana pakalpojumam Microsoft Dynamics 365 for Talent. Šajā tēmā tiek pieņemts, ka pakalpojumu Talent iegādājāties, izmantojot mākoņrisinājumu nodrošinātāja (Cloud Solution Provider — CSP) vai uzņēmuma arhitektūras (Enterprise Architecture — AE) līgumu. Ja jums ir Microsoft Dynamics 365 licence, kur jau ir ietverts Talent pakalpojumu plāns, bet nevarat izpildīt šajā tēmā aprakstītās darbības, sazinieties ar atbalsta dienestu.

Lai sāktu, globālajam administratoram ir jāpierakstās pakalpojumā [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) un jāizveido jauns Talent projekts. Nav nepieciešama palīdzība no atbalsta dienesta vai Dynamics Service tehniskajiem (Dynamics Service Engineering — DSE) pārstāvjiem, izņemot gadījumus, kad Talent nodrošināšanu jums neļauj veikt kāda licencēšanas problēma.

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
 
   **Noklusējuma PowerApps vides** Lai gan katram nomniekam tiek automātiski nodrošināta noklusējuma PowerApps vide, tās nav ieteicams izmantot programmatūrā Talent, jo visi nomnieku lietotāji var piekļūt PowerApps videi un nejauši sabojāt ražošanas datus, izmēģinot vai iepazīstot PowerApps vai Flow integrāciju.
   
   <strong>Izmēģinājuma vides</strong> Ir izveidotas vides ar līdzīgu nosaukumu kā “TestDrive — alias@domain”, kurām ir 60 dienu izmēģinājuma periods, pēc kura beigām beidzas vides derīgums un tā tiek automātiski noņemta.
   
   **Neatbalstītie reģioni** Pašlaik Talent tiek atbalstīts tikai šādos reģionos: ASV, Eiropa vai Austrālija.
  
6. Pēc vajadzīgās vides noteikšanas nav jāveic nekādas konkrētas darbības. Turpiniet nodrošināšanas procesu. 
 
## <a name="grant-access-to-the-environment"></a>Piekļuves piešķiršana videi
Pēc noklusējuma videi var piekļūt globālais administrators, kas to izveidoja. Taču citiem programmas lietotājiem piekļuve ir jāpiešķir. Piekļuvi var piesķirt, [pievienojot lietotājus](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) un [piešķirot viņiem atbilstošās lomas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles) pamata personāla vadības vidē. Globālajam administratoram, kas izvietoja Talent, ir jāpalaiž arī programmas Attract un Onboard, lai pabeigtu inicializēšanu un iespējotu piekļuvi citiem nomnieku lietotājiem.  Kamēr tas nav izdarīts, citi lietotāji nevarēs piekļūt programmām Attract un Onboard un tiem tiks rādītas piekļuves pārkāpumu kļūdas.


