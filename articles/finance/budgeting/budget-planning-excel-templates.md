---
title: Excelin budjettisuunnittelumallit
description: Tässä ohjeaiheessa kuvataan, miten luodaan Microsoft Excel -malleja, joita voidaan käyttää budjettisuunnitelmissa.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 471c719a8e6de0ebe6fcdad0ae222453db841c87
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442895"
---
# <a name="budget-planning-templates-for-excel"></a>Excelin budjettisuunnittelumallit

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan, miten luodaan Microsoft Excel -malleja, joita voidaan käyttää budjettisuunnitelmissa.

Tässä ohjeaiheessa kuvataan, miten luodaan Excel-malleja, joita käytetään budjettisuunnitelmissa käyttämällä vakionäytetietoja ja Järjestelmänvalvoja-käyttäjätunnusta. Lisätietoja budjettisuunnittelusta on kohdassa [Budjettisuunnittelun yleiskatsaus](budget-planning-overview-configuration.md). Voit myös seurata [Budjettisuunnittelun perusteet](budget-plan.md) -opastusta, jossa on perustiedot moduulin määrityksestä sekä käytön periaatteet.

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

> [!NOTE] 
> Voit välttää mahdollisia ongelmia budjettisuunnitelman tietojen tarkastelemisessa ja muokkaamisessa Excelissä, jos sama käyttäjä on kirjautunut sekä Microsoft Dynamics 365 Financeen että Microsoft Dynamics Office -apuohjelman tietoyhdistimeen.

## <a name="add-a-header-to-budget-plan-document-template"></a>Otsikon lisääminen budjettisuunnitelman asiakirjamalliin
Jos haluat lisätä otsikkotietoja, valitse ylin rivi Excel-tiedostossa ja lisää tyhjiä rivejä. Lisää otsikkokentät Excel-tiedostoon valitsemalla **Rakenne** **Data Connector** -sovelluksessa.

Valitse **Rakenne**-välilehdessä, **Lisää kenttiä** ja sitten **BudgetPlanHeader** yksikön tietolähteeksi.

Siirrä kohdistin Excel-tiedostossa haluamaasi paikkaan. Valitse **Lisää otsikko** lisätäksesi kentän otsikon valittuun sijaintiin. Valitse **Lisää arvo** lisätäksesi arvokentän valittuun paikkaan. Valitse **Valmis** sulkeaksesi suunnitteluohjelman.

## <a name="select-add-valuemediabpt7png"></a>[![Valitse Lisää arvo](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Lasketun sarakkeen lisääminen budjettisuunnitelman asiakirjamallin taulukkoon
--------------------------------------------------------------

Seuraavaksi, lasketut sarakkeet lisätään muodostettuun budjettisuunnitelman asiakirjamalliin. **Total Request** -sarake, joka summaa sarakkeet Request Q1 – Request Q4 ja **Oikaisu**-sarakkeen, joka laskee **Total request** -sarakkeen esimääritetyn kertoimen avulla.

Lisää sarakkeet taulukkoon valitsemalla **Rakenne** **Data Connector** -sovelluksessa. Valitse **Muokkaa** **BudgetPlanWorksheet**-tietolähteen vieressä aloittaaksesi sarakkeiden lisäämisen.

[![Sarakkeiden lisäämisen aloittaminen](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Valittu kenttäryhmää näyttää mallissa käytettävissä olevat sarakkeet. Valitse **Kaava**, kun haluat lisätä uuden sarakkeen. Nimeä uusi sarake ja liitä sitten kaava **Kaava**-kenttään. Valitse **Päivitä**, jos haluat lisätä sarakkeen.

[![Sarakkeen lisääminen](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Luo kaava laskentataulukossa ja kopioi se **Rakenne**-ikkunaan määrittääksesi kaavan. Finance and Operationsin sidottu taulukko on yleensä nimeltään AXTable1. Jos esimerkiksi haluat summata laskentataulukossa sarakkeet Request Q1 – Request Q4, kaava on: AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].

Toista nämä vaiheet lisätäksesi **Oikaisu**-sarakkeen. Käytä tälle sarakkeelle kaavaa = AxTable1\[Total request\]\*$I$1. Tämä ottaa solun I1 arvon ja kertoo **Total request** -sarakkeen laskeakseen oikaisusummat.

Tallenna ja sulje Excel-tiedosto. Lataa budjettisuunnitelmassa käytettävä tallennettu Excel-malli valitsemalla **Asettelu**-kohdassa **Malli &gt; Lataa**. 

[![Excel-malli lataaminen palvelimeen](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Sulje **Asettelut**-liukusäädin. Valitse **Budjettisuunnitelma**-asiakirjassa **Työkirja**, jolloin voit tarkastella ja muokata asiakirjaa Excelissä. Huomaa, että tämän budjettisuunnitelman työkirjan luomiseen käytettiin oikaistua Excel-mallia, ja lasketut sarakkeet päivitetään käyttäen kaavoja, jotka määritettiin edellisissä vaiheissa. 

[![Tiedoston näyttäminen ja muokkaaminen Excelissä](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Vinkkejä budjettisuunnitelman mallien luomiseen
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Voinko lisätä ja käyttää muita tietolähteitä budjettisuunnitelman malliin?

Kyllä, voit käyttää **Rakenne**-valikkoa lisätäksesi lisäyksikköjä samaan tai muihin taulukoihin Excel-mallissa. Esimerkiksi, voit lisätä **BudgetPlanProposedProject**-tietolähteen luodaksesi ja ylläpitääksesi ehdotettujen projektien luetteloa samaan aikaan kun työstät budjettisuunnitelman tietoja Excelissä. Huomaa, että suuren datamäärän tietolähteiden lisääminen saattaa heikentää Excel-työkirjan suorituskykyä. 

Voit käyttää **Suodatin** -vaihtoehtoa kohdassa **Data Connector** lisätäksesi haluamasi suodattimet muihin tietolähteisiin.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Voinko piilottaa Rakenne-toiminnon Data Connectorissa muilta käyttäjiltä?

Kyllä, avaa **Data Connector** -asetukset piilottaaksesi **Rakenne**-vaihtoehdon muilta käyttäjiltä.

[![Data Connector -asetusten avaaminen](./media/bpt13-1024x565.png)](./media/bpt13.png)

Laajenna **Data connector -asetukset** ja tyhjennä **Ota rakenne käyttöön** -valintaruutu. Tämä piilottaa **Rakenne**-asetuksen **Data connector** -kohdasta.

[![Rakenne-vaihtoehdon piilottaminen Data Connectorissa](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Voinko estää käyttäjiä vahingossa sulkemasta Data Connectorin, kun he työstävät tietoja?

Suosittelemme, että haluat estää käyttäjiä sulkemasta mallin lukitsemalla mallin. Voit määrittää lukituksen valitsemalla **Data connector** oikeassa yläkulmassa, jolloin näkyviin tulee nuoli. 

[![Lukituksen ottaminen käyttöön](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Klikkaamalla nuolta näet lisävalikon. Valitse **Lukitse**.

### <a name="select-lockmediabpt16png"></a>[![Lukituksen valinta](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>voinko käyttää muita Excelin ominaisuuksia, kuten solun muotoilua, värejä, ehdollista muotoilua ja kaavioita omissa budjettisuunnitelmamalleissani?

Kyllä, useimmat Excelin perusominaisuudet toimivat budjettisuunnitelmamalleissa. On suositeltavaa käyttää värikoodausta käyttäjille, jotta he erottavat Vain luku- ja muokattavat sarakkeet. Ehdollista muotoilua voi käyttää korostamaan budjetin ongelmallisia alueita. Sarakkeiden summat voidaan esittää helposti tavallisten Excel-kaavojen (taulukon yläpuolella) avulla.

Voit myös luoda ja käyttää pivot-taulukoita ja kaavioita budjetin tietojen ylimääräisiin ryhmittelyihin ja visualisointeihin. Valitse **Tiedot**-välilehden **Yhteydet**-ryhmässä **Päivitä kaikki** ja sitten **Yhteyden ominaisuudet**. Valitse **Käyttö**-välilehti ja valitse kohdassa **Päivitä** **Päivitä tiedot, kun tiedosto avataan** -valintaruutu. 



