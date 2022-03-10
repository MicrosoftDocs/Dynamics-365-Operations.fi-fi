---
title: Työn komponenttien määrittäminen
description: Tässä aiheessa kuvataan käsitteellisiä elementtejä, joita työssä voi olla ja annetaan esimerkkejä siitä, miten voit käyttää näitä elementtejä organisaatiossasi.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle, HcmPersonnelManagementWorkspace, HCMJobFamily
audience: Application User
ms.author: twheeloc
ms.search.scope: Human Resources
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e2c9421646dacc5523f40b28b550881dc4b25dd
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068156"
---
# <a name="set-up-the-components-of-a-job"></a>Työn komponenttien määrittäminen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä aiheessa kuvataan käsitteellisiä elementtejä, joita työssä voi olla ja annetaan esimerkkejä siitä, miten voit käyttää näitä elementtejä organisaatiossasi. 

Ennen kuin voit luoda uusia töitä, sinun pitää määrittää joitakin viitetietoja. Voit luoda työn, jolla on vain nimi. Kuitenkin antamalla lisätiedot, kuten tehtävänimike, annat oletusarvot toimille, jotka on määritetty työhön. Lisäksi joitakin antamiasi tietoja voidaan käyttää suodattamaan kompensaatiosuunnitelmia tiettyihin töihin. Jos haluat määrittää oikeutuksen, jota voit käyttää suodattamaan kompensaatiosuunnitelmia tiettyyn työhön, sinun on määritettävä työtehtävät ja työtyypit ennen töiden määrittämistä. Kun nämä oletusarvot on käytettävissä, säästät aikaa, kun lisäät toimia työhön. 

Jotkin työtä koskevat tiedot, kuten ammattinimike, tyyppi ja toiminto, ovat päivämääräsidonnaisia. Jos luot työn tänään, mutta lisäät näitä tietoja vasta myöhemmin, ja sitten katsot työtä luontipäivämäärän suhteen, nämä tiedot eivät näy. Siksi kannattaa luoda joitakin näitä viitetietoja ennen kuin niitä vaaditaan. Tällä tavalla voit lisätä tiedot uusiin töihin niitä luotaessa.

## <a name="job-titles"></a>Ammattinimikkeet
Ennen kuin voit luoda töitä, on määritettävä kyseisten töiden otsikot. Toimet perivät ammattinimikkeet töiltä, joihin toimet liittyvät. 

Ylläpidä ammattinimikkeitä käyttäen **Tittelit**-sivua, jonka voit avata käyttämällä hakutoimintoa. Syötä **Tittelit** -sivulle tittelit, joita aiot käyttää töillesi.

## <a name="job-types"></a>Työtyypit
Työtyyppien avulla voi luokitella samankaltaisia töitä. Työtyypit eivät ole pakollisia. Kuitenkin jos aiot käyttää työtyyppejä, kun määrität oikeutussäännöt kompensaationhallintaan, sinun tulee määrittää työtyypit ennen töiden määrittämistä. Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka. Voit ylläpitää työtyyppejä **Työtyypit**-sivulla. Anna **Työtyypit**-sivulla työtyypin nimi ja lyhyt kuvaus. Valitse **Vapautustila**-kentässä jokin seuraavista asetuksista ja ilmaistaksesi Fair Labor Standards Act (FLSA) -vapautustilan tämän työtyypin töille:

-   **Vapautus** – Työt on vapautettu ylitöistä FLSA-säädösten mukaisesti.
-   **Ei vapautusta** – Töitä ei ole vapautettu ylitöistä FLSA-säädösten mukaisesti.
-   **Ei koske** – FLSA-kattavuus ei ole käytössä.

## <a name="job-family"></a>Työluokka
Työluokka on ryhmä samankaltaisia töitä, jotka vaativat samankaltaista koulutusta, taitoja, tietämystä ja osaamista. Työluokka voidaan linkittää työhön **Työt**-sivun **Työn luokittelu** -pikavälilehdestä ja **Kaikki toimet** -sivun **Yleiset**-pikavälilehdestä. Työluokat voivat olla yleisiä tai tarkkoja, riippuen liiketoiminta- ja raportointivaatimuksistasi. Yleisiä työluokkia ovat esimerkiksi **Ammattitaitoiset työt** ja **Ammattitaidottomat työt**. Tarkkoja työluokkia ovat esimerkiksi **Kirjanpito**, **Valmistus** ja **Myynti**.

Ylläpidä työluokkia **Työluokka**-sivulta, jonka voit avata käyttämällä hakutoimintoa. Syötä **Työluokka**-sivulle luokan yksilöivä nimi ja kirjoita yksityiskohtainen kuvaus, jota aiot käyttää töillesi.

## <a name="job-functions"></a>Työtehtävät
Työtehtävät kuvaavat toiminnalliset luokat korkealla tasolla ja yhdistävät korkean tason velvollisuudet. Työtehtävät eivät ole pakollisia. Voit käyttää työtehtäviä yhdessä työtyyppien kanssa suodattaaksesi kompensaatiosuunnitelmia tiettyihin töihin. Voit liittää työtehtävät ja työtyypit kompensaatiosuunnitelmiin määrittämällä oikeutussäännöt **Oikeutussäännöt**-sivulla. Sitten voit liittää kompensaatiosuunnitelmaan tasojoukon, jota käytetään tietyssä oikeutussäännön kautta määritetyssä työtyypin ja -tehtävän yhdistelmässä. (Nämä ominaisuudet koskevat sekä kiinteitä kompensaatiosuunnitelmia että muuttuvia kompensaatiosuunnitelmia). Jos kuitenkin aiot käyttää työtehtäviä, kun määrität oikeutussäännöt kompensaationhallinnalle, sinun tulee määrittää työtehtävät ennen kuin määrität työt. Seuraavassa taulukossa on joitakin esimerkkejä työtehtävistä.

| Työ           | Työtehtävä         |
|---------------|----------------------|
| Myyntipäällikkö | Keskijohdon päällikkö    |
| Kirjanpitäjä    | Ammattilaiset        |

Voit ylläpitää työtehtäviä **Työtehtävät**-sivulla. Anna **Työtehtävät**-sivulla työtehtävän tunnistekoodi ja lyhyt kuvaus.

## <a name="compensation"></a>Kompensaatio
Jos haluat kohdistaa kiinteän kompensaatiosuunnitelman työntekijälle, jolla on toimi työssä, sinun täytyy määrittää työlle kompensaatiotasot. **Kompensaatiotasoa** käytetään, kun vähimmäis-, keskipiste- ja enimmäissummat on määritetty kompensaatiorakenteessa (kompensaatioruudukko). Kun kiinteä kompensaatiosuunnitelma luodaan, kompensaatiorakenne valitaan. Kompensaatiorakenne sisältää myös kompensaatiotason. Kun valitset työntekijälle kiinteää kompensaatiosuunnitelmaa, valittavissa olevat kompensaatiotasot riippuvat työstä, johon työntekijän toimi on liitetty. Lisätietoja kompensaation määrittämisestä on kohdassa [Kompensaatiosuunnitelmat](hr-compensation-overview.md).

## <a name="job-skills"></a>Työ osaamisalueet
Työn osaamisalueet kuvaavat työn suorittamiseen tarvittavia taitoja. Jokaiseen osaamisalueeseen täytyy liittää osaamistaso. Osaamistasot ovat käyttäjien määrittämiä. Ne ilmaisevat osaamisalueen edellyttämän tietämyksen tai osaamisen tason. Yritykset voivat esimerkiksi määrittää numeerisia tasoja, kuten 1–5, jossa **1** tarkoittaa aloittelijaa ja **5** asiantuntijaa. Vaihtoehtoisesti yritykset voivat määrittää tasoja, joilla on otsikot **Aloittelija**, **Keskitaso** tai **Asiantuntija**. Kun osaamistaso on määritetty, myös osaamisen tärkeys voidaan määrittää. Jos esimerkiksi kirjanpitäjältä edellytetään vahvaa tietämystä Microsoft Excelistä, voit luoda osaamisalueen nimeltään **Excel-taidot**. Osaamistasoksi voidaan määrittää **Keskitaso** ja tärkeydeksi voidaan määrittää **Tärkein**.

Työhön sisältyviä osaamisalueita voidaan käyttää osaamisaluekartoituksessa. Osaamisaluekartoitus voi verrata työn edellyttämää osaamisalueiden joukkoa ja työntekijään liittyviä osaamisalueita. Sen jälkeen se voi määrittää vastaavuuden prosentteina yhteensopivien osaamisalueiden perusteella. Lisätietoja osaamisaluekartoituksesta on kohdassa [Osaamisalueiden määrittäminen](hr-develop-skills.md). 

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

## <a name="steps-for-creating-a-job"></a>Työn luontiohjeet
Uuden työn luomisen vaiheittaiset ohjeet löytyvät [Uusien töiden määrittäminen](./hr-personnel-define-jobs.md) -artikkelista. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
