---
title: Sähköisten asiakirjojen luominen ja päivittäminen sovellustiedoilla sähköistä raportointia (ER) käyttäen
description: Voit suunnitella sähköisen raportoinnin muotoja, joilla voidaan luoda sovelluksessa lähteviä sähköisiä asiakirjoja.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f66a173c7d66f915a7802e42caf1a36f661eea1
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944314"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>Sähköisten asiakirjojen luominen ja sovellustietojen päivittäminen ER:n avulla

[!include [banner](../includes/banner.md)]

Voit suunnitella sähköisen raportoinnin muotoja, joilla voidaan luoda sovelluksessa lähteviä sähköisiä asiakirjoja. Voit suunnitella myös sähköisiä raportointimuotoja, jotka jäsentävät saapuvia sähköisiä asiakirjoja ja jotka päivittävät sovelluksen tiedot kyseisten asiakirjojen tiedoilla.

Tämän toiminnon avulla yhdellä sähköisen raportoinnin muodolla voidaan luoda lähteviä sähköisiä asiakirjoja ja päivittää sitten sovelluksen tiedot. Tätä toimintoa voidaan käyttää seuraavissa skenaarioissa:

- Voit estää sovelluksen tietojen toistuvan käytön myöhemmissä prosessissa merkitsemällä sovelluksen tiedot heti, kun niillä on luotu sähköisiä asiakirjoja. Voit esimerkiksi merkitä maksutapahtumat käsitellyiksi heti, kun ne on sisällytetty luotuun maksusanomaan.
- Sähköisen raportoinnin logiikan avulla luotujen sähköisten asiakirjojen käsittelytietojen tallennus, Esimerkiksi yksilöllinen maksusanoman tunnus, joka luodaan ER-lausekkeella. Lauseke perustuu tietoihin, jotka annettiin ER-valintaikkunassa, kun asiakirjoja luodaan suorittamalla sähköisen raportoinnin muoto.

Saat lisätietoja tästä ominaisuudesta toistamalla joukon ER-luontiasiakirjoja sovellustietojen päivityksen tehtäväoppaassa (osa liiketoimintaprosessia 7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)), joka opastaa Intrastat-raportoinnin ja -arkistoinnin vaiheissa. Seuraavat tiedostot tarvitaan joidenkin tehtäväoppaiden vaiheiden suorittamiseen. Lataa ja tallenna nämä tiedostot paikallisesti tietokoneeseen.

- [Sähköisen raportoinnin tietomallien määritys: Intrastat (malli)](https://download.microsoft.com/download/9/c/e/9ceeacbe-c13e-422e-96f2-594c4a6b45b7/Intrastatmodel.xml)
- [Sähköisen raportoinnin mallin yhdistämismäärityksen määrittäminen: Intrastat (yhdistämismääritys)](https://download.microsoft.com/download/2/1/d/21ddaaeb-64c5-4408-a35f-1ccb922d40a4/Intrastatmapping.xml)
- [Sähköisen raportointimuodon määritys: Intrastat (muoto)](https://download.microsoft.com/download/8/b/b/8bbb8891-e88d-4739-b92a-2d1d2fffcb79/Intrastatformat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
