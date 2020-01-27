---
title: Kyselylomakkeiden tulosten tarkasteleminen ja arvioiminen
description: Tässä aiheessa kerrotaan, miten vastaajien täyttämien kyselylomakkeiden tuloksia voidaan tarkastella ja arvioida.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 9c8c963fb2212df2dfa6e7f00ddd3e55e0749214
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898337"
---
# <a name="view-and-evaluate-the-results-of-questionnaires"></a>Kyselylomakkeiden tulosten tarkasteleminen ja arvioiminen

Tässä aiheessa kerrotaan, miten vastaajien täyttämien kyselylomakkeiden tuloksia voidaan tarkastella ja arvioida. 

Kun vastaajat ovat täyttäneet kyselylomakkeen, voit tarkastella ja arvioida kyselylomakkeen tuloksia seuraavilla tavoilla.

-   **Valmiit vastausistunnot** – Voit tarkastella kyselylomakkeen niitä tietoja, jotka vastaajat ovat täyttäneet, ja luoda yhteenvetoraportteja vastauksista ja saaduista pisteistä.
-   **Tulosryhmät** – Voit tarkastella kyselylomakkeiden tulosryhmän tietoja, kuten tilastotietoja. Tulosryhmän tilastotiedot voidaan luoda kyselylomakkeen yhdelle vastausistunnolle tai kaikille vastausistuinnoille.
-   **Kyselylomakkeen tilastotiedot** – Voit määrittää ehdot, joiden mukaan tietyn vastaajaryhmän tilastotiedot lasketaan.

Voit luoda erilaisia raportteja myös henkilön, vastausistunnon tai tulosryhmän mukaan lajiteltujen tulosten tarkastelemista varten. Käytettävissä ovat seuraavat täytettyihin kyselylomakkeisiin liittyvät raportit:

-   Vastaukset
-   Kyselylomakekohtaiset kysymykset
-   Henkilökohtaiset vastaukset
-   Palauteanalyysi

## <a name="answer-session-results"></a>Vastausistunnon tulokset
Kun vastaajat ovat täyttäneet kyselylomakkeen, voit tarkastella valmiiden vastausistuntojen tuloksia. Vastausistunto on yhden käyttäjän vastaus kyselylomakkeessa. Voit tarkastella valmiiden vastausistuntojen tietoja **Vastaukset**-sivulla. **Vastaukset**-sivun vastausistunnot suodatetaan eri tavoin riippuen siitä, miten sivu avataan.

-   Kaikki kyselylomakkeet
-   Tietty kyselylomake
-   Yksittäinen henkilö

**Vastaukset**-sivulla voit tarkastella vastausten, saatujen pisteiden, vastaajan vastauksia kussakin tulosryhmässä ja valitun kyselylomakkeen mahdollisen kysymyshierarkian tietoja. Voit myös luoda ja tulostaa seuraavat raportit:

-   **Tulosraportti** – Tämä raportti sisältää graafisen esityksen valitussa vastausistunnossa saaduista pisteitä tulosryhmää kohti.
-   **Vastausraportti** – Tämä raportti sisältää vastaajan kyselylomakkeen kuhunkin kysymykseen valitsemat vastaukset.
-   **Väärät vastaukset** – Tämä raportti sisältää vastaajan valitsemiin vääriin vastauksiin liittyvät tiedot.

> [!NOTE]
> **Tulokset**-raportti on käytettävissä vain, jos kyselylomakkeessa on käytetty tulosryhmiä ja jos **Kyselylomakkeet**-sivun **Tulokset**-sivu on valittu. **Vastausraportti** ja **väärien vastausten raportti** ovat käytettävissä vain, jos **Kyselylomakkeet**-sivun **vastausraportti** on valittu.

## <a name="questionnaire-statistics"></a>Kyselylomakkeen tilastotiedot
Voit käyttää kyselylomakkeen tilastotietoja, kun haluat analysoida täytettyjen kyselylomakkeiden tulokset määrittämiesi laskelmien perusteella. Voit määrittää laskelmat seuraavien tehtävien avulla.

-   Valitse tilastotietojen laskemisessa ja näyttämisessä käytettävät ehdot.
    -   Voit näyttää tilastotiedot kyselylomakkeen, kysymysten, kysymysrivien tai tulosryhmien mukaan.
    -   Valitse tulosten tarkastelemisessa käytettävä kaaviotyyppi.
    -   Valitse niiden verkkoon kuuluvien henkilöiden tyypit (työntekijä, yhteyshenkilö tai hakija), joiden vastaukset haluat ottaa mukaan. Voit ottaa mukaan myös nimettömästi täytettyjen kyselylomakkeiden vastaukset.
    -   Määritä tulosten analysoimista varten välit iän tai virkaiän perusteella.
-   Tässä välilehdessä voit valita ja tarkistaa tilastoitavan kohteen tarkentavia asetuksia. Esimerkiksi valitsemalla postinumeron voit analysoida kyseisellä postinumeroalueella olevien vastaajien tuloksia.
-   Valitse tai tarkista ehdot, kun haluat analysoida tulokset vastaajan tai kyselylomakkeen ominaisuuksien perusteella. Voit analysoida esimerkiksi vastaajan sijainnin ja oikeiden vastausten välisen korrelaation valitsemalla **Postinumero**.

Määrittämäsi asetukset tallennetaan ja niitä voidaan käyttää tulosten kausittaiseen uudelleenlaskemiseen.

<a name="additional-resources"></a>Lisäresurssit
--------

[Kyselylomakkeiden suunnitteleminen](design-questionnaires.md)

[Kyselylomakkeet](questionnaires.md)

[Kyselylomakkeiden jakelu ja aikataulutus](distribute-questionnaires.md)

