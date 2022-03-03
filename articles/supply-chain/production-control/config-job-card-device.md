---
title: Konfiguroi työkortti laitteita varten
description: Tässä ohjeaiheessa kuvataan työkorttilaitteen konfiguroinnissa käytettävissä olevat eri asetukset.
author: johanhoffmann
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch, JmgRegistrationTouchUserConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 4c7a9585d96a1e08790e0f3c972e704971f27dc0
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103435"
---
# <a name="configure-job-card-for-devices"></a>Konfiguroi työkortti laitteita varten

[!include [banner](../includes/banner.md)]

Työntekijät käyttävät työkorttilaitetta rekisteröimään päivittäisen työnsä, esimerkiksi töiden aloittamisen, töiden palautteen ilmoittamisen, epäsuorien tehtävien rekisteröimisen ja poissaolon raportoinnin. Nämä rekisteröinnit ovat perusta, jolla seurataan tuotantotilausten edistymistä ja kustannuksia sekä lasketaan työntekijöiden palkan perusta. Tässä ohjeaiheessa kuvataan työkorttilaitteiden konfiguroinnissa käytettävissä olevat eri asetukset.

## <a name="enable-new-features-in-feature-management"></a>Ominaisuuksien hallinnan uusien ominaisuuksien ottaminen käyttöön

Jotkin tässä ohjeaiheessa kuvatut asetukset on otettava käyttöön järjestelmässä, ennen kuin ne ovat käytettävissäsi. Käytä [ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -sivua, kun haluat ottaa käyttöön jotkin tai kaikki seuraavat ominaisuudet tarpeen mukaan.

### <a name="generate-license-plate"></a>Muodosta rekisterikilpi

Jos haluat käyttää tätä toimintoa, ota seuraavat ominaisuudet käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (järjestyksessä):

1. *Rekisterikilpi valmiiksi raportointia varten on lisätty työkorttilaitteeseen*<br>(Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on oletusarvoisesti käytössä. Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on pakollinen.)
1. *Ota käyttöön rekisterikilven numeron automaattinen luonti, kun työkorttilaitteessa raportoidaan valmiiksi*<br>(Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on pakollinen.)

### <a name="print-label"></a>Tulosta etiketti

Jos haluat käyttää tätä toimintoa, ota seuraavat ominaisuudet käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (järjestyksessä):

1. *Rekisterikilpi valmiiksi raportointia varten on lisätty työkorttilaitteeseen*<br>(Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on oletusarvoisesti käytössä. Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on pakollinen.)
1. *Tulosta etiketti työkorttilaitteesta*<br>(Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on pakollinen.)

### <a name="allow-locking-of-touch-screen"></a>Salli kosketusnäytön lukitseminen

Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä. Supply Chain Managementin versiosta 10.0.25 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä. Jos käytät vanhempaa versiota kuin 10.0.25, järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Toiminto, jolla voi lukita työkorttilaitteen ja työkorttipäätteen desinfiointia varten* -toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilasta.

## <a name="manage-your-device-configurations"></a>Laitteesi konfiguraatioiden hallinta

Määrittääksesi laitteesi konfiguraation valitse **Tuotannonhallinta > Asetukset > Tuotannonohjaus > Konfiguroi työkortti laitteita varten**. Näyttöön tulee **Konfiguroi työkortti laitteille** -sivu, jossa näkyy aiemmin luotujen konfiguraatioiden luettelo. Tämän jälkeen voit toimia seuraavasti: 

- Valitse kaikki vasemmassa sarakkeessa luetellut laitemääritykset, jos haluat tarkastella ja muokata niitä.
- Valitse toimintoruudusta **Uusi**, kun haluat lisätä luetteloon uuden laitekonfiguraation. Määritä sen jälkeen **Konfigurointi**-kenttään nimi, jonka avulla uusi konfigurointi on helppo tunnistaa. Tässä syötettävän arvon on oltava yksilöivä kaikkien laitekokoonpanojen joukossa, etkä voi muokata sitä myöhemmin.

Seuraavissa osissa on lisätietoja kustakin työkorttilaitteiden konfigurointiasetuksista.

## <a name="general-settings"></a>Yleiset asetukset

**Yleinen**-pikavälilehdessä voit määrittää kaikki valitun laitekokoonpanon käytettävissä olevat asetukset. Seuraavat asetukset ovat käytettävissä:

- **Ilmoita määrä uloskuittauksessa** - Määritä arvoksi **Kyllä**, jos haluat, että työntekijöitä kehotetaan raportoimaan meneillään olevien töiden palautteen. Kun asetus on **Ei**, työntekijöitä ei kehoteta.
- **Lukitse työntekijä** - Kun tämä asetus on **Ei**, kukin työntekijä kirjataan ulos heti, kun hän on tehnyt rekisteröitymisen (esimerkiksi uusi työ), ja laite palaa kirjautumissivulle. Kun tämän asetuksen arvoksi on määritetty **Kyllä**, kukin työntekijä pysyy kirjautuneena työkorttilaitteeseen. Työntekijä voi kuitenkin kirjautua ulos manuaalisesti, jotta toinen työntekijä voi kirjautua sisään, kun työkorttilaite pysyy käynnissä saman järjestelmän käyttäjätilillä. Lisätietoja tämän tyyppisistä tileistä on kohdassa [Määritetyt käyttäjät](#assigned-users).
- **Viivakoodinlukija** – Määritä arvoksi **Kyllä**, jos haluat antaa työkorttilaitteelle vaihtoehdon, jonka avulla työntekijät voivat rekisteröidä uuden työn lukemalla viivakoodin.
- **Käytä todellista kirjaamisaikaa** - Määritä arvoksi **Kyllä**, jos haluat määrittää, että kukin uusi kirjaus vastaa tarkkaa aikaa, jolloin työntekijä on lähettänyt rekisteröitymisen. Määritä arvoksi **Ei**, jos haluat käyttää kirjautumisaikaa. Haluat yleensä määrittää tämän arvoksi **Kyllä**, jos olet ottanut käyttöön **Lukitse työntekijä**- ja/tai **Yksittäinen työntekijä** -asetukset, joissa työntekijät pysyvät usein kirjautuneina pitkiä aikoja.
- **Yksittäinen työntekijä** - Määritä tämän vaihtoehdon arvoksi **Kyllä**, jos vain yksi työntekijä käyttää kutakin työkorttilaitetta, jossa tämä konfiguraatio on aktiivinen. Kun tämä vaihtoehto on valittuna, **Lukitse työntekijä** -asetukseksi määritetään automaattisesti **Kyllä**. Lisäksi tämä vaihtoehto poistaa vaatimuksen (ja mahdollisuuden), jonka mukaan työntekijä kirjautuu sisään käyttämällä nimilapun tunnusta (tai vastaavaa). Sen sijaan työntekijä kirjautuu sisään Supply Chain Managementiin käyttäen järjestelmän käyttäjätiliä, joka on linkitetty *aikarekisteröityyn työntekijään* ( *työntekijät*-taulukosta), ja saa kirjautua työkorttilaitteeseen samaan aikaan.  Lisätietoja tämän tyyppisistä tileistä on kohdassa [Määritetyt käyttäjät](#assigned-users).
- **Salli työntekijöiden määrittää henkilökohtaiset suodattimet** - Määritä tämän asetuksen arvoksi **Kyllä**, jotta työntekijät voivat suodattaa heille näkyvät työt laitteessa. Työntekijä voi muokata kaikkien kolmen suodatusehdon arvoja: **Tuotantoyksikkö**, **Resurssiryhmä** ja **Resurssi**. Laitteessa näkyvät vain työt, jotka on ajoitettu valittujen suodatusehtojen mukaisiin resursseihin. Voit myös määrittää oletusarvot mille tahansa tai kaikille näistä kriteereistä, ja niitä käytetään, vaikka tämä vaihtoehto ei olisi valittuna.
- **Salli kosketusnäytön lukitseminen** – Määritä tämän asetuksen arvoksi **Kyllä**, jos työntekijät voivat lukita työkorttilaitteen kosketusnäytön, jotta he voivat puhdistaa sen. Kun tämä asetus on käytössä, laitteen kirjautumissivulle tulee näkyviin **Lukitse näyttö puhdistusta varten** -painike. Kun työntekijä valitsee tämän painikkeen, kosketusnäyttö lukittuu tilapäisesti tahattoman syötön estämiseksi ja ajastin näytetään. Työntekijä voi nyt turvallisesti puhdistaa laitteen ja näytön. Kun ajastin on valmis, kosketusnäyttö aukeaa uudelleen automaattisesti.
- **Näytön lukituksen kesto** – Kun **Salli kosketusnäytön lukitus** on käytössä, käytä tätä vaihtoehtoa, jotta voit määrittää, kuinka monta sekuntia kosketusnäyttö on lukittu desinfiointia varten. Keston on oltava 5 – 120 sekunnin välillä.
- **Tuotantoyksikkö** - Valitse tuotantoyksikkö, jota käytetään kullekin työntekijälle näytettävän luettelon oletussuodatusehtona. Laite näyttää aluksi vain valittuun tuotantoyksikköön ryhmitetyillä resursseilla ajoitetut työt. Jos **Salli työntekijöiden määrittää henkilökohtaiset suodattimet** on käytössä, työntekijät voivat muokata tätä arvoa. Muuten tätä suodatinta käytetään aina, kun tämä laitekonfiguraatio on aktiivinen.
- **Resurssiryhmä** - Valitse resurssiryhmä, jota käytetään kullekin työntekijälle näytettävän luettelon oletussuodatusehtona. Laite näyttää aluksi vain valittuun resurssiryhmään ryhmitetyillä resursseilla ajoitetut työt. Jos **Salli työntekijöiden määrittää henkilökohtaiset suodattimet** on käytössä, työntekijät voivat muokata tätä arvoa. Muuten tätä suodatinta käytetään aina, kun tämä laitekonfiguraatio on aktiivinen.
- **Resurssi** - Valitse resurssi, jota käytetään kullekin työntekijälle näytettävän luettelon oletussuodatusehtona. Laite näyttää aluksi vain valittuun resurssiin ajoitetut työt. Jos **Salli työntekijöiden määrittää henkilökohtaiset suodattimet** on käytössä, työntekijät voivat muokata tätä arvoa. Muuten tätä suodatinta käytetään aina, kun tämä laitekonfiguraatio on aktiivinen.
- **Luo rekisterikilpi** – Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat luoda uuden rekisterikilven aina, kun työntekijä käyttää työkorttilaitetta ilmoittaakseen olevansa valmis. Rekisterikilpinumero muodostetaan **Varastonhallinnan parametrit** -sivulla määritetystä numerosarjasta. Kun asetus on **Ei**, työntekijöiden on määritettävä aiemmin määritetty rekisterikilpi, kun ilmoittavat työn valmistumisesta.
- **Tulosta etiketti** - Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat tulostaa käyttöoikeuskilven otsikon, kun työntekijä käyttää työkorttilaitetta valmiiksi raportoidessaan. Etiketin konfiguraatio määritetään tiedoston reitityksessä, kuten on kuvattu kohteessa [Rekisterimerkintöjen asiakirjan reititysasettelu](../warehousing/document-routing-layout-for-license-plates.md).

<a name="assigned-users"></a>

## <a name="assigned-users"></a>Määritetyt käyttäjät

**Määritetyt käyttäjät** -pikavälilehdessä voit liittää vähintään yhden järjestelmän käyttäjät nykyiseen laitekokoonpanoon. Kullekin järjestelmän käyttäjälle voidaan määrittää vain yksi työlaitekonfiguraatio.

Kun laite määritetään, IT-työntekijä kirjautuu yleensä Supply Chain Managementiin käyttämällä järjestelmän käyttäjätiliä. Tämän jälkeen kyseiseen järjestelmäkäyttäjään liittyvä työlaitteen konfigurointi on voimassa niin kauan kuin järjestelmäkäyttäjä on kirjautuneena sisään. Nämä järjestelmäkäyttäjä tilit rajoittuvat yleensä vain työkorttilaitesivulle, eikä mikään muu osa Supply Chain Managementia ole sallittua.

Kun järjestelmän käyttäjä on kirjautunut sisään ja työlaitteen määritykset on ladattu, työntekijät voivat kirjautua työkorttilaitteeseen käyttämällä *aikarekisteröitynyt työntekijä* -tiliään (esimerkiksi lukemalla viivakoodin kortissa), jotta he voivat aloittaa uusia töitä ja tehdä muunlaisia kirjauksia. Useat työntekijät voivat kirjautua sisään ja ulos päivän aikana, samalla kun sama laitekokoonpano pysyy voimassa kyseisessä koneessa, koska järjestelmäkäyttäjä pysyy kirjautuneena Supply Chain Managementiin koko päivän.

Kuten aiemmin mainittiin, kun käytät laitekonfiguraatiota yhdessä **Yksi työntekijä** -asetuksen kanssa, työntekijät voivat itse yleensä kirjautua Supply Chain Managementiin käyttämällä käyttäjän omaan *aikarekisteröitynyt työntekijä* - tiliin linkitettyä järjestelmäkäyttäjää , jotta he voivat ladata laitteen kokoonpanon ja kirjautua työkorttilaitteen työntekijänä samaan aikaan.

## <a name="additional-resources"></a>Lisäresurssit

[Ilmoita valmiiksi työkorttilaitteesta](report-finished-job-device.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]