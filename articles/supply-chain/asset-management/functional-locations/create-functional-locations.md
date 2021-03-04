---
title: Luo toiminnalliset sijainnit
description: Tässä ohjeaiheessa kerrotaan toiminnallisten sijaintien luonnista resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationCopyStructure, EntAssetFunctionalLocationCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37da9d59e4e9cf84238f6798a1aa7de72ff91f02
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426966"
---
# <a name="create-functional-locations"></a>Luo toiminnalliset sijainnit

[!include [banner](../../includes/banner.md)]

 

Tässä ohjeaiheessa kerrotaan toiminnallisten sijaintien luonnista resurssien hallinnassa.

Kun luot toiminnallisen sijainnin rakenteen, huomaa, että kun olet luonut toiminnallisen sijainnin, et voi siirtää sitä alkuperäisestä sijainnista. Tämä tarkoittaa, että sinun on harkittava tarkkaan toiminnallisten sijaintien rakennetta, ennen kuin aloitat niiden luomisen resurssien hallinnassa. Jos haluat peruuttaa toiminnallisen sijainnin luonnin, voit poistaa sen, jos sitä ei ole vielä otettu käyttöön.

Jotta voit työskennellä toiminnallisten sijaintien kanssa, aloita luomalla kaksi toiminnallisen sijaintien luokkaa:

- Luo *yksi* oletusarvoinen toiminnallinen sijainti, jossa ei ole alisijainteja. Tätä toiminnallista sijaintia käytetään vain resurssien vakiosijaintiksi, kun luot uusia resursseja.  
- Luo toiminnalliset sijaintirakenteet, joita tarvitaan yrityksen ylläpitotöiden hallintaan.

## <a name="create-a-default-functional-location"></a>Toiminnallisen oletussijainnin luominen

Kun käytät toiminnallisia sijainteja,aloita luomalla yksi oletussijainti, jota käytetään luodessasi uusia resursseja. tämä toiminnallinen sijainti on se, jonka valitset kohdassa **Resurssien hallinta** > **Asetukset** > **Resurssienhallinnan parametrit** > **Resurssit** -linkki > **Toiminnallinen oletussijainti** -kenttä. Oletusarvoinen toiminnallinen sijaintia voidaan käyttää luotaessa uusia resursseja, etkä ole vielä määrittänyt toiminnallista sijaintirakennetta näille resursseille.

1. Valitse **Resurssien hallinta** > **Yhteiset** > **Toiminnalliset sijainnit** > **Kaikki toiminnalliset sijainnit**.  
2. Valitse **Kaikki toiminnalliset sijainnit** -kohdassa **Uusi**.
3. Lisää tunnus **Toiminnallinen sijainti** -kenttään, esimerkiksi "0000" tai "Oletus", osoittamaan, että tämä on erityinen toiminnallinen sijainti.
4. Kirjoita **Nimi**-kenttään toiminnallisen oletussiajiannin nimi.
5. *Älä* valitse ylätasoa **Ylätaso** -kentässä – jätä tämä kenttä tyhjäksi.
6. Valitse **Toiminnallisen sijainnin tyyppi** -kentässä toiminnallinen sijaintityyppi, jota käytetään oletusarvoiseen toiminnalliseen sijaintiin. Lisätietoja toiminnallisten sijaintityyppien määrittämisestä on kohdassa [Toiminnalliset sijaintityypit](../setup-for-functional-locations/functional-location-types.md).
7. Valitse **OK**. Älä lisää tähän toiminnalliseen sijaintiin muita tietoja, koska sitä käytetään vain uusien resurssien väliaikaisena sijaintina, ennen kuin asennat resurssit yrityksesi käyttämien toiminnallisten sijaintien mukaan.

## <a name="create-functional-locations"></a>Luo toiminnalliset sijainnit

Seuraavassa menettelyssä kuvaillaan, miten yrityksesi ylläpidon hallintaan tarvittavat toiminnalliset sijainnit luodaan.

1. Valitse **Resurssien hallinta** > **Yhteiset** > **Toiminnalliset sijainnit** > **Kaikki toiminnalliset sijainnit**. Voit luoda toiminnallisen sijainnin ruudukkonäkymästä tai Tiedot-näkymästä.
2. Valitse **Uusi**-painike.
3. Lisää tunnus **Toiminnallinen sijainti** -kenttään.
4. Kirjoita **Nimi**-kenttään toiminnallisen sijainnin nimi.
5. Jos toiminnallinen sijainti on rakenteen alisijainti, valitse ylätason sijainti **Ylätaso**-kentässä.
6. Valitse tyyppi **Toiminnallisen sijainnin tyyppi** -kentässä.
7. Valitse **OK**.
8. Valitse toiminnallinen sijainti ja lisää lisätietoja napsauttamalla **Muokkaa**-painiketta.

>[!NOTE]
>Toiminnallisen sijainnin elinkaaren tilan määritysten mukaan sinun on ehkä luotava kaikki alisijainnit toiminnalliseen sijaintiin ja muutettava sitten toiminnallisen sijainnin elinkaaren tilaa, ennen kuin voit aloittaa resurssien asentamisen. Lisätietoja resurssien asentamisesta on kohdassa [Asenna toiminnallisten sijaintien resurssit](../functional-locations/install-objects-on-functional-locations.md). Lisätietoja toiminnallisen sijainnin elinkaaritilojen määrittämisestä on kohdassa [Toiminnallisen sijainnin elinkaaren tilat](../setup-for-functional-locations/functional-location-stages.md).

Tiedot-näkymän pikavälilehdissä voit lisätä ja muokata toiminnallisen sijainnin tietoja.

## <a name="general-information"></a>Yleistiedot

Tässä osassa on ylätason ja alitason itietojen yleiskatsaus toiminnallisen sijainnin rakenteessa. **Tiedot** osassa näet, kuinka useita resurssimääritteitä, ylläpitosuunnitelmia ja toiminnalliseen sijaintiin liittyviä resursseja on. **Varasto**-osassa voidaan valita toimipaikka ja varasto, johon toiminnallinen sijainti liittyy. Toimipaikkaa ja varastoa käytetään työtilauksen nimike-ennusteiden yhteydessä. Kun luodaan nimike-ennustetta, toimipaikan ja varaston tietoja käytetään automaattisesti resurssin toiminnallisesta sijainnista. **Elinkaaren tila** -osassa näytetään tietoja toiminnallisen sijainnin elinkaaren tilasta.

## <a name="installed-assets"></a>Asennetut resurssit

Lisätietoja resurssien asentamisesta on kohdassa [Asenna toiminnallisten sijaintien resurssit](../functional-locations/install-objects-on-functional-locations.md). Tämän pikavälilehden **Näytä**-painikkeen avulla voit näyttää lisää pikavälilehden kenttiä. Ruudukossa voidaan näyttää **Voimassaolo alkaa**- ja **Aliresurssit** -kentät.

## <a name="asset-attribute-requirements"></a>Resurssien määritteiden vaatimukset

Tässä pikavälilehdessä voidaan lisätä tiettyjä määritevaatimuksia resursseille, jotka asennetaan toiminnalliseen sijaintiin. Nämä vaatimukset ovat vain tiedoksi. Ne eivät estä sinua asentamasta resursseja muiden määritevaatimusten kanssa. Valitse **Lisää rivi** ja valitse määritetyyppi. Lisää sitten asiaankuuluva **Arvo**, valitse kynnys **Raja-arvon ehto** -kentässä ja tallenna tietue.

## <a name="maintenance-plans-and-maintenance-rounds"></a>Huoltosuunnitelmat ja huoltokierrokset

Tässä voit lisätä huoltosuunnitelmia ja huoltokierroksia toiminnalliseen sijaintiin, mukaan lukien alkamispäivämäärän. Toiminnalliseen sijaintiin asennetuilla resursseilla voi olla määritetty muita ylläpitosuunnitelmia. Kaikkia ylläpitosuunnitelmia ja ylläpitokierroksia voidaan käyttää resurssikalenterin tapahtumien ajoittamiseen toiminnalliseen sijaintiin ja sen tällä hetkellä asennettuihin resursseihin.

>[!NOTE]
>Jos päivität resurssityyppien, resurssien merkkien ja resurssien mallien asetukset ylläpitosuunnitelmille **Kaikki toiminnalliset sijainnit** -tietonäkymän **Ylläpitosuunnitelmat**-pikavälilehdessä ja olet suunnitellut kunnossapitosuunnitelmat, aiemmin luodut kyseiseen toiminnalliseen sijaintiin liittyvät kunnossapitoaikataulun merkinnät poistetaan automaattisesti. Jotta voit luoda uusia aikataulumerkintöjä, jotka vastaavat toiminnallisen sijainnin päivitettyjä ylläpitosuunnitelman asetuksia, sinun on suoritettava kyseiselle toiminnalliselle sijainnille uusi ylläpitosuunnitelman aikataulu. 

## <a name="address"></a>Osoite

Lisää toiminnallisen sijainnin osoite **Osoite**-pikavälilehdessä. Toiminnallisten sijaintien osoitteet periytyvät, mikä tarkoittaa, että jos alisijainnissa ei ole määritettyä osoitetta, käytetään ylätason sijainnin osoitetta.

## <a name="workers"></a>Työntekijät

Tässä pikavälilehdessä voit lisätä toimintosijaintiin liittyviä työntekijöitä, ja voit valita toimipaikan ensisijaiseksi työntekijälle. 

## <a name="attributes"></a>Ominaisuudet

Tässä pikavälilehdessä voit määrittää toiminnallisen siajinnin määritteiden arvot. Näiden määritteiden avulla voidaan kuvata ominaisuuksia, jotka liittyvät toiminnalliseen sijaintiin, esimerkiksi rakenneominaisuuksiin, rakennustyyppiin, aluekuvauksiin tai sijaintiin maan ylä- tai alapuolella.

Valitse **Lisää rivi** ja valitse määritetyyppi. Lisää seuraavaksi määritetyyppiin liittyvä **Arvo** ja tallenna tietue.

## <a name="financial-dimensions"></a>Taloushallinnon dimensiot

Voit valita toiminnalliselle sijainnille taloushallinnon dimensiot. [Toiminnallisen sijainnin tyypit](../setup-for-functional-locations/functional-location-types.md) voidaan määrittää siten, että taloushallinnon dimensiot päivitetään automaattisesti toiminnallisesta sijainnista. Tämä tarkoittaa, että taloushallinnon dimensioon asennetut resurssit saavat automaattisesti taloushallinnon dimensiot toiminnallisesta sijainnista. Tästä on hyötyä, jos haluat käyttää eri kustannuspaikkoja sijaintien mukaan.

Kun tietoja, jotka liittyvät kohteisiin **Toimipaikka**, **Varasto**, **Osoite** ja **taloushallinnon dimensiot**, päivitetään ylätason toiminnallisessa sijainnissa, toiminnalliset alisijainnit voidaan päivittää vastaavasti, jos teet tämän valinnan päivityksen aikana. Näyttöön tulee valintaikkuna, joka sisältää päivitysvaihtoehdot.

## <a name="copy-a-functional-location-structure"></a>Kopioi toiminnallisen sijainnin rakenne

Jos yrityksellä on useita toiminnallisia sijainteja, joissa on samanlaiset sijaintirakenteet, voit luoda nopeasti useita samankaltaisia sijaintihierarkioita käyttämällä resurssien hallinnan kopiointitoimintoa. Kun kopioit tietyn toimintosijainnin tai koko rakenteen, uudella sijainnilla tai rakenteella on sama nimi kuin kopioitavalla nimellä. Kun kopiointi on valmis, voit helposti muuttaa nimeä tai muita asetuksia uudessa toimintosijainnissa, jos uuden toimintosijainnin toimintosijainnin elinkaaritila sallii sen.

1. Valitse **Kaikki toiminnalliset sijainnit**-kohdasta kopioitava toiminnallinen sijainti. Voit esimerkiksi valita ylimmän sijainnin (pääkohde), jos haluat kopioida koko toiminallisen sijainnin rakenteen, mukaan lukien alisijainnit.
2. Valitse **Kopioi toiminnallisen sijainnin rakenne** -painike. Luettelosivulla valitsemasi sijainti näkyy **Kopioi kohteesta** -kentässä.
3. Lisää uuden sijainnin nimi **Uusi toiminnallinen sijainti** -kenttään.
4. **Ylätaso, johon liitetään** -kenttään lisätään vain päätunnus, jos luotavan sijainnin on oltava osa aiemmin luotua toiminnallista sijaintirakennetta.
5. Valitse **OK**. Uusi toiminnallinen sijaintirakenne näkyy **Kaikki toiminnalliset sijainnit** -kohdassa.

>[!NOTE]
>Kun kopioit toiminallisen sijaintirakenteen, toimintojen sijainnin elinkaaritilat uudessa rakenteessa määritetään "ensimmäiseksi tilaksi", jonka olet luonut toiminnallisille sijainneille. Sen, voitko nimetä toimipaikan uudelleen tai poistaa sen käyttämällä **Kaikki toiminnalliset sijainnit** -kohdassa **Nimeä uudelleen**- ja **Poista**-painikkeita, määräytyy toimintoijainnin nykyisen elinkaaritilan mukaan.

## <a name="delete-a-functional-location"></a>Toiminnalliset sijainnin poistaminen

Toiminnallinen sijainti ja siihen liittyvät alisijainnit voidaan poistaa, jos mitään resursseja ei ole asennettu mihinkään toimintosijaintiin, jota yrität poistaa, ja jos nykyinen toimintosijainnin elinkaaritila sallii sen.

1. Valitse **Kaikki toiminnalliset sijainnit**-kohdasta poistettava toiminnallinen sijainti.
2. Päivitä tarvittaessa toiminnallinen sijainti toimintosijainnin elinkaaritilaan, joka sallii toimintosijainnin poistamisen.
3. Valitse **Poista**.

>[!NOTE]
>Jos et voi poistaa toiminnallista sijaintia, voit sen sijaan käsitellä poistoa määrittämällä tähän tarkoitukseen toimintosijainnin elinkaaritilan. Voit esimerkiksi määrittää "Hävikki"- tai "Poistettu"-vaiheen, joka ei saa olla aktiivinen vaihe, **Toiminnallisen sijainnin elinkaaren tilat** -lomakkeessa.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]