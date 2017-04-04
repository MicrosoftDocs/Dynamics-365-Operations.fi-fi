---
title: "Vähittäismyyntikanavan viestinnän määrittäminen (Commerce Data Exchange)"
description: "Tässä artikkelissa on Commerce Data Exchangen ja sen komponenttien yleiskatsaus. Siinä kuvataan osan, joka toistetaan kunkin osan tietojen siirto Microsoft Dynamics-365 operaatioille ja vähittäiskaupan kanavia."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: d3b36ec2a3f859215d93dd7ebf1f1ecfb2731c59
ms.lasthandoff: 03/31/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Vähittäismyyntikanavan viestinnän määrittäminen (Commerce Data Exchange)

Tässä artikkelissa on Commerce Data Exchangen ja sen komponenttien yleiskatsaus. Siinä kuvataan osan, joka toistetaan kunkin osan tietojen siirto Microsoft Dynamics-365 operaatioille ja vähittäiskaupan kanavia.

<a name="overview"></a>Yleiskuvaus
--------

Commerce Data Exchange on järjestelmä, joka siirtää tietoja Dynamics 365 operaatioille ja vähittäiskaupan kanavia, kuten Internet-kaupat- tai Tiili ja laastin kaupat. Tietokanta, johon tallennetaan Vähittäismyyntikanavan tiedot on erillään tietokannan toimintoja Dynamics-365. Kanavan tietokanta sisältää vain vähittäismyyntitapahtumissa tarvittavat tiedot. Päätietojen määritetty Dynamics 365 operaatioille ja jakaa kanavat. Tapahtumatietojen luodaan kohdassa järjestelmän myyntiä (POS) tai online tallentaa ja sitten ladata Dynamics 365 operaatioille. Tietojen jakelu tapahtuu asynkronisesti. Tietojen kerääminen ja pakkaaminen lähteessä tapahtuu siis erillisenä prosessina kuin tietojen vastaanottaminen ja käyttäminen kohteessa. Joissakin skenaarioissa, kuten hinta- ja varastohauissa, tiedot on haettava reaaliaikaisesti. Näissä tilanteissa tukemaan Commerce Data Exchange on palvelu, joka mahdollistaa reaaliaikaisen viestinnän Dynamics 365 operaatioille ja kanavan välillä. 

[![päivitetty-retail-grafiikka](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Asynkroninen palvelu
Tietojen muutokset, jotka on lähetettävä kanavia käytetään Microsoft SQL Server-tietokannan toimintoja Dynamics-365 muutosloki. Jakelu aikataulun mukaan, Dynamics 365 työvaiheiden pakkaa tiedot ja tallentaa sen keskitettynä tallennus (Azure blob storage). Erillinen eräprosessi käyttää Commerce Data Exchange: Asynkroninen asiakaskirjasto -kohtaa, kun tämä tietopaketti lisätään kanavatietokantaan. 

[![Async Service](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Retail-ajastus

Ajastustöiden avulla tiedot jaetaan sijainteihin ja niistä pois. Työt muodostuvat alitöistä, jotka määrittävät jaettavat tiedot sisältävät taulut ja taulukentät. Työvaiheiden Dynamics 365 sisältää ennalta ajoituksen työt ja alityöt, jotka täyttävät useimpien organisaatioiden replikointi. Luodaan seuraavat ennalta määritetyt työtyypit:

-   **Lataa työt** – Download työ lähettää tietoja, joka on muuttunut Dynamics 365 työvaiheiden kanavan tietokantoihin. Tietueiden muutoksia seurataan SQL Serverin muutosten seurannan avulla.
-   **Lataa työt (P-työt)** – Lataa noutavat myyntien kauppatapahtumissa kanavan tiedot tietokannan toimintoja Dynamics-365. Noutotyöt siirtävät tiedot lisäävästi. Kun noutotyöt suoritetaan, asynkroninen asiakaskirjasto tarkistaa aiemmin sijainnista vastaanotettujen tietueiden replikointilaskurin. Tietue noudetaan vain, jos sen replikointilaskurin arvo on suurempi kuin löydetty suurin arvo. Noutotyöt eivät päivitä aiemmin noudettuja tietoja.

Jakelu aikataulun avulla suoritetaan tietojen siirto, joko manuaalisesti tai ajoitus työvaiheiden 365 Dynamics-eräajon avulla. Jakeluaikataulu voi sisältää vähintään yhden kanavatietoryhmän ja vähintään yhden ajastustyön.

## <a name="realtime-service"></a>Realtime-palvelu
Commerce Data Exchange: Reaaliaikainen palvelu on integroitu palvelu, joka tarjoaa reaaliaikaisen viestinnän välillä Dynamics 365 operaatioille ja vähittäiskaupan kanavia. Reaaliaikaisen palvelun avulla yksittäiset POS-tietokoneet ja Internet-kauppojen hakemaan tiettyjä toimintoja varten 365 Dynamics reaaliajassa. Vaikka useimmat tärkeimmät toiminnot voidaan suorittaa tietokannan paikallisen kanavan, suora pääsy tietoihin, joka tallennetaan Dynamics 365 työvaiheiden vaatia seuraavissa tilanteissa:

-   Lahjakorttien luovuttaminen ja lunastaminen.
-   Kanta-asiakkuuspisteiden lunastaminen.
-   Hyvityslaskujen tekeminen ja hyvittäminen.
-   Asiakastietueiden luominen ja päivittäminen.
-   Myyntitilausten luominen, päivittäminen ja viimeisteleminen.
-   Varaston vastaanottaminen ostotilauksen tai siirtotilauksen mukaan.
-   Varaston inventointien suorittaminen.
-   Myyntitapahtumien hakeminen myymälöistä ja palautustapahtumien valmisteleminen.

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Ennalta määritetyt Real-time Service-profiili luodaan.


