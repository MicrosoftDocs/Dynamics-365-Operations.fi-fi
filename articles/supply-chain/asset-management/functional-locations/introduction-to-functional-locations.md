---
title: Toiminnallisten sijaintien esittely
description: Tässä artikkelissa on yleiskatsaus toiminnallisista sijainneista resurssien hallinnassa.
author: johanhoffmann
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationEditSubLocations, EntAssetFunctionalLocationLookup, EntAssetFunctionalLocationRename, EntAssetFunctionalLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2214"
- intro-internal
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a94b366dc725db3af01c156ae517a241213f7d52
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016040"
---
# <a name="introduction-to-functional-locations"></a>Toiminnallisten sijaintien esittely

[!include [banner](../../includes/banner.md)]

 

Tässä artikkelissa on yleiskatsaus toiminnallisista sijainneista resurssien hallinnassa. Toiminnalliset sijainnit ovat teknisen rakenteen elementtejä, kuten järjestelmän toiminnallisia yksiköitä. Toiminnalliset sijainnit luodaan hierarkkisesti ja niihin asennetaan resursseja. Yrityksen toiminnallisten sijaintien asetukset määräytyvät yrityksen tarpeiden mukaan.

Seuraavassa on esimerkkejä siitä, miten voit käyttää toiminnallisia sijainteja:

- **Toiminnallinen** – toiminnalliset sijainnit voivat olla käyttäjälähtöisiä ja käyttää hallitsemaan resursseja, joilla on samanlainen käyttäytyminen.
- **Prosessiin liittyvät** – toiminnalliset sijainnit voivat olla työnkulkuun suuntautuneita.
- **Tilaan liittyvät** – toiminnalliset sijainnit voivat edustaa maantieteellisiä sijainteja tai toimipaikkoja.

Jokaista toiminnallista sijaintia hallitaan itsenäisesti resurssien hallinnassa. Tässä on muutamia toiminnallisten siajintien hyödyllisiä ominaisuuksia:

- Määritä toiminnalliset sijaintimääritykset.
- Määritä resurssin määrittelyvaatimukset.
- Määritä ennaltaehkäisevän ja reaktiivisen kunnossapidon huoltojaksot.
- Hallitse asennettuja resursseja.
- Voit seurata asennettuun omaisuuteen liittyviä aktiivisia pyyntöjä ja työtilauksia.
- Seuraa vikoja, jotka on rekisteröity resursseille.
- Seuraa huoltokustannuksia resursseille, jotka liittyvät toiminnalliseen sijaintiin tiettynä ajankohtana.

Toiminnalliset sijainnit tarjoavat resurssien jäljitettävyyden pyyntöjen, työtilausten, vikarekisteröintien, kunnon arviointien, tuotannon keskeytyksen rekisteröintien ja resurssien laskurien rekisteröintien suhteen.

> [!NOTE]
> Vaikka resurssi asennetaan eri toiminnallisiin paikkoihin sen elinkaaren aikana, kustannukset voivat liittyä kuhunkin sijaintiin. Toisin sanoen resurssien kustannukset liittyvät aina siihen toiminnalliseen sijaintiin, johon resurssi on kullakin hetkellä asennettu.

Toiminnalliset sijainnit **eivät** ole joustavia. Siksi, kun olet määrittänyt toiminnallisen sijainnin hierarkian, et voi siirtää sijainteja sen ympärillä. 

Kun olet luonut toiminnallisen sijainnin hierarkian, seuraava vaihe on asentaa resurssit siihen. Lisätietoja on kohdassa [Asenna toiminnallisten sijaintien resurssit](../functional-locations/install-objects-on-functional-locations.md).

## <a name="all-functional-locations"></a>Kaikki toiminnalliset sijainnit

Valitse **Resurssien hallinta** \> **Toiminnalliset sijainnit** \> **Kaikki toiminnalliset sijainnit**, jos haluat avata **Kaikki toiminnalliset sijainnit** -luettelosivun. Tällä sivulla näkyvät kaikki toiminnalliset sijainnit ja jotkin kuhunkin liittyvät tiedot. Jos haluat tarkastella vain aktiivisia toiminnallisia sijainteja , valitse **Aktiiviset toiminnalliset sijainnit**. Jos haluat tarkastella vain toiminnallisia sijainteja, joihin olet yhteydessä työntekijänä, valitse **Omat aktiiviset toiminnalliset sijainnit**. (Tämä suhde määritetään **Työntekijät**-sivulla. Lisätietoja on kohdassa [Ylläpitotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).)

Valitse **Kaikki toiminnalliset sijainnit**-luettelosivulla **Toiminnallinen sijainti** -sarakkeesta linkki, jos haluat tarkastella valitun tietueen tietoja. Muokkaa toiminnallista sijaintia valitsemalla **Muokkaa**-painike. Tiedot-näkymässä näkyvät sijaintiin liittyvät yksityiskohtaiset tiedot. Se sisältää myös oikealla olevan **Aiheeseen liittyvät tiedot** -ruudun. Tässä ruudussa näkyy toiminnallisen sijainnin hierarkia. Voit laajentaa ja tiivistää **Aiheeseen liittyvät tiedot** -ruudun.

Toimintoruudun painikkeet on järjestetty välilehtiin. Seuraavassa taulukossa kuvataan lyhyesti resurssien hallintaan liittyvät painikkeet.

| Painikkeen nimi                         | Kuvaus                                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Muokkaa                                | Siirtyy sivun muokkaustilasta ja katselutilasta toiseen.                                                                                         |
| Uusi                                 | Luo uusi toiminnallinen sijainti                                                                                                            |
| Poista                              | Poista valittu toiminnallinen sijainti                                                                                                     |
| Nimeä uudelleen                              | Nimeä valittu toiminnallinen sijainti uudelleen                                                                                                     |
| Kopioi toiminnallisen sijainnin rakenne  | Kopioi toiminnallisen sijainnin hierarkia.                                                                                                      |
| Asenna resurssi                       | Asenna resurssi, mukaan lukien aliresurssit, toiminnalliseen sijaintiin.                                                                        |
| Korvaa resurssi                       | Korvaa resurssihierarkia toiminnallisen sijainnin toisella resurssihierarkialla.                                                         |
| Kustannusseuranta                        | Avaa **Toiminnallisen sijainnin kustannusten hallinta** -sivu, jolla voit tehdä valitun toiminnallisen sijainnin kustannuslaskennan.                |
| Tuntien hallinta                        | Avaa **Toiminnallisen sijainnin tuntien hallinta** -sivu, jolla voit tehdä valitun toiminnallisen sijainnin kustannuslaskennan.                |
| Resurssit                              | Avaa **Kaikki resurssit** -sivu, jolla voit tarkastella luetteloa resursseista, jotka liittyvät valittuun toiminnalliseen sijaintiin.                      |
| Pyynnöt                            | Avaa **Aktiiviset resurssit** -sivu, jolla voit tarkastella luetteloa pyynnöistä, jotka liittyvät valittuun toiminnalliseen sijaintiin.               |
| Työtilaukset                         | Avaa **Aktiiviset työtilaukset** -sivu, jolla voit tarkastella luetteloa työtilauksista, jotka liittyvät valittuun toiminnalliseen sijaintiin.         |
| Viat                              | Avaa **Resurssin viat** -sivu, jolla voit tarkastella luetteloa resurssin vikarekisteröinneistä, jotka liittyvät valittuun toiminnalliseen sijaintiin. |
| Päivitä toiminnallisen sijainnin tila    | Päivitä valitun toiminnallisen siajinnin vaihe                                                                                        |
| Elinkaaren tilan loki                 | Tarkastele lokia, joka näyttää valitun toiminnallisen sijainnin vaiheet.                                                                        |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]