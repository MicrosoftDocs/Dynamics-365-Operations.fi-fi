---
title: Rekisterikilven vastaanotto varastointisovelluksen kautta
description: Tässä ohjeaiheessa selitetään, kuinka varastointisovellus määritetään tukemaan rekisterikilven vastaanottoprosessin käyttöä fyysisen varaston vastaanottamiseen.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346373"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a>Rekisterikilven vastaanotto varastointisovelluksen kautta

Tässä ohjeaiheessa selitetään, kuinka varastointisovellus määritetään niin, että se tukee rekisterikilven vastaanottoprosessin käyttöä fyysisen varaston vastaanottamiseen.

Tämän toiminnon avulla voit nopeasti kirjata saapuvaa varastoa koskevan vastaanoton, joka liittyy ennakkoilmoitukseen (ASN). Järjestelmä luo automaattisesti ASN-arvon, kun siirtotilauksen lähetys suoritetaan varastoinnin hallintaprosessien avulla. Ostotilausprosessin aikana ASN voidaan tallentaa manuaalisesti, tai se voidaan tuoda automaattisesti käyttämällä saapuvan ASN-tietoyksikkö prosessia.

ASN-tiedot linkitetään kuormiin ja lähetyksiin *pakkausrakenteiden*kautta, joissa kuormalavat (päärekisterikilvet) voivat sisältää palvelupyyntöjä (sisäkkäisiä rekisterikilpiä).

> [!NOTE]
> Kun käytetään sisäkkäisten rekisterikilpien pakkausrakenteita, järjestelmä tallentaa varastotapahtumien määrän pääkäyttöoikeusrekisterikilpeen. Jos haluat käynnistää fyysisen käytettävissä olevan varaston siirtämisen pääkäyttöoikeusrekisterikilvestä sisäkkäisiin rekisteritietoihin perustuen, mobiililaitteen on määritettävä pakkausrakenteen tietojen perusteella valikkovaihtoehto, joka perustuu *pakkauksen sisäkkäinen rekisterikilpi* -töiden luomisprosessiin.

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>Vastaanottavan yhteenvetosivun näyttäminen tai ohittaminen

Voit käyttää *ohjausobjektia, näytetäänkö vastaanottavan yhteenvetosivun mobiililaitteissa* -ominaisuutta, jotta saat lisätietoja fyysisen varastoinnin sovelluskulusta osana rekisterikilven vastaanottoprosessia.

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa tämä ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Ominaisuuden nimi:** *Määrittää, näytetäänkö vastaanottava yhteenvetosivu mobiililaitteissa*

Kun tämä toiminto on otettu käyttöön, kannettavien laitteiden valikkokohteet, jotka koskevat rekisteritietoja tai rekisterikilven vastaanottoa ja hyllytystä, sisältävät **näytön vastaanottamisen yhteenvetosivu** -asetuksen. Tällä asetuksella on seuraavat vaihtoehdot:

- **Näytä yksityiskohtainen yhteenveto** – Rekisterikilven vastaanottamisen aikana työntekijät näkevät ylimääräisen sivun, jossa näkyvät kaikki ASN-tiedot.
- **Ohita yhteenveto** – Työntekijät eivät näe kaikkia ASN-tietoja. Varastotyöntekijät eivät voi määrittää käsittelykoodia tai lisätä poikkeuksia vastaanottoprosessin aikana.

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Estä siirtotilauksen lähettämien rekisterikilpien käyttö muissa varastoissa kuin kohdevarastossa

Rekisterikilven vastaanottoprosessia ei voi käyttää, jos ASN sisältää rekisterikilven tunnuksen, joka on jo olemassa ja jolla on fyysisiä käytettävissä olevia tietoja varastosijainnissa, joka ei ole sama kuin varastosijainti, jossa rekisterikilpi rekisteröidään.

Siirtotilausten tapauksissa, joissa kuljetusvarasto ei jäljitä rekisterikilpiä (eikä näin ollen myöskään kirjaa fyysistä käytettävissä olevaa varastoa rekisterikilpeä kohden), voit käyttää *Estä siirtotilauksen mukana toimitettuja rekisterikilpiä käytettäväksi muissa varastoissa kuin kohdevarastossa* -toimintoa, joka estää kauttakuljetuksessa olevien rekisterikilpien fyysisten käytettävissä olevien päivitysten käytön.

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa tämä ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Ominaisuuden nimi:** *Estä siirtotilauksen lähettämien rekisterikilpien käyttö muissa varastoissa kuin kohdevarastossa*

Voit hallita toimintoja, kun tämä toiminto on käytettävissä, noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
1. Määritä **Yleinen**-välilehden **Rekisterikilvet**-pikavälilehdessä, että **Kuljetusvaraston rekisterikilpikäytäntö** -kenttä on jokin seuraavista arvoista:

    - **Salli ei-seurattujen rekisterikilpien uudelleenkäyttö** – Järjestelmä toimii samalla tavalla kuin se toimii, kun *Estä siirtotilauksen toimittamien rekisterikilpien käyttö muissa varastoissa kuin kohdevarasto* -toiminto ei ole käytössä. Tämä arvo on oletusasetus, kun aktivoit ominaisuuden ensimmäisen kerran.
    - **Ei-seuratun rekisterikilven uudelleenkäytön estäminen** – Kohdevarastossa sallitaan vain käytettävissä olevat päivitykset, jotka liittyvät toimitettuun rekisterikilpeen, kunnes siirtotilaus on vastaanotettu.

## <a name="more-information"></a>Lisätietoja

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

Lisätietoja mobiililaitteiden valikkokohteista on kohdassa [Mobiililaitteiden määrittäminen varastotyötä varten](configure-mobile-devices-warehouse.md).
