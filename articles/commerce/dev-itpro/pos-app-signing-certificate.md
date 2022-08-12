---
title: MPOS:n appx-tiedoston allekirjoittaminen koodin allekirjoitusvarmenteella
description: Tässä artikkelissa kerrotaan, miten MPOS allekirjoitetaan koodin allekirjoitusvarmenteella.
author: mugunthanm
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 28021
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.openlocfilehash: 4cbdfcb5229be2f04531031c80f41f672b2a4747
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169096"
---
# <a name="sign-the-mpos-appx-file-with-a-code-signing-certificate"></a>MPOS:n appx-tiedoston allekirjoittaminen koodin allekirjoitusvarmenteella

[!include [banner](../includes/banner.md)]

Jos haluat asentaa Modern POS:n (MPOS), sinun on allekirjoitettava MPOS-sovellus luotettavan palveluntarjoajan koodin allekirjoitusvarmenteella ja asennettava sama varmenne kaikkiin koneisiin, joissa MPOS on asennettu nykyisen käyttäjän luotettuun juurikansioon.

Voit allekirjoittaa MPOS-sovelluksen varmenteella käyttämällä yhtä näistä **Retail SDK\\Build tool\\Customization.settings** -tiedoston vaihtoehdoista:

- Lisää Azure DevOps-koontivaiheiden Suojattu tiedosto - tehtäväosa ja suojaa tiedostotehtävä lataamalla varmenne. Käytä suojatun tiedoston tehtävän tulostuspolun muuttujaa Customization.settings-tiedoston parametrina.

    > [!NOTE]
    > Suojattu tiedosto -tehtävä ei tue salasanalla suojattua varmennetta. Sinun on poistettava salasana ennen tehtävän lataamista. Koska varmenne ladataan suojatun tiedoston järjestelmän tehtävälle Azuressa, voit poistaa salasanan vain tätä vaihetta varten. Sinun tulee kuitenkin keskustella salasanan poistamisesta tietoturva-asiantuntijoiden kanssa selvittääksesi, onko tämä oikea toimenpide projektillesi. Älä poista muiden skenaarioiden varmenteiden salasanaa.
- Käytä tiedostojärjestelmässä käytettävää varmennetta. Voit tehdä tämän lataamalla tai muodostamalla varmenteen ja asettamalla sen tiedostojärjestelmään, jossa koontiversio on käynnissä. Microsoftin isännöimällä agentilla tai koontiversion käyttäjällä tulisi olla tämän polun ja tiedoston käyttöoikeus.
- Käytä allekirjoitusta etsiäksesi varmennetta kaupasta ja kirjautuaksesi sisään kyseisellä varmenteella.

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>Käytä suojatun tiedoston tehtävää Universal Windows Platform -sovelluksen allekirjoittamiseen

> [!NOTE]
> Voit myös käyttää Azure Key Vaultia varmenteen tallentamiseen ja Azuren allekirjoitustyökalua Modern POS:n .appx-tiedoston ja itsepalveluasentajien allekirjoittamiseen. Katso esimerkkijakson komentosarjoja ja lisätietoja kohdasta [Määritä koontijakso Azure DevOps-ohjelmassa vähittäismyynnin itsepalvelupakettien luomiseksi](build-pipeline.md#set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages).

Suojattu tiedosto -tehtävän käyttäminen on suositeltu lähestymistapa Universal Windows Platform (UWP) -sovelluksen allekirjoitukseen. Lisätietoja paketin allekirjoittamisesta on kohdassa [Määritä paketin allekirjoitus](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing). Tämä prosessi on esitetty seuraavassa kuvassa.

![MPOS-sovelluksen allekirjoitusvirta.](media/POSSigningFlow.png)

> [!NOTE]
> Tällä hetkellä OOB-pakkaus tukee vain .appx-tiedoston allekirjoittamista, eri itsepalveluasennusohjelmia, kuten MPOIS, RSSU ja HWS, ei allekirjoiteta tällä prosessilla. Se on allekirjoitettava manuaalisesti SignToolilla tai muiden allekirjoitustyökalujen avulla. Appx-tiedoston allekirjoittamiseen käytettävä varmenne on asennettava koneeseen, johon Modern POS on asennettu.

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a>Vaiheet varmenteen määrittämiseksi Azure Pipelinesissa allekirjoittamista varten

### <a name="certificate-in-the-file-systemsecure-location"></a>Varmenne tiedostojärjestelmässä/suojatussa paikassa

Lataa [DownloadFile-tehtävä](/visualstudio/msbuild/downloadfile-task) ja lisää se koontiversioprosessin ensimmäiseksi vaiheeksi. Suojattu tiedosto -tehtävän käytön etuna on, että tiedosto salataan ja sijoitetaan levylle koonnin aikana riippumatta siitä, onnistuuko, epäonnistuu tai peruutetaanko koontiprosessi. Tiedosto poistetaan lataussijainnista, kun koontiprosessi on valmis.

1. Lataa Suojattu tiedosto -tehtävä ja lisää se Azuren koontijakson ensimmäiseksi vaiheeksi. Voit ladata Suojattu tiedosto -tehtävän [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile)-kohdasta.
1. Lataa varmenne Suojattu tiedosto -tehtävään ja määritä viitenimi Tulostusmuuttujat-kohdassa seuraavan kuvan mukaisesti.
    > [!div class="mx-imgBorder"]
    > ![Suojattu tiedosto -tehtävä.](media/SecureFile.png)
1. Luo uusi muuttuja Azure Pipelinesissa valitsemalla **Muuttujat**-välilehdestä **Uusi muuttuja**.
1. Kirjoita muuttujan nimi arvokenttään, esimerkiksi **MySigningCert**.
1. Tallenna muuttuja.
1. Avaa **Customization.settings**-tiedosto kohteesta **RetailSDK\\BuildTools** ja päivitä **ModernPOSPackageCertificateKeyFile** jaksossa luodun muuttujan nimellä (vaihe 3). Esimerkki:

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    Tämä vaihe on pakollinen, jos varmennetta ei ole suojattu salasanalla. Jos varmenne on suojattu salasanalla, noudata seuraavia ohjeita.
    
1. Jos haluat aikaleiman MPOS:n .appx -tiedostoon varmennetta allekirjoitettaessa, avaa **Retail SDK\\Build tool\\Customization.settings** -tiedosto ja päivitä **ModernPOSPackageCertificateTimestamp** -muuttuja aikaleimapalveluntarjoajalla (esimerkiksi `http://timestamp.digicert.com`).
1. Lisää jakson **Muuttujat**-välilehteen uusi suojaustekstimuuttuja. Määritä nimeksi **MySigningCert.secret** ja määritä varmenteen salasanan arvo. Voit suojata muuttujan valitsemalla lukituskuvakkeen.
1. Lisää **Powershellin komentosarja** -tehtävä jaksoon (Lataa suojattu tiedosto jälkeen ja ennen koontivaihetta). Anna **Näyttönimi** ja määritä tyypiksi **Sisäinen**. Kopioi ja liitä seuraavat tiedot komentosarjaosaan.

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

1. Avaa **Customization.settings**-tiedosto kohteesta **RetailSDK\\BuildTools** ja päivitä **ModernPOSPackageCertificateThumbprint** varmenteen allekirjoituksen arvolla.

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
Lisätietoja allekirjoituksen saamisesta varmenteelle on kohdassa [varmenteen allekirjoituksen noutaminen](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate#to-retrieve-a-certificates-thumbprint). 

## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a>Lataa tai luo varmenne allekirjoittaaksesi MPOS-sovelluksen manuaalisesti SDK:n msbuildin avulla

Jos MPOS-sovelluksen allekirjoittamiseen käytetään ladattua tai luotua varmennetta, päivitä **ModernPOSPackageCertificateKeyFile**-solmu **BuildTools\\Customization.settings** -tiedostossa osoittamaan pfx-tiedoston sijaintiin (**$(SdkReferencesPath)\\appxsignkey.pfx**). Esimerkki:

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

Tässä tapauksessa varmennetiedoston nimi on **appxsignkey.pfx**, joka sijaitsee **Retail SDK\\Viite** -kansiossa.

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>Käytä allekirjoitusta MPOS-sovelluksen allekirjoittamiseen

Jos allekirjoitit MPOS-sovelluksen allekirjoituksen avulla, asenna varmenne paikallisesti. Päivitä allekirjoituksen arvo **ModernPOSPackageCertificateThumbprint**-solmussa **BuildTools\\Customization.settings** -tiedostossa.

Tämä vaihtoehto toimii, jos koontikäyttäjä on paikallinen käyttäjä. Jos kuitenkin käytät Azure DevOps-agentteja koontiversion luomiseen, agentilla ei ehkä ole oikeutta käyttää cert-myymälää varmenteen käyttämiseen allekirjoittamiseen, tai koontiversiokoneessa ei ole sertifikaattia asennettuna. Tässä tapauksessa voit muuttaa koontiversion käyttäjän paikalliseksi käyttäjäksi ja asentaa varmenteen ruutuun. Tämä vaihtoehto ei kuitenkaan toimi, jos et voi käyttää ruutua järjestelmänvalvojana.

> [!NOTE]
> Jos .pfx-tiedostoa tai suojatun tiedoston tehtävävaihtoehtoa käytetään sovelluksen allekirjoittamiseen, jätä **ModernPOSPackageCertificateThumbprint**-solmu kohdassa **Customization.settings** tyhjäksi. Jos käytetään allekirjoitusvaihtoehtoa, **ModernPOSPackageCertificateKeyFile**-kohta tyhjäksi. Jos molemmat arvot päivitetään, koontiversio epäonnistuu.

### <a name="certification-renewal"></a>Varmenteen uusiminen

### <a name="renew-a-certificate-from-trusted-ca"></a>Varmenteen uusiminen luotettavalta varmenteen myöntäjältä

Ota yhteyttä varmenteiden myöntäjään (CA) varmenteen uusimisprosessia varten Luotettavassa varmenteessa MPOS-puolelta ei edellytetä toimenpiteitä.

### <a name="renew-a-self-signed-certificate"></a>Itseallekirjoitetun varmenteen uusiminen

Älä käytä Retail SDK:n mallivarmennetta tuotantoa varten. Sitä voidaan käyttää vain kehityksessä. Contoso-esimerkkivarmennetta ei voi uusita, ja Retail SDK -versioon 10.0.16 tai aiempiin versioihin sisältyvä mallivarmenne vanhenee 31.12.2020. Jos tätä varmennetta tai itse allekirjoitettua varmennetta on käytetty mukautetun Modern POS:n allekirjoittamiseen, on erittäin mahdollista, että Modern POS ei toimi oikein tämän päivämäärän jälkeen.
 
### <a name="impact"></a>Vaikutus
 
Jos yllä esitetty pitää paikkansa, ongelma, joka ilmenee on se, että asennusohjelmaa ei voi suorittaa 31.12.2020 jälkeen. Käytetyistä yrityksen IT-käytännöistä riippuen Modern POS ei ehkä toimi. On tärkeää testata tämä vaihtamalla päivämäärä väliaikaisesti tulevaksi päiväksi, jotta vaikutus organisaatioosi määritetään.
 
### <a name="steps-to-determine-the-issue"></a>Toimenpiteet ongelman määrittämiseksi
 
1.  Windowsin asetusten avulla voit muuttaa tietokoneen kellon vuoden 2021 päivämääräksi ja kellonajaksi.
2.  Varmista, että Modern POS voidaan avata, sisäänkirjautuminen onnistuu ja tapahtuma voidaan suorittaa.
3.  Varmista, että Modern POS:n itsepalveluasennusohjelma voidaan suorittaa, ja jos voidaan, että asennus suoritetaan onnistuneesti.
4.  Palauta Windowsin kellon asetukset oikeaan päivämäärään ja kellonaikaan.
 
Jos kaikki nämä vaiheet voidaan suorittaa ongelmatta, voit käyttää nykyistä varmennetta 31.12.2020 jälkeen.  
 
### <a name="steps-going-forward"></a>Seuraavat vaiheet 

Aiemmin käytetyn varmenteen uusiminen on suositeltavaa. Suosittelemme uuden varmenteen hankkimista. Voit tehdä tämän suorittamalla jonkin seuraavista toimista:
 
- **Ensisijainen** - Hanki koodin allekirjoitusvarmenne luotettavalta varmenteen myöntäjältä.

- **Ei ensisijainen** - Luo itseallekirjoitettu koodin allekirjoitusvarmenne käytettäväksi. Sitä käytetään yleensä vain toimialueen kehitystarkoituksiin. Sitä ei suositella tuotantoa varten. 

- **Saatavana väliaikaisena ratkaisuna** - Käytä uusittua Contoso-koodin allekirjoitusvarmennetta. Tätä käytetään yleensä testaustarkoituksiin, joten sitä ei suositella käytettäväksi tuotannossa.
 
Luo seuraavaksi uusi mukautettu Modern POS -paketti, joka on allekirjoitettu jollakin yllä olevista toimista saadulla varmenteella. Varmenteen mukaan on suoritettava jokin seuraavista vaiheista:
 
- Jos käytät uutta luotettua varmennetta (tai uutta, itse allekirjoitettua varmennetta), sinun on asennettava uusi varmenne jokaiseen laitteeseen. Tämän jälkeen sinun on otettava äskettäin luotu Modern POS -paketti (asennusohjelma), poistettava olemassa oleva sovellus ja asennettava sitten uusi Modern POS -paketti uudelleen. Sinun on suoritettava Modern POS -laitteen aktivointi jokaisessa laitteessa.

- Jos käytät uusittua Contoso-varmennetta, sinun on asennettava uusi varmenne jokaiseen laitteeseen ja asennettava Modern POS -paketti (asennusohjelma). Sinun ei tarvitse poistaa asennusta, mutta sinun on asennettava laitteeseen uudelleen. Huomaa, että Modern POS:n laitteen aktivointia ei tarvita. Tämä vaihtoehto on väliaikainen ratkaisu. Käytä tätä vaihtoehtoa vain välttääksesi uudelleenaktivoinnin ja ratkaistaksesi ongelman ennen uuden luotettavan varmenteen hankkimista.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
