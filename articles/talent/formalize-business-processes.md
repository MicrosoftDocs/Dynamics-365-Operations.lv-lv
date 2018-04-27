---
title: "Biznesa procesu noformēšana"
description: "Izmantojot funkciju Biznesa process, var izveidot to procesu biznesa procesa veidni, kuri ir jāpabeidz jūsu organizācijā."
author: ShielaSogge
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1b50a97f5e2fc94255ff71702faf91ab36e68eb4
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="formalize-business-processes"></a>Biznesa procesu noformēšana
Izmantojot funkciju Biznesa process, var izveidot to procesu biznesa procesa veidni, kuri ir jāpabeidz jūsu organizācijā. Piemēram, jūsu uzņēmums var pabeigt personāla vadības auditu katru gadu. Veidni var izveidot, lai izsekotu visus auditā ietvertos uzdevumus, lai palīdzētu nodrošināt, ka, katru reizi pabeidzot procesu, visi uzdevumi ir izpildīti un, ja nepieciešams, lai palīdzētu nodrošināt, ka uzdevumi tiek izpildīti pareizā secībā. Regulāri veiktiem procesiem veidnes var izmantot vairākkārt vai tās var kopēt, lai izmantotu kā jaunas veidnes izmantošanas sākumpunktu.

Kad veidne ir izveidota, var sākt procesu, un to var izsekot darbvietā Biznesa process.  Uzsākto biznesa procesu, uzdevumi tiek piešķirti attiecīgajiem darbiniekiem, un tie ietver arī izpildes datumu. Šo komponentu sīks apraksts ir sniegts tālāk.

## <a name="business-process-template"></a>Biznesa procesa veidne
Biznesa procesa veidnē ir ietverta to uzdevumu grupa, kuri veido biznesa procesu. Cilvēkresursu nodaļas vadītāji un asistenti var izveidot noklusējuma biznesa procesu.  Tomēr to var mainīt drošības konfigurācijas sadaļā, rediģējot pienākumu Vispārējo biznesa procesu uzturēšana.

Katram procesam var definēt procesa īpašnieku. Procesa īpašnieks var redzēt visus procesa uzdevumus un var mainīt piešķirtos uzdevumus vai izpildes datumu.  Piemēram, Cilvēkresursu nodaļas direktors var izveidot veidni Biznesa process atvieglojumu pārskatīšanai.  Kā procesa īpašnieku var iestatīt Kompensāciju un atvieglojumu jautājumu nodaļas vadītāju, lai viņam ir pārskats par uzdevumiem, kas jāpabeidz pārskata ietvaros.  Procesa īpašnieks nevar izveidot vai dzēst aktīvo biznesa procesu vai biznesa procesa veidnes.

## <a name="task"></a>Uzdevums
Biznesa process bieži ietver vairākus uzdevumus. Dažus uzdevumus var pabeigt programmā Dynamics 365 for Talent, piemēram, iekšējā kursa piedāvājuma pārskatīšanu. Šajā gadījumā uzdevuma laukā Uzdevuma saite jāatlasa vienums Izvēlne. Citi uzdevumi var ietvert formu pārskatīšanu vai aizpildīšanu tīmekļa vietnē. Atlasot laukā Uzdevuma saite URL, var ievadīt tīmekļa vietnes adresi. Šajā laukā var ievadīt gan ārējās, gan iekšējās saites URL. Var izveidot arī manuāli izpildāmu darbību uzdevumus, piemēram, visu struktūras pieejamības pārskatīšana. Šajā gadījumā uzdevuma saite nav nepieciešama. Šī elastība ļauj izsekot visaptveroša procesa dažāda veida uzdevumus.

Uzdevumu var piešķirt konkrētam darbiniekam vai pozīcijai. Piemēram, Kompensāciju un atvieglojumu jautājumu nodaļas vadītājs vienmēr ir persona, kas veic apdrošināšanas prēmiju pārskatīšanu.   Izveidojot šo uzdevumu, atlasiet veidu Amats uzdevuma piešķiršanai un pēc tam sarakstā Amats atlasiet Kompensāciju un atvieglojumu jautājumu nodaļas vadītājs. Kad process tiek sākts, uzdevums tiek piešķirts darbiniekam, kas ieņem Kompensāciju un atvieglojumu jautājumu nodaļas vadītāja amatu. Uzdevumu var piešķirt arī konkrētam darbiniekam, atlasot lauku Darbinieks, kas atbilst uzdevuma piešķiršanas tipam, un pēc tam atlasot attiecīgo personu.

Uzdevumu izpildes datumi ir atkarīgi no laukā Mērķa datums ievadītās vērtības procesa sākumā. Daži uzdevumi ir jāpabeidz pirms mērķa datums, un dažus uzdevumus var pabeigt pēc mērķa datums.  Definējot uzdevumu, tiek ievadīts izpildes datums, kas ir saistīts ar mērķa datumu laukā Izpildes datuma nobīde no mērķa datuma. Piemēram, pieņemsim, ka Kompensāciju un atvieglojumu jautājumu nodaļas vadītājam jāsagatavo pārskats par apdrošināšanas prēmijām 10 dienas pirms cilvēkresursu audita pabeigšanas. Izveidotajā uzdevumā ir norādīts ar mērķa datumu -10 dienas saistīts izpildes datums. Tādējādi, ja šis process tiek sākts 13. maijā, uzdevuma izpildes datums ir 3. maijs. Piezīme. Izpildes datumus var arī pielāgot, kad process ir jau uzsākts.

Sarežģītiem uzdevumiem var būt nepieciešamas vairākas darbības vai var būt nepieciešama konkrēta persona, kas izpilda uzdevumus, lai iegūtu sīkāku informāciju. Uzdevumam var pievienot norādījumus un var arī iekļaut norādījumiem paredzētu bagātinātā teksta formatēšanu. Norādījumi var ietvert sīkāku informāciju personai, kurai piešķirta uzdevuma izpilde, par to, kā to izpildīt.

## <a name="starting-a-process"></a>Procesa sākšana
Lai sāktu procesu, veidnē Biznesa process atlasiet opciju Sākt procesu.  Kad process ir uzsākts, uzdevumi tiek izveidoti atlasītajiem darbiniekiem un/vai amatiem, kuri ir noteikti veidnē Biznesa process ietvertajiem uzdevumiem. Pievienojot vai atņemot nobīdes dienu skaitu no mērķa datuma, visiem uzdevumiem tiek piešķirts izpildes datums (skatiet informāciju par nobīdes dienu skaitu sadaļā “Uzdevums”). Aktīvo biznesa procesu var skatīt darbvietā Biznesa process. 

## <a name="employee-self-service"></a>Darbinieku pašapkalpošanās
Ja darbiniekam ir piešķirts uzdevums, viņam piešķirtos uzdevumus var skatīt lapā Darbinieku patstāvīgi izmantojamais pakalpojums. Darbinieki, kuriem ir piešķirts biznesa procesa uzdevums, savā lapā Darbinieku patstāvīgi izmantojamais pakalpojums var redzēt uzdevumu, tā aprakstu, norādījumus par tā izpildi, kā arī kontaktpersonas vārdu un uzvārdu, un viņi var atvērt saistīto Dynamics365 lapu vai tīmekļa vietnes lapu. Uzdevumus var atzīmēt ar statusu Procesā, Atcelts vai Pabeigts.

## <a name="business-process-workspace"></a>Darbvieta Biznesa process
Cilvēkresursu jautājumu speciālisti aktīvo biznesa procesu var skatīt darbvietā Biznesa process. Darbvietā ir norādīti visi aktīvie procesi un ar katru no tiem saistītie uzdevumi. Vispusīgu uzdevumu sarakstu var filtrēt pēc izpildes datuma. Lapā ir norādīti nokavētie uzdevumi un īpaši cilvēkresursu jautājumu speciālistam piešķirtie uzdevumi. Viņi var arī atjaunināt visu uzdevumu statusu un, ja nepieciešams, mainīt piešķirtos uzdevumus, lai nodrošinātu vispārējā biznesa procesa izpildi.

## <a name="my-business-processes-workspace"></a>Darbvieta Mani biznesa procesi
Izmantojot darbvietu Mani biznesa procesi, procesu īpašnieki var skatīt viņiem piešķirtos aktīvos biznesa procesus. Darbvietā ir norādīti visi īpašnieka aktīvie procesi un saistītie uzdevumi.  Vispusīgu uzdevumu sarakstu var filtrēt pēc izpildes datuma. Lapā ir arī norādīti īpaši procesa īpašniekam piešķirtie uzdevumi. Procesa īpašnieks var arī atjaunināt visu uzdevumu statusu, kā arī mainīt jebkuru piešķirto uzdevumu.

## <a name="navigating-business-processes"></a>Pārvietošanās biznesa procesos
1. Lai pievienotu veidni Biznesa process, dodieties uz sadaļu Biznesa procesi — saites — Biznesa procesu administrēšana.
   - a.   Izmantojot opciju Jauns, tiek izveidota jauna veidne.
   - b.   Izmantojot opciju Kopēt no veidnes, atlasītā veidne tiek iekopēta jaunā veidnē.
   - c.   Izmantojot opciju Sākt procesu, tiek sākts atlasītais biznesa process, tiek piešķirti uzdevumi un aprēķināts izpildes datums.  
2. Lai skatītu aktīvos procesus un saistītos uzdevumus, dodieties uz darbvietu Biznesa procesi.

