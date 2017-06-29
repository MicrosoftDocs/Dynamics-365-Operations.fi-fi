---
title: Operations-resurssit
description: "Operatiiviset resurssit suorittaa projektin tai tuotantoprosessin aktiviteetit. Ne voivat olla erityyppisiä, ja niillä voi olla eri ominaisuuksia."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WrkCtrCapability
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 30f5ef06fe20894f373e342d09a1e642ab1f0caf
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="operations-resources"></a>Operations-resurssit

[!include[banner](../includes/banner.md)]


Operatiiviset resurssit suorittaa projektin tai tuotantoprosessin aktiviteetit. Ne voivat olla erityyppisiä, ja niillä voi olla eri ominaisuuksia. 

<a name="operations-resources"></a>Operations-resurssit
--------------------

Operatiiviset resurssit ovat koneita, työkaluja, työntekijöitä, toimitiloja, fyysisiä alueita tai toimittajia, jotka suorittavat projektiin tai tuotantoprosessiin liittyvät tehtävät. Ne voivat olla erityyppisiä, ja niillä voi olla eri ominaisuuksia.

-   **Toimittaja** – Ulkoinen resurssi, joka suorittaa projektitehtäviä tai tuotannon työvaiheita. Tällainen on esimerkiksi alihankkija. Linkittämällä toimittajaresursseja toimittajan tiliin voit luoda alihankkijoille ostoja tuoterakenteen tai tuotantorivien perusteella.
-   **Henkilöstö** – Projekti- tai tuotantotyöntekijä, joka suorittaa tehtävän joko yksin tai työkalun tai koneen käyttäjänä. Jos käytät Henkilöstö-toimintoja, voit linkittää henkilöstöresurssit työntekijään. Ajoitusmoduuli voi tämän jälkeen kohdistaa resurssit työntekijälle määriteltyjen osaamisalueiden perusteella.
-   **Kone** – Kone tai muu tuotantolaite, joita tarvitaan tuotannossa.
-   **Työkalu** – Väline tai laite, jota käytetään yleensä yhdessä toisen resurssin kanssa jonkin tehtävän suorittamiseen projektissa tai tuotannossa.
-   **Toimipaikka** – Tietyn kokoinen fyysinen sijainti, jota tehtävän suorittamiseen tarvitaan. Tällainen on esimerkiksi kokoonpanoalue.
-   **Toimitila** – Rakennus tai kiinteä rakennelma, joka tarvitaan tehtävän suorittamiseen.

## <a name="calendars"></a>Kalenterit
Operatiiviselle resurssille voidaan määrittää kalenteri, joka kuvaa kyseisen resurssin kapasiteettia (tunteina). Operatiivisen resurssin työajat määritellään kalenterissa, joka lisätään siihen resurssiryhmään, johon operatiivinen resurssi kuuluu. Voit määrittää kalenterille voimaantulopäivän ja vanhenemispäivämäärän. Tämän jälkeen voit luoda operatiiviselle resurssille useita kalentereita. Määritettyjen kalenterien päivämäärät eivät saa mennä päällekkäin, ja operatiiviselle resurssille voidaan määrittää vain yksi kalenteri kerrallaan. **Huomautus:** Jos resurssiryhmälle ei ole voimassa olevia työskentelykalentereita (esimerkiksi silloin, jos viimeisin määritetty kalenteri tai ainoa määritetty kalenteri on vanhentunut), et voi enää käyttää operatiivisia resursseja, jotka on määritetty resurssiryhmään tuotannon suunnittelemiseksi ja työvaiheiden ajoittamiseksi. Voit myös liittää kalenterin resurssiryhmään, jotta voit määrittää sekä resurssiryhmän että siihen liitettyjen operatiivisten resurssien työajat. Resurssiryhmään kapasiteetti lasketaan kunkin resurssiryhmään liitetyn operatiivisen resurssin kapasiteettien summasta. Resurssiryhmään liitetty kalenteri voi muuttua ajan mittaan.

## <a name="resource-capabilities"></a>Resurssin ominaisuudet
Toiminto on operatiivisen resurssin kyky suorittaa tietty aktiviteetti. Voit liittää operatiiviseen resurssiin useita toimintoja. Ajoitusmoduuli kohdistaa resurssit kohdistamalla kunkin tehtävän resurssivaatimukset käytettävissä olevien operatiivisten resurssien toimintoihin. Toimintoja voi määrittää kaikentyyppisille operatiivisille resursseille (**Työkalu**, **Toimittaja**, **Kone**, **Henkilöstö**, **Toimipaikka** tai **Toimitila**). Jos haluat määrittää toiminnot operatiivisille resursseille rajoitetuksi ajaksi, määritä toiminnolle alkamis- ja päättymispäivämäärä. Lisätietoja on aiheessa [Resurssin ominaisuudet](resource-capabilities.md).

## <a name="resource-groups"></a>Resurssiryhmät
Resurssiryhmä on operatiivisten resurssien joukko, joka edustaa rakeisuutta, jolla haluat ajoittaa resursseja käyttäessäsi työvaiheiden ajoitusmenetelmää. Niinpä resurssiryhmät vastaavat yleensä tuotannon työnohjauksen keltaisten viivojen määrittämää työsolujen fyysistä organisaatiota. Resurssiryhmä määrittää ryhmään lisättyjen operatiivisten resurssien toimipaikan, tuotantoyksikön ja varaston kontekstin. Kun liität operatiivisen resurssin resurssiryhmään, resurssi voidaan ajoittaa toimipaikassa, jossa resurssiryhmä sijaitsee. Luotavia operatiivisia resursseja ei tarvitse liittää resurssiryhmään. Operatiivinen resurssi on kuitenkin liitettävä johonkin resurssiryhmään, ennen kuin se voidaan ajoittaa suorittamaan työ. Operatiivinen resurssi voidaan määrittää resurssiryhmälle rajoitetuksi ajaksi. Voit määrittää operatiivisen resurssin myös useisiin resurssiryhmiin niin, että voit sen jälkeen jakaa resurssit toimipaikkojen kesken. Voimaantulo- ja vanhenemispäivämäärät eivät saa kuitenkaan mennä päällekkäin. Operatiivista resurssia ei voi toisin sanoen liittää kahteen resurssiryhmään samanaikaisesti. Resurssiryhmän määritysten muutokset tulevat voimaan vain uusien resurssien kohdistuksen yhteydessä. Tämä ei vaikuta jo ajoitettujen töiden, työvaiheiden ja projektituntiennusteiden kapasiteettivarauksiin. **Huomautus:** Kun lisäät **Toimittaja**-tyyppisiä operatiivisia resursseja resurssiryhmään, kaikkien kyseiseen resurssiryhmään lisättävien operatiivisten resurssien on oltava **Toimittaja**-tyyppiä ja ne on linkitettävä samaan toimittajatiliin.

## <a name="production-units"></a>Tuotantoyksiköt
Tuotantoyksikkö on hallinnollinen yksikkö, joka on kokoelma resurssiryhmiä. Tuotantoyksikkö voi sisältää useita resurssiryhmiä, mutta resurssiryhmän voidaan määrittää vain yhteen tuotantoyksikköön. Tuotantoyksikkö kuvastaa tuotantoresurssien fyysistä kaavaa, eikä sillä ole vaikutusta tapahtumiin tai niiden käsittelyyn. Sinun on liitettävä tuotantoyksikkö toimipisteeseen. Voit myös määrittää tuotantoyksikölle keräysvaraston ja säilytysvaraston. Tuotantoyksikön avulla voit konsolidoida ja suodattaa tuotantoon liittyviä tietoja. Työnohjauksen johtaja voi esimerkiksi tarkastella tietyn tuotantoyksikön jäljellä olevan kuormituksen ja käytettävissä olevan kapasiteetin yhteenvetoa. Voit vaihtaa resurssiryhmään kohdistettua tuotantoyksikköä. Voit myös poistaa tuotantoyksikön. Tuotantoyksikköön tehtävät muutokset vaikuttavat kuitenkin vain uusiin tilauksiin, jotka luodaan pääajoituksen suorittamisen jälkeen. Jos haluat ottaa tuotantoyksikön muutokset käyttöön aiemmin luoduissa tilauksissa, muutokset on tehtävä manuaalisesti.

## <a name="resource-scheduling"></a>Resurssien ajoitus
Operatiiviset resurssit lisätään tehtäviin, kun projektia tai tuotantoa ajoitetaan. Käytettävissä on kaksi ajoitusmenetelmää: työvaiheiden ajoittaminen ja töiden ajoittaminen. Työvaiheiden ajoituksessa kukin projektitehtävän työvaihe ajoitetaan resurssiryhmälle, jonka sisältämät operatiiviset resurssit vastaavat työvaiheelle määritettyjä resurssivaatimuksia. Jos työvaiheeseen tarvitaan jokin tietty operatiivinen resurssi, ajoitus varaa kapasiteettia vain ryhmän tietylle operatiiviselle resurssille. Töiden ajoitus on tarkempi kuin työvaiheiden ajoitus. Se erittelee kunkin työvaiheen yksittäisiksi tehtäviksi tai töiksi. Nämä työt määritetään sitten ne suorittaville operatiivisille resursseille. Ajoitus varaa kapasiteettia resurssiryhmistä tuotannon reititys- tai projektitehtäville määritettyjen työvaiheaikojen perusteella. Jos käytettävissä on vain rajallisesti kapasiteettia, ajoitus on riippuvainen tehtävän suorittamiseen tarvittavien operatiivisten resurssien saatavuudesta. Työvaiheiden ajoituksessa resurssiryhmään kapasiteetti on ryhmään kuuluvien operatiivisten resurssien käytettävissä olevan kapasiteetin summa. Operatiivisille resursseille jo aiemmin tehdyt kapasiteettivaraukset katsotaan kapasiteetiksi, joka ei ole käytettävissä. Jos tuotannolle ei ole riittävästi käytettävissä olevaa kapasiteettia, tuotantotilaukset saattavat viivästyä tai jopa pysähtyä. **Resurssit**-sivulla voit määrittää useita ominaisuuksia, jotka määrittävät, miten kapasiteettivaraukset tehdään:

-   **Kapasiteetti** – Määritä operatiivisten resurssien kapasiteetti tunteina kapasiteetin mittayksikön perusteella.
-   **Erän kapasiteetti** – Määritä, kuinka monta kappaletta operatiivinen resurssi pystyy enintään käsittelemään suorituksen aikana.
-   **Tehokkuusprosentti** – Määritä operatiiviselta resurssilta odotettava tehokkuus. Tehokkuusprosentti muokkaa operatiivisen resurssin tuotantokapasiteettia ja vaikuttaa resurssille varattavaan aikaan. Operatiivisia resursseja käyttävien työvaiheiden läpimenoaikoja oikaistaan vastaavasti. Laskutoimituksessa käytetään seuraavaa kaavaa: Ajoitusaika = Aika × 100 ÷ Tehokkuusprosentti Tässä kaavassa *Aika* sisältää sekä asetus- että suoritusajan.
-   **Työvaiheen karkeasuunnittelun prosenttiosuus** – Määritä työvaiheiden ajoituksessa käytettävän operatiivisen resurssin kapasiteetin enimmäisprosentti. Arvon olisi oltava alle 100 prosenttia, jotta kapasiteetti voisi joustaa töitä ajoitettaessa.
-   **Rajallinen kapasiteetti** – Määritä asetukseksi **Kyllä**, jos operatiivinen resurssi tulee ajoittaa käytettävissä olevan toteutuneen kapasiteetin perusteella ja aiemmin määritetyt kapasiteettivaraukset tulee ottaa huomioon. Jos tämän asetuksen arvoksi on määritetty **Ei**, operatiivisella resurssin kapasiteetin oletetaan olevan rajaton, ja resurssi saatetaan ylivarata.
-   **Rajallinen ominaisuus** – Määritä asetukseksi **Kyllä**, jos haluat, että operatiivinen resurssi ajoitetaan käytettävissä olevan todellisen kapasiteetin perusteella suhteessa tarvittaviin työajan ajoitusominaisuuksiin.
-   **Poissulkeva** – Valitse asetukseksi **Kyllä**, jos et halua, että operatiivinen resurssi on muiden töiden tai työvaiheiden käytettävissä, ennen kuin nykyinen tuotanto on valmistunut. Tällöin operatiivista resurssia ei voi käyttää, vaikka resurssin suoritusajassa olisi aukkoja.
-   **Pullonkaularesurssi** – Määritä operatiivinen resurssi pullonkaularesurssiksi. Pullonkaularesurssi ajoitetaan käyttämällä rajallista kapasiteettia, kun **Rajallinen kapasiteetti**- ja **Pullonkaula-ajoitus**-vaihtoehdot on valittu **Pääsuunnitelmat**-sivulla.

Jos haluat ajoittaa useita operatiivisia resursseja samanaikaisesti esimerkiksi tuotannon työvaiheen suorittamista varten, sinun täytyy määrittää eri resurssien vaatimukset käyttämällä ensisijaisia ja toissijaisia työvaiheita. Tämän jälkeen voit varata useita operatiivisia resursseja, joilla on eri kapasiteetti. Operatiiviset resurssit, jotka ajoitetaan ensisijaiseen työvaiheeseen, määrittävät tehtävän keston.

## <a name="lean-work-cells"></a>Lean-työsolut
Voit määrittää resurssiryhmän lean-työsoluksi. Tällöin resurssiryhmä voi olla tuotantovirran osa. Määrittämällä resurssiryhmään lean-työsoluksi voit myös estää resurssiryhmän ja liitettyjen operatiivisten resurssien kohdistamisen tuotantotilauksen työvaiheisiin tai projektituntiennusteeseen. Kullekin lean-työsoluna toimivalle resurssiryhmälle on määritettävä seuraavat tiedot:

-   **Kalenteri** – Työsolun työkalenteri, jossa täytyy olla Tavallinen työpäivä -ominaisuus.
-   **Saapuva varasto ja toimipaikka** – Oletussijainti, josta tehtävän materiaalit keräillään.
-   **Lähtevä varastoa ja toimipaikka** – Oletussijainti, johon työsolun tuotanto siirretään.
-   **Suoritusajan kustannusluokka** – Tämä luokka on määritettävä työsolulle, jos kustannuslaskennassa seurataan suoria työkustannuksia.

Kun resurssiryhmää käytetään lean-työsoluna, työsolun kapasiteetti määritetään suoraan resurssiryhmälle. Operatiivisia resursseja ei siten tarvitse liittää resurssiryhmään. Vain kun alihankkija hallinnoi työsolua, **Toimittaja**-tyyppinen operatiivinen resurssi on liitettävä työsoluun. Jos liität operatiivisen resurssin resurssiryhmään, joka on merkitty työsoluksi, tämä ei vaikuta työsolun kapasiteettiin.

## <a name="costing-resources"></a>Kustannuslaskentaresurssit
Kun määrität tehtävän, kuten reitityksen työvaiheen tai projektituntiennusteen, voit määrittää vaatimuksen tietystä operatiivisesta resurssista tai resurssiryhmästä. Voit kuitenkin määrittää vaatimuksen myös tietyntyyppisestä operatiivisesta resurssista tai operatiivisesta resurssista, jolla on tietty pätevyys tai osaamisalue. Tästä syystä todellinen resurssimääritys tehdään vasta, kun tehtävä on ajoitettu ja kapasiteetti varattu. Näin voit reititystyövaiheessa määrittää, että arvioinnin ja tuoterakennelaskelman on perustuttava tiettyyn operatiiviseen resurssiin. Operatiivista resurssia kutsutaan kustannuslaskentaresurssiksi. Voit myös siirtää kustannusluokkia ja työvaiheaikoja kustannuslaskentaresurssista tehtävään. Kun työvaihe ajoitetaan, arviointi ja tuoterakenteen laskenta tehdään käyttämällä operatiivista resurssia, joka on todellisuudessa ajoitettu.




