---
title: "Työn komponenttien määrittäminen"
description: "Tässä aiheessa kuvataan käsitteellisiä elementit työ voi olla ja antaa esimerkkejä siitä, miten voit käyttää niitä osia organisaatiossa."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: d96b1f01a5cb4370436888deae8fd4835a0dbb80
ms.openlocfilehash: b8143db5b133337603a7f2f46028d91bb81cd947
ms.lasthandoff: 03/31/2017


---

# <a name="setting-up-the-components-of-a-job"></a>Työn komponenttien määrittäminen

Tässä aiheessa kuvataan käsitteellisiä elementit työ voi olla ja antaa esimerkkejä siitä, miten voit käyttää niitä osia organisaatiossa. 

Ennen kuin voit luoda töitä, joitakin tietoja on määritettävä. Voit luoda projektin, jonka nimi. Kuitenkin mukaan lukien lisätiedot, kuten Tehtävänimike, annat oletusarvot toimilla, jotka on liitetty työ. Lisäksi joitakin tietoja, jotka syötetään avulla voidaan suodattaa kompensaatiosuunnitelmia tiettyihin töihin. Jos haluat määrittää kelpoisuus, jonka avulla voit suodattaa kompensaatiosuunnitelmia tietyn työn, olisi määritettävä työtehtävät ja työtyypit ennen töitä. Ottaa nämä oletusarvot on käytettävissä, säästät aikaa, kun lisäät toimia työn. 

Työtä koskevat tiedot, kuten ammatti, tyyppi ja funktio, ovat tehokkaan päivämäärä. Luoda työtä tänään, mutta älä lisää näitä tietoja myöhemmin, ja sitten luontipäivämäärä työtä katsomalla, jos nämä tiedot eivät näy. Siksi kannattaa luoda joitakin tietoja tästä ennen sitä edellyttävät. Tällä tavalla voit lisätä tietoja uusia töitä niitä luotaessa.

## <a name="job-titles"></a>Ammattinimikkeet
Ennen kuin voit luoda töitä, on määritettävä kyseisten töiden otsikot. Toimet perivät ammattinimikkeet töiltä, joihin toimet liittyvät. 

Ylläpidä ammattinimikkeitä käyttäen **otsikoiden** sivu, jonka voit avata käyttämällä Etsi-toimintoa. Käyttöön ** otsikot ** kirjoittaa otsikoita, joita aiot käyttää Projektit-sivulla.

## <a name="job-types"></a>Työtyypit
Työlajit avulla voit ryhmitellä luokkiin vastaavia töitä. Tyypit eivät ole pakollisia. Kuitenkin jos aiot käyttää työtyyppejä, kun määrität oikeutussäännöt kompensaationhallintaan, sinun tulee määrittää työtyypit ennen töiden määrittämistä. Työlajit ovat täysipäiväisiä ja osa-aikaisen tai maksettava palkka ja hourly. Voit säilyttää käyttämällä työtyyppejä **työlajit** sivulla. - **Työlajit** nimi ja lyhyt kuvaus työn tyyppi-sivulta. - **Vapauttaa tilaa** jokin seuraavista asetuksista ja määritä käyvän työn Standards Act (FLSA) vapauttaa tilan työt, joilla on tämä työlaji-kenttään:

-   **Vapauttaa** – töiden on vapautettu ylityötä FLSA kohdassa.
-   **Ei vapautusta** – työt eivät ole ylitöitä FLSA mukaisesti vapautettu.
-   **Ei koske** – FLSA kattavuus ei ole tarpeellinen.

## <a name="job-functions"></a>Työtehtävät
Työn liitoskohtia kuvaavat toiminnalliset luokat korkean tason ja korkean tason tehtävät liittyvät. Työtehtävät eivät ole pakollisia. Voit käyttää työtehtäviä yhdessä työtyyppien, voit suodattaa kompensaatiosuunnitelmia tiettyihin töihin. Voit liittää työtehtävät ja työtyypit kompensaatiosuunnitelmiin määrittämällä oikeutussääntöjä **oikeutussääntöjä** sivulla. Sitten voit liittää kompensaatiosuunnitelmaan, jotka koskevat tietyn työn tyyppi ja työtehtävä, jonka olet määritellyt oikeutussäännön kautta yhdistelmä Tasoryhmää. (Nämä toiminnot ovat sekä kiinteiden kompensaatiosuunnitelmien muuttuvia kompensaatiosuunnitelmia.) Kuitenkin jos aiot käyttää työtehtäviä, kun määrität Kompensaationhallinnan oikeutussäännöt, olisi määritettävä työtehtäviä ennen töitä. Seuraavassa taulukossa on joitakin esimerkkejä työtehtäviä.

| Työ           | Työtehtävä      |
|---------------|-------------------|
| Myyntipäällikkö | Puolivälin tason hallinta |
| Kirjanpitäjä    | Asiantuntijat     |

Voit säilyttää käyttämällä työtehtäviä **työtehtävien** sivulla. - **Työtehtävien** sivulla, kirjoita tunnus ja lyhyt kuvaus työtehtävän.

## <a name="job-tasks"></a>Työtehtävät
Työtehtävät kuvataan perustehtäviä, että työntekijällä, joka on sellaisessa asennossa, työn on valmis. Saman tehtävän työn voidaan lisätä useita töitä, ja paikat, joissa käytetään projektitehtävät työt. Seuraavassa taulukossa on esimerkkejä työn tehtäviä.

<table>
<thead>
<tr class="header">
<th>Työ</th>
<th>Työtehtävä</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Myyntipäällikkö</td>
<td><ul>
<li><strong>Perf-Tarkista</strong> – arvioi jokaisen myyjän työn suorituskykyä.</li>
<li><strong>Abs-Tarkista</strong> – Hyväksy tai Hylkää poissaolopyynnöt tai rekisteröintien kunkin myyjän.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kirjanpitäjä</td>
<td><strong>FIN-raportti</strong> – esittää viikoittain tilinpäätökset rahoitusjohtaja.</td>
</tr>
</tbody>
</table>

Voit säilyttää projektitehtäviä käyttämällä **projektin tehtävien** sivulla. - **Projektitehtävien** sivulla, kirjoita nimi ja projektitehtävän kuvaus. - **Huomaa** kenttään, voit halutessasi kirjoittaa lisätietoja. Muistiinpanot voi päivittää muuttamatta huomauttaa, että olet kirjoittanut tähän työlle.

## <a name="areas-of-responsibility"></a>Vastuualueet
Käytetään osoittamaan työroolien, prosesseja ja tuotteita, jotka ovat vastuussa oleva työntekijä, joka on sellaisessa asennossa, työn vastuualueet. Esimerkiksi työn, jonka nimi on "Kirjanpitäjä", yksi vastuualue voi olla "Rahoitus tuotteen A. raportointi" Ylläpidä vastuualueita avulla **vastuualueet** sivulle, jossa voit etsiä käyttämällä Etsi-toimintoa. - **Vastuualueet** sivulla, kirjoita nimi ja kuvaus vastuualueen. - **Huomaa** kenttään, voit halutessasi kirjoittaa lisätietoja. Muistiinpanot voi päivittää muuttamatta huomauttaa, että olet kirjoittanut tähän työlle.


