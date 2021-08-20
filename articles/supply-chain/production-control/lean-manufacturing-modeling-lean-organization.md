---
title: Racionālas organizācijas modelēšana
description: Šajā rakstā ir sniegta informācija par racionālās organizācijas modelēšanas galvenajiem jēdzieniem.
author: cvocph
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, KanbanFlowSelection, KanbanFlow
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53141
ms.assetid: 4f272f2f-ec2c-4b0d-a652-00a63b719b9e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f30496540f6493c68d953af6b3d959acc30efbf1faf72f7cbd6de374c30b9c4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738943"
---
# <a name="modeling-a-lean-organization"></a>Racionālas organizācijas modelēšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par racionālās organizācijas modelēšanas galvenajiem jēdzieniem. 

Parasti Lean manufacturing scenārijs nozīmē vairāk nekā nesaistītu Kanban nosacījumu vai materiālu piedāvājuma politiku kolekciju. Materiālu un preču plūsmu darba šūnās un novietojumos konkrēta ražošanas vai piegādes scenārija nolūkos var raksturot kā nelielu procesu vai pārsūtīšanas aktivitāšu secību vai tīklu. Šo secību vai tīklu dēvē par ražošanas plūsmu.

## <a name="production-flows-in-lean-manufacturing"></a>Lean manufacturing ražošanas plūsmas
Ražošanas scenārijos, kuru pamatā ir ražošanas pasūtījumi, materiāls tiek izsniegts atbilstoši noteiktam ražošanas pasūtījumam. Operāciju secības laikā, kuru pamatā ir materiālu komplekti (MK) un maršruti, preces tiek izveidotas un visbeidzot tiek saņemtas norādītajā novietojumā. Ražošanas pasūtījumu caurlaides laiks var ilgt no minūtēm līdz nedēļām. Visas saistītās izmaksas, materiāli un darbaspēks tiek uzkrāti ražošanas pasūtījumā. 

Lai samazinātu piegādes izpildes laikus un liekus krājumus starp resursiem, ko izraisa partiju ražošana, Lean manufacturing ražošanas un noliktavas papildināšanā ievieš Kanban papildināšanu un lielveikalus. Parasti šie līdzekļi izjauc daļēji neatkarīgu Kanban ciklu ražošanu. Pabeigtas preces pasūtījums vairs neizraisa Kanban papildināšanu nepabeigtai precei. 

Lai atjaunotu ražošanas un izmaksu kontekstu dažādiem Kanban scenārijiem, kas tiek piedāvāti kā lean manufacturing pamats, ir ieviestas uz aktivitātēm balstītas ražošanas plūsmas. Visi Kanban nosacījumi attiecas uz šo iepriekš definētu struktūru. Ar aktivitāti saistīts modelis atbalsta plašu scenāriju klāsta iestatījumus. Taču šis modelis nevairo sarežģītību ražotnes darbiniekiem, jo visi scenāriji lieto to pašu uz aktivitātēm balstīto lietotāja interfeisu.

## <a name="semi-finished-products-non-bom-levels"></a>Nepabeigtas preces (ne no MK līmeņiem)
Lean manufacturing ir integrēti Kanban, kas paredzēti inventarizētām precēm un nepabeigtām precēm vienotā sistēmā, līdz ar to piedāvājot vienotu lietotāju pieredzi visos gadījumos. Šīs arhitektūras dēļ vairs nav jāievieš papildu MK līmeņi, lai Kanban varētu izmantot nepabeigtām precēm. Šī arhitektūra palīdz arī līdz minimumam samazināt krājumu transakcijas.

## <a name="products-and-material-in-work-in-progress"></a>Preces un materiāls nepabeigtos darbos
Partijas izmēru samazināšana līdz Lean manufacturing viengabalainas plūsmas ideālam stāvoklim var izraisīt ievērojamu krājumu transakciju pieaugumu, ja katrs izdošanas process vai Kanban reģistrācija izraisa patērēto krājumu transakcijas. Ražošanas plūsmas arhitektūra ļauj veikt materiāla pārnesi uz ražošanas plūsmu kopā ar atvilkumu Kanban uzdevumiem uzglabājamu un transportējamu materiālu apstrādes vienību izmēros. Izdotā materiāla vērtība tiek pievienota nepabeigta darba (NP) kontam, kas ir saistīts ar ražošanas plūsmu. Šī darbība līdzinās tam, kā tiek apstrādāts ražošanas pasūtījumam izsniegts materiāls. Tādu pašu principu var lietot precēm un nepabeigtām precēm. Ja vien šīs preces netiek izveidotas, pārsūtītas vai patērētas ražošanas plūsmā, krājumu transakcijas nav obligātas. Kad preces ir grāmatotas krājumos, ražošanas plūsmas NP konts tiek samazināts, atņemot saistītās standarta izmaksas.

## <a name="value-streams-and-value-stream-mapping"></a>Vērtību plūsmas un vērtību plūsmu kartēšana
Lean manufacturing arhitektūru iedvesmoja pieci racionāli principi, ko formulēja Womack un Jones: klientu vērtība, vērtību plūsma, kā arī plūsma, pieprasījumpiegāde un pilnība. Viena apstiprināta metode Lean manufacturing risinājumu ieviešanai ražošanas fiziskajā pasaulē ir vērtību plūsmas kartēšanu (value stream mapping — VSM). Šo metodi Rother un Shook ieviesa savā Lean Manufacturing institūta publikācijā “Mācīšanās redzēt” (“Learning to See”). 

Nākotnes stāvokļa vērtību plūsmu var modelēt kā ražošanas plūsmas versiju. Visi vērtību plūsmas procesi tiek modelēti kā procesu aktivitātes. Kustības vai pārsūtīšanas var modelēt kā pārsūtīšanas aktivitātes, ja pārsūtīšanas statusu ir nepieciešams reģistrēt vai ja ir nepieciešama integrēšana ar krājumu izdošanu vai konsolidētajiem sūtījumiem. 

Pati vērtību plūsma tiek modelēta kā pārvaldības struktūrvienība. Tāpēc vērtību plūsmu var izmantot kā finanšu dimensiju.

Papildinformāciju par pārvaldības struktūrvienībām skatiet šeit: [Pārvaldības struktūrvienības izveide](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md).

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>Lean manufacturing izmaksu aprēķināšana, pamatojoties uz ražošanas plūsmu
Ražošanas plūsmas izmaksu periodiskā konsolidēšana koriģē saistīto NP kontu un ļauj noteikt novirzes precēs, ko nodrošina ražošanas plūsma.

## <a name="continuous-improvement"></a>Nepārtraukta uzlabošana
Lai labāk atbalstītu nepārtrauktu uzlabošanu, ražošanas plūsma tiek ieviesta versijās ar minimālu laika patēriņu. Tāpēc pastāvošo ražošanas plūsmas versiju, kā arī visus saistītos Kanban nosacījumus var kopēt uz ražošanas plūsmas nākotnes versiju. Turklāt nākotnes stāvokļa ražošanas plūsmu var modelēt, pirms tā ir apstiprināta un aktivizēta ražošanai. Lai palīdzētu garantēt nemanāmu materiālu plūsmu pārejas datumā un vēlāk, esošie Kanban uzdevumi no vecajām ražošanas plūsmas versijām tiek automātiski saistīti ar jauno versiju.

## <a name="simplicity"></a>Vienkāršība
Lai ieviestu Lean Manufacturing, mēs izvēlējāmies ražošanas plūsmas un aktivitātes pieeju, kas sniedz iespēju modelēt vienkāršus un sarežģītus ražošanas scenārijus vienā mērogojamā arhitektūrā. Aktivitātes pieeja nodrošina vēl vienkāršāku procesu tiem lietotājiem, kuriem tas ir nepieciešams: ražotnē un loģistikas nodaļā nodarbinātajiem. Pretojoties uz aktivitātes balstītiem darbiem salīdzinot ar krājumu transakcijām, unificēts lietotāja interfeiss visiem lean manufacturing variantiem pārsūta biznesa sarežģītību no lietotāja interfeisa tur, kur tai jābūt: ražošanas plūsma kā lean manufacturing pamats.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]