---
title: Menojen tarkistajien määrittäminen
description: Tässä artikkelissa kuvataan, kuinka menojen tarkistajia käytetään valitsemaan dynaamisesti käyttäjä, jolle työnkulkutehtävä, hyväksyntä tai manuaalinen päätös on kohdistettu.
author: rachel-profitt
ms.date: 06/25/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2021-06-24
ms.openlocfilehash: 110edf4c2733f899368069c7d215ae5b0882f5cc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863220"
---
# <a name="configure-expenditure-reviewers"></a>Menojen tarkistajien määrittäminen
[!include[banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Voit määrittää dynaamisia menojen tarkistajia reitittääksesi menoja tarkistettavaksi joko projektirooliin kohdistetun käyttäjän perusteella tai sen taloushallinnon dimension perusteella, jossa meno veloitetaan. Työnkulkuprosessi määrittää tietyn projektin roolin tai taloushallinnon dimension omistajan avulla, kenelle menot reititetään.

Voit määrittää yhden tai useamman menojen tarkistajan määrityksen ja valita määrityksen, kun luot työnkulun. Voit määrittää menojen tarkistajan arvot jokaiselle organisaatiosi yritykselle. Kun olet määrittänyt menojen tarkistajan määritykset, voit kohdistaa määrityksen. Menojen tarkistajat voidaan kohdistaa työnkulkutehtäviin, hyväksyntöihin ja manuaalisiin päätöksiin.

> [!NOTE]
> Vaikka meojen tarkistajat eivät ole pakollisia, ne voivat tehdä työnkulkusi määrittämisestä yksinkertaisempaa. Sinun ei tarvitse esimerkiksi luoda yhtä ehdollista päätöstä tarkistaaksesi kunkin kustannuspaikkadimension ja luoda sitten toisen elementin, jotta voisit kohdistaa hyväksynnän tai tehtävän tietylle käyttäjälle tai käyttäjäryhmälle. Sen sijaan voit määrittää kustannuspaikkadimension omistajan ja valita oikean käyttäjän dynaamisesti menojen tarkistajan avulla. Tällä tavalla, kun kustannuspaikkojen omistaja tai kohdistus muuttuu, sinun tarvitsee päivittää vain taloushallinnon dimension **Omistaja**-kenttä.

## <a name="types-of-expenditure-reviewers"></a>Menojen tarkistajien tyypit

Kaikki työnkulut eivät tue menojen tarkistajien käsitettä. Voit määrittää menojen tarkistajia oletusarvoisesti ostoehdotuksille, ostotilauksille, toimittajalaskuille ja kuluraporteille. Kaikki nämä työnkulkutyypit edellyttävät, että määrität menojen tarkistajat erillisellä sivulla, joka koskee vain tiettyä ominaisuutta ja moduulia. Menojen tarkistajia voidaan käyttää kullekin tuetulle tiedostolle joko otsikkotason työnkuluissa tai rivitason työnkuluissa.

Seuraava taulukko näyttää, mistä voit määrittää menojen tarkistajan kullekin tuetulle asiakirjalle.

| Tiedosto | Siirtymispolku |
|----------|-----------------|
| Kuluraportit | Kulujenhallinta \> Asetukset \> Käytännöt \> Menojen tarkistajat |
| Ostotilaukset | Hankinta \> Asetukset \> Käytännöt \> Ostotilausten menojen tarkistajat |
| Ostoehdotukset | Hankinta \> Asetukset \> Käytännöt \> Ostoehdotusten menojen tarkistajat |
| Toimittajan laskut | Ostoreskontra \> Käytännön asetukset \> Toimittajalaskujen menojen tarkistajat |

## <a name="expenditure-reviewer-assignments"></a>Menojen tarkistajien tehtävät

Menojen tarkistajalle on saatavilla kaksi tehtävätyyppiä: *projektin jakaumat* ja *organisaation jakaumat*. Voit valita projektin jakaumalle projektiviranomaiset tai taloushallinnon dimensiot. Voit valita organisaation jakaumalle taloushallinnon dimensiot.

Projektiviranomaiset sisältävät projektipäällikön, projektin budjettipäällikön ja projektin myyntipäällikön. Voit määrittää nämä viranomaiset suoraan projektissasi valitsemalla työntekijän asianmukaisista kentistä.

Kunkin yrityksen tilirakenteet hallitsevat taloushallinnon dimensioita. Voit valita kullekin yritykselle taloushallinnon dimensiot, joita käytetään menojen tarkistajan kanssa. Dimensiot voidaan saada joko projektista (jolloin valitset dimensiot **Projektin jakaumat** -välilehdestä) tai asiakirjasta (jolloin valitset dimensiot **Organisaation jakauma** -välilehdessä). Voit valita jokaiselle taloushallinnon dimensiolle työntekijän **Taloushallinnon dimensioiden arvot** -sivun **Omistaja**-kentästä.

## <a name="example-1-expenditure-reviewers-based-on-organization-distributions"></a>Esimerkki 1: Organisaation jakaumiin perustuvat menojen tarkistajat

Työskentelet Contoso Appliances -yrityksessä, ja organisaatiollasi on kuusi osastoa ja 10 kustannuspaikkaa. Kun uusi ostoehdotus lähetetään, hyväksyntä täytyy saada ensin osastopäälliköltä ja sitten kustannuspaikan päälliköltä.

Tässä esimerkissä määrität kaksi *ostoehdotusten menojen tarkistajaa*:

- Annat ensimmäiselle tarkistajalle osaston nimen ja valitset sitten taloushallinnon **Osasto**-dimension **Organisaation jakaumat** -välilehdestä. 
- Toiselle tarkistajalle annat kustannuspaikan nimen ja valitset sitten taloushallinnon **Kustannuspaikka**-dimension **Organisaation jakaumat** -välilehdestä.

Kun määrität työnkulun, luot kaksi hyväksyntävaihetta. Ensimmäinen on osastolle ja toinen kustannuspaikalle. Valitset jokaiselle hyväksyntäelementille **Rooliperustainen**-välilehden **Tehtävän tyyppi** -kentästä **Osallistuja**, valitset **Osallistujan tyyppi** -kentästä **Kulujen osallistujat** ja valitset sitten asiaankuuluvan osallistujan **Osallistuja**-kentästä.

Kun ostoehdotus luodaan, taloushallinnon Osaston ja Kustannuspaikka-dimensiot kohdistetaan ostoehdotuksen riveille. Kun työnkulku lähetetään, järjestelmä arvioi ensin ostoehdotuksen osaston ja kohdistaa hyväksyntäelementin käyttäjälle, joka liittyy osastolle valitsemaasi työntekijään. Kun ensimmäinen hyväksyntävaihe on suoritettu, järjestelmä arvioi toisen hyväksyntävaiheen ja kohdistaa toisen hyväksyntäelementin käyttäjälle, joka liittyy kustannuspaikalle valitsemaasi työntekijään.

## <a name="example-2-expenditure-reviewers-based-on-project-distributions"></a>Esimerkki 2: Projektin jakaumiin perustuvat menojen tarkistajat

Työskentelet Contoso Appliances -yrityksen palveluosastolla. Organisaatio edellyttää, että kunkin ostotilauksen projektipäällikön täytyy hyväksyä meno. Lisäksi projektin kustannuspaikan päällikön on hyväksyttävä se. Hyväksynnät voidaan tehdä samanaikaisesti. Molempien käyttäjien on joka tapauksessa hyväksyttävä ostotilaus ennen kuin työnkulku voi jatkaa.

Tässä esimerkissä luot yhden *ostotilausten menojen tarkistajan*, jonka nimi on **Projektipäällikkö ja kustannuspaikka**. Valitset **Projektipäällikkö**-valintaruudun ja määrität **Ostotilausten menojen tarkistaja** -sivun **Projektin jakaumat** -välilehden **Kustannuspaikan dimensio** -vaihtoehdoksi **Kyllä**. Sinun täytyy varmistaa osana kokoonpanoa, että **Projektipäällikkö**-kenttä on määritetty kaikille projekteille ja että kaikille kustannuspaikoille on määritetty omistaja **Taloushallinnon dimension arvot** -sivulla.

Kun määrität työnkulun, tarvitset yhden hyväksyntäelementin. Valitset **Tehtävän tyyppi** -kentästä **Osallistuja**. Sen jälkeen valitset **Rooliperustainen**-välilehden **Osallistujan tyyppi** -kentästä **Kulujen osallistujat** ja valitset projektipäällikön ja kustannuspaikan **Osallistuja**-kentästä. Valitset **Valmistumiskäytäntö**-kentästä **Kaikki hyväksyjät** varmistaaksesi, ettei työnkulku voi jatkaa ennen kuin sekä projektipäällikkö että kustannuspaikan omistaja ovat hyväksyneet työnkulun.

Kun ostotilaus luodaan, **Projekti**-kenttä on määritettävä. Jos et vaadi projektia kaikille ostotilauksille, sinun tulisi lisätä työnkulkuusi ehdollinen päätös, joka etsii projektia ennen hyväksyntävaiheen suorittamista. Tämän jälkeen järjestelmä tarkistaa, että ostotilaukselle on määritetty projekti, ja kohdistaa hyväksyntäelementin **Projektipäällikkö**-kentässä valittuun työntekijään liittyvälle käyttäjälle. Lisäksi järjestelmä luo tehtävän ja kohdistaa sen käyttäjälle, joka liittyy projektista kustannuspaikalle **Omistaja**-kentässä valitsemaasi työntekijään. Huomaa, että tässä esimerkissä käytetään projektin kustannuspaikkaa, ei ostotilauksen kustannuspaikkaa.

## <a name="set-up-expenditure-reviewers"></a>Menojen tarkistajien määrittäminen

Tässä esimerkissä näytetään, miten voit määrittää ostosehdotusten menojen tarkistajan. Jos haluat määrittää muun tyyppisiä menojen tarkistajia, korvaa vaiheessa 1 oleva siirtymispolku asiaankuuluvalla polulla tämän artikkelin aiemman [Menojen tarkistajien tyypit](configure-expenditure-reviewers.md#types-of-expenditure-reviewers) -osan taulukosta.

1. Siirry kohtaan **Hankinta \> Asetukset \> Käytännöt \> Ostoehdotusten menojen tarkistajat**.
2. Valitse **Ostoehdotusten menojen tarkistajat** -sivulta **Uusi**.
3. Kirjoita **Nimi**-kenttään menojen tarkistajien määrityksen nimi, esimerkiksi **kustannuspaikka**.
4. Valitse määritettävä yritys **Menojen tarkistajat yrityksittäin** -pikavälilehdestä.
5. Jos käytät projektin jakaumaa, valitse jokaisen projektiviranomaisen valintaruutu ja valitse jokaiselle käyttöön otettavalle taloushallinnon dimensiolle **Kyllä**. 
6. Jos käytät organisaation jakaumaa, valitse jokaiselle käyttöön otettavalle taloushallinnon dimensiolle **Organisaation jakaumat** -välilehdestä **Kyllä**.
7. Toista vaiheet 4-6 jokaiselle lisäyritykselle.

## <a name="assign-owners-to-financial-dimensions"></a>Omistajien kohdistaminen taloushallinnon dimensioihin

Kohdista taloushallinnon dimensiolle omistaja noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Kirjanpito \> Tilikartta \> Dimensiot \> Taloushallinnon dimensiot**.
2. Valitse luettelosta taloushallinnon dimensio, jolle haluat kohdistaa omistajat.
3. Valitse **Dimensioarvot**.
4. Valitse **Muokkaa** tehdäksesi muutoksia dimensioarvoihin.
5. Valitse luettelosta dimensioarvo, jolle haluat kohdistaa omistajan.
6. Valitse **Omistaja**-kentästä työntekijä, jolle dimensioarvo kohdistetaan.

## <a name="configure-project-distributions"></a>Projektin jakaumien määrittäminen

Kohdista projektille projektiviranomaisia noudattamalla seuraavia ohjeita.

1. Valitse **Projektinhallinta ja kirjanpito \> Projektit \> Kaikki projektit**.
2. Valitse projekti, johon viranomaiset kohdistetaan.
3. Valitse **Muokkaa** tehdäksesi muutoksia projektiin.
4. Valitse **Yleiset**-pikavälilehden **Vastuuhenkilö**-osiosta työntekijä **Myyntipäällikkö**-, **Projektipäällikkö**- ja **Projektin budjettipäällikkö** -kenttiin tarpeen mukaan.
5. Valitse **Taloushallinnon dimensiot** -pikavälilehdestä projektille tarvittavat taloushallinnon dimensiot.

## <a name="assign-expenditure-reviewers-to-a-workflow-task"></a>Menojen tarkistajien kohdistaminen työnkulkutehtävään

Tässä esimerkissä näytetään, miten ostoehdotusten työnkulku määritetään käyttämään ostoehdotusten menojen tarkistajaa. Jos haluat määrittää myyn tyyppisiä työnkulkuja, vaiheessa 1 avattava työnkulkusivu voi olla **Kulujenhallinta**- tai **Ostoreskontra**-moduulissa **Hankinta**-moduulin sijaan.

Voit kohdistaa ostosehdotusten menojen tarkistajia työnkulkutehtävään noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Hankinta \> Asetukset \> Hankinnan työnkulut**.
2. Kaksoisnapauta (kaksoisnapsauta) olemassa olevaa työnkulkua tai luo uusi työnkulku.
3. Valitse työnkulkueditorin **Työnkulku**-ruudusta tehtävä, jolle menojen tarkistajien kokoonpano kohdistetaan. Valitse sitten **toimintoruudun** **Näytä**-ryhmästä **Ominaisuudet**.
4. Valitse **Ominaisuudet**-sivun vasemmanpuoleisesta ruudusta **Tehtävä**.
5. Valitse **Tehtävän tyyppi** -välilehdestä **Osallistuja**.
6. Valitse **Rooliperustainen**-välilehden **Osallistujan tyyppi** -kentästä **Kulujen osallistujat**. Valitse sitten **Osallistuja**-kentästä menojen tarkistajan kokoonpano, jota käytetään työnkulkutehtävälle.
