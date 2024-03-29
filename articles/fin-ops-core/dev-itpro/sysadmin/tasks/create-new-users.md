---
title: Jaunu lietotāju izveide
description: Lietotāji ir jūsu organizācijas iekšējie darbinieki vai ārējie debitori un kreditori, kuriem nepieciešama piekļuve sistēmai sava darba veikšanai.
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 00da7c69ff18abd02ca0cd7984e9b2de5e453a0c
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103331"
---
# <a name="create-new-users"></a>Jaunu lietotāju izveide

[!include [banner](../../includes/banner.md)]

Pirms varat piekļūt finanšu un operāciju programmām, vispirms jāpievieno lietotāju lapai **(** Sistēmas **administrēšanas \> lietotāju \> lietotāji**). Lietotāji ietver jūsu organizācijas iekšējos darbiniekus vai ārējos debitorus un kreditorus. Lietotājus var manuāli importēt vai pievienot. Visiem lietotājiem jābūt korekti licencētiem atbilstošai lietošanai.

Informāciju par to, kā pirkt un licencēt finanšu un operāciju programmām, skatiet [Microsoft Dynamics 365. licencēšanas rokasgrāmatā](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).

## <a name="assign-a-license-to-a-user"></a>Piešķiriet licenci lietotājam
Sistēmas administratori [var piešķirt licences lietotājiem](/office365/admin/subscriptions-and-billing/assign-licenses-to-users) administrēšanas [Microsoft 365 centrā](/office365/admin/admin-overview/about-the-admin-center).

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a>Ārēja lietotāja pievienošana Azure AD un licences piešķiršana 
Ārējiem lietotājiem jābūt norādītiem savā nomnieka direktorijā (Azure Active Directory (Azure AD)), lai tiem varētu piešķirt licences. Šie ārējie lietotāji jāpievieno nomniekam Azure AD kā vieslietotāji un pēc tam jāpiešķir atbilstošās licences. Finanšu un operāciju programmu vajadzība ir, lai viesa lietotāja uzņēmumam būtu jāizmanto Azure AD. Papildinformāciju skatiet [Pievienot Azure Active Directory B2B sadarbības lietotājus Azure portālā](/azure/active-directory/b2b/add-users-administrator).

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
 - Kontiem, kasAzure AD nav lietotāji, piemēram, Service-2-Service, ievadiet pamatteksta vērtību. Piemēram, NA. Šī vērtība palīdzēs izvairīties no nepareiziem autentifikācijas izsaukumi, kas var izraisīt kļūdas, ja tiek izmantota derīga identitātes nodrošinātāja vērtība.  
 - Ārējiem vai viesa lietotājiem pievienojiet viņu Azure AD nomnieka vārdu pēc https://sts.windows.net/.
6. Laukā **E-pasts** ievadiet pilnu lietotāja e-pasta/lietotāja principa nosaukumu.  
7. Laukā **Uzņēmums** atlasiet noklusējuma starta uzņēmumu lietotājam. 
8. Atlasiet **Saglabāt**.

Identitātes nodrošinātāja un telemetrijas ID vērtības tiks atjauninātas, pamatojoties uz [Microsoft grafika](/graph/overview) izsaukumu, saglabājot lietotāja ierakstu. Telemetrijas ID ir balstīts uz lietotāja objekta ID/drošības identifikatoru (SID) Azure AD.

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
