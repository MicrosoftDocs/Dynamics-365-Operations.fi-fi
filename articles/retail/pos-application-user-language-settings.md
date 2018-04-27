---
title: "Myyntipistesovellus ja käyttäjän kieli- ja alueasetukset"
description: "Tässä ohjeaiheessa kuvataan, miten kieliasetukset muutetaan Retail Modern -myyntipisteessä (MPOS) ja pilvimyyntipisteessä."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: dacc072ab5c070010d86302fa08a3066125b23a6
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="pos-application-and-user-language-settings"></a>Myyntipistesovellus ja käyttäjän kieli- ja alueasetukset

[!INCLUDE [banner](includes/banner.md)]

Tässä ohjeaiheessa kuvataan, miten kieliasetukset muutetaan Retail Modern -myyntipisteessä (MPOS) ja pilvimyyntipisteessä.

## <a name="overview"></a>Yleiskuvaus
Retail Modern -myyntipiste (MPOS) ja pilvimyyntipiste tukevat ympäristöjä, joissa kielisetukset ja käännökset voivat vaihdella myymälän ja käyttäjäasetusten mukaan. Esimerkiksi myymälä saattaa sijaita alueella, jossa englannin kieli on asiakkaiden yleisimmin käyttämä, mutta jotkut työntekijät käyttävät mieluummin sovellusta ranskankielisillä käännöksillä.

## <a name="data-language"></a>Tietojen kieli
Käyttäjän asetuksista riippumatta, Retail Modern -myyntipiste ja pilvimyyntipiste käyttävät aina myymälän kieliasetuksia tietojen käännöksen määrittämiseen. Näin voidaan varmistaa, että kaikilla käyttäjillä ja asiakkailla on yhtenevä kokemus.  Esimerkkejä tiedoista ovat:

-   Tuotteet
-   Määritteet ja arvot
-   Luokkien nimet
-   Tulostetut tai sähköpostitse toimitetut tapahtumien kuitit
-   Maksutapojen nimet
-   Riveillä näytettävät sanomat

Myymälän kieltä käytetään myös myyntipisteen pääkirjautumissivulla, koska käyttäjää ei tunneta ennen kirjautumista. Jos myymälän kielellä olevaa käännöstä ei ole saatavilla, myyntipiste palaa yrityksen kieleen.

### <a name="configuring-the-stores-language-setting"></a>Myymälän kieliasetusten määrittäminen

Myymälän kieliasetukset määritetään **Kaikki vähittäismyymälät**-kohdassa **Vähittäismyymälä**-sivulla kohdassa Yleinen &gt; Alueasetukset &gt; Kieli. **Valitse kunkin myymälän kieli avattavasta luettelosta.

## <a name="user-interface-language"></a>Käyttöliittymän kieli
Myyntipisteen käyttäjän kieliasetukset määrittävät sovelluksen käyttöliittymässä käytettävät käännökset. Tähän sisältyvät kaikki otsikot, valikot ja luettelot, joita ei pidetä tietoina. Yksi poikkeus tähän on teksti, joka näytetään myyntipisteen painikeruudukoissa. Ne eivät tue käännöksiä, joten ne näyttävät aina tekstin siten, kuin se on määritetty painikkeessa. Jos haluat, että ne tukevat käännettyjä painikkeita, sinun on kopioitava erilliset painikeruudukot ja ylläpidettävä niitä, ja määritettävä ne soveltuville käyttäjille.

### <a name="configuring-the-users-language-setting"></a>Käyttäjän kieliasetusten määrittäminen

Myyntipisteen kieliasetukset määritetään kohdassa **Kaikki työntekijät** **Työntekijä**-sivulla kohdassa **Vähittäismyynti &gt; Kieli**.  Sitä ei määritetä Profiilin päävälilehdellä. Myyntipiste ei käytä tätä asetusta. Jos käyttäjän kieltä ei määritetä tai jos se on määritetty kielelle, jolla ei ole saatavilla käännöksiä, myyntipiste palaa myymälän kieleen.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **Käyttöliittymän kieli**      | **Tietojen kieli (tuotteet, kuittimuodot, rivinäyttö, jne.)** |
| **Yritys** | Oletusarvo                    | Oletusarvo                                                           |
| **Myymälä**   | Ohittaa yrityksen          | Ohittaa yrityksen                                                 |
| **Käyttäjä**    | Ohittaa myymälän tai yrityksen | En koskaan                                                             |






