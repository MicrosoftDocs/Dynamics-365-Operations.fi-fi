---
title: B2C-vuokraajan määrittäminen Commerce-sivuston luontiohjelmassa
description: Tässä artikkelissa kerrotaan, miten kuluttajakaupan vuokraaja määritetään Microsoft Dynamics 365 Commercen sivustonmuodostimessa.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 181edf1570f1a9d071a7fae38ff9d73ff3c068fa
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785260"
---
# <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>B2C-vuokraajan määrittäminen Commerce-sivuston luontiohjelmassa

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten kuluttajakaupan vuokraaja määritetään Microsoft Dynamics 365 Commercen sivustonmuodostimessa.

Kun Azure AD B2C -vuokraajan määrittäminen on tehty, B2C-vuokraaja on määritettävä Commerce-sivuston luontiohjelmassa. Määritysvaiheita ovat esimerkiksi B2C-sovelluksen tietojen kerääminen Azure-portaalista, B2C-sovelluksen tietojen syöttäminen sivuston luontiohjelmaan ja B2C-sovelluksen liittäminen sivustoon ja kanavaan.

### <a name="collect-the-required-application-information"></a>Tarvittavien sovellustietojen kerääminen

Voit kerätä tarvittavat sovellustiedot seuraavasti.

1. Siirry Azure-portaalissa kohtaan **Aloitus \> Azure AD B2C - sovellusrekisteröinnit**.
1. Valitse sovellus ja valitse sitten vasemmanpuoleisesta navigointiruudusta **Yleiskatsaus**, jos haluat hakea sovelluksen tiedot.
1. Kerää **Sovelluksen (asiakasohjelman) tunnus** -viitteestä B2C-sovelluksen tunnus, jonka B2C-vuokraaja loi. Tämä syötetään myöhemmin **Asiakasohjelman GUID** -arvona sivuston luontiohjelmaan.
1. Valitse **Uudelleenohjaa URI-osoitteet** ja kerää sivustolle näytetty vastauksen URL-osoite (määrityksen yhteydessä kirjoitettu vastauksen URL-osoite).
1. Siirry kohtaan **Aloitus \> Azure AD B2C – käyttäjän työnkulut** ja kerää sitten kunkin käyttäjän työnkulkukäytännön koko nimet.

Seuraavassa kuvassa on esimerkki **Azure AD B2C - sovellusrekisteröinnit** -yleiskuvaussivusta.

![Azure AD B2C - sovellusrekisteröinnit -yhteenvetosivu, jossa sovelluksen (asiakkaan) tunnus on korostettuna](./media/ClientGUID_Application_AzurePortal.png)

Seuraavassa kuvassa on esimerkki käyttäjän työnkulkukäytännöistä **Azure AD B2C – käyttäjän työnkulut (käytännöt)** -sivulla.

![Kaikkien B2C-käytännön työnkulun nimien kerääminen.](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>Azure AD B2C -vuokraajan sovelluksen tietojen syöttäminen Commerceen

Anna Azure AD B2C -vuokraajan tiedot Commercen sivuston luontiohjelmaan ennen B2C-vuokraajan liittämistä sivustoihin.

Voit lisätä Azure AD B2C -vuokraajan sovelluksen tiedot Commerceen seuraavasti.

1. Kirjaudu sisään järjestelmänvalvojana Commerce-sivuston luontiohjelmaan ympäristössä.
1. Laajenna se valitsemalla vasemmasta siirtymisruudusta **Vuokraajan asetukset**.
1. Valitse **Vuokraajan asetukset** -kohdasta **Sivuston todennuksen määritys**. 
1. Valitse pääikkunassa **Sivuston todennusprofiilit** -kohdan vierestä **Hallitse**. (Jos vuokraaja näkyy sivuston todennusprofiilien luettelossa, järjestelmänvalvoja on jo lisännyt sen. Tarkista, että vaiheen 6 nimikkeet vastaavat aiottua B2C-määritystä. Uuden profiilin voi luoda myös vastaavien Azure AD B2C-vuokralaisten tai sovellusten avulla, jotta voidaan ottaa huomioon pieniä eroja, kuten erilaiset käytännön tunnukset).
1. Valitse **Lisää sivuston todennusprofiili**.
1. Anna seuraavat pakolliset nimikkeet näkyvissä olevassa muodossa käyttämällä B2C-vuokraajan ja sovelluksen arvoja. Kentät, jotka eivät ole pakollisia (joissa ei ole tähteä), voidaan jättää tyhjäksi.

    - **Sovelluksen nimi**: B2C-sovelluksen nimi, esimerkiksi FABRIKAM B2C.
    - **Vuokralaisen nimi**: B2C-vuokralaisen nimi (Käytä esimerkiksi fabrikam-nimeä, jos toimialue näkyy muodossa "fabrikam.onmicrosoft.com" B2C-vuokralaiselle). 
    - **Unohdetun salasanan käytännön tunnus**: Unohdetun salasanan käyttäjän työnkulkukäytännön tunnus, esimerkiksi B2C_1_PasswordReset.
    - **SignUp SignIn -käytännön tunnus**: Rekisteröitymisen ja sisäänkirjauksen käyttäjän työnkulkukäytännön tunnus, esimerkiksi B2C_1_signup_signin.
    - **Asiakasohjelman GUID**: B2C-sovelluksen tunnus, esimerkiksi 22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6.
    - **Profiilin muokkauskäytännön tunnus**: Profiilin muokkaamisen käyttäjän työnkulkukäytännön tunnus, esimerkiksi B2C_1A_ProfileEdit.

1. Valitse **OK**. B2C-sovelluksen nimi tulee nyt näkyviin luetteloon.
1. Tallenna muutokset valitsemalla **Tallenna**.

Valinnaista **Kirjaudu mukautettuun toimialueeseen** -kenttää tulee käyttää vain, jos määrität mukautetun toimialueen Azure AD B2C-vuokraajalle. Lisätietoja **Kirjaudu mukautettuun toimialueeseen** -kentästä on kohdassa [Kuluttajakaupan lisätiedot](additional-b2c-info.md).

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>B2C-sovelluksen liittäminen sivustoon ja kanavaan

> [!WARNING]
> - Jos sivusto on jo liitetty B2C-sovellukseen, toiseen B2C-sovellukseen vaihtaminen poistaa tähän ympäristöön jo rekisteröityneiden käyttäjien nykyiset viitteet. Jos tätä muutetaan, mitkään tällä hetkellä liitetyn B2C-sovelluksen tunnistetiedot eivät ole käyttäjien käytettävissä. 
> - Päivitä vain B2C-sovellus, jos olet määrittämässä kanavan B2C-sovellusta ensimmäistä kertaa tai jos yrität saada käyttäjät rekisteröitymään uudelleen tähän kanavaan uuden B2C-sovelluksen avulla uusilla tunnistetiedoilla. Ole varovainen, kun liität kanavia B2C-sovelluksiin. Anna sovelluksille selkeät nimet. Jos kanavaa ei ole liitetty B2C-sovellukseen alla kuvattujen vaiheiden avulla, kanavaan kirjautuvat käyttäjät siirretään B2C-sovellukseen, joka on **oletussovellus** B2C-sovellusten **Vuokraajan asetukset \> B2C-asetukset** -luettelossa.

Voit liittää B2C-sovelluksen sivustoon ja kanavaan seuraavasti.

1. Siirry sivustoon Commerce-sivuston luontiohjelmassa.
1. Laajenna se valitsemalla vasemmasta siirtymisruudusta **Sivuston asetukset**.
1. Valitse **Sivuston asetukset** -kohdassa **Kanavat**.
1. Valitse pääikkunassa **Kanavat**-kohdassa kanava.
1. Valitse oikeanpuoleisessa kanavan ominaisuuksien ruudussa B2C-sovelluksen nimi avattavasta **Valitse B2C-sovellus** -luettelosta.
1. Valitse **Sulje** ja valitse sitten **Tallenna ja julkaise**.

## <a name="next-steps"></a>Seuraavat vaiheet

Jos haluat jatkaa kuluttajakaupan vuokraajan määrittämisprosessia Commercessa, jatka [Kuluttajakaupan lisätiedot](additional-b2c-info.md) -kohtaan.

## <a name="additional-resources"></a>Lisäresurssit

[B2C-vuokraajan määrittäminen Commercessa](set-up-b2c-tenant.md)

[Olemassa olevan Azure AD:n kuluttajakaupan vuokraajan luominen tai linkittäminen Azure-portaalissa](create-link-aad-b2c-tenant.md)

[B2C-sovelluksen luominen](create-b2c-app.md)

[Käyttäjän työnkulkukäytäntöjen luominen](create-user-flow-policies.md)

[Yhteisöpalvelun tunnistetietojen tarjoajien lisääminen (valinnainen)](add-social-identity-providers.md)

[Commerce headquartersin päivittäminen uusilla Azure AD:n kuluttajakaupan tiedoilla](update-hq-aad-b2c-info.md)

[B2C-lisätiedot](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
