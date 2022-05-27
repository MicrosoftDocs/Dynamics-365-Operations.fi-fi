---
title: Maksuliikenteen työtila
description: Tässä ohjeaiheessa on tietoja maksuliikenteen työtilasta. Tässä työtilassa on yrityksen pankkitileihin liittyviä tietoja.
author: kweekley
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 9c0642664cbae84c966f2cd514a176e1412c80d5
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711461"
---
# <a name="bank-management-workspace"></a>Maksuliikenteen työtila

[!include [banner](../includes/banner.md)]

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

Voit tarkastella kaikkien yritysten pankkitietojen analytiikkaa **Kassayhteenveto – kaikki yritykset** -työtilassa. Lisätietoja on kohdassa [Kassayhteenvedon Power BI -sisältö](Cash-Overview-Power-BI-content.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
