---
title: Biznesa procesu formalizēšana
description: Šajā tēmā ir paskaidrots, kā, izmantojot funkciju Biznesa process, var izveidot to procesu biznesa procesa veidni, kuri ir jāpabeidz jūsu organizācijā.
author: ShielaSogge
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: ShielaS
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.openlocfilehash: fd538677d897c1e7d3103cd714c688373aab8d29
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "305375"
---
# <a name="formalize-business-processes"></a>Biznesa procesu formalizēšana

[!include[banner](includes/banner.md)]

Izmantojot funkciju Biznesa process, var izveidot to to biznesa procesu veidni, kuri ir jāpabeidz jūsu organizācijā. Piemēram, katru gadu jūsu uzņēmums veic cilvēkresursu auditu. Šajā gadījumā varat izveidot veidni, kas izseko visus uzdevumus, kas iekļauti auditā. Šī veidne nodrošinās to, ka visi uzdevumi, kas tikuši veikti katru reizi, kad tiek veikts audita. Turklāt, ja uzdevumi jāizpilda noteiktā secībā, veidne nodrošināt to, ka tie tiek veikti pareizā secībā.

Veidnes var atkārtoti izmantot periodiskajiem procesiem. Tās arī var apvienot un izmantot kā sākuma punktu, lai izveidotu jaunas veidnes.

Kad biznesa procesa veidne ir izveidota, var sākt biznesa procesu, un to var izsekot darbvietā **Biznesa process**. Uzsākto biznesa procesu, uzdevumi tiek piešķirti attiecīgajiem darbiniekiem, un tie ietver arī izpildes datumu.

## <a name="business-process-templates"></a>Biznesa procesa veidnes
Biznesa procesa veidnē ir ietverta to uzdevumu grupa, kuri veido biznesa procesu. Pēc noklusējuma cilvēkresursu nodaļas vadītāji un asistenti var izveidot biznesa procesu. Tomēr lomas, kas var izveidot biznesa procesus, var mainīt, modificējot drošības konfigurācijas pienākumu **Uztur vispārīgos biznesa procesus**.

Katram biznesa procesam var definēt procesa īpašnieku. Procesa īpašnieks varēs redzēt visus procesa uzdevumus un var mainīt piešķirtos uzdevumus vai izpildes datumu. Piemēram, cilvēkresursu nodaļas direktors var izveidot veidni Biznesa process atvieglojumu pārskatīšanai un kā procesa īpašnieku norādīt Atlīdzību un atvieglojumu vadītājs. Pēc tam atlīdzību un atvieglojumu vadītājs var redzēt uzdevumus, kas jāveic pārskatīšanas ietvaros.

Procesa īpašnieks nevar izveidot jaunus biznesa procesus vai biznesa procesu veidnes vai dzēst aktīvos biznesa procesus vai biznesa procesu veidnes.

## <a name="tasks"></a>Uzdevumi
Biznesa process bieži ietver vairākus uzdevumus. Dažus uzdevumus, piemēram, iekšējā kursa piedāvājuma pārskatīšanu, var izpildīt programmā Microsoft Dynamics 365 for Talent[?]. Šajā gadījumā opcija ir atlasīta laukā **Uzdevuma saite**. Citi uzdevumi var ietvert lapu pārskatīšanu vai aizpildīšanu tīmekļa vietnē. Šajā gadījumā **vietrādis URL** tiek atlasīts laukā **Uzdevuma saite**​. Tādā gadījumā var ievadīt tīmekļa vietnes adresi. Var ievadīt gan ārējās, gan iekšējās saites URL. Var izveidot arī manuāli izpildāmu darbību uzdevumus, piemēram, visu struktūras pieejamības pārskatīšana. Šajā gadījumā uzdevuma saite nav nepieciešama. Šī elastība ļauj izsekot visaptveroša procesa dažāda veida uzdevumus.

Uzdevumu var piešķirt konkrētam darbiniekam vai pozīcijai. Piemēram, Kompensāciju un atvieglojumu jautājumu nodaļas vadītājs vienmēr ir persona, kas veic apdrošināšanas prēmiju pārskatīšanu. Tādēļ, izveidojot šo uzdevumu, atlasiet **Amats** laukā **Piešķires tips** un pēc tam atlasiet **Atlīdzību un atvieglojumu vadītājs** sarakstā **Amats**. Kad biznesa process tiek sākts, uzdevums tiek piešķirts darbiniekam, kas ieņem amatu **Atlīdzību un atvieglojumu vadītājs**. Lai uzdevumu piešķirtu konkrētam darbiniekam, atlasiet **Darbinieks** laukā **Piešķires tips** un pēc tam atlasiet attiecīgo personu.

Uzdevumu izpildes datumi ir atkarīgi no lauka mērķa datuma, kas ievadīts biznesa procesa sākumā. Daži uzdevumi ir jāveic pirms mērķa datuma, bet citus var veikt pēc mērķa datuma. Definējot uzdevumu, laukā **Izpildes datuma nobīde no mērķa datuma** norādiet izpildes datumu, kas ir saistīts ar mērķa datumu. Piemēram, atlīdzību un atvieglojumu vadītājam ir jāsagatavo pārskats par apdrošināšanas prēmijām 10 dienas pirms cilvēkresursu audita pabeigšanas. Šādā gadījumā uzdevums, kas ir jāizveido pārskatam, ir **Izpildes datuma nobīde no mērķa datuma** ar vērtību **–10**. Tādējādi, ja šis biznesa process tiek sākts 13. maijā, uzdevuma izpildes datums ir 3. maijs.

> [!NOTE]
> Izpildes datumus var arī pielāgot, kad biznesa process ir jau uzsākts.

Sarežģītiem uzdevumiem var būt nepieciešamas vairākas darbības vai personai, kas izpilda uzdevumus, ir jāsniedz papildinformācija. Minētajos scenārijos uzdevumam var pievienot norādījumus. Norādījumi var ietvert sīkāku informāciju personai, kurai piešķirta uzdevuma izpilde, par to, kā to izpildīt. Norādījumos var pat iekļaut bagātinātā teksta formātu.

## <a name="starting-a-business-process"></a>Biznesa procesa sākšana
Biznesa procesa veidnē biznesa procesu varat sākt, atlasot **Sākt procesu**. Kad process ir sākts, uzdevumi ir izveidoti atlasītajiem darbiniekiem un/vai amatiem, kuri ir definēti veidnē iekļautajiem uzdevumiem. Pievienojot vai atņemot nobīdes dienu skaitu no mērķa datuma, visiem uzdevumiem tiek piešķirts izpildes datums, kā paskaidrots sadaļā“Uzdevumi”. Aktīvo biznesa procesu var skatīt darbvietā **Biznesa procesi**.

## <a name="employee-self-service"></a>Darbinieku pašapkalpošanās
Kad uzdevums ir piešķirts darbiniekam, šo uzdevumu un visus citus piešķirtos uzdevumus darbinieks var skatīt lapā **Darbinieku patstāvīgi izmantojamais pakalpojums**. Katram biznesa procesa uzdevumam, kas darbiniekam tiek piešķirts, darbinieks var redzēt uzdevuma nosaukumu un aprakstu, norādījumus par tā izpildi un kontaktpersonas vārdu. Lapā **Darbinieku patstāvīgi izmantojamais pakalpojums** darbinieks var atvērt arī saistīto Microsoft Dynamics 365 lapu vai saistīto tīmekļa lapu un atzīmēt uzdevumus kā izpildes procesā, atceltus vai pabeigtus.

## <a name="business-process-workspace"></a>Darbvieta Biznesa process
Cilvēkresursu jautājumu speciālisti aktīvo biznesa procesu var skatīt darbvietā **Biznesa process**. Darbvietā ir norādīti visi aktīvie procesi un ar katru no tiem saistītie uzdevumi. Vispusīgu uzdevumu sarakstu var filtrēt pēc izpildes datuma. Darbvietā ir norādīti nokavētie uzdevumi un īpaši cilvēkresursu jautājumu speciālistam piešķirtie uzdevumi. Cilvēkresursu jautājumu speciālisti var arī atjaunināt visu uzdevumu statusu un, ja nepieciešams, mainīt piešķirtos uzdevumus, lai nodrošinātu vispārējā biznesa procesa izpildi.

## <a name="my-business-processes-workspace"></a>Darbvieta Mani biznesa procesi
Izmantojot darbvietu **Mani biznesa procesi**, procesu īpašnieki var skatīt viņiem piešķirtos aktīvos biznesa procesus. Šajā darbvietā ir norādīti visi īpašnieka aktīvie procesi un saistītie uzdevumi. Vispusīgu uzdevumu sarakstu var filtrēt pēc izpildes datuma. Darbvietā ir norādīti arī īpaši procesa īpašniekam piešķirtie uzdevumi. Procesa īpašnieks var arī atjaunināt visu uzdevumu statusu, kā arī mainīt jebkuru piešķirto uzdevumu.

## <a name="navigating-business-processes"></a>Pārvietošanās biznesa procesos
Lai izveidotu vai kopētu biznesa procesu veidni vai sāktu biznesa procesu, pārejiet uz lapu Biznesa procesi — Saites — Biznesa procesu administrēšana. Varat veikt šādas darbības:

- lai izveidotu jaunu biznesa procesa veidni, atlasiet **Jauns**;
- lai kopētu atlasīto veidni jaunā veidnē, atlasiet **Kopēt no veidnes**;
- lai sāktu atlasīto biznesa procesu, piešķirtu uzdevumus un aprēķinātu izpildes datumus, atlasiet **Sākt procesu**;

lai skatītu aktīvos procesus un saistītos uzdevumus, atveriet darbvietu **Biznesa procesi**.

