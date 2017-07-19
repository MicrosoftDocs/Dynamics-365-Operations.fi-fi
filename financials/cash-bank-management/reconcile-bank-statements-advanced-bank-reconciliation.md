---
title: "Tiliotteiden täsmäytys pankkitilin täsmäytyksen lisätoiminnoilla"
description: "Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköiset tiliotteet ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa. Tässä aiheessa käsitellään täsmäytysprosessia."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 98243
ms.assetid: 9df13adf-aa9d-4f6b-bde6-25a214611692
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: eb7fd01874b08417933ddf575c7d6ff866b4e6f8
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="reconcile-bank-statements-by-using-advanced-bank-reconciliation"></a>Tiliotteiden täsmäytys pankkitilin täsmäytyksen lisätoiminnoilla

[!include[banner](../includes/banner.md)]


Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköiset tiliotteet ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa. Tässä aiheessa käsitellään täsmäytysprosessia.  

<a name="import-an-electronic-bank-statement"></a>Tuo sähköinen tiliote
-----------------------------------

Voit tuoda tiliotteet **Tiliotteet**-sivun **Tuo tiliote** -toiminnolla. Tiliotteessa pankkitili tunnistetaan tiliotteessa pankkitilin tiedoissa määritetyillä arvoilla. Näitä arvoja ovat pankin nimi, tilinumero, reititysnumero, SWIFT (Society for Worldwide Interbank Financial Telecommunication) -koodi ja kansainvälinen tilinumero (IBAN). 

Voit ladata yhden tilin tai useiden tilien tietoja sisältävän tiliotteen. Jos tilejä on useita, tilit voivat kuulua eri yrityksille.

-   Jos haluat tuoda yhden tilin tiliotetiedoston, valitse ensin **Tuo useiden pankkitilien tiliote kaikista yrityksistä** -asetukseksi **Ei** ja valitse sitten tiliotteeseen liitetty pankkitili. Valitse liitetty tiliotetiedosto valitsemalla **Selaa** ja valitse sitten **Lataa palvelimeen**.
-   Jos haluat tuoda yhden, useita tilejä sisältävän tiliotetiedoston, valitse **Tuo useiden pankkitilien tiliote kaikista yrityksistä** -asetukseksi **Kyllä**. Valitse liitetty tiliotetiedosto valitsemalla **Selaa** ja valitse sitten **Lataa palvelimeen**.

Jos mitään sähköisen tiedoston tiliotetta ei voida liittää pankkitiliin käyttämällä tunnistekenttiä, niitä ei tuoda. Muita tiedoston tiliotteita voidaan silti tuoda. Käyttäjä saa tällöin viestin, jossa ilmoitetaan, että tiliotteiden tuonti ei onnistunut määritetylle pankkitilille. Huomaa, että käyttäjällä, joka tuo tiliotetiedoston, täytyy olla yrityksen käyttöoikeudet, jotta hän voi tuoda tiliotteita yrityksen pankkitileiltä. 

Voit myös ladata useita tiliotetiedostoja Finance and Operationsiin yhdellä kertaa käyttämällä zip-tiedostoa. Jos haluat tuoda useita tilejä sisältäviä useita tiliotetiedostoja, lisää kaikki tiliotetiedostot yhteen zip-tiedostoon. Valitse **Tuo tiliotteet** -valintaikkunassa **Tuo useiden pankkitilien tiliote kaikista yrityksistä** -asetukseksi **Kyllä**. Valitse tiliotetiedostot sisältävä zip-tiedosto valitsemalla **Selaa** ja valitse sitten **Lataa palvelimeen**. Tuontiprosessin tunnistaa zip-tiedoston ja lataa kaikki siihen sisältyvät tiliotteet, riippumatta pankkitilin omistavasta yrityksestä. 

Valittavana on **Täsmäytä tuonnin jälkeen** -asetus. Kun tässä asetuksessa on valittu **Kyllä**, järjestelmä tarkistaa automaattisesti tiliotteen, luo uuden pankkitilin täsmäytyksen ja laskentataulukon sekä suorittaa oletusarvoisen täsmäytyksen sääntöjoukon, kun tiliote ladataan palvelimeen. Tämä toiminto automatisoi siihen pisteeseen, jossa tapahtumat on täsmäytettävä manuaalisesti.

## <a name="validate-the-bank-statement"></a>Tarkista tiliotteen oikeellisuus
Tarkista tiliote valitsemalla **Vahvista** **Tiliotteet**-sivulla. Tiliotteet on tarkistettava ennen täsmäytystä. Tämä vaihe suoritetaan automaattisesti, jos **Täsmäytä tuonnin jälkeen** -asetukseksi oli valittu tuonnin aikana **Kyllä**. 

Tiliotteen vahvistuksessa tarkistetaan seuraavat tiedot:

-   Tiliote vastaa valittua pankkitiliä.
-   Tiliotteen valuuttaa vastaa pankkitilin valuuttaa.
-   Tiliotteen alkusaldo on sama kuin pankkitilin edellisen tiliotteen loppusaldo.
-   Päivämäärä ei ole päällekkäinen saman pankkitilin toisen tiliotteen kanssa.
-   Pankkitilin tiliotteiden päivämäärissä ei ole aukkoja.
-   Tiliotteen rivien päivämäärät ovat tiliotteen alku- ja loppupäivämäärän välillä.
-   Alkusaldon ja yhteenlaskettujen rivisummien summa on sama kuin loppusaldo.

Kun vahvistus on valmis, tiliotteen tilaksi päivitetään **Vahvistettu**. Tiliote on tarkistettava ennen täsmäytystä.

## <a name="reconcile-the-bank-statement"></a>Täsmäytä tiliote
Kun olet tuonut sähköisen tiliotteen ja vahvistanut sen **Tiliotteet**-sivulla, voit täsmäyttää tiliotteen **Pankkitilin täsmäytys**- ja **Pankkitilin täsmäytyksen laskentataulukko** -sivuilla. 

Luo uusi täsmäytys valitsemalla **Pankkitilin täsmäytys** -sivulla **Uusi** ja valitse sitten tuodun tiliotteen pankkitili. Pankkitilillä voi olla vain yksi avoin pankkitilin täsmäytys. Katkaisupäivämäärä määrittää, mitkä tiliotteen tapahtumat ja Dynamics 365 for Operations -pankkitapahtumat sisältyvät täsmäytyksen laskentataulukkoon. Oletusarvoisesti katkaisupäivämääränä käytetään kuluvaa järjestelmäpäivämäärää, mutta voit muuttaa täsmäytyksen päivämäärän. Muut otsikkotiedot haetaan automaattisesti tiliotteesta. Tämä vaihe suoritetaan automaattisesti, jos **Täsmäytä tuonnin jälkeen** -asetukseksi oli valittu tuonnin aikana **Kyllä**. 

Avaa **Pankkitilin täsmäytyksen laskentataulukko** -sivu valitsemalla **Pankkitilin täsmäytys** -sivulla **Laskentataulukko**. Jos **Täsmäytä tuonnin jälkeen** -asetukseksi oli valittu **Kyllä**, täsmäytyksessä suoritetaan automaattisesti oletusarvoinen täsmäytyksen sääntöjoukko. Jos haluat suorittaa täsmäytyssäännöt manuaalisesti, valitse pankkitapahtumisissa käytettävät täsmäytyksen sääntöjoukot tai täsmäytyssäännöt valitsemalla **Suorita täsmäytyssäännöt**. Jos käsiteltäviä tapahtumia on paljon, voit suorittaa tämän vaiheen eräprosessina. 

**Pankkitilin täsmäytyksen laskentataulukko** -sivulla on neljä ruudukkoja, joissa on tapahtumia. Kahdessa yläruudukossa on näkyvissä tiliotteiden ja Dynamics Operations -tapahtumat, joita ei ole vielä täsmäytetty. Täsmäytetyt tapahtumat näkyvät kahdessa alaruudukossa. **Tiliotteen tapahtumatiedot** -välilehdessä näkyy niiden täsmäyttämättömien tiliotetapahtumien tiedot, jotka valittiin yläruudukosta. 

Tiliotteen tapahtumia voi täsmäyttää kolmella tavalla:

-   Täsmäytä tapahtumat Dynamics 365 for Operations -pankkitapahtumien kanssa.
-   Täsmäytä tapahtumat vastatiliotetapahtumien kanssa.
-   Merkitse tapahtumat **uusiksi**, jolloin ne kirjataan myöhemmin pankkitapahtumiksi Finance and Operationsissa.

Voit täsmäyttää tapahtumat manuaalisesti valitsemalla ensin tapahtumat **Tiliotteen tapahtumat** -ruudukossa, valitsemalla siten tapahtumat **Operations-pankkitapahtumat**-ruudukossa. Valitse lopuksi **Täsmäytä**. Valitut tapahtumat siirretään täsmäyttämättömien tapahtumien yläruudukoista täsmäytettyjen tapahtumien alaruudukoihin. Lisäksi täsmäytetyt ja täsmäyttämättömät kokonaissummat päivitetään. Voit käyttää Voi olla yksi yhteen-, monta yhteen- ja monta moneen -tapahtumatäsmäytyksiä. Täsmäytysten on noudatettava sääntöjä sallituista päivämääräeroista ja tapahtumatyyppien yhdistämismäärityksistä. Nämä säännöt määritetään **Maksuliikennetiedot** -sivulla.

Täsmäytyksessä voi esiintyä pyöristyseroja. Voit täsmäyttää yhden tiliotteen tapahtuman ja yhden Dynamics 365 for Operations -pankkitapahtuman, jolla on pyöristyseroja, jos pyöristyserot ovat pankkitilin **Sallittu pyöristysero** -kentässä määritetyn toleranssisumman rajoissa. Summa näkyy **Oikaisusumma**-kentässä vastaavassa Dynamics 365 for Operations -pankkitapahtumassa. Kun pankkitilin täsmäytys on merkitty täsmäytetyksi, korjaukset kirjataan automaattisesti käyttämällä päätiliä, joka on määritetty liitetyssä pankkitapahtumatyypissä. Korjauksia ei tueta **Tarkistus** ja **Talletus** -asiakirjatyypeissä. 

Tiliotteen vastatapahtumat täsmäytetään käyttämällä täsmäytyksen laskentataulukkoa. Tiliotteen kaksi riviä voidaan täsmäyttää, jos summat ovat vastakkaiset ja jos toinen tapahtumista on merkitty vastatapahtumaksi. Voit myös määrittää täsmäytyssäännön **Tyhjennä palautuslaskelman rivit** -toiminnolle.

Dynamics 365 for Operations -järjestelmässä pankin vastatapahtumat on täsmäytettävä **Dynamics 365 for Operations -pankkitapahtumat** -sivulla. Voit täsmäyttää kaksi Dynamics 365 for Operations -pankkitapahtumaa yhdessä, jos asiakirjojen pankkitili, asiakirjatyyppi ja maksuviite on sama ja jos niiden summat ovat vastakkaiset. Voit täsmäyttää myös yhden selvitetyn sekin. Tämä estää kyseisten tapahtumien näkymisen täsmäytyksen laskentataulukossa. 

Jos kyse on uusista pankista peräisin olevista tapahtumista, kuten korosta, maksuista tai kuluista, jotka eivät ole vielä Finance and Operationsissa, voit lisätä ne kirjauskansioon, joka liittyy valittuun tiliotteen täsmäytykseen. Valitse ensin täsmäyttämättömien tapahtumien **Tiliotteen tapahtumat** -ruudukossa tiliotteen tapahtuma ja sitten **Merkitse uudeksi**. Tapahtuman tilaksi on valittu **Uusi** ja tapahtuma on siirretty täsmäytettyjen tapahtumien **Tiliotteen tapahtumat** -ruudukkoon. **Uudeksi** merkityt tapahtumat kirjataan myöhemmin **Tiliote**-sivulla. 

Voit kumota virheellisesti täsmäytettyjen tapahtumien täsmäytykset. Valitse ensin täsmäytetty tiliotteen tapahtuma ja sitten **Kumoa täsmäytys**. Kaikki liitetyt tapahtumat siirretään takaisin täsmäyttämättömien tapahtumien yläruudukoihin. Lisäksi täsmäytetyt ja täsmäyttämättömät kokonaissummat päivitetään. 

Kun kaikki tiliotteen rivit on käsitelty, merkitse pankkitilin täsmäytyksen laskentataulukko täsmäytetyksi.

## <a name="post-new-transactions-that-are-associated-with-the-reconciliation"></a>Kirjaa uudet täsmäytykseen liitetyt tapahtumat
Täsmäytyksen laskentataulukossa **uusiksi** merkityt tiliotteen tapahtumat kirjataan **Tiliote**-sivulla. Voit tarkastella tiliotteen tietoja valitsemalla **Tiliote**-sivulla tiliotteen tunnuksen. Voit tarkastella uusien tapahtumien ja niihin liitettyjen kirjanpidon merkintöjen tietoja valitsemalla **Kirjanpito**-sivulla **Näytä jakaumat**- ja **Tarkastele kirjanpitoa** -vaihtoehdot. Kirjaa **uusiksi** merkityt tiliotteen rivit kirjanpitoon valitsemalla **Kirjaa**. Huomaa, että tiliote voidaan kirjata vain kerran.




