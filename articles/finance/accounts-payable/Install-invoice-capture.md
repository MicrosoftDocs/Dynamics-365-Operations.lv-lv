---
title: Rēķina ieguves risinājuma instalēšana
description: Šajā rakstā ir sniegta informācija par to, kā instalēt rēķina tveršanas risinājumu un integrēt to ar Microsoft Dynamics 365 Finansēm.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691007"
---
# <a name="install-the-invoice-capture-solution"></a>Rēķina ieguves risinājuma instalēšana

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Ja risinājumu instalējāt privātā priekšskatījumā, pirms turpināt, jums jāatinstalē vecais risinājums.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms rēķina tveršanas risinājuma instalēšanas ir jāpabeidz šādi priekšnosacījumi:

1. Reģistrējiet programmu un pievienojiet klienta noslēpumu korporācijai Microsoft Azure Active Directory (Azure AD) atbilstoši Azure abonementam. Papildinformāciju skatiet sadaļā [Tīmekļa programmas reģistrēšana AAD](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad).

    > [!NOTE]
    > Atzīmējiet programmas (klienta **) ID**, klienta **noslēpuma** **un nomnieka ID** vērtības, jo tās būs nepieciešamas vēlāk.

2. Reģistrējiet Azure programmu Dynamics 365 finanšu vidē. Papildinformāciju skatiet sadaļā [Ārējās programmas reģistrēšana](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application).

## <a name="install-and-set-up-the-solution"></a>Risinājuma instalēšana un iestatīšana

Lai instalētu rēķina tveršanas risinājumu, AppSource dodieties uz un atlasiet [saiti Dynamics 365 rēķina tveršanas priekšskatījuma versijai](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture). Kad instalēšana ir pabeigta, risinājums ir instalēts atlasītajā vidē Power Apps sadaļā.

Lai pabeigtu iestatīšanu, sekojiet šiem soļiem.

1. Lejupielādējiet [asistenta](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip) risinājumu, lai iestatītu šādu informāciju:

    - Komunikācija starp Microsoft Power Platform finanšu vidi un par finansēm
    - Savienojuma atsauce programmai Dataverse un Office 365 Outlook, ko izmantos kanāls

2. Dodieties Power Apps uz vidi un atlasiet Importēt **risinājumu**.
3. Atlasiet **Pārlūkot**, atlasiet lejupielādēto asistenta risinājumu pakotni un pēc tam atlasiet **Tālāk**.
4. Atlasiet **Nākamais**.
5. Piešķiriet esošu savienojumu vai izveidojiet jaunu, atlasot Jauns **savienojums**.
6. Pēc pakotnes veiksmīgas importēšanas atveriet **Dynamics 365 rēķina tveršanu — instalēšanas rīkus**.
7. Palaidiet mākoņa plūsmu, lai iestatītu savienojumu starp rēķina ieguves risinājumu un Finansēm Microsoft Power Platform.
8. Atlasiet **Palaist** un norādiet šādus parametrus:

    - **Dynamics 365 Finanšu URL** — tās finanšu vides URL, ar kuru vēlaties integrēt.
    - **Nomnieka ID — finanšu vides nomnieka ID**.
    - **Klienta ID — reģistrētais Azure programmas ID**.
    - **Klienta noslēpums** — klienta noslēpums, kas ģenerēts Azure programmai.
