---
title: Tilin hallintasivut ja -moduulit
description: Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Commercen tilienhallintasivuista ja -moduuleista.
author: v-chgri
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 2db9a1218802234297e9d027691e5887d6a5c808
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274452"
---
# <a name="account-management-pages-and-modules"></a>Tilin hallintasivut ja -moduulit

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Commercen tilienhallintasivuista ja -moduuleista.

Tilien hallinta viittaa sivuryhmään, jota käytetään Dynamics 365 Commercen käyttäjän tileihin liittyvien tietojen hallinnassa. Tilinhallinnan sivut sisältävät tilinhallinnan saapumissivun, käyttäjäprofiilisivun, käyttäjän osoitteen sivun, tilaushistoriasivun, tilaustietojen sivun, kanta-asiakkuussivun ja toivomusluettelosivun.

### <a name="account-management-landing-page"></a>Tilinhallinnan saapumissivu

Tilihallinnan saapumissivulla käytetään seuraavia moduuleja:

- **Säilö** – kaikki tilinhallinnan saapumissivumoduulit on sijoitettava säilöön. 
- **Tilin tervetuloruutu** – Tämä moduuli sisältää tervetulosanoman tilinhallinnan sivulla. Se sisältää otsikon ominaisuudet.
- **Tilin yleinen ruutu** – Tämän moduulin avulla saadaan otsikot ja linkit tilinhallintasivuille, kuten Tilaushistoria- ja Oma profiili -sivuille. Yleinen ruutumoduulin avulla voidaan määrittää minkä tahansa sivun ruutu. Fabrikamissa tätä moduulia käytetään Tilaushistoria- ja Oma profiili -sivulinkeissä tilinhallinnan saapumissivulla.
- **Toivelistaruutu** – Tämän moduulin avulla määritetään asiakkaan toivelistan nimikkeiden yhteenveto. Se voi esimerkiksi ilmoittaa, että toivomuslistassa on 10 nimikettä. Se sisältää otsikon ja Näytä tiedot -linkin. Näytä tiedot -linkki on määritettävä niin, että se ohjaa uudelleen toivelistasivulle. 
- **Tilin osoiteruutu** – Tätä moduulia käytetään käyttäjän osoitteiden yhteenvedon määrityksessä. Siinä voi lukea esimerkiksi seuraava teksti: Tilillesi on lisätty 2 osoitetta. Se sisältää otsikon ja Näytä tiedot -linkin. Näytä tietojen -linkki on määritettävä niin, että se ohjaa uudelleen käyttäjän osoitesivulle.
- **Tilin kanta-asiakasruutu** – Tämän moduulin avulla näytetään ja linkitetään kanta-asiakasohjelman tiedot. Tässä ruudussa on kakis tilaa: toinen tila näyttää linkin kanta-asiakasohjelmaan liittymiseen, jos käyttäjä ei ole vielä jäsen. Toinen tila näyttää linkit kanta-asiakastietojen sivulle, kun käyttäjä on jo jäsen. Ominaisuuksia ovat otsikko, Rekisteröidy-linkki ja Näytä kanta-asiakkuus -linkki. Näytä kanta-asiakkuus -linkki on määritettävä niin, että se ohjaa uudelleen kanta-asiakkuussivulle. Rekisteröidy-linkki on määritettävä niin, että se ohjaa sivulle, jossa käyttäjät voivat liittyä kanta-asiakasohjelmaan. 

### <a name="order-history-page"></a>Tilaushistoriasivu

Tilaushistoriasivulla näkyvät kaikki käyttäjän asettamat viimeaikaiset tilaukset tilaushistoriamoduulissa.

### <a name="order-details-page"></a>Tilauksen tietojen sivu

Tilaustietojen sivulla on eriteltyjä tietoja jokaisesta tilauksesta. Sitä voi käyttää tilaushistoriasivulta. Se käyttää tilaustietojen moduulia, jossa edellytetään myynnin tai tapahtuman tunnusta tilaustietojen noutamiseksi.

### <a name="my-profile-page"></a>Oma profiili -sivu

Oma profiili -sivulla näkyvät käyttäjän tiliprofiilin tiedot käyttämällä tiliprofiilimoduulia. Sivulla näkyy käyttäjän tiliin liitetty sähköpostiosoite sekä tilille määritetyt asetukset. Jos määrität mukautettuja asiakkaan määritteitä, nämä määritteet näkyvät myös Lisätiedot-osassa. Käyttäjät voivat muokata nimeään, asetuksiaan tai lisätietojaan (jos käytettävissä).

### <a name="user-address-page"></a>Käyttäjän osoitteen sivu

Käyttäjän osoitteen sivulla on niiden osoitteiden luettelo, jotka on liitetty käyttäjätiliin. Käyttäjä on antanut nämä osoitteet kassatoiminnon aikana tai lisännyt ne suoraan tälle sivulle. Käyttäjän osoitteen moduulia käytetään osoitteiden lisäämiseen ja muokkaamiseen, ensisijaisen osoitteen määrittämiseen ja sivun olemassa olevien osoitteiden hahmontamiseen.

### <a name="wish-list-page"></a>Toivomuslistasivu

Toivomuslistasivulla ovat nimikkeet, jotka on lisätty asiakkaan toivomuslistaan. Se käyttää toivomuslistamoduulia toivomuslistan nimikkeiden hahmontamiseen.

### <a name="loyalty-page"></a>Kanta-asiakassivu

Kanta-asiakkuussivulla asiakkaat voivat tarkastella omia kanta-asiakastietojaan, jos he ovat jo kanta-asiakasohjelman jäseniä. He voivat myös tarkastella pisteitä, jotka he ovat ansainneet ja lunastaneet edellisten tapahtumien aikana. Sivu käyttää kanta-asiakastietomoduulia näyttämään kanta-asiakastiedot. 

Kanta-asiakasohjelmaan liittymistä varten voidaan luoda markkinointisivu, jossa on kanta-asiakkaiden rekisteröitymisen ja kanta-asiakkuuden ehtojen moduulit. Jos käyttäjä ei ole kanta-asiakasohjelman jäsen, käyttäjä voi rekisteröityä näiden moduulien avulla.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[Kassamoduuli](add-checkout-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
