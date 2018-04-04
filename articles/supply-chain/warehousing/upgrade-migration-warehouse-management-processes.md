---
title: "Tuote- ja varastonhallinnan päivittäminen AX 2012:sta Finance and Operationsiin"
description: "Tämä aihe on yleiskatsaus tuote- ja varastonhallinnan siirtovaihtoehdoista."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 92d0b4dd9611de4d717f30dc8736c673835bea29
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="migrate-products-and-warehouse-management-from-ax-2012-to-finance-and-operations"></a>Tuote- ja varastonhallinnan päivittäminen AX 2012:sta Finance and Operationsiin

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa on yhteenveto tuotteen ja varastonhallinnan siirtoasetuksista Microsoft Dynamics 365 for Finance and Operationsissa.

<a name="introduction"></a>Johdanto
------------

Finance and Operationsin päivityksen aikana tuotteiden käyttö on estetty, jos ne liitetään varastodimensioryhmään, joka ei vastaa varastodimensioryhmän asetuksia Finance and Operationsissa. Päivityksen jälkeen voit kuitenkin käyttää siirtoasetuksia **Vaihda nimikkeen varastodimensioryhmä** -prosessissa ja poistaa käyttöeston tuotteista, jotka on estetty päivityksen aikana. Sitten voit käsitellä kyseisten tuotteiden tapahtumia. Jotkin nimikkeet voi olla liitetty aiemmin varastodimensioryhmiin, missä toimipaikka-, varasto- ja sijainti-varastodimensiot ovat käytössä ja niitä seurataan fyysisesti. Tässä tapauksessa voit käyttää **Vaihda nimikkeen varastodimensioryhmä** -prosessia ja ottaa käyttöön nimikkeet, joita käytetään varaston hallintaprosesseissa. Tämä ominaisuus on hyödyllinen, jos haluat käyttää varaston hallintatoimintoja nykyisille nimikkeille.

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>Finance and Operationsin päivittäminen, kun AX 2012 R3 WMSII on käytössä
Finance and Operations ei enää tue vanhaa **WMSII** -moduulia, joka on peräisin Microsoft Dynamics AX 2012:sta. Sen sijaan voit käyttää uutta **Varastonhallinta**-moduulia. Aiemmissa versioissa kirjanpitovarastosta voi valita varastodimensioiden sijainnin ja kuormalavatunnuksen. Kuitenkin osana päivitysprosessia kuormalavatunnus-varastodimensiota ei enää voida ottaa käyttöön kirjanpitovarastossa. Kaikki tuotteet, jotka liittyvät varastodimensioryhmään, joka käyttää kuormalavatunnus-varastodimensiota, estetään eikä niitä käsitellä.

### <a name="enabling-items-in-finance-and-operations"></a>Nimikkeiden ottaminen käyttöön Finance and Operations

Finance and Operationsissa nimikkeet, joita käytetään osana varaston hallintaprosesseja, täytyy liittää varastodimensioryhmään, jossa **Käytä varastonhallintaprosesseja** -parametri on valittu. Kun tämä asetus on valittuna, toimipaikka-, varasto-, varaston tila-, sijainti- ja rekisterikilpi-varastodimensiot tulevat aktiivisiksi. Voit vaihtaa tämän tyyppisen varastodimensioryhmän vain niille nimikkeille, jotka on jo liitetty varastodimensioryhmiin, joissa sijainnin varastodimensio on aktiivinen.

### <a name="items-that-are-blocked-for-inventory-updates"></a>Nimikkeet, joiden varastopäivitykset on estetty

Näet luettelon vapautetuista tuotteista, joka on estetty päivityksen yhteydessä ja joita ei voi käsitellä, valitse **Inventoinnin- ja varastonhallinta** &gt; **Asetukset** &gt; **Varasto** &gt; **Nimikkeet, joiden varastopäivitykset on estetty**.

### <a name="reapplying-blocked-products"></a>Toimituskiellossa olevien tuotteiden ottaminen käyttöön

Tuotteet, jotka on estetty päivityksen yhteydessä, pitää valita uusi varastodimensioryhmä tuotteille. Huomaa, että voit vaihtaa varastodimensioryhmän vaikka varastotapahtumia on avoimena. Voit käyttää nimikkeitä, jotka on estetty päivityksen yhteydessä, voit valita toisen seuraavista vaihtoehdoista:

-   Muuta varastodimensioryhmä nimikkeelle varastodimensioryhmässä, joka käyttää vain toimipaikka-, varasto- ja toimipaikka-varastodimensioita. Tämän muutoksen tuloksena kuormalavatunnus-varastodimensio ei ole enää käytössä.
-   Muuta varastodimensioryhmä nimikkeelle varastodimensioryhmässä, joka käyttää vain varastonhallintaprosesseja. Tämän muutoksen tuloksena rekisterikilpi-varastodimensio on nyt käytössä.

### <a name="migration-processes"></a>Siirtämisprosessit

Finance and Operationsissa nimikkeiden seuranta on osa varastonhallintaprosesseja. Näissä prosesseissa kaikki varastot ja niiden sijainnit pitää liittää sijainnin profiiliin. Käsitteellisesti näitä prosesseja on käsiteltävä, jos haluat käyttää varaston hallintaprosesseja:

-   Kaikkien kohteiden ja varastojen on oltava käytössä varastonhallintaprosesseja varten.
-   Aiemmin vapautetut tuotteet täytyy liittää uuteen varastodimensioryhmään, joka käyttää varaston hallintaprosesseja.

Jos lähdevarastodimensioryhmät käyttävät kuormalavatunnus-varastodimensiota, aiemmin käytettävissä olevan varaston, jota käytti kuormalavatunnus-varastodimensiota, sijainnit pitää liittää sijaintiprofiiliin, missä **Käytä rekisterikilven seurantaa**-parametri on valittuna. Jos olemassa olevia varastoja ei saa ottaa käyttöön varaston hallintaprosessien käyttämiseksi, voit muuttaa olemassa olevan varaston varastodimensioryhmät ryhmiin, jotka käsittelevät vain toimipaikka-, varasto- ja sijaintivarastodimensioita.

### <a name="using-the-warehouse-management-processes"></a>Varastonhallintaprosessien käyttäminen

Ennen kuin voit käyttää vapautettuja tuotteita **Varastonhallinta**-moduulissa, tuotteiden on käytettävä varastodimensioryhmää, missä **Käytä varastonhallintaprosesseja** -parametri on valittuna.

#### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Ota varastot käyttöön varastonhallintaprosesseja varten

1.  Luo vähintään yksi uusi sijaintiprofiili.
2.  Valitse **Varastonhallinta** &gt; **Asetukset** &gt; **Ota varastonhallintaprosessit käyttöön** &gt; **Ota varaston asetukset käyttöön**.
3.  **Ota varaston asetukset käyttöön** -sivulla lisää varastot, jotka haluat ottaa käyttöön. Voit tehdä tämän vaiheen suoraan sivulla tai käyttämällä Microsoft Office -integrointi.
4.  Varastopaikan profiilin määrittäminen kaikkiin sijainteihin. Voit tehdä tämän vaiheen helposti käyttämällä Microsoft Office -integrointia suoraan sivulla. Voit viedä ja tuoda tietoja tai käyttää tietoja yksikön käsittelyyn [Tietojen hallinta](../../dev-itpro/data-entities/data-entities.md).
5.  Vahvista muutokset. Vahvistusprosessin osana suoritetaan erilaisia tietojen eheyden vahvistusprosesseja. Suuremman päivitysprosessin yhteydessä ilmeneviä ongelmia saatetaan joutua säätämään lähteen käyttöönoton yhteydessä. Tässä tapauksessa tarvitaan lisätietopäivitystä.
6.  Muutosten käsittely.

#### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Nimikkeiden varastodimensioryhmän muuttaminen siten, että se käyttää varastonhallintaprosesseja

1.  Luo uusi **Varaston tila** -arvo ja määritä **Oletusvarastotilan tunnus** -arvo **Varastonhallinnan parametrit** -asetuksista.
2.  Luo uusi varastodimensioryhmä, missä **Käytä varastonhallintaprosesseja** -parametri on valittuna.
3.  Määritä **Varaushierarkia**-sivulla uusi varaushierakia nimikkeen varasto- ja seurantadimensioryhmien mukaan.
4.  Luo vähintään yksi sarjaryhmä, joka sisältää vähintään samat yksiköt, joita käytetään nimikkeiden varastoyksiköissä.
5.  Valitse **Varastonhallinta** &gt; **Asetukset** &gt; **Ota varastonhallintaprosessit käyttöön** &gt;**Vaihda nimikkeen varastodimensioryhmä**.
6.  Lisää **Vaihda nimikkeen varastodimensioryhmä** -sivulla nimikenumerot, varastodimensioryhmät ja yksikön sarjaryhmät. Voit tehdä tämän vaiheen helposti käyttämällä Microsoft Office -integrointia tai tietoyksikköprosessin avulla [Tietojen hallinta](../../dev-itpro/data-entities/data-entities.md).
7.  Vahvista muutokset. Vahvistusprosessin osana suoritetaan erilaisia tietojen eheyden vahvistusprosesseja. Suuremman päivitysprosessin yhteydessä ilmeneviä ongelmia saatetaan joutua säätämään lähteen käyttöönoton yhteydessä. Tässä tapauksessa tarvitaan lisätietopäivitystä.
8.  Muutosten käsittely. Kaikkien varastodimensioiden päivitys voi kestää jonkin aikaa. Voit valvoa edistymistä erätehtävätöillä.



