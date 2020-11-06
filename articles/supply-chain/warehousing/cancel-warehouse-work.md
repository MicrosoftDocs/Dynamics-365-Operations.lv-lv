---
title: Atcelt noliktavas darbu izņēmumu apstrādei
description: Šajā tēmā ir aprakstīta funkcionalitāte Atcelt darbu, kas ļauj noliktavas uzraudzītājiem apstrādāt bloķētu darbu.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: daa8f0d19de75e6c126fe7a5fe312bca24c89bdc
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016245"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="b9271-103">Atcelt noliktavas darbu izņēmumu apstrādei</span><span class="sxs-lookup"><span data-stu-id="b9271-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9271-104">Funkcija Atcelt darbu sistēmā Microsoft Dynamics 365 Supply Chain Management ļauj administratoram lietotājam atcelt konkrētu pašlaik notiekošu noliktavas darbu, kuru sistēma ir bloķējusi vai to nevar pabeigt ārkārtēju apstākļu dēļ.</span><span class="sxs-lookup"><span data-stu-id="b9271-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="b9271-105">Šī funkcionalitāte ir pievilcīga un droša alternatīva SQL labojošajiem skriptiem, kas labo nekonsekventus datus.</span><span class="sxs-lookup"><span data-stu-id="b9271-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="b9271-106">Tomēr, tā kā šie skripti parasti tiek pieprasīti no IT profesionāļiem, funkcionalitāti Atcelt darbu var izmantot tie lietotāji uzņēmumā, kam ir administratora tiesības.</span><span class="sxs-lookup"><span data-stu-id="b9271-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="b9271-107">Varat piekļūt funkcionalitātei Atcelt darbu sadaļā **Noliktavas pārvaldība** \> **Periodiskie uzdevumis** \> **Iztīrīt \> Atcelt darbu**.</span><span class="sxs-lookup"><span data-stu-id="b9271-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="b9271-108">Dialoglodziņā **Atcelt darbu** norādiet darba ID darbam, kas jāatceļ, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b9271-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="b9271-109">Noliktavas darbs, kuru var atcelt</span><span class="sxs-lookup"><span data-stu-id="b9271-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="b9271-110">Veicot noliktavas izdošanas darbības, darbinieks var saskarties ar situācijām, kad tiem ir reģistrēti daudzumi kā izdoti no glabāšanas vietas uz to lietotāja atrašanās vietu, taču tad tie nevar reģistrēt izvietošanas darbību.</span><span class="sxs-lookup"><span data-stu-id="b9271-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="b9271-111">Nekonsekventi noliktavas dati bieži, bet ne vienmēr, ir iemesls, kāpēc darbs tiek bloķēts.</span><span class="sxs-lookup"><span data-stu-id="b9271-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="b9271-112">Atšķirībā no parastās atcelšanas funkcionalitātes, kam var piekļūt, izmantojot pogu **Atcelt** darba virsrakstā, funkcionalitātei Atcelt darbu nav nepieciešams, lai pēdējā pabeigtā darba rinda būtu **izvietošanas** veida darba rinda.</span><span class="sxs-lookup"><span data-stu-id="b9271-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="b9271-113">Citiem vārdiem sakot, funkcionalitātei Atcelt darbu atcelšanas loģiku var palaist pat tad, ja krājuma daudzums darba rindā ir lietotāja atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="b9271-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="b9271-114">Darbam, kas jāatceļ operatīvu iemeslu dēļ, noliktavas lietotājiem ir jāturpina izmantot parasto atcelšanas funkcionalitāti darba lapā.</span><span class="sxs-lookup"><span data-stu-id="b9271-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="b9271-115">Izmantojot funkcionalitāti Atcelt darbu, var atcelt tikai **Pārdošanas** , **Izsniegšanas pārsūtīšanai** , **Izejmateriālu izdošanas** vai **Papildināšanas** veida darbu.</span><span class="sxs-lookup"><span data-stu-id="b9271-115">Only work of the **Sales** , **Transfer issue** , **Raw material picking** , or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="b9271-116">Atcelšanas loģika netiks palaista iesaldētam izejmateriālu izdošanas darbam vai darbam, ko var atcelt, lietojot parasto atcelšanas funkcionalitāti (sk. iepriekšējo piezīmi).</span><span class="sxs-lookup"><span data-stu-id="b9271-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="b9271-117">Lai atbloķētu darbu, sistēma atceļ visas atlikušās darba rindas un labo noliktavas datus, kas ir saistīti ar lietotāja norādīto darba ID.</span><span class="sxs-lookup"><span data-stu-id="b9271-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="b9271-118">Pēc tam var atsākt visas parastās noliktavas apstrādes darbības, kas ietver ietekmēto vienību daudzumu.</span><span class="sxs-lookup"><span data-stu-id="b9271-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="b9271-119">Lai ietekmēto vienību izvietotu noteiktā vietā pēc darba atcelšanas, lietotājam jāizmanto krājumu kustība vai daudzuma korekcijas operācija mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="b9271-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>
