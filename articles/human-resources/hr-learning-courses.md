---
title: Määritä koulutuskursseja
description: Henkilöstöhallinnon järjestelmänvalvojat ja esimiehet voivat ylläpitää tietoja työntekijöille tarjottavista kursseista kurssitoiminnoilla.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 45466b8f52ddc261737da7474767c21f5bd331f8
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689884"
---
# <a name="set-up-training-courses"></a>Määritä koulutuskursseja


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Henkilöstöhallinnon järjestelmänvalvojat ja esimiehet voivat ylläpitää tietoja työntekijöille tarjottavista kursseista kurssitoiminnoilla.

##  <a name="set-up-prerequisites"></a>Määritä edellytykset

Seuraavat tiedot ovat pakollisia, ja ne on määritettävä ennen kurssien luontia.
-   **Kurssityypit**

Seuraavat tiedot ovat valinnaisia, jotka voit halutessasi määrittää kursseille. Jos tiedät, että kirjoitat kursseille nämä tiedot, sinun on määritettävä nämä tiedot, ennen kuin voit luoda kurssin tietueita.
-   **Luokkahuoneryhmät**
-   **Kurssiryhmät**
-   **Kurssipaikat**
-   **Luokkahuoneet**
-   **Opettajat**

## <a name="course-types"></a>Kurssityypit
Voit käyttää kurssityyppejä kurssien luokittelemiseen kurssin rakenteen tai sisällön perusteella. Voit luoda kurssityyppejä **Kurssityypit**-sivulla. Sinun on valittava kurssityyppi, kun luot kurssitietueen.

## <a name="course-setup-type"></a>Kurssin asetustyyppi
Seuraavassa taulukossa luetellaan kurssien kolme asetustyyppiä. Kurssin rakenteen määrittävät asetustyypit.

<table>
<thead>
<tr class="header">
<th>Asetustyyppi</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Vakio</strong></td>
<td>Valitse tämä tyyppi kursseille, joille ei ole määritetty päivittäistä työjärjestystä. Tämä on oletusarvoinen asetustyyppi, kun luot uuden kurssin.</td>
</tr>
<tr class="even">
<td><strong>Työjärjestys</strong></td>
<td>Valitsemalla tämän tyypin voit suunnitella useita päiviä kestävän kurssin eri päivien sisällön.</td>
</tr>
<tr class="odd">
<td><strong>Työjärjestys ja istunto</strong></td>
<td>Valitse tämä laji monimutkaisemmille kursseille. Voit esimerkiksi jakaa kurssin ohjelman kappaleisiin ja istuntoihin.
<ul>
<li><strong>Etenemissuunnitelma</strong> – etenemissuunnitelmat ovat kurssin erityisiä aihealueita.</li>
<li><strong>Istunnot</strong> – istunnot jaetaan etenemissuunnitelmiin ja auttamat tunnistamaan prosesseja tai tekniikkoja, joilla on merkitystä etenemissuunnitelman kannalta.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a>Kurssin tehtävät
Voit suorittaa jokaiselle kurssille seuraavat tehtävät:
- Osallistujien rekisteröinti
- Rekisteröinnin määräajan määritys
- Osallistujien vähimmäis- ja enimmäismäärien määritys
- Kurssipaikan ja luokkahuoneen määritys
- Hotellien suosittelu kurssin osallistujille
- kurssikuvauksen luonti, jota voidaan mainostaa **työntekijöiden itsepalvelussa**

  >**Huomautus** Voit poistaa kurssin vain, jos kukaan ei ole rekisteröitynyt siihen. 

## <a name="course-statuses"></a>Kurssin tilat
Seuraavassa taulukossa luetellaan mahdolliset kurssin tilat sekä toiminnot, jotka voidaan suorittaa, kun kurssilla on tietty tila.

<table>
<thead>
<tr class="header">
<th>Tila</th>
<th>Toimet</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Luotu</strong></td>
<td><ul>
<li>Kirjoita ja muuta kurssin tietoja.</li>
<li>Muuta kurssin tilaksi <strong>Avoin</strong>, jotta työntekijät voivat rekisteröityä kurssille.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Avaa</strong></td>
<td><ul>
<li>Rekisteröi kurssin osallistujat.</li>
<li>Poista kurssin osallistujia.</li>
<li>Vahvista kurssin osallistujat</li>
<li>Muuta kurssin tilaksi <strong>Suljettu</strong> tai <strong>Peruutettu</strong>.</li>
<li>Suunnittele kyselylomakkeita osallistujille, joiden tila on <strong>Vahvistettu</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Suljettu</strong></td>
<td>Voit avata kurssin uudelleen.</td>
</tr>
<tr class="even">
<td><strong>Peruutettu</strong></td>
<td>Voit avata kurssin uudelleen.</td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a>Kurssin osallistujat
Kurssin osallistujat ovat työntekijöitä, jotka osallistuvat koulutuskurssille tai tapahtumaan. Voit rekisteröidä osallistujia vain avoimille kursseille. Kurssille rekisteröitävien osallistujien vähimmäis- ja enimmäismäärä on määritetty **Kurssit**-sivun **Yleinen**-pikavälilehdessä.

## <a name="workflow"></a>Työnkulku

Työntekijät, jotka ilmoittautuvat kurssille **työntekijän itsepalvelun** sivulla, voivat saada ilmoittautumisen reititettyä hyväksynnän työnkulun kautta. Voit määrittää työnkulun kurssille **Kurssit**-sivun **Yleiset** -pikavälilehdessä.







[!INCLUDE[footer-include](../includes/footer-banner.md)]
