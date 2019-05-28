---
title: Poistokirjan päivityksen yleiskatsaus
description: 'Aiemmissa julkaisuversioissa oli kaksi käyttöomaisuuserien arviointikäsitettä: arvomallit ja poistokirjat. Microsoft Dynamics 365 for Operationsissa (1611) arvomallin toiminnot ja poistokirjatoiminnot on yhdistetty yhdeksi käsitteeksi, jota kutsutaan kirjaksi. Tämä aihe käsittelee päivityksessä huomioitavia seikkoja.'
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 805f6ab1cd1d0996e685278cc997f532213c76c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546452"
---
# <a name="depreciation-book-upgrade-overview"></a>Poistokirjan päivityksen yleiskatsaus

[!include [banner](../includes/banner.md)]

Aiemmissa julkaisuversioissa oli kaksi käyttöomaisuuserien arviointikäsitettä: arvomallit ja poistokirjat. Microsoft Dynamics 365 for Operationsissa (1611) arvomallin toiminnot ja poistokirjatoiminnot on yhdistetty yhdeksi käsitteeksi, jota kutsutaan kirjaksi. Tämä aihe käsittelee päivityksessä huomioitavia seikkoja. 

Päivitysprosessi siirtää aiemmin määritetyt asetukset ja kaikki olemassa olevat tapahtumat uuden kirjan rakenteeseen. Arvomallit säilyvät nykyisellään, kirjana joka tekee kirjauksia kirjanpitoon. Poistokirjat siirretään kirjaan, jonka **Kirjaa kirjanpitoon** -asetus on **Ei**. Poistokirjan kirjauskansioiden nimet siirretään kirjanpidon kirjauskansion nimeen, jonka kirjanpitotasoksi on määritetty **Ei mitään**. Poistokirjatapahtumat siirretään käyttöomaisuustapahtumiin. 

Ennen tietojen päivityksen suorittamista sinun on hyvä ymmärtää käytettävissä olevat kaksi vaihtoehtoa poistokirjan kirjauskansion rivien päivittämiseksi tapahtumatositteisiin, ja numerosarja, jota käytetään tositesarjaan. 

Vaihtoehto 1: **Järjestelmän määrittämä numerosarjan**: tämä on oletusasetus päivityksen suorituskyvyn parantamiseksi. Päivitys ei käytä numerosarjojen kehystä, mutta sen sijaan kohdistaa tositteet joukkoon perustuvan mallin pohjalta. Päivityksen jälkeen uusi numerosarjan luodaan **Seuraava numerosarja** asianmukaisesti päivitettyjen tapahtumien perusteella. Oletuksena käytettävä numerosarjan muoto on FADBUpgr\#\#\#\#\#\#\#\#\#. Voit muuttaa muotoa muutamien parametrien avulla käyttäen tätä menetelmää:

-   **Numerosarjan koodi**: koodi numerosarjan tunnistamiseen. Tätä numerosarjan koodia ei ole olemassa, sillä koodi luodaan päivityksen jälkeen.
    -   Vakion nimi: **NumberSequenceDefaultCode**
    -   Oletusarvo: "FADBUpgr"
-   **Etuliite**: kiinteä merkkijonon arvo, jota käytetään etuliitteenä tositenumeroissa.
    -   Vakion nimi: **NumberSequenceDefaultParameterPrefix**
    -   Oletusarvo: "FADBUpgr"
-   **Aakkosnumeerinen pituus**: aakkosnumeerisen segmentin numerosarjan pituus.
    -   Vakion nimi: **NumberSequenceDefaultParameterAlpanumericLength**
    -   Oletusarvo: 9
-   **Ensimmäinen numero**: numerosarjan ensimmäinen numero.
    -   Vakion nimi: **NumberSequenceDefaultParameterStartNumber**
    -   Oletusarvo: 1

Vaihtoehto 2: **Aiemmin käyttäjän luoma numerosarja**: tämän vaihtoehdon avulla voit määrittää päivitystä varten käytettävän numerosarjan. Tämä vaihtoehto kannattaa, jos tarvitaan edistynyttä numerosarjan konfigurointia. Numerosarjan käyttöä varten on muokattava päivitysluokkaa ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans seuraavilla tiedoilla:

-   **Numerosarjan koodi**: Numerosarjan koodi.
    -   Vakion nimi: **NumberSequenceExistingCode**
    -   Oletusarvo: Ei oletusarvoa, tämä on päivitettävä numerosarjan koodiksi.
-   **Jaettu numerosarja**: totuusarvo, jolla tunnistetaan numerosarjan vaikutusalue. Käytä jaetun numerosarjan arvoa "tosi" kaikissa yrityksissä ja arvoa "false" yrityskohtaisella alueella. Käytettäessä "false"-arvoa samanniminen numerosarja on oltava kaikissa yrityksissä, joissa on poistokirjatapahtumia. Jaettuja numerosarjoja on jokaisessa osiossa, joka sisältää poistokirjatapahtumia.
    -   Vakion nimi: **NumberSequenceExistingIsShared**
    -   Oletusarvo: tosi

Parametrit ovat ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans -luokan alussa. 

*// Tositteiden kohdistuksen ensisijaisen menetelmän määrittäminen* 
 *// tosi, jos haluat käyttää aiemmin luotua numerosarjan koodia* 
 *// epätosi, jos aiot käyttää järjestelmän määrittämää numerosarjaa (oletus)* const boolean NumberSequenceUseExistingCode = false;  

*// Jos käytetään järjestelmän määrittämää numerosarjaa, määritä numerosarjan parametrit.*
 *// Näillä parametreilla luodaan uusi numerosarja.* const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*// Jos käytetään aiemmin luotua numerosarjaa, anna nykyinen numerosarjan koodi* 
 *// Tositteen kohdistus siirtyy riveittäin käyttämään aiemmin luotua numerosarjaa.* const str NumberSequenceExistingCode = ''; *// Määritä aiemmin luodun numerosarjan koodin vaikutusalue* 
 *// tosi, jos annettu numerosarja on jaettu* 
 *// epätosi, jos annettu numerosarja on yrityskohtainen* 
 *// Järjestelmän määrittämää oletusnumerosarjaa käytetään, jos määritetyllä alueella olevaa numerosarjaa ei löydy.* const boolean NumberSequenceExistingIsShared = true; 

Muodosta uudelleen projekti, joka sisältää luokan vakioiden muuttamisen jälkeen. 

Käytettäessä järjestelmän luomaa numerosarjaa (vaihtoehto 1) päivitys käyttää joukkoon perustuvaa käsittelyä kohdistaessaan tositenumerot päivityskomentosarjan parametrien mukaisesti. Se luo myös uuden numerosarjan määritetyillä parametreilla kohdistuksen jälkeen. 

Käytettäessä käyttäjän määrittämää numerosarjaa (vaihtoehto 2) tietopäivitys tarkistaa, esiintyykö määritetyllä alueella vaikuttava numerosarja jokaisen osion tietokannassa ja yrityksessä, jolla on poistokirjatapahtumia. Jos se esiintyy, päivitys kohdistaa tositenumerot riveittäin numerosarjan määrittämällä tavalla käyttäen numerosarjan kehystä. Jos numerosarjaa ei ole olemassa määritetyllä alueella, päivitys käyttää oletusarvona olevaa järjestelmän määrittämää numerosarjaa tositenumeroiden kohdistamiseen ja luo uuden numerosarjan määritetyillä oletusparametreilla kohdistuksen jälkeen.

Kummassakin menetelmässä tietojen päivityskomentosarja käyttää myös numerosarjaa **Tositesarja**-kentässä uusissa kirjauskansion nimissä, jotka luotiin vanhan poistokirjan kirjauskansion nimiä varten.



