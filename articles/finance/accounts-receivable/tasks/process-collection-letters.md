---
title: Käsittele maksukehotuksia
description: Tässä aiheessa käsitellään, miten maksukehotuksia luodaan, tulostetaan ja kirjataan.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 2b8ce102086535a5462d3fa0e8ac76e9ec3dd15c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442704"
---
# <a name="process-collection-letters"></a>Käsittele maksukehotuksia

[!include [banner](../../includes/banner.md)]

Tässä aiheessa käsitellään, miten maksukehotuksia luodaan, tulostetaan ja kirjataan. Tässä tehtävässä käytetään esittely-yritystä USMF.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Määritä maksukehotusjärjestys kirjausprofiilissa
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Luotonvalvonta > Asetukset > Asiakkaan kirjausprofiilit**.
2. Valitse **Muokkaa**.
3. Valitse maksukehotussarja avattavasta luettelosta. Jos et halua luoda maksukehotuksia tapahtumille tämän kirjausprofiilin avulla, jätä kenttä tyhjäksi.  
4. Laajenna **Taulurajoitus**-välilehti ja muuta tapaa, jolla maksukehotuksia käsitellään. Jos kentän arvoksi on määritetty **Kyllä**, tälle kirjausprofiilille luodaan maksukehotus.  

## <a name="create-collection-letters"></a>Luo maksukehotukset
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Luotonvalvonta > Maksukehotus > Luo maksukehotukset**.
2. Valitse tapahtumatyypit, joissa käytetään maksukehotuksia. Kaikki tämän tyyppiset avoimet tapahtumat sisällytetään laskentaan.  
3. Valitse asetus **Maksukehotus**-kentässä.
4. Lisää **Maksukehotuksen päivämäärä** -kenttään maksukehotuksen päivämäärä.
5. Valitse kirjausprofiili, jos muutit **Käytettävä kirjausprofiili** -asetukseksi **Valitse**. Käytettävissä ovat seuraavat kaksi kirjausprofiilivaihtoehtoa:   

   - **Tili** – Käytä kunkin korkolaskun asiakastilille määritettyä kirjausprofiilia.   
   - **Valitse** – Käytä **Kirjausprofiili**-kentässä valittavaa kirjausprofiilia.  

6. Laajenna **Sisällytettävät tietueet** -osa.
7. Valitse **Suodata**.
8. Anna **Ehdot**-kentässä asiakkaan tunnus. Syötä arvoksi esimerkiksi US-001.
9. Valitse **OK**.
10. Valitse **OK**.

## <a name="print-collection-letters"></a>Tulostaa maksukehotukset
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Luotonvalvonta > Maksukehotus > Tarkastele ja käsittele maksukehotuksia**.
2. Valitse **Tila**-kentässä **Luotu**.
3. Valitse **Tulostettu**-kentässä **Ei tulostettu**.
4. Valitse **Tulosta**.
5. Valitse **Maksukehotus**.
6. Kirjoita **Parametrit** -osaan kirjausten katkaisupäivämäärä.
7. Laajenna **Sisällytettävät tietueet** -osa ja kirjoita maksukehotushuomautuksen tiedot.
8. Tulosta maksukehotus valitsemalla **OK**.
9. Kirjaa maksukehotus.

    1. Valitse **Kirjaa**.
    1. Anna maksukehotuksen kirjauspäivämäärä.
    1. Laajenna **Sisällytettävät tietueet** -osa.
    1. Valitse **OK**.
    1. Valitse **Tila**-kentässä **Kirjattu**.
    1. Valitse asetus **Tulostettu**-kentässä.

## <a name="control-collection-letters-at-the-customer-level"></a>Maksukehotusten hallinta asiakastasolla
Jos maksukehotukset määritetään tapahtumatasolla, asiakkaalle voidaan luoda useita kehotuksia tapahtuman vanhentumisen perusteella. Jos tapahtuma näkyy eri kehotussarjoissa, erilliset maksukehotukset luodaan jokaiselle asiakkaan eräätyneiden tapahtumien ryhmälle. Tämän vuoksi yksittäinen asiakas saattaa vastaanottaa esimerkiksi yhden maksukehotuksen 60 päivää vanhasta tapahtumasta ja toisen maksukehotuksen tapahtumista, jotka ovat erääntyneet 90 päivää sitten. 

Kukin maksukehotus liittyy myös maksukehotuskoodiin. Maksukehotuskoodi liittyy yksittäisiin tapahtumiin. Sen avulla määritetään, milloin seuraava maksukehotus luodaan kullekin tapahtumalle. Jos tapahtuma on esimerkiksi 30 päivää myöhässä, maksukehotuskoodi määrittää, että seuraava maksukehotuys lähetetään tapahtuman ollessa 60 päivää myöhässä, jos sitä ei makseta ennen tätä. 

Maksukehotukset voidaan määrittää myös asiakastasolla. Tässä tapauksessa voit määrittää maksukehotukset myös asiakastasolla, jolloin kunkin tapahtuman maksukehotuskoodia seurataan. Maksukehotuksen käsittely perustuu kuitenkin yhteen asiakkaalle tallennettuun maksukehotetasoon. Yksi maksukehotus sisältää kaikki kyseisen asiakkaan erääntyneet tapahtumat. Koska eräpäivän jälkeistä maksuaikaa seurataan nyt asiakastasolla, seuraavaa maksukehotusta ei lähetetä, ennen kuin tietty määrä päiviä sarjan seuraavan maksukehotuksen eräpäivän jälkeistä maksuaika on kulunut, vaikka tapahtumat erääntyvät sen jälkeen, kun viimeisin maksukehotus on lähetetty. Tämä asetus auttaa vähentämään kullekin asiakkaalle lähetettävien maksukehotusten määrää.

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Asiakkaan määrittäminen maksukehotusten hallintaan asiakastasolla
1.  Valitse ensin **Siirtymisruutu > Moduulit > Luotonvalvonta > Asetukset > Myyntireskontran parametrit** ja sitten **Perintä**-välilehti. 
2.  Muuta **Luo maksukehotus per** -arvoksi **Asiakas**. 
3.  Siirry kohtaan **Siirtymisruutu > Moduulit > Luotonvalvonta > Maksukehotus > Tarkastele ja käsittele maksukehotuksia**. Asiakkaan kaikille erääntyneille tapahtumille luodaan vain yksi maksukehotus.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Maksujen ja hyvityslaskujen ohittaminen maksukehotuksen koodia laskettaessa
Jos sisällytät maksukehotuksiin sisältyviin tapahtumiin maksuja ja hyvityslaskuja, sinulla voi olla maksukehotuksen käynnistäviä maksuja tai hyvityslaskuja. Voit hallita, miten maksut ja hyvityslaskut hallitsevat maksukehotuskoodia vaihtamalla **Älä huomioi maksuja tai hyvityslaskuja maksukehotuksen koodin laskemisessa** -parametrin arvon. 

Ohita maksut ja hyvityslaskut maksukehotuksen koodia laskettaessa seuraavasti.

1. Valitse ensin **Siirtymisruutu > Moduulit > Luotonvalvonta > Asetukset > Myyntireskontran parametrit** ja sitten **Perintä**-välilehti. 
2. Vaihda **Älä huomioi maksuja tai hyvityslaskuja maksukehotuksen koodin laskemisessa** -arvoksi **Kyllä**.
