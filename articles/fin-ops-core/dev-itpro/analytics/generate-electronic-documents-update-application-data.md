---
title: Sähköisten asiakirjojen luominen ja päivittäminen sovellustiedoilla sähköistä raportointia (ER) käyttäen
description: Voit suunnitella sähköisen raportoinnin muotoja, joilla voidaan luoda sovelluksessa lähteviä sähköisiä asiakirjoja.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 4ae3405a882ac37fd9758d8ff0902896562fa06b
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093870"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>Sähköisten asiakirjojen luominen ja sovellustietojen päivittäminen ER:n avulla

[!include [banner](../includes/banner.md)]

Voit suunnitella sähköisen raportoinnin muotoja, joilla voidaan luoda sovelluksessa lähteviä sähköisiä asiakirjoja. Voit suunnitella myös sähköisiä raportointimuotoja, jotka jäsentävät saapuvia sähköisiä asiakirjoja ja jotka päivittävät sovelluksen tiedot kyseisten asiakirjojen tiedoilla.

Tämän toiminnon avulla yhdellä sähköisen raportoinnin muodolla voidaan luoda lähteviä sähköisiä asiakirjoja ja päivittää sitten sovelluksen tiedot. Tätä toimintoa voidaan käyttää seuraavissa skenaarioissa:

- Voit estää sovelluksen tietojen toistuvan käytön myöhemmissä prosessissa merkitsemällä sovelluksen tiedot heti, kun niillä on luotu sähköisiä asiakirjoja. Voit esimerkiksi merkitä maksutapahtumat käsitellyiksi heti, kun ne on sisällytetty luotuun maksusanomaan.
- Sähköisen raportoinnin logiikan avulla luotujen sähköisten asiakirjojen käsittelytietojen tallennus, Esimerkiksi yksilöllinen maksusanoman tunnus, joka luodaan ER-lausekkeella. Lauseke perustuu tietoihin, jotka annettiin ER-valintaikkunassa, kun asiakirjoja luodaan suorittamalla sähköisen raportoinnin muoto.

Saat lisätietoja tästä ominaisuudesta toistamalla joukon ER-luontiasiakirjoja sovellustietojen päivityksen tehtäväoppaassa (osa liiketoimintaprosessia 7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)), joka opastaa Intrastat-raportoinnin ja -arkistoinnin vaiheissa. Seuraavat tiedostot tarvitaan joidenkin tehtäväoppaiden vaiheiden suorittamiseen. Lataa ja tallenna nämä tiedostot paikallisesti tietokoneeseen.

- [Sähköisen raportoinnin tietomallien määritys: Intrastat (malli)](https://go.microsoft.com/fwlink/?linkid=849038)
- [Sähköisen raportoinnin mallin yhdistämismäärityksen määrittäminen: Intrastat (yhdistämismääritys)](https://go.microsoft.com/fwlink/?linkid=849038)
- [Sähköisen raportointimuodon määritys: Intrastat (muoto)](https://go.microsoft.com/fwlink/?linkid=849038)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]