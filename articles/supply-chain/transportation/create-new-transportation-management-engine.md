---
title: Jaunas transportēšanas pārvaldības programmas izveide
description: Šajā tēmā ir aprakstīts, kā izveidot jaunu transportēšanas pārvaldības programu Dynamics 365 Supply Chain Management.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be52c6afb66e88b36f3b2cdf5af14e17b3d3005f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678127"
---
# <a name="create-a-new-transportation-management-engine"></a>Jaunas transportēšanas pārvaldības programmas izveide

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izveidot jaunu transportēšanas pārvaldības programu Dynamics 365 Supply Chain Management. 

Transportēšanas pārvaldības (TMS) programmas definē loģiku, ko izmanto, lai izveidotu un apstrādātu transportēšanas likmes transportēšanas pārvaldības procesā. Supply Chain Management nodrošina vairākus dažādus programmas tipus, kas aprēķina dažādus parametrus, piemēram, likmes, tranzīta laikus un zonu skaitu, kas tiks šķērsotas tranzīta laikā. Šajā rakstā skaidrots, kā izmantot Microsoft Visual Studio izstrādes vidi kopā ar Supply Chain Management izstrādes rīkiem, lai izveidotu un izvietotu jaunu TMS programmu, un tad kā iestatīt programmu Operācijās. Plašāku informāciju par programmām skatiet [Transportēšanas pārvaldības programmas](transportation-management-engines.md).

## <a name="create-a-new-tms-engine"></a>Izveidot jaunu TMS programmu

Šajā sadaļā skaidrots, kā izveidot klašu bibliotēku, kam ir TMS programmas ieviešana, un kā uz to atsaukties no Supply Chain Management modeļa.

1. Lai izvietotu jaunās programmas, jums jābūt modelim, kas saturēs programmas. Izvēlnē **Dynamics 365** &gt; **Modeļu pārvaldība** noklikšķiniet uz **Izveidot modeli**, lai izveidotu jaunu modeli. **Modeļa izveides** ceļveža pirmajā lapā nosauciet modeli par **TMSEngines**. 

   [![Modeļa izveide.](./media/012.png)](./media/012.png)

2. Nākamajā lapā atlasiet **Izveidot jaunu pakotni**. 

   [![Jaunas pakotnes izveide.](./media/021.png)](./media/021.png)

3. Nākamajā lapā atlasiet modeli **ApplicationSuite**, uz kuru ir atsauce. (Ir iepriekša atlasīts modelis **ApplicationPlatform**.) 

   [![Modeļa atlasīšana atsaucei.](./media/032.png)](./media/032.png)

4. Nākamajā lapā noklikšķiniet uz **Pabeigt**, lai apstiprinātu jauna modeļa izveidi. 

   [![Pabeigt modeļa izveidi.](./media/042.png)](./media/042.png)

5. Jaunā risinājumā izveidojiet jaunu Supply Chain Management projektu un nosauciet to par **TMSThirdParty**. Projekta rekvizītos iestatiet projekta modeli uz **TMSEngines**.
6. Pievienojiet risinājumam jaunu C\# klašu bibliotēku un nosauciet to par **ThirdPartyTMSEngines**.
7. Projektā ThirdPartyTMSEngines pievienojiet atsauces Supply Chain Management raksturīgām komplektācijām:
   -   Programmas komplektācijas, kas iespējo atsauces uz X++ tipiem. Šīs komplektācijas var atrast šādās vietās. \[Pakotnes sakne\] ir ceļš uz vietu, kur tiek novietotas visas izvietotās komplektācijas, piemēram, C:\\Pakotnes.

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   Struktūras komplektācijās, kas iespējo piekļuvi datiem, LINQ un papildu funkcijām. Visas šīs komplektācijas var atrast nodalījumā \[Pakotņu saknes\]\\.

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   TMS komplektācijas kodols (kas satur programmas) un TMS bāzes komplektācija (kas satur palīgus, konstantes, datu pārsūtīšanas klases definīcijas utt). Šīs komplektācijas var atrast šādās vietās.

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. Pārdēvējiet C\#klasi, kas projektā ThirdPartyTMSEngines automātiski ģenerēta par **SampleRatingEngine**.
9. Ieviesiet programmu. Tā kā šajā piemērā veidojam likmes programmu, mēs pārmantojam no likmes programmas pamatklases. Pamatklase ievieš lielāko likmes programmas interfeisa daļu (**TMSFwkIRateEngine**). Mums tikai jāievieš likmes metode. Lai saglabātu šo piemēru vienkāršu, mēs padarām šo metodi par stingri kodētu likmi 100. Varat izveidot programmas, kas ievieš jebkuru no programmas interfeisiem, piemēram, **TMSFwkIAccessorialEngine**. Visi programmas interfeisi ir definēti X++.

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. Veidot risinājumu.
11. Pievienojiet jaunu atsauci projektam TMSThirdParty. Atsaucei ir jānorāda uz ThirdPartyTMSEngines projektu. Pēc risinājuma pabeigšanas tas izskatītos šādi. 

    [![Risinājums, kas ietver atsauci uz projektu TMSThirdParty.](./media/052.png)](./media/052.png)

12. Veidot risinājumu. Pārbaudiet, vai jaunā bibliotēka parādās Application Explorer zarā **Atsauces**. 

    [![Jaunā Application Explorer atsauču zara bibliotēka.](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>Izvietot TMS programmu kā pakotni

Viens veids, kā izvietot trešās puses TMS programmas, ir caur izvietošanas pakotni. Šī pieeja ir ieteicama ražošanas vidē. Izstrādes vidē varat manuāli kopēt komplektācijas, kā aprakstīts nākamajā sadaļā "TMS programmas iestatīšana Supply Chain Management." Lai izvietotu programmu kā pakotni, izpildiet tālāk aprakstītos norādījumus.

1. Izvēlnē **Dynamics 365** &gt; izvēlnē **Izvietot** noklikšķiniet uz <strong>Izveidot izvietošanas pakotni</strong>.
2. Dialoglodziņā **Izveidot izvietošanas pakotni** atlasiet TMSEngines modeli un ievadiet ceļu uz vietu, kur vēlaties glabāt pakotnes failus. 

   [![TMSEngines modeļa atlasīšana.](./media/071.png)](./media/071.png)

3. Tagad varat izvietot pakotni mērķa vidē. Informāciju par apmācību skatiet sadaļā [Izvietojamas pakotnes instalēšana](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md).

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>Iestatīt TMS programmu Supply Chain Management

Šajā sadaļā skaidrots, kā iestatīt Supply Chain Management, lai izmantotu TMS programmu, un parāda, kā jaunā programma, ko esam izveidojuši, tiek izmantota likmes iepirkšanā. Šajā piemērā tiek izmantots USMF paraugdatu uzņēmums.

1. Izveidojiet jaunu programmu, kā tas ir aprakstīts sadaļā "Izveidot jaunu TMS programmu".
2. Veidot savu risinājumu.
3. Kopējiet iegūto montāžu Supply Chain Management servera \[AOSWebRoot\] nodalījuma binārajā vietā. **Piezīme.** Šis solis ir svarīgs tikai izstrādes vidē. Ražošanas vidē jums ir jāizvieto, izmantojot izvietošanas pakotni. Norādījumus skatiet iepriekšējā sadaļā "TMS programmas izvietošana kā pakotne."
4. Supply Chain Management lapā **Likmes programmas** izveidojiet jaunu likmju programmu. Programma norāda uz programmas komplektāciju, ko saražo, veidojot programmas klases bibliotēku un jūsu ieviesto programmas klasi. 

   [![Izveidojeit jaunu vērtēšanas programmu Likmju programmu lapā.](./media/081.png)](./media/081.png)

5. Izveidojiet sūtījuma pārvadātāju, kas izmanto parauga likmes programmu. Tā kā mūsu programma neizmanto nekādus datus, likmes šablons nav jāpiešķir. 

   [![Jauna nosūtījumu pārvadātāja izveide.](./media/092.png)](./media/092.png)

6. **Likmes un maršruta** lapā noklikšķiniet uz **Likmju pirkšana**. Jums vajadzētu redzēt 100,00 likmi no SampleCarrier, kā parādīts šajā ekrānuzņēmumā. Šajā piemērā mēs novērtējam iepirkšanos maršrutam no noliktavas 24 līdz debitoram US-004. Tomēr, tā kā likme ir stingri kodēta, vienmēr redzēsit likmi 100,00.

   [![Likmju un maršrutu rīks.](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>Padomi un ieteikumi

- Ja izmantojat izstrādes rīkus Supply Chain Management, ir noderīgi savam risinājumam pievienot jaunu projektu. Ja iestatāt šo projektu kā starta projektu un startējat atkļūdošanas sesiju, tajā pašā atkļūdošanas sesijā atkļūdošanai var atkļūdot gan X++, gan C\#kodu.
- Katru reizi mainot un pārkompilējot savu ThirdPartyTMSEngines projektu, iegūtā montāža ir manuāli jākopē binārajā atrašanās vietā vai jāizvieto, izmantojot izvietošanas pakotni. Pretējā gadījumā var palaist programmu, izmantojot novecojušu komplektāciju.
- Pēc TMS raksturīgo operāciju izpildes Supply Chain Management, interneta informācijas pakalpojumu (IIS) darbinieka process var bloķēt ThirdPartyTMSEngines komplektāciju, lai to nevarētu atjaunināt. Šajā gadījumā restartējiet w3svc procesu.

### <a name="whitepaper"></a>Tehniskais dokuments

Lai iegūtu plašāku informāciju, lejupielādējiet tālāk norādīto papīru (rakstīts AX 2012 atbalstam, bet joprojām tiek piemērots Dynamics 365 Supply Chain Management)

- [Transportēšanas pārvaldības programmu ieviešana un izvietošana](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]