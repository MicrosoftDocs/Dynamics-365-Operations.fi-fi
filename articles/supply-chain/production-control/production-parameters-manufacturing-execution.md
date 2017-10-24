---
title: Tuotannonohjauksen tuotantoparametrit
description: "Tässä ohjeaiheessa on tietoja tuotannonohjauksen tuotantoparametrien asetuksista."
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: b24bb43e740835da25d44cb971e8f528db9cfacb
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="production-parameters-in-manufacturing-execution"></a>Tuotannonohjauksen tuotantoparametrit

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja tuotannonohjauksen tuotantoparametrien asetuksista.

**Tuotannonohjaus**-moduuli on suunnattu ensisijaisesti tuotantoyrityksille. Sillä voidaan rekisteröidä ajan ja nimikkeen kulutuksen tuotantotöissä tai -projekteissa. Ennen kuin töitä voidaan rekisteröidä tuotannonohjauksella, useat tuotantoparametrit on määritettävä. Nämä parametrit määrittävät miten ja milloin rekisteröinnit kirjataan tuotantoprosessin aikana. Tuotantoparametrien asetukset vaikuttavat varastonhallintaan, tuotantoon hallinnan ja kustannuslaskentaan.

Harkitse tarkasti, mitä **Tuotantotilausten oletusarvot** -sivun asetuksia haluat käyttää, ennen kuin työntekijät voivat aloittaa tuotantotöiden rekisteröinnin. Valitse **Tuotannonhallinta** &gt; **Asetukset** &gt; **Tuotannonohjaus** &gt; **Tuotantotilauksen oletusarvot**. Jos yritys käyttää multisite-toimintoja, kullekin toimipaikalle kannattaa määrittää erilaiset tuotantoparametrit. **Tuotanto**-moduulin integrointiparametrit määritetään seuraavilla **Tuotantoparametrit**-sivun välilehdillä:

- **Yleinen** – tuotannonohjauksen tuotantotöiden yleiset parametriasetukset.
- **Aloita** – parametrit, joita käytetään, kun tuotantovaiheet aloitetaan.
- **Työvaiheet** – parametrit, joita käytetään tuotantovaiheissa ja vaiheiden palautteessa tuotantoprosessin aikana.
- **Ilmoita valmiiksi** – parametrit, joita käytetään, kun nimikkeitä ilmoitetaan valmiiksi tuotantotilauksen viimeisessä työvaiheessa.
- **Oikeellisuustarkistus** – parametrit joilla tarkistetaan tuotantotilausten aloitus- ja palautemäärien oikeellisuus.

## <a name="types-of-production-jobs"></a>Tuotannon töiden tyypit
Voit valita **Työvaiheet** -välilehdessä **Työn rekisteröinti** -sivulla rekisteröivät tuotantotöiden tyypit.

Tavallisesti työntekijät voivat luoda rekisteröintejä asetus- ja prosessitöille. Jos kuitenkin töiden ajoitus on käytössä, voit valita muitakin työtyyppejä, jotka työntekijöiden on rekisteröitävä, kun tuotantotilauksia käsitellään. Voit esimerkiksi edellyttää siirtotöiden rekisteröintiä.

> [!IMPORTANT]
> Varmista, että olet valinnut kaikki soveltuvat työtyypit. Muutoin työt eivät välttämättä ole rekisteröitävissä **Työn rekisteröinti** -sivulla. Omien valintojen on vastattava valintoja, jotka on tehty **Töiden hallinta** -sarakkeessa **Reititysryhmät**-sivun **Asetukset**-välilehdessä (**Tuotannonhallinta** &gt; **Asetukset** &gt; **Reitit** &gt; **Reititysryhmät**).

Jos reititysryhmässä on valittu **Töiden hallinta**, kyseinen työtyyppi ilmoitetaan valmiiksi tuotantotilauksessa, kun työ ilmoitetaan valmiiksi tuotannonohjauksessa. Kun kaikki työtyypit, joissa **Töiden hallinta** on valittuna, on ilmoitettu valmiiksi työvaiheessa, tuotannonohjaus ilmoittaa työvaiheen valmiiksi.

> [!NOTE]
> Osan työtyypeistä voidaan voi ilmoittaa manuaalisesti tuotantokirjauskansioiden avulla. Valitse siinä tapauksessa työtyypiksi **Töiden hallinta** mutta älä valitse rekisteröinnin työtyyppiä tuotannonohjauksen **Tuotantoparametrit**-sivun **Työvaiheet**-välilehdessä.

## <a name="bom-consumption-and-picking-list-journals"></a>Tuoterakenteen kulutuksen ja keräysluettelon kirjauskansiot
Tuotantorakenteen kulutuksen yhdenmukainen määrittäminen on tärkeää, sillä sen avulla voidaan varmistaa, että varastonhallinta on tehokasta. Jos esimerkiksi tuoterakenteen kulutuksen parametreja ei määritetä oikein tuotannonohjauksessa, materiaalit voidaan vähentää varastosta kahdesti tai niitä ei vähennetä lainkaan.

Automaattinen tuoterakenteen kulutus määritetään **Tuotantoparametrit**-sivulla kolmessa vaiheessa:

- Tuotannon alkaessa. Määritä tämä vaihe **Alku**-välilehdessä.
- Tuotantoprosessin aikana, kun työvaihe on valmis. Määritä tämä vaihe **Työvaiheet**-välilehdessä.
- Ilmoitettaessa tuotantotilauksen olevan valmis. Määritä tämä vaihe **Ilmoita valmiiksi** -välilehdessä.

Voit valita kussakin vaiheessa **Automaattinen tuoterakennekulutus** -kentässä jonkin kolmesta tuotantotilauksen nimikkeiden keräysmenetelmästä:

- **Materiaaliottosääntö** – tätä asetusta käytetään yhdessä tuoterakenteen **Tuotanto**-moduulissa määritetyn asetuksen kanssa. Valitse **Tuotannonhallinta** &gt; **Yleinen** &gt; **Tuotantotilaukset** &gt; **Kaikki tuotantotilaukset**. Valitse **Kaikki tuotantotilaukset** -sivulla luettelosta tuotantotilaus ja valitse sitten toimintoruudussa **Tuoterakenne**. Valitse **Tuoterakenne**-sivun **Asetukset**-välilehden **Materiaaliottosääntö**-kentässä jokin seuraavista vaihtoehdoista:

    - **Alku**
    - **Lopetus**
    - **Manuaalinen**
    - Tyhjä (yhtään vaihtoehtoa ei valita).
    - **Käytettävissä sijainnissa**

    Jos tuotannonohjauksessa on valittu **Materiaaliottosääntö** **Alku**-välilehden **Automaattinen tuoterakennekulutus** -kentässä, kaikki tuoterakenteen materiaalit, joissa on valittu **Alku**, vähennetään varastosta työvaiheen alkaessa. **Käytettävissä sijainnissa** -vaihtoehtoa käytetään tuotteissa, joissa edistykselliset varastoprosessit on otettu käyttöön. Jos valitset tämän materiaalinottosäännön, materiaali otetaan, kun raaka-aineen keräyksen varastotyö on valmis. Materiaali otetaan myös silloin, kun tätä materiaaliottosääntöä käyttävä tuoterakenteen rivi vapautetaan varastoon ja materiaali on saatavana tuotannon varastosijainnissa.
    
    > [!NOTE]
    > Jos **Materiaaliottosääntö**-kenttä on valittu tuotannonohjauksen **Alku**-välilehdessä, sama sääntö on valittava myös joko **Työvaiheet**- tai **Ilmoita valmiiksi** -välilehdessä. Tämä edellytys auttaa varmistamaan, että materiaalit vähennetään varastoista niissä tuoterakenteissa, joissa tuotantotilauksen materiaaliottosäännöksi on valittu **Lopetus**. Jos samaa materiaaliottosääntöä ei valita joko **Työvaiheet**- tai **Ilmoita valmiiksi** -välilehdessä, on mahdollista, että materiaalit vähennetään varastosta kahdesti.
 
- **Aina** – Jos valitset tämän vaihevaihtoehdon, materiaalit vähennetään varastosta tässä vaiheessa. Tuotannon materiaalit vähennetään esimerkiksi silloin, kun tuotantotilaus aloitetaan. Tämä asetus edellyttää, että **Työvaiheet**- ja **Ilmoita valmiiksi** -välilehdissä valitaan **Ei koskaan**. Tämä edellytys auttaa estämään sen, että nimikkeet vähennetään varastosta kahdesti.
- **Ei koskaan** – Jos valitset tämän vaihevaihtoehdon, tuoterakennekulutusta ei tapahdu koskaan tässä vaiheessa. Jos esimerkiksi valitset **Ei koskaan** kaikissa kolmessa välilehdessä (**Alku**, **Työvaiheet** ja **Ilmoita valmiiksi**), materiaalit on vähennettävä varastosta manuaalisesti.

> [!IMPORTANT]
> Ole huolellinen tuotantoparametrien määrityksissä ja varmista, että **Tuotantoparametrit**-sivun eri välilehdissä valitut parametrit eivät ole keskenään ristiriitaisia.

Seuraavissa esimerkeissä esimerkkejä erilaisia tuoterakenteen kulutussääntöjä tukevista parametriasetuksista. Parametrit on määritetään tuotannonohjauksen **Tuotantoparametrit**-sivulla.

### <a name="example-1-backflushing-on-operations"></a>Esimerkki 1: Työvaiheiden jälkipoisto

Käytä seuraavia asetuksia, jos keräysluettelon kirjauskansiot ja tuoterakennenimikkeiden kulutus on luotava, kun työvaiheen nimikkeet ilmoitetaan valmiiksi.

| Välilehti                | Kenttä                          | Asetus                             |
|--------------------|--------------------------------|-------------------------------------|
| Alku              | Päivitä online-aloitus           | **Tila** tai **Tila + määrä** |
| Alku              | Automaattinen tuoterakennekulutus      | **Ei koskaan**                           |
| Operations         | Automaattinen tuoterakennekulutus      | **Aina**                          |
| Ilmoita valmiiksi | Automaattinen tuoterakennekulutus      | **Ei koskaan**                           |
| Ilmoita valmiiksi | Päivitä valmis online-raportti | **Tila + määrä**               |

### <a name="example-2-backflushing-on-production"></a>Esimerkki 2: Tuotannon jälkipoisto

Käytä seuraavia asetuksia, jos keräysluettelon kirjauskansiot ja tuoterakennenimikkeiden kulutus on luotava, kun tuotantotilauksen nimikkeet ilmoitetaan valmiiksi.

| Välilehti                | Kenttä                          | Asetus                             |
|--------------------|--------------------------------|-------------------------------------|
| Alku              | Päivitä online-aloitus           | **Tila** tai **Tila + määrä** |
| Alku              | Automaattinen tuoterakennekulutus      | **Ei koskaan**                           |
| Operations         | Automaattinen tuoterakennekulutus      | **Ei koskaan**                           |
| Ilmoita valmiiksi | Automaattinen tuoterakennekulutus      | **Aina**                          |
| Ilmoita valmiiksi | Päivitä valmis online-raportti | **Tila + määrä**               |

### <a name="example-3-flushing-principle"></a>Esimerkki 3: Materiaaliottosääntö

Käytä seuraavia asetuksia, jos keräysluettelon kirjauskansiot ja tuoterakennenimikkeiden kulutus on luotava tuoterakennenimikkeiden materiaalinottosäännön asetuksen mukaisesti.

| Välilehti                | Kenttä                          | Asetus                |
|--------------------|--------------------------------|------------------------|
| Alku              | Päivitä online-aloitus           | **Tila + määrä**  |
| Alku              | Automaattinen tuoterakennekulutus      | **Materiaaliottosääntö** |
| Operations         | Automaattinen tuoterakennekulutus      | **Materiaaliottosääntö** |
| Ilmoita valmiiksi | Automaattinen tuoterakennekulutus      | **Ei koskaan**              |
| Ilmoita valmiiksi | Päivitä valmis online-raportti | **Tila + määrä**  |

### <a name="example-4-deduction-of-materials-during-startup-of-a-production-order"></a>Esimerkki 4: Materiaalien vähennys tuotantotilauksen käynnistyksen aikana

Käytä seuraavia asetuksia, jos keräysluettelon kirjauskansiot ja tuoterakennenimikkeiden kulutus on luotava, kun tuotanto aloitetaan.

| Välilehti                | Kenttä                          | Asetus                             |
|--------------------|--------------------------------|-------------------------------------|
| Alku              | Päivitä online-aloitus           | **Tila + määrä**               |
| Alku              | Automaattinen tuoterakennekulutus      | **Aina**                          |
| Operations         | Automaattinen tuoterakennekulutus      | **Ei koskaan**                           |
| Ilmoita valmiiksi | Automaattinen tuoterakennekulutus      | **Ei koskaan**                           |
| Ilmoita valmiiksi | Päivitä valmis online-raportti | **Tila** tai **Tila + määrä** |

Keräysluettelon kirjauskansiot kirjataan aiemmin tässä osassa käsiteltyjen valintojen perusteella tuotantotilausprosessin eri vaiheissa:

- Työvaiheen alkaessa
- Työvaiheen määrää koskevaa palautetta ilmoitettaessa
- Ilmoitettaessa nimikkeitä valmiiksi tuotantotilauksessa

### <a name="example-5-manual-bom-consumption"></a>Esimerkki 5: Manuaalinen tuoterakennekulutus

Voit käyttää seuraavia asetuksia, jos materiaalit on poistettava aina manuaalisesti varastosta. Keräysluettelon kirjauskansioita ei siinä tapauksessa kirjata.

| Välilehti                | Kenttä                          | Asetus    |
|--------------------|--------------------------------|------------|
| Alku              | Päivitä online-aloitus           | **Tila** |
| Alku              | Automaattinen tuoterakennekulutus      | **Ei koskaan**  |
| Operations         | Automaattinen tuoterakennekulutus      | **Ei koskaan**  |
| Ilmoita valmiiksi | Automaattinen tuoterakennekulutus      | **Ei koskaan**  |
| Ilmoita valmiiksi | Päivitä valmis online-raportti | **Tila** |

