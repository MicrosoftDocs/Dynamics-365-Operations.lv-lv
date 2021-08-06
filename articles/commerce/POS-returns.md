---
title: Atpakaļ atdošanas izveide programmā POS
description: Šajā tēmā ir aprakstīts, kā uzsākt atpakaļ atdošanu darījumiem skaidrā naudā bez piegādes vai debitoru pasūtījumiem Microsoft Dynamics 365 Commerce Point of Sale (POS) programmā.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.20
ms.openlocfilehash: 53cad70e2c4866a18427157bc8b7fa1c3fda4daa
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638149"
---
# <a name="create-returns-in-pos"></a>Atpakaļ atdošanas izveide programmā POS

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā uzsākt atpakaļ atdošanu darījumiem skaidrā naudā bez piegādes vai debitoru pasūtījumiem Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) programmā.

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

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Iespējot pareizu nodokļu aprēķināšanu daļējai atgriešanai

Šis līdzeklis nodrošina, ka gadījumā, ja pasūtījums tiek atgriezts vairākus rēķinos, nodokļi beigās būs vienādi ar sākotnēji iekasēto nodokļu summu.
1.  Dodieties uz darbvietu **Līdzekļu pārvaldība** un meklējiet **Iespējot pareizu nodokļu aprēķināšanu daļējai atgriešanai**.
2.  Atlasiet **Iespējot pareizu nodokļu aprēķināšanu daļējai atgriešanai** un pēc tam noklikšķiniet uz **Iespējot**.


## <a name="additional-resources"></a>Papildu resursi

[Sērijveida kontrolētu preču atdošana atpakaļ pārdošanas punktā (POS)](POS-serial-returns.md)

[Iepriekš apstiprinātu darījumu saistītās atmaksas](dev-itpro/linked-refunds.md)

[Izveidot un atjaunināt kanāla atgriešanas un atmaksas politiku](refund_policy_returns.md)

[POS lietotāja interfeisa vizuālās konfigurācijas](pos-screen-layouts.md)
