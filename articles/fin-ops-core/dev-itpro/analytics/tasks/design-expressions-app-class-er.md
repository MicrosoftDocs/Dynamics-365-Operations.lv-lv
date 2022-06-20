---
title: ER izteiksmju noformēšana programmas klases metožu izsaukšanai
description: Šajā rakstā ir aprakstīts, kā atkārtoti izmantot esošo programmas loģiku elektronisko pārskatu konfigurācijās, izsaucot nepieciešamās programmas klašu metodes.
author: NickSelin
ms.date: 11/02/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0fb0a9725d882fdc330d7adbb49bd3dcadf7805f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883630"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>ER izteiksmju noformēšana programmas klases metožu izsaukšanai

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā atkārtoti izmantot esošo programmas [loģiku Elektronisko pārskatu (ER)](../general-electronic-reporting.md) konfigurācijās, izsaucot nepieciešamās programmas klašu metodes ER izteiksmēs. Klašu izsaukšanas argumentu vērtības var dinamiski definēt izpildlaikā. Piemēram, vērtības var būt balstītas uz informāciju parsēšanas dokumentā, lai nodrošinātu tās pareizību.

Piemēram, šajā rakstā jums tiks veidots process, kas parsē ienākošos bankas izrakstus pieteikuma datu atjaunināšanai. Ienākošos bankas izrakstus saņemsit kā teksta (.txt) failus, kuros ir starptautiskais bankas konta numura (IBAN) kods. Kā daļu no bankas izrakstu importēšanas procesa, jums ir jāapstiprina IBAN koda pareizību, izmantojot jau pieejamo loģiku.

## <a name="prerequisites"></a>Priekšnosacījumi

Procedūras šajā rakstā ir paredzētas lietotājiem, kuriem ir piešķirta sistēmas **administratora vai elektronisko pārskatu** izstrādātāja **loma**.

Procedūras var veikt, izmantojot jebkādu datu kopu.

Lai tos pabeigtu, lejupielādējiet un saglabājiet šādu failu: [SampleIncomingMessage.txt](https://download.microsoft.com/download/8/0/a/80adbc89-f23c-46d9-9241-e0f19125c04b/SampleIncomingMessage.txt).

Šajā rakstā izveidojat nepieciešamās ER konfigurācijas uzņēmumam Litware, Inc. sample. Tādēļ pirms šajā rakstā procedūru veikšanas ir jāveic šie soļi.

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapā Lokalizācijas **konfigurācijas pārbaudiet,** vai Litware, Inc.**parauga uzņēmuma konfigurācijas nodrošinātājs ir pieejams un atzīmēts** kā aktīvs. Ja šī konfigurācijas nodrošinātāja nav redzams, vispirms ir jāveic darbības, kas jāveic, izveidojot [konfigurācijas nodrošinātājus, un jāatzīmē tie kā aktīvi](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-a-new-er-model-configuration"></a>Importēt jaunu ER modeļa konfigurāciju

1. **Lapā Lokalizācijas konfigurācijas** sadaļā Konfigurācijas nodrošinātāji **atlasiet** Microsoft konfigurācijas nodrošinātāja **elementu**.
2. Atlasiet **Repozitoriji**.
3. Lapā Lokalizācijas **repozitoriju iestatījumi** atlasiet Rādīt **filtrus**.
4. Lai atlasītu globālo repozitorija ierakstu, pievienojiet **nosaukuma** filtra lauku.
5. Laukā **Nosaukums ievadiet Globāls** **·**. Pēc tam atlasiet ietver **filtra** operatoru.
6. Atlasiet **Lietot**.
7. Atlasiet **[Atvērt,](../er-download-configurations-global-repo.md#open-configurations-repository)** lai atlasītajā repozitorijā pārskatītu ER konfigurāciju sarakstu.
8. Konfigurācijas repozitorija **lapas** konfigurācijas kokā atlasiet Maksājumu **modelis**.
9. Ja kopsavilkuma **cilnē** Versijas ir pieejama poga **Importēt**, atlasiet to un pēc tam atlasiet **Jā**.

    Ja poga **Importēt** nav pieejama, jūs jau esat importējis atlasīto maksājumu modeļa **ER** konfigurācijas versiju.

10. Aizveriet konfigurācijas **repozitorija** lapu un pēc tam **aizveriet lapu Lokalizācijas atkārtotas darbības**.

## <a name="add-a-new-er-format-configuration"></a>Jaunas ER formāta konfigurācijas pievienošana

Pievienojiet jaunu ER formātu, lai parsētu ienākošos bankas izrakstus TXT formātā.

1. **Lapā Lokalizācijas konfigurācijas** atlasiet elementu **Pārskatu** konfigurācijas.
2. **Konfigurācijas lapas** konfigurācijas kokā kreisajā rūtī atlasiet Maksājumu **modelis**.
3. Atlasiet **Izveidot konfigurāciju**. 
4. Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības.

    1. Laukā **Jauns** ievadiet **Format based on data model PaymentModel**.
    2. Laukā **Nosaukums** ievadiet bankas **izraksta importa formātu (paraugs)**.
    3. Laukā **Atbalsta datu importēšanu** atlasiet **Jā**.
    4. Atlasiet **Izveidot konfigurāciju,** lai pabeigtu konfigurācijas izveidi.

## <a name="design-the-er-format-configuration--format"></a>ER formāta konfigurācijas dizains — formāts

Veidot ER formātu, kas parāda ārējā faila paredzamo struktūru TXT formātā.

1. Pievienotajā **bankas izraksta importa formāta (parauga)** formāta konfigurācijā atlasiet **veidotāju**.
2. **Formāta veidotāja** lapas formāta struktūras kokā kreisajā rūtī atlasiet Pievienot **sakni**.
3. Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības:

    1. Koka struktūrā atlasiet teksta secību **\\, lai** pievienotu secības **formāta** komponentu.
    2. Laukā **Nosaukums ievadiet** Sakne **·**.
    3. Laukā **Īpašās rakstzīmes** atlasiet **Jauna rinda - Windows (CR LF)**. Pamatojoties uz šo iestatījumu, katra parsēšanas faila rinda tiks uzskatīta par atsevišķu ierakstu.
    4. Atlasiet **Labi**.

4. Atlasiet **Pievienot**.
5. Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības:

    1. Koka struktūrā atlasiet teksta **\\ secību**.
    2. Laukā **Nosaukums** ievadiet **Rindas**.
    3. Laukā **Daudzkārtīgums** atlasiet **One many**. Pamatojoties uz šo iestatījumu, vismaz viena rinda tiks gaidīta parsēšanas failā.
    4. Atlasiet **Labi**.

6. Koka struktūrā atlasiet saknes **rindas\\ un** pēc tam atlasiet Pievienot **secību**.
7. Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības:

    1. Laukā **Nosaukums** ievadiet **Lauki**.
    2. Laukā **Daudzkāršana** atlasiet **Tieši vienu**.
    3. Atlasiet **Labi**.

8. Kokā atlasiet Saknes **rindu\\ lauki\\** un pēc tam atlasiet **Pievienot**.
9. Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības:

    1. Koka struktūrā atlasiet teksta **\\ virkni**.
    2. Laukā **Nosaukums ievadiet** IBAN **·**.
    3. Atlasiet **Labi**.

10. Atlasiet **Saglabāt**.

Konfigurācija tagad ir iestatīta tā, lai katra rinda parsēšanas failā satur tikai IBAN kodu.

![Bankas izraksta importa formāta (parauga) formāta konfigurācija formāta veidotāja lapā.](../media/design-expressions-app-class-er-01.png)

## <a name="design-the-er-format-configuration--mapping-to-a-data-model"></a>ER formāta konfigurācijas dizains — kartēšana uz datu modeli

Izstrādā ER formāta kartēšanu, kas izmanto informāciju no parsēšanas faila, lai aizpildītu datu modeli.

1. **Formāta veidotāja** lapā Darbību rūtī atlasiet Kartēt **formātu uz modeli**.
2. **Lapas Modelis datu avota kartēšanai** darbību rūtī atlasiet **Jauns**.
3. Laukā **Definīcija** atlasiet **BankToCustomerDebitCreditNotificationInitiation**.
4. Laukā **Nosaukums** ievadiet Kartēšana **uz datu modeli**.
5. Atlasiet **Saglabāt**.
6. Atlasiet **Noformētājs**.
7. Modeļu kartēšanas **veidotāja** lapā datu avota **tipu kokā** atlasiet **Dynamics 365 for Operations\\ Klase**.
8. Sadaļā Datu **avoti atlasiet** Pievienot **sakni**, lai pievienotu datu avotu, kas izsauc esošo programmas loģiku IBAN kodu validēšanai.
9. Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības:

    1. Laukā **Nosaukums ievadiet Čeku** kodus **\_**.
    2. Laukā **Klase** ievadiet vai atlasiet **ISO7064**.
    3. Atlasiet **Labi**.

10. **Datu avota tipu kokā** rīkojieties šādi:

    1. Izvērsiet formāta **datu** avotu.
    2. Izvērst **formāta\\ sakni: Sequence(Root)**.
    3. Izvērst **formāta\\ sakni: Secība(saknes)\\ Rindas: 1. secība\* (rindas)**.
    4. Izvērst **formāta\\ sakni: Secība(saknes)\\ Rindas: 1.\* secība (rindas)\\ Lauki: 1..1. secība (lauki)**.

11. **Datu modeļa kokā** rīkojieties šādi:

    1. Izvērsiet datu **modeļa** lauku Maksājumi.
    2. Izvērsiet **maksājumu\\ kreditora kontu (CreditorAccount)**.
    3. Izvērsiet **maksājumu\\ kreditora konta (CreditorAccount)\\ identifikāciju**.
    4. Izvērsiet **maksājumu\\ kreditora konta (CreditorAccount)\\ identifikācijas\\ IBAN**.

12. Sekojiet šiem soļiem, lai saistītu konfigurētā formāta komponentus datu modeļa laukos:

    1. Izvēlieties **formāta\\ sakni: Sequence(Root)\\ Rindas: 1. secība\* (rindas)**.
    2. Atlasiet **maksājumus**.
    3. Atlasiet **Saistīt**. Pamatojoties uz šo iestatījumu, katra parsēšanas faila rinda tiks uzskatīta par vienu maksājumu.
    4. Atlasiet **formāta sakni\\: Secība(saknes)\\ Rindas: 1. secība..\* (rindas)\\ Lauki: 1..1. secība (lauki)\\ IBAN: String(IBAN)**.
    5. Atlasiet **maksājumu\\ saņēmēja konta (CreditorAccount)\\ identifikācijas\\ IBAN**.
    6. Atlasiet **Saistīt**. Pamatojoties uz šo iestatījumu, **datu modeļa IBAN** lauks tiks aizpildīts ar vērtību no parsēšanas faila.

    ![Formāta komponentu saistīšana ar datu modeļa laukiem modeļu kartēšanas veidotāja lapā.](../media/design-expressions-app-class-er-02.png)

13. Cilnē Pārbaudes **izpildiet šos soļus, lai pievienotu apstiprināšanas noteikumu, kas parāda kļūdas ziņojumu jebkurai rindai parsēšanas** failā, [kas](../general-electronic-reporting-formula-designer.md#Validation) satur nederīgu IBAN kodu:

    1. Atlasiet **Jauns** un tad atlasiet Rediģēt **nosacījumu**.
    2. Formulas **veidotāja** lapā datu **avota** kokā izvērsiet pārbaudes kodu datu avotu, kas pārstāv ISO7064 **programmas klasi,\_** **lai** skatītu šīs klases pieejamās metodes.
    3. Atlasiet **čeku\_ kodus\\ verifyMOD1271\_ 36**.
    4. Atlasiet **Pievienot datu avotu**.
    5. Formulas **laukā** ievadiet šādu [izteiksmi](../general-electronic-reporting-formula-designer.md#Binding): **Pārbaudīt\_ kodus.verifyMOD1271\_ 36(formāts. Root.Rows.Fields.IBAN)**.
    6. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.
    7. Atlasiet **Labot ziņojumu**.
    8. Formulas **veidotāja** lapas laukā **Formula** **ievadiet CONCATENATE("Atrasts nederīgs IBAN kods:&nbsp;", formāts. Root.Rows.Fields.IBAN)**.
    9. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

    Pamatojoties uz šiem iestatījumiem, pārbaudes nosacījums atgriezīs FALSE par jebkuru nederīgu IBAN *[kodu,](../er-formula-supported-data-types-primitive.md#boolean)* izsaucot esošo ISO7064 **programmas klases metodi VerifyMOD1271\_ 36** **.** Ievērojiet, ka IBAN koda vērtība izpildlaikā ir dinamiski definēta kā izsaukšanas metodes arguments, balstoties uz parsēšanas teksta faila saturu.

    ![Pārbaudes noteikums Modeļu kartēšanas veidotāja lapā.](../media/design-expressions-app-class-er-03.png)

14. Atlasiet **Saglabāt**.
15. Aizveriet modeļu kartēšanas **veidotāja** lapu un pēc tam aizveriet lapu **Modelis ar datu avota kartēšanu**.

## <a name="run-the-format-mapping"></a>Formāta kartēšanas palaišana

Testēšanas nolūkos palaidiet formāta kartēšanu, izmantojot iepriekš lejupielādēto SampleIncomingMessage.txt failu. Ģenerētais rezultāts ietvers datus, kas tiek importēti no atlasītā teksta faila un ieejot pielāgotajā datu modelī reālā importa laikā.

1. Lapā Modelis **datu avota kartēšanai** atlasiet **Palaist**.
2. Lapā Elektroniskā **pārskata parametri atlasiet** Pārlūkot, **·** **pārlūkojiet SampleIncomingMessage.txt** failu, kuru lejupielādējāt, un atlasiet to.
3. Atlasiet **Labi**.
4. Ņemiet vērā **, ka modelis datu avota kartēšanas** lapā parāda kļūdas ziņojumu par nederīgu IBAN kodu.

    ![Formāta kartēšanas rezultāts lapā Modelis un Datu avota kartēšana.](../media/design-expressions-app-class-er-04.png)

5. Pārskatiet izvadi XML formātā, kas parāda no atlasītā faila importētos un uz datu modeli pārnestos datus. Ņemiet vērā, ka tikai trīs importētā teksta faila rindas tika apstrādātas bez kļūdām. IBAN kods tiešsaistē 4 nav derīgs un tika izlaists.

    ![XML izvade.](../media/design-expressions-app-class-er-05.png)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
