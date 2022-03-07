---
title: Iespējot debitora atdošanas paziņojumus pārdošanas punktā (POS)
description: Šajā tēmā ir aprakstīts, kā iespējot debitoru atdošanas paziņojumus Microsoft Dynamics 365 Commerce pārdošanas punktā (POS).
author: bicyclingfool
ms.date: 12/03/2021
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
ms.openlocfilehash: 320e9d73ca98bf4ed22ac9bdff2fc34ae83223ec
ms.sourcegitcommit: 5f5a8b1790076904f5fda567925089472868cc5a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891416"
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

Pievienojiet saiti vai pogu veidnei, kas ir kartēta uz paziņojuma veidu **Iepakošanas pabeigšana** un piegādes veidu, ko izmantojat, lai novērstu pasūtījuma izpildi. Veidnē izveidojiet HTML saiti vai pogu, kas norāda uz jūsu izveidotās reģistrēšanās apstiprinājuma lapas URL un kas ietver parametru nosaukumus un vērtības, kā parādīts nākamajā piemērā.

`<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%confirmationid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>`

Papildinformāciju par e-pasta veidņu konfigurēšanu skatiet sadaļā [Transakciju e-pasta ziņojumu pielāgošana piegādes režīmā](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>POS ir izveidots pārbaudes apstiprināšanas uzdevums

Pēc tam, kad klients ir paziņos veikalam, ka atrodas uz paņemšanu, reģistrēšanās lapā tiek parādīts apstiprinājuma ziņojums un neobligāts QR kods, kas satur klienta pasūtījuma apstiprinājuma ID. Tajā pašā laikā uzdevums tiek izveidots POS uzdevumu sarakstā veikalam, kurā klients paņem pasūtījumu. Šis uzdevums satur visu klienta un pasūtījuma informāciju, kas nepieciešama pasūtījuma izpildei. Uzdevuma instrukciju laukā ir norādīta visa informācija, kas iegūta no klienta, izmantojot papildinformācijas veidlapu.

## <a name="end-to-end-testing"></a>Testēšana no gala līdz galam

Lai reģistrētos klients, noteikti parametri un vērtības ir jānodod reģistrēšanās lapai un pēc tam klientu reģistrēšanās API. Tāpēc vienkāršākā pieeja ir pārbaudīt funkciju vidē, kurā var izveidot un iepakot testa pasūtījumu. Tādā veidā var ģenerēt e-pasta ziņojumu "pasūtījums gatavs savākšanai", kura URL satur nepieciešamos parametru nosaukumus un vērtības.

Lai pārbaudītu klienta reģistrēšanās līdzekli, rīkojieties šādi.

1. Izveidojiet debitora reģistrēšanās lapu un pēc tam pievienojiet un konfigurējiet debitoru reģistrēšanās moduli. Plašāku informāciju skatiet [Check-in for pickup module](check-in-pickup-module.md). 
1. Atdetiet lapu, bet nepublicējiet to.
1. Pievienojiet šo saiti e-pasta veidnei, uz kuru savākšanas veidam tiek izsaukts pilns iepakojuma paziņojuma tips. Papildinformāciju skatiet rakstā [E-pasta veidņu izveide darījumu notikumiem](email-templates-transactions.md).

    - **Pirmsražošanas (UAT) vidēm:** pievienojiet koda fragmentu no [sadaļas Konfigurēt transakciju e-pasta veidni](#configure-the-transactional-email-template) šīs tēmas sākumā.
    - **Ražošanas vidēm:** pievienojiet šādu komentētu kodu, lai netiktu ietekmēti esošie klienti.

        `<!-- https://[DOMAIN]/[CHECK_IN_PAGE]?channelReferenceId=%confirmationid%&channelId=%pickupchannelid%&packingSlipId=%packingslipid%&preview=inprogress -->`

1. Izveidojiet pasūtījumu, kurā ir norādīts saņemšanas veids.
1. Kad saņemat e-pasta ziņojumu, ko aktivizē iepakojuma pilns paziņojuma veids, pārbaudiet reģistrēšanās plūsmu, atverot reģistrēšanās lapu, kurai ir iepriekš pievienotais URL. Tā kā vietrādī URL ir `&preview=inprogress` iekļauts karodziņš, pirms lapas skatīšanas jums tiks piedāvāts autentificēties.
1. Ievadiet papildu informāciju, kas nepieciešama moduļa konfigurēšanai.
1. Pārbaudiet, vai reģistrēšanās apstiprinājuma skats ir parādīts pareizi.
1. Atveriet POS termināli veikalam, kurā tiks paņemts pasūtījums.
1. Atlasiet **elementu Pasūtījumi, lai paņemtu,** un pārbaudiet, vai pasūtījums tiek parādīts.
1. Pārbaudiet, vai detalizētas informācijas rūtī tiek parādīta papildu informācija, kas tika konfigurēta reģistrēšanās modulī.

Kad esat pārliecinājies, ka klientu reģistrēšanās līdzeklis darbojas no beigām līdz beigām, veiciet tālāk norādītās darbības.

1. Publicēt reģistrēšanās lapu.
1. Ja testējat ražošanas vidē, atvienojiet URL e-pasta veidnē "Pasūtīt gatavs savākšanai", lai **tiktu parādīta saite Vai poga Es esmu** šeit. Pēc tam atkārtoti ielādējiet veidni.

## <a name="additional-resources"></a>Papildu resursi

[Izdošanas moduļa atdošana](check-in-pickup-module.md)

[Darījumu e-pasta ziņojumu pielāgošana pēc piegādes veida](customize-email-delivery-mode.md)

[E-pasta ziņojumu veidņu izveide transakciju notikumiem](email-templates-transactions.md)
