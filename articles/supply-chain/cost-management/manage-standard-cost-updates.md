---
title: Vakiokustannuspäivitysten hallinta
description: Vakiokustannustietojen päivityksiä voi hallita kahdella eri tavalla, joita ovat yhden tai kahden version menetelmä.
author: JennySong-SH
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a6d693b58e7fbbd8e082d68d124eae52fb840b02
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674530"
---
# <a name="manage-standard-cost-updates"></a>Vakiokustannuspäivitysten hallinta

[!include [banner](../includes/banner.md)]

Vakiokustannustietojen päivityksiä voi hallita kahdella eri tavalla, joita ovat yhden tai kahden version menetelmä.

Yhden version menetelmässä käytetään yhtä kustannuslaskennan versiota, joka sisältää kaikki kustannustietueet. Näihin tietueisiin sisältyvät alkuperäiset kustannukset sekä kaikki kustannuspäivitykset.

Kahden version menetelmässä käytetään yhtä versiota, joka sisältää alkuperäisen kustannusten tietueet ja toista versiota, joka sisältää tiedot kaikista kustannuspäivityksistä. Kahden version mallin tärkein etu on se, että kustannuspäivitykset voi rajata selkeästi ja asettaa seurantaan erilliseen kustannuslaskelmaversioon eikä tämä vaikuta alkuperäiseen kustannuslaskelmaversioon. Kahden version mallin avulla voidaan määrittää useita lisäpäivityksiä siten, että jokaisella lisäpäivityksellä on oma erillinen kustannuslaskelmaversionsa, joka sisältää asianmukaiset lisäkustannustietueet.

## <a name="example"></a>Esimerkki

Seuraavassa esimerkissä kuvataan, miten yhden version ja kahden version menettelyitä voi käyttää valmistusympäristön vakiokustannusten päivityksissä. Päivitykset voivat esimerkiksi vastata uusia nimikkeitä tai korjauksia. Oletetaan, että yksi kustannuslaskelmaversio edustaa kuluvan vuoden vakiokustannuksia. Tämän version tunnus on 2020-STD. 2020-STD -versio sisältää kaikkien nimikkeiden nykyiset aktiiviset kustannukset. Lisäksi se sisältää kaikki reititykseen liittyvät kustannusluokat sekä yleiskustannusten laskentakaavat, jotka olivat tiedossa vuoden 2020 alkaessa. 2020-STD on alkuperäinen kustannuslaskelmaversio.

- **Yhden version malli kustannustietojen päivityksessä** − Yhden version malli tarkoittaa, että alkuperäinen kustannuslaskelmaversio 2020-STD sisältää kaikki kustannustietueet. Kustannuspäivitykset kirjataan 2020-STD-versioon ja niiden tilaksi määritetään Odottaa. Odottavat kustannukset voidaan lisätä manuaalisesti uusia ostettuja nimikkeitä varten, tai ne voidaan laskea valmistettua nimikettä varten siten, että korjaukset on otettu huomioon. Yhden version mallissa tuoterakennelaskelmat eivät edellytä varmistustietojen lähdettä, koska kaikki aktiiviset kustannukset sisältyvät kustannuslaskelmaversioon. Kun odottavat kustannukset on aktivoitu, alkuperäinen kustannuslaskelmaversio 2020-STD sisältää jälleen kaikki nykyiset aktiiviset kustannukset.
- **Kahden version malli kustannustietojen päivityksessä** − Kahden version mallissa edellytetään toista kustannuslaskelmaversiota, joka sisältää ainoastaan kustannuspäivitykset. Tämän version tunnus on 2020-STD-CHANGES. Kustannuspäivitykset kirjataan 2020-STD-CHANGES-versioon ja niiden tilaksi määritetään Odottaa. Kun käytössä on kaksi versiota, valmistettujen nimikkeiden odottavien kustannusten tuoterakennelaskelmat vaativat varmistustietojen lähteen. Tämä johtuu siitä, että kustannuslaskelmien lisäversio 2020-STD-CHANGES sisältää vain osan kustannustiedoista. Varmistuksen voi esittää aktiivisna kustannuksina tai kustannuslaskennan versiona 2020-STD, koska molemmissa tunnistetaan kustannustietojen lähde silloin, kun se ei sisälly 2020-STD-CHANGES -versioon. Kun odottavat kustannukset ovat käytössä, kustannuslaskennan versio 2020-STD-CHANGES sisältää nykyiset aktiiviset kustannukset, jotka vastaavat päivityksiä; alkuperäinen kustannuslaskelmaversio 2020-STD ei muutu. Kun käytössä on kahden version malli, alkuperäisen kustannuslaskelmaversion estomenettelyt on määritettävä estämään päivitykset. Samat estomenettelyt tulisi määrittää toiselle kustannuslaskelmaversiolle, lukuun ottamatta valikoitua alkamispäivämäärää ja valikoitua estokäytäntöjä, joilla määritellään sallitut päivitykset. Määritetty alkamispäivämäärä tulisi päivittää jokaisen muutoserän yhteydessä vastaamaan ajoitettua aktivointipäivämäärää.

Tässä esimerkissä käytettiin vielä yhtä kustannuslaskelmaversiota koko vuoden 2020 päivitysten hallintaan. Lisäkustannuslaskelmaversioita voi käyttää useita; esimerkiksi jokaisella päivityserällä voi olla oma, erillinen versionsa. Kun käytössä on useampia kustannuslaskentoja, varmistus on ilmaistava aktiivisina kustannuksina, koska ne jakautuvat useille kustannuslaskentaversioille.

## <a name="financial-dimensions-for-the-standard-cost-revaluation"></a>Vakiokustannusten uudelleenarvostuksen taloushallinnon dimensiot

Uuden vakiohinnan aktivointi arvostaa yleensä uudelleen käytettävissä olevan varaston arvon vakiokustannuksen uudelleenarvostustapahtumien perusteella. Nimikkeen taloushallinnon dimensiot kirjataan yleensä tapahtumiin. Jos kuitenkin haluat hallita taloushallinnon dimensioiden kirjaamista ja kirjaamistapaa, ota *Varaston vakiokustannusten uudelleenarvostuksen taloushallinnon dimensioihin oletusarvoihin palaamisen vaihtoehdot* -toiminto käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Kun tämä toiminto on otettu käyttöön valitse **Kustannusten hallinta > Varaston kirjanpitokäytäntöjen määrittäminen > Parametrit** ja määritä avattavassa **Taloushallinnon dimension alkuperä** luettelossa jokin seuraavista arvoista:

- **Ei mitään** – Taloushallinnon dimensioita ei kirjata uudelleenarvostustapahtumiin. Jos tilirakenteessa sisältää pakollisen taloushallinnon dimension, uudelleenarvostusprosessi suoritetaan siitä huolimatta, mutta se luo kirjanpitomerkinnät, joissa ei ole taloushallinnon dimensioita. Siinä tapauksessa käyttäjät saavat ensin varoitusanoman, jotta he voivat tarvittaessa peruuttaa uudelleenarvostuksen.
- **Taulu** – Taloushallinnon dimensiot kirjataan uudelleenarvotustapahtumiin. Tämä on oletusasetus ja on yhdenmukainen alkuperäisen järjestelmän toiminnan kanssa ilman, että *Varaston vakiokustannusten uudelleenarvostuksen taloushallinnon dimensioihin oletusarvoihin palaamisen vaihtoehdot* -toiminto otetaan käyttöön.
- **Kirjaus** – Uudelleenarvostustapahtumiin kirjataan uudelleenarvostettavana olevan tapahtuman taloushallinnon dimensioita. Alkuperäisen tapahtuman varastotilin taloushallinnon dimensioita käytetään oletusarvoisesti sekä varastotilillä että uudelleenarvostustilillä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]