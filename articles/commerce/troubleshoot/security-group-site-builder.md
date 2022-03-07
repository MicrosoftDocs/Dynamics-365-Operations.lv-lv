---
title: Sākotnējās izvietošanas laikā Commerce vietnes veidotājā nevar konfigurēt drošības grupu
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad Microsoft Azure Active Directory (Azure AD) drošības grupa Commerce vietnes veidotājam neparādās kā opcija, kad izveidojat e-komercijas komponentus Microsoft Dynamics Lifecycle Services (LCS) jauna e-komercijas nomnieka sākotnējās izvietošanas laikā.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36ea43e19f395e3914d3eda1a9b8f5487b0926c5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585432"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Sākotnējās izvietošanas laikā Commerce vietnes veidotājā nevar konfigurēt drošības grupu

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad Microsoft Azure Active Directory (Azure AD) drošības grupa Commerce vietnes veidotājam neparādās kā opcija, kad izveidojat e-komercijas komponentus Microsoft Dynamics Lifecycle Services (LCS) jauna e-komercijas nomnieka sākotnējās izvietošanas laikā.

## <a name="description"></a>Apraksts

Kad izveidojat e-komercijas komponentus kā daļu no jauna e-komercijas nomnieka, kas ietver Commerce vietnes veidotāja komponentu, izvietošanas procesa ietvaros drošības grupa neparādīsies kā Azure AD opcija dialoglodziņā.

## <a name="resolution"></a>Novēršana

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>E-komercijas vietnes nodrošināšana ar lietotāju pareizajā nomniekā

1. Dodieties uz [Azure portālu](https://portal.azure.com/).
1. Zem nomnieka, kam tika nodrošināts LCS projekts jūsu e-komercijas vietnei, izpildiet norādes sadaļā [Pamata grupas izveide un dalībnieku pievienošana, izmantojot Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. Dodieties uz [LCS](https://lcs.dynamics.com/) un pierakstieties, izmantojot kontu, kam ir tāds pats nomnieks kā Azure AD drošības grupai, kuru tikko izveidojāt. Kontam jābūt piekļuvei, lai skatītu Azure AD drošības grupu.
1. Izpildiet iestatīšanas darbības, lai konfigurētu e-komercijas vietni. Izveidojot e-komercijas komponentus, drošības grupai tagad ir jāparādās kā opcijai dialoglodziņā.

> [!NOTE]
> Lai nodrošinātu, ka lauks dialoglodziņā ir aizpildīts ar drošības grupu sarakstu, jums jāatlasa **Ievadīt**, kad esat ievadījis izveidotās Azure AD drošības grupas nosaukumu. Meklēšanas rezultātos tiks uzskaitītas visas Azure AD drošības grupas, kuras sākas ar meklēšanas tekstu un kurām lietotājam ir piekļuve. Lai panāktu plašākus meklēšanas rezultātus, varat izmantot īsāku meklējamo terminu.

## <a name="additional-resources"></a>Papildu resursi

[Pamatgrupas izveide un dalībnieku pievienošana, izmantojot Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Jauna e-komercijas nomnieka izvietošana](../deploy-ecommerce-site.md)
