---
title: Sähköisen kaupankäynnin sivuston luominen
description: Tämä artikkeli sisältää ohjeet ja tiedot, jotka tarvitaan uuden sähköisen kaupankäynnin sivun luomiseen Dynamics 365 Commerce sivustonmuodostimessa.
author: bicyclingfool
ms.date: 03/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: ea9afd89ce9ff79edbe5bff609b9843026005493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270234"
---
# <a name="create-an-e-commerce-site"></a>Sähköisen kaupankäynnin sivuston luominen

[!include [banner](includes/banner.md)]

Tämä artikkeli sisältää ohjeet ja tiedot, jotka tarvitaan uuden sähköisen kaupankäynnin sivun luomiseen Dynamics 365 Commerce sivustonmuodostimessa.

Kun lisensoit Dynamics 365 Commercen ominaisuuksia, sivuston luontiohjelmalle valmistellaan aloitussivusto, jota voit käyttää oman sivustosi pohjana. Jos kuitenkin haluat tehdä kaiken alusta tai jos haluat luoda toisen sivuston, sinun on luotava uusi sivusto sivuston muokkausympäristössä. 

## <a name="site-creation-prerequisites"></a>Sivuston luonnin edellytykset

Sivustonmuodostajan käyttäjän on omattava Microsoft Azure Active Directory (Azure AD) -käyttäjätili, joka sisältyy Azure AD -suojausryhmään, joka on määritetty sähköisen kaupankäynnin järjestelmänvalvojille. Lisätietoja on kohdassa [Uuden sähköisen kaupankäynnin vuokraajan käyttöönottaminen](deploy-ecommerce-site.md).

> [!NOTE]
> Azure AD -vieraskäyttäjillä voi olla eri käyttöoikeudet Azure AD -vuokraajassasi. Vaikka sisältyisikin sähköisen kaupan järjestelmänvalvojille määritettyyn Azure AD -suojausryhmään, vieraskäyttäjän on ehkä muutettava Azure AD:n **Ulkoiset käyttäjät** -käyttöoikeusasetuksia, jotta verkkokauppasivusto voidaan luoda Commercessa. 

Voit muokata Azure AD:n **ulkoisten käyttäjien** asetuksia noudattamalla seuraavia ohjeita.

1. Siirry Azure-portaalissa Azure AD -vuokraajaan.
1. Siirry kohtaan **Käyttäjäasetukset \> Ulkoiset käyttäjät** ja valitse **Ulkoisen yhteistyön asetusten hallinta** -linkki. Tämä avaa **Ulkoisen yhteistyön asetukset** -sivun, jossa voidaan määrittää vieraan käyttöoikeudet, vieraan kutsua koskevat asetukset ja yhteiskäytön rajoitukset. 
1. Muuta ulkoisen yhteiskäytön asetukset yrityksen suojauskäytäntöjen mukaan. 

## <a name="set-up-your-site"></a>Sivuston määrittäminen

Määritä sivusto seuraavasti.

1. Avaa sivustonmuodostimen ympäristö. Löydät linkin sivustonmuodostimeen Microsoft Lifecycle Servicesin (LCS) ympäristöominaisuuksien sivulta.
1. Valitse sivuston muokkausympäristön aloitussivulla **Uusi sivusto**.
1. Anna seuraavat tiedot **Uusi sivusto** -valintaikkunaan.

| Kenttä                               | Kuvaus |
|-------------------------------------|-------------|
| Sivuston nimi                           | Anna näyttönimi, jota käytetään sivuston muokkausympäristön sivustossa. Tämä nimi näkyy vain muokkausympäristössä. Se ei näy asiakkaille. |
| Sivuston järjestelmänvalvojan käyttöoikeusryhmä | Määritä Microsoft Azure Active Directory (Azure AD) -käyttöoikeusryhmä. Se hallitsee käyttäjiä, joilla on tämän sivuston järjestelmänvalvojan rooli. |
| Oletuskanava (toimintayksikön numero) | Valitse verkkomyymälä, jonka verkkomyymälä tämä sivusto on. Jos haluat, että sähköisen kaupankäynnin sivusto tukee useita verkkomyymälöitä, liitä myymälät sivustoon **Sivuston asetukset** -kohdassa sivuston määrityksen jälkeen. |
| Oletuskieli                            | Määritä tämän verkkomyymälän ja -markkinan oletuskieli. Verkkomyymälä voi tukea useita kieliä. Jos haluat, että tämä verkkomyymälä tai toinen verkkomyymälä tukee useita kieliä, määritä tuki **Sivuston asetukset** -kohdassa sivuston määrityksen jälkeen.  |
| Toimialue                              | Valitse toimialueen nimi, joka toimii tämän verkkomyymälän toimialueena. Jos et ole määrittänyt toimialueita LCS:ssä, voit jättää tämän kentän tyhjäksi. Kun toimialue on määritetty LCS:ssä, lisää se verkkomyymälään **Sivuston asetukset** -kohdassa.  |
| Polku                              | Kun sivusto tukee useita kieliä tietyssä toimialueessa, käytä polkukenttää ja luo yksilöivä sivuston URL-osoite kyseiselle toimialueelle ja kielen yhdistelmälle. Jos **Oletuskieli**-kentässä määritetty kieli on ainoa kieli, jota tuetaan tässä toimialueessa, tai jos se on oletuskieli sen jälkeen kun sivusto on lokalisoitu muille kielille, suosittelemme, että tämä kenttä jätetään tyhjäksi. |

Kun sivusto on luotu, voit varmistaa, että se on liitetty verkkomyymälään, valitsemalla **Tuotteet**-välilehden. Näkyvissä on tuotevalikoima, joka on määritetty verkkomyymälälle. Voit käyttää avattavaa valikkoa sivun vasemmassa yläosassa, jos haluat käyttää kohdistettuja tuotteita luokan mukaan.

## <a name="rename-your-site"></a>Sivuston nimeäminen uudelleen

Voit nimetä sivuston uudelleen sivuston muodostimessa seuraavasti.

1. Voit avata sivustoluettelonäkymän valitsemalla oikeasta yläkulmasta **Sivuston valitsin** ja valitsemalla sitten **Sivustojen hallinta**. 
1. Valitse uudelleennimettävän sivuston vieressä valintaruutu ja valitse sitten komentopalkissa **Nimeä uudelleen**.
1. Kirjoita **Uusi sivuston nimi** -valintaikkunaan sivuston uusi nimi ja valitse sitten **OK**. Sivustoluettelo päivittyy niin, että se näyttää sivuston uuden nimen.

## <a name="delete-a-site"></a>Poista sivusto

Voit poistaa sivuston sivuston muodostimessa seuraavasti.

1. Voit avata sivustoluettelonäkymän valitsemalla oikeasta yläkulmasta **Sivuston valitsin** ja valitsemalla sitten **Sivustojen hallinta**.
1. Valitse poistettava sivusto ja valitse sitten komentopalkissa **Poista**.
1. Kirjoita **Poista \<site name\>** -valintaikkunaan sivuston uusi nimi ja valitse sitten **Poista**.

## <a name="additional-resources"></a>Lisäresurssit

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto](deploy-ecommerce-site.md)

[Dynamics 365 Commerce -sivuston liittäminen online-kanavaan](associate-site-online-store.md)

[Robots.txt-tiedostojen hallinta](manage-robots-txt-files.md)

[URL-uudelleenohjausten joukkolataus palveluun](upload-bulk-redirects.md)

[B2C-vuokraajan määrittäminen Commercessa](set-up-B2C-tenant.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)

[Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä](configure-multi-B2C-tenants.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
