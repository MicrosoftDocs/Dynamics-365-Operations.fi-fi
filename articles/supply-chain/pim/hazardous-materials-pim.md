---
title: Vaaralliset materiaalit
description: Tässä ohjeaiheessa annetaan tietoa vaarallisten aineiden asiakirjoista ja tiedoista, jotka tallennetaan ympäristöösi.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5006f06d90ddcc314a51878e9e21337de7d493e7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208457"
---
# <a name="hazardous-materials"></a>Vaaralliset materiaalit

[!include [banner](../includes/banner.md)]

Vaarallisia aineita koskevat tiedot määritetään tuotetietojen hallinnassa. Tämä moduuli myös tarjoaa asiakirjoja, jotka voidaan tulostaa varastonhallinnan kautta.

Kun lähetät aineita, jotka luokitellaan vaaralliseksi tavaraksi, lähetysten mukana on toimitettava ylimääräistä paperityötä. Vaarallisten aineiden toiminnon avulla asiakkaat voivat tallentaa luokittelutietoja ja liittää sen vapautettaviin nimikkeisiin. Näitä tietoja voidaan sitten käyttää lähetysdokumentaation valmisteluun.

> [!IMPORTANT]
> Vaarallisten tavaroiden lähetysten hallintaa varten Microsoft Dynamics 365 Supply Chain Management antaa sinun määrittää tuotteisiin liittyviä ylimääräisiä viitetietoja. Voit myös määrittää ylimääräisiä toimitusasiakirjoja. Järjestelmä ei kuitenkaan ole automaattisesti maan tai alueen säädösten mukainen. Sen sijaan se on työkalu, joka voi auttaa ohjelmaa yleisellä tasolla.

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
