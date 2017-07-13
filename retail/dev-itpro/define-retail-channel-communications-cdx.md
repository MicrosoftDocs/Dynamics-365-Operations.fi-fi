---
title: "Vähittäismyyntikanavan viestinnän määrittäminen (Commerce Data Exchange)"
description: "Tässä artikkelissa on Commerce Data Exchangen ja sen komponenttien yleiskatsaus. Artikkelissa kerrotaan kunkin komponentin toiminta Microsoft Dynamics 365 for Retailin ja vähittäismyyntikanavien välisessä tiedonsiirrossa."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 68252e52da47b89166627edbf2aa530e762354c6
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017


---

# Vähittäismyyntikanavan viestinnän määrittäminen (Commerce Data Exchange)
<a id="define-retail-channel-communications-commerce-data-exchange" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on Commerce Data Exchangen ja sen komponenttien yleiskatsaus. Artikkelissa kerrotaan kunkin komponentin toiminta Microsoft Dynamics 365 for Retailin ja vähittäismyyntikanavien välisessä tiedonsiirrossa.

Yleiskuvaus
<a id="overview" class="xliff"></a>
--------

Commerce Data Exchange -järjestelmä siirtää tietoja Dynamics 365 for Retailin ja vähittäismyyntikanavien, kuten verkkokauppojen tai perinteisten myymälöiden, välillä. Vähittäismyyntikanavan tiedot tallentava tietokanta on eri kuin Dynamics 365 for Retail -tietokanta. Kanavan tietokanta sisältää vain vähittäismyyntitapahtumissa tarvittavat tiedot. Päätiedot määritetään Dynamics 365 for Retailissa ja jaetaan sitten kanaville. Tapahtumatiedot luodaan myyntipisteen järjestelmässä tai verkkokaupassa, jonka jälkeen ne ladataan Dynamics 365 for Retailiin. Tietojen jakelu tapahtuu asynkronisesti. Tietojen kerääminen ja pakkaaminen lähteessä tapahtuu siis erillisenä prosessina kuin tietojen vastaanottaminen ja käyttäminen kohteessa. Joissakin skenaarioissa, kuten hinta- ja varastohauissa, tiedot on haettava reaaliaikaisesti. Commerce Data Exchange tukee näitä skenaarioita Dynamics 365 for Retailin ja kanavan välillä tapahtuvan reaaliaikaisen viestinnän mahdollistavan palvelun avulla. 

[![updated-retail-graphic](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## Asynkroninen palvelu
<a id="async-service" class="xliff"></a>
Dynamics 365 for Retail -tietokannan Microsoft SQL Server -palvelimen muutosten seurantaa käytetään kanaville lähetettävien tietojen muutosten määrittämisessä. Dynamics 365 for Retail pakkaa tiedot jakeluaikataulun perusteella ja tallentaa ne keskitettyyn tallennuspaikkaan (Azure Blob -säilö). Erillinen eräprosessi käyttää Commerce Data Exchange: Asynkroninen asiakaskirjasto -kohtaa, kun tämä tietopaketti lisätään kanavatietokantaan. 

[![Asynkroninen palvelu](./media/async-300x239.png)](./media/async.png)

### Retail-ajastus
<a id="retail-scheduler" class="xliff"></a>

Ajastustöiden avulla tiedot jaetaan sijainteihin ja niistä pois. Työt muodostuvat alitöistä, jotka määrittävät jaettavat tiedot sisältävät taulut ja taulukentät. Dynamics 365 for Retail sisältää ennalta määritetyt ajoitustyöt ja -alityöt, jotka vastaavat useimpien organisaatioiden replikointivaatimuksia. Luodaan seuraavat ennalta määritetyt työtyypit:

-   **Lataustyöt** – Lataustyöt lähettävät muutetut tiedot Dynamics 365 for Retailista kanavatietokantoihin. Tietueiden muutoksia seurataan SQL Serverin muutosten seurannan avulla.
-   **Noutotyöt** – Noutotyöt hakevat myyntitapahtumat kanavasta Dynamics 365 for Retail -tietokantaan. Noutotyöt siirtävät tiedot lisäävästi. Kun noutotyöt suoritetaan, asynkroninen asiakaskirjasto tarkistaa aiemmin sijainnista vastaanotettujen tietueiden replikointilaskurin. Tietue noudetaan vain, jos sen replikointilaskurin arvo on suurempi kuin löydetty suurin arvo. Noutotyöt eivät päivitä aiemmin noudettuja tietoja.

Jakeluaikataulua käytetään tiedonsiirron suorittamisessa manuaalisesti tai ajoittamalla erätyö Dynamics 365 for Retailissa. Jakeluaikataulu voi sisältää vähintään yhden kanavatietoryhmän ja vähintään yhden ajastustyön.

## Realtime Service
<a id="realtime-service" class="xliff"></a>
Commerce Data Exchange: Real-time Service on integroitu palvelu, joka mahdollistaa Dynamics 365 for Retailin ja vähittäismyyntikanavien reaaliaikaisen viestinnän. Real-time Servicen avulla yksittäisten myyntipisteiden tietokoneet ja verkkokaupat voivat hakea määritettyjä tietoja Dynamics 365 for Retailista reaaliaikaisesti. Vaikka useimmat tärkeät toiminnot voidaan suorittaa paikallisissa kanavatietokannoissa, seuraavat skenaariot vaativat Dynamics 365 for Retailiin tallennettujen tietojen suoraa käyttöä:

-   Lahjakorttien luovuttaminen ja lunastaminen.
-   Kanta-asiakkuuspisteiden lunastaminen.
-   Hyvityslaskujen tekeminen ja hyvittäminen.
-   Asiakastietueiden luominen ja päivittäminen.
-   Myyntitilausten luominen, päivittäminen ja viimeisteleminen.
-   Varaston vastaanottaminen ostotilauksen tai siirtotilauksen mukaan.
-   Varaston inventointien suorittaminen.
-   Myyntitapahtumien hakeminen myymälöistä ja palautustapahtumien valmisteleminen.

[![Real-time Service -palvelu](./media/rts.png)](./media/rts.png) 

Luodaan ennalta määritetty Real-time Service -palvelun profiili.




