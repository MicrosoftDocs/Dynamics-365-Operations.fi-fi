---
title: "Päivityksen valmistelusiirron testaus"
description: "Tässä ohjeaiheessa kerrotaan, miten voit testata tehtäviä, jotka saat AX 2012:n käytöstäpoiston jälkeen mutta ennen kuin otat Dynamics 365 for Finance and Operationsin käyttöön."
author: tariqbell
manager: AnnBe
ms.date: 05/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 711ad5cc3aafacf209704349effb4e08019205ac
ms.contentlocale: fi-fi
ms.lasthandoff: 06/15/2017

---

# Päivityksen valmistelusiirron testaus
<a id="upgrade-cutover-testing" class="xliff"></a>

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

*Valmistelusiirto* on termi, jota käytämme uuden järjestelmän käyttöönoton viimeisestä prosessista. Valmistelusiirto koostuu tehtävistä, jotka saadaan Microsoft Dynamics AX 2012:n käytöstäpoiston jälkeen mutta ennen kuin otat Microsoft Dynamics 365 for Finance and Operationsin käyttöön. Päivityksen valmistelusiirron testauksen tarkoituksena on harjoitella valmistelusiirtoprosessia, jotta varmistetaan sujuva kokemus kaikille käyttäjille, joihin todellinen käyttöönoton valmistelusiirto vaikuttaa.

Valmistelusiirron aikana on kaksi pääasiallista työnkulkua:

- **Tekninen työnkulku** – Tämä työnkulku sisältää tietopäivityksen suorittamisprosessin. Yrityksesi määrää sallitun käyttämättömyysajan. Käyttämättömyysaikana AX 2012 ja Finance and Operations eivät kumpikaan ole käytettävissä. Työnkulku saattaa hienosäätää päivitysprosessin suorituskykyä, jotta se täyttää yrityksen käyttämättömyysaikaa koskevat vaatimukset.
- **Toiminnallinen työnkulku** – Tämä työnkulku sisältää määritystehtäviä, joka suoritetaan tietopäivityksen jälkeen. Nämä tehtävät pitää dokumentoida ja laskea ja niille pitää kohdistaa tarvittava resurssi, koska toiminnallisen työnkulun ja teknisen työnkulun on sovittava yrityksen käyttämättömyysajan rajoihin.

Seuraavassa kuvassa on koko käyttöönoton valmistelusiirtoprosessi sellaisena kuin se suoritetaan tuotantoympäristössä.

![Valmistelusiirtoprosessi](./media/cutover_1.png)

Valmistelusiirtoprosessi poikkeaa perustietopäivityksestä eristysympäristössä seuraavilla tavoilla:

- AX 2012-tietokantaa ei kopioida vaan varmuuskopioidaan, minkä jälkeen alkuperäistä tietokantaa muokataan. Tämä vaihtoehto on nopeampi ja varmuuskopio sisältää peruutusmahdollisuuden, jos peruuttaminen on välttämätöntä.
- Finance and Operations -tuotantoympäristöllä on rajoitetut käyttöoikeudet, minkä vuoksi Microsoft DSE -tiimi suorittaa nyt tehtävät, jotka on aiemmin suoritettu Application Object Server (AOS) -eristysympäristössä. Tällaisia tehtäviä ovat esimerkiksi bacpac-tiedoston lataaminen ja tuonti ja MajorversionDataUpgrade.zip-paketin suorittaminen.
- Seuraavat tehtävät on lisätty:

    - Savutestin suorittaminen.
    - Sovelluksen määritystehtävien suorittaminen. Tämä voi olla pitkä vaihe riippuen käytetystä toiminnosta. Tässä vaiheessa toimintotiimi määrittää uuden sovelluksen toiminnot siten, että sitä voidaan käyttää päivitetyssä järjestelmässä.
    - Käyttäjien kirjautumisoikeuksien palautus. Ilmoita käyttäjäkunnalle, että päivitys on valmis ja että he voivat taas käyttää järjestelmää.

## Tekninen työnkulku
<a id="technical-workstream" class="xliff"></a>

Tekniseen työnkulkuun osallistuu useita teknisen tiimin jäseniä: tietokannan järjestelmänvalvoja (DBA), AX 2012 -järjestelmänvalvoja, palvelimen järjestelmänvalvojat ja kehittäjät, jotka tuntevat AX 2012:n ja Finance and Operationsin. Tässä ohjeaiheessa kerrotaan, mitä rooleja eri tehtävät edellyttävä.

Valmistelusiirron testauksen aikana tekninen ryhmä keskittyy tietojen päivitysprosessin suorituskyvyn ja luotettavuuden testaukseen, jotta varmistetaan, että se täyttää yrityksen käyttämättömyysaikaa koskevat vaatimukset. Tähän prosessiin liittyy useita laite- ja ohjelmistoelementtejä. Osa näistä elementeistä ovat paikallisia, toiset ovat Microsoftin pilvipalveluissa. Lisäksi siihen liittyy mukautettua useita sovelluskoodin ja vakiokoodin elementtejä. Tämän testauksen seurauksena tulisi olla ympäristön valmistelusiirtoprosessin luotettavuus.

### AX 2012:n AOS-esiintymien poistaminen käytöstä
<a id="turn-off-the-ax-2012-aos-instances" class="xliff"></a>

Tämä tehtävä kuuluu AX 2012:n järjestelmänvalvojalle ja palvelimen järjestelmänvalvojalle.

Seuraavat alueet on tarkistettava:

- **Erätyöt, jotka ovat käynnissä olevat valmistelusiirron aikana** – Pitkäkestoisten erätyö, joka on aloitettu aiemmin, estää järjestelmän pysähtymisen. Suunnittele etukäteen niin, että voit lopettaa AOS-esiintymät haluamasi hetkellä. Erät kannattaa ajoittaa siten, että ne ovat valmiita jonkin aikaa ennen kuin suljet AX 2012:n.
- **Integroidut järjestelmät** – Sinulla voi olla muita järjestelmiä, jotka on integroitu AX 2012 -ympäristöön. Sinun täytyy jakaa näitä järjestelmiä osiin, jotta voit poistaa AX 2012:n käytöstä. Saatat esimerkiksi joutua poistamaan käytöstä integroidut järjestelmät jonkin aikaa ennen kuin suljet itse AX 2012:n siten, jotta mahdolliset käynnissä olevat tapahtumat voidaan suorittaa. Integroitujen järjestelmien vaatimukset vaihtelevat paljon eri yrityksissä. Siksi asiantuntijatiimisi pitää suunnitella tämä skenaario erikseen.

### AX 2012 -tietokannan varmuuskopion luominen
<a id="create-a-backup-of-the-ax-2012-database" class="xliff"></a>

Tämä tehtävä kuuluu tietokannan järjestelmävalvojalle (DBA). Varmuuskopiota käytetään jos peruutus on välttämätön . Sitä käytetään myös viitepisteenä, jota säilytetään määräaika ja joka näyttää järjestelmän tilan siirtymispäivänä.

Seuraavat alueet on tarkistettava:

- Saat konkreettiset ajoitukset varmuuskopiointiprosessia varten.
- Säädä varmuuskopioinnin asetuksia, joita käytetään (esimerkiksi pakkaus / ei pakkaus), jotta varmistetaan nopein mahdollinen varmuuskopio.

### Tietokannan vieminen bacpac-tiedostoon
<a id="export-the-database-to-bacpac" class="xliff"></a>

Tämä tehtävä kuuluu tietokannan järjestelmävalvojalle (DBA). Tämän tehtävän tulos on vientitiedosto, joka ladataan Microsoft Azureen uutta järjestelmää varten.

Seuraavat alueet on tarkistettava:

- Saat konkreettiset ajoitukset varmuuskopiointiprosessia varten.
- Optimoi vientiprosessi nopeimman mahdollisen siirtymiskokemuksen varmistamiseksi. Optimointi saattaa edellyttää seuraavia tehtäviä:

    - Järjestelmäresurssien mittaaminen viennin aikana, kuten suoritin, levyn I/O ja muisti.
    - Jos resurssin pullonkauloja havaitaan, luo suunnitelma niiden minimoimiseksi. Tavallisesti voit pienentää pullonkauloja määrittämällä lisää tarvittavia resursseja.

### Bacpac-tiedoston lataaminen Azure-tallennustilaan
<a id="upload-the-bacpac-file-to-azure-storage" class="xliff"></a>

Tämä tehtävä kuuluu tietokannan tai palvelimen järjestelmänvalvojille. Tämän tehtävän aikana bacpac-tiedosto siirretään Azureen.

Seuraavat alueet on tarkistettava:

- Valitse laite, jota käytetään palvelimeen lataamiseen ja varmista, että Azuren tallennuksen hallintatyökalu on konfiguroitu ja valmiina käyttöön.
- Saat siirtoprosessin konkreettiset ajoitukset mittaamalla sen useita kertoja. Latausajat vaihtelevat Internet-yhteytesi nopeuden ja Azure-datakeskuksesi maantieteellisen sijainnin mukaan suhteessa sijaintiisi.

### Lataa ja tuo bacpac-tiedosto Azure SQL-tietokantaan
<a id="download-and-import-the-bacpac-file-to-the-azure-sql-database" class="xliff"></a>

Kun tämä tehtävä tulee esiin käyttöönoton yhteydessä, Microsoft DSE-tiimi suorittaa sen. Valmistelusiirron testauksen aikana tarvitaan kuitenkin yrityksesi järjestelmänvalvojaa. Tämän tehtävän tulos on vientitiedosto, joka ladataan Microsoft Azureen uutta järjestelmää varten.

Seuraavat alueet on tarkistettava:

- Saat konkreettiset ajoitukset tuontiprosessia varten.
- Optimoi vientiprosessi nopeimman mahdollisen siirtymiskokemuksen varmistamiseksi. Optimointi saattaa edellyttää seuraavia tehtäviä:

    - Mittaa järjestelmäresurssit viennin aikana. Seuraavassa on muutamia esimerkkejä:

        - **AOS-tietokoneessa:** Suoritin, levyn I/O ja muisti
        - **Azuren SQL-tietokantaesiintymässä:** SQL-tietokannan siirtomäärä (DTU). Voit valvoa Azure SQL:n siirtomäärää AOS-tietokoneen Microsoft SQL Server Management Studiossa katsomalla sys.dm_resource_stats -järjestelmänäkymää.

    - Jos resurssin pullonkauloja havaitaan, luo suunnitelma niiden minimoimiseksi. Tavallisesti voit pienentää pullonkauloja määrittämällä lisää tarvittavia resursseja. Koska tämä on Microsoftin ylläpitämä laite, sinun pitää lähettää Microsoftille suurentaa resurssien lisäyspyyntö, jos havaitset pullonkauloja.

### MajorVersiondataUpgrade.zip-paketin suorittaminen
<a id="run-the-majorversiondataupgradezip-package" class="xliff"></a>

Kun tämä tehtävä tulee esiin käyttöönoton yhteydessä, Microsoft DSE-tiimi suorittaa sen. Valmistelusiirron testauksen aikana tarvitaan kuitenkin järjestelmäkehittäjiä. Tämän tehtävän yhteydessä vanha tietokantarakenne muunnetaan uuden järjestelmän rakenteeseen.

Tietokannan synkronointiprosessi suoritetaan osana tätä tehtävää. Tietokannan synkronointi saattaa kestää kauan tietyissä tilanteissa, esimerkiksi kun klusteroitu indeksi on muuttunut taulukossa, koska tämä on kallis SQL-toimenpide.

On suositeltavaa ensin suorittaa analyysi ja virheenkorjausprosessi kehitysympäristössä. Virheenkorjaus- ja analyysivaihtoehdot ovat rajoitetummat eristysympäristössä. Tavoitteena on, että valmistelusiirron testauksen yhteydessä on mahdollisimman vähän tai ei yhtään käsiteltäviä ongelmia.

Seuraavat alueet on tarkistettava:

- Saat konkreettiset ajoitukset tuontiprosessia varten.
- Optimoi prosessi nopeimman siirtymiskokemuksen varmistamiseksi. Optimointi saattaa edellyttää seuraavia tehtäviä:

    - Valvo yksittäisiä päivityksen komentosarjoja ReleaseUpdateScriptsExecution-taulukon avulla.
    - Muuta komentosarjoja suorituskyvyn parantamiseksi. Tehtävä saattaa edellyttää komentosarjan X ++-koodin mukauttamista tietojoukon optimointia varten.
    - Valvo Azure SQL tietomäärää (DTU) Microsoft Dynamicsin elinkaaripalvelujen (LCS) valvontatoiminnolla tai sys.dm_resources_stats -järjestelmänäkymän avulla Management Studiossa. Jos kaikki resurssit ovat käytössä, saatat joutua pyytämään korkeampaa tietokantatasoa Microsoft DSE -tiimiltä.

### AX 2012:n palauttaminen
<a id="roll-back-to-ax-2012" class="xliff"></a>

Tämän tehtävän tarkoituksena on palauttaa tietokanta varmuuskopiosta, joka luotiin, kun AX 2012 poistettiin käytöstä, ja ottaa AX 2012 uudelleen käyttöön. Integroitujen järjestelmien tila voidaan niin ikään joutua palauttamaan. Koska integroidut järjestelmät vaihtelevat yrityskohtaisesti, tämä skenaario on suunniteltava itsenäisesti tilanteen mukaan. Palauttaminen on epätodennäköistä, mutta on kuitenkin tärkeää että prosessia on testattu siltä varalta, että sitä tarvitaan.

## Toiminnallinen työnkulku
<a id="functional-workstream" class="xliff"></a>

Tietojen päivittämisen jälkeen uudessa ympäristössä tarvitaan useita määritystehtäviä. Tämän työnkulun tavoitteena on dokumentoida ja määrittää kaikki määritystehtävät ja määrittää resurssit kullekin tehtävälle, jotta nämä tehtävät voidaan tehdä teknisten työnkulkujen yhteydessä käyttökatkoaikana.

Toimintatehtäviin liittyy yleensä tiettyjen Järjestelmäparametrien tai muiden määritystietojen arvojen muuttaminen. Nämä tehtävät tunnistetaan täydellisen toimintatestausjakson avulla, joka on valmistelusiirron testauksesta erillinen tehtävä. Kun tämäntyyppinen tehtävä on määritetty, se on tarkistettava toimintaresurssien ja järjestelmäkehittäjän kanssa.

Suuremmat muutokset saattavat edellyttää uusien mukautettujen tietojen päivityskomentosarjan kirjoittamista tietojen päivittämistä varten tietojen päivitysprosessin aikana. Kuitenkin toimintaresurssi voi manuaalisesti suorittaa pienempiä muutoksia uuden järjestelmän kautta tietojen päivittämisen jälkeen.

Suuremmat muutokset, joissa on uusia päivityskomentosarjoja, on testattava. Tämän vuoksi vähintään yksi MajorVersionDataUpgrade.zip-paketin iteraatio on suoritettava. On tärkeää, että vertaat paketin tietojen manuaalisen suorittamisen kustannuksia manuaalisen tietojen syötön kustannuksiin.

Valmistelusiirtosuunnitelma-asiakirjaan pitää lisätä jokaista manuaalista muutosta vastaava tehtävä. Tehtävässä pitää näkyä seuraavat tiedot:

-   Mikä tehtävä on ja mitä on suoritettava?
-   Kuka tekee sen?
-   Kuinka kauan se kestää?

