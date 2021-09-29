---
title: Kvīšu formātu iestatīšana un noformēšana
description: Šajā rakstā ir aprakstīts, kā izveidot un modificēt formu izkārtojumus, lai kontrolētu to, kā tiek drukāti rēķini, kvītis un citi dokumenti. Programmā Dynamics 365 Commerce ir ietverts formas izkārtojuma noformētājs, ko varat izmantot, lai viegli izveidotu un izmainītu dažādu viedu formu izkārtojumus.
author: rubencdelgado
ms.date: 09/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFormLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a2107670cb5dbac3b8f28c4e3caa357102932291
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500174"
---
# <a name="set-up-and-design-receipt-formats"></a>Kvīšu formātu iestatīšana un noformēšana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot un modificēt formu izkārtojumus, lai kontrolētu to, kā tiek drukāti rēķini, kvītis un citi dokumenti. Dynamics 365 Commerce ir ietverts formas izkārtojuma noformētājs, kuru varat izmantot, lai ērtā un grafiskā veidā izveidotu un modificētu dažādus formu izkārtojumus.

> [!IMPORTANT]
> Lai drukātu kvītis un citus dokumentus programmās Retail Modern POS un Cloud POS, ir jāiestata formu izkārtojumi un kvīšu profili. Kvīšu profilā var ietvert vairākus formu izkārtojumus. Pēc tam kvīts profilu var piešķirt printerim, modificējot aparatūras profilu.

## <a name="set-up-a-receipt-format"></a>Kvīts formāta iestatīšana

1. Noklikšķiniet uz **Retail un Commerce** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS** &gt; **Kvīšu formāti**.
2. Lapā **Kvīts formāts** noklikšķiniet uz **Jauns**, lai izveidotu jaunu formas izkārtojumu, vai atlasiet esošu formas izkārtojumu.
3. Laukā **Kvīts formāts** ievadiet formas izkārtojuma identifikatoru un pēc tam atlasiet šajā izkārtojumā izmantotās kvīts veidu. Laukā **Nosaukums** var arī ievadīt kvīts aprakstu un īsu tās nosaukumu.
4. Kopsavilkuma cilnē **Vispārīgi** atlasiet opciju, kas definētu drukāšanas režīmu.

    - **Drukāt vienmēr** — kvīts, ja nepieciešams, tiek drukāta automātiski.
    - **Nedrukāt** — kvīts netiek drukāta.
    - **Parādīt lietotājam uzvedni** — lietotājam tiek parādīta uzvedne par kvīts drukāšanu.
    - **Kā nepieciešams** — šo opciju izmanto tikai dāvanu kvītīm. Ja ir nepieciešama dāvanu kvīts un šī opcija ir atlasīta, lietotājs var izdrukāt dāvanu kvīti, izmantojot lapu **Mainīt**.

## <a name="print-images"></a>Attēlu drukāšana

Kvīšu noformētājs ietver mainīgo **Logotips**. Šo mainīgo varat izmantot, lai konkretizētu attēlu, kuru vajadzētu drukāt uz kvītīm. Attēliem, kas tiek drukāti uz kvītīm, izmantojot **Logotipa** mainīgo, ir jābūt vienkrāsainiem bitkartes (.bmp) tipu failiem. Ja kvīšu noformētājā ir norādīts bitmap attēls, bet tas netiek drukāts, kad kvīts tiek nosūtīta uz printeri, problēmu var būt izraisījis viens no tālāk minētajiem iemesliem:

- Fails ir pārāk liels vai attēla pikseļu izmēri neatbilst printerim. Šādā gadījumā mēģiniet samazināt attēla faila izšķirtspēju vai izmēru.
- Daži objektu saistīšanas un iegulšanas pārdošanas punktā (OPOS) printeru draiveri neizmanto metodi **PrintMemoryBitmap**, kuru aparatūras stacijas izmanto logotipu attēlu drukāšanā. Šādā gadījumā mēģiniet jūsu privātās vai koplietotās aparatūras stacijas failam **HardwareStation.Extension.config** pievienot šādu karodziņu:

    `<add name="HardwareStation.UsePrintBitmapMethod" value="true"/>`

## <a name="design-a-receipt-format"></a>Kvīts formāta noformēšana

Izmantojiet formas izkārtojuma noformētāju, lai grafiski izveidotu formas dokumenta izkārtojumu. Lapā **Kvīts formāta dizains** ir trīs sadaļas: **Galvene**, **Rindas** un **Kājene**. Dažos formas izkārtojuma veidos tiek izmantoti elementi no visam trīs sadaļām, bet citos veidos tiek izmantoti tikai vienas vai divu sadaļu elementi. Lai redzētu katrā sadaļā pieejamos elementus, noklikšķiniet uz attiecīgās pogas navigācijas rūtī lapas kreisajā pusē.

1. Noklikšķiniet uz **Retail un Commerce** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS** &gt; **Kvīšu formāti**.
2. Lapā **Kvīts formāts** atlasiet formas izkārtojumu un pēc tam noklikšķiniet uz **Noformētājs**.
3. Lai uzsāktu Commerce noformētāja resursdatora instalēšanu, noklikšķiniet uz **Palaist**.
4. Internet Explorer loga apakšdaļā parādītajā paziņojumu joslā noklikšķiniet uz **Atvērt**, lai sāktu viena klikšķa noformētāja instalēšanu. (Citās pārlūkprogrammās paziņojumu josla var tikt rādīta citā vietā.) Norises indikators norāda instalēšanas procesa norisi.
5. Kad instalēšana ir pabeigta, ievadiet savu Commerce lietotājvārdu un paroli un pēc tam noklikšķiniet uz **Pierakstīties**, lai palaistu noformētāju.
6. Kad jūsu akreditācijas dati ir apstiprināti un noformētājs ir palaists, var sākt kvīts formāta veidošanu vai esošā formāta mainīšanu.
7. Lai izveidotu formas elementus, atlasiet sadaļu **Galvene**, **Rindas** vai **Kājene** un pēc tam velciet elementu no šīs sadaļas uz darbvietu. Vairums elementos ir iekļauti mainīgie, kas tiek automātiski aizpildīti ar datiem no datu bāzes. Citi elementi, piemēram, **Teksts**, ļauj jums kvītī drukāt pielāgotu tekstu.

    > [!NOTE]
    > Var norādīt, cik rindu aizņem katra sadaļa, pielāgojot šīs sadaļas apakšējā labajā stūrī redzamo skaitli. Lai atvieglotu sadaļas modificēšanu, palieliniet tās augstumu, velkot sadaļas apakšdaļā redzamo izmēra maiņas joslu. Sadaļas augstums darbvietā neietekmē faktiskās kvīts rindu skaitu.

8. Kad elements ir ievilkts darbvietā, iestatiet šīs daļas rekvizītus lapas apakšā redzamajā rūtī **Objekta dati**. Ievadiet vienu vai vairākus no šiem iestatījumiem:

    - **Līdzināt** — iestatiet lauka līdzinājuma metodi **Pa kreisi** vai **Pa labi**.
    - **Aizpildīšanas rakstzīme** — norādiet baltstarpas rakstzīmi. Pēc noklusējuma tiek izmantota atstarpe, bet var ievadīt jebkuru rakstzīmi.
    - **Prefikss** — ievadiet vērtību, kas ir jāparāda lauka sākumā. Šis iestatījums attiecas tikai uz izkārtojuma sadaļu **Rindas**.
    - **Rakstzīmes** — norādiet maksimālo laukā iekļaujamo rakstzīmju skaitu, ja elementā ir iekļauts mainīgais. Ja laukā teksts ir garāks par norādīto rakstzīmju skaitu, šis teksts tiek apcirsts, lai to ietilpinātu laukā.
    - **Mainīgais** — šī izvēles rūtiņa tiek atzīmēta automātiski, ja elementā ir iekļauts mainīgais un to nevar pielāgot.
    - **Fonta tips** — iestatiet fonta stilu kā **Parasts** vai **Treknraksts**. Treknraksta burti izmanto divreiz vairāk vietas nekā parastie burti. Tāpēc dažas rakstzīmes var tikt apcirstas.
    - **Fonta lielums** — iestatiet fonta lielumu kā **Parasts** vai **Liels**. Lielie burti ir divas reizes augstāki nekā parastie burti. Tādēļ, izmantojot lielus burtus, var izraisīt teksta pārklāšanos kvītī.
    - **Dzēst** — noklikšķiniet uz šīs pogas, lai atlasīto daļu noņemtu no formas izkārtojuma.

## <a name="assign-receipt-profiles"></a>Kvīšu profilu piešķiršana

Kvīšu profili tiek piešķirti tieši printeriem, izmantojot aparatūras profilu.

1. Lai atvērtu aparatūras profilu, noklikšķiniet uz **Retail un Commerce** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS profili** &gt; **Aparatūras profili**.
2. Atlasiet printeri un pēc tam laukā **Kvīts profils** norādiet kvīts profilu, kas jāizmanto reģistrā.

> [!NOTE]
> Ja tiek izmantoti divi printeri, vienu printeri var izmantot, lai izdrukātu standarta 40 sleju termodrukas kvītis. Otro printeri parasti izmanto, lai izdrukātu pilnas lapas kvītis veidus, kuros jāiekļauj papildu informācija. Šie kvīšu veidi iekļauj debitora pasūtījuma kvītis un debitora rēķinus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
