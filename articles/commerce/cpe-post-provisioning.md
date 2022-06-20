---
title: Dynamics 365 Commerce novērtēšanas vides konfigurēšana
description: Šajā rakstā ir izskaidrots, kā Microsoft Dynamics 365 Commerce konfigurēt novērtēšanas vidi pēc tās nodrošinājuma.
author: psimolin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 19d88139e35554bce68bc6203141957b96e439a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892334"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>Dynamics 365 Commerce novērtēšanas vides konfigurēšana

[!include [banner](includes/banner.md)]

Šajā rakstā ir izskaidrots, kā Microsoft Dynamics 365 Commerce konfigurēt novērtēšanas vidi pēc tās nodrošinājuma.

Veiciet šajā rakstā sniegtās procedūras tikai pēc tam, kad ir nodrošināta Commerce novērtēšanas vide. Informāciju par to, kā nodrošināt Commerce novērtējuma vidi, skatiet [Commerce novērtējuma vides nodrošināšana](provisioning-guide.md).

Kad jūsu Commerce novērtējuma vide ir pilnībā nodrošināta, ir jāpabeidz papildu pēc nodrošināšanas konfigurācijas darbības, pirms var sākt novērtēt vidi. Lai veiktu šīs darbības, ir jāizmanto Microsoft Dynamics Lifecycle Services (LCS) un Dynamics 365 Commerce.

## <a name="before-you-start"></a>Pirms darba sākšanas

1. Pierakstieties [LCS portālā](https://lcs.dynamics.com).
1. Dodieties uz savu projektu.
1. Augšējā izvēlnē atlasiet **Mākoņvides**.
1. No saraksta atlasiet savu vidi.
1. Vides informācijas labajā pusē atlasiet **Pieteikties vidē**. Jūs tiksiet nosūtīts uz Commerce galveno biroju.
1. Pārliecinieties, ka ir atlasīta **USRT** juridiskā persona (augšējā labajā stūrī).
1. Dodieties uz **commerce parametru \> konfigurācijas** parametriem un nodrošiniet, ka parametram ProductSearch.UseAzureSearch **ir ievadīts** ieraksts un vai vērtība ir iestatīta kā **patiesa**. Ja šī ieraksta nav, to **·** **\>** var pievienot, iestatīt vērtību kā patiesu un pēc tam atlasīt Kanāla datu bāzes pilnu datu sinhronizāciju commerce Scale vienībai, kas ir saistīta ar jūsu e-commerce vietni.
1. Pārejiet uz **retail and Commerce \> Headquarters iestatīšanas \> Commerce plānotāju \> Inicializējiet Commerce plānotāju**. **Izvēlnē Inicializēt Commerce Scheduler** izniršanas izvēlni iestatiet opciju **Dzēst esošo** konfigurāciju **kā** Jā un pēc tam atlasiet **Labi**.
1. Lai Commerce Scale Unit pievienotu kanālus, **dodieties uz mazumtirdzniecības un Commerce \> Headquarters \> iestatīšanas Commerce plānotāja \>** kanāla datu bāzi un pēc tam kreisajā rūtī atlasiet Commerce Scale Unit. Kopsavilkuma cilnē **Mazumtirdzniecības** kanāls pievienojiet **AW** tiešsaistes veikalu, **AW biznesa tiešsaistes** **veikalu un Fabrikam paplašinātos tiešsaistes veikala kanālus**. Pēc izvēles varat arī pievienot mazumtirdzniecības veikalus, ja izmantosit POS (piemēram, Sietlā, **·** **San Arko** un **San Arko).**

Pēc nodrošināšanas darbību laikā Commerce Headquarters, pārliecinieties, ka **USRT** juridiskā persona vienmēr ir atlasīta.

## <a name="configure-the-point-of-sale"></a>Pārdošanas punkta konfigurācija

### <a name="associate-a-worker-with-your-identity"></a>Nodarbinātā saistīšana ar jūsu identitāti

Lai saistītu darbinieku ar jūsu identitāti, veiciet Commerce Headquarters norādītās darbības.

1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi \> Mazumtirdzniecība un komercija \> Darbinieki \> Nodarbinātie**.
1. Sarakstā atrodiet un atlasiet šādu ierakstu **000713 – Endrjū Kollete**.
1. Darbību rūtī atlasiet **Commerce**.
1. Atlasiet **Piesaistīt esošu identitāti**.
1. Laukā **E-pasts** (pa labi no **Meklēt, izmantojot e-pastu**) ievadiet savu e-pasta adresi.
1. Atlasiet **Meklēt**.
1. Atlasiet ierakstu ar savu vārdu.
1. Atlasiet **Labi**.
1. Atlasiet **Saglabāt**.

### <a name="activate-cloud-pos"></a>mākoņa POS aktivizēšana;

Lai aktivizētu mākoņa POS, veiciet LCS norādītās darbības.

1. Augšējā izvēlnē atlasiet **Mākoņvides**.
1. No saraksta atlasiet savu vidi.
1. Vides informācijas labajā pusē atlasiet **Pieteikties mākoņa pārdošanas punktā**.
1. Atlasiet **Tālāk**, lai atvērtu dialoglodziņu **Pirms darba sākšanas**.
1. Atstājiet lauku **Servera URL**, kā tas ir. Atlasiet **Nākamais**.
1. Piesakieties, izmantojot savu Microsoft Azure Active Directory (Azure AD) kontu.
1. Sadaļā **Veikala nosaukums** atlasiet **Sanfrancisko** un pēc tam atlasiet **Tālāk**.
1. Sadaļā **Reģistrs un ierīce** atlasiet **SANFRAN-1**.
1. Atlasiet **Aktivizēt**. Jūs esat izrakstījies un aizvirzīts uz POS pierakstīšanās lapu.
1. Tagad varat pieteikties mākoņa POS pieredzei, izmantojot operatora ID **000713** un paroli **123**.

## <a name="set-up-your-site-in-commerce"></a>Iestatiet savu vietni pakalpojumā Commerce.

Lai sāktu iestatīt novērtējuma vietni pakalpojumā Commerce, veiciet tālāk norādītās darbības.

1. Piesakieties vietņu veidotājā, izmantojot URL vietrādi, kuru atzīmējāt, kad nodrošināšanas laikā inicializējāt e-komerciju (skatiet [e-komercijas inicializēšana](provisioning-guide.md#initialize-e-commerce)).
1. Atlasiet vietni **Fabrikam**, lai atvērtu vietnes iestatīšanas dialoglodziņu.
1. Atlasiet domēnu, kuru ievadījāt, kad inicializējat e-Commerce.
1. Kā noklusējuma kanālu atlasiet **Fabrikam paplašinātais tiešsaistes veikals**. (Pārliecinieties, ka atlasāt **paplašināto** tiešsaistes veikalu.)
1. Ka noklusējuma valodu atlasiet **en-us**.
1. Atstājiet lauka **Path** vērtību tādu, kāda tā ir.
1. Atlasiet **Labi**. Tiek parādīts vietnes lapu saraksts.
1. Atkārtojiet soļus 2-7 **AdventureWorks** vietai (kas kartē uz AW tiešsaistes **veikala kanālu)** **AdventureWorks un biznesa vietni (kas tiek kartēta uz AW biznesa tiešsaistes veikala** kanālu).**·** **Ja Fabrikam** vietas ceļš ir tukšs AdventureWorks, ir jāpievieno ceļi divām vietām (piemēram, "aw" un "awbusiness").

## <a name="enable-jobs"></a>Darbu iespējošana

Lai iespējotu darbus pakalpojumā Commerce, izpildiet tālāk aprakstītās darbības.

1. Pierakstieties vidē (HQ).
1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Mazumtirdzniecība un komercija \> Pieprasījumi un pārskati \> Pakešuzdevumi**.

    Šīs procedūras atlikušie soļi jāaizpilda katram no šiem darbiem:

    * Apstrādāt mazumtirdzniecības pasūtījuma e-pasta paziņojumu
    * Preču pieejamība
    * P-0001
    * Darbs Sinhronizēt pasūtījumus

1. Izmantojiet ātro filtru, lai meklētu darbu pēc nosaukuma.
1. Ja darba statuss ir **Izpilda**, veiciet tālāk norādītās darbības:

    1. Atlasiet ierakstu.
    1. Darbību rūtī noklikšķiniet uz cilnes **Pakešuzdevums**, pēc tam atlasiet **Mainīt statusu**.
    1. Atlasiet **Atcelt** un pēc tam atlasiet **Labi**.

1. Ja darba statuss ir ieturēts **, sekojiet** šiem soļiem:

    1. Atlasiet ierakstu.
    1. Darbību rūtī noklikšķiniet uz cilnes **Pakešuzdevums**, pēc tam atlasiet **Mainīt statusu**.
    1. Atlasiet **Gaida** un pēc tam atlasiet **Labi**.

Pēc izvēles var arī iestatīt atkārtošanās intervālu uz vienu (1) minūti šādiem darbiem:

* Apstrādāt mazumtirdzniecības pasūtījuma e-pasta paziņojuma darbu
* P-0001 darbs
* Darbs Sinhronizēt pasūtījumus

### <a name="run-full-data-synchronization"></a>Izpildīt pilnīgu datu sinhronizāciju

Lai pakalpojumā Commerce palaistu pilnu datu sinhronizāciju, veiciet Commerce Headquarters norādītās darbības.

1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi \> Mazumtirdzniecība un komercija \> Mazumtirdzniecības uzstādīšana \> Komercijas plānotājs \> Kanāla datubāze**.
1. Atlasiet kanālu ar nosaukumu **scXXXXXXXXX**.
1. Darbību rūtī atlasiet **Pilnīga datu sinhronizācija**.
1. Ievadiet **9999** kā sadales grafiku.
1. Atlasiet **Labi**.
1. Atlasiet **Labi**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Kredītkartes informācijas pārbaude, lai veiktu pārbaudes pirkumus

Lai vietnē veiktu pārbaudes transakcijas, varat izmantot tālāk minēto pārbaudes kredītkartes informāciju.

- **Kartes numurs:** 4111-1111-1111-1111
- **Beigu datums:** 10/30
- **Kartes verificēšanas vērtības (CVV) kods:** 737

> [!IMPORTANT]
> Pārbaudes vietnē nekādā gadījumā nemēģiniet izmantot īstas kredītkartes informāciju.

## <a name="next-steps"></a>Nākamās darbības

Kad nodrošināšanas un konfigurēšanas darbības ir pabeigtas, varat sākt izmantot novērtējuma vidi. Izmantojiet Commerce vietnes veidotāja URL, lai dotos uz autorēšanas pieredzi. Izmantojiet Commerce vietnes URL, lai dotos uz mazumtirdzniecības klienta vietnes pieredzi.

Lai konfigurētu neobligātos līdzekļus savai Commerce novērtējuma videi, skatiet [Commerce novērtējuma vides neobligāto līdzekļu konfigurācija](cpe-optional-features.md).

> [!NOTE]
> Commerce novērtēšanas vidēs ir iepriekš ielādēts Azure Active Directory (Azure AD) “no uzņēmuma patērētājam” (Business-to-Consumer — B2C) nomnieks demonstrācijas nolūkiem. Paša Azure AD B2C nomnieka konfigurēšana nav nepieciešama novērtēšanas vidēm. Tomēr, ja jūs konfigurējat novērtēšanas vidi, lai izmantotu savu Azure AD B2C nomnieku, lūdzu, pievienojiet ``https://login.commerce.dynamics.com/_msdyn365/authresp`` kā atbildes URL Azure AD B2C programmā, izmantojot Azure portālu.

## <a name="troubleshooting"></a>Problēmu novēršana

### <a name="site-builder-channel-list-is-empty-when-configuring-site"></a>Vietas veidotāja kanālu saraksts ir tukšs, konfigurējot vietu

Ja vietas veidotājs nerāda nevienu tiešsaistes veikala kanālu, galvenajā birojā nodrošiniet, lai kanāli tiktu pievienoti Commerce Scale Unit [saskaņā](#before-you-start) ar aprakstu iepriekš sadaļā Pirms sākšanas. Palaidiet arī commerce **Scheduler**, lai dzēstu esošo **konfigurācijas vērtību, kas** iestatīta uz **Jā**.  Kad šie soļi ir pabeigti, **Kanāla** datu bāzes lapā (**Retail un Commerce \> Headquarters \> iestatīšanas Commerce plānotāja \>** kanāla datu bāze) **izpildiet 9999**. darbu Commerce Scale Unit.

### <a name="color-swatches-are-not-rendering-on-the-category-page-but-are-rendering-on-the-product-details-page-pdp-page"></a>Krāsu aizstāsumi kategoriju lapā netiek renderti, bet tiek renderti preces informācijas lapas (PDP) lapā.

Ievērojiet šos soļus, lai nodrošinātu, ka krāsa un izmērs ir iestatīti uz uzdefinējamiem.

1. Galvenajā birojā dodieties uz sadaļu **Mazumtirdzniecības un Commerce \>\> kanāla iestatīšanas kanāla kategorijas un preces īpašības**.
1. Kreisajā rūtī atlasiet tiešsaistes veikala kanālu un pēc tam atlasiet Iestatīt **atribūta metadatus**.
1. Kanāla opcijai **Rādīt atribūtu** iestatiet vērtību **Jā**, iestatiet opciju **Var precizēt uz** Jā **un** pēc tam atlasiet **Saglabāt**. 
1. Atgriezieties tiešsaistes veikala kanāla lapā un pēc tam atlasiet Publicēt **kanāla atjauninājumus**.
1. Dodieties uz **mazumtirdzniecības un Commerce \> Headquarters iestatīšanas \> Commerce plānotāja \> kanāla** **datu bāzi un izpildiet 9999** . darbu commerce Scale Unit.

### <a name="business-features-dont-appear-to-be-turned-on-for-the-adventureworks-business-site"></a>Biznesa vietnei nav ieslēgti biznesa AdventureWorks līdzekļi.

Galvenajā birojā nodrošiniet, lai tiešsaistes veikala kanāls tiktu konfigurēts ar debitora veidu, kas **iestatīts** uz **B2B**. **Ja debitora veids** ir iestatīts **uz B2C**, ir jāizveido jauns kanāls, jo esošo kanālu nevar rediģēt. 

Demonstrācijas dati tika nosūtīti Commerce versijā 10.0.26 un agrāk **, kad AW Business tiešsaistes** veikala kanāls tika konfigurēts nepareizi. Risinājums ir izveidot jaunu kanālu ar tādiem **pašiem** iestatījumiem un konfigurācijām, izņemot debitora veidu, **kas jāiestata uz B2B**.

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 Commerce novērtējuma vides pārskats](cpe-overview.md)

[Nodrošināt Dynamics 365 Commerce novērtējuma vidi](provisioning-guide.md)

[Izvēles funkciju konfigurācija Dynamics 365 Commerce novērtējuma videi](cpe-optional-features.md)

[BOPIS konfigurācija Dynamics 365 Commerce novērtējuma videi](cpe-bopis.md)

[Dynamics 365 Commerce novērtējuma vide - bieži uzdotie jautājumi](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portāls](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce tīmekļa vietne](https://aka.ms/Dynamics365CommerceWebsite)

[B2C nomnieka iestatīšana programmā Commerce](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
