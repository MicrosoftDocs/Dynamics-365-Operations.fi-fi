---
title: Ylätunnistemoduuli
description: Tässä ohjeaiheessa on tietoja ylätunnistemoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697272"
---
# <a name="header-module"></a>Ylätunnistemoduuli

[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja ylätunnistemoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.

## <a name="overview"></a>Yleiskatsaus

Ylätunnistemoduuli on erityinen säilö, jota käytetään kaikkien sivun ylätunnisteessa näkyvien moduulien isännöinnissä. Se voi sisältää esimerkiksi sivuston logon, siirtymishierarkian linkit, sivuston muiden sivujen linkit ja hakupalkin..

Ylätunnistemoduuli optimoidaan automaattisesti sitä laitetta varten, jolla sivustoa tarkastellaan (eli pöytätietokonetta tai mobiililaitetta varten). Esimerkiksi mobiililaitteessa siirtymispalkki tiivistetään **Valikko**-painikkeeksi (jossa on useita *viivoja*).

## <a name="properties-of-a-header"></a>Ylätunnisteen ominaisuudet

Ylätunnistemoduuli tukee yleisten säilöen tapaan **ylätunniste**- ja **leveys**-ominaisuuksia.

Ylätunnistemoduulissa on useita paikkoja. Paikkoja on esimerkiksi tietosanomassa, siirtymisvalikossa, logossa, hakupalkissa, ostoskorikuvakkeessa, toivomuslistakuvakkeessa ja tilin tiedoissa. Jokainen paikka tukee tiettyä moduulijoukkoa.

## <a name="modules-that-are-available-in-a-header-module"></a>Ylätunnistemoduulin käytettävissä olevat moduulit

Seuraavia moduuleja voi käyttää ylätunnistemoduulissa:

- **Siirtymisvalikko** – Siirtymisvalikko edustaa kanavan siirtymishierarkiaa ja muita staattisia siirtymislinkkejä. Kanavan siirtymishierarkia voidaan määrittää Dynamics 365 Retail -sovelluksessa. Määritetyt nimikkeet näkyvät tämän jälkeen ylätunnisteen siirtymistoiminnossa. Lisäksi voidaan määrittää staattisia siirtymislinkkejä ja suhteellisia linkkejä muille sähköisen kaupankäynnin sivuston sivuille. Ylätunniste voidaan tasata vasemmalle, oikealle tai keskelle.
- **Ostoskorikuvake** – Ostoskorikuvake on erityinen kuvake ostoskoria varten. Se näkyy ylätunnisteessa ja osoittaa ostoskorin nimikkeiden määrän. Ostoskorisivun linkin yhteydessä on oltava ostoskorikuvake, jonka avulla asiakkaat ohjataan uudelleen ostoskorisivulle kuvakkeen valitsemisen jälkeen.
- **Toivomuslistakuvake** – Toivomuslistakuvake näkyy ylätunnisteessa. Se osoittaa asiakkaan toivomuslistaan lisättyjen nimikkeiden määrän. Toivomuslistasivun linkin yhteydessä on oltava tämä kuvake. Sen avulla asiakkaat ohjataan uudelleen toivomuslistasivulle kuvakkeen valitsemisen jälkeen.
- **Sisäänkirjausmoduuli** – Sisäänkirjautumismoduuli näkyy ylätunnisteessa. Sen avulla asiakkaat voivat kirjautua sisään tilille tai rekisteröityä tilille. Jos asiakas on jo kirjautunut sisään, moduuli voidaan määrittää näyttämään linkit tilisivulle, tilaushistoriasivulle tai toiselle sivulle.
- **Logomoduuli** – Tämä moduuli näyttää logon, joka edustaa jälleenmyyjää ja tuotemerkkiä. Se on kuva, jossa on linkki. Linkki määritetään yleensä niin, että se ohjaa uudelleen aloitussivulle. Tämän vuoksi asiakkaat voivat nopeasti palata aloitussivulle miltä tahansa sivuston sivulta.
- **Hälytys** – Hälytys näkyy ylätunnisteessa. Sitä käytetään sivuston kaikkia sivuja koskevan sisäisen sanoman näyttämisessä. Hälytys voi esimerkiksi näyttää Vuosittainen alennus päättyy 2 päivän kuluttua -sanoman.
- **Hakupalkki** – Hakupalkin avulla käyttäjät voivat syöttää hakusanoja ja etsiä tuotteita. Moduulissa on määritettävä hakutulossivun URL-osoite. Kyselymerkkijonon parametri voidaan määrittää (oletusarvo on **q**). Hakupalkissa on automaattisen ehdotuksen paikka, johon automaattisen ehdotuksen moduuli lisätään.
- **Automaattinen ehdotus** – Automaattisesti ehdotetut tulokset näytetään automaattisen ehdotuksen moduulissa. Nämä tulokset voivat olla avainsanoja, tuotteita tai luokkia, joista hakusana löytyy.

## <a name="create-a-header-module"></a>Ylätunnistemoduulin luominen

Voit luoda ylätunnistemoduulin seuraavasti.

1. Luo sivun osa, jossa ylätunnistemoduuli on.
1. Lisää moduulit ylätunnistemoduulin paikkoihin.
1. Päivitä kunkin moduulin asetukset.
1. Tallenna sivun osa. 
1. Kirjaa sivu sisään ja julkaise se.

Voit varmistaa, että ylätunniste näkyy jokaisella sivulla, noudattamalla näitä ohjeita jokaisen sivustolle luodun sivumallin kohdalla.

1. Lisää oletussivun ylätunnisteen pääpaikkaan sivun osa, joka sisältää ylätunnistemoduulin.
1. Tallenna malli. 
1. Kirjaa malli sisään ja julkaise se.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)
