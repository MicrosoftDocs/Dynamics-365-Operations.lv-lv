---
title: Konfigurēt Azure Active Directory autentifikāciju, lai veiktu pierakstīšanos POS
description: Šajā tēmā skaidrots, kā Azure Active Directory pārdošanas punktā konfigurēt kā autentifikācijas metodi pakalpojumā Microsoft Dynamics 365 Commerce.
author: boycezhu
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 9dfb0389b0ca4b2cf75ccc70f35824674e618055
ms.sourcegitcommit: dca3279a8b7cd5d0bcd4e4a3aa9938b337aa8849
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/19/2021
ms.locfileid: "7402155"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a>Konfigurēt Azure Active Directory autentifikāciju, lai veiktu pierakstīšanos POS

[!include [banner](includes/banner.md)]

Šajā tēmā skaidrots, kā Azure Active Directory (Azure AD) pārdošanas punktā (point of sale - POS) konfigurēt kā autentifikācijas metodi pakalpojumā Microsoft Dynamics 365 Commerce.

Mazumtirgotāji, kas izmanto Dynamics 365 Commerce kopā ar citiem Microsoft mākoņa pakalpojumiem, piemēram, Microsoft Azure, Microsoft 365 un Microsoft Teams parasti vēlas izmantot Azure AD lietotāja akreditācijas datu centralizētai pārvaldībai, lai nodrošinātu drošu un netraucētu pierakstīšanos visās programmās. Lai izmantotu Azure AD autentifikāciju pakalpojumam Commerce POS, vispirms ir jākonfigurē Azure AD kā autentifikācijas metodi programmā Commerce Headquarters.

## <a name="configure-pos-authentication-method"></a>POS autentifikācijas metodes konfigurēšana

Lai konfigurētu POS autentifikācijas metodi programmā Commerce Headquarters, veiciet tālāk norādītās darbības.
    
1. Dodieties uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> POS iestatījumi \> POS profili \> Funkcionalitātes profili** un izvēlieties maināmo funkcionalitātes profilu.
1. Kopsavilkuma cilnes **Funkcijas** sadaļā **POS personāla pieteikšana** atlasiet nepieciešamo autentifikācijas metodes opciju no nolaižamā saraksta **Pieteikšanās autentifikācija**.

    Sarakstam **Pieteikšanās autentifikācijas metode** ir trīs opcijas:
    
    - **Personāla ID un parole** — šī noklusējuma opcija prasa POS lietotājiem ievadīt personāla ID un paroli, lai pieteiktos POS un piekļūtu vadītāja pārlabošanas funkcionalitātei.
    - **Azure AD bez vienas pierakstīšanās** - šī opcija prasa POS lietotājiem izmantot Azure AD akreditācijas datus, lai pieteiktos POS un piekļūt vadītāja pārlabošanas funkcionalitātei. Kad POS klients tiek atsvaidzināts vai no jauna atvērts, POS lietotājam ir jānodrošina Azure AD akreditācijas dati, lai pieteiktos vēlreiz.
    - **Azure AD ar vienu pierakstos** - ja ir atlasīta šī opcija, POS lietotāji var pieteikties Cloud POS (CPOS), izmantojot aktīvos Azure AD akreditācijas datus, ko izmanto citas tīmekļa programmas tajā pašā tīmekļa pārlūkprogrammā, vai pieteikties Modern POS (MPOS), izmantojot sistēmā Windows pieteiktos Azure AD akreditācijas datus. Abas metodes ļauj pierakstīties, bez nepieciešamības ievadīt Azure AD akreditācijas datus POS pierakstīšanās ekrānā. Tomēr, piekļūstot POS pārvaldnieka pārlabošanas funkcionalitātei, joprojām būs nepieciešama pierakstīšanās, izmantojot Azure AD akreditācijas datus.

1. Dodieties uz **Mazumtirdzniecība un komercija > Mazumtirdzniecība un komercija IT > Sadales grafiks** un palaidiet darbu **1070 (Kanāla konfigurācija)**, lai sinhronizētu visjaunākos funkcionalitātes profila iestatījumus POS klientiem.

> [!NOTE]
> - Pakalpojums **Azure AD bez vienas pierakstīšanās** autentifikācijas metodes opcija aizstāj opciju **Azure Active Directory** Commerce versijā 10.0.18 vai agrākajā.
> - Azure AD autentifikācijai ir nepieciešams aktīvs interneta savienojums, un, ja POS ir bezsaistē, šī autentifikācija nedarbosies.

## <a name="associate-azure-ad-accounts-with-pos-users"></a>Saistīt Azure AD kontus ar POS lietotājiem

Lai Azure AD izmantotu kā POS autentifikācijas metodi, sistēmā Commerce Headquarters ir jāsaista Azure AD konti ar POS lietotājiem. 

Lai programmā Commerce Headquarters saistītu Azure AD kontus ar POS lietotājiem, izpildiet šīs darbības.
    
1. Dodieties uz **Mazumtirdzniecība un komercija > Darbinieki > Nodarbinātie** un atveriet nodarbinātā ierakstu.
1. Darbību rūtī atlasiet cilni **Commerce** tad zem **Ārējā identitāte** atlasiet **Saistīt esošo identitāti**. 
1. Dialoglodziņā **Izmantot esošo ārējo identitāti** atlasiet opciju **Meklēt, izmantojot e-pastu**, ievadiet Azure AD e-pasta adresi un pēc tam atlasiet **Meklēt**.
1. Atlasiet Azure AD kontu, kas tiek atgriezts, pēc tam atlasiet **Labi**.

Pēc iepriekš minētajiem konfigurācijas darbībām, darbinieka detalizētas informācijas lapas cilnē **Commerce** tiks ievadīti lauki **Aizstājvārds**, **UPN** un **Ārējais apakšidentifikators**.

Lai sinhronizētu jaunāko POS lietotāju un Azure AD konta datus ar kanālu, jāpalaiž darbs **1060 (personāls)** sadaļā **Mazumtirdzniecība un komercija > Mazumtirdzniecība un komercija IT > Sadales grafiks**.

> [!NOTE]
> Pēc tam, kad programmā Commerce Headquarters tiek atjaunināta darbinieku informācija, piemēram, parole, POS atļauja, saistītais Azure AD konts vai darbinieku adrešu grāmata, ieteicams palaist darbu **1060 (personāls)**, lai sinhronizētu jaunāko darbinieka informāciju kanālā. POS klients pēc tam var iegūt pareizos datus lietotāja autentifikācijai un autorizācijas pārbaudēm.

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a>POS bloķēšanas reģistrs un pierakstīšanās ar Azure AD autentifikāciju

Šī problēma rodas, ja POS ir konfigurēts Azure AD autentifikācijas metodes izmantošanai:

- POS programmā nav pieejama funkcija **Reģistra bloķēšana**. 
- Funkcija **Automātiskā bloķēšana** darbojas tāpat kā funkcija **Automātiska atteikšanās**.
- Ja POS lietotājs atlasa **Atteikties**, lietotājam nākamajā POS palaišanas reizē ir jāpiesakās, izmantojot Azure AD akreditācijas datus neatkarīgi no tā, vai ir iespējota viena pierakstīšanās.

## <a name="manager-override-functionality-with-azure-ad-authentication"></a>Pārvaldnieka pārlabošanas funkcionalitāte ar Azure AD autentifikāciju

Kad POS ir konfigurēts izmantot Azure AD autentifikāciju, vadītāja pārlabošanas funkcionalitāte atvērs dialoglodziņu, kurā tiks parādīta uzvedne ar aicinājumu ievadīt vadītāja lietotāja Azure AD akreditācijas datus. Kad pārvaldnieka reģistrēšanās ir apstiprināta, vadītāja Azure AD akreditācijas dati tiks nomesti un iepriekšējā lietotāja Azure AD akreditācijas dati tiks izmantoti turpmākajām POS operācijām.

> [!NOTE]
> - Gan Commerce versijās 10.0.18, gan agrākās versijās vadītāja pārlabošanas funkcija neatbalsta Azure AD. Ir jānorāda personāla ID un parole, pat ja POS ir konfigurēta Azure AD autentifikācijas metodes izmantošanai.
> - Kad Jūs izmantojat CPOS ar Safari tīmekļa pārlūkprogrammu Apple iOS ierīcē, vispirms jāizslēdz **Bloķēt uznirstošos logus** Safari iestatījumos, lai vadītājs pārlabotu funkcionalitāti darbam ar Azure AD autentifikāciju. 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a>Drošības labākās prakses uz POS autentifikācijas balstītam Azure AD koplietotajās ierīcēs

Daudzi mazumtirgotāji iestata mazumtirdzniecības veikala vidi tā, lai vairākiem lietotājiem būtu piekļūšana POS programmai no koplietojamas fiziskas ierīces. Šajā kontekstā, lai gan viena pierakstīšanās nodrošina ērtu un vienlaidu autentifikācijas pieredzi, var arī izveidot drošības cilpu, kur pašreizējais POS lietotājs var nerealizēt, ka POS darbību vai operāciju veikšanai tiek izmantoti cita lietotāja akreditācijas dati. Pirms POS konfigurēšanas, lai lietotu Azure AD autentifikācijas metodi, ļoti ieteicams pārskatīt savu drošības politiku un koplietotās ierīces pierakstīšanās iestatījumus, lai izlemtu, kura opcija ir vislabāk piemērota.

- Ja mazumtirdzniecības vidē fiziskās ierīces pierakstīšanās kontam tiek izmantots koplietots konts (piemēram, lokāls konts), ieteicams izmantot opciju **Azure AD bez vienas pierakstīšanās**. Tas nodrošina, ka katrs POS lietotājs skaidri nodrošina Azure AD akreditācijas datus, lai pieteiktos POS.
- Ja mazumtirdzniecības vidē darbiniekiem ir jāizmanto savs Azure AD konts, lai pierakstītos POS un tās viesošanas fiziskajā ierīcē, ieteicams izmantot opciju **Azure AD ar vienu pierakstīšanu**.

## <a name="additional-resources"></a>Papildu resursi

[Nodarbinātā konfigurēšana](tasks/worker.md)

[Izveidot mazumtirdzniecības funkcionalitātes profilu](retail-functionality-profile.md)


[Paplašinātās pieteikšanās funkcionalitātes iestatīšana MPOS un Cloud POS](extended-logon.md)

[Labākās drošības prakses Cloud POS koplietotās vidēs](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
