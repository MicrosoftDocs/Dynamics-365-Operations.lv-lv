---
title: Finanšu žurnālu veidņu atvēršana sistēmā Office
description: Šajā tēmā aprakstītas problēmas, kas var rasties, veidojot pielāgotus finanšu žurnālus, izmantojot Microsoft Excel veidni.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089461"
---
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="7d4dd-103">Finanšu žurnālu veidņu atvēršana sistēmā Office</span><span class="sxs-lookup"><span data-stu-id="7d4dd-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d4dd-104">Šajā tēmā aprakstītas problēmas, kas var rasties, veidojot pielāgotus finanšu žurnālus, izmantojot Microsoft Excel veidni.</span><span class="sxs-lookup"><span data-stu-id="7d4dd-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="7d4dd-105">Simptoms</span><span class="sxs-lookup"><span data-stu-id="7d4dd-105">Symptom</span></span>

<span data-ttu-id="7d4dd-106">Jūs izveidojāt pielāgotu Excel veidni finanšu žurnāliem, bet tā neparādās izvēlnē **Atvērt rindas programmā Excel**.</span><span class="sxs-lookup"><span data-stu-id="7d4dd-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="7d4dd-107">Vai arī tā parādās izvēlnē, tiek atvērta cita veidne, bet, kad to atlasāt.</span><span class="sxs-lookup"><span data-stu-id="7d4dd-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="7d4dd-108">Novēršana</span><span class="sxs-lookup"><span data-stu-id="7d4dd-108">Resolution</span></span>

<span data-ttu-id="7d4dd-109">Noklusējuma funkcionalitāte Atvērt programmā Excel izmanto pašreizējās lapas saknes datu avotu (tabulu), lai noteiktu, kuras Office veidnes vai datu elementi tiek parādīti kā opcijas izvēlnē **Atvērt programmā Excel**.</span><span class="sxs-lookup"><span data-stu-id="7d4dd-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="7d4dd-110">Šī darbība nav ideāla pieredze finanšu žurnāliem, jo finanšu žurnāli izmanto tās pašas tabulas (LedgerJournalTable un LedgerJournalTrans) kā daudzu citu žurnālu tipu saknes datu avotu.</span><span class="sxs-lookup"><span data-stu-id="7d4dd-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="7d4dd-111">Finanšu žurnāliem funkcionalitāte Atvērt rindas programmā Excel ir paredzēta, lai parādītu veidnes, kas ir paredzētas žurnālam, kurā pašlaik strādājat, piemēram, virsgrāmatas žurnāla vai maksājumu žurnāla kontekstā.</span><span class="sxs-lookup"><span data-stu-id="7d4dd-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="7d4dd-112">Piemēram, veidne, ko ir paredzēts izmantot ar kreditoru maksājumu žurnālu, tiks izveidota, lai ieviestu jūsu primāro kontu kā kreditoru kontu.</span><span class="sxs-lookup"><span data-stu-id="7d4dd-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="7d4dd-113">Ja vēlaties paaugstināt veidni tā, lai tā būtu pieejama izvēlnēs **Atvērt rindas programmā Excel** un **Atvērt programmā Excel** vienkārša izstrādātāja pieredze ir ieviest **LedgerIJournalExcelTemplate** interfeisu un paplašināt **DocuTemplateRegistrationBase** klasi.</span><span class="sxs-lookup"><span data-stu-id="7d4dd-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="7d4dd-114">Daudzi šīs pieejas piemēri ir ieviesti sistēmā.</span><span class="sxs-lookup"><span data-stu-id="7d4dd-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="7d4dd-115">Viens piemērs, ko var izmantot atsaucei, ir Virsgrāmatas Žurnālam (vai ikdienas žurnālam) izveidotais **LedgerDailyJournalExcelTemplate** interfeiss.</span><span class="sxs-lookup"><span data-stu-id="7d4dd-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="7d4dd-116">Kad veidnei ir ieviests **LedgerIJournalExcelTemplate** interfeiss, izvēlnē **Atvērt rindas programmā Excel** veidnes tiks filtrētas pēc jūsu žurnāla tipa, kā arī tiks rādītas tikai šim žurnālam pieejamās veidnes.</span><span class="sxs-lookup"><span data-stu-id="7d4dd-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="7d4dd-117">Interfeiss nodrošina arī validācijas metodi, kas nodrošina, ka veidni nevar atvērt žurnālam, ja tā neatbilst konta tipa prasībām.</span><span class="sxs-lookup"><span data-stu-id="7d4dd-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="7d4dd-118">Piemēram, varat norādīt, ka konta tipam jābūt **Kreditors** vai **Virsgrāmata**.</span><span class="sxs-lookup"><span data-stu-id="7d4dd-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="7d4dd-119">Lai iegūtu papildinformāciju par šo funkcionalitāti, skatiet rakstu [Veidņu pievienošana izvēlnei Atvērt rindas programmā Excel](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span><span class="sxs-lookup"><span data-stu-id="7d4dd-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>
