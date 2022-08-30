---
title: Etujen hallinnan yleiskatsaus
description: Tässä artikkelissa on Dynamics 365 Human Resourcesin etujen hallintaominaisuuden yleiskatsaus.
author: twheeloc
ms.date: 12/06/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2e3fa839b6e0f3cbaea8d2225b5a42ee8a368272
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336933"
---
# <a name="benefits-management-overview"></a>Etujen hallinnan yleiskatsaus

Pysyäksesi kilpailukykyisenä sinun on tarjottava laaja etuvalikoima. Näin houkuttelet parhaita työntekijöitä ja saat heidät pidettyä. Vakioetujen, kuten terveyshuollon ja hammashoidon lisäksi, sinun kannattaa ehkä tarjota myös laajennettuja palveluja, kuten adoptioapua, virkistysohjelmia ja vaatetuslisiä. Microsoft Dynamics 365 Human Resourcesin etujen hallinta on joustava ratkaisu, joka tukee monenlaisia etuvaihtoehtoja. Human Resources sisältää myös helppokäyttöisen työntekijäkokemuksen, joka esittelee valikoimasi.

- Parannettujen etuussuunnitelmien avulla voit luoda ja hallita yksilöllisiä etuussuunnitelmia ja tukea monimutkaisia etujen hinnastoja ja sisäkkäisiä tasoja. Voit helposti luoda etuusohjelmia ja -nippuja sekä automaattisen rekisteröinnin sääntöjä, jotka helpottavat työntekijöiden kokemusta.
- Joustoluotto-ohjelmien avulla voit käyttää suhteellista laskentaa eläköitymisen ja muiden elämäntapahtumien tukemiseen.
- Laajat kelpoisuussäännöt varmistavat, että annat oikeat edut oikeiden työntekijöiden käyttöön.
- Verkkorekisteröinti etuja varten tarjoaa työntekijöillesi helpon kokemuksen.
- Pätevän elämäntapahtuman käsittely tukee tulevia elämäntapahtumia.

Jos haluat käyttää demotietoja, sinun on otettava eristysympäristösi uudelleen käyttöön.

> [!NOTE]
> Voit nyt mukauttaa etujen hallinnan sivuja. Kattavuusprosentteihin liittyviä mukautettuja kenttiä voidaan lisätä etusuunnitelmien **Kattavuusvaihtoehto**-sivulle. Lisätietoja mukautettujen kenttien käyttämisestä on kohdassa [Mukautetut kentät](hr-developer-custom-fields.md).
>
> ![Etujen hallinnan mukautetut kentät](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Etujen hallinnan käyttöönotto

Tässä artikkeleissa esitellään, miten ominaisuudet otetaan käyttöön Human Resourcesissa. Siinä käsitellään myös, mitkä Human Resourcesin olemassa olevat ominaisuudet etujen hallinta korvaa ja mitkä ominaisuudet poistetaan käytöstä sen jälkeen, kun etujen hallinta otetaan käyttöön.

> [!IMPORTANT]
> Kun etujenhallinta on otettu käyttöön **Tuotanto**-ympäristössä, sitä ei voi poistaa käytöstä. On suositeltavaa ottaa käyttöön ja testata etujenhallinta **Eristys**-ympäristössä, ennen kuin otat sen käyttöön **Tuotanto** -ympäristössä. Vanhojen etutoimintojen ja uusien etujen hallintatoimintojen välillä on huomattavia eroja, jotka edellyttävät lisäasetuksia ja jotka on testattava ennen niiden asettamista tuotantoon.

Lisätietoja on ohjeaiheessa [Toimintojen hallinta](hr-admin-manage-features.md).

## <a name="process-overview"></a>Prosessin yleiskuvaus

Etujen määritysprosessiin kuuluu seuraavia tehtäviä:

1.  Määritä pakolliset etutiedot.
2.  Määritä valinnaiset etutiedot.
3.  Määritä etupalvelupaketit.
4.  Liukumahyvitysohjelmien määrittäminen (valinnainen).
5.  Määritä pakolliset työntekijätiedot.
6.  Määritä valinnaiset työntekijätiedot.
7.  Käsittele työntekijät oikeutuksen määrittämiseksi.
8.  Työntekijät valitsevat palvelupaketit työntekijän itsepalvelun kautta (valinnainen).
9.  Vahvista työntekijöiden palvelupakettivalinnat.
10. Elinkaaritapahtuman käsittelyn (valinnainen).
11. Hintojen päivitykset (valinnainen).

## <a name="set-up-required-benefit-information"></a>Määritä pakolliset etutiedot

Ennen kuin työntekijät voidaan rekisteröidä paketteihin, on määritettävä useita komponentteja:

- **Edunhallinnan parametrit** – Nämä asetukset jaetaan yritysten välillä. Voit määrittää oletussyykoodit, ottaa käyttöön **Edut-vuosipalkka**-vaihtoehdon, määrittää uusien työntekijöiden oletusmaksutiheyden ja ottaa elämäntapahtumat käyttöön. Lisätietoja on kohdassa [Etujen hallinnan parametrien määrittäminen](hr-benefits-setup-parameters.md).
- **Henkilökohtaisen kontaktin kelpoisuusvaihtoehdot** – Henkilökohtaiset yhteyshenkilöt ovat henkilöitä, jotka ovat joko riippuvaisia tai edunsaajia määritetyille palvelupaketeille. Tyypillisesti he ovat lapsia, puolisoita tai säätiöorganisaatioita. Katso lisätietoja kohdasta [Henkilökohtaisten yhteyshenkilöiden oikeutusasetusten määrittäminen](hr-benefits-setup-contact-eligibility-options.md).
- **Kattavuusvaihtoehdot** – Määritä paketin kattavuustyypit. Määritä erityisesti, kuka on katettu tai kuinka paljon vakuutusturvaa on saatavilla. Lisätietoja on kohdassa [Kattavuusvaihtoehtojen luominen](hr-benefits-setup-coverage-options.md).
- **Palvelupakettityypit** – Määritä palvelupakettityypit, jotka ovat käytettävissä etusuunnitelmaa luotaessa. Esimerkkejä pakettityypeistä ovat **Hampaat**, **Näkö** ja **Säästö**. Jotkin pakettityypin tärkeät asetukset määrittävät etuussuunnitelmassa käytettävissä olevat asetukset. Lisätietoja on kohdassa [Suunnitelmatyyppien luominen](hr-benefits-setup-plan-types.md).
- **Kelpoisuussääntöjen** avulla määritetään, omko työntekijä oikeutettu palvelupakettiin. Jokaiseen etuussuunnitelmaan on liityttävä vähintään yksi kelpoisuussääntö. Katso lisätietoja kohdasta [Kelpoisuussääntöjen ja -vaihtoehtojen määrittäminen](hr-benefits-setup-eligibility-rules.md).
- **Maksutiheydet** – Maksutiheydet ovat pakollisia, kun etuushinnat on määritetty. Maksutiheys, jota hinnalle käytetään, auttaa tunnistamaan summan, jonka työntekijä ja/tai työnantaja on velkaa viikoittain, kuukausittain tai vuosittain. Lisätietoja: [Maksutiheyksien määrittäminen](hr-benefits-setup-payment-frequencies.md).
- **Hinnat** – Hinnat määrittävät, kuinka paljon etuus maksaa joko työntekijälle tai työnantajalle. Jos rahaa pitäisi kohdentaa takaisin työntekijälle (esimerkiksi luotto kuntosalijäsenyydelle), syötetään negatiivinen hinta. Lisätietoja on kohdassa [Hintojen määrittäminen](hr-benefits-setup-rates.md).
- **Tasohinnat** – Tasohintoja käytetään, kun hinnan on muututtava joidenkin ehtojen perusteella. Yleisin tasohinta on yksi taso, joka perustuu ikään. Kaksitasoisia hintoja voidaan kuitenkin määrittää myös, jolloin kurssi voi muuttua sukupuolen, iän tai muiden kriteerien perusteella.
- **Vähennykset** – Vähennykset ovat pohjimmiltaan otsikkotietoja/-koodeja, jotka välitetään palkanlaskentajärjestelmään edun vähennyksen yksilöimiseksi. Nämä vähennykset on määritettävä, koska ne vaaditaan etuussuunnitelmassa. Lisätietoja on kohdassa [Vähennysten määrittäminen](hr-benefits-setup-deductions.md).
- **Etuuskaudet** – Etuuskausi on kausi, jolloin työntekijöillä on etuusturva. Se tunnetaan myös paketin vuotena. Avoimet ilmoittautumisajat on myös määritetty tässä.

## <a name="set-up-optional-benefit-information"></a>Määritä valinnaiset etutiedot

Seuraavia osia ei tarvitse määrittää etusuunnitelman luomiseksi:

- **Ohjelmat** – Ohjelma on joukko etuja, joihin sovelletaan samoja kelpoisuussääntöjä. Esimerkiksi kaikki myyntiosastolla voivat saada matkapuhelimen.
- **Paketit** – Paketti on etujen ryhmä, jossa on valittava yksi palvelupaketti, ennen kuin lisäsuunnitelmien valintamahdollisuus on käytettävissä. Esimerkiksi korkeasti vähennyskelpoinen lääketieteellinen suunnitelma voidaan yhdistää terveyssäästötilisuunnitelmaan (HSA).
- **Elämäntapahtumatyypit** – Elämäntapahtumat ovat tapahtumia, jotka mahdollistavat työntekijän kattavuuden muuttamisen. Elinkaaritapahtumatyypit on linkitetty palvelupakettityyppiin. Esimerkiksi lääketieteellinen palvelupakettityyppi voi sallia muutoksia palvelupaketteihin syntymän tai adoption tai siviilisäädyn muutoksen vuoksi. Vakuutussuunnitelmatyyppi ei kuitenkaan välttämättä salli muutoksia elämäntapahtumien vuoksi. Lisätietoja on kohdassa [Elämäntapahtumatyyppien määrittäminen](hr-benefits-setup-life-event-types.md).
- **Odotuspäivät ja odotusajat** – Etuussuunnitelmalle voidaan asettaa kattavuuden odotusaika. Esimerkiksi vasta palkattu työntekijä voi rekisteröityä 401(k)-numeroon vasta kolmen kuukauden työsuhteen jälkeen. Tässä tapauksessa odotusaika on kolme kuukautta. Odotuspäiviä käytetään odotusaikana, jos uusia rekisteröintejä voidaan käsitellä ja lähettää palveluntarjoajalle vain tiettynä kuukauden päivänä. Jos esimerkiksi 401(k) ilmoittautumista voidaan käsitellä vain kuukauden viidentenätoista päivänä, kolmen kuukauden työsuhteen jälkeen, asetettu odotusaika on kolme kuukautta ja odotuspäivä viidestoista. Lisätietoja on aiheissa [Odotuspäivien määrittäminen](hr-benefits-setup-waiting-days.md) ja [Odotusaikojen määrittäminen](hr-benefits-setup-waiting-periods.md).
- **Syykoodit** – Syykoodeja käytetään selittämään, miksi etu saattaa muuttua työntekijälle. Lisätietoja on kohdassa [Syykoodien määrittäminen](hr-benefits-setup-reason-codes.md).

## <a name="set-up-benefit-plans"></a>Etusuunnitelmien määrittäminen

Kun määrität etusuunnitelman, sinun on suoritettava seuraavat vaiheet, ennen kuin työntekijät voidaan rekisteröidä:

- Etuusjakson määrittäminen.
- Liitä kattavuusvaihtoehdot.
- Määritä kelvollinen alkamispäivämäärä ja kelvollinen päättymispäivämäärä **Yleiset**-välilehdessä.
- Määritä vähintään yksi kelpoisuussääntö.
- Määritä **Salli/jatka rekisteröinti** -kenttä **Asetukset**-välilehdessä. 

Lisätietoja nimikkeiden etuuspalvelupakettien määrittämisestä on kohdassa [Etuuspalvelupakettien määrittäminen](hr-benefits-plans-setup.md).

## <a name="set-up-flex-credit-programs-optional"></a>Liukumahyvitysohjelmien määrittäminen (valinnainen)

Liukumahyvitysohjelmien avulla voit rekisteröidä työntekijöitä etuuksiin ennalta määrätyn joustohyvitysten määrän perusteella. Työntekijät voivat valita, miten he kohdistavat joustopisteensä. Jos työntekijät kuuluvat jo puolisonsa sairausvakuutuksen piiriin, heidän ei esimerkiksi tarvitse käyttää hyvityksiään sairausvakuutukseen. Siksi he saattavat haluta käyttää niitä sen sijaan muihin etuuksiin. Lisätietoja joustohyvitysohjelmista on kohdassa [Joustohyvitysohjelmien määritys](hr-benefits-plans-flex-credit-programs.md).

## <a name="configure-required-employee-information"></a>Määritä pakolliset työntekijätiedot

Ennen kuin voit rekisteröidä työntekijöitä etuuksiin, sinun on annettava heistä tarvittavat tiedot. 

Työntekijällä on oltava **Toimi** määritettynä. Työntekijälle voidaan määrittää **Toimi** **Työntekijä**- tai **Toimi**-sivuilla päivittämällä **Työntekijän määritys**. 

Seuraavaksi työntekijöiden on kuuluttava kiinteään palkkiojärjestelmään aloituspäivänä tai heillä on oltava **Vuotuinen etuuspalkka**. Ennen **Kiinteän kompensaation** liittämistä työntekijälle on määritettävä **Toimi**. 

> [!NOTE] 
> **Kiinteän kompensaation alkamispäivämäärä** ei voi olla ennen **Toimen määrityksen päivämäärää**.

Vaihtoehtoisesti, jos sinulla on työntekijä, joka saa lisäkompensaation, kuten provisioita, voit lisätä **Etuuksien vuosipalkka** -summan työntekijätietueesta. Human Resources käyttää **Etuuksien vuosipalkka** -summaa määrittämään katetut summat **Kiinteän vuosittaisen kompensaatio** -summan sijaan. **Etuuksien vuosipalkan** on oltava voimassa työntekijän alkamispäivästä tai etuuskauden alusta sen mukaan, kumpi on uudempi. **Etujen vuosipalkan** kohdistaminen ei kuitenkaan ole tarpeen. Voit ottaa **Etujen vuosipalkan** käyttöön **henkilöstöhallinnon jaetut parametrit** -sivulla **Etujenhallinta**-välilehdessä. Tämä toiminto on oletusarvoisesti poissa käytöstä.

> [!IMPORTANT]
> Jos työntekijälle syötetään sekä **kiinteän kompensaation** että **etuuksien vuosipalkan** summa, **etuuksien vuosipalkkaa** käytetään katettavien summien määrittämiseen. **Työn tiedot** -osassa **Työntekijä**-sivulla on valittava arvo kentässä **Etuuksien maksutiheys**.

## <a name="configure-optional-employee-information"></a>Määritä valinnaiset työntekijätiedot
Kun luot etuussuunnitelman, joka käyttää sukupuoleen tai ikään perustuvia kursseja, sinun on syötettävä työntekijän syntymäpäivämäärä ja sukupuoli, jotta voit laskea etuuskustannuksen.

## <a name="process-employees-to-determine-eligibility"></a>Käsittele työntekijät oikeutuksen määrittämiseksi
Ennen kuin työntekijät voidaan rekisteröidä palvelupaketteihin, kelpoisuuskäsittely suoritetaan sen määrittämiseksi, mihin paketteihin he ovat oikeutettuja. Voit tarkastella kelpoisuusprosessin tuloksia prosessin **tulosten katseluohjelmassa**. Lisätietoja on kohdassa [Rekisteröimisen kelpoisuuden käsittely](hr-benefits-process-enrollment-eligibility.md).

## <a name="employees-select-plans-using-employee-self-service-optional"></a>Työntekijät valitsevat palvelupaketit **työntekijän itsepalvelun** avulla (valinnainen)

Kun avoin ilmoittautuminen tapahtuu, työntekijät on juuri palkattu, tai tapahtuu elämäntapahtuma, työntekijät voivat valita tai päivittää etunsa **Työntekijän itsepalvelun** kautta. Lisätietoja on kohdassa [Työntekijän itsepalvelun määrittäminen](hr-benefits-setup-employee-self-service.md).

## <a name="confirm-employee-plan-selections"></a>Vahvista työntekijöiden palvelupakettivalinnat

Työntekijöiden valitsemat edut on vahvistettava, ennen kuin työntekijät katsotaan ilmoittautuneiksi niihin. Edut voidaan valita myös työntekijän puolesta. Jos haluat valita tai vahvistaa edut, valitse **Työntekijä**-sivun **Edut**-välilehdessä **Työsuhde-etuussuunnitelmat**. Jos haluat valita tai vahvistaa useiden työntekijöiden edut, käytä **Työetusuunnitelmien joukkopäivitys** -sivua.

## <a name="life-event-processing-optional"></a>Elinkaaritapahtuman käsittely (valinnainen)

Työntekijän elinkaaren aikana jokainen työntekijä voi kokea erilaisia elämäntapahtumia, kuten avioliiton, työsuhteen muutoksia tai muutoksia huollettavissa tai edunsaajissa. Jos haluat käyttää elämäntapahtumia, sinun on otettava ne käyttöön **Henkilöstöresurssien jaetut parametrit** -sivulla. Määritä palvelupakettityyppien elinkaaritapahtumatyypit ja elinkaaritapahtuma-asetukset.

Ennen kuin voit käsitellä elämäntapahtumia, avoin rekisteröinti on suoritettava vähintään kerran palkkausjakson aikana. Yhdysvalloissa avoin rekisteröityminen järjestetään tyypillisesti kerran vuodessa. Yhdysvaltojen ulkopuolella avoin rekisteröityminen saatetaan suorittaa palkkauksen yhteydessä. Elämäntapahtuman käsittely ei edellytä, että työntekijät valitsevat etuussuunnitelman. Työntekijöiden on kuitenkin täytynyt olla mukana avoimessa ilmoittautumiskäsittelyssä. Lisätietoja on seuraavissa aiheissa:

- [Elämäntapahtumien käsittely](hr-benefits-process-life-events.md)
- [Elämäntapahtumien muutosten käsittely](hr-benefits-process-life-event-changes.md)
- [Elämäntapahtumien oikeutusten käsittely](hr-benefits-process-life-event-eligibility.md)

Kun elämäntapahtuman käsittely on suoritettu loppuun ja niin kauan kuin elämäntapahtuman rekisteröinti on avoinna, työntekijät voivat tehdä muutoksia suunnitelman asetuksiin, joihin elämäntapahtuma vaikuttaa. Järjestelmänvalvojat voivat tehdä muutoksia työntekijöiden puolesta. Kun rekisteröintikausi on päättynyt eikä mitään vahvistamattomia suunnitelmatyyppejä liity elämäntapahtuman transaktioon, transaktio suljetaan.

Kaikkien niiden suunnitelmien, joihin elämäntapahtuma vaikuttaa, on oltava joko valittu tai peruutettava ja vahvistettava. Jos suunnitelmaa ei ole valittu, eikä sitä peruuteta eikä sitä ole siten vahvistettu, elämäntapahtuman transaktiota ei suljeta.

Järjestelmänvalvojat voivat tarvittaessa sulkea elämäntapahtuman transaktion manuaalisesti valitsemalla sen ja valitsemalla sitten **Sulje**. Jos transaktiossa on vahvistamattomia suunnitelmia ja järjestelmänvalvoja haluaa sulkea sen, elämäntapahtuman sulkeminen voi rajoittaa muokkausta näihin suunnitelmiin.

Suljettuja elämäntapahtumia ei voi poistaa.

Järjestelmänvalvojat voivat tarvittaessa avata uudelleen elämäntapahtuman transaktion manuaalisesti valitsemalla sen ja valitsemalla sitten **Avaa uudestaan**.

## <a name="rate-updates-optional"></a>Hintojen päivitykset (valinnainen)

Joskus etuuden määrä muuttuu palvelupaketin voimassaolokauden aikana. Jos haluat päivittää pakettiin jo rekisteröityneiden työntekijöiden hinnat, sinun on käsiteltävä hintamuutokset. Lisätietoja on kohdassa [Hinnanmuutosten käsittely](hr-benefits-process-rate-changes.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
