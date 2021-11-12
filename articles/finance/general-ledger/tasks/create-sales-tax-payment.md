---
title: PVN maksājuma izveide
description: PVN segšanas un iegrāmatošanas darba procedūra sedz PVN bilances PVN kontos un noteiktajam periodam atlīdzina tās PVN maksājumu kontā.
author: twheeloc
ms.date: 10/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54132ca4775482b4a06ff7e73125e804aff40cb4
ms.sourcegitcommit: f8b597b09157d934b62bd5fb9a4d05b8f82b5a0e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/26/2021
ms.locfileid: "7700117"
---
# <a name="create-a-sales-tax-payment"></a>PVN maksājuma izveide

[!include [banner](../../includes/banner.md)]

PVN segšanas un iegrāmatošanas darba procedūra sedz PVN bilances PVN kontos un noteiktajam periodam atlīdzina tās PVN maksājumu kontā.

1. Dodieties uz **Nodokļi > Deklarācijas > PVN > Nosegt un grāmatot PVN**.
2. Laukā **Nomaksas periods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Ievadiet datumu laukā **No datuma**.
    - Ja lapā **Virsgrāmatas parametri** neatlasīsiet opciju **Iekļaut labojumus**, segšanu var apstrādāt dažādām versijām. Oriģināls ir pirmais maksājums perioda intervālā, un to perioda intervālam var apstrādāt tikai vienu reizi. Jaunākie labojumi nosegs PVN transakcijas, kas ir iegrāmatotas pēc oriģinālās versijas izveides.
5. Ievadiet datumu laukā **Transakcijas datums**.
6. Noklikšķiniet uz **Labi**.

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
