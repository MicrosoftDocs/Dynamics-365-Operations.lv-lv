---
title: Uzskaites vai pārskata valūtas maiņa
description: Šajā tēmā ir paskaidrots, kā mainīt uzskaites vai pārskata valūtu vai pievienot pārskata valūtu virsgrāmatas iestatījumiem.
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0435deb009173684c7faaf5340e8095c019ec71c
ms.sourcegitcommit: 2cd82983357b32f70f4e4a0c15d4d1f69e08bd54
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/20/2021
ms.locfileid: "6085478"
---
# <a name="change-the-accounting-or-reporting-currency"></a>Uzskaites vai pārskata valūtas maiņa

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā mainīt uzskaites vai pārskata valūtu vai pievienot pārskata valūtu virsgrāmatas iestatījumiem.

## <a name="symptom"></a>Simptoms

Jūs vēlaties mainīt uzskaites vai pārskata valūtu vai pievienot pārskata valūtu virsgrāmatas iestatījumiem. Tas parasti notiek tālāk aprakstītajos gadījumos.

- Iestatot juridisku personu, tika norādīta nepareiza uzskaites vai pārskata valūta. Tagad jūs vēlaties mainīt šo valūtu.
- Iestatot juridisku personu, tika norādīta pārskata valūta, bet tagad organizācija vēlas noņemt pārskata valūtu.
- Organizācija jaunina vai migrē uz Microsoft Dynamics 365 Finance un vēlas mainīt uzskaites vai pārskata valūtu.

Organizācija, kas iepriekš neizmantoja divkāršās valūtas iespēju, vēlas sākt to izmantot. Šī problēma parasti notiek tālāk aprakstītajos gadījumos.

- Iestatot juridisku personu, netika norādīta nekāda uzskaites vai pārskata valūta. (Pārskata valūta nav obligāta.) Tagad vēlaties pievienot pārskata valūtu.

## <a name="resolution"></a>Novēršana

Svarīgākais apsvērums ir tas, vai virsgrāmatas iestatījumos juridiskajai personai ir iegrāmatotas jebkādas transakcijas (faktiskas vai budžeta). **Ja par juridisko personu ir iegrāmatotas jebkādas transakcijas (faktiskas vai budžeta), nav iespējams mainīt uzskaites vai pārskata valūtu vai pievienot pārskata valūtu.** Atkarībā no tā, vai transakcijas ir iegrāmatotas, veiciet kādā no tālāk norādītajām sadaļām aprakstītās darbības.

### <a name="no-transactions-have-been-posted"></a>Nav iegrāmatota neviena transakcija

1. Tās juridiskās personas sadaļā, kurai atjaunināt valūtas, dodieties uz **Virsgrāmata \> Virsgrāmatas iestatīšana \> Virsgrāmata**.
2. Lapā **Virsgrāmata** atlasiet **Rediģēt**.
3. Kopsavilkuma cilnē **Valūta** atlasiet juridiskajai personai izmantojamo uzskaites valūtu un pārskata valūtu.
4. Atlasiet **Saglabāt**.

Ja lapā **Virsgrāmata** nav pieejami uzskaites valūtas un pārskata valūtas lauki, par juridisko personu ir iegrāmatota viena vai vairākas transakcijas (faktiskas vai budžeta). Tādēļ valūtas nevar mainīt. Šādā gadījumā veiciet nākamajā sadaļā norādītās darbības.

### <a name="transactions-have-been-posted"></a>Ir iegrāmatotas transakcijas

**Ja juridiskajai personai ir iegrāmatotas transakcijas, tad vienīgais veids, kā mainīt vai pievienot uzskaites un pārskata valūtas, ir izveidot jaunu juridisko personu ar pareizajām valūtām.** Lai palīdzētu padarīt šo procesu ērtāku, datu pārvaldības opcija sistēmā sniedz iespēju kopēt iestatīšanas ierakstus un pamata ierakstus no pašreizējās juridiskās personas uz jaunu juridisko personu.

Uzskaites un pārskata valūtu izmaiņas tiek izplatītas. Tās ietekmē ne tikai virsgrāmatu, bet arī visas apakšvirsgrāmatas (Debitori, Kreditori, Krājumi, Projekts un citas apakšvirsgrāmatas), visus neatkarīgo programmatūras izstrādātāju (independent software vendor — ISV) risinājumus un visus izveidotos paplašinājumus, kuros tiek glabātas summas.

Katras summas atrašanas un tulkošanas process uz citu valūtu ir pakļauts kļūdas riskam. Tādēļ inženieru grupa neapstiprinās skriptu, kas maina vai pievieno uzskaites un pārskata valūtas. Turklāt, lai gan rīks, kas agrāk bija pieejams risinājumā Microsoft Dynamics AX 2012, sniedza iespēju mainīt vai pievienot uzskaites un pārskata valūtas, šis rīks tika atzīts par novecojušu risinājumam AX 2012 R3 un Finance.

Veiciet šīs darbības, lai kopētu iestatījumu datus un pamatdatus no pašreizējās juridiskās personas uz jaunu juridisku personu.

1. Dodieties uz **Darbvietas \> Datu pārvaldība**.
2. Grupā **Importēšana/eksportēšana** atlasiet **Veidnes**.
3. Pārliecinieties, vai veidnes ir pieejamas. Ja veidnes nav pieejamas, atlasiet **Ielādēt noklusējuma veidnes** un uzgaidiet, līdz veidnes tiek ģenerētas.
4. Atgriezieties darbvietā **Datu pārvaldība**.
5. Atlasiet **Kopēt juridiskajā personā**.
6. Ievadiet grupas nosaukumu un aprakstu.
7. Laukā **Avota juridiskā persona** atlasiet juridisko personu, no kuras kopēt datus.
8. Kopsavilkuma cilnē **Mērķa juridiskās personas** atlasiet **Izveidot juridiskās personas**, lai izveidotu jaunu juridisko personu, kurā varat kopēt avota juridiskās personas datus. Atlasiet **Atlasīt esošu**, lai kopētu datus esošā juridiskajā personā.
9. Neobligāti: laukā **Kopēt skaitļu virknes** norādiet vērtību **Jā**. (Šī darbība ir ieteicama, kopējot datus.)
10. Apgabalā **Atlasītie elementi** atlasiet **Pievienot veidni**.
11. Atlasiet veidnes, ko izmantot. Ieteicamās veidnes jaunai juridiskajai personai iever **025 — Virsgrāmata** un **Finanses**. Ieteicams pārskatīt visas pārējās pieejamās veidnes, lai noteiktu, vai kāda no tām attiecas uz jūsu prasībām.
12. Atlasiet **Kopēt juridiskajā personā**, lai sāktu pakešveida apstrādi, kas izveidos atlasītos elementus un kopēs tos mērķa juridiskajā personā.
13. Kad process ir pabeigts, bet pirms kāda transakcija ir iegrāmatota, dodieties uz virsgrāmatu un atjauniniet uzskaites un pārskata valūtas, kā aprakstīts iepriekš šajā tēmā.

Ja izveidojāt jaunu juridisku personu, lai varētu mainīt uzskaites vai pārskata valūtu, pārbaudiet, vai sākuma bilances tiek pārrēķinātas no iepriekšējās juridiskās personas valūtām uz jaunajām valūtām.

Video, kurā parādītas iepriekšējās darbības, skatiet vietnē [Kopēšana juridiskajā personā](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).
