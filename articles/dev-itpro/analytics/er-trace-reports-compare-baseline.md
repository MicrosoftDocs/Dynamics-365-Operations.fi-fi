---
title: Seuraa luotuja raporttituloksia ja vertaa niitä perusarvoihin
description: Tässä ohjeaiheessa on tietoja siitä, miten voit verrata tuloksia luoduista ER-raporteista raportin perusarvoihin.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 7f7877ccaa0c45ab5f0032d6808280e3c47a43ca
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "317933"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Seuraa luotuja raporttituloksia ja vertaa niitä perusarvoihin

[!include[banner](../includes/banner.md)]

Voit seurata lähteviä sähköisiä tiedostoja luovien ER-muotojen tuloksia. Kun seuranta on käytössä (ER-käyttäjäparametri **Suorita vianmääritystilassa**), uusi jäljitystietue luodaan ER-muodon suorittamisen lokiin aina, kun ER-raportti suoritetaan. Seuraavat tiedot on tallennettu jokaiseen luotuun jäljitykseen:

- Kaikki varoitukset, jotka on luonut oikeellisuustarkistussäännöt
- Kaikki virheet, jotka on luonut oikeellisuustarkistussäännöt
- Kaikki luodut tiedostot, jotka on tallennettu seurantatietueen liitteinä

Voit tallentaa yksittäisiä kohdearvon sovellustiedostoja kaikille ER-muodoille. Tiedostoja käsitellään kohdearvotiedostoina, kun ne kuvaavat suoritettavien raporttien odotettuja tuloksia. Jos kohdearvotiedosto on käytettävissä ER-muodolle, joka suoritettiin, kun jäljitysluonti oli käytössä, jäljitys tallentaa aiemmin mainittujen tietojen lisäksi tulokset luodun sähköisen tiedoston vertailusta kohdearvotiedostoon. Yhdellä napsautuksella voit ladata myös luodun sähköisen tiedoston ja sen kohdearvotiedoston yhtenä zip-tiedostona. Sitten voit tehdä yksityiskohtaisen vertailun ulkoisella työkalulla, kuten Windiff-sovelluksella.

Voit arvioida jäljitystä analysoidaksesi, sisältävätkö luodut sähköiset tiedostot odotetun sisällön. Voit tehdä tämän arvioinnin hyväksyntätestausympäristössä, kun koodiperuste on muutettu (kun esimerkiksi päivitit sovelluksen uuteen ilmentymään, asensit korjaustiedostopaketit tai otit koodin muutokset käyttöön). Näin voit varmistaa, että arviointi ei vaikuta käytettävien ER-raporttien suorittamiseen. Monille ER-raporteille arviointi voidaan tehdä automaattisesti.

Lisätietoja tästä toiminnosta saat toistamalla tehtävöoppaat **ER - Luo raportteja ja vertaa tuloksia (osa 1)** ja **ER - Luo raportteja ja vertaa tuloksia (osa 2)**, jotka ovat osa **7.5.4.3 Testaa IT-palveluita ja ratkaisuja (10679)** -liiektoimintaprosessia, jonka voi ladata [Microsoft Download Centeristä](https://go.microsoft.com/fwlink/?linkid=874684). Näissä tehtäväoppaissa kerrotaan, miten voit määrittää ER-kehyksen käyttämään kohdearvotiedostoja, jotta voit arvioida sähköisiä asiakirjoja.
