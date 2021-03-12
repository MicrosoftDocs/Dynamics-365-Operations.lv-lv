---
title: Detalizētās bankas darbību saskaņošanas pārskats
description: Šajā rakstā ir aprakstīta detalizētās bankas darbību saskaņošanas procesa plūsma. Detalizētās bankas darbību saskaņošanas līdzeklis jums ļauj importēt bankas izrakstus, kurus var automātiski saskaņot bankas transakciju ietvaros.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09128f33d4208bc5c987683bb881aa1129b0dc8e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985440"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="0c9e2-104">Detalizētās bankas darbību saskaņošanas pārskats</span><span class="sxs-lookup"><span data-stu-id="0c9e2-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c9e2-105">Šajā rakstā ir aprakstīta detalizētās bankas darbību saskaņošanas procesa plūsma.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="0c9e2-106">Detalizētās bankas darbību saskaņošanas līdzeklis jums ļauj importēt bankas izrakstus, kurus var automātiski saskaņot bankas transakciju ietvaros.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="0c9e2-107">Detalizētās bankas darbību saskaņošanas funkcija ļauj importēt banku izrakstus.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="0c9e2-108">Pēc tam importēto bankas izrakstu var automātiski saskaņot no bankas transakciju vides.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="0c9e2-109">Šeit aprakstīti soļi detalizētās bankas darbību saskaņošanas plūsmā.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="0c9e2-110">Iestatiet bankas izraksta importēšanu.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="0c9e2-111">Importējiet bankas izrakstus, izmantojot datu elementu struktūru.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="0c9e2-112">Ir iebūvēti trīs tipiski bankas izrakstu formāti: ISO20022, BAI2 un MT940.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="0c9e2-113">Šī funkcionalitāte var tikt paplašināta uz jebkuru formātu.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="0c9e2-114">Iestatiet numuru sēriju, kuru lietot detalizētajai bankas darbību saskaņošanai un definējiet bankas darbību saskaņošanas atbilstības kārtulas.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="0c9e2-115">Saskaņošanas atbilstības kārtula ir kritēriju kopa, kas tiek izmantota, lai filtrētu bankas izrakstu rindas un Microsoft Dynamics 365 Finance bankas transakciju rindas saskaņošanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 Finance bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="0c9e2-116">Atkarībā no jūsu biznesa prakses varat iestatīt vairākas atbilstības kārtulas, lai automatizētu un optimizētu saskaņošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="0c9e2-117">Saskaņojiet bankas izrakstus ar finanšu bankas transakcijām.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-117">Reconcile bank statements with Finance bank transactions.</span></span>
    -   <span data-ttu-id="0c9e2-118">Veiciet automātisku atbilstības noteikšanu un saskaņošanas žurnālu izveidi.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="0c9e2-119">Skatiet bankas izrakstus un finanšu bankas transakcijas vienu otram līdzās.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-119">View bank statements and Finance bank transactions side by side.</span></span>
    -   <span data-ttu-id="0c9e2-120">Automātiski grāmatojiet finanšu bankas transakcijas, ja tās ir ietvertas bankas izrakstā, taču nav redzamas programmā Finance.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-120">Automatically post Finance bank transactions if they appear on a bank statement but don't appear in the Finance app.</span></span>
    -   <span data-ttu-id="0c9e2-121">Izveidojiet saskaņošanas paziņojumu.</span><span class="sxs-lookup"><span data-stu-id="0c9e2-121">Generate a reconciliation statement.</span></span>





