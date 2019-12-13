---
title: Sähköisen kaupankäynnin arviointiympäristön määrittäminen
description: Tässä oppaassa on vaiheittaiset ohjeet Microsoft Dynamics 365 Commerce Preview -ympäristön valmistelusta ja määrittämisestä.
author: v-chgri
manager: annbe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0dce2796e69cd8dee87cba176a521c26c81eb1a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771677"
---
# <a name="configure-an-e-commerce-evaluation-environment"></a>Sähköisen kaupankäynnin arviointiympäristön määrittäminen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä oppaassa on vaiheittaiset ohjeet Microsoft Dynamics 365 Commerce Preview -ympäristön valmistelusta ja määrittämisestä. Ennen kuin aloitat, kannattaa lukaista dokumentaation läpi. Näin saat käsityksen siitä, millainen prosessi on ja mitä opas sisältää.

*Huomautus: Jos sinulle ei ole vielä myönnetty Microsoft Dynamics 365 Commerce Preview -sovelluksen käyttöoikeutta, voit pyytää esiversion käyttöoikeuden [Commerce-sivuston](https://aka.ms/Dynamics365CommerceWebsite) avulla.*

## <a name="summary"></a>Yhteenveto
Ympäristön valmistelu onnistuu, jos luotavalla projektilla on tietty nimi ja tyyppi. Ympäristöllä ja Retail Cloud Scale Unit -ratkaisulla on myös joitakin tiettyjä parametreja, joita on käytettävä sähköisen kaupankäynnin valmistelussa myöhemmin. Tässä oppaassa olevat ohjeet sisältävät tiedot kaikista suoritettavista vaiheista ja käytettävistä parametreista.

Kun valmistelu on tehty, esiversioympäristössä tehdään muutama valmistelun jälkeinen vaihe. Jotkin vaiheet ovat valinnaisia. Tämä riippuu siitä, mitä järjestelmän alueita haluat arvioida. Jos muutat mielesi myöhemmin, voit suorittaa valinnaiset vaiheet myöhemmin.

Jos haluat lisätietoja valmistelun vaiheista tai jos kohtaat ongelmia, ota yhteyttä [Microsoft Dynamics 365 Commerce Preview Yammer -ryhmän](https://aka.ms/Dynamics365CommercePreviewYammer) kautta. 

## <a name="prerequisites"></a>Edellytykset
Seuraavassa kerrotaan Dynamics 365 Preview -ympäristön valmistelun edellytykset:
* Sinulla on **Lifecycle Services -portaalin (LCS)** käyttöoikeus
* Sinut on **hyväksytty Dynamics 365 Commerce Preview -ohjelmaan**
* Sinulla on projektin luomisessa vaaditut **Mahdolliset myyntiä edeltävät toimet**- tai **Siirrä, luo ratkaisuja ja opi** -kohtien oikeudet
* Olet **Ympäristövastaava**- tai **Projektin omistaja** -roolin jäsen projektissa, jolle valmistelet ympäristöä
* Sinulla on järjestelmänvalvojan oikeudet Azure-tilausta varten, tai ota yhteyttä tilauksen järjestelmänvalvojaan, joka voi suorittaa puolestasi järjestelmänvalvojan oikeudet vaativat kaksi vaihetta
* Sinulla on käytettävissä **AAD-vuokralaisen tunnus**
* Olet luonut **AAD-käyttöoikeusryhmän**, jota käytetään **sähköisen kaupankäynnin järjestelmänvalvojien ryhmänä**, ja sinulla on ryhmän tunnus
* Olet luonut **AAD-käyttöoikeusryhmän**, jota käytetään **luokitusten ja arvosteluiden valvojien ryhmänä** ja sinulla on sen tunnus (joka voi olla sama käyttöoikeusryhmä kuin yllä mainittu järjestelmänvalvojien ryhmä)
## <a name="provisioning-preview-environment"></a>Esiversioympäristön valmistelu
Näissä ohjeissa käsitellään Microsoft Dynamics 365 Commerce Preview -ympäristön valmistelua. Kun olet suorittanut nämä vaiheet, esiversioympäristö on valmis määritettäväksi. Kaikki tässä kuvatut toiminnot tapahtuvat LCS-portaalissa.

*Huomaa, että esiversion käyttöoikeus on sidottu LCS-tiliin ja -organisaatioon, jonka olet määrittänyt esiversiosovelluksessa. Tätä samaa tiliä on käytettävä valmistelun yhteydessä. Jos haluat käyttää toista LCS-tiliä tai -vuokralaista esiversioympäristössä, sinun on annettava nämä tiedot. Yhteystiedot löytyvät alla olevasta Lisäresurssit-kohdasta.*
### <a name="before-starting"></a>Ennen kuin aloitat
##### <a name="grant-access-to-e-commerce-applications"></a>Sähköisen kaupankäynnin sovellusten käyttöoikeuden myöntäminen

*Huomautus: **Sisäänkirjautuvan henkilön on oltava AAD-vuokraajan järjestelmänvalvoja**. Jos tämän vaiheen suorittaminen epäonnistuu, myös loput valmisteluvaiheet epäonnistuvat.*

1. Tässä vaiheessa tarvitaan **AAD-vuokraajan tunnus**. Azure-tilauksen käyttäminen edellyttää sähköisen kaupankäynnin sovellusten hyväksyntää. Helpoin tapa toteuttaa tämä on koota URL-osoite näin:

https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345

2. **Älä valitse URL-osoitetta suoraan**, vaan kopioi ja liitä se selaimeen tai tekstieditoriin ja korvaa **\{AAD_TENANT_ID\}** omalla **AAD-vuokraajan tunnuksellasi** ennen kuin siirryt URL-osoitteeseen.
3. Näyttöön tulee Microsoft AAD -sisäänkirjausvalintaikkuna, jossa voit vahvistaa, että haluat myöntää tilaukselle Dynamics 365 Commerce (Preview) -käyttöoikeuden.
4. Näyttöön avautuu toiminnon onnistumisen vahvistava sivu.

##### <a name="log-in-to-the-lcs"></a>Kirjautuminen LCS-portaaliin
1. Kirjaudu LSC-portaaliin: https://lcs.dynamics.com
1. Varmista, että olet kirjautunut saman LCS-tilin avulla, jota käytit Preview-käyttöoikeutta pyytäessäsi.
##### <a name="confirm-that-preview-features-are-available-and-enabled"></a>Tarkista, että esiversio-ominaisuudet ovat käytettävissä ja että ne on otettu käyttöön
1. Vieritä LCS:n etusivua oikeaan reunaan ja valitse **Esiversio-ominaisuuksien hallinta** -ruutu.
1. Vieritä YKSITYISEN ESIVERSION OMINAISUUDET -kohtaan ja varmista, että seuraavat ominaisuudet ovat käytettävissä ja että ne on otettu käyttöön:
    1. **Sähköisen kaupankäynnin arviointi**
    1. **Commerce Preview -ohjelman ympäristöt**
1. Jos näitä toimintoja ei näy luettelossa, ota yhteyttä työsähköpostin avulla ja kerro LCS-tilin ja vuokralaisen tiedot. Lisätietoja yhteydenotosta on alla olevassa **Lisäresurssit**-kohdassa.

![Esiversion hallinta -ruutu](./media/preview1.png)

![Esiversio-ominaisuudet](./media/preview2.png)
### <a name="create-project"></a>Luo projekti
##### <a name="creating-new-project"></a>Uuden projektin luominen
1. Luo uusi projekti valitsemalla **+**.
1. Jos olet kumppani, valitse **Siirrä, luo ratkaisuja ja opi**.
1. Jos olet asiakas, valitse **Mahdolliset myyntiä edeltävät toimet**.
1. Kirjoita nimi, kuvaus ja toimiala parhaaksi katsomallaan tavalla.
1. Valitse **Tuotenimi**-kohdassa **Dynamics 365 Retail**.
1. Valitse **Tuotteen versio** -kohdassa **Dynamics 365 Retail**.
1. Valitse **Metodologia**-kohdassa **Dynamics Retail -implementointimetodologia**.
1. Voit tuoda halutessasi rooleja ja käyttäjiä aiemmin luodusta projektista.
1. Valitse **Luo**.
1. Sinut siirretään projektinäkymään.
##### <a name="add-azure-connector"></a>Azure-yhdistimen lisääminen
1. Jos olet kumppani, valitse **Projektin asetukset** oikealla olevista työkaluruuduista.
1. Jos olet asiakas, valitse ylävalikosta **Projektin asetukset**.
1. Valitse **Azure-yhdistimet**.
1. Lisää Azure-yhdistin valitsemalla **+ Lisää**.
1. Kirjoita nimi.
1. Anna **Azure-tilauksen tunnus**.
1. Ota käyttöön **Määritä Azuren resurssienhallinta (ARM) käyttöön**.
1. Varmista, että **Azure-tilauksen AAD-vuokraajan toimialue (tai tunnus)** on määritetty oikein. Ota tarvittaessa yhteys Azure-tilauksen järjestelmänvalvojaan.
1. Valitse **Seuraava**.
1. Noudata näyttöön tulevia ohjeita ja myönnä tilaukselle tarvittavien sovellusten käyttöoikeudet. Ota tarvittaessa yhteys Azure-tilauksen järjestelmänvalvojaan seuraavasti:
    1. Kirjaudu Azure-portaaliin: https://portal.azure.com/
    1. Varmista, että olet valinnut oikean hakemiston.
    1. Valitse olevasta valikosta **Tilaukset**.
    1. Etsi oikea tilaus luettelosta ja valitse se. Käytä tarvittaessa hakua.
    1. Valitse valikosta **Käyttöoikeuksien hallinta (IAM)**.
    1. Valitse **Lisää** oikealla olevassa **Lisää roolin määritys** -kohdassa. **Lisää roolin määritys** -ruutu avautuu.
    1. Valitse **Rooli**-kohdassa **Osallistuja**.
    1. Jätä **Delegoi käyttöoikeus** -kohtaan **Azure AD -käyttäjä, -ryhmä tai -palveluobjekti** -arvo.
    1. Syötä **Valitse**-kohtaan **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Valitse luettelosta **Dynamics-käyttöönoton palvelut Services [käytössä wsfed]**.
    1. Valitse **Tallenna**.
1. Valitse **Seuraava**.
1. Noudata näyttöön tulevia ohjeita ja myönnä tilaukselle tarvittavien sovellusten käyttöoikeudet. Ota tarvittaessa yhteys Azure-tilauksen järjestelmänvalvojaan.
1. Valitse **Seuraava**.
1. Valitse **Azure-alue**-kohtaan **Itä-Yhdysvallat**, **Itä-Yhdysvallat 2**, **Länsi-Yhdysvallat** tai **Länsi-Yhdysvallat 2**.
1. Valitse **Yhdistä**.
1. Azure-yhdistin näkyy luettelossa.
### <a name="import-extension"></a>Laajennuksen tuominen
1. Siirry takaisin projektin etusivulle valitsemalla projektin nimi näytön yläosasta.
1. Jos olet kumppani, valitse **Resurssikirjasto** oikealla olevista työkaluruuduista.
1. Jos olet asiakas, valitse ylävalikosta **Resurssikirjasto**.
1. Valitse vasemmalla olevasta luettelosta **Käyttöönotettava ohjelmistopaketti**.
1. Valitse toimintoruudussa **TUO**.
1. Valitse **Commerce Preview -esittelyn peruslaajennus** **JAETTU RESURSSIKIRJASTO** -kohdan resurssiluettelosta.
1. Valitse **Kerää**.
1. Sinut siirretään resurssikirjastoon. Laajennuksen tulisi näkyä luettelossa.

![Projektin luominen - versiot](./media/import.png)
### <a name="deploy-environment"></a>Käyttöönottoympäristö

*Huomautus: Vaiheet 6, 7 ja/tai 8 eivät välttämättä ole näkyvissä, koska yhden valinnan sisältävät näytöt ohitetaan. Kun näkyvissä on **Ympäristöparametrit**-näkymä, vahvista, että Dynamics 365 Commerce (Preview) - esittely (10.0.6 ja Platform update 30) -teksti on heti **Ympäristön nimi** -kentän yläpuolella. Katso alla oleva näyttökuva.*

1. Valitse päävalikosta **Pilvipalveluympäristöt**.
1. Lisää ympäristö valitsemalla **+ Lisää**.
1. Valitse **Sovelluksen versio** -kohdassa **10.0.6**.
1. Valitse **Ympäristön versio** -kohdassa **Platform Update 30**.
1. Valitse **Seuraava**.
1. Valitse ympäristön topologian arvoksi **ESITTELY**.
1. Valitse ympäristön topologian arvoksi **Dynamics 365 Commerce (Preview) - esittely**.
1. Jos olet määrittänyt aiemmin yhden Azure-yhdistimen, sitä käytetään tässä ympäristössä. Jos määritit useita Azure-yhdistimiä, voit valita haluamasi yhdistimen seuraavista: **Itä-Yhdysvallat**, **Itä-Yhdysvallat 2**, **Länsi-Yhdysvallat** tai **Länsi-Yhdysvallat 2** (suositellaan parasta kokonaisvaltaista suorituskykyä varten)
1. Anna **ympäristön nimi**.
1. Säädä virtuaalikoneen kokoa parhaaksi katsomallaan tavalla. (Suosittelemme virtuaalikoneen varastointiyksiköksi **D13 v2** -arvoa.)
1. Älä muuta **Lisäasetukset**-kohtaa.
1. Kun olet tarkistanut hinnoittelu- ja käyttöoikeusehdot näytössä, valitse sopimuksen ruutu.
1. Valitse **Seuraava**.
1. Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistusnäytössä, valitse **Ota käyttöön**.
1. Sinut siirretään **Pilvipalveluympäristöt**-näkymään ja ympäristösi pitäisi näkyä luettelossa.
1. Pyydetty ympäristö näkyy jonossa. Tämän jälkeen se otetaan käyttöön. Ympäristön työnkulkujen valmistumiseen menee jonkin aikaa. Palaa takaisin muutaman tunnin kuluttua (noin 6-9 tuntia).
1. Varmista ennen jatkamista, että ympäristön tila on **Otettu käyttöön**.

![Projektin luominen - versiot](./media/project1.png)

![Projektin luominen - topologia 1](./media/project2.png)

![Projektin luominen - topologia 2](./media/project3.png)

![Projektin luominen - ympäristöparametrit](./media/project4.png)
### <a name="initialize-rcsu"></a>RCSU:n alustaminen
1. Valitse **Pilvipalveluympäristöt**-näkymässä luettelosta ympäristösi.
1. Valitse näytön oikeassa reunassa olevassa ympäristönäkymästä **Täydet tiedot**. Näkyviin tulee ympäristön tietojen näkymä.
1. Valitse **YMPÄRISTÖN OMINAISUUDET** -kohdassa **Hallitse**.
1. Valitse **Vähittäismyynti**-välilehdessä **Alusta**. Näkyviin tulee RCSU-alustusparametrien näkymä.
1. Valitse **ALUE**-kohtaan **Itä-Yhdysvallat**, **Itä-Yhdysvallat 2**, **Länsi-Yhdysvallat** tai **Länsi-Yhdysvallat 2**.
1. Valitse **VERSIO**-kohdassa ensin **Määritä versio** avattavasta luettelosta ja valitse sitten alle näkyviin tulevaan tekstikenttään **9.16.19262.5**. *Huomautus: Varmista, että **määrität tarkan version** luettelosta, jotta RCSU-versiota ei tarvitse päivittää myöhemmin oikeaksi.*
1. Ota käyttöön **Käytä laajennusta**.
1. Valitse laajennusluettelosta **Commerce Preview -esittelyn peruslaajennus**.
1. Napsauta **Alusta**.
1. Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistusnäytössä, valitse **Kyllä**.
1. Palaat **Vähittäismyynnin hallinta** -näkymään, jossa on auki **Vähittäismyynti**-välilehti. RCSU on asetettu jonoon valmistelua varten.
1. Odota, kunnes RCSU:n tila on **ONNISTUI**, ennen kuin jatkat (kestää noin 2-5 tuntia).
### <a name="initialize-e-commerce"></a>Sähköisen kaupankäynnin alustaminen
1. Siirry **Sähköinen kaupankäynti (esiversio)** -välilehteen.
1. Kun olet tarkistanut esiversion suostumuksen, valitse **Asetukset**.
1. Kirjoita **sähköisen kaupankäynnin vuokraajan nimi**. Ota huomioon, että tämä nimi näkyy joissakin sähköisen kaupankäynnin esiintymään vievissä URL-osoitteissa.
1. Valitse **Retail Cloud Scale Unit -nimeksi** luettelosta RCSU (luettelossa pitäisi olla vain yksi vaihtoehto).
1. **Sähköisen kaupankäynnin maantieteellinen alue** täytetään automaattisesti. Arvoa ei voi muuttaa.
1. Jatka valitsemalla **Seuraava**.
1. Anna **Tuetut isäntänimet** -kohtaan sallittu toimialue (esimerkiksi www.fabrikam.com).
1. Anna **Järjestelmänvalvojan AAD-käyttöoikeusryhmä** -kohtaan AAD-käyttöoikeusryhmän tunnus, jota haluat käyttää sähköisen kaupankäynnin järjestelmänvalvojan ryhmänä
1. Anna **Luokitusten ja arvostelujen valvojan AAD-käyttöoikeusryhmä** -kohtaan se AAD-käyttöoikeusryhmän tunnus, jota haluat käyttää luokitusten ja arvostelujen valvojan ryhmänä.
1. Jätä **Kuluttajakauppa**-kenttien arvot tyhjiksi (7 kenttää, jotka alkavat kuluttajakauppa-sanalla).
1. Jätä **Ota luokitus- ja arviointipalvelu käyttöön** -kohta valituksi.
1. Napsauta **Alusta**.
1. Palaat **Vähittäismyynnin hallinta** -näkymään, jossa on auki **Sähköinen kaupankäynti (esiversio)**-välilehti. Sähköisen kaupankäynnin alustaminen on aloitettu.
1. Ennen kuin jatkat, odota, kunnes sähköisen kaupankäynnin alustamisen tila on **ALUSTAMINEN ONNISTUI**.
1. **LINKIT**-kohdassa alhaalla oikealla.
    * Laita **Sähköisen kaupankäynnin sivusto** -linkki muistiin. Tämä on linkki C2-pääsivuston.
    * Laita **Sähköisen kaupankäynnin hallintatyökalu** -linkki muistiin. Tämä on sivuston hallintatyökalun linkki (C1-muokkaustyökalu).
## <a name="post-provisioning-steps"></a>Valmistelun jälkeiset vaiheet
Tässä vaiheessa ympäristö on valmisteltu alusta loppuun. Ennen ympäristön arvioimista on kuitenkin suoritettava määritysvaiheet.
### <a name="before-starting"></a>Ennen kuin aloitat
1. Valitse päävalikosta **Pilvipalveluympäristöt**.
1. Valitse ympäristö luettelosta.
1. Valitse ympäristön tiedoista oikealla oleva **Täydet tiedot**.
1. Avaa valikko valitsemalla **Kirjaudu sisään** ja valitse sitten **Kirjaudu ympäristöön**.

Varmista, että valittuna on **USRT**-yritys (oikealla yläkulmassa).

### <a name="configure-pos"></a>Konfiguroi POS
##### <a name="associate-worker-with-your-identity"></a>Työntekijän liittäminen tunnukseen
1. Valitse vasemmalla olevasta valikosta **Moduulit > Vähittäismyynti > Työntekijät > Työntekijät**.
1. Etsi ja valitse luettelosta **000713 - Andrew Collette** -tietue.
1. Valitse toimintoruudussa **Vähittäismyynti**.
1. Valitse **Liitä aiemmin luotu tunnus**.
1. Kirjoita **Sähköposti**-kenttään (**Hae sähköpostiosoitteen avulla** -kohdan oikealla puolelle) sähköpostiosoite.
1. Valitse **Haku**.
1. Valitse tietue, joka sisältää nimesi.
1. Valitse **OK**.
1. Valitse **Tallenna**.
##### <a name="activate-cloud-pos"></a>Pilvipalvelun myyntipisteen aktivoiminen
1. Kirjaudu LSC-portaaliin.
1. Siirry projektiin.
1. Valitse päävalikosta **Pilvipalveluympäristöt**.
1. Valitse ympäristö luettelosta.
1. Valitse ympäristön tiedoista oikealla oleva **Täydet tiedot**.
1. Avaa valikko valitsemalla **Kirjaudu sisään**. Valitse **Kirjaudu pilvimyyntipisteeseen**. Myyntipiste latautuu.
1. Valitse **Seuraava**.
1. Kirjaudu sisään AAD-tilin avulla.
1. Valitse **Myymälän nimi** -kohdassa **San Francisco**.
1. Valitse **Seuraava**.
1. Valitse **Kassakone ja laite** -kohdassa **SANFRAN-1**.
1. Valitse **Aktivoi**.
1. Sinut kirjataan ulos, näkyviin tulee myyntipisteen sisäänkirjausnäyttö.
1. Voit nyt kirjautua pilvimyyntipistekokemukseen operaattorin tunnuksella **000713** ja salasanalla **123**.
### <a name="site-setup"></a>Sivuston asetukset
1. Kirjaudu **sivuston hallintatyökaluun** käyttämällä aiemmin mainittua URL-osoitetta.
1. Avaa sivuston asetusvalintaikkuna valitsemalla **Fabrikam**-sivusto.
1. Valitse toimialueeksi aiemmin sähköisen kaupankäynnin alustuksessa syötetty toimialue.
1. Valitse oletuskanavaksi **Fabrikamin laajennettu verkkokauppa**. *Huomautus: Varmista, että valitset **laajennetun** verkkokaupan*
1. Valitse oletuskieleksi **en-us**.
1. Älä muuta **polun** asetuksia.
1. Valitse **OK**.
1. Sinut siirretään sivuston sivuluetteloon.
### <a name="enable-jobs"></a>Töiden ottaminen käyttöön
1. Kirjaudu sisään ympäristöön (pääkonttori).
1. Siirry vasemmalla olevan valikon avulla kohtaan **Vähittäismyynti > Kyselyt ja raportit > Erätyöt**.
1. Suorita jokaiselle alla olevan luettelon työlle seuraavat vaiheet:
    * **Vähittäismyyntitilauksen sähköposti-ilmoituksen käsittely**.
    * **Tuotteen saatavuus**.
    * **P-0001**.
    * **Synkronoi tilaukset -työ**.
1. Hae työ pikasuodattimen avulla käyttämällä sen nimeä (lueteltu yllä).
1. Jos työn tila on **Pidätä**, suorita seuraavat vaiheet:
    1. Valitse tietue.
    1. Avaa toimintoruudussa **Erätyö**-valintanauha ja valitse **Muuta tila**.
    1. Valitse **Odottaa** ja valitse sitten **OK**.
### <a name="run-full-data-sync"></a>Suorita täydellinen tietojen synkronointi
1. Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit > Vähittäismyynti > Headquarters-asetukset > Retail-ajastus > Kanavan tietokanta**.
1. Vasemmalla olevasta luettelosta valitaan **oletuskanava**. *Valitse toinen käytettävissä oleva kanava (nimeltä **scXXXXXXXXX**)*.
1. Valitse toimintoruudusta **Täydellinen tiedon synkronointi**.
1. Syötä jakeluaikatauluksi **9999**.
1. Valitse **OK**.
1. Valitse **OK**.
### <a name="after-these-steps-you-are-ready-to-start-evaluating-your-preview-environment"></a>Näiden vaiheiden jälkeen olet valmis arvioimaan esiversioympäristön.
Siirry C1-muokkauskokemukseen käyttämällä **Sähköisen kaupankäynnin hallintatyökalu** -URL-osoitetta ja C2-sivustokokemukseen käyttämällä **Sähköisen kaupankäynnin sivusto** -URL-osoitetta.

## <a name="additional-resources"></a>Lisäresurssit
### <a name="how-to-find-your-aad-tenant-id"></a>Miten AAD-vuokraajan tunnus löytyy
AAD-vuokraajan tunnus on GUID. Se voi olla esimerkiksi tällainen: **72f988bf-86f1-41af-91ab-2d7cd011db47**
##### <a name="from-azure-portal"></a>Azure-portaalista
1. Kirjaudu Azure-portaaliin: https://portal.azure.com/
1. Varmista, että olet valinnut oikean hakemiston.
1. Valitse vasemmalla olevasta valikosta **Azure Active Directory**.
1. Valitse **Ominaisuudet** **Hallinta**-kohdassa.
1. AAD-vuokraajan tunnus näkyy **Hakemuksen tunnus** -kohdassa.
##### <a name="from-openid-connect-metadata"></a>OpenID-yhteyden metatiedoista
Luo **OpenID-URL-osoite** korvaamalla **\{YOUR_DOMAIN\}** omalla toimialueella, esimerkiksi microsoft.com: esimerkiksi osoitteesta https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration tulee osoite https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration

1. Siirry **OpenID-URL-osoitteeseen**, joka sisältää toimialueesi.
1. AAD-vuokraajan tunnus näkyy usean ominaisuuden arvoissa.
1. Etsi **authorization_endpoint** ja pura GUID heti osoitteen **login.microsoftonline.com/** jälkeen.
### <a name="how-to-find-the-id-of-your-aad-security-group"></a>Lisätietoja AAD-käyttöoikeusryhmän tunnuksen etsimisestä
AAD-käyttöoikeusryhmän tunnus on GUID. Se voi olla esimerkiksi tällainen: **436ea7f5-ee6c-40c1-9f08-825c5811066a**

Tässä vaiheessa oletetaan, että käyttäjä on sen ryhmän jäsen, jonka tunnusta etsitään.
1. Siirry Graph-työkalun testaukseen: https://developer.microsoft.com/en-us/graph/graph-explorer#
1. Valitse **Kirjaudu sisään Microsoftin avulla** ja kirjaudu sisään tunnistetietojen avulla.
1. Kun olet kirjautunut sisään, valitse näytön vasemmassa laidassa oleva **Näytä lisää malleja** -kohta.
1. Ota **ryhmät** käyttöön oikeanpuoleisesta ruudusta.
1. Sulje oikeanpuoleinen ruutu.
1. Valitse **kaikki ryhmät, joihin kuulun**.
1. Etsi ryhmä **Vastauksen esikatselu** -tekstiruudusta.
1. Käyttöoikeusryhmän tunnus merkitään ominaisuuden **tunnukseen**.
### <a name="test-credit-card-information-to-perform-test-purchases"></a>Luottokortin testitiedot testiostojen suorittamista varten
Voit käyttää seuraavia luottokortin testitietoja sivuston testitapahtumien suorittamisessa:

Kortin numero: 4111-1111-1111-1111, vanhenee: 10/20, CVV: 737

*Huomautus: Älä milloinkaan yritä käyttää testisivustossa todellisia luottokortin tietoja.*
### <a name="useful-links"></a>Hyödyllisiä linkkejä
* [LCS (Lifecycle services)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)
* [RCSU (Retail Cloud Scale Unit)](https://docs.microsoft.com/en-us/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)
* [Microsoft Azure -portaali](https://azure.microsoft.com/en-us/features/azure-portal)
* [Dynamics 365 Commerce -sivusto](https://aka.ms/Dynamics365CommerceWebsite)
* [Dynamics 365 Retailin ohjeresurssit](../retail/index.md)
### <a name="microsoft-dynamics-365-commerce-preview-support"></a>Microsoft Dynamics 365 Commerce Preview -tuki
Jos valmisteluvaiheiden aikana on ongelmia, saat apua [Microsoft Dynamics 365 Commerce Preview Yammer -ryhmästä](https://aka.ms/Dynamics365CommercePreviewYammer). 

Jos et pääse käyttämään Yammer-ryhmää, voit lähettää sähköpostia osoitteeseen **Dynamics365Commerce@microsoft.com**. Tätä sähköpostiosoitetta ei seurata aktiivisesti, joten vastauksen saaminen voi kestää jonkin aikaa.
***
## <a name="prerequisites-for-optional-features"></a>Valinnaisten ominaisuuksien edellytykset
Jos haluat arvioida tapahtuman sähköpostiominaisuuksia, seuraavat edellytykset on täytettävä:
* Käytettävissä on sähköpostipalvelin (SMTP-palvelin), jota voi käyttää sen Azure-tilauksen kanssa, jossa esiversioympäristö valmisteltiin.
* Sinulla on käytettävissä palvelimen FQDN/IP, SMTP-portin numero ja todennustiedot.

Jos haluat arvioida digitaalisten resurssien hallintaominaisuuksia ja erityisesti käyttää uuden monikanavan kuvia, seuraavien edellytysten on täytyttävä:
* Käytettävissä on **CMS-vuokraajan nimi**. Alla ovat ohjeet, joiden avulla tämä nimi löytyy.
### <a name="configure-image-backend-optional"></a>Taustalla olevan kuvan määrittäminen (valinnainen)
##### <a name="finding-your-media-base-url"></a>Median URL-perusosoitteen löytäminen
*Huomautus: Ennen kuin voit suorittaa tämän vaiheen, sinun on suoritettava **sivuston asetukset**.*
1. Kirjaudu sivuston hallintatyökaluun käyttämällä aiemmin mainittua URL-osoitetta.
1. Avaa **Fabrikam**-sivusto.
1. Valitse vasemmalla olevasta valikosta **Resurssit**.
1. Valitse jokin yksittäinen kuvaresurssi.
1. Etsi **julkinen URL-osoite** oikealla olevan ominaisuuden tarkistustoiminnon avulla. Se sisältää URL-osoitteen.
    * URL-osoite-esimerkki: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC
1. Korvaa URL-osoitteen viimeinen tunniste (MA1nQC yllä olevassa URL-osoite-esimerkissä) seuraavalla merkkijonolla: **search?fileName=**
    * URL-osoite-esimerkki korvaamisen jälkeen: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=
    * Tämä on **median URL-perusosoite**. Kirjoita se muistiin.
##### <a name="updating-the-media-base-url"></a>Median URL-perusosoitteen päivittäminen
1. Kirjaudu sisään ympäristöön (pääkonttori).
1. Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit > Vähittäismyynti > Kanavan asetukset > Kanavaprofiilit**.
1. Valitse **Muokkaa**.
1. Korvaa **Profiilin ominaisuudet**, korvaa **Mediapalvelimen URL-perusosoite** -kohdan arvo aiemmin luodulla **Median URL-perusosoite** -kohdan arvolla.
1. Valitse toinen kanava vasemmalla olevasta luettelosta **Oletuskanava**-kohdassa.
1. Valitse **Profiilin ominaisuudet** -kohdassa **+ Lisää**.
1. Valitse lisätylle ominaisuudelle **Mediapalvelimen URL-perusosoite** ominaisuuden avaimeksi ja syötä ominaisuuden arvolle aiemmin luotu **Median URL-perusosoite**.
1. Valitse **Tallenna**.

### <a name="configure-email-server-optional"></a>Sähköpostipalvelimen määrittäminen (valinnainen)
Ota huomioon, että tähän syötettävän SMTP-palvelimen tai sähköpostipalvelun on oltava käytettävissä ympäristössä käytettävän Azure-tilauksen avulla.
1. Kirjaudu sisään ympäristöön (pääkonttori).
1. Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit > Vähittäismyynti > Headquarters-asetukset > Parametrit > Sähköpostiparametrit**.
1. Valitse **SMTP-asetukset**-välilehti.
1. Kirjoita **SMTP-välityspalvelimen nimi -kenttään** SMTP-palvelimen tai sähköpostipalvelun FQDN tai IP-osoite.
1. Kirjoita portin numero **SMTP-portin numero** -kenttään (oletusarvo on 25, kun käytössä ei ole SSL).
1. Kirjoita **Käyttäjänimi**-kenttään arvo (jos todennus on pakollinen).
1. Kirjoita **Salasana**-kenttään arvo (jos todennus on pakollinen).
1. Valitse **Tallenna**.
1. Valitse **Päivitä**.
1. Valitse **Testisähköpostiviesti**-välilehti.
1. Valitse Sähköpostipalvelu-kentässä **SMTP**.
1. Kirjoita **Lähetä**-kenttään sähköpostiosoite, johon haluat testisähköpostiviestin toimitettavan.
1. Valitse **Lähetä testisähköpostiviesti**.
### <a name="configure-email-templates-optional"></a>Sähköpostimallien määrittäminen (valinnainen)
Jokaisen tapahtuman sähköpostimalliin, josta haluat lähettää sähköposteja, on päivitettävä sallittu lähettäjän sähköpostiosoite.
1. Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit > Organisaation hallinta > Asetukset > Organisaation sähköpostimallit**.
1. Valitse **Näytä luettelo**.
1. Kaikki luettelon mallit:
    1. Kirjoita **Lähettäjän sähköposti** -kenttään tämän sähköpostimallin lähettäjän sähköpostiosoite.
    1. (Valinnainen) Kirjoita **Lähettäjän nimi** -kenttään nimi, jota haluat käyttää tämän sähköpostimallin lähettäjänä.
1. Valitse **Tallenna**.
### <a name="customizing-email-templates-optional"></a>Sähköpostimallien mukauttaminen (valinnainen)
Haluat ehkä päivittää sähköpostimallit käyttämään erilaisia kuvia tai mallien linkit sellaisiksi, että ne vievät takaisin esiversioympäristöön. Seuraavassa kerrotaan, miten oletusmallit ladataan ja mukautetaan ja miten järjestelmän mallit päivitetään.
1. Lataa selaimen avulla [Microsoft Dynamics 365 Commerce Preview -sovelluksen oletussähköpostimallien .zip-tiedosto](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip), joka sisältää seuraavat HTML-asiakirjat paikallista tietokonetta varten.
    1. Tilauksen vahvistuksen malli
    1. Lahjakorttimallin lähettäminen
    1. Uusi tilausmalli
    1. Pakkaustilauksen malli
    1. Keräystilauksen malli
1. Mukauta malleja teksti- tai HTML-editorin avulla. Lisätietoja on alla olevassa tuettujen tunnusten luettelossa.
1. Kirjaudu sisään ympäristöön (pääkonttori).
1. Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit > Vähittäismyynti > Headquarters-asetukset > Parametrit > Organisaation sähköpostimallit**.
1. Laajenna vasemmanpuoleista luetteloa, niin näet kaikki mallit.
1. Suorita seuraavat vaiheet kaikille malleille, joita haluat mukauttaa:
    1. Valitse malli luettelosta.
    1. Valitse **Sähköpostiviestin sisältö** -kohdassa soveltuva kieliversio luettelosta (oletuskieli on **en-us**).
    1. Valitse **Sähköpostiviestin sisältö** -kohdassa **Muokkaa**. Näkyviin tulee **Lataa sähköpostimalli** -ruutu.
    1. Valitse **Selaa** ja etsi HTML-tiedosto, jossa on mukautettua sisältöä.
    1. Valitse **Lataa**, jonka jälkeen malli ladataan järjestelmään ja näkyviin tulee esikatselu.
    1. Valitse **OK**.
    1. (Valinnainen) Mukauta mallin **Aihe**-ominaisuutta.
    1. Valitse **Tallenna**.

#### <a name="supported-tokens-in-the-email-template"></a>Sähköpostimallin tuetut tunnukset
Nämä tunnukset korvataan sähköpostin muodostusajalla ja todellisilla arvoilla, jotka koskevat asiakasta ja tämän tilausta.

**Myyntitilaus** - Seuraavat tunnukset koskevat yleistä myyntitilausta.

|Tunnuksen nimi|Tunnus|
|---|---|
|Tilausnumero|%salesid%|
|Asiakkaan nimi|%customername%|
|Toimitusosoite|%deliveryaddress%|
|Laskutusosoite|%customeraddress%|
|Tilauspäivämäärä|%shipdate%|
|Toimitustapa|%modeofdelivery%|
|Alennus|%discount%|
|Arvonlisävero|%tax%|
|Tilauksen kokonaissumma|%total%|

**Myyntirivi** - Jokaiselle tilauksen tuotteelle täytetään seuraavat tunnukset.

*Huomautus: Sijoita **Tuoteluettelo - alku**- ja **Tuoteluettelo - loppu** -tunnukset jokaisessa tuotteessa toistuvan HTML-lohkon alkuun ja loppuun.*

|Tunnuksen nimi|Tunnus|
|---|---|
|Tuoteluettelo - alku|\<!--%tablebegin.salesline% -->|
|Tuoteluettelo - loppu|\<!--%tableend.salesline%-->|
|Tuotteen nimi|%lineproductname%|
|Kuvaus|%lineproductdescription%|
|Määrä|%linequantity%|
|Rivin yksikköhinta|%lineprice% (verify)|
|rivinimikkeen kokonaissumma|%linenetamount%|
|rivin alennus|%linediscount%|
|Lähetyspäivä|%lineshipdate%|
|Hankintamenetelmä|%linedeliverymode%|
|toimitusosoite|%linedeliveryaddress%|
|Rivin myyntiyksikkö|%lineunit%|

