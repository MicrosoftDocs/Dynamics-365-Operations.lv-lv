---
title: Daudzums nav derīgs, reģistrējot ienākošos pasūtījumus
description: 'Ja daudzums, kas ir piešķirts numura zīmei, pārsniedz daudzumu, kas vēl jāsaņem, tiks saņemts kļūdas ziņojums: "Daudzums nav derīgs".'
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5099b320447bf59c72f5017564ea660f19c690a5
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477024"
---
# <a name="license-plate-quantity-is-not-valid-when-registering-inbound-orders"></a>Numuru zīmju daudzums nav derīgs, reģistrējot ienākošos pasūtījumus

## <a name="symptoms"></a>Simptomi

Reģistrējot ienākošos pasūtījumus, var parādīties šāds kļūdas ziņojums:

> Daudzuma vērtība nav derīga.

Ja lauks **Numuru zīmju grupēšanas politika** ir iestatīts uz *Lietotāja definēta* mobilās ierīces izvēlnes elementam, kas tiek izmantots, lai reģistrētu ienākošos pasūtījumus, jūs saņemsit šo kļūdas ziņojumu un nevarēsit pabeigt reģistrāciju.

## <a name="cause"></a>Iemesls

Ja *Lietotājs, kas ir definēts* tiek izmantots kā numura zīmi grupēšanas politika, sistēma ienākošos krājumus sadala atsevišķās numura vienībai, kā norādīts vienību secību grupā. Ja partijas vai sērijas numuri tiek izmantoti, lai izsekotu elementam, kas tiek saņemts, katras partijas vai sērijas daudzumi ir jānorāda katrai reģistrētajai numuru zīmei. Ja daudzums, kas ir piešķirts numura zīmei, pārsniedz daudzumu, kas vēl jāsaņem pašreizējām dimensijām, tiks saņemts šāds kļūdas ziņojums.

## <a name="resolution"></a>Novēršana

Kad reģistrējiet krājumu, izmantojot mobilās ierīces izvēlnes vienumu, kura **Numura zīmi grupēšanas politikas** lauks ir iestatīts uz *Lietotājs, kas ir definēts*, sistēmai var būt nepieciešams apstiprināt vai ievadīt numura zīmi numurus, partijas numurus vai sērijas numurus.

Numura zīmes apstiprinājuma lapā sistēma rādīs daudzumu, kas piešķirts pašreizējai numura zīmei. Partijas vai sērijas apstiprinājuma lapās sistēma rādīs daudzumu, kas ir jāsaņem pašreizējā numura zīmi. Šeit tiks iekļauts arī lauks, kur varat ievadīt daudzumu, ko reģistrēt numura zīmes un paketes vai sērijas numura kombinācijai. Šajā gadījumā pārliecinieties, ka daudzums, kas tiek reģistrēts numura zīmei, nepārsniedz daudzumu, kas vēl ir jāsaņem.

Ja saņemšanas pasūtījuma reģistrācijā tiek ģenerēts pārāk daudz numura zīmju, **Numura zīmes grupēšanas politikas** lauka vērtību var mainīt uz *Numura zīmes grupēšanu*, krājumam var piešķirt jaunu vienību secību grupu vai vienību secību grupas opciju **Numura zīmju grupai** var deaktivizēt.
