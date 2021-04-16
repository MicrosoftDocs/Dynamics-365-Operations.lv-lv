---
title: Atgriešanas pasūtījuma atmaksa ir noraidīta
description: Šajā tēmā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad atgriešanas pasūtījuma atmaksa ir noraidīta, jo rēķina izrakstīšanai izmantotā kredītkarte atšķiras no kartes, kas tika izmantota sākotnējās maksājuma autorizācijas laikā.
author: Reza-Assadi
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
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5961e77de1de5dc23454fc1a6e16f8c0b4e7cc6a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801559"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="92cfb-103">Atgriešanas pasūtījuma atmaksa ir noraidīta</span><span class="sxs-lookup"><span data-stu-id="92cfb-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="92cfb-104">Šajā tēmā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, kad atgriešanas pasūtījuma atmaksa ir noraidīta, jo rēķina izrakstīšanai izmantotā kredītkarte atšķiras no kartes, kas tika izmantota sākotnējās maksājuma autorizācijas laikā.</span><span class="sxs-lookup"><span data-stu-id="92cfb-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="92cfb-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="92cfb-105">Description</span></span>

<span data-ttu-id="92cfb-106">Atmaksa tiek noraidīta, ja kredītkarte, kas tiek izmantota atgriešanas pasūtījuma rēķinam, atšķiras no kartes, kas tika izmantota sākotnējās maksājuma autorizācijas laikā.</span><span class="sxs-lookup"><span data-stu-id="92cfb-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="92cfb-107">Tiek saņemts šāds kļūdas ziņojums: "Dažiem maksājumiem nav pareizais grāmatošanas statuss.</span><span class="sxs-lookup"><span data-stu-id="92cfb-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="92cfb-108">Lūdzu, atkārtoti pārbaudiet visu maksājumu statusu pirms rēķina izrakstīšanas."</span><span class="sxs-lookup"><span data-stu-id="92cfb-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="92cfb-109">Maksājuma autorizācijas papildinformācijā tiks iekļauts šāds kļūdas ziņojums: "Adyen vārteja SendRequest() neizdevās ar statusu 'InternalServerError'.22144; Tukša atbilde atgriezta no Adyen.(22001);"</span><span class="sxs-lookup"><span data-stu-id="92cfb-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![Noraidītas atgriešanas pasūtījuma atmaksas kļūda](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="92cfb-111">Novēršana</span><span class="sxs-lookup"><span data-stu-id="92cfb-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="92cfb-112">Diskrēti slēgto atgriešanu iespējošana Adyen</span><span class="sxs-lookup"><span data-stu-id="92cfb-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="92cfb-113">Lai iespējotu diskrēti slēgtās atgriešanas, izpildiet darbības [Dynamics 365 maksājumu savienotāja problēmu novēršana Adyen problēmām](adyen-support.md), lai sazinātos ar Adyen atbalsta komandu un pieprasītu, lai jūsu Adyen tirgotāja kontā tiktu iespējotas diskrēti slēgtās atgriešanas.</span><span class="sxs-lookup"><span data-stu-id="92cfb-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92cfb-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="92cfb-114">Additional resources</span></span>

[<span data-ttu-id="92cfb-115">Dynamics 365 maksājumu savienotājs pakalpojumam Adyen</span><span class="sxs-lookup"><span data-stu-id="92cfb-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="92cfb-116">Adyen maksājumu savienotāja iestatīšana risinājumam Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="92cfb-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
