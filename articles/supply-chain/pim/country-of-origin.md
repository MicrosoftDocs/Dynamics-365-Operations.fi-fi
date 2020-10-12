---
title: Alkuperämaa
description: Monet organisaatiot myöntänyt toimittajille todistuksia varmistamaan, että tuotteet vastaavat tiettyjä sertifiointistandardeja. Nämä todistukset määräytyvät usein alkuperämaasta. Tässä ohjeaiheessa käsitellään alkuperämaatoimintoa, jonka avulla tuotteen voi linkittää alkuperämaahan ja seurata tuotteen sertifiointeja.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0471785991a307de11147e9773d9abe1e02941d6
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895545"
---
# <a name="country-of-origin"></a>Alkuperämaa

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Monet organisaatiot myöntänyt toimittajille todistuksia varmistamaan, että tuotteet vastaavat tiettyjä sertifiointistandardeja. Nämä todistukset määräytyvät usein alkuperämaasta. Alkuperämaatoiminnon avulla tuotteen voi linkittää alkuperämaahan ja seurata tuotteen sertifiointeja.

## <a name="turn-on-the-country-of-origin-feature"></a>Alkuperämaa-ominaisuuden ottaminen käyttöön

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Tuotetietojen hallinta*
- **Ominaisuuden nimi:** *Alkuperämaan hallinta -ominaisuus*

## <a name="configure-source-and-destination-countries"></a>Lähde- ja kohdemaiden määrittäminen

Ennen kuin tuotteelle myönnetään todistus, tuote on linkitettävä kohdemaahan ja sen alkuperämaahan.

1. Valitse **Tuotetietojen hallinta \> Asetukset \> Tuotteen yhteensopivuus \> Alkuperämaa \> Alkuperämaasäännöt**.
2. Valitse aiemmin luodun maan asetukset muokattavaksi tai luo uudet maa-asetukset valitsemalla toimintoruudussa **Uusi**.
3. Määritä seuraavat valitun tai uuden maan arvot:

    | Kenttä | kuvaus |
    |---|---|
    | Nimiketunnus | Valitse tuotteen nimiketunnus. |
    | Kohdemaa | Valitse maa, johon tuote lähetetään. |
    | Alkuperämaa | Valitse maa, josta tuote lähetetään. |

Tämän asetuksen tarkoitus on auttaa luomaan tuoterakenneraportti, jossa alkuperämaa voidaan sisällyttää kuhunkin osaan, johon lähde- ja kohdemaa on määritetty. Tämän raportin avulla saadaan kokonaisvaltainen käsityksen siitä, mistä osat tulevat ja mihin ne ovat menossa.

## <a name="keep-track-of-vendor-certificates"></a>Toimittajien varmenteiden seuraaminen

Voit seurata toimittajille myönnettyjä varmenteita **Toimittajien alkuperämaavarmenteet** -sivulla.

Sinun on päätettävä, mitä varmenneasiakirjoja myönnetään ja miten ne raportoidaan asiakkaille. Tämä toimintoa auttaa seuraamaan varmenteita. Sen avulla voi myös valita, näkyvätkö varmennenumerot laskuissa, pakkausluetteloissa ja/tai tilausvahvistuksissa.

Voit määrittää varmenteen tiedot seuraavasti:

1. Valitse **Tuotetietojen hallinta \> Asetukset \> Tuotteen yhteensopivuus \> Alkuperämaa \> Toimittajan alkuperämaavarmenteet**.
2. Valitse aiemmin luodun varmenteen asetukset muokattavaksi tai luo uudet varmenneasetukset valitsemalla toimintoruudussa **Uusi**.
3. Määritä seuraavat valitun tai uuden varmenteen asetukset:

    | Kenttä | kuvaus |
    |---|---|
    | Toimittajatili | Valitse toimittaja, jolle varmenne myönnetään. |
    | Nimiketunnus | Valitse nimike, jolle varmenne myönnetään. |
    | Maa/alue | Kohdemaa tai -alue, jossa tätä varmennetta on käytettävä. |
    | Varmenteen numero | Anna myönnetyn varmenteen tunnusnumero. |
    | Voimassa | Valitse ensimmäinen päivämäärä, jolloin nykyinen varmenne on voimassa.|
    | Vanhentumisaika | Valitse viimeinen päivämäärä, jolloin nykyinen varmenne on voimassa. |
    | Tulosta laskulle | Valitse tämä valintaruutu, kun varmennenumero tulostetaan laskuihin, joiden osoitteena on määritetty maa määritetyllä päivämääräalueella. |
    | Tulosta pakkausluettelossa | Valitse tämä valintaruutu, kun varmennenumero tulostetaan pakkausluetteloihin, joiden osoitteena on määritetty maa määritetyllä päivämääräalueella. |
    | Tulosta myyntitilauksessa | Valitse tämä valintaruutu, kun varmennenumero tulostetaan myyntitilauksiin, joiden osoitteena on määritetty maa määritetyllä päivämääräalueella. |

## <a name="include-the-country-of-origin-on-bom-reports"></a>Sisällytä alkuperämaa tuoterakenneraportteihin

Kun luot tuoterakenneraportin, voit sisällyttää kunkin sellaisen osan alkuperämaan, jonka lähde- ja kohdemaa on määritetty **Alkuperämaasäännöt**-sivulla.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Avaa tuotteen **Vapautetun tuotteen tiedot** -sivu valitsemalla tai luomalla tuote.
1. Valitse toimintoruudun **Suunnittele**-välilehden **Tuoterakenne**-ryhmässä **Suunnittelutoiminto**.
1. Valitse avautuvan sivun toimintoruudussa **Tuoterakenne \> Tulosta**.
1. Määritä **Tuoterakennerivit**-valintaikkunassa **Kohdemaa**-kentässä kohdemaa, jota haluat tarkastella raportissa.
1. Valitse **OK**.

Kunkin osan alkuperämaasta tietoja sisältävä raportti luodaan ja näytetään. Esimerkki raportista.

![Alkuperämaaraportti](media/country-of-origin-report.png "Alkuperämaaraportti")
