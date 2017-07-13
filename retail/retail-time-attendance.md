---
title: "Työajan seuranta vähittäismyynnissä"
description: "Tässä aiheessa on kuvaus vähittäismyynnin ajan ja työajan hallinnassa tuettavista skenaarioista Microsoft Dynamics 365 for Retailissa."
author: MargoC
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: b458d1938f49a2f33f7dd3ce3062880f0d4d7bfc
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017



---

# Vähittäismyynnin työajan seuranta
<a id="retail-time-and-attendance" class="xliff"></a>

[!include[banner](includes/banner.md)]


Tässä aiheessa on kuvaus vähittäismyynnin ajan ja työajan hallinnassa tuettavista skenaarioista Microsoft Dynamics 365 for Retailissa. 

Työntekijän asetusten ja ajoituksen hallinta
<a id="manage-worker-setup-and-scheduling" class="xliff"></a>
----------------------------------

###  - alkukokoonpano
<a id="initial-configuration" class="xliff"></a>

-   Suorita ohjattu konfigurointitoiminto.
-   Rekisteröi työntekijät aikakirjausten työntekijöiksi.

### Suunnittele työntekijöiden aikatauluja
<a id="plan-worker-schedules" class="xliff"></a>

-   Liitä profiileita työn suunnittelutoiminnon avulla. Lisätietoja on kohdassa <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Tietoja määritysten vaiheista on kohdassa<https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### Vähittäismyynnille ominaiset määritykset
<a id="retail-specific-configuration" class="xliff"></a>

-   Ota toimintoprofiili käyttöön aikamerkinnöissä työntekijöille, joille haluat ottaa käyttöön aikakirjaukset. Valitse **Myyntipisteen toimintoprofiilit** &gt; **Toiminnot** &gt; **Myyntipisteen aikakirjaukset** &gt; **Ota käyttöön aikakirjaukset**.
-   Määritä myyntipisteen käyttöoikeudet ottaaksesi käyttöön aikamerkintöjen tarkasteluluvat. Tämä lupa antaa käyttäjälle oikeuden tarkastella muiden saman myymälän työntekijöiden aikakirjauksia, ja lisäksi osoitekirjan kautta muiden myymälöiden, joihin käyttäjä on liitetty. Haluat ehkä myöntää tämän oikeuden päällikköroolille mutta ei kassanhoitajan roolille. Valitse **Myyntipisteen käyttöoikeusryhmät** &gt; **Näytä aikamerkinnät**.

## Rekisteröi aika
<a id="register-time" class="xliff"></a>
### Kassanhoitajien ja muiden kuin kassanhoitajien kirjaukset
<a id="cashier-and-non-cashier-time-registrations" class="xliff"></a>

-   Myyntipisteellä:
    -   Saapumistoiminnot:
        -   Kirjaudu sisään muulla kuin kassatoiminnolla tai Uusi vuoro -toiminnolla.
        -   Valitse aikamerkintätoiminto.
        -   Valitse haluttu toiminto:
            -   Saapuminen
            -   Työtauko
            -   Lounastauko
            -   Poistuminen

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Nykyinen tila:</th>
    <th>Käytettävissä olevat toiminnot</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Saapuminen</td>
    <td><ul>
    <li>Työtauko</li>
    <li>Lounastauko</li>
    <li>Poistuminen</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Työtauko</td>
    <td>Saapuminen</td>
    </tr>
    <tr class="odd">
    <td>Lounastauko</td>
    <td>Saapuminen</td>
    </tr>
    <tr class="even">
    <td>Poistuminen</td>
    <td>Saapuminen</td>
    </tr>
    </tbody>
    </table>

    [![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)
-   Tarkastele vahvistussanomaa ja vahvista, että nykyinen merkinnän aika on oikea.
-   Lokikirja:
    -   Valitse **Lokikirja** tarkastellaksesi aikamerkintöjä.
    -   Käytä ajan suodattimia eri aikaikkunoiden valitsemiseen.
    -   Jos työskentelet useissa myymäläsijainneissa, näet aikakirjauksesi kaikista myymälöistä, joihin sinulle on kirjattu aikaa. Voit käyttää myymäläsuodatinta tarkastellaksesi valitun myymälän aikakirjauksia.

<!-- -->

-   Eri aikavyöhykkeet:
    -   Jos tarkastelet aikoja eri sijainnista (kassan lokikirjaa varten tai käyttämällä **Näytä aikamerkinnät** -toimintoa päällikköskenaariossa), ja kyseinen sijainti on eri aikavyöhykkeellä, näkemäsi aikamerkinnät muunnetaan paikalliseen aikavyöhykkeeseesi. Ajatellaan, että olet kahden myymälän päällikkö, joista toinen sijaitsee Arizonassa ja toinen Nevadassa. Kassa kirjaa saapumisen klo 9:00 Arizonassa. Tuolla hetkellä kello on Nevadassa 8.00. Näin ollen, jos olet Nevadan liikkeessä ja katsot aikakirjaustietueita, kirjaus on merkitty klo 8.00:ksi.

## Työntekijän aikarekisteröintien tarkasteleminen
<a id="view-worker-time-registrations" class="xliff"></a>
### Näytä työntekijän aikakirjaukset ja suodata myymälän tai tapahtumatyypin perusteella.
<a id="view-worker-time-registrations-and-filter-by-store-or-activity-type" class="xliff"></a>

Myyntipisteellä:

-   Valitse **Näytä aikamerkinnät**.
-   Näet kaikkien niiden työntekijöiden aikakirjaustapahtumat, jotka on määritetty samoihin myymälöihin kuin sinä.
-   Voit käyttää tehtävätyyppiä ja myymälän suodattimia suodattamaan aikamerkintöjä.

## Aikarekisteröintien käsitteleminen ja hallinta
<a id="process-and-manage-time-registrations" class="xliff"></a>
A Dynamics 365 for Retail -käyttäjä noudattaa työnkulkua aikakirjausten laskemiseen, hyväksymiseen ja palkanlaskentaan siirtämiseen.

### Tärkeimmät työvaiheet
<a id="primary-operations" class="xliff"></a>

-   Laske
-   Hyväksy
-   Lähetä palkanlaskentaan

### Muut yleiset toiminnot
<a id="other-common-operations" class="xliff"></a>

-   Joukkopoistuminen
-   Poissaolon kirjaaminen

Saat lisätietoja työajan seurannan kirjausten käsittelystä kohdassa <https://technet.microsoft.com/en-us/library/aa573180.aspx>.




