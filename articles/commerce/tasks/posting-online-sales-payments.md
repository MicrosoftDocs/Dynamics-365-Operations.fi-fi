---
title: Online-myynti- ja maksujen kirjaaminen
description: Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan verkkokaupan tapahtumien myyntitilausten ja maksujen luomista varten.
author: psimolin
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58af31464768e988bfa8727bcd836032d06b3a9dcfb416c3b9ed274af3285c79
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720901"
---
# <a name="posting-of-online-sales-and-payments"></a>Online-myynti- ja maksujen kirjaaminen

[!include [banner](../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan verkkokaupan tapahtumien myyntitilausten ja maksujen luomista varten.

Online-myynnin ja maksujen kirjaaminen on kaksivaiheinen prosessi.

- Online-kaupan tapahtumatietojen vetäminen pääkonttorissa.
- Synkronoidaan tilauksia, jotta myyntitilaukset luodaan pääkonttorissa.

Online-myynnin tapahtumatietojen vetäminen onnistuu joko suorittamalla P-työ manuaalisesti tai luomalla toistuva erätyö.

### <a name="manually-running-the-p-job"></a>P-työn manuaalinen suoritus

1. Valitse Kaikki työtilat > Retail ja Commerce IT.
2. Valitse Jakeluaikataulu.
3. Valitse P-0001.
4. Säädä kanavan tietokantaryhmiä tarvittaessa.
5. Valitse Suorita nyt.
6. Valitse Kyllä.

### <a name="scheduling-a-recurring-p-job"></a>Toistuvan P-työn ajoittaminen

1. Valitse Kaikki työtilat > Retail ja Commerce IT.
2. Valitse Jakeluaikataulu.
3. Valitse P-0001.
4. Valitse Luo erätyö.
5. valitse Suorita taustalla.
5. Ota käyttöön Eräkäsittely.
6. Valitse Toistuminen.
7. Valitse päättymispäivämääräasetuksen arvoksi Ei.
8. Syötä Määrä-kenttään ajojen aikaväli minuutteina. Yleensä tämä olisi 5-10.
9. Valitse OK.
10. Valitse OK.

Tilaukset voidaan synkronoida joko manuaalisesti suorittamalla Synkronoi tilaukset -työ tai luomalla toistuva erätyö.

### <a name="manually-running-order-synchronization"></a>Tilauksen synkronoinnin suorittaminen manuaalisesti 

Suorittamalla seuraavat vaiheet voit suorittaa "Synkronoi tilaukset" -työn manuaalisesti kerran.

1. Siirry kohtaan Kaikki työtilat > Myymälän myyntitiedot.
2. Valitse Synkronoi tilaukset.
3. Valitse Organisaatiohierarkia-kentässä Myymälät alueen mukaan.
    * Valitse tietty verkkokauppa tai solmu, jos haluat luoda myymäläryhmälle erätyön.  
    * Lisää valinta nuolen avulla.  
4. Valitse Laajenna Suorita taustalla -välilehti.
5. Ota pois käytöstä Eräkäsittely.
6. Valitse Toistuminen.
7. Valitse Päättyy jälkeen -vaihtoehto
8. Kirjoita Päättyy jälkeen -kenttään 1.
9. Valitse OK.
10. Valitse OK.

### <a name="scheduling-recurring-order-synchronization"></a>Toistuvien tilausten synkronointien ajoittaminen

Tässä menettelyssä kerrotaan, miten toistuva erätyö määritetään ja suoritetaan verkkokaupan tapahtumien myyntitilausten ja maksujen luomista varten. Menettely käyttää esittelytietojen USRT-yritystä.

1. Siirry kohtaan Kaikki työtilat > Myymälän myyntitiedot.
2. Valitse Synkronoi tilaukset.
3. Valitse Organisaatiohierarkia-kentässä Myymälät alueen mukaan.
    * Valitse tietty verkkokauppa tai solmu, jos haluat luoda myymäläryhmälle erätyön.  
    * Lisää valinta nuolen avulla.  
4. Valitse Laajenna Suorita taustalla -välilehti.
5. Ota käyttöön Eräkäsittely
6. Valitse Toistuminen.
7. Valitse päättymispäivämääräasetuksen arvoksi Ei.
8. Syötä Määrä-kenttään ajojen aikaväli minuutteina. Yleensä tämä olisi 2-20
9. Valitse OK.
10. Valitse OK.

## <a name="data-entities-involved-in-the-process"></a>Prosessiin liittyvät tietoyksiköt

- RetailTransactionTable
- RetailTransactionAddressTrans
- RetailTransactionInfocodeTrans
- RetailTransactionTaxTrans
- RetailTransactionSalesTrans
- RetailTransactionTaxMeasure
- RetailTransactionDiscountTrans
- RetailTransactionTaxTransGTE
- RetailTransactionMarkupTrans
- RetailTransactionPaymentTrans
- RetailTransactionAttributeTrans


[!INCLUDE[footer-include](../../includes/footer-banner.md)]