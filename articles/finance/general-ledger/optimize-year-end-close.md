---
title: Optimoi tilikauden lopetus
description: Tässä artikkelissa kerrotaan Optimoi tilikauden lopetus -palvelun lisäosasta, joka on käytettävissä kirjanpidon tilivuoden sulkemisprosessille.
author: moaamer
ms.date: 11/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2022-11-28
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 41d0c2975341cf3d612cc36be348326e24e94f1b
ms.sourcegitcommit: 707957bb7bcd98faf2600eff1c98067901a0fb73
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750007"
---
# <a name="optimize-year-end-close"></a>Optimoi tilikauden lopetus

Microsoft Dynamics 365 Financelle tarkoitettu Optimoi tilikauden lopetus -palvelun lisäosa mahdollistaa tilikauden sulkemisprosessin suorittamisen Dynamics 365 Finance -resurssien Application Object Server (AOS) -esiintymän ulkopuolella. Se käyttää mikropalveluteknologiaa. Optimoi tilikauden lopetus -ominaisuuteen liittyviä etuja ovat esimerkiksi suorituskyvyn parantuminen ja vähäinen vaikutus SQL-tietokantaan tilikauden lopetusprosessin aikana.

Sinun täytyy suorittaa seuraavat tehtävät käyttääksesi Optimoi tilikauden lopetus -ominaisuutta:

1. Asenna Optimoi tilikauden lopetus -palvelun lisäosa Microsoft Dynamics Lifecycle Service -projektistasi.
2. Ota **Optimoi tilikauden lopetus** -ominaisuus käyttöön ominaisuuksien hallinnasta.

> [!NOTE]
> Voit edelleen käyttää Financen tämänhetkistä tilikauden lopetustoimintoa poistamalla **Optimoi tilikauden lopetus** -ominaisuuden käytöstä ominaisuuksien hallinnasta.

## <a name="improved-performance"></a>Parantunut suorituskyky

**Optimoi tilikauden lopetus** -ominaisuus on suunniteltu nopeuttamaan tilikauden lopetusprosessia erityisesti asiakkaille, joilla on suuria määriä tietoja. Kun tilikauden lopetus suoritetaan palvelussa, raskasta käsittelyä tasapainotetaan pois Finance-resursseista, jotta käsittelyaikaa voidaan lyhentää ja jotta voidaan vapauttaa resursseja, jotka saattavat vaikuttaa muiden käyttäjien päivittäisiin toimiin.

**Optimoi tilikauden lopetus** -ominaisuus voi auttaa sinua saavuttamaan seuraavat tavoitteet:

- Paranna tilikauden lopetuksen suorituskykyä lyhentämällä suoritusaikaa.
- Vähennä vaikutusta muihin prosesseihin tilikauden lopetuksen suorittamisen aikana.
- Paranna tilinpäätöksen raportointia ja oikaisuja, koska tilikauden lopetuksen suorittaminen kestää vähemmän aikaa.

## <a name="new-options-and-visibility"></a>Uudet vaihtoehdot ja näkyvyys

Kun **Optimoi tilikauden lopetus** -ominaisuus käytössä, seuraaviin paikkoihin lisätään kaksi uutta saraketta, **Tulokset** ja **Tila**:

- **Tilinpäätös**-sivulle
- **Tilikauden lopetustulokset** -valintaikkunaan
- **Tilinpäätösmalli**-sivun **Taseen taloushallinnon dimensioiden siirto** -vaihtoehtoihin

Seuraavassa kuvassa on esimerkki **Tilinpäätös**-sivun **Tulokset**- ja **Tila**-sarakkeista . Voit valita **Tulokset**-sarakkeesta **Näytä tulokset** -linkin avataksesi tilinpäätöksen tulokset. **Tila**-sarake näyttää tilikauden lopetusprosessin tämänhetkisen tilan. Näin ollen uudet sarakkeet näyttävät tietoja tilikauden sulkemisprosessin edistymisestä.

[![Tilinpäätös-sivun Tulokset- ja Tila-sarakkeet.](./media/Yearendclose.jpg)](./media/Yearendclose.jpg)

Lisäksi, kun **Optimoi tilikauden sulkeminen** -ominaisuus otetaan käyttöön, **Taseen taloushallinnon dimensiot** -pikavälilehti tulee käyttöön **Tilinpäätösmalli**-sivulle. Voit käyttää tätä pikavälilehteä määrittääksesi taseen taloushallinnon dimensiot yksityiskohtaisesti tehdessäsi tilinpäätöstä. Tämä ominaisuus vastaa tulostileille jo käytettävissä olevaa ominaisuutta.

## <a name="architecture-and-data-flow"></a>Arkkitehtuuri ja tiedonkulku

Jos haluat käyttää **Optimoi tilikauden lopetus** -ominaisuutta ja suorittaa tilinpäätöksen mikropalvelussa, sinun täytyy asentaa Optimoi tilikauden lopetus -palvelun lisäosa Lifecycle Services -portaalista ja ottaa sitten **Optimoi tilikauden lopetus** -ominaisuus käyttöön ominaisuuksien hallinnasta.

Kuten seuraavassa kuvassa näkyy, tilikauden lopetusprosessi vahvistaa, että lisäosa on asennettuna ja että ominaisuus on otettu käyttöön. Jos molemmat edellytykset täyttyvät, tilikauden lopetus suoritetaan mikropalvelussa.

[![Tietojen vuokaavio.](./media/Lifecycle-services.jpg)](./media/Lifecycle-services.jpg)

## <a name="high-level-flow-for-year-end-close-processing"></a>Tilikauden lopetusprosessin yleinen työnkulku

1. Tilikauden lopetusprosessi alkaa Financesta kohdasta **Kirjanpito \> Kausi suljettu \> Tilinpäätös**. Prosessi luo sulkevia erätyöitä ja tehtäviä tilinpäätöksen tekeville yrityksille.
2. Tilikauden lopetus määrittää, tulisiko se suorittaa mikropalvelussa vai nykyisellä tilinpäätöslogiikalla.

    - Jos Optimoi tilikauden lopetus -palvelun lisäosa on asennettuna Lifecycle Services -portaaliin ja **Optimoi tilikauden lopetus** -ominaisuus on käytössä ominaisuuksien hallinnassa, tilikauden lopetus suoritetaan mikropalvelussa.

        1. Optimoi tilikauden lopetus -ominaisuus luo tilipäätöksen palvelutyön jokaiselle tilinpäätöstä tekevälle yritykselle ja suorittaa sitten tilinpäätöslogiikan. Mikropalvelu suorittaa tilinpäätöksen.
        2. Finance kuuntelee tilinpäätöstä mikropalvelusta määrittääkseen, milloin mikropalvelu on saanut työn päätökseen. Tämän jälkeen tilikauden sulkemisen tulokset päivitetään Financen **Tilinpäätös**-sivulla.

    - Muussa tapauksessa tilikauden sulkeminen suoritetaan nykyisen tilinpäätöslogiikan mukaisesti.
