---
title: Mērķauditorijas atlase ierīcēs, tirgū un ģeogrāfiskā atrašanās vietā
description: Šajā rakstā ir aprakstīts, kā izveidot, rediģēt un pārvaldīt mērķauditorijas Microsoft Dynamics 365 Commerce un mērķus vietas veidotājā, izmantojot informāciju par ierīci, tirgu un ģeovietu.
author: sushma-rao
ms.date: 02/03/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2021-07-31
ms.dyn365.ops.version: AX 10.0.21
ms.openlocfilehash: 90772fd942db30bbf4f65a87b1dca4b2aaacee1e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881661"
---
# <a name="device-market-and-geolocation-targeting"></a>Mērķauditorijas atlase ierīcēs, tirgū un ģeogrāfiskā atrašanās vietā

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot, rediģēt un pārvaldīt mērķauditorijas Microsoft Dynamics 365 Commerce un mērķus vietas veidotājā, izmantojot informāciju par ierīci, tirgu un ģeovietu.

Dynamics 365 Commerce ļauj personalizēt jūsu lapas satura variācijas (pazīstamas kā *mērķi*) konkrētām klientu grupām (pazīstamas kā *auditorijas*), lai palīdzētu palielināt lietotāju iesaisti un apmierinātību. Vispirms varat izveidot auditoriju vai mērķi. Tomēr veiksmīgai mērķauditorijas atlases pieredzei ir nepieciešami abi šie komponenti.

Jūs izveidojat un pārvaldāt auditorijas Commerce vietņu veidotājā, pamatojoties uz klientu datiem, piemēram, atrašanās vietu, ierīces informāciju, pierakstīšanās statusu un citu dinamiski atvasinātu informāciju no klientu tīmekļa pieprasījumiem. Jūs arī izveidojat un pārvaldāt mērķus e-komercijas moduļiem un fragmentiem Commerce vietņu veidotājā.

**Saistību atruna**: jūs esat atbildīgs par šī līdzekļa izmantošanu saskaņā ar visiem piemērojamiem normatīvajiem aktiem, tostarp tiem, kas saistīti ar mērķauditorijas atlasi un profilēšanu. 

## <a name="audiences"></a>Auditorijas

Auditorija ir lietotāju grupa, un dalību grupā nosaka dinamisku kārtulu kopa. Šie noteikumi ir vienkārši loģiskie testi, kas tiek veikti, izmantojot informāciju, kas ir pieejama klientu pieprasījumos vai citos pieejamos segmentos. Varat kombinēt vairākas kārtulas, izmantojot operatorus UN/VAI.

Commerce dabiski atbalsta pamata segmentus, piemēram, ierīces informāciju, pierakstīšanās statusu, atsauces dokumentu un vaicājumu virknes parametrus. Tas atbalsta arī paplašināmus segmentus, izmantojot savienojumus ar trešo pušu pakalpojumu sniedzējiem.

### <a name="basic-segments"></a>Pamata segmenti

Pēc noklusējuma ir pieejami šādi segmenti, kurus var iekļaut auditorijas definīcijās:

- **Pierakstījies statuss** – pārbaudiet, vai lietotājs ir autentificēts.
- **Ierīces platforma** - Pārbaudiet šādus ierīču tipus:

    - Mobilā ierīce
    - Dators
    - Planšetdators
    - Cita

- **Ierīces operētājsistēma** - pārbaudiet šādas operētājsistēmas:

    - Windows
    - Linux
    - iOS
    - Android, cits

- **Vaicājuma virknes parametri** — pieprasījuma URL vaicājuma virknes parametra atslēgas vērtību pāra esamības pārbaude. Piemēram, vietrādim URL `www.fabrikam.com/en-us/request?promo=true` var ierakstīt kārtulu, lai pārbaudītu, vai **reklāmas** parametram ir vērtība **patiess**.
- **Sīkfails** — pārbaudiet sīkfaila vērtību, kas ir iestatīta domēnam pieprasījuma vietrādī URL. Piemēram, Fabrikam.com pieprasījumā var būt iekļauts sīkfails ar nosaukumu **CustomLayout** un vērtību **1**. Sīkdatņu pārbaude pārbauda sīkfaila esamību, bet to skaidri neizveido. Iepriekšējā piemērā JavaScript iepriekš ir iestatījis **CustomLayout** sīkfailu no cita moduļa vai kāda cita biznesa procesa.

    > [!NOTE]
    > Pārliecinieties, ka jūsu sīkdatņu izmantošana atbilst piemērojamajiem tiesību aktiem.

- **Atsauces avots** — ja lietotājs seko saitei, lai pieprasītu lapu, atsauces avots ir tās lapas URL, kurā tika viesota saite.

### <a name="extensible-segments"></a>Paplašināmie segmenti

Commerce ļauj paplašināt pieejamo segmentu sarakstu, izveidojot savienojumu ar trešo pušu segmentācijas pakalpojumu sniedzējiem. Segmentācijas nodrošinātājs apraksta pieejamo segmentu tipus. Papildinformāciju par to, kā izveidot savienojumu ar ģeolokācijas vai segmentācijas nodrošinātāju, skatiet rakstā [Savienotāju konfigurēšana un iespējošana](e-commerce-extensibility/connectors.md).

> [!NOTE]
> - Ja ārējais pakalpojumu sniedzējs ir iespējots, tas var izveidot savienojumu ar pakalpojumu, kuram ir neprognozējama veiktspēja. Lai palīdzētu nodrošināt labāku lietotāja pieredzi, ja lietotājs pieprasa lapu, kurā ir mērķauditorijas atlase, un šī lapa atsaucas uz auditoriju, kas pārbauda trešās puses segmenta nodrošinātāju, tiek parādīta lapas noklusējuma versija.
> - Lietotājam ir jāpiekrīt sīkdatņu izmantošanai. Pēc tam lietotāja pārlūkprogramma pieprasa visus segmentus no attiecīgajiem pakalpojumu sniedzējiem, un rezultāti tiek ievietoti sīkdatnē, kas tiek atgriezta lietotājam. Turpmākie lapas pieprasījumi izmantos šo informāciju, lai lietotājam nodrošinātu mērķtiecīgu saturu. Papildinformāciju par atbilstību sīkdatnēm skatiet sadaļā [Atbilstība sīkdatnēm](cookie-compliance.md).

**Saistību atruna:** ja iespējosiet šo līdzekli, jūsu dati tiks kopīgoti ar jūsu atlasītām trešo pušu sistēmām. Jūs kontrolējat, kādus datus, ja tādi ir, jūs sniedzat trešajai pusei. Jūs saprotat, ka trešās puses datu apstrādes un atbilstības standarti var atšķirties no Microsoft Dynamics 365 Commerce. Jūsu konfidencialitāte ir svarīga korporācijai Microsoft. Lai uzzinātu vairāk, izlasiet mūsu [Paziņojumu par konfidencialitāti un sīkfailiem](https://privacy.microsoft.com/privacystatement).

### <a name="create-an-audience-in-site-builder"></a>Auditorijas izveide vietņu veidotājā

Lai izveidotu jaunu fragmentu Commerce vietņu veidotājā, izpildiet tālāk norādītās darbības.

1. Kreisās puses navigācijas rūtī atlasiet **Auditorijas**.
1. Atlasiet **Jauns**.
1. Ievadiet auditorijas nosaukumu. Varat arī pēc izvēles pievienot atzīmes un aprakstu.
1. Atlasiet **Izveidot** un pēc tam **Pievienot jaunu kārtulu bloku**. Kārtulu bloks ir kārtulu kopums, kam pievienojas UN nosacījumi. Varat arī izveidot vairākus kārtulu blokus, kuru starpā ir nosacījumi VAI.
1. Atlasiet segmentu datu avotu un pēc tam norādiet segmenta nosaukumu, operatoru un vērtības. Kārtulu blokā var izveidot un dzēst papildu kārtulas vai arī izveidot un dzēst visus kārtulu blokus. Varat arī pārvietot kārtulu blokus uz augšu vai uz leju, kā nepieciešams.

    > [!NOTE]
    > Sarakstā var būt līdz 100 vērtībām, un katrā saraksta elementā var būt līdz 50 rakstzīmēm.

1. Kad esat apmierināts ar auditorijas konfigurāciju, atlasiet **Pabeigt rediģēšanu**. Pēc tam varat atlasīt **Publicēt**, lai auditorija būtu pieejama izmantošanai tiešraides mērķī. Varat arī publicēt auditoriju kopā ar mērķi. 

Lai rediģētu auditoriju, cilnē **Auditorijas** atlasiet hipersaiti un pēc tam parādītajā auditorijas redaktorā atlasiet **Rediģēt**. Lai skatītu mērķu un lapu sarakstu, kas atsaucas uz auditoriju, auditorijas saraksta skatā atlasiet auditoriju un pēc tam atlasiet **Skatīt piešķires**. Lai auditorijas saraksta skatā vai auditorijas redaktorā izdzēstu auditoriju, atsaistiet tās publicēšanu, ja tā jau ir publicēta, un pēc tam komandjoslā atlasiet **Dzēst**.

> [!NOTE]
> Auditorijas ir vietnes līmeņa koncepcija Commerce vietņu veidotājā. Varat kopīgot vienu un to pašu auditoriju vairākos mērķos.

### <a name="rename-an-audience-in-site-builder"></a>Mērķauditorijas pārdēvēšana vietu veidotājā

Lai pārdēvētu esošu mērķauditoriju Commerce Site Builder, sekojiet šiem soļiem.

1. Kreisās puses navigācijas rūtī atlasiet **Auditorijas**.
1. Atlasiet mērķauditorijas segmenta nosaukumu, ko vēlaties pārdēvēt.
1. Atlasiet **Labot,** lai sāktu mērķauditorijas rediģēšanu.
1. Mērķauditorijas rekvizītu rūtī atlasiet pie mērķauditorijas vārda savu zīmuli.
1. Pēc nepieciešamības rediģējiet mērķauditorijas nosaukumu.
1. Atzīmējiet izvēles rūtiņu, lai apstiprinātu nosaukuma maiņu.
1. Atlasiet **Beigt rediģēšanu**.

## <a name="targets"></a>Mērķi

Mērķis ir lietotāja pieredze, kas tiek rādīta vienas vai vairāku atlasīto auditoriju dalībniekiem. Tas var ietvert viena vai vairāku moduļu variācijas lapā vai fragmentā. 

Varat definēt mērķu grafiku, lai norādītu, cik ilgi tiem jāpaliek aktīviem. Ņemiet vērā, ka šī darbība ir atdalīta no publicēšanas grupas plānošanas darbības, kas nosaka, kad satura kolekcija tiks publicēta. Varat arī priekšskatīt savus mērķus, lai redzētu, kā tie izskatīsies atlasītās auditorijas dalībniekiem. Turklāt varat noteikt mērķu prioritātes, lai norādītu, kurš mērķis ir jārāda konflikta gadījumā.

### <a name="create-a-target"></a>Mērķa izveide

Lai izveidotu lapu moduļiem pamata čaulu Commerce vietņu veidotājā, sekojiet šiem soļiem.

1. Kreisās puses navigācijas rūtī atlasiet **Lapas**. Pēc tam atlasiet hipersaiti lapai, kurā ir moduļi, kurus vēlaties atlasīt.
1. Atlasiet **Rediģēt**, lai paņemtu lapu.
1. Izvēlnē **Mērķis** atlasiet **Jauns mērķis**, lai izveidotu jaunu mērķa čaulu. Pēc vajadzības lapā var izveidot vairākus mērķus.
1. Ievadiet mērķa nosaukumu un aprakstu un pēc tam atlasiet **Tālāk**.
1. Atlasiet **Pievienot**, lai iekļautu auditorijas, kas redzēs mērķa saturu, vai izslēgtu auditorijas. Pēc tam atlasiet **Jauns**.

    > [!NOTE]
    > Auditorijas piešķire nav obligāts solis mērķa izveides laikā. Tomēr pirms mērķa publicēšanas ir jāiekļauj vismaz viena auditorija, lai nodrošinātu, ka paredzētās lietotāju grupas redzēs mērķa saturu.

1. Definējiet mērķa rādīšanas laika logu, atlasot laika joslu, kā arī sākuma un beigu datumus un laikus. Mērķi var iestatīt tā, lai tas vienmēr būtu redzams loga laikā, vai arī varat atlasīt noteiktas dienas un laikus. Pēc pabeigšanas atlasiet **Tālāk**.

    > [!NOTE]
    > Norādītie laiki un laika josla ir globāli. Ja vēlaties atlasīt dažādas mērķa vietas dažādās vietās dažādos laikos vai dažādās laika joslās, ir jāizveido dažādi mērķi un jādefinē vēlamais grafiks katram novietojumam.

1. Pārskatiet detalizētu informāciju un, kad viss izskatās pareizi, atlasiet **Izveidot mērķa pieredzi** un pēc tam **Doties uz mērķi**. Mērķa čaula ir izveidots. Tagad varat tam pievienot moduļus.
1. Atlasiet moduli, uz kuru mērķēt, atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot pašreizējam mērķim**. Kad mērķē uz primāro moduli, visi tā atvasinātie elementi kļūst par šī mērķa daļu. Mērķorientētie moduļi ir izcelti zaļā krāsā.
1. Veiciet nepieciešamos satura atjauninājumus mērķa modulim un pēc vajadzības pievienojiet mērķim papildu moduļus. Atlasiet **Saglabāt**, lai saglabātu visas izmaiņas.
1. Pirms mērķa publicēšanas pārliecinieties, vai komandjoslā ir atlasīts **Priekšskatījums**, lai to pārskatītu. Varat atlasīt no vienu no šīm opcijām:

    - **Pamata priekšskatījums** — atlasiet šo opciju, lai priekšskatītu tikai atlasīto variantu (noklusējuma lapu vai mērķi) bez saistītām auditorijām.
    - **Detalizēts priekšskatījums** — atlasiet šo opciju, ja lapā ir vairāki mērķi un vēlaties tos priekšskatīt kā lietotāju, kas pieder atlasītajai auditoriju kopai, vai noteiktā datumā/laikā. Atlasiet **Tālāk**, lai atlasītu atbilstošo auditoriju sarakstā. Varat arī noņemt filtru, lai atlasītu starp visām auditorijām.

1. Kad esat apmierināts ar mērķa konfigurāciju, jums ir jāpublicē lapa, lai mērķis būtu tiešraidē. Atlasiet **Publicēt**, lai mērķis tūlīt nonāktu tiešraidē. Alternatīvi var lietot publicēšanas grupu, lai ieplānotu, kad lapa nonāk tiešraidē. Informāciju par publicēšanas grupām, skatiet sadaļā [Darbs ar publicēšanas grupām](publish-groups.md).

Jūs varat arī mērķēt uz fragmentiem. Procedūra ir līdzīga. Tomēr 1. solī navigācijas rūtī **Lapas** vietā atlasiet **Fragmenti**.

> [!NOTE]
> Lai izvairītos no jebkādas negatīvas ietekmes uz jūsu rādītājiem, lapā vai fragmentā var būt gan eksperiments, gan mērķi. Nevar būt gan eksperiments, gan mērķi.

### <a name="manage-targets"></a>Pārvaldīt mērķus

Lai rediģētu, dublētu vai dzēstu mērķus, dodieties uz noklusējuma lapu vai fragmentu un izpildiet šīs darbības.

1. Nolaižamajā izvēlnē atlasiet **Mērķis** un pēc tam atlasiet **Pārvaldīt mērķus**.
1. Atlasiet mērķi rediģēšanai, dublikātam vai dzēšanai.
1. Ja vienā modulī ir vairāki mērķi vai arī vairākiem mērķiem ir konfliktējoši grafiki, atlasiet **Sakārtot mērķus pēc prioritātes**, lai norādītu secību, kurā tos rādīt. Ja lapā vai fragmentā pievienojat vairāk nekā vienu mērķi, paziņojuma joslā tiek parādīta arī poga **Sakārtot mērķus pēc prioritātes**, lai atgādinātu par mērķu prioritāti. Ja nav norādīta prioritāte, jaunākais mērķis tiek atlasīts pēc noklusējuma.

### <a name="localize-targets"></a>Mērķu lokalizācija

Mērķi lapās un fragmentos tiek automātiski iekļauti, eksportējot un importot XLIFF failus lokalizācijas nolūkos. Tomēr, ja nav nepieciešama neviena atrašanās vietas informācija, to mērķus var dzēst pēc tam, kad ir importēti lokalizētie XLIFF faili.

> [!NOTE]
> Mērķi tiek pārvaldīti pa kanāliem un atrašanās vietām. Izmaiņas, ko veicat mērķos vienā kanālā vai darbības vietā, netiek automātiski pārnestas uz citiem kanāliem vai darbības vietām.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
