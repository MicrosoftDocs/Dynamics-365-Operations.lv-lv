---
title: ER konfigurāciju noformēšana ienākošo dokumentu parsēšanai
description: Šajā procedūrā ir parādīts, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai parsētu ienākošu elektronisku dokumentu.
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83fbcd2cedab02643f8a2b22a098343ff065047d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884175"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>ER konfigurāciju noformēšana ienākošo dokumentu parsēšanai

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai parsētu ienākošu elektronisku dokumentu. Šajā procedūrā jūs importēsiet nepieciešamās ER konfigurācijās, kuras ir izveidotas parauga uzņēmumam “Litware, Inc.”, un pēc tam, izmantojot tās, parsēsiet ienākošos elektroniskos dokumentus. Lai izpildītu šīs procedūras darbības, vispirms izpildiet procedūru "ER Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu".

Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.

Šīs darbības var veikt, izmantojot jebkuru datu kopu. Pirms sākat, lejupielādējiet un saglabājiet raksta uzskaitītos failus sadaļā "Parsēt ienākošos dokumentus, lai atjauninātu programmas datus" (Parsēt [ienākošos dokumentus](../parse-incoming-electronic-documents.md)). Minētie faili ir: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
    * Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un ir atzīmēts kā aktīvs. Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.
2. Atlasiet Pārskatu konfigurācijas.
    * Lai demonstrētu ienākošo elektronisko dokumentu parsēšanas XML formātā iespējas, tiks izmantots šāds scenārijs: ERP pieteikums pieprasa datus no tīmekļa pakalpojuma (piemēram, [efsta](http://efsta.org/) finanšu pakalpojum) un parsē ienākošās atbildes, lai attiecīgi atjauninātu pieteikuma datus. Visefektīvākajai parsēšanai tiek izmantots viens ER formāts, neraugoties uz paredzamo ienākošo dokumentu XML formātā atšķirīgo struktūru.

## <a name="import-and-review-er-configurations"></a>ER konfigurāciju importēšana un pārskatīšana

Importējiet ER modeļa konfigurāciju, kura satur parauga datu modeli, kas paredzēts ienākošā faila informācijas glabāšanai.

1. Atlasiet Maiņa.
2. Atlasiet Ielādēt no XML faila.
    * Atlasiet Pārlūkot un atlasiet EFSTA failu model.xml.
3. Atlasiet Labi.
4. Kokā atlasiet “EFSTA modelis”.
5. Atlasiet Noformētājs.
    * Pārskatiet importētā datu modeļa struktūru. enumType uzskaitījums ir definēts, lai atpazītu tālāk norādītos pakalpojumu atbilžu veidus: iegūt apstiprinājumu par transakcijas iesniegšanu, iegūt informāciju par pēdējo iesniegto transakciju un atpazīt neatbalstītus atbilžu veidus.
6. Kokā izvērsiet “Atbilde”.
    * Saknes krājums 'Atbilde' ir definēts, lai norādītu, kāda veida dati jāņem no atbalstīto pakalpojumu atbildēm, lai attiecīgi atjauninātu pieteikuma datus.
7. Aizvērt lapu.
    * Jūs importēsit ER formāta konfigurāciju, kas norāda, kā ienākošie dokumenti tiks parsēti datu uzglabāšanai ER datu modelī.
8. Atlasiet Maiņa.
9. Atlasiet Ielādēt no XML faila.
    * Atlasiet Pārlūkot un atlasiet EFSTA failu format.xml.
10. Atlasiet Labi.
11. Kokā izvērsiet “EFSTA modelis”.
12. Kokā atlasiet “EFSTA model\EFSTA format”.
13. Atlasiet Noformētājs.
14. Atlasiet Izvērst/sakļaut.
    * Formāta elements CASE tiek izmantots kā saknes elements un satur trīs ligzdotos elementus FILE, kas nozīmē to, ka šis formāts ir paredzēts, lai parsētu vairāku formātu ienākošos failus.
15. Kokā atlasiet “Atbildes\Transakcijas izpilde\TraC”.
    * Atbilde par iesniegto transakciju sākas ar saknes elementu 'TraC'.
16. Kokā atlasiet “Atbildes\Pēdējais transakcijas pieprasījums\Tra”.
    * Atbilde par pēdējo iesniegto transakciju sākas ar saknes elementu 'Era'.
17. Kokā atlasiet “Atbildes\Neparedzēta atbilde\Teksts”.
    * Trešais elements FILE ar ligzdoto elementu TEXT ir pievienots, lai atpazītu citus atbilžu tipus, kuri atšķiras no iepriekš minētajiem.
18. Atlasiet Kartēt formātu uz modeli.
    * Šis modeļa kartējums satur datu plūsmas definīciju, lai saglabātu detalizētu informāciju par parsēto ienākošo dokumentu, izmantojot datu modeļa vienumus.
19. Atlasiet Noformētājs.
20. Kokā izvērsiet "format".
21. Kokā izvērsiet “formāts\Atbildes: Gadījums(Atbildes)”.
    * Pārskatiet datu avota 'formāts' struktūru. Visi trīs atbilžu veidi tiek piedāvāti atsevišķi.
22. Kokā atlasiet “formāts\Atbildes: Gadījums(Atbildes)\aType”.
    * Datu avota vienums 'aType' ir pievienots, lai norādītu atbildes tipu, un ir piesaistīts datu modeļa vienumam 'Veids'.
23. Atlasiet cilni Validācijas.
24. Kokā atlasiet “Tips = format.Responses.aType”.
    * ER pārbaude ir konfigurēta, lai informētu lietotāju par situāciju, kad atbildes struktūra neatbilst apstiprinājumam par transakcijas iesniegšanu vai informācijai par pēdējo iesniegto transakciju (neatbalstīts atbildes gadījums).
25. Aizvērt lapu.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Palaist ER formāta modeļa kartējumu, kas konfigurēts ienākošo failu parsēšanai

Jūs palaidīsit izveidoto modeļa kartējumu testēšanas nolūkos, lai redzētu, kā konfigurētais ER formāts parsēs ienākošās pakalpojumu atbildes. Šajā solī tiek izmantoti dažādi XML faili, lai simulētu dažāda tipa tīmekļa pakalpojumu atbildes.

1. Atveriet failu Response1.xml XML lasītājā, piemēram, tīmekļa pārlūkprogrammā. Šis fails satur apstiprinājuma informāciju par pabeigtu transakciju ('TraC' ir saknes elements).
2. Atlasiet Izpildīt.
    * Atlasiet Pārlūkot un atlasiet failu Response1.xml.
3. Atlasiet Labi.
    * Pārskatiet ģenerēto izvadi. Atbildes veids ir pareizi atpazīts un parsēts (`ERModelEnumDataSourceHandler#EFSTA model#enumType#C` nozīmē transakcijas pabeigšanas gadījumu).
    * Atveriet failu Response2.xml XML lasītājā. Šis fails satur informāciju par pēdējo iesniegto transakciju (`Tra` ir saknes elements).
4. Atlasiet Izpildīt.
    * Atlasiet Pārlūkot un atlasiet failu Response2.xml.
5. Atlasiet Labi.
    * Pārskatiet ģenerēto izvadi. Atbildes veids ir pareizi atpazīts un parsēts (`ERModelEnumDataSourceHandler#EFSTA model#enumType#R` nozīmē sistēmas restartēšanas gadījumu).
    * Atveriet failu Response3.xml XML lasītājā. Šis fails sākas ar TraZ saknes vienumu un ka šī struktūra nav konfigurēta, izmantojot ER formātu.
6. Atlasiet Izpildīt.
    * Atlasiet Pārlūkot un atlasiet failu Response3.xml.
7. Atlasiet Labi.
    * Pārskatiet ģenerēto izvadi. Atbildes veids ir pareizi atpazīts kā neatbalstīts (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Informācijas žurnālā ir reģistrēts atbilstošais ziņojums (saskaņā ar ER pārbaudes iestatījumu), un lielākā daļa datu modeļa nav aizpildīta.
    * Atveriet failu Response4.xml XML lasītājā. Šī faila struktūra ir gandrīz tāda pati kā veiksmīgi parsētam failam Response1.xml, izņemot saknes elementa 'TraC' ligzdotu elementu secību.
8. Atlasiet Izpildīt.
    * Atlasiet Pārlūkot un atlasiet failu Response4.xml.
9. Atlasiet Labi.
    * Pārskatiet ģenerēto izvadi. Atbildes veids ir pareizi atpazīts kā neatbalstīts (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Informācijas žurnālā ir reģistrēts atbilstošais ziņojums, un lielākā daļa datu modeļa nav aizpildīta. Šī uzvedība skaidrojama ar to, ka šī ER formāta pašreizējais iestatījums paredz noteiktu ienākošā faila saknes vienuma ligzdoto elementu secību.
10. Aizvērt lapu.
11. Kokā atlasiet “Atbildes\Transakcijas izpilde\TraC”.
12. Laukā Ligzdoto elementu parsēšanas kārtība atlasiet “Jebkura”.
    * Atlasiet iestatījumu Jebkura laukā 'Ligzdoto elementu parsēšanas kārtība', lai atļautu jebkuru ligzdoto elementu secību šim saknes XML vienumam.
13. Atlasiet Saglabāt.
14. Atlasiet Kartēt formātu uz modeli.
15. Atlasiet Izpildīt.
    * Atlasiet Pārlūkot un atlasiet failu Response4.xml.
16. Atlasiet Labi.
    * Pārskatiet ģenerēto izvadi. Tagad atbildes veids ir pareizi atpazīts kā līdzvērtīgs failam Response1.xml.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]