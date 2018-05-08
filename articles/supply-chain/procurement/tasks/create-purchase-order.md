--- 
title: Luo ostotilaus
description: "Tässä menettelyssä näytetään, miten ostotilaus luodaan manuaalisesti."
author: FrankDahl
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 27ed15e6d9a376c4203e5446d056f221bd3eb730
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order"></a>Luo ostotilaus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä näytetään, miten ostotilaus luodaan manuaalisesti. Ostotilaukset luodaan yleensä automaattisesti pääsuunnittelun, suoratoimituksen ja muiden prosessien tuloksena. Ostotilaukset luo yleensä ostoedustaja. Tätä esimerkkiä voidaan käyttää USMF-esimerkkiyrityksessä eri vaiheiden muistiinpanoissa ehdotetuin arvoin.


## <a name="create-the-purchase-order-header"></a>Luo ostotilauksen otsikko
1. Valitse Hankinta > Ostotilaukset > Kaikki ostotilaukset.
2. Valitse Uusi.
3. Valitse toimittajan tili US-101.
    * Kun valitset toimittajan, toimittajatietueen tiedot, kuten osoite, laskutustili, toimitusehdot ja -tapa kopioidaan oletusarvoina tilauksen otsikkoon. Voit muuttaa näitä arvoja milloin tahansa.  
4. Laajenna Yleiset-osa.
    * Toimipiste-kenttä ja Varasto-kenttä määrittävät yhdessä, mihin hankitut tuotteet tai palvelut tulee toimittaa. Oletustoimitusosoite on toimipaikan osoite. Molempiin kenttiin voidaan esitäyttää valitulle toimittajalle määritetyt arvot, tai ne voidaan määrittää manuaalisesti.  
    * Toimituspäivä-kentässä määritetään, milloin hankitut tuotteet ja palvelut tulisi toimittaa. Voit määrittää koko tilauksella yhden toimituspäivän tai omat toimituspäivät yksittäisille tilausriveille. Jos tässä määritettyä toimituspäivää ei voida toteuttaa tiettyjen tuotteiden tai palveluiden kohdalla, koska niiden läpimenoajat ovat pidempiä, niiden tilausriveille annetaan myöhempi toimituspäivä, jotta ne voidaan käsitellä.  
5. Tiivistä Yleinen-osa.
6. Laajenna Hallinta-osa.
    * Tilauksen tehneen henkilön voi määrittää Tilaaja-kentässä. Tämän jakaminen toimittajalle voi olla hyödyksi, jos ko. henkilöön on otettava yhteyttä. Kentän arvo voi olla määritetty automaattisesti, jos kirjautuneen käyttäjän tili on liitetty nimeen Käyttäjät-sivulla.  
7. Tiivistä Hallinta-osa.
8. Valitse OK.
    * Tilauksen otsikko on nyt luotu. Ostotilausrivejä käsiteltäessä näytetään ainoastaan yhteenveto otsikkotiedoista. Jos haluat nähdä tarkat tiedot, napsauta otsikkoa.  

## <a name="add-a-purchase-order-line"></a>Ostotilausrivin lisääminen
1. Valitse Ostotilausrivi.
2. Valitse Dimensiot.
    * Tuotteilla voi olla variantteja, jotka eroavat toisistaan dimensioiden, kuten värin, koon tai tyylin perusteella. Tuotteet voidaan myös asettaa käyttämään varastodimensioita, kuten toimipaikkaa ja varastoa. Käytettävissä on myös valinnaisia seurantadimensioita, kuten erä- ja sarjanumerot. Tilaustenkäsittelyn tehokkuuden parantamiseksi voit lisätä useimmin käytetyt dimensiokentät suoraan tilausruudukkoon.  
3. Merkitse Väri-valintaruutu.
    * Valinnainen: Jos valitset Tallenna asetukset -kentän, valitsemasi dimensiot näytetään myös tilausrivien ruudukossa seuraavalla kerralla, kun avaat ostotilauksen sivun.  
4. Valitse OK.
5. Valitse Nimiketunnus-kenttään T0004.
    * Tilausrivit luodaan tuotteille ja palveluille määrittämällä nimikenumero tai kuluina määrittämällä hankintaluokka.  
    * Hankintaluokka -kentän avulla lisätään rivejä, joiden hankittujen nimikkeiden kulut kirjataan suoraan varastoon siirtämisen sijasta. Tämä tarkoittaa että, jos oston kulu on kirjattava suoraan, sen voi tehdä luomalla ostotilausrivin, joka osoittaa hankintaluokan sen sijaan, että loisit rivin, jolla on nimiketunnus. Nimikkeitä voi myös liittää hankintaluokkaan ja tällöin hankintaluokan näytetään ainoastaan tiedoksi.  
6. Syötä tai valitse Väri-kentän arvo.
    * Toimipaikka- ja Varasto-kenttiin täytetään yleensä automaattisesti tilausotsikon arvot, mutta kentät on mahdollista ohittaa, jos jotkin rivit on toimitettava eri sijainteihin.  
7. Kirjoita numero Määrä-kenttään.
    * Valitse määrä, jonka haluat ostaa. Määrä-kenttä täytetään automaattisesti tuotteen vähimmäistilausmäärällä, jos sellainen on määritetty, tai arvolla 1.  
    * Yksikkö-kenttä ilmaisee tilatun määrän mittayksikön. Yleensä yksikkö annetaan automaattisesti päätuotteen tietojen ostoyksiköstä, mutta tämän voi muuttaa.  
    * Yksikköhinta-kentässä on tavallisesti arvo joko osto- tai kauppasopimuksesta. Yksikköhinnan voi muuttaa kullekin tilausriville, jos toimittajan kanssa on neuvoteltu esimerkiksi erillinen hinta.  
    * Alennus-kenttä edustaa tuoteyksikkökohtaista alennussummaa. Tämä alennus siis laskee yksikköhintaa alennuksen verran. Alennus annetaan yleensä automaattisesti osto- tai kauppasopimuksesta, mutta se on mahdollista ohittaa yksittäisillä riveillä, jos toimittajan kanssa on neuvoteltu erillisiä alennuksia.  
    * Alennusprosentti voidaan lisätä, joka vähentää rivin nettosummaa vastaavasti. Alennusprosentti annetaan usein automaattisesti osto- tai kauppasopimuksesta, mutta se on mahdollista ohittaa yksittäisillä riveillä, jos toimittajan kanssa on neuvoteltu erillisiä alennusprosentteja.  
    * Nettosumma-kentän arvo lasketaan muista rivin kentistä, kuten määrä, yksikköhinta, alennus ja alennusprosentti. Voit muuttaa nettosumman, mutta yksikköhinta-, alennus- ja alennusprosentti-kentät ovat tyhjiä, ja kun teet kirjauksen riville, kirjattu summa on suhteessa nettosummaan. Yleensä nettosummakenttää käytetään ainoastaan rivin nettosumman esittämiseen.  
8. Laajenna Rivin erittely -osa.
9. Valitse Toimitus-välilehti.
    * Kullekin tilausriville voi määrittää yksilöllisen toimituspäivän. Päivämäärä periytyy ostotilauksen otsikon kentästä, mutta sen voi muuttaa.  
10. Tiivistä Rivitiedot-osa.

## <a name="review-order-totals"></a>Tilauksen kokonaissummien tarkastelu
1. Valitse Summat.
    * Jos et näe Summat-toimintoa, napsauta Ostotilaus-välilehteä toimintoriviltä.  
    * Tässä valintaikkunassa esitetään koko tilauksen kokonaissummat.  
    * Valinta-kentän avulla voit muuttaa kokonaissummien laskentaperusteen. Voit esimerkiksi valita Tuotteen vastaanottomäärän, jos haluat esittää kokonaissummat, jotka liittyvät vastaanotettujen tuotteiden määrään, tai Tilatun määrän, jos haluat esittää tuotteen tilausmäärät.  
2. Valitse OK.


