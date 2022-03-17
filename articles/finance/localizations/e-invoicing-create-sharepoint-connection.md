---
title: SharePoint-yhteyden konfiguroiminen
description: Tässä aiheessa kuvataan yhteyden konfiguroimista siten, että sähköinen laskutus voi käyttää Microsoft SharePoint -sivustoa.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6b9fffc1f3525e69792517dd1c6ebdcfbe5a74d2
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371596"
---
# <a name="configure-a-sharepoint-connection"></a>SharePoint-yhteyden konfiguroiminen

[!include [banner](../includes/banner.md)]

Sähköinen laskutuspalvelu voi lukea tiedostoja Microsoft SharePoint -kansioista ja ladata tiedostoja SharePointiin. Jotta varmistetaan, että sähköinen laskutus voi käyttää tiettyä SharePoint-sivustoa, sinun on annettava sivuston tunnistetiedot sähköiselle laskutuspalvelulle. Voit myös varmistaa, että tunnistetiedot on tallennettu suojatusti, kun niitä ei anneta suoraan. Tallenna sen sijaan ne Azure Key Vaultiin ja määritä Azure Key Vaultin salainen koodi.

## <a name="grant-access-to-a-sharepoint-folder"></a>SharePoint-kansion käyttöoikeuden myöntäminen

1. Luo sovellusrekisteröinti vuokraajassa, johon Regulatory Configuration Service (RCS) on asennettu.

    1. Kirjaudu [Azure-portaalin osoitteessa](https://portal.azure.com/).
    2. Siirry kohtaan **Sovellusrekisteröinnit**.
    3. Valitse **Uusi rekisteröinti**.
    4. Kirjoita nimi, esimerkiksi **SharePoint-sovellus sähköiseen laskutukseen** ja suorita rekisteröinti loppuun.
    5. Valitse uusi sovellusrekisteröinti.
    6. Ota **Todennus**-välilehdessä käyttöön **Salli julkisen asiakkaan työnkulut** -vaihtoehto.
    4. Valitse **Varmenteet ja salaiset koodit** -välilehdessä **Uusi asiakasohjelman salaisuus** luodaksesi asiakasohjelman salaisuuden.
    5. Kopioi luodun salaisen koodin arvo.

    Noudata seuraavasti ohjeita:

    - Älä käytä samaa sovelluksen rekisteröintiä eri palveluissa.
    - Noudata [salasanakäytännön suosituksia](/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide).
    - Määritä salasanojen kierto. Luo kierron aikana sovellusrekisteröinnille uusi asiakasohjelman salaisuus, päivitä avainsäilö ja poista sitten vanha salaisuus.

2. Tallenna **Sovellusrekisteröinnin salaisuus**- ja **Sovelluksen (asiakasohjelman) tunnus** -arvot kahtena uutena salaisuutena sähköisen laskutusympäristön asetuksiin.
3. Lisää luomasi salaisuudet Key Vault -parametreihin sähköisen laskutusympäristön määrityksiin RCS:ssä.
4. Myönnä Azure-portaalissa SharePoint-käyttöoikeus. Vuokraajan järjestelmänvalvojan on suoritettava tämä vaihe.

    1. Valitse luomasi sovellusrekisteröinti.
    2. Valitse **API-käyttöoikeudet**-välilehdestä **Lisää käyttöoikeus**.
    3. Valitse **Microsoft Graph (sovellusoikeudet)**\>**Sites.Selected**.
    4. Valitse **Myönnä järjestelmänvalvojan suostumus käyttäjälle \<user&nbsp;name\>**.
    5. Tarkista **Tila**-kenttä ja varmista, että käyttöoikeudet on myönnetty.

        ![API-käyttöoikeudet-välilehdessä myönnetyt käyttöoikeudet.](media/configured-permissions.jpg)

    6. Avaa [Graph Explorer – Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer) ja kirjaudu sisään.
    7. Valitse vasemmanpuoleisen ruudun **Mallikyselyt**-välilehden **SharePoint-sivustot**-kohdasta **Hae SharePoint-sivusto sivuston suhteellisen polun perusteella**.
    8. Täytä **\{isäntänimi\}**- ja **\{palvelimen suhteellinen polku\}** -parametrit. Kirjoita esimerkiksi `<domain>.sharepoint.com` kohdassa **\{isäntänimi\}** ja `sites/<siteName>` kohdassa **\{palvelimen suhteellinen polku\}**.

        > [!NOTE]
        > Jätä **\{palvelimen suhteellinen polku\}** -parametri tyhjäksi oletussivustolle.

    9. Valitse **Suorita kysely** ja tallenna tulos.
    10. Konfiguroi seuraava kysely.

        `POST https://graph.microsoft.com/v1.0/sites/{site-id}/permissions`

        Tässä kyselyssä **\{sivuston tunnus\}** on edellisen kyselyn vastauksen **tunnus**-solmun arvo.

        Tässä on pyynnön runko.

        ```json
        {
            "roles": [
                "read",
                "write"
            ],
            "grantedToIdentities": [
                {
                    "application": {
                        "id": "{app-id}",
                        "displayName": "{app-name}"
                    }
                }
            ]
        }
        ```

        Tässä pyyntöosassa **\{sovellustunnus\}** on **Sovelluksen (asiakasohjelman) tunnus** -arvo ja **\{sovelluksen nimi\}** on **Sovelluksen nimi** -arvo.

        ![POST-kysely.](media/app-id-query.jpg)

    11. Valitse **Muokkaa käyttöoikeuksia** -välilehdessä **Avaa käyttöoikeuspaneeli** ja valitse sitten **Sivustot** \> **Sites.FullControl.All** \> **Suostumus**.
    12. Valitse **Suorita kysely**.

Sähköisellä laskutuspalvelulla on nyt SharePoint-sivuston käyttöoikeus.
