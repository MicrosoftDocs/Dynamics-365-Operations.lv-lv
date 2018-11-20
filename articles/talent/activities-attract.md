---
title: "Aktivitātes procesa ietvaros"
description: "Šajā tēma ir sniegta informācija par dažādajiem aktivitāšu veidiem, ko var izmantot darbā pieņemšanas procesa ietvaros."
author: 
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: ccd9e2d0ff1f7fb6825c6823936b4013b3054f5d
ms.contentlocale: lv-lv
ms.lasthandoff: 10/22/2018

---

# <a name="activities-in-the-hiring-processes"></a>Aktivitātes darbā pieņemšanas procesa ietvaros

[!include[banner](../includes/banner.md)]

Darbā pieņemšanas procesam programmā Microsoft Dynamics 365 for Talent: Attract var pievienot aktivitātes. Aktivitātes var pievienot procesa veidnei vai tiešā veidā pievienot vakances darbā pieņemšanas procesam. Definējot vakanci, tiek atlasīta procesa veidne un šai vakancei tiek lietotas veidnē ietvertās aktivitātes. Ja netiek atlasīta veidne, tiek izmantota noklusējuma veidne. Vakances darbā pieņemšanas procesu var modificēt arī pēc veidnes lietošanas.

> [!NOTE] 
> Procesa veidnes ir pieejamas tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums.

## <a name="prospect-activity"></a>Aktivitāte Potenciālais kandidāts

Aktivitāte Potenciālais kandidāts sniedz iespēju kontrolēt to, vai potenciālos kandidātus var pievienot vakancei. Pēc noklusējuma vakancei var pievienot potenciālos kandidātus. Lai izslēgtu aktivitāti Potenciālais kandidāts, iestatiet opcijas **Iespējot potenciālos kandidātus** vērtību **Izslēgts**. Kad ir ieslēgta aktivitāte Potenciālais kandidāts, par pieņemšanu darbā atbildīgie vadītāji var pievienot un skatīt potenciālos kandidātus un vakances sadaļā tiek rādīta cilne **Potenciālais kandidāts**.

## <a name="application-activity"></a>Aktivitāte Pieteikums

Aktivitāte Pieteikums ir obligāta darbā pieņemšanas procesa veidnes aktivitāte. Lai kandidātiem nosūtītu e-pasta ziņojumu, kad viņi iesniedz savu pieteikumu vai tiek pievienoti posmam Pieteikums, iestatiet opcijas **Sūtīt vēstuli kandidātam** vērtību **Ieslēgts**.

## <a name="scheduler-activity"></a>Aktivitāte Plānotājs

Aktivitāte Plānotājs ir izvēles aktivitāte. Šī aktivitāte sastāv no diviem komponentiem: Kandidāta pieejamība un Grafiks. Komponents Kandidāta pieejamība sniedz jums iespēju izmantot e-pastu, lai pieprasītu kandidāta pieejamību. Komponents Grafiks sniedz iespēju ieplānot intervijas, saskaņojot grafiku ar kandidātu un darbā pieņemšanas grupu. Aktivitātes Plānotājs ietvaros var konfigurēt šādas opcijas: **Pieprasīt kandidāta pieejamību**, **Tiešsaistes sapulce** un **Sūtīt vēstuli kandidātam**.

- Lai sūtītu kandidātiem e-pasta ziņojumus un pieprasītu viņu pieejamību, iestatiet opcijas **Pieprasīt kandidāta pieejamību** vērtību **Ieslēgts**. Ja iestatāt šīs opcijas vērtību **Izslēgts**, šī darbība netiek rādīta vakances darbā pieņemšanas procesa ietvaros.
- Lai veiktu tiešsaistes straumēšanu vai konferences zvanu, izmantojot Skype darbam, iestatiet lauka **Tiešsaistes sapulce** vērtību **Skype darbam**. Pēc tam intervētājiem nosūtītajā intervijas sapulces pieprasījumā tiek ietverta pareizā saite **Pievienoties Skype sapulcei**.
- Lai sūtītu kandidātiem e-pasta ziņojumus un precizētu grafiku, iestatiet opcijas **Sūtīt vēstuli kandidātam** vērtību **Ieslēgts**. Ja iestatāt šīs opcijas vērtību **Izslēgts**, kandidāti saņem intervijas grafiku tikai pēc pierakstīšanās kandidātu portālā.

## <a name="feedback-activity"></a>Aktivitāte Atsauksmes

Aktivitāte Atsauksmes ir izvēles aktivitāte. Šī aktivitāte sniedz intervijas dalībniekiem iespēju ievadīt ieteikumus kandidātam. Viņi var arī ievadīt jebkādus komentārus ar atsauksmēm. Ja ieslēdzat opciju **Pārmantot atsauksmju dalībniekus no darbā pieņemšanas grupas**, personāla atlases darbinieks, par pieņemšanu darbā atbildīgais vadītājs un intervētāji tiek automātiski pievienoti aktivitātei Atsauksmes. Organizācijas var atļaut intervētajiem skatīt citu personu atsauksmes pirms savu atsauksmju iesniegšanas. Organizācijas var atļaut intervētājiem arī rediģēt savas atsauksmes pēc to iesniegšanas.

## <a name="interview-activity"></a>Aktivitāte Intervija

Aktivitāte Intervija ir izvēles aktivitāte. Šī aktivitāte sastāv no trim komponentiem: Kandidāta pieejamība, Grafiks un Atsauksmes. Komponents Kandidāta pieejamība sniedz jums iespēju izmantot e-pastu, lai pieprasītu kandidāta pieejamību. Komponents Grafiks sniedz iespēju ieplānot intervijas, saskaņojot grafiku ar kandidātu un darbā pieņemšanas grupu. Aktivitātes Plānotājs ietvaros var konfigurēt šādas opcijas: **Pieprasīt kandidāta pieejamību**, **Tiešsaistes sapulce** un **Sūtīt vēstuli kandidātam**.

- Lai sūtītu kandidātiem e-pasta ziņojumus un pieprasītu viņu pieejamību, iestatiet opcijas **Pieprasīt kandidāta pieejamību** vērtību **Ieslēgts**. Ja iestatāt šīs opcijas vērtību **Izslēgts**, šī darbība netiek rādīta vakances darbā pieņemšanas procesa ietvaros.
- Lai veiktu tiešsaistes straumēšanu vai konferences zvanu, izmantojot Skype darbam, iestatiet lauka **Tiešsaistes sapulce** vērtību **Skype darbam**. Pēc tam intervijas sapulces pieprasījumā tiek ietverta pareizā saite **Pievienoties Skype sapulcei**.
- Lai sūtītu kandidātiem e-pasta ziņojumus un precizētu grafiku, iestatiet opcijas **Sūtīt vēstuli kandidātam** vērtību **Ieslēgts**. Ja iestatāt šīs opcijas vērtību **Izslēgts**, kandidāti saņem intervijas grafiku tikai pēc pierakstīšanās kandidātu portālā.

Komponents Atsauksmes sniedz personām iespēju ievadīt ieteikumus kandidātam. Viņi var arī ievadīt jebkādus komentārus ar atsauksmēm. Ja ieslēdzat opciju **Pārmantot atsauksmju dalībniekus no darbā pieņemšanas grupas**, personāla atlases darbinieks, par pieņemšanu darbā atbildīgais vadītājs un intervētāji tiek automātiski pievienoti komponentam Atsauksmes. Organizācijas var atļaut intervētajiem skatīt citu personu atsauksmes pirms savu atsauksmju iesniegšanas. Organizācijas var atļaut intervētājiem arī rediģēt savas atsauksmes pēc to iesniegšanas.

## <a name="powerapps-activity"></a>Aktivitāte PowerApps

Aktivitāte PowerApps sniedz jums iespēju iegult darbā pieņemšanas procesā Microsoft PowerApps programmu. Programma var būt obligāta visiem kandidātiem, tikai iekšējiem kandidātiem, tikai ārējiem kandidātiem vai nevienam kandidātam. Ja programma ir atzīmēta kā obligāta, tā ir jāizpilda, pirms var pāriet uz nākamo posmu. Ja programma nav atzīmēta kā obligāta, šī aktivitāte ir izvēles darbība un uz nākamo posmu var pāriet pat tad, ja programma nav izpildīta.

Lai saglabātu aktivitāti PowerApps darbā pieņemšanas procesā, ir jāievada PowerApps ID. Lai uzzinātu PowerApps ID, pārejiet uz sadaļu [PowerApps](https://web.powerapps.com), atlasiet **Programmas** un pēc tam atlasiet **Detalizēta informācija**.

Ja atlasāt opciju **Atļaut pievienot dalībniekus šai aktivitātei**, lietojumprogrammai, kas izmanto aktivitāti PowerApps, var pievienot papildu dalībniekus. Piemēram, organizācija var izveidot PowerApps programmu, kas ir tehnisko amatu kandidātu intervijām paredzētu jautājumu bibliotēka. Organizācija vēlas pieņemt darbā jaunu programmatūras izstrādātāju un ir pievienojusi amata Programmatūras izstrādātājs darbā pieņemšanas procesam aktivitāti PowerApps. Ja ir atlasīta opcija **Atļaut pievienot dalībniekus šai aktivitātei**, personāla atlases darbinieks vai par pieņemšanu darbā atbildīgais vadītājs, kas skata amata Programmatūras izstrādātājs kandidātu, var pievienot personas aktivitātei PowerApps. Pēc tam šīs personas var skatīt programmu, kurā ir ietverti intervijas jautājumi.

> [!NOTE]
> Aktivitāte PowerApps ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums.

## <a name="youtube-activity"></a>Aktivitāte YouTube

Aktivitāte YouTube sniedz jums iespēju darbā pieņemšanas procesa ietveros kopīgot YouTube video. Lai saglabātu aktivitāti YouTube darbā pieņemšanas procesā, ir jānorāda YouTube video vietrādis URL. Tāpat kā aktivitātes PowerApps gadījumā varat atļaut dalībnieku pievienošanu aktivitātei. Ja atlasāt opciju **Rādīt tikai kandidātam**, video tiek rādīts tikai kandidātam pieejamā satura ietvaros. Tas netiek rādīts darbā pieņemšanas procesa ietvaros programmā Attract.

> [!NOTE]
> Aktivitāte YouTube ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums.

## <a name="web-content-activity"></a>Aktivitāte Tīmekļa saturs

Aktivitāte Tīmekļa saturs sniedz jums iespēju iegult darbā pieņemšanas procesā tiešsaistes saturu. Lai saglabātu aktivitāti Tīmekļa saturs darbā pieņemšanas procesā, ir jānorāda satura vietrādis URL. Tāpat kā aktivitāšu PowerApps un YouTube gadījumā varat atļaut dalībnieku pievienošanu aktivitātei. Ja atlasāt opciju **Rādīt tikai kandidātam**, saturs tiek rādīts tikai kandidātam pieejamā satura ietvaros. Tas netiek rādīts darbā pieņemšanas procesa ietvaros programmā Attract. Varat atlasīt rādītā satura izmēru.

> [!NOTE]
> Aktivitāte Tīmekļa aktivitāte ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums

## <a name="microsoft-forms-activity"></a>Aktivitāte Microsoft Forms

Aktivitāte Microsoft Forms sniedz jums iespēju iegult darbā pieņemšanas procesā Microsoft Forms veidlapu. Microsoft Forms sniedz jums iespēju izveidot testus, aptaujas un balsojumus. Lai saglabātu aktivitāti Microsoft Forms darbā pieņemšanas procesā, ir jānorāda veidlapas vietrādis URL. Tāpat kā aktivitāšu PowerApps un YouTube un Tīmekļa saturs gadījumā varat atļaut dalībnieku pievienošanu aktivitātei. Ja atlasāt opciju **Rādīt tikai kandidātam**, veidlapa tiek rādīta tikai kandidātam pieejamā satura ietvaros. Tas netiek rādīts darbā pieņemšanas procesa ietvaros programmā Attract.

Autori var mainīt Microsoft Forms iestatījumus, lai atļautu savu aptauju vai testu izpildīt lietotājiem ārpus savas organizācijas. Šādā gadījumā lietotāji iesniedz atbildes anonīmi. Ja vēlaties redzēt, kas ir izpildījuši jūsu aptauju vai testu, varat pieprasīt, lai respondenti aptaujas vai testa ietvaros ievadītu savu vārdu.

> [!NOTE]
> Aktivitāte Microsoft Forms ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums.

