---
title: Darbs ar serializētajiem krājumiem punktā POS
description: Šajā tēmā skaidrots, kā pārvaldīt sērijas krājumus pārdošanas punkta (POS) lietojumprogrammā.
author: boycezhu
manager: annbe
ms.date: 04/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 1e0d6aa7cd5576578378e70c6ee808833314aff3
ms.sourcegitcommit: 919620b4aca425e6a1248ee12f50a622d2531e58
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2020
ms.locfileid: "3290774"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Darbs ar serializētajiem krājumiem punktā POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Daudzi mazumtirgotāji pārdod preces, kurām nepieciešama sērijas kontrole. Šie krājumi tiek saukti par *sērijas krājumiem*. Daži mazumtirgotāji var vēlēties saglabāt sērijas numurus izsekošanas nolūkiem. Citi mazumtirgotāji pārdošanas procesa laikā var vēlēties iegūt sērijas numurus pakalpojumu un garantijas nolūkiem. Šajā tēmā skaidrots, kā jūs varat pārvaldīt sērijas krājumus Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) lietojumprogrammā.

## <a name="serial-number-configurations"></a>Sērijas numura konfigurācijas

Krājums tiek uzskatīts par sērijas krājumu, ja tam ir piešķirta izsekošanas dimensiju grupa, kas ir iestatīta, lai atļautu sērijas numurus. Commerce galvenajā birojā lapā **Izsekošanas dimensiju grupas** atlasiet opciju **Aktīvs**, lai iespējotu sērijas numuru izmantošanu krājumu procesam. Lai aktivizētu pārdošanas procesa sērijas numurus, atlasiet opciju **Aktīvs pārdošanas procesā**.

Ja opcija **Tukša kvīts atļauta** ir iespējota cilnē **Izsekošanas dimensijas**, sērijas numurs ir izvēles ievade krājumu ieejas plūsmas procesa laikā. Ja opcija ir izslēgta, ir jānorāda sērijas numurs.

Ja opcija **Sērijas numuru kontrole** ir ieslēgta kopsavilkuma cilnē **Sērijas numuri**, sērijas numuram jābūt unikālam katrā vienībā. Citiem vārdiem sakot, dublētie sērijas numuri nav atļauti.

## <a name="serialized-items-in-the-receiving-process"></a>Sērijas krājumi saņemšanas procesā

**Saņemšanas krājumu** operācija POS programmā ļauj lietotājiem veikt šādus sērijas krājumu uzdevumus:

- Reģistrēt sērijas numurus, salīdzinot ar sērijas krājumiem, kad šie krājumi tiek saņemti veikalā, izmantojot pirkšanas pasūtījumu.
- Apstiprināt iepriekš reģistrētus sērijas numurus, salīdzinot ar sērijas krājumiem, kad šie krājumi tiek saņemti veikalā, izmantojot pirkšanas pasūtījumu vai pārskaitījuma pasūtījumu.

> [!NOTE]
> Lai izmantotu **Ienākošo krājumu** operāciju, lai reģistrētu vai apstiprinātu sērijas krājumu, krājumam ir jāpiešķir izsekošanas dimensiju grupa, kas ir iestatīta, lai atļautu opciju **Aktīvs** sērijas numuriem, nevis opciju **Aktīvs pārdošanas procesā**.

Lai sāktu saņemšanas procesu **Ienākošo krājumu** operācijā, varat sākt ar skatu **Saņemšana tagad**, skenējot preces svītrkodu vai ievadot krājuma ID. Varat arī sākt skatā **Pilnā pasūtījuma saraksts**, manuāli atlasot krājumu.

Ja krājums, kas tiek atlasīts vai saņemts, ir sērijas krājums, rūts **Detalizētas informācija** krājumam ietver saiti **Pārvaldīt sērijas numuru**, kas atver lapu **Sērijas numura pārvaldība**. Lapu **Sērijas numura pārvaldība** varat atvērt arī, vai nu atlasot **Sērijas numuru** pasūtījuma detalizētas informācijas skata programmas joslā vai atlasot **Pārvaldīt sērijas numuru** dialoglodziņā, kurā tiek parādīts uzaicinājums saņemšanas procesa laikā. **Sērijas numura pārvaldības** lapā ir uzskaitītas visas atvērtās sērijas numura rindas, kas gaida reģistrāciju vai apstiprināšanu. Šajā lapā varētu būt divas cilnes: viena pašreizējam krājumam un viena visām sērijas precēm pasūtījumā.

**Statusa** lauks lapā **Sērijas numura pārvaldība** sniedz informāciju par pašreizējo stadiju, kurā katrs sērijas numurs ir:

- **Nav reģistrēts** – nav norādīts sērijas numurs vai arī reģistrētais sērijas numurs vēl nav apstiprināts.
- **Reģistrācija** — sērijas numurs ir reģistrēts un saglabāts veikala kanāla datu bāzē, vai arī reģistrētais sērijas numurs ir apstiprināts. Commerce galvenajā birojā tiks iesniegti tikai tie sērijas numuri, kuriem pēc saņemšanas ir statuss **Reģistrēts**.

### <a name="register-serial-numbers-against-serialized-items"></a>Reģistrēt sērijas numurus ar sērijas krājumiem

Dialoglodziņš, kas uzaicina jūs sērijas krājuma saņemšanas procesa laikā, piedāvā opciju **Pārvaldīt sērijas numuru** pirkšanas pasūtījumam. Jūs varat atlasīt šo opciju, lai atvērtu **Sērijas numura pārvaldības** lapu un sāktu reģistrēt sērijas numurus. Jūs varat arī izlaist šo darbību saņemšanas procesa laikā un sniegt ievadi vēlāk, pirms kvīts tiek grāmatota.

Pēc noklusējuma tiek rādīta cilne pašreizējam krājumam. Visām sērijas numuru rindām ir tukša sērijas numura vērtība un statuss **Nav reģistrēts**. Jūs varat skenēt sērijas numura svītrkodus vai arī varat izvēlēties **Sērijas numuru** programmas joslā, lai pastāvīgi ievadītu sērijas numurus dialoglodziņā. Ievadītie sērijas numuri parādās sarakstā, un sērijas numura rindu statuss tiek mainīts uz **Reģistrēts**. Maksimālais sērijas numuru skaits, ko var reģistrēt sarakstā, ir vienāds ar saņemšanas daudzumu. Ja kļūdāties, varat atlasīt **Rediģēt** vai **Dzēst** rūtī **Detalizētas informācija**, lai veiktu izmaiņas ievadītajiem sērijas numuriem.

Sērijas numurus var reģistrēt arī cilnē **Visi sērijas krājumi** lapā **Sērijas numura pārvaldība**. Sarakstā atlasiet krājumu, kuru vēlaties reģistrēt ar sērijas numuriem.

Šīs lapas sērijas numura reģistrācijas laikā tiek veikta dublikāta apstiprināšana. Ja mēģināsit ievadīt dublētu sērijas numuru krājumam, kam ir ieslēgta sērijas numura kontrole, saņemsit kļūdas ziņojumu, un tam būs jānorāda atšķirīgs numurs.

### <a name="validate-serial-numbers-on-serialized-items"></a>Apstiprināt sērijas numurus sēriju krājumos

Pārsūtīšanas pasūtījumam nosūtīšanas procesa laikā sērijas numuri ir jāreģistrē sērijas krājumos. Pirkšanas pasūtījumam piegādātājs var sniegt sērijas numura informāciju, izmantojot Iepriekšējo paziņojumu par nosūtīšanu (IPPN), un jūs varat iepriekš reģistrēt numurus precēm, kas tiks nosūtītas. Abos gadījumos sērijas numuri ir zināmi pirms rēķina. Tāpēc no saņemšanas puses ir tikai jāpārbauda, vai esat saņēmis to, ko bija paredzēts saņemt.

Lai apstiprinātu sērijas numurus, varat atvērt lapu **Sērijas numura pārvaldība** vai nu saņemšanas procesa laikā, vai jebkurā laikā pirms rēķina iegrāmatošanas. Katram sēriju krājumam, kam ir sākotnēji reģistrēti sērijas numuri, šajā lapā tie automātiski tiek iestatīti uz statusu **Nav reģistrēts**. Lai apstiprinātu sērijas numurus, varat tos skenēt vai ievadīt. Kad tiek ievadīts sērijas numurs, lietojumprogramma pārbauda, vai tie atbilst ierakstītajiem sērijas numuriem. Ja tie atbilst, to statuss tiek mainīts uz **Reģistrēts**. Pretējā gadījumā tiks parādīts kļūdas ziņojums. Maksimālais sērijas numuru skaits, ko var apstiprināt sarakstā, ir vienāds ar saņemšanas daudzumu.

Sērijas numurus var apstiprināt arī cilnē **Visi sērijas krājumi** lapā **Sērijas numura pārvaldība**. Sarakstā atlasiet krājumu, kuru vēlaties apstiprināt ar sērijas numuriem.

## <a name="additional-resources"></a>Papildu resursi

[Ienākošo krājumu operācija punktā POS](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)
