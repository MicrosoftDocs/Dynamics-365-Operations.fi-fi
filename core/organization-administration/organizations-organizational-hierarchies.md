---
title: Organisaatiot ja organisaatiohierarkiat
description: "Organisaatio on joukko ihmisiä, jotka työskentelevät yhdessä liiketoimintaprosessin suorittamiseksi tai tavoitteen saavuttamiseksi. Organisaatiohierarkiat edustavat liiketoimintasi muodostavien organisaatioiden välisiä suhteita."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17291
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 4a7e1253d83e9212d423868a1f841b6944b07ad7
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="organizations-and-organizational-hierarchies"></a>Organisaatiot ja organisaatiohierarkiat

[!include[banner](../includes/banner.md)]


Organisaatio on joukko ihmisiä, jotka työskentelevät yhdessä liiketoimintaprosessin suorittamiseksi tai tavoitteen saavuttamiseksi. Organisaatiohierarkiat edustavat liiketoimintasi muodostavien organisaatioiden välisiä suhteita.

<a name="organizations"></a>Organisaatiot
-------------

Microsoft Dynamics 365 for Finance and Operationsissa voi määrittää seuraavantyyppisiä sisäisiä organisaatioita: yrityksiä, toimintayksiköitä ja ryhmiä.

Kaikki sisäiset organisaatiot ovat **Osapuoli**-tyyppisiä yksiköitä. Tämän vuoksi nämä organisaatiot käyttävät osoitekirjaa osoitteen ja yhteystietojen tallentamiseen. Osapuoli, joka voi olla joko henkilö tai organisaatio voi kuulua yhteen tai useampaan osoitekirjaan.
### <a name="legal-entities"></a>Oikeushenkilöt

Yritys on organisaatio, jolla on rekisteröity tai lain vaatima rakenne. Yritys voi solmia oikeudellisia sopimuksia ja yritykseltä edellytetään suorituskykyä kuvaavien lausuntojen valmistelemista. Yritys on tietyntyyppinen oikeushenkilö Tässä Microsoft Dynamics 365 for Finance and Operationsin versiossa yritykset ovat ainoita luotavia oikeushenkilöitä ja jokaisella oikeushenkilöllä on yritystunnus. Tämä liitos on olemassa, koska ohjelman eräät toiminnalliset alueet käyttävät yritystunnusta tai DataAreaId-tunnusta tietomalleissaan. Näillä toiminnallisilla alueilla yrityksiä käytetään tietoturvan rajana. Käyttäjillä on pääsy vain sen yrityksen tietoihin, jonka järjestelmään he ovat sillä hetkellä kirjautuneena.

### <a name="operating-units"></a>Käyttöyksiköt

Toimintayksikkö on organisaatio, jota käytetään jakamaan liiketoiminnan taloudellisten resurssien hallinta ja operationaaliset prosessit. Toimintayksikön henkilöiden vastuulla on rajattujen resurssien maksimointi, prosessien tehostaminen ja suorituskyvyn raportointi. Microsoft Dynamics 365 for Finance and Operationsin toimintayksikkötyyppejä ovat kustannuspaikat, liiketoimintayksiköt, arvovirrat, osastot ja vähittäismyyntikanavat. Seuraavassa taulukossa on lisätietoja jokaisesta toimintayksikön tyypistä:
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

Määritä organisaatiohierarkioita liiketoiminnan tarkastelemiseen ja raportointiin eri näkökulmista. Voit esimerkiksi määrittää yritysten hierarkian verotuksellista, oikeudellista tai lakisääteistä raportointia varten. Aseta hierarkia, joka perustuu toimintayksiköihin, raportoimaan sellaiset taloustiedot, joiden raportointia lainsäädäntö ei edellytä mutta joita käytetään sisäisessä valvonnassa. Voit esimerkiksi luoda ostohierarkian ostokäytäntöjen, sääntöjen ja liiketoimintaprosessien hallintaan. Microsoft Dynamics 365 for Finance and Operationsissa jokaiseen hierarkiaan liitetään tarkoitus. Hierarkian tarkoitus määrittää hierarkiaan sisällytettävät organisaatiotyypit. Tarkoitus määrittää myös käyttötilanteet, joissa hierarkiaa voidaan käyttää. Hierarkian organisaatiot voivat jakaa parametrejä, käytäntöjä ja tapahtumia. Organisaatio voi periä tai ohittaa ylätason organisaation parametrit. Jaetut perustiedot, kuten tuotteet ja osoitekirja, koskevat koko organisaatiota, mutta niitä ei voi ohittaa yksittäisissä organisaatioissa. Organisaatioiden ja hierarkioiden luominen edellyttää huolellista suunnittelua. Lisätietoja on aiheessa [Suunnittele organisaatiohierarkia](plan-organizational-hierarchy.md).






