---
title: Kirjanpidon selvitysten automatisointi
description: Tässä artikkelissa on tietoja kirjanpidon selvityksen automatisointiprosessista.
author: abruer
ms.date: 9/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: b43eeeefa581b5d8b40dc2cf0187c7c781b18be3
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708328"
---
# <a name="automate-ledger-settlements"></a>Kirjanpidon selvitysten automatisointi

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Financen versiossa 10.0.31 **Kirjanpidon selvityksen automatisointiprosessi** -ominaisuus on käytettävissä **Ominaisuuksien hallinta** -työtilassa. Voit ottaa käyttöön **Kirjanpidon selvityksen automatisointiprosessi** -ominaisuuden vain, jos **Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä** -ominaisuus on otettu käyttöön.

Kirjanpidon tilitys on prosessi, jossa kirjanpidon debet- ja kredittapahtumat täsmäytetään. Kirjanpidon selvitysaktiviteetteja toistuvasti suorittavat organisaatiot voivat nyt automatisoida prosessin. Kirjanpidon automaattisen selvitysprosessin aikana debet- ja kredittapahtuma voidaan kohdistaa automaattisesti vain, jos niiden summat kirjanpitovaluuttana ovat samat. Esimerkiksi debet-summa 1,00 $ voidaan täsmäyttää automaattisesti kredit-summaan 1,00 $. Debetarvoa 1,00 $ ei kuitenkaan voi automaattisesti täsmäyttää kahteen kreditarvoon, joiden kummankin arvo on 0,50 $. kirjanpitotapahtumien osittaista täsmäytystä ei tueta.

Kirjanpidon selvityksen automaatio määrittää seuraavat tiedot:

- kirjanpidon selvitysten suoritusaika
- automaattisesti selvitettävien debet- ja kredit-summien täsmäyttämisessä käytettävät ehdot
- kirjanpidon täsmäytyksen tietojen käsittelyjärjestys.

## <a name="define-the-occurrence-of-ledger-settlements"></a>Kirjanpidon selvitysten esiintymän määrittäminen

Kirjanpidon selvityksen automaatio käyttää prosessien automaatiokehystä. Eri liiketoimintaprosessit käyttävät tätä kehystä valitun prosessin toistumisen määrittämiseen. Voit käsitellä kirjanpidon selvityksiä siirtymällä kohtaan  **Järjestelmän hallinta \> Asetus \> Prosessien automatisoinnit** tai **Kirjanpito \> Kirjanpidon asetukset \> Prosessien automatisoinnit**.

Valitse ensin **Luo uusi prosessin automatisointi** -vaihtoehto ja valitse sitten **Kirjanpidon selvitykset**. Ohjattu toiminto opastaa automatisoinnin määritysprosessissa.

## <a name="general-page"></a>Yleiset-sivu

Syötä ohjatun toiminnon **Yleiset** -sivulla luotavan kirjanpidon selvityksen esiintymän nimi. Jos esimerkiksi täsmäytettävät debet- ja kreditarvot on täsmäytetty kirjanpidossa maanantaina, anna kuvaavaksi nimeksi esimerkiksi **Kirjanpitoselvitys\_ma**. Syöttämäsi nimi näkyy **Automaatiosääntö**-sarakkeessa **Kirjanpidon selvitykset** -sivulla.

Muut sivun asetukset ovat yleisiä. Ne määrittävät kirjanpidon selvitysten tämän version esiintymämallin. Jos esiintymä on tarkoitettu esimerkiksi maanantaina, voit määrittää sen niin, että se suoritetaan viikoittain, ja voit valita maanantain viikon päiväksi, jolloin se suoritetaan. Voit myös määrittää aikaisen aikataulun ajan, kuten 2.00, jolloin prosessiautomaatio valmistuu ennen seuraavan työpäivän alkua. Prosessin automaatio kannattaa ajoittaa niin, että se suoritetaan normaalin työajan ulkopuolella. Näin voit vähentää vaikutusta kirjanpitohenkilöstöön työpäivän aikana.

Lisätietoja muut **Yleiset** -sivun kentistä on prosessin automaation ohjeissa.

## <a name="ledger-settlements-match-criteria-page"></a>Kirjanpidon selvitysten vastaavuusehdot -sivu

Seuraava ohjatun toiminnon sivu on **Kirjanpidon selvitysten vastaavuusehdot** -sivu. Sen avulla määritetään prosessin automaation esiintymään sisältyvät päätilit sekä debet- ja kreditarvojen määrittämisessä käytettävät ehdot.

### <a name="account-selection"></a>Tilin valinta

Näkyviin tulevat ne päätilit, jotka olet aiemmin määrittänyt yrityksen kirjanpidon selvitystileiksi. (Voit määrittää päätilit kirjanpidon selvitystileiksi kohdassa **Kirjanpito \> Kirjanpidon asetukset \> Kirjanpitoparametrit \> Kirjanpidon selvitykset**.)

### <a name="main-account-and-posting-layer"></a>Päätili ja kirjanpitotaso

Pakollisia täsmäytysehtoja ovat  **päätilin** ja **kirjanpitotason** arvot. Kirjanpidon debet- ja kredittapahtuman **päätilin** ja **kirjanpitotason** arvojen on oltava samat automaattisen kirjanpidon selvitysprosessin aikana täsmäytystä varten.

### <a name="posting-type"></a>Kirjaustyyppi

Valitse **Kirjaustyyppi**-vaihtoehto, jos debet- ja kredittapahtumien täsmäyttäminen kirjanpidon automaattisen selvitysprosessin aikana edellyttää, että niiden kirjaustyyppi on sama.

### <a name="financial-dimensions"></a>Taloushallinnon dimensiot

Valitse **Taloushallinnon dimensiot** -vaihtoehto, jos debet- ja kredittapahtumien täsmäyttäminen kirjanpidon automaattisen selvitysprosessin aikana edellyttää, että niiden taloushallinnon dimensiot ovat samat. Kun tämä vaihtoehto on valittuna, taloushallinnon dimensioiden arvojen ehdot on valittava **Käytettävissä olevat taloushallinnon dimensiot** -luettelossa. **Käytettävissä olevat taloushallinnon dimensiot** -luettelo ei sisällä päätilin dimensiota, koska se vaaditaan automaattisesti täsmäytysehtojen osana.

## <a name="view-the-results-of-a-ledger-settlement-automation"></a>Kirjanpidon selvityksen automatisoinnin tulosten tarkasteleminen

Kun kirjanpidon selvityksen automatisointisarja on luotu, kunkin kirjanpidon selvityksen esiintymät näkyvät prosessin automaation viikkonäkymässä. Lisäksi näytetään kunkin esiintymän tila. Seuraavat tilat ovat käytössä:

- **Ajoitettu** – Automaatio on ajoitettu, mutta sitä ei ole vielä suoritettu.
- **Suoritetaan** – Automaatio on parhaillaan käynnissä.
- **Error** – Automaatio on suoritettu, mutta se päättyi virheeseen. Voit tarkastella virheitä valitsemalla **Näytä tulokset** -painikkeen.
- **Valmis** – Automaation suorittaminen onnistui. Voit tarkastella selvityksen tuloksia **Kirjanpidon selvitykset** -sivulla.

Jos haluat tarkastella täsmäytyksen tuloksia, siirry kohtaan **Kirjanpito \> Kausittaiset tehtävät \> Kirjanpidon selvitykset**. **Automaatiosääntö**-kenttä **Kirjanpidon selvitykset** -sivulla näyttää automatisoidun kirjanpidon selvityksen ajoitetun tehtävän, jota käytettiin tapahtuman selvittämisessä. Epäonnistuneet selvitysyritykset eivät päivitä **Automaatiosääntö**-kohdan arvoa. Jos manuaalisesti peruutat tapahtuman, jonka automaatioprosessi selvitti aiemmin onnistuneesti, **Automaatiosääntö**-kohdan arvo poistetaan.

Täsmäytettyjen tietueiden **Selvityspäivämäärä**-kentässä on päivämäärä, jona automaatioprosessi suoritettiin.

## <a name="editing-a-ledger-settlement-automation"></a>Kirjanpidon selvityksen automaation muokkaaminen

Prosessin automaatiokehyksen avulla voit muokata sarjoja ja esiintymiä, jotka luodaan kirjanpidon selvitykselle. Sarjaa voi muokata **Prosessin automaatio** -sivulla tai prosessin automaation viikkonäkymässä. Jos esimies esimerkiksi päättää suorittaa kirjanpidon selvityksen keskiviikkona maanantain asemesta, tämä voi löytää esiintymän viikkonäkymästä ja valita **Näytä/muokkaa – Sarjat**.

Jos muokkaat sarjaa, sinua pyydetään määrittämään, tuleeko muutos tehdä kaikkiin aiemmin luotuihin esiintymiin vai vain uusiin esiintymiin. Historialliset esiintymiä, joiden tila on jo **Valmis** tai joiden tilaksi on muutettu **Virhe** lopussa, ei muuteta.

Voit myös lisätä uuden esiintymän tai muuttaa aiemmin luotua esiintymää. Esimerkiksi seuraava kirjanpidon selvityksen esiintymä ajoitetaan suoritettavaksi keskiviikkona 1. tammikuuta, mutta päivämäärä on vapaapäivä. Voit muuttaa tapahtumaa **Prosessin automaatio** -sivulla tai prosessin automaation viikoittaisessa näkymässä. Näkyviin tulee sivu, jossa näkyvät aikataulutiedot ja täsmäytysehdot. Tässä voit muokata ajoitettua kellonaikaa ja päivämäärää. Voit myös muokata täsmäytysehtoja, jos muutokset ovat pakollisia. 

Voit myös poistaa esiintymän tai sarjan käytöstä. Jos haluat poistaa esiintymän käytöstä ja keskeyttää sen käsittelyn, valitse se prosessin automaation viikkonäkymässä ja valitse sitten **Poista käytöstä**. Voit poistaa sarjan käytöstä **Prosessin automaatio** -sivulla.

## <a name="security-for-ledger-settlement-automation"></a>Kirjanpidon selvityksen automaation suojaus

**Ylläpidä kirjanpidon selvitysten automaatiosarjojen asetuksia** -tehtävä on lisätty laskentapäällikön ja taloushallintopäällikön rooleihin. **Näytä kirjanpidon selvitysten automaatiosarjojen asetukset** -tehtävä on lisätty kirjanpitäjän, laskentapäällikön ja taloushallintopäällikön rooleihin kirjanpidon selvityksen automaatioita varten. Nämä tehtävät ovat oletussuojausasetuksia, mutta niitä voidaan muuttaa organisaation tarpeiden mukaan.

## <a name="general-ledger-parameters-for-ledger-settlement-automation"></a>Kirjanpidon parametrit kirjanpidon selvityksen automaatiota varten

**Selvityksen tyypillinen saldo** -kenttä osoittaa järjestyksen, jossa automaattinen kirjanpidon selvitys käsitellään. Voit määrittää **Selvityksen tyypillinen saldo** -arvon ja tarkastella sitä siirtymällä kohtaan **Kirjanpito \> Asetus \> Kirjanpitoparametrit** ja valitsemalla **Kirjanpidon selvitykset** -välilehden.

Jos valittuna on **Debet**, automaattinen kirjanpidon selvitysprosessi alkaa debettapahtumista ja hakee vastaavat kredittapahtumat. Jos valittuna on **Kredit**, automaattinen kirjanpidon selvitysprosessi aloittaa kredittapahtumista ja hakee vastaavat debettapahtumat. Tämän vaihtoehdon tulee vastata päätilin tyypillistä saldoa.

## <a name="processing-a-ledger-settlement-automation"></a>Kirjanpidon selvityksen automaation käsitteleminen

Kun automaatiota suoritetaan, järjestelmä valitsee kirjanpitotapahtumat päätileille, jotka on määritetty prosessin automaation sarjoja varten. Se järjestää tapahtumat päivämäärän mukaan käyttämällä päivämääräväliä tilivuoden alusta päivämäärään, jona prosessin automaatio suoritetaan. Se vastaa määritettyjä täsmäytysehtoja. Kirjanpitovaluutan debet- ja kreditsummien absoluuttiset arvot on täsmäytettävä selvitystä varten.

Kun kirjanpidon selvityksen automaation esiintymä käsittelee päätiliä, et voi näyttää **Kirjanpidon selvitykset** -sivua. Odota, kunnes automaatioprosessi on valmis. Prosessin automaatio kannattaa ajoittaa suoritettavaksi työajan ulkopuolella ristiriitojen välttämiseksi.

Automaatioprosessi sisältää kaikki ehtoja vastaavat tapahtumat lukuun ottamatta tapahtumia, jotka on manuaalisesti merkitty selvitettäviksi **Kirjanpidon selvitykset** -sivulla.

## <a name="reversal-of-transactions-that-are-settled-by-the-automation-process"></a>Automaatioprosessin selvittää tapahtumien peruutuksen

Voit peruuttaa automaattisen kirjanpidon selvitysprosessin tekemän selvityksen. Kun automaatioprosessin selvittämä tapahtuma peruutetaan, **Automaatiosääntö**-arvo poistetaan.
