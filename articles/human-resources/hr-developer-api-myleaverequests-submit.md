---
title: Atvaļinājuma pieprasījuma iesniegšana darbplūsmai
description: Programmā Microsoft Dynamics 365 Human Resources, varat izmantot MyLeaveRequests iesniegt () lietojumprogrammu programmēšanas interfeiss (API), lai darbplūsmā iesniegtu atvaļinājuma pieprasījumu.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aeb3d66ad24f96efea1b0ea9828a537f8853c94b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465490"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="27ea3-103">Atvaļinājuma pieprasījuma iesniegšana darbplūsmai</span><span class="sxs-lookup"><span data-stu-id="27ea3-103">Submit a leave request to workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="27ea3-104">Programmā Microsoft Dynamics 365 Human Resources, varat izmantot MyLeaveRequests iesniegt () lietojumprogrammu programmēšanas interfeiss (API), lai darbplūsmā iesniegtu atvaļinājuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="27ea3-104">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="27ea3-105">Šis API ir parādīts kā darbība MyLeaveRequests OData elementā.</span><span class="sxs-lookup"><span data-stu-id="27ea3-105">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="27ea3-106">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="27ea3-106">Prerequisites</span></span>

<span data-ttu-id="27ea3-107">Atvaļinājuma pieprasījums jāsaglabā datu bāzē, un tam ir jābūt izgūstamam, izmantojot MyLeaveRequests elementu.</span><span class="sxs-lookup"><span data-stu-id="27ea3-107">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="27ea3-108">Tiesības</span><span class="sxs-lookup"><span data-stu-id="27ea3-108">Permissions</span></span>

<span data-ttu-id="27ea3-109">Lai izsauktu šo API, ir nepieciešama viena no šīm atļaujām.</span><span class="sxs-lookup"><span data-stu-id="27ea3-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="27ea3-110">Plašāku informāciju par atļaujām un to atlasi skatiet [Autentifikācija](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="27ea3-110">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="27ea3-111">Atļaujas veids</span><span class="sxs-lookup"><span data-stu-id="27ea3-111">Permission type</span></span>                    | <span data-ttu-id="27ea3-112">Atļaujas (no vismazāk priviliģētās uz priviliģētāko)</span><span class="sxs-lookup"><span data-stu-id="27ea3-112">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="27ea3-113">Deleģēta (darba vai skolas konts)</span><span class="sxs-lookup"><span data-stu-id="27ea3-113">Delegated (work or school account)</span></span> | <span data-ttu-id="27ea3-114">lietotāja \_ personifikācija</span><span class="sxs-lookup"><span data-stu-id="27ea3-114">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="27ea3-115">HTTPS pieprasījums</span><span class="sxs-lookup"><span data-stu-id="27ea3-115">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="27ea3-116">Pieprasījums atbilst OData standartiem.</span><span class="sxs-lookup"><span data-stu-id="27ea3-116">The request conforms to OData standards.</span></span> <span data-ttu-id="27ea3-117">Parametri {requestId}, {leaveType}, {leaveDate} un {dataArea} attiecas uz laukiem, kas veido kompozīta parasto atslēgu MyLeaveRequests entītijai.</span><span class="sxs-lookup"><span data-stu-id="27ea3-117">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="27ea3-118">Lai gan MyLeaveRequests elementa lauki attiecas uz atsevišķu rindu, kas atrodas atvaļinājumu pieprasījumā, izsaucot iesniegto API, darbplūsmai tiks iesniegts viss atvaļinājuma pieprasījums (visas rindas).</span><span class="sxs-lookup"><span data-stu-id="27ea3-118">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="27ea3-119">Pieprasījuma galvenes</span><span class="sxs-lookup"><span data-stu-id="27ea3-119">Request headers</span></span>

| <span data-ttu-id="27ea3-120">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="27ea3-120">Header</span></span>         | <span data-ttu-id="27ea3-121">Value</span><span class="sxs-lookup"><span data-stu-id="27ea3-121">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="27ea3-122">Autorizācija</span><span class="sxs-lookup"><span data-stu-id="27ea3-122">Authorization</span></span>  | <span data-ttu-id="27ea3-123">Nesējs {token} (obligāts)</span><span class="sxs-lookup"><span data-stu-id="27ea3-123">Bearer {token} (required)</span></span> |
| <span data-ttu-id="27ea3-124">Satura veids</span><span class="sxs-lookup"><span data-stu-id="27ea3-124">Content-Type</span></span>   | <span data-ttu-id="27ea3-125">pieteikums/json</span><span class="sxs-lookup"><span data-stu-id="27ea3-125">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="27ea3-126">Pieprasījuma pamatteksts</span><span class="sxs-lookup"><span data-stu-id="27ea3-126">Request body</span></span>

<span data-ttu-id="27ea3-127">Nesniedziet pieprasījuma pamattekstu šai metodei.</span><span class="sxs-lookup"><span data-stu-id="27ea3-127">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="27ea3-128">Atbilde</span><span class="sxs-lookup"><span data-stu-id="27ea3-128">Response</span></span>

<span data-ttu-id="27ea3-129">Veiksmīga atbilde vienmēr ir atbilde **204 Nav satura**.</span><span class="sxs-lookup"><span data-stu-id="27ea3-129">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="27ea3-130">Neautorizēti zvanītāji saņems **401 Neautorizēts** vai **403 Aizliegts**.</span><span class="sxs-lookup"><span data-stu-id="27ea3-130">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="27ea3-131">Ja iesniegums ir neveiksmīgs (piemēram, pārbaudes dēļ), atbilde būs **500 Servera kļūda**, un atbildes teksts ietvers JSON objektu ar sīkāku informāciju.</span><span class="sxs-lookup"><span data-stu-id="27ea3-131">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="27ea3-132">Paraugs</span><span class="sxs-lookup"><span data-stu-id="27ea3-132">Example</span></span>

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a><span data-ttu-id="27ea3-133">Pārbaude un kļūdu ziņojumi</span><span class="sxs-lookup"><span data-stu-id="27ea3-133">Validation and error messages</span></span>

<span data-ttu-id="27ea3-134">API iesniedzamā zvana ietvaros Human Resources veic biznesa loģikas validāciju pirms iesniegšanas, kas nodrošina, ka atvaļinājuma pieprasījums ir iesniegšanai derīgā stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="27ea3-134">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="27ea3-135">Iespējamie kļūdu ziņojumi, ko var saņemt atbildē, ja pārbaudes neatbilst:</span><span class="sxs-lookup"><span data-stu-id="27ea3-135">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="27ea3-136">Pieprasījums iekļaus {LeaveTypeId} bilanci zem {date} minimālās atļautās bilances.</span><span class="sxs-lookup"><span data-stu-id="27ea3-136">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="27ea3-137">Brīvā laika pieprasījumu pabeigtā stāvoklī nevar iesniegt.</span><span class="sxs-lookup"><span data-stu-id="27ea3-137">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="27ea3-138">Nevar iesniegt vai saglabāt pieprasījumu, jo nav izdarītas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="27ea3-138">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="27ea3-139">Pievienojiet vai atjauniniet summu vai atvaļinājuma veidu un mēģiniet vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="27ea3-139">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="27ea3-140">Ievadītais brīvā laika pieprasījums ietver vienu vai vairākas dienas ar vienādu datumu un atvaļinājuma veidu kā gaidīšanā jau esošu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="27ea3-140">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="27ea3-141">Lūdzu, atsauciet esošo pieprasījumu, lai veiktu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="27ea3-141">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="27ea3-142">Iemesla kods '{ReasonCodeId}' neattiecas uz nevienu no pieprasījumā norādītajiem atvaļinājuma veidiem.</span><span class="sxs-lookup"><span data-stu-id="27ea3-142">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="27ea3-143">Atvaļinājuma tipam '{LeaveTypeId}' ir nepieciešams pamatojuma kods.</span><span class="sxs-lookup"><span data-stu-id="27ea3-143">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="27ea3-144">Atlasiet atbilstošo veidu un pamatojuma kodu.</span><span class="sxs-lookup"><span data-stu-id="27ea3-144">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="27ea3-145">Brīvais laiks netika iesniegts veiksmīgi.</span><span class="sxs-lookup"><span data-stu-id="27ea3-145">The time off was not submitted successfully.</span></span> <span data-ttu-id="27ea3-146">Brīvais laiks ir saglabāts kā melnraksta pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="27ea3-146">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="27ea3-147">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="27ea3-147">See also</span></span>

- [<span data-ttu-id="27ea3-148">MyLeaveRequests pārskats</span><span class="sxs-lookup"><span data-stu-id="27ea3-148">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="27ea3-149">Autentifikācija</span><span class="sxs-lookup"><span data-stu-id="27ea3-149">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]