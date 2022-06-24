---
title: Lähetysten konsolidointi, kun ne vapautetaan varastoon myyntitilausten automaattisella vapauttamisella
description: Tässä artikkelissa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon samassa automatisoidussa varaston vapautuksen jaksottaisessa menettelyssä.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 36eb5e788d0473e2fec2214e9aa7e245304347e3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875069"
---
# <a name="consolidate-shipments-released-to-the-warehouse-using-automatic-release-of-sales-orders"></a>Lähetysten konsolidointi, kun ne vapautetaan varastoon myyntitilausten automaattisella vapauttamisella

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään skenaariota, jossa useita tilauksia vapautetaan varastoon samassa automatisoidussa varaston vapautuksen jaksottaisessa menettelyssä. Tilaukset konsolidoidaan automaattisesti lähetyksiksi lähetyksen konsolidointikäytännöiksi määritettyjen sääntöjen perusteella.

Tämän skenaarion aikana luodaan myyntitilausjoukkoja ja kukun joukko vapautetaan varastoon. Tämän jälkeen lähetyksen konsolidoinnin aikana luodut tai päivitetyt lähetykset tarkistetaan määritettyjen käytäntöjen perusteella.

## <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Artikkelin skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin. Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu **USMF** ennen aloittamista.

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

#### <a name="sales-order-1-2"></a>Myyntitilaus 1-2

1. Luo myyntitilaus, jossa on seuraavat asetukset:

    - **Asiakastili:** *US-001*
    - **Toimitustapa:** *Lento-Ilma*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

#### <a name="sales-order-1-3"></a>Myyntitilaus 1-3

1. Luo myyntitilaus, jossa on seuraavat asetukset:

    - **Asiakastili:** *US-001*
    - **Toimitustapa:** *10*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

1. Lisää toinen tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0002* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*
    - **Toimitustapa:** *Lento-Ilma*

### <a name="create-order-set-2"></a>Tilausjoukon 2 luonti

#### <a name="sales-orders-2-1-and-2-2"></a>Myyntitilaukset 2-1 ja 2-2

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-002*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *M9200* (nimike, jonka **Koodi 4** -suodattimen arvo on *Tulenarka*)
    - **Määrä** *1.00*

1. Lisää toinen tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *M9201* (nimike, jonka **Koodi 4** -suodattimen arvo on *Räjähdysherkkä*)
    - **Määrä** *1.00*
    - **Toimitustapa:** *Lento-Ilma*

### <a name="create-order-set-3"></a>Tilausjoukon 3 luonti

#### <a name="sales-order-3-1"></a>Myyntitilaus 3-1

1. Luo myyntitilaus, jossa on seuraavat asetukset:

    - **Asiakastili:** *US-002*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *M9200* (nimike, jonka **Koodi 4** -suodattimen arvo on *Tulenarka*)
    - **Määrä** *1.00*

1. Lisää toinen tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *M9201* (nimike, jonka **Koodi 4** -suodattimen arvo on *Räjähdysherkkä*)
    - **Määrä** *1.00*
    - **Toimitustapa:** *Lento-Ilma*

> [!NOTE]
> Tämä tilaus on samanlainen kuin kaksi tilausjoukkoon 2 luotua tilausta. Se mainitaan kuitenkin omana tilausjoukkona, koska se julkaistaan erikseen myöhemmin tässä skenaariossa.

### <a name="create-order-set-4"></a>Tilausjoukon 4 luonti

#### <a name="sales-order-4-1"></a>Myyntitilaus 4-1

1. Luo myyntitilaus, jossa on seuraavat asetukset:

    - **Asiakastili:** *US-001*
    - **Asiakkaan ehdotus:** *1*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

### <a name="create-order-set-5"></a>Tilausjoukon 5 luonti

#### <a name="sales-orders-5-1-and-5-2"></a>Myyntitilaukset 5-1 ja 5-2

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-001*
    - **Asiakkaan ehdotus:** *2*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

#### <a name="sales-order-5-3"></a>Myyntitilaus 5-3

1. Luo myyntitilaus, jossa on seuraavat asetukset:

    - **Asiakastili:** *US-001*
    - **Asiakkaan ehdotus:** *1*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

### <a name="create-order-set-6"></a>Tilausjoukon 6 luonti

#### <a name="sales-orders-6-1-and-6-2"></a>Myyntitilaukset 6-1 ja 6-2

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-003*
    - **Asiakkaan ehdotus:** *2*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

#### <a name="sales-orders-6-3-and-6-4"></a>Myyntitilaukset 6-3 ja 6-4

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-004*
    - **Asiakkaan ehdotus:** *1*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

#### <a name="sales-orders-6-5-and-6-6"></a>Myyntitilaukset 6-5 ja 6-6

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-007*
    - **Toimipaikka:** *6*
    - **Varasto**: *61*
    - **Pooli:** *ShipCons*

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

#### <a name="sales-orders-6-7-and-6-8"></a>Myyntitilaukset 6-7 ja 6-8

1. Luo kaksi samanlaista myyntitilausta, joissa on seuraavat asetukset:

    - **Asiakastili:** *US-007*
    - **Toimipaikka:** *6*
    - **Varasto**: *61*
    - **Pooli:** jätä tämä kenttä tyhjäksi.

1. Lisää tilausrivi, jossa on seuraavat asetukset:

    - **Nimiketunnus:** *A0001* (nimike, johon ei ole määritetty mitään **Koodi 4** -suodatinta)
    - **Määrä** *1.00*

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a>Myyntitilausten automaattinen vapautus varastoon

Jokaisen aiemmin luodun myyntitilausjoukon osalta suoritetaan automaattinen varastoon vapautusmenettely. Kussakin tapauksessa käytetään tässä käsiteltyä [varastoon vapautuksen perusmenettelyä](#release-procedure).

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a>Varastoon vapautuksen perusmenettely

Kunkin aiemmin luodun myyntitilausjoukon osalta suoritetaan kolme menettelyä, joita käsitellään seuraavissa aliosioissa.

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a>Vapautuksen aikana käytetyn aaltomallin päivittäminen

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.
1. Määritä **Aaltomallin tyyppi** -kentän arvoksi *Lähetys*.
1. Etsi ja valitse siihen varastoon liitetty aaltomalli, jota käytit tätä skenaariota varten luoduissa tilausjoukoissa. Jos esimerkiksi käytit varastoa *24*, valitse **24 Lähetysoletus** -aaltomalli. Jos käytit varastoa *61*, valitse **61 Lähetys**-aaltomalli.
1. Valitse toimintoruudussa **Muokkaa**.
1. Määritä **Käsittele aalto, kun se vapautetaan varastoon** -asetuksen arvoksi *Ei*.

#### <a name="release-to-the-warehouse"></a>Vapauttaminen varastoon

1. Valitse **Varastonhallinta \> Vapauta varastoon \> Myyntitilausten automaattinen vapautus**.
1. Määritä **Vapautettava määrä** -kentän arvoksi *Kaikki*.
1. Avaa kyselyvalintaikkuna valitsemalla **Sisällytettävät tietueet** -pikavälilehdessä **Suodatus**.
1. Lisää seuraavat asetukset sisältävä rivi ruudukkoon valitsemalla **Alue**-välilehdessä **Lisää**:

    - **Taulu:** *Myyntitilaus*
    - **Johdettu taulu:** *Myyntitilaus*
    - **Kenttä:** *Myyntitilaus*
    - **Ehdot:** anna toivotun tilausjoukon pilkuin eroteltu myyntitilausnumeroiden luettelo.

1. Tallenna kysely valitsemalla **OK**.
1. Käynnistä *Automaattinen vapautus varastoon* -menettely valitsemalla **OK**.

#### <a name="review-the-shipment-that-is-created-or-updated"></a>Luodun tai päivitetyn lähetyksen tarkistaminen

1. Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.
1. Etsi ja valitse tarvittava lähetys.
1. Jos lähetystä luotaessa tai päivitettäessä käytettiin konsolidointikäytäntöä, sen pitäisi näkyä **Lähetyksen konsolidointikäytäntö** -kentässä.

### <a name="release-sales-orders-from-order-set-1"></a>Myyntitilausten vapauttaminen tilausjoukosta 1

Vapauta myyntitilaukset tilausjoukosta 1 [varastoon vapauttamisen perusmenettelyn](#release-procedure) mukaisesti.

Lopuksi näkyvissä pitäisi olla kaksi luotua lähetystä:

- Ensimmäisessä lähetyksessä on kolme riviä, ja se luotiin käyttämällä lähetysten *CustomerMode*-konsolidointikäytäntöä.
- Toinen lähetys luotiin käyttämällä lähetyksen *CustomerOrderNo*-konsolidointikäytäntöä, ja siinä kuljetuksen toimitustapana ei ole *Lento*.

### <a name="release-sales-orders-from-order-set-2"></a>Myyntitilausten vapauttaminen tilausjoukosta 2

Vapauta myyntitilaukset tilausjoukosta 2 [varastoon vapauttamisen perusmenettelyn](#release-procedure) mukaisesti.

Lopuksi näkyvissä pitäisi olla kolme luotua lähetystä:

- Ensimmäinen lähetys sisältää *Tulenarka*-nimikkeitä.
- Kummassakin lähetyksessä on yksi rivi, jolla on *Räjähdysherkkä*-nimike.

### <a name="release-sales-orders-from-order-set-3"></a>Myyntitilausten vapauttaminen tilausjoukosta 3

Vapauta myyntitilaukset tilausjoukosta 3 [varastoon vapauttamisen perusmenettelyn](#release-procedure) mukaisesti.

Lopputuloksena pitäisi näkyvä seuraavat tapahtuneet toiminnot:

- Yksi aiemmin luotu lähetys (lähetys, joka luotiin vapauttamalla tilausjoukko 2 varastoon) päivitettiin. Yhdelle riville on lisätty *Tulenarka*-nimike.
- Luotiin yksi uusi lähetys, joka sisältää *Räjähdysherkkä*-nimikkeen.

### <a name="release-sales-orders-from-order-set-4"></a>Myyntitilausten vapauttaminen tilausjoukosta 4

Vapauta myyntitilaukset tilausjoukosta 4 [varastoon vapauttamisen perusmenettelyn](#release-procedure) mukaisesti.

Lopputuloksena pitäisi näkyä, että yksi aiemmin luotu lähetys (jossa **Asiakkaan ehdotus** -kentän arvoksi on määritetty *1*) päivitettiin. Siihen lisättiin yksi uusi rivi.

### <a name="release-sales-orders-from-order-set-5"></a>Myyntitilausten vapauttaminen tilausjoukosta 5

Vapauta myyntitilaukset tilausjoukosta 5 [varastoon vapauttamisen perusmenettelyn](#release-procedure) mukaisesti.

Lopputuloksena pitäisi näkyvä seuraavat tapahtuneet toiminnot:

- Yksi aiemmin luotu lähetys (jossa **Asiakkaan ehdotus** -kentän arvoksi on määritetty *1*) päivitettiin. Siihen lisättiin myyntitilauksen 5-3 rivi (jossa **Asiakkaan ehdotus** -kentän arvoksi on määritetty *1*).
- Luotiin yksi uusi lähetys, jossa myyntitilausten 5-1 ja 5-2 rivit ryhmitettiin yhdeksi lähetykseksi.

### <a name="release-sales-orders-from-order-set-6"></a>Myyntitilausten vapauttaminen tilausjoukosta 6

Vapauta myyntitilaukset tilausjoukosta 6 [varastoon vapauttamisen perusmenettelyn](#release-procedure) mukaisesti.

Lopputuloksena pitäisi näkyä neljä luotua lähetystä:

- Tilin *US-003* kahden tilauksen rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.
- Tilin *US-004* kahden tilauksen rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.
- Tilin *US-007* myyntitilausten 6–5 ja 6–6 rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *Tilauspooli*-konsolidointikäytäntöä.
- Tilin *US-007* myyntitilausten 6–7 ja 6–8 rivit ryhmitettiin yhdeksi lähetykseksi käyttämällä lähetyksen *CrossOrder*-konsolidointikäytäntöä.

## <a name="additional-resources"></a>Lisäresurssit

- [Lähetyksen konsolidoinnin käytännöt](about-shipment-consolidation-policies.md)
- [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]