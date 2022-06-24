---
title: Hylättyjen ostoskorien tunnistaminen ja ilmoitusten lähettäminen asiakkaille
description: Tässä artikkelissa kuvataan, kuinka voit mukauttaa Microsoft Dynamics 365 Commercen hylättyjen ostoskorien liittimen näytesovelluksen hylättyjen ostoskorien havaitsemiseksi ja muistutussähköpostiviestin lähettämiseksi asiakkaille.
author: bicyclingfool
ms.date: 02/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 707640ca211e997533d0f5a0b4e6d52cb5be9db4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899207"
---
# <a name="detect-abandoned-carts-and-send-notifications-to-customers"></a>Hylättyjen ostoskorien tunnistaminen ja ilmoitusten lähettäminen asiakkaille

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka voit mukauttaa Microsoft Dynamics 365 Commercen hylättyjen ostoskorien liittimen näytesovelluksen hylättyjen ostoskorien havaitsemiseksi ja muistutussähköpostiviestin lähettämiseksi asiakkaille.

Mahdollisuus parantaa tuottoa ja säilyttää asiakkaat hylättyjen ostoskorien ilmoitusten avulla on tärkeä ominaisuus, jota Dynamics 365 Commerce tukee. Mukauttamalla Commercen hylätyn ostoskärryn näytesovelluksen, vähittäismyyjät voivat käyttää Retail Serverissä ostoskärryjä, joita ei ole muutettu vähittäismyyjien määrittämän aikaikkunan aikana. Nämä ostoskorit voidaan sitten hakea, laajentaa tuote- ja asiakastiedoilla ja siirtää kolmannen osapuolen sähköpostimarkkinoinnin tarjoajalle, joka voi luoda sähköposti-ilmoituksia ja lähettää niitä asiakkaille.

Hylättyjen ostoskärryjen sähköposti-ilmoitus, jonka asiakkaat saavat, voi sisältää seuraavat tiedot:

- Asiakkaan etunimi.
- Asiakkaan sukunimi.
- Asiakkaan sähköpostiosoite.
- URL-osoite, joka palauttaa asiakkaan ostoskoriinsa.
- Tapahtuman valuutta.
- Asiakkaan ostoskärryssä olevien tuotteiden luettelo. Seuraavat tiedot sisältyvät kuhunkin tuotteeseen:

    - Tuotteen näyttönimi
    - Tuotetunnus (jota käytetään URL-osoitteen muodostamiseen tuotekuvaussivulle)
    - Tuotekuva, jonka kokoa voidaan muuttaa automaattisesti eri näyttökokoja varten.
    - Tuotekuvan vaihtoehtoinen teksti
    - Tuotteen yksikköhinta

## <a name="abandoned-cart-connector-sample"></a>Hylätty ostoskorin liittimen esimerkki

Microsoftin Retail-ohjelmistokehityssarjan (SDK) kautta toimitettavan liitinmallin avulla hylättyjen ostoskärryjen tiedot voidaan hakea ja lähettää kolmannen osapuolen sähköpostimarkkinoinnin tarjoajalle. Tämä liitin käsittelee viestintää Retail Serverin kanssa, käyttää Azure Key Vaultia tietoturvaan, käsittelee ostoskorien haun ajoitusta määritettyä aikaikkunaa varten sekä noutaa tilaus- ja tuotetiedot. Mukana on myös esimerkki käyttöönotosta kolmannen osapuolen sähköpostimarkkinoinnin tarjoajan kanssa integroimista varten. Liitin on suunniteltu niin, että se kommunikoi käyttövalmiina [Emarsysin](https://emarsys.com) kanssa. Se voidaan kuitenkin helposti integroida muihin ratkaisuihin, kuten Constant Contact, Mailchimp ja SendGrid.

Seuraavassa kuvassa on hylättyjen ostoskärryjen liittimen näytesovelluksen komponentit.

![Hylätyn ostoskorin liittimen mallisovelluksen komponentit](media/AbandonedCartConnector.png)

> [!IMPORTANT]
> Joissakin alueissa edellytetään, että asiakkaat voivat estää ostoskoritietonsa välittämisen sähköpostimarkkinoinnin palveluntarjoajalle tai pyytää tietojen poistamista. Microsoft ei kuitenkaan tarjoa näitä asetuksia asiakkaille. Jos siis aiot tehdä liiketoimintaa alueilla, joilla nämä määritykset ovat pakollisia, sinun on toimitettava tarvittava infrastruktuuri ja mukautukset asiakkaiden tarpeiden seuraamista varten. Näiden asetusten perusteella estät asiakastietojen välittämisen sähköpostiympäristöösi. Määritä myös prosessi, jonka avulla asiakastiedot voidaan tyhjentää sähköpostimarkkinoinnin palveluntarjoajalta asiakkaan pyynnöstä.

## <a name="obtain-the-code-sample"></a>Koodiesimerkin hankkiminen.

Hylätyn ostoskorin liittimen mallisovellus sisältyy Retail SDK -pakettiin versiosta 10.0.16 alkaen. Koodi löytyy kohdasta **\\RetailSDK\\Code\\SampleExtensions\\RetailServer\\Extensions.AbandonedCartSample**. Lisätietoja Retail SDK:n käytöstä ja hankkimisesta on kohdassa [Retail SDK](retail-sdk/retail-sdk-overview.md).

> [!NOTE]
> Vaikka mallikoodi on ensimmäisen kerran käytettävissä versiossa 10.0.16, se on yhteensopiva Retail Serverin version 10.0.13 ja sitä myöhempien versioiden kanssa.

## <a name="prerequisites-and-dependencies"></a>Edellytykset ja riippuvuudet

Ennen kuin voit ottaa käyttöön ja konfiguroida hylätyn ostoskärryn liittimen näytekoodin, seuraavien edellytysten on täytyttävä.

### <a name="access-to-commerce-resources"></a>Commerce-resurssien käyttö

Jotta voit konfiguroida ja ottaa käyttöön hylätyn ostoskorin liitinsovelluksen, sinulla on oltava seuraavien Commerce-resurssien käyttöoikeus:

- Ympäristösi Commerce Headquartersin järjestelmänvalvojan käyttöoikeudet
- Ympäristösi Microsoft Dynamics Lifecycle Services (LCS) -projektin käyttöoikeus

### <a name="azure-cosmos-db"></a>Azure Cosmos DB

Hylätyn ostoskorin liitinsovellus seuraa aiemmin haettujen ostoskärryjen tunnuksia ja aikaleimoja Azure Cosmos DB:n avulla. Voit käyttää Azure Cosmos DB -tietokantaa, että kaikki nämä tiedot säilyvät tai voit integroida muihin tallennusvaihtoehtoihin räätälöimällä koodiesimerkkiä. Lisätietoja Azure Cosmos DB:stä on kohdassa [Azure Cosmos DB: esittely](/azure/cosmos-db/introduction).

Jos käytät Azure Cosmos DB:tä, seuraavien edellytysten on toteuduttava, ennen kuin voit suorittaa esimerkin:

- Sinulla on oltava aktiivinen Azure Cosmos DB -tili. Jos sinulla ei ole tiliä, katso lisätietoja kohdassa [Tietokantatilin luominen](/azure/cosmos-db/create-sql-api-dotnet#create-a-database-account).
- Sinun on noudettava **URI**- ja **PRIMARY KEY**- (tai **SECONDARY KEY**) -arvot **Avaimet**-osiosta Azure Cosmos DB -tilissä Azure-portaalissa. Lisätietoja päätepisteen Azure Cosmos DB -tilin tietojen ja avaintietojen noutamisesta on kohdassa [Käyttöoikeusavainten ja salasanojen tarkasteleminen, kopioiminen ja muodostaminen uudelleen](/azure/cosmos-db/manage-account#keys).

### <a name="azure-key-vault"></a>Azure Key Vault

Hylätyn ostoskorin liitinsovellus tallentaa Key Vaultiin suojausta edellyttävät komponenttien nimet ja salasanat.

Määritä avainsäilö noudattamalla seuraavia ohjeita.

1. Noudata seuraavia ohjeita: [Key Vaultin hallinta Azure Stack Hubissa portaalin avulla](/azure-stack/user/azure-stack-key-vault-manage-portal?view=azs-2002&preserve-view=true).
2. Luo salasanat seuraaville tiedoille:

    - Emarsys-ohjelmointirajapinnan (API) käyttäjänimi ja salasana
    - Hylätyn ostoskorin sovelluksen tunnus ja salasana

Hylätyn ostoskorin liittimen mallikoodi käyttää Key Vaultiin Azure-oletustunnistetietoja. Sinun on annettava **Luettelo**- ja **Luku**-oikeudet tunnistetiedoille, joita aiot käyttää Key Vaultiin.

Lisätietoja Azure-oletustunnistetiedoista: [DefaultAzureCredential-luokka](/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet&preserve-view=true).

## <a name="create-an-abandoned-cart-connector-sample-app-application-id-for-the-azure-ad-tenant"></a>Luo hylätyn ostoskorin liittimen mallisovelluksen tunnus Azure AD -vuokraajalle

Sinun on luotava hylätyn ostoskorin liittimen mallisovelluksen tunnus Azure Active Directory (AD) -vuokraajalle. Lisätietoja sovellustunnuksen luomisesta on kohdassa [Azure AD -sovelluksen ja resursseja käyttävän palvelun päänimen luonti portaalin avulla](/azure/active-directory/develop/howto-create-service-principal-portal).

## <a name="add-the-abandoned-cart-connector-sample-app-application-id-to-the-allow-list-for-the-retail-server-api"></a>Lisää hylätyn ostoskorin liitinmallisovelluksen sovellustunnus Retail Server -ohjelmointirajapinnan sallittujen luetteloon

Seuraavaksi on lisättävä hylätyn ostoskorin liitinmallisovelluksen sovellustunnus Retail Server -ohjelmointirajapinnan sallittujen luetteloon. Lisätietoja sovellustunnuksen lisäämisestä Azuren sallittujen luetteloon: [Retail Serverin tuki palvelulta palvelulle -todennukselle](https://community.dynamics.com/ax/b/axforretail/posts/support-for-service-to-service-authentication-in-retail-server).

## <a name="configure-the-abandoned-cart-connector-sample-app"></a>Hylätyn ostoskorin liittimen mallisovelluksen määritys

Voit konfiguroida hylätyn ostoskorin liitinmallisovellusta muokkaamalla **AbandonedCartDetectionSample**-hakemiston juuressa sijaitsevaa **appSettings.json**-konfigurointitiedostoa. Seuraavissa taulukoissa kuvaillaan konfigurointitiedoston ominaisuudet.

### <a name="keyvaultoptions"></a>KeyVaultOptions

| Ominaisuus    | Kuvaus |
| ----------- | ----------- |
| KeyVaultURI | Sen avainsäilön DNS-toimialuenimi, jota käytät Azure-portaalissa. |

### <a name="retailserverclientoptions"></a>RetailServerClientOptions

| Ominaisuus                                      | Kuvaus |
| --------------------------------------------- | ----------- |
| TenantId                                      | Azure-vuokraajan Azure AD -vuokraajatunnus. |
| RetailServerAudienceId                        | Retail Serverin kohdeyleisötunnus. Voit jättää oletusarvon. |
| AppIdKeyVaultSecretName                       | Hylätyn ostoskorin liittimen mallisovelluksen tunnukselle luodun salasanan nimi. |
| AppSecretKeyVaultSecretName                   | Hylätyn ostoskorin liittimen mallisovelluksen tunnuksen sovellussalasanan tallentavan salasanan nimi. |
| RetailServerUrl                               | Retail Server -instanssin URL-osoite. Tämä arvo löytyy LCS:stä. |
| OperatingUnitNumber                           | Toimintayksikön numero (OUN). Tämä arvo löytyy Commerce Headquartersista. |
| IncludeAbandonedCartsModifiedSinceLastMinutes | Aikaikkunan alku hylättyjä niitä ostoskärryjä varten, jotka haluat noutaa. Arvo ilmaistaan minuutteina ennen kuluvaa aikaa. Määritä esimerkiksi arvoksi **120**, kun haluat noutaa kaikki ostoskorit, joita on viimeksi muokattu aikavälillä 120 minuuttia sitten – aikaikkunan loppuaika, jonka määrittää **ExcludeAbandonedCartsModifiedSinceLastMinutes**-ominaisuus. |
| ExcludeAbandonedCartsModifiedSinceLastMinutes | Aikaikkunan loppu hylättyjä niitä ostoskärryjä varten, jotka haluat noutaa. Arvo ilmaistaan minuutteina ennen kuluvaa aikaa. Jos esimerkiksi **IncludeAbandonedCartsModifiedSinceLastMinutes**-ominaisuudenarvoksi on määritetty **120**, määritä tämän ominaisuuden arvoksi **30**, jotta voit noutaa kaikki ostoskorit, joita muokattiin välillä 120 minuuttia sitten – 30 minuuttia sitten. Käytännössä tämä ominaisuus määrittää ajan, jonka jälkeen ostoskori katsotaan hylätyksi. |
| ReturnToCartUrl                               | Verkkokaupan sivuston ostoskärryn URL-osoite muodossa, jota käytetään **app.config**-tiedostossa. |

### <a name="azurecosmosoptions"></a>AzureCosmosOptions

Hylättyjen ostoskärryjen noutotyön tila, kärryjen tunnukset ja muokatut aikaleimat tallennetaan Azure Cosmos DB -tietokantaan. Oletusarvon mukaan konfigurointitiedostossa olevat asetukset osoittavat Azure Cosmos DB:n paikalliseen emulaattoriesiintymään. Kun otat liittimen käyttöön tuotannossa, nämä asetukset on päivitettävä niin, että ne viittaavat Azure-tilauksesi Azure Cosmos DB -esiintymään. Paikallisessa tai eristysympäristön testeissä voit käyttää [Azure Cosmos DB -emulaattoria](/azure/cosmos-db/local-emulator).

| Ominaisuus    | Kuvaus |
| ----------- | ----------- |
| EndPointUri | URI-päätepiste, jonka toimittaa Azure tai emulaattori. |
| PrimaryKey  | Ensisijainen avain, jonka toimittaa Azure tai emulaattori. |
| DatabaseId  | Tietokannan tunnus. Voit jättää oletusarvon tai antaa oman arvon. |
| ContainerId | Säilön tunnus. Voit jättää oletusarvon tai antaa oman arvon. |

### <a name="emarsysclientoptions"></a>EmarsysClientOptions

> [!NOTE]
> Jos integroit muuhun sähköpostimarkkinoinnin palveluntarjoajaan kuin Emarsys-tarjoajaan, sinun on laajennettava **IEmailProvider**-liittymää niin, että se on yhteydessä kyseiseen palveluntarjoajaan.

| Ominaisuus                      | Kuvaus |
| ----------------------------- | ----------- |
| ApiUrl                        | `https://api.emarsys.net/api/v2/event/{0}/trigger` |
| ExternalEventId               | Emarsysissa luodun ulkoisen tapahtumatietueen tunnus. **Käynnistinasetukset**-kohdassa on tämä arvo kampanjassa, jonka loit hylätyn ostoskärryn sähköposti-ilmoitusten lähettämiseen. |
| ApiUserNameKeyVaultSecretName | Sen avaimen nimi, johon Emarsys-ohjelmointirajapinnan käyttäjänimi tallennetaan. |
| ApiSecretKeyVaultSecretName   | Sen avaimen nimi, johon Emarsys-ohjelmointirajapinnan salasana tallennetaan. |
| EmarsysContactKeyId           | Emarsys-yhteyshenkilötietokannan sähköpostisarakkeen tunnus. Oletusarvo on **3**, eikä sitä tarvitse muuttaa. |

### <a name="mediaoptions"></a>MediaOptions

Jos käytät Commercen sähköisen kaupankäynnin ominaisuuksia, voit hakea tuotekuvia Commercen digitaalisten resurssien hallinnan avulla. Lisätietoja kuvan koon muuttamisen ominaisuuksista digitaalisten resurssien hallinnassa on kohdassa [ImageSettings-näyttökokokonfiguraatio](../e-commerce-extensibility/image-component.md#imagesettings-viewport-configuration).

| Ominaisuus                             | Kuvaus |
| ------------------------------------ | ----------- |
| ImageServerUrl                       | Sivustosi digitaalisten resurssien hallinnan juuri-URL-osoite. Löydät arvon **Mediapalvelimen perus-URL-osoite** -ominaisuudesta kohdassa **Retail ja Commerce \> Kanavan asetukset \> Kanavaprofiilit** Commerce Headquartersissa. |
| ImageViewPorts                       | Yksittäisten näyttökokokonfiguraatioiden säilösolmu. |
| ImageViewPorts/viewport              | Näyttökoon määritys. Tämän ominaisuuden avulla voit määrittää näyttökoon leveysvälit kuvapisteinä. Esimerkki siitä, miten tätä ominaisuutta käytetään, on **appSettings.json**-konfigurointitiedostossa. |
| ImageViewPorts/imageWidth            | Näyttökoon kuvaleveys kuvapisteinä. |
| imageViewPorts/imageHeight           | Näyttökoon kuvakorkeus kuvapisteinä. |
| imageViewPorts/useForDefaultImageTag | **Tosi**/**Epätosi**-arvo, joka ilmaisee, käytetäänkö näyttökoon ilmaisemia kuvadimensioita, jos HTML-tunnistetta `<picture>` ei tueta www-selaimessa tai sähköpostiohjelmassa. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
