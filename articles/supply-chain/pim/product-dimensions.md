---
title: Preces dimensijas
description: Pastāv piecas preču dimensijas - krāsa, konfigurācija, izmērs, stils un versija. Preču dimensijas var apvienot dimensiju grupās, un dimensiju grupas var piešķirt preču šabloniem. Preču dimensiju kombinācijas nosaka, kā tiek definēti preču varianti.
author: t-benebo
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle, EcoResVersionNameLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 46079daafc744421abcbdf0a3539428f2a39f13c
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920527"
---
# <a name="product-dimensions"></a>Preces dimensijas

[!include [banner](../includes/banner.md)]

Pastāv piecas preču dimensijas: krāsa, konfigurācija, izmērs, stils un versija. Preču dimensijas var apvienot dimensiju grupās, un dimensiju grupas var piešķirt preču šabloniem. Preču dimensiju kombinācijas nosaka, kā tiek definēti preču varianti.

Preču dimensijas ir īpašības, ko izmanto, lai identificētu preces variantu. Preču variantu definēšanai vai izmantot preču dimensiju kombinācijas. Lai izveidotu preces variantu, ir jādefinē vismaz viena preces dimensija preces šablonam.

## <a name="product-variants"></a>Preces varianti

Preču varianti tiek saukti arī par krājumiem. Krājums ir materiāla prece, kas nav tāds pats kā pakalpojums. Var arī definēt preces šablonu, kura veids ir Pakalpojums. Izmantojot pakalpojuma tipu, varat norādīt preču variantus, kas ietver pakalpojumus. Piemēram, var norādīt preces šablonu konsultāciju darbam un preču variantus darbam, ko veic vecākie konsultanti un jaunākie konsultanti.

## <a name="product-dimensions"></a>Preces dimensijas

Pamatojoties uz preces dimensijas vērtībām, var ģenerēt preces variantu.

Preces dimensijas vērtības izmēru, krāsu un stila dimensijām var izveidot šādās vietās:

- **Izmēru** lapa (**Preces informācijas pārvaldība \> Iestatījumi \> Dimensiju un variantu grupas \> Izmēri**)
- **Krāsu** lapa (**Preces informācijas pārvaldība \> Iestatījumi \> Dimensiju un variantu grupas \> Krāsas**)
- **Stilu** lapa (**Preces informācijas pārvaldība \> Iestatījumi \> Dimensiju un variantu grupas \> Stili**)

Preces konfigurācijas dimensijas vērtības parasti tiek izveidotas, izmantojot preču konfiguratoru vai dimensiju konfiguratoru. 

Preces versijas parasti tiek veidotas noteiktām versijām, jo prece attīstās tās dzīves cikla laikā. Preces versijas tālāk ir detalizēti aprakstītas šajā tēmā.

Preces dimensijas var izveidot un uzturēt arī lapā **Preces dimensijas**, kam var piekļūt tālāk norādītajās vietās.

- Dodieties uz **Preču informācijas pārvaldība \> Produkts \> Produktu šabloni**. Darbību rūtī atlasiet **Preču dimensijas**.
- Dodieties uz **Preču informācijas pārvaldība \> Preces \> Visas preces un preču šabloni**. Atlasiet preces šablonu. Darbību rūtī atlasiet **Preču dimensijas**.
- Dodieties uz **Preču informācijas pārvaldība \> Izlaistās preces**. Atlasiet preces šablonu. Darbību rūtī grupas **Preces šablons** cilnē **Prece** atlasiet **Preces dimensijas**.

Krājumam izveidojamo variantu skaitu ierobežo iespējamo preču dimensiju kombināciju skaits.

> [!TIP]
> Ja izmantojat preci pasūtījuma rindā, piemēram, izvēlieties preču dimensijas, lai norādītu preces variantu, ar ko vēlaties strādāt.

## <a name="example"></a>Paraugs

Uzņēmums pārdod džinsus. Krājumam *Džinsi* tiek izmantotas preces krāsas un izmēra dimensijas. Džinsi tiek pārdoti trīs dažādās krāsas un sešos dažādos izmēros. Krāsas ir zila, melna un brūna. Izmēri ir XS, S, M, L, XL un XXL. Ne visi izmēri ir pieejami visās trīs krāsās. Ja būtu pieejamas visas kombinācijas, tā rezultātā būtu 18 dažādi džinsu veidi. Lai gan šajā piemērā tiek iegūtas tikai šādas deviņās preču variantu kombinācijas.

| Krāsa | Izmēri |
|-------|------|
| Zila  | XS   |
| Zilā  | S    |
| Zilā  | P    |
| Melna | P    |
| Melna | L    |
| Melna | XL   |
| Brūna | L    |
| Brūna | XL   |
| Brūna | XXL  |

## <a name="the-version-product-dimension"></a>Versijas preces dimensija

Versija ir produkta dimensija, kas paredzēta, lai palīdzētu uzturēt un izsekot vairāku preču versijas visā piegādes ķēdē. Versiju izsekošana ir būtiska to ražotājiem, kuri darbojas pasaules mērogā, sašaurinot preču dzīves ciklus, palielinātu kvalitātes un drošības prasību līmeni, kā arī palielinātu fokusu uz preču drošību.

Kā standarta preces dimensija versija darbosies līdzīgi esošajām preču dimensijām (izmērs, stils, krāsa un konfigurācija). Tāpēc to var izmantot citiem nolūkiem, izņemot produktu versiju izsekošanai.

### <a name="turn-on-the-version-dimension"></a><a name="enable-version-dim"></a>Ieslēdziet versijas dimensiju

#### <a name="before-you-turn-on-the-version-dimension"></a>Pirms ieslēdzat versijas dimensiju

Ieslēdzot versijas dimensiju, dažas funkcijas var var sabojāties vai pārtraukt darbu, kā paredzēts, ja esat instalējis citus risinājumus, kas pievieno pielāgojumus krājumu dimensijām. Lai versijas dimensija būtu pilnībā funkcionāla, iespējams, šie risinājumi būs jāatjaunina, lai tajos būtu iekļauta versijas dimensija savās atsaucēs uz krājumu dimensijām.

Kad pārbaudāt savu risinājumu saderību ar versijas dimensiju, meklējiet šādus elementus:

1. **Funkcionalitāte:** vissvarīgākais ir novērtēt visus pielāgojumus, kas ietver krājumu dimensijas, lai nodrošinātu, ka tie var strādāt kopā ar versijas dimensiju.
1. **Atsauces uz krājumu dimensijām:** meklējiet atsauces uz krājumu dimensijām (tas ir, vietas, kur dimensijām ir skaidri norādītas atsauces). Atsaucēm uz `InventDimId` jāstrādā no kastes, bet meklējiet arī atsauces uz stilu vai krāsu. Piemēram, noteikti pārbaudiet šādus elementus:

    - API izsaukumi paplašinātās klasēs
    - Visas atsauces uz noteiktām krājumu dimensijām paplašinājuma kodā (šim kodam ir jāmaina versijas dimensija kopā ar stilu, krāsu un izmēra dimensijām.)

1. **Atsauces uz novecojušiem API izsaukumiem:** tās versijas dimensijas ieviešanā korporācija Microsoft ir mēģinājusi pēc iespējas mazāk API padarīt par novecojušām. Nedaudzas novecojušās API parādīs brīdinājumu, kad ieslēgsit **Preču dimensija - versija** konfigurācijas atslēga. Izsaukumi uz šīm API jāfiksē savos paplašinātajos risinājumos, pirms ieslēdzat versijas dimensiju ražošanas sistēmā. Šeit ir versijai raksturīgs novecojis API:

    - RetailTransactionServiceInventory::getProductRecordId
    - EcoResProductNumberIdentifiedProductVariantEntity::find
    - EGAISAlcoholProduction_RU::findByItemDim
    - PCVariantConfiguration::findByProductMasterAndDimensions

1. **Kartes:** ja kāda karte izmanto krājumu dimensijas, atbilstošais relāciju kartējums uz šīm kartēm ir jāatjaunina, lai tās ietvertu versijas dimensiju. Paplašinātajā modelī vai tabulas paplašinājumiem skatiet tabulas, kurās lauki ietver krājumu dimensijas.
1. **Microsoft Dynamics 365 Commerce funkcionalitāte:** pēc tam, kad tā ir ieslēgta, versijas dimensija tiks rādīta visā Commerce noteiktajā kodā programmā Dynamics 365 Supply Chain Management. Tomēr versijas dimensiju vēl neatbalsta Commerce kanāla datu bāze vai pārdošanas punktā (POS), vai e-komercijas programmas. Šīs ar Commerce saistītās programmas neatbalstīs lietotājus, kas pārdod/nosūta vai atgriež/saņem krājumus pēc versijas dimensijas. Krājumu pieejamības uzmeklēšanas funkcijas neatšķir krājumu, izmantojot versijas dimensiju Commerce programmās. Šī uzvedība atgādina pašreizējo konfigurācijas dimensijas uzvedību programmā Commerce.

#### <a name="turn-on-the-version-dimension"></a>Ieslēdziet versijas dimensiju

Lai varētu izmantot versijas dimensiju, tas vispirms ir jāiespējo jūsu sistēmā. Šim uzdevumam ir nepieciešamas administratora atļaujas.

1. Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**.
1. Ieslēdziet līdzekli, kura nosaukums ir *Preču dimensijas versija*. (Papildinformāciju skatiet [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Sistēmas ieslēgšana [Apkopes režīmā](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**.
1. Cilnē **Konfigurācijas atslēgas** paplašiniet **Tirdzniecību** un atlasiet izvēles rūtiņu **Preces dimensija - versija**.
1. Izslēdziet [Apkopes režīmu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

### <a name="areas-where-the-version-dimension-isnt-supported"></a>Vietas, kur versijas dimensija nav atbalstīta

Tālāk norādītajiem apgabaliem netiek atbalstīta versijas dimensija (joprojām varat izmantot šos apgabalus, bet nevarēsit pievienot versijai preces (preces, kurām tiek izmantota versijas dimensija)). Piemēram, piegādātāju katalogam nevar pievienot versiju izveidotu krājumu. Tas ir tāpēc, ka preču pievienošana ar versijas dimensiju šiem apgabaliem var izraisīt iztrādāmas izmaiņas.

- Izmaksu objekta mēneša izraksts
- Izmaksu objekta pārskata kešatmiņa
- MCR pārdošanas statistika pa krājumiem
- Piegādātāju katalogi
- EcoResProductDimensionGroupEntity

Turklāt pasūtījuma izveides un pasūtījumu apstrādes līdzekļi Commerce (piemēram, POS, zvanu centrs un e-commerce pasūtījumi) neatbalsta versijas dimensiju. Nav apstiprināts laika periods, kad Commerce pasūtījumi tiks uzlaboti, lai to atbalstītu.

### <a name="functional-characteristics-of-the-version-dimension"></a>Versijas dimensijas funkcionālie raksturlielumi

Versijas dimensija darbojas tāpat kā citas preces dimensijas. Tomēr, ņemot vērā tās specifisko raksturu un to, ka tā ir paredzēta vairāku preču versiju saglabāšanai un izsekošanai, tā darbojas nedaudz atšķirīgi. Lūk, dažas no atšķirībām un līdzībām:

- **Nav versijas grupas.**

    Kaut arī pastāv grupu koncepcija izmēram, krāsai un stilam (krāsu grupa, izmēru grupa un stilu grupa), nepastāv versijas grupas koncepcija. Grupas ļauj iepriekš definēt piemērojamās vērtības tā, ka, piemēram, piešķirot krāsu grupu precei, prece var izmantot visas krāsu grupas krāsas. Šī koncepcija neattiecas uz versijas dimensiju, jo preces izveidošanas laikā netiek iepriekš definētas versijas, kas tiek izmantotas. Tā vietā versijas tiek veidotas produkta dzīves cikla laikā, jo tās ir nepieciešamas. Parasti, ja preces forma, atbilstība un funkcija paliek tāda pati, jaunas preces vietā tiek izveidota jauna versija.

- **Preces variantu ieteikumi darbojas tāpat kā pašlaik.**

    Preces variantu ieteikumi izveidos ieteikumus par visām versijas dimensiju vērtībām, tāpat kā tas ir citās dimensijās. Versijas preču izveides un izlaišanas process ir tāds pats kā precēm, kuras lieto citas dimensijas. Kad tiek izveidota preces versija, pirmā versija (v1) tiks izveidota kā preces dimensija, un tiks izlaisti varianti. Tā kā prece mainās un ir nepieciešama jauna versija, tiks pievienota jauna versijas vērtība (v2) un tiks izlaisti nepieciešamie varianti. Nav cerību, ka visas versijas (v1, v2 un v3) iepriekš tiks izveidotas precei.

> [!IMPORTANT]
> Ieslēdzot un lietojot versijas dimensiju, daži risinājumi, kas atsaucas uz krājumu dimensijām, var pārstāt darboties. Lai apstiprinātu un labotu šīs problēmas, sazinieties ar neatkarīgā programmatūras pārdevēju (ISV), lai uzzinātu par ietekmētajiem risinājumiem. Papildinformāciju skatiet šeit [Iespējot versijas dimensiju](#enable-version-dim).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]