---
title: Papildu līgumu izveide norēķiniem, pamatojoties uz progresu
description: Šajā tēmā skaidrots, kā izveidot projektu līgumus, lai varētu ģenerēt debitoru rēķinus, pamatojoties uz pabeigto darbu procentuālo attiecību.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282837"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Papildu līgumu izveide norēķiniem, pamatojoties uz progresu
[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā izveidot projektu līgumus, lai varētu izveidot debitoru rēķinus, pamatojoties uz pabeigto darbu procentuālo attiecību. Rēķina summas tiek aprēķinātas automātiski darba budžeta kategorijām, ko iestatījāt projektam. Rēķinu izrakstīšanas grafiks tiek iestatīts, kad ar debitoru vienojaties par projekta līgumu.

Izmantojiet procedūras šajā tēmā, lai uzstādītu līgumu, saistītu projektu un norēķinu nosacījumus, ko izmantot, lai aprēķinātu rēķinu summas darba budžeta kategorijām, ko esat uzstādījis projektam.

Pēc tam, kad esat izveidojis līgumu un projektu, varat iestatīt projekta detaļas. Piemēram, varat definēt projekta aktivitātes un piešķirt projektam darbiniekus.

## <a name="example"></a>Paraugs

Jūsu organizācija ir programmatūras izstrādes firma. Jūs piekrītat debitoram izstrādāt algu uzskaites pakotni par 20 000 ASV dolāru (USD) kopējo samaksu. Jūsu organizācija piekrīt nosūtīt debitoram rēķinu, kad pabeidzat noteiktu procentuālu daudzumu projekta darba. Jūs varat iestatīt šādas projekta kategorijas darbam, lai tās varētu izmantot norēķinu procesā:

- Konsultācijas
- Dizains
- Instalēšana

Iestatiet arī norēķinu nosacījumus, kas automātiski aprēķina rēķina summas procentuālajam daudzumam projekta darba, kas ir pabeigts katrā kategorijā.

Budžeta pārvaldītājs izveido budžetu projekta kategorijām. Pabeigtā darba apjoms tiek automātiski aprēķināts kā faktiskā darba procentuālais apjoms salīdzinājumā ar budžetā paredzēto apjomu.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms izveidojat projektu, kas izmanto norēķinu kārtulas, ir jāiestata numuru sērijas norēķinu kārtulām un papildmaksu žurnālam, ko izmanto progresa rēķinu grāmatošanai.

1. Dodieties uz **Projektu vadība un uzskaite** \> **Iestatīšana** \> **Projektu vadības un uzskaites parametri**.
2. Lapā **Projekta pārvaldības un uzskaites parametri** cilnē **Numuru sērijas** iestatiet numuru sēriju, ko vēlaties izmantot, izveidojot norēķinu kārtulas.
3. Dodieties uz **Projekta vadība un uzskaite** \> **Žurnāli** \> **Maksa**.
4. Lapā **Maksas žurnāls** atlasiet **Jauns** un ievadiet žurnāla nosaukumu.

## <a name="create-a-contract-for-progress-billings"></a>Izveidot līgumu apmaksai atbilstoši progresam

Izmantojiet šo procedūru, lai izveidotu projekta līgumu fiksētas cenas projektam. Jāizveido projekta rēķins, kad projektā pabeigtais darbs sasniedz norādīto procentuālo vērtību.

1. Dodieties uz **Projektu vadība un uzskaite** \> **Projekti** \> **Projekta līgumi**.
2. Lapā **Projekta līgumi** atlasiet **Jauns**.
3. Dialoglodziņā **Jauns projekta līgums** iestatiet sekojošus laukus:

    - **Vārds/nosaukums**
    - **Finansējuma veids**
    - **Finansējuma avots**
    - **Pārdošanas valūta** — pēc noklusējuma šo valūtu lieto debitoru rēķiniem, kas saistīti ar projekta līgumu. Tomēr varat mainīt noteikta debitora rēķina pārdošanas valūtu.

4. Atlasiet **Labi**. Informācija tiek kopēta uz lapas **Projekta līgumi** galveni.
5. Lapā **Projekta līgumi** aizpildiet visu nepieciešamo projekta informāciju.

## <a name="create-a-project-for-progress-billings"></a>Izveidot projektu apmaksai atbilstoši progresam

Sekojiet šiem soļiem, lai izveidotu projektu un apakšprojektus, kas ir saistīti ar projekta līgumu.

1. Dodieties uz **Projektu vadība un uzskaite** \> **Projekti** \> **Visi projekti**.
2. Lapā **Visi projekti** atlasiet **Jauns**.
3. Dialoglodziņā **Jauns projekts** laukā **Projekta veids** atlasiet **Laiks un materiāli**.
4. Atlasiet projektu grupu. Projektu grupa nosaka grupai piešķirto projektu grāmatošanas informāciju.
5. Atlasiet **Izveidot projektu**.
6. Kad esat izveidojis projektu, iestatiet projekta posmu kā **Notiek**.

## <a name="create-a-budget-for-a-project"></a>Izveidot budžetu projektam

Budžeta kategorijas tiek izmantotas, lai automātiski aprēķinātu summas par katrā kategorijā pabeigtā darba procentuālo apjomu. Sekojiet šiem soļiem, lai izveidotu budžeta kategorijas prognozētajām izmaksām.

1. Dodieties uz **Projektu vadība un uzskaite** \> **Projekti** \> **Visi projekti**.
2. Lapā **Visi projekti** atlasiet un atveriet vēlamo projektu.
3. Lapā **Projekti**, kas atrodas darbības rūtī, cilnē **Plāns**, grupā **Budžets** atlasiet **Projekta budžets**.
4. Lapā **Projekta budžets** ievadiet novērtētās izmaksas katrai projekta kategorijai.

## <a name="create-billing-rules-for-progress-billings"></a>Izveidot norēķinu nosacījumus apmaksai atbilstoši progresam

1. Dodieties uz **Projektu vadība un uzskaite** \> **Projekti** \> **Projekta līgumi**.
2. Lapā **Projekta līgumi** atlasiet un atveriet projekta līgumu.
3. Projekta līguma lapā, kas atrodas **Norēķinu kārtulas** kopsavilkuma cilnē atlasiet **Pievienot**.
4. Lapā **Norēķinu kārtula** laukā **Rindas veids** atlasiet **Progress**.
5. **Norēķinu kārtulu līnijas informācija** kopsavilkuma cilnē laukā **Līguma vērtība** ievadiet līguma kopējo vērtību.
6. Laukā **Kategorija** atlasiet kategoriju, uz kuru grāmatot apmaksas transakciju.
7. Laukā **Projekts** atlasiet projektu, kas izmanto šo norēķinu kārtulu.
8. Neobligāti: piešķirt norēķinu kārtulu papildu projektiem. Kopsavilkuma cilnē **Projekts** sadaļā **Pieejamie projekti** atlasiet projektu un pēc tam atlasiet labo bultiņu, lai pievienotu projektu sadaļai **Atlasītie projekti**.
9. Neobligāti: aprēķiniet procentuālu vērtību, ko klients ietur no rēķina maksājumiem. Kopsavilkuma cilnē **Maksājuma ieturēšanas noteikumi** atlasiet finansējuma avotu un pēc tam laukā **Ieturēšanas procents** ievadiet ieturēšanas procentu.
10. Atkārtojiet šos soļus, lai izveidotu papildu norēķinu kārtulas projekta līgumam.
