---
title: Reititykset ja työvaiheet
description: Tämä aihe sisältää yleisiä tietoja reitityksistä ja työvaiheista.
author: sorenva
manager: tfehr
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable, ProdRouteJob, ProdRouteTrans, ProdRouteOverview, ProdRouteJobOverview, ProdRouteJobListPagePreviewPane, RouteTable, RouteVersionFeasibility, ProdRouteJobCurrent, RouteGroup, RouteProductionOrder, EngChgCaseRouteTablePart, EcoResProductProdTypeFormulaNoActiveRouteFormPart,
ms.author: sorenand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: daed55821617e688811ffc33ee8bc2847c37c242
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986576"
---
# <a name="routes-and-operations"></a>Reitit ja työvaiheet

[!include [banner](../includes/banner.md)]

Tämä aihe sisältää yleisiä tietoja reitityksistä ja työvaiheista. Reititys määrittää tuotteen tai tuotevariantin tuotantoprosessin. Siinä kuvaillaan tuotantoprosessin jokainen vaihe (työvaihe) ja vaiheiden suoritusjärjestys. Reitityksessä määritetään myös jokaisen vaiheen pakolliset operatiiviset resurssit, vaadittu asetus- ja ajoaika sekä kustannusten laskemistapa.

<a name="overview"></a>Yleiskuvaus
--------

Reititys osoittaa tuotteen tai tuotevariantin tuottamisessa vaadittujen työvaiheiden järjestyksen. Reititys määrittää myös jokaisen työvaiheen vaaditut operatiiviset resurssit, työvaiheen asetukseen ja ajoon kuluvan ajan ja kustannusten laskentatavan. Samaa reititystä voi käyttää useiden tuotteiden tuotannossa. Kullekin tuotteelle tai tuotevariantille voi kuitenkin luoda myös yksilöllisen reitityksen. Tietyllä tuotteella voi myös olla useita reitityksiä. Tällöin käytettävä reititys vaihtelee usein sen mukaan, miten paljon tuotetta valmistetaan. Supply Chain Managementin reitityksen määritys sisältää neljä seuraavaa erillistä elementtiä, jotka yhdessä muodostavat tuotantoprosessin:

- **Reititys** – Reititys määrittää tuotantoprosessin rakenteen. Toisin sanoen se määrittää työvaiheiden järjestyksen.
- **Työvaihe** – Työvaihe tunnistaa reitissä nimetyn vaiheen, kuten **kokoonpanon**. Sama työvaihe voi esiintyä useissa reitityksissä ja sillä voi olla useita työvaihenumeroita.
- **Työvaihesuhde** – Työvaihesuhde määrittää työvaiheen operatiiviset ominaisuudet, kuten asetus- ja ajoajan, kustannusluokat, kulutuksen parametrit ja resurssivaatimukset. Työvaihesuhteen vuoksi työvaiheen operationaaliset ominaisuudet voivat vaihdella sen mukaan, missä reitityksessä työvaihetta käytetään tai valmistettavien tuotteiden mukaan.
- **Reititysversio** – Reititysversio määrittää reitityksen, jota käytetään tuotteen tai tuotevariantin tuottamisessa. Reititysversio mahdollistaa reititysten käyttämisen uudelleen tuotteissa tai reitityksen muuttamisen ajan kuluessa. Reititysversiot mahdollistavat myös eri reititysten käyttämisen saman tuotteen tuottamisessa. Tällöin käytettävä reititys riippuu eri tekijöistä, kuten sijainnista ja tuotettavasta määrästä.

## <a name="routes"></a>Reititykset
Reititys osoittaa tuotteen tai tuotevariantin tuottamisessa käytettävien työvaiheiden järjestyksen. Jokaiselle työvaiheelle määritetään työvaihenumero ja seuraava työvaihe. Työvaiheiden järjestys muodostaa reittiverkoston, joka voidaan esittää suunnatussa kaaviossa, jolla on vähintään yksi aloituspiste ja yksi päätepiste. Supply Chain Managementissa reititykset erotetaan toisistaan rakennetyypin perusteella. Reititystyypit ovat yksinkertainen reititys ja reittiverkosto. Tuotannonohjauksen parametrien avulla voi määrittää, ovatko käytössä ainoastaan yksinkertaiset reititykset vai myös monimutkaisemmat reittiverkostot.

### <a name="simple-routes"></a>Yksinkertaiset reititykset

Yksinkertaiset reititykset ovat peräkkäisiä. Reitityksellä on vain yksi aloituspiste.  

[![Yksinkertainen reititys](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Jos tuotannonhallinnan parametreissa otetaan käyttöön vain yksinkertaiset reititykset, Supply Chain Management luo automaattisesti työvaihenumerot (10, 20, 30 jne.) reitityksen määrittämisen yhteydessä.

### <a name="route-networks"></a>Reittiverkostot

Jos tuotannonohjauksen parametreissa otetaan käyttöön monimutkaisempia reittiverkostoja, voit määrittää useita aloituspisteitä ja rinnakkain suoritettavia työvaiheita sisältävät reititykset.  

[![Reittiverkosto](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

> [!NOTE]
> - Jokaisella työvaiheella voi olla vain yksi seuraava työvaihe. Koko reitityksen on loputtava yhteen työvaiheeseen.
> - Vaikka useilla työvaiheilla olisi sama seuraava työvaihe (esimerkiksi työvaiheet 30 ja 40 edellä olleessa kuvassa), niitä ei voida taata, että ne suoritettaisiin rinnakkain. Resurssien saatavuus ja kapasiteetti saattaa rajoittaa tapaa, joilla työvaiheet ajoitetaan.
> - Työvaihenumerona ei voi käyttää nollaa (0). Kyseinen numero on varattu. Sitä käytetään määritettäessä tilanne, jossa reitityksen viimeisellä työvaiheella ei ole seuraavaa työvaihetta.

### <a name="parallel-operations"></a>Rinnakkaiset työvaiheet

Joskus työvaiheen suorittaminen vaatii useita erilaisia ominaisuuksia omaavien operatiivisten resurssien yhdistelmän. Esimerkiksi kokoonpanotyövaihe saattaa vaatia koneen, työkalun ja yhden työvaihetta valvovan työntekijän joka toiselle koneelle. Tämä esimerkki voidaan mallintaa käyttämällä rinnakkaisia työvaiheita, joissa yksi työvaihe on määritetty ensisijaiseksi työvaiheeksi ja muut toissijaisiksi.  

[![Reititys, jolla on ensisijainen työvaihe ja toissijaisia työvaiheita](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Yleensä ensisijainen työvaihe edustaa pullonkaularesurssi. Se määrittää toissijaisten työvaiheiden ajoajan. Jos kapasiteetti kuitenkin on rajallinen, sekä ensisijaiselle työvaiheelle että toissijaisille työvaiheille ajoitettujen resurssien on oltava käytettävissä ja niillä on oltava vapaata kapasiteettia samanaikaisesti.  

Sekä ensisijaisella työvaiheella että toissijaisilla työvaiheilla on oltava sama työvaihenumero (30 edellä olevassa kuvassa).  

Ensisijaisen työvaiheen (30) resurssivaatimus edellisessä kuvassa on kone, kun taas toissijaisten työvaiheiden (30' ja 30'') resurssivaatimukset ovat työkalu ja työntekijä. 50 prosentin kuormitus auttaa varmistamaan, että ajoitettu työntekijä voi valvoa kahta konetta samanaikaisesti.

### <a name="approval-of-routes"></a>Reititysten hyväksyntä

Reititys on hyväksyttävä, ennen kuin sitä voidaan käyttää suunnittelu- ja tuotantoprosessissa. Hyväksyntä osoittaa, että reitityksen suunnittelu on valmis. Tietyllä vapautetulla tuotteella tai vapautetulla tuotevariantilla voi olla useita hyväksyttyjä reitityksiä. Yleensä reitityksen hyväksyminen tapahtuu, kun ensimmäinen olennainen reititysversio on hyväksytty. Joissakin liiketoimintaskenaarioissa reitityksen hyväksyntä ja reititysversio ovat kuitenkin erillisiä aktiviteetteja, jotka saattavat liittyä erilaisia prosessin omistajia.  

Kukin reititys voidaan hyväksyä erikseen tai jättää hyväksymättä. Huomaa kuitenkin, että jos reititys on hyväksymistä odottava, myös kaikki siihen liittyvät reititysversiot ovat silloin hyväksymättömiä. Tuotannonohjauksen parametreissa määritetään, voivatko reititykset olla hyväksymättömiä ja voiko hyväksyttyjä reitityksiä muuttaa.  

Jos ylläpidät lokia, johon tallennetaan kunkin reitityksen hyväksyjä, voit vaatia reitityksen hyväksynnästä sähköiset allekirjoitukset. Käyttäjien on tällöin vahvistettava henkilöllisyytensä [sähköisen allekirjoituksen](../../fin-and-ops/organization-administration/electronic-signature-overview.md) avulla.

## <a name="operations"></a>Operations
Työvaihe on tuotantoprosessin vaihe. Jokaisella työvaiheella on tunnus ja yksinkertainen kuvaus. Seuraavissa taulukoissa esitellään tyypilliset esimerkit konepajan työvaiheista.

| Työvaihe  | kuvaus        |
|------------|--------------------|
| PipeCut    | Putkien leikkaaminen       |
| TIGweld    | TIG-hitsaus        |
| JigAssy    | Kiinnittimen kokoonpano       |
| Tarkastus | Laatutarkastus |

Työvaihesuhde määrittää työvaiheen operatiiviset ominaisuudet, kuten asetus- ja ajoajan, resurssivaatimukset, kustannustiedot ja kulutuksen laskennan. (Lisätietoja työvaihesuhteista on seuraavassa osassa.)

## <a name="operation-relations"></a>Työvaihesuhteet
Työvaiheen seuraavia operationaalisia ominaisuuksia ylläpidetään työvaihesuhteessa:

- Kustannusluokat
- Kulutuksen parametrit
- Käsittelyajat
- Käsiteltävät määrät
- Resurssivaatimukset
- Huomautukset ja ohjeet

Voit määrittää useita työvaihesuhteita samalle työvaiheelle. Kukin työvaihesuhde koskee kuitenkin yhtä tiettyä työvaihetta. Se tallentaa nimikeryhmään liittyvän reitityksen, vapautetun tuotteen tai vapautettujen tuotteiden joukon ominaisuudet. Tämän vuoksi samaa työvaihetta voidaan käyttää useissa reitityksissä, joilla on erilaiset operationaaliset ominaisuudet. Lisäksi päätietojen ylläpitäminen on helpompaa, jos käytössä on vakiotyövaiheet, joilla on samat operationaaliset ominaisuudet riippumatta käytettävästä reitityksestä ja valmistettavasta tuotteesta. Työvaihesuhteen vaikutusalue määritetään **Nimikekoodi**, **Nimikesuhde**-, **Reitityskoodi**- ja **Reitityssuhde**-ominaisuuksien avulla seuraavassa taulukossa esitetyllä tavalla.

| Nimikekoodi | Nimikkeen suhde         | Reitityskoodi | Reitityssuhde   | Työvaihesuhteen vaikutusalue                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Taulu     | &lt;Nimikkeen tunnus&gt;       | Reititys      | &lt;Reittitunnus&gt; | Työvaiheen operationaaliset ominaisuudet, kun niitä käytetään reitityksessä, jonka **reititysnumero**=&lt;reitityksen tunnus&gt; ja valmistetaan vapautettua tuotetta, jonka **nimikenumero**=&lt;nimikkeen tunnus&gt;.                                                                                                                        |
| Taulu     | &lt;Nimikkeen tunnus&gt;       | Kaikki        |                  | Työvaiheen operationaaliset oletusominaisuudet, kun niitä käytetään reitityksessä, jonka **nimikenumero**=&lt;nimikkeen tunnus&gt;. Toisin sanoen näitä operationaalisia ominaisuuksia käytetään, kun vapautetulla tuotteella ei ole reitityskohtaista työvaihesuhdetta.                                     |
| Ryhmä     | &lt;Nimikeryhmän tunnus&gt; | Reititys      | &lt;Reittitunnus&gt; | Työvaiheen operationaaliset ominaisuudet, kun sitä käytetään reitityksessä, jossa **reititysnumero**=&lt;reitityksen tunnus&gt;, kun valmistetaan vapautettuja tuotteita, jotka on liitetty nimikeryhmään &lt;nimikeryhmän tunnus&gt;, jos vapautetulla tuotteella ei ole reitityskohtaista työvaihesuhdetta.                         |
| Ryhmä     | &lt;Nimikeryhmän tunnus&gt; | Kaikki        |                  | Työvaiheen operationaaliset oletusominaisuudet, kun sitä käytetään valmistettaessa vapautettuja tuotteita, jotka on liitetty nimikeryhmään &lt;nimikeryhmän tunnus&gt;, jos yksityiskohtaisempaa työvaihesuhdetta ei ole.                                                                                                  |
| Kaikki       |                       | Reititys      | &lt;Reittitunnus&gt; | Työvaiheen operationaaliset oletusominaisuudet, kun sitä käytetään reitityksessä, jonka **reititysnumero**=&lt;reitityksen tunnus&gt;. Toisin sanoen näitä operationaalisia ominaisuuksia käytetään, kun tällä reitityksellä, joka on määritetty joko vapautetulle tuotteelle tai siihen liitetylle nimikeryhmälle, ei ole työvaihesuhdetta. |
| Kaikki       |                       | Kaikki        |                  | Työvaiheen operatiiviset oletusominaisuudet. Näitä operationaalisia ominaisuuksia käytetään, kun yksityiskohtaisempaa työvaihesuhdetta ei ole määritetty.                                                                                                                                                                |

Voit määrittää myös toimipaikkakohtaisen työvaihesuhteen. Työvaiheen operationaaliset ominaisuudet voivat siis vaihdella työvaiheen suoritussijainnista (eli toimipaikasta) riippuen. Määritetyille tuotteille voidaan määrittää myös erilaisia operationaalisia ominaisuuksia kullekin tuotekonfiguraatiolle.  

Työvaihesuhteiden avulla reititysten määrittäminen on joustavaa. Oletusominaisuuksien määritysmahdollisuuden avulla ylläpidettävien päätietojen määrä vähenee. Joustavuus tarkoittaa kuitenkin myös sitä, että työvaihesuhteen konteksti, jota muokataan, on otettava huomioon.  

> [!NOTE]
> Koska operationaaliset ominaisuudet tallennetaan työvaihesuhteisiin reitityksen ja työvaiheen perusteella, kaikilla saman työvaiheen esiintymillä (esimerkiksi kokoonpanolla) on sama asetus- ja ajoaika ja resurssivaatimukset. Jos siis työvaiheen kaksi esiintymää löytyvät samasta reitityksestä, mutta niillä on eri ajoajat, niille on luotava kaksi erillistä työvaihetta, kuten esimerkiksi Kokoonpano1 ja Kokoonpano2.

### <a name="modifying-product-specific-routes"></a>Tuotekohtaisten reititysten muokkaaminen

Kun avaat **Reititys**-sivun **Vapautetun tuotteen tiedot** -sivulla, sivulla näkyvät valittuun vapautettuun tuotteeseen liittyvät reititysversiot. Tässä kontekstissa Supply Chain Management näyttää jokaisen työvaiheen toiminalliset ominaisuudet reititysversiota parhaiten vastaavasta työvaihesuhteesta. Työvaiheluettelo sisältää työvaihesuhteen **Nimikekoodi**- ja **Reitityskoodi**-ominaisuudet. Tämän vuoksi määritetään, mikä työvaihesuhde näytetään.  

**Reititys**-sivulla voi muokata työvaiheen operationaalisia ominaisuuksia, kuten ajoaika ja kustannusluokat. Muutokset tallennetaan työvaihesuhteeseen, joka liittyy reititykseen ja vapautettuun tuotteeseen, johon nykyisessä reititysversiossa viitataan. Jos näytettävä työvaihesuhde ei liity reititykseen ja vapautettuun tuotteeseen, järjestelmä luo työvaihesuhteesta kopion ennen muutosten tallentamista. Tämä kopio *on* liittyy reititykseen ja vapautettuun tuotteeseen. Tämän vuoksi muutokset eivät vaikuta muihin reitityksiin tai vapautettuihin tuotteisiin. Voit varmistaa **Reititys**-sivulla muokattavan työvaihesuhteen **Nimikekoodi**- ja **Reitityskoodi**-kentän avulla.  

Voit myös luoda manuaalisesti työvaiheen, joka liittyy reititykseen ja vapautettuun tuotteeseen, käyttämällä **Kopioi suhde ja muokkaa sitä** -toimintoa.  

> [!NOTE]
> Jos lisäät reititykseen uuden työvaiheen **Reititys**-sivulla, työvaihesuhde luodaan vain nykyiselle vapautetulle tuotteelle. Jos siis reititystä käytetään myös muiden vapautettujen tuotteiden valmistamisessa, näille vapautetuille tuotteille ei ole käytettävissä olevaa työvaihesuhdetta eikä reititystä enää käytetä näissä vapautetuissa tuotteissa.

### <a name="maintaining-operation-relations-per-route"></a>Työvaihesuhteiden reitityskohtainen ylläpitäminen

Kun avaat **Reititystiedot**-sivun **Reititykset**-luettelosivulla, näkyviin tulee kaikkien valittuun reititykseen liittyvien työvaihesuhteiden luettelo. Näin voit helposti tarkistaa eri tuotteissa käytettävät operationaaliset ominaisuudet. Voit muokata sekä oletusominaisuuksien arvoja että tuotekohtaisten ominaisuuksien arvoja.  

Jos lisäät uuden työvaihesuhteen **Reititystiedot**-sivulla, **Reitityskoodi**-kentän arvoksi määritetään automaattisesti **Reititys** ja **Reitityssuhde**-kentän arvoksi nykyisen reitityksen reititysnumero.

### <a name="maintaining-operation-relations-per-operation"></a>Työvaihesuhteiden työvaihekohtainen ylläpitäminen

Voit avata **Työvaiheet**-sivulla **Työvaihesuhteet**-sivun. Tällä sivulla voit muokata tietyn työvaiheen kaikkia työvaihesuhteita. Voit muokata myös työvaihesuhteita, jotka sisältävät oletusarvoja.  

Jos yrityksesi käyttää vakiotyövaiheita ja toimintaparametrit ovat samat kaikilla tuotteilla ja kaikissa prosesseissa, **Työvaihesuhteet**-sivu on kätevä tapa ylläpitää näiden työvaiheiden toiminnallisia ominaisuuksia.

### <a name="applying-operation-relations"></a>Työvaihesuhteiden käyttäminen

Joissakin tapauksissa Supply Chain Managementin on löydettävä työvaiheen toiminnalliset ominaisuudet. Jos esimerkiksi luodaan ostotilaus, kunkin työvaiheen operationaaliset ominaisuudet on kopioitava työvaihesuhteista tuotantoreititykseen. Näissä tilanteissa Supply Chain Management hakee liittyviä työvaihesuhteita aina yksityiskohtaisimmista yhdistelmistä vähemmän yksityiskohtaisiin yhdistelmiin.  

Kun Supply Chain Management hakee vapautetulle tuotteelle soveltuvinta työvaihesuhdetta, työvaihesuhdetta, joka vastaa vapautetun tuotteen nimikkeen tunnusta, pidetään ensisijaisena verrattuna työsuhteeseen, joka vastaa nimikeryhmän tunnusta. Vastaavasti työvaihesuhdetta, joka vastaa nimikeryhmän tunnusta, pidetään ensisijaisena verrattuna oletustyövaihesuhteeseen. Haku tehdään seuraavassa järjestyksessä:

1.  **Nimikekoodi**=**taulukko** ja **nimikesuhde**=&lt;nimikkeen tunnus&gt;
2.  **Nimikekoodi**=**ryhmä** ja **nimikesuhde**=&lt;nimikeryhmän tunnus&gt;
3.  **Nimikekoodi**=**kaikki**
4.  **Reitityskoodi**=**reititys** ja **reitityssuhde**=&lt;reitityksen tunnus&gt;
5.  **Reitityskoodi**=**Kaikki**
6.  **Kokoonpano**=&lt;kokoonpanon tunnus&gt;
7.  **Kokoonpano**=
8.  **Toimipaikka**=&lt;toimipaikan tunnus&gt;
9.  **Toimipaikka**=

Tämän vuoksi työvaihetta tulisi käyttää vain kerran kussakin reitityksessä. Jos työvaihe esiintyy samassa reitityksessä useita kertoja, kaikilla työvaiheen esiintymillä on sama työvaihesuhde. Esiintymillä ei voi olla erilaisia ominaisuudet (esimerkiksi ajoaika).

## <a name="route-versions"></a>Reititysversiot

Reititysversioita käytetään tuotteiden tuotannossa esiintyvien vaihtelujen huomioonottamiseen tai tuotantoprosessin tarkempaan hallintaan. Ne määrittävät, mitä reititystä käytetään, kun tietty vapautettu tuote tai vapautettu tuotevariantti valmistetaan. Seuraavien rajoitusten avulla voit määrittää, mitä reitityksiä vapautetussa tuotteessa käytetään:

- Tuotedimensiot (koko, väri, tyyli tai kokoonpano)
- Tuotantomäärä
- Tuotantopaikka
- Tuotantopäivämäärä

Kun tuotetta valmistetaan tietyssä toimipaikassa, tietty määrä tai tiettynä ajankohtana, voit määrittää oletusreititysversioksi tietyn reititysversion. Huomaa kuitenkin, että annetulle vapautetulle tuotteelle ja annettujen rajoitusten joukolle sallitaan vain yksi aktiivinen reititys.  

Tuotannonohjauksen parametrien avulla voi määrittää, että reititysversion voimassaoloaika on aina määritettävä.

### <a name="approval-of-route-versions"></a>Reititysversioiden hyväksyminen

Reititysversio on hyväksyttävä, ennen kuin sitä voidaan käyttää suunnittelu- ja tuotantoprosessissa. Voit hyväksyä reititysversion yhteydessä myös liittyvän reitityksen. Huomaa kuitenkin, että reititysversio voidaan hyväksyä vain, jos myös liittyvä versio on hyväksytty.

### <a name="activating-the-default-route-version"></a>Oletusreititysversion aktivoiminen

Voit määrittää reititysversion aktivoinnin yhteydessä oletusreititysversioksi, jota pääsuunnittelu käyttää tai jota käytetään tuotantotilausten luomisessa. Annetulla rajoitusten (esimerkiksi kausi, toimipaikka tai määrä) joukolla voi olla vain yksi aktiivinen reititysversio. Jos yrität aktivoida version, joka on ristiriidassa aktiivisen version kanssa, näyttöön ilmestyy virhesanoma. Voit estää epäselvän aktivoinnin poistamalla ensin ristiriitainen versio tai muokkaamalla version rajoituksia (yleensä kausi).

### <a name="electronic-signatures"></a>Sähköiset allekirjoitukset

Jos ylläpidät lokia, johon tallennetaan kunkin reititysversion hyväksyjä ja aktivoija, voit vaatia näistä tehtävistä sähköiset allekirjoitukset. Käyttäjien, jotka hyväksyvät ja aktivoivat reititysversioita, on vahvistettava henkilöllisyys [sähköisen allekirjoituksen](../../fin-and-ops/organization-administration/electronic-signature-overview.md) avulla.

### <a name="product-change-that-uses-case-management"></a>Tuotemuutos, joka käyttää tapaustenhallintaa

Uusien tai muuttuneiden reititysten ja reititysversioiden hyväksymisen ja aktivoimisen tuotemallitapaus tarjoaa helpon tavan nähdä reititysversion rajoitukset kokonaisuudessaan. Voit hyväksyä ja aktivoida myös kaikki reititykset, jotka liittyvät tiettyyn yhden työvaiheen muutokseen. Tämän jälkeen voit tallentaa tulokset tuotemuutostapaukseen.

## <a name="maintaining-routes"></a>Reititysten ylläpitäminen

Liiketoimintatarpeiden perusteella voit mahdollisesti vähentää työtä, joka vaaditaan prosessimääritysten ylläpitämiseen.

### <a name="making-routes-independent-of-resources"></a>Reittien määrittäminen resursseista riippumattomiksi

Useissa järjestelmissä operatiivinen resurssi tai resurssiryhmä, joka suorittaa työvaiheen, on määritettävä reitityksessä. Supply Chain Managementissa voit kuitenkin määrittää joukon vaatimuksia, jotka operatiivisen resurssin on täytettävä, jotta sitä voidaan käyttää työvaiheessa. Tämän vuoksi tiettyä operatiivista resurssia tai resurssiryhmää, jota tullaan käyttämään, ei tarvitse määrittää ennen työvaiheen ajoittamista. Tämä toiminto on erityisen hyödyllinen silloin, kun useat työntekijät tai koneet voivat suorittaa saman työvaiheen.  

Voit määrittää esimerkiksi, että työvaihe vaatii operatiivisen resurssin, jonka tyyppi on **Kone** ja jonka **leimauskapasiteetti** on 20 tonnia. Ajoitusmoduuli ratkaisee nämä vaatimukset tietyn operatiivisen resurssin tai resurssiryhmän osalta, kun työvaihe ajoitetaan. Joustavuus paranee, koska voit määrittää nämä vaatimukset sen sijaan, että työvaihe olisi sidottava tiettyyn koneeseen. Lisäksi ylläpito on helpompaa, kun resursseja siirretään tai uusia resursseja lisätään.  

Lisätietoja resurssivaatimusten eri tyypeistä ja niiden käyttämisestä on kohdissa Operatiivisten resurssien vaatimukset ja [Resurssin ominaisuudet](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Reititysten jakaminen toimipaikkojen kesken

Jos valmistat samaa tuotetta useassa tuotantopaikassa ja tuotteen valmistusvaiheet ovat samat kaikissa toimipaikoissa, voit usein suunnitella jaetun reitityksen, jota käytetään kaikissa tuotantopaikoissa. Kun luot jaetun reitityksen, älä määritä toimipaikkaa reititykseen. Jaetun reitityksen ja tuotteen toisiinsa liittävä reititysversio on silti luotava jokaisessa toimipaikassa.  

On myös varmistettava, että reitityksen minkään työvaiheen resurssivaatimukset eivät kutsu tiettyjä operatiivisia resursseja tai resurssiryhmiä. Tämän sijaan on käytettävä vaadittujen resurssien ominaisuuksia. Ajoitusmoduuli pystyy tämän jälkeen liittämään sen toimipaikan soveltuvat operatiiviset resurssit, jonne tuotanto on ajoitettu. Jos esimerkiksi ajoajoissa on pieniä eroja tai tietyn työvaiheen asetusaika on toimipaikkakohtainen, voit määrittää tiedot lisäämällä toimipaikalle uuden työvaihesuhteen.  

Saat kaikki jaettujen reititysten edut käyttöön, kun otat käyttöön myös vastaavien tuoterakenteiden resurssien kulutuksen. Kun resurssien kulutuksen merkinnän tuoterakenneriville, varasto ja sijainti, josta raaka-aineet kulutetaan, johdetaan operatiivisesta resurssista, jolle työvaihe on ajoitettu. Tämän vuoksi varastoa ja sijaintia ei tarvitse määrittää ennen tuotannon todellista ajoittamista. Näin voit tehdä sekä tuoterakenteesta että reitityksestä tuotteen valmistuspaikan fyysisestä sijainnista riippumattoman.

### <a name="standard-operation-relations"></a>Vakiotyövaihesuhteet

Jos yrityksessä käytetään koko tuotannossa vakiotyövaiheita ja jos asetusajoissa, ajoajassa, kulutuksen laskennassa, kustannusten laskennassa jne. on vain vähän tai ei lainkaan eroja, kannattaa ehkä kaikille työvaiheille luoda oletustyövaihesuhteet. Vältä tällöin niiden työvaihesuhteiden luomista, jotka ovat liittyvät tiettyyn reititykseen tai vapautettuun tuotteeseen.  

Jos ilmaiset resurssivaatimukset osaamisalueina ja suorituskykynä ja teet reitityksistä toimipaikoista riippumattomia, liiketoimintaprosessien jatkuvan ylläpidon tarve vähenee.  

Tällöin **Työvaihesuhteet**-sivusta tulee ensisijainen kohde, kun ylläpidät ajoaika ja muita ominaisuuksia.

### <a name="resource-specific-process-times"></a>Resurssikohtaiset prosessiajat

Jos et määritä operatiivista resurssia tai resurssiryhmää osaksi työvaiheen resurssivaatimuksia, käytettävissä olevat resurssit saattavat toimia eri nopeuksilla. Tämän vuoksi työvaiheen käsittelyyn kuluva aika saattaa vaihdella. Voit ratkaista tämän ongelman määrittämällä työvaihesuhteen **Kaava**-kenttään prosessiajan laskentatavan. Valittavissa ovat seuraavat vaihtoehdot:

- **Vakio** – (oletusvalinta) Laskelmassa käytetään vain työvaihesuhteen kenttiä. Määritetty ajoaika kerrotaan tilausmäärällä.
- **Kapasiteetti** – Laskenta sisältää operatiivisen resurssin **Kapasiteetti**-kentän. Aika siis riippuu resurssista. Operatiiviselle resurssille määritetty arvo on kapasiteetti tuntia kohti. **Käsittelyaika** lasketaan **kapasiteetilla** jaetulla **tilausmäärällä**.
- **Erä** – Erän kapasiteetti lasketaan työvaihesuhteen tietojen avulla. Erien määrä ja prosessiaika voidaan laskea tilausmäärän perusteella.
- **Resurssierä** – Tämä vaihtoehto on periaatteessa sama kuin **Erä**-vaihtoehto. Laskenta sisältää kuitenkin operatiivisen resurssin **Eräkapasiteetti**-kentän. Aika siis riippuu resurssista.

### <a name="set-up-route-groups"></a>Määritä reititysryhmät

Voit määrittää reittiryhmät ja sen reitin tai työtyyppien asetukset kohdasta **Tuotannonvalvonta > Asetukset > Reititykset > reitityksen ryhmät**. Voit valita tai tyhjentää seuraavat reititysryhmän reitti-/työtyypin kohdat:

- **Aktivointi** - Valitse tämä vaihtoehto, jos haluat ottaa työn ajoituksen yhteydessä käyttöön valitun työtyypin laskelmat ja ajoituksen sekä vastaanottaa palautetta työstä. Sinun on valittava tämä vaihtoehto, jos haluat ottaa työtyypin käyttöön, ja valitse sitten kyseisen työtyypin muut vaihtoehdot. Jos aktivointia ei ole valittu, kyseistä työtyyppiä ei oteta käyttöön muiden vaihtoehtojen valinnasta riippumatta. 
- **Töiden hallinta** - Valitse tämä vaihtoehto, jos haluat sisällyttää työtyypin töiden hallintaan työtä ajoitettaessa. 
- **Työaika** Valitse tämä vaihtoehto, jos haluat ajoittaa työtyypin operatiiviselle resurssille määritetyn työaikakalenterin mukaan. Muussa tapauksessa käytetään gregoriaanista kalenteria. Työaika voidaan ajoittaa gregoriaanisen kalenterin tai määritetyn työkalenterin mukaan. Jos valitset tämän vaihtoehdon, ajoitus perustuu määritettyyn työaikakalenteriin. Lisäksi työtyypin työ on ajoitettu sen päivämäärän keskiyöstä, joka on määritetty työn aloituspäiväksi.
- **Kapasiteetti** - Valitse tämä vaihtoehto, jos haluat varata työtyypille kapasiteettia työtä ajoitettaessa. Jos valitset tämän vaihtoehdon, kapasiteetti varataan, kun valittu työtyyppi ajoitetaan. Saat tällä tavoin yhteenvedon siitä, mitkä kunkin reititysryhmän työtyypit käyttävät operatiivisia resursseja. Esimerkiksi tilanteessa, jossa kuivausresurssit, ovat pullonkaularesursseja, kyseiset resurssit on määritettävä pullonkauloiksi. Jonotusajan työtyyppeihin määritetyt kuivauksen työvaiheet varaavat kuivausresurssit. 

Jokaista työtyyppiä varten sinun on ensin aktivoitava se tai poistettava se käytöstä. Kun toiminto on poistettu käytöstä, mitään muuta asetusta (työnhallinta, työaika ja kapasiteetti) ei oteta huomioon, koska työn tyyppi ei ole aktiivinen. 

Voit etsiä limityksiä työtyyppien väliltä. Limitysten avulla voit suorittaa eri töitä yhtä aikaa. Kun työt ovat päällekkäisiä, resursseja voidaan käyttää, mutta niitä ei voi varata tiettyihin töihin.
Tästä syystä kun limityksen aktivointi on valittuna, muut asetukset (töiden hallinta, työaika ja kapasiteetti) eivät vaikuta reititysryhmään. 

> [!NOTE]
> Päivitettäessä versioita seuraava virhe saattaa esiintyä: **Kumottujen varmenteiden luettelovirhe ajoitusohjelmaa käytettäessä”**. Jos saat tämän virhesanoman, mene **Reitityksen ryhmät** -sivulle ja kaikissa reitityksissä, mistä olet aktivoinut valinnan **limitys**-vaihtoehdon, poista **töiden hallinta**, **työaika**- ja **kapasiteetti**-valinnat. 

## <a name="additional-resources"></a>Lisäresurssit

- [Tuoterakenteet ja kaavat](bill-of-material-bom.md)

- [Tuotannon reitityksessä käytetyt kustannusluokat](../cost-management/cost-categories-used-production-routings.md)

- [Resurssin ominaisuudet](resource-capabilities.md)

- [Sähköisten allekirjoitusten yleiskatsaus](../../fin-and-ops/organization-administration/electronic-signature-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]