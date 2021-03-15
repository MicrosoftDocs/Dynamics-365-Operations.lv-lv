---
title: Jaunu lietotāju izveide
description: Lietotāji ir jūsu organizācijas iekšējie darbinieki vai ārējie debitori un kreditori, kuriem nepieciešama piekļuve sistēmai sava darba veikšanai.
author: peakerbl
manager: AnnBe
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca062ddd49f1c206c503fb6160ed436fe2d6f7e9
ms.sourcegitcommit: 9e27a097b7eb3c8f2df66011ccc597ad18bc5445
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/13/2021
ms.locfileid: "4878661"
---
# <a name="create-new-users"></a>Jaunu lietotāju izveide

[!include [banner](../../includes/banner.md)]

Pirms varat piekļūt Finance and Operations programmām, vispirms jums jābūt pievienotam lapai **Lietotāji** (**Sistēmas administrēšana \> Lietotāji \> Lietotāji**). Lietotāji ietver jūsu organizācijas iekšējos darbiniekus vai ārējos debitorus un kreditorus. Lietotājus var manuāli importēt vai pievienot. Visiem lietotājiem jābūt korekti licencētiem atbilstošai lietošanai.

Papildinformāciju par to, kā pirkt un licencēt Finance and Operations lietojumprogrammas, skatiet [Microsoft Dynamics 365 licencēšanas rokasgrāmatā](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).

## <a name="assign-a-license-to-a-user"></a>Piešķiriet licenci lietotājam
Sistēmas administratori var [piešķirt licences lietotājiem](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) [Microsoft 365 administrēšanas centrā](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a>Ārēja lietotāja pievienošana Azure AD un licences piešķiršana 
Ārējiem lietotājiem jābūt norādītiem savā nomnieka direktorijā (Azure Active Directory (Azure AD)), lai tiem varētu piešķirt licences. Šie ārējie lietotāji jāpievieno nomniekam Azure AD kā vieslietotāji un pēc tam jāpiešķir atbilstošās licences. Finance and Operations programmām ir prasība, ka viesa lietotāja uzņēmumam ir jāizmanto Azure AD. Papildinformāciju skatiet [Azure Active Directory B2B sadarbības lietotāju pievienošana Azure portālā](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="import-new-users-from-azure-ad"></a>Jaunu lietotāju importēšana no Azure AD 
1. Dodieties uz **Sistēmas administrēšana** \> **Lietotāji** \> **Lietotāji**.
2. Darbību rūtī atlasiet **Importēt lietotājus**.
3. Atlasiet importējamos lietotājus. Sarakstā ir iekļauti Azure AD lietotāji, kas pašlaik nav šīs vides lietotāji.
4. Atlasiet **Importēt lietotājus**.
5. Atlasiet **Aizvērt**.

> [!NOTE]
> Lauka **Uzņēmums** vērtība tiks iestatīta, pamatojoties uz pašreizējo sesijas uzņēmumu administratoram. Pēc importēšanas jums jāpiešķir lomas un organizācijas pēc vajadzības. Plašāku informāciju skatiet [Lietotāju piešķiršana drošības lomām](assign-users-security-roles.md). Ar nosacījumiem tas var būt pieprasīts arī, lai saistītu lietotāju ar **Personu** un atjauninātu lietotāja opcijas, piemēram, valodu.

## <a name="manually-add-a-new-user"></a>Manuāli pievienot jaunu lietotāju
1. Dodieties uz **Sistēmas administrēšana** \> **Lietotāji** \> **Lietotāji**.
2. Darbību rūtī atlasiet **Jauns**.
3. Laukā **Lietotāja ID** ievadiet lietotāja unikālu identifikatoru.   
4. Laukā **Lietotāja vārds** ievadiet lietotāja vārdu.  
5. Laukā **Nodrošinātājs**:
 - Iekšējiem lietotājiem izmantojiet noklusējuma vērtību. Piemēram, Azure AD nomnieka prefikss https://sts.windows.net/.  
 - Kontiem, kas Azure AD nav lietotāji, piemēram, Service-2-Service, ievadiet pamatteksta vērtību. Piemēram, NA. Šī vērtība palīdzēs izvairīties no nepareiziem autentifikācijas izsaukumi, kas var izraisīt kļūdas, ja tiek izmantota derīga identitātes nodrošinātāja vērtība.  
 - Ārējiem vai viesa lietotājiem pievienojiet viņu Azure AD nomnieka vārdu pēc https://sts.windows.net/.
6. Laukā **E-pasts** ievadiet pilnu lietotāja e-pasta/lietotāja principa nosaukumu.  
7. Laukā **Uzņēmums** atlasiet noklusējuma starta uzņēmumu lietotājam. 
8. Atlasiet **Saglabāt**.

Identitātes nodrošinātāja un telemetrijas ID vērtības tiks atjauninātas, pamatojoties uz [Microsoft grafika](https://docs.microsoft.com/graph/overview) izsaukumu, saglabājot lietotāja ierakstu. Telemetrijas ID ir balstīts uz lietotāja objekta ID/drošības identifikatoru (SID) Azure AD.

> [!NOTE]
> Pēc lietotāja pievienošanas jums jāpiešķir lomas un organizācijas pēc vajadzības. Plašāku informāciju skatiet [Lietotāju piešķiršana drošības lomām](assign-users-security-roles.md). Ar nosacījumiem tas var būt pieprasīts arī, lai saistītu lietotāju ar **Personu** un atjauninātu **Lietotāja opcijas**, piemēram, valodu.

## <a name="change-a-user-id"></a>Lietotāja ID maiņa
Lai mainītu lietotāja ID, datu bāzē ir jāpārdēvē atslēga. Ja, izmantojot šo procedūru, maināt lietotāja ID, visi saistītie lietotāja iestatījumi tiek modificēti tā, lai izmantotu jauno lietotāja ID. Piemēram, lietojuma informācija tabulā **SysLastValue** tiek atjaunināta uz jauno lietotāja ID.

> [!NOTE]
> Lietotāja ID ir primārā lietotāja informācijas tabulas atslēga. Primārās atslēgas pārdēvēšana var aizņemt kādu laiku esošiem lietotājiem, jo visas atsauces uz atslēgu arī tiek atjauninātas datu bāzē. 

1. Dodieties uz **Sistēmas administrēšana \> Lietotāji \> Lietotāji**.
2. Sarakstā atlasiet lietotāju un atlasiet **Opcijas\> Informācija par ierakstu**.
3. Atlasiet **Pārdēvēt**.
4. Ievadiet jaunu Lietotāja ID unikālo vērtību, tad atlasiet **Labi**. 
5. Lai apstiprinātu, atlasiet **Jā**.

## <a name="additional-resources"></a>Papildu resursi

Papildinformāciju par B2B lietotāju implementēšanu skatiet [sadaļā "Eksportēt B2B lietotājus uz Azure AD](../implement-b2b.md).

Informāciju par iepriekškonfigurētiem sistēmas kontiem skatiet [Iepriekš konfigurētos sistēmas kontus](../pre-configured-system-accounts.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]