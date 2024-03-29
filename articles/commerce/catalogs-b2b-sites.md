---
title: Commerce katalogu izveide B2B vietnēm
description: Šajā rakstā ir aprakstīts, kā izveidot Commerce katalogus "bizness-biznesam Microsoft Dynamics 365 Commerce " (B2B).
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 7d4ed3e2a76924c2c3c0ba55e21ba648e8da7b76
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136831"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>Commerce katalogu izveide B2B vietnēm

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot Commerce preču katalogus Microsoft Dynamics 365 Commerce "bizness-biznesam" (B2B). Atbildes uz bieži uzdotiem jautājumiem par Commerce katalogiem B2B vietnēm skatiet Commerce [katalogos, kas paredzēts B2B FAQ](catalogs-b2b-sites-FAQ.md).

> [!NOTE]
> Šis raksts attiecas uz Dynamics 365 Commerce versiju 10.0.27 un vēlākiem laidieniem.

Varat izmantot Commerce katalogus, lai identificētu preces, ko vēlaties piedāvāt savā B2B tiešsaistes veikalos. Izveidojot katalogu, jūs identificējiet tiešsaistes veikalus, kuros preces tiek piedāvātas, pievienojiet preces, kuras vēlaties iekļaut, un pastipriniet preču piedāvājumus, pievienojot detalizētu informāciju par preču mazumtirdzniecību. Katram B2B tiešsaistes veikalam var izveidot vairākus katalogus, kā parādīts šajā ilustrācijā.

![Commerce preču katalogu priekšskatījums.](./media/Commerce_Catalogs.png)

Commerce preču katalogi ļauj definēt šādu informāciju:

- **Kataloga tips** - konfigurējiet vērtību kā **B2B**. Varat definēt B2B katalogam raksturīgos rekvizītus, piemēram, navigācijas hierarhiju, debitoru hierarhiju un kataloga atribūtu metadatus. 
- **Katalogam raksturīga navigācijas hierarhija** — organizācijas var izveidot atšķirīgu kategorijas struktūru to konkrētam katalogam.
- **Katalogam raksturīgi atribūtu metadati** — atribūti satur detalizētu informāciju par preci. Piešķirot atribūtus navigācijas hierarhijas kategorijai, šo atribūtu vērtības var definēt tai kategorijai piešķirto preču līmenī. Tad organizācijas var veikt šos uzdevumus:

    - Definējiet katalogam raksturīgās atribūtu vērtības.
    - Kontrolēt atribūtu redzamību kataloga līmenī.
    - Atlasiet atsevišķu katalogu specifiskos uzlabotājus.

- **Kanāli** – organizācijas var saistīt vairāk nekā vienu B2B tiešsaistes kanālu ar katalogu. Pašlaik beigu atbalsts katalogiem ir pieejams tikai B2B tiešsaistes veikaliem.
- **Debitoru hierarhijas** – dotajā B2B kanālā organizācijas var izveidot specifisku katalogu, kas pieejams atlasītajiem B2B partneriem, saistot debitoru hierarhijas ar šo katalogu.
- **Cenu grupas** - jūs varat konfigurēt cenas un veicināšanas pasākumi, kas ir specifiski noteiktam katalogam. Šī iespēja ir galvenais iemesls kataloga definēšana B2B kanālam. Kataloga cenu grupas ļauj organizācijām padarīt produktus pieejamus to paredzētajām B2B organizācijām un piemērot savas vēlamās cenu noteikšanas un atlaides. B2B debitori, kuri pasūta no konfigurēta kataloga, var gūt labumu no īpašām cenām un veicināšanas pasākumiem pēc pieteikšanās Commerce B2B vietnē. Lai konfigurētu katalogam raksturīgās cenas, **atlasiet cenu** grupas **cilnē Katalogi**, lai saistītu vienu vai vairākas cenu grupas ar katalogu. Visi tirdzniecības līgumi, cenu korekcijas žurnāli un papildu atlaides, kas ir saistītas ar to pašu cenu grupu, tiks piemērotas, kad debitori ir pasūtīti no šī kataloga. (Papildu atlaides ietver sliekšņa, daudzuma un komplekta atlaides.) Papildinformāciju par cenu grupām skatiet sadaļā [Cenu grupas](price-management.md#price-groups).

> [!NOTE]
> Šis līdzeklis ir pieejams, sākot ar versiju Dynamics 365 Commerce 10.0.27 izlaidi. Lai konfigurētu katalogam raksturīgās konfigurācijas, piemēram, navigācijas hierarhiju un debitoru hierarhiju programmā Commerce headquarters, **atveriet** līdzekļu pārvaldības darbvietu (**Sistēmas administrēšanas \>\> darbvietu līdzekļu pārvaldība**), **·** **iespējojiet vairāku katalogu lietošanu mazumtirdzniecības kanālu līdzeklī un pēc tam izpildiet 1110 CDX** darbu. Kad iespējojat šo iespēju, visi esošie katalogi, kas tiek izmantoti POS **veikaliem vai zvanu centram, tiks atzīmēti kā Kataloga veids = B2C** **lapā Katalogi**. Tikai esošie un jaunie katalogi, kas atzīmēti kā **kataloga tips = B2C**, ir piemērojami POS veikaliem un zvanu centram. 

## <a name="b2b-catalog-process-flow"></a>B2B kataloga apstrādes plūsma

Kataloga izveides un apstrādes procesam ir četras galvenās darbības. Katrs solis ir detalizētā veidā izskaidrots nākamajā sadaļā.

> [!NOTE]
> Pirms turpināt, pārliecinieties, vai katalogs ir atzīmēts kā **Kataloga tips = B2B**.

1. **[Konfigurācija](#configure-the-catalog)**

    - Saistiet navigācijas hierarhiju.
    - Norādiet laika efektīvos un beigu datumus, ja tie ir piemērojami.
    - Pievienojiet un kategorizēt preces.
    - Saistīt cenu grupas.
    - Saistiet debitoru hierarhiju, kas ir raksturīga jūsu B2B organizācijām. 
    - Saistiet noklusējuma dimensijas atribūtu grupu uzlabotājiem, piemēram, izmēru, stilu un krāsu.
    - Iestatiet atribūtu metadatus.

1. **[Apstiprināšana](#validate-the-catalog)** – šajā solī tiek palaisti apstiprināšanas noteikumi, kas īsteno īpašu uzvedību. Daži piemēri:

    - Pārliecinieties, ka nav ne kategorizētu preču.
    - Pārliecinieties, ka visi krājumi, kas ir sašķiroti katram kanālam, ir saistīti ar katalogu.

1. **[Apstiprinājums](#approve-the-catalog)**
1. **[Publicēšana](#publish-the-catalog)**

## <a name="set-up-the-catalog"></a>Iestatīt katalogu

Lietojiet šīs sadaļas informāciju, lai iestatītu katalogu.

### <a name="configure-the-catalog"></a>Konfigurējiet katalogu

Lai konfigurētu katalogu, programmā **\> Commerce headquarters dodieties uz sadaļu \> Mazumtirdzniecības un tirdzniecības katalogi** un preču klāsti.

Izveidojot jaunu katalogu, tas vispirms ir jāsaista ar vienu vai vairākiem kanāliem. Kataloga izveides laikā var izmantot tikai tos krājumus [, kas](/dynamics365/unified-operations/retail/assortments) ir saistīti ar atlasīto kanāla preču klāstu. Lai saistītu katalogu ar vienu vai vairākiem kanāliem, **atlasiet Pievienot** **kataloga iestatīšanas lapas** **Commerce kanālu kopsavilkuma cilnē**. Pārliecinieties, ka katalogs ir atzīmēts kā **Kataloga tips = B2B**.

#### <a name="associate-the-navigation-hierarchy"></a>Saistīt navigācijas hierarhiju

Lai katalogam pievienotu preces, ir jāatlasa navigācijas hierarhija. Navigācijas hierarhija atbalsta kataloga kategoriju struktūru. Jāatlasa viena no navigācijas hierarhijām, kas ir saistītas ar kanāliem **, ko atlasījāt lapas Kataloga iestatīšana kopsavilkuma** cilnē **Komercijas** kanāli. Lai saistītu noklusējuma navigācijas hierarhiju ar katru kanālu, dodieties uz sadaļu **Mazumtirdzniecības un komercijas \> kanāla \> iestatīšanas kanāla kategorijas un preces īpašības**.

#### <a name="specify-time-effective-and-expiration-dates"></a>Norādīt laika efektīvos un beigu datumus

Lai norādītu katalogam spēkā stāšanās un beigu datumus, atlasiet kataloga hierarhijas augšējo mezglu, lai atgrieztos galvenajā kataloga virsraksta skatā. Pēc tam kopsavilkuma cilnē Vispārīgi **konfigurējiet** efektīvos un termiņa beigu datumus pēc vajadzības.

#### <a name="add-and-categorize-products"></a>Pievienot un kategorizēt preces

Lai konfigurētu katalogam pievienojamās preces, programmā Commerce headquarters dodieties uz sadaļu **Mazumtirdzniecības un tirdzniecības \> katalogi un preču klāsts \> visiem katalogiem**. Pēc tam cilnē **Katalogi** atlasiet Pievienot **preces**.

Vai arī atlasiet mezglu navigācijas hierarhijā. Pēc tam preces varēsiet pievienot tieši kategorijai katalogā.

#### <a name="associate-price-groups"></a>Saistīt cenu grupas

Lai konfigurētu katalogam pievienojamās preces, programmā Commerce headquarters dodieties uz sadaļu **Mazumtirdzniecības un tirdzniecības \> katalogi un preču klāsts \> visiem katalogiem**. Pēc tam cilnē **Katalogi** atlasiet Pievienot **preces**. 

Preces, kas **tika** pievienotas katalogam no navigācijas hierarhijas saknes zara, darbību rūtī atlasot Pievienot preces, pārmantos to kategorijas, ja avota navigācijas hierarhija ir saistīta arī ar katalogu. Izmaiņas kategorijās, kas tiek veiktas avota navigācijas hierarhijā, nekavējoties tiks atspoguļotas katalogos. Lai atjauninātu kanālus, vēlreiz publicējiet katalogus.

Vai arī navigācijas hierarhijā varat atlasīt zaru un pievienot preces tieši katalogā atlasītajai kategorijai. 

Kad pievienojat preces, būs **pieejama opcija Automātiski iekļaut visus variantus, ja būs atlasīts tikai** preces šablons. Lai nepieļautu visu variantu iekļaušanu, atlasiet preces šablonam vismaz vienu variantu. 

> [!NOTE]
> Ja liels preču šablonu atlasē izvēlaties automātiski iekļaut visus variantus, var rasties ilgāks apstrādes laiks. Apjomīgām atlasēm ieteicams **izvēlēties Iekļaut visus variantus** katalogu lapas darbību rūtī, lai palaistu operāciju pakešveida režīmā. Ja katalogā ietverat tikai preces šablonu un neietverat variantus, variantu atlasītājs var nebūt pieejams, kad pārvietojaties uz detalizētas informācijas lapu par preci. 

Lai konfigurētu katalogam raksturīgās cenas, ir jāpiesaista katalogam viena vai vairākas cenu grupas. Lai saistītu cenu grupas ar katalogu, programmā Commerce headquarters dodieties uz sadaļu **Mazumtirdzniecības un tirdzniecības \> katalogi un preču klāsti \> visos katalogos**. Pēc tam cilnes **Katalogi** sadaļā Cenu **noteikšana** atlasiet **Cenu grupas**. Visi tirdzniecības līgumi, cenu korekcijas žurnāli un papildu atlaides (slieksnis, daudzums un komplekta atlaides), kas ir saistītas ar to pašu cenu grupu, tiks piemērotas, kad debitoru pasūtījums ir no kataloga.

Papildinformāciju par cenu grupām skatiet sadaļā [Cenu grupas](price-management.md#price-groups).

> [!NOTE]
> No visu katalogu lapas nevar izveidot jaunu **cenu** grupu. Tā vietā tā ir jāizveido no lapas **Visas cenu** grupas. Pēc tam jums tas ir jāsaista ar katalogu **visu katalogu** lapā.

#### <a name="associate-a-customer-hierarchy"></a>Saistīt debitoru hierarhiju

Lai saistītu debitoru hierarhijas, programmā Commerce headquarters dodieties uz sadaļu **Mazumtirdzniecības un komercijas \> katalogi un preču klāsti \> visos katalogos**. Pēc tam cilnes Katalogi **sadaļā Debitoru** **hierarhija atlasiet Piešķirt hierarhijas,** **lai saistītu vienu vai vairākas debitoru hierarhijas** ar katalogu.

> [!NOTE]
> Nevarat izveidot jaunu debitoru hierarhiju no visu **katalogu** lapas. Tā vietā tā ir jāizveido no **Debitoru hierarhiju** lapas. Pēc tam jums tas ir jāsaista ar katalogu **visu katalogu** lapā.

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>Saistīt noklusējuma dimensijas atribūtu grupu uzlabotājiem, piemēram, izmēru, stilu un krāsu

Lai programmā Commerce Headquarters saistītu noklusējuma dimensijas atribūtu grupu uzlabotājiem, piemēram, izmēra, stila un krāsas, **pārejiet uz sadaļu Mazumtirdzniecības un Commerce \> Catalogs \> un preču klāsts visiem katalogiem**. Pēc tam cilnes **Katalogi** sadaļā **Atribūti** atlasiet **Atribūtu grupas**.

#### <a name="set-attribute-metadata"></a>Atribūtu metadatu iestatīšana

Lai konfigurētu atribūtu metadatus, programmā Commerce headquarters dodieties uz sadaļu **Mazumtirdzniecības un commerce \> katalogi un preču klāsti \> visos katalogos**. Pēc tam cilnes Katalogi **sadaļā Atribūti** **atlasiet Iestatīt** atribūtu metadatus **.** Lai atlasītu atribūtus, **kuriem** jābūt skatāmiem un pārdefinējamiem, atlasiet kategoriju saistītajā katalogam raksturīgajā navigācijas hierarhijā un pēc tam sadaļā Kataloga preces īpašības atlasiet atribūtu. Pēc tam atlasiet **Rādīt atribūtu kanālā**. Pēc noklusējuma visi skatāmie atribūti ir arī meklējami. Lai atribūtus pēc izvēles varētu pārdefinēt, atlasiet **Var precizēt**.

### <a name="validate-the-catalog"></a>Kataloga validēšana

Pirms jaunais katalogs ir pieejams lietošanai, tas ir jāpārbauda un jāpublicē.

Lai pārbaudītu katalogu, veiciet šādas darbības:

1. Cilnes Katalogi lapas Visi katalogi **sadaļā** Pārbaudīt atlasiet **Pārbaudīt** katalogu **·**, lai izpildītu pārbaudi.**·** Šis solis ir obligāts. Tas apstiprinās, ka nepieciešamais iestatījums ir pareizs.
1. Atlasiet **Skatīt rezultātus**, lai skatītu pārbaudes detaļas. Ja tiek atrastas kļūdas, jums jāizlabo dati un pēc tam vēlreiz jāpalaiž pārbaude, līdz tā tiek no jauna veikta.

> [!NOTE]
> Ja **kataloga tips = B2B**, apstiprināšana neizdosies, ja katalogam pievienosiet POS veikalus vai zvanu centru. B2B katalogiem drīkst būt tikai B2B tiešsaistes kanāli, kas ar tiem saistīti. Apstiprināšana neizdosies arī tad, ja debitora hierarhija nav saistīta ar B2B katalogu. 

### <a name="approve-the-catalog"></a>Apstiprināt katalogu

Kad katalogs ir pārbaudīts, tam jābūt apstiprinātam.

Lai sāktu kataloga apstiprināšanas darbplūsmu, sekojiet šiem soļiem.

1. Visu katalogu lapas darbību **rūtī** atlasiet Darbplūsmas **\> iesniegt**.
1. Dodieties uz **mazumtirdzniecības un Commerce \> Headquarters iestatīšanas \> Commerce darbplūsmām, lai konfigurētu soļus** un pilnvarotos darbplūsmas lietotājus. Darbplūsma definēs soļus, kas ir nepieciešami, lai iegūtu katalogu ar **statusu Apstiprināts**.

### <a name="publish-the-catalog"></a>Kataloga publicēšana

Kad kataloga statuss ir **Apstiprināts**, to var publicēt, izvēlnē **Katalogi** atlasot **Publicēt**. Kad katalogs ir publicēšanas **stāvoklī**, to var izmantot zvanu centra pasūtījuma ierakstā un sūtīt kataloga procesus. Jūs varat publicēt katalogu manuāli vai izmantojot pakešveida procesu. Katalogam definētais efektīvais datums nosaka, kad preces ir pieejamas tiešsaistes veikalā. Jūsu definētais beigu datums nosaka, kad preces tiek noņemtas no tiešsaistes veikala.

> [!NOTE]
> Varat publicēt katalogu, kurā ir preces ar brīdinājumiem. Tomēr šīs preces netiks rādītas tiešsaistes veikalā.

## <a name="additional-resources"></a>Papildu resursi

[Commerce katalogu paplašināmības ietekme B2B pielāgojumiem](catalogs-b2b-sites-dev.md)

[Bieži uzdotie jautājumi par Commerce katalogiem B2B vietnēm](catalogs-b2b-sites-FAQ.md)

[Kataloga izdošanas modulis](catalog-picker.md)
