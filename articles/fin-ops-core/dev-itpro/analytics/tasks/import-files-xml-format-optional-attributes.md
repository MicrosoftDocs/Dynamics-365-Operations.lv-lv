---
title: (RCS) Failu importēšana XML formātā ar neobligātiem atribūtiem
description: Šajā tēmā ir sniegta informācija par to, kā lietotājs var izveidot ER formāta konfigurāciju, lai importētu failus XML formātā ar neobligātiem atribūtiem.
author: NickSelin
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b9447c827a02acb616bbfdcb2c7305e8bdd013c9811e28bb25256db056d85d6a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720716"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a>(RCS) Failu importēšana XML formātā ar neobligātiem atribūtiem

[!include [banner](../../includes/banner.md)]

Nākamajās darbībās ir paskaidrots, kā lietotājs ar lomu “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs” var izveidot ER formāta konfigurāciju, lai importētu XML formātā tādus failus, kuros ir neobligāti atribūti. Lai izpildītu tālāk norādītās darbības, vispirms izpildiet darbības, kas aprakstītas procedūrā "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu". Pirms sākšanas lejupielādējiet un lokāli saglabājiet failu IncomingDocumentToLearnHowToHandleOptionalAttributes.xml no [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=874684).

1.    Dodieties uz **Visas darbvietas** > **Elektroniskie pārskati**.
2.    Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam Litware, Inc. ir pieejams un ir atzīmēts kā **Aktīvs**. Ja neredzat šo konfigurācijas nodrošinātāju, izpildiet darbības, kas ir aprakstītas procedūrā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](er-configuration-provider-mark-it-active-2016-11.md).
3.    Noklikšķiniet uz **Pārskatu veidošanas konfigurācijas**.

## <a name="create-a-new-data-model-configuration"></a>Jaunas datu modeļa konfigurācijas izveide
1.    Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.
2.    Laukā **Nosaukums** ierakstiet “Modelis XML faila importēšanai”.
3.    Klikšķiniet **Izveidot konfigurāciju**.
4.    Noklikšķiniet uz **Veidotājs**.
5.    Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.
6.    Laukā **Nosaukums** ierakstiet “Sakne”.
7.    Noklikšķiniet uz **Pievienot**.
8.    Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.
9.    Laukā **Nosaukums** ierakstiet “Saraksts”.
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
1.    Noklikšķiniet uz **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu.
2.    Laukā **Jauns** ierakstiet “Formāts balstīts uz datu modeli Modelis XML faila importēšanai”.
3.    Laukā **Nosaukums** ierakstiet “Formāts XML faila importēšanai”.
4.    Laukā **Atbalsta datu importēšanu** atlasiet **Jā**.
5.    Klikšķiniet **Izveidot konfigurāciju**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Formāta veidošana ienākoša faila parsēšanai XML formātā
1.    Noklikšķiniet uz **Veidotājs**.
2.    Noklikšķiniet uz **Pievienot sakni**, lai atvērtu nolaižamo dialoglodziņu.
3.    Kokā atlasiet **XML\Elements**.
4.    Laukā **Nosaukums** ierakstiet “root”.
5.    Noklikšķiniet uz **Labi**.
6.    Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.
7.    Kokā atlasiet **XML\Elements**.
8.    Laukā **Nosaukums** ierakstiet “document”.
9.    Laukā **Daudzkārtīgums** atlasiet **One many**.
10.    Noklikšķiniet uz **Labi**.
11.    Koka struktūrā atlasiet **root\document**.
12.    Noklikšķiniet uz **Pievienot**, lai atvērtu nolaižamo dialoglodziņu.
13.    Kokā atlasiet **XML\Atribūts**.
14.    Laukā **Nosaukums** ierakstiet “ID”.
15.    Noklikšķiniet uz **Labi**.
16.    Noklikšķiniet uz **Saglabāt**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Formāta kartējuma veidošana parsētās informācijas saglabāšanai datu modelī
1. Noklikšķiniet uz **Kartēt formātu uz modeli**.
2. Klikšķiniet **Jauns**.
3. Laukā **Definīcija** ievadiet vai atlasiet kādu vērtību.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Laukā **Nosaukums** ierakstiet “Kartēšana”.
6. Noklikšķiniet uz **Saglabāt**.
7. Noklikšķiniet uz **Noformētājs**.
8. Koka struktūrā izvērsiet zaru **format**.
9. Koka struktūrā izvērsiet zaru **format\root: XML Element(root)**.
10.    Koka struktūrā atlasiet **format\root: XML Element(root)\document: XML Element 1..* (dokuments)**.
11.    Noklikšķiniet uz **Saistīt**.
12.    Koka struktūrā izvērsiet zaru **format\root: XML Element(root)\document: XML Element 1..* (dokuments)**.
13.    Koka struktūrā atlasiet **format\root: XML Element(root)\document: XML Element 1..* (dokuments)\id**.
14.    Koka struktūrā izvērsiet zaru **List = format.root.document**.
15.    Koka struktūrā atlasiet zaru **List = format.root.document\Code**.
16.    Noklikšķiniet uz **Saistīt**.
17.    Noklikšķiniet uz **Saglabāt**.
18.    Aizvērt lapu.
 
## <a name="run-format-mapping"></a>Formāta kartēšanas darbināšana
1. Noklikšķiniet uz **Palaist**.
2. Noklikšķiniet uz **Pārlūkot** un atlasiet **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
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
5. Pārskatiet ģenerēto failu. 

> [!NOTE]
> Tiek importēts tas pats fails, jo formāta dizainā tiek pieņemts, ka elementam 'document' atribūts 'id' ir neobligāts.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]