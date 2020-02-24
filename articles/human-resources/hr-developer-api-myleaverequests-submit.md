---
title: Atvaļinājuma pieprasījuma iesniegšana darbplūsmai
description: ''
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 008ee231ca9f0459e332b17cea9f2a3f3e3cc2a5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009854"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="4449c-102">Atvaļinājuma pieprasījuma iesniegšana darbplūsmai</span><span class="sxs-lookup"><span data-stu-id="4449c-102">Submit a leave request to workflow</span></span>

<span data-ttu-id="4449c-103">Programmā Microsoft Dynamics 365 Human Resources, varat izmantot MyLeaveRequests iesniegt () lietojumprogrammu programmēšanas interfeiss (API), lai darbplūsmā iesniegtu atvaļinājuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="4449c-103">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="4449c-104">Šis API ir parādīts kā darbība MyLeaveRequests OData elementā.</span><span class="sxs-lookup"><span data-stu-id="4449c-104">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4449c-105">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="4449c-105">Prerequisites</span></span>

<span data-ttu-id="4449c-106">Atvaļinājuma pieprasījums jāsaglabā datu bāzē, un tam ir jābūt izgūstamam, izmantojot MyLeaveRequests elementu.</span><span class="sxs-lookup"><span data-stu-id="4449c-106">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="4449c-107">Tiesības</span><span class="sxs-lookup"><span data-stu-id="4449c-107">Permissions</span></span>

<span data-ttu-id="4449c-108">Lai izsauktu šo API, ir nepieciešama viena no šīm atļaujām.</span><span class="sxs-lookup"><span data-stu-id="4449c-108">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="4449c-109">Plašāku informāciju par atļaujām un to atlasi skatiet [Autentifikācija](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="4449c-109">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="4449c-110">Atļaujas veids</span><span class="sxs-lookup"><span data-stu-id="4449c-110">Permission type</span></span>                    | <span data-ttu-id="4449c-111">Atļaujas (no vismazāk priviliģētās uz priviliģētāko)</span><span class="sxs-lookup"><span data-stu-id="4449c-111">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="4449c-112">Deleģēta (darba vai skolas konts)</span><span class="sxs-lookup"><span data-stu-id="4449c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="4449c-113">lietotāja \_ personifikācija</span><span class="sxs-lookup"><span data-stu-id="4449c-113">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="4449c-114">HTTPS pieprasījums</span><span class="sxs-lookup"><span data-stu-id="4449c-114">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="4449c-115">Pieprasījums atbilst OData standartiem.</span><span class="sxs-lookup"><span data-stu-id="4449c-115">The request conforms to OData standards.</span></span> <span data-ttu-id="4449c-116">Parametri {requestId}, {leaveType}, {leaveDate} un {dataArea} attiecas uz laukiem, kas veido kompozīta parasto atslēgu MyLeaveRequests entītijai.</span><span class="sxs-lookup"><span data-stu-id="4449c-116">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="4449c-117">Lai gan MyLeaveRequests elementa lauki attiecas uz atsevišķu rindu, kas atrodas atvaļinājumu pieprasījumā, izsaucot iesniegto API, darbplūsmai tiks iesniegts viss atvaļinājuma pieprasījums (visas rindas).</span><span class="sxs-lookup"><span data-stu-id="4449c-117">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="4449c-118">Pieprasījuma galvenes</span><span class="sxs-lookup"><span data-stu-id="4449c-118">Request headers</span></span>

| <span data-ttu-id="4449c-119">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="4449c-119">Header</span></span>         | <span data-ttu-id="4449c-120">Value</span><span class="sxs-lookup"><span data-stu-id="4449c-120">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="4449c-121">Autorizācija</span><span class="sxs-lookup"><span data-stu-id="4449c-121">Authorization</span></span>  | <span data-ttu-id="4449c-122">Nesējs {token} (obligāts)</span><span class="sxs-lookup"><span data-stu-id="4449c-122">Bearer {token} (required)</span></span> |
| <span data-ttu-id="4449c-123">Satura veids</span><span class="sxs-lookup"><span data-stu-id="4449c-123">Content-Type</span></span>   | <span data-ttu-id="4449c-124">pieteikums/json</span><span class="sxs-lookup"><span data-stu-id="4449c-124">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="4449c-125">Pieprasījuma pamatteksts</span><span class="sxs-lookup"><span data-stu-id="4449c-125">Request body</span></span>

<span data-ttu-id="4449c-126">Nesniedziet pieprasījuma pamattekstu šai metodei.</span><span class="sxs-lookup"><span data-stu-id="4449c-126">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="4449c-127">Atbilde</span><span class="sxs-lookup"><span data-stu-id="4449c-127">Response</span></span>

<span data-ttu-id="4449c-128">Veiksmīga atbilde vienmēr ir atbilde **204 Nav satura**.</span><span class="sxs-lookup"><span data-stu-id="4449c-128">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="4449c-129">Neautorizēti zvanītāji saņems **401 Neautorizēts** vai **403 Aizliegts**.</span><span class="sxs-lookup"><span data-stu-id="4449c-129">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="4449c-130">Ja iesniegums ir neveiksmīgs (piemēram, pārbaudes dēļ), atbilde būs **500 Servera kļūda**, un atbildes teksts ietvers JSON objektu ar sīkāku informāciju.</span><span class="sxs-lookup"><span data-stu-id="4449c-130">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="4449c-131">Paraugs</span><span class="sxs-lookup"><span data-stu-id="4449c-131">Example</span></span>

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

## <a name="validation-and-error-messages"></a><span data-ttu-id="4449c-132">Pārbaude un kļūdu ziņojumi</span><span class="sxs-lookup"><span data-stu-id="4449c-132">Validation and error messages</span></span>

<span data-ttu-id="4449c-133">API iesniedzamā zvana ietvaros Human Resources veic biznesa loģikas validāciju pirms iesniegšanas, kas nodrošina, ka atvaļinājuma pieprasījums ir iesniegšanai derīgā stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="4449c-133">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="4449c-134">Iespējamie kļūdu ziņojumi, ko var saņemt atbildē, ja pārbaudes neatbilst:</span><span class="sxs-lookup"><span data-stu-id="4449c-134">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="4449c-135">Pieprasījums iekļaus {LeaveTypeId} bilanci zem {date} minimālās atļautās bilances.</span><span class="sxs-lookup"><span data-stu-id="4449c-135">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="4449c-136">Brīvā laika pieprasījumu pabeigtā stāvoklī nevar iesniegt.</span><span class="sxs-lookup"><span data-stu-id="4449c-136">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="4449c-137">Nevar iesniegt vai saglabāt pieprasījumu, jo nav izdarītas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="4449c-137">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="4449c-138">Pievienojiet vai atjauniniet summu vai atvaļinājuma veidu un mēģiniet vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="4449c-138">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="4449c-139">Ievadītais brīvā laika pieprasījums ietver vienu vai vairākas dienas ar vienādu datumu un atvaļinājuma veidu kā gaidīšanā jau esošu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="4449c-139">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="4449c-140">Lūdzu, atsauciet esošo pieprasījumu, lai veiktu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="4449c-140">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="4449c-141">Iemesla kods '{ReasonCodeId}' neattiecas uz nevienu no pieprasījumā norādītajiem atvaļinājuma veidiem.</span><span class="sxs-lookup"><span data-stu-id="4449c-141">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="4449c-142">Atvaļinājuma tipam '{LeaveTypeId}' ir nepieciešams pamatojuma kods.</span><span class="sxs-lookup"><span data-stu-id="4449c-142">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="4449c-143">Atlasiet atbilstošo veidu un pamatojuma kodu.</span><span class="sxs-lookup"><span data-stu-id="4449c-143">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="4449c-144">Brīvais laiks netika iesniegts veiksmīgi.</span><span class="sxs-lookup"><span data-stu-id="4449c-144">The time off was not submitted successfully.</span></span> <span data-ttu-id="4449c-145">Brīvais laiks ir saglabāts kā melnraksta pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="4449c-145">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="4449c-146">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="4449c-146">See also</span></span>

- [<span data-ttu-id="4449c-147">MyLeaveRequests pārskats</span><span class="sxs-lookup"><span data-stu-id="4449c-147">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="4449c-148">Autentifikācija</span><span class="sxs-lookup"><span data-stu-id="4449c-148">Authentication</span></span>](hr-developer-api-authentication.md)