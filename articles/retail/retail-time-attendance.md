---
title: Ajan ja läsnäolon hallinta Retailissa
description: Tässä aiheessa on kuvaus Microsoft Dynamics 365 for Retailin ajan ja työajan hallinnassa tuettavista skenaarioista.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 4c54909a02376a62a72a986e634649fa0ae54284
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567950"
---
# <a name="time-and-attendance-management-in-retail"></a>Ajan ja läsnäolon hallinta Retailissa

[!include [banner](includes/banner.md)]

Tässä aiheessa on kuvaus Microsoft Dynamics 365 for Retailin ajan ja työajan hallinnassa tuettavista skenaarioista.

## <a name="manage-worker-setup-and-scheduling"></a>Työntekijän asetusten ja ajoituksen hallinta

### <a name="initial-configuration"></a> - alkukokoonpano

- Suorita ohjattu konfigurointitoiminto.
- Rekisteröi työntekijät aikakirjausten työntekijöiksi.

### <a name="plan-worker-schedules"></a>Suunnittele työntekijöiden aikatauluja

- Liitä profiileita työn suunnittelutoiminnon avulla. Lisätietoja on kohdassa [Profiilien käyttäminen työn suunnittelun avulla](https://technet.microsoft.com/library/aa551234.aspx).

Lisätietoja määritysvaiheista on kohdassa [Työajan seurannan määrittäminen](https://technet.microsoft.com/library/aa496971.aspx).

### <a name="retail-specific-configuration"></a>Vähittäismyynnille ominaiset määritykset

- Ota toimintoprofiili käyttöön aikamerkinnöissä työntekijöille, joille haluat ottaa käyttöön aikakirjaukset. Valitse **Myyntipisteen toimintoprofiilit** &gt; **Toiminnot** &gt; **Myyntipisteen aikakirjaukset** &gt; **Ota käyttöön aikakirjaukset**.
- Määritä myyntipisteen käyttöoikeudet ottaaksesi käyttöön aikamerkintöjen tarkasteluluvat. Tämä lupa antaa käyttäjälle oikeuden tarkastella muiden saman myymälän työntekijöiden aikakirjauksia, ja lisäksi osoitekirjan kautta muiden myymälöiden, joihin käyttäjä on liitetty. Haluat ehkä myöntää tämän oikeuden päällikköroolille mutta ei kassanhoitajan roolille. Valitse **Myyntipisteen käyttöoikeusryhmät** &gt; **Näytä aikamerkinnät**.

## <a name="register-time"></a>Rekisteröi aika

### <a name="cashier-and-non-cashier-time-registrations"></a>Kassanhoitajien ja muiden kuin kassanhoitajien kirjaukset

- Myyntipisteellä:

    - Saapumistoiminnot:

        - Kirjaudu sisään muulla kuin kassatoiminnolla tai Uusi vuoro -toiminnolla.
        - Valitse aikamerkintätoiminto.
        - Valitse haluttu toiminto:

            - Saapuminen
            - Työtauko
            - Lounastauko
            - Poistuminen

        <table>
        <thead>
        <tr>
        <th>Nykyinen tila:</th>
        <th>Käytettävissä olevat toiminnot</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td>Saapuminen</td>
        <td>
        <ul>
        <li>Työtauko</li>
        <li>Lounastauko</li>
        <li>Poistuminen</li>
        </ul>
        </td>
        </tr>
        <tr>
        <td>Työtauko</td>
        <td>Saapuminen</td>
        </tr>
        <tr>
        <td>Lounastauko</td>
        <td>Saapuminen</td>
        </tr>
        <tr>
        <td>Poistuminen</td>
        <td>Saapuminen</td>
        </tr>
        </tbody>
        </table>

        [![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)

- Tarkastele vahvistussanomaa ja vahvista, että nykyinen merkinnän aika on oikea.
- Lokikirja:

    - Valitse **Lokikirja** tarkastellaksesi aikamerkintöjä.
    - Käytä ajan suodattimia eri aikaikkunoiden valitsemiseen.
    - Jos työskentelet useissa myymäläsijainneissa, näet aikakirjauksesi kaikista myymälöistä, joihin sinulle on kirjattu aikaa. Voit käyttää myymäläsuodatinta tarkastellaksesi valitun myymälän aikakirjauksia.

- Eri aikavyöhykkeet:

    - Jos tarkastelet aikoja eri sijainnista (kassan lokikirjaa varten tai käyttämällä **Näytä aikamerkinnät** -toimintoa päällikköskenaariossa), ja kyseinen sijainti on eri aikavyöhykkeellä, näkemäsi aikamerkinnät muunnetaan paikalliseen aikavyöhykkeeseesi. Ajatellaan, että olet kahden myymälän päällikkö, joista toinen sijaitsee Arizonassa ja toinen Nevadassa. Kassa kirjaa saapumisen klo 9:00 Arizonassa. Tuolla hetkellä kello on Nevadassa 8.00. Näin ollen, jos olet Nevadan liikkeessä ja katsot aikakirjaustietueita, kirjaus on merkitty klo 8.00:ksi.

## <a name="view-worker-time-registrations"></a>Työntekijän aikarekisteröintien tarkasteleminen

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Näytä työntekijän aikakirjaukset ja suodata myymälän tai tapahtumatyypin perusteella.

Myyntipisteellä:

- Valitse **Näytä aikamerkinnät**.
- Näet kaikkien niiden työntekijöiden aikakirjaustapahtumat, jotka on määritetty samoihin myymälöihin kuin sinä.
- Voit käyttää tehtävätyyppiä ja myymälän suodattimia suodattamaan aikamerkintöjä.

## <a name="process-and-manage-time-registrations"></a>Aikarekisteröintien käsitteleminen ja hallinta

Dynamics 365 for Retailin käyttäjä noudattaa työnkulkua aikakirjausten laskemiseen, hyväksymiseen ja palkanlaskentaan siirtämiseen.

### <a name="primary-operations"></a>Tärkeimmät työvaiheet

- Laske
- Hyväksy
- Lähetä palkanlaskentaan

### <a name="other-common-operations"></a>Muut yleiset toiminnot

- Joukkopoistuminen
- Poissaolon kirjaaminen

Lisätietoja työajan seurannan rekisteröintien käsittelystä on kohdassa [Työajan seurannan rekisteröintien käsittely](https://technet.microsoft.com/library/aa573180.aspx).
