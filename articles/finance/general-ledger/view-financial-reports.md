---
title: Raporttien tarkasteleminen
description: Tässä ohjeaiheessa käsitellään talousraporttien tarkastelemista ja niihin perehtymistä Microsoft Dynamics 365 Financessa. Artikkelissa on tietoja erilaisista vaihtoehdoista, joilla voit muuttaa talousraporttien ulkoasua ja niihin sisältyviä tietoja.
author: kweekley
ms.date: 03/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f729b1703a7703a8a604b007bd1c8d9e1f604a6
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897281"
---
# <a name="view-financial-reports"></a>Raporttien tarkasteleminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään talousraporttien tarkastelemista ja niihin perehtymistä. Artikkelissa on tietoja erilaisista vaihtoehdoista, joilla voit muuttaa talousraporttien ulkoasua ja niihin sisältyviä tietoja.

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
Voit lisätä ominaisuus- ja dimensiosuodattimia tai vaihtaa budjettisuunnitelmaa **todellinen vs. budjetti** -raportissa. Valitse toimintoruudussa **Raportin asetukset** ja noudata sitten jotakin seuraavista askelista:

-   Käyttääksesi raportissa ominaisuus suodattimia, valitse **lisää ominaisuus suodatin**. Valitse määrite, näppäile määritteen arvo ja klikkaa sitten **OK**. Esimerkiksi jos valitset **tililuokka**-määritteen, syötä **myynti** määritteen arvona. Poistaaksesi määritte-suodattimen, klikkaa **poista**.
-   Käyttääksesi raportissa dimensioiden suodattimia, valitse **Lisää dimension suodatin**. Valitse dimensio ja kirjoittaa joko dimensiotunnus tai valitse dimensio luettelosta. Poistaaksesi dimensiosuodattimen, klikkaa **poista**.
-   Muuttaaksesi skenaariota **todellinen vs. budjetti** -raportissa, valitse uusi skenaario ja valitse sitten **OK**. Jos valittu skenaario on eri tilikaudelle, tuloksia ei palauteta. Jos esimerkiksi raportti luodaan FY2015:lle ja nykyinen skenaario on FY2015 ja uusi valittu skenaario on FY2016, tuloksia ei palauteta. Jos tarvitaan uusi skenaario eri tilikaudelle, luo skenaarioon liittyvä uusi raportti tilikaudelle.

Kun klikkaat **OK**, kaikki valitsemasi vaihtoehdot käytetään raporttiin. Jos päätät, että et halua käyttää valittuja asetuksia, klikkaa **peruuta**.

## <a name="update-a-financial-report"></a>Päivitä talousraportti
Voit päivittää (päivitys) talousraportin siten, että siinä näkyy kaikkein viimeisimmät tiedot sille vuodelle ja kaudelle, jolle raportti luotiin. Jos esimerkiksi päivität talousraportin, joka on luotu lokakuulle 2015, raportti sisältää kaikki uudet lokakuulle 2015 kirjatut tapahtumat. Päivitä raportti valitsemalla toimintoruudussa **Päivitä**. Päivitetty raportti on saatavissa vain sen päivittäneelle henkilölle. Raportti on julkaistava, jotta muut käyttäjät näkevät samat tiedot.

## <a name="publish-a-financial-report"></a>Julkaise talousraportti
Kun olet päivittänyt talousraportin, voit julkaista sen. Organisaation muut käyttäjät voivat sitten tarkastella sitä. Julkaistaksesi raportin toimintoruudussa, klikkaa **julkaise**.

## <a name="display-a-financial-report-in-a-different-currency"></a>Näytä talousraportti eri valuuttana
Talousraportti voidaan näyttää minä vain valuuttana milloin tahansa. Näyttääksesi raportin toisena valuuttana, toimintoruudussa, klikkaa **valuutta** ja valitse sitten valuutta. Raportti käännetään kyseiseksi valuutaksi ja tulokset näytetään. kaikki valuuttakoodit tai merkit, jotka sisällytetään raportin rakenteen osaksi, päivitetään vastaamaan uutta valuuttaa. Luettelossa näkyvät valuutat ovat raportoinnin valuuttoja, jotka on määritetty Financessa.

## <a name="display-a-summarized-view-of-the-financial-report"></a>Näytä talousraportti yhteenvetona
Talousraportti voi sisältää erittelyrivejä ja yhteenveto-rivejä. Erittelyrivit ovat rivejä, joilla on päätilit tai dimensiot. Yhteenvetorivit ovat kuvaus-, summa- ja laskentarivejä. Näyttääksesi vain yhteenvetorivit raportissa, klikkaa **näytä** ja valitse sitten **vain yhteenvetorivit**. Raportti on tiivistetty ja näyttää vain yhteenvetorivit. Nähdäksesi yhteenvetorivit sekä erittelyrivit, klikkaa **näytä** ja valitse sitten **vain yhteenvetorivit** uudelleen.

## <a name="print-a-financial-report"></a>Tulosra talousraportti
Taloushallinnon raportin tulostaminen luo PDF-tiedoston, joka voidaan sitten tulostaa manuaalisesti. Luo tulostettava talousraportti valitsemalla toimintoruudussa **Tulosta** ja määritä sitten tulostusasetukset seuraavien ohjeiden mukaan:

-   Sisällyttääksesi yksityiskohtaisia tasoja tulostettavaan raporttiin, säädä liukusäätimellä **kyllä** tai **ei**. Jos raportissa käytetään raportointipuuta, voit valita kaikki raportointiyksiköt tai vain nykyisen raportointiyksikön.
-   Määrittääksesi sivun koon, valitse luettelosta sivun koko.
-   Määrittääksesi sivun asettelun, valitse sivun asettelu luettelosta. Jos haluat raportin sisällön mahtuvan leveyteen, jonka olet valinnut, aseta liukusäädin asentoon **kyllä**.
-   Määrittääksesi sivun varmuusmarginaalit, kirjoita ylä- ja alamarginaalin sekä vasemman ja oikean marginaalin koko tuumina.

Kun tulostusasetukset on määritetty, jatka valitsemalla **Tulosta**, jolloin kysytään, haluatko ladata tiedoston, tai tallennan tiedosto OneDriveen tai SharePointiin. Jos päätät, ettet halua jatkaa, valitse siinä tapauksessa **Peruuta**. Kun jatkat, raportin hahmonnus palvelimessa alkaa ja sinua pyydetään lataamaan raportti PDF-muodossa. Voit nyt tarkastella raporttia PDF-katseluohjelmassa sekä valita tulostimen, johon raportti lähetetään, sekä tehdä muutoksia tulostusasetuksiin.

## <a name="export-a-financial-report"></a>Lähetä talousraportti
Lähettääksesi talousraportin. toimintoruudussa, klikkaa **lähetä**. Raportti lähetetään Microsoft Exceliin ja selaimesi kysyy, haluatko avata tai tallentaa vientitiedostoon. Vientiasetuksia, jotka on määritetty raportin suunnittelussa, käytetään vietävään raporttiin.    

<a name="additional-resources"></a>Lisäresurssit
--------

[Talousraportointi](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]