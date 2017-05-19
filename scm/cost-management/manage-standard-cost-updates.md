---
title: "Vakiokustannuspäivitysten hallinta"
description: "Vakiokustannustietojen päivityksiä voi hallita kahdella eri tavalla: yhden tai kahden version menetelmällä."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 12ef9b3de7b489eb53de0a7ea82e4605cd2f4b0b
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="manage-standard-cost-updates"></a>Vakiokustannuspäivitysten hallinta

[!include[banner](../includes/banner.md)]


Vakiokustannustietojen päivityksiä voi hallita kahdella eri tavalla: yhden tai kahden version menetelmällä. 

Yhden version menetelmässä käytetään yhtä kustannuslaskennan versiota, joka sisältää kaikki kustannustietueet. Näihin tietueisiin sisältyvät alkuperäiset kustannukset sekä kaikki kustannuspäivitykset.
Kahden version menetelmässä käytetään yhtä versiota, joka sisältää alkuperäisen kustannusten tietueet ja toista versiota, joka sisältää tiedot kaikista kustannuspäivityksistä. Kahden version mallin tärkein etu on se, että kustannuspäivitykset voi rajata selkeästi ja asettaa seurantaan erilliseen kustannuslaskelmaversioon eikä tämä vaikuta alkuperäiseen kustannuslaskelmaversioon. Kahden version mallin avulla voidaan määrittää useita lisäpäivityksiä siten, että jokaisella lisäpäivityksellä on oma erillinen kustannuslaskelmaversionsa, joka sisältää asianmukaiset lisäkustannustietueet. **Esimerkki** Seuraavassa esimerkissä kuvataan, miten yhden version ja kahden version menettelyitä voi käyttää valmistusympäristön vakiokustannusten päivityksissä. Päivitykset voivat esimerkiksi vastata uusia nimikkeitä tai korjauksia. Oletetaan, että yksi kustannuslaskelmaversio edustaa kuluvan vuoden vakiokustannuksia. Tämän version tunnus on 2016-STD. 2016-STD -versio sisältää kaikkien nimikkeiden nykyiset aktiiviset kustannukset. Lisäksi se sisältää kaikki reititykseen liittyvät kustannusluokat sekä yleiskustannusten laskentakaavat, jotka olivat tiedossa vuoden 2016 alkaessa. 2016-STD on alkuperäinen kustannuslaskelmaversio.
-   **Yhden version malli kustannustietojen päivityksessä** − Yhden version malli tarkoittaa, että alkuperäinen kustannuslaskelmaversio 2016-STD sisältää kaikki kustannustietueet. Kustannuspäivitykset kirjataan 2016-STD -versioon ja niiden tilaksi määritetään "Odottava". Odottavat kustannukset voi lisätä manuaalisesti uusille ostetuille nimikkeille, tai ne voidaan laskea valmistetulle nimikkeelle niin, että ne vastaavat korjauksia. Yhden version lähestymistapaa käytettäessä tuoterakennelaskelmat eivät edellytä varmistustietojen lähdettä, koska kaikki aktiiviset kustannukset sisältyvät kustannuslaskentaversioon. Kun odottavat kustannukset on aktivoitu, alkuperäinen kustannuslaskelmaversio 2016-STD sisältää jälleen kaikki nykyiset aktiiviset kustannukset.
-   **Kahden version malli kustannustietojen päivityksessä** − Kahden version mallissa edellytetään toista kustannuslaskelmaversiota, joka sisältää ainoastaan kustannuspäivitykset. Tämän version tunnus on 2016-STD-CHANGES. Kustannuspäivitykset tallennetaan 2016-STD-CHANGES -version tilassa "Odottava". Kahden version mallia käytettäessä valmistettujen nimikkeiden tuoterakennelaskelmissa odottavat kustannukset tarvitsevat lähteen varmistustiedoille. Tämä johtuu siitä, että kustannuslaskelmien lisäversio 2016-STD-CHANGES sisältää vain osan kustannustiedoista. Varmistuksen voi esittää aktiivisna kustannuksina tai kustannuslaskennan versiona 2016-STD, koska molemmissa tunnistetaan kustannustietojen lähde silloin, kun se ei sisälly 2016-STD-CHANGES -versioon. Kun odottavat kustannukset on aktivoitu, nykyiset, päivityksiä vastaavat aktiiviset kustannukset ovat mukana lisäkustannuslaskelmaversiossa 2016-STD-CHANGES, ja alkuperäinen kustannuslaskelmaversio 2016-STD jää entiselleen. Kun käytössä on kahden version malli, alkuperäisen kustannuslaskelmaversion estomenettelyt on määritettävä estämään päivitykset. Samat estomenettelyt tulisi määrittää toiselle kustannuslaskelmaversiolle, lukuun ottamatta valikoitua alkamispäivämäärää ja valikoitua estokäytäntöjä, joilla määritellään sallitut päivitykset. Määritetty alkamispäivämäärä tulisi päivittää jokaisen muutoserän yhteydessä vastaamaan ajoitettua aktivointipäivämäärää.

Tässä esimerkissä käytettiin vielä yhtä kustannuslaskelmaversiota koko vuoden 2016 päivitysten hallintaan. Lisäkustannuslaskelmaversioita voi käyttää useita; esimerkiksi jokaisella päivityserällä voi olla oma, erillinen versionsa. Kun käytössä on useampia kustannuslaskentoja, varmistus on ilmaistava aktiivisina kustannuksina, koska ne jakautuvat useille kustannuslaskentaversioille.






