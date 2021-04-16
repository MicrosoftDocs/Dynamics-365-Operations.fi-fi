---
title: Työn luonnin aikatauluttaminen aallon aikana
description: Tässä aiheessa käsitellään työn luonnin aikatauluttamisen aaltokäsittelymenetelmän määrittämistä ja käyttämistä.
author: perlynne
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e4258c03b12a80a5bd81328ae7418835d68f82e7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835699"
---
# <a name="schedule-work-creation-during-wave"></a>Työn luonnin aikatauluttaminen aallon aikana

[!include [banner](../../includes/banner.md)]

*Työn luonnin aikataulutustoimintoa* käytetään aaltoprosessin osana parantamaan aaltokäsittelyn siirtomäärää siten, että järjestelmä luo työn käyttämällä rinnakkaiskäsittelyä.

Kun toiminto on otettu käyttöön, suunniteltu työ luodaan automaattisesti, ja järjestelmä käsittelee sen jossain vaiheessa, jolloin varsinainen työ luodaan. Jos aallon kuormarivien määrä saavuttaa esimääritetyn rajan, järjestelmä luo varsinaisen työn nopeammin hyödyntämällä rinnakkaista, asynkronista käsittelyä.

## <a name="turn-on-the-scheduled-work-creation-features-in-feature-management"></a>Ajoitetun työnluontiominaisuuden käyttöön ottaminen käyttöön ominaisuuksien hallinnassa

Jos haluat käyttää tässä ohjeaiheessa kuvattuja ominaisuuksia, niiden on oltava käytössä järjestelmässäsi. Ota [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa käyttöön seuraavat ominaisuudet seuraavassa järjestyksessä:

1. **Organisaation laajuinen töiden nesto** – Tarvitaan ajoitetun työn luomisen sekä manuaaliseen että automaattiseen määritykseen.
1. **Työn luomisen ajoitus** – Tarvitaan ajoitetun työn luomisen sekä manuaaliseen että automaattiseen määritykseen.
1. **Organisaation laajuinen Työn luomisen ajoitus -aaltomenetelmä** – Tarvitaan ajoitetun työn luomisen automaattiseen määritykseen. Et tarvitse tätä ominaisuutta, jos käytät vain manuaalista määritystä.

<a name="Auto-enable-schedule-work-creation"></a>

## <a name="automatically-configure-scheduled-work-creation"></a>Ajoitetun työn luomisen määrittäminen automaattisesti

Jos otat käyttöön *Organisaation laajuinen Työn luomisen ajoitus -aaltomenetelmä* -ominaisuuden, järjestelmässä tapahtuu automaattisesti seuraavat toimet:

- *Ajoita työn luonti* -aaltomenetelmä (`WHSScheduleWorkCreationWaveStepMethod`) lisätään ja määritetään toimimaan rinnakkain kaikkien oikeushenkilöiden välillä.
- Kaikkien oikeushenkilöiden aaltomallien, joiden **Aaltomallin tyyppi** -arvoksion määritetty *Toimitus* ja **mallin tilaksi** on määritetty *Voimassa*, *Luo työ* -menetelmä korvataan *Ajoita työn luonti* -menetelmällä. Niiden oikeushenkilöiden aaltomalleja, joissa *Luo työ* -menetelmän voi toistaa, ei kuitenkaan muokata.
- *Ajoita työn luonti* -menetelmän tehtävämääritykset luodaan kaikille varastoille kaikissa yrityksissä, joissa on käytössä **Käytä varastonhallintaprosesseja**. Tämä tarkoittaa, että *Ajoita työn luonti* -menetelmä suoritetaan nyt oletusarvoisesti rinnakkain. Olemassa olevat varastot, joiden **Käytä varastonhallintaprosesseja** -asetuksen arvo muuttu *Ei*-arvosta *Kyllä*-arvoon, suorittaa myös tämän menetelmän oletusarvoisesti rinnakkain.
- Kaikki oikeushenkilöt käsittelevät aaltoja erissä ja **Odota lukitusta (ms)** -arvoksi asetetaan oletusarvo *60 000* ms, jos sen arvoksi on aiemmin määritetty *0* ms.
- Kaikissa luomissasi uusissa aaltomalleissa on *Ajoita työn luonti* -aaltomenetelmä *Luo työ* -menetelmän sijaan.

Aiemmin luodut tehtävä- ja aaltokäsittelymääritykset säilytetään myös kaikille oikeushenkilöille, jotka on jo määritetty käsittelemään aaltoja erissä, ja kaikille varastoille, jotka on jo määritetty käyttämään *Ajoita työn luonti* -menetelmää samanaikaisesti.

Voit tarvittaessa palauttaa manuaalisesti minkä tahansa tai kaikki asetukset, jotka on tehty automaattisesti, kun otit käyttöön *Organisaation laajuinen Työn luomisen ajoitus -aaltomenetelmä* -ominaisuuden seuraavasti:

- Siirry aaltomallien käsittelemiseksi kohtaan **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**. Korvaa *Ajoita työn luonti* -menetelmä *Luo työ* -menetelmällä.
- Voit käsitellä varastonhallinnan parametreja valitsemalla **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**. Käytä **Aallon käsittely** -välilehdessä haluamiasi arvoja **Käsittele aallot erinä**- ja **Odota lukitusta (ms)** -asetuksille.
- Voit käsitellä aaltomenetelmiä valitsemalla **Varastonhallinta \> Asetukset \> Aallot \> Aallon käsittelymenetelmät**. Valitse `WHSScheduleWorkCreationWaveStepMethod` ja toimintoruudussa **Tehtävän määritys**. Muokkaa tai poista erätehtävien määrää ja määritettyä aaltoryhmää kullekin luettelossa olevalle varastolle tarpeen mukaan.

## <a name="manually-configure-scheduled-work-creation"></a>Ajoitetun työn luomisen määrittäminen manuaalisesti

Jos et ottanut käyttöön [*Organisaation laajuinen Työn luomisen ajoitus -aaltomenetelmä* -ominaisuutta](#Auto-enable-schedule-work-creation), voit määrittää ajoitetun työn luomisen manuaalisesti tässä osassa annettujen menettelyjen avulla tarpeen mukaan.

### <a name="manually-enable-batch-processing-of-waves"></a>Aaltojen eräkäsittelyn ottaminen käyttöön manuaalisesti

Varastotyön luominen hyödyntämällä rinnakkaista, asynkronista menetelmää edellyttää, että aaltokäsittely suoritetaan erinä. Se määritetään seuraavasti:

1. Valitse  **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
1. Määritä **Yleiset**-välilehden **Käsittele aaltoja erässä** -asetukseksi *Kyllä*. Valinnaisena on mahdollista valita myös erillinen **Aallon käsittelyn eräryhmä**, joka estää eräjonon käsittelemisen suorittaminen samanaikaisesti muiden prosessien kanssa.
1. Määritä **Odota lukitusta (ms)**, jota käytetään, kun järjestelmä käsittelee useita aaltoja samanaikaisesti. Useimmille suurille aaltokäsittelyille arvoksi kannattaa valita *60 000*.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>Uuden aallon vaihemenetelmän ottaminen käyttöön manuaalisesti aiemmin luoduissa aaltomalleissa

Aloita luomalla uusi aallon vaihemenetelmä ja ottamalla se käyttöön rinnakkaisessa, asynkronisessa tehtävän käsittelyssä.

1. Valitse  **Varastonhallinta \> Asetukset \> Aallot \> Aallon käsittelymenetelmät**.
1. Valitse  **Luo menetelmät uudelleen** ja kiinnitä huomiota siihen, että *WHSScheduleWorkCreationWaveStepMethod* on lisätty luetteloon lähetyksen aaltomalleissa käytettävissä olevista aallon käsittelymenetelmistä.
1. Valitse tietue, jonka **Menetelmän nimi** on *WHSScheduleWorkCreationWaveStepMethod*, ja valitse **Tehtävän määritys**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi** ja käyttämällä seuraavia asetuksia:

    - **Varasto** – valitse varasto, jota käytetään työn luonnin käsittelyn aikatauluttamiseen.
    - **Erätehtävien enimmäismäärä** – Määritä erätehtävien enimmäismäärä. Useimmissa tapauksissa tämän arvon on syytä olla 8–16, mutta optimaalista asetusta eri skenaarioihin kannattaa etsiä kokeilemalla.
    - **Aallon käsittelyn eräryhmä** – valitse erillinen aallon käsittelyn eräryhmä optimoimaan eräjonon käsittely.

Aiemmin luotu aaltomalli voidaan nyt päivittää (tai uusi aaltomalli luoda) käyttämään aallon *Aikatauluta työn luonti* -käsittelymenetelmää.

1. Valitse  **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse luetteloruudussa päivitettävä aaltomalli. (Jos testaukseen käytetään esittelytietoja, voit käyttää mallia *24 Lähetyksen oletus*).
1. Laajenna **Menetelmät**-pikavälilehti ja valitse **Jäljellä olevat menetelmät** -ruudukossa rivi, jonka **Nimi** on *Aikatauluta työn luonti*.
1. Valitse **Valitut menetelmät** -sarakkeeseen osoittava nuoli ja siirrä valittu rivi kyseiseen sarakkeeseen. (Valittuna voi olla kerralla vain yksi menetelmä, jossa on käytössä joko `WHSScheduleWorkCreationWaveStepMethod` tai `createWork`, joten aiemmin luotu rivi, jonka **menetelmän nimi** on `createWork`, siirretään automaattisesti **Jäljellä olevat menetelmät** -ruudukkoon.)

## <a name="set-wave-task-processing-threshold-data"></a>Aallon tehtävän käsittelyn raja-arvotietojen määrittäminen

Järjestelmä luo oletusarvoiset aallon tehtävän käsittelyn raja-arvotiedot, kun aaltokäsittely suoritetaan ensimmäisen kerran käyttämällä tehtävään perustuvaa käsittelyä. Tietojen avulla määritetään, milloin aaltokäsittely suoritetaan asynkronisesti ja tehtävään perustuen, jolloin työn rinnakkainen käsittely ja luonti on mahdollista.

Oletustiedot käyttävät aluksi kuormarivien minimimäärän (`MINIMUMWAVELOADLINES`) raja-arvona 15:tä. Tämä tarkoittaa sitä, että kun järjestelmä käsittelee yli 15 kuormariviä sisältävää aaltoa, se käyttää asynkronista tehtävien käsittelyä. Voit lisätä tai päivittää nämä tiedot manuaalisesti testiympäristöjen `WHSWaveTaskProcessingThresholdParameters`-taulukkoon. Jos sinun on muutettava tätä asetusta tuotantoympäristössä, pyydä päivitys Microsoft-tuesta.

## <a name="work-with-the-scheduled-work-creation"></a>Ajoitetun työn luomisen käsittely

Lisätietoja ajoitetun työn luomisen käsittelystä on kohdassa [Aallon luominen ja käsittely](wave-processing.md). 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
