---
title: Darbs ar sērijas krājumiem punktā POS
description: Šajā tēmā skaidrots, kā pārvaldīt sērijas krājumus pārdošanas punkta (POS) lietojumprogrammā.
author: boycezhu
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 5725943fd249e1b5d66b08b829c2eb58b6aad3ee24db9ca83bbde9be906bbf82
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737582"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Darbs ar sērijas krājumiem punktā POS

[!include [banner](includes/banner.md)]

Daudzi mazumtirgotāji pārdod preces, kurām nepieciešama sērijas kontrole. Šīs preces tiek sauktas par *sērijas krājumiem*. Daži mazumtirgotāji var vēlēties saglabāt sērijas numurus krātuves vai noliktavas krājumā izsekošanas nolūkiem. Citi mazumtirgotāji pārdošanas procesa laikā var vēlēties iegūt sērijas numurus pakalpojumu un garantijas nolūkiem. Šajā tēmā skaidrots, kā jūs varat pārvaldīt sērijas krājumus Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) lietojumprogrammā.

## <a name="serial-number-configurations"></a>Sērijas numura konfigurācijas

Krājums tiek uzskatīts par sērijas krājumu, ja tam ir piešķirta izsekošanas dimensiju grupa, kas ir iestatīta, lai atļautu sērijas numurus. Commerce Headquarters lapā **Izsekošanas dimensiju grupas** atlasiet opciju **Aktīvs**, lai iespējotu krājumu procesa sērijas numurus, vai atlasiet opciju **Aktīvs pārdošanas procesā**, lai iespējotu pārdošanas procesa sērijas numurus.

Ieslēdziet parametru **Tukša kvīts atļauta** cilnē **Izsekošanas dimensijas**, lai sērijas numurs ir izvēles ievade sērijas krājumu ieejas plūsmas procesa laikā. Izslēdzot šo parametru, sērijas numurs kļūst par obligātu ievadi. Līdzīgi, parametrs **Tukšs numurs atļauts** kontrolē, vai krājumu nosūtīšanas procesa laikā ir nepieciešams sērijas numurs.

> [!NOTE]
> Lai izmantotu POS operācijas **Ienākošais krājums** un **Izejošais krājums**, lai reģistrētu vai apstiprinātu sērijas numurus pret sērijas krājumu, šis vienums ir jākonfigurē, lai tam piešķirtu izsekošanas dimensiju grupu, kas ir iestatīta, lai sērijas numuriem atļautu opciju **Aktīvs**, nevis opciju **Aktīvs pārdošanas procesā**.

## <a name="serial-number-management-page"></a>Sērijas numura pārvaldības lapa

POS operācijās **Ienākošais krājums** un **Izejošais krājums**, ja krājums, kas tiek atlasīts, saņemts vai nosūtīts, ir sērijas krājums, rūtī **Detalizēta informācija** ir ietverta opcija **Pārvaldīt sērijas numuru**, kas ir saistīta ar lapu **Sērijas numura pārvaldība**, kur var reģistrēt vai validēt krājuma sērijas numurus. Lapu **Sērijas numura pārvaldība** varat atvērt arī, vai nu atlasot **Sērijas numura** darbību pasūtījuma detalizētas informācijas skata programmas joslā vai atlasot opciju **Pārvaldīt sērijas numuru** dialoglodziņā, kurā tiek parādīts uzaicinājums saņemšanas vai piegādes procesa laikā. 

**Sērijas numura pārvaldības** lapā ir uzskaitītas visas atvērtās sērijas numura rindas, kas gaida reģistrāciju vai apstiprināšanu. Šajā lapā varētu būt divas cilnes: viena pašreizējam krājumam un cita visiem sērijas krājumiem pasūtījumā.

**Statusa** lauks lapā **Sērijas numura pārvaldība** sniedz informāciju par pašreizējo stadiju, kurā ir katrs sērijas numurs:

- **Nav reģistrēts** – nav norādīts sērijas numurs vai arī reģistrētais sērijas numurs vēl nav apstiprināts (saņemšanas procesā).
- **Reģistrācija** — sērijas numurs ir reģistrēts un saglabāts veikala kanāla datu bāzē, vai arī reģistrētais sērijas numurs ir apstiprināts. Commerce galvenajā birojā tiks iesniegti tikai tie sērijas numuri, kuriem pēc saņemšanas vai izpildīšanas ir statuss **Reģistrēts**.

## <a name="receive-serialized-items"></a>Sērijas krājumu saņemšana

POS operācija **Saņemšanas krājumi** ļauj lietotājiem veikt šādus sērijas krājumu uzdevumus:

- Reģistrēt sērijas numurus, salīdzinot ar sērijas krājumiem, kad šie krājumi tiek saņemti veikalā, izmantojot pirkšanas pasūtījumu.
- Apstiprināt iepriekš reģistrētus sērijas numurus, salīdzinot ar sērijas krājumiem, kad šie krājumi tiek saņemti veikalā, izmantojot pirkšanas pasūtījumu vai pārskaitījuma pasūtījumu.

### <a name="register-serial-numbers-against-serialized-items"></a>Sērijas numuru reģistrēšana pret sērijas krājumiem

Pirkšanas pasūtījumam tiks piedāvāts dialoglodziņš ar opciju **Pārvaldīt sērijas numuru** sērijas krājuma saņemšanas procesa laikā. Jūs varat atlasīt šo opciju, lai atvērtu **Sērijas numura pārvaldības** lapu un sāktu reģistrēt sērijas numurus. Jūs varat arī izlaist šo darbību saņemšanas procesa laikā un sniegt ievadi vēlāk, pirms kvīts tiek grāmatota.

Pēc noklusējuma tiek rādīta cilne pašreizējam krājumam. Visām sērijas numuru rindām ir tukša sērijas numura vērtība un statuss **Nav reģistrēts**. Jūs varat skenēt sērijas numura svītrkodus vai arī varat izvēlēties **Sērijas numuru** programmas joslā, lai pastāvīgi ievadītu sērijas numurus. Ievadītie sērijas numuri parādās sarakstā, un to statuss tiek mainīts uz **Reģistrēts**. Maksimālais sērijas numuru skaits, ko var reģistrēt sarakstā, ir vienāds ar saņemšanas daudzumu. Ja kļūdāties, varat atlasīt **Rediģēt** vai **Dzēst** rūtī **Detalizēta informācija**, lai veiktu izmaiņas ievadītajiem sērijas numuriem.

Sērijas numurus var reģistrēt arī cilnē **Visi sērijas krājumi** lapā **Sērijas numura pārvaldība**. Sarakstā atlasiet krājumu, kuru vēlaties reģistrēt ar sērijas numuriem.

### <a name="validate-serial-numbers-on-serialized-items"></a>Apstiprināt sērijas numurus sēriju krājumos

Pārsūtīšanas pasūtījumam nosūtīšanas procesa laikā sērijas numuri ir jāreģistrē sērijas krājumos. Pirkšanas pasūtījumam piegādātājs var sniegt sērijas numura informāciju, izmantojot Iepriekšējo paziņojumu par nosūtīšanu (IPPN), un jūs varat iepriekš reģistrēt numurus precēm, kas tiks nosūtītas. Abos gadījumos sērijas numuri ir zināmi pirms rēķina. Tāpēc no saņemšanas puses ir tikai jāpārbauda, vai esat saņēmis to, ko bija paredzēts saņemt.

Lai apstiprinātu sērijas numurus, varat atvērt lapu **Sērijas numura pārvaldība** vai nu saņemšanas procesa laikā, vai jebkurā laikā pirms rēķina iegrāmatošanas. Katram sēriju krājumam, kam ir sākotnēji reģistrēti sērijas numuri, šajā lapā tie automātiski tiek iestatīti uz statusu **Nav reģistrēts**. Lai apstiprinātu sērijas numurus, varat tos skenēt vai ievadīt. Kad tiek ievadīts sērijas numurs, lietojumprogramma pārbauda, vai tie atbilst ierakstītajiem sērijas numuriem. Ja tie atbilst, to statuss tiek mainīts uz **Reģistrēts**. Pretējā gadījumā tiks parādīts kļūdas ziņojums. Varat arī tieši izvēlēties sērijas numuru, pēc tam atlasīt opciju **Pārbaudīt sērijas numuru** rūtī **Detalizētā informācija**, lai ātri atzīmētu šo sērijas numuru kā validētu. Maksimālais sērijas numuru skaits, ko var apstiprināt sarakstā, ir vienāds ar saņemšanas daudzumu.

Sērijas numurus var apstiprināt arī cilnē **Visi sērijas krājumi** lapā **Sērijas numura pārvaldība**. Sarakstā atlasiet krājumu, kuru vēlaties apstiprināt ar sērijas numuriem.

## <a name="ship-serialized-items"></a>Sērijas krājumu nosūtīšana

Varat izmantot POS operāciju **Izejošais krājums**, lai reģistrētu sērijas numurus attiecībā pret sērijas krājumiem, kad tie tiek piegādāti no pašreizējās krātuves, izmantojot pārsūtīšanas pasūtījumu.

### <a name="register-serial-numbers-against-serialized-items"></a>Sērijas numuru reģistrēšana pret sērijas krājumiem

Pārsūtīšanas pasūtījumam tiks piedāvāts dialoglodziņš ar opciju **Pārvaldīt sērijas numuru** sērijas krājuma piegādes procesa laikā. Jūs varat atlasīt šo opciju, lai atvērtu **Sērijas numura pārvaldības** lapu un sāktu reģistrēt sērijas numurus. Jūs varat arī izlaist šo darbību piegādes procesa laikā un sniegt ievadi vēlāk, pirms piegāde tiek grāmatota.

Pēc noklusējuma tiek rādīta cilne pašreizējam krājumam. Visām sērijas numuru rindām ir tukša sērijas numura vērtība un statuss **Nav reģistrēts**. Jūs varat skenēt sērijas numura svītrkodus vai arī varat izvēlēties **Sērijas numuru** programmas joslā, lai pastāvīgi ievadītu sērijas numurus. Ievadītie sērijas numuri parādās sarakstā, un to statuss tiek mainīts uz **Reģistrēts**. Maksimālais sērijas numuru skaits, ko var reģistrēt sarakstā, ir vienāds ar piegādes daudzumu. Ja kļūdāties, varat atlasīt **Rediģēt** vai **Dzēst** rūtī **Detalizēta informācija**, lai veiktu izmaiņas ievadītajiem sērijas numuriem.

Sērijas numurus var reģistrēt arī cilnē **Visi sērijas krājumi** lapā **Sērijas numura pārvaldība**. Sarakstā atlasiet krājumu, kuru vēlaties reģistrēt ar sērijas numuriem.

Pēc izvēles var iespējot sērijas numura pieejamības pārbaudi sērijas numura reģistrācijas laikā pret izejošo pārsūtīšanas pasūtījumu. Ja tiek mēģināts nosūtīt sērijas numuru, kas nav pieejams sūtījumu krātuves krājumos, tiek parādīts kļūdas ziņojums, un tam ir jānorāda atšķirīgs numurs.

Lai iespējotu šādu validāciju, kā priekšnoteikums ir jāplāno šo darbu periodiska izpilde:

- **Retail un Commerce** > **Retail un Commerce IT** > **Preces un krājumi** > **Preču pieejamība ar izsekošanas dimensijām**
- **Retail un Commerce** > **Sadales grafiki** > **1130** (**Preču pieejamība**)

## <a name="sell-serialized-items-in-pos"></a>Sērijas krājumu pārdošana punktā POS

Lai gan POS lietojumprogramma vienmēr ir atbalstījusi sērijas krājumu pārdošanu, Commerce versijā 10.0.17 un jaunākās versijās organizācijas var iespējot funkcionalitāti, kas uzlabo biznesa loģiku, kas tiek aktivizēta, pārdodot preces, kuras ir konfigurētas sērijas numuru izsekošanai.

Ja ir iespējots līdzeklis **Uzlabota sērijas numura validācija POS pasūtījuma saņemšanā un izpildē**, pārdodot sērijas preces punktā POS, tiek novērtētas šādas preces konfigurācijas:

- **Sērijas veida** iestatījums precei (**aktīvs** vai **aktīvs pārdošanas procesā**).
- **Tukša izejas plūsma atļauta** iestatījums precei.
- **Negatīvi fiziskie krājumi** iestatījums precei un/vai pārdošanas noliktavai.

### <a name="active-serial-configurations"></a>Aktīvas sērijas konfigurācijas

Ja krājumi tiek pārdoti POS, kas konfigurēts ar **Aktīvu** sērijas numuru izsekošanas dimensiju, POS iniciē validācijas loģiku, kas neļauj lietotājiem pabeigt sērijas krājuma pārdošanu ar sērijas numuru, kas nav atrodams pārdošanas noliktavas pašreizējā krājumā. Šai pārbaudes kārtulai ir divi izņēmumi:

- Ja krājums ir konfigurēts arī ar iespējotu **Tukša izejas plūsma atļauta**, lietotāji var izlaist sērijas numura ierakstu un pārdot krājumu bez sērijas numura apzīmējuma.
- Ja krājums un/vai pārdošanas noliktava ir konfigurēta ar iespējotu **Negatīvi fiziskie krājumi**, lietojumprogramma pieņem un pārdod sērijas numuru, kuru nevar apstiprināt, vai tas atrodas noliktavas krājumā, no kuras tas tiek pārdots. Šī konfigurācija ļauj konkrētā krājuma/sērijas numura krājuma darījumam būt negatīvam, un tāpēc sistēma atļauj nezināmu sērijas numuru pārdošanu.

> [!IMPORTANT]
> Lai nodrošinātu, ka POS lietojumprogramma var pareizi validēt, vai sērijas numuri, kas tiek pārdoti kā **Aktīvi** sērijas veida krājumi, patiešām ir pārdošanas noliktavas krājumos, ir nepieciešams, lai organizācijas bieži veiktu **Preču pieejamība ar izsekošanas dimensijām** darbu Commerce Headquarters un pievienoto **1130** preču pieejamības sadales darbu, izmantojot Commerce Headquarters. Kad jauni sērijas krājumi saņemti pārdošanas noliktavās, krājumu šablonam bieži jāatjaunina kanāla datu bāze ar visjaunākajiem krājumu pieejamības datiem, lai POS varētu validēt pārdoto sērijas numuru krājumu pieejamību. Darbs **Preču pieejamība ar izsekošanas dimensijām** veic šablona krājuma momentuzņēmumu, ietverot visu uzņēmuma noliktavu sērijas numurus. Sadales darbs **1130** veic krājuma momentuzņēmuma kopīgošanu ar visām konfigurētajām kanālu datu bāzēm.

### <a name="active-in-sales-process-serial-configurations"></a>Aktīvs pārdošanas procesā sērijas konfigurācijas

Krājumi, kas konfigurēti ar sērijas dimensiju kā **Aktīvs pārdošanas procesā**, neatbilst nevienai krājumu validācijas loģikai, jo šī konfigurācija nozīmē, ka krājumu sērijas numuri nav iepriekš reģistrēti krājumos un sērijas numuri tiek saņemti tikai pārdošanas brīdī.  

Ja **Tukša izejas plūsma atļauta** ir konfigurēts arī **Aktīvs pārdošanas procesā** konfigurētajiem krājumiem, sērijas numura ierakstu var izlaist. Ja **Tukša izejas plūsma atļauta** nav konfigurēts, lietojumprogramma pieprasa lietotājam ievadīt sērijas numuru, lai gan tas netiks validēts attiecībā pret pieejamajiem krājumiem.

### <a name="apply-serial-numbers-during-creation-of-pos-transactions"></a>Sērijas numuru pielietošana POS darījumu izveides laikā

Lietojumprogramma POS nekavējoties piedāvā lietotājiem sērijas numura saņemšanu, pārdodot sērijas krājumu, bet lietojumprogramma ļauj lietotājiem izlaist sērijas numuru ievadi līdz noteiktam pārdošanas procesa punktam. Kad lietotājs sāk saņemt maksājumu, lietojumprogramma ievieš un pieprasa sērijas numura ievadi visiem krājumiem, kas nav konfigurēti izpildei, izmantojot turpmākās nosūtīšanas vai izdošanas. Jebkuram sērijas krājumam, kas konfigurēts pārdošanai skaidrā naudā bez piegādes vai tūlītējai pārdošanai, ir nepieciešams, lai lietotājs saņemtu sērijas numuru pirms pārdošanas (vai piekrīt to atstāt tukšu, ja krājumu konfigurācija to atļauj).

Sērijas krājumiem, kas pārdoti turpmākai izdošanai vai nosūtīšanai, POS lietotāji var izlaist sērijas numura sākotnēju ievadīšanu un joprojām pabeigt klienta pasūtījuma izveidi.   

> [!NOTE]
> Pārdodot vai nodrošinot izpildi sērijas precēm, izmantojot POS lietojumprogrammu, pārdošanas darījumā sērijas krājumiem tiek piemērots daudzums “1”. Tā rezultātā tiek izsekota sērijas numura informācija pārdošanas rindā. Pārdodot vai nodrošinot izpildi darījumiem ar vairākiem sērijas krājumiem, izmantojot POS, katra pārdošanas rinda ir jākonfigurē tikai ar daudzumu “1”. 

### <a name="apply-serial-numbers-during-customer-order-fulfillment-or-pickup"></a>Sērijas numuru pielietošana klienta pasūtījumu izpildes vai izdošanas laikā

Izpildot klientu pasūtījumu rindas sērijas precēm, izmantojot POS operāciju **Pasūtījuma izpilde**, POS sērijas numuru saņem pirms galīgās izpildes. Tāpēc, ja sākotnēji pasūtījuma saņemšanas laikā netika norādīts sērijas numurs, tas ir jāiegūst POS izdošanas, iepakošanas vai nosūtīšanas procesu laikā. Katrā darbībā tiek veikta validācija, un lietotājam tiks prasīts sērijas numurs tikai tad, ja tas trūkst vai tas vairs nav derīgs. Piemēram, ja lietotājs izlaiž izdošanu vai iepakošanas darbības un uzreiz uzsāk nosūtīšanu, bet sērijas numurs rindai nav reģistrēts, POS pieprasīs ievadīt sērijas numuru pirms pēdējās rēķina darbības pabeigšanas. Piemērojot sērijas numura saņemšanu, pasūtījuma operāciju izpildes laikā programmā POS, joprojām ir spēkā visi šajā tēmā iepriekš minētie noteikumi. Sērijas numura krājumu validācija attiecas tikai uz sērijas krājumiem, kas ir konfigurēti kā **Aktīvi**. Krājumi, kas ir konfigurēti kā **Aktīvi pārdošanas procesā** netiks validēti. Ja **Aktīvām** precēm ir atļauti **Negatīvi fiziskie krājumi**, tiks pieņemts jebkurš sērijas numurs neatkarīgi no krājumu pieejamības. Izdošanas, iepakošanas un nosūtīšanas darbību laikā, lietotājs var atstāt sērijas numuru lauku tukšu pēc nepieciešamības, gan **Aktīvi**, gan **Aktīvi pārdošanas procesā** krājumiem, ja ir konfigurēts **Tukša izejas plūsma atļauta**.

Sērijas numuru validācija tiks veikta arī tad, kad lietotājs veic klienta pasūtījumu izdošanu operācijām programmā POS. POS lietojumprogramma neļauj izdot sērijas preci, ja tā nav izturējusi validāciju, kā norādīts iepriekš. Validācija vienmēr tiek pamatota uz preces izsekošanas dimensiju un pārdošanas noliktavas konfigurācijām. 

## <a name="additional-resources"></a>Papildu resursi

[Ienākošo krājumu operācija punktā POS](./pos-inbound-inventory-operation.md)

[Izejošo krājumu operācija punktā POS](./pos-outbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]