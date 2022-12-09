---
title: Talousraporttien suunnittelutoiminnon raportin määritykset
description: Tässä artikkelissa on tietoja raportin määrityksistä.
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.form: FinancialReports
ms.openlocfilehash: 2ffef335c694af56486ccd7738818c4edda49b9e
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802529"
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
<td>Tulos ja jakelu</td>
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
