---
title: Iespējot debitora atdošanas paziņojumus pārdošanas punktā (POS)
description: Šajā tēmā ir aprakstīts, kā iespējot debitoru atdošanas paziņojumus Microsoft Dynamics 365 Commerce pārdošanas punktā (POS).
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e4defc15d9ef198a361934d51e31016747dbb5ab
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937600"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Iespējot debitora atdošanas paziņojumus pārdošanas punktā (POS)

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā ir aprakstīts, kā iespējot debitoru atdošanas paziņojumus Microsoft Dynamics 365 Commerce pārdošanas punktā (POS).

Organizācijas savos e-pasta ziņojumos "pasūtījums ir gatavs savākšanai", var nodrošināt saiti vai pogu, kas ļauj debitoriem paziņot veikalam, ka viņi atrodas uz vietas, un gaida, kad viņu pakotne tiks iznesta. Pēc tam debitori saņem reģistrēšanās apstiprinājumu, un veikals savā POS programmā saņem paziņojumu kā uzdevumu. Šis uzdevums kalpo kā uzvedne pārdošanas piesaistēm, lai piegādātu pasūtījumu debitoram transportlīdzeklim. Tādēļ debitoram nav jāievada veikals.

Debitora reģistrēšanās darbplūsmu var konfigurēt, lai apkopotu papildu informāciju no debitoriem, piemēram, viņu stāvvietas numuru, transportlīdzekļa izgatavotāju, modeli un krāsu un piegādes instrukcijas. Mazumtirdzniecības veikala grāmatvedis var izmantot šo informāciju, lai atvieglotu pasūtījuma izpildi.

## <a name="enable-customer-check-in"></a>Iespējot debitora atdošanu

Ja debitora reģistrēšanās līdzeklis ir ieslēgts, Commerce ģenerē pasūtījuma apstiprinājuma ID (zināms arī kā kanāla atsauces ID). Tas ģenerē arī pasūtījumu apstiprinājumu ID pasūtījumiem, kas ir izveidoti, izmantojot pārdošanas punkta (POS) vai zvanu centra kanālus. 

Lai ieslēgtu debitoru atdošanas līdzeki Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Dodieties uz **Darbvietas \> Līdzekļu pārvaldība**.
2. Meklējiet līdzekli **Izveidot konsekventu kanāla atsauces ID formātu vairākos kanālos**. 
3. Atlasiet līdzekli un pēc tam rekvizītu rūtī atlasiet **Iespējot tūlīt**. 

## <a name="create-a-check-in-confirmation-page"></a>Izveidot atdošanas apstiprināšanas lapu

Jūsu e-komercijas vietnē jums ir jāizveido jauna lapa, kas kalpos kā pārbaudes apstiprinājumu pieredze. Izmantojot papildu konfigurāciju, lapa var arī iekļaut formu, kas ievāc papildu informāciju no debitoriem, lai atvieglotu pasūtījuma izpildi. Papildinformāciju par lapas un moduļa iestatīšanas veidu skatiet [Debitoru atdošanas modulī](check-in-pickup-module.md).

## <a name="configure-the-transactional-email-template"></a>Transakciju e-pasta veidnes konfigurēšana

Šeit ir jāpievieno **Esmu šeit** saite vai poga veidnei, kas ir pieejama transakciju e-pasta ziņojumā, ko debitori saņem, kad viņu pasūtījums ir gatavs saņemšanai. Debitori izmantos šo saiti vai pogu, lai paziņotu veikalam, ka ir atnākuši saņemt pasūtījumu. 

Pievienojiet saiti vai pogu veidnei, kas ir kartēta uz paziņojuma veidu **Iepakošanas pabeigšana** un piegādes veidu, ko izmantojat, lai novērstu pasūtījuma izpildi. Veidnē izveidojiet HTML saiti vai pogu, kas norāda uz jūsu izveidotās apstiprināšanas lapas URL. Tālāk ir minēts piemērs.

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
Papildinformāciju par e-pasta veidņu konfigurēšanu skatiet sadaļā [Transakciju e-pasta ziņojumu pielāgošana piegādes režīmā](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>POS ir izveidots pārbaudes apstiprināšanas uzdevums

Kad debitors paziņo veikalam, ka ir klāt saņemšanai, viņi saņem saņemšanas apstiprinājuma paziņojumu, un uzdevums tiek izveidots uzdevumu sarakstā POS veikalam, kur debitors saņem pasūtījumu. Uzdevumā ietverta visa informācija par debitoru un pasūtījumu, kas nepieciešama pasūtījuma izpildei. Uzdevumu norādījumu laukā ir parādīta jebkura informācija, kas apkopota no debitora, izmantojot papildinformācijas formu. 

## <a name="additional-resources"></a>Papildu resursi

[Izdošanas moduļa atdošana](check-in-pickup-module.md)
