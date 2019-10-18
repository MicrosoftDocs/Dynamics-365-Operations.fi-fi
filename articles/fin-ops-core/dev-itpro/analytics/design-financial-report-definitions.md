---
title: Talousraporttien suunnittelutoiminnon raportin määritykset
description: Tässä artikkelissa on tietoja raportin määrityksistä. Raportin määritys on raporttiosa (tai rakenneosa), joka käyttää raportin luontiin rivin, sarakkeen ja valinnaisesti myös raportointipuun määritystä. Raportin määrityksessä on myös vaihtoehtoja ja asetuksia raportin mukauttamiseen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 07f49e63fc2e0410d2673f3ca9378325e9b4ebf8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174141"
---
# <a name="report-definitions-in-financial-report-designer"></a>Talousraporttien suunnittelutoiminnon raportin määritykset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja raportin määrityksistä. Raportin määritys on raporttiosa (tai rakenneosa), joka käyttää raportin luontiin rivin, sarakkeen ja valinnaisesti myös raportointipuun määritystä. Raportin määrityksessä on myös vaihtoehtoja ja asetuksia raportin mukauttamiseen. 

Raportin määritys on raporttiosa (tai rakenneosa), joka käyttää raportin luontiin rivin, sarakkeen ja valinnaisesti myös raportointipuun määritystä. Raporttimääritys sisältää myös vaihtoehtoja ja asetuksia, joiden avulla voit mukauttaa raporttia. Kun olet määrittänyt rivi- ja sarakemääritykset, ne on yhdistettävä raportin määrityksessä. Tällöin määritetään myös muita määrityksen osia, kuten erittelytaso ja raportin päivämäärä. Voit nyt tallentaa ja luoda raportin. Talousraportointi sisältää seuraavat erittelytasot:

- Taloushallinto
- Taloudellinen ja Tili
- Taloudellinen, Tili ja Tapahtuma

Tapahtumatiedot eivät kuitenkaan välttämättä ole käytettävissä raporteissa. Tämä riippuu siitä, miten tiedot tallennetaan Microsoft Dynamics ERP -järjestelmään.

## <a name="create-a-report-definition"></a>Luo raportin määritys
1. Valitse raportin suunnitteluohjelman **Tiedosto** -valikosta **Uusi**, ja valitse sitten **Raportin määritys**.
2. Määritä tarvittavat tiedot **Raportti**, **Tuotos ja Jakelu**, **Ylä- ja alatunnisteet** ja **Asetukset** -välilehdille.

## <a name="contents-of-a-report-definition"></a>Raportin määrityksen sisältö
Seuraavassa taulukossa kuvataan raportin määrityksen välilehdet sekä tietojen käyttötapa.

<table>
<thead>
<tr>
<th>Sarkain</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr>
<td>Raportti</td>
<td>Luo raportti, määritä raportti tai muokkaa aiemmin luotua raporttia.</td>
</tr>
<tr>
<td>Tuotos ja Jakelu</td>
<td>Muuttaa tuotoksen tyypin ja raportin kohteen.</td>
</tr>
<tr>
<td>Ylä- ja alatunnisteet</td>
<td>Määrittää ja muotoilee raportin ylä- ja alatunnisteet. Voit esimerkiksi lisätä tekstiä tai kuvia tunnisteisiin. Talousraportointi tukee .bmp-, .jpg- ja .png-kuvatiedostoja. Voit myös käyttää automaattisia koodeja lisätäksesi muita tietoja, kuten yrityksen nimen, raportin nimen tai sivunumeron.</td>
</tr>
<tr>
<td>Asetukset</td>
<td>Määritä raportin määritysasetukset, joihin voi sisältyä seuraavia asetuksia:
<ul>
<li>Muotoilu ja pyöristyssummat</li>
<li>Raporttierittelyn muoto</li>
<li>Raporttipuiden muoto</li>
<li>Luo poikkeusraportti</li>
<li>Valuuttamuunnoksen määritys</li>
<li>Välisumma- ja suodatintilitiedot</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Lisäresurssit

[Talousraportointi](financial-reporting-intro.md)
