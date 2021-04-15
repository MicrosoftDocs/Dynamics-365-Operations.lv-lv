---
title: QR koda vai svītrkoda pievienošana transakciju un kvīšu e-pastiem
description: Šajā tēmā paskaidrots, kā ievietot QR kodus un svītrkodus, kuri norāda uz pasūtījuma ID, transakciju un kvīšu e-pastos risinājumā Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: f8d9408090846799c1bb421c4b6e5e248d37fa07
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797507"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a><span data-ttu-id="2c0f2-103">QR koda vai svītrkoda pievienošana transakciju un kvīšu e-pastiem</span><span class="sxs-lookup"><span data-stu-id="2c0f2-103">Add a QR code or bar code to transactional and receipt emails</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="2c0f2-104">Šajā tēmā paskaidrots, kā ievietot QR kodus un svītrkodus, kuri norāda uz pasūtījuma ID, transakciju un kvīšu e-pastos risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-104">This topic explains how to insert QR codes and bar codes that represent order IDs into transactional and receipt emails in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2c0f2-105">Jūs varat viegli iekļaut QR kodus un svītrkodus transakciju e-pastos, lai paātrinātu pasūtījuma uzmeklēšanas procesu mazumtirdzniecības vidē.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-105">You can easily include QR codes and bar codes in transactional emails to help speed up the order lookup process in a retail environment.</span></span> <span data-ttu-id="2c0f2-106">Lai e-pastos ievadītu QR kodus un svītrkodus, jūs izmantojat HTML **\<img\>** atzīmi, kura pieprasa QR koda vai svītrkoda attēlu no ģenerēšanas un atveides pakalpojuma.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-106">To insert QR codes and bar codes into emails, you use an HTML **\<img\>** tag that requests a QR code or bar code image from a generation and rendering service.</span></span> <span data-ttu-id="2c0f2-107">Korporācija Microsoft nenodrošina šo pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-107">Microsoft doesn't provide this service.</span></span> <span data-ttu-id="2c0f2-108">Taču ir daudzi bezmaksas vai izdevīgi pakalpojumi, kuri apkalpo QR kodus vai svītrkodus, kuri tiek dinamiski ģenerēti, balstoties kārtībā, kas tiek padota pieprasījumu virknē.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-108">However, there are many free or inexpensive services that can serve QR codes or bar codes that are dynamically generated based on a value that is passed in a query string.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a><span data-ttu-id="2c0f2-109">QR koda vai svītrkoda pievienošana transakcijas e-pastam</span><span class="sxs-lookup"><span data-stu-id="2c0f2-109">Add a QR code or bar code to a transactional email</span></span>

<span data-ttu-id="2c0f2-110">Lai ievietotu QR kodu vai svītrkodu transakcijas e-pastā, kas tiek izsūtīts kā daļa no e-komercijas pirkuma, izpildiet šīs darbības:</span><span class="sxs-lookup"><span data-stu-id="2c0f2-110">To insert a QR code or bar code into a transactional email that is sent as part of an e-commerce purchase, follow these steps.</span></span>

1. <span data-ttu-id="2c0f2-111">Atveriet transakcijas e-pasta veidnes HTML un pievienojiet HTML **\<img\>** atzīmi, kura norāda uz jūsu QR koda vai svītrkoda pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-111">Open the source HTML for the transactional email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="2c0f2-112">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-112">Here is an example.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    <span data-ttu-id="2c0f2-113">Šeit ir iepriekšējā parauga skaidrojums:</span><span class="sxs-lookup"><span data-stu-id="2c0f2-113">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="2c0f2-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE**  norāda uz jūsu QR koda vai svītrkoda pakalpojuma domēnu.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="2c0f2-115">**dati** ir parametrs, kuru QR koda vai svītrkoda pakalpojums izmanto, lai saņemtu saturu, kuru vajadzētu atveidot kā QR kodu vai svītrkodu.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-115">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="2c0f2-116">Šim parametram ir jāpiešķir vērtība **%salesid%**.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-116">The value **%salesid%** must be assigned to this parameter.</span></span> <span data-ttu-id="2c0f2-117">Ievērojiet, ka šajā piemērā vērtība tiek arī izmantota kā attēla alternatīvais teksts.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-117">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="2c0f2-118">**param1** un **param2** norāda uz papildu, neobligātiem parametriem.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-118">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="2c0f2-119">Dodieties uz **Retail un Commerce \> Galvenās pārvaldes iestatīšana \> Parametri \> Organizācijas e-pastu veidnes** un augšupielādējiet atjaunināto HTML atbilstošajā transakcijas e-pasta veidnē.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the appropriate transactional email template.</span></span>

> [!NOTE]
> <span data-ttu-id="2c0f2-120">Parametri var atšķirties QR koda un svītrkoda pakalpojumu sniedzēju starpā.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-120">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="2c0f2-121">Tāpēc pārliecinieties, ka sazināties ar savu pakalpojumu sniedzēju, lai apstiprinātu parametrus, kuriem jums ir jāpiešķir vērtības.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-121">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a><span data-ttu-id="2c0f2-122">QR koda vai svītrkoda pievienošana kvīts e-pastam</span><span class="sxs-lookup"><span data-stu-id="2c0f2-122">Add a QR code or bar code to a receipt email</span></span> 

<span data-ttu-id="2c0f2-123">Lai ievietotu QR kodu vai svītrkodu kvīts e-pastā, ko var nosūtīt pēc pirkuma veikšanas pārdošanas punktā (POS), izpildiet šīs darbības:</span><span class="sxs-lookup"><span data-stu-id="2c0f2-123">To insert a QR code or bar code into a receipt email that can be sent after a purchase is made at the point of sale (POS), follow these steps.</span></span>

1. <span data-ttu-id="2c0f2-124">Atveriet kvīts e-pasta veidnes HTML un pievienojiet HTML **\<img\>** atzīmi, kura norāda uz jūsu QR koda vai svītrkoda pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-124">Open the source HTML for the receipt email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="2c0f2-125">Tālāk sniegts piemērs.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-125">Here is an example below.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    <span data-ttu-id="2c0f2-126">Šeit ir iepriekšējā parauga skaidrojums:</span><span class="sxs-lookup"><span data-stu-id="2c0f2-126">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="2c0f2-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE**  norāda uz jūsu QR koda vai svītrkoda pakalpojuma domēnu.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="2c0f2-128">**dati** ir parametrs, kuru QR koda vai svītrkoda pakalpojums izmanto, lai saņemtu saturu, kuru vajadzētu atveidot kā QR kodu vai svītrkodu.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-128">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="2c0f2-129">Šim parametram ir jāpiešķir vērtība **%receiptid%**.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-129">The value **%receiptid%** must be assigned to this parameter.</span></span> <span data-ttu-id="2c0f2-130">Ievērojiet, ka šajā piemērā vērtība tiek arī izmantota kā attēla alternatīvais teksts.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-130">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="2c0f2-131">**param1** un **param2** norāda uz papildu, neobligātiem parametriem.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-131">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="2c0f2-132">Dodieties uz **Retail un Commerce \> Galvenās pārvaldes iestatīšana \> Parametri \> Organizācijas e-pastu veidnes** un augšupielādējiet atjaunināto HTML e-pasta veidnē ar e-pasta ID **emailrecpt**.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the email template that has the email ID **emailrecpt**.</span></span>

> [!NOTE]
> <span data-ttu-id="2c0f2-133">Parametri var atšķirties QR koda un svītrkoda pakalpojumu sniedzēju starpā.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-133">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="2c0f2-134">Tāpēc pārliecinieties, ka sazināties ar savu pakalpojumu sniedzēju, lai apstiprinātu parametrus, kuriem jums ir jāpiešķir vērtības.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-134">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c0f2-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2c0f2-135">Additional resources</span></span>

[<span data-ttu-id="2c0f2-136">E-pasta kvīšu sūtīšana no Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="2c0f2-136">Send email receipts from Modern POS (MPOS)</span></span>](email-receipts.md)

[<span data-ttu-id="2c0f2-137">E-pasta ziņojumu veidņu izveide transakciju notikumiem</span><span class="sxs-lookup"><span data-stu-id="2c0f2-137">Create email templates for transactional events</span></span>](email-templates-transactions.md)
