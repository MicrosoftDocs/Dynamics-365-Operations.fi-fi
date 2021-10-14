---
title: Ostohyvitysten hallintaryhmät
description: Tässä aiheessa käsitellään ostohyvitysten hallintaryhmien määrittämistä. Ostohyvitysten hallintaryhmiä voi käyttää ostohyvitysten laskennassa, ja ne voidaan liittää päätietueeseen.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1f9deeedef504d1b2d0ba3431902c50bc65d62ba
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572694"
---
# <a name="rebate-management-groups"></a>Ostohyvitysten hallintaryhmät

[!include [banner](../includes/banner.md)]

Ostohyvityksen hallintalaskelmat voidaan määrittää ryhmien perusteella. Ostohyvitysten hallintaryhmiä voi luoda asiakkaille, toimittajille ja nimikkeille. Ne voidaan liittää päätietueeseen.

## <a name="rebate-management-customer-groups"></a>Ostohyvitysten hallinnan asiakasryhmät

Asiakasryhmän laskenta luodaan usein yritysketjulle, kuten marketketjulle tai franchise-yritykselle. Tämäntyyppinen laskentatapa liittyy yleensä ostohyvitykseen.

Vähennys lasketaan usein niin, että ei oteta huomioon sitä, kenelle hyväksytty tilaus on myyty. Tähän on kuitenkin poikkeuksia. Lisenssinhaltija voi esimerkiksi luoda vähennysmallin, johon asiakasryhmä A saa 4 prosenttia, mutta asiakasryhmä B saa vain 3 prosenttia.

### <a name="set-up-customer-groups"></a>Määritä asiakasryhmät

Voit käyttää ostohyvityksen hallinnan asiakasryhmiä kohdassa **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Asiakasryhmät**. Voit lisätä ja poistaa ryhmiä tarpeen mukaan käyttämällä toimintoruudun painikkeita. Määritä kullekin ryhmälle seuraavat kentät:

- **Ostohyvitysten hallintaryhmä** – Anna ryhmän yksilöivä nimi.
- **Kuvaus** – Syötä ryhmän kuvaus, joka sisältää lisätietoja ryhmän käytöstä.

### <a name="manage-customer-group-assignments"></a>Asiakasryhmän määritysten hallinta

Kukin asiakas voi kuulua mihin tahansa määrään ostohyvityksen hallintaryhmiä. Jos haluat tarkastella ja liittää ryhmän jäseniä, voit aloittaa joko ryhmäluettelosta tai asiakasluettelosta.

Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun ryhmän asiakkaita.

1. Siirry kohtaan **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Asiakasryhmät**.
1. Valitse hallittava ryhmä.
1. Valitse toimintoruudussa **Asiakkaat**. Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon asiakkaista, jotka kuuluvat jo valittuun ryhmään.
1. Lisää uusi asiakas ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon. Määritä sitten uudelle rivillä seuraava kenttä:

    - **Asiakastili** – Valitse asiakastilin tunnus.

1. Jos haluat poistaa asiakkaan ryhmästä, valitse asiakas ja valitse sitten toimintoruudusta **Poista**.

Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun asiakkaan ryhmämäärityksiä.

1. Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.
1. Valitse asiakas, jonka kanssa haluat työskennellä.
1. Valitse toimintoruudun **Asiakas**-välilehden **Ostohyvitysten hallinta** -ryhmässä **Ostohyvitysten hallintaryhmät**. Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon ryhmistä, joihin valittu asiakas jo kuuluu.
1. Lisää asiakas uuteen ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon. Määritä sitten uudelle rivillä seuraava kenttä:

    - **Ostohyvityksen hallintaryhmä** – Valitse ryhmä, johon asiakas lisätään.

1. Jos haluat poistaa asiakkaan ryhmästä, valitse ryhmä ja valitse sitten toimintoruudusta **Poista**.

## <a name="rebate-management-vendor-groups"></a>Ostohyvitysten hallinnan toimittajaryhmät

Toimittajaryhmän laskenta luodaan usein toimituspisteiden ryhmälle. Tämäntyyppinen laskentatapa liittyy yleensä ostohyvitykseen.

### <a name="set-up-vendor-groups"></a>Toimittajaryhmien määrittäminen

Voit käyttää ostohyvityksen hallinnan toimittajaryhmiä kohdassa **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Toimittajaryhmät**. Voit lisätä ja poistaa ryhmiä tarpeen mukaan käyttämällä toimintoruudun painikkeita. Määritä kullekin ryhmälle seuraavat kentät:

- **Ostohyvitysten hallintaryhmä** – Anna ryhmän yksilöivä nimi.
- **Kuvaus** – Syötä ryhmän kuvaus, joka sisältää lisätietoja ryhmän käytöstä.

### <a name="manage-vendor-group-assignments"></a>Toimittajaryhmän määritysten hallinta

Kukin toimittaja voi kuulua mihin tahansa määrään ostohyvityksen hallintaryhmiä. Jos haluat tarkastella ja liittää ryhmän jäseniä, voit aloittaa joko ryhmäluettelosta tai toimittajaluettelosta.

Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun ryhmän toimittajia.

1. Siirry kohtaan **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Toimittajaryhmät**.
1. Valitse hallittava ryhmä.
1. Valitse toimintoruudussa **Toimittajat**. Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon toimittajista, jotka kuuluvat jo valittuun ryhmään.
1. Lisää uusi toimittaja ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon. Määritä sitten uudelle rivillä seuraava kenttä:

    - **Toimittajatili** – Valitse toimittajatilin tunnus.

1. Jos haluat poistaa toimittajan ryhmästä, valitse toimittaja ja valitse sitten toimintoruudusta **Poista**.

Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun toimittajan ryhmämäärityksiä.

1. Siirry kohtaan **Ostoreskontra \> Toimittajat \> Kaikki toimittajat**.
1. Valitse toimittaja, jonka kanssa haluat työskennellä.
1. Valitse toimintoruudun **Toimittaja**-välilehden **Ostohyvitysten hallinta** -ryhmässä **Ostohyvitysten hallintaryhmät**. Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon ryhmistä, joihin valittu toimittaja jo kuuluu.
1. Lisää toimittaja uuteen ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon. Määritä sitten uudelle rivillä seuraava kenttä:

    - **Ostohyvityksen hallintaryhmä** – Valitse ryhmä, johon toimittaja lisätään.

1. Jos haluat poistaa toimittajan ryhmästä, valitse ryhmä ja valitse sitten toimintoruudusta **Poista**.

## <a name="item-rebate-groups"></a>Nimikkeen ostohyvitysryhmät

Nimikkeitä ryhmittelemällä saat enemmän joustavuutta ostohyvitysten ja vähennysten laskennan ajoitukseen. Tämä on usein tehokkaampi tapa määrittää asiakkaille ja toimittajille ostohyvitykset ja vähennykset.

### <a name="set-up-item-groups"></a>Määritä nimikeryhmät

Voit käyttää ostohyvityksen hallinnan nimikeryhmiä kohdassa **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Nimikeryhmät**. Voit lisätä ja poistaa ryhmiä tarpeen mukaan käyttämällä toimintoruudun painikkeita. Määritä kullekin ryhmälle seuraavat kentät:

- **Ostohyvitysten hallintaryhmä** – Anna ryhmän yksilöivä nimi.
- **Kuvaus** – Syötä ryhmän kuvaus, joka sisältää lisätietoja ryhmän käytöstä.

### <a name="manage-item-group-assignments"></a>Nimikeryhmän määritysten hallinta

Kukin nimike voi kuulua mihin tahansa määrään ostohyvityksen hallintaryhmiä. Jos haluat tarkastella ja liittää ryhmän jäseniä, voit aloittaa joko ryhmäluettelosta tai nimikeluettelosta. Voit myös lisätä nimikkeitä luokkahierarkian mukaan.

Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun ryhmän nimikkeitä.

1. Siirry kohtaan **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Nimikeryhmät**.
1. Valitse hallittava ryhmä.
1. Valitse toimintoruudussa **Nimikkeet**. Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon nimikkeistä, jotka kuuluvat jo valittuun ryhmään.
1. Lisää uusi nimike ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon. Määritä sitten uudelle rivillä seuraava kenttä:

    - **Nimikejatili** – Valitse nimiketilin tunnus.

1. Jos haluat poistaa nimikkeen ryhmästä, valitse nimike ja valitse sitten toimintoruudusta **Poista**.

Noudattamalla seuraavia ohjeita voit tarkastella, lisätä tai poistaa valitun nimikkeen ryhmämäärityksiä.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse nimike, jonka kanssa haluat työskennellä.
1. Valitse toimintoruudun **Tuote**-välilehden **Ostohyvitysten hallinta** -ryhmässä **Ostohyvitysten hallintaryhmät**. Näkyviin tulee **Ostohyvityksen hallintaryhmät** -sivu, joka sisältää luettelon ryhmistä, joihin valittu nimike jo kuuluu.
1. Lisää nimike uuteen ryhmään valitsemalla toimintoruudussa **Uusi**, mikä lisää rivin ruudukkoon. Määritä sitten uudelle rivillä seuraava kenttä:

    - **Ostohyvityksen hallintaryhmä** – Valitse ryhmä, johon nimike lisätään.

1. Jos haluat poistaa nimikkeen ryhmästä, valitse ryhmä ja valitse sitten toimintoruudusta **Poista**.

Voit lisätä nimikkeitä ryhmään luokkahierarkian mukaan noudattamalla seuraavia vaiheita.

1. Siirry kohtaan **Ostohyvitysten hallinta \> Ostohyvitysten hallintaryhmien asetukset \> Nimikeryhmät**.
1. Valitse hallittava ryhmä.
1. Valitse toimintoruudussa **Lisää nimikkeitä**.
1. Valitse **Lisää nimikkeitä** -valintaikkunan **Luokkahierarkia**-kentästä ylätason luokka.
1. Nimikehierarkia avataan vasemmassa ruudussa. Valitse etsi haluamasi hierarkiataso. 
1. Valitun hierarkian ja hierarkiatason nimikkeet näkyvät nyt oikeanpuoleisessa ruudussa. Noudata seuraavia ohjeita, kun haluat käyttää ruutua:

    - Valitse jokaisen lisättävän nimikkeen valintaruutu.
    - Valitse kaikki luettelon nimikkeet valitsemalla ruudukon otsikon valintaruutu.
    - Valitse **Näytä valitut** -painike, kun haluat suodattaa ruudukon siten, että siinä näkyvät vain tähän mennessä valitsemasi nimikkeet. Voit palata koko luetteloon valitsemalla painikkeen uudelleen.

1. Ota nimikevalinta käyttöön valitussa ryhmässä valitsemalla **OK**.
