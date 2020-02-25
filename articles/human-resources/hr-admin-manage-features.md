---
title: Hallitse ominaisuuksia
description: Tutustu uusien ominaisuuksien käyttöönottoon ja käytöstä poistamiseen Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 84ff11e8237ce0669f7f6ac70c5b4411c5d4b466
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008853"
---
# <a name="manage-features"></a>Hallitse ominaisuuksia

Julkaisemme jatkuvasti uusia ominaisuuksia Microsoft Dynamics 365 Human Resourcesissa ja haluamme tarjota ne asiakkaillemme mahdollisimman pian. Tarjoamme esikatseluominaisuuksia, jotka ovat lähes valmiita yleiseen käyttöön ja ne ovat läpäisseet laajan testauksen. Haluamme saada vielä viimeisen asiakaspalautekierroksen, ennen kuin hyväksymme ominaisuudet yleisesti saataville.

Katso lisätietoja uusista ominaisuuksista Human Resourcesissa kohdista [Uutta Human Resourcesissa](hr-admin-whats-new.md) ja [Dynamics 365:n ja Power Platformin julkaisusuunnitelma](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1).

**Toimintojen hallinta** -työtilassa on luettelo kussakin julkaisussa toimitetuista toiminnoista. Uudet asetukset ovat oletusarvoisesti poissa käytöstä. Työtilan avulla voit ottaa ne käyttöön ja tarkastella niiden dokumentaatiota. Lisätietoja Toimintojen hallinnasta on kohdassa [Toimintojen hallinnan yleiskuvaus](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Kaikki uudet toiminnot pysyvät esiversiossa ainakin 30 päivää ja yleensä 30–60 päivää. Tärkeimmät toiminnot ovat yleensä saatavana kunkin vuoden lokakuussa ja huhtikuussa esiversiojakson jälkeen. Voit ottaa uudet ominaisuudet käyttöön heti, kun näet ne **Toimintojen hallinta** -työtilassa. Jotkin toiminnot on ehkä otettu käyttöön oletusarvoisesti.

Kun toiminto on yleisesti saatavana, se voidaan ottaa käyttöön tai poistaa käytöstä tuotantoympäristöissä. **Toimintojen hallinta** -työtila ilmaisee, milloin esiversiotoiminto tulee pakolliseksi. Tämä päivämäärä on yleensä 1. lokakuuta tai 1. huhtikuuta eli ne vastaavat puolivuotisia julkaisusuunnitelmia. Pakollisia toimintoja ei voi poistaa käytöstä. Toiminnon voi ottaa käyttöön ja poistaa käytöstä kaikissa ympäristöissä siihen saakka, että muuttuu pakolliseksi.

## <a name="enable-or-disable-preview-features"></a>Esiversio-ominaisuuksien ottaminen käyttöön tai poistaminen käytöstä

Jos haluat käyttää esikatselutoimintoja, sinun on ensin otettava ne käyttöön omassa ympäristössäsi. Esiversio-ominaisuuksien käyttöönotto on ympäristökohtainen.

> [!IMPORTANT]
> Esiversiotoiminnot ovat käytettävissä vain **eritys**ympäristöissä. Kun otat esikatseluominaisuuden käyttöön, sallit esikastseluominaisuudet organisaation kaikille käyttäjille kyseisessä ympäristössä. Kun poistat esikatseluominaisuuden käytöstä, esikatseluominaisuudet eivät ole käyttäjien käytettävissä. Esiversio-ominaisuuksilla on Human Resourcesissa rajoitettu tuki. Niissä voi olla tavallista vähemmän tietosuoja- ja suojausominaisuuksia, eivätkä ne sisälly Human Resourcesin palvelutasosopimukseen (SLA). Älä käytä esiversio-ominaisuuksia henkilötietojen (eli henkilökohtaisesti tunnistettavien tietojen) käsittelyyn tai muiden sellaisten tietojen käsittelyyn, jotka edellyttävät lain- tai säädöstenmukaista suojelua.

1. Valitse Human Resourcesissa **Järjestelmän hallinta**.

2. Valitse **Ominaisuuksien hallinta** -ruutu.

3. Ota esikatseluomionaisuus käyttöön valitsemalla se luettelosta ja valitsemalla sitten **Ota käyttöön**. Poista esikatseluomionaisuus käytöstä valitsemalla se luettelosta ja valitsemalla sitten **Poista käytöstä**.

## <a name="preview-feature-benefits-management"></a>Esiversio-ominaisuus: Etujen hallinta

Etujen hallinta tarjoaa joustavan ratkaisun, joka tukee monia erilaisia etuusvaihtoehtoja, sekä helppokäyttöisen työntekijäkokemuksen, joka esittelee valikoimasi. Lisätietoja etujen hallinnan määrityksestä ja käytöstä on kohdassa [Etujen hallinnan yhteenveto](hr-benefits-management-overview.md).

Etujen hallinta **Edut** -työtilan toimintoja. Kun otat etujen hallinnan esikatseluominaisuuden käyttöön, et voi enää käyttää seuraavia **Edut**-työtilan lomakkeita:

- **Edut**
- **Edun elementit**
- **Osuuden laskentahinnat**
- **Edun rekisteröinnin tulokset**
- **Edun päättämisen ja laajennuksen tulokset**
- **Etukelpoisuuden käytäntösääntötyypit**
- **Etuuskelpoisuuden käytännöt**
- **Kelpoisuustapahtumat**

Voit tarkastella näiden lomakkeiden tietoja vain luku -tilassa. Jos haluat muokata tietoja, sinun on ensin poistettava etujen hallinnan esikatseluominaisuus käytöstä.

### <a name="benefits-management-known-issues"></a>Etujen hallinnan tunnetut ongelmat

#### <a name="life-events"></a>Elinkaaritapahtumat

Elämäntapahtumien käsittelyssä käyttäjä saa virheilmoituksen:

Kattavuuden alkamispäivän on oltava *suunnitelmajakson alun* ja *suunnitelmajakson lopun* välillä. 

Elämäntapahtuman käsittelyä jatketaan odotetulla tavalla.

#### <a name="eligibility-processing"></a>Kelpoisuuden käsittely

Käsiteltäessä kelpoisuutta sellaisten etujen osalta, joissa käytetään arvoja 1–5 kertaa palkka, prosenttiosuutta pakasta ja kiinteä kattavuusmäärä, edun tietopäivämääräksi on asetettava työntekijän aloituspäivämäärä kohdassa **Työhistoria** työtunnit, maksuvälit ja vuosittaisten etujen palkkasumma mukaan luettuna. Jos työntekijän osalta käytetään kiinteää kompensaatiota, syötä siihen liittyvät työtunnit ja maksuvälit, jolloin vuosittainen palkkamäärä lasketaan automaattisesti. Jos työntekijä on palkallinen, työtunteja ei tarvita. Suosittelemme uusia työntekijöitä luotaessa ensin kiinteän kompensaation syöttämistä. Voit päivittää etutietojen tietuetta kohdassa **Työntekijä > Työntekijän historia > Työsuhteen tiedot**. Muuta päivämääräksi työntekijän aloituspäivämäärä.

#### <a name="employee-self-service"></a>Työntekijän itsepalvelu

Työntekijät voivat valita suunnitelman, joiden vaatimuksia he eivät täytä ja tarkastella sitä. Esimerkki: Työntekijällä ei ole huollettavia, mutta hän voi vallita terveydenhuoltosuunnitelman perhekattavuusvaihtoehdolla.

Työntekijän summaa ei lasketa, kun henkivakuutuksen kattavuutta päivitetään. Jos työntekijälle esimerkiksi tarjotaan henkivakuutussuunnitelmaa, hän voi valita enintään 50 000 dollarin kattavuuden hintaan 0,36 dollaria per 1 000 dollaria kattavuutta.  Kun työntekijä päivittää kattavuusmäärän, työntekijän siihen liittyvät kulut pysyvät nollana.

Jos kyseessä on etuussuunnitelma, jossa kyseisen suunnitelmatyypin voi valita vain kerran, käyttäjä saa virheilmoituksen, jos hän yrittää luopua suunnitelmasta sellaisen valittuaan. Esimerkki: Käyttäjä valitsee terveydenhuoltosuunnitelman ja lisää sen ostoskoriin. Sen jälkeen hän valitsee **Luovu** saadakseen toisen terveydenhuoltosuunnitelman. Käyttäjä saa virheilmoituksen.

## <a name="preview-features-in-leave-and-absence"></a>Esikatseluominaisuudet lomissa ja poissaoloissa

Lomien ja poissaolojen esikatseluominaisuuksia ovat esimerkiksi:

- **Loma- ja poissaolokalenteri** – Loma- ja poissaoloparametrit siirtyvät kohdasta **Henkilöhallinnon parametrit** uuteen näyttöön nimeltään **Loma- ja poissaoloparametrit**. Uudessa näytössä on uusi **Kalenteri**-välilehti. Tämä esikatselu mahdollistaa vain parametrien osajoukon. Voit käyttää uutta näyttöä **Lomat ja poissaolot** -työtilan **Linkit**-välilehdestä. Kalentereja ovat esimerkiksi:
  - **Yrityksen kalenteri** – Näyttää kaikki työntekijöiden vapaa-aikapyynnöt. Henkilöt, joilla on **Henkilöstöhallinto**-rooli voivat käyttää tätä **Linkit**-välilehdessä **Lomat ja poissaolot** -työtilassa.
  - **Johtajaryhmän kalenteri** – Näyttää kaikkien suorien alaisten vapaa-aikapyynnöt. Johtajat voivat käyttää kalenteria työntekijän itsepalvelun **Lomat ja poissaolot** -kohdan **Oma ryhmä** -välilehdessä. 

- **Lomien ja poissaolojen vapaakalenterit** – Lomatyyppeihin kuuluu nyt **Loma**-vaihtoehto, jota käytetään yhdessä työaikakalenterin kanssa. Lomiksi ja kiinnioloajoiksi määritettyjä päivä kutsutaan nyt työpäivä luotaessa nimellä **Loma**. Kun jaksotuksia käsitellään, työntekijöille, joille kalenteri on määritetty, tehdään muutoksia, jotta otetaan huomiot työpäiville osuvat lomat.

- **Lomien jaksotusten valvonta** – Uuden näytön avulla voit tarkistaa, milloin jaksotukset on käsitelty ja poistettu sekä kaikkien työntekijöiden että yksittäisten työntekijöiden osalta. Voit käyttää tätä uutta näyttöä **Lomat ja poissaolot** -työtilan **Linkit**-välilehdestä.

- **Loman jaksotuksen poisto** – Voit nyt poistaa tiettyjen lomasuunnitelmien jaksotustietueita. Voit käyttää tätä uutta valintaa **Lomat ja poissaolot** -työtilan **Linkit**-välilehdestä. Yksittäisten työntekijöiden osalta tämä valinta näkyy työntekijän profiilin **Lomat ja poissaolot** -ryhmittelyssä. 

- **Lomien jaksotuksen pyöristys** – Uudet **Lomatyypin**asetukset määrittävät, millaista pyöristystä jaksotuksessa käytetään sekä pyöristyksen desimaalitarkkuuden jaksotusprosessin aikana. Kun jaksotuksia käsitellään, pyöristystä ja tarkkuutta sovelletaan jaksotustietueisiin. 

- **Määritä useita lomatyyppejä yksittäisessä lomasuunnitelmassa** – Uudessa lomatyyppien sarakkeessa loman jaksotusaikataulussa voit määrittää loma- ja poissaolosuunnitelmalle useita lomatyyppejä eri jaksotusaikatauluineen. Aiempi **Lomatyyppi**-kenttä poistetaan. Työntekijöiden rekisteröitymisessä lomatyyppien saldot esitetään nyt taulukossa ruudun yläreunan sijaan.

  > [!IMPORTANT]
  > Tätä ominaisuutta ei voi poistaa käytöstä sen jälkeen, kun se on otettu käyttöön.

- **Käytä työntekijän laskennallista kokopäiväisyyttä (FTE) jaksotuksessa** – Uusi loman jaksotusaikataulun sarake, joka mahdollistaa FTE-arvon käytön jaksotuksessa. Kun jaksotuksia käsitellään, sovellus käyttää työntekijän ensisijaista asemaa ja määritettyä FTE-arvoa määrittääkseen suhteellisen jaksotusmäärän.

  > [!NOTE]
  > Tämä ominaisuus on käytössä vain, kun **Määritä useita lomatyyppejä lomasuunnitelmaa kohden** on käytössä. 

## <a name="feedback"></a>Palaute

Haluamme kuulla kokemuksistasi esikatseluominaisuuksien parissa. Kannustamme sinua antamaan säännöllisesti palautetta, kun käytät näitä sivustoja tai muita ominaisuuksia:

- [Yhteisö](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Tämä sivusto on erinomainen resurssi, jossa käyttäjät voivat keskustella tapauksista, esittää kysymyksiä ja saada ohjeita yhteisöltä.
- Ilmoita meille, mitä ominaisuuksia haluaisit tuotteeseen ja kerro, mitä muutoksia nykyisiin ominaisuuksiin pitäisi mielestäsi tehdä. Ehdota tuoteideoita kohdassa [Human Resources -ideat](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    
Älä sisällytä mitään henkilötietoja (eli henkilökohtaisesti tunnistettavia tietoja) palautteeseesi tai tuotearvioihisi. Kerättyjä tietoja voidaan analysoida tarkemmin, eikä niitä käytetä pyyntöihin vastaamiseen tietosuojalakien mukaisesti. Henkilökohtaisiin tietoihin, jotka kerätään erillään näistä ohjelmista, sovelletaan [Microsoftin tietosuojalausuntoa](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Lisätietoja

- [Uutta henkilöstöhallinnossa](hr-admin-whats-new.md)
- [Dynamics 365:n ja Power Platformin julkaisusuunnitelma](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1)