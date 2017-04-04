---
title: "Kvīts veidnes un drukāšana"
description: "Šajā rakstā ir aprakstīts, kā izveidot un modificēt formu izkārtojumus, lai kontrolētu to, kā tiek drukāti rēķini, kvītis un citi dokumenti. Microsoft Dynamics 365 operācijām - mazumtirdzniecība ietver izkārtojuma veidlapas dizainers, ko var izmantot, lai viegli izveidot un modificēt dažāda veida veidlapas izkārtojumu."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fabaacbc7187b38a1745c2139a9eb7760f2be987
ms.lasthandoff: 03/31/2017


---

# <a name="receipt-templates-and-printing"></a>Kvīts veidnes un drukāšana

Šajā rakstā ir aprakstīts, kā izveidot un modificēt formu izkārtojumus, lai kontrolētu to, kā tiek drukāti rēķini, kvītis un citi dokumenti. Microsoft Dynamics 365 operācijām - mazumtirdzniecība ietver izkārtojuma veidlapas dizainers, ko var izmantot, lai viegli izveidot un modificēt dažāda veida veidlapas izkārtojumu.

**Svarīgi:** jāiestata veidlapas izkārtojumu un saņemšanas izdrukāt kvītis un citus dokumentus no mazumtirdzniecības mūsdienu POS un mākonis POS profili. Saņemšanas profils var iekļaut vairākus veidlapas izkārtojumu. Pēc tam kvīts profilu var piešķirt printerim, modificējot aparatūras profilu.

## <a name="set-up-a-receipt-format"></a>Kvīts formāta iestatīšana
1.  Noklikšķiniet uz **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**POS**&gt;**saņemšanas formātus**.
2.  Lapā **Kvīts formāts** noklikšķiniet uz **Jauns**, lai izveidotu jaunu formas izkārtojumu, vai atlasiet esošu formas izkārtojumu.
3.  Laukā **Kvīts formāts** ievadiet formas izkārtojuma identifikatoru un pēc tam atlasiet šajā izkārtojumā izmantotās kvīts veidu. Laukā **Nosaukums** var arī ievadīt kvīts aprakstu un īsu tās nosaukumu.
4.  Kopsavilkuma cilnē **Vispārīgi** atlasiet opciju, kas definētu drukāšanas režīmu.
    -   **Drukāt vienmēr** — kvīts, ja nepieciešams, tiek drukāta automātiski.
    -   **Nedrukāt** — kvīts netiek drukāta.
    -   **Parādīt lietotājam uzvedni** — lietotājam tiek parādīta uzvedne par kvīts drukāšanu.
    -   **Kā nepieciešams** — šo opciju izmanto tikai dāvanu kvītīm. Ja ir nepieciešama dāvanu kvīts un šī opcija ir atlasīta, lietotājs var izdrukāt dāvanu kvīti, izmantojot lapu **Mainīt**.

## <a name="design-a-receipt-format"></a>Kvīts formāta noformēšana
Izmantojiet formas izkārtojuma noformētāju, lai grafiski izveidotu formas dokumenta izkārtojumu. Lapā **Kvīts formāta dizains** ir trīs sadaļas: **Galvene**, **Rindas** un **Kājene**. Dažos formas izkārtojuma veidos tiek izmantoti elementi no visam trīs sadaļām, bet citos veidos tiek izmantoti tikai vienas vai divu sadaļu elementi. Lai redzētu katrā sadaļā pieejamos elementus, noklikšķiniet uz attiecīgās pogas navigācijas rūtī lapas kreisajā pusē.

1.  Noklikšķiniet uz **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**POS**&gt;**saņemšanas formātus**.
2.  Lapā **Kvīts formāts** atlasiet formas izkārtojumu un pēc tam noklikšķiniet uz **Veidotājs**.
3.  Lai uzsāktu mazumtirdzniecības veidotāja resursdatora instalēšanu, noklikšķiniet uz **Palaist**.
4.  Lai sāktu veidotāja instalēšanu ar vienu klikšķi, pārlūkprogrammas Internet Explorer loga apakšā parādītajā paziņojumu joslā noklikšķiniet uz **Atvērt**. (Uz paziņojumu joslas var parādīties citās pārlūkprogrammās citā vietā.) Progresa indikatora redzama instalācijas procesu norise.
5.  Pēc tam, kad instalācija ir pabeigta, ievadiet Dynamics 365 operācijas lietotāja vārdu un paroli un pēc tam noklikšķiniet uz **pieteikties** sākt dizainers.
6.  Kad jūsu akreditācijas dati ir apstiprināti un veidotājs ir palaists, var sākt kvīts formāta veidošanu vai esošā formāta mainīšanu.
7.  Lai izveidotu formas elementus, atlasiet sadaļu **Galvene**, **Rindas** vai **Kājene** un pēc tam velciet elementu no šīs sadaļas uz darbvietu. Vairums elementos ir iekļauti mainīgie, kas tiek automātiski aizpildīti ar datiem no datu bāzes. Citi elementi, piemēram, **Teksts**, ļauj jums kvītī drukāt pielāgotu tekstu. **Piezīme.** Var norādīt, cik rindu aizņem katra sadaļa, pielāgojot šīs sadaļas apakšējā labajā stūrī redzamo skaitli. Lai atvieglotu sadaļas modificēšanu, palieliniet tās augstumu, velkot sadaļas apakšdaļā redzamo izmēra maiņas joslu. Sadaļas augstums darbvietā neietekmē faktiskās kvīts rindu skaitu.
8.  Kad elements ir ievilkts darbvietā, iestatiet šīs daļas rekvizītus lapas apakšā redzamajā rūtī **Objekta dati**. Ievadiet vienu vai vairākus no šiem iestatījumiem:
    -   **Līdzināt** — iestatiet lauka līdzinājuma metodi **Pa kreisi** vai **Pa labi**.
    -   **Aizpildīšanas rakstzīme** — norādiet baltstarpas rakstzīmi. Pēc noklusējuma tiek izmantota atstarpe, bet var ievadīt jebkuru rakstzīmi.
    -   **Prefikss** — ievadiet vērtību, kas ir jāparāda lauka sākumā. Šis iestatījums attiecas tikai uz izkārtojuma sadaļu **Rindas**.
    -   **Rakstzīmes** — norādiet maksimālo laukā iekļaujamo rakstzīmju skaitu, ja elementā ir iekļauts mainīgais. Ja laukā teksts ir garāks par norādīto rakstzīmju skaitu, šis teksts tiek apcirsts, lai to ietilpinātu laukā.
    -   **Mainīgais** — šī izvēles rūtiņa tiek atzīmēta automātiski, ja elementā ir iekļauts mainīgais un to nevar pielāgot.
    -   **Fonta tips** — iestatiet fonta stilu kā **Parasts** vai **Treknraksts**. Treknraksta burti izmanto divreiz vairāk vietas nekā parastie burti. Tāpēc dažas rakstzīmes var tikt apcirstas.
    -   **Dzēst** — noklikšķiniet uz šīs pogas, lai atlasīto daļu noņemtu no formas izkārtojuma.

## <a name="assign-receipt-profiles"></a>Kvīšu profilu piešķiršana
Kvīšu profili tiek piešķirti tieši printeriem, izmantojot aparatūras profilu.

1.  Aparatūras profilu var atvērt, noklikšķinot uz **mazumtirdzniecības un komercijas**&gt;**Channel setup**&gt;**POS uzstādīšanas**&gt;**POS profili**&gt;**aparatūras profilu**.
2.  Atlasiet printeri un pēc tam laukā **Kvīts profils **norādiet kvīts profilu, kas jāizmanto reģistrā.

**Piezīme.** Ja tiek izmantoti divi printeri, vienu printeri var izmantot, lai izdrukātu standarta 40 sleju termodrukas kvītis. Otro printeri parasti izmanto, lai izdrukātu pilnas lapas kvītis veidus, kuros jāiekļauj papildu informācija. Šie kvīšu veidi iekļauj debitora pasūtījuma kvītis un debitora rēķinus.


