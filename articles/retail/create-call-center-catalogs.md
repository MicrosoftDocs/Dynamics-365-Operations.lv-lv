---
title: Zvanu centra kataloga izveide
description: "Šajā rakstā ir sniegts zvanu centra kataloga izveides procesa apraksts."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 94ff6d74d4a11b3b04be6b69f85e778c3b45de92
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-call-center-catalog"></a>Zvanu centra kataloga izveide

[!include[banner](includes/banner.md)]


Šajā rakstā ir sniegts zvanu centra kataloga izveides procesa apraksts. 

Zvanu centrā preču katalogus var izmantot, lai identificētu preces, kuras vēlaties piedāvāt debitoriem. Zvanu centros parasti tiek izmantoti drukātie katalogi. Drukāta kataloga noformēšana un ražošana tiek veikta ārpus programmatūras Microsoft Dynamics 365 for Retail. Taču varat izveidot katalogu un saglabāt to digitālā formātā, izmantojot tās pašas veidlapas, ko lietojāt tiešsaistes mazumtirdzniecības katalogu iestatīšanai. Lai varētu izveidot katalogu, jāiestata preču klāsti un jāpiešķir tie zvanu centram. Pēc tam pievienojiet preces katalogam, atlasot preces no šiem preču klāstiem. Kad preces ir pievienotas katalogam un katalogs ir pabeigts, validējiet katalogu, lai verificētu datus. Pēc tam iesniedziet katalogu pārskatīšanai un apstiprināšanai. Kad katalogs ir apstiprināts, to var publicēt. Kad zvanu centra katalogs izveidots, kataloga publicēšanas brīdī varat izveidot kataloga datu momentuzņēmumu. Šī momentuzņēmumu funkcionalitāte ļauj piekļūt noteiktām kataloga versijām pat tad, ja katalogā vēlāk tiek veiktas izmaiņas un tas tiek atjaunināts. Zvanu centra katalogiem arī var iestatīt, lai tiktu iekļauti šādi izvēles līdzekļi.

-   **Avota kod** — kodi, kas tiek izmantoti, lai izsekotu debitora reakciju uz noteiktiem kataloga pasta sūtījumiem.
-   **Bezmaksas preces** — preces, kas ir iekļautas debitora pasūtījumā bez papildu maksas. Šīs preces tiek automātiski pievienotas pasūtījumam, ja pasūtījumā ir ievadīts kataloga avota kods.
-   **Skripti** — teksti, kurus zvanu centra darbinieks nolasa debitoram, kad tiek izveidots pārdošanas pasūtījums. Skriptos var iekļaut sveicienus vai ieteikumus pirkumu veikšanai.
-   **Papildu pārdošanas vai šķērspārdošanas krājumi** — krājumi, kas tiek parādīti, kad pasūtījumam tiek pievienota konkrēta prece.

Šīs opcijas jāiestata pirms kataloga apstiprināšanas un publicēšanas.

## <a name="prerequisites"></a>Priekšnosacījumi
Pirms darba sākšanas izpildiet tālāk minētos uzdevumus.

-   Iestatiet preces un preču klāstu.
-   Iestatiet mazumtirdzniecības preces.
-   Iestatiet preču klāstu.
-   Izveidojiet zvanu centru.
-   Iestatiet zvanu centru.
-   Pievienojiet zvanu centru organizācijas hierarhijai.
-   Izveidojiet vai pārveidojiet organizācijas hierarhiju.

## <a name="create-a-catalog"></a>Kataloga izveidošana
Vispirms ir jāizveido katalogs, jāpievieno katalogam preces un pēc tam jāpārskata un jāatjaunina preču atribūti.

## <a name="validate-the-catalog"></a>Kataloga validēšana
Kad katalogs iestatīts, jums tas jāvalidē. Validēšanas process pārbauda, vai kanāla īpašībām un preču īpašībām nepieciešamie dati ir pilnīgi un derīgi, kā arī tiek pārbaudīts, vai katalogu var publicēt.

## <a name="submit-the-catalog-for-review-and-approval"></a>Kataloga iesniegšana tā pārskatīšanai un apstiprināšanai
Kad katalogs ir pārbaudīts, jūs varat iesniegt katalogu pārskatīšanai un apstiprināšanai. Katalogs vispirms jāapstiprina, un tikai tad to var publicēt. Darbplūsmu var konfigurēt tā, lai katalogi vai nu tiktu apstiprināti automātiski, vai arī tiem būtu nepieciešama manuāla apstiprināšana.

## <a name="optional-add-source-codes-free-products-and-scripts"></a>Pēc izvēles: avota kodu, bezmaksas preču un skriptu pievienošana
Zvanu centra katalogam var pievienot arī šādus vienumus. Šīs vienumi nav obligāti.

-   **Avota kodus** var izmantot uzņēmumi, kas nodrošina drukātos katalogus, lai izsekotu debitora reakciju uz noteiktiem katalogiem. Avotu kodi bieži tiek uzdrukāti kataloga aizmugurē un tiek ievadīti pārdošanas pasūtījumā, kad debitors veic pirkumu. Lai katalogam pievienotu avota kodu, vispirms ir jāizveido mērķa tirgus. Mērķa tirgus parasti ir kartēts uz īpašumā esošu vai nomātu adresātu sarakstu.
-   **Bezmaksas preces** ir reklāmas vienumi, kas iekļauti bez maksas debitora pasūtījumā, kad tiek norādīta atsauce uz katalogu.
-   **Skriptus** var izmantot, lai vadītu darbinieka mijiedarbību ar klientiem kataloga vai preču kontekstā kataloga ietvaros.

## <a name="publish-the-catalog"></a>Kataloga publicēšana
Publicējot zvanu centra katalogu, katalogā tiek noformēta informācija par preci. Publicēšana norāda arī, ka katalogs ir sagatavots papildu darbībām, kuras vēlaties veikt. Piemēram, varat izveidot drukāto katalogu. Katalogus var publicēt manuāli, vai arī varat veikt pakešveida apstrādi, lai tos publicētu saskaņā ar grafiku. Pirms publicējat katalogu, katalogs ir jāpārbauda un jāapstiprina. Lai pēc kataloga publicēšanas veiktu tajā izmaiņas, varat izņemt katalogu un pēc tam publicēt to atkārtoti.




