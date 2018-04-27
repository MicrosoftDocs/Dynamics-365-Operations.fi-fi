---
title: "Laskujen täsmäytys ja konsernin sisäiset ostotilaukset"
description: "Konsernin sisäisen kauppatapahtuman ostavan yrityksen asetukset on voitu määritettää siten, että käytössä on ostoreskontran laskujen täsmäytys. Tässä tapauksessa sekä konsernin sisäisen välisen kaupan että ostoreskontran laskujen täsmäytyksen kirjausvaatimusten on täytyttävä, ennen kuin konsernin sisäiset ostolaskut voidaan kirjata."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3d0eb5c19c07313f4d4c0bac1b9c48375446afd9
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="invoice-matching-and-intercompany-purchase-orders"></a>Laskujen täsmäytys ja konsernin sisäiset ostotilaukset

[!INCLUDE [banner](../includes/banner.md)]

Konsernin sisäisen kauppatapahtuman ostavan yrityksen asetukset on voitu määritettää siten, että käytössä on ostoreskontran laskujen täsmäytys. Tässä tapauksessa sekä konsernin sisäisen välisen kaupan että ostoreskontran laskujen täsmäytyksen kirjausvaatimusten on täytyttävä, ennen kuin konsernin sisäiset ostolaskut voidaan kirjata.

Tämän ohjeaiheen esimerkeissä käytetään seuraavia konsernin sisäisen kaupan asetuksia:
-   Fabrikam Purchase on tuotteet ostava yritys.
-   Fabrikam Sales on tuotteet myyvä yritys.
-   Asiakas 4020 kuuluu yritykseen Fabrikam Sales.
-   Toimittaja 3024 kuuluu yritykseen Fabrikam Purchase.
-   Fabrikam Purchasessa konsernin sisäiset tiedot on määritetty toimittajalle 3024. Fabrikam Sales on määritetty asiakasyritykseksi ja asiakas 4020 on määritetty Fabrikam Purchase -yritystä vastaavaksi asiakastiliksi.
-   Fabrikam Salesissa konsernin sisäiset tiedot on määritetty asiakkaalle 4020. Fabrikam Purchase on määritetty toimittajayritykseksi ja toimittaja 3024 on määritetty Fabrikam Sales -yritystä vastaavaksi toimittajatiliksi.

Esimerkeissä käytetään seuraavia Fabrikam Purchase -yrityksen ostoreskontran laskujen täsmäytyksen asetuksia:
-   Ota käyttöön laskujen täsmäytyksen vahvistus -vaihtoehto on valittu Ostoreskontran parametrit -sivulla.
-   Kirjaa lasku, jossa on ristiriitoja -kentän arvoksi on valittu Ostoreskontran parametrit -sivulla Edellytä hyväksyntä.
-   Yrityksen hintatoleranssin prosentti on 2 prosenttia.

## <a name="example-price-matching-and-intercompany-trade"></a> Esimerkki: Hinnan täsmäytys ja konsernin sisäinen kauppa
Konsernin sisäisen ostolaskun ja konsernin sisäisen myyntilaskun nettosummien on oltava yhtä suuret. Tämä vaatimus ohittaa kaikki sovellettavat laskun täsmäytyksen hyväksynnän tai hintatoleranssiprosenttien vaatimukset. Esimerkiksi seuraavia ohjeita noudatetaan.
1.  Luo Fabrikam Purchase -yrityksessä asiakkaalle 4020 myyntitilaus SO888. Toimittajalle 3024 luodaan automaattisesti konsernin sisäinen ostotilaus ICPO222 Fabrikam Purchasessa ja Fabrikam Salessa luodaan automaattisesti myyntitilaus ICSO888.
2.  Rekisteröi nimikkeet Fabrikam Salesissa vastaanotetuiksi ja kirjaa pakkausluettelo. Tilauksen ICSO888 tilaksi tulee Toimitettu. Tilauksen ICPO222 tilaksi tulee Vastaanotettu.
3.  Päivitä tilauksen ICSO888 lasku Fabrikam Salesissa. Yksikköhinta on 0,45, ja päivitettäviä nimikkeitä on 100.
4.  Luo tilauksen ICPO222 lasku Fabrikam Purchasessa. Muutat nettohinnan arvon 45,00 vahingossa arvoksi 54,00. Näyttöön tuleva kuvake ilmaisee, että hinta ylittää sallitun 2 prosentin hintatoleranssin.
5.  Valitse Laskun täsmäytyksen tiedot -sivulla vaihtoehto, jolla hyväksytään täsmäytysristiriitojen kirjaaminen. Valitse Toimittajan lasku -sivulla OK Jos toimittajan lasku ei ole konsernin sisäinen ostolasku, kirjaus onnistuu. Koska kuitenkin käsittelet konsernin sisäistä ostolaskua, kirjaus ei onnistu. Konsernin sisäisessä kaupassa konsernin sisäisen myyntilauksen laskusumman on oltava sama kuin vastaavan konsernin sisäisen ostotilauksen laskusumma. Ratkaise tämä ongelma korjaamalla laskun nettohinta muuttamalla nettohinta takaisin oletussummaan 45,00.

## <a name="example-quantity-matching-with-intercompany-trade"></a> Esimerkki: Määrän täsmäytys konsernin sisäisessä kaupassa
Konsernin sisäisen ostotilauksen ja konsernin sisäisen myyntitilauksen määrän on oltava sama. Tämä vaatimus ohittaa sovellettavat laskun täsmäytyksen hyväksynnät. Tässä esimerkissä käytetään seuraavia konsernin sisäisen kaupan lisäasetuksia:
-   Toimittajan 3024 ostotilauksen toimenpidemenettely on määritetty Fabrikam Purchasessa siten, että sekä alkuperäinen myyntilasku että konsernin sisäinen ostolasku kirjataan automaattisesti.

Tässä esimerkissä käytetään seuraavia Fabrikam Purchasen ostoreskontran laskujen täsmäytyksen lisäasetuksia:
-   Nimikkeen B-R14 käyttämän malliryhmän Nimikemalliryhmät-sivulla on valittu Vastaanottovaatimukset-vaihtoehto.
-   Nimikkeen B-R14 käytettävissä oleva määrä on 0 (nolla).

Esimerkiksi seuraavia ohjeita noudatetaan.
1.  Luo Fabrikam Purchase -yrityksessä asiakkaalle 4020 myyntitilaus SO999. Tilauksessa on yksi rivinimike: 100 paristoa (nimike B-R14), jonka yksikköhinta on 1,00. Toimittajalle 3024 luodaan automaattisesti konsernin sisäinen ostotilaus ICPO333 Fabrikam Purchasessa ja Fabrikam Salessa luodaan automaattisesti myyntitilaus ICSO999.
2.  Päivitä tilauksen ICSO999 lasku Fabrikam Salesissa. Kirjaus ei onnistu, koska nimike on loppunut varastosta eikä sitä ole vielä vastaanotettu. Niinpä taloushallinnon tietoja ei voi päivittää.
3.  Rekisteröi nimikkeet Fabrikam Salesissa vastaanotetuiksi ja kirjaa tilauksen ICSO999 pakkausluettelo. Tilauksen ICPO333 tuotteen vastaanotto kirjataan automaattisesti Fabrikam Purchasessa. Nimikkeen B-R14 vastaanotettu määrä muuttuu Fabrikam Purchasessa arvoksi 100.
4.  Päivitä tilauksen ICSO999 lasku Fabrikam Salesissa. Kirjaus onnistuu molemmissa yrityksissä. Nimikkeen B-R14 ostettu määrä muuttuu Fabrikam Purchasessa arvoksi 100. 






