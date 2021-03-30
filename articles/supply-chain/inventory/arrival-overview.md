---
title: Saapumisten yhteenveto
description: Tässä aiheessa on tietoja Saapumisen yleiskuva -ominaisuudesta. Saapumisen yleiskuva -sivu on osa tätä ominaisuutta ja se tarjoaa yhteenvedon kaikista saapuvista nimikkeistä, joita odotetaan.
author: perlynne
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 2bc0cfc3c4689953c867109da4e414d4291515f9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219410"
---
# <a name="arrival-overview"></a>Saapumisten yhteenveto

[!include [banner](../includes/banner.md)]

Tässä aiheessa on tietoja Saapumisen yleiskuva -ominaisuudesta. Saapumisen yleiskuva -sivu on osa tätä ominaisuutta ja se tarjoaa yhteenvedon kaikista saapuvista nimikkeistä, joita odotetaan.

**Saapumisen yleiskuva** -sivulla on yhteenveto kaikista saapumista odottavista nimikkeistä. Siinä näytetään myös saapumiset, jotka voidaan alustaa yhteenvedon perusteella. Tässä ohjeaiheessa keskitytään vastaanottoprosessiin.

## <a name="business-scenario"></a>Yrityksen skenaario
Seuraavana on esimerkki saapuvien prosessista.

[![Yrityksen skenaario](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png)

Sammy, vastaanottoassistentti, haluaa tietää, mitä odotetaan saapuvan tänä päivänä. Hän näkee **Saapumisen yleiskuva** -sivulla tiedot nykyisistä tehtävistä ja karkean arvion määristä, tilavuudesta, painosta, tilaustyypeistä ja niin edelleen. Toimitus saapuu myöhemmin saapuvien laiturille ja Sammy vastaanottaa toimitusluettelon. Sammy voi suorittaa **Saapumisen yleiskuva** -sivulla seuraavat tehtävät:

-   Tunnista vastaava vastaanottotilaus ja rekisteröi vastaanotto **käsittelyyn**. Rekisteröintiä varten tarvittavat rivit luodaan automaattisesti ja vastaanottoa voidaan seurata, vaikka tapahtumia ei ole vielä kirjattu **rekisteröidyksi**.
-   Avaa asiaankuuluva saapumisen kirjauskansioviite (eli **Nimikkeen saapumisen** tai **Tuotannon varastoinnin** kirjauskansio) ja tunnista kirjauskansiot, jotka ovat valmiina tuotteen vastaanottopäivitykseen.

## <a name="arrival-overview-page"></a>Saapumisen yleiskuva -sivu
**Saapumisen yleiskuva** -sivu aukeaa valitsemalla **Varastonhallinta** &gt; **Saapuvat tilaukset** &gt; **Saapuneiden yhteenveto**. Voit tarkastella luetteloa saapuvaksi odotetuista tilauksista. Yhteenveto on jaettu otsikoihin ja riveihin. Otsikon tiedot on ryhmitelty tilaustyypin, odotetun saapumispäivämäärän ja toimituskohteen mukaan. Kun otsikkorivi valitaan saapuvaksi, kaikki vastaanoton viitteeseen liittyvät tietorivit valitaan saapuvaksi sivun rivitieto-osassa. Kun kaikki liittyvät kirjauskansiorivit on kirjattu, näitä tietoja ei näytetä.

### <a name="arrival-overview-profiles"></a>Saapumisen yleiskuvaprofiilit

**Saapumisen yleiskuva** -sivulla on yhteenveto nimikkeistä, joiden odotetaan saapuvan, sekä kyseisten nimikkeiden odotetut saapumispäivämäärät. Useita käyttäjäkohtaisten asetusten joukkoja voidaan käyttää osana saapumisten prosessia. Yksittäiset käyttäjät voivat määrittää henkilökohtaiset asetuksensa **Saapumisen yleiskuvaprofiilit** -sivulla.

### <a name="set-up-item-arrival"></a>Määritä nimikkeen saapuminen

Esimerkissä Sammy haluaa määrittää uuden tietokoneen sijainnissa, jota käytetään valmiiden tuotteiden vastaanottamiseen tuotannosta Toimipaikasta 1. Sammy luo **Saapumisen yleiskuvaprofiilit** -sivulla uuden määrityksen nimeltä **Toimipaikan 1 tuotanto** ja määrittää sille seuraavat asetukset.

1.  Syötä **Saapumisen asetukset** -välilehden **Alue**-kenttäryhmään tiedot päivämäärävälistä ja yhteenvetoon sisältyvistä varastoista.
2.  Syötä **Saapumisen asetukset** -välilehden **Kirjauskansio**-kenttäryhmään vastaanottava varasto, sijainti ja kirjauskansion nimi (nimikkeen saapuminen/tuotannon varastointi).
3.  Syötä **Saapumiskyselyn tiedot** -välilehden **Toimipaikka**-kenttäryhmän **Rajoita toimipaikkaan** -kenttään toimipaikka, johon yhteenvetoalueen näkymä rajoitetaan.
4.  Aseta **Saapumiskyselyn tiedot** -välilehdessä **Näkyvät tapahtumatyypit** -kenttäryhmän **Tuotantotilaukset**-asetukseksi **Kyllä**.
5.  Aseta **Saapumiskyselyn tiedot** -välilehden **Muut**-ryhmässä **Päivitä käynnistettäessä** -asetuksen arvoksi **Kyllä**, jos haluat, että näkymä päivitetään automaattisesti käynnistyksen yhteydessä. Aseta **Päivitä aluetta muutettaessa** -asetukseksi **Kyllä**, jos näkymä tulee päivittää automaattisesti, kun alueen arvot muuttuvat.

Tässä esimerkissä **Saapumisen yleiskuvaprofiilin nimi** -kentän arvoksi **Saapumisen yleiskuva** -sivun **Saapumisen asetukset** -pikavälilehdessä määritetään **Toimipaikan 1 tuotanto**.

### <a name="prerequisites-for-arrival-journals"></a>Saapumiskirjauskansioiden edellytykset

Jotta saapumisen kirjauskansiot luotaisiin automaattisesti **Saapumisen yleiskuva** -sivulta, sinun on määritettävä asianmukaiset tiedot **Kirjauskansio**-kenttäryhmään **Saapumisen asetukset** -välilehdellä.

-   Kirjauskansion nimi on määritettävä, jotta kansion voi luoda.

[![Kirjauskansion nimen määrittäminen](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)

-   Jos määrität arvon **Varasto**- ja **Sijainti**-kenttiin, arvoja käytetään kirjauskansion riveillä. Jos et määritä arvoja, järjestelmä käyttää varastotapahtumille määritetyn dimension arvoja.

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a>Vastaanottotilaukselta saadut, odotetut nimikkeet

Sammy valitsee **Vastaanotot**-välilehdeltä rivin ja napsauttaa **Aloita saapuminen** -painiketta. Kaikki liittyvät rivit, jotka sisältyvät määritettyyn alueeseen ja joilla on rekisteröitävä määrä valitaan automaattisesti. Järjestelmä luo nimikkeen saapumisen kirjauskansion, joka vastaa odotettua vastaanottoa ja kirjauskansiota. Määrä alustetaan automaattisesti kaikille luoduille riveille.

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a>Useammalta vastaanottotilaukselta saadut, odotetut nimikkeet

Sammy valitsee **Vastaanotot**-välilehdeltä monta riviä ja napsauttaa **Aloita saapuminen** -painiketta. Järjestelmä luo nimikkeen saapumisen kirjauskansion, joka vastaa kaikkia odotettuja vastaanottoja ja kirjauskansiota. Kaikki rivit luodaan yhdelle nimikkeen saapumisen kirjauskansion otsikolle ja määrä alustetaan automaattisesti.

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a>Nimikkeiden vastaanotto yhdestä tai useammasta odotetusta vastaanottotilauksesta

#### <a name="view-information"></a>Näytä tiedot

Sammy haluaa yhteenvedon odotetuista vastaanotoista tietyllä aikavälillä ja syöttää seuraavat tiedot **Saapumisen asetukset** -välilehdelle **Saapumisen yleiskuva** -sivulla ja päivittää sitten näkymän **Päivitä** -painikkeella:

-   Saapumisen yleiskuvaprofiilin nimi: **Kysely**
-   Näytä rivit: **Kaikki**
-   Päivää taaksepäin: (Tyhjä)
-   Päivää eteenpäin: **0**
-   Varastot: **GW, MW**

Hän voi tarkastella seuraavia tietoja:

-   Kaikki liittyvät vastaanottotilaukset järjestelmän päivämäärälle ja siitä taaksepäin (**InventTrans.StatusDate** -väli) ja vastaanotot varastoihin GW ja MW tilasta riippumatta.
-   Tarkat rivitiedot useammalle tilaukselle. Sammy voi valita usean otsikkorivin yhteenvedosta ja näyttää kaikkia valittuja tilauksia vastaavat rivitiedot napsauttamalla **Näytä kaikki valitut** -painiketta.
-   Tietyn ostotilauksen tiedot. Sammy haluaa nähdä yhteenvedossa vain tiettyyn viitenumeroon liittyvät tiedot, joten hän syöttää tilinumeron **Tilinumero**-kenttään ja tilausnumeron **Viitenumero**-kenttään.
-   Yhteenveto rekisteröintitehtävistä, jotka on tehtävä kaikille tilausriveille, joille on luotu nimikkeen saapumiskirjauskansio, jota ei ole kirjattu vielä. Sammy avaa nämä tiedot valitsemalla **Näytä rivit** -kentän arvoksi **Käsittelyssä**.

### <a name="update-journals"></a>Päivityskirjauskansiot

Rekisteröidäkseen yhden tai useamman prosessointia odottavan rivin, Sammy valitsee rivit yhteenvedon tai rivien ruudukossa ja sitten **Kirjauskansiot** &gt; **Näytä vastaanottojen saapumiset**. Järjestelmä näyttää nimikkeen saapumisotsikot, jotka vastaavat rivejä. Sammy avaa päivitysvalmiit nimikkeen saapumiskirjauskansion otsikot ja päivittää rekisteröityjen nimikkeiden ostotilausten vastaanoton. Hän avaa nämä nimikkeiden saapumiskirjauskansion otsikot napsauttamalla **Kirjauskansiot** &gt; **Tuotteen vastaanottoon valmiit kirjauskansiot**. Järjestelmä näyttää kaikki otsikkorivit, jotka ovat valmiita tuotteen vastaanoton päivittämiseen määritetyllä varastoalueella. (Näytettävät otsikkorivit eivät liity päivämääräväliin).

### <a name="start-an-arrival-registration"></a>Saapumisrekisteröinnin aloittaminen

Sammy voi aloittaa useamman vastaanottoviitteen saapumisen valitsemalla useamman rivin **Saapumisen yleiskuva** -sivulla. Kun hän valitsee rivin vastaanottojen yhteenvedosta, valitaan myös vastaavat rivitiedot. Jos rekisteröinnillä on määrä, **Aloita saapuminen** -painike on käytettävissä. Sammy voi aloittaa saapumisrekisteröinnin kahdella tavalla:

-   Voit suodattaa siten, että siinä näytetään vain tietueet, jotka täyttävät tietyt ehdot lukemalla esimerkiksi toimitusilmoituksen viivakoodissa olevan toimittajan viitenumeron **Toimittajan viite** -kenttään.
-   Voit valita saapuvaksi rekisteröitävät tietueet tai peruuttaa niiden valinnan **Saapumisen yleiskuva** -sivun yhteenveto- tai lisätieto-osassa. Kun Sammy tämän jälkeen napsauttaa **Aloita saapuminen** -painiketta, valitut tietueet luodaan automaattisesti nimikkeen saapumiskansioon. Tietueet sisältävät rivitiedot ja kaikki yksilölliset kenttätiedot määritetään.

## <a name="update-arrival-information-and-process-a-product-receipt"></a>Saapumistietojen päivittäminen ja tuotteen vastaanoton käsittely
Kun kaikki tavarat on rekisteröity, varastopäällikkö tai ostopäällikkö voi päivittää vastaanotetut nimikkeet tuotekuitilla fyysisten kustannusten lisäämiseksi. Seuraa näitä vaiheita, jos haluat päivittää saapumistiedot ja kirjata tuotteen vastaanoton.

1.  Valitse **Varastonhallinta** &gt; **Saapuvat tilaukset** &gt; **Saapumisen yleiskuva**.
2.  Napsauta **Saapumisen yleiskuva** -sivulla **Kirjauskansiot** &gt; **Tuotteen vastaanottoon valmiit kirjauskansiot** näyttääksesi luettelon tuotteen vastaanottopäivitykseen valmiista kirjauskansioista.
3.  Valitse päivitettävät kirjauskansiot ja napsauta sitten **Toiminnot** &gt; **Tuotteen vastaanotto**.
4.  Syötä tuotteen vastaanottonumero **Kirjaus**-sivulla, jos se ei ole jo saatavilla ja napsauta sitten **OK** käsitelläksesi tuotteen vastaanoton.

## <a name="summary"></a>Yhteenveto
**Saapumisen yleiskuva** -sivun avulla varastopäällikkö ja varastotyöntekijät voivat nähdä yleiskuvan odotettavissa olevasta työstä, joka on tehtävä saapuvien käsittelyn aikana. Sivun avulla voidaan myös aloittaa nimikkeiden saapumisprosessi, jotta nimikkeiden seuranta voidaan aloittaa heti, kun ne saapuvat varastolle.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]