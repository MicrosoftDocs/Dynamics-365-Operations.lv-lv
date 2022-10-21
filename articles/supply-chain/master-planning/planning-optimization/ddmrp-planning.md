---
title: Uz pieprasījumu balstīta plānošana
description: Šajā dokumentā ir aprakstīts, kā ģenerēt plānotos pasūtījumus krājumiem, kas iestatīti kā dekompozīcijas punkti.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: f1e2cfca47d507c8de7f9323bb8e4262a0e90949
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689209"
---
# <a name="demand-driven-planning"></a>Uz pieprasījumu balstīta plānošana

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Šajā dokumentā ir aprakstīts, kā ģenerēt plānotos pasūtījumus krājumiem, kas iestatīti kā dekompozīcijas punkti.

## <a name="net-flow-and-qualified-demand"></a>Neto plūsma un kvalificēts pieprasījums

Vispārējās plānošanas laikā sistēma piemēro neto plūsmas koncepciju, lai izveidotu faktisko rīcībā esošo daudzumu, *pamatojoties* uz faktiskajiem rīcībā esošajiem krājumiem, pieskaitot pasūtītos krājumus (esošie piegādes pasūtījumi, kas vēl nav saņemti), *atņemot* to, kas tiek saukts par kvalificētu pieprasījumu (kvalificēta gaidāmā pārdošana), kā parādīts šajā ilustrācijā. Kad sistēma nosaka, kurā bufervietā krājums pieder un kādam jābūt pasūtītam daudzumam, tas novērtē neto plūsmu, nevis faktiskos rīcībā esošos krājumus.

![Neto plūsmas aprēķina diagrammas piemērs.](media/ddmrp-net-flow-example.png "Neto plūsmas aprēķina diagrammas piemērs")

Ja plānotais pasūtījums tiek izraisīts plānošanas izpildes laikā, pasūtītais daudzums būs maksimālais līmenis, kas atņemot neto plūsmu. Lai piešķirtu pasūtījuma prioritāti, sistēma vajadzības datumu vietā [izmanto uz prioritāti](priority-based-planning.md) balstītu plānošanas funkcionalitāti. Pieprasījumam orientētu materiālu prasību plānošana (DDMRP) piešķir plānotā pasūtījuma prioritāti, pamatojoties uz pasūtīto daudzumu kā procentu no maksimālā krājuma. Iepriekšējā ilustrācijā pasūtītais daudzums ir 53 procenti no maksimālā daudzuma. Tādējādi papildināšanas pasūtījuma prioritāte būs 53. (Kontekstam 0 ir augstākā prioritāte, un 100 ir zemākā prioritāte.)

*Kvalificēts* pieprasījums ir pagātnes pieprasījums, plus šodienas pieprasījums, plus kvalificēti pasūtījumu saskaitīumi nākotnē. Šajā attēlā parādīts pieprasījuma līmeņu piemērs šodienai (12. jūnijs) un nākamajām trim dienām. DDMRP ļauj iestatīt pasūtījuma svērtāju, lai identificētu pieprasījumu, kas pārsniedz parastās prognozes. Ja slieksnis ir iestatīts uz 25 gabaliem, divi turpmākie datumi, kas ir redzami ilustrācijā, tiks kvalificēti kā pasūtījumu saīsumi. Pasūtījuma sakrāšanas **slieksnis** katrai precei ir jāpiešķir atsevišķi, izmantojot krājumu vajadzības lapu, [kā aprakstīts Buferu iestatīšana dekompilēšanas punkta krājumam](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

![Kvalificētas pieprasījuma aprēķina diagrammas piemērs.](media/ddmrp-net-qualified-demand-example.png "Kvalificētas pieprasījuma aprēķina diagrammas piemērs")

Ja nav pagātnes pieprasījuma, tagad ir iespējams pievienot šodienas pieprasījumu (18) divu pasūtījumu spikes daudzumiem (29 un 26), lai iegūtu kvalificētu pieprasījumu 73. Kaut arī pastāv pieprasījums 23. jūnijā, ievērojiet, ka tas nav iekļauts neto plūsmas aprēķinā, jo DDMRP izraisa plānoto pasūtījumu atšķirīgi no tradicionālajām plānošanas vajadzību grupām.

## <a name="generating-planned-orders-with-ddmrp"></a>Plānoto pasūtījumu ģenerēšana ar DDMRP

Plānošanas izpildes laikā sistēma izveidos jaunu plānoto pasūtījumu, ja krājuma neto plūsma nomesies zem pārkārtošanas punkta. Ja lietojat DDMRP, plānošanu parasti veic katru dienu. Tādēļ jūs pamatā pārbaudiet krājumu līmeņus reizi dienā, lai noteiktu, kuri krājumi ir jāpapildina.

Šajā ilustrācijā parādīts piemērs situācijai, kad pasūtījums uz 20. jūnija ir 18 gabali, 29 gabali uz 21. jūnija, 26 gabali 22. jūnijā un 20 gabali 23. jūnijā. Ņemot vērā, ka 25 gabalu izspīdēja slieksnis ir iestatīts, divi no šiem pasūtījumiem tiek atzīmēti kā spikeļi. Rīcībā ir 220 šī krājuma vienības.

![1. plānošanas piemērs.](media/ddmrp-planning-example-1.png "1. plānošanas piemērs")

Ja vispārējā plānošana tiek palaista tagad, tiks ģenerēts plānotais pasūtījums, ja ir atrasta neto plūsma, kas nomests zem pasūtījuma pārkārtošanas punkta (šajā piemērā 219 gabali).

![2. plānošanas piemērs.](media/ddmrp-planning-example-2.png "2. plānošanas piemērs")

Šis piemērs izveido plānoto pirkšanas pasūtījumu daudzumam 130, kas ir vienāds ar maksimālo līmeni mīnus neto plūsma. Plānotajam pasūtījumam tiek piešķirta prioritāte 53,07, pamatojoties uz tā procentuālo vērtību no maksimālā daudzuma. Tā kā šīs vērtības tika atrastas 20. jūnijā, sistēma izveido plānoto pasūtījumu, kas datēts ar 20. jūniju plus atšifrēto izpildes laiku krājumam (šajā piemērā piecas darba dienas). Tāpēc, tā kā piecas darba dienas ir no šodienas vienu nedēļu, plānotais pasūtījums ir datēts ar 27. jūniju.

> [!NOTE]
> Optimizācijas plānošana aprēķina tikai dekompozīcijas krājumus, izmantojot DDMRP. Visi pārējie krājumi tiek aprēķināti, izmantojot standarta materiālu prasību plānošanu (MRP).
