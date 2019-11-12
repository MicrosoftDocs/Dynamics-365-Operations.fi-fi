---
title: Esiversio-ominaisuuksien käyttö Microsoft Dynamics 365 Talentissa
description: Tässä aiheessa kuvataan, kuinka järjestelmänvalvoja voi ottaa käyttöön esiversio-ominaisuudet Microsoft Dynamics 365 Talentissa. Siinä listataan myös ominaisuudet, jotka ovat tällä hetkellä käytössä esikatselua varten.
author: tracykeya
manager: AnnBe
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 0f9a83aeea3942d3c56d32956f79490c91565e9e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551592"
---
# <a name="access-preview-features-in-microsoft-dynamics-365-talent"></a>Esiversio-ominaisuuksien käyttö Microsoft Dynamics 365 Talentissa

[!include[banner](../includes/banner.md)]

Parannamme jatkuvasti henkilöstöresurssien hallinnan (HCM) ominaisuuksia Microsoft Dynamics 365 Talentissa ja haluamme tarjota ne asiakkaillemme mahdollisimman pian. Järjestelmänvalvojat voivat tarkastella ja käyttää esiversio-ominaisuuksia ympäristöissään. Nämä ominaisuudet ovat lähes valmiita yleiseen käyttöön ja ne ovat läpäisseet laajan testauksen. Haluamme saada vielä viimeisen asiakaspalautekierroksen, ennen kuin hyväksymme ominaisuudet yleisesti saataville.

Tässä aiheessa kuvataan, kuinka voit ottaa käyttöön esiversio-ominaisuudet. Siinä listataan myös ominaisuudet, jotka ovat tällä hetkellä saatavilla esikatselua varten. Tätä luetteloa päivitetään sitä mukaa, kun ominaisuuksia julkaistaan yleiseen käyttöön ja uusia ominaisuuksia tuodaan esikatseltavaksi. Erillistä ilmoitusta ei anneta, kun uusia ominaisuuksia julkaistaan esikatseluun. Ominaisuudet tuodaan vain käyttäjien saataville. Lisätietoja Talentin uusista ominaisuuksista on kohdassa [Uudet tai muuttuneet ominaisuudet Dynamics 365 Talentissa](./whats-new.md)ja [Dynamics 365- ja Power Platform -julkaisutiedot](https://docs.microsoft.com/business-applications-release-notes) -kohdissa.

## <a name="enable-or-disable-preview-features"></a>Esiversio-ominaisuuksien ottaminen käyttöön tai poistaminen käytöstä

Jos haluat käyttää esikatselutoimintoja, sinun on ensin otettava ne käyttöön omassa ympäristössäsi. Esiversio-ominaisuuksien käyttöönotto on ympäristökohtainen.

> [!IMPORTANT]
> Kun otat **Esiversio-ominaisuudet**-asetuksen käyttöön sallit esiversio-ominaisuudet organisaation kaikille käyttäjille kyseisessä ympäristössä. Kun poistat asetuksen käytöstä, esiversio-ominaisuudet eivät ole käyttäjien käytettävissä. Esiversio-ominaisuuksilla on Talentissa rajoitettu tuki. Niissä voi olla tavallista vähemmän tietosuoja- ja suojausominaisuuksia, eivätkä ne sisälly Talentin palvelutasosopimukseen (SLA). Älä käytä esiversio-ominaisuuksia henkilötietojen (eli henkilökohtaisesti tunnistettavien tietojen) käsittelyyn tai muiden sellaisten tietojen käsittelyyn, jotka edellyttävät lain- tai säädöstenmukaista suojelua.

### <a name="attract"></a>Kerätä

1. Kirjaudu Microsoft Dynamics 365 Talent: Attractiin.
2. Valitse **Asetukset**-valikossa (hammasrataskuvake) oikeassa alakulmassa **Hallintakeskus**.
3. Valitse **Ominaisuuksien hallinta** -välilehdestä kohdan **Esiversio-ominaisuudet** vieressä oleva vaihtoehto siten, että se muuttuu siniseksi ja siinä lukee **Päällä**.

    ![Ota esiversio-ominaisuudet käyttöön Attractissa](./media/attract-enable-preview-features.png)

4. Valitse tai Peruuta henkilökohtaisten esikatseluominaisuuksien valinta. Jos et tee mitään, kaikki käytettävissä olevat esikatseluominaisuudet ovat käytössä.
5. Päivitä selaimesi ikkuna nähdäksesi uudet ominaisuudet. Käyttäjät, jotka ovat jo kirjautuneet sisään, näkevät ominaisuudet seuraavan sisäänkirjautumiskerran yhteydessä tai päivittäessään selaimen ikkunan.

> [!NOTE]
> Jotkin esikatseluominaisuudet saattavat edellyttää lisämääritystä. Viimeistele sen määritys seuraamalla esikatselutoiminnon vieressä olevaa linkkiä.

### <a name="core-hr"></a>Henkilöstöhallinnon perusversio

1. Kirjaudu sisään Talentiin.
2. Valitse **Järjestelmän hallinta**ja valitse sitten **Linkit**-välilehti.
3. Valitse **Järjestelmänhallinta** -sivun **Asetukset** -kohdasta **Järjestelmän parametrit**.
4. Valitse **Järjestelmän parametrit** -sivulla **Esikatseluominaisuudet**-välilehti.
5. Aseta kohtaan **Kaikkien käyttäjien esikatselutila** vaihtoehto **Kyllä**, jos haluat käyttää esikatselutoimintoja.

    ![Ota esiversio-ominaisuudet käyttöön Core HR:ssä](./media/corehr-enable-preview-features.png)

> [!NOTE]
> Jos et halua käyttää esikatselutoimintoja, tee samat toimet, mutta aseta kohtaan **Kaikkien käyttäjien esikatselutila** vaihtoehto **Ei** Kun esiversio-ominaisuudet poistetaan käytöstä, käyttäjät eivät voi käyttää niitä ja kyseisiin ominaisuuksiin liittyvissä prosesseissa voi esiintyä virheitä.

### <a name="onboard"></a>Perehdytys

Microsoft Dynamics 365 Talent: Onboardissa ei ole tällä hetkellä käytettävissä esiversiotoimintoja.

## <a name="features-that-are-currently-in-preview"></a>Tämänhetkiset esiversio-ominaisuudet

### <a name="attract"></a>Kerätä

- [Hakijasuositus](./intelligent-recommendations.md#candidate-recommendations) – Jos työpaikkaan on yli kymmenen hakijaa tai potentiaalista ehdokasta, joilla on ansioluettelo tai täydellinen profiili, työpaikan vaatimuksia parhaiten vastaavat hakijat tulevat näkyviin kyseisen työn **Hakijat harkittavaksi** -osassa.
- [Työsuositus](./intelligent-recommendations.md#job-recommendations) - Jos urasivustollesi on lähetetty yli kymmenen työpaikkaa, Attract tarjoaa työsuosituksia prospekteille.
- [Broadbean-integrointi](./posting-jobs-external.md#post-jobs-to-broadbean) - Voit lähettää työpaikkoja Attractista Broadbeaniin, ulkoiseen urasivustoon. Kun olet määrittänyt tämän esikatselutoiminnon, sinun on täytettävä määritykset syöttämällä Broadbean-käyttäjänimesi, asiakastunnuksesi ja salaustunnuksesi.
- [Analyysit](./analytic-reports.md) – Analytics Hubissa työhönottotiimit voivat tarkastella sekä yksittäisen työn keskeisiä mittareita että yhteenlaskettuja mittareita kaikkien töiden yhteydessä.
- [EEO](./activities-attract.md) – Uudet tehtävätyypit mahdollistavat valmiiksi täytetyn lomakkeen käytön, jolla kerätään ehdokkaan Equal Employment Opportunity (EEO) - ja Office of Federal Contract Compliance Program (OFCCP) -tiedot. Ennalta määritettyä lomaketta ei voi muokata.
- [Prospektisuositus](./intelligent-recommendations.md#prospect-recommendations) – Attract arvioi aiempia hakijoita ja nykyisiä ehdokkaita ja antaa luettelon prospekteista, jotka sopivat työhösi.
- [Osuvuushaku](./attract-talent-pools.md#search-and-view-candidate-profiles) – Voit etsiä koko ehdokastietokannasta tiettyjä osaamisalueita, nimiä tai koulutustaustoja. Attract tekee hakuja koko profiilista ja korostaa kaikki löytämänsä osumat. Attract hakee myös kaikki hakijan käytettävissä olevat asiakirjat ja luokittelee älykkäästi hakutulokset.
- [Tehtävän kohderyhmä](./whats-new-talent-march-20.md#setting-the-audience-on-activities) – Voit määrittää tehtävien (kuten haastattelun, aikataulun tai palautteen) kohderyhmäksi **Kaikki ehdokkaat**, **Sisäiset ehdokkaat** tai **Ulkoiset ehdokkaat**. Asiakastoiminnot, kuten YouTube-videot ja WWW-sisältö ja Microsoft Forms voidaan toimittaa kaikille ehdokkaille, vain sisäisille ehdokkaille, vain ulkoisille ehdokkaille tai työhönottoryhmälle.
- [Käytä LinkedIniä](./career-site.md#enable-applying-for-jobs-with-linkedin-profiles) – Voit määrittää vaihtoehdon Attract-urasivustollesi, jotta työnhakijat voivat hakea LinkedInin kautta. Tämä toiminto virtaviivaistaa ehdokkaiden hakuprosessia antamalla heidän käyttää LinkedIn-profiiliaan, jotta heidän hakemuksensa täytetään automaattisesti urasivustossa.
- [Lähdeseuranta](./source-tracking.md) – Attract seuraa hakijasovellusten lähdettä ja antaa arvokasta tietoa, jonka avulla voit kohdentaa työhönottopyrkimyksiäsi. Voit myös valita sovelluslähteen samalla, kun lisäät hakijan työ- tai lahjakkuusalueelle.
- [Hopeamitalisti](./whats-new-talent-march-20.md#designate-silver-medalists-to-assign-high-value-applicants-for-future-positions) – Jos jotkin ehdokkaista sopivat hyvin organisaatioosi, mutta et antanut tarjousta nykyiseen paikkaan, voit määrittää heidät hopeamitalisteiksi. Tämä toiminto auttaa lyhentämään palkkausaikaa, kun seuraavan kerran vastaava paikka on tarjolla.

### <a name="core-hr"></a>Henkilöstöhallinnon perusversio

- [Vahvista toimihierarkian tiedot](./whats-new-talent-may-13-2019.md#new-page-to-validate-position-hierarchy-data) – Voit vahvistaa kaikkien vahingossa tuotujen kehäviitteiden johtamishierarkian.
- [Määritä poissaolotyyppien syykoodit](./whats-new-talent-may-13-2019.md#specify-reason-codes-on-leave-types) – Voit määrittää poissaolotyyppien syykoodit.
- [Vaadi syykoodit poissaolopyynnöille](./whats-new-talent-may-13-2019.md#require-reason-codes-for-specific-leave-types-on-time-off-requests) – Voit poissaolotyyppien syykoodien määrittämisen lisäksi vaatia syykoodeja poissaolopyyntöjä varten.
- [Anna loma-ja poissaolotapahtumaluettelo HR:lle](./whats-new-talent-may-13-2019.md#provide-a-leave-and-absence-transaction-list-for-hr) – Voit tarkastella loma- ja poissaolotapahtumien luetteloa, jotta saat tietoja aikasaldoista.

### <a name="onboard"></a>Perehdytys

Tällä hetkellä ei ole käytettävissä esikatselutoimintoja kohteelle: Onboard

## <a name="feedback"></a>Palaute

Haluamme kuulla kokemuksistasi näistä esikatseluominaisuuksista. Kannustamme sinua antamaan säännöllisesti palautetta, kun käytät näitä sivustoja tai muita ominaisuuksia:

- [Yhteisö](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Tämä sivusto on erinomainen resurssi, jossa käyttäjät voivat keskustella tapauksista, esittää kysymyksiä ja saada ohjeita yhteisöltä.
- Ilmoita meille, mitä ominaisuuksia haluaisit tuotteeseen ja kerro, mitä muutoksia nykyisiin ominaisuuksiin pitäisi mielestäsi tehdä. Ehdota tuoteideoita seuraavilla sivustoilla:

    - [Attract-ideat](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Core HR -ideat](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    - [Onboard-ideat](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

Varmista, että et sisällytä mitään henkilötietoja (eli henkilökohtaisesti tunnistettavia tietoja) palautteeseesi tai tuotearvioihisi. Kerättyjä tietoja voidaan analysoida tarkemmin, eikä niitä käytetä pyyntöihin vastaamiseen tietosuojalakien mukaisesti. Henkilökohtaisiin tietoihin, jotka kerätään erillään näistä ohjelmista, sovelletaan [Microsoftin tietosuojalausuntoa](https://privacy.microsoft.com/privacystatement).

> [!TIP]
> Lisää kirjanmerkki tähän aiheeseen ja käy säännöllisesti katsomassa tietoa uusista julkaistuista esiversio-ominaisuuksista.

## <a name="see-also"></a>Lisätietoja

- [Kokeile tai osta Talent-sovelluksia](https://dynamics.microsoft.com/talent/overview/)
- [Uutta](./whats-new.md)
- [Julkaisutiedot](https://docs.microsoft.com/business-applications-release-notes/index)
- [Talent-tuen saaminen](./talent-support.md)
