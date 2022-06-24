---
title: Näytä lomasaldot tuotannon käyttöliittymässä
description: Tämä artikkeli sisältää esimerkkiskenaarion, jossa esitetään, miten Microsoft Dynamics 365 Supply Chain Management määritetään antamaan työntekijöille palkanlaskennan tilastotietojen avulla yhteenvedon nykyisen vuoden lomasaldosta.
author: johanhoffmann
ms.date: 04/22/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-04-22
ms.dyn365.ops.version: 10.0.XX
ms.openlocfilehash: 2a6b6f52bfa7539b7c9bb5841536b0d564d0274c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852270"
---
# <a name="show-vacation-balances-in-the-production-floor-execution-interface"></a>Näytä lomasaldot tuotannon käyttöliittymässä

[!include [banner](../includes/banner.md)]

Tämä artikkeli sisältää esimerkkiskenaarion, jossa esitetään, miten Microsoft Dynamics 365 Supply Chain Management määritetään antamaan kullekin työntekijälle palkanlaskennan tilastotietojen avulla yhteenvedon nykyisen vuoden lomasaldosta. Työntekijät voivat nähdä lomasaldonsa tuotannon käyttöliittymän **Päivän tehtävät** -valintaikkunassa.

Tässä skenaariossa käytetään Tanskan lomalainsäädäntöä, jossa lomavuosi ulottuu välille 1.9. - 31.8. Tässä skenaariossa yritys on palkannut uuden työntekijän ja myöntää työntekijälle 10 lomapäivän saldon lomavuoden loppuun.

## <a name="turn-on-the-required-features"></a>Tarvittavien ominaisuuksien ottaminen käyttöön

Tämän skenaarion suorittaminen edellyttää, että *Tuotannon käyttöliittymän Päivän tehtävät -näkymä* -ominaisuus otetaan käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Lisätietoja tämän ja muiden ominaisuuksien määrityksestä tuotannon käyttöliittymää varten on kohdassa [Tuotannon käyttöliittymän konfigurointi](production-floor-execution-configure.md).

## <a name="make-sample-data-available"></a>Ota mallitiedot käyttöön

Tämän skenaarion käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.

## <a name="create-a-new-pay-type"></a>Luo uusi maksutyyppi

Luo aluksi uusi *maksutyyppi*, jonka avulla seurataan työntekijöiden ansaittuja lomapäiviä (kutsutaan myös heidän *lomasaldokseen*). Maksutyyppien avulla lasketaan yleensä työntekijöiden palkka. Tässä luotavaa maksutyyppiä käytetään kuitenkin saldon laskemiseen.

1. Siirry kohtaan **Työajan seuranta \> Asetukset \> Palkanlaskenta \> Maksutyypit**
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.
1. Aseta uudelle riville seuraavat arvot:

    - **Maksutyyppi:** *5151-1*
    - **Kuvaus:** *Työntekijänlomapäivien laskuri*
    - **Sisällytä vientiin:** *Ei*

## <a name="update-the-pay-agreement"></a>Päivitä maksusopimus

Tässä osassa voit muokata aiemmin luotua *maksusopimusta* lisäämällä uuden maksutyypin ja määrittämällä säännöt, jotka määrittävät, miten työntekijän lomasaldo oikaistaan lomapäivien rekisteröintiä varten.

1. Siirry kohtaan **Työajan seuranta \> Asetukset \> Palkanlaskenta \> Maksusopimukset**
1. Valitse maksusopimus, jossa haluat määrittää lomakäytännön. (Jos käytät USMF-näytetietoja, käytettävissä on vain yksi maksusopimus, *Man*.)
1. Varmista, että valittu maksusopimus on voimassa kuluvana päivänä. Jos käytät USMF-mallitietoja, *Man*-maksusopimuksen **Päivämäärään**-kentän arvoksi voidaan määrittää jo mennyt päivämäärä. Muuta arvoa niin, että se on tulevaisuudessa vuoden tai kaksi.
1. Valitse toimintoruudussa **Sopimusrivit**.
1. Määritä työkaluriville seuraavat arvot **Maksusopimusrivit**-sivun **Yhteenveto**-pikavälilehdessä:

    - Valitse ensimmäisestä avattavasta luettelosta **Maanantai**.
    - Valitse toisesta avattavasta luettelosta **Poissaolo**.

1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.
1. Määritä uudelle riville **Maksulaji**-kentän arvoksi tälle skenaariolle luomasi maksulaji (*5151-1*). Voit jättää kaikki muut kentät oletusarvoihinsa.
1. Kun uusi rivi on vielä valittuna, määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Poissaolokoodi:** *Loma*
    - **Käytä kiinteää määrää:** *Kyllä*
    - **Vakio:** *-1*

1. Valitse toimintoruudussa **Kopioi päivä**.
1. Määritä **Kopioi päivä** -valintaikkunassa seuraavat arvot:

    - **Tiistai**, **Keskiviikko**, **Torstai** ja **Perjantai:** *Kyllä*
    - **Korvaa:** *Kyllä*
    - **Poissaolo:** *Kyllä*

1. Valitse **OK**.

## <a name="create-a-payroll-statistic-group"></a>Palkanlaskennan tilastoryhmän luominen

*Palkanlaskennan tilastoryhmien* avulla määritetään työntekijöiden rekisteröintien tilastotiedot kauden aikana. Tässä skenaariossa lasketaan palkanlaskennan tilastoryhmän avulla niiden lomapäivien määrä, jotka työntekijät ansaitsevat lomajakson aikana. Tanskassa lomajakso kestää 1.9. - 31.8.

1. Siirry kohtaan **Työajan seuranta \> Asetukset \> Palkanlaskenta \> Palkanlaskennan tilastoryhmät**
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.
1. Aseta uudelle riville seuraavat arvot:

    - **Palkanlaskennan tilastoryhmä:** *VAC*
    - **Kuvaus:** *Lomasaldo*
    - **Siirrä:** *Ei*

1. Kun uusi rivi on vielä valittuna, valitse **Määritys** toimintoruudusta.
1. Valitse **Määritys**-sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon.
1. Määritä uuden rivin **Maksutyyppi**-kentän arvoksi *5151-1*.
1. Voit valita ja pitää **Kausikoodi**-kenttää painettuna (tai napsauttaa sitä hiiren kakkospainikkeella) ja valita sitten **Näytä tiedot**. Voit nyt määrittää kausikoodin, joka määritetään tähän kenttään myöhemmin.
1. Valitse **Kausityypit** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon.
1. Aseta uudelle riville seuraavat arvot:

    - **Kausityypit:** *VacYear*
    - **Kuvaus:** *Lomavuosi*
    - **Tiheys:** *Vuodet*

1. Kun uusi rivi on vielä valittuna, valitse **Luo kaudet** toimintoruudusta.
1. Määritä **Luo kaudet** -valintaikkunassa seuraavat arvot:

    - **Määritä kauden aloituspäivämäärä:** *1.9.2021*
    - **Kauden pituus:** *5*

1. Valitse **OK**.
1. Palaa **Palkanlaskennan tilastoryhmät** -sivulle sulkemalla **Kausityypit**-sivu.
1. Määritä **Kausikoodi**-kenttään luomasi kausityyppi (*VacYear*).

## <a name="create-a-statistical-balance-setup"></a>Luo tilastosaldon asetukset

Tässä osassa luodaan *tilastosaldoasetukset*, jotka on linkitetty edellisessä osiossa luotuun palkanlaskennan tilastoryhmään. Nämä tilastosaldoasetukset linkitetään myöhemmin tuotannon käyttöliittymän **Päivän tehtävät** -näkymään. Tämä **Päivän tehtävät** -näkymä voi näyttää siihen liittyvään palkanlaskennan tilastoryhmään määritetyn maksulajin lomasaldot.

1. Siirry kohtaan **Työajan seuranta \> Asetukset \> Palkanlaskenta \> Tilastosaldon asetukset**
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.
1. Aseta uudelle riville seuraavat arvot:

    - **Palkanlaskennan tilastoryhmä:** *VAC*
    - **Ulkoinen nimi:** *Lomasaldo*
    - **Liukuma:** *Ei*

## <a name="create-a-manual-premium"></a>Manuaalisten lisien luominen

*Manuaaliset lisät* myönnetään työntekijöille tavallisesti ylimääräisenä maksuna lisätyöstä. Tässä skenaariossa luot manuaalisen lisän, jonka avulla voit määrittää kunkin työntekijän alkuperäisen lomasaldon.

1. Siirry kohtaan **Työajan seuranta \> Asetukset \> Palkanlaskenta \> Manuaaliset lisät**
1. Lisää tietue valitsemalla toimintoruudussa **Uusi**.
1. Aseta uudelle tietueelle seuraavat arvot:

    - **Lisät:** *VAC*
    - **Kuvaus:** *Työntekijöiden lomasaldojen oikaisut*
    - **Maksutyyppi:** *5151-1*

## <a name="set-a-workers-initial-vacation-balance-and-adjust-it-by-one-day"></a>Työntekijän alkuperäisen lomasaldon asettaminen ja sen oikaiseminen yhdellä päivällä

Palkanlaskennan järjestelmänvalvojat tarkistavat ja hyväksyvät työntekijöiden päivittäiset rekisteröinnit **Hyväksy**-sivun avulla. Tässä skenaariossa otat järjestelmänvalvojan roolin, jotta voit määrittää työntekijän alkuperäisen lomasaldon ja rekisteröidä työntekijän ottamat lomapäivät.

1. Valitse **Työajan seuranta \> Tarkista ja hyväksy \> Hyväksy**.
1. Määritä seuraavat kentät **Hyväksy**-valintaruudussa:

    - **Hyväksyntäryhmä** – Valitse hyväksyntäryhmä, johon kuulut. (Jos käytät USMF-näytetietoja, käytettävissä on vain yksi hyväksyntäryhmä, *AdmMan*.)
    - **Tarkastele koko ryhmää, 1 päivä** – Valitse vaihtoehto ja määritä kentän arvoksi nykyinen päivämäärä.

1. Valitse **OK**.
1. **Hyväksy**-sivulla näkyy luettelo tietueista, jotka vastaavat ehtojasi. Valitse työntekijä, jonka haluat hyväksyä. Jos käytät USMF-vakionäytetietoja, valitse työntekijä *000496* (*Christina Portra*).
1. Myönnä valitulle työntekijälle 10 vuorokautta lomaa:

    1. Kun työntekijä on vielä valittuna, valitse **Lisän rivit** toimintoruudusta.
    1. Valitse **Lisän rivit** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon.
    1. Aseta uudelle riville seuraavat arvot:

        - **Lisät:** *VAC*
        - **Määrä** *10*

    1. Sulje **Lisän rivit** -sivu.

1. Kirjaa **Hyväksy**-sivulla se, että työntekijä on käyttänyt yhden lomapäivän kuluvana päivänä:

    1. Kun työntekijä on vielä valittuna, lisää rivi ruudukkoon valitsemalla sivun alaosan **Yhteenveto**-välilehdestä **Uusi**.
    1. Aseta uudelle riville seuraavat arvot:

        - **Kirjauskansion rekisteröintityyppi:** *Poissaolo*
        - **Viite:** *Loma*

    1. Ota lomasaldo käyttöön ja laske vähennys valitsemalla sivun yläosassa työkaluriviltä **Siirto**.

## <a name="configure-the-production-floor-execution-interface-so-that-it-includes-the-my-day-dialog-box"></a>Konfiguroi tuotannon käyttöliittymä niin, että se sisältää Päivän tehtävät -valintaikkunan

Tässä osassa lisäät **Päivän tehtävät** -painikkeen tuotannon käyttöliittymään. Tämän painikkeen avulla työntekijät voivat avata **Päivän tehtävät** -valintaikkunan.

1. Valitse **Tuotannonhallinta \> Asetukset \> Tuotannonohjaus \> Määritä tuotantoliittymä**.
1. Valitse konfiguraatio, esim. *Oletus*.
1. Valitse toimintoruudussa **Suunnitteluvälilehdet**.
1. Valitse **Suunnitteluvälilehdet**-sivun luetteloruudusta *Kaikki työt*, jos haluat tarkastella välilehden asetuksia. **Päänäkymä**-kentässä pitäisi nyt näkyä arvo *Kaikki työt*.
1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse **Toissijainen työkalurivi** -pikavälilehden **Käytettävissä olevat toimenpiteet** -sarakkeesta **Päivän tehtävät**. Siirrä se **Valitut toiminnot** -sarakkeeseen valitsemalla oikea nuolipainike.

## <a name="check-your-balance-in-the-production-floor-execution-interface"></a>Tarkista saldo tuotannon käyttöliittymässä

Tässä osassa kirjaudut sisään tuotannon käyttöliittymään työntekijänä, jonka loma-ajan olet määrittänyt aiemmin. Tämän jälkeen voit tarkastella lomasaldoasi avaamalla **Päivän tehtävät** -valintaikkunan.

1. Valitse **Tuotannonhallinta \> Määritys \> Tuotannonohjaus \> Tuotantoliittymä**.
1. Jos järjestelmä pyytää valitsemaan konfiguraation, valitse aiemmin tässä skenaariossa määritetty konfiguraatio (*Oletus*).
1. Kirjaudu sisään tässä skenaariossa aiemmin määrittämänäsi käyttäjänä. Jos käytät USMF-vakionäytetietoja, voit kirjautua sisään kirjoittamalla **Nimilapputunnus**-kenttään arvon *123*. Tämä nimilapun tunnus vastaa työntekijää Christina Portra.
1. Valitse vasemmassa työkalurivissä **Päivän tehtävät**.
1. Tarkista valintaikkunan **Saldot**-osa. Tässä osassa pitäisi nyt näkyä, että saldosi on yhdeksän lomapäivää.
