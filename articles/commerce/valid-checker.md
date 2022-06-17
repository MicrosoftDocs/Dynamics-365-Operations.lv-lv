---
title: Veikala transakciju apstiprināšana pārskata aprēķinam
description: Šajā rakstā ir aprakstīta veikala transakciju apstiprināšanas funkcionalitāte produktā Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 01/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: analpert
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4be40189777a37495f185467050b61af47b684d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890518"
---
# <a name="validate-store-transactions-for-statement-calculation"></a>Veikala transakciju apstiprināšana pārskata aprēķinam

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīta veikala transakciju apstiprināšanas funkcionalitāte produktā Microsoft Dynamics 365 Commerce. Apstiprināšanas process identificē un atzīmē tās transakcijas, kas izraisīs grāmatošanas kļūdas, pirms šīs transakcijas izvēlas pārskata grāmatošanas process.

Mēģinot grāmatot pārskatu, apstiprināšanas process var neizdoties nekonsekventu datu dēļ Commerce transakciju tabulās. Šeit sniegti daži faktoru piemēri, kas var izraisīt šādas nekonsekvences:

- Transakcijas kopsumma virsraksta tabulā neatbilst transakcijas kopsummai rindās.
- Vienumu skaits, kas norādīts virsraksta tabulā, neatbilst vienumu skaitam transakcijas tabulā.
- Nodokļi virsraksta tabulā neatbilst nodokļu summai rindās. 

Kad pārskatu grāmatošanas process uzņem nekonsekventas transakcijas, izveidotie pārdošanas rēķini un maksājumu žurnāli var izraisīt pārskata grāmatošanas neveiksmi. Process **Veikala transakciju apstiprināšana** novērš šīs problēmas, nodrošinot, ka tikai transakcijas, kas atbilst transakciju apstiprināšanas kārtulām, tiek pievienotas transakciju pārskata aprēķināšanas procesam.

Tālāk esošajā attēlā redzami periodiskie dienas laika procesi transakciju augšupielādei, transakciju apstiprināšanai un transakciju pārskatu aprēķināšanai un grāmatošanai, kā arī finanšu pārskata aprēķināšanas un grāmatošanas dienas beigu procesi.

![Attēls, kurā redzami periodiskie dienas laika procesi transakciju augšupielādei, transakciju apstiprināšanai un transakciju pārskatu aprēķināšanai un grāmatošanai, kā arī finanšu pārskata aprēķināšanas un grāmatošanas dienas beigu procesi.](./media/valid-checker-statement-posting-flow.png)

## <a name="store-transaction-validation-rules"></a>Veikala transakciju apstiprināšanas kārtulas

Pakešveida apstrāde **Veikala transakciju apstiprināšana** pārbauda Commerce transakciju tabulu konsekvenci, pamatojoties uz šīm apstiprināšanas kārtulām.

> [!NOTE]
> Apstiprināšanas kārtulu pievienošana turpināsies nākamajos laidienos.

### <a name="transaction-header-validation-rules"></a>Transakcijas virsraksta apstiprināšanas kārtulas

Tālāk sniegtajā tabulā ir sniegtas transakcijas virsraksta apstiprināšanas kārtulas, kas ir pārbaudītas attiecībā pret mazumtirdzniecības transakciju virsrakstiem, pirms šīs transakcijas tiek pievienotas pārskata grāmatošanai.

| Kārtula | Apraksts |
|-------|-------------|
| Biznesa datums | Šī kārtula apstiprina, ka transakcijas biznesa datums virsgrāmatā ir saistīts ar atvērtu finanšu periodu. |
| Valūtas noapaļošana | Šī kārtula apstiprina, vai transakcijas summas tiek noapaļotas atbilstoši valūtas noapaļošanas kārtulai. |
| Debitora konts | Šī kārtula apstiprina, vai datu bāzē pastāv transakcijā izmantotais debitors. |
| Atlaides summa | Šī kārtula apstiprina, vai virsrakstā iekļautā atlaides summa ir līdzvērtīga rindu atlaides summai. |
| Finanšu dokumenta grāmatošanas statuss (Brazīlija) | Šī kārtula apstiprina, vai finanšu dokumentu var sekmīgi grāmatot. |
| Bruto summa | Šī kārtula apstiprina, vai transakcijas virsrakstā iekļautā bruto summa atbilst transakcijas rindu neto summai ar nodokļiem, kam pieskaitītas izmaksas. |
| Neto | Šī kārtula apstiprina, vai transakcijas virsrakstā iekļautā neto summa atbilst transakcijas rindu neto summai bez nodokļiem, kam pieskaitītas izmaksas. |
| Neto + nodoklis | Šī kārtula apstiprina, vai transakcijas virsrakstā iekļautā bruto summa atbilst transakcijas rindu neto summai bez nodokļiem, kam pieskaitīti visi nodokļi un izmaksas. |
| Vienumu skaits | Šī kārtula apstiprina, vai vienumu skaits, kas norādīts transakcijas galvenē, atbilst vienumu summai transakcijas rindās. |
| Maksājuma summa | Šī kārtula apstiprina, ka maksājuma summa transakcijas virsrakstā atbilst visu maksājuma transakciju summai. |
| Nodokļa atbrīvojuma aprēķināšana | Šī kārtula apstiprina, ka aprēķinātā daudzuma summa un no nodokļiem atbrīvotā maksas rindu summa ir vienāda ar sākotnēji aprēķināto summu. |
| Izcenojumā iekļauts nodoklis | Šī kārtula apstiprina, vai **Nodoklis ir iekļauts cenā** karodziņš ir konsekvents visā transakcijas galvenē un nodokļu transakcijās. |
| Transakcija nav tukša | Šī kārtula apstiprina, vai transakcija satur rindas un vismaz viena rinda nav tukša. |
| Nepilnīgs maksājums/pārmaksa | Šī kārtula apstiprina, vai bruto summas un maksājuma summas starpība nepārsniedz maksimālo konfigurēto nepilnīga maksājuma/pārmaksas summu. |

### <a name="transaction-line-validation-rules"></a>Transakcijas rindu apstiprināšanas kārtulas

Tālāk sniegtajā tabulā ir sniegtas transakcijas rindas apstiprināšanas kārtulas, kas ir pārbaudītas attiecībā pret mazumtirdzniecības transakciju rindu informāciju, pirms šīs transakcijas tiek pievienotas pārskata grāmatošanai.

| Kārtula | Apraksts |
|-------|-------------|
| Svītrkods | Šī kārtula apstiprina, vai visi vienumu svītrkodi, kas tiek izmantoti transakciju rindās, pastāv datu bāzē. |
| Maksu rindas | Šī kārtula apstiprina, ka aprēķinātā daudzuma summa un no nodokļiem atbrīvotā maksas rindu summa ir vienāda ar sākotnēji aprēķināto summu. |
| Dāvanu kartes atgriešana | Šī kārtulā apstiprina, vai transakcijā nav dāvanu karšu atgriešanas. |
| Vienuma variants | Šī kārtula apstiprina, vai visi vienumi un visi to varianti, kas tiek izmantoti transakciju rindās, pastāv datu bāzē. |
| Rindas atlaide | Šī kārtula apstiprina, vai rindas atlaides summa atbilst atlaižu transakciju summai. |
| Rindas nodoklis | Šī kārtula apstiprina, vai rindas nodokļa summa atbilst nodokļu transakciju summai. |
| Negatīva cena | Šī kārtula apstiprina, vai transakciju rindās netiek izmantotas negatīvas cenas. |
| Sērijas numura kontrole | Šī kārtula apstiprina, vai sērijas numurs atrodas transakcijas rindā tiem vienumiem, kas tiek kontrolēti pēc sērijas numura. |
| Sērijas numura dimensija | Šī kārtula apstiprina, vai nav norādīts sērijas numurs, ja vienuma sērijas numura dimensija nav aktīva. |
| Zīmju pretruna | Šī kārtula apstiprina, vai daudzuma un neto summas zīme ir vienāda visās transakciju rindās. |
| Ar nodokli neapliekams | Šī kārtula apstiprina, ka rindas vienuma cenas summa un no nodokļiem atbrīvotā maksas rindu summa ir vienāda ar sākotnējo cenu. |
| Nodokļu grupas piešķire | Šī kārtula apstiprina, ka pārdošanas nodokļu grupas un vienumu nodokļu grupas kombinācija rada derīgu nodokļu krustošanos. |
| Mērvienības pārvēršana | Šī kārtula apstiprina, ka visu rindu mērvienības ir derīgas pārvēršanai vienumu mērvienībās. |

## <a name="enable-the-store-transaction-validation-process"></a>Veikala transakciju apstiprināšanas procesa iespējošana

Konfigurējiet darbu **Apstiprināt veikala transakcijas** periodiskai izpildei komponentā Commerce Headquarters (**Retail un Commerce \> Retail un Commerce IT \> POS grāmatošana**). Pakešuzdevums ir ieplānots, ņemot vērā veikala organizācijas hierarhiju. Mēs iesakām jums konfigurēt šo pakešveida apstrādi, lai tā tiktu izpildīta tikpat bieži kā jūsu **P-darba** un **Transakciju pārskata aprēķina** pakešuzdevumi.

## <a name="results-of-the-validation-process"></a>Apstiprināšanas procesa rezultāti

Katras **Veikala transakciju apstiprināšanas** pakešveida apstrādes rezultātus var skatīt par katru mazumtirdzniecības veikala transakciju. Lauks **Apstiprināšanas statuss** transakcijas ierakstā tiek iestatīts kā **Sekmīgs**, **Kļūda** vai **Nav**. Laukā **Pēdējās apstiprināšanas laiks** redzams pēdējās apstiprināšanas izpildes datums.

Tālāk esošajā tabulā ir aprakstīts katrs apstiprināšanas statuss.

| Apstiprināšanas statuss | Apraksts |
|-------------------|-------------|
| Sekmīgs | Izpildītas visas iespējotās apstiprināšanas kārtulas. |
| Kļūda | Iespējota apstiprināšanas kārtula ir konstatējusi kļūdu. Plašāku informāciju par kļūdu var skatīt, darbību rūtī atlasot **Apstiprināšanas kļūdas**. |
| Nav | Transakcijas veidam nav nepieciešams, lai tiktu lietotas apstiprināšanas kārtulas. |

![Veikala transakciju lapa, kurā tiek rādīts lauks Apstiprināšanas statuss un poga Apstiprināšanas kļūdas.](./media/valid-checker-validation-status-errors.png)

Transakciju pārskatos tiks iekļautas tikai tās transakcijas, kuru apstiprināšanas statuss ir **Sekmīgs**. Lai skatītu transakcijas ar statusu **Kļūda**, pārskatiet elementu **Skaidras naudas un pārvedumu apstiprināšanas kļūmes** darbvietā **Veikala finanses**.

![Elementi darbvietā Veikala finanses.](./media/valid-checker-cash-carry-validation-failures.png)

Papildinformāciju par to, kā novērst skaidras naudas un pārvedumu apstiprināšanas kļūmes, skatiet sadaļā [Transakciju, kas saistītas ar pārdošanu skaidrā naudā bez piegādes, un skaidras naudas pārvaldības darījumu rediģēšana un auditēšana](edit-cash-trans.md).

## <a name="additional-resources"></a>Papildu resursi

[Transakciju, kas saistītas ar pārdošanu skaidrā naudā bez piegādes, un skaidras naudas pārvaldības darījumu rediģēšana un auditēšana](edit-cash-trans.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
