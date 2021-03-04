---
title: Jaunumi vai izmaiņas risinājumā Dynamics 365 Talent (2019. gada 23. aprīlis)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/23/2019
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
ms.search.validFrom: 2019-04-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 53faf972759c8f770017fcd3a87920410988e626
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527191"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-23-2019"></a>Jaunumi vai izmaiņas risinājumā Dynamics 365 Talent (2019. gada 23. aprīlis)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract
Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard
Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR
Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2253. Numuri iekavās attiecas uz atbalsta numuriem portālā Lifecycle Services (LCS).

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service elementu atbalsts pielāgotajiem laukiem
Līdz ar šīs nedēļas laidienu pielāgotus laukus atbalsta šādi elementi: Atlīdzības līmenis, Atvieglojumu opcijas, Prasmju tips un Atlīdzības reģions.

### <a name="additional-odata-entities-302992"></a>Papildu OData elementi (302992)
Tagad pakalpojumā OData tiek atbalstīti šādi elementi: Nodarbinātā profesionālā pieredze un Nodarbinātā izglītība.
   
### <a name="performance-journal-attachments-for-managers-and-employees-308248"></a>Veiktspējas žurnālu pielikumi vadītājiem un darbiniekiem (308248)
Līdz ar šo laidienu pielikumi tagad ir pieejami gan vadītājiem, gan darbiniekiem, veidojot un atjauninot veiktspējas žurnāla ierakstus.

### <a name="employee-rehire-flag-always-available-310047"></a>Darbinieka atkārtotas pieņemšanas karodziņš vienmēr pieejams (310047)
Darbinieku atkārtotas pieņemšanas opcija tagad ir pieejama atjaunināšanai ārpus izbeigšanas procesa. 

### <a name="cannot-change-the-name-of-my-payment-method-308815"></a>Nevar mainīt etiķetes **Mana maksājumu metode** nosaukumu (308815)
Ir iespējota personalizācija, lai etiķeti **Mana maksājumu metode** varētu mainīt sadaļā Darbinieku pašapkalpošanās.

### <a name="financial-dimensions-against-a-position-cant-be-deleted-293908"></a>Finanšu dimensijas pret pozīciju nevar dzēst (293908)
Finanšu dimensijas tagad var noņemt, kad tiek pieprasītas izmaiņas esošajā pozīcijā un finanšu dimensijas robežās visā uzņēmumā. 

### <a name="customer-is-unable-to-publish-back-data-into-talent-when-opening-the-data-from-excel-302955"></a>Klients nevar publicēt datus atpakaļ programmā Talent, atverot datus programmā Excel (302955)
Šīs izmaiņas labo publicēšanas problēmu, kas rodas, izmantojot saistītās tabulas.

## <a name="in-preview"></a>Priekšskatījumā

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Atļaušana norādīt iemeslu kodus atvaļinājumu tipiem
Organizācijām, iespējams, ir nepieciešama papildinformācija par brīvā laika pieprasījumiem. Tagad atvaļinājumu tipiem varat norādīt iemeslu kodus un ļaut darbiniekiem savos brīvā laika pieprasījumos atlasīt iemesla kodu.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Iemeslu kodu pieprasīšana noteiktiem atvaļinājumu tipiem brīvā laika pieprasījumos
Organizācijām var būt nepieciešami iemeslu kodi noteiktiem atvaļinājumu tipiem, kad darbinieki iesniedz brīvā laika pieprasījumu. Tas varētu būt saistīts ar uzņēmuma politiku vai normatīvajām prasībām. Tagad varat norādīt, kuriem atvaļinājumu tipiem ir nepieciešams iemesla kods, un varat pieprasīt, lai darbinieki savos brīvā laika pieprasījumos atvaļinājuma tipam norādītu iemesla kodu.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Atvaļinājumu un kavējumu transakciju sarakstu nodrošināšana personāla vadībai
Darbinieku brīvā laika izsekošana un saprašana, kā tiek aprēķināts brīvais laiks, ne tikai palīdz personāla vadībai atbildēt uz darbinieku jautājumiem, bet arī nodrošina darbiniekiem precīzas brīvā laika piemaksas. Personāla vadībai tagad ir jauns skats uz transakcijām (dotācijām, uzkrājumiem, korekcijām un pieprasījumiem), lai redzētu bilanču aprēķinu ietekmējošos faktorus.

## <a name="coming-soon"></a>Drīzumā

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Lietotāja interfeisa uzlabojumi dublētu darbinieku pārbaudei
Līdz ar šīs izmaiņas ieviešanu dublikāti tiek noteikti, kad aizpildāt vārda/uzvārda/nosaukuma laukus, un statuss parāda atrasto dublikātu skaitu. Varat atlasīt norādīto saiti, lai atvērtu jaunu lapu, kur novērtēt, vai atrastā atbilstība ir jāizmanto. Lai izvairītos no datu ievades pārtraukšanas, dublikātu forma netiek atvērta automātiski.
## <a name="known-issues"></a>Zināmās problēmas

### <a name="email-support-for-alerts"></a>E-pasta atbalsts brīdinājumiem
Līdz ar platformas atjauninājumu 26 Finance and Operations ieviešanu lietotāji var izveidot brīdinājumu kārtulas, kas automātiski sūta e-pasta paziņojumus kontaktpersonām, ja kāds notikums tās aktivizē.


[!INCLUDE[footer-include](../includes/footer-banner.md)]