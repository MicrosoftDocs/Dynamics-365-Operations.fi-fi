---
title: Tuoterakenteet ja kaavat
description: "Tässä ohjeaiheessa on tietoja tuoterakenteista ja kaavoista, jotka ovat keskeinen osa tuotteiden ja tuotevarianttien määritelmää."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, EcoResProductProcessManufacturingWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19331
ms.assetid: c19b437a-2de2-4728-9477-2bcb0c2b1f5e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 430e2ab0c4438222ceb9102c011940af803acfbc
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="bills-of-materials-and-formulas"></a>Tuoterakenteet ja kaavat

[!INCLUDE [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja tuoterakenteista ja kaavoista, jotka ovat keskeinen osa tuotteiden ja tuotevarianttien määritelmää. Tuoterakenteet ja kaavat määrittävät tietyn tuotteen tarvittavat materiaalit tai ainesosat. Kaavoissa on myös oheis- ja sivutuotteita, jotka vastaanotetaan tietyn tuotannon yhteydessä. 

<a name="bills-of-materials"></a>Tuoterakenteet
------------------

Tuoterakenne (BOM) määrittää komponentit, joita tarvitaan, jotta tuote voidaan valmistaa. Komponentit voivat olla raaka-aineita, puolivalmiita tuotteita tai ainesosia. Joissakin tapauksissa palveluihin voidaan viitata tuoterakenteessa. Kuitenkin tuoterakenteet kuvailevat tyypillisesti tarvittavia *materiaaliresursseja*.  

Kun se on yhdistetty reititys tai tuotantovirtaan, joka kuvaa työvaiheita ja resursseja, joita tarvitaan rajentamaan tuote, tuoterakenne muodostaa perustan tuotteen kustannusarvion laskennassa.  

Tuoterakenne on yksittäinen yksikkö, joka on kuvattu seuraavanlaisesti:

-   BOM-tunnus
-   Tuoterakenteen nimi
-   Tuoterakennerivit, jotka kuvaavat komponentteja ja ainesosia
-   Tuoterakenneversiot, jotka määrittelevät tuotemallin ja ajanjakson, johon Tuoterakennetta käytetään

Yksittäinen Tuoterakenne kuvaa yhtä tasoa, jolla on yksilöllinen tunnus. Osilla voi olla omat tuoterakenteet, joihin viitataan tuoterakenneversioina. Voit näyttää ja muokata tuoterakenteiden koko hierarkian tietylle tuotteelle graafisessa rakennesuunnittelussa.

### <a name="formulas-co-products-and-by-products"></a>Kaavat, oheis- ja sivutuotteet

Kaava on tuoterakenteen alatyyppi, jota käytetään yleensä prosessivalmistuksessa. Kaava kuvaa oheistuotteita ja sivutuotteita komponenttien ja ainesosien lisäksi. Todellisessa versiossa kaavan oheis-ja sivutuotteiden määritys vaatii reseptin versiota. Kaava määritellään yleensä yhdelle tietylle valmiille tuotteelle (kaava tai suunnittelunimike), joka on määritetty reseptiversiossa.

### <a name="boms-in-the-product-lifecycle"></a>Tuoterakenteet tuotteen elinkaaressa

Tuotteen elinaikana monentyyppisiä tuoterakenteita voidaan luoda monista syistä:

-   **Tuoterakenteen ulkoasu tai luonnos** – tämä tuoterakenne antaa arvion tarvittavista materiaaleista aikaisessa suunnitteluvaiheessa ja auttaa tekemään karkean kustannusarvioinnin ja arvioi tuotemääritteet. Tätä tuoterakennetta ei yleensä käytetä yrityksen resurssien suunnittelussa (ERP).
-   **Tuotannon tuoterakenne** – tätä tuoterakennetta käytetään yleensä kun suunnitellaan tuotteita, jotka perustuvat jo olemassa oleviin tuoteportfolioihin. Tuotannon tuoterakenteet on muodostettu yksinkertaistamaan suunnitteluprosessia ja ryhmittämään monimutkaisia tuotteita tuotannon moduuleihin. Yksinkertaisille tuotteille voi ehkä olla mahdollista selvittää tuoterakenne varsinaiselle tuotantoprosessille. Kuitenkin, muita tuotteita varten, tekniikan tuoterakenne on muunnettava todelliseksi tuotannon tuoterakenteeksi. Tekniikan tuoterakenteet yleensä esitetään yleensä harhakuvina tuoterakenteen hierarkiassa. Vaikka tekniikan tuoterakenteita voidaan käyttää tuotannon toimien suunnitteluun ja suorittamiseen, tämä lähestymistapa voi aiheuttaa tehottomuutta, etenkin toistuvissa operaatioissa joissa luodaan useita tilauksia.
-   **Suunnittelun tuoterakenne** – tätä tuoterakennetta käytetään tarvelaskentasuunnittelua varten. Komponenttien ja ainesosien kysyntä lasketaan valmiiden tuotteiden kysyntään perustuen. Kuten kustannuslaskennan tuoterakenteet, suunnittelun tuoterakenteet saattavat edustaa tiettyä materiaalien yhdistelmää, jota käytetään sinä aikakautena.
-   **Tuotannon tuoterakenne** – tämä on se todellinen tuoterakenne, jota käytetään tietyssä tuotannossa. Tuotannon tuoterakenteen on otettava huomioon todelliset resurssit, joita käytetään tuotteen valmistuksessa. Luotaessa tuotantotilausta, erätilausta tai kanbania, tuoterakenteiden eri tasot, joita harhakuvat esittävät, tiivistyvät yhdelle tasolle ja ne jaetaan työvaiheisiin tilauksen ajalta.
-   **Hinnan tuoterakenne** – tätä tuoterakennetta käytetään tuotteen arvioitujen kustannusten laskemisessa. Esimerkiksi voit käyttää kustannuksen tuoterakennetta, kun standardikustannusta käytetään tai tietyn tuotteen suunnitellut arvioidut kustannukset lasketaan. Kustannuslaskennan tuoterakenteet voivat viitata materiaalien ja resurssien tiettyihin yhdistelmiin, jota on tarkoitus käyttää. Joten, voit käyttää kustannuksen tuoterakennetta luodaksesi kustannuslaskelmaversion tietylle kaudelle ja auttaaksesi välttämään eri aikoijen variansseja.

Tuoterakenteen tyypit, joita käytetään toteuttamisessa, määräytyvät toteutuksen mukaan, sekä myös yritysskenaarioiden ja vaatimuksien mukaan. Yksinkertaisissa toteutuksissa, suunnittelun tuoterakenne, tuotannon tuoterakenne ja kulujen tuoterakenne voidaan mallintaa yhtenä tuoterakenteena. Ympäristöissä, joissa on usein teknisiä muutoksia ja useita vaihtoehtoisia reittejä, suurempi joukko tuoterakennetyyppejä todennäköisesti tarvitaan.

### <a name="approval-of-boms-and-formulas"></a>Kaavojen ja tuoterakenteiden hyväksyminen

Kukin tuoterakenne ja kaava voidaan hyväksyä erikseen tai jättää hyväksymättä. Yleensä tuoterakenteen tai kaavan hyväksyminen tapahtuu, kun ensimmäinen olennainen tuoterakenneversio on hyväksytty. Kuitenkin joissakin liiketilanteissa nämä hyväksynnät voi olla prosessin eri vaiheita ja niihin saattaa liittyä erilaisia prosessin omistaja.  

Huomaa, että jos tuoterakenne on hyväksymistä odottava, myös kaikki siihen liittyvät tuoterakenneversiot ovat silloin hyväksymättömiä.

## <a name="bom-and-formula-versions"></a>Tuoterakenteen ja kaavan versiot
Liittääksesi tietyn tuotemallin tai kaavan valmistettavaan tuotevarianttiin, sinun on luotava tuoterakenneversio tai kaavaversio. Tuoterakenneversioiden ja kaavaversioiden voimassaoloaika voidaan rajoittaa kauden, määrän, toimipaikan, tietyn nimikedimension ja muiden ehtojen mukaan. Kaavaversioissa on lisäksi tärkeitä ominaisuuksia kuten tuotto, oheis- ja sivutuote määritykset ja kaavan kustannusten jako-ohjeet.

### <a name="approval-of-bom-and-formula-versions"></a>Tuoterakenteen ja kaavaversion hyväksyminen

Ennen kuin tuoterakenneversiota voidaan käyttää suunnittelu- ja tuotantoprosessissa, se pitää hyväksyä. Kun tuoterakenneversio on hyväksytty, siihen liittyvä tuoterakenne voidaan myös hyväksyä, riippuen käyttäjän valinta- ja todennusoikeuksista. Huomaa, että tuoterakenneversio voidaan hyväksyä vain, jos siihen liittyvä tuoterakenne on hyväksytty.

### <a name="activation-of-the-default-bom-or-formula-version"></a>Oletusarvo tuoterakenteen tai kaavaversion aktivointi

Määrittääksesi tietyn tuoterakenteen tai kaavan oletusarvo tuoterakenneversioksi tai kaavaversioksi, jota käytetään pääsuunnittelussa tai tuotantotilausten luomisessa, sinun on aktivoitava versio. Kun versio on käytössä, version yksilöllisyys vahvistetaan tietyille rajoituksille (esimerkiksi kausi, toimipaikka tai määrä). Näyttöön tulee virhesanoma jos yrität aktivoida version, joka on ristiriidassa aktiivisen version kanssa. Sitten sinun tulee joko poistaa ristiriitainen versio tai muokata version rajoituksia (yleensä kauden) estääksesi epäselvän aktivoinnin.

### <a name="product-change-with-case-management"></a>Tuotemuutoksen tapaushallinta

Tuotemallin vaihtaminen hyväksynnäksi ja uusien tai muuttuneiden tuoterakenteiden ja tuoterakenneversioiden aktivointi takaa helpon tavan nähdä tuoterakenneversion rajoitukset kokonaisuudessaan. Voit myö hyväksyä ja aktivoida kaikki tuoterakenteet ja kaavat, jotka liittyvät johonkin tiettyyn muutokseen yhdelle aktivointipäivämäärälle.

### <a name="alternative-bom-versions"></a>Vaihtoehtoiset tuoterakenneversiot

Joskus aktiivista tuoterakenneversiota tai kaavaversiota ei tule käyttää ennusteissa, myynnissä tai ylemmän tason tuotteissa. Tässä tapauksessa voit valita tietyn hyväksytyn tuoterakenteen osana vaatimusta (ennusterivin, myyntirivin tai tuoterakennerivin), jos hyväksytty tuoterakenneversio tai kaavaversio on olemassa vaihtoehtoiselle tuoterakenteelle tai kaavalle.  

Kun suunnitellut tilaukset, tuotantotilaukset tai kanbanit luodaan, suunnittelija tai työnohjauksen esimies voivat käyttää mitä vain hyväksyttyä tuoterakenneversiota, mikä on voimassa vaadittuna suunniteltuna tuotantotilauksen päivämääränä, suunnitellakseen tai tuottaakseen tietyn tuotteen. Tuoterakenneversion, jota käytetään, ei tarvitse olla aktivoitu tuoterakenneversion oletusarvona.

## <a name="bom-and-formula-lines"></a>Tuoterakenne ja kaavarivit
Tuoterakennerivi luodaan kaikelle materiaalille, palvelulle tai ainesosalle. Rivi määrittää tietyn tuotemallivariantin suunnitellun kulutuksen ja määrittää myös erilaisia tuntomerkkejä, jotka liittyvät suunniteltuun kulutukseen.  

Tuoterakenneriveissä voi olla seuraavanlaisia rivityyppejä: **Nimike**, **Haamu**, **Tarvekohdistettu tarjonta**, **Toimittaja**.

### <a name="item"></a>Nimike

Valitse **Nimike** -rivityyppi materiaaleille tai palveluille, jotka kulutetaan suoraan ja joita ei tarvitse hajoittaa enempää tai tarvekohdistetulle tarjonnalle.

### <a name="phantom"></a>Haamu

Valitse **Haamu** rivityyppi, kun haluat purkaa minkä tahansa alemman tason tuoterakennenimikkeen, joka sisältyy tuoterakenneriviin. Pääajoituksessa, suunniteltujen kustannusten laskennassa tai tuotantotilauksen arvioinnissa, joka käyttää **Haamu**-tuotantorakennerivejä, vanhempi tuoterakennerivi, joka viittaa tuotevarianttiin, jolla on haamu tuoterakenne, korvataan komponenttinimikkeillä jotka on listattu tuoterakenneriveinä kyseisessä tuoterakenteessa, kuten on sen tuotevariantin käytettävissä oleva aktiivinen tuoterakenneversio määrää. Jos tuotevariantilla on käyttökelpoinen aktiivinen reitti, sen reitityksen toimenpiteet yhdistetään pääreititykseen.  

Huomaa, että haamuja käytetään yleensä yksinkertaistamaan teknistä prosessia. Liiallinen monitasoinen haamutuoterakenteiden käyttö vaikuttaa suorituskykyyn, erityisesti paljon toistuvissa tuotantoskenaarioissa. Vältä haamujen suuria hierarkioita suorituskyvyn parantamiseksi. Sen sijaan, käytä ennalta hajotettuja tuotannon tuoterakenteita ja reitityksiä.

### <a name="pegged-supply"></a>Tarvekohdistuksen tarjonta

Valitse **tarvekohdistettu toimitus** -rivityyppi, kun haluat luoda osatuotannon, tuoterakenteen rivin tapahtuma kanbanin tai suoran ostotilauksen mille vain tuotemallin muuttujalle, johon tuoterakennerivi viittaa. Osatuotanto, tapahtuman kanban tai ostotilaus luodaan, kun arvioit tuotantotilauksen. Kuluttavaan tuotantotilaukseen varataan automaattisesti pakolliset nimikemäärät.

### <a name="vendor"></a>Toimittaja

Valitse **Toimittaja**-rivityyppi, jos tuotantoprosessi käyttää alihankkijaa ja haluat luoda alihankkijalle osatuotannon tai ostotilauksen automaattisesti.  

**Huomautus alihankintatoimenpiteistä tuoterakenteessa:** alihankkijan suorittama huolto tai työ on luotava huoltonimikkeenä, jota seurataan varaston seurannassa. Sinun on liitettävä huoltonimike yläkansioon tuoterakennerivinä. Reititykseen on sisällyttävä työvaihe, joka on liitetty alihankkijan operatiivisiin resursseihin.




