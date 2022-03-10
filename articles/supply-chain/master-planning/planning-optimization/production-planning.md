---
title: Ražošanas plānošana
description: Šajā tēmā ir aprakstīta ražošanas plānošana un skaidrots, kā modificēt plānotos ražošanas pasūtījumus, izmantojot plānošanas optimizāciju.
author: ChristianRytt
ms.date: 06/01/2021
ms.topic: article
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 85167e3de5f586c341143a43412501377a6c689e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570901"
---
# <a name="production-planning"></a>Ražošanas plānošana

[!include [banner](../../includes/banner.md)]

Optimizācijas plānošana atbalsta vairākus ražošanas scenārijus. Ja migrēsit no esošās iebūvētās vispārējās plānošanas programmas, ir svarīgi atcerēties kādu no mainītajiem scenārijiem.

Tālāk sniegtais video sniedz īsu ievadu dažiem šajā tēmā minētajiem koncepcijām: [Dynamics 365 Supply Chain Management: optimizācijas uzlabojumu plānošana](https://youtu.be/u1pcmZuZBTw).

## <a name="turn-on-this-feature-for-your-system"></a>Līdzekļa ieslēgšana sistēmā

Ja sistēmā vēl nav ietverti šajā tēmā aprakstītie līdzekļi, pārejiet uz sadaļu [Līdzekļu pārvaldība](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un iespējojiet līdzekli *Plānotie ražošanas pasūtījumi Plānošanas optimizācijai*.

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

Lai nodrošinātu, ka plānošanas optimizācijai ir informācija, kas ir nepieciešama pareiza rezultāta aprēķināšanai, jums ir jāietver visas preces, kurām ir jebkāda saistība ar precēm visā plānotā pasūtījuma MK struktūrā. Plānošanas scenārijos, kuros ietilpst ražošana, mēs iesakām izvairīties palaist filtrētas vispārējās plānošanas.

Lai arī pakārtotie atvasinātie krājumi tiek automātiski noteikti un ietverti vispārējā plānošanā, kad tiek izmantota iebūvētā vispārējās plānošanas programma, plānošanas optimizācija šobrīd neveic šo darbību.

Piemēram, ja MK struktūras preces A skrūve tiek izmantota arī preces B ražošanai, tad visas preces A un B preču MK struktūrā ir jāiekļauj filtrā. Tā kā ir sarežģīti nodrošināt visu preču ietveršanu filtrā, ieteicams izvairīties no filtrētas vispārējās plānošanas, kad ir iesaistīti ražošanas pasūtījumi. Pretējā gadījumā vispārējā plānošana sniegs nevēlamus rezultātus.

### <a name="reasons-to-avoid-filtered-master-planning-runs"></a>Iemesli izvairīties palaist filtrētas vispārējās plānošanas

Palaižot preces filtrētu vispārējo plānošanu, plānošanas optimizācija (atšķirībā no iebūvētās vispārējās plānošanas programmas) nenosaka visus šīs preces MK struktūras apakšproduktus un izejmateriālus un tāpēc neiekļauj tos vispārējā plānošanā. Kaut arī plānošanas optimizācija identificē pirmo līmeni preces MK struktūrā, no datu bāzes netiek ielādēti preču iestatījumi (piemēram, noklusējuma pasūtījuma veids vai krājuma nodrošinājums).

Plānošanas optimizācijas gadījumā vispirms tiek ielādēti palaišanas dati un pielietoti filtri. Tas nozīmē, ka gadījumā, ja konkrētā precē iekļautais apakšprodukts vai izejmateriāls nav daļa no filtra, informācija par to nebūs ietverta palaišanā. Turklāt, ja apakšprodukts vai izejmateriāls ir iekļauts arī citā precē, tad filtrēta palaišana, kas ietver tikai oriģinālo preci un tās komponentus, noņems esošo plānoto pieprasījumu, kas tika izveidots citai precei.

Šī loģika var izraisīt filtrētas vispārējās plānošanas palaišanas darbībām sniegt neatbalstītus rezultātus. Turpmākajās sadaļās sniegti piemēri, kas attēlo iespējamos neatbalstītos rezultātus.

### <a name="example-1"></a>1. piemērs

Saražotās preces *FG* sastāv no tālāk norādītajiem komponentiem:

- Izejmateriāls *R*
- Apakšprodukts *S1*, kas sastāv no apakšprodukta *S2*

Krājumi ir pieejami izejmateriālam *R*, bet krājumos nav apakšprodukta *S1*.

Veicot filtrētu vispārējo plānošanas palaišanu saražotajām precēm *FG*, iegūsit plānoto ražošanas pasūtījumu saražotajām precēm *FG*, plānoto pirkšanas pasūtījumu izejmateriālam *R* un plānoto pirkšanas pasūtījumu apakšproduktam *S1*. Tas ir nevēlams rezultāts, jo plānošanas optimizācija ir ignorējusi esošo izejmateriālu *R* piegādi un apakšproduktam *S1* ir jābūt ražotam, izmantojot *S2*, nevis tieši pasūtītam. Tas notika tāpēc, ka plānošanas optimizācijai ir tikai saražoto preču *FG* komponentu saraksts bez jebkādas saistītas informācijas, piemēram, ar esošo komponentu piegādi vai to noklusējuma pasūtījuma iestatījumiem.

### <a name="example-2"></a>2. piemērs

Balstoties uz iepriekšējo piemēru, papildus saražotajām precēm arī *FG2* izmanto apakšproduktu *S1*. Plānotais pasūtījums ir saražotajām precēm *FG2* un plānotais pieprasījums ir visiem komponentiem, tostarp *S1*.

Jūs nolemjat labot filtrētās vispārējās plānošanas nevēlamos resultātus no iepriekšējā piemēra, pievienojot filtram visus MK struktūras apakšproduktus un izejmateriālus no saražotajām precēm *FG* un pēc tam veicot pilnu atkārtotu palaišanu.

Veicot pilnu atkārtotu palaišanu, sistēma izdzēš visus esošos rezultātus visām iekļautajām precēm un pēc tam atkārtoti izveido rezultātus, pamatojoties uz jaunajiem aprēķiniem. Tas nozīmē, ka esošais plānotais pieprasījums precei *S1* tiek izdzēsts un pēc tam izveidots no jauna, ņemot vērā tikai saražoto preču *FG* prasības, bet saražotās preces *FG2* prasības netiek ņemtas vērā. Tas notiek, jo, palaižot plānošanas optimizāciju, netiek iekļauts citu plānoto ražošanas pasūtījumu plānotais pieprasījums&mdash;tiek izmantots tikai palaišanas laikā ģenerētais plānotais pieprasījums.

> [!NOTE]
> Ja esošais plānotais pasūtījums saražotajām precēm *FG2* ir ar statusu *Apstiprināts*, tad apstiprinātais plānotais pieprasījums tiks iekļauts pat tad, ja pamatprodukts netiks pievienots filtram.

Tāpēc, ja nepievienosit visus saražoto preču *FG* komponentus, saražotās preces *FG2* un visus citus produktus, kas ir šo komponentu daļa (kopā ar to komponentiem), filtrētā vispārējās plānošanas palaišana nodrošinās nevēlamus rezultātus.

Tā kā ir sarežģīti nodrošināt visu preču ietveršanu filtrā, ieteicams izvairīties no filtrētas vispārējās plānošanas, kad ir iesaistīti ražošanas pasūtījumi.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
