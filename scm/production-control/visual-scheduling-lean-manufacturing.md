---
title: Lean-valmistuksen visuaalinen ajoitus
description: "Tässä ohjeaiheessa on tietoja Kanban-aikataulusta, jota tuotannon suunnittelija käyttää kanban-töiden tuotantosuunnitelman valvontaan ja optimointiin."
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: KanbanBoard KanbanJobSchedulingListPage, LeanProductionFlowVisulaization
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: johanhoffmann
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 1a3f43c2812cdf1c9f5c564bc86abe4fcc90b8a3
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017

---

# Lean-valmistuksen visuaalinen ajoitus
<a id="visual-scheduling-for-lean-manufacturing" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa on tietoja Kanban-aikataulusta, jota tuotannon suunnittelija käyttää kanban-töiden tuotantosuunnitelman valvontaan ja optimointiin.

Tässä ohjeaiheessa on tietoja Kanban-aikataulusta, jota tuotannon suunnittelija käyttää kanban-töiden tuotantosuunnitelman valvontaan ja optimointiin.

Kanban-aikataulun avulla suunnittelija valvoo ja optimoi kanban-töiden tuotantosuunnitelman. Se tekee kanban-töiden työnkuluista avoimia ja antaa tuotannon suunnittelijalle työkaluja, joilla optimoidaan ja säädetään tuotantosuunnitelman Lean-valmistuksen työsoluja.

## Kanban-töiden visuaalinen ajoitus
<a id="visual-scheduling-of-kanban-jobs" class="xliff"></a>
Kanban-työ voi muodostua yhdestä tai useasta kanban-työstä. Kanban-töitä on kahdenlaisia:

-   Prosessoi
-   Tapahtumien siirto

Voit aikatauluttaa ainoastaan **Prosessi**-tyyppisiä töitä. Kanban-työ ja sen ominaisuudet, kuten tehtäväaika, määritetään Kanban-tuotantovirrassa. Kanban-tuotantovirrassa kanban-työ liitetään myös työsoluun. Työsolun päivittäinen kapasiteetti lasketaan työsolun kapasiteetin perusteella, joka on määritetty resurssiryhmälle. Sitä oikaistaan päivittäisen työajan mukaan liittyvässä kalenterissa. Kun kanban-työ on ajoitettu, työ lataa työsolun kapasiteetin. Kanban-aikataulun tärkeimmät ominaisuudet:

-   Tuotantosuunnitelman graafinen yhteenveto Lean-työsolussa. Tämä yleiskuvaus esittää kanban-prosessitöitä määritettyinä kausina.
-   Työkalu, jonka avulla voit ajoittaa suunnittelemattomat kanban-työt ja ajoittaa ajoitetut työt uudelleen.

## Kanban-aikataulu
<a id="kanban-schedule-board" class="xliff"></a>
**Kanban-aikataulu** -sivulla on seitsemän pääelementtiä, jotka esitetään oheisessa kuvassa. 

![Kanban-aikataulu](./media/kanban-schedule-board-1024x554.png)
1.  Toimintoruutu
2.  Kenttien suodatus
3.  Suunnittelemattomat työt -painike
4.  Kausi-solmu
5.  Kanban-työ
6.  Kapasiteettipalkki
7.  Aika-asteikko

### Aika-asteikon tarkasteleminen
<a id="view-the-time-scale" class="xliff"></a>

Aikataulu jaetaan kausiin, jotka esitetään solmuina (4). Kauden solmut näkyvät pystyakselilla ja vaaka-akseli vastaa aika-asteikkoa (7), joka ilmaisee kauden pituuden. Kauden pituus on yksi päivä tai yksi viikko. Kauden pituus määräytyy työsolun määrityksen mukaan, joka on valittu Kanban-aikataululle (2). Kunkin kauden solmun Kanban-aikataulu ilmaisee, paljonko kaudelle ladataan aikataulutettuja kanban-töitä. Siinä on myös ilmaisin kauden enimmäistuotantokapasiteetista. Jos aikataulutettu tuotantokapasiteetti ylittää enimmäistuotantokapasiteetin, kauden katsotaan olevan ylikuormitettu ja näkyy punainen varoitussymboli. Aikataulutettu kanban-työ näkyy jaksossa, jossa on suunniteltu alkamis- ja päättymisaika (5). Työn pituus vastaa tehtäväaikaa. Kanban-työt näkyvät muutetaan päällekkäisiä jaksossa, jos niiden tehtäväaika ylittää työsolun tahtiajan.

### Näytä töiden tila
<a id="view-job-status" class="xliff"></a>

Lisätietoja kanban-työstä on työkaluvihjeessä, joka tulee näkyviin, kun viet hiiren osoittimen työn päälle. Symboli sisältää tietoja työn tilasta. Esimerkiksi kello-symboli ilmaisee, että kanban-työ on erääntynyt.

### Värien käyttö Kanban-aikataulun esittämisessä
<a id="use-colors-to-view-the-kanban-schedule-board" class="xliff"></a>

Voit parantaa Kanban-aikataulun yhteenvetoa väreillä, jotka erottavat kanban-työt. Kanban-työn väri on määritetty Lean-aikatauluryhmässä, jossa voidaan koota tuotteet, jotka on esitettävä samassa järjestyksessä. **Käytä teeman värejä** -painikkeella **Taulu**-välilehdellä toimintoruudussa voit vaihtaa sovelluksen värejä ja värit, jotka on määritetty lean aikatauluryhmälle. Kunkin kauden kapasiteettipalkki (6) ilmaisee, montako käytettävissä olevaa tuntia on ladattu kanban-töille. Jos kausi on ylikuormitettu, kapasiteettipalkki näkyy paksumpana ja punaisena. Kaikki nämä toiminnot ovat käytettävissä **Taulu**-välilehdellä toimintoruudussa (1) **Kanban-aikataulu**-sivun yläosassa.

## Suunnittele suunnittelemattomat työt
<a id="plan-unplanned-jobs" class="xliff"></a>
Voit aikatauluttaa suunnittelemattomat kanban-työt **Suunnittele suunnittelemattomat työt** -valintaikkunassa. Avaa valintaikkuna valitsemalla **suunnittelemattomat työt** -painike, joka näyttää suunnittelemattomien töiden määrän. Vaihtoehtoisesti napsauta **Suunnittele suunnittelemattomat työt** **Taulu** välilehdellä toimintoruudussa. Valintaikkunassa näkyy työsolun suunnittelemattomien kanban-töiden luettelo. Voit suodattaa kaikki ruudukon kentät **Suodatin**-kentän avulla. Voit esimerkiksi suodattaa tietyn tuotteen kanban-työt. Kun olet suodattanut ajoitettavien töiden luettelon, valitse ne luettelosta ja valitse sitten **OK**. Jos haluat käyttää töiden ajoittamiseen automaattista suunnittelua, määritä **Automaattinen suunnittelu** -asetukseksi **Kyllä**. Tässä tapauksessa työt ajoitetaan tietylle kaudelle eräpäivän mukaan. Voit myös ajoittaa töitä kausittain. Valitse kausi **Kausi**-kentästä. Seuraavassa kuvassa on esimerkki **SSuunnittele suunnittelemattomat työt** -valintaikkunasta. 

![Suunnittele suunnittelemattomat työt -valintaikkuna](./media/plan-unplanned-jobs-1024x564.png)

## Saman kauden kanban-töiden järjestäminen
<a id="sequence-kanban-jobs-within-the-same-period" class="xliff"></a>
Voit muuttaa kauden valittujen projektien numerosarjan. Tämä ominaisuus on hyödyllinen, jos haluat priorisoida joitakin töitä kauden aikana. Vaihtoehtoisesti voit halutessasi järjestää työt saman työmääritteen perusteella optimoidaksesi työn suorituksen. Voit muuttaa järjestystä vetämällä ja pudottamalla tai käyttämällä **Taaksepäin**- ja **Eteenpäin** -valikkovaihtoehtoja **Taulu**-välilehdessä toimintoruudussa.

## Kanban-töiden uudelleenmäärittäminen kausille
<a id="reassign-kanban-jobs-across-periods" class="xliff"></a>
Työt voidaan määrittää uudelleen kaudesta toiseen. Tämä toimintoa voi olla hyödyllinen, jos kausi on ylikuormitettu ja haluat tasata kuormitusta kausille, joissa on vapaata kapasiteettia. Voit määrittää töitä uudelleen vetämällä ja pudottamalla tai käyttämällä **Seuraava jakso**- ja **Edellinen jakso** -valikkovaihtoehtoja **Taulu**-välilehdessä toimintoruudussa.

## Avaa kanban-aikataulu
<a id="open-the-kanban-schedule-board" class="xliff"></a>
Voit avata Kanban-aikataulun valikkokohdasta seuraavilla sivuilla:

-   **Tuotantoalue**-sivu
-   **Kanban-työn aikataulutus** -sivu
-   **Tuotantovirran visualisointi** -sivu


Lisätietoja
<a id="see-also" class="xliff"></a>
--------

[Lean-valmistus – Kanban-työn aikataulutus](lean-manufacturing-kanban-job-scheduling.md)


