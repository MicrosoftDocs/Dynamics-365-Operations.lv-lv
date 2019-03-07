---
title: Izdevumu pārskati un vairāki apstiprinātāji
description: Šajā tēmā ir sniegta informācija par izdevumu pārskatiem, kuriem ir nepieciešams vairāku personu apstiprinājums.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1483de5405895d60f0cb302ab622758b2b05d2ca
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "362422"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="a124a-103">Izdevumu pārskati un vairāki apstiprinātāji</span><span class="sxs-lookup"><span data-stu-id="a124a-103">Expense reports and multiple approvers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a124a-104">Atkarībā no jūsu organizācijas izdevumu apstiprināšanas politikām darbinieka iesniegto izdevumu pārskatu var būt nepieciešams apstiprināt vairākām personām.</span><span class="sxs-lookup"><span data-stu-id="a124a-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="a124a-105">Iestatot darbplūsmas procesu izdevumu pārskatu apstiprināšanai, varat pievienot darbplūsmas elementus, kas ietver viena vai vairāku izdevumu pārskatu apstiprinātāju veicamos uzdevumus vai darbības.</span><span class="sxs-lookup"><span data-stu-id="a124a-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="a124a-106">Piemēram, var būt nepieciešams, ka visi izdevumu pārskati vispirms jāapstiprina tā darbinieka vadītājam, kurš iesniedza pārskatu, un pēc tam — kreditoru koordinatoram.</span><span class="sxs-lookup"><span data-stu-id="a124a-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="a124a-107">Ja nolemjat, ka nepieciešami vairāki izdevumu pārskatu apstiprinātāji, darbplūsmas elementus var pievienot jebkurā no šiem veidiem:</span><span class="sxs-lookup"><span data-stu-id="a124a-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="a124a-108">Pievienojiet vienu apstiprināšanas elementu, kam ir viena darbība.</span><span class="sxs-lookup"><span data-stu-id="a124a-108">Add one approval element that has one step.</span></span> <span data-ttu-id="a124a-109">Piemēram, darbības izpildei var būt nepieciešams, ka izdevumu pārskats jāpiešķir lietotāju grupai un tas ir jāapstiprina 50 procentiem lietotāju grupas dalībnieku.</span><span class="sxs-lookup"><span data-stu-id="a124a-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="a124a-110">Pievienojiet vienu apstiprināšanas elementu, kam ir vairākas darbības.</span><span class="sxs-lookup"><span data-stu-id="a124a-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="a124a-111">Piemēram, apstiprināšanas elementam var būt šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="a124a-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="a124a-112">Izdevumu pārskatu apstiprina tā darbinieka vadītājs, kurš iesniedza.</span><span class="sxs-lookup"><span data-stu-id="a124a-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="a124a-113">Kreditora darbinieks pārbauda kvītis un izdevumu pārskata krājumus.</span><span class="sxs-lookup"><span data-stu-id="a124a-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="a124a-114">Budžeta īpašnieks apstiprina izdevumu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="a124a-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="a124a-115">Pievienojiet vairākus apstiprināšanas elementus ar vienu darbību katram.</span><span class="sxs-lookup"><span data-stu-id="a124a-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="a124a-116">Piemēram, pievienojiet atsevišķu apstiprināšanas elementu katrai no šīm darbībām:</span><span class="sxs-lookup"><span data-stu-id="a124a-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="a124a-117">Darbinieka vadītājs apstiprina izdevumu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="a124a-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="a124a-118">Budžeta īpašnieks apstiprina izdevumu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="a124a-118">The budget owner approves the expense report.</span></span>
