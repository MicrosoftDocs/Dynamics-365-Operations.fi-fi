---
title: Dynamics 365 Commercen eristysympäristön määrittäminen
description: Tässä artikkelissa kerrotaan, kuinka voit määrittää Microsoft Dynamics 365 Commercen eristysympäristön, kun se on valmisteltu.
author: psimolin
ms.date: 06/14/2022
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
ms.openlocfilehash: 259a580981003f135e234f66e9e93ceb18605412
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013106"
---
# <a name="configure-a-dynamics-365-commerce-sandbox-environment"></a>Dynamics 365 Commercen eristysympäristön määrittäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, kuinka voit määrittää Microsoft Dynamics 365 Commercen eristysympäristön, kun se on valmisteltu.

Suorita tämän artikkelin toimet vasta, kun Commercen eristysympäristö on valmisteltu. Katso lisätietoja Commercen eristysympäristön valmistelusta kohdasta [Commercen eristysympäristön valmisteleminen](provisioning-guide.md).

Kun Commercen eristysympäristö on valmisteltu loppuun, lisävalmistelun jälkeiset määritysvaiheet on suoritettava, ennen kuin voit aloittaa ympäristön käytön. Näiden vaiheiden suorittaminen edellyttää, että käytössä ovat Microsoft Dynamics Lifecycle Services (LCS) ja Dynamics 365 Commerce.

## <a name="before-you-start"></a>Ennen aloittamista

1. Kirjaudu [LSC-portaaliin](https://lcs.dynamics.com).
1. Siirry projektiisi.
1. Valitse ympäristö luettelosta.
1. Valitse oikealla ympäristön tiedoista **Kirjaudu ympäristöön**. Siirryt Commercen pääkonttorisovellukseen.
1. Varmista, että valittuna on **USRT**-yritys oikealla yläkulmassa. Tämä yritys on määritetty ennalta esittelytiedoissa.
1. Siirry kohtaan **Commerce-parametrit \> Määritysparametrit** ja varmista, että **ProductSearch.UseAzureSearch**-merkinnän arvo on **tosi**. Jos tämä merkintä puuttuu, lisää se ja määritä arvoksi **tosi**.
1. Siirry kohtaan **Retail ja Commerce \> Headquarters-asetukset \> Commerce-ajastus \> Alusta Commerce-ajastus**. Määritä **Alusta Commerce-ajoitustoiminto** -tietoikkunassa **Poista olemassa oleva määritys** -vaihtoehdon arvoksi **Kyllä**. Valitse sitten **OK**.
1. Jotta myymälän ja sähköisen kaupankäynnin kanavat toimivat oikein, ne on lisättävä Commerce Scale Unitiin. Valitse **Vähittäismyynti ja kaupankäynti \> Pääkonttorin asetukset \> Commerce-ajastus \> Kanavatietokanta** ja valitse sitten vasemmanpuoleisessa ruudussa Commerce Scale Unit. Lisää **Vähittäismyyntikanava**-pikavälilehdellä **AW-verkkomyymälä**-, **AW Business -verkkomyymälä**- ja **Laajennettu Fabrikam-verkkomyymälä** -kanavat, jos haluat käyttää näitä sähköisen kaupankäynnin kanavia. Vaihtoehtoisesti voit myös lisätä vähittäismyyntiliikkeitä, jos käytät myyntipistettä (esimerkiksi **Seattlea**, **San Franciscoa** ja/tai **San Joseta**).
1. Varmista, että kaikki muutokset on synkronoitu kanavatietokannan kanssa, valitsemalla Commerce Scale Unitille **Kanavatietokanta \> Tietojen täydellinen synkronointi**.

Varmista Commercen pääkonttorissa tehtävien valmistelun jälkeisten toimintojen aikana, että **USRT**-yritys on koko ajan valittuna.

## <a name="configure-the-point-of-sale"></a>Myyntipisteen määrittäminen

### <a name="associate-a-worker-with-your-identity"></a>Työntekijän liittäminen tunnukseen

Voit liittää työntekijän käyttäjätietoihin seuraavien ohjeiden avulla Commercen pääkonttorissa.

1. Valitse vasemmalla olevasta valikosta **Moduulit \> Vähittäismyynti ja kauppa \> Työntekijät \> Työntekijät**.
1. Etsi ja valitse luettelosta seuraava tietue: **000713 - Andrew Collette**. Tässä esimerkissä käyttäjä on liitetty seuraavassa osassa käytettävään San Franciscon myymälään.
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

## <a name="set-up-your-e-commerce-sites"></a>Sähköisen kaupankäynnin sivustojen määrittäminen

Seuraavat kolme sähköisen kaupankäynnin esittelysivustoa ovat käytettävissä: Fabrikam, Adventure Works ja Adventure Works Business. Voit määrittää kunkin esittelysivuston alla olevien ohjeiden avulla.

1. Kirjaudu sivustonmuodostimeen käyttämällä URL-osoitetta, josta kirjoitit muistiin sähköisen kaupankäyntiä alustettaessa valmistelun aikana (katso [Sähköisen kaupankäynnin alustaminen](provisioning-guide.md#initialize-e-commerce)).
1. Valitse sivusto (**Fabrikam**, **Adventure Works** tai **Adventure Works Business**) ja avaa sivuston asetusvalintaikkuna.
1. Valitse verkkotunnus, jonka syötit Commerce alustamisen yhteydessä.
1. Valitse pääkonttorissa esimääritetty verkkokauppakanava (**Fabrikamin laajennettu verkkokauppa**, **AW-verkkomyymälä** tai **AW Business -verkkomyymälä**), joka vastaa oletuskanavaa.
1. Valitse **en-us** oletuskieleksi.
1. Määritä polun kentät. Kentän voi jättää tyhjäksi yhden sivuston kohdalla, mutta sille tulee määrittää arvo, jos käytössä on sama toimialueen nimi useissa sivustoissa. Jos toimialueen nimi on esimerkiksi `https://www.constoso.com`, voit käyttää Fabrikamille tyhjää polkua (`https://contoso.com`), Adventure Worksille aw-päätettä (`https://contoso.com/aw`) ja Adventure Works -liiketoimintasivustolle awbusiness-päätettä (`https://contoso.com/awbusiness`).
1. Valitse **OK**. Sivuston sivuluettelo tulee näkyviin.
1. Vaihtoehtoisesti voit toistaa vaiheet 2–7 ja määrittää muita esittelysivustoja tarvittaessa.

## <a name="enable-jobs"></a>Töiden ottaminen käyttöön

Voit ottaa käyttöön työt Commercessa seuraavien vaiheiden avulla.

1. Kirjaudu headquarters-ympäristöön.
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

Kun valmistelu- ja määritysvaiheet on suoritettu, voit aloittaa eristysympäristön käytön. Siirry sisällönluontikokemukseen Commercen sivustonmuodostimen URL-osoitteen avulla. Siirry vähittäismyynnin asiakassivustokokemukseen Commercen sivuston URL-osoitteen avulla.

Jos haluat määrittää valinnaiset ominaisuudet Commercen eristysympäristöön, katso [Lisäominaisuuksien määrittäminen Commercen eristysympäristöä varten](cpe-optional-features.md).

Jos haluat ottaa käyttöön sähköisen kaupankäynnin käyttäjien sisäänkirjauksen sähköisen kaupankäynnin sivustoon, ota käyttöön sivuston todennus Azure Active Directoryn kuluttajakaupan avulla tekemällä lisämäärityksiä. Lisätietoja on kohdassa [Kuluttajakaupan vuokraajan määrittäminen Commercessa](set-up-b2c-tenant.md).

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

[Dynamics 365 Commercen eristysympäristön valmistelu](provisioning-guide.md)

[Valinnaisten ominaisuuksien määrittäminen Dynamics 365 Commercen eristysympäristöä varten](cpe-optional-features.md)

[BOPIS:n määritykset Dynamics 365 Commercen eristysympäristössä](cpe-bopis.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure -portaali](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce -sivusto](https://aka.ms/Dynamics365CommerceWebsite)

[Kuluttajakaupan vuokraajan määrittäminen Commercessa](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
