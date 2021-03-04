---
title: Bieži uzdotie jautājumi par preču konfigurācijas modeļu aprēķiniem
description: Šajā tēmā ir aprakstīti preču konfigurācijas modeļu aprēķini un ir paskaidrots, kā šos aprēķinus lietot kopā ar ierobežojumiem.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7fac3ec6df53dcc6e459f62f76d856a11d294b6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432444"
---
# <a name="calculations-for-product-configuration-models-faq"></a>Bieži uzdotie jautājumi par preču konfigurācijas modeļu aprēķiniem

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti preču konfigurācijas modeļu aprēķini un ir paskaidrots, kā šos aprēķinus lietot kopā ar ierobežojumiem.

Aprēķinus var izmantot aritmētisko vai loģisko operāciju veikšanai. Tie papildina izteiksmju ierobežojumus preču konfigurācijas modeļos. Aprēķinus var definēt lapā **Detalizēta informācija par ierobežojumam atbilstošu preces konfigurācijas modeli** un pēc tam izveidot izteiksmes aprēķiniem izteiksmju redaktorā. Papildu informāciju skatiet sadaļā Aprēķinu izveide.

## <a name="what-is-a-calculation"></a>Kas ir aprēķins?
Aprēķins ir elements, ko varat izmantot preču konfigurācijas modelī. Aprēķini papildina ierobežojumus, ļaujot izmantot decimālskaitļus, lai aprēķinātu vērtības preces konfigurēšanas laikā. Turklāt, aprēķiniem ir pieejama plašāka operatoru kopa nekā ierobežojumiem.  

Tāpat kā ierobežojums, arī aprēķins ir saistīts ar noteiktu preču konfigurēšanas modeļa komponentu, un to nevar izmantot atkārtoti vai koplietot ar citu komponentu. Viena svarīga atšķirība starp aprēķiniem un ierobežojumiem ir, ka aprēķini ir obligāti (vienvirziena), bet ierobežojumi ir deklaratīvi (divvirzienu). Plašāku informāciju par ierobežojumiem skatiet rakstā [Izteiksmes ierobežojumi un tabulas ierobežojumi preču konfigurācijas modeļos](expression-constraints-table-constraints-product-configuration-models.md).  

Aprēķinu veido mērķa atribūts un aprēķina izteiksme.

## <a name="what-is-a-target-attribute"></a>Kas ir mērķa atribūts?
Mērķa atribūts ir atribūts, kas saņem aprēķina izteiksmes rezultātu.  

Nākamajā izteiksmē mērķa atribūts ir galdautu mērījums.  

**Izteiksme:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]  

**DecimalAttribute1** ir tabulas garums, un **decimalAttribute2** ir galdauta garums. Šī izteiksme mērķa atribūtam atgriež vērtību **True**, ja vērtība **decimalAttribute2** ir lielāka par vai vienāda ar vērtību **decimalAttribute1**. Pretējā gadījumā izteiksme atgriež vērtību **False**. Tātad galdauta mērījums ir pieņemams, ja galdauta garums ir vienāds ar vai lielāks par galda garumu.

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a>Kādus atribūtu tipus var iestatīt mērķa atribūtiem?
Par mērķa atribūtiem var iestatīt visus atribūtu tipus, ko atbalsta preču konfigurators, izņemot tekstu bez fiksēta saraksta.

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a>Vai mērķa atribūta vērtība aprēķinā var ierobežot ievades atribūtu vērtības?
Nē, mērķa atribūta vērtība aprēķinā nevar ierobežot ievades atribūtu vērtības, jo aprēķini ir vienvirziena. Tāpēc mērķa atribūta vērtība tiek iestatīta, pamatojoties uz ievades atribūtu vērtības izmaiņām, bet mērķa vērtības izmaiņas neietekmē ievades atribūtu vērtības. Šis princips atšķiras no ierobežojumu principa. Ierobežojumi notiek abos virzienos.

### <a name="example"></a>Piemērs

Nākamajā izteiksmē aprēķina mērķis ir strāvas vada garums un ievades vērtība ir krāsa.  

**Izteiksme:** \[If Krāsa == "Zaļš", 1.5, 1.0\]  

Konfigurējot krājumu, strāvas vada garums tiek iestatīts uz **1,5**, ja kā krāsas atribūta vērtību norādāt **Zaļš**. Ja norādāt jebkuru citu krāsu, garums ir iestatīts uz **1,0**. Tomēr, tā kā aprēķini ir vienvirziena, šis aprēķins neiestata krāsas atribūta vērtību kā **Zaļa**, kad norādāt garumu **1,5**.

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a>Kas notiek, ja aprēķina mērķa atribūta tips ir vesels skaitlis, bet aprēķins ģenerē decimāldaļskaitli?
Ja mērķa atribūtam ir vesela skaitļa tips, bet aprēķins ģenerē decimālskaitli, tiek atgriezta tikai aprēķinātā rezultāta vesela skaitļa daļa. Decimāldaļa tiek noņemta, un rezultāts netiek noapaļots. Piemēram, rezultāts 12,70 tiek parādīts kā 12.

## <a name="when-do-calculations-occur"></a>Kad aprēķini tiek veikti?
Aprēķini tiek veikti, kad visiem ievades atribūtiem ir norādīta vērtība.

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a>Vai varu pārrakstīt mērķa atribūtam aprēķināto vērtību?
Jūs varat pārrakstīt mērķa atribūtam aprēķināto vērtību, izņemot gadījumus, kad mērķa atribūts ir iestatīts kā slēpts vai tikai lasāms.

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-read-only"></a>Kā mērķa atribūtu var iestatīt kā slēptu vai tikai lasāmu?
Lai atribūtu iestatītu kā slēptu vai tikai lasāmu, izpildiet tālāk aprakstītās darbības.

1.  Noklikšķiniet uz **Preču informācijas pārvaldība** &gt; **Vispārīgi** &gt; **Preču konfigurācijas modeļi**.
2.  Atlasiet preces konfigurācijas modeli un pēc tam darbību rūtī noklikšķiniet uz **Rediģēt**.
3.  Lapā **Detalizēta informācija par ierobežojumam atbilstošu preces konfigurācijas modeli** atlasiet atribūtu, kas tiks izmantots kā mērķa atribūts.
4.  Kopsavilkuma cilnē **Atribūti** atlasiet **Slēpts** vai **Tikai lasāms**.

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a>Vai aprēķins var pārrakstīt iestatītās vērtības?
Nē. Tiek izmantotas tās vērtības, ko iestatāt preces konfigurēšanas laikā. Aprēķins, kas notiek, kad ir mainītas aprēķina ievades vērtības, nevar pārrakstīt vērtības, kuras jūs norādījāt attiecīgajam atribūtam.

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a>Kas notiek, ja aprēķinam noņemu ievades vērtību?
Ja aprēķinam noņemat ievades vērtību, tiek noņemta arī mērķa atribūta vērtība.

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a>Kāpēc tiek parādīts kļūdas ziņojums, ka manam modelim ir pretrunas?
Šis ziņojums tiek parādīts, ja aprēķins ietver kļūdu vai ja vienam vai vairākiem ierobežojumiem pastāv pretruna. Plašāku informāciju par pretrunām ierobežojumos skatiet rakstā [Izteiksmes ierobežojumi un tabulas ierobežojumi preču konfigurācijas modeļos](expression-constraints-table-constraints-product-configuration-models.md). Šeit ir norādītas dažas situācijas, kad var rasties kļūdas aprēķinos:

-   Vērtība tiek dalīta ar 0 (nulli).
-   Pastāv neatbilstība starp šādiem diviem elementiem:
    -   Vērtības, kas atribūtam ir pieejamas, un vērtības, ko ierobežo ierobežojums.
    -   Vērtība, kas tiek izveidota ar aprēķinu.
-   Aprēķina atgrieztās vērtības neatbilst atribūta sfērai. Piemēram, vesels skaitlis \[1..10\], kas tiek aprēķināts kā 0.

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a>Kāpēc tiek parādīts kļūdas ziņojums, lai gan esmu veiksmīgi validējis savu preču modeli?
Aprēķini nav iekļauti validācijā. Ir jāpārbauda preču konfigurācijas modelis, lai atrastu aprēķinu kļūdas. Nākamajās darbībās ir paskaidrots, kā pārbaudīt preču konfigurācijas modeli.

1.  Noklikšķiniet uz **Preču informācijas pārvaldība** &gt; **Vispārīgi** &gt; **Preču konfigurācijas modeļi**.
2.  Atlasiet preces konfigurācijas modeli un pēc tam darbību rūtī grupā **Izpildīt** noklikšķiniet uz **Pārbaudīt**.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]