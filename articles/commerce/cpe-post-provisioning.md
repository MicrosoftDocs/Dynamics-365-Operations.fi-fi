---
title: Dynamics 365 Commerce -arviointiympäristön määritykset
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää Microsoft Dynamics 365 Commercen arviointiympäristön, kun se on valmisteltu.
author: psimolin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9738700ca495d54c91ad91aa9c5a3d32c95a5a5
ms.sourcegitcommit: 4a973ac0e7af0176270a8070a96a52293567dfbf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/13/2022
ms.locfileid: "8747634"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>Dynamics 365 Commerce -arviointiympäristön määritykset

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää Microsoft Dynamics 365 Commercen arviointiympäristön, kun se on valmisteltu.

Suorita tämän ohjeaiheen toimet vasta, kun Commercen arviointiympäristö on valmisteltu. Lisätietoja Commercen arviointiympäristön valmistelusta on kohdasta [Commercen arviointiympäristön valmisteleminen](provisioning-guide.md).

Kun Commercen arviointiympäristö on valmisteltu kokonaisuudessaan, valmistelun jälkeiset lisämääritysvaiheet on suoritettava, ennen kuin voit aloittaa ympäristön arvioinnin. Näiden vaiheiden suorittaminen edellyttää, että käytössä ovat Microsoft Dynamics Lifecycle Services (LCS) ja Dynamics 365 Commerce.

## <a name="before-you-start"></a>Ennen aloittamista

1. Kirjaudu [LSC-portaaliin](https://lcs.dynamics.com).
1. Siirry projektiisi.
1. Valitse päävalikosta **Pilvipalveluympäristöt**.
1. Valitse ympäristö luettelosta.
1. Valitse oikealla ympäristön tiedoista **Kirjaudu ympäristöön**. Siirryt Commercen pääkonttorisovellukseen.
1. Varmista, että valittuna on **USRT**-yritys oikealla yläkulmassa.
1. Siirry kohtaan **Commerce-parametrit \> Määritysparametrit** ja varmista, että **ProductSearch.UseAzureSearch**-merkinnän arvo on **tosi**. Jos tämä merkintä puuttuu, voit lisätä tämän merkinnän, määrittää arvoksi **tosi** ja valita **Kanavatietokanta \> Täydellinen tiedon synkronointi** eCommerce-sivustoon liittyvälle Commerce Scale Unitille.
1. Siirry kohtaan **Retail ja Commerce \> Headquarters-asetukset \> Commerce-ajastus \> Alusta Commerce-ajastus**. Määritä **Alusta Commerce-ajoitustoiminto** -tietoikkunassa **Poista olemassa oleva määritys** -vaihtoehdon arvoksi **Kyllä**. Valitse sitten **OK**.
1. Jos haluat lisätä kanavia Commerce Scale Unit -yksikköön, valitse **Retail ja Commerce \> Pääkonttorin asetukset \> Commerce-ajastus \>Kanavatietokanta** ja valitse sitten Commerce Scale Unit -yksikkö vasemmanpuoleisesta ruudusta. Lisää **Vähittäismyyntikanava**-pikavälilehdellä **AW-verkkomyymälä**-, **AW Business -verkkomyymälä**- ja **Laajennettu Fabrikam-verkkomyymälä** -kanavat. Vaihtoehtoisesti voit myös lisätä vähittäismyyntiliikkeitä, jos käytät myyntipistettä (esimerkiksi **Seattlea**, **San Franciscoa** tai **San Joseta**).

Varmista Commercen pääkonttorissa tehtävien valmistelun jälkeisten toimintojen aikana, että **USRT**-yritys on koko ajan valittuna.

## <a name="configure-the-point-of-sale"></a>Myyntipisteen määrittäminen

### <a name="associate-a-worker-with-your-identity"></a>Työntekijän liittäminen tunnukseen

Voit liittää työntekijän käyttäjätietoihin seuraavien ohjeiden avulla Commercen pääkonttorissa.

1. Valitse vasemmalla olevasta valikosta **Moduulit \> Vähittäismyynti ja kauppa \> Työntekijät \> Työntekijät**.
1. Etsi ja valitse luettelosta seuraava tietue: **000713 - Andrew Collette**.
1. Valitse toimintoruudussa **Commerce**.
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
1. Valitse oikealla ympäristön tiedoista **Kirjaudu pilvimyyntipisteeseen**.
1. Avaa **Ennen aloittamista** -valintaikkunassa **Seuraava**.
1. Älä tee muutoksia **Palvelimen URL-osoite** -kenttään. Valitse **Seuraava**.
1. Kirjaudu sisään käyttämällä Microsoft Azure Active Directory (Azure AD) -tiliäsi.
1. Valitse **Myymälän nimi** -kentässä **San Francisco** ja valitse sitten **Seuraava**.
1. Valitse **Kassakone ja laite** -kohdassa **SANFRAN-1**.
1. Valitse **Aktivoi**. Olet kirjautunut ulos ja sinut on ohjattu POS-kirjautumissivulle.
1. Voit nyt kirjautua pilvimyyntipistekokemukseen käyttämällä operaattorin tunnusta **000713** ja salasanaa **123**.

## <a name="set-up-your-site-in-commerce"></a>Urasivuston määrittäminen Commercessa

Voit aloittaa arviointisivuston määrittämisen Commercessa noudattamalla seuraavia ohjeita.

1. Kirjaudu sivustonmuodostimeen käyttämällä URL-osoitetta, josta kirjoitit muistiin sähköisen kaupankäyntiä alustettaessa valmistelun aikana (katso [Sähköisen kaupankäynnin alustaminen](provisioning-guide.md#initialize-e-commerce)).
1. Avaa sivuston asetusvalintaikkuna valitsemalla **Fabrikam**-sivusto.
1. Valitse verkkotunnus, jonka syötit sähköistä kaupankäyntiä alustettaessa.
1. Valitse **Fabrikamin laajennettu verkkokauppa** oletuskanavaksi. (Huomautus: Varmista, että valitset **laajennetun** verkkokaupan.)
1. Valitse **en-us** oletuskieleksi.
1. Jätä **polku** -kentän arvo sellaiseksi kuin se on.
1. Valitse **OK**. Sivuston sivuluettelo tulee näkyviin.
1. Toista vaiheet 2-7 **AdventureWorks**-sivustossa (joka yhdistää **AW-verkkokauppa**-kanavaan) ja **AdventureWorks Business**-sivustoon (joka yhdistää **AW Business -verkkokauppa** -kanavaan). Jos **Polku**-kenttä on tyhjä Fabrikam-sivustossa, sinun on lisättävä polut kahteen AdventureWorks -sivustoon (esim. "aw" ja "awbusiness").

## <a name="enable-jobs"></a>Töiden ottaminen käyttöön

Voit ottaa käyttöön työt Commercessa seuraavien vaiheiden avulla.

1. Kirjaudu sisään ympäristöön (pääkonttori).
1. Siirry vasemmalla olevan valikon avulla kohtaan **Vähittäismyynti ja kauppa \> Kyselyt ja raportit \> Erätyöt**.

    Tämän menettelyn jäljellä olevat vaiheet on täytettävä kunkin seuraavan työn osalta:

    * Vähittäismyyntitilauksen sähköposti-ilmoituksen käsittely
    * Tuotteen saatavuus
    * P-0001
    * Synkronoi tilaukset -työ

1. Hae työ pikasuodattimen avulla nimen perusteella.
1. Jos työn tila on **Suoritetaan**, toimi seuraavasti:

    1. Valitse tietue.
    1. Valitse toimintoruudussa **Erätyö**-välilehdellä **Muuta tila**.
    1. Valitse ensin **Peruuttaminen** ja sitten **OK**.

1. Jos työn tila on **Pidätetty**, seuraa näitä vaiheita:

    1. Valitse tietue.
    1. Valitse toimintoruudussa **Erätyö**-välilehdellä **Muuta tila**.
    1. Valitse **Odottaa** ja valitse sitten **OK**.

Vaihtoehtoisesti voit määrittää toistuvuusvälin yhteen (1) minuuttiin seuraavissa töissä:

* Vähittäismyyntitilauksen sähköposti-ilmoitustyön käsittely
* P-0001 työ
* Synkronoi tilaukset -työ

### <a name="run-full-data-synchronization"></a>Suorita täydellinen tietojen synkronointi

Suorita täydellinen tietojen synkronointi Commercessa, toimi seuraavasti Commercen pääkonttorissa.

1. Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Headquarters-asetukset \> Commerce-ajastus \> Kanavan tietokanta**.
1. Valitse kanava, jonka nimi on **scXXXXXXXXX**.
1. Valitse toimintoruudusta **Tietojen täydellinen synkronointi**.
1. Syötä jakeluaikatauluksi **9999**.
1. Valitse **OK**.
1. Valitse **OK**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Luottokortin testitiedot testiostojen tekemistä varten

Voit käyttää seuraavia luottokortin testitietoja sivuston testitapahtumien suorittamisessa:

- **Kortin numero:** 4111-1111-1111-1111
- **Vanhentumispäivä:** 10/30
- **Kortin tarkistusnumero (CVV) -koodi:** 737

> [!IMPORTANT]
> Älä milloinkaan, missään tapauksessa yritä käyttää testisivustossa todellisia luottokortin tietoja.

## <a name="next-steps"></a>Seuraavat vaiheet

Kun valmistelu- ja määritysvaiheet on suoritettu, voit aloittaa arviointiympäristön käytön. Siirry sisällönluontikokemukseen Commercen sivustonmuodostimen URL-osoitteen avulla. Siirry vähittäismyynnin asiakassivustokokemukseen Commercen sivuston URL-osoitteen avulla.

Lisätietoja Commercen arviointiympäristön valinnaisten ominaisuuksien määrittämisestä on kohdassa [Commercen arviointiympäristön valinnaisten ominaisuuksien määrittäminen](cpe-optional-features.md).

> [!NOTE]
> Commerce-arviointiympäristöihin ladattu valmiiksi Azure Active Directory (Azure AD) kuluttajakauppavuokraaja esittelyä varten. Arviointiympäristöissä ei tarvitse määrittää omaa Azure AD -kuluttajakauppavuokraajaa. Jos arviointiympäristö kuitenkin määritetään käyttämään omaa Azure AD -kuluttajakauppavuokraajaa, ``https://login.commerce.dynamics.com/_msdyn365/authresp`` on muistettava lisätä Azure AD -kuluttajakauppasovellukseen URL-vastausosoitteena Azure-portaalin kautta.

## <a name="troubleshooting"></a>Vianmääritys

### <a name="site-builder-channel-list-is-empty-when-configuring-site"></a>Sivustonmuodostimen kanavaluettelo on tyhjä, kun sivustoa konfiguroitaan

Jos sivustonmuodostin ei näytä verkkomyymälän kanavia, varmista pääkonttorissa, että kanavat on lisätty Commerce Scale Unit -yksikköön edellä olevassa [Ennen aloittamista](#before-you-start) -osassa kuvatulla tavalla. Suorita myös **Alusta Commerce-ajastus** siten, että **Poista olemassa oleva määritys** -kohdan arvona on **Kyllä**.  Kun nämä vaiheet on suoritettu, suorita **Kanavatietokanta**-sivulla (**Retail ja Commerce \> Pääkonttorin asetukset \> Commerce-ajastus \> Kanavatietokanta**) **9999**-työ Commerce Scale Unitissa.

### <a name="color-swatches-are-not-rendering-on-the-category-page-but-are-rendering-on-the-product-details-page-pdp-page"></a>Väriruudut eivät hahmonnu luokkasivulla, mutta ne hahmontuvat tuotetietosivulla.

Noudattamalla näitä ohjeita voit varmistaa, että väri- ja kokoruudut määritetään tarkennettaviksi.

1. Pääkonttorissa valitse **Retail ja Commerce \> Kanavan asetukset \> Kanavaluokat ja tuotemääritteet**.
1. Valitse vasemmanpuoleisesta ruudusta verkkomyymälän kanava ja valitse sitten **Määritä määritteen metatiedot**.
1. Määritä kohdan **Näytä määrite kanavassa** asetukseksi **Kyllä**, määritä kohdan **Voidaan tarkentaa** -asetukseksi **Kyllä** ja valitse sitten **Tallenna**. 
1. Palaa verkkomyymälän kanavasivulle ja valitse sitten **Julkaise kanavan päivitykset**.
1. Valitse **Retail ja Commerce \> Pääkonttorin asetukset \> Commerce-ajastus \> Kanavatietokanta** ja suorita **9999**-työ Commerce Scale Unitissa.

### <a name="business-features-dont-appear-to-be-turned-on-for-the-adventureworks-business-site"></a>Liiketoimintatoiminnot eivät näytä olevan käytössä liiketoimintasivustoa AdventureWorks varten

Varmista pääkonttorissa, että verkkomyymälän kanava on määritetty niin, että **Asiakastyyppinä** on **B2B**. Jos **asiakastyypiksi** on määritetty **B2C**, on luotava uusi kanava, sillä aiemmin luotua kanavaa ei voi muokata. 

Commerce-version 10.0.26 ja sitä aiemmin toimitetuissa versioissa **AW Business -verkkomyymälän** kanava on määritetty väärin. Voit luoda uuden kanavan, jolla on samat asetukset ja konfiguraatiot, lukuun ottamatta **asiakastyyppiä**, jonka on oltava **B2B**.

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Commerce -arviointiympäristön yleiskuvaus](cpe-overview.md)

[Dynamics 365 Commerce -arviointiympäristön valmisteleminen](provisioning-guide.md)

[Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset](cpe-optional-features.md)

[BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä](cpe-bopis.md)

[Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure -portaali](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce -sivusto](https://aka.ms/Dynamics365CommerceWebsite)

[Kuluttajakaupan vuokraajan määrittäminen Commercessa](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
