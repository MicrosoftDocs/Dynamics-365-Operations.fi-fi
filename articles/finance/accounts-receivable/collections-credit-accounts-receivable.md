---
title: Hyvitykset ja perinnät myyntireskontrassa
description: Myyntireskontran perimistietoja hallitaan keskitetysti yhdessä näkymässä Microsoft Dynamics 365 Financen Perintä-sivulla. Luotonvalvonnan esimiehet voit hallita perintää tästä keskusnäkymästä. Perimisasiamiehet voivat aloittaa perintäprosessin asiakasluetteloista, jotka muodostetaan ennalta määritettyjen ehtojen mukaan, tai Asiakkaat-sivulta.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustAgingSnapshot, CustBankAccounts, CustCollections, CustCollectionsActivitiesListPage, CustCollectionsAgent, CustCollectionsCaseListPage, CustCollectionsPool, CustCollectionsPoolsListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3061
ms.assetid: fd851520-8d93-434b-845b-be127d6ac3a6
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 471de43bc0d171e60100613a6d779a249cd9e92f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189174"
---
# <a name="credit-and-collections-in-accounts-receivable"></a>Hyvitykset ja perinnät myyntireskontrassa

[!include [banner](../includes/banner.md)]

Myyntireskontran perimistietoja hallitaan keskitetysti yhdessä näkymässä Microsoft Dynamics 365 Financen Perintä-sivulla. Luotonvalvonnan esimiehet voit hallita perintää tästä keskusnäkymästä. Perimisasiamiehet voivat aloittaa perintäprosessin asiakasluetteloista, jotka muodostetaan ennalta määritettyjen ehtojen mukaan, tai Asiakkaat-sivulta.

Ennen kuin aloitat perinnän määrittämisen tai sen kanssa työskentelyn, on hyvä ymmärtää seuraavat käsitteet:
-   Asiakkaan erääntymistilannevedokset sisältävät erääntyneet saldotiedot tietyltä aikajaksolta
-   Perinnän asiakaspoolit helpottavat työn organisointia
-   Perimisasiamiehet voivat ylläpitää omia asiakaspoolejaan
-   Luettelosivuilla voi järjestää perinnän asiakkaita, tehtäviä ja tapauksia
-   Kaikki asiakkaan perintätiedot yhdellä sivulla, jolta voit ryhtyä toimenpiteisiin
-   Korkojen ja maksujen peruuttaminen, palauttaminen tai kääntäminen onnistuu yhdellä askeleella
-   Luo poistotapahtumia yhdellä askeleella
-   Ei katetta -maksujen (NSF) käsittely on mahdollista yhdellä askeleella

Seuraavissa osissa kuvataan kutakin konseptia.

## <a name="customer-aging-snapshots"></a>Asiakkaan erääntymistilannevedokset
Erääntymistilannevedos sisältää asiakkaan lasketut erääntyneet saldot kyseisenä ajankohtana. Nämä tiedot näkyvät Erääntyneet saldot- ja Perintä-sivulla. Erääntymistilannevedos on luotava ennen kuin voit tarkastella Perintä-luettelosivujen tietoja. 

Kunkin asiakkaan erääntymistilannevedos sisältää erääntymistilanteen otsikko- ja erittelytietueet, jotka vastaavat kutakin erääntymiskautta erääntymiskauden määrityksessä. 

Erääntymistilannevedoksen otsikko sisältää asiakkaan tilillä erääntyneen kokonaissumman, luottorajan, pakkausluettelon summan, myyntitilauksen summan, riitautettujen tapahtumien määrän ja riitautettujen tapahtumien kokonaissumman. Kaikki tämän asiakkaan tapahtumat sisällytetään näiden summien laskentaan. Erääntynyt kokonaissumma, luottoraja, pakkausluettelon summa ja myyntitilauksen summa näytetään Perintä-sivun Luottotiedot-tietoruudussa. 

Erääntymistilannevedoksen erittelytietue luodaan jokaiselle erääntymiskauden määrittelyyn sisältyvälle erääntymiskaudelle. Kunkin erääntymistilannevedoksen erittelytietue sisältää erääntymiskauden tunnuksen sekä tapahtumien kokonaissumman erääntymiskauden päivämääriltä. Tapahtumat määritetään erääntymiskaudelle, kuten 30 päivää myöhässä. Päivämäärä on suhteessa Erääntyy-päivämäärään, joka määritetään erääntymistilannevedosta luotaessa. Nämä tiedot näytetään Erääntyneet saldot -luettelosivulla sekä ja Perintä-sivun Erääntyneet saldot -tietoruudussa.

## <a name="collections-customer-pools"></a> Perinnän asiakaspoolit 
Asiakaspoolit ovat kyselyitä, jotka määrittävät asiakastietueiden joukkoa, joka näytetään ja jota hallitaan kokoelmia tai erääntymisprosesseja varten. Voit suodattaa Erääntyneet saldot-, Perintätoimet- ja Perintätapaukset-luettelosivujen tietoja asiakaspoolien avulla. Voit suodattaa myös erääntymistilannevedoksen luontiin sisältyneet asiakastilit asiakaspoolien avulla.

## <a name="collections-agents"></a>Perimisasiamiehet
Käyttäjät voivat tarkastella oletusarvoisesti kaikkia asiakastietoja perinnän luettelosivuilla. Voit käyttää perimisasiamiestietueita määrittämään asiakaspoolit, jotka ovat saatavilla tietojen suodattamiseen perinnän luettelosivuilla ja Perintä-sivulle. 

Perimisasiamies on henkilö, joka työskentelee asiakkaiden kanssa varmistaakseen, että maksut peritään ajoissa. Perimisasiamiehet ovat työtekijöitä, jotka on määritetty käyttäjille Käyttäjän määritys -sivulla.

## <a name="collections-list-pages"></a> Perinnän luettelosivut 
Seuraavat luettelosivut ovat hyödyllisiä perintätietojen järjestämisessä.
-   Erääntyneet saldot – Sarakkeet luettelosivulla näyttävät asiakkaan saldot ja erääntyneet summat erääntymiskauden mukaan. Nämä tiedot on tallennettu erääntymistilannevedokseen. Erääntymiskaudet on määritelty käytetyn erääntymiskauden määritelmän mukaan. Erääntymiskauden määritelmä on otettu asiakkaspoolista, jos sellainen on määritetty poolikyselylle. Jos asiakaspoolilla ei ole erääntymiskausimääritelmää, käytetään Myyntireskontran parametrit -sivulla määritettyä oletuserääntymiskauden määritelmää. Jos oletuserääntymiskauden määritystä ei ole määritetty, käytetään Erääntymiskausien määritykset -sivun ensimmäistä erääntymiskausimääritystä.
-   Perintätehtävät – Luettelosivun sarakkeissa näytetään tehtävät, jotka on tunnistettu perintätehtäviksi. Nämä tehtävät luodaan Perintä-sivulla. Aktiviteettien avulla seurataan työtä, joka liittyy perimisiin.
-   Perintätapaukset – Luettelosivun sarakkeissa näytetään tietoja tapauksista, joiden tapausluokkaan sisältyy Perintä-tapaustyyppi.

> [!NOTE]
> Erääntymistilannevedos on luotava ennen kuin voit tarkastella kyseisten luettelosivujen tietoja. Näkyvissä ovat vain niiden asiakkaiden tiedot, joita varten on luotu erääntymistilannevedos. Luettelosivulla näkyvät tietueet voi suodattaa seuraavasti:
> <li>Oletusarvoisesti Finance and Operationsin käyttäjällä on käyttöoikeus kaikkiin asiakkaisiin, joilla on erääntymistilannevedos.</li>
> <li>Jos järjestelmässä on asiakaspooleja, käyttäjä on määritettävä perimisasiamieheksi voidakseen käyttää pooleja perinnän luettelosivun tietojen suodattamiseen. Tiedot rajoitetaan asiakkaisiin, jotka kuuluvat valittuun asiakaspooliin.</li>
> <li>Jos käyttäjä on määritetty perimisasiamieheksi, ainoastaan kyseiselle perimisasiamiehelle valitut poolit ovat saatavilla luettelosivulla. Jos Anna edustajan tarkastella kaikkia asiakaspooleja -asetus on valittuna perimisasiamiehen Perimisasiamies-sivulla, kyseinen edustaja voi käyttää kaikkia pooleja.</li>


## <a name="collections-page"></a> Perintä-sivu
Perintä-sivulla voit tarkastella ja hallita asiakkaan perintätietoja, tehtäviä ja tapauksia sekä suorittaa niille toimenpiteitä. 

Ylemmässä ruudussa näytetään valitun asiakkaan tapaukset. Keskiruutu näyttää asiakkaan tapahtumat. Alemmassa ruudussa näkyvät asiakasta koskevat tehtävät. Voit luoda perintätapauksia seurataksesi yhden tai useamman tapahtuman ja tehtävän perintätietoja. Ylä- ja alaruutujen tietoja voidaan suodattaa tapauskohtaisesti. 

Valitun asiakkaan erääntyneet saldot ja luottorajatiedot näkyvät tietoruuduissa. Nämä tiedot on tallennettu erääntymistilannevedokseen. Voit päivittää erääntymistilannevedoksen tiedot nykyisillä tiedoilla tarvittaessa. 

Toimintoruutu sisältää painikkeita, joissa näytetään valittuun asiakkaaseen, tapaukseen, tapahtumaan tai tehtävään liittyviä tietoja. Voit myös suorittaa yleisiä toimintoja, kuten tapahtuman perintätilan muuttaminen, sähköpostiviestien lähettäminen sähköpostitarjoaja-integraation välityksellä, asiakkaiden hyvittäminen, NSF-maksujen käsittely ja perintäkelvottomien saldojen poiskirjaaminen.

## <a name="waive-reinstate-or-reverse-interest-and-fees"></a> Korkojen ja kulujen peruuttaminen, palauttaminen tai kääntäminen 
Voit peruuttaa, palauttaa tai kääntää kokonaisia korkolaskuja tai niiden osana olevia kuluja ja tapahtumakorkoja. Voit tehdä tämän Kaikki asiakkaat -luettelosivun toimintoruudun Perintä-välilehdeltä napsauttamalla kohtia Korkolasku, Tapahtumakorko tai Kulu. 

Nämä muutokset vaikuttavat vain korkolaskuihin sekä niihin sisältyviin korkoihin ja kuluihin. Poista kaikki maksut, jotka asiakas on velkaa kohdan "Luo poistotapahtumia yhdellä askeleella" vaiheiden avulla.

Lisätietoja on ohjeaiheissa [Korkoryhmäalueen luominen](tasks/create-interest-code-range.md) ja [Koron käsittely](tasks/process-interest.md). 

## <a name="create-writeoff-transactions"></a>Luo poistotapahtumat
Voit kirjata epävarmat saatavat pois napsauttamalla Kirjaa pois -painiketta Perintä-lomakkeessa tai Erääntyneet saldot-, Asiakkaat- ja Avoimet asiakkaan laskut -luettelosivuilla. 

Kun kirjaat pois asiakkaan tapahtumia, kaikki asiakkaan tapahtumat merkitään automaattisesti selvitettäväksi. Poiskirjattava summa riippuu merkittyjen tapahtumien nettosummasta. Poiskirjaustapahtuma luodaan yleisessä kirjauskansiossa ja se voi sisältää enintään kolmen tyyppisiä kirjauskansion rivejä.

-   Ensimmäinen kirjauskansiorivi sisältää asiakastapahtuman poiskirjauksen. Jos merkityt tapahtumat sisältävät useita valuuttakoodien, dimensioiden ja kirjausprofiilien yhdistelmiä, kullekin yhdistelmälle luodaan erillinen kirjauskansion rivi.
-   Toinen kirjauskansiorivi sisältää kirjanpidon poiskirjauksen. Jos merkityt tapahtumat sisältävät useita valuuttakoodien, dimensioiden ja kirjausprofiilien yhdistelmiä, kullekin yhdistelmälle luodaan erillinen kirjauskansion rivi.
-   Kirjauskansiorivin kolmas tyyppi on kirjanpidon poiskirjaustieto arvonlisäveroille. Kirjauskansiorivi luodaan vain, jos Erillinen arvonlisävero -asetus on valittuna myyntireskontran parametrisivulla. Jos merkityt tapahtumat sisältävät useita arvonlisäveron kulutilien, dimensioiden ja arvonlisäverokoodien yhdistelmiä, kullekin yhdistelmälle luodaan erillinen kirjauskansion rivi.

Poiskirjaustapahtuma luodaan tapahtuman valuutalla.

Lisätietoja on ohjeaiheessa [Poiskirjauksen kirjauskansion luominen asiakkaalle](tasks/create-write-off-journal-customer.md).

<a name="process-not-sufficient-funds-nsf-payments"></a>Ei katetta -maksujen (NFS) käsittely  
--------------------------------------------

Voit käsitellä NSF-maksuja napsauttamalla Perintä-sivulla NSF-maksu -kohtaa. Maksu peruutetaan, kun napsautat tätä painiketta. Jos NSF-maksu koskee asiakkaan kuluja, veloitustapahtuma luodaan maksujen kirjauskansioon. Maksusumma perustuu automaattisten veloitusten asetuksiin. Automaattiset veloitukset, joita sovelletaan NSF-maksuihin määritetään kuluryhmässä, joka on valittu Pankkitilit-sivulla pankkitilille, jota asia koskee.





