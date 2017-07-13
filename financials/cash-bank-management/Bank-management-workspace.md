---
title: "Maksuliikenteen työtila"
description: "Tässä ohjeaiheessa on tietoja maksuliikenteen työtilasta. Työtilassa on näkyvillä yrityksen pankkitileihin liittyviä tietoja. Siinä on myös yhteenvetonäkymä ja analytiikkasivu. Yhteenvetonäkymässä on yhteenvetoruudut, pankkitilitiedot, saldokaavio ja liittyvät tiedot. Analytiikkasivu näyttää Microsoft Power BI:n ominaisuuksien avulla pankkitilin saldoihin liittyviä visuaalisia tietoja."
author: saraschi
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 3abf4b151b177095b71d44e9a6c9fd8541eaa64e
ms.openlocfilehash: 759de82e9cd1c08f86c0a8eb55fa7bae5c4f740f
ms.contentlocale: fi-fi
ms.lasthandoff: 06/14/2017

---
# Maksuliikenteen työtila
<a id="bank-management-workspace" class="xliff"></a>

**Maksuliikenne**-työtilassa on yrityksen pankkitileihin liittyviä tietoja. Työtilassa on **Yhteenveto**-näkymä ja **Analytiikka**-sivu. **Yhteenveto**-näkymässä on yhteenvetoruudut, pankkitilitiedot, saldokaavio ja liittyvät tiedot. **Analytiikka**-sivu näyttää Microsoft Power BI:n ominaisuuksien avulla pankkitilin saldoihin liittyviä visuaalisia tietoja.

## Yhteenvetonäkymä
<a id="summary-view" class="xliff"></a>

### Yhteenveto
<a id="summary" class="xliff"></a>

**Yhteenveto**-osan ruuduissa on pankkitilien yleiskatsaus, Siitä voi myös siirtyä nopeasti eniten käytetyille sivuille. Pankkitilin täsmäytystiedot koskevat Pankkitilin täsmäytyksen lisätoiminnot -toimintoa. Tiedot koskevat vain niitä pankkitilejä, joiden **Pankkitilin täsmäytyksen lisätoiminnot** -asetukseksi on valittu **Kyllä** **Pankkitili**-sivulla. Voit tuoda **Yhteenveto**-osiossa kaikkien yritysten pankkitilien pankkitiedostoja.

### Pankkitilit
<a id="bank-accounts" class="xliff"></a>

Kutakin yrityksen pankkitiliä vastaa **Pankkitilit**-osion kortti. Näkyvissä on nykyinen saldo. Lisäksi kyseisen yhteenvedon saldosumman tapahtumiin voi porautua. Myös **Välitilitapahtumat**-summassa voi porautua kyseisen yhteenvetosumman tapahtumiin. Välitilitapahtumat ovat odottavia tapahtumia, jotka on kirjattu välitiliöintitoiminnolla mutta joita ei ole vielä selvitetty. **Odottava saldo** -summa on nykyinen saldo, josta on vähennetty välitiliöidyt eli odottavat tapahtumat.

Kortista näkee myös, milloin pankkitili täsmäytettiin viimeksi. Nämä tiedot näkyvät vain, jos pankkitilissä on otettu käyttöön Pankkitilin täsmäytyksen lisätoiminnot.

### Tase
<a id="balance" class="xliff"></a>

**Saldo**-kaaviossa on näkyvissä joko **Pankkitilit**-osiossa valitun tilin historialliset saldotiedot tai yrityksen kaikkien pankkitilien historiallisten saldotietojen yhteenveto. Nämä tiedot ovat saatavilla eripituisille jaksoille: kuluva viikko, kuluva kuukausi, kuluva vuosi, viimeiset viisi vuotta ja kaikki kaudet (pankkitilin koko historia). 

Jos tarkastelet yksittäisen pankkitilin **Saldo**-kaaviota, historialliset saldot näytetään pankkitilin valuuttana. Jos tarkastelet yrityksen kaikkien pankkitilin kaaviota, historialliset saldot näytetään kirjapitovaluuttana.

Kaavion yläreunasta voi tarkistaa, milloin tiedot on viimeksi päivitetty. Voit päivittää tietoja tarpeen mukaan:

### Aiheeseen liittyviä tietoja
<a id="related-information" class="xliff"></a>

Voit viimeistellä pankkisiirrot avaamalla **Liittyvät tiedot** -osiossa **Kirjauskansio**-sivun. Voit avata myös **Pankkitapahtumat**- ja **Välitilitapahtumat**-sivut nopeasti.

## Analytiikkanäkymä
<a id="analytics-view" class="xliff"></a>

**Analytiikka**-sivulla on tärkeitä valitun yrityksen pankkitilien mittareita. Sivulla on seuraavat visualisoinnit:

-   Pankkitilin kokonaissaldo järjestelmän valuuttana
-   Saldo yrityksen mukaan
-   Kuluvan päivän toteutuneen ja ennustetun saldon vertailu pankkitilin valuuttana
-   Saldo pankkitilin mukaan
-   Saldo valuutan mukaan

Voit tarkastella kaikkien yritysten pankkitietojen analytiikkaa **Kassayhteenveto – kaikki yritykset** -työtilassa.

