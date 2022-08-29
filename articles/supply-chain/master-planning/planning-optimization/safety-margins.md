---
title: Drošības rezerves
description: Šajā rakstā ir aprakstīts, kā drošības rezerves var izmantot ar Microsoft plānošanas optimizācijas pievienojumprogrammu Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 247b48afab68651cff0ce84c8268a1df35a15c02
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335201"
---
# <a name="safety-margins"></a>Drošības rezerves

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā drošības rezerves var izmantot ar Microsoft plānošanas optimizācijas pievienojumprogrammu Dynamics 365 Supply Chain Management.

## <a name="safety-margins-overview"></a>Drošības rezervju apskats

Drošības rezervju nolūks ir iespējot iestatījumu, kas nodrošina zināmu bufera laiku pēc parastā izpildes laika. Piemēram, ja materiālam jābūt izsaiņotam vai pārbaudītam pēc tā saņemšanas no kreditora, jūs nevarat vienkārši pievienot papildu laiku pirkšanas izpildes laikam, jo šī pieeja piegādātājam dos papildu bufera laiku. Šajā piemērā ieejas plūsmas rezerve var tikt izmantota, lai nodrošinātu, ka piegādātājs piegādā agrāk. Šī pieeja nodrošina bufera laiku, lai preces varētu apstrādāt iekšēji.

Ir pieejami trīs drošības rezervju veidi.

- **Pasūtījuma rezerve** – bufera laiks piegādes pasūtījuma izvietošanai
- **Ieejas plūsmas rezerve** – bufera laiks ienākošās piegādes apstrādei
- **Izejas plūsmas rezerve** – kravu apstrādes bufera laiks

Šajā attēlā parādīts, kā šīs drošības rezerves tiek piemērotas laika gaitā.

![Drošības rezerves.](media/safety-margins-1.png)

Visas rezerves ir definētas dienās. Noklusējuma vērtība, *0* (nulle), norāda, ka rezerve netiek lietota. Iestatot vairākas vezerves, tās visas pievieno kopējam laikam no piegādes *pasūtījuma datuma* līdz pieprasījuma *vajadzības datumam* . Piemēram, iestatījumam nav izpildes laika, un visi trīs vezervju veidi ir iestatīti uz vienu dienu. Šādā gadījumā starp piegādes pasūtījuma datumu un pieprasījuma vajadzības datumu būs trīs dienas, tātad, ja pasūtījuma datums ir 1. jūlijs, vajadzības datums ir 4. jūlijs.

### <a name="receipt-margin"></a>Ieejas plūsmas rezerve

Ieejas plūsmas rezerve visticamāk tiek izmantota trijās drošības rezervēs. Tā ir piemērota *izpildes datumam* un pretēji no *pieprasījuma datuma*. Citiem vārdiem, preces jāsaņem pirms norādītā saņemšanas uzcenojuma dienu skaita no tās dienas, kad tās tiek pieprasītas.

Sekojošajā attēlā ir parādīta ieejas plūsmas rezerve.

![Ieejas plūsmas rezerve.](media/safety-margins-2.png)

Parasti ieejas plūsmas rezerve tiek izmantota kā buferis, lai nodrošinātu noliktavas reģistrācijas laiku vai citus laikietilpīgus procesus, kas netiek uztverti kā daļa no vispārējā izpildes laika sistēmā. Pirkumiem viena priekšrocība ir tāda, ka pirkšanas pasūtījuma *piegādes datums* tiek attiecīgi pārvietots uz priekšu. Palielinot izpildes laiku tā vietā, lai izmantotu drošības rezervi, kreditoram joprojām tiks lūgts veikt piegādi pēdējā minūtē.

Ievērojiet, ka ieejas plūsmas rezerve nemaina piegādes *vajadzības datumu*. Tāpēc ieejas plūsmas rezerve nav tieši redzama, ja tiek salīdzināti pieprasījuma un piedāvājuma vajadzības datumi (piemēram, lapā **Neto vajadzības** ). Piemēram, ja ieejas plūsmas rezerve ir iestatīta uz četrām dienam un pirkšanas pasūtījuma rinda ir plānota saņemšanai mēneša piecpadsmitajā datumā, vispārējā plānošana par koriģēto saņemšanas datumu aprēķina mēneša deviņpadsmito datumu.

Ņemiet vērā, ka ieejas plūsmas rezerve netiek lietota, kad piegādei tiek izmantots rīcībā esošais krājums. Visi rīcībā esošie krājumi tiek uzskatīti par pieejamiem nekavējoties, neskatoties uz to, kad tie tika faktiski saņemti.

### <a name="reorder-margin"></a>Pasūtījuma rezerve

Sekojošajā attēlā ir parādīta pasūtījuma rezerve.

![Pasūtījuma rezerve.](media/safety-margins-3.png)

Pasūtījuma rezerve tiek pievienota pirms krājuma izpildes laika visiem plānotajiem pasūtījumiem vispārējās plānošanas laikā. Tāpēc tā nodrošina papildu laiku piegādes pasūtījuma ievietošanai. Šī rezerve parasti tiek izmantota kā buferis, lai nodrošinātu laiku apstiprināšanas procesiem vai citiem iekšējiem procesiem, kas ir nepieciešami piegādes pasūtījumu izveides laikā. Pasūtījuma rezerve tiek novietota starp piegādes *pasūtījuma datumam* un *sākuma datumam*.

### <a name="issue-margin"></a>Izejas plūsmas rezerve

Sekojošajā attēlā ir parādīta izejas plūsmas rezerve.

![Izejas plūsmas rezerve.](media/safety-margins-4.png)

Vispārējās plānošanas laikā izejas plūsmas rezerve tiek atskaitīta no pieprasījuma vajadzības datuma. Tas palīdz nodrošināt, ka ir laiks reaģēt un nosūtīt ienākošos pieprasījuma pasūtījumus. Šo rezervi parasti izmanto kā buferi, lai nodrošinātu nosūtīšanas laiku un saistītos nosūtīšanas noliktavas procesus.

Ievērojiet, ka tad, kad tiek lietota izejas plūsmas rezerve, saistītie piedāvājuma un pieprasījuma datumi nesakrīt. Tā vietā tie atšķiras ar izejas plūsmas rezervi, jo izejas plūsmas rezerve tiek pievienota starp piegādes *vajadzības datumu* un pieprasījuma *vajadzības datumu*.

## <a name="set-up-safety-margins"></a>Iestatīt drošības rezerves

### <a name="turn-safety-margins-on-or-off"></a>Drošības rezervju izslēgšana vai izslēgšana

Lai izmantotu šo funkciju, tai jābūt ieslēgtai jūsu sistēmai. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 funkcija ir obligāta, un to nevar izslēgt. Ja lietojat versiju, kas vecāka par 10.0.29, administratori šo funkcionalitāti var ieslēgt vai izslēgt, meklējot *optimizācijas*[līdzekļu](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) plānošanas līdzekli līdzekļu pārvaldības darbvietā.

### <a name="define-safety-margins"></a>Definēt drošības rezerves

Drošības rezervēm ir elastīga iestatīšana. Tos var iestatīt gan *seguma grupai*, gan *vispārējam plānam* . Ir svarīgi saprast, ka rezerves tiek pievienotas viena otrai virsū. Piemēram, ieejas plūsmas rezerve seguma grupai divām dienam un trījām dienam vispārējām plānam radīs efektīvu ieejas plūsmas rezervi piecām dienām.

Iespēja iestatīt rezervi vispārējām plānam var būt noderīga, ja vēlaties simulēt ilgāku izpildes laiku vai nenoteiktību konkrētam plānam, bet neietekmējot ikdienas plānošanu.

#### <a name="coverage-group-safety-margins"></a>Seguma grupas drošības rezerves

Lai pielietotu drošības rezervi seguma grupai, veiciet šādas darbības.

1. Dodieties uz sadaļu **Vispārējā plānošana \> Iestatījumi \> Seguma grupas**.
1. Sarakstu rūtī atlasiet nepieciešamo seguma grupu.
1. Kopsavilkuma cilnē **Cits** sadaļā **Drošības rezerves dienās** izmantojiet sekojošos laukus, lai iestatītu nepieciešamās drošības rezerves (dienās):

    - Pievienotā ieejas plūsma pieprasījuma datumam
    - Atskaitītā izejas plūsma no pieprasījuma datuma
    - Pasūtījuma rezerve, kas pievienota krājumam izpildes laikā

#### <a name="master-plan-safety-margins"></a>Vispārējā plāna drošības rezerves

Lai pielietotu drošības rezervi vispārējām plānam, veiciet šādas darbības.

1. Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**.
1. Sarakstu rūtī atlasiet nepieciešamo vispārējo plānu.
1. Kopsavilkuma cilnē **Drošības rezerves dienās** izmantojiet sekojošos laukus, lai iestatītu nepieciešamās drošības rezerves (dienās):

    - Pievienotā ieejas plūsma pieprasījuma datumam
    - Atskaitītā izejas plūsma no pieprasījuma datuma
    - Pasūtījuma rezerve, kas pievienota krājumam izpildes laikā

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a>Definējiet, vai aprēķini ir balstīti uz kalendārajām dienām vai darba dienām

Varat iestatīt visas drošības rezerves tā, lai tās tiktu aprēķinātas, balstoties uz kalendāra dienām vai darba dienām.

1. Dodieties uz **Vispārējā plānošana \> Iestatīšana \> Vispārējas plānošanas parametri**.
1. Cilnē **Vispārīgi** sadaļā **Drošības rezerves dienās** iestatiet opciju **Darba dienas** uz *Jā*, lai aprēķinātu rezerves, balstoties uz darbdienām. Iestatiet opciju uz *Nē*, lai aprēķinātu rezerves, pamatojoties uz kalendārām dienām.

Piemēram, kalendārs ir atvērts no pirmdienas līdz piektdienai un ir slēgts no sestdienas līdz svētdienai. Ja ir vienas dienas ieejas plūsmas rezerve, vajadzības datums pirmdien izveido piegādes datumu iepriekšējā piektdienā, jo sestdienas un svētdienas nav darba dienas.

Kalendārs, kas tiek izmantots darba dienu noteikšanai, ir atkarīgs no iestatījuma un piegādes veida. To var kontrolēt seguma grupas, noliktavas un kreditora kalendāri.

> [!NOTE]
> Ja *noliktava* nav daļa no seguma dimensijas (citiem vārdiem, plānošana ir balstīta tikai uz *vietnes*), noliktavas kalendārs netiek lietots.

Sistēma var apstrādāt iestatījumu, kur ir definēti viens vai vairāki kalendāri. Šajās apakšsadaļās ir aprakstītas iespējamās kombinācijas, ko var izmantot, lai kontrolētu rezultātu.

#### <a name="calendar-that-is-used-for-the-duration"></a>Kalendārs, kas tiek izmantots ilgumam

Definētie kalendāri kontrolē faktisko kopējās izpildes laiku kalendārās dienās no piegādes pasūtījuma datuma līdz pieprasījuma vajadzības datumam. Tiek izmantota šāda kalendāra prioritātes noteikšana:

- **Pirkšanas izpildes laiks** – tiek ņemts vērā tikai seguma grupas kalendārs.
- **Ieejas plūsmas rezerve** – seguma grupas kalendārs tiek lietots, ja tas ir definēts. Pretējā gadījumā tiek izmantots noliktavas kalendārs.
- **Izejas plūsmas rezerve** – seguma grupas kalendārs tiek lietots, ja tas ir definēts. Pretējā gadījumā tiek izmantots noliktavas kalendārs.
- **Pasūtījuma rezerve** – tiek ņemts vērā tikai seguma grupas kalendārs.

#### <a name="calendar-that-is-used-for-the-final-date"></a>Kalendārs, kas tiek izmantots beigu datumam

Lai noteiktu, vai plānošanas programma konkrētajam datuma veidam var izmantot norādīto datumu, tiek piemēroti šādi noteikumi:

- **Pirkšanas saņemšanas datums** – tiek izmantots kreditora kalendārs, ja tas ir definēts. Pretējā gadījumā seguma grupas kalendārs tiek lietots, ja tas ir definēts. Ja neviens no šiem kalendāriem nav definēts, tiek izmantots noliktavas kalendārs.
- **Pārsūtīšanas saņemšanas datums** – seguma grupas kalendārs tiek lietots, ja tas ir definēts. Pretējā gadījumā tiek izmantots noliktavas kalendārs.
- **Ražošanas saņemšanas datums** – seguma grupas kalendārs tiek lietots, ja tas ir definēts. Pretējā gadījumā tiek izmantots noliktavas kalendārs.
- **Pieprasījuma jautājuma atvēršanas diena** – noliktavas grupas kalendārs tiek lietots, ja tas ir definēts. Pretējā gadījumā tiek lietots seguma grupas kalendārs.
- **Pasūtījuma atvēršanas diena** – tiek izmantota seguma grupas kalendāra un kreditora kalendāra kombinācija (krustošanās). Lai izmantotu šo datumu, abiem kalendāriem ir jābūt atvērtiem. Ja tikai viens no šiem kalendāriem ir definēts, tiek izmantots tikai tas kalendārs.

#### <a name="calendar-setup-overview-matrix"></a>Kalendāra iestatīšanas pārskata matrica

Sekojošajā attēlā redzama matrica, kas apkopo, kuri kalendāri tiek lietoti, aprēķinot drošības rezerves. (Atlasiet attēlu, lai atvērtu augstas izšķirtspējas versiju.) Šādi saīsinājumi un krāsas tiek izmantotas, lai norādītu, kur katrs kalendāra tips ir norādīts:

- **Seguma grupa (Coverage group - CG):** Zaļa
- **Noliktava (Warehouse - WH):** Dzeltena
- **Kreditors (Vendor - V):** Zila

[![Kalendāra iestatīšanas pārskata matrica.](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)

## <a name="calculating-delays"></a>Kavējumu aprēķināšana

Visi trīs drošības rezervju veidi tiek iekļauti, kad sistēma nosaka, vai pasūtījums ir aizkavēts.

Piemēram, krājumam ir vienas dienas izpildes laiks un trīs dienu ieejas plūsmas rezerve. Pārdošanas pasūtījums šim krājumam ir iestatīts kā nepieciešams šodien. Šādā gadījumā aizkave tiek aprēķināta kā *izpildes laiks* + *ieejas plūsmas rezerve* = četras dienas. Tāpēc, ja šodien ir 14. augusts, četras aizkaves dienas veido piegādi 18. augustā. Tālāk redzamajā attēlā parādīts šis piemērs.

![Kavējuma aprēķina piemērs.](media/safety-margins-delays.png)

## <a name="additional-resources"></a>Papildu resursi

[Darba sākšana ar plānošanas optimizāciju](get-started.md)

[Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]