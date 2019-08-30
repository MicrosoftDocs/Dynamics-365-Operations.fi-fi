---
title: Luo ylläpitopyyntöjä
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpitopyynnöt luodaan resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 03e090633276cd264ad03f561ddb425a9816357e
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847502"
---
# <a name="create-maintenance-requests"></a>Luo ylläpitopyyntöjä

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Ylläpitopyyntöjä voidaan käyttää, jos huoltotyöntekijät tai tuotannon työntekijät saavat selville, että laitteet vaativat korjausta, mutta korjaustyötä ei voi tehdä heti.

**Esimerkki:** Kun kunnossapitotyöntekijä tekee korjauksen, hän havaitsee, että samassa sijainnissa on huollettava toinenkin resurssi. Huoltotyöntekijällä ei kuitenkaan ole aikaa tai tarvittavia varaosia korjaustyön tekemistä varten. Tämän vuoksi hän luo resurssille ylläpitopyynnön ja kirjoittaa ongelmasta lyhyen kuvauksen.

**Aktiiviset ylläpitopyynnöt** -osa **Aiheeseen liittyviä tietoja** -ruudussa **Kaikki resurssit**- tai **Aktiiviset resurssit** -sivulla (**Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit** tai **Aktiiviset resurssit**) näyttää aktiiviset ylläpitopyynnöt, jotka on liitetty valittuuun resurssiin.

1. Valitse **Resurssien hallinta** \> **yhteiset** \> **Ylläpitopyynnöt** \> **Kaikki ylläpitopyynnöt** ta **Aktiiviset ylläpitopyynnöt**.
2. Valitse **Uusi**.
3. Valitse **Luo pyyntö** -valintaikkunan **Ylläpitopyynnön tyyppi** -kentässä ylläpitopyynnön tyyppi. Ehdotetaan oletustyyppiä.
4. Kirjoita **kuvaus**-kenttään nimi tai otsikko, joka kuvaa lyhyesti ylläpitopyyntöä.
5. Valitse **toiminnallinen sijainti**- ja **resurssi**-kentissä toiminnallinen sijainti tai resurssi tai toiminnallisen sijainnin ja resurssin yhdistelmä, kuten tarvitset. Voit luoda ylläpitopyynnön valitsematta resurssia, ja resurssi voidaan lisätä ylläpitopyyntöön myöhemmin. Jos kunnossapitotyöntekijä, joka on kirjautuneena Microsoft Dynamics 365 for Finance and Operationsiin, liittyy resurssiin, joka liittyy resurssiin **Resurssi**-kenttä määritetään automaattisesti.

    Jos valittuun resurssiin on jo liitetty ylläpitopyyntö, **Luo pyyntö** -valintaikkunan yläosassa näkyy sanomapalkki, joka ilmoittaa olemassa olevan ylläpitopyynnön tunnuksesta. Sanomapalkki ilmoittaa myös, jos resurssi kuuluu takuusopimuksen piiriin.

6. Valitse **Palvelutaso**-kentässä palvelutasto, joka ilmaisee pyynnön kiireellisyyden.
7. Jos valitsit resurssin vaiheessa 5, voit luoda vikarekisteröinnin käyttämällä kenttiä **Vian oire**, **Vika-alue** ja **Vikatyyppi**.
8. Jos huoltopyyntö on aiheuttanut huoltokatkoksia, anna seisonta-ajan alkamispäivä ja -aika.

    **Aloittanut** -kentän arvoksi määritetään automaattisesti nimesi.

10. **Toteutunut aloitus** -kenttään valitaan automaattisesti nykyinen päivämäärä ja aika. Voit kuitenkin muuttaa arvoa tarpeen mukaan.
11. Kirjoita **Huomautukset**-kenttään tarvittavat lisähuomautukset.
12. Valitse **OK**.

![Kuva 1](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a>Kunnossapitopyyntöjen myöhempi käsittely

Kun ylläpitopyyntö on luotu, mutta ennen kuin se muunnetaan työtilaukseksi, siihen tulee päivittää erilaisia tietoja. Yleensä suunnittelija tai muu hallinnollinen työntekijä suorittaa tämän tehtävän.

- Valitse **Kaikki ylläpitopyynnöt**- tai **Aktiiviset ylläpitopyynnöt** -sivulla haluamasi pyyntö ja valitse sitten **Muokkaa** .

Tiedot-näkymässä voit päivittää erilaisia tietoja. Seuraavassa on muutamia esimerkkejä:

- Valitse ja vahvista resurssi. Jos sinun on valittava toinen resurssi myöhemmin, voit määrittää **Resurssi vahvistettu** -asetukseksi **Ei**.
- Valitse vastuullinen kunnossapitotyöntekijäryhmä ja/tai vastuullinen huoltotyöntekijä. Lisätietoja vaadittavista asetuksista on kohdassa [Vastuulliset kunnossapitotyöntekijät](../setup-for-maintenance-requests/responsible-workers.md).
- Valitse kunnossapitotyön tyyppi ja, jos nämä tiedot ovat merkityksellisiä, liittyvä kunnossapitotyön variantti ja työn toimiala.
- Kirjoita **Leveysaste**- ja **Pituusaste**-kenttiin maantieteelliset koordinaatit. Kaikki ylläpitopyyntöön lisätyt koordinaatit siirretään automaattisesti liittyvään työtilaukseen. 

![Kuva 2](media/04-manage-maintenance-requests.png)

> [!NOTE]
> Jos valitset resurssin, kun luot ylläpitopyynnön, voit lisätä resurssiin yhden virheen. Kun kunnossapitopyyntö on luotu, voit lisätä vikoja, kuten tarvitset. Jos haluat lisätä vikoja, valitse **Resurssin vika** **Kaikki ylläpito pyynnöt** -sivulla.