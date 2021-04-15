---
title: Dynamics 365 Payment Connector Adyen problēmu novēršana
description: Šajā tēmā sniegti norādījumi problēmu novēršanai, kas var palīdzēt, ja jums radušās ar Adyen Microsoft Dynamics 365 Payment Connector.
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
ms.openlocfilehash: c779997d530d60f945bee19ee09bdabbff121fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801823"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="4f139-103">Dynamics 365 Payment Connector Adyen problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="4f139-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4f139-104">Šajā tēmā sniegti norādījumi problēmu novēršanai, kas var palīdzēt, ja jums radušās ar Adyen Microsoft Dynamics 365 Payment Connector.</span><span class="sxs-lookup"><span data-stu-id="4f139-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="4f139-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="4f139-105">Description</span></span>

<span data-ttu-id="4f139-106">Jums ir radušās problēmas ar Adyen Dynamics 365 Payment Connector šādās jomās, un jums ir nepieciešams atbalsts no Adyen komandas:</span><span class="sxs-lookup"><span data-stu-id="4f139-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="4f139-107">Pārdošanas punkta (POS), modernā pārdošanas punkta (MPOS), zvanu centra vai Dynamics 365 Commerce konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="4f139-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="4f139-108">Adyen maksājumu pakalpojumu sniedzēja (PSP) atsauces numurs (piemēram, ja jums radušies jautājumi par atteikumiem, tostarp attiecībā uz manuālo atslēgu ievadi \[MKE\])</span><span class="sxs-lookup"><span data-stu-id="4f139-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="4f139-109">Jebkas, kas nedarbojas testa vai tiešo pārdevēju vidēs</span><span class="sxs-lookup"><span data-stu-id="4f139-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="4f139-110">Novēršana</span><span class="sxs-lookup"><span data-stu-id="4f139-110">Resolution</span></span>

<span data-ttu-id="4f139-111">Izmantojiet šo e-pasta veidni, lai sāktu atbalsta procesu ar Adyen komandu.</span><span class="sxs-lookup"><span data-stu-id="4f139-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="4f139-112">Lai paātrinātu problēmu novēršanu, nodrošiniet, ka e-pastā ir visa nepieciešamā informācija.</span><span class="sxs-lookup"><span data-stu-id="4f139-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="4f139-113">Lauks</span><span class="sxs-lookup"><span data-stu-id="4f139-113">Field</span></span>        | <span data-ttu-id="4f139-114">Vērtība</span><span class="sxs-lookup"><span data-stu-id="4f139-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="4f139-115">Kam</span><span class="sxs-lookup"><span data-stu-id="4f139-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="4f139-116">Kopija</span><span class="sxs-lookup"><span data-stu-id="4f139-116">Cc</span></span>           | |
| <span data-ttu-id="4f139-117">Tēmas rindiņa</span><span class="sxs-lookup"><span data-stu-id="4f139-117">Subject line</span></span> | <span data-ttu-id="4f139-118">Microsoft Dynamics atbalsta pieprasījums</span><span class="sxs-lookup"><span data-stu-id="4f139-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="4f139-119">Pamatteksts</span><span class="sxs-lookup"><span data-stu-id="4f139-119">Body</span></span>         | <p><span data-ttu-id="4f139-120">Sveicināti, Atbalsta komanda,</span><span class="sxs-lookup"><span data-stu-id="4f139-120">Hi Support,</span></span></p><p><span data-ttu-id="4f139-121">Lūdzu, sniedziet atbalstu saistībā ar šādu problēmu:</span><span class="sxs-lookup"><span data-stu-id="4f139-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="4f139-122">Tirgotāja konts</span><span class="sxs-lookup"><span data-stu-id="4f139-122">Merchant account</span></span></li><li><span data-ttu-id="4f139-123">Vide (Testa/Ražošanas)</span><span class="sxs-lookup"><span data-stu-id="4f139-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="4f139-124">Kanāls (POS/zvanu centrs/Commerce e-komercija)</span><span class="sxs-lookup"><span data-stu-id="4f139-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="4f139-125">PSP atsauces numurs, ja rēķins iesaistīts konkrētā transakcijā (PSP numuru varat atrast uz kvīts, Adyen klientu zonā vai POS termināla transakciju izvēlnē.)</span><span class="sxs-lookup"><span data-stu-id="4f139-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="4f139-126">Kļūdas ziņojuma ekrānuzņēmums vai fotoattēls, ja piemērojami.</span><span class="sxs-lookup"><span data-stu-id="4f139-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="4f139-127">Event Viewer žurnāli (.txt formātā)</span><span class="sxs-lookup"><span data-stu-id="4f139-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="4f139-128">Problēmas apraksts un jūsu izmēģinātās problēmu novēršanas darbības</span><span class="sxs-lookup"><span data-stu-id="4f139-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="4f139-129">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4f139-129">Additional resources</span></span>

[<span data-ttu-id="4f139-130">Maksājumu pieņemšana ar Adyen savienotāju Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4f139-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="4f139-131">Dynamics 365 maksājumu savienotājs pakalpojumam Adyen</span><span class="sxs-lookup"><span data-stu-id="4f139-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="4f139-132">Adyen maksājumu savienotāja iestatīšana risinājumam Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4f139-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
