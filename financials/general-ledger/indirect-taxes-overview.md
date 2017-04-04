---
title: "Arvonlisäveron yleiskuvaus"
description: "Tämä artikkeli sisältää arvonlisäverojärjestelmän yleiskatsauksen. Artikkelissa esitellään arvonlisäveroasetusten elementit ja se, miten ne toimivat yhdessä."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxPeriod, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13111
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 1adee145d705f239e0c663d310234286478fead0
ms.lasthandoff: 03/31/2017


---

# <a name="sales-tax-overview"></a>Arvonlisäveron yleiskuvaus

Tämä artikkeli sisältää arvonlisäverojärjestelmän yleiskatsauksen. Artikkelissa esitellään arvonlisäveroasetusten elementit ja se, miten ne toimivat yhdessä.

<a name="overview"></a>Yleiskuvaus
--------

Arvonlisävero-kehys tukee monenlaisia välillisten verojen, kuten arvonlisäveron, arvonlisävero (ALV), tavaroiden ja palvelujen tax (GST), yksikkökohtaisena maksut ja ennakonpidätys. Nämä verot lasketaan ja dokumentoitu osto- ja myynti-tapahtumien aikana. Ajoittain ne täytyy raportoida ja makseta veroviranomaisille. 

Yksiköt, joista veroasetukset kostuvat, ja niiden väliset suhteet näkyvät seuraavassa kaaviossa.

[![TaxOverview](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

Jokainen, joka on otettava huomioon yrityksen arvonlisäveron arvonlisäverokoodi on määritettävä. Arvonlisäverokoodi sisältää veroprosentin ja arvonlisäveron laskusäännöt. 

Jokainen arvonlisäverokoodi on linkitettävä arvolisäveron tilityskauteen. Arvonlisäveron tilityskausi määrittää, kuinka usein arvolisävero on ilmoitettava ja maksettava arvonlisäveroviranomaisille. Jokainen arvonlisäveron tilityskausi on määritettävä arvolisäveroviranomaiseen. Arvonlisäveroviranomainen ilmaisee yksikön, jolle arvonlisävero ilmoitetaan ja maksetaan. Se määrittää myös arvonlisäveroilmoituksen asettelun. Arvonlisäveroviranomaiset voivat liittyä toimittajatileihin. 

Jokainen arvonlisäverokoodi on linkitettävä myös kirjanpidon kirjausryhmään. Kirjanpidon kirjausryhmä määrittää päätilin, johon arvonlisäverokoodien summat kirjataan. 

Lisäksi voidaan määrittää valinnaisia arvonlisäveroilmoituksen koodeja. Ne voidaan määrittää arvonlisäverokoodille, jotka on laskettu erilaisten summatyyppien arvonlisäverokoodeille. **Arvonlisäveromaksu koodeittain** -rapotti sisältää annetun arvolisäveron tilityskauden ja välin arvonlisäveroilmoituksen koodikohtaiset kokonaissummat 

Jokaisella tapahtumalla, jolle on laskettava arvonlisävero ja joka on kirjattava, on oltava arvonlisäveroryhmä ja nimikkeen arvonlisäveroryhmä. Arvonlisäveroryhmät liittyvät tapahtuman osapuoleen (kuten asiakkaaseen tai toimittajaan, kun taas nimikkeen arvonlisäveroryhmät liittyvät tapahtuman resurssiin (kuten nimikkeeseen tai hankintaluokkaan). Veroryhmät sisältävät verokoodiluettelon. Tapahtumassa käytetään verokoodeja, joka sisältyvät sekä tapahtuman arvonlisäveroryhmään että nimikkeen arvonlisäveroryhmään. 

Seuraavassa taulussa käsitellään yksiköitä ja veroasetusten järjestystä.

| Määritystapahtuma                                                  | Pakollinen/Valinnainen ja kuvaus                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Luo päätilit.                                           | Pakollinen. Ennen kuin arvonlisäveroihin liittyviä toimintoja voi määrittää, on luotava päätilit, joita yritys käyttää verojen maksamiseen ja kirjaamiseen.                                                                                                                                                                             |
| Aseta arvonlisäveron kirjanpidon kirjausryhmät.                     | Pakollinen. Kirjanpidon kirjausryhmät määrittävät arvonlisäverojen kirjaamisen ja maksamisen päätilit.                                                                                                                                                                                                                            |
| Määritä arvonlisäveroviranomaiset.                                   | Pakollinen. Arvonlisäveroviranomaiset ovat yksiköitä, joille vero on ilmoitettava ja maksettava.                                                                                                                                                                                                                                   |
| Määritä arvonlisäveron tilityskaudet.                            | Pakollinen. Arvonlisäveron tilityskausissa on tiedot siitä, milloin arvonlisävero on ilmoitettava ja maksettava sekä kuinka usein se on tehtävä. Ne on liitetty arvonlisäveroviranomaiseen.                                                                                                                                                       |
| Määritä arvonlisäveroilmoituksen koodit.                               | Valinnainen. Arvonlisäverokoodeille voidaan määrittää arvonlisäveroilmoituksen koodeja, joilla useiden arvolisäverokoodien summat ilmoitetaan yhdellä arvonlisäveroilmoituksen koodilla.                                                                                                                                                                 |
| Määritä arvonlisäverokoodit.                                         | Pakollinen. Arvonlisäverokoodit sisältävät veroprosentit ja kunkin arvonlisäveron laskusäännöt. Arvonlisäverokoodit liittyvät arvonlisäveron tilityskauteen ja kirjanpidon kirjausryhmään.                                                                                                                                        |
| Määritä arvonlisäveroryhmät.                                        | Pakollinen. Arvonlisäveroryhmät sisältää luettelon arvolisäverokoodeista, joita tapahtuman osapuoleen (asiakas tai toimittaja) käytetään. Tiettyä tapahtumaa koskeva arvonlisävero määräytyy sekä tapahtuman arvonlisäveroryhmään että nimikkeen arvonlisäveroryhmään sisältyvien arvonlisäverokoodien mukaan.                  |
| Määritä nimikkeiden arvonlisäveroryhmät.                                   | Pakollinen. Nimikkeen arvonlisäveroryhmät sisältävät luettelon koodeista, joita käytetään tapahtuman resurssille (kuten tuote tai palvelu). Tiettyä tapahtumaa koskeva arvonlisävero määräytyy sekä tapahtuman arvonlisäveroryhmään että nimikkeen arvonlisäveroryhmään sisältyvien arvonlisäverokoodien mukaan. |
| Määritä arvolisäveron parametrit sovelluksen parametrisivulla. | Pakollinen. Parametrit on määritettävä eri alueilla, kuten kirjanpidossa, myyntireskontrassa ja ostoreskontrassa, jotta välilliset verot voidaan laskea oikein. Vaikka useimmilla näistä parametreista on oletusarvot, ne on muokattava kunkin yrityksen tarpeisiin sopiviksi.                                          |

## <a name="sales-tax-on-transactions"></a>Tapahtumien arvonlisävero
Jokaiselle tapahtumalle (kuten myynti- ja ostoasiakirjan riveille ja kirjauskansioille) on annettava arvonlisäveroryhmä tai nimikkeen arvonlisäveroryhmä, jotta arvolisävero voidaan laskea. Oletusryhmät on määritetty päätiedoissa (niitä ovat esimerkiksi asiakas, toimittaja, nimike ja hankintaluokka), mutta voit tarvittaessa muuttaa tapahtuman ryhmiä manuaalisesti. Kummassakin ryhmässä on arvonlisäverokoodiluettelo ja kahden arvolisäverokoodiluettelon leikkauspiste määrittää tapahtumassa käytettävien arvolisäverokoodien luettelon. 

Voit hakea lasketun arvonlisäveron jokaisessa tapahtumassa avaamalla **Arvonlisäverotapahtuma**-sivun. Voit etsiä arvolisäveron joko asiakirjan riville tai koko asiakirjalle. Voit oikaista tiettyjen asiakirjojen (kuten toimittajan laskun ja kirjauskansioiden) lasketun arvonlisäveron, jos alkuperäisessä asiakirjassa on poikkeavia summia.

## <a name="sales-tax-settlement-and-reporting"></a>Arvonlisäveron tilitys ja ilmoittaminen
Arvonlisävero on ilmoitettava ja maksettava veroviranomaisille säännöllisin väliajoin (esimerkiksi kuukausittain tai neljännesvuosittain). Microsoft Dynamics-365 toiminnoissa on toimintoja, joiden avulla voit maksaa veroa välin ja Vastatilin ALV-laskelmatilille kirjanpidon kirjausryhmät on määritetty saldoa. Voit käyttää tätä toimintoa **selvittää ja kirjata arvonlisäveron** sivulla. Arvonlisäveron tilityskauden arvonlisävero tulisi selvittää, on määritettävä. 

Kun arvonlisävero on maksettu, arvolisäveron tilitystilin saldo on täsmäytettävä pankkitiliin. Jos arvonlisäveron tilityskaudessa määritetty arvonlisäveroviranomainen liittyy toimittajatiliin, arvolisäveron saldo kirjataan avoimena toimittajan laskuja, joka voidaan sisällyttää säännölliseen maksuehdotukseen.

## <a name="conditional-sales-tax"></a>Suoritusperusteinen vero
Suoritusperusteinen vero on arvonlisävero, joka maksetaan suhteessa todellisten summa, joka maksetaan lasku. Vastaavasti normaalin ALV lasketaan laskutuksen yhteydessä. Suoritusperusteinen vero on maksettava arvonlisäveroviranomaisen, kun maksu kirjataan, ei silloin, kun lasku kirjataan. Kun lasku on kirjattu, tapahtuma on kuvattava arvonlisäverokirjan raporttiin. Tapahtuma on kuitenkin jätetään arvonlisäveron maksuraportti. 

Jos valitset Suoritusperusteinen vero-valintaruutu parametrit-lomakkeessa Kirjanpito, ei arvonlisäveroa voidaan vähentää ennen kuin lasku on maksettu. Tämä on lakisääteinen joissakin maissa/alueilla.

> [!NOTE]
> Kun valitset Suoritusperusteinen vero-valintaruutu, arvonlisäverokoodien ja arvonlisäveroryhmien määrittäminen ja myös Luo kirjanpidon kirjausryhmät-toiminnot. |

###  <a name="example"></a>Esimerkki

Arvonlisäverot tilitetään kuukausittain. 15. kesäkuuta-Luo myyntilasku 10 000 + ALV.
-   Arvonlisävero on 25 prosenttia eli 2 500.
-   Laskun maksu on maksettava 30 päivänä heinäkuuta.

Voit yleensä on tilitettävä ja maksettava 2 500 veroviranomaiselle kirjaamisen yhteydessä kesäkuussa, vaikka et ole saanut maksun asiakkaalta. 

Kuitenkin Jos käytät suoritusperusteisen arvonlisäveron, selvitetään veroviranomaiselle kun saat maksun asiakkaalta heinäkuun 30.


