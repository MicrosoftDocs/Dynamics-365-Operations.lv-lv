---
title: Izveidot Azure krātuves kontu un galveno akreditācijas datu glabātavu
description: Šajā tēmā ir paskaidrots, kā izveidot Azure krātuves kontu un galveno akreditācijas datu glabātavu.
author: gionoder
ms.date: 08/17/2021
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
ms.openlocfilehash: 23fec7a00d800719e1a7d2c90f9d0977d56be038
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463861"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Izveidot Azure krātuves kontu un galveno akreditācijas datu glabātavu

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu izpildīt šajā tēmā aprakstītās darbības, ir jāpārliecinās, ka tālāk norādītie uzdevumi tika izpildīti.

- Galvenās akreditācijas datu glabātavas resursa veidošana risinājumā Azure. Plašāku informāciju skatiet sadaļā [Par Azure Key Vault](/azure/key-vault/general/overview).
- Izveidot Azure krātuves kontu (BLOB Storage). Papildinformāciju skatiet šeit: [Azure krātuves konta uzturēšana](/azure/storage/blobs/).

## <a name="overview"></a>Pārskats

Šajā tēmā jūs veiksiet divas galvenās darbības:

- Iestatiet Azure krātuves kontu, lai iegūtu krātuves konta URI.
- Iestatiet galveno akreditācijas datu glabātavu, lai saglabātu krātuves konta URI.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Iestatiet Azure krātuves kontu, lai iegūtu krātuves konta URI

1. Atveriet krātuves kontu, ko plānojat izmantot kopā ar Elektronisko rēķinu izrakstīšanu.
2. Dodieties uz **Datu glabātuve**  > **Konteineri** un izveidojiet jaunu konteineru.
3. Ievadiet konteinera nosaukumu un iestatiet lauku **Publiskās piekļuves līmenis** uz **Privāts (nav anonīmas piekļuves)**.
4. Atveriet konteineru un dodieties uz **Iestatījumi**  > **Piekļuves politika**.
5. Atlasiet **Pievienot politiku**, lai pievienotu saglabāto piekļuves politiku.
6. Pēc nepieciešamības iestatiet laukus **Identifikators** un **Atļaujas**. Laukā **Atļaujas** jāatlasa visas atļaujas.

    ![BLOB krātuves atļaujas piešķiršana.](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Ievadiet sākuma un beigu datumus. Beigu datumam ir jābūt nākotnē.
8. Atlasiet **Labi**, lai saglabātu politiku, un pēc tam saglabājiet izmaiņas konteinerā.
9. Dodieties uz **Iestatījumi** > **Kopīgotie piekļuves marķieri** un iestatiet lauku vērtības. 
10. Ievadiet sākuma un beigu datumu. Beigu datumam jābūt nākotnē.
11. Laukā **Atļauja** atlasiet šādas atļaujas **Lasīt**, **Pievienot**, **Izveidot**, **Rakstīt**, **Dzēst** un **Izveidot sarakstu**. 
12. Atlasiet **Ģenerēt SAS marķieri un URL**.
13. Kopējiet un saglabājiet vērtību laukā **BLOB SAS URL**. Šī vērtība tiks izmantota nākamajā procedūrā, un tā tiks saukta par *koplietojamās piekļuves paraksta URI*.

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Iestatiet galveno akreditācijas datu glabātavu, lai saglabātu krātuves konta URI

1. Atveriet galveno akreditācijas datu glabātavu, ko plānojat izmantot kopā ar Elektronisko rēķinu izrakstīšanu.
2. Dodieties uz **Iestatījumi** \> **Noslēpumi** un pēc tam atlasiet **Ģenerēt/Importēt**, lai izveidotu jaunu noslēpumu.
3. Lapā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāls**.
4. Ievadiet noslēpuma nosaukumu. Šis nosaukums tiks izmantots, iestatot pakalpojumu regulatīvās konfigurācijas pakalpojumā (Regulatory Configuration Service - RCS), un tas tiks saukts par *galvenās akreditācijas datu glabātavas nosaukums*.
5. Laukā **Vērtība** ievadiet kopīgotās piekļuves paraksta URI, kuru iekopējāt iepriekšējā darbībā, un pēc tam atlasiet **Izveidot**.
6. Iestatiet piekļuves politiku, lai elektronisko rēķinu izrakstīšanai piešķirtu pareizu drošas piekļuves līmeni jūsu izveidotajam noslēpumam. Dodieties uz **Iestatījumi \> Piekļuves politika** un atlasiet **Pievienot piekļuves politiku**.
7. Iestatiet noslēpuma atļaujas operācijām **Iegūt** un **Uzskaitīt**.

    ![Pakalpojumu piekļuves piešķiršana.](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Iestatiet sertifikāta atļaujas operācijām **Iegūt** un **Uzskaitīt**.

    ![Sertifikāta atļaujas piešķiršana.](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. Laukā **Atlasīt vadītāju** atlasiet **Nav atlasīts**.
10. Dialoglodziņā **Vadītājs** atlasiet vadītāju, pievienojot **Elektronisko rēķinu izrakstīšanas pakalpojums**.
11. Atlasiet **Pievienot** un pēc tam atlasiet **Saglabāt**.
12. Lapā **Pārskats** nokopējiet vērtību **DNS nosaukums** galvenajai akreditācijas datu glabātavai. Šī vērtība tiks izmantota pakalpojuma iestatīšanas laikā ar RCS un tiks saukta par *galveno galvenajās akreditācijas datu glabātavas URI*.

> [!NOTE]
> Lai glabāšanas kontā iegūtu papildu drošību, konfigurējiet Azure Defender krātuvei.
> 
> Papildinformāciju skatiet sadaļā [Ievads programmā Azure Defender krātuvei](/azure/security-center/defender-for-storage-introduction).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
