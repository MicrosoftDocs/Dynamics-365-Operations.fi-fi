---
title: Ostotilauksen luominen
description: Tässä aiheessa näytetään, miten ostotilaus luodaan manuaalisesti.
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventDimParmFixed, InventItemIdLookupPurchase, InventProductDimensionLookup, PurchTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec91174f291bcfa7027a93ca344823561cc29e3f
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018148"
---
# <a name="create-a-purchase-order"></a>Ostotilauksen luominen

[!include [banner](../../includes/banner.md)]

Tässä aiheessa näytetään, miten ostotilaus luodaan manuaalisesti. Ostotilaukset luodaan yleensä automaattisesti pääsuunnittelun, suoratoimituksen ja muiden prosessien tuloksena. Ostotilaukset luo yleensä ostoedustaja. Tätä esimerkkiä voidaan käyttää USMF-esimerkkiyrityksessä eri vaiheiden muistiinpanoissa ehdotetuin arvoin.


## <a name="create-the-purchase-order-header"></a>Luo ostotilauksen otsikko
1. Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Ostotilaukset > Kaikki ostotilaukset**.
2. Valitse **Uusi**.
3. Valitse toimittajan tili **US-101**. Kun valitset toimittajan, toimittajatietueen tiedot, kuten osoite, laskutustili, toimitusehdot ja -tapa kopioidaan oletusarvoina tilauksen otsikkoon. Voit muuttaa näitä arvoja milloin tahansa.  
4. Laajenna **Yleiset** -osa.

    - **Toimipiste** -kenttä ja **Varasto** -kenttä määrittävät yhdessä, mihin hankitut tuotteet tai palvelut tulee toimittaa. Oletustoimitusosoite on toimipaikan osoite. Molempiin kenttiin voidaan esitäyttää valitulle toimittajalle määritetyt arvot, tai ne voidaan määrittää manuaalisesti.  
    - **Toimituspäivä** -kentässä määritetään, milloin hankitut tuotteet ja palvelut tulisi toimittaa. Voit määrittää koko tilauksella yhden toimituspäivän tai omat toimituspäivät yksittäisille tilausriveille. Jos tässä määritettyä toimituspäivää ei voida toteuttaa tiettyjen tuotteiden tai palveluiden kohdalla, koska niiden läpimenoajat ovat pidempiä, niiden tilausriveille annetaan myöhempi toimituspäivä, jotta ne voidaan käsitellä.  

5. Laajenna **Hallinta** -osa. Tilauksen tehneen henkilön voi määrittää **Tilaaja** -kentässä. Tämän jakaminen toimittajalle voi olla hyödyksi, jos ko. henkilöön on otettava yhteyttä. Kentän arvo voi olla määritetty automaattisesti, jos kirjautuneen käyttäjän tili on liitetty nimeen **Käyttäjät** -sivulla.  
6. Valitse **OK**. Tilauksen otsikko on nyt luotu. Ostotilausrivejä käsiteltäessä näytetään ainoastaan yhteenveto otsikkotiedoista. Jos haluat nähdä tarkat tiedot, valitse **Otsikko**.  

## <a name="add-a-purchase-order-line"></a>Ostotilausrivin lisääminen
1. Valitse **Ostotilausrivi**.
2. Valitse **Dimensiot**. Tuotteilla voi olla variantteja, jotka eroavat toisistaan dimensioiden, kuten värin, koon tai tyylin perusteella. Tuotteet voidaan myös asettaa käyttämään varastodimensioita, kuten toimipaikkaa ja varastoa. Käytettävissä on myös valinnaisia seurantadimensioita, kuten erä- ja sarjanumerot. Tilaustenkäsittelyn tehokkuuden parantamiseksi voit lisätä useimmin käytetyt dimensiokentät suoraan tilausruudukkoon.  
3. Merkitse **Väri** -valintaruutu. Valinnainen: Jos valitset **Tallenna asetukset** -kentän, valitsemasi dimensiot näytetään myös tilausrivien ruudukossa seuraavalla kerralla, kun avaat ostotilauksen sivun.  
4. Valitse **OK**.
5. Valitse **Nimikkeen numero** -kentässä **T0004**.

    - Tilausrivit luodaan tuotteille ja palveluille määrittämällä nimikenumero tai kuluina määrittämällä hankintaluokka. 
    - **Hankintaluokka** -kentän avulla lisätään rivejä, joiden hankittujen nimikkeiden kulut kirjataan suoraan varastoon siirtämisen sijasta. Tämä tarkoittaa että, jos oston kulu on kirjattava suoraan, sen voi tehdä luomalla ostotilausrivin, joka osoittaa hankintaluokan sen sijaan, että loisit rivin, jolla on nimiketunnus. Nimikkeitä voi myös liittää hankintaluokkaan ja tällöin hankintaluokan näytetään ainoastaan tiedoksi.  

6. Syötä tai valitse **Väri** -kentän arvo. **Toimipaikka** - ja **Varasto** -kenttiin täytetään yleensä automaattisesti tilausotsikon arvot, mutta kentät on mahdollista ohittaa, jos jotkin rivit on toimitettava eri sijainteihin.  
7. Anna **Määrä** -kentässä numero.

    - Valitse määrä, jonka haluat ostaa. **Määrä** -kenttä täytetään automaattisesti tuotteen vähimmäistilausmäärällä, jos sellainen on määritetty, tai arvolla 1.  
    - **Yksikkö** -kenttä ilmaisee tilatun määrän mittayksikön. Yleensä yksikkö annetaan automaattisesti päätuotteen tietojen ostoyksiköstä, mutta tämän voi muuttaa.  
    - **Yksikköhinta** -kentässä on tavallisesti arvo joko osto- tai kauppasopimuksesta. Yksikköhinnan voi muuttaa kullekin tilausriville, jos toimittajan kanssa on neuvoteltu esimerkiksi erillinen hinta.  
    - **Alennus** -kenttä edustaa tuoteyksikkökohtaista alennussummaa. Tämä alennus siis laskee yksikköhintaa alennuksen verran. Alennus annetaan yleensä automaattisesti osto- tai kauppasopimuksesta, mutta se on mahdollista ohittaa yksittäisillä riveillä, jos toimittajan kanssa on neuvoteltu erillisiä alennuksia.  
    - Alennusprosentti voidaan lisätä, joka vähentää rivin nettosummaa vastaavasti. Alennusprosentti annetaan usein automaattisesti osto- tai kauppasopimuksesta, mutta se on mahdollista ohittaa yksittäisillä riveillä, jos toimittajan kanssa on neuvoteltu erillisiä alennusprosentteja.  
    - **Nettosumma** -kentän arvo lasketaan muista rivin kentistä, kuten määrä, yksikköhinta, alennus ja alennusprosentti. Voit muuttaa nettosumman, mutta **Yksikköhinta** -, **Alennus** - ja **Alennusprosentti** -kentät ovat tyhjiä, ja kun teet kirjauksen riville, kirjattu summa on suhteessa nettosummaan. Yleensä **Nettosumma** -kenttää käytetään ainoastaan rivin nettosumman esittämiseen.  

8. Laajenna **Rivin erittely** -osa.
9. Valitse **Toimitus** -välilehti. Kullekin tilausriville voi määrittää yksilöllisen toimituspäivän. Päivämäärä periytyy ostotilauksen otsikon kentästä, mutta sen voi muuttaa.  

## <a name="review-order-totals"></a>Tilauksen kokonaissummien tarkastelu
1. Valitse **Summat**.

    - Jos et näe **Summat** -toimintoa, valitse **Ostotilaus** -välilehti toimintoruudussa.  
    - Tässä valintaikkunassa esitetään koko tilauksen kokonaissummat.  
    - **Valinta** -kentän avulla voit muuttaa kokonaissummien laskentaperusteen. Voit esimerkiksi valita **Tuotteen vastaanottomäärä** -kentän, jos haluat esittää kokonaissummat, jotka liittyvät vastaanotettujen tuotteiden määrään, tai **Tilattu määrä** -kentän, jos haluat esittää tuotteen tilausmäärät.  

2. Valitse **OK**.

