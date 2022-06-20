---
title: Atpakaļ atdošanas izveide programmā POS
description: Šajā rakstā ir aprakstīts, kā pārdošanas punkta (POS) programmā sākt atgriešanas darbībām, kas ir jāveic, izmantojot kases ieņēmumus Microsoft Dynamics 365 Commerce no pārdošanas punkta (POS).
author: hhainesms
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.20
ms.openlocfilehash: a49e9abd0143d480cc1cafb05be5e995fb3cebdd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857002"
---
# <a name="create-returns-in-pos"></a>Atpakaļ atdošanas izveide programmā POS

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā pārdošanas punktā (POS) programmā sākt atgriešanas darbības, kas ir jāveic, izmantojot kases un pārvadāšanas Microsoft Dynamics 365 Commerce darbības vai debitora pasūtījumus.

> [!NOTE]
> Commerce 10.0.20 un jaunākās versijās ir pieejams jauns līdzeklis ar nosaukumu **Vienotā atpakaļ atdošanas apstrādes pieredze programmā POS**. Šis līdzeklis nodrošina konsekventāku un vienotu atpakaļ atdošanas procesu programmā POS neatkarīgi no darījuma veida (darījumiem skaidrā naudā bez piegādes vai debitoru pasūtījumiem) vai sākotnējā kanālā, kurā pasūtījums tika izveidots. Ieteicams ieslēgt šo jauno līdzekli visās organizācijās, lai palīdzētu uzlabot kopējo atpakaļ atdošanas procesa uzticamību, izmantojot POS.
>
> Kad līdzeklis ir ieslēgts, to nevar izslēgt.

## <a name="process-returns-by-using-the-return-transaction-operation"></a>Atpakaļ atdošanas apstrāde, izmantojot atpakaļ atdošanas darījuma operāciju

Atpakaļ atdošanas darījuma operāciju ir ieteicams pievienot POS [ekrāna izkārtojumam](pos-screen-layouts.md). Iepriekšējā laidienā, pirms Commerce versijas 10.0.20 laidiena, atpakaļ atdošanas darījuma operācija pareizi atbalsta tikai atpakaļ atdošanu darījumiem skaidrā naudā bez piegādes. Pēc tam, kad Commerce 10.0.20 versijas vai jaunākā laidienā ir ieslēgts līdzeklis **Vienotā atpakaļ atdošanas apstrādes pieredze programmā POS**, atpakaļ atdošanas darījumu operācijas atbalsta arī tādu atpakaļ atdošanu, kas rodas no klientu pasūtījumiem, piemēram, “izdošanas” vai “nosūtīt uz mājām” pasūtījumi, kuriem jau ir izrakstīts rēķins.

No atpakaļ atdošanas darījuma operācijas lietotāji var meklēt darījumus skaidrā naudā bez piegādes vai debitoru pasūtījumus, lai tos atdotu atpakaļ, ievadot jebkuru no četriem tālāk norādītajiem meklēšanas kritērijiem. Lietotāji var ievadīt šos kritērijus, izmantojot ierīces tastatūru, ekrāntastatūru vai svītrkodu skeneri.

- Kvīts ID
- Pasūtījuma numurs
- Kanāla atsauces ID (ko sauc arī par pasūtījuma apstiprinājuma ID)
- Rēķina ID

Ja tiek atrasts darījums vai pasūtījums, kas atbilst meklēšanas kritērijiem, tiek parādīta lapa **Atpakaļ atdodamās preces**. Tur lietotāji var norādīt krājumus, kas tiek atdoti atpakaļ. Viņi var ievadīt arī atpakaļ atdošanas daudzumus un pamatojuma kodus.

Katrai pasūtījuma rindai atpakaļ atdoto preču sarakstā POS tiek parādīta informācija par sākotnējo pirkšanas daudzumu un visiem iepriekš apstrādātajiem atpakaļ atdotajiem daudzumiem. Atpakaļ atdošanas daudzumam, ko lietotājs ievada pasūtījuma rindai, ir jābūt mazākam vai vienādam ar vērtību, kas ir laukā **Pieejams atdošanai atpakaļ**.

![Atpakaļ atdodamo preču lapa.](media/returnslist.png)

Ja atpakaļ atdošanas apstrādes laikā lietotājam ir fiziska prece un tai precei ir svītrkods, lietotājs var skenēt svītrkodu, lai reģistrētu atpakaļ atdošanu. Katra svītrkoda skenēšana palielina atpakaļ atdodamo daudzumu par vienu preci. Tomēr, ja svītrkoda etiķetei ir iegults daudzums, šis daudzums tiks ievadīts laukā **Atpakaļ atdots**.

Lietotāji var arī manuāli atlasīt atpakaļ atdodamās preces lapā **Atpakaļ atdodamās preces** un pēc tam atjaunināt lauku **Atpakaļ atdots**, izmantojot informācijas rūti labajā pusē.

Ja darījumam tiek norādīts maksimālais pieejamais **Atpakaļ atdotais** daudzums, lietotājs POS programmas joslā var atlasīt operāciju **Atlasīt visu**, lai iestatītu maksimālo atpakaļ atdodamo daudzumu visās rindās.

Katrai rindai, kurai ir **Atpakaļ atdotais** daudzums, lietotājam jāatlasa atpakaļ atdošanas pamatojuma kods, izmantojot informācijas paneli. Atpakaļ atdošanas pamatojuma kodi darījumiem skaidrā naudā bez piegādes tiek konfigurēti kā informācijas kodi veikala funkcionalitātes profilā. Debitoru pasūtījumu atpakaļ atdošanas pamatojumu kodi ir konfigurēti Dynamics 365 Commerce Headquarters lapā **Atpakaļ atdošanas pamatojumu kodi**.

Pēc tam, kad atpakaļ atdotais daudzums un pamatojuma kods ir iestatīts katrai precei, kas ir jāatdod atpakaļ, lietotājs POS programmas joslā var atlasīt **Atpakaļ atdošanas** operāciju, lai turpinātu apstrādi. Tiek parādīta POS darījumu lapa, kur grozam ir pievienotas iepriekšējā lapā atlasītās atpakaļ atdodamās preces. Preču **Atpakaļ atdodamie** daudzumi darījumā parādās kā negatīvu daudzumu rindas, un tiek aprēķināta atmaksas kopsumma.

Lietotāji var pievienot rindas atpakaļ atdodamajam darījumam, ja tie izveido apmaiņas pasūtījumu. Lietotāji atpakaļ atdošanas darījumam var pievienot arī papildu ekspromta atpakaļ atdodamās preces, izmantojot operāciju **Atdot atpakaļ preci** atlasītajai pievienotajai pārdošanas rindai ar pozitīvu daudzumu.

> [!NOTE]
> Programmas POS operācija **Atdot atpakaļ preci** nesniedz nekādu validāciju nevienam sākotnējam darījumam un ļauj atdot atpakaļ jebkuru preci. Tāpēc ieteicams atļaut veikt šo operāciju tikai sankcionētiem lietotājiem vai pieprasīt vadītāja pārlabošanu, ja šī operācija tiek izmantota.

Ja atmaksa ir jāveic darījuma laikā, organizācijas var konfigurēt [atmaksas maksājumu politikas](refund_policy_returns.md), kas ierobežo maksājumu metodes, kuras var izmantot, lai klientiem atmaksātu naudu. Ja sākotnējais darījums tika apmaksāts, izmantojot kredītkarti, atkarībā no maksājumu apstrādātāja un sistēmas konfigurācijas, lietotājiem var būt pieejama iespēja [izsniegt atmaksu oriģinālajai kartei](dev-itpro/linked-refunds.md). Šajā gadījumā atmaksu var apstrādāt, nepieprasot debitoram no jauna lasīt kredītkarti. Sākotnējais maksājuma marķieris tiek izmantots atmaksas izsniegšanai.

## <a name="other-return-options-in-pos"></a>Citas atpakaļ atdošanas opcijas programmā POS

Ja ir ieslēgts līdzeklis **Vienotā atpakaļ atdošanas apstrādes pieredze programmā POS**, lietotāji programmā POS var izmantot arī operāciju **Rādīt žurnālu**, lai uzsāktu darījuma skaidrā naudā bez piegādes vai debitora pasūtījuma atdošanu atpakaļ. Pēc tam žurnālā var atlasīt darījumu un pēc tam POS programmas joslā var atlasīt operāciju **Atdot atpakaļ**. Šī operācija ir pieejama tikai tad, ja pasūtījumā ir atpakaļ atdošanas rindas. Tās uzsāk tādu pašu lietotāja pieredzi kā operācija **Atgriezt darījumu**.

Lietotāji var izmantot arī POS operāciju **Pasūtījuma atsaukšana**, lai meklētu un atsauktu debitoru pasūtījumus. (Šo operāciju nevar izmantot darījumiem skaidrā naudā bez piegādes). Šajā gadījumā pēc debitora pasūtījuma izvēles POS programmas joslā esošo **Atpakaļ atdošanas** operāciju var izmantot, lai uzsāktu debitora pasūtījuma atdošanu atpakaļ. Šī operācija ir pieejama tikai tad, ja pasūtījumā ir atpakaļ atdošanas rindas. Tā uzsāk tādu pašu lietotāja pieredzi kā operācija **Atgriezt darījumu** vai **Rādīt žurnālu**.

## <a name="return-orders-are-posted-to-commerce-headquarters-as-sales-orders"></a>Atpakaļ atdotie pasūtījumi programmā Commerce Headquarters tiek iegrāmatoti kā pārdošanas pasūtījumi 

Ja ir ieslēgts līdzeklis **Vienotā atpakaļ atdošanas apstrādes pieredze programmā POS**, visas atpakaļ atdošanas, kas tiek izveidotas programmā POS, tiek ierakstītas Commerce Headquarters kā pārdošanas pasūtījumi ar negatīvām rindām. Iepriekšējos laidienos, pirms Commerce versijas 10.0.20 laidiena, lietotāji var atlasīt, vai atpakaļ atdotie pasūtījumi jāiegrāmato kā pārdošanas pasūtījumi ar negatīvām rindām vai arī tiem jābūt atpakaļ atdotiem pasūtījumiem, kas izveidoti, izmantojot atpakaļ atdoto preču autorizācijas (RMA) procesu. 

Līdzeklī **Vienotā atpakaļ atdošanas apstrādes pieredze programmā POS** opcija izmantot RMA procesu, lai izveidotu atpakaļ atdošanu programmā POS ir novecojusi. Ja šis līdzeklis ir ieslēgts, visas atpakaļ atdošanas tiks izveidotas kā pārdošanas pasūtījumi ar negatīvām rindām.

## <a name="offline-return-processing-improvements"></a>Bezsaistes atpakaļ atdošanas apstrādes uzlabojumi

Vairākumā gadījumu, kad tiek veikta atdošana atpakaļ programmā POS, sistēma mēģina veikt reāllaika pakalpojuma (RTS) izsaukumu uz Commerce Headquarters, lai validētu pašreizējos atdošanai atpakaļ pieejamos daudzumus. Šī validācija palīdz novērst krāpnieciskus scenārijus, kuros debitors mēģina atdot atpakaļ vienu un to pašu preci vairākās vietās.

Situācijās, kad RTS izsaukumu nevar veikt tīkla vai savienojamības problēmu dēļ, ir izveidots process, lai periodiski sinhronizētu atpakaļ atdoto daudzumu datus no Commerce Headquarters uz veikala kanāla datu bāzi. Šī kanāla puses atpakaļ atdošanas izsekošana palīdz nodrošināt, ka **Pieejams atdošanai atpakaļ** daudzums, kas tiek parādīts POS, ir pietiekami precīzs, pat ja POS ir bezsaistē. Tas nodrošina arī to, ka POS var turpināt validēt kanāla puses informāciju, lai palīdzētu novērst krāpnieciskas atpakaļ atdošanas.

Lai izmantotu bezsaistes atpakaļ atdošanas procesu atbilstošā veidā, organizācijām ir jāplāno **Atpakaļ atdošanas daudzumu** pakešuzdevums programmā Commerce Headquarters, lai tas bieži tiktu palaists. Ieteicams, lai šis darbs tiktu palaists tikpat bieži kā P darbs, kas jaunus darījumus no Commerce kanāliem pārnes uz Commerce Headquarters.

Darbs **Atpakaļ atdošanas daudzums** aprēķina daudzumu, kas ir pieejams atdošanai atpakaļ visiem pārdošanas pasūtījumiem, kas ir atrodami Commerce Headquarters. Pēc tam dati, ko darbs aprēķina, ir jānosūta uz kanālu datu bāzēm, lai varētu atjaunināt veikalu kanālus. Šim nolūkam tiek izmantots sadales darbs **Atpakaļ atdošanas daudzums** (1200). Tā kā dati par atpakaļ atdodamo daudzumu tiek sinhronizēti no programmas Commerce Headquarters, ja atpakaļ atdošana tiek apstrādāta POS, bet nevar veikt RTS izsaukumu, tad POS var izmantot kanāla puses atpakaļ atdošanas informāciju, lai validētu **Pieejams atdošanai atpakaļ** daudzumus attiecīgajai pārdošanas rindai.

Ja nevar veikt RTS izsaukumus un POS izmanto kanāla puses datus atpakaļ atdošanas validēšanai, tad brīdinājuma ziņojums informē lietotājus, ka viņi veido “bezsaistes” atpakaļ atdošanu. Tādā veidā viņi apzinās, ka **Pieejams atdošanai atpakaļ** daudzums, kas tiek parādīts POS, iespējams, ir novecojis un vairs nav precīzs, atkarībā no tā, kad darbs **Atpakaļ atdošanas daudzums** pēdējo reizi tika apstrādāts un sinhronizēts ar kanālu.

Piemēram, debitors nesen apstrādāja atpakaļ atdošanu pasūtījuma rindai citā kanālā, taču dati vēl nav sinhronizēti kanāla datu bāzēs, izmantojot darbu **Atpakaļ atdošanas daudzums**. Pēc tam debitors dodas uz citu veikalu un mēģina vēlreiz atdot atpakaļ to pašu preci. Šajā gadījumā, ja veikals nevar veikt RTS izsaukumu programmā Commerce Headquarters, lai iegūtu reāllaika atpakaļ atdošanas datus, tad POS ļaus preci atdot atpakaļ atkārtoti. Tomēr lietotājs tiek brīdināts, ka informācija, kas tiek izmantota validējot atdošanu atpakaļ, var būt novecojusi. Ziņojums, kuru lietotājs saņem, ir tikai brīdinājuma ziņojums. Tas neliedz lietotājam turpināt atpakaļ atdošanas procesu.

Ja kanāla puses informācija kāda iemesla dēļ nav atjaunināta un bezsaistes atpakaļ atdošana tiek apstrādāta daudzumam, kas pārsniedz faktisko **Pieejams atdošanai atpakaļ** daudzumu, tad var rasties kļūda, palaižot pārskata iegrāmatošanu, lai izveidotu darījumu Commerce Headquarters.

> [!NOTE]
> Ja ir ieslēgts līdzeklis **Vienotā atpakaļ atdošanas apstrādes pieredze programmā POS**, tad var piekļūt jauniem izvēles līdzekļiem, kas atbalsta serializētās preces atpakaļ atdošanas validāciju. Papildinformāciju skatiet sadaļā [Sērijveida kontrolētu preču atdošana atpakaļ pārdošanas punktā POS](POS-serial-returns.md).

## <a name="version-details"></a>Detalizēta informācija par versiju

Šajā sarakstā sniegtas minimālās versijas prasības dažādiem komponentiem.
- Commerce headquarters: versija 10.0.20
- Commerce Scale Unit (CSU): versija 9.30
- Pārdošanas punkts (POS): versija 9.30

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Iespējot pareizu nodokļu aprēķināšanu daļējai atgriešanai

Šis līdzeklis nodrošina, ka gadījumā, ja pasūtījums tiek atgriezts vairākus rēķinos, nodokļi beigās būs vienādi ar sākotnēji iekasēto nodokļu summu.

1. Līdzekļu pārvaldības **darbvietā** meklējiet Iespēju veikt **pareizu nodokļu aprēķinu atgrieztām daļējām kravēm**.
1. Atlasiet funkciju **Aktivizēt pareizu nodokļu aprēķinu atgriezt ar daļēju daudzumu** un pēc tam atlasiet **Aktivizēt**.

## <a name="set-up-return-locations-for-retail-stores"></a>Atgriešanas vietu iestatīšana mazumtirdzniecības veikaliem

Commerce ļauj iestatīt atgriešanas vietas, kuru pamatā ir mazumtirdzniecības infokodi un pārdošanas un mārketinga iemeslu kodi. Kad debitori atgriež pirkumus, kasieri bieži norāda atgriešanas iemeslu. Varat norādīt, ka atgrieztās preces ir jāpiešķir dažādām atgriešanas vietām krājumos, pamatojoties uz informācijas kodiem un pamatojuma kodiem, kurus kasieri izvēlas POS kases sistēmā.

Piemēram, debitors atgriež bojāto preci, un kasieris apstrādā atgriešanas darbību. Kad sistēmā Retail POS tiek rādīts atgriezto krājumu informācijas kods, kasieris atlasa bojāto atgriešanu apakškodu. Pēc tam atgrieztā prece tiek automātiski piešķirta noteiktai atgriešanas vietai.

Atgriešanas vieta var būt noliktava, atrašanās vieta noliktavā vai pat noteikta palete atkarībā no jūsu uzņēmuma iestatītajām krājumu vietām. Katru atgriešanas vietu var kartēt uz vienu vai vairākiem mazumtirdzniecības infokodiem, pārdošanas un mārketinga iemeslu kodiem.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms jūs iestatiet atgriešanas vietas, jums jāuzstāda sekojošos elementus:

- **Mazumtirdzniecības** informācijas kodi — tiek parādītas uzvednes POS kases sistēmā, kas ir iestatīta modulī **Mazumtirdzniecība**. Papildinformāciju skatiet informācijas [kodu iestatīšanai](/dynamicsax-2012/appuser-itpro/setting-up-info-codes).
- **Pārdošanas un mārketinga iemeslu kodi** – pos kases sistēmā tiek parādītas uzvednes, kas ir iestatītas Pārdošanas **un mārketinga modulī**. Papildinformāciju skatiet pamatojuma [kodu iestatīšana](/dynamicsax-2012/appuser-itpro/set-up-return-reason-codes).
- **Krājumu vietas** - vietas, kur tiek glabāti krājumi. Papildinformāciju skatiet sadaļā [Krājumu vietu iestatīšana](/dynamicsax-2012/appuser-itpro/about-locations).
    
### <a name="set-up-return-locations"></a>Iestatīt atgriešanas vietas

Lai iestatītu atgriešanas vietas, sekojiet šiem soļiem.

1. Pārejiet uz **sadaļu Mazumtirdzniecības \> un \> Komercijas kanāla iestatīšanas** noliktavas un atlasiet noliktavu.
1. Kopsavilkuma cilnes **Mazumtirdzniecība** laukā Noklusējuma atgriešanas vieta atlasiet krājumu atrašanās vietu, **kas** jāizmanto atgriešanai, kur informācijas kodi vai iemeslu kodi nav kartēti uz atgriešanas vietām.
1. Laukā Noklusējuma **atgriešanas palete** atlasiet paleti atgriešanai, kuru informācijas kodi vai iemeslu kodi nav kartēti atgriešanas vietām.
1. Pārejiet uz sadaļu **Mazumtirdzniecības un Commerce \> Krājumu vadības \> atgriešanas vietas**.
1. Atlasiet **Jauns,** lai izveidotu atgriešanas vietas politiku.
1. Ievadiet unikālu atgriešanas vietas nosaukumu un aprakstu.

    > [!NOTE]
    > Ja numuru secība ir iestatīta atgriešanas vietām, nosaukums tiek ievadīts automātiski.

1. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju Drukāt etiķetes **uz** Jā **·**, lai drukātu visu preču etiķetes, kas piešķirtas atgriešanas vietām.
1. Iestatiet opciju **Bloķēt krājumus** uz Jā **,** lai atgrieztās preces noklusējuma atgriešanas vietā pārdotu ārpus noliktavas un neļautu tās pārdot.
1. Lai kartētu noteiktus mazumtirdzniecības infokodus un apakškodas atrašanās vietu atgriešanai, veiciet tālāk aprakstītās darbības.

    1. Kopsavilkuma cilnē **Mazumtirdzniecības infokodi** atlasiet **Pievienot**.
    1. Informācijas koda **laukā** atlasiet atgriešanas informācijas kodu.
    1. Laukā **Apakškods** atgriešanas iemeslam atlasiet apakškodu. **Laukā** Apraksts ir parādīts atlasītā apakškoda apraksts.
    1. Laukā **Veikals** atlasiet veikalu, kurā tiek izmantots informācijas kods.
    1. Lai norādītu **atgriešanas** vietu **·**, lietojiet laukus **Noliktava**, Novietojums un Paletes ID. Piemēram, lai norādītu atrašanās vietu veikalā, **laukā** Vieta atlasiet veikalu un atrašanās **vietu**.
    1. Atzīmējiet **izvēles rūtiņu Bloķēt** krājumus, lai atgrieztās preces neļautu pārdot.

1. Lai kartētu konkrētus pārdošanas un mārketinga iemeslu kodus atgriešanas vietām, veiciet tālāk aprakstītās darbības.

    1. Kopsavilkuma cilnē **Pārdošanas un mārketinga iemeslu** kodi atlasiet **Pievienot**.
    1. Laukā **Iemesla** kods atlasiet atgriešanas iemesla kodu. Apraksta **lauks** parāda atlasītā iemesla koda aprakstu.
    1. Laukā **Veikals** atlasiet veikalu, kur tiek izmantots šis pamatojuma kods.
    1. Lai norādītu **atgriešanas** vietu **·**, lietojiet laukus **Noliktava**, Novietojums un Paletes ID. Piemēram, lai noliktavā norādītu paleti, **laukā** Noliktava atlasiet noliktavu, **·** **vietu laukā Vieta un paleti laukā Paletes kods**.
    1. Atzīmējiet **izvēles rūtiņu Bloķēt** krājumus, lai atgrieztās preces neļautu pārdot.

    > [!NOTE]
    > Ja krājumam tiek izmantots atgriešanas vietas politika, bet atgriešanas iemesls, kādēļ kasieris atlasa neatbilst nevienam kodam, kas ir norādīts kopsavilkuma cilnē Mazumtirdzniecības **informācijas** **kodi vai Pārdošanas un mārketinga iemeslu kodi, prece tiek nosūtīta uz noklusējuma atgriešanas** vietu, **kas ir noteikta lapā** Noliktava. Turklāt atzīme izvēles **rūtiņā** **·** **Bloķēt** krājumus kopsavilkuma cilnē Vispārīgi atgriešanas novietojumu lapā nosaka, vai atgrieztā prece jābloķē.

1. Pārejiet uz **preču hierarhiju Retail un Commerce \> Commerce**.
1. Kopsavilkuma cilnes **Pārvaldīt krājumu kategoriju rekvizītus** laukā Atgriešanas **vieta** atlasiet atgriešanas vietu. Tā kā vienā veikalā var definēt vairākas atgriešanas vietu politikas, šeit atlasītā vērtība nosaka izmantoto atgriešanas vietas politiku.

## <a name="additional-resources"></a>Papildu resursi

[Sērijveida kontrolētu preču atdošana atpakaļ pārdošanas punktā (POS)](POS-serial-returns.md)

[Iepriekš apstiprinātu darījumu saistītās atmaksas](dev-itpro/linked-refunds.md)

[Izveidot un atjaunināt kanāla atgriešanas un atmaksas politiku](refund_policy_returns.md)

[POS lietotāja interfeisa vizuālās konfigurācijas](pos-screen-layouts.md)
