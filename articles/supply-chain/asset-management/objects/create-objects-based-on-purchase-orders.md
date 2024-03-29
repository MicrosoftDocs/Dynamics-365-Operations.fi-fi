---
title: Luo ostotilauksiin perustuvia resursseja
description: Tässä artikkelissa kerrotaan, kuinka voit luoda luettelon resursseista, joita voidaan käyttää perustana luotaessa resursseja resurssien hallinnan kunnossapitotöille.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccd14493aac6484dc54ccf51ae159a071c8697a5
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015606"
---
# <a name="create-assets-based-on-purchase-orders"></a>Luo ostotilauksiin perustuvia resursseja

[!include [banner](../../includes/banner.md)]

 

Tässä artikkelissa kerrotaan, kuinka voit luoda luettelon resursseista, joita voidaan käyttää perustana luotaessa resursseja resurssien hallinnan kunnossapitotöille. Resurssien perusteella voit tarkastella luetteloa ostotilausriveistä, jotka on luotu kyseisiin nimikkeisiin. Tämän toiminnon tarkoituksena on helposti luoda resurssi resurssien hallinnassa ostotilauksen perusteella.

Ensin määritetään nimikkeet, joita käytetään resurssien luomiseen ostotilauksesta kohdassa **Resurssinimikkeet**. Kun olet luonut ostotilausrivin, voit luoda resurssit **Odottavat resurssit** -kohdassa. On mahdollista päättää, missä ostotilauksen vaiheessa resurssi on luotava.


## <a name="select-asset-items"></a>Valitse resurssinimikkeet

1. Valitse **resurssien hallinta** > **Asetukset** > **resurssit** > **nimikkeet**.
2. Luo uusi resurssinimike napsauttamalla **Uusi**.
3. Valitse **Nimiketunnus**-kentässä nimike. Kun poistut kyseisestä kentästä, nimikkeen nimi lisätään automaattisesti **Tuotteen nimi** -kenttään.
4. Valitse **Yleiset**-pikavälilehdessä nimikkeen resurssityyppi.
5. Valitse nimikkeelle resurssin valmistaja ja malli.
6. Tallenna nimike.


## <a name="create-assets-from-pending-assets"></a>Resurssien luominen odottavista resursseista

1. Valitse **Resurssien hallinta** > **Resurssit** > **Odottavat resurssit**.
2. Näet päivitetyn luettelon ostotilauksista, jotka perustuvat **resurssinimikkeet** -kohdassa valittuihin nimikkeisiin.
3. Voit suodattaa ostotilausten tiloja ja valita, missä elinkaaren tilassa resurssi luodaan. Haluat ehkä esimerkiksi luoda resursseja vain, kun tuotteen vastaanotto on kirjattu ostotilaukseen.
4. Valitse ostotilausrivin **Viitenumero**-linkki, jos haluat tarkastella nimikkeen yksityiskohtaisia tietoja.
5. Jos haluat muokata, mitkä dimensiot näkyvät **varastodimensiot**-pikavälilehdessä, napsauta **Näytä dimensiot** -painiketta ja tee valintasi.
6. Jos haluat luoda resurssin ostotilausrivin perusteella, valitse luettelo sivulla kyseisen rivin **Merkitse**-sarakkeen valintaruutu ja valitse sitten **Luo resurssit.** Näyttöön tulee sanoma, jossa ilmoitetaan resurssin tunnus.
7. Valitse resurssi **Kaikki resurssit** -luettelosta ja valitse **Muokkaa** lisätäksesi lisätietoja resurssiin.
8. Jos haluat poistaa rivin **Odottavat resurssit** -kohdassa, koska et halua luoda resurssia, valitse kyseisen rivin **Merkitse**-sarakkeen valintaruutu ja valitse **Hylkää odottavat resurssit**. Näyttöön tulee sanoma, jossa ilmoitetaan resurssin tunnus. Et poista ostotilausta tai myyntitilausta, vaan vain sen tietueen, josta olet voinut luoda resurssin **resurssien hallinnassa**.

>[!NOTE]
>Kaikki tuotedimensiot (koko, väri, konfiguraatio jne.) siirretään automaattisesti resurssin määritteisiin. Seurantadimensiot (sarjanumerot) tallennetaan suoraan resurssiin, kun resurssi luodaan.


## <a name="find-pending-assets"></a>Odottavien resurssien etsiminen

Voit tarkistaa odottavat resurssit suorittamalla **Odottavien resurssien määrä** -toiminnon. Tätä toimintoa voidaan käyttää esimerkiksi ilmoituksen vastaanottamiseen aina, kun odottava resurssi on valmis luotavaksi resurssina.

1. Valitse **resurssien hallinta** > **Kausittainen** > **resurssit** > **Odottavien resurssien määrä**.
2. Suorita työ valitsemalla **OK** ja luettelo päivittyy kohdassa **Odottavat resurssit**.
3. Voit määrittää tämän työn suoritettavaksi erätyönä, esimerkiksi kerran päivässä.

**Varoitus:** jos tietoja muutetaan ostotilauksessa *sen jälkeen*, resurssi on luotu nimikkeeseen perustuen, kyseiset muutokset eivät vaikuta resurssiin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]