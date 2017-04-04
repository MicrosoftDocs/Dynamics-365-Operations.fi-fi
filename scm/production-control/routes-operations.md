---
title: "Reittien ja työvaiheiden"
description: "Tässä aiheessa on tietoja reittejä ja toimintoja. Reitti määritetään tuottavat Tuotevariantin tuotteen tai prosessin. Siinä kuvataan tuotantoprosessin ja siihen järjestykseen, jossa nämä vaiheet on suoritettava jokaisen työvaiheen (työvaihe). Reitti määritetään myös tarvittavat toiminnot resurssien vaadittu Asetusaika- ja Ajoaika, ja miten kustannukset on laskettava kunkin vaiheen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 556b9859d0b162b11f0bcbfc6552f6fd9a900596
ms.lasthandoff: 03/31/2017


---

# <a name="routes-and-operations"></a>Reittien ja työvaiheiden

Tässä aiheessa on tietoja reittejä ja toimintoja. Reitti määritetään tuottavat Tuotevariantin tuotteen tai prosessin. Siinä kuvataan tuotantoprosessin ja siihen järjestykseen, jossa nämä vaiheet on suoritettava jokaisen työvaiheen (työvaihe). Reitti määritetään myös tarvittavat toiminnot resurssien vaadittu Asetusaika- ja Ajoaika, ja miten kustannukset on laskettava kunkin vaiheen.

<a name="overview"></a>Yleiskuvaus
--------

Reitti kuvaa, joka vaaditaan, jotta voidaan tuottaa tuotteen tai Tuotevariantin toimintojen järjestyksen. Kunkin operaation osalta reitin määrittää toimintojen resursseihin, joita tarvitaan, aika, joka vaaditaan, jotta voidaan määrittää ja suorittaa toiminnon ja miten kustannukset lasketaan. Voit käyttää samaa reititystä tuottamaan useita tuotteita tai voit määrittää yksilöllisen reitin jokaiselle tuotteelle tai tuotteen variantti. Voi jopa olla useita reittejä samaan tuotteeseen. Tässä tapauksessa, jota käytetään reitin vaihtelee sen mukaan, sellaiset tekijät kuin se määrä, joka on tuotettu. Reitityksen työvaiheiden Microsoft Dynamics-365-määritelmä sisältää neljä eri elementtejä, jotka kuvaavat yhdessä tuotantoprosessin:

-   **Reitin** – määrittää reitin tuotantoprosessin rakenne. Toisin sanoen määrittää työvaiheiden järjestyksen.
-   **Toiminto** – toiminto tunnistaa reitin, nimetty vaiheessa **kokoonpanon**. Sama toiminto saattaa ilmetä useita reittejä ja voi olla eri numeroita.
-   **Työvaihesuhde** – työvaihesuhteen määrittää toiminnon, kuten Asetusaika ja Ajoaika, kustannusluokat, kulutus parametrit ja resurssivaatimukset toiminnalliset ominaisuudet. Työvaihesuhde ottaa operaation vaihtelevat sen mukaan, jota käytetään työvaiheen reitityksen tai tuotteet, jotka on tuotettu toiminnallisia ominaisuuksia.
-   **Reititysversion** – määrittää reititysversion reitin, jota käytetään tuottamaan tuotteen tai tuotteen variantin. Reititysversion käyttöön reittien tuotteet uudelleen tai muuttaa ajan myötä. Ne mahdollistavat myös eri reittejä voidaan käyttää samaa tuotetta. Tässä tapauksessa, jota käytetään reitin vaikuttavat tekijät kuten sijainti tai määrä, joka on tuotettu.

## <a name="routes"></a>Reititykset
Reitti kuvaa, jota käytetään tuottamaan tuotteen tai Tuotevariantin toimintojen järjestyksen. Jokaiselle operaatiolle määritetään työvaihenumero ja seuraaja-toimintoa. Toimintojen suoritusjärjestys muodostavat Reittiverkosto, joka voi edustaa ohjattua kaavion, jossa on vähintään yksi ensimmäinen pistettä ja yhden loppupisteen. Dynamics 365 operaatioille reitit on erottaa rakenne tyypin perusteella. Yksinkertainen reitit ja reitti on reittien kahdenlaisia verkoissa. Tuotannonohjauksen parametrit voit määrittää voidaanko käyttää yksinkertaisia reittejä tai onko voidaan käyttää monimutkaisempia reittiverkostoista.

### <a name="simple-routes"></a>Yksinkertainen reitit

Yksinkertainen reitti on järjestyksessä ja vain yksi reitin aloituspiste on.  

[![Yksinkertainen reitti](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Jos otat käyttöön vain yksinkertainen reittien tuotannonohjauksen parametrit, työvaiheiden 365 Dynamics luo automaattisesti numerot (10, 20, 30 ja niin edelleen) kun haluat määrittää reitin.

### <a name="route-networks"></a>Reittiverkostoista

Jos otat käyttöön monimutkaisempia reittiverkostoista-tuotannonohjauksen parametrit, voit määrittää reittejä, joissa on useita pisteitä ja toiminnot, jotka voidaan suorittaa samanaikaisesti.  

[![Route network](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Huomautuksia:**

-   Jokaisella toiminnolla voi olla vain yksi seuraaja toiminta ja koko reitti pitää loppua yhdellä kertaa.
-   On useita toimintoja, joilla on sama seuraaja toiminto (esimerkiksi toimintojen 30 ja 40 edellisessä kuvassa) todellisuudessa toteutua rinnakkain ei voida taata. Käytettävyys ja kapasiteetti, resurssien asettaa rajoituksia siitä, miten työvaiheet ajoitetaan.
-   Työvaihenumero 0 (nolla) ei voi käyttää. Numero on varattu, ja määritetään, että reitityksen viimeinen työvaihe on seuraaja ei toimintaa.

### <a name="parallel-operations"></a>Samanaikaisia työvaiheita

Joskus useiden toimintojen resursseihin, joilla on erilaiset ominaisuudet yhdistelmä tarvitaan toiminnon suorittamiseksi. Kokoonpanon operaation saattaa vaatia esimerkiksi koneen ja työkalun yksin valvoa toimintaa aina kahta konetta, yksi työntekijä. Tämä esimerkki voi mallintaa avulla samanaikaisia työvaiheita, joissa yksi toiminto on määritetty ensisijaisen työvaiheen ja muut ovat toissijaisia.  

[![Reitti, jossa on ensisijaisia ja toissijaisia työvaiheita](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Yleensä ensisijaisen työvaiheen edustaa pullonkaula resurssien ja määrittää suorituksen aikana toissijaisissa työvaiheissa. Kuitenkin ajoituksessa rajallista kapasiteettia, joka liittyy, resurssit, jotka ajoitetaan ensisijaisen työvaiheen sekä toissijaisille työvaiheille on oltava käytettävissä ja vapaata kapasiteettia on samaan aikaan.  

Ensisijaisen työvaiheen sekä toissijaisille työvaiheille on oltava sama työvaihenumero (edellisessä kuvassa 30).  

Edellisessä esimerkissä resurssitarve ensisijaiselle työvaiheelle (30) on kone, toissijaiset työvaiheet (30' ja 30'') resurssivaatimuksia on työkalu ja se työntekijä. Viisikymmentä prosentin kuormituksen auttaa takaamaan, että suunniteltu työntekijä yksin voi valvoa kahta konetta samaan aikaan.

### <a name="approval-of-routes"></a>Reititysten hyväksyntä

Reitti on hyväksyttävä ennen kuin sitä voidaan käyttää suunnitteluun tai tuotannon aikana. Hyväksynnän osoittaa reitin suunnittelu on suoritettu. Sama tuote luovutetaan tai tuotevariantti on vapautettu voi olla hyväksytty useita reittejä. Reitityksen hyväksyminen ilmenee yleensä, kun ensimmäinen asiaa reititysversio on hyväksytty. Jotkin Business skenaariot, reitti ja reititysversio hyväksyminen ovat kuitenkin erillistä toimintaa, joka saattaa liittyä eri prosessien omistajat.  

Kunkin reitin voi olla hyväksytty tai hyväksymätön erikseen. Huomaa kuitenkin, että kun reitti on hyväksymätön, liittyvät reititysversiot ovat myös hyväksymättömiä. Tuotannonohjauksen parametrit voit määrittää onko reitit voi olla hyväksymätön ja onko hyväksyttyjä reitityksiä voi muuttaa.  

Jos pitää kirjaa, joka hyväksyy kunkin reitin tietueita, voit edellyttää sähköisiä allekirjoituksia reitin hyväksyttäväksi. Käyttäjien on henkilöllisyytensä avulla [sähköisen allekirjoituksen](/dynamics365/operations/organization-administration/electronic-signature-overview).

## <a name="operations"></a>Työvaiheet
Toiminto on tuotantoprosessin vaiheessa. Dynamics 365 toimintoihin kunkin toiminnon on tunnus ja yksinkertainen kuvaus. Seuraavissa taulukoissa on tyypillisiä esimerkkejä machine shop-toimintoja.

| Työvaihe  | kuvaus        |
|------------|--------------------|
| PipeCut    | Putkien leikkaamiseen       |
| TIGweld    | Hitsaamalla TIG        |
| JigAssy    | Kiinnittimen kokoonpano       |
| Tarkastus | Laadun tarkastus |

Työvaiheen asetusaika ja Ajoaika, resurssivaatimukset, kustannustiedoista ja kulutuksen laskenta toiminnalliset ominaisuudet määritetään työvaihesuhteen. (Lisätietoja työvaiheiden suhteet, katso seuraava osa.)

## <a name="operation-relations"></a>Työvaihesuhteet
Ylläpidetään Työvaihesuhde operaation operatiivisten seuraavat ominaisuudet:

-   Kustannusluokat
-   Kulutuksen parametrit
-   Käsittelyajat
-   Määrät käsitellään
-   Resurssivaatimukset
-   Huomautukset ja ohjeet

Voit määrittää useita saman työvaiheen työvaihesuhteet. Kuitenkin jokainen työvaihesuhteen liittyy vain yksi toiminto ja sisältää ominaisuuksia, jotka koskevat reitti, vapautetun tuotteen tai joukko vapautetut tuotteet, jotka liittyvät nimikeryhmä. Tämän vuoksi sama toiminto voidaan useita reittejä, joilla on erilaisia toiminnallisia ominaisuuksia. Lisäksi voit helposti ylläpitää päätiedot Jos käytät vakio-operaatiot, joita on samat toiminnalliset ominaisuudet, jota käytetään reititys- ja tuote, joka valmistetaan riippumatta. Työvaihesuhde laajuus määritellään kautta **Nimikekoodi**, **Nimikkeen suhde**, **lähettää koodin** ja **kierrättää suhde** ominaisuudet seuraavassa taulukossa esitetyllä tavalla.

| Nimikekoodi | Nimikkeen suhde         | Reitityskoodi | Reitityssuhde   | Työvaihesuhde soveltamisala                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Taulu     | &lt;Nimikkeen tunnus&gt;       | Reititys      | &lt;Reittitunnus&gt; | Käytettäessä reitityksen työvaiheen toiminnalliset ominaisuudet jossa **Tienumero**=&lt;reitin&gt; vapautetun tuotteen jossa **Tavaraerän numero**=&lt;kohteen tunnus&gt;.                                                                                                                        |
| Taulu     | &lt;Nimikkeen tunnus&gt;       | Kaikki        |                  | Toimintoa käytettäessä vapautetun tuotteen toiminnallisia ominaisuuksia jossa **Tavaraerän numero**=&lt;kohteen tunnus&gt;. Nämä toiminnalliset ominaisuudet koskevat toisin sanoen, kun ei ole reittiä koskevia työvaihesuhteen vapautetun tuotteen.                                     |
| Ryhmä     | &lt;Nimikeryhmän tunnus&gt; | Reititys      | &lt;Reittitunnus&gt; | Käytettäessä reitityksen työvaiheen toiminnalliset ominaisuudet jossa **Tienumero**=&lt;reitin&gt; tuottamaan vapautetut tuotteet, jotka on liitetty nimikeryhmän &lt;tuotteen tai Ryhmätunnus&gt;, ellei ole erityinen reitin työvaihesuhteen vapautetun tuotteen.                         |
| Ryhmä     | &lt;Nimikeryhmän tunnus&gt; | Kaikki        |                  | Toiminnon, kun sitä käytetään tuottamaan vapautetut tuotteet, jotka on liitetty nimikeryhmän toiminnallisia ominaisuuksia &lt;tuotteen tai Ryhmätunnus&gt;, ellei ole olemassa erityisiä työvaihesuhteen.                                                                                                  |
| Kaikki       |                       | Reititys      | &lt;Reittitunnus&gt; | Käytettäessä reitityksen työvaiheen toiminnallisia ominaisuuksia jossa **reitityksen numero**=&lt;reitin&gt;. Toisin sanoen nämä toiminnalliset ominaisuudet koskevat on ei työvaihesuhteen tämän reitin, joka liittyy joko julkaistu tuote, tai se on liitetty nimikeryhmän. |
| Kaikki       |                       | Kaikki        |                  | Toiminnon toiminnallisia ominaisuuksia. Näitä toiminnallisia ominaisuuksia käytetään, kun ei ole tarkempia työvaihesuhteen.                                                                                                                                                                |

Voit myös määrittää, että työvaihesuhteen liittyy sivuston. Tällä tavalla operaation toiminnallisia ominaisuuksia voi vaihdella, jossa toiminto suoritetaan sijainti (eli sivusto). Konfiguroituja tuotteita voit myös määrittää erilaisia toiminnallisia ominaisuuksia kunkin tuotteen kokoonpanon.  

Työvaihesuhteet antaa sinulle joustava määrittäessäsi yhteyttä reittejä. Lisäksi voidaan määrittää oletusasetuksia auttaa vähentämään perustiedot, jotka on säilytettävä. Kuitenkin Tämä joustavuus tarkoittaa myös sitä, että sinun on oltava tietoinen haluat muokata työvaihesuhteen-yhteydessä.  

**Huomautus:** koska kohden reitityksen työvaiheen työvaihesuhteet toiminnalliset ominaisuudet on tallennettu, kaikki esiintymät samassa työvaiheessa (esimerkiksi kokoonpano) on sama Asetusaika, Ajoaika, resurssivaatimukset ja niin edelleen. Siksi operaation kaksi esiintymää on ilmetä samalla, mutta on eri ajoajat, jos sinun on luotava kaksi erillistä toimintoja, kuten Assembly1 ja Assembly2.

### <a name="modifying-product-specific-routes"></a>Tuotekohtaiset reittien muokkaaminen

Kun avaat **reitin** sivun **julkaissut tuotteen tiedot** sivun reititysversiot, jotka on liitetty valittuun vapautetun tuotteen näytetään. Tältä osin kunkin operaation osalta Dynamics 365 toiminnoissa näkyy työvaihesuhteen-toiminnalliset ominaisuudet, joka parhaiten vastaa reititysversion. Huomaat, että työvaiheiden luettelo sisältää **Nimikekoodi** ja **lähettää koodin** työvaihesuhteen-ominaisuudet. Tämän vuoksi voit määrittää, mitkä työvaihesuhteen näkyy.  

- **Reitin** -sivulla voit muokata toiminnalliset ominaisuudet toiminnon suorituksen aikana kustannusluokat. Tekemäsi muutokset on tallennettu työvaihe suhteessa, joka vastaa reitityksen ja vapautetun tuotteen, joihin viitataan nykyinen reititysversio. Jos työvaihe suhteessa, joka esitetään ei ole tietyn reitin ja vapautetun tuotteen, ennen kuin muutokset on tallennettu, järjestelmä luo siitä kopion työvaihesuhteen. Tämä *on* reitin ja vapautetun tuotteen. Siksi muutokset eivät vaikuta muiden reittien tai vapautetut tuotteet. Voit tarkistaa, mitkä työvaihesuhteen muokataan useassa **reitin** -sivulla Katso **Nimikekoodi** ja **kierrättää koodi** kentät.  

Voit luoda myös manuaalisesti työvaihe, joka on tietyn reitin ja vapautetun tuotteen **kopioi suhde ja muokkaa** funktio.  

**Huomautus:** Jos voit lisätä uuden työvaiheen reititykseen **reitin** -sivun työvaihesuhteen luodaan vain nykyisen julkaistun tuotteen. Siksi reittiä käytetään myös muiden vapautettujen tuotteiden tuottamiseen, jos ei ole sovellettavissa työvaihesuhteen on olemassa näiden vapautettujen tuotteiden ja reitti ei enää voi käyttää vapautetut tuotteet.

### <a name="maintaining-operation-relations-per-route"></a>Reitityksen työvaiheiden suhteet ylläpito

Kun avaat **reitittää tiedot** sivun **reitit** sivun kaikkien työvaiheiden suhteet, jotka koskevat valitun reitityksen luettelo näkyy. Siksi voit helposti tarkistaa mitä tuotteita käytetään toiminnalliset ominaisuudet. Voit muokata sekä ominaisuuksien oletusarvot ja tuotekohtaisia ominaisuusarvoja.  

Jos lisäät uuden työvaihesuhteen **reitittää tiedot** -sivulla **kierrättää koodi** kentän arvoksi määritetään automaattisesti **reitin**, ja **kierrättää suhde** kentän arvoksi nykyisen reitityksen reititysnumero.

### <a name="maintaining-operation-relations-per-operation"></a>Ylläpito työvaihetta kohti työvaihesuhteet

- **Toimintojen** sivulla, voit avata **työvaiheiden suhteet** sivun. Tällä sivulla voit muokata kaikkien työvaiheiden suhteet tiettyyn toimintoon. Vaikka voit muokata, joissa on oletusarvot työvaiheiden suhteet.  

Jos yrityksesi käyttää standardin toimintoja ja toiminnalliset parametrit ovat samat kaikkien tuotteiden ja prosessien kautta **työvaiheiden suhteet** sivu on kätevä tapa säilyttää toimintoihin toiminnallisia ominaisuuksia.

### <a name="applying-operation-relations"></a>Käytetään työvaiheiden suhteet

Joissakin tapauksissa Dynamics 365 toimintoja varten on löydettävä operaation toiminnallisia ominaisuuksia. Esimerkiksi, kun ostotilaus luodaan, jokaista toiminnallisia ominaisuuksia on kopioidaan operation relations tuotantoreitityksen. Näissä tilanteissa toiminnoissa 365 Dynamics etsii halutun toiminnon-suhteet tarkimman-yhdistelmän määritetty yhdistelmä.  

Kun toimintoja hakujen kannalta työvaihesuhteen vapautetun tuotteen, joka vastaa nimikkeen tunnus vapautetun tuotteen työvaihesuhteen Dynamics 365 on ensisijainen työvaihesuhteen päälle, että osumia nimikeryhmän tunnus. Puolestaan työvaihesuhteen, joka vastaa nimikeryhmän tunnus on ensisijainen oletusarvon työvaihesuhteen. Haku tehdään seuraavassa järjestyksessä:

1.  **Nimikkeen koodi**=**taulukko** ja **Nimikkeen suhde**=&lt;kohteen tunnus&gt;
2.  **Nimikkeen koodi**=**ryhmään** ja **Nimikkeen suhde**=&lt;nimikkeen tunnus&gt;
3.  **Nimikkeen koodi**=**kaikki**
4.  **Route koodi**=**reitin** ja **kierrättää suhde**=&lt;reitin&gt;
5.  **Route koodi**=**kaikki**
6.  **Kokoonpanon**=&lt;Konfiguraatiotunnus&gt;
7.  **Configuration**=
8.  **Sivuston**=&lt;-sivuston tunnus&gt;
9.  **Site**=

Siksi toimintoa tulisi käyttää vain kerran kunkin reitityksen. Jos toiminto tapahtuu samaa reittiä useasti, kaikki esiintymät, että toiminto on sama työvaihesuhteen ja et voi olla eri ominaisuudet (esimerkiksi ajoaikojen) jokaista.

## <a name="route-versions"></a>Reititysversiot
Reititysversioita käytetään tuotteiden tuotannon vaihtelujen tai tuotantoprosessin tarkemmin. Ne määrittävät, mitä reititysversioita käytetään, kun yksittäinen vapautettu tuote tai tuotetaan tuotevariantti on vapautettu. Voit määrittää, mitä reititysversioita käytetään vapautetun tuotteen seuraavat rajoitukset:

-   Tuotteen mitat (koon, värin, tyylin tai kokoonpano)
-   Tuotannon määrä
-   Tuotantosivuston
-   Tuotanto päivämäärä

Kun olet tuottavat tietyn sivuston tietyn määrän tuotteen tai tietyltä ajanjaksolta, voit määrittää oletusarvon reititysversion tiettyä reititysversiota. Huomaa kuitenkin, että vain yhtä aktiivista reittiä voidaan käyttää tietyn vapautetun tuotteen ja määritettyjen rajoitusten.  

Tuotannonohjauksen parametrit voit vaatia voimassaoloaikaa reititysversio aina määritettävä.

### <a name="approval-of-route-versions"></a>Reititysversioiden hyväksyminen

Ennen reititysversion voidaan käyttää suunnitteluun ja valmistusprosessi, se on hyväksyttävä. Kun hyväksyt reititysversion, voit hyväksyä liittyvät reitin. Huomaa kuitenkin, että reititysversio hyväksytään vain, jos Aiheeseen liittyviä reitti on myös hyväksytty.

### <a name="activating-the-default-route-version"></a>Oletus reititysversion aktivoiminen

Kun reititysversion aktivoiminen, voit nimetä sen, tai käyttää reitin oletusversio, jota Pääsuunnittelu suunnittelu, joita käytetään luotaessa tuotantotilauksia. Voit valita vain yhden aktiivisen reititysversion määritettyjen rajoitusten (piste, sivuston tai määrä). Jos yrität aktivoida versio on ristiriidassa version, joka on jo käytössä, näyttöön tulee virhesanoma. Jotta epäselvä aktivointi, sinun on sitten ristiriidassa versio käytöstä tai muokata reititysversio rajoituksia (yleensä piste).

### <a name="electronic-signatures"></a>Sähköiset allekirjoitukset

Jos pitää kirjaa, joka hyväksyy ja Aktivoi reititysversio kunkin tietueita, voit edellyttää sähköisiä allekirjoituksia näille tehtäville. Käyttäjät, joilla on hyväksyä ja aktivoida reititysversiot on henkilöllisyytensä avulla [sähköisen allekirjoituksen](/dynamics365/operations/organization-administration/electronic-signature-overview).

### <a name="product-change-that-uses-case-management"></a>Tuotteen muutoksen, joka käyttää palvelupyyntöjen hallinta

Tuotteen Muuta kirjainkoko hyväksymistä ja uudet tai muutetut reitit ja reititysversiot aktivointi antaa helppo on yleiskuvaus reitityksen versio rajoituksia. Voit myös hyväksyä ja aktivoida kaikki reitit, jotka liittyvät tietyn muutoksen yhdellä kertaa ja tulokset tapauksessa tuotteen Muuta asiakirjan.

## <a name="maintaining-routes"></a>Reiteillä ylläpidosta
Business-tarpeidesi mukaan voit ehkä vähentää vaivaa, joita tarvitaan prosessin määritelmiä säilyttämiseksi.

### <a name="making-routes-independent-of-resources"></a>Reittien tekemisen resursseista erillään

Monissa järjestelmissä toimintojen resurssi tai resurssiryhmä tulee suorittaa toiminnon, joka on määritettävä reitin. Kuitenkin Dynamics 365 toimintoja varten, voit määrittää joukon vaatimuksia, jotka operations-resurssin on täytettävä sovellettavat toiminnan. Tämän vuoksi erityistoimia resurssi tai resurssiryhmä, jota käytetään ei tarvitse määritetään kunnes työvaihe ajoitetaan. Tämä toiminto on erityisen hyödyllinen, kun sinulla on useita työntekijöitä tai koneita, jotka voi suorittaa saman toiminnon.  

Esimerkiksi, voit määrittää, että toiminto vaatii toimintoja resurssin **koneen** tyyppi, joka on **Stamping** 20 tonnia ominaisuutta. Aikataulutusmoduuli sitten ratkaisee nämä vaatimukset tiettyihin toimintoihin resurssi tai resurssiryhmä, kun työvaihe ajoitetaan. Voit määrittää juuri näitä vaatimuksia, eikä sitoa tiettyä konetta toimintoa, koska on joustavaa. Lisäksi ylläpito on helpompaa, kun resursseja siirretään tai uusia resursseja on lisätty.  

Saat lisätietoja erityyppisten resurssivaatimukset ja kuinka niitä käytetään työvaiheiden resurssivaatimukset ja [resurssin ominaisuudet](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Toimipaikkojen jakaminen reitit

Jos samaa tuotetta useita tuotannon luona tuottavat ja tuottavat tuotteen vaiheet ovat samat kaikilla sivustot, voit suunnitella usein jaettu reitin, jota käytetään kaikissa tuotantolaitoksissa. Voit luoda jaetun reitin, älä määritä sivuston itse reitillä. On kuitenkin vielä luotava reititysversio, joka yhdistää jaetun reitin läpi kaikki tuotteen.  

Sinun täytyy myös varmistaa kunkin reitityksen työvaiheen resurssivaatimuksia ei Soita erityistoimia resurssien tai resurssiryhmien, mutta ovat sen sijaan ilmaistaan tarvittavia resursseja ominaispiirteet. Aikataulutusmoduuli voi määrittää tarvittavat toimintojen resursseihin, tuotanto ajoitetaan-sivustosta. Esimerkiksi jos suorituksen aikana pieniä eroja tai jos tietyn työvaiheen asetusaika on toimipaikkakohtainen, voit määrittää nämä tiedot lisäämällä ylimääräisiä työvaihesuhteen sivuston.  

Saadaksesi täyden hyödyn eduista jaetun reittejä, kannattaa myös käyttää resurssikulutuksen vastaavan tuoterakenne (BOM). Kun määrität Tuoterakenteen rivin resurssin kulutuksen lippu, varasto ja sijainti, josta tulisi kuluttaa raaka-aineita käytetään monikkoa, työvaihe ajoitetaan-toimintoja resurssien. Vuoksi varastoa ja sijaintia ei tarvitse määrittää vasta, kun tuotanto ajoitetaan. Tällä tavalla voit tehdä sekä Tuoterakenteen ja reitityksen riippumaton fyysisen sijainnin missä tuote on valmistettu.

### <a name="standard-operation-relations"></a>Standard työvaihesuhteet

Jos yrityksessä käytetään standardoitua koko tuotannon työvaiheiden ja on vain vähän tai ei lainkaan vaihtelua Asetusaika-, Ajoaika, kulutuslaskentaa, Kustannuslaskenta, ja niin edelleen, voit hyötyä luomasta työvaiheiden suhteet kaikkiin toimintoihin. Tässä tapauksessa välttää työvaiheiden suhteet ovat reitiltä tai julkaissut tuotteen luomiseen.  

Jos myös express resurssivaatimukset taitoja ja ominaisuuksia, ja varmista, että reitit riippumaton sivusto, voit parantaa liiketoimintaprosessien jatkuvaa ylläpitoa pienenä.  

Kun käytät tätä lähestymistapaa **työvaiheiden suhteet** sivusta tulee ensisijaiseen kohteeseen ylläpitoon ajoajat ja muita ominaisuuksia.

### <a name="resource-specific-process-times"></a>Resurssikohtaisia prosessiajat

Jos et määritä toiminnon resurssivaatimuksia osana toimintoja resurssin tai resurssiryhmän, käytettävissä olevia resursseja saattaa toimia eri nopeuksilla. Tämän vuoksi aika, joka vaaditaan, jotta voidaan käsitellä toiminto saattaa vaihdella. Voit ratkaista tämän ongelman käyttämällä **kaavan** voit määrittää, miten prosessiaika lasketaan työvaihesuhteen-kenttään. Valittavissa ovat seuraavat vaihtoehdot:

-   **Vakio** – (oletus-vaihtoehto) laskennassa käytetään vain työvaihesuhteen kentät ja kertoo määritetyllä Ajoaika tilausmäärän mukaan.
-   **Kapasiteetin** – laskentaan sisältyvät **kapasiteetti** kentän toimintojen resurssilta. Aika on siis riippuvainen resurssin. Arvo, joka on määritetty operations-resurssissa on kapasiteetti per tunti. Tämä arvo saadaan kertomalla määrän ja **kerroin** arvon työvaihesuhteen.
-   **Erä** – erän kapasiteetti lasketaan käyttämällä tietoja työvaihesuhteen. Eriä ja siksi käsittelyaika sitten voidaan laskea mukaan tilauksen määrä.
-   **Resurssin erän** – tämä vaihtoehto on periaatteessa sama kuin **erän** vaihtoehto. Laskentaan sisältyvät kuitenkin **erän kapasiteetti** kentän toimintojen resurssilta. Aika on siis riippuvainen resurssin.


<a name="see-also"></a>Lisätietoja
--------

[Bills of materials and formulas](bill-of-material-bom.md)

[Cost categories used in production routing](../cost-management/cost-categories-used-production-routings.md)

[Resource capabilities](resource-capabilities.md)

[Electronic signature overview](/dynamics365/operations/organization-administration/electronic-signature-overview)


