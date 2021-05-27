---
title: Dynamics 365 Payment Connector Adyen problēmu novēršana
description: Šajā tēmā sniegti norādījumi problēmu novēršanai, kas var palīdzēt, ja jums radušās ar Adyen Microsoft Dynamics 365 Payment Connector.
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
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 707efeba9553b996e4e33a4754e42a9d22643e33
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019593"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="a6920-103">Dynamics 365 Payment Connector Adyen problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="a6920-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6920-104">Šajā tēmā sniegti norādījumi problēmu novēršanai, kas var palīdzēt, ja jums radušās ar Adyen Microsoft Dynamics 365 Payment Connector.</span><span class="sxs-lookup"><span data-stu-id="a6920-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="a6920-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a6920-105">Description</span></span>

<span data-ttu-id="a6920-106">Jums ir radušās problēmas ar Adyen Dynamics 365 Payment Connector šādās jomās, un jums ir nepieciešams atbalsts no Adyen komandas:</span><span class="sxs-lookup"><span data-stu-id="a6920-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="a6920-107">Pārdošanas punkta (POS), modernā pārdošanas punkta (MPOS), zvanu centra vai Dynamics 365 Commerce konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="a6920-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="a6920-108">Adyen maksājumu pakalpojumu sniedzēja (PSP) atsauces numurs (piemēram, ja jums radušies jautājumi par atteikumiem, tostarp attiecībā uz manuālo atslēgu ievadi \[MKE\])</span><span class="sxs-lookup"><span data-stu-id="a6920-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="a6920-109">Jebkas, kas nedarbojas testa vai tiešo pārdevēju vidēs</span><span class="sxs-lookup"><span data-stu-id="a6920-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="a6920-110">Novēršana</span><span class="sxs-lookup"><span data-stu-id="a6920-110">Resolution</span></span>

<span data-ttu-id="a6920-111">Izmantojiet šo e-pasta veidni, lai sāktu atbalsta procesu ar Adyen komandu.</span><span class="sxs-lookup"><span data-stu-id="a6920-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="a6920-112">Lai paātrinātu problēmu novēršanu, nodrošiniet, ka e-pastā ir visa nepieciešamā informācija.</span><span class="sxs-lookup"><span data-stu-id="a6920-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="a6920-113">Lauks</span><span class="sxs-lookup"><span data-stu-id="a6920-113">Field</span></span>        | <span data-ttu-id="a6920-114">Vērtība</span><span class="sxs-lookup"><span data-stu-id="a6920-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="a6920-115">Kam</span><span class="sxs-lookup"><span data-stu-id="a6920-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="a6920-116">Kopija</span><span class="sxs-lookup"><span data-stu-id="a6920-116">Cc</span></span>           | |
| <span data-ttu-id="a6920-117">Tēmas rindiņa</span><span class="sxs-lookup"><span data-stu-id="a6920-117">Subject line</span></span> | <span data-ttu-id="a6920-118">Microsoft Dynamics atbalsta pieprasījums</span><span class="sxs-lookup"><span data-stu-id="a6920-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="a6920-119">Pamatteksts</span><span class="sxs-lookup"><span data-stu-id="a6920-119">Body</span></span>         | <p><span data-ttu-id="a6920-120">Sveicināti, Atbalsta komanda,</span><span class="sxs-lookup"><span data-stu-id="a6920-120">Hi Support,</span></span></p><p><span data-ttu-id="a6920-121">Lūdzu, sniedziet atbalstu saistībā ar šādu problēmu:</span><span class="sxs-lookup"><span data-stu-id="a6920-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="a6920-122">Tirgotāja konts</span><span class="sxs-lookup"><span data-stu-id="a6920-122">Merchant account</span></span></li><li><span data-ttu-id="a6920-123">Vide (Testa/Ražošanas)</span><span class="sxs-lookup"><span data-stu-id="a6920-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="a6920-124">Kanāls (POS/zvanu centrs/Commerce e-komercija)</span><span class="sxs-lookup"><span data-stu-id="a6920-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="a6920-125">PSP atsauces numurs, ja rēķins iesaistīts konkrētā transakcijā (PSP numuru varat atrast uz kvīts, Adyen klientu zonā vai POS termināla transakciju izvēlnē.)</span><span class="sxs-lookup"><span data-stu-id="a6920-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="a6920-126">Kļūdas ziņojuma ekrānuzņēmums vai fotoattēls, ja piemērojami.</span><span class="sxs-lookup"><span data-stu-id="a6920-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="a6920-127">Event Viewer žurnāli (.txt formātā)</span><span class="sxs-lookup"><span data-stu-id="a6920-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="a6920-128">Problēmas apraksts un jūsu izmēģinātās problēmu novēršanas darbības</span><span class="sxs-lookup"><span data-stu-id="a6920-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="a6920-129">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a6920-129">Additional resources</span></span>

[<span data-ttu-id="a6920-130">Maksājumu pieņemšana ar Adyen savienotāju Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a6920-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="a6920-131">Dynamics 365 maksājumu savienotājs pakalpojumam Adyen</span><span class="sxs-lookup"><span data-stu-id="a6920-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="a6920-132">Adyen maksājumu savienotāja iestatīšana risinājumam Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a6920-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
