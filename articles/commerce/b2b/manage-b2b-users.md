---
title: Biznesa partneru lietotāju pārvaldīšana B2B e-komercijas tīmekļa vietnēs
description: Šajā tēmā aprakstīts, kā administratori var pievienot, rediģēt un dzēst biznesa partneru lietotājus bizness-biznesam (B2B) e-komercijas tīmekļa vietnēs.
author: josaw1
ms.date: 10/26/2021
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
ms.openlocfilehash: 090dc9af49840e559b4c1ad1500718fde9764aa2
ms.sourcegitcommit: 6bf9e18989e6d77497a9dda1c362f324b3c2fbf2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/27/2021
ms.locfileid: "7713697"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Biznesa partneru lietotāju pārvaldīšana B2B e-komercijas tīmekļa vietnēs

[!include [banner](../../includes/banner.md)]

Šajā tēmā aprakstīts, kā administratori var pievienot, rediģēt un dzēst biznesa partneru lietotājus bizness-biznesam (B2B) e-komercijas tīmekļa vietnēs.

B2B e-komercijas tīmekļa vietnes pieprasa, lai organizācijas reģistrētos kļūt par biznesa partneriem. Pēc tam, kad organizācija iesniedz reģistrācijas datus B2B e-komercijas tīmekļa vietnē, tai ir jāveic kvalifikācijas process. Ja organizācija ir sekmīgi kvalificēta, tā tiek pievienota kā biznesa partneris.

Kad organizācija ir pievienota kā biznesa partneris, organizācijas lietotājs, kurš ierosināja pieprasījumu kļūt par biznesa partneri, tiek identificēts kā administrators un tam tiek piešķirtas privilēģijas pievienot papildu autorizētus lietotājus B2B e-komercijas tīmekļa vietnei. Šie autorizētie lietotāji var veikt pasūtījumus biznesa partnera vārdā.

## <a name="turn-on-the-b2b-e-commerce-capabilities-feature-in-commerce-headquarters"></a>B2B e-komercijas iespēju līdzekļa ieslēgšana Commerce Headquarters

B2B e-komercijas iespēju līdzeklis komponentā Commerce Headquarters ļauj organizācijām pievienot biznesa partnerus un definēt administratorus. Šis līdzeklis arī iespējo administratorus izveidot un pārvaldīt biznesa partnera lietotājus un darba grupas, kā arī piešķirt tiem specifiskas lomas. Visbeidzot, tas iespējo biznesa partnera lietotājus izveidot pasūtījumu veidnes un izmantot esošos pasūtījumus, lai pārkārtotu preces.

Lai ieslēgtu B2B e-komercijas iespēju līdzeki Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Dodieties uz **Darbvietas \> Līdzekļu pārvaldība**.
1. Cilnē **Visi** filtrējiet lauku **Modulis**, izmantojot terminu **Mazumtirdzniecība un komercija**.
1. Atrodiet un atlasiet līdzekli ar nosaukumu **Iespējot B2B e-komercijas iespēju izmantošanu** un pēc tam atlasiet **Iespējot tūlīt**.

## <a name="create-a-number-sequence-and-add-it-to-commerce-shared-parameters"></a>Numuru sērijas izveidošana un pievienošana Commerce kopīgotajiem parametriem

Numuru sērijas tiek izmantotas, lai ģenerētu lasāmus, unikālus identifikatorus pamatdatu ierakstiem un transakciju ierakstiem, kam ir nepieciešami identifikatori. Papildinformāciju par numuru sērijām skatiet nodaļā [Numuru sēriju pārskats](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).

Lai izveidotu numuru sēriju un to pievienotu Commerce kopīgotajiem parametriem komponentā Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Dodieties uz **Retail un Commerce \> Headquarters iestatīšana \> Numuru sērijas \> Numuru sērijas** un izveidojiet numuru sēriju.
1. Dodieties uz **Retail un Commerce \> Headquarters iestatīšana \> Parametri \> Commerce kopīgotie parametri** un pievienojiet jaunu numuru sēriju **Klientu hierarhijas ID** atsaucei.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Administratora iestatīšana jaunam biznesa partnerim

Potenciālie biznesa partneri var uzsākt pievienošanas procesu B2B e-komercijas tīmekļa vietnē, iesniedzot pievienošanas pieprasījumu, izmantojot saiti vietnē. Kad potenciālā biznesa partnera lietotāji atlasa saiti, viņi var sniegt informāciju, kas nepieciešama, lai pievienotos un pierakstītos. Pēc pieprasījuma iesniegšanas tiek parādīta iesniegšanas apstiprinājuma lapa. Ja iesniegtais pieprasījums tiek apstiprināts, pieprasītājs (t.i., lietotājs, kurš uzsāka pievienošanas pieprasījumu) kļūst par biznesa partnera administratoru.

Lai apstiprinātu un iestatītu biznesa partnera administratoru komponentā Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Dodieties uz **Retail un Commerce IT \> Sadales grafiks**.
1. Palaidiet **P-0001** darbu, lai visus biznesa partneru pievienošanas pieprasījumus nogādātu Commerce Headquarters.
1. Pēc veiksmīga **P-0001** darba izpildes, dodieties uz **Mazumtirdzniecības un tirdzniecības IT \> Klients** un palaidiet darbu **Sinhronizēt klientus un biznesa partnerus no asinhronā režīma**. Kad šis darbs ir veiksmīgi izpildīts, pievienošanas pieprasījumi tiek izveidoti kā potenciālo klientu ieraksti Commerce Headquarters. Šo ierakstu lauks **Tipa ID** ir iestatīts kā **B2B potenciālais klients**.
1. Dodieties uz **Klienti \> Visi potenciālie klienti** un atveriet potenciālo klientu lapu.
1. Atlasiet potenciālā klienta ierakstu jaunajam biznesa partnerim, lai atvērtu potenciālā klienta informācijas lapu.
1. Cilnē **Vispārīgi** atlasiet **Konvertēt \> Apstiprināt/Noraidīt**, lai apstiprinātu vai noraidītu pievienošanas pieprasījumu. Kad parādās apstiprinājuma ziņojums, apstipriniet, ka vēlaties turpināt procesu un apstipriniet pieprasījumu. Pēc tam uz pieprasītāja e-pasta adresi tiek nosūtīts e-pasta ziņojums, apstiprinot, ka viņa organizācija ir apstiprināta kā biznesa partneris.

    Pēc pieprasījuma apstiprināšanas potenciālā klienta ieraksta lauks **Statuss** tiek iestatīts uz **Apstiprināts**. Turklāt sistēmā tiek izveidoti divi jauni klientu ieraksti: **Organizācijas tipa** klienta ieraksts biznesa partnera organizācijai un **Personas tipa** klienta ieraksts pieprasītājam. Biznesa partnerim tiek izveidots arī klientu hierarhijas ieraksts. <!--(Please refer to the Org modeling of B2B customer section in this document for more information)-->

1. Dodieties uz **Mazumtirdzniecības un tirdzniecības IT \> Sadales grafiks** un palaidiet **1010** (**Klienti**) darbu, lai pievienotu jaunizveidoto klientu un klientu hierarhijas ierakstus kanāla datu bāzei.

Pēc pieprasījuma apstiprināšanas, arī klientu un klientu hierarhijas ierakstu sinhronizēšanas ar kanālu datu bāzi, pieprasītājs var pierakstīties B2B e-komercijas tīmekļa vietnē, izmantojot e-pasta adresi, ko tas norādījis, iesniedzot pieprasījumu. Lietotāji var izmantot pierakstīšanās plūsmu, lai definētu sava konta paroli. Lai iespējotu identitātes nodrošinātāja (Azure AD B2C) ierakstu, kas jāsaista ar B2B debitora ierakstu, kas tika izveidots, reģistrējoties vai pierakstoties, izpildiet norādījumus sadaļā [Iespējot automātisku identitātes ierakstu saistīšanu ar debitora kontiem](../identity-record-linking.md).

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>Paziņot B2B potenciālajiem klientiem, ja tie tiek apstiprināti vai noraidīti

Apstiprinot vai noraidot B2B potenciālo klientu darba pieprasījumā, varat automātiski nosūtīt e-pasta paziņojumu potenciālajam klientam. 

Lai programmā Commerce Headquarters iestatītu e-pasta paziņojumus par B2B potenciālā klienta apstiprinātajiem notikumiem vai B2B potenciālā klienta noraidīto paziņojumu veidu, veiciet šīs darbības.

1. Izveidojiet e-pasta veidnes e-pasta ziņojumiem, kas tiks nosūtīti potenciālajiem ziņojumiem, ja B2B potenciālais klients ir apstiprināts, vai B2B potenciālā klienta noraidītā paziņojuma veids tiek parādīts.

    Informāciju par vietturiem, ko B2B potenciālais klients apstiprināja un B2B potenciālā klienta noraidīto paziņojumu tipu atbalstu, skatiet [Paziņojumu tipus](../email-templates-transactions.md#notification-types). Papildinformāciju par e-pasta veidņu izveidi skatiet [E-pasta veidnes izveide](../email-templates-transactions.md#create-an-email-template). 

1. Pievienojiet B2B potenciālo klientu apstiprinātos un B2B potenciālo klientu noraidīto paziņojumu tipus savam e-pasta paziņojuma profilam un kartējiet tos uz jūsu izveidotajām e-pasta veidnēm. Informāciju par to, kā iestatīt paziņojumu profilus, skatiet [E-pasta paziņojuma profila iestatīšana](../email-notification-profiles.md). 

## <a name="onboard-additional-business-partner-users"></a>Papildu biznesa partneru lietotāju pievienošana

Biznesa partnera administratos var pievienot papildu biznesa partnera lietotājus B2B e-komercijas tīmekļa vietnē pēc vajadzības.

Lai B2B e-komercijas tīmekļa vietnei pievienotu papildu biznesa partnera lietotājus, veiciet tālāk norādītās darbības.

1. Pierakstieties B2B e-komercijas tīmekļa vietnē kā administrators.
1. Dodieties uz **Mans konts \> Organizācijas lietotāji \> Skatīt detalizētu informāciju** un atlasiet **Pievienot lietotāju**.
1. Ievadiet nepieciešamo informāciju un pēc tam atlasiet **Saglabāt**. Jauna lietotāja statuss ir iestatīts kā **Gaida**.

    Pēc **P-0001** un **Sinhronizēt klientus un biznesa partnerus no asinhronā režīma** darbu izpildes **Personas tipa** klienta ieraksts jaunam lietotājam tiek izveidots komponentā Commerce Headquarters. Šis klienta ieraksts ir saistīts arī ar attiecīgā biznesa partnera klienta hierarhijas ierakstu. Turklāt uz jauno lietotāju e-pasta adresi tiek nosūtīts e-pasts, lai paziņotu, ka viņi ir pievienoti kā biznesa partnera organizācijas lietotāji un tagad var pierakstīties B2B e-komercijas tīmekļa vietnē.

1. Palaidiet **1010** (**Klienti**) darbu, lai sinhronizētu jauno biznesa partnera lietotāju ar kanālu datu bāzēm.

Pēc klienta ieraksta sinhronizēšanas lietotāja statuss B2B e-komercijas tīmekļa vietnē ir iestatīts uz **Aktīvs**, un jaunais lietotājs var pierakstīties B2B e-komercijas tīmekļa vietnē, izmantojot savu e-pasta adresi. Lietotāji var izmantot pierakstīšanās plūsmu, lai definētu sava konta paroli. Lai iespējotu identitātes nodrošinātāja (Azure AD B2C) ierakstu, kas jāsaista ar B2B debitora ierakstu, kas tika izveidots, reģistrējoties vai pierakstoties, izpildiet norādījumus sadaļā [Iespējot automātisku identitātes ierakstu saistīšanu ar debitora kontiem](../identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>Biznesa partnera lietotāja datu rediģēšana

Lai rediģētu biznesa partnera lietotāju informāciju, veiciet tālāk norādītās darbības.

1. Pierakstieties B2B e-komercijas tīmekļa vietnē kā administrators.
1. Dodieties uz **Mans konts \> Organizācijas lietotāji \> Skatīt detalizētu informāciju**, atlasiet pogu **Rediģēt** (zīmuļa simbols), veiciet nepieciešamās izmaiņas un pēc tam atlasiet **Saglabāt**. Izmaiņas stājas spēkā tikai pēc **P-0001**, **Sinhronizēt klientus un biznesa partnerus no asinhronā režīma** un **1010** (**Klienti**) darbu izpildes.

## <a name="remove-a-business-partner-user"></a>Biznesa partnera lietotāja noņemšana

Pēc vajadzības administrators no lietotāju saraksta var noņemt esošos biznesa partnera organizācijas lietotājus, kuri var piekļūt B2B e-komercijas tīmekļa vietnei.

Lai noņemtu biznesa partnera lietotāju, veiciet tālāk norādītās darbības.

1. Pierakstieties B2B e-komercijas tīmekļa vietnē kā administrators.
1. Dodieties uz **Mans konts \> Organizācijas lietotāji \> Skatīt detalizētu informāciju** un atlasiet **Noņemt** pogu (“X” simbols). Kad parādās apstiprinājuma ziņojums, apstipriniet, ka vēlaties noņemt lietotāju. Izmaiņas stājas spēkā tikai pēc **P-0001**, **Sinhronizēt klientus un biznesa partnerus no asinhronā režīma** un **1010** (**Klienti**) darbu izpildes.

> [!NOTE]
> Noņemot lietotāju no to lietotāju saraksta, kuri var piekļūt B2B e-komercijas tīmekļa vietnei, atbilstošais klienta ieraksts tiek noņemts no biznesa partnera klientu hierarhijas ieraksta. Tomēr pats klienta ieraksts netiek dzēsts no Commerce Headquarters.

## <a name="onboard-business-partner-and-users-in-commerce-headquarters"></a>Pievienotie biznesa partneri un lietotāji komponentā Commerce Headquarters

Administratori var pievienot biznesa partnerus un lietotājus tieši Commerce Headquarters.

Lai pievienotu biznesa partnerus un lietotājus Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Izveidojiet biznesa partnera organizācijai **Organizācijas tipa** klienta ierakstu.
1. Izveidojiet biznesa partnera lietotājiem **Personas tipa** klienta ierakstus. Pārliecinieties, vai katram klientam ir norādīta primārā e-pasta adrese.
1. Katram **Personas tipa** klienta ierakstam, kas jānorāda kā biznesa partnera organizācijas administrators, kopsavilkuma cilnē **Retail** iestatiet **B2B administratora** opciju uz **Jā**.
1. Izveidojiet klientu hierarhijas ID. Laukā **Nosaukums** ievadiet nosaukumu.
1. Laukā **Organizācija** ievadiet biznesa partnera organizācijas klientu.
1. Atlasiet **Pievienot** un pēc tam laukā **Nosaukums** atlasiet klientu.
1. Atkārtojiet šo procesu, lai hierarhijai pievienotu papildu klientus.

## <a name="additional-information"></a>Papildinformācija

- Visus šajā tēmā minētos darbus var konfigurēt, lai tie tiktu izpildīti pēc grafika pakešuzdevuma formātā. Paredzams, ka biznesa partneri konfigurēs pakešuzdevumus pēc vajadzības.
- Pašlaik tikai vienu lietotāja/klienta ierakstu var norādīt kā administratoru, un šo lomu var mainīt tikai komponentā Commerce Headquarters. Pašapkalpošanās iespējām nav atbalsta, kas biznesa partneriem ļautu izraudzīties vairākus administratorus vai mainīt administratorus no B2B e-komercijas tīmekļa vietnēm.
<!--- The modules and labels of the different fields referenced in the screenshots for e-commerce are only for illustration purposes. Customers have complete control on the placement of the B2B related modules and the labels.-->
- Lai gan izdevumu ierobežojumus lietotājiem var noteikt, izdevumu ierobežojumu izpilde pasūtījuma iesniegšanas procesā vēl nav ieviesta.
- Visa biznesa loģika un validācijas lietotāja pieredzei B2B e-komercijas tīmekļa vietnē ir balstītas uz tā klienta ieraksta konfigurāciju, kas ir kartēta lietotājam komponentā Commerce Headquarters.

## <a name="additional-resources"></a>Papildu resursi

[B2B e-komercijas vietnes iestatīšana](set-up-b2b-site.md)

[Organizāciju hierarhiju modelēšanas izveidošana B2B organizācijām](org-model.md)

[Klienta konta maksājuma metodes konfigurēšana B2B e-komercijas vietnēs](payment-method.md)

[Preču daudzuma ierobežojumu iestatīšana B2B e-komercijas vietnēs](quantity-limits.md)

[Pārskats par numuru sērijām](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
