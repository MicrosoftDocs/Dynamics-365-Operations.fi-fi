---
title: luoda myyntitilauksia
description: Tässä menettelyssä näytetään, miten myyntitilaus luodaan.
author: Henrikan
ms.date: 04/06/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User, SalesTableDelete, SalesTableListPagePreviewPage, SalesUpdateRemain
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 462f47ab5d85665ed8132e5bfb6dd945c537c1ef
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551721"
---
# <a name="create-sales-orders"></a>luoda myyntitilauksia

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä näytetään, miten myyntitilaus luodaan. Voit käyttää tätä menettelyä esittely-yrityksessä USMF. Myyntitilausten käsittelijä luo yleensä myyntitilaukset. 

## <a name="enter-sales-order-header-details"></a>Syötä myyntitilauksen otsikon tiedot
1. Valitse **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset**.
2. Valitse **Uusi**.
3. Avaa haku valitsemalla **Asiakastili**-kentässä avattavan valikon painike.
4. Etsi asiakastietue luettelosta ja valitse se.
    - Valitse tässä esimerkissä asiakasnumero US-004.  
5. Valitse **OK**.

## <a name="enter-sales-order-line-details"></a>Syötä myyntitilausrivin tiedot
    
Organisaation myymät tuotteet voivat olla dimensioiden erottelemia variantteja, kuten määritys, väri, koko ja tyyli. Tuotteet voidaan määrittää myös käyttämään varastodimensioita, kuten toimipaikkaa, varastoa ja kuormalava, sekä seurantadimensioita, kuten erää ja sarjanumeroita. Valitse dimensioiden määrittämisen jälkeen kyseisille tilausrivin dimensioille arvot. Voit parantaa tilaustenkäsittelyn tehokkuutta lisäämällä tilausruudukkoon vastaavien dimensioiden kentät.
    
1. Valitse **Myyntitilausrivit**-osassa **Myyntitilausrivi**.
2. Valitse **Dimensiot**.
    
    Tässä esimerkissä valitaan väri-, toimipaikka ja varastodimensio. Tässä valitut dimensiot näkyvät myyntitilausruudukossa. Jos haluat säilyttää valinnat, määritä **Tallenna asetukset** -vaihtoehdon arvoksi Kyllä.
    
3. Valitse **OK**.
4. Avaa haku valitsemalla **Nimiketunnus**-kentässä avattavan valikon painike.
5. Valitse tässä esimerkissä nimiketunnus T0004.
    - Jos nimike on osa myyntiluokkaa, nimikkeen nimi näkyy automaattisesti Myyntiluokka-kentässä.  
    - Jos tuotedimensiokentissä on jo arvo, se on luultavasti kopioitu tuotetietueesta, jossa se on määritetty oletustuotedimensioksi. Voit muuttaa oletusarvoa milloin tahansa.   
6. Avaa haku valitsemalla **Väri**-kentässä avattavan valikon painike.
7. Etsi haluamasi tietue luettelosta ja valitse se.
8. Anna **Määrä**-kentässä numero.
    - Jos nimike myydään eri yksikköinä kuin missä se ostettiin, tuotettiin ja varastoitiin, ja myynnin mittayksikkö on määritetty tuotetietueessa, tämä arvo näkyy **Yksikkö**-kentässä. Voit muuttaa arvoa milloin tahansa.   
    - Jos **Toimipaikka**-kentässä on jo arvo, se on kopioitu tilausotsikosta tai tuotteeseen liitetyistä tilausasetuksista. Voit muuttaa arvoa milloin tahansa. Jos kenttä on tyhjä, valitse arvo.   
    - Jos **Yksikön hinta** -kentässä on jo arvo, se on kopioitu kelvollisesta kauppasopimuksesta tai tuotetietueesta. (Yksikköhinta voi olla peräisin myös myyntisopimuksesta, mutta myyntitilausten luontiprosessi myyntisopimuksista on erilainen kuin tässä esiteltävä prosessi.) Jos kenttä on tyhjä, syötä arvo.   
    - **Alennus**-kenttä sisältää tuoteyksikkökohtaisen alennussumman. Voit laskea rivialennuksen kokonaissumman kertomalla alennuksen arvon rivin määrällä. Jos **Alennus**-kentässä on jo arvo, se on kopioitu kelvollisesta kauppasopimuksesta. Syötä arvo, jos kenttä on tyhjä ja haluat antaa asiakkaalle rivialennuksen.  
    - **Alennusprosentti**-kenttä sisältää prosenttiarvon, jonka mukaan rivin kokonaisbruttosummaa vähennetään.  Jos **Alennusprosentti**-kentässä on jo arvo, se on kopioitu kelvollisesta kauppasopimuksesta. Syötä arvo, jos kenttä on tyhjä ja haluat antaa asiakkaalle rivialennuksen. 
    - **Nettosumma**-kentässä on arvo, joka on laskettu rivisumman ja alennusten mukaan oikaistun yksikköhinnan perusteella.  Lasketun arvon voi korvata toisella arvolla.  

## <a name="review-the-order-totals"></a>Tarkastele tilauksen kokonaissummia
1. Valitse **toimintoruudussa** **Myyntitilaus**.
2. Valitse **Summat**.
    
    **Summat**-sivulla näkyvät koko tilauksen tiedot. Näkyvillä olevia tietoja ovat esimerkiksi välisumma, joka on lopullisille rivialennuksille oikaistujen kaikkien rivin nettosummien summa, laskun kokonaissumma, joka on lopullisille tilaustason alennukselle oikaistu kokonaisvälisumma, kulut, arvonlisävero ja asiakkaan luottorajan tilanne. Laskun summa on asiakkaan laskuasiakirjassa näkyvä summa.  
    
3. Valitse **OK**.

## <a name="sales-order-creation-performance-enhancement"></a>Myyntitilauksen luonnin suorituskykyparannus
Sovelluksen 10.0.26 version uusi ominaisuus vähentää taulujen **SourceDocumentHeader** ja **SourceDocumentLine** lisätietueiden luontia. Suorituskykyä parannetaan ja tallennuskoko pienenee, koska näitä tietueita ei luoda. Näitä taustalla olevia lähdeasiakirjakehystaulukoita ei käytetä tällä hetkellä tuotteen myyntitilauksissa, eikä niiden hyödyntämistä ole suunniteltu. Tämän ominaisuuden ottaminen käyttöön on turvallinen muutos suorituskyvyn parantamiseksi. 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
