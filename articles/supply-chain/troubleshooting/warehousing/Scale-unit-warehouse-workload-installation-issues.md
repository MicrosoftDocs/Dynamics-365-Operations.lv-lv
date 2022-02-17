---
title: Apstrādes problēmas rodas pēc mēroga vienības noliktavas darba slodzes instalēšanas
description: Šajā tēmā ir aprakstītas problēmas, kas var rasties drīz pēc mēroga vienības noliktavas darba slodzes instalēšanas, un sniegti padomi to novēršanai.
author: perlynne
ms.date: 1/13/2022
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningWorkbench, WHSOutboundLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-01-13
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f589ffed61b695f471989ab1dd693f30cd5d5262
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071777"
---
# <a name="processing-issues-occur-after-a-scale-unit-warehouse-workload-is-installed"></a>Apstrādes problēmas rodas pēc mēroga vienības noliktavas darba slodzes instalēšanas

Šajā tēmā ir aprakstītas problēmas, kas var rasties drīz pēc mēroga vienības noliktavas darba slodzes instalēšanas, un sniegti padomi to novēršanai.

## <a name="issue-1-error-after-a-load-is-released-from-a-load-planning-workbench"></a>1. problēma. Kļūda pēc slodzes atbrīvošanas no slodzes plānošanas darbgalda

### <a name="symptoms-of-issue-1"></a>Problēmas simptomi 1

Kad atbrīvojat slodzi no **Slodzes plānošanas darbgalds** vai **Izejošās slodzes plānošanas darbgalds** lapā tiek parādīts šādas kļūdas ziņojums:

> Grāmatojot noslodzi %1, tika konstatēts izņēmums — noslodzi neizdevās izlaist.
> 
> ATJAUNINĀT PIEGĀDES TABULAS KOMPLEKTI...
> 
> Nevar rediģēt ierakstu sadaļā Sūtījumi (WHSShipmentTable). Sūtījuma ID:...

Šeit ir faktisks piemērs, kas ietver datu paraugus:

> Izņēmums tika noķerts, ievietojot kravu USMF-000033, kravu nevarēja atbrīvot.
Sesija 5133 (administrators)
>
> ATJAUNINĀT WHSSHIPMENTTABLE SET ORDERNUM=?,RECVERSION=?,MODIFIEDDATETIME=?,MODIFIEDBY=? KUR ((RECID=?) UN (RECVERSION=?))  
> [Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Mēroga vienība @@ mēģināja atjaunināt ierakstus, kas pieder mēroga vienībai @A.  
> Object Server Azure:
>
> Nevar rediģēt ierakstu sadaļā Sūtījumi (WHSShipmentTable). Sūtījuma ID: USMF-000031, USMF-000033. SQL datu bāze ir paziņojusi par kļūdu.

### <a name="cause-of-issue-1"></a>Problēmas cēlonis 1

Šī problēma var rasties, ja, instalējot mēroga vienības noliktavas darba slodzi, pastāv šāda nosacījumu kombinācija:

- Sistēma ietver neatbrīvotu kravu, kurā vairākas rindas ir saistītas ar dažādiem pasūtījumiem, un dažas kravas rindas nav saistītas ar sūtījumu.
- Sistēma ir iestatīta, lai izmantotu sūtījumu konsolidāciju.

Izkliedētā hibrīda topoloģijas izvietošanā katrs kravas un sūtījuma ieraksts tiek atzīmēts kā piederošs noteiktai mēroga vienībai vai centrmezglam. Kad atbrīvojat slodzi no **Slodzes plānošanas darbgalds** lapā, sistēma maina piešķirtās īpašumtiesības. Tomēr iepriekš uzskaitīto nosacījumu dēļ sistēma, iespējams, nevarēs atrisināt datu īpašumtiesības. Tāpēc tas neizdodas atbrīvot kravu uz noliktavu.

### <a name="resolution-of-issue-1"></a>1. jautājuma risinājums

Sadaliet kravu divās mazākās kravās, pirms to izlaižat noliktavā.

## <a name="issue-2-error-while-a-wave-is-processed-on-a-scale-unit"></a>2. problēma: kļūda, apstrādājot viļņu skalas vienībā

### <a name="symptoms-of-issue-2"></a>2. problēmas simptomi

Apstrādājot mēroga vienību vilni, tiek parādīts kļūdas ziņojums, kura forma ir šāda:

> Slodzes rindu nevar modificēt ar RecId =%1, ielādes id=%2 jo tas joprojām pieder uzņēmuma centram. Lūdzu, pārliecinieties, vai atbilstošā izejošā slodze ir atbrīvota uz mēroga vienību un līdz ar to ir izveidotas noliktavas pasūtījuma rindas.

Šeit ir faktisks piemērs, kas ietver datu paraugus:

> Informācijas žurnāls darbam Execute Wave USMF-000000012 (9223377668365210)  
> Informācijas žurnāls uzdevumam Izpildīt vilni USMF-000000012 (9223377668370462)  
> Slodzes rindu nevar modificēt ar RecId = 68719478242, load id= USMF-000034, jo tā joprojām pieder uzņēmuma centram. Lūdzu, pārliecinieties, vai atbilstošā izejošā slodze ir atbrīvota uz mēroga vienību un līdz ar to ir izveidotas noliktavas pasūtījuma rindas.

### <a name="cause-of-issue-2"></a>Problēmas cēlonis 2

Izplatītā hibrīda topoloģijas izvietošanā kravas un sūtījuma datu īpašumtiesības tiek piešķirtas noteiktai mēroga vienībai vai centrmezglam. Paredzams, ka datu pārvietošanas apstrādes laikā īpašumtiesības uz datiem tiks piešķirtas mēroga vienībai.

Ja instalējat mēroga vienības noliktavas darba slodzi, ja atvērts sūtījums ir saistīts ar kravu un vilni, sistēma nevar kontrolēt datu īpašumtiesības. Tāpēc skalas vienībā viļņu apstrāde neizdodas.

### <a name="resolution-of-issue-2"></a>2. jautājuma risinājums

Atbrīvojiet kravu no rumbas uz noliktavu.

## <a name="troubleshoot-issues-by-viewing-a-records-ownership-and-destination"></a>Novērsiet problēmas, apskatot ieraksta īpašumtiesības un galamērķi

Izkliedētā hibrīda topoloģijas izvietošanā daudzu veidu ieraksti tiek atzīmēti kā īpašumi noteiktai mēroga vienībai vai centrmezglam. Kad esat pārslēdzies uz izplatīto hibrīda topoloģiju un/vai iestatījis jaunu mēroga vienības noliktavas darba slodzi, sistēma piešķir īpašumtiesības katram atbilstošajam ierakstam. Šis process dažkārt var izraisīt kļūdas vai negaidītus rezultātus. Tāpēc informācija par ieraksta īpašumtiesībām un nodošanas galamērķi var palīdzēt novērst problēmas, kas rodas pēc šāda veida izmaiņu veikšanas.

Veiciet šīs darbības, lai skatītu ieraksta īpašumtiesības un nodošanas galamērķi.

1. Atveriet attiecīgo ierakstu.
1. Darbību rūtī, uz **Iespējas** cilnē **Ierakstiet informāciju** grupu, izvēlieties **Rādīt visus laukus**.
1. Parādītajā lapā tiek rādītas vērtības visiem laukiem, kas ir pieejami atlasītajam ierakstam. Pārskatiet tālāk norādītos laukus.

    - **SYSSCALEUNITID** – Šajā laukā ir redzams pašreizējais ieraksta īpašnieks.
    - **SYSTARGETSCALEUNITID** – Šajā laukā tiek rādīts centrmezgla vai mēroga vienības ID, uz kuru ieraksts tiks pārsūtīts, kad pašreizējais īpašnieks būs beidzis ar to strādāt. Šī lauka vērtību izmanto pakešu darbi, kas pārvalda šāda veida procesu. Lai gan šis lauks nav tieši saistīts ar īpašumtiesībām, īpašumtiesības var mainīties, nododot ierakstu. Dažos gadījumos šis lauks būs tukšs.
