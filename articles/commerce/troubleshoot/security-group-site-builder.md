---
title: Sākotnējās izvietošanas laikā Commerce vietnes veidotājā nevar konfigurēt drošības grupu
description: Šajā rakstā ir sniegti norādījumi par problēmu novēršana, kas var palīdzēt, kad Microsoft Azure Active Directory (Azure AD) drošības grupa Commerce Site Builder neparādās kā opcija, kad izveidojat e-commerce Microsoft Dynamics komponentus Lifecycle Services (LCS) sākotnējās jaunas e-komercijas nomnieka izvietošanas laikā.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 7098c853c262fd7e0d48231634b232eef71c2b8d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292005"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Sākotnējās izvietošanas laikā Commerce vietnes veidotājā nevar konfigurēt drošības grupu

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegti norādījumi par problēmu novēršana, kas var palīdzēt, kad Microsoft Azure Active Directory (Azure AD) drošības grupa Commerce Site Builder neparādās kā opcija, kad izveidojat e-commerce Microsoft Dynamics komponentus Lifecycle Services (LCS) sākotnējās jaunas e-komercijas nomnieka izvietošanas laikā.

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
