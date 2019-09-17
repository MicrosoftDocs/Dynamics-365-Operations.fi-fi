---
title: Työpaikkojen luominen, hyväksyminen ja julkaiseminen Attractissa
description: Tässä ohjeaiheessa käsitellään työn elementtejä Attractissa. Siinä käsitellään myös työn luomista.
author: hasrivas
manager: AnnBe
ms.date: 07/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 351fd03f6a27073b850729e2eef5516556292225
ms.sourcegitcommit: b24c36cdd3b6f6085447bf81cb034d13d5b081fe
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/18/2019
ms.locfileid: "1773250"
---
# <a name="create-a-job"></a>Työn luominen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään työn elementtejä Microsoft Dynamics 365 for Talent: Attractissa. Siinä käsitellään myös työn luomista.

## <a name="job-creation"></a>Työn luonti

Järjestelmänvalvojat, työhönottajat ja työhönottopäälliköt voivat luoda työpaikkoja. Kun luot työtä, sinua pyydetään valitsemaan rooli, joka sinulla on prosessissa: työhönottopäällikkö tai työhönottaja. Kun olet valinnut roolin, sinua pyydetään valitsemaan prosessimalli. Jos valitset **Ohita**, oletusmalli on käytössä. Lisätietoja prosessimalleista on kohdassa [Prosessimallin luonti Attractissa](./process-templates-attract.md).

Attractin työ sisältää työn tiedot, työhönottoryhmä, työhönottoprosessi, työpaikkailmoitukset ja analyysin.

## <a name="job-details"></a>Työn tiedot

**Työn tiedot** -välilehdessä on tietoja työn vastuualueista ja määritteistä. Ammattinimikkeen, työnkuvauksen ja työn sijainnin kentät ovat pakollisia. Muut kentät ovat valinnaisia.

**Avoimien paikkojen määrä** -kentän asetuksena on oletusarvoisesti **1**. Voit kuitenkin muuttaa arvon. Kun työpaikkaa varten on valmisteltu tarjous, **Avoimien paikkojen määrä** -kentän arvo pienenee.

Jos toimien hallinta on otettu hallintakeskuksessa käyttöön, **Päivitä toimet** -haku on käytettävissä. Haku lukee Common Data Servicein JobPosition-yksikön ja palauttaa luettelon toimista, jotka työtä varten voidaan valita. Jos valittujen toimien määrä ylittää avoimien paikkojen määrän, saat siitä varoituksen. Saat varoituksen myös silloin, kun toimea käytetään useissa töissä.

> [!NOTE]
> Toimien hallinta sisältyy kattavaan työhönottolaajennukseen.

Työhönottoprosessin tarjoustoiminnon asetusten mukaan toimen numeroa voi olla mahdollista käyttää tarjouksessa kahdesti. Lisätietoja on kohdassa [Työhönottoprosessi](./activities-attract.md).

Attractiin sisältyy oletusjoukko **osaamisalueita**. Näitä osaamisalueita ehdotetaan, kun kirjoitat. Voit lisätä uusia osaamisalueita kirjoittamalla uuden osaamisalueen kenttään ja painamalla Enter-näppäintä.

Attractiin sisältyy oletusjoukko **työtehtäviä**. Voit lisätä enintään kolme uutta työtehtävää kirjoittamalla uuden työtehtävän kenttään ja painamalla sitten Enter-näppäintä.

Attractiin sisältyy oletusjoukko **yrityksen toimialoja**. Voit lisätä enintään kolme uutta yrityksen toimialaa kirjoittamalla uuden yrityksen toimialan kenttään ja painamalla sitten Enter-näppäintä.

## <a name="hiring-team"></a>Työhönottoryhmä

**Työhönottoryhmä**-välilehdessä on luettelo työhön liittyvistä henkilöistä. Kun käyttäjiä lisätään työhönottoryhmään, heille on määritettävä rooli työhönottoryhmässä. Rooli määrittää tiedot, joita käyttäjät saavat käyttää, ja ilmoitukset, joita käyttäjät saavat. Valittavana on seuraavat roolit: **Työhönottaja**, **Työhön ottava esimies**, **Edustaja** ja **Haastattelija**. Lisätietoja roolien käyttöoikeuksista on Roolien hallinta -tiedostossa. Työhönottajat ja työhön ottavat esimiehet voivat nimetä edustajia työskentelemään heidän puolestaan. Lisätietoja edustajista on kohdassa [Suojaus ja roolien hallinta Attractissa](./security-attract.md).

Työhönottoryhmä voidaan päivittää sen jälkeen, kun työ on aktivoitu.

## <a name="process"></a>Prosessoi

Työhönottoprosessin oletustiedot perustuvat prosessimalliin, joka valittiin työtä luotaessa. Jos tiettyä mallia ei valittu tässä vaiheessa, käyttöön otetaan oletusmalli. Kun määrität työhönottoprosessia, voit lisätä tai poistaa eri vaiheita Potentiaalinen ehdokas-, Hakemus- ja Tarjous-vaiheita lukuun ottamatta. Vaikka Potentiaalinen ehdokas -vaihetta ei voi poistaa, sen voi poistaa käytöstä. Voit lisätä tai poistaa kussakin vaiheessa ennalta määritettyjä tehtäviä.

Lisätietoja työhönottoprosessiin lisättävistä tehtävistä on kohdassa [Työhönottoprosessin tehtävät Attractissa](./activities-attract.md).

> [!NOTE]
> Työhönottoprosessia ei voi päivittää sen jälkeen, kun työ on aktivoitu.

## <a name="postings"></a>Kirjaukset

Kun työ on aktivoitu, se voidaan julkaista. Vain työhönottajat ja järjestelmänvalvojat voivat julkaista töitä. Työ voidaan julkaista joko Talent Careers -sivustossa (Microsoft Dynamics 365 for Talentin urasivustossa) tai LinkedInissä. Attract-ryhmä tekee jatkuvasti yhteistyötä työpaikkailmoitussivujen kanssa. Tämä luettelo tulee laajenemaan ajan mittaan. Kun työ on julkaistu vain sisäiseksi, ehdokkailla on oltava AAD-tili, jotta he voivat tarkastella työtä ja hakea sitä. Jos työ on julkinen, ehdokkaat voivat tarkastella ja hakea sitä minkä tahansa todennusvaihtoehdon avulla. 

Lisätietoja työpaikkailmoituksista on kohdassa [Attractin urasivuston toiminnot](career-site.md).

> [!NOTE]
> Työpaikkailmoitustoiminto on käytettävissä vain Attractin kattavan työhönottolaajennusta käytettäessä.

## <a name="activate"></a>Aktivoi

Kun työ on aktivoitu, se voidaan julkaista. Siihen voidaan myös lisätä potentiaalisia ehdokkaita ja hakijoita. Potentiaalisten ehdokkaiden työhön lisäämisen asetus määritetään työhönottoprosessin Potentiaalinen ehdokas -tehtävässä.

> [!NOTE]
> Työhönottoprosessia ei voi päivittää sen jälkeen, kun työ on aktivoitu.

## <a name="prospects-and-applicants"></a>Potentiaaliset ehdokkaat ja hakijat

Potentiaalisten ehdokkaiden työhön lisäämisen asetus määritetään työhönottoprosessin [Potentiaalinen ehdokas -tehtävässä](./activities-attract.md#prospect-activity). Tämä asetus on määritettävä ennen työn aktivointia. Kun työ on aktivoitu, siihen voidaan lisätä potentiaalisia ehdokkaita ja hakijoita.

## <a name="approvals"></a>Hyväksymiset

Attract-työt voidaan lähettää hyväksyttäväksi. Kaikki töihin ei tarvita hyväksyntää. Vaatimus määritetään mallitasolla. Hyväksynnät on oletusarvoisesti poistettu mallissa käytöstä. Voit määrittää hyväksynnän valitsemalla ensin prosessimallin ja määrittämällä sitten **Hyväksyntä**-kentän asetukseksi Oletus. Valitse sitten malli, kun luot työn.

Kun työ on tallennettu, se voidaan lähettää hyväksyttäväksi. Seuraavassa taulukossa on luettelo hyväksyntää käyttävän asiakirjan tiloista.

| Tila   | Alue                                                               |
|----------|---------------------------------------------------------------------|
| Luonnos    | Työ on tallennettu, mutta sitä ei ole vielä lähetetty työnkulkuun. |
| Odottaa  | Työ on lähetetty hyväksyjille.                            |
| Hyväksytty | Työ on hyväksytty, mutta sitä ei ole aktivoitu.            |
| Hylätty | Työ on hylätty eikä sitä voida aktivoida.               |
| Aktiiviset   | Työ on hyväksytty ja aktivoitu.                            |

Voit suodattaa työn tiloja työluettelossa.

Hyväksynnät voidaan lähettää yrityksessä kenelle tahansa Microsoft Azure Active Directoryn (Azure AD) käyttäjälle. Hyväksynnät lähetetään samanaikaisesti kaikille hyväksyjiksi merkityille käyttäjille. Kaikkien hyväksyjien on hyväksyttävä työ, ennen kuin se voidaan siirtää eteenpäin. Jos yksi hyväksyjä hylkää työn, sen tilaksi tulee **Hylätty**. Kun työ on hyväksytty, se voidaan aktivoida.

Jos käyttäjä muokkaa työtä sen jälkeen, kun se on hyväksytty mutta ei aktivoitu, työn tilaksi palautetaan **Luonnos**. Tämän jälkeen työ on lähetettävä uudelleen hyväksyttäväksi. Kun hyväksytty työ on aktivoitu, sitä ei voi enää muokata.

Hyväksyjiksi merkityt henkilöt saavat Attractissa ilmoituksen ja sähköposti-ilmoituksen, jossa kerrotaan, että heillä on hyväksyttävä kohde.  Hyväksyjät voivat valita sähköpostiviestissä olevan linkin, jolloin työ avautuu. He voivat tarkastella tietoja ja joko hyväksyä tai hylätä sen. Kun työn tilaksi on määritetty **Hyväksytty** tai **Hylätty**, lähettäjälle lähetetään ilmoitus Attractissa sekä sähköpostitse. Hyväksyjät saavat myös muistutussähköpostiviestin, jos he eivät vastaa hyväksyntäpyyntöön 24 tunnin kuluessa.

> [!NOTE]
> Voit luoda mukautettuja sähköpostimalleja hyväksyntäsähköposteja varten. Lisätietoja on kohdassa [Sähköpostimallien luominen ja hallinta](https://docs.microsoft.com/dynamics365/unified-operations/talent/email-templates).

## <a name="create-a-job"></a>Työn luominen

Luo työ seuraavien ohjeiden avulla.

1. Valitse **Työt**.
2. Valitse **Uusi**.
3. Kirjoita ammattinimike **Ammattinimike**-kenttään. Ilmoita rooli **Rooli**-kentässä.
4. Valitse malli **Malli**-kentässä. Voit valita myös **Ohita**. Jos valitset **Ohita**, oletusmalliksi määritettyä mallia käytetään.

    Jos asiakirjaan käytetään hyväksyntäprosessia, valitse malli, jossa **Hyväksyntäprosessi**-kentän asetuksena on **Oletus**.

5. Anna **Tiedot**-välilehdessä työn tiedot. **Ammattinimike**-, **Työnkuvaus**- ja **Sijainti**-kentät ovat pakollisia.
6. Valitse **Tallenna**.
7. Lisää **Työhönottoryhmä**-välilehdessä työhön ottava esimies, työhönottaja tai haastattelija.
8. Valitse **Tallenna**.
9. Lisää tai poista tarvittavat vaiheet **Prosessi**-välilehdessä:

    - Lisää vaihe valitsemalla **+ Uusi vaihe**.
    - Poista vaihe pitämällä osoitinta poistettavan vaiheen päällä ja valitse esiin tuleva roskakoripainike.

        > [!NOTE]
        > Potentiaalinen vaihe-, Hakemus- ja Tarjous-vaiheita ei voi poistaa.

10. Lisää tai poista tehtäviä tarpeen mukaan:

    - Voit lisätä tehtävän vetämällä sen oikeaan vaiheeseen oikealla olevassa luettelossa. Vaihtoehtoisesti voit kaksoisnapsauttaa tehtävää ja valita sitten vaiheen, johon se lisätään.
    - Poista tehtävä laajentamalla se ja valitsemalla sitten roskakorikuvake tehtävän ylätunnisteessa.

11. Valitse **Tallenna**.
12. Jos valitsit hyväksyntäprosessin käytön, toimi seuraavasti:

    1. Valitse **+ Lisää hyväksyjä** ja anna sitten käyttäjä, jolla on Azure AD -tili. Voit lisätä useita hyväksyjiä.
    2. Valitse **Lähetä hyväksyjille**.

    Työn **Työn tila** -kentän asetuksena on **Odottaa**. Kun **Työn tila** -kentän arvona on **Hyväksytty**, työ voidaan aktivoida.

13. Aktivoi työ valitsemalla **Aktivoi**.
14. Julkaise työ valitsemalla ensin **Ilmoitukset** ja sitten **Julkaise nyt** Talent Careers -sivustossa tai LinkedInissä.
