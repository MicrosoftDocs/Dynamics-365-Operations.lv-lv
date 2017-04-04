---
title: "Izmantotu pārlūkos atrast informāciju"
description: "Microsoft Dynamics 365 operācijām, daudzās jomās ir pārlūkiem, kas var palīdzēt jums viegli atrast pareizo vai vēlamo vērtību. Pārlūkiem, kas padara šīs vadīklas atbilstošāka, un padarītu lietotājus vairāk produktīvu ir pievienoti vairāki uzlabojumi. Šajā tēmā uzzināsit par šiem jaunajiem līdzekļiem pārlūkošanas un saņems dažus noderīgus padomus, lai iegūtu optimālu no pārlūkos sistēmā."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 6a25593632575dcd71fa4a3c9cf5b83c9f8ecd39
ms.lasthandoff: 03/31/2017


---

# <a name="use-lookups-to-find-information"></a>Izmantotu pārlūkos atrast informāciju

Microsoft Dynamics 365 operācijām, daudzās jomās ir pārlūkiem, kas var palīdzēt jums viegli atrast pareizo vai vēlamo vērtību. Pārlūkiem, kas padara šīs vadīklas atbilstošāka, un padarītu lietotājus vairāk produktīvu ir pievienoti vairāki uzlabojumi. Šajā tēmā uzzināsit par šiem jaunajiem līdzekļiem pārlūkošanas un saņems dažus noderīgus padomus, lai iegūtu optimālu no pārlūkos sistēmā.  

<a name="responsive-lookups"></a>Atsaucīgi pārlūkus
------------------

Iepriekšējās versijās Dynamics 365 operācijām, mijiedarbojoties ar uzmeklēšanas vadīklu, lietotājs būtu veikt tiešas darbības, lai atvērtu nolaižamo izvēlni. Šīs varbūt bija, ievadot zvaigznīti (\*), lai filtrētu, pamatojoties uz vadīklas pašreizējo vērtību uzmeklēšanas vadīklu, noklikšķiniet uz pogas nolaižamo sarakstu vai lietojot **Alt**+**lejupvērstā bultiņa** tastatūras īsinājumtaustiņu. Uzmeklēšanas vadīklu tika grozīti, lai labāk atbilstu pašreizējai web praksei šādos veidos:

-   Uzmeklēšanas nolaižamās izvēlnes tagad automātiski atveras pēc nelielas pauzes, ierakstot ar nolaižamo izvēlņu saturu filtrētas pēc uzmeklēšanas vadīklu vērtību.
    -   Ņemiet vērā, ka veco uzvedību nolaižamajā automātisku atvēršanu pēc ievadot zvaigznīti (\*) ir novecojusi.
-   Pēc tam, kad ir atvērts uzmeklēšanas nolaižamo izvēlni, tad notiks šādi:
    -   Kursors paliek uzmeklēšanas vadīklu (nevis uzmanību pārceļas uz nolaižamo izvēlni) lai varētu turpināt veikt grozījumus vadīklas vērtību. Tomēr, lietotājs var lietot **augšupvērstā bultiņa** un **lejupvērstā bultiņa** jāmaina rindas nolaižamajā izvēlnē un enter, lai atlasītu pašreizējās rindas nolaižamajā izvēlnē.
    -   Saturu, nolaižamajā izvēlnē, koriģēs pēc jebkuras izmaiņas tiek veiktas uzmeklēšanas vadīklu vērtību.

Piemēram, apsveriet uzmeklēšanas lauku ar nosaukumu **pilsētas**. 

Kad fokusējums atrodas **pilsētas** jomā, var sākt meklēt, ierakstot dažas vēstules, piemēram, "col." vēlamā pilsēta  Pēc tam, kad jūs pārtraucat rakstīt, uzmeklēšanas atvērsies automātiski, filtrēts, šīm pilsētām, kas sākas ar "krāsa". 

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png) 

Šajā brīdī, kursors, joprojām ir uzmeklēšanas lauks. Ja turpināsit rakstīt tā vērtība ir "kolonnas", uzmeklēšanas saturu automātiski pielāgotu atspoguļo jaunākās vērtību vadīklā. 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

Pat tad, ja uzmanības centrā joprojām ir uzmeklēšanas vadīklu, varat arī izmantot **augšupvērstā bultiņa** vai **lejupvērstā bultiņa** taustiņu iezīmējiet rindu, kuru vēlaties atlasīt. Ja nospiežat **Enter** izceltā rinda tiks atlasīti no pārlūkošanas un vadīklas vērtība tiek atjaunināta. 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Ierakstot vairāk nekā ID
Ievadot datus, tas ir dabiski, ka lietotājiem, lai mēģinātu identificēt entītiju, piemēram, debitors vai kreditors, attiecībā uz nosaukumu, nevis identifikatoru, kas apzīmē vienības. Dynamics 365 operācijām, daudzas (bet ne visi) pārlūkiem tagad ļauj ievadīt konteksta datus pašreizējā versijā. Šo spēcīgs līdzeklis ļauj lietotājam ievadīt ID vai attiecīgais vārds uzmeklēšanas vadīklu. 

Piemēram, uzskata, **debitora konta** lauks, veidojot pārdošanas pasūtījumu. Šajā laukā ir norādīts **─ ülais kontu ID** attiecībā uz klientu, bet lietotājs parasti gribētu ieiet **konta nosaukums** nevis **─ ülais kontu ID** šim laukam, veidojot pārdošanas pasūtījumu, piemēram, "Meža Wholesales", nevis "ASV-003."

Ja lietotājs sāka iebraukt **─ ülais kontu ID** vērā uzmeklēšanas vadīklu nolaižamajā izvēlnē automātiski tiks atvērts, kā aprakstīts iepriekšējā sadaļā, un lietotājs varētu redzēt uzmeklēšanas, kā parādīts zemāk.

[![Kad ievadīts debitora konta ID konteksta uzmeklēšanas](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Tomēr lietotājs var ievadīt arī tagad sākumā **konta nosaukums** arī. Ja tas ir atrasta, lietotājs redzēs šādu uzmeklēšanas. Paziņojums cik **nosaukums** kolonna tiek pārvietots par pirmo uzmeklēšanas kolonnu, un kā uzmeklēšanas sakārtota un filtrēta pamatā **nosaukums** kolonnu.

[![Ievadot debitora nosaukuma konteksta uzmeklēšanas](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Plašākas filtrēšanas un kārtošanas izmantošanu režģa kolonnu galvenes
Uzmeklēšanas uzlabojumi apsprieda iepriekšējās divās sadaļās ievērojami uzlabotu lietotāja spēju orientēties rindās, uzmeklēšanas pamatā "sākas ar" kratīšanu **ID** vai **Name** uzmeklēšanas laukā. Tomēr ir situācijas, kurās sarežģītāku filtrēšanu (vai šķirošanas) ir nepieciešama, lai atrastu pareizo rindu. Šajās situācijās, lietotāju vajadzībām izmantot filtrēšanas un kārtošanas opcijas režģa kolonnu galvenēs iekšpusē uzmeklēšanas. Piemēram, apsveriet pārdošanas pasūtījuma rindas ievadīšanas darbinieku, kurš ir nepieciešams atrast labi "kabelis" kā produktu. Ierakstot "kabelis" **krājums** kontroles nav lietderīga, jo nav nekādu produktu nosaukumus, kas sākas ar "kabelis". 

![emptyitemlookup](./media/emptyitemlookup.png) 

Tā vietā, lietotāju vajadzībām, lai notīrītu vērtības uzmeklēšanas vadīklu, atveriet uzmeklēšanas nolaižamo izvēlni un filtra nolaižamo izvēlni, izmantojot režģa kolonnas galvenē, kā parādīts zemāk. Peli (vai touch) lietotājs var vienkārši noklikšķiniet (vai pieskarties) jebkuras kolonnas virsraksta, lai piekļūtu filtrēšanas un kārtošanas iespējas šai kolonnai. Tastatūras lietotāja, lietotājs vienkārši nepieciešams nospiest **Alt**+**pa****bultiņas** otrreiz, lai pārvietotu fokusu uz nolaižamo izvēlni, pēc kura lietotājs var ar tabulatoru aizejiet līdz pareizā kolonnas un pēc tam nospiediet taustiņu **CTRL +**+**G**, lai atvērtu nolaižamo izvēlni režģa kolonnu galvenes. 

[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png) 

Pēc tam, kad ir ticis izmantots filtrs (skatīt attēlu zemāk), lietotājs var atrast un atlasīt rindas kā parasti. 

![filtereditemlookup](./media/filtereditemlookup.png)


