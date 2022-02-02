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
ms.openlocfilehash: 95b4e3a1750cf072db919492f7445e87654701da
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983165"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Iespējot debitora atdošanas paziņojumus pārdošanas punktā (POS)

[!include [banner](includes/banner.md)]

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

Pievienojiet saiti vai pogu veidnei, kas ir kartēta uz paziņojuma veidu **Iepakošanas pabeigšana** un piegādes veidu, ko izmantojat, lai novērstu pasūtījuma izpildi. Veidnē izveidojiet HTML saiti vai pogu, kas norāda uz url jūsu izveidotajā pārbaudes apstiprinājuma lapā, kas ietver parametru nosaukumus un vērtības, kā parādīts šajā piemērā.

`<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%confirmationid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>`

Papildinformāciju par e-pasta veidņu konfigurēšanu skatiet sadaļā [Transakciju e-pasta ziņojumu pielāgošana piegādes režīmā](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>POS ir izveidots pārbaudes apstiprināšanas uzdevums

Kad debitors informē veikalu, ka tas ir klātesošs savākšanai, atdīšanas lapa rāda apstiprinājuma ziņojumu un neobligātu QR kodu, kas ietver debitora pasūtījuma apstiprinājuma ID. Tajā pašā laikā uzdevums tiek izveidots POS uzdevumu sarakstā veikalam, kur debitors izdod pasūtījumu. Šis uzdevums ietver visu debitora un pasūtījuma informāciju, kas nepieciešama pasūtījuma izpildei. Uzdevuma instrukciju laukā ir parādīta jebkura informācija, kas apkopota no debitora, izmantojot papildinformācijas formu.

## <a name="end-to-end-testing"></a>Beigu testēšana

Debitora reģistrēšanās pieprasa, lai noteikti parametri un vērtības tiktu nodotas atdēšanas lapai un pēc tam debitora reģistrēšanās API. Tāpēc visvieglāk izmantotā pieeja ir pārbaudīt funkciju vidē, kurā var izveidot un iepakot testa pasūtījumu. Šādā veidā var tikt izveidots e-pasta ziņojums "Pasūtījums gatavs savākšanai", kam ir vietrādis URL, kurā ir ietverti nepieciešamie parametru nosaukumi un vērtības.

Lai pārbaudītu debitora reģistrēšanās līdzekli, sekojiet šiem soļiem.

1. Izveidojiet debitora atdlapas lapu un tad pievienojiet un konfigurējiet debitora atdlapas moduli. Papildinformāciju skatiet [savākšanas moduļa atdākšanas modulī](check-in-pickup-module.md). 
1. Atdot lapā, bet nepublicēt to.
1. Pievienojiet tālāk norādīto saiti e-pasta veidnei, kas tiek izsaukta, izmantojot iepakojuma pabeigšanas paziņojuma veidu piegādes savākšanas režīmam. Papildinformāciju skatiet sadaļā [E-pasta veidņu izveide transakciju notikumiem](email-templates-transactions.md).

    - **Pirms-ražošanas (UAT) vidēm: pievienojiet koda fragmentu no iepriekš šīs tēmas sadaļas Darbības e-pasta**[veidnes](#configure-the-transactional-email-template) konfigurēšana.
    - **Ražošanas vidēm: pievienojiet** šādu komentāra kodu, lai esošie debitori nebūtu ietekmēti.

        `<!-- https://[DOMAIN]/[CHECK_IN_PAGE]?channelReferenceId=%confirmationid%&channelId=%pickupchannelid%&packingSlipId=%packingslipid%&preview=inprogress -->`

1. Izveidojiet pasūtījumu, kur norādīts piegādes izdošanas režīms.
1. Kad saņemat e-pasta ziņojumu, kas ir izraisīts, izmantojot iepakojuma pabeigšanas paziņojuma veidu, pārbaudiet atdošanas plūsmu, atverot atdošanas lapu, kam iepriekš tika pievienots URL. Tā kā URL ietver karodziņu, pirms lapas skatīšanas jums tiks parādīta uzvedne `&preview=inprogress` autentifikācijai.
1. Ievadiet jebkādu papildinformāciju, kas nepieciešama moduļa konfigurēšanai.
1. Pārbaudiet, vai atd apstiprināšanas skats tiek rādīts pareizi.
1. Atveriet POS termināli veikalam, kur tiks saņemts pasūtījums.
1. Atlasiet **pasūtījumus elementa** izvēlei un pārbaudiet, vai pasūtījums parādās.
1. Apstipriniet, ka detalizētas informācijas rūtī parādās jebkāda papildinformācija, kas tika konfigurēta atdotajā modulī.

Pēc tam, kad esat pārbaudījis, ka debitora reģistrēšanās līdzeklis darbojas no beigu datuma līdz beigām, sekojiet šiem soļiem.

1. Publicēt atdlapu.
1. Ja testēsiet ražošanas vidē, noņemiet URL e-pasta veidnē "Pasūtījums gatavs savākšanai", lai tiek parādīta saite vai **poga**. Pēc tam atkārtoti ielādēt veidni.

## <a name="additional-resources"></a>Papildu resursi

[Izdošanas moduļa atdošana](check-in-pickup-module.md)

[Darījumu e-pasta ziņojumu pielāgošana pēc piegādes veida](customize-email-delivery-mode.md)

[E-pasta ziņojumu veidņu izveide transakciju notikumiem](email-templates-transactions.md)
