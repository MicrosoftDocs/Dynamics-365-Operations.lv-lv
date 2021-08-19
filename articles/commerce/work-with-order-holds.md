---
title: Zvanu centra pasūtījumu aizturēšanas konfigurēšana un darbs ar to
description: Šajā tēmā ir aprakstīts, kā strādāt ar pasūtījumu aizturēšanu, izmantojot Dynamics 365 Commerce.
author: josaw1
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans, MCROrderEventSetup, MCROrderEventTable
audience: Application User
ms.reviewer: josaw
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f474b5936f2ae154ad54185becd91865642e8efe3cf10e7dcdbb650c6c833b21
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762600"
---
# <a name="configure-and-work-with-call-center-order-holds"></a>Zvanu centra pasūtījumu aizturēšanas konfigurēšana un darbs ar to

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstītas pasūtījumu aizturēšanas funkcijas, kuras ir ietvertas programmā Dynamics 365 Commerce zvanu centra pasūtījumiem.

## <a name="configuring-call-center-order-holds"></a>Zvanu centra pasūtījumu konfigurēšana

Lai izmantotu zvanu centra pasūtījumu aizturēšanas funkcijas, vispirms ir jānorāda aizturēšanas kodi. Lai izveidotu lietotāja definētu aizturēšanas kodu kopu, pamatojoties uz jūsu uzņēmuma prasībām, dodieties uz **Pārdošana un mārketings** \> **Iestatījumi** \> **Pārdošanas pasūtījumi** \> **Pasūtījumu aizturēšanas kodi**. Jūs varat pēc izvēles atzīmēt ar karodziņu vienu no aizturēšanas kodiem kā noklusējuma aizturēšanas kodu, iestatot opcijai **Pārdošanas pasūtījuma noklusējums** vienumu **Jā**. Šis aizturēšanas kods tiks lietots ikreiz, kad pārdošanas pasūtījums tiek aizturēts. Ja pārdošanas pasūtījumam ir rezervēti krājumi un rezervācijas ir automātiski jānoņem, ja pasūtījums tiek aizturēts noteikta iemesla dēļ, iestatiet iemeslu kodiem opcijas **Noņemt krājumu rezervācijas** vienumu **Jā**.

Lai norādītu, kāda tipa piezīme tiks saglabāta, kad lietotāji, kas aiztur pārdošanas pasūtījumu, ievada papildu piezīmes, dodieties uz **Debitoru parādi** \> **Iestatījumi** \> **Debitoru parādu parametri** un pēc tam kopsavilkuma cilnes **Pārdošanas iestatījumi** cilnē **Vispārīgi** iestatiet lauku **Piezīmes veids**. Izmantojiet lauku **Pārdošanas pasūtījuma statuss “Aizturēts”**, lai definētu krāsu, kas tiks izmantota, lai iezīmētu pārdošanas pasūtījumus, kas ir aizturēti, kad tie tiek aplūkoti lapā **Klientu apkalpošana**.

Lai izveidotu aizturēšanas iemeslu kodu papildu kopu, dodieties uz **Mazumtirdzniecība un komercija** \> **Kanāla iestatīšana** \> **Informācijas kodi**. Šos informācijas kodus var izmantot kā sekundāro iemesla kodu, lai papildus definētu galveno aizturēšanas kodu. Atlasiet **Jauns**, lai izveidotu iemeslu kodu kopu, un pēc tam atlasiet **Apakškodi**, lai definētu papildu iemeslu sarakstu. Lai saistītu definētos informācijas kodus ar zvanu centra kanālu, dodieties uz **Retail un Commerce** \> **Kanāli** \> **Zvanu centri** \> **Visi zvanu centri**. Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Aizturēšanas kods**.

## <a name="putting-orders-on-hold"></a>Pasūtījumu aizturēšana

Pasūtījumus, kurus zvanu centra lietotāji izveido uzskaites daļas programmā Commerce, var aizturēt manuāli vai automātiski īpašās situācijās.

Pasūtījuma izveides laikā, bet pirms pasūtījuma iesniegšanas un apstiprināšanas, zvanu centra lietotāji var manuāli aizturēt pasūtījumu, lai neļautu tā nosūtīšanu uz noliktavu tālākai apstrādei. Piemēram, klients, kas veic pasūtījumu, var nebūt gatavs to pabeigt, vai var nebūt norādīti svarīgi dati, kas ir nepieciešami, lai varētu apstrādāt pasūtījumu.

Pasūtījuma izveides lapā zvanu centra lietotājs var aizturēt pasūtījumu, izmantojot pasūtījumu ievades izvēlnes cilnes **Pārdošanas pasūtījums** opciju **Pasūtījumu aizturēšana**. Vai arī lietotājs var atlasīt lapā **Pārdošanas pasūtījumu kopsavilkums** izvēlnes vienumu **Aizturēt**, kas tiek parādīts, atlasot vienumu **Pabeigt** zvanu centra pārdošanas pasūtījumā.

Abos gadījumos tiek parādīta lapa **Pasūtījumu aizturēšana**. Lietotājs pēc tam var atlasīt vienumu **Jauns** pasūtījuma aizturēšanas izveidei. Laukā **Aizturēšanas kods** lietotājam jāatlasa kods, kas visprecīzāk raksturo aizturēšanas iemeslu. Laukā **Iemesla kods** lietotājs var izvēlēties papildu kodu, lai nodrošinātu aizturēšanas otrā līmeņa aprakstu.

Kopsavilkuma cilnes **Piezīmes** laukā **Aizturēšanas piezīmes** lietotājs var ievadīt papildu piezīmes brīvā formā, lai sniegtu papildu kontekstu vai informāciju par aizturēšanu. Šīs piezīmes var palīdzēt citiem lietotājiem, kuri vēlāk pārskata aizturēto pasūtījumu vai strādā ar to.

Pēc tam, kad aizturēšanas informācija ir ievadīta un saglabāta, lietotājs var aizvērt lapu **Pasūtījumu aizturēšana**. Pēc tam lietotājs atgriežas pārdošanas pasūtījuma ievades lapā. Ja nav nepieciešamas turpmākas darbības attiecībā uz pārdošanas pasūtījumu, lietotājs var aizvērt pārdošanas pasūtījuma ievades lapu.

Ja zvanu centra kanālā ir ieslēgts karodziņš **Iespējot pasūtījuma pabeigšanu**, pasūtījumam, kas ir aizturēts, nav jāpiemēro maksājums. Turpretim tāda pārdošanas pasūtījuma gadījumā, kas nav aizturēts, lietotāji nevar aizvērt pārdošanas pasūtījuma ievades lapu, līdz tiek piemērots maksājums. Maksājums būs nepieciešams, pirms pasūtījuma aizturēšanas noņemšanas.

Turklāt zvanu centra lietotāji var noteikt manuālu aizturēšanu pārkāpuma dēļ pasūtījumiem, kas ir aizdomīgi kāda iemesla dēļ. Pasūtījumiem var arī noteikt aizturēšanu automātiski, ja tie atbilst aktīviem pārkāpuma kritērijiem un kārtulām. Plašāku informāciju par šāda veida pasūtījuma aizturēšanu skatiet sadaļā [Pārkāpumu brīdinājumu iestatīšana](/dynamics365/unified-operations/retail/set-up-fraud-alerts).

## <a name="viewing-and-managing-orders-that-are-on-hold"></a>Aizturētu pasūtījumu skatīšana un pārvaldīšana

### <a name="viewing-hold-information-for-a-single-sales-order"></a>Aizturēšanas informācijas skatīšana vienam pārdošanas pasūtījumam

Lapā **Klientu apkalpošana** lietotāji var vizuāli identificēt pasūtījumus, kas ir aizturēti, jo pasūtījuma rindas ir iezīmētas noteiktā krāsā. Šo krāsu nosaka lauks **Pārdošanas pasūtījuma statuss “Aizturēts”** lapā **Debitoru parādu parametri**.

> [!NOTE]
> Ja rinda ir atzīmēta attiecīgajā lapā, izcelšanas krāsa nav redzama.

Lietotāji arī var skatīt detalizētu statusa informāciju par pārdošanas pasūtījumu, lai uzzinātu, vai pasūtījums ir aizturēts. Detalizētai statusa informācijai var piekļūt lapā **Visi pārdošanas pasūtījumi** vai **Klientu apkalpošana**. Ja pasūtījums ir aizturēts, tam tiek iestatīts karodziņš **Neapstrādāt** un laukā **Detalizēts statuss** ir norādīts statuss **Aizturēts** vai **Aizturēšana pārkāpuma dēļ** atkarībā no scenārija.

Lai skatītu detalizētu informāciju par atsevišķu pasūtījumu aizturēšanu, lietotāji var atvērt lapas **Pasūtījuma aizturēšana** detalizētu skatu no lapas **Klientu apkalpošana**, izmantojot izvēlni **Opcijas** atlasītajam pasūtījumam. Lietotāji arī var piekļūt šim skatam no lapas **Visi pārdošanas pasūtījumi**, atlasot izvēlnes vienumu **Pasūtījumu aizturēšana** cilnē **Pārdošanas pasūtījums**.

### <a name="viewing-all-orders-that-are-on-hold"></a>Visu aizturēto pasūtījumu skatīšana

Lai skatītu visus pasūtījumus, kas ir aizturēti manuāli vai automātiski, dodieties uz **Retail un Commerce** \> **Debitori** \> **Pasūtījumu aizturēšana**.

Rīks **Pasūtījumu aizturēšana** sniedz visu tādu pasūtījumu saraksta skatu, kuriem ir noteikta aizturēšana manuālu vai ar pārkāpumiem saistītu aizturēšanas darbību rezultātā. Izmantojot standarta filtrēšanas un kārtošanas opcijas lapā, lietotāji var veidot skatus, kas ļauj viņiem strādāt ar vai pārvaldīt konkrētus aizturēšanas kodus, par kuru pārskatīšanu viņi ir atbildīgi. Rīks **Pasūtījumu aizturēšana** arī norāda pasūtījuma aizturēšanas dienu skaitu. Šī informācija var palīdzēt lietotājiem noteikt rindas prioritātes.

Lai iegūtu detalizētāku aizturēto pasūtījumu skatu, lietotāji var noklikšķināt uz izvēlnes opcijas **Pasūtījuma aizturēšana**. Šis skats sniedz informāciju par debitoru un piezīmes attiecībā uz pasūtījumu, debitoru vai aizturēšanas darbību. Skatā arī ir norādīta informācija par automātiskās aizturēšanas iemeslu, ja pasūtījums tika aizturēts, jo tas atbilda pārkāpuma kārtulai.

Gan saraksta skatā, gan detalizētajā skatā lapā **Pasūtījumu aizturēšana** lietotāji var skatīt vai rediģēt ar pasūtījumiem saistītu papildinformāciju, piemēram, maksājumus, kopsummas un piezīmes.

Opcijas cilnē **Aizturēšanas paņemšana** var būt noderīgas, ja vairāki lietotāji jūsu uzņēmumā vienlaicīgi strādā ar aizturēšanas rindu. Atlasot opciju **Paņemt**, lietotāji var norādīt, ka viņi strādā ar aizturētā pasūtījuma pārskatīšanu un izpēti. Tādējādi citi lietotāji netērē laika, mēģinot paveikt to pašu darbu. Detalizētajā skatā lapā **Pasūtījumu aizturēšana** lietotāji var skatīt informāciju par paņemšanas datumu un laiku, kā arī lietotāju, kurš paņēmis aizturēšanas ierakstu.

Pēc tam, kad ir paņemts aizturēšanas ieraksts, paņemšanu var notīrīt tikai lietotājs, kurš to ir paņēmis. Šis ierobežojums ir paredzēts, lai neļautu lietotājiem paņemt ierakstus, ar kuriem jau strādā citi lietotāji. Lai pasūtījumu iekļautu atpakaļ rindā, lai citi lietotāji ar to varētu strādāt, lietotājs, kurš paņēma attiecīgo ierakstu, atlasa opciju **Dzēst paņemšanu**.

> [!NOTE]
> Aizturēšana netiek atcelta, kad tiek dzēsta paņemšana.

Dažās situācijās, piemēram, ja lietotājs neierodas darbā slimības dēļ vai ir atstājis uzņēmumu, ieraksti, kurus paņēmis attiecīgais lietotājs, var būt nepieciešams atkārtoti piešķirt citam lietotājam. Vadītājs var atkārtoti piešķirt ierakstus, izmantojot opciju **Ignorēt paņemšanu**.

## <a name="releasing-orders-that-are-on-hold"></a>Aizturēto pasūtījumu izlaišana

Gan saraksta skatā, gan detalizētajā skatā lapā **Pasūtījumu aizturēšana** cilne **Dzēst aizturēšanu** ietver opcijas, kas tiek izmantotas, lai izlaistu aizturētu pasūtījumu. Izmantojiet opciju **Dzēst aizturi**, lai atceltu pasūtījumam atlasīto aizturēšanas kodu.

Zvanu centra pasūtījumiem ir nepieciešams maksājums. Tāpēc aizturēšanu nevar pilnībā dzēst, ja pasūtījumam nav piemērots maksājums. Pārliecinieties, ka lapas **Zvanu centra parametri** cilnē **Aiztures** ir ieslēgts parametrs **Iesniegt, kad notīrīts**. Šis iestatījums palīdz nodrošināt, ka pasūtījumam, kuram ir dzēsta aizturēšana, tiek izpildīta pareiza pasūtījuma iesniegšanas loģika, lai validētu un autorizētu maksājumus. Ja nav maksājuma, lietotājs saņem kļūdas ziņojumu un aizturēšanas kods netiek dzēsts.

Ja parametrs **Iesniegt, kad notīrīts** nav iestatīts, lietotājiem jāatlasa opcija **Noņemt un iesniegt** izvēlnē **Dzēst aizturi**, lai palīdzētu nodrošināt, ka pasūtījumam tiks veiktas visas nepieciešamās maksājumu pārbaudes. Ja pasūtījuma iesniegšana neizdodas, kad zvanu centra kanālā ir ieslēgts karodziņš **Iespējot pasūtījuma pabeigšanu**, pasūtījumam tiek atcelts aizturēšanas statuss, bet karodziņš **Neapstrādāt** joprojām ir aktīvs. Tādējādi pasūtījums netiek nosūtīts uz noliktavu līdz brīdim, kad ir piemēroti un validēti pareizi maksājumi.

Ja lietotāji vēlas dzēst aizturi, bet veikt papildu izmaiņas pasūtījumā, pirms tā nodošanas tālākai apstrādei, viņi var atlasīt opciju **Noņemt un modificēt**. Šī opcija noņem aizturēšanas kodu un atver pārdošanas pasūtījuma detalizētu informāciju, lai lietotāji varētu veikt papildu izmaiņas pasūtījumā. Lietotāji var arī lietot maksājumu un iesniegt pārdošanas pasūtījumu, izmantojot maksājumu validēšanas loģiku, ja zvanu centra kanālā ir ieslēgts karodziņš **Iespējot pasūtījuma pabeigšanu**.

## <a name="reporting-options"></a>Pārskatu veidošanas opcijas

Dodieties uz **Retail un Commerce** \> **Pieprasījumi un pārskati** \> **Zvanu centra pārskati** \> **Pasūtījumu aizturēšanas pārskats**, lai veidotu pārskatu par aizturētiem pasūtījumiem pēc datumu diapazona, aizturēšanas koda vai citiem saistītajiem kritērijiem.


[!INCLUDE[footer-include](../includes/footer-banner.md)]