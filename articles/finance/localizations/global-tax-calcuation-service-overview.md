---
title: Verolaskennan yleiskatsaus
description: Tässä ohjeaiheessa selitetään verolaskentamahdollisuuden yleinen laajuus ja ominaisuudet.
author: wangchen
ms.date: 11/17/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b5f9f41bdadc76064aa9aee92e27e6b504baf461
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986013"
---
# <a name="tax-calculation-overview"></a>Verolaskennan yleiskatsaus

[!include [banner](../includes/banner.md)]

Verolaskenta on hyperskaalautuva monivuokaajapalvelu, jonka avulla Global Tax Engine voi automatisoida ja yksinkertaistaa verotuksen määritys- ja laskentaprosessia. Veromoduuli on täysin konfiguroitavissa. Määritettäviä elementtejä ovat muun muassa verotettava tietomalli, verokoodi, verojen kohdistuksen matriisi ja verolaskelmakaava. Veromoduuli toimii Microsoft Azure -ydinpalvelualustalla ja tarjoaa modernia teknologiaa ja eksponentiaalisen skaalautuvuuden.

Verolaskenta integroituu Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin kanssa. Lopulta se tulee integroitumaan myös Dynamics 365 Project Operationsiin, Dynamics 365 Commerceen ja muihin ensimmäisen ja kolmannen osapuolen sovelluksiin.

> [!IMPORTANT]
> Kun veron laskentapalvelu otetaan käyttöön, joitakin liittyvien tietojen toimintoja voidaan suorittaa muissa kuin palvelun tietoja ylläpitävässä palvelinkeskuksessa. Tutustu [käyttöehtoihin](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md), ennen kuin otat veron laskentapalvelun käyttöön. Tietosuojasi on meille tärkeä. Lisätietoja on [tietosuojalausekkeessa](https://go.microsoft.com/fwlink/?LinkId=521839).

Verolaskenta on mikropalvelupohjainen veromoduuli, jonka äärimmäinen skaalautuva ja jolla voi suorittaa seuraavat tehtävät:

- Oikean arvolisäveroryhmän, nimikkeen arvonlisäveroryhmän ja verokoodin määrittäminen automaattisesti parannetun määritysmekanismin avulla.
- Useiden verorekisteröintinumeroiden tuki yhdessä yrityksessä ja oikean verorekisteröintinumeron määrittäminen automaattisesti verotettavissa tapahtumissa.
- Siirtotilausten veron määrittämisen, laskemisen, kirjaamisen ja tilityksen tuki.
- Määritettävien veron laskentakaavojen ja -ehtojen määrittäminen liiketoimintatarpeiden mukaisesti.
- Veron määritys- ja laskentaratkaisun jakaminen yrityksessä, mikä vähentää ylläpitotarpeita ja virheitä.
- Asiakkaan ja toimittajan verorekisteröintinumeron määrityksen tuki.
- Luettelokoodin määrityksen tuki.
- Veron laskentaparametrien tuki veroviranomaistasolla.

Verolaskennan käyttöä varten on asennettava verolaskennan apuohjelma Microsoft Dynamics Lifecycle Servicesin projektista. Määritys viimeistellään [Regulatory Configuration Servicessa](https://marketing.configure.global.dynamics.com/) ja verolaskenta otetaan käyttöön Financessa ja Supply Chain Managementissa. Lisätietoja on kohdassa [Veroaplvelun käytön aloittaminen](global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Käytettävyys

Verolaskenta on yleisesti saatavana kaikkien asiakkaiden tuotantoympäristöissä versiosta 10.0.21 alkaen.

Uusia ominaisuuksia toimitetaan myös jatkossa. Uusin julkaisusuunnitelma kannattaa tarkistaa usein, sillä siinä on lisätietoja tuettujen ominaisuuksien kattavuudesta ja laajuudesta.

Verolaskenta otetaan käyttöön seuraavilla Azuren maantieteellisillä alueilla. Uusia Azuren maantieteellisiä alueita lisätään asiakkaiden tarpeiden mukaan.

- Aasia ja Tyynenmeren alue
- Australia
- Kanada
- Eurooppa
- Japani
- Iso-Britannia
- Yhdysvallat

> [!NOTE]
> Verolaskenta ei tue Dynamics 365:n aiempia versioita, kuten Dynamics AX 2012, tai Dynamics 365:n paikallisissa käyttöönotoissa.

## <a name="versions"></a>Versiot
On suositeltavaa tuoda ja määrittää verolaskelman konfiguraatio versiolle, joka vastaa Financen tai Supply Chain Managementin versiota.

| Financen tai Supply Chain Managementin versio | Veromääritysten versio               |
| --------------- | --------------------------------------- |
| 10.0.18         | Veromääritys – Eurooppa 30.12.82     |
| 10.0.19         | Verolaskentamääritys 36.38.193 |
| 10.0.20         | Verolaskentamääritys 40.43.208 |
| 10.0.21         | Verolaskentamääritys 40.48.215 |
| 10.0.22         | Verolaskentamääritys 40.48.215 |
| 10.0.23         | Verolaskentamääritys 40.50.221 |
| 10.0.24         | Verolaskentamääritys 40.50.225 |


## <a name="data-flow"></a>Tietojen virtaus

Verolaskennan tietovuoprosessin yhteenveto. 

1. Tarkastele ja tuo verottavien asiakirjojen mallimääritykset ja mallin yhdistämismäärityksen määritykset RCS:ssä. Lisätietoja määritysten laajentamisesta edistyneissä skenaarioissa on kohdassa [Tietokenttien lisääminen veromäärityksissä](tax-service-add-data-fields-tax-configurations.md).
2. Luo tai ylläpidä verotoimintoja RCS:ssä. Verotoimintojen avulla voidaan ylläpitää veroprosentteja ja veron käytettävyyssääntöjä.
3. Kun verotoiminto on määritetty, julkaise veromääritykset ja verotoiminnot RCS:stä yleiseen säilöön.
4. Valitse Financessa tietyssä yrityksessä käytettävä verotoiminnon määritysversio.
5. Käytä toimintoja Financessa ja Supply Chain Managementissa tavalliseen tapaan. Kun verolaskentaa tarvitaan, asiakasohjelma kerää tapahtumasta tietoja, kuten myyntitilauksen tai ostotilauksen, ja paketoi tiedot lisätietoina. Sen jälkeen lähetetään veron laskentapyyntö.
6. Veron laskentapyyntö vastaanotetaan asiakasohjelmasta ja laskenta on valmis. Verotulos palautetaan sitten asiakasohjelmaan.
7. Dynamics 365 -asiakasohjelma vastaanottaa verotuloksen ja näyttää verolaskennan tuloksena arvonlisäverosivulla.

## <a name="supported-transactions"></a>Tuetut tapahtumat

Tapahtumat voivat ottaa verolaskennan käyttöön. 

Seuraavia tapahtumia tuetaan versiossa 10.0.21: 

- Myynti

    - Myyntitarjous
    - Myyntitilaus
    - Vahvistus
    - Materiaaliluettelo
    - Pakkausluettelo
    - Myyntilasku
    - Hyvityslasku
    - Palautustilaus
    - Otsikon muu kulu
    - Rivin muu kulu

- Osto

    - Ostotilaus
    - Vahvistus
    - Saapumisluettelo
    - Tuotteen vastaanotto
    - Ostolasku
    - Otsikon muu kulu
    - Rivin muu kulu
    - Hyvityslasku
    - Palautustilaus
    - Ostoehdotus
    - Ostoehdotuksen rivin muu kulu
    - Tarjouspyyntö
    - Tarjouspyynnön otsikon muu kulu
    - Tarjouspyynnön rivin muu kulu

- Varasto

    - Siirtotilaus – lähetä
    - Siirtotilaus – vastaanota

Seuraavia tapahtumia tuetaan versiossa 10.0.23: 

- Vapaatekstilasku

## <a name="supported-countriesregions"></a>Tuetut maat/alueet

Yritys voi ottaa verolaskennan käyttöön. 

Versiossa 10.0.21 tuetaan seuraavia maita tai alueita yrityksenä ensisijaisena osoitteena:

- Itävalta
- Belgia
- Tanska
- Viro
- Suomi
- Ranska
- Saksa
- Unkari
- Islanti
- Italia
- Latvia
- Liettua
- Alankomaat
- Norja
- Puola
- Ruotsi
- Sveitsi
- Iso-Britannia
- Yhdysvallat

Versiossa 10.0.22 tuetaan seuraavia maita tai alueita yrityksenä ensisijaisena osoitteena:

- Australia
- Bahrain
- Kanada
- Egypti
- Hongkong, erityishallintoalue
- Kuwait
- Uusi-Seelanti
- Oman
- Qatar
- Saudi-Arabia
- Etelä-Afrikka
- Yhdistyneet arabiemiirikunnat

Versiossa 10.0.23 tuetaan seuraavia maita tai alueita yrityksenä ensisijaisena osoitteena:

- Thaimaa
- Japani
- Malesia
- Singapore

Versiossa 10.0.24 tuetaan seuraavia maita tai alueita yrityksenä ensisijaisena osoitteena:

- Meksiko

## <a name="related-resources"></a>Liittyvät resurssit

[Veroapalvelun käytön aloittaminen](./global-get-started-with-tax-calculation-service.md)

[Useita ALV-rekisterinumeroita](./emea-multiple-vat-registration-numbers.md)

[Siirtotilauksen verotoiminnon tuki](./tasks/tax-feature-support-for-transfer-order.md)

[Näin rakennat laajennuksen veropalveluun](./tax-service-add-data-fields-tax-integration-by-extension.md)
