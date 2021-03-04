---
title: Izveidot Azure krātuves kontu un galveno akreditācijas datu glabātavu
description: Šajā tēmā ir paskaidrots, kā izveidot Azure krātuves kontu un galveno akreditācijas datu glabātavu.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 5a883011bbff6d82504497d739c07f1ada9e5f69
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/19/2020
ms.locfileid: "4445767"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Izveidot Azure krātuves kontu un galveno akreditācijas datu glabātavu

[!include [banner](../includes/banner.md)]



Elektronisko rēķinu izrakstīšanas pievienojumprogramma uzņemas atbildību par visu jūsu uzņēmuma datu glabāšanu Microsoft Azure resursos, kas pieder jūsu uzņēmumam. Lai nodrošinātu, ka pakalpojums darbojas pareizi un ka visiem biznesa datiem, kas ir nepieciešami un ko ģenerē Elektronisko rēķinu izrakstīšanas pievienojumprogramma, ir piekļuve tikai pievienojumprogrammai, ir jāizveido divi galvenie Azure resursi:

- Azure krātuves konts (BLOB krātuve) elektronisko rēķinu glabāšanai
- Azure atslēgu glabātuve, kur glabāt sertifikātus un krātuves konta vienoto resursu identifikatoru (Uniform Resource Identifier - URI)

> [!NOTE]
> Īpašam galvenās akreditācijas datu glabātavas resursam un debitora BLOB krātuvei ir jābūt piešķirtai tieši lietošanai ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu izpildīt šajā tēmā aprakstītās darbības, ir jāpārliecinās, ka tālāk norādītie uzdevumi tika izpildīti.

- Galvenās akreditācijas datu glabātavas resursa veidošana risinājumā Azure. Plašāku informāciju skatiet sadaļā [Par Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).
- Izveidot Azure krātuves kontu (BLOB Storage). Papildinformāciju skatiet šeit: [Azure krātuves konta uzturēšana](https://docs.microsoft.com/azure/storage/blobs/).

## <a name="overview"></a>Pārskats

Šajā tēmā jūs veiksiet divas galvenās darbības:

- Iestatiet Azure krātuves kontu, lai iegūtu krātuves konta URI.
- Iestatiet galveno akreditācijas datu glabātavu, lai saglabātu krātuves konta URI.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Iestatiet Azure krātuves kontu, lai iegūtu krātuves konta URI

1. Atveriet krātuves kontu, ko plānojat izmantot kopā ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu.
2. Dodieties uz **BLOB pakalpojums** \> **Konteineri** un izveidojiet jaunu konteineru.
3. Ievadiet konteinera nosaukumu un iestatiet lauku **Publiskās piekļuves līmenis** uz **Privāts (nav anonīmas piekļuves)**.
4. Atveriet konteineru un dodieties uz **Iestatījumi \> Piekļuves politika**.
5. Atlasiet **Pievienot politiku**, lai pievienotu saglabāto piekļuves politiku.
6. Pēc nepieciešamības iestatiet laukus **Identifikators** un **Atļaujas**. Laukā **Atļaujas** jāatlasa visas atļaujas.

    ![BLOB krātuves atļaujas piešķiršana](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Ievadiet sākuma un beigu datumus. Beigu datumam ir jābūt nākotnē.
8. Atlasiet **Labi**, lai saglabātu politiku, un pēc tam saglabājiet izmaiņas konteinerā.
9. Atgriezieties krātuves kontā un atveriet **Storage Explorer (priekšskatījums)**.
10. Ar peles labo pogu noklikšķiniet uz konteinera un pēc tam atlasiet **Iegūt koplietojamās piekļuves parakstu**.
11. Dialoglodziņā **Koplietotas piekļuves paraksts** kopējiet un saglabājiet vērtību laukā **URI**. Šī vērtība tiks izmantota nākamajā procedūrā, un tā tiks saukta par *koplietojamās piekļuves paraksta URI*.

    ![Atlasīt un kopēt URI vērtību](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Iestatiet galveno akreditācijas datu glabātavu, lai saglabātu krātuves konta URI

1. Atveriet galveno akreditācijas datu glabātavu, ko plānojat izmantot kopā ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu.
2. Dodieties uz **Iestatījumi** \> **Noslēpumi** un pēc tam atlasiet **Ģenerēt/Importēt**, lai izveidotu jaunu noslēpumu.
3. Lapā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāls**.
4. Ievadiet noslēpuma nosaukumu. Šis nosaukums tiks izmantots, iestatot pakalpojumu regulatīvās konfigurācijas pakalpojumā (Regulatory Configuration Service - RCS), un tas tiks saukts par *galvenās akreditācijas datu glabātavas nosaukums*.
5. Laukā **Vērtība** atlasiet **Koplietojamās piekļuves paraksta URI** un pēc tam atlasiet **Izveidot**.
6. Iestatiet piekļuves politiku, lai elektronisko rēķinu izrakstīšanas pievienojumprogrammai piešķirtu pareizu drošas piekļuves līmeni jūsu izveidotajam noslēpumam. Dodieties uz **Iestatījumi \> Piekļuves politika** un atlasiet **Pievienot piekļuves politiku**.
7. Iestatiet noslēpuma atļaujas operācijām **Iegūt** un **Uzskaitīt**.

    ![Pakalpojumu piekļuves piešķiršana](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Iestatiet sertifikāta atļaujas operācijām **Iegūt** un **Uzskaitīt**.

    ![Sertifikāta atļaujas piešķiršana](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. Dialoglodziņā **Galvēnais** atlasiet galvēno, pievienojot **Elektronisko rēķinu izrakstīšanas pievienojumprogramma**.
10. Atlasiet **Pievienot** un pēc tam atlasiet **Saglabāt Key Vault izmaiņas**.
11. Lapā **Pārskats** nokopējiet vērtību **DNS nosaukums** galvenajai akreditācijas datu glabātavai. Šī vērtība tiks izmantota pakalpojuma iestatīšanas laikā ar RCS un tiks saukta par *galveno galvenajās akreditācijas datu glabātavas URI*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]