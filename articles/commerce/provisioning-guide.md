---
title: Dynamics 365 Commercen eristysympäristön valmistelu
description: Tässä artikkelissa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen eristysympäristön esittely- tai eristyskäyttöä varten valmiiden esittelytietojen avulla.
author: psimolin
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3ada30fc9d86d236b71d018ef77f2ae8573f2285
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013131"
---
# <a name="provision-a-dynamics-365-commerce-sandbox-environment"></a>Dynamics 365 Commercen eristysympäristön valmistelu

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen eristysympäristön esittelykäyttöä varten valmiiden esittelytietojen avulla. Tuotantoympäristön asetusprosessi on samanlainen, mutta työläämpi, sillä useat eristysympäristön edellytykset on jo määritetty esittelytiedoissa.

Ennen kuin aloitat, suosittelemme, että tarkistat tämän artikkelin nopeasti, jotta saat käsityksen prosessin vaatimista aiheista.

Määritä Commercen eristysympäristöä varten myöhemmin Commercen valmistelua varten parametreja ympäristölle ja Commerce Scale Unitille (CSU). Tämän artikkelin ohjeissa kuvataan kaikki vaiheet, joita tarvitaan valmisteluun, ja parametrit, joita on käytettävä.

Kun Commercen ympäristö on valmisteltu onnistuneesti, suoritetaan jotkin valmistelun jälkeiset vaiheet ympäristön valmistelemiseksi käyttöä varten. Jotkin vaiheet ovat valinnaisia. Tämä riippuu siitä, mitä järjestelmän alueita haluat käyttää. Voit aina suorittaa valinnaiset vaiheet myöhemmin.

Katso lisätietoja Commercen ympäristön määrittelystä kohdasta sen jälkeen, kun olet valmistellut sen [Commercen eristysympäristön määrittäminen](cpe-post-provisioning.md). Jos haluat lisätietoja valinnaisten ominaisuuksien määrittämisestä Commercen ympäristöön, katso [Lisäominaisuuksien määrittäminen Commercen eristysympäristöä varten](cpe-optional-features.md).

## <a name="prerequisites"></a>Edellytykset

Seuraavien edellytysten on oltava käytössä, ennen kuin voit määrittää Commercen ympäristön:

- Sinulla on Microsoft Dynamics Lifecycle Services -portaalin (LCS) käyttöoikeus
- Olet jo Microsoft Dynamics 365 -kumppani tai -asiakas, jolla on käyttöönottoprojekti jo luotuna ja käytettävissä LCS:ssä.  
- Olet luonut Azure Active Directory (Azure AD) -käyttöoikeusryhmän, jota voidaan käyttää sähköisen Commerce-järjestelmänvalvojaryhmänä, ja sinulla on ryhmän tunnus.
- Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää arvioiden ja arvosteluiden moderaattorien ryhmänä, ja sinulla on ryhmän tunnus. (Tämä suojausryhmä voi olla sama kuin Commerce-järjestelmänvalvojaryhmä.)
- Olet ottanut käyttöön pääkonttorin esiintymän LCS:ssä. Lisätietoja on kohdassa [Uuden ympäristön käyttöönottaminen](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).

Huomaa, että tämä luettelo ei ole täydellinen. Jos ongelmia esiintyy, ota yhteys Microsoft-kumppaniin.

## <a name="provision-your-commerce-environment"></a>Commercen ympäristön valmisteleminen

Seuraavissa ohjeissa kerrotaan, miten Commercen ympäristö valmistellaan. Kun olet suorittanut vaiheet onnistuneesti, Commercen ympäristö on valmis määritettäväksi. Kaikki alla kuvatut vaiheet tapahtuvat LCS-portaalissa.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Alusta Commerce Scale Unit (pilvi)

Alusta CSU seuraavien ohjeiden avulla.

1. Valitse ympäristö luettelosta LCS:ssä.
1. Valitse oikealla olevassa **YMPÄRISTÖT**-näkymässä **Täydet tiedot**. Näkyviin tulee ympäristön tietojen näkymä.
1. Valitse **Ympäristön hallinta** -osassa **YMPÄRISTÖN OMINAISUUDET** -kohdassa **Hallinta**.
1. Valitse **Commerce Scale Unitit** -välilehdestä **Alusta**. Näkyviin tulee **Lisää skaalausyksikkö** -näkymä.
1. Valitse **ALUE**-kentässä alue, joka on sama alue tai lähellä sitä aluetta, jossa ympäristö otettiin käyttöön.
1. Valitse uusin saatavilla oleva versio avattavasta **Versio**-luettelosta.
1. Valitse **Alusta**.
1. Varoitusikkunassa pyydetään vahvistamaan Commerce Scale Unit -alustus. Valitse **Kyllä**. CSU on nyt asetettu jonoon valmistelua varten.
1. Varmista ennen jatkamista, että CSU:si tila on **ONNISTUNUT**. Alustus kestää noin kahdesta viiteen tuntia.

Jos **Hallinta**-linkki ei ole ympäristön tietonäkymässä, ota yhteys Microsoftin yhteyshenkilöön.

### <a name="initialize-e-commerce"></a>Sähköisen kaupankäynnin alustaminen

Alusta Commerce seuraavien ohjeiden avulla.

1. Valitse **Sähköinen kaupankäynti** -välilehdessä **Asetukset**.
1. Anna **Sähköisen kaupankäynnin ympäristön nimi** -kenttään nimi. Ota huomioon, että tämä nimi näkyy joissakin sähköisen kaupankäynnin esiintymään vievissä URL-osoitteissa.
1. Valitse **Commerce Scale Unitin nimi** -kentässä CSU-luettelosta. (Luettelossa pitäisi olla vain yksi vaihtoehto.)

    **Sähköisen kaupankäynnin maantieteellinen alue** -kenttä täytetään automaattisesti.

1. Jatka valitsemalla **Seuraava**.
1. Kirjoita **Tuetut isäntänimet** -kenttään mikä tahansa kelvollinen toimialue, kuten `www.fabrikam.com`.
1. Anna **Järjestelmänvalvojan AAD-käyttöoikeusryhmä** -kentässä käytettävän käyttöoikeusryhmän nimen kaksi ensimmäistä kirjainta ja näytä sitten hakutulokset valitsemalla suurennuslasikuvake. Valitse luettelossa oikea käyttöoikeusryhmä.
1.  Anna **Luokitusten ja arvostelujen valvojan AAD-käyttöoikeusryhmä** -kentässä käytettävän käyttöoikeusryhmän nimen kaksi ensimmäistä kirjainta ja näytä sitten hakutulokset valitsemalla suurennuslasikuvake. Valitse luettelossa oikea käyttöoikeusryhmä.
1. Jätä **Ota luokitukset ja arvostelupalvelu käyttöön** -asetuksen arvoksi **Kyllä**.
1. Valitse **Alusta**. **Commercen hallinta** -näkymä tulee uudelleen näkyviin, kun **e-Commerce**-välilehti on valittuna. Sähköisen kaupankäynnin alustaminen on aloitettu.
1. Ennen kuin jatkat, odota, kunnes Commercen alustamisen tila on **ALUSTAMINEN ONNISTUI**.
1. Merkitse oikeassa alakulmassa olevassa **Linkit**-kohdassa seuraavien linkkien URL-osoitteet:

    * **Sähköisen kaupankäynnin sivusto** – linkki verkkokaupan sivustosi juureen.
    * **Commerce-sivuston luontiohjelma** – linkki sivuston hallintatyökaluun.

## <a name="next-steps"></a>Seuraavat vaiheet

Jatkaaksesi käyttöönotto- ja määritysprosessia Commercen ympäristön määrittelystä, katso [Commercen eristysympäristön määrittäminen](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Commercen eristysympäristön määrittäminen](cpe-post-provisioning.md)

[BOPIS:n määritykset Dynamics 365 Commercen eristysympäristössä](cpe-bopis.md)

[Valinnaisten ominaisuuksien määrittäminen Dynamics 365 Commercen eristysympäristöä varten](cpe-optional-features.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (pilvi)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure -portaali](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce -sivusto](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
