---
title: Darbs ar publicēšanas grupām
description: Šajā tēmā ir aprakstīts publicēšanas grupu līdzeklis programmā Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d757f34d3e16850e4f5de122f63b2b3342f612e49f07c7cf6585362999f03c02
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717676"
---
# <a name="work-with-publish-groups"></a>Darbs ar publicēšanas grupām

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts publicēšanas grupu līdzeklis programmā Microsoft Dynamics 365 Commerce.

E-tirdzniecības tīmekļa vietnes visu gadu tiek pastāvīgi atjauninātas ar jaunu saturu. Atjauninājumi bieži tiek publicēti pakešveidā ap noslogotiem e-tirdzniecības notikumiem, piemēram, brīvdienām, sezonālām mārketinga kampaņām vai reklāmu palaišanas. Šie atjauninājumi bieži vien pieprasa, lai tīmekļa vietnes satura grupas (piemērus, lapas, attēli, fragmenti un veidnes) ir iekārtotas, validētas un publicētas vienlaicīgi vienā darbībā.

Iespēja grupēt vienumus loģiskās kopās, kas publicē vienumus kopā, kur katrai kopai ir savs dzīves cikls, sniedz daudzas priekšrocības vietņu autoriem. Commerce šīs loģiskās kopas tiek sauktas par publicēšanas grupām. Tās ļauj vietnes autoriem izsekot atjauninājumu kopas kā atsevišķas konfigurējamas, testējamas un publicējamas entītijas.

Autori var priekšskatīt atjauninājumus iekārtotā publicēšanas grupā, neietekmējot aktuālo vietni vai citas atsevišķas publicēšanas grupas. Autori pēc tam var ieplānot publicēšanas darbību, lai vienlaikus aktuālajā vietnē publicētu visus vienumus, kas ir publicēšanas grupā. Iespēja grupēt, priekšskatīt un plānot publicēšanai paredzētos atjauninājumus ir svarīga daudzām uzņēmuma līmeņa kompānijām, kas gūst ievērojamus ikgadējos ieņēmumus saistībā ar vietnes atjaunināšanu, kas balstīta uz svarīgiem notikumiem.

Kompānija var ciest zaudējumus no lēnām vai nederīgām satura publikācijām, kas nenotiek plūstoši. Publicēšanas grupas palīdz garantēt, ka palaišanas tiek organizētas, validētas un publicētas laikā. Neatkarīgi no tā, vai lielas, vai mazas, publicēšanas grupas nodrošina vērtīgu rīku kopu, kas palīdz autoriem organizēt un vienkāršot notiekošos vietnes atjaunināšanas uzdevumus.

## <a name="when-to-use-publish-groups"></a>Kad izmantot publicēšanas grupas

Varat izmantot publicēšanas grupas, kad vien jums jāiekārto un jāpublicē vairāki dokumenti kopā. Piemēram, ja jūsu vietne atjaunina saturu katru sezonu, varat izveidot publicēšanas grupas šīm sezonālā mārketinga kustībām. Jūsu publicēšanas grupā "Rudens sezonas atjauninājums" būt jauni sezonas attēli, fragmenti ar sezonas mārketinga ziņojumiem, lapas, kurās ir ietvertas sezonas produktu kolekcijas vai citi sezonas atjauninājumi tīmekļa vietnei.

Publicēšanas grupu priekšrocība ir tā, ka varat iekārtot vairākus atjauninājumus paralēli. Piemēram, neilgi pēc atjaunināšanas publicēšanas grupai "Rudens sezonas atjauninājums", iespējams, notiks satura atjauninājums īpašai svētku nedēļas nogalei. Šajā gadījumā jūs varat iekārtot saturu publicēšanas grupai "Rudens sezonas atjauninājums" tajā pašā laikā, kad jūs iekārtojat saturu sekojošajai publicēšanas grupai "Rudens brīvdienu atjauninājums". Katrai publicēšanas grupai ir savs unikāls lapu, attēlu, fragmentu, veidņu utt. kopums. Varat iekārtot, priekšskatīt un validēt šīs divas publicēšanas grupas neatkarīgi vienu no otras, bet sakrītošā laika grafikā. Pēc tam katru publicēšanas grupu var ieplānot kā aktuālu jūsu vietnē konkrētos datumos un laikos.

## <a name="turn-on-the-publish-groups-feature"></a>Publicēšanas grupu līdzekļa ieslēgšana

Publicēšanas grupu līdzeklis nav obligāts, un to jūsu vietnei ir jāieslēdz.

Lai Commerce autorēšanas rīkos jūsu vietnei ieslēgtu publicēšanas grupas līdzekli, veiciet tālāk norādītās darbības.

1. Kreisās puses navigācijas rūtī atlasiet **Vietnes iestatījumi**, lai to izvērstu.
1. **Vietnes iestatījumi** atlasiet **Līdzekļi**.
1. Iestatiet opciju **Publicēšanas grupas** kā **Ieslēgts**.

## <a name="create-a-publish-group"></a>Publicēšanas grupas izveide

Lai Commerce autorēšanas rīkos jūsu vietnei izveidotu publicēšanas grupu, veiciet tālāk norādītās darbības.

1. Kreisās puses navigācijas rūtī atlasiet **Publicēšanas grupas**.
1. Augšējā komandjoslā atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot publicēšanas grupu** sadaļā **Publicēšanas grupas nosaukums** ievadiet aprakstošu nosaukumu. Tad atl. **Labi**.

## <a name="set-the-publish-group-authoring-context"></a>Publicēšanas grupas autorēšanas konteksta iestatīšana

Commerce noklusējuma autorēšanas konteksts ir aktuālais vietnes konteksts. Aktuālais vietnes autorēšanas konteksts ir noklusējuma skats, kurā varat skatīt un veikt izmaiņas tieši savā tīmekļa vietnē, neizmantojot publicēšanas grupu. Tas atspoguļo jūsu vietnes publicētās versijas jaunākos tiešos atjauninājumus. Ja **Publicēšanas grupas** konteksta vadīkla kreisās puses navigācijas rūtī rāda nosaukumu **Aktuālā vietne**, jūs strādājat aktuālās saites autorēšanas kontekstā. **Aktuālā vietne** ir konteksta vadīklas noklusējuma nosaukums. Citos gadījumos konteksta vadīkla rāda publicēšanas grupas nosaukumu.

Lai strādātu publicēšanas grupā, jāpārslēdzas uz publicēšanas grupas autorēšanas kontekstu. Lai iestatītu publicēšanas grupas kontekstu, veiciet vienu no tālāk norādītajām darbībām.

- Kreisās puses navigācijas rūtī atlasiet konteksta vadīklu, kas atrodas tieši sadaļā **Publicēšanas grupas**, un pēc tam parādītajā opciju sarakstā atlasiet publicēšanas grupas nosaukumu. Konteksta vadīkla ir pārdēvēta un rāda publicēšanas grupas nosaukumu.
- Kreisās puses navigācijas rūtī atlasiet **Publicēšanas grupas** un pēc tam sadaļā **Publicēšanas grupas** atlasiet publicēšanas grupas nosaukumu. Konteksta vadīkla ir pārdēvēta un rāda publicēšanas grupas nosaukumu.

Kad esat iestatījis publicēšanas grupas autorēšanas kontekstu, jūs strādājat šajā publicēšanas grupas kontekstā, kad priekšskatāt un rediģējat vietnes saturu.

Lai atgrieztos pie noklusējuma aktuālās vietnes autorēšanas konteksta, atlasiet konteksta vadīklu un pēc tam atlasiet **Aktuālā vietne**.

## <a name="add-pages-or-other-items-to-a-publish-group"></a>Lapu vai citu vienumu pievienošana publicēšanas grupai

Pēc tam, kad esat atlasījis publicēšanas grupas autorēšanas kontekstu, un konteksta vadīkla kreisās puses navigācijas rūtī rāda tās nosaukumu, varat izveidot saturu tāpat, kā to darāt noklusējuma aktuālās vietnes kontekstā. Varat arī pievienot esošas lapas vai citus vienumus no citām publicēšanas grupām vai no aktuālās vietnes konteksta.

Lai kopētu esošas lapas uz publicēšanas grupu, veiciet tālāk norādītās darbības.

1. Atlasiet autorēšanas kontekstu, no kura kopēt, un pēc tam kreisās puses navigācijas rūtī atlasiet **Lapas**.
1. Atlasiet lapu, ko pievienot publicēšanas grupai.
1. Komandjoslā atlasiet **Kopēt uz publicēšanas grupu**.
1. Dialoglodziņā **Atlasīt publicēšanas grupu** atlasiet publicēšanas grupu, kurai pievienotu lapu, un pēc tam atlasiet **Labi**.

Varat izmantot tās pašas pamatdarbības, lai izveidotu pielāgotas preču lapas, URL, veidnes, izkārtojumus, fragmentus un multivides bibliotēkas līdzekļus vai lai pievienotu esošus šo veidu vienumus publicēšanas grupai.

## <a name="validate-a-publish-group"></a>Publicēšanas grupas validācija

Lai pārliecinātos, ka ir apmierinātas visas atkarības publicēšanas grupas saturā un tiek nodotas visas validācijas, varat izpildīt validāciju, lai identificētu visas problēmas, kas jānovērš pirms plānot publicēšanas darbību.

Lai validētu savu publicēšanas grupu pirms tās ieplānošanas, veiciet tālāk norādītās darbības.

1. Kreisās puses navigācijas rūtī atlasiet **Publicēšanas grupas**.
1. Atlasiet validējamo publicēšanas grupu.
1. Komandjoslā atlasiet **Validēt**.

Validācija tiek izpildīta visam saturam publicēšanas grupā. Visas problēmas, kas kavēs sekmīgu publicēšanas darbību, tiek parādītas paziņojumu lodziņā, kas parādās augšējā labajā stūrī.

> [!NOTE]
> Validācija vienmēr tiek izpildīta automātiski, kad ir ieplānota publicēšanas grupa. Tomēr poga **Validēt** komandjoslā ir noderīga, jo tā palīdz identificēt problēmas, kas jums jānovērš, pirms mēģināt ieplānot publicēšanas grupas padarīt par aktuālām.

## <a name="schedule-a-publish-group-to-go-live"></a>Ieplānošana publicēšanas grupu padarīt par aktuālu

Lai ieplānotu publicēšanas grupu padarīt par aktuālu savā vietnē, veiciet tālāk norādītās darbības.

1. Kreisās puses navigācijas rūtī atlasiet **Publicēšanas grupas**.
1. Sadaļā **Publicēšanas grupas** atlasiet publicēšanas grupu, ko ieplānot.
1. Komandjoslā atlasiet **Rediģēt grafiku**. Tiek parādīts dialoglodziņš **Rediģēt grafiku**.
1. Atlasiet datumu un laiku, kad publicēšanas grupai jākļūst par aktuālu, pēc tam atlasiet **Labi**.

Lai atceltu publicēšanas grupas ieplānošanu, veiciet tās pašas darbības, bet atlasiet **Atcelt publicēšanas grupu** dialoglodziņā **Rediģēt grafiku**.

> [!NOTE]
> Ļoti lielām publicēšanas grupām var būt nepieciešams minūti vai divas ilgs laiks, lai tās tiktu publicētas, pienākot to ieplānotajam laikam. Ņemiet vērā, ka publicēšanas darbība nav momentāna un ka mazākas publicēšanas grupas tiks publicētas ātrāk.

## <a name="publish-groups-faq"></a>Bieži uzdotie jautājumi par publicēšanas grupām

**Cik daudz vienumu var būt publicēšanas grupā?**

Pašlaik pastāv ierobežojums — 2 000 vienumi katrai publicēšanas grupai. Ņemiet vērā, ka ļoti lielām publicēšanas grupām var būt nepieciešamas vairākas minūtes, lai tās tiktu publicētas, pienākot to ieplānotajam laikam.

**Vai publicēšanas grupas līdzinās koda "zaram" programmatūras izstrādes terminoloģijā?**

Jā un nē. Publicēšanas grupas var uzskatīt par jūsu vietnes sazarotu versiju. Tādā veidā tās darbojas kā zari. Tomēr nepastāv sapludināšanas jēdziens atsevišķu vienumu līmenī. Vienums, kas tiek publicēts pēdējais, vienkārši pārraksta iepriekš pastāvējušo, un visjaunākā publicēšanas darbība vienmēr aizstāj iepriekšējās publicēšanas darbības.

**Vai iespējams ieplānot, lai vienlaikus tiktu padarītas par aktuālām divas publicēšanas grupas?**

Nr.p.k. Veiktspējas un konfliktu iemeslu dēļ sistēma liks jums regulēt ieplānotās publicēšanas grupas ar vismaz piecu minūšu intervālu.

**Vai iespējams izmantot publicēšanas grupas, lai plānotu daudzkanālu administrācijas vienumus, piemēram, atlaides un preču jauninājumus?**

Pašlaik publicēšanas grupu līdzeklis atbalsta tikai tīmekļa vietnes saturu. Tomēr Microsoft apzinās, ka integrācija ar administrācijas mazumtirdzniecības scenārijiem varētu būt vērtīga, koordinējot un automatizējot daudzkanālu kampaņas palaišanu.

## <a name="additional-resources"></a>Papildu resursi

[Satura pievienošanas veidi](add-manage-content.md)

[Lapas modeļa glosārijs](page-elements-overview.md)

[Dokumenta stāvokļi un dzīves cikls](document-states-overview.md)

[Šķērskanālu kopīgošanas iespējošana un izmantošana](cross-channel-sharing.md)

[Darbs ar moduļiem](work-with-modules.md)

[Darbs ar fragmentiem](work-with-fragments.md)

[Pārskats par veidnēm un izkārtojumiem](templates-layouts-overview.md)

[Vietnes navigācijas pielāgošana](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
