---
title: Mākoņa darbinātas meklēšanas pārskats
description: Šis raksts sniedz pārskatu par mākoņa cenas meklēšanu Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 02/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: ed80ff42ea5c6e6a904ea2855953d006f66aad37
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273671"
---
# <a name="cloud-powered-search-overview"></a>Mākoņa darbinātas meklēšanas pārskats

[!include [banner](includes/banner.md)]

Šis raksts sniedz pārskatu par mākoņa cenas meklēšanu Microsoft Dynamics 365 Commerce.

Preces atrodamība palīdz nodrošināt to, ka klienti var ātri un viegli atrast preces, pārlūkojot kategorijas, meklējot un filtrējot. Mazumtirgotāji apsver preču noteikšanu kā primāro rīku debitoru mijiedarbībai kanālos, ko nodrošina Mākoņa skalas vienība (CSU), piemēram, e-komercija un pārdošanas punkts (POS).

Klienti ir pieraduši pie gandrīz momentānās tīmekļa meklētājprogrammas atbildes laikiem, izsmalcinātām E-komercijas tīmekļa vietnēm, sociālajām lietotnēm, automātiskiem ieteikumiem, kas tiek parādīti, ievadot meklējamos vārdus, kategoriālās navigācijas un iezīmēšanas. Ja debitori nevar ātri atrast preci, ko tie meklē vienā e-komercijas veikalā, debitori nevarēs pāriet uz citu e-komercijas veikalu.

Mākoņainā preču pārdošanas iespēja programmā Commerce palīdz mazumtirgotājiem turpināt palielināt patērētāja ieturējumu un konvertēšanas likmes kanālos, izmantojot CSU.

Komercijas meklēšanas pieredzei ir uzlabotas iespējas, lai palīdzētu mazumtirgotājiem sasniegt labāku preču atklājamību. Tajā pašā laikā šīs iespējas nodrošina mērogojamu un veiktspēju, kas ir nepieciešama e-komercijas trafikam.

## <a name="browse-and-search"></a>Pārlūkošana un meklēšana

Meklēšanas atbilstība un veiktspēja ir galvenie faktori daudzkanālu pieredzei, jo preču atklāšana galvenokārt balstās uz meklēšanas funkcionalitāti informācijas izguves un satura navigācijas jomā. Derīga un efektīva pārlūkošanas un meklēšanas pieredze palīdz palielināt pārveidošanu.

Sekojošajā attēlā parādīts tipisks pārlūkošanas un meklēšanas funkcionalitātes piemērs.

![Ielādes lapas meklēšana.](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Kategoriālās navigācijas un izvēļu kopsavilkums 

Kategoriālā navigācija palīdz klientiem vieglāk pārlūkot saturu, ļaujot filtrēt pēc rafinētājiem, kas ir saistīti ar terminiem terminu kopā. Pēc tam, kad klients ir atlasījis un pielietojis rafinētāju, tiek parādīti izvēļu kopsavilkumi. 

Izmantojot kategoriālo navigāciju, varat konfigurēt dažādus rafinētājus dažādiem terminiem terminu kopā bez nepieciešamības izveidot papildu lapas. 

Sekojošajā attēlā parādīts piemērs, kur meklēšanā tiek izmantota kategoriālā navigācija.

![Izvēles kopsavilkums.](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Visaptveroša automātiskā piedāvāšana

Pašreizējā autosugest funkcionalitāte rāda atslēgvārdus, kas izraisa sakritības atslēgvārda meklēšanu. Uzņēmuma Commerce jauno uzlabojumu dēļ debitori bieži var skatīt saites uz precēm, pirms tie ir beidzuši ierakstīšanu.

Commerce atbalsta arī atslēgvārdu atbilstību funkcionalitāti dažādās kategorijās. Šī funkcionalitāte liek klientiem redzēt kategorijām atbilstošu atslēgvārdu skaitu un aktivizēt atslēgvārdu meklēšanu citās kategorijās.

Sekojošajā attēlā parādīts piemērs, kur tiek izmantota visaptveroša automātiskā piedāvāšana.

![visaptveroša automātiskā piedāvāšana.](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Kārtot

Kārtošanas funkcionalitāte ļauj debitoriem kārtot, meklēt un pārlūkot kategoriju rezultātus un precizēt tos pēc tādiem kritērijiem kā cena, preces nosaukums un preces numurs. Ja iespējojat [Produktu ieteikumus](product-recommendations.md) savā vidē, debitori var arī kārtot rezultātus, balstoties uz uzlabotiem kārtošanas kritērijiem, piemēram, jauniem, labākais pārdošanas un tendenču šķirošanas kritērijiem.


> [!NOTE]
> Mākoņa darbinātas meklēšanas iespējas ir pieejamas, sākot ar versiju 10.0.8. Pārliecinieties, ka "ProductSearch.UseAzureSearch" ir iestatīts uz "patiess **", kas atrodas Commerce Parameters > konfigurācijas parametri**. 
![Mākoņa darbinātas meklēšanas konfigurācijas parametri.](./media/CloudPoweredSearchConfigurationParameters.png)
>Papildu kārtošanas opcijas, piemēram, jaunas, labākā pārdošana un tendences, ir pieejamas Commerce SSK versijā 9.35+ Dynamics 365 Commerce un 10.0.20 versijā.  


## <a name="additional-resources"></a>Papildu resursi

[Noklusējuma kategorijas reklāmas mērķlapas un meklēšanas rezultātu lapas pārskats](category-search-page-overview.md)

[SEO metadatu pārvaldība](manage-seo-metadata.md)


[!INCLUDE [footer-include](../includes/footer-banner.md)]
