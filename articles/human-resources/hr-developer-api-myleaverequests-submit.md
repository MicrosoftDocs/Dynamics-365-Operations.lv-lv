---
title: Atvaļinājuma pieprasījuma iesniegšana darbplūsmai
description: Programmā Microsoft Dynamics 365 Human Resources, varat izmantot MyLeaveRequests iesniegt () lietojumprogrammu programmēšanas interfeiss (API), lai darbplūsmā iesniegtu atvaļinājuma pieprasījumu.
author: twheeloc
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba2867646ac03953a43404984a5d04d4edb1f5ac
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687000"
---
# <a name="submit-a-leave-request-to-workflow"></a>Atvaļinājuma pieprasījuma iesniegšana darbplūsmai


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Programmā Microsoft Dynamics 365 Human Resources, varat izmantot MyLeaveRequests iesniegt () lietojumprogrammu programmēšanas interfeiss (API), lai darbplūsmā iesniegtu atvaļinājuma pieprasījumu. Šis API ir parādīts kā darbība MyLeaveRequests OData elementā.

## <a name="prerequisites"></a>Priekšnosacījumi

Atvaļinājuma pieprasījums jāsaglabā datu bāzē, un tam ir jābūt izgūstamam, izmantojot MyLeaveRequests elementu.

## <a name="permissions"></a>Tiesības

Lai izsauktu šo API, ir nepieciešama viena no šīm atļaujām. Plašāku informāciju par atļaujām un to atlasi skatiet [Autentifikācija](hr-developer-api-authentication.md).

| Atļaujas veids                    | Atļaujas (no vismazāk priviliģētās uz priviliģētāko) |
|------------------------------------|--------------------------------------------------------|
| Deleģēta (darba vai skolas konts) | lietotāja\_personifikācija                                    |

## <a name="https-request"></a>HTTPS pieprasījums

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

Pieprasījums atbilst OData standartiem. Parametri {requestId}, {leaveType}, {leaveDate} un {dataArea} attiecas uz laukiem, kas veido kompozīta parasto atslēgu MyLeaveRequests entītijai.

> [!NOTE]
> Lai gan MyLeaveRequests elementa lauki attiecas uz atsevišķu rindu, kas atrodas atvaļinājumu pieprasījumā, izsaucot iesniegto API, darbplūsmai tiks iesniegts viss atvaļinājuma pieprasījums (visas rindas).

### <a name="request-headers"></a>Pieprasījuma galvenes

| Virsraksts         | Value                     |
|----------------|---------------------------|
| Autorizācija  | Nesējs {token} (obligāts) |
| Satura veids   | pieteikums/json          |

### <a name="request-body"></a>Pieprasījuma pamatteksts

Nesniedziet pieprasījuma pamattekstu šai metodei.

### <a name="response"></a>Atbilde

Veiksmīga atbilde vienmēr ir atbilde **204 Nav satura**.

Neautorizēti zvanītāji saņems **401 Neautorizēts** vai **403 Aizliegts**.

Ja iesniegums ir neveiksmīgs (piemēram, pārbaudes dēļ), atbilde būs **500 Servera kļūda**, un atbildes teksts ietvers JSON objektu ar sīkāku informāciju.

## <a name="example"></a>Paraugs

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

## <a name="validation-and-error-messages"></a>Pārbaude un kļūdu ziņojumi

API iesniedzamā zvana ietvaros Human Resources veic biznesa loģikas validāciju pirms iesniegšanas, kas nodrošina, ka atvaļinājuma pieprasījums ir iesniegšanai derīgā stāvoklī. Iespējamie kļūdu ziņojumi, ko var saņemt atbildē, ja pārbaudes neatbilst:

 - Pieprasījums iekļaus '{LeaveTypeId}' bilanci zem {date} minimālās atļautās bilances.
 - Brīvā laika pieprasījumu pabeigtā stāvoklī nevar iesniegt.
 - Nevar iesniegt vai saglabāt pieprasījumu, jo nav izdarītas izmaiņas. Pievienojiet vai atjauniniet summu vai atvaļinājuma veidu un mēģiniet vēlreiz.
 - Ievadītais brīvā laika pieprasījums ietver vienu vai vairākas dienas ar vienādu datumu un atvaļinājuma veidu kā gaidīšanā jau esošu pieprasījumu. Lūdzu, atsauciet esošo pieprasījumu, lai veiktu izmaiņas.
 - Iemesla kods '{ReasonCodeId}' neattiecas uz nevienu no pieprasījumā norādītajiem atvaļinājuma veidiem.
 - Atvaļinājuma tipam '{LeaveTypeId}' ir nepieciešams pamatojuma kods. Atlasiet atbilstošo veidu un pamatojuma kodu.
 - Brīvais laiks netika iesniegts veiksmīgi. Brīvais laiks ir saglabāts kā melnraksta pieprasījums.

## <a name="see-also"></a>Skatiet arī

- [MyLeaveRequests pārskats](hr-developer-api-myleaverequests-overview.md)
- [Autentifikācija](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
