---
title: Jaunumi vai izmaiņas risinājumā Dynamics 365 Talent (2019. gada 30. aprīlis)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 38c30a878ada9ed0b63ade3d0f234aeffce0ad12
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897893"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-30-2019"></a>Jaunumi vai izmaiņas risinājumā Dynamics 365 Talent (2019. gada 30. aprīlis)

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2270. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).

### <a name="provide-feedback"></a>Sniegt atsauksmes

Atsauksmju sniegšanas opcija programmā Talent ir izvēlnē **Palīdzība** (**?**). Šajā izvēlnē ir nodrošināta piekļuve tālāk minētajiem resursiem.

- Dati
- Palīdzība
- Darba sākšana
- Atbalsts
- Idejas
- Par

### <a name="improvements-to-the-user-interface-for-duplicate-employee-detection"></a>Lietotāja interfeisa uzlabojumi dublētu darbinieku noteikšanai

Šo izmaiņu dēļ dublikāti tagad tiek noteikti, kad tiek iestatīti nosaukumu lauki, un statusa indikators rāda noteikto dublikātu skaitu. Norādītā saite atver lapu, kur varat novērtēt, vai ir jāizmanto viens no dublikātiem. Lai izvairītos no datu ievades pārtraukšanas, dublikātu lapa netiek atvērta automātiski. Lai atvērtu lapu, ir jāatlasa saite.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service elementu atbalsts pielāgotajiem laukiem

Šīs nedēļas laidienā tālāk minētie elementi atbalsta pielāgotus laukus: Nodarbinātība, Atvieglojumu tips un Apmaksas cikls.

### <a name="an-error-occurs-when-an-off-boarding-checklist-is-assigned-299877"></a>Rodas kļūda, kad tiek piešķirts darba pārtraukšanas kontrolsaraksts (299877)

Šīs izmaiņas labo kļūdas ziņojumu, kas parādās, kad piešķirat darbiniekam darba pārtraukšanas kontrolsarakstu ārpus darba attiecību pārtraukšanas procesa.

### <a name="the-exited-workers-link-opens-the-wrong-worker-309939"></a>Aizgājušo nodarbināto saite atver neatbilstošu nodarbināto (309939)

Šīs izmaiņas labo problēmu, kas rodas, kad atkārtoti pieņemat darbā darbinieku no citas juridiskas personas un mēģināt pāriet pie darbinieka no aizgājušo nodarbināto saraksta.

### <a name="the-employee-self-service-compensation-card-doesnt-show-summary-values-when-advanced-security-is-turned-on-315231"></a>Darbinieku pašapkalpošanās sadaļas atlīdzības kartītē netiek rādītas kopsavilkuma vērtības, ja ir ieslēgta papildu drošība (315231)

Šīs izmaiņas labo problēmu, kas rodas, lietojot papildu atlīdzības drošību. Kad papildu drošība ir ieslēgta, darbinieku pašapkalpošanās sadaļā tiek rādītas gan darbinieku, gan vadītāju kopējās atlīdzības summas. Pirms šīm izmaiņām kopsavilkuma vērtības tika parādītas kā 0 (nulle).

### <a name="if-a-position-without-a-title-is-created-in-common-data-service-no-position-is-created-in-talent-314562"></a>Ja pakalpojumā Common Data Service tiek izveidots amats bez nosaukuma, programmā Talent netiek izveidots amats (314562)

Šīs nedēļas izmaiņas labo problēmu, kas rodas, ja izveidojat amatus pakalpojumā Common Data Service, bet nenorādāt nosaukumu.

### <a name="error-message-in-performance-journal-entries-in-employee-self-service-314134"></a>Kļūdas ziņojums veiktspējas žurnāla ierakstos darbinieku pašapkalpošanās sadaļā (314134)

Šīs izmaiņas labo problēmu, kas rodas, pievienojot veiktspējas mērķus veiktspējas žurnāla ierakstiem darbinieku pašapkalpošanās sadaļā.

## <a name="in-preview"></a>Priekšskatījumā

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Atļaušana norādīt iemeslu kodus atvaļinājumu tipiem

Organizācijām, iespējams, ir nepieciešama papildinformācija par brīvā laika pieprasījumiem. Tagad atvaļinājumu tipiem varat norādīt iemeslu kodus un ļaut darbiniekiem savos brīvā laika pieprasījumos atlasīt iemesla kodu.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Iemeslu kodu pieprasīšana noteiktiem atvaļinājumu tipiem brīvā laika pieprasījumos

Organizācijām var būt nepieciešami iemeslu kodi noteiktiem atvaļinājumu tipiem, kad darbinieki iesniedz brīvā laika pieprasījumu. Šī prasība var pastāvēt uzņēmuma politikas vai reglamentējošo prasību dēļ. Tagad varat norādīt, kuriem atvaļinājumu tipiem ir nepieciešams iemesla kods, un varat pieprasīt, lai darbinieki savos brīvā laika pieprasījumos atvaļinājuma tipam norādītu iemesla kodu.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Atvaļinājumu un kavējumu transakciju sarakstu nodrošināšana personāla vadībai

Iespēja izsekot darbinieku brīvajam laikam un saprast, kā tiek aprēķināts brīvais laiks, ne tikai palīdz personāla vadībai (Human Resources — HR) atbildēt uz darbinieku jautājumiem, bet arī nodrošina darbiniekiem precīzas brīvā laika piemaksas. Personāla vadībai tagad ir jauns skats uz transakcijām (dotācijām, uzkrājumiem, korekcijām un pieprasījumiem), lai personāla vadības darbinieki redzētu bilanču aprēķinu ietekmējošos faktorus.

## <a name="coming-soon"></a>Drīzumā

### <a name="email-support-for-alerts"></a>E-pasta atbalsts brīdinājumiem

Finance and Operations atjauninājumā Platform update 26 lietotāji var izveidot brīdinājumu kārtulas, kas automātiski sūta e-pasta paziņojumus kontaktpersonām, ja kāds notikums tās aktivizē.
