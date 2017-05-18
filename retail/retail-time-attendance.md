---
title: "Työajan seuranta vähittäismyynnissä"
description: "Tässä aiheessa on kuvaus vähittäismyynnin ajan ja työajan hallinnassa tuettavista skenaarioista Microsoft Dynamics 365 for Operations - Retailissa."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: f256839e1fad810e24d2ed95a933fbeacee4722b
ms.contentlocale: fi-fi
ms.lasthandoff: 04/26/2017


---

# <a name="retail-time-and-attendance"></a>Työajan seuranta vähittäismyynnissä

[!include[banner](includes/banner.md)]


Tässä aiheessa on kuvaus vähittäismyynnin ajan ja työajan hallinnassa tuettavista skenaarioista Microsoft Dynamics 365 for Operations - Retailissa. 

<a name="manage-worker-setup-and-scheduling"></a>Työntekijän asetusten ja ajoituksen hallinta
----------------------------------

### <a name="initial-configuration"></a> - alkukokoonpano

-   Suorita ohjattu konfigurointitoiminto.
-   Rekisteröi työntekijät aikakirjausten työntekijöiksi.

### <a name="plan-worker-schedules"></a>Suunnittele työntekijöiden aikatauluja

-   Liitä profiileita työn suunnittelutoiminnon avulla. Lisätietoja on kohdassa <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Tietoja määritysten vaiheista on kohdassa<https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>Vähittäismyynnille ominaiset määritykset

-   Ota toimintoprofiili käyttöön aikamerkinnöissä työntekijöille, joille haluat ottaa käyttöön aikakirjaukset. Valitse **Myyntipisteen toimintoprofiilit** &gt; **Toiminnot** &gt; **Myyntipisteen aikakirjaukset** &gt; **Ota käyttöön aikakirjaukset**.
-   Määritä myyntipisteen käyttöoikeudet ottaaksesi käyttöön aikamerkintöjen tarkasteluluvat. Tämä lupa antaa käyttäjälle oikeuden tarkastella muiden saman myymälän työntekijöiden aikakirjauksia, ja lisäksi osoitekirjan kautta muiden myymälöiden, joihin käyttäjä on liitetty. Haluat ehkä myöntää tämän oikeuden päällikköroolille mutta ei kassanhoitajan roolille. Valitse **Myyntipisteen käyttöoikeusryhmät** &gt; **Näytä aikamerkinnät**.

## <a name="register-time"></a>Rekisteröi aika
### <a name="cashier-and-non-cashier-time-registrations"></a>Kassanhoitajien ja muiden kuin kassanhoitajien kirjaukset

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

## <a name="view-worker-time-registrations"></a>Työntekijän aikarekisteröintien tarkasteleminen
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Näytä työntekijän aikakirjaukset ja suodata myymälän tai tapahtumatyypin perusteella.

Myyntipisteellä:

-   Valitse **Näytä aikamerkinnät**.
-   Näet kaikkien niiden työntekijöiden aikakirjaustapahtumat, jotka on määritetty samoihin myymälöihin kuin sinä.
-   Voit käyttää tehtävätyyppiä ja myymälän suodattimia suodattamaan aikamerkintöjä.

## <a name="process-and-manage-time-registrations"></a>Aikarekisteröintien käsitteleminen ja hallinta
A Dynamics 365 for Operations - Retail -käyttäjä noudattaa työnkulkua aikakirjausten laskemiseen, hyväksymiseen ja palkanlaskentaan siirtämiseen.

### <a name="primary-operations"></a>Tärkeimmät työvaiheet

-   Laske
-   Hyväksy
-   Lähetä palkanlaskentaan

### <a name="other-common-operations"></a>Muut yleiset toiminnot

-   Joukkopoistuminen
-   Poissaolon kirjaaminen

Saat lisätietoja työajan seurannan kirjausten käsittelystä kohdassa <https://technet.microsoft.com/en-us/library/aa573180.aspx>.




