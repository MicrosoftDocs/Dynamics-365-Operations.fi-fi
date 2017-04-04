---
title: "Standardikustannusten päivityksissä hallinta"
description: "Standardikustannusten päivityksiä voi hallita kahdella eri - yhden version malli ja kahden version malli."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 7e0f0817ff37c82ed98a51f10bcdde7e785a19a3
ms.lasthandoff: 03/31/2017


---

# <a name="manage-standard-cost-updates"></a>Standardikustannusten päivityksissä hallinta

Standardikustannusten päivityksiä voi hallita kahdella eri - yhden version malli ja kahden version malli. 

Yhden version menetelmässä käytetään yhtä kustannuslaskennan versiota, joka sisältää kaikki kustannustietueet. Näihin tietueisiin sisältyvät alkuperäiset kustannukset sekä kaikki kustannuspäivitykset.
Kahden version menetelmässä käytetään yhtä versiota, joka sisältää alkuperäisen kustannusten tietueet ja toista versiota, joka sisältää tiedot kaikista kustannuspäivityksistä. Kahden version mallin tärkein etu on se, että kustannuspäivitykset voi rajata selkeästi ja asettaa seurantaan erilliseen kustannuslaskelmaversioon eikä tämä vaikuta alkuperäiseen kustannuslaskelmaversioon. Kahden version mallin avulla voidaan määrittää useita lisäpäivityksiä siten, että jokaisella lisäpäivityksellä on oma erillinen kustannuslaskelmaversionsa, joka sisältää asianmukaiset lisäkustannustietueet. **Esimerkki** Seuraavassa esimerkissä kuvataan, miten yhden version ja kahden version menettelyitä voi käyttää valmistusympäristön vakiokustannusten päivityksissä. Päivitykset voivat esimerkiksi vastata uusia nimikkeitä tai korjauksia. Oletetaan, että yksi kustannuslaskelmaversio edustaa kuluvan vuoden vakiokustannuksia. Tämän version tunnus on 2016-STD. 2016-STD -versio sisältää kaikkien nimikkeiden nykyiset aktiiviset kustannukset. Lisäksi se sisältää kaikki reititykseen liittyvät kustannusluokat ja yleiskustannusten laskentakaavoja, jotka ovat olleet tiedossa vuoden 2016 alkuun. 2016-STD on alkuperäiseen kustannuslaskelmaversioon.
-   **Yhden version malli kustannustietojen päivityksessä** − Yhden version malli tarkoittaa, että alkuperäinen kustannuslaskelmaversio 2016-STD sisältää kaikki kustannustietueet. Kustannusten päivityksiä 2016-STD kirjataan ja määritetään tila on "Odottaa". Odottavat kustannukset voi lisätä manuaalisesti uusia ostettuja nimikkeitä varten, tai ne voidaan laskea valmistettua nimikettä vastaavat korjaukset. Yhden version lähestymistapaa käytetään, kun tuoterakennelaskelmat eivät edellytä varalla oleva tietolähde, koska kaikki aktiiviset kustannukset sisältyvät kustannuslaskelmaversioon. Kun odottavat kustannukset on aktivoitu, alkuperäinen kustannuslaskelmaversio 2016-STD sisältää jälleen kaikki nykyiset aktiiviset kustannukset.
-   **Kahden version malli kustannustietojen päivityksessä** − Kahden version mallissa edellytetään toista kustannuslaskelmaversiota, joka sisältää ainoastaan kustannuspäivitykset. Tämän version tunnus on 2016-STD-CHANGES. Kustannuspäivitykset tallennetaan 2016-STD-CHANGES -version tilassa "Odottava". Kahden version mallia käytettäessä valmistettujen nimikkeiden tuoterakennelaskelmissa odottavat kustannukset tarvitsevat lähteen varmistustiedoille. Tämä johtuu siitä, että kustannuslaskelmien lisäversio 2016-STD-CHANGES sisältää vain osan kustannustiedoista. Varmistuksen voi esittää aktiivisna kustannuksina tai kustannuslaskennan versiona 2016-STD, koska molemmissa tunnistetaan kustannustietojen lähde silloin, kun se ei sisälly 2016-STD-CHANGES -versioon. Kun odottavat kustannukset on aktivoitu, nykyiset, päivityksiä vastaavat aktiiviset kustannukset ovat mukana lisäkustannuslaskelmaversiossa 2016-STD-CHANGES, ja alkuperäinen kustannuslaskelmaversio 2016-STD jää entiselleen. Kun käytössä on kahden version malli, alkuperäisen kustannuslaskelmaversion estomenettelyt on määritettävä estämään päivitykset. Samat estomenettelyt tulisi määrittää toiselle kustannuslaskelmaversiolle, lukuun ottamatta valikoitua alkamispäivämäärää ja valikoitua estokäytäntöjä, joilla määritellään sallitut päivitykset. Määritetty alkamispäivämäärä tulisi päivittää jokaisen muutoserän yhteydessä vastaamaan ajoitettua aktivointipäivämäärää.

Tässä esimerkissä käytetään toisen kustannuslaskelmaversion koko vuoden 2016 päivitysten hallintaan. Useamman kuin yhden toisen kustannuslaskelmaversion avulla voidaan esimerkiksi erillinen versio kutakin erää päivitykset. Kun käytössä on useampia kustannuslaskentoja, varmistus on ilmaistava aktiivisina kustannuksina, koska ne jakautuvat useille kustannuslaskentaversioille.




