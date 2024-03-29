---
title: Elektronisko pārskatu (ER) paplašinātā formāta uzmeklēšana
description: Šajā rakstā ir aprakstīts, kā ER formāta atsauci var iestatīt ER formāta meklējot, kad nepieciešamais formāts tiek saglabāts Globālajā repozitorijā.
author: kfend
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: 624f5c347c27cc2075f9602087c1c49e84340565
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274925"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a>Ļaut lietotājiem iestatīt ER formāta atsauci, pieprasot formātu no globālās krātuves

[!include [banner](../includes/banner.md)]

Jūs variet izmantot [Elektronisko pārskatu](general-electronic-reporting.md) (ER) struktūru, lai konfigurētu formātus nosūtīšanas dokumentiem saskaņā ar dažādu valstu/reģionu juridiskajām prasībām. Varat arī izmantot ER struktūru, lai konfigurētu formātus ienākošo dokumentu parsēšanai un izmantotu informāciju no šiem dokumentiem, lai pievienotu vai atjauninātu programmas datus. Katru no šiem formātiem var izmantot jūsu Dynamics 365 finanšu instancē ienākošo vai izejošo biznesa dokumentu apstrādei kā daļu no noteikta biznesa procesa.

Parasti jānorāda, kāds ER formāts konkrētā biznesa procesā jāizmanto. Lai to izdarītu, atlasiet uzmeklēšanas laukā vienu ER formātu, kas ir konfigurēts kā daļa no biznesa procesam raksturīgiem parametriem. Šie uzmeklēšanas lauki parasti tiek ieviesti, izmantojot attiecīgo ER struktūras API. Plašāku informāciju skatiet [ER struktūras API kods formāta kartēšanas uzmeklēšanas atspoguļošanai](er-apis-app73.md#code-to-display-a-format-mapping-lookup).

Piemēram, konfigurējot [ārējās tirdzniecības parametrus](../../../finance/localizations/emea-intrastat.md#set-up-foreign-trade-parameters), jāiestata atsauces uz atsevišķiem ER formātiem, kas tiks izmantoti, lai ģenerētu Intrastat deklarāciju un Intrastat deklarācijas kontroles pārskatu. Tālak redzamajos ekrānuzņēmumos parādīts, kā tiek ER formātu uzmeklēšanas lauks izskatās lapā **Ārējās tirdzniecības parametri**.

Ja pašreizējā Finance instancē nav iekļauti ar Intrastat biznesa procesu saistīti ER formāti, šis uzmeklēšanas lauks būs tukšs.

[![Ārējās tirdzniecības parametru lapa, tukšs pārskata formāta kartēšanas lauks.](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)

Ja pašreizējā Finance instancē ir iekļauti ar Intrastat biznesa procesu saistīti ER formāti, šis uzmeklēšanas lauks piedāvā ER formātus.

[![Ārējās tirdzniecības parametru lapa, tukšs pārskata formāta kartēšanas lauks ar opcijām.](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)

Šī uzmeklēšana piedāvā tikai tādus ER formātus, kas jau ir importēti uz pašreizējo Finance instanci. Lai [importētu](./tasks/er-import-configuration-lifecycle-services.md) ER risinājumus uz pašreizējo Finance instanci, jums vajadzīgas atļaujas, lai palaistu attiecīgo ER struktūras funkciju, kas atbalsta tādu ER risinājumu [dzīves ciklu](general-electronic-reporting-manage-configuration-lifecycle.md), kurā iekļauti ER formāti.

Sākot no Finance versijas 10.0.9 (2020. gada aprīļa izlaidums), ir paplašināts lietotāja interfeiss ar ER formāta meklēšanu, kas ieviesta, izmantojot ER struktūras API. Joprojām varat atlasīt esošos ER formātus kopsavilkuma cilnē **Atlasīt formāta konfigurāciju**. Papildus paplašinātā uzmeklēšana piedāvā jaunu opciju, lai meklētu globālajā krātuvē (GR) un atrastu konkrētus ER formātus. Visi ER formāti no GR tiek piedāvāti kopsavilkuma cilnē **Importēt no globālās repozitorija**.

[![Ārējās tirdzniecības parametru lapa, Importēt no globālā repozitorija kopsavilkuma cilnes.](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)

Līdzīgi kā kopsavilkuma cilnē **Atlasīt formāta konfigurāciju**, kopsavilkuma cilne **Importēt no globālā repozitorija** rāda tikai tādus ER formātus, kas attiecas uz biznesa procesu, kuram ER formāts ir izvēlēts šajā uzmeklēšanas laukā. Šajā piemērā - Intrastat deklarācijas ģenerēšana. ER formāts ir piemērojams uzņēmumam, kurā lietotājs pašlaik ir pierakstījies (atkarībā no uzņēmuma valsts konteksta).

Atlasot kopsavilkuma cilnē **Importēt no globālā repozitorija** ER formātu, atlasītais ER formāts [konfigurācija](general-electronic-reporting.md#Configuration) tiek importēts no GR uz pašreizējo Finance instanci.

[![Ārējās tirdzniecības parametru lapa, operācijas piezīmes apstrāde.](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)

Pēc tam, ja importēšana pabeigta veiksmīgi, šajā uzmeklēšanas laukā tiek saglabāta atsauce uz importēto ER formātu. Piekļūstot GR pirmo reizi, jāseko sniegtajai saitei, lai pierakstītos pakalpojumam [Regulatory Configuration Service](https://aka.ms/rcs) (RCS), ko izmanto, lai pārvaldītu piekļuvi GR uzglabāšanai.

[![Ārējās tirdzniecības parametru lapa, saite uz pierakstīšanos RCS.](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)

Kopsavilkuma cilne **Importēt no globālā repozitorija** pēc noklusējuma sniedz ER formātu sarakstu no pagaidu krātuves, kas tiek automātiski izveidota, pamatojoties uz veiktspējas uzlabojumiem paredzēto GR saturu. Tas notiek, ja kopsavilkuma cilne **Importēt no globāla repozitorija** tiek atvērta pirmo reizi, kas var ilgt vairākas sekundes.

Ja kopsavilkuma cilnē **Importēt no globālā repozitorija** neredzat nepieciešamo ER formātu, bet esat pārliecināts, ka šis ER formāts ir saglabāts GR, izvēlieties opciju **Sinhronizēts**. Šī opcija atjauninās pagaidu uzglabāšanu, un tas tiks sinhronizēts ar pašreizējo GR saturu.

## <a name="feature-activation"></a>Līdzekļu aktivizēšana

Šīs funkcionalitātes pieejamību kontrolē līdzeklis **Paplašinātā ER formāta konfigurāciju meklēšana, kas ļauj meklēt globālajā repozitorijā**, kas pieejams lapā **Līdzekļu pārvaldība**. Šis līdzeklis ir iespējots pēc noklusējuma.

[![Lapa Līdzekļu pārvaldība.](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)

## <a name="security-considerations"></a>Drošības apsvērumi

Privilēģija **Uzturēt konfigurācijas repozitorijus** (**ERMaintainSolutionRepositories**) kontrolē piekļuvi GR, lai lietotājs varētu atvērt ER formāta uzmeklēšanu ar iespējotu kopsavilkuma cilni **Importēt no globālā repozitorija**. Lai lietotāji varētu piekļūt GR saturam no ER formāta uzmeklēšanas, jāmaina drošības iestatījumi, piešķirot lietotājiem privilēģiju **ERMaintainSolutionRepositories** vai nu tieši, vai izmantojot jau piešķirtās lomas un pienākumus.

Tālāk redzamajā ekrānuzņēmumā parādīts, kā šo privilēģiju var piešķirt lietotājiem, kuriem ir piešķirta **Grāmatveža** loma. Šī loma ļauj lietotājiem konfigurēt ārējās tirdzniecības parametrus un iesatīt atsauces uz ER formātiem lapas **Ārējās tirdzniecības parametri** laukos **Faila formāta kartēšana** un **Pārskata formāta kartēšana**.

[![Lapa Drošības konfigurācija.](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)

## <a name="limitations"></a>Ierobežojumi

ER formāta uzmeklēšanā piekļuve GR pašlaik tiek atbalstīta tikai tiem ER formātiem, kas tiek izmantoti izejošo dokumentu ģenerēšanai.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a>Kāpēc nevar no ER uzmeklēšanas piekļūt globālajam repozitorijam?

Ja lapā **Līdzekļu pārvaldība** esat iespējojis līdzekli **Paplašinātā ER formāta konfigurāciju meklēšana, kas ļauj meklēt globālajā repozitorijā**, bet lietotājiem nav redzami ER formāti kopsavilkuma cilnē **Importēt no globālā repozitorija**, un opcija **Sinhronizēt** ir redzama, bet atspējota, pārliecinieties, ka lietotājam ir piešķirta privilēģija **Uzturēt konfigurācijas repozitorijus** (**ERMaintainSolutionRepositories**). Sazinieties ar sistēmas administratoru, lai saņemtu šo privilēģiju.

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)
- [Elektronisko pārskatu veidošanas (ER) struktūras API](er-apis-app73.md)
- [Elektronisko pārskatu veidošanas (ER) konfigurāciju dzīves cikla pārvaldība](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
