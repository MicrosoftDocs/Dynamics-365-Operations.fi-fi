---
title: "Käyttöomaisuuden integrointi"
description: "Käyttöomaisuus voidaan integroida kirjanpitoon, varastonhallintaan, myyntireskontraan ja ostoreskontraan. Käyttöomaisuuden voi integroida myös ostotilauksiin."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3501
ms.assetid: f0639053-d99c-432a-8ead-5c26e0d4eaec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 305010c41aa87222c652f98e6aa2b097606052e8
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="fixed-assets-integration"></a>Käyttöomaisuuden integrointi

[!include[banner](../includes/banner.md)]


Käyttöomaisuus voidaan integroida kirjanpitoon, varastonhallintaan, myyntireskontraan ja ostoreskontraan. Käyttöomaisuuden voi integroida myös ostotilauksiin.

<a name="general-ledger"></a>Kirjanpito
--------------

Kirjanpidossa käyttöomaisuus esitetään yleensä arvon yhteenvetona useilla pääkirjanpitotileillä, joita tarvitaan tilinpäätöksissä. **Käyttöomaisuus**-sivulla voit kuitenkin luoda useita käyttöomaisuustietueita. Näihin tietueisiin voi sisältyä tietoja, kuten hankintahinta, poisto ja arvostus. Aina kun kirjaat käyttöomaisuustapahtuman, asianmukaiset päätilit päivitetään. Käyttöomaisuuden päätileillä näkyy aina käyttöomaisuuden päivitetty arvo.

**Käyttöomaisuuserän kirjausprofiilit** -sivulla määritetään ensisijaiset tilit, joille käyttöomaisuuskirjan tapahtumat kirjataan. Voit myös määrittää ne käyttöomaisuustapahtumien tyypit, jotka kirjataan päätileille. Voit luoda erilaisia ensisijaisen tilit yhdistelmiä käyttöomaisuudelle sen mukaan, minkä tietotason haluat käyttöomaisuudelle kirjanpitoon. Päätilit voidaan määrittää perustumaan tapahtumatyyppeihin, kirjoihin ja muihin päätileihin.

## <a name="inventory-management"></a>Inventoinnin- ja varastonhallinta
Käyttöomaisuuden varastokirjauskansiossa voit kirjoittaa käyttöomaisuuden hankinnan, jonka yritys on tuottanut tai valmistanut itselleen. Tämän jälkeen voit siirtää varastonimikkeet käyttöomaisuuteen joko hankintana tai osana hankintaa. 

Käyttöomaisuuseriä voi hankkia myös ostotilauksia käyttäen. Kun ostotilauksissa on käyttöomaisuuseriksi määritettyjä varastonimikkeitä, **Salli käyttöomaisuuden hankinta ostosta** -vaihtoehdon asetus **Käyttöomaisuuden parametrit** -sivulla määrittää, kirjataanko hankinta käyttöomaisuuserälle laskun kirjaamisen yhteydessä. Käyttöomaisuuden hankinnan vaikutus varastoon riippuu yrityksen asetuksista. 

Kun varastonimikkeestä tulee käyttöomaisuushankinta varastokirjauskansion, ostotilauksen tai hankintaehdotuksen kautta, käyttöomaisuuskirjan hankintatapahtuma muodostetaan. Jos kirjan hankinta sisältää johdetun kirjan, luodaan myös johdetun kirjan hankintatapahtuma. 

**Kirjaus**-sivulla varastonhallinnassa määritetyt kirjaussäännöt määrittävät varastovähennyksen, kun hankinta kirjataan. Varastovähennystä ei kuitenkaan aina tarvitse tehdä, kun käyttöomaisuuseriin liittyviä laskuja kirjataan. Joissakin tilanteissa käyttöomaisuuseriä voidaan ostaa sisäiseen käyttöön. Esimerkiksi kannettavan tietokoneen voi ostaa myyntiosaston käyttöön. Kun ostotilauksia käsitellään, voit käyttää nimikkeitä, jotka määritetty sekä jälleenmyyntiin että sisäiseen käyttöön. 

Jos käytätä nimikeryhmien käyttöomaisuuserissä tiettyjä vastaanotto- ja varasto-ottotilejä, samaa varastonimikettä voi käyttää sekä sisäisissä ostoissa että jälleenmyyntivarastossa. 

Sisäiseen käyttöön tarkoitetun käyttöomaisuuden tilityypiksi määritetään**Käyttöomaisuuden vastaanotto**. Tätä tilityyppiä käytetään seuraamaan käyttöomaisuuden vastaanottamista. Kun kirjaat toimittajalaskun, käytä käyttöomaisuuserän vastaanottotiliä, jos jokin seuraavista ehdoista toteutuu:

-   Laskurivi sisältää olemassa olevan käyttöomaisuuden sisäisiin tarkoituksiin.
-   **Uusi käyttöomaisuus?** -valintaruutu valitaan kirjatulle tuotteen vastaanottoriville.
-   **Luo uusi käyttöomaisuuserä** -valintaruutu valitaan toimittajan laskuriville.

Tämä tili on tavallisesti kulutili. **Käyttöomaisuuden vastaanotto** -tilityypin voi määrittää joko nimikeryhmälle tai yksittäiselle nimikkeelle **Ostotilaus**-välilehdessä **Nimikeryhmä**- tai **Kirjaus**-sivulla.

Vastaavasti sisäiseen käyttöön tarkoitetun käyttöomaisuuden tilityypiksi voidaan määrittää **Käyttöomaisuuden otto**. Tätä tilityyppiä käytetään seuraamaan käyttöomaisuuden myöntämistä vastaanottajalle. Kun käyttöomaisuuserä hankitaan ostotilausta käyttämällä, käyttöomaisuuden oton tili toimii käyttöomaisuuden debet-tilin vastatilinä. Käyttöomaisuushankinnan voi kirjata joko toimittajan laskun kirjauksen yhteydessä tai kun kirjaat käyttöomaisuushankinnan Käyttöomaisuus-kirjauskansiossa käyttämällä vaikkapa hankintaehdotusta. **Käyttöomaisuuden otto** -tilityypin voi määrittää joko nimikeryhmälle tai yksittäiselle nimikkeelle **Varasto**-välilehdessä **Nimikeryhmä**- tai **Nimikekirjaus**-sivulla. 

Kirjaukseen käytettävät päätilit määräytyvät lopulta nimikemalliryhmälle määriteltyjen kirjanpidon integrointiasetusvaihtoehtojen mukaan. Lisäksi, käytettävät päätilit muuttuvat, riippuen siitä, onko käyttöomaisuus määritetty ostotilausriville. Tilit ovat peräisin kunkin nimikeryhmän kirjausprofiilista. 
**Huomautus:** Jos varastovarauksia on käytössä tuotteen vastaanoton kirjauksen yhteydessä, käyttöomaisuuserää ei voi määrittää eikä riviltä voi luoda käyttöomaisuuserää. 

Siihen, mille tileille käyttöomaisuustapahtumat kirjataan, vaikuttaa kaksi tekijää: onko omaisuuserä ostettu vai yrityksen valmistama, sekä käyttöomaisuustapahtuman laji. 

Tapahtumalaji liittää varastotapahtuman käyttöomaisuuden kirjausprofiiliin. Käyttöomaisuuden kirjausprofiili määrää, mitä tilejä päivitetään, joten käyttöomaisuuden tapahtumalajin valinta on epäsuoraan myös niiden päätilien valinta, joille tapahtuma kirjataan. Sekä valmistettujen että ostettujen käyttöomaisuuserien tapahtumatyyppi on yleensä **Hankinta** tai **Hankintaoikaisu**.

## <a name="accounts-receivable"></a>Myyntireskontra
Käyttöomaisuuden integrointi myyntireskontran kanssa käyttää kirjausprofiileita, jotka on määritetty käyttöomaisuudessa. Nämä kirjausprofiilit aktivoidaan, kun käyttöomaisuus, kirja ja käyttöomaisuuden tapahtumatyyppi valitaan myyntilaskulle ennen myyntilaskun kirjausta. Käyttöomaisuuserät eivät kuulu varastonhallintaan, joten käytä **Vapaatekstilasku**-sivua, kun myyt käyttöomaisuuserän. 

Jos kirjaan sisältyy johdettu kirja, luodaan asiakkaan laskun kirjauksen yhteydessä myös johdetun kirjan tapahtuma.

## <a name="accounts-payable"></a>Ostoreskontra
Yleensä käyttöomaisuuserät hankitaan ulkoisilta toimittajilta. **Käyttöomaisuuden parametrit** -sivulla voit määrittää, kirjataanko käyttöomaisuushankinnat aina toimittajien laskujen kirjaamisen yhteydessä vai voiko käyttöomaisuushankintoja kirjata vain käyttöomaisuudesta. Jos käyttöomaisuuden kirjaaminen ostoreskontrasta sallitaan, käyttöomaisuustilit päivitetään aina, kun käyttöomaisuushankinnan toimittajalasku kirjataan. 

Jos järjestelmä kirjaa käyttöomaisuuden hankinnan, kun lasku kirjataan, tapahtuma kirjataan käyttöomaisuuden tapahtumalajeille määritettyjen kirjausprofiilien mukaan. Kirjausta ohjaa käyttöomaisuus, kirja ja käyttöomaisuuden tapahtumatyyppi, jotka valitaan **Ostotilaus**-sivulta ennen toimittajan laskun kirjaamista. 

Jos kirjaan sisältyy johdettu kirja, luodaan toimittajan laskun kirjauksen yhteydessä myös johdetun kirjan tapahtuma.

Jokaisen tilausrivin integrointi aktivoidaan **Käyttöomaisuus**-välilehdessä **Ostotilaus**-sivun **Rivin erittely** -pikavälilehdessä. Voit lähettää käyttöomaisuuden ostotilauksen toimittajalle. Käyttöomaisuus ja ensisijaiset tilit päivitetään vasta, kun toimittajalasku kirjataan, sitten kun käyttöomaisuus vastaanotetaan. Ostotilaukset voivat sisältää vain varastonimikkeitä, joten käyttöomaisuuden hankinnan vaikutus varastoon riippuu yrityksen asetuksista.

## <a name="project-management-and-accounting"></a>Projektinhallinta ja kirjanpito
Voit liittää projektin käyttöomaisuuserään, johon projekti vaikuttaa. Voit myös liittää kunkin vaiheen, tehtävän tai aliprojektin eri käyttöomaisuuserään. Jokaiseen projektitietueeseen voidaan liittää yksi käyttöomaisuus. Voit luoda liitoksen, kun kirjoitat käyttöomaisuuden numeron **Projektit**-sivulla olevaan **Käyttöomaisuuserän numero** -kenttään. Projektityypin on oltava **Sisäinen** tai **Kustannusprojekti**. 

Voit tarkastella projekteihin liittyvien käyttöomaisuuserien tietoja myös **Projektit**-sivulla. Kun haluat tarkastella käyttöomaisuustietuetta, napsauta omaisuuserän linkkiä **Käyttöomaisuus**-sivun **Asetukset**-pikavälilehdessä. Valitsemalla sitten **Projektit** &gt; **Kaikki projektit** voit tarkastella käyttöomaisuuserään liittyviä projekteja. 

Käyttöomaisuuserät liitetään tavallisesti projekteihin, kun projektit liittyvät työhön, ylläpitoon tai käyttöomaisuuserän parannuksiin. Kun projekti on valmis, käyttöomaisuudelle ei automaattisesti tehdä kirjanpitoarvon korotusta. Jos kirjanpitoarvon korottamista vaaditaan, sinun on luotava se manuaalisesti. 

Voit poistaa projektin ja käyttöomaisuuden välisen liitoksen poistamalla **Projektit**-sivulla **Käyttöomaisuuserän numero** -kentän arvon. 

Voit myös määrittää käyttöomaisuuserän, jota luot tai valmistat arviointiprojektiin kuuluvana. Arviointiprojektin päätteeksi voit kirjata automaattisesti käyttöomaisuuden hankintatapahtuman.

Lisätietoja on ohjeaiheessa [Hankkia omaisuuseriä hankintojen kautta](acquire-assets-procurement.md).




