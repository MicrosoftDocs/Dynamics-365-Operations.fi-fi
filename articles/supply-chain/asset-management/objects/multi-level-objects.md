---
title: Monitasoiset resurssit
description: Tässä ohjeaiheessa kerrotaan, kuinka voit luoda ja poistaa monitasoisia resursseja.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f43c7c97f8b05a1bf76b2f2c869e6868689f388d06337064f04af839f2403357
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769608"
---
# <a name="multi-level-assets"></a>Monitasoiset resurssit

[!include [banner](../../includes/banner.md)]

 

Tässä ohjeaiheessa kerrotaan, kuinka voit luoda ja poistaa monitasoisia resursseja. Voit luoda resursseja ja niihin liittyviä alaresursseja hierarkkisessa puurakenteessa. Näin voit näyttää suhteet ja riippuvuudet resurssien välillä. Ylläpitotöitä voidaan liittää kaikkiin puurakenteen tasoihin. Tilastoja voidaan luoda myös yksittäiselle tasolle tai kaikkien aliresurssitasojen summana.

**Kaikki resurssit** -luettelosivun (**Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit**) **Resurssi**-sarakkeessa on resurssit hirarkkisessa jäsjestyksessä. **Ylätaso**-sarakkeessa näkyy liittyvä ylätaso. Lisäksi jos resurssit ja aliresurssit on jo luotu,**Liittyvät tiedot** -ruudun **Resurssipuu**-osassa näkyvät resurssit puurakenteessa.

Lisä tietoja resurssien luomisesta on kohdassa [Resurssin luominen](../objects/create-an-object.md). Jos haluat luoda aliresurssin, valitse ylätason resurssi **Ylätaso**-kentässä **Yleiset**-pikavälilehdessä.

## <a name="copy-an-asset-or-asset-structure"></a>Kopioi resurssi tai resurssirakenne

Jos yritykselläsi on useita samankaltaisia resurssirakenteita, voit luoda ne nopeasti käyttämällä resurssien hallinnan Kopioi-toimintoa.

1. Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit**.
2. Valitse **Kaikki resurssit** -luettelosivulla kopioitava resurssi. Jos esimerkiksi haluat kopioida koko resurssirakenteen, mukaan lukien aliresurssit, valitse ylätason resurssi.
3. Valitse **Kopioi resurssi**. **Kopioi kohteesta**-osassa **Resurssi**-kentän arvoksi on valittu resurssi, jonka valitsit luettelosivulla.
4. Kirjoita **Kopioi kohteeseen** -osassa **Resurssi**-kenttään uuden resurssin nimi.
5. Jos luotavalla resurssin on oltava osa aiemmin luotua resurssirakennetta, valitse **Ylätason resurssi** -osan **Resurssi** -kentässä ylätason tunnus.
6. Valitse **OK**. Uusi resurssirakenne näkyy **Kaikki resurssit** -luettelosivulla. Kaikki resurssin määritteet, ylläpitosuunnitelmat ja kunnossapitokierrokset, jotka liittyvät kopioimaasi resurssiin, siirretään uuteen resurssiin tai resurssirakenteeseen.

Kun kopioit resurssirakenteen, uuden rakenteen alivresursseilla on sama nimi kuin kopioimillasi aliresursseilla. Kun kopiointitoiminto on valmis, voit helposti muuttaa resurssin nimeä ja muita asetuksia. Valitse resurssi **Kaikki resurssit** -luettelosivulla ja valitse sitten **Muokkaa**-painike.

> [!NOTE]
> Kun kopioit resurssin tai resurssirakenteen, uusien resurssien elinkaaritila palautetaan mihin tahansa tilaan, jonka olet määrittänyt resurssien elinkaaren alkutilaksi. Toiminnallinen sijainti palautetaan oletusarvoiseen toiminnalliseen sijaintiin.

## <a name="delete-an-asset-or-asset-structure"></a>Poista resurssi tai resurssirakenne

Jos resurssiin liittyy alaresursseja, voit poistaa sen vain, jos mihinkään resurssiin ei ole rekisteröity ylläpitopyyntöjä, työtilaustöitä, vikarekisteröintejä tai kunnon arviointeja.

1. Valitse **Kaikki resurssit** -luettelosivulla poistettava resurssi.
2. Valitse **Poista**.

> [!NOTE]
> Jos et voi poistaa resurssia tämän menettelyn avulla, toinen tapa käsitellä poistoa on määrittää resurssin elinkaaren tila tätä tarkoitusta varten. Voit esimerkiksi määrittää elinkaareen **Hävikki**- tai **Poistettu**-tilan **Resurssien elinkaaritilat** -sivulla.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]