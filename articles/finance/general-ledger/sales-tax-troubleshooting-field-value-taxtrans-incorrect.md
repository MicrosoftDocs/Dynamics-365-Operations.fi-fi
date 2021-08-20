---
title: TaxTrans-kentän arvo on virheellinen
description: Tässä aiheessa on tietoja virheellisten kenttien arvojen vianmäärityksestä TaxTrans-kentässä.
author: bijian
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
ms.openlocfilehash: 5c1c034c6037d2e8920d9744903debebb2dc537f2644093d5e1eef66f2681191
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746341"
---
# <a name="incorrect-field-value-in-taxtrans"></a>TaxTrans-kentän arvo on virheellinen

[!include [banner](../includes/banner.md)]

Jos **TaxTrans**-kentän arvo on virheellinen, voit yrittää ratkaista ongelman tämän ohjeaiheen tietojen avulla.

## <a name="overview-of-values"></a>Arvojen yleiskatsaus
Seuraavassa luettelossa näkyy, että **TaxTrans**, **TaxUncommitted** ja **TmpTaxWorkTrans** ovat samanlaisia tietojoukkoja, mutta toimivat eri tavoin.

  - **TaxTrans** on viimeinen kirjattu verotapahtuman tulos, joka säilyy tietokannassa.
  - **TaxUncommitted** on väliaikainen laskettu verotulos, joka säilyy tietokannassa (jos käytettävissä), jota käytetään myöhemmin kirjauksen yhteydessä.
  - **TmpTaxWorkTrans** on väliaikainen laskettu verotulos muistissa olevassa taulukossa (taulutyyppi = InMemory).

Jos virheellisen **TaxTrans**-sarakkeen juurisyy löytyy, olet myös löytänyt virheellisen **TaxUncommitted**- tai **TmpTaxWorkTrans**-sarakkeen juurisyyn. Tämä johtuu siitä, että nämä kolme saraketta kopioidaan toisistaan.

Yleensä verolaskennan aikana luodaan **TmpTaxWorkTrans** ja sitten, jos käytettävissä, luodaan **TaxUncommitted**. Verojen kirjaamisen aikana luodaan **TaxTrans**.


## <a name="add-breakpoints"></a>Keskeytyskohtien lisääminen
Lisää keskeytyskohtia seuraavien ohjeiden mukaan: 

1. Lisää laajennuksia ja keskeytyskohtia *lisää()*- ja *päivitä()*-kohdissa laajennuksiin alla esitetyllä tavalla.

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

2. Voit myös lisätä keskeytyskohtia suoraan, kun **TaxUncommitted** ei sisälly.

     - *TaxTrans.insert()*, *TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>Toistaminen ja virheenkorjaus

Kun keskeytyskohdat on määritetty, kaikki tietojen säilymisen muutokset näkyvät virheenkorjauksen aikana. Voit etsiä juurisyyn virheelliselle sarakkeelle **TaxTrans**, **TaxUncommitted** tai **TmpTaxWorkTrans** tarkistamalla ja huomioimalla seuraavat nimikkeet:

- Viimeinen keskeytyskohta, jossa sarake on oikea.
- Ensimmäinen keskeytyskohta, jossa sarake on väärä.
- Mitä näiden kahden pisteen välillä tapahtuu.

## <a name="determine-whether-customization-exists"></a>Määritä, onko mukautus olemassa
Jos olet suorittanut edellisten osien vaiheet, mutta et voi ratkaista ongelmaa, selvitä, onko mukautus olemassa. Jos mukautusta ei ole, ota yhteyttä Microsoftin tukeen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

