---
title: Biznesa partneru lietotāju pārvaldīšana B2B e-komercijas tīmekļa vietnēs
description: Šajā tēmā ir aprakstīts, kā biznesa partnera lietotājus pievienot, Microsoft Dynamics 365 Commerce dzēst un rediģēt sadaļā "bizness-biznesam" (B2B) e-komercijas vietnes un programmā Commerce Headquarters.
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c2fb4846a8457296a2ce758198ade5f4b0df8124
ms.sourcegitcommit: 96e2fb26efd2cd07bbf97518b5c115e17b77a0a8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2022
ms.locfileid: "8616861"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Biznesa partneru lietotāju pārvaldīšana B2B e-komercijas tīmekļa vietnēs

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā biznesa partnera lietotājus pievienot, Microsoft Dynamics 365 Commerce dzēst un rediģēt sadaļā "bizness-biznesam" (B2B) e-komercijas vietnes un programmā Commerce Headquarters.

> [!NOTE]
> - Tēma [Pārvaldīt B2B biznesa partnerus, izmantojot debitoru hierarhijas](partners-customer-hierarchies.md) ir šī dokumenta priekšnosacījums.
> - Pārliecinieties, ka inicializējiet dokumentu tipu elementu programmā Commerce headquarters, atverot dokumentu **tipu** formu organizācijas administrēšanas **dokumentu \> pārvaldības dokumentu \> tipos**.

B2B e-komercijas tīmekļa vietnes pieprasa, lai organizācijas reģistrētos kļūt par biznesa partneriem. Kad organizācija iesniedz reģistrācijas datus B2B e-komercijas vietnei, reģistrācijas pieprasījums tiek apstrādāts kvalifikācijas procesā. Ja organizācija ir sekmīgi kvalificēta, tā tiek pievienota kā biznesa partneris.

Kad organizācija ir pievienota kā biznesa partneris, organizācijas lietotājs, kurš ierosināja pieprasījumu kļūt par biznesa partneri, tiek identificēts kā administrators un tam tiek piešķirtas privilēģijas pievienot papildu autorizētus lietotājus B2B e-komercijas tīmekļa vietnei. Šie autorizētie lietotāji var veikt pasūtījumus biznesa partnera vārdā.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Administratora iestatīšana jaunam biznesa partnerim

Potenciālie biznesa partneri var uzsākt uzņēmumā esošās darbības procesu B2B e-komercijas vietnē, iesniedzot onboarding pieprasījumu, izmantojot saiti B2B vietnē. Tad viņi var izmantot pielāgojamu formu, lai sniegtu detalizētu informāciju, kas nepieciešamaboardingam un pierakstīšanāsi. Pēc pieprasījuma iesniegšanas tiek parādīta iesniegšanas apstiprinājuma lapa. Ja iesniegšana tiek apstiprināta, uzņēmums, kam tika iesniegts pieprasījums, kļūst par biznesa partneri, un pieprasītājs (lietotājs, kas uzsākis pieprasījumu) kļūst par biznesa partnera administratoru.

Lai apstiprinātu biznesa partnera pieprasījumu programmā Commerce Headquarters, izpildiet šīs darbības.

1. Dodieties uz **Retail un Commerce IT \> Sadales grafiks**.
1. Palaidiet **P-0001** darbu, lai visus biznesa partneru pievienošanas pieprasījumus nogādātu Commerce Headquarters.
1. **Kad P-0001** darbs ir veiksmīgi izpildīts, **dodieties uz Retail and Commerce IT \> Customer** **un palaidiet debitoru sinhronizēšanas un kanāla pieprasījumu** darbu. Kad šis darbs ir veiksmīgi izpildīts, uzņēmuma commerce headquarters uzņēmuma B2B **potenciālo klientu tipa potenciālie pieprasījumi tiek izveidoti, izmantojot esošos pieprasījumus**. 
1. Dodieties uz **Visi \> potenciālie klienti** un atlasiet jauno biznesa partnera potenciālā klienta ierakstu, lai atvērtu detalizētas informācijas lapu par potenciālo klientu.
1. Cilnē Vispārīgi **atlasiet** Pārvērst apstiprināšanu **\>/noraidīšanu,** lai apstiprinātu onboarding pieprasījumu. Kad parādās apstiprinājuma ziņojums, apstipriniet, ka vēlaties turpināt procesu, un tad apstipriniet pieprasījumu. Apstiprināšana izmaina potenciālā **klienta** ieraksta statusa lauku uz **Apstiprināts**. Pēc tam uz pieprasītāja e-pasta adresi tiek nosūtīts e-pasta ziņojums, apstiprinot, ka viņa organizācija ir apstiprināta kā biznesa partneris. Tiek izveidota arī debitoru hierarhija, kur pieprasītājs ir pievienots kā biznesa partnera administrators.

    > [!NOTE]
    > Pašlaik apstiprinājuma e-pasta ziņojums tiek nekavējoties nosūtīts pēc apstiprināšanas. Tomēr nākamā Commerce funkcionalitāte ļaus administratoram manuāli aktivizēt e-pasta ziņojumus.

1. Dodieties uz **mazumtirdzniecības un Commerce IT \>** **sadales grafiku un palaidiet darbu 1010 (Debitori),** lai jaunos debitoru un debitoru hierarhijas ierakstus virzītu uz kanāla datu bāzi.

> [!NOTE]
> Lai nodrošinātu, ka jaunie debitoru ieraksti tiek sūtīti uz kanāla datu bāzi, ar debitoru saistītajām adrešu grāmatām ir jāiekļauj vismaz viena no debitora adrešu grāmatām, kas ir saistītas ar tiešsaistes veikalu. Jūs varat automatizēt šo procesu, konfigurējot adrešu grāmatu tiešsaistes veikala noklusējuma debitoram, lai sistēma kopētu adrešu grāmatas vērtību katram jaunam debitoram.

Kad debitora hierarhijas ieraksti ir sinhronizēti ar kanāla datu bāzi, pieprasītājs var pieteikties B2B e-komercijas vietnē, izmantojot e-pasta adresi, ko tie sniedza, kad tie iesniedza uzņēmuma pieprasījumu. Lietotāji var izmantot pierakstīšanās plūsmu, lai definētu sava konta paroli. Informāciju par to, kā Azure Active Directory iespējot (Azure AD) B2C identitātes nodrošinātāja ierakstu, ko saistīt ar B2B debitora ierakstu, kas tika izveidots potenciālā klienta apstiprinājumā, [skatiet Sadaļā Iespējot automātisko saistīšanu](../identity-record-linking.md).

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>Paziņot B2B potenciālajiem klientiem, ja tie tiek apstiprināti vai noraidīti

Apstiprinot vai noraidot B2B potenciālo klientu darba pieprasījumā, automātiski var nosūtīt e-pasta paziņojumu potenciālā klientam.

Lai programmā Commerce headquarters **iestatītu e-pasta paziņojumus par B2B** **potenciālā klienta apstiprinātajiem notikumiem vai B2B** potenciālā klienta noraidīto paziņojumu veidu, veiciet šīs darbības.

1. Izveidojiet e-pasta veidnes e-pasta ziņojumiem, kas tiks nosūtīti potenciālajiem ziņojumiem, ja ir izraisīts **vai nu B2B** **potenciālais klients, vai B2B potenciālā** klienta noraidīts paziņojuma veids. Informāciju par vietturiem, kurus atbalsta šie paziņojumu tipi, skatiet paziņojumu [tipos](../email-templates-transactions.md#notification-types). Papildinformāciju par e-pasta veidņu izveidi skatiet [E-pasta veidnes izveide](../email-templates-transactions.md#create-an-email-template).
1. **Pievienojiet B2B potenciālo klientu apstiprinātos** **un B2B** potenciālo klientu noraidīto paziņojumu tipus savam e-pasta paziņojuma profilam un pēc tam kartējiet tos uz jūsu izveidotajām e-pasta veidnēm. Informāciju par to, kā iestatīt paziņojumu profilus, skatiet [E-pasta paziņojuma profila iestatīšana](../email-notification-profiles.md).

## <a name="onboard-additional-business-partner-users"></a>Papildu biznesa partneru lietotāju pievienošana

Biznesa partnera administratos var pievienot papildu biznesa partnera lietotājus B2B e-komercijas tīmekļa vietnē pēc vajadzības.

Lai B2B e-komercijas tīmekļa vietnei pievienotu papildu biznesa partnera lietotājus, veiciet tālāk norādītās darbības.

1. Pierakstieties B2B e-komercijas tīmekļa vietnē kā administrators.
1. Dodieties uz **Mans konts \> Organizācijas lietotāji \> Skatīt detalizētu informāciju** un atlasiet **Pievienot lietotāju**.
1. Ievadiet nepieciešamo informāciju un pēc tam atlasiet **Saglabāt**. Jauna lietotāja statuss ir iestatīts kā **Gaida**.

**Pēc tam, kad ir palaisti P-0001** **un** Sinhronizēt debitoru un kanāla pieprasījumu darbus, **jaunajam** programmas Commerce Headquarters lietotājam tiek izveidots debitora tipa ieraksts. Šis klienta ieraksts ir saistīts arī ar attiecīgā biznesa partnera klienta hierarhijas ierakstu. Turklāt uz jauno lietotāju e-pasta adresi tiek nosūtīts e-pasts, lai paziņotu, ka viņi ir pievienoti kā biznesa partnera organizācijas lietotāji un tagad var pierakstīties B2B e-komercijas tīmekļa vietnē.

Pēc tam palaidiet darbu **1010 (Debitori),** lai sinhronizētu jauno biznesa partnera lietotāju kanāla datu bāzē.

Kad debitora ieraksts ir sinhronizēts, lietotāja statuss B2B e-komercijas **vietnē** ir iestatīts uz Aktīvs, un jaunais lietotājs var pieteikties B2B e-komercijas vietnē, izmantojot viņu e-pasta adresi. Lietotāji var izmantot pierakstīšanās plūsmu, lai definētu sava konta paroli. Informāciju par to, kā Azure AD iespējot B2C identitātes nodrošinātāja ierakstu, ko saistīt ar B2B debitora ierakstu, kas tika izveidots programmā Commerce Headquarters, [skatiet sadaļā Iespējot automātisko saistīšanu](/dynamics365/commerce/identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>Biznesa partnera lietotāja datu rediģēšana

Lai rediģētu biznesa partnera lietotāju informāciju, veiciet tālāk norādītās darbības.

1. Pierakstieties B2B e-komercijas tīmekļa vietnē kā administrators.
1. Dodieties uz **Mans konts \> Organizācijas lietotāji \> Skatīt detalizētu informāciju**, atlasiet pogu **Rediģēt** (zīmuļa simbols), veiciet nepieciešamās izmaiņas un pēc tam atlasiet **Saglabāt**. Izmaiņas stājas spēkā tikai pēc P-0001 **,** Sinhronizēt **debitorus un kanāla pieprasījumus un** ir palaisti 1010 (Debitori) **darbi.**

## <a name="remove-a-business-partner-user"></a>Biznesa partnera lietotāja noņemšana

Pēc vajadzības administrators no lietotāju saraksta var noņemt esošos biznesa partnera organizācijas lietotājus, kuri var piekļūt B2B e-komercijas tīmekļa vietnei.
Lai noņemtu biznesa partnera lietotāju, veiciet tālāk norādītās darbības.
- Pierakstieties B2B e-komercijas tīmekļa vietnē kā administrators.
- Pārejiet **uz sadaļu Mani > organizācijas lietotāju \> skata** dati un atlasiet pogu **Noņemt** (simbols X). Kad parādās apstiprinājuma ziņojums, apstipriniet, ka vēlaties noņemt lietotāju. Izmaiņas stājas spēkā tikai pēc P-0001 **,** Sinhronizēt **debitorus un kanāla pieprasījumus,** un ir palaisti 1010 (Debitori) **darbi.**

> [!NOTE]
> Noņemot lietotāju no to lietotāju saraksta, kuri var piekļūt B2B e-komercijas tīmekļa vietnei, atbilstošais klienta ieraksts tiek noņemts no biznesa partnera klientu hierarhijas ieraksta. Tomēr pats klienta ieraksts netiek dzēsts no Commerce Headquarters.

## <a name="onboard-existing-customers-as-business-partners-on-the-b2b-e-commerce-website"></a>Esošie debitori kā biznesa partneri B2B e-komercijas vietnē

Administratori var pievienot biznesa partnerus un lietotājus tieši Commerce Headquarters. Šī iespēja ir noderīga, ja ieturēsiet esošos biznesa partnerus B2B e-komercijas vietnē.

Lai pievienotu biznesa partnerus un lietotājus Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Izveidojiet vai atlasiet organizācijas tipa **debitoru**, ko pievienot kā biznesa partneri.
1. Izveidojiet vai atlasiet personas tipa **debitoru**, ko biznesa partnerim pievienot kā administratoru vai lietotāju. Pārliecinieties, ka primārās e-pasta adreses ir saistītas ar debitoriem. Šīs e-pasta adreses tiek izmantotas, lai pieteiktos vietnē. 

    > [!NOTE]
    > Sistēmai jāresistē atrast unikālu debitora ierakstu lietotājiem, kuriem vajadzētu būt iespējai pieteikties vietnē. Ja sistēma atrod vairāk nekā vienu debitoru, kuram juridiskā persona ir tāda pati primārā e-pasta adrese, lietotājs nevarēs pieteikties vietnē.

1. Izveidojiet klientu hierarhijas ID.
1. Laukā **Nosaukums** ievadiet nosaukumu.
1. Laukā **Organizācija** ievadiet biznesa partnera organizācijas klientu.
1. Kopsavilkuma cilnē **Hierarhija** atlasiet **Pievienot**.
1. Laukā **Nosaukums** atlasiet personas tipa **debitoru**.
1. **Atlasiet administratora** lomu debitoram, kas jānorāda kā administrators.
1. Atkārtojiet šo procesu, lai hierarhijai pievienotu vairāk debitoru.

## <a name="additional-information"></a>Papildinformācija

- Visus šajā tēmā minētos darbus var konfigurēt, lai tie tiktu izpildīti pēc grafika pakešuzdevuma formātā. Paredzams, ka biznesa partneri konfigurēs pakešuzdevumus pēc vajadzības.
- Pašlaik tikai vienu lietotāja/klienta ierakstu var norādīt kā administratoru, un šo lomu var mainīt tikai komponentā Commerce Headquarters. Pašapkalpošanās iespējām nav atbalsta, kas biznesa partneriem ļautu izraudzīties vairākus administratorus vai mainīt administratorus no B2B e-komercijas tīmekļa vietnēm.
- Lai gan izdevumu ierobežojumus lietotājiem var noteikt, izdevumu ierobežojumu izpilde pasūtījuma iesniegšanas procesā vēl nav ieviesta.
- Visa biznesa loģika un validācijas lietotāja pieredzei B2B e-komercijas tīmekļa vietnē ir balstītas uz tā klienta ieraksta konfigurāciju, kas ir kartēta lietotājam komponentā Commerce Headquarters.

## <a name="additional-resources"></a>Papildu resursi

[B2B e-komercijas vietnes iestatīšana](set-up-b2b-site.md)

[B2B biznesa partneru pārvaldība, izmantojot debitoru hierarhijas](partners-customer-hierarchies.md)

[Klienta konta maksājuma metodes konfigurēšana B2B e-komercijas vietnēs](payment-method.md)

[Preču daudzuma ierobežojumu iestatīšana B2B e-komercijas vietnēs](quantity-limits.md)

[Pārskats par numuru sērijām](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
