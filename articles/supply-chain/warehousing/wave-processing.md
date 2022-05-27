---
title: Aaltojen luominen ja käsittely
description: Tässä ohjeaiheessa kuvataan, kuinka aalto luodaan, käsitellään ja vapautetaan keräilytyön luomiseksi kuormalle, lähetykselle, tuotantotilaukselle tai kanban-tilaukselle.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, WHSParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage, WHSProdWaveTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 349285f089ecab00c4c1c0a0315c4223314e3e79
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687501"
---
# <a name="wave-creation-and-processing"></a>Aaltojen luominen ja käsittely

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan, kuinka aalto luodaan, käsitellään ja vapautetaan keräilytyön luomiseksi kuormalle, lähetykselle, tuotantotilaukselle tai kanban-tilaukselle. Voit luoda aaltoja seuraaville tilaustyypeille:

- **Myyntitilaukset** – ota myyntitilauksien rivit mukaan lähetysaaltojen avulla. Kun myyntitilaus on vapautettu varastoon, myyntitilauksen rivit voidaan sisällyttää aaltoon.
- **Tuotantotilaukset** – Käytä tuotantoaaltoja ottaaksesi mukaan tuotteen tuoterakenteen (BOM) rivit.
- **Kanban-tilaukset** – kanban-aallot sisältävät keräysluettelorivit kanban-tilauksista.

Myynti- ja kanbantilauksille inventaario tulee varata ennen kuin tilaus viedään varastolle. Muussa tapauksessa tietyn kohdistuksen rivejä ei voi käsitellä aallossa. Tuotantotilaukset ovat hieman joustavampia. Tuotantotilauksia varten voit valita jommankumman seuraavista vaihtoehdoista:

- Edellytä, että kaikki materiaalit on varattava, ennen kuin tilauksen voi vapauttaa varastoon.
- Salli tuotantotilausten vapautus varastoon vaikka kaikkia materiaaleja ei voi varata. Jos valitset tämän vaihtoehdon, pitää vapautus varastoprosessiin toistaa manuaalisesti, kun muut materiaalit tulevat käyttöön. Tämä on hyödyllistä esimerkiksi silloin, kun sinulla on tuotannon käynnistämiseen tarvittavat materiaalit ja voit odottaa, kunnes muut materiaalit ovat käytettävissä.

**Tuotannonhallinnan parametrit** -sivun **Materiaalivarauksen tarve** -kentän avulla voit määrittää, mitä näistä tuotantotilauksen vaihtoehdoista käytetään oletusarvoisesti. Voit kuitenkin muuttaa kunkin tietyn tuotantotilauksen asetuksia tarpeen mukaan. Lisätietoja: [Varaston parametrit aaltojen käsittelylle](wave-warehouse-parameters.md).

## <a name="create-and-process-a-wave"></a>Luo ja käsittele aaltoja

Seuraavassa kaaviossa näkyy työnkulku lähetysaaltojen luonnille, käsittelylle ja vapautukselle. Numerot vastaavat aiheessa myöhemmin käsiteltäviä osia.

![Aallon luomisen prosessi.](media/wave-processing-diagram.png "Aallon luomisen prosessi")

### <a name="prerequisites"></a>Edellytykset

Ennen kuin aloitat, aaltomalli on oltava luotavalle aaltotyypille (lähetys, tuotanto tai kanban). Aaltomalli määrittää monia asetuksia sille, miten aallot luodaan ja käsitellään, myös sen, mitä vaiheita on tehtävä manuaalisesti ja mitkä tehdään automaattisesti. Lisätietoja on kohdassa [Aaltomallit](wave-templates.md).

### <a name="create-a-wave"></a>Luo aalto

#### <a name="automatically-create-waves-based-on-warehouse-and-order-type"></a>Automaattinen aaltojen luominen varaston ja tilaustyypin perusteella

Jos haluat luoda aaltoja automaattisesti, määritä [aaltomallit](wave-templates.md), jotka koskevat kutakin tilaustyyppiä ja varastoa. Varmista, että jokaiseen malliin on määritetty **Automatisoi aallon luonti** -arvoksi *Kyllä*.

#### <a name="manually-create-waves"></a>Luo aaltoja manuaalisesti

Luo aalto manuaalisesti seuraavien ohjeiden avulla:

1. Varmista, että asiaankuuluvia [aaltomalleja](wave-templates.md) ei ole määritetty automaattisesti luomaan varastolle ja tilaustyypille aaltoa, kun haluat tehdä sen manuaalisesti.
1. Napsauta yhtä seuraavista riippuen luotavan aallon tyypistä:

    - Valitse **Varastonhallinta** \> **Yhteiset** \> **Aallot** \> **Lähetysaallot** \> **Kaikki aallot**. Valitse toimintoruudussa **Aalto**.
    - Valitse **Varastonhallinta** \> **Yhteiset** \> **Aallot** \> **Tuotantoaallot** \> **Kaikki tuotantoaallot**. Valitse toimintoruudussa **Tuotantoaalto**.
    - Valitse **Varastonhallinta** \> **Yhteiset** \> **Aallot** \> **Kanban-aallot** \> **Kaikki kanban-aallot**. Valitse toimintoruudussa **Luo aalto**.

1. Kirjoita **Kuvaus**-kenttään aallon lyhyt kuvaus. Tästä tulisi käydä ilmi, mitä aallossa käsitellään.

1. Valitse **Aaltomallin nimi**-kenttään aaltomalli luotavan aallon tyypille. Aaltomalli sisältää aaltomenetelmiä, jotka suorittavat toimintoja, kuten työn luonti aallolle. Esimerkiksi lähetysaaltojen aaltomalli voi sisältää menetelmiä kuormien luontiin, rivien liittämiseksi aaltoihin, täydentämiseen ja keräilytyön luomiseksi aallolle.

1. Halutessasi käyttää aaltomääritteitä kyselyn lisäehtoina aallolle, valitse määritteet **Aallon määritteet**-kentissä.

### <a name="specify-what-to-include-in-a-wave"></a>Määritä, mitä haluat sisällyttää aaltoon

Kun aalto on luotu, voit alkaa lisätä siihen sisältöä.

> [!NOTE]
> Voit tarvittaessa lisätä rivejä aaltoon myös sen jälkeen, kun se on käsitelty, kunhan sitä ei ole vapautettu.

#### <a name="automatically-specify-what-to-include-in-a-wave"></a>Määritä automaattisesti, mitä haluat sisällyttää aaltoon

Jos haluat luoda aaltoja automaattisesti, määritä [aaltomallit](wave-templates.md), jotka koskevat kutakin tilaustyyppiä ja varastoa. Varmista, että jokaiseen malliin on määritetty **Automatisoi aallon luonti** -arvoksi *Kyllä*. Vaihtoehtoisesti malli voi liittää rivejä automaattisesti mihin tahansa kelvolliseeen avoimeen aaltoon, jos **Määritä avoimiin aaltoihin** -asetus on *Kyllä*.

#### <a name="manually-specify-what-to-include-in-a-wave"></a>Määritä manuaalisesti, mitä haluat sisällyttää aaltoon

Kun aalto on luotu, mutta sitä ei ole vielä vapautettu, voit määrittää manuaalisesti, mitä siihen sisällytetään. Rivien lisääminen aaltoon manuaalisesti:

1. Suorita jokin seuraavista riippuen aallon tyypistä, johon rivit lisätään:

    - Valitse **Varastonhallinta** \> **Yhteiset** \> **Aallot** \> **Lähetysaallot** \> **Kaikki aallot**. Valitse toimintoruudussa **Aalto**.
    - Valitse **Varastonhallinta** \> **Yhteiset** \> **Aallot** \> **Tuotantoaallot** \> **Kaikki tuotantoaallot**. Valitse toimintoruudussa **Tuotantoaalto**.
    - Valitse **Varastonhallinta** \> **Yhteiset** \> **Aallot** \> **Kanban-aallot** \> **Kaikki kanban-aallot**. Valitse toimintoruudussa **Luo aalto**.

1. Valitse aalto. Valitse toimintoruudussa yksi seuraavista:

      - **Ylläpidä lähetyksiä**
      - **Ylläpidä tuotantoja**
      - **Ylläpidä kanban-työn keräysluetteloita**

1. Valitse ikkunan yläosassa aaltoon lisättävä rivi ja valitse sitten **Lisää aaltoon**. Rivi siirretään **Aallon rivit** -pikavälilehdelle.

    Toista tämä vaihe kullekin lisättävälle riville. Jos haluat lisätä kaikki rivit, valitse **Lisää kaikki**.

    > [!TIP]
    > Lähetysaalloille voit löytää tietyn tilauksen valitsemalla yksilöllisen suodattimen **Aallon suodatinkoodi** -kentässä. Aallon suodatinkoodit sisältävät kyselykriteereitä lähetyksille, jotka on luotu **Aallon suodattimet** -lomakkeella. Tämä kenttä ei ole käytettävissä tuotantoaalloille tai kanban-aalloille.
    > Vihreä valintamerkki **Aallossa**-sarakkeessa ilmaisee, että lähetys on lisätty aaltoon.

### <a name="process-the-wave-to-create-the-picking-work"></a>Käsittele aalto luodaksesi keräystyön

Kun aalto on luotu ja se sisältää kaikki tarvittavat rivit, voit käsitellä sitä vastaavan keräystyön luomista varten.

#### <a name="automatically-process-a-wave"></a>Käsittele aalto automaattisesti

Jos haluat käsitellä aallon automaattisesti, määritä asianmukaiset [aaltomallit](wave-templates.md), joissa on tarvittavat automaattisen käsittelyn asetukset.

#### <a name="manually-process-a-wave"></a>Käsittele aalto manuaalisesti

Voit käsitellä aallon vain, kun **Aallon tila** on *Luotu*. Kun olet käsitellyt aallon, **Aallon tila** -arvoksi tulee *Pidossa*.

Jos haluat manuaalisesti käsitellä aallon, jossa on kaikki sen edellyttämät sisällöt, noudata seuraavia ohjeita:

1. Tee jokin seuraavista riippuen käsiteltävän aallon tyypistä:

    - Valitse **Varastonhallinta** \> **Yhteiset** \> **Aallot** \> **Lähetysaallot** \> **Kaikki aallot**. Valitse toimintoruudussa **Aalto**.
    - Valitse **Varastonhallinta** \> **Yhteiset** \> **Aallot** \> **Tuotantoaallot** \> **Kaikki tuotantoaallot**. Valitse toimintoruudussa **Tuotantoaalto**.
    - Valitse **Varastonhallinta** \> **Yhteiset** \> **Aallot** \> **Kanban-aallot** \> **Kaikki kanban-aallot**. Valitse toimintoruudussa **Luo aalto**.

1. Valitse aalto, jonka haluat käsitellä. Valitse toimintoruudussa **Käsittely**.

### <a name="release-the-wave-to-the-warehouse-to-start-picking-and-packing"></a>Vapauta aalto varastoon aloittaaksesi keräily ja pakkaus

Sinun on käsiteltävä aalto ennen kuin voit vapauttaa sen. Kun vapautat aallon, keräilytyö on käytettävissä varastossa. Voit peruuttaa aallon sen jälkeen, kun se on vapautettu, ja lisätä rivejä, mutta rivejä ei voi muuttaa.

#### <a name="automatically-release-a-wave"></a>Vapauta aalto automaattisesti

Jos haluat käsitellä aallon automaattisesti, määritä asianmukaiset [aaltomallit](wave-templates.md), joissa on tarvittavat automaattisen käsittelyn asetukset.

#### <a name="manually-release-a-wave"></a>Vapauta aalto manuaalisesti

Vapauta aalto manauaalisesti seuraavien ohjeiden avulla:

1. Tee jokin seuraavista riippuen vapautettavan aallon tyypistä:

      - Valitse **Varastonhallinta** \> **Yhteiset** \> **Aallot** \> **Lähetysaallot** \> **Kaikki aallot**. Valitse toimintoruudussa **Aalto**.
      - Valitse **Varastonhallinta** \> **Yhteiset** \> **Aallot** \> **Tuotantoaallot** \> **Kaikki tuotantoaallot**. Valitse toimintoruudussa **Tuotantoaalto**.
      - Valitse **Varastonhallinta** \> **Yhteiset** \> **Aallot** \> **Kanban-aallot** \> **Kaikki kanban-aallot**. Valitse toimintoruudussa **Luo aalto**.

1. Valitse aalto, jonka haluat vapauttaa. Valitse toimintoruudussa **Vapauta aalto**.

## <a name="containerize-a-wave"></a>Aallon konttiinpakkaus

Automaattinen konttiin pakkaus luo kontit ja keräilytyön lähetyksille aallon käsittelyn yhteydessä. Lisätietoja sen määrittämisestä on kohdassa [Konttiinpakkaus](wave-containerization.md).

## <a name="work-with-the-scheduled-work-creation"></a>Ajoitetun työn luomisen käsittely

Kun *Aikatauluta työn luonti* -toiminto on otettu käyttöön, aaltokäsittely luo suunnitellun työn, jota uuden työn luontiprosessi käyttää jossain vaiheessa. Työ estetään työn luonnin aikana *Organisaation laajuinen työn esto* -toiminnolla. Lisätietoja on kohdassa [Työn luonnin aikatauluttaminen aallon aikana](configure-wave-schedule-work-creation.md).

Seuraava vuokaavio osoittaa, miten suunniteltu työ luodaan aaltokäsittelyn aikana.

![Ajoita työn luonti.](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Suunniteltu työ

**Suunnitellun työn tiedot** -sivulla (**Varastonhallinta \> Työ \> Suunnitellun työn tiedot**) on tietoja suunnitellusta työstä, joka luotiin ensin aaltokäsittelyn aikana. Seuraavat **Prosessin tila** -arvot ovat käytettävissä:

- **Asetettu jonoon** – suunniteltu työ odottaa, että sitä käytetään työn luontiin.
- **Valmis** – suunniteltua työtä on käytetty työn luontiin.
- **Epäonnistui** – Aaltokäsittely on epäonnistunut. Huomaa, että suunnitellun työn tila voi olla **Epäonnistui** riippumatta siitä, onko sillä liittyvää varsinaista työtä. Kun varsinaisen työn luontiprosessi epäonnistuu, varsinaisen työn tilaksi jää *Peruutettu*.

### <a name="batch-job-for-the-work-creation-process"></a>Työn luontiprosessin erätyö

Käsittelyaaltojen erätöitä voi tarkastella valitsemalla **Kaikki aallot** -sivun toimintoruudussa **Erätyöt**.

Tällä tavoin voi tarkastella kunkin erätyötunnuksen kaikki erätehtävän tietoja.

## <a name="cancel-a-wave"></a>Aallon peruuttaminen

Tarvittaessa voit peruuttaa aallon, joka on käsitelty. Voit peruuttaa aallon ja luodun keräilytyön seuraavasti:

1. Tee jokin seuraavista riippuen peruutettavan aallon tyypistä:

      - Valitse **Varastonhallinta** \> **Yhteiset** \> **Aallot** \> **Lähetysaallot** \> **Kaikki aallot**.
      - Valitse **Varastonhallinta** \> **Yhteiset** \> **Aallot** \> **Tuotantoaallot** \> **Kaikki tuotantoaallot**.
      - Valitse **Varastonhallinta** \> **Yhteiset** \> **Aallot** \> **Kanban-aallot** \> **Kaikki kanban-aallot**.

1. Valitse aalto, jonka haluat peruuttaa. Valitse toimintoruudun **Työ**-välilehdessä **Peruuta**.

## <a name="review-wave-batch-job-details"></a>Aallon eräajon tietojen tarkasteleminen

**Aallon eräajon tiedot** -sivulla voit tarkastella erätöitä ja mihin tahansa aaltoon liittyviä tehtäviä. Tästä on hyötyä erityisesti epäonnistuneen aallon vianmäärityksessä. Jos tätä toimintoa ei ole, vain järjestelmänvalvojilla on yleensä erätyön tietojen käyttöoikeus. **Aallon eräajon tiedot** -sivu voidaan antaa muiden kuin järjestelmänvalvojien käyttöön, ja siinä voi tarkastella vain luku -tilassa erätöitä ja niihin liittyviä tehtäviä.

### <a name="turn-the-wave-batch-job-details-page-on-or-off"></a>Ota Aallon eräajon tiedot -sivu käyttöön tai pois käytöstä

Supply Chain Managementin versiosta 10.0.25 alkaen **Aallon erätyön tiedot** -sivu on oletusarvoisesti käytössä. Järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Aallon erätyön tiedot* -toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

### <a name="use-the-wave-batch-job-details-page"></a>Käytä Aallon eräajon tiedot -sivua

**Aallon eräajon tiedot** -sivulla erätyöt ja erätyötehtävät yhdistetään. Tämän avulla voit tutkia kaikkia aallon vaiheita tarvitsematta siirtyä takaisin ja edestakaisin yksittäisen erätyön ja erätehtäväluettelon välillä. Sivulla on myös erälokin käyttöoikeus, ja jos sinulla on tarvittavat käyttöoikeudet, voit avata linkin **Erätyöt**-sivulle.

Voit avata sivun valitsemalla aallon miltä tahansa eri aaltosivulta ja valita sitten toimintoruudusta **Aallon eräajon tiedot**.

## <a name="review-load-validation-and-error-messages"></a>Tarkista kuormituksen oikeellisuustarkistus ja virhesanomat

Järjestelmä tarkistaa kunkin kuormitusrivin tilan ja näyttää tilan aallon käsittelyn aikana. Jos varoituksia ei tule, se jatkaa seuraavaan aallon vaiheeseen. Jos varoituksia tapahtuu, järjestelmä näyttää sen sijaan seuraavan virheen sen jälkeen, kun koko aallon tarkistus on valmis:

> Aallosta löytyi virheellisiä kuormitusrivejä. Poista virheelliset kuormitusrivit.

Tämän jälkeen voit tarkistaa aallon kunkin kuormitusrivin lopullisen tilan ja korjata kaikki varoitukset ennen uudelleen yrittämistä. Näin voit käsitellä kaikki varoitukset kerralla ennen aallon uudelleenkäsittelyä. (Aiemmissa versioissa järjestelmä lopetti aallon käsittelyn ensimmäisen varoituksen jälkeen, joten varoituksia pysyi korjaamaan vain yhden kerrallaan.)

Tapa, jolla järjestelmä näyttää aallon käsittelytilan sanomat, määräytyy sen mukaan, miten **Varastonhallinnan parametrit** -sivulla on määritetty **Luo aallon käsittelyhistorian loki** -asetus.

- Kun **Luo aallon käsittelyhistorian loki** -asetus on *Ei*, **infolokissa** näkyvät kuormitusrivin tilasanomat.
- Kun **Luo aallon käsittelyhistorian loki** -asetus on *Kyllä*, **Aallon käsittelyhistorian loki** -sivulla näkyvät kuormitusrivin tilasanomat. Jos haluat tarkastella lokia, siirry kohtaan **Varastonhallinta \> Lähtevät aallot \> Aallon käsittelyhistorian loki**.

## <a name="additional-resources"></a>Lisäresurssit

- [Aaltokäsittelyn konfiguroinnin esimerkki](tasks/configure-wave-processing.md)
- [Aaltomallit](wave-templates.md)
- [Konttiinpakkaus](wave-containerization.md)