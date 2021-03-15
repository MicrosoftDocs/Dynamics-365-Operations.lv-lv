---
title: Nosacījumu novērtējums
description: Šajā tēmā ir paskaidrots, kā izveidot nosacījuma novērtējuma veidni un reģistrēt līdzekli Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 18be786e6f78829f61db1521a923e229fc4f0e70
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021119"
---
# <a name="condition-assessment"></a>Nosacījumu novērtējums

[!include [banner](../../includes/banner.md)]

 

Šajā tēmā ir paskaidrots, kā izveidot nosacījuma novērtējuma veidni un reģistrēt līdzekli Līdzekļu pārvaldībā. Nosacījumu novērtējumu veic regulāri, un primārais mērķis ir izveidot un uzturēt nosacījumu datus par līdzekļiem. Raugoties no profilaktiskās uzturēšanas perspektīvas, ir svarīgi pārraudzīt svarīgāko informāciju, piemēram, pašreizējo stāvokli un atlikušo mūža ilgumu. Turklāt, ja regulāri veicat nosacījumu novērtējumu, jūs varēsit pārraudzīt un salīdzināt iekārtu nosacījumus jūsu rūpnīcā.

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

1. Atlasiet **Līdzekļu pārvaldība** > **Kopīgi** > **Līdzekļi** > **Visi līdzekļi**.
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
>Varat arī reģistrēt nosacījumu novērtējumu darba pasūtījumā (**Līdzekļu pārvaldība** > **Kopīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** > **Nosacījumu novērtējuma** poga.)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]