---
title: Suunnittelun muutostenhallinnan yleiskatsaus (sisältää videon)
description: Tässä aiheessa on yleiskatsaus suunnittelun muutostenhallintaan, jonka avulla voi suunnitella ja hallita tuotteen versiointia sekä hallita tuotteen elinkaaria ja suunnittelun muutoksia.
author: t-benebo
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d667aef827addcf7c34075b08afffffe3fd71935
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952595"
---
# <a name="engineering-change-management-overview"></a>Suunnittelun muutostenhallinnan yleiskuvaus

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Toiminnon yhteenveto

Valmistajat tarvitset nykyisin tehokasta tuotetietojen hallintaa, versionhallintaa ja suunnittelun muutoksenhallintaa, jotta ne menestyisivät jatkuvasti lyhenevistä tuotteiden elinkaaresta, kasvavista laatu- ja luotettavuusvaatimuksista sekä entistä tarkemmasta tuotteiden turvallisuustarkkailusta huolimatta.

Suunnittelun muutostenhallinta tuo rakennetta ja täsmällisyyttä tuotetietojen hallintaprosessiin sekä mahdollistaa tuotteiden hallitun määrittämisen, vapauttamisen ja korjaamiseen työnkulkujen avulla. Tuoteversioiden ja suunnittelun muutostenhallinnan ansiosta suunnittelun muutokset voidaan dokumentoida, niiden vaikutus voidaan arvioida ja ne voidaan ottaa käyttöön koko tuotteen elinkaaren ajan.

Suunnittelun muutostenhallinta auttaa suunnittelemaan ja hallitsemaan tuotteen versiointia sekä hallitsemaan tuotteen elinkaaria ja suunnittelun muutoksia. Tärkeimmät toiminnot:

- Tuotteen versiointi
- Parannettujen tuotteen vapautustoimintojen avulla voidaan ylläpitää tuotteen päätietoja yhdessä yrityksessä (suunnitteluyritys) ja julkaista täysin määritetyt vapautetut tuotteet muihin yrityksiin
- Säännöt, joilla tarkistetaan, että pakolliset tiedot on annettu ennen tuoteversion aktivointia (valmiustarkistukset)
- Parannettu tuotteen elinkaaren hallinta valvomalla tarkasti, milloin vapautettua tuotetta voidaan käyttää tietyissä liiketoimintaprosesseissa
- Työnkulkujen tukemat suunnittelun muutospyynnöt
- Työnkulkujen tukemat suunnittelun muutostilaukset

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Edellä oleva video ([Dynamics 365 Supply Chain Managementin muutostenhallinnan ominaisuudet](https://youtu.be/N313FqvRuBc)) sisältyy [Finance and Operations -toistoluetteloon](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on saatavana YouTubessa.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Järjestelmän suunnittelun muutostenhallinnan ominaisuuksien ottaminen käyttöön

Ennen kuin voit käyttää suunnittelun muutostenhallintaa, sinun on otettava käyttöön sekä *Suunnittelun muutostenhallinta* -toiminto että sen määritysavain. Jos haluat seurata myös tapahtumien versiodimensiota (valinnainen), sinun on otettava käyttöön sekä *Tuoteversion dimensio* -toiminto että sen määritysavain. Kun nämä edellytykset on määritetty vaaditulla tavalla, voit ottaa käyttöön lisäominaisuuksia suunnittelun muutostenhallintaa varten.

### <a name="turn-on-the-basic-engineering-change-management-features"></a>Suunnittelun muutostenhallinnan perusominaisuuksien ottaminen käyttöön

Ota toiminnot ensin käyttöön seuraavasti.

1. Valitse [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtila.
1. Tarkista päivitysten saatavuus.
1. Ota käyttöön *Suunnittelun muutostenhallinta* -niminen toiminto.
1. Jos haluat käyttää sitä, sinun on otettava käyttöön myös *Tuotteen dimensioversio* -niminen toiminto.

### <a name="turn-on-the-required-configuration-keys"></a>Vaadittujen määritysavainten käyttöönotto

Ota seuraavaksi määritysavaimet käyttöön seuraavia vaiheita noudattamalla.

1. Siirrä järjestelmä ylläpitotilaan kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.
1. Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**.
1. **Kauppa**-solmun laajentaminen.
1. Ota pääominaisuuden määritysavain käyttöön valitsemalla **Suunnittelun muutostenhallinta** -valintaruutu.
1. Laajenna **Tekninen suunnittelun muutoksenhallinta** -solmu ja valitse tarpeen mukaan seuraavat valintaruudut tai poista niiden valinta (käytettävien ominaisuuksien mukaan):

    - **Määritteen haku** – Valitsemalla tämän valintaruudun voit ottaa [määritteen hakutoiminnon](engineering-attributes-and-search.md) käyttöön. On suositeltavaa ottaa tämä toiminto käyttöön, mutta voit poistaa valintaruudun valinnan, jos et käytä sitä.
    - **Prosessivalmistuksen muutoksenhallinta** – Valitse tämä valintaruutu, jos haluat hallita prosessivalmistuksen kaavojen muutoksia suunnittelumuutoksen hallintaominaisuuksien avulla. Jos kaavojen hallintaa ei tarvitse tehdä, tämän valintaruudun voi poistaa. Lisätietoja on kohdassa [Kaavojen ja niiden osien muutosten hallinta](manage-formula-changes.md).

1. Jos haluat myös käyttää versiodimensiota, valitse myös **Tuotedimensio – Versio** -valintaruutu. (Tämä valintaruutu on luettelossa alempana, ei **Suunnittelun muutoshallinta** -solmussa.)
1. Poista järjestelmän ylläpitotila käytöstä kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.
1. Suorita tietokantasynkronointi, kun haluat varmistaa, että määritysavaimet ovat oikein käytössä.

> [!IMPORTANT]
> Huhtikuussa 2022 alkaen sekä **Suunnittelun muutostenhallinta**- että **Tuotedimensio - Versio** -lisenssiavaimet ovat oletusarvon mukaan käytössä kaikissa uusissa asennuksissa, mutta ne voidaan tarvittaessa poistaa käytöstä.

### <a name="turn-on-additional-engineering-change-management-features"></a>Suunnittelun muutostenhallinnan lisäominaisuuksien ottaminen käyttöön

Kun olet ottanut suunnittelun muutostenhallinnan perusominaisuudet ja niiden määritysavaimet käyttöön, ominaisuuksien hallintaan lisätään useita suunnittelun muutostenhallinnan lisäominaisuuksia ja valinnaisia ominaisuuksia. Kaikki nämä ominaisuudet on lueteltu **Suunnittelun muutostenhallinta** -moduulissa. Seuraavassa taulukossa kuvataan kaikki lisäominaisuudet ja annetaan linkkejä lisätietoihin.

| Ominaisuuden nimi ominaisuuksienhallinnassa | kuvaus |
|---|---|
| Aiemmin luotujen tuotteiden muutostenhallinnan ottaminen käyttöön | <p>Tämän ominaisuuden avulla voit muuntaa olemassa olevia tuotteita suunnittelutuotteiksi, jotta voit alkaa hallita niitä käyttäen suunnittelun muutostenhallintaa.</p><p>Lisätietoja: [Ota olemassa olevien tuotteiden muutostenhallinta käyttöön](change-management-existing-products.md).</p> |
| Suunnittelun ilmoitukset tuotannolle | <p>Kun tuotetta muutetaan suunnittelussa, voi olla tärkeää ilmoittaa muutoksista tuotantoon. Tällöin tuotantotyöntekijät voivat ryhtyä asianmukaisiin toimenpiteisiin, kuten komponenttien korvaamiseen, tuoterakenteen korvaamiseen tai reitityksen korvaamiseen. Tämän ominaisuuden avulla voit ilmoittaa tuotantoon tuotettavien tuotteiden muutoksista.</p><p>Lisätietoja on kohdassa [Suunnittelutuotteiden muutosten hallinta](engineering-change-management.md).</p> |
| Parannettu suunnittelun muutostenhallinnan määritteiden periytyvyys | <p>Tämä ominaisuus yksinkertaistaa valmiiden tuotteiden tai välinimikkeiden määritteiden hallintaa. Kun tämä ominaisuus on käytössä, on helpompi tunnistaa kaikki nimikkeelle kuuluvat määritteet. Voit myös valita määritteet, jotka välitetään kyseiseltä nimikkeeltä päänimikkeelle. Tämä ominaisuus on hyödyllinen esimerkiksi silloin, kun jokin valmiin tuotteen komponentti on särkyvä, myrkyllinen tai helposti syttyvä, koska voit helposti tunnistaa särkyvän, myrkyllisen tai helposti syttyvän määritteen ja välittää sen valmiiseen tuotteeseen.</p><p>Lisätietoja: [Suunnittelumääritteet ja suunnittelumääritteiden haku](engineering-attributes-and-search.md).</p> |
| Tuotteen valmiustarkistukset | <p>Tämän toiminon avulla voit määrittää vakiotuotteille (ei suunniteltu) suoritettavia valmiustarkistuksia. Tuotteiden valmiustarkistusten avulla voit varmistaa, että kukin tuote on täydellisesti määritetty ja että kaikki tarvittavat käytännöt on määritetty, ennen kuin tuote otetaan käyttöön ja sitä käytetään tapahtumissa. Jos poistat tämän ominaisuuden käytöstä, kun olet käyttänyt sitä jonkin aikaa, kaikki vakiotuotteiden valmiustarkistukset poistetaan.</p><p>Lisätietoja on kohdassa [Tuotteen valmius](product-readiness.md).</p> |
| Hallitse kaavojen ja niiden ainesosien muutoksia | <p>Tämän ominaisuuden avulla voit seurata muutoksia reseptin ainesosiin, oheistuotteisiin ja sivutuotteisiin.</p><p>Lisätietoja on kohdassa [Kaavojen ja niiden osien muutosten hallinta](manage-formula-changes.md).</p> |
| Muuttujien luominen suunnittelun tuotteille | <p>Tämän ominaisuuden avulla voit luoda suunnittelutuotteiden muuttuja käytettävissä olevien dimensioarvojen perusteella.</p><p>Lisätietoja [Versioiden luominen suunnittelutuotteista](engineering-variants.md).</p> |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
