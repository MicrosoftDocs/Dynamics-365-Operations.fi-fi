---
title: Luo raportteja lisäämällä sisältöä XML-raakatiedostona
description: Voit suunnitella sähköisen raportoinnin (ER) muotoja, jotka luovat lähteviä tiedostoja XML-muodossa.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 824d6bdf53cacbd81004a009e4019b5ab7e5cff0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686714"
---
# <a name="generate-reports-by-adding-content-as-raw-xml"></a>Luo raportteja lisäämällä sisältöä XML-raakatiedostona

[!include[banner](../includes/banner.md)]

Voit käyttää uutta **RAW XML** -muotoelementtiä suunnitellaksesi sähköisen raportoinnin (ER) muotoja, jotka luovat lähteviä asiakirjoja XML-muodossa. Haluat joskus ehkä lisätä XML-raakatietoja näihin raportteihin esimerkiksi seuraavista syistä:

- On helpompaa käyttää XML-raakatietoja raportin alkuperäisessä suunnittelussa ja jatkuvassa ylläpidossa, koska XML-rakenne voidaan luoda automaattisesti suorittamalla suorituksenaikainen lauseke. Siksi useita sidontoja ei tarvitse määrittää suunnitteluvaiheessa useille muodon elementeille. Tämä on mahdollista, kun käyttämäsi tietolähteet sisältävät tietoja, joiden avulla voidaan luoda XML-elementit raporttia luotaessa.
- Muita menetelmiä ei voi käyttää raportin täyttämiseksi XML-sisällöllä, joka aiemmin vastaanotettiin ja tallennettiin järjestelmään. Esimerkiksi luotavan XML-vastauksen tulisi sisältää aiemmin lähetetyn XML-pyynnön sisältö.
- Muita menetelmiä ei voi käyttää merkkien lisäämiseen luotuun asiakirjaan niiden numeeristen koodien perusteella. Joillekin kielille ja merkeille tällaisia koodeja ei ole. Esimerkkejä ovat kreikan kirjain rho (ρ) sekä HTML-entiteettikoodit, kuten \&eacute *e*-kirjaimelle, jossa on akuuttiaksentti (é).

> [!NOTE]
> Huomaa, että kehys ei hallinnoi sitä, onko **RAW XML** -muotoelementin avulla luotuun asiakirjaan lisätty elementin muoto on oikein muotoiltu.

Lisätietoja tästä toiminnosta saat toistamalla tehtäväoppaat **ER XML-raakadatan käyttäminen XML-raporttien luomiseen (osa 1: suunnittele tietomalli)** ja **ER XML-raakadatan käyttäminen XML-raporttien luomiseen (osa 2: raportin suunnittelu ja suorittaminen)**, jotka kuuluvat **7.5.4.3 Hanki/Kehitä IT-palvelu/ratkaisukomponentit (10677)** -liiketoimintaprosessiin, joka voidaan ladata [Microsoft Download Centeristä](https://go.microsoft.com/fwlink/?linkid=874684). Nämä tehtäväoppaat selittävät prosessin, jossa määritetään ER-muoto lisäämään XML-raakadataa luotuihin asiakirjoihin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]