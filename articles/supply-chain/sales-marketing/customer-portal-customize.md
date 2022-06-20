---
title: Debitoru portāla pielāgošana un izmantošana
description: Šajā rakstā ir paskaidrots, kā pielāgot debitoru portālu pēc tā pievienošanas sistēmai.
author: Henrikan
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 85ec4beda2efe62ff5076a5ed694efbc47c6d87f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878879"
---
# <a name="customize-and-use-the-customer-portal"></a>Debitoru portāla pielāgošana un izmantošana

[!include [banner](../includes/banner.md)]


Šajā rakstā aprakstītas dažādas lapas, kas pieejamas lodziņā Debitoru portāls. Ir paskaidrots, ko dara lapas un kā tās var pielāgot.

Debitora portāls standarta variantā piedāvā dažas tīmekļa lapas un darbības. Vietnes kartē zemāk ir sniegts pārskats par šīm tīmekļa lapām un darbībām, kā arī lomām, kas var veikt darbības.

![Debitoru portāla vietnes karte.](media/customer-portal-site-map.png "Debitoru portāla vietnes karte")

## <a name="typical-customizations"></a>Parastie pielāgojumi

Tālāk sniegtie raksti palīdzēs jums uzzināt pamata par portiem Power Apps un veidu, kā varat pielāgot portālus:

- [Darbs ar veidnēm](/powerapps/maker/portals/work-with-templates) – šis raksts sniedz vispārīgu pārskatu par to, Power Apps kā portāls darbojas un kā jūs varat veikt vienkāršus portālu pielāgojumus.
- [Pārvaldīt portāla saturu](/dynamics365/portals/manage-portal-content) – šajā rakstā skaidrots, kā varat pārvaldīt un pielāgot saturu, ko izmantojat jūsu portālā.
- [Rediģēt CSS](/powerapps/maker/portals/edit-css) – šis dokuments palīdz veikt sarežģītākus pielāgojumus portāla lietotāja interfeisam (UI).
- [Izveidojiet tēmu savam portālam](/dynamics365/portals/create-theme) – šis raksts palīdz izveidot jūsu portāla UI tēmu.
- [Viegli izveidot un atklāt portāla saturu](/dynamics365/portals/create-expose-portal-content) – šis raksts palīdz pārvaldīt pamatdatu un tabulas, ko izmantojat jūsu portālam.
- [Konfigurējiet kontaktpersonu izmantošanai portālā](/powerapps/maker/portals/configure/configure-contacts) – šajā rakstā skaidrots, kā izveidot un pielāgot lietotāju lomas, un kā drošības un autentifikācijas darbs Power Apps portālā.
- [Piezīmju konfigurēšana tabulu formām un tīmekļa formām](/powerapps/maker/portals/configure-notes) portālā – šajā rakstā skaidrots, kā pievienot dokumentus un papildu krātuvi jūsu portālam.
- [Kļūdu apstrāde portāla vietnei](/powerapps/maker/portals/admin/view-portal-error-log) – šajā rakstā skaidrots, kā skatīt portāla kļūdu žurnālus un uzglabāt tos savā Microsoft Azure BLOB glabāšanas kontā.

## <a name="customize-the-order-creation-process"></a>Pasūtījuma izveides procesa pielāgošana

Kad lietotājs iesniedz pasūtījumu, izmantojot Debitoru portālu, pasūtījums tiek automātiski sinhronizēts atbilstošajā Dynamics 365 Supply Chain Management vidē. Tā kā lietotājs ir ārējs debitors, daļa nepieciešamās informācijas ar nolūku no viņa ir slēpta. Šī informācija automātiski tiks aizpildīta, iesniedzot veidlapu.

Šajā sadaļā ir parādīts, kā jāiestata kontaktpersonas, lai izvairītos no kļūdām. Tajā ir paskaidroti lauki, kas tiek iestatīti automātiski, un tas, kā vajadzības gadījumā var modificēt šo lauku vērtību.

### <a name="the-out-of-box-order-creation-process"></a>Standarta pasūtījuma izveides process

Tālāk ir norādītas standarta darbības pasūtījuma iesniegšanai no Debitoru portāla.

1. Sākumlapā atlasiet elementu **Izveidot pasūtījumu**, lai atvērtu vedni **Izveidot pasūtījumu**.
1. Lapā **Pasūtījuma informācija** iestatiet tālāk minētos laukus.

    - **Pieprasītais saņemšanas datums** — norādiet piegādes datumu.
    - **Piegādes adrese** — ievadiet adresi, uz kuru jāpiegādā pasūtījums.
    - **Uzņēmums** — atlasiet debitora uzņēmuma nosaukumu. Šis lauks tiek automātiski iestatīts lietotājiem, kuri nav administratori.
    - **Pieprasījuma numurs** — ievadiet pasūtījuma pieprasījuma numuru. Šis lauks nav obligāts.
    - **Nosūtīt uz valsti/reģionu** — ievadiet valsti vai reģionu, uz kuru tiks nogādāti krājumi. Šis lauks tiek automātiski iestatīts lietotājiem, kuri nav administratori.

    ![Pasūtījuma informācijas lapa.](media/customer-portal-order-information.png "Pasūtījuma informācijas lapa")

1. Atlasiet **Nākamais**.
1. Lapā **Krājumi** atlasiet **Pievienot krājumu**.

    ![Krājumu lapa.](media/customer-portal-items.png "Krājumu lapa")

1. Dialoglodziņā **Krājumu informācija** iestatiet tālak norādītos laukus.

    - **Preces nosaukums** — atrodiet un atlasiet preci, ko pievienot pasūtījumam.
    - **Daudzums** — ievadiet atlasītās preces daudzumu.
    - **Vienība** — norādiet mērvienību (piemēram, **ea.**, **kg** vai **kaste**).
    - **Prognozētā neto summa** — vērtība tiek aprēķināta kā krājuma paredzētā cena × atlasītās vienības daudzums.

    ![Dialoglodziņš Krājumu informācija.](media/customer-portal-item-information.png "Dialoglodziņš Krājumu informācija")

1. Atlasiet **Labi**, lai pievienotu krājumu pasūtījumam.
1. Atkārtojiet 4.–6. darbību, līdz esat pievienojis visus krājumus, ko vēlaties pasūtīt.
1. Kad esat pabeidzis krājumu pievienošanu, lapā **Krājumi** atlasiet **Tālāk**.
1. Lapā **Informācija par pasūtījumu** ir sniegts pasūtījuma kopsavilkums. Pārskatiet pasūtījuma saturu un informāciju par piegādi. Ja viss izskatās pareizi, atlasiet **Iesniegt**, lai iesniegtu pasūtījumu.

    ![Pabeigta pasūtījuma informācijas lapa.](media/customer-portal-order-submit.png "Pabeigta pasūtījuma informācijas lapa")

### <a name="standard-data-setup"></a>Standarta datu iestatīšana

Lai palīdzētu nodrošināt sekmīgu lietotāja pieredzi, Debitoru portāls automātiski aizpilda vērtības vairākos obligātos laukos. Šīs vērtības ir pamatotas uz informāciju klienta kontaktpersonas, kas iesniedz pasūtījumu, ierakstu.

Katrai [kontaktpersonas rindai](/powerapps/maker/portals/configure/configure-contacts), kas attiecas uz klientu, kurš izmantos Debitoru portālu pasūtījuma iesniegšanai, ir jānorāda vērtības tālāk minētajiem obligātajiem laukiem. Pretējā gadījumā radīsies kļūdas.

- **Uzņēmums** — juridiskā persona, kam pieder pasūtījums
- **Potenciālais debitors** — debitora konts, kas saistīts arpasūtījumu
- **Cenu saraksts** — debitoram pielāgoto cenu saraksts
- **Valūta** — cenas valūta
- **Nosūtīt uz valsti/reģionu** — valsti vai reģions, uz kuru tiks nogādāti krājumi

Tālāk minētie lauki tiek automātiski iestatīti pārdošanas pasūtījuma tabulai:

- **Valoda** — pasūtījuma valoda (pēc noklusējuma vērtība tiek ņemta no kontaktpersonas ieraksta).
- **Nosūtīt uz valsti/reģionu** — valsts vai reģions, uz kuru tiks nogādāti krājumi (pēc noklusējuma vērtība tiek ņemta no kontaktpersonas ieraksta.)
- **Kontaktpersona** — lietotājs, ar kuru var sazināties, lai iegūtu informāciju par pasūtījumu (pēc noklusējuma vērtība tiek ņemta no kontaktpersonas ieraksta.)
- **Uzņēmums** — juridiska persona, kurai pieder pasūtījums (pēc noklusējuma vērtība tiek ņemta no kontaktpersonas ieraksta.)
- **Potenciālais debitors** — debitora konts, kas ir saistīts ar pasūtījumu (pēc noklusējuma vērtība tiek ņemta no kontaktpersonas ieraksta.)
- **Rēķina debitors** — pasūtījuma norēķinu konts (pēc noklusējuma vērtība ir potenciālais debitors kontaktpersonas ieraksta.)
- **Pārdošanas pasūtījuma nosaukums** — pārdošanas pasūtījuma nosaukums (noklusētā vērtība ir **pārdošanas pasūtījums**.)
- **Valūta** — cenas valūta (pēc noklusējuma vērtība tiek ņemta no kontaktpersonas ieraksta).
- **Cenu saraksts** — pielāgoto cenu saraksts debitoram (pēc noklusējuma vērtība tiek ņemta no kontaktpersonas ieraksta).
- **Piegādes adreses apraksts** — pārdošanas pasūtījuma piegādes adrese (noklusējuma vērtība ir **piegādes adreses apraksts**).

### <a name="modify-the-order-creation-process"></a>Pasūtījuma izveides procesa modificēšana

Varat brīvi modificēt Debitoru portāla izskatu un lietotāja interfeisu, ja nemaināt pasūtījuma izveides pamata procesu. Ja vēlaties mainīt pasūtījuma izveides procesu, ir dažas lietas, kas jāpatur prātā.

Nenoņemiet tālāk norādītos laukus no pārdošanas pasūtījuma tabulas pakalpojumā Microsoft Dataverse, jo tie ir nepieciešami, lai izveidotu pārdošanas pasūtījumu duālajā ierakstā:

- **Uzņēmums** — juridiskā persona, kam pieder pasūtījums
- **Nosaukums** — pārdošanas pasūtījuma nosaukums
- **Valūta** — cenas valūta
- **Cenu saraksts** — debitoram pielāgoto cenu saraksts
- **Nosūtīt uz valsti/reģionu** — valsti vai reģions, uz kuru tiks nogādāti krājumi
- **Potenciālais debitors** — debitora konts, kas saistīts arpasūtījumu
- **Valoda** — pasūtījuma valoda (parasti šī valoda ir potenciālā debitora valoda).
- **Piegādes adreses apraksts** — pārdošanas pasūtījuma piegādes adrese

Krājumiem ir nepieciešamas tālāk minētas kolonnas:

- **Prece** — pasūtījumā norādītā prece
- **Daudzums** — atlasītās preces daudzums
- **Vienība** — mērvienība (piemēram, **ea.**, **kg** vai **kaste**)
- **Nosūtīt uz valsti/reģionu** — piegādes valsts vai reģions
- **Piegādes adreses apraksts** — pasūtījuma piegādes adrese

Jums ir jāpārliecinās, ka jūsu Debitoru portālā kaut kādā veidā tiek iesniegtas vērtības visām tālāk minētajām kolonnām.

Ja vēlaties pievienot lapai kolonnas vai noņemt tās, skatiet [Ātrās izveides veidlapu izveide vai rediģēšana racionalizētai datu ievades pieredzei](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).

Ja vēlaties mainīt to, kā ir priekšiestatītas kolonnas un kā tiek iestatītas vērtības, kad lapa tiek saglabāta, skatiet tālāk norādīto informāciju Power Apps portālu dokumentācijā:

- [Lauka iepriekšēja aizpildīšana](/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [Vērtības iestatīšana saglabāšanai](/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a>Sākumlapas pielāgošana

Visas Debitoru portālā esošās vadīklas ir iebūvētas Power Apps portālu vadīklas. Varat tos pielāgot, izpildot darbības, kas aprakstītas [Lapas definēšana](/powerapps/maker/portals/compose-page) Power Apps portālu dokumentācijā.

Tikai pielāgota vadīkla, kas ir iekļauta Debitoru portāla veidnē, tiek izmantota, lai izveidotu elementus sākumlapā.

![Elementi sākumlapā.](media/customer-portal-home-page-tiles.png "Elementi sākumlapā")

Lai modificētu elementus, veiciet tālāk noradītās darbības.

1. Atveriet [Portāla pārvaldības programma](/powerapps/maker/portals/configure/configure-portal).
1. Navigācijas rūtī kreisajā pusē atlasiet **Lapas veidnes**.

    ![Portāla pārvaldības navigācijas rūts.](media/customer-portal-nav.png "Portāla pārvaldības navigācijas rūts")

1. Atlasiet lapas veidni, kuras nosaukums ir **Sākums**.
1. Laukā **Tīmekļa veidne** atlasiet saiti **Sākums**, lai atvērtu šīs lapas pirmkodu.

    ![Tīmekļa veidnes lauks.](media/customer-portal-web-template.png "Tīmekļa veidnes lauks")

1. Tagad jums vajadzētu redzēt visu šīs sākumlapas pirmkodu un varat to modificēt pēc vajadzības.

## <a name="resources"></a>Resursi

Lai uzzinātu vairāk par to, kā varat iestatīt un pielāgot Debitoru portālu, skatiet tālāk norādītos resursus.

- [Power Apps portālu dokumentācija](/powerapps/maker/portals/overview)
- [Duālā ieraksta dokumentācija](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [Par portāla dzīves ciklu](/powerapps/maker/portals/admin/portal-lifecycle)
- [Portāla jaunināšana](/powerapps/maker/portals/admin/upgrade-portal)
- [Portāla konfigurācijas migrācija](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Risinājuma dzīves cikla pārvaldība: programma Dynamics 365 for Customer Engagement](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]