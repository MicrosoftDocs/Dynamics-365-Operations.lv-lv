---
title: Papildināšanas metodes un daudzuma modificēšana
description: Šajā tēmā ir sniegta informācija par papildināšanas metodēm un Plānošanas optimizāciju. Tajā skaidrots arī, kā preces vairāku pasūtījumu daudzums ietekmē rezultātu.
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261700"
---
# <a name="replenishment-methods-and-quantity-modification"></a>Papildināšanas metodes un daudzuma modificēšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegta informācija par papildināšanas metodēm un Plānošanas optimizāciju. Tajā skaidrots arī, kā preces vairāku pasūtījumu daudzums ietekmē rezultātu.

Papildināšanas metodes pazīstamas arī kā pārklājuma metodes un laidiena izmēru metodes.

## <a name="coverage-codes"></a>Vajadzības kodi

Plānošanas optimizāciju var konfigurēt tā, lai izmantotu dažādas papildināšanas metodes. Papildināšanas metodes ir metodes, ko sistēma izmanto, lai aprēķinātu preces prasības. Papildināšanas metodes tiek definētas pēc vajadzības kodiem, kurus var iestatīt vajadzību grupai vai precei.

Šie vajadzību kodi var tikt izmantoti Plānošanas optimizācijā:

- **Periods** – papildināšanas metode, kas apvieno visu perioda pieprasījumu vienā pasūtījumā šai precei. Pasūtījums tiks plānots pirmajai perioda dienai, un tā daudzums atbilstīs neto prasībām noteiktajā periodā. Periods sākas ar preces pirmo pieprasījumu un sedz noteikto laika periodu. Nākamais periods sāksies ar nākamās preces prasībām. Vajadzības kods *Periods* bieži tiek izmantots neprognozējamu krājumu izvelkšanai, sezonas ietekmējamām precēm vai augstas izmaksas precēm. Tālāk redzamajā attēlā parādīts piemērs.

    ![Perioda vajadzības koda izmantošanas piemērs](./media/coverage-code-period.png "Perioda vajadzības koda izmantošanas piemērs")

- **Prasība** – papildināšanas metode, saskaņā ar kuru sistēma izveido plānoto pirkšanas, pārsūtīšanas vai ražošanas pasūtījumu preces prasību. Šī metode tiek izmantota dārgam precēm, kam ir intermitējošs pieprasījums. Vajadzības kods *Prasība* bieži tiek izmantots konfigurējamām precēm vai pasūtījumā veidotiem scenārijiem. Tālāk redzamajā attēlā parādīts piemērs.

    ![Prasības vajadzības koda izmantošanas piemērs](./media/coverage-code-requirement.png "Prasības vajadzības koda izmantošanas piemērs")

- **Min./maks.** – Papildināšanas metode ir balstīta uz krājumu līmeni. Tā definē krājumu papildināšanu līdz noteiktam līmenim, kad paredzamais rīcībā esošo krājumu līmenis ir zem noteikta sliekšņa. Papildināšanas daudzums būs vienāds ar starpību starp maksimālo līmeni un prognozēto rīcībā esošo līmeni. Vienība *Min./maks.* vajadzības kods bieži tiek izmantots paredzamu krājumu izvelkšanai, labākām precēm vai lētākām precēm. Tālāk redzamajā attēlā parādīts piemērs.

    ![Min./Maks. vajadzības koda izmantošanas piemērs](./media/coverage-code-min-max.png "Min./Maks. vajadzības koda izmantošanas piemērs")

- **Manuāla** – papildināšanas metode, kad sistēma neiesaka precei pirkšanas, pārsūtīšanas vai ražošanas pasūtījumus. Tā vietā produkta plānotājs ir atbildīgs par nepieciešamo pasūtījumu izveidi preces papildināšanai. Vajadzības kods *Manuāls* bieži tiek izmantots precēm, kurām nav vajadzīgi sistēmas ģenerētie plānotie pasūtījumi.

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a>Pasūtījuma daudzuma ietekme no noklusējuma pasūtījuma iestatījumiem

Izlaistai precei lapā **Noklusējuma pasūtījuma iestatījumi** varat norādīt katru no šiem daudzuma iestatījumiem kopsavilkuma cilnēs **Pirkšanas pasūtījums**, **Krājumi** un **Pārdošanas pasūtījums**. (Kopsavilkuma cilne **Krājumi** tiek izmantota gan pārsūtīšanas, gan ražošanas pasūtījumiem.)

- **Daudzkārtīgi** – plānotie pasūtījumi būs daudzkārtīgi no šī daudzuma.

    Piemēram, ja lauks **Daudzkārtīgi** ir iestatīts uz *5*, pasūtījums var būt ar daudzumu 5, 10, 15, 20 un tā tālāk.

- **Min. pasūtījuma daudzums** – plānotie pasūtījumi nebūs mazāki par norādīto vērtību.

    Piemēram, ja lauks **Min. pasūtījuma daudzums** ir iestatīts uz *10*, tiks izveidots plānotais pasūtījums daudzumam 10, pat ja pieprasījuma izpildei nepieciešami tikai četri.

- **Maks. pasūtījuma daudzums** – plānotie pasūtījumi nebūs lielāki par norādīto vērtību. Ja pieprasījums ir lielāks nekā vērtība **Maks. pasūtījuma daudzums**, tiks izveidoti vairāki plānotie pasūtījumi, lai to nosegtu.

    Piemēram, ja lauks **Maks. pasūtījuma daudzums** ir iestatīts uz *100* un pieprasījums ir 450, tiks izveidoti četri plānotie pasūtījumi daudzumam 100 un viens plānotais pasūtījums daudzumam 50.

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a>Papildināšanas piemēri, kas izmanto Min./Maks. vajadzības kods

Ja precei laukā **Daudzkārtīgi** nav norādīta vērtība lapā **Noklusējuma pasūtījuma iestatījumi** un ja izmantojat *Min./Max.* papildināšanas metodi, Plānošanas optimizācija papildinās krājumus līdz noteiktam līmenim, kad paredzamais rīcībā esošo krājumu līmenis ir zem noteikta sliekšņa.

Ja precei definējat vairākus daudzumus, *Min./Maks.* papildināšanas metode maina tās darbību un ņem vērā vērtību **Daudzkārtīgi**.

Citiem vārdiem sakot, Plānošanas optimizācija joprojām papildinās krājumus līdz definētajam maksimālajam līmenim, ja prognozētais rīcībā esošo krājumu līmenis ir mazāks par noteikto minimālo līmeni. Tomēr papildināšanas daudzumam jābūt daudzkārtīgai vērtībai **Daudzkārtīgi**.

Ja papildināšanas daudzums (starpība starp maksimālo līmeni un prognozēto rīcībā esošo līmeni) nedalās ar definēto daudzkārtēju daudzumu, Plānošanas optimizācija izmanto pirmo iespējamo vērtību, kas kopā ar prognozēto rīcībā esošo līmeni būs zem maksimālā līmeņa. Ja summa ir mazāka par minimālo līmeni, Plānošanas optimizācija izmanto pirmo vērtību, kas kopā ar prognozējamu rīcībā esošo, būs virs maksimālā līmeņa.

Sekojošās apakšsadaļas sniedz dažus piemērus, kas parāda, kā daudzkārtēju pasūtījumu daudzums precei ietekmē rezultātu *Min./Max.* papildināšanas metode.

### <a name="example-1"></a>1. piemērs

Precei ir šāda konfigurācija:

- **Vajadzību kods:** *Min./Max.*
- **Minimums:** *15*
- **Maksimums:** *22*
- **Daudzkārtīgi:** *0*

Precei ir 10 rīcībā esošo krājumu vienības, un nav cita pieprasījuma vai piedāvājuma.

Kad tiek palaista vispārējā plānošana, tiek izveidots plānotais pasūtījums 12 gabaliem, lai papildinātu krājumus līdz maksimālām daudzumam.

### <a name="example-2"></a>2. piemērs

Precei ir šāda konfigurācija:

- **Vajadzību kods:** *Min./Max.*
- **Minimums:** *15*
- **Maksimums:** *22*
- **Daudzkārtīgi:** *5*

Precei ir 10 rīcībā esošo krājumu vienības, un nav cita pieprasījuma vai piedāvājuma.

Kad tiek palaista vispārējā plānošana, tiek izveidots plānotais pasūtījums 10 gabaliem (jo 15 papildināšanas gabali plus 10 rīcībā esošo krājumu vienības pārsniegs maksimālo daudzumu).

### <a name="example-3"></a>3. piemērs

Precei ir šāda konfigurācija:

- **Vajadzību kods:** *Min./Max.*
- **Minimums:** *21*
- **Maksimums:** *24*
- **Daudzkārtīgi:** *5*

Precei ir 10 rīcībā esošo krājumu vienības, un nav cita pieprasījuma vai piedāvājuma.

Kad tiek palaista vispārējā plānošana, tiek izveidots plānotais pasūtījums 15 gabaliem (jo 10 papildināšanas gabali plus 10 rīcībā esošo krājumu vienības nesasniegs minimālo daudzumu).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
