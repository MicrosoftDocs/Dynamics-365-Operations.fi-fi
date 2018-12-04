---
title: Kulujen hallinnan parametrit
description: Kulujen hallintaa ohjataan seuraavilla parametreilla.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 22f766b780d10d4fc615660990729f008007787a
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="expense-management-parameters"></a>Kulujen hallinnan parametrit

[!include [banner](../includes/banner.md)]

-----------------------------

Kulujen hallintaa ohjataan yleisesti seuraavilla parametreilla.

### <a name="general"></a>Yleiset

| **Kenttä**                                                | **Kuvaus**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Vakiokilometrikorvaus**                             | Anna kilometrikorvaus. Hinta kerrotaan kulussa ilmoitetulle kilometrimäärälle, jonka perusteella lasketaan matkakuluista hyvitettävä summa.                       |
|**Henkilökohtaisten kulujen maksaja**                             | Valitse, kuka on vastuussa henkilökohtaisiksi luokiteltavien luottokorttitapahtumien summien maksamisesta.                                                                                                     |
|**Näytä koko kuluraportti takaisin siirtymisen yhteydessä**               | Valitse tämä vaihtoehto, jos haluat nähdä kuluraportin kaikki kulut katsottaessa tietyn tositteen alkuperäisen asiakirjan tietoja. Tämä tosite luotiin, kun kuluraportti kirjattiin.              |
|**Matka on esihyväksyttävä**                 | Valitse tämä vaihtoehto, jos edellytät, että pyyntö on lähetettävä ja hyväksyttävä, ennen kuin työntekijä voi lähettää kuluraportin.                                                                    |
|**Salli jakojen muokkaaminen ennen kirjaamista**            | Valitse, voidaanko kuluraportti jakoja muokata ennen kirjaamista.                                                                                                                 |
|**Laske kulujen hallintakäytännöt**                     | Valitse, milloin kulut lasketaan, jotta voidaan selvittää, rikkovatko ne kulukäytäntöä. Kulujen mahdolliset rikkomukset voidaan tarkistaa kulun kirjauksen ja tallennuksen yhteydessä tai kun kulu lähetetään hyväksyttäväksi. Pakolliset kuittien käytäntösäännöt tarkistetaan, kun kulurivi tallennetaan.                   |
|**Salli konsernin sisäiset kulurivit**                         | Valitse, sallitaanko muiden yrityksen kulujen kirjaaminen kuluraportissa.                                                                                                          |
|**Salli luottokorttikulujen vaihtokurssin muokkaus** | Valitse tämä vaihtoehto, jos käyttäjät voivat muokkaa tuotujen luottokorttikulujen vaihtokurssia.                                                                        |
|**Näytettävät monitasoisen hierarkian kentät**                  | Valitse, mitkä hyväksyjän kentät näkyvät, kun kuluraportin työnkulun määritystyypiksi on määritetty hierarkia ja hierarkiavalinta on määritetty käyttämään kulun monitasoista hyväksymishierarkiaa. Kun työnkulussa käytetään monitasoista hyväksymishierarkiaa, valitut kentät näkyvät muokattavina kuluraportissa. |
|**Anna työntekijän luottokortin numero (heinäkuun 2017 päivitys)**     | Valitse, voidaanko työntekijän 15- tai 16-merkkinen luku antaa ja tallentaa **Kortin tunnus** -kentässä **Luottokortit**-sivulla.                                                                          |

### <a name="financial"></a>Taloushallinto

| **Kenttä**                                                            | **Kuvaus**     |
|----------------------------------------------------------------------|------------------------------------|
|**Kirjanpidon kirjauskansion nimi**                                         | Valitse sen kirjanpidon kirjauskansion nimi, johon hyväksytyt kuluraportit kirjataan.            |
|**Ota kulujen veronpalautus käyttöön**                                  | Valitse tämä vaihtoehto, jos haluat ottaa käyttöön kulujen veronpalautukset soveltuvissa kuluissa. Tämä vaihtoehto ei voi olla käytössä, jos Yhdysvaltojen arvonlisävero- ja käyttöverosäännöt on otettu käyttöön.      |
|**Kirjaa käteisennakot välittömästi**                                     | Valitse tämä vaihtoehto, jos haluat kirjata hyväksytyt käteisennakot, kun maksu- ja siirtoprosessi on valmis. Jos tätä vaihtoehtoa ei valita, maksu- ja siirtoprosessi luo kirjaamattoman kirjauskansion. |
|**Korjaa kirjauspäivä kirjauksen yhteydessä**                             | Valitse tämä vaihtoehto, jos haluat päivittää kulujen kirjauspäivänpidon, mikäli kuluva kausi on pidossa tai suljettu. Kirjauspäivä määritetään seuraavaan avoimeen kauteen.   |
|**Salli tapahtumien ryhmittely maksutavassa määritetyn vastatilin perusteella**      | Valitse tämä vaihtoehto, jos haluat yhteenvedon kuluraportin kulutapahtumista kulujen maksutavassa määritetyn vastatilin perusteella.   
|**Vero sisältyy**                                                   | Valitse tämä vaihtoehto, jos haluat, että arvonlisävero sisältyy oletusarvoisesti kulusummaan.             |
|**Vapauta varaukset matkustusehdotusten sulkemisen yhteydessä**            | Valitsema tämä vaihtoehto, jos haluat vapauttaa varaukset, kun hyväksytty matkustusehdotus suljetaan.                                                                                   |
|**Salli matkustusehdotuksen lähettäminen budjetin ylittyessä, kun kyseessä on budjettirekisteri tai projektibudjetti** | Valitse tämä vaihtoehto, jos haluta, että työntekijät saavat lähettää hyväksyttäväksi matkustusehdotuksia, jotka ylittävät budjettirekisterissä määritetyn sallittu budjetin tai projektin sallitun budjetin.            |
|**Salli kuluraportin lähettäminen budjetin ylittyessä, kun kyseessä on budjettirekisteri tai projektibudjetti**    | Valitse tämä vaihtoehto, jos haluta, että työntekijät saavat lähettää hyväksyttäväksi kuluraportteja, jotka ylittävät budjettirekisterissä määritetyn sallittu budjetin tai projektin sallitun budjetin.                |
|**Salli kuluraportin hyväksyminen budjetin ylittyessä vain, kun kyseessä on budjettirekisteri**                | Valitse tämä vaihtoehto, jos haluat, että hyväksyjät saavat hyväksyä kuluraportit, jotka ylittävät budjettirekisterissä määritetyn budjetin.                                                                       |

### <a name="per-diem"></a>Päiväraha

| **Kenttä**                             | **Kuvaus**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Päivärahan vähimmäistunnit**           | Anna pienin oletustuntimäärä, jonka työntekijän on päivän aikana tehtävä töitä, jotta matkakuluihin liittyvä päiväraha voidaan maksaa.  Tätä arvoa käytetään vain oletusarvona päivärahatasojen Minimitunnit-kentässä.                                                                                      |
|**Ateriaprosentti**                          | Anna matkakuluihin liittyvänä ensimmäisenä ja viimeisenä päivänä käytettävä aterioiden oletusarvoinen prosenttiosuus päivärahasta, kun **Laske ateriavähennys käyttäen:** -kentässä on valittu joko **Päiväkohtainen ateriatyyppi** tai **Aterioiden määrä päivässä**. Ensimmäisen ja viimeisen päivän työpäivä voi olla lyhyempi kuin tavallinen työpäivä. Tämän vuoksi näiden päivien päivärahan määrä voi poiketa vakiomäärästä. Jos prosentiksi määritetään 0, ensimmäisen ja viimeisen päivän vähennys on 0,00. |
|**Hotelliprosentti**                        | Anna matkakuluihin liittyvänä ensimmäisenä ja viimeisenä päivänä hotelleihin käytettävä oletusarvoinen prosenttiosuus päivärahasta. Ensimmäisen ja viimeisen päivän työpäivä voi olla lyhyempi kuin tavallinen työpäivä. Tämän vuoksi näiden päivien päivärahan määrä voi poiketa vakiomäärästä. Jos prosentiksi määritetään 0, ensimmäisen ja viimeisen päivän vähennys on 0,00.                                              |
|**Muu prosentti**                        | Anna matkakuluihin liittyvänä ensimmäisenä ja viimeisenä päivänä sekalaisiin kuluihin käytettävä oletusarvoinen prosenttiosuus päivärahasta. Ensimmäisen ja viimeisen päivän työpäivä voi olla lyhyempi kuin tavallinen työpäivä. Tämän vuoksi näiden päivien päivärahan määrä voi poiketa vakiomäärästä. Jos prosentiksi määritetään 0, ensimmäisen ja viimeisen päivän vähennys on 0,00.                                                                                                     |
|**Aamiaisen prosenttivähennys** | Anna määrä, jolla aamiainen vähentää päivärahaa. Jos työntekijä esimerkiksi saa ilmaisen aamiaisen, voit pienentää päivärahasummaa kymmenen prosenttia.                               |
|**Lounaan prosenttivähennys**    | Anna määrä, jolla lounas vähennetään päivärahasta. Jos työntekijä esimerkiksi saa ilmaisen lounaan, voit pienentää päivärahasummaa kymmenen prosenttia.                                       |
|**Päivällisen prosenttivähennys**   | Anna määrä, jolla päivällinen vähennetään päivärahasta. Jos työntekijä esimerkiksi saa ilmaisen päivällisen, voit pienentää päivärahasummaa kymmenen prosenttia.                                     |
|**Laske ateriavähennys käyttäen:**         | Valitse, miten järjestelmä laskea päivärahan ateriavähennyksen valitsemalla, perustuuko vähennys matka- vai päiväkohtaiseen ateriatyyppiin vai perustuuko se kullekin päivälle sallittujen aterioiden määrään.|
|**Päivärahapyöristys**                  | Valitse päivärahakuluissa käytettävä pyöristystapa. Jos valitset normaalin pyöristyksen, kaikki päivärahakulut, joiden summa on 0,50, pyöristetään ylöspäin arvoon 1,00, kun taas päivärahakulut, joiden summa on alle 0,50 pyöristetään alaspäin arvoon 0,00.                                                                                              |
|**Päivärahalaskenta perustuu**         | Valitse, perustuuko päivärahasumma kalenteripäiviin vai 24 tunnin jaksoihin.       |

### <a name="fax-cover-pages"></a>Faksin kansilehdet

| **Kenttä**                      | **Kuvaus**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Ohjeet**                   | Anna ohjeet, joita työntekijöiden on noudatettava, kun he luovat kansilehden faksille, jolla lähetetään kuluraporttiin liittyviä kuitteja. Valitsemalla **Käännökset** voit antaa kielikohtaisen tekstin, joka näytetään käyttäjän kielen perusteella. |
|**Käyttäjätunnus (Viivakoodin tiedot)** | Valitse tämä vaihtoehto, jos haluat tallentaa työntekijän yksilöivän tunnuksen faksin kansilehdessä käytettävään viivakoodiin.                 |
|**Viivakoodi**                      | Valitse faksin kansilehdellä käytettävä viivakoodi. Kulujen hallinta tukee viivakoodeja 39 ja 128.               |

### <a name="anti-corruption"></a>Korruption vastainen

|                 <strong>Kenttä</strong>                 |                                                                                                                                                                                            <strong>Kuvaus</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Näytä korruption vastainen todennus</strong>  | Valitse tämä vaihtoehto, jos haluat näyttää korruption vastaisen tekstin uutta kuluraporttia luotaessa. Tämän jälkeen voidaan ottaa käyttöön tiettyjä kululuokkia, jotka edellyttävät korruption vastaisen todennuksen valitsemista kuluraportissa. Esimerkiksi virkamieskuluihin liittyvä lahjaluokka voi edellyttää, että työntekijä vahvistaa kulujen vastaavan yrityksen virkamiehiin liittyvää käytäntöä. |
| <strong>Lähettäjän korruption vastainen sanoma</strong> |                                                                                             Anna teksti, jonka työntekijä näkee uutta kuluraporttia luodessaan. Valitsemalla <strong>Käännökset</strong> voit antaa kielikohtaisen tekstin, joka näytetään käyttäjän kielen perusteella.                                                                                             |
| <strong>Hyväksyjän korruption vastainen sanoma</strong>  |                                                                                             Anna teksti, jonka hyväksyjä näkee uutta kuluraporttia luodessaan. Valitsemalla <strong>Käännökset</strong> voit antaa kielikohtaisen tekstin, joka näytetään käyttäjän kielen perusteella.                                                                                             |


