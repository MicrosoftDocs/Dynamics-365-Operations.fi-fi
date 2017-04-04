---
title: "Työajan seuranta vähittäismyynnissä"
description: "Tässä aiheessa kuvataan skenaarioita, jotka tukevat työajan hallinta Microsoft Dynamics-365 työvaiheiden - tuotepaketti."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eac0b85a17df33c860333c5c19d4fb58f160930f
ms.lasthandoff: 03/31/2017


---

# <a name="retail-time-and-attendance"></a>Työajan seuranta vähittäismyynnissä

Tässä aiheessa kuvataan skenaarioita, jotka tukevat työajan hallinta Microsoft Dynamics-365 työvaiheiden - tuotepaketti. 

<a name="manage-worker-setup-and-scheduling"></a>Hallitse työntekijän asennus ja ajoitus
----------------------------------

### <a name="initial-configuration"></a> - alkukokoonpano

-   Suorita ohjattu konfigurointitoiminto.
-   Rekisteröi työntekijät aikakirjausten työntekijöiksi.

### <a name="plan-worker-schedules"></a>Suunnittele työntekijöiden aikatauluja

-   Liitä profiileita työn suunnittelutoiminnon avulla. Lisätietoja on kohdassa <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Tietoja määritysten vaiheista on kohdassa<https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>Vähittäismyynnille ominaiset määritykset

-   Ota toimintoprofiili käyttöön aikamerkinnöissä työntekijöille, joille haluat ottaa käyttöön aikakirjaukset. Valitse **Myyntipisteen Toimintoprofiilit**&gt;**toimintojen**&gt;**POS, kun rekisteröinnit**&gt;**aikarekisteröinnit käyttöön**.
-   Määritä myyntipisteen käyttöoikeudet ottaaksesi käyttöön aikamerkintöjen tarkasteluluvat. Tämä lupa antaa käyttäjälle oikeuden tarkastella muiden saman myymälän työntekijöiden aikakirjauksia, ja lisäksi osoitekirjan kautta muiden myymälöiden, joihin käyttäjä on liitetty. Haluat ehkä myöntää tämän oikeuden päällikköroolille mutta ei kassanhoitajan roolille. Valitse **POS-käyttöoikeusryhmät**&gt;**tarkastella aikamerkinnät**.

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
    -   Jos tarkastelet aikoja eri sijainnista (kassan lokikirjaa varten tai käyttämällä **Näytä aikamerkinnät** -toimintoa päällikköskenaariossa), ja kyseinen sijainti on eri aikavyöhykkeellä, näkemäsi aikamerkinnät muunnetaan paikalliseen aikavyöhykkeeseesi. Esimerkiksi olet esimies kaksi kaupoissa, se, Arizonan ja toinen solmittu. Kassanhoitaja Rekisteröi Saapumisrekisteröinti klo 9:00 -Arizonan. Tuolla hetkellä kello on Nevadassa 8.00. Näin ollen, jos olet Nevadan liikkeessä ja katsot aikakirjaustietueita, kirjaus on merkitty klo 8.00:ksi.

## <a name="view-worker-time-registrations"></a>Näytä työntekijän aikarekisteröinnit
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Näytä työntekijän aikakirjaukset ja suodata myymälän tai tapahtumatyypin perusteella.

Myyntipisteellä:

-   Valitse **Näytä aikamerkinnät**.
-   Näet kaikkien niiden työntekijöiden aikakirjaustapahtumat, jotka on määritetty samoihin myymälöihin kuin sinä.
-   Voit käyttää tehtävätyyppiä ja myymälän suodattimia suodattamaan aikamerkintöjä.

## <a name="process-and-manage-time-registrations"></a>Käsitellä ja hallita aikarekisteröinnit
Dynamics-365 - toimintojen vähittäiskaupan käyttäjä seuraa laskea, hyväksyä ja siirtää palkanlaskennan aikarekisteröinnit työnkulun.

### <a name="primary-operations"></a>Tärkeimmät työvaiheet

-   Laske
-   Hyväksy
-   Lähetä palkanlaskentaan

### <a name="other-common-operations"></a>Muut yleiset toiminnot

-   Joukkopoistuminen
-   Poissaolon kirjaaminen

Saat lisätietoja työajan seurannan kirjausten käsittelystä kohdassa <https://technet.microsoft.com/en-us/library/aa573180.aspx>.


