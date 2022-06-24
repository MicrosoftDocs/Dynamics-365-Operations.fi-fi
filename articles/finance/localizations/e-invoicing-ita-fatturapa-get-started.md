---
title: Italian FatturaPA:n ja SDI:n suoran integroinnin määritys
description: Tässä artikkelissa on tietoja, joiden avulla voit aloittaa Italian sähköisen laskutuksen ja määrittää Italian FatturaPA:n suoran integroinnin Exchange-järjestelmään (SDI).
author: abaryshnikov
ms.date: 01/15/2022
ms.topic: article
audience: Application User, Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: abaryshnikov
ms.search.validFrom: 2021-10-18
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 510cf05e7bbc925478f9a1a4ea2ea27fe397c570
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853189"
---
# <a name="set-up-direct-integration-of-italian-fatturapa-with-sdi"></a>Italian FatturaPA:n ja SDI:n suoran integroinnin määritys

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Italian sähköinen laskutus ei tällä hetkellä välttämättä tue kaikkia funktioita, jotka ovat käytettävissä Microsoft Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin laskuissa.

Tässä artikkelissa on tietoja, joiden avulla voit aloittaa Italian sähköisen laskutuksen käytön Financessa ja Supply Chain Managementissa. Se opastaa Regulatory Configuration Servicesin (RCS) maa-/aluekohtaisissa määritysvaiheissa. Nämä vaiheet täydentävät [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md) -kohdassa kuvattuja vaiheita.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit suorittaa tämän artikkelin vaiheet loppuun, seuraavien edellytysten on täytyttävä:

- Suorita vaiheet kohdassa [Sähköisen laskutuksen aloittaminen](e-invoicing-get-started.md).
- Tuo sähköinen **Italian FatturaPA (IT)** -laskutusominaisuus RCS:ään yleisestä tietovarastosta. Lisätietoja on aiemmin mainitun Sähköisen laskutuksen käytön aloittaminen -artikkelin [Tuo sähköisen laskutuksen ominaisuus Microsoftin konfiguraatiopalvelusta](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider)-osassa.
- Lisää linkit vaadituista varmenteista palveluympäristöön. Pakollisia todistuksia ovat digitaalisten allekirjoitusten sertifikaatti, sertifikaattiviranomaisen (CA) sertifikaatti ja asiakassertifikaatti. Lisätietoja on [Luo digitaalisen sertifikaatin salasana](e-invoicing-get-started-service-administration.md#create-a-digital-certificate-secret) -osassa Sähköisen laskutuksen käytön aloittaminen -artikkelissa.

## <a name="country-specific-configuration-for-the-italian-fatturapa-it-electronic-invoicing-feature"></a>Maa-/aluekohtainen konfigurointi Italian FatturaPA (IT) – sähköinen laskutus -ominaisuudelle

Suorita seuraavat vaiheet, ennen kuin otat sovelluksen määritykset käyttöön yhdistetyssä Finance- tai Supply Chain Management -sovelluksessa.

Tämä osa täydentää [Sovellusasetusten maa-/aluekohtainen konfigurointi](e-invoicing-get-started.md#country-specific-configuration-of-application-setup) -osaa Sähköisen laskutuksen käytön aloittaminen -artikkelissa.

### <a name="create-a-new-feature"></a>Luo uusi ominaisuus

1. Kirjaudu sisään RCS:ään.
2. Merkitse **Sähköinen raportointi** -työtilan **Konfigurointipalveluntarjoajat**-osassa yrityksesi konfiguraation tarjoaja aktiiviseksi.
3. Valitse **Globalisaatio-ominaisuus** -työtilan **Toiminnot**-osassa **Sähköinen laskutus** -ruutu.
4. Valitse **Sähköisen laskutuksen ominaisuudet** -sivulla **Lisää** \> **Aiemmin luodun ominaisuuden perusteella**.
5. Valitse **Microsoftin konfigurointipalvelussa** **Italian FatturaPA (IT)** perusominaisuutena, anna nimi ja valitse sitten **Luo ominaisuus**.

### <a name="set-up-application-specific-parameters"></a>Sovelluskohtaisten parametrien määrittäminen

1. Valitse **Sähköisen laskutuksen ominaisuudet** -sivulla muokattava ominaisuus.
2. Tarkista **Versiot**-välilehdessä, että **Luonnos**-versio on valittuna.
3. Valitse **Määritykset**-välilehdessä määritys ja sitten **Sovelluskohtaiset parametrit**.
4. Varmista **Haku**-osassa, että **Luonnollisen käänteisen kulun alaluokkien luettelo** on valittuna.
5. Valitse **Ehdot**-osasta **Lisää**.
6. Lisää kuhunkin järjestelmässä määritettyyn aliluokkaan erityisehdot ja tallenna muutokset.

    > [!NOTE]
    > **Nimi**-sarakkeessa voit valita **\*Tyhjä\***- tai **\*Ei tyhjä\*** -paikkamerkin arvon tietyn arvon asemesta.

### <a name="configure-a-processing-pipeline-for-export"></a>Käsittelyputken konfiguroiminen vientiä varten

1. Valitse **Sähköisen laskutuksen ominaisuudet** -sivulla muokattava ominaisuus.
2. Valitse **Asetukset**-välilehdessä ensin **Myyntilaskut** ja sitten **Muokkaa**.
3. Käy **Käsittelyputki** -osassa toimenpiteet läpi ja määritä kaikki pakolliset kentät:

    - Määritä **Allekirjoita tiedosto** -toiminnossa **Sertifikaatin nimi** -kenttään digitaalinen allekirjoitussertifikaatti.
    - Määritä **Lähetä**- toimille **URL-osoite**- ja **Sertifikaatti**-kentät. **Sertifikaatit**-kentän arvo on sertifikaattien ketju, joista ensimmäinen on juuri-CA-sertifikaatti (caentrate.cer) ja toinen asiakassertifikaatti.

4. Varmista valitsemalla **Vahvista**, että kaikki pakolliset kentät on määritetty.
5. Tallenna muutokset ja sulje sivu.
6. Valitse **Asetukset**-välilehdessä ensin **Projektilaskut** ja sitten **Muokkaa**.
7. Tee vaiheet 3-5 uudelleen projektilaskuille.

### <a name="configure-the-processing-pipeline-for-import"></a>Käsittelyputken konfiguroiminen tuontia varten

1. Valitse **Sähköisen laskutuksen ominaisuudet** -sivulla muokattava ominaisuus.
2. Valitse **Asetukset**-välilehdessä ensin **Tuo laskut** ja sitten **Muokkaa**.
3. Anna merkkijonoarvo **Tietokanava**-osan **Parametrit**-välilehden **Tietokanava**-kentässä.
4. Määritä asetusten kentät **Soveltuvuussäännöt**-välilehdessä. Voit käyttää **Kanava**-oletuslauseketta ohittamalla edellisessä vaiheessa **Tietokanava**-kentälle asettamasi arvon **Arvo**-kenttään.

    ![Soveltuvuussääntöjen määrittäminen.](media/e-invoicing-ita-fatturapa-get-started-apprules-setup.png)

5. Varmista valitsemalla **Vahvista**, että kaikki pakolliset kentät on määritetty.

### <a name="deploy-the-feature"></a>Toiminnon käyttöönotto

1. Ominaisuuden viimeisteleminen, julkaiseminen ja ottaminen käyttöön palveluympäristössä. Lisätietoja on aiemmin mainitun Sähköisen laskutuksen käytön aloittaminen -artikkelin [Sähköisen laskutuksen ominaisuuden käyttöönotto palveluympäristössä](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) -osassa.
2. Ota ominaisuus käyttöön yhdistetyssä sovelluksessa. Lisätietoja on aiemmin mainitun Sähköisen laskutuksen käytön aloittaminen -artikkelin [Sähköisen laskutuksen ominaisuuden käyttöönotto yhdistetyssä sovelluksessa](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application) -osassa.

### <a name="set-up-finance"></a>Financen määrittäminen

1. Kirjaudu Finance-ympäristöön.
2. Valitse **Sähköisen raportointi** -työtilan **Määrityslähteet** -osassa **Microsoft**.
3. Select **Säilöt** \> **Yleinen** \> **Avaa**.
4. Valitse ja tuo **Myyntilaskun kontekstimalli**- sekä **Toimittajan laskun tuonti (IT)** -konfiguraatiot.
5. Siirry kohtaan **Organisaation hallinta** \> **Määritys** \> **Sähköisten asiakirjojen parametrit**.
6. Etsi ja valitse **Ominaisuudet**-välilehdessä **Italian sähköinen laskutus** -toiminto ja valitse sitten **Ota käyttöön** -valintaruutu.
7. Varmista **Sähköinen tiedosto** -välilehdessä, että **myyntilaskukirjauskansion** ja **projektilaskun** kentät on määritetty [sovelluksen asetusten konfiguroinnissa](e-invoicing-get-started.md#configure-the-application-setup) määritettyjen tietojen mukaan.

### <a name="set-up-vendor-invoice-import"></a>Toimittajan laskujen tuonnin määrittäminen 

1. Merkitse Financessa **Sähköinen raportointi** -työtilan **Konfigurointipalveluntarjoajat**-osassa yrityksesi konfiguraation tarjoaja aktiiviseksi.
2. Valitse **Raportointikonfiguraatiot**.
3. Valitse **Myyntilaskun kontekstimalli** ja valitse **Luo määritys**.
4. Luo johdettu määritys valitsemalla **Johda nimestä: Myyntilaskun konteksti, Microsoft**.
5. Valitse **Luonnos**-versiossa **Suunnitteluohjelma**.
6. Valitse **Tietomalli**-puussa **Yhdistä malli tietolähteeseen**.
7. Valitse **Määritelmät**-puussa **DataChannel** ja valitse sitten **Suunnitteluohjelma**.
8. Laajenna **Tietolähteet**-puussa säilö **\$Context\_Channel**.
9. Valitse **Arvo**-kentässä **Muokkaa**. 
10. Kirjoita tietokanavan nimi. Nimen enimmäispituus on 10 merkkiä. Sen on oltava sama kuin RCS:n sähköisen laskutustoiminnon **Tietokanava**-parametrin arvo.
11. Tallenna muutokset ja siirry kohtaan **Raportointikonfiguraatiot** \> **Suorita konfiguraatioversio**.
12. Valitse **Ulkoiset kanavat** -välilehden **Kanavat**-osassa **Lisää**.
13. Kirjoita **Kanava**-kenttään **\$Context Channel** -arvo.
14. Kirjoita arvot **Kuvaus**- ja **Yritys**-kenttiin.
15. Valitse **Asiakirjan konteksti**-kentässä uusi johdettu määritys kohdasta **Asiakaslaskun kontekstimalli**. Yhdistämismäärityksen kuvauksen pitäisi olla **Tietokanavakonteksti**.
16. Valitse **Tuonnin lähteet** -välilehdestä **Lisää** ja määritä sitten seuraavat arvot:

    - **Nimi:** OutputFile
    - **Tietoyksikön nimi:** Toimittajalaskun otsikko  (**Tietoyksikkö:** VendorInvoiceHeaderEntity)
    - **Mallimääritys:** Toimittajalaskun tuonti (IT)

> [!NOTE]
> Jos tuot toimittajan laskuja eri lähteistä, voit luoda useita ulkoisia kanavia ja useita johdettuja konfiguraatioita, joissa on eri **\$Context Channel**-arvot. Voit esimerkiksi tuoda eri yksiköiden toimittajalaskuja.

## <a name="proxy-server-setup"></a>Välityspalvelimen asetukset

Tässä osassa on tietoja, joiden avulla voit määrittää ja konfiguroida välityspalvelinpalvelun Exchange-järjestelmän (SDI) ja sähköisen laskutuspalvelun välistä tiedonsiirtoa varten.

### <a name="create-an-app-registration"></a>Luo sovellusrekisteröinti

1. Seuraavan Windows PowerShell -komentosarjan avulla voit luoda itse allekirjoitetun sertifikaatin palveluiden väliseen (S2S) todennukseen.

    ```powershell
    $certOutputLocation = "C:\certs\proxytest"
    $certName = "sdiProxyClientS2SCert"
    $certPassword = "123"

    $certCerFile = Join-Path $certOutputLocation "$certName.cer"
    $certPfxFile = Join-Path $certOutputLocation "$certName.pfx"

    $securePassword = ConvertTo-SecureString $certPassword -AsPlainText -Force

    $cert = New-SelfSignedCertificate -KeyLength 2048 -KeyExportPolicy Exportable -FriendlyName "CN=$certName" -CertStoreLocation Cert:\CurrentUser\My -Subject $certName -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider"

    Export-Certificate -Cert $cert -FilePath $certCerFile -type CERT | Out-Null
    Export-PfxCertificate -Cert $cert -FilePath $certPfxFile -Password $securePassword | Out-Null
    ```

2. Tallenna .pfx-sertifikaattitiedosto avainsäilöön ja sen jälkeen poista paikallinen kopio.
3. Kirjaudu sisään [Azure-portaaliin](https://portal.azure.com) järjestelmänvalvojana.
4. Luo sovelluksen rekisteröinti SDI Proxy -palvelua varten.

    1. Siirry kohtaan **Sovellusrekisteröinnit**, luo rekisteröinti ja määritä sille sitten seuraavat arvot:

        - **Nimi:** SDI Proxy Client
        - **Tuetut tilityypit:** Vain tämän organisaatiohakemiston tilit (Yksittäinen vuokraaja)

    2. Valitse **Rekisteröi** ja valitse sitten juuri luomasi sovelluksen rekisteröinti.
    3. Siirry kohtaan **Ohjelmointirajapinnan käyttöoikeudet** ja valitse **Myönnä järjestelmänvalvojan hyväksyntä**.
    4. Siirry kohtaan **Sertifikaatit ja salasanat** **Lataa sertifikaatti** ja lataa .cer-sertifikaattitiedosto S2S-todennusta varten.
    5. Siirry kohtaan **Yrityssovellukset** ja valitse luomasi sovellus.
    6. Tallenna sovelluksen **Sovellustunnus** (asiakastunnus) ja **objektitunnus**.
    7. Laskutuspalveluryhmän on myönnettävä sovellukselle käyttöoikeus palveluun. Lähetä seuraavien parametrien arvot osoitteeseen <D365EInvoiceSupport@microsoft.com>:

        - AAD-vuokraajan tunnus
        - LCS-ympäristön tunnus
        - Sovelluksen tunnus
        - Objektin tunnus

5. Lisää RCS:ssä sovellus palveluympäristön sovellusluetteloon.

    1. Siirry kohtaan **Globalisaatio-ominaisuudet** \> **Ympäristöt** \> **Sähköinen laskutus** \> **Palveluympäristöt** ja valitse ympäristö.
    2. Lisää ruudukkoon rivi **Sovellukset**-osassa ja lisää sovelluksen nimi ja objektitunnus.

        ![Sovelluksen lisääminen palveluympäristöön.](media/e-invoicing-ita-fatturapa-get-started-add-app-to-env.png)

    3. Valitse ensin **Tallenna** ja sitten **Julkaise**.

### <a name="create-an-azure-virtual-machine"></a>Luo Azure-näennäiskone

1. Siirry [Azure-portaalissa](https://portal.azure.com) kohtaan **Näennäiskoneet** ja valitse **Luo uusi**.
2. Valitse tilaus ja resurssiryhmä **Perustiedot**-välilehdessä. Arvojen tulisi olla tilaus ja resurssiryhmä, jossa avainsäilö ja Blob-säilö sijaitsevat.
3. Valitse alue. Arvon tulisi olla alue, jossa Finance-ympäristö on otettu käyttöön.
4. Lisää järjestelmänvalvojan käyttäjänimi ja salasana ja tallenna ne avainsäilölle.
5. Valitse kohdassa **Valitse saapuvat portit** **HTTPS (443)** ja **RPD (3389)**.

    > [!NOTE]
    > Suosittelemme, että **RDP (3389)** -portti poistetaan käytöstä, kun järjestelmä siirtyy tuotantoon. Voit ottaa sen uudelleen käyttöön, jos sinun on yhdistettävä virtuaalikoneeseen (VM) vianmääritystarkoituksessa.

    ![Kenttiä määritetään Perustiedot-välilehdessä, jos haluat luoda Azure-virtuaalikoneen.](media/e-invoicing-ita-fatturapa-get-started-create-vm-1.png)

6. Valitse **Levyt**-välilehden **Lisäasetukset**-pikavälilehden **Käytä hallittuja levyjä** -valintaruutu. Jätä **Väliaikainen käyttöjärjestelmälevy** -valintaruutu tyhjäksi.

    ![Kenttiä määritetään Levyt-välilehdessä, jos haluat luoda Azure-virtuaalikoneen.](media/e-invoicing-ita-fatturapa-get-started-create-vm-2.png)

7. Valitse **Verkkopalvelut**-välilehden **Julkinen IP-osoite** -kentässä **Luo uusi**.

    ![Kenttiä määritetään Verkkopalvelut-välilehdessä, jos haluat luoda Azure-virtuaalikoneen.](media/e-invoicing-ita-fatturapa-get-started-create-vm-3.png)

8. Valitse **Luo julkinen IP-osoite** -valintaikkunasta **SKU**-kenttäryhmästä **Vakio**-vaihtoehto. Valitse **Määritys** -kenttäryhmässä **Staattinen**-vaihtoehto.

    ![Julkisen IP-osoitteen luominen.](media/e-invoicing-ita-fatturapa-get-started-create-vm-4.png)

9. Poista **Hallinta**-välilehdessä **Automaattinen sammutus**  -valintaruudun valinta, jos haluat poistaa automaattisen sammutuksen käytöstä.
10. Määritä **Vieraan käyttöjärjestelmän päivitykset** -kentän arvoksi **Manuaalinen** ja määritä sitten muut käytännöt.
11. Tarkista ja luo näennäiskone.
12. Siirry uudessa näennäiskoneessa kohtaan **Tunnistetiedot** \> **Järjestelmän määrittämät** ja määritä **Tila**-asetukseksi **Käytössä**.
13. Myönnä näennäiskoneelle käyttöoikeus avainsäilöön.

    1. Siirry avainsäilössä kohtaan **Käyttöoikeuksien hallinta (IAM)** \> **Roolimääritykset**.
    2. Valitse **Lisää roolimääritys** ja valitse sitten seuraavat kentät:

        1. Määritä **Rooli**-kentässä **Key Vault -salasanan käyttäjä**.
        2. Määritä **Liitä käyttöoikeus** -kenttään **Virtuaalikone**.
        3. Määritä **Tilaus**-kentässä tilauksesi.
        4. Määritä **Valitse**-kentässä näennäiskoneesi.

    3. Siirry kohtaan **Käyttöoikeuskäytännöt**.
    4. Valitse **Lisää käyttöoikeuskäytäntö** ja valitse sitten seuraavat kentät:

        1. Valitse **Valittu päänimi** -kentässä näennäiskoneesi.
        2. Valitse **Sertifikaatti** -osassa **Luettelo** ja **Nouda** oikeudet.

14. Siirry [Azure-portaalissa](https://portal.azure.com) kohtaan **Julkiset IP-osoitteet** ja valitse näennäiskoneessa luotu IP-osoite.
15. Siirry kohtaan **Määritys** DNS (Domain Name System) -nimi.

### <a name="prepare-the-proxy-service-environment"></a>Välityspalvelinympäristön valmisteleminen

Noudata seuraavia vaiheita koneessa, jossa välityspalvelinta ylläpidetään.

1. Muodosta yhteys näennäiskoneeseen etätyöpöytäyhteydellä.
2. Avaa paikallisen koneen sertifikaatti -kohta. Lisätietoja on kohdassa [Ohje: Sertifikaattien tarkasteleminen (MMC)](/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in).
3. Tuo **caentrate.cer**-todistus tuotantoa varten ja **CAEntratetest.cer** testausta varten [Trusted Root Certification Authorities -myymälään](/dotnet/framework/wcf/feature-details/working-with-certificates#certificate-stores). (**CAEntratetest.cer** on viranomaisen toimittama juuri-CA-sertifikaatti.)
4. Avaa Ohjauspaneelissa **Ota Windows-toiminnot käyttöön tai poista ne käytöstä** tai siirry kohtaan **Palvelimen hallinta** \> **Roolien ja ominaisuuksien lisääminen** palvelimen käyttöjärjestelmässä ja ota Internet Information Services (IIS) -toiminnot käyttöön:

    - Web Management Tools
        - IIS Management Console
    - World Wide Web Services
        - Application Development Features
            - .NET Extensibility 4.7 (or 4.8)
            - ASP
            - ASP.NET 4.7 (tai 4.8)
            - CGI
            - ISAPI-laajennukset
            - ISAPI-suodattimet
        - Yleiset HTTP-toiminnot
            - Oletustiedosto
            - Hakemiston selaaminen
            - HTTP-virheet
            - Staattinen sisältö
        - Kunto ja diagnostiikka
            - HTTP-lokiinkirjoitus
            - Seuranta
        - Suorituskykyominaisuudet
            - Staattisen sisällön tiivistys
        - Suojaus
            - Pyynnön suodatus

    ![IIS-toimintojen ottaminen käyttöön.](media/e-invoicing-ita-fatturapa-get-started-turnon-features.png)

### <a name="set-up-the-sdi-proxy-service-in-iis"></a>SDI Proxy -palvelun määrittäminen IIS:ssä

1. Avaa Microsoft Dynamics Lifecycle Servicesissa (LCS) jaettu omaisuuskirjasto, valitse omaisuustyypiksi **Tietopaketti**.
2. Etsi **Sähköisen laskutuksen palvelun SDI Proxy** ja lataa se näennäiskoneeseen.
3. Konfiguroi palvelu.

    1. Pura lataamasi **Electronic Invoicing Service Sdi Proxy** -arkistokansio.
    2. Avaa **src\\FattureService** -kansiossa **appsettings.json**-tiedosto ja määritä seuraavat parametrit:

        - **KeyVaultUri** – Määritä sen avainsäilön osoite, johon laskutuspalvelun asiakassertifikaatti tallennetaan.
        - **TenantId** – Määritä asiakkaan vuokraajan yleinen yksilöivä tunnus (GUID).
        - **EnvironmentId** – Määritä LCS-ympäristön tunnus.
        - **ClientId** – Määritä palvelun sovellusrekisteröinnin sovellustunnus asiakkaan vuokraajassa.
        - **ClientCertificateName** – Määritä S2S-sertifikaatin nimi avainsäilössä.
        - **SecurityServiceClientOptions.Endpoint** – Määritä suojauspalvelun URL-osoite.
        - **SecurityServiceClientOptions.Resource** – Määritä alue, jolle tunnus hankitaan.
        - **InvoicingServiceClientOptions.Endpoint** – Määritä laskutuspalvelun päätepiste. Tämän arvon tulisi olla sama päätepiste, jota käytetään RCS:lle ja Financelle.
        - **InvoicingServiceClientOptions.ServiceEnvironmentId** – Määritä palveluympäristön nimi. Arvon tulee olla Finance-ympäristösi nimi.
        - **NotificationsFolder** – Määritä kansio, johon saapuvat ilmoitustiedostot tallennetaan.

    3. Etsi **web.config**-tiedostosta seuraava rivi ja lisää välityspalvelinsertifikaatin allekirjoitus.

        `<serviceCertificate findValue="[certificate thumbprint]" storeLocation="LocalMachine" storeName="My" x509FindType="FindByThumbprint">`

        > [!TIP]
        > Kun järjestelmä siirtyy tuotantoon, voit muuttaa joitakin web.config-tiedoston arvoja. Näin voidaan vähentää kerätyn lokin tietojen määrää ja säästää tilaa. Muuta **\<system.diagnostics\>\<source\>**-solmussa **switchValue**-arvoksi **Critical,Error**. Lisätietoja on kohdassa [MS Service Trace Viewer](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).

4. Avaa IIS Manager. Pysy juurisolmussa vasemman puolen puussa. Valitse oikealla **Palvelinsertifikaatit**.

    ![Palvelusertifikaattien valitseminen IIS Managerissa.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-1.png)

5. Avaa valikko ja valitse **Tuo**.
6. Määritä **Tuo sertifikaatti** -valintaikkunan **Sertifikaattitiedosto (.pfx)** -kenttään välityspalvelinsertifikaatin .pfx-tiedoston polku.

    ![Välityspalvelinpalvelun sertifikaattitiedoston määrittäminen.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-2.png)

7. Pidä valittuna (tai napsauta sitä hiiren kakkospainikkeella) **Sivustot** ja valitse **Lisää verkkosivusto**.
8. Anna sivuston nimi **Lisää verkkosivusto** -valintaikkunan **Sivuston nimi** -kenttään.
9. Osoita **Fyysinen polku** -kentässä **src\\FattureService**-kansioon.
10. Valitse **Sidontatyyppi**-kentässä **https**.
11. Määritä isännän nimi **Isäntänimi**-kentässä.
12. Jätä **IP-osoite**- ja **Portti**-kentät oletusarvoiksi.
13. Varmista, että **Vaadi palvelimen nimen ilmaisin** -valintaruutu on tyhjä, koska SDI ei tue tätä tekniikka.
14. Valitse **SSL-sertifikaatti**-kentästä tuomasi välityspalvelinsertifikaatti.
15. Määritä **Sovelluspooli**-kentässä sivuston pooli ja merkitse sen nimi (esimerkiksi **SdiAppPool**).

    ![Verkkosivuston lisääminen.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-1.png)

16. Kun olet luonut sivuston loppuun, avaa **SSL-asetusten** valikko.

    ![SSL-asetusten valikon avaaminen.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-2.png)

17. Valitse **Edellytä SSL-suojaus** -valintaruutu ja valitse sitten **Asiakkaan sertifikaatit** -kenttäryhmästä **Edellytä**-vaihtoehto.

    ![Määritä SSL-asetukset.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-3.png)

18. Avaa **Hakemiston selaus** ja valitse **Ota käyttöön**.
19. Siirry missä tahansa Internet-selaimessa kohtaan **serverDNS/TrasmissioneFatture.svc**. Palvelun vakiosivun on oltava näkyvissä.

    ![Palvelun tarkistaminen selaimella.](media/e-invoicing-ita-fatturapa-get-started-proxy-open-browser.png)

20. Luo seuraavat kansiot lokien ja tiedostojen tallentamista varten:

    - **C:\\Logs\\** – Tallenna lokitiedostot tänne. [MS Service Trace Viewer](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe) voi tarkastella näitä tiedostoja.
    - **C:\\Files\\** – Tallenna kaikki vastaustiedostot tänne.

21. Myönnä tiedostovalitsimessa **NETWORK SERVICE**- ja **IIS AppPool\\SdiAppPool**- (tai **IIS AppPool\\DefaultAppPool** jos käytätä oletuspoolia) -käyttöoikeudet **Logs**- ja **Files**-kansioihin.

    1. Pidä yhtä kansiota valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse **Ominaisuudet**.
    2. Valitse **Ominaisuudet**-valintaikkunan **Suojaus**-välilehdestä **Muokkaa**.
    3. Lisää käyttäjät, jos käyttäjiä ei ole luettelossa.
    4. Toista vaiheet 1-3 toisen kansion kohdalla.

    ![Käyttöoikeuksien lisääminen palvelun käyttäjälle.](media/e-invoicing-ita-fatturapa-get-started-proxy-add-user.png)

## <a name="privacy-notice"></a>Tietosuojatiedot 

**Italialaisen sähköisen laskun** ottaminen käyttöön saattaa edellyttää, että rajoitetut tiedot lähetetään. Tietoihin sisältyy organisaation verorekisteröintitunnus. Järjestelmänvalvoja voi ottaa käyttöön ja poistaa käytöstä Italian sähköisen laskun toiminnon. Ominaisuus poistetaan käytöstä seuraavasti.

1. Siirry kohtaan **Organisaation hallinta** \> **Määritys** \> **Sähköisten asiakirjojen parametrit**.
2. Valitse **Ominaisuudet**-välilehdessä **Italian sähköinen laskutus** -toiminnon sisältävät rivit ja valitse sitten **Poista nyt käytöstä**.

Näistä ulkoisista järjestelmistä tähän Dynamics 365 -verkkopalveluun tuotuihin tietoihin sovelletaan [tietosuojalausuntoamme](https://go.microsoft.com/fwlink/?LinkId=512132). Katso lisätietoja maa-/aluekohtaisten toimintodokumentaatioiden tietosuojaosista.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen laskutuksen yleiskatsaus](e-invoicing-service-overview.md)
- [Sähköisen laskutuksen palvelun hallinnan aloittaminen](e-invoicing-get-started-service-administration.md)
- [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
