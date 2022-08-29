---
title: Darbs ar stila sākotnējiem iestatījumiem
description: Šajā rakstā ir aprakstīts, kā strādāt ar vietas stila iestatījumiem vietas veidotājā Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ea22c4c50a25c18d25980b8d2ce9bcf8cd315e87
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267517"
---
# <a name="work-with-style-presets"></a>Darbs ar stila sākotnējiem iestatījumiem

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā strādāt ar vietas stila iestatījumiem vietas veidotājā Microsoft Dynamics 365 Commerce.

Stilu priekšiestatījums ir uzglabāta visu atļaujamo stila vērtību kopa visā vietnes dizainā. To var izmantot, lai nekavējoties mainītu vietnes izskatu no vietnes veidotāja. Stila priekšiestatījumi ļauj Commerce vietnes būvētāja autoriem ātri mainīt, priekšskatīt un aktivizēt stila vērtību kopu visā savā vietnē bez nepieciešamības izmantot kaskadētās stilu lapas (CSS) vai izvietot dizainus. Fontu stili, pogu stili un vietnes krāsas ir raksturīgi stila mainīgo piemēri, kurus var pārvaldīt, izmantojot stila priekšiestatījumus.

Stila mainīgo kopu, kas ir pieejama vietnē, nosaka dizainu un moduļu bibliotēka, kura ir izvietota vietnes nomniekam. Dynamics 365 Commerce tiešsaistes programmatūras izstrādes komplekts (SDK) ļauj izstrādātājs ieviest tik daudz (vai tik maz) atļaujamos stila mainīgos, cik tiem ir nepieciešami konkrētajam dizainam. Iespējojot vairāk stila mainīgos, dizaina izstrādātājs var nodot galīgo izvēli par vietnes stiliem vietnes veidotāja autoru rokās. Tāpēc personas, kas nav izstrādātāji, var atjaunināt un priekšskatīt vietnes stilus, izmantojot rīku komplektu. Šī iepēja ir noderīga arī ikvienam scenārijam, kurā tiešas izmaiņas dizainos vai CSS izraisīs nevajadzīgas pieskaitāmās izmaksas.

Dizainos, kuros ir iespējoti atļaujamie stila mainīgie, ir nepieciešams noklusējuma stila priekšiestatījums. Tās pēc izvēles var iekļaut papildu iepriekšiestatītās opcijas kā daļu no izvietotas dizaina pakotnes. Piemēram, var izvietot dizainu, kam ir viens noklusējuma "Modern Light" stila priekšiestatījums. Tāpat tas var ietvert papildu stila priekšiestatījuma opcijas papildus noklusētajam priekšiestatījumam, piemēram, "modern dark", "vintage light" vai "vintage dark". Šos iebūvētos dizaina priekšiestatījumus izveido izstrādātāji un tos var izmantot par jaunu vietnes noformējumu sākuma punktiem.

Vietnes veidotājā autori var izvēlēties no dizaina iebūvētajiem priekšiestatījumiem vai arī var izveidot savus stila priekšiestatījumus un pielāgojumus, izmantojot iespējotos stila mainīgos. Stila priekšiestatījumu var priekšskatīt vietnes veidotājā, pirms tas ir aktivizēts tiešsaistes vietnē. Kad autora stila izmaiņas ir pārskatītas, tad stila priekšiestatījumu tiešsaistes vietnei var iestatīt kā "aktīvu".

## <a name="preview-a-style-preset"></a>Stila priekšiestatījuma priekšskatīsana

Lai priekšskatītu stilu priekšiestatījumu savā vietnē vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Vietnes kreisajā navigācijas rūtī dodieties uz **Vietnes iestatījumi \> Noformējums**.
1. Cilnē **Stila priekšiestatījumi**, kas atrodas noformējuma redaktora augšējā malā, sarakstā **Pieejamie priekšiestatījumi** atlasiet priekšiestatījumu un pēc tam atlasiet **Skatīt**, lai dotos uz priekšiestatījumu redaktoru.

    Ja sarakstā **Pieejamie priekšiestatījumi** pašlaik nav priekšiestatījumu, skatiet sadaļu [Pielāgota stila priekšiestatījumu izveide](#create-a-custom-style-preset) informācijai par to, kā izveidot pielāgotu stila priekšiestatījumu.

    > [!NOTE]
    > Priekšiestatījumi, kas bija iekļauti dizainā, ir atzīmēti ar žetonu **Iebūvēts**. Šie iebūvētie priekšiestatījumi ir tikai lasāmi. Lai kopētu iebūvēto priekšiestatījumu kā jaunu pielāgojamu priekšiestatījumu, atlasiet priekšiestatījuma daudzpunktes pogu (**...**) un pēc tam atlasiet **Saglabāt kā**.

1. Komandjoslā atlasiet **Priekšskatīt**.
1. Atlasiet URL no jūsu vietnes, lai to izmantotucstila priekšiestatījuma priekšskatīšanai un pēc tam atlasiet **Labi**.
1. Atlasiet kanālam raksturīgo un lokalizācijai raksturīgo URL variantu, lai priekšskatītu, atlasot varianta nosaukumu. Tiek atvērts jauns priekšskatījuma pārlūkprogrammas logs, kurā atlasītais stila priekšiestatījums tiek lietots norādītajai lapai.

> [!NOTE]
> Priekšskatījuma URL ir pastāvīgs un autentisks. Tāpēc jūs varat kopēt, ielīmēt un nosūtīt to citiem autentificētiem kolēģiem pārskatīšanai, pirms iestatāt to uz "aktīvs" savā tiešsaistes vietnē. Priekšskatījuma URL ir arī noderīgs, lai pārbaudītu stilus dažādās ierīcēs, dažādās pārlūkprogrammās un dažādos ekrānos.

> [!TIP]
> Rediģējot stila priekšiestatījumu, var būt noderīgi atstāt tā priekšskatījuma pārlūkprogrammas logu atvērtu atsevišķā pārlūkprogrammas logā, lai jūs varētu ātri validēt veiktās izmaiņas. Pēc izmaiņu saglabāšanas priekšiestatījumā atsvaidziniet atvērto priekšskatījuma pārlūkprogrammas logu, lai validētu lietotāja pieredzi.

## <a name="create-a-custom-style-preset"></a>Pielāgota stila priekšiestatījuma izveide

Lai izveidotu pielāgotu stilu priekšiestatījumu vietnes veidotājā, izpildiet tālāk norādītās darbības.

1. Vietnes kreisajā navigācijas rūtī dodieties uz **Vietnes iestatījumi \> Noformējums**.
1. Cilnē **Stilu priekšiestatījumi**, kas atrodas noformējuma redaktora augšējā malā, komandjoslā atlasiet **Jauns priekšiestatījums**.
1. Ievadiet jaunā priekšiestatījuma nosaukumu un aprakstu un pēc tam atlasiet **Saglabāt**. Tiek izveidots jauns pielāgojams priekšiestatījums, kas izmanto dizaina noklusētās vērtības kā sākuma punktu.

> [!NOTE]
> Varat arī izveidot jaunu pielāgotu stila priekšiestatījumu no jebkura esoša priekšiestatījuma, izvēloties daudzpunktes pogu (**...**) šim priekšiestatījumam un pēc tam atlasot **Saglabāt kā**. Varat arī izvēlēties **Saglabāt kā** komandjoslā priekšiestatījuma redaktorā.

## <a name="modify-global-and-module-type-style-values"></a>Globālo un moduļa veida stila vērtību modificēšana

Daži no dizaina stila mainīgajiem tiek koplietoti vairākos moduļu veidos. Šie stilu mainīgie tiek saukti par *globāliem* stila mainīgiem. Piemēri ietver primārās vietnes krāsas, noklusējuma fontu stilus un pogu stilus. Iestatot globālos mainīgos, var mainīt daudzu dažādu moduļa veidu izskatu.

Dažas stila vērtības var būt unikālas moduļa veidam, vai arī tām var būt nepieciešams pēc izvēles ignorēt noklusējuma globālo vērtību. Ja vietnes dizains ir ieviesis moduļa veida stila mainīgos, vietnes veidotāja autori var pielāgot moduļa veida stilu neatkarīgi no globālajiem iestatījumiem. Moduļa veida mainīgie var palielināt vai ignorēt globālo stilu mainīgos dizainā.

> [!NOTE]
> Stila vērtību hierarhija vietnē darbojas tālāk minētajā veidā. Stila vērtības, kas parādās tālāk pa labi, ignorē stila vērtības pa kreisi no tām.
>
> Dizaina noklusējuma vērtības \< Globālās stila vērtības \< Moduļa veida stila vērtības \< CSS ignorēt

Lai mainītu stila priekšiestatījuma globālās vai moduļa veida vērtības vietnes veidotājā, veiciet tālāk norādītās darbības.

1. Vietnes kreisajā navigācijas rūtī dodieties uz **Vietnes iestatījumi \> Noformējums**.
1. Cilnē **Stila priekšiestatījumi**, kas atrodas noformējuma redaktora augšējā malā, atlasiet **Skats** jebkuram stila priekšiestatījumam, lai pārietu uz priekšiestatījuma redaktoru.
1. Atlasiet **Priekšskatīt** un pēc tam izpildiet URL atlases darbības, lai atvērtu pilna pārlūka loga priekšskatījumu jūsu priekšiestatījumam. Atstājiet šo priekšskatījuma pārlūka logu atvērtu.
1. Priekšiestatījuma redaktora augšējā labajā stūrī atlasiet **Rediģēt**.
1. Lai mainītu dažas globālās stila vērtības, redaktorā izmantojiet stila mainīgo vadīklas.
1. Redaktora augšā cilnē **Moduļi** pa labi no cilnes **Globāls** atlasiet moduļa veidu, kam jāpiemēro stils.
1. Izmantojiet stila vadīklas, lai mainītu dažas moduļa veida vērtības.
1. Kad esat gatavs priekšskatīt veiktās izmaiņas, komandjoslā atlasiet **Saglabāt**.
1. Atgriezieties atvērtajā priekšskatījuma pārlūkprogrammas logā un atsvaidziniet to. Pilna pārlūka logu priekšskatījums noder, lai pārbaudītu stila izmaiņas dažādos skatījuma pārtraukumpunktos, dažādās pārlūkprogrammās un dažādās ierīču platformās.
1. Kad visas izmaiņas ir pabeigtas un validētas, redaktora augšējā labajā stūrī atlasiet **Pabeigt rediģēšanu**.

> [!NOTE]
> Ja rediģējat stila iestatījumu, kas pašlaik ir aktīvs jūsu vietnē, redaktorā redzēsit zilu žetonu **Aktīvs**. Šis žetons norāda, ka priekšiestatījums pašlaik ir tiešsaistē jūsu vietnē. Ja maināt aktīvo priekšiestatījumu, atlasiet **Publicēt**, lai izstumtu šīs izmaiņas savā tiešsaistes vietnē.

## <a name="make-a-new-style-preset-active-on-your-live-site"></a>Jauna stila priekšiestatījuma aktivizēšana jūsu tiešsaistes

Lai iestatītu stila priekšiestatījumu kā jauno aktīvo priekšiestatījumu savā vietnē, izpildiet tālāk norādītās darbības.

- Atlasiet pogu **Iestatīt kā aktīvu** vienā no tālāk minētajām vietām.

    - Komandjosla stila priekšiestatījuma redaktorā
    - Daudzpunktes izvēlne (**...**) jebkuram pieejamam priekšiestatījumam galvenajā skatā, kas atrodas cilnē **Stila priekšiestatījumi** **Vietnes iestatījumi \> Noformējums**

Priekšiestatījuma stila vērtības tiek aktivizētas visā publiski redzamajā vietnē.

## <a name="additional-resources"></a>Papildu resursi

[Logotipa pievienošana](add-logo.md)

[Vietnes dizaina atlase](select-site-theme.md)

[Darbs ar CSS ignorēšanas failiem](css-override-files.md)

[Izlases ikonas pievienošana](add-favicon.md)

[Autortiesību paziņojuma pievienošana](add-copyright-notice.md)

[Valodu pievienošana vietnei](add-languages-to-site.md)

[Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
