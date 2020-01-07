---
title: Hallitse AI-ML-pohjaisia tuotesuositustuloksia
description: Tässä ohjeaiheessa kerrotaan, miten yrityksen tuotesuositusten tuloksia räätälöidään tekoälyn koneoppimisen perusteella.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770067"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a>Hallitse AI-ML-pohjaisia tuotesuositustuloksia

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten yrityksen tuotesuositusten tuloksia räätälöidään tekoälyn koneoppimisen perusteella. 

Kun tuotesuositukset on otettu käyttöön, oletusasetukset tulevat voimaan. Nämä parametrit voivat toimia erilaisissa tilanteissa. Kannattaa käyttää jonkin verran aikaa ja pohtia, miten tulokset sopivat tuotteiden myyntiin. Suosittelemme tulosten arviointia muutaman päivän ajan, ennen kuin parametreja muutetaan ennen testaamista uudelleen. 

## <a name="understanding-recommendation-list-parameters"></a>Tietoja suositusluettelon parametreista

Tutustu siihen, miten parametrit vaikuttavat alla oleviin tuloksiin, ennen kuin muutat parametreja.

### <a name="trending-product-list"></a>Suosittujen tuotteiden luettelo

**Suosittujen** tuotteiden luettelossa on kaksi parametria, jotka voi muuttaa: ![Esimerkki Suositut-luettelon oletusparametreista](./media/exampletrendingparameters.png)
1. **Sisällytä uudet tuotteet X päivän ajalta** - Tuotteita, jotka on lisätty tiettyjä päiviä ennen kuluvaa päivää, voidaan käyttää tuote-ehdokkaiden valinnassa. Kuvan oletusarvo ehdottaa, että 180 päivää vanhempia tuotteita voi käyttää suosittujen tuotteiden luettelossa.
1. **Sisällytä myynti X päivän ajalta** - Myyntitapahtumia, jotka ovat tapahtuneet tiettyjä päiviä ennen kuluvaa päivää, voidaan käyttää tuotteiden tilaamisessa. Yllä oleva oletusarvo viittaa siihen, että kaikkia edellisten 30 päivän aikaisia tuoteostoja voidaan käyttää tuotteen sijoituksen määrittämisessä suosittujen tuotteiden luetteloa varten. 

### <a name="best-selling-product-list"></a>Myydyimpien tuotteiden luettelo

Liiketoiminnasta riippuen Myydyimmät-luettelossa voi olla eri tulokset kuin Suositut-luettelossa, vaikka molemmissa käytetään tapahtumatietoja tuotteiden järjestämiseksi. Koska myydyimmillä tuotteilla ei ole katkaisua lajittelupäivämäärän perusteella, Myydyimmät-luettelon tuotteissa voi olla hyvin suosittuja mutta vanhoja tuotteita, jotka ovat jo pudonneet suosittujen tuotteiden luettelosta. 

**Myydyimmät**-tuoteluettelossa on yksi parametri, jonka voi muuttaa:

![Esimerkki Myydyimmät-luettelon oletusparametrista](./media/examplebestsellingparameters.PNG)
1. **Sisällytä myynti X päivän ajalta** - Myyntitapahtumia, jotka ovat tapahtuneet tiettyjä päiviä ennen kuluvaa päivää, voidaan käyttää tuotteiden tilaamisessa. Yllä oleva oletusarvo viittaa siihen, että kaikkia edellisten 30 päivän aikaisia tuoteostoja voidaan käyttää tuotteen sijoituksen määrittämisessä myydyimpien tuotteiden luetteloa varten. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Tuotteiden lisääminen suositusluetteloihin tai niiden poistaminen luetteloista manuaalisesti

### <a name="for-new-trending-or-best-selling"></a>Uudet, suositut tai myydyimmät

1.  Siirry kohtaan **Retail** > **Tuotesuositukset** > **Suositusparametrit**.
1.  Valitse vähittäismyynnin jaettujen parametrien luettelossa **Suositusluettelot**.
1.  Valitse luettelon lisätyt tai poistetut tuotteet.
1.  Voit lisätä tuotteita taulukkoon valitsemalla **Lisää rivi**. 
1.  Etsi tuote Tuote-sarakkeessa **Nimi**-tai **Tuotenumero**-arvolla.
![Esimerkki tuotteen hakemisesta Uusi tuote -luettelosta](./media/examplenewlistconfiguration1.png)
1.  Valitse Rivityyppi-sarakkeesta jompikumpi seuraavista vaihtoehdoista:
    -   **Sisällytä** – Pakottaa tuotteen luettelon alkuun
    -   **Sulje pois** – Estää tuotetta näkymästä luettelossa ![Tuotteen Uusi tuote -luetteloon sisällyttämisen tai siitä poissulkemisen esimerkki](./media/examplenewlistconfiguration2.png)
1.  Jos **näyttöjärjestystä** muutetaan, **Sisällytä**-merkinnän saaneiden tuotteiden järjestys luettelossa muuttuu.
    - Jos kahdella tuotteilla on sama **näyttöjärjestyksen** arvo, näiden kahden tuloksen lopullinen järjestys voi poiketa taustasovelluksen järjestyksestä.
1.  Voit poistaa tuotteita taulukosta valitsemalla poistettavan rivin ja valitsemalla sitten **Poista**.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>Ihmiset pitävät myös- tai Ostetaan usein yhdessä -luettelot

**Ostetaan usein yhdessä**- tai **Ihmiset pitävät myös** -luetteloiden kontekstissa koneoppimista käytetään kuluttajan ostomallien analysoimisessa. Näin voidaan suositella liittyviä tuotteita, jotka ostetaan usein yhdessä yksilöllisen alkutuotteen kohdalla. 
 
**Alkutuote** on tuote, jolle haluat luoda tuloksia. Lisää tälle tuotteelle tuloksia tai poista niitä, kun haluat muokata suositusluetteloita manuaalisesti. 

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

[Ota tuotesuositukset käyttöön](enable-product-recommendations.md)

[Tuotesuositusluetteloiden lisääminen sivuille](add-reco-list-to-page.md)