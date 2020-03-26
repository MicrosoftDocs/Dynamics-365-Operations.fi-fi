---
title: Asiakkaiden luotonhallintatietojen lisääminen
description: Tässä ohjeaiheessa käsitellään asiakkaan luotonhallintietojen lisäämistä.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 872d129494b815d6dbf88cc9f84b4e80723a8d6d
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124320"
---
# <a name="add-credit-management-information-for-customers"></a>Asiakkaiden luotonhallintatietojen lisääminen

[!include [banner](../includes/banner.md)]

Kun luotonhallintaa ohjaavat parametrit on määritetty, voit lisätä lisää tietoja kustakin asiakkaasta. Nämä tiedot ohjaavat luotonhallintaprosesseja, ja ne antavat myös lisätietoja, joiden avulla perintäryhmän jäsenet voivat hallita asiakkaita.

## <a name="customer-information"></a>Asiakastiedot

Asiakastiedot lisätään **Kaikki asiakkaat** -sivun **Luotonvalvonta**-pikavälilehdessä (**Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**).

1. Valitse **Rajoittamaton luottoraja** -asetukseksi **Kyllä**, jos asiakasta ei rajoiteta millään luottorajatestillä.
2. Valitse **Ohita luotohallinnassa** -asetukseksi **Kyllä**, jos luotonhallintaprosessien aikana yleensä tehtävät toimet ohitetaan asiakkaan kohdalla.
3. Valitse asiakkaan luotonhallintaryhmä.
4. Voit laskea luottorajan asiakkaan valuuttana antamalla **Luottaraja asiakkaan valuuttana** -kentässä asiakkaan luottorajan. Yritysvaluutan luottoraja muunnetaan käyttämällä vaihtokursseja, jotka luotonhallinnan parametreissa valittu luottorajan vaihtokurssin tyyppi määrittää.
5. Anna **Viimeksi tarkistettu** -kenttään päivämäärä, jolloin luottopäällikkö viimeksi tarkisti asiakkaan luottorajan.
6. Anna **Seuraava ajoitettu tarkistuspäivä** -kenttään päivämäärä, jolloin asiakkaan luottotarkistus ja -päivitys on ajoitettu.
7. Anna **Hyväksyttävä luottoraja** -kenttään korkein luottoraja, joka voidaan määrittää asiakkaalle asiakkaan luottotietojen arvioinnin perusteella. Hyväksyttävän luottorajan arvo ei ole välttämättä sama kuin **Luotonvalvonta**-pikavälilehdessä oleva luottoraja.
8. Anna **Hyväksyttävän luottorajan valuutta** -kenttään hyväksyttävän luottorajan valuutta.
9. Anna **Hyväksyttävän luottorajan päivämäärä** -kenttään päivämäärä, jolloin hyväksyttävä luottoraja luotiin.
10. Anna **Luottotilin tila** -kenttään asiakkaan luottotilin tila.
11. Anna **Tilan syy** -kenttään tilin tilaan liitetty syy.
12. Kun **Luottolaitoksen kautta**-asetuksena on **Kyllä**, asiakkaan ilmaistaan olevan määritetty luottolaitokseen. Tämä arvo on tarkoitettu vain tiedoksi. Sitä ei käytetä luotonhallintaprosesseissa.
13. Kun **Omistusoikeus**-asetuksena on **Kyllä**, omistusoikeutta säilytetään yrityksen puolesta. Tämä arvo on tarkoitettu vain tiedoksi. Sitä ei käytetä luotonhallintaprosessissa.
14. Anna **Yrityksen aloituspäivämäärä** -kenttään päivämäärä, jolloin asiakas aloitti yritystoimintansa. Tätä tietoa käytetään riskipisteitä luotaessa.
15. Anna **Asiakas alkaen** -kenttään päivämäärä, jolloin asiakkaan ensimmäiset tapahtumat käsiteltiin. Tätä tietoa käytetään riskipisteitä luotaessa.
16. Kirjoita muistiinpanoja, jotka auttaa luottoryhmää arvioimaan asiakkaan luottokelpoisuutta.

Huomaa, että osa **Asiakas**-sivulla näkyvistä tiedoista on luotu toisessa prosessissa:

- **Luottorajan vanhentumispäivä** -kentässä on päivämäärä, jolloin luottoraja vanhenee. Jos kenttää ei määritetä, asiakkaan luottoraja ei vanhene.
- **Luottorajan päivämäärä** -kentässä on päivämäärä, jolloin luottoraja luotiin. Tämä kenttä päivitetään aina, kun luottorajaa muutetaan.
- Väliaikaiset luottorajat ohittavat asiakkaan kausikohtaisen luottorajan. Niitä käytetään luottorajan sijaan laskemaan kokonaisluottoraja. Nämä tiedot näkyvät vain, jos käytössä aktiivinen luottoraja. Voit lisätä tilapäisiä luottorajoja luottorajaoikaisuilla.
- **Vakuus tai takaukset** -kentässä on niiden vakuuksien ja takausten kokonaismäärä, jotka voivat nostaa asiakkaan luottorajaa.
- **Kokonaisluottoraja**-kentässä on asiakkaan lopullinen luottoraja. Kokonaisluottoraja sisältää vakuudet ja takaukset sekä väliaikaiset luottorajat.

## <a name="temporary-credit-limits"></a>Väliaikaiset luottorajat

Väliaikaiset luottorajat ohittavat asiakkaan määritetyn kauden luottorajat. Voit lisätä väliaikaisia luottorajoja luottorajaoikaisuilla. Luottorajaoikaisujen avulla luottopäälliköt voivat päivittää yhden asiakkaan, asiakasryhmän tai kaikkien asiakkaiden luottorajat ja vanhentumispäivät käyttämällä kirjausprosessia.

Voit luoda luottorajan oikaisumerkintöjä **Luottorajaoikaisut**-sivulla (**Luotonhallinta \> Luottorajaoikaisut \> Luottorajaoikaisut**).

## <a name="create-insurance-policies-and-guarantees"></a>Vakuussopimusten ja takausten luominen

Voit luoda kullekin asiakkaalle vähintään yhden vakuussopimuksen ja takauksen. Voit sitten laskea niiden avulla, minkälainen on yrityksesi riski, kun se antaa luottoa asiakkaalle. Vakuussopimukset ja takaukset voidaan sisällyttää myös asiakkaan luottorajaan.

Voit luoda vakuussopimuksia ja takauksia **Kaikki asiakkaat** -sivulla (**Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**). Valitse ensin asiakas ja valitse sitten toimintoruudussa **Luotonhallinta**-välilehdessä **Vakuus ja takaukset**.

> [!NOTE]
> Seuraavassa menettelyssä valitaan vakuuttaja tai takaaja yleisestä osoitekirjasta. Niinpä ennen tämän menettelyn aloittamista on varmistettava, että vakuuttajat ja takaajat on lisätty yleiseen osoitekirjaan.

1. Valitse **Tunniste**-kentässä **Takaus** tai **Vakuus**.
2. Valitse **Takauksen tai vakuuden tyyppi** -kentässä jokin aiemmin määritetyistä takaus- tai vakuustyypeistä.
3. Valitse **Vakuuttaja tai takaaja** -kentässä vakuuttaja tai takaaja yleisestä osoitekirjasta. 
4. Jos **Tunniste**-kentässä on valittu **Vakuus**, valitse **Sopimuksen kattavuustyyppi** -kentässä jokin aiemmin määritetyistä kattavuustyypeistä. Takaukselle ei voi valita sopimuksen kattavuustyyppiä.
5. Anna **Tunnus**-kentässä sopimuksen tunnus. Tämä tunnus on yleensä sopimusnumero.
6. Anna **Voimassa**-kentässä vakuussopimuksen tai takauksen aloituspäivä.
7. Anna **Päättyminen**-kentässä päivämäärä, jolloin vakuussopimus tai takaus. päättyy.
8. Anna **Arvo**-kentässä vakuussopimuksen tai takauksen arvo. Tämä arvo on sopimuksen täysi arvo.
9. Valitse **Valuutta** -kentässä sopimuksen arvon valuutta. 
10. Määritä **Päivitä luottoraja** -kentässä prosenttiosuudeksi **0**–**100**. Tätä prosenttiosuutta käytetään sopimuksen arvoon ja luottorajalaskelmissa käytettävää luottorajaa nostetaan tuloksena olevan summan verran. Laskettu arvo näkyy **Kokonaisluottoraja, vakuus ja takaukset** -kohdassa **Asiakkaat**-sivun **Luotonvalvonta**-pikavälilehdessä.

    Tässä on esimerkki:

    - Luottoraja (A) on 100 000.
    - Sopimuksen arvo (B) on 50 000.
    - **Päivitetty luottoraja** -prosentti (C) on 50,00.
    
    Tässä tapauksessa todellinen luottoraja is 125 000 (= A + \[B × C\]).

11. **Sisältyy riskiin** -valintaruudun valinta pienentää luottorajalaskelmiin käytettävää luottorajaa sopimuksen täydellä arvolla. Jos tämä valintaruutu valitaan, arvoa, joka lasketaan **Päivitä luottoraja** -prosenttia määritettäessä, ei käytetä luottorajalaskelmissa.

    Tässä on esimerkki:

    - Luottoraja (A) on 100 000.
    - Sopimuksen arvo (B) on 50 000.
    - **Päivitetty luottoraja** -prosentti (C) on 50,00.

    Tässä tapauksessa todellinen luottoraja is 125 000 (= A + \[B × C\]).
    
    Jos kuitenkin **Sisältyy riskiin** -valintaruutu valitaan, **Päivitä luottoraja** -kohdan arvo 50 000 (= 50,00 prosenttia 100 000:sta) poistetaan ja riskiarvoksi tulee 75 000 (= A + \[B × C\] – B).
