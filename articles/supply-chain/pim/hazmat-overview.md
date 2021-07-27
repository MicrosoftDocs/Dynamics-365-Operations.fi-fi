---
title: Vaarallisten aineiden yleiskatsaus
description: Tässä ohjeaiheessa on sellaisten vaarallisten aineiden käsittelyyn ja dokumentointiin liittyvien toimintojen yleiskatsaus, joita käytetään tuotetietojen hallinnassa ja varastonhallinnassa.
author: dasani-madipalli
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 5f8c3dc084f4f260f8cc29b3957913e9bc1b762d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356996"
---
# <a name="hazardous-materials-overview"></a>Vaarallisten aineiden yleiskatsaus

[!include [banner](../includes/banner.md)]

Lähetys- ja kuljetusmääräysten noudattaminen edellyttää, että organisaatiot, jotka lähettävät vaarallisiksi aineiksi luokiteltuja materiaaleja, sisällyttävät lähetyksiin lisäasiakirjoja. Vaarallisten aineiden toiminnon avulla asiakkaat voivat tallentaa vapautettuihin nimikkeisiin liittyviä tietoja. Näitä tietoja voidaan sitten käyttää lähetysdokumentaation valmisteluun. Vaarallisia aineita lähettävälä organisaatiolla on oltava omat lähetysprosessin hallintaan käytettävät prosessit ja menettelytavat. Microsoft Dynamics 365 Supply Chain Management on vain työkalu, joka auttaa tarvittavien asiakirjojen luonnissa.

Seuraava kaavio sisältää vaarallisten aineiden toiminnon määrittämiseen ja käyttämiseen tarvittavat vaiheet.

![Vaarallisten aineiden toiminnon määrittäminen ja käyttäminen.](media/hazmat-overview.png "Vaarallisten aineiden toiminnon määrittäminen ja käyttäminen")

Vaarallisten aineiden toiminto määritetään tuotetietojen hallinnassa, ja se sisältää asiakirjoja, jotka voidaan tulostaa varastonhallinnassa. Ne ovatkin kaksi tärkeintä aluetta, joissa ominaisuuden toiminnot tarkastellaan ja määritetään ja joissa niitä käytetään.

- **Tuotetietojen hallinta** – vapautetussa tuotteessa käytettävien koodien määrittäminen.
- **Varastonhallinta** – lähetykseen tulostettavien lähetyksen lisäasiakirjojen käyttäminen.

> [!IMPORTANT]
> Supply Chain Managementin vaarallisten aineiden toiminnot muodostavat hyödyllisten tuotetietokenttien ja liittyvien toimintojen kokoelman, joka auttaa kirjaamaan vaarallisiin tuotteisiin liittyviä tietoja ja viittaamaan niihin. Nämä toiminnot auttavat myös suunnittelemaan ja tulostamaan lähetysasiakirjoja, joissa on joitakin samoja tietoja lähetettävistä vaarallisista aineista. Järjestelmä ei kuitenkaan automaattisesti takaa, että maan tai alueen kaikkia soveltuvia säädöksiä noudatetaan. Vaikka nämä työkalut on tarkoitettu auttamaan yleisten määräysten noudattamisessa, ne eivät yksin riitä eikä ole takeita, että määräyksiä noudatetaan niiden avulla. Organisaatio vastaa siitä, että se on tietoinen kaikissa käytössä olevista säädöksistä ja että se tekee tarvittavan niiden noudattamiseksi.

## <a name="product-information-management"></a>Tuotetietojen hallinta

Tuotetietojen hallinnassa on määritystaulukkojen joukko, jossa voit antaa erilaisten vaarallisten aineiden luetteloiden viitetiedot maa-, ilma- ja vesikuljetuksia varten.

Tämän toiminnon kehittämisessä käytettiin seuraavia yleisiä määräyksiä:

- **ADR** – Vaarallisten tavaroiden kansainväliseen maantiekuljetukseen liittyviä säädöksiä
- **CFR 49** – Yhdysvaltojen vaarallisten tavaroiden kuljetusta koskevia säädöksiä
- **IMDG** – Merenkulun kansainvälinen vaarallisten tavaroiden koodeksi (IMDG)
- **IATA** – Kansainvälisin ilmakuljetusliiton (IATA) vaarallisten tavaroiden säädökset

Kukin määräysjoukko sisältää vaarallisten aineiden ja viitekoodien standardoidut luettelot. Supply Chain Managementissa onkin näissä luetteloissa olevien yleisten koodien viitetaulukko. Jokaisessa luettelossa on myös joitakin yksilöllisiä, määritettäviä koodeja.

Lisätietoja vaarallisten aineiden määräysten ja arvojen määrittämisestä ja arvojen määrittämisestä tuotteisiin on seuraavissa ohjeaiheissa:

- [Vaarallisten aineiden määrittäminen](hazmat-setup.md)
- [Tuotteiden, tilausten, lähetysten ja kuormien vaaralliset aineet](hazmat-items.md)

## <a name="warehouse-management"></a>Varastonhallinta  

Kun lähetystä valmistellaan varastonhallinnassa, voit tulostaa useita uusia raportteja, joissa käytetään tuotetietojen hallinnassa määritettyjä tietoja. Lisätietoja käytettävissä olevista raporteista ja niiden käyttämisestä on kohdassa [Vaarallisten aineiden kyselyt ja raportit](hazmat-reports.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]