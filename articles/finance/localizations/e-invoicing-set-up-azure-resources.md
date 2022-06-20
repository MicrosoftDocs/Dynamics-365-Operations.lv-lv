---
title: Iestatīt Azure resursus elektroniskajai rēķinu izrakstīšanai
description: Šajā rakstā sniegts pārskats par elektronisko rēķinu izrakstīšanas Microsoft Azure resursu iestatīšanas procesu.
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
ms.openlocfilehash: c5b7b2ca4d7733fb1c75ded8798655699284fe1a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907734"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Iestatīt Azure resursus elektroniskajai rēķinu izrakstīšanai

[!include [banner](../includes/banner.md)]

Elektronisko rēķinu izrakstīšanas Microsoft Azure resursu iestatīšanas procesam ir trīs soļi. Pirmās divas darbības " Azure atslēgas izveide Azure portālā" un "Azure noliktavas konta izveide Azure portālā" ir obligātas. Trešais solis "Savienojuma konfigurēšana SharePoint " nav obligāts.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Azure atslēgas izveide Azure portālā

Izveidojiet atslēgu Azure abonementā. Elektronisko rēķinu izrakstīšanai ir ieteicams izveidot atsevišķu atslēgu, kas neapvieno noslēpumus ar citām programmām. Izveidojiet tik daudz noslēpumu un sertifikātu, cik nepieciešams saviem scenārijiem elektroniskajā dokumentos. Lai saglabātu kopīgoto piekļuves paraksta (SAS) marķieri no Azure glabāšanas konta, ko izveidosit nākamajā darbībā, ir jāizveido vismaz viens noslēpums.

Papildinformāciju par to, kā izpildīt šo darbību, [skatiet sadaļā Azure atslēgas izveide Azure portālā](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Azure krātuves konta izveide Azure portālā

Jums pieder visi elektroniskie dokumenti un faili, ko ģenerējis Elektronisko rēķinu izrakstīšanas pakalpojums vai pakalpojuma ievadīšana. Šie dokumenti un faili tiek glabāti Azure krātuves kontā, kas tiek izveidots Azure abonementā. Pakalpojums varēs piekļūt jūsu glabāšanas kontam, izmantojot SAS marķieri, kas tiek paņemts no jūsu Atslēgas noslēpuma.

Papildinformāciju par to, kā izpildīt šo darbību, [skatiet sadaļā Azure glabāšanas konta izveide Azure portālā](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>SharePoint savienojuma konfigurēšana

Dažos scenārijos, iespējams, būs jāsaglabā elektroniskie faili, lai tos SharePoint izgūtu, un no tiem jāielādē SharePoint. Lai nodrošinātu, ka Elektronisko rēķinu izrakstīšanas pakalpojums var piekļūt jūsu SharePoint mapēm, konfigurējiet piekļuvi SharePoint.

Papildinformāciju par to, kā pabeigt šo darbību, skatiet [sadaļā Savienojuma SharePoint konfigurēšana](e-invoicing-create-sharepoint-connection.md).
