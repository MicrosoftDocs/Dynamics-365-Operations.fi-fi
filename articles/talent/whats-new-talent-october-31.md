---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (31. lokakuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4851c62a19bb562c7f5f578aecbae99cfcdb982f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461057"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-31-2018"></a>Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (31. lokakuuta 2018)

**Koontiversio 8.1.2031**

Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.

## <a name="create-links-from-talent-to-finance"></a>Linkkien luonti Talentista Financeen
Tällä uudella siirtymistoiminnolla voi muodostaa linkin Talentista Financeen, joten voit siirtyä suoraan Finance-sivuille. Voit määrittää linkkien määrityksen yhteydessä linkin nimen ja ryhmän, kohdan, jossa linkkiä käytetään Talentissa, ja Financessa avattavan kohdesivun.

#### <a name="coming-soon"></a>Tulossa pian
Myöhemmin lisättävä kenttäkonteksti mahdollistaa suoran siirtymisen vastaaviin Financen tietueisiin. Voit esimerkiksi antaa **Linkki kenttään** -asetuksella kontekstin, jolla siirrytään suoraan tiettyyn työntekijään tai työpaikkaan Financessa.

### <a name="configure-target-systems"></a>Kohdejärjestelmien määrittäminen

Järjestelmänvalvojat voivat määrittää Talentissa linkit, joita käytetään järjestelmänhallinnan työtilan kautta. Määrityksen osan muodostavat Finance-ympäristöt, joihin haluat siirtyä linkin kohteena. Se tehdään nimeämällä kohdejärjestelmä ja antamalla Finance-ympäristön URL-osoite. Esimerkki annettavasta Financen URL-osoitteesta: https://devax00124aos.cloud.test.dynamics.com/. Kun olet määrittänyt kohdejärjestelmät, voit määrittää linkit.

### <a name="configure-links"></a>Määritä linkit

Jokaiseen luotavaan linkkiin on määritettävä seuraavat tiedot.

- Linkki – linkin nimi, jota käytetään vain tunnistamiseen.

- Ota tämä linkki käyttöön – valitse **Kyllä**, jos haluat näyttää linkin Talentin käyttäjille.

- Näyttönimi – Määritä nimi, joka näkyy Financeen vievänä linkkinä. Näitä tietoja ei ole tällä hetkellä käännetty.

- Surface-linkki lomakkeessa – valitse sivu, jolla haluat linkin näkyvän.

- Ryhmä – ryhmät eivät ole pakollisia, mutta jos haluat järjestää linkit ryhmien avulla, valitse **Ryhmä**-kentässä aiemmin luotu ryhmä tai luo uusi ryhmä.

- Kohdejärjestelmä – Valitse kohderyhmä, joka luotiin **Määritä kohdejärjestelmä** -asetuksella. Se on Finance-ympäristö, jota käytetään siirryttäessä linkin avulla.

- Käytä käyttäjän nykyistä yritystä – Valitse **Kyllä**, jos haluat käyttää käyttäjän nykyistä yrityskontekstia Financeen siirryttäessä. Jos valitset **Ei**, voit valita käytettävän yrityksen.

- Kohdevalikkovaihtoehto – Anna Financen valikkovaihtoehto, jota linkin on käytettävä siirryttäessä. Käytettävissä on ne valikkotoiminnot, joihin voi siirtyä suoraan. Voit etsiä tarvittavan valikkotoiminnon avaamalla ensin Financen ja sitten sivun, johon siirrytään. Kopioi valikkotoiminto URL-osoitteesta. Jos haluat linkin vievän esimerkiksi Finance and Operationsin työntekijäluetteloon, syötä URL-osoitteen &mi-merkkien jälkeen näkyvä arvo. https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees. Tässä esimerkissä valikkotoiminto, johon työntekijäluettelosivulla siirrytään on HcmWorkerListPage_Employees.

- Linkki tietolähteeseen – Valitse tietolähde, johon linkki viittaa. Käytettävissä on tavallisimmat lähteet, kuten **Työntekijä** ja **Toimi**.

- Linkki kenttään – (tulossa pian) Tämän kentän valinta mahdollistaa suoran siirtymisen yhdestä Talentin tietueesta yhteen Financen tietueeseen.

### <a name="access-to-links"></a>Linkkien käyttöoikeus

Järjestelmänvalvojat näkevät juuri luodut linkit määritetyillä sivuilla, vaikka **Ota tämä linkki käyttöön** -asetuksena olisi **Ei**. Tämä mahdollistaakin linkkien testaamisen, ennen kuin ne ovat muiden työntekijöiden käytössä. Kaikki muut roolit näkevät määritetyt linkit vasta, kun **Ota tämä linkki käyttöön** -asetuksena on **Kyllä**. Työntekijät, joilla on linkit sisältävien sivujen käyttöoikeus, on myös linkkien käyttöoikeus.

Käyttäjillä voi olla myös Financessa määritettyjä käyttöoikeuksia, jotka koskevat Finance and Operationsin sivujen käyttöoikeuksia. Jos heillä ei niitä ole, linkkiä käytettäessä avautuu suojauksen valintaikkuna.


## <a name="other-changesfixes"></a>Muut muutokset ja korjaukset

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a>Uudelleen työntekijälle ei voi määrittää toimea, jonka aloituspäivä on tulevaisuudessa

Tehtyjen muutosten myöstä työntekijälle voidaan määrittää tulevaisuudessa alkava toimi. Toimet, joiden alkamispäivä on tulevaisuudessa, voidaan valita ja työntekijän määritys tehdään tallennettaessa tai työnkulun päättyessä (jos työnkulku on otettu käyttöön).

### <a name="new-employee-cannot-be-assigned-existing-position"></a>Uutta työntekijää ei voi määrittää aiemmin luotuun toimeen

Tehtyjen muutosten myötä uuden työntekijän määritys voidaan nyt määrittää aiemmin luotuihin toimiin.

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a>Ikälisäpäivä tai toimiston sijainti katoaa, kun työsuhteen alkamispäivä on menneisyydessä ja tietue tallennetaan

Tehtyjen muutosten myötä **Ikälisäpäivä** ja **Toimiston sijainti** näkyvät nyt oikein, kun entisten työntekijöiden muutokset tallennetaan.

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a>Työntekijän sivulla ei voi antaa tulevaisuuteen päivättyjä työsuhteita

Tulevaisuuteen päivättyjen työsuhteiden työsuhdetiedot on poistettu käytöstä työntekijän pääsivulla. Työnsuhdetiedot voidaan antaa **Päivämäärän hallinta** -sivuilla. Tulevissa versioissa tehdään lisää muutoksia, jotta työsuhdetiedot voidaan tehdä suoraan työnkulkuprosessin aikana.

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a>ValidFrom ja ValidTo HcmPersonalContactPersonEntity lisätty

Data Management Framework (DMF) -yksikkö HcmPersonalContactPersonEntity on päivitetty sisältämään voimassaolon alkamis- ja päättymispäivät, jotta tietyt etujen integrointiskenaariot voidaan ottaa käyttöön. 

## <a name="known-issue"></a>Tunnettu ongelma
- **Ongelma**: kun työntekijään lisätään uusi liite, **Uusi**- ja **Muokkaa**-painikkeet näkyvät harmaina. 
- **Ongelman kiertäminen:** Varmista ennen liitesivun avaamista, että **Työntekijä**-sivun tietoruudut on suljettu. Jos tietoruudut ovat suljettuja **Työntekijä**-sivua ladattaessa, liitepainikkeet otetaan käyttöön. (Tämä ongelma korjataan seuraavassa ympäristöpäivityksessä.)
