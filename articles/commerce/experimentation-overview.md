---
title: Eksperimentēšana pakalpojumā Dynamics 365 Commerce
description: Eksperimentēšana ļauj veidot, rediģēt un pārvaldīt lapu izkārtojumu un satura apstrādi vietnes veidotājā. E-komercijas lapām un lapas entītijām ir iespējots nepārtraukts eksperimentēšanas atbalsts.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: overview
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1ef877072ba7ffe1b0326cf8d526b512b5ab30b8
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946218"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Eksperimentēšana pakalpojumā Dynamics 365 Commerce
Izmantojiet eksperimentēšanu pakalpojumā Dynamics 365 Commerce, lai pārbaudītu hipotēzi par jūsu e-komercijas lapu efektivitāti un pieņemtu lēmumus, pamatojoties uz datiem. Commerce atbalsta A/B testēšanu lapās, moduļos un fragmentos un ļauj novērtēt piedāvāto izmaiņu ietekmi uz jūsu tīmekļa vietni.

Varat veidot, rediģēt un pārvaldīt lapu un satura apstrādi, ko sauc par **variantiem** Commerce vietņu veidotājā. Commerce ir integrēts trešās puses pakalpojumos, ko varat izmantot eksperimentu izveidošanai un apstrādes uzdevumiem. Pakalpojumā Commerce tvertās reāllaika notikumu straumes iespējo analīzi, kas definē eksperimenta rezultātus trešās puses pakalpojumā. Pēc tam šo analīzi varat izmantot, lai palīdzētu atbalstīt vai atspēkot jūsu hipotēzi.

## <a name="set-up-prerequisites"></a>Priekšnoteikumu iestatīšana

1. **Pareizās Commerce versijas iegūšana** — jauniniet savu moduļu bibliotēku, tiešsaistes kanāla paplašināmības programmatūras izstrādes komplektu (SDK) un Commerce Scale Unit uz Commerce versiju 10.0.13 vai jaunāku.
1. **Eksperimenta savienotāja iestatīšana** – eksperimenta savienotājs ļauj Commerce izveidot savienojumu ar trešās puses pakalpojumiem, lai izgūtu eksperimentu sarakstu un noteiktu, kad lietotājam jāparāda eksperiments. Varat iegādāties trešās puses savienotāju pakalpojumā [AppSource](https://appsource.microsoft.com). Sekojiet izdevēja nodrošinātajām iestatīšanas instrukcijām. Kā alternatīvu var izmantot testa savienotāja paraugu no Commerce, lai testētu eksperimenta darbplūsmu, bez nepieciešamības konfigurēt ārēju pakalpojumu. Papildinformāciju skatiet sadaļā [Savienotāju konfigurēšana un iespējošana](e-commerce-extensibility/connectors.md). 
1. **Aktivizējiet** eksperimenta iezīmes karodziņu Commerce - **\>** Varat aktivizēt eksperimentu īrnieka līmenī, dodoties uz nomnieka iestatījumu līdzekļiem vai atrašanās vietas līmenī, **dodoties uz vietnes iestatījumu \> līdzekļiem**. Lai sāktu moduļa **variāciju** izveidi, grieziet karodziņu Eksperimentu karogi. Šī karodziņa atspējošana pārtrauc visu eksperimentu rādīšanu lietotājiem un noņem visus vietnes veidotājā esošos rediģēšanas līdzekļus.
    
## <a name="experimentation-lifecycle"></a>Eksperimenta dzīves cikls

Eksperimenta iestatīšana, variantu izveide un eksperimenta izpildīšana ir iteratīvs process. Tālāk redzamajā diagrammā parādīts eksperimenta dzīves cikls pakalpojumā Commerce un trešās puses pakalpojumā. 

[ ![Eksperimenta dzīves cikls.](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Lai uzzinātu vairāk par katru soli eksperimenta procesā, skatiet sekojošos rakstus.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
