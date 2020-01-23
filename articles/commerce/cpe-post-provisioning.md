---
title: Commercen esikatseluympäristön määrittäminen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää Microsoft Dynamics 365 Commercen esikatseluympäristön, kun se on valmisteltu.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f19d03f3f2f5a9f6f7ba08b682277e4e3b764d10
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906136"
---
# <a name="configure-a-commerce-preview-environment"></a>Commercen esikatseluympäristön määrittäminen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää Microsoft Dynamics 365 Commercen esikatseluympäristön, kun se on valmisteltu.

## <a name="overview"></a>Yleiskatsaus

Suorita tämän ohjeaiheen toimet vasta, kun Commercen esikatseluympäristö on valmisteltu. Katso lisätietoja Commercen esikatseluympäristön valmistelusta kohdasta [Commercen esikatseluympäristön valmisteleminen](provisioning-guide.md).

Kun Commercen esikatseluympäristö on valmisteltu loppuun, lisävalmistelun jälkeiset määritysvaiheet on suoritettava, ennen kuin voit aloittaa ympäristön arvioinnin. Näiden vaiheiden suorittaminen edellyttää, että käytät Microsoft Dynamics Lifecycle Servicesiä (LCS), Dynamics 365 Commercea ja Dynamics 365 Retailis.

## <a name="before-you-start"></a>Ennen aloittamista

1. Kirjaudu [LSC-portaaliin](https://lcs.dynamics.com).
1. Siirry projektiisi.
1. Valitse päävalikosta **Pilvipalveluympäristöt**.
1. Valitse ympäristö luettelosta.
1. Valitse oikealla olevista ympäristön tiedoista **Täydet tiedot**.
1. Valitse **Kirjaudu sisään** avataksesi valikon ja valitse sitten **Kirjaudu ympäristöön**.
1. Varmista, että valittuna on **USRT**-yritys oikealla yläkulmassa.

## <a name="configure-the-point-of-sale-in-lcs"></a>Määritä myyntipiste LCS:ssä

### <a name="associate-a-worker-with-your-identity"></a>Työntekijän liittäminen tunnukseen

Voit liittää työntekijän identiteettisi LCS:iin noudattamalla seuraavia ohjeita.

1. Valitse vasemmalla olevasta valikosta **Moduulit \> Vähittäismyynti \> Työntekijät \> Työntekijät**.
1. Etsi ja valitse luettelosta seuraava tietue: **000713 - Andrew Collette**.
1. Valitse toimintoruudussa **Vähittäismyynti**.
1. Valitse **Liitä aiemmin luotu tunnus**.
1. Syötä **Sähköposti**-kenttään **Hae sähköpostiosoitteen avulla** -kohdan oikealla puolelle sähköpostiosoite.
1. Valitse **Haku**.
1. Valitse tietue, joka sisältää nimesi.
1. Valitse **OK**.
1. Valitse **Tallenna**.

### <a name="activate-cloud-pos"></a>Pilvipalvelun myyntipisteen aktivoiminen

Jos haluat aktivoida pilvimyyntipisteen LCS:ssä, toimi seuraavasti.

1. Valitse päävalikosta **Pilvipalveluympäristöt**.
1. Valitse ympäristö luettelosta.
1. Valitse oikealla olevista ympäristön tiedoista **Täydet tiedot**.
1. Avaa valikko valitsemalla **Kirjaudu** ja avaa sitten myyntipiste (POS) valitsemalla **Kirjaudu pilvimyyntipisteeseen**.
1. Valitse **Seuraava**.
1. Kirjaudu sisään käyttämällä Microsoft Azure Active Directory (Azure AD) -tiliäsi.
1. Valitse **Myymälän nimi** -kohdassa **San Francisco**.
1. Valitse **Seuraava**.
1. Valitse **Kassakone ja laite** -kohdassa **SANFRAN-1**.
1. Valitse **Aktivoi**. Olet kirjautunut ulos ja sinut on ohjattu POS-kirjautumissivulle.
1. Voit nyt kirjautua pilvimyyntipistekokemukseen käyttämällä operaattorin tunnusta **000713** ja salasanaa **123**.

## <a name="set-up-your-site-in-commerce"></a>Urasivuston määrittäminen Commercessa

Voit aloittaa esikatseluruudun määrittämisen Commerce-sivustossa noudattamalla seuraavia ohjeita.

1. Kirjaudu sivustonhallintatyökaluun käyttämällä URL-osoitetta, johon olet tehnyt huomautuksen verkkokaupan valmistelusta valmistelun aikana (katso [verkkokaupan alustaminen](provisioning-guide.md#initialize-e-commerce)).
1. Avaa sivuston asetusvalintaikkuna valitsemalla **Fabrikam**-sivusto.
1. Valitse verkkotunnus, jonka syötit sähköistä kaupankäyntiä alustettaessa.
1. Valitse **Fabrikamin laajennettu verkkokauppa** oletuskanavaksi. (Huomautus: Varmista, että valitset **laajennetun** verkkokaupan.)
1. Valitse **en-us** oletuskieleksi.
1. Jätä **polku** -kentän arvo sellaiseksi kuin se on.
1. Valitse **OK**. Sivuston sivuluettelo tulee näkyviin.

## <a name="enable-jobs-in-retail"></a>Ota projektit käyttöön Retailissa

Voit ottaa käyttöön työt Retailissa seuraavien vaiheiden avulla.

1. Kirjaudu sisään ympäristöön (pääkonttori).
1. Siirry vasemmalla olevan valikon avulla kohtaan **Retail \> Kyselyt ja raportit \> Erätyöt**.

    Tämän menettelyn jäljellä olevat vaiheet on täytettävä kunkin seuraavan työn osalta:

    * Vähittäismyyntitilauksen sähköposti-ilmoituksen käsittely
    * Tuotteen saatavuus
    * P-0001
    * Synkronoi tilaukset -työ

1. Hae työ pikasuodattimen avulla nimen perusteella.
1. Jos työn tila on **Pidätä**, seuraa näitä vaiheita:

    1. Valitse tietue.
    1. Valitse toimintoruudussa **Erätyö**-välilehdellä **Muuta tila**.
    1. Valitse **Odottaa** ja valitse sitten **OK**.

### <a name="run-full-data-synchronization-in-retail"></a>Suorita täydellinen tietojen synkronointi Retailissa

Jos haluat suorittaa täyden tietojen synkronoinnin Retailissa, toimi seuraavasti.

1. Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit \> Retail \> Headquarters-asetukset \> Retail-ajastus \> Kanavan tietokanta**.
1. Vasemmalla olevasta luettelosta valitaan **oletuskanava**. Valitse toinen käytettävissä oleva kanava. Tämä kanava on nimeltään **scXXXXXXXXX**.
1. Valitse toimintoruudusta **Tietojen täydellinen synkronointi**.
1. Syötä jakeluaikatauluksi **9999**.
1. Valitse **OK**.
1. Valitse **OK**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Luottokortin testitiedot testiostojen tekemistä varten

Voit käyttää seuraavia luottokortin testitietoja sivuston testitapahtumien suorittamisessa:

- **Kortin numero:** 4111-1111-1111-1111
- **Vanhentumispäivä:** 10/20
- **Kortin tarkistusnumero (CVV) -koodi:** 737

> [!IMPORTANT]
> Älä milloinkaan, missään tapauksessa yritä käyttää testisivustossa todellisia luottokortin tietoja.

## <a name="next-steps"></a>Seuraavat vaiheet

Kun valmistelu- ja konfigurointivaiheet on suoritettu, olet valmis arvioimaan esikatseluympäristön. Siirry sisällönluontikokemukseen Commercen sivustonhallintatyökalun URL-osoitteen avulla. Siirry Retail-asiakassivustokokemukseen Commercen sivuston URL-osoitteen avulla.

Jos haluat määrittää valinnaiset ominaisuudet Commercen esikatseluympäristöön, katso [Lisäominaisuuksien määrittäminen Commercen esikatseluympäristöä varten](cpe-optional-features.md).

## <a name="additional-resources"></a>Lisäresurssit

[Commercen esikatseluympäristön yleiskuvaus](cpe-overview.md)

[Commercen esikatseluympäristön valmisteleminen](provisioning-guide.md)

[Valinnaisten ominaisuuksien määrittäminen Commercen esikatseluympäristöä varten](cpe-optional-features.md)

[Commercen esikatseluympäristön usein kysytyt kysymykset](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure -portaali](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce -sivusto](https://aka.ms/Dynamics365CommerceWebsite)

[Dynamics 365 Retailin ohjeresurssit](../retail/index.md)