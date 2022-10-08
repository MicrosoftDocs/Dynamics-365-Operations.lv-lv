---
title: Atkārtota pirkšanas pasūtījuma izveide
description: Šajā rakstā ir parādīts, kā izveidot atkārtotu pirkšanas pasūtījumu (PP), kopējot rindas no agrāka pirkšanas pasūtījuma dokumenta uz jaunu PP vai esošo PP.
author: GalynaFedorova
ms.date: 09/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 335461d60fa0bc92e9711806c6e42643a3f75d02
ms.sourcegitcommit: 073604c07116e0a87f78ab2c76cb89ae83ebba3c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608116"
---
# <a name="create-a-repeat-purchase-order"></a>Atkārtota pirkšanas pasūtījuma izveide

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir parādīts, kā izveidot atkārtotu pirkšanas pasūtījumu (PP), kopējot rindas no agrāka pirkšanas pasūtījuma dokumenta uz jaunu PP vai esošo PP. Atkārtotu pasūtījumu izveidošanai pastāv divas metodes. Varat izmantot darbības, kas no darbību rūts ir pieejamas dokumenta līmenī, vai varat izmantot rindas detaļu darbības. Dokumenta līmeņa darbības ir paredzētas jauna pirkšanas pasūtījuma izveidošanai, pievienojot rindas un virsraksta informāciju no cita pasūtījuma, bet rindas informācijas darbība galvenokārt ir paredzēta rindu pievienošanai esošajam pasūtījumam. Šajā ceļvedī rādīto piemēru var izmantot paraugdatu uzņēmumā USMF. Šo uzdevumu parasti veic pirkšanas aģents.

## <a name="create-a-new-repeat-purchase-order"></a>Izveidot jaunu atkārtotu pirkšanas pasūtījumu

1. Navigācijas rūtī dodieties uz Moduļiem Sagāde **\> un Pirkšanas pasūtījumu avotu visi \> pirkšanas \> pasūtījumi**. Vispirms mēs izmēģināsim opciju informācijas kopēšanai uz jaunu pasūtījumu.  
1. Atlasiet **Jauns**.
1. Laukā **Kreditora konts** ievadiet `US-101`.
1. Atlasiet **Labi**.
1. Darbību rūtī atveriet cilni Pirkšanas **pasūtījums** un no grupas **Kopēt** atlasiet **No visiem**. Tiek **atvērts dialogs Kopēt no** citiem dokumentiem. No šejienes var kopēt pasūtījumā no esošajiem pasūtījumiem. Veidam, kādā rindas tiek kopētas, pastāv dažādas opcijas, un pastāv dažādi dokumentu veidi, no kuriem varat kopēt. Vispirms mēs apskatīsim opcijas tam, kā rindas tiek kopētas.
1. Izvērsiet kopsavilkuma **cilni** Parametri.

    - Lauks **Daudzuma koeficients** ir noderīgs, ja vēlaties izmantot daudzumu, kas atšķiras no tā, kas ir pasūtījumā, no kura kopējat. Piemēram, ja vēlaties pasūtīt divreiz lielāku daudzumu, nekā norādīts rindās, no kurām kopējat, tad šajā laukā būtu jāievada '2', un pēc tam sistēma pievienotu rindas, kur sākotnējais daudzums ir dublēts.  
    - Lauks **Apgriešanas zīme** arī atbalsta pasūtītā daudzuma maiņu, mainot daudzuma zīmi pasūtījuma rindām, kas tiek pievienotas. Tas var būt noderīgi, ja ir nepieciešams atsaukt kādu transakciju, izveidojot pasūtījuma rindas, kuras anulē šo transakciju. Šī iespēja tiek atlasīta automātiski, kad lapa tiek atvērta no darbības **Izveidot kredītnotu**.  
    - Opcija **Kopēt maksas** ļauj kopēt maksas uz jauno pasūtījumu no dokumenta, no kura kopējat pasūtījuma rindas.  
    - Opcija **Pārrēķināt cenas** izmanto esošās cenas un atlaides, nevis kopē tās no dokumenta, no kura kopējat citu informāciju.  
    - Opcija **Kopēt precīzi** kopē vērtību vairākus laukus pasūtījuma galvā un rindās. Ja šī opcija nav atlasīta, noklusējuma vērtības tiks izmantotas daudziem laukiem, kas saistīti ar kreditoru un precēm, tieši tāpat kā izveidojot jaunu pasūtījumu manuāli. Piemēram, ja **·** *precīzi* iestatāt Kopēt uz Jā un kopējiet pasūtījumu, kas ignorē kreditora noklusēto rēķina kontu, tas pats rēķina konts tiks kopēts jaunajā pasūtījumā. Ja jūs iestatāt **Kopēt** precīzi *uz Nē*, noklusējuma rēķina konts kreditoram tiktu izmantots jaunajā pasūtījumā. Ja Kopēšana ir precīzi iestatīta uz Jā, šādu lauku **vērtības** tiek *kopētas*:
        - Valoda
        - Apmaksas nosacījumi
        - Maksāšanas metode
        - Maksājuma apraksts
        - Numuru sēriju grupa
        - Termiņatlaide
        - Atlaides procenti
        - Valūta
        - Piegādes nosacījumi
        - Piegādes veids
        - Dimensija
        - PVN grupa
        - Ignorēt PVN
        - Cenās iekļauts PVN
        - Transportēšana
        - Osta
        - Intrastat statistikas procedūra
        - Veidnes ID
        - Piegādes nosaukums
        - Pasta adrese
        - Atsauce
        - Atsauces tabulas ID
    - Opcija **Dzēst pirkuma rindas** ļauj dzēst visas pirkšanas pasūtījuma rindas, kas jau ir pirkšanas pieprasījumā, uz kuru kopējat, pirms piemērot jaunās rindas. Šī opcija ir jālieto uzmanīgi, jo tā dzēš visas pastāvošās rindas bez papildu brīdinājuma.  
    - Ja atlasāt opciju **Kopēt pasūtījuma galveni**, jaunajam pasūtījumam galvenes informācija nav jāveido manuāli. Šīs opcijas rezultātā noklusētās vērtības tiks izmantotas ar kreditoru saistītiem laukiem. Ja dokumentam, no kura kopējat, ir nenoklusējuma vērtības, ko vēlaties kopēt, izmantojiet arī opciju **Kopēt precīzi**.
    - Pastāv dažādi dokumentu avotiem, no kuriem varat kopēt, un katram šajā lapā ir atsevišķa sadaļa. Piemēram, sadaļa **Pirkšanas pasūtījumi** ļauj kopēt no esošiem pirkšanas pasūtījumiem.  

1. Sadaļā **Pirkšanas pasūtījumi** atlasiet rindas, ko vēlaties kopēt starpliktuvē. Ir iespējams atlasīt papildu pirkšanas pasūtījumu rindas no citiem pirkšanas pasūtījumiem un arī tās kopēt uz savu pasūtījumu. Ir iespējams arī pievienot rindas no citu veidu pirkšanas dokumentiem. Nākamajās dažās darbības ir apskatītas šīs dažādās opcijas.  
1. Izvērsiet sadaļu **Apstiprinājums**. Šeit varat atlasīt pirkšanas pasūtījumu apstiprinājumus, no kuriem kopēt. Pirkšanas pasūtījuma apstiprinājumi tiek identificēti ar saistīto pirkšanas žurnāla ID vai pirkšanas pasūtījuma ID.  
1. Izvērsiet sadaļu **Produktu saņemšanas**. Šeit varat atlasīt produktu ieejas plūsmas žurnālus, no kuriem kopēt. Produktu ieejas plūsmas žurnāli tiek identificēti ar produktu ieejas plūsmas dokumentu vai pirkšanas pasūtījuma ID.
1. Izvērsiet sadaļu **Rēķini**. Šeit varat atlasīt kreditoru rēķinus, no kuriem kopēt. Rēķini tiek identificēti ar rēķina dokumentu vai pirkšanas pasūtījuma ID.
1. Izvērsiet sadaļu **Atlasītās rindas vai kopējamā galvene**. Šajā skatā tiek rādīts kopsavilkums par visiem dokumentiem un rindām, kas ir atlasītas kopēšanai uz jūsu pasūtījumu.
1. Atlasiet **Labi**. Rindas, ko atlasījāt, ir iekopētas jūsu jaunajā pirkšanas pasūtījumā.

## <a name="copy-lines-to-an-existing-purchase-order"></a>Kopēt rindas uz esošu pirkšanas pasūtījumu  

Tā vietā, lai kopētu visu pasūtījumu, biežāk tiek izveidots jauns pirkšanas pasūtījums (PP) un aizpildīta informācija šī PP virsrakstā, un pēc tam kopētas atsevišķas rindas no esošajiem pasūtījumiem.  

1. Atlasiet rindu **Pirkšanas pasūtījums**.
1. Atlasiet **No visiem**. Tiek atvērta iepriekš parādītajai identiska lapa, bet ir atlasītas citādas opcijas, kad tā tiek atvērta no pasūtījuma rindu skata. Apskatīsim parametrus.
1. Izvērsiet sadaļu **Parametri**.

    - Nav **atlasīta opcija Dzēst** pirkšanas rindas. Tas nozīmē, ka uz savu pasūtījumu varat kopēt jaunas rindas, noņem esošās rindas.
    - Arī opcija **Kopēt pasūtījuma galveni** nav atlasīta, jo pievienojam pasūtījumam tikai papildu rindas.
    - Šajā piemērā mēs kopēsim rindas no esoša pirkšanas pasūtījuma.

1. Atlasiet vēlamā pirkšanas pasūtījuma rindu. Ņemiet vērā, ka ir atlasīta arī vienīgā pasūtījuma rinda, kas atrodas šajā pirkšanas pasūtījumā (PO).  
1. Atlasiet **Labi**. Jūsu pirkšanas pasūtījumam ir pievienota papildu pasūtījuma rinda.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]