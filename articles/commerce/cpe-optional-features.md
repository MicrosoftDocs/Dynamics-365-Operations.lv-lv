---
title: Izvēles funkciju konfigurēšana Dynamics 365 Commerce smilškastes videi
description: Šajā rakstā ir skaidrots, kā konfigurēt izvēles līdzekļus kastu Microsoft Dynamics 365 Commerce videi.
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4935f5f6ee17cba9c09eb79132119a7cbc08d9ad
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270360"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-sandbox-environment"></a>Izvēles funkciju konfigurēšana Dynamics 365 Commerce smilškastes videi

[!include [banner](includes/banner.md)]

Šajā rakstā ir skaidrots, kā konfigurēt izvēles līdzekļus kastu Microsoft Dynamics 365 Commerce videi.

## <a name="prerequisites"></a>Priekšnosacījumi

Ja vēlaties pazemināt darbību e-pasta līdzekļus, ir jāizpilda šādi priekšnosacījumi:

- Jums ir pieejams e-pasta serveris (vienkārša pasta pārsūtīšanas protokola \[SMTP\] serveris), Microsoft Azure ko var izmantot no abonementa, kur nodrošināti skārbas vidi.
- Jums ir pieejams pilnībā kvalificēts servera domēna nosaukums (FQDN)/IP adrese, SMTP porta numurs un autentifikācijas informācija.

## <a name="configure-the-image-back-end"></a>Attēla aizmugures konfigurēšana

### <a name="find-your-media-base-url"></a>Savas multivides bāzes URL atrašana

> [!NOTE]
> Lai varētu pabeigt šo procedūru, jums ir jāizpilda darbības, kas norādītas sadaļā [Savas vietnes iestatīšana pakalpojumā Commerce](cpe-post-provisioning.md#set-up-your-e-commerce-sites).

1. Piesakieties Commerce vietņu veidotājā, izmantojot URL vietrādi, kuru atzīmējāt, kad nodrošināšanas laikā inicializējāt e-komerciju (skatiet [e-komercijas inicializēšana](provisioning-guide.md#initialize-e-commerce)).
1. Atveriet **Fabrikam**, **Adventure Works** vai **Adventure Works biznesa** vietni, ar kuru vēlaties strādāt.
1. Kreisās puses izvēlnē atlasiet **Multivides bibliotēka**.
1. Atlasiet jebkuru atsevišķu attēla līdzekli.
1. Rekvizītu inspektors labajā pusē atrodiet rekvizītu **Publiskais URL**. Vērtība ir vietrādis URL. Tas ir piemērs:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.

1. Aizstājiet URL pēdējo identifikatoru (augstākminētajā URL piemērā —**MA1nQC** ) ar virkni **search?fileName=**. Tālāk parādīts, kā izskatās URL piemērs, kad šīs izmaiņas ir veiktas.

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    Šis vietrādis URL ir jūsu multivides bāzes vietrādis URL. Pierakstiet to.

### <a name="update-the-media-base-url"></a>Multivides bāzes URL atjaunināšana

1. Pieteikšanās Commerce Headquarters.
1. Izmantojiet izvēlni kreisajā pusē, lai dotos uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Kanālu iestatīšana \> Kanālu profili**.
1. Atlasiet **Rediģēt**.
1. Sadaļā **Profila rekvizīti** aizstājiet rekvizīta **Multivides servera bāzes URL** vērtību ar iepriekš izveidoto multivides bāzes URL.
1. Atlasiet kanālu ar nosaukumu **scXXXXXXXXX**.
1. Sadaļā **Profila rekvizīti** atlasiet **Pievienot**.
1. Rekvizītam, kas tika pievienots, atlasiet **Multivides servera bāzes URL** kā rekvizīta atslēgu. Kā rekvizīta vērtību ievadiet iepriekš izveidoto multivides bāzes vietrādi URL.
1. Atlasiet **Saglabāt**.

## <a name="configure-and-test-the-email-server"></a>E-pasta servera konfigurācija un testēšana

> [!NOTE]
> Šeit ievadītajam SMTP serverim vai e-pasta pakalpojumam jābūt pieejamam no Azure abonementa, kuru izmantojat videi.

1. Pieteikšanās Commerce Headquarters.
1. Izmantojiet izvēlni kreisajā pusē, lai dotos uz **Moduļi \> Retail un Commerce \> Headquarters iestatīšana \> Parametri \> E-pasta parametri**.
1. Cilnes **SMTP iestatījumi** laukā **Izejošā pasta serveris** ievadiet SMTP servera vai e-pasta pakalpojuma FQDN vai IP adresi.
1. Laukā **SMTP porta numurs** ievadiet porta numuru. (Ja neizmantojat drošligzdu slāņa \[SSL\], noklusējuma porta numurs ir **25**.)
1. Ja autentifikācija ir nepieciešama, ievadiet vērtības laukos **Lietotājvārds** un **Parole**.
1. Atlasiet **Saglabāt**.
1. Atlasiet **Atsvaidzināt**.
1. Cilnes **Testa e-pasts** laukā **E-pasta pakalpojumu sniedzējs** atlasiet **SMTP**.
1. Laukā **Nosūtīt uz** ievadiet e-pasta adresi, uz kuru jāpiegādā testa e-pasts.
1. Atlasiet **Sūtīt e-pasta ziņojumu.**

## <a name="configure-email-templates"></a>E-pasta veidņu konfigurēšana

Katram darījuma notikumam, kuram vēlaties sūtīt e-pasta ziņojumus, jums ir jāatjaunina e-pasta veidne ar derīgu sūtītāja e-pasta adresi.

1. Pieteikšanās Commerce Headquarters.
1. Izmantojiet izvēlni kreisajā pusē, lai dotos uz **Moduļi \> Retail un Commerce \> Headquarters iestatīšana \> Parametri \> Organizācijas e-pasta veidnes**.
1. Atlasiet **Rādīt sarakstu**.
1. Katrai veidnei sarakstā izpildiet tālākās transakcijas.

    1. Laukā **Sūtītāja e-pasta adrese** ievadiet sūtītāja e-pasta adresi.
    1. Neobligāti: laukā **Sūtītāja vārds** ievadiet nosaukumu, kas jāizmanto kā sūtītāja vārds.

1. Atlasiet **Saglabāt**.

## <a name="customize-email-templates"></a>E-pasta veidņu pielāgošana

Iespējams, vēlēsieties pielāgot e-pasta veidnes, lai tās izmantotu dažādus attēlus. Vai arī vēlaties atjaunināt veidnēs esošās saites, lai tās pārietu uz kases vides informāciju. Šī procedūra izskaidro, kā lejupielādēt noklusējuma veidnes, pielāgot tās un atjaunināt veidnes sistēmā.

1. Tīmekļa pārlūkprogrammā lejupielādējiet demonstrācijas noklusējuma e-pasta [Microsoft Dynamics 365 Commerce veidņu zip failu](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) lokālajā datorā. Šajā failā ir ietverti tālāk norādītie HTML dokumenti.

    - Pasūtījuma apstiprinājuma veidne
    - Dāvanu kartes izsniegšanas veidne
    - Jauna pasūtījuma veidne
    - Pasūtījuma iesaiņošanas veidne
    - Pasūtījuma saņemšanas veidne

1. Pielāgojiet veidnes, izmantojot teksta vai HTML redaktoru. Tālāk šajā rakstā [skatiet atbalstīto marķieru](#supported-tokens-in-the-email-template) sarakstu.
1. Pieteikšanās Commerce.
1. Izmantojiet izvēlni kreisajā pusē, lai dotos uz sadaļu **Moduļi \> Organizācijas administrācija \> Iestatījumi \> Organizācijas e-pasta veidnes**.
1. Paplašiniet sarakstu kreisajā pusē, lai redzētu visas veidnes.
1. Attiecībā uz katru veidni, kuru vēlaties pielāgot, veiciet tālāk norādītās darbības.

    1. Atlasiet sarakstā veidni.
    1. Sadaļā **E-pasta ziņojuma saturs** no saraksta atlasiet atbilstošo valodas versiju. (Noklusējuma valoda ir **en-us**.)
    1. Sadaļā **E-pasta** ziņojuma saturs atlasiet **Rediģēt**. Tiek parādīta rūts **Augšupielādēt e-pasta veidni**.
    1. Atlasiet **Pārlūkot** un atrodiet HTML failu, kurā ir pielāgots saturs.
    1. Atlasiet **Augšupielādēt**. Veidne tiek augšupielādēta sistēmā, un tiek parādīts priekšskatījums.
    1. Atlasiet **Labi**.
    1. Pēc izvēles: pielāgojiet veidnes rekvizītu **Temats**.
    1. Atlasiet **Saglabāt**.

### <a name="supported-tokens-in-the-email-template"></a>E-pasta veidnē atbalstītie marķieri

Kad e-pasts tiek atveidots, šie marķieri tiek aizstāti ar faktiskajām vērtībām, kas attiecas uz klientu un klienta pasūtījumu.

#### <a name="sales-order"></a>Pārdošanas pasūtījums

Tālāk minētie marķieri attiecas uz vispārēju pārdošanas pasūtījumu.

| Marķējuma nosaukums | Marķieris |
|-------------------|-------|
| Pasūtījuma numurs      | %salesid% |
| Klienta vārds/nosaukums   | %customername% |
| Piegādes adrese  | %deliveryaddress% |
| Norēķinu adrese   | %customeraddress% |
| Ordera datums        | %shipdate% |
| Piegādes veids     | %modeofdelivery% |
| Atlaide          | %discount% |
| PVN         | %tax% |
| Pasūtījuma kopsumma       | %total% |

#### <a name="sales-line"></a>Pārdošanas rinda

Tālāk esošie marķieri tiek aizstāti ar vērtībām katram produktam pasūtījumā.

> [!NOTE]
> Ievietojiet marķieri **Preču saraksts — sākums** HTML bloka sākumā, kas atkārtojas katram produktam, un marķieri **Preču saraksts — beigas** bloka beigās.

| Marķējuma nosaukums      | Marķieris |
|------------------------|-------|
| Preču saraksts — sākums   | \<!--%tablebegin.salesline% --\> |
| Preču saraksts — beigas     | \<!--%tableend.salesline%--\> |
| Preces nosaukums           | %lineproductname% |
| Apraksts            | %lineproductdescription% |
| Daudzums               | %linequantity% |
| Rindas vienības cena        | %lineprice% (pārbaudīt) |
| rindas preču kopsumma        | %linenetamount% |
| rindas atlaide          | %linediscount% |
| Nosūtīšanas datums              | %lineshipdate% |
| Iepirkuma metode     | %linedeliverymode% |
| piegādes adrese       | %linedeliveryaddress% |
| Rindas pārdošanas vienība | %lineunit% |

## <a name="additional-resources"></a>Papildu resursi

[Kases vides Dynamics 365 Commerce nodrošināšana](provisioning-guide.md)

[Konfigurēt kases Dynamics 365 Commerce vides](cpe-post-provisioning.md)

[Konfigurēt BTOPS kastēs Dynamics 365 Commerce](cpe-bopis.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portāls](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce tīmekļa vietne](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
