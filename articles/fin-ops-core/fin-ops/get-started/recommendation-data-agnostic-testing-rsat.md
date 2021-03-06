---
title: Datasta riippumaton testaus Regression Suite Automation Toolilla
description: Tämä ohjeaihe sisältää suosituksia datasta riippumattomaan testaukseen Regression Suite Automation Toolilla.
author: kfend
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 120a88790b7cdb6a8cfcf97cbafeced4685384f2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744660"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a>Datasta riippumaton testaus Regression Suite Automation Toolilla

[!include [banner](../includes/banner.md)]

Vaikka ERP-sovelluksen toiminnan vahvistaminen ei voi olla täysin datasta riippumaton, testauksessa on useita vaiheita ja lähestymistapoja. Näihin testausvaiheisiin sisältyy:  

- SysTest-sovelluskehys
- ATL-sovelluskehys
- Regression Suite Automation Tool (RSAT)

[![Testiluokituksen pyramidi](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)

## <a name="overview"></a>Yleiskuvaus
-   **SysTest-sovelluskehitys** – SysTest-sovelluskehys on luotettava vaihtoehto yksikkötestien kirjoittamiseen. Koska yksikkötestit testaavat tavallisesti metodia tai funktiota, niiden tulisi olla aina datasta riippumattomia ja riippuvaisia vain tiedoista, jotka annetaan osana testiä.
-   **ATL-sovelluskehys** – Microsoftin ATL-sovelluskehys on SysTest-sovelluskehys abstraktio, joka tekee toiminnallisten testien kirjoittamisesta huomattavasti yksinkertaisempaa ja luotettavampaa. Tätä sovelluskehystä tulisi käyttää komponenttitestien tai yksinkertaisten integraatiotestien kirjoittamiseen.
-   **RSAT** – RSAT-työkalula käytetään integrointien ja liiketoimintasyklien testeihin. Liiketoimintasyklien testit, joita kutsutaan myös regressioanalyyseiksi, ovat riippuvaisia olemassa olevista tiedoista. Näistä testeistä voi kuitenkin tehdä datasta riippumattomia, jos otat muut tekijät huomioon. 

    - o Yksikkö- ja komponenttitestit ovat matalan tason testejä ja ne voivat olla täysin datasta riippumattomia (eli eivät riippuvaisia olemassa olevasta tietojoukosta), kun taas liiketoimintasyklien testit, eli regressioanalyysit, ovat riippuvaisia joistakin olemassa olevista tiedoista. Näihin tietoihin sisältyy esimerkiksi määritykset, konfiguraatioasetukset (parametrit) ja perustiedot (asiakas, toimittajat, nimikkeet, jne.), mutta ei koskaan tapahtumatietoja. Jos jotkin näistä tiedoista muuttuvat testauksen aikana, muista palauttaa ne ennalleen osana lopullista testiä.
    - Valitse perustiedot tiettyjen ehtojen perusteella yksittäisten tietueen valitsemisen sijaan. Jos haluat esimerkiksi valita nimikkeen sen dimensioarvojen ja saatavuuden perusteella, suodata tuotteiden luettelo näiden arvojen mukaisesti, valitse ensimmäinen nimike ja kopioi sen numero tulevia testejä varten. Jos kyseessä on yksinkertainen perustietorivi, kuten asiakas, toimittaja tai nimike, se voidaan luoda osana automaatiota ja käyttää tulevissa testeissä ketjutuksen kautta. 
    - o Syötä yksilölliset tiedot, kuten laskujen numerot, käyttämällä numerosarjaa tai Microsoft Excel -funktioita, kuten =TEKSTI(NYT(),"yyyymmddhhmm"). Tämä funktio tarjoaa yksilöllisen numeron joka minuutti, mikä sallii sinun seurata, milloin toiminto tapahtui. Tätä voidaan käyttää muuttujille, kuten tuotteiden vastaanottojen ja toimittajien laskujen numeroille. Nämä testit toimivat edelleen samassa tietokannassa uudelleen ja uudelleen ilman, että niitä tarvitsee palauttaa.
    - Määritä ympäristön **muokkaustilaksi** aina **Luku** tai **Muokkaus** ensimmäisessä testissä, koska oletusasetus on **Automaattinen**. **Automaattinen**-asetukset käyttävät aina edellistä asetusta, ja ne voivat aiheuttaa epäluotettavia testejä. 
 
    [![Asetukset-sivu, Suorituskyky-välilehti](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)
 
    - Vahvista vasta, kun olet suodattanut valinnan tiettyyn tapahtumaan yleisen vahvistuksen sijaan. Jos haluat esimerkiksi käyttää tietueiden määrää, suodata tapahtuman numeron tai päivämäärän perusteella siten, että mitään muita tapahtumia ei käytetä vahvistuksessa. 
    - Jos olet tarkistamassa asiakkaan saldoa tai budjettia, tallenna arvo ensin ja lisää sitten tapahtuma-arvosi vahvistaaksesi odotetun tuloksen sen sijaan, että vahvistaisit kiinteän odotetun arvon. 
 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]