---
title: Iespējot debitora atdošanas paziņojumus pārdošanas punktā (POS)
description: Šajā tēmā ir aprakstīts, kā iespējot debitoru atdošanas paziņojumus Microsoft Dynamics 365 Commerce pārdošanas punktā (POS).
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e4defc15d9ef198a361934d51e31016747dbb5ab
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937600"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="69c77-103">Iespējot debitora atdošanas paziņojumus pārdošanas punktā (POS)</span><span class="sxs-lookup"><span data-stu-id="69c77-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="69c77-104">Šajā tēmā ir aprakstīts, kā iespējot debitoru atdošanas paziņojumus Microsoft Dynamics 365 Commerce pārdošanas punktā (POS).</span><span class="sxs-lookup"><span data-stu-id="69c77-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="69c77-105">Organizācijas savos e-pasta ziņojumos "pasūtījums ir gatavs savākšanai", var nodrošināt saiti vai pogu, kas ļauj debitoriem paziņot veikalam, ka viņi atrodas uz vietas, un gaida, kad viņu pakotne tiks iznesta.</span><span class="sxs-lookup"><span data-stu-id="69c77-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="69c77-106">Pēc tam debitori saņem reģistrēšanās apstiprinājumu, un veikals savā POS programmā saņem paziņojumu kā uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="69c77-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="69c77-107">Šis uzdevums kalpo kā uzvedne pārdošanas piesaistēm, lai piegādātu pasūtījumu debitoram transportlīdzeklim.</span><span class="sxs-lookup"><span data-stu-id="69c77-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="69c77-108">Tādēļ debitoram nav jāievada veikals.</span><span class="sxs-lookup"><span data-stu-id="69c77-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="69c77-109">Debitora reģistrēšanās darbplūsmu var konfigurēt, lai apkopotu papildu informāciju no debitoriem, piemēram, viņu stāvvietas numuru, transportlīdzekļa izgatavotāju, modeli un krāsu un piegādes instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="69c77-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="69c77-110">Mazumtirdzniecības veikala grāmatvedis var izmantot šo informāciju, lai atvieglotu pasūtījuma izpildi.</span><span class="sxs-lookup"><span data-stu-id="69c77-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="69c77-111">Iespējot debitora atdošanu</span><span class="sxs-lookup"><span data-stu-id="69c77-111">Enable customer check-in</span></span>

<span data-ttu-id="69c77-112">Ja debitora reģistrēšanās līdzeklis ir ieslēgts, Commerce ģenerē pasūtījuma apstiprinājuma ID (zināms arī kā kanāla atsauces ID).</span><span class="sxs-lookup"><span data-stu-id="69c77-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="69c77-113">Tas ģenerē arī pasūtījumu apstiprinājumu ID pasūtījumiem, kas ir izveidoti, izmantojot pārdošanas punkta (POS) vai zvanu centra kanālus.</span><span class="sxs-lookup"><span data-stu-id="69c77-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="69c77-114">Lai ieslēgtu debitoru atdošanas līdzeki Commerce Headquarters, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="69c77-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="69c77-115">Dodieties uz **Darbvietas \> Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="69c77-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="69c77-116">Meklējiet līdzekli **Izveidot konsekventu kanāla atsauces ID formātu vairākos kanālos**.</span><span class="sxs-lookup"><span data-stu-id="69c77-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="69c77-117">Atlasiet līdzekli un pēc tam rekvizītu rūtī atlasiet **Iespējot tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="69c77-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="69c77-118">Izveidot atdošanas apstiprināšanas lapu</span><span class="sxs-lookup"><span data-stu-id="69c77-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="69c77-119">Jūsu e-komercijas vietnē jums ir jāizveido jauna lapa, kas kalpos kā pārbaudes apstiprinājumu pieredze.</span><span class="sxs-lookup"><span data-stu-id="69c77-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="69c77-120">Izmantojot papildu konfigurāciju, lapa var arī iekļaut formu, kas ievāc papildu informāciju no debitoriem, lai atvieglotu pasūtījuma izpildi.</span><span class="sxs-lookup"><span data-stu-id="69c77-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="69c77-121">Papildinformāciju par lapas un moduļa iestatīšanas veidu skatiet [Debitoru atdošanas modulī](check-in-pickup-module.md).</span><span class="sxs-lookup"><span data-stu-id="69c77-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="69c77-122">Transakciju e-pasta veidnes konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="69c77-122">Configure the transactional email template</span></span>

<span data-ttu-id="69c77-123">Šeit ir jāpievieno **Esmu šeit** saite vai poga veidnei, kas ir pieejama transakciju e-pasta ziņojumā, ko debitori saņem, kad viņu pasūtījums ir gatavs saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="69c77-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="69c77-124">Debitori izmantos šo saiti vai pogu, lai paziņotu veikalam, ka ir atnākuši saņemt pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="69c77-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="69c77-125">Pievienojiet saiti vai pogu veidnei, kas ir kartēta uz paziņojuma veidu **Iepakošanas pabeigšana** un piegādes veidu, ko izmantojat, lai novērstu pasūtījuma izpildi.</span><span class="sxs-lookup"><span data-stu-id="69c77-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="69c77-126">Veidnē izveidojiet HTML saiti vai pogu, kas norāda uz jūsu izveidotās apstiprināšanas lapas URL.</span><span class="sxs-lookup"><span data-stu-id="69c77-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="69c77-127">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="69c77-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="69c77-128">Papildinformāciju par e-pasta veidņu konfigurēšanu skatiet sadaļā [Transakciju e-pasta ziņojumu pielāgošana piegādes režīmā](customize-email-delivery-mode.md).</span><span class="sxs-lookup"><span data-stu-id="69c77-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="69c77-129">POS ir izveidots pārbaudes apstiprināšanas uzdevums</span><span class="sxs-lookup"><span data-stu-id="69c77-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="69c77-130">Kad debitors paziņo veikalam, ka ir klāt saņemšanai, viņi saņem saņemšanas apstiprinājuma paziņojumu, un uzdevums tiek izveidots uzdevumu sarakstā POS veikalam, kur debitors saņem pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="69c77-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="69c77-131">Uzdevumā ietverta visa informācija par debitoru un pasūtījumu, kas nepieciešama pasūtījuma izpildei.</span><span class="sxs-lookup"><span data-stu-id="69c77-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="69c77-132">Uzdevumu norādījumu laukā ir parādīta jebkura informācija, kas apkopota no debitora, izmantojot papildinformācijas formu.</span><span class="sxs-lookup"><span data-stu-id="69c77-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="69c77-133">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="69c77-133">Additional resources</span></span>

[<span data-ttu-id="69c77-134">Izdošanas moduļa atdošana</span><span class="sxs-lookup"><span data-stu-id="69c77-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)
