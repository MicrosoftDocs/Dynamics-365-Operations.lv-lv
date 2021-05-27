---
title: Ierakstīt TDS koncesijas sertifikātu numurus
description: Šajā tēmā skaidrots, kā reģistrēt No kopējās ienākumu summas atskaitītais nodoklis (TDS) koncesijas sertifikātu numurus, kas tiek izsniegti kreditoriem.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023406"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="38fef-103">Ierakstīt TDS koncesijas sertifikātu numurus</span><span class="sxs-lookup"><span data-stu-id="38fef-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38fef-104">Šajā tēmā skaidrots, kā reģistrēt No kopējās ienākumu summas atskaitītais nodoklis (TDS) koncesijas sertifikātu numurus, kas tiek izsniegti kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="38fef-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="38fef-105">Pārejiet uz sadaļu **Nodokļi \> Netiešie nodokļi \> Ieturētais nodoklis \> Ieturētā nodokļa koncesijas**.</span><span class="sxs-lookup"><span data-stu-id="38fef-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="38fef-106">Laukā **Nodokļu tips** atlasiet **TDS**, lai ierakstītu koncesijas sertifikātus TDS nodokļu veidam.</span><span class="sxs-lookup"><span data-stu-id="38fef-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="38fef-107">Cilnē **Pārskats** atlasiet **Alt+N**, lai izveidotu rindu.</span><span class="sxs-lookup"><span data-stu-id="38fef-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="38fef-108">[![Jaunās rindas virsraksts](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="38fef-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="38fef-109">Laukā **Ieturētā nodokļa kods** atlasiet TDS nodokļa kodu, kuram kreditora koncesijas sertifikāti ir izsniegti.</span><span class="sxs-lookup"><span data-stu-id="38fef-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="38fef-110">Lauks **Ieturētā nodokļa koda nosaukums** parāda TDS nodokļa koda nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="38fef-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="38fef-111">Laukos **sākuma datums** un **Beigu datums** definējiet derīguma termiņu koncesijas sertifikātam, kas izmanto TDS nodokļu kodu, lai piegādātājam aprēķinātu TDS, pamatojoties uz koncesiju.</span><span class="sxs-lookup"><span data-stu-id="38fef-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="38fef-112">Laukā **Piezīmes** ievadiet visas piezīmes.</span><span class="sxs-lookup"><span data-stu-id="38fef-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="38fef-113">Laukā **Sadaļa** ievadiet juridiskās sadaļas kodu, kurā ir pieejams TDS koncesijas sertifikāts.</span><span class="sxs-lookup"><span data-stu-id="38fef-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="38fef-114">Ja sadaļas kods ir 197, vērtība "A" tiek parādīta gan formas 26Q kolonnā "Iemesls neatskaitīšanai / mazāka atskaitīšana", gan formas 27Q kolonnā "Iemesls neatskaitīšanai / mazāka atskaitīšana / bruto palielināšana (ja tāds ir)".</span><span class="sxs-lookup"><span data-stu-id="38fef-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="38fef-115">Ja sadaļas kods ir 197A, vērtība "B" ir redzama abās šajās vietās.</span><span class="sxs-lookup"><span data-stu-id="38fef-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="38fef-116">Atlasiet kopsavilkuma cilni **Sertifikāts**, lai ierakstītu TDS koncesijas sertifikātu numurus kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="38fef-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="38fef-117">Laukā **Kreditora konts** atlasiet kreditora kontu, kuram ir izsniegts TDS koncesijas sertifikāts.</span><span class="sxs-lookup"><span data-stu-id="38fef-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="38fef-118">Laukos **sākuma datums** un **Beigu datums** definējiet TDS koncesijas sertifikāta derīguma termiņu.</span><span class="sxs-lookup"><span data-stu-id="38fef-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="38fef-119">TDS aprēķināšana koncesionālā veidā ir balstīta uz periodu, kad kreditoram tiek izveidots sertifikāts.</span><span class="sxs-lookup"><span data-stu-id="38fef-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="38fef-120">Laukā **Sertifikāts** ievadiet TDS koncesijas sertifikāta numuru.</span><span class="sxs-lookup"><span data-stu-id="38fef-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="38fef-121">[![Sertifikāta kopsavilkuma cilne](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="38fef-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="38fef-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="38fef-122">Close the page.</span></span>
