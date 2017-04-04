---
title: Excelin budjettisuunnittelumallit
description: "Tässä aiheessa kuvataan, miten Luo Microsoft Excel-malleja, joita voidaan käyttää budjettisuunnitelmat."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 0e2eb6e7c130f03edbf60a185d397d94b5d61d7d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-templates-for-excel"></a>Excelin budjettisuunnittelumallit

Tässä aiheessa kuvataan, miten Luo Microsoft Excel-malleja, joita voidaan käyttää budjettisuunnitelmat.

Tässä ohjeaiheessa kuvattaan, miten luoda Excel-malleja, jota käytetään standardin esittely tietojoukon ja Admin kirjautuminen budjettisuunnitelmat. Saat lisätietoja budjettisuunnittelua [budjetin yhteenveto.](budget-planning-overview-configuration.md) Voit myös seurata [101 budjettisuunnittelu](budget-plan.md) opetusohjelma saat perustiedot-moduulin määrityksen ja käytön periaatteet.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Luo budjettisuunnitelman asiakirjan asettelua käyttämällä laskentataulukon
Budjetin suunnitelma-asiakirjoja voi tarkastella ja muokata yhden tai useita asetteluja käyttämällä. Kussakin asettelussa voi olla liitetty budjettisuunnitelman asiakirjamalli voidaan tarkastella ja muokata budjettisuunnitelman tiedot Excel-laskentataulukkoon. Tässä ohjeaiheessa budjettisuunnitelman asiakirjamalli luodaan käyttämällä valmista layout-määritystä. Avaa **budjetin toimenpidesuunnitelmien luettelo** (**budjetoinnin**&gt;**budjettisuunnitelmat**). Valitse **uusi** voit luoda uuden budjettisuunnitelman asiakirjan. [![bpt1](./media/bpt11-1024x552.png)](./media/bpt11.png) 

Käytössä **Lisää** rivi-vaihtoehto, jos haluat lisätä rivejä. Valitse **rakenteita** voit tarkastella budjettisuunnitelman asiakirjan asettelun määritykset. 
[![bpt2](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Voit tarkistaa asettelun määritykset ja muuta sitä tarvittaessa. Siirry **malli**&gt;**Luo** Luo asettelu Excel-tiedostoon. Kun malli luodaan, siirry **malli**&gt;**View** avaaminen ja tarkasteleminen budjettisuunnitelman asiakirjamalli. Voit tallentaa Excel-tiedosto kansioon paikalliseen asemaan. [![bpt3](./media/bpt3-1024x545.png)](./media/bpt3.png) 

> [!NOTE] 
> Budjettisuunnitelman asiakirjan asettelua ei voi muokata, kun Excel-malli on liitetty siihen. Muokkaa asettelua, poistaa liitetyn mallin Excel-tiedoston ja luo se uudelleen. Tarvitaan pitämään kenttien asettelun ja taulukon synkronoituna. 

Excel-malli sisältää kaikki osat budjettisuunnitelman asiakirja-asettelu, jossa **käytettävissä taulukon** -sarakkeen arvo on True. Excel-malli päällekkäiset osat eivät ole sallittuja. Esimerkiksi jos asettelu sisältää pyynnön Q1, Q2 pyyntö, pyynnön Q3 ja pyynnön Q4 sarakkeet ja pyynnön yhteensä-saraketta, joka edustaa 4 neljännesvuosittain kaikkien sarakkeiden summan, neljännesvuosittain sarakkeita tai yhteensä-sarakkeessa on käytettävissä Excel-mallia voidaan käyttää. Excel-tiedosto ei voi päivittää päällekkäisiä sarakkeet päivityksen aikana, koska taulukon tiedoista voi tulla vanhentuneita tai virheellisiä.

[![bpt4](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Voit välttää mahdollisia ongelmia tarkastelemisen ja muokkaamisen budjettisuunnitelman tiedot Excelissä, sama käyttäjä olisi on kirjauduttava sekä Dynamics 365 toiminnoissa ja Dynamics Microsoft Office-apuohjelma Data Connector.

## <a name="add-a-header-to-budget-plan-document-template"></a>Otsikon lisääminen budjettisuunnitelman Asiakirjamalli
Jos haluat lisätä otsikkotietoja, ylin rivi Excel-tiedoston ja Lisää tyhjiä rivejä. Valitse **rakenne** - **Data Connector** ylä-kenttien lisääminen Excel-tiedosto.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

- **Rakenne** -välilehden ** ** valitsemalla **Lisää** kentät ja valitse sitten **BudgetPlanHeader** yksikön tietolähteenä.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Valitse kohdistimen Excel-tiedoston haluamaasi paikkaan. Valitse **Lisää otsikko** kentän otsikon lisääminen valittuun sijaintiin. Valitse **Lisää arvo** voit lisätä arvo-kentässä valittuun paikkaan. Valitse **tehty** ja sulje suunnitteluohjelma.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Lisää budjettisuunnitelman asiakirjan malli-taulukon laskettu sarake
--------------------------------------------------------------

Seuraava, lasketut sarakkeet lisätään Muodostetuilla asiakirjamalli. A **yhteensä pyynnön** sarake, jossa on esitetty pyyntö Q1: pyyntö Q4 sarakkeet ja **säätö** sarakkeen, joka laskee **yhteensä pyynnön** käyttämällä ennalta määritettyä saraketta.

Valitse **rakenne** - **Data connector** voit lisätä taulukon sarakkeita. Valitse **Muokkaa** vieressä **BudgetPlanWorksheet** tietolähde, johon haluat lisätä sarakkeet.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Valittua kenttäryhmää näyttää mallissa käytettävissä olevat sarakkeet. Valitse **kaavan** haluat lisätä uuden sarakkeen. Uuden sarakkeen nimi ja valitse sitten Liitä huomioon kaava **kaavan** kenttä. Valitse **päivitys** Jos haluat lisätä sarakkeen.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Määritä kaava, kaavan luominen laskentataulukkoon ja kopioi se **rakenne** ikkuna. Dynamics-365 sidotun taulukon toiminnot yleensä nimetään "AXTable1". Esimerkiksi yhteenvedon pyytää Q1: pyytää Q4 sarakkeita laskentataulukkoon, kaava = AxTable1\[pyytää Q1\]+ AxTable1\[pyytää Q2\]+ AxTable1\[pyytää Q3\]+ AxTable1\[pyytää Q4\].

Toistamalla näitä vaiheita voit lisätä **muutos** sarakkeeseen. Käytä kaavaa = AxTable1\[yhteensä pyynnön\]\*$I$ 1 sarakkeen. Tämä kestää I1-solun arvo ja kerro arvot **yhteensä pyynnön** sarakkeen laskennassa oikaisuihin.

Tallenna ja sulje Excel-tiedosto. Dynamics 365 Operations, ja palaa **rakenteita**, valitse **malli &gt;Lataa** Lataa tallennettu Excel-malli, jota käytetään budjetin suunnitelman. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Sulje **rakenteita** liukusäädintä. - **Budjettisuunnitelman** asiakirjassa, valitse **laskentataulukon** voit tarkastella ja muokata sitä Excelissä. Huomaa, että tämä talousarvio suunnitelman luomiseen käytetyn muutettu Excel-malli ja päivittää laskettujen sarakkeiden kaavat, jotka määritettiin edellä kuvattujen toimien avulla. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Tips & tricks budjettisuunnitelman mallien luominen
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Voit lisätä ja käyttää muita tietolähteitä budjettisuunnitelman malli?

Kyllä, voit käyttää **rakenne** valikon muita kohteita samaan tai muita taulukoita Excel-malli. Esimerkiksi, voit lisätä **BudgetPlanProposedProject** voit luoda ja ylläpitää ehdotettujen projektien luettelo samaan aikaan kun talousarvion parissa suunnitteleminen Excelissä tietolähdettä. Huomaa, että myös suuria tietolähteitä saattaa heikentää suorituskykyä Excel-työkirjan. 

Voit käyttää **suodatin** -vaihtoehdon **Data Connector** voit lisätä haluamasi suodattimia muissa tietolähteissä.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Voit piilottaa toiminnon rakenne-Data connector for muille käyttäjille?

Kyllä, Avaa **Data Connector** asetuksia, joilla piilotetaan **rakenne** vaihtoehto muilta käyttäjiltä.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Laajenna **tiedot yhdistinasetukset** ja poista **käyttöön rakenne** valintaruutu. Tämä piilottaa **rakenne** asetus **Data connector**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Käyttäjien estämään sulkemasta vahingossa Data connector tietojen käsittelemisessä

Suosittelemme, että haluat estää käyttäjiä sulkemista mallin lukituksen. Voit poistaa lukituksen valitsemalla **Data connector**, oikeassa yläkulmassa näkyy nuoli. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Lisää valikon nuolta. Valitse **Lock**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Muita Excelin ominaisuuksia, kuten solun muotoilu, värit, ehdollinen muotoilu ja kaavioiden avulla omien budjettisuunnitelmamallit kanssa

Kyllä, useimpia ominaisuuksia standardi Excel toimii budjettisuunnitelmamallit. On suositeltavaa käyttää vain luku- ja muokattavat sarakkeet erottaa värikoodaus käyttäjille. Ehdollisen muotoilun avulla voit korostaa talousarvion ongelmallisia alueita. Sarakkeiden summat voidaan esittää helposti taulukon yläpuolella tavallinen Excel-kaavojen avulla.

Voit myös luoda ja käyttää pivot-taulukoita ja kaavioita ylimääräisiä ryhmittelyjä ja budjetin tiedot visualisointeja. - **Tiedot** -lehden **yhteydet** ryhmän, valitse **Päivitä kaikki**, ja valitse sitten **ominaisuudet**. Valitse **käyttö** välilehti. Valitse **päivittää**, valitse **Päivitä tiedot, kun tiedosto avataan** valintaruutu. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)


