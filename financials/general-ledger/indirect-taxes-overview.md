---
title: "Arvonlisäveron yleiskuvaus"
description: "Tämä artikkeli sisältää arvonlisäverojärjestelmän yleiskatsauksen. Artikkelissa esitellään arvonlisäveroasetusten elementit ja se, miten ne toimivat yhdessä."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: bdb3188f533cf0cdb1e70c63891408e45d02418d
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="sales-tax-overview"></a>Arvonlisäveron yleiskuvaus

[!include[banner](../includes/banner.md)]


Tämä artikkeli sisältää arvonlisäverojärjestelmän yleiskatsauksen. Artikkelissa esitellään arvonlisäveroasetusten elementit ja se, miten ne toimivat yhdessä.

<a name="overview"></a>Yleiskuvaus
--------

Arvonlisäveroympäristö tukee monenlaisia välillisiä veroja, kuten arvonlisäveroja (ALV), GST-veroa, yksikköperusteisia maksuja ja ennakonpidätystä. Nämä verot lasketaan ja dokumentoidaan osto- ja myyntitapahtumien aikana. Ne on myös ilmoitettava ja maksettava veroviranomaisille säännöllisesti. 

Yksiköt, joista veroasetukset kostuvat, ja niiden väliset suhteet näkyvät seuraavassa kaaviossa.

[![TaxOverview](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

Jokaiselle yrityksen kirjaamalle arvonlisäverolle on määritettävä arvolisäverokoodi. Arvonlisäverokoodi sisältää veroprosentin ja arvonlisäveron laskusäännöt. 

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
Arvonlisävero on ilmoitettava ja maksettava veroviranomaisille säännöllisin väliajoin (esimerkiksi kuukausittain tai neljännesvuosittain). Microsoft Dynamics 365 for Operationsissa on toimintoja, joilla voit tilittää kauden verotilit ja vastakirjat saldot verotilitystilille kirjanpidon kirjausryhmien määritysten mukaisesti. Voit käyttää tätä toimintoa **Tilitä ja kirjaa arvonlisävero** -sivulla. Arvonlisäveron tilityskausi, jonka ajalta arvonlisäverot on tilitettävä, on määritettävä. 

Kun arvonlisävero on maksettu, arvolisäveron tilitystilin saldo on täsmäytettävä pankkitiliin. Jos arvonlisäveron tilityskaudessa määritetty arvonlisäveroviranomainen liittyy toimittajatiliin, arvolisäveron saldo kirjataan avoimena toimittajan laskuja, joka voidaan sisällyttää säännölliseen maksuehdotukseen.

## <a name="conditional-sales-tax"></a>Suoritusperusteinen vero
Suoritusperusteinen vero ilmaisee, että arvonlisävero on maksettava suhteessa laskulla maksettuun summaan. Vastaavasti normaali ALV lasketaan laskutuksen yhteydessä. Suoritusperusteinen vero on maksettava veroviranomaiselle maksun kirjaamisen yhteydessä, ei laskua kirjattaessa. Kun lasku on kirjattu, tapahtuma on raportoitava arvonlisäverokirjan raporttiin. Tapahtuma on kuitenkin jätettävä pois arvonlisäveron maksuraportista. 

Jos valitset Suoritusperusteinen vero -valintaruudun Kirjanpidon parametrit -lomakkeessa, arvonlisäveroa ei voida vähentää ennen kuin lasku on maksettu. Tämä on juridinen edellytys muutamissa maissa/alueilla.

> [!NOTE]
> Kun valitset Suoritusperusteinen vero -valintaruudun, toiminnon käyttäminen edellyttää arvonlisäverokoodien ja -ryhmien määrittämistä ja kirjanpidon kirjausryhmien luomista. |

###  <a name="example"></a>Esimerkki

Arvonlisäverot tilitetään kuukausittain. Kesäkuun 15. päivä luodaan asiakaslasku 10 000 + ALV.
-   Arvonlisävero on 25 prosenttia eli 2 500 euroa.
-   Lasku on maksettava 30.7.

Yleensä ALV 2 500 olisi tilitettävä ja maksettava veroviranomaiselle laskun kirjaamisen yhteydessä kesäkuussa, vaikka et ole saanut maksua asiakkaalta. 

Jos kuitenkin käytät suoritusperusteista arvonlisäveroa, täsmäytät veron veroviranomaiselle, kun saat maksun asiakkaalta 30.7.




