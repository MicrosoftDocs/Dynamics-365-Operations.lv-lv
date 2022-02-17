---
title: Konfigurēt likmes
description: Likmes programmā Microsoft Dynamics 365 Human Resources definē, cik daudz darba devēji un nodarbinātie sniedz ieguldījumu atvieglojumā.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2822f6e339323ca6731ef042ffef3c400ae077d4
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068313"
---
# <a name="configure-rates"></a>Konfigurēt likmes


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Likmes definē, cik daudz darba devēji un nodarbinātie sniedz ieguldījumu atvieglojumā. Vērtība var būt vai nu summa vai vairāki elastīgie kredīti atkarībā no jūsu konfigurācijas.

Izmantojiet likmes, lai noteiktu, cik daudz darbinieku un darba devēju maksā par katru atvieglojumu, pamatojoties uz vairākiem faktoriem. Vajadzības likmes ir spēkā esošas, tāpēc varat uzturēt vēsturisku likmju uzskaiti. 

## <a name="set-up-rates"></a>Iestatīt likmes

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Likmes**.

2. Atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Norma** | Unikāls nosaukums, kas identificē atvieglojuma likmi. |
   | **Apraksts** | Atvieglojumu likmes apraksts. |
   | **Ir spēkā** | Datums, kurā likme kļūst efektīva. Noklusējuma vērtība ir pašreizējais sistēmas datums. Šim datumam jābūt atvieglojumu periodā vai pirms tā. Lai šo datumu iestatītu atvieglojuma plāna datumā, ir laba prakse. |
   | **Termiņa beigas** | Likmes beigu datums. 12/31/2154 (kas apzīmē "nekad") ir noklusētā vērtība. |
   | **Izmantot pakāpes** |  Lietojiet šo lauku, ja ir loģika, kas jāizmanto likmes noteikšanai. Piemēram, ja, pamatojoties uz vecumu, likmei ir jāpalielina, atlasiet šeit vērtību. Atlasiet **Vienkāršais līmenis** viena līmeņa atvieglojuma likmei vai **Divkāršais līmenis** divu līmeņu atvieglojuma likmei. Divkārša līmeņa piemērs ir līmenis, kas balstīts dzimumā un vecumā. Pēc vērtības atlases atlasiet **Darbības** un pēc tam atlasiet **Pakāpju likmes**. Ja jums ir vienotā likme, kas nemainās, atstājiet šo lauku tukšu. |
   | **Maksājumu biežums** | Norādiet, cik bieži atvieglojumu prēmijas likme jāmaksā atvieglojumu sniedzējam. Likmes, kuras ievadāt tālāk šajā tēmā aprakstītajā lapā, tiks balstītas uz maksāšanas biežumu, kuru norādīsiet šeit. Piemēram, ja ievadāt šajā laukā **Ik mēnesi** un ievadāt darbinieka likmi **$100**, ir pieņemts, ka atvieglojums darbiniekam izmaksās $100 mēnesi. Tomēr darbiniekam var maksāt divas reizes mēnesī, pamatojoties uz atvieglojumu maksājuma biežumu, kas iestatīts darbinieka ierakstā. Ja darbinieks pierakstās **Darbinieku pašapkalpošanā** daudzums, kuru viņi maksās, būs 50$, jo likme ar kādu rāda **Darbinieku pašapkalpošanās** ir pamatota darbinieka maksājumu biežumā. |
   | **Maksājumu biežuma likmes noapaļošana** | Likmes noapaļošanas metodes ir: standarta, saīsināta, parasta, uz leju un noapaļošana uz augšu. </br></br><ul><li>**Standarta** – vienmēr noapaļot uz augšu. Piemēram, 10,611 tiks noapaļots uz 10,62. – 10,231 tiks noapaļots uz -10,23. </li><li>**Saīsināta** – vienmēr noapaļot uz leju. Piemēram, 10,619 tiks noapaļots uz 10,61. – 10,231 tiks noapaļots uz -10,24. </li><li>**Parasta** – decimālskaitļu vērtības, kas beidzas ar 5, vai lielākas par 5, tiks noapaļotas no nulles. Decimālskaitļu vērtības, kas beidzas ar 4, vai mazākas par 4, tiks noapaļotas uz nulli. Piemēram, 10,615 tiks noapaļots uz 10,62. – 10,235 tiks noapaļots uz -10,24. 10,614 tiks noapaļots uz 10,61. – 10,234 tiks noapaļots uz -10,23. </li><li>**Uz leju** – noapaļot uz nulli. Piemēram, 10,619 tiks noapaļots uz 10,61. – 10,231 tiks noapaļots uz -10,23. </li><li>**Noapaļošana uz augšu** – noapaļot no nulles. Piemēram, 10,619 tiks noapaļots uz 10,62. – 10,231 tiks noapaļots uz -10,24. |
   | **Nesmēķētāja darbinieka summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par nesmēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Nesmēķētāja darba devēja summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par nesmēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Smēķētāja darbinieka summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par smēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Smēķētāja darba devēja summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par smēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Administratīvā summa** | Administratīvā summa, ko ietur trešās puses administrators. Šī ir summa, ko darba devējs maksā trešās puses administratoram, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Brīvā režīma kredīta likme** | Atvieglojuma izmaksu elastīgo kredītu skaits. Tas attiecas tikai uz likmēm, kas ir paredzētas atvieglojumu plāniem, kas saistīti ar elastīgo kredīta programmām. Ja izmantojat līmeņa likmes, elastīgā kredīta likme tiek definēta opcijās Darbības > Līmeņu likmes. |
   | **Izmaiņu spēkā stāšanās datums** | Datums, kad stājas spēkā atvieglojuma izmaiņas. Sistēma automātiski mainīs atvieglojumu likmi un atjauninās visus atvieglojumu plānus, kas saistīti ar šo likmi, ar noteikumu, ka palaižat likmes izmaiņu atjaunināšanas apstrādi. Neiestatiet šo datumu, ja vēlaties, lai sistēma automātiski atjauninātu nodarbināto atvieglojumu plānus, pamatojoties uz šo likmi. Tas parasti tiek rezervēts automātiskai turpmākai likmes izmaiņu apstrādei. **Izmaiņu spēkā stāšanās datumam** jāiekļaujas ieguvumu likmes spēkā stāšanās un termiņa beigu datumos. |
   | **Likmes izmaiņas pabeigtas** | Pēc tam, kad funkcija Likmju maiņas atjaunināšanas apstrāde mainīs atvieglojumu likmi, izvēles rūtiņa **Likmes maiņa pabeigta** tiks atlasīta automātiski. |

4. Lai izsekotu un uzturētu izmaiņas atvieglojumu likmes iestatījumā, atlasiet **Darbības** un pēc tam atlasiet **Uzturēt versijas**.

5. Atlasiet **Saglabāt**. 

## <a name="set-up-tier-rates"></a>Iestatīt līmeņa likmes

Varat izmantot līmeņa likmes savos likmes iestatījumos, ja likme mainās atkarībā no dažādiem faktoriem. Piemēram, varat konfigurēt līmeņa likmes, lai teiktu, ka, ja jūsu vecums ir līdz 34,99, tad nesmēķētāja summa ir 2. Ja jūsu vecums ir līdz 39,99, tad nesmēķētāja summa ir 3.

Varat arī izmantot divkāršos līmeņus. Ja atlasāt **Divkāršais līmenis** vērtībai **Izmantot līmeņus** veidlapā **Likmes iestatīšana**, varat definēt likmes, pamatojoties uz divām dimensijām. Piemēram, varat konfigurēt divkāršā līmeņa sistēmu, lai teiktu, ka, ja esat vīrietis un jūsu vecums ir līdz 34,99, tad nesmēķētāja summa ir 2. Ja esat vīrietis un jūsu vecums ir līdz 39,99, tad nesmēķētāja summa ir 3. Ja esat sieviete un jūsu vecums ir līdz 34,99, tad nesmēķētāja summa ir 1.8. Ja esat sieviete un jūsu vecums ir līdz 39,99, tad nesmēķētāja summa ir 2.8.

> [!IMPORTANT]
> Darbinieka ieraksta sadaļā **Personas informācija** ir opcija, kuru izmanto, lai noteiktu, vai darbinieks ir smēķētājs. Ja darbinieks ir ierakstīts kā darbinieks, tiks izmantota drošības likme. (Darbiniekam nekad netiek rādīta vāja norāde.)
   
1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Likmes**.

2. Atlasiet vienu vai vairākas likmes no saraksta, atlasiet **Darbības** un pēc tam atlasiet **Līmeņu likmes**.

3. Atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | apraksts |
   | --- | --- | 
   | **Apraksts** | Lauka **Apraksts** vērtība ir piemērota no apraksta, kas atrodas likmes iestatīšanas ierakstā. Tas palīdz noteikt, kuram likmes iestatījumam ir piesaistītas līmeņu likmes. |
   | **Pakāpes kods** | Atlasiet līmeņa kodu. Līmeņu kodi ir definēti lapā **Līmeņu kodi**. Sistēma automātiski parādīs līmeņu koda aprakstu režģī pa kreisi. |
   | **Pakāpes veids** | Norāda, kurš lauks jālieto kā līmeņa likmes aprēķina procesa atlases kritērijs. Piemēram:</br></br><ul><li>Ja lietots **Vecums**, sistēma atvieglojumu likmes aprēķina procesā izmantos darbinieka dzimšanas datumu.</li><li>Ja lietots **Atalgojums**, sistēma atvieglojumu likmes aprēķina procesā izmantos nodarbinātā gada atvieglojuma algu.</li><li>Ja tiek lietots **Darba veids**, darbinieka pašreizējais aktīvais pozīcijas ieraksts tiek izmantots, lai noteiktu darba veidu pēc pozīcijai saistītā darba ieraksta.</li></ul></br></br>Pakāpes veidi ir **Vecums**, **Alga**, **Fiziskais**, **Dzimums**, **Pilnas slodzes ekvivalents**, **Darba veids**, **Atlīdzības reģions** un **Līmenis**. | 
   | **Līmenis** | Vērtība, kas jāizmanto ar līmeņa veidu atvieglojumu likmes aprēķina procesa laikā. Piemēram:</br></br><ul><li>Ja pakāpes veids ir **Vecums**, tā būtu vecuma vērtība.</li><li>Ja pakāpes veids ir **Atalgojums**, tā būtu algas summa.</li><li> Ja pakāpes veids ir **Darba veids**, tas būtu darba veids.</li></ul></br></br>Ar pakāpes veidu **Vecums** vai **Alga**, vērtība laukā **Līmenis** attēlo pakāpes augšējo robežu. Ar līmeņa veidu **Darba veids**, līmeņa likmes atlasē tiek izmantota pilnās atbilstības pieeja. |
   | **Aprēķina tips** | Norāda, kā izmantot summu aprēķina summas laukā un kuru matemātisko aprēķinu veikt, ja nepieciešams. Ja aprēķina veids ir pamatsumma, izmantotā daudzuma lauks netiek mainīts. Ja aprēķina veids ir uz $ summu no algas vai seguma, tiek izmantots aprēķina daudzums un aprēķina daudzums matemātiskajos aprēķinos.</br></br>Ja aprēķina veids ir uz $ summu no algas, tiek izmantots šāds matemātiskais vienādojums:</br></br>Ikgadējās atvieglojumu algas, kas dalītas ar aprēķina summu (noapaļota uz augšu vai uz leju), sareizināta ar smēķētāja vai nesmēķētāja summu darbiniekam vai darba devējam.</br></br>Ja aprēķina veids ir uz $ summu no seguma, tiek izmantots šāds matemātiskais vienādojums:</br></br>Nodrošinājuma summa, kas dalīta ar aprēķina summu (noapaļota uz augšu vai uz leju), sareizināta ar smēķētāja vai nesmēķētāja summu darbiniekam vai darba devējam.</br></br>Abos aprēķinos aprēķina virziens tiek izmantots, lai noteiktu, vai noapaļot gada atvieglojumu algu vai nodrošinājuma summu, kas dalīta ar aprēķina summu uz augšu vai uz leju. |
   | **Aprēķinātā summa** | Summa, ko izmantot atvieglojuma likmes aprēķina procesā. Šī summa būs dalītājs līmeņa likmes matemātiskā aprēķina laikā. |
   | **Aprēķina virziens** | Virziens, kurā būtu jānoapaļo rezultāta summa. Sistēma atbalsta trīs aprēķina virzienus: tukšs (precīzā metode), **Palielināt** un **Samazināt**.</br></br><ul><li>Ja lauks ir tukšs, sistēma izmantos precīzu algas/nodrošinājuma summas aprēķinu, kas dalīts ar aprēķina summu. Ja šai vērtībai ir daļskaitlis, tas tiks izmantots aprēķinā.</li><li>**Pieauguma** gadījumā matemātiskais aprēķins palielinās algas/seguma summu, izdalītu ar aprēķina daudzumu līdz nākamajam veselajam skaitlim, kas nozīmē, ka 12,25 tiktu palielināts līdz 13.</li><li>**Samazinājuma** gadījumā matemātiskais aprēķins samazinās algas/seguma summu, izdalītu ar aprēķina daudzumu līdz pašreizējam veselajam skaitlim, kas nozīmē, ka 12,25 tiktu samazināts līdz 12.</li></ul> |
   | **Nesmēķētāja darbinieka summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par nesmēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Nesmēķētāja darba devēja summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par nesmēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Smēķētāja darbinieka summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par nesmēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Smēķētāja darba devēja summa** | Summa, kuru atvieglojumu nodrošinātājs ietur par nesmēķētāju darbinieku. Šī ir summa, ko darba devējs maksā atvieglojumu nodrošinātājam, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Administratīvā summa** | Administratīvā summa, ko ietur trešās puses administrators. Šī ir summa, ko darba devējs maksā trešās puses administratoram, un tai ir jābalstās likmes iestatījumu maksājumu biežumā. |
   | **Elastīgā kredīta nesmēķētāju likme** | Atvieglojuma izmaksu elastīgo kredītu skaits, pamatojoties uz aprēķiniem, kas noteikti nesmēķētāju līmenim. Piemēram, ja aprēķina tips ir **Par $ nodrošinājuma summu**, aprēķina summa ir 10 000 un elastīgā kredīta nesmēķētāju likme ir 6, tas nozīmē, ka, ja nesmēķētājs darbinieks izvēlas $10 000 nodrošinājumu, tas izmaksās sešus elastīgos kredītus. Ja tiek izvēlēta $20 000, tas izmaksās 12 elastīgos kredītus un tā tālāk. |
   | **Elastīgā kredīta smēķētāju likme** | Atvieglojuma izmaksu elastīgo kredītu skaits, pamatojoties uz aprēķiniem, kas noteikti smēķētāju līmenim. |

5. Atlasiet **Saglabāt**. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
