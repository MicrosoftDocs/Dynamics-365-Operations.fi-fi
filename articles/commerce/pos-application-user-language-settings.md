---
title: Myyntipistesovellus (POS) ja käyttäjän kielialueasetukset
description: Tässä ohjeaiheessa kuvataan, miten kieliasetukset muutetaan Modern POS:ssa (MPOS) ja Cloud POS:ssa.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0c5087ee04030a76aef774871b88b7970391723c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804378"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a>Myyntipistesovellus (POS) ja käyttäjän kielialueasetukset

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kuvataan, miten kieliasetukset muutetaan Modern POS:ssa (MPOS) ja Cloud POS:ssa.

## <a name="overview"></a>Yleiskatsaus
Modern POS (MPOS) ja Cloud POS tukevat ympäristöjä, joissa kielisetukset ja käännökset voivat vaihdella myymälän ja käyttäjäasetusten mukaan. Esimerkiksi myymälä saattaa sijaita alueella, jossa englannin kieli on asiakkaiden yleisimmin käyttämä, mutta jotkut työntekijät käyttävät mieluummin sovellusta ranskankielisillä käännöksillä.

## <a name="data-language"></a>Tietojen kieli

Käyttäjän asetuksista riippumatta, MPOS ja Cloud POS käyttävät aina myymälän kieliasetuksia tietojen käännöksen määrittämiseen. Näin voidaan varmistaa, että kaikilla käyttäjillä ja asiakkailla on yhtenevä kokemus. Esimerkkejä tiedoista ovat:

- Tuotteet
- Määritteet ja arvot
- Luokkien nimet
- Tulostetut tai sähköpostitse toimitetut tapahtumien kuitit
- Maksutapojen nimet
- Riveillä näytettävät sanomat

Myymälän kieltä käytetään myös myyntipisteen pääkirjautumissivulla, koska käyttäjää ei tunneta ennen kirjautumista. Jos myymälän kielellä olevaa käännöstä ei ole saatavilla, myyntipiste palaa yrityksen kieleen.

### <a name="configuring-the-stores-language-setting"></a>Myymälän kieliasetusten määrittäminen

Myymälän kieliasetukset määritetään **Kaikki myymälät** -kohdassa **Myymälä**-sivulla valitsemalla **Yleinen &gt; Alueasetukset &gt; Kieli**. Valitse kunkin myymälän kieli avattavasta luettelosta.

## <a name="user-interface-language"></a>Käyttöliittymän kieli

Myyntipisteen käyttäjän kieliasetukset määrittävät sovelluksen käyttöliittymässä käytettävät käännökset. Tähän sisältyvät kaikki otsikot, valikot ja luettelot, joita ei pidetä tietoina. Yksi poikkeus tähän on teksti, joka näytetään myyntipisteen painikeruudukoissa. Ne eivät tue käännöksiä, joten ne näyttävät aina tekstin siten, kuin se on määritetty painikkeessa. Jos haluat, että ne tukevat käännettyjä painikkeita, sinun on kopioitava erilliset painikeruudukot ja ylläpidettävä niitä, ja määritettävä ne soveltuville käyttäjille.

### <a name="configuring-the-users-language-setting"></a>Käyttäjän kieliasetusten määrittäminen

Myyntipisteen kieliasetukset määritetään kohdassa **Työntekijä**-sivun **Kaikki työntekijät** -kohdassa valitsemalla **Retail ja Commerce &gt; Kieli**. Sitä ei määritetä profiilin päävälilehdellä. Myyntipiste ei käytä tätä asetusta. Jos käyttäjän kieltä ei määritetä tai jos se on määritetty kielelle, jolla ei ole saatavilla käännöksiä, myyntipiste palaa myymälän kieleen.

|             | Käyttöliittymän kieli                   | Tietojen kieli (tuotteet, kuittimuodot, rivinäyttö, jne.) |
|-------------|----------------------------|---------------------------------------------------------------|
| **Yritys** | Oletusarvo                    | Oletusarvo                                                       |
| **Myymälä**   | Ohittaa yrityksen          | Ohittaa yrityksen                                             |
| **Käyttäjä**    | Ohittaa myymälän tai yrityksen | En koskaan                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]