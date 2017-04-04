---
title: "Näytä raportit"
description: "Tässä artikkelissa käsitellään talousraporttien tarkastelemista ja niihin perehtymistä Microsoft Dynamics AX:ssä. Artikkelissa on tietoja erilaisista vaihtoehdoista, joilla voit muuttaa talousraporttien ulkoasua ja niihin sisältyviä tietoja."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 5535a7897eb328e97a9c8a4ca7986ed5cf9381af
ms.lasthandoff: 03/31/2017


---

# <a name="view-financial-reports"></a>Näytä raportit

Tässä artikkelissa käsitellään talousraporttien tarkastelemista ja niihin perehtymistä Microsoft Dynamics AX:ssä. Artikkelissa on tietoja erilaisista vaihtoehdoista, joilla voit muuttaa talousraporttien ulkoasua ja niihin sisältyviä tietoja.

<a name="financial-reporting-overview"></a>Taloushallinnon raportoinnin yleiskatsaus
----------------------------

## <a name="open-a-financial-report"></a>Avaa taloudellinen raportti
Voit avata raportin valitsemalla raportin nimen. Kun raportti avataan ensimmäistä kertaa, se luodaan automaattisesti edelliselle kuukaudelle. Jos esimerkiksi avaat raportin ensimmäisen kerran elokuussa 2015, raportti luotiin päivämäärälle 31.7.2015. Kun raportti on avattu, voit aloittaa siihen perehtymisen porautumalla tiettyyn tietoon ja muuttamalla raporttiasetuksia.

## <a name="drill-down-on-a-financial-report"></a>Raportin tietoihin perehtyminen
Taloudelliset raportit voivat sisältää useita yksityiskohtaisia tasoja. Taloushallinnon taso on ensimmäinen taso jonka näet, kun avaat taloushallinnon raportin. Siirtyäksesi kirjanpitotasoon, valitse tiedot joihin haluat perehtyä. Esimerkiksi, tarkastellaksesi tilin myyntitietoja, valitse myyntitiedot, joita haluat tutkia. Kirjanpitotasolta, voit mennä alaspäin tarkastelemaan tapahtumia, joista tilin saldo muodostuu. Voit tarkastella tapahtumia kahdella tavalla: raportin tapahtumat ja tositetapahtumat.

-   **Raportin tapahtumat** – tapahtumat näkyvät muotoillussa näkymässä, joka kuuluu taloushallinnon raporttiin. Tarkastellaksesi tapahtumia muotoillussa näkymässä, valitse tieto johon haluat perehtyä ja valitse sitten **Perehdy raportin tapahtumatasolle**.
-   **Tositetapahtumat** – tositteen tapahtumakysely avautuu, jossa voit tarkastella tapahtumia. Voit tarkastella tositetapahtumakyselyn tapahtumia valitsemalla tiedon, johon haluat porautua, ja valitsemalla sitten **Avoimet tilitapahtumat**.

Jos tiedot ovat budjettitietoja, voit avata budjettitilimerkinnöt. Sulkeaksesi raportin tasoja ja palataksesi sinne mistä aloitit, voit painaa Esc-näppäintä tai klikata **Sulje**-painiketta (**X**) oikeassa yläkulmassa.

## <a name="change-report-options"></a>Muuta raporttiasetuksia
Voit muuttaa raportin päivämäärää, lisätä ominaisuus- ja dimensiosuodattimia tai vaihtaa budjettisuunnitelmaa **todellinen vs. budjetti** -raportissa. Valitse toimintoruudussa **Raportin asetukset** ja noudata sitten jotakin seuraavista askelista:

-   Muuttaaksesi raportin perustekautta ja perustevuotta, valitse perustekausi ja perustevuosi ja klikkaa sitten **OK**.
-   Käyttääksesi raportissa ominaisuus suodattimia, valitse **lisää ominaisuus suodatin**. Valitse määrite, näppäile määritteen arvo ja klikkaa sitten **OK**. Esimerkiksi jos valitset **tililuokka**-määritteen, syötä **myynti** määritteen arvona. Poistaaksesi määritte-suodattimen, klikkaa **poista**.
-   Voit käyttää dimensio-suodatukset raporttiin valitsemalla **lisätä dimension suodattimen**. Valitse dimensio ja kirjoittaa Dimensiotunnus tai valitse dimensio-luettelosta. Poistaaksesi dimensiosuodattimen, klikkaa **poista**.
-   Muuttaaksesi skenaariota **todellinen vs. budjetti** -raportissa, valitse uusi skenaario ja valitse sitten **OK**. Jos valittu skenaario on eri vuodelle, varmista päivittää perustevuosi. Esimerkiksi jos nykyinen skenaario on FY2015 ja valitset uuden skenaarion FY2016, sinun on muutettava perustevuosi vuodeksi **2016**.

Kun klikkaat **OK**, kaikki valitsemasi vaihtoehdot käytetään raporttiin. Jos päätät, että et halua käyttää valittuja asetuksia, klikkaa **peruuta**.

## <a name="update-a-financial-report"></a>Päivitä talousraportti
Voit päivittää (päivitys) talousraportin siten, että siinä näkyy kaikkein viimeisimmät tiedot sille vuodelle ja kaudelle, jolle raportti luotiin. Jos esimerkiksi päivität talousraportin, joka on luotu lokakuulle 2015, raportti sisältää kaikki uudet lokakuulle 2015 kirjatut tapahtumat. Päivitä raportti valitsemalla toimintoruudussa **Päivitä**. Päivitetty raportti on saatavissa vain sen päivittäneelle henkilölle. Raportti on julkaistava, jotta muut käyttäjät näkevät samat tiedot.

## <a name="publish-a-financial-report"></a>Julkaise talousraportti
Kun olet päivittänyt talousraportin, voit julkaista sen. Organisaation muut käyttäjät voivat sitten tarkastella sitä. Julkaistaksesi raportin toimintoruudussa, klikkaa **julkaise**.

## <a name="display-a-financial-report-in-a-different-currency"></a>Näytä talousraportti eri valuuttana
Talousraportti voidaan näyttää minä vain valuuttana milloin tahansa. Näyttääksesi raportin toisena valuuttana, toimintoruudussa, klikkaa **valuutta** ja valitse sitten valuutta. Raportti käännetään kyseiseksi valuutaksi ja tulokset näytetään. kaikki valuuttakoodit tai merkit, jotka sisällytetään raportin rakenteen osaksi, päivitetään vastaamaan uutta valuuttaa. Listalla näkyvät valuutat ovat raportoinnin valuuttoja, jotka on määritetty Microsoft Dynamics AX:ssä.

## <a name="display-a-summarized-view-of-the-financial-report"></a>Näytä talousraportti yhteenvetona
Talousraportti voi sisältää erittelyrivejä ja yhteenveto-rivejä. Erittelyrivit ovat rivejä, joilla on päätilit tai dimensiot. Yhteenvetorivit ovat kuvaus-, summa- ja laskentarivejä. Näyttääksesi vain yhteenvetorivit raportissa, klikkaa **näytä** ja valitse sitten **vain yhteenvetorivit**. Raportti on tiivistetty ja näyttää vain yhteenvetorivit. Nähdäksesi yhteenvetorivit sekä erittelyrivit, klikkaa **näytä** ja valitse sitten **vain yhteenvetorivit** uudelleen.

## <a name="open-a-financial-report-from-a-previous-month"></a>Avaa edellisen kuukauden taloudellinen raportti
Voit tarkastella edellisten kuukauksien tai kuluvan kuukauden raportteja ilman raportin uudelleen tekemistä. Avaa raportti edellisen kuukauden, napsauta **näyttää**, ja sitten **Edellinen raportit**. Näkyviin tulee luettelo, joka on luotu raportti edeltävän kuukauden aikana. Laajenna kuukausi lukeaksesi raportin, valitse päivämäärä ja valitse sitten **OK**. Edellisen kuukauden raportti tulee näkyviin. Voit palauttaa kuluvan kuukauden raportin valitsemalla **peruuta**.

## <a name="print-a-financial-report"></a>Tulosra talousraportti
Tulostaaksesi talousraportin toimintoruudussa, valitse **tulosta** ja noudata sitten yhtä tai useampaa seuraavista askeista määrittääksesi tulostusasetukset:

-   Sisällyttääksesi yksityiskohtaisia tasoja tulostettavaan raporttiin, säädä liukusäätimellä **kyllä** tai **ei**. Jos raportissa käytetään raportointipuuta, voit valita kaikki raportointiyksiköt tai vain nykyisen raportointiyksikön.
-   Määrittääksesi sivun koon, valitse luettelosta sivun koko.
-   Määrittääksesi sivun asettelun, valitse sivun asettelu luettelosta. Jos haluat raportin sisällön mahtuvan leveyteen, jonka olet valinnut, aseta liukusäädin asentoon **kyllä**.
-   Määrittääksesi sivun varmuusmarginaalit, kirjoita ylä- ja alamarginaalin sekä vasemman ja oikean marginaalin koko tuumina.

Sen jälkeen, kun olet määritätänyt tulostusasetukset, valitse **tulosta** tulostaaksesi raportin. Jos päätät, että et halua tulostaa raporttia, klikkaa **peruuta** sen sijaan. Tulostettavan raportin esikatselu tulee näkyviin. Voit valita tulostimen, johon raportti lähetetään ja voit myös määrittää tulostusasetuksia.

## <a name="export-a-financial-report"></a>Lähetä talousraportti
Lähettääksesi talousraportin. toimintoruudussa, klikkaa **lähetä**. Raportti lähetetään Microsoft Exceliin ja selaimesi kysyy, haluatko avata tai tallentaa vientitiedostoon. Vientiasetuksia, jotka on määritetty raportin suunnittelussa, käytetään vietävään raporttiin.    

<a name="see-also"></a>Lisätietoja
--------

[Microsoft Dynamics AX:n talousraportointi](/dynamics365/operations/dev-itpro/analytics/financial-reporting-intro)


