---
title: Preču personalizētu ieteikumu iespējošana
description: Šajā tēmā ir aprakstīts, kā padarīt personalizētus preču ieteikumus pieejamus klientiem risinājumā Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 74bf2c96d744b8101151be9288a956d46ce3b6885f0cb593dc1b78728b018fb4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770961"
---
# <a name="enable-personalized-recommendations"></a>Personalizētu ieteikumu iespējošana

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā padarīt personalizētus preču ieteikumus pieejamus klientiem risinājumā Microsoft Dynamics 365 Commerce.

Sistēmā Dynamics 365 Commerce mazumtirgotāji var padarīt personalizētus produktu ieteikumus (sauktus arī par personalizēšanu) pieejamus. Šādā veidā personificētus ieteikumus var iekļaut klientu tiešsaistes pieredzē un pārdošanas punktā (POS). Kad personalizācijas funkcionalitāte ir ieslēgta, sistēma var saistīt lietotāja pirkuma un preces informāciju, lai ģenerētu individualizētus preces ieteikumus.

## <a name="personalization-prerequisites"></a>Personalizācijas priekšnosacījumi

Pirms padarīt personalizētus preču ieteikumus pieejamus klientiem, ņemiet vērā, ka preču ieteikumi tiek atbalstīti tikai tiem Commerce lietotājiem, kuri migrēja to glabāšanu Azure Data Lake veikalā. Pirms klienti var saņemt personalizētus preču ieteikumus, mazumtirgotājiem ir [jāaktivizē preču ieteikumi](enable-product-recommendations.md).

> [!NOTE]
> Ieslēdzot preču ieteikumus, varat ieslēgt arī personalizāciju. Tomēr, izslēdzot personalizāciju, netiek izslēgti citi preču ieteikumu veidi.

Lai iegūtu vairāk informācijas par preču ieteikumiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).

## <a name="turn-on-personalization"></a>Personalizācijas aktivizēšana

Lai aktivizētu personalizāciju, veiciet tālāk minētās darbības.

1. Programmā Commerce Headquarters meklējiet **Funkciju pārvaldība**.
1. Atlasiet **Visi**, lai skatītu pieejamo funkciju sarakstu. 
1. Meklēšanas lodziņā ievadiet **Ieteikumi**.
1. Atlasiet līdzekli **Personalizēto preču ieteikumi**.
1. **Personalizēto preču ieteikumi** rekvizītu rūtī atlasiet **Iespējot tagad**.

![Personalizācijas aktivizēšana.](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> Ieslēdzot personalizāciju, tiek sākts personalizētu preču ieteikumu saraksta ģenerēšanas process. Var tikt pieprasīta līdz vienai dienai, pirms šie saraksti ir pieejami un redzami tiešsaistē un POS.

## <a name="personalized-lists"></a>Personalizēti saraksti

Līdztekus iespējai personalizēt esošus automātiski ģenerētus sarakstus, ieteikumu pakalpojums ļauj personalizēt produktu atklāšanas pieredzi gan tiešsaistē, gan POS.

Pēc personalizācija ir ieslēgta, tirgotāji var rādīt pircējiem personalizētus "ieteikumu" sarakstus tiešsaistē vai "ieteicams klientam" sarakstiem POS termināļos. Turklāt mazumtirgotāji var piemērot personalizāciju esošajiem preču ieteikumu sarakstiem un nodrošināt Vispārējās datu aizsardzības regulas (VDAR) atteikšanās pieredzi autentificētiem lietotājiem. Izslēdzot personalizāciju, arī šie līdzekļi tiek izslēgti.

### <a name="online-picks-for-you-lists"></a>Tiešsaistes "ieteikumu" saraksti

"Tiešsaistes" saraksts ir mākslīgā intelekta, datormācīšanās (AI-ML) saraksts, kas parāda autentificētam lietotājam personalizētu ieteikto preču sarakstu. Šis saraksts ir balstīts uz lietotāja universālā kanāla pirkšanas vēsturi. Personalizētie ieteikumi tiek dinamiski atjaunināti, kad lietotājs veic vairāk pirkumu. Šis saraksta veids atbalsta arī kategoriju filtrēšanu, lai mazumtirgotāji varētu rādīt populārākos ieteikumus, pamatojoties uz navigācijas hierarhijām.

Pirms "ieteikumu" sarakstu var parādīt jebkurā e-komercijas lapā, ir jāizpilda šādas lietotāju prasības:

- Lietotājiem ir jāpiesakās sistēmā. Anonīmie lietotāji neredzēs personalizētus ieteikumus.
- Lietotājiem ir jābūt vismaz vienam pirkumam viņu kontā.
- Lietotājiem ir jāizvēlas saņemt personalizētus ieteikumus.

Sekojošajā attēlā ir parādīts saraksts "ieteikumu" saraksts tiešsaistes veikala lapā.

![Tiešsaistes "ieteikumu" saraksts.](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a>"Klientu ieteikumu" saraksti POS

Lai uzlabotu savu klientu apkalpošanas pieredzi, mazumtirgotāji var personalizēt esošās detalizētās informācijas lapas par klientiem, pievienojot kontekstuālo "klientu ieteikumu" sarakstu.

Sekojošajā attēlā ir parādīts "klientu ieteikumu" saraksts POS terminālī.

![Klientu ieteikumu saraksts POS.](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a>Lietot personalizāciju esošajiem ieteikumu sarakstiem

Mazumtirgotāji var piemērot personalizāciju esošajiem ieteikumu sarakstiem, piemēram, "Jaunas", "Populāri", "Pirktākās", "Cilvēkiem patīk arī" un "Bieži pirktas kopā". Ja personalizācija tiek lietota esošajiem sarakstiem, vienumi, kurus iepriekš iegādājies pierakstījies lietotājs, tiek noņemti no šiem sarakstiem. Gan anonīmajiem lietotājiem, gan lietotājiem, kas izvēlējās nesaņemt personalizētus ieteikumus, tiek parādītas esošo sarakstu noklusētās versijas. Tāpēc mazumtirgotājiem nav manuāli jāuztur atsevišķas lapu iespējas.

Piemēram, pierakstījies lietotājs jau ir iegādājies melnu rokaspulksteni un brūnus darba zābakus, kas parādās "populāri-noklusējuma" sarakstā nākamajā attēlā. Tāpēc lietotājs redzēs jaunas preces, nevis šīs preces, kā norādīts sarakstā "populāri — personalizēts".

![Personalizācijas piemērošana.](./media/applypersonalization.png)

Lai piemērotu personalizāciju esošam rekomendāciju sarakstam Commerce vietnes noformētājā, rīkojieties šādi.

1. Atveriet esošu vietnes noformētāja lapu, kas satur preču ievākšanas moduli.
1. Navigācijas rūtī kreisajā pusē atlasiet produkta ievākšanas moduli.
1. Navigācijas rūtī labajā pusē sadaļā **Preces** atlasiet sarakstu.
1. Dialoglodziņā **Atlasīt preču saraksta konfigurāciju** sadaļā **Veids** atlasiet saraksta veidu.
1. Atzīmējiet izvēles rūtiņu **Piemērot personalizāciju** un pēc tam atlasiet **Labi**.

    ![Personalizācijas piemērošana populāru preču sarakstam.](./media/ApplyPersonalizationToTrending.PNG)

1. Saglabājiet lapu, pabeidziet to rediģēt un publicējiet to. Kad lapa ir publicēta, pierakstītie lietotāji redzēs personalizētus populāru preču sarakstus.

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Iespējojiet Azure Data Lake Storage pakalpojuma Dynamics 365 Commerce vidē](enable-adls-environment.md)

[Iespējot preču ieteikumus](enable-product-recommendations.md)

[Iespējot "veikala līdzīgie izskati" rekomendācijas](shop-similar-looks.md)

[Atteikšanās no personalizētiem ieteikumiem](personalization-gdpr.md)

[Pievienot preču ieteikumus punktā POS](product.md)

[Ieteikumu pievienošana transakciju ekrānam](add-recommendations-control-pos-screen.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Manuāli izveidot pārraudzītus ieteikumus](create-editorial-recommendation-lists.md)

[Izveidot ieteikumus ar demonstrācijas datiem](product-recommendations-demo-data.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
