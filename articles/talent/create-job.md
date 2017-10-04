---
title: "Työn komponenttien määrittäminen"
description: "Tässä aiheessa kuvataan käsitteellisiä elementtejä, joita työssä voi olla ja annetaan esimerkkejä siitä, miten voit käyttää näitä elementtejä organisaatiossasi."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: rschloma
ms.reviewer: rschloma
ms.search.scope: Core, Operations, UnifiedOperations, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4ab38cd1865a9329d785ed406f24e113c1a0e495
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017

---

# <a name="setting-up-the-components-of-a-job"></a>Työn komponenttien määrittäminen

[!include[banner](includes/banner.md)]

[!include[retail name](includes/retail-name.md)]


Tässä aiheessa kuvataan käsitteellisiä elementtejä, joita työssä voi olla ja annetaan esimerkkejä siitä, miten voit käyttää näitä elementtejä organisaatiossasi. 

Ennen kuin voit luoda uusia töitä, sinun pitää määrittää joitakin viitetietoja. Voit luoda työn, jolla on vain nimi. Kuitenkin antamalla lisätiedot, kuten tehtävänimike, annat oletusarvot toimille, jotka on määritetty työhön. Lisäksi joitakin antamiasi tietoja voidaan käyttää suodattamaan kompensaatiosuunnitelmia tiettyihin töihin. Jos haluat määrittää oikeutuksen, jota voit käyttää suodattamaan kompensaatiosuunnitelmia tiettyyn työhön, sinun on määritettävä työtehtävät ja työtyypit ennen töiden määrittämistä. Kun nämä oletusarvot on käytettävissä, säästät aikaa, kun lisäät toimia työhön. 

Jotkin työtä koskevat tiedot, kuten ammattinimike, tyyppi ja toiminto, ovat päivämääräsidonnaisia. Jos luot työn tänään, mutta lisäät näitä tietoja vasta myöhemmin, ja sitten katsot työtä luontipäivämäärän suhteen, nämä tiedot eivät näy. Siksi kannattaa luoda joitakin näitä viitetietoja ennen kuin niitä vaaditaan. Tällä tavalla voit lisätä tiedot uusiin töihin niitä luotaessa.

## <a name="job-titles"></a>Ammattinimikkeet
Ennen kuin voit luoda töitä, on määritettävä kyseisten töiden otsikot. Toimet perivät ammattinimikkeet töiltä, joihin toimet liittyvät. 

Ylläpidä ammattinimikkeitä käyttäen **Tittelit**-sivua, jonka voit avata käyttämällä hakutoimintoa. Anna **Tittelit **-sivulla tittelit, joita aiot käyttää töihisi.

## <a name="job-types"></a>Työtyypit
Työtyyppien avulla voi luokitella samankaltaisia töitä. Työtyypit eivät ole pakollisia. Kuitenkin jos aiot käyttää työtyyppejä, kun määrität oikeutussäännöt kompensaationhallintaan, sinun tulee määrittää työtyypit ennen töiden määrittämistä. Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka. Voit ylläpitää työtyyppejä **Työtyypit**-sivulla. Anna **Työtyypit**-sivulla työtyypin nimi ja lyhyt kuvaus. Valitse **Vapautustila**-kentässä jokin seuraavista asetuksista ja ilmaistaksesi Fair Labor Standards Act (FLSA) -vapautustilan tämän työtyypin töille:

-   **Vapautus** – Työt on vapautettu ylitöistä FLSA-säädösten mukaisesti.
-   **Ei vapautusta** – Töitä ei ole vapautettu ylitöistä FLSA-säädösten mukaisesti.
-   **Ei koske** – FLSA-kattavuus ei ole käytössä.

## <a name="job-functions"></a>Työtehtävät
Työtehtävät kuvaavat toiminnalliset luokat korkealla tasolla ja yhdistävät korkean tason velvollisuudet. Työtehtävät eivät ole pakollisia. Voit käyttää työtehtäviä yhdessä työtyyppien kanssa suodattaaksesi kompensaatiosuunnitelmia tiettyihin töihin. Voit liittää työtehtävät ja työtyypit kompensaatiosuunnitelmiin määrittämällä oikeutussäännöt **Oikeutussäännöt**-sivulla. Sitten voit liittää kompensaatiosuunnitelmaan tasojoukon, jota käytetään tietyssä oikeutussäännön kautta määritetyssä työtyypin ja -tehtävän yhdistelmässä. (Nämä ominaisuudet koskevat sekä kiinteitä kompensaatiosuunnitelmia että muuttuvia kompensaatiosuunnitelmia). Jos kuitenkin aiot käyttää työtehtäviä, kun määrität oikeutussäännöt kompensaationhallinnalle, sinun tulee määrittää työtehtävät ennen kuin määrität työt. Seuraavassa taulukossa on joitakin esimerkkejä työtehtävistä.

| Työ           | Työtehtävä         |
|---------------|----------------------|
| Myyntipäällikkö | Keskijohdon päällikkö    |
| Kirjanpitäjä    | Ammattilaiset        |

Voit ylläpitää työtehtäviä **Työtehtävät**-sivulla. Anna **Työtehtävät**-sivulla työtehtävän tunnistekoodi ja lyhyt kuvaus.

## <a name="job-tasks"></a>Työtehtävät
Työtehtävät kuvaavat kyseisessä toimessa toimivan työntekijän perustehtäviä. Sama työtehtävä voidaan lisätä useisiin töihin, ja sellaisten töiden toimiin, jotka käyttävät näitä työtehtäviä. Seuraavassa taulukossa on joitakin esimerkkejä työtehtävistä.

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
<li><strong>Suorituskykytarkistus</strong> – Arvioi jokaisen myyjän suorituskykyä.</li>
<li><strong>Poissaolotarkistus</strong> – Hyväksy tai hylkää kunkin myyjän poissaolopyynnöt tai -rekisteröinnit.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kirjanpitäjä</td>
<td><strong>TAL-raportti</strong> – Esitä viikoittaiset talousraportit talousjohtajalle.</td>
</tr>
</tbody>
</table>

Voit ylläpitää työtehtäviä **Työtehtävät**-sivulla. Anna **Työtehtävät**-sivulla työtehtävän nimi ja lyhyt kuvaus. Voit myös lisätä lisätietoja **Huomautus**-kenttään. Muistiinpanoja voi päivittää tietylle työlle muuttamatta tähän kirjoitettuja muistiinpanoja.

## <a name="areas-of-responsibility"></a>Vastuualueet
Vastuualueiden avulla voi osoittaa tietyssä toimessa toimivan työntekijän vastuulla olevat työroolit, prosessit ja tuotteet. Esimerkiksi Kirjanpitäjä-toimessa vastuualue voi olla Tuotteen A talousraportointi. Ylläpidä vastuualueita **Vastuualueet**-sivulla, jonka voit etsiä käyttämällä hakutoimintoa. Anna **Vastuualueet**-sivulla vastuun nimi ja lyhyt kuvaus. Voit myös lisätä lisätietoja **Huomautus**-kenttään. Muistiinpanoja voi päivittää tietylle työlle muuttamatta tähän kirjoitettuja muistiinpanoja.



