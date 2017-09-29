---
title: "Pārvaldīt noliktavu darbiniekus"
description: "Šajā rakstā aprakstīts, kā izmantot programmatūru Dynamics 365 for Finance and Operations, lai palīdzētu kontrolēt un pārraudzīt darbu, ko darbinieki veic jūsu noliktavās."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: 52753c21862a2955e15140bb1cdb5ef6f6efe31a
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017

---

# <a name="manage-warehouse-workers"></a>Pārvaldīt noliktavu darbiniekus

[!include[banner](../includes/banner.md)]


Šajā rakstā aprakstīts, kā izmantot programmatūru Microsoft Dynamics 365 for Finance and Operations, izdevumu Enterprise, lai palīdzētu kontrolēt un pārraudzīt darbu, ko darbinieki veic jūsu noliktavās.

Ja jūs izmantojat funkcionalitāti Noliktavas pārvaldībā, visas noliktavas darbinieka operācijas tiek sauktas par *darbu*. Tāds darbs kā rīcībā esošo krājumu izdošana, pārvietošana un uzskaite tiek reģistrēts, izmantojot mobilās ierīces. Pirms noliktavas darbinieks var veikt darbu, viņam ir jābūt saistītam ar darbinieku Personāla vadībā. Ar katru **Darbinieka** kontu var būt saistīti vairāki noliktavas darba lietotāji. Šie darba lietotāji var strādāt dažādās noliktavās un tiem var būt dažādi piekļuves līmeņi dažādām mobilās ierīces izvēlnēm. Noliktavas darba lietotājus var uzskatīt par vairākām pieteikšanām atlasītajam darbiniekam. Katram darba lietotājam ir noklusētā noliktava, un noteiktas darbplūsmas tiek atklātas caur izvēlnes elementiem, kas ir pieejami šī darba lietotājam. 

Lai izveidotu jaunu darba lietotāju lapā **Darbinieki** cilnē **Vispārējā** sadaļā **Noliktavas**, noklikšķiniet uz **Darbinieks**. Jānorāda lietotāja ID, lietotāja vārds, noklusētā noliktava un izvēlnes nosaukums. Šī izvēlne tiek ielādēta, kad lietotājs pierakstās noliktavas mobilo ierīču portālā un ļauj definēt, kuriem izvēlnes elementiem lietotājam ir piekļuve. 

Kā daļu no katra darba lietotāja iestatīšanas varat arī noteikt specifiskas procesa darbplūsmas. Piemēram, var izmantot lauku **Ir cikla inventarizācijas supervizors**, lai norādītu, vai lietotājs var apstrādāt korekcijas cikla inventarizācijas neatbilstībās inventarizācijas darbības laikā un vai šīs korekcijas ir vispirms jāpārskata citam lietotājam.

## <a name="defining-labor-standards"></a>Darbaspēka standartu definēšana
Lapa **Darbspēka standarti** ļauj definēt aprēķinu metodes, ko sistēma izmanto, lai aprēķinātu plānoto laiku, kas būs nepieciešams noteikta veida darbam. Šo definīciju var iestatīt vispārīgā līmenī vai noteiktā līmenī. Piemēram, varat noteikt laiku, kas būtu nepieciešamas, lai varētu apstrādāt pārdošanas pasūtījuma izdošanu par svara konkrētai vienības definīcijai, kad tiek izmantots specifisks izdošanas process. Tajā pašā laikā, rīcībā esošiem krājumiem, kas tiek izdoti izvietošanas darbībai, var reģistrēt laiku, pamatojoties uz citu aprēķina metodi. 

Lai iespējotu definētos darbaspēka standartus, ir jāatlasa opcija **Atļaut darbaspēka standartus** katrai noliktavai, kurā tiek izmantoti darbaspēka standarti.

## <a name="monitoring-and-controlling-warehouse-work"></a>Noliktavas darba uzraudzība un kontrole
Lapa **Viss darbs** ļauj jums pārraudzīt un uzturēt visu darbu, kas tiek plānots, notiek un ir pabeigts. No šīs lapas var atjaunināt dažādus procesus, piemēram, noliktavas darba lietotāju piešķires un darba prioritāti. Jūs varat arī apskatīt detalizētas ziņas, kas saistītas ar darba virsrakstu un darba rindām, lai izprastu paredzamos vai pabeigtus darba procesus. 

Ja iespējosit opciju **Darbaspēka standarti**, jūs varat redzēt aprēķināto plānoto darba laiku. Kad darbs ir apstrādāts, faktiskais laiks tiks rādīts arī katrai darba operācijai. Šādā veidā var salīdzināt paredzamā laika aprēķinus ar faktisko laiku. 

Turklāt varat izmantot plānoto laiku noteikumos, lai automātiski sadalītu darbu darba izveides laikā. Šādā veidā varat ielādēt bilances darbu, pamatojoties uz paredzamo laiku, lai pabeigtu uzdevumus. 

Laika, ko izmanto, lai apstrādātu darba vienumus, analīze var palīdzēt organizēt uzlabojumus noliktavas darbinieku efektivitātē. Lai palīdzētu veikt šo analīzi, ir pieejami šādi pārskati:

-   **Darbspēks pēc lietotāja** — šis pārskats parāda darbinieku darba ražīgumu, pamatojoties uz faktisko laiku, salīdzinot ar plānoto laiku.
-   **Darbaspēks pēc darba transakcijas veida** — varat izmantot šo pārskatu, lai izpētītu neefektivitāti konkrētos noliktavas procesos. Piemēram, jūs pamanāt, ka pārsūtīšanas pasūtījumu izdošanai šonedēļ ir vajadzīgs ilgāks laiks nekā iepriekšējās nedēļas. Pēc tam šo informāciju var izmantot turpmākai izmeklēšanai.




