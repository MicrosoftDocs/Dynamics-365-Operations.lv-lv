---
title: Pielāgotu lauku ieviešana Microsoft Dynamics 365 Project Timesheet mobilajai programmai operētājsistēmā iOS un Android
description: Šajā tēmā ir aprakstīti parastās metodes paplašinājumu izmantošanai, lai ieviestu pielāgotus laukus.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 48854c15e429d51dcf30ea804eb636dee7965443
ms.sourcegitcommit: a356299be9a593990d9948b3a6b754bd058a5b3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/21/2020
ms.locfileid: "3080776"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Pielāgotu lauku ieviešana Microsoft Dynamics 365 Project Timesheet mobilajai programmai operētājsistēmā iOS un Android

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti parastās metodes paplašinājumu izmantošanai, lai ieviestu pielāgotus laukus. Ir aprakstītas tālāk norādītās tēmas.

- Dažādie datu tipi, ko atbalsta pielāgoto lauku struktūra
- Kā darba laika uzskaites tabulu ierakstos rādīt tikai lasāmus vai rediģējamus laukus un kā datu bāzē saglabāt lietotāja norādītas vērtības.
- Kā darba laika uzskaites tabulas virsrakstā rādīt tikai lasāmus laukus
- Kā integrēt citu pielāgoto biznesa loģiku, lai laukos ievadītu noklusējuma vērtības un veiktu papildu validēšanu

## <a name="audience"></a>Mērķauditorija

Šī tēma ir paredzēta izstrādātājiem, kas savus pielāgotos laukus integrē Microsoft Dynamics 365 Project Timesheet mobilajā programmā, kura ir pieejama operētājsistēmai Apple iOS un Google Android. Tiek pieņemts, ka lasītāji pārzina X++ izstrādes un projektu darba laika uzskaites tabulu funkcionalitāti.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Datu līgums – TSTimesheetCustomField X++ klase

**TSTimesheetCustomField** klase ir X++ datu līguma klase, kas pārstāv informāciju par pielāgotu lauku darba laika uzskaites tabulas funkcionalitātei. Pielāgoto lauku objektu saraksti tiek nodoti gan TSTimesheetDetails datu līgumam, gan TSTimesheetEntry datu līgumam, lai pielāgotus laukus rādītu mobilajā programmā.

- **TSTimesheetDetails** — darba laika uzskaites tabulas virsraksta līgums.
- **TSTimesheetEntry** — darba laika uzskaites tabulas transakcijas līgums. Šo objektu grupas, kam ir vienāda projekta informācija un vērtība **timesheetLineRecId**, veido vienu rindu.

### <a name="fieldbasetype-types"></a>fieldBaseType (tipi)

Rekvizīts **FieldBaseType** objektā **TsTimesheetCustom** nosaka programmā rādītā lauka tipu. Tiek atbalstītas tālāk norādītās vērtības **Tipi**.

| Vērtības Tipi | Tips              | Piezīmes |
|-------------|-------------------|-------|
| 0           | Virkne (un Uzskaitījums) | Šis lauks izskatās kā teksta lauks. |
| 1           | Vesels skaitlis           | Vērtība tiek rādīta kā skaitlis bez cipariem aiz komata. |
| 2           | Real              | Vērtība tiek rādīta kā skaitlis ar cipariem aiz komata.<p>Lai reālo skaitļu vērtības programmā radītu kā valūtu, izmantojiet rekvizītu **fieldExtenededType**. Varat arī izmantot rekvizītu **numberOfDecimals**, lai iestatītu, cik cipari aiz komata tiek rādīti.</p> |
| 3           | Datums              | Datuma formātus nosaka lietotāja iestatījums **Datumu, laiku un skaitļu formāts**, kas ir norādīts iestatījumā **Valodas un valsts/reģiona preferences**, sadaļā **Lietotāja opcijas**. |
| 4.           | Būla           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Ja objektā **TSTimesheetCustomField** nav norādīts rekvizīts **stringOptions**, lietotājam tiek nodrošināts brīva teksta lauks.

    Var izmantot rekvizītu **stringLength**, lai iestatītu maksimālo virknes garumu, kādu lietotāji var ievadīt.

- Ja objektā **TSTimesheetCustomField** ir norādīts rekvizīts **stringOptions**, šie saraksta elementi ir vienīgās vērtības, ko lietotāji var atlasīt, izmantojot opciju pogas (radiopogas).

    Tādā gadījumā virknes lauks lietotāja ievades nolūkos var darboties kā uzskaitījuma vērtība. Lai šo vērtību datu bāzē saglabātu kā uzskaitījumu, manuāli kartējiet virknes vērtību atpakaļ uz uzskaitījuma vērtību, pirms to saglabājat datu bāzē, izmantojot komandķēdi (piemēru skatiet tālāk šajā tēmā, sadaļā “Komandķēdes lietošana klasei TSTimesheetEntryService, lai darba laika uzskaites tabulas ierakstu no programmas saglabātu atpakaļ datu bāzē”).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Šo rekvizītu varat izmantot, lai reālu skaitļu vērtības formatētu kā valūtu. Šī pieeja ir piemērojama tikai tad, ja vienuma **fieldBaseType** vērtība ir **Real**.

- **TSCustomFieldExtendedType:None** — netiek lietots nekāds formatējums.
- **TSCustomFieldExtendedType::Valūta** — formatēt vērtību kā valūtu.

    Kad ir aktīvs valūtas formatējums, var izmantot lauku **stringValue**, lai nodotu valūtas kodu, kas ir jārāda programmā. Šī vērtība ir tikai lasāma vērtība.

    Laukā **realValue** ir naudas summa, kas ir jāsaglabā datu bāzē.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Šo rekvizītu varat izmantot, lai norādītu, kur šis pielāgotais lauks ir jārāda programmā.

- **TSCustomFieldSection::Virsraksts** — šis lauks programmā tiek rādīts sadaļā **Skatīt vairāk informācijas**. Šie lauki vienmēr ir tikai lasāmi.
- **TSCustomFieldSection::Rinda** — šis lauks tiek rādīts pēc visiem darba laika uzskaites tabulu ierakstu standarta komplektācijas rindu laukiem. Šie lauki var būt rediģējami vai tikai lasāmi.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Šis rekvizīts norāda lauku, kad programmas nodrošinātās vērtības tiek saglabātas atpakaļ datu bāzē.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Šis rekvizīts norāda lauku, kad programmas nodrošinātās vērtības tiek saglabātas atpakaļ datu bāzē.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Iestatiet šo rekvizītu uz **Jā**, lai norādītu, ka darba laika uzskaites tabulas ieraksta sadaļā esošo lauku lietotājiem ir jāvar rediģēt. Iestatiet šo rekvizītu uz **Nē**, lai lauku padarītu par tikai lasāmu.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Iestatiet šo rekvizītu uz **Jā**, lai norādītu, ka darba laika uzskaites tabulas ieraksta sadaļā esošajam laukam ir jābūt obligātam.

### <a name="label-str"></a>label (str)

Šis rekvizīts norāda etiķeti, kas programmā tiek rādīta blakus šim laukam.

### <a name="stringoptions-list-of-strings"></a>stringOptions (virkņu saraksts)

Šis rekvizīts ir piemērojams tikai tad, ja vienums **fieldBaseType** ir iestatīts uz **String**. Ja ir iestatīts vienums **stringOptions**, ar virknēm šajā sarakstā tiek norādītas virkņu vērtības, kas ir pieejamas atlasei, izmantojot opciju pogas (radiopogas). Ja nav norādīta neviena virkne, ir atļauta brīvā teksta ievadīšana virknes laukā (piemēru skatiet tālāk šajā tēmā, sadaļā “Komandķēdes lietošana klasei TSTimesheetEntryService, lai darba laika uzskaites tabulas ierakstu no programmas saglabātu atpakaļ datu bāzē”).

### <a name="stringlength-int"></a>stringLength (int)

Šis rekvizīts norāda virknes lauka maksimālo garumu. Tas ir piemērojams tikai tad, ja vienums **fieldBaseType** ir iestatīts uz **String**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Šis rekvizīts norāda ciparu skaitu aiz komata, kas tiek rādīti reāla skaitļa laukam. Tas ir piemērojams tikai tad, ja vienums **fieldBaseType** ir iestatīts uz **Real**.

### <a name="ordersequence-int"></a>orderSequence (int)

Šis rekvizīts kontrolē secību, kādā programmā tiek rādīti pielāgoti lauki, ja ir norādīti vairāki pielāgoti lauki. Vispirms tiek rādīti lauki, kuru skaitļi ir mazāki.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Laukiem, kuru tips ir **Būla**, šis rekvizīts nodod lauka Būla vērtību starp serveri un programmu.

### <a name="guidvalue-guid"></a>guidValue (guid)

Laukiem, kuru tips ir **GUID**, šis rekvizīts nodod lauka globāli unikālā identifikatora (GUID) vērtību starp serveri un programmu.

### <a name="int64value-int64"></a>int64Value (int64)

Laukiem, kuru tips ir **Int64**, šis rekvizīts nodod lauka int64 vērtību starp serveri un programmu.

### <a name="intvalue-int"></a>intValue (int)

Laukiem, kuru tips ir **Int**, šis rekvizīts nodod lauka int vērtību starp serveri un programmu.

### <a name="realvalue-real"></a>realValue (real)

Laukiem, kuru tips ir **Real**, šis rekvizīts nodod lauka reālā skaitļa vērtību starp serveri un programmu.

### <a name="stringvalue-str"></a>stringValue (str)

Laukiem, kuru tips ir **String**, šis rekvizīts nodod lauka virknes vērtību starp serveri un programmu. Tas tiek izmantots arī laukiem ar tipu **Real**, kuri ir formatēti kā valūta. Šiem laukiem šis rekvizīts tiek izmantots, lai valūtas kodu nodotu programmai.

### <a name="datevalue-date"></a>dateValue (date)

Laukiem, kuru tips ir **Datums**, šis rekvizīts nodod lauka datuma vērtību starp serveri un programmu.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Pielāgotu lauku rādīšana un saglabāšana darba laika uzskaites tabulas ieraksta sadaļā

Tālāk ir ekrānuzņēmums no laika uzskaites tabulas ieraksta izveides mobilās lietotnes. Tajā ir redzami standarta komplektācijā esošie lauki un pielāgots lauks sadaļā “Laika ievade” ar nosaukumu “Testa virkne”, kuram jau ir iestatīta uzskaitījuma vērtība “Otrā opcija”.

![Testa virknes pielāgotais lauks programmā](media/timesheet-entry.jpg)



Tālāk ir ekrānuzņēmums no mobilās lietotnes lietotājam, kas atlasa vienu no uzskaitījuma opcijām, kuras ir pieejamas pielāgotajam laukam “Testa virkne”.  Abas opcijas ir “Pirmā opcija” un “Otrā opcija” un tiek rādītas kā radiopogas. Pašlaik ir atlasīta otrā opcija.

![Opciju pogas (radiopogas) testa virknes pielāgotajam laukam](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Tabulas TSTimesheetLine paplašināšana, lai tai būtu pielāgots lauks

Tipiskos scenārijos darba laika uzskaites tabulas ieraksta sadaļas pielāgotā lauka dati visticamāk tiks saglabāti tabulā TSTimesheetLine. Taču var izmantot citas tabulas, ja datus var izgūt, pamatojoties uz nodrošināto TSTimesheetTrans ierakstu, vai ja tam nav konkrēta ieraksta konteksta (piemēram, ja projekta parametros šis lauks ir iestatīts kā tikai lasāms).

Ņemiet vērā, ka pielāgotajiem laukiem pamatā nav datu bāzes ieraksti. Tos var dinamiski ģenerēt, pamatojoties uz X++ loģiku. Šī pieeja var būt noderīga tikai lasāmos scenārijos (dinamiski ģenerētu pielāgotu lauku vērtību piemēru skatiet sadaļā “Komandķēdes lietošana klasē TSTimesheetDetails, metodē buildCustomFieldListForHeader, lai aizpildītu darba laika uzskaites tabulas informāciju”.)

Tālāk ir ekrānuzņēmums no programmas objektu koka Visual Studio. Tajā ir redzams TSTimesheetLine tabulas paplašinājumu ar lauku TestLineString, kas ir pievienots kā pielāgots lauks.

![Rindas virkne](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Komandķēdes lietošana klases TSTimesheetSettings metodei buildCustomFieldList, lai darba laika uzskaites tabulas ieraksta sadaļā rādītu kādu lauku

Šis kods kontrolē programmas lauka rādīšanas iestatījumus. Tas kontrolē, piemēram, lauka tipu, etiķeti, vai lauks ir obligāts un kurā sadaļā šis lauks tiek rādīts.

Nākamajā piemērā ir parādīts virknes lauks laika ierakstos. Šim laukam ir divas opcijas, **Pirmā opcija** un **Otrā opcija**, un tās ir pieejamas, izmantojot opciju pogas (radiopogas). Šis lauks programmā ir saistīts ar lauku **TestLineString**, kas ir pievienots tabulai TSTimesheetLine.

Ņemiet vērā metodes **TSTimesheetCustomField::newFromMetatdata()** lietošanu, lai vienkāršotu inicializēšanu pielāgotajiem lauku rekvizītiem: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** un **numberOfDecimals**. Šos parametrus varat iestatīt arī manuāli, ja vēlaties.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Komandķēdes lietošana klases TSTimesheetEntry metodei buildCustomFieldListForEntry, lai darba laika uzskaites tabulas ierakstā ievadītu vērtības

Metode **buildCustomFieldListForEntry** tiek lietota, lai ievadītu vērtības mobilajā programmā saglabātajās darba laika uzskaites tabulas rindās. Šī metode kā parametru izmanto ierakstu TSTimesheetTrans. Laukus no šī ieraksta var izmantot, lai programmā aizpildītu pielāgotā lauka vērtību.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Komandķēdes lietošana klasei TSTimesheetEntryService, lai darba laika uzskaites tabulas ierakstu no programmas saglabātu atpakaļ datu bāzē

Lai pielāgotu lauku saglabātu atpakaļ datu bāzē tipiskā lietojumā, jums ir jāpaplašina vairākas metodes.

- Metode **timesheetLineNeedsUpdating** tiek lietota, lai noteiktu, vai lietotājs ir mainījis rindas ierakstu programmā un vai tas ir jāsaglabā datu bāzē. Ja nav jāraizējas par veiktspēju, šo metodi var vienkāršot, lai tā vienmēr atgrieztu vērtību **true**.
- Metodi **populateTimesheetLineFromEntryDuringCreate** un **populateTimesheetLineFromEntryDuringUpdate** var paplašināt tā, lai tās ievadītu vērtības TSTimesheetLine datu bāzes ierakstā no nodrošinātā TSTimesheetEntry datu līguma ieraksta. Nākamajā piemērā pievērsiet uzmanību tam, kā kartēšana starp datu bāzes lauku un ieraksta lauku tiek manuāli veikta, izmantojot X++ kodu.
- Metodi **populateTimesheetWeekFromEntry** var arī paplašināt, ja pielāgotajam laukam, kas ir kartēts uz **TSTimesheetEntry** objektu, būtu jāraksta atpakaļ uz TSTimesheetLineweek datu bāzes tabulu.

> [!NOTE]
> Nākamajā piemērā lietotāja atlasītā vērtība **firstOption** vai **secondOption** tiek saglabāta datu bāzē kā neapstrādātas virknes vērtība. Ja datu bāzes lauks ir lauks ar tipu **Uzskaitījums**, šīs vērtības var manuāli kartēt uz uzskaitījuma vērtību un pēc tam saglabāt datu bāzes tabulas uzskaitījuma laukā.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Pielāgotu lauku rādīšana darba laika uzskaites tabulas virsraksta sadaļā

Tālāk ir ekrānuzņēmums no mobilās lietotnes lietotājam, kurš apskata darba laika uzskaites tabulu. Augšējā labajā stūrī ir atlasīta poga “Papildinformācija”, lai rādītu opciju “Skatīt vairāk informācijas”.  

![Komanda Skatīt vairāk informācijas](media/show-more.png)

Tālāk ir ekrānuzņēmums no mobilās lietotnes, kur ir redzama darba laika uzskaites tabulas sadaļa “Vairāk”. Darba laika uzskaites tabulas virsraksta sadaļai ir pievienots pielāgots lauks ar nosaukumu “Šīs darba laika uzskaites tabulas lietojuma koeficients (aprēķināts pielāgots lauks)”. Pielāgotajā laukā ir iestatīta tikai lasāma vērtība “0,667”.

![Sadaļa Vairāk](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Tabulas TSTimesheetTable paplašināšana, lai tai būtu pielāgots lauks

Tipiskos scenārijos virsraksta sadaļas pielāgotā lauka dati visticamāk tiks izgūti no tabulas TSTimesheetHeader. Taču var izmantot citas tabulas, ja datus var izgūt, pamatojoties uz nodrošināto TSTimesheetTable ierakstu, vai ja tam nav konkrēta ieraksta konteksta (piemēram, ja projekta parametros šis lauks ir iestatīts kā tikai lasāms).

Ņemiet vērā, ka pielāgotajiem laukiem pamatā nav datu bāzes ieraksti. Tos var dinamiski ģenerēt, pamatojoties uz X++ loģiku. Šī pieeja ir parādīta nākamajā piemērā.

Programmā lauki virsraksta sadaļā vienmēr ir tikai lasāmi.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Komandķēdes lietošana klases TSTimesheetSettings metodei buildCustomFieldList, lai virsraksta sadaļā rādītu kādu lauku

Šis kods kontrolē programmas lauka rādīšanas iestatījumus. Tas kontrolē, piemēram, lauka tipu, etiķeti, vai lauks ir obligāts un kurā sadaļā šis lauks tiek rādīts.

Nākamajā piemērā ir parādīta aprēķināta vērtība programmas virsraksta sadaļā.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Komandķēdes lietošana klases TSTimesheetDetails metodei buildCustomFieldListForHeader, lai aizpildītu darba laika uzskaites tabulas informāciju

Metode **buildCustomFieldListForHeader** tiek lietota, lai mobilajā programmā aizpildītu darba laika uzskaites tabulas virsraksta informāciju. Šī metode kā parametru izmanto ierakstu TSTimesheetTable. Laukus no šī ieraksta var izmantot, lai programmā aizpildītu pielāgotā lauka vērtību. Nākamajā piemērā no datu bāzes netiek nolasītas nekādas vērtības. Tā vietā tiek izmantota X++ loģika, lai ģenerētu aprēķinātu vērtību, kura pēc tam tiek rādīta programmā.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Citas konfigurēšanas/paplašināšanas iespējas

### <a name="adding-additional-validation-for-the-app"></a>Papildu validēšanas pievienošana programmai

Pastāvošā darba laika uzskaites tabulas funkcionalitātes loģika datu bāzes līmenī joprojām darbosies paredzētajā veidā. Lai pārtrauktu saglabāšanas vai iesniegšanas operāciju pabeigšanu un parādītu konkrētu kļūdas ziņojumu, varat kodam pievienot **throw error("ziņojums lietotājam")**, izmantojot komandķēdes paplašinājumu. Tālāk ir trīs noderīgu paplašināmu metožu piemēri.

- Ja **validateWrite** tabulā TSTimesheetLine atgriež **false** kādas darba laika uzskaites tabulas rindas saglabāšanas operācijas laikā, mobilajā programmā tiek parādīta kļūda.
- Ja **validateSubmit** tabulā TSTimesheetTable atgriež **false** laikā, kad darba laika uzskaites tabula tiek iesniegta programmā, lietotājam tiek parādīta kļūda.
- Joprojām darbosies loģika, kas aizpilda laukus (piemēram, **Rindas rekvizīts**) tabulai TSTimesheetLine metodes **ievietot** laikā.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Standarta komplektācijā ietverto lauku slēpšana un atzīmēšana kā tikai lasāmus, izmantojot konfigurāciju

No projekta parametriem standarta komplektācijā ietvertos laukus mobilajā programmā varat padarīt par tikai lasāmiem vai paslēptiem. Iestatiet opcijas lapas **Projektu vadības un uzskaites parametri** cilnes **Darba laika uzskaites tabula** sadaļā **Mobilās darba laika uzskaites tabulas**.

![Projektu parametri](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Tādu aktivitāšu maiņa, kuras ir pieejamas atlasīšanai, izmantojot paplašinājumus

Aktivitātes, kas projektam ir pieejamas atlasīšanai, tiek aizpildītas, izmantojot metodi **getActivitiesForProject()** un **getActivityQuery()** klasē **TsTimesheetProjectService**. Varat izmantot komandķēdi, lai mainītu šo uzvedību un padarītu to atbilstošu jūsu biznesa scenārijam attiecība uz aktivitātēm, kas ir pieejamas atlasīšanai kādam noteiktam projektam.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Noklusējuma projekta kategorijas ievadīšana darba laika uzskaites tabulu ierakstos

Noklusējuma projekta kategorijas ievadīšana darba laika uzskaites tabulu ierakstos notiek trīs līmeņos. Lai sasniegtu vēlamo uzvedību, varat izmantot komandķēdi, lai paplašinātu šo uzvedību jebkurā līmenī vai visos šajos līmeņos. Tiek izmantota tālāk aprakstītā hierarhija.

1. Programma mēģina ievietot noklusējuma kategoriju no projekta resursa. Šī noklusējuma kategorija ir iestatīta metodē **getCurrentUserResource** un **getDelegatedResourcesForCurrentUser**, klasē **TSTimesheetSettingsService**.
2. Ja noklusējuma kategorija nav norādīta projekta resursa līmenī, programma mēģina to izgūt no projekta aktivitātes. Šī noklusējuma kategorija ir iestatīta metodē **getActivitiesForProject**, klasē **TSTimesheetProjectService**.
3. Ja noklusējuma kategorija nav norādīta projekta aktivitātes līmenī, noklusējuma kategorija tiek ņemta no projekta parametriem. Šī noklusējuma kategorija ir iestatīta metodē **getProjectDetailsbyRule**, klasē **TSTimesheetProjectService**.
