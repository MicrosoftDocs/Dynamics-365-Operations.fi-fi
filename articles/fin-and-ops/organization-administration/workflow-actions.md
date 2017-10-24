---
title: "Työnkulkutehtävät"
description: "Tässä artikkelissa kuvataan toimenpiteet, jotka kukin työnkulun hyväksyntäprosessin osallistuja voi suorittaa."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bbaac72d8adb764c4b186b022100248b1c5a3804
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="workflow-actions"></a>Työnkulkutehtävät

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan toimenpiteet, jotka kukin työnkulun hyväksyntäprosessin osallistuja voi suorittaa.

Työnkulkuun voi liittyä useita käyttäjäryhmiä: aloittaja, tehtävän osallistuja, päätöksentekijät ja hyväksyjät. Esimerkiksi seuraavassa kuluraportin työnkulussa Sam on aloittaja, jonon jäsenet ovat tehtävän osallistujia, John on päätöksentekijä sekä Frank, Sue sekä Ann ovat hyväksyjiä.   

[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif) 

Seuraavissa kappaleissa kuvataan kunkin ryhmän mahdolliset toimenpiteet.

## <a name="actions-that-an-originator-can-perform"></a>Toiminnot, joita aloittaja voi suorittaa
Aloittaja käynnistää työnkulkuesiintymän lähettämällä tiedoston käsiteltäväksi. Sam voi esimerkiksi lähettää kuluraporttinsa napsauttamalla **Lähetä**-painiketta **Kuluraportti**-sivulla.

## <a name="actions-that-a-task-assignee-can-perform"></a>Toiminnot, joita tehtävän osallistuja voi suorittaa
Tehtävä voidaan määrittää useille henkilöille tai useiden henkilöiden seuraamalle työnimikejonolle. Kuitenkin vain yksi henkilö voi suorittaa tehtävän. Sam on esimerkiksi lähettänyt kuluraportin ja reitittänyt kuittinsa organisaationsa kuluraporttiosastolle tarkistusta varten. 

Adventure Worksin kuluraporttiosaston jäsenet seuraavat jonoa. Tämän osaston jäsen, Julie, on hyväksynyt Samin kuluraportin ja kuittien tarkistustehtävän. Julie voi suorittaa jonkin seuraavista toiminnoista: valmis, hylkää, delegointi, pyydä muutosta, määritä uudelleen tai vapauta. 

**Huomautus.** Käytettävissä olevat toiminnot vaihtelevat sen mukaan, miten ohjelmistokehittäjä on suunnitellut tehtävän.

### <a name="complete"></a>Valmis

Kun käyttäjä suorittaa tehtävän loppuun, käsiteltäväksi lähetetty tiedosto lähetetään työnkulussa mahdollisesti seuraavaksi määritetylle käyttäjälle. Jos lisäkäsittelyä ei tarvita, työnkulkuprosessi päättyy. 

Esimerkiksi Julie, joka on Adventure Worksin kuluraporttiosaston jäsen, on hyväksynyt Samin kuluraportin ja kuittien tarkistustehtävän. Kun Julie on suorittanut tarkistuksen, asiakirja määritetään Johnille.

### <a name="reject"></a>Hylkää

Jos käyttäjä hylkää tiedoston, työnkulku päättyy. 

Esimerkiksi Julie, joka on Adventure Worksin kuluraporttiosaston jäsen, on hyväksynyt Samin kuluraportin ja kuittien tarkistustehtävän. Jos Julie hylkää kuluraportin, työnkulkuprosessi päättyy. 

San voi sitten lähettää kuluraportin uudelleen. Hän voi tehdä siihen ensin muutoksia tai lähettää alkuperäisen version uudelleen. Jos Sam lähettää kuluraportin uudelleen, työnkulkuprosessi käynnistyy manuaalisesta tarkistustehtävästä.

### <a name="delegate"></a>Delegointi

Jos käyttäjä delegoi tehtävän, se määritetään toisen käyttäjän suoritettavaksi. 

Esimerkiksi Julie, joka on Adventure Worksin kuluraporttiosaston jäsen, on hyväksynyt Samin kuluraportin ja kuittien tarkistustehtävän. Julie delegoi tehtävän Timille, joka on hänen avustajansa. 

Tim toimii sitten Julien puolesta. Kun Tim sitten päättää tarkistuksensa, kuluraportti määritetään Johnille aivan kuten, jos Julie olisi suorittanut tehtävän.

### <a name="request-change"></a>Pyydä muutosta

Jos käyttäjä tekee muutospyynnön, tiedosto palautetaan sen lähettäneelle aloittajalle. 

Esimerkiksi Julie, joka on Adventure Worksin kuluraporttiosaston jäsen, on hyväksynyt Samin kuluraportin ja kuittien tarkistustehtävän. Julie huomaa kuluraportissa virheitä ja pyytää muutoksia. Kuluraportti lähetetään takaisin Samille. 

Sam voi lähettää kuluraportin uudelleen. Hän voi tehdä siihen ensin pyydetyt muutokset tai lähettää alkuperäisen version. Jos Sam lähettää kuluraportin uudelleen, työnimikejonon jäsenen on tarkistettava kuluraportti ja kuitit uudelleen.

### <a name="reassign"></a>Määritä uudelleen

Työnimijonon jäsenet voivat määrittää jonossa olevat asiakirjat toiseen jonoon. 

Esimerkiksi Julie, Adventure Worksin kuluraporttiosaston jäsen, seuraa jonoa. Julie voi tasapainottaa kuormitusta määrittämällä kuluraportin ja siihen sisältyvät kuitit uudelleen toiseen jonoon.

### <a name="release"></a>Vapauta

Työnimikejonon jäsen voi joskus hyväksyä tehtävän mutta päättää myöhemmin, ettei hän voikaan suorittaa tehtävää. Siinä tapauksessa tehtävän hyväksynyt henkilö vapauttaa asiakirjan takaisin työnimikejonoon. 

Esimerkiksi Julie, joka on Adventure Worksin kuluraporttiosaston jäsen, on hyväksynyt Samin kuluraportin ja kuittien tarkistustehtävän. Jos Julie päättää, ettei hän voi suorittaa tehtävää, hän vapauttaa asiakirjan. Kuluraportti palautetaan jonoon, jolloin Adventure Worksin kuluraporttiosaston muut jäsenet voivat suorittaa tehtävän.

## <a name="actions-that-a-decision-maker-can-perform"></a>Toiminnot, joita päätöksentekijä voi suorittaa
Asiakirja määritetään yleensä päätöksentekijälle siksi, että siihen sisältyy kysymys, johon päätöksentekijän on vastattava. Kysymyksen vastaus on yleensä **Kyllä** tai **Ei** tai **Tosi** tai **Epätosi**. Jos päätöksentekijä ei valitse yhtä näistä vaihtoehdoista, hän delegoida päätöksen.

### <a name="choice-1-or-choice-2"></a>\[Vaihtoehto 1\] tai \[Vaihtoehto 2\]

Päätöksentekijän on vastattava asiakirjaan liittyvään kysymykseen. Kysymyksen vastaus on yleensä **Kyllä** tai **Ei** tai **Tosi** tai **Epätosi**. Päätöksentekijän valitsema vastaus määrittää työnkulun haaran, jossa asiakirja käsitellään. 

Samin kuluraportti on esimerkiksi määritetty Johnille. Johnin on päätettävä, onko hänen soitettava Samin esimiehelle asiakirjan tietojen perusteella. John päättää, että puhelu on välttämätön, kuluraportti määritetään Arethalla, jonka on sitten soitettava Samin esimiehelle. Jos John päättää, että puhelua ei tarvita, kuluraportti määritetään Frankille hyväksyttäväksi.

### <a name="delegate"></a>Delegointi

Kun päätöksentekijä delegoi päätöksen, asiakirja määritetään toiselle käyttäjälle, jonka on tehtävä päätös. 

Samin kuluraportti on esimerkiksi määritetty Johnille. John delegoi päätöksen Maria, joka on hänen avustajansa. 

Maria toimii sitten Johnin puolesta. Jos Maria päättää, että puhelu on Samin esimiehelle on välttämätön, kuluraportti määritetään Arethalla, jonka on sitten soitettava Samin esimiehelle. Jos Maria päättää, että puhelua ei tarvita, kuluraportti määritetään Frankille hyväksyttäväksi.

## <a name="actions-that-an-approver-can-perform"></a>Toiminnot, joita aloittaja voi suorittaa
Kun tiedosto määritetään hyväksyjälle, hän voi suorittaa jonkin seuraavista toiminnoista: hyväksyntä, hylkäys, delegointi, pyydä muutosta.

### <a name="approve"></a>Hyväksyminen

Jos hyväksyjä hyväksyy asiakirjan, se lähetetään työnkulussa mahdolliselle seuraavaksi määritetylle käyttäjälle. Jos lisäkäsittelyä ei tarvita, työnkulkuprosessi päättyy. 

Sam on esimerkiksi lähettänyt 6 000 dollarin arvoisen kuluraportin ja asiakirja on määritetty Frankille. Kun Frank hyväksyy raportin, se määritetään Suelle hyväksyttäväksi. Kun Sue hyväksyy kuluraportin, työnkulkuprosessi päättyy.

### <a name="reject"></a>Hylkää

Jos hyväksyjä hylkää tiedoston, työnkulku päättyy. 

Sam on esimerkiksi lähettänyt 12 000 dollarin arvoisen kuluraportin ja asiakirja on määritetty Suelle. Jos Sue hylkää kuluraportin, työnkulkuprosessi päättyy. 

Sam voi lähettää kuluraportin uudelleen. Hän voi tehdä siihen ensin muutoksia tai lähettää kuluraportin alkuperäisen version uudelleen. Jos Sam lähettää kuluraportin uudelleen, työnkulkuprosessi käynnistyy hyväksyntäprosessista.

### <a name="delegate"></a>Delegointi

Jos hyväksyjä delegoi tiedoston, se lähetetään hyväksyttäväksi toiselle käyttäjälle. 

Sam on esimerkiksi lähettänyt 12 000 dollarin arvoisen kuluraportin ja asiakirja on määritetty Frankille. Frank delegoi kuluraportin Annille. 

Ann toimii sitten Frankin puolesta. Kun Ann sitten hyväksyy asiakirjan, se määritetään Suelle hyväksyttäväksi, aivan kuten jos Frank olisi hyväksynyt asiakirjan. Kun Sue hyväksyy asiakirjan, se lähetetään Annille hyväksyttäväksi.

### <a name="request-change"></a>Pyydä muutosta

Jos hyväksyjä tekee muutospyynnön, tiedosto palautetaan sen lähettäneelle aloittajalle. 

Sam on esimerkiksi lähettänyt 12 000 dollarin arvoisen kuluraportin ja asiakirja on määritetty Suelle. Jos Sue pyytää muutosta, kuluraportti lähetetään takaisin Samille. 

Sam voi lähettää kuluraportin uudelleen. Hän voi tehdä siihen ensin pyydetyt muutokset tai lähettää kuluraportin alkuperäisen version uudelleen. Jos Sam lähettää kuluraportin uudelleen, se lähetetään Frankille hyväksyttäväksi, koska Frank on hyväksyntäprosessin ensimmäinen hyväksyjä.




