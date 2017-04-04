---
title: Organisaatiot ja organisaatiohierarkiat
description: "Organisaatio on joukko ihmisiä, jotka työskentelevät yhdessä liiketoimintaprosessin suorittamiseksi tai tavoitteen saavuttamiseksi. Organisaatiohierarkiat edustavat liiketoimintasi muodostavien organisaatioiden välisiä suhteita."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17291
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5dc866e2d366138d2fd9d0f9c41cb66892051f3c
ms.lasthandoff: 03/31/2017


---

# <a name="organizations-and-organizational-hierarchies"></a>Organisaatiot ja organisaatiohierarkiat

Organisaatio on joukko ihmisiä, jotka työskentelevät yhdessä liiketoimintaprosessin suorittamiseksi tai tavoitteen saavuttamiseksi. Organisaatiohierarkiat edustavat liiketoimintasi muodostavien organisaatioiden välisiä suhteita.

<a name="organizations"></a>Organisaatiot
-------------

Microsoft Dynamics-365 toimintoja varten, voit määrittää seuraavanlaisia sisäiset organisaatiot: oikeussubjektien liiketoiminnan yksiköiden ja tiimien.

Kaikki sisäiset organisaatiot ovat **Osapuoli**-tyyppisiä yksiköitä. Tämän vuoksi nämä organisaatiot käyttävät osoitekirjaa osoitteen ja yhteystietojen tallentamiseen. Osapuoli, joka voi olla joko henkilö tai organisaatio voi kuulua yhteen tai useampaan osoitekirjaan.
### <a name="legal-entities"></a>Oikeushenkilöt

Yritys on organisaatio, jolla on rekisteröity tai lain vaatima rakenne. Yritys voi solmia oikeudellisia sopimuksia ja yritykseltä edellytetään suorituskykyä kuvaavien lausuntojen valmistelemista. Yritys on tietyntyyppinen oikeushenkilö Yritykset ovat vain tällaisen oikeushenkilön, jonka voit luoda tässä versiossa Microsoft Dynamics-365 operaatioille ja oikeushenkilö, joka on liitetty yrityksen tunnus Tämä liitos on olemassa, koska ohjelman eräät toiminnalliset alueet käyttävät yritystunnusta tai DataAreaId-tunnusta tietomalleissaan. Näillä toiminnallisilla alueilla yrityksiä käytetään tietoturvan rajana. Käyttäjillä on pääsy vain sen yrityksen tietoihin, jonka järjestelmään he ovat sillä hetkellä kirjautuneena.

### <a name="operating-units"></a>Käyttöyksiköt

Toimintayksikkö on organisaatio, jota käytetään jakamaan liiketoiminnan taloudellisten resurssien hallinta ja operationaaliset prosessit. Toimintayksikön henkilöiden vastuulla on rajattujen resurssien maksimointi, prosessien tehostaminen ja suorituskyvyn raportointi. Microsoft Dynamics-365 operaatioille tyypit toimintayksiköt ovat kustannuspaikkojen, liiketoimintayksiköiden, arvovirrat, osastot ja vähittäiskaupan kanavia. Seuraavassa taulukossa on lisätietoja jokaisesta toimintayksikön tyypistä:
| Toimintayksikön tyyppi | Kuvaus                                                                                                                                    | Tarkoitus                                                                                                                                 |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Kustannuspaikka         | Toimintayksikkö, jossa esimiehet vastaavat budjetoiduista ja toteutuneista menoista.                                                      | Käytetään liiketoimintaprosessien hallintaan ja operatiiviseen ohjaukseen kaikissa yrityksissä.                                         |
| Liiketoimintayksikkö       | Osittain itsenäinen toimintayksikkö, joka luodaan vastaamaan yrityksen strategisiin tavoitteisiin.                                                        | Käytetään taloushallinnan raportointiin, joka perustuu toimialoihin tai tuotelinjoihin, joita organisaatio palvelee yrityksistä itsenäisenä. |
| Arvovirta        | Toimintayksikkö, joka hallitsee yhtä tai useaa tuotantovirtaa.                                                                                  | Yleensä käytetään lean-valmistuksessa ohjaamaan toimintoja ja työnkulkuja, joita tarvitaan tuotteen tai palvelun tuottamiseksi kuluttajille.  |
| Osasto          | Toimintayksikkö, joka edustaa organisaation luokkaa tai toiminnallista osaa, joka suorittaa tietyn tehtävän (kuten myynti tai kirjanpito). | Käytetään toiminnallisia alueita koskevaan raportointiin. Osastolla voi olla tulos- ja tappiovastuu, ja se voi koostua ryhmästä kustannuspaikkoja.   |
| Vähittäismyyntikanava      | Toimintayksikkö, joka edustaa kivijalkaliikettä, verkkokauppaa tai online-kauppapaikkaa.                                          | Käytetään yhden tai useamman myymälän liiketoimintaprosessien hallintaan ja operatiiviseen ohjaukseen yritysten sisällä tai niiden läpi.                                  |

### <a name="teams"></a>Ryhmät

Ryhmä on organisaatio, jonka jäsenet jakavat yhteisen vastuun, intressin tai tavoitteen. Ryhmiä ei voi käyttää organisaatiohierarkioissa.
Organisaatiohierarkiat
--------------------------

Määritä organisaatiohierarkioita liiketoiminnan tarkastelemiseen ja raportointiin eri näkökulmista. Voit esimerkiksi määrittää yritysten hierarkian verotuksellista, oikeudellista tai lakisääteistä raportointia varten. Aseta hierarkia, joka perustuu toimintayksiköihin, raportoimaan sellaiset taloustiedot, joiden raportointia lainsäädäntö ei edellytä mutta joita käytetään sisäisessä valvonnassa. Voit esimerkiksi luoda ostohierarkian ostokäytäntöjen, sääntöjen ja liiketoimintaprosessien hallintaan. Jokaisella hierarkialla on varattu tarkoitukseen-operaatioille Microsoft Dynamics-365. Hierarkian tarkoitus määrittää hierarkiaan sisällytettävät organisaatiotyypit. Tarkoitus määrittää myös käyttötilanteet, joissa hierarkiaa voidaan käyttää. Hierarkian organisaatiot voivat jakaa parametrejä, käytäntöjä ja tapahtumia. Organisaatio voi periä tai ohittaa ylätason organisaation parametrit. Jaetut perustiedot, kuten tuotteet ja osoitekirja, koskevat koko organisaatiota, mutta niitä ei voi ohittaa yksittäisissä organisaatioissa. Organisaatioiden ja hierarkioiden luominen edellyttää huolellista suunnittelua. Lisätietoja on aiheessa [Suunnittele organisaatiohierarkia](plan-organizational-hierarchy.md).




