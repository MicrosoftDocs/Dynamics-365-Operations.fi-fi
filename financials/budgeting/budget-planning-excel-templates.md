---
title: Excelin budjettisuunnittelumallit
description: "Tässä aiheessa kuvataan, miten luodaan Microsoft Excel -malleja, joita voidaan käyttää budjettisuunnitelmissa."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 9f8073a2eb0d1b61d6a168f43eba983d113cf453
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Excelin budjettisuunnittelumallit
<a id="budget-planning-templates-for-excel" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan, miten luodaan Microsoft Excel -malleja, joita voidaan käyttää budjettisuunnitelmissa.

Tässä ohjeaiheessa kuvataan, miten luodaan Excel-malleja, joita käytetään budjettisuunnitelmissa käyttämällä vakionäytetietoja ja Järjestelmänvalvoja-käyttäjätunnusta. Saat lisätietoja budjettisuunnittelusta artikkelista [Budjetin suunnittelun yhteenveto.](budget-planning-overview-configuration.md) Voit myös seurata [Budjettisuunnittelun perusteet](budget-plan.md) -opetusohjelma oppiaksesi perustiedot moduulin määrityksestä sekä käytön periaatteet.

## Luo laskentataulukko budjettisuunnitelman asiakirja-asettelun avulla
<a id="generate-a-worksheet-using-budget-plan-document-layout" class="xliff"></a>
Budjettisuunnitelma-asiakirjoja voi tarkastella ja muokata käyttämällä yhtä tai useampaa asettelua. Kussakin asettelussa voi olla liitetty budjettisuunnitelman asiakirjamalli, jotta budjettisuunnitelman tietoja voidaan tarkastella ja muokata Excel-laskentataulukossa. Tässä ohjeaiheessa luodaan budjettisuunnitelman asiakirjamalli käyttämällä valmista asettelumääritystä. Avaa **Budjettisuunnitelmien luettelo** (**Budjetointi**&gt; **Budjettisuunnitelmat**). Luo uusi budjettisuunnitelma-asiakirja valitsemalla **Uusi**. [![bpt1](./media/bpt11-1024x552.png)](./media/bpt11.png) 

Käytä **Lisää rivi** -vaihtoehtoa, jos haluat lisätä rivejä. Voit tarkastella budjettisuunnitelman asiakirjan asettelun määrityksiä valitsemalla **Asettelut**. 
[![bpt2](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Voit tarkistaa asettelun määritykset ja muuttaa niitä tarvittaessa. Siirry kohtaan **Malli** &gt; **Luo** luodaksesi Excel-tiedoston tälle asettelulle. Kun malli on luotu, siirry kohtaan **Malli** &gt; **Näytä** avataksesi ja tarkistaaksesi budjettisuunnitelman asiakirjamallin. Voit tallentaa Excel-tiedoston paikalliseen asemaan. [![bpt3](./media/bpt3-1024x545.png)](./media/bpt3.png) 

> [!NOTE] 
> Budjettisuunnitelman asiakirjan asettelua ei voi muokata, kun Excel-malli on liitetty siihen. Voit muokata asettelua, poistamalla liitetyn Excel-mallitiedoston ja luomalla se uudelleen. Tämä tarvitaan pitämään asettelun kentät ja laskentataulukko synkronoituna. 

Excel-malli sisältää budjettisuunnitelman asiakirja-asettelun kaikki osat, joiden **Käytettävissä työkirjassa** -sarakkeen arvo on Tosi. Excel-mallissa ei sallita päällekkäisiä osia. Esimerkiksi jos asettelu sisältää sarakkeet Request Q1, Request Q2, Request Q3 ja Request Q4 sekä summasarakkeen, joka edustaa kaikkien neljän neljännesvuosittaisen sarakkeen summaa, vain neljännesvuosittaisia sarakkeita tai summasaraketta voidaan käyttää Excel-mallissa. Excel-tiedosto ei voi päivittää päällekkäisiä sarakkeita päivityksen aikana, koska taulukon tiedoista voi tulla vanhentuneita tai virheellisiä.

[![bpt4](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Voit välttää mahdollisia ongelmia budjettisuunnitelman tietojen tarkastelemisessa ja muokkaamisessa Excelissä, jos sama käyttäjä on kirjautunut sekä Microsoft Dynamics 365 for Finance and Operations, Enterprise Editioniin että Microsoft Dynamics Office -apuohjelman Data Connectoriin.

## Otsikon lisääminen budjettisuunnitelman asiakirjamalliin
<a id="add-a-header-to-budget-plan-document-template" class="xliff"></a>
Jos haluat lisätä otsikkotietoja, valitse ylin rivi Excel-tiedostossa ja lisää tyhjiä rivejä. Lisää otsikkokentät Excel-tiedostoon valitsemalla **Rakenne** **Data Connector** -sovelluksessa.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

Valitse **Rakenne**-välilehdessä,** ****Lisää kenttiä** ja sitten **BudgetPlanHeader** yksikön tietolähteeksi.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Siirrä kohdistin Excel-tiedostossa haluamaasi paikkaan. Valitse **Lisää otsikko** lisätäksesi kentän otsikon valittuun sijaintiin. Valitse **Lisää arvo** lisätäksesi arvokentän valittuun paikkaan. Valitse **Valmis** sulkeaksesi suunnitteluohjelman.

## [![bpt7](./media/bpt7.png)](./media/bpt7.png)
<a id="bpt7mediabpt7pngmediabpt7png" class="xliff"></a>

Lasketun sarakkeen lisääminen budjettisuunnitelman asiakirjamallin taulukkoon
<a id="add-a-calculated-column-to-budget-plan-document-template-table" class="xliff"></a>
--------------------------------------------------------------

Seuraavaksi, lasketut sarakkeet lisätään muodostettuun budjettisuunnitelman asiakirjamalliin. **Total Request** -sarake, joka summaa sarakkeet Request Q1 – Request Q4 ja **Oikaisu**-sarakkeen, joka laskee **Total request** -sarakkeen esimääritetyn kertoimen avulla.

Lisää sarakkeet taulukkoon valitsemalla **Rakenne** **Data Connector** -sovelluksessa. Valitse **Muokkaa** **BudgetPlanWorksheet**-tietolähteen vieressä aloittaaksesi sarakkeiden lisäämisen.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Valittu kenttäryhmää näyttää mallissa käytettävissä olevat sarakkeet. Valitse **Kaava**, kun haluat lisätä uuden sarakkeen. Nimeä uusi sarake ja liitä sitten kaava **Kaava**-kenttään. Valitse **Päivitä**, jos haluat lisätä sarakkeen.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Luo kaava laskentataulukossa ja kopioi se **Rakenne**-ikkunaan määrittääksesi kaavan. Finance and Operationsin sidottu taulukko nimeksi annetaan yleensä AXTable1. Jos esimerkiksi haluat summata laskentataulukossa sarakkeet Request Q1 – Request Q4, kaava on: AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].

Toista nämä vaiheet lisätäksesi **Oikaisu**-sarakkeen. Käytä tälle sarakkeelle kaavaa = AxTable1\[Total request\]\*$I$1. Tämä ottaa solun I1 arvon ja kertoo **Total request** -sarakkeen laskeakseen oikaisusummat.

Tallenna ja sulje Excel-tiedosto. Palaa Finance and Operationsiin ja lataa budjettisuunnitelmassa käytettävä tallennettu Excel-malli valitsemalla **Asettelu**-kohdassa **Malli &gt; Lataa**. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Sulje **Asettelut**-liukusäädin. Valitse **Budjettisuunnitelma**-asiakirjassa **Työkirja**, jolloin voit tarkastella ja muokata asiakirjaa Excelissä. Huomaa, että tämän budjettisuunnitelman työkirjan luomiseen käytettiin oikaistua Excel-mallia, ja lasketut sarakkeet päivitetään käyttäen kaavoja, jotka määritettiin edellisissä vaiheissa. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## Vinkkejä budjettisuunnitelman mallien luomiseen
<a id="tips--tricks-for-creating-budget-plan-templates" class="xliff"></a>
### Voinko lisätä ja käyttää muita tietolähteitä budjettisuunnitelman malliin?
<a id="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template" class="xliff"></a>

Kyllä, voit käyttää **Rakenne**-valikkoa lisätäksesi lisäyksikköjä samaan tai muihin taulukoihin Excel-mallissa. Esimerkiksi, voit lisätä **BudgetPlanProposedProject**-tietolähteen luodaksesi ja ylläpitääksesi ehdotettujen projektien luetteloa samaan aikaan kun työstät budjettisuunnitelman tietoja Excelissä. Huomaa, että suuren datamäärän tietolähteiden lisääminen saattaa heikentää Excel-työkirjan suorituskykyä. 

Voit käyttää **Suodatin** -vaihtoehtoa kohdassa **Data Connector** lisätäksesi haluamasi suodattimet muihin tietolähteisiin.

### Voinko piilottaa Rakenne-toiminnon Data Connectorissa muilta käyttäjiltä?
<a id="can-i-hide-the-design-option-in-the-data-connector-for-other-users" class="xliff"></a>

Kyllä, avaa **Data Connector** -asetukset piilottaaksesi **Rakenne**-vaihtoehdon muilta käyttäjiltä.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Laajenna **Data connector -asetukset** ja tyhjennä **Ota rakenne käyttöön** -valintaruutu. Tämä piilottaa **Rakenne**-asetuksen **Data connector** -kohdasta.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### Voinko estää käyttäjiä vahingossa sulkemasta Data Connectorin, kun he työstävät tietoja?
<a id="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data" class="xliff"></a>

Suosittelemme, että haluat estää käyttäjiä sulkemasta mallin lukitsemalla mallin. Voit määrittää lukituksen valitsemalla **Data connector** oikeassa yläkulmassa, jolloin näkyviin tulee nuoli. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Klikkaamalla nuolta näet lisävalikon. Valitse **Lukitse**.

### [![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)
<a id="bpt16mediabpt16-1024x614pngmediabpt16png" class="xliff"></a>

### voinko käyttää muita Excelin ominaisuuksia, kuten solun muotoilua, värejä, ehdollista muotoilua ja kaavioita omissa budjettisuunnitelmamalleissani?
<a id="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates" class="xliff"></a>

Kyllä, useimmat Excelin perusominaisuudet toimivat budjettisuunnitelmamalleissa. On suositeltavaa käyttää värikoodausta käyttäjille, jotta he erottavat Vain luku- ja muokattavat sarakkeet. Ehdollista muotoilua voi käyttää korostamaan budjetin ongelmallisia alueita. Sarakkeiden summat voidaan esittää helposti tavallisten Excel-kaavojen (taulukon yläpuolella) avulla.

Voit myös luoda ja käyttää pivot-taulukoita ja kaavioita budjetin tietojen ylimääräisiin ryhmittelyihin ja visualisointeihin. Valitse **Tiedot**-välilehden **Yhteydet**-ryhmässä **Päivitä kaikki** ja sitten **Yhteyden ominaisuudet**. Valitse **Käyttö**-välilehti. valitse kohdassa **Päivitä** **Päivitä tiedot, kun tiedosto avataan** -valintaruutu. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)




