---
title: Dynamics 365 for Talent Core HR -ohjelman uudet tai muuttuneet ominaisuudet (31. lokakuuta 2018)
description: "Tässä aiheessa käsitellään Microsoft Dynamics 365 for Talent Core HR -ohjelman uusia tai muuttuneita ominaisuuksia."
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c5acd09e25ecd5fefa637342f83d0ee0f1891402
ms.contentlocale: fi-fi
ms.lasthandoff: 11/01/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a>Dynamics 365 for Talent Core HR -ohjelman uudet tai muuttuneet ominaisuudet (31. lokakuuta 2018)

[!include [banner](includes/banner.md)]

**Koontiversio 8.1.2031**

Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.

## <a name="create-links-from-talent-to-finance-and-operations"></a>Linkkien luonti Talentista Finance and Operationsiin
Tällä uudella siirtymistoiminnolla voi muodostaa linkin Talentista Finance and Operationsiin, joten voit siirtyä suoraan Finance and Operations -sivuille. Voit määrittää linkkien määrityksen yhteydessä linkin nimen ja ryhmän, kohdan, jossa linkkiä käytetään Talentissa, ja Finance and Operationsissa avattavan kohdesivun.

#### <a name="coming-soon"></a>Tulossa pian
Myöhemmin lisättävä kenttäkonteksti mahdollistaa suoran siirtymisen vastaaviin Finance and Operationsin tietueisiin. Voit esimerkiksi antaa **Linkki kenttään** -asetuksella kontekstin, jolla siirrytään suoraan tiettyyn työntekijään tai työpaikkaan Finance and Operationsissa.

### <a name="configure-target-systems"></a>Kohdejärjestelmien määrittäminen

Järjestelmänvalvojat voivat määrittää Talentissa linkit, joita käytetään järjestelmänhallinnan työtilan kautta. Määrityksen osan muodostavat Finance and Operations -ympäristöt, joihin haluat siirtyä linkin kohteena. Se tehdään nimeämällä kohdejärjestelmä ja antamalla Finance and Operations -ympäristön URL-osoite. Esimerkki annettavasta Finance and Operationsin URL-osoitteesta: https://devax00124aos.cloud.test.dynamics.com/. Kun olet määrittänyt kohdejärjestelmät, voit määrittää linkit.

### <a name="configure-links"></a>Määritä linkit

Jokaiseen luotavaan linkkiin on määritettävä seuraavat tiedot.

- Linkki – linkin nimi, jota käytetään vain tunnistamiseen.

- Ota tämä linkki käyttöön – valitse **Kyllä**, jos haluat näyttää linkin Talentin käyttäjille.

- Näyttönimi – Määritä nimi, joka näkyy Finance and Operationsiin vievänä linkkinä. Näitä tietoja ei ole tällä hetkellä käännetty.

- Surface-linkki lomakkeessa – valitse sivu, jolla haluat linkin näkyvän.

- Ryhmä – ryhmät eivät ole pakollisia, mutta jos haluat järjestää linkit ryhmien avulla, valitse **Ryhmä**-kentässä aiemmin luotu ryhmä tai luo uusi ryhmä.

- Kohdejärjestelmä – Valitse kohderyhmä, joka luotiin **Määritä kohdejärjestelmä** -asetuksella. Se on Finance and Operations -ympäristö, jota käyttämään siirrytään linkin avulla.

- Käytä käyttäjän nykyistä yritystä – Valitse **Kyllä**, jos haluat käyttää käyttäjän nykyistä yrityskontekstia Finance and Operationsiin siirryttäessä. Jos valitset **Ei**, voit valita käytettävän yrityksen.

- Kohdevalikkovaihtoehto – Anna Finance and Operationsin valikkovaihtoehto, jota linkin on käytettävä siirryttäessä. Käytettävissä on ne valikkotoiminnot, joihin voi siirtyä suoraan. Voit etsiä tarvittavan valikkotoiminnon avaamalla ensin Finance and Operationsin ja sitten sivun, johon siirrytään. Kopioi valikkotoiminto URL-osoitteesta. Jos esimerkiksi haluat, että linkki vie Finance and Operationsin työntekijäluetteloon, anna arvo, joka URL-osoitteessa &mi-kohdan jälkeen. https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees. Tässä esimerkissä valikkotoiminto, johon työntekijäluettelosivulla siirrytään on HcmWorkerListPage_Employees.

- Linkki tietolähteeseen – Valitse tietolähde, johon linkki viittaa. Käytettävissä on tavallisimmat lähteet, kuten **Työntekijä** ja **Toimi**.

- Linkki kenttään – (tulossa pian) tämän kentän valinta mahdollistaa suoran siirtymisen yhdestä Talentin tietueesta yhteen Finance and Operationsin tietueeseen.

### <a name="access-to-links"></a>Linkkien käyttöoikeus

Järjestelmänvalvojat näkevät juuri luodut linkit määritetyillä sivuilla, vaikka **Ota tämä linkki käyttöön** -asetuksena olisi **Ei**. Tämä mahdollistaakin linkkien testaamisen, ennen kuin ne ovat muiden työntekijöiden käytössä. Kaikki muut roolit näkevät määritetyt linkit vasta, kun **Ota tämä linkki käyttöön** -asetuksena on **Kyllä**. Työntekijät, joilla on linkit sisältävien sivujen käyttöoikeus, on myös linkkien käyttöoikeus.

Käyttäjillä voi olla myös Finance and Operationsissa määritettyjä käyttöoikeuksia, jotka koskevat Finance and Operationsin sivujen käyttöoikeuksia. Jos heillä ei niitä ole, linkkiä käytettäessä avautuu suojauksen valintaikkuna.


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

