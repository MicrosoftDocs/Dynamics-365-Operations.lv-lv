---
title: Darba sākšana ar elektroniskās rēķinu izveides servisa administrēšanu
description: Šajā tēmā ir paskaidrots, kā sākt darbu ar Elektronisko rēķinu izrakstīšanu.
author: gionoder
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f77c8fd1696b74f852d04cc0a696d4816ef9af1f
ms.sourcegitcommit: 5033d42a2aac852916d726e40bd98a164d1a837d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/23/2022
ms.locfileid: "7984832"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>Darba sākšana ar elektroniskās rēķinu izveides servisa administrēšanu

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms pabeidzat šajā tēmā norādītās procedūras, ir jāievieš šādi priekšnosacījumi:

- Jums ir jābūt piekļuvei jūsu Microsoft Dynamics Lifecycle Services (LCS) kontam.
- Jums ir jābūt LCS projektam ar Microsoft Dynamics 365 Finance vai Dynamics 365 Supply Chain Management 10.0.17. vai jaunāku versiju. Turklāt šīs programmas ir jāizvieto vienā no tālāk minētajām Azure ģeogrāfiskām vietām:

    - ASV
    - Eiropa
    - Apvienotā Karaliste
    - Āzija

- Jums ir jābūt piekļuvei jūsu Dynamics 365 Regulatory Configuration Services (RCS) kontam.
- Jums jāaktivizē Globalizācijas līdzeklis jūsu RCS kontā Līdzekļu pārvaldībā. Papildinformāciju skatiet sadaļā [Regulatory Configuration Services (RCS) — Globalizācijas līdzekļi](rcs-globalization-feature.md).
- Jums jāizveido galvenā glabātuve un krātuves kontu risinājumā Azure. Papildinformāciju skatiet šeit: [Azure krātuves konta un galvenās glabātavas izveide](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Instalējiet programmu Microservices pievienojumprogrammu pakalpojumam Lifecycle Services

1. Pierakstieties jūsu LCS kontā un LCS informācijas panelī, atlasiet LCS projektu.
2. Projekta informācijas panelī **Vides** atlasiet izvietoto vidi. atlasītājai videi jābūt palaistai.
3. Cilnes **Power Platform integrācija** lauku grupā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.
4. Atlasiet **Elektronisko rēķinu izrakstīšana**.
5. Laukā **AAD pieteikuma ID** ievadiet **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Šī ir fiksēta vērtība.
6. Laukā **AAD nomnieka ID** ievadiet jūsu Azure abonementa konta nomnieka ID. Azure Active Directory (Azure AD) nomniekam, kuru norādāt, jābūt tam pašam nomniekam, kas tiek izmantots RCS.
7. Pārskatiet noteikumus un nosacījumus un atzīmējiet izvēles rūtiņu.
8. Atlasiet **Instalēt**. Instalēšana var ilgt vairākas minūtes.


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Iestatiet RCS integrācijas parametrus ar elektronisko rēķinu izrakstīšanu

1. Piesakieties savā RCS kontā.
2. **Globalizācijas līdzekļu** darbtelpas sadaļā **Saistītie iestatījumi** atlasiet **Elektroniskās ziņošanas parametri**.
3. Cilnes **Elektroniskā rēķinu izrakstīšana** laukā **Apkalpošanas galapunkta URI** ievadiet jūsu Azure ģeogrāfijai atbilstošo servisa galapunktu, kā parādīts tabulā tālāk.

    | Datacenter Azure ģeogrāfija | Pakalpojuma galapunkta URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | ASV              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Eiropa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Apvienotā Karaliste             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Āzija                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. Pārbaudiet, vai lauks **Lietojumprogrammas ID** ir iestatīts uz **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Šī vērtība ir fiksēta vērtība.
5. Laukā **LCS vides ID** ievadiet jūsu LCS vides ID.
6. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

## <a name="create-key-vault-references"></a>Atslēgas akreditācijas datu komplekta atsauksmju veidošana

1. Piesakieties savā RCS kontā.
2. Darbvietā **Globalizācijas līdzeklis** sadaļā **Vide** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
3. Lapas **Vides iestatījumi** darbību rūtī atlasiet **Servisa vides** un pēc tam atlasiet **Key Vault parametri**.
4. Atlasiet **Jauns**, lai izveidotu atslēgas glabātuves atsauci.
5. Laukā **Nosaukums** ievadiet atslēgas glabātuves atsauces nosaukumu. Ievadiet aprakstu laukā **Apraksts**.
6. Laukā **Atslēgas glabātuves URI** ielīmējiet atslēgas glabātuves noslēpumu no Azure atslēgas glabātuves. Papildinformāciju skatiet šeit: [Azure krātuves konta un galvenās glabātavas izveide](e-invoicing-create-azure-storage-account-key-vault.md).
7. Atlasiet **Saglabāt**.

## <a name="create-storage-account-secret"></a>Izveidojiet krātuves noslēpumu

1. Lapā **Vides iestatījumi** darbības rūtī atlasiet **Pakalpojuma vide** > **Atslēgas glabātuves parametri**.
2. Atlasiet **Atslēgas glabātuves atsauce** un sadaļā **Sertifikāti** atlasiet **Pievienot**.
3. Laukā **Nosaukums** ievadiet glabātuves konta noslēpuma nosaukumu. Papildinformāciju skatiet šeit: [Azure krātuves konta un galvenās glabātavas izveide](e-invoicing-create-azure-storage-account-key-vault.md).
4. Ievadiet aprakstu laukā **Apraksts**.
5. Laukā **Tips** atlasiet **Noslēpums**.
6. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

## <a name="create-a-digital-certificate-secret"></a>Ciparsertifikātu noslēpuma izveide

1. Lapas **Vides iestatījumi** darbību rūtī atlasiet **Servisa vide** un pēc tam atlasiet **Key Vault parametri**.
2. Atlasiet **Atslēgas glabātuves atsauce** un tad sadaļā **Sertifikāti** atlasiet **Pievienot**.
3. Laukā **Nosaukums** ievadiet ciparsertifikāta noslēpuma nosaukumu. Papildinformāciju skatiet šeit: [Azure krātuves konta un galvenās glabātavas izveide](e-invoicing-create-azure-storage-account-key-vault.md).
4. Ievadiet aprakstu laukā **Apraksts**.
5. Laukā **Tips** atlasiet **Sertifikāts**.
6. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

## <a name="create-a-service-environment"></a>Pakalpojumu vides izveide

1. Piesakieties savā RCS kontā.
2. Darbvietā **Globalizācijas līdzeklis** sadaļā **Vide** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
3. Lapā **Vides iestatījumi** darbību rūtī atlasiet **Pakalpojuma vide**.
4. Atlasiet **Jauns**, lai izveidotu jaunu pakalpojuma vidi.
5. Laukā **Nosaukums** ievadiet e-rēķinu izrakstīšanas vides nosaukumu. Ievadiet aprakstu laukā **Apraksts**.
6. Laukā **Krātuves SAS marķiera noslēpums** atlasiet tā krātuves konta noslēpuma nosaukumu, kas jāizmanto, lai autentificētu piekļuvi krātuves kontam.
7. Sadaļā **Lietotāji** atlasiet **Pievienot**, lai pievienotu lietotāju, kuram ir atļauts iesniegt elektroniskos rēķinus, izmantojot vidi, un arī pievienojieties krātuves kontam.
8. Laukā **Lietotāja ID** ievadiet lietotāja aizstājvārdu. Laukā **E-pasta adrese** ievadiet lietotāja e-pasta adresi.
9. Atlasiet **Saglabāt**.
10. Ja jūsu valstij/reģionam raksturīgiem rēķiniem ir nepieciešama sertifikātu ķēde, lai pielietotu elektroniskos parakstus, Darbības rūtī atlasiet **Atslēgas glabātuves parametrus** pēc tam atlasiet **Sertifikātu ķēde** un sekojiet šīm darbībām:

    1. Atlasiet **Jauns**, lai izveidotu sertifikātu ķēdi.
    2. Laukā **Nosaukums** ievadiet sertifikātu ķēdes nosaukumu. Ievadiet aprakstu laukā **Apraksts**.
    3. Sadaļā **Sertifikāti** atlasiet **Pievienot**, lai pievienotu ķēdei sertifikātu.
    4. Izmantojiet pogu **Augšā** vai **Lejā**, lai mainītu sertifikāta pozīciju ķēdē.
    5. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.
    6. Aizvērt lapu.

11. Darbības rūtī lapā **Pakalpojuma vide** atlasiet **Publicēt**, lai publicētu vidi mākonī. Lauka **Statuss** vērtība mainīta uz **Publicēts**.

## <a name="create-a-connected-application"></a>Izveidojiet pievienotu pievienojumprogrammu

1. Lapas **Vides iestatīšana** darbību rūtī atlasiet **Pieslēgtās lietojumprogrammas**.
2. Atlasiet **Jauns**, lai izveidotu savienotu lietojumprogrammu.
3. Laukā **Nosaukums** ievadiet savienotās lietojumprogrammas nosaukumu.
4. Laukā **Lietojumprogramma** ievadiet Finance un Supply Chain Management vides URL, ar kuru veidot savienojumu.
4. Laukā **Īrnieks** ievadiet Finance un Supply Chain Management vides īrnieku.
5. Atlasiet **Saglabāt**.
6. Darbību rūtī atlasiet **Pārbaudīt savienojumu**, lai pārbaudītu savienojumu ar vidi. Tad aizveriet lapu.

## <a name="link-connected-applications-to-environments"></a>Saistīt savienotās programmas ar vidēm

1. Lapā **Vides iestatīšana** atlasiet **Jauna**, lai videi piešķirtu pieslēgto lietojumprogrammu.
2. Laukā **Savienotā programma** atlasiet savienoto lietojumprogrammu.
3. Laukā **Pakalpojuma vide** atlasiet darba pasūtījuma pakalpojuma vidi.
4. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>Iestatīt elektronisko rēķinu izrakstīšanas integrēšanu Finance un Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>Iesledziet elektronisko rēķinu izrakstīšanas integrācijas līdzekli

1. Pierakstieties jūsu Finance vai Supply Chain Management instancē.
2. Darbvietā **Līdzekļu pārvaldība** meklējiet līdzekli **Konfigurējamā elektronisko rēķinu izrakstīšanas integrācija**. Ja šis līdzeklis lapā nav redzams, atlasiet **Pārbaudīt, vai nav atjauninājumu**.
3. Atlasiet līdzekli un pēc tam atlasiet **Iespējot tūlīt**.

### <a name="set-up-the-service-endpoint-url"></a>Pakalpojuma galapunkta URL iestatīšana

1. Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.
2. Cilnes **Elektroniskā rēķinu izrakstīšana** laukā **Galapunkta URL** ievadiet jūsu Azure ģeogrāfijai atbilstošo servisa galapunktu, kā parādīts tabulā tālāk.

    | Datacenter Azure ģeogrāfija | Pakalpojuma galapunkta URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | ASV              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Eiropa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Apvienotā Karaliste             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Āzija                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Laukā **Vide** ievadiet pakalpojumu vides nosaukumu, kas publicēts elektronisko rēķinu izrakstīšanā.
4. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

### <a name="enable-flighting-keys-for-finance-or-supply-chain-management-version-10017"></a>Lidojošo taustiņu iespējošana Finance vai Supply Chain Management 10.0.17. versijai

1. Izpildiet šādu SQL komandu:

    IEVIETOT SYSFLIGHTING (FLIGHTNAME, IESPĒJOTS) VĒRTĪBAS ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    IEVIETOT SYSFLIGHTING (FLIGHTNAME, IESPĒJOTS) VĒRTĪBAS ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. Veiciet IISreset komandu visiem AOS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
