---
title: Attractin urasivuston toiminnot
description: Tässä ohjeaineessa on Attractin ehdokkaalle tarkoitetun urasivustotoimintojen yleiskatsaus.
author: hasrivas
manager: AnnBe
ms.date: 03/20/2019
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
ms.author: hasrivas
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: a56f162ccc6b6099fd62e0cb7e10076368d8e653
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517939"
---
# <a name="career-site-functionality-in-attract"></a>Attractin urasivuston toiminnot

[!include[banner](../includes/banner.md)]

Tässä ohjeaineessa on Microsoft Dynamics 365 for Talent: Attractin ehdokkaalle tarkoitetun urasivustotoimintojen yleiskatsaus. Siinä käsitellään myös toiminnon määrittäminen.

Attractissa on yksi urasivusto vuokraajan kullekin ympäristölle. Jos organisaatiossa on esimerkiksi kehitysympäristö ja testiympäristö, sekä kehitys- että testiympäristölle valmistellaan oma urasivusto. Kumpikin urasivusto on täysin eristetty ja kummassakin oma todennusmekanismi. Urasivustot eivät jaa töitä eivätkä hakijaprofiileja keskenään.

Urasivusto on oletusarvoisesti julkinen. Niinpä hakijat voivat tarkastella kaikki ulkoiseksi merkittyjä töitä ilman kirjautumista. Kaikkia muita toimintoja varten hakijoiden on kuitenkin kirjauduttava sisään.

## <a name="career-site-management"></a>Urasivuston hallinta

Voit määrittää seuraavat kohdat kirjautumalla järjestelmänvalvojana Attractiin ja valitsemalla ensin **Asetukset**-valikossa (hammasrataskuvake) **Hallintakeskus** ja sitten **Yrityksen tiedot** -välilehden.

-   **Organisaation nimi** – Organisaation nimi näkyy siirtymispalkissa urasivuston yläosassa. Valitsemalla organisaation nimet hakijat voivat siirtyä sivulle, jossa on luettelo avoimista työpaikoista.

-   **Organisaation logo** – Organisaation logo näkyy urasivuston vasemmassa yläkulmassa. Valitsemalla organisaation logon hakijat voivat siirtyä sivulle, jossa on luettelo avoimista työpaikoista.

    > [!NOTE] 
    > Urasivustossa näkyvän logon korkeus on aina 20 kuvapistettä (px). Hallintakeskukseen lisätty kuva sovitetaan oikean kokoiseksi. Tämän vuoksi kuvan leveys voi muuttua.
 
Voit määrittää seuraavat kohdat kirjautumalla järjestelmänvalvojana Attractiin ja valitsemalla ensin **Asetukset**-valikossa **Hallintakeskus** ja sitten **Urasivuston hallinta** -välilehden.

-   **Hakukoneoptimointi** – Kun otettu käyttöön, kaikkia Attractin urasivustossa julkaistuja julkisia työpaikkoja voi hakea hakukoneilla, kuten Bingillä ja Googlella.

    > [!NOTE] 
    > Tämän asetuksen käyttöönottamisessa ja hakutulosten näkymisessä voi olla viive, joka määräytyy käytetyn hakukoneen mukaan.
         
## <a name="career-site-urls"></a>Urasivuston URL-osoitteet

Seuraavassa luettelossa on yleisesti käytettyjen urasivustojen URL-osoitteita ja ohjeita niiden käyttämiseen.

-   **Urasivuston aloitussivun URL-osoite** – voit tarkastella urasivuston aloitussivun URL-osoitetta kirjautumalla Attractiin järjestelmänvalvojana, valitsemalla **Hallintakeskus** **Asetukset**-valikossa ja valitsemalla sitten **Urasivuston hallinta** -välilehden.

-   **Yksittäisen työpaikkailmoituksen käyttämisen URL-osoite** – Kun [teet ulkoisen työpaikkailmoituksen](Creating-jobs-Attract.md#postings) ensimmäisen kerran, voit kopioida **Käytä**-linkin Attract-sovelluksesta. Tämän linkin URL-osoitteen muoto on seuraavanlainen: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)

-   **Yksittäisen työpaikkailmoituksen URL-osoite** – Työpaikkailmoituksen URL-osoite on käytön URL-osoitteen alimerkkijono. Se sisältää työnumerosta oikealle kaikki merkkijonon tiedot. Niinpä edellisessä Käytä-linkin URL-osoitteessa työpaikkailmoituksen URL-osoite on [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e).

## <a name="authentication-options"></a>Todennusasetukset

Hakijat voivat kirjautua Attract-urasivustoon seuraavin tavoin:

-   Henkilökohtainen tili:

    -   LinkedIn

    -   Microsoft

    -   Google

    -   Facebook

-   Työ- tai opiskelijatili:

    -   Microsoft Azure Active Directory (Azure AD)

Azure AD -kirjautuminen on tarkoitettu vain sisäisille hakijoille. Tämän vuoksi vain yrityksen Azure AD -tunnistetietoja käyttävät sisäiset hakijat voivat käyttää tätä vaihtoehtoa. Esimerkiksi hakija, joka on tällä hetkellä Contoso Ltd:n työntekijä, halua hakea töitä Alpine Ski Housesta, joka on erillinen yritys. Kirjautuminen ei tässä tapauksessa onnistu, jos työntekijä yrittää käyttää Contoso Ltd:n Azure AD -tunnistetietoja. 

Ehdokkaiden on kirjauduttava sisään käyttämällä Azure AD:ta, jos työ, jota he tarkastelevat tai johon he hakevat, on merkitty vain sisäiseksi.

## <a name="create-and-maintain-a-profile"></a>Profiilin luominen ja ylläpitäminen

Kun hakijat ovat kirjautuneet urasivustoon, he voivat luoda profiilin ja ylläpitää sitä valitsemalla sivun yläosan siirtymispalkissa **Oma profiili**.
Profiili sisältää henkilötiedot, tietoja työkokemuksesta ja koulutuksesta sekä asiakirjoja, linkkejä ja tietoja osaamisalueista. Kun profiili on luotu, sen avulla voi hakea työpaikkoja, joista hakija on kiinnostunut. Lisäksi Attract voi suositella profiilien avulla hakijoille sopivia työpaikkoja.

> [!NOTE]
> Jos hakija kirjautuu johonkin edellä mainittuun todennuspalveluun sähköpostitunnuksella, kyseinen sähköpostitunnus muuttuu oletusarvoisesti profiiliin liitetyksi yhteyshenkilön sähköpostitunnukseksi. Jälkimmäinen voidaan kuitenkin muuttaa ja on täysin erillinen edellisestä. Attract liittää aina profiilin kaikkeen sähköpostiviestintään yhteyshenkilön sähköpostitunnuksen avulla.

## <a name="find-the-right-job"></a>Oikean työpaikan etsiminen

Hakijat voivat hakea tiettyä työpaikkaa työluettelosivulla hakuehtojen avulla. Hakutoiminto hakee tiettyjä sanoja työnimikkeistä ja työnkuvauksista sekä näyttää sopivat työpaikat tuloksina. Hakijat voivat suodattaa tuloksia koska tahansa työn sijainnin tai työtehtävän perusteella.

Hakijat voivat tarkastella urasivustossa myös suositeltuja työpaikkoja. Hakijalle suositellaan työpaikkoja hakijan aiempien hakemusten, profiilin ja ansioluetteloiden perusteella.

> [!NOTE] 
> Työpaikkasuositukset näytetään vain, jos urasivustossa on julkaista vähintään 10 työpaikkaa ja jos hakija on täyttänyt profiilitiedot.

Sisäiset ehdokkaat voivat myös tarkastella, kuka työhön ottava esimies ja/tai muu työhönottaja on, jos he haluavat ottaa yhteyttä työhönottoryhmän jäseniin. Ulkoisilla ehdokkailla ei kuitenkaan ole mahdollisuutta tarkastella minkään työn työhönottoryhmän jäsenten tietoja.

## <a name="contact-the-hiring-team"></a>Ota yhteyttä työhönottoryhmään
Vain sisäiset ehdokkaat voivat ottaa yhteyttä työhönottoryhmään. Tämä rajoitus koskee kaikkia töitä, niin sisäisiä kuin julkisiakin.

Ehdokkaat voivat haluta ottaa yhteyden työhönottoryhmään ja ilmaista kiinnostuksensa ilmoitettua työtä kohtaan tai kysyä siitä lisätietoja. He voivat ottaa yhteyttä keneen tahansa luettelossa olevaan työhönottoryhmän jäseneen (työhön ottava esimies tai muut työhönottajat). Vaihtoehtoisesti he voivat myös liittää viestiin ansioluettelon tai valita olemassa olevan ansioluettelon, joka on ladattu aikaisemmin profiilin osana.

Kun sisäinen hakija valitsee työhönottoryhmän jäseniä yhteydenottoa varten, Attract lähettää sähköpostiviestin näille henkilöille ehdokkaan puolesta. Samaan aikaan ehdokkaan profiili lisätään **Prospekti**-vaiheeseen, jos tämä vaihe on käytettävissä työhön liittyen. Valitse **Prospekti**-vaiheessa työhön ottavat esimiehet tai muut työhönottajat, jotka voivat tarkastella heihin yhteyttä ottaneiden ehdokkaiden tietoja. He voivat myös tarkastella ehdokkaiden profiileja ja kutsua mahdollisia ehdokkaita hakemaan työtä.

Ehdokkaat voivat hakea töitä, joihin liittyen he ovat jo ottaneet yhteyttä työhön ottaviin esimiehiin. Kun he hakevat työtä, ehdokkaat eivät enää voi ottaa yhteyttä työhön ottavaan esimieheen urasivuston kautta.

## <a name="apply-for-jobs"></a>Työpaikkojen hakeminen

Kun hakija löytää oikean työpaikan, sitä voi hakea **Työn tiedot** -sivun **Hae** painikkeella. Hakijat voivat tässä vaiheessa joko luoda uuden profiilin tai tarkistaa aiemmin luodun profiilin tiedot.
Hakija voi myös tarvittaessa ladata ansioluettelon ja lähettää sitten työhakemuksen.

### <a name="enable-applying-for-jobs-with-linkedin-profiles"></a>Otetaan käyttöön töiden hakeminen LinkedIn-profiilien avulla

Voit auttaa ehdokkaita hakemaan toimia määrittämällä Attractin niin, että se sallii ehdokkaiden hakea töitä LinkedInin kautta.

> [!NOTE] 
> LinkedInissä on oltava vähintään yksi työhönottajan käyttöoikeus, ennen kuin ehdokkaiden voi antaa hakea töitä LinkedInin avulla.

1. Kirjaudu Attractiin järjestelmänvalvojana.
2. Valitse **Asetukset**-painike (rataskuvake) sivun oikeassa yläkulmassa ja valitse sitten **Hallintakeskus**.
3. Valitse **LinkedIn-integrointi**-välilehti ja muodosta yhteys LinkedInin työhönottajan tiliin.
4. Valitse **LinkedIn Recruiter System Connect -integrointi** -osassa **Käytössä** **Hae LinkedInin kautta** -asetusta varten.

Kun olet ottanut asetuksen käyttöön, ehdokkaat voivat hakea käyttämällä olemassa olevan LinkedIn-profiilin tietojen avulla. Kun ehdokkaat hakevat töitä valitsemalla **Hae LinkedInin kautta** -painikkeen, heitä pyydetään tekemään todennus LinkedInin avulla, jos he eivät ole kirjautuneena sisään. Kun he ovat tehneet todennuksen, LinkedIn-profiili korvaa aiemmin määritetyt profiilin tiedot hakemuksen sivulla. Ehdokkaat voivat muokata tietoja tarvittaessa. Tämän jälkeen he voivat lähettää sovelluksen. Jos ehdokas siirtyy pois sivulta eikä hae työtä, heidän profiilinsa tietoja ei päivitetä Attractiin.

## <a name="check-application-status"></a>Hakemuksen tilan tarkistaminen

Kun hakija on hakenut yhtä tai useaa työpaikkaa, hän voi tarkastella avoimia ja suljettuja hakemuksia valitsemalla sivun yläosan siirtymispalkissa **Hakemukset**. Kun hakija avaa jonkin hakemuksensa, näkyviin tulee hakemuksen nykyinen tila ja mahdolliset odottavat toiminnot, jotka hakijan on tehtävä. Jos hakijan on esimerkiksi annettava mahdolliset päivämäärät henkilökohtaista haastattelua varten, käytettävissä olevat vaihtoehdot näkyvät sivulla.

## <a name="internal-jobs"></a>Sisäiset työpaikat

Tällä hetkellä sisäisiksi merkityt Attractin urasivustoon julkaistut työt eivät näy urasivustossa. Niitä voi käyttää vain avaamalla suoran **Käytä**-linkin URL-osoitteen, joka voidaan kopioida Attract-sovelluksesta.
