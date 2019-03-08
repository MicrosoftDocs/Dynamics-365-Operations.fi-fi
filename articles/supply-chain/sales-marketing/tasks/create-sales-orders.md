---
title: luoda myyntitilauksia
description: Tässä menettelyssä näytetään, miten myyntitilaus luodaan.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8af0333d979ba3a4e12d4f22b1225f3b72d66a7a
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2019
ms.locfileid: "352111"
---
# <a name="create-sales-orders"></a>luoda myyntitilauksia

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä näytetään, miten myyntitilaus luodaan. Voit käyttää tätä menettelyä esittely-yrityksessä USMF. Myyntitilausten käsittelijä luo yleensä myyntitilaukset. 




## <a name="enter-sales-order-header-details"></a>Syötä myyntitilauksen otsikon tiedot
1. Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.
2. Valitse Uusi.
3. Avaa haku valitsemalla Asiakastili-kentässä avattavan valikon painike.
4. Etsi asiakastietue luettelosta ja valitse se.
    * Valitse tässä esimerkissä asiakasnumero US-004.  
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Valitse OK.

## <a name="enter-sales-order-line-details"></a>Syötä myyntitilausrivin tiedot
    * Organisaation myymät tuotteet voivat olla dimensioiden erottelemia variantteja, kuten määritys, väri, koko ja tyyli. Tuotteet voidaan määrittää myös käyttämään varastodimensioita, kuten toimipaikkaa, varastoa ja kuormalava, sekä seurantadimensioita, kuten erää ja sarjanumeroita. Valitse dimensioiden määrittämisen jälkeen kyseisille tilausrivin dimensioille arvot. Voit parantaa tilaustenkäsittelyn tehokkuutta lisäämällä tilausruudukkoon vastaavien dimensioiden kentät.  
1. Valitse myyntitilausrivi.
2. Valitse Dimensiot.
    * Tässä esimerkissä valitaan väri-, toimipaikka ja varastodimensio. Tässä valitut dimensiot näkyvät myyntitilausruudukossa. Jos haluat säilyttää valinnat, määritä Tallenna asetukset -vaihtoehdon arvoksi Kyllä.   
3. Valitse OK.
4. Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.
5. Valitse tässä esimerkissä nimiketunnus T0004.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Jos nimike on osa myyntiluokkaa, nimikkeen nimi näkyy automaattisesti Myyntiluokka-kentässä.  
    * Jos tuotedimensiokentissä on jo arvo, se on luultavasti kopioitu tuotetietueesta, jossa se on määritetty oletustuotedimensioksi. Voit muuttaa oletusarvoa milloin tahansa.   
7. Avaa haku valitsemalla Väri-kentässä avattavan valikon painike.
8. Etsi haluamasi tietue luettelosta ja valitse se.
9. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
10. Kirjoita numero Määrä-kenttään.
    * Jos nimike myydään eri yksikköinä kuin missä se ostettiin, tuotettiin ja varastoitiin, ja myynnin mittayksikkö on määritetty tuotetietueessa, tämä arvo näkyy Yksikkö-kentässä. Voit muuttaa arvoa milloin tahansa.   
    * Jos Toimipaikka-kentässä on jo arvo, se on kopioitu tilausotsikosta tai tuotteeseen liitetyistä tilausasetuksista. Voit muuttaa arvoa milloin tahansa. Jos kenttä on tyhjä, valitse arvo.   
    * Jos Yksikön hinta -kentässä on jo arvo, se on kopioitu kelvollisesta kauppasopimuksesta tai tuotetietueesta. (Yksikköhinta voi olla peräisin myös myyntisopimuksesta, mutta myyntitilausten luontiprosessi myyntisopimuksista on erilainen kuin tässä esiteltävä prosessi.) Jos kenttä on tyhjä, syötä arvo.   
    * Alennus-kenttä sisältää tuoteyksikkökohtaisen alennussumman. Voit laskea rivialennuksen kokonaissumman kertomalla alennuksen arvon rivin määrällä.    Jos Alennus-kentässä on jo arvo, se on kopioitu kelvollisesta kauppasopimuksesta. Syötä arvo, jos kenttä on tyhjä ja haluat antaa asiakkaalle rivialennuksen.  
    * Alennusprosentti-kenttä sisältää prosenttiarvon, jonka mukaan rivin kokonaisbruttosummaa vähennetään.  Jos Alennusprosentti-kentässä on jo arvo, se on kopioitu kelvollisesta kauppasopimuksesta. Syötä arvo, jos kenttä on tyhjä ja haluat antaa asiakkaalle rivialennuksen.  
    * Nettosumma-kentässä on arvo, joka on laskettu rivisumman ja alennusten mukaan oikaistun yksikköhinnan perusteella.  Lasketun arvon voi korvata toisella arvolla.  

## <a name="review-the-order-totals"></a>Tarkastele tilauksen kokonaissummia
1. Valitse toimintoruudussa Myyntitilaus.
2. Valitse Summat.
    * Summat-sivulla näkyvät koko tilauksen tiedot. Näkyvillä olevia tietoja ovat esimerkiksi välisumma, joka on lopullisille rivialennuksille oikaistujen kaikkien rivin nettosummien summa, laskun kokonaissumma, joka on lopullisille tilaustason alennukselle oikaistu kokonaisvälisumma, kulut, arvonlisävero ja asiakkaan luottorajan tilanne.  Laskun summa on asiakkaan laskuasiakirjassa näkyvä summa.  
3. Valitse OK.

