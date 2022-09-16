---
title: 'Asinhronā debitora izveides režīms: bieži uzdotie jautājumi'
description: Šajā rakstā ir sniegtas atbildes uz bieži uzdotiem jautājumiem par asinhrono debitora izveidošanas režīmu Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: bd5741aeb3278f1d40d63bb02ca57571a907dc21
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474074"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>Asinhronā debitora izveides režīms: bieži uzdotie jautājumi

[!include [banner](includes/banner.md)]

Šajā rakstā ir sniegtas atbildes uz bieži uzdotiem jautājumiem par asinhrono (async) debitoru izveides režīmu Microsoft Dynamics 365 Commerce.

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>Kādēļ nevar iespējot līdzekli Iespējot debitoru rediģēšanu asinhronā režīmā?

Pirms iespējot Iespējot debitoru **rediģēšanu asinhronajā režīmā**, jāiespējo šādas funkcijas:

- Debitoru pasūtījumu un debitoru darbību veiktspējas uzlabojumi
- Iespējot uzlabotu Async debitoru izveidi
- Iespējot klientu adrešu asinhrono izveidi

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>Kādēļ joprojām tiek skatīti reāllaika pakalpojumu izsaukumi, kas tika veikti Commerce Headquarters pēc tam, kad ir iespējota funkcija Iespējot debitoru rediģēšanu asinhronā režīmā?

Šī problēma rodas, Commerce Data Exchange kad (CDX) darbi netika palaisti, lai nodrošinātu, ka līdzekļu stāvoklis un citi kanāla metadati tiek sinhronizēti ar kanālu. Pirms scenārija atkārtotas mēģinājuma nodrošiniet, lai programmā Commerce Headquarters tiktu palaisti šādi CDX darbi:

- 1110 (Globālā konfigurācija)
- 1010 (Debitori)
- 1070 (Kanāla konfigurācija)

Dati, kas ir kešoti Commerce Scale Unit (CSU) programmā, var nebūt tūlīt noteikti programmā Commerce Headquarters pēc CDX darbu izpildes.

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>Kādēļ programmā Commerce Headquarters netiek rādīta debitora izveide vai atjauninājumi no pārdošanas punkta (POS) vai e-komercijas kanāla?

Pārliecinieties, ka šīs darbības ir veiktas tādā secībā, kā tās uzskaitītas šeit.

1. Palaidiet CDX P-darbu programmā Commerce Headquarters **, lai nodrošinātu, ka tabulās RETAILASYNCCUSTOMERV2, RETAILASYNCADDRESSV2** **,** **RETAILASYNCCUSTOMERCONTACT**, **RETAILASYNCCUSTOMERAFFILIATION** **un RETAILASYNCCUSTOMERATTRIBUTEV2 ir pieejami retailASYNCCUSTOOMEREV2** dati.
1. Palaidiet programmu **Sinhronizēt debitorus un kanālu pieprasījumu pakešuzdevumu** programmā Commerce Headquarters. Pēc veiksmīgas pakešuzdevuma izpildes visiem ierakstiem **, kas ir veiksmīgi apstrādāti no iepriekš minētajām tabulām, būs iestatīts lauks OnlineOperationCompleted** uz **1**.
