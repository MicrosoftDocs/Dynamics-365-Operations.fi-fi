---
title: Regression Suite Automation Tool -oppaan määrittäminen ja asentaminen
description: Tämä ohjeaihe on opas, joka käsittelee Regression Suite Automation Tool (RSAT) -työkalun määrittämistä ja asentamista.
author: robinarh
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 46115dc4a46be951517265197f76637ad3e63b78
ms.sourcegitcommit: b337b647a1be4908fc361fb6d962e96a69f301a9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/21/2021
ms.locfileid: "5036708"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool -oppaan määrittäminen ja asentaminen

Tämä opas auttaa RSAT-työkalun asennuksessa sekä RSAT-työkalun ja sen käyttöön liittyvien työkalujen käytön aloittamisessa.

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Lataa ja tallenna tämä tiedosto selaimen työkaluilla PDF-tiedostona.

## <a name="key-concepts"></a>Avainkäsitteet

- Tietoja Regression Suite Automation Tool (RSAT) -työkalua tukevien erilaisten sovellusten asennuksesta ja pakollisista määrityksistä.
- Tietoja tavasta, jolla in tehtävien tallennustoiminnolla yhdessä Microsoft Dynamics Lifecycle Servicesin (LCS) ja Microsoft Azure DevOpsin avulla voi luoda, määrittää, suorittaa, tutkia ja raportoida testitapauksia.
- Toimintokäyttäjille annetaan mahdollisuudet tallentaa liiketoimintatehtäviä tehtävien tallennustoiminnolla ja muuntaa sitten tehtävätallenteet automatisoiduiksi testeiksi – ilman lähdekoodin kirjoittamista.

## <a name="before-you-begin"></a>Ennen aloittamista

### <a name="prerequisites"></a>Edellytykset

- Oppaan käyttöä varten tarvitaan ympäristö, jossa on käytössä Microsoft Dynamics 365 for Finance and Operations -versio 10.0 (huhtikuu 2019) tai uudempi. Lisäksi tuetaan asiakkaita, joiden käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) tai uudempi.
- Käyttäjällä on oltava ympäristön järjestelmänvalvojan oikeudet.
- Asiakkaan vuokraajan LCS:n ja Azure DevOpsin (entinen Microsoft Visual Studio Team Services \[VSTS\]) käyttöoikeus.
- Testipaketteja luovalla ja hallitsevalla käyttäjällä on oltava Azure DevOps Test Plans- tai Test Manager -käyttöoikeus. Test Plans -käyttö on mahdollista seuraavilla käyttöoikeuksilla:
    - Visual Studio Enterprise -käyttöoikeus
    - Visual Studio Test Professional -käyttöoikeus
    - MSDN Platforms -tilaajan käyttöoikeus
- RSAT-työkalua on voitava käyttää testiympäristössä selaimen kautta.
- Microsoft Excel on oltava asennettuna testiparametrien luontia ja muokkausta varten.

## <a name="configure-azure-devops"></a>Konfiguroi Azure DevOps

### <a name="user-eligibility"></a>Käyttäjien kelpoisuus

Varmista, että käyttäjä on luotu Azure DevOpsissa ja että tilauksen taso mahdollistaa Azure Test Plans -käytön. Azure DevOps Test Plans -käyttöoikeus tarvitaan vain, jos käyttäjä luo ja hallitsee testitapauksia. (Toisin sanoen kaikki RSAT-käyttäjät eivät tarvitse tätä käyttöoikeutta.) Lisätietoja vaadittavista käyttöoikeuksista on kohdassa [Vaadittavat käyttöoikeudet](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).

### <a name="create-a-new-azure-devops-project"></a>Uuden Azure DevOps -projektin luominen

RSAT käyttää Azure DevOpsia testitapausten ja testipakettien hallintaan, raportointiin ja suoritettuihin testituloksiin perehtymiseen.

> [!NOTE]
> Voit käyttää aiemmin luotua Azure DevOps -projektia. Jos aiemmin luotuun Azure DevOps -projektiin on kuitenkin määritetty mukautettu malli, saat Epäonnistuneet VSTS-synkronoinnit -virheilmoituksen, kun synkronoit testitapauksia liiketoimintaprosessien mallintajasta (BPM) Azure DevOpsiin. (Lisätietoja on osassa [Synkronoinnin testaus liiketoimintaprosessien mallintajasta Azure DevOpsiin](#test-the-synchronization-from-bpm-to-azure-devops).) Jos mukautetussa mallissa on käytetty seuraavia parhaita käytäntöjä, testitapaukset voidaan synkronoida Azure DevOpsiin. (Nämä parhaat käytännöt on mainittu virheilmoituksessa.)

- Älä poista mitään työnimiketyyppejä tai valmiita kenttiä.
- Älä poista mitään työnimiketyyppien tiloja.
- Älä lisää mitään pakollisia kenttiä työnimiketyyppiin.

![Virheilmoitus ja parhaiden käytäntöjen luettelo](./media/setup_rsa_tool_02.png)

Muussa tapauksessa tässä oppaassa suositellaan uuden Azure DevOps -projektin luomista. Lisätietoja on kohdassa [Ongelmat synkronoitaessa liiketoimintaprosessien mallintajaan mukautetulla Azure DevOps (VSTS) -prosessimallilla](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).

1. Avaa Azure DevOpsin URL-osoite (`https://dev.azure.com/<Azure DevOps Name>`).
2. Valitse Azure DevOps -sivu oikeassa yläkulmassa **Luo projekti**.

    ![Luo projekti -painike](./media/setup_rsa_tool_03.png)

3. Täytä seuraavat kentät ja valitse **Luo**:

    - **Projektinimi**
    - **Versionhallinta** – Valitse **Team Foundation Version Control**. Huomaa, että oletusvaihtoehtoa **Git** ei tueta.
    - **Työnimikeprosessi**

    ![Luo uusi projekti -valintaikkuna](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a>Henkilökohtaisen käyttöoikeustunnuksen luominen

Tässä oppaassa testitapauskirjasto luodaan ja testitapaukset synkronoidaan Azure DevOpsin kanssa LCS:n liiketoimintaprosessien mallintajan (BPM) avulla. Tarvitset henkilökohtaisen käyttöoikeustunnuksen liiketoimintaprosessien mallintajan ja Azure DevOpsin synkronointiin.

1. Valitse Azure DevOps -projektisivun oikeassa yläkulmassa profiilikuvake ja valitse sitten **Suojaus**.

    ![Suojaus-komento](./media/setup_rsa_tool_05.png)

2. Valitse vasemman ruudun **Suojaus**-kohdassa **Henkilökohtaiset käyttöoikeustunnukset**. Valitse sitten **Uusi tunnus**.

    ![Uusi tunnus -painike käyttäjän asetusten Henkilökohtaiset käyttöoikeustunnukset -välilehdessä.](./media/setup_rsa_tool_06.png)

3. Täytä seuraavat kentät ja valitse **Luo**:

    - **Nimi**
    - **Vanhentuminen (UTC)** – valitse ensin **Mukautettu määritys** ja valitse sitten päivämäärävalitsimella viimeinen päivämäärä, jolloin tunnus on käytössä.
    - **Vaikutusalueet** – valitse **Täydet käyttöoikeudet** -vaihtoehto.

    ![Luo uusi henkilökohtainen käyttöoikeustunnus -valintaikkuna](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > Kirjoita luotu henkilökohtainen käyttöoikeustunnus muistiin. Tarvitset sitä myöhemmin RSAT-määrityksiä tehtäessä.

    ![Henkilökohtainen käyttöoikeustunnus](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a>LCS-projektin määrittäminen

Päätestikirjastoa varten tarvitaan Lifecycle Services (LCS) -projekti. LCS:n liiketoimintaprosessien mallintajaa (BPM) käytetään testitapausten pääkirjastona. Liiketoimintaprosessien mallintajan avulla hallitaan ja jaetaan LCS-projektien kirjastoja. Esimerkiksi testikirjastoja muodostava Microsoftin kumppani tai riippumaton ohjelmistotoimittaja (ISV) julkaisee testitapaukset BPM-kirjastoina. Liiketoimintaprosessien mallintajassa testitapaukset on järjestetty liiketoimintaprosessien perusteella. Liiketoimintaprosessien mallintaja ei määritä suoritusjärjestystä eikä testausvälejä. Näitä tietoja hallitaan Azure DevOpsissa myöhemmin tässä ohjeaiheessa käsiteltävällä tavalla.  

LCS-projektissa voidaan käyttää asiakkaan nykyistä käyttöönottoa tai kumppanin projektia.

### <a name="update-the-lcs-language"></a>LCS-kielen päivittäminen

> [!NOTE]
> Liiketoimintaprosessit näkyvät käyttöliittymässä oikein vain, LCS:n ensisijaiseksi kieleksi on määritetty **Englanti (Yhdysvallat)**.

1. Siirry LCS-käyttöönottoprojektiin.
2. Valitse **Asetukset**-painike (rataskuvake) oikeassa yläkulmassa ja valitse sitten **Kieliasetus**.

    ![Kieliasetuksen päivitys](./media/setup_rsa_tool_09.png)

3. Valitse **Ensisijainen kieli** -kentässä **Englanti (Yhdysvallat)** ja valitse sitten **Tallenna**.

    ![Käyttäjäasetusten Kieliasetus-välilehti](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a>LCS:n määrittäminen muodostamaan yhteys Azure DevOps -projektiin

Jos loit aiemmin uuden Azure DevOps-projektin, määritä LCS-projekti muodostamaan siihen yhteys. Jos LCS-projekti on kuitenkin jo yhdistetty Azure DevOps-projektiin, voit jatkaa seuraavaan osaan.

1. Siirry LCS-käyttöönottoprojektiin.
2. Valitse ensin **Valikko**-painike ja sitten **Projektiasetukset**.

    ![Projektiasetukset-komento](./media/setup_rsa_tool_11.png)

3. Valitse vasemmassa ruudussa ensin **Visual Studio Team Services** ja sitten **Määritä Visual Studio Team Services**.

    ![Projektiasetusten Visual Studio Team Services -välilehti:](./media/setup_rsa_tool_12.png)

4. Anna **Azure DevOps -sivuston URL-osoite** -kentässä Azure DevOps-sivuston URL-osoite. Anna **Henkilökohtainen käyttöoikeustunnus** -kentässä aiemmin luotu henkilökohtainen käyttöoikeustunnus.

    > [!NOTE]
    > Vaikka VSTS on nykyään Azure DevOps, käytä vanhaa URL-osoitetta, kun yhdistät LCS:n Azure DevOps-projektiin. Esimerkiksi tässä oppaassa käytetään seuraavaa Azure DevOpsin URL-osoitetta: `https://dev.azure.com/D365FOFastTrack/`. Seuraavassa kuvassa se on kuitenkin on muodossa `https://D365FOFastTrack.visualstudio.com/`.

    ![Visual Studio Team Servicesin määrittämisen vaihe 1](./media/setup_rsa_tool_13.png)

5. Valitse **Jatka**.
6. Valitse **Visual Studio Team Services -projekti** -kentässä valitun sivuston VSTS-projekti, joka yhdistetään LCS-projektiin. **Prosessimalli**-kentän asetuksena on oletusarvoisesti **Ketterä**. Tutustu mukautetun mallin parhaita käytäntöjä koskeviin ohjeisiin osassa [Uuden Azure DevOps-projektin luominen](#create-a-new-azure-devops-project). Valitse sitten **Jatka**.

    ![Visual Studio Team Servicesin määrittämisen vaihe 2](./media/setup_rsa_tool_14.png)

7. Tarkista asetukset ja valitse sitten **Tallenna**.

    ![Visual Studio Team Servicesin määrittämisen vaihe 3](./media/setup_rsa_tool_15.png)

8. Valitse **Valtuuta**. LCS on nyt valtuutettu käyttämään määritettyä Azure DevOps -sivustoa puolestasi ja ottamaan VSTS:n kanssa integroituvat toiminnot käyttöön.

    ![Valtuuta-painike](./media/setup_rsa_tool_16.png)

9. Avautuvassa viestiruudussa on seuraava ilmoitus: Sinut ohjataan ulkoiselle sivustolle, jossa voit valtuuttaa Lifecycle Servicesin muodostamaan yhteyden Visual Studio Team Services -palveluun puolestasi. Jatketaanko? Valitse **Kyllä**.

    ![Viestiruutu](./media/setup_rsa_tool_17.png)

10. Valitse **Hyväksy**.

    ![Käytön valtuuttaminen](./media/setup_rsa_tool_18.png)

11. Jos sinut valtuutetaan käyttäjäksi, käyttöliittymän pitäisi palautua LCS-projektin asetussivulle.

    ![Valtuutettu käyttäjä](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a>Uuden BPM-kirjaston luominen

1. Siirry LCS-käyttöönottoprojektiin.
2. Valitse ensin **Valikko**-painike ja sitten **Liiketoimintaprosessien mallintaja**.

    ![Liiketoimintaprosessien mallintaja -komento](./media/setup_rsa_tool_20.png)

3. Valitse **Uusi kirjasto**.

    ![Uusi kirjasto -painike](./media/setup_rsa_tool_21.png)

4. Anna **Kirjaston nimi** -kentässä nimi ja valitse sitten **Luo**. Tässä oppaassa BPM-kirjaston nimeksi annetaan **RSAT**.

    ![Luo uusi kirjasto -valintaikkuna](./media/setup_rsa_tool_22.png)

5. Avaa uusi **RSAT**-BPM-kirjasto.
6. Valitse **Ydinliiketoimintaprosessin malli** -prosessi ja valitse sitten oikealla **Muokkaustila**.

    ![Muokkaustila-painike](./media/setup_rsa_tool_23.png)

7. Vaihda sekä **Nimi**- että **Kuvaus**-kentän nimeksi **Luo tuote**. Valitse sitten **Tallenna**.

    ![Nimi- ja Kuvaus-kentät](./media/setup_rsa_tool_24.png)

## <a name="environment"></a>Ympäristö

### <a name="version-requirement"></a>Version vaatimus

Edellytyksenä on testi- tai eristysympäristö, jossa käytössä versio 10. Lisäksi tuetaan asiakkaita, joiden käytössä on versio7.3, Platform update 20 tai uudempi.

> [!NOTE]
> RSAT-työkalua on voitava käyttää testiympäristössä selaimen kautta.

### <a name="user-criteria"></a>Käyttäjän vaatimukset

Käyttäjällä on oltava ympäristön järjestelmänvalvojan oikeudet.

### <a name="set-up-help-settings-to-connect-with-lcs"></a>LCS:n yhdistämisen ohjeasetusten määrittäminen

Tämä vaihe on välttämätön muodostettaessa yhteyttä LCS:ään, sillä sen avulla tehtävätallenteet voidaan tallentaa sopivaan LCS:n BPM-kirjastoon asiakasohjelman avulla.

1. Avaa asiakasohjelma.
2. Valitse **Järjestelmän hallinta \> Asetukset \> Järjestelmän parametrit**.
3. Valitse **Ohje**-välilehden **Lifecycle Services -palvelun ohjeiden konfiguraatio** -kentässä soveltuva LCS-projekti (tässä oppaassa se on **RSAT**).

    ![Lifecycle Services -palvelun ohjeiden konfiguraatio -kenttä Ohje-välilehdessä](./media/setup_rsa_tool_25.png)

    Soveltuvan LCS-projektin BPM-kirjastot täytetään.

4. Valitse **Tallenna**.
5. Selain on ehkä päivitettävä, ennen kuin päivitetty Ohje-sisältö tulee näkyviin.

    ![Ilmoitus selaimen päivittämisestä](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a>Tehtävätallenteet

> [!NOTE]
> Varmista, että kaikki tehtävätallenteet käynnistyvät pääkoontinäytöstä. Yksittäiset tallenteet kannattaa pitää lyhyinä ja niissä kannattaa keskittyä yhteen liiketoimintatehtävään, kuten myyntitilauksen luontiin.

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a>Tehtävätallenteen luominen ja tallentaminen BPM-kirjastoon

Luo vastaava tehtävätallenne, jonka voit liittää uuteen BPM-kirjastoon luotuun yksinkertaiseen liiketoimintaprosessiin.

1. Avaa asiakasohjelma.
2. Valitse pääkoontinäytössä **Asetukset**-painike (rataskuvake) ja valitse sitten **Tehtävän tallennustoiminto**.

    ![Tehtävien tallennustoiminnon valitseminen Asetukset-valikossa](./media/setup_rsa_tool_27.png)

3. Valitse **Luo tallenne**.

    ![Luo tallenne -painike](./media/setup_rsa_tool_28.png)

4. Täytä **Tallenteen nimi**- ja **Tallenteen kuvaus** -kentät ja valitse sitten **Tallenna**.

    ![Tallenteen nimi- ja Tallenteen kuvaus -kentät](./media/setup_rsa_tool_29.png)

5. Tallenna tuotteen luontivaiheet. Kun olet valmis, lopeta tallennus valitsemalla **Pysäytä**.

    ![Tuotteen luontiohjeet](./media/setup_rsa_tool_30.png)

6. Valitse **Tallenna Lifecycle Servicesiin**.

    ![Tehtävien tallennustoiminnon tallentaminen Lifecycle Servicesiin](./media/setup_rsa_tool_31.png)

    Kirjaston tiedot ladataan LCS:stä.

    ![Kirjaston tietojen lataaminen](./media/setup_rsa_tool_32.png)

7. Valitse tehtävätallenteeseen liitettävä BPM-kirjasto. Tässä oppaassa valitaan aiemmin luotu **RSAT**-BPM-kirjasto ja siinä oleva **Luo tuote** -liiketoimintaprosessi. Valitse sitten **OK**.

    ![Tehtävätallenteen liittäminen BPM-kirjastoon ja liiketoimintaprosessiin](./media/setup_rsa_tool_33.png)

    Tallennus Lifecycle Servicesiin onnistui -sanoma avautuu.

    ![Sanoma onnistuneesta LCS-tallennuksesta](./media/setup_rsa_tool_34.png)

8. Jos haluat tallentaa tehtävätallenteen paikallisesti ja ladata sen sitten liiketoimintaprosessien mallintajaan LCS:n kautta, toimi seuraavasti:

    1. Kun tallenne on valmis, valitse **Tallenna tälle tietokoneelle**.

        ![Tallenna tälle tietokoneelle](./media/setup_rsa_tool_35.png)

    2. Tallenna tiedosto paikallisesti tietokoneeseen valitsemalla selaimen ilmoituspalkissa **Tallenna** tai **Tallenna nimellä**.

        ![Ilmoituspalkki](./media/setup_rsa_tool_36.png)

    3. Siirry **RSAT**-BPM-kirjasto ja valitse liiketoimintaprosessi, jonka tehtävätallenne tallennetaan.
    4. Valitse **Yleiskuvaus**-välilehdessä **Lataa palvelimeen**.

        ![Lataa palvelimeen -painike](./media/setup_rsa_tool_37.png)

    5. Valitse ensin **Selaa** ja sitten aiemmin tallennettu .axtr-tiedosto. Valitse sitten **Lataa palvelimeen**.

        ![Palvelimeen ladattavan. axtr-tiedoston valitseminen](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a>Liiketoimintaprosessien mallintajasta Azure DevOpsiin tapahtuvan synkronoinnin testaaminen

Nyt kun tehtävätallenne on liitetty liiketoimintaprosessiin, sinun on tarkistettava, että kyseinen liiketoimintaprosessi ja liitetty tehtävätallenne voidaan synkronoida Azure DevOpsiin ominaisuutena ja testitapauksena käyttämällä VSTS:n synkronointiominaisuutta LCS:ssä.

> [!NOTE]
> Azure DevOpsissa luotava vastaava työnimiketyyppi vaihtelee sen prosessimallin mukaan, joka valittiin, kun LCS-projekti määritettiin Azure DevOpsin kanssa osassa [Uuden Azure DevOps -projektin luominen](#create-a-new-azure-devops-project) kuvatulla tavalla.

1. Siirry BPM-kirjastoon ja avaa aiemmin luotu **RSAT**-kirjastoon.
2. Valitse ensin kolme pistettä -painike (**...**) ja sitten **VSTS-synkronointi**.

    ![Kolme pistettä -valikon VSTS-synkronointikomento](./media/setup_rsa_tool_39.png)

    Kun VSTS-synkronointi on valmis, vasemmalle avautuu **Tarpeet**-välilehti, jossa on vastaava Azure DevOps-työnimike.

    > [!NOTE]
    > Azure DevOpsissa luodussa työnimikkeessä BPM-kirjaston nimi on otsikon etuliitteenä.

    ![Tarpeet-välilehti](./media/setup_rsa_tool_40.png)

3. Päivitä sivu.
4. Valitse kolme pistettä (**...**) -painike. Näkyviin tulee lisäasetus **Synkronoi testitapaukset**. Valitse tämä vaihtoehto.

    ![Kolme pistettä -valikon Synkronoi testitapaukset -komento](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > Jos **Synkronoi testitapaukset** -vaihtoehto ei ole valittavissa sivun päivityksen jälkeen, siirry liiketoimintaprosessien mallintajan pääsivulle ja valitse koko kirjaston **Synkronoi testitapaukset**. Tällä tavoin voit pakottaa tehokkaasti koko kirjaston synkronoinnin.
    >
    > ![Koko kirjaston Synkronoi testitapaukset -asetuksen valitseminen](./media/setup_rsa_tool_42.png)

    Kun Synkronoi testitapaukset on valmis, **Tarpeet**-välilehteen luodaan uusi testitapaus.

    ![Uusi testitapaus Tarpeet-välilehdessä](./media/setup_rsa_tool_43.png)

5. Siirry Azure DevOps -projektiin ja valitse **Taulut \> Työnimikkeet**.

    ![Taulujen Työnimikkeet-komento](./media/setup_rsa_tool_44.png)

6. Tarkista, että BPM-synkronoinnilla luotu työnimike ja testitapaus ovat olemassa.

    ![Työnimike ja testitapaus](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a>RSAT-työkalun määrittäminen ja asentaminen

RSAT voidaan asentaa mihin tahansa tietokoneeseen, jossa on Windows 10 ja joka voidaan yhdistää ympäristöön selaimella (Internet Explorer tai Google Chrome).

> [!NOTE]
> Työkalun aiemman version asennus kannattaa poistaa ennen uuden version asentamista.

### <a name="install-an-authentication-certificate"></a>Todennuksen varmenteen asentaminen

Todenteen käyttöönottaminen edellyttää, että varmenne luodaan ja asennetaan siihen tietokoneeseen, jossa RSAT-työkalua käytetään.

#### <a name="generate-a-certificate"></a>Uuden varmenteen luominen

1. Luo varmennetiedosto avaamalla Microsoft Windowsin PowerShell-ikkuna järjestelmänvalvojana ja suorittamalla seuraava komento.

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. Avaa varmenteiden hallinta kirjoittamalla **certlm.msc** **Suorita**-valintaikkunaan ja vahvistamalla, että **Automaattinen D365-testausvarmenne** on luotu, valitsemalla **Henkilökohtainen \> Varmenteet**.

    > [!NOTE]
    > Varmista, että olet kirjoittanut **certlm.msc** eikä **certmgr.msc**, sillä varmenteet on tallennettu paikallisesti tietokoneeseen.

    ![Automatisoitu D365-testausvarmenne](./media/setup_rsa_tool_46.png)

3. Napsauta varmennetta hiiren kakkospainikkeella ja valitse sitten **Kopioi**.
4. Valitse **Luotetut varmenteiden päämyöntäjät \> Varmenteet**.

    ![Luotetut varmenteiden päämyöntäjät -kansiossa oleva Varmenteet-kansio](./media/setup_rsa_tool_47.png)

5. Valitse **Toiminto**-valikossa **Liitä**. Varmenne kopioidaan nyt **Luotetut varmenteiden päämyöntäjät** -sijaintiin.

    ![Toimintovalikon Liitä-komento](./media/setup_rsa_tool_48.png)

6. Saat asennetun varmenteen allekirjoituksen ilman välilyöntejä ja erikoismerkkejä avaamalla Windows PowerShell -ikkunan järjestelmänvalvojana ja suorittamalla seuraavat komennot.

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > Tallenna allekirjoitus, koska tarvitset sitä myöhemmin, kun päivität AOS-palvelimen .wif-tiedostot ja määrität RSAT-määritykset.

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a>AOS-tietokoneen määrittäminen luottamaan yhteyteen

> [!NOTE]
> Jos ympäristö on taso 2+ -ympäristö, **kaikkien** ympäristön AOS-tietokoneiden varmenteen allekirjoitus on päivitettävä wif.config-tiedostossa.

1. Muodosta RDP-etäkäyttöprotokollayhteys AOS-tietokoneeseen. Kirjautumistiedot ovat LCS:n ympäristön tietojen sivulla.
2. Avaa Microsoft Internet Information Services (IIS) ja etsi **AOSService** sivustoluettelossa.

    ![AOSService sivustoluettelossa](./media/setup_rsa_tool_49.png)

3. Napauta oikealla hiiren painikkeella **Selaa** avataksesi kansion **\<Drive\>: \\AosService\\WebRoot**. Etsi **wif.config**-tiedosto.

    ![Wif.config-tiedosto WebRoot-kansiossa](./media/setup_rsa_tool_50.png)

4. Päivitä **wif.config**-tiedosto lisäämällä varmenteen ja myöntäjän nimeen uusi myöntäjä, kuten seuraavassa esimerkissä.

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > Jos samalla sovelluksella on useita käyttäjiä, kunkin käyttäjän on luotava erillinen allekirjoitus ja kaikki nämä allekirjoitukset on lisättävä **\<keys\>**-osaan.

5. Jos AOS-tietokonetta on useita, toista vaiheet 3–4 kussakin tietokoneessa.

    > [!NOTE]
    > Vanhoista tason 2 ympäristöistä poiketen, uudet tason 2 ympäristöt otetaan käyttöön kahdessa AOS-esiintymässä.

6. Suorita **iisreset** kaikissa AOS-tietokoneissa.

    > [!NOTE]
    > Jos sinulla ei ole tarvittavia järjestelmänvalvojan oikeuksia **iisreset**-komennon suorittamiseen tason 1 tietokoneessa, valitse LCS:n Ympäristön tiedot -sivulla Ylläpidä > Käynnistä palvelut uudelleen.

#### <a name="tier-2-environment"></a>Tason 2+ ympäristö

Jos käytössä on tason 2+ (Standard-hyväksyntätestaus-eritysympäristö tai uudempi) ympäristö, varmista tai määritä seuraava rekisteriasetus siinä tietokoneessa, johon RSAT on asennettu. Tämä vaihe on pakollinen, koska sen avulla vältetään todennus- tai RSAT-yhteysvirheet.

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a>RSAT-työkalun asentaminen

1. Siirry sivustoon <https://www.microsoft.com/download/details.aspx?id=57357> ja valitse **Lataa**.
2. Valitse ensin kaikki tiedostot ja valitse sitten **Seuraava**.

    ![Kaikkien tiedostojen valitseminen](./media/setup_rsa_tool_51.png)

3. Suorita asennusohjelmalla kaksoisnapsauttamalla .msi-pakettia. Valitse asennuksen valmistumisen jälkeen **Valmis**.

    ![RSAT-asennusohjelmatiedosto](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a>Seleniumin ja selainohjaimien asentaminen

RSAT-työkalun vanhoissa versioissa oli asennettava Selenium ja selaimen ohjaimet. Näitä ohjaimia ei enää tarvitse asentaa, sillä ne asennetaan automaattisesti.

1. Kun avaat RSAT-työkalun ensimmäisen kerran, sinulla pyydetään automaattisesti lataamaan ja asentamaan Selenium. Lisätietoja on osassa [RSAT-työkalun määrittäminen](#configure-rsat).
2. Ennen kuin voit suorittaa testitapauksen, sinua pyydetään lataamaan ja asentamaan automaattisesti RSAT-määrityksissä valittua oletusselainta vastaava selaimen ohjain. Lisätietoja on osassa [Testitapausten lataaminen ja suorittaminen](#load-and-run-test-cases).

## <a name="get-started-with-rsat"></a>RSAT-työkalun käytön aloittaminen

### <a name="create-a-test-plan-and-test-suites"></a>Testisuunnitelman ja testipakettien luominen

1. Siirry Azure DevOps -projektiin ja valitse **Testisuunnitelmat**.

    ![Testisuunnitelmat-komento](./media/setup_rsa_tool_53.png)

2. Valitse **Uusi testisuunnitelma**.

    ![Uusi testisuunnitelma -painike](./media/setup_rsa_tool_54.png)

3. Täytä **Nimi**-kenttä ja valitse sitten **Luo**. Anna tässä oppaassa testisuunnitelman nimeksi **RSAT-testisuunnitelma**.

    ![Uusi testisuunnitelma -valintaikkuna](./media/setup_rsa_tool_55.png)

4. Luo uuteen testisuunnitelmaan staattinen sarja valitsemalla ensin plus-merkki (**+**) ja sitten **Staattinen sarja**. Annan uuden testisarjan nimeksi **T01 – Valmistus varastoon**.

    > [!NOTE]
    > Voit luoda myös kyselypohjaisen sarjan, jos haluat, että uudet liiketoimintaprosessien mallintajan uudet testitapaukset noudetaan automaattisesti RSAT-testisarjaan.

    ![Staattisen sarjan luominen](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a>Testitapausten liittäminen testisarjoihin

1. Lisää aiemmin luodut testitapaukset testisaraan valitsemalla oikealla puolella **Lisää aiemmin luotu**.

    ![Lisää aiemmin luotu -painike](./media/setup_rsa_tool_57.png)

2. Valitse **Lisää testitapaukset sarjaan** -sivulla **Tee kysely** ja valitse sitten testisarjaan lisättävä testitapaus. Valitse tässä oppaassa **Luo uusi tuote** -testitapaus. Valitse sitten **Lisää testitapauksia** sivun oikeassa alakulmassa (tämä painike ei näy seuraavassa kuvassa).

    ![Tee kysely -painike](./media/setup_rsa_tool_58.png)

    Testitapaus lisätään **T01–Valmista varastoon** -testisarjaan.

    ![Testisarjaan lisätty testitapaus](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a>Konfiguroi RSAT

1. Avaa RSAT.

    ![RSTA-kuvake](./media/setup_rsa_tool_60.png)

2. Saat varoitussanoman, jonka mukaan Regression Suite Automation Tool tarvitsee Seleniumia. Lisäksi sinulta kysytään, haluatko ladata ja asentaa sen nyt automaattisesti. Valitse **Kyllä**.

    ![Varoitussanoma, jonka mukaan Regression Suite Automation Tool edellyttää Seleniumia](./media/setup_rsa_tool_61.png)

3. Valitse oikeassa yläkulmassa **Asetukset**-painike (rataskuvake) ja täytä sitten seuraavat kentät avautuvassa valintaikkunassa:

    - **Azure DevOps -URL-osoite** – anna Azure DevOps -projektin URL-osoite, kuten `https://yourAzureDevOpsUrlHere.visualStudio.com`.
    - **Käyttöoikeustunnus** – Anna käyttöoikeustunnus, jonka avulla työkalu voi muodostaa yhteyden Azure DevOpsiin. Käytä aiemmin tässä oppaassa luotua henkilökohtaista käyttöoikeustunnusta. Lisätietoja on kohdassa [Käytön todentaminen henkilökohtaisilla käyttöoikeustunnuksilla](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).
    - **Projektin nimi** – valitse Azure DevOps -projektin nimi.
    - **Testisuunnitelma** – Valitse testitapaukset sisältävä Azure DevOps -testisuunnitelma. Lisätietoja on kohdassa [Testisuunnitelmien ja -sarjojen luominen](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan). Kun olet valinnut testisuunnitelman, testaa Azure DevOps -yhteys valitsemalla **Testaa yhteyttä**.
    - **Isäntänimi** – Syötä kokeiluympäristön isäntänimi, esimerkiksi **\<myaos\>.cloudax.dynamics.com**. Älä käytä **https://**- tai **http://**-etuliitettä.
    - **SOAP-isäntänimi** – Anna testiympäristön SOAP-isäntänimi. SOAP-isäntänimi on yleensä sama kuin isäntänimi, mutta siinä on **soap**-pääte. Esimerkki: **\<myaos\>soap.cloudax.dynamics.com**. Älä käytä **https://**- tai **http://**-etuliitettä.

        > [!NOTE]
        > Voit etsiä isäntänimien ja SOAP-isäntänimen avaamalla IIS-palvelun hallinnan sekä valitsemalla hiiren kakkospainikkeella ensin **Sivustot \> AOSService** ja sitten **Muokkaa sidontoja**. Saat isännän ja SOAP-isännän nimen **Isäntänimi**-sarakkeen arvoista. (SOAP-isännän nimessä on **soap**-pääte URL-osoitteessa.)

        ![Isännän a SOAP-isännän nimi Isäntänimi-sarakkeessa](./media/setup_rsa_tool_63.png)

    - **Järjestelmänvalvojakäyttäjän nimi** – anna testiympäristön järjestelmävalvojakäyttäjän sähköpostiosoite.
    - **Allekirjoitus** – anna todennusvarmenteen allekirjoitus aiemmin tässä oppaassa kuvatulla tavalla.
    - **Työhakemisto** – Määritä testin automaatiotiedostojen, kuten Excelin tietotiedostojen, tallennuskansion sijainti. Kirjoita tai valitse esimerkiksi **C:\\Temp\\RegressionTool**.

        > [!NOTE]
        > Jos kansion nimessä on välilyöntejä, suorittaminen ei onnistu, sillä kansiota ei löydetä. Tämä on tunnettu ongelma ja sen pitäisi olla korjattu työkalun uusimmassa versiossa.

    - **Oletusselain** – Valitse joko **Internet Explorer** tai **Google Chrome**. Varmista, että tarvittavat selainohjaimet on asennettu.
    - **Testiajon aikakatkaisu** – Määritä testiajojen aikakatkaisuaika minuutteina. Kun aikakatkaisuaika päättyy, kaikki aktiiviset ikkunat suljetaan ja odottavat testitapaukset epäonnistuvat.
    - **Testitoiminnon aikakatkaisu** – Tämä kenttä ohjaa Finance and Operation -ympäristön palvelinpyyntöjen aikakatkaisuaikaa minuutteina. Oletusarvo (2 minuuttia) on yleensä riittävä. Hitaissa ympäristöissä tätä arvo on kuitenkin ehkä suurennettava, jos aikakatkaisuihin liittyviä virheitä tapahtuu.
    - **Yrityksen nimi** – Anna sen yrityksen nimi, jota käytetään oletusyrityksenä Excelin parametritiedostoja luotaessa. Voit muuttaa yritystä myöhemmin muokkaamalla Excelin parametritiedostoa.

    ![Asetukset-valintaikkuna](./media/setup_rsa_tool_62.png)

4. Ota asetukset käyttöön ja tallenna ne valitsemalla **Käytä**.

    Voit tallentaa nykyiset asetukset määritystiedostoon omassa tietokoneessa valitsemalla **Tallenna nimellä**. Voit palauttaa asetukset omassa tietokoneessa olevasta määritystiedostosta valitsemalla **Avaa**.

5. Sulje valintaikkuna valitsemalla **Sulje**.

### <a name="load-and-run-test-cases"></a>Testitapausten lataaminen ja suorittaminen

1. Lataa **RSAT-testisuunnitelma** Azure DevOps-projektista valitsemalla **Lataa**.

    ![Lataa-painike](./media/setup_rsa_tool_64.png)

2. Valitse testisarjasta **Luo uusi tuote** -testitapaus ja valitse sitten **Uusi \> Luo testin suoritus- ja parametritiedostot**.

    ![Uusi-valikon Luo testin suoritus -ja parametritiedostot -komento](./media/setup_rsa_tool_65.png)

    Excelin parametritiedostot luodaan RSAT-määrityksissä määritetyssä paikallisessa kansiossa (kuten **C:\\Temp\\RegressionTool**).

    ![Luotu Excelin parametritiedosto](./media/setup_rsa_tool_66.png)

3. Jos haluat tallentaa parametritiedostot, valitse **Lataa palvelimeen**. Valittujen testitapausten testin automaatiotiedostot ladataan Azure DevOpsiin tulevaa käyttöä varten. (Nämä tiedostot sisältävät Excelin testiparametritiedostot.)

    Tällä tavoin ladata testitapauksen parametritiedostot (ja automaatiotiedostot) suoraan Azure DevOpsista valitsemalla **Lataa**. Parametritiedostoja ei siis tarvitse luoda uudelleen. Tämä menettelytapa osoittautuu tärkeäksi myöhemmin, kun haluat säilyttää parametritiedoston muokkaukset etkä halua, että ne korvataan.

4. Voit tarkistaa, että automaatio- ja parametritiedostot on tallennettu Azure DevOpsiin, siirtymällä Azure DevOps -projektiin, valitsemalla **Taulut \> Työnimikkeet** ja valitsemalla lopuksi **Luo uusi tuote** -testitapauksen. **Liitteet**-välilehdessä pitäisi olla neljä tiedostoa:

    - **.cs** – C\#-automaatiotiedosto
    - **.dll** – käännetty automaatiotiedosto koottuna
    - **.xlsx** – Excelin parametritiedosto
    - **.xml** – tallennetiedosto

    ![Liitteet-välilehden tiedostot](./media/setup_rsa_tool_67.png)

5. Valitse ensin suoritettava testitapaus ja sitten **Suorita**.

    > [!NOTE]
    > Jos käytät selaimena Internet Exploreria, varmista ennen testitapausten suorittamista, että työpöydän tarkkuudeksi on valittu **100 %**. Voit tehdä tämän valitsemalla **Windowsin näyttöasetukset\> Skaalaus ja asettelu**. Jos voi muuttaa tätä asetusta virtuaalikoneessa (VM), muuta se siinä asiakasohjelmassa (kannettava), josta yrität käyttää virtuaalikonetta. Virtuaalikoneen näyttöasetukset perivät sitten tarkkuusasetukset.

    ![Työpöydän tarkkuudeksi on määritetty 100 %](./media/setup_rsa_tool_68.png)

6. Jos selainohjaimia ei ole asennettu järjestelmään, näyttöön avautuva varoitussanoma ilmoittaa, että toiminto edellyttää \<browser name\> -ohjainta. haluatko ladata ja asentaa sen nyt automaattisesti. Valitse **Kyllä**.

    ![Internet Explorerin varoitussanoma](./media/setup_rsa_tool_69.png)

    ![Chromen varoitussanoma](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > Jos selaimena Chrome selaimena ja avautuva virhesanoma ilmoittaa, että istuntoa ei luotu virheellinen Chrome-version vuoksi, lataa uusin Chrome-ohjain osoitteesta <http://chromedriver.chromium.org/downloads> kansioon **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**.

    ![Chromen virhesanoma](./media/setup_rsa_tool_71.png)

    Testitapaus suoritetaan ja **Tulos**-kenttä päivitetään.

    ![Päivitetty Tulos-kenttä](./media/setup_rsa_tool_72.png)

    Jos olet toiminut oppaan ohjeiden mukaisesti, **Luo uusi tuote** -testitapaus epäonnistuu, koska tuotteen luonnin tehtävätallenne tallensi tuotenimen pysyväiskoodattuna arvona. Jos suoritat saman testitapauksen uudelleen, näyttöön pitäisi tulla virhesanoma, koska tuote on luotu jo aiemmin.

    ![Tulos-kentän asetukseksi on määritetty Epäonnistui](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a>Testitulosten näyttäminen

1. Kaksoisnapsauta epäonnistunutta testitapausta.

    Näyttöön avautuu virhesanoma.

    ![Virhesanoma](./media/setup_rsa_tool_73.png)

2. Voit näyttää koko virhesanoman valitsemalla **Tiedot**.

    ![Koko virhesanoma](./media/setup_rsa_tool_74.png)

3. Voit näyttää virhesanoman yksityiskohtaisen version Azure DevOpsissa valitsemalla **Avaa Azure DevOpsissa**. Voit näyttää testitapauksen tilan ja yksityiskohtaisen virhesanoman Azure DevOpsissa.

    ![Yksityiskohtainen virhesanoma Azure DevOpsissa](./media/setup_rsa_tool_75.png)

4. Voit näyttää testitulokset suoraan Azure DevOps -projektissa valitsemalla **Testisuunnitelmat \> Testisuunnitelmat \> Ajot**. Kaksoisnapsauta sitä testiajoa, jonka tiedot haluat nähdä.

    ![Testiajoluettelo Azure DevOpsissa](./media/setup_rsa_tool_76.png)

5. **Suorita yhteenveto** -välilehti ilmaisee, että testitapaus epäonnistui. Varsinainen virhesanoma ei kuitenkaan ole saatavana. Voit näyttää virhesanoman tarkat tiedot valitsemalla **Testin tulokset** -välilehden.

    ![Suorita yhteenveto -välilehti](./media/setup_rsa_tool_77.png)

    **Testin tulokset** -välilehdessä on testitapauksen tiedot sekä tulos ja virhesanoma.

    ![Testin tulokset -välilehti](./media/setup_rsa_tool_78.png)

6. Voit näyttää yksityiskohtaisen virhesanoman kaksoisnapsauttamalla kyseistä tietuetta.

    ![Yksityiskohtainen virhesanoma](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > Kaikki virhesanomat ovat saatavana myös paikallisesti kansiossa **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.

7. Voit myös viedä testiajon tulokset testisuunnitelmatasolta valitsemalla **Vie**.

    ![Testisuunnitelman vieminen](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a>Excelin parametritiedoston muokkaaminen

1. Avaa RSAT.
2. Valitse ensin testitapaus ja avaa sitten Excelin parametritiedosto valitsemalla **Muokkaa**.

    Huomaa, että **EcoResProductCreate**-taulukon **Tuotenumero**-kentän arvo on pysyväiskoodattu. Tähän kenttään on päivitettävä uusi tuotenumero ennen testitapauksen suorittamista uudelleen.

3. Käyttämällä seuraavaa Excel-kaavaa voit luoda yksilöivän tuotenumeron jokaiselle ajolle ilman Excelin parametritiedoston avaamista ja tuotenumeron manuaalista päivittämistä joka kerta erikseen.

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > **Yleiset**-välilehden lisäksi Excelin parametritiedostossa on tietovälilehti jokaiselle lomakesivulle, jota testitapaus käyttää.

    ![Tuotenumero-kenttä](./media/setup_rsa_tool_81.png)

4. Valitse **Tallenna** ja sulje sitten Excel-työkirja.
5. Tallenna Excelin parametritiedosto Azure DevOpsiin valitsemalla **Lataa palvelimeen**.

    ![Sanoma onnistuneesta latauksesta](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > Jos haluat suorittaa testitapaukset tietyssä käyttäjäkontekstissa, anna käyttäjän sähköpostitunnus Excelin parametritiedoston **Yleiset**-välilehden **Testikäyttäjä**-kentässä. Excelin parametritiedoston kenttien asettelu on päivitetty uusimmassa RSAT-versiossa, perusidea on edelleen sama.
    >
    > ![Testikäyttäjä-kenttä](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a>Tulosten tarkistaminen

- Suorita testitapaus uudelleen valitsemalla **Suorita** ja tarkista, että testitapaus on suoritettu hyväksytysti. Voit näyttää testitulokset osassa [Testitulosten näyttäminen](#view-the-test-results) kuvatulla tavalla.

    ![Tulos-kentän asetukseksi on määritetty Hyväksytty](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a>Testitapausten ketjuttaminen

Yksi RSAT-työkalun keskeisistä ominaisuuksista on testitapausten ketjuttaminen (jolloin testi voi siirtää arvot toisiin testeihin). Testitapaukset suoritetaan Azure DevOps -testisuunnitelmassa määritetyssä järjestyksessä. (Tämä järjestys voidaan päivittää myös itse testityökalussa.) Niinpä jos haluat välittää muuttujia testitapauksesta toiseen, on erittäin tärkeää, että testit ovat oikeassa järjestyksessä.

Tässä osassa luodaan tallennettu muuttuja ensimmäisessä testitapauksessa, sen jälkeen luodaan toinen testitapaus ja ensimmäisen testitapauksen tallennettu muuttuja välitetään toiseen testitapaukseen. Sen jälkeen testitapaukset suoritetaan ketjutettuna testitapauksena RSAT-työkalussa.

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a>Tallennetun muuttujan luominen muokkaamalla aiemmin luotua tehtävätallennetta

1. Avaa asiakasohjelma.
2. Valitse ensin **Asetukset**-painike (rataskuvake) ja sitten **Tehtävän tallennustoiminto**.
3. Valitse **Muokkaa tallennetta**.

    ![Muokkaa tallennetta -painike](./media/setup_rsa_tool_85.png)

4. Valitse **Avaa Lifecycle Services -palveluista**.

    ![Avaa Lifecycle Services -palveluista -painike](./media/setup_rsa_tool_86.png)

5. Valitse **Valitse Lifecycle Services -kirjasto**.

    ![Valitse Lifecycle Services -kirjasto -painike](./media/setup_rsa_tool_87.png)

    BPM-kirjastot ladataan LCS:tä.

    ![BPM-kirjastojen lataaminen](./media/setup_rsa_tool_88.png)

6. Kun BPM-kirjastot on ladattu LCS:stä, valitse **RSAT**-BPM-kirjasto ja **Luo uusi tuote** -liiketoimintaprosessi, johon tehtävätallenne on liitetty. Valitse sitten **OK**.

    ![BPM-kirjaston ja liiketoimintaprosessin valitseminen](./media/setup_rsa_tool_89.png)

7. Sopivan tehtävätallenteen nimi annetaan **Tallenteen nimi** -kentässä. Valitse **Aloita**.

    ![Tehtävätallenteen nimi Tallenteen nimi -kentässä](./media/setup_rsa_tool_90.png)

8. Avaa sivu, jossa alkuperäinen tehtävätallenne, **Luo tuote**, tallennettiin valitsemalla ensin **Tuotetietojen hallinta \> Tuotteet** ja sitten **Uusi**.
9. Valitse **Lisää vaihe**.

    > [!NOTE]
    > Uusi vaihe lisätään ruudussa valitun vaiheen **jälkeen**.

    ![Lisää vaihe -painike](./media/setup_rsa_tool_91.png)

10. Napsauta hiiren kakkospainikkeella **Tuotenumero**-kenttää ja valitse sitten **Tehtävän tallennustoiminto \> Kopioi**.

    ![Kopioi-komento](./media/setup_rsa_tool_92.png)

11. Uusi vaihe on lisätty ruutuun. Kirjaa **Tuotenumero**-kentän arvo muistiin, sillä tarvitset sitä myöhemmin.

    ![Uusi vaihe lisätty](./media/setup_rsa_tool_93.png)

12. Valitse **Muokkaus valmis**.
13. Valitse **Tallenna Lifecycle Servicesiin** ja liitä uusi tehtävätallenne samaan BPM-kirjastoon ja liiketoimintaprosessiin, johon alkuperäinen tehtävätallenne on liitetty. Lisätietoja on osassa [Tehtävätallenteen luominen ja tallentaminen BPM-kirjastoon](#create-a-task-recording-and-save-it-to-the-bpm-library).
14. Siirtymällä BPM-kirjastoon ja valitsemalla **Synkronoi testitapaukset** voit korvata testitapaukseen Azure DevOpsissa liitetyn tehtävätallenteen osassa [Liiketoimintaprosessien mallintajasta Azure DevOpsiin tapahtuvan synkronoinnin testaaminen](#test-the-synchronization-from-bpm-to-azure-devops) kuvatulla tavalla.
15. Avaa RSAT ja lataa kaikki testisarjan testitapaukset uudelleen valitsemalla **Lataa**. Sopivan testitapauksen automaatio- ja parametritiedostot on luotava uudelleen valitsemalla ensin testitapaus ja sitten **Uusi \> Luo testin suoritus -ja parametritiedostot** osassa [Testitapausten lataaminen ja suorittaminen](#load-and-run-test-cases) kuvatulla tavalla.

    > [!NOTE]
    > Jos Excelin parametritiedosto on jätetty auki, uudelleenluonti epäonnistuu. Varmista tämän vuoksi, että testitapauksen Excelin parametritiedosto on suljettu, ennen kuin luot uuden Excelin parametritiedoston.

16. Avaa uusi Excelin parametritiedosto valitsemalla **Muokkaa**. Uusi **Tallennettu muuttuja** -merkintä näkyy rivillä 9. Tämä muuttuja, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, tallennetaan tehtävätallenteen XML-tiedostoon, ja sitä voidaan käyttää seuraavissa testeissä.

    ![Tallennettu muuttuja -merkintä](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a>Uuden testitapauksen luominen

1. Siirry **RSAT**-BPM-kirjastoon.
2. Valitse **Tuen liiketoimintaprosessin malli** -prosessi ja valitse sitten oikealla **Muokkaustila**.
3. Vaihda sekä **Nimi**- että **Kuvaus**-kentän nimeksi **Vapauta tuote**. Valitse sitten **Tallenna**.

    ![Nimeksi ja kuvaukseksi on muutettu Vapauta tuote](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a>Uuden tarkistustoiminnon sisältävän tehtävätallenteen luominen

- Luo tehtävätallenne, jolla vapautetaan aiemmin luotu tuote USRT-yritykseen. Lisätietoja on osassa [Tehtävätallenteen luominen ja tallentaminen BPM-kirjastoon](#create-a-task-recording-and-save-it-to-the-bpm-library).

    > [!NOTE]
    > Ketjutettujen testitapausten osalta suositellaan aina, että tarvittava tallenne etsitään tai suodatetaan *kirjoittamalla kentän arvo manuaalisesti kenttään*. Työkalu määrittää tällä tavoin tallenteen, jossa toiminto tehdään seuraavassa testitapauksessa.

    ![Tarkistustoiminnon sisältävä uusi tehtävätallenne](./media/setup_rsa_tool_96.png)

    Edellinen kuva osoitti, miten sen jälkeen, kun tuote on löydetty pikasuodattimella mutta ennen **Vapauta tuotteet** -vaihtoehdon valitsemista, **Tuotenumero**-kentän arvo tarkistetaan. Tällä tavoin voidaan varmistaa, että tuotenumero on aiemmin luotu tuotenumero. Voit tarkistaa arvon napsauttamalla hiiren kakkospainikkeella **Tuotenumero**-kenttää ja valitsemalla sitten **Tehtävän tallennustoiminto \> Tarkista \> Nykyinen arvo**.

    ![Nykyisen arvon tarkistaminen](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a>Tehtävätallenteen tallentaminen liiketoimintaprosessien mallintajaan

1. Kun tehtävätallenne on valmis, valitse **Tallenna Lifecycle Servicesiin**.

    ![Valmiin tehtävien tallennustoiminnon tallentaminen Lifecycle Servicesiin](./media/setup_rsa_tool_98.png)

2. Kirjaston tiedot ladataan LCS:stä.

    ![Kirjaston tietojen lataaminen LCS:stä](./media/setup_rsa_tool_99.png)

3. Valitse tehtävätallenteeseen liitettävä BPM-kirjasto. Tässä oppaassa valitaan aiemmin luotu **RSAT**-BPM-kirjasto ja siinä oleva **Vapauta tuote** -liiketoimintaprosessi. Valitse sitten **OK**.

#### <a name="sync-bpm-to-azure-devops"></a>Liiketoimintaprosessien synkronointi Azure DevOpsiin

1. Siirry BPM-kirjastoon ja avaa **RSAT**-kirjasto.
2. Valitse ensin **VSTS-synkronointi** ja sitten **Synkronoi testitapaukset**. Lisätietoja on osassa [Liiketoimintaprosessien mallintajasta Azure DevOpsiin tapahtuvan synkronoinnin testaaminen](#test-the-synchronization-from-bpm-to-azure-devops).

    Kun synkronointi on valmis, uusi työnimike ja vastaava **Vapauta tuote** -liiketoimintaprosessin testitapaus näkyvät Azure DevOpsissa kohdassa **Taulut \> Työnimikkeet**.

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a>Uuden testitapauksen lisääminen aiemmin luotuun testisarjaan

1. Valitse ensin **Testisuunnitelmat \> Testisuunnitelmat** ja sitten **RSAT-testisuunnitelma**.
2. Valitse **Lisää aiemmin luotu**.
3. Valitse **Lisää testitapaukset sarjaan** -sivulla **Suorita kysely**.
4. Valitse uusi **Vapauta tuote** -prosessia varten luotu testitapaus. Valitse sitten sivun oikeassa alakulmassa **Lisää testitapaukset** (tämä painike ei näy seuraavassa kuvassa).

    ![Lisää testitapaukset sarjaan -sivu](./media/setup_rsa_tool_100.png)

    Testisarjassa on nyt kaksi testitapausta.

    ![Testisarjan kaksi testitapausta](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a>Testitapausten lataaminen RSAT-työkaluun

1. Avaa RSAT ja valitse **Lataa**.
2. Testitapaukset ladataan, ja saat varoituksen, jonka mukaan toiminto korvaa Excelin testidatatiedostot ja paikalliset muutokset menetetään ja sinulta kysytään, haluatko jatkaa. **Kyllä**-vaihtoehdon valinta päivittää paikallisessa järjestelmässä olevat Excelin parametritiedostot mutta ei Azure DevOpsiin ladattujen Excelin parametritiedostoja.

    ![Tämä toiminto korvaa Excelin testitietotiedostot](./media/setup_rsa_tool_102.png)

    Molemmat testitapaukset on ladattu yhdessä ensimmäisen testitapauksen Excelin parametritiedoston kanssa. Koska valitse viimeisessä ajossa **Lataa palvelimeen**, parametritiedosto haetaan Azure DevOpsiin.

    ![Ladatut testitapaukset](./media/setup_rsa_tool_103.png)

3. Valitse vain toinen testitapaus ja valitse sitten **Uusi \> Luo testin suoritus -ja parametritiedostot**.

#### <a name="edit-the-excel-parameter-file"></a>Excelin parametritiedoston muokkaaminen

1. Valitse vain toinen testitapaus ja avaa sitten vastaava Excelin parametritiedosto valitsemalla **Muokkaa**.
2. Kopioi tallennettu muuttuja **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** ensimmäisestä testitapauksesta kaikkiin kenttiin, joissa tuotenumeroa käytetään. (Lisätietoja on osassa [Tallennetun muuttujan luominen muokkaamalla aiemmin luotua tehtävätallennetta](#modify-an-existing-task-recording-to-create-a-saved-variable).) Tässä tapauksessa muuttuja kopioidaan **Tuotenumero**- ja **Tarkista tuotenumero** -kenttiin **EcoResProductListPage**-taulukossa.

    ![Tuotenumero- ja Tarkista tuotenumero -kentät](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > Muuttujia voidaan siirtää testien välillä vain saman testiajon aikana. Muuttujien nimien on oltava täsmälleen samat.

3. Valitse **Tallenna** ja sulje sitten Excel-työkirja.
4. Tallenna Excelin parametritiedostoon tehdyt muutokset valitsemalla **Lataa palvelimeen**.

#### <a name="run-the-chained-test-cases"></a>Ketjutettujen testitapausten suorittaminen

1. Valitse ensin molemmat testitapaukset ja sitten **Suorita**.
2. Tarkista, että molemmat testitapaukset on hyväksytty.

    ![Kummankin testitapauksen hyväksytyksi määritetty Tulos-kenttä](./media/setup_rsa_tool_105.png)
