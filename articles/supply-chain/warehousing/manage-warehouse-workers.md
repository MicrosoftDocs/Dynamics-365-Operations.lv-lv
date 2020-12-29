---
title: Noliktavā nodarbināto pārvaldība
description: Šajā rakstā ir aprakstīts, kā varat izmantot noliktavas lietotni, lai palīdzētu kontrolēt un uzraudzīt noliktavu darbinieku veikto darbu.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage, WHSResetUserPassword
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2156b5de6abc3751cae1822b3825acbbd0b9a712
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433095"
---
# <a name="manage-warehouse-workers"></a>Noliktavā nodarbināto pārvaldība

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā varat izmantot noliktavas lietotni, lai palīdzētu kontrolēt un uzraudzīt noliktavu darbinieku veikto darbu.

Ja jūs izmantojat funkcionalitāti Noliktavas pārvaldībā, visas noliktavas darbinieku operācijas tiek sauktas par *darbu*. Tāds darbs kā rīcībā esošo krājumu izsniegšana, pārvietošana un uzskaite tiek reģistrēts, izmantojot mobilās ierīces. Pirms noliktavas darbinieks var veikt darbu, viņam ir jābūt saistītam ar darbinieku Personāla vadībā. Ar katru **Darbinieka** kontu var būt saistīti vairāki noliktavas darba lietotāji. Šie darba lietotāji var strādāt dažādās noliktavās, un tiem var būt atšķirīgi piekļuves līmeņi dažādām mobilās ierīces izvēlnēm. Noliktavas darba lietotājus var uzskatīt par vairākām pieteikšanām atlasītajam darbiniekam. Katram darba lietotājam ir noklusētā noliktava, un noteiktas darbplūsmas tiek atklātas caur izvēlnes elementiem, kas ir pieejami šī darba lietotājam. 

Lai izveidotu jaunu darba lietotāju lapā **Darbinieki** cilnē **Vispārējā** sadaļā **Noliktavas**, noklikšķiniet uz **Darbinieks**. Jānorāda lietotāja ID, lietotāja vārds, noklusējuma noliktava un izvēlnes nosaukums. Šī izvēlne tiek ielādēta, kad lietotājs pierakstās noliktavas mobilo ierīču portālā un ļauj definēt, kuriem izvēlnes elementiem lietotājam ir piekļuve. 

Kā daļu no katra darba lietotāja iestatīšanas varat arī noteikt specifiskas procesa darbplūsmas. Piemēram, var izmantot lauku **Ir cikla inventarizācijas uzraugs**, lai norādītu, vai lietotājs var apstrādāt cikla inventarizācijas neatbilstību korekcijas inventarizācijas darbības laikā un vai šīs korekcijas ir vispirms jāpārskata citam lietotājam.

## <a name="defining-labor-standards"></a>Darbaspēka standartu definēšana
Lapa **Darbspēka standarti** ļauj definēt aprēķinu metodes, ko sistēma izmanto, lai aprēķinātu plānoto laiku, kas būs nepieciešams noteikta veida darbam. Šo definīciju var iestatīt vispārīgā vai noteiktā līmenī. Piemēram, varat noteikt laiku, kas būtu nepieciešamas, lai varētu apstrādāt pārdošanas pasūtījuma izdošanu par svaru konkrētai vienības definīcijai, kad tiek izmantots specifisks izsniegšanas process. Tajā pašā laikā var reģistrēt laiku rīcībā esošiem krājumiem, kas tiek izdoti izvietošanas darbībai, pamatojoties uz citu aprēķina metodi. 

Lai iespējotu definētos darbaspēka standartus, ir jāatlasa opcija **Atļaut darbaspēka standartus** katrai noliktavai, kurā tiek izmantoti darbaspēka standarti.

## <a name="monitoring-and-controlling-warehouse-work"></a>Noliktavas darba uzraudzība un kontrole
Lapa **Visi darbi** ļauj jums pārraudzīt un uzturēt visu darbu, kas tiek plānots, notiek un ir pabeigts. No šīs lapas var atjaunināt dažādus procesus, piemēram, noliktavas darba lietotāju piešķires un darba prioritāti. Jūs varat arī apskatīt detalizētas ziņas, kas saistītas ar darba virsrakstu un darba rindām, lai izprastu paredzamos vai pabeigtus darba procesus. 

Ja iespējosit opciju **Darbaspēka standarti**, jūs varat redzēt aprēķināto plānoto darba laiku. Kad darbs ir apstrādāts, faktiskais laiks tiks rādīts arī katrai darba operācijai. Šādā veidā var salīdzināt paredzamā laika aprēķinus ar faktisko laiku. 

Turklāt varat izmantot plānoto laiku noteikumos, lai automātiski sadalītu darbu darba izveides laikā. Šādā veidā varat ielādēt bilances darbu, pamatojoties uz paredzamo laiku, lai pabeigtu uzdevumus. 

Darba vienumu apstrādei izmantotā laika analīze var palīdzēt organizēt uzlabojumus noliktavas darbinieku efektivitātē. Lai palīdzētu veikt šo analīzi, ir pieejami šādi pārskati:

-   **Darbspēks pēc lietotāja** — šis pārskats parāda darbinieku darba ražīgumu, pamatojoties uz faktisko laiku, salīdzinot ar plānoto laiku.
-   **Darbaspēks pēc darba transakcijas veida** — varat izmantot šo pārskatu, lai izpētītu neefektivitāti konkrētos noliktavas procesos. Piemēram, jūs pamanāt, ka pārsūtīšanas pasūtījumu izsniegšanai šonedēļ ir vajadzīgs ilgāks laiks nekā iepriekšējās nedēļas. Pēc tam šo informāciju var izmantot turpmākiem pētījumiem.




