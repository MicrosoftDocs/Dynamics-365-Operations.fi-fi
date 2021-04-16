---
title: Vaaralliset materiaalit
description: Tässä ohjeaiheessa annetaan tietoa vaarallisten aineiden asiakirjoista ja tiedoista, jotka tallennetaan ympäristöösi.
author: lachlancashMS
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: bda81f72d5dea24c7ba678b9a86258a02f7b8cd5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829423"
---
# <a name="hazardous-materials"></a>Vaaralliset materiaalit

[!include [banner](../includes/banner.md)]

Vaarallisia aineita koskevat tiedot määritetään tuotetietojen hallinnassa. Tämä moduuli myös tarjoaa asiakirjoja, jotka voidaan tulostaa varastonhallinnan kautta.

Kun lähetät aineita, jotka luokitellaan vaaralliseksi tavaraksi, lähetysten mukana on toimitettava ylimääräistä paperityötä. Vaarallisten aineiden toiminnon avulla asiakkaat voivat tallentaa luokittelutietoja ja liittää sen vapautettaviin nimikkeisiin. Näitä tietoja voidaan sitten käyttää lähetysdokumentaation valmisteluun.

> [!IMPORTANT]
> Microsoft Dynamics 365 Supply Chain Managementin vaarallisten aineiden toiminnot muodostavat hyödyllisten tuotetietokenttien ja liittyvien toimintojen kokoelman, joka auttaa kirjaamaan vaarallisiin tuotteisiin liittyviä tietoja ja viittaamaan niihin. Nämä toiminnot auttavat myös suunnittelemaan ja tulostamaan lähetysasiakirjoja, joissa on joitakin samoja tietoja lähetettävistä vaarallisista aineista. Järjestelmä ei kuitenkaan automaattisesti takaa, että maan tai alueen kaikkia soveltuvia säädöksiä noudatetaan. Vaikka nämä työkalut on tarkoitettu auttamaan yleisten määräysten noudattamisessa, ne eivät yksin riitä eikä ole takeita, että määräyksiä noudatetaan niiden avulla. Organisaatio vastaa siitä, että se on tietoinen kaikissa käytössä olevista säädöksistä ja että se tekee tarvittavan niiden noudattamiseksi.

Ennen tämän toiminnon käyttöä on tehtävä seuraavat määritykset:

- **Tuotetietojen hallinta:** Määritä koodit, joita voidaan soveltaa vapautettuihin tuotteisiin.
- **Varastonhallinta:** Käytä ylimääräisiä lähetysasiakirjoja lähetystietojen tulostamiseen.

## <a name="product-information-management"></a>Tuotetietojen hallinta

Tuotetietojen hallinnassa on määritystaulukkojen joukko, jossa voit lisätä viitetiedot, jotka annetaan vaarallisten tavaroiden luetteloissa maa-, ilma- ja vesikuljetuksia varten.

Tässä on joitakin säädöksiä, joihin usein viitataan:

- **ADR** – Vaarallisten tavaroiden kansainväliseen maantiekuljetukseen liittyviä säädöksiä
- **CFR 49** – Yhdysvaltojen vaarallisten tavaroiden kuljetusta koskevia säädöksiä
- **IMDG** – Merenkulun kansainvälinen vaarallisten tavaroiden koodeksi (IMDG)
- **IATA** – Kansainvälisin ilmakuljetusliiton (IATA) vaarallisten tavaroiden säädökset

Kussakin näistä säädöksistä on viitekoodeja sisältävät vaarallisten tavaroiden luettelo. Kunkin kuljetustavan luettelot yhdistetään jaetuissa kansainvälisissä luokituksissa. Supply Chain Management tarjoaa viitetaulukon näiden luettelojen jaetuille koodeille. Kullakin luettelolla on myös joitakin yksilöllisiä koodeja, jotka voidaan määrittää.

Voit aloittaa näiden tietojen määrittämisen luomalla säädöksen, jonka avulla voit määrittää alustavat parametrit.

## <a name="warehouse-management"></a>Varastonhallinta

Lähetyksen valmistelun yhteydessä voi tulostaa useita uusia raportteja. Näissä raporteissa käytetään tuotetietojen hallinnassa määritettyjä tietoja.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]