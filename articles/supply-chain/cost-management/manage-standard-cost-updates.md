---
title: Vakiokustannuspäivitysten hallinta
description: Vakiokustannustietojen päivityksiä voi hallita kahdella eri tavalla, joita ovat yhden tai kahden version menetelmä.
author: AndersGirke
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8e72d4e90ac83787ed7c58d91c2102696acfac68
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "367544"
---
# <a name="manage-standard-cost-updates"></a>Vakiokustannuspäivitysten hallinta

[!include [banner](../includes/banner.md)]

Vakiokustannustietojen päivityksiä voi hallita kahdella eri tavalla, joita ovat yhden tai kahden version menetelmä. 

Yhden version menetelmässä käytetään yhtä kustannuslaskennan versiota, joka sisältää kaikki kustannustietueet. Näihin tietueisiin sisältyvät alkuperäiset kustannukset sekä kaikki kustannuspäivitykset.

Kahden version menetelmässä käytetään yhtä versiota, joka sisältää alkuperäisen kustannusten tietueet ja toista versiota, joka sisältää tiedot kaikista kustannuspäivityksistä. Kahden version mallin tärkein etu on se, että kustannuspäivitykset voi rajata selkeästi ja asettaa seurantaan erilliseen kustannuslaskelmaversioon eikä tämä vaikuta alkuperäiseen kustannuslaskelmaversioon. Kahden version mallin avulla voidaan määrittää useita lisäpäivityksiä siten, että jokaisella lisäpäivityksellä on oma erillinen kustannuslaskelmaversionsa, joka sisältää asianmukaiset lisäkustannustietueet. 

**Esimerkki** 

Seuraavassa esimerkissä kuvataan, miten yhden version ja kahden version menettelyitä voi käyttää valmistusympäristön vakiokustannusten päivityksissä. Päivitykset voivat esimerkiksi vastata uusia nimikkeitä tai korjauksia. Oletetaan, että yksi kustannuslaskelmaversio edustaa kuluvan vuoden vakiokustannuksia. Tämän version tunnus on 2016-STD. 2016-STD -versio sisältää kaikkien nimikkeiden nykyiset aktiiviset kustannukset. Lisäksi se sisältää kaikki reititykseen liittyvät kustannusluokat sekä yleiskustannusten laskentakaavat, jotka olivat tiedossa vuoden 2016 alkaessa. 2016-STD on alkuperäinen kustannuslaskelmaversio.

-   **Yhden version malli kustannustietojen päivityksessä** − Yhden version malli tarkoittaa, että alkuperäinen kustannuslaskelmaversio 2016-STD sisältää kaikki kustannustietueet. Kustannuspäivitykset kirjataan 2016-STD -versioon ja niiden tilaksi määritetään "Odottava". Odottavat kustannukset voidaan lisätä manuaalisesti uusia ostettuja nimikkeitä varten, tai ne voidaan laskea valmistettua nimikettä varten siten, että korjaukset on otettu huomioon. Yhden version mallissa tuoterakennelaskelmat eivät edellytä varmistustietojen lähdettä, koska kaikki aktiiviset kustannukset sisältyvät kustannuslaskelmaversioon. Kun odottavat kustannukset on aktivoitu, alkuperäinen kustannuslaskelmaversio 2016-STD sisältää jälleen kaikki nykyiset aktiiviset kustannukset.
-   **Kahden version malli kustannustietojen päivityksessä** − Kahden version mallissa edellytetään toista kustannuslaskelmaversiota, joka sisältää ainoastaan kustannuspäivitykset. Tämän version tunnus on 2016-STD-CHANGES. Kustannuspäivitykset kirjataan 2016-STD-CHANGES-versioon ja niiden tilaksi määritetään Odottaa. Kun käytössä on kaksi versiota, valmistettujen nimikkeiden odottavien kustannusten tuoterakennelaskelmat vaativat varmistustietojen lähteen. Tämä johtuu siitä, että kustannuslaskelmien lisäversio 2016-STD-CHANGES sisältää vain osan kustannustiedoista. Varmistuksen voi esittää aktiivisna kustannuksina tai kustannuslaskennan versiona 2016-STD, koska molemmissa tunnistetaan kustannustietojen lähde silloin, kun se ei sisälly 2016-STD-CHANGES -versioon. Kun odottavat kustannukset ovat käytössä, kustannuslaskennan versio 2016-STD-CHANGES sisältää nykyiset aktiiviset kustannukset, jotka vastaavat päivityksiä; alkuperäinen kustannuslaskelmaversio 2016-STD pysyy koskemattomana. Kun käytössä on kahden version malli, alkuperäisen kustannuslaskelmaversion estomenettelyt on määritettävä estämään päivitykset. Samat estomenettelyt tulisi määrittää toiselle kustannuslaskelmaversiolle, lukuun ottamatta valikoitua alkamispäivämäärää ja valikoitua estokäytäntöjä, joilla määritellään sallitut päivitykset. Määritetty alkamispäivämäärä tulisi päivittää jokaisen muutoserän yhteydessä vastaamaan ajoitettua aktivointipäivämäärää.

Tässä esimerkissä käytettiin vielä yhtä kustannuslaskelmaversiota koko vuoden 2016 päivitysten hallintaan. Lisäkustannuslaskelmaversioita voi käyttää useita; esimerkiksi jokaisella päivityserällä voi olla oma, erillinen versionsa. Kun käytössä on useampia kustannuslaskentoja, varmistus on ilmaistava aktiivisina kustannuksina, koska ne jakautuvat useille kustannuslaskentaversioille.





