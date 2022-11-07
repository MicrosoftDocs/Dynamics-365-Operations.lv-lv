---
title: Norēķināšanās moduļa kļūdas atsauces kodi
description: Šajā rakstā ir aprakstītas pārbaudes moduļa kļūdu atsauces kodi, kas ir parādīti uz lietotājam uzvērstos kļūdu ziņojumos Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 952cb932522b4e0bb91be985e4f8974cb6cd8bc0
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728250"
---
# <a name="checkout-module-error-reference-codes"></a>Norēķināšanās moduļa kļūdas atsauces kodi

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā rakstā aprakstīti pārbaudes moduļa kļūdu kodi, kas ir parādīti uz lietotājam uzvērstos kļūdu ziņojumos Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce Ir ieviestas standartizētas kļūdu atsauces, kas var būt ietvertas tiešsaistes kanāla pārbaudes kļūdās, kas tiek iesniegtas tiešsaistes klientiem. Commerce versijā 10.0.31 vai jaunākā versijā kļūdu ziņojumi pārbaudes modulī ietver kļūdu kodus un nerāda nevajadzīgo informāciju tiešsaistes debitoram. Kļūdu kodi attiecas uz šajā rakstā detalizētām kļūdām.

Atkarībā no radušās kļūdas, šī raksta tabulā ir ietverta šāda detalizēta informācija:

- Tā nosacījuma apraksts, kas radīja kļūdu, vai papildu informācija
- Informācija, kas ir jāņem vērā vidē vai maksājumu savienotāja konfigurācijās
- Informācija, uz kuru var atsaukties atbalsta gadījumā, ja nepieciešama papildu palīdzība

## <a name="prerequisites"></a>Priekšnosacījumi

Lai iespējotu pārbaudes moduļa kļūdu atsauces kodus, kas uzskaitīti tālāk, vietnes veidotājā jūsu vietnei, **dodieties uz Vietnes iestatījumu paplašinājumi un \>** sadaļā Grozs **un paņemiet atlasiet** Iespējot uzlaboto tiešsaistes kanāla kļūdu parādīšanas ziņojumapmaiņu **.** 

## <a name="checkout-module-error-reference-codes"></a>Norēķināšanās moduļa kļūdas atsauces kodi

Izmantojiet šo tabulu, lai iegūtu detalizētu informāciju par kļūdas koda atsaucēm, ko nodrošina debitori vai kas radās tiešsaistes veikalā. Ritināt pa labi, lai skatītu kļūdas **apraksta kolonnu**.

| Kļūdas kods | Dynamics savstarpēji nesaistītas kļūdas kods | Kļūdas apraksts |
| ---------- | ------------------------------ | ----------------- |
| CCR001(S)     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ UnableToAuthorizePaymentCardTypeMissingOrNotSupported | Maksājumu nevarēja autorizēt. Nav norādīts kartes tipa ID **, kas ir norādīts TokenizedPaymentCard**, vai arī netiek atbalstīts kartes tipa ID. |
| CCR002     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ UnableToAuthorizePayment | Noraidīts. Maksājumu nevarēja autorizēt. |
| CCR003     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ UnableToAuthorizePaymentCardAdditionalContextRequired | Maksājumu nevarēja autorizēt. No debitora pieprasītā papildinformācija. |
| CCR004     | Microsoft\_ Dynamics\_ Commerce Runtime\_\_ UnableToRetriardCardPaymentAcceptResult | Diemžēl radās problēma. Nevarēja iegūt kartes maksājuma saņemšanas rezultātu. Mēģiniet vēlreiz vai sazinieties ar sistēmas administratoru. |
| CCR005     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ PaymentRequiresMerchantProperties | Nav iespējams veikt maksājumu, jo nav tirgotāja maksājuma rekvizītu. Sazinieties ar sistēmas administratoru. |
| CCR006     | Microsoft\_ Dynamics\_ Commerce Runtime\_\_ InvalidPaymentRequest | Nevar izgūt operācijas norēķinu pakalpojumu. Pārbaudiet atlasītā norēķinu veida maksāšanas metodes iestatījumus. |
| CCR007     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ MultipleCustomerAccountPaymentsNotAllowed | Debitora konta maksājums jau ir lietots, un katrai darbībai drīkst būt tikai viens maksājums. |
| CCR008     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ CustomerAccountLimitSignDifferentFromAmountDue | Debitora konta limits atšķiras no apmaksas summas. Pamēģiniet citu maksāšanas metodi vai sazinieties ar klientu atbalsta dienestu, lai saņemtu palīdzību. |
| CCR009     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ CustomerAccountPaymentExceedsTotalAmountForCarryOutAndReturnItems | Debitora konta maksājums pārsniedz kopējo apmaksu sarakstā iekļautajiem vienumiem. Vēlāk mēģiniet vēlreiz vai sazinieties ar klientu atbalsta dienestu, lai saņemtu palīdzību. |
| CCR010     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ PaymentUsingUnauthorizedAccount | Debitora konta maksājumam ir nepieciešams sava konts vai atbilstošs rēķina konts norēķinu rindā. |
| CCR011     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ CustomerAccountPaymentExceedsCustomerAccountFloorLimit | Pašlaik nevar apstrādāt debitora konta maksājumu — pārsniegta minimālā robežas vērtība. |
| CCR012     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ CustomerAccountPaymentForCustomerWithoutAllowOnAccount | Šim debitoram nav atļauts apmaksāt starpkontu. |
| CCR013     | Microsoft\_ Dynamics\_ Commerce Runtime\_\_ UnableToCancelPayment | Diemžēl radās problēma. Maksājumu nevarēja atcelt. Mēģini vēlreiz. |
| CCR014     | Microsoft\_ Dynamics\_ Commerce Runtime\_\_ UnableToReadCardTokenInfo | Apstrādājot maksājumu, radās kļūda. Vēlāk mēģiniet vēlreiz. |
| CCR015     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ NotEnoughRewardPoints | Lojalitātes programmas maksājuma summa pārsniedz šai transakcijai izmantotās lojalitātes programmas kartes summu. |
| CCR016     | Microsoft\_ Dynamics\_ Commerce Runtime\_\_ RefundAmountMoreThanAllowed | Lojalitātes programmas atmaksas summa pārsniedz šai transakcijai izmantoto lojalitātes programmas karti. |
| CCR017     | Microsoft\_ Dynamics\_ Commerce Runtime\_\_ InvalidLoyaltyCardNumber | Lojalitātes kartes numurs netika atrasts. Aktivizējiet lojalitātes programmas kartes numuru vai ievadiet citu kartes numuru un pēc tam mēģiniet vēlreiz. |
| CCR018     | Microsoft\_ Dynamics Commerce\_ Runtime\_\_ BlockedLoyaltyCard | Lojalitātes programmas kartes numurs nav pieejams. Ievadiet citu kartes numuru un pēc tam mēģiniet vēlreiz. |
| CCR019     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ NoTenderLoyaltyCard | Šī lojalitātes programmas karte nav piemērota lojalitātes programmas punktu izpirkšanai šajā darbībā. |
| CCR020     | Microsoft\_ Dynamics\_ Commerce izpildlaika\_\_ GiftCardCurrencyMismatch | Dāvanu kartes numurs konstatēja kļūdu. Pamēģiniet citu dāvanu karti vai sazinieties ar klientu atbalsta dienestu, lai saņemtu palīdzību. |
| CCR021 (Tikai CCR021)     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ PaymentAmountExceedsGiftBalance | Summa pārsniedz dāvanu kartes bilanci. Ievadiet citu summu un pēc tam mēģiniet vēlreiz. |
| CCR022     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ NoMoreThanOneLoyaltyTender | Transakcijā nedrīkst būt vairākas lojalitātes programmas maksājuma rindas. |
| CCR023     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ PaymentAlreadyVoided | Trūkst informācijas par maksājumu vai tā ir nepareiza. Pārbaudiet informāciju par maksājumu un pēc tam mēģiniet vēlreiz. |
| CCR024     | Microsoft\_ Dynamics\_ Commerce Runtime\_\_ Fraud Runtime | Šoreiz pasūtījumu nevar apstrādāt. Vēlāk mēģiniet vēlreiz. |
| CCR025     | Priekšgalā beigu noildze, kas paredzēts API pārbaudei | Priekšgalā beigu operācijai iebeidzas taimauts. Apstipriniet, vai pasūtījums ir apstrādāts galvenajā birojā Dynamics 365 Commerce. |
| CCR026     | Sākotnējā autorizētā summa ir mainīta | Pasūtījuma summa ir mainīta no sākotnējās autorizācijas summas, kas apstrādāta ar maksājuma vārteju. Tas var būt kupona, veicināšanas vai pārdošanas termiņa beigu termiņa dēļ. |
| CCR027     | Microsoft\_ Dynamics\_ Commerce Runtime\_\_ InvalidCartVersion | Apstrādājot maksājumu, radās kļūda. Atsaucei, kas sniegta groza API, ir atšķirīga atsauce nekā prognozēts (norādot iespējamo neatbilstību pārbaudes procesa laikā). |
| CCR028     | Microsoft\_ Dynamics\_ Commerce\_ Runtime\_ MissingRequiredCartTenderLines | Maksāšanas metodē, notika mēģinājums, radās kļūda. Sazinieties ar atbalsta dienestu, lai pārskatītu konta iestatījumus vai mēģinātu vēlreiz ar citu maksājuma metodi. |

## <a name="additional-resources"></a>Papildu resursi

[Bieži uzdotie jautājumi par maksājumiem](dev-itpro/payments-retail.md)

[Izrakstīšanas modulis](add-checkout-module.md)

[Maksājumu modulis](payment-module.md)
