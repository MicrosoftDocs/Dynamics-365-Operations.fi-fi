---
title: Lähetysten konsolidointi käyttämällä Vapauta varastoon -toimintoa kuormasuunnittelun työtilassa
description: Tässä ohjeaiheessa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon samassa kuormassa ja jotka sitten konsolidoidaan automaattisesti lähetyksiksi.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 2f1dd5c743664e638c043b600ae7b0f6bce5ddcd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426837"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a>Lähetysten konsolidointi käyttämällä Vapauta varastoon -toimintoa kuormasuunnittelun työtilassa

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon samassa kuormassa ja jotka sitten konsolidoidaan automaattisesti lähetyksiksi.

## <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Ohjeaiheen skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin. Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu **USMF** ennen aloittamista.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Lähetyksen konsolidointikäytäntöjen ja tuotesuodattimien määrittäminen

Tässä skenaariossa oletetaan, että toiminto on jo otettu käyttöön ohjeaiheen [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md) harjoitukset on tehty sekä tässä kuvatut käytännöt ja muut tietueet on luotu. Varmista, että nämä harjoitukset on tehty ennen jatkamista tässä skenaariossa.

## <a name="create-the-sales-orders-for-this-scenario"></a>Myyntitilausten luonti skenaarioon

Aloita luomalla myyntitilauskokoelma, jota voit käyttää. Käytössä on oltava varasto, jossa edistyneet varastoprosessit (WMS) on otettu käyttöön. Ellei jotain muuta varastoa nimenomaisesti mainita, jokaisessa seuraavista tilausjoukoista on käytettävä samaa varastoa.

Valitse **Myyntireskontra \> Tilaukset \> Kaikki myyntitilaukset** ja luo myyntitilauskokoelma, jonka asetukset käsitellään seuraavissa kohdissa.

### <a name="create-order-set-1"></a>Tilausjoukon 1 luonti

#### <a name="sales-order-1-1"></a>Myyntitilaus 1-1

1. Luo myyntitilaus, jossa on seuraavat asetukset:

    - **Asiakastili:** *US-001*
    - **Toimitustapa:** *Lento-Ilma*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

1. Valitse ensin **Varasto \> Varaus** ja varaa sitten tilausrivi valitsemalla toimintoruudussa **Varaa erä**.

#### <a name="sales-order-1-2"></a>Myyntitilaus 1-2

1. Luo myyntitilaus, jossa on seuraavat asetukset:

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

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a>Kuormien luonti ja niiden vapauttaminen varastoon kuormasuunnittelun työtilassa

Luo jokaiselle tähän skenaarioon luodulle tilausjoukolle kuorma ja vapauta se sitten varaston näiden ohjeiden avulla.

1. Valitse **Varastonhallinta \> Kuormat \> Kuormasuunnittelun työtila**.
1. Etsi ja valitse **Myyntirivit**-välilehdessä kaikki myyntitilausrivit yhdestä tätä skenaariota varten luodusta tilausjoukosta.
1. Lisää valitut tilausrivit uuteen kuormaan valitsemalla toimintoruudun **Tarjonta ja kysyntä** -välilehdessä **Lisää \> Uuteen kuormaan**.
1. Valitse **Lataa mallin määritys** -valintaikkunan **Kuorman mallitunnus** -kentässä kuormamalli, kuten *Vakiokuormamalli*.
1. Sulje valintaikkuna valitsemalla **OK**. 
1. Etsi ja valitse juuri luotu kuorma **Kuormat**-osassa.
1. Vapauta valittu kuorma varastoon valitsemalla **Vapautus \> Vapauta varastoon**.
1. Toista tämä menettely kolmen muun tähän skenaarioon luodun tilausjoukon osalta.

## <a name="verify-the-shipments"></a>Lähetysten tarkistaminen

Seuraavan menettelyn avulla voi tarkistaa lähetykset, jotka on luotu tai päivitetty lähetyksen konsolidoinnin tuloksena. Sen avulla voi tarkistaa kunkin skenaarioon luodun tilausjoukon sekä seuraavat osiot. Tällä tavoin voidaan varmistaa, että tulokset ovat odotetunkaltaiset.

1. Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.
1. Etsi ja valitse tarvittava lähetys.
1. Jos lähetystä luotaessa tai päivitettäessä käytettiin konsolidointikäytäntöä, sen pitäisi näkyä **Lähetyksen konsolidointikäytäntö** -kentässä.

### <a name="release-order-set-1-in-one-load"></a>Tilausjoukon 1 vapauttaminen yhdessä kuormassa

Luotuja lähetyksiä on oltava kaksi:

- Ensimmäisessä lähetyksessä on kolme riviä, ja se luotiin käyttämällä lähetysten *CustomerMode*-konsolidointikäytäntöä.
- Toinen lähetys luotiin käyttämällä lähetyksen *CustomerOrderNo*-konsolidointikäytäntöä, ja siinä kuljetuksen toimitustapana ei ole *Lento*.

### <a name="release-order-set-2-in-one-load"></a>Tilausjoukon 2 vapauttaminen yhdessä kuormassa

Luotuja lähetyksiä on oltava kolme:

- Ensimmäinen lähetys sisältää *Tulenarka*-nimikkeitä.
- Kummassakin lähetyksessä on yksi rivi, jolla on *Räjähdysherkkä*-nimike.

### <a name="release-order-set-3-in-one-load"></a>Tilausjoukon 3 vapauttaminen yhdessä kuormassa

Luotuja lähetyksiä on oltava kaksi:

- Ensimmäisessä lähetyksessä on sellaisen myyntitilauksen rivejä, jossa **Asiakkaan ehdotus** -kentän arvo on *1*.
- Toisessa lähetyksessä on sellaisen myyntitilauksen rivejä, jossa **Asiakkaan ehdotus** -kentän arvo on *2*.

### <a name="release-order-set-4-in-one-load"></a>Tilausjoukon 4 vapauttaminen yhdessä kuormassa

Luotuja lähetyksiä on oltava neljä:

- Asiakastilin *US-003* kahden tilauksen rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.
- Asiakastilin *US-004* kahden tilauksen rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.
- Asiakastilin *US-007* myyntitilausten 4–5 ja 4–6 rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.
- Asiakastilin *US-007* myyntitilausten 4–7 ja 4–8 rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilaustenvälinen*-konsolidointikäytäntöä.

## <a name="additional-resources"></a>Lisäresurssit

- [Lähetyksen konsolidoinnin käytännöt](about-shipment-consolidation-policies.md)
- [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md)
