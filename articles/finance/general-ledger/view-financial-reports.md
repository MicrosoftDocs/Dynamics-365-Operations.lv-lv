---
title: Skatīt finanšu pārskatus
description: Šajā rakstā ir aprakstīts, kā skatīt un apskatīt finanšu pārskatus Microsoft Dynamics 365 Finansēs. Tas ietver informāciju par dažādām opcijām, kuras varat lietot finanšu atskaitēm, lai mainītu to izskatu un tajās ietvertos datus.
author: kweekley
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f932bbef2543e4894c65b9a04c1ef66f1b3ab8e
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802396"
---
# <a name="view-financial-reports"></a>Skatīt finanšu pārskatus

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā skatīt un apskatīt finanšu pārskatus. Tas ietver informāciju par dažādām opcijām, kuras varat lietot finanšu atskaitēm, lai mainītu to izskatu un tajās ietvertos datus.

## <a name="financial-reporting-overview"></a>Finanšu atskaišu veidošanas apskats

## <a name="open-a-financial-report"></a>Finanšu pārskata atvēršana
Lai atvērtu pārskatu, atlasiet pārskata nosaukumu. Kad pārskatu atverat pirmo reizi, tas tiek automātiski ģenerēts par iepriekšējo mēnesi. Piemēram, ja atskaiti pirmo reizi atverat 2020. gada augustā, šī atskaite tiek ģenerēta par 2020. gada 31. jūliju. Pēc pārskata atvēršanas varat sākt to pētīt, detalizējot konkrētus datus un mainot pārskata opcijas.

## <a name="drill-down-on-a-financial-report"></a>Finanšu pārskata datu skatīšana detaļās
Finanšu pārskati var ietvert vairākus detalizācijas līmeņus. Finanšu līmenis ir pirmais līmenis, ko redzat, atverot finanšu pārskatu. Lai dotos uz konta līmeni, atlasiet datus, ko vēlaties skatīt detalizēti. Piemēram, lai skatītu detalizētu pārdošanas konta informāciju, atlasiet izvēršamos pārdošanas datus. No konta līmeņa varat ritināt lejup, lai skatītu transakcijas, kas veido konta bilanci. Transakcijas var skatīt divos veidos: pārskata transakcijas un dokumentu transakcijas.

-   **Pārskata transakcijas** — transakcijas parādās formatētā skatā, kas tiek iekļauts finanšu pārskatā. Lai skatītu transakcijas formatētā skatā, atlasiet detalizēti skatāmos datus un pēc tam noklikšķiniet uz **Rādīt detalizēti līdz pārskata transakciju līmenim**.
-   **Dokumentu transakcijas** — tiek atvērts dokumenta transakcijas pieprasījums, kur var skatīt transakcijas. Lai transakcijas skatītu dokumenta transakcijas pieprasījumā, atlasiet detalizēti skatāmos datus un pēc tam noklikšķiniet uz **Atvērt konta transakcijas**.

Ja dati ir budžeta dati, varat atvērt budžeta konta ierakstus. Lai aizvērtu jebkuru pārskata līmeni un atgrieztos sākuma punktā, varat nospiediest taustiņu Esc vai augšējā labajā pusē noklikšķināt uz pogas **Aizvērt** (**X**).

## <a name="change-report-options"></a>Pārskata opciju maiņa
Varat lietot atribūtu un dimensiju filtrus vai mainīt budžeta scenāriju pārskatā **Faktiskās pret budžeta**. Darbību rūti noklikšķiniet uz **Pārskata opcijas** un pēc tam izpildiet vienu vai vairākas no tālāk minētajām darbībām.

-   Lai pārskatam lietotu atribūta filtrus, atlasiet **Pievienot atribūta filtru**. Atlasiet atribūtu, ierakstiet atribūta vērtību un tad noklikšķiniet uz **Labi**. Piemēram, atlasot atribūtu **Konta kategorija**, ievadiet **PĀRDOŠANA** kā atribūta vērtību. Lai noņemtu atribūtu filtru, noklikšķiniet uz **Notīrīt**.
-   Lai pārskatam lietotu dimensiju filtrus, atlasiet **Pievienot dimensiju filtru**. Atlasiet dimensiju un pēc tam vai nu ierakstiet dimensijas ID, vai atlasiet dimensiju sarakstā. Lai noņemtu dimensiju filtru, noklikšķiniet uz **Notīrīt**.
-   Lai mainītu scenāriju pārskatā **Faktiskās pret budžeta**, atlasiet jaunu scenāriju un pēc tam noklikšķiniet uz **Labi**. Ja atlasītais scenārijs ir citam finanšu gadam, netiks atgriezti nekādi rezultāti. Piemēram, ja tiek ģenerēts pārskats gadam FY2015 un pašreizējais scenārijs ir paredzēts gadam FY2020, un ja jaunais scenārijs tiek atlasīts gadam FY2016, netiek atgriezti nekādi rezultāti. Ja ir nepieciešams jauns scenārijs citam finanšu gadam, ģenerējiet jaunu pārskata versiju ar attiecīgo scenāriju saistītajam finanšu gadam.

Noklikšķinot uz **Labi**, pārskatā tiek lietotas visas atlasītās opcijas. Ja izlemjat, ka nevēlaties lietot atlasītās opcijas, noklikšķiniet uz **Atcelt**.

## <a name="update-a-financial-report"></a>Finanšu pārskata atjaunināšana
Varat atsvaidzināt (atjaunināt) finanšu pārskatu, lai tajā parādītu jaunākos datus par periodu un gadu, kam pārskats tika ģenerēts. Piemēram, ja atjaunināt finanšu atskaiti, kas tika ģenerēta 2020. gada oktobrim, šī atskaite atspoguļo visas jaunās transakcijas, kas tika grāmatotas 2020. gada oktobrim. Lai atjauninātu finanšu atskaiti, darbību rūti noklikšķiniet uz **Atsvaidzināt**. Atjauninātais pārskats ir pieejams tikai tai personai, kas to atjaunina. Lai citas personas skatītu šos datus, pārskats ir jāpublicē.

## <a name="publish-a-financial-report"></a>Finanšu pārskata publicēšana
Pēc finanšu pārskata atjaunināšanas to var publicēt. Citas personas organizācijā varēs to skatīt. Lai publicētu pārskatu, darbību rūti noklikšķiniet uz **Publicēt**.

## <a name="display-a-financial-report-in-a-different-currency"></a>Finanšu pārskata parādīšana citā valūtā
Jebkurā laikā finanšu pārskatu var parādīt jebkurā valūtā. Lai pārskatu parādītu citā valūtā, darbību rūtī noklikšķiniet uz **Valūta** un pēc tam atlasiet valūtu. Pārskats tiek pārveidots izvēlētajā valūtā un rezultāti tiek parādīti. Valūtas kodi vai simboli, kas ir iekļauti pārskata noformējumā, tiek atjaunināti, lai atspoguļotu jauno valūtu. Valūtas, kuras tiek rādītas sarakstā, ir pārskata valūtas, kas ir konfigurētas programmā Finance.

## <a name="display-a-summarized-view-of-the-financial-report"></a>Finanšu pārskata kopskata parādīšana
Finanšu pārskats var ietvert detalizētas rindas un kopsavilkuma rindas. Detalizētās rindas ir rindas, kas ietver galvenos kontus vai dimensijas. Kopsavilkuma rindas ir apraksts, kopsumma un aprēķina rinda. Lai parādītu tikai pārskata kopsavilkuma rindas, noklikšķiniet uz **Rādīt** un pēc tam noklikšķiniet uz **Tikai kopsavilkuma rindas**. Pārskats tiek sakļauts un tiek parādītas tikai kopsavilkuma rindas. Lai skatītu detalizētas rindas kopā ar kopsavilkuma rindām, noklikšķiniet uz **Rādīt** un pēc tam vēlreiz noklikšķiniet uz **Tikai kopsavilkuma rindas**.

## <a name="print-a-financial-report"></a>Finanšu pārskata drukāšana
Drukājot finanšu pārskatu, tiek izveidots PDF formāta fails, ko pēc tam var manuāli izdrukāt. Lai izveidotu drukājamu finanšu pārskatu, darbību rūtī noklikšķiniet uz **Drukāt** un pēc tam izpildiet vienu vai vairākas no tālāk minētajām darbībām, lai iestatītu drukas opcijas.

-   Lai drukātajā pārskata iekļautu dažādus detalizācijas līmeņus, iestatiet slīdni **Jā** vai **Nē**. Ja pārskats izmanto pārskata koku, var izvēlēties, vai iekļaut visus pārskata vienumus vai tikai pašreizējo pārskata vienumu.
-   Lai iestatītu lappuses izmērus, sarakstā atlasiet lappuses izmērus.
-   Lai iestatītu lappuses izkārtojumu, sarakstā atlasiet izkārtojumu. Ja vēlaties, lai pārskata saturs tiktu ietilpināts lappusē atbilstoši atlasītajam platumam, iestatiet slīdni uz **Jā**.
-   Lai iestatītu lappuses piemales, ierakstiet augšējās, apakšējās, kreisās un labās piemales lielumu collās.

Kad esat pabeidzis iestatīt drukas opcijas, noklikšķiniet uz **Drukāt**, lai turpinātu un saņemtu uzvedni ar jautājumu, vai vēlaties failu lejupielādēt vai saglabāt pakalpojumā OneDrive vai SharePoint. Ja izlemjat, ka nevēlaties tirpināt, tā vietā noklikšķiniet uz **Atcelt**. Kad turpināt, serverī tiek sākta pārskata atveidošana un jums tiek parādīta uzvedne ar aicinājumu lejupielādēt pārskatu PDF formātā. Tagad varat skatīt pārskatu PDF skatītājā, kur varat atlasīt printeri, uz kuru ir jāsūta pārskats, un veikt jebkādus drukas opciju papildu pielāgojumus.

## <a name="export-a-financial-report"></a>Finanšu pārskata eksportēšana
Lai eksportētu finanšu pārskatu, darbību rūti noklikšķiniet uz **Eksportēt**. Pārskats tiks eksportēts programmā Microsoft Excel, un pārlūkprogrammā tiks parādīts aicinājums atvērt vai saglabāt eksportēto failu. Eksporta iestatījumi, kas tiek definēti pārskata noformējumā, tiek lietoti eksportētajam pārskatam.    

## <a name="additional-resources"></a>Papildu resursi

[Finanšu pārskatu veidošana](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
