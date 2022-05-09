---
title: Klienta konta maksājuma metodes konfigurēšana B2B e-komercijas vietnēs
description: Šajā tēmā ir aprakstīts, kā konfigurēt debitora konta maksājuma metodi sistēmā Microsoft Dynamics 365 Commerce. Tajā aprakstīts arī tas, kā kredīta limiti ietekmē starpkontu maksājuma tveršanu e-komercijas vietnēs "bizness-biznesam".
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a8fdeb109204557f0e44457e23a60224e662474f
ms.sourcegitcommit: 96e2fb26efd2cd07bbf97518b5c115e17b77a0a8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2022
ms.locfileid: "8616836"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Klienta konta maksājuma metodes konfigurēšana B2B e-komercijas vietnēs

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā konfigurēt debitora konta maksājuma metodi sistēmā Microsoft Dynamics 365 Commerce. Tajā aprakstīts arī tas, kā kredīta limiti ietekmē starpkontu maksājuma tveršanu e-komercijas vietnēs "bizness-biznesam".

Mazumtirgotāji var pieņemt dažāda veida maksājumus apmaiņā pret pārdotajām precēm un pakalpojumiem e-komercijas kanālā. Sistēmas iestatīšanas laikā programmā Dynamics 365 Commerce ir jākonfigurē katrs maksājuma veids, ko pieņem mazumtirgotājs. Debitora konta (vai "starpkonta") maksāšanas metode ir jāatbalsta B2B e-komercijas vietnēs. 

## <a name="prerequisites"></a>Priekšnosacījumi

1. Pievienojiet klienta konta maksāšanas metodi komponentam Commerce Headquarters.
2. Saistiet klienta konta maksāšanas metodi ar e-komercijas kanālu.
3. Pārliecinieties, ka **rekvizīts Ļaut starpkontu** ir **iespējots programmas Commerce Headquarters debitoram, kas atrodas mazumtirdzniecībā Retail un Commerce \> Customers \> Visi \> debitora maksājuma noklusējums**.

    > [!NOTE]
    > Ja visiem debitoriem jāatļauj starpkonta maksājuma metode, jūs varat iestatīt rekvizītu Atļaut starpkontu uz Jā tā kanāla noklusējuma debitoram, **·** **kas** ir saistīts ar B2B vietni. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Klienta konta maksājuma metodes iespējošana Commerce vietnes veidotājā 

Lai iespējotu klienta konta maksājuma metodi Commerce vietnes veidotājā, veiciet tālāk norādītās darbības.

1. Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**.
1. Iestatiet rekvizītu **Iespējot klienta konta maksājumus** uz **Iespējot B2B klientiem**. 
1. Atlasiet **Saglabāt un publicēt**.

> [!NOTE]
> Jaunās vietnes iestatījumi stājas spēkā tikai pēc faila app.settings.json atjaunināšanas. Papildinformāciju skatiet [SDK un moduļu bibliotēkas atjauninājumi](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Klienta konta maksājuma metodes iespējošana B2B e-komercijas vietnes norēķināšanās lapā

Lai iespējotu klienta konta maksājuma metodes B2B e-komercijas vietnes norēķināšanās lapā, veiciet tālāk norādītās darbības.

1. Commerce vietnes veidotājā atrodiet un rediģējiet norēķināšanās lapu vai fragmentu, kas satur B2B e-komercijas vietnes norēķināšanās moduli.
1. Slotā **Norēķināšanās sekcijas konteiners** atlasiet **Pievienot moduli** un pēc tam pievienojiet **Klienta konta maksājuma** moduli.
1. Novietojiet **Klienta konta maksājumu** moduli, atlasot daudzpunktes (**...**), un pēc nepieciešamības atlasot **Pārvietot uz augšu** vai **Pārvietot uz leju**.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Klienta konta maksājuma metodes iespējošanas un publicēšanas apstiprinājums

Lai apstiprinātu, vai klienta konta maksājuma metode ir iespējota, veiciet tālāk norādītās darbības.

1. Pierakstieties e-komercijas vietnē.
1. Pievienojiet grozam preci.
1. Doties uz norēķināšanās lapu. Jums vajadzētu redzēt jauno **Klienta konta** maksājuma metodi.

## <a name="work-with-credit-limits"></a>Darbs ar kredīta limitiem

Kad debitora konta maksājumu iespējas ir iespējotas B2B vietnē, organizācijas parasti vēlas rādīt informāciju par kredīta limitiem un kredīta limita bilancēm pasūtījuma tveršanas procesa laikā. Debitora kredīta limits tiek definēts, **·** **izmantojot kredīta limita rekvizītu debitora galvenās pārvaldes debitora ieraksta kopsavilkuma cilnē Kredīts** un iekasēšana. Tomēr B2B scenārijos pasūtījums, kurā debitoram vieta bieži ir jāierēķinās tās organizācijas kontā, pie kuras pieder debitors. Tādēļ klienta ieraksta rēķina **un** **piegādes** kopsavilkuma cilnē ir jāiestata rēķina konta rekvizīts uz organizācijas debitora konta ID. Tad, kad debitors veic pasūtījumu B2B vietā, par pasūtījumu tiks izrakstīts rēķins organizācijai. B2B vieta izmantos arī organizācijas kredīta limitu kredīta limita vietā, kas ir definēts debitora ierakstā.

Kredīta limita aprēķins un bilance, kas tiek rādīti B2B **vietnē, ir atkarīgi no kredīta limita tipa rekvizīta** iestatījuma programmā Commerce Headquarters. Šī rekvizīta atrašanās vieta atšķiras atkarībā no tā, vai kredīta **pārvaldības** funkcija ir iespējota līdzekļu **pārvaldības darbvietā**:

- Ja kredīta **pārvaldības funkcija** ir aktivizēta, **rekvizīts** atrodas kredīta limitu kopsavilkuma cilnē **Kredīta un iekasēšanas iestatījumu \>\> kredīta un iekasēšanas parametru kredīts \>**. 
- Ja kredīta **pārvaldības funkcija ir** atspējota, rekvizīts atrodas **kredītreitingā pie** Debitoru **parādu \>\> iestatījuma debitoru parādu parametriem \> Kredītreitings**.

Vērtības, ko kredīta **limita tipa rekvizīts** atbalsta **, ir** Nav, **Bilance**, **Bilance + pavadzīme vai produktu ieejas** plūsma, un **Bilance + Visi**. Papildinformāciju par šīm vērtībām skatiet sadaļā [Kredīta limita tipa vērtības](/dynamics365/supply-chain/sales-marketing/credit-limits-customers).

> [!NOTE]
> Ieteicams iestatīt kredīta **limita** **tipa rekvizītu bilance +** pavadzīme vai produktu pavadzīme, lai atvērtie pārdošanas pasūtījumi neuzskaitītos bilances aprēķinā. Tad, ja debitori veiks turpmākus pasūtījumus, tiem nav jāietekmē šo pasūtījumu pašreizējā bilance.

Cits rekvizīts, kas ietekmē starpkontu **pasūtīšanas** ir obligātais kredīta limita rekvizīts, **kas atrodas debitora ieraksta kopsavilkuma cilnē Kredīts** un iekasēšana. Iestatot šo **rekvizītu** kā Jā noteiktiem debitoriem, var likt sistēmai pārbaudīt to kredīta limitu, **·** **pat ja kredīta limita tipa rekvizīts ir iestatīts uz Nav**, lai norādītu, ka nevienam debitoram kredīta limits nav jāpārbauda.

Pašlaik debitors, kas izmanto starpkonta maksājuma metodi, nevar maksāt vairāk par pasūtījuma atlikušo kredīta bilanci. Piemēram, ja debitora atlikusī kredīta bilance ir $1,000 bet pasūtījuma vērtība ir $1,200, debitors var maksāt $1,000, izmantojot starpkontu metodi. Pēc tam debitoram bilances apmaksai jāizmanto kāda cita maksājuma metode. Turpmākajā laidienā Commerce konfigurācija ļaus lietotājiem, veicot pasūtījumus, tēriņus pārsniedz kredīta limitu.

Kredīta **un iekasēšanas modulim** ir jaunas kredīta pārvaldības iespējas. Lai ieslēgtu šīs iespējas, iespējojiet kredīta pārvaldības **līdzekli** līdzekļu pārvaldības **darbvietā**. Viena no jaunajām iespējām ļauj aizturēt pārdošanas pasūtījumus, pamatojoties uz bloķēšanas nosacījumiem. Kredīta pārvaldnieka persona pēc tam var izlaist vai noraidīt pasūtījumus pēc tālākas analīzes. Tomēr iespēja aizturēt pārdošanas pasūtījumus nav piemērota Commerce pasūtījumiem, jo pārdošanas pasūtījumiem bieži ir priekšapmaksa un **kredīta** pārvaldības funkcija pilnībā neatbalsta priekšapmaksas scenārijus. 

Neatkarīgi no **tā**, vai kredīta pārvaldības funkcija ir iespējota, ja debitora bilance pārsniedz kredīta limitu pasūtījuma izpildes laikā, pārdošanas pasūtījumi netiks aizturēti. Tā vietā komercija ģenerēs brīdinājuma ziņojumu vai kļūdas ziņojumu atkarībā no ziņojuma vērtības, **·** **pārsniedzot kredīta limita lauku kopsavilkuma cilnē Kredīta** limits.

Rekvizīts **Izslēgt no kredīta pārvaldības** rekvizīta, kas neļauj commerce pārdošanas pasūtījumiem aizturēt, ir novietots pārdošanas pasūtījuma virsrakstā (**Visi mazumtirdzniecības un commerce \> Debitori \> visi pārdošanas pasūtījumi**). Ja šis rekvizīts Commerce pārdošanas pasūtījumiem **ir** iestatīts uz Jā (noklusējuma vērtība), pasūtījumi tiek izslēgti no aizturētās kredīta pārvaldības darbplūsmas. Lai gan rekvizīta nosaukums ir **Izslēgt no kredīta pārvaldības**, definētais kredīta limits joprojām tiks izmantots pasūtījuma izpildes laikā. Pasūtījumi tikko netiks aizturēti.

Iespēja aizturēt Commerce pārdošanas pasūtījumus, pamatojoties uz aizturēšanas nosacījumiem, ir plānota nākamajiem Commerce laidieniem. Līdz tam, kamēr tas netiek atbalstīts, ja ir nepieciešams, lai Commerce pārdošanas pasūtījumi izietu cauri jaunām kredīta pārvaldības plūsmām, risinājumā varat pielāgot šādus XML failus Visual Studio. Failos modificējiet loģiku tā, lai **CredManExcludeSalesOrder karodziņš** būtu iestatīts uz **Nē**. Šādā veidā rekvizīts **Izslēgt no kredīta pārvaldības tiks** iestatīts uz **Nē** pēc noklusējuma commerce pārdošanas pasūtījumiem.

- RetailCreateCustomerOrderExtensions_CredMan_Extension.xml
- RetailCallCenterOrderExtensions_CredMan_Extension.xml

**Ja CredManExcludeSalesOrder** **karodziņš** ir iestatīts uz Nē un B2B debitors var iegādāties no veikaliem, izmantojot pārdošanas punkta (POS) programmu, skaidras naudas un pārvadāšanas darbību grāmatošana var neizdoties. Piemēram, pastāv bloķēšanas noteikums skaidras naudas maksājuma veidam, un B2B debitors veikalā iegādājās dažas preces, izmantojot skaidru naudu. Šajā gadījumā rezultāta pārdošanas pasūtījums netiks sekmīgi iekļauts rēķinā, jo tas tiks aizturēts. Tādēļ grāmatošana neizdosies. Tāpēc pēc šīs pielāgošanas ir ieteicams veikt beigu pārbaudi.

## <a name="additional-resources"></a>Papildu resursi

[B2B e-komercijas vietnes iestatīšana](set-up-b2b-site.md)

[B2B biznesa partneru pārvaldība, izmantojot debitoru hierarhijas](partners-customer-hierarchies.md)

[Biznesa partnera lietotāju pārvaldība B2B e-komercijas vietnēs](manage-b2b-users.md)

[Preču daudzuma ierobežojumu iestatīšana B2B e-komercijas vietnēs](quantity-limits.md)

[SDK un moduļu bibliotēkas atjauninājumi](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
