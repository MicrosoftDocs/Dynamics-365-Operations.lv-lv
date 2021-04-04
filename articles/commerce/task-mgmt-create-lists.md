---
title: Uzdevumu sarakstu izveidošana un uzdevumu pievienošana
description: Šī tēma aprakstīts, kā izveidot uzdevumu sarakstus un tiem pievienot uzdevumus programmā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 28bea16c3266115cf09aa80a364344789d60af7a
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477834"
---
# <a name="create-task-lists-and-add-tasks"></a>Uzdevumu sarakstu izveidošana un uzdevumu pievienošana

[!include [banner](includes/banner.md)]

Šī tēma aprakstīts, kā izveidot uzdevumu sarakstus un tiem pievienot uzdevumus programmā Microsoft Dynamics 365 Commerce.

*Uzdevums* definē noteiktu darba daļu vai darbību, ko kādam jāpabeidz noteiktā termiņā vai pirms tā. Programmā Dynamics 365 Commerce uzdevums var iekļaut detalizētas instrukcijas un informāciju par kontaktpersonu. Tas var ietvert arī saites uz fona darbībām, pārdošanas punktu (POS) operācijām vai vietnes lapām, lai palīdzētu uzlabot produktivitāti un nodrošinātu kontekstu, kas ir nepieciešams uzdevuma īpašniekam efektīvai uzdevuma pabeigšanai.

*Uzdevumu saraksts* ir uzdevumu apkopojums, kas ir jāpabeidz kā daļa no biznesa procesa. Piemēram, var būt uzdevumu saraksts, kas jaunajam darbiniekam ir jāizpilda pievienošanās laikā, uzdevumu saraksts kasieriem, kuri strādā vakara maiņas, vai uzdevumu saraksts, kas jāaizpilda, lai sagatavotu veikalu gaidāmai atvaļinājumu sezonai. Programmā Commerce katram uzdevumu sarakstam, kam ir mērķa datums, var piešķirt neierobežotu skaitu veikalu vai darbinieku, un var konfigurēt tā periodiskumu.

Gan vadītāji, gan darbinieki var izveidot uzdevumu sarakstus Commerce atbalsta birojā, un pēc tam piešķirt tos veikalu kopai.

## <a name="create-a-task-list"></a>Izveidot uzdevumu sarakstu

Lai izveidotu uzdevumu sarakstu, izpildiet šīs darbības.

1. Dodieties uz **Retail un Commerce \>Uzdevumu pārvaldība \>Uzdevumu pārvaldības administrēšana**.
1. Atlasiet **Jauns** un pēc tam ievadiet vērtības laukos **Nosaukums**, **Apraksts** un **Īpašnieks**.
1. Atlasiet **Saglabāt**.

## <a name="add-tasks-to-a-task-list"></a>Uzdevumu pievienošana uzdevumu sarakstam

Lai uzdevumu sarakstam pievienotu uzdevumus, veiciet šīs darbības.
 
1. Esoša uzdevuma kopsavilkuma cilnē **Uzdevumi** atlasiet **Jauns**, lai pievienotu uzdevumu.
1. Dialoglodziņā **Izveidot jaunu uzdevumu**, laukā **Nosaukums** ievadiet uzdevuma nosaukumu.
1. Laukā **Izpildes datuma nobīde no mērķa datuma** ievadiet pozitīvu vai negatīvu veselu skaitli. Piemēram, ievadiet **-2**, ja uzdevums jāpabeidz divas dienas pirms uzdevumu saraksta izpildes datuma.
1. Laukā **Piezīmes** Ievadiet detalizētus norādījumus.
1. Laukā **Kontaktpersona** ievadiet tēmas eksperta vārdu, ar kuru uzdevuma īpašnieks var sazināties, ja viņam ir nepieciešama palīdzība.
1. Laukā **Uzdevuma saite** ievadiet saiti, pamatojoties uz uzdevuma iedabu.

> [!TIP]
> Lai gan varat izmantot lauku **Piešķirts**, lai piešķirtu uzdevumus kādam, kamēr veidojat uzdevumu sarakstu, mēs iesakām izvairīties no uzdevumu piešķiršanas uzdevumu saraksta izveides laikā. Tā vietā piešķiriet uzdevumus pēc tam, kas atsevišķu veikalu sarakstam ir izveidota instance.

## <a name="use-task-links-to-help-improve-worker-productivity"></a>Izmantojiet uzdevumu saites, lai uzlabotu darbinieku produktivitāti

Commerce ļauj saistīt uzdevumus ar konkrētām POS operācijām, piemēram, palaižot pārdošanas pārskatu, apskatot tiešsaistes mācību videoklipu jaunai darbinieka orientācijai vai veicot darbību operāciju uzskaites daļā. Šis līdzeklis palīdz uzdevumu īpašniekiem iegūt informāciju, kas nepieciešama efektīvai uzdevuma izpildei.

Lai, veidojot uzdevumu, pievienotu uzdevumu saites, veiciet šīs darbības.

1. Esoša uzdevuma kopsavilkuma cilnē **Uzdevumi** atlasiet **Rediģēt**.
1. Dialoglodziņā **Rediģēt uzdevumu** laukā **Uzdevuma saite** atlasiet vienu vai vairākas no šīm opcijām:

    - Atlasiet **Izvēlnes elements**, lai konfigurētu operāciju uzskaites daļas darbību, piemēram "Preču komplekti."
    - Atlasiet **POS operācija**, lai konfigurētu POS operāciju, piemēram, "Pārdošanas pārskati."
    - Atlasiet **URL**, lai konfigurētu absolūto vietrādi URL.

Šajā ilustrācijā redzama uzdevumu saišu atlase dialoglodziņā **Rediģēt uzdevumu**.

![Uzdevumu saišu atlasīšana dialoglodziņā Rediģēt uzdevumu](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a>Konfigurējiet POS operāciju, lai to varētu saistīt ar uzdevumu

Lai konfigurētu POS operāciju, lai to varētu saistīt ar uzdevumu, veiciet šīs darbības.

1. Dodieties uz **Retail un Commerce \> Kanāla iestatīšana \> POS iestatīšana \> POS \> POS operācijas**.
1. Atlasiet **Rediģēt**, atrodiet POS operāciju un pēc tam atzīmējiet izvēles rūtiņu **Iespējot Task Management**.

## <a name="additional-resources"></a>Papildu resursi

[Uzdevumu pārvaldības pārskats](task-mgmt-overview.md)

[Uzdevumu pārvaldības konfigurēšana](task-mgmt-configure.md)

[Uzdevumu sarakstu piešķiršana veikaliem vai darbiniekiem](task-mgmt-assign-lists.md)

[Uzdevumu pārvaldība punktā POS](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
