---
title: Työn luonnin aikatauluttaminen aallon aikana
description: Tässä aiheessa käsitellään työn luonnin aikatauluttamisen aaltokäsittelymenetelmän määrittämistä ja käyttämistä.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed8f43c7db139b7b16ac6901d5db56ba2f021690
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078256"
---
# <a name="schedule-work-creation-during-wave"></a>Työn luonnin aikatauluttaminen aallon aikana

[!include [banner](../includes/banner.md)]

*Työn luonnin aikataulutustoimintoa* käytetään aaltoprosessin osana parantamaan aaltokäsittelyn siirtomäärää siten, että järjestelmä luo työn käyttämällä rinnakkaiskäsittelyä.

Kun toiminto on otettu käyttöön, suunniteltu työ luodaan automaattisesti, ja järjestelmä käsittelee sen jossain vaiheessa, jolloin varsinainen työ luodaan. Jos aallon kuormarivien määrä saavuttaa esimääritetyn rajan, järjestelmä luo varsinaisen työn nopeammin hyödyntämällä rinnakkaista, asynkronista käsittelyä.

## <a name="enable-the-schedule-work-creation-feature"></a>Työn luonnin aikataulutustoiminnon ottaminen käyttöön

### <a name="enable-the-feature-in-feature-management"></a>Toiminnon ottaminen käyttöön ominaisuuksien hallinnassa

Ennen kuin *työn luonnin aikataulutustoimintoa* voidaan käyttää, se on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Työn luonnin aikataulutus*

> [!NOTE]
> *Organisaation laajuinen työn esto* -toiminto on oltava otettuna käyttöön, ennen kuin *Aikatauluta työn luonti* voidaan ottaa käyttöön.

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

1. Valitse **Valitut menetelmät** -sarakkeeseen osoittava nuoli ja siirrä valittu rivi kyseiseen sarakkeeseen. (Valittuna voi olla kerralla vain yksi menetelmä, jossa on käytössä joko *WHSScheduleWorkCreationWaveStepMethod* tai *createWork*, joten aiemmin luotu rivi, jonka **Menetelmän nimi** on *createWork*, siirretään automaattisesti **Jäljellä olevat menetelmät** -ruudukkoon.)

## <a name="set-wave-task-processing-threshold-data"></a>Aallon tehtävän käsittelyn raja-arvotietojen määrittäminen

Järjestelmä luo oletusarvoiset aallon tehtävän käsittelyn raja-arvotiedot, kun aaltokäsittely suoritetaan ensimmäisen kerran käyttämällä tehtävään perustuvaa käsittelyä. Tietojen avulla määritetään, milloin aaltokäsittely suoritetaan asynkronisesti ja tehtävään perustuen, jolloin työn rinnakkainen käsittely ja luonti on mahdollista.

Oletustiedot käyttävät aluksi kuormarivien minimimäärän (MINIMUMWAVELOADLINES) raja-arvona 15:tä. Tämä tarkoittaa sitä, että kun järjestelmä käsittelee yli 15 kuormariviä sisältävää aaltoa, se käyttää asynkronista tehtävien käsittelyä. Nämä tiedot voidaan lisätä tai päivittää manuaalisesti testiympäristöjen **WHSWaveTaskProcessingThresholdParameters**-taulussa. Jos tätä asetusta on muutettava tuotantoympäristössä, päivitystä on pyydettävä Microsoftin tuesta.

## <a name="work-with-the-feature"></a>Toiminnon käyttäminen

Kun *Aikatauluta työn luonti* -toiminto on otettu käyttöön, aaltokäsittely luo suunnitellun työn, jota uuden työn luontiprosessi käyttää jossain vaiheessa. Työ estetään työn luonnin aikana *Organisaation laajuinen työn esto* -toiminnolla.

Seuraava vuokaavio osoittaa, miten suunniteltu työ luodaan aaltokäsittelyn aikana.

![Ajoita työn luonti](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Suunniteltu työ

**Suunnitellun työn tiedot** -sivulla (**Varastonhallinta \> Työ \> Suunnitellun työn tiedot**) on tietoja suunnitellusta työstä, joka luotiin ensin aaltokäsittelyn aikana. Seuraavat **Prosessin tila** -arvot ovat käytettävissä:

- **Asetettu jonoon** – suunniteltu työ odottaa, että sitä käytetään työn luontiin.
- **Valmis** – suunniteltua työtä on käytetty työn luontiin.
- **Epäonnistui** – Aaltokäsittely on epäonnistunut. Huomaa, että suunnitellun työn tila voi olla **Epäonnistui** riippumatta siitä, onko sillä liittyvää varsinaista työtä. Kun varsinaisen työn luontiprosessi epäonnistuu, varsinaisen työn tilaksi jää *Peruutettu*.

### <a name="batch-job-for-the-work-creation-process"></a>Työn luontiprosessin erätyö

Käsittelyaaltojen erätöitä voi tarkastella valitsemalla **Kaikki aallot** -sivun toimintoruudussa **Erätyöt**.

Tällä tavoin voi tarkastella kunkin erätyötunnuksen kaikki erätehtävän tietoja.
