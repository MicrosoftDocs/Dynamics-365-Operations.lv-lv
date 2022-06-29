---
title: Konfigurēt BTOPS kastēs Dynamics 365 Commerce
description: Šajā rakstā ir skaidrots, kā konfigurēt pirkšanu tiešsaistē, saņemt veikalā (BIOS) Microsoft Dynamics 365 Commerce kases vidē pēc tās nodrošināšanas.
author: BrianShook
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 16cea7beb6ca05b5e96a9713b1217b414e27d56e
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013179"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-sandbox-environment"></a>Konfigurēt BTOPS kastēs Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Šajā rakstā ir skaidrots, kā pēc vides nodrošināšanas konfigurēt pirkšanu tiešsaistē, savākšanu veikalā (BIOS) Microsoft Dynamics 365 Commerce kases vidē.

## <a name="prerequisite"></a>Priekšnoteikumi

Veiciet šajā rakstā sniegtās procedūras tikai pēc tam, kad Commerce kastu vide ir nodrošināta un konfigurēta. Papildinformāciju par to, kā nodrošināt un konfigurēt vidi, [skatiet sadaļu Kases Dynamics 365 Commerce vides nodrošināšana](provisioning-guide.md) un [kases Dynamics 365 Commerce vides konfigurēšana](./cpe-post-provisioning.md).

Pēc tam, kad commercea vide ir nodrošināta un konfigurēta līdz beigām, varat izmantot šo rakstu, lai iespējotu B IZAS scenārijus.

## <a name="configure-the-pos"></a>POS konfigurēšana

### <a name="configure-modern-pos"></a>Modern POS konfigurēšana

BOPIS scenārijiem, kas ietver kredītkartes maksājumu, ir nepieciešama aparatūras stacija. Aparatūras stacija ir iebūvēta Modern POS operētājsistēmas Windows un Android klientiem. Ja izmantojat mākoni POS vai Modern POS sistēmai iOS, pārdošanas punkts (POS) klientam ir jāsavieno pārī ar koplietojamo aparatūras staciju. Šajā rakstā skaidrots, kā konfigurēt BTOPS Windows un Android klientiem. Papildinformāciju par to, kā uzstādīt koplietojamo aparatūras staciju, skatiet [Retail aparatūras stacijas konfigurēšana un instalēšana](./retail-hardware-station-configuration-installation.md).

1. Dodieties uz **Mazumtirdzniecība un Komercija \> Kanāla iestatīšana \> POS iestatīšana \> Reģistri**.
2. Atlasiet reģistru **SANFRAN-5** un pēc tam atlasiet **Rediģēt**.
3. Mainiet **Aparatūras profila** lauka vērtību no **HW002** uz **HW001** un pēc tam atlasiet **Saglabāt**.
4. Lai sinhronizētu izmaiņās, dodieties uz **Mazumtirdzniecība un Komercija \> Mazumtirdzniecības un Komercijas IT \> Sadales grafiks**.
5. Atlasiet sadales grafiku **1090** un pēc tam Darbību rūtī atlasiet **Palaist tagad**.
6. Atlasiet **Jā** un pēc tam **Labi**, lai uzsāktu datu sinhronizāciju. 

### <a name="install-modern-pos"></a>Instalēt Modern POS

1. Dodieties uz **Mazumtirdzniecība un Komercija \> Kanāla iestatīšana \> POS iestatīšana \> Ierīces**.
2. Atlasiet ierīci **SANFRANCIS-5**.
3. Darbību rūtī atlasiet **Lejupielādēt** un pēc tam atlasiet **Konfigurācijas fails**.
4. Atlasiet **Lejupielādēt** un pēc tam atlasiet **Retail Modern POS**. 
5. Kad **ModernPOSSetup.exe** faila lejupielāde ir pabeigta, atlasiet **Atvērt failu**.

    ![Atvērt failu.](./dev-itpro/media/PAYMENTS/openfile.png)

6. Atlasiet **Tālāk**, lai varētu iziet caur instalēšanas procesam. Kad instalēšana ir pabeigta, atlasiet **Aizvērt**.

### <a name="activate-modern-pos"></a>Aktivizēt Modern POS

1. Windows darbvirsmā atlasiet pogu **Sākums** un ievadiet **Retail Modern POS**.
2. Atlasiet **Retail Modern POS** programmu, lai iniciētu aktivizāciju.
3. Atlasiet **Nākamais**. **Servera URL**, **Ierīces ID** un **Reģistra numuru** lauki ir jāiestata, izmantojot informāciju no konfigurācijas faila, ko lejupielādējāt iepriekšējā procedūrā.
4. Atlasiet **Aktivizēt**.
5. Tiek parādīts autentifikācijas dialoglodziņš. Atlasiet kontu, kas izmanto e-pasta adresi, kas iepriekš bija saistīta ar darbinieku **000713 - Andrew Collette**.

    > [!NOTE]
    > Ja vēl neesat saistījis darbinieku ar savu identitāti, aktivizēšana nebūs veiksmīga. Šajā gadījumā veiciet darbības, kas sadaļā Saistīt darbinieku ar savu identitāti, [kas atrodas kas atrodas lodziņos Kastes Dynamics 365 Commerce vides konfigurēšana](cpe-post-provisioning.md#associate-a-worker-with-your-identity).
    
6. Kad tiek parādīta uzvedne ar aicinājumu ļaut organizācijai pārvaldīt ierīci, atlasiet **Tikai šo programmu**.
7. Kad aktivizēšana ir pabeigta, atlasiet **Sākt darbu**.

### <a name="enable-bopis-in-modern-pos"></a>Iespējot BOPIS Modern POS

1. Piesakieties Modern POS, izmantojot **000713** kā operatora ID un **123** kā paroli.
2. Kamēr tiek demonstrēts ievada video, atzīmējiet abas izvēles rūtiņas dialoglodziņa apakšējā kreisajā stūrī un pēc tam aizveriet dialoglodziņu.
3. Ja netiek parādīta uzvedne, lai aizvērtu maiņu, ritiniet pa labi **Sveiciena** lapā, atlasiet **Aizvērt maiņu** un pēc tam piesakieties POS.
4. Pēc tam, kad esat pieteicies, saņemot aicinājumu, atlasiet **Veikt neapstrādātu operāciju**.
5. **Sveiciena** lapā ritiniet pa labi un atlasiet darbību **Atlasīt aparatūras staciju**.
6. Atlasiet **Pārvaldīt**, iestatiet opciju **Izmantot aparatūras staciju** uz **Ieslēgts** un pēc tam atlasiet **Labi**.
7. Izrakstieties no POS un pēc tam pierakstieties tajā atkal.
8. Kad esat pieteicies, atlasiet **Atvērt jaunu maiņu** un pēc tam atlasiet **Atvilktne**.

## <a name="complete-a-bopis-scenario"></a>Pabeigt BOPIS scenāriju

### <a name="create-a-storefront-order-for-in-store-pickup"></a>Izveidot veikala pasūtījumu savākšanai veikalā

1. Dodieties uz vietrādi URL, kas norādīts, [Inicializēt e-Commerce](./provisioning-guide.md#initialize-e-commerce) darbībā vides konfigurācijas laikā.
2. Atlasiet krājumu un izvēlieties **Pievienot grozam**.
3. Iepirkumu groza lapā atlasiet opciju **Paņemt šo** pasūtījuma rindai, kuru tikko pievienojāt.
4. Dialoglodziņā **Atlasīt veikalu** ievadiet **Sanfrancisko** un pēc tam atlasiet pogu **Meklēt**.
5. Rezultātu sarakstā atrodiet Sanfrancisko veikalu un atlasiet **Saņemt šeit**.
6. Iepirkumu groza lapā atlasiet **Norēķināties kā viesim**. 

    > [!NOTE]
    > Lai turpinātu norēķināšanos, ir jāpiekrīt sīkfailu paziņojumam. Šis paziņojums tiek parādīts kā reklāmkarogs norēķinu lapas augšpusē.

7. Kredītkartes maksājuma metodei ievadiet šādu informāciju:

    - **Kartes īpašnieka vārds:** ievadiet jebkādu vārdu.
    - **Kartes numurs:** ievadiet **4111-1111-1111-1111**.
    - **Derīguma termiņa datums:** ievadiet **10/20**.
    - **Kartes verificēšanas vērtības (CVV) kods:** ievadiet **737**.

    > [!IMPORTANT]
    > Pārbaudes vietnē nekādā gadījumā nemēģiniet izmantot īstas kredītkartes informāciju.

8. Turpiniet norēķināšanos, ievadot detalizētu informāciju par rēķina adresi, un pēc tam atlasiet **Saglabāt un turpināt**.
9. Kad pasūtījums ir gatavs, atlasiet **Norēķināties**.

### <a name="synchronize-online-orders-to-the-back-office"></a>Sinhronizēt tiešsaistes pasūtījumus uz atbalsta biroju

Lai iegūtu informāciju par to, kā sinhronizēt tiešsaistes pasūtījumus, skatiet [Tiešsaistes pārdošanas un maksājumu grāmatošana](./tasks/posting-online-sales-payments.md).

### <a name="pick-up-an-order-in-the-store"></a>Pasūtīšana tiešsaistē un saņemšana veikalā

1. Pierakstieties pārdošanas punktā (POS).
2. **Sveiciena** ekrānā atlasiet **Pasūtījuma izpilde**
3. Saņemšanai paredzēto krājumu sarakstā atlasiet rindu no pasūtījuma, kas tika ievietots tiešsaistē.
4. Kad ir atlasīta pasūtījuma rinda, atlasiet **Saņemt**.

    Rindas vienums tiek pievienots darbības ekrānam, un **$0,00** tiek rādīta kā maksājamā bilance.

5. Izvēlieties atlikumu **$0,00**, vai atlasiet jebkuru maksāšanas metodi, lai noslēgtu transakciju.

## <a name="troubleshooting"></a>Problēmu novēršana

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a>POS izveidotajiem tiešsaistes pasūtījumiem nav nulles bilances

Kad pasūtījums ir iegūts saņemšanai veikalā, ja atlikums nav 0 (nulle), pārliecinieties, ka Modern POS tiek izmantots un ka aparatūras stacija ir aktīva. Ja tiek izmantota sistēma Mākonis POS vai Modern POS operētājsistēmai iOS, pārliecinieties, ka koplietojamā aparatūras stacija ir aktīva. Lai izgūtu maksājumus, kas veikti tiešsaistē, ir nepieciešama kāda aktīva aparatūras stacijas forma.

### <a name="general-issues-with-payment-capture"></a>Galvenās problēmas ar maksājuma tveršanu

Par visiem vispārējiem jautājumiem kā pirmo darbību vienmēr ir jākonsultējas ar Modern POS vai interneta informācijas pakalpojumu (IIS) aparatūras stacijas notikumu žurnāliem. Šos žurnālus var atrast šādos mezglos Windows notikumu žurnālā:

- Programmu un pakalpojumu žurnāli \> Microsoft \> Dynamics \> Commerce-ModernPOS
- Programmu un pakalpojumu žurnāli \> Microsoft \> Dynamics \> Commerce-Hardware Station

## <a name="additional-resources"></a>Papildu resursi

[Kases vides Dynamics 365 Commerce nodrošināšana](provisioning-guide.md)

[Konfigurēt kases vides neobligātos Dynamics 365 Commerce līdzekļus](cpe-optional-features.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portāls](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce tīmekļa vietne](https://aka.ms/Dynamics365CommerceWebsite)

[Adyen maksājumu savienotājs](./dev-itpro/adyen-connector.md?tabs=8-1-3)

[Tiešsaistes maksājumu instrumentu saglabāšana, izmantojot savienotāju Adyen](./dev-itpro/adyen-connector-listpi.md)

[Pārskats par Omni kanāla maksājumiem](./omni-channel-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
