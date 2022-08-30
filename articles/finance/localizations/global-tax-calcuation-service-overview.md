---
title: Verolaskennan yleiskatsaus
description: Tässä artikkelissa selitetään verolaskentamahdollisuuden yleinen laajuus ja ominaisuudet.
author: EricWangChen
ms.date: 03/02/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: 2765b922bcc58837c32973b7ca96e0d63eb8b9d6
ms.sourcegitcommit: 14a27b776befbc6793390f97e8fb0279c0ea18c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/15/2022
ms.locfileid: "9295988"
---
# <a name="tax-calculation-overview"></a>Verolaskennan yleiskatsaus

[!include [banner](../includes/banner.md)]

Verolaskenta on hyperskaalautuva monivuokaajapalvelu, jonka avulla Global Tax Engine voi automatisoida ja yksinkertaistaa verotuksen määritys- ja laskentaprosessia. Veromoduuli on täysin konfiguroitavissa. Määritettäviä elementtejä ovat muun muassa verotettava tietomalli, verokoodi, verojen kohdistuksen matriisi ja verolaskelmakaava. Veromoduuli toimii Microsoft Azure -ydinpalvelualustalla ja tarjoaa modernia teknologiaa ja eksponentiaalisen skaalautuvuuden.

Verolaskenta integroituu Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin kanssa. Lopulta se tulee integroitumaan myös Dynamics 365 Project Operationsiin, Dynamics 365 Commerceen ja muihin ensimmäisen ja kolmannen osapuolen sovelluksiin.

> [!IMPORTANT]
> Kun veron laskentapalvelu otetaan käyttöön, joitakin liittyvien tietojen toimintoja voidaan suorittaa muissa kuin palvelun tietoja ylläpitävässä palvelinkeskuksessa. Tutustu [käyttöehtoihin](https://go.microsoft.com/fwlink/?linkid=2156043), ennen kuin otat veron laskentapalvelun käyttöön. Tietosuojasi on meille tärkeä. Lisätietoja on [tietosuojalausekkeessa](https://go.microsoft.com/fwlink/?LinkId=521839).

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
- Brasilia
- Kanada
- Eurooppa
- Ranska
- Intia
- Japani
- Etelä-Afrikka
- Sveitsi
- Yhdistyneet arabiemiirikunnat
- Yhdistynyt kuningaskunta
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
| 10.0.25         | Verolaskentamääritys 40.50.225 |
| 10.0.26         | Verolaskentamääritys 40.54.234 |
| 10.0.27         | Verolaskentamääritys 40.54.234 |
| 10.0.28         | Verolaskentamääritys 40.54.234 |
| 10.0.29         | Verolaskentamääritys 40.55.236 |


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

Seuraavia tapahtumia tuetaan versiossa 10.0.26: 

- Yleiset kirjauskansiot
- Toimittajan laskun kirjauskansio

Seuraavia tapahtumia tuetaan versiossa 10.0.28: 

- Toimittajan maksukirjauskansio
- Asiakkaan maksukirjauskansio

Seuraavia tapahtumia tuetaan versiossa 10.0.29: 


- Kausikirjauskansiot

## <a name="supported-countriesregions"></a>Tuetut maat/alueet

Verolaskelma voidaan suorittaa yhdessä seuraavien maiden/alueiden tuettujen lokisointiominaisuuksien kanssa yrityksen ensisijaista osoitetta varten: 

Tuettu versiossa 10.0.21:

- Itävalta
- Belgia
- Tanska
- Viro
- Suomi
- Ranska
- Saksa
- Unkari
- Islanti
- Irlanti
- Italia
- Latvia
- Liettua
- Alankomaat
- Norja
- Puola
- Ruotsi
- Sveitsi
- Yhdistynyt kuningaskunta
- Yhdysvallat

Tuettu versiossa 10.0.22:

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

Tuettu versiossa 10.0.23:

- Thaimaa
- Japani
- Malesia
- Singapore

Tuettu versiossa 10.0.24:

- Meksiko

Tuettu versiossa 10.0.26:

- Kiina
- Tšekin tasavalta
- Espanja

Verolaskelman voi ottaa käyttöön ja suorittaa myös muissa yleisissä ominaisuuksissa, kun maa tai alue ei ole Microsoftin lokalisoima.

## <a name="related-resources"></a>Liittyvät resurssit

[Veroapalvelun käytön aloittaminen](./global-get-started-with-tax-calculation-service.md)

[Useita ALV-rekisterinumeroita](./emea-multiple-vat-registration-numbers.md)

[Siirtotilauksen verotoiminnon tuki](./tasks/tax-feature-support-for-transfer-order.md)

[Näin rakennat laajennuksen veropalveluun](./tax-service-add-data-fields-tax-integration-by-extension.md)
