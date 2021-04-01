---
title: Izveidot līdzekli
description: Šajā tēmā aprakstīts, kā izveidot līdzekli Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTableCopyStructure, EntAssetObjectTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a01c1fd72b96bd6ff5e6c76e659394e17060c681
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253402"
---
# <a name="create-an-asset"></a>Izveidot līdzekli

[!include [banner](../../includes/banner.md)]

 

Šajā tēmā aprakstīts, kā izveidot līdzekli Līdzekļu pārvaldībā.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopīgie** > **līdzekļi** > **Visi līdzekļi** vai **Aktīvie līdzekļi**.
2. Noklikšķiniet uz pogas **Jauns**.
3. Dialoglodziņā **Izveidot līdzekļus** ievadiet datus par **Līdzekli** (līdzekļa ID) un līdzekļa nosaukumu. Laukā **Ir spēkā** atlasiet līdzekļa datumu un laiku. Sākot ar šo datumu, varat uzstādīt līdzekli funkcionālā novietojumā, kā arī pārvietot un aizstāt līdzekli līdzekļu struktūrā.
4. Laukā **Līdzekļa veids** atlasiet līdzeklim līdzekļa veidu (obligāts lauks). Ja nepieciešams, atlasiet līdzeklim **Līdzekļa ražotājs** un **Līdzekļa modelis**. Ja ir iestatīta tikai viena prece, šī prece tiek automātiski atlasīta laukā **Līdzekļa ražotājs**. Atlases, kas pieejamas laukos **Līdzekļa ražotājs** un **Līdzekļa modelis**, ir atkarīgas no iestatījuma [Līdzekļu ražotāji un modeļi](../setup-for-objects/product-and-model.md).
5. Grupā **Primārais līdzeklis** lauks **Līdzeklis** pēc noklusējuma ir tukšs. Ja nepieciešams, varat atlasīt primāro līdzekli, un pēc tam visi lauki grupā **Primārais līdzeklis** tiks aizpildīti automātiski.
    >[!NOTE]  
    >Kad atlasāt primāro līdzekli, ir pieejamas divas vai trīs cilnes: cilnē **Mani līdzekļi** ir ietverti līdzekļi, kas ir saistīti ar funkcionālajiem novietojumiem, kam jūs (uzturēšanas darbinieks, kurš ir pieteicies sistēmā) var piešķirt. Ja funkcionālie novietojumi ir iestatīti uzturēšanas darbiniekam veidlapā [Uzturēšanas darbinieki un darbinieku grupas](../setup-for-objects/workers-and-worker-groups.md), cilne **Mani līdzekļi** nebūs redzama. Cilnē **Aktīvie līdzekļī** ir iekļauts visu līdzekļu saraksts ar līdzekļa dzīves cikla statusu "Aktīvs". Cilne **Līdzekļu skats** parāda funkcionālo novietojumu koku un šajos novietojumos uzstādītos līdzekļus.

6. Noklusējuma funkcionālais novietojums, ko esat iestatījis, līdzeklim tiek ieteikts grupas **Līdzeklis** laukā **Funkcionālais novietojums**. Ja nepieciešams, atlasiet citu funkcionālo novietojumu.

    >[!NOTE]
    >Kad esat izveidojis līdzekli, vajadzības gadījumā varat to uzstādīt citā funkcionālajā novietojumā. Funkcionālā novietojumā var uzstādīt tikai augšējā līmeņa līdzekļus (līdzekļus, kam pašlaik nav primārā līdzekļa). Tas nozīmē, ka uzstādāt augšējo līmeni, kā arī pakārtotos līdzekļus atlasītajā funkcionālajā novietojumā. Lasiet vairāk par līdzekļu uzstādīšanu funkcionālajos novietojumos sadaļā [Ievads par funkcionālajiem novietojumiem](../functional-locations/introduction-to-functional-locations.md).

7. Noklikšķiniet uz **Labi**.
8. Atlasiet līdzekli sarakstā **Visi līdzekļi** un noklikšķiniet uz pogas **Rediģēt**, lai pievienotu līdzeklim papildu informāciju.

## <a name="general-information"></a>Vispārīga informācija

Funkcionālais novietojums, ar kuru līdzeklis ir saistīts, ir parādīts laukā **Funkcionālais novietojums**. Ja līdzeklis ir primārais pamatlīdzeklis, ar līdzekli saistīto apakšelementu skaits ir parādīts laukā **Apakšelementi**. Ja līdzeklis ir apakšlīdzeklis esošam līdzeklim, primārā līdzekļa ID ir parādīts laukā **Primārais**.

Varat rediģēt **Līdzekļa ražotāja** un **Līdzekļu modeļa** informāciju par līdzekli, ko izmanto rezerves daļu, alternatīvo rezerves daļu un darba veidu noklusējumu pārvaldīšanai. Plašāku informāciju skatiet sadaļā [Līdzekļu ražotāji un modeļi](../setup-for-objects/product-and-model.md). Ja nepieciešams, varat arī pievienot informāciju par **Modeļa gadu** un **Sērijas numuru**.

**Pašreizējais dzīves cikla stāvoklis** tiek izmantots, lai definētu, vai līdzeklis ir aktīvs vai neaktīvs. Veidojot līdzekli, posms vienmēr tiek iestatīts uz līdzekļa posmu grupas pirmo posmu. Kad esat gatavs aktivizēt līdzekli, noklikšķiniet uz **Atjaunināt līdzekļa stāvokli** un atlasiet dzīves cikla stāvokli, kuru esat definējis kā "līdzeklis aktīvs", un noklikšķiniet uz **Labi**.

**Piezīme:** ja līdzeklis ir iestatīts uz "neaktīvs", līdzeklim vairs nav iespējams izveidot darba pasūtījumus. Tāpat nevarat ieplānot preventīvās uzturēšanas darbus neaktīvam līdzeklim.

Lauki **Pakalpojumu līmenis** un **Kritiskums** attiecas uz līdzeklim izveidotajiem darba pasūtījumiem. Šie lauki parāda **Pakalpojumu līmeņa** un **Kritiskuma** skaitļus, kas aprēķināti līdzekļa pašreizējam iestatījumam. Skatiet sadaļu [Līdzekļa pakalpojumu līmeņi](../setup-for-objects/object-priorities.md) un [Līdzekļa kritiskuma veidi](../setup-for-objects/object-criticalities.md) par šo vērtību iestatīšanu.

## <a name="asset"></a>Līdzeklis

Līdzeklim varat atlasīt **Resursu**. Resursa atlase nosaka, kurš kalendārs tiek izmantots darba pasūtījuma plānošanai. Resursu atlasi bieži izmanto pamatlīdzekļiem. Resursi un resursu grupas ir iestatīti **Organizācijas administrācijā** > **Resursos** > **Resursu grupās** vai **Resursos**.

Laukā **Pamatlīdzekļu skaits** varat atlasīt pamatlīdzekli, kas ir saistīts ar līdzekli. Tas ir svarīgi, ja jūsu līdzeklis ir saistīts ar investīciju projektu.

- Ja līdzeklis ir saistīts ar pamatlīdzekli, varat izveidot darba pasūtījuma veidu, ko izmantot darba pasūtījumiem, kas saistīti ar investīciju projektu. 
- Informācija par līdzekļa pamatlīdzekļiem ir saistīta ar moduli **Pamatlīdzekļi** sadaļā Dynamics 365 Supply Chain Management. Tas nozīmē, ka **Pamatlīdzekļos** > **Pamatlīdzekļos** > **Pamatlīdzekļos** var iegūt pārskatu par Līdzekļu pārvaldības projektiem, kas var būt saistīti ar pamatlīdzekli, atlasot līdzekli sarakstā un skatot saturu rūts **Saistītā informācija** sadaļā > **Saistītie projekti**.


## <a name="details"></a>Detalizēta

Laukā **Aktīvs no** ir norādīts datums, kurā līdzekļa dzīves cikla stāvoklis tika atjaunināts uz aktīvu stāvokli (skatiet [Līdzekļa dzīves cikla stāvokļi](../setup-for-objects/object-stages.md) attiecībā uz līdzekļa dzīves cikla stāvokļa iestatīšanu). Ja līdzeklis vairs nav aktīvs un esat atjauninājis līdzekļa dzīves cikla stāvokli uz neaktīvu dzīves cikla stāvokli, datums, no kura līdzeklis ir neaktīvs, ir parādīts laukā **Aktīvs līdz**. Ja vajadzīgs, varat manuāli mainīt šos datumus.

Ja nepieciešams, laukā **Aizstāšanas datums** varat ievadīt paredzamo līdzekļa nomaiņas datumu. Līdzekļa aizstāšanas paredzamo vērtību var ievietot laukā **Aizstāšanas vērtība**. Piemērs: informāciju par aizstāšanu var izmantot, lai salīdzinātu to ar līdzekļa uzturēšanas izmaksām, un pēc tam pieņemt lēmumu par jauna īdzekļa iegādi, ja strauji pieaug uzturēšanas izmaksas par esošo līdzekli.

## <a name="notes"></a>Piezīmes

Kopsavilkuma cilnē **Piezīmes** varat pievienot piezīmes, kas attiecas uz šo līdzekli. Noklikšķiniet uz pogas **Pievienot**, pirms rakstāt piezīmi, ja vēlaties piezīmei pievienot lietotāja informāciju un datumu/laikspiedolu.

## <a name="attributes"></a>Atribūti

Šajā kopsavilkuma cilnē var iestatīt vērtības līdzekļa atribūtiem. Šos atribūtus var izmantot, lai aprakstītu līdzeklim atbilstošos rekvizītus vai raksturlielumus, piemēram, lielumu, svaru vai mašīnas konfigurāciju.

Noklikšķiniet uz **Pievienot rindu** un atlasiet atribūta veidu. Pēc tam ievietojiet ar atribūta veidu saistīto **Vērtību** un saglabājiet ierakstu.

>[!NOTE] 
>Varat iegūt pārskatu par līdzekļu atribūtu veidiem un to saistību ar līdzekļiem **Līdzekļu atribūtā** un **Līdzekļu atribūtu pārskatā**. Papildinformāciju skatiet sadaļā [Līdzekļu atribūtu pārskats](../objects/object-specification-overview.md).

## <a name="vendor"></a>Kreditors

Kopsavilkuma cilnē **Kreditors** atlasiet līdzekļa kreditora kontu. Arī, ja ir piešķirta kreditora garantija, šeit varat ievietot garantijas informāciju.

## <a name="address"></a>Adrese

Kopsavilkuma cilnē **Adrese** varat ievietot iekārtas adresi. Ja līdzeklim nav ievietota neviena adrese, līdzeklis izmanto primārā līdzekļa adresi, ja primārajam līdzeklim ir adrese. Ja nav nevienas adreses, kas saistīta ar līdzekli vai primārajiem līdzekļiem līdzekļu hierarhijā, var izmantot tā funkcionālā novietojuma adresi, kurā līdzeklis ir uzstādīts. Ja šim funkcionālajam novietojumam nav ar to saistītas adreses, līdzeklim tiek izmantota primārā līdzekļa funkcionālā novietojuma adrese.

## <a name="asset-management-plans"></a>Līdzekļu pārvaldības plāni

Uzturēšanas plāni tiek izmantoti, plānojot līdzekļa profilaktiskās uzturēšanas darbus ar regulāriem intervāliem. Šajā kopsavilkuma cilnē varat iestatīt atlasītā līdzekļa uzturēšanas plāna rindas. Uzturēšanas ciklus var iestatīt dažādiem līdzekļiem, kuriem jums regulāri jāveic līdzīgs uzdevums. Cilnē **Funkcionālā novietojuma uzturēšanas plāni** ir redzami uzturēšanas plāni, kas saistīti ar funkcionālo novietojumu, kurā līdzeklis ir uzstādīts.

>[!NOTE]
>Ja izdzēšat uzturēšanas plāna rindu vai uzturēšanas ciklu, kas saistīts ar līdzekli **Visos līdzekļos**, automātiski tiek izdzēsti visi uzturēšanas grafiki ar statusu "Izveidots", kas ir izveidoti, pamatojoties uz šo uzturēšanas plānu vai uzturēšanas ciklu.

## <a name="functional-location-maintenance-plans"></a>Funkcionālā novietojuma uzturēšanas plāni

Šajā kopsavilkuma cilnē ir sniegts pārskats par uzturēšanas plāniem, kas saistīti ar funkcionālo novietojumu, kurā līdzeklis ir uzstādīts.

## <a name="maintenance-rounds"></a>Uzturēšanas cikli

Šajā kopsavilkuma cilnē varat pievienot vai noņemt ar līdzekli saistītos uzturēšanas ciklus.

## <a name="financial-dimensions"></a>Finanšu dimensijas

Līdzeklim varat atlasīt finanšu dimensijas.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]