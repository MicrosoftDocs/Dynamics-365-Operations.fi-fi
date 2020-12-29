---
title: Resurssien siirtäminen, korvaaminen ja asentaminen
description: Tässä ohjeaiheessa kerrotaan, miten resursseja siirretään, korvataan ja asennetaan resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec150adb35eb0600844245b14cbec9e9632ab337
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427130"
---
# <a name="move-replace-and-install-assets"></a>Resurssien siirtäminen, korvaaminen ja asentaminen

[!include [banner](../../includes/banner.md)]

 

Tässä ohjeaiheessa kerrotaan, miten resursseja siirretään, korvataan ja asennetaan resurssien hallinnassa. Voit luoda yksittäisiä resursseja, joilla ei ole suhteita muihin resursseihin, tai voit luoda resurssirakenteen, joka sisältää pääresurssin (ylätason resurssi) ja siihen liittyvät aliresurssit. Resurssien hallinnassa on kolme lähestymistapaa, joilla resurssin sijaintia siirretään ja muutetaan:

- **Siirrä** – Siirrä resurssi joko toiseen resurssirakenteeseen tai toiseen sijaintiin samassa resurssirakenteessa.
- **Korvaa** – Poista resurssi resurssirakenteesta tilapäisesti, jotta se voidaan korjata tai kunnostaa, ja lisätä sitten kunnostettu resurssi takaisin resurssirakenteeseen myöhemmin. Vaihtoehtoisesti voit korvata käytetyn resurssin pysyvästi uudella resurssilla.
- **Asenna** – Asenna pääresurssi ja kaikki siihen liittyvät aliresurssit toiminnalliseen sijaintiin.

> [!NOTE]
> Siirrettävä, korvattava tai asennettava resurssi saattaa liittyä toiseen toiminnalliseen sijaintiin. Tässä tapauksessa resurssi voi käyttää toiminnallisen sijainnin taloushallinnon dimensioita. **Toiminnallisen sijainnin tyypit** -sivulla voit määrittää taloushallinnon dimensioiden käsittelyn toiminnallisissa sijainneissa.

## <a name="move-asset"></a>Siirrä resurssi

Käytä **Siirrä resurssi** -toimintoa siirtääksesi resurssin joko toiseen resurssirakenteeseen tai toiseen sijaintiin samassa resurssirakenteessa. Voit myös siirtää resurssin pois resurssirakenteesta niin, että siitä tulee itsenäinen resurssi, jolla ei ole rakennesuhteita.

> [!NOTE]
> Älä käytä tätä toimintoa, jos resursseja korjataan tai vaihdetaan väliaikaisesti. Käytä sen sijaan **Korvaa resurssi** -toimintoa, joka on kuvattu myöhemmin tässä ohjeaiheessa.

1. Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit** tai **Aktiiviset resurssit**.
2. Valitse luettelosta siirrettävä resurssi. Jos resurssilla on aliresursseja, siirrät myös kyseiset resurssit.
3. Valitse **Siirrä resurssi**.
4. Jos haluat siirtää resurssin siten, että siitä tulee osa resurssirakennetta, valitse uusi pääresurssi **Pääresurssi**-kentässä. Jos siirrät alatason resurssin ja haluat tehdä siitä erillisen resurssin, jolla ei ole rakennesuhteita, jätä **Pääresurssi**-kenttä tyhjäksi.
5. **Voimassa**-kenttään valitaan oletusarvoisesti nykyinen päivämäärä ja aika. Voit kuitenkin valita eri päivämäärän ja ajan, josta lähtien resurssin siirto on voimassa.
6. Valitse **OK**.

## <a name="replace-asset"></a>Korvaa resurssi

Käytä **Korvaa resurssi** -toimintoa resurssin korjausten, kunnostuksen tai kuluneen resurssin pysyvän korvaamisen uudella resurssilla yhteydessä. Tätä funktiota käytetään korvaamaan resurssirakenteen alieliresurssit. Pääresursseille (eli resursseille, joilla ei tällä hetkellä ole pääresurssia) tämä korvaus tehdään toiminnallisessa sijainnissa. Lisätietoja toiminnallisen sijainnin pääresurssien korvaamisesta on kohdassa [Resurssien asentaminen toiminnallisiin sijainteihin](../functional-locations/install-objects-on-functional-locations.md).

> [!NOTE]
> Jos korjausosasto liittyy tuotanto-osastoosi, voit luoda toiminnallisia sijainteja, kuten **Korjaus**, **Hävikki** ja **Varastointi**, jotta voidaan käsitellä resurssien korjausta ja korvaamista.

1. Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit** tai **Aktiiviset resurssit**.
2. Valitse luettelosta korvattava aliresurssi. Jos resurssilla on aliresursseja, korvaat myös kyseiset resurssit.
3. Valitse **Korvaa resurssi**.

    **Rakenne on muuttunut** -kentässä näkyy viimeisin päivämäärä ja aika, jolloin valittu resurssi ja siihen liittyvät aliresurssit siirrettiin resurssirakenteeseen.

4. Valitse **Valittu resurssi** -osan **Toiminnallinen kohdesijainti** -kentässä toiminnallinen sijainti, johon resurssi siirretään. Valitse esimerkiksi sijainniksi **Korjaus** tai **Hävikki**.

    **Pääresurssi**-osan **Voimassa**-kentässä näkyy viimeisin päivämäärä ja aika, jolloin pääresurssi ja siihen liittyvät aliresurssit on asennettu tai siirretty nykyiseen toiminnalliseen sijaintiin.

5. Valitse **Uusi resurssi** -osion **Resurssi**-kentässä resurssi, joka lisätään väliaikaisena tai pysyvänä korvaavana resurssina valitulle resurssille. Tämä resurssi saattaa tällä hetkellä sijaita toisessa toiminnallisessa sijainnissa, kuten **Varastointi**.
7. **Voimassa lähtien** -osan **Voimassa**-kenttään valitaan oletusarvoisesti nykyinen päivämäärä ja aika. Voit kuitenkin valita eri päivämäärän ja ajan, josta lähtien resurssin korvaaminen on voimassa.
8. Valitse **OK**.

## <a name="install-asset"></a>Asenna resurssi

Käytä **Asenna resurssi** -toimintoa resurssirakenteen asentamiseen toiminnalliseen sijaintiin.

> [!NOTE]
> Valitse aina pääresurssi. Pääresurssi ja siihen liittyvät aliresurssit siirretään valittuun toiminnalliseen sijaintiin.

1. Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit** tai **Aktiiviset resurssit**.
2. Valitse luettelosta pääresurssi, joka asennetaan toiseen toiminnalliseen sijaintiin.
3. Valitse **Asenna resurssi**.

    **Määritteet**-osassa näkyvät resurssimääritteet, jotka on määritetty pääresurssille.

4. Valitse uusi sijainti **Toiminnallinen sijainti** -kentässä.
5. **Voimassa**-kenttään valitaan oletusarvoisesti nykyinen päivämäärä ja aika. Voit kuitenkin valita eri päivämäärän ja ajan, josta lähtien resurssin asentaminen resurssirakenteeseen on voimassa.
6. Valitse **OK**.
