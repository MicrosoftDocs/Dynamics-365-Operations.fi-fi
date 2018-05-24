---
title: "Palautuksen kustannushinta ja erätunnus"
description: "Saatat haluta, että palautettujen tuotteiden kustannus vastaa tuotteiden kustannusta sinä hetkenä, kun myit tuotteet asiakkaalle. Voit tehdä tämän käyttämällä **Palauta erätunnus** -kenttää."
author: YuyuScheller
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: aeba56128ab6c9ab7d244bdf153faba8e96069d6
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="return-cost-price-and-return-lot-id"></a>Palautuksen kustannushinta ja erätunnus        

[!include [banner](../includes/banner.md)]



Varastoon palautettavien tuotteiden kustannus lasketaan käyttämällä tuotteiden nykyistä kustannusta. Saatat kuitenkin haluta, että palautettujen tuotteiden kustannus vastaa tuotteiden kustannusta sinä hetkenä, kun myit tuotteet asiakkaalle. Voit tehdä tämän käyttämällä **Palauta erätunnus** -kenttää, joka on **Rivin tiedot** -pikavälilehdellä **Myyntitilaus** -lomakkeessa.

Tässä on yksi esimerkkitilanne. Teet asiakkaalle laskun. Asiakas palauttaa toimitetut tuotteet sinulle. Palautat tuotteen varastoon. Tässä tapauksessa kyseisten tuotteiden kustannus lasketaan käyttämällä tuotteiden nykyistä kustannusta, kun hyvität palautetut tuotteet asiakkaalle. Jos käytät **Palauta erätunnus** -kenttää, palautettujen tuotteiden kustannus lasketaan asiakkaan alkuperäisessä laskussa olevan kustannuksen mukaan.

Jos haluat käyttää muuta kuin nykyistä kustannusta asiakkaan palautuksille, käytä jotakin seuraavista tavoista.

## <a name="method-1-manually-enter-the-return-cost-price"></a>Menetelmä 1: Syötä palautuksen kustannushinta käsin

Oletusarvon mukaan lisätessäsi nimikkeitä palautustilaukseen nimikkeet palautetaan varastoon nykyisellä kustannushinnalla. Voit määrittää muun palautuksen kustannushinnan seuraavasti.

1.  Valitse **Myynti ja markkinointi** \> **Yleinen** \> **Palautustilaukset** \> **Kaikki palautustilaukset**.

2.  Valitse **toimintoruudussa** **Uusi** -ryhmästä **Palautustilaus**.

3.  Valitse **Luo palautustilaus** -lomakkeessa asiakastili ja valitse sitten **OK**.

4.  Valitse **Palautustilaus - palautusnumero: %1, %2** -lomakkeessa nimike, ja kirjoita negatiivinen määrä **Määrä**-kenttään.

5.  Valitse **Rivin erittely** -pikavälilehti.

6.  Syötä **Yleinen**-välilehdessä arvo **Palautuksen kustannushinta** -kenttään. Tätä arvoa käytetään, kun tavaroita palautetaan varastoon. Jos et syötä arvoa, nykyistä kustannushintaa käytetään, kun tavaroita palautetaan varastoon.

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a>Menetelmä 2: Luo kustannushinta automaattisesti myyntilaskun rivin perusteella

Tämä on ensisijainen menetelmä palautusrivien luomiseen. Käyttääksesi tuotteiden kustannusta, joka oli voimassa kun tuotteet myytiin asiakkaalle, luo palautustilaus ja määritä myyntirivi palautukseen.

1.  Valitse **Myynti ja markkinointi** \> **Yleinen** \> **Palautustilaukset** \> **Kaikki palautustilaukset**.

2.  Valitse **toimintoruudussa** **Uusi** -ryhmästä **Palautustilaus**.

3.  Valitse **Luo palautustilaus** -lomakkeessa asiakastili ja valitse sitten **OK**.

4.  Napsauta **Palautustilaus - palautusnumero: %1, %2** -lomakkeen **toimintoruudussa** kohtaa **Etsi myyntitilaus**.

5.  Valitse **Etsi myyntitilaus** -lomakkeessa palautettava laskurivi ja napsauta sitten **OK**.
    
    **Rivin erittely** -pikavälilehden **Yleinen**-välilehdessä oleva **Palauta erätunnus** -kenttä näyttää alkuperäisen myyntirivin arvon. Lisäksi **Palautuksen kustannushinta** -kentässä näkyy alkuperäisen myyntirivin kustannusarvo.

## <a name="cost-calculation-example"></a>Kustannuksen esimerkkilaskelma

Kun käytät **Palauta erätunnus** -kenttää palautustilausrivillä palautuksen kustannushinnan määrittämiseksi, palautustilausrivin kustannusta käytetään. Jos suoritat varaston sulkemis- tai uudelleenlaskentatoiminnon, kustannus oikaistaan alkuperäisellä myyntirivillä. Palautustilausrivin kustannus oikaistaan automaattisesti samaan kappalekohtaiseen kustannukseen.

1.  Luo ja vapauta tuote, jonka nimi on Testi. Määritä **Vapautetun tuotteen tiedot** -lomakkeessa seuraavat tiedot:
    
    1.  Valitse **Kustannusten hallinta** -pikavälilehden **Nimikeryhmä**-kentässä **Osat**-ryhmä.
    
    2.  Valitse **Yleinen**-pikavälilehden **Nimikemalliryhmä**-kentässä **DEF**.
    
    3.  Kirjoita **Osto**-pikavälilehden **Hinta**-kenttään 10.00 nimikkeen hintayksiköksi.
    
    4.  Valitse **toimintoruudussa** **Dimensioryhmät**. Valitse **Varastodimensioryhmä**-kentässä **Vain toimipaikka ja varasto**. Valitse **Seurantadimensioryhmä**-kentässä **Ei aktiivisia seurantadimensioita**.

2.  Luo ostotilaus 10 kappaleelle Testi-nimikettä kappalehinnalla 6,00, ja kirjaa sitten lasku ostotilaukselle.
    
    Luo toinen ostotilaus 10 kappaleelle Testi-nimikettä kappalehinnalla 8,00, ja kirjaa sitten lasku ostotilaukselle.

3.  Kirjaa laskun myyntitilaukselle myydäksesi viisi kappaletta Testi-nimikettä.
    
    Tässä tapauksessa myyntitilausrivin kustannus on 35,00 (5 kappaletta \*keskimääräinen kustannus per kappale 7,00).

4.  Luo palautustilaus asiakkaalle. Valitse **Etsi myyntitilaus** -lomakkeessa laskurivi ja napsauta sitten **OK**.

5.  Tarkista **Palautustilaus - palautusnumero: %1, %2** -lomakkeessa, että palautustilaus luodaan Testi-nimikkeen palautusta varten. Palautustilauksen määräksi määritetään -5,00.
    
    **Palauta erätunnus** -kentässä näkyy erätunnus. Tämä erätunnus haetaan asiakkaalle alkunperin myydyn nimikkeen myyntitilauksesta. **Palautuksen kustannushinta** -kentässä näkyy alkuperäisen myyntirivin kustannushinta.

6.  Rekisteröi palautettujen nimikkeiden vastaanotto.

7.  Kirjaa pakkausluettelo palautetuille nimikkeille.

8.  Kirjaa palautustilauksen lasku. Valitse **Kaikki myyntitilaukset** -luettelosivulla myyntitilaus, jonka tilaustyyppi on **Palautustilaus**.

9.  Avaa **Varastotapahtumat**-lomake. Varmista, että palautuksen kappalekohtainen kustannus on 7,00 käyttämällä **Palautuksen kustannushinta** -arvoa, jolloin **Kustannussumma**-kentän summa on 35,00. Voit avata **Varastotapahtumat**-lomakkeen **Palautustilaus - palautusnumero: %1, %2** -lomakkeesta. Valitse **Rivit**-ruudukossa **Varasto** \> **Tapahtumat**.

10. Käyt Varastonhallinta-moduulin **Päätös ja oikaisu** -lomaketta **Sulje**-menettelyn suorittamiseksi.
    
    Tämä toiminto oikaisee alkuperäisen myyntirivin kustannuksen -35,00 (5 kappaletta \* 7,00) muotoon -30,00 (5 kappaletta \* 6,00). Tämä johtuu siitä, varastomalliryhmä käyttää First in, First out (FIFO) -mallia ja kappalehinta 6,00 on FIFO-kustannus ensimmäisestä ostotilauksesta. Lisäksi toiminto oikaisee palautuksen myyntirivin kustannuksen vastaamaan alkuperäisen myyntitilausrivin kappalehintaa. Palautusrivin kustannus oikaistaan siten 35,00 > 30,00.





