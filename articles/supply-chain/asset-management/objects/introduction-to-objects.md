---
title: Resurssien esittely
description: Tässä aiheessa on yleiskatsaus resurssien hallinnan resursseihin.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetTimeline, EntAssetObjectTableLookup, EntAssetObjectTableParent, EntAssetObjectOverview, EntAssetObjectImage, EntAssetObjectTable, EntAssetLifecycleStateLog, EntAssetObjectWorkOrderActive, EntAssetObjectAttribute
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91c4ad4a96ce94c911066604794420c335a491b1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808565"
---
# <a name="introduction-to-assets"></a>Resurssien esittely

[!include [banner](../../includes/banner.md)]

 

Tässä aiheessa on yleiskatsaus resurssien hallinnan resursseihin. *Resurssi* on minkä tahansa tyyppinen laite, kuten kone tai koneen osa, joka edellyttää ylläpitoa, huoltoa tai korjausta.

Resurssiiin päivitetään automaattisesti ja siihen liittyvät tiedot. Nämä liittyvät tiedot voivat olla esimerkiksi uusista tai päivitetyistä työtilauksista. Voit luoda resursseja käyttämällä joko **Kaikki resurssit** -valikkonimikettä tai **Odottavat resurssit** -valikkonimikettä. Tässä ohjeaiheessa kerrotaan, kuinka resurssit luodaan käyttämällä **Kaikki resurssit**-valikkonimikettä. Lisätietoja resurssien luomisesta **Odottavat resurssit** -valikkovaihtoehdon avulla on kohdassa [Resurssien luominen ostotilausten perusteella](../objects/create-objects-based-on-purchase-orders.md).

## <a name="all-assets"></a>Kaikki käyttöomaisuus

Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit**. **Kaikki resurssit** -luettelosivulla näkyvät kaikki resurssit ja niihin liittyvät tiedot. Jos haluat tarkastella vain aktiivisia resursseja, valitse **Aktiiviset resurssit**. Jos haluat tarkastella vain toiminnallisiin sijainteihin asennettuja resursseja, joihin olet yhteydessä ylläpitotyöntekijänä, valitse **Omat aktiiviset resurssit**. (Tämä suhde määritetään **Työntekijät**-sivulla. Lisätietoja on kohdassa [Ylläpitotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).)

Valitse **Kaikki resurssit**-ruudukkonäkymässä **Resurssi**-sarakkeesta linkki, jos haluat tarkastella valitun tietueen tietoja. Muokkaa tietuetta valitsemalla **Muokkaa**-painike. Tiedot-näkymässä näkyvät resurssiin liittyvät yksityiskohtaiset tiedot. Oikeanpuoleinen **Aiheeseen liittyvät tiedot** -ruutu sisältää muita resurssiin liittyviä tietoja. Laajenna ruutu, jos haluat näyttää valitun resurssin liittyvät tiedot.

Toimintoruudun painikkeet on järjestetty välilehtiin. Seuraavassa taulukossa kuvataan lyhyesti resurssien hallintaan liittyvät painikkeet.

| Painikkeen nimi          | Kuvaus                                                                                                                                                       |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Muokkaa                 | Muokkaa valittua resurssia.                                                                                                                                         |
| Uusi                  | Luo uusi resurssi.                                                                                                                                                |
| Poista               | Poista valittu resurssi.                                                                                                                                       |
| Siirrä resurssi           | Siirrä resurssit joko toiseen resurssirakenteeseen tai toiseen sijaintiin samassa resurssirakenteessa.                                                                                         |
| Korvaa resurssi        | Korvaa yksi alemman tason resurssi resurssihierarkiassa toisella resurssilla.                                                                                                  |
| Asenna resurssi        | Asenna resurssi toiminnalliseen sijaintiin.                                                                                                                          |
| Kopioi resurssi           | Kopioi resurssihierarkia toiseen resurssiin.                                                                                                                          |
| Pyynnöt             | Avaa **Aktiiviset resurssit** -luettelosivu, jolla voit tarkastella ylläpitopyyntöjä, jotka on luotu valitulle resurssille.                                                                         |
| Tapahtumahistoria        | Tarkastele resurssiin tehtyjen rekisteröintien yhteenvetoa.                                                                                                         |
| Resurssirakenne            | Näytä kaikkien resurssiin käytettävien nimikkeiden (varaosien ja muiden nimikkeiden) luettelo.                                                                                  |
| Työtilaukset          | Avaa **Aktiivisten työtilaukset** -luettelosivu, jolla voit tarkastella resurssin työtilauksia.                                                                                        |
| Tarkistusluettelo            | Tarkastele resurssille kirjattujen kunnossapidon tarkistusluetteloiden ja mittausten yhteenvetoa.                                                                                                 |
| Ylläpidon käyttökatko | Luo tai tarkastele resurssin kunnossapitoseisokkeja koskevia rekisteröintejä.                                                                                                       |
| Projektitapahtumat | Näytä kaikki kirjatut tapahtumat, jotka liittyvät resurssille luotuihin työtilauksiin.                                                                                       |
| Resurssien mittarit       | Luo tai tarkastele resurssin mittauksia.                                                                                                               |
| Ylläpitoaikataulu | Avaa **Avaa ylläpitoaikataulu** -luetteloivu, jossa voit tarkastella resurssiin liittyviä ylläpitosuunnitelmia, ylläpitopyyntöjä ja ylläpitokierroksia, joiden tila on **Luotu**. |
| Päivitä resurssin tila   | Resurssin elinkaaren tilan päivittäminen. Voit valita useita resursseja **Kaikki resurssit** luettelosivulta ja päivittää sitten kaikkien resurssien elinkaaritilan samaan aikaan.              |
| Elinkaaren tilan loki  | Avaa loki, joka näyttää valitun resurssin elinkaaritilat.                                                                                                                 |
| Resurssin tiedostot      | Tarkastele valittuun resurssiin liitettyjen asiakirjojen luetteloa. Nämä asiakirjat määritetään kohdassa **Resurssien hallinta** \> **Asetukset** \> **Resurssin tiedostot**.                 |
| Ominaisuudet           | Luo tai näytä resurssin määritteet.                                                                                                                             |
| Kuva                | Valitse kuva resurssia varten.                                                                                                                                   |
| Ylätason resurssit        | Tarkastele valitun resurssin pääresurssin historiaa.                                                                                                                |
| Toiminnalliset sijainnit | Tarkastele valitun resurssin toiminnallisen sijainnin historiaa.                                                                                                          |
| Kunnon arviointi | Rekisteröi resurssin kunnon arviointimittaukset.                                                                                                         |
| Viat               | Avaa **resurssin viat** -luettelosivu, jolla voit tarkastella resurssille kirjattuja vikoja.                                                                                             |
| Kustannusseuranta         | Vertaa resurssin budjettikustannuksia ja todellisia kustannuksia.                                                                                                              |
| Tuntien hallinta         | Vertaa resurssin ennustetunteja ja todellisia tunteja.                                                                                                              |
| Resurssien suorituskykyilmaisimet           | Laske ja tarkastele resurssin suorituskykyilmaisimia.                                                                                              |
| Työtyypit            | Tarkastele resurssin nykyisten oletustyötyyppien yhteenvetoa.                                                                                                            |
| Kriittisyyden tyypit    | Näytä tai päivitä resurssin kriittisyystyyppejä.                                                                                                                              |
| Varaosat          | Tarkastele resurssiin käytettävissä olevien hyväksyttyjen ja vaihtoehtoisten varaosien luetteloa.                                                                               |
| Resurssien kulutus    | Tulosta raportti, joka sisältää resurssin kulutuksen rekisteröinnit.                                                                                                |
| Resurssin vika          | Tulosta raportti, joka sisältää resurssin vikarekisteröinnit.                                                                                                      |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]