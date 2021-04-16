---
title: AI-ML-pohjaisten tuotesuositustulosten muokkaaminen
description: Tässä ohjeaiheessa kerrotaan, miten yrityksen tuotesuositusten tuloksia räätälöidään tekoälyn koneoppimisen perusteella.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfe04881e71558ed326025d8f2545c3c611df3aa
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796967"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a>AI-ML-pohjaisten tuotesuositustulosten muokkaaminen


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten yrityksen tuotesuositusten tuloksia muokataan tekoälyn koneoppimisen perusteella. 

Kun tuotesuositukset on otettu käyttöön, oletusasetukset tulevat voimaan. Nämä parametrit voivat toimia erilaisissa tilanteissa. Kannattaa käyttää jonkin verran aikaa ja pohtia, miten tulokset sopivat tuotteiden myyntiin. Suosittelemme tulosten arviointia muutaman päivän ajan, ennen kuin parametreja muutetaan ennen testaamista uudelleen. 

## <a name="understanding-recommendation-list-parameters"></a>Tietoja suositusluettelon parametreista

Tutustu siihen, miten parametrit vaikuttavat alla oleviin tuloksiin, ennen kuin muutat parametreja.

### <a name="trending-product-list"></a>Suosittujen tuotteiden luettelo

Suositut-tuoteluettelossa on kaksi parametria, jotka voi muuttaa:

![Esimerkki Suosituimmat-luettelon oletusparametreista](./media/exampletrendingparameters.png)

1. **Sisällytä uudet tuotteet X päivän ajalta** - Tuotteita, jotka on lisätty tiettyjä päiviä ennen kuluvaa päivää, voidaan käyttää tuote-ehdokkaiden valinnassa. Kuvan oletusarvo ehdottaa, että 180 päivää vanhempia tuotteita voi käyttää suosittujen tuotteiden luettelossa.
1. **Sisällytä myynti X päivän ajalta** - Myyntitapahtumia, jotka ovat tapahtuneet tiettyjä päiviä ennen kuluvaa päivää, voidaan käyttää tuotteiden tilaamisessa. Yllä oleva oletusarvo viittaa siihen, että kaikkia edellisten 30 päivän aikaisia tuoteostoja voidaan käyttää tuotteen sijoituksen määrittämisessä suosittujen tuotteiden luetteloa varten. 

### <a name="best-selling-product-list"></a>Myydyimpien tuotteiden luettelo

Liiketoiminnasta riippuen Myydyimmät-luettelossa voi olla eri tulokset kuin Suositut-luettelossa, vaikka molemmissa käytetään tapahtumatietoja tuotteiden järjestämiseksi. Koska myydyimmillä tuotteilla ei ole katkaisua lajittelupäivämäärän perusteella, Myydyimmät-luettelon tuotteissa voi olla hyvin suosittuja mutta vanhoja tuotteita, jotka ovat jo pudonneet suosittujen tuotteiden luettelosta. 

Myydyimmät-tuoteluettelossa on yksi parametri, jonka voi muuttaa:

![Esimerkki Myydyimmät-luettelon oletusparametrista](./media/examplebestsellingparameters.PNG)

1. **Sisällytä myynti X päivän ajalta** - Myyntitapahtumia, jotka ovat tapahtuneet tiettyjä päiviä ennen kuluvaa päivää, voidaan käyttää tuotteiden tilaamisessa. Yllä oleva oletusarvo viittaa siihen, että kaikkia edellisten 30 päivän aikaisia tuoteostoja voidaan käyttää tuotteen sijoituksen määrittämisessä myydyimpien tuotteiden luetteloa varten. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Tuotteiden lisääminen suositusluetteloihin tai niiden poistaminen luetteloista manuaalisesti

### <a name="for-new-trending-or-best-selling-lists"></a>Uudet-, suositut- tai myydyimmät -luettelot

1.  Siirry kohtaan **Retail ja Kauppa** > **Tuotesuositukset** > **Suositusparametrit**.
1.  Valitse jaettujen parametrien luettelossa **Suositusluettelot**.
1.  Valitse luettelon lisätyt tai poistetut tuotteet.
1.  Voit lisätä tuotteita taulukkoon valitsemalla **Lisää rivi**. 
1.  Etsi tuotesarakkeesta tuotteen **Nimi** tai **Tuotenumero.**

    ![Esimerkki tuotteen etsimisestä uudesta tuoteluettelosta](./media/examplenewlistconfiguration1.png)

1.  Valitse Rivityyppi-sarakkeesta jompikumpi seuraavista vaihtoehdoista:
    -   **Sisällytä** – Pakottaa tuotteen luettelon alkuun
    -   **Jätä pois** – Estää tuotetta näkymästä luettelossa
    
    ![Esimerkki tuotteen sisällytysluettelosta tai poisjättämisestä uuden tuoteluettelon avulla](./media/examplenewlistconfiguration2.png)

1.  Jos **näyttöjärjestystä** muutetaan, **Sisällytä**-merkinnän saaneiden tuotteiden järjestys luettelossa muuttuu.
    - Jos kahdella tuotteilla on sama **näyttöjärjestyksen** arvo, näiden kahden tuloksen lopullinen järjestys voi poiketa taustasovelluksen järjestyksestä.
1.  Voit poistaa tuotteita taulukosta valitsemalla poistettavan rivin ja valitsemalla sitten **Poista**.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>Ihmiset pitävät myös- tai Ostetaan usein yhdessä -luettelot

Ostetaan usein yhdessä- tai Ihmiset pitävät myös -luetteloiden kontekstissa koneoppimista käytetään kuluttajan ostomallien analysoimisessa. Näin voidaan suositella liittyviä tuotteita, jotka ostetaan usein yhdessä yksilöllisen alkutuotteen kohdalla. 
 
*Alkutuote* on tuote, jolle haluat luoda tuloksia. Lisää tälle tuotteelle tuloksia tai poista niitä, kun haluat muokata suositusluetteloita manuaalisesti. 

Seuraavia ohjeita noudattamalla voit lisätä alkutuotteen tuloksia tai poistaa niitä:
1.  Valitse **Alkutuote**. 
1.  Valitse **Tuote**-sarakkeessa ominaisuutta **nimellä** tai **tuotenumerolla.**
![Esimerkki tuotteen hakemisesta Ostetaan usein yhdessä -luettelosta](./media/exampleFBTlistconfiguration1.png)
1. Valitse **Rivityyppi**-sarakkeesta jompikumpi seuraavista vaihtoehdoista:
    - **Sisällytä** – Pakottaa tuotteen luettelon alkuun
    - **Jätä pois** – Estää tuotetta näkymästä luettelossa     
![Esimerkki tuotteen sisällyttämisestä Ostetaan usein yhdessä -luetteloon tai sen sulkemisesta pois luettelosta](./media/exampleFBTlistconfiguration2.png)
1.  Voit poistaa tuotteita taulukosta valitsemalla poistettavan rivin ja valitsemalla sitten Poista.


## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä](enable-adls-environment.md)

[Tuotesuositusten ottaminen käyttöön](enable-product-recommendations.md)

[Kohdennettujen suositusten ottaminen käyttöön](personalized-recommendations.md)

[Kohdennetuista tuotesuosituksista kieltäytyminen](personalization-gdpr.md)

["Osta samankaltaisia tyylejä" -suositusten käyttöönotto](shop-similar-looks.md)

[Tuotesuositusten lisääminen myyntipisteessä](product.md)

[Suositusten lisääminen tapahtumanäyttöön](add-recommendations-control-pos-screen.md)

[Kuratoitujen suositusten manuaalinen luominen](create-editorial-recommendation-lists.md)

[Suositusten luominen esittelytietojen avulla](product-recommendations-demo-data.md)

[Tuotesuositukset – usein kysytyt kysymykset](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]