---
title: Konfigurēt likmes
description: Likmes programmā Microsoft Dynamics 365 Human Resources definē, cik daudz darba devēji un nodarbinātie sniedz ieguldījumu atvieglojumā.
author: andreabichsel
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e397e20b6b6307349020c8dfd238b4b59eeca527
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419570"
---
# <a name="configure-rates"></a>Konfigurēt likmes

Likmes programmā Microsoft Dynamics 365 Human Resources definē, cik daudz darba devēji un nodarbinātie sniedz ieguldījumu atvieglojumā. Vērtība var būt summa vai elastīgie kredīti atkarībā no jūsu konfigurācijas.

Izmantojiet likmes, lai noteiktu, cik daudz darbinieku un darba devēju maksā par katru atvieglojumu, pamatojoties uz vairākiem faktoriem. Vajadzības likmes ir spēkā esošas, tāpēc varat uzturēt vēsturisku likmju uzskaiti. 

## <a name="set-up-rates"></a>Iestatīt likmes

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Likmes**.

2. Atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Norma** | Unikāls nosaukums, kas identificē atvieglojuma likmi. |
   | **Apraksts** | Atvieglojumu likmes apraksts. |
   | **Ir spēkā** | Datums, kad likme ir spēkā. Noklusējuma vērtība ir pašreizējais sistēmas datums. 
   | **Termiņa beigas** | Likmes beigu datums. 12/31/2154 (kas apzīmē "nekad") ir noklusētā vērtība. |
   | **Izmantot pakāpes** | Līmenis, ko izmantot atvieglojumu likmes aprēķinam. Vienkāršais līmenis viena līmeņa atvieglojuma likmei vai divkāršais līmenis divu līmeņu atvieglojuma likmei. Divkārša līmeņa piemērs ir līmenis, kas balstīts dzimumā un vecumā. |
   | **Maksājumu biežums** | Maksājumu biežums, kas nosaka to, cik bieži atvieglojuma prēmijas likme tiek izmaksāta atvieglojuma nodrošinātājam. Piemēram, ja maksājuma biežums ir reizi mēnesī, tad atvieglojumu likme apzīmē ikmēneša maksājuma summu. |
   | **Maksājumu biežuma likmes noapaļošana** | Likmes noapaļošanas metode: standarta vai saīsinātā. |
   | **Nesmēķētāja darbinieka summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par nesmēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Nesmēķētāja darba devēja summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par nesmēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Smēķētāja darbinieka summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par smēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Smēķētāja darba devēja summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par smēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Administratīvā summa** | Administratīvā summa, ko ietur trešās puses administrators. Šī ir summa, ko darba devējs maksā trešās puses administratoram, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Brīvā režīma kredīta likme** | Atvieglojuma izmaksu elastīgo kredītu skaits. Tas attiecas tikai uz likmēm, kas ir paredzētas atvieglojumu plāniem, kas saistīti ar elastīgo kredīta programmām. Ja izmantojat līmeņa likmes, elastīgā kredīta likme tiek definēta opcijās Darbības > Līmeņu likmes. |
   | **Izmaiņu spēkā stāšanās datums** | Datums, kad stājas spēkā atvieglojuma izmaiņas. Sistēma automātiski mainīs atvieglojumu likmi un atjauninās visus atvieglojumu plānus, kas saistīti ar šo likmi, kamēr vien palaižat likmes izmaiņu atjaunināšanas apstrādi. Neiestatiet šo datumu, ja vēlaties, lai sistēma automātiski atjauninātu nodarbināto atvieglojumu plānus, pamatojoties uz šo likmi. Tas parasti tiek rezervēts automātiskai turpmākai likmes izmaiņu apstrādei. Izmaiņu spēkā stāšanās datumam jāatbilst atvieglojumu likmes stāšanās spēkā un beigu datumam. |
   | **Likmes izmaiņas pabeigtas** | Pēc tam, kad funkcija Likmju maiņas atjaunināšanas apstrāde mainīs atvieglojumu likmi, izvēles rūtiņa **Likmes maiņa pabeigta** tiks atlasīta automātiski. |

4. Lai izsekotu un uzturētu izmaiņas atvieglojumu likmes iestatījumā, atlasiet **Darbības** un pēc tam atlasiet **Uzturēt versijas**.

5. Atlasiet **Saglabāt**. 

## <a name="set-up-tier-rates"></a>Iestatīt līmeņa likmes

Varat izmantot līmeņa likmes savos likmes iestatījumos, ja likme mainās atkarībā no dažādiem faktoriem. Piemēram, varat konfigurēt līmeņa likmes, lai teiktu, ka, ja jūsu vecums ir līdz 34,99, tad nesmēķētāja summa ir 2. Ja jūsu vecums ir līdz 39,99, tad nesmēķētāja summa ir 3.

Varat arī izmantot divkāršos līmeņus. Ja atlasāt **Divkāršais līmenis** vērtībai **Izmantot līmeņus** veidlapā **Likmes iestatīšana**, varat definēt likmes, pamatojoties uz divām dimensijām. Piemēram, varat konfigurēt divkāršā līmeņa sistēmu, lai teiktu, ka, ja esat vīrietis un jūsu vecums ir līdz 34,99, tad nesmēķētāja summa ir 2. Ja esat vīrietis un jūsu vecums ir līdz 39,99, tad nesmēķētāja summa ir 3. Ja esat sieviete un jūsu vecums ir līdz 34,99, tad nesmēķētāja summa ir 1.8. Ja esat sieviete un jūsu vecums ir līdz 39,99, tad nesmēķētāja summa ir 2.8.

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Likmes**.

2. Atlasiet vienu vai vairākas likmes no saraksta, atlasiet **Darbības** un pēc tam atlasiet **Līmeņu likmes**.

3. Atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | apraksts |
   | --- | --- | 
   | **Apraksts** | Lauka **Apraksts** vērtība ir piemērota no apraksta, kas atrodas likmes iestatīšanas ierakstā. Tas palīdz noteikt, kuram likmes iestatījumam ir piesaistītas līmeņu likmes. |
   | **Pakāpes kods** | Atlasiet līmeņa kodu. Līmeņu kodi tiek definēti Līmeņu kodu veidlapā. Sistēma automātiski parādīs līmeņu koda aprakstu režģī pa kreisi. |
   | **Pakāpes veids** | Norāda, kurš lauks jālieto kā līmeņa likmes aprēķina procesa atlases kritērijs. Piemēram:</br></br><ul><li>Ja lietots **Vecums**, sistēma atvieglojumu likmes aprēķina procesā izmantos darbinieka dzimšanas datumu.</li><li>Ja lietots **Atalgojums**, sistēma atvieglojumu likmes aprēķina procesā izmantos nodarbinātā gada atvieglojuma algu.</li><li>Ja lietots **Darba veids**, sistēma izmantos darbinieka pašreizējo aktīvās pozīcijas ierakstu, lai noteiktu darba veidu pēc darba ieraksta, kas saistīts ar amatu.</li></ul></br></br>Pakāpes veidi ir **Vecums**, **Alga**, **Fiziskais**, **Dzimums**, **Pilnas slodzes ekvivalents**, **Darba veids**, **Atlīdzības reģions** un **Līmenis**. | 
   | **Līmenis** | Vērtība, kas jāizmanto ar līmeņa veidu atvieglojumu likmes aprēķina procesa laikā. Piemēram:</br></br><ul><li>Ja pakāpes veids ir **Vecums**, tā būtu vecuma vērtība.</li><li>Ja pakāpes veids ir **Atalgojums**, tā būtu algas summa.</li><li> Ja pakāpes veids ir **Darba veids**, tas būtu darba veids.</li></ul></br></br>Ar pakāpes veidu **Vecums** vai **Alga**, vērtība laukā **Līmenis** attēlo pakāpes augšējo robežu. Ar pakāpes veidu **Darba veids** sistēma izmanto precīzas atbilstības pieeju pakāpes likmes atlases laikā. |
   | **Aprēķina tips** | Norāda, kā izmantot summu aprēķina summas laukā un kuru matemātisko aprēķinu veikt, ja nepieciešams. Ja aprēķina tips ir fiksēta summa, sistēma izmanto summas laukus, kā tas ir. Ja aprēķina tips ir USD par algu vai nodrošinājumu, sistēma izmanto aprēķina summu un aprēķina virzienu savā matemātiskajā aprēķinā.</br></br>Ja aprēķina tips ir USD par algu, sistēma izmantos šādu matemātisku vienādojumu:</br></br>Ikgadējās atvieglojumu algas, kas dalītas ar aprēķina summu (noapaļota uz augšu vai uz leju), sareizināta ar smēķētāja vai nesmēķētāja summu darbiniekam vai darba devējam.</br></br>Ja aprēķina tips ir USD par nodrošinājuma summu, sistēma izmantos šādu matemātisku vienādojumu:</br></br>Nodrošinājuma summa, kas dalīta ar aprēķina summu (noapaļota uz augšu vai uz leju), sareizināta ar smēķētāja vai nesmēķētāja summu darbiniekam vai darba devējam.</br></br>Abos aprēķinos aprēķina virziens tiek izmantots, lai noteiktu, vai noapaļot gada atvieglojumu algu vai nodrošinājuma summu, kas dalīta ar aprēķina summu uz augšu vai uz leju. |
   | **Aprēķinātā summa** | Summa, ko izmantot atvieglojuma likmes aprēķina procesā. Šī summa būs dalītājs līmeņa likmes matemātiskā aprēķina laikā. |
   | **Aprēķina virziens** | Virziens, kurā būtu jānoapaļo rezultāta summa. Sistēma atbalsta trīs aprēķina virzienus: tukšs (precīzā metode), **Palielināt** un **Samazināt**.</br></br><ul><li>Ja lauks ir tukšs, sistēma izmantos precīzu algas/nodrošinājuma summas aprēķinu, kas dalīts ar aprēķina summu. Ja šai vērtībai ir daļskaitlis, sistēma to izmantos aprēķinos.</li><li>Ja **Palielināt**, sistēma palielinās algas/nodrošinājuma summas matemātisko aprēķinu, kas dalīta ar aprēķina summu, līdz nākošajam veselajam skaitlim, kas nozīmē, ka 12,25 palielinātu līdz 13.</li><li>Ja **Samazināt** sistēma samazinās algas/nodrošinājuma summas matemātisko aprēķinu, kas dalīta ar aprēķina summu, līdz pašreizējam veselajam skaitlim, kas nozīmē, ka 12,25 samazinātu līdz 12.</li></ul> |
   | **Nesmēķētāja darbinieka summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par nesmēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Nesmēķētāja darba devēja summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par nesmēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Smēķētāja darbinieka summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par nesmēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Smēķētāja darba devēja summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par nesmēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Administratīvā summa** | Administratīvā summa, ko ietur trešās puses administrators. Šī ir summa, ko darba devējs maksā trešās puses administratoram, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Elastīgā kredīta nesmēķētāju likme** | Atvieglojuma izmaksu elastīgo kredītu skaits, pamatojoties uz aprēķiniem, kas noteikti nesmēķētāju līmenim. Piemēram, ja aprēķina tips ir **Par $ nodrošinājuma summu**, aprēķina summa ir 10 000 un elastīgā kredīta nesmēķētāju likme ir 6, tas nozīmē, ka, ja nesmēķētājs darbinieks izvēlas $10 000 nodrošinājumu, tas izmaksās sešus elastīgos kredītus. Ja tiek izvēlēta $20 000, tas izmaksās 12 elastīgos kredītus un tā tālāk. |
   | **Elastīgā kredīta smēķētāju likme** | Atvieglojuma izmaksu elastīgo kredītu skaits, pamatojoties uz aprēķiniem, kas noteikti smēķētāju līmenim. |

5. Atlasiet **Saglabāt**. 
