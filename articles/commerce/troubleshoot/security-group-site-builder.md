---
title: Sākotnējās izvietošanas laikā Commerce vietnes veidotājā nevar konfigurēt drošības grupu
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad Microsoft Azure Active Directory (Azure AD) drošības grupa Commerce vietnes veidotājam neparādās kā opcija, kad izveidojat e-komercijas komponentus Microsoft Dynamics Lifecycle Services (LCS) jauna e-komercijas nomnieka sākotnējās izvietošanas laikā.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: f930cac61b747037b9fbecc7397a9b1b7db5dabd8a86b63a61c92ac7abe17516
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765174"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Sākotnējās izvietošanas laikā Commerce vietnes veidotājā nevar konfigurēt drošības grupu

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, kad Microsoft Azure Active Directory (Azure AD) drošības grupa Commerce vietnes veidotājam neparādās kā opcija, kad izveidojat e-komercijas komponentus Microsoft Dynamics Lifecycle Services (LCS) jauna e-komercijas nomnieka sākotnējās izvietošanas laikā.

## <a name="description"></a>Apraksts

Kad izveidojat e-komercijas komponentus kā daļu no jauna e-komercijas nomnieka, kas ietver Commerce vietnes veidotāja komponentu, izvietošanas procesa ietvaros drošības grupa neparādīsies kā Azure AD opcija dialoglodziņā.

## <a name="resolution"></a>Novēršana

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>E-komercijas vietnes nodrošināšana ar lietotāju pareizajā nomniekā

1. Dodieties uz [Azure portālu](https://portal.azure.com/).
1. Zem nomnieka, kam tika nodrošināts LCS projekts jūsu e-komercijas vietnei, izpildiet norādes sadaļā [Pamata grupas izveide un dalībnieku pievienošana, izmantojot Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. Dodieties uz [LCS](https://lcs.dynamics.com/) un pierakstieties, izmantojot kontu, kam ir tāds pats nomnieks kā Azure AD drošības grupai, kuru tikko izveidojāt. Kontam jābūt piekļuvei, lai skatītu Azure AD drošības grupu.
1. Izpildiet iestatīšanas darbības, lai konfigurētu e-komercijas vietni. Izveidojot e-komercijas komponentus, drošības grupai tagad ir jāparādās kā opcijai dialoglodziņā.

> [!NOTE]
> Lai nodrošinātu, ka lauks dialoglodziņā ir aizpildīts ar drošības grupu sarakstu, jums jāatlasa **Ievadīt**, kad esat ievadījis izveidotās Azure AD drošības grupas nosaukumu. Meklēšanas rezultātos tiks uzskaitītas visas Azure AD drošības grupas, kuras sākas ar meklēšanas tekstu un kurām lietotājam ir piekļuve. Lai panāktu plašākus meklēšanas rezultātus, varat izmantot īsāku meklējamo terminu.

## <a name="additional-resources"></a>Papildu resursi

[Pamatgrupas izveide un dalībnieku pievienošana, izmantojot Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Jauna e-komercijas nomnieka izvietošana](../deploy-ecommerce-site.md)