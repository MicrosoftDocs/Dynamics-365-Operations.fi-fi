---
title: Sähköisen laskutuksen lisäosan palvelun hallinnan aloittaminen
description: Tässä aiheessa selitetään, miten sähköisen laskutuksen lisäosan käyttö voidaan aloittaa.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104373"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a>Sähköisen laskutuksen lisäosan palvelun hallinnan aloittaminen

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit suorittaa tämän ohjeaiheen vaiheita, seuraavien edellytysten on toteuduttava:

- Sinulla on oltava Microsoft Dynamics Lifecycle Services (LCS) -tili.
- Käytössäsi on oltava LCS-projekti, joka sisältää Microsoft Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin version 10.0.13 tai sitä myöhemmän version. Lisäksi nämä sovellukset on otettava käyttöön jossakin seuraavista Azure-alueista:

    - Itä-Yhdysvallat
    - Länsi-Yhdysvallat
    - Pohjois-EU
    - Länsi-EU

- Dynamics 365 Regulatory Configuration Services (RCS) -tilin on oltava käytettävissä.
- RCS-tilin globalisointiominaisuus on otettava käyttöön toiminnonhallinnan kautta. Lisätietoja: [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md).
- On luotava avainsäilö ja tallennustili Azuressa. Lisätietoja: [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a>Microservices-lisäosan asentaminen Lifecycle Servicesissa

1. Kirjaudu LCS-tilille.
2. Valitse **Esiversiotoiminnon hallinta** -ruutu.
3. Valitse **Julkisen esiversion ominaisuudet** -osasta **Sähköisen laskutuksen palvelu**.
4. Varmista, että **Esiversiotoiminto käytössä** -asetukseksi on valittu **Kyllä**.

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a>Määritä RCS-integroinnin parametrit sähköisen laskutuksen lisäosan avulla.

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
5. Syötä **LCS-ympäristötunnus**-kenttään LCS-tilaustilisi tunnus.
6. Valitse **Tallenna** ja sulje sitten sivu.

## <a name="create-key-vault-secret"></a>Luo avainsäilön salainen koodi

1. Kirjaudu RCS-tilille.
2. Valitse **Globalisointitoiminnot**-työtila ja **Ympäristö**-kohdan **Sähköinen laskutus** -ruutu.
3. Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Palveluympäristö** ja valitse sitten **Key Vault -parametrit**.
4. Valitse **Uusi**, jos haluat luoda avainsäilön salaisen koodin.
5. Syötä **Nimi**-kenttään avainsäilön salaisen koodin nimi. Syötä **Kuvaus**-kenttään kuvaus.
6. Liitä **Key Vault – URI** -kenttään Azure Key Vaultin salainen koodi.
7. Valitse **Tallenna**.

## <a name="create-storage-account-secret"></a>Luo tallennustilin salainen koodi

1. Valitse **Varmenteet**-osasta **Key Vault -parametrit** -sivulla **Lisää**.
2. Syötä **Nimi**-kenttään tallennustilin salaisen koodin nimi. Syötä **Kuvaus**-kenttään kuvaus.
3. Valitse **Tyyppi**-kentästä **Varmenne**.
4. Valitse **Tallenna** ja sulje sitten sivu.

## <a name="create-an-electronic-invoicing-add-on-environment"></a>Sähköisen laskutuksen lisäosaympäristön luonti

1. Kirjaudu RCS-tilille.
2. Valitse **Globalisointitoiminnot**-työtila ja **Ympäristö**-kohdan **Sähköinen laskutus** -ruutu.

## <a name="create-a-service-environment"></a>Palveluympäristön luominen

1. Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Palveluympäristö**.
2. Luo uusi palveluympäristö valitsemalla **Uusi**.
3. Syötä **Nimi**-kenttään sähköisen laskutuksen ympäristön nimi. Syötä **Kuvaus**-kenttään kuvaus.
4. Valitse **Tallennutilin SAS-tunnuksen salasana** -kentässä sen varmenteen nimi, jota on käytettävä tallennustiliin todentautumisessa.
5. Valitse **Käyttäjät**-osassa **Lisää**, kun haluat lisätä käyttäjän, joka voi lähettää sähköisiä laskuja ympäristön kautta sekä muodostaa yhteyden tallennustiliin.
6. Kirjoita **Käyttäjätunnus**-kenttään käyttäjän alias. Kirjoita **Sähköpostiosoite**-kenttään käyttäjän sähköpostiosoite.
7. Valitse **Tallenna**.
8. Jos maa-/aluekohtaiset laskut edellyttävät tiettyjen varmenteiden soveltamista digitaaliseen allekirjoitukseen, valitse toimintoruudusta **Key Vaultin parametrit** sitten **Varmenneketju** ja suorita seuraavat vaiheet:

    1. Valitse **Uusi**, jos haluat luoda varmenneketjun.
    2. Syötä **Nimi**-kenttään varmenneketjun nimi. Syötä **Kuvaus**-kenttään kuvaus.
    3. Lisää ketjuun varmenne valitsemalla **Varmenteet**-osasta **Lisää**.
    4. Voit muuttaa todistuksen sijaintia ketjussa **Ylös**- tai **Alas**-painikkeella.
    5. Valitse **Tallenna** ja sulje sitten sivu.
    6. Sulje sivu.
9. Julkaise ympäristö pilveen valitsemalla **Palveluympäristö**-sivun toimintoruudussa **Julkaise**. **Tila**-kentän arvoksi tulee **Julkaisu**.

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

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a>Sähköisen laskutuksen lisäosan integroinnin määrittäminen Financessa tai Supply Chain Managementissa

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Sähköisen laskutuksen lisäosan integrointitoiminnon käyttöönotto

1. Kirjaudu Finance- tai Supply Chain Management -esiintymään.
2. Etsi **Sähköisen laskutuksen lisäosan integrointi** -toimintoa **Toiminnonhallinta**-työtilassa. Jos tämä toiminto ei näy sivulla, valitse **Tarkista päivitykset**.
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

3. Syötä **Ympäristö**-kenttään sähköisen laskutuksen lisäosan ympäristön nimi.
4. Valitse **Tallenna** ja sulje sitten sivu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]