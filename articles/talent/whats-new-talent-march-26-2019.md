---
title: Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 26. marts)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
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
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 568a16a17ed3269c7b72f27f0d4b7bbdbd56630e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518583"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-26-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 26. marts)

[!include [banner](includes/banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

### <a name="enhancements-to-interview-scheduling"></a>Uzlabojumi interviju plānošanā
Interviju plānošanā ir pieejami šādi uzlabojumi.

- Tagad darbinieku atlases speciālisti vai par pieņemšanu darbā atbildīgie vadītāji var manuāli aktivizēt atgādinājumu, ka intervētājam ir jāiesniedz savas atsauksmes. Var arī konfigurēt ar šo atgādinājumu saistīto e-pasta veidni.
- Kopīgojot intervijas kopsavilkumu ar kandidātu, intervētājs var izvēlēties slēpt intervētāju vārdus, kā arī var izvēlēties intervijas kopsavilkuma skatā slēpt kādas rindas.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

### <a name="embedded-images-in-activities"></a>Aktivitātēs iegultie attēli
Tagad attēlus varat iegult tieši aktivitātēs. Papildus iespējai kopēt un ielīmēt attēlus no tīmekļa, attēlus varat augšupielādēt arī no savas vietējās failu sistēmas. Aktivitātes lieluma ierobežojums ir 1 MB. Ja attēls ir pārāk liels, mainiet tā lielumu un mēģiniet augšupielādēt vēlreiz.

[![Kartēšana](./media/embedimages.png)](./media/embedimages.png)

Šajā laidienā ir ietverti nelieli programmas Dynamics 365 Talent: Onboard kļūdu labojumi.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR
**8.1.2210 būvējums**

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a>Pielāgotu lauku atbalsta pieejamība noteiktiem elementiem pakalpojumā Common Data Service 

Tālāk norādītie Common Data Service elementi tagad atbalsta klientu laikus, kas ir izveidoti programmā Dynamics 365 for Talent.

- Nodarbinātais
- Etniskā izcelsme
- Veterāna statuss
- Valodas kods
- Darbs
- Darba tips
- Darba funkcija
- Ieņemamais amats
- Amata veids
 
### <a name="employment-history-not-displayed-chronologically"></a>Nodarbinātības vēsture netiek rādīta hronoloģiskā secībā
Ar šīs izmaiņas ieviešanu nodarbinātības vēstures lapā nodarbinātības ieraksti tagad tiek rādīti hronoloģiskā secībā, neatkarīgi no uzņēmuma. Varat arī izmantot kārtošanas opcijas, lai kārtotu pēc uzņēmuma.

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a>Fiksētās atlīdzības plāni netiek rādīti, kad drošībā lietotājs tiek ierobežots pēc uzņēmuma.
Šajā laidienā fiksētās atlīdzības plāni tagad tiek rādīti, kad drošībā lietotāji tiek ierobežoti pēc uzņēmuma. Visi drošības iestatījumi tiek ievēroti, un fiksētie plāni tiek rādīti tiem uzņēmumiem, kuriem lietotājam ir atļauts piekļūt. 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a>Nevar dzēst darbu ierakstus, programmā Talent izmantojot opciju Atvērt programmā Excel
Līdz ar šī laidiena ieviešanu tagad varat noņemt darbu ierakstus, izmantojot opciju **Atvērt programmā Excel** programmā Dynamics 365 for Talent.

### <a name="upgrade-to-common-data-service"></a>Jaunināšana uz Common Data Service
Drīz būs pienācis termiņš jaunināšanai uz Common Data Service. Pierakstieties PowerApps administrēšanas centrā, lai noteiktu, vai jūsu datu bāzi ir nepieciešams jaunināt. Papildinformāciju par termiņiem un jaunināšanai nepieciešamajām darbībām skatiet rakstā [Jaunināšana uz Common Data Service](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>Priekšskatījumā

Informāciju par priekšskatījuma līdzekļu iespējošanas skatiet rakstā [Piekļuve priekšskatījuma līdzekļiem programmā Talent](./access-preview-feature.md).

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Atļaušana norādīt iemeslu kodus atvaļinājumu tipiem
Organizācijām, iespējams, ir nepieciešama papildinformācija saistībā ar brīvā laika pieprasījumiem. Lai iegūtu šo informāciju, darbiniekiem savos brīvā laika pieprasījumos ir jāiekļauj iemesla kods. Līdz ar šī laidiena ieviešanu tagad varat norādīt iemeslu kodus, kas ir saistīti ar noteiktu atvaļinājuma tipu, un sniegt iespēju darbiniekiem savos brīvā laika pieprasījumos atlasīt kādu iemesla kodu.

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a>Noteiktu atvaļinājumu tipu iesniegšanai nepieciešamo iemeslu kodu konfigurēšana
Organizācijām var būt nepieciešams iestatīt iemeslu kodus noteiktiem atvaļinājumu tipiem, kad darbinieki iesniedz brīvā laika pieprasījumu. Tas var būt nepieciešams, pamatojoties uz normatīvajām prasībām attiecīgajā valstī/reģionā vai uz uzņēmuma politiku. Šajā laidienā personāla vadībai ir dota iespēja norādīt, kuriem atvaļinājumu tipiem ir nepieciešams iemesla kods. Šī prasība ir jāievēro, kad darbinieki iesniedz brīvā laika pieprasījumus, kuriem atvaļinājumam ir nepieciešams iemesla kods.

## <a name="coming-soon"></a>Drīzumā

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Papildu atlīdzības drošība (fiksētā un mainīgā)
Daudzās organizācijās atlīdzību un atvieglojumu pārvaldnieki var piekļūt tikai noteiktiem atlīdzības ierakstiem. Piemēram, tie varētu būt par vadītājiem vai reģionālajiem darbiniekiem. Šīs izmaiņas dod iespēju personāla vadībai pārvaldīt un uzturēt atlīdzības plānus dažādām darbinieku grupām organizācijā. Fiksētajiem un mainīgajiem plāniem var piešķirt drošības lomas, kuras nosaka piekļuvi plāniem un ar šiem plāniem saistītajiem darbinieku datiem, piemēram, algu vai prēmiju ierakstiem. Atlīdzību šiem darbiniekiem var apstrādāt tikai lietotāji, kuriem ir piešķirtas lomas ar piekļuvi.

###  <a name="email-support-for-alerts"></a>E-pasta atbalsts brīdinājumiem
Līdz ar atjauninājuma Platform update 25 ieviešanu lietotāji var izveidot brīdinājumu kārtulas, kas automātiski izsūta e-pasta paziņojumus kontaktpersonām, ja kāds notikums tās aktivizē. 

### <a name="duplicate-employee-checks-user-interface-changes"></a>Dublētu darbinieku pārbaudes: lietotāja interfeisa izmaiņas
Līdz ar šīs izmaiņas ieviešanu dublikāti tiek noteikti, kad aizpildāt vārda/uzvārda/nosaukuma laukus, un statuss parāda atrasto dublikātu skaitu. Varat atlasīt norādīto saiti, lai atvērtu jaunu lapu, kur novērtēt, vai atrastā atbilstība ir jāizmanto. Lai izvairītos no datu ievades pārtraukšanas, dublikātu forma netiek atvērta automātiski.
