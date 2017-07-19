---
title: "Mukauta käyttäjäkokemusta"
description: "Tässä artikkelissa kerrotaan, kuinka voit mukauttaa Microsoft Dynamics 365 for Finance and Operationsia."
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: b338a930777a5945eb6318dc8066fb3649c79dbe
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="personalize-the-user-experience"></a>Käyttäjäkokemuksen mukauttaminen

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, kuinka voit mukauttaa Microsoft Dynamics 365 for Finance and Operationsia.

Microsoft Dynamics 365 for Finance and Operationsissa on monenlaisia mukauttamismahdollisuuksia. Jotkut mukautukset ovat valintoja, jotka teet asetussivulla vaihtoehtojen luettelossa. Jotkin mukautukset ovat implisiittisiä, esimerkiksi Finance and Operations seuraa ruudukoiden sarakeleveyksiä, jos muutat niitä, sekä pikavälilehtien laajennus- ja tiivistystiloja. Muut mukautukset ovat eksplisiittisiä. Eksplisiittistä mukauttamista varten siirryt vuorovaikutteiseen mukautustilaan ja muutat sivun ulkonäköä hallitsemalla suoraan tapaa, jolla eri elementit näkyvät tai toimivat sivulla. 

Kaikki ja kaiken tyyppiset käyttäjän Finance and Operationsissa tekemät mukautukset koskevat vain kyseistä käyttäjää riippumatta siitä yrityksestä, jonka kanssa käyttäjä on vuorovaikutuksessa. Käyttäjän sivulle tekemät muutokset eivät vaikuta järjestelmän muihin käyttäjiin.

## <a name="systemwide-options-for-the-current-user"></a>Nykyisen käyttäjän järjestelmänlaajuiset vaihtoehdot
Näet Siirtymispalkissa rattaan kuvan, jota kutsutaan **Asetukset**-valikkopainikkeeksi. Tämän **Asetukset**-valikon avaaminen tuo näyttöön eri vaihtoehtoja. Valinta **Asetukset** avaa käyttäjälle **Asetukset**-sivun. Tällä sivulla on neljä vaihtoehtovälilehteä: **Visuaalinen**, **Valinnat**, **Tili**, ja **Työnkulku**.

-   **Visuaalinen:** Käytä tätä valitaksesi väriteeman ja sivusi elementtien oletuskoon.
-   **Valinnat:** Voit valita täällä oletusasetukset, jotka näkyvät aina, kun avaat Finance and Operationsin. Näitä asetuksia ovat yritys, aloitussivu ja oletusnäkymä tai -muokkaustila (joka määrittää, onko sivu lukittu katselua varten vai avautuuko se muokkausta varten aina, kun avaat sen). Löydät myös kieli-, aikavyöhyke-, päivämäärä-, aika- ja numeromuotojen vaihtoehdot. Viimeisenä sivulla on erilaisia sekalaisia valintoja, jotka vaihtelevat versioiden välillä.
-   **Tili:** Anna tässä käyttäjätunnuksesi ja muut tiliin liittyvät vaihtoehdot.
-   **Työnkulku:** Tässä voit valita työnkulkuun liittyviä vaihtoehtoja.

## <a name="implicit-personalizations"></a>Implisiittiset mukautukset
Implisiittiset mukautukset ovat niitä mukautuksia, jotka suoritat yksinkertaisesti olemalla vuorovaikutuksessa tiettyjen tarkistusten kanssa, jotka muistavat nykyisen näkyvän tilansa. 

**Ruudukon sarakkeet:** Voit muokata luettelon sarakkeen leveyttä valitsemalla koon muuttamiseen tarkoitetun palkin sarakkeen otsikon vasemmalla tai oikealla puolella ja vetämällä sitä vasemmalle tai oikealle haluttuun leveyteen. Finance and Operations tallentaa haluamasi leveyden ja näyttää kyseisen sarakkeen tämänlevyisenä aina, kun avaat kyseisen luettelon sisältämän sivun. 

**Pikavälilehdet:** Joillain sivuilla on laajennettavia osioita nimeltä pikavälilehdet. Finance and Operations tallentaa tiedon, mitkä pikavälilehdet olet laajentanut ja mitkä pikavälilehdet olet tiivistänyt. Aina palatessasi sivulle samat pikavälilehdet laajennetaan tai tiivistetään edellisen käyttökertasi perusteella. Tässä artikkelissa kerromme, miten voit muuttaa pikavälilehtien osioiden järjestystä. Joissain tapauksissa pikavälilehden tiivistäminen parantaa suorituskykyä, koska Finance and Operationsin ei tarvitse noutaa tietoja kyseistä pikavälilehteä varten ennen kuin se laajennetaan. 

**Tietoruudut:** Joillain sivuilla on osioita nimeltä Tietoruutu. Tämä ruutu sisältää kyseisen sivun aihepiiriin liittyvää tietoa vain-luku-muodossa. Kutakin Tietoruutu-osion osa kutsutaan Tietoruuduksi. Voit laajentaa tai tiivistää Tietoruudun, ja Finance and Operations tallentaa valintasi. Joissain tapauksissa tietoruudun tiivistäminen parantaa suorituskykyä, koska Finance and Operationsin ei tarvitse noutaa tietoja kyseistä tietoruutua varten ennen kuin se laajennetaan.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Eksplisiittinen mukauttaminen Mukauttaminen-työkalurivin avulla
Jokaisella henkilöllä ja yrityksellä on eri perspektiivi siihen, mitkä tiedot ovat heille tärkeimpiä, tai mitkä tiedot eivät ole tarpeen heidän tavassaan harjoittaa liiketoimintaa. Mahdollisuus muokata tapaa, jolla tiedot järjestetään, miten niiden kanssa ollaan vuorovaikutuksessa tai jopa miten ne piilotetaan, on avain siihen, miten Finance and Operationsista tehdään henkilökohtainen ja tuottava kokemus. 

Eksplisiittinen mukauttaminen on mukauttamista, jonka suoritat nimenomaisena tarkoituksenasi muuttaa elementin tai sivun ulkonäköä valitsemalla mukauttamisvalikko. Perustasollaan eksplisiittistä mukauttamista on, kun napsautat elementtiä hiiren oikealla painikkeella ja valitset **Mukauta**. (Huomaa, että kaikkia sivusi elementtejä ei voida mukauttaa.). Kun valitset tämän mukauttamistavan, näet elementin ominaisuusikkunan. 

[![Elementin ominaisuuksien mukauttaminen](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Voit mukauttaa sivun elementtiä tällä tavoin, jos haluat vain muuttaa elementin otsikkoa, piilottaa elementin niin, että se ei näy sivulla (mitään tietoja ei muuteta, mutta tiedot eivät ole näkyvissä), sisällyttää tiedot pikavälilehden yhteenveto-osioon (jos elementti on pikavälilehdessä), ohittaa kentän sarkaimella siirryttäessä tai määrittää sen niin, ettei tietoja ei voi muuttaa, liittämällä siihen Älä muokkaa -merkinnän. 

Kun haluat siirtää tai piilottaa elementtejä tai tehdä useita muutoksia, voit käyttää Mukautus-työkaluriviä, joka on käytettävissä elementin Ominaisuusikkunasta valitsemalla **Mukauta tämä lomake**. Mukauttaminen-työkalurivi on myös käytettävissä lomakkeen Toimintoruudun kautta **Asetukset**-välilehden Mukauttaminen-ryhmässä. Valitse **Mukauta tämä lomake** ja saat näkyviin Mukauttaminen-työkalurivin. 

[![Mukauttamisen työkalurivi](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Mukauttaminen-työkalurivi sisältää useita mukauttamistoimintoja. Napsauta **Valitse**-työkalua, kun haluat valita ja muuttaa useiden elementtien ominaisuuksia yksi kerrallaan. Napsauta ensin Valitse-työkalua ja valitse sitten elementti, jonka ominaisuuksia haluat muokata. Kun valitset elementin, sen ominaisuusikkuna avautuu ja voit muokata elementin kaikkia ominaisuuksia. Voit toistaa prosessin muille lomakkeesi elementeille, jotka ovat mukautettavissa. Joissain tapauksissa voit valita elementin ja huomaat, että joitain ominaisuuksia ei voida muokata. Tämä tarkoittaa, että elementin nykyisen käyttötavan perusteella Finance and Operations ei anna muuttaa kyseistä ominaisuutta. Et esimerkiksi voi piilottaa kenttää, jota tarvitaan. 

Valitse **Siirrä**-työkalu, kun haluat valita ja siirtää elementin toiseen sijaintiin nykyisen elementtiryhmän sisällä. (Et voi siirtää elementtiä sen pääryhmän ulkopuolelle). Napsauta ensin Siirrä-työkalua ja valitse sitten elementti, jonka haluat siirtää. Kun napsautat siirrettävää elementtiä, Finance and Operations skannaa lomakkeen selvittääkseen, minne tämä elementti voidaan siirtää, ja luo sitten sarjan pudotusvyöhykkeitä, jotka näytetään värillisenä, lihavoituna rivinä sen alueen vieressä, mihin elementti voidaan pudottaa vetäessäsi sitä nykyisen ryhmän sisällä. 

Valitse **Piilota**-työkalu, kun haluat valita ja piilottaa elementin. Piilota elementti valitsemalla Piilota-työkalu ja napsauttamalla sitten elementtiä, jonka haluat piilottaa. Kun valitset Piilota-työkalun, kaikki sillä hetkellä piilotetut elementit tulevat näkyviin varjostettuun säilöön niin, että voit valita elementin, jonka piilotuksen haluat perua. Napsauta Valitse-työkalua katsoaksesi, miltä sivu tulee näyttämään, kun valitut elementit on piilotettu. Valitse **Yhteenveto**-työkalu, kun haluat näyttää numeerisen tai merkkijonokentän pikavälilehden yhteenvetoalueella. Yhteenvetotyökalu koskee vain kenttiä, jotka sisältyvät pikavälilehtiosioon. Kun valitset yhteenvetotyökalun, Finance and Operations näyttää kaikki kentät, jotka on valittu yhteenvetokentiksi sisällyttämällä ne varjostettuun säilöön. Voit lisätä ja poistaa kenttiä interaktiivisesti pikavälilehden yhteenvedosta napsauttamalla kenttää. 

Valitse **Ohita** -työkalu poistaaksesi elementin sivun Näppäimistö-välilehden sarjasta. Kun valitset Ohita-työkalun, kaikki sillä hetkellä ohitetut elementit näytetään varjostetussa säilössä niin, että voit valita ne uudelleen ja tehdä niistä osan välilehden sarjaa valitsemalla ohitetun elementin. 

Valitse **Muokkaa**-työkalu, kun haluat merkitä elementin Muokattavaksi tai Ei-muokattavaksi. Kun valitset Muokkaa-työkalun, kaikki sillä hetkellä ei-muokattavat elementit tulevat näkyviin varjostettuun säilöön niin, että voit muuttaa ne muokattaviksi valitsemalla ne. Huomaa, että joitain kenttiä tarvitaan eikä niiden muokkaamista voida estää. Näiden kenttien vieressä näkyy riippulukkokuvake. 

Valitse **Lisää**-työkalu lisätäksesi kentän sivullesi. Et voi luoda uutta kenttää lisäystyökalulla, mutta voit lisätä kenttiä, jotka ovat osa nykyistä sivun määritystä mutta joita ei näytetä sivulla. Kun valitset lisäystyökalun, sinun on ensin valittava ryhmä tai alue, johon haluaisit lisätä kentän. Valintaikkunassa näytetään luettelo kentistä, jotka liittyvät valitsemaasi osioon. Tässä valintaikkunassa voit valita yhden tai useampia lisättäviä kenttiä, napsauta sitten Lisää. Jos haluat myöhemmin poistaa aiemmin lisäämäsi kentän, toista prosessi mutta tyhjennä valinta kentästä, jonka aiemmin lisäsit. 

Valitse **Hallinta**-painike nähdäksesi luettelon senhetkisen sivun kaikkien mukautusmahdollisuuksien hallintavaihtoehdoista. 

Valitse **Tyhjennä** palauttaaksesi sivun oletusasennustilaan. Kaikki senhetkisen sivun mukautukset tyhjennetään. Tälle ei ole kumoa-toimintoa, joten käytä tätä vaihtoehtoa vain, kun olet varma, että haluat palauttaa sivusi asetukset. 

Valitse **Tuo** käyttääksesi mukautusta mukauttamistiedostosta, jonka sinä tai joku muu on luonut sivulle aikaisemmin. Mukautusten tuominen tyhjentää kaikki koko sivulla suorittamasi mukautukset ja niiden sijaan käytetään valitusta tiedostosta tulevia mukautuksia. Jos haluat tallentaa tai jakaa mukautuksen, valitse **Vie**-vaihtoehto tallentaaksesi mukautukset tiedostoon. 

Valitse **Sulje**-painike sulkeaksesi työkalurivin ja palauttaaksesi sivun sen alkuperäiseen vuorovaikutteiseen tilaan. 

Mukauttaminen-työkaluriviä käytettäessä tallentaminen on implisiittistä. Mukautuksesi tulevat voimaan heti, kun olet tehnyt ne, eikä **Tallenna**-painiketta tarvitse napsauttaa. Joissain tapauksissa näet riippulukon kuvan elementin vieressä, kun valitset työkalun. Tämä tarkoittaa, että sivun oikein toimiminen edellyttää, että valittuun työkaluun liittyviä ominaisuuksia ei muuteta. Kun Mukauttaminen-työkalu avataan, sivusta tulee ei-vuorovaikutteinen. Et voi syöttää tietoja etkä laajentaa tai tiivistää osioita.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Eksplisiittinen mukauttaminen: Ruudun tai luettelon lisääminen työtilaan
Joillain luetteloja sisältävillä sivuilla on käytettävissä mukauttamisen lisätoiminto sen Toimintoruudussa Mukauttaminen-ryhmän Asetukset-välilehdessä. Valitse **Lisää työtilaan** avataksesi avattavan luettelon, jonka avulla voit näyttää työtilassa nykyisen luettelosi tiedot (suodatettuina ja lajiteltuina tai oletusmuotoisina) luettelon tai yhteenvetoruudun muodossa (jota voidaan käyttää näyttämään luettelossa olevien nimikkeiden lukumäärä). 

[![Lisää työtilaan](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Lisää luettelo työtilaan lajittelemalla tai suodattamalla luettelo ensin tiedot sellaisiksi kuin haluat ne nähdä työtilassa ja valitsemalla sitten Lisää työtilaan -valintaikkuna. Valitse seuraavaksi haluamasi työtila ja valitse sitten **Luettelo** Esitys-nimisestä avattavasta luettelosta. Kun valitset vaihtoehdon **Luettelo**, avautuu valintaikkuna, jonka avulla voit valita sarakkeet, jotka haluat nähdä luettelossa sekä luettelon otsikon siten, kuin se tulee näkymään työtilassa. 

Lisää ruutu työtilaan suodattamalla luettelo niin, että se näyttää tiedot, joiden yhteenvedon haluat nähdä (tai joita haluat päästä käyttämään nopeasti). Avaa sitten Lisää työtilaan -valintaikkuna. Valitse seuraavaksi haluamasi työtila ja valitse sitten **Ruutu** Esitys-nimisestä avattavasta luettelosta. Kun napsautat valintaa **Ruutu**, aukeaa valintaikkuna, jonka avulla voit antaa ruudulle otsikon ja päättää, näyttääkö ruutu lukumäärän. Kun ruutu sijoitetaan työtilaan, voit sen avulla avata nykyisen sivun työtilasta ja näyttää kyseiseen ruutuun liittyvien tietojen luettelon. 

Kun luettelosi tai ruutusi on lisätty työtilaan, voit avata kyseisen työtilan ja järjestää luettelon tai ruudun uudelleen sen ryhmän sisällä, johon se on sijoitettu.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Eksplisiittinen mukauttaminen: Yhteenvedon lisääminen työtilasta koontinäyttöön
Joissain työtiloissa on lukumääräruutuja (ruutuja, joissa on numeroita), jotka haluaisit nähdä myös koontinäytössäsi. Napsauta työtilassa lukumääräruutua hiiren oikealla painikkeella ja valitse **Mukauta**. Valitse **Kiinnitä koontinäyttöön**. Kun seuraavan kerran siirryt valittuun koontinäyttöön (ja päivität sen), näet, kyseisen lukumäärän kyseessä olevan työtilan siirtymisruudun alapuolella koontinäytössä.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Eksplisiittinen mukauttaminen: Koontinäyttösi mukauttaminen
Koontinäyttö on usein ensimmäinen sivu, jonka näet, kun avaat Finance and Operationsin. Voit mukauttaa koontinäytön nimeämällä uudelleen työtilasi siirtymisruudut, näyttämällä vain haluamasi ruudut, nimeämällä ruudut uudelleen, tai järjestämällä ruudut haluamaasi järjestykseen. Mukauta koontinäkymä valitsemalla mikä tahansa ruutu ja avaa kontekstivalikko napsauttamalla hiiren oikealla painikkeella. Valitse kontekstivalikossa **Mukauta**. Jos valittu ruutu on se, jonka haluaisit piilottaa, nimetä uudelleen tai ohittaa, voit tehdä muutoksen suoraan esiin tulleessa Ominaisuudet-ikkunassa. Jos haluat järjestää ruudut, valitse **Mukauta tämä lomake** Ominaisuudet-ikkunassa avataksesi Mukauttaminen-työkalurivin. Voit sitten järjestää ruudut Siirrä-työkalun avulla.

## <a name="administration-of-personalization"></a>Mukauttamisen hallinta
Kun olet mukauttanut sivun, voit jakaa mukautuksesi muiden käyttäjien kanssa. Se onnistuu viemällä mukautettuja sivuja. Tämän jälkeen voit pyytää käyttäjiä siirtymään mukautetulle sivulle ja tuomaan luomasi mukautustiedoston.

Jos käyttäjällä on järjestelmänvalvojan oikeudet, hän voi myös hallita muiden käyttäjien mukautuksia **Mukautukset**-sivulla. Tällä sivulla on neljä välilehteä: **Järjestelmä**, **Käyttäjät**, **Tuonti** ja **Tyhjennä**.

- **Järjestelmä** – Voit poistaa tässä välilehdessä kaikki järjestelmän mukautukset tilapäisesti tai kokonaan käytöstä. Mukautuksia ei kuitenkaan poisteta. Sen sijaan kaikki sivut palautetaan oletustilaan. Jos otat mukautukset myöhemmin uudelleen käyttöön, kaikkia mukautuksia käytetään uudelleen kunkin käyttäjän sivulla. Voit myös poistaa kaikkien käyttäjien kaikki mukautukset. Huomioi, että kun poistat kaikki mukautukset, ei ole mitään tapaa ottaa ne uudelleen käyttöön järjestelmän kautta. Varmista sen vuoksi ennen tämän vaiheen suorittamista, että olet vienyt kaikki ne mukautukset, jotka ehkä haluat tuoda myöhemmin.
- **Käyttäjät** – Voit määrittää tässä välilehdessä, voiko kukin käyttäjä tehdä implisiittisen vai eksplisiittisen mukautuksen. Voit myös määrittää, voiko kukin käyttäjä suorittaa implisiittisen vai eksplisiittisen mukautuksen tietyllä sivulla. Voit myös tuoda, viedä tai poistaa mukautuksia kullekin käyttäjälle.
- **Tuonti** – Voit yhden tai usean käyttäjän mukautuksen. Voit käyttää välilehteä, kun olet luonut sivun tai työtilan mukautuksen, ja tuoda sitten mukautuksen mukautustiedostona. Voit tuoda mukautustiedoston ja käyttää sitä yhdelle tai usealle käyttäjälle valitsemalla kaikkien käyttäjien luettelosta yksittäiset käyttäjät. Vaihtoehtoisesti voit suodattaa tietyn rooli ja valita käyttäjät kyseisessä roolissa. Kun olet valinnut mukautusta käyttävät käyttäjät, valitse ensin **Tuo** ja sitten mukautustiedostosi. Mukautuksen oikeellisuus tarkistetaan ja sitä käytetään kaikille käyttäjille, kun he seuraavan kerran avaavat valitun sivun.
- **Tyhjennä** – Voit tyhjentää yhden tai usean käyttäjän sivun tai työtilan mukautukset. Valitse ensin sivu tai työtila, josta mukautukset tyhjennetään. Valitse seuraavaksi yksittäiset käyttäjät kaikkien käyttäjien luettelosta. Vaihtoehtoisesti voit suodattaa tietyn rooli ja valita käyttäjät kyseisestä roolista. Kun olet valinnut sekä sivun tai työtilan ja käyttäjät, valitse **Tyhjennä**. Kaikki mukautukset, joita valitut käyttäjät ovat käyttäneet valitulla sivulla tai valitussa työtilassa, poistetaan. Tätä toimintoa ei voi kumota. Jos sivulla tai työtilassa on kuitenkin tallennettuja mukautuksia, nämä mukautukset voidaan tuoda uudelleen.




