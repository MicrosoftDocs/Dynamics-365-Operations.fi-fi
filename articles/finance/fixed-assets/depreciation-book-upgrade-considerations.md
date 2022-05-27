---
title: Poistokirjojen päivityksen yleiskatsaus
description: Tässä aiheessa kuvataan nykyiset käyttöomaisuuden kirjatoiminto. Tämä toiminto perustuu arvomallitoimintoon, joka oli käytettävissä aiemmissa versioissa, mutta se sisältää myös kaikki aiemmin pelkästään poistokirjoihin sisältyneet toiminnot.
author: moaamer
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom:
- "221624"
- intro-internal
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: moaamer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b43c499928988e98cae63b85f528b8a71e042cc7
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713639"
---
# <a name="depreciation-book-upgrade-overview"></a>Poistokirjojen päivityksen yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan nykyiset käyttöomaisuuden kirjatoiminto. Tämä toiminto perustuu arvomallitoimintoon, joka oli käytettävissä aiemmissa versioissa, mutta se sisältää myös kaikki aiemmin pelkästään poistokirjoihin sisältyneet toiminnot. Arvomallin toiminnot ja poistokirjatoiminnot on yhdistetty yhdeksi käsitteeksi, jota kutsutaan kirjaksi. Kirjatoiminnon avulla voit käyttää yksittäistä sivujen, kyselyjen ja raporttien sarjaa kaikkiin organisaation käyttöomaisuusprosesseihin. Tämä aihe sisältää joitakin asioita, jotka on otettava huomioon ennen päivittämistä. 

Päivitysprosessi siirtää aiemmin määritetyt asetukset ja kaikki olemassa olevat tapahtumat uuden kirjan rakenteeseen. Arvomallit säilyvät nykyisellään, kirjana joka tekee kirjauksia kirjanpitoon. Poistokirjat siirretään kirjaan, jonka Kirjaa kirjanpitoon -asetus on Ei. Poistokirjan kirjauskansioiden nimet siirretään kirjanpidon kirjauskansion nimeen, jonka kirjanpitotasoksi on määritetty Ei mitään. Poistokirjatapahtumat siirretään käyttöomaisuustapahtumiin.

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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
