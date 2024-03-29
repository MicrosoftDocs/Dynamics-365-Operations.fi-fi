---
title: Luo uusi kauppasopimus
description: Tämä menetelmä selittää, miten luodaan kauppasopimus, johon rekisteröidään tuotteen tietyn asiakkaan kanssa sovittu uusi hinta.
author: Henrikan
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24290ec873da9e871c001bcdc97e14dcad0e3d1e
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111104"
---
# <a name="create-a-new-trade-agreement"></a>Luo uusi kauppasopimus

[!include [banner](../../includes/banner.md)]

Tämä menetelmä selittää, miten luodaan kauppasopimus, johon rekisteröidään tuotteen tietyn asiakkaan kanssa sovittu uusi hinta. Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi. Jos käytät omia tietojasi, varmista ennen tämän ohjeen käyttöä, että kauppasopimuksen kirjauskansion nimi on kohteeseen, jossa Oletussuhde-arvoksi on valittu Hinta (myynti).

## <a name="create-and-post-a-new-trade-agreement-journal"></a>Luo ja kirjaa uusi kauppasopimuksen kirjauskansi

1. Valitse **Siirtymisruutu > Moduulit >Myynti ja markkinointi > Hinnat ja alennukset > Kauppasopimuksen kirjauskansiot**.
2. Valitse **Uusi**.
3. Avaa haku valitsemalla **Nimi**-kentässä avattavan valikon painike.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Valitse **toimintoruudussa** **Rivit**.
6. Valitse **Tilikoodi**-kentässä Taulu.
    
    Tässä esimerkissä päivitetään tietyn asiakkaan hinta, joten sinun on valittava Taulu. Jos päivittäisit tuotteen luettelohinnan, valitsisit Kaikki, jotta uusi hinta koskisi kaikkia asiakkaita. Jos eri asiakassegmenteillä olisi eri hinta, valitsisit Ryhmä. Ryhmä-vaihtoehdon käyttö edellyttää asiakkaan hintaryhmien määrittämistä.  

7. Avaa haku napsauttamalla **Tilin valinta** -kentässä avattavan valikon painiketta.
8. Etsi haluamasi tietue luettelosta ja valitse se.
9. Valitse **Nimikekoodi**-kentässä Taulu.
    
    Kun annat kauppasopimuksen tyypiksi Hinta (myynti), **Nimikekoodi**-kentässä valitaan vain Taulu. Tämä johtuu siitä, että hinta on absoluuttinen arvo eikä kaikilla tuotteilla tai tuoteryhmillä voi olla sama hinta.
    
10. Avaa haku napsauttamalla **Nimikkeen suhde**-kentässä avattavan valikon painiketta.
11. Valitse luettelossa sopimukseen sisällytettävä tuote. Kirjaa muistiin valitsemasi tuotteet.  
12. Anna **Mistä**-kenttään vähimmäismäärä.
    - Jos asiakkaalla on tietty määrä, joka on tilattava ennen uuden hinnan käyttöönottoa, määrä on ilmoitettava tässä.  
    - Määritä **Mihin**-kenttään arvo, jota suurempana sopimuksen hinta ei kelpaa. Jos hinnat ja alennukset perustuvat useisiin hintarajoihin, määritä kunkin hintahaarukan vähimmäis- ja enimmäismäärä **Mistä**- ja **Mihin**-kenttiin.
13. Anna **Summa valuuttana** -kenttään hinta.
14. Anna **Tiedot**-osan **Päivämäärästä**-kenttään päivämäärä, jolloin sopimus astuu voimaan.
15. Valitse **Tallenna**.
16. Valitse **Vahvista**.
17. Valitse **Tarkista valitut rivit**.
18. Valitse **OK**.
19. Valitse **Kirjaa**.
20. Valitse **OK**.

## <a name="view-trade-agreements-for-a-product"></a>Näytä tuotteen kauppasopimukset

1. Valitse **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**.
2. Etsi ja valitse luettelosta tuote, jonka hinnan päivitit.
3. Valitse **toimintoruudussa** **Myynti**.
4. Valitse **Näytä kauppasopimukset**.
    
    Tarkastele juuri luodun hinnan kauppasopimuksen tietoja.

5. Sulje sivu.

## <a name="additional-resources"></a>Lisäresurssit

### <a name="whitepaper"></a>Tekninen raportti

Lisätietoja saa lataamalla seuraava tekninen raportti (joka on kirjoitettu tukemaan AX2012-versiota, mutta koskee myös Dynamics 365 Supply Chain Managementia)

- [Kauppasopimukset](https://download.microsoft.com/download/0/2/9/02972c8b-0159-4936-a3ef-1e64252b2d2f/TradeAgreementsInAX.pdf)

### <a name="community-blogs"></a>Yhteisöblogit

- [Talous- ja toimintosovellusten myyntihinnat](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
