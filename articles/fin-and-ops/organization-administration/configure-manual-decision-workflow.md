---
title: "Manuaalisten päätösten konfiguroiminen työnkulkuun"
description: "Tässä ohjeaiheessa kerrotaan, miten manuaalisen päätöksen eri ominaisuudet määritetään."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: d09e99a5bf99593a8fa7682f9d4f29eaa4e7c836
ms.contentlocale: fi-fi
ms.lasthandoff: 12/18/2018

---

# <a name="configure-manual-decisions-in-a-workflow"></a>Manuaalisten päätösten konfiguroiminen työnkulkuun

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten manuaalisen päätöksen eri ominaisuudet määritetään.

Manuaalinen päätös konfiguroidaan työnkulkueditorissa napsauttamalla päätöstä hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**, joka avaa **Ominaisuudet**-sivun. Sitten voit määrittää seuraavien ohjeiden avulla manuaalisen päätöksen ominaisuudet.

## <a name="name-the-decision"></a>Päätöksen nimi

Kirjoita näiden ohjeiden avulla nimi manuaaliselle päätökselle.

1. Napsauta vasemmassa ruudussa **Perusasetukset**.
2. Kirjoita manuaalisen päätöksen yksilöivä nimi **Nimi**-kenttään.

## <a name="enter-a-subject-line-and-instructions"></a>Aiherivin ja ohjeiden määrittäminen

Sinun on luotava aiherivi ja ohjeet käyttäjille, jotka on määritetty manuaaliseen päätökseen. Esimerkiksi jos olet konfiguroimassa ostoehdotukselle päätöstä, sille määritetty käyttäjä näkee aiherivin ja ohjeet **Ostoehdotukset**-sivulla. Aiherivi näytetään sivulla olevalla viestirivillä. Käyttäjä voi sitten avata ohjeet napsauttamalla viestirivin kuvaketta. Seuraavia ohjeita noudattamalla voit määrittää aiherivin ja ohjeet.

1. Napsauta vasemmassa ruudussa **Perusasetukset**.
2. Kirjoita aiherivi **Ohjeet**-välilehden **Työnimikkeen aihe** -kenttään.
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

## <a name="specify-the-possible-outcomes-of-a-decision"></a>Määritä päätöksen mahdolliset tulokset

Kun asiakirja määritetään päätöksentekijälle, siihen sisältyy yleensä kysymys, johon päätöksentekijän on vastattava. Kysymyksen vastaus on yleensä **Kyllä** tai **Ei** tai **Tosi** tai **Epätosi**. Noudata seuraavia ohjeita määrittääksesi manuaalisen päätöksen mahdolliset tulokset.

1. Napsauta vasemmassa ruudussa **Perusasetukset**.
2. Valitse **Tulokset**-välilehden **Tulos 1** -kenttään tuloksen nimi tai vaihtoehto.
3. Tulosten käännökset voit lisätä seuraavasti:

    1. Napsauta **Käännökset**-painiketta.
    2. Valitse esiin tulevalla sivulla **Lisää**.
    3. Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.
    4. Kirjota tekstisi **Käännetty teksti** -kenttään.
    5. Valitse **Sulje**.

4. Valitse **Tulos 2** -kenttään tuloksen nimi tai vaihtoehto.
5. Tulosten käännökset voit lisätä seuraavasti:

    1. Napsauta **Käännökset**-painiketta.
    2. Valitse esiin tulevalla sivulla **Lisää**.
    3. Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.
    4. Kirjota tekstisi **Käännetty teksti** -kenttään.
    5. Valitse **Sulje**.

## <a name="specify-when-notifications-are-sent"></a>Määritä, milloin ilmoitukset lähetetään

Voit lähettää käyttäjille ilmoituksia, kun päätös on tehty, delegoitu tai eskaloitu. Toimi seuraavasti määrittääksesi, milloin ilmoitukset lähetetään, ja kenelle ne lähetetään.

1. Valitse vasemmasta ruudusta **Ilmoitukset**.
2. Valitse tapahtuman vieressä oleva valintaruutu, jos haluat lähettää siihen liittyviä ilmoituksia:

    - **\[Vaihtoehto 1\]** – Määritetty käyttäjä on valinnut **\[vaihtoehdon 1\]**.
    - **\[Vaihtoehto 2\]** – Määritetty käyttäjä on valinnut **\[vaihtoehdon 2\]**.
    - **Delegoi** – Määritetty käyttäjä on delegoinut päätöksen toiselle käyttäjälle.
    - **Eskaloi** – Määritetty käyttäjä ei ole tehnyt päätöstä määräajassa.

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
    <td>Tietyt Microsoft Dynamics 365 for Finance and Operations -käyttäjät</td>
    <td>
    <ol>
    <li>Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</li>
    <li><strong>Käytettävissä olevat käyttäjät</strong>: luettelo sisältää kaikki Finance and Operations -käyttäjät. Valitse käyttäjät, joille ilmoituksia lähetetään ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Toista vaiheet 3-7 kullekin tapahtumalle, jonka valitsit vaiheessa 2.

## <a name="assign-a-decision"></a>Määritä päätös

Seuraavia ohjeita noudattamalla voit määrittää käyttäjät, joille manuaalinen päätös määritetään.

1. Valitse vasemmasta ruudusta **Määritys**.
2. Valitse **Määrityksen tyyppi** -välilehdellä jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 3.

    <table>
    <thead>
    <tr>
    <th>Vaihtoehto</th>
    <th>Käyttäjät, joille päätös on määritetty</th>
    <th>Lisävaiheet</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Osallistuja</td>
    <td>Käyttäjät, jotka on määritetty tiettyyn ryhmään tai rooliin</td>
    <td>
    <ol>
    <li>Valittuasi <strong>osallistujan</strong>, valitse <strong>Rooliperustainen</strong>-välilehdellä <strong>Osallistujan tyyppi</strong> -luettelosta ryhmän tai roolin tyyppi, jolle päätös määritetään.</li>
    <li>Valitse <strong>Osallistuja</strong>-luettelosta, ryhmä tai rooli, jolle päätös määritetään.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hierarkia</td>
    <td>Tietyssä organisaatiohierarkiassa olevat käyttäjät</td>
    <td>
    <ol>
    <li>Valittuasi <strong>hierarkian</strong>, valitse <strong>Hierarkian valinta</strong> -välilehdellä <strong>Hierarkian tyyppi</strong> -luettelosta hierarkian tyyppi, jolle päätös määritetään.</li>
    <li>Järjestelmän on noudettava käyttäjien nimijoukko hierarkiasta. Nämä nimet edustavat käyttäjiä, joille päätöksen voi määrittää. Noudata näitä ohjeita määrittääksesi järjestelmän noutamien käyttäjänimien joukon aloituspiste ja lopetuspiste: <ol>
    <li>Määritä aloituspiste valitsemalla henkilö <strong>Alku</strong>-luettelosta.</li>
    <li>Määritä lopetuspiste valitsemalla <strong>Lisää pysäytysehto</strong>. Määritä sitten ehto, joka ilmaisee, missä kohtaa hierarkiaa järjestelmä lopettaa nimien noutamisen.</li>
    </ol>
    </li>
    <li>Määritä <strong>Hierarkian asetukset</strong> -välilehdellä, mille valitun joukon käyttäjille päätös määritetään: <ul>
    <li><strong>Määritä kaikille noudetuille työntekijöille</strong> – Päätös määritetään joukon kaikille käyttäjille.</li>
    <li><strong>Määritä vain viimeksi noudetulle käyttäjälle</strong> – Päätös määritetään vain joukon viimeiselle työntekijälle.</li>
    <li><strong>Jätä pois käyttäjät, joilla on seuraava ehto</strong> – Päätöstä ei liitetä niille joukon käyttäjille, jotka täyttävät määritetyn ehdon. Määritä ehto valitsemalla <strong>Lisää ehto</strong>.</li>
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
    <td>Tietyt Finance and Operations -käyttäjät</td>
    <td>
    <ol>
    <li>Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</li>
    <li><strong>Käytettävissä olevat käyttäjät</strong>: luettelo sisältää kaikki Finance and Operations -käyttäjät. Valitse käyttäjät, joille päätös liitetään ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Jono</td>
    <td>Työnimikejono</td>
    <td>
    <ol>
    <li>Valittuasi <strong>jonon</strong>, napsauta <strong>Jonoperustainen</strong>-välilehteä.</li>
    <li>Voit määrittää päätöksen tiettyyn jonoon seuraavasti: <ol>
    <li>Valitse <strong>Jonon tyyppi</strong> -luettelosta <strong>Työnimikejonot</strong>.</li>
    <li>Valitse jono <strong>Jonon nimi</strong> -luettelosta.</li>
    </ol>
    </li>
    <li>Noudata seuraavia ohjeita, jos haluat, että tietty ehto päättää, mihin jonoon päätös määritetään: <ol>
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

3. Määritä **Aikaraja**-välilehden **Kesto**-kenttään kuinka paljon aikaa käyttäjällä on tehdä päätös. Valitse jompikumpi seuraavista vaihtoehdoista:

    - **Tunnit** – Määritä käyttäjän päätöksentekoaika tunteina. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    - **Päivät** – Määritä käyttäjän päätöksentekoaika päivinä. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    - **Viikot** – Määritä käyttäjän päätöksentekoaika viikkoina.
    - **Kuukaudet** – Valitse päivä ja viikko, johon mennessä käyttäjän tulee tehdä päätös. Voit esimerkiksi määrittää, että käyttäjän tulee tehdä päätös kuukauden kolmannen viikon perjantaihin mennessä.
    - **Vuodet** – Valitse päivä, viikko ja kuukausi, johon mennessä käyttäjän tulee tehdä päätös. Voit esimerkiksi määrittää, että käyttäjän tulee tehdä päätös joulukuun kolmannen viikon perjantaihin mennessä.

    Jos käyttäjä ei tee päätöstä aikarajan puitteissa, päätös on erääntynyt. Erääntyneet päätökset eskaloidaan, sivun **Eskalointi**-alueessa valitsemiesi asetusten mukaan.

## <a name="specify-what-happens-when-a-decision-is-overdue"></a>Erääntyneen päätöksen toimenpiteiden määrittäminen

Jos käyttäjä ei tee päätöstä aikarajan puitteissa, päätös on erääntynyt. Erääntyneen päätöksen voi eskaloida tai määrittää automaattisesti toisen käyttäjän tehtäväksi. Seuraa näitä ohjeita, jos haluat eskaloida erääntyneet päätökset.

1. Valitse vasemmasta ruudusta **Eskalointi**.
2. Luo eskalointipolku valitsemalla **Käytä eskalointipolkua** -valintaruutu. Järjestelmä määrittää päätöksen automaattisesti eskalointipolussa luetelluille käyttäjille. Seuraava taulukko on esimerkki eskalointipolusta.

    | Järjestys | Eskalointipolku            |
    |----------|----------------------------|
    | 1        | Määritä rooliin: Donna           |
    | 2        | Määritä rooliin: Erin            |
    | 3        | Lopullinen toiminto: \[Vaihtoehto 1\] |

    Tässä esimerkissä järjestelmä määrittää erääntyneen päätöksen Donnalle. Jos Donna ei tee päätöstä ajoissa, päätöksenteko määritetään Erinille. Jos Erin ei tee päätöstä ajoissa, järjestelmä valitsee **\[vaihtoehdon 1\]**.

3. Voit lisätä käyttäjän eskalointipolkuun valitsemalla **Lisää eskalaatio**. Valitse jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 4.

    <table>
    <thead>
    <tr>
    <th>Vaihtoehto</th>
    <th>Käyttäjät, joille päätös eskaloidaan</th>
    <th>Lisävaiheet</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hierarkia</td>
    <td>Tietyssä organisaatiohierarkiassa olevat käyttäjät</td>
    <td>
    <ol>
    <li>Valittuasi <strong>hierarkian</strong>, valitse <strong>Hierarkian valinta</strong> -välilehdellä <strong>Hierarkian tyyppi</strong> -luettelosta hierarkian tyyppi, jolle päätös eskaloidaan.</li>
    <li>Järjestelmän on noudettava käyttäjien nimijoukko hierarkiasta. Nämä nimet edustavat käyttäjiä, joille päätöksen voi eskaloida. Noudata näitä ohjeita määrittääksesi järjestelmän noutamien käyttäjänimien joukon aloituspiste ja lopetuspiste: <ol>
    <li>Määritä aloituspiste valitsemalla henkilö <strong>Alku</strong>-luettelosta.</li>
    <li>Määritä lopetuspiste valitsemalla <strong>Lisää pysäytysehto</strong>. Määritä sitten ehto, joka ilmaisee, missä kohtaa hierarkiaa järjestelmä lopettaa nimien noutamisen.</li>
    </ol>
    </li>
    <li>Määritä <strong>Hierarkian asetukset</strong> -välilehdellä, mille valitun joukon käyttäjille päätös eskaloidaan: <ul>
    <li><strong>Määritä kaikille noudetuille työntekijöille</strong> – Päätös eskaloidaan joukon kaikille käyttäjille.</li>
    <li><strong>Määritä vain viimeksi noudetulle käyttäjälle</strong> – Päätös eskaloidaan vain joukon viimeiselle työntekijälle.</li>
    <li><strong>Jätä pois käyttäjät, joilla on seuraava ehto</strong> – Päätöstä ei eskaloida niille joukon käyttäjille, jotka täyttävät määritetyn ehdon. Määritä ehto valitsemalla <strong>Lisää ehto</strong>.</li>
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
    <td>Tietyt Finance and Operations -käyttäjät</td>
    <td>
    <ol>
    <li>Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</li>
    <li><strong>Käytettävissä olevat käyttäjät</strong>: luettelo sisältää kaikki Finance and Operations -käyttäjät. Valitse käyttäjät, joille päätös eskaloidaan ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. Määritä **Aikaraja**-välilehden **Kesto**-kenttään kuinka paljon aikaa käyttäjällä on tehdä päätös. Valitse jompikumpi seuraavista vaihtoehdoista:

    - **Tunnit** – Määritä käyttäjän päätöksentekoaika tunteina. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    - **Päivät** – Määritä käyttäjän päätöksentekoaika päivinä. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    - **Viikot** – Määritä käyttäjän päätöksentekoaika viikkoina.
    - **Kuukaudet** – Valitse päivä ja viikko, johon mennessä käyttäjän tulee tehdä päätös. Voit esimerkiksi määrittää, että käyttäjän tulee tehdä päätös kuukauden kolmannen viikon perjantaihin mennessä.
    - **Vuodet** – Valitse päivä, viikko ja kuukausi, johon mennessä käyttäjän tulee tehdä päätös. Voit esimerkiksi määrittää, että käyttäjän tulee tehdä päätös joulukuun kolmannen viikon perjantaihin mennessä.

5. Toista vaiheet 3 ja 4 jokaiselle käyttäjälle, joka lisätään eskalointipolkuun. Käyttäjien järjestystä voi muuttaa.
6. Jos eskalointipolun käyttäjät eivät tee päätöstä ajoissa, järjestelmä tekee päätöksen automaattisesti. Voit määrittää vaihtoehdon, jonka järjestelmän valitsee valitsemalla **Toiminto**-rivin ja sitten valitsemalla **Lopetustoiminto**-välilehdellä vaihtoehdon.

## <a name="set-a-time-limit"></a>Aikarajan määrittäminen

Noudata seuraavia ohjeita, jos päätös on tehtävä tietyn ajan kuluessa.

> [!NOTE]
> Näiden ohjeiden mukaan valitsemasi asetukset korvaavat asetukset, jotka olet valinnut kunkin hyväksyntävaiheen **Liitos**- ja **Eskalointi**-alueilla.

1. Napsauta vasemmassa ruudussa **Lisäasetukset**.
2. Merkitse **Aseta aikaraja työnkulun elementille** -valintaruutu.
3. Valitse **Kesto**-kenttään, aika, johon mennessä päätös on tehtävä. Valitse jompikumpi seuraavista vaihtoehdoista:

    - **Tunnit** – Anna tuntien määrä. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    - **Päivät** – Anna päivien määrä. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    - **Viikot** – Anna viikkojen määrä.
    - **Kuukaudet** – Valitse päivä ja viikko, johon mennessä päätös on tehtävä. Voit esimerkiksi määrittää, että päätös on tehtävä kuukauden kolmannen viikon perjantaihin mennessä.
    - **Vuodet** – Valitse päivä, viikko ja kuukausi, johon mennessä päätös on tehtävä. Voit esimerkiksi määrittää, että päätös on tehtävä joulukuun kolmannen viikon perjantaihin mennessä.

4. Jos aikaraja ylittyy, järjestelmä tekee päätöksen automaattisesti. Valitse **Toiminto**-luettelosta vaihtoehto, jonka haluat järjestelmän valitsevan.

