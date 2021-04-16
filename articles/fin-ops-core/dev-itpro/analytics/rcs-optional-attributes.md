---
title: Failu importēšana XML formātā ar neobligātiem atribūtiem
description: Šajā tēmā ir sniegta informācija par tādu ER formātu veidošanu, kuri nosaka XML atribūtus ienākošo elektronisko dokumentu parsēšanai XML formātā.
author: NickSelin
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd5add18f2f1588cef02afae052d29dc1a28face
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748273"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a>Failu importēšana XML formātā ar neobligātiem atribūtiem

[!include [banner](../includes/banner.md)]

Varat veidot elektronisko pārskatu (Electronic Reporting — ER) formātus ienākošo dokumentu parsēšanai XML formātā. Izveidotajā ER formātā noteiktus XML elementu atribūtus var norādīts kā neobligātus. Tādējādi jūs varat pareizi apstrādāt ienākošos failus gan ar šādiem XML atribūtiem, gan bez tiem. Pēc tam saturu no šiem failiem varat izmantot, lai atjauninātu programmas datus.

Lai par šo līdzekli uzzinātu vairāk, izpildiet darbības, kas ir aprakstītas tēmā [(RCS) Failu importēšana XML formātā ar neobligātiem atribūtiem](tasks/import-files-xml-format-optional-attributes.md), kura veido daļu no biznesa procesa 7.5.4.3 IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677). Šo uzdevuma ceļvedi un saistītos parauga failus varat lejupielādēt no [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=874684).


| Satura apraksts       | Fails                                                         |
|---------------------------|--------------------------------------------------------------|
| Parauga fails XML formātā | IncomingDocumentToLearnHowToHandleOptionalAttributes.xml     |
| Uzdevuma ceļvedis                | RCS failu importēšana XML formātā ar neobligātiem atribūtiem.axtr |


Nākamajās darbībās ir paskaidrots, kā lietotājs ar lomu “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs” var izveidot ER formāta konfigurāciju, lai importētu XML formātā tādus failus, kuros ir neobligāti atribūti. Lai izpildītu tālāk norādītās darbības, vispirms izpildiet darbības procedūrā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md). Pirms sākšanas lejupielādējiet un lokāli saglabājiet failu IncomingDocumentToLearnHowToHandleOptionalAttributes.xml no Microsoft lejupielādes centra (https://go.microsoft.com/fwlink/?linkid=874684 ).

1. Dodieties uz **Organizācijas administrēšana** > **Darbvietas** > **Elektronisko pārskatu veidošana**.
2. Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**. Ja neredzat šo konfigurācijas nodrošinātāju, izpildiet darbības tēmā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**.

## <a name="create-a-new-data-model-configuration"></a>Jaunas datu modeļa konfigurācijas izveide
1. Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā **Nosaukums** ierakstiet “Modelis XML faila importēšanai”.
3. Klikšķiniet **Izveidot konfigurāciju**.
4. Noklikšķiniet uz **Veidotājs**.
5. Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.
6. Laukā **Nosaukums** ierakstiet “Sakne”.
7. Noklikšķiniet uz **Pievienot**.
8. Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.
9. Laukā **Nosaukums** ierakstiet “Saraksts”.
10.    Laukā **Vienuma veids** atlasiet **Ierakstu saraksts**.
11.    Noklikšķiniet uz **Pievienot**.
12.    Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.
13.    Laukā **Nosaukums** ierakstiet “Kods”.
14.    Laukā **Vienuma veids** atlasiet **Virkne**.
15.    Noklikšķiniet uz **Pievienot**.
16.    Noklikšķiniet uz **Saglabāt**.
17.    Aizvērt lapu.
18.    Noklikšķiniet uz **Mainīt statusu**.
19.    Noklikšķiniet uz **Pabeigt**.
20.    Noklikšķiniet uz **Labi**.

## <a name="create-a-format-for-data-import"></a>Formāta izveidošana datu importēšanai
1. Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.
2. Laukā **Jauns** ierakstiet “Formāts balstīts uz datu modeli Modelis XML faila importēšanai”.
3. Laukā **Nosaukums** ierakstiet “Formāts XML faila importēšanai”. 
4. Laukā **Atbalsta datu importēšanu** atlasiet **Jā**.
5. Klikšķiniet **Izveidot konfigurāciju**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Formāta veidošana ienākoša faila parsēšanai XML formātā
1. Noklikšķiniet uz **Veidotājs**.
2. Noklikšķiniet uz **Pievienot sakni**, lai atvērtu nolaižamo dialoglodziņu.
3. Kokā atlasiet **XML\Elements**.
4. Laukā **Nosaukums** ierakstiet “root”.
5. Noklikšķiniet uz **Labi**.
6. Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.
7. Kokā atlasiet **XML\Elements**.
8. Laukā **Nosaukums** ierakstiet “document”.
9. Laukā **Daudzkārtīgums** atlasiet **One many**.
10.    Noklikšķiniet uz **Labi**.
11.    Koka struktūrā atlasiet **root\document**.
12.    Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.
13.    Kokā atlasiet **XML\Atribūts**.
14.    Laukā **Nosaukums** ierakstiet “id”.
15.    Noklikšķiniet uz **Labi**.
16.    Noklikšķiniet uz **Saglabāt**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Formāta kartējuma veidošana parsētās informācijas saglabāšanai datu modelī
1.    Noklikšķiniet uz **Kartēt formātu uz modeli**.
2.    Noklikšķiniet uz **Jauns**.
3.    Laukā **Definīcija** ievadiet vai atlasiet kādu vērtību.
4.    Laukā **Nosaukums** ierakstiet “Kartēšana”.
5.    Noklikšķiniet uz **Saglabāt**.
6.    Noklikšķiniet uz **Noformētājs**.
7.    Koka struktūrā izvērsiet zaru **format**.
8.    Koka struktūrā izvērsiet zaru **format\root: XML Element(root)**.
9.    Koka struktūrā atlasiet **format\root: XML Element(root)\document: XML Element 1..* (dokuments)**.
10.    Noklikšķiniet uz **Saistīt**.
11.    Koka struktūrā izvērsiet zaru **format\root: XML Element(root)\document: XML Element 1..* (dokuments)**.
12.    Koka struktūrā atlasiet **format\root: XML Element(root)\document: XML Element 1..* (dokuments)\id**.
13.    Koka struktūrā izvērsiet zaru **List = format.root.document**.
14.    Koka struktūrā atlasiet zaru **List = format.root.document\Code**.
15.    Noklikšķiniet uz **Saistīt**.
16.    Noklikšķiniet uz **Saglabāt**.
17.    Aizveriet lapu.

## <a name="run-format-mapping"></a>Formāta kartēšanas darbināšana
1. Noklikšķiniet uz **Palaist**.
2. Noklikšķiniet uz **Pārlūkot** un atlasiet failu **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
3. Noklikšķiniet uz **Labi**.

> [!NOTE]
> Atlasītais fails nav importēts, jo formāta dizainā tiek pieņemts, ka elementam “document” ir atribūts “id”, bet importētajā failā tāda atribūta nav.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Formāta struktūras modificēšana, lai XML atribūtu apstrādātu kā neobligātu
1. Aizvērt lapu.
2. Koka struktūrā izvērsiet zaru **root\document**.
3. Koka struktūrā atlasiet zaru **root\document\id**.
4. Laukā **Tukša virkne trūkstošam atribūtam** atlasiet **Jā**.
5. Noklikšķiniet uz **Saglabāt**.

## <a name="run-format-mapping-to-test-changes"></a>Formāta kartējuma palaišana, lai testētu izmaiņas
1. Noklikšķiniet uz **Kartēt formātu uz modeli**.
2. Noklikšķiniet uz **Palaist**.
3. Noklikšķiniet uz **Pārlūkot** un atlasiet failu **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
4. Noklikšķiniet uz **Labi**.
5. Pārskatiet ģenerēto failu. Ievērojiet, ka tas pats fails ir importēts, jo formāta dizainā tiek pieņemts, ka elementam “document” atribūts “id” ir neobligāts.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]