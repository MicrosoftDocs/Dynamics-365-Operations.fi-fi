---
title: Keräyksen ja pakkauksen vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä kerättäessä ja pakattaessa Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 74854fa95837dd8a133860e2a017be4c92ff84a3
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645474"
---
# <a name="troubleshoot-picking-and-packing"></a>Keräyksen ja pakkauksen vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä kerättäessä ja pakattaessa Microsoft Dynamics 365 Supply Chain Managementissa.

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a>Seuraava virhesanoma avautuu: Dimension sijaintia ei voi jättää tyhjäksi, jos dimension sarjanumero on määritetty.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä virhesanoma avautuu, jos sarjanimikkeelle luodaan siirtotilaus käyttämällä varastoa, jossa on otettu käyttöön edistyksellinen varastonhallinta, ja kun lähetystä yritetään vahvistaa työn valmistumisen jälkeen.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Lähtövaraston kuljetusvaraston **Oletusvastaanottosijainti** -kenttä on tyhjä. Korjaa ongelma määrittämällä oletusvastaanottosijainti kuljetusvarastossa. Varmista, että tämä sijainti on rekisterikilpiohjattu.

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a>Seuraava virhesanoma avautuu: Virheellinen rekisterikilpi.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä virhesanoma avautuu varastosovelluksessa, kun rekisterikilven tunnus skannataan.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Varmista, että rekisterikilven tunnus on rekisterikilpitaulukossa ja että rekisterikilven nimikkeet ja määrät ovat käytettävissä (eli niitä ei ole estetty).

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a>Seuraava virhesanoma avautuu: Kenttä Kuorman paino(=-%1) voi sisältää vain positiivisia lukuja. Päivitys on keskeytetty.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä virhesanoma avautuu, jos työ on avoin, kun työ käsitellään pakkaussijainneista valmistelusijainteihin tai valmistelusijainneista laiturisijainteihin.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Voit korjata ongelman valitsemalla **Järjestelmänhallinta \> Kausittaiset tehtävät \> Tietokanta \> Yhdenmukaisuustarkistus** ja suorittamalla **Varaston kuorman painon yhdenmukaisuustarkistus** -prosessin.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Seuraava virhesanoma avautuu: Yksikön %1 määrä ei kelpaa.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä virhesanoma avautuu, kun yrität suorittaa *jaetun keräilyn* useissa erissä.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Varastotyöntekijän on käytettävä *Lyhyt keräily* -prosessia varastosovelluksessa. Jos yrität kerätä useita eriä samasta sijainnista, voit käyttää myös varastosovelluksen **Täysi**-vaihtoehdolla.

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a>Varastoa ei voi siirtää rekisterikilpiohjattuun sijaintiin.

### <a name="issue-description"></a>Ongelman kuvaus

Kuormituksen kerättyjä määriä ei voi vähentää.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Aiemmissa versioissa kuormituksen kerättyjä määriä ei voi vähentää. Voit nyt kumota keräyksen rekisterikilpiohjattuun sijaintiin. Sekä **Sijainti**- että **Rekisterikilpi**-arvo on määritettävä kuormariville **Vähennä keräiltyä määrää** -sivulla.

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a>Voidaanko toimitusilmoitus tai pakkaussisältö tulostaa varastokohtaisesti?

### <a name="issue-description"></a>Ongelman kuvaus

Haluat tulostaa toimitusilmoituksen tai pakkaussisällön varasto- tai sivustokohtaisesti **Työn tarkistusmallin rivien päivitys** -sivulla.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Kun asiakirja tulostetaan tulostuksen hallinta-asetuksilla, rajoita laajuus (toimipaikka tai varasto) tulostuksen hallinnassa sen sijaan, että valitsisit **Muokkaa tulostusasetuksia** **Työn tarkistusmallin rivien päivitys** -sivulla.

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Pakkausluetteloa ei voi peruuttaa sen jälkeen, kun se on kirjattu myyntitilauksesta

### <a name="issue-description"></a>Ongelman kuvaus

Kun keräily- ja lähetysprosessit on otettu käyttöön varastonhallintajärjestelmässä, pakkausluettelo ei voi peruuttaa, kun se on kirjattu myyntitilauksesta.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Varastonhallintajärjestelmää käyttävien nimikkeiden kirjattujen pakkausluetteloiden korjaaminen edellyttää, että kirjaaminen tehdään kuormasta eikä tilauksesta. Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus. Yleisesti ottaen myyntitilauksen, joka on kerätty ja lähetetty varastonhallintaprosesseilla, pakkausluettelopäivitys voidaan tehdä kuormituksesta tai lähetyksestä ja itse myyntitilausasiakirjasta. Jos myyntitilauksen pakkausluettelopäivitys kuitenkin tehdään myyntitilausasiakirjasta, pakkausluettelon palautusta ei voi edelläänkään tehdä kuormasta tai myyntitilauksesta. Tämän vuoksi kannattaa käyttää pakkausluettelon kirjaamista kuormasta. Siinä tapauksessa kuormasta tehtävä peruutus otetaan käyttöön.

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a>Seuraava virhesanoma avautuu: Klusterille ei löydy tarpeeksi työtä.

### <a name="issue-description"></a>Ongelman kuvaus

Jos määrität *Järjestelmäohjattu klusterikeräily* -prosessia käytettäessä klusteriprofiilin, jossa voidaan kerätä esimerkiksi 10 paikkaa, prosessi toimii suunnitellusti, kun töitä on riittävästi 10 paikkaan keräilyyn. Jos keräilyyn on kuitenkin vain kahdeksan paikkaa, tämä virhesanoma avautuu, koska työtä ei ole riittävästi yhdelle klusterille.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Korjaa tämä ongelma muokkaamalla klusteriprofiilia ja määrittämällä **Aktivoi toimet** -asetukseksi *Ei*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]