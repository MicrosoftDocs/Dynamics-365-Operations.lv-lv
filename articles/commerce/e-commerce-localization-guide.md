---
title: Dynamics 365 Commerce e-commerce lokalizācijas ceļvedis
description: Šajā rakstā ir aprakstīts, kā lokalizēt Microsoft Dynamics 365 Commerce e-komercijas vietni papildu valodās un konfigurēt vietu, lai atbalstītu vairākus kanālus.
author: bicyclingfool
ms.date: 04/29/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 955a85340f6d35f1e203d74920d07b5dc6ff8654
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873388"
---
# <a name="dynamics-365-commerce-e-commerce-localization-guide"></a>Dynamics 365 Commerce e-commerce lokalizācijas ceļvedis

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, Microsoft Dynamics 365 Commerce kā lokalizēt e-komercijas vietni papildu valodās un konfigurēt vietu, lai atbalstītu vairākus kanālus, kā arī ietvertas koncepcijas un terminoloģija, kas saistīta ar šo procesu.

E-komercijas Dynamics 365 Commerce iespējas ir veidotas, lai iespējotu tiešsaistes pieredzi, ko var pielāgot noteiktām valstīm un valodām, bet tajā pašā laikā atļaut veidņu, lapu, satura un plašsaziņas līdzekļu maksimālo atkārtotu izmantošanu. Varat arī izveidot pamata vietu un pēc tam paplašināt jaunās tirgus, pievienojot papildu valstu un valodu atbalstu laika gaitā.

## <a name="definitions"></a>Definīcijas

**Darbības vieta, atrašanās vietas** identifikators: atrašanās vieta (ko sauc arī par lokalizācijas identifikatoru) definē valodu, kas saistīta ar valsti vai reģionu. Piemēram, atrašanās vietas identifikators "fr-ca" ir saistīts ar Kanādas franču.

**Pamatvaloda**: valoda, kurā jūsu veidojat vietnes saturu, pirms to eksportējat lokalizācijai.

**Kanāls, tiešsaistes** veikals: kanāls (ko sauc arī par tiešsaistes veikalu) nosaka maksājumu metodes, cenu grupas, preču hierarhijas, preču klāstu un produktus tiešsaistes e-komercijas veikalam.

## <a name="concepts"></a>Koncepcijas

### <a name="url-driven-experience"></a>Vietrāža URL vadāmā pieredze

Dynamics 365 Commerce e-komercijas vietas nodrošina unikālu marketizētu un lokalizētu pieredzi klientiem caur kanāliem un atrašanās vietas identifikatoriem. Kanāli definē unikālus tirgus produktus, kategorijas, valūtas un maksājumu metodes, kā arī atrašanās vietas identifikatorus nosaka debitoru skatītā satura valodu. E-komercijas vietne izmanto vietrāžus URL, lai atšķirtu tirgus un lokalizēto pieredzi. Vietnes vietrāži URL šiem unikālajam kanālam un atrašanās vietas pieredze ir definēti vietai vietnes **iestatījumu kanālu \> lapā** vietņu veidotājā Dynamics 365 Commerce.

Vietas veidotājā URL ir domēna kombinācija un ceļš, kas nosaka ieejas punktu unikālai kanāla un darbības vietas kombinācijai. Šajā piemērā fiktīvais tiešsaistes veikals Fabrikam Inc. definē četras unikālas kanāla un darbības vietas kombinācijas un kartē katru kombināciju uz unikālu URL, kas kalpo saturam klientiem.

| Domēns                     |  Ceļš      | Kanāls       |   Atrašanās     |
|------------------------|--------|--------------------------------|--------|
| `https://fabrikam.com` | /      | Fabrikam paplašinātais tiešsaistes veikals | lv  |
| `https://fabrikam.com` | /es    | Fabrikam paplašinātais tiešsaistes veikals | es     |
| `https://fabrikam.ca`  | /      | Contoso tiešsaistes veikals    | fr-ca  |
| `https://fabrikam.ca`  | /en-ca | Contoso tiešsaistes veikals    | en-ca  |

#### <a name="domain"></a>Domēns

Domēni tiek izveidoti, kad iestatāt e-komercijas vietni pakalpojumā Microsoft Dynamics Lifecycle Services (LCS). Kad jūsu e-komercijas vide ir nodrošināta, jūs varat pievienot vairāk domēnu, atverot pakalpojuma pieprasījumu. Papildinformāciju par to, kā iestatīt domēnus jūsu e-komercijas vietnei, skatiet sadaļā [Domēni Dynamics 365 Commerce](domains-commerce.md).

#### <a name="path"></a>Ceļš

- Ceļš ir auklas virkne, kas kombinācijā ar domēnu ir kartēta uz unikālu kanāla un lokalizācijas kombināciju. Iepriekšējā piemērā virkne, kas tiek izmantota kā ceļš, atbilst atrašanās vietas identifikatoram, uz kuru ceļš ir kartēts. Taču jūs varat izmantot citu pieeju.
- Kanāla un lokalizācijas kombināciju var kartēt uz domēnu un tukšu ceļu ("/"). Iepriekšējā piemērā debitori, kuri `https://fabrikam.ca/` apmeklēs, saņems produktus un klāstu Kanādas tirgū Kanādas franču valodā.
- Komercijas vietnes veidotājs neļauj izveidot dublētas domēna un ceļa kombinācijas. Tomēr jūs varat kartēt kanāla un lokalizācijas kombinācijas citā domēna un ceļa kombinācijā.

#### <a name="channel"></a>Kanāls

- Kanāli (ko sauc arī par tiešsaistes veikaliem) definē maksājumu metodes, cenu grupas, preču hierarhijas, preču klāstu un preces tiešsaistes e-komercijas veikalam.
- Kanāli ir definēti, konfigurēti un publicēti galvenajā birojā Dynamics 365 Commerce.
- Vietas veidotājs var noteikt tiešsaistes veikalus, kas ir konfigurēti Commerce Headquarters un ir pieejami kartēt uz vietu.

Papildinformāciju par kanāliem skatiet sadaļā [Kanālu apskats](channels-overview.md). Papildinformāciju par to, kā iestatīt tiešsaistes kanālu, [skatiet sadaļā Tiešsaistes kanāla iestatīšana](channel-setup-online.md).

#### <a name="locale"></a>Atrašanās

- Atrašanās vietas ir faktiskais identifikators, ko izmanto, kad tiek nodota XML lokalizācijas apmaiņas faila formāta (XLIFF) faili lokalizācijai. Atrašanās vietas tiek definētas un publicētas katram commerce headquarters kanālam. Informāciju par to, kā konfigurēt valodas un kanālus vietas veidotājā, skatiet nākamajā sadaļā.
- Vienu lokalizāciju var kartēt uz vairākiem kanāliem. Šādā veidā iespējams piedāvāt kopēju valodu vairākos tirgus piedāvās.

## <a name="configure-languages-and-channels-for-your-e-commerce-site"></a>Konfigurēt valodas un kanālus jūsu e-komercijas vietnei

Ārpus lodziņa visas e-komercijas vietnes ir konfigurētas tā, Dynamics 365 Commerce lai izmantotu vienu tiešsaistes kanālu un vienu valodu neatkarīgi no tā, vai sākat ar Fabrikam demonstrācijas vietni vai izveidojat jaunu vietu no jauna.

Šajā konfigurācijā debitori un partneri parasti izstrādā visus līdzekļus, ko izmantos valstīs un valodās. Šie līdzekļi ietver veidnes, lapas, fragmentus, saturu un medijus. Viss vietnes saturs tiek izstrādāts pirmajā valodā, ko atlasījāt jūsu vietnei, vai, ja izmantojat Fabrikam demonstrācijas vietni, vietnes saturs tiks izstrādāts angļu valodā.

![Ārpus kastes Dynamics 365 Commerce e-komercijas vietnes](media/loc-guide-1.png)

> [!NOTE]
> Jūs varat konfigurēt Fabrikam demonstrācijas vietni papildu valodai, lai varētu veikt satura attīstību šajā valodā. Papildinformāciju par to, kā vietnei un kanālam pievienot jaunu valodu, [skatiet](#configure-an-additional-language-for-your-site) tālāk šī raksta sadaļā Papildu valodas konfigurēšana vietnei.

Tomēr satura pārvaldības sistēma (CMS) Dynamics 365 Commerce un e-komercijas vietņu lapas modelis ir veidoti, lai iespējotu paplašināto tirgu un vietējos tirgus. Tādējādi, izmantojot vienu e-komercijas vietni, varat pārvaldīt līdzekļus tiešsaistes veikalam, kas aptver vairākus tirgus un valodas.

![Dynamics 365 Commerce e-komercijas vieta, kas aptver daudzus tirgus un valodas](media/loc-guide-2.png)

### <a name="configure-an-additional-language-for-your-site"></a>Konfigurējiet papildu valodu jūsu vietnei

E-komercijas vietnes jaunas valodas konfigurēšanas procesam ir trīs soļi.

#### <a name="step-1-add-the-language-to-your-channel-online-store-in-commerce-headquarters"></a>1. darbība: valodas pievienošana programmas Commerce Headquarters kanālam (interneta veikals)

1. Programmā Commerce headquarters dodieties uz kanālu, kuram vēlaties pievienot jauno valodu. Lai atrastu to kanālu sarakstu, ko esat konfigurējis programmā Commerce Headquarters, dodieties uz Mazumtirdzniecības **un Commerce \> kanālu \> tiešsaistes veikaliem**.
1. Atveriet tiešsaistes veikalu, kas ir kartēts jūsu vietnē, atlasot tā mazumtirdzniecības **kanāla ID** vērtību. Varat pārbaudīt uz jūsu **vietni** **kartēto tiešsaistes veikalu, atverot Kanālu vietnes iestatījumu lapu Komercijas vietņu veidotājā un meklējot tiešsaistes veikala nosaukumu kolonnā** Kanāli. 
1. Kopsavilkuma cilnē **Valodas** atlasiet **Pievienot**. Laukā **Valoda** atlasiet jaunās valodas lokalizācijas kodu. Pēc tam atlasiet **Saglabāt**.
1. Dodieties uz **grafiku \> Mazumtirdzniecība un Commerce Retail un Commerce IT \> sadale** un palaidiet darbu **1070 kanāla konfigurāciju**. Kad darbs ir pabeigts, varat pārvietoties uz 2. soli un pievienot valodu kanālam jūsu vietā izstrādātājā.

![Programmu Commerce Headquarters tiešsaistes veikala valodu kopsavilkuma cilne](media/loc-guide-3.png)

#### <a name="step-2-add-the-language-to-a-channel-in-site-builder"></a>2. solis. Valodas pievienošana kanālam vietas veidotājā

Lai pievienotu valodu kanālam vietas veidotājā, sekojiet šiem soļiem.

1. Commerce Site Builder atveriet savu vietni un pēc tam atveriet kanālu lapu **vietnes** iestatījumos.
1. Atlasiet tā kanāla nosaukumu, kuram vēlaties pievienot valodu.
1. Labās puses rūtī atlasiet **Pievienot atrašanās vietu**.
1. Dialoglodziņa Pievienot **atrašanās vietu** sadaļā Pievienot atrašanās vietu atlasiet tās valodas atrašanās vietu, **kas** iepriekš pievienota kanālam programmā Commerce Headquarters.
1. Atlasiet domēnu un ceļu, ko debitori pieprasīs skatīt jūsu vietni šajā kanālā un valodā.
1. Ja vēlaties, lai valoda būtu noklusējuma valoda vietas veidotāja lapu un fragmentu skatīšanai, izveidošanai un atjaunināšanai, **atzīmējiet izvēles rūtiņu Izmantot kā noklusējuma autorēšanas** kanāla valodu. 
    > [!NOTE]
    > Šis iestatījums ietekmē tikai vietas veidotāju. Tas neietekmē publicēto vietņu pieredzi jūsu klientiem.
1. Atlasiet **Labi**.
1. Atlasiet **Saglabāt un publicēt**.

#### <a name="step-3-localize-your-site-content"></a>3. solis. Vietnes satura lokalizācija

Kad atgriezīsieties **Commerce Site** Builder skatījumā Lapas, jaunā valoda būs pieejama kanālā un atrašanās vietas izvēle augšējā labajā pusē. Tagad varat izveidot lokalizētās lapu versijas savā pamatvalodā.

Jūsu lapu un fragmentu satura lokalizēšanas process ir iekļauts e-komercijas [vietnes](#localize-e-commerce-site-content) satura sadaļā lokalizācija tālāk šajā rakstā.

### <a name="configure-a-new-channel-for-your-site"></a>Konfigurējiet jaunu kanālu jūsu vietnei

Dynamics 365 Commerce E-komercijas vietnes var kalpot pieredzei, kas ir definēta vairākos tiešsaistes kanālos, kas ir konfigurēti programmā Commerce Headquarters. Vieta izmanto vairākus kanālus, lai parādītu debitoriem unikālu maksājumu metožu konfigurāciju, cenu grupas, preču hierarhijas, preču klāstu un preču kopu. Kanāls parasti tiek izmantots, lai konfigurētu šīs dimensijas atbilstoši prasībām un preferences pieredzei, kas saistīta ar atsevišķām valstīm. Tomēr šī pieeja ir klienta lēmumu pieņēmējs. Tā nav prasība.

Priekšnosacījumi un uzdevumi, kas ir saistīti ar kanāla (tiešsaistes veikala) iestatīšanu, pārsniedz šī dokumenta darbības jomu. Papildinformāciju par tiešsaistes kanāla iestatīšanu programmā Commerce Headquarters skatiet sadaļā Kanāla [iestatīšanas pamati](channels-overview.md#channel-setup-basics). Papildinformāciju par tiešsaistes kanāliem specifiskajām darbībām un prasībām skatiet [sadaļā Tiešsaistes kanāla iestatīšana](channel-setup-online.md).

Lai pievienotu kanālu jūsu vietnei vietas veidotājā, sekojiet šiem soļiem.

1. Commerce Site Builder atveriet sadaļu Vietnes **iestatījumi \>**. 
1. Atlasiet **Pievienot kanālu**.
1. **Sadaļas Kanāla dialoglodziņa** pievienošana sadaļā **Kanāls atlasiet** kanālu, ko vēlaties pievienot. 
    > [!NOTE]
    > Varat pievienot tikai kanālus, kas nav jau pievienoti jūsu vietnei.
1. Atlasiet kanāla noklusēto darbības laiku. Ja kanālam pievienojat jaunas valodas, varat mainīt noklusējuma valodu uz kādu no tām.
1. Norādiet domēnu un ceļu, kas veido URL, kas kalpo saturam un pieredzei kanāla un valodas kombinācijai.
1. Atlasiet **Labi**.
1. Atlasiet **Saglabāt un publicēt**.

## <a name="localize-e-commerce-site-content"></a>Lokalizēt e-commerce vietnes saturu

### <a name="xliff-basics"></a>XLIFF pamati

XLIFF ir nozares standarta faila formāts lokālajam satura nodošanai starp satura pārvaldības rīkiem. Commerce Site Builder izmanto XLIFF faila formātu, lai eksportētu lapu, fragmentu un attēla metadatu saturu tā, lai to varētu lokalizēt un no jauna importēt.

Microsoft Dynamics Debitori parasti strādā ar trešās puses lokalizācijas kreditoriem, [piemēram, Translated.com](https://translated.com/welcome) tekstus XLIFF failiem nepieciešamajās valodās.

### <a name="localize-assets-in-site-builder"></a>Lokalizēt līdzekļus vietas veidotājā

Šādi e-komercijas vietnes līdzekļi var tikt lokalizēti vietas veidotājā:

- Lapas
- Fragmenti
- Līdzekļu līdzekļi
- Moduļi

Visas jaunās lapas, fragmenti un plašsaziņas līdzekļi tiek veidoti kanāla un valodas kontekstā, kas pašreiz atlasīti kanālā un atrašanās vietas izvēlei. Šī valoda parasti ir jūsu "pamatvaloda", ja nav konfigurētas papildu valodas vai kanāli. Vietnēs, kurās ir konfigurēti vairāki kanāli un valodas, "pamatvaloda" **tiek** definēta pēc kanāla un atrašanās vietas, ko esat iestatījis kā noklusējumu kanāla lapā vietnes iestatījumos.

Darbības lapu, fragmentu un plašsaziņas līdzekļu satura lokalizēšanai ir līdzīgas. Izņēmumi un atšķirības tiks norādīts turpmākās sadaļās. Tomēr darbības moduļa satura lokalizēšanai atšķiras. Papildinformāciju skatiet tālāk šī [raksta](#localize-modules) sadaļā Lokalizēt moduļus.

#### <a name="step-1-export-an-xliff-file"></a>1. darbība: XLIFF faila eksportēšana

Lai eksportētu XLIFF failu lapas, fragmenta vai attēlam vietas veidotājā, sekojiet šiem soļiem.

1. Atveriet līdzekli, kam vēlaties eksportēt pamatvalodas saturu, lai to varētu lokalizēt.
1. Komandjoslā atlasiet Lokalizācijas **Eksportēt \> XLIFF**.
    > [!NOTE]
    > Lokalizācijas **opcija** ir redzama tikai tad, ja pamatlīdzeklis ir rediģēšanas **stāvoklī**.

XLIFF fails ar nosaukumu **\<assetname\>.xlf** tiks lejupielādēts jūsu pārlūkprogrammas lejupielādes mapē. Šis XLIFF fails ir specifisks pamatlīdzeklim, ko lokalizē. XLIFF failu eksportējat katram pamatlīdzeklim, kuru vēlaties lokalizēt.

#### <a name="step-2-localize-the-xliff-file"></a>2. darbība. XLIFF faila lokalizācija

Parasti strādāsit ar lokalizācijas kreditoru, lai tulkotu XLIFF failus. Tomēr, ja pamatlīdzekļus lokalizējat iekšēji vai vēlaties tikai pārbaudīt lokalizācijas procesu, XLIFF failā veiciet šādas izmaiņas:

- Pievienojiet mērķa valodas atribūtu elementam /xliff/file un iestatiet vērtību tās valodas atrašanās vietas identifikatoram, uz kuru vēlaties lokalizēt. 
    > [!NOTE]
    > Šim atrašanās vietas identifikatoram ir jāatbilst atrašanās vietas identifikatoram **vietnes** iestatījumu lapā Kanāli.
- Katram/avota elementam pievienojiet mērķa elementu atvasi, kur teksta vērtība ir šī avota elementa satura lokalizētā versija.

Informāciju par shēmu, kas pārvalda XLIFF failus, skatiet [XLIFF 1.2 specifikāciju](http://docs.oasis-open.org/xliff/xliff-core/xliff-core.html).

> [!NOTE]
> Lai lokalizētu līdzekli vairākās valodās, ir jāizveido lokalizēts XLIFF fails katrai no šīm valodām.

#### <a name="step-3-import-the-localized-xliff-file"></a>3. darbība. Lokalizētā XLIFF faila importēšana

Lai importētu XLIFF failu pamatlīdzeklim, sekojiet šiem soļiem.

1. Commerce Site Builder atveriet līdzekli, kam vēlaties importēt XLIFF failu.
1. Kanāla un lokalizācijas atlasītājā augšējā labajā pusē atlasiet kanālu un valodu, kam importējat lokalizēto saturu.
1. Komandjoslā atlasiet lokalizācijas **importēšanas \> XLIFF**. Pēc tam pārlūkojiet un atlasiet lokalizēto XLIFF failu atlasītajam līdzeklim un valodai.

Kad XLIFF fails ir veiksmīgi importēts, tiek izveidots lapas, fragmenta vai pamatlīdzekļa "variants". No šī laika uz priekšu visas lokalizētajā variantā veiktās izmaiņas ietekmēs tikai šo variantu. Tās neietekmēs bāzes līdzekli, no kā variants tika iegūts. Arī pamatlīdzekļa izmaiņas neietekmēs šī pamatlīdzekļa variantu. 

Tomēr lapu gadījumā izmaiņas variantos var veikt, modificējot veidni vai izkārtojumu, kam šīs lapas ir piesaistītas. Tāpat fragmenta izmaiņas ietekmēs visas lapas, kas izmanto atkarību no šī varianta.

### <a name="images"></a>Attēli

Attēlus var renderēt lapas vai moduļa variantā tikai tad, ja ir lokalizēti ar šiem attēliem saistītie satura metadati. Pašlaik lokāli var izmantot šādus metadatus plašsaziņas līdzekļa līdzekļos:

- Alternatīvais teksts
- Apraksts
- Nosaukums

Pašlaik nevar lokalizēt bināro vērtību digitālam pamatlīdzeklim, piemēram, attēlam vai video. Preču Dynamics 365 Commerce grupa pašlaik strādā pie šīs iespējas.

### <a name="localize-modules"></a>Lokalizēt moduļus

Virknes, kas ir atveidotas kā daļa no pašā moduļa (piemēram, "Iepriekšējais" un "Tālāk" modulī) ir lokalizētas atsevišķi no moduļa satura. Norādījumus skatiet sadaļā [Moduļa lokalizācija](e-commerce-extensibility/localize-module.md).

## <a name="additional-resources"></a>Papildu resursi

[Lapas modeļa glosārijs](page-elements-overview.md)

[Starpkanālu koplietošana](cross-channel-sharing.md)

[Moduļa lokalizēšana](e-commerce-extensibility/localize-module.md)

[Moduļa definīciju fails](e-commerce-extensibility/module-definition-file.md)

[Commerce paplašinājumu resursu un etiķešu failu lokalizēšana](dev-itpro/extension-resource-localization.md)

[Globalizēt moduļus, izmantojot klasi CultureInfoFormarag](e-commerce-extensibility/globalize-modules.md)

[Lietojumprogrammas iestatījumi: tēmas](e-commerce-extensibility/app-settings.md#themes-section)
