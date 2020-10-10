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
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b26b6e1e50e5a9b53ca6b5315de760f5bcec4769
ms.sourcegitcommit: 74b10104338222a945684d841d60ab4b8e570168
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3899401"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="8c10b-104">Detalizētās bankas darbību saskaņošanas pārskats</span><span class="sxs-lookup"><span data-stu-id="8c10b-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c10b-105">Šajā rakstā ir aprakstīta detalizētās bankas darbību saskaņošanas procesa plūsma.</span><span class="sxs-lookup"><span data-stu-id="8c10b-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="8c10b-106">Detalizētās bankas darbību saskaņošanas līdzeklis jums ļauj importēt bankas izrakstus, kurus var automātiski saskaņot bankas transakciju ietvaros.</span><span class="sxs-lookup"><span data-stu-id="8c10b-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="8c10b-107">Detalizētās bankas darbību saskaņošanas funkcija ļauj importēt banku izrakstus.</span><span class="sxs-lookup"><span data-stu-id="8c10b-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="8c10b-108">Pēc tam importēto bankas izrakstu var automātiski saskaņot no bankas transakciju vides.</span><span class="sxs-lookup"><span data-stu-id="8c10b-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="8c10b-109">Šeit aprakstīti soļi detalizētās bankas darbību saskaņošanas plūsmā.</span><span class="sxs-lookup"><span data-stu-id="8c10b-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="8c10b-110">Iestatiet bankas izraksta importēšanu.</span><span class="sxs-lookup"><span data-stu-id="8c10b-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="8c10b-111">Importējiet bankas izrakstus, izmantojot datu elementu struktūru.</span><span class="sxs-lookup"><span data-stu-id="8c10b-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="8c10b-112">Ir iebūvēti trīs tipiski bankas izrakstu formāti: ISO20022, BAI2 un MT940.</span><span class="sxs-lookup"><span data-stu-id="8c10b-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="8c10b-113">Šī funkcionalitāte var tikt paplašināta uz jebkuru formātu.</span><span class="sxs-lookup"><span data-stu-id="8c10b-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="8c10b-114">Iestatiet numuru sēriju, kuru lietot detalizētajai bankas darbību saskaņošanai un definējiet bankas darbību saskaņošanas atbilstības kārtulas.</span><span class="sxs-lookup"><span data-stu-id="8c10b-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="8c10b-115">Saskaņošanas atbilstības kārtula ir kritēriju kopa, kas tiek izmantota, lai filtrētu bankas izrakstu rindas un Microsoft Dynamics 365 Finance bankas transakciju rindas saskaņošanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="8c10b-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 Finance bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="8c10b-116">Atkarībā no jūsu biznesa prakses varat iestatīt vairākas atbilstības kārtulas, lai automatizētu un optimizētu saskaņošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="8c10b-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="8c10b-117">Saskaņojiet bankas izrakstus ar finanšu bankas transakcijām.</span><span class="sxs-lookup"><span data-stu-id="8c10b-117">Reconcile bank statements with Finance bank transactions.</span></span>
    -   <span data-ttu-id="8c10b-118">Veiciet automātisku atbilstības noteikšanu un saskaņošanas žurnālu izveidi.</span><span class="sxs-lookup"><span data-stu-id="8c10b-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="8c10b-119">Skatiet bankas izrakstus un finanšu bankas transakcijas vienu otram līdzās.</span><span class="sxs-lookup"><span data-stu-id="8c10b-119">View bank statements and Finance bank transactions side by side.</span></span>
    -   <span data-ttu-id="8c10b-120">Automātiski grāmatojiet finanšu bankas transakcijas, ja tās ir ietvertas bankas izrakstā, taču nav redzamas programmā Finance.</span><span class="sxs-lookup"><span data-stu-id="8c10b-120">Automatically post Finance bank transactions if they appear on a bank statement but don't appear in the Finance app.</span></span>
    -   <span data-ttu-id="8c10b-121">Izveidojiet saskaņošanas paziņojumu.</span><span class="sxs-lookup"><span data-stu-id="8c10b-121">Generate a reconciliation statement.</span></span>





