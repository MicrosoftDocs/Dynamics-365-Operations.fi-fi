---
title: Luo ja käsittele asiakkaan ostohyvityksiä
description: Tämä menettely ilmaisee, miten asiakkaan ostohyvityksen käsitellään vaatimuksen muodostamisesta niiden siirtämiseen jaksotuksina myyntireskontraan.
author: omulvad
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsRebateAgreement, SalesTableListPage, SalesCreateOrder, SalesTable, MCRPriceHistory, SalesEditLines,  PdsRebateTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 73bc22949d0b19fa04bf27e6fd7df7b27832795b
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148581"
---
# <a name="generate-and-process-customer-rebates"></a>Luo ja käsittele asiakkaan ostohyvityksiä

[!include [banner](../../includes/banner.md)]

Tämä menettely ilmaisee, miten asiakkaan ostohyvityksen käsitellään vaatimuksen muodostamisesta niiden siirtämiseen jaksotuksina myyntireskontraan. Menettely selittää esimerkkien avulla, miten ostohyvitysrivien erilaiset ehdot vaikuttavat asiakkaalle hyvitettäviin lopullisiin määriin. Sinun on käytettävä USMF-demotietoyritystä ja suoritettava seuraavat tehtävät ennen opastuksen aloittamista: (1) Siirry Myyntireskontran parametrit -sivulle, laajenna ensin Hinnat-välilehti ja sitten Hintatiedot-välilehti ja tarkista lopuksi, että Ota käyttöön hintatiedot -asetukseksi on valittu Kyllä. (2) Siirry Ostohyvityssopimukset-sivulle ja valitse asiakkaan ostohyvityssopimus: USMF-000001. Jos Työnkulun hyväksyntätila -kentän asetukseksi ei ole valittu Hyväksytty, hyväksy se valitsemalla toimintoruudussa Tarkistus.


## <a name="review-a-customer-rebate-agreement"></a>Tarkista asiakkaan ostohyvityssopimus
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Asiakkaan ostohyvitykset > Ostohyvityssopimukset**.
    - Seuraavissa vaiheissa tarkastellaan sopimuksen USMF-000001 ehtoja. Se auttaa ymmärtämään, miten asiakashyvityksen arvot lasketaan menettelyn myöhemmässä vaiheessa.  
    - Tämä yksittäiselle asiakkaalle tarkoitettu sopimus. Tässä esimerkissä kyse on asiakkaasta US-009.  
    - Asiakkaat saavat ostohyvityksiä, kun he ostavat tietyn tuotteen. Tässä tapauksessa tuotteen nimiketunnus on T0020.   
    - Asiakkaan myyntisuoritus, jonka perusteella ostohyvityssummat arvioidaan, kerätään viikoittain.  
    - Hinta saadaan -asetus on Brutto eli rivin myyntisummasta, jonka perusteella vaatimus arvioidaan, ei ole vähennetty alennusta.  
    - Ostohyvitysten laskentatapa näkyy Ostohyvitysrivin vaihtotyyppi -kentässä. Tässä tapauksessa myyntitavoitteeksi, jonka perusteella ostohyvitykset arvioidaan, on valittu Laatu.   
    - Sopimuksen rivit määrittävät ostohyvityssumman tyypin, ostohyvityksen todellisen arvon ja raja-arvot. Tässä esimerkissä asiakas saa 20 dollarin ostohyvityksen jokaisesta myydystä yksiköstä, jos tuotteen viikko-ostoja on 1–50 yksikköä, ja 40 dollarin ostohyvityksen jokaisesta myydystä yksiköstä, jos he ostavat yli 50 yksikköä.  
2. Sulje sivu.

## <a name="generate-rebate-claims"></a>Muodosta ostohyvitysvaatimukset
1. Valitse **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset**.
2. Valitse **Uusi**. Jotta ostohyvitysvaatimusten muodostuksesta saisi käsityksen, seuraavana tehtävänä on luoda myyntitilaus, jossa tuote ja määrä määrittää, saako kyseinen asiakas ostohyvityksen.    
3. Syötä tai valitse arvo **Asiakastili**-kentässä.
4. Valitse **OK**.
5. Syötä tai valitse arvo **Nimiketunnus**-kentässä.
6. Valitse **määräksi** 40.
7. Valitse **Myyntitilausrivit**-osassa **Myyntitilausrivi**.
8. Valitse **Hintatiedot**. Jos tämä asetus ei näy, et valinnut **Ota käyttöön hintatiedot** -asetuksen arvoksi Kyllä ennen opastuksen aloittamista.     
9. Laajenna **Ostohyvitykset**-osa. **Ostohyvitykset**-välilehdessä on luettelo kaikista ostohyvityssopimuksista, joita nykyisellä tilausrivillä voi käyttää. Myös arvioitu ostohyvityssumma on näkyvissä. Huomaa, että näytetyt summat ovat vain esimerkkejä mahdollisista tulevista ostohyvitysvaatimuksista. Todelliset ostohyvityssummat voi vaihdella sen mukaan, mikä on asiakkaan kausittaisen ostohyvityssopimuksen kokonaismyyntimäärä, onko asiakas palauttanut kaikki tai osan määristä ja onko soveltuva myyntitilaus laskutettu.
10. Sulje sivu.
11. Valitse **Lisää rivi**.
12. Syötä tai valitse arvo **Nimiketunnus**-kentässä.
13. Valitse **määräksi** 60.
14. Valitse **Tallenna**.
15. Valitse **toimintoruudussa** **Lasku**.
16. Valitse **Lasku**.
17. Laajenna **Parametrit**-osa.
18. Valitse **Määrä**-kentässä Kaikki.
19. Valitse **OK**.
20. Valitse **OK**.

## <a name="process-rebate-claims"></a>Käsittele ostohyvitysvaatimukset
1. Siirry kohtaan **Siirtymisruutu > Moduulit > Myynti ja markkinointi > Asiakkaan ostohyvitykset > Hyvitykset**.
    - Ostohyvitykset-sivu on työtila, jossa voit tarkastella, hyväksyä ja käsitellä ostohyvitysvaatimuksia. Voit nyt käsitellä vaatimukset, jotka luotiin asiakkaan US-009 myyntitilauksen laskutuksen seurauksena. Tämä asiakas on nyt ostohyvityssopimuksen USMF-000001 aihe.   
    - Ensimmäinen rivi ilmaisee 800 dollarin ostohyvitysvaatimuksen, joka perustuu tuotteen T0020 myytiin. Yksiköitä myytiin 40 ja yksikköhinta oli 20 dollaria. Tämä vastaa ostohyvityssopimuksen ensimmäisen määrärajoituksen ehtoja.  
    - Toinen vaatimus on 2 400 dollarille, ja se perustuu tuotteen T0020 myyntiin, kun myytyjä yksiköitä oli 60 ja yksikkökohtainen hinta 40 dollaria sopimuksen toisen määrärajoituksen mukaisesti.  
    - Kumpikin vaatimus on Lasketaan-tilassa. Tämä tarkoittaa, että ne liittyvät sopimukseen, joka seuraa asiakkaan myyntisuoritusta kausittain, ja että ne on laskettava uudelleen, jotta kyseisen kauden kokonaismyyntimäärä otetaan huomioon.   
2. Valitse **Kumuloi**.
3. Kirjoita **Asiakas**-kenttään arvo tai valitse se.
4. Valitse **Alkamispäivä**-kentässä kuluvan päivän päivämäärä.
5. Valitse **OK**. **Kumuloi**-toiminnon suorittamisen jälkeen arvioitua vaatimussummaa on säädetty ottamaan huomioon, että asiakkaan kokonaismyyntimäärä on kyseisellä kaudella on suurempi kuin ensimmäistä ostohyvistä muodostettaessa. Tämä siis tarkoittaa, että koska kokonaisostomäärä on 100 yksikköä, asiakas on nyt oikeutettu 40 dollarin yksikkökohtaiseen hyvitykseen (sopimuksen toisen määrärajan mukaisesti) tai 400 dollarin kokonaisostohyvitykseen. Ero kirjataan uutena vaatimuksen ylimääräisenä 800 dollarin oikaisuna. Kumulointipäivitykseen sisällytettyjen ostohyvitysvaatimusten tilaksi on nyt määritetty Laskettu. 
6. Merkitse luettelossa kaikki rivit.
7. Valitse **Hyväksy**.
8. Valitse **Prosessi**.
9. Kirjoita **Asiakas**-kenttään arvo tai valitse se.
10. Valitse **OK**. Sanoma osoittaa, että ostohyvityksen käsittely onnistui, ja vaatimusten tilaksi on vaihtunut Merkitse. Tämä tarkoittaa, että ostohyvityksen jaksotuskirjauskansion kirjaamisen jälkeen:
    - Vaatimukset on nyt siirretty asiakkaan väliaikaiseen saldoon vähennyksinä.
    - Ostohyvityksen jaksotuskirjauskansiota on hyvitetty ilmaisemaan tulevaa velkaa asiakkaalle.
    - Ostohyvityksen kulutiliä on veloitettu osoituksena myyntiin liittyvistä kustannuksista.   

