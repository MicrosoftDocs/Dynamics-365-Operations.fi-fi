---
title: Paikallisen tilikartan suunnittelu
description: Tämä artikkeli sisältää tietoja, joiden avulla voit suunnitella tilikartan, kun organisaatioltasi vaaditaan lakisääteisten/paikallisten vaatimusten noudattamista.
author: VeselinaE
ms.date: 10/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts, LedgerConsolidateAccountGroup, MainAccountConsolidateAccount, DimensionDetails, MainAccountDetails
ROBOTS: ''
audience: Application User
ms.devlang: ''
ms.reviewer: twheeloc
ms.tgt_pltfrm: ''
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.search.industry: ''
ms.author: veneva
ms.search.validFrom: 10/07/2021
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78379fd51cf24985fce83e2b6aa9a475af7df363
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946242"
---
# <a name="plan-your-local-chart-of-accounts"></a>Paikallisen tilikartan suunnittelu

[!include [banner](../includes/banner.md)]

Tämä artikkeli sisältää tietoja, joiden avulla voit suunnitella tilikartan, kun organisaatiossa on yrityksiä, joiden on täytettävä tiettyjen toimipaikkojensa paikalliset vaatimukset. Tässä artikkelissa käytetään seuraavia käsitteitä tilikarttojen kuvaamiseen:

- **Yleinen** – Tilikartta, jota organisaatio käyttää yleisesti. Useimmiten tämä tilikartta konsolidoidaan.
- **Paikallinen** – Tilikartta, jota käyttävät tietyn maan tai alueen yritykset.
- **Jaettu** – Tilikartta, jota voi käyttää useampi kuin yksi yritys. Sekä yleisiä että paikallisia tilikarttoja voi jakaa.

Voit luoda ja jakaa useita tilikarttoja. Useampi kuin yksi yritys voi käyttää jaettua tilikarttaa, mutta kullekin yritykselle voi määrittää vain yhden tilikartan. Yrityksen käyttämä tilikartta määritetään **Kirjanpito**-sivulla.

Kun organisaatiot suunnittelevat tilikartan, monilla niistä on päämääränä yleinen tilikartta. Jaetun tilikartan mahdollisuus mahdollistaa yleisen tilikartan luomisen. Yksittäisen tilikartan luomisella ja käyttämisellä on etuja. Esimerkiksi hallinto ja hallinta, ylläpito ja raportointi ovat helpompia.

Useimmat organisaatiot haluavat käyttää yleistä tilikarttaa, ja se onkin helpoin tyyppi toteutettavaksi. Tästä huolimatta osa yrityksistä tarvitsee paikallisen tilikartan seuraavista syistä:

- Paikalliset lakisääteiset vaatimukset
- Paikallisten kirjanpitostandardien vaatimukset
- Toimialan vaatimukset
- Yrityskohtaiset raportointi- ja analyysivaatimukset

Jos organisaatio edellyttää, että yritys käyttää paikallista tilikarttaa, sen voi toteuttaa kahdella eri tavalla:

- Määritä yleinen tilikartta ja määritä muita keinoja paikalliset vaatimusten täyttämiselle.
- Määritä yritykselle paikallinen tilikartta ja määritä suhteet yleiseen tilikarttaan.

Käytettävä vaihtoehto määräytyy organisaation ja raportoinnin rakenteen mukaan.

[![Kaavio, jossa näkyy, miten organisaatiorakenne määrittää, käytetäänkö yleistä vai paikallista tilikarttaa](./media/local-chart-of-accounts-diagram.png)](./media/local-chart-of-accounts-diagram.png)

Jos yritykselle on määritetty yleinen tilikartta, paikalliset raportointivaatimukset voi täyttää seuraavin keinoin:

- Suorita paikallista konsolidointia.
- Seuraa paikallista tilikarttaa taloushallinnon dimension avulla.
- Luo yleisessä tilikartassa paikallisia päätilejä.
- Suorita ulkoisia yhdistämismäärityksiä paikallisiin tilikarttoihin.

Jos yritykselle on määritetty paikallinen tilikartta, tällä hetkellä ainoa mahdollisuus täyttää yleiset raportointivaatimukset on yleinen konsolidointi.

## <a name="global-chart-of-accounts-assigned-to-a-legal-entity"></a>Yritykselle määritetty yleinen tilikartta

Jos yritykselle on määritettävä yleinen tilikartta, järjestelmän määrittämiselle on olemassa neljä vaihtoehtoa, kuten aiemmin kuvattiin. Kaikissa neljässä vaihtoehdossa määritetään tilikartta, joka linkitetään kuhunkin yritykseen **Kirjanpito**-sivulla. Kussakin vaihtoehdossa käytetään sitten erilaista lähestymistapaa lokalisointivaatimusten täyttämiseen. Seuraavissa osissa kuvataan korkean tason vaiheet, joilla järjestelmä määritetään lokalisointivaatimuksia varten. Niissä kuvataan myös kunkin vaihtoehdon hyvät ja huonot puolet.

### <a name="do-local-consolidation"></a>Paikallinen konsolidointi

Paikallinen konsolidointi on suositeltava tapa täyttää paikallisen tilikartan vaatimukset ja hyödyntää järjestelmän toiminnot, jotka on suunniteltu tähän tarkoitukseen.

#### <a name="set-up-consolidation-for-a-local-chart-of-accounts"></a>Paikallisen tilikartan konsolidoinnin määritys

1. Luo yksi yleinen tilikartta, joka sisältää kaikki tarvittavat päätilit.
2. Määritä kullekin yritykselle yleinen tilikartta **Kirjanpito**-sivulla.
3. Luo konsolidointiyritys jokaiselle vaaditulle lokalisoinnille.
4. Noudata seuraavia ohjeita:

    - Jos tarvitaan vain yksi lokalisointi, määritä konsolidointitili **Päätili**-sivulla tai käytä sivuja **Konsolidointiryhmät** ja **Konsolidoinnin lisätilit**.
    - Jos tarvitaan useita lokalisointeja tai jos sekä tilinumero että tilin nimi on käännettävä, käytä sivuja **Konsolidointiryhmät** ja **Konsolidointiryhmät** edustamaan lokalisointivaatimuksia.

5. Suorita konsolidointiprosessi muuntaaksesi yleistä tilikarttaa käyttävän lähdeyrityksen arvon konsolidointiyritykselle, joka käyttää paikallista tilikarttaa.

#### <a name="advantages"></a>Edut

- Tämä on yhdenmukainen tapa työskennellä koko organisaatiossa.
- Yksi paikallisen sijainnin käännös on tehty.
- Tämä menetelmä tukee sekä päätilin tunnuksen että kunkin päätilin nimen kääntämistä.
- Se tukee useita lokalisointeja.

#### <a name="disadvantages"></a>Huonot puolet

- Luodaan ylimääräinen konsolidointiyritys.
- Suoritetaan ylimääräinen konsolidointiprosessi.
- Tämä menetelmä voi raportoida lokalisoidun kartan perusteella vasta, kun konsolidointiprosessi on suoritettu.

### <a name="use-a-financial-dimension-to-track-the-local-chart-of-accounts"></a>Paikallisen tilikartan seuraaminen taloushallinnon dimension avulla

Tässä menetelmässä käytetään taloushallinnon dimensiota, jossa taloushallinnon dimension arvot edustavat lokalisointiin vaadittavia paikallisia päätilejä. Se toimii hyvin, kun tarvitaan vain yksi lokalisointi. Se on kuitenkin vähemmän käyttökelpoinen, kun lisätään enemmän lokalisointeja ja taloushallinnon dimensioita.

#### <a name="set-up-a-financial-dimension-for-a-local-chart-of-accounts"></a>Paikallisen tilikartan taloushallinnon dimension määrittäminen

1. Luo yksi yleinen tilikartta, joka sisältää kaikki tarvittavat päätilit.
2. Määritä kullekin yritykselle yleinen tilikartta **Kirjanpito**-sivulla.
3. Luo taloushallinnon dimensio, joka edustaa paikallista tilikarttaa.
4. Luo taloushallinnon dimension arvoja, jotka edustavat paikallisen tilikartan päätilejä.
5. Päivitä tilirakennetta siten, että se sisältää taloushallinnon dimension "paikallinen tilikartta".
6. Varmista, että taloushallinnon dimensiolla "paikallinen tilikartta" on aina arvo ja ettei se salli tyhjää arvoa. Harkitse johdettujen dimensioiden tai kiinteiden dimensioiden käyttöä.
7. Luo taloushallinnon dimensioiden sarja, jossa taloushallinnon dimensio "paikallinen tilikartta" on ensimmäinen valittu taloushallinnon dimensio. Taloushallinnon dimensioiden sarjaa voidaan käyttää, kun luodaan pääkirja.

#### <a name="advantages"></a>Edut

- Sekä yleisten että paikallisten tilikarttojen päätilit ovat olemassa tapahtumatasolla. Päätili on yleinen ja taloushallinnon dimension arvo on paikallinen.
- Tämä menetelmä tarjoaa reaaliaikaista raportointia ja sekä yleisen rahoitusaseman että paikallisen rahoitusaseman näkymiä.

#### <a name="disadvantages"></a>Huonot puolet

- Jos kirjanpidon parametrien **Reskontratilissä käytetyt arvot** -kentän arvoksi on määritetty **Kirjanpidolliset jaot**, kulua/varaa/voittoa varten käytettävää päätiliä edustavia taloushallinnon dimensioita käytetään virheellisesti myyntireskontran ja ostoreskontran reskontratilissä. Suosittelemme, että määrität kentän arvoksi tämän sijaan lähdeasiakirjan, sen varmistamiseksi, että käytetään oikeita taloushallinnon dimension arvoja.
- Jos tarvitaan useita paikallisia tilikarttoja ja niihin kaikkiin käytetään yhtä taloushallinnon dimensiota, käytettävien taloushallinnon dimensioiden arvojen luettelo voi olla pitkä ja vaikea käyttää.
- Jos tarvitaan useita paikallisia tilikarttoja ja kutakin tilikarttaa edustamaan käytetään erillistä taloushallinnon dimensiota, tämä voi vaikuttaa järjestelmän käytettävyyteen ja suorituskykyyn, kun lisätään taloushallinnon dimensioita ja niiden sarjoja.
- Suosittelemme harkitsemaan tarvittujen taloushallinnon dimensioiden lukumäärää, niissä olevien arvojen määrää sekä taloushallinnon dimensioiden sarjojen määrää, koska kaikki nämä tekijät voivat vaikuttaa järjestelmän suorituskykyyn.

### <a name="create-local-main-accounts-in-the-global-chart-of-accounts"></a>Paikallisten päätilien luonti yleisessä tilikartassa

*Mitä kopioeditori kysyi:* Tässä menetelmässä yleisen tilikartan paikalliset päätilit sisältävät paikallisen tilikartan päätilit yleisessä tilikartassa.

*Alkuperäisversio:* Paikallisten päätilien yleiseen analyysitodistukseen sisältymisen menetelmä tarkoittaa, että analyysitodistuksen päätilit sisällytetään yleiseen analyysitodistukseen.

*Pitäisikö sen sanoa näin:* Tässä menetelmässä paikallisen tilikartan päätilit sisällytetään yleiseen tilikarttaan.


#### <a name="set-up-local-main-accounts-in-the-global-chart-of-accounts"></a>Paikallisten päätilien määrittäminen yleisessä tilikartassa

1. Luo yksittäinen tilikartta, joka sisältää sekä yleisen tilikartan että paikallisen tilikartan päätilit.
2. Määritä kullekin yritykselle tilikartta **Kirjanpito**-sivulla.
3. Luo tilikartassa summatilejä, joilla lasketaan yhteen samaan tarkoitukseen käytettävät päätilit.
4. Luo kullekin paikalliselle tilille yritysten ohituksia, joilla estetään siirrot muilta yrityksiltä yrityksille, joille niitä ei ole tarkoitettu.
5. Luo kullekin yleiselle tilille yritysten ohituksia, joilla estetään siirtoja lokalisointiyrityksiltä.

#### <a name="advantages"></a>Edut

- Tietyissä raporteissa ja tietyissä järjestelmän näytöissä, kuten taselaskelmaraportissa, on käytettävissä reaaliaikainen näkymä sekä yleisestä rahoitusasemasta että paikallisesta rahoitusasemasta. Sen voi avata myös käyttämällä summatilin **Jakso**-painiketta.
- Kirjanpitotilissä ei ole ylimääräistä segmenttiä.

#### <a name="disadvantages"></a>Huonot puolet

- Summatilin käyttö ja näkyvyys ovat rajalliset. Summatilit eivät esimerkiksi näy **Pääkirja**-luettelosivulla.
- Ylläpito edellyttää lisätyötä.
- Talousraporttien luominen edellyttää manuaalista lisätyötä.

### <a name="do-external-mapping-to-the-local-chart-of-accounts"></a>Ulkoisten yhdistelmämääritysten paikallisiin tilikarttoihin luonti

Yleisen tilikartan käyttöönotossa oletetaan, että yhdistämismäärityksiä ja lokalisointia hallitaan järjestelmän ulkopuolella. Tässä menetelmässä luodaan vain yksi yleinen tilikartta Microsoft Dynamics 365 Financessa ja vaatimukset käsitellään järjestelmän ulkopuolella.

#### <a name="set-up-external-mapping-to-a-local-chart-of-accounts"></a>Ulkoisten yhdistämismääritysten määrittäminen paikalliseen tilikarttaan

1. Luo yksi yleinen tilikartta, joka sisältää kaikki tarvittavat päätilit.
2. Määritä kullekin yritykselle yleinen tilikartta **Kirjanpito**-sivulla.
3. Suorita yhdistämismääritys paikalliseen tilikarttaan Financen ulkopuolella.

#### <a name="advantages"></a>Edut

- Tämä menetelmä tarjoaa yhdenmukaisia työskentelytapoja koko organisaation laajuisesti.

#### <a name="disadvantages"></a>Huonot puolet

- Käytettävissä ei ole paikallista raportointia järjestelmästä.
- Tämä menetelmä on virhealtis, kun luodaan talousraportteja.

## <a name="local-chart-of-accounts-assigned-to-legal-entity"></a>Yritykselle määritetty paikallinen tilikartta

Jos organisaatio ei halua käyttää yleistä tilikarttaa kaikissa yrityksissä, jokaiselle yksilölliselle paikalliselle tilikartalle luodaan erillinen tilikartta. Kukin yritys linkitetään sen jälkeen vastaavaan tilikarttaan **Kirjanpito**-sivulla.

### <a name="do-global-consolidation"></a>Yleinen konsolidointi

Tässä menetelmässä käytetään konsolidointiyritystä kunkin paikallisen lähdeyrityksen taseiden koontiin ja yhdistämiseen yhdistetyksi konsolidointiyrityksen tilikartaksi. Tämä menetelmä edellyttää, että kustakin paikallisesta tillikartasta ylläpidetään yhdistämismääritystä konsolidointiyrityksen yleiseen tilikarttaan.

#### <a name="set-up-global-consolidation"></a>Yleisen konsolidoinnin määrittäminen

1. Luo erillinen tilikartta kullekin yritykselle, jolla on eri paikallinen tilikartta. Jos joillakin yrityksillä on sama paikallinen tilikartta, tarvitaan vain yksi paikallinen tilikartta, joka voidaan jakaa.
2. Määritä kullekin yritykselle asianmukainen tilikartta **Kirjanpito**-sivulla.
3. Valinnainen: Luo tilikartta kunkin konsolidointiyrityksen yleisille tilikartalle, jolla on eri yleinen tilikartta.
4. Luo kullekin vaadittavalle konsolidointitasolle konsolidointiyritys ja määritä asianmukainen tilikartta **Kirjanpito**-sivulla.
5. Noudata seuraavia ohjeita:

    - Jos tarvitaan vain yksi konsolidointi, määritä konsolidointitili **Päätili**-sivulla.
    - Jos tarvitaan useita konsolidointia tai jos sekä tilinumero että tilin nimi on käännettävä, käytä sivuja **Konsolidointiryhmät** ja **Konsolidointiryhmät** edustamaan yleiseen tilikarttaan kohdistuvia vaatimuksia.

6. Suorita konsolidointiprosessi siirtääksesi taseet paikallisilta yrityksiltä konsolidoidulle yritykselle. Tämä konsolidoitu yritys käyttää vaiheessa 5 määritettyjä konsolidointitilejä.

#### <a name="advantages"></a>Edut

- Paikallisen kirjanpidon standardimuotoa sovelletaan suoraan.
- Tämä menetelmä helpottaa paikallisen taloushallinnon tiimin työtä.

#### <a name="disadvantages"></a>Huonot puolet

- Yleisestä asemasta ei ole saatavilla reaaliaikaista näkymää.
- Konsolidointiprosessi saatetaan suorittaa useammin.

## <a name="additional-resources"></a>Lisäresurssit

- [Tilikartan suunnittelu](plan-chart-of-accounts.md)
- [Kirjanpitojen määrittäminen](configure-ledger.md)
- [Taloushallinnon dimensiot ja kirjaaminen](Default-dimensions.md#balancing-dimension)
- [Taloushallinnon dimensioyhdistelmät](financial-dimension-sets.md)
- [Konsolidoinnin ja eliminoinnin yleiskatsaus](../budgeting/consolidation-elimination-overview.md)
- [Konsolidointitiliryhmät ja lisäkonsolidointitilit](../budgeting/consolidation-account-groups-consolidation-accounts.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
