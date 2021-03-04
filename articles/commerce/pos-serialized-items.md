---
title: Darbs ar serializētajiem krājumiem punktā POS
description: Šajā tēmā skaidrots, kā pārvaldīt sērijas krājumus pārdošanas punkta (POS) lietojumprogrammā.
author: boycezhu
manager: annbe
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 6ba01abc3d1a4496ec586a621aa03b4981f84d76
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414163"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Darbs ar serializētajiem krājumiem punktā POS

[!include [banner](includes/banner.md)]

Daudzi mazumtirgotāji pārdod preces, kurām nepieciešama sērijas kontrole. Šīs preces tiek sauktas par *sērijas krājumiem*. Daži mazumtirgotāji var vēlēties saglabāt sērijas numurus krātuves vai noliktavas krājumā izsekošanas nolūkiem. Citi mazumtirgotāji pārdošanas procesa laikā var vēlēties iegūt sērijas numurus pakalpojumu un garantijas nolūkiem. Šajā tēmā skaidrots, kā jūs varat pārvaldīt sērijas krājumus Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) lietojumprogrammā.

## <a name="serial-number-configurations"></a>Sērijas numura konfigurācijas

Krājums tiek uzskatīts par sērijas krājumu, ja tam ir piešķirta izsekošanas dimensiju grupa, kas ir iestatīta, lai atļautu sērijas numurus. Risinājumā Commerce Headquarters lapā **Izsekošanas dimensiju grupas** atlasiet opciju **Aktīvs**, lai iespējotu krājumu procesa sērijas numurus, vai atlasiet opciju **Aktīvs pārdošanas procesā**, lai iespējotu pārdošanas procesa sērijas numurus.

Ieslēdziet parametru **Tukša kvīts atļauta** cilnē **Izsekošanas dimensijas**, lai sērijas numurs ir izvēles ievade serializētā vienuma krājumu ieejas plūsmas procesa laikā. Izslēdzot šo parametru, sērijas numurs kļūst par obligātu ievadi. Līdzīgi, parametrs **Tukšs numurs atļauts** kontrolē, vai krājumu nosūtīšanas procesa laikā ir nepieciešams sērijas numurs.

> [!NOTE]
> Lai izmantotu POS operācijas **Ienākošais krājums** un **Izejošais krājums**, lai reģistrētu vai apstiprinātu sērijas numurus pret sērijas krājumu, šis vienums ir jākonfigurē, lai tam piešķirtu izsekošanas dimensiju grupu, kas ir iestatīta, lai sērijas numuriem atļautu opciju **Aktīvs**, nevis opciju **Aktīvs pārdošanas procesā**.

## <a name="serial-number-management-page"></a>Sērijas numura pārvaldības lapa

POS operācijās **Ienākošais krājums** un **Izejošais krājums**, ja krājums, kas tiek atlasīts, saņemts vai nosūtīts, ir serializētais krājums, rūtī **Detalizēta informācija** ir ietverta opcija **Pārvaldīt sērijas numuru**, kas ir saistīta ar lapu **Sērijas numura pārvaldība**, kur var reģistrēt vai validēt krājuma sērijas numurus. Lapu **Sērijas numura pārvaldība** varat atvērt arī, vai nu atlasot **Sērijas numura** darbību pasūtījuma detalizētas informācijas skata programmas joslā vai atlasot opciju **Pārvaldīt sērijas numuru** dialoglodziņā, kurā tiek parādīts uzaicinājums saņemšanas vai piegādes procesa laikā. 

**Sērijas numura pārvaldības** lapā ir uzskaitītas visas atvērtās sērijas numura rindas, kas gaida reģistrāciju vai apstiprināšanu. Šajā lapā varētu būt divas cilnes: viena pašreizējam krājumam un cita visām sērijas precēm pasūtījumā.

**Statusa** lauks lapā **Sērijas numura pārvaldība** sniedz informāciju par pašreizējo stadiju, kurā katrs sērijas numurs ir:

- **Nav reģistrēts** – nav norādīts sērijas numurs vai arī reģistrētais sērijas numurs vēl nav apstiprināts (saņemšanas procesā).
- **Reģistrācija** — sērijas numurs ir reģistrēts un saglabāts veikala kanāla datu bāzē, vai arī reģistrētais sērijas numurs ir apstiprināts. Commerce galvenajā birojā tiks iesniegti tikai tie sērijas numuri, kuriem pēc saņemšanas vai izpildīšanas ir statuss **Reģistrēts**.

## <a name="receive-serialized-items"></a>Serializēto krājumu saņemšana

POS operācija **Saņemšanas krājumu** ļauj lietotājiem veikt šādus sērijas krājumu uzdevumus:

- Reģistrēt sērijas numurus, salīdzinot ar sērijas krājumiem, kad šie krājumi tiek saņemti veikalā, izmantojot pirkšanas pasūtījumu.
- Apstiprināt iepriekš reģistrētus sērijas numurus, salīdzinot ar sērijas krājumiem, kad šie krājumi tiek saņemti veikalā, izmantojot pirkšanas pasūtījumu vai pārskaitījuma pasūtījumu.

### <a name="register-serial-numbers-against-serialized-items"></a>Reģistrēt sērijas numurus ar sērijas krājumiem

Pirkšanas pasūtījumam tiks piedāvāts dialoglodziņš ar opciju **Pārvaldīt sērijas numuru** serializētā krājuma saņemšanas procesa laikā. Jūs varat atlasīt šo opciju, lai atvērtu **Sērijas numura pārvaldības** lapu un sāktu reģistrēt sērijas numurus. Jūs varat arī izlaist šo darbību saņemšanas procesa laikā un sniegt ievadi vēlāk, pirms kvīts tiek grāmatota.

Pēc noklusējuma tiek rādīta cilne pašreizējam krājumam. Visām sērijas numuru rindām ir tukša sērijas numura vērtība un statuss **Nav reģistrēts**. Jūs varat skenēt sērijas numura svītrkodus vai arī varat izvēlēties **Sērijas numuru** programmas joslā, lai pastāvīgi ievadītu sērijas numurus. Ievadītie sērijas numuri parādās sarakstā, un to statuss tiek mainīts uz **Reģistrēts**. Maksimālais sērijas numuru skaits, ko var reģistrēt sarakstā, ir vienāds ar saņemšanas daudzumu. Ja kļūdāties, varat atlasīt **Rediģēt** vai **Dzēst** rūtī **Detalizētas informācija**, lai veiktu izmaiņas ievadītajiem sērijas numuriem.

Sērijas numurus var reģistrēt arī cilnē **Visi sērijas krājumi** lapā **Sērijas numura pārvaldība**. Sarakstā atlasiet krājumu, kuru vēlaties reģistrēt ar sērijas numuriem.

### <a name="validate-serial-numbers-on-serialized-items"></a>Apstiprināt sērijas numurus sēriju krājumos

Pārsūtīšanas pasūtījumam nosūtīšanas procesa laikā sērijas numuri ir jāreģistrē sērijas krājumos. Pirkšanas pasūtījumam piegādātājs var sniegt sērijas numura informāciju, izmantojot Iepriekšējo paziņojumu par nosūtīšanu (IPPN), un jūs varat iepriekš reģistrēt numurus precēm, kas tiks nosūtītas. Abos gadījumos sērijas numuri ir zināmi pirms rēķina. Tāpēc no saņemšanas puses ir tikai jāpārbauda, vai esat saņēmis to, ko bija paredzēts saņemt.

Lai apstiprinātu sērijas numurus, varat atvērt lapu **Sērijas numura pārvaldība** vai nu saņemšanas procesa laikā, vai jebkurā laikā pirms rēķina iegrāmatošanas. Katram sēriju krājumam, kam ir sākotnēji reģistrēti sērijas numuri, šajā lapā tie automātiski tiek iestatīti uz statusu **Nav reģistrēts**. Lai apstiprinātu sērijas numurus, varat tos skenēt vai ievadīt. Kad tiek ievadīts sērijas numurs, lietojumprogramma pārbauda, vai tie atbilst ierakstītajiem sērijas numuriem. Ja tie atbilst, to statuss tiek mainīts uz **Reģistrēts**. Pretējā gadījumā tiks parādīts kļūdas ziņojums. Varat arī tieši izvēlēties sērijas numuru, pēc tam atlasīt opciju **Pārbaudīt sērijas numuru** rūtī **Detalizētā informācija**, lai ātri atzīmētu šo sērijas numuru kā validētu. Maksimālais sērijas numuru skaits, ko var apstiprināt sarakstā, ir vienāds ar saņemšanas daudzumu.

Sērijas numurus var apstiprināt arī cilnē **Visi sērijas krājumi** lapā **Sērijas numura pārvaldība**. Sarakstā atlasiet krājumu, kuru vēlaties apstiprināt ar sērijas numuriem.

## <a name="ship-serialized-items"></a>Nosūtīt serializētos krājumus

Varat izmantot POS operāciju **Izejošais krājums**, lai reģistrētu sērijas numurus attiecībā pret sērijas krājumiem, kad tie tiek piegādāti no pašreizējās krātuves, izmantojot pārsūtīšanas pasūtījumu.

### <a name="register-serial-numbers-against-serialized-items"></a>Reģistrēt sērijas numurus ar sērijas krājumiem

Pārsūtīšanas pasūtījumam tiks piedāvāts dialoglodziņš ar opciju **Pārvaldīt sērijas numuru** serializētā krājuma piegādes procesa laikā. Jūs varat atlasīt šo opciju, lai atvērtu **Sērijas numura pārvaldības** lapu un sāktu reģistrēt sērijas numurus. Jūs varat arī izlaist šo darbību piegādes procesa laikā un sniegt ievadi vēlāk, pirms piegāde tiek grāmatota.

Pēc noklusējuma tiek rādīta cilne pašreizējam krājumam. Visām sērijas numuru rindām ir tukša sērijas numura vērtība un statuss **Nav reģistrēts**. Jūs varat skenēt sērijas numura svītrkodus vai arī varat izvēlēties **Sērijas numuru** programmas joslā, lai pastāvīgi ievadītu sērijas numurus. Ievadītie sērijas numuri parādās sarakstā, un to statuss tiek mainīts uz **Reģistrēts**. Maksimālais sērijas numuru skaits, ko var reģistrēt sarakstā, ir vienāds ar piegādes daudzumu. Ja kļūdāties, varat atlasīt **Rediģēt** vai **Dzēst** rūtī **Detalizētas informācija**, lai veiktu izmaiņas ievadītajiem sērijas numuriem.

Sērijas numurus var reģistrēt arī cilnē **Visi sērijas krājumi** lapā **Sērijas numura pārvaldība**. Sarakstā atlasiet krājumu, kuru vēlaties reģistrēt ar sērijas numuriem.

Pēc izvēles var iespējot sērijas numura pieejamības pārbaudi sērijas numura reģistrācijas laikā pret izejošo pārsūtīšanas pasūtījumu. Ja tiek mēģināts nosūtīt sērijas numuru, kas nav pieejams sūtījumu krātuves krājumos, tiek parādīts kļūdas ziņojums, un tam ir jānorāda atšķirīgs numurs.

Lai iespējotu šādu validāciju, kā priekšnoteikums ir jāplāno šo darbu periodiska izpilde:

- **Retail un Commerce** > **Retail un Commerce IT** > **Preces un krājumi** > **Preču pieejamība ar izsekošanas dimensijām**
- **Retail un Commerce** > **Sadales grafiki** > **1130** (**Preču pieejamība**)

## <a name="additional-resources"></a>Papildu resursi

[Ienākošo krājumu operācija punktā POS](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Izejošo krājumu operācija punktā POS](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)


[!INCLUDE[footer-include](../includes/footer-banner.md)]