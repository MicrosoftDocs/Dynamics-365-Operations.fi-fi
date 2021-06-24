---
title: Useiden noutotoimitustapojen ottaminen käyttöön asiakastilauksille
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commercen toiminnoista, joiden avulla voit luoda asiakastilauksia noudettavaksi myymälästä.
author: hhainesms
ms.date: 06/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ae7df6679c261b5e5dcd39e4ca6fe0e21d993927
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216764"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>Useiden noutotoimitustapojen ottaminen käyttöön asiakastilauksille

[!include [banner](includes/banner.md)]


Microsoft Dynamics 365 Commerce -versiossa 10.0.16 ja uudemmissa versioissa organisaatiot voivat määrittää useita toimitustapoja, joita ostajat tai myyjät voivat valita, kun he luovat tilauksen, joka noudetaan myymälästä. Tällä tavoin organisaatiot voivat tarjota ostajille useita noutovaihtoehtoja. Esimerkiksi monet jälleenmyyjät tarjoavat nyt ostajille mahdollisuuden valita tilauksen noudon myymälästä tai tien varresta. Commerce tukee näiden eri noutotoimitustapojen konfigurointia. Käyttäjät voivat hyödyntää niitä, kun he luovat asiakastilauksia missä tahansa tuetussa Commerce-kanavassa (sähköinen kaupankäynti, puhelinkeskus tai myymälä).

## <a name="enable-and-configure-pickup-delivery-modes"></a>Noutotoimitustapojen käyttöönotto ja määritys

Jos haluat käyttää tätä toimintoa, ota **Useiden noutotoimitustapojen tuki** -ominaisuus käyttöön **Ominaisuuksien hallinta** -työtilassa Commerce Headquarters -sovelluksessa. Kun otat toiminnon käyttöön, lisämääritykset ovat pakollisia.

Commerce-versiossa 10.0.15 ja aiemmissa versioissa organisaatiot voivat määrittää vain yhden toimitustavan nimetyksi noutotoimitustavaksi. Tämä määritelmä tehdään **Commerce-parametrit** -sivulla. Kun otat versiossa 10.0.16 tai uudemmasa versiossa käyttöön **Useiden noutotoimitustapojen tuki** -ominaisuuden, toimitustapa, joka oli määritetty aiemmin noutotoimitustavaksi **Commerce-parametrit** -sivulla, kopioidaan automaattisesti noutotoimitustapojen uuteen kokoonpanoon.

![Noutotoimitustavat Commerce-parametrit -sivulla](media/multiplepickupparameter.png)

Kun olet määrittänyt **Useiden noutotoimitustapojen tuki** -ominaisuuden käyttöön, voit määrittää useita noutotoimitustapoja **Noutotoimitustapa**-ruudukon **Toimitustapa**-pikavälilehdessä **Asiakastilaukset**-välilehdessä **Commerce-parametrit** -sivulla.

**Noutotoimitustapa**- ja **Sähköinen toimitustapa**- kentät sekä **Näytä lähetystilauksissa vain rahdinkuljettajien toimitustavat** asetus on siirretty tähän pikavälilehteen.

Ennen kuin määrität muita noutotoimitustapoja, sinun on määritettävä toimitustavat. Lisää Commerce Headquarters -sovelluksen **Toimitustavat**-sivulla toimitustavat, joita voidaan pitää noutotoimitustapoina. Varmista, että kaikki määritykset on tehty. Jos esimerkiksi tarjoat verkko-ostajille noutoa tien vierestä tietyille kaupoille sinun on luotava uusi toimitustapa tätä varten. Voit luoda tämän toimitustavan käyttäen kuvauksena "nouto tien vierestä". Tämän jälkeen haluat varmistaa, että "Nouto tien vierestä" -toimitustapa on yhdistetty kaikkiin Commerce-kanaviin, joka voi tarjota sitä, mukaan lukien verkkokaupoissa, jotka voivat tarjota tätä vaihtoehtoa, sekä yksittäisen myymälän kanaville, jotka tarjoavat tämän tilauksen täyttämistavan. Toimitustavat on myös linkitettävä tuotteisiin. Jos tässä esimerkissä on tiettyjä tuotteita, joita ei voida täyttää käyttäen "noutoa tien vierestä", on varmistettava, että nämä nimikkeet jätetään pois. Kun olet lisännyt tarvittavat uudet toimitustavat, suorita **Käsittele toimitustavat** -työ luodaksesi toimitustapojen, kanavien ja nimikkeiden väliset suhteet. Kun työ on valmis, avaa **Jakeluaikataulu** -sivu Commerce Headquarters -sovelluksessa ja suorita **1120**- jakelutehtävä varmistaaksesi, että asianmukaiset Commerce-kanavan tietokannat päivitetään uuden toimitustavan määrityksillä.

![Esimerkki toimitustavan määrityksestä tien vierestä noudolle](media/pickupmodes.png)

Kun olet määrittänyt lisänoutotoimitustavat, lisää ne **Commerce-parametrit** -sivun **Noutotoimitustavat**-ruudukkoon. Päivitä sitten asiaankuuluvat Commerce-kanavan tietokannat konfiguraation muutoksella suorittamalla asianmukaiset jakelutyöt.

> [!NOTE]
> Sen lisäksi, että käytössä on nykyinen noutotoimitustapa, joka kopioidaan **Noutotoimitustapa**-ruudukkoon, kun otat käyttöön **Useiden noutotoimitustapojen tuki** -ominaisuuden, sinun on konfiguroitava jokaiselle luomallesi noutotoimitustavalle uudet toimitustavat. Kun lisäät toimitustapoja **Noutotoimitustapa**-ruudukkoon, Commerce tarkistaa, käyttävätkö aktiiviset avoimet myyntirivit jo niitä. Jos avoimia myyntirivejä löytyy, näyttöön tulee virhesanoma. Toimitustapoja ei pidetä noutotoimitustapoina, ennen kuin kaikki niitä käyttävät avoimet myyntirivit on suljettu (joko laskutettu tai peruutettu).

> [!IMPORTANT]
> Kun olet määrittänyt useamman kuin yhden noutotoimitustavan **Commerce-parametrit** -sivulla, **Useiden noutotoimitustapojen tuki** -ominaisuus muuttuu pakolliseksi eikä sitä voi enää poistaa käytöstä. Jos toiminto on poistettava käytöstä, poista kaikki paitsi yksi noutotoimitustapa **Noutotoimitustapa**-ruudukosta. Kun vain yksi noutotoimitustapa määritetään, toimintoa ei enää pidetä pakollisena, ja se voidaan poistaa käytöstä.

### <a name="e-commerce-site-configurations"></a>Sähköisen kaupankäynnin sivuston määritykset

Kun **Useiden noutotoimitustapojen tuki** on käytössä, seuraavat verkkokauppasivujen moduulit näyttävät uudet noutotoimitustavat määritysten mukaisesti:

- Ostoruutu
- Myymälän valitsin
- Ostoskori
- Noutotiedot
- Tilauksen vahvistus
- Tilauksen tiedot

Verkkokauppasivuilla ei tarvita lisätoimia, jotta noutotoimitustavat olisivat käytettävissä.

## <a name="work-with-multiple-pickup-delivery-modes"></a>Useiden noutotoimitustapojen käyttö

Kun kanavalle on käytettävissä useita noutotoimitustapoja, asiakkaille tarjotaan parannettua kokemusta, kun he ostavat tuotteita, jotka noudetaan. 

- Sähköisen kaupankäynnin kanavissa ostajat voivat valita minkä tahansa voimassa olevan noutotoimitustavan, joka on käytettävissä. Esimerkiksi vähittäiskauppias määrittää kaksi noutotoimitustapaa (myymälästä nouto ja tien vierestä nouto), jotka molemmat on määritetty **Noutotoimitustapa**-ruudukossa ja molemmat ovat voimassa tilauksen toteutuskanavalle ja ostetuille tuotteille. Tässä tapauksessa ostaja voi valita haluamansa noutotoimitustavan. Valitusta noutotoimitustavasta tulee toimitustapa, joka on linkitetty myyntitilausriviin, kun tilaus luodaan Commerce Headquarters -sovelluksessa.

    ![Noutovaihtoehdon valitseminen sähköisessä kaupankäynnissä](media/pickupecommerce.png)

- Jos myymäläkanavassa luodaan asiakastilaus noudettavaksi myyntipistesovelluksessa, myyjän on valittava käytettävissä olevista noutotoimitustavoista, jos niitä on konfiguroitu. Jos kanavalla ja nimikkeellä on käytettävissä vain yksi kelvollinen noutotoimitustapa, myyjää ei kehoteta valitsemaan sitä. Sen sijaan käytettävissä oleva noutotoimitustapa otetaan automaattisesti käyttöön tilausriveille.

    ![Noutovaihtoehdon valitseminen myyntipistesovelluksessa](media/pickuppos.png)

- Kun käyttäjät luovat noutotilauksia puhelinkeskuskanavissa, he voivat valita manuaalisesti minkä tahansa määritetyn noutotoimitustavan, joka on linkitetty puhelinkeskuskanavaan. Järjestelmä vahvistaa sitten, että valittua noutotoimitustapaa voidaan käyttää, kun siihen linkitetty nimike tilataan. Kun noutotoimitustapa on valittuna puhelinkeskuskanavissa, myyntitilausrivit on linkitettävä kelvolliseen myymälävarastoon. Jos muu kuin myymälävarasto on määritetty puhelinkeskuksen myyntirivillä, kyseiselle myyntiriville ei voi määrittää noutotoimitustapaa.
- Myyjät voivat käyttää **Tilauksen peruutus**- tai **Tilauksen täyttäminen** -toimintoa myyntipistesovelluksessa noutakseen tilausten tai tilausrivien luettelon noutoa varten. Jos myyjä käyttää ennalta määritettyä hakusuodatinta näyttämään kaikki tilaukset, jotka noudetaan nykyisestä myymälästä, kyselyt muokataan sen varmistamiseksi, että hakutuloksissa näkyvät kaikki noutotoimitustapaa käyttävät soveltuvat tilaukset. Myyntipisteen käyttäjät voivat myös käyttää aiemmin luotuja suodattimia tilausten luettelon rajaamiseksi tiettyyn noutotoimitustapaan. Ne voivat esimerkiksi näyttää vain tien vierestä noudettavat tilaukset.

    ![Palautustilausten luetteloon sovellettujen noutotapojen suodattaminen](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>Jaetun tilausten hallinnan huomioon otettavia seikkoja

Commercen [jaetun tilausten hallinnan (DOM)](./dom.md) toiminnot ohittavat kaikki myymälästä noutoa varten merkityt myyntirivit. Nämä ominaisuudet on päivitetty siten, että konfiguroituihin noutotoimitustapoihin linkitetyt myyntirivit ohittavat DOM-logiikan eikä niitä kohdisteta uuteen toteutusvarastoon.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
