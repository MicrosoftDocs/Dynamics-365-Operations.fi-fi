---
title: Sähköisen laskutuksen palvelun hallinnan aloittaminen
description: Tässä aiheessa selitetään, miten sähköisen laskutuksen käyttö voidaan aloittaa.
author: gionoder
ms.date: 03/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: be9e823a0c70aebcfd5353f7b922f8f4b1aa3d73
ms.sourcegitcommit: cc49cf74bd5a34f97a02cdccd473a6479e175a5b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/30/2022
ms.locfileid: "8493911"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>Sähköisen laskutuksen palvelun hallinnan aloittaminen

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit suorittaa tämän ohjeaiheen vaiheita, seuraavien edellytysten on toteuduttava:

- Sinulla on oltava Microsoft Dynamics Lifecycle Services (LCS) -tili.
- Käytössäsi on oltava LCS-projekti, joka sisältää Microsoft Dynamics 365 Financen tai Dynamics 365 Supply Chain Managementin version 10.0.17 tai sitä myöhemmän version. Lisäksi nämä sovellukset on otettava käyttöön jossakin seuraavista Azure-alueista:

    - Yhdysvallat
    - Eurooppa
    - Iso-Britannia
    - Aasia

- Dynamics 365 Regulatory Configuration Services (RCS) -tilin on oltava käytettävissä.
- RCS-tilin globalisointiominaisuus on otettava käyttöön toiminnonhallinnan kautta. Lisätietoja: [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md).
- On luotava avainsäilö ja tallennustili Azuressa. Lisätietoja: [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Microservices-lisäosan asentaminen Lifecycle Servicesissa

1. Kirjaudu sisään LCS-tiliiso ja LCS-koontinäytössä valitse LCS-projekti.
2. Valitse projektissa **Ympäristö**-koontinäytössä valitse käyttöön otettu ympäristö. Valitun ympäristön on oltava käynnissä.
3. Valitse **Power Platform -integrointi** -välilehden **Ympäristön lisäosat** -kenttäryhmässä **Asenna uusi lisäosa**.
4. Valitse **Sähköinen laskutus**.
5. Kirjoita **AAD-sovellustunnus**-kenttään **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Tämä on kiinteä arvo.
6. Syötä **AAD-vuokraajatunnus**-kenttään Azure-tilaustilisi vuokraajan tunnus. Määrittämäsi Azure Active Directory (Azure AD) -vuokraajan on oltava sama kuin RCS:ää varten käytetyn vuokraajan.
7. Lue ehdot ja valitse valintaruutu.
8. Valitse **Asenna**. Asennus voi kestää useita minuutteja.


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Määritä RCS-integroinnin parametrit sähköisen laskutuksen avulla

1. Kirjaudu RCS-tilille.
2. Valitse **Globalisaatiotoiminnot**-työtilan **Liittyvät asetukset** -osassa **Sähköisen raportoinnin parametrit**.
3. Kirjoita **Sähköinen laskutus** -välilehdessä **Palvelun päätepisteen URI** -kenttään asianmukainen Azure-alueen palvelun päätepiste, joka näkyy seuraavassa taulukossa.

    | Konesalin Azure-alue | Palvelun päätepisteen URI-osoite                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Yhdysvallat              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Eurooppa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Yhdistynyt kuningaskunta             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Aasia                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Japani                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Sveitsi                | <p>`https://gw.ch-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Brasilia                     | <p>`https://gw.br-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.br-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Yhdistyneet arabiemiirikunnat       | <p>`https://gw.ae-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Australia                  | <p>`https://gw.au-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.au-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Kanada                     | <p>`https://gw.ca-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.ca-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Ranska                     | <p>`https://gw.fr-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Intia                      | <p>`https://gw.in-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |


4. Varmista, että **Sovellustunnus**-kentän arvo on **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Tämä arvo on kiinteä arvo.
5. Syötä **LCS-ympäristötunnus**-kenttään LCS-ympäristösi tunnus.
6. Valitse **Tallenna** ja sulje sitten sivu.

## <a name="create-key-vault-references"></a>Avainsäilöviitteiden luominen

1. Kirjaudu RCS-tilille.
2. Valitse **Globalisaatio-ominaisuudet**-työtilan **Ympäristö**-osassa **Sähköinen laskutus** -ruutu.
3. Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Palveluympäristöt** ja valitse sitten **Key Vault -parametrit**.
4. Valitse **Uusi**, jos haluat luoda avainsäilön viitteen.
5. Syötä **Nimi**-kenttään avainsäilön viitteen nimi. Syötä **Kuvaus**-kenttään kuvaus.
6. Liitä **Key Vault – URI** -kenttään Azure Key Vaultin avainsäilön salainen koodi. Lisätietoja: [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).
7. Valitse **Tallenna**.

## <a name="create-storage-account-secret"></a>Luo tallennustilin salainen koodi

1. Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Palveluympäristö** > **Key Vault -parametrit**.
2. Valitse **Varmenteet**-osasta **Key Vault -viite** ja sitten **Lisää**.
3. Syötä **Nimi**-kenttään tallennustilin salaisen koodin nimi. Lisätietoja: [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).
4. Syötä **Kuvaus**-kenttään kuvaus.
5. Kirjoita **Tyyppi**-kenttään **Salainen koodi**.
6. Valitse **Tallenna** ja sulje sitten sivu.

## <a name="create-a-digital-certificate-secret"></a>Digitaalisen varmenteen salaisen koodin luonti

1. Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Palveluympäristö** ja valitse sitten **Key Vault -parametrit**.
2. Valitse **Varmenteet**-osasta **Key Vault -viite** ja sitten **Lisää**.
3. Syötä **Nimi**-kenttään digitaalisen varmenteen salaisen koodin nimi. Lisätietoja: [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).
4. Syötä **Kuvaus**-kenttään kuvaus.
5. Valitse **Tyyppi**-kentästä **Varmenne**.
6. Valitse **Tallenna** ja sulje sitten sivu.

## <a name="create-a-service-environment"></a>Palveluympäristön luominen

1. Kirjaudu RCS-tilille.
2. Valitse **Globalisaatio-ominaisuudet**-työtilan **Ympäristö**-osassa **Sähköinen laskutus** -ruutu.
3. Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Palveluympäristö**.
4. Luo uusi palveluympäristö valitsemalla **Uusi**.
5. Syötä **Nimi**-kenttään sähköisen laskutuksen ympäristön nimi. Syötä **Kuvaus**-kenttään kuvaus.
6. Valitse **Tallennutilin SAS-tunnuksen salasana** -kentässä sen tallennustilin varmenteen nimi, jota on käytettävä tallennustiliin todentautumisessa.
7. Valitse **Käyttäjät**-osassa **Lisää**, kun haluat lisätä käyttäjän, joka voi lähettää sähköisiä laskuja ympäristön kautta sekä muodostaa yhteyden tallennustiliin.
8. Kirjoita **Käyttäjätunnus**-kenttään käyttäjän alias. Kirjoita **Sähköpostiosoite**-kenttään käyttäjän sähköpostiosoite.
9. Valitse **Tallenna**.
10. Jos maa-/aluekohtaiset laskut edellyttävät tiettyjen varmenteiden soveltamista digitaaliseen allekirjoitukseen, valitse toimintoruudusta **Key Vaultin parametrit** sitten **Varmenneketju** ja suorita seuraavat vaiheet:

    1. Valitse **Uusi**, jos haluat luoda varmenneketjun.
    2. Syötä **Nimi**-kenttään varmenneketjun nimi. Syötä **Kuvaus**-kenttään kuvaus.
    3. Lisää ketjuun varmenne valitsemalla **Varmenteet**-osasta **Lisää**.
    4. Voit muuttaa todistuksen sijaintia ketjussa **Ylös**- tai **Alas**-painikkeella.
    5. Valitse **Tallenna** ja sulje sitten sivu.
    6. Sulje sivu.

11. Julkaise ympäristö pilveen valitsemalla **Palveluympäristö**-sivun toimintoruudussa **Julkaise**. **Tila**-kentän arvoksi tulee **Julkaisu**.

## <a name="create-a-connected-application"></a>Luo yhdistetty sovellus

1. Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Yhdistetyt sovellukset**.
2. Luo yhdistetty sovellus valitsemalla **Uusi**.
3. Syötä **Nimi**-kenttään yhdistettävän sovelluksen nimi.
4. Kirjoita **Sovellus**-kenttään sen Finance- tai Supply Chain Managements -ympäristön URL-osoite, johon haluat yhdistää.
4. Kirjoita **Vuokraaja**-kenttään Finance- tai Supply Chain Managements -ympäristön vuokraaja.
5. Valitse **Tallenna**.
6. Testaa yhteys ympäristöön valitsemalla toimintoruudussa **Tarkista yhteys**. Sulje sitten sivu.

## <a name="link-connected-applications-to-environments"></a>Liitettyjen sovellusten linkittäminen ympäristöihin

1. Valitse **Ympäristöasetus**-sivulla **Uusi**, jos haluat määrittää liitetyn sovelluksen ympäristöön.
2. Valitse **Yhdistetty sovellus** -kentässä yhdistetty sovellus.
3. Valitse **Palveluympäristö**-kentässä palveluympäristö.
4. Valitse **Tallenna** ja sulje sitten sivu.

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>Sähköisen laskutuksen integroinnin määrittäminen Financessa ja Supply Chain Managementissa

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>Sähköisen laskutuksen integrointitoiminnon käyttöönotto

1. Kirjaudu Finance- tai Supply Chain Management -esiintymään.
2. Etsi **Sähköisen laskutuksen integrointi** -toimintoa **Toiminnonhallinta**-työtilassa. Jos tämä toiminto ei näy sivulla, valitse **Tarkista päivitykset**.
3. Valitse toiminto ja valitse sitten **Ota käyttöön nyt**.

### <a name="set-up-the-service-endpoint-url"></a>Palvelun päätepisteen URL-osoitteen määritys

1. Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.
2. Kirjoita **Sähköinen laskutus** -välilehdessä **Päätepisteen URL** -kenttään asianmukainen Azure-alueen palvelun päätepiste, joka näkyy seuraavassa taulukossa.

    | Konesalin Azure-alue | Palvelun päätepisteen URI-osoite                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Yhdysvallat              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Eurooppa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Yhdistynyt kuningaskunta             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Aasia                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Japani                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Sveitsi                | <p>`https://gw.ch-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Brasilia                     | <p>`https://gw.br-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.br-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Yhdistyneet arabiemiirikunnat       | <p>`https://gw.ae-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Australia                  | <p>`https://gw.au-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.au-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Kanada                     | <p>`https://gw.ca-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.ca-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Ranska                     | <p>`https://gw.fr-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Intia                      | <p>`https://gw.in-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Syötä **Ympäristö**-kenttään sähköisessä laskutuksessa julkaistun palveluympäristön nimi.
4. Valitse **Tallenna** ja sulje sitten sivu.

### <a name="enable-flighting-keys-for-finance-or-supply-chain-management-version-10017"></a>Väliversioavainten käyttöönotto Financelle tai Supply Chain Managementin versiolle 10.0.17

1. Suorita seuraava SQL-komento:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. Suorita IISreset-komento kaikille AOS-kohteille.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
