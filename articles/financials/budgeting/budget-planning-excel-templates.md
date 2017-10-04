---
title: Excelin budjettisuunnittelumallit
description: "Tässä aiheessa kuvataan, miten luodaan Microsoft Excel -malleja, joita voidaan käyttää budjettisuunnitelmissa."
author: ryansandness
manager: AnnBe
ms.date: 07/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1945d137b337508a1850e3e679a60487aecb6b84
ms.openlocfilehash: 7cec40859a8c68cb8a9751c5531c67cef7706258
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---

# <a name="budget-planning-templates-for-excel"></a>Excelin budjettisuunnittelumallit

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan, miten luodaan Microsoft Excel -malleja, joita voidaan käyttää budjettisuunnitelmissa.

Tässä ohjeaiheessa kuvataan, miten luodaan Excel-malleja, joita käytetään budjettisuunnitelmissa käyttämällä vakionäytetietoja ja Järjestelmänvalvoja-käyttäjätunnusta. Saat lisätietoja budjettisuunnittelusta artikkelista [Budjetin suunnittelun yhteenveto.](budget-planning-overview-configuration.md) Voit myös seurata [Budjettisuunnittelun perusteet](budget-plan.md) -opetusohjelma oppiaksesi perustiedot moduulin määrityksestä sekä käytön periaatteet.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Luo laskentataulukko budjettisuunnitelman asiakirja-asettelun avulla

Budjettisuunnitelma-asiakirjoja voi tarkastella ja muokata käyttämällä yhtä tai useampaa asettelua. Kussakin asettelussa voi olla liitetty budjettisuunnitelman asiakirjamalli, jotta budjettisuunnitelman tietoja voidaan tarkastella ja muokata Excel-laskentataulukossa. Tässä ohjeaiheessa luodaan budjettisuunnitelman asiakirjamalli käyttämällä valmista asettelumääritystä. 

1. Avaa **Budjettisuunnitelmien luettelo** (**Budjetointi** &gt; **Budjettisuunnitelmat**). 
2. Luo uusi budjettisuunnitelma-asiakirja valitsemalla **Uusi**. 

  [![Budjettisuunnitelmaluettelo](./media/bpt11-1024x552.png)](./media/bpt11.png) 

3. Käytä **Lisää rivi** -vaihtoehtoa, jos haluat lisätä rivejä. Voit tarkastella budjettisuunnitelman asiakirjan asettelun määrityksiä valitsemalla **Asettelut**. 

  [![Budjettisuunnitelmien lisäys](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Voit tarkistaa asettelun määritykset ja muuttaa niitä tarvittaessa. 
1. Siirry kohtaan **Malli** &gt; **Luo** luodaksesi Excel-tiedoston tälle asettelulle. 
2. Kun malli on luotu, siirry kohtaan **Malli** &gt; **Näytä** avataksesi ja tarkistaaksesi budjettisuunnitelman asiakirjamallin. Voit tallentaa Excel-tiedoston paikalliseen asemaan. 

[![Tallenna nimellä](./media/bpt3-1024x545.png)](./media/bpt3.png)

> [!NOTE] 
> Budjettisuunnitelman asiakirjan asettelua ei voi muokata, kun Excel-malli on liitetty siihen. Voit muokata asettelua, poistamalla liitetyn Excel-mallitiedoston ja luomalla se uudelleen. Tämä tarvitaan pitämään asettelun kentät ja laskentataulukko synkronoituna. 

Excel-malli sisältää budjettisuunnitelman asiakirja-asettelun kaikki osat, joiden **Käytettävissä työkirjassa** -sarakkeen arvo on Tosi. Excel-mallissa ei sallita päällekkäisiä osia. Esimerkiksi jos asettelu sisältää sarakkeet Request Q1, Request Q2, Request Q3 ja Request Q4 sekä summasarakkeen, joka edustaa kaikkien neljän neljännesvuosittaisen sarakkeen summaa, vain neljännesvuosittaisia sarakkeita tai summasaraketta voidaan käyttää Excel-mallissa. Excel-tiedosto ei voi päivittää päällekkäisiä sarakkeita päivityksen aikana, koska taulukon tiedoista voi tulla vanhentuneita tai virheellisiä.

[![Esimerkki](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Voit välttää mahdollisia ongelmia budjettisuunnitelman tietojen tarkastelemisessa ja muokkaamisessa Excelissä, jos sama käyttäjä on kirjautunut sekä Microsoft Dynamics 365 for Finance and Operations, Enterprise Editioniin että Microsoft Dynamics Office -apuohjelman Data Connectoriin.

## <a name="add-a-header-to-budget-plan-document-template"></a>Otsikon lisääminen budjettisuunnitelman asiakirjamalliin
Jos haluat lisätä otsikkotietoja, valitse ylin rivi Excel-tiedostossa ja lisää tyhjiä rivejä. Lisää otsikkokentät Excel-tiedostoon valitsemalla **Rakenne** **Data Connector** -sovelluksessa.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

Valitse **Rakenne**-välilehdessä, **Lisää kenttiä** ja sitten **BudgetPlanHeader** yksikön tietolähteeksi.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Siirrä kohdistin Excel-tiedostossa haluamaasi paikkaan. Valitse **Lisää otsikko** lisätäksesi kentän otsikon valittuun sijaintiin. Valitse **Lisää arvo** lisätäksesi arvokentän valittuun paikkaan. Valitse **Valmis** sulkeaksesi suunnitteluohjelman.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Lasketun sarakkeen lisääminen budjettisuunnitelman asiakirjamallin taulukkoon
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

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Vinkkejä budjettisuunnitelman mallien luomiseen
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Voinko lisätä ja käyttää muita tietolähteitä budjettisuunnitelman malliin?

Kyllä, voit käyttää **Rakenne**-valikkoa lisätäksesi lisäyksikköjä samaan tai muihin taulukoihin Excel-mallissa. Esimerkiksi, voit lisätä **BudgetPlanProposedProject**-tietolähteen luodaksesi ja ylläpitääksesi ehdotettujen projektien luetteloa samaan aikaan kun työstät budjettisuunnitelman tietoja Excelissä. Huomaa, että suuren datamäärän tietolähteiden lisääminen saattaa heikentää Excel-työkirjan suorituskykyä. 

Voit käyttää **Suodatin** -vaihtoehtoa kohdassa **Data Connector** lisätäksesi haluamasi suodattimet muihin tietolähteisiin.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Voinko piilottaa Rakenne-toiminnon Data Connectorissa muilta käyttäjiltä?

Kyllä, avaa **Data Connector** -asetukset piilottaaksesi **Rakenne**-vaihtoehdon muilta käyttäjiltä.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Laajenna **Data connector -asetukset** ja tyhjennä **Ota rakenne käyttöön** -valintaruutu. Tämä piilottaa **Rakenne**-asetuksen **Data connector** -kohdasta.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Voinko estää käyttäjiä vahingossa sulkemasta Data Connectorin, kun he työstävät tietoja?

Suosittelemme, että haluat estää käyttäjiä sulkemasta mallin lukitsemalla mallin. Voit määrittää lukituksen valitsemalla **Data connector** oikeassa yläkulmassa, jolloin näkyviin tulee nuoli. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Klikkaamalla nuolta näet lisävalikon. Valitse **Lukitse**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>voinko käyttää muita Excelin ominaisuuksia, kuten solun muotoilua, värejä, ehdollista muotoilua ja kaavioita omissa budjettisuunnitelmamalleissani?

Kyllä, useimmat Excelin perusominaisuudet toimivat budjettisuunnitelmamalleissa. On suositeltavaa käyttää värikoodausta käyttäjille, jotta he erottavat Vain luku- ja muokattavat sarakkeet. Ehdollista muotoilua voi käyttää korostamaan budjetin ongelmallisia alueita. Sarakkeiden summat voidaan esittää helposti tavallisten Excel-kaavojen (taulukon yläpuolella) avulla.

Voit myös luoda ja käyttää pivot-taulukoita ja kaavioita budjetin tietojen ylimääräisiin ryhmittelyihin ja visualisointeihin. Valitse **Tiedot**-välilehden **Yhteydet**-ryhmässä **Päivitä kaikki** ja sitten **Yhteyden ominaisuudet**. Valitse **Käyttö**-välilehti. valitse kohdassa **Päivitä** **Päivitä tiedot, kun tiedosto avataan** -valintaruutu. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)



