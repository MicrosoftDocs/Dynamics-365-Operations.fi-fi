---
title: Toiminnallisen sijainnin tyypit
description: Tässä ohjeaiheessa kerrotaan toiminnallisten sijaintien tyyppien luonnista resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0468cb0b1717b7cf0ccb391da09a4e7d788124f3
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812211"
---
# <a name="functional-location-types"></a>Toiminnallisen sijainnin tyypit

[!include [banner](../../includes/banner.md)]

 

Tässä ohjeaiheessa kerrotaan toiminnallisten sijaintien tyyppien luonnista resurssien hallinnassa. Toiminnallisten sijaintityyppien avulla hallitaan toiminnallisten sijaintien vaatimuksia, kuten sitä, miten resurssit asennetaan toiminnallisessa sijainnissa. Voit määrittää resurssityyppejä, ylläpitosuunnitelmia, toiminnallisia sijaintimääritteitä ja resurssin määrite vaatimuksia, joita käytetään tiettyä toiminnallista sijaintityyppiä käyttävässä toiminnallisessa sijainnissa. Kun luot toiminnallisen sijainnin, toiminnallisen sijainnin tyyppi on pakollinen.

>[!NOTE] 
>Jotta voit käyttää toiminnallisia sijainteja, sinun on luotava toiminnallinen oletussijainti, jota käytetään vain uusien resurssien luomiseen. Oletusarvoiselle toiminnalliselle sijainnille on luotava oletustoiminnallinen sijaintityyppi, joka on todella yksinkertainen, ja sallii useiden resurssien asentamisen oletusarvoiseen toiminnalliseen sijaintiin. Lisätietoja toiminnallisten sijaintien määrittämisestä on kohdassa [Luo toiminnallisia sijainteja](../functional-locations/create-functional-locations.md).

## <a name="create-a-default-functional-location-type"></a>Toiminnallisen sijainnin oletustyypin luominen

Tässä kuvataan, miten luodaan oletusarvoinen toiminnallinen sijaintityyppi, jota käytetään toiminnallisessa oletussijainnissa.

1. Valitse **Resurssien hallinta** > **Asetukset** > **Toiminnalliset sijainnit** > **Toiminnallisten sijaintien tyypit**.
2. Luo uusi toiminnallisen sijainnin tyyppi valitsemalla **Uusi**.
3. Lisää toiminnallisen sijaintityypin tunnus **Toiminnallisen sijainnin tyyppi** -kenttään, esimerkiksi "Oletus", ja nimi **Nimi**-kenttään.
4. Valitse elinkaarimalli **Toiminnallisen sijainnin elinkaarimalli** -kentässä.
5. Valitse "Kyllä" **Useita resursseja** -vaihtopainikkeesta, jos haluat sallia useamman resurssin asentamisen toiminnallisessa sijainnissa (oletustoimintosijainnissa) tätä tyyppiä käyttäen.

Nyt luodaan oletusarvoinen toiminnallinen sijaintityyppi, jota käytetään vain toiminnallisessa oletussijainnissa. Älä lisää tähän oletustoimintosijainnin tyyppiin enempää vaatimuksia tai rajoituksia.


## <a name="create-functional-location-types"></a>Luo toiminnallisen sijainnin tyypit

1. Valitse **Resurssien hallinta** > **Asetukset** > **Toiminnalliset sijainnit** > **Toiminnallisten sijaintien tyypit**.
2. Luo uusi toiminnallisen sijainnin tyyppi valitsemalla **Uusi**.
3. Lisää toiminnallisen sijaintityypin tunnus **Toiminnallisen sijainnin tyyppi** -kenttään ja nimi **Nimi**-kenttään.
4. Valitse elinkaarimalli **Toiminnallisen sijainnin elinkaarimalli** -kentässä. Lisätietoja toiminnallisten sijaintien elinkaaritiloista ja elinkaarimalleista on kohdassa [Toimintosijainnin elinkaaritilat](../setup-for-functional-locations/functional-location-stages.md).
5. Valitse "Kyllä" **Useita resursseja** -vaihtopainikkeesta, jos haluat mahdollistaa useamman resurssin asentamisen toiminnallisessa sijainnissa käyttäen tätä toiminnallisen sijainnin tyyppiä. Jos valitset vaihtoehdon "Ei", voit asentaa vain *yhden* resurssin toiminnallisessa sijainnissa käyttämällä tätä toiminnallista sijaintityyppiä.
6. Valitse **Päivitä resurssin dimensio** -vaihtopainikkeessa "Kyllä", jos haluat, että tämän tyypin toiminnallisessa sijainnissa asennettuna olevat resurssit käyttävät automaattisesti kyseiseen toimintosijaintiin liittyviä taloushallinnon dimensioita. Tämä tarkoittaa, että jos muutat taloushallinnon dimensioita [Toiminnallisten sijaintien luominen](../functional-locations/create-functional-locations.md) -lomakkeessa ja toiminnallisessa sijainnissa on käytössä toiminnallinen sijaintityyppi, jossa tämä vaihtopainike on asennossa Kyllä, taloushallinnon dimensiot päivitetään automaattisesti kaikkiin kyseiseen toiminnalliseen sijaintiin asennettuihin resursseihin.
7. **Resurssityyppi**-kenttää käytetään, jos haluat luoda toimintosijainnille automaattisesti *yhden* resurssin, jolla on sama tunnus ja nimi kuin luotavalla toiminnallisella sijainnilla. Tämä voi olla tarpeen esimerkiksi, jos luot staattisen funktionaalisen sijainnin, kuten rakennuksen tai putkiston. Valitse tällöin resurssityyppi, jota haluat käyttää automaattisesti luodussa resurssissa. Muista, että jos teet valinnan tässä kentässä, **Useita resursseja** -vaihtoainikkeeksi on määritettävä "Ei".
8. Valitse **Resurssityypit**-pikavälilehdessä resurssityypit, jotka liittyvät toiminnalliseen sijaintityyppiin. Valitse **Lisää rivi** ja valitse resurssityypit. Jos lisäät resurssityypit tähän, vain näitä resurssityyppejä käyttävät resurssit voidaan asentaa toiminnalliseen sijaintiin käyttämällä tätä toimintosijaintityyppiä. Jos resurssityyppejä ei valita **resurssityypit**-pikavälilehdessä, kaikkia resurssityyppejä voidaan asentaa.
9. Valitse **Ylläpitosuunnitelmat**-pikavälilehdessä ylläpitosuunnitelmat, jotka määritetään automaattisesti uusille toiminnallisille sijainneille käyttämällä tätä toimintosijaintityyppiä. Valitse **Lisää rivi** ja valitse ylläpitosuunnitelmat. Jos lisäät huoltosuunnitelmia tähän, vain näitä suunnitelmia voidaan käyttää toiminnallisessa sijainnissa, jotka käyttävät tätä toimintosijaintityyppiä.
10. Määritä **Resurssimääritteiden vaatimukset** -pikavälilehdessä resurssimääritteet, jotka määritetään automaattisesti uusille toiminnallisille sijainneille käyttämällä tätä toimintosijaintityyppiä. Valitse **Lisää rivi** ja valitse määrite. Nämä määritevaatimukset toimivat ohjeina. Niitä ei tarkisteta resurssiin määritettyihin määritteisiin verraten (**Resurssien hallinta** > **Yhteiset** > **Resurssit** > **Kaikki resurssit** > valitse resurssi luettelosivlla > **Yleiset**-välilehti > **Määritteet**-painike). Määriteaatimukset näytetään, kun resursseja asennetaan toiminnallisiin sijainteihin.
11. Valitse **Sallitut tyypit** -pikavälilehdellä toiminnalliset sijaintityypit, joiden pitäisi olla voimassa ylemmän tason toiminnallisen sijainnin tyyppiin liittyvissä toiminnallisissa alisijaintityypeissä, jotka käyttävät valittua toiminnallisen sijainnin tyyppiä.
12. Valitse **Määritteet**-pikavälilehdessä toiminnallisen sijainnin määritteet, jotka määritetään automaattisesti uusille toiminnallisille sijainneille käyttämällä tätä toimintosijaintityyppiä. Valitse **Lisää rivi** ja valitse määrite.


>[!NOTE] 
>**Yleiset**-pikavälilehdessä voit saada yleiskatsauksen resurssityyppien määrästä, ylläpitosuunnitelmista, resurssimääritteiden vaatimuksista, sallituista tyypeistä, määritteistä ja toiminnallisista sijainneista, jotka on määritetty toiminnallisen sijainnin tyypissä. **Toiminnalliset sijainnit** -kentässä näkyy niiden toiminnallisten sijaintien määrä, jotka käyttävät tätä toimintosijaintityyppiä. **Kopioi**-painikkeen avulla voit kopioida asetukset toiminnallisen sijainnin tyypistä valittuun toiminnallisen sijainnin tyyppiin.
