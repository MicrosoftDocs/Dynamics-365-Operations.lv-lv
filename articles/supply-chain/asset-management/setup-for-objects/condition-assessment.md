---
title: Nosacījuma novērtējums
description: Šajā rakstā skaidrots, kā izveidot nosacījumu novērtēšanas veidni un reģistrāciju līdzeklim Pamatlīdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c43424a0955d7a046186e8a4120c050990df6060
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015061"
---
# <a name="condition-assessment"></a>Nosacījuma novērtējums

[!include [banner](../../includes/banner.md)]

 

Šajā rakstā skaidrots, kā izveidot nosacījumu novērtēšanas veidni un reģistrāciju līdzeklim Pamatlīdzekļu pārvaldībā. Nosacījumu novērtējumu veic regulāri, un primārais mērķis ir izveidot un uzturēt nosacījumu datus par līdzekļiem. Raugoties no profilaktiskās uzturēšanas perspektīvas, ir svarīgi pārraudzīt svarīgāko informāciju, piemēram, pašreizējo stāvokli un atlikušo mūža ilgumu. Turklāt, ja regulāri veicat nosacījumu novērtējumu, jūs varēsit pārraudzīt un salīdzināt iekārtu nosacījumus jūsu rūpnīcā.

Nosacījumu novērtējumu var izmantot, lai izmērītu un uzraudzītu daudzus jūsu iekārtu nosacījumus. Piemērs: jūs varētu mērīt jūsu mašīnu vibrācijas. Kad esat reģistrējis vibrācijas mērījumus Līdzekļu pārvaldībā par dažādu veidu iekārtām, varat meklēt jaunāko reģistrēto novērtējumu un skatīt vibrācijas mērījumus.

Nosacījumu novērtējums tiek veidots par līdzekļiem. Pirms veicat nosacījumu novērtēšanas procedūru, ir jāiestata nosacījumu novērtējuma veidne līdzekļa veidam. Veidņu izmantošanas nosacījumu novērtēšanai iemesls ir novērst izvairīties no nosacījumu datu variantiem par līdzīgiem līdzekļiem. Nosacījumu novērtējuma iestatīšanas un izmantošanas secība Līdzekļu pārvaldībā ir: vispirms iestatiet nepieciešamās nosacījumu novērtēšanas veidnes. Pēc tam saistiet veidnes ar līdzekļu veidiem veidlapā **Līdzekļu veidi**. Visbeidzot varat izveidot nosacījumu novērtēšanas reģistrācijas par līdzekli veidlapā **Līdzeklis**.

## <a name="create-a-condition-assessment-template"></a>Nosacījumu novērtējuma veidnes izveide

1. Atlasiet **Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļu veidi** > **Nosacījumu novērtējums**.
2. Atlasiet **Jauns**, lai izveidotu jaunu veidni.
3. Laukā **Veidne** ievadiet veidnes ID.
4. Laukā **Nosaukums** ievadiet veidnes nosaukumu.
5. Kopsavilkuma cilnē **Nosacījumu novērtējuma rindas** pievienojiet nosacījumu novērtējumam nepieciešamās rindas, tostarp atbilstošā nosacījumu veida un mērvienību atlasi.
6. Kopsavilkuma cilnē **Līdzekļu veidi** pievienojiet līdzekļu veidus, kuriem jāizmanto nosacījumu novērtējuma veidne.
7. Laukos **Rindas** un **Līdzekļu veidi**, kas atrodas grupā ekrāna augšdaļā **Detalizēta informācija**, redzēsit novērtēšanas rindu un līdzekļu veidu skaitu, kas saistīti ar atlasīto nosacījumu novērtējuma veidni.


## <a name="create-condition-assessment-registration-on-an-asset"></a>Nosacījumu novērtējuma reģistrācijas izveide līdzeklim

1. Atlasiet **Pamatlīdzekļu pārvaldības** > **līdzekļi** > **visi pamatlīdzekļi**.
2. Sarakstā atlasiet līdzekli, kuram vēlaties izveidot nosacījumu novērtējuma reģistrāciju.
3. Cilnē **Vispārīgie iestatījumi** noklikšķiniet uz **Nosacījumu novērtējums**.
4. Noklikšķiniet uz **Jauns**, lai veiktu jaunu reģistrāciju.
5. Laukā **Datums** atlasiet nosacījumu novērtējuma datumu.
6. Laukā **Darbinieks** atlasiet tā darbinieka vārdu, kurš veica novērtējuma reģistrāciju.
7. Laukā **Rindas** ir redzams nosacījumu novērtējumam iestatīto novērtējuma rindu skaitu.
8. Laukā **Veidne** atlasiet nosacījumu novērtējuma veidni. Veidnes nosaukums tiek automātiski ievietots laukā **Nosaukums**, un saistītās reģistrācijas rindas tiek ievietotas kopsavilkuma cilnē **Nosacījumu novērtējuma rindas**.
9. Kopsavilkuma cilnē **Piezīmes** var ievietot piezīmes, kas attiecas uz atlasīto nosacījumu novērtējumu.
10. Katrai nosacījumu novērtējuma rindai ievadiet mērījumu datus laukā **Vērtība.**
11. Varat ievietot komentāru, kas attiecas uz atlasīto reģistrācijas rindu kopsavilkuma cilnes **Nosacījumu novērtējuma rindas** laukā > **Komentāri**. Ja rindā pievienojat komentāru, automātiski tiek atlasīta izvēles rūtiņa **Komentārs**.

Kad esat veicis nosacījumu novērtējuma reģistrēšanu līdzeklim, varat izdrukāt nosacījumu novērtējuma atskaiti.

>[!NOTE]
>Darba pasūtījumā var arī reģistrēt nosacījumu novērtējumu (Pamatlīdzekļu **pārvaldības darba** > **pasūtījumi visi darba pasūtījumu** > **nosacījuma** > **novērtēšanas** poga.)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]