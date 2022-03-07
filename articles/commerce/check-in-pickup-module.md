---
title: Izdošanas moduļa atdošana
description: Šis temats attiecas uz izdošanas moduļa atdošanu un tajā tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e7bae4ae7c2f3367132b03accb31c01c5f3b673e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937601"
---
# <a name="check-in-for-pickup-module"></a>Izdošanas moduļa atdošana

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šis temats attiecas uz izdošanas moduļa atdošanu un tajā tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.

Izdošanas moduļa atdošana nodrošina apstiprinājuma lapu klientiem, kuri izmanto Dynamics 365 Commerce klientu izdošanas iespējas, lai paziņotu veikalam par to ierašanos. Izdošanas moduļa atdošana arī ļauj konfigurēt veidlapu, kas ievāc papildu informāciju no debitoriem, lai atvieglotu pasūtījuma piegādi. Šī informācija ietver debitora auto novietošanas vietas numuru un tā transportlīdzekļa izgatavotāju un modeli. 

## <a name="module-properties"></a>Moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | Apraksts |
|---------------|--------|-------------|
| Apstiprinājuma teksts | Teksta virkne | Virsraksta saturs, kas tiek parādīts atdošanas apstiprināšanas lapā. |
| Rādīt QR kodu | **Patiess** vai **Nepatiess** | Ja šis rekvizīts ir iestatīts kā **Patiess**, atdošanas apstiprināšanas lapa rāda QR kodu, kas norāda pasūtījuma apstiprinājuma ID. |
| Papildinformācijas virsraksts | Teksta virkne | Virsraksta saturs, kas tiek parādīts, konfigurējot papildu informācijas laukus. |
| Papildinformācijas atslēgas | Resursa ID/resursu vērtību pāris | Katra atslēga izveido veidlapas lauku un saistīto iezīmi, kas tiek izmantota, lai apkopotu papildinformāciju no debitoriem. |
| Papildinformācijas atslēgas \> Resursa ID | Teksta virkne | Katra informācijas atslēga izveido veidlapas lauku un saistīto iezīmi, kas tiek izmantota, lai apkopotu papildinformāciju no debitoriem. Šis rekvizīts identificē papildinformācijas atslēgu. Uzdevumā, kas ir izveidots pārdošanas punktā (POS), šī rekvizīta vērtība tiek parādīta instrukcijas laukā kā etiķete. |
| Papildinformācijas atslēgas \> Resursa vērtība | Teksta virkne | POS uzdevuma teksta lauka iezīme. |
| Papildinformācijas atslēgas \> Obligāti | **Patiess** vai **Nepatiess** | Šis rekvizīts norāda, vai pirms turpināšanas debitoriem ir jāaizpilda veidlapas lauks. Kad šis rekvizīts ir iestatīts uz **Patiess**, līdz veidlapas etiķetei tiek atveidota zvaigznīte, un tiek veikta nulles pārbaude, lai neļautu debitoriem turpināt darbu, ja nav ievadīta vērtība. |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a>Izdošanas moduļa atdošanas pievienošana lapai

Izdošanas moduļa atdošanu jāpievieno jaunajai lapai, ko izveidojat atdošanas apstiprinājumam. Šī lapa kalpos kā atdošanas apstiprinājumu pieredze klientiem, kuri atlasīs saiti vai pogu **Esmu šeit** e-pasta ziņojumā. 

## <a name="configure-the-additional-information-form"></a>Papildu informācijas veidlapas konfigurēšana

Pēc noklusējuma, ja nav konfigurētas papildu informācijas atslēgas, modulis rāda debitoriem atdošanas apstiprināšanas lapu. Kad tiek rādīts atdošanas apstiprinājums, POS tiek izveidots uzdevums veikalam, kur pasūtījums tiek izdots.

Konfigurējot vienu vai vairākas informācijas atslēgas, debitoriem vispirms tiek parādīta uzvedne ar aicinājumu ievadīt informāciju. Kad tiek atlasīts **Iesniegt**, tiem tiek rādīts atdošanas apstiprinājums un POS tiek izveidots uzdevums. 

## <a name="additional-resources"></a>Papildu resursi

[Iespējot debitora atdošanas paziņojumus pārdošanas punktā (POS)](enable-customer-check-in.md)
