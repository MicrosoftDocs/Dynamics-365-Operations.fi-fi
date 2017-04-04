---
title: "Myyntipistesovellus ja käyttäjän kieli- ja alueasetukset"
description: "Tässä ohjeaiheessa kuvataan muuttaa Retail Moderni POS (MPOS) ja Cloud POS kieliasetukset."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf5b75572529bb497d3079752de187f30aa59294
ms.lasthandoff: 03/31/2017


---

# <a name="pos-application-and-user-language-settings"></a>Myyntipistesovellus ja käyttäjän kieli- ja alueasetukset

Tässä ohjeaiheessa kuvataan muuttaa Retail Moderni POS (MPOS) ja Cloud POS kieliasetukset.

<a name="overview"></a>Yleiskuvaus
========

Vähittäismyynnin Moderni POS (MPOS) ja Cloud POS tukevat ympäristöjä, joissa kieli ja käännökset voi vaihdella myymälä- ja käyttäjäkäytäntöjä. Esimerkiksi myymälän löytynyt alue, jossa englanti on yleisin asiakkaitaan varten, mutta joidenkin työntekijöiden mieluummin käyttää sovelluksen kanssa Ranskan käännökset.

## <a name="data-language"></a>Tietojen kieli
Riippumatta käyttäjän asetukset MPOS ja Cloud POS käyttää aina myymälän kieliasetusten määrittämiseen käytettävä tietojen käännökset. Näin varmistetaan, että kaikki käyttäjät ja asiakkaat on yhtenäinen kokemus.  Tietoja ovat esimerkiksi:

-   Tuotteet
-   Määritteet ja arvot
-   Luokkien nimet
-   Tulostetut tai sähköpostitse toimitetut tapahtumien kuitit
-   Maksutapojen nimet
-   Riveillä näytettävät sanomat

Tärkeimmät POS-kirjautumisnäyttö myös käyttää myymälän kieli, koska käyttäjä ei ole tiedossa, ennen kuin kirjaudut. Jos käännöstä ei ole käytettävissä myymälän kielen, Myyntipiste takaisin yrityksen kieli.

### <a name="configuring-the-stores-language-setting"></a>Myymälän kieliasetusten määrittäminen

Myymälän kieleksi on määritetty **kaikki liikkeistä** - **Retail Store** kohdassa sivulla ** yleinen &gt;Aluekohtaiset asetukset &gt;kieli. ** Avulla pudota alas valita kielen kullekin myymälälle.

## <a name="user-interface-language"></a>Käyttöliittymän kieli
POS-käyttäjän kieliasetus määrittää käytetyn sovelluksen käyttöliittymän käännöksiä. Tämä sisältää kaikki otsikot, valikot ja luettelot, joita ei pidetä tietojen. Ainoa poikkeus on teksti, joka näytetään POS painikeruudukot. Painikeruudukkoja eivät tue käännökset, joten ne näkyy aina teksti-painikkeella määritellyllä tavalla. Tukemiseksi käännetty painikkeita täytyy kopioida ja ylläpitää erillistä painikeruudukot ja määritellä tarvittaessa käyttäjät.

### <a name="configuring-the-users-language-setting"></a>Käyttäjän kieliasetusten määrittäminen

POS-käyttäjän kieleksi on määritetty **kaikille työntekijöille** - **työntekijän** sivulla kohdassa **Retail &gt;kielen**.  Sitä ei ole määritetty ensisijainen profiili-välilehti.  Tätä asetusta ei käytetä Myyntipisteen mukaan. Jos käyttäjän kieltä ei määritetä tai jos se on määritetty kielelle, jolla ei ole saatavilla käännöksiä, myyntipiste palaa myymälän kieleen.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **Käyttöliittymäkielen** ** **      | **Tietojen kieli (tuotteet, kuittimuodot, rivinäyttö, jne.)** |
| **Yritys** | Oletusarvo                    | Oletusarvo                                                           |
| **Myymälä**   | Ohittaa yrityksen          | Ohittaa yrityksen                                                 |
| **User**    | Ohittaa myymälän tai yrityksen | En koskaan                                                             |




