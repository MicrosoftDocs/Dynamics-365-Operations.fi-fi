--- 
title: "Syötä ja vertaa tarjouspyyntöjä ja myönnä sopimuksia"
description: "Seuraavassa menettelyssä kuvataan tarjouspyynnön vastauksien kirjoittaminen, tarjousten pisteytys ja vertailu, sekä tarjouksen antaminen yhdelle toimittajista."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d7c76eab2cca4e15c13dd9f79432b9c6d81071a2
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Syötä ja vertaa tarjouspyyntöjä ja myönnä sopimuksia

[!include[task guide banner](../../includes/task-guide-banner.md)]

Seuraavassa menettelyssä kuvataan tarjouspyynnön vastauksien kirjoittaminen, tarjousten pisteytys ja vertailu, sekä tarjouksen antaminen yhdelle toimittajista. Voit käyttää tätä menettelyä esittely-yrityksessä USMF. Ennen kuin aloitat, varmista, että sinulla on tarjouspyyntö, joka sisältää kaksi riviä ja joka on lähetetty vähintään kahdelle toimittajalle. Voit ajaa "Luo tarjouspyyntö" -toimintosarjan luodaksesi tämän edellytyksen. Pisteytysehdot on määritettävä ennen tämän menettelyn suorittamista.


## <a name="enter-a-reply-from-a-vendor"></a>Kirjoita toimittajan vastaus
1. Valitse Hankinta > Tarjouspyynnöt > Kaikki tarjouspyynnöt.
2. Valitse tarjouspyyntö, jonka tila on lähetetty ja napsauta tarjouspyynnön tapausnumeron linkkiä.
    * Tarjouspyyntö tulisi lähettää vähintään 2 toimittajalle.  
3. Napsauta otsikkoa siirtyäksesi toimittajien luetteloon.
4. Valitse toimittaja, jolle haluat kirjoittaa vastauksen tarjouspyyntöön.
5. Napsauta Kirjoita vastaus -kohtaa.
6. Valitse toimintoruudussa Vastaa.
7. Napsauta Kopioi tiedot vastauskenttiin -kohtaa.
    * Toiminto kopioi valitut tiedot, esimerkiksi määrän tarjouspyynnön tapauksesta tarjouspyynnön vastaukseen. Voit ohittaa tämän toiminnon ja täyttää vastauskentät manuaalisesti, kun muokkaat vastausta.  
8. Valitse Muokkaa.
9. Syötä Yksikköhinta-kenttään numero.
10. Valitse toinen tarjousrivi.
11. Syötä Yksikköhinta-kenttään numero.

## <a name="score-the-bid"></a>Pisteytä tarjous
1. Napsauta otsikkoa siirtyäksesi tarjouksen pisteytykseen.
2. Laajenna Tarjouksen pisteytys -osa.
3. Kirjoita Tulos-kenttään jokin pisteytysehdon numero.
    * Jos pidät kohdistinta pisteytysperusteen yllä, työkaluvihjeen näyttää alueen, jolle pisteytys on annettava. Tässä demossa voit lisätä numeron väliltä 1-5 mihin tahansa perusteeseen.  
4. Valitse toinen pisteytysehto.
5. Kirjoita Tulos-kenttään numero.
6. Laajenna Kyselylomakkeet-osa.
    * Jos tarjouspyynnön tapauksessa on kyselylomake, joka on lähetetty toimittajille, voit kirjoittaa vastaukset kyselylomakkeen osaan.  
7. Sulje sivu.

## <a name="enter-a-reply-for-another-vendor"></a>Kirjoita toisen toimittajan vastaus
1. Valitse seuraava toimittaja poistamalla kentästä se toimittaja,jolle olet kirjoittanut vastauksen ja valitsemalla sitten seuraavan toimittajan rivi.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta Kirjoita vastaus -kohtaa.
4. Napsauta Kopioi tiedot vastauskenttiin -kohtaa.
5. Valitse Muokkaa.
6. Syötä Yksikköhinta-kenttään numero.
7. Valitse toinen tarjousrivi.
8. Syötä Yksikköhinta-kenttään numero.

## <a name="score-the-second-bid"></a>Pisteytä toinen tarjous
1. Napsauta otsikkoa siirtyäksesi tarjouksen pisteytykseen.
2. Kirjoita Tulos-kenttään numero.
3. Etsi haluamasi tietue luettelosta ja valitse se.
4. Kirjoita Tulos-kenttään numero.

## <a name="compare-the-replies"></a>Vertaa vastauksia
1. Valitse toimintoruudussa Yleiset.
2. Napsauta Vertaa vastauksia -kohtaa.
3. Kirjoita Sijoitus-kenttään numero.
    * Tällä sivulla näytetään tarjoukset otsikossa ja riveillä, ja kokonaispistemäärä otsikon tasolla. Voit verrata rivejä lajittelemalla ruudukon siten, että vertailtavat rivit ovat vierekkäin. Tietoihin sisältyy myös: Määrä: toimittajan tarjoama määrä. Tämä määrä ei ehkä vastaa tarjouspyynnössä määritettyä määrää.   Nettosumma: Toimittajan tarjouksen hinta rivin nimikkeistä alennusten vähentämisen jälkeen.   Poikkeama: Päivien määrä, jonka verran tarjouksen otsikon tai rivin toimituspäivämäärä poikkeaa tarjouspyynnön otsikon tai tarjouspyynnön rivin pyydetystä toimituspäivämäärästä.   Voit määrittää kullekin tarjoukselle sijoituksen.  
4. Valitse sijoitettavan tarjouksen otsikkorivi.
5. Kirjoita Sijoitus-kenttään numero.
6. Valitse Tallenna.

## <a name="reject-a-bid"></a>Hylkää tarjous
1. Valitse hylättävän tarjouksen otsikkorivi.
    * Voit hyväksyä, hylätä tai palauttaa vain yhden tarjouksen tai yhden tarjouksen rivejä kerralla.  
2. Valitse Merkitse-valintaruutu.
    * Jos valitset Merkitse-valintaruudun tarjouksen otsikossa, kaikki tarjouksen rivit merkitään lisäksi. Voit myös merkitä osan tarjouksen riveistä hylättäväksi tai hyväksyttäväksi. On mahdollista hyväksyä yhden toimittajan tarjous tietyille tarjouspyynnön riveille ja antaa muut tarjouspyynnön rivit toiselle toimittajalle; tämä on kuitenkin tehtävä 2 vaiheessa, yksi tarjous kerrallaan. Jos on olemassa vaihtoehtoisia rivejä, voit hyväksyä vain joko alkuperäisen tarjousrivin tai sen vaihtoehdon, mutta et molempia.  
3. Napsauta Hylkää.
4. Avaa valintaikkuna valitsemalla Parametrit.
5. Anna tai valitse Hylkäyksen syy -kenttään arvo.
    * Vastaukseen tallennetaan hylkäyksen syy.  
6. Valitse OK.
7. Valitse OK.
8. Sulje sivu.
9. Sulje sivu.
10. Päivitä sivu.

## <a name="accept-a-bid"></a>Hyväksy tarjous
1. Valitse tarjous, jonka haluat hyväksyä ja napsauta sitten tarjouspyyntökentän linkkiä.
2. Valitse toimintoruudussa Vastaa.
3. Valitse Hyväksy.
    * Jos olet merkinnyt tiettyjä rivejä mutta jättänyt muita merkitsemättä, Hyväksy-toimenpide sisältää vain merkityt rivit. Voit hyväksyä kaikki tarjouksen rivit merkitsemättä niitä.  
4. Avaa valintaikkuna valitsemalla Parametrit.
    * Voit kirjata syyn tarjouksen hyväksynnälle. Syy tallennetaan tarjoukseen.  
5. Anna tai valitse Hyväksynnän syy -kenttään arvo.
6. Valitse OK.
7. Valitse OK.
    * Kun napsautat OK, järjestelmä luo ostotilauksen tarjouspyynnössä hyväksyttyjen rivien perusteella.. Jos tarjouspyynnöllä on muita tarjouksia, joita ei ole käsitelty (hyväksytty, hylätty tai palautettu), järjestelmä kehottaa hylkäämään jäljellä olevat tarjoukset.  

## <a name="view-the-purchase-order-thats-been-generated"></a>Näytä luotu ostotilaus
1. Valitse toimintoruudussa Yleiset.
2. Valitse Ostotilaus.
    * Tässä kentässä näet ostotilauksen, joka luotiin, kun hyväksyit tarjouksen.  
3. Sulje sivu.
4. Sulje sivu.
5. Sulje sivu.
6. Sulje sivu.


