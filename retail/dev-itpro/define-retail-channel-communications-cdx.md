---
title: "Vähittäismyyntikanavan viestinnän määrittäminen (Commerce Data Exchange)"
description: "Tässä artikkelissa on Commerce Data Exchangen ja sen komponenttien yleiskatsaus. Artikkelissa kerrotaan kunkin komponentin toiminta Microsoft Dynamics 365 for Operationsin ja vähittäismyyntikanavien välisessä tiedonsiirrossa."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
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

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on Commerce Data Exchangen ja sen komponenttien yleiskatsaus. Artikkelissa kerrotaan kunkin komponentin toiminta Microsoft Dynamics 365 for Operationsin ja vähittäismyyntikanavien välisessä tiedonsiirrossa.

<a name="overview"></a>Yleiskuvaus
--------

Commerce Data Exchange -järjestelmä siirtää tietoja Dynamics 365 for Operationsin ja jälleenmyyntikanavien, kuten verkkokauppojen tai perinteisten myymälöiden, välillä. Vähittäismyyntikanavan tiedot tallentava tietokanta on eri kuin Dynamics 365 for Operations -tietokanta. Kanavan tietokanta sisältää vain vähittäismyyntitapahtumissa tarvittavat tiedot. Päätiedot määritetään Dynamics 365 for Operationsissa ja jaetaan sitten kanaville. Tapahtumatiedot luodaan myyntipisteen järjestelmässä tai verkkokaupassa, jonka jälkeen ne ladataan Dynamics 365 for Operationsiin. Tietojen jakelu tapahtuu asynkronisesti. Tietojen kerääminen ja pakkaaminen lähteessä tapahtuu siis erillisenä prosessina kuin tietojen vastaanottaminen ja käyttäminen kohteessa. Joissakin skenaarioissa, kuten hinta- ja varastohauissa, tiedot on haettava reaaliaikaisesti. Commerce Data Exchange tukee näitä skenaarioita Dynamics 365 for Operationsin ja kanavan välillä tapahtuvan reaaliaikaisen viestinnän mahdollistavan palvelun avulla. 

[![updated-retail-graphic](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Asynkroninen palvelu
Dynamics 365 for Operations -tietokannan Microsoft SQL Server -palvelimen muutosten seurantaa käytetään kanaville lähetettävien tietojen muutosten määrittämisessä. Dynamics 365 for Operations pakkaa tiedot jakeluaikataulun perusteella ja tallentaa ne keskitettyyn tallennuspaikkaan (Azure Blob -säilö). Erillinen eräprosessi käyttää Commerce Data Exchange: Asynkroninen asiakaskirjasto -kohtaa, kun tämä tietopaketti lisätään kanavatietokantaan. 

[![Asynkroninen palvelu](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Retail-ajastus

Ajastustöiden avulla tiedot jaetaan sijainteihin ja niistä pois. Työt muodostuvat alitöistä, jotka määrittävät jaettavat tiedot sisältävät taulut ja taulukentät. Dynamics 365 for Operations sisältää ennalta määritetyt ajoitustyöt ja -alityöt, jotka vastaavat useimpien organisaatioiden replikointivaatimuksia. Luodaan seuraavat ennalta määritetyt työtyypit:

-   **Lataustyöt** – Lataustyöt lähettävät muutetut tiedot Dynamics 365 for Operationsista kanavatietokantoihin. Tietueiden muutoksia seurataan SQL Serverin muutosten seurannan avulla.
-   **Noutotyöt** – Noutotyöt hakevat myyntitapahtumat kanavasta Dynamics 365 for Operations -tietokantaan. Noutotyöt siirtävät tiedot lisäävästi. Kun noutotyöt suoritetaan, asynkroninen asiakaskirjasto tarkistaa aiemmin sijainnista vastaanotettujen tietueiden replikointilaskurin. Tietue noudetaan vain, jos sen replikointilaskurin arvo on suurempi kuin löydetty suurin arvo. Noutotyöt eivät päivitä aiemmin noudettuja tietoja.

Jakeluaikataulua käytetään tiedonsiirron suorittamisessa manuaalisesti tai ajoittamalla erätyö Dynamics 365 for Operationsissa. Jakeluaikataulu voi sisältää vähintään yhden kanavatietoryhmän ja vähintään yhden ajastustyön.

## <a name="realtime-service"></a>Realtime Service
Commerce Data Exchange: Real-time Service -palvelu on integroitu palvelu, joka mahdollistaa Dynamics 365 for Operationsin ja vähittäismyyntikanavien reaaliaikaisen viestinnän. Real-time Service -palvelun avulla yksittäisten myyntipisteiden tietokoneet ja verkkokaupat voivat hakea määritettyjä tietoja Dynamics 365 for Operationsista reaaliaikaisesti. Vaikka useimmat tärkeät toiminnot voidaan suorittaa paikallisissa kanavatietokannoissa, seuraavat skenaariot vaativat Dynamics 365 for Operationsiin tallennettujen tietojen suoran käytön.

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




