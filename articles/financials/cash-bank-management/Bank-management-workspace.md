---
title: "Maksuliikenteen työtila"
description: "Tässä ohjeaiheessa on tietoja maksuliikenteen työtilasta. Työtilassa on näkyvillä yrityksen pankkitileihin liittyviä tietoja. Siinä on myös yhteenvetonäkymä ja analytiikkasivu. Yhteenvetonäkymässä on yhteenvetoruudut, pankkitilitiedot, saldokaavio ja liittyvät tiedot. Analytiikkasivu näyttää Microsoft Power BI:n ominaisuuksien avulla pankkitilin saldoihin liittyviä visuaalisia tietoja."
author: saraschi2
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 91a6c2e5aeee4a10ffbd574f99218d49f9a19bbc
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="bank-management-workspace"></a>Maksuliikenteen työtila

**Maksuliikenne**-työtilassa on yrityksen pankkitileihin liittyviä tietoja. Työtilassa on **Yhteenveto**-näkymä ja **Analytiikka**-sivu. **Yhteenveto**-näkymässä on yhteenvetoruudut, pankkitilitiedot, saldokaavio ja liittyvät tiedot. **Analytiikka**-sivu näyttää Microsoft Power BI:n ominaisuuksien avulla pankkitilin saldoihin liittyviä visuaalisia tietoja.

## <a name="summary-view"></a>Yhteenvetonäkymä

### <a name="summary"></a>Yhteenveto

**Yhteenveto**-osan ruuduissa on pankkitilien yleiskatsaus, Siitä voi myös siirtyä nopeasti eniten käytetyille sivuille. Pankkitilin täsmäytystiedot koskevat Pankkitilin täsmäytyksen lisätoiminnot -toimintoa. Tiedot koskevat vain niitä pankkitilejä, joiden **Pankkitilin täsmäytyksen lisätoiminnot** -asetukseksi on valittu **Kyllä** **Pankkitili**-sivulla. Voit tuoda **Yhteenveto**-osiossa kaikkien yritysten pankkitilien pankkitiedostoja.

### <a name="bank-accounts"></a>Pankkitilit

Kutakin yrityksen pankkitiliä vastaa **Pankkitilit**-osion kortti. Näkyvissä on nykyinen saldo. Lisäksi kyseisen yhteenvedon saldosumman tapahtumiin voi porautua. Myös **Välitilitapahtumat**-summassa voi porautua kyseisen yhteenvetosumman tapahtumiin. Välitilitapahtumat ovat odottavia tapahtumia, jotka on kirjattu välitiliöintitoiminnolla mutta joita ei ole vielä selvitetty. **Odottava saldo** -summa on nykyinen saldo, josta on vähennetty välitiliöidyt eli odottavat tapahtumat.

Kortista näkee myös, milloin pankkitili täsmäytettiin viimeksi. Nämä tiedot näkyvät vain, jos pankkitilissä on otettu käyttöön Pankkitilin täsmäytyksen lisätoiminnot.

### <a name="balance"></a>Tase

**Saldo**-kaaviossa on näkyvissä joko **Pankkitilit**-osiossa valitun tilin historialliset saldotiedot tai yrityksen kaikkien pankkitilien historiallisten saldotietojen yhteenveto. Nämä tiedot ovat saatavilla eripituisille jaksoille: kuluva viikko, kuluva kuukausi, kuluva vuosi, viimeiset viisi vuotta ja kaikki kaudet (pankkitilin koko historia). 

Jos tarkastelet yksittäisen pankkitilin **Saldo**-kaaviota, historialliset saldot näytetään pankkitilin valuuttana. Jos tarkastelet yrityksen kaikkien pankkitilin kaaviota, historialliset saldot näytetään kirjapitovaluuttana.

Kaavion yläreunasta voi tarkistaa, milloin tiedot on viimeksi päivitetty. Voit päivittää tietoja tarpeen mukaan:

### <a name="related-information"></a>Aiheeseen liittyviä tietoja

Voit viimeistellä pankkisiirrot avaamalla **Liittyvät tiedot** -osiossa **Kirjauskansio**-sivun. Voit avata myös **Pankkitapahtumat**- ja **Välitilitapahtumat**-sivut nopeasti.

## <a name="analytics-view"></a>Analytiikkanäkymä

**Analytiikka**-sivulla on tärkeitä valitun yrityksen pankkitilien mittareita. Sivulla on seuraavat visualisoinnit:

-   Pankkitilin kokonaissaldo järjestelmän valuuttana
-   Saldo yrityksen mukaan
-   Kuluvan päivän toteutuneen ja ennustetun saldon vertailu pankkitilin valuuttana
-   Saldo pankkitilin mukaan
-   Saldo valuutan mukaan

Voit tarkastella kaikkien yritysten pankkitietojen analytiikkaa **Kassayhteenveto – kaikki yritykset** -työtilassa.
