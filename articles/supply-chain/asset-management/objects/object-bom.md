---
title: Resurssien tuoterakenteet
description: Tässä ohjeaiheessa kuvataan resurssin tuoterakenteita resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f42646ae865cd530203c997fd10c8ccd59e7fa2b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427210"
---
# <a name="asset-boms"></a>Resurssien tuoterakenteet

[!include [banner](../../includes/banner.md)]

 

Tässä ohjeaiheessa kuvataan resurssin tuoterakenteita resurssien hallinnassa. **Resurssin tuoterakenne** -sivulla näkyy luettelo kaikista nimikkeistä (varaosista ja muista nimikkeistä), joita resurssin koko käyttöiän aikana käytetään. Kun luot uuden resurssin, sinun kannattaa harkita resurssin tuoterakenteen määrittämistä osana asetusmenettelyä. Tällä tavoin voit seurata resurssin nimikehistoriaa luontipäivästä lähtien.

Kun kunnossapitotyö on suoritettu ja nimikekulutus on rekisteröity työtilaukseen, voit seurata varaosien ja muiden resurssin käyttämien nimikkeiden kulutusta. Tämän toiminnon avulla voit säilyttää täydellisen nimikekulutustietueen kaikille resursseille. Voit käyttää tietuetta esimerkiksi valvomaan, onko tietty varaosa usein korvattu, tai seurata varaosia tai muita nimikkeitä, joita käytetään tällä hetkellä käyttö resurssissa.

> [!NOTE]
> Työtilauksessa nimikkeen kulutus voi sisältää sekä varaosia että muita nimikkeitä, kuten voiteluaineita, pultteja ja tiivisteitä.

Resurssin tuoterakenne voidaan päivittää automaattisesti resurssien hallinnan asetusten perusteella. Jos työtilauksen elinkaaren tila on luotu käsittelemään suoritettuja tai valmiita työtilauksia ja jos **Päivitä resurssin tuoterakenne** -vaihtoehto kyseiselle työtilauksen elinkaaritilalle on **Kyllä** **Työtilauksen elinkaaren tilat** -sivulla, kaikki työtilauksessa käytettävät nimikkeet päivitetään automaattisesti **Resurssin tuoterakenne** -sivulla, kun työtilaus päivitetään kyseiseen elinkaaren tilaan. 


Voit myös päivittää resurssin tuoterakenteen manuaalisesti luomalla uusia nimikerivejä **Resurssin tuoterakenne** -sivulla.

**Resurssin tuoterakenne** -sivulla voit seurata resurssien varaosahistoriaa sen jälkeen, kun nimikekulutus on rekisteröity työtilaukseen. Jotta voit käyttää tätä toimintoa, sinun on valittava nimikeryhmät, joita käytetään varaosien rekisteröintiin **Varaosien nimikeryhmät** -sivulla.

Jotta voit käyttää resurssin tuoterakenteen toiminnallisuutta, sinun on ensin määritettävä tarvittavat varaosien nimikeryhmät. Jos sitten haluat, että resurssin tuoterakenne päivitetään automaattisesti, kun työtilaus on valmis, voit määrittää työtilauksen elinkaaritilan käsittelemään kyseistä päivitystä. 


## <a name="set-up-spare-parts-item-groups"></a>Määritä varaosien nimikeryhmät

Varaosien historian asetukset perustuvat nimikeryhmiin, jotka on luotu **Varastonhallinta** -moduulissa. Resurssien hallinnassa määritetään nimikeryhmät, jotta voit seurata valittujen nimikeryhmien nimikkeiden varaosahistoriaa.

1. Valitse **resurssien hallinta** \> **Asetukset** \> **resurssi** \> **Varaosien nimikeryhmät**.
2. Määritä nimikeryhmä valitsemalla **Uusi**.
3. Valitse **Nimikeryhmä**-kentässä ryhmä. Ryhmän nimi tulee automaattisesti **Nimi**-kenttään.

## <a name="view-and-update-asset-boms"></a>Tarkastele ja päivitä resurssien tuoterakenteita

Kun olet kirjannut nimikekulutuksen työtilaukseen, voit tarkastella rekisteröityjen nimikkeiden kulutusta **resurssin tuoterakenne** -sivulla.

1. Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Aktiiviset resurssit**. Valitse resurssiluettelosta resurssi ja valitse sitten **Resurssin tuoterakenne**.

    > [!NOTE]
    > Voit tarkastella kaikkien resurssien kaikkien nimikkeiden kulutuksen rekisteröintejä valitsemalla **Resurssien hallinta** \> **Kyselyt** \> **Resurssit** \> **Resurssin tuoterakenne**.

2. Valitse **Päivitä resurssin tuoterakenne**. Voit lisätä päivitykseen resursseja, resurssityyppejä ja resursseja valitsemalla **Valitse**. Aloita päivitys valitsemalla **OK**. Voit myös määrittää Päivitä-funktion erätyöksi.
3. Jos haluat nähdä lisätietoja, jotka liittyvät nimikkeisiin, voit lisätä varastodimensioita. Valitse **Varasto** \> **Dimensionäyttö** ja valitse sitten niiden dimensioiden valintaruudut, jotka haluat nähdä. Jos haluat säilyttää tämän määrityksen kaikille **Resurssin tuoterakenne** -sivun resursseille, määritä **Tallenna asetukset** -asetukseksi **Kyllä**.
4. Saat yleiskatsauksen siitä, missä resurssien hallinnassa valitulla rivillä olevaa nimikettä käytetään suhteessa resursseihin, työtyypin oletuksiin, varaosiin ja työtilauksiin, valitse **Nimike, missä käytetty**. 
5. Jos haluat nähdä vain aktiiviset nimikerivit, valitse **Näytä** \> **Nykyinen**. Jos haluat nähdä kaikki nimikerivit, mukaan lukien rivit, joiden vanhentumispäivämäärä on aikaisempi kuin nykyinen päivämäärä, valitse **Näytä** \> **Kaikki**.

> [!NOTE]
> Kun olet suorittanut työtilauksen, jos jotkin kyseiseen resurssiin liittyvät nimikkeet tai varaosat ovat vanhentuneet tai ne on korvattu muilla nimikkeillä tai varaosilla, on suositeltavaa päivittää resurssin tuoterakenne vastaavasti.

## <a name="create-a-new-item-line-in-an-asset-bom"></a>Uuden nimikerivin luominen resurssin tuoterakenteeseen

Voit luoda nimikerivejä manuaalisesti resursseille.

1. Valitse **Resurssin tuoterakenne** -sivulla **Uusi**.
2. Valitse **Resurssi**-kentässä resurssi, jolle nimikerivi lisätään.
3. Syötä luku **Rivinumero**-kenttään rivin järjestysnumero.
4. Valitse **Voimassa**-kentässä nimikkeen alkamispäivä.
5. Jos nimike vanhenee, kirjoita päättymispäivä **Vanheneminen**-kenttään.
6. Valitse **Nimiketunnus**-kentässä nimike. Nimi tulee automaattisesti **Tuotteen nimi** -kenttään.
7. Anna käytetty määrä **Määrä**-kenttään. **Yksikkö**-kenttä päivittyy automaattisesti.
