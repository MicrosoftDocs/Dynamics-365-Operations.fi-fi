---
title: Tuotantorakenne- ja reseptirivien vapauttaminen varastoon
description: Tässä ohjeaiheessa käsitellään tuoterakennerivien ja reseptirivien raaka-aineiden varastoon vapauttamisprosessia.
author: johanhoffmann
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 8ccdb71f49652d6cca6ced2e9e9764d9ad0fffd8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552904"
---
# <a name="release-bom-and-formula-lines-to-the-warehouse"></a>Tuotantorakenne- ja reseptirivien vapauttaminen varastoon

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään tuoterakennerivien ja reseptirivien raaka-aineiden varastoon vapauttamisprosessia. Kun vapautat tuoterakenne- tai reseptirivin varastoon, järjestelmä määrittää ensin, onko materiaalia jo saatavana työnohjauksessa tuotannon syöttösijainnissa, jossa tuotantoprosessi kuluttaa materiaalin.

- Jos materiaalia on saatavana tuotannon syöttösijainnissa, se kerätään kyseisestä sijainnista heti, kun signaali materiaalin vapauttamisesta varastoon on annettu.
- Jos materiaalia ei ole saatavana tuotannon syöttösijainnissa, materiaalin vapautus ilmaisee, että materiaali on siirrettävä varastosijainneista tuotannon syöttösijaintiin. Materiaali siirretään raaka-aineiden keräilyn varastotyön kautta. Tämän vuoksi raaka-aineiden varastoprosessit on määritettävä. Lisätietoja on kohdissa [Täydennys](../warehousing/replenishment.md) ja [Varastotyön valvonta työmallien ja sijaintidirektiivien avulla](../warehousing/control-warehouse-location-directives.md).

## <a name="methods-for-releasing-bom-and-formula-lines"></a>Tuoterakenne- ja reseptirivien vapauttamistavat

Voit määrittää tuoterakenne- ja reseptirivien vapauttamisen osaksi tuotanto- tai erätilauksen vapauttamista. Vaihtoehtoisesti myös erätyö voi hallita vapautusta tai se voidaan tehdä manuaalisesti.

Tuotantorakenne- ja reseptirivien vapautustapaa hallitaan **Tuotantorivin vapautus** -parametrilla. Pääset parametriin valitsemalla **Tuotannonhallinta** \> **Asetukset** \> **Tuotantoparametrit**.

- **Vapauta tuoterakenne- ja reseptirivit osana tuotanto- tai erätilauksen vapautusta** – Tässä menetelmässä tuotanto- tai erätilauksen tuoterakenne- tai reseptirivit vapautetaan osan tilauksen vapautusprosessia. Tuotantotyöt vapautetaan yleensä tuotanto- tai erätilauksen vapautuksen yhteydessä tuotantotyöntekijöille. Lisäksi tuotantoasiakirjat tulostetaan. Tilauksen tilaksi tulee tämän prosessin aikana **Vapautettu**.
- **Vapauta tuoterakenne- ja reseptirivit erätyön avulla tai manuaalisesti** – Tässä tavassa tuoterakenne- ja reseptirivit vapautetaan vain **Tuoterakenteen ja reseptirivien automaattinen vapautus** -erätyön avulla tai manuaalisesti. Voit vapauttaa tuoterakenne- ja reseptirivejä manuaalisesti valitsemalla tuotantotilauksen luettelosivulla tai tuotantotilauksen tietosivulla toimintoruudussa **Vapauta varastoon**.

Seuraavassa lyhyessä YouTube-videossa näytetään, miten tuorerakenne- ja reseptirivit vapautetaan tuotantoon erätyön avulla: [Tuotannon keräilyn vapautus eränä varastoon](https://www.youtube.com/watch?v=8urAJn50dQ8).

## <a name="releasing-the-bom-and-formula-lines-by-using-a-batch-job"></a>Tuoterakenne- ja reseptirivien vapauttaminen erätyön avulla

**Tuoterakenne- ja reseptirivien automaattinen vapautus** -erätyö käsittelee valitut tuoterakenne- ja reseptirivit, joiden jäljellä olevan määrän voi vapauttaa. Työ ottaa huomioon vain tilaukset, joiden tila on **Vapautettu**, **Aloitettu** tai **Ilmoitettu valmiiksi**. Jos tuoterakenne- tai reseptirivillä on jäljellä vapautettavaa, työ vapauttaa enintään määrän, jonka jo fyysisesti varattu määrä ja fyysisesti saatavana oleva määrä kattaa.

### <a name="example-of-a-batch-job-release"></a>Erätyön vapautusesimerkki

| Skenaario | Jäljellä oleva vapautettava määrä | Varattu fyysinen määrä | Käytettävissä oleva fyysinen määrä | Erätyön vapauttama määrä |
|----------|-------------------------------|------------------------------|-------------------------------|------------------------------------|
| 1        | 100                           | 20                           | 90                            | 100                                |
| 2        | 100                           | 20                           | 70                            | 90                                 |
| 3        | 100                           | 0                            | 90                            | 90                                 |
| 4        | 100                           | 0                            | 110                           | 100                                |
| 5        | 100                           | 20                           | 0                             | 20                                 |

### <a name="batch-job-setup"></a>Erätyön asetukset

Voit määrittää **Tuoterakenteen ja reseptirivien automaattinen vapautus** -erätyön kyselyssä suodatusehdot määrittämään, kuinka monta päivää eteenpäin työn on haettava rivejä, joilla on vapauttamattomia määriä. Käytä työn kyselyssä suodatusehtona **Raaka-aineen päivämäärä** -kentässä **(LessThanDate())**-funktiota.

Seuraavan kuvan tuotantotilauksessa on kaksi työtä, 10 ja 20, jotka kattavat tuotantotilauksen kokoonpanon ja pakkauksen. Kumpikin työ on määritetty kuluttamaan tietty määrä materiaalia. Tässä kuvassa vapautuksen aikarajan ilmaiseva aikajanan alla oleva vihreä nuoli on sama **(LessThanDate())**-ehdoissa määritetty päivien määrä. Esimerkiksi **(LessThanDate(2))** ilmaisee, että työn on haettava vapauttamattomia määriä vain kahden päivän aikarajan ajalta.

![Esimerkki kaksi erätyötä sisältävästä tuotantotilauksesta](media/bach-job-setup.PNG)

## <a name="releasing-material-per-operation-number-or-in-proportion-to-the-amount-of-finished-goods"></a>Materiaalin vapauttaminen työvaiheen numeron mukaan tai suhteessa valmiiden tavaroiden määrään

Jos vapautat materiaaleja **Tuotantotilauksen vapauttamisen yhteydessä** -parametriasetuksella manuaalisen vapautuksen yhteydessä, sinulla on kaksi vaihtoehtoa materiaalin vapautuksen hallintaan:

- Materiaalin vapauttaminen työvaiheen numeron mukaan.
- Materiaalin vapauttaminen suhteessa valmiiden tavaroiden määrään.

### <a name="release-material-per-operation-number"></a>Materiaalin vapauttaminen työvaiheen numeron mukaan

Voit hallita työvaiheita, joihin materiaali on vapautettava, **Vapauta varastoon** -sivulla.

- Valitse ensin **Tuotannonhallinta** \> **Tuotantotilaukset** \> **Kaikki tuotantotilaukset**, sitten tuotantotilaus ja lopuksi **Varasto**-välilehdessä **Vapauta varastoon**. Määritä sen jälkeen **Työvaihenumerosta**- **Työvaihenumeroon**-kentissä työvaihenumeroalue.

Seuraavan kuvan tuotantotilauksessa on kaksi työvaihetta, 10 ja 20. Jos rajoitat tässä esimerkissä vapautuksen työvaiheeseen 10, vain materiaali M9203 vapautetaan.

![Esimerkki materiaalin vapauttamisesta työnumeron mukaan](media/two-operations.PNG)

Tässä lyhyessä YouTube-videossa näytetään, miten materiaali vapautetaan suhteessa valmiiden tuotteiden määrään: [Tuotantotilauksen vapautusprosessin parannukset Dynamics 365 for Finance and Operationsissa](https://www.youtube.com/watch?v=Rm3ojAz6Zu0)

### <a name="release-material-in-proportion-to-the-amount-of-finished-goods"></a>Materiaalin vapauttaminen suhteessa valmiiden tavaroiden määrään

Voit vapauttaa raaka-aineen osittaista valmiiden tavaroiden määrää varten tai tiettynä yksikkönä.

- Voit vapauttaa raaka-aineen osittaista valmiiden tavaroiden määrää varten valitsemalla ensin **Tuotannonhallinta** \> **Tuotantotilaukset** \> **Kaikki tuotantotilaukset**, sitten tuotantotilaus ja lopuksi **Varasto**-välilehdessä **Vapauta varastoon**. Anna sitten määrä **Määrä**-kenttään.

    Esimerkki: 1 000 kappaleen (kpl) tuotantotilaus luodaan ja ajoitetaan. Tuotannon valvoja suunnittelee 100 kpl:n tuotannon. seuraavalle vuorolle ja haluaa vapauttaa materiaalit vain kyseiselle vuorolle. Tässä tapauksessa valvoja voi käyttää **Määrä**-kenttää vapauttamaan materiaalit niille 100 kappaleelle, jotka on suunniteltu seuraavaa vuoroa varten.

- Voit vapauttaa raaka-aineen tietyn yksikön valitsemalla ensin **Tuotannonhallinta** \> **Tuotantotilaukset** \> **Kaikki tuotantotilaukset**, sitten tuotantotilaus ja lopuksi **Varasto**-välilehdessä **Vapauta varastoon**. Valitse sitten **Yksikkö**-kentässä valmiin tavaran yksikkö, jolle materiaali vapautetaan.

    Käytettävissä olevat yksiköt määritetään valmiin tuotteen yksikön sarjaryhmässä.

    Esimerkki: valmiin tavaran yksikön muunto kilogrammojen (kg) ja kuormalavojen (KL) välillä on 1 KL = 100 kg. Jos haluat luoda tuotantotilauksen 10 000 kg:lle valmista tavaraa, voit vapauttaa raaka-aineet sille kuormalavamäärälle, jonka aiot tuottaa. Valitse ensin yksiköksi **KL** ja sitten vastaava luku **Määrä**-kentässä.
