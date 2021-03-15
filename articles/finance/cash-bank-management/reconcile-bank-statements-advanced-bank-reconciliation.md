---
title: Tiliotteiden täsmäytys pankkitilin täsmäytyksen lisätoiminnoilla
description: Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköisiä tiliotteita ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Microsoft Dynamics 365 Financessa. Tässä aiheessa käsitellään täsmäytysprosessia.
author: saraschi2
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationWorksheet
audience: Application User
ms.reviewer: roschlom
ms.custom: 98243
ms.assetid: 9df13adf-aa9d-4f6b-bde6-25a214611692
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92c04a47b134584280736f4d3d2fa401d2a2a9b7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969425"
---
# <a name="reconcile-bank-statements-by-using-advanced-bank-reconciliation"></a>Tiliotteiden täsmäytys pankkitilin täsmäytyksen lisätoiminnoilla

[!include [banner](../includes/banner.md)]

Voit tuoda pankkitilin täsmäytyksen lisätoimintojen avulla sähköiset tiliotteet ja täsmäyttää ne automaattisesti pankkitapahtumien kanssa Dynamics 365 Financeissa. Tässä aiheessa käsitellään täsmäytysprosessia.  

<a name="import-an-electronic-bank-statement"></a>Tuo sähköinen tiliote
-----------------------------------

Voit tuoda tiliotteet **Tiliotteet**-sivun **Tuo tiliote** -toiminnolla. Tiliotteessa pankkitili tunnistetaan tiliotteessa pankkitilin tiedoissa määritetyillä arvoilla. Näitä arvoja ovat pankin nimi, tilinumero, reititysnumero, SWIFT (Society for Worldwide Interbank Financial Telecommunication) -koodi ja kansainvälinen tilinumero (IBAN). 

Voit ladata yhden tilin tai useiden tilien tietoja sisältävän tiliotteen. Jos tilejä on useita, tilit voivat kuulua eri yrityksille.

-   Jos haluat tuoda yhden tilin tiliotetiedoston, valitse ensin **Tuo useiden pankkitilien tiliote kaikista yrityksistä** -asetukseksi **Ei** ja valitse sitten tiliotteeseen liitetty pankkitili. Valitse liitetty tiliotetiedosto valitsemalla **Selaa** ja valitse sitten **Lataa palvelimeen**.
-   Jos haluat tuoda yhden, useita tilejä sisältävän tiliotetiedoston, valitse **Tuo useiden pankkitilien tiliote kaikista yrityksistä** -asetukseksi **Kyllä**. Valitse liitetty tiliotetiedosto valitsemalla **Selaa** ja valitse sitten **Lataa palvelimeen**.

Jos mitään sähköisen tiedoston tiliotetta ei voida liittää pankkitiliin tai jos se on liitetty useisiin pankkitileihin käyttämällä tunnistekenttiä, niitä ei tuoda. Muita tiedoston tiliotteita voidaan silti tuoda. Käyttäjä saa tällöin viestin, jossa ilmoitetaan, että tiliotteiden tuonti ei onnistunut määritetylle pankkitilille. Huomaa, että käyttäjällä, joka tuo tiliotetiedoston, täytyy olla yrityksen käyttöoikeudet, jotta hän voi tuoda tiliotteita yrityksen pankkitileiltä. 

Voit myös ladata useita tiliotetiedostoja Financeen yhdellä kertaa käyttämällä zip-tiedostoa. Jos haluat tuoda useita tilejä sisältäviä useita tiliotetiedostoja, lisää kaikki tiliotetiedostot yhteen zip-tiedostoon. Valitse **Tuo tiliotteet** -valintaikkunassa **Tuo useiden pankkitilien tiliote kaikista yrityksistä** -asetukseksi **Kyllä**. Valitse tiliotetiedostot sisältävä zip-tiedosto valitsemalla **Selaa** ja valitse sitten **Lataa palvelimeen**. Tuontiprosessin tunnistaa zip-tiedoston ja lataa kaikki siihen sisältyvät tiliotteet, riippumatta pankkitilin omistavasta yrityksestä.

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

Luo uusi täsmäytys valitsemalla **Pankkitilin täsmäytys** -sivulla **Uusi** ja valitse sitten tuodun tiliotteen pankkitili. Pankkitilillä voi olla vain yksi avoin pankkitilin täsmäytys. Katkaisupäivämäärä määrittää, mitkä tiliotteen tapahtumat ja Operations-pankkitapahtumat sisältyvät täsmäytyksen laskentataulukkoon. Oletusarvoisesti katkaisupäivämääränä käytetään kuluvaa järjestelmäpäivämäärää, mutta voit muuttaa täsmäytyksen päivämäärän. Muut otsikkotiedot haetaan automaattisesti tiliotteesta. Tämä vaihe suoritetaan automaattisesti, jos **Täsmäytä tuonnin jälkeen** -asetukseksi oli valittu tuonnin aikana **Kyllä**. 

Avaa **Pankkitilin täsmäytyksen laskentataulukko** -sivu valitsemalla **Pankkitilin täsmäytys** -sivulla **Laskentataulukko**. Jos **Täsmäytä tuonnin jälkeen** -asetukseksi oli valittu **Kyllä**, täsmäytyksessä suoritetaan automaattisesti oletusarvoinen täsmäytyksen sääntöjoukko. Jos haluat suorittaa täsmäytyssäännöt manuaalisesti, valitse pankkitapahtumisissa käytettävät täsmäytyksen sääntöjoukot tai täsmäytyssäännöt valitsemalla **Suorita täsmäytyssäännöt**. Jos käsiteltäviä tapahtumia on paljon, voit suorittaa tämän vaiheen eräprosessina. 

**Pankkitilin täsmäytyksen laskentataulukko** -sivulla on neljä ruudukkoja, joissa on tapahtumia. Kahdessa yläruudukossa on näkyvissä tiliotteiden ja Dynamics Operations -tapahtumat, joita ei ole vielä täsmäytetty. Täsmäytetyt tapahtumat näkyvät kahdessa alaruudukossa. **Tiliotteen tapahtumatiedot** -välilehdessä näkyy niiden täsmäyttämättömien tiliotetapahtumien tiedot, jotka valittiin yläruudukosta. 

Tiliotteen tapahtumia voi täsmäyttää kolmella tavalla:

-   Täsmäytä tapahtumat Operations-pankkitapahtumien kanssa.
-   Täsmäytä tapahtumat vastatiliotetapahtumien kanssa.
-   Merkitse tapahtumat **uusiksi**, jolloin ne kirjataan myöhemmin pankkitapahtumiksi Financeen.

Voit täsmäyttää tapahtumat manuaalisesti valitsemalla ensin tapahtumat **Tiliotteen tapahtumat** -ruudukossa, valitsemalla siten tapahtumat **Operations-pankkitapahtumat**-ruudukossa. Valitse lopuksi **Täsmäytä**. Valitut tapahtumat siirretään täsmäyttämättömien tapahtumien yläruudukoista täsmäytettyjen tapahtumien alaruudukoihin. Lisäksi täsmäytetyt ja täsmäyttämättömät kokonaissummat päivitetään. Voit käyttää Voi olla yksi yhteen-, monta yhteen- ja monta moneen -tapahtumatäsmäytyksiä. Täsmäytysten on noudatettava sääntöjä sallituista päivämääräeroista ja tapahtumatyyppien yhdistämismäärityksistä. Nämä säännöt määritetään **Maksuliikennetiedot** -sivulla.

Täsmäytyksessä voi esiintyä pyöristyseroja. Voit täsmäyttää yhden tiliotteen tapahtuman ja yhden Operations-pankkitapahtuman, jolla on pyöristyseroja, jos pyöristyserot ovat pankkitilin **Sallittu pyöristysero** -kentässä määritetyn toleranssisumman rajoissa. Summa näkyy **Oikaisusumma**-kentässä vastaavassa Operations-pankkitapahtumassa. Kun pankkitilin täsmäytys on merkitty täsmäytetyksi, korjaukset kirjataan automaattisesti käyttämällä päätiliä, joka on määritetty liitetyssä pankkitapahtumatyypissä. Korjauksia ei tueta **Tarkistus** ja **Talletus** -asiakirjatyypeissä. 

Tiliotteen vastatapahtumat täsmäytetään käyttämällä täsmäytyksen laskentataulukkoa. Tiliotteen kaksi riviä voidaan täsmäyttää, jos summat ovat vastakkaiset ja jos toinen tapahtumista on merkitty vastatapahtumaksi. Voit myös määrittää täsmäytyssäännön **Tyhjennä palautuslaskelman rivit** -toiminnolle.

Operations-pankin vastatapahtumat on täsmäytettävä **Operations-pankkitapahtumat** -sivulla. Voit täsmäyttää kaksi Operations-pankkitapahtumaa yhdessä, jos asiakirjojen pankkitili, asiakirjatyyppi ja maksuviite on sama ja jos niiden summat ovat vastakkaiset. Voit täsmäyttää myös yhden selvitetyn sekin. Tämä estää kyseisten tapahtumien näkymisen täsmäytyksen laskentataulukossa. 

Jos kyse on uusista pankista peräisin olevista tapahtumista, kuten koroista, maksuista tai kuluista, jotka eivät ole vielä Financessa, voit lisätä ne kirjauskansioon, joka liittyy valittuun tiliotteen täsmäytykseen. Valitse ensin täsmäyttämättömien tapahtumien **Tiliotteen tapahtumat** -ruudukossa tiliotteen tapahtuma ja sitten **Merkitse uudeksi**. Tapahtuman tilaksi on valittu **Uusi** ja tapahtuma on siirretty täsmäytettyjen tapahtumien **Tiliotteen tapahtumat** -ruudukkoon. **Uudeksi** merkityt tapahtumat kirjataan myöhemmin **Tiliote**-sivulla. 

Voit kumota virheellisesti täsmäytettyjen tapahtumien täsmäytykset. Valitse ensin täsmäytetty tiliotteen tapahtuma ja sitten **Kumoa täsmäytys**. Kaikki liitetyt tapahtumat siirretään takaisin täsmäyttämättömien tapahtumien yläruudukoihin. Lisäksi täsmäytetyt ja täsmäyttämättömät kokonaissummat päivitetään. 

Kun täsmäytys on valmis, merkitse pankkitilin täsmäytyksen laskentataulukko täsmäytetyksi.  Prosessi kirjaa korjaussummat automaattisesti **Pankkitapahtuman laji** -sivulla asetettujen tilien mukaisesti.  Pankkitilin täsmäytyksen voi merkitä valmiiksi milloin tahansa, vaikka tiliotteella olisikin rivejä, joita ei ole täsmäytetty.  Täsmäyttämättömät tapahtumat siirretään automaattisesti seuraavaan täsmäytystaulukkoon täsmäytettävinä tiliotteen tapahtumina, joita ei ole täsmäytetty.  Huomaa, että tiliotteen täsmäytyksen merkitsemistä valmiiksi ei voi perua.  Täsmäytystä ei voi tällöin enää muokata, etkä voi tehdä siihen päivityksiä.

## <a name="post-new-transactions-that-are-associated-with-the-reconciliation"></a>Kirjaa uudet täsmäytykseen liitetyt tapahtumat
Täsmäytyksen laskentataulukossa **uusiksi** merkityt tiliotteen tapahtumat kirjataan **Tiliote**-sivulla. Voit tarkastella tiliotteen tietoja valitsemalla **Tiliote**-sivulla tiliotteen tunnuksen. Voit tarkastella uusien tapahtumien ja niihin liitettyjen kirjanpidon merkintöjen tietoja valitsemalla **Kirjanpito**-sivulla **Näytä jakaumat**- ja **Tarkastele kirjanpitoa** -vaihtoehdot. Kirjaa **uusiksi** merkityt tiliotteen rivit kirjanpitoon valitsemalla **Kirjaa**. Huomaa, että tiliote voidaan kirjata vain kerran.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]