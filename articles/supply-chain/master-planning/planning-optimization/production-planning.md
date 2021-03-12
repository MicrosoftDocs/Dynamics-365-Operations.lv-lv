---
title: Ražošanas plānošana
description: Šajā tēmā ir aprakstīta ražošanas plānošana un skaidrots, kā modificēt plānotos ražošanas pasūtījumus, izmantojot plānošanas optimizāciju.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eda22aa6f1e8d665d8ef390f24b247a76d4c2956
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992399"
---
# <a name="production-planning"></a>Ražošanas plānošana

Optimizācijas plānošana atbalsta vairākus ražošanas scenārijus. Ja migrēsiet no esošās iebūvētās vispārējās plānošanas programmas, ir svarīgi atcerēties kādu no mainītajiem scenārijiem.

<!-- The following video gives a short introduction to some of the current capabilities. 
KFM: Link to video for production functionality, coming soon... -->

## <a name="planned-production-orders"></a>Plānotie ražošanas pasūtījumi

Kad vispārējā plānošana izveido plānotos pasūtījumus vajadzības izpildei, pasūtījuma tipu nosaka lauka **Plānotais pasūtījums** vērtība. Ja **Plānotā pasūtījuma tips** ir iestatīts uz *Ražošana*, tiek izveidoti plānotie ražošanas pasūtījumi. Šie plānotie ražošanas pasūtījumi ietver informāciju par aktīvo materiālu komplektu (MK) un maršruta ID no saistītā ražošanas iestatījuma.

## <a name="requirements-from-boms"></a>MK prasības

MK informācija tiek izplāta vispārējās plānošanas laikā. Plāna izvade ietver materiālu piedāvājumu, lai segtu saistīto materiālu pieprasījumu ražošanai.

Vispārējās plānošanas laikā pašreizējais aktīvais MK tiek izmantots, lai noteiktu ražošanai nepieciešamos materiālus. Šis solis tiek veikts caur visiem MK struktūras līmeņiem, kas saistīti ar pieprasīto ražošanas pasūtījumu. Materiālu vajadzības tiek izpildītas, izmantojot pieejamos rīcībā esošos krājumus, esošos pasūtījuma piegādi un apstiprinātos plānotos pasūtījumus. Ja jebkurā vietā ir nepieciešami papildu materiāli, pieprasījuma segšanai tiek izveidots plānotais pasūtījums.

## <a name="scheduling-during-firming"></a>Plānošana apstiprināšanas laikā

Plānotie ražošanas pasūtījumi ietver maršruta ID, kas nepieciešams ražošanas plānošanai. Tomēr plānošanas atbalsts plānotajiem pasūtījumiem tiek gaidīts plānošanas izpildes laikā. Maršruta ID tiek lietots plānoto ražošanas pasūtījumu plānošanai apstiprināšanas laikā. Tāpēc plānoto ražošanas pasūtījumu izpildes laiks var atšķirties no izpildes laika saistītajos, apstiprinātos ražošanas pasūtījumos, kas tiek ģenerēti no tiem, kā aprakstīts šeit:

- **Plānotais ražošanas pasūtījums** – izpildes laiks ir balstīts uz izlaistās preces statisko izpildes laiku.
- **Apstiprināts ražošanas pasūtījums** – izpildes laiks ir balstīts uz plānošanu, kas izmanto maršruta informāciju un saistītos resursu ierobežojumus.

Papildinformāciju par paredzamo līdzekļu pieejamību skatiet sadaļā [Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md).

Ja ir atkarīga ražošanas funkcionalitāte, kas vēl nav pieejama optimizācijas plānošanai, varat turpināt izmantot iebūvēto vispārējās plānošanas programmu. Izņēmumi nav nepieciešami.

## <a name="delays"></a>Aizkaves

Ja pieprasītā materiāla izpildes laiks ir ilgāks par laiku starp šodienas datumu un materiālu vajadzības datumu, pieprasītā materiāla plānotais pasūtījums un saistītais ražošanas pasūtījums tiks aizkavēts. Plānotiem pasūtījumiem aizkave (dienās) tiek aprēķināta, pamatojoties uz izpildei nodotās preces izpildes laiku. Tad aizkavēšanās informācija tiek izplatīta caur visiem MK struktūras līmeņiem. Tāpēc var izsekot atlikto izejmateriālu ietekmi visu veidu debitora pārdošanas pasūtījumam.

## <a name="modifying-planned-orders"></a>Plānoto pasūtījumu uzturēšana

Kad jūs maināt informāciju plānotajā pasūtījumā, jūs saņemat šādu ziņojumu: "Ievērojiet, ka manuālo izmaiņu ietekme uz plānotajiem pasūtījumiem netiks atspoguļota pārējā plānā līdz nākamās vispārējās plānošanas palaišanai."

Ja vēlaties mainīt informāciju plānotajā pasūtījumā un redzēt ietekmi uz saistītajām materiālu vajadzībām, sekojiet šiem soļiem.

1. Atjauniniet plānoto pasūtījumu.
2. Apstipriniet plānoto pasūtījumu.
3. Palaidiet vispārējo plānošanu.

Palaižot vispārējo plānošanu, nav jāizmanto filtri, ja iekļauti plānotie ražošanas pasūtījumi. Papildinformāciju skatiet šīs tēmas turpinājumā esošajā sadaļā [Filters](#filters).

> [!NOTE]
> Ja plānotā pasūtījuma piegādes datums tiek mainīts uz vēlāku datumu, pieprasījums var tikt piesaistīts jaunajam plānotajam pasūtījumam. Šī darbība notiek, kad jaunais piegādes datums izraisa piesaistītā pieprasījuma aizkavēšanos, bet atbilstīgi izpildes laika iestatījumiem aizkavēšanos var kavēt.

## <a name="explosion-page"></a>Izvēršanas lapa

Jūs varat izmantot **Izvēršanas** lapu, lai analizētu pieprasījumu, kas nepieciešams noteiktam ražošanas pasūtījumam vai plānotam ražošanas pasūtījumam, saistītajam segumam un piesaistes informācijai. Informācija par **Izvēršanas** lapu tiek atjaunināta vispārējās plānošanas laikā. Informāciju nevar atjaunināt tieši no **Izvēršanas** lapas.

## <a name="filters"></a><a name="filters"></a>Filtri

Plānošanas scenārijos, kuros ietilpst ražošana, mēs iesakām izvairīties no filtrētām vispārējās plānošanas palaišanas. Lai nodrošinātu, ka plānošanas optimizācijai ir informācija, kas ir nepieciešama pareizā rezultāta jāaprēķina, ir jāietver visas preces, kurām ir jebkādas saistības ar precēm visā plānotā pasūtījuma MK struktūrā.

Lai arī pakārtotie pakārtotie krājumi tiek automātiski noteikti un ietverti vispārējā plānošanā, kad tiek izmantota iebūvētā vispārējās plānošanas programma, plānošanas optimizācija neveic šo darbību.

Piemēram, ja viena produkta A MK struktūras skrūve tiek izmantota arī preces B ražošanai, tad visi produkti A un B preču MK struktūrā jāiekļauj filtrā. Tā kā tā var būt ļoti sarežģīta, lai nodrošinātu, ka visas preces ir daļa no filtra, ieteicams izvairīties no filtrētas vispārējās plānošanas, kad ir iesaistīti ražošanas pasūtījumi.
