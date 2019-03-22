---
title: Attractin urasivuston toiminnot
description: Tässä ohjeaineessa on Attractin ehdokkaalle tarkoitetun urasivustotoimintojen yleiskatsaus.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/13/2019
ms.locfileid: "389960"
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

    >   [!NOTE] 
    >   Urasivustossa näkyvän logon korkeus on aina 20 kuvapistettä (px). Hallintakeskukseen lisätty kuva sovitetaan oikean kokoiseksi. Tämän vuoksi kuvan leveys voi muuttua.
 
Voit määrittää seuraavat kohdat kirjautumalla järjestelmänvalvojana Attractiin ja valitsemalla ensin **Asetukset**-valikossa **Hallintakeskus** ja sitten **Urasivuston hallinta** -välilehden.

-   **Hakukoneoptimointi** – Kun otettu käyttöön, kaikkia Attractin urasivustossa julkaistuja julkisia työpaikkoja voi hakea hakukoneilla, kuten Bingillä ja Googlella.

    >   [!NOTE] 
    >   Tämän asetuksen käyttöönottamisessa ja hakutulosten näkymisessä voi olla viive, joka määräytyy käytetyn hakukoneen mukaan.
         
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

## <a name="create-and-maintain-a-profile"></a>Profiilin luominen ja ylläpitäminen

Kun hakijat ovat kirjautuneet urasivustoon, he voivat luoda profiilin ja ylläpitää sitä valitsemalla sivun yläosan siirtymispalkissa **Oma profiili**.
Profiili sisältää henkilötiedot, tietoja työkokemuksesta ja koulutuksesta sekä asiakirjoja, linkkejä ja tietoja osaamisalueista. Kun profiili on luotu, sen avulla voi hakea työpaikkoja, joista hakija on kiinnostunut. Lisäksi Attract voi suositella profiilien avulla hakijoille sopivia työpaikkoja.

>   [!NOTE]
>   Jos hakija kirjautuu johonkin edellä mainittuun todennuspalveluun sähköpostitunnuksella, kyseinen sähköpostitunnus muuttuu oletusarvoisesti profiiliin liitetyksi yhteyshenkilön sähköpostitunnukseksi. Jälkimmäinen voidaan kuitenkin muuttaa ja on täysin erillinen edellisestä. Attract liittää aina profiilin kaikkeen sähköpostiviestintään yhteyshenkilön sähköpostitunnuksen avulla.

## <a name="find-the-right-job"></a>Oikean työpaikan etsiminen

Hakijat voivat hakea tiettyä työpaikkaa työluettelosivulla hakuehtojen avulla. Hakutoiminto hakee tiettyjä sanoja työnimikkeistä ja työnkuvauksista sekä näyttää sopivat työpaikat tuloksina. Hakijat voivat suodattaa tuloksia koska tahansa työn sijainnin tai työtehtävän perusteella.

Hakijat voivat tarkastella urasivustossa myös suositeltuja työpaikkoja. Hakijalle suositellaan työpaikkoja hakijan aiempien hakemusten, profiilin ja ansioluetteloiden perusteella.

>   [!NOTE] 
>   Työpaikkasuositukset näytetään vain, jos urasivustossa on julkaista vähintään 10 työpaikkaa ja jos hakija on täyttänyt profiilitiedot.

## <a name="apply-for-jobs"></a>Työpaikkojen hakeminen

Kun hakija löytää oikean työpaikan, sitä voi hakea **Työn tiedot** -sivun **Käytä**-painikkeella. Hakijat voivat tässä vaiheessa joko luoda uuden profiilin tai tarkistaa aiemmin luodun profiilin tiedot.
Hakija voi myös tarvittaessa ladata ansioluettelon ja lähettää sitten työhakemuksen.

## <a name="check-application-status"></a>Hakemuksen tilan tarkistaminen

Kun hakija on hakenut yhtä tai useaa työpaikkaa, hän voi tarkastella avoimia ja suljettuja hakemuksia valitsemalla sivun yläosan siirtymispalkissa **Hakemukset**. Kun hakija avaa jonkin hakemuksensa, näkyviin tulee hakemuksen nykyinen tila ja mahdolliset odottavat toiminnot, jotka hakijan on tehtävä. Jos hakijan on esimerkiksi annettava mahdolliset päivämäärät henkilökohtaista haastattelua varten, käytettävissä olevat vaihtoehdot näkyvät sivulla.

## <a name="internal-jobs"></a>Sisäiset työpaikat

Tällä hetkellä sisäisiksi merkityt Attractin urasivustoon julkaistut työt eivät näy urasivustossa. Niitä voi käyttää vain avaamalla suoran **Käytä**-linkin URL-osoitteen, joka voidaan kopioida Attract-sovelluksesta.
