---
title: Manuaalisten tehtävien konfiguroiminen työnkulkuun
description: Tässä ohjeaiheessa kerrotaan, miten manuaalisen tehtävän ominaisuudet määritetään.
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2cae815bede98df7e5b937f6ffda99fa4ffed937
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698216"
---
# <a name="configure-manual-tasks-in-a-workflow"></a>Manuaalisten tehtävien konfiguroiminen työnkulkuun

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten manuaalisen tehtävän ominaisuudet määritetään.

Manuaalinen tehtävä konfiguroidaan työnkulkueditorissa napsauttamalla tehtävää hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**, joka avaa **Ominaisuudet**-sivun. Sitten voit määrittää seuraavien ohjeiden avulla manuaalisen tehtävän ominaisuudet.

## <a name="name-the-task"></a>Tehtävän nimeäminen

Kirjoita näiden ohjeiden avulla nimi manuaaliselle tehtävälle.

1. Napsauta vasemmassa ruudussa **Perusasetukset**.
2. Kirjoita tehtävän yksilöivä nimi **Nimi**-kenttään.

## <a name="enter-a-subject-line-and-instructions"></a>Aiherivin ja ohjeiden määrittäminen

Sinun on luotava aiherivi ja ohjeet käyttäjille, jotka on määritetty tähän tehtävään. Esimerkiksi jos olet konfiguroimassa ostoehdotukselle tehtävää, sille määritetty käyttäjä näkee aiherivin ja ohjeet **Ostoehdotukset**-sivulla. Aiherivi näytetään sivulla olevalla viestirivillä. Käyttäjä voi sitten avata ohjeet napsauttamalla viestirivin kuvaketta. Seuraavia ohjeita noudattamalla voit määrittää aiherivin ja ohjeet.

1. Napsauta vasemmassa ruudussa **Perusasetukset**.
2. Kirjoita aiherivi **Työnimikkeen aihe** -kenttään.
3. Voit mukauttaa aiheriviä lisäämällä paikkamerkkejä. Kun käyttäjät tarkastelevat ilmoitusta, paikkamerkit korvataan asianmukaisilla tiedoilla. Paikkamerkkejä voit lisätä seuraavasti:

    1. Napsauta tekstiruudussa kohtaa, johon haluat lisätä paikkamerkin.
    2. Napsauta **Lisää paikkamerkki** -painiketta.
    3. Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.
    4. Valitse **Lisää**.

4. Aiherivin käännökset voit lisätä seuraavasti:

    1. Napsauta **Käännökset**-painiketta.
    2. Valitse esiin tulevalla sivulla **Lisää**.
    3. Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.
    4. Kirjota tekstisi **Käännetty teksti** -kenttään.
    5. Voit mukauttaa tekstiä lisäämällä paikkamerkkejä vaiheen 3 mukaisesti.
    6. Valitse **Sulje**.

5. Kirjoita ohjeet **Työnimikkeen ohjeet** -kenttään.
6. Voit mukauttaa ohjeita lisäämällä paikkamerkkejä. Kun käyttäjät tarkastelevat ohjeita, paikkamerkit korvataan asianmukaisilla tiedoilla. Paikkamerkkejä voit lisätä seuraavasti:

    1. Napsauta tekstiruudussa kohtaa, johon haluat lisätä paikkamerkin.
    2. Napsauta **Lisää paikkamerkki** -painiketta.
    3. Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.
    4. Valitse **Lisää**.

7. Ohjeiden käännökset voit lisätä seuraavasti:

    1. Napsauta **Käännökset**-painiketta.
    2. Valitse esiin tulevalla sivulla **Lisää**.
    3. Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.
    4. Kirjota tekstisi **Käännetty teksti** -kenttään.
    5. Voit mukauttaa tekstiä lisäämällä paikkamerkkejä vaiheen 6 mukaisesti.
    6. Valitse **Sulje**.

## <a name="assign-the-task"></a>Tehtävän määrittäminen

Seuraavia ohjeita noudattamalla voit määrittää käyttäjät, joille manuaalinen tehtävä määritetään.

1. Valitse vasemmasta ruudusta **Määritys**.
2. Valitse **Määrityksen tyyppi** -välilehdellä jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 3.

    <table>
    <thead>
    <tr>
    <th>Vaihtoehto</th>
    <th>Käyttäjät, joille tehtävä on määritetty</th>
    <th>Lisävaiheet</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Osallistuja</td>
    <td>Käyttäjät, jotka on määritetty tiettyyn ryhmään tai rooliin</td>
    <td>
    <ol>
    <li>Valittuasi <strong>osallistujan</strong>, valitse <strong>Rooliperustainen</strong>-välilehdellä <strong>Osallistujan tyyppi</strong> -luettelosta ryhmän tai roolin tyyppi, jolle tehtävä määritetään.</li>
    <li>Valitse <strong>Osallistuja</strong>-luettelosta, ryhmä tai rooli, jolle tehtävä määritetään.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hierarkia</td>
    <td>Tietyssä organisaatiohierarkiassa olevat käyttäjät</td>
    <td>
    <ol>
    <li>Valittuasi <strong>hierarkian</strong>, valitse <strong>Hierarkian valinta</strong> -välilehdellä <strong>Hierarkian tyyppi</strong> -luettelosta hierarkian tyyppi, jolle tehtävä määritetään.</li>
    <li>Järjestelmän on noudettava käyttäjien nimijoukko hierarkiasta. Nämä nimet edustavat käyttäjiä, joille tehtävän voi määrittää. Noudata näitä ohjeita määrittääksesi järjestelmän noutamien käyttäjänimien joukon aloituspiste ja lopetuspiste: <ol>
    <li>Määritä aloituspiste valitsemalla henkilö <strong>Alku</strong>-luettelosta.</li>
    <li>Määritä lopetuspiste valitsemalla <strong>Lisää pysäytysehto</strong>. Määritä sitten ehto, joka ilmaisee, missä kohtaa hierarkiaa järjestelmä lopettaa nimien noutamisen.</li>
    </ol>
    </li>
    <li>Määritä <strong>Hierarkian asetukset</strong> -välilehdellä, mille valitun joukon käyttäjille tehtävä määritetään: <ul>
    <li><strong>Määritä kaikille noudetuille työntekijöille</strong> – Tehtävä määritetään joukon kaikille käyttäjille.</li>
    <li><strong>Määritä vain viimeksi noudetulle käyttäjälle</strong> – Tehtävä määritetään vain joukon viimeiselle työntekijälle.</li>
    <li><strong>Jätä pois käyttäjät, joilla on seuraava ehto</strong> – Tehtävää ei liitetä niille joukon käyttäjille, jotka täyttävät määritetyn ehdon. Määritä ehto valitsemalla <strong>Lisää ehto</strong>.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Työnkulun käyttäjä</td>
    <td>Nykyisen työnkulun käyttäjät</td>
    <td>
    <ul>
    <li>Valittuasi <strong>työnkulun käyttäjän</strong>, valitse <strong>Työnkulun käyttäjä</strong> -välilehdessä <strong>Työnkulun käyttäjä</strong> -luettelosta käyttäjä, joka osallistuu työnkulun.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Käyttäjä</td>
    <td>Tietyt käyttäjät</td>
    <td>
    <ol>
    <li>Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</li>
    <li><strong>Käytettävissä olevat käyttäjät</strong> -luettelo sisältää kaikki käyttäjät. Valitse käyttäjät, joille tehtävä liitetään ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Jono</td>
    <td>Työnimikejono</td>
    <td>
    <ol>
    <li>Valittuasi <strong>jonon</strong>, napsauta <strong>Jonoperustainen</strong>-välilehteä.</li>
    <li>Voit määrittää tehtävän tiettyyn jonoon seuraavasti: <ol>
    <li>Valitse <strong>Jonon tyyppi</strong> -luettelosta <strong>Työnimikejonot</strong>.</li>
    <li>Valitse jono <strong>Jonon nimi</strong> -luettelosta.</li>
    </ol>
    </li>
    <li>Noudata seuraavia ohjeita, jos haluat, että tietty ehto päättää, mihin jonoon tehtävä määritetään: <ol>
    <li>Valitse <strong>Jonon tyyppi</strong> -luettelosta <strong>Ehdolliset työnimikejonot</strong>.</li>
    <li>Valitse <strong>Ehdollinen jono</strong> <strong>Jonon nimi</strong> -luettelosta.</li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] Tätä vaihtoehtoa käytetään vain muutamissa työnkuluissa, kuten Palvelupyynnön hallinnassa.</blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. Määritä **Aikaraja**-välilehden **Kesto**-kenttään kuinka paljon aikaa käyttäjällä on suorittaa tehtävä valmiiksi. Valitse jompikumpi seuraavista vaihtoehdoista:

    - **Tunnit** – Määritä käyttäjän suoritusaika tunteina. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    - **Päivät** – Määritä käyttäjän suoritusaika päivinä. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    - **Viikot** – Määritä käyttäjän suoritusaika viikkoina.
    - **Kuukaudet** – Valitse päivä ja viikko, johon mennessä käyttäjän tulee suorittaa tehtävä valmiiksi. Voit esimerkiksi määrittää, että käyttäjän pitää suorittaa tehtävä kuukauden kolmannen viikon perjantaihin mennessä.
    - **Vuodet** – Valitse päivä, viikko ja kuukausi, johon mennessä käyttäjän tulee suorittaa tehtävä valmiiksi. Voit esimerkiksi määrittää, että käyttäjän pitää suorittaa tehtävä joulukuun kolmannen viikon perjantaihin mennessä.

    Jos käyttäjä ei suorita tehtävää aikarajan puitteissa, tehtävä on erääntynyt. Erääntyneet tehtävät voidaan eskaloida, sivun **Eskalointi**-alueessa valitsemiesi asetusten mukaan.

## <a name="specify-what-happens-when-the-task-is-overdue"></a>Erääntyneen tehtävän toimenpiteiden määrittäminen

Jos käyttäjä ei suorita manuaalista tehtävää aikarajan puitteissa, tehtävä on erääntynyt. Erääntyneen tehtävän voi eskaloida tai määrittää automaattisesti toisen käyttäjän hyväksyttäväksi. Seuraa näitä ohjeita, jos haluat eskaloida erääntyneet tehtävät.

1. Valitse vasemmasta ruudusta **Eskalointi**.
2. Luo eskalointipolku valitsemalla **Käytä eskalointipolkua** -valintaruutu. Järjestelmä määrittää tehtävän automaattisesti eskalointipolussa luetelluille käyttäjille. Seuraava taulukko on esimerkki eskalointipolusta.

    | Järjestys | Eskalointipolku      |
    |----------|----------------------|
    | 1        | Määritä rooliin: Donna     |
    | 2        | Määritä rooliin: Erin      |
    | 3        | Viimeinen toimi: Hylkäys |

    Tässä esimerkissä järjestelmä määrittää erääntyneen tehtävän Donnalle. Jos Donna ei suorita tehtävää ajoissa, tehtävä määritetään Erinille. Jos Erinkään ei suorita tehtävää määräajassa, järjestelmä hylkää käsittelyyn lähetetyn asiakirjaan.

3. Voit lisätä käyttäjän eskalointipolkuun valitsemalla **Lisää eskalaatio**. Valitse **Määrityksen tyyppi** -välilehdellä jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 4.

    <table>
    <thead>
    <tr>
    <th>Vaihtoehto</th>
    <th>Käyttäjät, joille tehtävä eskaloidaan</th>
    <th>Lisävaiheet</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hierarkia</td>
    <td>Tietyssä organisaatiohierarkiassa olevat käyttäjät</td>
    <td>
    <ol>
    <li>Valittuasi <strong>hierarkian</strong>, valitse <strong>Hierarkian valinta</strong> -välilehdellä <strong>Hierarkian tyyppi</strong> -luettelosta hierarkian tyyppi, jolle tehtävä eskaloidaan.</li>
    <li>Järjestelmän on noudettava käyttäjien nimijoukko hierarkiasta. Nämä nimet edustavat käyttäjiä, joille tehtävän voi eskaloida. Noudata näitä ohjeita määrittääksesi järjestelmän noutamien käyttäjänimien joukon aloituspiste ja lopetuspiste: <ol>
    <li>Määritä aloituspiste valitsemalla henkilö <strong>Alku</strong>-luettelosta.</li>
    <li>Määritä lopetuspiste valitsemalla <strong>Lisää pysäytysehto</strong>. Määritä sitten ehto, joka ilmaisee, missä kohtaa hierarkiaa järjestelmä lopettaa nimien noutamisen.</li>
    </ol>
    </li>
    <li>Määritä <strong>Hierarkian asetukset</strong> -välilehdellä, mille valitun joukon käyttäjille tehtävä eskaloidaan: <ul>
    <li><strong>Määritä kaikille noudetuille työntekijöille</strong> – Tehtävä eskaloidaan joukon kaikille käyttäjille.</li>
    <li><strong>Määritä vain viimeksi noudetulle käyttäjälle</strong> – Tehtävä eskaloidaan vain joukon viimeiselle työntekijälle.</li>
    <li><strong>Jätä pois käyttäjät, joilla on seuraava ehto</strong> – Tehtävää ei eskaloida niille joukon käyttäjille, jotka täyttävät määritetyn ehdon. Määritä ehto valitsemalla <strong>Lisää ehto</strong>.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Työnkulun käyttäjä</td>
    <td>Nykyisen työnkulun käyttäjät</td>
    <td>
    <ul>
    <li>Valittuasi <strong>työnkulun käyttäjän</strong>, valitse <strong>Työnkulun käyttäjä</strong> -välilehdessä <strong>Työnkulun käyttäjä</strong> -luettelosta käyttäjä, joka osallistuu työnkulun.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Käyttäjä</td>
    <td>Tietyt käyttäjät</td>
    <td>
    <ol>
    <li>Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</li>
    <li><strong>Käytettävissä olevat käyttäjät</strong> -luettelo sisältää kaikki käyttäjät. Valitse käyttäjät, joille tehtävä eskaloidaan ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. Määritä **Aikaraja**-välilehden **Kesto**-kenttään kuinka paljon aikaa käyttäjällä on suorittaa tehtävä valmiiksi. Valitse jompikumpi seuraavista vaihtoehdoista:

    - **Tunnit** – Määritä käyttäjän suoritusaika tunteina. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    - **Päivät** – Määritä käyttäjän suoritusaika päivinä. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    - **Viikot** – Määritä käyttäjän suoritusaika viikkoina.
    - **Kuukaudet** – Valitse päivä ja viikko, johon mennessä käyttäjän tulee suorittaa tehtävä valmiiksi. Voit esimerkiksi määrittää, että käyttäjän pitää suorittaa tehtävä kuukauden kolmannen viikon perjantaihin mennessä.
    - **Vuodet** – Valitse päivä, viikko ja kuukausi, johon mennessä käyttäjän tulee suorittaa tehtävä valmiiksi. Voit esimerkiksi määrittää, että käyttäjän pitää suorittaa tehtävä joulukuun kolmannen viikon perjantaihin mennessä.

5. Toista vaiheet 3 ja 4 jokaiselle käyttäjälle, joka lisätään eskalointipolkuun. Käyttäjien järjestystä voi muuttaa.
6. Jos eskalointipolun käyttäjät eivät suorita tehtävää ajoissa, järjestelmä suorittaa tehtävän toimenpiteen automaattisesti. Voit määrittää järjestelmän suorittaman toimenpiteen valitsemalla **Toimenpide**-rivin ja sitten valitsemalla **Lopetustoiminto**-välilehdellä toimenpiteen.

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a>Määritä, milloin järjestelmä suorittaa tehtävän toimenpiteen automaattisesti

Voit määrittää järjestelmän tekemään jonkin tietyn toiminnon automaattisesti manuaaliselle tehtävälle, kun määritetyt ehdot täyttyvät. Tehtävä voi esimerkiksi edellyttää, että kuluraporttiosaston jäsen tarkastaa kuitit, jotka lähetetään kuluraportin liitteenä. Yrityksen käytäntöjen mukaan tämä tehtävä on suoritettava, jos kuluraportin kokonaissumma on yli 100 USD. Tässä skenaariossa voit määrittää järjestelmän automaattisesti merkitsemään tehtävän tilaan **Valmis**, kun kokonaissumma on pienempi kuin 100. Noudata seuraavia ohjeita määrittääksesi, milloin järjestelmä suorittaa manuaalisen tehtävän toimenpiteen.

1. Valitse vasemmasta ruudusta **Automaattiset toiminnot**.
2. Merkitse **Ota käyttöön automaattiset toiminnot** -valintaruutu.
3. Valitse **Lisää ehto**.
4. Määritä ehto.
5. Kirjoita kaikki muut tarvittavat ehdot.
6. Voit tarkistaa, onko ehdot määritetty oikein seuraavien ohjeiden avulla:

    1. Valitse **Testi**.
    2. Valitse tietue **Testaa työnkulun ehto** -sivun **Tarkista ehto** -alueella.
    3. Valitse **Testi**. Järjestelmä arvioi, täyttääkö tietue määrittämäsi ehdot.
    4. Palaa **Ominaisuudet**-sivulle valitsemalla **OK** tai **Peruuta**.

7. Valitse **Automaattinen loppuunvientitoiminto**-luettelosta toiminto, jonka haluat järjestelmän suorittavan.

## <a name="specify-when-notifications-are-sent"></a>Määritä, milloin ilmoitukset lähetetään

Voit lähettää käyttäjille ilmoituksia, kun manuaalinen tehtävä on suoritettu, delegoitu, eskaloitu tai hylätty, tai kun muutosta on pyydetty. Toimi seuraavasti määrittääksesi, milloin ilmoitukset lähetetään, ja kenelle ne lähetetään.

1. Valitse vasemmasta ruudusta **Ilmoitukset**.
2. Valitse tapahtuman vieressä oleva valintaruutu, jos haluat lähettää siihen liittyviä ilmoituksia:

    - **Delegoi** – Tehtävä on määritetty toiselle käyttäjälle.
    - **Eskaloi** – Määritetty käyttäjä ei ole suorittanut tehtävää määräajassa.
    - **Valmis** – Määritetty käyttäjä on suorittanut tehtävän.
    - **Hylkää** – Määritetty käyttäjä on hylännyt lähetetyn asiakirjaan.
    - **Pyydä muutosta** – Määritetty käyttäjä on pyytänyt muutosta lähetettyyn asiakirjaan.

3. Valitse sen tapahtuman rivi, jonka valitsit vaiheessa 2.
4. Kirjoita **Ilmoitusteksti**-välilehden tekstiruutuun ilmoituksen leipäteksti.
5. Voit mukauttaa ilmoitusta lisäämällä paikkamerkkejä. Kun käyttäjät tarkastelevat ilmoitusta, paikkamerkit korvataan asianmukaisilla tiedoilla. Paikkamerkkejä voit lisätä seuraavasti:

    1. Napsauta tekstiruudussa kohtaa, johon haluat lisätä paikkamerkin.
    2. Napsauta **Lisää paikkamerkki** -painiketta.
    3. Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.
    4. Valitse **Lisää**.

6. Ilmoitusten käännökset voit lisätä seuraavasti:

    1. Napsauta **Käännökset**-painiketta.
    2. Valitse esiin tulevalla sivulla **Lisää**.
    3. Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.
    4. Kirjota tekstisi **Käännetty teksti** -kenttään.
    5. Voit mukauttaa tekstiä lisäämällä paikkamerkkejä vaiheen 5 mukaisesti.
    6. Valitse **Sulje**.

7. Valitse **Vastaanottaja**-välilehdellä käyttäjät, joille ilmoitukset lähetetään. Valitse jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 8.

    <table>
    <thead>
    <tr>
    <th>Vaihtoehto</th>
    <th>Ilmoituksen vastaanottajat</th>
    <th>Lisävaiheet</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Osallistuja</td>
    <td>Käyttäjät, jotka on määritetty tiettyyn ryhmään tai rooliin</td>
    <td>
    <ol>
    <li>Valittuasi <strong>osallistujan</strong>, valitse <strong>Rooliperustainen</strong>-välilehdellä <strong>Osallistujan tyyppi</strong> -luettelosta ryhmän tai roolin tyyppi, jolle ilmoituksia lähetetään.</li>
    <li>Valitse <strong>Osallistuja</strong>-luettelosta, ryhmä tai rooli, jolle ilmoituksia lähetetään.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Työnkulun käyttäjä</td>
    <td>Nykyisen työnkulun käyttäjät</td>
    <td>
    <ul>
    <li>Valittuasi <strong>työnkulun käyttäjän</strong>, valitse <strong>Työnkulun käyttäjä</strong> -välilehdessä <strong>Työnkulun käyttäjä</strong> -luettelosta käyttäjä, joka osallistuu työnkulun.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Käyttäjä</td>
    <td>Tietyt käyttäjät</td>
    <td>
    <ol>
    <li>Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</li>
    <li><strong>Käytettävissä olevat käyttäjät</strong> -luettelo sisältää kaikki käyttäjät. Valitse käyttäjät, joille ilmoituksia lähetetään ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Toista vaiheet 3-7 kullekin tapahtumalle, jonka valitsit vaiheessa 2.

## <a name="set-a-time-limit"></a>Aikarajan määrittäminen

Noudata seuraavia ohjeita, jos manuaalinen tehtävä on suoritettava tietyn ajan kuluessa.

> [!NOTE]
> Näiden ohjeiden mukaan valitsemasi asetukset korvaavat asetukset, jotka olet valinnut kunkin hyväksyntävaiheen **Liitos**- ja **Eskalointi**-alueilla.

1. Napsauta vasemmassa ruudussa **Lisäasetukset**.
2. Merkitse **Aseta aikaraja työnkulun elementille** -valintaruutu.
3. Valitse **Kesto**-kenttään, aika, johon mennessä tehtävä on suoritettava. Valitse jompikumpi seuraavista vaihtoehdoista:

    - **Tunnit** – Määritä tuntien määrä, jonka aikana tehtävän tulee olla valmis. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    - **Päivät** – Määritä päivien määrä, jonka aikana tehtävän tulee olla valmis. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    - **Viikot** – Määritä viikkojen määrä, jonka aikana tehtävän tulee olla valmis.
    - **Kuukaudet** – Valitse päivä ja viikko, johon mennessä tehtävä on suoritettava. Voit esimerkiksi määrittää, että tehtävä on oltava valmis kuukauden kolmannen viikon perjantaihin mennessä.
    - **Vuodet** – Valitse päivä, viikko ja kuukausi, johon mennessä tehtävän tulee olla valmis. Voit esimerkiksi määrittää, että tehtävän on oltava valmis joulukuun kolmannen viikon perjantaihin mennessä.

4. Jos aikaraja ylittyy, järjestelmä suorittaa automaattisesti tehtävälle toiminnon. Valitse **Toiminto**-luettelosta toiminto, jonka haluat järjestelmän suorittavan.

## <a name="specify-which-actions-are-available-to-the-user"></a>Määritä käyttäjän käytettävissä olevat toiminnot

Kun manuaalinen tehtävä on määritetty käyttäjälle, käyttäjän pitää suorittaa tehtävälle toiminto. Noudata seuraavia ohjeita määrittääksesi, mitä toimintoja käyttäjät voivat tehdä tehtävälle.

> [!NOTE]
> Käytettävissä olevat toiminnot vaihtelevat sen mukaan, miten tehtävä on suunniteltu.

1. Napsauta vasemmassa ruudussa **Lisäasetukset**.
2. Valitse **Valmis**-valintaruutu, jos haluat, että käyttäjä voi merkitä tehtävän **valmiiksi**.
3. Valitse **Hylkää** -valintaruutu, jos haluat, että käyttäjä voi hylätä lähetetyn asiakirjan.
4. Valitse **Pyydä muutosta** -valintaruutu, jos haluat, että käyttäjä voi pyytää muutosta lähetettyyn asiakirjaan.
5. Valitse **Delegoi**-valintaruutu, jos haluat, että käyttäjä voi määrittää tehtävän toiselle käyttäjälle.
6. Valitse **Määritä uudelleen**-valintaruutu, jos haluat, että käyttäjä voi määrittää tehtävän uudelleen toiselle käyttäjälle työnimikejonossa.
7. Valitse **Vapauta**-valintaruutu, jos haluat, että käyttäjä voi vapauttaa tehtävän työnimikejonoon. Toinen käyttäjä voi sitten suorittaa tehtävän.
