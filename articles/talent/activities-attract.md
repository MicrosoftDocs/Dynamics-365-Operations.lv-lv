---
title: Aktivitāšu pievienošana darbā pieņemšanas procesam
description: Šajā tēma ir sniegta informācija par dažādajiem aktivitāšu veidiem, ko varat pievienot darbā pieņemšanas procesam Microsoft Dynamics 365 Talent - Attract.
author: hasrivas
manager: AnnBe
ms.date: 05/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ce8c0bd74a41b9857538b37d0875583d06e8c11d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461907"
---
# <a name="add-activities-to-a-hiring-process"></a>Aktivitāšu pievienošana darbā pieņemšanas procesam

[!include [banner](includes/banner.md)]

Programmā Microsoft Dynamics 365 Talent: Attract darbā pieņemšanas procesa ietvaros var pievienot aktivitātes. Aktivitātes var pievienot procesa veidnei vai tiešā veidā pievienot vakances darbā pieņemšanas procesam. Definējot vakanci, tiek atlasīta procesa veidne un šai vakancei tiek lietotas veidnē ietvertās aktivitātes. Ja netiek atlasīta veidne, tiek izmantota noklusējuma veidne. Vakances darbā pieņemšanas procesu var modificēt arī pēc veidnes lietošanas.

> [!NOTE] 
> Procesa veidnes ir pieejamas tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums. Papildinformāciju skatiet rakstā [Kura Microsoft Dynamics 365 Talent versija - Attract](./attract-comprehensive-hiring.md).

## <a name="prospect-activity"></a>Aktivitāte Potenciālais kandidāts

Aktivitāte Potenciālais kandidāts sniedz iespēju kontrolēt to, vai potenciālos kandidātus var pievienot vakancei. Pēc noklusējuma vakancei var pievienot potenciālos kandidātus. Lai izslēgtu aktivitāti Potenciālais kandidāts, iestatiet opcijas **Iespējot potenciālos kandidātus** vērtību **Izslēgts**. Kad ir ieslēgta aktivitāte Potenciālais kandidāts, par pieņemšanu darbā atbildīgie vadītāji var pievienot un skatīt potenciālos kandidātus un vakances sadaļā tiek rādīta cilne **Potenciālais kandidāts**.

> [!NOTE]
> Lai ļautu kandidātiem pievienot darbu no LinkedIn, opcija **Iespējot potenciālos kandidātus** ir jāiestata uz **Ieslēgts**.

## <a name="application-activity"></a>Aktivitāte Pieteikums

Aktivitāte Pieteikums ir obligāta darbā pieņemšanas procesa veidnes aktivitāte. Lai kandidātiem nosūtītu e-pasta ziņojumu, kad viņi iesniedz savu pieteikumu vai tiek pievienoti posmam Pieteikums, iestatiet opcijas **Sūtīt vēstuli kandidātam** vērtību **Ieslēgts**.

## <a name="interview-schedule-and-feedback-activity"></a>Aktivitāte Interviju plānošana un atsauksmes

Šī aktivitāte sastāv no trim komponentiem: Kandidāta pieejamības pieprasījums, Grafiks un Atsauksmes. Izmantojiet intervijas aktivitāti darba veidnē, ja vēlaties komponentus Kandidāta pieejamības pieprasījums, Grafiks un Atsauksme iekļaut procesā, nevis tos izmantot atsevišķi darbā pieņemšanas procesa ietvaros. Papildinformāciju skatiet rakstā [Interviju plānošana un atsauksmes](interview-scheduling-feedback.md).

## <a name="power-apps-activity"></a>Aktivitāte Power Apps

Aktivitāte Power Apps sniedz iespēju darbā pieņemšanas procesā iegult Microsoft Power Apps. Programma var būt obligāta visiem kandidātiem, tikai iekšējiem kandidātiem, tikai ārējiem kandidātiem vai nevienam kandidātam. Ja programma ir atzīmēta kā obligāta, tā ir jāizpilda, pirms var pāriet uz nākamo posmu. Lai lauks **JobApplicationStatus** tiktu uzskatīts par pabeigtu, tas jāiestata kā **Pabeigts**. Šis lauks atrodas elementā JobApplicationActivity, lai Power Apps programami šis lauks būtu jāatjaunina, pirms var pāriet uz nākamo posmu. Ja programma nav atzīmēta kā obligāta, šī aktivitāte ir izvēles darbība un uz nākamo posmu var pāriet pat tad, ja programma nav izpildīta.

Lai saglabātu aktivitāti Power Apps darbā pieņemšanas procesā, ir jāievada Power Apps ID. Lai uzzinātu Power Apps ID, pārejiet uz sadaļu [Power Apps](https://web.powerapps.com), atlasiet **Programmas** un pēc tam atlasiet **Detalizēta informācija**.

Pēc noklusējuma aktivitāte Power Apps ir pieejama par pieņemšanu darbā atbildīgajam vadītājam, personāla atlases darbiniekam un viņu pārstāvjiem. Ja atlasāt opciju **Atļaut pievienot dalībniekus šai aktivitātei** lietojumprogrammai, kas izmanto aktivitāti Power Apps, var pievienot papildu dalībniekus no darbā pieņemšanas grupas. Piemēram, organizācija var izveidot Power Apps programmu, kas ir tehnisko amatu kandidātu intervijām paredzētu jautājumu bibliotēka. Organizācija vēlas pieņemt darbā jaunu programmatūras izstrādātāju un ir pievienojusi amata Programmatūras izstrādātājs darbā pieņemšanas procesam aktivitāti Power Apps. Ja ir atlasīta opcija **Atļaut pievienot dalībniekus šai aktivitātei**, personāla atlases darbinieks vai par pieņemšanu darbā atbildīgais vadītājs, kas skata amata Programmatūras izstrādātājs kandidātu, var pievienot intervētājus aktivitātei Power Apps. Pēc tam šīs personas var skatīt programmu, kurā ir ietverti intervijas jautājumi.

> [!NOTE]
> Aktivitāte Power Apps ir pieejama tikai tad, ja ir pieejams visaptverošais darbā pieņemšanas papildinājums. Papildinformāciju skatiet rakstā [Kura Microsoft Dynamics 365 Talent versija - Attract](./attract-comprehensive-hiring.md).

## <a name="youtube-activity"></a>Aktivitāte YouTube

Aktivitāte YouTube sniedz iespēju darbā pieņemšanas procesa ietveros kopīgot YouTube video. Lai saglabātu aktivitāti YouTube darbā pieņemšanas procesā, ir jānorāda YouTube video vietrādis URL. Varat izvēlēties rādīt saturu **darbā pieņemšanas grupai**, **tikai iekšējiem kandidātiem**, **tikai ārējiem kandidātiem** vai **visiem kandidātiem**. Tāpat kā aktivitātes Power Apps gadījumā varat atļaut darbā pieņemšanas grupas dalībnieku pievienošanu aktivitātei. Ja izvēlaties rādīt saturu kandidātiem, videoklips tiek rādīts tikai kā kandidātu pieredzes daļa, bet ne darbā pieņemšanas procesa laikā.

> [!NOTE]
> Aktivitāte YouTube ir pieejama tikai tad, ja ir pieejams visaptverošais darbā pieņemšanas papildinājums. Papildinformāciju skatiet rakstā [Kura Microsoft Dynamics 365 Talent versija - Attract](./attract-comprehensive-hiring.md).

## <a name="web-content-activity"></a>Aktivitāte Tīmekļa saturs

Aktivitāte Tīmekļa saturs sniedz jums iespēju iegult darbā pieņemšanas procesā tiešsaistes saturu. Lai saglabātu aktivitāti Tīmekļa saturs darbā pieņemšanas procesā, ir jānorāda satura vietrādis URL. Varat izvēlēties rādīt saturu **darbā pieņemšanas grupai**, **tikai iekšējiem kandidātiem**, **tikai ārējiem kandidātiem** vai **visiem kandidātiem**. Tāpat kā aktivitātes Power Apps un YouTube gadījumā varat atļaut darbā pieņemšanas grupas dalībnieku pievienošanu aktivitātei. Ja izvēlaties rādīt saturu kandidātiem, tīmekļa saturs tiek rādīts tikai kā kandidātu pieredzes daļa, bet ne darbā pieņemšanas procesa laikā. Varat izvēlēties rādītā satura izmēru.

> [!NOTE]
> Aktivitāte Tīmekļa aktivitāte ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums Papildinformāciju skatiet rakstā [Kura Microsoft Dynamics 365 Talent versija - Attract](./attract-comprehensive-hiring.md).

## <a name="microsoft-forms-activity"></a>Aktivitāte Microsoft Forms

Aktivitāte Microsoft Forms sniedz jums iespēju iegult darbā pieņemšanas procesā aktivitāti Microsoft Forms. Microsoft Forms sniedz jums iespēju izveidot testus, aptaujas un balsojumus. Lai saglabātu aktivitāti Microsoft Forms darbā pieņemšanas procesā, ir jānorāda veidlapas vietrādis URL. Varat izvēlēties rādīt saturu **darbā pieņemšanas grupai**, **tikai iekšējiem kandidātiem**, **tikai ārējiem kandidātiem** vai **visiem kandidātiem**. Tāpat kā aktivitātes Power Apps, YouTube un tīmekļa satura gadījumā varat atļaut darbā pieņemšanas grupas dalībnieku pievienošanu aktivitātei. Ja izvēlaties rādīt saturu kandidātiem, veidlapa tiek rādīta tikai kā kandidātu pieredzes daļa, bet ne darbā pieņemšanas procesa laikā.

Autori var mainīt Microsoft Forms iestatījumus, lai atļautu savu aptauju vai testu izpildīt lietotājiem ārpus savas organizācijas. Šādā gadījumā lietotāji iesniedz atbildes anonīmi. Ja vēlaties redzēt, kas ir izpildījuši jūsu aptauju vai testu, varat pieprasīt, lai respondenti aptaujas vai testa ietvaros ievadītu savu vārdu.

> [!NOTE]
> Aktivitāte Microsoft Forms ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums. Papildinformāciju skatiet rakstā [Kura Microsoft Dynamics 365 Talent versija - Attract](./attract-comprehensive-hiring.md).

## <a name="offer-activity"></a>Piedāvājuma aktivitāte

Darbā pieņemšanas procesa veidnei ir nepieciešama piedāvājuma aktivitāte. Lai izmantotu integrēto piedāvājumu pārvaldības programmu, atlasiet opcijas **Palaist programmu Offer Management piedāvājuma sagatavošanai** iestatījumu **Ieslēgts**. Ja šis iestatījums ir izslēgts, kandidāts nav redzams piedāvājumu programmā, tādēļ kandidāta piedāvājuma aktivitātes atjauninājumi ir jāizseko manuāli. Lai noteiktu, vai par pieņemšanu darbā atbildīgie vadītāji var piedāvājumu programmā sagatavot kandidāta piedāvājumu, atlasiet opcijas **Par pieņemšanu darbā atbildīgie vadītāji var sagatavot piedāvājumu** iestatījumu **Ieslēgts**. Ja ar darbu ir saistītas vairākas pozīcijas, varat izlemt, vai vēlaties sagatavot vairākus piedāvājumus attiecībā pret tādu pašu pozīciju skaitu. Ja vēlaties atļaut tikai vienu piedāvājumu uz pozīciju katram darbam, izvēlieties opcijas **Atļaut pozīcijas izmantot atkārtoti darba ietvaros** iestatījumu **Izslēgts**.

> [!NOTE]
> Integrētā piedāvājumu pārvaldības programma ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums. Papildinformāciju skatiet rakstā [Kura Microsoft Dynamics 365 Talent versija - Attract](./attract-comprehensive-hiring.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]