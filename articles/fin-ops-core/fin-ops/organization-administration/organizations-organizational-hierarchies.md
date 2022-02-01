---
title: Organisaatiot ja organisaatiohierarkiat – yleiskatsaus
description: Organisaatiohierarkiat edustavat liiketoimintasi muodostavien organisaatioiden välisiä suhteita.
author: sericks007
ms.date: 01/03/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMOperatingUnit,
audience: Application User
ms.reviewer: sericks
ms.custom:
- "17291"
- intro-internal
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8e8f2c2004582f42c3f464fedf9f3d049b5278f
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2022
ms.locfileid: "7992078"
---
# <a name="organizations-and-organizational-hierarchies-overview"></a>Organisaatiot ja organisaatiohierarkiat – yleiskatsaus

[!include [banner](../includes/banner.md)]

Organisaatio on joukko ihmisiä, jotka työskentelevät yhdessä liiketoimintaprosessin suorittamiseksi tai tavoitteen saavuttamiseksi. Organisaatiohierarkiat edustavat liiketoimintasi muodostavien organisaatioiden välisiä suhteita.

## <a name="organizations"></a>Organisaatiot

Voit määrittää seuraavan tyyppisiä sisäisiä organisaatioita: yritysten toimintayksiköt ja ryhmiä.

Kaikki sisäiset organisaatiot ovat **Osapuoli**-tyyppisiä yksiköitä. Tämän vuoksi nämä organisaatiot käyttävät osoitekirjaa osoitteen ja yhteystietojen tallentamiseen. Osapuoli, joka voi olla joko henkilö tai organisaatio voi kuulua yhteen tai useampaan osoitekirjaan.

### <a name="legal-entities"></a>Oikeushenkilöt

Yritys on organisaatio, jolla on rekisteröity tai lain vaatima rakenne. Yritys voi solmia oikeudellisia sopimuksia ja yritykseltä edellytetään suorituskykyä kuvaavien lausuntojen valmistelemista.

Yritys on tietyntyyppinen oikeushenkilö Tällä hetkellä yritykset ovat ainoita luotavia oikeushenkilöitä ja jokainen oikeushenkilö on liitetty yritystunnukseen. Tämä liitos on olemassa, koska ohjelman eräät toiminnalliset alueet käyttävät yritystunnusta tai DataAreaId-tunnusta tietomalleissaan. Näillä toiminnallisilla alueilla yrityksiä käytetään tietoturvan rajana. Käyttäjillä on pääsy vain sen yrityksen tietoihin, jonka järjestelmään he ovat sillä hetkellä kirjautuneena.

### <a name="operating-units"></a>Käyttöyksiköt

Toimintayksikkö on organisaatio, jota käytetään jakamaan liiketoiminnan taloudellisten resurssien hallinta ja operationaaliset prosessit. Toimintayksikön henkilöiden vastuulla on rajattujen resurssien maksimointi, prosessien tehostaminen ja suorituskyvyn raportointi.

Toimintayksiköihin kuuluvat kustannuspaikat, liiketoimintayksiköt, arvovirrat, osastot ja kauppakanavat. Seuraavassa taulukossa on lisätietoja jokaisesta toimintayksikön tyypistä:

| Toimintayksikön tyyppi | Kuvaus | Tarkoitus |
|---------------------|-------------|---------|
| Kustannuspaikka         | Toimintayksikkö, jossa esimiehet vastaavat budjetoiduista ja toteutuneista menoista. | Käytetään liiketoimintaprosessien hallintaan ja operatiiviseen ohjaukseen kaikissa yrityksissä. |
| Liiketoimintayksikkö       | Osittain itsenäinen toimintayksikkö, joka luodaan vastaamaan yrityksen strategisiin tavoitteisiin. | Käytetään taloushallinnan raportointiin, joka perustuu toimialoihin tai tuotelinjoihin, joita organisaatio palvelee yrityksistä itsenäisenä. |
| Arvovirta        | Toimintayksikkö, joka hallitsee yhtä tai useaa tuotantovirtaa. | Yleensä käytetään lean-valmistuksessa ohjaamaan toimintoja ja työnkulkuja, joita tarvitaan tuotteen tai palvelun tuottamiseksi kuluttajille. |
| Osasto          | Toimintayksikkö, joka edustaa organisaation luokkaa tai toiminnallista osaa, joka suorittaa tietyn tehtävän (kuten myynti tai kirjanpito). | Käytetään toiminnallisia alueita koskevaan raportointiin. Osastolla voi olla tulos- ja tappiovastuu, ja se voi koostua ryhmästä kustannuspaikkoja. |
| Vähittäismyyntikanava      | Toimintayksikkö, joka edustaa kivijalkaliikettä, verkkokauppaa tai puhelinkeskusta. | Käytetään yhden tai useamman myymälän liiketoimintaprosessien hallintaan ja operatiiviseen ohjaukseen yritysten sisällä tai niiden läpi. |

### <a name="teams"></a>Ryhmät

Ryhmä on organisaatio, jonka jäsenet jakavat yhteisen vastuun, intressin tai tavoitteen. Ryhmiä ei voi käyttää organisaatiohierarkioissa.

## <a name="organizational-hierarchies"></a>Organisaatiohierarkiat

Määritä organisaatiohierarkioita liiketoiminnan tarkastelemiseen ja raportointiin eri näkökulmista. Voit esimerkiksi määrittää yritysten hierarkian verotuksellista, oikeudellista tai lakisääteistä raportointia varten. Aseta hierarkia, joka perustuu toimintayksiköihin, raportoimaan sellaiset taloustiedot, joiden raportointia lainsäädäntö ei edellytä mutta joita käytetään sisäisessä valvonnassa. Voit esimerkiksi luoda ostohierarkian ostokäytäntöjen, sääntöjen ja liiketoimintaprosessien hallintaan.

> [!NOTE]
> Kun toimintayksikkö on lisätty hierarkiaan, toimintayksikköä ei voi poistaa. 

Jokaiseen hierarkiaan liitetään tarkoitus. Hierarkian tarkoitus määrittää hierarkiaan sisällytettävät organisaatiotyypit. Tarkoitus määrittää myös käyttötilanteet, joissa hierarkiaa voidaan käyttää.

Hierarkian organisaatiot voivat jakaa parametrejä, käytäntöjä ja tapahtumia. Organisaatio voi periä tai ohittaa ylätason organisaation parametrit. Jaetut perustiedot, kuten tuotteet ja osoitekirja, koskevat koko organisaatiota, mutta niitä ei voi ohittaa yksittäisissä organisaatioissa. Organisaatioiden ja hierarkioiden luominen edellyttää huolellista suunnittelua. Lisätietoja on kohdassa [Organisaatiohierarkian suunnitteleminen](plan-organizational-hierarchy.md).

## <a name="additional-resources"></a>Lisäresurssit
- [Organisaatiohierarkian suunnitteleminen](plan-organizational-hierarchy.md)
- [Organisaation hierarkian luominen](tasks/create-organization-hierarchy.md)
- [Yrityksen luominen](tasks/create-legal-entity.md)
- [Toimintayksikön luominen](tasks/create-operating-unit.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
