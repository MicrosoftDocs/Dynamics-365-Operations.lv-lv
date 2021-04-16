---
title: Hibrīdie debitoru pasūtījumi
description: Hibrīds debitora pasūtījums ir atsevišķs pasūtījums, kurā ir ietvertas gan tādas preces, ko debitors var iznest no veikala, gan tādas, kas tiks izdots vai nosūtītas vēlāk.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6357c034059523f83ba05a1da53cae691ef74758
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798941"
---
# <a name="hybrid-customer-orders"></a><span data-ttu-id="290f1-103">Hibrīdie debitoru pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="290f1-103">Hybrid customer orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="290f1-104">Hibrīds debitora pasūtījums ir atsevišķs pasūtījums, kurā ir ietvertas gan tādas preces, ko debitors var iznest no veikala, gan tādas, kas tiks izdots vai nosūtītas vēlāk.</span><span class="sxs-lookup"><span data-stu-id="290f1-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="290f1-105">Commerce debitora pasūtījumam varat atlasīt opciju iznest visas preces vai iznest atlasītās preces.</span><span class="sxs-lookup"><span data-stu-id="290f1-105">In Commerce, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="290f1-106">Par preču grupām, kas ir atzīmētas kā iznesamas, tiek automātiski izrakstīts rēķins uzreiz pēc pasūtījuma izveides. Tas pats pēc pasūtījuma izveides tiek darīts arī ar izdodamām precēm.</span><span class="sxs-lookup"><span data-stu-id="290f1-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="290f1-107">Hibrīdo pasūtījumu apmaksas summa tiek aprēķināta, saskaitot izdodamo un nosūtāmo preču rindu depozīta procentu summu un iznesamo preču rindu pilnu summu.</span><span class="sxs-lookup"><span data-stu-id="290f1-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="290f1-108">Apstrādājot hibrīdos pasūtījumus, sistēma pārslēdz debitora pasūtījumu režīmu un pārdošanas skaidrā naudā bez piegādes režīmiem tālāk norādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="290f1-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

- <span data-ttu-id="290f1-109">Ja visām grozā esošajām precēm ir iestatīta opcija **Piegāde iznesot**, pasūtījums tiek apstrādāts kā pārdošanas skaidrā naudā bez piegādes transakcija.</span><span class="sxs-lookup"><span data-stu-id="290f1-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
- <span data-ttu-id="290f1-110">Ja vienai vai visām groza rindām ir iestatīta opcija **Piegāde izdodot** vai **Piegāde nosūtot**, pasūtījums tiek apstrādāts kā debitora pasūtījuma transakcija.</span><span class="sxs-lookup"><span data-stu-id="290f1-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="290f1-111">Ja tiek atlasīta kāda groza rinda un tiek atlasīta opcija **Izdot atlasīto**, **Nosūtīt atlasīto** vai **Iznest atlasīto**, attiecīgā piegādes metode tiek iestatīta tikai atlasītajai groza rindai.</span><span class="sxs-lookup"><span data-stu-id="290f1-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="290f1-112">Šādā gadījumā operācijas lejupstraumes plūsma turpinās kā parasti.</span><span class="sxs-lookup"><span data-stu-id="290f1-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="290f1-113">Taču, ja opcija **Izdot atlasīto**, **Nosūtīt atlasīto** vai **Iznest atlasīto** tiek atlasīta, neatlasot nevienu groza rindu, tiek atvērta jauna lapa, kurā ir norādītas visas groza rindas.</span><span class="sxs-lookup"><span data-stu-id="290f1-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="290f1-114">Šajā ekrānā varat vienlaikus atlasīt vairākas rindas, kam ir jāiestata attiecīgā piegādes metode.</span><span class="sxs-lookup"><span data-stu-id="290f1-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="290f1-115">Ja izmantojat rindu atlases metodi, tiek pārrakstīta jebkura rindai iepriekš piešķirtā piegādes metode.</span><span class="sxs-lookup"><span data-stu-id="290f1-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="290f1-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="290f1-116">Additional resources</span></span>

[<span data-ttu-id="290f1-117">Debitoru pasūtījumi Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="290f1-117">Customer orders in Modern POS (MPOS)</span></span>](customer-orders-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]