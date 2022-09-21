---
title: IoT-ratkaisun käyttöönotto Azuressa
description: Sensor Data Intelligence käyttää Microsoft Azureen liitettyjen tunnistimien tietoja. Tässä artikkelissa kerrotaan, miten esineiden internet (IoT) -ratkaisu otetaan käyttöön Azure-tilauksessa.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreAzureResourceDeploymentWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 284aba91aa436ed1dfc02b5a93b4358ffc518017
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428390"
---
# <a name="deploy-an-iot-solution-on-azure"></a>IoT-ratkaisun käyttöönotto Azuressa

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Sensor Data Intelligence käyttää Microsoft Azureen liitettyjen tunnistimien tietoja. Jos haluat ottaa käyttöön Azuren noutaaksesi tietoja tunnistimista ja jakaaksesi ne Dynamics 365 Supply Chain Managementissa, ota käyttöön esineiden internet (IoT) -ratkaisu Azure-tilauksessa. Seuraavassa arkkitehtuurin kaaviossa on ratkaisun ja sen komponenttien yleiskatsaus.

![Sensor Data Intelligencen arkkitehtuurin kaavio.](media/sdi-architecture.png "Sensor Data Intelligencen arkkitehtuurin kaavio")

Alla olevien vaiheiden avulla voit ottaa käyttöön vaaditut resurssit Azuressa.

1. Kirjaudu sisään Supply Chain Managementiin järjestelmänvalvojana.
1. Siirry kohtaan **Järjestelmän hallinta \> Asetukset \> Sensor Data Intelligence \> Ota käyttöön Azure-resurssit ja muodosta niihin yhteys**, jos haluat avata ohjatun käyttöönottotoiminnon.
1. Lue **tervetulosivun** tiedot ja valitse **Seuraava**.
1. Lue **IoT-malliratkaisun ottaminen käyttöön Azuressa** -sivun tiedot ja valitse **Ohjeet**-osassa **Ota käyttöön**.
1. Uusi selainvälilehti avautuu, ja siirryt Azure-portaaliin, jossa voit ottaa käyttöön Azure-resursseja. Jos näyttöön tulee kehote, kirjaudu sisään Azure-tilauksen valtuustietoja.
1. Valitse **Mukautettu käyttöönotto** -sivun **Tilaus**-kentässä oma tilauksesi.
1. Valitse **Resurssiryhmä**-kentässä **Luo uusi**, jos haluat luoda resurssiryhmän käyttöönotettaville Azure-komponenteille.
1. Syötä näkyviin tulevan avattavan valintaikkunan **Nimi**-kenttään uuden resurssiryhmän nimi (esimerkiksi *IoT-esittely*). Valitse sitten **OK**.
1. Määritä seuraavat kentät:

    - **Resurssiryhmä** – Valitse juuri luotu resurssiryhmä.
    - **Alue** – Valitse alue mielellään alueelta, jossa Supply Chain Management environment on otettu käyttöön. Muista, että Azure-alueilla on erilainen hinnoittelu. Voit tarkastella alueen arvioituja kustannuksia käyttämällä [Sensor Data Intelligencen hintalaskinta](https://azure.com/e/c36c4947ebff4215b2e62590c2a24c68).
    - **Supply Chain Management -ympäristön URL-osoite** – Syötä Supply Chain Management -ympäristön URL-osoite.
    - **Käytä uudelleen olemassa olevaa Azure IoT -keskitintä** – Jätä tämä valintaruutu tyhjäksi.

1. Valitse **Seuraava: Tarkista ja luo**.
1. Varmista **Mukautettu käyttöönotto** -sivulla, että vahvistus on tehty, ja valitse sitten **Luo**.
1. **Käyttöönotto on käynnissä** -sivu seuraa käyttöönoton edistymistä. Käyttöönottoprosessi voi kestää 30 minuuttia. Kun **Käyttöönotto on käynnissä** -sivu osoittaa käyttöönoton olevan valmis, valitse resurssiryhmän nimen linkki. Näyttöön avautuu ryhmässä käytössä olevien resurssien luettelo.
1. Etsi resurssiluettelossa tietue, jonka **Tyyppi**-kentän arvoksi on määritetty *Hallinnoitu identiteetti*. Valitse **Nimi**-sarakkeessa nimi, jotta resurssin tietosivu avautuu.
1. Kopioi arvo **Asiakasohjelman tunnus** -kenttään (esimerkiksi valitsemalla **Kopioi leikepöydälle** -painike).
1. Siirry takaisin selainvälilehteen, jossa Supply Chain Management on käynnissä, *mutta älä sulje Azure-portaalin välilehteä*. Ohjatun **Ota käyttöön IoT-malliratkaisu Azuressa** -toiminnon sivun tulisi yhä olla auki. 
1. Valitse **Seuraava**.
1. Liitä **Azure-resurssien yhdistäminen** -sivun **Azure AD -sovelluksen asiakasohjelman tunnus** -kenttään kopioitu **Asiakasohjelman tunnus** -arvo.
1. Siirry takaisin selainvälilehteen, jossa Azure-portaali on auki, *mutta älä sulje Supply Chain Managementin välilehteä*. Resurssin tietosivu tulisi yhä olla auki.
1. Valitse selaimen **Takaisin**-painike, jos haluat palata uuden resurssiryhmän resurssiluetteloon.
1. Etsi resurssiluettelossa tietue, jonka **Tyyppi**-kentän arvoksi on määritetty *Azuren Redis-välimuisti*. Valitse **Nimi**-sarakkeessa nimi, jotta resurssin tietosivu avautuu.
1. Valitse vasemmassa siirtymisruudussa **Käyttöoikeusavaimet**.
1. Kopioi **Käyttöoikeusavaimet**-sivulla **Ensisijainen yhteysmerkkijono (StackExchange.Redis)** -kohdan arvo (esimerkiksi valitsemalla **Kopioi leikepöydälle** -painike).
1. Siirry takaisin selainvälilehteen, jossa Supply Chain Management on käynnissä. **Azure-resurssien yhdistäminen** -sivun tulisi yhä olla auki.
1. Liitä **Redis-mittarin säilön yhteysmerkkijono** -kenttään kopioitu **Ensisijainen yhteysmerkkijono (StackExchange.Redis)** -kohdan arvo.
1. Valitse **Valmis**.

Sensor Data Intelligencen Azure-resurssit on nyt otettu käyttöön Azure-tilauksessa.

> [!NOTE]
> Voit tarkastella milloin tahansa Supply Chain Managementiin tallennettuja yhteystietoja tai muokata niitä avaamalla **Sensor Data Intelligencen parametrit** -sivun. Lisätietoja on kohdassa [Sensor Data Intelligencen parametrit](sdi-parameters.md).
