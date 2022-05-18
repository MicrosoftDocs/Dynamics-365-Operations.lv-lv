---
title: PVN maksājuma izveide
description: PVN segšanas un iegrāmatošanas darba procedūra sedz PVN bilances PVN kontos un noteiktajam periodam atlīdzina tās PVN maksājumu kontā.
author: twheeloc
ms.date: 01/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c388a8f98cd4581abe2ec13d8922e232321e4039
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735867"
---
# <a name="create-a-sales-tax-payment"></a>PVN maksājuma izveide

[!include [banner](../../includes/banner.md)]

PVN segšanas un iegrāmatošanas darba procedūra sedz PVN bilances PVN kontos un noteiktajam periodam atlīdzina tās PVN maksājumu kontā.

1. Dodieties uz **Nodokļi > Deklarācijas > PVN > Nosegt un grāmatot PVN**.
2. Laukā **Maksājumu periods** atlasiet nolaižamo pogu, lai atvērtu uzmeklēšanu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Ievadiet datumu laukā **No datuma**. Ja lapā **Virsgrāmatas parametri** neatlasīsiet opciju **Iekļaut labojumus**, segšanu var apstrādāt dažādām versijām. **Oriģināls** ir pirmais perioda intervāla nosegšana, un to var apstrādāt tikai vienreiz perioda intervālam. Pēdējie labojumi nosegs PVN darbības, kas ir grāmatotas pēc sākotnējās versijas izveides.
5. Ievadiet datumu laukā **Transakcijas datums**.
6. Atlasiet **Labi**. Lai **apskatītu periodā** nosegtās PVN darbības, tiek drukāts PVN maksājumu pārskats.

Sākot ar finanšu versiju 10.0.24, varat izlaist PVN maksājumu pārskatu, kas tiek ģenerēts tieši pēc tam, **·** **·** **·** **kad apmaksas un grāmatošanas PVN periodiskā procedūra ir ieviesta Atsevišķā PVN maksājuma pārskata ģenerēšanas no PVN maksāšanas līdzekļa līdzekļu pārvaldības darbvietā.**

Kad šis līdzeklis ir iespējots, pēc segšanas procesa pabeigšanas NETIEK drukāts PVN maksājumu pārskats. Tā vietā jūs saņemat šādu ziņojumu" "PVN apmaksa un grāmatošana ir pabeigta. Dokuments 'xxxx, m/d/gggg' ir grāmatots.

Jūs joprojām varat manuāli palaist PVN maksājumu pārskatu, ejot uz TaxInquiries **un reportsPārdošanas** > **nodokļu pieprasījumiPārdošanas** > **nodokļu maksājumi** > **.**

## <a name="performance-consideration"></a>Veiktspējas apsvērumi

PVN apmaksas procedūra var aizņemt ilgāku laiku. Galvenie faktori, kas ietekmē procedūras veiktspēju, ir rēķinu skaits maksājumu periodā un ierakstu skaits, kas jāgrāmato PVN apmaksas dokumentā. Lai uzlabotu veiktspēju, varat apiet kādu no funkcijām, kas jūsu procesā nav nepieciešamas.

### <a name="enable-the-sales-tax-payment-performance-improvement-feature"></a>Iespējot PVN maksājumu veiktspējas uzlabošanas līdzekli

**PVN maksājumu veiktspējas uzlabošanas** funkcija var palīdzēt uzlabot PVN apmaksas procedūras veiktspēju, vienā rindā saskaitot uzskaites valūtas summu un pārskata valūtas summu PVN maksājuma dokumenta rindās, kurās ir viens galvenais konts, virsgrāmatas dimensija un valūta.

1. Dodieties uz **Sistēmas administrēšana** \> **Darbvietas** \> **Līdzekļu pārvaldība**.
2. Cilnē **Viss** meklējiet un atlasiet **PVN maksājuma veiktspējas uzlabojumu**.
3. Atlasiet **Iespējot**.

### <a name="prevent-generation-of-offset-tax-transactions"></a>Neļaut korespondējošo nodokļu darbību ģenerēšanu

Pēc noklusējuma PVN maksājuma dokuments grāmato korespondējošās PVN darbības katram PVN darījumam, kas tiek segts PVN apmaksas procedūrā. Šīs korespondējošās PVN darbības ir iekļautas **PVN/Virsgrāmatas saskaņošanas** pārskatā. Tās parāda neapmaksāto PVN darbību bilanci, kas perioda laikā nav nosegta.

Tomēr korespondējošās PVN darbības var palielināt slogu PVN apmaksas procedūrā. Tāpēc reisu ar nosaukumu **TaxReportGenOffsetTaxTransPerRecordSetFlighting** var aktivizēt pēc pieprasījuma. Šī lidojuma izpilde var palīdzēt uzlabot korespondējošo nodokļu darbību ģenerēšanu valstīm un reģioniem, izņemot Taizemi, Poliju, Ungārijui, Lietuvu, Malaiziju, Itāliju, Krieviju, Čehiju, Igauniju un Latviju.

> [!NOTE]
> Ja nodokļu transakciju tabulā ir pielāgoti lauki, nevar aktivizēt lidojuma datus.

Tā kā **PVN/Virsgrāmatas saskaņošanas** pārskats parasti tiek izmantots tikai iekšējās kontroles nolūkiem un nav nepieciešams daudzos nodokļu atvieglojumos, var izvēlēties neģenerēt korespondējošā PVN darbības PVN maksājuma dokumentā.

1. Pārejiet uz sadaļu **Nodokļi** \> **Netiešie nodokļi** \> **PVN** \> **PVN apmaksas periodi**.
2. Atlasiet apmaksas periodu.
3. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Novērst korespondējošo nodokļu darbību ģenerēšanu** uz **Jā**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
