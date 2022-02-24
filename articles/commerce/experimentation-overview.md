---
title: Eksperimentēšana pakalpojumā Dynamics 365 Commerce
description: Eksperimentēšana ļauj veidot, rediģēt un pārvaldīt lapu izkārtojumu un satura apstrādi vietnes veidotājā. E-komercijas lapām un lapas entītijām ir iespējots nepārtraukts eksperimentēšanas atbalsts.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 85eb7a661cc66c42699797cca4fa6820941de7c0
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/22/2020
ms.locfileid: "4414189"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Eksperimentēšana pakalpojumā Dynamics 365 Commerce
Izmantojiet eksperimentēšanu pakalpojumā Dynamics 365 Commerce, lai pārbaudītu hipotēzi par jūsu e-komercijas lapu efektivitāti un pieņemtu lēmumus, pamatojoties uz datiem. Commerce atbalsta A/B testēšanu lapās, moduļos un fragmentos un ļauj novērtēt piedāvāto izmaiņu ietekmi uz jūsu tīmekļa vietni.

Varat veidot, rediģēt un pārvaldīt lapu un satura apstrādi, ko sauc par **variantiem** Commerce vietņu veidotājā. Commerce ir integrēts trešās puses pakalpojumos, ko varat izmantot eksperimentu izveidošanai un apstrādes uzdevumiem. Pakalpojumā Commerce tvertās reāllaika notikumu straumes iespējo analīzi, kas definē eksperimenta rezultātus trešās puses pakalpojumā. Pēc tam šo analīzi varat izmantot, lai palīdzētu atbalstīt vai atspēkot jūsu hipotēzi.

## <a name="set-up-prerequisites"></a>Priekšnoteikumu iestatīšana
1. **Pareizās Commerce versijas iegūšana** — jauniniet savu moduļu bibliotēku, tiešsaistes kanāla paplašināmības programmatūras izstrādes komplektu (SDK) un Commerce Scale Unit uz Commerce versiju 10.0.13 vai jaunāku.
1. **Eksperimenta savienotāja iestatīšana** – eksperimenta savienotājs ļauj Commerce izveidot savienojumu ar trešās puses pakalpojumiem, lai izgūtu eksperimentu sarakstu un noteiktu, kad lietotājam jāparāda eksperiments. Varat iegādāties trešās puses savienotāju pakalpojumā [AppSource](https://appsource.microsoft.com). Sekojiet izdevēja nodrošinātajām iestatīšanas instrukcijām. Kā alternatīvu var izmantot testa savienotāja paraugu no Commerce, lai testētu eksperimenta darbplūsmu, bez nepieciešamības konfigurēt ārēju pakalpojumu. Papildinformāciju skatiet sadaļā [Savienotāju konfigurēšana un iespējošana](e-commerce-extensibility/connectors.md). 
1. **Eksperimenta līdzekļu karodziņu ieslēgšana pakalpojumā Commerce** – iespējojiet eksperimentu nomnieka līmenī, dodoties uz **Nomnieka iestatījumi > Līdzekļi** vai vietnes līmenī uz **Vietnes iestatījumi > Līdzekļi**.
    - Iespējojiet karodziņu **Eksperimentēšana**, lai izveidotu eksperimenta moduļu variantus lapā, neietekmējot vai nekopējot citu saturu, kas nav eksperimenta daļa. Tādējādi nodrošinot, ka ārpus eksperimenta notiekošie satura atjauninājumi tiek sinhronizēti eksperimenta dzīves cikla laikā. Šī karodziņa atspējošana pārtrauc visu eksperimentu rādīšanu lietotājiem un noņem visus vietnes veidotājā esošos rediģēšanas līdzekļus.
    - Iespējojiet karodziņu **Eksperimentēt ar lapām vai fragmentiem**, lai izpildītu eksperimentus lapā vai fragmentā. Tiek izveidota pilnīga visas lapas vai fragmenta kopija visiem lapas vai fragmenta moduļiem. Izmantojiet šo režīmu, ja vēlaties pārbaudīt visaptverošas satura izmaiņas vai kad notiekošo satura izmaiņu sinhronizēšana dažādās instancēs norit bez problēmām. Atspējojot šo karodziņu, tiek novērsta jaunu eksperimentu izveidošana un rediģēšana lapās un fragmentos.
    > [!NOTE]
    > Karodziņam **Eksperimentēšana** ir jābūt iespējotam arī līdzeklī **Eksperimentēt ar lapām vai fragmentiem**, lai tas darbotos.
    
## <a name="experimentation-lifecycle"></a>Eksperimenta dzīves cikls
Eksperimenta iestatīšana, variantu izveide un eksperimenta izpildīšana ir iteratīvs process. Tālāk redzamajā diagrammā parādīts eksperimenta dzīves cikls pakalpojumā Commerce un trešās puses pakalpojumā. 

[ ![Eksperimenta dzīves cikls](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Lai uzzinātu vairāk par katru eksperimenta procesa darbību, skatiet tālāk norādītās tēmas.
- [Hipotēzes identificēšana un eksperimenta rādītāju noteikšana](experimentation-identify.md)
- [Eksperimenta iestatīšana](experimentation-setup.md)
- [Eksperimenta pievienošana un rediģēšana](experimentation-connect-edit.md)
- [Eksperimenta priekšskatīšana un publicēšana](experimentation-preview-publish.md)
- [Eksperimenta izpildīšana un pārraudzīšana](experimentation-run-monitor.md)
- [Variācijas veicināšana un eksperimenta pabeigšana](experimentation-review-complete.md)

> [!NOTE]
> Lai uzzinātu, kur dzīves ciklā šobrīd atrodas eksperiments, kreisajā navigācijas rūtī vietņu veidotājā atlasiet **Eksperimenti**. Tiks parādīts eksperimentu saraksts ar katra eksperimenta statusu gan pakalpojumā Commerce, gan trešās puses pakalpojumā. Papildinformāciju skatiet sadaļā [Eksperimenta statusa pārskatīšana](experimentation-status.md).

## <a name="next-step"></a>Nākamā darbība
[Hipotēzes identificēšana un eksperimenta panākumu rādītāju noteikšana](experimentation-identify.md) 
