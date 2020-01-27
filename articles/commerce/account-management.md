---
title: Tilinhallinnan sivut ja moduulit
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commercen tilienhallintasivuista ja -moduuleista.
author: v-chgri
manager: annbe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885806"
---
# <a name="account-management-pages-and-modules"></a>Tilinhallinnan sivut ja moduulit

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commercen tilienhallintasivuista ja -moduuleista.

## <a name="overview"></a>Yleiskatsaus

Tilien hallinta viittaa sivuryhmään, jota käytetään Dynamics 365 Commercen käyttäjän tileihin liittyvien tietojen hallinnassa. Tilinhallinnan sivut sisältävät tilinhallinnan saapumissivun, käyttäjäprofiilisivun, käyttäjän osoitteen sivun, tilaushistoriasivun, tilaustietojen sivun, kanta-asiakkuussivun ja toivomusluettelosivun.

### <a name="account-management-landing-page"></a>Tilinhallinnan saapumissivu

Tilihallinnan saapumissivulla käytetään seuraavia moduuleja:

- **Sisällönsijoittelu** – Tämä moduuli on säilömoduuli, joka sisältää kaikki moduulit tilinhallinnan saapumissivulla.
- **Tilin tervetulonimike** – Tämä moduuli sisältää tervetulosanoman tilinhallinnan sivulla. Se sisältää ylätunnisteen ja ruudun koon ominaisuudet. **Ruudun koko** -ominaisuus määrittää moduulin leveyden sisällönsijoittelumoduulissa. Arvot vaihtelevat välillä **1**–**12**, jossa **12** edustaa sisällönsijoitussäilön täyttä leveyttä.
- **Tilin tilauksen sijoittelunimike** – Tämän moduulin avulla voit määrittää yhteenvedon käyttäjätilin tekemistä tilauksista. Se sisältää ylätunnisteen ja ruudun koon ominaisuudet sekä näkymän tietojen linkin. Näkymän tietojen linkki on määritettävä niin, että se ohjaa uudelleen tilaushistoriasivulle.
- **Tiliprofiilin sijoittelunimike** – Tätä moduulia käytetään käyttäjäprofiilin yhteenvedon määrityksessä. Se sisältää ylätunnisteen ja ruudun koon ominaisuudet sekä näkymän tietojen linkin. Näkymän tietojen linkki on määritettävä niin, että se ohjaa uudelleen käyttäjäprofiilisivulle.
- **Toivomuslistan nimike** – Tämän moduulin avulla määritetään asiakkaan toivomuslistan nimikkeiden yhteenveto. Se voi esimerkiksi ilmoittaa, että toivomuslistassa on 10 nimikettä. Se sisältää ylätunnisteen ja ruudun koon ominaisuudet sekä näkymän tietojen linkin. Näkymän tietojen linkki on määritettävä niin, että se ohjaa uudelleen toivomuslistasivulle.
- **Tilin osoitteen nimike** – Tätä moduulia käytetään käyttäjän osoitteiden yhteenvedon määrityksessä. Siinä voi lukea esimerkiksi seuraava teksti: Tilillesi on lisätty 2 osoitetta. Se sisältää ylätunnisteen ja ruudun koon ominaisuudet sekä näkymän tietojen linkin. Näkymän tietojen linkki on määritettävä niin, että se ohjaa uudelleen käyttäjän osoitteen sivulle.
- **Tilin kanta-asiakasnimike** – Tämän moduulin avulla näytetään ja linkitetään kanta-asiakasohjelman tiedot. Se sisältää ylätunnisteen ja ruudun koon ominaisuudet, näkymän tietojen linkin ja Liity jäseneksi -linkin. Näkymän tietojen linkki on määritettävä niin, että se ohjaa uudelleen kanta-asiakkuussivulle. Liity jäseneksi -linkki on määritettävä niin, että se ohjaa sivulle, jossa käyttäjät voivat liittyä kanta-asiakasohjelmaan.

### <a name="order-history-page"></a>Tilaushistoriasivu

Tilaushistoriasivulla näkyvät kaikki käyttäjän asettamat viimeaikaiset tilaukset tilaushistoriamoduulissa.

### <a name="order-details-page"></a>Tilauksen tietojen sivu

Tilaustietojen sivulla on eriteltyjä tietoja jokaisesta tilauksesta. Sitä voi käyttää tilaushistoriasivulta. Se käyttää tilaustietojen moduulia, jossa edellytetään myynnin tai tapahtuman tunnusta tilaustietojen noutamiseksi.

### <a name="user-profile-page"></a>Käyttäjäprofiilisivu

Käyttäjäprofiilisivulla näkyvät käyttäjätilin tiedot, kuten käyttäjän nimi ja sähköpostiosoite. Se käyttää käyttäjäprofiilimoduulia. Vaikka sähköpostiosoitetta ei voi poistaa, sitä voi muokata. Käyttäjäprofiilisivulla näkyvät myös käyttäjäasetukset, joiden avulla käyttäjä voi halutessaan valita tiettyjä ominaisuuksia, kuten suositusluetteloiden mukauttamisen, tai poistaa ne käytöstä. 

### <a name="user-address-page"></a>Käyttäjän osoitteen sivu

Käyttäjän osoitteen sivulla on niiden osoitteiden luettelo, jotka on liitetty käyttäjätiliin. Käyttäjä on antanut nämä osoitteet kassatoiminnon aikana tai lisännyt ne suoraan tälle sivulle. Käyttäjän osoitteen moduulia käytetään osoitteiden lisäämiseen ja muokkaamiseen, ensisijaisen osoitteen määrittämiseen ja sivun olemassa olevien osoitteiden hahmontamiseen.

### <a name="wish-list-page"></a>Toivomuslistasivu

Toivomuslistasivulla ovat nimikkeet, jotka on lisätty asiakkaan toivomuslistaan. Se käyttää toivomuslistamoduulia toivomuslistan nimikkeiden hahmontamiseen.

### <a name="loyalty-page"></a>Kanta-asiakassivu

Kanta-asiakkuussivulla asiakkaat voivat liittyä kanta-asiakasohjelmaan. Jos he ovat jo kanta-asiakasohjelman jäseniä, he voivat katsella omia tietojaan. He voivat myös tarkastella pisteitä, jotka he ovat ansainneet ja lunastaneet edellisten tapahtumien aikana.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)
