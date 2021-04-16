---
title: Sähköisen laskutuksen palvelun hallinnan aloittaminen
description: Tässä aiheessa selitetään, miten sähköisen laskutuksen käyttö voidaan aloittaa.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840145"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>Sähköisen laskutuksen palvelun hallinnan aloittaminen

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit suorittaa tämän ohjeaiheen vaiheita, seuraavien edellytysten on toteuduttava:

- Sinulla on oltava Microsoft Dynamics Lifecycle Services (LCS) -tili.
- Käytössäsi on oltava LCS-projekti, joka sisältää Microsoft Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin version 10.0.17 tai sitä myöhemmän version. Lisäksi nämä sovellukset on otettava käyttöön jossakin seuraavista Azure-alueista:

    - Itä-Yhdysvallat
    - Länsi-Yhdysvallat
    - Pohjois-EU
    - Länsi-EU

- Dynamics 365 Regulatory Configuration Services (RCS) -tilin on oltava käytettävissä.
- RCS-tilin globalisointiominaisuus on otettava käyttöön toiminnonhallinnan kautta. Lisätietoja: [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md).
- On luotava avainsäilö ja tallennustili Azuressa. Lisätietoja: [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Microservices-lisäosan asentaminen Lifecycle Servicesissa

1. Kirjaudu LCS-tilille.
2. Valitse **Esiversiotoiminnon hallinta** -ruutu.
3. Valitse **Julkisen esiversion ominaisuudet** -osasta **Sähköisen laskutuksen palvelu**.
4. Varmista, että **Esiversiotoiminto käytössä** -asetukseksi on valittu **Kyllä**.
5. Valitse LCS-käyttöönottoprojekti LCS-koontinäytössä. LCS-projektin on oltava käynnissä.
7. Valitse **Ympäristöapuohjelmat**-välilehdessä **Asenna uusi apuohjelma**.
8. Valitse **sähköisen laskutuksen palvelut**.
9. Kirjoita **AAD-sovellustunnus**-kenttään **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Tämä on kiinteä arvo.
10. Syötä **AAD-vuokraajatunnus**-kenttään Azure-tilaustilisi vuokraajan tunnus.
11. Lue ehdot ja valitse valintaruutu.
12. Valitse **Asenna**.


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Määritä RCS-integroinnin parametrit sähköisen laskutuksen avulla

1. Kirjaudu RCS-tilille.
2. Valitse **Sähköisen raportointi** -työtilan **Liittyvät linkit** -osassa **Sähköisen raportoinnin parametrit**.
3. Kirjoita **Sähköisen laskutuksen palvelu** -välilehdessä **Palvelun päätepisteen URI** -kenttään asianmukainen Azure-alueen palvelun päätepiste, joka näkyy seuraavassa taulukossa.

    | Konesalin Azure-alue | Palvelun päätepisteen URI-osoite                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Itä-Yhdysvallat                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | Länsi-Yhdysvallat                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Pohjois-EU                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Länsi-EU                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. Varmista, että **Sovellustunnus**-kentän arvo on **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Tämä arvo on kiinteä arvo.
5. Syötä **LCS-ympäristötunnus**-kenttään LCS-ympäristösi tunnus.
6. Valitse **Tallenna** ja sulje sitten sivu.

## <a name="create-key-vault-references"></a>Avainsäilöviitteiden luominen

1. Kirjaudu RCS-tilille.
2. Valitse **Globalisaatio-ominaisuudet**-työtilan **Ympäristö**-osassa **Sähköinen laskutus** -ruutu.
3. Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Palveluympäristö** ja valitse sitten **Key Vault -parametrit**.
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

1. Valitse **Ympäristöasetukset**-sivulla **Uusi**, jos haluat määrittää liitetyn sovelluksen ympäristöön.
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
2. Kirjoita **Lähetyspalvelu** -välilehdessä **Palvelun päätepisteen URL** -kenttään asianmukainen Azure-alueen palvelun päätepiste, joka näkyy seuraavassa taulukossa.

    | Konesalin Azure-alue | Palvelun päätepisteen URL-osoite                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Itä-Yhdysvallat                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | Länsi-Yhdysvallat                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Pohjois-EU                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Länsi-EU                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. Syötä **Ympäristö**-kenttään sähköisessä laskutuksessa julkaistun palveluympäristön nimi.
4. Valitse **Tallenna** ja sulje sitten sivu.

### <a name="enable-flighting-keys"></a>Väliversioavainten ottaminen käyttöön

Ota käyttöön väliversioavaimet Microsoft Dynamics 365 Financelle tai Microsoft Dynamics 365 Supply Chain Management -versiolle 10.0.17 tai vanhemmalle versiolle. 
1. Suorita seuraava SQL-komento:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. Suorita IISreset-komento kaikille AOS-kohteille.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
