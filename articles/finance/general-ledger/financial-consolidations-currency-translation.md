---
title: Taloushallinnon konsolidoinnit ja valuutan muunto – yleiskatsaus
description: Tässä artikkelissa käsitellään kirjanpidon taloushallinnon konsolidointeja ja valuutan muuntoja.
author: jinniew
ms.date: 10/07/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 1b2f5f56e757e89339c12fd41c59848b4c987a2f
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831830"
---
# <a name="financial-consolidations-and-currency-translation-overview"></a>Taloushallinnon konsolidoinnit ja valuutan muunto – yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään tapaa, jolla sekä Microsoft Dynamics 365 Finance että talousraportointi tekevät konsolidointeja. Siinä käsitellään skenaarioita, joihin sisältyy monen yrityksen raportointi, koonti, eliminointi ja vähimmäisosuus. Siinä selitään myös, miten käsitellään erikoistilanteita, kuten skenaarioita, joissa yrityksillä on erilaiset tilikaudet tai tilikartat.

Tämä artikkeli on kirjoitettu käyttäjille ja toiminnallisille konsulteille. Siinä oletetaan, että lukijoilla on yleistason tietämys Financesta ja taloushallinnon raportoinnista. Perusasetuksia ei käsitellä.

> [!NOTE]
> Financessa käytetään termiä *yritys*, kun taas taloushallinnon raportoinnissa puhutaan usein *yhtiöstä*. Kumpaakin termiä käytetään tässä artikkelissa. Tämän artikkelin tarkoituksen kannalta niiden merkityksessä ei ole eroa.

## <a name="audience"></a>Yleisö
Tämä artikkeli on tarkoitettu taloushallinnon ja kirjanpidon käyttäjille sekä sovelluskonsulteille, jotka haluavat konsolidoida Finance and Reportingin sekä taloushallinnon raportoinnin avulla monen yrityksen tietoja ja tietoja, joissa on käytössä monta valuuttaa.

## <a name="approach"></a>Menetelmä
Finance käsittelee konsolidoinnin erillisen yrityksen avulla. Tällä tavoin konsolidointi voidaan tehdä yhdessä esiintymässä samalla, kun tietoja on mahdollista tuoda muista lähteistä. Konsolidointiprosessi on suoritettava aina, kun lähdeyrityksiin tehdään muutoksia.

Taloushallinnon raportointi voi konsolidoida useita yrityksiä raportin laatimisen aikana. Vaikka tiedot tallennetaan tietovaraston osajoukkoon, versioidaan ja voidaan viedä, kukin lähdeyritys omistaa tietosäilön. Raportin voi suorittaa milloin tahansa vaikkapa minuutin välein. Siinä monia lisäetuja, kuten mahdollisuus porautua kaikkiin yrityksiin ja dimensioihin.

Käyttäjät voivat käyttää verkossa konsolidointia, taloushallinnon raportointia tai näiden yhdistelmää. Valinta määräytyy yrityksen tarpeiden ja tilintarkastajien mieltymysten mukaan.

## <a name="consolidations"></a>Konsolidoinnit
**Konsolidoinnit**-moduuli sisältää asetukset monen yrityksen konsolidointiin konsolidointiprosessin aikana sekä yrityksen taseen tuontiin ja vientiin. Voit määrittää myös eliminointeja ja kirjat eliminoinnin kirjauskansioita.

## <a name="benefits-of-using-consolidate-online"></a>Verkossa tapahtuvan konsolidoinnin edut
**Konsolidoinnit**-moduulia käyttävät asiakkaat saavat erilaisia etuja:

- **Tietojen yksityiskohtaisuus** – Voit luoda konsolidoituja raportteja, jotka yhdistävät toteutuneet ja budjetin tiedot sekä tili- että dimensiotasolla.
- **Dynaamiset konsolidoinnit** – konsolidoinnit voidaan käsitellä useita kertoja.
- **Valvontatoiminnot** – Dimensioita ja tilejä ylläpidetään analyysia ja valvontaa varten ja taseet luodaan päivämäärän mukaan.
- **Valuutan muunto** – Voit määrittää tilialueet ja kurssit muunnettavaksi lähdeyrityksen kirjanpitovaluutasta konsolidointiyrityksen kirjanpitovaluuttaan.
- **Eliminointien käsittely konsolidointi- tai eliminointiyrityksenä** – Voit käsitellä ja kirjat eliminoinnit yhtenä prosessina konsolidoinnin aikana. Voit suorittaa ehdotuksen myös erikseen.

## <a name="supported-consolidation-scenarios"></a>Tuetut konsolidointiskenaariot
Konsolidointi verkossa tukee esimerkiksi seuraavia konsolidointiskenaarioita:

- Yksitasoiset yritysten väliset konsolidoinnit
- Eliminointeja sisältävät konsolidoinnit
- Vähemmistöosuus (tässä skenaariossa yrityksessä on käytettävä manuaalista laskentaa ja vientiä)
- Useita yritysten välisiä tilikarttoja
- Erilaiset kirjanpidon kalenterit useiden yritysten välillä
- Useita raportointivaluuttoja sisältäviä konsolidointeja

## <a name="legal-entity-setup"></a>Yrityksen määritys
Yritys on määritettävä ennen konsolidoinnin käsittelyä. Voit suorittaa konsolidoinnin niin monta kertaa kuin on tarpeellista, ja kaikki tiedot muunnetaan lähdeyrityksen kirjanpito- tai raportointivaluutasta konsolidointiyritykselle määritettyyn valuuttaan. Niinpä jos seuraavassa organisaatiorakenteessa kaikkien pohjoisamerikkalaisten yritysten valuutta on ensin muutettava Yhdysvaltain dollareiksi (USD) ja sitten euroiksi (EUR), mikä on emoyrityksen valuutta, tarvitset ainakin kaksi konsolidointiyritystä.

![Organisaatiorakenne.](./media/organizational-structure.png "Organisaatiorakenne")

Edellisessä organisaatiorakenteessa tarvitset yrityksen Pohjois-Amerikan konsolidointia varten, koska konsolidoinnit konsolidoivat aina lähdeyrityksen kirjanpitovaluutasta konsolidointiyrityksen valuutaksi. Jos esimerkissä kaikki yritykset sisällytetään yhteen konsolidointiin, meksikolainen tytäryhtiö muunnetaan Meksikon pesoista (MXN) euroiksi (EUR) eikä pesoista dollareiksi (USD) ja sitten euroiksi.

Kun luot yrityksen, voit määrittää, käytetäänkö yritystä sekä konsolidointi- että eliminointiprosessiin tai vain toiseen prosessiin. Seuraavassa kuvassa yritystä käytetään kumpaankin prosessiin. Huomaa, ettet voi kirjata päivittäisiin kirjauskansioihin konsolidointiryrityksessä mutta voit kirjata ne eliminointiyrityksessä. Tämän vuoksi erillinen eliminointiyritys voi olla hyvä vaihtoehto.

![Sekä konsolidointiin että eliminointiin käytetty yritys.](./media/sep-elimination-company.png "Sekä konsolidointiin että eliminointiin käytetty yritys")

## <a name="main-accounts-and-consolidation-account-groups"></a>Päätilit ja konsolidointitiliryhmät
Sinun on valittava, miten tilikartat konsolidoidaan. Sinulla on konsolidointiprosessin aikana kolme vaihtoehtoa päätilien konsolidointiin.

Ensimmäinen vaihtoehto lähdeyritysten päätilien käyttäminen. Siinä tapauksessa kaikkien yritysten kaikki tilit konsolidoidaan. Jos käteinen on tilillä 100000 USMF-yrityksessä ja tilillä 1100 DEMF-yrityksessä, konsolidointiyritys sisältää molemmat tilit. Kullakin tilillä on oma saldo.

Toinen vaihtoehto on oletusarvoisen konsolidointilin määrittäminen **Päätilit**-sivulla. Tili yhdistetään sitten konsolidointitiliin. Tämä vaihtoehto voi olla hyödyllinen, jos tilikarttoja on useita tai yhdistäminen on tehtävä pääkonttorin määrittämään tilikarttaan.

![Päätilit-sivulla määritetty konsolidointitili.](./media/main-accounts.png "Päätilit-sivulla määritetty konsolidointitili")

Kolmas vaihtoehto on konsolidointitiliryhmien käyttäminen. Voit määrittää tarvittavan määrän konsolidointitiliryhmiä. Voit sitten yhdistää **Lisäkonsolidointitilit**-sivulla tilikartan päätilin ryhmän tarvitsemaan tiliin.

![Yhdistäminen Lisäkonsolidointitilit-sivulla.](./media/additional-consolidation-accounts.png "Yhdistäminen Lisäkonsolidointitilit-sivulla")

## <a name="consolidating-online"></a>Konsolidointi verkossa
Lisätietoja konsolidointitietojen antamisesta verkossa on kohdassa [Verkossa tapahtuva taloushallinnon konsolidointi](./consolidate-online.md).

## <a name="managing-consolidation-transactions"></a>Konsolidointitapahtumien hallinta
Konsolidoinnin tarkasteluvaihtoehtoja on useita:

- Luo konsolidointiyrityksessä raportti.
- Tarkastele **Pääkirja**-luettelosivua konsolidointiyrityksessä.
- Tarkastele **Konsolidoinnit**-sivun konsolidointiluettelossa saldoja, jotka on luotu päivämäärän mukaan kunkin lähdeyrityksen jokaiselle kaudelle.

    ![Konsolidointitapahtumat Konsolidoinnit-sivulla.](./media/managing-consolidation-transactions.png "Konsolidointitapahtumat Konsolidoinnit-sivulla")

Voit suorittaa konsolidoinnin uudelleen käsittelemällä sen. Vaihtoehtoisesti voit valita ensin **Poista tapahtumat** **Konsolidoinnit**-sivulla.
Jos konsolidointitilin saldot eivät ole oikein, nämä saldot voidaan korjata käyttämällä **Lopetuskauden oikaisut** -sivua.

## <a name="consolidate-with-import"></a>Konsolidoi tuonnin kanssa
Konsolidoi tuonnin kanssa -toiminto toimii Konsolidoi verkossa -toiminnon tavoin. Kun valitse yrityksiä, siirryt tiedot sisältävään lähdetiedostoon.

## <a name="export-company-balances"></a>Vie yrityksen saldot
Myös Vie yrityksen saldot -toiminto toimii Konsolidoi verkossa -toiminnon tavoin. Kun valitse yrityksiä, tiedostopolku määritetään tulosteelle.

## <a name="elimination-rules"></a>Eliminointisäännöt
Voit eliminoida konsernin sisäiset tapahtumat luomalla eliminointisäännön. Vaihtoehtoisesti voit tehdä manuaalisen eliminointimerkinnän yrityksessä, joka määritetty eliminointiyritykseksi. Jos luot eliminointisäännön, sinulla on kaksi eliminointimenetelmävaihtoehtoa: **Nettomuutos** ja **Kiinteä**.

### <a name="set-up-elimination-rules"></a>Määritä eliminointisääntöjä
Kun määrität eliminointisääntöjä Financessa, voit luoda nimenomaisesti eliminoinnissa käytettävän taloushallinnon dimension. Useimmat asiakkaat antavat tälle taloushallinnon dimensiolle nimen **Kauppakumppani** tai jotain vastaavaa. Jos et halua käyttää taloushallinnon dimensiota, varmista, että sinulla on päätilejä, joita käytetään vain konserniyritysten välisissä tapahtumissa.

Eliminointiasetukset ovat **Konsolidoinnit**-moduulin **Asetukset**-alueelta. Kun annat säännön kuvauksen, sinun on valittava yritys, johon eliminoinnin kirjauskansio kirjataan. Valitun yrityksissä on oltava **Käytetään taloushallinnon eliminointiprosessissa** valittuna.

Voit määrittää tarpeiden mukaisen päivämäärän, jolloin eliminointisääntö otetaan käyttöön, ja päivämäärän, jolloin se vanhenee. Jos haluat, että eliminointisääntö käytettävissä eliminoinnin ehdotusprosessissa, valitse **Aktiivinen**-asetukseksi **Kyllä**. Valitse kirjauskansion nimeksi **Eliminointi**-tyyppi.

![Eliminointisäännön perusominaisuudet.](./media/ledger-elimination-rule-journal.png "Eliminointisäännön perusominaisuudet")

Kun olet määritellyt perusominaisuudet, määritä todelliset käsittelysäännöt valitsemalla **Rivit**. Eliminointivaihtoehtoja on kaksi: voit eliminoida nettomuutossumman tai määrittää kiinteän summan.

Valitse lähdetilit. Voit käyttää tähteä (\*) yleismerkkinä. Esimerkiksi **1\**valitse kaikki _* 1**-alkuiset tilit kohdistuksen tietolähteenä.

Kun olet valinnut lähdetilin, käytä **Tilin määrittely** -kenttää määrittämään käytettävä tili kohdeyrityksestä. Valitse **Lähde**, jos haluat käyttää samaa, lähdetilissä määritettyä päätiliä. Jos valitset **Käyttäjän määrittämä**, sinun on määritettävä kohdetili.

![Kirjanpidon eliminointisääntörivi -sivu.](./media/ledger-elimination-rule-line.png "Kirjanpidon eliminointisääntörivi -sivu")

**Dimension määrittely** -kenttä toimii samalla tavoin kuin **Tilin määrittely** -kenttä. Valitse **Lähde**, jos haluat käyttää samoja dimensioita kohde- ja lähdeyrityksessä. Jos valitset **Käyttäjän määrittämä**, sinun on määritettävä kohdeyrityksen dimensiot valitsemalla **Kohdedimensiot**. Valitse sitten lähdedimensiot ja taloushallinnon dimensiot sekä eliminoinnin lähteenä käytettävät arvot.

### <a name="process-elimination-transactions"></a>Käsittele eliminointitapahtumia
Eliminointitapahtumat voidaan käsitellä kahdella tavalla. Tapahtuma voidaan käsitellä konsolidoinnin verkkoprosessin aikana tai voit luoda eliminoinnin kirjauskansion ja suorittaa eliminoinnin ehdotusprosessin. Tässä osassa käsitellään jälkimmäistä vaihtoehtoa.

Valitse eliminointiyritykseksi määritellyssä yrityksessä **Eliminoinnin kirjauskansio** **Konsolidoinnit**-moduulissa. Kun olet valinnut kirjauskansion nimen, valitse **Rivit**. Suorita ehdotus valitsemalla **Ehdotukset** \> **Eliminointiehdotus**.

Valitse yritys, joka on koottujen tietojen lähde, ja valitse sitten käsiteltävä sääntö. Määritä päivämääräalue antamalla alkamis- ja päättymispäivämäärät. Eliminointisummat haetaan tältä alueelta. **Kirjanpidon kirjauspäivä** -kenttä määrittää päivämäärän, jolloin kirjauskansio kirjataan kirjanpitoon. Sen jälkeen kun olet valinnut **OK**, voit tarkistaa määrät ja kirjata kirjauskansion.

> [!NOTE]
> Eliminointikirjauskansio näyttää tiliarvojen summat alkuperäisten tapahtumien valuutassa eikä kirjanpitovaluutassa. Kun tarkastelet eliminoinnin kirjauskansion summia, tämä voi vaikuttaa sekavalta.

Lisätietoja ja esimerkkejä on kohdassa [Eliminointisäännöt](./elimination-rules.md).

## <a name="currency-revaluation-in-a-consolidation-company"></a>Valuutan uudelleenarvostus konsolidointiyrityksessä
Kun konsolidoit tietoja yhdestä kirjanpitovaluutasta toiseen, valuutan uudelleenarvostus on silti suoritettava, jos vaihtokurssit muuttuvat, jotta tilien saldot on uudelleenarvostettu oikein. Kun konsolidoit tiedot ensimmäisen kerran, valitse **Valuutan muuntaminen** -välilehdessä ensimmäiset vaihtokurssit, joita käytetään muuntamiseen konsolidointiprosessin aikana. Kun uusi vaihtokurssi on syötetty (esimerkiksi seuraavana kuukautena), sinun on uudelleenarvostettava tilisaldot. Toteutumattomat voitot tai tappiot päivitetään sitten tämän uuden vaihtokurssin ja päivämäärän perusteella.

Lisätietoja valuutan uudelleenarvostuksesta konsolidointiyrityksessä on kohdassa [Valuutan uudelleenarvostus konsolidointiyrityksessä](currency-revaluation-consolidation-company.md).

Lisätietoja valuutan uudelleenarvostuksesta **Kirjanpito**-moduulissa on kohdassa [Kirjanpidon ulkomaanvaluutan uudelleenarvostus](./foreign-currency-revaluation-general-ledger.md).

### <a name="additional-information"></a>Lisätiedot
- Kaikki kirjanpitotasot konsolidoidaan, kun konsolidointi käsitellään.
- Eliminointikirjauskansiot voidaan kirjata vain valitulle tasolle.
- Vain operatiiviset saldot konsolidoidaan. Niinpä alkusaldon näkemistä varten on suoritettava tilikauden lopetus konsolidointiyrityksessä.
- Voit kirjata päivittäisiin kirjauskansioihin eliminointiyrityksessä muttet konsolidointiryrityksessä.
- Konsolidointiyrityksen saldoja voi oikaista vain **Lopetuskauden oikaisut** -sivun avulla. 

## <a name="benefits-of-using-financial-reporting-for-financial-consolidations-and-currency-translation-or-to-complement-consolidate-online-for-consolidated-reporting"></a>Taloushallinnon raportoinnin käytön edut taloushallinnon konsolidoinneissa ja valuutan muunnossa tai verkossa tapahtuvan konsolidoinnin täydentämisessä konsolidoidussa raportoinnissa
Asiakkaat, jotka käyttävät taloushallinnon raportointia taloushallinnon konsolidoinneissa ja valuutan muunnossa tai verkossa tapahtuvan konsolidoinnin täydentämisessä konsolidoidussa raportoinnissa, saavat erilaisia etuja:

- **Tietojen yksityiskohtaisuus** – Voit luoda konsolidoituja raportteja, jotka yhdistävät toteutuneet ja budjetin tiedot sekä tili- että dimensiotasolla. Financessa nämä tiedot sisältävät sekä budjetin hallinnan että budjetin suunnittelun tietoja.
- **Dynaamiset konsolidoinnit** – Konsolidoinnit voivat tehdä milloin tahansa ja millä tahansa organisaation hierarkiatasolla.
- **Täydelliset valvontatoiminnot** – Kaikki dimensioita, tilejä ja tapahtumatietoja ylläpidetään analyysia ja valvontaa varten. Lisäksi taloushallinnon raportointi sisältää täydellisen porautumisen alkuperäiseen tapahtumaan missä tahansa konsolidoidussa yrityksessä.
- **Sujuva valuutan muunto** – Kun Financessa on tehty muutamia asetuksia, voit muuntaa taloushallinnon raportoinnin raportin yhdeksi määritetyistä raportointivaluutoista. Voit lisäksi määrittää rajoittamattoman määrän raportointivaluuttoja.
- **Eliminointien kirjaaminen lähteessä** – Voit luoda ja tulostaa eliminointiraportin eliminointitapahtumien tarkistamista varten. Voit sitten kirjat uudet eliminoinnit tavallisina konsernin sisäisinä tapahtumina. Voit käyttää eliminointiyritystä missä tahansa tapahtumassa, jota et halua yrityksiin.

## <a name="supported-consolidation-scenarios-for-financial-reporting"></a>Financial Reportingin tuetut konsolidointiskenaariot

Taloushallinnan raportointi tukee esimerkiksi seuraavia konsolidointiskenaarioita:

- Yksi- ja monitasoiset yritysten väliset konsolidoinnit
- Yrityksistä luotuja organisaatiorakenteita käyttävät konsolidoinnit
- Eliminointeja sisältävät konsolidoinnit
- Vähemmistöosuus
- Useita yritysten välisiä tilikarttoja
- Erilaiset kirjanpidon kalenterit useiden yritysten välillä
- Useita raportointivaluuttoja sisältäviä konsolidointeja
- Liiketoimintayksikön konsolidoinnit

## <a name="generating-consolidated-financial-statements"></a>Konsolidoitujen raporttien laatiminen
Lisätietoja skenaarioista, joissa voidaan laatia konsolidoituja raportteja, on kohdassa [Konsolidoitujen raporttien laatiminen](./generating-consolidated-financial-statements.md).

## <a name="performance-enhancement-for-large-consolidations"></a>Suurten konsolidointien suorituskyvyn parannus

Ympäristöissä, joissa on useita kirjanpitotapahtumia, voidaan suorittaa hitaammin kuin on optimaalista. Voit korjata tämän ongelman asettamalla rinnakkaiskäsittelyn erille, jotka käyttävät käyttäjän määrittämiä päivämääriä. Varmista, että ratkaisu toimii suunnitellulla tavalla, lisäämällä konsolidointiin laajennuspiste päivämäärävälien säilön palauttamiseksi. Peruskäyttöönoton pitäisi sisältää yhden päivämäärävälin konsolidoinnin aloitus- ja päättymispäiville. Perustoteutuksen päivämäärävälit tarkistetaan, jotta varmistetaan, ettei niissä ole aukkoja tai päällekkäisyyksiä. Päivämäärävälien avulla luodaan rinnakkaisia eränippuja kullekin yritykselle.

Voit mukauttaa päivämäärävälien määrää organisaation vaatimusten mukaisesti. Päivämäärävälien määrää mukauttamalla voit helpottaa testausta ja pienentää vaikutusta aiemmin luotuun koodiin, koska kohdistuslogiikkaa ei ole. Ainoat pakolliset uudet testit vahvistavat eränippujen luomisen, päivämäärävälit ja testin päivämäärävälien osajoukon sen varmistamiseksi, että eriä voi yhdistää lopulliseen erätehtävään. 

Tämä ominaisuus parantaa kirjanpidon konsolidointiprosessia, kun prosessi suoritetaan erätyönä. Parannus parantaa kirjanpidon konsolidointiprosessin suorituskykyä jakamalla konsolidoinnin useisiin tehtäviin, jotka voidaan käsitellä rinnakkain. Konsolidoinnin suorituksen oletusmenetelmässä jokainen tehtävä käsittelee kahdeksan päivän mittaisen kauden kirjanpitoaktiviteetteja. On kuitenkin lisätty laajennuspiste, jonka avulla voit mukauttaa luotujen tehtävien määrää.

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää **Toimintojen hallinnan** työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** Kirjanpito
- **Ominaisuuden nimi:** Suurten konsolidointien suorituskyvyn parannus

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
