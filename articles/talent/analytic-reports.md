---
title: Analyysiraporttien käyttäminen Microsoft Dynamics 365 Talent – Attractissa
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent – Attractin työhönottoprosessin merkityksellisten tietojen analyysiraportteja
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: be62fe9a5021cfa83a465d316b182c0a154c0c50
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010005"
---
# <a name="use-analytic-reports"></a>Analyysiraporttien käyttäminen

Microsoft Dynamics 365 Talent: Attractin analyyttiset raportit tarjoavat OOTB-ratkaisun työhönottoprosessin merkityksellisille tiedoille. Käytettävissä olevia ominaisuuksia ovat:

- **Työn analytiikka** Napsauta työpaikan hakijoiden mittarit **Analytiikka**-välilehdessä.
- **Analyysikeskus:** Valitse **Analyysit** vasemmanpuoleisesta siirtymispalkista, kun haluat yhdistää eri töiden metriikat.
- **Käyttäjäkohtaiset käyttöoikeudet:** Attractin [roolin](security-attract.md) hallitsemien raporttien käyttäminen ja työn osallistujarooli.
- **Ristiinsuodatus:** Valitse raportissa visualisointi, jos haluat tarkastella muita valittujen tietojen mukaan suodatettuja mittareita.

>[!NOTE] 
>- Tämä ominaisuus on tällä hetkellä vain [esiversiossa](access-preview-feature.md). Jos haluat kokeilla sitä, sinulla on oltava [**kattava työhönottolisäosa**](attract-comprehensive-hiring.md).
>- Kaikki julkiset esikatseluraportit näkyvät englanniksi.
>- Raportit päivitetään joka kolmas tunti. Viimeisin päivitysaika (paikallisessa aikavyöhykkeessä) sijaitsee raportin yläosassa. Päivitysajat ovat likiarvo ja vaihtelevat alueen tietojen määrän ja resurssien kuormituksen mukaan.

## <a name="job-analytics"></a>Työn analytiikka

Työn analytiikka -raportit ovat tilannekuva työn työhönottoprosessista.  Tärkeimpiä mittareita ovat seuraavat:

- Aktiiviset hakijat vaiheen mukaan
- Hakijalähde
- Hakijan tyyppi (sisäinen tai ulkoinen)

## <a name="analytics-hub"></a>Analytiikkakeskus

Analytiikkakeskus raportoi eri töistä kerätyt tiedot, mikä auttaa löytämään työhönottoprosessin trendejä. Attract sisältää kaksi OOTB-raporttia: putken yhteenveto ja kanava-analyysi.

### <a name="pipeline-summary"></a>Putken yhteenveto

Putken yhteenvetoraportti kokoaa avoimien töiden tiedot. Tärkeimpiä mittareita ovat seuraavat:

- Kaikkien työpaikkojen hakijat vaiheen mukaan
- Hakijalähde
- Avoimet työpaikat virkaikätason mukaan

### <a name="funnel-analysis"></a>Kanava-analyysi

Kanava-analyysiraportti kokoaa tiedot täytettyjen töiden osalta. Tärkeimpiä mittareita ovat seuraavat:

- Palkkausaika
- Muuntomittarit (valittaessa osoittamalla)
- Tarjouksen hyväksymisprosentti

Huomautus: kun haluat käyttää raportoinnissa mahdollisimman tarkkaa aikaa, suosittelemme, että käytät [tarjouksen hallinta](offer-setup.md) -toimintoa, joka on käytettävissä osana kattavaa työhönottolisäosaa.

>[!TIP] 
>Saat lisätietoja viemällä osoittimen grafiikkakohdan päälle. Jos esimerkiksi viet osoittimen **aktiivisten hakijoiden** päälle, näytössä näkyy keskimääräiset päivät vaiheessa. Näiden tietojen analysointi voi antaa tärkeitä tietoja, joiden avulla työhönottoaikaa voidaan vähentää ja jotta rekrytoijat voivat keskittyä eri vaiheissa käytetyn ajan lyhentämiseen.

## <a name="user-specific-security"></a>Käyttäjäkohtainen turvallisuus

Attract-raportit ovat käytettävissä järjestelmänvalvoja-, lue kaikki-, rekrytoija-, ja vuokrauspäällikkö[rooleille](security-attract.md). Jos käyttäjälle ei ole määritetty roolia, hän ei voi käyttää kumpaakaan analyysiraporttisivua (Työn analytiikka tai Analytiikkakeskus).

Työn analytiikka -raportti esittää tietoja valitusta työstä. Analyysikeskus raportoi koostettuja tietoja kaikista töistä, joita käyttäjä voi tarkastella. Käyttäjät, jotka voivat tarkastella työsivun sekä omat työt- että kaikki työt -sivua, käyttävät samoja näkymiä analyysikeskuksessa.

## <a name="cross-filter"></a>Ristiinsuodatin

Yksi Power BI -järjestelmän suurista ominaisuuksista on se, miten kaikki raporttisivun visualisoinnit ovat yhteydessä toisiinsa. Jos valitset tietopisteen jostakin visuaalista, kaikki muut sivun visualisoinnit, jotka sisältävät kyseisen tiedon muutoksen, perustuvat kyseiseen valintaan. Lue lisää ja katso esimerkki siitä [miten visualisoinnit ristiinsuodattavat toisensa Power BI -raportissa.](https://docs.microsoft.com/power-bi/consumer/end-user-interactions)

## <a name="export-to-excel"></a>Vie Exceliin

Jos haluat tarkastella raportin tietoja Excelissä, voit napsauttaa asetukset-valikkoa (kolme pistettä) visuaalisessa näkymässä ja valita **vie pohjana olevat tiedot**. Viedyt tiedot viedään suodatettuina ja niiden käyttöoikeudet otetaan huomioon Attractissa. Lisätietoja on kohdassa [tietojen vieminen visualisoinnin](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data)avulla.
