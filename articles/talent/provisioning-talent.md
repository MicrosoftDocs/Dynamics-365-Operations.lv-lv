---
title: Talent nodrošināšana
description: Šajā tēmā ir detalizēti aprakstīta jaunas vides nodrošināšana programmai Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 05/15/2019
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
ms.openlocfilehash: ba0d11efe868d57c74f6ae4b069d1cb8351f7213
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773061"
---
# <a name="provision-talent"></a>Talent nodrošinājums

[!include [banner](includes/banner.md)]

Šajā tēmā ir detalizēti aprakstīta jaunas ražošanas vides nodrošināšana programmai Microsoft Dynamics 365 Talent. Šajā tēmā tiek pieņemts, ka pakalpojumu Talent iegādājāties, izmantojot mākoņrisinājumu nodrošinātāja (Cloud Solution Provider — CSP) vai uzņēmuma arhitektūras (Enterprise Architecture — AE) līgumu. Ja jums ir Microsoft Dynamics 365 licence, kurā jau ir ietverts Talent pakalpojumu plāns, un nevarat izpildīt šajā tēmā aprakstītās darbības, sazinieties ar atbalsta dienestu.

Lai sāktu, globālajam administratoram ir jāpierakstās pakalpojumā [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) un jāizveido jauns Talent projekts. Nav nepieciešama palīdzība no atbalsta dienesta vai Dynamics Service tehniskajiem (Dynamics Service Engineering — DSE) pārstāvjiem, izņemot gadījumus, kad Talent nodrošināšanu jums neļauj veikt kāda licencēšanas problēma.

## <a name="create-an-lcs-project"></a>LCS projekta izveidošana
Lai lietotu LCS un pārvaldītu savas Talent vides, vispirms ir jāizveido LCS projekts.

1. Pierakstieties pakalpojumā [LCS](https://lcs.dynamics.com/Logon/Index), izmantojot to pašu kontu, ko lietojat Talent abonēšanai.
2. Atlasiet pluszīmi (**+**), lai izveidotu projektu.
3. Kā produkta nosaukumu un produkta versiju atlasiet **Microsoft Dynamics 365 Talent**.
4. Atlasiet metodoloģiju **Dynamics 365 Talent**.
5. Atlasiet **Izveidot**.

Informāciju par to, kā sākt darbu ar pakalpojumu Talent, skatiet **Talent** metodoloģijā, ko izveidojāt savā jaunajā projektā. Kad projekta izveidošana ir pabeigta, izpildiet tālāk norādīto procedūru, lai nodrošinātu savu Talent vidi.

## <a name="provision-a-talent-project"></a>Talent projekta nodrošināšana
Kad esat izveidojis LCS projektu, pakalpojumu Talent varat nodrošināt kādā vidē.

1. LCS projektā atlasiet elementu **Talent programmas pārvaldība**.
2. Norādiet, vai šī ir Talent smilškastes vai ražošanas instance. Smilškastes instancēs varētu būt pieejami agrīni priekšskatījuma līdzekļi, lai varētu agri veikt testēšanu un saņemt atsauksmes. 
    > [!NOTE]
    > Talent instances tips ir neatkarīgs no Microsoft Power Apps vides instances tipa, kuru jūs iestatāt Power Apps administrēšanas centrā.
3. Atlasiet opciju **Iekļaut demonstrācijas datus**, ja vēlaties konkrētajā vidē iekļaut to pašu demonstrācijas datu kopu, kas izmantota Talent izmēģinājuma vides ietvaros. Tas ir izdevīgi ilgtermiņa demonstrācijas vai apmācības vidē, un to nekādā gadījumā nedrīkst lietot ražošanas vidē.  Ņemiet vērā, ka šī opcija ir jāizvēlas pēc sākotnējās izvietošanas. Esošu izvietošanu vēlāk nevar atjaunināt.
4. Programma Talent vienmēr tiek nodrošināta Microsoft Power Apps vidē, lai nodrošinātu Power Apps integrāciju un paplašināmību. Pirms turpināšanas izlasiet šīs tēmas sadaļu “ Power Apps vides izvēle”. Ja jums vēl nav pieejama Power Apps vide, pakalpojumā LCS atlasiet Pārvaldīt vides vai pārejiet uz Power Apps administrēšanas centru. Pēc tam izpildiet norādījumus par procedūru [Izveidot Power Apps vidi](https://docs.microsoft.com/powerapps/administrator/create-environment).

    > [!NOTE]
    > Lai skatītu esošās vides vai izveidotu jaunas vides, tā nomnieka administratoram, kurš nodrošina pakalpojumu Talent, ir jābūt piešķirtai Power Apps P2 licencei. Ja jūsu organizācijai nav Power Apps P2 licences, tādu varat saņemt no sava CSP vai no [Power Apps izcenojuma lapas](https://powerapps.microsoft.com/pricing/).

5. Atlasiet vidi, kurā nodrošināt programmu Talent.
6. Atlasiet **Jā**, lai piekristu nosacījumiem un sāktu izvietošanu.

    Jūsu jaunā vide tiek rādīta navigācijas rūts kreisajā pusē, sarakstā ar vidēm. Taču vidi nevar sākt izmantot, kamēr izvietošanas statuss tiek atjaunināts uz **Izvietots**. Šis process parasti aizņem dažas minūtes. Ja nodrošinājuma process ir nesekmīgs, sazinieties ar atbalsta dienestu.

7. Atlasiet **Pieteikties pakalpojumā Talent**, lai izmantotu jauno vidi.

    > [!NOTE]
    > Ja vēl neesat izpildījis gala prasības, projektā varat izvietot Talent testa instanci. Pēc tam šo instanci varat lietot sava risinājuma testēšanai līdz brīdim, kad izrakstāties. Ja testēšanai lietojat savu jauno vidi, šī procedūra ir jāatkārto, lai izveidotu ražošanas vidi.

    > Tā kā Talent abonementa ietvaros ir atļautas tikai divas LCS vides, var apsvērt iespēju izmantot bezmaksas 60 dienu [Talent izmēģinājuma vidi](https://dynamics.microsoft.com/talent/overview/). Kaut arī izmēģinājuma vide pieder lietotājam, kurš to pieprasīja, citus lietotājus var uzaicināt, izmantojot pamata personāla vadības sistēmas administrēšanu. Izmēģinājuma vides satur fiktīvsu datus, ko var izmantot, lai izpētītu programmu drošā veidā. Šīs vides nav paredzētas izmantošanai kā ražošanas vides. Ņemiet vērā, ka, beidzoties izmēģinājuma vides termiņam pēc 60 dienām, visi tajā esošie dati tiek dzēsti un nevar tikt atgūti. Pēc esošās vides termiņa beigām jūs varat pieteikties jaunai izmēģinājuma videi.

## <a name="select-a-power-apps-environment"></a>Atlasiet Power Apps vidi

Izmantojot integrāciju starp Talent un Power Apps vidēm, varat integrēt un paplašināt Talent datu lietojumu, izmantojot Power Apps rīkus. Izpratne par Power Apps vides mērķi ne tikai palīdzēs izveidot programmas, lai paplašinātu programmatūru Talent, bet arī palīdzēs izvēlēties vajadzīgo vidi programmatūras Talent nodrošināšanas laikā. Papildinformāciju par Power Apps vidēm, tostarp vides tvērumu, piekļuvi videi, kā arī vides izveidi un izvēli skatiet tēmā [Paziņojums par Power Apps vidēm](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Izvēloties Power Apps vidi, kurā izvietot programmatūru Talent, ņemiet vērā tālāk sniegtos norādījumus. 

1. LCS atlasiet **Pārvaldīt vides** vai dodieties tieši uz Power Apps administrēšanas centru, kur varat skatīt esošās vides un izveidot jaunas vides.
2. Katra Talent vide ir kartēta ar atsevišķu Power Apps vidi.
3. Power Apps vidē ir ietverta Talent, kā arī atbilstošās Power Apps, Power Automate un Common Data Service programmas. Ja tiek dzēsta Power Apps vide, kopā ar to tiek dzēstas arī programmas. Kad veicat Talent vides nodrošināšanu, jūs varat nodrošināt vidi **Izmēģinājumversija** vai **Ražošana**. Vides tips ir jāizvēlas atkarībā no veida, kādā šī vide tiks izmantota. 
4. Ir jāapsver datu integrācijas un pārbaudes metodes, piemēram, smilškastes, UAT vai ražošanas. Mēs iesakām apsvērt dažādos izvietojuma saistīšanas iespējas, jo vēlāk nevar viegli mainīt ar Power Apps vidi kartēto Talent vidi.
5. Tālāk norādītās Power Apps vides nevar lietot programmatūrā Talent, tāpēc tās netiek rādītas LCS esošajā atlases sarakstā.
 
    - **Noklusējuma Power Apps vides**— lai gan katram nomniekam tiek automātiski nodrošināta noklusējuma Power Apps vide, tās nav ieteicams izmantot programmatūrā Talent, jo visi nomnieku lietotāji var piekļūt Power Apps videi un nejauši sabojāt ražošanas datus, izmēģinot vai iepazīstot Power Apps vai Power Automate integrāciju.
   
    - **Izmēģinājuma vides** – šīs vides ir izveidotas beigu datumu, un tās pēc šī laika to derīgums beidzas, tāpēc vide un tajā ietvertās visas Talent instances tiek automātiski noņemtas.
   
    - **Neatbalstītie reģioni** – pašlaik pakalpojums Talent tiek atbalstīts tikai šādos reģionos: ASV, Eiropa, Apvienota Karaliste, Austrālija, Kanāda un Āzija.
  
6. Kad ir noteikta izmantošanai pareizā vide, var pāriet pie nodrošinājuma procesa. 
 
## <a name="grant-access-to-the-environment"></a>Piekļuves piešķiršana videi
Pēc noklusējuma videi var piekļūt globālais administrators, kas to izveidoja. Taču citiem programmas lietotājiem piekļuve ir jāpiešķir. Lai piešķirtu piekļuvi, ir jāpievieno lietotāji un jāpiešķir viņiem atbilstošās lomas Core HR vidē. Globālajam administratoram, kas izvietoja Talent, ir jāpalaiž programmas Attract un Onboard, lai pabeigtu inicializēšanu un iespējotu piekļuvi citiem nomnieku lietotājiem.  Kamēr tas nav izdarīts, citi lietotāji nevarēs piekļūt Attract un Onboard un tiem tiks rādītas piekļuves pārkāpumu kļūdas. Plašāku informāciju skatiet tēmā [Jaunu lietotāju izveide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) un [Drošības lomu piešķiršana lietotājiem](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
