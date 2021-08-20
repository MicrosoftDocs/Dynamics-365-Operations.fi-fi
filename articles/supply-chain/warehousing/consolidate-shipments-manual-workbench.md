---
title: Lähetysten konsolidointi käyttämällä lähetyksen konsolidoinnin työtilaa
description: Tässä ohjeaiheessa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon ja jotka sitten konsolidoidaan lähetyksiksi lähetysten konsolidoinnin työtilassa.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 5c4234cbe591079daf45aef6309cc84da16246ba6461a513b93589b2e1e6bf28
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728432"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a>Lähetysten konsolidointi käyttämällä lähetyksen konsolidoinnin työtilaa

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon ja jotka sitten konsolidoidaan lähetyksiksi lähetysten konsolidoinnin työtilassa.

## <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Ohjeaiheen skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin. Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu **USMF** ennen aloittamista.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Lähetyksen konsolidointikäytäntöjen ja tuotesuodattimien määrittäminen

Tässä skenaariossa oletetaan, että toiminto on jo otettu käyttöön ohjeaiheen [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md) harjoitukset on tehty sekä tässä kuvatut käytännöt ja muut tietueet on luotu. Varmista, että nämä harjoitukset on tehty ennen jatkamista tässä skenaariossa.

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a>Manuaalisen lähetyksen konsolidointitoiminnon ottaminen käyttöön

*Lähetyksen manuaalinen konsolidointi* -toiminto on otettava järjestelmässä käyttöön, ennen kuin sitä voi käyttää. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Manuaalinen lähetyksen konsolidointi*

Kuten ohjeaiheessa [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md) mainittiin, myös *Konsolidoi lähetys* -toiminto on otettava käyttöön ennen käytäntöjen luontia. Tämä vaihe pitäisi kuitenkin olla jo tehtynä.

## <a name="create-the-sales-orders-for-this-scenario"></a>Myyntitilausten luonti skenaarioon

Aloita luomalla myyntitilauskokoelma, jota voit käyttää. Käytössä on oltava varasto, jossa edistyneet varastoprosessit (WMS) on otettu käyttöön. Ellei jotain muuta varastoa nimenomaisesti mainita, jokaisessa seuraavista tilausjoukoista on käytettävä samaa varastoa.

Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset** ja luo myyntitilauskokoelma, jonka asetukset käsitellään seuraavissa kohdissa.

### <a name="create-order-set-1"></a>Tilausjoukon 1 luonti

#### <a name="sales-orders-1-1-and-1-2"></a>Myyntitilaukset 1-1 ja 1-2

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-001*
    - **Toimitustapa:** *Lento-Ilma*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

1. Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.

#### <a name="sales-order-1-3"></a>Myyntitilaus 1-3

1. Luo myyntitilaus, jossa on seuraavat asetukset:

    - **Asiakastili:** *US-001*
    - **Toimitustapa:** *10*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

1. Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.
1. Lisää toinen tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0002* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*
    - **Toimitustapa:** *Lento-Ilma*

1. Valitse ensin **Varasto \> Varaus** ja varaa sitten toinen tilausrivi valitsemalla toimintoruudussa **Varaa erä**.

### <a name="create-order-set-2"></a>Tilausjoukon 2 luonti

#### <a name="sales-orders-2-1-and-2-2"></a>Myyntitilaukset 2-1 ja 2-2

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-002*
    - **Toimitustapa:** *Lento-Ilma*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *M9200* (nimike, jonka **Koodi 4** -suodattimen arvo on *Tulenarka*)
    - **Määrä** *1.00*

1. Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.
1. Lisää toinen tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *M9201* (nimike, jonka **Koodi 4** -suodattimen arvo on *Räjähdysherkkä*)
    - **Määrä** *1.00*
    - **Toimitustapa:** *Lento-Ilma*

1. Valitse ensin **Varasto \> Varaus** ja varaa sitten toinen tilausrivi valitsemalla toimintoruudussa **Varaa erä**.

### <a name="create-order-set-3"></a>Tilausjoukon 3 luonti

#### <a name="sales-orders-3-1-and-3-2"></a>Myyntitilaukset 3-1 ja 3-2

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-001*
    - **Asiakkaan ehdotus:** *1*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

1. Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.

#### <a name="sales-orders-3-3-and-3-4"></a>Myyntitilaukset 3-3 ja 3-4

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-001*
    - **Asiakkaan ehdotus:** *2*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

1. Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.

### <a name="create-order-set-4"></a>Tilausjoukon 4 luonti

#### <a name="sales-orders-4-1-and-4-2"></a>Myyntitilaukset 4-1 ja 4-2

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-003*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

1. Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.

#### <a name="sales-orders-4-3-and-4-4"></a>Myyntitilaukset 4-3 ja 4-4

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-004*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

1. Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.

#### <a name="sales-orders-4-5-and-4-6"></a>Myyntitilaukset 4-5 ja 4-6

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-007*
    - **Toimipaikka:** *6*
    - **Varasto**: *61*
    - **Pooli:** *ShipCons*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

1. Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.

#### <a name="sales-orders-4-7-and-4-8"></a>Myyntitilaukset 4-7 ja 4-8

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-007*
    - **Toimipaikka:** *6*
    - **Varasto**: *61*
    - **Pooli:** jätä tämä kenttä tyhjäksi.

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

1. Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.

## <a name="release-the-orders-to-the-warehouse"></a>Tilausten vapauttaminen varastoon

Vapauta jokainen tähän skenaarioon luotu myyntitilaus varastoon seuraavien ohjeiden avulla:

1. Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset**.
1. Etsi ja valitse vapautettava myyntitilaus.
1. Vapauta valittu myyntitilaus valitsemalla toimintoruudun **Varasto**-välilehdessä **Toiminnot \> Vapauta varastoon**.
1. Toista tämä menettely jokaisen tähän skenaarioon luodun myyntitilauksen osalta.

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a>Lähetysten konsolidointi käyttämällä lähetyksen konsolidoinnin työtilaa

1. Valitse **Varastonhallinta \> Vapauta varastoon \> Lähetyksen konsolidoinnin työtila**.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Lisää kyselyeditoriin valintaikkunassa seuraavat asetukset sisältävä rivi ruudukkoon valitsemalla **Alue**-välilehdessä **Lisää**:

    - **Taulu:** *Myyntitilaukset*
    - **Kenttä:** *Myyntitilaus*
    - **Ehdot:** anna kunkin tähän skenaarion luodun tilausjoukon pilkuin eroteltu myyntitilausnumeroiden luettelo.

1. Tallenna kysely ja sulje valintaikkuna valitsemalla **OK**.
1. Valitse toimintoruudussa **Konsolidoi lähetykset**.
1. Valitse ensin kaikki lähetykset ja sitten toimintoruudussa **Konsolidoi**.

## <a name="verify-the-shipments"></a>Lähetysten tarkistaminen

Seuraavan menettelyn avulla voi tarkistaa lähetykset, jotka on luotu tai päivitetty lähetyksen konsolidoinnin tuloksena. Sen avulla voi tarkistaa kunkin skenaarioon luodun tilausjoukon sekä seuraavat osiot. Tällä tavoin voidaan varmistaa, että tulokset ovat odotetunkaltaiset.

1. Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.
1. Etsi ja valitse tarvittava lähetys.
1. Jos lähetystä luotaessa tai päivitettäessä käytettiin konsolidointikäytäntöä, sen pitäisi näkyä **Lähetyksen konsolidointikäytäntö** -kentässä.

### <a name="related-shipments-for-order-set-1"></a>Tilausjoukkoon 1 liittyvät lähetykset

Luotuja lähetyksiä on oltava kaksi:

- Ensimmäisessä lähetyksessä on kolme riviä, ja se luotiin käyttämällä lähetysten *CustomerMode*-konsolidointikäytäntöä.
- Toinen lähetys luotiin käyttämällä lähetyksen *CustomerOrderNo*-konsolidointikäytäntöä, ja siinä kuljetuksen toimitustapana ei ole *Lento*.

### <a name="related-shipments-for-order-set-2"></a>Tilausjoukkoon 2 liittyvät lähetykset

Luotuja lähetyksiä on oltava kolme:

- Ensimmäinen lähetys sisältää *Tulenarka*-nimikkeitä.
- Kummassakin lähetyksessä on yksi rivi, jolla on *Räjähdysherkkä*-nimike.

### <a name="related-shipments-for-order-set-3"></a>Tilausjoukkoon 3 liittyvät lähetykset

Luotuja lähetyksiä on oltava kaksi:

- Ensimmäisessä lähetyksessä on sellaisen myyntitilauksen rivejä, jossa **Asiakkaan ehdotus** -kentän arvo on *1*.
- Toisessa lähetyksessä on sellaisen myyntitilauksen rivejä, jossa **Asiakkaan ehdotus** -kentän arvo on *2*.

### <a name="related-shipments-for-order-set-4"></a>Tilausjoukkoon 4 liittyvät lähetykset

Luotuja lähetyksiä on oltava neljä:

- Tilin *US-003* kahden tilauksen rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.
- Tilin *US-004* kahden tilauksen rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.
- Tilin *US-007* myyntitilausten 4–5 ja 4–6 rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.
- Tilin *US-007* myyntitilausten 4–7 ja 4–8 rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *CrossOrder*-konsolidointikäytäntöä.

## <a name="additional-resources"></a>Lisäresurssit

- [Lähetyksen konsolidoinnin käytännöt](about-shipment-consolidation-policies.md)
- [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]