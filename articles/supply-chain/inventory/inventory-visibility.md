---
title: Inventory Visibility pievienojumprogrammas pārskats
description: Šajā rakstā ir paskaidrots, kas ir krājumu redzamība, un aprakstīti tās līdzekļi.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dd790bcaada0c1a05e46b4edacaa31fc4e15be92
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762812"
---
# <a name="inventory-visibility-add-in-overview"></a>Inventory Visibility pievienojumprogrammas pārskats

[!include [banner](../includes/banner.md)]

Krājumu redzamības pievienojumprogramma (saukta arī par *krājumu redzamības pakalpojumu) nodrošina neatkarīgu un ļoti mērogojamu mikropakalpojumu, kas ļauj reāllaikā veikt rīcībā esošo krājumu* izmaiņu publicēšanu un redzamības izsekošanu visos jūsu datu avotos un kanālos. Tas nodrošina platformu, kas ļauj pārvaldīt globālos krājumus, izmantojot funkcionalitāti, kas ietver (bet neaprobežojas ar) šādu sarakstu:

- Centralizēti izsekojiet jaunāko krājumu statusu (piemēram, rīcībā esošs, pasūtīts, iegādāts, pārsūtīts, atgriezts un ievietots karantīnā) visos datu avotos, noliktavās un atrašanās vietās, savienojot savus Supply Chain Management vai trešo pušu loģistikas datu avotus (piemēram, pasūtījumu pārvaldības sistēmas, trešo pušu uzņēmuma resursu plānošanas \[ERP\] sistēmas, tirdzniecības vietu \[POS\] sistēmas un noliktavas pārvaldības sistēmas) ar krājumu redzamības pakalpojumu.
- Vaicājiet rīcībā esošo krājumu pieejamību un trūkumu un saņemiet tūlītējas atbildes, tieši zvanot uz krājumu redzamības pakalpojumu.
- Izvairieties no pārpārdošanas, it īpaši, ja jūsu pieprasījums nāk no dažādiem kanāliem, veicot reāllaika mīkstās rezervācijas pakalpojumā Krājumu redzamība.
- Labāk pārvaldiet solītos pasūtījumus un klientu vēlmes, norādot precīzus pašreizējos vai nākamos pieejamos datumus, lai daudzkanālu funkcija "Pieejams solīšanai" (ATP) varētu aprēķināt paredzamos pasūtījuma izpildes datumus.

## <a name="extensibility"></a>Paplašināmība

Krājumu redzamības pakalpojums ir ļoti paplašināms, jo datu ievade un izvade neaprobežojas tikai ar Microsoft lietojumprogrammām. Ārējās sistēmas var piekļūt pakalpojumam, izmantojot RESTful lietojumprogrammu saskarnes (API). Papildus iebūvēto kartējumu izmantošanai, kas tiek nodrošināti Supply Chain Management datu avotam un dimensijām, varat integrēt krājumu redzamību ar vairākām trešo pušu sistēmām, iestatot papildu datu avotus, krājumu statusu mērus (pakalpojumā Krājumu redzamība tiek dēvēti par *fiziskiem mēriem*) un krājumu dimensijas, izmantojot konfigurācijas programmu. Tādā veidā varat elastīgi vaicāt un mainīt vairākus datu avotus un iepriekš definētas krājumu dimensijas.

Turklāt, tā kā krājumu redzamība ir veidota uz Microsoft Dataverse, tās datus var izmantot, lai izveidotu un integrētu ar Power Apps. Varat arī izmantot Power BI, lai izveidotu pielāgotus informācijas paneļus, kas atbilst jūsu uzņēmuma prasībām.

## <a name="scalability"></a>Mērogojamība

Pakalpojumu Krājumu redzamība var palielināt vai samazināt atkarībā no datu apjoma. Mērogojamības pieredze lielākoties ir nevainojama, un to veic Microsoft platformas komanda, pamatojoties uz jūsu darījumu datu apjoma automātisku noteikšanu un novērtēšanu.

Nākamajā attēlā ir parādīta krājumu redzamības arhitektūra.

[<img src="media/inventory-visibility-architecture.png" alt="Inventory Visibility architecture." title=" Krājumu redzamības arhitektūra" width="720" />](media/inventory-visibility-architecture.png)

## <a name="feature-highlights"></a>Līdzekļu iezīmēšana

### <a name="get-a-global-view-of-real-time-inventory"></a>Iegūstiet globālu skatījumu uz reāllaika krājumiem

Krājumu redzamība nodrošina, ka jums vienmēr ir piekļuve visjaunākajiem krājumu daudzumiem visos jūsu kanālos, atrašanās vietās un noliktavās. Jūs gūsiet vislielāko labumu no tā izmantošanas, lai atbalstītu savu ikdienas darbības biznesu ikreiz, kad jums būs jāiegūst krājumu ieraksti. Fiziskie rīcībā esošie krājumi, pārdotie daudzumi un iegādātie daudzumi ir pieejami ārpus kastes. Varat arī konfigurēt citus fizisko krājumu mērus (piemēram, atgrieztos, karantīnā ievietotos un izliktos datus) pēc nepieciešamības, lai iegūtu šo informāciju reāllaikā. Krājumu redzamība var efektīvi apstrādāt miljoniem krājumu izmaiņu ziņu. Šos datus var apkopot un atspoguļot jaunākajos krājumu daudzumos pakalpojumā uzreiz, sekundē vai minūtē atkarībā no intervāla, kurā dati tiek publicēti. Papildinformāciju skatiet sadaļā [Krājumu redzamības publiskās API.](inventory-visibility-api.md)

### <a name="central-inventory-adjustment"></a>Centrālā inventāra korekcija

Krājumu redzamība ļauj ārējām sistēmām izsaukt savu API, lai publicētu krājumu izmaiņas. Izmaiņas nekavējoties stāsies spēkā sadaļā Krājumu redzamība. Tāpēc rīcībā esošais inventārs tiek uzreiz atskaitīts.

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Vienkārša rezervācija, lai izvairītos no pārpārdošanas visos pasūtījumu kanālos

Mīkstā *rezervācija* ļauj piešķirt vai atzīmēt ar karodziņu noteiktus daudzumus, lai izpildītu pasūtījumu vai pieprasījumu. Mīkstā rezervācija neietekmē fiziskos krājumus, bet tā tiek atskaitīta no *rezervācijai* pieejamā krājumu daudzuma un nodrošina atjauninātu daudzumu turpmākai pasūtījuma izpildei. Šis līdzeklis būs noderīgs, ja pārdošanas pieprasījumi vai pasūtījumi ienāk jūsu uzņēmumā no viena vai vairākiem kanāliem vai datu avotiem, kas atrodas ārpus jūsu ierakstu sistēmas uzņēmuma resursu plānošanas (ERP) sistēmas.

Ja neizmantojat mīkstās rezervācijas pakalpojumā Krājumu redzamība, jums ir jāgaida, līdz pasūtījums tiek sinhronizēts ar ERP sistēmu un apstrādāts ar to, lai saņemtu fiziskā inventāra daudzuma atjauninājumu. Šim procesam parasti ir milzīgs latentums. Tomēr mīkstās rezervācijas stājas spēkā nekavējoties katru reizi, kad pārdošanas kanālos tiek ģenerēts pārdošanas pieprasījums vai pasūtījums. Tāpēc tie palīdz novērst pārpārdošanas situācijas, nodrošinot, ka jūsu daudzkanālu pasūtījumi netraucēs viens otram, kad tie galu galā sasniegs ERP sistēmu. Mīkstās rezervācijas arī nodrošina, ka varat izpildīt visus solītos pasūtījumus. Tāpēc tie palīdz jums apmierināt klientu vēlmes un saglabāt klientu lojalitāti. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas rezervācijas](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-quantity-and-dates"></a>ATP daudzuma un datumu tūlītēja reakcija

Ir svarīgi redzēt jūsu tuvākās nākotnes plānotos krājumus (tostarp piedāvājumu, pieprasījumu un prognozēto rīcībā esošo informāciju), jo palīdz jūsu uzņēmumam sasniegt tālāk norādītos mērķus.

- Samaziniet krājumu līmeni, lai samazinātu krājumu pārvaldības izmaksas.
- Atvieglojiet iekšējo pasūtījumu apstrādi, lai pārdevēji varētu aprēķināt nosūtīšanas un piegādes datumus, pamatojoties uz pasūtīto preču pieejamību.
- Nodrošiniet pārredzamību par to, kad klienti var sagaidīt, ka krājumā neesoša prece kļūs pieejama, norādot nākamo pieejamo datumu.

ATP funkciju ir viegli ieviest ikdienas pasūtījumu izpildes procesā. Vissvarīgākais ir tas, ka, tāpat kā citi krājumu redzamības piedāvājumi, ATP funkcija ir *globāla un reāllaika*. Tādēļ varat iestatīt vairākas ATP aprēķinu formulas, lai tām būtu pilni krājumu pieejamības vaicājumi, kas aptver visus jūsu biznesa kanālus un datu avotus. Papildinformāciju skatiet sadaļā [Krājumu redzamības rīcībā esošie izmaiņu grafiki, kas ir pieejami solīšanai](inventory-visibility-available-to-promise.md).

### <a name="preallocate-your-stock-to-important-channels-or-customers-with-inventory-allocation"></a>Iepriekš piešķiriet savus krājumus svarīgiem kanāliem vai klientiem, izmantojot krājumu sadalījumu

Krājumu redzamības sadalījuma līdzeklis ļauj aizsargāt un norobežot vērtīgos rīcībā esošos krājumus svarīgiem kanāliem, klientu grupām vai atrašanās vietām. Pēc krājumu piešķiršanas krājumu patēriņš tiek ierobežots līdz iedalītajam pūlam, un daudzumi, kas palikuši baseinā, tiks atskaitīti gandrīz reālā laikā, lai atspoguļotu daudzumu, kas joprojām ir pieejams patēriņam. Papildinformāciju skatiet sadaļā [Krājumu redzamības krājumu sadalījums](inventory-visibility-allocation.md).

### <a name="compatibility-with-wms-items"></a>Saderība ar WMS vienumiem

Microsoft mērķis ir nodrošināt gatavu integrāciju ar noliktavas pārvaldības procesiem (WMS), lai WMS klienti varētu izmantot arī krājumu redzamības pakalpojuma priekšrocības. Saskaņā ar 2022. gada 1. viļņa laidienu (publiskais priekšskatījums martā) krājumu pakalpojums atbalsta rīcībā esošos WMS vienumu vaicājumus un ATP. Mīkstās rezervēšanas un piešķiršanas funkcija tiks atbalstīta WMS klientiem nākamajā kārtā. Papildinformāciju skatiet sadaļā [Krājumu redzamības atbalsts WMS vienumiem](inventory-visibility-whs-support.md).

Nākamajā attēlā ir parādīts augsta līmeņa kopsavilkums par esošajiem līdzekļiem un to, kā tos var novietot datu plūsmā.

[<img src="media/inventory-visibility-feature-overview.png" alt="Inventory Visibility feature overview." title=" Krājumu redzamības līdzekļa pārskats" width="720" />](media/inventory-visibility-feature-overview.png)

## <a name="licensing"></a>Licencēšana

Krājumu redzamības pakalpojums ir pieejams šādās versijās:

- **Krājumu redzamības pievienojumprogramma korporācijai Microsoft Dynamics 365 Supply Chain Management** — uzņēmumiem, kuriem ir derīga Supply Chain Management licence, krājumu redzamība ir pieejama bez papildu maksas. Tā kā krājumu redzamības pamatā Microsoft Power Platform ir, uz to attiecas krātuves Microsoft Power Platform noslodzes un API ierobežojumi. Supply Chain Management licencē ir jāiekļauj noklusējuma krātuve un API ietilpība. Ja jums nepieciešama lielāka krātuves vieta un API ietilpība, varat iegādāties profesionālu licenci. Detalizētu informāciju par noklusējuma API piešķiršanu un profesionālo licenci skatiet sadaļā [Ierobežojumu un piešķīrumu](/power-platform/admin/api-request-limits-allocations) pieprasīšana un [Licencēšanas pārskats Microsoft Power Platform](/power-platform/admin/pricing-billing-skus). Izmantojot noklusējuma krātuvi un API piešķīrumus, varat sākt izmēģināt krājumu redzamības pievienojumprogrammu jau šodien. Detalizētu informāciju par instalēšanu skatiet sadaļā [Krājumu redzamības](inventory-visibility-setup.md) instalēšana un iestatīšana. Ja jūsu aprēķinātais API un krātuves lietojums pārsniedz standarta piešķīrumu, varat sazināties ar savu tirdzniecības pārstāvi un lūgt viņu sazināties ar platformas komandu, lai saņemtu izņēmumu.
- **Krājumu redzamības pakalpojums kā IOM komponents - šī versija ir paredzēta inteliģentās pasūtījumu pārvaldības (IOM**) klientiem vai uzņēmumiem, kas neizmanto Supply Chain Management kā savu ERP sistēmu. Licence ir iekļauta inteliģentās pasūtījumu pārvaldības komplektā. Papildinformāciju skatiet sadaļā [Pārskats par viedo pasūtījumu pārvaldību](/dynamics365/intelligent-order-management/overview).

## <a name="inventory-visibility-terminology"></a>Krājumu redzamības terminoloģija

Strādājot ar krājumu redzamības pievienojumprogrammu, ir svarīgi saprast tālāk norādītos jēdzienus un terminus.

- **Datu avots — datu avots** attēlo sistēmu, no kuras ir jūsu dati.
- **Izmēri — izmēri** identificē produkta īpašības. Tās var būt krātuves dimensijas (piemēram, vieta vai noliktava) vai preču dimensijas (piemēram, krāsa, izmērs vai stils).
- **Fiziskie mēri** — fiziskie mēri ir daudzumi, kas mēra dažādus krājumu statusus, piemēram, rīcībā, iegādāti, pasūtīti vai pārdoti.
- **Aprēķinātie mēri — aprēķinātie mēri ir kvantitatīvi mēri**, kas tiek aprēķināti no fizisko mēru kopas. Piemēram, aprēķinātais mērs Kopējais pieejamais tiek aprēķināts kā *Rīcībā iegādāts* *–* + *Pēc pasūtījuma* – *Pārdots* *.*
- **Nodalījums** — nodalījums definē hierarhiju, kā krājumu redzamība izplatīs saņemtos datus. Pašlaik noklusējuma nodalījums ir vieta un atrašanās vieta.
- **Indeksu hierarhija — indeksu hierarhija** tālāk definē, kā vēlaties vaicāt krājumus un iegūt rezultātus, kuriem ir detalizētāka informācija.

Papildinformāciju par šiem terminiem un jēdzieniem skatiet krājumu [redzamības](inventory-visibility-configuration.md) konfigurēšana.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
