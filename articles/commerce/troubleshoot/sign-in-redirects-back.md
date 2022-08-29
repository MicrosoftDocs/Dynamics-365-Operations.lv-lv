---
title: Pierakstīšanās saite novirza atpakaļ uz e-komercijas vietni
description: Šajā rakstā ir sniegti traucējummeklēšanas norādījumi, kas var palīdzēt, kad pierakstīšanās saite novirza atpakaļ uz e-komercijas vietni, nevis doties uz pierakstīšanās lapu.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 0bc9c0afbd6b349d8565f9eea56e207eae179f65
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291460"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>Pierakstīšanās saite novirza atpakaļ uz e-komercijas vietni

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegti traucējummeklēšanas norādījumi, kas var palīdzēt, kad pierakstīšanās saite novirza atpakaļ uz e-komercijas vietni, nevis doties uz pierakstīšanās lapu.

## <a name="description"></a>Apraksts

Pēc jauna Microsoft Azure Active Directory B2C (Azure AD B2C) nomnieka konfigurēšanas Commerce vietnes veidotājā lietotāji, kuri atlasa saiti **Pierakstīties**, tiek pārvirzēti atpakaļ uz galveno e-komercijas informācijas lapu, neatverot pierakstīšanās lapu.

## <a name="resolution"></a>Novēršana

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>Apstipriniet, ka atbildes vietrādis URL ir pareizi konfigurēts Azure AD B2C programmā

Lai apstiprinātu, ka atbildes vietrādis URL ir pareizi konfigurēts Azure AD B2C programmā, izpildiet tālāk minētās darbības.

1. Dodieties uz [Azure portālu](https://portal.azure.com/).
1. Atlasiet Azure AD B2C programmu, ko izveidojāt jūsu vietnes piekļuvei.
1. Atlasiet programmu, ko izveidojāt Azure AD B2C iestatīšanas laikā.
1. Sadaļā **Atbildes vietrādis URL** pārliecinieties, vai sarakstā ir ietverti gan vietnes domēna vietrāža URL, gan e-komercijas ģenerētā vietrāža URL ieraksti, kā parādīts piemērā nākamajā attēlā.

    ![Azure AD B2C atbildes vietrāža URL ieraksti.](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> Gan vietnes domēna vietrādim URL, gan e-komercijas ģenerētajam vietrādim URL ir jābūt derīgā URL formātā, kas neietver sākuma un beigu slīpsvītras.

## <a name="additional-resources"></a>Papildu resursi

[Tīmekļa programmas reģistrēšana portālā Azure Active Directory B2C](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[B2C nomnieka iestatīšana programmā Commerce](../set-up-b2c-tenant.md)
