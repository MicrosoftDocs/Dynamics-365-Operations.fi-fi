---
title: Attractin urasivuston toiminnot
description: "Tässä artikkelissa on Microsoft Dynamics 365 for Talent - Attractin hakijalle suunnatun urasivuston toimintojen yleiskatsaus. Siinä käsitellään myös toiminnon määrittäminen."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: fi-fi
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a>Attractin urasivuston toiminnot

[!include [banner](includes/banner.md)]

Tässä artikkelissa on Microsoft Dynamics 365 for Talent: Attractin hakijalle suunnatun urasivuston toimintojen yleiskatsaus. Siinä käsitellään myös toiminnon määrittäminen.

## <a name="overview"></a>Yleiskuvaus

Attractissa on yksi urasivusto vuokraajan kullekin ympäristölle. Jos organisaatiossa on esimerkiksi kehitysympäristö ja testiympäristö, sekä kehitys- että testiympäristölle valmistellaan oma urasivusto. Kumpikin urasivusto on **täysin eristetty** ja kummassakin oma todennusmekanismi. Urasivustot eivät jaa töitä ja hakijaprofiileja keskenään.

Urasivusto on oletusarvoisesti julkinen. Niinpä hakijat voivat tarkastella kaikki ulkoiseksi merkittyjä töitä ilman kirjautumista. Kaikkia muita toimintoja varten hakijoiden on kuitenkin kirjauduttava sisään.

## <a name="career-site-management"></a>Urasivuston hallinta

Asetuksilla hallitaan seuraavia urasivuston kohteita:

- **Organisaation nimi:** Organisaation nimi näkyy siirtymispalkissa urasivuston yläosassa. Valitsemalla organisaation nimet hakijat voivat siirtyä sivulle, jossa on luettelo avoimista työpaikoista.
- **Organisaation logo:** Organisaation logo näkyy urasivuston vasemmassa yläkulmassa. Valitsemalla organisaation logon hakijat voivat siirtyä sivulle, jossa on luettelo avoimista työpaikoista.

Voit määrittää organisaation nimen ja logon arvot kirjautumalla järjestelmänvalvojana Attractiin ja valitsemalla ensin **Asetukset**-valikossa (hammasrataskuvake) **Hallintakeskus** ja sitten **Yrityksen tiedot** -välilehden.

> [!NOTE]
> Urasivustossa näkyvän logon korkeus on aina 20 kuvapistettä (px). Hallintakeskukseen lisätty kuva sovitetaan oikean kokoiseksi. Tämän vuoksi kuvan leveys voi muuttua.

## <a name="career-site-url"></a>Urasivuston URL-osoite

Kun [teet ulkoisen työpaikkailmoituksen](./Creating-jobs-Attract.md#postings) ensimmäisen kerran, voit kopioida **Käytä**-linkin Attract-sovelluksesta. Tämän linkin URL-osoitteen muoto on seuraavanlainen: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`

Urasivuston URL-osoite on **Käytä**-linkin URL-osoitteen alimerkkijono. Se sisältää yrityksen nimestä oikealle kaikki merkkijonon tiedot. Niinpä edellisessä **Käytä**-linkin URL-osoitteessa urasivuston URL-osoite on `https://jobs.talent.dynamics.com/jobs/<company_name>/`.

## <a name="authentication-options"></a>Todennusasetukset

Hakijat voivat kirjautua Attract-urasivustoon seuraavin tavoin:

- Henkilökohtainen tili:

    - LinkedIn
    - Microsoft 
    - Google
    - Facebook

- Työ- tai opiskelijatili:

    - Microsoft Azure Active Directory (Azure AD)

Azure AD -kirjautuminen on tarkoitettu vain sisäisille hakijoille. Tämän vuoksi vain yrityksen Azure AD -tunnistetietoja käyttävät sisäiset hakijat voivat käyttää tätä vaihtoehtoa. Esimerkiksi hakija, joka on tällä hetkellä Contoso Ltd:n työntekijä, halua hakea töitä Alpine Ski Housesta, joka on erillinen yritys. Kirjautuminen ei tässä tapauksessa onnistu, jos työntekijä yrittää käyttää Contoso Ltd:n Azure AD -tunnistetietoja.

## <a name="create-and-maintain-a-profile"></a>Profiilin luominen ja ylläpitäminen

Kun hakijat ovat kirjautuneet urasivustoon, he voivat luoda profiilin ja ylläpitää sitä valitsemalla sivun yläosan siirtymispalkissa **Oma profiili**. Profiili sisältää henkilötiedot, tietoja työkokemuksesta ja koulutuksesta sekä asiakirjoja, linkkejä ja tietoja osaamisalueista. Kun profiili on luotu, sen avulla voi hakea työpaikkoja, joista hakija on kiinnostunut. Lisäksi Attract voi suositella profiilien avulla hakijoille sopivia työpaikkoja.

## <a name="find-the-right-job"></a>Oikean työpaikan etsiminen

Hakijat voivat hakea tiettyä työpaikkaa työluettelosivulla hakuehtojen avulla. Hakutoiminto hakee tiettyjä sanoja työnimikkeistä ja työnkuvauksista sekä näyttää sopivat työpaikat tuloksina. Hakijat voivat suodattaa tuloksia koska tahansa työn sijainnin tai työtehtävän perusteella.

Hakijat voivat tarkastella urasivustossa myös suositeltuja työpaikkoja. Hakijalle suositellaan työpaikkoja hakijan aiempien hakemusten, profiilin ja ansioluetteloiden perusteella.

> [!NOTE]
> Työpaikkasuositukset näytetään vain, jos urasivustossa on julkaista vähintään 10 työpaikkaa ja jos hakija on täyttänyt profiilitiedot.

## <a name="apply-for-jobs"></a>Hae työtä

Kun hakija löytää oikean työpaikan, sitä voi hakea työn tietosivun **Käytä**-painikkeella. Hakijat voivat tässä vaiheessa joko luoda uuden profiilin tai tarkistaa aiemmin luodun profiilin tiedot. Hakija voi myös tarvittaessa ladata ansioluettelon ja lähettää sitten työhakemuksen.

## <a name="check-application-status"></a>Hakemuksen tilan tarkistaminen

Kun hakija on hakenut yhtä tai useaa työpaikkaa, hän voi tarkastella avoimia ja suljettuja hakemuksia valitsemalla sivun yläosan siirtymispalkissa **Hakemukset**. Kun hakija avaa jonkin hakemuksensa, näkyviin tulee hakemuksen nykyinen tila ja mahdolliset odottavat toiminnot, jotka hakijan on tehtävä. Jos hakijan on esimerkiksi annettava mahdolliset päivämäärät henkilökohtaista haastattelua varten, käytettävissä olevat vaihtoehdot näkyvät sivulla.

## <a name="internal-jobs"></a>Sisäiset työpaikat

Tällä hetkellä sisäisiksi merkityt Attractin urasivustoon julkaistut työt eivät näy urasivustossa. Niitä voi käyttää vain avaamalla suoran **Käytä**-linkin URL-osoitteen, joka voidaan kopioida Attract-sovelluksesta.

