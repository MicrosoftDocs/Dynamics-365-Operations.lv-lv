---
title: Izdošanas moduļa atdošana
description: Šis temats attiecas uz izdošanas moduļa atdošanu un tajā tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e7bae4ae7c2f3367132b03accb31c01c5f3b673e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937601"
---
# <a name="check-in-for-pickup-module"></a><span data-ttu-id="be004-103">Izdošanas moduļa atdošana</span><span class="sxs-lookup"><span data-stu-id="be004-103">Check-in for pickup module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="be004-104">Šis temats attiecas uz izdošanas moduļa atdošanu un tajā tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="be004-104">This topic covers the check-in for pickup module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="be004-105">Izdošanas moduļa atdošana nodrošina apstiprinājuma lapu klientiem, kuri izmanto Dynamics 365 Commerce klientu izdošanas iespējas, lai paziņotu veikalam par to ierašanos.</span><span class="sxs-lookup"><span data-stu-id="be004-105">The check-in for pickup module provides a confirmation page for customers who use the Dynamics 365 Commerce customer check-in capabilities to notify a store about their arrival.</span></span> <span data-ttu-id="be004-106">Izdošanas moduļa atdošana arī ļauj konfigurēt veidlapu, kas ievāc papildu informāciju no debitoriem, lai atvieglotu pasūtījuma piegādi.</span><span class="sxs-lookup"><span data-stu-id="be004-106">The check-in for pickup module also lets you configure a form that collects additional information from customers to facilitate order delivery.</span></span> <span data-ttu-id="be004-107">Šī informācija ietver debitora auto novietošanas vietas numuru un tā transportlīdzekļa izgatavotāju un modeli.</span><span class="sxs-lookup"><span data-stu-id="be004-107">This information includes a customer's parking spot number, and the make and model of their vehicle.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="be004-108">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="be004-108">Module properties</span></span>

| <span data-ttu-id="be004-109">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="be004-109">Property name</span></span> | <span data-ttu-id="be004-110">Vērtības</span><span class="sxs-lookup"><span data-stu-id="be004-110">Values</span></span> | <span data-ttu-id="be004-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="be004-111">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="be004-112">Apstiprinājuma teksts</span><span class="sxs-lookup"><span data-stu-id="be004-112">Confirmation text</span></span> | <span data-ttu-id="be004-113">Teksta virkne</span><span class="sxs-lookup"><span data-stu-id="be004-113">Text string</span></span> | <span data-ttu-id="be004-114">Virsraksta saturs, kas tiek parādīts atdošanas apstiprināšanas lapā.</span><span class="sxs-lookup"><span data-stu-id="be004-114">Content for the heading that appears on the check-in confirmation page.</span></span> |
| <span data-ttu-id="be004-115">Rādīt QR kodu</span><span class="sxs-lookup"><span data-stu-id="be004-115">Show QR code</span></span> | <span data-ttu-id="be004-116">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="be004-116">**True** or **False**</span></span> | <span data-ttu-id="be004-117">Ja šis rekvizīts ir iestatīts kā **Patiess**, atdošanas apstiprināšanas lapa rāda QR kodu, kas norāda pasūtījuma apstiprinājuma ID.</span><span class="sxs-lookup"><span data-stu-id="be004-117">When this property is set to **True**, the check-in confirmation page shows a QR code that represents the order confirmation ID.</span></span> |
| <span data-ttu-id="be004-118">Papildinformācijas virsraksts</span><span class="sxs-lookup"><span data-stu-id="be004-118">Additional information heading</span></span> | <span data-ttu-id="be004-119">Teksta virkne</span><span class="sxs-lookup"><span data-stu-id="be004-119">Text string</span></span> | <span data-ttu-id="be004-120">Virsraksta saturs, kas tiek parādīts, konfigurējot papildu informācijas laukus.</span><span class="sxs-lookup"><span data-stu-id="be004-120">Content for the heading that appears when additional information fields have been configured.</span></span> |
| <span data-ttu-id="be004-121">Papildinformācijas atslēgas</span><span class="sxs-lookup"><span data-stu-id="be004-121">Additional information keys</span></span> | <span data-ttu-id="be004-122">Resursa ID/resursu vērtību pāris</span><span class="sxs-lookup"><span data-stu-id="be004-122">Resource ID/resource value pair</span></span> | <span data-ttu-id="be004-123">Katra atslēga izveido veidlapas lauku un saistīto iezīmi, kas tiek izmantota, lai apkopotu papildinformāciju no debitoriem.</span><span class="sxs-lookup"><span data-stu-id="be004-123">Each key creates a form field and an associated label that are used to collect additional information from customers.</span></span> |
| <span data-ttu-id="be004-124">Papildinformācijas atslēgas \> Resursa ID</span><span class="sxs-lookup"><span data-stu-id="be004-124">Additional information keys \> Resource ID</span></span> | <span data-ttu-id="be004-125">Teksta virkne</span><span class="sxs-lookup"><span data-stu-id="be004-125">Text string</span></span> | <span data-ttu-id="be004-126">Katra informācijas atslēga izveido veidlapas lauku un saistīto iezīmi, kas tiek izmantota, lai apkopotu papildinformāciju no debitoriem.</span><span class="sxs-lookup"><span data-stu-id="be004-126">Each information key creates a form field and an associated label that are used to collect additional information from customers.</span></span> <span data-ttu-id="be004-127">Šis rekvizīts identificē papildinformācijas atslēgu.</span><span class="sxs-lookup"><span data-stu-id="be004-127">This property identifies the additional information key.</span></span> <span data-ttu-id="be004-128">Uzdevumā, kas ir izveidots pārdošanas punktā (POS), šī rekvizīta vērtība tiek parādīta instrukcijas laukā kā etiķete.</span><span class="sxs-lookup"><span data-stu-id="be004-128">In the task that is created in point of sale (POS), the value of this property is shown as the label in the instructions field.</span></span> |
| <span data-ttu-id="be004-129">Papildinformācijas atslēgas \> Resursa vērtība</span><span class="sxs-lookup"><span data-stu-id="be004-129">Additional information keys \> Resource value</span></span> | <span data-ttu-id="be004-130">Teksta virkne</span><span class="sxs-lookup"><span data-stu-id="be004-130">Text string</span></span> | <span data-ttu-id="be004-131">POS uzdevuma teksta lauka iezīme.</span><span class="sxs-lookup"><span data-stu-id="be004-131">The label for the text field in the task in POS.</span></span> |
| <span data-ttu-id="be004-132">Papildinformācijas atslēgas \> Obligāti</span><span class="sxs-lookup"><span data-stu-id="be004-132">Additional information keys \> Required</span></span> | <span data-ttu-id="be004-133">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="be004-133">**True** or **False**</span></span> | <span data-ttu-id="be004-134">Šis rekvizīts norāda, vai pirms turpināšanas debitoriem ir jāaizpilda veidlapas lauks.</span><span class="sxs-lookup"><span data-stu-id="be004-134">This property specifies whether customers must fill in the form field before they can continue.</span></span> <span data-ttu-id="be004-135">Kad šis rekvizīts ir iestatīts uz **Patiess**, līdz veidlapas etiķetei tiek atveidota zvaigznīte, un tiek veikta nulles pārbaude, lai neļautu debitoriem turpināt darbu, ja nav ievadīta vērtība.</span><span class="sxs-lookup"><span data-stu-id="be004-135">When this property is set to **True**, an asterisk is rendered next to the form label, and a null check is done to prevent customers from continuing if no value is entered.</span></span> |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a><span data-ttu-id="be004-136">Izdošanas moduļa atdošanas pievienošana lapai</span><span class="sxs-lookup"><span data-stu-id="be004-136">Add the check-in for pickup module to a page</span></span>

<span data-ttu-id="be004-137">Izdošanas moduļa atdošanu jāpievieno jaunajai lapai, ko izveidojat atdošanas apstiprinājumam.</span><span class="sxs-lookup"><span data-stu-id="be004-137">The check-in for pickup module should be added to the new page that you create for check-in confirmation.</span></span> <span data-ttu-id="be004-138">Šī lapa kalpos kā atdošanas apstiprinājumu pieredze klientiem, kuri atlasīs saiti vai pogu **Esmu šeit** e-pasta ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="be004-138">That page will serve as the check-in confirmation experience for customers who select the **I am here** link or button in their email.</span></span> 

## <a name="configure-the-additional-information-form"></a><span data-ttu-id="be004-139">Papildu informācijas veidlapas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="be004-139">Configure the additional information form</span></span>

<span data-ttu-id="be004-140">Pēc noklusējuma, ja nav konfigurētas papildu informācijas atslēgas, modulis rāda debitoriem atdošanas apstiprināšanas lapu.</span><span class="sxs-lookup"><span data-stu-id="be004-140">By default, if no additional information keys are configured, the module shows customers the check-in confirmation page.</span></span> <span data-ttu-id="be004-141">Kad tiek rādīts atdošanas apstiprinājums, POS tiek izveidots uzdevums veikalam, kur pasūtījums tiek izdots.</span><span class="sxs-lookup"><span data-stu-id="be004-141">As the check-in confirmation is shown, a task is created in POS for the store where the order is being picked up.</span></span>

<span data-ttu-id="be004-142">Konfigurējot vienu vai vairākas informācijas atslēgas, debitoriem vispirms tiek parādīta uzvedne ar aicinājumu ievadīt informāciju.</span><span class="sxs-lookup"><span data-stu-id="be004-142">When one or more additional information keys are configured, customers are first prompted to enter information.</span></span> <span data-ttu-id="be004-143">Kad tiek atlasīts **Iesniegt**, tiem tiek rādīts atdošanas apstiprinājums un POS tiek izveidots uzdevums.</span><span class="sxs-lookup"><span data-stu-id="be004-143">When they select **Submit**, they are shown the check-in confirmation, and a task is created in POS.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="be004-144">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="be004-144">Additional resources</span></span>

[<span data-ttu-id="be004-145">Iespējot debitora atdošanas paziņojumus pārdošanas punktā (POS)</span><span class="sxs-lookup"><span data-stu-id="be004-145">Enable customer check-in notifications in point of sale (POS)</span></span>](enable-customer-check-in.md)
