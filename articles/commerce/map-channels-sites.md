---
title: Kanālu kartēšana uz e-komercijas vietnēm
description: Šajā rakstā ir aprakstīti daži no biežāk izmantotajiem kanālu kartēšanas scenārijiem Microsoft Dynamics 365 Commerce, kas var tikt papildus apskatīti lielākajai daļai citu biznesa prasību.
author: samjarawan
ms.date: 05/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 94c43df26e8d6e55a5b6d459b65066d5873e1063
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902767"
---
# <a name="map-channels-to-e-commerce-sites"></a>Kanālu kartēšana uz e-komercijas vietnēm

Šajā rakstā ir aprakstīti daži no biežāk izmantotajiem kanālu kartēšanas scenārijiem Microsoft Dynamics 365 Commerce, kas var tikt papildus apskatīti lielākajai daļai citu biznesa prasību.

Dynamics 365 Commerce atbalsta daudzus biznesa scenārijus [tiešsaistes](#channels) kanālu kartēšanai, kam ir konfigurēta preču, [cenu un atlaižu kopa klientu e-komercijas](#e-commerce-sites) vietnes pieredzei.

Šajā rakstā ir apskatīti šādi scenāriji:

- **Vienas valodas kanāls, kam ir viena e-komercijas vietnes pieredze.** Piemēram, šajā scenārijā varētu būt viena zīmola vietne, kas ir konfigurēta ASV angļu tirgū.
- **Daudzvalodu kanāls, kam ir viena lokalizēta vietu pieredze.** Piemēram, šajā scenārijā varētu būt iekļauts viens zīmola vietne, kas ir konfigurēta Kanādai ar francijas un angļu valodas atbalstu. Šajā scenārijā lietotājiem, kuri izvēlas dažādas valodas, ir viena un tā pati vietu pieredze, bet tā ir lokalizēta katra lietotāja izvēlētajā valodā.
- **Daudzvalodu kanāls, kam ir atšķirīga pieredze dažādās valodās.** Piemēram, šajā scenārijā varētu būt iekļauts viens zīmola vietne, kas ir konfigurēta Kanādai ar francijas un angļu valodas atbalstu. Šajā scenārijā katrai valodai ir unikāla vietu pieredze.
- **Vairāki kanāli (vienas valodas un/vai vairāku valodu), kuriem ir viena lokalizēta vietu pieredze.** Piemēram, šajā scenārijā varētu būt viena zīmola vietne, kas ir konfigurēta Austrālijai un Jaunzēlandei. Šajā scenārijā abām valstīm ir vienāda pieredze angļu valodā, taču katra valsts ir konfigurēta ar atšķirīgiem produktiem, valūtu, cenām, atlaidēm un nosūtīšanas režīmiem.
- **Vairāki kanāli (vienas valodas un/vai vairāku valodu), kuriem ir atšķirīga pieredze kanāla vietā.** Piemēram, šajā scenārijā varētu būt viena zīmola vietne, kas ir konfigurēta Austrālijai, Kanādai un Vācijai vairākās valodās. Šajā scenārijā katrai valstij ir unikāla pieredze vietnē, kas ir konfigurēta ar dažādiem produktiem, valūtu, cenām, atlaidēm un nosūtīšanas režīmiem.

## <a name="channels"></a>Kanāli

Kanāls (ko sauc arī par tiešsaistes veikalu vai tiešsaistes kanālu) pārstāv tiešsaistes e-komercijas veikala kontu, ko izmanto, lai kartētu preces, cenu noteikšanu, atlaides, valodas, maksājumu metodes, piegādes veidus, izpildes centrus un citus tiešsaistes pieredzes aspektus, kas būs pieejami jūsu e-komercijas klientiem. Kanāli tiek izveidoti un pārvaldīti programmā Commerce Headquarters un kartēti uz vienu [juridisku personu](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json#legal-entities). Juridiskā persona parasti ir bāzēta vienā valstī, kurai kanālam ir nepieciešami nodokļu pārskati, un to var konfigurēt tikai vienā valūtā.

Papildinformāciju par kanāliem skatiet sadaļā [Kanāla apskats](channels-overview.md). Papildinformāciju par to, kā izveidot tiešsaistes kanālu [, skatiet sadaļā Tiešsaistes kanāla iestatīšana](channel-setup-online.md).

Šajā commerce headquarters piemērā redzami noklusējuma tiešsaistes kanāli, kas tiek Dynamics 365 Commerce izvietoti, ja ir atlasīta demonstrācijas datu opcija.

![Noklusējuma demonstrācijas datu kanāli programmā Commerce Headquarters.](media/channel-mapping-1.png)

## <a name="e-commerce-sites"></a>E-komercijas vietnes

E-komercijas vietnē ir ietverta vietņu lapu kopa, ko debitori izmanto, lai pārlūkotu un iepirktos. E-komercijas vietnes tiek pārvaldītas Commerce Site Builder.

Plašāku informāciju par to, kā izveidot un pārvaldīt vietas vietas veidotājā, skatiet [e-komercijas vietnes apskatu](online-store-overview.md).

## <a name="common-channel-mapping-scenarios"></a>Kopīgie kanāla kartēšanas scenāriji

Dynamics 365 Commerce atbalsta plašu kanālu kartēšanas scenāriju klāstu. Kanāla kartēšanas scenāriji, kas seko, ir tikai visu iespējamo kanāla kartēšanas scenāriju apakškopa. Tie ir paredzēti kā ceļvedis, lai palīdzētu jums plānot jebkurus unikālus jūsu uzņēmuma scenārijus. Fiktīvais Adventure Works, kas darbojas preču Dynamics 365 Commerce veikalā, kas ir iekļauts demonstrācijas datos, tiek izmantots kā piemērs katram scenārijam.

### <a name="single-language-channel-that-has-a-single-e-commerce-site-experience"></a>Vienas valodas kanāls, kam ir viena e-komercijas vietu pieredze

Pamata scenārijā vienam kanālam ir viena valoda pārdošanai vienotā tirgū. Šāda scenārija piemērs ir Adventure Works tiešsaistes veikals, kas ir iestatīts tikai ASV angļu tirgum.

Šajā piemērā parādīts kanāla konfigurācija programmā Commerce Headquarters. Šajā konfigurācijā tiešsaistes kanāls atbalsta tikai vienu valodu (en-us **), vienu valūtu (** USD **) un vienu uzņēmumu (** **usrt**), ko izmanto nodokļu pārskatiem.

![Juridiskas personas, valūtas un valodas vērtības Adventure Works interneta veikalā, kas izcelts programmā Commerce Headquarters.](media/channel-mapping-3.png)

Vienu tiešsaistes kanālu var kartēt uz vienu e-komercijas vietni vietas veidotājā. Informāciju par to, kā izveidot jaunu vietu un kartēt to [ar kanālu,](#map-a-channel-to-a-site-in-site-builder) skatiet sadaļā Kartēt kanālu uz vietni šī raksta sadaļā Vietas veidotājs.

### <a name="multi-language-channel-that-has-a-single-localized-site-experience"></a>Vairākvalodu kanāls, kam ir viena lokalizēta vietu pieredze

Šajā scenārijā viens kanāls atbalsta vairākas valodas. Tāpēc preču nosaukumus, aprakstus un īpašības var lokalizēt galvenajā birojā Commerce Headquarters. Lai nodrošinātu pilnīgu lokalizētas vietu pieredzi, mārketinga saturu šajā vietnē var arī lokalizēt Commerce Site Builder.

Šī scenārija ierobežojums ir tāds, ka vienu kanālu var konfigurēt tikai ar vienu valūtu, vienu juridisku personu un vienu preču un cenu kopu. Šī konfigurācija vislabāk darbojas valstīm, kurām ir viena valūta un vairākas valodas (piemēram, Kanāda, kurai ir angļu un franču valodas), viena juridiska persona un viena preču un cenu kopa.

Katru kanāla valodu var konfigurēt ar savu domēna nosaukumu. Piemēram, domēnu `www.adventure-works.ca` var konfigurēt Kanādas angļu versijai, `www.adventure-works-fr.ca` un domēnu var konfigurēt Kanādas franču versijai. Alternatīva ir, ka dažādas valodas kanālā var konfigurēt vienā domēnā, un tad katrai valodai var izmantot citu ceļu. Piemēram, domēnu `www.adventure-works.ca` var konfigurēt Kanādas angļu versijai, `www.adventure-works.ca/fr` un tad ceļu var izmantot Kanādas franču versijai. [Ģeogrāfiskā noteikšana](geo-detection-redirection.md) var tikt iespējota arī, lai automātiski novirzītu lietotāju uz pareizo vietu atkarībā no lietotāja atrašanās vietas.

Papildinformāciju par to, kā aktivizēt debitorus manuālai pārslēgšanās starp valodām, [skatiet](#add-and-configure-the-site-picker-module) šī raksta sadaļā Pievienot un konfigurēt vietas izvēles moduli. Informāciju par to, kā pielāgot lokalizētās lapas un fragmentus, skatiet sadaļā [Pārvaldīt vietnes saturu, kam ir vairāki kanāli un](#manage-site-content-that-has-multiple-channels-and-languages) valodas.

### <a name="multi-language-channel-that-has-a-different-site-experience-per-language"></a>Vairākvalodu kanāls ar atšķirīgu vietu pieredzi katrai valodai

Varat dot priekšroku scenārijam, kurā viens kanāls atbalsta vairāk nekā vienu valodu, bet katrai valodai tiek atveidota pilnīgi atšķirīga vietu pieredze. Šī scenārija īstenošanas ieteiktā metode ir vienā [vietā izmantot](#implement-page-variants-for-each-language) lapu variantus.

Cita metode ir izveidot jaunu e-komercijas vietni katrai valodai vietas veidotājā un pēc tam kartēt katru vietu vienā tiešsaistes kanālā un valodā. Rezultāts būs viens tiešsaistes kanāls, kas ir kartēts vairākām e-komercijas vietnēm– viens katrā valodā. Šai vairāku vietu metodei ir nepieciešami papildu vadības resursi, jo būs vairāk nekā viena vieta, ko pārvaldīt vietas veidotājā.

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-single-localized-site-experience"></a>Vairāki kanāli (vienas valodas un/vai vairāku valodu), kuriem ir viena lokalizēta vietu pieredze

Zīmola vietai var būt nepieciešami vairāki tiešsaistes kanāli katrā reģionā, lai atbalstītu atšķirīgu valūtu, produktu kopu un cenu kopu katram kanālam vienā vietā. Piemēram, Adventure Works vietai varētu būt tiešsaistes kanāls Kanādas tirgum, kuram ir vairākas valodas, kanāls ASV tirgum, kuram ir viena valoda, un kanāls Vācijas tirgum, kurā ir viena valoda. Šajā scenārijā katrs tiešsaistes kanāls tiks konfigurēts reģionam raksturīgai juridiskajai personai, un tam var būt tāda pati preču kopa, kas ir citiem kanāliem, šo preču apakškopai vai citai preču kopai. Katram kanālam būs savas cenas reģionālajā valūtā, nodokļos, atlaidēs un nosūtīšanas režīmos.

Šajā scenārijā katru tirgu var konfigurēt ar saviem domēnu nosaukumiem. Piemēram, domēnu `www.adventure-works.com` var konfigurēt ASV tirgum, un `www.adventure-works.de` domēnu var konfigurēt Vācijas tirgum. Alternatīvi katru tirgu var konfigurēt cita ceļa izmantošanai. Piemēram, domēnu `www.adventure-works.com` var konfigurēt ASV tirgum, un tad `www.adventure-works.com/de` ceļu var izmantot Vācijas tirgum. [Ģeogrāfiskā noteikšana](geo-detection-redirection.md) var tikt iespējota arī, lai automātiski novirzītu lietotājus uz pareizo vietu, pamatojoties uz viņu reģionu.

Iespējams, vēlēsieties arī norādīt nolaižamo sarakstu, kas lietotājiem ļauj manuāli pārslēgties uz noteiktu tirgu. Papildinformāciju skatiet šī [raksta sadaļā Pievienot un konfigurēt](#add-and-configure-the-site-picker-module) vietnes atlasītāja moduli.

Informāciju par to, kā konfigurēt vairākus kanālus vienā vietā, skatiet [sadaļā Vairāku kanālu konfigurēšana e-komercijas vietnē](#configure-multiple-channels-on-an-e-commerce-site).

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-different-site-experience-per-channel"></a>Vairāki kanāli (vienas valodas un/vai vairāku valodu), kuriem ir atšķirīga pieredze attiecībā uz katru kanālu

Iespējams, vēlēsieties izveidot vairākus kanālus vienam zīmolam dažādos reģionos, un, iespējams, vēlēsieties, lai katram reģionam būtu atšķirīga vietņu pieredze. Pastāv divas metodes, kā īstenot šo scenāriju:

- Izmantot [lapu variantus](#implement-page-variants-for-each-language).
- Konfigurējiet atšķirīgu vietni katram tiešsaistes kanālam vietu veidotājā un pēc tam kartējiet katru vietni citā tiešsaistes kanālā un valodā. Šai metodei ir nepieciešami papildu vadības resursi, jo būs vairāk nekā viena vieta, ko pārvaldīt vietas veidotājā.

## <a name="cross-channel-sharing"></a>Starpkanālu koplietošana

Starpkanālu koplietošana ir noderīga, kad vienas vietnes vairāki kanāli var kopīgot saturu. Piemēram, mazumtirgotājs, kam ir vairāki zīmoli un tīmekļa vitrīnas, kas ir grupētas zem vienas vietnes, var kopīgot atsevišķu saturu starp dažām vai visām tīmekļa vitrīnām. Kopīgotais saturs var ietvert lapas noteikumiem un nosacījumiem, maksājumu nosacījumiem, nosūtīšanas metodēm un bieži uzdotiem jautājumiem (FAQ). Papildinformāciju skatiet sadaļā Starpkanālu [kopīgošanas iespējošana un izmantošana](cross-channel-sharing.md).

## <a name="map-a-channel-to-a-site-in-site-builder"></a>Kanāla kartēšana uz vietu vietas veidotājā

Pastāv vairākas metodes, kā izveidot un konfigurēt vietnes, lai izmantotu dažādus tiešsaistes kanālus.

### <a name="create-a-new-site"></a>Jauna veikala izveide

Jūs varat izveidot zīmolu jaunu vietni vietnes veidotājā, ejot uz **Vietņu** saraksta lapu un atlasot **Jauna vieta**. Pēc tam, **parādīsies** dialoglodziņā Jauna vieta, varat atlasīt noklusējuma tiešsaistes kanālu un valodu vietai, kā parādīts šajā piemēra ilustrācijā.

![Tiek veidots jauns kanāls vietu veidotājā.](media/channel-mapping-4.png)

Šādā veidā izveidota vietne būs tukša un netiks ietverta neviena vietnes lapa (piemēram, mājas lapa, kategoriju lapas un preču lapas).

Papildinformāciju skatiet [E-tirdzniecības vietnes izveide](create-ecommerce-site.md).

### <a name="create-a-new-site-by-using-the-site-copy-operation"></a>Izveidot jaunu vietni, izmantojot vietnes kopēšanas operāciju

Tā vietā, lai izveidotu zīmolu jaunu, tukšu vietni, kā aprakstīts iepriekšējā sadaļā, labāks prakse ir sākties ar kopiju vienai no sākuma vietnēm, kas tiek sniegtas Commerce moduļa bibliotēkā, piemēram, Fabrikam vai Adventure Works vietnē.

Lai kopētu esošo vietu, dodieties uz vietņu **saraksta** lapu vietas veidotājā un atlasiet Kopēt **vietu**. Pēc tam dialoglodziņā **Kopēt vietu**, kas tiek parādīta, varat atlasīt avota vietni un norādīt mērķa vietas nosaukumu.

Šajā brīdī jūs vēl nevarat atlasīt noklusējuma tiešsaistes kanālu un valodu šai vietai. Tomēr šos rekvizītus var konfigurēt pēc tam, kad ir pabeigta vietnes kopēšanas operācija. Kad jūs pirmo reizi izvēlaties vietu **Vietņu** saraksta lapā vietas veidotājā, **Parādās** Jūsu vietnes dialoglodziņš, kur jūs variet izvēlēties noklusējuma kanālu un valodu.

Papildinformāciju par vietnes kopēšanas operāciju skatiet sadaļā [E-komercijas vietnes kopēšana](copy-ecommerce-site.md).

### <a name="manage-an-existing-site-channel"></a>Pārvaldīt esošu vietnes kanālu

Pēc tam, kad vieta ir konfigurēta ar kanālu, **\> jūs varat pārvaldīt un atjaunināt kanālu no atlasītās vietas vietas veidotājā Vietnes iestatījumu kanālos**, kā parādīts šajā piemēra ilustrācijā.

![Kanāla kartēšanas pārvaldīšana vietu veidotājā;](media/channel-mapping-7.png)

## <a name="support-multiple-sites-in-a-single-tenant"></a>Atbalstīt vairākas vietas vienā nomniekā

Daudzas zīmola vietnes var līdzāspastāv viena nomnieka. Šajā piemērā redzamas trīs dažādas zīmola vietnes (Adventure Works, Adventure Works Business un Fabrikam), no kurām katra ir kartēta vienā atsevišķā tiešsaistes kanālā.

![Vietu saraksts vietu veidotājā.](media/channel-mapping-8.png)

## <a name="configure-a-single-domain-name-with-paths-for-multiple-sites"></a>Konfigurēt vienu domēna nosaukumu ar ceļiem vairākām vietnēm

Vairākām vietām var lietot vienu domēna nosaukumu, un pēc tam ceļus var izmantot, lai atdalītu vietas vai valodas. Piemēram, domēns `www.mycompany.com` ir konfigurēts divām atšķirīgām e-komercijas vietnēm: vienai Fabrikam un vienai – Adventure Works. Šajā gadījumā noklusējuma ceļu (`www.mycompany.com` kas pazīstams arī kā tukšs ceļš) var izmantot Fabrikam vietai, un citu ceļu (piemēram, `www.mycompany.com/adventureworks`) var izmantot Adventure Works vietai. Cita opcija ir izmantot pielāgotu ceļu (piemēram, `www.mycompany.com/fabrikam`) noklusējuma ceļa vietā arī Fabrikam vietai.

Alternatīvi katrai vietai (piemēram, un) var izmantot citu domēna `www.adventure-works.com` nosaukumu`www.fabrikam.com`. Pēc tam ceļus var izmantot atšķirīgām valodām vai reģioniem (piemēram, Kanādas `www.adventure-works.com/fr-ca` franču).

## <a name="configure-multiple-languages-on-a-site"></a>Konfigurējiet vairākas valodas vietnē

Valodas var konfigurēt e-komercijas vietnei vietas veidotājā vietnes **iestatījuma kanālos \>**. Šajā piemēra piemērā katra valoda ir konfigurēta, izmantojot ceļa lokalizāciju, lai katrai valodai būtu unikāls URL.

![Vairākas valodas, kas konfigurētas vietnē.](media/channel-mapping-10.png)

Lai pievienotu jaunu kanāla valodu, atveriet sadaļu **Vietnes iestatījumi \>** un atlasiet kanāla saiti. Rūtī, kas tiek parādīta labajā pusē, atlasiet **Pievienot atrašanās vietu**, lai atlasītu kanālu un atrašanās vietu, ko vēlaties pievienot. Pēc tam norādiet ceļu, ko izmantot atlasītajam kanālam.

### <a name="add-and-configure-the-site-picker-module"></a>Pievienot un konfigurēt vietas izvēles moduli

Pēc tam, kad būsiet konfigurējis vietni ar vairākām valodām un vai kanāliem, iespējams, vēlēsieties pievienot valodas atlasītāju vietnes lapas galvenei, lai lietotāji varētu manuāli atlasīt savu valodu vai valsti. Moduļa bibliotēkas [virsraksta modulis](author-header-module.md) ir iebūvēts atbalsts lietotājiem, lai atlasītu valodu, izmantojot vietas [izvēles moduli](site-selector.md). Vietas izvēles moduli var pievienot virsraksta modulim virsraksta fragmentā.

Papildinformāciju par to, kā pievienot un konfigurēt vietas izvēles moduli, skatiet vietnes [izvēles modulī](site-selector.md).

### <a name="implement-page-variants-for-each-language"></a>Implementē lapu variantus katrai valodai

Šajā scenārijā ir tikai viens kanāls, bet ir vairākas valodas. Lapas izskatu var mainīt, pamatojoties uz atlasīto valodu, izveidojot tam lapas variantu. Tad variantam var pievienot lokalizētu saturu.

Kad ir atvērta lapa vietu veidotājā un jūs atlasāt saiti augšējā labajā pusē, kas rāda pašreizējo kanālu un valodu, parādās kanāls un valodas izvēle, kā parādīts šajā piemēra attēlā. Ja vēlaties ignorēt lapu pašreizējai valodai, atlasiet citu lokalizāciju un pēc tam atlasiet **Mainīt**. Jūs varat mainīt kanālu arī tad, ja pārvaldāt [vietni ar vairākiem kanāliem un valodām](#manage-site-content-that has-multiple-channels-and-languages).

![Lapas maiņu vietas veidotājā;](media/channel-mapping-14.png)

Ja atlasītās lapas vai fragmenta variants vēl nav izveidots, tiek parādīts brīdinājuma ziņojums, kā parādīts šajā piemēra ilustrācijā. Šajā gadījumā ziņojuma tekstā atlasiet **saiti Izveidot** lapas variantu. Redzamais dialoglodziņš nodrošina opcijas, kas ļauj sākties ar esoša varianta kopiju vai izveidot no veidnes jaunu zīmolu lapu.

![Pieprasīt izveidot lapas variantu vietas veidotājā](media/channel-mapping-16.png)

Ja neizveidosit variantu, oriģinālā lapa tiek atveidota un rāda moduļu virknēm atbilstošo valodu un informāciju par preci no programmas Commerce Headquarters. Tomēr, ja teksts, piemēram, lapas nosaukums vai cits mārketinga saturs ir norādīts tieši noklusējuma lapas moduļos, šī teksta virkne paliek sākotnējā valodā.

Tā vietā, lai manuāli izveidotu katru lapu un fragmentu, jūs varat eksportēt katru lapu un fragmentu XML lokalizācijas apmaiņas faila formātā (XLIFF), kuru pēc tam var nosūtīt lokalizācijai. Kad katrs XLIFF ir lokalizēts, to var importēt kā lokalizētu lapas variantu. Lai eksportētu XLIFF failu no lapas vai fragmenta vietas veidotājā, vai lai importētu XLIFF failu lapā vai fragmentā, **atlasiet Lokalizācija** komandjoslā. Pēc tam atlasiet **Eksportēt XLIFF** vai **Import XLIFF**, kā parādīts šajā piemēra ilustrācijā.

![Notiek lapas vai fragmenta importēšana vai eksportēšana XLIFF formātā.](media/channel-mapping-18.png)

## <a name="manage-site-content-that-has-multiple-channels-and-languages"></a>Pārvaldīt vietnes saturu, kam ir vairāki kanāli un valodas

Vieta, kurā ir vairāki kanāli un/vai valodas, saglabā unikālu katras lapas variantu un fragmentu katrai kanāla kombinācijai un valodai. Šī darbība iespējo lapas variantus saturēt lokalizētus datus, bet arī sniedz jums elastīgumu, lai mainītu noteikta varianta lapas izskatu un darbību.

Lai iegūtu informāciju par to, kā strādāt ar lapas variantiem, [skatiet Implementa lapas variantus katrai](#implement-page-variants-for-each-language) valodas sadaļai šajā rakstā.

## <a name="configure-multiple-channels-on-an-e-commerce-site"></a>Vairāku kanālu konfigurēšana e-komercijas vietnē

Jūs varat pievienot kanālus e-komercijas vietnei vietas veidotājā, **izvēloties Vietnes iestatījumu \> kanālus** un izvēloties **Pievienot kanālu**. Pēc tam dialoglodziņā **Pievienot kanālu**, kas tiek parādīts, varat atlasīt tiešsaistes kanālu un noklusējuma darbības vietu.

## <a name="additional-resources"></a>Papildu resursi

[Kanālu apskats](channels-overview.md)

[Tiešsaistes kanāla iestatīšana](channel-setup-online.md)

[Organizāciju un organizāciju hierarhiju pārskats](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md)

[Ģeolokācijas noteikšanas un pārvirzīšanas iestatīšana](geo-detection-redirection.md)

[Šķērskanālu kopīgošanas iespējošana un izmantošana](cross-channel-sharing.md)

[E-komercijas vietnes izveide](create-ecommerce-site.md)

[E-komercijas vietnes kopēšana](copy-ecommerce-site.md)

[Vietas izvēles modulis](site-selector.md)
