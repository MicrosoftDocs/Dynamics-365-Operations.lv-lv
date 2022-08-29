---
title: Konfigurēt PVN tiešsaistes pasūtījumiem
description: Šajā rakstā sniegts pārskats par PVN grupu atlasi dažādiem tiešsaistes pasūtījumu tipiem Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 5936d16039927812dabf99bd770afcc0e827f1ca
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276721"
---
# <a name="configure-sales-tax-for-online-orders"></a>Konfigurēt PVN tiešsaistes pasūtījumiem

[!include [banner](includes/banner.md)]

Šajā rakstā sniegts pārskats par PVN grupu atlasi dažādiem tiešsaistes pasūtījumu tipiem, izmantojot mērķa vai debitora konta nodokļu iestatījumus. 

Iespējams, vēlēsities, lai jūsu e-komercijas kanāls atbalsta tādas opcijas, kā piegāde vai saņemšana tiešsaistes pasūtījumiem. PVN piemērojamība ir balstīta uz opciju, ko atlasa tiešsaistes klienti. 

## <a name="destination-based-taxes-for-online-orders"></a>Tiešsaistes pasūtījumu mērķa nodokļi

Parasti nodokļus tiešsaistes pasūtījumiem, kas nosūtāmi uz klienta adresēm, definē adresāts. Katrai PVN grupai ir mazumtirdzniecības mērķa nodokļu konfigurācija, kurā jūsu uzņēmums var definēt adresāta informāciju, piemēram, apgabals vai reģions, rajons, apgabals un pilsēta hierarhiskā formā.

### <a name="orders-delivered-to-customer-address"></a>Pasūtījumi, kas piegādāti uz klienta adresi

Kad tiek veikts tiešsaistes pasūtījums, Commerce nodokļu programma izmanto katra pasūtījuma rindas krājuma piegādes adresi un atrod PVN grupas, kas atbilst ar mērķi balstītus nodokļu kritērijus. Piemēram, tiešsaistes pasūtījumam ar rindas krājuma piegādes adresi uz Sanfrancisko, Kalifornijā, nodokļu programma atradīs PVN grupu un PVN kodu Kalifornijā un tad aprēķiniet nodokli katram rindas krājumam atbilstoši.

### <a name="order-pick-up-in-store"></a>Pasūtījuma saņemšana veikalā

Pasūtījuma rindām ar saņemšanu veikalā vai saņemšanu pa ceļam tiek lietota atlasītā saņemšanas veikala nodokļu grupa. Papildinformāciju par to, kā iestatīt PVN noteiktam veikalam, skatiet sadaļā [Citu nodokļu opciju iestatīšana veikaliem](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

## <a name="customer-account-based-taxes-for-online-orders"></a>Tiešsaistes pasūtījumu debitora konta nodokļi

Var būt biznesa scenārijs, kurā vēlaties konfigurēt PVN grupu noteiktā debitora kontā programmā Commerce Headquarters. Galvenajā birojā ir divas vietas, kur varat konfigurēt PVN debitora kontam. Lai piekļūtu tiem, vispirms ir jānokļūst debitora detalizētas informācijas lapā, dodoties uz **Mazumtirdzniecība un Komercija \> Debitori \> Visi debitori**, un pēc tam atlasot debitoru.

Divas vietas, kur tiek konfigurēts PVN debitora kontam:

- **PVN grupa** debitoru informācijas lapas kopsavilkuma cilnē **Rēķins un piegāde**. 
- **PVN** kopsavilkuma cilnē **Vispārīgi** lapā **Pārvaldīt adreses**. Lai tur nokļūst no debitora informācijas lapas, atlasiet noteiktu adresi kopsavilkuma cilnē **Adreses** un pēc tam atlasiet **Detalizēti**.

> [!TIP]
> Tiešsaistes debitoru pasūtījumos, ja vēlaties piemērot tikai mērķa nodokļus un izvairīties no debitora konta nodokļiem, pārliecinieties, ka lauks **PVN grupa** ir tukšs debitora informācijas lapas kopsavilkuma cilnē ir tukšs debitora informācijas lapas kopsavilkuma cilnē **Rēķins un piegāde**. Lai nodrošinātu, ka jaunie debitori, kuri pierakstās, izmantojot tiešsaistes kanālu, nepārmanto PVN grupas iestatījumus no noklusējuma debitora vai debitoru grupas iestatījumiem, nodrošiniet, ka lauks **PVN grupa** ir tukšs arī tiešsaistes kanāla noklusējuma debitora iestatījumiem un debitoru grupas iestatījumiem (**Mazumtirdzniecība un Komercija \> Debitors \> Debitoru grupas**).

## <a name="determine-destination-based-tax-or-customer-account-based-tax-applicability"></a>Mērķa nodokļu vai debitora kontu nodokļu piemērojamības noteikšana 

Šajā tabulā skaidrots, vai mērķa nodokļi vai debitora konta nodokļi tiek piemēroti tiešsaistes pasūtījumiem. 

| Debitora veids | Piegādes adrese                   | Debitors > Rēķins un piegāde > PVN grupa? | Vai šī ir debitora adrese galvenajā birojā? | Debitora adrese > Detalizēti> Visparīgi > PVN grupa?                                              | Lietotā PVN grupa      |
|---------------|------------------------------------|-----------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------|
| Viesis         | Manhetena, Ņujorka                      | Nē (tukšs)                                                | Nē (tukšs)                              | Nē (tukšs)                                                                                                   | Ņujorka (mērķa nodokļi) |
| Ir pierakstījies     | Ostins, Teksasa                          | Nē (tukšs)                                             | Jā                               | Neviens<br/><br/>Jauna adrese, kas pievienota, izmantojot tiešsaistes kanālu.                                                            | Teksasa (mērķa nodokļi) |
| Ir pierakstījies     | Sanfrancisko, Kalifornija (saņemt veikalā) | Jā (Ņujorka)                                            | Nav attiecināms                              | Nav attiecināms                                                                                                    | Kalifornija (mērķa nodokļi) |
| Ir pierakstījies     | Hjūstona, Teksasa                         | Jā (Ņujorka)                                            | Jā                               | Jā (Ņujorka)<br/><br/>Jauna adrese, kas pievienota, izmantojot tiešsaistes kanālu un PVN grupu, kas mantota no debitora konta. | Ņujorka (debitora konta nodokļi)  |
| Ir pierakstījies     | Ostins, Teksasa                          | Jā (Ņujorka)                                            | Jā                               | Jā (Ņujorka)<br/><br/>Jauna adrese, kas pievienota, izmantojot tiešsaistes kanālu un PVN grupu, kas mantota no debitora konta. | Ņujorka (debitora konta nodokļi)  |
| Ir pierakstījies     | Sarasota, Florida                       | Jā (Ņujorka)                                            | Jā                               | Jā (Vašingtona)<br/><br/>Manuāli iestatīts uz Vašingtona.                                                                          | Vašingtona (debitora konta nodokļi)  |
| Ir pierakstījies     | Sarasota, Florida                       | Nē (tukšs)                                                | Jā                               | Jā (Vašingtona)<br/><br/>Manuāli iestatīts uz Vašingtona.                                                                          | Vašingtona (debitora konta nodokļi)  |

## <a name="additional-resources"></a>Papildu resursi

[Iestatīt nodokļus tiešsaistes veikaliem, pamatojoties uz mērķa](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)

[PVN pārskats](../finance/general-ledger/indirect-taxes-overview.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[PVN aprēķināšanas metodes laukā Izcelsme](../finance/general-ledger/sales-tax-calculation-methods-origin-field.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[PVN piešķire un pārrakstīšana](../supply-chain/procurement/tasks/sales-tax-assignment-overrides.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Visas summas un intervāla aprēķināšanas opcijas PVN kodiem](../finance/general-ledger/whole-amount-interval-options-sales-tax-codes.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Nodokļa atbrīvojuma aprēķināšana](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
