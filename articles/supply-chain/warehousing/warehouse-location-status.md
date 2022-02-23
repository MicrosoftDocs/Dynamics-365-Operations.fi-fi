---
title: Varastosijainnin tila
description: Tässä aiheessa on yleiskatsaus fyysisen varaston sijainnin tila -ominaisuudesta.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 31216c24f54f22ec928eb143d4a913aabcd50cf8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4427454"
---
# <a name="warehouse-location-status"></a>Varastosijainnin tila

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management sisältää useita sijaintikenttiä, jotka antavat sinulle joustavuutta, kun käsittelet sijainteja ja ylläpidät niitä. Sijaintidirektiivikyselyn avulla voit parantaa varastotyönkulun hallintaa.

Seuraavat neljä **Toimipaikat**-sivulla olevaa kenttää ovat sijainnin nykyisen tilan tietoja. Näiden kenttien avulla varaston valvojat saavat yleiskuvan varaston sijaintien tilasta. Ne mahdollistavat myös kehittyneet raportointi- ja suodatusasetukset.

- **Nimiketunnus** – Nimike, joka on tällä hetkellä sijainnissa. Jos sijainnissa on useita nimikkeitä, tämä kenttä on tyhjä.
- **Viimeinen tehtävän päivämäärä ja kellonaika** – Viimeistä varastopaikkaa vasten suoritetun fyysisen varastoinnin tapahtuman aikaleima.
- **Erääntymispäivämäärä** – Päivämäärä, jolloin varastosijainti tuotiin varastoon. Tämä arvo lasketaan rekisterikilven erääntymispäivämäärän perusteella. Se on tarkka sellaisissa sijainneissa, joissa on rekisterikilpiseuranta, mutta se ei ehkä ole tarkka sellaisissa sijainneissa, jotka eivät ole rekisterikilpiseurannassa.
- **Sijainnin tila** – Sijainnin tila. Mahdollisia arvoja on neljä:

    - **Määrittelemätön** – Sijaintiprofiili ei voi jäljittää tilaa. Näin ollen nykyistä tilaa ei tunneta.
    - **Tyhjä** – Sijainnissa ei ole varastoa.
    - **Poiminta** – Lähtevät tapahtumat on suoritettu sijainnille, koska se oli viimeksi tyhjä.
    - **Varasto** – Vain saapuvat tapahtumat on suoritettu sijainnille, koska sijainti oli viimeksi tyhjä.

## <a name="turn-on-the-warehouse-location-status-feature"></a>Varaston tilatoiminnon käyttöönotto

Ennen kuin voit käyttää *Varaston sijainnin tila* -toimintoa, sen pitää olla otettu käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Varaston tilatoiminnon käyttöönotto*

## <a name="set-up-warehouse-location-status"></a>Määritä varastosijainnin tila

### <a name="prepare-the-sample-data-that-is-required-for-the-example-scenario"></a>Esimerkkiskenaarion mukaisten mallitietojen valmisteleminen

Ennen kuin aloitat skenaarion käsittelyn, sinun on aktivoitava mallitiedot ja määritettävä ominaisuus tässä osassa kuvatulla tavalla. Esimerkkiskenaarion suorittaminen edellyttää, että käytössä on joko varastosovellus tai selainpohjainen emulaattori. Tässä annetut vaiheet käyttävät varastosovellusta. Selainpohjaisen emulaattorin vaiheet ovat samankaltaisia.

#### <a name="use-the-usmf-legal-entity"></a>Käytä USFM-yritystä

Esimerkkiskenaarion käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.

#### <a name="set-up-location-profiles"></a>Määritä sijaintiprofiilit

Esimerkkiskenaario edellyttää kahden sijaintiprofiilin valmistelemista.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit**.
1. Valitse **Muokkaa**, jotta saat sivun muokkaustilaan.
1. Valitse **BULKKI-06**-profiili.
1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Ota nimike sijainnissa käyttöön:** Määritä tähän arvoksi _Kyllä_.
    - **Ota käyttöön sijaintitehtävän päivämäärä ja aika:** Määritä asetukseksi _Kyllä_.
    - **Ota sijainnin tila käyttöön:** Määritä tähän arvoksi _Kyllä_.

    Nämä asetukset määrittävät, ovatko sijainnin viitekentät aktiivisia.

1. Toista vaiheet 3-4 **POIMINTA-06**-profiilissa.

> [!NOTE]
> Kun sijaintiprofiilin (**Ota nimike käyttöön sijainnissa**, **Ota käyttöön sijaintitehtävä**, **Ota käyttöön sijainnin tila**) parametrien arvoksi on määritetty *Kyllä*, järjestelmä päivittää heti vastaavat sijainnit suorittamalla *Varastosijainnin tilan yhdenmukaisuustarkistus* -työn.

### <a name="scenario"></a>Skenaario

1. Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Valitse **Uusi**.
1. Valitse **Luo ostotilaus** -valintaikkunan **Toimittaja**-pikavälilehden **Toimittajatili**-kentässä *104*.
1. Valitse **Yleinen**-pikavälilehden **Varasto**-kentässä *61*.
1. Valitse **OK**.
1. Uusi ostotilaus (PO) avataan. **Ostotilausrivit**-ruudukko sisältää tyhjän rivin. Määritä tälle riville seuraavat arvot:

    - **Nimiketunnus:** _A0002_
    - **Määrä** _5_

1. Valitse Toimintoruudussa **Osto**-välilehdellä **Toiminnot**-ryhmässä **Vahvista** vahvistaaksesi ostotilauksen.
1. Siirry mobiililaitteen **Saapuva \> Oston vastaanotto** -kohtaan.
1. Valitse **PONUM**-kenttä ja syötä ostotilauksen numero ja vahvista.
1. Valitse **NIMIKE**-kenttä ja syötä nimikkeen numeroksi *A0002* ja vahvista.
1. Määritä **MÄÄRÄ**-sivulla määräksi *5* ja vahvista.

    Voit syöttää määrän jommallakummalla seuraavista tavoista:

    - Lisää tai vähennä numeerinen arvo valitsemalla plusmerkki (**+**) tai miinusmerkki (**–**).
    - Avaa numeronäppäimistö valitsemalla plusmerkki- (**+**) ja miinusmerkki (**–**) -painikkeiden välissä oleva tyhjä kenttä.

1. Vahvista nimiketunnuksen *A0002* ja määrän *5* valinta. Sivun alaosaan tulee T valmiina-sanoma.
1. Valitse oikeasta yläkulmasta valikkopainike (jota kutsutaan myös hampurilaiseksi tai hampurilaispainikkeeksi) ja poistu **Oston vastaanotto**- valikosta palaamalla valitsemalla **Peruuta** ja palaa **Saapuva**-valikkoon.
1. Valitse ostotilaus-sivulta **Työn tiedot** **Ostotilauksen rivit** -ruudukon yläpuolella.
1. Huomaa **Yleiset**-välilehdessä luodut **Työtunnuksen** ja **Kohderekisterikilven tunnus** -arvot.
1. Huomaa *Poiminta*- ja *Hyllytys*-työtyyppien **Sijainti**-arvot **Rivit**-osassa.
1. Siirry mobiililaitteen **Saapuva \> Oston hyllytys** -kohtaan.
1. Valitse **TUNNUS**-kenttä, syötä työtunnus ja vahvista.
1. Vahvista *Poiminta*-merkinnän suorittaminen vielä kerran.
1. Valitse valikkopainike oikeassa yläkulmassa ja valitse sitten **Valmis** lopettaaksesi *Poiminta*-työn.
1. Tee merkintä hyllytyssijainnista ja vahvista. Sivun alaosaan tulee T valmiina-sanoma.
1. Valitse oikeassa yläkulmassa oleva valikkopainike ja poistu **Oston hyllytyksestä** ja palaa **Saapuvat**-valikkoon valitsemalla **Peruuta**.
1. Palaa päävalikkoon valitsemalla **Takaisin**.
1. Mene Dynamics 365 Supply Chain Managementissa kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijainnit**.
1. Suodata **Sijainnin** mukaan ja syötä hyllytyksen sijainti ostotilauksen työstä. Sinun pitäisi nähdä seuraavat tulokset:

    - **Sijainnin tila** -sarakkeessa näkyy *Varaston* arvo , koska viimeinen tätä sijaintia vastaan tehty tapahtuma oli hyllytys.
    - **Nimiketunnus**-sarakkeessa näkyy arvo *A0002*, koska nimike vastaanotettiin ja siirrettiin sijaintiin.
    - **Viimeinen tehtävän päivämäärä ja aika** -sarakkeessa näkyy aikaleima päivämäärän ja kellonajan osalta, jolloin työ on saatu valmiiksi sijainnissa.

1. Siirry mobiililaitteessa kohtaan **Laatu \> Siirto**.
1. Valitse **SIJ/RK**-kenttä ja kirjoita edellisten vaiheiden sijainti, johon teit huomautuksen.
1. Vahvista näytettävät tiedot. Kirjoita muistiin luotava rekisterinumero.
1. Valitse **Tiedot**-näytössä **SIJ/RK**-kenttä ja syötä *06A07R2S1B* sijainniksi, johon nimike siirretään.
1. Vahvista **Tiedot**-näytössä **RK**-arvo (kohderekisterikilpitunnus), joka luodaan automaattisesti. Sivun alaosaan tulee T valmiina-sanoma.
1. Valitse oikeassa yläkulmassa oleva valikkopainike ja valitse **Siirto** ja palaa **Laadunhallinta**-valikkoon valitsemalla **Peruuta**.
1. Palaa päävalikkoon valitsemalla **Takaisin**.
1. Mene Dynamics 365 Supply Chain Managementissa kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijainnit**.
1. Päivitä **Sijainnit**-sivu ja näytä alkuperäinen hyllytyspaikka uudelleen. Huomaa, että **Sijainnin tila** -kentän arvo on nyt *Tyhjä* ja **Nimiketunnus**-sarake on tyhjä.
1. Näytä sijaintitietue kohteelle *06A07R2S1B* ja huomaa, että **Tila**-arvo on muuttunut *Varastoksi* ja että **Nimiketunnus** sekä **Viimeinen tehtävän päivämäärä- ja aika** -kentät on päivitetty.
1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse **Uusi**.
1. Valitse **Luo myyntitilaus** -valintaikkunan **Asiakastili**-kentässä *US-002*.
1. Valitse **Varasto**-kentässä *61*.
1. Valitse **OK**.
1. Uusi myyntitilauksesi avataan. **Myyntitilausrivit**-ruudukko sisältää tyhjän rivin. Määritä tälle riville seuraavat arvot:

    - **Nimiketunnus:** _A0002_
    - **Määrä** _1_

1. Valitse **Myyntitilausrivit**-pikavälilehdellä **Varasto**-valikosta **Varaus**.
1. Valitse **Varaus**-sivulla **Varaa erä** voidaksesi varata tilausrivin. Valitse sitten **Sulje**-painike (**X**) oikeassa yläkulmassa sulkeaksesi sivun.
1. Valitse toimintoruudussa **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.
1. Valitse **Myyntitilausrivit**-osassa **Varasto**-valikosta **Työn tiedot**.
1. Kopioi luotu **Työtunnuksen** arvo.
1. Siirry mobiililaitteen kohtaan **Lähtevä \> Myyntikeräily**.
1. Valitse **TUNNUS**-kenttä, syötä työtunnus, jonka kopioit aiemmin ja vahvista.
1. **Myyntitilaukset: Poiminta**-sivulla **SIJ**-kenttä ehdottaa keräilysijaintia aiemmin luodussa hyllytyssijainnissa. Kirjoita sijainti muistiin.
1. Valitse **SIJ**-kenttä, syötä sijainti ja vahvista.
1. Valitse **RK**-kenttä, anna rekisterinumero, josta olet tehnyt muistiinpanon siirron aikana, ja vahvista.
1. Valitse **Nimike**-kenttä ja syötä nimikkeen numeroksi *A0002* ja vahvista.
1. Määritä **MÄÄRÄ**-sivulla määräksi *1* ja vahvista.

    Voit syöttää määrän jommallakummalla seuraavista tavoista:

    - Lisää tai vähennä numeerinen arvo valitsemalla plusmerkki (**+**) tai miinusmerkki (**–**).
    - Avaa numeronäppäimistö valitsemalla plusmerkki- (**+**) ja miinusmerkki (**–**) -painikkeiden välissä oleva tyhjä kenttä.

1. Valitse **KOHDE-RK**-kenttä, kirjoita käyttäjän määrittämä kohderekisterikilpitunnus ja vahvista.
1. Vahvista poimintatyön suorittaminen vielä kerran. Sivun alaosaan tulee T valmiina-sanoma.
1. Valitse oikeassa yläkulmassa oleva valikkopainike ja valitse **Peruuta** lopettaaksesi poimintatyön ja palaa **Lähtevä**-valikkoon.
1. Mene Dynamics 365 Supply Chain Managementissa kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijainnit**.
1. Suodata **Sijainnin** mukaan ja syötä poiminnan sijainti myyntitilauksen työstä.
1. Huomaa, että **Sijainnin tila** -kentän, josta myyntitilaustyö poimi arvoksi on nyt määritetty *poiminta* ja **viimeinen tehtävän päivämäärä ja aika** -kenttä on päivitetty.

> [!NOTE]
> Sijaintikentät päivitetään vain varastotapahtumien mukaan. Jos varasto siirretään kirjauskansion tai muiden kuin WHS-prosessien avulla, kenttiä ei päivitetä.
