---
title: Dynamics 365 Supply Chain Management -asiakasportaalin yleiskuvaus (sisältää videon)
description: Tässä artikkelissa esitellään asiakasportaali ja selitetään, kenen tulisi käyttää sitä ja miten se toimii.
author: Henrikan
ms.date: 06/16/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ff074e62489fe74f0c2de6dae0e02d1da7e7f6ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901905"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>Asiakasportaali Dynamics 365 Supply Chain Managementin yhteenvedoksi

[!include [banner](../includes/banner.md)]


## <a name="what-is-the-customer-portal"></a>Mikä on asiakasportaali?

Nykyaikaiset toimitusketjujärjestelmät perustuvat integrointiin. Ne edellyttävät, että varasto, asiakkaiden kysyntä ja myyntiosastot yhdistetään sen sijaan, että ne olisivat erillisissä siiloissa. Asiakasportaali auttaa Microsoft Dynamics 365 Supply Chain Management -organisaatioita tehostamaan tätä integrointia ja pitämään asiakkaat ajan tasalla.

Asiakasportaali on [Power Apps -portaalien](/powerapps/maker/portals/overview) malli, jonka avulla yritykset voivat luoda ulkoisesti yritysten välisten (B2B) Internet-sivuston myyntitilausten käsittelyyn liittyviin tilanteisiin. Mallissa käytetään [kaksoiskirjoittamista](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md), Supply Chain Managementia ja Power Apps -portaaleja, joiden avulla ulkoiset yritysasiakkaat voivat tarkastella ja luoda tietoja yrityksen Dynamics 365 -ympäristöstä.

Asiakasportaalimallissa on kaikki mukautustoiminnot, joita Power Appsin portaaliominaisuus tarjoaa. Mallia voidaan helposti muokata siten, että se edustaa yrityksen brändiä, lisää toimintojen lisäämistä ja muuttaa käyttökokemusta. Kaikkia toimintoja, jotka malli tarjoaa valmiina, voidaan muokata halutulla tavalla.

> [!IMPORTANT]
> Mallin ei odoteta olevan täysin toimintakykyinen. Se vain toimii mahdollistajana asiakkaille, jotka haluavat luoda ulkopuolisen sivuston, jotta yritysasiakkaat voivat sitoutua Supply Chain Managementista saataviin tietoihin.

> [!NOTE]
> Asiakasportaalin dokumentaatio on suunnattu järjestelmänvalvojille, mukauttajille ja järjestelmäintegraattoreille, jotka määrittävät asiakasportaalin Supply Chain Managementin asennusta varten. Se käyttää termejä _asiakas_ ja _käyttäjä_ kuvaamaan ihmisiä, jotka ovat asiakkaita organisaatiossa, joka käyttää Supply Chain Managementia ja joka käyttää lopullista portaalia itse.

## <a name="video"></a>Video

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

[Yleiskatsaus Dynamics 365 Supply Chain Managementin asiakasportaalimallista](https://youtu.be/nPrqoLuHfV8) -video (edellä) sisältyy [taloushallinnon ja toimintojen sovellusten toistoluetteloon](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on saatavana YouTubessa.

## <a name="who-should-use-it"></a>Kenen pitäisi käyttää sitä?

Asiakasportaali on suunniteltu yrityksille, jotka käyttävät Supply Chain Managementia ja joilla on seuraavat ominaisuudet:

- He haluavat rakentaa ulkoisen sivuston, joka kommunikoi tilauksen käsittelytietojen (kuten tilauksen tila tai tilitiedot) suoraan heidän Supply Chain Management -järjestelmästään heidän yritysasiakkailleen.
- He ovat siirtymässä Dynamics AX 2012:sta Supply Chain Managementiin ja aiemmin käyttivät [AX 2012 Asiakkaan itsepalveluportaalia](/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).

Seuraavat organisaatiotyypit **eivät** ole hyviä ehdokkaita asiakasportaalin käyttöönottoon:

- Yritykset, jotka haluavat luoda verkkosivuston muille kuin yritysasiakkaille. Näiden yritysten tulisi harkita [Dynamics 365 Commerce -verkkokaupan verkkosivuston](../../commerce/create-ecommerce-site.md) luomista.
- Yritykset, jotka käyttävät jo aiemmin luotuja Power Apps -portaaliverkkosivustoja samaan tarkoitukseen. Nämä yritykset eivät saa lisäetuja asiakasportaalista. Asiakasportaali toimitetaan mallina, joka toimii oppaana ja lähtöpisteenä asiakkaille, jotka haluavat yhdistää pisteet kaksoiskirjoituksen, Supply Chain Managementin ja Power Apps -portaalien välillä. Jos olet jo määrittänyt verkkosivuston, joka palvelee tätä tarkoitusta, et ehkä saa paljonkaan arvoa käyttämällä asiakasportaalin mallipohjaa sivuston uudelleentarjoamiseen.

## <a name="how-does-it-work"></a>Miten se toimii?

Asiakasportaali toimitetaan Power Apps -portaalien mallina. Se on riippuvainen Power Apps -portaaleista ja kaksoiskirjoituksesta.

[Power Apps -portaalit](/powerapps/maker/portals/overview) on ominaisuus, jonka avulla käyttäjät voivat luoda ulkoisen sivuston, johon organisaation ulkopuolelta tulevat henkilöt voisivat kirjautua. Portaalien tekemiseen tarvitaan vain vähän koodausta. Asiakasportaali on yksi monista Microsoftin käytettävissä olevista [Dynamics 365 -portaalin malleista](/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365).

[Kaksoiskirjoitus](/powerapps/maker/portals/overview) on valmis infrastruktuurituote, joka sisältää lähes reaaliaikaisen vuorovaikutuksen asiakkaiden aktivointisovellusten ja taloushallinnon ja toimintojen sovellusten välillä. Kaksoiskirjoitus sisältää kaksisuuntaisen integroinnin taloushallinnon ja toimintojen sovellusten ja Microsoft Dataversen välillä. Tästä syystä tietovirta tarjoaa integroidun käyttökokemuksen eri sovelluksissa. Asiakasportaali määräytyy niiden taulukoiden mukaan, jotka on synkronoitu kaksoiskirjoituksella. Ennen kuin Supply Chain Managementin tiedot voidaan tuoda esiin asiakasportaalissa, kaksoiskirjoitus on otettava käyttöön kaikissa soveltuvissa taulukoissa.

![Asiakasportaalin riippuvuudet.](media/customer-portal-elements.png "Asiakasportaalin riippuvuudet")

Asiakasportaali toimii lähtökohtana organisaatioille, jotka haluavat käyttää Power Apps -portaaleja, joiden on tarkoitus muodostaa ulkoinen verkkosivusto, joka käyttää Supply Chain Managementin asennuksen tietoja. Sen avulla organisaatiot voivat yhdistää kaksoiskirjoituksen, Supply Chain Managementin ja Power Apps -portaalit.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]