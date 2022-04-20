---
title: Krājumu redzamības pievienojumprogrammas pārskats
description: Šajā tēmā skaidrots, kas ir Krājumu redzamība un apraksta tās funkcijas.
author: yufeihuang
ms.date: 03/18/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9eb8a135d2415c867c746a1c40a80cdb84819c0e
ms.sourcegitcommit: d475dea4cf13eae2f0ce517542c5173bb9d52c1c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/05/2022
ms.locfileid: "8547906"
---
# <a name="inventory-visibility-add-in-overview"></a>Krājumu redzamības pievienojumprogrammas pārskats

[!include [banner](../includes/banner.md)]

Krājumu redzamības pievienojumprogramma (*tiek* saukta arī par krājumu redzamības pakalpojumu) nodrošina neatkarīgu un ļoti mērogojamu mikropakošanu, kas iespējo rīcībā esošo krājumu izmaiņu reāllaika grāmatojumus un redzamības izsekošanu visos datu avotos un kanālos. Tā nodrošina platformu, kas ļauj pārvaldīt globālos krājumus, izmantojot funkcionalitāti, kas ietver (bet nav ierobežota) šādu sarakstu:

- Centrāāli izsekojiet pēdējo krājumu statusu (piemēram, rīcībā esošo, pasūtīto, iepirkto, nopirkto, atgriezto un karantīnu) visos datu avotos, noliktavās un atrašanās vietās, savienojot piegādes ķēdes pārvaldību vai trešās puses loģistikas datu avotus (piemēram, pasūtījumu pārvaldības sistēmas, \[trešās puses uzņēmuma resursu plānošanas ERP\] sistēmas, pārdošanas \[POS\] sistēmu un noliktavas pārvaldības sistēmas) ar Krājumu redzamības pakalpojumu.
- Vaicāt rīcībā esošo krājumu pieejamību un iztrūkumus un iegūt tūlītēju atbildi, izsaucot krājumu redzamības pakalpojumu tieši.
- Izvairītos no cenas, it īpaši, ja jūsu pieprasījums ir no dažādiem kanāliem, veicot reāllaika vieglās rezervācijas krājumu redzamības pakalpojumā.
- Labāk pārvaldiet solītos pasūtījumus un debitoru cerības, nodrošinot precīzus pašreizējos vai nākamos pieejamos datumus, tā, lai solīšanai pieejamais rēķins (ATP) varētu aprēķināt prognozētos pasūtījuma izpildes datumus.

## <a name="extensibility"></a>Paplašināmība

Krājumu redzamības pakalpojums ir ļoti paplašināms, jo datu ievade un izvade nav ierobežota ar Microsoft programmām. Ārējās sistēmas var piekļūt pakalpojumam ar RESTful application programming interfaces (API). Papildus piegādes ķēdes pārvaldības datu avotam un dimensijām nodrošināto izvēles kartējumu izmantošanai varat integrēt Krājumu redzamību vairākās trešās personas sistēmās, iestatot papildu datu avotus, krājumu statusus (*tos* sauc par fiziskajiem līdzekļiem krājumu redzamības pakalpojumā) un krājumu dimensijas, izmantojot konfigurācijas programmu. Šādā veidā var elastīgi veikt vaicājumu un mainīt vairākus datu avotus un iepriekš definētas krājumu dimensijas.

Turklāt, tā kā ir veidota krājumu redzamība Microsoft Dataverse, tās datus var izmantot, lai veidotu un integrētu ar Power Apps. Var izmantot arī, lai Power BI izveidotu pielāgotus informācijas paneļus, kas atbilst uzņēmuma prasībām.

## <a name="scalability"></a>Mērogojamību

Atkarībā no datu apjoma krājumu redzamības pakalpojumu var samazināt vai samazināt. Mērogojamības pieredze ir lielākā daļa viengabalu, un to veic Microsoft platformu grupa, pamatojoties uz automātisku darbību datu apjoma noteikšanu un vērtēšanu.

## <a name="feature-highlights"></a>Līdzekļu iezīmēšana

### <a name="get-a-global-view-of-real-time-inventory"></a>Iegūt reāllaika krājumu globālo skatu

Krājumu redzamība nodrošina, ka visos kanālos, vietās un noliktavās jums visu laiku ir piekļuve vislietākais krājumu daudzumam. Jūs no tā gūsiet lielāko labumu, lai atbalstītu ikdienas darbību biznesu ikreiz, kad jāiegūst krājumu ieraksti. Fiziskie rīcībā esošie krājumi, pārdotie daudzumi un iepirktie daudzumi visi ir pieejami no kastes. Jūs variet arī konfigurēt citus fiziskus krājumu pasākumus (piemēram, atgrieztus, karantīnu un iegrāmatotus datus) pēc savas atrašanās vietas, lai iegūtu šo informāciju reāllaikā. Krājumu redzamība var efektīvi apstrādāt miljonu krājumu izmaiņu grāmatošanas. Šos datus var apkopot un atspoguļot jaunākajos krājumu daudzumos pakalpojumā nekavējoties, sekundē vai minūtē atkarībā no datu grāmatošanas intervāla. Plašāku informāciju skatiet krājumu redzamības [publiskajiem API](inventory-visibility-api.md).

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Vieglā rezervācija, lai izvairītos no cenu pārklāšanās visos pasūtījuma kanālos

Vieglā *rezervācija ļauj* piešķirt vai atzīmēt noteiktus daudzumus, lai izpildītu pasūtījumu vai pieprasījumu. Vieglā rezervācija neietekmē fiziskos krājumus, *bet* tā atskaitās no rezervēšanas krājumu daudzuma pieejamā daudzuma un nodrošina atjauninātu daudzumu turpmāko pasūtījuma nosacījumu izpildei. Šī funkcija būs noderīga, ja pārdošanas pieprasījumi vai pasūtījumi jūsu uzņēmumā ienāk no viena vai vairākiem kanāliem vai datu avotiem, kas ir ārpus jūsu uzņēmuma resursu plānošanas (ERP) sistēmas.

Ja krājumu redzamības pakalpojumā netiek lietotas vieglās rezervācijas, jums ir jāuzgaida, līdz pasūtījums tiek sinhronizēts un apstrādāts, izmantojot ERP sistēmu, lai atjauninātu fizisko krājumu daudzumu. Parasti šim procesam ir ļoti liels latentums. Tomēr vieglās rezervācijas stājas spēkā nekavējoties katru reizi, kad pārdošanas kanālos tiek ģenerēts pārdošanas pieprasījums vai pasūtījums. Tāpēc tie palīdz novērst pārsaukt situācijas, nodrošinot, ka jūsu pārdošanas kanālu pasūtījumi netiks atbalstīti viens ar otru, kad tie visbeidzot sasniedz ERP sistēmu. Vieglās rezervācijas nodrošina arī to, ka varat izpildīt visus pasūtījumus, ko esat solīti. Tāpēc tie palīdz jums apmierināt debitora cerības un uzturēt debitoru lojalitāti. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas rezervācijas](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-dates-confirmation"></a>ATP datumu tūlītējā atbilde

Ir svarīga jūsu tuvāko turpmāko prognozēto krājumu redzamība (ieskaitot piegādi, pieprasījumu un detalizētu informāciju par rīcībā ajiem krājumiem), jo tas palīdz uzņēmumam sasniegt šādus mērķus:

- Minimizēt krājumu līmeņus, lai samazinātu krājumu pārvaldības izmaksas.
- Atvieglot iekšējā pasūtījuma apstrādi, lai pārdevēji varētu aprēķināt nosūtīšanas un piegādes datumus, balstoties uz pasūtīto preču pieejamību.
- Nodrošināt caurspīdīgumu par to, kad debitori var gaidīt, ka noliktavā pieejams krājums kļūs pieejams, norādot nākamo pieejamo datumu.

ATP funkcija ir viegli pieņemt savā ikdienas pasūtījumu izpildes procesā. Līdzīgi, kā tas ir ar citiem krājumu redzamības piedāvājumiem, ATP funkcija ir *globāla un reāllaika*. Tāpēc jūs variet iestatīt vairākas ATP aprēķina formulas, lai būtu pilnīgas krājumu pieejamības vaicājumi, kas aptver visus jūsu biznesa kanālus un datu avotus. Papildinformāciju skatiet krājumu redzamības [rīcībā esošo izmaiņu grafiki un apsolīšanai pieejamos.](inventory-visibility-available-to-promise.md)

### <a name="compatibility-with-advanced-warehouse-management-items"></a>Saderība ar papildu noliktavas pārvaldības krājumiem

Microsoft krājums, kas nodrošina ārpus kastes integrāciju ar papildu noliktavas pārvaldību (WHS), lai WHS debitori varētu gūt labumu no krājumu redzamības pakalpojuma. Katrā 2022. gada 1. laidiena laidienā (publiskais priekšskatījums martā), krājumu pakalpojums atbalsta WHS krājumu rīcībā esošos vaicājumus un ATP. Nākamajā laišanā WHS debitoriem tiks atbalstīts vieglās rezervēšanas un piešķiršanas līdzeklis. Papildinformāciju skatiet noliktavas [redzamības atbalsta sadaļā WHS krājumiem](inventory-visibility-whs-support.md).

## <a name="licensing"></a>Licencēšana

Krājumu redzamības pakalpojums ir pieejams šādās versijās:

- **Krājumu redzamības pievienojumprogramma korporācijai Microsoft Dynamics 365 Supply Chain Management** — uzņēmumiem, kuriem ir derīga piegādes ķēdes pārvaldības licence; krājumu redzamība ir pieejama bez papildu licences izmaksām. Varat sākt to izmēģini šodien. Detalizētu informāciju par instalāciju skatiet sadaļā [Krājumu redzamības instalēšana un iestatīšana](inventory-visibility-setup.md).
- **Krājumu redzamības pakalpojums kā IOM** komponents — šī versija ir klientiem Intelligent Order Management (IOM), vai uzņēmumiem, kas kā ERP sistēmu nelieto piegādes ķēžu pārvaldību. Šī licence ir iekļauta IOM komplektā. Papildinformāciju skatiet sadaļā Intelligent [Order Management pārskats](/dynamics365/intelligent-order-management/overview).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
