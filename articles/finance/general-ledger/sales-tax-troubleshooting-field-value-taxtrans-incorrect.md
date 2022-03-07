---
title: Nepareiza lauka vērtība kolonnā TaxTrans
description: Šajā tēmā sniegta informācija par nepareizu lauka vērtību novēršanu kolonnā TaxTrans.
author: EricWangChen
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 00424d98d5ff99123edf42ee19919d149e7a6abc
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488291"
---
# <a name="incorrect-field-value-in-taxtrans"></a>Nepareiza lauka vērtība kolonnā TaxTrans

[!include [banner](../includes/banner.md)]

Ja lauka vērtība kolonnā **TaxTrans** nav pareiza, izmantojiet informāciju šajā tēmā, lai mēģinātu atrisināt šo problēmu.

## <a name="overview-of-values"></a>Vērtību apskats
Šajā sarakstā ir parādīts, kā **TaxTrans**, **TaxUncommitted** un **TmpTaxWorkTrans** ir līdzīgas datu kopas, bet darbojas citādi.

  - **TaxTrans** ir pēdējais grāmatoto nodokļu transakciju rezultāts, kas saglabājas datu bāzē.
  - **TaxUncommitted** ir vidējais aprēķinātais nodokļu rezultāts, kas saglabājas datu bāzē (ja piemērojams), kas vēlāk tiks izmantota grāmatojot.
  - **TmpTaxWorkTrans** ir pagaidu aprēķinātais nodokļu rezultāts atmiņā esošajā tabulā (Tabulas tips = Atmiņā).

Ja konstatējat nepareizu kolonnu **TaxTrans** ir atrasts arī pamatcēlonis nepareizai kolonnai **TaxUncommitted** vai **TmpTaxWorkTrans**. Tas ir tāpēc, ka trīs kolonnas tiek kopētas viena no otras.

Parasti nodokļu aprēķina laikā tiek ģenerēts **TmpTaxWorkTrans** un pēc tam, ja piemērojams, tiek ģenerēts **TaxUncommitted**. Nodokļu grāmatošanas laikā tiek ģenerēts **TaxTrans**.


## <a name="add-breakpoints"></a>Pievienot pārtraukumpunktus
Lai pievienotu pārtraukumpunktus, veiciet tālāk norādītās darbības: 

1. Paplašinājumu un pārtraukumpunktu pievienošana paplašinājumos *ievietot()* un *atjaunināt()*.

     - **TaxTrans**

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TaxUncommitted**

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TmpTaxWorkTrans**

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. Alternatīvi pārtraukumpunktus var pievienot tieši, ja **TaxUncommitted** nav iekļauts.

     - *TaxTrans.insert()*, *TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>Pavairot un atkļūdot

Kad pārtraukumpunkti ir iestatīti, atkļūdošanas laikā tiek redzamas visas datu saglabātās izmaiņas. Lai atrastu nepareizas **TaxTrans**, **TaxUncommitted** vai **TmpTaxWorkTrans** kolonnas pamatcēloni, pārskatiet un atzīmējiet šādus elementus:

- Pēdējais pārtraukumpunkts, kur kolonna ir pareiza.
- Pirmais pārtraukumpunkts, kur kolonna ir nepareiza.
- Kas notiek starp šiem diviem punktiem.

## <a name="determine-whether-customization-exists"></a>Noteikt, vai pielāgojums pastāv
Ja esat pabeidzis iepriekšējās sadaļās norādītās darbības, bet problēmas nav iespējams atrisināt, nosakiet, vai pielāgošana eksistē. Ja pielāgošana nepastāv, sazinieties ar Microsoft atbalsta dienestu, lai saņemtu palīdzību.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

