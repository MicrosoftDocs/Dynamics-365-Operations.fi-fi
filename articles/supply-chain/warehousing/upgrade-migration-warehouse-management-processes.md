---
title: "Varastonhallintaprosessien päivittäminen Microsoft Dynamics AX 2012:sta Finance and Operationsiin"
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e0ff3a22b89ce22096198d2e1dd1ea9ed10239a9
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="upgrade-warehouse-management-from-microsoft-dynamics-ax-2012-to-finance-and-operations"></a>Varastonhallintaprosessien päivittäminen Microsoft Dynamics AX 2012:sta Finance and Operationsiin

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe sisältää yhteenvedon Microsoft Dynamics AX 2012 R3:n (jossa WMSII-moduuli) päivittämisestä Microsoft Dynamics 365 for Finance and Operationsiin.

Finance and Operations ei enää tue vanhaa **WMSII** -moduulia, joka on peräisin Microsoft Dynamics AX 2012:sta. Sen sijaan voit käyttää **Varastonhallinta**-moduulia. WMSII-moduulissa Sijainti- ja Kuormalavan tunnus -varastodimensiot voidaan valita kirjanpitovarastoa varten, mutta Kuormalavan tunnus -varastodimensiota ei voida käyttää kirjanpitovarastoon Finance and Operationsissa.

Päivityksen aikana kaikki Kuormalavatunnus-varastodimensiota käyttävään varastodimensioryhmään liittyvät tuotteet tunnistetaan ja merkitään lukituksi eikä niitä käsitellä päivitystä varten.

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>Finance and Operationsin päivittäminen, kun AX 2012 R3 WMSII on käytössä
Päivityksen jälkeen voit kuitenkin käyttää asetuksia **Vaihda nimikkeen varastodimensioryhmä** -lomakkeessa ja poistaa käyttöeston tuotteista, jotka on estetty päivityksen aikana. Sen jälkeen voit käsitellä näiden tuotteiden tapahtumia.

### <a name="enabling-items-in-finance-and-operations"></a>Nimikkeiden ottaminen käyttöön Finance and Operations
Tämä muutos on tarpeen, koska Finance and Operationsissa nimikkeiden seuranta on osa varastonhallintaprosesseja. Näissä prosesseissa kaikki varastot ja niiden sijainnit pitää liittää sijainnin profiiliin. Jos haluat käyttää varaston hallintaprosesseja, seuraavat tiedot on määritettävä:
-   Kaikkien kohteiden ja varastojen on oltava käytössä varastonhallintaprosesseja varten 
-   Aiemmin vapautetut tuotteet täytyy liittää varastodimensioryhmään, joka käyttää varaston hallintaprosesseja 

Jos lähdevarastodimensioryhmät käyttävät kuormalavatunnus-varastodimensiota, aiemmin käytettävissä olevan varaston, jota käytti kuormalavatunnus-varastodimensiota, sijainnit pitää liittää sijaintiprofiiliin, missä **Käytä rekisterikilven seurantaa**-parametri on valittuna. Jos olemassa olevia varastoja ei saa ottaa käyttöön varaston hallintaprosessien käyttämiseksi, voit muuttaa olemassa olevan varaston varastodimensioryhmät ryhmiin, jotka käsittelevät vain toimipaikka-, varasto- ja sijaintivarastodimensioita. 

> [!NOTE] 
>  Voit vaihtaa nimikkeiden varastodimensioryhmän vaikka varastotapahtumia on avoimena.

## <a name="find-products-that-were-blocked-because-of-pallet-id"></a>Etsi tuotteita, jotka on estetty kuormalavatunnuksen vuoksi
Näet luettelon vapautetuista tuotteista, joka on estetty päivityksen yhteydessä ja joita ei voi käsitellä, valitse **Inventoinnin- ja varastonhallinta** &gt; **Asetukset** &gt; **Varasto** &gt; **Nimikkeet, joiden varastopäivitykset on estetty**.

## <a name="change-storage-dimension-group-for-blocked-products"></a>Estettyjen tuotteiden varastodimensioryhmän muuttaminen 
 
Jotta nimikeittä voidaan käyttää osana varaston hallintaprosessia, se täytyy liittää varastodimensioryhmään, jossa Varaston sijaintidimensio on aktiivinen ja **Käytä varastonhallintaprosesseja** -parametri on valittu. Kun tämä asetus on valittuna, toimipaikka-, varasto-, varaston tila-, sijainti- ja rekisterikilpi-varastodimensiot tulevat aktiivisiksi.

Tuotteet, jotka on estetty päivityksen yhteydessä, pitää valita uusi varastodimensioryhmä tuotteille. Huomaa, että voit vaihtaa varastodimensioryhmän vaikka varastotapahtumia on avoimena. Voit käyttää nimikkeitä, jotka on estetty päivityksen yhteydessä, voit valita toisen seuraavista vaihtoehdoista:

-   Muuta varastodimensioryhmä nimikkeelle varastodimensioryhmässä, joka käyttää vain toimipaikka-, varasto- ja toimipaikka-varastodimensioita. Tämän muutoksen tuloksena kuormalavatunnus-varastodimensio ei ole enää käytössä.
-   Muuta varastodimensioryhmä nimikkeelle varastodimensioryhmässä, joka käyttää vain varastonhallintaprosesseja. Tämän muutoksen tuloksena rekisterikilpi-varastodimensio on nyt käytössä.

## <a name="configure-warehouse-management-processes"></a>Varastonhallintaprosessien määrittäminen
Ennen kuin voit käyttää vapautettuja tuotteita **Varastonhallinta**-moduulissa, tuotteiden on käytettävä varastodimensioryhmää, missä **Käytä varastonhallintaprosesseja** -parametri on valittuna.

### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Ota varastot käyttöön varastonhallintaprosesseja varten

1.  Luo vähintään yksi uusi sijaintiprofiili.
2.  Valitse **Varastonhallinta** &gt; **Asetukset** &gt; **Ota varastonhallintaprosessit käyttöön** &gt; **Ota varaston asetukset käyttöön**.
3.  **Ota varaston asetukset käyttöön** -sivulla lisää varastot, jotka haluat ottaa käyttöön. Voit tehdä tämän vaiheen suoraan sivulla tai käyttämällä Microsoft Office -integrointi.
4.  Varastopaikan profiilin määrittäminen kaikkiin sijainteihin. Voit tehdä tämän vaiheen helposti käyttämällä Microsoft Office -integrointia suoraan sivulla. Voit viedä ja tuoda tietoja tai käyttää tietoja yksikön käsittelyyn [Tietojen hallinta](../../dev-itpro/data-entities/data-entities.md).
5.  Vahvista muutokset. Vahvistusprosessin osana suoritetaan erilaisia tietojen eheyden vahvistusprosesseja. Suuremman päivitysprosessin yhteydessä ilmeneviä ongelmia saatetaan joutua säätämään lähteen käyttöönoton yhteydessä. Tässä tapauksessa tarvitaan lisätietopäivitystä.
6.  Muutosten käsittely.

### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Nimikkeiden varastodimensioryhmän muuttaminen siten, että se käyttää varastonhallintaprosesseja

1.  Luo uusi **Varaston tila** -arvo ja määritä **Oletusvarastotilan tunnus** -arvo **Varastonhallinnan parametrit** -asetuksista.
2.  Luo uusi varastodimensioryhmä, missä **Käytä varastonhallintaprosesseja** -parametri on valittuna.
3.  Määritä **Varaushierarkia**-sivulla uusi varaushierakia nimikkeen varasto- ja seurantadimensioryhmien mukaan.
4.  Luo vähintään yksi sarjaryhmä, joka sisältää vähintään samat yksiköt, joita käytetään nimikkeiden varastoyksiköissä.
5.  Valitse **Varastonhallinta** &gt; **Asetukset** &gt; **Ota varastonhallintaprosessit käyttöön** &gt;**Vaihda nimikkeen varastodimensioryhmä**.
6.  Lisää **Vaihda nimikkeen varastodimensioryhmä** -sivulla nimikenumerot, varastodimensioryhmät ja yksikön sarjaryhmät. Voit tehdä tämän vaiheen helposti käyttämällä Microsoft Office -integrointia tai tietoyksikköprosessin avulla [Tietojen hallinta](../../dev-itpro/data-entities/data-entities.md).
7.  Vahvista muutokset. Vahvistusprosessin osana suoritetaan erilaisia tietojen eheyden vahvistusprosesseja. Suuremman päivitysprosessin yhteydessä ilmeneviä ongelmia saatetaan joutua säätämään lähteen käyttöönoton yhteydessä. Tässä tapauksessa tarvitaan lisätietopäivitystä.
8.  Muutosten käsittely. Kaikkien varastodimensioiden päivitys voi kestää jonkin aikaa. Voit valvoa edistymistä erätehtävätöillä.

