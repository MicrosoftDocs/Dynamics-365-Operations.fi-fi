---
title: "Mukauta käyttäjäkokemusta"
description: "Tässä artikkelissa kerrotaan, kuinka voit mukauttaa Microsoft Dynamics 365 for Operationsia."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 8965c193839002776b3c61036b23b54625c974a4
ms.lasthandoff: 03/31/2017


---

# <a name="personalize-the-user-experience"></a>Mukauta käyttäjäkokemusta

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, kuinka voit mukauttaa Microsoft Dynamics 365 for Operationsia.

Microsoft Dynamics 365 for Operationsissa on monenlaisia mukauttamismahdollisuuksia. Jotkut mukautukset ovat valintoja, jotka teet asetussivulla vaihtoehtojen luettelossa. Jotkut mukautukset ovat implisiittisiä, esimerkiksi Dynamics 365 for Operations seuraa ruudukoiden sarakeleveyksiä, jos muutat niitä, sekä pikavälilehtien laajennus- ja tiivistystiloja. Muut mukautukset ovat eksplisiittisiä. Eksplisiittistä mukauttamista varten siirryt vuorovaikutteiseen mukautustilaan ja muutat sivun ulkonäköä hallitsemalla suoraan tapaa, jolla eri elementit näkyvät tai toimivat sivulla. 

Kaikki ja kaiken tyyppiset käyttäjän Dynamics 365 for Operationsissa tekemät mukautukset koskevat vain kyseistä käyttäjää siitä yrityksestä riippumatta, jonka kanssa käyttäjä on vuorovaikutuksessa. Käyttäjän sivulle tekemät muutokset eivät vaikuta järjestelmän muihin käyttäjiin.

## <a name="systemwide-options-for-the-current-user"></a>Nykyisen käyttäjän järjestelmänlaajuiset vaihtoehdot
Näet Siirtymispalkissa rattaan kuvan, jota kutsutaan **Asetukset**-valikkopainikkeeksi. Tämän **Asetukset**-valikon avaaminen tuo näyttöön eri vaihtoehtoja. Valinta **Asetukset** avaa käyttäjälle **Asetukset**-sivun. Tällä sivulla on neljä vaihtoehtovälilehteä: **Visuaalinen**, **Valinnat**, **Tili**, ja **Työnkulku**.

-   **Visuaalinen: **Käytä tätä valitaksesi väriteeman ja sivusi elementtien oletuskoon.
-   **Valinnat: **Tässä voit valita oletusasetukset, jotka näkyvät aina, kun avaat Dynamics 365 for Operationsin. Tähän sisältyvät yritys, aloitussivu ja oletusnäkymä/-muokkaustila (joka määrittää, onko sivu lukittu katselua varten vai avautuuko se muokkausta varten aina kun avaat sen). Löydät myös kieli-, aikavyöhyke-, päivämäärä-, aika- ja numeromuotojen vaihtoehdot. Viimeisenä sivulla on erilaisia sekalaisia valintoja, jotka vaihtelevat versioiden välillä.
-   **Tili: **Anna tässä käyttäjätunnuksesi ja muut tiliin liittyvät vaihtoehdot.
-   **Työnkulku: **Tässä voit valita työnkulkuun liittyviä vaihtoehtoja.

## <a name="implicit-personalizations"></a>Implisiittiset mukautukset
Implisiittiset mukautukset ovat niitä mukautuksia, jotka suoritat yksinkertaisesti olemalla vuorovaikutuksessa tiettyjen tarkistusten kanssa, jotka muistavat nykyisen näkyvän tilansa. 

**Ruudukon sarakkeet:** Voit muokata luettelon sarakkeen leveyttä valitsemalla koon muuttamiseen tarkoitetun palkin sarakkeen otsikon vasemmalla tai oikealla puolella ja vetämällä sitä vasemmalle tai oikealle haluttuun leveyteen. Dynamics 365 for Operations tallentaa haluamasi leveyden ja näyttää kyseisen sarakkeen tässä leveydessä aina, kun avaat kyseisen luettelon sisältämän sivun. 

**Pikavälilehdet:** Joillain sivuilla on laajennettavia osioita nimeltä pikavälilehdet. Dynamics 365 for Operations tallentaa tiedon, mitkä pikavälilehdet olet laajentanut ja mitkä pikavälilehdet olet tiivistänyt. Aina palatessasi sivulle samat pikavälilehdet laajennetaan tai tiivistetään edellisen käyttökertasi perusteella. Tässä artikkelissa kerromme, miten voit muuttaa pikavälilehtien osioiden järjestystä. Joissain tapauksissa pikavälilehden tiivistäminen parantaa suorituskykyä, koska Dynamics 365 for Operationsin ei tarvitse noutaa tietoja kyseistä pikavälilehteä varten ennen kuin se laajennetaan. 

**Tietoruudut:** Joillain sivuilla on osioita nimeltä Tietoruutu. Tämä ruutu sisältää kyseisen sivun aihepiiriin liittyvää tietoa vain-luku-muodossa. Kutakin Tietoruutu-osion osa kutsutaan Tietoruuduksi. Voit laajentaa tai tiivistää Tietoruudun, ja Dynamics 365 for Operations tallentaa valintasi. Joissain tapauksissa Tietoruudun tiivistäminen parantaa suorituskykyä, koska Dynamics 365 for Operationsin ei tarvitse noutaa tietoja kyseistä Tietoruutua varten ennen kuin se laajennetaan.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Eksplisiittinen mukauttaminen Mukauttaminen-työkalurivin avulla
Jokaisella henkilöllä ja yrityksellä on eri perspektiivi siihen, mitkä tiedot ovat heille tärkeimpiä, tai mitkä tiedot eivät ole tarpeen heidän tavassaan harjoittaa liiketoimintaa. Mahdollisuus muokata tapaa, jolla tiedot järjestetään, miten niiden kanssa ollaan vuorovaikutuksessa tai jopa miten ne piilotetaan, on avain siihen, miten Dynamics 365 for Operationsista tehdään henkilökohtainen ja tuottava kokemus. 

Eksplisiittinen mukauttaminen on mukauttamista, jonka suoritat nimenomaisena tarkoituksenasi muuttaa elementin tai sivun ulkonäköä valitsemalla mukauttamisvalikko. Perustasollaan eksplisiittistä mukauttamista on, kun napsautat elementtiä hiiren oikealla painikkeella ja valitset **Mukauta**. (Huomaa, että kaikkia sivusi elementtejä ei voida mukauttaa.). Kun valitset tämän mukauttamistavan, näet elementin ominaisuusikkunan. 

[![Elementin ominaisuuksien mukauttaminen](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Voit mukauttaa sivun elementtiä tällä tavoin, jos haluat vain muuttaa elementin otsikkoa, piilottaa elementin niin, että se ei näy sivulla (mitään tietoja ei muuteta, mutta tiedot eivät ole näkyvissä), sisällyttää tiedot pikavälilehden yhteenveto-osioon (jos elementti on pikavälilehdessä), ohittaa kentän sarkaimella siirryttäessä tai määrittää sen niin, ettei tietoja ei voi muuttaa, liittämällä siihen Älä muokkaa -merkinnän. 

Kun haluat siirtää tai piilottaa elementtejä tai tehdä useita muutoksia, voit käyttää Mukautus-työkaluriviä, joka on käytettävissä elementin Ominaisuusikkunasta valitsemalla **Mukauta tämä lomake**. Mukauttaminen-työkalurivi on myös käytettävissä lomakkeen Toimintoruudun kautta **Asetukset**-välilehden Mukauttaminen-ryhmässä. Valitse **Mukauta tämä lomake** ja saat näkyviin Mukauttaminen-työkalurivin. 

[![Mukauttamisen työkalurivi](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Mukauttaminen-työkalurivi sisältää useita mukauttamistoimintoja. Napsauta **Valitse**-työkalua, kun haluat valita ja muuttaa useiden elementtien ominaisuuksia yksi kerrallaan. Napsauta ensin Valitse-työkalua ja valitse sitten elementti, jonka ominaisuuksia haluat muokata. Kun valitset elementin, sen ominaisuusikkuna avautuu ja voit muokata elementin kaikkia ominaisuuksia. Voit toistaa prosessin muille lomakkeesi elementeille, jotka ovat mukautettavissa. Joissain tapauksissa voit valita elementin ja huomaat, että joitain ominaisuuksia ei voida muokata. Tämä tarkoittaa, että elementin nykyisen käyttötavan perusteella Dynamics 365 for Operations ei voi antaa sinun muuttaa kyseistä ominaisuutta. Et esimerkiksi voi piilottaa kenttää, jota tarvitaan. 

Valitse **Siirrä**-työkalu, kun haluat valita ja siirtää elementin toiseen sijaintiin nykyisen elementtiryhmän sisällä. (Et voi siirtää elementtiä sen pääryhmän ulkopuolelle). Napsauta ensin Siirrä-työkalua ja valitse sitten elementti, jonka haluat siirtää. Kun napsautat elementtiä, jonka haluat siirtää, Dynamics 365 for Operations skannaa lomakkeen selvittääkseen, minne tämä elementti voidaan siirtää ja luo sitten sarjan "pudotusvyöhykkeitä", jotka näytetään värillisenä, lihavoituna rivinä sen alueen vieressä, mihin elementti voidaan pudottaa vetäessäsi sitä nykyisen ryhmän sisällä. 

Valitse **Piilota**-työkalu, kun haluat valita ja piilottaa elementin. Piilota elementti valitsemalla Piilota-työkalu ja napsauttamalla sitten elementtiä, jonka haluat piilottaa. Kun valitset Piilota-työkalun, kaikki sillä hetkellä piilotetut elementit tulevat näkyviin varjostettuun säilöön niin, että voit valita elementin, jonka piilotuksen haluat perua. Napsauta Valitse-työkalua katsoaksesi, miltä sivu tulee näyttämään, kun valitut elementit on piilotettu. Valitse **Yhteenveto**-työkalu, kun haluat näyttää numeerisen tai merkkijonokentän pikavälilehden yhteenvetoalueella. Yhteenvetotyökalu koskee vain kenttiä, jotka sisältyvät pikavälilehtiosioon. Kun valitset yhteenvetotyökalun, Dynamics 365 for Operations näyttää kaikki kentät, jotka on valittu yhteenvetokentiksi sisällyttämällä ne varjostettuun säilöön. Voit lisätä ja poistaa kenttiä interaktiivisesti pikavälilehden yhteenvedosta napsauttamalla kenttää. 

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
Koontinäyttö on usein ensimmäinen sivu, jonka näet kun avaat Dynamics 365 for Operationsin. Voit mukauttaa koontinäytön nimeämällä uudelleen työtilasi siirtymisruudut, näyttämällä vain haluamasi ruudut, nimeämällä ruudut uudelleen, tai järjestämällä ruudut haluamaasi järjestykseen. Mukauta koontinäkymä valitsemalla mikä tahansa ruutu ja avaa kontekstivalikko napsauttamalla hiiren oikealla painikkeella. Valitse kontekstivalikossa **Mukauta**. Jos valittu ruutu on se, jonka haluaisit piilottaa, nimetä uudelleen tai ohittaa, voit tehdä muutoksen suoraan esiin tulleessa Ominaisuudet-ikkunassa. Jos haluat järjestää ruudut, valitse **Mukauta tämä lomake** Ominaisuudet-ikkunassa avataksesi Mukauttaminen-työkalurivin. Voit sitten järjestää ruudut Siirrä-työkalun avulla.

## <a name="administration-of-personalization"></a>Mukauttamisen hallinta
Sivu voidaan mukauttaa ja jakaa muiden käyttäjien kanssa yksinkertaisesti suorittamalla mukautetun sivun vienti ja pyytämällä muita käyttäjiä siirtymään mukautetulle sivulle ja tuomaan luomasi mukautustiedosto. Jos käyttäjällä on järjestelmänvalvojan oikeudet, hän voi myös hallita muiden käyttäjien mukautuksia **Mukautusasetukset**-sivulla. B-sivulle siirtyminen Löydät **Mukauttaminen**-sivulta kaksi välilehteä, joista toisen otsikko on **Järjestelmä** ja toisen** Käyttäjät**. 

**Järjestelmä:** Täällä voit tilapäisesti poistaa käytöstä tai "sammuttaa" kaiken mukauttamisen järjestelmässä. Tämä ei poista mukautuksia vaan palauttaa kaikki lomakkeet niiden oletustilaan. Voit myöhemmin ottaa mukautukset uudelleen käyttöön siten, että kaikki mukautukset ovat taas käytössä jokaisessa käyttäjän lomakkeessa. Voit myös poistaa kaikkien käyttäjien kaikki mukautukset. Huomioi, että kun poistat kaikki mukautukset, ei ole mitään tapaa ottaa ne uudelleen käyttöön järjestelmän kautta. Varmista, että olet vienyt ne mukautukset, jotka haluat mahdollisesti tuoda ennen tämän vaiheen suorittamista. 

**Käyttäjät:** Tässä voit päättää kunkin käyttäjän kohdalla, voivatko he suorittaa implisiittistä vai eksplisiittistä mukautusta. Voit myös päättää kunkin käyttäjän kohdalla, voivatko he suorittaa implisiittistä vai eksplisiittistä mukautusta tietyllä lomakkeella. Viimeisenä, voit tuoda, viedä tai poistaa mukautukset kullekin käyttäjälle. 

**Huomautus:** Ensimmäisessä versiossaan mukautuksen hallinta sallii vain käyttäjäkohtaisen hallinnan.




