---
title: Rēķinu atjauninājumu veikšana atgrieztajiem krājumiem
description: Šī funkcionalitāte atbalsta uzņēmējdarbības procesus daudzās organizācijās, kas izvēlas vienlaicīgu rēķinu izrakstīšanu atgriešanas pasūtījumiem un pārdošanas pasūtījumiem, un to veic viens darbinieks.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d60e29aec1ebdec939aaafc978ee4de04b96136
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983847"
---
# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="b58aa-103">Rēķinu atjauninājumu veikšana atgrieztajiem krājumiem</span><span class="sxs-lookup"><span data-stu-id="b58aa-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b58aa-104">Atgriešanas pasūtījums ir pārdošanas pasūtījuma veids, kas ir atzīmēts kā atgriešanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="b58aa-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="b58aa-105">Tādēļ atgriešanas pasūtījumu rēķinu ģenerēšanai tiek izmantota saraksta lapa **Visi pārdošanas pasūtījumi**, nevis veidlapa **Atgriešanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="b58aa-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="b58aa-106">Šī funkcionalitāte atbalsta uzņēmējdarbības procesus daudzās organizācijās, kas izvēlas vienlaicīgu rēķinu izrakstīšanu atgriešanas pasūtījumiem un pārdošanas pasūtījumiem, un to veic viens darbinieks.</span><span class="sxs-lookup"><span data-stu-id="b58aa-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="b58aa-107">Tā kā atgriezta krājuma rēķinā ir negatīva summu, to sauc par kredīta notu.</span><span class="sxs-lookup"><span data-stu-id="b58aa-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="b58aa-108">Kad tiek iestatīta rēķina atjaunināšana pakešuzdevumu apstrādei, pārdošanas pasūtījumam, kura tips ir **Atgriešanas pasūtījums**, ir jāatgriež statuss **Saņemts**, kas norāda, ka pasūtījuma pavadzīme tikusi atjaunināta.</span><span class="sxs-lookup"><span data-stu-id="b58aa-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="b58aa-109">Rēķina par atgriešanas pasūtījumu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="b58aa-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="b58aa-110">Noklikšķiniet uz **Debitoru parādi** \> **Vispārīgi** \> **Pārdošanas pasūtījumi** \> **Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="b58aa-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="b58aa-111">Atlasiet pārdošanas pasūtījumu, kuram laukā **Pasūtījuma tips** tiek rādīts vienums **Atgriešanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="b58aa-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="b58aa-112">Darbību rūtī, cilnē **Rēķins**, grupā **Ģenerēt** noklikšķiniet uz **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="b58aa-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="b58aa-113">Cilnē **Parametri** atzīmējiet izvēles rūtiņu **Grāmatošana**.</span><span class="sxs-lookup"><span data-stu-id="b58aa-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="b58aa-114">Pārskatiet informāciju veidlapā un veiciet nepieciešamās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="b58aa-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="b58aa-115">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b58aa-115">Click **OK**.</span></span> <span data-ttu-id="b58aa-116">Kredīta nota ir grāmatota.</span><span class="sxs-lookup"><span data-stu-id="b58aa-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="b58aa-117">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="b58aa-117">See also</span></span>

[<span data-ttu-id="b58aa-118">Pavadzīmju atjauninājumi atgrieztajiem krājumiem</span><span class="sxs-lookup"><span data-stu-id="b58aa-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  


