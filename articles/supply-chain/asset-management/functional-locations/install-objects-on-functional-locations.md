---
title: Asenna toiminnallisten sijaintien resurssit
description: Tässä ohjeaiheessa kerrotaan, miten resursseja asennetaan toiminnallisiin sijainteihin resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationObjectChange, EntAssetFunctionalLocationObjectInstall, EntAssetFunctionalLocationObject
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ea67e2392d8e25a2a5f3cb7e1ff5032322f2c48
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022027"
---
# <a name="install-assets-on-functional-locations"></a>Asenna toiminnallisten sijaintien resurssit

[!include [banner](../../includes/banner.md)]

 

Kun olet luonut toiminnalliset sijaintirakenteet, seuraava vaihe on asentaa resurssit asiaankuuluviin toiminnallisiin sijainteihin. Tässä ohjeaiheessa kerrotaan, miten resursseja asennetaan näihin toiminnallisiin sijainteihin resurssien hallinnassa. Lisätietoja resurssien luomisesta on kohdassa [Resurssien esittely](../objects/introduction-to-objects.md).

Jos olet luonut resurssirakenteen, koko resurssirakenne on asennettava toiminnalliseen sijaintiin. Tämän vuoksi toiminnalliseen sijaintiin voidaan valita vain pääresursseja (ylätason resurssit, joilla ei ole pääresursseja). Kaikki liittyvät aliresurssit asennetaan myös kyseiseen toiminnalliseen sijaintiin. Kun asennat resursseja toiminnalliseen sijaintiin, toiminnallisen sijainnin taloushallinnon dimensiot voidaan siirtää niille automaattisesti toiminnalliseen sijaintiin valitun toiminnallisen sijaintityypin asetusten mukaan. Lisätietoja toiminnallisten sijaintityyppien määrittämisestä on kohdassa [Toiminnalliset sijaintityypit](../setup-for-functional-locations/functional-location-types.md).

> [!NOTE]
> Voit määrittää resurssityyppejä toiminnallisen sijainnin tyypille, jota käytetään toiminnalliseen sijaintiin. Tässä tapauksessa, kun asennat resursseja toiminnalliseen sijaintiin, vain sellaiset pääresurssit, joilla on sama resurssityyppi, näkyvät niiden resurssien luettelossa, jotka voidaan asentaa kyseiseen toiminnalliseen sijaintiin.

Kun olet asentanut resursseja toiminnalliseen sijaintiin, voit korvata pääresurssin tai resurssirakenteen, kuten tarvitset. Kun asennat resursseja, valitse korvattava pääresurssi. Myös kaikki liittyvät alatason resurssit korvataan. 


## <a name="install-an-asset-structure-on-a-functional-location"></a>Resurssirakenteen asentaminen toiminnalliseen sijaintiin

1. Valitse **resurssien hallinta** \> **Yhteiset** \> **Toiminnalliset sijainnit** \> **Kaikki toiminnalliset sijainnit** tai **Aktiiviset toiminnalliset sijainnit**.
2. Valitse toiminnallinen sijainti, johon resurssi asennetaan.
3. Valitse **Asenna resurssi**.

    **Määritteet**-osassa on luettelo resurssimääritteen vaatimuksista, jotka on määritetty toiminnalliselle sijainnille valitulle toiminnalliselle sijaintityypille. Määritteet on tarkoitettu vain tiedoksi. Järjestelmä ei vahvista määritteitä niiden resurssimääritteiden perusteella, jotka on määritetty resurssille asennettaessa. Sinun on tehtävä oikeellisuustarkistus, kun olet valinnut resurssin **Resurssi**-kentässä.

4. Valitse **resurssi**-kentässä asennettava pääresurssi. Kaikki liittyvät aliresurssit sisällytetään automaattisesti asennukseen.

    **Resurssimääritteet** -osassa resurssiluettelon oikealla näkyvät valittuun resurssiin liittyvät resurssimääritteet.

5. Valitse **Voimassa**-kentässä päivämäärä ja aika, josta lähtien resurssin asennus on voimassa. Kyseisen päivämäärän ja ajan jälkeen resurssin ja siihen liittyvien aliresurssien kustannukset liittyvät toiminnalliseen sijaintiin.

    > [!NOTE]
    > Resurssille määritetyt määritteet lisätään **Määritteet**-osaan. Esimerkiksi **Paino**-määritteen vaatimus on lisätty vaatimuksena sekä resurssille että toiminnalliselle sijainnille. Jos resurssin määritevaatimukset ovat samaa tyyppiä kuin toiminnallinen sijainti, **Arvo**-kenttiin syötetään resurssin määritevaatimusten arvot. Tämän vuoksi voit vahvistaa resurssin arvot niiden määritevaatimusten perusteella, jotka on määritetty toiminnalliseen sijaintiin. Määritevaatimukset, jotka on määritetty toiminnalliseen sijaintiin on merkitty rastilla.

6. Valitse **OK**.

    > [!NOTE]
    > Voit muuttaa resurssin asennusta asentamalla sen uuteen toiminnalliseen sijaintiin noudattamalla tämän toimenpiteen vaiheita 1–6. Kun asennat resurssin uuteen toiminnalliseen sijaintiin, resurssi poistetaan automaattisesti edellisestä toiminnallisesta sijainnista. Kaikki aktiiviset ylläpitopyynnöt tai työtilaukset, jotka on luotu resurssille ennen sen asentamista uuteen toiminnalliseen sijaintiin, **eivät** siirry automaattisesti uuteen toiminnalliseen sijaintiin. Jos resurssin ylläpitopyynnöt ja työtilaukset ovat edelleen pakollisia, ne on luotava manuaalisesti uudelleen sen jälkeen, kun resurssi on asennettu uuteen sijaintiin.

7. Jos haluat tarkastella kaikkien toiminnalliseen sijaintiin asennettuja resursseja (ml. aliresurssit) valitse toiminnallinen sijainti **Kaikki toiminnalliset sijainnit** -sivulla ja valitse sitten **Resurssit**.
8. Nähdäksesi luettelon aktiivisista ylläpitopyynnöistä, aktiivisista työtilauksista tai vikarekisteröinneistä, jotka liittyvät toiminnalliseen sijaintiin asennettuihin resursseihin, valitse toiminnallinen sijainti **Kaikki toiminnalliset sijainnit** -sivulla ja valitse **Pyynnöt**, **Työtilaukset** tai **Viat**.

> [!NOTE]
> Kun resurssiin liittyviä tietoja muutetaan, se päivitetään automaattisesti toiminnalliseen sijaintiin, johon resurssi on asennettu. Tämä automaattinen päivitys koskee kunnossapitopyyntöjen, työtilausten, resurssin vikarekisteröintien, kunnossapitokatkoksien rekisteröintien ja resurssien mittausrekisteröintien muutoksia.

## <a name="automatically-create-one-asset-on-a-functional-location"></a>Luo yksi resurssi automaattisesti toiminnalliseen sijaintiin

Voit määrittää toiminnallisen sijainnin vaiheita ja toiminnallisia sijaintityyppejä, jotka käsittelevät *yhden* resurssin automaattista luomista toiminnalliseen sijaintiin. Resurssi saa saman tunnuksen ja nimen kuin toiminnallinen sijainti. Tämä toiminto voi olla hyödyllinen, kun käsittelet kunnossapitoa suuressa, staattisessa resurssissa, kuten rakennuksessa.

Ennen kuin voit luoda resurssin automaattisesti toiminnalliseen sijaintiin, seuraavien asetustietojen on oltava käytettävissä:

- Luo toiminnallinen sijaintityyppi, joka käsittelee resurssin automaattista luomista. Valitse **Resurssittyyppi** -kentässä resurssityyppi. Lisätietoja on kohdassa [Toiminnalliset sijaintityypit](../setup-for-functional-locations/functional-location-types.md).
- Luo toiminnallisen sijainnin elinkaaren tila, joka käsittelee resurssin automaattista luomista. Määritä **Luo resurssi** -asetukseksi **Kyllä**. Lisätietoja on kohdassa [Toiminnallisen sijainnin elinkaaren tilat](../setup-for-functional-locations/functional-location-stages.md).

Kun asetustiedot ovat käytettävissä, olet valmis luomaan resurssin.

1. Varmista **Kaikki toiminnalliset sijainnit** -sivulla, että toiminnallinen sijainti, johon haluat luoda automaattisesti resurssin, käyttää tätä tarkoitusta varten luomaasi toiminnallisen sijainnin tyyppiä.
2. Valitse luettelosta toiminnallinen sijainti.
3. Valitse **Päivitä toiminnallisen sijainnin tila** ja valitse sitten sen elinkaaren tila, jonka loit tätä tarkoitusta varten. Yksi resurssi asennetaan nyt automaattisesti toiminnalliseen sijaintiiin. Resurssi saa saman tunnuksen ja nimen kuin toiminnallinen sijainti.
