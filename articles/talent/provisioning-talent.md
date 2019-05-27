---
title: Talent nodrošināšana
description: Šajā tēmā ir detalizēti aprakstīta jaunas vides nodrošināšana programmai Microsoft Dynamics 365 for Talent.
author: andreabichsel
manager: AnnBe
ms.date: 00/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: 98f60e466b8b97215fdba0f48ca53ca57157283b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518561"
---
# <a name="provision-talent"></a>Talent nodrošinājums

[!include [banner](includes/banner.md)]

Šajā tēmā ir detalizēti aprakstīta jaunas ražošanas vides nodrošināšana programmai Microsoft Dynamics 365 for Talent. Šajā tēmā tiek pieņemts, ka pakalpojumu Talent iegādājāties, izmantojot mākoņrisinājumu nodrošinātāja (Cloud Solution Provider — CSP) vai uzņēmuma arhitektūras (Enterprise Architecture — AE) līgumu. Ja jums ir Microsoft Dynamics 365 licence, kurā jau ir ietverts Talent pakalpojumu plāns, un nevarat izpildīt šajā tēmā aprakstītās darbības, sazinieties ar atbalsta dienestu.

Lai sāktu, globālajam administratoram ir jāpierakstās pakalpojumā [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) un jāizveido jauns Talent projekts. Nav nepieciešama palīdzība no atbalsta dienesta vai Dynamics Service tehniskajiem (Dynamics Service Engineering — DSE) pārstāvjiem, izņemot gadījumus, kad Talent nodrošināšanu jums neļauj veikt kāda licencēšanas problēma.

## <a name="create-an-lcs-project"></a>LCS projekta izveidošana
Lai lietotu LCS un pārvaldītu savas Talent vides, vispirms ir jāizveido LCS projekts.

1. Pierakstieties pakalpojumā [LCS](https://lcs.dynamics.com/Logon/Index), izmantojot to pašu kontu, ko lietojat Talent abonēšanai.
2. Atlasiet pluszīmi (**+**), lai izveidotu projektu.
3. Kā produkta nosaukumu un produkta versiju atlasiet **Microsoft Dynamics 365 for Talent**.
4. Atlasiet metodoloģiju **Dynamics 365 for Talent**.
5. Atlasiet **Izveidot**.

Informāciju par to, kā sākt darbu ar pakalpojumu Talent, skatiet **Talent** metodoloģijā, ko izveidojāt savā jaunajā projektā. Kad projekta izveidošana ir pabeigta, izpildiet tālāk norādīto procedūru, lai nodrošinātu savu Talent vidi.

## <a name="provision-a-talent-project"></a>Talent projekta nodrošināšana
Kad esat izveidojis LCS projektu, pakalpojumu Talent varat nodrošināt kādā vidē.

1. LCS projektā atlasiet elementu **Talent programmas pārvaldība**.
2. Programma Talent vienmēr tiek nodrošinātaMicrosoft PowerApps vidē, lai nodrošinātu PowerApps integrāciju un paplašināmību. Pirms turpināšanas izlasiet šīs tēmas sadaļu “PowerApps vides izvēle”. Ja jums vēl nav pieejama PowerApps vide, pakalpojumā LCS atlasiet Pārvaldīt vides vai pārejiet uz PowerApps administrēšanas centru. Pēc tam izpildiet norādījumus par procedūru [PowerApps vides izveidošana](https://docs.microsoft.com/en-us/powerapps/administrator/create-environment).

    > [!NOTE]
    > Lai skatītu esošās vides vai izveidotu jaunas vides, tā nomnieka administratoram, kurš nodrošina pakalpojumu Talent, ir jābūt piešķirtai PowerApps P2 licencei. Ja jūsu organizācijai nav PowerApps P2 licences, tādu varat saņemt no sava CSP vai no [PowerApps izcenojuma lapas](https://powerapps.microsoft.com/en-us/pricing/).

4. Atlasiet **Pievienot** un pēc tam atlasiet vidi, kurā nodrošināt pakalpojumu Talent.
5. Atlasiet opciju **Iekļaut demonstrācijas datus**, ja vēlaties konkrētajā vidē iekļaut to pašu demonstrācijas datu kopu, kas izmantota Talent izmēģinājuma vides ietvaros. Tas ir izdevīgi ilgtermiņa demonstrācijas vai apmācības vidē, un to nekādā gadījumā nedrīkst lietot ražošanas vidē.  Ņemiet vērā, ka šī opcija ir jāizvēlas pēc sākotnējās izvietošanas. Esošu izvietošanu vēlāk nevar atjaunināt.
6. Atlasiet **Jā**, lai piekristu nosacījumiem un sāktu izvietošanu.

    Jūsu jaunā vide tiek rādīta navigācijas rūts kreisajā pusē, sarakstā ar vidēm. Taču vidi nevar sākt izmantot, kamēr izvietošanas statuss tiek atjaunināts uz **Izvietots**. Šis process parasti aizņem dažas minūtes. Ja nodrošinājuma process ir nesekmīgs, sazinieties ar atbalsta dienestu.

7. Atlasiet **Pieteikties pakalpojumā Talent**, lai izmantotu jauno vidi.

    > [!NOTE]
    > Ja vēl neesat izpildījis gala prasības, projektā varat izvietot Talent testa instanci. Pēc tam šo instanci varat lietot sava risinājuma testēšanai līdz brīdim, kad izrakstāties. Ja testēšanai lietojat savu jauno vidi, šī procedūra ir jāatkārto, lai izveidotu ražošanas vidi.

    > Tā kā Talent abonementa ietvaros ir atļautas tikai divas LCS vides, var apsvērt iespēju izmantot bezmaksas 60 dienu [Talent izmēģinājuma vidi](https://dynamics.microsoft.com/en-us/talent/overview/). Kaut arī izmēģinājuma vide pieder lietotājam, kurš to pieprasīja, citus lietotājus var uzaicināt, izmantojot pamata personāla vadības sistēmas administrēšanu. Izmēģinājuma vides satur fiktīvsu datus, ko var izmantot, lai izpētītu programmu drošā veidā. Šīs vides nav paredzētas izmantošanai kā ražošanas vides. Ņemiet vērā, ka, beidzoties izmēģinājuma vides termiņam pēc 60 dienām, visi tajā esošie dati tiek dzēsti un nevar tikt atgūti. Pēc esošās vides termiņa beigām jūs varat pieteikties jaunai izmēģinājuma videi.

## <a name="select-a-powerapps-environment"></a>PowerApps vides izvēle

Izmantojot integrāciju starp Talent un PowerApps vidēm, varat integrēt un paplašināt Talent datu lietojumu, izmantojot PowerApps rīkus. Izpratne par PowerApps vides mērķi ne tikai palīdzēs izveidot programmas, lai paplašinātu programmatūru Talent, bet arī palīdzēs izvēlēties vajadzīgo vidi programmatūras Talent nodrošināšanas laikā. Papildinformāciju par PowerApps vidēm, tostarp vides tvērumu, piekļuvi videi, kā arī vides izveidi un izvēli skatiet tēmā [Paziņojums par PowerApps vidēm](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Izvēloties PowerApps vidi, kurā izvietot programmatūru Talent, ņemiet vērā tālāk sniegtos norādījumus. 

1. LCS atlasiet **Pārvaldīt vides** vai dodieties tieši uz PowerApps administrēšanas centru, kur varat skatīt esošās vides un izveidot jaunas vides.
2. Katra Talent vide ir kartēta ar atsevišķu PowerApps vidi.
3. PowerApps vidē ir ietverta Talent lietojumprogramma, kā arī atbilstošās PowerApps, Flow un Common Data Service programmas. Ja tiek dzēsta PowerApps vide, kopā ar to tiek dzēstas arī programmas. Kad veicat Talent vides nodrošināšanu, var nodrošināt vidi “Izmēģinājumversija” vai “Ražošana”. Vides tips ir jāizvēlas atkarībā no veida, kādā šī vide tiks izmantota. 
4. Ir jāapsver datu integrācijas un pārbaudes metodes, piemēram, smilškastes, UAT vai ražošanas. Mēs iesakām apsvērt dažādos izvietojuma saistīšanas iespējas, jo vēlāk nevar viegli mainīt ar PowerApps vidi kartēto Talent vidi.
5. Tālāk norādītās PowerApps vides nevar lietot programmatūrā Talent, tāpēc tās netiek rādītas LCS esošajā atlases sarakstā.
 
    - **Noklusējuma PowerApps vides** — lai gan katram nomniekam tiek automātiski nodrošināta noklusējuma PowerApps vide, tās nav ieteicams izmantot programmatūrā Talent, jo visi nomnieku lietotāji var piekļūt PowerApps videi un nejauši sabojāt ražošanas datus, izmēģinot vai iepazīstot PowerApps vai Flow integrāciju.
   
    - **Izmēģinājuma vides** — šīs vides ir izveidotas beigu datumu, un tās pēc šī laika to derīgums beidzas, tāpēc vide un tajā ietvertās visas Talent instances tiek automātiski noņemtas.
   
    - **Neatbalstītie reģioni** — pašlaik pakalpojums Talent tiek atbalstīts tikai šādos reģionos: ASV, Eiropa, Apvienota Karaliste vai Austrālija.
  
6. Kad ir noteikta izmantošanai pareizā vide, var pāriet pie nodrošinājuma procesa. 
 
## <a name="grant-access-to-the-environment"></a>Piekļuves piešķiršana videi
Pēc noklusējuma videi var piekļūt globālais administrators, kas to izveidoja. Taču citiem programmas lietotājiem piekļuve ir jāpiešķir. Lai piešķirtu piekļuvi, ir jāpievieno lietotāji un jāpiešķir viņiem atbilstošās lomas Core HR vidē. Globālajam administratoram, kas izvietoja Talent, ir jāpalaiž arī programmas Attract un Onboard, lai pabeigtu inicializēšanu un iespējotu piekļuvi citiem nomnieku lietotājiem.  Kamēr tas nav izdarīts, citi lietotāji nevarēs piekļūt programmām Attract un Onboard un tiem tiks rādītas piekļuves pārkāpumu kļūdas. Plašāku informāciju skatiet tēmā [Jaunu lietotāju izveide](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) un [Drošības lomu piešķiršana lietotājiem](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
