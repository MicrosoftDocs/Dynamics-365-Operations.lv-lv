---
title: Iestatīt Azure resursus elektroniskajiem rēķiniem
description: Šajā tēmā ir sniegts pārskats par elektronisko rēķinu resursu iestatīšanas Microsoft Azure procesu.
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cb1fcddce1054aebf9ef70ba69eb7aca98093cbe
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371938"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Iestatīt Azure resursus elektroniskajiem rēķiniem

[!include [banner](../includes/banner.md)]

Elektronisko rēķinu resursu iestatīšanas Microsoft Azure procesam ir trīs soļi. Pirmās divas darbības : "Izveidot Azure atslēgu seifu Azure portālā" un "Izveidot Azure krātuves kontu Azure portālā" ir obligātas. Trešais solis "Konfigurēt savienojumu" nav obligāts SharePoint.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Izveidot Azure key vault in the Azure portal

Izveidojiet atslēgu seifu savā Azure abonementā. Ieteicams izveidot atsevišķu atslēgu seifu elektroniskajiem rēķiniem un neapvienot noslēpumus ar citām lietojumprogrammām. Izveidojiet tik daudz noslēpumu un sertifikātu, cik nepieciešams saviem scenārijiem elektroniskajos dokumentos. Lai nākamajā darbībā saglabātu tā Azure krātuves konta koplietojamās piekļuves paraksta (SAS) pilnvaru, kuru izveidosit, ir jāizveido vismaz viens noslēpums.

Informāciju par to, kā veikt šo darbību, skatiet rakstā [Azure atslēgu glabātuves izveide Azure portālā](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Izveidot Azure glabāšanas kontu Azure portālā

Jums pieder visi elektroniskie dokumenti un faili, ko ģenerē elektronisko rēķinu izrakstīšanas pakalpojums vai kas tiek ievadīti pakalpojumā. Šie dokumenti un faili tiek glabāti Azure krātuves kontā, ko izveidojat savā Azure abonementā. Pakalpojums piekļūst jūsu krātuves kontam, izmantojot SAS marķieri, kas ir ņemts no atslēgas seifa noslēpuma.

Informāciju par to, kā veikt šo darbību, skatiet rakstā [Azure krātuves konta izveide Azure portālā](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>SharePoint Savienojuma konfigurēšana

Dažos gadījumos, iespējams, būs jāsaglabā elektroniskie faili programmā SharePoint un jāizgūst tie no programmas SharePoint. Lai nodrošinātu, ka elektronisko rēķinu izrakstīšanas pakalpojums var piekļūt jūsu SharePoint mapēm, konfigurējiet piekļuvi SharePoint.

Informāciju par to, kā veikt šo darbību, skatiet rakstā [Savienojuma SharePoint konfigurēšana](e-invoicing-create-sharepoint-connection.md).
