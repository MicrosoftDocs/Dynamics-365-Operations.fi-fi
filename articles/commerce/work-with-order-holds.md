---
title: Puhelinkeskuksen tilauspitojen määrittäminen ja käyttäminen
description: Tässä ohjeaiheessa käsitellään tilausten pitojen käyttämistä Dynamics 365 Commercein avulla.
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans, MCROrderEventSetup, MCROrderEventTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b11dd48ac629910a82b4d5bfdf9889809b0d829d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411987"
---
# <a name="configure-and-work-with-call-center-order-holds"></a>Puhelinkeskustilauksen pidon määrittäminen ja käyttäminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään puhelinkeskuksen tilauksissa käytettäviä Dynamics 365 Commercein tilauksen pitotoimintoja.

## <a name="configuring-call-center-order-holds"></a>Puhelinkeskuksen tilauspitojen määrittäminen

Puhelinkeskuksen tilauspitotoimintojen käyttöä varten on ensin määritettävä pitokoodit. Voit luoda yrityksen tarpeiden perusteella käyttäjän määrittämän pitokoodijoukon valitsemalla **Myynti ja markkinointi** \> **Määritys** \> **Myyntitilaukset** \> **Tilauksen pitokoodit**. Voit halutessasi merkintä jonkin pitokoodeista oletuspitokoodiksi valitsemalla kyseisen koodin **Myyntitilauksen oletusarvo** -asetuksiksi **Kyllä**. Tätä pitokoodia käytetään aina, kun pitokoodi asetetaan pitoon. Jos myyntilauksella on varattua varastoa ja varaukset on automaattisesti poistettava, jos tilaus asetetaan tietystä syytä pitoon, valitse syykoodien **Poista varastovarauksia** -asetukseksi **Kyllä**.

Voit määrittää minkä tyyppinen huomautus siepataan, kun myyntitilauksen pitoon asettavat käyttäjät lisäävät lisähuomautuksia, valitsemalla ensin **Myyntireskontra** \> **Määritys** \> **Myyntireskontran parametrit** ja määrittämällä sitten **Myynnin asetukset** -pikavälilehden **Yleiset**-välilehdessä **Huomautustyyppi**-kentän. Voit määrittää **Pidossa olevan myyntitilauksen tila** -kentässä millä värillä pidossa olevat myyntitilauksen korostetaan, kun näitä tilauksia katsotaan **Asiakaspalvelu**-sivulla.

Voit luoda valinnaisen pidon syykoodijoukon valitsemalla **Retail ja Commerce** \> **Kanavan asetukset** \> **Tietokoodit**. Näitä tietokoodeja voi käyttää toissijaisina syykoodeina, jotka tarkentavat pääpitokoodin määritystä. Voit luoda uuden syykoodijoukon valitsemalla **Uusi** ja määrittää sitten lisäsyiden luettelon valitsemalla **Alikoodit**. Voit linkittää minkä tahansa määrittämäsi tietokoodin puhelinkeskuskanavaan valitsemalla **Retail ja Commerce** \> **Kanavat** \> **Puhelinkeskukset** \> **Kaikki puhelunkeskukset**. Määritä **Yleiset**-pikavälilehdessä **Pitokoodi**-kenttä.

## <a name="putting-orders-on-hold"></a>Tilausten asettaminen pitoon

Puhelinkeskuksen käyttäjien taustatoimiston Commerce-ohjelmassa luomat tilaukset voidaan asettaa tietyissä tilanteissa pitoon manuaalisesti tai automaattisesti.

Puhelinkeskuksen käyttäjät haluavat ehkä asettaa tilauksen pitoon tilaustenkäsittelyn aikana ennen tilauksen lähettämistä ja vahvistamista, koska he haluavat estää sen vapauttamisen varastoon lisäkäsittelyä varten. Tilauksen tekevä asiakas ei ehkä ole valmis vahvistamaan tilausta tai tilauksen käsittelyn kannalta olennaisia tietoja puuttuu.

Puhelinkeskuksen käyttäjä voi asettaa tilauksen pitoon tilaustenkäsittelysivulla käyttämällä tilaustenkäsittelyvalikon **Myyntitilaus**-välilehden **Tilauksen pidot** -asetusta. Vaihtoehtoisesti käyttäjä voi valita **Pito**-valikkovaihtoehdon **Myyntilauksen yhteenveto** -sivulla. Tämä asetus on valittavissa, kun käyttäjä valitsee **Viimeistele** puhelinkeskuksen myyntitilauksessa.

Kummassakin tapauksessa avautuu **Tilausten pidot** -sivu. Käyttäjä sitten tilaukselle pidon valitsemalla **Uusi**. Käyttäjän on valittava **Pitokoodi**-kentässä koodi, joka vastaa parhaiten pidon syytä. Käyttäjä voi valita **Syykoodi**-kentässä myös lisäkoodin, jolla pidon kuvaukseen saadaan toinen taso.

Käyttäjä antaa **Huomautukset**-pikavälilehden **Pidon huomautukset** -kentässä vapaamuotoisia lisätietoja pidosta. Näistä huomautuksista on apua pitoon asetettua tilausta myöhemmin arvioivia tai käsitteleviä käyttäjiä.

Kun pidon tiedot on annettu ja tallennettu, käyttäjä voi sulkea **Tilausten pidot** -sivun. Käyttäjä siirretään sitten myyntitilausten käsittelysivulle. Jos myyntitilauksessa ei tarvitse tehdä muita toimintoja, käyttäjä voi sulkea myyntitilausten käsittelysivun.

Jos **Ota käyttöön tilausten viimeistely** -merkintä on otettu puhelinkeskuskanavassa käyttöön, maksua ei sovelleta pitoon asetettuun tilaukseen. Jos myyntitilausta ei sen sijaan ole asetettu pitoon, käyttäjät eivät voi poistua myyntitilauksen käsittelysivulta, ennen kuin maksua on käytetty. Maksu tietenkin edellytetään ennen tilauksen vapauttamista.

Puhelinkeskuksen työntekijät voivat asettaa manuaalisesti pitoon myös sellaiset tilaukset, jotka vaikuttavat jostain syytä epäilyttäviltä. Tilaukset voidaan asettaa pitoon myös automaattisesti, jos ne vastaavat aktiivisia petosehtoja ja -sääntöjä. Lisätietoja tästä tilausten pitotyypistä on kohdassa [Petoshälytysten määrittäminen](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts).

## <a name="viewing-and-managing-orders-that-are-on-hold"></a>Pitoon asetettujen tilausten näyttäminen ja hallinta

### <a name="viewing-hold-information-for-a-single-sales-order"></a>Yhden myyntitilauksen pitotietojen näyttäminen

Käyttäjät voivat tunnistaa **Asiakaspalvelu**-sivulla visuaalisesti pitoon asetetut tilaukset, koska tilausrivit on korostettu tietyn värisenä. Tämä väri määritetään **Pidossa olevan myyntitilauksen tila** -kentässä **Myyntireskontran parametrit** -sivulla.

> [!NOTE]
> Jos rivi valitaan sivulla, korostusväri ei ole näkyvissä.

Käyttäjät voivat selvittää myös myyntitilauksen tilan tietojen avulla, onko tilaus asetettu pitoon. Tilan tietoja voi tarkastella **Kaikki myyntitilaukset**- tai **Asiakaspalvelu**-sivulla. Jos tilaus on pidossa, sille valitaan **Älä käsittele** -merkintä ja **Tilan tiedot** -kentässä näkyy joko **Pidossa** tai **Petospito** skenaarion mukaan.

Käyttäjät voivat tarkastella yksittäisen tilauksen pitoa avaamalla **Tilaus pidossa**-sivun yksityiskohtaisen näkymän **Asiakaspalvelu**-sivulla. Sivu avataan valitun tilauksen **Asetukset**-valikon avulla. Käyttäjät pääsevät näkymään myös **Kaikki myyntitilaukset** -sivulta valitsemalla **Tilausten pidot** -valikkovaihtoehdon **Myyntitilaus**-välilehdessä.

### <a name="viewing-all-orders-that-are-on-hold"></a>Kaikkien pitoon asetettujen tilausten näyttäminen

Voit tarkastella kaikkia manuaalisesti tai automaattisesti pitoon asetettuja tilauksia valitsemalla **Retail ja Commerce** \> **Asiakkaat** \> **Tilausten pidot**.

**Tilausten pidot** -työtilassa on luettelonäkymä kaikista tilauksista, jotka ovat pidossa manuaalisten tai petoksiin liittyvien pitotoimien vuoksi. Käyttäjät voivat käyttää suodatuksen ja lajittelun perusasetuksia sellaisten näkymien luontiin, joissa he voivat käsitellä tai hallita pitokoodeja, joiden tarkistamisesta he vastaavat. **Tilausten pidot** -työtilassa näkee myös, kuinka monta päivää tilaus on ollut pidossa. Nämä tiedot auttavat priorisoimaan jonoa.

Käyttäjät saavat yksityiskohtaisemman näkymän pidossa olevista tilauksesta valitsemalla valikossa **Tilaus pidossa** -asetuksen. Tässä näkymässä on tietoja asiakkaasta sekä mahdollisesti tilausta, asiakasta tai pitotoimintoa koskevia huomautuksia. Näkymässä on myös tietoja automaattisen pidon syystä sekä siitä, asetettiinko tilaus pitoon, koska se vastasi petossääntöä.

Käyttäjät voivat tarkastella tai muokata muita tilaukseen liittyviä tietoja, kuten maksuja, yhteismääriä ja huomautuksia, kummassakin luettelonäkymässä ja **Tilausten pidot** -sivun yksityiskohtaisessa näkymässä.

**Pidä uloskuittaus** -välilehden asetukset voivat olla hyödyllisiä, jos useat käyttäjät käyttävät pitojonoa yrityksessä samanaikaisesti. Valitsemalla **Kuittaa ulos** -asetuksen, käyttäjät voivat ilmaista, että he ovat arvioimassa tilauksen pitoa ja tutustuvat siihen. Tällä tavoin muut käyttäjät eivät tuhlaa aikaa saman työn tekemiseen. Käyttäjät voivat tarkastella **Tilausten pidot**-sivun yksityiskohtaisessa näkymässä tietoja uloskuittauksen päivämäärästä tai ajasta sekä pitotietueen uloskuitanneesta käyttäjästä.

Kun pitotietue on kuitattu ulos, vain sen uloskuitannut käyttäjä voi poistaa uloskuittauksen. Tämän rajoituksen tarkoitus on estää käyttäjiä ottamasta tietueita, joita muut käyttäjät jo käsittelevät. Tietueen uloskuitannut käyttäjä vapauttaa tilauksen takaisin jonoon muiden käyttäjien käsiteltäväksi valitsemalla **Poista uloskuittaus** -asetuksen.

> [!NOTE]
> Pitoa ei vapauteta, kun uloskuittaus poistetaan.

Joissakin tilanteissa, esimerkiksi käyttäjän ollessa sairaana tai hänen vaihtaessaan työpaikkaa, kyseisen käyttäjän uloskuittaamat tietueet on ehkä määritettävä toiselle käyttäjälle. Esimies voi määrittää tietueet uudelleen **Ohita uloskuittaus** -asetuksella.

## <a name="releasing-orders-that-are-on-hold"></a>Pitoon asetettujen tilausten vapauttaminen

Sekä luettelonäkymän että **Tilausten pidot** -sivun yksityiskohtaisen näkymän **Vapauta pito** -välilehdessä on asetuksia, joilla tilauksen pito vapautetaan. Voit vapauttaa tilauksen valitusta pitokoodista **Vapauta pidot** -asetuksella.

Puhelinkeskusten tilaukset edellyttävät maksua. Pitoa ei tämän vuoksi voi poistaa kokonaan, jos maksua ei ole kohdistettu tilaukseen. Varmista **Puhelinkeskuksen parametrit** -sivun **Pidot**-välilehdessä, että **Lähetä vapautettaessa** -parametri on otettu käyttöön. Tämä asetus auttaa varmistamaan, että pidosta vapautettu tilaus siirtyy oikeaan tilauslogiikkaan, jossa maksut tarkistetaan ja valtuutetaan. Jos maksut puuttuvat, käyttäjä vastaanottaa virheen eikä pitokoodia poisteta.

Jos **Lähetä vapautettaessa** -parametria ei ole määritetty, käyttäjien on valittava **Vapauta ja lähetä** -asetus **Vapauta pito** -valikossa. Tämä auttaa varmistamaan, että kaikkia tarvittavia maksutarkistuksia käytetään tilauksessa. Jos tilauksen lähettäminen epäonnistuu, kun **Ota käyttöön tilausten viimeistely** -merkintä on otettu käyttöön puhelinkeskuskanavassa, tilaus vapautetaan pitotilasta, mutta **Älä käsittele** -merkintä pysyy määritettynä. Tilausta ei näin ollen vapauteta varastoon, ennen kuin oikeat maksut on kohdistettu ja tarkistettu.

Jos käyttäjät haluavat poistaa pidon mutta tehdä tilaukseen muutoksia ennen sen vapauttamista lisäkäsittelyyn, he voivat valita **Vapauta ja muokkaa** -asetuksen. Tämä asetus poistaa pitokoodin ja avaa myyntitilauksen tiedot, joten käyttäjät voivat tehdä muutoksia tilaukseen. Käyttäjät voivat myös kohdistaa maksun ja lähettää myyntitilauksen maksun tarkistuslogiikan kautta, kun **Ota käyttöön tilausten viimeistely** -merkintä on otettu käyttöön puhelinkeskuskanavassa.

## <a name="reporting-options"></a>Raportointivaihtoehdot

Valitse **Retail ja Commerce** \> **Kyselyt ja raportit** \> **Puhelinkeskuksen raportit** \> **Tilausten pitoraportti**, jos haluat suorittaa tilauspitoja koskevan raportin päivämääräalueen, pitokoodin tai muiden liittyvien ehtojen perusteella.
