---
title: Tuotetietosivujen yleiskatsaus
description: Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen tuotetietosivujen (PDP:t) yleiskatsaus.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697862"
---
# <a name="overview-of-product-details-pages"></a>Tuotetietosivujen yleiskatsaus

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen tuotetietosivujen (PDP:t) yleiskatsaus.

## <a name="overview"></a>Yleiskatsaus

PDP-sivulla on tuotteen eritellyt tiedot. Sen avulla asiakkaat voivat valita tuotevaihtoehtoja, kuten koon, tyylin ja värin. PDP-sivulla on oltava kaikki tuotteen tiedot, joita asiakas tarvitsee ostopäätöksen tekemiseen.

Seuraavassa kuvassa on esimerkki PDP-sivusta.

![Esimerkki tuotetietosivusta](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Ylä- ja alatunnistemoduulit

PDP-sivun yläosassa on ylätunniste, joka sisältää kaikki tuoteluokat ja muut sivut, joita jälleenmyyjä haluaa asiakkaiden selaavan. Sivun alaosassa on alatunniste, joka sisältää pikalinkkejä erilaisiin asiakasta mahdollisesti kiinnostaviin aiheisiin.

## <a name="buy-box-module"></a>Ostoruutumoduuli

PDP-sivun tärkein moduuli on ostoruutumoduuli. Siksi se on sivun pääosan ensimmäinen nimike. Ostoruutumoduuli on säilömoduuli. Se isännöi useita moduuleja, jotka sisältävät tuotetta koskevia tärkeitä tietoja. Näitä tietoja ovat esimerkiksi tuotteen nimi, tuotteen kuvat, kuvaus, hinta ja tuoteluokitukset.

Ostoruutumoduulin avulla asiakas voi valita tuotevaihtoehtoja (esimerkiksi koon, tyylin ja värin) ja lisätä tuotteen ostoskoriin. Sen avulla asiakas voi myös ostaa tuotteen verkosta ja noutaa sen myymälästä. Osta verkosta ja nouda myymälästä -moduulissa käytetään Bing Maps -ohjelmointirajapintojen integrointia. Sen avulla etsitään lähellä olevat myymälät tai asiakkaan määrittämässä sijainnissa olevat myymälät.

Ostoruutumoduuli vaatiin tuotteen tunnuksen. Tämä tunnus johdetaan sivun kontekstista. Jos ostoruutumoduuli lisätään sivulle, jossa sivun konteksti ei sisällä tuotteen tunnusta, se ei hahmonna tietoja oikein.

## <a name="product-specifications-module"></a>Tuotemääritysten moduuli

Tuotemääritysten moduulia voi käyttää tuotteen lisätietojen näyttämisessä. Nämä tiedot haetaan Dynamics 365 Retail -sovelluksen tuotemääritteistä. Tuotemääritysten moduulissa näytetään kaikki määritteet, joiden **käytettävissä**-ominaisuuden arvoksi on määritetty **Tosi**. Tuotemääritysten hakeminen vaatii tuotteen tunnuksen.

## <a name="recommendations-module"></a>Suositusten moduuli

Suositusten moduuli on tärkeä moduuli PDP-sivulla. Kun asiakkaat selaavat tuotteita, heille kannattaa esittää useita tuotevaihtoehtoja. Näin he voivat löytää oikean tuotteen ja ostaa sen. Suositusten avulla asiakkaat löytävät helposti liittyvän sisällön ja jatkavat ostosten tekemistä.

Käytettävissä on erityyppisiä suositusluetteloita:

- **Ihmiset pitävät myös** -luettelo perustuu koneoppimiseen. Se käyttää muiden asiakkaiden tapahtumahistoriaa suositusten antamiseen. Tämä luettelo on luotu suositusten palvelun avulla. Se muistuttaa Asiakkaat, jotka ostivat tämän, ostivat myös... -luetteloa. Tämän luettelon luomiseen tarvitaan tuotteen tunnus.
- Retailin tuotteelle voidaan määrittää **Liittyvät**-luettelo. Esimerkiksi ruskealle nahkaiselle matkustusta varten tehdylle käsilaukulle voidaan määrittää Liittyvät-luettelo, joka sisältää nahkaisia tai matkustusta varten suunniteltuja käsilaukkuja. Retailissa voidaan määrittää myös muun tyyppisiä Liittyvät-luetteloita, kuten **Lisävarusteet** ja **Lisää samanlaisia**. Tämän luettelon luomiseen tarvitaan tuotteen tunnus. Jos tämä lisätään aloitussivulle, jossa sivun konteksti ei sisällä tuotteen tunnusta, luettelo on tyhjä.
- PDP-sivuilla voi käyttää algoritmien avulla luotuja suositusluetteloita, kuten **Suositut**, **Myydyimmät** ja **Uudet**. Vaikka nämä luettelot eivät välttämättä liity suoraan PDP-sivulla olevaan tuotteeseen, asiakkaat voivat etsiä niiden avulla heitä mahdollisesti kiinnostavia tuotteita. Tämäntyyppiset luettelot eivät edellytä tuotteen tunnusta. Nämä ovat yleisiä luetteloita, joita luodaan ostokäyttäytymisen mukaan sivustossa.
- Toimitukselliset luettelot ovat manuaalisesti kuratoituja luetteloita. Jälleenmyyjä voi esimerkiksi päättää manuaalisesti luetteloiden sisältämät tuotteet.

## <a name="ratings-and-reviews-module"></a>Luokitusten ja arvosteluiden moduuli

Luokitukset ja arvostelut -moduulissa näkyvät muiden asiakkaiden antamat luokitukset ja arvostelut. Sen avulla asiakas voi myös kirjoittaa tuotteesta oman arvostelun. Lisäksi se sisältää histogrammin, joka ilmaisee tuotteen luokitusten kehityksen. Lisätietoja on kohdassa [Luokitusten ja arvostelujen yleiskuvaus](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Markkinointimoduulit

Jos markkinointisisältö koskee vain tiettyä tuotetta, mikä tahansa markkinointimoduuli voidaan lisätä PDP-sivulle. Voit lisätä markkinointimoduuleja PDP-sivulla täydentämällä sivua. 

## <a name="additional-resources"></a>Lisäresurssit

[Aloitussivun yleiskatsaus](quick-tour-home-page.md)

[Luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus](category-search-page-overview.md)

[Ostoskorin ja maksusivun yleiskatsaus](quick-tour-cart-checkout.md)

[Tilinhallintasivujen yleiskatsaus](quick-tour-account-management.md)
