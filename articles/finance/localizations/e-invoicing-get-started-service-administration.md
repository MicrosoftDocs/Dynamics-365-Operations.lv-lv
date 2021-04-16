---
title: Darba sākšana ar elektroniskās rēķinu izveides servisa administrēšanu
description: Šajā tēmā ir paskaidrots, kā sākt darbu ar Elektronisko rēķinu izrakstīšanu.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840152"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>Darba sākšana ar elektroniskās rēķinu izveides servisa administrēšanu

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms pabeidzat šajā tēmā norādītās procedūras, ir jāievieš šādi priekšnosacījumi:

- Jums ir jābūt piekļuvei jūsu Microsoft Dynamics Lifecycle Services (LCS) kontam.
- Jums jābūt LCS projektam, kas ietver Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management programmu versiju 10.0.17 vai jaunāku. Turklāt šīs programmas ir jāizvieto vienā no tālāk minētajām Azure ģeogrāfiskām vietām:

    - ASV austrumi
    - ASV rietumi
    - Ziemeļeiropa
    - Rietumeiropa

- Jums ir jābūt piekļuvei jūsu Dynamics 365 Regulatory Configuration Services (RCS) kontam.
- Jums jāaktivizē Globalizācijas līdzeklis jūsu RCS kontā Līdzekļu pārvaldībā. Papildinformāciju skatiet sadaļā [Regulatory Configuration Services (RCS) — Globalizācijas līdzekļi](rcs-globalization-feature.md).
- Jums jāizveido galvenā glabātuve un krātuves kontu risinājumā Azure. Papildinformāciju skatiet šeit: [Azure krātuves konta un galvenās glabātavas izveide](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Instalējiet programmu Microservices pievienojumprogrammu pakalpojumam Lifecycle Services

1. Piesakieties savā LCS kontā.
2. Atlasiet **Priekšskatījuma līdzekļu pārvaldības** elementu.
3. Sadaļā **Publiskā priekšskatījuma līdzekļi** atlasiet **e-rēķinu izrakstīšanas pakalpojumu**.
4. Pārliecinieties, vai opcija **Priekšskatījuma līdzeklis iespējots** ir iestatīta uz **Jā**.
5. LCS informācijas panelī atlasiet savu LCS izvietošanas projektu. LCS projektam jādarbojas.
7. Cilnē **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.
8. Izvēlieties **e-rēķinu pakalpojumus**.
9. Laukā **AAD pieteikuma ID** ievadiet **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Šī ir fiksēta vērtība.
10. Laukā **AAD nomnieka ID** ievadiet jūsu Azure abonementa konta nomnieka ID.
11. Pārskatiet noteikumus un nosacījumus un atzīmējiet izvēles rūtiņu.
12. Atlasiet **Instalēt**.


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Iestatiet RCS integrācijas parametrus ar elektronisko rēķinu izrakstīšanu

1. Piesakieties savā RCS kontā.
2. Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Saistītās saites** atlasiet **Elektronisko pārskatu veidošanas parametri**.
3. Cilnē **e-rēķinu pakalpojums** laukā **Pakalpojuma galapunkta URI** ievadiet atbilstoši azure ģeogrāfijas pakalpojuma galapunktu, kā norādīts tālāk sniegtajā tabulā.

    | Datacenter Azure ģeogrāfija | Pakalpojuma galapunkta URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | ASV austrumi                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | ASV rietumi                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Ziemeļeiropa                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Rietumeiropa                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. Pārbaudiet, vai **Lietojumprogrammas Id** lauks ir iestatīts uz **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Šī vērtība ir fiksēta vērtība.
5. Laukā **LCS vides Id** ievadiet jūsu LCS vides ID.
6. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

## <a name="create-key-vault-references"></a>Atslēgas akreditācijas datu komplekta atsauksmju veidošana

1. Piesakieties savā RCS kontā.
2. Darbvietā **Globalizācijas līdzeklis** sadaļā **Vide** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
3. Lapā **Vides iestatījumi** darbības rūtī atlasiet **Pakalpojuma vide** un atlasiet **Atslēgas glabātuves parametri**.
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

1. Lapā **Vides iestatījumi** darbības rūtī atlasiet **Pakalpojuma vide** un atlasiet **Atslēgas glabātuves parametri**.
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

1. Lapā **Vides iestatījumi** darbību rūtī atlasiet **Savienotās lietojumprogrammas**.
2. Atlasiet **Jauns**, lai izveidotu savienotu lietojumprogrammu.
3. Laukā **Nosaukums** ievadiet savienotās lietojumprogrammas nosaukumu.
4. Laukā **Lietojumprogramma** ievadiet Finance un Supply Chain Management vides URL, ar kuru veidot savienojumu.
4. Laukā **Īrnieks** ievadiet Finance un Supply Chain Management vides īrnieku.
5. Atlasiet **Saglabāt**.
6. Darbību rūtī atlasiet **Pārbaudīt savienojumu**, lai pārbaudītu savienojumu ar vidi. Tad aizveriet lapu.

## <a name="link-connected-applications-to-environments"></a>Saistīt savienotās programmas ar vidēm

1. Lai videi piešķirtu pievienoto programmu **Vides iestatījumu** lapā atlasiet **Jauns**.
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
2. Cilnē **Iesniegšanas pakalpojums** laukā **Pakalpojuma galapunkta URL** ievadiet atbilstoši azure ģeogrāfijas pakalpojuma galapunktu, kā norādīts tālāk sniegtajā tabulā.

    | Datacenter Azure ģeogrāfija | Pakalpojuma galapunkta URL                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | ASV austrumi                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | ASV rietumi                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Ziemeļeiropa                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Rietumeiropa                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. Laukā **Vide** ievadiet pakalpojumu vides nosaukumu, kas publicēts elektronisko rēķinu izrakstīšanā.
4. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

### <a name="enable-flighting-keys"></a>Iespējot testējamās atslēgas

Iespējojiet testējamās atslēgas Microsoft Dynamics 365 Finance vai Microsoft Dynamics 365 Supply Chain Management versijām 10.0.17 vai vecākām versijām. 
1. Izpildiet šādu SQL komandu:

    IEVIETOT SYSFLIGHTING (FLIGHTNAME, IESPĒJOTS) VĒRTĪBAS ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    IEVIETOT SYSFLIGHTING (FLIGHTNAME, IESPĒJOTS) VĒRTĪBAS ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. Izpildiet IISreset komandu visām AOS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
