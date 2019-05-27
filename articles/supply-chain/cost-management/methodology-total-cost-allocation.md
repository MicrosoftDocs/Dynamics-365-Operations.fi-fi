---
title: Kokonaiskustannusten kohdistustapa
description: Tämä ohjeaihe sisältää kokonaiskustannusten kohdistuksen käyttöön liittyviä ohjeita. Kokonaiskustannusten kohdistus on menetelmä, jolla lasketaan erätilauksen pääreseptinimikkeen ja reseptille määritettyjen oheistuotteiden välinen kustannus.
author: AndersGirke
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, PmfFormulaCoBy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83852
ms.assetid: 7c14c3e5-9476-4a79-a210-e77fc91cc7fc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cda1c5251b81a3bb73d4d8703d7c3fa1ab4e9c16
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546725"
---
# <a name="total-cost-allocation-method"></a>Kokonaiskustannusten kohdistustapa

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe sisältää kokonaiskustannusten kohdistuksen käyttöön liittyviä ohjeita. Kokonaiskustannusten kohdistus on menetelmä, jolla lasketaan erätilauksen pääreseptinimikkeen ja reseptille määritettyjen oheistuotteiden välinen kustannus.

Kokonaiskustannusten kohdistus on menetelmä, jolla lasketaan erätilauksen pääreseptinimikkeen ja reseptille määritettyjen oheistuotteiden välinen kustannus. Menetelmä on dynaaminen. Se laskee kustannukset reseptinimikkeen valmiiksi ilmoitettujen määrien ja oheistuotteiden välisenä painotettuna keskiarvona. Kokonaiskustannusten kohdistusta käytetään kunkin erätilauksen kustannusten kohdistuksen tarkistamiseen. Jos kokonaiskustannusten kohdistusta ei käytetä, reseptin laskennassa käytetään olemassa olevaa toimintoa.

## <a name="using-tca-for-coproducts"></a>Kokonaiskustannusten kohdistuksen käyttäminen oheistuotteille
Seuraavassa on muutamia ohjeita, jotka liittyvät kokonaiskustannusten kohdistuksen käyttämiseen oheistuotteiden yhteydessä:

-   Jos reseptiversion **Kokonaiskustannusten kohdistus** -liukusäädin asetetaan arvoon **Kyllä**, oheistuotteilla on oltava kustannushinta, joka on suurempi kuin nolla (0). Arvo voidaan hakea aktiivisesta kustannuslaskelmaversiosta samalle toimipaikalle tai muun kuin toimipaikkakohtaisen reseptin ensimmäiselle toimipaikalle. Ehto tarkistetaan reseptin hyväksymisen yhteydessä.

    -   Oheistuotteille ei tarvitse syöttää kustannusten kohdistusprosentteja käsin. Järjestelmä luo sen sijaan kustannusten kohdistusprosentin automaattisesti oheistuotteiden aktiivisten kustannushintojen keskiarvosta. 
    -   Vakiokustannusta ei tarvitse täyttää ei-vakiokustannuksellisille nimikkeille, jotka ovat oheistuotteita. Järjestelmässä on kaksi erilaista kustannuslaskentaversiota: vakiokustannus ja suunniteltu kustannus 
    -   Jos nimikettä ei arvosteta vakiokustannuksen arvostustavalla, suosittelemme, että käytät suunnitellun kustannusversion aktiivista kustannushintaa. Tätä hintaa käytetään kustannusten arvioinnissa, esimerkiksi tuoterakennelaskelmissa, tuotantokustannusarvioissa ja varahinnoissa varaston arvostusprosessin aikana. 

-   Jos reseptiversion **Kokonaiskustannusten kohdistus** -liukusäädin asetetaan arvoon **Kyllä** ja seuraavat ehdot toteutuvat, kustannusten kohdistusmenetelmä on **Kokonaiskustannusten kohdistus** ja kustannusten kohdistuksen prosentti pysyy ennallaan:
    -   Olet lisännyt oheistuotteita.
    -   Olet käyttänyt oheistuotteille eri kustannusten kohdistusmenetelmää.
-   Jos reseptiversion **Kokonaiskustannusten kohdistus** -liukusäädin asetetaan arvoon **Ei** ja seuraavat ehdot toteutuvat, kustannusten kohdistusmenetelmäksi muutetaan **Manuaalinen** ja kustannusten kohdistuksen prosentti pysyy ennallaan:
    -   Olet lisännyt oheistuotteita.
    -   Kustannusten kohdistuksen prosentti on suurempi kuin 0 (nolla).
-   Kustannusten kohdistuksen prosentit on arvioitava, ennen kuin voit suorittaa reseptin laskennan. Voit suorittaa tämän vaiheen manuaalisesti tai käyttämällä **Arvioi kustannukset** -vaihtoehtoa **Oheistuotteet**-sivulla. **Huomautus:** **Arvioi kustannukset** -vaihtoehto on käytettävissä vain, kun reseptiversion **Kokonaiskustannusten kohdistus** -liukusäätimen arvoksi on asetettu **Kyllä**. Voit tarkastella odotettua kohdistusta, jos valmiiksi ilmoitetut erätilausmäärät vastaavat reseptissä näkyviä määriä.
-   Kun erätilaus luodaan manuaalisesti tai suunniteltu erätilaus vahvistetaan, reseptiversion **Kokonaiskustannusten kohdistus** -liukusäätimen arvo kopioidaan erätilaukseen. Voit kuitenkin muuttaa asetusta erätilauksessa. Jos reseptiversion **Kokonaiskustannusten kohdistus** -liukusäätimen arvoksi on asetettu **Ei** ja erätilausta varten arvoksi valitaan **Kyllä**, niiden rivien, joiden kustannusten kohdistusmenetelmä on **Manuaalinen**, kustannusten kohdistusmenetelmäksi muutetaan **Kokonaiskustannusten kohdistus**. Kustannusten kohdistus **Ei mitään** ei muutu. Jos reseptiversion **Kokonaiskustannusten kohdistus** -liukusäätimen arvoksi on asetettu **Kyllä** ja erätilausta varten arvoksi valitaan **Ei**, **Tuotanto**-tyypin oheistuotteen kustannusten kohdistusmenetelmäksi muutetaan **Manuaalinen**. Kustannusten kohdistuksen arvioitu prosenttiosuus ei muutu.
-   **Oheistuotteen kustannusten kohdistus** -sivulla näkyy laskettu kustannusten kohdistusprosentti. Voit avata sivun **Erätilaus**-sivulta. Tiedot ovat hyödyllisiä silloin, kun raportoidut tuotteet ja määrät poikkeavat erätilauksen suunnitelluista tai aloitetuista määristä. Kun kustannus on valmis, uudet prosenttikohdistukset kokonaiskustannusten kohdistuksesta näkyvät **Oheistuotteen kustannusten kohdistus** -sivulla.

## <a name="calculating-the-burden-for-byproducts"></a>Sivutuotteiden Yk-lisän laskeminen
**Oheistuotteet**-sivun **Sivutuotteen kustannusten kohdistus** -kenttä on luettelointikenttä, jota käytetään vain sivutuotteille. Oheistuotteiden osalta tämän kentän arvo on aina **Ei mitään**. Sivutuotteiden osalta tämä kenttä määrittää, kuinka sivutuoterivin kustannussumma lisätään tuotannon kokonaiskustannuksiin. Valittavissa ovat seuraavat vaihtoehdot:

-   **Ei mitään** – Tuotannon kokonaiskustannuksiin ei lisätä summaa tämän sivutuoterivin osalta.
-   **Prosentti** – Kustannussumma lasketaan prosenttiosuutena tuotannossa käytettävien raaka-aineiden kokonaiskustannuksista. Tähän kenttään lisätään prosentti, jota käytetään laskennassa.
-   **Per sarja** – Kustannussumma lasketaan summana per tuotantotilauksen vakioeräkoko. Summa on riippumaton tuotannon raportoidusta määrästä. Tähän kenttään lisätään summa, jota käytetään laskennassa.
-   **Per määrä** – Kustannussumma lasketaan summana per tuotannon reseptinimikkeen raportoitu määrä. Tähän kenttään lisätään summa, jota käytetään laskennassa.




